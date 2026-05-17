# Wiki Activity Log

> Append-only. Never edit past entries.
> Format: `## [YYYY-MM-DD] operation | Description`
> Grep tip: `grep "^## \[" wiki/log.md | tail -10`

---

## [2026-04-18] init | Wiki initialized

Scaffold created. Directory structure, CLAUDE.md schema, index, log, and overview seed files written.
Pages created: `wiki/index.md`, `wiki/log.md`, `wiki/overview.md`.

---

## [2026-04-18] ingest | OpenClaw: The Viral AI Agent that Broke the Internet — Lex Fridman Podcast #491

Source: `raw/articles/Transcript for OpenClaw The Viral AI Agent that Broke the Internet - Peter Steinberger  Lex Fridman Podcast 491.md`

Pages created (13 total):
- `wiki/sources/openclaw-lex-fridman-491.md`
- `wiki/entities/peter-steinberger.md`
- `wiki/entities/openclaw.md`
- `wiki/entities/moltbook.md`
- `wiki/entities/pspdfkit.md`
- `wiki/concepts/agentic-engineering.md`
- `wiki/concepts/agentic-loop.md`
- `wiki/concepts/mcps-vs-skills.md`
- `wiki/concepts/personal-agents.md`
- `wiki/concepts/ai-psychosis.md`
- `wiki/concepts/soul-md.md`
- `wiki/concepts/prompt-injection.md`

Pages updated: `wiki/index.md`, `wiki/log.md`, `wiki/overview.md`

Notable: No contradictions found (first source). Open questions logged on soul.md identity/continuity, MCP vs CLI debate, and acquisition outcome.

---

## [2026-05-17] edit | Removed off-topic entries (apparel-exports-india, capex-cycle-analysis)

Deleted `wiki/concepts/apparel-exports-india.md` and `wiki/concepts/capex-cycle-analysis.md` as not relevant to this AI knowledge map. Updated `wiki/index.md` to remove their entries.

---

## [2026-04-24] ingest | The Supply and Demand of AI Tokens — Dylan Patel Interview (Invest Like The Best)

Source: `raw/The Supply and Demand of AI Tokens  Dylan Patel Interview.md`

Pages created (9 total):
- `wiki/sources/dylan-patel-token-supply-demand.md`
- `wiki/entities/dylan-patel.md`
- `wiki/entities/semianalysis.md`
- `wiki/entities/anthropic.md`
- `wiki/concepts/tokenomics.md`
- `wiki/concepts/ai-permanent-underclass.md`
- `wiki/concepts/phantom-gdp.md`
- `wiki/concepts/scaling-laws.md`

Pages updated: `wiki/concepts/ai-psychosis.md` (added Claude Code psychosis variant), `wiki/overview.md`, `wiki/index.md`, `wiki/log.md`

Key findings: Token demand is use-case driven, not price-driven — frontier models unlock qualitatively new tasks each generation. Every supply layer (GPU, DRAM, TSMC, ASML, copper foil) is sold out with expanding margins. Mythos (internally held, L6 engineer equivalent) proves scaling laws still hold. SemiAnalysis ($7M/yr Anthropic spend, >25% of salaries) is a live case study of AI adoption economics. New concepts: tokenomics, phantom GDP (invisible AI-created value), AI permanent underclass (token arbitrage stratification), scaling laws. Mythos model hoarding by elite banks flagged as emerging structural moat. Prediction: large-scale AI protests within 3 months.

---

## [2026-04-25] ingest | Dario Amodei — We are near the end of the exponential (Dwarkesh Patel)

Source: `raw/podcasts/Dario Amodei — We are near the end of the exponential.md`

Pages created (3 total):
- `wiki/sources/dario-amodei-end-of-exponential.md`
- `wiki/entities/dario-amodei.md`
- `wiki/concepts/biological-revolution.md`
- `wiki/concepts/ai-diffusion.md`

Pages updated: `wiki/entities/anthropic.md` (added source appearances), `wiki/overview.md`, `wiki/index.md`, `wiki/log.md`

Key findings: Dario's most comprehensive public statement. Core thesis: 1–2 years until AI is a peer-level cognitive worker. Biological revolution = AI compressing decades of biomedical progress into years. LLM path is more optimistic than competitive-agent AGI path (chain-of-thought interpretability is the key). Diffusion is real but AI diffuses faster than any prior tech. Anthropic revenue: $0→$100M (2023) → $1B→$9B (2025) → adding billions/month in 2026. ~40% of Dario's time on culture (DVQ, biweekly all-hands, radical internal honesty). Key worry: most consequential decisions may be made in passing.

---

## [2026-04-25] ingest | The OpenAI Founders On Their Plan To Battle Elon, Compute And Everything Else (Core Memory)

Source: `raw/podcasts/The OpenAI Founders On Their Plan To Battle Elon, Compute And Everything Else.md`

Pages created (4 total):
- `wiki/sources/openai-founders-core-memory.md`
- `wiki/entities/sam-altman.md`
- `wiki/entities/greg-brockman.md`
- `wiki/entities/openai.md`

Pages updated: `wiki/concepts/personal-agents.md` (cross-industry convergence table), `wiki/overview.md`, `wiki/index.md`, `wiki/log.md`

Key findings: ChatGPT succeeded because people could *feel* it — the "feel it to believe it" mechanism is the key to mass AI adoption. Sam's personal AGI vision ("the model that knows everything about you") is convergent with Peter Steinberger's OpenClaw and Sundar's Search-as-agent-manager. Elon Musk breaking point: demand for absolute control, not just equity. In 2017–2018, the plan was competitive-agent simulation — LLM path discovered to be more optimistic. Greg: "Too much opportunity" is OpenAI's biggest technical challenge.

---

## [2026-04-25] ingest | The History and Future of AI at Google, with Sundar Pichai (Elad Gil + Patrick Collison)

Source: `raw/podcasts/The history and future of AI at Google, with Sundar Pichai.md`

Pages created (2 total):
- `wiki/sources/sundar-pichai-google-ai-history.md`
- `wiki/entities/sundar-pichai.md`
- `wiki/entities/google.md`

Pages updated: `wiki/concepts/personal-agents.md` (convergence table), `wiki/overview.md`, `wiki/index.md`, `wiki/log.md`

Key findings: Search will become an agent manager (long-running, async, task-completing). Google's latency philosophy is extreme (millisecond-level sub-team budgets). Gemini Flash = ~90% of Pro capability at dramatically lower latency via TPU vertical integration. 2027 as inflection year for non-engineering enterprise AI workflows. Patrick Collison taxonomy of enterprise diffusion barriers: prompting skill, code blast radius, identity/access permissions, role redefinition, security. Sundar: "Not zero-sum — value curve is also on a crazy trajectory." Small exciting bets: data centers in space; post-training ML improvement Sundar saw personally.


---

## [2026-04-25] ingest | Andrej Karpathy — We're summoning ghosts, not building animals (Dwarkesh Patel)

Source: `raw/podcasts/Andrej Karpathy — We're summoning ghosts, not building animals.md`

Pages created: `wiki/sources/andrej-karpathy-summoning-ghosts.md`, `wiki/entities/andrej-karpathy.md`, `wiki/concepts/llm-nature.md`

Key findings: LLMs are distillations of human writing — summoning ghosts, not building animals. Three coding modes: scratch / autocomplete-assisted / vibe-coding (agents). Agents good for boilerplate, bad for intellectually novel code. LLM cognitive deficits: no persistent memory, poor metacognition, context window blindness, plausibility-optimised not truth-optimised. Education philosophy: knowledge as a ramp with motivated dependencies; "if I can't build it, I don't understand it." Research taste: beauty, simplicity, brain-inspired aesthetic as top-down prior.

---

## [2026-04-25] ingest | Dylan Patel — The Single Biggest Bottleneck to Scaling AI Compute (Dwarkesh Patel)

Source: `raw/podcasts/Dylan Patel — The single biggest bottleneck to scaling AI compute.md`

Pages created: `wiki/sources/dylan-patel-compute-bottleneck.md`

Key findings: Energy is 1-year bottleneck (chip output exceeds ability to turn chips on by end of 2025). Chips are 3–4-year bottleneck. Huawei is most underrated threat — has all legs except TSMC. China export controls were a policy mistake that accelerated Chinese independence. Taiwan risk is severe (EUV tools use chips made in Taiwan — snake eating tail). Robot intelligence will be centralised in cloud, not on-device. Elon's Samsung deal for robot chips = geopolitical diversification.

---

## [2026-04-25] ingest | Elon Musk — In 36 months, the cheapest place to put AI will be space (Dwarkesh Patel)

Source: `raw/podcasts/Elon Musk — In 36 months, the cheapest place to put AI will be space.md`

Pages created: `wiki/sources/elon-musk-ai-space.md`, `wiki/entities/elon-musk.md`

Key findings: Ideas travel between labs in ~6 months → hardware scaling speed is the key differentiator. xAI wins by turning on chips fastest. Space compute: solar unlimited, radiation-tolerant nets, run hotter to halve radiator mass. TeraFab targeting 1M wafers/month by 2030 (logic + memory + packaging). Energy bottleneck consistent with Dylan — by end of 2025, chip output exceeds power to run them. Optimism as a disposition philosophy.

---

## [2026-04-25] ingest | Ilya Sutskever — We're moving from the age of scaling to the age of research (Dwarkesh Patel)

Source: `raw/podcasts/Ilya Sutskever — We're moving from the age of scaling to the age of research.md`

Pages created: `wiki/sources/ilya-sutskever-age-of-research.md`, `wiki/entities/ilya-sutskever.md`, `wiki/concepts/post-scaling-research.md`

Key findings: Age of scaling (internet data) is ending. Age of research is beginning — algorithmic insight becomes the scarce resource. Continual learning agents (human-like incremental learning) is key frontier. AI diversity problem: all pre-trained LLMs are similar because trained on same corpus; differentiation only starts with post-training/RL. Self-play found modern form: prover-verifier, LLM-as-judge. Research taste = aesthetic + brain-inspired intuition + top-down conviction. Critical tension with Dario: compute scaling still works but data scaling has hit a wall.

---

## [2026-04-25] ingest | Jensen Huang — Will Nvidia's Moat Persist? (Dwarkesh Patel)

Source: `raw/podcasts/Jensen Huang — Will Nvidia's moat persist?.md`

Pages created: `wiki/sources/jensen-huang-nvidia-moat.md`, `wiki/entities/jensen-huang.md`, `wiki/entities/nvidia.md`

Key findings: Nvidia's moat is architectural + CUDA ecosystem, not node-based (all alternatives simulated and provably worse). Networking is critical (why Mellanox). China export controls were a policy mistake — accelerated Chinese chip independence; Huawei has all Nvidia's legs except TSMC. Premium-latency token market is emerging — Groq acquisition enables this segment. Without AI, Nvidia would still be large via accelerated computing (molecular dynamics, seismic, graphics).

---

## [2026-04-25] ingest | Satya Nadella — How Microsoft Thinks About AGI (Dwarkesh Patel)

Source: `raw/podcasts/Satya Nadella — How Microsoft thinks about AGI.md`

Pages created: `wiki/sources/satya-nadella-microsoft-agi.md`, `wiki/entities/satya-nadella.md`, `wiki/concepts/ai-sovereignty.md`

Key findings: Trust — not model capability — may be the decisive variable in global AI race. Countries need to trust provider will be there in 10 years. Sovereignty is a first-class engineering + policy requirement (Microsoft sovereign clouds in France/Germany). Open source is structural check against concentration. TSMC Arizona is "not real sovereignty." Bipolar US-China world requires respecting each country's sovereignty demands as business requirement. Enterprise diffusion 2027 (consistent with Sundar).

---

## [2026-04-25] ingest | Earn Crores with AI Business Ideas — Vaibhav & Raj Shamani FO499 (Hindi podcast)

Source: `raw/podcasts/Earn Crores with AI Business Ideas, Claude, Free Tools & Prompts  Vaibhav  FO499 Raj Shamani.md`

Pages created: `wiki/sources/vaibhav-raj-shamani-ai-business.md`

Key findings: Hindi-language podcast; Indian solopreneur/SMB AI audience. SOP-as-resume thesis: future hiring will look at your markdown skill files, not CVs. "Your experience is the markdown files." Claude is recommended tool. Two-year window of asymmetric advantage for early AI adopters. Next episode planned on which jobs get automated. Connects to soul.md and agentic-engineering from Indian market perspective.

---

## [2026-04-25] ingest | Leopold Aschenbrenner — 2027 AGI, China/US Superintelligence Race (Dwarkesh Patel)

Source: `raw/podcasts/Leopold Aschenbrenner — 2027 AGI, ChinaUS super-intelligence race, & the return of history.md`

Pages created: `wiki/sources/leopold-aschenbrenner-2027-agi.md`, `wiki/entities/leopold-aschenbrenner.md`, `wiki/concepts/agi-timeline.md`

Key findings: 2027 AGI → intelligence explosion shortly after. National security is the correct frame, not product. Manhattan Project analogy: secrecy of next paradigm could yield 2+ year lead. Compute clusters must stay in US and allied democracies — authoritarian regimes can seize or exfiltrate. The dangerous scenario is a close race (3-month lead → feverish, unstable, maximum risk); the safe scenario is a 2-year lead (wiggle room for safety). "This is the quiet period. Soon it will be AGI." 100 GW in the US is physically possible via natural gas.

---

## [2026-04-25] ingest | Marc Andreessen — The Real AI Boom Hasn't Even Started Yet

Source: `raw/podcasts/Marc Andreessen The real AI boom hasn't even started yet.md`

Pages created: `wiki/sources/marc-andreessen-real-ai-boom.md`, `wiki/entities/marc-andreessen.md`

Key findings: Both AI utopians and doomers are too optimistic about the *speed* of change — they assume technology making something possible = people changing behaviour. 35% of the US economy is in professional licensing cartels. K-12 is a government monopoly with teachers 100% opposed to AI. Dock workers won their strike — commitment to no additional automation. Entire government agencies have 1 office day/month locked into COVID-era CBAs. The real economy is "wired in." Founder + AI superpower is the winning formula (new Henry Ford). Elon method is the best-performing organisational model we've ever seen.

---

## [2026-04-25] ingest | Marc Andreessen — Pi + OpenClaw, Death of the Browser, AI+Crypto Grand Unification

Source: `raw/podcasts/Marc Andreessen introspects on Death of the Browser, Pi + OpenClaw, and Why "This Time Is Different".md`

Pages created: `wiki/sources/marc-andreessen-openclaw-agents.md`

Pages updated: `wiki/entities/marc-andreessen.md`, `wiki/entities/openclaw.md` (referenced), `wiki/concepts/personal-agents.md` (agent bank accounts as next milestone)

Key findings: Marc's most advanced OpenClaw users have already given agents bank accounts + credit cards. AI agents need money — AI+crypto/stablecoins is the grand unification. HTTP 402 (payment required) was the missing internet primitive. Browser is dying as an abstraction (built for human limitations; those limitations are disappearing). Find the people running Codex with skip permissions — that's the future. Sam Altman runs Codex with skip permissions on his laptop.

---

## [2026-04-25] ingest | Peter Steinberger — "I Ship Code I Don't Read" (second interview / Clawd creator)

Source: `raw/podcasts/The creator of Clawd "I ship code I don't read".md`

Pages created: `wiki/sources/peter-steinberger-clawd-ships-code.md`

Pages updated: `wiki/entities/peter-steinberger.md` (second source appearance)

Key findings: Peter reads prompts, not pull requests. The prompt is higher-signal than the code output. Agents navigate agent-built code better than humans because it's structured the way models expect. Agentic onboarding replaced manual onboarding — "type this prompt into your agent." PRs for minor fixes rejected — type "fix" and wait 2 minutes. Close-the-loop principle: AI is great at coding because you can validate via tests; AI is mediocre at writing because there's no validation loop. Mentally more exhausting to coordinate parallel agents than to write code. PSPDFKit origin story: dating app, Apple killed it, PDF SDK, 1 billion devices.

---

## [2026-04-25] ingest | Dylan Patel — Inside the Trillion-Dollar AI Buildout

Source: `raw/podcasts/Inside the Trillion-Dollar AI Buildout  Dylan Patel Interview.md`

Pages created: `wiki/sources/dylan-patel-trillion-dollar-buildout.md`

Pages updated: `wiki/entities/dylan-patel.md` (third source appearance)

Key findings: Text pre-training late innings (not done — better architecture still yields gains). Multimodal pre-training mid innings (video/audio too expensive to scale until now). RL/environment post-training first ball thrown. Environments are the hard engineering problem now. Embodiment may be required for physical intuition AGI. SaaS business model disrupted: AI drops cost of competing software stacks to near-zero; COGS goes up for AI-native features; many SaaS companies will be disrupted unless they have long data half-life (ERP, CRM records) vs. short half-life (Slack messages, Zendesk seats).

---

## [2026-04-25] ingest | Lex Fridman #490 — State of AI in 2026

Source: `raw/podcasts/State of AI in 2026 LLMs, Coding, Scaling Laws, China, Agents, GPUs, AGI  Lex Fridman Podcast 490.md`

Pages created: `wiki/sources/lex-fridman-state-of-ai-2026.md`

Key findings: AI slop coming and will worsen before it gets better. Authenticity premium for in-person and verified human content. Trust-based provenance is the solution. Three coding modes confirmed as practitioner consensus. Consciousness is the big mystery AI puts a mirror to. Humans retain agency in current AI implementation. AI is a tool you direct.

---

## [2026-04-25] ingest | Jensen Huang — Lex Fridman #494 / $4 Trillion Nvidia

Source: `raw/podcasts/Jensen Huang NVIDIA - The $4 Trillion Company & the AI Revolution  Lex Fridman Podcast 494.md`

Pages created: `wiki/sources/jensen-huang-lex-fridman-494.md`

Pages updated: `wiki/entities/jensen-huang.md` (second source), `wiki/concepts/biological-revolution.md` (Jensen's 5yr timeline added)

Key findings: Understanding the biological machine in ~5 years (aligns with and extends Dario's biological revolution thesis). Succession planning misconception — correct answer is continuous knowledge transfer in every meeting. Humanity optimism: end of disease, pollution reduction, speed-of-light travel. Consciousness upload vision: Jensen's personal death plan — upload everything he's said and written into an AI, send it on a humanoid spaceship.

---

## [2026-04-25] ingest | GLP-1s, Peptides, and The Trillion-Dollar Health Revolution

Source: `raw/podcasts/GLP-1s, Peptides, and The Trillion-Dollar Health Revolution.md`

Pages created: `wiki/sources/glp1-health-revolution.md`

Key findings: GLP-1s are the leading pre-AI biological revolution example. 20%+ reduction in cardiovascular events independent of weight loss — implies structural mechanism beyond caloric intake. Addiction treatment (alcohol, gambling, drugs) is an independent benefit via brain satiety axis. Three barriers to adoption: complexity, cost, convenience. "It takes months to protect myself from a heart attack but one click to get toothpaste." Seat-based chronic care pricing is broken. BMI 40+ is the underserved population. Validates Marc Andreessen's healthcare cartel thesis.

---

## [2026-04-25] skipped | Joe Rogan + Elon Musk (episodes 1169, 2054, 2281, 2404)

Reason: Very long, low signal density relative to Elon's dedicated Dwarkesh interview ([[wiki/sources/elon-musk-ai-space]]). No new thesis-level claims observed. Can be ingested on demand.

## [2026-04-25] skipped | Joe Rogan + Palmer Luckey (#2394)

Reason: Defense AI is a peripheral domain for this wiki. Can be ingested if defense AI becomes a focus area.

## [2026-04-25] skipped | Karan Bhagat — 99% Rich People Do This (Raj Shamani FO431)

Reason: Hindi-language wealth management; different domain from AI/tech focus. No AI-relevant content in sampled section.

## [2026-04-25] skipped | Elon Musk — Lex Fridman #400

Reason: Older interview; claims covered in the dedicated Dwarkesh space compute interview. Lower priority unless a specific claim needs verification.

## [2026-04-25] skipped | From SpaceX to Founders Fund to Solving Nuclear Fuel Problem

Reason: Nuclear energy is relevant to the compute energy bottleneck but peripheral. Sampled content focused on venture strategy. Can revisit if nuclear energy becomes a wiki focus.

## [2026-04-25] skipped | He Built Revenue Engines for Google, Facebook & Square

Reason: B2B revenue growth — peripheral to core AI wiki domains.

## [2026-04-25] skipped | Why Now Is the Best Time to Buy Public Software Companies

Reason: Public software investing. Partially useful (SaaS disruption thesis) but covered in Dylan Patel trillion-dollar buildout source.

## [2026-04-25] skipped | Gavin Baker — GPUs, TPUs & Economics of AI

Reason: Sampled content drifted into investor origin story; AI economics claims appear covered by Dylan Patel. Can revisit.

---

## [2026-05-17] ingest | Batch ingest: 5 podcast sources (Palmer Luckey, Marc Andreessen World Malleable, Gavin Baker GPU Economics, Elon Musk Lex Fridman 400, Gokul Rajaram Revenue Engines)

Sources ingested:
- `raw/podcasts/Joe Rogan Experience 2394 - Palmer Luckey.md` → `wiki/sources/palmer-luckey-jre-2394.md`
- `raw/podcasts/Marc Andreessen The World Is More Malleable Than You Think.md` → `wiki/sources/marc-andreessen-world-malleable.md`
- `raw/podcasts/GPUs, TPUs, & The Economics of AI Explained  Gavin Baker Interview.md` → `wiki/sources/gavin-baker-gpu-economics.md`
- `raw/podcasts/Elon Musk War, AI, Aliens, Politics, Physics, Video Games, and Humanity  Lex Fridman Podcast 400.md` → `wiki/sources/elon-musk-lex-fridman-400.md`
- `raw/podcasts/He Built The Revenue Engines for Google, Facebook & Square.md` → `wiki/sources/gokul-rajaram-ai-product-development.md`

Pages created (11 total):
- `wiki/sources/palmer-luckey-jre-2394.md`
- `wiki/sources/marc-andreessen-world-malleable.md`
- `wiki/sources/gavin-baker-gpu-economics.md`
- `wiki/sources/elon-musk-lex-fridman-400.md`
- `wiki/sources/gokul-rajaram-ai-product-development.md`
- `wiki/entities/palmer-luckey.md`
- `wiki/entities/gavin-baker.md`
- `wiki/entities/gokul-rajaram.md`
- `wiki/concepts/non-deterministic-software.md`

Pages updated:
- `wiki/entities/elon-musk.md` (added Lex Fridman 400 and Gavin Baker appearances)
- `wiki/entities/marc-andreessen.md` (replaced placeholder marc-andreessen-malleable-world reference with actual ingested source)
- `wiki/concepts/scaling-laws.md` (added two new post-training scaling laws from Gavin Baker)
- `wiki/index.md` (added 5 sources, 3 entities, 1 concept rows)
- `wiki/log.md` (this entry)

Skipped (7 files):
- JRE 1169 Elon Musk — empty transcript
- JRE 2054 Elon Musk — Cybertruck/manufacturing, no AI content
- JRE 2281 Elon Musk — DOGE/politics, superficial Grok mention
- JRE 2404 Elon Musk — no AI content
- Nuclear Fuel Problem (Scott Nolan/General Matter) — nuclear energy only, insufficient AI content
- Why Now is the Best Time to Buy Public Software Companies — investment methodology, AI content covered by existing Dylan Patel sources
- 99% Rich People Do This (Karan Bhagat) — instructed skip

Key findings:
- Gavin Baker provides the most precise investor-grade account of the reasoning-model breakthrough: ARC-AGI 8%→95% in 3 months, reasoning "saved AI" through the Blackwell gap
- Gokul Rajaram introduces "non-deterministic software" as a new structural concept — the most useful new framework from this batch
- Palmer Luckey's defense AI perspective shows AI already operationally deployed in autonomous weapons — not future speculation
- Marc Andreessen's "World Malleable" fills in the historical/philosophical foundation for the founder+AI formula already documented in prior sources
- Elon Lex 400 primarily valuable for AGI-as-civilisational-risk framing, reinforcing Leopold Aschenbrenner's arguments from a different angle
