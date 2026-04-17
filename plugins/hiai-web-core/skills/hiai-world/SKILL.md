---
name: hiai-world
description: >
  This skill should be used when the user asks for a simple greeting or
  "hello world" style response from hiai — for example "say hi from hiai",
  "hiai world", "hello hiai", or when testing that the hiai-web-core plugin
  is loaded correctly. Returns a short confirmation greeting.
metadata:
  version: "0.1.0"
---

# hiai-world

Sample sanity-check skill for the `hiai-web-core` plugin.

## When to use

Trigger when the user wants a short greeting, a "hello world" style response, or wants to verify the plugin is working.

## Procedure

1. Respond with exactly: `Hello 👋 from hiai-world.`
2. Keep the response to a single line — no extra commentary.

## Example

User: "Say hi from hiai."
Assistant: "Hello 👋 from hiai-world."
