---
name: heymyapps-public
description: Connect AI agents to Public using one HeyMyApps API key and actual hosted tool discovery.
---

# Public MCP setup and connection checker

Read capabilities.json and README.md. Use authenticated discovery before selecting a tool. The actual server schemas and selected connection define what can run; never infer tool names from the repository title.

Use `HEYMYAPPS_API_KEY` for HeyMyApps (`PIPMCP_API_KEY` remains a supported alias). Provider credentials belong in the hosted product. Do not request another AI model API key for these instructions. Never print keys or commit result records.

Twenty-five read tools are on by default; four trading tools (`place_order`, `place_multileg_order`, `replace_order`, `cancel_order`) are off by default and require HeyMyApps pending approvals when enabled. Confirm with the user before calling non-read-only tools. Never store Public API secrets in the repo or chat.

For a no-network setup plan run `npm start`. For authenticated discovery run `npm run doctor` after the user supplies an authorized scoped key. This is a setup utility; it does not establish an installed or live connector.

Preserve policy/approval receipts and stable idempotency keys. Pending is not completed. Uncertain writes must be reconciled; never retry with a new key to bypass a hold. Existing MCP client approval and hosted policy remain authoritative.