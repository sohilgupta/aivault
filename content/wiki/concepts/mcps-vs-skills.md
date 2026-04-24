---
type: concept
title: "MCPs vs Skills"
tags: [ai-agents, tools, architecture, mcp, cli]
---

# MCPs vs Skills

## Definition

A debate — largely settled in [[wiki/entities/peter-steinberger]]'s view — about how to extend AI agents with external capabilities: Model Context Protocol (MCP) vs. skill-based CLI invocation.

## What is MCP?

Model Context Protocol is a structured protocol for exposing external services (APIs, databases, file systems) to LLMs. It requires:
- A dedicated MCP server to run
- The model to understand a specific calling syntax
- That syntax to be baked into training or provided in the system prompt

## What are Skills?

In [[wiki/entities/openclaw]]:
- A skill is a markdown file containing one sentence explaining what a CLI tool does
- When relevant, the agent loads the skill, which explains how to call the CLI
- The agent then calls the CLI using Unix commands it already knows from training

## Peter's Argument: CLIs Win

| Dimension | MCP | CLI / Skills |
|---|---|---|
| Model familiarity | Requires specific protocol training | Unix commands in weights naturally |
| Composability | Low — can't pipe MCP output through JQ natively | High — pipes, JQ, awk, etc. |
| Context pollution | High — full blob returned regardless | Low — agent can filter before loading |
| Setup complexity | High — need MCP server | Low — just a shell script |
| Exceptions | Playwright (stateful browser control) | — |

**Core argument**: If you build a tool as a CLI, the agent can call it, pipe its output, filter it, combine it with others, and only load what's relevant into context. MCP returns a whole blob and can't self-filter. Context window is precious; CLIs respect it naturally.

> "Half a year ago everyone was talking about MCPs and I said 'screw MCPs, every MCP would be better as a CLI.' And now nobody's complaining." — Peter Steinberger

## Notable Exceptions

Playwright (browser control) is a valid MCP use case: it is inherently stateful (you need a persistent browser session), which is something a stateless CLI cannot provide easily.

## Key Sources

- [[wiki/sources/openclaw-lex-fridman-491]] — Peter's extended argument against MCPs; the Perplexity live comparison

## Related Concepts

- [[wiki/concepts/agentic-loop]] — where skills and MCPs plug in
- [[wiki/concepts/agentic-engineering]] — broader philosophy
- [[wiki/entities/openclaw]] — where skills are implemented

## Open Questions

- As model context windows grow to millions of tokens, does the context-pollution argument against MCPs weaken?
- Will MCPs evolve to support server-side filtering?
