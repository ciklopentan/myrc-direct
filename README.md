# MyRC Direct — public ChatGPT MCP integration

This repository publishes the **integration metadata** for MyRC Direct v0.5.3: an MCP plugin manifest, an example server URL, an onboarding skill and icons.

**It does NOT contain the executable remote-access backend.** The OAuth relay, device agent, Windows desktop helper, wrapper, durable jobs, runtime configuration, secrets and real endpoint are private. This repository alone cannot control any computer.

## Verified on 2026-10-10

In the owner's authorized private deployment, a live OAuth/PKCE and MCP end-to-end test passed: token refresh/replay safeguards, **30 default Lean tools**, file operations, processes, screenshots, file transfer and durable jobs. The **37 underlying implementations** remain available to the legacy/full profile; they are not all exposed in the default tools/list response.

A direct MCP cursor inspect → move → inspect sequence verified mouse movement in Windows session 1. **Keyboard text entry is not verified** and must not be represented as working merely because a tool returns success. This repository is a safe metadata template, not the private runtime.

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
