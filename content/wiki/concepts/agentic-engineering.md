---
type: concept
title: "Agentic Engineering"
tags: [ai-agents, programming, workflow, philosophy]
---

# Agentic Engineering

## Definition

Agentic engineering is the disciplined practice of building software by directing AI agents — giving them clear architectural context, maintaining oversight, and collaborating on design decisions — as opposed to prompting carelessly without system understanding. The term was coined (or popularised) by [[wiki/entities/peter-steinberger]] as a deliberate counter to the more pejorative "vibe coding."

> "I do agentic engineering — and then maybe after 3AM I switch to vibe coding, and then I have regrets the next day." — Peter Steinberger

## Core Principles

### 1. Empathise with the agent
Agents start every session from zero. They know nothing about your project's history, the subtle bugs in module X, or why you made a particular architectural choice. Empathising with this blank-slate condition leads to better prompts: point the agent to the right files, provide architectural context, explain the intent before the implementation.

### 2. Design for agents, not for yourself
Build a codebase that is easy for an agent to navigate — obvious naming, modular structure, flat hierarchies where possible. Don't override names the agent picks; those names are from the weights and will be what the agent searches for next time.

### 3. Short prompts at the elite level
The arc: short prompts → over-orchestrated complexity → back to short natural language. The plateau is simple prompts from someone who deeply understands the system. Long prompts often indicate unclear thinking.

### 4. Use voice
Peter conducts most agent interaction via voice for natural language input. Typing is reserved for CLI commands (switching folders, running scripts).

### 5. Discuss, then build
Use trigger words ("discuss", "give me options", "don't write code yet") to enter planning mode. When ready: "okay, build." This prevents 20-minute manic runs in the wrong direction.

### 6. Ask "what can we refactor?" after every feature
Once the agent has built something, it understands the pain points it encountered. Asking for a post-build refactor suggestion harvests that knowledge.

### 7. Never revert — move forward
If something goes wrong, ask the agent to fix it rather than rolling back. Rolling back loses the intermediate work; pushing forward is usually faster.

### 8. Run multiple agents in parallel
4–10 agents simultaneously on different tasks: one building a big feature, one exploring an idea, two fixing bugs, one writing documentation.

## The Agentic Trap

A trap many developers hit: they over-architect their agent workflow — complex orchestrators, sub-agent pipelines, custom slash commands — before understanding the fundamentals. The full curve:

1. Short prompt (beginner)
2. Complex orchestration, chained agents, sub-agents (intermediate trap)
3. Short prompt again, informed by deep system understanding (elite)

The trap feels like progress because it is complicated. It isn't maturity.

## Key Sources

- [[wiki/sources/openclaw-lex-fridman-491]] — Peter's full philosophy on agentic engineering and dev workflow

## Related Concepts

- [[wiki/concepts/agentic-loop]] — the technical building block
- [[wiki/concepts/mcps-vs-skills]] — Peter's strong tooling preference
- [[wiki/concepts/personal-agents]] — the destination this workflow is building toward
- [[wiki/concepts/prompt-injection]] — security concern relevant to this workflow

## Open Questions

- Does the "empathise with the agent" principle still apply as models develop better persistent memory and session continuity?
- Is there a systematic way to document the "context" needed from a human that's more efficient than verbal briefing?
