---
type: entity
title: "Cartesia"
entity_type: organisation
tags: [cartesia, state-space-models, ssm, multimodal, voice, tts, realtime, on-device]
---

# Cartesia

**Type:** Organisation
**Also known as:** cartesia.ai (playground: play.cartesia / play.ai)

## Overview

Cartesia is a real-time foundation-model company founded by [[wiki/entities/karan-goel]] and colleagues out of the Stanford lab of Chris Ré. It builds multimodal models on a **state space model (SSM)** stack rather than Transformers, targeting streaming/real-time intelligence — conversational voice, world generation, on-device assistants, robotics — that runs fast and at low power on any device.

## Key Facts

| Attribute | Value |
|-----------|-------|
| Founder / CEO | Karan Goel (Stanford PhD, ex-IIT Delhi, CMU) |
| Lineage | Chris Ré's Stanford lab; early SSM work → Mamba |
| Core tech | State space models (linear-scaling, compression-based) |
| First product | Low-latency text-to-speech voice model (data-center + on-device roadmap) |
| Thesis | Real-time multimodal intelligence needs new (non-Transformer) architectures |

## Why It Matters in This Wiki

Cartesia represents the **architecture-side** attack on inference cost — replacing quadratic attention with linear-scaling recurrent compression — complementing the hardware-side attacks documented elsewhere (batching, low precision, inference ASICs). It is the wiki's main entry point for SSMs and real-time/on-device multimodal AI.

## Appearances in Sources

- [[wiki/sources/karan-goel-state-space-models]] — primary; SSM thesis, batch-vs-streaming, compression-vs-retrieval, TTS release

## Connections

- Founded/led by [[wiki/entities/karan-goel]]
- Central to [[wiki/concepts/state-space-models]]
- Complements [[wiki/concepts/inference-economics]], [[wiki/concepts/asic-vs-gpu]] (architecture vs hardware levers)
- Real-time/on-device assistants connect to [[wiki/concepts/personal-agents]]
