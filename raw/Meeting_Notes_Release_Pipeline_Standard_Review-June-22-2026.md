# Meeting Summary — Review: Release Pipeline Standard (Andrei)
**Date:** June 22, 2026, 10:01 AM Eastern
**Duration:** ~1 hour 16 minutes
**Segment:** Segment 1 of 2
**Attendees:** Val Levitan, Andrei Bosik, Irina Shishko, Pavel Frolov, Evgeny Kharetski

## Summary

Andrei presented his 5-stage release pipeline standard covering the path from commit to production deployment.

**Stage 1 — Feature branch.** Developer works in a feature branch. Pushes to the branch trigger no automated tests (revised from original — unit tests moved to Stage 2).

**Stage 2 — Pull request to main.** When a PR is opened: unit tests, contract tests (a subset of integration testing), security scans, and Claude code review run automatically. Additional commits to the PR re-trigger all checks. Linting was discussed — the team agreed it's a non-issue in practice since developers already check their code compiles before pushing.

**Stage 3 — Pre-release / Integration testing.** The biggest debate. Andrei originally had end-to-end tests running after merge to main. Evgeny argued strongly that code must not reach main until all tests pass — broken code in main creates messy rollback situations. The group agreed in principle but could not resolve the cross-service coordination problem: when two services need simultaneous contract changes, how do you test them together before either is merged? Pavel suggested testing against mock services at Stage 2, then doing real integration at Stage 3 using specific branches from both repos. Evgeny noted that services typically ship sequentially, not simultaneously, making coordination harder. This was left as an open research question for everyone.

**Stage 4 — Release.** A version matrix is formed listing the release tag of each artifact in the platform. Each release creates a new matrix file (not overwritten) so you can always see what versions were compatible at any point in time. Release notes auto-generate when the matrix is complete.

**Stage 5 — Deployment.** Only the integration repository can deploy to production. Individual artifact repos cannot deploy directly — this is a security constraint. The release manager triggers deployment from the integration repo, which dispatches build actions to each artifact's repo.

**Versioning** was a recurring side-topic. The team previously agreed on a 4-segment version (major.minor.patch.build). Andrei prefers 3 segments. No resolution — a versioning standard needs to be written, likely as a subsection of the release standard.

**Linking Jira to GitHub release numbers** came up: Val wants to mark a future release date in Jira with a version number, but GitHub assigns version numbers dynamically. No one had an answer. Evgeny suggested using GitHub milestones to bridge the two. Left open.

**Standards consolidation.** The team has accumulated several standards in different places (Sasha's repo standard, Dima's Jira standard, Andrei's testing diagram, this release standard). Andrei will consolidate everything into the "knowledge" repository and share the link. Val wants standards published with version numbers: ADR standard as v0.5 (based on Pavel/Sarah's template), Dima's Jira standard at ~v2.

## Decisions Made

- **Production deploys only from the integration repository** — individual artifact repos cannot deploy to prod, even accidentally. (Decided by Andrei, confirmed by group)
- **Unit tests run at PR stage, not on branch push** — developers may push incomplete work to branches. (Decided by Evgeny, confirmed by group)
- **Version matrix stored as separate files per release** — not overwritten, so history is preserved. (Decided by Andrei, confirmed by Pavel)
- **All standards consolidated into the "knowledge" repository** — single source of truth for team standards. (Decided by Val and Andrei)
- **ADR standard to be published as v0.5** — based on Pavel/Sarah's existing template. (Decided by Val)
- **Dima's Jira standard to be published at ~v2** — it's already well-discussed. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Update the release pipeline diagram based on today's feedback. Post both the current version and the updated version to the meeting chat. | TBD | High | Val wants both versions in the chat alongside the transcript for full traceability |
| 2 | Andrei Bosik | Add versioning rules (3-or-4-segment scheme, when to bump each segment) as a subsection of the release standard | TBD | Normal | No versioning standard exists yet; team cannot resolve numbering questions without one |
| 3 | Andrei Bosik | Consolidate all existing standards (Sasha's repo standard, Dima's Jira standard, release pipeline, testing diagrams) into the "knowledge" repository and share the link with the team | TBD | High | Standards are currently scattered across different repos; agents and team need a single reference point |
| 4 | Andrei Bosik, Evgeny Kharetski, Irina Shishko, Pavel Frolov | Research the cross-service integration testing problem independently — consult AI, think through approaches — then reconvene to consolidate into a unified solution | Before next meeting | High | Key unresolved question: how to test two services with simultaneous contract changes before either merges to main |
| 5 | Dima [not present — relay needed] | Publish his Jira hierarchy standard under a version number (~v2) into the knowledge repository | TBD | Normal | Val wants all existing standards versioned and centralized |

## Open Questions

- **When exactly do cross-service integration tests run relative to merge-to-main?** The group agrees broken code should not reach main, but the mechanism for coordinating multi-repo contract changes is unresolved. Everyone to research independently.
- **How to link Jira release versions to future GitHub release numbers?** Val wants to plan releases by date in Jira but doesn't know how to pre-assign the version number that GitHub will generate. Evgeny suggested milestones; no decision made.
- **3-segment or 4-segment version numbers?** Andrei prefers 3 (major.middle.minor). Aaron previously proposed 4 (major.minor.patch.build). Val likes the 4th segment for bugfixes. No resolution — pending the versioning standard.

---
*Processed from Teams transcript on June 22, 2026*
*Source meeting: Review: Release Pipeline Standard (Andrei) — Segment 1*
