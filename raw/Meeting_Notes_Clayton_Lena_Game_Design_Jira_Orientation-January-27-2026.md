# Meeting Summary — Clayton Chancey / Lena Zhukova: game design workflow and Jira automation orientation

**Date:** January 27, 2026, 9:58 AM Eastern
**Duration:** approximately 56 minutes of content (80-minute recording; slow start waiting for Lena)
**Attendees:** Val Levitan, Clayton Chancey, Lena Zhukova (director of game design), Aaron Bockelie (joins mid-meeting). First of the two orientation meetings agreed on January 23.
**Raw transcript:** [[Meeting_Transcript_Clayton_Lena_Game_Design_Jira_Orientation-January-27-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "Clayton-Aaron-JVL", 10:00–11:00 AM ET, organiser Clayton Chancey. Clayton and Lena both named in the transcript; confirmed on both keys.

## Summary

The working orientation for Clayton's engagement: Val and Lena walked him through how game design actually runs, and the meeting ended with the first concrete build direction.

**The pipeline.** Game design is three baskets — game concept, game design, game production — run as a conveyor. Concept is mainly the product manager (Juan) and producer (Michael); Lena is present but contributes little there. From design down, "Lena is mainly running the show and pushing the production." Her team of designers sits mainly in Europe (Portugal, Poland); she reports to the producer. Jira layering: initiative → product → features and stories; a feature signifies a feature branch in GitHub, and "if a feature does not produce an artifact, it's probably not a feature." The roadmap's ~five months of dates are cumulative workload per basket, not one linear schedule: about five months of concepts, under a month of design, four to six months of production, each basket's outputs "put on a shelf" until pulled. Lena added the two product cycles: new complex games (multiple bonuses) can be ~5 months, while market adaptations of existing games are a different, faster cycle that varies with complexity (same theme/symbols, different math/bonus/orientation).

**History and where Jira stands.** For ten years Jira/Confluence were "a central notepad repository… not to forget to do things"; about five years ago JVL deleted 80,000 tasks, halved the workforce, and removed the CTO and CFO. Today Jira is productive but "quite bureaucratic — a process that sucks life out of us… if we lost Jira today, the company would not go down." Clayton asked the key question — is it accurate? Lena: "not bad, we're trying to keep it up to date"; Val agreed ("does it show truth? It does… not bad at all") and noted Jira has become the unification tool that makes running meetings easier. Confluence is judged polluted; the decision — final, not for re-discussion — is to move artifacts from Confluence to GitHub.

**The legacy swamp: Rage Studio.** JVL's own engine/framework, born when an in-house graphics-engine department could no longer compete. On a consultant's advice the framework moved under HTML: design happens in Unity, then a homemade translator distils it into the free 2D Pixi engine (Unity itself was too bulky and expensive to license). Val's verdict: "the judgment is still out there." Rage Studio sits on SVN and Jenkins, is pinned to 3ds Max 11 — no longer supported by Autodesk, with no team to upgrade Rage to newer versions — so the art chain runs on unsupported software (Lena's risk flag). Lena's "prime bureaucratic swamp" is Rage Studio, and Val estimates she loses 20–40% of productive time to bureaucracy.

**The transition to Omni.** Markets (e.g. South Dakota) still demand Rage Studio product, so JVL does "the very minimum the market can tolerate" there while shifting to Omni — new framework, internal database, and new FP7 hardware replacing the AMD V1000 processor. The industry's technical-lab approval process gates the move: Omni lab submission scheduled for March, expected through by June. Val's target: at least three more games in approved Omni on FP7 hardware placed in locations by year-end — "a tall order" while designers still feed the must-maintain Rage markets.

**Silos.** Beyond the three design baskets: core technology/hardware runs under an entirely different set of people, QA is its own barely-communicating silo, and nothing unites them except Val trying "to be vertically responsible for everything" while, by his own account, not an engineer, not a designer, and short on time.

**Lena's actual pain.** Not decomposition per se but volume: per game a deliverables list, milestones treated as features, stories kept to roughly two days each — "the amount of issues you need to enter, and the descriptions, story by story." Her two "art managers" are really senior game artists doing Jira entry relief without managerial roles or appetite (Val: "it's like getting the teeth out"). Clayton asked to see exactly what those two do — inputs and outputs — as a target. Lena has tried AI (Cline a couple of days earlier): it asks endless questions, needs constant rechecking, and "he's trying to fix our help because he thinks it's better — but we are saying it because there are regulations on our market." Aaron's counter: her impressions predate the last ~10 months of tool change. Val's additions: JVL people are poor prompters, ESL prompting makes it worse — he encourages prompting in the mother tongue, but Europeans practice English instead; artists mostly use ChatGPT for art references and concepts, and Aaron wants designers moved to graphics-specific AI tools.

**Val's own method (stated as the model).** He records meetings, squeezes explanations out of developers ("explain it to me, break it down"), then drops the transcript into Claude — 15 minutes and a few prompts open the tasks and features. His caveat: as a non-engineer his errors propagate; an engineer doing the same would get clean results. Lena has no Claude Desktop/MCP yet.

**Clayton's plan — the opinionated MCP.** His case study: for another client he built a custom, opinionated Atlassian MCP in ~10 hours (each tool call wraps 5–20 API calls plus embedded prompts encoding house semantics — "when the user says release, look up fixed version"), then one-shot a two-hour meeting transcript into **340 organised Jira tickets**, saving perhaps 60 hours. Plan for JVL: fork that foundation (he'll MIT-license it), get access (Dima's email arrived during the call), study how design actually uses Jira, and bring a read-only prototype to the Thursday meeting for Lena to judge right/wrong as the feedback loop. Goal within one–two weeks: the tool does ~75% of what the art managers do. Aaron is separately building the developer-side Jira MCP; they agreed the answer is multiple focused role-based MCP servers, not one-size-fits-all (a TypeScript directory/tool-search pattern was floated for later design sessions). Aaron's efficiency warning: the official Atlassian MCP burned a quarter of a context window on one call — custom tools must stay lean. Clayton also noted the recursive loop: he transcribes these meetings into his own Claude project to populate his Jira backlog about populating JVL's.

**Closing.** Val gave Clayton a direct line to Lena ("my main objective is to make your life personally easier — unload the bureaucracy on automation"), asked Clayton to get onto JVL Microsoft/Outlook (onboarding today/tomorrow), and told Lena the compliment straight: "Clayton is really hired because of you, for you." Clayton's synthesis of the real problem: generation is easy now, judgment is the cost — "the goal is to bake the judgment work into the tool so you do it once and can trust the generation."

## Decisions Made

- **Build direction approved: a custom, opinionated, role-scoped Jira MCP for game design**, read-only prototype by Thursday's meeting, Lena as the expert judge. (Val: "That's a great direction. I really like it.")
- **Multiple focused MCP servers by role** (design vs developer), coordinated by Clayton and Aaron, rather than one generic server. (Clayton, Aaron)
- **Confluence → GitHub artifact migration is final** — "it's a decision; we're not discussing it anymore." (Val, restating)
- **Omni schedule of record:** lab submission March, approval expected by June, ≥3 Omni/FP7 games in locations by year-end. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Clayton Chancey | Fork/license the MCP foundation, explore JVL Jira, bring a read-only prototype | Thursday's meeting (Jan 29) | High | Access email from Dima received during the call |
| 2 | Clayton Chancey | Complete JVL Microsoft/Outlook onboarding | Today/tomorrow morning | High | Val asked to move onto Microsoft tooling |
| 3 | Clayton Chancey | Email back to secure Atlassian access as well | Immediately | High | Had GitHub and Outlook; Atlassian pending |
| 4 | Lena Zhukova | Join the Thursday meeting and judge the prototype's answers | Jan 29 | High | The expert feedback loop |
| 5 | Clayton + Aaron | Coordinate role-based MCP designs (design vs developer hierarchies) in their design session | This week | Normal | Including tool-search/one-server-many-roles question |
| 6 | Clayton Chancey | Study the two art managers' actual inputs/outputs in Jira | This week | High | Target: automate ~75% of that work |

## Open Questions

- Whether Rage Studio gets any automation investment at all, given all momentum points to Omni ("I don't know how much effort you want to put on Rage Studio").
- Whether Lena's 20–40% bureaucracy share is closer to 20 or to 40 — Val explicitly does not know.
- One JVL MCP server with baked-in roles vs several separate ones (parked for the design session).

## Possible mis-transcriptions (not in glossary — confirm before fixing)

- "home park" (00:09:16) — garbled; context suggests "artwork" or similar.
- "Yanami" (00:21:19) — likely **Lena**; "Darian" (00:26:51) — likely **there and**; "Leona/Lianna/Elena/Leonard" — all **Lena** variants.
- "Citi on the side" (00:23:45) — likely **CD/DB on the side** (internal database reference, garbled).
- "spline / Klein / Klein's" (00:40:09, 00:42:15) — **Cline** (the coding agent Lena tried).
- "Robo" (00:44:13) — likely **Rovo** (Atlassian's AI).
- "Elastique / ElastiNMT / Elastic MCP" (00:51:09, 00:51:28) — **Atlassian** MCP variants, garbled.
- "3D Max" — **3ds Max** (Lena's own line has it right).
- "FP seven" / "AMD V ten hundred" — **FP7** processor, **AMD V1000**.

## Dispatch Log

---
*Processed from Plaud recording on September 24, 2026 (backlog batch 1)*
*Source recording: 01-27 Strategic Review of Development Workflows and AI-Driven Automation Proposal (Plaud)*
