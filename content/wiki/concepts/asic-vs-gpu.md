---
type: concept
title: "ASIC vs GPU (AI Chip Architectures)"
tags: [hardware, asic, gpu, tpu, fpga, systolic-arrays, inference]
---

# ASIC vs GPU (AI Chip Architectures)

## Definition

The trade-off space among AI compute substrates — general-purpose GPUs, TPUs and other purpose-built ASICs, and FPGAs — spanning cost, energy efficiency, flexibility, latency determinism, and the specialization that inference-era workloads reward.

## How It Appears in This Wiki

Recurring theme across the hardware sources. The unifying principle (Reiner Pope): at every level of the stack you maximize compute relative to communication (data movement), and specialization lets you break general-purpose "buffer" and change constraints.

Key points assembled from sources:

- **Systolic array (Tensor Core / MXU)** is the most efficient known matmul circuit — bakes loop levels into fixed hardware, keeps weights stationary, amortizes register-file cost. Larger arrays amortize better. ([[wiki/sources/reiner-pope-chip-design]])
- **GPU ≈ many tiny TPUs** — regular grid of small SMs (matmul+vector) vs a TPU's few big matrix units + vector unit. GPUs move more data vector↔matrix but pay cross-SM cost; TPUs use scratchpad (deterministic) vs GPU/CPU caches (non-deterministic).
- **Low precision** — multiply area is quadratic in bit width, so FP4/FP8 are hugely favorable (Nvidia B300: FP4 = 3x FP8).
- **FPGA vs ASIC** — same conceptual model; ASIC ~10x cheaper/more efficient but $30M tape-out vs $10k first FPGA. FPGA use case: deterministic low latency + frequently changing workload (HFT — Jane Street). ([[wiki/sources/jane-street-gpus-trading]])
- **Purpose-built inference ASICs** — Etched argues all chips predate ChatGPT; relaxing false constraints (e.g. freezing-temp EDA corners) + low-voltage inference + cluster-scale memory yields step-change gains. ([[wiki/sources/harvard-dropouts-nvidia-challenger]])
- **"Different AND hard"** — Gavin Baker: don't build a better GPU; make a *hard* different trade-off (prefill capacity-bound vs decode bandwidth-bound) or Nvidia fast-follows anything reaching 1-3% share. Trainium/Cerebras cited; ~1% share ≈ $100B. ([[wiki/sources/gavin-baker-watts-wafers]])
- **Existential focus wins** — the best chip is built by a company that only builds that chip (Nvidia); hyperscaler in-house chips have lower flop density because they don't have to take the risk.
- **LPU (Groq)** — inference ASIC optimized for the memory-throughput-bound weight-application part of the decoder; pairs with GPUs (compute-bound attention) rather than replacing them. Ross (TPU's creator) concedes GPUs now beat TPUs, crediting ecosystem scale. Ended in a ~$20B NVIDIA deal, not head-on competition. ([[wiki/sources/jonathan-ross-groq]])

## Key Sources

- [[wiki/sources/reiner-pope-chip-design]] — gates → systolic arrays → FPGA/ASIC → GPU-vs-TPU, cache vs scratchpad
- [[wiki/sources/harvard-dropouts-nvidia-challenger]] — Etched inference ASIC (low voltage, cluster-scale memory, PD disaggregation)
- [[wiki/sources/gavin-baker-watts-wafers]] — "different AND hard," Trainium/Cerebras, iron-triangle framing
- [[wiki/sources/jane-street-gpus-trading]] — FPGA-for-determinism in HFT
- [[wiki/sources/jensen-huang-nvidia-moat]] — the incumbent's architectural moat
- [[wiki/sources/jonathan-ross-groq]] — Groq LPU inference ASIC; GPU+LPU pairing; TPU-creator concedes GPUs now win

## Related Concepts

- [[wiki/concepts/inference-economics]] — what these chips are optimized to serve
- [[wiki/concepts/scaling-laws]] — hardware roadmap enables model scaling
- [[wiki/concepts/state-space-models]] — architecture-side alternative to hardware specialization for cheap inference

## Open Questions

- Can a purpose-built inference ASIC's advantages survive gigawatt production and Nvidia's fast-follow?
- Are FP4/FP8 units fungible, or a fixed design-time area split? (Reiner: not fungible.)
