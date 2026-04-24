---
type: source
title: "Dylan Patel — Inside the Trillion-Dollar AI Buildout"
source_type: transcript
date_ingested: 2026-04-25
original_file: raw/podcasts/Inside the Trillion-Dollar AI Buildout  Dylan Patel Interview.md
tags: [dylan-patel, ai-buildout, reinforcement-learning, environments, post-training, scaling, multimodal, embodiment]
---

# Dylan Patel — Inside the Trillion-Dollar AI Buildout

**Source type:** Transcript (podcast interview)  
**Host:** (Invest Like the Best / Patrick O'Shaughnessy style interview)  
**Original:** [[raw/podcasts/Inside the Trillion-Dollar AI Buildout  Dylan Patel Interview]]  
**Ingested:** 2026-04-25

---

## Summary

A third Dylan Patel interview (companion to [[wiki/sources/dylan-patel-token-supply-demand]] and [[wiki/sources/dylan-patel-compute-bottleneck]]), this one focused on the *post-training frontier*: reinforcement learning environments, multimodal scaling, and whether the "data wall" in text pre-training matters as much as people think. Dylan argues we're in the "first ball thrown" of RL/environment post-training — early innings — while text pre-training is "late innings" but not over, and multimodal (video/audio/image) pre-training is "mid innings." The trillion-dollar buildout refers to the physical infrastructure investment.

---

## Key Claims

- **Text pre-training is late innings, not done**: We've consumed most internet text, but you can train smarter (better architecture, better curriculum). The same textbook read differently yields different results. Pre-training gains feed directly into post-training efficiency.
- **Multimodal pre-training is mid innings**: Video, audio, and image are computationally very expensive — "so expensive we didn't get to that." There's enormous latent value in scaling multimodal models. Google's video/image models (Genie, V3) are evidence of this path.
- **RL/environment post-training is early innings — first ball thrown**: The diversity of environments you can train on (math puzzles, medical cases, code execution, games, data cleaning) is almost unlimited. From Q4 of 2024 to Q2 of 2025, models climbed math benchmarks dramatically through RL, not from raw internet text.
- **Environments are the hard engineering problem now**: Pre-training was: filter internet data, throw at model. Post-training requires building rich, graded, iterative environments. That's a different engineering discipline.
- **Embodiment might be required for AGI**: Dylan discusses the view (associated with Elon/xAI) that models need to be embodied in robots to learn physical intuition — concepts that can't be extracted from video alone (weight, resistance, rotation). This is an open question.
- **Software SaaS business model is in trouble**: As AI drops the cost of building competing software stacks to near-zero, the SaaS model (high CAC, high R&D amortized over many customers) breaks. COGS goes up, CAC stays high, competitor count rises = no escape velocity. Exception: systems-of-record with long data half-lives (ERP, Salesforce records) are protected; seat-pricing models (Zendesk) are in trouble.
- **Robots will be cloud-driven**: On-device robots need leading-edge, low-power chips — they compete with data center demand. Better to have the large model in cloud driving robot actions at 1-10Hz, with lightweight on-device interpolation.

---

## Notable Quotes

> "It's not like pre-training is done. Any gains on pre-training — the model learns a little faster or is a little bit smaller for the same quality — feeds into the next stage, which will subsume the majority of the compute." — Dylan Patel

> "We're so early in reinforcement learning. Think about how much we observe throughout our life and how much information we throw away. These models throw away infinitely more." — Dylan Patel

> "The software companies most at risk are where they are pricing the product based on utility per seat. Zendesk is a good example — I can have 30 AI agents sitting next to Zendesk, paying for 20 seats instead of 50." — Dylan Patel

---

## Connections

- Third source for [[wiki/entities/dylan-patel]]
- Extends [[wiki/concepts/post-scaling-research]] — RL environments as the next frontier; specific engineering challenges
- Extends [[wiki/concepts/scaling-laws]] — pre-training not dead, multimodal has long runway, post-training is early
- New material for [[wiki/concepts/ai-diffusion]] — software SaaS business model disruption is a diffusion-layer consequence
- Related to [[wiki/sources/ilya-sutskever-age-of-research]] — both see environments/RL as the post-data-wall path; slightly different framings

---

## Questions Raised

- What does a world look like where most model improvement comes from RL environments rather than internet text? Who builds the environments — labs, enterprises, open source?
- At what COGS percentage does SaaS become unviable? Which specific public software companies are most at risk, and which are most protected?
- Does embodiment (robot + physical sensing) actually unlock capabilities unavailable from video data? What's the evidence?
