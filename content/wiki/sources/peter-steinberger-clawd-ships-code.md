---
type: source
title: "Peter Steinberger — The Creator of Clawd: 'I Ship Code I Don't Read'"
source_type: transcript
date_ingested: 2026-04-25
original_file: raw/podcasts/The creator of Clawd "I ship code I don't read".md
tags: [peter-steinberger, openclaw, agentic-engineering, pspdfkit, vibe-coding, agents, prompts]
---

# Peter Steinberger — "I Ship Code I Don't Read"

**Source type:** Transcript (podcast interview)  
**Note:** This is Peter Steinberger in a second interview, primarily about the PSPDFKit → OpenClaw transition. The "Clawd" in the title refers to OpenClaw (his agent product uses Claude).  
**Original:** [[raw/podcasts/The creator of Clawd "I ship code I don't read"]]  
**Ingested:** 2026-04-25

---

## Summary

A second Peter Steinberger interview, this time focused on the PSPDFKit origin story and the transition to AI-first development. Peter describes his coding philosophy in the OpenClaw era: **he reads prompts, not pull requests**. The key metric is no longer code quality — it's the quality of the prompt request and the structural clarity of the problem definition. He onboards users by pointing an agent at the repository to read and configure itself. He ships code he hasn't read because the agent wrote it correctly.

This is the most granular source in the wiki on real-world agentic engineering practice — complementing the philosophical framing from the Lex Fridman interview.

---

## Key Claims

- **"I read prompts, not code"**: When reviewing contributions, Peter is more interested in the prompts used than the code produced. The prompt is a higher-signal indicator of how the developer thinks and how much steering was involved.
- **The work is the thinking, not the coding**: If someone writes a "prompt request" (describing a feature clearly), Peter can point an agent at the GitHub issue and it will implement it correctly. "The work is thinking about how it should work."
- **Agents are better at navigating agent-built code**: Because OpenClaw was built by agents, the code is structured exactly how agents expect — named in ways encoded in model weights. Agents navigate it better than humans do.
- **"Agentic onboarding" replaced manual onboarding**: Instead of a manual setup guide, onboarding was literally: "Type this prompt into your agent." The agent reads the GitHub repo, writes its own configuration, and sets up a launch agent. This would have been "mind-blowing even a year ago."
- **Don't send me a PR with minor fixes**: "It takes me 10 times longer to review than to type 'fix' and wait a few minutes." The PR review paradigm is being deprecated.
- **"Close the loop" is the secret to making AI work**: AI is great at coding because you can validate code (compile it, run tests, check output). AI is mediocre at writing because there's no loop. Design your system so the AI can run the test.
- **PSPDFKit origin**: Started with a dating app he built on top of a scraped HTML API. Made $10k/month. App got killed by Apple. Pivoted to iOS PDF rendering SDK. Sold it after 13 years. The PSPDFKit code is on 1 billion devices.
- **Mentally more exhausting to juggle parallel agents**: Than to write code yourself — you're the architect coordinating multiple threads of execution simultaneously.

---

## Notable Quotes

> "I'm actually more interested in the prompts than the code. I ask people to please add the prompts. The prompt is a way higher signal of how they got to the solution than the actual output." — Peter Steinberger

> "Since the product was built by agents, it's structured exactly the way agents expect things to be named. They're really good at navigating their own product." — Peter Steinberger

> "Onboarding was literally: type this prompt into your agent. It would check out the GitHub repository, read the things, and write the configuration. I didn't have to work on onboarding because agents can do that for you now." — Peter Steinberger

> "The reason AI is so good at coding but often mediocre at writing is because you can validate code. The secret to making AI system development work well is to design your system to close the loop." — Interview host summary of Peter

---

## Connections

- Second primary source for [[wiki/entities/peter-steinberger]] and [[wiki/entities/openclaw]]
- Extends [[wiki/concepts/agentic-engineering]] — "read the prompt not the PR" is the most concrete practice from the Lex Fridman philosophical framing
- Extends [[wiki/concepts/soul-md]] — agents navigating agent-built code suggests agents understand their own context better than external reviewers do
- Related to [[wiki/entities/pspdfkit]] — origin story fills in the background on why Peter has the credibility to speak about building complex software systems

---

## Questions Raised

- What percentage of OpenClaw's production codebase has Peter personally read? Is there code running in production that no human has reviewed?
- What are the failure modes when agents navigate agent-built code? Are there classes of bugs that agents systematically miss because they match the training distribution?
- How does "prompt request" review actually work in practice — does Peter have a standard format for prompt PRs?
