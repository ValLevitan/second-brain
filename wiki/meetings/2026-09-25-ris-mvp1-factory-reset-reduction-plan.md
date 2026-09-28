---
type: meeting
title: RIS follow-up three — "MVP1 release of the RIS rework", Pavel's six-point list to cut factory resets, Flex only, and Felipe as product owner (Sept 25 2026, 10:31–11:33 AM)
date: 2026-09-25
aliases: [RIS features follow-up fewer factory resets, RIS MVP1 Factory Reset Reduction Plan, RIS Pre-Meeting Travel Productivity Chat, RIS meeting three, MVP1 release of the RIS rework, RIS rework MVP1, Sept 25 RIS follow-up]
source-count: 4
open-commitments: 0
open-questions: 0
---

# RIS follow-up three (Sept 25 2026, 10:31 AM)

**Date/time:** September 25 2026, **10:31 – 11:33 AM Eastern**, from the two `**Date:**` header lines (segment 1: 10:31–10:34 AM; segment 2: 10:34–11:33 AM). Teams title "RIS features follow-up: fewer factory resets" [[raw/Meeting_Transcript_RIS_Pre_Meeting_Travel_Productivity_Chat-September-25-2026.md]] [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]. **Language:** mostly English; Russian in two stretches (about minutes 13–15 and 31–37 of segment 2), where speech recognition is very poor [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]].

**Attendees** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]] (ran it), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/felipe-miranda.md|Felipe Miranda Giorgi]] [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]. [[wiki/people/sebastian.md|Sebastian]] could not join: Felipe said he was driving and about to reach Georgia [[raw/Meeting_Transcript_RIS_Pre_Meeting_Travel_Productivity_Chat-September-25-2026.md]].

**Purpose.** Meeting three on the hard-reset problem. It is the follow-up Val ruled for on Sept 24, narrowed to one subject: fewer factory resets ([[wiki/decisions/2026-09-24-reducing-factory-resets-is-the-one-urgent-fix.md]]). Val asked for one to three items that remove "maybe 50, 60% of the issues", and called it the "MVP1 release of the RIS. So RIS rework" [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]].

## Where the substance lives

- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Sept 25, 10:34 AM) — Pavel's six points, the soft-reset logic, Irina's one-RIS idea, error codes 2/3, the IO board, the release-packaging question, the modem and the RIS-in-the-cabinet idea.
- [[wiki/decisions/2026-09-24-reducing-factory-resets-is-the-one-urgent-fix.md]] — Sept-25 update: the follow-up held; both Sept-24 commitments discharged.
- [[wiki/decisions/2026-09-25-the-ris-rework-mvp1-is-for-flex-machines-only.md]] — "Altera is done".
- [[wiki/decisions/2026-09-25-felipe-acts-as-product-owner-for-the-ris-rework.md]] — the grooming task, the hand-off chain, and the Monday Sept-28 review.
- [[wiki/decisions/2026-09-24-engineering-plans-to-switch-off-the-passport-check-for-georgia-builds.md]] — Sept-25 update: the passport QR screen moves out of the factory reset.
- People: [[wiki/people/val-levitan.md]] · [[wiki/people/pavel.md]] · [[wiki/people/felipe-miranda.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/sebastian.md]] · [[wiki/people/genadi-peari.md]] (in absentia)

## Notes on the sources

- **§12 — one meeting in two segments, four files (source-count 4).** Both segments carry the same Teams title, both headers say "Segment 1 of 2" / "Segment 2 of 2", and the times run on without a gap (10:34 AM end, 10:34 AM start). Segment 2 opens mid-sentence ("meeting. Yeah. So what we were…"). So segment 1 is the **opening of this meeting**, not a separate chat. It holds only greetings, Sebastian's absence and Val's personal travel talk, which is not recorded [[raw/Meeting_Transcript_RIS_Pre_Meeting_Travel_Productivity_Chat-September-25-2026.md]] [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]. A corpus-wide grep ("fewer factory resets", "RIS_MVP1", "RIS_Pre_Meeting", "MVP1 release") found no other stub. It is a different event from the [[wiki/meetings/2026-09-24-ris-serial-binding-and-factory-reset-focus.md|Sept-24 7:02 AM meeting two]]. New meeting.
- **Held at 10:31 AM, not 7 AM.** On Sept 24 Val said he would book the follow-up for 7 AM on Sept 25 (see [[wiki/decisions/2026-09-24-reducing-factory-resets-is-the-one-urgent-fix.md]]). The recording starts at 10:31 AM [[raw/Meeting_Transcript_RIS_Pre_Meeting_Travel_Productivity_Chat-September-25-2026.md]]. The sources do not say why.
- **§12 concurrent capture — the InComm call.** The [[wiki/meetings/2026-09-25-incomm-john-exit-and-blue-card-hold.md|Plaud call with John of InComm]] (~10:39 AM, 7m 16s) falls inside segment 2, at about minutes 5–12 (time from that stub). At 00:04:27 Val says "I need, I need to take this, continue talking." He then has **zero turns** until 00:13:37. The meeting went on without him: Pavel, Felipe and Irina talk about use cases, meters and the soft reset [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]. This fits Val stepping out of the RIS meeting to take the InComm call (**inference**). Two separate events; nothing is merged.
- **§4 name calls.** "Sebastian" = [[wiki/people/sebastian.md|Sebastian Cortes]], the field product manager in Val's hand-off chain. "Genadi", who suggested moving the IO board connection, = [[wiki/people/genadi-peari.md|Genadi Peari]] (hardware). "Juan", whose role Felipe takes for this work ("which would be one's responsibility normally. We obviously regret that Juan is not here"), is probably [[wiki/people/juan-martinez.md|Juan Martinez]] (**inference**; not asserted). Garbled words in Russian stretches — "Elisa", "Alex", "Seven and Shavialeu", "Victoria", "Arnold", and Pavel's "Juan. Cortana" — are not read as people. Val's "Call Chudzinau" is his Russian idiom for a roundabout workaround (he first says "Cherez Zhukova"); it is **not** read as [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (inference).
- **Notes vs transcript — the wiki follows the transcript** ([[raw/Meeting_Notes_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]], [[raw/Meeting_Notes_RIS_Pre_Meeting_Travel_Productivity_Chat-September-25-2026.md]]):
  1. **Omitted: Irina's one-RIS idea** (Russian, 00:31:22–00:33:15) — one RIS with a list of machine numbers; Pavel's reply that this is a rework of installation. Recorded on the topic page.
  2. **Omitted: Val stepping out** at 00:04:27 ("I need to take this").
  3. **Omitted: Val's Russian turn** at 00:13:37, "я думаю, что нам не нужно передавать статистику" (the rest is garbled).
  4. **Soft reset and meters.** Pavel first said "Clearing some known critical data, like meters", then, after Felipe asked, "Left meters, left meters". The notes give only the corrected version.
  5. **"Product manager" first.** Val first said "You're acting as a product manager now", then corrected himself to product owner. The notes give only the correction.
  6. **Segment-1 attendees.** The segment-1 notes list Val, Irina and Felipe only, but Val speaks there of "Irina and Pavel". Pavel has no turn in segment 1.
- **§15.8:** clear. Val's personal travel and work habits (segment 1), a hotel story, and his joke name for the final tilt are small talk and are not recorded. No pay, health or performance judgements.
- **§15 #9:** clear. "Build 1919" is a software build label, not a corporate identifier.

## Sources

- [[raw/Meeting_Notes_RIS_Pre_Meeting_Travel_Productivity_Chat-September-25-2026.md]]
- [[raw/Meeting_Transcript_RIS_Pre_Meeting_Travel_Productivity_Chat-September-25-2026.md]]
- [[raw/Meeting_Notes_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]
- [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]
