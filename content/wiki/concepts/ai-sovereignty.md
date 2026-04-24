---
type: concept
title: "AI Sovereignty"
tags: [sovereignty, geopolitics, trust, open-source, concentration-risk, microsoft, satya-nadella]
---

# AI Sovereignty

## Definition

AI sovereignty refers to a country's or organisation's ability to control, access, and trust the AI systems it depends on — including where models are trained, where data is stored, who holds the encryption keys, and whether the provider can cut off access. It is the AI equivalent of semiconductor sovereignty or food sovereignty: a strategic rather than purely economic concern.

## Why It Matters Now

As AI becomes critical infrastructure — powering enterprise decisions, government services, and national security operations — the question of who controls the AI becomes a first-class political problem. Countries that are entirely dependent on a single foreign AI provider face:
- **Concentration risk**: If the provider changes terms, is acquired, or goes under, the country loses access
- **Data sovereignty risk**: Sensitive data processed by foreign models may be accessible to foreign governments
- **Long-term reliability uncertainty**: Will this provider still exist and be trustworthy in 10 years?

## The TSMC Analogy (and its Limits)

[[wiki/entities/satya-nadella]] offers the TSMC analogy: TSMC is just better than alternatives for semiconductors, but countries cannot accept full dependency. TSMC Arizona is "not real sovereignty" — it's not close to replacing Taiwan's actual production. But nations demand the gesture anyway.

AI is similar: the best models will likely come from a small number of labs. Countries will use them. But they will simultaneously demand:
- Data residency within their borders
- Key management sovereignty (their own encryption keys)
- Capability to switch providers (reduced lock-in)
- Some local model training capability, even if it's not frontier

## The Open Source Check

A vital structural element: open source LLMs (Llama, Mistral, etc.) ensure that no single lab can achieve permanent global lock-in. Nations know that if a proprietary provider becomes unacceptable, they can always fall back to open source. This gives them negotiating leverage and reduces the risk of dependency.

**Satya's formulation**: "Open source is always going to be there. There will, by definition, be multiple models. That's one way for people to demand continuity and not have concentration risk."

## Trust as Competitive Advantage

Satya's key insight: in the US-China AI competition, trust — not model capability — may be the decisive variable. The question becomes: "Can I trust you, the company, can I trust you, your country, and its institutions to be a long-term supplier?"

This frames American tech companies' advantage not as technological lead but as institutional trust: rule of law, long track record, reliability. Chinese alternatives may be cheaper or even technically comparable — but do governments trust that they won't be cut off, surveilled, or weaponised?

## Microsoft's Strategy

Microsoft has built sovereign cloud deployments in France and Germany, and offers "Sovereign Services on Azure" including confidential computing and confidential GPU computing (with Nvidia collaboration). This is a direct response to sovereignty as a business requirement.

## Key Sources

- [[wiki/sources/satya-nadella-microsoft-agi]] — primary; trust thesis, TSMC analogy, open source check, Microsoft sovereign cloud

## Related Concepts

- [[wiki/concepts/ai-diffusion]] — sovereignty requirements slow enterprise diffusion in regulated markets
- [[wiki/concepts/tokenomics]] — who controls the token supply chain has sovereignty implications

## Open Questions

- Will open source remain viable at the frontier, or will frontier capabilities become exclusively proprietary?
- Can a country that doesn't train foundational models ever have real AI sovereignty?
- How does the US-China bifurcation play out for countries that want to trade with both? (India, Gulf states, Southeast Asia)
- If trust is the key differentiator, what happens to US tech trust if policy behavior becomes unpredictable?
