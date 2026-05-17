---
type: concept
title: "Non-Deterministic Software"
tags: [ai-product, product-management, evals, agentic-software, reliability]
---

# Non-Deterministic Software

## Definition

Non-deterministic software produces variable outputs for identical or nearly identical inputs — the behaviour cannot be fully predicted or replicated from a specification. AI-powered applications, particularly those using large language models or agentic pipelines, are inherently non-deterministic. This contrasts with classical deterministic software where if X then Y is always guaranteed.

## How It Appears in This Wiki

Introduced by [[wiki/entities/gokul-rajaram]] in [[wiki/sources/gokul-rajaram-ai-product-development]] as the central structural change in software product development. The shift from deterministic to non-deterministic software changes who owns quality — and how quality is defined, measured, and maintained.

## The Eval Problem

In deterministic software, quality control is simple: write a test, run it, check if the output is correct. In non-deterministic software:

- The "correct" output varies across contexts, users, and model states
- A small variation in input can produce a completely different output
- Human evals can't scale to the number of test cases needed
- Therefore: **you need AI to evaluate AI**

The product manager's job shifts from writing the Product Requirements Document (what to build) to owning **evaluations** (is what we built good?). Gokul argues this is now a core PM responsibility.

## Implications for Team Structure

- PM:engineer ratio is expanding from 1:3 historically toward 1:20+ as AI automates implementation
- The PM/designer/engineer separation is collapsing into bottoms-up building
- "Prototyping interviews" are now an explicit step in PM hiring loops
- Designers are being replaced at the margin by AI operating on existing design systems; a small number of "design system keepers" remains

## The Judgment Gap

Non-determinism, combined with the ability to build almost anything quickly, creates a new scarcity: **judgment**. When infinite code can be produced by AI agents, the bottleneck is knowing which outputs matter, which code is correct, and which features should be built at all. Gokul identifies this as the one future-proof human skill.

## Connection to AI Slop

The fear of AI slop (see [[wiki/concepts/ai-psychosis]]) is structurally linked to non-deterministic software: when AI can produce plausible-but-wrong outputs at scale, and when the volume of generated content is enormous, the quality signal drowns in noise. Evals are the mechanism to fight slop.

## Key Sources

- [[wiki/sources/gokul-rajaram-ai-product-development]] — primary; introduced the concept and its product management implications

## Related Concepts

- [[wiki/concepts/agentic-engineering]] — non-determinism is why agentic engineering requires discipline, not just prompts
- [[wiki/concepts/agentic-loop]] — the agentic loop is the runtime context in which non-determinism operates
- [[wiki/concepts/ai-psychosis]] — AI slop is non-deterministic software's failure mode at the output layer

## Open Questions

- Will dedicated "eval engineers" emerge as a new discipline, or will PMs absorb this role?
- What is the right benchmark for acceptable non-determinism in high-stakes applications (legal, medical, financial)?
- Can formal verification techniques from deterministic software eventually be applied to LLM outputs?
