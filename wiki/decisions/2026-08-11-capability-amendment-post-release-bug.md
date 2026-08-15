---
type: decision
title: The "Capability Amendment" standard for treating post-release bugs
date: 2026-08-11
aliases: [Capability Amendment, capability amendment standard, post-release bug workflow, bug treatment workflow, fix branch workflow]
source-count: 2
status: active
open-commitments: 1
---

# The "Capability Amendment" standard for treating post-release bugs

On the [[wiki/meetings/2026-08-11-bug-treatment-workflow.md|Aug 11 2026 bug-treatment session]] ([[wiki/people/val-levitan.md|Val]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/andrey-bosik.md|Andrei Bosik]]) the team agreed and published the mechanism for bringing a **bug found after release** back into a product's already-closed feature hierarchy. It is the concrete follow-through on the Aug 4 principle that [[wiki/decisions/2026-08-04-bug-only-against-closed-feature.md|a bug only exists against a closed (released) feature and a closed capability is never reopened]]. Val's stated method is to publish one small standard at a time and accumulate them in a **Design Criteria folder in GitHub** that Claude reads. [[raw/Meeting_Notes_Bug_Treatment_Workflow-August-11-2026.md]]

## What was decided

- **Create a new item type, the "Capability Amendment."** When one or more confirmed bugs exist against a product whose Features and Key Capabilities are already closed (they leave the working view but stay in history and are never reopened), you open a **Capability Amendment** whose **version field holds the fix version**. It is a **new dedicated JIRA issue type**, made **visually distinct** from a normal Capability so it can be told apart and, where needed, **linked** to the closed capabilities. (Proposed by Dmitri Kovalchuk; accepted by Val and the group.) [[raw/Meeting_Notes_Bug_Treatment_Workflow-August-11-2026.md]]
- **Bugs hang under the Capability Amendment.** Under the amendment you attach the **bugs**, which take the place features normally hold. The fix item carries **issue type = Bug** (shown as a red icon rather than the purple Capability icon); if more work surfaces under a not-yet-closed amendment it is added as a Story/Feature under that fix branch, still typed as Bug. (Dmitri; agreed.) [[raw/Meeting_Notes_Bug_Treatment_Workflow-August-11-2026.md]]
- **The GitHub cycle per bug:** open a **fix branch** (Dmitri corrected Val that GitHub distinguishes a fix branch from a feature branch) → make the fix → raise a pull request → merge into main → deploy under that fix number → release. When done the fix branch is deleted and that version of the Capability Amendment is **closed**; if more bugs surface later, open a **new Capability Amendment version** and run the cycle again. [[raw/Meeting_Notes_Bug_Treatment_Workflow-August-11-2026.md]]
- **Ship as v1.0.** The standard ships as **v1.0** and can be revised to v1.1 / v2.0 once in use (Andrei's point). Dmitri committed to polishing the wording and publishing it to the Design Criteria folder **today** (he leaves on vacation tomorrow). [[raw/Meeting_Notes_Bug_Treatment_Workflow-August-11-2026.md]]

## Requirements & tests are part of the amendment

Creating a Capability Amendment should push the team to **open the Requirements**, review the acceptance criteria, **add new acceptance criteria** for the missed case, and **add test cases** that catch the bug. Either write a new narrow requirement or open an existing one and add to it (with a dated comment noting the bug that prompted the change) — both are allowed, and requirements can be **linked across capabilities**. Val suggested using **Claude** to find the requirement that best fits a bug and to help draft the acceptance criteria and test cases. [[raw/Meeting_Notes_Bug_Treatment_Workflow-August-11-2026.md]]

## Ticket roles

On the Customer Support Port ticket, **Creator cannot be changed** (e.g. Felipe, who raised it), **Reporter can be reassigned** (the person who owns/leads the item), and **Assignee** does the work. JIRA's creator field is not displayed, so the team repurposed the **Reporter** field to avoid paying for extra licenses; the bug itself later carries its own reporter and assignee. Triage items are auto-assigned or left unassigned, and the responsible person assigns themselves. [[raw/Meeting_Transcript_Bug_Treatment_Workflow-August-11-2026.md]]

## Open questions (ruled a separate future standard)

- **Branch-and-release management when main has moved ahead** — how to release only a small bugfix against an already-released/certified old version (e.g. a Georgia COAM build) without pulling in unrelated later changes: release from a tag/branch vs from main, how a tag relates to main, and whether old fix branches must keep living. Discussed at length (Pavel: release new products from main, but for a backfix to old certified software, branch from the released tag, make the small fix, tag it, and still merge the fix into main; Dmitri and Andrei worked through how a tag is a marked commit, not a slice of main). **Val explicitly ruled this a separate standard, to be published later — no decision today.** (Raised by Irina Shishko.) [[raw/Meeting_Notes_Bug_Treatment_Workflow-August-11-2026.md]]
- **Requirements fragmentation** — how to choose between reusing/amending an existing requirement and creating a new narrow one, so the requirement set stays a single source of truth; partially addressed (AI grooming to find the best-fit requirement) but flagged as an ongoing practice concern. (Irina Shishko.) [[raw/Meeting_Notes_Bug_Treatment_Workflow-August-11-2026.md]]

## Open commitments

- [ ] Dmitri Kovalchuk — polish the Capability Amendment standard v1.0, publish it to the Design Criteria folder in GitHub, and circulate it — due Aug 11 2026 (before his vacation) — [[raw/Meeting_Notes_Bug_Treatment_Workflow-August-11-2026.md]]

Related process context on [[wiki/topics/github-release-management-pipeline.md]] and the Aug-4 predecessor [[wiki/decisions/2026-08-04-bug-only-against-closed-feature.md]].

## Sources
- [[raw/Meeting_Notes_Bug_Treatment_Workflow-August-11-2026.md]]
- [[raw/Meeting_Transcript_Bug_Treatment_Workflow-August-11-2026.md]]
