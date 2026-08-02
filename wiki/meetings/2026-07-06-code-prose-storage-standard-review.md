---
type: meeting
title: Code prose storage standard — review & sign-off (Jul 6 2026)
date: 2026-07-06
aliases: [code prose storage review, as-built documentation, as-built code standard, prose sign-off, reverse-engineered requirements, 222 requirements 1836 acceptance criteria, data contract capability, Fable five multi-agent prompt, July 6 2026 prose review]
source-count: 1
---

# Code prose storage standard — review & sign-off (Jul 6 2026)

TRANSCRIPT-ONLY · 6 July 2026, 11:04 AM ET · ~54m. **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]].

**Purpose:** The booked review of the [[wiki/meetings/2026-07-02-code-prose-storage-standard.md|July-2 code-prose storage standard]] (which continued the [[wiki/meetings/2026-07-02-ris-prose-documentation-standard.md|July-2 RIS prose meeting]]). A scope misunderstanding surfaced at the top — Val expected to sign off a written *standard*, Andrei expected a full *implementation* — so Val reopened the discussion rather than cancel. Val walked the team through the "as-built" documentation method he ran himself on the RIS repo (prose → architectural clusters → reverse-engineered requirements → per-requirement acceptance criteria + tests), the tooling he used, and how it feeds a future new ARS. He confirmed the durable decision: **every repository must contain prose as a company standard**, versioned into the repo standard (5.1/5.2 → 6.0).

The durable substance lives on:
- **The "as-built" documentation standard, the reverse-engineered requirements/acceptance-criteria chain, repo-standard versioning, and Jira flagging** → [[wiki/topics/github-release-management-pipeline.md]] (Jul-6).
- **The Fable-5 + Claude-Code multi-agent tooling, prose/cluster/mermaid generation, the data-contract-equals-capability idea, and the MVP-first path to a new ARS** → [[wiki/topics/ai-assisted-development.md]] (Jul-6).

§15.8 clear — coding-standard, tooling and prose/requirements economics only; no named-person compensation.

## Sources

- [[raw/Meeting_Transcript_Code_Prose_Storage_Standard_Review-July-6-2026.md]]
