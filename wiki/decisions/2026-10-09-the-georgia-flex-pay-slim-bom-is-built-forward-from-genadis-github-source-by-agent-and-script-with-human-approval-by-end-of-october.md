---
type: decision
title: The Georgia Flex Pay Slim BOM is built forward from Genadi's GitHub source — a flat parts list, the agent builds the BOM without the existing structure, a script checks the interfaces, a human approves, and it is pushed into MSBC; Val wants it by end of October
date: 2026-10-09
aliases: [Flex Pay Slim for Georgia BOM, Pay Slim first real test, flat parts list test, agent builds the BOM without the structure, MSBC is not the starting point, trust and verify, script validation of interfaces, human review and approval stage, trace report, highest assembly point, 30 consecutive BOMs, end of month BOM]
source-count: 2
status: active
open-commitments: 4
open-questions: 4
---

# The Georgia Flex Pay Slim BOM is built forward from Genadi's GitHub source (Oct 9 2026)

Agreed at the [[wiki/meetings/2026-10-09-github-msbc-agent-bom-assembly-and-pay-slim-first-test.md|Oct 9 2026 11:37 AM "GitHub-MSBC" meeting]] (English) by [[wiki/people/nathan-carver.md|Nathan Carver]] and [[wiki/people/genadi-peari.md|Genadi Peari]], with [[wiki/people/val-levitan.md|Val Levitan]] taking part mostly by Teams chat because his audio was choppy [[raw/Meeting_Notes_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]. Val's chat text is not in the transcript; only what Nathan and Genadi said about it is on record. It is the next step after Nathan's [[wiki/decisions/2026-10-05-nathan-carver-runs-the-flex-pay-slim-bom-reverse-spike-and-flex-port-follows.md|Oct-5 reverse spike]] and follows [[wiki/decisions/2026-10-08-msbc-stops-being-the-bom-source-and-the-week-of-october-12-goes-to-ordering-without-mikhail.md|Oct 8]]. The thread is sequenced on [[wiki/decisions/2026-09-23-the-bom-source-of-truth-is-the-latest-design-in-github-and-sync-runs-one-way.md]].

## What was decided

- **MSBC is not the starting point; GitHub is.** Reading Val's chat aloud, Nathan said "Engineering source of truth… Correct" and "Okay, so Val doesn't want Msbc as a starting point." Earlier: "So he wants, okay, so Github and Msbc have to be in sync." [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- **How the flow runs, as Genadi put it.** "Github provides the bill of material, you export it into Msbc and then look it there, and if there is a change, it exports another bill of material, new revision." The engineering sources are in GitHub, "the connection is by part number", and it is "very easy to pull it from the Github. By part number and revision." [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- **The test: a flat list, no structure given.** Genadi: "Can you take a flat structure, flat? Parts for one or even for this product. and try to build a bill of material without having the structure in front of, without giving him the structure, the existing structure, to see what they were coming up with." Nathan: "Let's do that, Genadi… I'll take the source that you have and use that as the starting point." [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- **The product: the Flex Pay Slim for Georgia.** Genadi chose "the current one, the the the pay slim": "this is the product we go into deploy soon and we actually need all this before that Val mentioned… Send it quotations and getting parts and everything." Nathan: "I'll take the Flex Pay slim for Georgia and start the process of… assembling a BOM. Running it through the… workflow." [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- **The workflow: agent, script check, human approval.** Nathan: the agent and a script generate a BOM, then "do some scripted validation to ensure that all the interfaces are correct. So at the end of that stream would be… a stage of human, human review and human approval." Humans also "review the instructions and update the instructions as needed to improve output." [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- **The source stays in GitHub whoever does the work.** Nathan: "the scripts don't need an agent to validate the BOM and they don't need an agent to push this up to Msbc. The agent is just there to… speed up some decision processes… the source would all stay in Github and get pushed up to Msbc regardless of… Who does that work?" [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- **When.** Nathan: "So I am out next week, but then that Val, you want this done. End of month, so I will… Jump on that when I'm back… following week." [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]] The notes set the due date as October 31 2026 and the start as the week of October 19 [[raw/Meeting_Notes_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]].

## Why

- **An agent BOM will never be fully right.** Genadi: "it might not never be perfect, right? It will be 90% correct… we basically need to keep the reference solid reference, which… is adjusted manually." Nathan: "I don't see that happening anytime soon for sure." Hence the check and the human stage [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]].
- **The Slim is needed for real.** It deploys soon in Georgia and needs quotes and parts (Genadi, above). See [[wiki/projects/georgia-market-rollout.md]].
- **What is downstream depends on a solid BOM.** Genadi: once a solid BOM exists, ordering "can be fully automated" — order 100 products, a part with two instances means an RFQ for 200, and a daily report of need against stock, what to order and lead time; "the source of everything is the bill of material." He called the five actions Val texted during the call "very important… a lot of saving might… bring to the company" and saw no reason "we won't have it tomorrow." Nathan agreed: "I think this is all reasonable," noting these work from an existing BOM, current inventory in BC and the BC supplier list [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]. The text of the five actions is not in the transcript [[raw/Meeting_Notes_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]].

## Genadi's doubts (still standing)

- **Building a BOM is not the slow part.** "the building bill of material is not a time-consuming part… Do the design like months or half a year, and then… you build the bill of material once. And then just maintain it." And: "The idea is not probably to save time." [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- **BOM levels follow production, not only contracts.** "that levels based not only on the contracts we have, it's also based on the how production is working… Because the logics between myself, the AI, and the production might be three different logics." A two-level BOM he was shown is "just for convenience treating of the procurement" — an assembly plus a PC board, so a revision change spreads to all products [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]].
- **He does not see the whole picture.** "I understand the idea of having the repositories and the contracts, it makes sense, but… I don't see the whole… how it…" Nathan, too: "I don't fully understand all of Val's vision, but I know the automation and the agenda part is important." [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]

## Variants (Genadi's point for the design)

Near-identical BOMs are made for different jurisdictions or customers, sometimes "the difference might be one item" — a cable, a different printer model, a particular bill acceptor. Each is a new top part number and a new BOM in MSBC, because "the production order has to see this, the difference." The difference "might come from the sales", not engineering. A final product has "like 5 different modules, one of them the kit for the money devices, one for the printer"; the final part numbers "might be… Six, 7, 10, at least." Nathan: in future a customer's change could be fed to the agent, which "automatically creates the new BOM"; Genadi: possible, but it needs "Human… Touch up… Verification" [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]].

## How it changes Oct 5 (evolution)

On Oct 5 the spike started from the existing BOM in MSBC, flattened it and rebuilt it ([[wiki/decisions/2026-10-05-nathan-carver-runs-the-flex-pay-slim-bom-reverse-spike-and-flex-port-follows.md]]). Nathan showed that reverse experiment on Oct 9. The next step runs the other way: from Genadi's GitHub source, with no existing structure shown to the agent. The product (Flex Pay Slim) and the doer (Nathan) stay the same. **Evolution, not contradiction** (inference from the two sources).

## Open commitments

- [ ] [[wiki/people/nathan-carver.md|Nathan Carver]] — build the Flex Pay Slim (Georgia) BOM from Genadi's GitHub source with the agent and script workflow, and push it to MSBC; keep Val's chat requirements for the "CO" agent in mind — due end of October 2026 (the notes: October 31; he is out the week after Oct 9) — [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]] [[raw/Meeting_Notes_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — send Nathan the GitHub link for the Pay Slim ("I'll show you in Github… I'll send the link") — due unspecified — [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- [ ] Nathan Carver — find a file a human can review efficiently for BOM approval, maybe "a CSV… that Excel can open" — due unspecified — [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- [ ] Nathan Carver — set up time with Genadi on reshuffling the repositories, as needed ("I'll set up time for us to discuss… as needed") — due unspecified — [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]

## Open questions

- How is the agent's output verified without taking more time than doing it by hand? Nathan: "how do we verify the output?… in a way that doesn't take you more time than what you're doing now"; Genadi: "I it definitely will." Nathan's ideas: a script check in a loop, an audit agent on a different model ("Claude build it and Grok or Astra audits it"), and confidence after "30 consecutive bombs that need no corrections" — [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- How do humans review near-identical BOM variants that differ by one part? Nathan: it may "come down to what tools do we use"; Genadi: "Yes" — [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- How should multi-level BOMs follow production's sub-assembly logic? Raised by Genadi; not answered — [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- What were Val's five chat actions and his requirements for the "CO" agent? Not in the transcript — [[raw/Meeting_Notes_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]

**§15.8:** clear — no pay, rate or hours. **§15 #9:** clear — no part number or identifier is spoken.

## Sources
- [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- [[raw/Meeting_Notes_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
