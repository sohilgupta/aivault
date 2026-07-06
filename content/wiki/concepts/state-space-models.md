---
type: concept
title: "State Space Models (SSMs)"
tags: [state-space-models, ssm, mamba, architectures, transformers, compression, recurrence, multimodal]
---

# State Space Models (SSMs)

## Definition

A class of sequence-model architectures that process tokens as a **stream**, updating a fixed-size internal recurrent state ("compressed / zipped" memory) and discarding each token after it's absorbed — giving **linear** scaling in context length, low memory usage, and low-power on-device operation. Contrast with Transformers, which attend to *every* past token (quadratic scaling) and keep all context around. Lineage: early Stanford work (Chris Ré's lab, Karan Goel et al.) → Mamba and modern variants.

## How It Appears in This Wiki

SSMs are the **architecture-side** lever on the same problem the hardware pages attack from below (batching, low precision, KV-cache, inference ASICs): serving long-context and multimodal inference cheaply and fast.

Key points assembled from sources:

- **Retrieval vs. compression.** Transformers are retrieval systems (keep all tokens, reason over them); SSMs are compression systems (fold the stream into a fixed state, discard tokens). Goel frames compression — not retrieval — as fundamental to intelligence. ([[wiki/sources/karan-goel-state-space-models]])
- **Linear vs. quadratic scaling.** Quadratic attention is tolerable for text (short, pre-compressed) but fatal for multimodal (audio/video/sensor streams are huge and mostly redundant). At 100–100,000× more inference, same-scaling models become prohibitively expensive.
- **Compression aids long-context quality.** Trade-off exists, but compressing on the fly (e.g. 24h of camera footage) answers questions better than re-scanning everything; less advantage on short context.
- **Recurrence** is core — leverages the same principle humans use; enables long-lived memory (recall "30 years ago" without RAG) and low-power on-device inference.
- **Batch vs. streaming regimes.** Batch intelligence (slow cloud reasoning) dominated 2020–24; streaming/real-time intelligence (voice, world-gen, robotics) is the next frontier and is SSM-favorable.

## Relationship to the Hardware Thread

SSMs eliminate the **KV-cache-linear-in-context** cost and the quadratic-attention compute that the hardware pages take as a given constraint (see [[wiki/concepts/inference-economics]], [[wiki/sources/reiner-pope-training-serving]]). Where [[wiki/entities/groq]] / [[wiki/entities/etched]] / MatX attack inference cost by building better chips for the Transformer workload, Cartesia attacks it by changing the workload. Complementary, not competing, levers.

## Key Sources

- [[wiki/sources/karan-goel-state-space-models]] — canonical: SSMs, compression-vs-retrieval, batch-vs-streaming, real-time multimodal

## Related Concepts

- [[wiki/concepts/inference-economics]] — the cost/latency problem SSMs address from the model side
- [[wiki/concepts/asic-vs-gpu]] — hardware-side attacks on the same problem
- [[wiki/concepts/scaling-laws]] — SSMs question the "throw compute at quadratic attention" recipe
- [[wiki/concepts/personal-agents]] — on-device real-time assistants

## Open Questions

- Do SSMs match Transformer quality on *short*-context reasoning, where compression helps least?
- Is the future hybrid (attention + SSM layers) rather than pure SSM?
- How much of the 2024 "next 3–5 years" adoption thesis has materialized by 2026? (Data gap — no later SSM source in the wiki.)
