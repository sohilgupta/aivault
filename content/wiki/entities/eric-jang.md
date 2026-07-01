---
type: entity
title: "Eric Jang"
entity_type: person
tags: [rl, robotics, alphago, self-play, research]
---

# Eric Jang

**Type:** Person (AI researcher)

## Overview

Eric Jang is an AI researcher, most recently VP of AI at 1X Technologies (humanoid robotics) and previously a senior research scientist at what is now Google DeepMind Robotics. On a sabbatical he rebuilt AlphaGo from scratch (largely LLM-assisted, ~$10K compute) to study self-play RL and what it implies for the future of LLMs and automated AI research.

## Key Facts

| Attribute | Value |
|-----------|-------|
| Recent role | VP of AI, 1X Technologies |
| Prior | Senior research scientist, Google (Brain/DeepMind) Robotics |
| Sabbatical project | Rebuild + improve AlphaGo (~$10K, Prime Intellect grant) |
| Expertise | RL, imitation learning (DAgger), robotics, self-play |
| Signature insight | AlphaGo is elegant RL because you never start at 0% success — it's supervised learning on improved labels |

## Intellectual Contributions (from source)

- MCTS as a policy-improvement operator; distill the visit-count *distribution* (soft labels) for more bits/sample.
- RL is doubly inefficient vs supervised learning: samples/FLOP drop with horizon length; bits/sample are near-zero at low pass rate ("supervision through a straw").
- Off-policy training is fine (DAgger view) when it funnels drift states back to the optimal trajectory.
- Observations on automated AI research: LLMs are strong at hyperparameter/code search and running experiments, weak at choosing the next experiment and lateral first-principles thinking.

## Appearances in Sources

- [[wiki/sources/eric-jang-alphago-selfplay]] — primary; AlphaGo from scratch, MCTS, self-play, RL efficiency, automated research

## Connections

- Core voice for [[wiki/concepts/self-play-rl]]
- Extends [[wiki/concepts/scaling-laws]] (inference/training compute tradeoff, distillation)
- Robotics/DAgger background ties to [[wiki/entities/google]] (DeepMind); uses [[wiki/entities/anthropic]] Opus models for automated research
