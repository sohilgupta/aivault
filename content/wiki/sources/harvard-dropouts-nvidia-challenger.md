---
type: source
title: "The Two Harvard Dropouts Who raised $800M to take on NVIDIA (Etched)"
source_type: transcript
date_ingested: 2026-05-23
original_file: raw/podcasts/The Two Harvard Dropouts Who raised $800M to take on NVIDIA.md
tags: [etched, asic, inference, chip-design, startups, sohu, low-voltage, cluster-memory]
---

# The Two Harvard Dropouts Who raised $800M to take on NVIDIA (Etched)

**Source type:** Transcript (Invest Like The Best, Patrick O'Shaughnessy; Gavin Uberti & Robert Wachen of Etched)
**Ingested:** 2026-05-23
**Original:** [[raw/podcasts/The Two Harvard Dropouts Who raised $800M to take on NVIDIA]]

## Summary

Gavin Uberti and Robert Wachen, Etched co-founders, tell the story of building an inference-only AI chip company. Three years after being two ~21-year-old Harvard dropouts nobody believed, Etched has raised ~$800M, signed >$1B in customer contracts, and taped out a working chip (Sohu) plus a full rack. The thesis: inference will be the biggest market in the world; whoever produces the most tokens is the most valuable company; all AI hardware was designed before ChatGPT and must be rebuilt for modern MoE inference.

Two core technical bets: (1) **low-voltage inference** — running at under half the voltage of any other AI chip to beat the thermal wall (Dennard scaling: voltage is quadratic in power; GPUs thermal-throttle so adding FLOPs doesn't help). (2) **cluster-scale memory** — a fully custom interconnect (rebuilt above L2 Ethernet) cutting chip-to-chip latency >5x (vs ~4000ns point-to-point on Blackwell → ~2-3ns is the speed-of-light limit), letting the whole scale-up cluster's SRAM+HBM act as one pool. They vertically integrate everything (chip, board, cold plates, interconnect, rack, production) — "production is the product." Recruiting philosophy: "legends" (e.g. Brian, who built Nvidia's HGX/DGX) paired with naive first-principles talent ("chips on shoulders"). Near-death: needed $100M for a Series A when the semi record was ~$40-50M; almost failed, snowballed soft commits to $103M.

## Key Claims

- **Inference is the coming largest market.** Today only a few million paid AI users (~1/1000th of humanity); serving billions concurrently requires multiple orders of magnitude more infra "from the wafer to the watt." Tokens today are hand-crafted (Renaissance screws); Etched wants iPhone-like economies of scale for token production.
- **All AI chips predate ChatGPT.** GPUs/TPUs are retrofit for MoE inference; a purpose-built inference chip looks very different (FLOP organization, voltage domains, power planes, packaging, board, interconnect).
- **Constraints are siloed and outdated.** Example: EDA tools default to freezing-temp corners, but AI data centers never run below ~80°C — relaxing false constraints yields 20%/50%/2x gains that compound.
- **Prefill vs decode disaggregation ("PD disaggregation").** Prefill = flops/flop-density bound (load the KV cache); decode = memory-bandwidth bound. Transfer KV caches from prefill to decode clusters. "Loading the gun, then firing it."
- **MFU reality:** GPUs get ~20-50% of advertised peak FLOPs on real workloads and provably can't hit 100% due to thermal throttling → must solve thermal (low voltage) before adding FLOPs.
- **Cluster-scale memory > per-chip bandwidth.** Ask how much bandwidth the whole scale-up cluster has, not one chip. Bad chip-to-chip latency (Blackwell ~4000ns) means 8x TP gives far less than 8x tokens/sec/user. Etched's custom stack cuts this >5x.
- **Vertical integration + parallelization + velocity.** Only startup building its own rack and chips; shipped rackless racks to customers, ran full inference stack on 700+ FPGAs, built thermal-mock chips and cold plates — all before silicon. Went silicon→inference-in-rack in **40 days** (a famous competitor took 10 months).
- **Existential focus wins.** "Google won't fail if TPUs fail; Meta won't fail if MTIA fails; OpenAI won't fail if Jalapeño fails. It is completely unsurprising the best chip is built by a company that only builds that chip — Nvidia." Hyperscaler in-house chips have lower FP8×FP8 flop density than B300 because they don't have to take the risk.
- **Supply is positive-sum, not zero-sum for them.** First-gen on 4nm (Rubin on 3nm), different HBM than Rubin → "not GPU-or-us, it's 2 gigawatts." TSMC's service (not just tech) is the real moat.
- **Machines don't think like brains.** For neurons, memory is cheap and math expensive; for chips, the reverse — and math gets cheaper faster than memory (fundamental DRAM limit). Build models that use huge compute (many experts, giant experts across servers, huge context). Future models need hardware for **dynamism** (per-token/per-user control of compute and memory in attention).
- **Futuristic claims:** inference → majority of global GDP; productivity measured as "agents per megawatt/gigawatt"; 2027 the first year more agents do knowledge work than humans; trillion-dollar single data centers inevitable (economies of scale don't stop at $40B fabs).

## Notable Quotes

> "We know inference is going to be the biggest market in the world. Whoever produces the most tokens is going to be the most valuable company in the world." — Gavin Uberti

> "You kind of have to be sick in the head to join our company... a design that they're saying is not going to be 10% better, but 10x better." — Robert Wachen

> "Production is the product." — Etched motto

> "The best part is no part. For us, it's also the best vendor is no vendor."

## Connections

- Direct rival framing to [[wiki/entities/nvidia]] and the [[wiki/sources/jensen-huang-nvidia-moat]] moat thesis
- Central case study for [[wiki/concepts/asic-vs-gpu]] — purpose-built inference ASIC vs general GPU
- Deepens [[wiki/concepts/inference-economics]] — PD disaggregation, MFU, thermal wall, cluster-scale memory, tokens-per-watt
- Echoes [[wiki/sources/reiner-pope-training-serving]] (scale-up domain size, MoE, chip-to-chip latency) and [[wiki/sources/gavin-baker-watts-wafers]] (new chip startups must be "different and hard"; prefill=capacity-bound, decode=bandwidth-bound)
- Related to [[wiki/entities/etched]] (new), [[wiki/entities/jane-street]] (HFT firms invested / joined — they hate compilers too), [[wiki/entities/openai]] (Jalapeño in-house chip)

## Questions Raised

- Does low-voltage inference + cluster-scale memory hold up at gigawatt production scale and real customer workloads?
- Will Nvidia simply fast-follow any "different" trade-off that reaches 1-3% share (Gavin Baker's exact warning)?
- Is the "inference = majority of GDP / 2027 agent-majority" timeline credible, or founder hype?
