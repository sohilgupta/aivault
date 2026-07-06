---
type: source
title: "State Space Models for Realtime Multimodal Intelligence: Karan Goel"
source_type: transcript
date_ingested: 2026-05-23
original_file: raw/podcasts/State Space Models for Realtime Multimodal Intelligence Karan Goel.md
tags: [state-space-models, ssm, mamba, cartesia, multimodal, realtime, architectures, transformers]
---

# State Space Models for Realtime Multimodal Intelligence: Karan Goel

**Source type:** Transcript (AI Engineer World's Fair 2024 talk)
**Original:** [[raw/podcasts/State Space Models for Realtime Multimodal Intelligence Karan Goel]]
**Ingested:** 2026-05-23

## Summary

Karan Goel — Cartesia CEO, Stanford PhD under Chris Ré, and a co-developer of the earliest **state space models (SSMs)** that led to Mamba — argues the last few years of AI optimized for *batch intelligence* (call a cloud model, wait seconds, get a good answer) but the next frontier is *streaming / real-time intelligence*: conversational voice, world/game generation, on-device assistants, and robotics that ingest continuous audio/video/sensor streams and respond instantly at low power.

His core technical thesis: **Transformers are built on retrieval, but intelligence is built on compression.** A Transformer attends to every past token (quadratic scaling in context length), keeping all context around. This is fine for text (already information-dense — a lot is packed into two sentences) but breaks down for multimodal data, which is enormous and mostly redundant (a day of security-camera footage is almost all uninteresting). Humans process ~1B text tokens, ~10B audio tokens, and ~1T video tokens per year, simultaneously, on a brain-sized low-power computer, remembering things from 30 years ago with no "RAG" — because we compress.

SSMs implement this: tokens stream in, update a fixed internal memory (a "zipped-file" state), then are **thrown away**. This gives linear scaling in context, low memory usage, low-power/on-device implementations, and much longer effective context — by taking advantage of recurrence, which Goel frames as core to human reasoning. The trade-off is compression vs. keeping-everything-around, but he argues compression actually *helps* quality on long-context and multimodal problems (compressing 24h of footage beats re-scanning it every query); it's less helpful for short context. Cartesia is building real-time foundation models on this stack, and had recently shipped a low-latency text-to-speech voice model (playground at play.ai / play.cartesia) that runs in the data center with work underway to run the same experience on Mac and other devices at low power.

## Key Claims

- **Two regimes of AI: batch vs. streaming.** Batch = long reasoning on hard problems (math, physics). Streaming = instant, continuous, low-latency generation/understanding (voice, video, sensors, robotics). The field over-focused on batch.
- **Transformers = retrieval; SSMs = compression.** Attention keeps all past tokens and reasons over them (quadratic); SSMs compress the stream into a fixed recurrent state and discard tokens (linear).
- **Quadratic scaling is fatal for multimodal.** Text context is short and pre-compressed; multimodal context is huge. At 100–100,000× more inference, same-scaling models make it prohibitively expensive to "permeate all these applications."
- **Compression is fundamental to intelligence.** Humans compress lifetimes of multimodal input into a brain-sized, variable-power machine and recall decades later without retrieval. Current AI (retrieval-based) doesn't exhibit this.
- **Compression helps quality on long context.** Trade-off exists, but for long/multimodal problems compressing on the fly answers questions *better* than re-reading everything; less advantage on short context.
- **New architectures are needed** — "we should not settle for one way of doing things." SSMs (Mamba lineage) are being adopted; expect a larger role over the next 3–5 years as multimodal data grows.
- **Real-time on-device is the goal** — the same data-center quality/latency, but on phone/laptop at low power (Cartesia's TTS + on-device work).

## Notable Quotes

> "Transformers are... generating quadratically by attending to every past token... with SSMs you just have a streaming system... the token gets thrown away." — the retrieval-vs-compression core

> "Compression is kind of really fundamental to intelligence." — why SSMs, not just efficiency

> "You're... doing it on a computer that fits in your brain... and you're still functioning fine." — the human-efficiency benchmark

## Connections

- **Genuinely new architectural axis vs. [[wiki/concepts/asic-vs-gpu]] and [[wiki/concepts/inference-economics]]** — those pages attack inference cost from *hardware* (systolic arrays, low precision, batching, KV-cache); SSMs attack it from *model architecture* (kill the quadratic attention / KV-cache entirely). Complementary levers on the same problem: serving multimodal cheaply.
- The quadratic-context / KV-cache-linear-in-context problem is documented from the hardware side in [[wiki/sources/reiner-pope-training-serving]] — SSMs are the algorithmic answer to that memory-bandwidth wall.
- Real-time / low-latency framing overlaps [[wiki/sources/jonathan-ross-groq]] (fast inference, agent-to-agent speed) but from the model rather than chip side.
- Contrasts with the Transformer-centric [[wiki/concepts/scaling-laws]] thread — SSMs question whether "throw compute at quadratic attention" is the right long-run recipe.
- On-device/personal real-time assistants connect to [[wiki/concepts/personal-agents]].
- New entities: [[wiki/entities/cartesia]], [[wiki/entities/karan-goel]]. New concept: [[wiki/concepts/state-space-models]].

## Questions Raised

- How far does SSM quality actually close on Transformers for *short*-context reasoning, where Goel concedes compression helps less?
- Is the future hybrid (attention + SSM layers) rather than pure-SSM? The talk implies SSMs "have more of a role," not full replacement.
- Talk is from Oct 2024 — how much of the "next 3–5 years" adoption thesis has held by 2026? (Data gap: no later Cartesia/SSM source in the wiki yet.)
