# Meeting Summary — Bug treatment: how a customer problem becomes a shipped fix
**Date:** August 11, 2026, 7:00–8:38 AM Eastern
**Duration:** ~1 hour 39 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko, Dmitri Kovalchuk, Andrei Bosik
**Raw transcript:** [[Meeting_Transcript_Bug_Treatment_Workflow-August-11-2026]]

## Summary

The meeting was held in Russian; this summary is in English. It followed on from the August 4 "Bug Documentation Standard" work. Val had circulated a short document proposing a standard for what to do with a bug found *after* a product is released, and the goal of the meeting was to agree that one standard and publish it — nothing more.

**The situation the standard covers.** When a product ships, all of its Features and Key Capabilities are closed and are never reopened; they leave the working view but stay in history. Requirements are different — they live on, are reused, are not part of the closed hierarchy, and each one is a narrow statement of quality for a capability. After release (or during internal testing), someone like Felipe finds something that looks wrong and files a Customer Support Port ticket describing it, not yet knowing what it is. QA triages the ticket — opens it, tries to reproduce it, and reclassifies it, for example as a bug. The question the standard answers: once you have one or more confirmed bugs against a product whose features and capabilities are already closed, how do you bring that work back into the hierarchy?

**Val's proposal (what was adopted).** Create a new item called a **Capability Amendment**. Its version field holds the fix version. Under the Capability Amendment you attach the **bugs**, which take the place features normally hold. For each bug you open a **fix branch** in GitHub (Dmitri corrected Val that GitHub distinguishes a fix branch from a feature branch), make the fix, raise a pull request, merge it into main, deploy under that fix number, and release. When done, the fix branch is deleted and that version of the Capability Amendment is closed. If more bugs surface later, open a new Capability Amendment version and run the cycle again.

**Requirements and tests.** Creating a Capability Amendment should push the team to open the Requirements, review the acceptance criteria, add new acceptance criteria for the case that was missed, and add test cases that catch the bug. Either write a new narrow requirement for the amendment, or open an existing requirement and add to it (with a comment noting the date and the bug that prompted the change) — both are allowed, and requirements can be linked across capabilities. Val suggested using Claude to find the requirement that best fits a bug and to help draft the acceptance criteria and test cases.

**Ticket roles.** On the Customer Support Port ticket, "Creator" cannot be changed (e.g. Felipe, who raised it), "Reporter" can be reassigned (the person who owns/leads the item), and "Assignee" does the work. JIRA has a creator field that is not displayed; the team repurposed the Reporter field to avoid paying for extra licenses. The bug itself later carries its own reporter and assignee. Triage items are auto-assigned or left unassigned, and the responsible person then assigns themselves.

**Scope discipline.** Val repeatedly steered the group back to publishing only this one standard today, deferring a broader branch-and-release question that Irina raised (see Open Questions). His stated method is to move in micro-steps, publish one standard at a time, and accumulate them in a Design Criteria folder in GitHub that Claude reads.

## Decisions Made

- **Adopt the "Capability Amendment" standard (v1.0)** for treating post-release bugs, as described above. (Decided by Val; agreed by all. Andrei noted it ships as v1.0 and can be revised to v1.1/2.0 once in use.)
- **"Capability Amendment" becomes a new dedicated JIRA issue type**, visually distinct from a normal Capability, so it can be told apart and, where needed, linked to closed capabilities. (Proposed by Dmitri Kovalchuk; accepted by Val and the group.)
- **The fix item under a Capability Amendment carries issue type = Bug** (raised to the correct hierarchy level so the type can be set; shows as a red icon instead of purple). If more work is found under a not-yet-closed amendment, it is added as a Story/Feature under that fix branch, still typed as Bug. (Dmitri; agreed.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dmitri Kovalchuk | Polish the wording of the Capability Amendment standard v1.0, publish it to the Design Criteria folder in GitHub, and circulate it to the group | August 11, 2026 (today) | High | Dmitri leaves on vacation tomorrow and committed to finishing it today |

## Open Questions

- **Branch and release management when main has moved ahead** — how to release only a small bugfix against an already-released/certified old version (e.g. a Georgia COAM build) without pulling in unrelated later changes: release from a tag/branch versus from main, how a tag relates to main, and whether old fix branches must keep living. Discussed at length (Pavel: release new products from main, but for a backfix to old certified software branch from the released tag, make the small fix, tag it, and still merge the fix into main; Dmitri and Andrei worked through how a tag is a marked commit, not a slice of main). Val explicitly ruled this a separate standard to be discussed and published later — no decision today. (Raised by Irina Shishko.)
- **Requirements fragmentation** — how to decide between reusing/amending an existing requirement and creating a new narrow one, so the requirement set stays a single source of truth. Partially addressed (use AI grooming to find the best-fit requirement) but flagged as an ongoing practice concern. (Irina Shishko.)

## Dispatch Log

---
*Processed from Teams transcript on August 11, 2026 (scheduled meeting-watcher run)*
*Source meeting: Bug treatment: how a customer problem becomes a shipped fix*
