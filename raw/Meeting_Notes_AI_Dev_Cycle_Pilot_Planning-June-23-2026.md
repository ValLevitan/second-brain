# Meeting Summary — AI Dev Cycle Pilot Planning
**Date:** June 23, 2026, 10:04 AM Eastern
**Duration:** ~1h 31m
**Attendees:** Val Levitan, Pavel Frolov, Evgeny Kharetski, Irina Shishko, Andrei Bosik
**Initiative:** [[Development and Release Processes and Procedures]]

## Summary

Val opened the meeting noting that two planned topics — JIRA hierarchy and Claude Code integration — overlap, and that's fine.

**Evgeny's current AI workflow.** Evgeny described how he works today: he takes a JIRA feature ticket (e.g., LGS-1050), creates a feature branch, and uses Claude with hooks for automated status transitions. He stores all Claude session history and coding mistakes in Obsidian, which feeds a self-learning code review system — Claude checks past gaps before writing new code. He's building toward an autonomous setup: one orchestrator agent monitors JIRA for tasks in "To Do" status, delegates them to specialized sub-agents, and no commits happen without his review. The main tooling gap is managing multiple loops across repos — closing a terminal kills the loop, and restarting 10 loops manually is painful.

**Testing and acceptance criteria.** Val pressed on how acceptance criteria from requirements translate into tests. Evgeny admitted this is still theoretical — he hasn't yet built the flow where an agent writes tests based on acceptance criteria. The team agreed the target state is: agent takes a feature, writes both code and unit/integration tests based on acceptance criteria, then reports for human review before the PR is created. Pavel argued AI-written end-to-end tests should run from an independent session with no access to the dev's conversation history, using only JIRA tasks and repo code as source of truth. Andrei supported separating dev and QA roles even with AI — a developer's AI may repeat the developer's blind spots.

**JIRA hierarchy.** The team walked through the structure: Capability (business-level, written by product) → Features (implementation work in repos) → Requirements (with acceptance criteria). Features link to requirements via "required by" link type. A capability is closed when all its features are done and end-to-end tests pass against the acceptance criteria. Val said he still doesn't see the full cycle clearly and suspects the team is also not fully certain.

**Pilot experiment.** Val pushed hard: he needs to see one full cycle run end-to-end before investing more effort in JIRA restructuring or GitHub migration. Evgeny proposed a trivial sandbox test (a yellow button). Pavel proposed using Flex Recycler instead — it already has capabilities and features in JIRA. They settled on Flex Recycler PoS: add a small visual feature (modem settings tab), write the requirements and acceptance criteria, implement it with AI agents, write end-to-end tests with AI, and release it. Val: "When this cycle works, we'll know how JIRA hierarchy should look, and then we can justify moving Raid Studio to GitHub."

## Decisions Made

- **Pilot on Flex Recycler, not a sandbox.** Real project with existing JIRA structure gives a more meaningful test. (Val, Pavel)
- **Small scope for the pilot.** Add a modem settings tab (or similar small visual feature) to Flex Recycler PoS — enough to touch front-end and back-end, easy to test visually. (Val, Pavel)
- **AI-written tests must use independent session.** No access to the developer's Claude conversation history — only JIRA tasks and repo code. Prevents the AI from repeating the developer's mistakes. (Pavel, Val)
- **Evgeny's white-label experiment deprioritized.** The pilot overlaps with that work; pilot takes precedence. (Evgeny)
- **Dima meeting moved to 9:00 AM** on June 23. (Pavel — confirmed done during call)

## Undertakings

| # | Who | What | By When | Priority | Status |
|---|-----|------|---------|----------|--------|
| 1 | ~~Pavel Frolov~~ Val | ~~Organize internal meeting~~ → Val scheduled "Flex_Recycler_pilot_release_schedule" for Thu June 25, 8:00–9:00 AM ET (Teams) with Pavel Frolov, Irina Shishko, Genadi Peari, Andrei Klimovich | June 25 | High | ✔ Scheduled |
| 2 | Pavel Frolov | Send Val a calendar invite for the Tuesday follow-up demo | June 24 | Normal | Open |
| 3 | Pavel, Irina, team | Run the pilot: pick a small capability on Flex Recycler PoS, implement + test through the full AI-driven cycle, and show results to Val | June 30 | High | Open |

## Open Questions

- How exactly should end-to-end tests be triggered when multiple repos contribute to one capability? Evgeny suggested collecting all PRs for a capability's features, then running tests against the combined set. Not resolved.
- Who operates the AI session for end-to-end test writing — a developer or QA? Val leaned toward the developer; Andrei and Pavel argued for separation. Deferred to the pilot to test in practice.
- What tooling is needed to manage multiple Claude loops across repos? Evgeny flagged the gap but no solution was decided.

---
*Processed from Teams transcript on June 24, 2026*
*Source meeting: Claude Code Integration with JIRA Hierarchy & Repo Standards*
