---
type: entity
title: "Reiner Pope"
entity_type: person
tags: [chip-design, matx, tpu, inference]
---

# Reiner Pope

**Type:** Person
**Also known as:** CEO of MatX

## Overview

Reiner Pope is the CEO of MatX, a new AI chip startup, and previously worked on TPU architecture (and much else) at Google. He is known for exceptionally clear first-principles explanations of how AI hardware and inference work, delivered as blackboard lectures with Dwarkesh Patel.

## Key Facts

| Attribute | Value |
|-----------|-------|
| Role | CEO, MatX |
| Prior | TPU architecture, Google |
| Known for | Bottom-up chip design + inference-economics lectures |
| Signature idea | Maximize compute relative to communication, at every level of the stack |
| MatX teaser | "Splittable systolic array" (big arrays that can act as small ones) |

## Appearances in Sources

- [[wiki/sources/reiner-pope-training-serving]] — how frontier LLMs are trained/served; batch size, MoE-on-rack, parallelism, ~100x over-training
- [[wiki/sources/reiner-pope-chip-design]] — logic gates → systolic arrays → FPGA/ASIC → GPU-vs-TPU

## Connections

- Runs MatX, an ASIC challenger — relevant to [[wiki/concepts/asic-vs-gpu]]
- Explains the mechanics behind [[wiki/concepts/inference-economics]] and [[wiki/concepts/scaling-laws]]
- Analytical counterpart to [[wiki/entities/dylan-patel]] and [[wiki/entities/gavin-baker]] on compute/hardware
- Discusses hardware from [[wiki/entities/nvidia]] (Blackwell/Rubin, Tensor Cores, FP4) and [[wiki/entities/google]] (TPUs)
