---
type: concept
title: "AI Diffusion"
tags: [ai, adoption, enterprise, economics, diffusion, technology]
---

# AI Diffusion

## Definition

AI diffusion is the process by which AI capabilities propagate from frontier research/early adopters into widespread economic and organisational use. It is distinct from AI capability: a model can be extraordinarily capable while diffusing slowly into the economy, resulting in a growing "intelligence overhang" — the gap between what AI can do in theory and what is actually being used in practice.

## How It Appears in This Wiki

AI diffusion is a theme across multiple sources, each offering a different perspective on its speed, barriers, and implications. It is the key concept for understanding why AI's economic impact may grow for years even if model capability improvements slowed today.

## The Feel-It-to-Believe-It Dynamic

Per [[wiki/entities/sam-altman]] in [[wiki/sources/openai-founders-core-memory]]: adoption doesn't come from reading about capabilities, winning competitions, or publishing blog posts. It comes from people *feeling* what AI can do. ChatGPT was not the most technically impressive thing OpenAI had done — but it was the first thing people could experience directly. This is the core mechanism of consumer diffusion.

Corollary: the next major mass adoption trigger will also be "feel it" — likely the personal AI that knows your full context, eliminating the constant re-explanation overhead.

## Capability vs Diffusion (Dario Amodei's Framework)

From [[wiki/sources/dario-amodei-end-of-exponential]]:
- **Capability exponential**: The model gets dramatically better on some fast curve.
- **Diffusion exponential**: The model's capabilities spread into the economy on a *different*, slower but still fast, curve.

These are two separate curves. Dario argues both are fast—faster than any prior technology—but diffusion lags capability by months to years. The current moment has an enormous intelligence overhang: AI can already do things that most people and organisations haven't yet figured out how to use.

Dario dismisses "diffusion is cope" (the claim that diffusion is just an excuse for AI not being as useful as claimed) — but notes AI *will* diffuse much faster than electricity or the printing press due to:
- Near-zero replication cost (software)
- Employees can onboard AI by reading your Slack, not learning over years
- No adverse selection in "hiring" AI

## Enterprise vs Individual Diffusion Gap

Multiple sources document a consistent gap between individual/startup adoption and enterprise adoption:

| Adopter type | Typical lag from release |
|---|---|
| Power users / Twitter-active devs | Days to weeks |
| Series A startups | Weeks to months |
| Large enterprises (SaaS, financial) | Months (Claude Code enterprise — per Dario) |
| Large enterprises (non-Eng workflows) | ~1–2 years (per Sundar: 2027 for Google itself) |

Per Patrick Collison (Stripe CEO, in [[wiki/sources/sundar-pichai-google-ai-history]]), the enterprise barriers are:
1. **Prompting skill** — both general and firm-specific prompting take time to develop
2. **Code blast radius** — AI generates so much code so fast that collaboration becomes harder
3. **Identity/access permissions** — agents need data access; current permission engines weren't built for this
4. **Role redefinition** — Eng/PM/Design boundaries may need to merge
5. **Security/compliance** — large firms have legal, security, and change management requirements

## Diffusion as Opportunity

The flip side of the diffusion lag is that it creates a sustained opportunity window: firms that adopt early have compounding advantages before diffusion equalises the playing field. This is the core of [[wiki/concepts/ai-permanent-underclass]] — those who fail to diffuse AI into their own workflows fall behind irreversibly.

## Key Sources

- [[wiki/sources/openai-founders-core-memory]] — ChatGPT feel-it-to-believe-it moment; personal AGI as next trigger
- [[wiki/sources/dario-amodei-end-of-exponential]] — most careful articulation of capability vs diffusion as separate curves; enterprise Claude Code as live case
- [[wiki/sources/sundar-pichai-google-ai-history]] — enterprise barriers taxonomy (Patrick Collison); Google's 2027 inflection prediction
- [[wiki/sources/dylan-patel-token-supply-demand]] — demand-side evidence of explosive diffusion among early adopters

## Related Concepts

- [[wiki/concepts/ai-permanent-underclass]] — diffusion failure is the mechanism of stratification
- [[wiki/concepts/tokenomics]] — diffusion drives the demand curve for tokens
- [[wiki/concepts/phantom-gdp]] — diffusion determines how fast phantom GDP accumulates
- [[wiki/concepts/personal-agents]] — likely the next major "feel it" diffusion trigger
- [[wiki/concepts/agentic-engineering]] — the skill set required to actually diffuse AI into workflows

## Open Questions

- Is there a way to measure the current intelligence overhang — what AI can do vs what's actually being used?
- Will the personal AI "know you" moment be the next ChatGPT-scale adoption trigger?
- Does Google's internal 2027 timeline predict large-enterprise adoption globally, or just Google-specific?
- What's the right diffusion comparison class for AI? Electricity? Mobile? The internet? Each implies a very different timeline and shock to labour markets.
