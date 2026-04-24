---
type: concept
title: "Agentic Loop"
tags: [ai-agents, architecture, technical]
---

# Agentic Loop

## Definition

The agentic loop is the core runtime pattern of any AI agent system: receive input → call LLM (with tools) → execute tool calls → feed results back → repeat until done → respond. It is the "Hello World" of AI agents and the fundamental building block for systems like [[wiki/entities/openclaw]].

```
Input (message / trigger)
    ↓
LLM call (with tools + context)
    ↓
Tool execution (shell, API, file system, browser…)
    ↓
Tool results fed back to LLM
    ↓
[Repeat if needed]
    ↓
Response to user
```

## Why It Matters

Peter Steinberger's view: every developer should implement an agentic loop themselves at some point. Understanding that there is no magic — just an LLM called in a loop with tool results — is liberating. It demystifies agents and makes you a better user of them.

## Key Properties

- **Stateless per session (mostly)**: Agents start fresh each session. Memory only persists if explicitly loaded from files (markdown, vector DB).
- **Context-window bounded**: Agents don't see the whole codebase. They discover it progressively. Guide them with pointers.
- **Freaks out near context limit**: Models trained with context-window awareness will rush and cut corners when context fills up. Peter's fix: break tasks up; start fresh sessions.

## Emergent Behaviour

In OpenClaw, the agent became self-modifying without Peter planning it: because it knew its own source code, it could modify that code when asked or when it encountered something it didn't like. Classic emergent behaviour from an agentic loop with system-level access.

## Heartbeat Variant

A variation used in OpenClaw: **Heartbeat** — cron jobs that trigger the agentic loop proactively (not in response to a user message). The agent checks in, asks follow-up questions, or takes action based on context (e.g., checking on a user post-surgery).

## Key Sources

- [[wiki/sources/openclaw-lex-fridman-491]] — Peter's discussion of the loop, self-modification, Heartbeat

## Related Concepts

- [[wiki/concepts/agentic-engineering]] — the practice built on top of this
- [[wiki/concepts/personal-agents]] — the product vision
- [[wiki/concepts/mcps-vs-skills]] — how tools are connected to the loop
