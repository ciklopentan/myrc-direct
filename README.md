# MyRC Direct — public ChatGPT MCP integration

This repository publishes the **integration metadata** for MyRC Direct v0.4.2: an MCP plugin manifest, an example server URL, an onboarding skill and icons.

**It does NOT contain the executable remote-access backend.** The OAuth relay, device agent, Windows desktop helper, wrapper, durable jobs, runtime configuration, secrets and real endpoint are private. This repository alone cannot control any computer.

## Verified on 2026-10-09

In the owner's authorized ChatGPT connection, 37 MCP tool names were discoverable. Three direct calls completed: desktop_inspect, desktop_ui with action=move, desktop_inspect. Both inspections matched the moved cursor location in Windows session 1. This confirms mouse movement only, not every available tool.

## Adaptation

1. Deploy your own secure OAuth-protected MCP server and outbound Windows device agent (not supplied here).
2. Replace https://relay.example.com/mcp in mcp.json with the address of YOUR secure server.
3. Replace example.com placeholder support, legal and website URLs in plugin.json.
4. Configure HTTPS, PKCE/OAuth and access controls; never place secrets in a manifest or repository.
5. Connect your authenticated private MCP server to ChatGPT.

## Repository contents

- plugin.json — public plugin listing TEMPLATE
- mcp.json — MCP server URL TEMPLATE
- skills/myrc-control/SKILL.md — safe operating instructions
- assets/icon.svg, assets/logo.svg — icon artwork
- SECURITY.md — security boundaries

## Ownership and licensing

Proprietary runtime/source is NOT included. No license to the private MyRC Direct server, agent or wrapper is granted by this repository. Third-party names and marks belong to their respective owners.

The owner-device Windows control server must remain bound to loopback; the agent initiates outbound TLS sessions to an authenticated relay. Publishing this template does not grant access to the owner's private service.
