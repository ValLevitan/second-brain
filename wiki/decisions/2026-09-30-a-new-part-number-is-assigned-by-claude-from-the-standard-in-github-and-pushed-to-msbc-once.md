---
type: decision
title: A new part number is assigned by Claude from the written part-number standard in the GitHub "standards" repo and pushed to MSBC once, when the part is created
date: 2026-09-30
aliases: [part number from the standard, Claude reads the standard and gives it a part number, standards repo part number, transferred into MSBC only for the first time, Claude can populate it, two sources of input for a new part number, posting groups dimensions units of measure, accounting fields on a new item, South Dakota cable for Light and Wonder example]
source-count: 2
status: active
open-commitments: 0
open-questions: 2
---

# A new part number comes from the standard in GitHub, assigned by Claude, and is pushed to MSBC once (Sept 30 2026)

Stated by [[wiki/people/val-levitan.md|Val Levitan]] and accepted by [[wiki/people/genadi-peari.md|Genadi Peari]] ("Perfect") on the [[wiki/meetings/2026-09-30-github-to-msbc-bom-flat-list-bridge.md|Sept-30 GitHub-to-MSBC meeting]] (English), with a caveat from [[wiki/people/lev-rudky.md|Lev Rudky]]. Quotations from [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].

## What was decided

- **Genadi's test case.** "let's say tomorrow we need South Dakota, we need to supply cable for light and wonder. I need to create the part number. I have a new number. What is automatically?" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]
- **Val's answer.** "Part number part number needs to be created based on a standard that is developed. You the Claude reads the standard. And it gives an automatic part number that is then transferred into Msbc only for the first time. When that part is created, it's done." Genadi: "Perfect." Then: "We have a standard of creating parts, part numbers. That is written in Github, in the knowledge base, in the repo that is called standards. So. Claude looks at the standards and gives it a part number." Genadi: "OK, good. No, no questions" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- **Where it is first created does not matter to Genadi.** "I can create it in Github. It's perfect. Or Msbc, it doesn't matter." Val: "But it's a different procedure" — the standard lives in GitHub [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- **Populating the part into products is also meant to be automatic — but unproven.** Genadi: "Then we need, I need to populate it in three different products." Val: "You don't need to populate it. Claude can populate it." Asked how exactly, Val: "Hopefully… I don't know… before Nathan had a chance to experiment with it, we don't know right now, but it's not… spaceship science. This is just a little bit of tinkering here and there" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].

The derived notes record it as "New part numbers come from a written standard in the GitHub standards repo, assigned by Claude, and pushed once to MSBC" — "Genadi agreed ('Perfect')" [[raw/Meeting_Notes_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].

## Lev's caveat — a part number in BC is more than engineering data

- "If the source of a new part number. He is in Github. And it automatically gets created in BC afterwards. So you need to populate there more than engineering parameters in order to create a part number. in BC. It's all kinds of BC classifications associated with the part number, which has nothing to do with engineering. It's various posting groups, things like that, dimensions." Genadi added "Serialized." So there are "Two sources of input. for a specific new part number" — one from engineers, one from somebody else [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- He was not talking about vendors: "talking strictly about part number as a stand-alone entity… when Genadi creates… a new part number in Msbc, he enters additional information that is not strictly engineering information. Things like Dimensions. Type of inventory in simple language… if there is, for example, a new unit of measure for some part, it has to be initialized in the system and has to be accommodated during transfer as well" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- **Val: nothing changes in who supplies what.** "Nothing changes, it's still the same. Today, we require two or three people participating in. Creating a proper. Part number in BC. Except we do it part by part manually." (His examples — vendor banking, address, contacts, payment terms — were about vendors, which Lev set aside.) Nathan: "that's accounting, entering that information"; "we have to map all the account codes to that item, all the other outside of engineering work" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- Lev's close: "it's probably a good idea to experiment with to see how this concept works, because there are… some unanswered questions there. I understand it on high level, but in terms of getting into practical implementation. There might be issues" [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].

## How this sits against earlier rulings

- **Against Aug 12 — a change in who assigns numbers.** The Aug-12 design said "BC assigns numbers, GitHub assigns meaning": a new part's item YAML says "new" and BC gives the number on the sync ([[wiki/topics/github-release-management-pipeline.md]], Aug 12). Sept 30 has Claude assign the number from the standard in GitHub and push it to MSBC once. Recorded as an **evolution** (later source, same thread); the two are not reconciled on tape [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- **Against Sept 23 — answers the open question** "where is a part number first created — by hand at drawing time?" on [[wiki/decisions/2026-09-23-the-bom-source-of-truth-is-the-latest-design-in-github-and-sync-runs-one-way.md]]: today Genadi assigns the number himself in SolidWorks when he makes a new part and enters it by hand in MSBC after the project; the rule above replaces the hand step [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].
- **Against Apr 6 2026** — the "smart/semantic naming convention" for top-level part numbers Genadi asked for then ([[wiki/topics/business-central-erp-implementation.md]], Apr 6) is the kind of standard Val now says is written in the standards repo. Whether the part-number standard already exists in writing is **not confirmed** on this tape — Val says it "is written in Github"; nobody opens it.

## Open questions

- Does the written part-number standard already exist in the standards repo, and what does it say? Not shown on the call — [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]
- Who supplies the accounting fields (posting groups, dimensions, inventory type, units of measure) for an item that starts in GitHub, and at what step? Lev's question; Val: the same people as today — [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]

**§15.8:** clear — process only. **§15 #9:** clear.

## Sources
- [[raw/Meeting_Notes_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]
- [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]
