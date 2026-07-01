---
type: source
title: "Chip design from the bottom up – Reiner Pope"
source_type: transcript
date_ingested: 2026-05-23
original_file: raw/podcasts/Chip design from the bottom up – Reiner Pope.md
tags: [chip-design, systolic-arrays, gpu, tpu, fpga, asic, hardware, dwarkesh]
---

# Chip design from the bottom up – Reiner Pope

**Source type:** Transcript (Dwarkesh Patel blackboard lecture)
**Original:** [[raw/podcasts/Chip design from the bottom up – Reiner Pope]]
**Ingested:** 2026-05-23

## Summary

Second Reiner Pope (MatX CEO) blackboard lecture, building an AI chip from logic gates up: AND gates and full adders → multiply-accumulate → Dadda multiplier → muxes and register files → systolic arrays (Tensor Cores) → clock cycles and pipeline registers → FPGAs vs ASICs → cache vs scratchpad → GPU vs TPU structure. The recurring theme is that most chip area is spent on data movement (communication), not on the arithmetic we care about (compute) — the same compute-vs-communication tension that governs cluster-level inference.

Key mechanisms: multiply area scales quadratically with bit width (why low precision — FP4/FP8 — is so favorable; Nvidia B300 made FP4 3x FP8, "should be 4x"). CUDA cores spend ~7/8 of area on register-file muxing; systolic arrays fix this by baking two loop levels into fixed-function hardware and keeping the weight matrix stationary, amortizing register-file cost. Clock speed is set by the longest logic path with a feedback loop; pipeline registers trade area for clock speed. FPGAs emulate ASICs via LUTs + muxes and cost ~10x more (a 4-input LUT ≈ 32 gates for what an ASIC does in 3). A GPU is high-level "a bunch of tiny TPUs" (SM ≈ small MXU+vector unit); TPUs use big systolic arrays + scratchpad (deterministic latency), GPUs use many small units with caches (non-deterministic).

## Key Claims

- **Data movement dominates area.** In a pre-Tensor-Core CUDA/CPU core, ~7/8 of circuit area is register-file muxing (3 × n × p AND gates for muxes vs p × q for the multiply-adder). Hidden to software ("select register 3" is a whole mux).
- **Multiply area is quadratic in bit width** (p×q ANDs + p×q full adders). Halving precision more than doubles FLOPs — Nvidia acknowledged this from B300 (FP4 = 3x FP8, though quadratic says 4x).
- **Systolic array (Tensor Core)** goes two loop levels up, stores the weight matrix locally/stationary, trickle-feeds weights in slowly to bound wiring to O(x) not O(xy). Larger arrays amortize register-file cost better; TPUs used 128×128. Most efficient known matmul circuit.
- **Clock cycle** = global lockstep sync via registers; set by the longest logic path, hardest case being a feedback loop (can't just insert a pipeline register). Pipeline-register insertion trades area for clock speed; margined many σ so it "always" meets timing.
- **FPGA vs ASIC**: same conceptual model; ASIC ~10x cheaper/more efficient but first ASIC ≈ $30M tape-out vs first FPGA ≈ $10k. FPGA use case = deterministic low latency + frequently changing workload (e.g. HFT). LUT = programmable gate via truth table; ~10x overhead because listing a truth table is less concise than placing gates.
- **Cache vs scratchpad**: cache (CPU/DDR) is the main source of non-deterministic latency; scratchpad (TPU/HBM) makes memory placement explicit in software → deterministic. Deterministic-latency CPUs are possible but unpopular.
- **CPU vs GPU**: CPU core is ~1/100 of die; big area goes to cache and the branch predictor (predicts branches ~5 cycles early to keep clock high). GPUs strip the branch predictor and tighten register files.
- **GPU ≈ many tiny TPUs.** GPU = regular grid of SMs (small MXU+vector) with L2; TPU = few big matrix units + vector unit. GPU moves more data vector↔matrix (16 lines vs 2) but pays cross-SM cost; MatX teases a "splittable systolic array."
- **Brain vs chip**: co-located memory/compute is similar; brain's slower clock saves energy (dynamic/switching power dominates; running 1000x slower ≈ 1000x less energy but not a silicon efficiency win). Brain is batch-1; chips run batch-1000, favoring high clocks/throughput.

## Notable Quotes

> "In both cases, you're trying to maximize compute relative to communication. This shows up all the way up and down the stack." — Reiner Pope

> "From a very high-level point of view, the GPU has a lot of tiny TPUs tiled across the whole chip."

## Connections

- Companion to [[wiki/sources/reiner-pope-training-serving]] — same compute-vs-communication theme, one level lower
- Grounds [[wiki/concepts/asic-vs-gpu]] (FPGA/ASIC/TPU/GPU trade-offs, systolic arrays, determinism)
- Explains hardware basis for [[wiki/concepts/inference-economics]] (low precision, data-movement cost)
- FPGA/deterministic-latency material overlaps [[wiki/sources/jane-street-gpus-trading]] (HFT uses FPGAs)
- Related to [[wiki/entities/reiner-pope]], [[wiki/entities/nvidia]] (Tensor Cores, FP4 specs), [[wiki/entities/google]] (TPU/MXU)

## Questions Raised

- Can FP4 and FP8 multiply-accumulate circuits be made fungible, or must die area be split at design time? (Reiner: not fungible as drawn; a design-time sizing choice.)
- What does MatX's "splittable systolic array" actually buy vs Nvidia's small-SM structure?
