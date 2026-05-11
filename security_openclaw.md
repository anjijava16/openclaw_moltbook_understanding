**OpenClaw Security Best Practices (2026)**

OpenClaw is a powerful self-hosted AI agent platform, but with great power comes responsibility. It connects LLMs to real tools, messaging channels, files, and execution environments, so misconfiguration can lead to significant risks (data exfiltration, unauthorized actions, prompt injection steering, etc.). The official model is a **personal assistant trust boundary** (one trusted operator per gateway), **not** a multi-tenant adversarial security boundary.

### 1. Run the Built-in Security Audit First
```bash
openclaw security audit
openclaw security audit --deep
openclaw security audit --fix     # Auto-fixes many common issues
```
Run this after any config change or new skill/channel. It checks exposures, permissions, policies, etc.

### 2. Isolation & Deployment (Highest Impact)
- **Dedicated environment** — Run on a separate device, VM, Raspberry Pi, or VPS (not your daily driver). Treat the host as potentially compromised if the agent is fully tool-enabled.
- **Never expose the Gateway publicly** — Bind to `127.0.0.1` (default). Do **not** publish port 18789. Use Tailscale, SSH tunnels, or a secure reverse proxy for remote access.
- **Container/VM hardening** — Run in Docker (non-root user) or a hardened systemd service (`NoNewPrivileges`, `ProtectSystem`, etc.). Use dedicated OS user.
- **Workspace & State** — Keep `~/.openclaw/` (config, credentials) and workspace separate. Set strict permissions: `chmod 700 ~/.openclaw` and `600` on sensitive files.

### 3. Channels & Access Control
- **Default to "pairing" mode** for DMs (manual approval for new senders). Use allowlists for groups.
- Require `@mention` in groups.
- Use separate numbers/accounts for bots (avoid linking to personal WhatsApp/Signal).
- Prefer E2E-encrypted channels like Matrix where possible.

### 4. Sandboxing & Tool Execution (Critical for Tool-Enabled Agents)
- Enable sandboxing: `agents.defaults.sandbox.mode: "all"` (or `"non-main"`) with Docker backend (default).
- Use **least privilege** tool policies: `exec.security: "allowlist"` + explicit commands only. Enable approvals for high-risk actions.
- Workspace-only mode where possible (`tools.exec.applyPatch.workspaceOnly: true`).
- Avoid `elevated` tools unless necessary; they bypass sandbox.

### 5. Skills & Plugins
- Only install from trusted sources on ClawHub. Review `SKILL.md` and code before enabling.
- Pin versions.
- Run new skills in sandbox with minimal permissions first.
- Regularly audit installed skills.

### 6. Credentials & Secrets
- Use dedicated, scoped, short-lived API keys/tokens (never personal full-access accounts).
- Rotate regularly.
- OpenClaw stores them securely in `credentials/`, but never put sensitive data in workspace files.
- Avoid `.env` files in workspace if possible.

### 7. Prompt Injection & Model Defenses
- Use strong instruction-following models (e.g., latest Claude/GPT).
- Consider self-hosted/local models for sensitive use cases.
- Keep tool surfaces narrow (reduces what injection can achieve).
- Enable redaction in logs.

### 8. Configuration Hardening Examples (from Official Baseline)
Key settings in `~/.openclaw/openclaw.json`:
- Gateway auth enabled (token/password).
- Tight channel policies.
- Sandbox enabled.
- Filesystem scoped to workspace.
- Logging redaction on.

### 9. Ongoing Practices
- Regular audits + updates (`openclaw update`).
- Monitor logs (`~/.openclaw/logs/`).
- Backup config/workspace (but sanitize secrets).
- Incident response: Contain → Rotate secrets → Audit → Report if needed.
- Browser control: Prefer node-based, tailnet-only, with approvals.

### Quick Production Checklist
- Gateway bound to localhost + auth.
- Sandbox enabled + tool allowlists.
- Channels use pairing/allowlist + mention gating.
- Strict file permissions on `~/.openclaw`.
- Dedicated/isolated host.
- `openclaw security audit --deep` clean.
- Only trusted skills.
- Regular key rotation & backups.

For the most authoritative and up-to-date details, read the official docs:  
**https://docs.openclaw.ai/gateway/security** and **https://docs.openclaw.ai/gateway/sandboxing**.

Security is layered and ongoing—start minimal and expand only as needed.  

Let me know if you want help with a specific part (e.g., sample `openclaw.json` hardening, Docker setup, or audit interpretation)!
