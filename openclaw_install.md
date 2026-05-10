# Installing OpenClaw - Setup Guide

Step 1: Install Homebrew

Homebrew is a package manager for macOS (and Linux). Open your Terminal and run:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

After installation, verify it works:

brew --version

Step 2: Install Node.js and npm

npm comes bundled with Node.js. Install it via Homebrew:

brew install node

Verify both are installed:

node --version

npm --version

Step 3: Install OpenClaw

Once npm is ready, install OpenClaw globally:

npm install -g openclaw

Or add it to a project locally:

npm install openclaw

Verify the installation:


# Openclaw: Complete Setup & Debugging Guid

A beginner-friendly guide to installing OpenClaw and troubleshooting like a pro.

What is OpenClaw? OpenClaw is an open-source AI agent gateway that lets you control your computer through WhatsApp, Telegram, Discord, Slack, Signal, iMessage, and more. Once set up, you can message your bot from anywhere and it will run commands on your machine.

(Previously known as Clawdbot / Moltbot — the project was renamed to OpenClaw.)



## Part 1: Prerequisites & Installation

What You Need Before Starting

- A computer (Mac, Linux, or Windows via WSL2)
- An internet connection
- An Anthropic API key (or another supported provider)
- About 20 minutes
- Node.js version 22 or higher



## Step 1: Install Homebrew (Mac/Linux)

Homebrew is a package manager that makes installing developer tools easy.

Open Terminal and paste this command:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Follow the prompts — it'll ask for your password.

Verify it worked:

brew --version

You should see something like Homebrew 4.x.x.



## Step 2: Install Node.js

OpenClaw requires Node.js version 22 or higher.

brew install node

Verify it installed:

node --version

npm --version

Make sure Node is version 22+. If it's lower, upgrade with:

brew upgrade node



## Step 3: Install OpenClaw

Option A — Install script (recommended):

macOS / Linux:

curl -fsSL https://openclaw.ai/install.sh | bash

Windows (PowerShell):

iwr -useb https://openclaw.ai/install.ps1 | iex

Option B — Install via npm:

npm install -g openclaw@latest

Verify installation:

openclaw --version



## Step 4: Run Onboarding

This is the main setup command that configures everything:

openclaw onboard --install-daemon

The onboarding wizard will:

- Create your config file at ~/.openclaw/openclaw.json
- Set up the gateway service
- Install the LaunchAgent (so it runs on startup)
- Walk you through API key and channel setup



## Step 5: Add Your Anthropic API Key

During onboarding, you'll be asked for your API key. If you need to add it later:

Get your key from console.anthropic.com

Set up auth via the models CLI (preferred):

openclaw models auth setup-token

Or set it in config:

openclaw config set anthropic.apiKey "your-api-key-here"

Or use an environment variable:

export ANTHROPIC_API_KEY="your-api-key-here"



## Step 6: Start the Gateway

openclaw gateway start

Check if it's running:

openclaw gateway status

Access the dashboard at:

http://127.0.0.1:18789/

Or open it directly:

openclaw dashboard



## Part 2: Connecting Telegram

Set Up Your Telegram Bot

1. Open Telegram and message @BotFather
2. Send /newbot
3. Follow the prompts to name your bot
4. Copy the API token BotFather gives you

## Add the Channel to OpenClaw

### openclaw channels add

Select Telegram when prompted, paste your bot token.

Or configure it directly in ~/.openclaw/openclaw.json:

```json5
{
  channels: {
    telegram: {
      enabled: true,
      botToken: "your-telegram-bot-token",
      dmPolicy: "pairing"
    }
  }
}
```

Restart the gateway:

openclaw gateway restart

Approve Your First Message

When you message your bot for the first time, OpenClaw requires pairing approval:

openclaw pairing list telegram
openclaw pairing approve telegram <CODE>

Pairing codes expire after 1 hour. After approval, your bot will respond to your messages.

Group Chat Tip: If the bot doesn't respond in group chats, disable privacy mode via BotFather's /setprivacy, then remove and re-add the bot to the group.



## Part 3: Changing the Model

By default, OpenClaw uses Sonnet. To switch to Opus:

openclaw models set anthropic/claude-opus-4-6

You can also set up fallback models:

openclaw models fallbacks add anthropic/claude-sonnet-4-6

Check what's configured:

openclaw models status

List all available models:

openclaw models list --all

Restart the gateway after model changes:

openclaw gateway restart



## Part 4: Common Commands

| Task | Command |
|------|---------|
| Check status | `openclaw gateway status` |
| Start gateway | `openclaw gateway start` |
| Stop gateway | `openclaw gateway stop` |
| Restart gateway | `openclaw gateway restart` |
| Open dashboard | `openclaw dashboard` |
| Run diagnostics | `openclaw doctor` |
| Auto-fix issues | `openclaw doctor --repair` |
| Deep scan + auto-fix | `openclaw doctor --deep --yes` |
| View logs | `openclaw logs --follow` |
| Check config | `openclaw config list` |
| List channels | `openclaw channels status --probe` |
| List models | `openclaw models list` |
| Security audit | `openclaw security audit --fix` |
| Full system check | `openclaw status --all --deep` |



## Part 5: Debugging & Troubleshooting

The Golden Rule

Never blindly copy-paste error messages. Always include context.



What to Copy When Debugging

1. The Command You Ran

Always include the exact command:

openclaw gateway start


2. The Full Error Output

Copy the complete error, not just the last line:

Runtime: stopped (state spawn scheduled)
RPC probe: failed
RPC target: ws://127.0.0.1:18789
  gateway closed (1006 abnormal closure (no close frame)): no close reason


3. The Doctor Output

openclaw doctor

This gives a full diagnostic snapshot covering 19 checks: config validation, OAuth tokens, service runtime, port collisions, sandbox status, channel health, and more.



How to Copy from Terminal

macOS Terminal / iTerm2

- Select + Copy: Click and drag, then Cmd + C
- Copy All Output: Cmd + A then Cmd + C

VS Code / Cursor Integrated Terminal

- Select + Copy: Click and drag, Cmd + C
- Right-click: Select text → Copy



Best Practices for Sharing Errors

DO:

- Include the command that triggered the error
- Copy the full stack trace
- Run `openclaw doctor` and include that output
- Include relevant log output
- Preserve formatting using code blocks

DON'T:

- Screenshot terminal text (hard to search/copy)
- Paraphrase the error ("it said something about gateway")
- Copy only the last line
- Skip the doctor output



Formatting for Claude

Wrap errors in code blocks:

```
[paste your error here]
```

For shell output:

```bash
$ openclaw gateway status
Runtime: stopped (state spawn scheduled)
```



Common Issues & Fixes

Gateway Won't Start

Symptoms: "Runtime: stopped" or "state spawn scheduled"

Fix:

openclaw doctor --repair
openclaw gateway restart

If that doesn't work, check the logs:

openclaw logs --follow

Or check log files directly:

tail -50 ~/.openclaw/logs/gateway.err.log


"command not found: openclaw"

Fix: The install directory isn't in your PATH.

npm config get prefix

Add that path to your shell profile:

echo 'export PATH="/opt/homebrew/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc


Telegram Bot Not Responding

Check:

- Is the gateway running? `openclaw gateway status`
- Did you approve pairing? `openclaw pairing list telegram`
- Is your bot token correct? `openclaw config list`
- Did you message your own bot (not BotFather)?
- For groups: Did you disable privacy mode via BotFather's /setprivacy?

Find your Telegram user ID:

Message your bot, then run `openclaw logs --follow` and look for the `from.id` field.


Deprecated Config Keys

If you see an error saying commands refuse to run due to deprecated keys:

openclaw doctor --repair

This backs up your config to ~/.openclaw/openclaw.json.bak, normalizes legacy values, and removes unknown keys.


Permission Errors

Fix:

sudo chown -R $(whoami) ~/.openclaw



Useful Debugging Commands

```bash
# Check gateway status
openclaw gateway status

# Run full diagnostics
openclaw doctor

# Auto-fix common issues
openclaw doctor --repair

# Deep scan + auto-fix (checks for extra gateway installs)
openclaw doctor --deep --yes

# Aggressive repair (overwrites supervisor configs)
openclaw doctor --repair --force

# View live logs
openclaw logs --follow

# JSON log output (for parsing)
openclaw logs --json

# Check specific log files
tail -50 ~/.openclaw/logs/gateway.log
tail -50 ~/.openclaw/logs/gateway.err.log

# View config
openclaw config list

# Restart everything
openclaw gateway restart

# Full system diagnosis
openclaw status --all --deep

# Security audit
openclaw security audit --fix

# Reset config if things are really broken
openclaw reset --scope config
```



Template for Reporting Issues

```
**Command run:**
[paste command]

**Expected behavior:**
[what should happen]

**Actual output:**
[paste full error]

**Doctor output:**
[paste openclaw doctor output]

**Environment:**
- OS: [macOS / Linux / Windows WSL2]
- Node version:
- OpenClaw version:
```



## Part 6: Optional — Remote Access with Tailscale

By default, OpenClaw only works locally (127.0.0.1). If you want to access the web dashboard from other devices:

Install Tailscale

brew install --cask tailscale

Sign In

Open Tailscale from Applications, or:

tailscale up

Configure OpenClaw

openclaw config set gateway.bind "tailnet"
openclaw config set gateway.tailscale.mode "on"
openclaw gateway restart

Get Your Tailscale IP

tailscale ip

Now access the dashboard from any device on your Tailscale network at http://100.x.x.x:18789/

Note: If you're using Telegram, you already have remote access — just message your bot from anywhere. Tailscale is only needed for the web dashboard.



Quick Reference

| Task | Command |
|------|---------|
| Install Homebrew | `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"` |
| Install Node.js | `brew install node` |
| Install OpenClaw (script) | `curl -fsSL https://openclaw.ai/install.sh \| bash` |
| Install OpenClaw (npm) | `npm install -g openclaw@latest` |
| Run onboarding | `openclaw onboard --install-daemon` |
| Start gateway | `openclaw gateway start` |
| Check status | `openclaw gateway status` |
| Open dashboard | `openclaw dashboard` or http://127.0.0.1:18789/ |
| Run diagnostics | `openclaw doctor --repair` |
| View logs | `openclaw logs --follow` |
| Set model to Opus | `openclaw models set anthropic/claude-opus-4-6` |
| Add Telegram | `openclaw channels add` |
| Approve pairing | `openclaw pairing approve telegram <CODE>` |
| Windows install | `iwr -useb https://openclaw.ai/install.ps1 \| iex` |



Getting Help

- Official Docs: https://docs.openclaw.ai
- Getting Started: https://docs.openclaw.ai/start/getting-started
- Troubleshooting: https://docs.openclaw.ai/gateway/troubleshooting
- GitHub: https://github.com/openclaw/openclaw


openclaw --version

That's it — you're all set!
