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

## Desktop actions (v0.4.2)
If desktop_inspect and desktop_ui are advertised, you can inspect the current Windows pointer, virtual screen dimensions and session number, move the pointer with action=move, then inspect again to verify its position. Never treat catalog availability as proof of execution. Obtain authorization before sensitive, destructive or externally communicating actions.
This repository ships no device agent, relay or credentials.
