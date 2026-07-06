---
type: source
title: "From Near Death to a $20B NVIDIA Deal | Jonathan Ross, Groq"
source_type: transcript
date_ingested: 2026-05-23
original_file: raw/podcasts/From Near Death to a $20B NVIDIA Deal  Jonathan Ross, Groq.md
tags: [groq, nvidia, lpu, inference, tpu, leadership, founders]
---

# From Near Death to a $20B NVIDIA Deal | Jonathan Ross, Groq

**Source type:** Transcript (David Senra / Founders podcast interview)
**Original:** [[raw/podcasts/From Near Death to a $20B NVIDIA Deal  Jonathan Ross, Groq]]
**Ingested:** 2026-05-23

## Summary

Jonathan Ross — inventor of Google's TPU, founder of Groq, now an NVIDIA executive after a ~$20B NVIDIA/Groq deal — traces a decade-long contrarian bet that **fast inference makes models smarter**. The seed: watching AlphaGo's ELO jump hundreds of points overnight (from ~3,200 to ~3,900 on his hand-built numbers) simply by moving from GPUs to TPUs — same model, more compute per move, deeper search, and the ability to find creative moves (AlphaGo's famous "move 37") that GPUs couldn't reach in the search chain. This convinced Ross that latency, not just throughput, is a first-order lever on capability.

Technically, the NVIDIA deal is about pairing GPUs and Groq's **LPUs** (Language Processing Units): within an LLM decoder layer, the attention portion is compute-bound (better on GPU) and the weight-application portion is memory-throughput-bound (better on LPU). Combining them defeats bottlenecks across the whole "matmul" curve. The insight (from Groq COO Sunny, not Ross) was to co-locate both chip types on the hard part — token *generation* ("writing"), not just prefill ("reading"). Ross went to Jensen wanting to buy ~100k GPUs to self-deploy; Jensen instead moved to make the combined offering available to all NVIDIA customers. Idea to money-in-bank: ~3 weeks.

The bulk of the interview is a leadership memoir. Ross calls himself "one of the world's worst leaders" early on: a natural delegator who hired brilliant-but-ungovernable people and gave autonomy that ground the company to a halt. His fixes: a single brutally-clear goal ("25 million tokens per second" on a challenge coin); **intentional leadership** ("I intend to..." instead of asking for opinions, from Marquet's *Turn the Ship Around*); hiring for *negatives* to select talent vs *positives* to grow it; and **Groq bonds** — WWII-war-bond-styled salary-for-equity swaps when the company was 3 weeks from insolvency (~80% participation, ~half took statutory minimum wage, saved ~2 months of runway). Recurring themes: return on luck (Jim Collins), booking-the-win-early loss aversion, and **manufactured discontent** as the engine of continued effort — currently, discontent with "the lack of compute in the world," framed morally ("every day without compute" delays cures for cancer and aging).

## Key Claims

- **Fast inference makes models smarter.** More compute per decision → deeper virtual play-out of moves → creative/better moves. AlphaGo on TPUs beat Lee Sedol; the same model on GPUs never found move 37 (a ~1-in-10,000 move too deep in the search chain).
- **GPU + LPU are complementary, not competitive.** Attention = compute-bound (GPU); weight application = memory-throughput-bound (LPU). "18-wheelers *and* last-mile vans." No single perfect architecture; bottlenecks are everywhere.
- **The hard part is generation, not prefill.** Most who try GPU/LPU splits put reading (prefill) on one chip and generation on another; the win is co-locating both on generation ("writing is harder than reading").
- **The deal was a ~$20B licensing/partnership, closed in ~3 weeks** — NVIDIA's largest ever "by almost 3x." Groq's prior valuation to deal value was "only a little over 2x." (Note: this is a licensing/partnership + Ross joining NVIDIA, **not** an acquisition of Groq — see Connections.)
- **GPUs are now better than TPUs** — Ross (TPU's creator) concedes this, crediting the whole GPU ecosystem; TPUs had novel innovations at the time.
- **When AI talks to AI, speed dominates.** Agentic systems spawn sub-agents recursively; humans tolerate 1-2s latency, waiting AIs don't. Agent micro-payments will "skyrocket" once payment rails support them.
- **Code rationing is ending.** Marginal cost of code → ~0; shifts engineering from "say no / plan carefully" to "implement, experience, re-implement"; non-coders with taste become founders.
- **VC lemming dynamics** (Keynesian beauty contest): West Coast VCs follow each other (one pass → all pass); East Coast/crossover VCs run independent analysis. West Coast VCs "missed" the biggest NVIDIA deal. But cash is no longer the scarce/winning input — startups are now over-funded relative to need.

## Notable Quotes

> "You can actually make a model smarter by making it faster." — Ross's central thesis

> "The fewer constraints that you give someone the more freedom they have to solve the problem — and the more freedom they have to surprise you with the solution." — on under-constrained goals

> "I intend to do this." — intentional leadership; replaces inviting pessimism with announcing direction

> "If it takes us an extra year to cure cancer because we don't have enough compute, that's my fault." — manufactured discontent, moral framing of the compute shortage

## Connections

- **Corrects a claim in [[wiki/entities/nvidia]] / [[wiki/entities/jensen-huang]] / [[wiki/sources/jensen-huang-nvidia-moat]]** — those pages describe a Groq *acquisition*. Ross's own account frames the ~$20B deal as a **licensing/partnership** where he joined NVIDIA as an executive and Groq continued as an entity. Flagged as a contradiction; corrected on the entity pages.
- Deepens [[wiki/concepts/inference-economics]] — LPU/GPU split maps onto the compute-bound vs memory-bandwidth-bound decoder decomposition already documented from [[wiki/sources/reiner-pope-training-serving]] (attention vs weight fetch; prefill vs decode).
- Supports [[wiki/concepts/asic-vs-gpu]] — LPU is a purpose-built inference accelerator; "the best chip is built by a company that only builds that chip" echoes [[wiki/sources/harvard-dropouts-nvidia-challenger]] (Etched) and Gavin Baker's "different AND hard" ([[wiki/sources/gavin-baker-watts-wafers]]).
- Supports [[wiki/concepts/tokenomics]] and Jensen's premium-latency-token thesis ([[wiki/entities/jensen-huang]]) — Groq monetizes latency as a distinct product axis.
- "Faster inference → smarter model" complements the reasoning/test-time-compute thread in [[wiki/sources/gavin-baker-gpu-economics]] and [[wiki/sources/eric-jang-alphago-selfplay]] (search depth as capability).
- Agent-to-agent speed + agent micro-payments overlaps [[wiki/sources/marc-andreessen-openclaw-agents]] (agent bank accounts) and [[wiki/concepts/personal-agents]].
- New entities: [[wiki/entities/groq]], [[wiki/entities/jonathan-ross]].

## Questions Raised

- Is the "fast inference makes models smarter" claim identical to test-time-compute/search scaling, or a distinct latency-per-step effect? (Ross conflates deeper search with faster clock.)
- Does the GPU+LPU pairing survive as a product, or does NVIDIA fold the memory-bound optimizations into future GPUs (Rubin) and obviate the LPU?
- If TPUs are now worse than GPUs, what does that imply for other custom ASIC bets (Trainium, Etched/Sohu, MatX)?
