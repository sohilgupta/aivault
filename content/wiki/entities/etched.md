---
type: entity
title: "Etched"
entity_type: organisation
tags: [asic, inference, chip-design, startup, sohu]
---

# Etched

**Type:** Organisation (AI inference chip startup)

## Overview

Etched is an inference-only AI chip company founded by two Harvard dropouts, Gavin Uberti and Robert Wachen, ~2022-2023. Its thesis: all existing AI hardware (GPUs/TPUs) was designed before ChatGPT and must be rebuilt for modern MoE inference; whoever produces the most tokens will be the most valuable company in the world. Etched builds a full inference solution — chip (Sohu), rack, board, cold plates, interconnect, and production — vertically integrated. "Production is the product."

## Key Facts

| Attribute | Value |
|-----------|-------|
| Founders | Gavin Uberti, Robert Wachen (Harvard dropouts, ~21 at founding) |
| Raised | ~$800M (Series A survival round was $103M) |
| Contracts | >$1B in customer commitments |
| First product | Sohu chip + full rack; taped out & running |
| Process | 4nm (vs Rubin on 3nm), different HBM than Rubin |
| Key bets | Low-voltage inference (<½ GPU voltage); cluster-scale memory (custom interconnect, >5x lower chip-to-chip latency) |
| Notable hire | Brian (built Nvidia's HGX/DGX systems) — a "legend" |
| Silicon→rack | 40 days (a famous competitor took 10 months) |

## Technical Bets

- **Low-voltage inference** — beats the thermal wall (Dennard scaling: voltage quadratic in power; GPUs thermal-throttle). Claims all future AI chips must be low-voltage.
- **Cluster-scale memory** — custom interconnect (rebuilt above L2 Ethernet) treats the whole scale-up cluster's SRAM+HBM as one pool; targets speed-of-light chip-to-chip latency (~2-3ns vs Blackwell ~4000ns).
- **PD disaggregation** — separate prefill (flop/capacity bound) and decode (bandwidth bound) clusters, transferring KV caches between them.
- **Kernels-first software** (no arbitrary graph compiler) — bet that <100 models matter and coding models will write kernels; HFT firms (who also hate compilers) invested and joined.

## Appearances in Sources

- [[wiki/sources/harvard-dropouts-nvidia-challenger]] — primary; full origin story, technical bets, recruiting, near-death fundraise, futuristic vision

## Connections

- Direct challenger to [[wiki/entities/nvidia]] and the [[wiki/sources/jensen-huang-nvidia-moat]] moat thesis
- Central case study for [[wiki/concepts/asic-vs-gpu]] and [[wiki/concepts/inference-economics]]
- Fits [[wiki/entities/gavin-baker]]'s "different AND hard" new-chip framework ([[wiki/sources/gavin-baker-watts-wafers]]) — and his warning that Nvidia fast-follows anything reaching 1-3% share
- HFT investors/joiners tie to [[wiki/entities/jane-street]]; competes with in-house chips from [[wiki/entities/openai]] (Jalapeño), [[wiki/entities/google]] (TPU)
