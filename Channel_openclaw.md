**OpenClaw Channel Integration Guide**

OpenClaw connects your AI agent to messaging apps (channels) via the **Gateway**. You can run multiple channels simultaneously (Telegram + WhatsApp + Discord, etc.), and messages route to your agent(s). Telegram is the easiest and most recommended for beginners.

### Common Commands
```bash
openclaw channels list          # View configured channels
openclaw channels status        # Check connection status
openclaw channels add           # Interactive wizard (recommended)
openclaw gateway restart        # Apply changes
openclaw dashboard              # Open UI for management
```

### 1. Telegram (Easiest & Fastest)
1. Open Telegram → Search **@BotFather** → Send `/newbot` → Follow prompts to create a bot and copy the **API token**.
2. Add/configure it:
   ```bash
   openclaw channels add --channel telegram
   ```
   Or via config (`~/.openclaw/openclaw.json` or similar):
   ```json
   {
     "channels": {
       "telegram": {
         "enabled": true,
         "botToken": "YOUR_BOT_TOKEN_HERE",
         "dmPolicy": "pairing",           // or "allowlist"
         "groups": { "*": { "requireMention": true } }
       }
     }
   }
   ```
3. Restart Gateway: `openclaw gateway restart`
4. Message your bot on Telegram to test. Use `openclaw pairing approve` if needed for new senders.

### 2. WhatsApp (Most Popular)
- Uses WhatsApp Web protocol (Baileys library) → QR code pairing.
1. Run:
   ```bash
   openclaw channels add --channel whatsapp
   ```
   Or with account name:
   ```bash
   openclaw channels add --channel whatsapp --account personal
   ```
2. A QR code appears (or link). Scan it with WhatsApp on your phone (**Linked Devices** → **Link a Device**).
3. Wait for pairing to complete. Credentials store locally.
4. Restart gateway and test by messaging the linked number.

**Tip**: Use a secondary number for production to avoid personal account issues.

### 3. Other Popular Channels
- **Discord**: Create a bot on Discord Developer Portal, get token, invite bot to server. Use `openclaw channels add --channel discord`.
- **Slack**: App manifest + Socket Mode or webhook.
- **Others**: Signal, iMessage (macOS), Google Chat, Microsoft Teams, etc. — check specific docs for tokens/QR/webhooks.

### Security & Policies (Important!)
- **Pairing Mode** (`dmPolicy: "pairing"`): Requires manual approval for new chats.
- **Allowlist**: Restrict to specific users/groups.
- Commands to manage:
  ```bash
  openclaw pairing list --pending
  openclaw pairing approve --channel telegram --all-pending
  openclaw pairing approve --channel whatsapp --sender "+1234567890"
  ```
- Groups often require `@mention` to activate the agent.

### Dashboard Management
Run `openclaw dashboard` → Go to **Channels** section for a visual overview, status, and easy configuration.

### Troubleshooting
- Check status: `openclaw gateway status` and `openclaw channels status`.
- Logs: Look in `~/.openclaw/logs/` or use `openclaw doctor`.
- Common fixes: Restart gateway, re-run `channels add`, verify tokens/QR, check firewall/port 18789.
- Multi-channel: All share the same agents/memory by default.

For the latest details on any channel, visit the official docs:  
**https://docs.openclaw.ai/channels** (includes Telegram, WhatsApp, Discord, Slack, etc.)

Would you like detailed steps for a specific channel (e.g., Discord, Slack), multi-channel routing, group chat setup, or security hardening? Let me know your preferred platform!
