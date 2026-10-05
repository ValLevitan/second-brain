---
type: decision
title: A bug only exists against a closed (released) feature; never reopen a closed capability
date: 2026-08-04
aliases: [bug definition closed feature, never reopen a closed capability, released-product issue flow, bug documentation standard]
source-count: 3
status: active
---

# A bug only exists against a closed (released) feature; never reopen a closed capability

On the [[wiki/meetings/2026-08-04-bug-documentation-standard.md|Aug 4 2026 bug-documentation session]] ([[wiki/people/val-levitan.md|Val]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]) Val set the standard for how bugs are documented once a feature is already released. [[raw/Meeting_Notes_Bug_Documentation_Standard-August-4-2026.md]]

## What was decided

- **A bug only exists against a closed (released) feature.** Anything found while a feature is still in development is **not** a bug — it is a change of scope, handled by adding a new story, adding acceptance criteria, or adding a feature. A problem caught in pull-request review means the reviewer rejects the PR and the feature moves from "complete" back to "to-do." A feature is "complete and closed" only once its branch is merged to main. Val estimated roughly **75%** of real bugs trace back to acceptance criteria written wrong, interpreted wrong, or tests written wrong. [[raw/Meeting_Notes_Bug_Documentation_Standard-August-4-2026.md]] [[raw/Meeting_Transcript_Bug_Documentation_Standard-August-4-2026.md]]
- **Never reopen a closed capability or feature to fix a released bug** — reopening "breaks the history." Bug/incident work moves **up** to capability/feature level and issues are **linked, not parented**. [[raw/Meeting_Notes_Bug_Documentation_Standard-August-4-2026.md]]
- **The released-product issue flow:** a field/customer problem enters as a **Customer Support / service ticket** (creator = Felipe) → triage reclassifies it (e.g. to an **Incident**) → the incident sits at capability level → features (the actual bug work) open under it, grow a feature branch with the fix, merge to main → the service ticket closes with them. Nothing duplicate is created and nothing is reopened, so the full history of why the change happened is preserved. In GitHub the fix becomes a new feature branch with a bug/bugfix prefix that merges to main like any feature. [[raw/Meeting_Notes_Bug_Documentation_Standard-August-4-2026.md]]
- **Roles:** Creator equals Reporter by default and Creator cannot be changed, so Creator stays Felipe; Val wants the **Reporter** field reassigned to the responsible manager (Irina or Pavel); the issue-type field (service request vs incident) is set at triage by the responsible person, not by the reporter. [[raw/Meeting_Notes_Bug_Documentation_Standard-August-4-2026.md]]

*Considered and superseded:* Pavel's mid-meeting proposal to **clone the old capability** (a clone link tying old and new) was rejected by Val and replaced by the reclassified-ticket-at-capability-level flow above. (The meeting notes were themselves corrected on Aug 6 to remove the clone proposal from the decisions, per the final-state rule.) [[raw/Meeting_Notes_Bug_Documentation_Standard-August-4-2026.md]]

## Open items

- Integration tests that gate pull requests currently number **zero**; Pavel raised it and Val agreed every developer must push these in. [[raw/Meeting_Notes_Bug_Documentation_Standard-August-4-2026.md]]
- Val still needs the correct term for the triage role that reclassifies a service ticket (he lacked the word and will read up). [[raw/Meeting_Notes_Bug_Documentation_Standard-August-4-2026.md]]
- Val will refine the standard once more and reconvene the group. [[raw/Meeting_Notes_Bug_Documentation_Standard-August-4-2026.md]]

**Follow-through (Aug 11 2026):** the concrete mechanism for this flow — a new **"Capability Amendment"** item that holds the bugs and drives the fix-branch cycle — was agreed and published on [[wiki/decisions/2026-08-11-capability-amendment-post-release-bug.md]].

**Follow-through (Oct 1 2026):** the in-development half of the rule got its Jira transition at the [[wiki/meetings/2026-10-01-daily-standup-sas-mode-flag-and-feature-status-rules.md|Oct-1 Minsk stand-up]] — [[wiki/people/irina-shishko.md|Irina]]: "Пока ты разрабатываешь нет бага ты просто чтото не доработал. Поэтому стори"; the feature goes from Completed back to To Do, which [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] adds; nothing Closed is reopened. See [[wiki/decisions/2026-10-01-completed-is-the-developers-last-step-and-a-found-problem-sends-the-feature-from-completed-back-to-to-do-as-a-story.md]] [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].

Related process context on [[wiki/topics/github-release-management-pipeline.md]].

## Sources
- [[raw/Meeting_Notes_Bug_Documentation_Standard-August-4-2026.md]]
- [[raw/Meeting_Transcript_Bug_Documentation_Standard-August-4-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
