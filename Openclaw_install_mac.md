
# macOS/Linux
1. curl -fsSL https://openclaw.ai/install.sh | bash

# Windows (PowerShell)
1. iwr -useb https://openclaw.ai/install.ps1 | iex

# Openclaw login
1. http://127.0.0.1:18789/chat?session=agent%3Amain%3Amain
2. 
# Key Files path

```

Last login: Tue May  5 22:57:52 on ttys018
welcome@jaisairams-Laptop service-env % ls -ltr
total 16
-rw-------@ 1 welcome  staff  822 May  5 22:55 ai.openclaw.gateway.env
-rwx------@ 1 welcome  staff   95 May  5 22:55 ai.openclaw.gateway-env-wrapper.sh
welcome@jaisairams-Laptop service-env % pwd
/Users/welcome/.openclaw/service-env
welcome@jaisairams-Laptop service-env % 

```
# Path
welcome@jaisairams-Laptop frontend % export PATH="/opt/homebrew/Cellar/node@22/22.22.2_2/bin:$PATH"


## Setup

```
welcome@jaisairams-Laptop ~ % openclaw setup

🦞 OpenClaw 2026.4.29 (a448042) — Claws out, commit in—let's ship something mildly responsible.

Config OK: ~/.openclaw/openclaw.json
Workspace OK: ~/.openclaw/workspace
Sessions OK: ~/.openclaw/agents/main/sessions
welcome@jaisairams-Laptop ~ %

```

## openclaw status

```

welcome@jaisairams-Laptop ~ % openclaw status

🦞 OpenClaw 2026.4.29 (a448042) — Give me a workspace and I'll give you fewer tabs, fewer toggles, and more oxygen.

│
◇
OpenClaw status

Overview
┌──────────────────────┬─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│ Item                 │ Value                                                                                                                                                               │
├──────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ OS                   │ macos 13.0 (arm64) · node 22.22.2                                                                                                                                   │
│ Dashboard            │ http://127.0.0.1:18789/                                                                                                                                             │
│ Tailscale exposure   │ off                                                                                                                                                                 │
│ Channel              │ stable (default)                                                                                                                                                    │
│ Update               │ available · pnpm · npm update 2026.5.4                                                                                                                              │
│ Gateway              │ local · ws://127.0.0.1:18789 (local loopback) · unreachable (connect ECONNREFUSED 127.0.0.1:18789)                                                                  │
│ Gateway service      │ LaunchAgent not installed                                                                                                                                           │
│ Node service         │ LaunchAgent not installed                                                                                                                                           │
│ Agents               │ 1 · 1 bootstrap file present · sessions 1 · default main active 3d ago                                                                                              │
│ Memory               │ enabled (plugin memory-core) · not checked                                                                                                                          │
│ Plugin compatibility │ none                                                                                                                                                                │
│ Probes               │ skipped (use --deep)                                                                                                                                                │
│ Events               │ none                                                                                                                                                                │
│ Tasks                │ none                                                                                                                                                                │
│ Heartbeat            │ 30m (main)                                                                                                                                                          │
│ Sessions             │ 1 active · default gpt-5.5 (200k ctx) · ~/.openclaw/agents/main/sessions/sessions.json                                                                              │
└──────────────────────┴─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘

Security audit
Skipped in fast status. Full report: openclaw security audit
Deep probe: openclaw status --deep

Channels
┌──────────┬─────────┬────────┬──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│ Channel  │ Enabled │ State  │ Detail                                                                                                                                                       │
├──────────┼─────────┼────────┼──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┤
└──────────┴─────────┴────────┴──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘

Sessions
┌──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┬────────┬─────────┬──────────────┬───────────────────┐
│ Key                                                                                                                                  │ Kind   │ Age     │ Model        │ Tokens            │
├──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┼────────┼─────────┼──────────────┼───────────────────┤
│ agent:main:main                                                                                                                      │ direct │ 3d ago  │ gpt-5.5      │ unknown/200k (?%) │
└──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┴────────┴─────────┴──────────────┴───────────────────┘

FAQ: https://docs.openclaw.ai/faq
Troubleshooting: https://docs.openclaw.ai/troubleshooting
```

# openclaw doctor

```
welcome@jaisairams-Laptop ~ % openclaw doctor

🦞 OpenClaw 2026.4.29 (a448042) — I can't fix your code taste, but I can fix your build and your backlog.

▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄
██░▄▄▄░██░▄▄░██░▄▄▄██░▀██░██░▄▄▀██░████░▄▄▀██░███░██
██░███░██░▀▀░██░▄▄▄██░█░█░██░█████░████░▀▀░██░█░█░██
██░▀▀▀░██░█████░▀▀▀██░██▄░██░▀▀▄██░▀▀░█░██░██▄▀▄▀▄██
▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀
                  🦞 OPENCLAW 🦞

┌  OpenClaw doctor
│
◇  Update ──────────────────────────────────────────────────────────────────────────────────╮
│                                                                                           │
│  This install is not a git checkout.                                                      │
│  Run `openclaw update` to update via your package manager (npm/pnpm), then rerun doctor.  │
│                                                                                           │
├───────────────────────────────────────────────────────────────────────────────────────────╯
│
◇  Command owner ────────────────────────────────────────────────────────────────────────────╮
│                                                                                            │
│  No command owner is configured.                                                           │
│  A command owner is the human operator account allowed to run owner-only commands and      │
│  approve dangerous actions, including /diagnostics, /export-trajectory, /config, and exec  │
│  approvals.                                                                                │
│  DM pairing only lets someone talk to the bot; it does not make that sender the owner for  │
│  privileged commands.                                                                      │
│  Fix: set commands.ownerAllowFrom to your channel user id, for example openclaw config     │
│  set commands.ownerAllowFrom '["telegram:123456789"]'                                      │
│  Restart the gateway after changing this if it is already running.                         │
│                                                                                            │
├────────────────────────────────────────────────────────────────────────────────────────────╯
│
◇  State integrity ──────────────────────────────────────────────────────────────────────────╮
│                                                                                            │
│  - OAuth dir not present (~/.openclaw/credentials). Skipping create because no             │
│    WhatsApp/pairing channel config is active.                                              │
│  - 1/1 recent sessions are missing transcripts.                                            │
│    Verify sessions in store: openclaw sessions --store                                     │
│    "/Users/welcome/.openclaw/agents/main/sessions/sessions.json"                           │
│    Preview cleanup impact: openclaw sessions cleanup --store                               │
│    "/Users/welcome/.openclaw/agents/main/sessions/sessions.json" --dry-run                 │
│    Prune missing entries: openclaw sessions cleanup --store                                │
│    "/Users/welcome/.openclaw/agents/main/sessions/sessions.json" --enforce --fix-missing   │
│  - Main session transcript missing                                                         │
│    (~/.openclaw/agents/main/sessions/86fd9fdb-2287-44c0-892b-c13f1d46e635.jsonl). History  │
│    will appear to reset.                                                                   │
│                                                                                            │
├────────────────────────────────────────────────────────────────────────────────────────────╯
│
◇  Security ─────────────────────────────────╮
│                                            │
│  - No channel security warnings detected.  │
│  - Run: openclaw security audit --deep     │
│                                            │
├────────────────────────────────────────────╯
22:54:21 [skills] root has many entries, truncating discovery.
│
◇  Skills status ────────────╮
│                            │
│  Eligible: 209             │
│  Missing requirements: 46  │
│  Blocked by allowlist: 0   │
│                            │
├────────────────────────────╯
│
◇  Plugins ──────╮
│                │
│  Loaded: 69    │
│  Imported: 0   │
│  Disabled: 48  │
│  Errors: 0     │
│                │
├────────────────╯
│
◇  Enable zsh shell completion for openclaw?
│  No
│
◇  Gateway ──────────────╮
│                        │
│  Gateway not running.  │
│                        │
├────────────────────────╯
│
◇  Gateway connection ─────────────────────────────╮
│                                                  │
│  Gateway target: ws://127.0.0.1:18789            │
│  Source: local loopback                          │
│  Config: /Users/welcome/.openclaw/openclaw.json  │
│  Bind: loopback                                  │
│                                                  │
├──────────────────────────────────────────────────╯
22:54:53 [plugins] memory-core staging bundled runtime deps (42 specs): @agentclientprotocol/claude-agent-acp@0.31.1, @agentclientprotocol/sdk@0.21.0, @clack/prompts@^1.2.0, @homebridge/ciao@^1.3.7, @lydell/node-pty@1.2.0-beta.12, @mariozechner/pi-ai@0.70.6, @mariozechner/pi-coding-agent@0.70.6, @modelcontextprotocol/sdk@1.29.0, @mozilla/readability@^0.6.0, @tencent-connect/qqbot-connector@^1.1.0, @zed-industries/codex-acp@0.12.0, acpx@0.6.1, ajv@^8.20.0, chokidar@^5.0.0, commander@^14.0.3, croner@^10.0.1, dotenv@^17.4.2, express@5.2.1, global-agent@^4.1.3, https-proxy-agent@^9.0.0, jiti@^2.6.1, json5@^2.2.3, jszip@^3.10.1, linkedom@^0.18.12, markdown-it@14.1.1, minimatch@10.2.4, mpg123-decoder@^1.0.3, node-edge-tts@^1.2.10, openai@^6.34.0, pdfjs-dist@^5.7.284, playwright-core@1.59.1, semver@7.7.4, silk-wasm@^3.7.1, sqlite-vec@0.1.9, tar@7.5.13, tslog@^4.10.2, typebox@1.1.34, undici@8.1.0, web-push@^3.6.7, ws@^8.20.0, yaml@^2.8.3, zod@^4.3.6
22:54:53 [plugins] memory-core installed bundled runtime deps in 5ms: @agentclientprotocol/claude-agent-acp@0.31.1, @agentclientprotocol/sdk@0.21.0, @clack/prompts@^1.2.0, @homebridge/ciao@^1.3.7, @lydell/node-pty@1.2.0-beta.12, @mariozechner/pi-ai@0.70.6, @mariozechner/pi-coding-agent@0.70.6, @modelcontextprotocol/sdk@1.29.0, @mozilla/readability@^0.6.0, @tencent-connect/qqbot-connector@^1.1.0, @zed-industries/codex-acp@0.12.0, acpx@0.6.1, ajv@^8.20.0, chokidar@^5.0.0, commander@^14.0.3, croner@^10.0.1, dotenv@^17.4.2, express@5.2.1, global-agent@^4.1.3, https-proxy-agent@^9.0.0, jiti@^2.6.1, json5@^2.2.3, jszip@^3.10.1, linkedom@^0.18.12, markdown-it@14.1.1, minimatch@10.2.4, mpg123-decoder@^1.0.3, node-edge-tts@^1.2.10, openai@^6.34.0, pdfjs-dist@^5.7.284, playwright-core@1.59.1, semver@7.7.4, silk-wasm@^3.7.1, sqlite-vec@0.1.9, tar@7.5.13, tslog@^4.10.2, typebox@1.1.34, undici@8.1.0, web-push@^3.6.7, ws@^8.20.0, yaml@^2.8.3, zod@^4.3.6
│
◇  Gateway ────────────────────────╮
│                                  │
│  Gateway service not installed.  │
│                                  │
├──────────────────────────────────╯
│
◇  Install gateway service now?
│  Yes
│
◇  Gateway service runtime
│  Node (recommended)

Installed LaunchAgent: /Users/welcome/Library/LaunchAgents/ai.openclaw.gateway.plist
Logs: /Users/welcome/.openclaw/logs/gateway.log
Run "openclaw doctor --fix" to apply changes.
│
└  Doctor complete.

welcome@jaisairams-Laptop ~ %

```

# Openclaw help commands

```
welcome@jaisairams-Laptop ~ % openclaw help

🦞 OpenClaw 2026.4.29 (a448042) — Give me a workspace and I'll give you fewer tabs, fewer toggles, and more oxygen.

Usage: openclaw [options] [command]

Options:
  --container <name>   Run the CLI inside a running Podman/Docker container
                       named <name> (default: env OPENCLAW_CONTAINER)
  --dev                Dev profile: isolate state under ~/.openclaw-dev, default
                       gateway port 19001, and shift derived ports
                       (browser/canvas)
  -h, --help           Display help for command
  --log-level <level>  Global log level override for file + console
                       (silent|fatal|error|warn|info|debug|trace)
  --no-color           Disable ANSI colors
  --profile <name>     Use a named profile (isolates
                       OPENCLAW_STATE_DIR/OPENCLAW_CONFIG_PATH under
                       ~/.openclaw-<name>)
  -V, --version        output the version number

Commands:
  Hint: commands suffixed with * have subcommands. Run <command> --help for details.
  acp *                Agent Control Protocol tools
  agent                Run one agent turn via the Gateway
  agents *             Manage isolated agents (workspaces, auth, routing)
  approvals *          Manage exec approvals (gateway or node host)
  backup *             Create and verify local backup archives for OpenClaw
                       state
  capability *         Run provider-backed inference commands (fallback alias:
                       infer)
  channels *           Manage connected chat channels (Telegram, Discord, etc.)
  chat                 Open a local terminal UI (alias for tui --local)
  clawbot *            Legacy clawbot command aliases
  commitments *        List and manage inferred follow-up commitments
  completion           Generate shell completion script
  config *             Non-interactive config helpers
                       (get/set/unset/file/validate). Default: starts guided
                       setup.
  configure            Interactive configuration for credentials, channels,
                       gateway, and agent defaults
  crestodian           Open the ring-zero setup and repair helper
  cron *               Manage cron jobs via the Gateway scheduler
  daemon *             Gateway service (legacy alias)
  dashboard            Open the Control UI with your current token
  devices *            Device pairing + token management
  directory *          Lookup contact and group IDs (self, peers, groups) for
                       supported chat channels
  dns *                DNS helpers for wide-area discovery (Tailscale + CoreDNS)
  docs                 Search the live OpenClaw docs
  doctor               Health checks + quick fixes for the gateway and channels
  exec-policy *        Show or synchronize requested exec policy with host
                       approvals
  gateway *            Run, inspect, and query the WebSocket Gateway
  health               Fetch health from the running gateway
  help                 Display help for command
  hooks *              Manage internal agent hooks
  infer *              Run provider-backed inference commands
  logs                 Tail gateway file logs via RPC
  mcp *                Manage OpenClaw MCP config and channel bridge
  memory               Search, inspect, and reindex memory files
  message *            Send, read, and manage messages
  migrate *            Import state from another agent system
  models *             Discover, scan, and configure models
  node *               Run and manage the headless node host service
  nodes *              Manage gateway-owned node pairing and node commands
  onboard              Interactive onboarding for gateway, workspace, and skills
  pairing *            Secure DM pairing (approve inbound requests)
  plugins *            Manage OpenClaw plugins
  proxy *              Run the OpenClaw debug proxy and inspect captured traffic
  qr                   Generate mobile pairing QR/setup code
  reset                Reset local config/state (keeps the CLI installed)
  sandbox *            Manage sandbox containers for agent isolation
  secrets *            Secrets runtime reload controls
  security *           Security tools and local config audits
  sessions *           List stored conversation sessions
  setup                Initialize local config and agent workspace
  skills *             List and inspect available skills
  status               Show channel health and recent session recipients
  system *             System events, heartbeat, and presence
  tasks *              Inspect durable background task state
  terminal             Open a local terminal UI (alias for tui --local)
  tui                  Open a terminal UI connected to the Gateway
  uninstall            Uninstall the gateway service + local data (CLI remains)
  update *             Update OpenClaw and inspect update channel status
  webhooks *           Webhook helpers and integrations

Examples:
  openclaw models --help
    Show detailed help for the models command.
  openclaw channels login --verbose
    Link personal WhatsApp Web and show QR + connection logs.
  openclaw message send --target +15555550123 --message "Hi" --json
    Send via your web session and print JSON result.
  openclaw gateway --port 18789
    Run the WebSocket Gateway locally.
  openclaw --dev gateway
    Run a dev Gateway (isolated state/config) on ws://127.0.0.1:19001.
  openclaw gateway --force
    Kill anything bound to the default gateway port, then start it.
  openclaw gateway ...
    Gateway control via WebSocket.
  openclaw agent --to +15555550123 --message "Run summary" --deliver
    Talk directly to the agent using the Gateway; optionally send the WhatsApp reply.
  openclaw message send --channel telegram --target @mychat --message "Hi"
    Send via your Telegram bot.

Docs: https://docs.openclaw.ai/cli

welcome@jaisairams-Laptop ~ %

```
welcome@jaisairams-Laptop frontend % more /Users/welcome/.zshrc


