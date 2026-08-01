# Meeting Summary — JIRA Hierarchy Standard

**Date:** June 16, 2026, 12:33 PM Eastern
**Duration:** ~1 hour 14 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko, Dmitri Kovalchuk, Andrei Bosik, Evgeny Kharetski (joined at ~12 min)

## Summary

The Minsk team had not resolved the capability lifecycle question from the prior day's session — specifically whether capabilities in JIRA should close after completion or live indefinitely. Val pushed for a decision.

**Hierarchy settled (top to bottom):**

- **Value Stream** — accounting line; where JVL earns or spends money. Already existed; not debated.
- **Initiative** — defines the final product and which services compose it. Example: Flex Recycler Family lives under Transaction Galaxy.
- **Capability** — what the system will be able to do by a target date. Must be scoped small enough to close within a planned release. The sum of closed capabilities determines the release point.
- **Project** — equals one Git repository, strictly 1:1. Projects are permanent buckets that never close. They exist in a separate dimension from the hierarchy — not nested under initiatives, but logically linked through capabilities and features.
- **Feature / Story / Sub-task** — lives inside projects; standard JIRA breakdown.

**Capability lifecycle resolved:** Capabilities close. Val reasoned that projects (repos) are continuously filled with code via CI/CD, capabilities close when their features are done, and the sum of closed capabilities within an initiative marks a release point. Adding an extra hierarchy level to keep capabilities alive indefinitely was rejected outright.

**Project = Repository, no exceptions.** Val rejected multi-repo projects and multi-project repos. Shared libraries get their own repo and JIRA project. Having many projects is preferable to ambiguous mappings — Val wants Claude Code to have clean, unambiguous mappings when working autonomously.

**Release mechanism:** Andrei presented a pipeline diagram (commit → PR → artifact → pre-release tag → integration testing → version matrix → release). The version matrix is formed once architecture is understood and capabilities are assigned to projects. JIRA's cross-space release feature shows releases as vertical lines on the timeline, with each release pulling in the relevant projects. Val wants release contents defined upfront — which capabilities and which repos — not left as a "blurred spot."

Irina showed two models for the hierarchy. Model A (capabilities as release-sized units that close) was selected over Model B (long-lived capabilities with an extra epic layer underneath).

## Decisions Made

- **Capabilities must close.** Scoped as release-sized units. No long-lived capabilities, no extra hierarchy level between capability and feature. (Decided by Val, supported by Pavel and Dmitri)
- **Project = Repository, 1:1 strictly.** Even small shared libraries get their own project and repo. (Decided by Val)
- **Hierarchy is: Value Stream → Initiative → Capability → [Project/Feature/Story/Sub-task].** Projects exist in a parallel dimension, linked through capabilities. (Team consensus, formalized by Val)
- **Release is defined by the sum of closed capabilities.** The set of projects serving an initiative determines which repos participate in the release. (Team consensus)
- **Model A adopted** from Irina's diagrams — capabilities close, no extra epic layer. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dmitri Kovalchuk | Write a new standard document for the JIRA hierarchy structure, based on Model A and this meeting's decisions. Consult with Andrei, Pavel, and Irina. Include a reference to Andrei's release/CI-CD standard at the ADR creation point. | Friday June 19, 2026 | High | Val wants this standard enforced going forward; replaces the old project structure |
| 2 | Andrei Bosik | Document the release pipeline/process diagram (commit → artifact → version matrix → release) as a formal standard, similar to how Standard 5.1 documented repository conventions | TBD | High | Val explicitly asked him to formalize what he presented; Dmitri's hierarchy standard will reference it |
| 3 | Val Levitan | Meet with Evgeny Kharetski to tie Claude Code autonomous development to the repo standard, CI/CD standard, and hierarchy standard that Dmitri will write | June 23, 2026 | High | Connecting autonomous AI coding workflows to the newly defined JIRA/Git structure |

## Open Questions

- How exactly will JIRA's cross-space release feature display release contents on the timeline? Pavel couldn't locate the full configuration during the meeting.
- How will the version matrix (Andrei's step 4) be maintained and linked back to JIRA — the GitHub-to-JIRA integration for release tracking was raised but not resolved.

---
*Processed from Teams transcript on June 16, 2026*
*Source meeting: Hierarchy_JIRA*