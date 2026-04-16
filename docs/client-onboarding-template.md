# Client onboarding template

Use this template for each client so setup is fast and repeatable.

## 1) Add marketplace source

Marketplace URL:

`<https://your-host/marketplace.json>`

In Claude settings, add this as a marketplace source.

## 2) Install purchased plugins

Enable only the plugins included in the client's package:

- `<plugin-id-1>`
- `<plugin-id-2>`

## 3) Configure credentials (if required)

For MCP-backed `hi-web-core`, set:

- `HIAI_MCP_API_KEY=<client-api-key>`
- MCP server: `hiai-web-core-mcp`
- Endpoint: `https://kindling-dev.hiai.studio/mcp/883cff48-8f22-43ef-ad12-04db761f4ac1`

Then confirm connectivity in Claude by running:

`/plugin validate .`

## 4) Verify installation

Run this smoke test prompt in Claude:

`Use <skill-id> and return a one-line confirmation.`

Expected result:

`<short expected response>`

## 5) Support handoff

- Owner: `<agency contact>`
- SLA: `<response window>`
- Change log URL: `<link>`
