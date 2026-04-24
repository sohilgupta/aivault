---
type: concept
title: "LLM Nature — Summoning Ghosts"
tags: [llm, cognition, alignment, karpathy, philosophy, training]
---

# LLM Nature — Summoning Ghosts

## Definition

"Summoning ghosts, not building animals" is [[wiki/entities/andrej-karpathy]]'s reframe of what large language models fundamentally are. LLMs are not novel intelligences constructed from first principles — they are a **distillation of humanity**: the statistical compression of everything humans have ever written. When you prompt an LLM, you are not talking to a thinking machine; you are summoning a pattern-matched reconstruction of the humans whose writing trained it.

## Why This Framing Matters

The framing has deep downstream implications:

### 1. On capabilities and limits
LLMs can produce any output that a human would plausibly produce in that context. They cannot produce outputs that are systematically outside the distribution of human writing. This sets a ceiling — but also explains their surprising breadth. They can write poetry, code, legal arguments, therapy scripts, philosophical treatises — because humans have written all of those.

### 2. On alignment
If LLMs are ghosts of humanity, the alignment problem is partly a *curation* problem: which humans' writing do you want to summon? A model trained on a curated, high-quality corpus will summon better ghosts. RLHF and Constitutional AI are mechanisms for preferring some ghosts over others.

### 3. On cognitive deficits
LLMs have specific failure modes that are explicable under this framing:
- **No persistent memory**: Each session starts fresh — the ghost doesn't remember previous conversations.
- **Poor metacognition**: Humans often don't know what they don't know; LLMs inherit this deficit and can produce plausible-sounding wrong answers confidently.
- **Context window blindness**: The ghost doesn't track how much of the "room" (context window) has been used.
- **Plausibility optimised, not truth optimised**: Training on human text means training on what humans find plausible — which is not always what is true.

### 4. On creativity
Can ghosts be creative? They can recombine and interpolate in ways their training authors never explicitly did. Whether this constitutes genuine creativity or sophisticated interpolation is a philosophically open question.

## Relationship to the "Summoning" Metaphor

The metaphor cuts two ways:
- **Comforting**: LLMs are not alien intelligences; they are reflections of us.
- **Unsettling**: Which aspects of humanity are being reflected? All of it — the wisdom and the delusion, the insight and the prejudice.

## Key Sources

- [[wiki/sources/andrej-karpathy-summoning-ghosts]] — primary; Karpathy's articulation of the ghost framing, cognitive deficits, and implications

## Related Concepts

- [[wiki/concepts/ai-psychosis]] — the ghost framing is a corrective: LLMs are neither gods nor animals; they are mirrors
- [[wiki/concepts/agentic-engineering]] — if LLMs are ghosts, agentic engineering is the craft of directing ghosts effectively
- [[wiki/concepts/scaling-laws]] — more compute → a more detailed, higher-resolution ghost of the corpus

## Open Questions

- Can LLMs transcend their training distribution, or are they fundamentally bounded by human-generated text?
- Does the ghost framing still hold for models trained on synthetic data (where the "humans" who wrote it are other LLMs)?
- What happens to the ghost metaphor when continual learning arrives (Ilya's thesis) — does the model become something that grows beyond its initial distillation?
