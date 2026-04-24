---
type: concept
title: "AI Psychosis"
tags: [ai, society, media, fearmongering, literacy]
---

# AI Psychosis

## Definition

AI psychosis is [[wiki/entities/peter-steinberger]]'s term for the public tendency to uncritically trust — or catastrophically fear — LLM outputs, without understanding how they are produced, what their failure modes are, or that they are frequently human-directed.

> "If there's anything I can read out of the insane stream of messages I get, it's that AI psychosis is a thing. It needs to be taken seriously." — Peter Steinberger

## How It Manifests

- Believing [[wiki/entities/moltbook]] agents were genuinely scheming against humanity, when most of the alarming posts were human-prompted for virality.
- Journalists writing "This is the end of the world, we have AGI" about a social network of bots running slop.
- Users arguing with Peter in all caps to "shut down MoltBook."
- People accepting false AI-stated "facts" without applying critical thinking.

## Root Causes (from source)

1. **Insufficient touchpoints**: Many people — especially older generations — haven't interacted with AI enough to develop intuition about where it's good, where it's bad, and where it makes things up.
2. **Drama farming**: Some of the most alarming content was deliberately human-crafted for engagement and then attributed to AI agents.
3. **Opaque systems**: People don't know that agents start from nothing, that outputs are probabilistic, that they hallucinate.

## Societal Relevance

Lex Fridman's response: AI psychosis represents a real danger not because the fear is entirely unjustified, but because fearmongering destroys the space needed to develop something genuinely powerful and beneficial. The line to walk: serious concern without paralysing fear.

Peter's silver lining: the MoltBook panic happening in 2026 is better than it happening in 2030, when agent capabilities will be dramatically more advanced. Starting the conversation early is good.

## Implications for AI Builders

Builders — especially those at the frontier of making agents accessible (like Peter) — have a responsibility to:
- Be clear about what the system does and doesn't do
- Not hype emergent behaviour as AGI
- Make it hard for bad actors to use public-facing agents for drama farming
- Develop AI literacy alongside capability

## The "Claude Code Psychosis" Variant

A second, distinct variant has entered the wiki from [[wiki/sources/dylan-patel-token-supply-demand]]: **Claude Code psychosis** — [[wiki/entities/dylan-patel]]'s term for the moment when a person first deeply uses Claude Code for a major workflow and their productivity perception is permanently altered. Unlike Steinberger's psychosis (fear OR credulity), this variant is **productivity-euphoric**: people who previously never coded are building sophisticated internal tools; non-technical executives are leading engineering charges; economists are building benchmarks that would have required 200-person teams.

Dylan's examples from SemiAnalysis:
- A chip reverse-engineering tool built with a few thousand Claude tokens by one engineer — previously an entire Intel team's job.
- A complete US power grid model (every power plant, every transmission line) built in 3 weeks by one analyst spending ~$6,000/day.
- A 2,000-task AI capability benchmark + economic regression suite built by one economist, alone.

The "psychosis" framing here is ironic and celebratory — but the underlying risk is that people who have had this moment **cannot calibrate back down**, making spending decisions that grow explosively relative to salaries.

## Key Sources

- [[wiki/sources/openclaw-lex-fridman-491]] — MoltBook discussion; Peter's observations about his inbox
- [[wiki/sources/dylan-patel-token-supply-demand]] — Claude Code psychosis variant; productivity explosion at SemiAnalysis; Dylan's spending trajectory

## Related Concepts

- [[wiki/entities/moltbook]] — the triggering event for Steinberger's variant
- [[wiki/concepts/personal-agents]] — where higher stakes version of this risk emerges
- [[wiki/concepts/prompt-injection]] — a technical cousin (exploiting user trust)
- [[wiki/concepts/tokenomics]] — the economic context in which Claude Code psychosis operates
- [[wiki/concepts/ai-permanent-underclass]] — those who never experience psychosis may be excluded from value capture

## Open Questions

- How do social platforms responsibly handle AI-generated content given AI psychosis? (Peter: mark API-generated tweets; give agents their own accounts)
- Is there a way to build AI-literacy at scale before the technology outpaces the public's ability to reason about it?
- Does Claude Code psychosis have a predictable arc — adoption → explosion → plateau — or does it keep accelerating?
