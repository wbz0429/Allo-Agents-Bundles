# MaaS Fleet Monitor New Agent Bundle

`maas-fleet-monitor-new` is an independent Allo Agent Bundle for MaaS monitoring. It intentionally does not replace or merge with the legacy `maas-fleet-monitor` Skill directory.

## What It Provides

- A top-level Allo Agent Bundle: `maas-fleet-monitor-new`
- A bundled Skill with the same new id: `maas-fleet-monitor-new`
- Read-only access to the public MaaS Web dashboard/API
- Generated Markdown summaries and PNG chart artifacts through `scripts/web_status.py`

## Required Credential

Set the MaaS Web dashboard Basic Auth password through Allo credentials or an environment variable:

```bash
export MAAS_MONITOR_WEB_PASSWORD=...
```

Never commit or print the password.

## Local Usage

Point Allo at this repository as an external bundle root:

```bash
export ALLO_BUNDLES_ROOT=/path/to/Allo-Agents-Bundles
```

Allo should discover `maas-fleet-monitor-new/` as an Agent Bundle and provision `provision/skills/maas-fleet-monitor-new` as its Skill dependency.

## Safety

This Bundle is Web-only and read-only. It does not ship private MCP, SSH tunnel, account mutation, Provider Pool mutation, or credential-changing logic.
