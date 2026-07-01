---
type: concept
title: "Scaling Laws"
tags: [ai, compute, models, research, capability, anthropic]
---

# Scaling Laws

## Definition

Scaling laws are empirical relationships observed in AI model training that describe how model capability improves predictably as a function of compute, data, and model size. More compute (and/or more data, or more parameters) reliably produces a more capable model — this relationship has held across many orders of magnitude and shows no clear sign of breaking down as of early 2026.

## How It Appears in This Wiki

Introduced by [[wiki/sources/dylan-patel-token-supply-demand]] as the supply-side explanation for why frontier model access is uniquely valuable and why token demand keeps growing. Mythos (Anthropic's internally-available model) is presented as the strongest recent validation that scaling laws still hold.

## Mythos as Proof

Anthropic internally released Mythos in February 2026. By April 2026, Claude 4.7 Opus was the public frontier. Dylan describes Mythos as:
- A materially larger model than prior generations
- Potentially the biggest capability jump in 2 years
- Rated internally at ~L6 software engineer level (vs 4.6 Opus's ~L4)
- 5–10x more expensive per token than Opus 4.6, but more token-efficient per task — often cheaper overall

The jump from L4 to L6 in two months (February to April) demonstrates both:
1. That scaling laws still produce step-change capability improvements when you push compute hard enough
2. That release cadence is now compressing (was 6 months between major models; now 2 months)

## The Two Compounding Effects

Scaling laws operate via two simultaneous axes:
1. **Raw capability jumps**: Throw enough compute at a model and you get a non-linear capability leap.
2. **Compute efficiency wins**: Reaching a given capability tier gets cheaper over time (Deepseek hit GPT-4 quality at 1/600th the cost). This frees up budget for even bigger models.

Both effects are happening simultaneously. The result: at any given capability tier, cost is falling — but the frontier keeps moving upward, so demand for the frontier keeps growing.

## Implications for Supply/Demand

- Compute constraints matter more than ever: you cannot get Mythos-level capability without massive compute investment. There is no shortcut.
- Each new capability tier unlocks qualitatively new use cases, not just more of the same. This is why demand is not price-elastic at the frontier.
- Labs with more compute (OpenAI vs Anthropic) have a structural advantage in reaching capability tiers sooner, even if their current models lag.

## Release Cadence Compression

Because implementation is now cheap (AI does it), labs can run more experiments per unit time. This means:
- More ideas tested faster
- More research compute can be applied iteratively
- External release cadence goes from 6 months → 2 months → potentially faster

## The Two New Post-Training Scaling Laws (Gavin Baker)

From [[wiki/sources/gavin-baker-gpu-economics]], Baker identifies two additional scaling laws that operate independently of pre-training:

1. **Reinforcement learning with verified rewards (RLVR)**: Any task where you can verify the correct answer can be trained via RL. This is distinct from RLHF (human preference) — it requires no human labellers, just a verifier.
2. **Test-time compute**: Allowing the model to "think longer" at inference time improves output quality. This is an inference-time scaling law, not a training-time one.

ARC-AGI benchmark moved from 8% to 95% in three months when reasoning models launched (Oct 2024), on the back of these two laws — not new hardware. Gemini 3 then confirmed the pre-training scaling law is still intact on top of these two.

All three scaling laws are **multiplicative** — better base models + better post-training + more inference compute compound together.

## Key Sources

- [[wiki/sources/dylan-patel-token-supply-demand]] — Dylan's explicit discussion of Mythos as scaling law proof; release cadence compression
- [[wiki/sources/gavin-baker-gpu-economics]] — two new post-training scaling laws; Gemini 3 confirmation; ARC-AGI evidence
- [[wiki/sources/reiner-pope-training-serving]] — equalizing train/RL/inference compute implies models are ~100x over-trained beyond Chinchilla; RL = 2-6 FLOP/param
- [[wiki/sources/gavin-baker-watts-wafers]] — bitter lesson (and its possible ASI-driven violation) and continual learning as the biggest scaling risks
- [[wiki/sources/eric-jang-alphago-selfplay]] — inference-compute/training-compute tradeoff (Andy Jones 2021); distillation bits/sample; RL info-inefficiency

## Related Concepts

- [[wiki/concepts/inference-economics]] — the train/inference compute balance that drives over-training
- [[wiki/concepts/self-play-rl]] — RL/search as a scaling axis; why AlphaGo-style RL differs from LLM RL
- [[wiki/concepts/tokenomics]] — scaling laws drive why frontier tokens generate outsized value
- [[wiki/concepts/ai-permanent-underclass]] — those with frontier model access benefit from capability jumps; others don't
- [[wiki/concepts/agentic-engineering]] — what becomes possible when scaling laws keep delivering better base models

## Open Questions

- Is there a physical or information-theoretic ceiling to scaling laws, and if so, where is it?
- Does model hoarding (selective Mythos release) suggest Anthropic believes the next jump will be even more dramatic — and therefore dangerous to release broadly?
- Will OpenAI's aggressive compute build-out allow it to leap past Anthropic's quality lead?
