---
type: source
title: "Jane Street on GPUs, Trading, and Hiring: A Conversation with Dwarkesh"
source_type: transcript
date_ingested: 2026-05-23
original_file: raw/podcasts/Jane Street on GPUs, Trading, and Hiring A Conversation with Dwarkesh.md
tags: [trading, gpu, fpga, inference, hiring, data-centers, agi, dwarkesh]
---

# Jane Street on GPUs, Trading, and Hiring: A Conversation with Dwarkesh

**Source type:** Transcript (Dwarkesh Patel at a Jane Street Texas data center; Ron Minsky, Dan Pontecorvo)
**Ingested:** 2026-05-23
**Original:** [[raw/podcasts/Jane Street on GPUs, Trading, and Hiring A Conversation with Dwarkesh]]

## Summary

Dwarkesh tours a Jane Street training data center with Ron Minsky (co-head of technology) and Dan Pontecorvo (physical engineering). Covers how a quant trading firm applies GPUs/ML across many time horizons (from <100ns FPGA packet turnaround to hour/day-scale model decisions), why they signed a $6B CoreWeave compute deal, how their inference workload differs from a chatbot lab, why Jane Street is not "AGI-complete-solvable" any time soon, and what data-center and ML/formal-methods roles they're hiring for.

Distinctive substance: Jane Street has its own scaling laws but far more architectural diversity than a foundation lab; financial data is noisier and less informative bit-for-bit, so models are smaller, data noisier and more plentiful, with high sequential data rates from feeds like NASDAQ. They're moving from x86-only/single-data-center simplicity to a disaggregated, ARM-supporting, multi-data-center world with intertwined compute+storage scheduling. Ron argues trading is "AGI-complete" and human cognition is more valuable than ever ("never been more desperate to hire").

## Key Claims

- **Many time horizons, not one.** Some trades need <100ns packet turnaround (FPGA wire-attached; "packet starts to leave before it's done being consumed"); others tolerate microseconds, milliseconds, or hours. Inference runs on CPU/FPGA/GPU depending on latency and model size.
- **A core prediction target is fair value** — what a thing is worth — composable into many trading processes; used since linear-regression days 25 years ago.
- **$6B CoreWeave deal** to train many diverse models. Value comes from architectural experimentation and faster researcher iteration, not one general model.
- **Why specialize (vs one general model):** adapted to different noisy data sources, different data rates, different bytes-to-FLOP ratios. High aggregate but low per-user sequential data in LLM labs; the opposite for a NASDAQ feed (very high sequential data rate in one causal domain).
- **Disaggregation forced two long-held shortcuts to unwind**: (1) x86-only (now must support ARM for Nvidia products), (2) single research data center + single storage cluster — you can't wire enough power into one site, so compute+storage scheduling are now intertwined.
- **Trading is "AGI-complete."** Predicting value = predicting the future; all world problems flow in. As pieces get automated, the un-automated hard parts become the edge. Humans work better through phase transitions; a human is always watching even for automated systems.
- **Non-electronic trading still real** — chat-based trading, adverse-selection judgment, bonds far less automated than equities even after 25-30 years.
- **Compute is a constraint, not a surplus.** Unlike Meta's Instagram-ad reserve use, Jane Street has "dark space" of valuable experiments it turns away; low-hanging fruit includes retraining models more often (quality decays). Growing from tens of thousands → hundreds of thousands of GPUs.
- **Hiring bottleneck is people/mentorship, not hardware.** More researchers → buy more compute (clearly good ROI). Roles: physical/mechanical/electrical engineers, ML architects, LLM lifecycle, traders, generalist SWE, fleetwide performance optimization (new, hyperscaler-style), custom ASIC work, front-end, and a speculative **formal-methods team** (AI makes formal methods newly interesting).
- **Data-center engineering shifts**: dropping generators (longest-lead item) except for a resilient core to get GPUs online ~6 months faster ("best business decision, maybe not best engineering decision"); modular/pre-built infra; bottlenecks rotate (generators, transformers, liquid-cooling gear); can bifurcate power/data-center commitment from the expensive chip decision.

## Notable Quotes

> "I have never been more desperate to hire more engineers and more traders than I am today, because everything people are doing is more valuable than it was." — Ron Minsky

> "Trading in particular feels to me as kind of AGI-complete, sort of like NP-complete." — Ron Minsky

> "You can build these giant grids of compute very easily that touch a hundred megabytes of SRAM and get your response back in tens of nanoseconds. That's basically impossible on a CPU." — Clark (Jane Street, quoted in Reiner Pope episode)

## Connections

- Cross-referenced heavily by [[wiki/sources/reiner-pope-training-serving]] and [[wiki/sources/reiner-pope-chip-design]] — Jane Street FPGA/HFT determinism is Reiner's ASIC-vs-FPGA case study
- Grounds [[wiki/concepts/asic-vs-gpu]] — real-world FPGA-for-determinism rationale
- Adds a demand-side data point to [[wiki/concepts/inference-economics]] (latency-critical, low-batch, high sequential data rate)
- Related to [[wiki/entities/jane-street]] (new), [[wiki/entities/nvidia]] (ARM requirement), [[wiki/sources/gavin-baker-watts-wafers]] (data-center power/cooling bottlenecks)

## Questions Raised

- How close is "AGI-complete" trading to being automated? Ron is skeptical it's near; edge keeps moving to un-automated parts.
- Does a formal-methods + LLM approach actually make software engineering measurably more effective? (Speculative bet.)
