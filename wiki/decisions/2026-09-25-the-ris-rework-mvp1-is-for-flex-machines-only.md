---
type: decision
title: The RIS rework MVP 1 (fewer factory resets) is for Flex machines only — "Altera is done"
date: 2026-09-25
aliases: [only Flex machines, Altera is done, MVP1 release of the RIS rework, RIS rework MVP1 scope, we're upgrading only Flex machines]
source-count: 2
status: active
open-commitments: 0
open-questions: 2
---

# The RIS rework MVP 1 is for Flex machines only

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-25-ris-mvp1-factory-reset-reduction-plan.md|Sept-25 10:31 AM RIS follow-up]]. All quotations from [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]].

## What was decided

- **The release.** Val named it the "MVP1 release of the RIS. So RIS rework." Its job is "An immediate relief… Of the suffering that is out there", and "the most suffering comes with the factory reset". He wanted one to three fixes that together remove "maybe 50, 60% of the issues". If item one can be done faster, "Let me introduce it in the MVP one, or even maybe possible within the V3 release. Maybe I will go through quick reapproval… Even if we can get it next week, OK, fine."
- **The scope.** Felipe: "Only Flex machines. We're not referring to Altera H or any." Val: "no, Altera is done, finished, finished, is done." Felipe: "we're upgrading only Flex machines, correct?" Val: "Yes."
- **The size.** Val: "we have 3000 machines and locations", then "Whatever that number is, 2000, 2 1/2, 3000, I don't know." *(Spoken, rounded; on Sept 24 he said "2 1/2 thousand machines" — see [[wiki/decisions/2026-09-24-reducing-factory-resets-is-the-one-urgent-fix.md]].)*
- **The field role.** Val: when [[wiki/people/sebastian.md|Sebastian]] arrives, "his job will be to go and… Update all of the machines… Of course, it will not be as direct as this, but assist in upgrading all of the machines."

## What was not decided

- **Games or no games.** Val first said the release "will not update any games… We're only upgrading that feature." Pavel then said: "As we have a big amount of different software, these fixes will require to make changes to these particular versions or to install the latest." Val set out the choice: fix each field version — "maybe 10, 20… So we will need 20 upgrades" — or "do only two upgrades", one for dual screen and one for vertical, bringing all to the latest. "But that will require game changes as well." His point on approvals: "So there's a difference, 20 approvals. Or 2 approvals."
- **Felipe's worry.** Earlier, "we would have one, two, three, 4, 5, 5 versions total. Three for dual, 2 for vertical. Has everyone updated the software? No." Customers on build 1919 "don't complain much about machines freezing or anything, and we have the highest performance from all the different versions". Getting everyone on board "would be a challenge".
- **Pavel's cost view.** "From the perspective of getting certificates, the cheaper is to get one bundle with 18 games within one package" for dual screen — "one file with speech 1 + 2 + 3" (read as Peach 1 + 2 + 3; Felipe names "Peach 1 software, Peach 2 software, and Peach 3 software"). Felipe: "Yes, that would be ideal" — technicians would carry one dongle instead of three.

## Open questions

- Fix each field version (about 20 approvals), or move all Flex machines to the latest software in two upgrades (about 2 approvals, with game changes), or one 18-game bundle? Not decided on Sept 25 [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]].
- Which of Pavel's six points go into MVP 1 or into V3, and how long each takes — Val asked for this at the start; no dates or percentages per point were given [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]] [[raw/Meeting_Notes_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]].

The six points are on [[wiki/topics/ris-remote-install-and-machine-states.md]] (Sept 25, 10:34 AM). The next step is [[wiki/decisions/2026-09-25-felipe-acts-as-product-owner-for-the-ris-rework.md]].

**§15.8:** clear. **§15 #9:** clear.

## Sources

- [[raw/Meeting_Notes_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]
- [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]
