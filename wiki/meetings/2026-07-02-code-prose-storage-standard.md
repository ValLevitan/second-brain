---
type: meeting
title: Code prose storage standard (Jul 2 2026)
date: 2026-07-02
aliases: [code prose storage, prose storage standard, docs folder prose, prose subfolder, prose verification control, Fable model cost, July 2 2026 prose storage]
source-count: 1
---

# Code prose storage standard (Jul 2 2026)

NOTES-ONLY · July 2, 2026, 11:04 AM ET · ~24m. **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/pavel.md|Pavel Frolov]].

**Purpose:** The same-morning companion to the [[wiki/meetings/2026-07-02-ris-prose-documentation-standard.md|10:03 AM RIS prose meeting]] — this session settled **where** Claude-generated prose (plain-language descriptions of code) should live in each repository and **how to check** it. Result: prose sits next to the code in a subfolder under each repo's existing `docs/` folder (the worldwide standard and where AI looks for documentation), `.claude` holds Claude's instructions only, and the CLAUDE.md/README points to the prose path. Andrei's dashboard report will verify the prose folder exists and flag whether pull requests changed files in it. A 1-hour sign-off meeting was booked for **Monday, July 6, 2026, 7:00–8:00 AM EDT** (Andrei Bosik, Pavel Frolov, Irina Shishko).

The durable substance — the storage standard, the verification control, the requirement-vs-prose match idea, and the administrative note on the new expensive **Fable** Claude model's cost/ROI — lives on [[wiki/topics/github-release-management-pipeline.md]] (Jul-2) and [[wiki/topics/ai-assisted-development.md]] (Jul-2). §15.8 clear — tooling/prose-standard/model economics only; no named-person compensation.

## Sources

- [[raw/Meeting_Notes_Code_Prose_Storage_Standard-July-2-2026.md]]
