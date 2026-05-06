
# macOS/Linux
1. curl -fsSL https://openclaw.ai/install.sh | bash

# Windows (PowerShell)
1. iwr -useb https://openclaw.ai/install.ps1 | iex


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


welcome@jaisairams-Laptop frontend % more /Users/welcome/.zshrc


