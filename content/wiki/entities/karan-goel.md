---
type: entity
title: "Karan Goel"
entity_type: person
tags: [cartesia, state-space-models, ssm, mamba, multimodal, researcher, founders]
---

# Karan Goel

**Type:** Person
**Also known as:** Founder/CEO of Cartesia; SSM researcher

## Overview

Karan Goel is the founder/CEO of [[wiki/entities/cartesia]] and a co-developer of the earliest **state space models (SSMs)** during his Stanford PhD under Chris Ré — the precursor line that led to Mamba. He graduated from IIT Delhi and CMU, is a Siebel Scholar, and works on ML, data systems, robust ML, and developer tools. His mission: put real-time multimodal intelligence on every device via compression-based architectures.

## Key Facts

| Attribute | Value |
|-----------|-------|
| Role | Founder/CEO, Cartesia |
| Education | IIT Delhi → CMU → Stanford PhD (advisor: Chris Ré) |
| Research | Early SSMs (pre-Mamba), data systems, robust ML |
| Awards | Siebel Scholar |

## Intellectual Contributions (from sources)

- **Batch vs. streaming intelligence** — the field over-optimized batch (slow, cloud, hard-reasoning); the frontier is real-time streaming (voice, video, sensors, robotics).
- **Retrieval vs. compression** — Transformers retrieve (attend to all past tokens, quadratic); SSMs compress the stream into a fixed recurrent state and discard tokens (linear). Compression is fundamental to intelligence.
- **Quadratic attention is fatal for multimodal** — text is short/pre-compressed; multimodal context is huge, making the Transformer recipe prohibitively expensive at scale.
- **Human benchmark** — humans compress ~1B text / ~10B audio / ~1T video tokens per year on a brain-sized low-power machine, recalling decades later without RAG.

## Appearances in Sources

- [[wiki/sources/karan-goel-state-space-models]] — primary; AI Engineer World's Fair 2024 talk

## Connections

- Founder/CEO of [[wiki/entities/cartesia]]
- Central to [[wiki/concepts/state-space-models]]
- Architecture-side counterpart to hardware thinkers [[wiki/entities/reiner-pope]], [[wiki/entities/jonathan-ross]] on the inference-efficiency problem
