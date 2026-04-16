# Agency packaging model

Use this model to productize agency services into installable Claude capabilities.

## Design principles

- One marketplace source per agency.
- One plugin per service line.
- One skill set per plugin, focused on a clear outcome.
- Keep shared utilities in a separate core plugin.
- Use MCP only where external systems or tools are required.

## Recommended plugin layout

`plugins/<service-id>/plugin.json`

`plugins/<service-id>/skills/<skill-id>/SKILL.md`

## Suggested service categories

- `hi-web-core` - shared helpers and base behaviors
- `hi-seo-audit` - SEO analysis and recommendations
- `hi-content-ops` - content workflows and QA
- `hi-growth-analytics` - reporting and insights

## MCP packaging guidance

For MCP-backed services, package each service independently:

- `templates/mcp-service/manifest.json` as the starting manifest
- A dedicated auth/config per service
- Narrow permissions/scopes per service

This keeps client onboarding safer and allows clean service-level enable/disable.
