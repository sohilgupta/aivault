---
type: entity
title: "Nvidia"
entity_type: organisation
tags: [nvidia, gpu, cuda, ai-infrastructure, semiconductors, inference]
---

# Nvidia

**Type:** Organisation

## Overview

Nvidia is the dominant GPU and AI accelerator company. Founded in 1993 by Jensen Huang et al., it became the foundational infrastructure company of the AI era through its CUDA software ecosystem — making GPUs programmable for general scientific computing long before AI demand emerged. Its H100/H200/Blackwell GPU families are the primary compute substrate for AI training and inference globally.

## Key Facts

| Attribute | Value |
|-----------|-------|
| CEO | Jensen Huang |
| Key product | H100, H200, Blackwell GPUs; CUDA; NVLink interconnects |
| Strategic acquisitions | Mellanox (networking); Groq (inference/latency) |
| Moat | CUDA ecosystem + architectural leadership + networking |
| Revenue model | GPU sales + software stack; expanding into inference market segmentation |
| China situation | Subject to US export controls; Huawei identified as most serious competitor if controls lifted |

## Why It Matters in This Wiki

Every major topic in this wiki eventually runs into Nvidia. Token economics (Dylan), space compute (Elon), compute bottlenecks (Dylan, Elon), model training (all AI labs) — all depend on Nvidia's supply, pricing, and roadmap. Understanding Nvidia's moat and its limits is critical for understanding the AI supply chain.

## Competitive Position

- **Moat**: Not node-based (TSMC process); architectural (CUDA ecosystem, networking, system-level engineering)
- **Threat**: Huawei (if TSMC ban lifted); custom AI ASICs (TPUs, Trainium, in-house Tenstorrent derivatives)
- **Expansion**: Groq acquisition opens premium-latency inference segment; distinct from throughput-optimised training

## Appearances in Sources

- [[wiki/sources/jensen-huang-nvidia-moat]] — primary; moat thesis, CUDA, China, Groq
- [[wiki/sources/dylan-patel-compute-bottleneck]] — supply chain role; Huawei threat
- [[wiki/sources/elon-musk-ai-space]] — Elon wants more chips; Nvidia is primary supplier but he's also diversifying to Samsung

## Connections

- Led by [[wiki/entities/jensen-huang]]
- Competes indirectly with [[wiki/entities/google]] (TPUs), Amazon (Trainium), and potentially Huawei
- Central to [[wiki/concepts/tokenomics]], [[wiki/concepts/scaling-laws]]
