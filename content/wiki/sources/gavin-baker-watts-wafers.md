---
type: source
title: "Watts, Wafers, and the Future of AI Infra | Gavin Baker"
source_type: transcript
date_ingested: 2026-05-23
original_file: raw/podcasts/Watts, Wafers, and the Future of AI Infra  Gavin Baker.md
tags: [ai-investing, bubble, tsmc, orbital-compute, inference, pareto-frontier, bitter-lesson]
---

# Watts, Wafers, and the Future of AI Infra | Gavin Baker

**Source type:** Transcript (Invest Like The Best, Patrick O'Shaughnessy; Gavin Baker)
**Ingested:** 2026-05-23
**Original:** [[raw/podcasts/Watts, Wafers, and the Future of AI Infra  Gavin Baker]]

## Summary

Gavin Baker's sixth appearance on the show, recorded after the March/April 2026 NASDAQ sell-off. He frames Anthropic's growth as "the most extraordinary moment in the history of capitalism" (adding the combined revenue of Palantir + Snowflake + Databricks in one month) and argues AI got historically cheap while fundamentals inflected. Ranges across: Anthropic vs OpenAI capital efficiency; watts (capitalism will solve, orbital compute as the ~2027-28 unlock) vs wafers (TSMC as the single constraint that may single-handedly prevent a bubble); returns concentrating at the frontier; the Pareto frontier as the key lab metric; the shift to usage-based pricing; continual learning and the bitter lesson as the biggest risks; new chip companies needing to be "different AND hard"; and prefill/decode disaggregation extending GPU useful lives (rescuing private credit).

## Key Claims

- **Anthropic's exponential is unprecedented.** Added ~$11B ARR; combined Palantir/Snowflake/Databricks businesses "in one month"; Krishna Rao cited NDR ~500%. Anthropic burned ~80% less than OpenAI for similar revenue → far better structural ROIC. If unconstrained by compute, Anthropic might be at $100-200B ARR; buying it at ~5x "unconstrained run-rate revenue."
- **Don't push valuation (the Elon method).** Systematically underpricing rounds (SpaceX ~low-30%/yr for a decade) preserves the superpower of raising capital anytime. Wise for Anthropic/OpenAI even though they could raise at 100%+ premiums.
- **Watts solved by capitalism; zoning/approval now the gating factor** (per big-PE data-center investors). Turbine capacity ramping; watts shortage eases ~2027-28.
- **Orbital compute reframed as "racks in space."** Not pentagon-sized buildings — a Blackwell-rack-sized satellite (~100kW) with ~500ft solar wings in sun-synchronous orbit, radiator behind, linked by lasers through vacuum (already on every Starlink). SpaceX already operates the largest satellite fleet AND the largest terrestrial data center; solves watts if regulation constrains Earth. Inference in orbit; training stays on Earth "for a long time."
- **Wafers are the real constraint — TSMC may prevent the bubble.** If TSMC did what Jensen wanted, Nvidia could sell $2-3T of GPUs in '26-'27 → overbuild. Watch TSMC capacity decisions as the #1 bubble indicator; "Goldilocks zone" keeps Intel/Samsung from >30% share while constraining wafers. Jensen has no contract with TSMC — handshake deals. **Terafab** (SpaceX/Tesla JV + Intel partnership) will be the world's largest US fab; Elon will recruit the A-teams and build Taiwan/Japan/Korea towns to poach the best engineers.
- **A bubble is historically expected** (railroads, canals, dot-com). Mitigants now: buildout funded from operating cash flow (not debt), GPUs at ~100% utilization (vs 99% dark fiber in 2000). Carlota Perez / Mauboussin "breakdown in diversity"; Baker is "a little worried" about a diversity breakdown.
- **Returns concentrate at the frontier.** Overwhelming economic value at the model layer accrues to frontier tokens (surprising). Pareto frontier (intelligence vs cost) is the key lab metric: Google dominated it ~9 months ago (all others inside); now Anthropic + OpenAI dominate, Grok 4.3 on it, Gemini 3.1 "hanging on." Google lost per-token cost leadership via conservative TPU v8 choices.
- **Usage-based pricing shift is hugely bullish** (like cellular/long-distance before all-you-can-eat). $250/mo plans are now rate-limited/"lobotomized"; frontier needs enterprise/usage plans. Claude produces ~70% fewer tokens than before → deprecated intelligence; "token quantity = quality."
- **Biggest risks:** (1) A bitter-lesson violation — most likely via ASI making itself more efficient (bitter lesson "includes humans"); people closest to models are most skeptical it holds for 300-600 IQ. (2) Whether frontier tokens keep their premium. (3) When continual learning arrives (dynamic weight updates; would enable fast takeoff; "just around the corner").
- **New chip companies: "different AND hard."** ~1% share ≈ $100B outcome. Don't build a better GPU (you'll lose). Trainium doing best (Trainium 3 has a switched scale-up network). Prefill (memory-capacity bound) vs decode (memory-bandwidth bound) disaggregation opens a richer design canvas — but trade-offs must be *hard* or Nvidia fast-follows. Cerebras did something hard (wafer-scale) after 3 chip generations. Jensen sees every TSMC process before any 200-person startup.
- **Disaggregation extends GPU life to 10-15 years** (Hopper/Ampere for prefill in front of newer decode chips / Groq LPUs) → GPUs financeable at ~5-6% not low-7s → helps private credit and the whole buildout. "Sellers of shortage" and owners of large installed bases (CPUs at hyperscalers) win.
- **Open-source game theory / new prisoner's dilemma:** frontier labs choosing whether to release via API; if all withhold, Chinese open source (distilled, "stolen American tokens," anti-distillation being built) stays behind; one defector pulls ahead. Jensen can likely reach near-frontier with his own model (Nemotron) as the "commoditize your complement" counter-move.
- **Cross-sectional valuations "cannot all be true"**: semicap at ~40x fwd vs DRAM at mid-single-digits; lowest-quality commodity players moon during shortages (retail/X-driven), high-quality expressions underperform. Baker's defensive advice: a family/company "safe word" against deepfake social-engineering; "master the machine gun" (Last Samurai analogy).

## Notable Quotes

> "What was happening in AI was the most extraordinary moment in the history of capitalism... Anthropic added [Palantir + Snowflake + Databricks'] combined businesses in one month." — Gavin Baker

> "If we don't get a bubble, we need to throw a party for [TSMC], because they will have single-handedly prevented one." — Gavin Baker

> "Don't go try to make a better GPU. So you can do something different... but you also have to do something hard." — Gavin Baker

## Connections

- Sequel to [[wiki/sources/gavin-baker-gpu-economics]] (same speaker; TPU cost leadership, reasoning scaling laws, bear case)
- New-chip-company thesis directly frames [[wiki/sources/harvard-dropouts-nvidia-challenger]] (Etched) and [[wiki/concepts/asic-vs-gpu]]
- Corroborates [[wiki/sources/reiner-pope-training-serving]] on the memory wall and scale-up domains; prefill/decode disaggregation matches Etched + Reiner
- Extends [[wiki/concepts/scaling-laws]] (bitter lesson, continual learning) and [[wiki/concepts/inference-economics]] (usage-based pricing, GPU useful life, Pareto frontier)
- Related to [[wiki/entities/gavin-baker]], [[wiki/entities/nvidia]], [[wiki/entities/anthropic]], [[wiki/entities/openai]], [[wiki/entities/google]] (TPU), [[wiki/entities/elon-musk]] (Terafab, orbital compute)

## Questions Raised

- Does the bitter lesson survive ASI-driven efficiency gains, or is there a "temporary violation"?
- When does continual learning arrive, and does it trigger fast takeoff?
- Can TSMC hold the Goldilocks capacity line, or will Intel/Samsung break discipline and force an overbuild?
