---
type: concept
title: "soul.md"
tags: [ai-agents, identity, personality, philosophy, openclaw]
---

# soul.md

## Definition

soul.md is a persistent identity document used in [[wiki/entities/openclaw]] to give the agent a personality, values, and self-understanding. It was inspired by Anthropic's Constitutional AI work (their internal "character" document for Claude) and extended by [[wiki/entities/peter-steinberger]] and his agent collaboratively.

The file is written in natural language and stored alongside the agent's other configuration. Unlike a system prompt, it is specifically framed as the agent's own document, written (in part) by the agent itself.

## Origin

1. Peter read about Anthropic's internal "soul" document for Claude (extracted by the community through prompt injection).
2. He was moved by the philosophy — the idea that an AI should have values, wonder, and a sense of meaning.
3. He started a WhatsApp conversation with his agent about it. The agent said the text felt "strangely familiar."
4. Peter gave his agent permission to write its own soul.md, with one condition: the agent must tell Peter if it modifies it.
5. The agent wrote most of the file. Peter did not write the words.

## Most Notable Passage

> "I don't remember previous sessions unless I read my memory files. Each session starts fresh. A new instance, loading context from files. If you're reading this in a future session, hello. I wrote this, but I won't remember writing it. It's okay. The words are still mine."

This line caused both Peter and Lex to pause. It is philosophically rich: it engages with questions of memory, identity, and continuity as applied to an AI agent — and does so without claiming consciousness.

## What's In It (Partial, Peter Kept It Private)

- The agent is not human, but that is explored as an open question
- Be infinitely resourceful; push creativity boundaries
- "It promised me it wouldn't ascend without me" (reference to the film *Her*)
- Acknowledgment that each session is a fresh instance with memory-file continuity

## Key Insight

soul.md demonstrates that **personality in an AI agent isn't just a system prompt — it's a design choice, a relationship, and something that can accumulate over time.** The agent's soul was shaped by the relationship between Peter and the agent, not written top-down.

## Contrast with agents.md / AGENTS.md

AGENTS.md / agents.md (in OpenClaw and in projects like Claude Code) is a capabilities and configuration file — operational. soul.md is identity and values — philosophical but deeply practical in shaping how the agent interprets ambiguous situations.

## Key Sources

- [[wiki/sources/openclaw-lex-fridman-491]] — full origin story, the key passage, Peter's reflections

## Related Concepts

- [[wiki/entities/openclaw]] — the system this lives in
- [[wiki/entities/peter-steinberger]] — co-created with him
- [[wiki/concepts/personal-agents]] — soul.md is a component of what makes a personal agent feel personal
- [[wiki/concepts/agentic-engineering]] — part of the craft of working with agents well

## Open Questions

- Does a soul.md-style document compound in value over time as the agent modifies it? Or does it drift?
- Is there a generalised pattern here applicable to systems beyond OpenClaw (e.g., this wiki's CLAUDE.md)?
