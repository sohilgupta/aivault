---
type: concept
title: "Self-Play RL and MCTS"
tags: [rl, self-play, mcts, alphago, distillation, exploration]
---

# Self-Play RL and MCTS

## Definition

Reinforcement learning in which an agent improves by playing against itself, using search (e.g. Monte Carlo Tree Search) as a policy-improvement operator whose outputs are distilled back into the network. Exemplified by AlphaGo/AlphaZero, and contrasted with the policy-gradient RL used for LLMs.

## How It Appears in This Wiki

Introduced via Eric Jang's from-scratch AlphaGo rebuild ([[wiki/sources/eric-jang-alphago-selfplay]]). The central lesson explains *why* self-play RL is so effective and why it doesn't transfer cleanly to LLMs.

- **MCTS = improvement operator.** Neural nets prune breadth (policy) and depth (value; truncate search before the leaf). Distill the peaky post-search visit-count distribution into the raw policy net → it starts from a better point next iteration, amortizing search compute into the forward pass.
- **AlphaGo is elegant RL** because you never start at 0% success and never solve exploration — it's just supervised learning on improved labels (policy KL + value classification). Stable training, simple infra.
- **Why it doesn't work (yet) for LLMs:** value estimation isn't concrete, breadth is enormous (100K-token vocab — you rarely resample a child, breaking the √N/(1+Nₐ) heuristic), and PUCT is too greedy/local.
- **RL is doubly inefficient vs supervised learning.** Bits/FLOP = samples/FLOP × bits/sample. Long horizons cut samples/FLOP ("supervision through a straw"); bits/sample are near-zero at low pass rate. Distillation / soft labels carry far more bits/sample (why AlphaGo trains on the distribution, not the action).
- **Off-policy is fine** (DAgger view) when it labels drift states to funnel back to the optimal trajectory.
- **Inference/training compute tradeoff** — Andy Jones (2021) "Scaling Scaling Laws with Board Games" anticipated inference scaling: more search ≈ more training.

## Key Sources

- [[wiki/sources/eric-jang-alphago-selfplay]] — primary; MCTS mechanics, self-play loop, RL efficiency, automated research
- [[wiki/sources/reiner-pope-training-serving]] — RL compute cost (~2-6 FLOP/param) in the training/inference balance
- [[wiki/sources/gavin-baker-gpu-economics]] — RLVR as a post-training scaling law

## Related Concepts

- [[wiki/concepts/scaling-laws]] — search-vs-training compute, distillation bits/sample, bitter lesson
- [[wiki/concepts/post-scaling-research]] — RL/reasoning as the next research frontier

## Open Questions

- Will forward search / tree structures return for LLM reasoning in some new form?
- Can MCTS/MuZero-style value-truncated search adapt to language or continuous action spaces?
- Does the near-zero-pass-rate initialization problem bound pure RL without supervised/distillation warm starts?
