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

For any MCP-backed plugin, provide the client's service credentials and confirm connectivity.

## 4) Verify installation

Run this smoke test prompt in Claude:

`Use <skill-id> and return a one-line confirmation.`

Expected result:

`<short expected response>`

## 5) Support handoff

- Owner: `<agency contact>`
- SLA: `<response window>`
- Change log URL: `<link>`
