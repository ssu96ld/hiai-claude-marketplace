# hiai-web-core (corrected)

Drop-in replacement files for the `hiai-web-core` plugin, corrected against the
documented plugin schema in `cowork-plugin-management/create-cowork-plugin/references/component-schemas.md`.

## Changes made

### 1. `plugin.json`
- Removed `mcpServers` block (moved to `.mcp.json`).
- Added `author` field.
- Bumped version to `0.1.3`.

### 2. `.mcp.json` (new)
- Created at plugin root.
- Changed `"type": "url"` (not a valid MCP transport) to `"type": "http"`.
  If the endpoint actually uses Server-Sent Events, change to `"type": "sse"` instead.

### 3. `skills/ask-hiai/SKILL.md` and `skills/hiai-world/SKILL.md`
- Stripped 11 non-schema frontmatter fields (`when_to_use`, `argument-hint`,
  `disable-model-invocation`, `user-invocable`, `allowed-tools`, `effort`,
  `context`, `agent`, `hooks`, `paths`, `shell`).
- Kept only the documented fields: `name`, `description`, `metadata`.
- Rewrote `description` in third-person with trigger phrases in quotes, per spec.
- Moved operational rules (allowed tools, behavior) into the SKILL.md body as prose.

## How to apply

Replace the corresponding files in your plugin source repo with these, then:

1. Bump the plugin version (already done: 0.1.3).
2. Publish / re-sync the plugin.
3. In Cowork settings, disable and re-enable the plugin (or restart).
4. Verify the skills appear in the Skill tool's list.

## Open questions

- **MCP transport type**: verify whether the `kindling-dev.hiai.studio/mcp/...`
  endpoint is HTTP streamable or SSE. Adjust `.mcp.json` accordingly.
- **Directory layout**: the documented pattern uses `.mcp.json` at plugin root.
  If your distribution tooling expects MCP config inside `plugin.json`, you may
  need to keep both until the loader is updated.
