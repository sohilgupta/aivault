---
type: entity
title: "Jane Street"
entity_type: organisation
tags: [trading, hft, gpu, fpga, compute]
---

# Jane Street

**Type:** Organisation (quantitative trading firm)

## Overview

Jane Street is a quantitative proprietary trading firm known for its OCaml codebase, puzzle culture, and (increasingly) large-scale ML infrastructure. It applies models across many time horizons, from sub-100ns FPGA packet turnaround to hour/day-scale decisions, and has become a serious compute buyer.

## Key Facts

| Attribute | Value |
|-----------|-------|
| Compute deal | $6B with CoreWeave |
| GPU fleet | Tens of thousands → heading to hundreds of thousands |
| Hardware | FPGAs (ultra-low latency), CPUs, GPUs; building custom ASICs |
| Data character | Noisier, less informative bit-for-bit than web text → smaller models, more data |
| Core prediction target | Fair value of instruments |
| Culture | Puzzles; human-oriented tooling; "team sport" hiring |

## Appearances in Sources

- [[wiki/sources/jane-street-gpus-trading]] — primary; Ron Minsky & Dan Pontecorvo on GPUs, trading horizons, data-center engineering, hiring, "AGI-complete" trading
- [[wiki/sources/reiner-pope-chip-design]] & [[wiki/sources/reiner-pope-training-serving]] — Jane Street FPGA/HFT engineers (Clark, Axel) as sponsors and case studies for deterministic-latency hardware
- [[wiki/sources/eric-jang-alphago-selfplay]] — KataGo author David Wu is from Jane Street

## Connections

- FPGA-for-determinism rationale is a case study in [[wiki/concepts/asic-vs-gpu]]
- Demand-side data point for [[wiki/concepts/inference-economics]] (latency-critical, low-batch, high sequential data rate)
- Buys from [[wiki/entities/nvidia]] (now must support ARM); related to compute analysis by [[wiki/entities/dylan-patel]]
