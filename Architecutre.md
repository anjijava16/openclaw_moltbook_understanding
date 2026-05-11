**OpenClaw Architecture Deep Dive (2026)**

OpenClaw is a **self-hosted, local-first AI agent gateway** and runtime. It acts as a persistent bridge between messaging channels (Telegram, WhatsApp, Discord, Slack, etc.), an LLM-powered agent runtime, tools/skills, and persistent memory. It follows a **hub-and-spoke model** with a single long-lived **Gateway** as the central control plane.

### 1. High-Level Architecture (Hub-and-Spoke)

- **Gateway (Control Plane)**: Single Node.js daemon (default port 18789, binds to `127.0.0.1` for security). It is the "single source of truth" for sessions, routing, channel connections, queuing, and state.
- **Channels (Spokes)**: Adapters normalize messages from platforms (WhatsApp via Baileys, Telegram via grammY, Discord, Slack, Signal, iMessage, etc.). Multiple channels run simultaneously.
- **Clients & Nodes**: WebSocket connections for control (CLI, Dashboard, macOS app) and extended capabilities (Nodes provide camera, screen, canvas, etc.).
- **Agent Runtime**: Executes the core agentic loop (independent of specific LLMs).
- **Workspace & Memory**: File-system-based "brain" for configuration, long-term memory, and context.
- **Tools/Skills**: Dynamic capabilities loaded from ClawHub or local files.

The Gateway owns everything; agents are channel-agnostic. One Gateway per host.

### 2. Core Components

- **Gateway Daemon**:
  - WebSocket server with typed protocol (TypeBox + JSON Schema).
  - Handles authentication, pairing, idempotency, retry policies.
  - Emits events: `agent`, `chat`, `presence`, `health`, `heartbeat`, `cron`.
  - Manages command/steering queues for serialized execution (prevents conflicts; lanes per session).
  - HTTP APIs (OpenAI-compatible endpoints for compatibility).

- **Agent Runtime**:
  - Model-agnostic (Claude, GPT, Gemini, Ollama, etc.).
  - Runs the **agent loop** (see below).
  - Uses Pi Agent Core or similar for orchestration.

- **Memory System** (Multi-tier):
  - Short-term: Conversation history in sessions.
  - Long-term: `MEMORY.md`, curated facts, vector stores (SQLite/LanceDB).
  - Episodic: Daily logs (`memory/YYYY-MM-DD.md`), heartbeat distillation.
  - Workspace files (`.md` files) injected into prompts.

- **Prompt Assembly / Context Engine**:
  - Builds system prompt from workspace bootstrap files (`AGENTS.md`, `SOUL.md`, `USER.md`, `MEMORY.md`, `HEARTBEAT.md`, skills, etc.).
  - Context management, compaction, and optimization.

- **Tools & Skills**:
  - Built-in + dynamic from `SKILL.md` files.
  - Sandboxing support (Docker or similar) for safe execution.
  - Filesystem, browser (Playwright), shell, etc.

### 3. Key Flows

**Inbound Message Flow (User Chat to Agent)**:
1. Message arrives via Channel Adapter (normalized: text, attachments, metadata).
2. Gateway routes it → Resolves session/agent (per sender/conversation).
3. Queued (command queue ensures serialization; one active run per session/lane).
4. Agent Runtime starts the **agent loop**.
5. Response streamed back through the originating channel (or multiple).

**Agent Loop (Core Execution Cycle)**:
This is the "observe-decide-act" heart of OpenClaw:
1. **Context Assembly**: Build full prompt (system + history + bootstrap files + skills + recent memory + current message).
2. **LLM Inference**: Send to model (with tool schemas).
3. **Tool Calls** (if any): Execute in sandbox → Feed results back into loop (multi-turn tool use until final answer).
4. **Streaming Response**: Partial outputs sent back in real-time (progress drafts, thinking steps).
5. **Persistence**: Update session transcript, memory distillation, logs.
6. **End Loop**: Final reply delivered; state saved.

Loops are serialized per session for reliability. Heartbeats/cron run background tasks (self-review, memory curation).

**Outbound / Proactive Flows**:
- Heartbeat (periodic self-improvement).
- Cron/scheduled jobs.
- Tool-initiated actions (e.g., agent sends message, creates file).
- Steering queue for follow-ups.

**Multi-Agent / Routing**:
- Rules-based or skill-driven routing to specialized agents.
- Shared or per-agent workspaces/sessions.

### 4. User Chat Flows (End-to-End Experience)

**Typical User Interaction**:
1. User sends message on Telegram/WhatsApp/etc. (or Dashboard/WebChat/CLI).
2. Gateway receives → Pairing/allowlist check (if new sender).
3. Message routed to session → Agent loop triggered.
4. Agent "thinks" (streams reasoning if enabled) → Decides on tools or direct reply.
5. Tools execute (with approvals for sensitive actions).
6. Response appears in the same chat thread.
7. Conversation history persists across restarts and channels.

**Special Features in Chat**:
- Slash commands (`/new` for fresh session).
- `@mention` required in groups.
- Multi-modal (images, files).
- Human-in-the-loop approvals for risky actions.
- Persistent memory across chats (agent remembers preferences).

**Session Management**:
- Per-sender or per-group.
- Compaction for long histories.
- `/new` resets context while keeping long-term memory.

### 5. Invariants & Design Philosophy
- **Local-first & Privacy**: Everything runs on your hardware; no cloud dependency for core operation.
- **Serialization**: One active agent run per session to avoid race conditions.
- **Extensibility**: Markdown-as-config (workspace files), skills via ClawHub, plugins.
- **Security Boundary**: Gateway + sandbox + pairing/approvals (detailed in previous response).

For the most authoritative details, refer to:
- Official Docs: [docs.openclaw.ai/concepts/architecture](https://docs.openclaw.ai/concepts/architecture) and [agent-loop](https://docs.openclaw.ai/concepts/agent-loop).
- Source/GitHub for internals.

This architecture makes OpenClaw feel like a personal Jarvis: always-on, multi-channel, tool-using, and memory-persistent. 

Let me know if you want diagrams (text-based), a specific sub-component (e.g., memory, queue, sandbox), code-level details, or comparisons to other frameworks!
