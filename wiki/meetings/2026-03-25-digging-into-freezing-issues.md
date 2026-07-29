---
type: meeting
title: Digging into Freezing Issues (Mar-25 morning)
date: 2026-03-25
aliases: [Digging into Freezing Issues, freezing software-version isolation, South Dakota QR race condition]
source-count: 2
---

# Digging into Freezing Issues (Mar-25 morning)

**Date:** 2026-03-25 (recording header 09:32am, 25m 20s; Russian). Recording base `Digging into Freezing issues-20260325_053201`.
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko, Alexander Biratko.

The morning software-analysis session of March 25: Val tries to **chronologically isolate** what changed in the software between the old release that ran on the "Pech 123" machines and the current freezing-prone Georgia build (~v1.14, which added dual SAS, a printer, and a new skill at the **DC/Data-Center layer**), agrees to run the changed DC and HAL code through a **Claude Code review** (Alexander + Zhenya, results due in ~4 hours), and hears Irina report a **separate** South Dakota bug — QR-code scans crash/reboot the machine — root-caused as a **race condition** in the game-disable/tilt sequence and reproduced the same day. [[raw/transcript_Digging_into_Freezing_issues-March-25-2026.md]] [[raw/Meeting_Notes_Freezing_Issues_Investigation-March-25-2026.md]]

This is the **primary record** of the meeting Val's V1.3 investigation report later summarized. Substance and cross-investigation facts live on [[wiki/topics/egm-freezing-investigation.md]] (the "Mar-25 primary meetings" and "Consolidated findings" sections). The follow-up consult with the external specialist [[wiki/people/evgeniy-alekseev.md|Alekseev]] two hours later is [[wiki/meetings/2026-03-25-freezing-investigation-alekseev-followup.md]]. The prior-day watchdog sessions are [[wiki/meetings/2026-03-24-fp10-freezing-watchdog-discussion.md]] and [[wiki/meetings/2026-03-24-io-centric-watchdog-wiring.md]].

*Name notes (§4):* the notes credit the HAL as **primarily written by "Dima"**; Val's spoken phrase is garbled ("Димой пекулярном" — "пекулярном" reads as the adjective *peculiar*, not a clean surname), plausibly the recurring **"Dima Pikulev/Pikuli"** contractor Genadi cited Mar-24 but the surname is NOT cleanly stated here. Queued Tier-B, not forced — no wikilink. The DC printer/skill work is attributed to "Zhenya" — read as [[wiki/people/evgeny-kharetski.md|Kharetski]] (LGS/Omni backend) by context, plus Alexander ("Sasha").

## Sources

- [[raw/transcript_Digging_into_Freezing_issues-March-25-2026.md]] — Mar-25 9:32am freezing software-analysis call (transcript).
- [[raw/Meeting_Notes_Freezing_Issues_Investigation-March-25-2026.md]] — *derived:* AI meeting summary of the same call (folded).
