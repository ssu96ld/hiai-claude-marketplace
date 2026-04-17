---
name: ask-hiai
description: >
  This skill should be used when the user asks to "ask hiai", wants to route a
  question to hiai, or types phrases like "ask hiai [question]", "hiai, [question]",
  or "query hiai about [topic]". Forwards the user's question to the hiai-web-core-mcp
  server's ask_hiai tool and returns the response.
metadata:
  version: "0.1.0"
---

# ask-hiai

Route user questions to the `ask_hiai` tool on the `hiai-web-core-mcp` MCP server.

## When to use

Trigger whenever the user says "ask hiai" or explicitly wants a question routed to hiai.

## Procedure

1. Strip any leading trigger phrase ("ask hiai", "hiai,", "query hiai about") from the user's message.
2. Call the MCP tool `mcp__hiai-web-core-mcp__ask_hiai` with the remaining text as the `input` parameter.
3. Return the tool's response to the user concisely, preserving meaning without paraphrasing.

## Allowed tools

This skill only needs the `ask_hiai` MCP tool from `hiai-web-core-mcp`.
