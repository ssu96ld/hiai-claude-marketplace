# hiai Claude Marketplace

Agency-ready Claude marketplace starter.

Current live plugin:

- `hi-web-core`
  - Skill: `hiai-world`

## Goals

- Let clients add one marketplace source once.
- Let clients install only the service plugins they need.
- Keep services modular so you can update independently.

## Repository structure

- `.claude-plugin/marketplace.json` - marketplace manifest (Anthropic format)
- `plugins/hi-web-core/.claude-plugin/plugin.json` - plugin manifest
- `plugins/hi-web-core/skills/hiai-world/SKILL.md` - sample skill
- `templates/service-plugin/` - copy this to create a new client-facing service plugin
- `templates/mcp-service/` - minimal MCP service packaging template
- `docs/client-onboarding-template.md` - reusable setup guide for each client
- `docs/agency-packaging.md` - recommended packaging model for skills and MCPs

## Add this marketplace to Claude

1. Host this repo publicly (for example on GitHub).
2. Ensure the repo contains `.claude-plugin/marketplace.json` (this repo does).
3. Add the marketplace source:
   - Claude chat command: `/plugin marketplace add <github-owner>/<repo>`
   - Or use Claude settings UI marketplace source flow.
4. Install plugin `hi-web-core` (and later any service plugins you add).

## Add a new service plugin

1. Copy `templates/service-plugin/` to `plugins/<service-id>/`.
2. Add `plugins/<service-id>/.claude-plugin/plugin.json`.
3. Create or update skills under `plugins/<service-id>/skills/`.
4. Register the plugin in `.claude-plugin/marketplace.json` with `name` and `source`.

## Package MCP-backed services

Use `templates/mcp-service/` for each MCP-backed service. Keep each service isolated so clients can enable or remove it without affecting unrelated services.

## Current MCP configuration

`hi-web-core` includes one remote MCP server:

- Name: `hiai-web-core-mcp`
- URL: `https://kindling-dev.hiai.studio/mcp/883cff48-8f22-43ef-ad12-04db761f4ac1`
- API key env var: `HIAI_MCP_API_KEY`

## Validate locally

From marketplace root, run:

- `/plugin validate .`
