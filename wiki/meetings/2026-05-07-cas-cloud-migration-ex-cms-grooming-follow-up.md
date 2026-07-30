---
type: meeting
title: CAS Cloud Migration — ex-CMS Grooming Follow-up (May 7 2026)
date: 2026-05-07
aliases: [CAS Cloud Migration ex-CMS Grooming Follow-up, CAS Cloud Migration Sequencing, CMS cloud-migration sequencing, ex-CMS grooming follow-up]
source-count: 2
---

# CAS Cloud Migration — ex-CMS Grooming Follow-up (May 7 2026)

**Date:** 7 May 2026, 12:59pm Eastern (§11 recording header time; the `_085927` filename stamp is a different zone, not the meeting time); ~19m 50s.
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (transcribed "Dzmitry Chudzinau"), [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (transcribed "Sergey Tsimanov").

The follow-up to the Apr-28 doc-readiness gate: with the Claude-Code documentation pass on the last CMS/CAS repositories nearly finished, the meeting turned to the core question of **how to sequence the cloud migration** — Chudinov/Bosik argued for a first "lift-and-shift" phase (containerize onto AWS, swap MS-SQL→PostgreSQL, architecture largely intact), Val pushed back that the team should define capabilities → architecture → tech-stack **first** and migrate directly to the new stack to hit a 3–5x cost reduction, and the two positions were reconciled into a staged plan gated by a May-14 tech-stack kickoff. Val also approved the annual Tableau renewal. Substance and citations live on [[wiki/topics/docs-as-code-and-atlassian-exit.md]] (May 7 2026 section). Continues the CMS-cloud thread from [[wiki/meetings/2026-03-23-data-access-strategy-cms-cloud-migration.md|Mar 23]] and [[wiki/meetings/2026-04-28-cas-cloud-migration-doc-readiness-review.md|Apr 28]]. §12: the "CAS Cloud Migration Sequencing" notes are the derived §3 summary of THIS same recording ("Source meeting: CAS Cloud Migration — ex-CMS Grooming Follow-up") → ONE stub, source-count 2. §15.8: only data/cloud/CMS/licensing economics recorded (MS-SQL licensing cost, ~3–5x cloud-cost target, Tableau at USD $900/yr); no named-person compensation. [[raw/Meeting_Notes_CAS_Cloud_Migration_Sequencing-May-7-2026.md]]

## Sources
- [[raw/CAS_Cloud_Migration_ex-CMS_Grooming_Follow-up-May-7-2026.md]]
- [[raw/Meeting_Notes_CAS_Cloud_Migration_Sequencing-May-7-2026.md]]
