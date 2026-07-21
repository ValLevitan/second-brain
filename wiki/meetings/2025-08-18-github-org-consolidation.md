---
type: meeting
title: GitHub org consolidation discussion — Aug 18 2025 (4:30pm)
date: 2025-08-18
aliases: [Git organization management, GitHub org consolidation, one organization, org restructure]
source-count: 1
---

# GitHub org consolidation discussion — Aug 18 2025 (4:30pm)

**Date:** 2025-08-18 4:30pm · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrey-bosik.md|Andrei Bosik]] (DevOps), [[wiki/people/pavel.md|Pavel Frolov]]. A distinct Aug-18 GitHub meeting from the same day's [[wiki/meetings/2025-08-18-git-meta-analysis-repo.md|2:04pm meta-analysis check-in]] (different time, different participants, different topic). Russian.

Purpose: whether to **collapse JVL's several GitHub organizations into one (or very few)**. The substance and dated evolution of the multi-org→one-org shift live on the decision sequencer: [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]].

Key points captured there:
- Restructuring the org/repo layout "is not a problem"; the cost is that **many GitHub Actions must be rewritten** (cross-referencing actions especially — Andrei, Pavel, [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (transcribed "Tsyganov"), "Sasha").
- Timing: **wait ~1–2 weeks** until people are back from holiday (the person who wrote an action edits it fastest); "no panic," plan it into the schedule.
- **Admin model changes:** with fewer orgs, ownership consolidates to **Andrei, Dima, Val and Aaron**; Andrei alone would grant rights/permissions.
- Val's rationale: one org **streamlines** everyone (everyone sees all repos), and managing many orgs (separate link structures per org) is inconvenient for all — he began pulling management info from GitHub via Yandex(?) and found the multi-org setup awkward. "Кругом бегом" advisors even push for a **single** organization.
- Val re-asserts the **use-case-first task discipline**: "if there's no user story, there's no task" — refuses "floating tasks in the air," and asks the meeting recording be written up into a use case, then a requirement.
- Andrei/Pavel to meet the next day to define **correct org naming** and the migration mapping; largest orgs today are "Cortex"(?) and the gaming platform.

## Sources

- [[raw/Git_organization_management.md]]
