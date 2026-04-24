---
type: concept
title: "Post-Scaling Research"
tags: [scaling, research, ilya-sutskever, synthetic-data, continual-learning, agi, algorithms]
---

# Post-Scaling Research

## Definition

"Post-scaling research" describes the era of AI development that follows the exhaustion of simple pre-training data scaling. [[wiki/entities/ilya-sutskever]] introduced this framing: the "age of scaling" (training ever-larger models on more internet text) is giving way to the "age of research," where algorithmic insight — not raw compute — becomes the limiting factor.

## The Data Wall

Current LLMs are trained primarily on internet text. There is a finite amount of high-quality human-generated text on the internet, and it has been largely consumed. Adding more compute to the same data distribution yields diminishing returns. The practical evidence: Ilya's observation that all pre-trained models are surprisingly similar, because they all train on the same internet corpus.

## What Replaces Scaling?

Ilya identifies several candidate directions:

1. **Synthetic data**: Generate training data with AI itself. This removes the internet text ceiling but raises the question: does training on AI-generated data lead to capability gains or to mode collapse (degeneration)?

2. **Continual learning / lifelong learning**: Build models that update incrementally from experience, like humans do. This is qualitatively different from current train-then-deploy models. A continual learning agent deployed in the world could compound its capabilities in ways static models cannot.

3. **New training paradigms**: Self-play, prover-verifier, adversarial debate. These use compute without new human data by having models compete and improve against each other. Narrow (good for strategic/social skills), but the best current example of post-scaling research yielding results.

4. **Better post-training / RL**: Differentiation increasingly comes from RL and RLHF, not pre-training. Where pre-training homogenises, post-training differentiates.

## The Tension with Dario's Thesis

This is the most important intellectual tension in the wiki:

| Position | Who | Claim |
|---------|-----|-------|
| Scaling still works | [[wiki/entities/dario-amodei]] | Mythos is proof; compute scaling still yields capability gains; we're near the end of the exponential |
| Scaling is ending | [[wiki/entities/ilya-sutskever]] | The data wall is real; paradigm is shifting; age of research is beginning |

**Possible reconciliation**: Both can be true simultaneously:
- **Compute scaling** still works — more FLOPs on a fixed high-quality data distribution still yields better models (Dario's claim)
- **Data scaling** on internet text has hit diminishing returns (Ilya's claim)
- Synthetic data and post-training are the new frontier for data, but the jury is out on whether they can substitute for novel high-quality human text

## Research Taste as the Key Differentiating Skill

If algorithms matter more than raw compute, then the skill of knowing *which* research directions to pursue becomes scarce and valuable. Ilya defines research taste as: guided by aesthetic (beauty, simplicity), brain-inspired intuition, and able to maintain top-down conviction when experiments fail.

## Key Sources

- [[wiki/sources/ilya-sutskever-age-of-research]] — primary; data wall, continual learning, self-play, research taste
- [[wiki/sources/dario-amodei-end-of-exponential]] — the tension; scaling still holds in Dario's view

## Related Concepts

- [[wiki/concepts/scaling-laws]] — the thing this concept supplements/challenges
- [[wiki/concepts/biological-revolution]] — post-scaling research is needed to reach the biology compression thesis
- [[wiki/concepts/agentic-engineering]] — continual learning agents would change what agentic engineering means

## Open Questions

- At what point does synthetic data training lead to mode collapse or capability ceiling?
- What is SSI (Ilya's company) actually building — and is it a radically new architecture or a refined version of current LLMs?
- If research taste is scarce, is it teachable? Or is it a permanent bottleneck?
- Does the compute vs data distinction hold indefinitely, or does post-training RL eventually also hit a data wall?
