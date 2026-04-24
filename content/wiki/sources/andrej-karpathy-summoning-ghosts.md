---
type: source
title: "Andrej Karpathy — We're summoning ghosts, not building animals"
source_type: transcript
date_ingested: 2026-04-25
original_file: raw/podcasts/Andrej Karpathy — We're summoning ghosts, not building animals.md
tags: [ai, llm, karpathy, education, software-engineering, vibe-coding, neural-networks, cognition, openai]
---

# Andrej Karpathy — We're summoning ghosts, not building animals

**Source type:** Transcript (podcast interview)  
**Host:** Dwarkesh Patel  
**Original:** [[raw/podcasts/Andrej Karpathy — We're summoning ghosts, not building animals]]  
**Ingested:** 2026-04-25

---

## Summary

Andrej Karpathy — former OpenAI (GPT-4 era) and Tesla Autopilot research lead, now independent educator — gives one of the most intellectually rich interviews in this wiki. The conversation spans: what LLMs actually are (a "distillation of humanity" — summoning ghosts from the corpus, not building animals); the three modes of working with code (scratch / autocomplete / vibe-coding agents); LLM cognitive deficits (no persistent memory, poor metacognition, context window blindness); the nanochat project; education philosophy (untangling knowledge into a ramp); and the research taste question (beauty, simplicity, brain-inspired intuition).

The title phrase — "summoning ghosts" — is Karpathy's reframe of what LLMs are. They are not intelligent agents in the sci-fi sense. They are distillations of everything humans have ever written. When you prompt an LLM, you are summoning a statistical ghost of the people whose writing trained it. This reframe has deep implications for how to think about alignment, about what LLMs can and can't do, and about why they behave strangely at the edges.

---

## Key Claims

- **LLMs as ghosts, not animals**: LLMs are a compression/distillation of human-generated text. They simulate what a human would write in a given context. They are not novel intelligences — they are pattern-matched reconstructions of human thought.
- **Three modes of AI-assisted coding**: (1) Write from scratch — increasingly wrong approach; (2) Autocomplete-assisted — Andrej's current mode; (3) Vibe coding / agents — good for boilerplate, bad for intellectually intense novel code. Nanochat was an example where agents were not helpful because the code was uniquely structured, not boilerplate.
- **LLM cognitive deficits**: No persistent memory across sessions; poor metacognition (can't tell when it doesn't know); context window blindness (doesn't track what's been used); can produce plausible-sounding wrong answers because plausibility is what training optimizes for.
- **Education philosophy — untangling knowledge**: Great education is a "ramp where everything only depends on the thing before it." The goal is to find the minimal, motivated presentation of an idea. The micrograd insight: neural net backpropagation is 100 lines of code. The nanochat insight: build from scratch, never copy-paste. "If I can't build it, I don't understand it."
- **On the future of neural nets**: Likely still giant nets with gradient descent in 10 years, but bigger. The 1989 → 2024 exercise showed that algorithms, data, compute, and software all improved roughly equally — no dominant factor.
- **Research taste**: Guide by aesthetic — beauty, simplicity, brain-inspired intuition. The brain is a good source of top-down prior when experiments fail. "Ugliness has no room."
- **Two types of knowledge**: Surface knowledge (can explain it) vs deep knowledge (can build it). Building forces you to encounter gaps you didn't know you had.
- **Self-play and diversity**: Agents competing with each other might generate diversity of approaches, but current self-play is too narrow (only good for strategic/social skills). RL adversarial setups (prover-verifier, LLM-as-judge) are the better modern form.

---

## Notable Quotes

> "We're summoning ghosts, not building animals. LLMs are a distillation of humanity — whatever humanity has ever written." — Andrej Karpathy

> "If I can't build it, I don't understand it." — Andrej Karpathy (crediting Feynman)

> "Ugliness has no room. It's beauty, simplicity, elegance, correct inspiration from the brain. All need to be present simultaneously." — Andrej Karpathy (on research taste)

> "The narration of how they would explain it to you over lunch is in 100% of cases more understandable and more accurate than the paper they wrote." — Andrej Karpathy (on scientific communication)

> "You take certain things for granted, and you can't put yourself in the shoes of new people who are starting out. This is pervasive and happens to me as well." — Andrej Karpathy (on the curse of expertise)

---

## Connections

- Extends [[wiki/concepts/agentic-engineering]] — Andrej's three-mode coding framework directly complements Peter Steinberger's agentic engineering vs vibe coding distinction
- Extends [[wiki/concepts/ai-psychosis]] — the "summoning ghosts" framing is a corrective to both uncritical trust and catastrophic fear
- New primary source for [[wiki/concepts/llm-nature]] (new concept) — what LLMs fundamentally are
- New primary source for [[wiki/concepts/vibe-coding]] (new concept, complement to agentic-engineering)
- Related to [[wiki/concepts/scaling-laws]] — Andrej's 1989 exercise shows all factors (data, compute, algorithms, software) improve roughly equally; no single dominant lever

---

## Questions Raised

- Does the "summoning ghosts" framing imply an upper limit on LLM capability — i.e., can they ever transcend the human distribution they're trained on?
- Andrej says agents are bad for intellectually novel code. Does this change as models get smarter (Mythos/beyond)?
- How does the LLM metacognition problem (can't tell when it's wrong) interact with agentic systems that take real-world actions?
- nanochat was released right before this interview — what was the reception, and has it become a standard educational resource?
