---
type: concept
title: "Inference Economics"
tags: [inference, batch-size, kv-cache, roofline, moe, cost]
---

# Inference Economics

## Definition

The set of first-principles relationships that determine the cost, latency, and throughput of serving LLM inference on GPU/TPU clusters — chiefly the interplay of batch size, weight fetches, KV-cache fetches, memory bandwidth, and compute (FLOPs), analyzed via roofline models.

## How It Appears in This Wiki

This concept ties together the hardware and economics threads. It explains why API prices and "fast/slow modes" are what they are, why models are architected as they are (MoE, sparsity, context limits), and why new inference chips (Etched) exist.

Key results assembled from sources:

- **Batch size dominates.** Not batching users costs up to ~1000x more per token. There is a latency floor (read all weights from HBM once, ~15-20ms/pass) and a cost floor (compute time once weight fetches amortize). "Slow mode" can't beat the compute-bound line. ([[wiki/sources/reiner-pope-training-serving]])
- **Optimal decode batch ≈ 300 × sparsity** (FLOP/bandwidth ≈ 300, stable across GPU generations). ~2000 sequences for DeepSeek-like sparsity; tokens/sec ≈ batch × 64.
- **KV-cache fetch is linear in context** (dense attention); sparse attention adds a √, scaling far better. Prefill = memory-capacity bound; decode = memory-bandwidth bound (PD disaggregation).
- **MFU reality:** GPUs get ~20-50% of peak FLOPs; can't hit 100% due to thermal throttling. ([[wiki/sources/harvard-dropouts-nvidia-challenger]])
- **Scale-up domain caps total parameters; compute cost caps active parameters.** MoE expert parallelism creates an all-to-all pattern that fits exactly in one rack; crossing racks hits the ~8x-slower scale-out network. ([[wiki/sources/reiner-pope-training-serving]])
- **Usage-based pricing** is replacing all-you-can-eat; token quantity ≈ answer quality; frontier is gated behind enterprise/usage plans. ([[wiki/sources/gavin-baker-watts-wafers]])
- **Disaggregation extends GPU useful life to 10-15 years** (old GPUs for prefill), improving financing. ([[wiki/sources/gavin-baker-watts-wafers]])

## Key Sources

- [[wiki/sources/reiner-pope-training-serving]] — the canonical derivation (roofline, batch, KV cache, MoE-on-rack)
- [[wiki/sources/harvard-dropouts-nvidia-challenger]] — MFU, thermal wall, cluster-scale memory, PD disaggregation
- [[wiki/sources/gavin-baker-watts-wafers]] — Pareto frontier, usage-based pricing, GPU life, prefill/decode canvas
- [[wiki/sources/jane-street-gpus-trading]] — atypical demand profile (latency-critical, low-batch)
- [[wiki/sources/dylan-patel-token-supply-demand]] — token supply/demand, memory wall

## Related Concepts

- [[wiki/concepts/asic-vs-gpu]] — hardware substrate for these economics
- [[wiki/concepts/scaling-laws]] — training/inference compute balance drives over-training
- [[wiki/concepts/tokenomics]] — token cost/pricing dynamics

## Open Questions

- How far can sparsity go before quality degrades faster than compute is saved?
- Is current hardware over-provisioned on HBM given the memory surplus for pipelining?
