---
type: entity
title: "Groq"
entity_type: organisation
tags: [groq, lpu, inference, ai-hardware, asic]
---

# Groq

**Type:** Organisation
**Also known as:** maker of the LPU (Language Processing Unit)

## Overview

Groq is an AI inference-hardware company founded by [[wiki/entities/jonathan-ross]] (inventor of Google's TPU). Its chip, the **LPU**, is a purpose-built inference accelerator optimized for low-latency, high-throughput token *generation* — the memory-throughput-bound part of the LLM decoder — as opposed to the compute-bound attention part that GPUs handle well. Groq's decade-long contrarian bet was that **fast inference makes models smarter and would become economically central**, a thesis widely dismissed (including internally) until ~2023–24.

## Key Facts

| Attribute | Value |
|-----------|-------|
| Founder / CEO | Jonathan Ross (ex-Google, TPU inventor) |
| COO | "Sunny" (originated the GPU+LPU pairing idea) |
| Key product | LPU (Language Processing Unit) — inference ASIC |
| Headcount at NVIDIA deal | ~450 |
| NVIDIA deal | ~$20B licensing/partnership (2026); NVIDIA's largest deal "by ~3x"; closed idea-to-wire in ~3 weeks |
| Near-death event | ~3 weeks from insolvency (years earlier); saved by "Groq bonds" (salary-for-equity swaps) |
| Funding note | Backed largely by East Coast / crossover VCs after West Coast VCs passed |

## Why It Matters in This Wiki

Groq is the concrete embodiment of the premium-latency inference thesis and of purpose-built inference ASICs. It sits alongside [[wiki/entities/etched]] (Sohu) and MatX ([[wiki/entities/reiner-pope]]) as a non-GPU inference bet — but is the one that ended in a landmark NVIDIA deal rather than head-on competition.

## GPU + LPU Complementarity

Within a decoder layer, attention is compute-bound (better on GPU) and weight application is memory-throughput-bound (better on LPU). Combining them defeats bottlenecks across the whole matmul curve — "18-wheelers and last-mile vans." The non-obvious win is co-locating both chip types on token *generation* ("writing"), not splitting prefill/decode across chips.

## Appearances in Sources

- [[wiki/sources/jonathan-ross-groq]] — primary; LPU thesis, AlphaGo→TPU origin, NVIDIA deal, Groq bonds, leadership
- [[wiki/sources/jensen-huang-nvidia-moat]] — referenced as NVIDIA's inference-market move (that source frames it as an "acquisition"; see contradiction below)

## Contradiction Flag

[[wiki/sources/jensen-huang-nvidia-moat]] and the entity pages [[wiki/entities/nvidia]] / [[wiki/entities/jensen-huang]] originally described NVIDIA **acquiring** Groq. Ross's own account ([[wiki/sources/jonathan-ross-groq]]) frames it as a **~$20B licensing/partnership** with Ross joining NVIDIA as an executive, not an acquisition of the company. Treat "partnership/licensing" as the primary account; "acquisition" flagged as unverified/loose usage.

## Connections

- Founded and led by [[wiki/entities/jonathan-ross]]
- Deep partnership with [[wiki/entities/nvidia]] / [[wiki/entities/jensen-huang]]
- Central to [[wiki/concepts/asic-vs-gpu]], [[wiki/concepts/inference-economics]], [[wiki/concepts/tokenomics]]
- Peer inference-ASIC bets: [[wiki/entities/etched]], [[wiki/entities/reiner-pope]] (MatX)
