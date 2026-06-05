```

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.


  Lightsail OpenClaw MOTD v3.0.1  (Ctrl+C to exit at any time)
+----------------------------------------------------------------+
|                   OpenClaw Dashboard Access                    |
+----------------------------------------------------------------+
  (Ctrl+C to exit at any time)

  Dashboard URL:
     https://34.228.253.230/overview

  Access Token:
     tr1joRwvnK9TKRJufI91yQ2PKaxzGtu5

  Current Model:
     bedrock/global.anthropic.claude-sonnet-4-6

------------------------------------------------------------------

+----------------------------------------------------------------+
|                        IP Configuration                        |
+----------------------------------------------------------------+
  (Ctrl+C to exit at any time)

  ⚠  Public IP has changed — updating gateway allowed origins.
     Previous: http://localhost:18789, http://127.0.0.1:18789, https://100.57.0.147
     Adding:   https://34.228.253.230
  ✓ Gateway update applied — restarting in background


+----------------------------------------------------------------+
|                     OpenClaw CLI Approval                      |
+----------------------------------------------------------------+
  (Ctrl+C to exit at any time)

2026/06/05 02:35:00 Warning: failed to handle openclaw cli approval: failed to list devices: exit status 1

+----------------------------------------------------------------+
|                     Browser Device Pairing                     |
+----------------------------------------------------------------+
  (Ctrl+C to exit at any time)

  1. Open the Dashboard URL in your browser:
     https://34.228.253.230/overview

  2. Enter your Access Token in the Gateway Token text box and press Connect:
     tr1joRwvnK9TKRJufI91yQ2PKaxzGtu5

  3. Once you see a device pairing required message, continue to next step below

  To view and approve other device pairings, use: openclaw devices list

  Continue with browser device pairing? (y = pair now, n = skip): y

+----------------------------------------------------------------+
|                       Device Management                        |
+----------------------------------------------------------------+
  (Ctrl+C to exit at any time)

Pending (1)
┌──────────────────────────────────────┬────────────────┬──────────┬─

Pending (1)
┌──────────────────────────────────────┬────────────────┬──────────┬──────────────────┬──────────────┬────────┬────────┐
│ Request                              │ Device         │ Role     │ Scopes           │ IP           │ Age    │ Flags  │
├──────────────────────────────────────┼────────────────┼──────────┼──────────────────┼──────────────┼────────┼────────┤
│ 49e6b7d7-590d-40da-8d0d-ab7c2767ee83 │ 41cad5b49243f6 │ operator │ operator.admin,  │ 73.233.51.81 │ 1m ago │        │
│                                      │ 98717e81dcab35 │          │ operator.read,   │              │        │        │
│                                      │ 98def2d5ecb238 │          │ operator.write,  │              │        │        │
│                                      │ 339dc0af893a41 │          │ operator.        │              │        │        │
│                                      │ 1cdae30e       │          │ approvals,       │              │        │        │
│                                      │                │          │ operator.pairing │              │        │        │
└──────────────────────────────────────┴────────────────┴──────────┴──────────────────┴──────────────┴────────┴────────┘
Paired (1)
┌──────────────────┬────────────┬────────────────────────────────────────────────────────────┬────────────┬────────────┐
│ Device           │ Roles      │ Scopes                                                     │ Tokens     │ IP         │
├──────────────────┼────────────┼────────────────────────────────────────────────────────────┼────────────┼────────────┤
│ 48c8c05be2676c60 │ operator   │ operator.admin, operator.read, operator.write, operator.   │ operator   │            │
│ f1ce6dfa83f8dd08 │            │ approvals, operator.pairing, operator.talk.secrets         │            │            │
│ c7f68a5e181cdede │            │                                                            │            │            │
│ 70d18b835fe82474 │            │                                                            │            │            │
└──────────────────┴────────────┴────────────────────────────────────────────────────────────┴────────────┴────────────┘

                                        
────────────────────────────────────────────────────────────────

Pending device request: 49e6b7d7-590d-40da-8d0d-ab7c2767ee83
Action? (a=approve, r=reject, s=skip all): a
  [████████████████████] 100%  Approving...
✓ Device approved successfully
  Waiting for gateway to process...
                                        
✓ No pending device requests


+----------------------------------------------------------------+
|                        Model Management                        |
+----------------------------------------------------------------+
  (Ctrl+C to exit at any time)

Current model: bedrock/global.anthropic.claude-sonnet-4-6

  Change model? (y/n): y

  ⚠  Bedrock requires one-time AWS account setup.
     See the Getting Started guide in your Lightsail console for details.

Select provider (1=Bedrock, c=cancel): 1

Available Bedrock models:

2026/06/05 02:36:48 Warning: failed to handle model management: failed to list Bedrock models: failed to list Bedrock models: exit status 254

------------------------------------------------------------------

+----------------------------------------------------------------+
|                       Security Settings                        |
+----------------------------------------------------------------+
  (Ctrl+C to exit at any time)

  Review security settings? (y/n): y

  [████████████████████] 100%  file permissions    
  ✓ Done

  Security Overview
  ─────────────────────────────────────────────────────────────

  File & folder protection
     Config, tokens, and session files should only be readable by you.
     Status: ✓ Protected


  Access token
     Rotate regularly or if you suspect your token has been compromised.
     Status: Last rotated: 4 Jun 2026 23:20

  Configurable Settings
  ─────────────────────────────────────────────────────────────

  1. Browser remote control
     When enabled, the AI can open and control a web browser on this machine.
     Status: ✓ Disabled — browser automation is off

  2. Rotate access token now
     Generates a new token and revokes all existing browser pairings.

  3. Auto-update allowed origins
     Automatically updates the gateway's allowed origin when SSH is done after IP changes.
     Status: ✓ Enabled — IP changes are handled automatically

  4. Daily token rotation
     Automatically rotates your access token every day at 03:00.
     Status: ✓ Enabled — token rotates daily at 03:00

  5. Shell command execution scope
     Controls where the AI is allowed to run shell commands.
     Status: ✓ Sandbox — commands run inside an isolated container only

  Enter setting number(s) to change, or n to skip: (1-5, comma-separated / n): n




------------------------------------------------------------------

OpenClaw CLI quick reference:

  openclaw tui                              Interactive chat with the agent
  openclaw agent --agent main -m 'hello'   One-off agent message
  openclaw agents list                      List configured agents
  openclaw gateway restart                  Restart the gateway
  openclaw health                           Check gateway health
  openclaw configure                        Interactive setup wizard
  openclaw help                             Full help
  openclaw-login                            Re-run this setup screen (Lightsail OpenClaw MOTD)  

------------------------------------------------------------------

ubuntu@ip-172-26-15-69:~$ 


+------------------------------------------------------------
```
