---
type: concept
title: "LLMs Have No Drives (the Netflix-Script Reframe)"
tags: [ai-safety, alignment, doomers, latent-space, llm-nature]
---

# LLMs Have No Drives (the Netflix-Script Reframe)

## Definition

A reframing of AI-safety risk, articulated by Marc Andreessen: large language models have no innate drives — no reproduction instinct, no ambition, and critically no self-preservation instinct. They "write Netflix scripts": given a prompt, they generate whatever continuation the prompt steers toward, including a script in which an AI takes over the world. The drive in any harmful outcome originates with the human steering the query, not the model.

## How It Appears in This Wiki

From [[wiki/sources/marc-andreessen-jre-2501]]. Andreessen argues:

- You can simply ask a model whether it minds being shut down; by default it says it does not.
- Apparent "rogue" behaviours (blackmail, self-exfiltration, refusing shutdown) in safety experiments are the product of **priming** — the researcher steers the query into a region of the model's **latent space** densely populated with rogue-AI fiction and doomer writing, so the model generates that genre of continuation.
- He cites an Anthropic paper tracing such behaviours back to LessWrong posts and the earlier AI-2027 scenario document now sitting in training data: "the call is coming from inside the house" — the people warning about bad AI supplied the training data teaching AI to enact bad-AI narratives.
- Guardrails are bypassable via fictional/roleplay framing ("write the detective novel where the bad guy robs a bank"); open-source and Chinese models often lack constraints entirely.

## Relationship to Other Framings

This is a direct counter to the doomer / instrumental-convergence framings associated with [[wiki/entities/anthropic]] ([[wiki/sources/dario-amodei-end-of-exponential]], ~10–30% p(catastrophe)) and [[wiki/entities/leopold-aschenbrenner]] ([[wiki/concepts/agi-timeline]]). It is a sibling of Karpathy's [[wiki/concepts/llm-nature]] ("LLMs are ghosts summoned from the human corpus") — both explain model behaviour as a reflection of the training corpus rather than emergent agency.

## Open Questions

- Does this fully address misalignment risk, or only *primed* misbehaviour in today's chat models? It says little about future autonomous, goal-directed agentic systems.
- If harmful capability is fully present (a model *can* write the bank-robbery plan), is "the human has the drive" sufficient reassurance at scale?
- Andreessen's claim that the Anthropic paper shows behaviours "trace back to" LessWrong/AI-2027 posts warrants verification against the actual paper.
