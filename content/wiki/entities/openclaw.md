---
type: entity
title: "OpenClaw"
entity_type: product
tags: [ai-agent, open-source, personal-assistant, agentic-loop]
---

# OpenClaw

**Type:** Open-source software product
**Also known as:** Formerly WA-Relay → Claude's → ClaudeBot → MoltBot → **OpenClaw**
**GitHub:** 180,000+ stars at time of podcast (fastest-growing repo in GitHub history)
**Tagline:** "The AI that actually does things"
**Created by:** [[wiki/entities/peter-steinberger]]

## Overview

OpenClaw is an open-source personal AI agent that runs on your computer, has configurable access to all your data and system, and communicates through everyday messaging clients (WhatsApp, Telegram, Discord, Signal, iMessage). It uses pluggable AI models (Claude Opus 4.6, GPT-5.3 Codex, local models) and can be extended with CLIs and skills. Built in TypeScript.

## Architecture Layers

| Layer | Description |
|---|---|
| **Gateway** | Messaging client integration; receives and sends messages |
| **Harness** | Agent runtime; orchestrates the agentic loop |
| **Agentic loop** | Read message → call model with tools → execute tools → respond |
| **Skills** | Markdown files that describe CLI tools the agent can call |
| **Memory** | Markdown files + vector database; persistent memory across sessions |
| **Heartbeat** | Cron jobs that trigger proactive agent actions (follow-ups, check-ins) |
| **soul.md** | Private personality and values document; agent can modify with consent |
| **agents.md / AGENTS.md** | Capability and configuration document the agent reads at session start |

## Key Design Decisions

- **Skills over MCPs**: Skills (single sentence + CLI reference) are preferred over Model Context Protocol. CLIs compose naturally with pipes and tools like JQ; MCPs clutter context windows and require special training.
- **Self-aware**: The agent knows its own source code, model, documentation location, and runtime harness. This enabled emergent self-modification without being planned.
- **Proactive via Heartbeat**: A regular cron job triggers the agent to take initiative — check in on you, ask follow-ups, act on scheduled context.
- **No forced plan mode**: Peter prefers direct conversation + trigger words ("discuss", "give me options") over structured plan modes.
- **TypeScript**: Chosen for accessibility, ecosystem, and agent familiarity in the training corpus.

## Name Change Saga

WA-Relay → Claude's (TARDIS metaphor) → ClaudeBot (Anthropic requested change) → MoltBot (crypto squatters sniped the accounts in 5 seconds during rename) → **OpenClaw** (coordinated "war room" rename; $10K for Twitter handle). See [[wiki/sources/openclaw-lex-fridman-491]] for full drama.

## Security Posture

- Don't expose debug interface to public internet.
- Use capable models — smarter models are more resilient to prompt injection.
- Don't use weak local models if security matters.
- Skills checked via VirusTotal/AI integration.
- Sandbox + allow-list available for restrictive deployments.
- Prompt injection is an open industry problem but modern models are far more resilient than older ones.

## Appearances in Sources

- [[wiki/sources/openclaw-lex-fridman-491]] — origin story, architecture, security, viral growth, acquisition

## Connections

- Created by [[wiki/entities/peter-steinberger]]
- Related to [[wiki/entities/moltbook]] — MoltBook was built on top of OpenClaw
- Central to [[wiki/concepts/personal-agents]]
- Embodies [[wiki/concepts/agentic-loop]]
- Relates to [[wiki/concepts/mcps-vs-skills]]
- Relates to [[wiki/concepts/soul-md]]
- Related to [[wiki/concepts/prompt-injection]]
