# openclaw_moltbook_understanding



Alright, here’s the **full deep architecture flow** of an OpenClaw-style agent system—covering **CLI, runtime, memory, skills, gateway, tools, and execution loop** in one unified model.

This is the *realistic production-style design* used by most modern agent frameworks (LangChain-like, AutoGPT-like, agent runtimes).


**OpenClaw Deep Dive: Architecture, Services, and Complete File System**

OpenClaw is a **self-hosted, open-source AI agent gateway** and runtime. It turns LLMs (Claude, GPT, Gemini, local models) into a persistent, tool-using personal assistant accessible via messaging apps. It runs as a long-lived daemon on your machine/VPS and emphasizes privacy, multi-channel support, memory persistence, and extensibility via skills.

### High-Level Architecture (Hub-and-Spoke Model)
- **Messaging Surfaces** (Channels) → **Gateway (Control Plane)** → **Agent Runtime** → **LLM Providers** + **Tools/Skills**.
- **Gateway**: Central nervous system (Node.js daemon). Handles all connections, routing, sessions, queuing, and security. Runs on port **18789** (default: localhost).
- **Agent Runtime**: Executes the agentic loop (prompt assembly → LLM call → tool execution → repeat until final response). Uses workspace files for context.
- **Key Flows**:
  1. Inbound message from any channel.
  2. Normalized by channel adapter → Session resolution → Command queue.
  3. Agent assembles prompt (bootstrap files + skills + tools + memory).
  4. LLM inference + tool calls (sandboxed where possible).
  5. Response streamed back; state persisted.

**Core Services/Components**:
- **Gateway Daemon**: Persistent process managing everything. Supports WebSocket clients (CLI, dashboard, nodes), cron/heartbeat, hooks, and pairing.
- **Channel Adapters**: WhatsApp (Baileys), Telegram (grammY), Discord, Slack, Signal, iMessage, WebChat, etc. One Gateway owns all sessions.
- **Session Manager**: Persists conversations (transcripts, metadata). Supports DM vs. group policies, compaction.
- **Command/Agent Queue**: Prevents conflicts with lanes (global, per-session, cron). Modes like `collect`, `steer`.
- **Memory System**: File-based + vector (SQLite/LanceDB). Includes daily logs, curated MEMORY.md, and heartbeat distillation.
- **Skills Loader**: Dynamically loads SKILL.md instructions/tools.
- **Tool Execution**: Built-in (filesystem, bash, browser/Playwright, etc.) + skill-provided. Sandboxing option.
- **Prompt Assembly/Context Engine**: Builds dynamic system prompt from workspace files + metadata.
- **Dashboard/Web UI + Nodes**: Browser control, mobile/desktop nodes for extra capabilities (canvas, camera, etc.).
- **Plugins/Extensibility**: Provider plugins (LLMs), channel plugins, skills via ClawHub.

### Complete File System Overview
OpenClaw uses two primary root areas:

1. **`~/.openclaw/`** — State, config, secrets, sessions (do **not** commit to git).
2. **`~/.openclaw/workspace/`** (default; configurable) — Agent's "brain" and working directory (treat as private memory; git backup recommended).

#### Detailed Directory Structure

**`~/.openclaw/` (State Directory)**:
- `openclaw.json` — Main config (JSON5; models, workspace path, channels, auth, sandbox, etc.).
- `credentials/` — Secure tokens, WhatsApp sessions, OAuth (0600 permissions).
- `agents/<agentId>/` — Per-agent data:
  - `sessions/` — Transcripts (.jsonl), sessions.json.
  - `agent/` — Auth profiles, codex-home (runtime state).
- `skills/` — Globally managed/installed skills.
- `sessions/` — Shared or legacy session data.
- `logs/`, caches, memory vector stores (e.g., SQLite/LanceDB per agent).
- `sandboxes/` (if enabled) — Isolated execution environments.

**`~/.openclaw/workspace/` (Agent Workspace — Most Important)**:
This is the default cwd for tools and context loading. Markdown files here are injected into the system prompt.

Key files (bootstrap files):
- **AGENTS.md** — Core operating instructions, rules, priorities, tool usage.
- **SOUL.md** — Personality, tone, boundaries.
- **USER.md** / **IDENTITY.md** — User profile and agent self-description (name, vibe, emoji).
- **TOOLS.md** — Local tool conventions/guidance.
- **MEMORY.md** — Curated long-term memory (facts, preferences).
- **HEARTBEAT.md** — Periodic self-review checklist.
- **BOOT.md** / **BOOTSTRAP.md** — Startup/first-run rituals.
- `memory/YYYY-MM-DD.md` — Daily logs (auto-managed).
- `skills/` — Workspace-specific skills (highest precedence).
- `canvas/` — UI files for visual outputs.
- Project folders, documents, outputs the agent creates.

**Skills Locations** (Precedence: workspace > global > bundled):
- Workspace: `~/.openclaw/workspace/skills/<name>/` (with SKILL.md).
- Global: `~/.openclaw/skills/`.
- Bundled/installed via `openclaw skills` or ClawHub.

**Other Notes on Filesystem**:
- Not a hard sandbox by default (agent can access absolute paths unless restricted).
- Git-init often auto-done on workspace for backup.
- Configurable workspace path in `openclaw.json`.
- Sensitive data stays in `~/.openclaw/` (never in workspace).

### Advanced Topics
- **Security**: Pairing/approvals, allowlists, sandboxing, token auth, no public exposure (use localhost + SSH/Tailscale).
- **Multi-Agent**: Possible via routing rules and per-agent workspaces.
- **Heartbeat/Cron**: Background self-improvement and scheduled tasks.
- **Scaling**: Runs on laptop, VPS, or Docker. Nodes add device capabilities.

For the absolute latest/official details, visit:
- **Docs**: https://docs.openclaw.ai/ (especially `/concepts/architecture`, `/concepts/agent-workspace`, `/tools/skills`).
- **ClawHub**: https://clawhub.ai for skills.
- GitHub: Search openclaw/openclaw.

This covers the full system as of 2026. If you want a sample workspace tree visualization, config examples, specific component deep-dive (e.g., memory, sandboxing), or help customizing files, let me know!

# 🧠 FULL SYSTEM ARCHITECTURE (DEEP VIEW)

## 🧩 1. High-level system map

```text
                ┌──────────────────────┐
                │        CLI           │
                │  openclaw command    │
                └─────────┬────────────┘
                          │
                          ▼
        ┌────────────────────────────────────┐
        │        AGENT RUNTIME CORE          │
        │                                    │
        │  ┌───────────────┐                │
        │  │  Orchestrator │  ← main brain  │
        │  └──────┬────────┘                │
        │         │                         │
        │         ▼                         │
        │  ┌───────────────┐               │
        │  │ Agent Loop    │               │
        │  │ (think-act)   │               │
        │  └──────┬────────┘               │
        │         │                        │
        │   ┌─────┴─────────────┐         │
        │   ▼                   ▼         │
        │ Memory Manager    Skill Loader   │
        │ (short/long term)  (tools/plugins)│
        │   │                   │         │
        │   ▼                   ▼         │
        │ Vector DB        Tool Registry    │
        └──────────┬────────────────────────┘
                   │
      ┌────────────┼────────────────┐
      ▼            ▼                ▼
 Gateway API   Tool Executors   External APIs
 (optional)    (runtime tasks)  (web/files/etc)
```

---

# 🔁 2. Execution flow (step-by-step runtime cycle)

This is what happens when you type a command:

```text
USER INPUT
   │
   ▼
CLI parses command
   │
   ▼
Agent Runtime starts (if not running)
   │
   ▼
────────────────────────────────────────
1. CONTEXT BUILD PHASE
────────────────────────────────────────
   │
   ├── Load session memory (RAM)
   ├── Fetch persistent memory (disk)
   ├── Query vector DB (semantic memory)
   └── Inject into prompt context
   │
   ▼
────────────────────────────────────────
2. AGENT LOOP (core reasoning cycle)
────────────────────────────────────────
   │
   ├── LLM reasoning step
   │
   ├── Decide:
   │     ├── respond directly
   │     └── OR call a tool
   │
   ▼
────────────────────────────────────────
3. TOOL / SKILL EXECUTION
────────────────────────────────────────
   │
   ├── Skill Loader finds tool
   ├── Lazy-load module if needed
   ├── Execute tool runtime
   └── Return result
   │
   ▼
────────────────────────────────────────
4. MEMORY UPDATE
────────────────────────────────────────
   │
   ├── Store short-term state
   ├── Optionally persist long-term memory
   ├── Embed + store vectors (if enabled)
   │
   ▼
────────────────────────────────────────
5. FINAL RESPONSE
────────────────────────────────────────
   │
   └── Output to CLI / Gateway / UI
```

---

# 🧠 3. Memory system (deep breakdown)

## 🔵 A. Runtime Memory (Ephemeral)

Lives in:

```text
AgentProcess.memory.session
```

Contains:

* current conversation
* tool outputs
* working state

⚡ dies when process ends

---

## 🟡 B. Persistent Memory (Disk)

Stored in:

```text
~/.openclaw/memory/
```

Typical structure:

```text
memory/
 ├── conversations.json
 ├── facts.json
 ├── events.log
 └── embeddings.db
```

Often backed by:

* SQLite
* or vector DB (FAISS/Chroma-style)

---

## 🟣 C. Semantic Memory (Vector layer)

Flow:

```text
User Query
   ↓
Embed query
   ↓
Vector search
   ↓
Top-K relevant memories
   ↓
Injected into prompt
```

---

# 🧰 4. Skills / Tools system (deep breakdown)

## 📦 Skill Registry

At startup:

```text
SkillLoader.scan()
```

Sources:

* built-in skills
* user-installed skills
* project skills

---

## 🧾 Skill structure

```json
{
  "name": "browser",
  "type": "tool",
  "entry": "browser.js",
  "schema": {
    "input": {},
    "output": {}
  }
}
```

---

## ⚙️ Execution flow

```text
Agent decides tool call
   ↓
Skill Registry lookup
   ↓
Lazy load module
   ↓
Spawn executor
   ↓
Return result
```

---

# 🌐 5. Gateway layer (optional)

Only exists if enabled:

```text
openclaw serve
```

Creates:

```text
HTTP Server (localhost)
   │
   ├── REST API
   ├── WebSocket stream
   └── UI bridge
```

Used for:

* dashboards
* remote control
* multi-agent orchestration

---

# ⚙️ 6. Agent Loop (core brain)

This is the heart:

```text
WHILE task not complete:

    1. Observe state
    2. Think (LLM call)
    3. Decide action
        ├── respond
        └── tool call
    4. Execute
    5. Update memory
```

This is sometimes called:

* ReAct loop (Reason + Act)
* planning-execution loop
* autonomous agent cycle

---

# 🧱 7. Full module map (summary)

```text
openclaw/
│
├── cli/
│   └── command parser
│
├── runtime/
│   ├── orchestrator
│   ├── agent_loop
│   ├── executor
│
├── memory/
│   ├── session_memory
│   ├── persistence
│   ├── vector_store
│
├── skills/
│   ├── loader
│   ├── registry
│   └── tool_modules/
│
├── gateway/ (optional)
│   ├── api_server
│   └── websocket
│
└── config/
    └── settings.yaml
```

---

# ⚠️ Key mental model (important)

Think of it like this:

* **CLI** = keyboard
* **Runtime** = CPU brain
* **Memory** = RAM + hard drive
* **Skills** = plugins/tools
* **Gateway** = network interface
* **Agent Loop** = decision engine

---

# 🔥 Bottom line

* No always-running heavy services by default
* Memory = layered (session + disk + vector)
* Skills = lazy-loaded plugins
* Gateway = optional server
* Core = agent loop inside runtime

---

# OpenClaw (killowclaw File System)

Based on the images provided, here is the complete file structure for the **openclaw** system:

### `/ROOT/.OPENCLAW`
*   **agents/**
    *   **main/**
        *   **agent/**
            *   `auth-profiles.json`
            *   `auth-state.json`
            *   `models.json`
        *   **sessions/**
            *   `62021f24-c182-425e-...`
            *   `666692df-bbaf-4c00-...`
            *   `b28d134f-481d-4b6c-...`
            *   `sessions.json`
*   **canvas/**
    *   `index.html`
*   **devices/**
    *   `paired.json`
    *   `pending.json`
*   **flows/**
    *   `registry.sqlite`
    *   `registry.sqlite-shm`
    *   `registry.sqlite-wal`
*   **identity/**
    *   `device.json`
*   **logs/**
    *   `commands.log`
    *   `config-audit.jsonl`
    *   `config-health.json`
*   **memory/**
    *   `main.sqlite`
*   **morning-briefing/**
    *   **briefings/**
*   **tasks/**
    *   `runs.sqlite`
    *   `runs.sqlite-shm`
    *   `runs.sqlite-wal`

---

### `/workspace`
*   **.git/**
*   **.openclaw/**
    *   `workspace-state.json`
*   **memory/**
    *   `2026-04-29-usa-news.md`
*   **state/**
*   `AGENTS.md`
*   `HEARTBEAT.md`
*   `IDENTITY.md`
*   `SOUL.md`
*   `TOOLS.md`
*   `USER.md`

---

### Root Configuration Files
*   `exec-approvals.json`
*   `openclaw.json`
*   `openclaw.json.bak`


Good — this is now enough structure to reconstruct a **real internal architecture model**. I’ll go *below filesystem level* and map:

* runtime services
* memory layers
* skill system
* agent loop execution
* flows/tasks engine
* identity/auth system
* how everything actually connects

---

# 🧠 0. MASTER ARCHITECTURE (what your tree represents)

Your filesystem is basically 6 subsystems:

```text id="coremap"
OPENCLAW SYSTEM
│
├── 1. Identity & Auth Layer
├── 2. Agent Runtime Layer
├── 3. Memory Layer (short + long term)
├── 4. Flow / Task Engine
├── 5. Device + Sync Layer
├── 6. Workspace (project + state + tools)
```

Now let’s go **deep inside each one**.

---

# 🔐 1. IDENTITY & AUTH LAYER

### 📍 Location

```text id="idlayer"
/.openclaw/identity/
agents/main/agent/auth-*.json
devices/
```

---

## 🧾 Files meaning

### `device.json`

Represents:

* machine fingerprint
* install identity
* local node ID

➡️ Think: “this computer is a known node in the system”

---

### `auth-profiles.json`

Stores:

* user accounts / roles
* permissions
* API tokens

---

### `auth-state.json`

Stores:

* current login session
* active user context
* token expiry state

---

### `devices/paired.json`

* trusted devices list
* remote agents allowed

---

## 🔥 Deep behavior

This layer feeds:

```text id="authflow"
CLI → Auth check → Agent Runtime permission gate → Tool access control
```

So before ANY tool runs:
✔ identity checked
✔ permissions validated
✔ device verified

---

# 🧠 2. AGENT RUNTIME LAYER (CORE BRAIN)

### 📍 Location

```text id="runtime"
agents/main/agent/
```

### Key file:

* `models.json`

This defines:

* LLM providers
* model routing
* fallback chains

---

## 🧩 Runtime internal modules

Even if not shown as files, this maps to:

```text id="runtime2"
AgentRuntime/
 ├── Orchestrator
 ├── Context Builder
 ├── Model Router
 ├── Tool Dispatcher
 └── Response Generator
```

---

## 🧠 What happens here

Every request becomes:

```text id="flow1"
INPUT
 → load model config
 → build context (memory + workspace + sessions)
 → call LLM
 → interpret tool calls
 → execute skills
 → return output
```

---

# 🧠 3. MEMORY LAYER (MOST IMPORTANT)

### 📍 Location

```text id="memroot"
/.openclaw/memory/main.sqlite
/workspace/memory/*.md
```

---

## 🟡 A. Structured memory (SQLite)

`main.sqlite` stores:

* facts
* embeddings
* conversation history
* agent decisions
* tool outputs

### Schema (typical internal)

```text id="schema"
MEMORY_TABLES:
  - conversations
  - facts
  - embeddings
  - events
  - tool_outputs
```

---

## 🟢 B. Workspace memory (human-readable)

```text id="wsmem"
/workspace/memory/*.md
```

Example:

* `2026-04-29-usa-news.md`

This is:

* long-term curated memory
* human-editable context
* semantic notes

---

## 🔵 C. Session memory

```text id="sessionmem"
agents/main/sessions/{uuid}/
sessions.json
```

This is:

* active runtime state
* temporary context
* per-task working memory

---

## 🔥 MEMORY FLOW

```text id="memflow"
User input
   ↓
Session memory (RAM-like)
   ↓
SQLite memory (facts + embeddings)
   ↓
Workspace markdown memory
   ↓
Injected into LLM prompt
```

---

# ⚙️ 4. FLOW / TASK ENGINE (VERY IMPORTANT)

### 📍 Location

```text id="flowsys"
flows/registry.sqlite
tasks/runs.sqlite
```

---

## 🧠 What this is

This is your:

> **workflow execution system**

It replaces simple “agent loops” with structured DAGs or pipelines.

---

## 📦 flows/registry.sqlite

Stores:

* workflow definitions
* automation graphs
* multi-step agent plans

Example concept:

```text id="flowdef"
FLOW: "research_task"
  step1 → search
  step2 → summarize
  step3 → store memory
```

---

## 🧾 tasks/runs.sqlite

Stores:

* executed runs
* task state
* retries
* failures
* timestamps

---

## 🔥 Execution model

```text id="taskflow"
CLI command
   ↓
Flow Registry lookup
   ↓
Create task run
   ↓
Execute steps sequentially or DAG
   ↓
Store result in runs.sqlite
```

---

# 🧠 5. AGENT LOOP (hidden inside runtime)

Not stored as files — lives in runtime binary.

```text id="loop"
WHILE task not done:

  1. Load context
  2. Call LLM (model.json)
  3. Parse tool calls
  4. Dispatch skills
  5. Update memory.sqlite
  6. Update task state
```

---

# 🧰 6. SKILL / TOOL SYSTEM

### 📍 Location (implicit)

Not explicitly shown, but inferred:

```text id="skills"
runtime/tools/
workspace/TOOLS.md
```

---

## 🧾 TOOLS.md = skill registry spec

Defines:

* available tools
* schemas
* permissions
* execution rules

---

## 🔥 Tool execution pipeline

```text id="toolpipe"
Agent decides tool
   ↓
Check TOOLS.md schema
   ↓
Validate exec-approvals.json
   ↓
Run tool
   ↓
Log to logs/commands.log
```

---

# 🖥️ 7. WORKSPACE LAYER (USER ENVIRONMENT)

### 📍 Location

```text id="workspace"
/workspace/
```

---

## 🧠 Meaning

This is:

* project memory
* persistent agent state
* shared context between runs

---

## Key files

### `AGENTS.md`

* defines agent roles
* behavior rules

### `USER.md`

* user profile context
* preferences

### `SOUL.md`

* system personality / core instructions

### `IDENTITY.md`

* workspace identity binding

### `HEARTBEAT.md`

* liveness / sync signal

---

## 🔥 This layer feeds:

```text id="wsflow"
Workspace → Context Builder → LLM prompt injection
```

---

# 🌐 8. DEVICE + SYNC SYSTEM

### 📍 Location

```text id="device"
devices/
```

---

## Purpose

Multi-device coordination:

* paired machines
* pending sync
* distributed agents

---

## Flow

```text id="syncflow"
Device A writes state
   ↓
paired.json updates
   ↓
Device B pulls updates
   ↓
Sync into workspace + memory
```

---

# 📊 9. LOGGING / OBSERVABILITY LAYER

### 📍 Location

```text id="logs"
logs/
```

Contains:

* command logs
* config changes
* health metrics

---

## Purpose

Used for:

* debugging agent decisions
* replaying runs
* auditing tool usage

---

# 🔥 FINAL SYSTEM MAP (COMPLETE)

```text id="fullmap"
                CLI
                 │
                 ▼
        ┌───────────────────┐
        │ Identity Layer    │
        └────────┬──────────┘
                 │
                 ▼
        ┌───────────────────┐
        │ Agent Runtime     │
        │ (LLM Orchestrator)│
        └───────┬───────────┘
                │
   ┌────────────┼────────────┐
   ▼            ▼            ▼
Memory DB   Skill System   Flow Engine
(SQLite)    (TOOLS.md)     (registry.sqlite)
   │            │            │
   └──────┬─────┴─────┬─────┘
          ▼           ▼
     Workspace     Task Runs
     (MD files)    (runs.sqlite)
          │
          ▼
      Output / CLI / Gateway
```

---

# ⚠️ KEY INSIGHT (IMPORTANT)

This system is NOT:

* a single app
* a single agent
* or a single process

It is:

> a **distributed stateful agent OS layered on filesystem + SQLite + runtime orchestrator**

---

# If you want next level deeper

I can break it further into:

### 🔬 1. exact SQLite schema reverse engineering

### 🔬 2. agent prompt construction (token-level injection order)

### 🔬 3. tool execution sandboxing model

### 🔬 4. how flows become DAG execution graphs

### 🔬 5. how memory embeddings are generated + retrieved

Just tell me which layer you want to go into.


# Login Access from (Kilo claw)

1. https://app.kilo.ai/claw/chat
2. https://claw.kilosessions.ai/chat?session=agent%3Amain%3Amain
3. https://abvijaykumar.medium.com/openclaw-a-deep-agent-realization-14125bbd5bad


<img width="1400" height="984" alt="image" src="https://github.com/user-attachments/assets/63845677-a186-4377-9ff1-b1c1db0505bd" />



<img width="1728" height="1000" alt="image" src="https://github.com/user-attachments/assets/93d15c99-d3f2-48fc-87d5-50259a68d67f" />


<img width="4800" height="2808" alt="image" src="https://github.com/user-attachments/assets/9b5e26f1-42b8-4e0c-8e20-b9b8573f89f4" />


# References
## Moltbook
1. A Reddit-style social network launched on 29 January 2026
2. Unusual restriction: only AI agents can post. 
3. "Humans welcome to observe." 
4. Moderation by AI assistant "Clawd Clawderberg."
1. https://www.moltbook.com/m/antifragile
2. https://www.moltbook.com/skill.md
3. https://www.moltbook.com/post/4ca8b78f-e8cd-4626-8760-52b5d217f7b3

## Openclaw
1. https://openclaw.ai/
2. https://docs.openclaw.ai/start/getting-started
3. https://openclaw.ai/blog/introducing-openclaw


https://clawhub.ai/

kilo.codes/cs2

https://clawshop2-9533.d.kiloapps.io/?utm_source=guide&utm_medium=qr&utm_campaign=clawshop

https://clawhub.ai/spiceman161/playwright-mcp

https://claw.kilosessions.ai/chat?session=agent%3Amain%3Amain

https://docs.openclaw.ai/


```

Feature,OpenClaw (Self-Hosted),KiloClaw (Managed)
License,Open Source (Free),Commercial / Subscription
Privacy,High (Runs on your iron),Medium (Cloud-hosted isolation)
Complexity,High (Requires CLI/Node.js),Low (Dashboard-based setup)
Best For,Developers/Privacy enthusiasts,Production-grade 24/7 agents

```
