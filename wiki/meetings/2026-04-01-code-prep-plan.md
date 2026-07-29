---
type: meeting
title: Code Prep Plan (Apr 1 2026)
date: 2026-04-01
aliases: [Code Prep Plan, Observability Platform code cleanup, Back Office cleanup]
source-count: 2
---

# Code Prep Plan (Apr 1 2026)

Short (~14 min) Russian-language planning call — [[wiki/people/val-levitan.md|Val]] with [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (transcript "Dzmitry Chudzinau"), [[wiki/people/andrey-bosik.md|Andrei Bosik]] and [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (transcript "Sergey Tsimanov") — to agree a plan for cleaning up and documenting the **Observability Platform** codebase (formerly "Back Office", now migrated to GitHub) so it can be worked with **Claude Code**, ahead of a later architecture migration. [[raw/Meeting_Transcript_Code_Prep_Plan-April-1-2026.md]] [[raw/Meeting_Notes_Code_Prep_Plan-April-1-2026.md]]

The plan: a "semi-contract" reserving **2 hours/day** uninterrupted per developer for the cleanup, an estimated **30–45 days**, and a decision to **document everything including deprecated legacy modules** (e.g. an unused "Italy" feature) rather than skip them, marking dead code for deletion. Val rejected tracking the effort in Jira, asking [[wiki/people/andrey-bosik.md|Andrei]] to build a visual repository-progress report instead; the "Azure architecture" review was renamed "optimized architecture" and deferred ~30 days pending Docker/PostgreSQL feasibility answers. Substance on [[wiki/topics/ai-assisted-development.md]] and [[wiki/topics/github-release-management-pipeline.md]] (Apr-1).

## Sources

- [[raw/Meeting_Transcript_Code_Prep_Plan-April-1-2026.md]]
- [[raw/Meeting_Notes_Code_Prep_Plan-April-1-2026.md]]
