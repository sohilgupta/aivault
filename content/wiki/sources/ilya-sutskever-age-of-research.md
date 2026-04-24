---
type: source
title: "Ilya Sutskever — We're moving from the age of scaling to the age of research"
source_type: transcript
date_ingested: 2026-04-25
original_file: raw/podcasts/Ilya Sutskever — We're moving from the age of scaling to the age of research.md
tags: [ilya-sutskever, scaling, research, agi, safe-superintelligence, continual-learning, self-play, diversity]
---

# Ilya Sutskever — We're moving from the age of scaling to the age of research

**Source type:** Transcript (podcast interview)  
**Host:** Dwarkesh Patel  
**Original:** [[raw/podcasts/Ilya Sutskever — We're moving from the age of scaling to the age of research]]  
**Ingested:** 2026-04-25

---

## Summary

Ilya Sutskever — co-founder of OpenAI, co-author of AlexNet and GPT-3, now founder of Safe Superintelligence (SSI) — argues that the "age of scaling" (pre-training at scale) is ending. The internet data scaling wall has been hit. The next phase is the "age of research" — where the path forward requires genuine algorithmic insight, not just more compute on existing approaches. He discusses continual learning agents (human-like incremental learning vs. current train-once models), self-play as a compute-only path, diversity among AI agents, and research taste as the key differentiating skill for the next era.

---

## Key Claims

- **The age of scaling is ending**: Pre-training on internet data has hit a wall — you can't just add more. The next breakthroughs require new algorithmic ideas (synthetic data, new training paradigms, continual learning).
- **The age of research is beginning**: The differentiator going forward is research *taste* — the ability to identify which ideas are worth pursuing. This is scarce and not scalable in the way compute is.
- **Continual learning agents**: The human-like model — an AI that incrementally learns from experience in real time, like a human worker learning a job — is very different from current train-run inference. If you achieve this, one deployed instance could learn every job, building a compounding advantage.
- **But recursive self-improvement won't go as expected**: Ilya's strong intuition is that the "million Ilyas on a server" scenario (copies doing research in parallel) won't play out as imagined. In theory it works; in practice, diminishing returns and the need for *diversity* of thought will constrain it.
- **Diversity problem**: All pre-trained LLMs are weirdly similar because they train on the same internet data. Differentiation only starts with RL/post-training. To get genuinely diverse AI researchers, you need different training — not just temperature.
- **Self-play found a home in a different form**: Classical narrow self-play (game-playing) was too narrow for general intelligence. But prover-verifier, LLM-as-judge, adversarial debate — these are the modern versions that do work and create diversity pressure.
- **Research taste is the key skill**: Guided by aesthetic (beauty, simplicity), by brain-inspired intuition as a top-down prior, and by holding conviction when experiments fail. "The top-down belief sustains you when experiments contradict you."
- **SSI's mission**: Build safe superintelligence. One product, one goal. No commercial distractions. (Not described in detail in this source but frames Ilya's post-OpenAI context.)

---

## Notable Quotes

> "We're moving from the age of scaling to the age of research." — Ilya Sutskever

> "In theory there is no difference between theory and practice. In practice, there is. I think recursive self-improvement is going to be one of those." — Ilya Sutskever

> "The reason there has been no diversity is because of pre-training. All pre-trained models are pretty much the same because they train on the same data." — Ilya Sutskever

> "The top-down belief is the thing that sustains you when the experiments contradict you. You can say things have to be this way. Something like this has to work, therefore keep going." — Ilya Sutskever

---

## Connections

- Primary source for [[wiki/entities/ilya-sutskever]]
- Directly tensions [[wiki/concepts/scaling-laws]] — Ilya says the *current* scaling paradigm (pre-training data scale) has hit a wall; Dario says scaling laws still hold. These can be reconciled: compute scaling still works (Mythos), but data scaling on internet text has a ceiling.
- New source for [[wiki/concepts/post-scaling-research]] (new concept) — the algorithmic ideas needed after the data wall
- Related to [[wiki/concepts/agentic-engineering]] — continual learning agents would change what agentic engineering means

---

## Contradictions / Tensions

- **Critical tension with scaling consensus**: Dario ([[wiki/sources/dario-amodei-end-of-exponential]]) says scaling laws still hold — and Mythos is proof. Ilya says the age of scaling is *ending*. Reconciliation: Dario is talking about compute scaling (more FLOPS → better model), Ilya is talking about *data* scaling (more internet text → diminishing returns). Both can be true simultaneously.
- Ilya's skepticism about million-Ilyas recursive self-improvement conflicts with some interpretations of Dario's "end of exponential" framing. If the exponential is ending, what replaces it?

---

## Questions Raised

- What exactly is SSI building? What does a "safe superintelligence" development process look like compared to Anthropic's?
- What is the data wall exactly — is it internet text, or does high-quality synthetic data genuinely remove the ceiling?
- Continual learning agents: what are the leading technical approaches? (Ilya hints at this as a key direction without detailing specific techniques.)
- If research taste is the key differentiating skill, how do you hire for it? And can AI itself develop research taste?
