# Empire Edge MCP client examples

Access control, DNS and CDN for your applications. Managed DNS $0/mo · Edge CDN $0/mo · Solo $99/mo · Team $499/mo · Enterprise $2500/mo

This repository holds small, working examples for the hosted **Empire Edge** MCP server. It is maintained by Elite AI Empire. The server itself is hosted; nothing here runs it.

- Product: https://cloud.eliteaiempire.com/edge/
- MCP endpoint (streamable HTTP): `https://access.eliteaiempire.com/mcp`
- OpenAPI: https://cloud.eliteaiempire.com/edge/openapi.json
- Pricing, machine readable: https://cloud.eliteaiempire.com/edge/pricing.json
- Discovery file: https://cloud.eliteaiempire.com/edge/.well-known/mcp.json

## Tools

| Tool | What it does |
|---|---|
| `approvalgate_get_status` | Read Approval Gate backend health (ok/degraded). |
| `approvalgate_list_requests` | List this account's approval requests (newest first, max 100). |
| `approvalgate_get_request` | Get one approval request by id. |
| `approvalgate_get_usage` | Read 30-day usage, free quota and billable units. |
| `approvalgate_export` | Export all of this account's objects (keys metadata, requests, usage) as JSON. |
| `approvalgate_file_request` | WRITE: file a human sign-off request (state PENDING_OWNER_SIGN). Metered: 1 request_filed. Requires confirm=true. Granting is owner-only and is not available as |

## Try it

```bash
bash examples/initialize.sh
python3 examples/client.py
```

`examples/client.py` uses only the Python standard library. It sends `initialize` and `tools/list` and prints the result. No key is needed for the public read tools. Tools that need an account say so in their description.

## Registry

Listed in the official MCP registry. Server manifest: `server.json`.

## Licence

MIT. See `LICENSE`.
