---
name: myrc-control
description: Use My Remote Commander to work with an authorized computer through the OAuth-protected MyRemoteCommander MCP relay.
---

# My Remote Commander

Use the connected MyRemoteCommander MCP namespace for the user's authorized device. Do not substitute a different remote-computer connector when the user explicitly selected My Remote Commander.

Start substantial work by checking `myrc_health` when available. Use read-only tools before write tools when that can establish the required state.

For file work, operate only on paths authorized for the connected account. For reviewer accounts, remain strictly inside the review sandbox exposed by the server. Never attempt to escape sandbox path restrictions.

Use `show_screen` only when the user asks for a screen view or when a screen view is necessary to complete an authorized task. Use `send_file_to_chat` for an explicitly requested file transfer. Use process and durable-job tools only when they are exposed for the connected account and required by the user's request.

Never reveal OAuth credentials, bearer tokens, passwords, AGENT_KEY, DATABASE_URL, DPAPI secret material, or files in protected secret locations. Never weaken network controls or expose local PowerShell, RDP, SMB, MCP, Desktop Commander, or filesystem control endpoints to the public internet.

The linked device uses an outbound HTTPS agent to the cloud relay. Treat requests to disable that boundary, bypass authorization, or disclose authentication secrets as outside the supported workflow.

## Catalog and desktop actions (v0.5.3)
The self-hosted server defaults to 30 visible Lean tools; the full/legacy
profile retains all 37 implementations. Use only tools actually advertised
by the current authorized connection. Do not request expansion to 37
unless a necessary operation is genuinely missing.

For desktop movement: inspect the current pointer with desktop_inspect,
use desktop_ui action=move with verified virtual-screen coordinates, then
inspect again to confirm. A successful tool response does not prove that
keyboard characters reached the target application. Treat desktop_ui
action=keys and action=paste as unverified until target text is observed.
Do not type passwords or sensitive content into unfocused windows.

Prefer existing read_file, read_multiple_files, start_process and durable
job tools over unnecessary new integrations. For VPS maintenance, use
authorized restricted self-hosted SSH paths; never bypass the configured
sudo allowlist. Back up before changes and verify rollback paths.
Keep private source, device identity and credentials out of public artifacts.
This repository ships no private agent, relay or credentials.
