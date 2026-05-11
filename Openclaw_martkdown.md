**OpenClaw Setup Tutorial (Official Quick Start)**

OpenClaw is an open-source personal AI assistant that runs on your device (Mac, Linux, Windows/WSL2). It connects to messaging apps like Telegram/WhatsApp and uses LLMs (Claude, GPT, Gemini, local models via Ollama, etc.) to perform real tasks.

### Prerequisites
- **Node.js** (v24 recommended; v22.16+ supported). The installer handles this automatically.
- An **API key** from a model provider (Anthropic/Claude recommended for best results, OpenAI, Google, etc.). Have it ready.
- Basic terminal comfort (commands are simple copy-paste).

**Windows users**: WSL2 is more stable for full features. Native Windows also works.

### Step-by-Step Installation

1. **Install OpenClaw** (one-liner, ~1-2 minutes)  
   **macOS / Linux**:  
   ```bash
   curl -fsSL https://openclaw.ai/install.sh | bash
   ```  
   **Windows (PowerShell)**:  
   ```powershell
   iwr -useb https://openclaw.ai/install.ps1 | iex
   ```

2. **Run Onboarding Wizard**  
   ```bash
   openclaw onboard --install-daemon
   ```  
   - This sets up your model provider, API key, and Gateway (the core service).  
   - It can install a daemon/service for auto-start.  
   - Takes ~2 minutes.

3. **Verify Gateway**  
   ```bash
   openclaw gateway status
   ```  
   You should see it listening on port **18789**.

4. **Open the Dashboard**  
   ```bash
   openclaw dashboard
   ```  
   This opens a browser Control UI. Test by sending a message in the chat.

5. **Connect a Messaging App (e.g., Telegram – easiest)**  
   - Go to Telegram BotFather, create a bot, and get the token.  
   - Follow OpenClaw’s channel setup (usually `openclaw channels login telegram` or via dashboard).  
   - Other options: WhatsApp, Discord, Slack, etc. See docs for details.

### Useful Commands
- `openclaw --version` — Check version.  
- `openclaw doctor` — Diagnose issues.  
- `openclaw gateway restart` — Restart service.  
- `openclaw update` — Update to latest.  
- `openclaw status` — Overall status.

### Next Steps After Setup
- **Install Skills**: Browse ClawHub or GitHub repos for extensions (web browsing, Gmail, calendar, GitHub, etc.).  
- **Security Best Practices**: Run on a dedicated machine/device if possible. Use approval gates for actions. Don’t expose the Gateway publicly (use SSH tunnels/Tailscale if needed). Start with read-only access.  
- **Local Models**: Configure Ollama for privacy/offline use.  
- Explore persistent memory, multi-agent setups, and jobs/cron tasks.

### Official Resources
- **Docs**: [docs.openclaw.ai/start/getting-started](https://docs.openclaw.ai/start/getting-started)  
- **Main Site**: [openclaw.ai](https://openclaw.ai/)  
- **GitHub**: github.com/openclaw/openclaw  
- YouTube: Search “OpenClaw setup tutorial” for visual walkthroughs (many cover VPS, security, Telegram in detail).

**Troubleshooting Tips**:
- If `openclaw` command not found: Check your PATH or open a new terminal.  
- API issues: Re-run onboarding or edit config in `~/.openclaw/`.  
- For VPS/Docker/Raspberry Pi setups, check the dedicated hosting guides in the docs.

The whole basic setup usually takes **5-15 minutes**. Once running, chat with your agent to customize it further (it can even help install skills or fix issues itself).  

Let me know your OS, if you want VPS/Docker instructions, Telegram-specific setup, or help with a particular part!
