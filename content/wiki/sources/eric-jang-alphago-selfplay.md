---
type: source
title: "What rebuilding AlphaGo teaches us about self-play, RL, and future of LLMs - Eric Jang"
source_type: transcript
date_ingested: 2026-05-23
original_file: raw/podcasts/What rebuilding AlphaGo teaches us about self-play, RL, and future of LLMs - Eric Jang.md
tags: [alphago, mcts, self-play, rl, scaling-laws, distillation, automated-research, dwarkesh]
---

# What rebuilding AlphaGo teaches us about self-play, RL, and future of LLMs - Eric Jang

**Source type:** Transcript (Dwarkesh Patel blackboard lecture; Eric Jang, ex-VP AI at 1X, ex-Google DeepMind Robotics)
**Ingested:** 2026-05-23
**Original:** [[raw/podcasts/What rebuilding AlphaGo teaches us about self-play, RL, and future of LLMs - Eric Jang]]

## Summary

Eric Jang rebuilds AlphaGo from scratch on a sabbatical (~$10K of rented compute via a Prime Intellect grant, largely LLM-assisted) and uses it to explain self-play RL and why it works so much better than the RL used for LLMs. He walks through Go rules and Tromp-Taylor scoring, Monte Carlo Tree Search (UCB1 → PUCT selection, expansion, evaluation, backup), the policy + value networks, and the self-play policy-improvement loop where MCTS acts as an "improvement operator": you distill the MCTS visit-count distribution back into the raw network so it starts from a better point next iteration.

The payoff for AI generally: AlphaGo is an elegant RL algorithm because you never start at 0% success and never have to solve exploration — it's just supervised learning on improved labels (policy KL + value classification), so training is stable and infra is simple. This contrasts sharply with LLM policy-gradient RL, which learns "through a straw" (whole-trajectory supervision) and is doubly inefficient: samples-per-FLOP drops as horizons lengthen, and bits-per-sample is far worse than supervised/soft-label distillation, with almost all training time spent in a near-zero pass-rate regime.

## Key Claims

- **Go was thought intractable** (~361^300 tree, more than atoms in the universe). AlphaGo's breakthrough: neural nets prune both breadth (policy net → which moves) and depth (value net → truncate search before the leaf, like a human glancing at a board).
- **MCTS = 4 steps per simulation** (selection via PUCT, expansion, evaluation with value net Vθ, backup). Runs from scratch each move (200-2048 sims in training; tens of thousands for the Lee Sedol match). Value flips as 1−V in the zero-sum game. Store visit counts, mean action value Q, prior P, children.
- **The raw policy net alone is already a strong player** (~<3M params, argmax the move) — beats most humans — but MCTS makes it much better.
- **Self-play improvement operator:** distill the peaky post-MCTS visit-count distribution into the policy net → the net "starts here" instead of at 0 sims, then 1000 more sims climb higher. Amortizes search compute into the forward pass. Andy Jones (2021) "Scaling Scaling Laws with Board Games" anticipated inference-compute/training-compute tradeoff.
- **MCTS isn't guaranteed better than the policy** — only a heuristic; fails if value functions are wrong (e.g. bots resign instead of playing to Tromp-Taylor end → forget late-stage values). Fix: force ~10% of games to resolve fully. Guaranteed only as sims→∞.
- **Off-policy is fine in AlphaGo** (DAgger view): you want mostly on-distribution states plus a tube of drift states with labels funneling back to the optimal trajectory. Off-policy only hurts if you label states you'd never visit. Jang even relabels random old states with the current net (robotics-style replay buffer) — works.
- **Why MCTS doesn't (yet) work for LLMs:** value estimation isn't concrete, breadth is enormous (100K-token vocab; you'll rarely resample the same child, so √N/(1+Nₐ) exploration heuristic breaks), and PUCT may be too greedy/local. LLMs do something reasoning-like without an explicit tree; forward search "might make a comeback" but jury's out.
- **RL is doubly information-inefficient.** Bits/FLOP = samples/FLOP × bits/sample. Long horizons cut samples/FLOP ("supervision through a straw"). Bits/sample is terrible: an untrained model guessing "the sky is ___" over 100K tokens learns almost nothing per sample (binary-entropy signal) vs supervised cross-entropy (−log p). Most of training is spent at near-zero pass rate where signal ≈ 0.
- **Distillation / soft labels give far more bits/sample** than one-hot — why AlphaGo trains on the MCTS *distribution*, not just the selected action, and why distillation is so effective.
- **Compute-efficiency of catching up:** AlphaGo Zero was ~3e23 FLOPS (an aberration on the compute-vs-time curve); Jang did it for ~$10K because first-movers optimize for "getting it to work," not compute-optimality, and followers use distillation/best-response training against KataGo (David Wu, Jane Street; 40x compute reduction in 2020). Architecture (ResNet vs Transformer) barely matters now; ResNets win at low budgets (local conv inductive bias); simpler synchronous infra works; small-board (9x9) pretraining warm-starts 19x19.
- **Automated AI research (Opus 4.6/4.7):** great at open-ended hyperparameter/code search and executing/plotting experiments (a "grad-student grind"); weak at picking the *next* experiment in a track and lateral "step back to first principles" thinking. Jang had to catch infra bugs himself. Opportunity: RL environments that reward lateral thinking.

## Notable Quotes

> "You get supervision through a straw." — on LLM trajectory-level RL (Karpathy paraphrase)

> "The major reason [AlphaGo is elegant] is that you never have to initialize at a zero percent success rate and solve the exploration problem." — Eric Jang

> "The problem with Go and chess is that the other player is always trying to do some shit." — on why off-policy correction (DAgger) matters

## Connections

- Deepens [[wiki/concepts/self-play-rl]] (new) — MCTS as improvement operator, why it beats LLM policy-gradient RL
- Extends [[wiki/concepts/scaling-laws]] — inference-compute/training-compute tradeoff (Andy Jones), bitter lesson, distillation bits/sample
- Complements [[wiki/sources/reiner-pope-training-serving]] on RL compute inefficiency (both discuss RL as ~2-6 FLOP/param and its cost)
- KataGo/David Wu tie to [[wiki/sources/jane-street-gpus-trading]] (Jane Street ML culture)
- Related to [[wiki/entities/eric-jang]] (new), [[wiki/entities/google]] (DeepMind AlphaGo), [[wiki/entities/anthropic]] (Opus/Mythos automated research)

## Questions Raised

- Will forward search / tree structures return for LLM reasoning in some new form, or is implicit reasoning enough?
- Can MCTS/MuZero-style value-truncated search be adapted to high-dimensional/continuous or language action spaces?
- Does the near-zero-pass-rate initialization problem bound how far pure RL can take LLMs without supervised/distillation warm starts?
