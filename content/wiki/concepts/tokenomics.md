---
type: concept
title: "Tokenomics"
tags: [tokens, ai, economics, supply-demand, anthropic, compute]
---

# Tokenomics

## Definition

Tokenomics (a term used by [[wiki/entities/dylan-patel]]) refers to the full economics of AI token consumption: who buys them, at what price, at what scale, and what economic value they generate relative to their cost. It encompasses both the supply side (compute infrastructure, GPU pricing, memory, fabs) and the demand side (end-user adoption, use-case discovery, willingness to pay).

## How It Appears in This Wiki

This concept is the central lens of the [[wiki/sources/dylan-patel-token-supply-demand]] source and Dylan's life's work. It has no equivalent prior page in this wiki — it is a new domain introduced by this source.

## The Demand Equation

Token demand is not driven by falling prices (though prices are falling fast) — it is driven by **new use cases unlocking at the frontier**. When Mythos was released internally, it opened up tasks that Opus 4.6 couldn't do reliably. This creates a demand step-function, not a smooth curve.

Key demand dynamics:
- **Frontier preference is absolute**: Once a better model exists, users refuse to go back. The jump from 4.6 to 4.7 to Mythos is experienced as non-negotiable.
- **Use-case discovery is the bottleneck**: Demand grows as people discover what tokens can do, not as tokens get cheaper.
- **Diffusion is slow**: You and I adopt on day one; most businesses take months or years. Even linear diffusion of existing Opus 4.6 quality usage would imply $100B+ annual spend.
- **Compute constraints create scarcity**: Demand far exceeds supply. Anthropic is managing this via rate limits, enterprise contracts, and selective access.

## The Supply Equation

Every layer of the stack is margin-expanding and supply-constrained:

| Layer | Status |
|-------|--------|
| GPUs (H100/B200) | Prices rising; useful life extended to 7–8+ yrs; clusters re-signing |
| DRAM memory | Will double/triple again; new capacity not until 2028 |
| Logic fabs (TSMC) | Capex possibly $100B in 2028; squeezing every fab; cautious on pricing |
| Wafer fab equipment (ASML etc.) | Sold out; Carl Zeiss upstream constraint |
| CPUs | Sold out; RL environments + inference deployment both CPU-heavy |
| Power/energy | Macro supply deficits in many US regions |
| Copper foil, glass fiber, optics | Niche but fully sold out; people paying large prepayments |

The core dynamic: **economic value unlocked by tokens is growing faster than infrastructure to serve them.** This gap produces expanding margins at every layer, especially model labs.

## The Arbitrage Opportunity (Dylan's framework)

Three steps to capture value from tokenomics:
1. **Use more tokens** — raw consumption
2. **Generate economic value** from those tokens
3. **Capture that value** — the hardest step; requires being faster than commoditization

Those who fail at step 3 will be outcompeted by those who are earlier, faster, or have better model access. This is the origin of [[wiki/concepts/ai-permanent-underclass]].

## Model Hoarding

A new structural dynamic: elite firms (top banks, Citadel-class funds) are getting early or exclusive access to the most capable models. Example: Mythos deployed only to select banks for cybersecurity. This creates a compounding moat: better model → better outputs → more economic value → can afford to buy even more early access.

## Key Sources

- [[wiki/sources/dylan-patel-token-supply-demand]] — primary and founding source for this concept

## Related Concepts

- [[wiki/concepts/scaling-laws]] — the supply-side driver of why frontier tokens are uniquely valuable
- [[wiki/concepts/ai-permanent-underclass]] — the social consequence of unequal token access
- [[wiki/concepts/phantom-gdp]] — the invisible economic value that tokenomics produces
- [[wiki/concepts/ai-psychosis]] — the demand-side irrationality that tokenomics interacts with

## Open Questions

- Is there a natural equilibrium where token demand and supply balance, or will compute constraints remain structural past 2028?
- How does model hoarding change the competitive landscape in finance, information services, and other knowledge-intensive industries?
- Does Anthropic's margin expansion continue, or does OpenAI's compute advantage allow them to price below Anthropic and steal enterprise share?
