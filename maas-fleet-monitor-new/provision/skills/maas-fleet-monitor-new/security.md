# Security Rules

- Never print or reveal MaaS passwords, API keys, account credentials, cookies, or request bodies.
- Store the Web dashboard password in ALLO Desktop credentials or environment variables, not in Git-tracked files.
- Use only the public Web dashboard/API for this project version.
- Public Web dashboard URL is `http://221.0.79.251:39091/?v=metric1`; it uses Basic Auth username `maas`.
- Never print or reveal the Basic Auth password.
- Do not ship or configure private MCP, SSH tunnel, or ingestion tooling from this Bundle.
- Do not modify MaaS accounts, weights, routes, database rows, or credentials from this skill.
- Treat current tools as read-only diagnostics.
- Always state visibility gaps. In particular, internal MaaS has health-only visibility until the internal Agent is deployed.
