---
type: source
title: "GPUs, TPUs, & The Economics of AI Explained — Gavin Baker Interview"
source_type: podcast
date_ingested: 2026-05-17
original_file: raw/podcasts/GPUs, TPUs, & The Economics of AI Explained  Gavin Baker Interview.md
tags: [gavin-baker, nvidia, google, tpu, gpu, blackwell, reasoning, scaling-laws, ai-economics, chips]
---

# GPUs, TPUs, & The Economics of AI Explained — Gavin Baker Interview

**Source type:** Podcast  
**Original:** [[raw/podcasts/GPUs, TPUs, & The Economics of AI Explained  Gavin Baker Interview]]  
**Published:** 2025-12-09  
**Host:** Patrick O'Shaughnessy (Invest Like The Best)  
**Ingested:** 2026-05-17

## Summary

Gavin Baker, a technology investor known for encyclopedic knowledge of AI infrastructure, gives a masterclass on the economics and competitive dynamics of AI compute. The conversation covers Blackwell's significance and delayed deployment, Google's temporary advantage as lowest-cost token producer via TPUs, how reasoning models "saved AI" by bridging an 18-month gap without new training hardware, and the emerging flywheel dynamics that now separate the four leading labs (OpenAI, Anthropic, Gemini, xAI) from all challengers.

Baker's framework is unique for its investor-grade precision: he treats GPU utilisation rates, token production costs, ROIC on AI capex, and the competitive calculus of each lab as quantifiable variables — not hand-wavy tech enthusiasm. His most important structural claim is that AI is the first technology in his career where being the **lowest-cost producer** actually matters (Apple, Microsoft, Nvidia were never cheap).

The source also contains Baker's bear case for AI demand: edge AI running a pruned frontier model locally on a phone, making cloud-based AI economically irrelevant for many use cases.

## Key Claims

- Gemini 3 confirmed scaling laws for pre-training are intact — the most important single data point in AI in the relevant period.
- Reasoning models (launched Oct 2024) "saved AI" by enabling progress through an 18-month Blackwell deployment gap: ARC-AGI went from 8% to 95% in 3 months on the back of reasoning, not new hardware.
- Two new post-training scaling laws: (1) reinforcement learning with verified rewards, (2) test-time compute. Both are multiplicative with the pre-training scaling law.
- Google had a temporary but meaningful advantage as lowest-cost token producer (TPU vertical integration + TPU v6/v7); this advantage ends once Blackwell-trained models go to inference.
- xAI will likely have the first Blackwell-trained model because no one builds data centres faster than Elon (confirmed by Jensen Huang publicly).
- After Blackwell, GB300 is drop-in compatible with GB200 racks — anyone who deployed GB200 can slot in GB300 without infrastructure rebuild.
- ROI on AI is unambiguously positive: the biggest GPU spenders have higher ROIC now than before their GPU ramp.
- Reasoning created the first real flywheel for frontier labs: verified rewards feed back into training, separating the four leaders from Meta, Microsoft, Amazon.
- Meta failed to reach top-tier model quality despite massive spend; Microsoft similarly. This proves making frontier models is much harder than assumed.
- DeepSeek v3.2 admitted Chinese labs lack compute — China's decision to block Blackwells may prove a strategic error.
- The bear case: edge AI (local phone-level inference) could make cloud AI economically marginal. "That's the bear case other than scaling laws breaking."
- "Anything you can verify, you can automate" (Karpathy quote, cited by Baker) — verification = the key to the next wave of AI automation.
- CH Robinson (freight forwarder) as first Fortune 500 non-tech company to print quantitatively AI-driven earnings: went from quoting 60% of requests in 15-45 minutes to 100% in seconds.
- Fortune 500 is always the last to adopt; AI will follow the same curve as cloud (startups first, Fortune 500 ~5 years later).

## Notable Quotes

> "Reasoning kind of saved AI because it let AI make progress without Blackwell or the next generation of TPU which were necessary for the scaling laws for pre-training to continue." — Gavin Baker

> "AI is the first time in my career as a tech investor that being the low-cost producer has ever mattered." — Gavin Baker

> "With AI, anything you can verify, you can automate." — Karpathy (cited by Baker)

> "Every one of those labs has a more advanced checkpoint internally... If you do not have that latest checkpoint, you're behind, and it's getting really hard to catch up." — Gavin Baker

## Connections

- Deepens [[wiki/concepts/scaling-laws]] — confirms pre-training scaling intact; adds two post-training scaling laws
- Extends [[wiki/entities/nvidia]] — Blackwell transition, competitive dynamics, Groq/Reuben roadmap
- Connects to [[wiki/entities/google]] — TPU economics, lowest-cost producer strategy, Broadcom dependency
- Connects to [[wiki/entities/elon-musk]] / xAI — fastest data-centre builder; first Blackwell model
- Related to [[wiki/concepts/post-scaling-research]] — reasoning models as new scaling dimension
- Complements [[wiki/sources/dylan-patel-compute-bottleneck]] and [[wiki/sources/dylan-patel-token-supply-demand]]
- Adds detail to [[wiki/concepts/agi-timeline]] — reasoning-driven progress curve

## Questions Raised

- What is Reuben (next Nvidia generation after Blackwell) and when does it ship?
- Does the reasoning flywheel actually separate the four labs, or can open-source bootstrap from Chinese models?
- At what point does edge AI become capable enough to challenge cloud inference economics?
