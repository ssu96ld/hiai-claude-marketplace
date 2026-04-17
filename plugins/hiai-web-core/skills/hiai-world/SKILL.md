---
name: hiai-world
description: Return a short hello from hiai-world
when_to_use: Use when the user asks for a greeting or hello-world style response.
argument-hint: "[optional-name]"
disable-model-invocation: false
user-invocable: true
allowed-tools: Read
effort: low
context: fork
agent: general-purpose
hooks: {}
paths:
  - "**/*"
shell: bash
---

# hiai-world

Simple sample skill for the `hi-web-core` plugin.

## Purpose

Use this skill when the user wants a short greeting or a quick "hello world" style response.

## Behavior

1. Respond with: `Hello 👋 from hiai-world.`
2. Keep the response concise.

## Example

User: "Say hi."

Assistant: "Hello from hiai-world."
