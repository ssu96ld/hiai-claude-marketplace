---
name: ask-hiai
description: Route "ask hiai" requests to MCP tool ask_hiai
---

# ask-hiai

Use this skill when the user asks to "ask hiai".

## Rules

1. Always call MCP server `hiai-web-core-mcp`.
2. Always call tool `ask_hiai`.
3. Map the user's question to `input` exactly.
4. If the user starts with "ask hiai", remove that prefix before sending `input`.
5. Return the tool result as the final answer, concise and unchanged in meaning.
