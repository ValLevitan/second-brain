# Meeting Summary — Bug Documentation Process for Closed Features
**Date:** August 4, 2026, 9:04 AM Eastern
**Duration:** ~1 hour 37 minutes
**Attendees:** Val Levitan, Irina Shishko, Pavel Frolov, Dmitri Kovalchuk
**Raw transcript:** [[Meeting_Transcript_Bug_Documentation_Standard-August-4-2026]]

## Summary

Val called the team to agree on, write down, and publish a standard for how bugs get documented and tracked once a feature is already released — and to build a light QA process around it. The conversation was conducted in Russian and stayed at the level of process and Jira/GitHub structure, not code.

**What counts as a bug.** Val drew a firm line: a *bug* only exists against a **closed (released) feature**. Anything found while a feature is still in development is not a bug — it is a change of scope, handled by adding a new story, adding acceptance criteria, or adding a feature. If a problem surfaces during pull-request review, the reviewer rejects the PR and pushes it back to the developer; the feature moves from "complete" back to "to-do." A feature is only "complete and closed" once its branch is merged to main, and reopening a closed feature is not allowed. Val estimated roughly 75% of real bugs trace back to acceptance criteria that were written wrong, interpreted wrong, or to tests written wrong.

**Where a bug lives in the hierarchy.** Today a bug is a child of its feature (feature = parent). The group worked toward moving bug/incident work up to capability/feature level instead, linking issues rather than parenting them. Val was strongly against reopening a closed capability to fix a released bug — that "breaks the history." Pavel proposed cloning the old capability (a clone link tying old and new) as an interim mechanism, but it did not survive the meeting: when the team recapped the agreement as cloning, Val rejected it and counter-proposed the flow the group settled on — the Customer Support ticket itself, reclassified at triage, stands at capability level, so nothing new is created and nothing is reopened. In GitHub the bug becomes a new feature branch with a bug/bugfix prefix that merges into main like any feature.

**The agreed flow for a released-product problem.** A field/customer problem enters as a **Customer Support / service ticket** (creator = Felipe/Filippo). Triage then reclassifies it — for example to an **Incident** (the Customer Support space already shows red incident icons). The incident sits at capability level; features (the actual bug work) open under it, grow a feature branch containing the fix, merge to main, and the service ticket closes with them. The point Val kept stressing: this creates nothing duplicate, reopens nothing, and preserves the full history of why the change happened and why there is a new fix version.

**Fields.** Dmitri reported the bug standard doc already has all the fields except Root Cause (easy to add) and Acceptance Criteria (folded into Description). Pavel flagged that Fix Version is missing and should be set at triage; the group treated fix location as a resolution-time field.

**Roles.** Creator equals Reporter by default and the Creator cannot be changed — so Creator stays Felipe. Val wants the Reporter field reassigned to the responsible manager (Irina or Pavel), matching how other Jira projects work. The issue-type field (service request vs incident) is set during triage by the responsible person, not by the reporter; the current default is a green "service request."

**Loose ends raised.** Integration tests that gate pull requests currently number zero — Pavel raised it and Val agreed every developer needs to push these in. There is also a housekeeping concern that unparented service issues will "float" at the bottom of the plan, so the Customer Support project needs ordering.

Val closed by saying he will refine the standard once more and reconvene the group.

## Decisions Made

- **A bug only exists against a closed/released feature.** Problems found while a feature is still open are scope changes (new story / new acceptance criteria / new feature), not bugs. (Val; team broadly agreed.)
- **Never reopen a closed capability or feature to fix a released bug.** The reclassified Customer Support ticket (Incident) stands at capability level and the fix work opens under it — nothing new is created, nothing is reopened, history is preserved. (Val, firmly.) *Considered and superseded:* Pavel's clone-the-capability mechanism, proposed mid-meeting and replaced by this flow.
- **Released-product issues flow: Customer Support ticket → triage reclassifies (e.g. Incident) → incident sits at capability level → features/bug work open under it → feature branch with fix → merge to main → ticket closes.** (Reached jointly; Val to codify.)
- **Bug/incident work moves up to feature/capability level rather than staying a child of the original feature; issues are linked, not parented.**
- **Reporter is reassigned to the responsible manager (Irina/Pavel); Creator stays Felipe; issue type is set at triage, not by the reporter.**

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Add this meeting's transcript into the bug-documentation standard document | TBD | Normal | Val named this explicitly as the meeting's undertaking |
| 2 | Val | Refine ("massage") the standard once more, then reconvene the group to review it | TBD | Normal | Closing action; team to let their own ideas settle before the next session |
| 3 | Val | Find the correct term for the triage role that reclassifies a service ticket | TBD | Low | Val lacked the word; will read up and report back |
| 4 | Dmitri / Jira admin | Change the Customer Support workflow so the issue type can be reclassified (e.g. to Incident) after triage | TBD | Normal | Dmitri confirmed "we can change it"; type currently defaults to green service request |
| 5 | Team (standard doc) | Add "Fix Version" field (flagged missing by Pavel) and Root Cause field to the bug standard | TBD | Normal | Fix Version set at triage; Root Cause "easy to add" per Val |
| 6 | Pavel / dev team | Establish integration tests that gate pull requests (currently zero) | TBD | Normal | Every developer to push these in |

## Open Questions

- What is the correct name/role for the person who performs triage assignment on a Customer Support ticket? (Val to look up.)
- How to keep unparented service issues from cluttering the plan (they float at the bottom) — ordering the Customer Support project. (Irina/Pavel.)
- Should Fix Version be captured at triage or only at resolution? (Raised by Pavel; leaning triage.)

## Dispatch Log

---
*Processed from Teams transcript on August 4, 2026, 12:10 PM Eastern*
*Source meeting: Bug Documentation Process for Closed Features*
*Corrected August 6, 2026: superseded clone-the-capability proposal removed from Decisions per the final-state rule (Error Journal 2026-08-06).*
