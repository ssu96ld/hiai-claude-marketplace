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

- `marketplace.json` - catalog index that lists installable plugins
- `plugins/hi-web-core/` - shared core plugin currently in catalog
- `templates/service-plugin/` - copy this to create a new client-facing service plugin
- `templates/mcp-service/` - minimal MCP service packaging template
- `docs/client-onboarding-template.md` - reusable setup guide for each client
- `docs/agency-packaging.md` - recommended packaging model for skills and MCPs

## Add this marketplace to Claude

1. Host this repo publicly (for example on GitHub).
2. Copy the public URL to `marketplace.json`.
3. In Claude settings, add a marketplace source using that URL.
4. Install plugin `hi-web-core` (and later any service plugins you add).

## Add a new service plugin

1. Copy `templates/service-plugin/` to `plugins/<service-id>/`.
2. Update the new `plugins/<service-id>/plugin.json`.
3. Create or update skills under `plugins/<service-id>/skills/`.
4. Register the plugin in `marketplace.json`.

## Package MCP-backed services

Use `templates/mcp-service/` for each MCP-backed service. Keep each service isolated so clients can enable or remove it without affecting unrelated services.
