---
type: meeting
title: CIBC / JVL MSBC API Integration (account structure settled, API role scoped)
date: 2026-07-28
aliases: [CIBC JVL MSBC API Integration, CIBC ACH Microsoft Dynamics API Integration, CIBC Nathan ZBA BusinessCentral API, ZBA account and Business Central API integration]
source-count: 4
---

# CIBC / JVL MSBC API Integration (account structure settled, API role scoped)

**Date:** July 28, 2026, 4:01 PM ET (~13 min). The fuller transcript's header gives 4:01 PM; the first copy's header said 4:00 PM. [[raw/Meeting_Transcript_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026.md]] [[raw/Meeting_Transcript_CIBC_JVL_MSBC_API_Integration-July-28-2026.md]]
**Attendees:** Michael Hill (CIBC, external); [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/nathan-carver.md|Nathan Carver]] (JVL). [[raw/Meeting_Transcript_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026.md]]

**Two copies of one recording.** `Meeting_Transcript_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026` is a fuller re-transcription of the same audio as `Meeting_Transcript_CIBC_JVL_MSBC_API_Integration-July-28-2026` — same timestamps and words, plus speaker labels and a header clock time. It is now the source of record for who said what. Its recording also runs on after ~00:23 with unrelated personal background talk; that part is not a meeting and is not recorded (§15.8 / personal). [[raw/Meeting_Transcript_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026.md]]

A short call to confirm how the new **CIBC account structure** for JVL will work and what role an **API** needs to play (CIBC ↔ Microsoft Business Central). The account structure is settled — a Zero Balance Account receives batched deposits and sweeps them to a separate account at end of day — and **Nathan** scoped the API down to read-only verification. This continues the CIBC banking-setup thread from the [[wiki/meetings/2026-07-02-cibc-business-central-integration.md|Jul-2]] and [[wiki/meetings/2026-07-06-cibc-banking-setup-review.md|Jul-6]] calls. [[raw/Meeting_Transcript_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026.md]] [[raw/Meeting_Notes_CIBC_JVL_MSBC_API_Integration-July-28-2026.md]]

Substance lives on:
- [[wiki/organizations/cibc.md]] (Jul-28) — the settled ZBA-plus-sweep account structure, the batch-deposit drill-down report, and Michael's setup being ready. [[raw/Meeting_Transcript_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026.md]]
- [[wiki/topics/business-central-erp-implementation.md]] (Jul-28) — the read-only API role, the Microsoft Dynamics / Business Net Banking integration, and Val's hunch that the existing CIBC–Dynamics integration may already be the easier path. [[raw/Meeting_Transcript_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026.md]]

**Notes vs transcript (transcript followed).** The first notes credit the "read-only API" point to Val and Michael; the speaker-labelled transcript shows Nathan said it. The new notes add things the transcript does not say: that Nathan "owns" the integration, a Nathan task to "build the BC-side API call", and "account paperwork" (Michael only said his part was "already done" and he would "press send"). The new notes also carry bank account and routing numbers taken from elsewhere; those are not copied here (held in Corporate Registry). [[raw/Meeting_Notes_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026.md]] [[raw/Meeting_Notes_CIBC_JVL_MSBC_API_Integration-July-28-2026.md]] [[raw/Meeting_Transcript_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026.md]]

## Sources

- [[raw/Meeting_Transcript_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026.md]]
- [[raw/Meeting_Notes_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026.md]]
- [[raw/Meeting_Notes_CIBC_JVL_MSBC_API_Integration-July-28-2026.md]]
- [[raw/Meeting_Transcript_CIBC_JVL_MSBC_API_Integration-July-28-2026.md]]
