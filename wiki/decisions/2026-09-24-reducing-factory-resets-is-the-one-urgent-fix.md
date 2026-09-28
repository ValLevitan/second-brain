---
type: decision
title: If only one thing can be fixed, it is to reduce the number of factory resets — urgent, and the next meeting is narrowed to it
date: 2026-09-24
aliases: [reduce the number of factory resets, as little factory reset as possible, low-hanging fruits, I am narrowing the subject, meeting three, 2 1/2 thousand machines in the field]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# Reducing factory resets is the one urgent fix

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the close of the [[wiki/meetings/2026-09-24-ris-serial-binding-and-factory-reset-focus.md|Sept 24 2026 7:02 AM RIS follow-up]], after the talk had drifted into redesign. All quotations up to the Sept-25 update from [[raw/Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026.md]].

## The stop

"I need to stop this. I need to stop this. The objective of this meeting is to find the low-hanging fruits… in what bothers technicians today in the field and fix those low-hanging fruit that bothers them the most. And we identify those as those eight." He agreed with the longer-term changes — "There are plenty of things to modify in the future. And I agree with those modifications" — but "the focus of this meeting must be on the low-hanging fruits."

## Why now

"They don't have a modem. And that will take us quite a bit of time to introduce modems, and modems may have other problems. So right now we're dealing with 2 1/2 thousand machines installed in the field. And one of the biggest issues is the time that it takes to recommission a machine… Due to a factory reset." *(The figure is Val's spoken, rounded count of machines in the field; the source does not say whether it is Georgia only or all markets.)*

## The ruling

"If there was a single point that we could fix one thing only… is to reduce the number of factory resets required in operation of our machine." And: "this is quite urgent, immediate. This is an immediate, urgent issue." Felipe: "Yes, agreed."

[[wiki/people/pavel.md|Pavel]]: "we need at least to split this case to separate to several. Because some cases with factory reset" (cut off). The engineers had already sketched three kinds of reset at 5:41 AM — see [[wiki/topics/ris-remote-install-and-machine-states.md]] (Sept 24).

## The next meeting

"I suggest having another meeting tomorrow at 7… on the same subject. I am narrowing the subject now… I will schedule another meeting for tomorrow at 7 A.m."

## Update — Sept 25 2026: the follow-up is held, and the fix gets a name

The narrowed meeting took place on Sept 25 at **10:31 AM**, not 7 AM ([[wiki/meetings/2026-09-25-ris-mvp1-factory-reset-reduction-plan.md|Sept-25 RIS follow-up]]). Val opened by repeating this ruling: "we lost our focus… I want to find at least one. maybe hopefully two, three items that by fixing it, we can alleviate maybe 50, 60% of the issues. And I would call it MVP1 release of the RIS. So RIS rework." And: "the most suffering comes with the factory reset, that everything requires a factory reset for us, which I'm repeating myself, is appropriate design for 20 year ago." [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]

- Pavel answered with a numbered list of six points; his first idea (point 4 in his final list) was to reuse the last RIS after a factory reset, which he thinks "will fix more than 50% of cases". The list is on [[wiki/topics/ris-remote-install-and-machine-states.md]] (Sept 25, 10:34 AM) [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]].
- Val also said all of it is "called patching. It's not really fixing. So fixing, for example, is moving people to a modem." [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]
- Scope and next step: [[wiki/decisions/2026-09-25-the-ris-rework-mvp1-is-for-flex-machines-only.md]] and [[wiki/decisions/2026-09-25-felipe-acts-as-product-owner-for-the-ris-rework.md]].

## History

- [x] Val Levitan — schedule the follow-up meeting for 7:00 AM on Sept 25, narrowed to reducing factory resets — due Sept 24 2026 — [[raw/Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026.md]] — **discharged Sept 25:** the follow-up was held that day, at 10:31 AM rather than 7 AM [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]
- [x] Pavel Frolov — split the factory-reset case into several separate cases — due unspecified (the next meeting) — [[raw/Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026.md]] — **discharged Sept 25:** Pavel read out six numbered points, and Felipe split the hard-reset need across the 8 use cases [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]

**§15.8:** clear.

## Sources

- [[raw/Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026.md]]
- [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]
