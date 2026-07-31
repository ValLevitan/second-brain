# Meeting Summary — Clayton MCP & JIRA Workflow (Call with Lena Zhukova)
**Date:** June 1, 2026, ~2:49 PM Eastern
**Duration:** ~11 minutes
**Attendees:** Val Levitan, Lena Zhukova

## Summary

**How Lena works with Michael.** There is no set meeting with Michael Gottlieb — they exchange text or call when needed. Michael sends review comments in Teams as text plus screenshots, often circling the areas he doesn't like, because written comments are clearer than verbal ones. Lena sorts his comments and passes developer comments to the developers and art comments to the responsible team member. Sometimes she has to go back to Michael — when he asks for something that can't fit the current release, she clarifies the technical details and pushes to defer it to the next release.

**Where Clayton MCP helps most.** Lena values Clayton MCP most at the start of a project. When Michael produces an abstract, the MCP analyzes the context, creates her issues, writes descriptions, and attaches images. She gave the new Georgia release as an example — about 8 games, each with roughly 15 compact images that must be attached to the right features and stories. Doing that by hand is a big stress at kickoff, and the MCP handles it very well. A good recent addition (built by Clayton) is that the MCP can now analyze the chat from their daily sync meetings and turn it into action items and issues.

**Where the savings are smaller.** Day to day, once the bulk of issues already exists, the Jira workload is much lighter and the time saved is marginal — including on review comments specifically. The heavy, high-value lift is at project start, not steady state. Attaching images during a project is spread out over days, so it is not a crunch.

**Two things the team wants from Clayton MCP next.**
1. **Status and timeline control.** Today the MCP can't move items on the timeline or change an issue's status (e.g., Action Item → In Progress, In Progress → Resolved). Lena, Julia, and Anastasiya all change statuses by hand (In Review → In Progress, In Review → Resolved, Resolved → Closed). Automating status changes would help all of them.
2. **Review-comment sorting (a later step).** Extend the MCP so that when Michael sends a list of review comments, it can read the relevant chat (e.g., for a given day), sort the comments, and suggest which Jira issue each belongs to. The MCP was originally built for daily-sync action items, not review comments, so this is new ground.

**Status changes today.** Whoever an issue is assigned to moves it from Action Item to In Progress when they start. The exception is Michael — he never changes statuses, so Lena closes and updates issues on his behalf.

**Recording practice.** Major issues are discussed by Lena, Anastasiya, Julia, and Dima. Calls with other members (Natalia, Arturo, Vitaliy) are occasional and not recorded — they are usually short clarifications, since stories are written to be clear enough on their own.

## Decisions Made

No formal decisions. The review-comment automation was framed as a future "next step," not a commitment. Val noted the day-to-day savings are marginal and the real value is concentrated at project start.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lena / Clayton | Ask Clayton whether the MCP can change issue status and move items on the timeline (Action Item → In Progress, In Progress → Resolved, etc.) | TBD | Normal | Would remove manual status changes for Lena, Julia, and Anastasiya |
| 2 | Lena / Clayton | Scope extending Clayton MCP to sort Michael's review comments from chat and suggest the target Jira issue | TBD | Low | Explicitly a later step; MCP was built for sync action items, not review comments |

## Open Questions

- Can Clayton MCP be extended to write issue status and timeline changes, or is that out of scope for the tool today? (Needs a conversation with Clayton.)
- Whether the review-comment workflow is worth automating, given the day-to-day savings are marginal.

---
*Processed from Teams transcript on June 1, 2026.*
*Source meeting: Call with Lena Zhukova — June 1, 2026.*
