# Security

- Never publish access tokens, OAuth client secrets, passwords, signing keys, private endpoints, IP addresses, database material, local project state, screenshot logs or credentials.
- Published JSON files use example.com domains, not a working deployment.
- Use authenticated HTTPS/OAuth with PKCE, state, issuer and redirect URI validation.
- Keep computer control services on loopback; only outbound agent connections may cross the host boundary.
- Require authorization for write, process, keyboard, mouse click and network actions.
- Use isolated reviewer accounts for review tests, never an owner's Windows machine.
- Report vulnerabilities privately to the service operator.
