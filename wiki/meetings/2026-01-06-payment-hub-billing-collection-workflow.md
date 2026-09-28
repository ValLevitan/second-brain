---
type: meeting
title: Payment Hub Location Billing & Collection Workflow (January 6 2026)
date: 2026-01-06
aliases: [Location_Billing_Collection, Payment Hub billing and collection workflow, Payment Hub Workflow and Business Rule Definition, location billing collection]
source-count: 2
---

# Payment Hub Location Billing & Collection Workflow (January 6 2026)

**Date:** January 6, 2026, 11:17 AM Eastern (header time; ~42 min per the notes). [[raw/Meeting_Transcript_Payment_Hub_Billing_Collection_Workflow-January-6-2026.md]] [[raw/Meeting_Notes_Payment_Hub_Billing_Collection_Workflow-January-6-2026.md]]

**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]]; [[wiki/people/nathan-carver.md|Nathan Carver]] (the walkthrough lead — Speaker 1, addressed as "Nathan"); [[wiki/people/pavel.md|Pavel Frolov]] (Speaker 5, addressed as "Pavel"); two more speakers (Speakers 3 and 4) who are not named in the transcript. [[raw/Meeting_Transcript_Payment_Hub_Billing_Collection_Workflow-January-6-2026.md]] The notes add, from the Outlook invite only, [[wiki/people/juan-martinez.md|Juan Martinez]] and "Dzmitry Chudzinau" ([[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]); the transcript does not confirm either of them spoke. [[raw/Meeting_Notes_Payment_Hub_Billing_Collection_Workflow-January-6-2026.md]]

**Purpose:** Nathan walked the team through the written Payment Hub **billing-and-collection workflow** (invoice header and lines in Business Central, the daily balance check and ACH draw through Dwolla, failure modes, alerting, retries) so the group could shape its business rules. [[raw/Meeting_Transcript_Payment_Hub_Billing_Collection_Workflow-January-6-2026.md]]

**Where the substance lives:**
- [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] — Jan 6 2026 section (the rules shaped, the open questions).
- [[wiki/people/nathan-carver.md]] — his follow-up work from this meeting.
- [[wiki/people/pavel.md]] and [[wiki/people/val-levitan.md]] — their points in the room.

**Notes vs transcript (transcript followed):**
- The notes call "no partial draw on a single invoice" **Val's ruling**. In the transcript Nathan raised the NACHA dispute risk first; later Val said "According to NACHA, we can't", was challenged by Speaker 4, and agreed: "We could, but it opens a dispute possibility." [[raw/Meeting_Transcript_Payment_Hub_Billing_Collection_Workflow-January-6-2026.md]]
- The notes say Pavel's "combination that brings the most cash" rule was **adopted, superseding oldest-first**. In the transcript Nathan said "So we'll do oldest first"; Pavel then raised the combination idea, Val restated it and called it "a great point", and Nathan answered "Okay, so that would be C" — recorded as a further option. No final choice is stated. [[raw/Meeting_Transcript_Payment_Hub_Billing_Collection_Workflow-January-6-2026.md]]
- The notes place "that's what it does for a living" (Business Central tracking what is owed) inside Val's architecture point. In the transcript an unnamed speaker (Speaker 4) said it. [[raw/Meeting_Transcript_Payment_Hub_Billing_Collection_Workflow-January-6-2026.md]]
- The notes read "1 to 1.30" as an overnight posting time (1:00–1:30). The transcript line is unclear. [[raw/Meeting_Transcript_Payment_Hub_Billing_Collection_Workflow-January-6-2026.md]]

**Transcription garbles:** "DWALA / Douala / Duvalo" = Dwolla (the ACH provider); "MSVC / MSNBC / MSPC" = MSBC (Business Central); "KLS" = POS, by context. [[raw/Meeting_Notes_Payment_Hub_Billing_Collection_Workflow-January-6-2026.md]]

§12: new meeting — no other stub on Jan 6 2026 or on this billing/collection workflow; both raws were uncited before this unit. §15.8: clear — fees and invoice amounts are worked examples of company billing logic; no named-person pay.

## Sources
- [[raw/Meeting_Notes_Payment_Hub_Billing_Collection_Workflow-January-6-2026.md]]
- [[raw/Meeting_Transcript_Payment_Hub_Billing_Collection_Workflow-January-6-2026.md]]
