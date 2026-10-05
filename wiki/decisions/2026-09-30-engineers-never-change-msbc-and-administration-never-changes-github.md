---
type: decision
title: Engineers never change anything in MSBC and administration never changes anything in GitHub — a "non-penetrable border", crossed only by a tool that carries flat revisions one way
date: 2026-09-30
aliases: [non-penetrable border, engineering territory and administrative territory, engineers are never allowed to change anything in MSBC, the administrator is never allowed to change anything in GitHub, under the key and lock, the transcriber, a tool that looks after the revisions all the time, hourly or by minute, supplier data lives in MSBC, engineering files live in GitHub, clear separation between engineering and administration]
source-count: 3
status: active
open-commitments: 0
open-questions: 1
---

# Engineers never change MSBC; administration never changes GitHub (Sept 30 2026)

Set by [[wiki/people/val-levitan.md|Val Levitan]] at the opening of the [[wiki/meetings/2026-09-30-github-to-msbc-bom-flat-list-bridge.md|Sept-30 GitHub-to-MSBC meeting]] (English) with [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/nathan-carver.md|Nathan Carver]] and [[wiki/people/lev-rudky.md|Lev Rudky]]. Quotations from [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]. It sharpens the Sept-24 rule on [[wiki/decisions/2026-09-23-the-bom-source-of-truth-is-the-latest-design-in-github-and-sync-runs-one-way.md]] ("Business Central holds a copy… plus everything commercial; data flows one way") into a rule about *who may touch which system*.

## What was decided

- **Where each kind of data lives.** "The supplier. Information. financial information, banking information, address, contact information for the supplier, active supplier. He is located and updated inside of the Msbc. The engineering. Files. Drawings, specs, live. And update it in Github" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- **The border.** "There is a clear separation between engineering territory and administrative territory. Engineers are never allowed. To change anything in Msbc. The administrator is never allowed to change anything in Github." Genadi: "And should we command this?" Val: "Yes, of course" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- **Restated later with the lock-and-key image.** "all the financial information to this particular or to these vendors are isolated. You never know that financial information. You have no effect on that financial information. Just like administration has no effect on what drawings are included in there. There is a clear separation, clear border, non-penetrable border, between engineering and administration, and they're located under the key and lock. Nobody has right to go in either side." Genadi: "Understood" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- **The only thing that crosses is a tool.** "We need a transcriber. We need a tool that looks after the revisions all the time, flat revisions, Whatever you substitute, whatever you said changes, and it's constant. It could be hourly, it could be by minute, I don't know what it is. And then it imports that in the form that is required by Msbc to structure a functioning bill of material. And what we're discussing here is that exact tool" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- **Nathan's reading of the same rule.** "Engineers are not going to go into Msbc and enter this information. So then we do need some way to structure a BOM outside of Msbc so it can be. Programmatically added" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].

The derived notes record it as "Engineering data lives in GitHub; supplier and financial data lives in MSBC; neither side edits the other" — "Val's set rule for the business" [[raw/Meeting_Notes_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].

## Why

- **Not a debate, a set-up.** "I don't want to play a role of a therapist that convinces why one thing is better than the other. I'm just saying that's how we are setting up our business. To function. And let's work through. Concerns. one by one, and let's find solutions to the concerns" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- **One source of truth, and it is the design.** "the source of truth here is your drawings, your design. From there, I want to automate… I want to remove all this labor from you"; "That's the source of truth. I don't want to create another source of truth. I already have one source of truth" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- **Nothing in the machine is improvised.** Every screw has a pre-drilled hole ("We don't have self-tapping screws"); a bought PC board has measured dimensions and posts; a lock has a drawing "either supplied by a supplier and you approve that drawing and you put it in the file, or alternatively you design and create a tool for it. and create a spec for it. Nothing gets improvised in the machine." So the design already says what goes where, and the rest can be derived [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].

## What this leaves to the tool, not to people

- The grouping of the flat list into MSBC assemblies ("that grouping, the step, could be a step of automation. It doesn't have to be a manual step") — the contested part, on [[wiki/decisions/2026-09-23-the-bom-source-of-truth-is-the-latest-design-in-github-and-sync-runs-one-way.md]] (Sept-30 update) [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- The accounting fields on a new item (posting groups, dimensions, inventory type, units of measure), which Lev says are not engineering data and today are entered by a person — on [[wiki/decisions/2026-09-30-a-new-part-number-is-assigned-by-claude-from-the-standard-in-github-and-pushed-to-msbc-once.md]] [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].

## How this sits against earlier rulings

- **Evolution of Aug 12 and Sept 24**, not a contradiction: Aug 12 agreed "GitHub is the source of design truth" with a sync robot into BC ([[wiki/topics/github-release-management-pipeline.md]], Aug 12); Sept 24 read out "Data flows one way only. GitHub to Business Central. Nothing flows back." Sept 30 adds the people rule — who may edit which system — and names the crossing tool. Genadi accepted the engineering half on all three dates; the BOM half stays contested [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- It also narrows the June-25 2026 "Business Central is the single source of truth" governance rule on [[wiki/topics/business-central-erp-implementation.md]] for design data, as Aug 12 and Sept 23–24 already did (inference).

## Oct 1 2026 — prices and quotations stay out of GitHub; revisions and datasheets go in

On the [[wiki/meetings/2026-10-01-genadi-io-board-chips-flat-bom-pilot-and-street-cabinet-panel.md|Oct 1 5:02 PM call]] (Russian) Genadi proposed putting, beside every bought item in GitHub, "как мы общаемся… что записывается с вендерами, cotation какие-то spex". Val: "в гетхабе это не нужно." Genadi: "Но вы сказали общение с вендором, ревизии, даташиты — не цены." So the border holds in practice: vendor revisions and datasheets with the engineering files; quotations and prices on the MSBC side. The same call restated "Туда [в MSBC] нужно загнать только готовый [bill of material]" — see [[wiki/decisions/2026-10-01-only-the-finished-bom-goes-into-msbc-the-configurator-is-ai-logic-outside-it-no-hybrid-and-the-pilot-is-the-flex-pay-slim.md]] [[raw/Meeting_Transcript_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026.md]].

## Open questions

- What exactly is the "transcriber" — a GitHub Action on merge or tag (the Aug-12 design), a scheduled job ("hourly… by minute"), or something Nathan designs after his experiments? Not settled — [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]

**§15.8:** clear — process rule only. Val's sharper remarks at Genadi on this call are not recorded. **§15 #9:** clear — "highly confidential banking information" for a vendor is a category, not a value.

## Sources
- [[raw/Meeting_Notes_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]
- [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]
- [[raw/Meeting_Transcript_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026.md]]
