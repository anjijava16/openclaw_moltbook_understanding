# Openclaw FS


```

welcome@jaisairams-Laptop workspace %  ls -ltr ~/.openclaw
total 72
drwxr-xr-x   3 welcome  staff    96 May  2 16:53 plugin-runtime-deps
drwx------@  3 welcome  staff    96 May  2 16:54 agents
drwx------@  5 welcome  staff   160 May  2 16:59 flows
drwxr-xr-x   3 welcome  staff    96 May  2 17:00 completions
drwxr-xr-x   3 welcome  staff    96 May  2 17:02 canvas
-rw-------@  1 welcome  staff  1403 May  2 17:16 openclaw.json.bak.4
drwx------@  4 welcome  staff   128 May  5 22:55 service-env
drwx------@  6 welcome  staff   192 May  5 22:55 logs
drwx------@  4 welcome  staff   128 May  5 22:55 tmp
drwxr-xr-x   4 welcome  staff   128 May  5 23:47 identity
-rw-------@  1 welcome  staff  1403 May  6 00:13 openclaw.json.bak.3
-rw-------@  1 welcome  staff  1595 May  6 22:43 openclaw.json.bak.2
drwxr-xr-x   3 welcome  staff    96 May  9 22:35 extensions
-rw-------   1 welcome  staff  2401 May  9 22:35 openclaw.json.bak.1
drwx------   3 welcome  staff    96 May  9 22:35 plugins
drwx------@  3 welcome  staff    96 May  9 23:19 memory
drwx------@  3 welcome  staff    96 May  9 23:47 subagents
drwx------@  5 welcome  staff   160 May 10 00:04 tasks
-rw-------@  1 welcome  staff   187 May 10 00:26 update-check.json
-rw-------   1 welcome  staff  2751 May 10 00:41 openclaw.json
-rw-------   1 welcome  staff  2680 May 10 00:41 openclaw.json.bak
-rw-------@  1 welcome  staff  2751 May 10 00:42 openclaw.json.last-good
-rw-------@  1 welcome  staff   180 May 10 00:50 exec-approvals.json
drwx------@  6 welcome  staff   192 May 10 08:36 cron
drwxr-xr-x   4 welcome  staff   128 May 10 21:24 devices
drwxr-xr-x@ 15 welcome  staff   480 May 10 21:33 workspace
welcome@jaisairams-Laptop workspace %  ls -ltr ~/.openclaw/workspace
total 64
-rw-r--r--@  1 welcome  staff  7835 May  2 16:54 AGENTS.md
-rw-r--r--@  1 welcome  staff  1806 May  2 16:54 SOUL.md
-rw-r--r--@  1 welcome  staff   920 May  2 16:54 TOOLS.md
-rw-r--r--@  1 welcome  staff   696 May  2 16:54 IDENTITY.md
-rw-r--r--@  1 welcome  staff   537 May  2 16:54 USER.md
-rw-r--r--@  1 welcome  staff   226 May  2 16:54 HEARTBEAT.md
-rw-r--r--@  1 welcome  staff  1531 May  2 16:54 BOOTSTRAP.md
drwx------@ 10 welcome  staff   320 May 10 00:08 google-adk-examples
drwx------@  3 welcome  staff    96 May 10 00:44 Users
drwxr-xr-x   3 welcome  staff    96 May 10 21:33 skills
welcome@jaisairams-Laptop workspace %

```

**OpenClaw File System & Directory Structure**

OpenClaw uses two main areas in your file system:

1. **State/Config Directory** (`~/.openclaw`): Stores configuration, credentials, sessions, and global skills.
2. **Workspace Directory** (`~/.openclaw/workspace` by default): The agent's "brain" and primary working area. This is where you customize behavior, memory, and files the agent can easily access.

### Key Directories

- **`~/.openclaw/`** (State directory)
  - `openclaw.json` — Main configuration file (models, defaults, workspace path, etc.).
  - `credentials/` — Secure storage for API keys, channel tokens (permissions restricted).
  - `sessions/` — Conversation histories and persistent state.
  - `skills/` — Global/shared installed skills (overrides).
  - Other: logs, caches, etc.

- **`~/.openclaw/workspace/`** (Default workspace — **most important**)
  - This is the default current working directory (cwd) for the agent.
  - Markdown files here are automatically loaded into the agent's context/prompt at session start.

#### Important Workspace Files (Bootstrap Files)
These Markdown files shape the agent's behavior and are injected into its system prompt:

| File              | Purpose |
|-------------------|---------|
| `AGENTS.md`       | Core instructions, rules, allowed actions, agent behavior (highest impact). |
| `SOUL.md`         | Personality, communication style, tone. |
| `IDENTITY.md` / `USER.md` | Agent's self-description and user preferences. |
| `TOOLS.md`        | Tool usage guidelines. |
| `MEMORY.md`       | Long-term memory summaries or instructions. |
| `HEARTBEAT.md`    | Periodic review instructions, self-improvement. |
| Others            | `BOOTSTRAP.md`, project-specific files, etc. |

**Note**: Total context has limits (e.g., ~20k chars per file, 150k total). Keep them concise.

- `skills/` (inside workspace or global) — Custom or installed skills.
- Project folders, documents, outputs — Agent can create/read/write here.

### File Access & Skills
- OpenClaw includes **filesystem tools** by default or via skills (e.g., `filesystem`, `file-browser`).
- The workspace is **not** a strict sandbox — the agent can access absolute paths unless you enable restrictions (`workspaceOnly: true`).
- For advanced file operations (search, batch processing, glob patterns), install a dedicated filesystem skill from ClawHub.

### How to View & Manage
- Open in your file explorer: `~/.openclaw` (on macOS/Linux; enable hidden files with Cmd+Shift+. on macOS).
- CLI commands:
  ```bash
  openclaw status                  # Overall status
  openclaw doctor                  # Check setup
  ls -la ~/.openclaw/workspace     # View workspace
  openclaw skills list             # Skills locations
  ```
- Change workspace path in `~/.openclaw/openclaw.json` under `agents.defaults.workspace`.

### Best Practices
- **Backup** `~/.openclaw/` and your workspace regularly.
- Keep sensitive files out of the workspace.
- Use a clean folder structure inside the workspace for better agent performance (e.g., separate projects, memory archives).
- For multi-agent setups: Per-agent sub-workspaces or shared files via `AGENTS.md`.
- Security: Review skills, use approval gates for writes, and consider running in a container or with limited permissions.

For the most accurate details, check the official docs:  
- [docs.openclaw.ai/concepts/agent-workspace](https://docs.openclaw.ai/concepts/agent-workspace)  
- Search for videos like “OpenClaw Folder Structure Explained”.

Would you like a sample workspace tree, help customizing specific `.md` files, filesystem skill recommendations, or instructions for a custom workspace path?
