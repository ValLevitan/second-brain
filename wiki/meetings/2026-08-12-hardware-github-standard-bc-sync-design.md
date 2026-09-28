---
type: meeting
title: Hardware GitHub standard + Business Central sync design (Val & Genadi Peari, Aug 12 2026)
date: 2026-08-12
aliases: [Hardware GitHub Standard and BC Sync Design, General_alignment-August-12-2026, General alignment Val Genadi Aug 12, BOM sync robot meeting]
source-count: 2
---

# Hardware GitHub standard + Business Central sync design (Val & Genadi Peari, Aug 12 2026)

**When:** August 12, 2026, 3:00 PM Eastern; mixed Russian/English; the transcript runs to about 2 h 38 min. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
**Who:** [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/genadi-peari.md|Genadi Peari]] (the transcript's "Speaker 1"; Val calls him "Gennady"). [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]] The diarization label "Abiguele" is a recording artifact, not a person. [[raw/Meeting_Notes_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]

**Purpose:** a long 1:1 that started with parts sourcing (a JCM recycler, a Rockchip board) and became a live design session, with Val's "second brain" agent on screen, for how JVL stores hardware information in GitHub and keeps Business Central in step with it. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]

Substance lives on:
- [[wiki/topics/github-release-management-pipeline.md]] — the hardware repository structure, the pull-request/merge/tag change process, and the sync robot (Aug-12 section).
- [[wiki/topics/business-central-erp-implementation.md]] — the assembly-BOM finding (no version history), GitHub tags as BOM history, and Val's core-fix order for BC (Aug-12 section).
- [[wiki/organizations/jcm.md]] — the four-drum JCM recycler as a second source (Aug-12 section).
- [[wiki/topics/low-cost-street-machine.md]] and [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]] — the RK3576 8 GB board picked for testing; 16 GB judged not worth it.
- People: [[wiki/people/genadi-peari.md]], [[wiki/people/nathan-carver.md]], [[wiki/people/evgeniy-alekseev.md]], [[wiki/people/andrey-bosik.md]], [[wiki/people/pavel.md]], [[wiki/people/mikhail-perelman.md]], [[wiki/people/cliff.md]].

**Notes vs transcript (the transcript was followed):**
- The notes say a hardware-repositories standard was "adopted August 12". In the transcript the agent first said so, then Val corrected it: it was only a chat, and the draft is a **proposal that still needs Genadi's approval**. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]] [[raw/Meeting_Notes_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- The notes say Nathan Carver was "brought in near the end". In the transcript Nathan never speaks; Val dictates a message ("Pismo" = письмо) addressed to him. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- The notes say JCM shipped a unit without a bezel. The transcript does not name the vendor of that unit. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- The notes give "proceed with the RK3576 8 GB board". The transcript says take **two boards and test them**. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- The notes give the duration as ~174 min; the transcript's last timestamp is 02:38:38. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]

**Unresolved names (queued):** "Eugene is the approver" (not clear who; Val then tells Genadi "you review and merge it"); "Ignatiy" (Val addresses someone by this name while asking for the draft to be read — likely a garble, not resolved); "Klotov" (Genadi: discuss the hardware structure "with Klotov" — not resolved). [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]

**§15.8:** Val's personal remarks about two named colleagues' age and work habits, and his view of one engineer's recent work, are withheld. Only process and company economics are recorded.

## Sources
- [[raw/Meeting_Notes_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
