---
type: meeting
title: GitHub for the graphic-design team — Sergey's Git LFS pushback, refine-don't-rollback, learn-the-tool (Nov 20 2025)
date: 2025-11-20
aliases: [application of GitHub for graphic design team, Git LFS artists, reduce interaction surface, squash merges art repos, GitHub Desktop for artists, Sergey Kleimenychev git, learn the tool or cannot work for JVL]
source-count: 1
open-commitments: 2
---

# GitHub for the graphic-design team — Sergey's Git LFS pushback, refine-don't-rollback, learn-the-tool (Nov 20 2025)

**Date:** 2025-11-20 (recording header 2:05 PM) · **Duration:** 26m 14s · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/aaron.md|Aaron Bockelie]], [[wiki/people/sergey-kleimenychev.md|Sergey Kleimenychev]] (design generalist), [[wiki/people/andrey-bosik.md|Andrei Bosik]] (DevOps). English.

The next step in the graphics-team-on-Git thread — see [[wiki/topics/graphics-team-git-workflow.md]] (Nov-20 section) and the docs-as-code direction ([[wiki/topics/docs-as-code-and-atlassian-exit.md]]), continuing the earlier design-team decisions [[wiki/decisions/2025-02-21-separate-game-and-design-repos.md]] and [[wiki/decisions/2025-02-26-designer-branching-workflow.md]]. Val convened it to put Sergey (who had complained Git is bad for artists) in front of Aaron and Andrei — Val noted Sergey and Andrei sit on either side of a thin office wall but don't talk to or trust each other, so he hoped this would build Sergey's trust in Andrei. This is the meeting Val moved Aaron into straight after the [[wiki/meetings/2025-11-20-aaron-board-bringup-rockchip.md|1:32 PM board bring-up call]].

Durable points (single-source stub, all from [[raw/application of GitHub for graphic design team.md]]):

- **The decision is not reopened — GitHub was chosen for the company, not the artists.** Val was blunt: JVL chose **GitHub over SVN** because it gives the company overall improvement (integrity, security, conveniences), "not necessarily the best possible choice for graphic designers." Whoever works for JVL must learn the tool "or cannot work for the company." Sergey agreed there is no point rolling back — the decision was made; the work is to **refine how Git is used**, not switch back to SVN.
- **Sergey's beef and his proposals.** His original objection: Git needs **Git LFS** (a "duct-tape solution"), and he'd wrongly believed an LFS pull fetches *every* blob — realising LFS only pulls the current commit removed the main worry. His concrete proposals: (1) **reduce the interaction surface** — artists should clone/pull/push at the press of a button via **onboarding scripts and aliases**, never touching LFS setup manually (a missed `git lfs install` leaves you with blob pointers, not blobs — artists panic); (2) **squash merges** to keep a tidy history and let old big blobs be pruned (daily renders are ~1 GB/person/day); (3) explain the **stash + LFS** pitfall (an un-stash where LFS doesn't fire leaves pointers).
- **Aaron's counter — tools, monitoring, but no crutches.** Aaron agreed: keep Git + LFS, modify usage. Suggested **GitHub Desktop** (better for artists than VS Code, integrates LFS cleanly); Andrei to add **commit hooks / blocks** and **DevOps monitoring dashboards** (LFS space usage) plus scheduled cleanup of stale intermediary files. But he pushed back hard on "conveniences and crutches": the artists don't understand the consequences of their Git steps, and if scripts hide everything "no one will grow." Two sides of the coin — convenience tools *and* the ability to work without them; "do not let them be lazy."
- **Small team makes it tractable.** Only about **5 people** commit art assets — Sergey, "Nesta," "Eula," "Dima," plus at least one commissioned artist. Aaron: with such a small population everyone can support each other; define a set of guidelines/requirements collectively.
- **Ownership assigned.** Aaron framed the simplified artist Git flow as a **product** and asked who owns it "forever" — **Sergey** took it (for as long as he works at JVL). Val declined to buy any new tools ("it's not about additional tools — it's about setting up existing tools"); Sergey and Andrei are cleared to fiddle with the setup and estimate effort. Val asked to be CC'd on their discussions — he won't always reply but wants to bring expertise and keep the tool decisions company-level, not designer-level.

## Open commitments

- [ ] Sergey Kleimenychev — own and build the simplified artist Git flow (onboarding scripts/aliases, one-shot clone setup, squash-merge convention, stash/LFS guidance) with Andrei; teach the artists to actually understand Git rather than only give them shortcuts — due unspecified — [[raw/application of GitHub for graphic design team.md]]
- [ ] Andrei Bosik — set up (using existing tools, no new purchases) commit hooks/blocks, LFS-usage monitoring dashboards and scheduled cleanup of stale blobs; help Sergey define the artist flow — due unspecified — [[raw/application of GitHub for graphic design team.md]]

**§15.8:** clear — tooling/process content only; no compensation figures (Sergey's "if I get fired" aside carries none).

**Same-name / resolution notes (§4):** "**Dima**," named as more Git-aware among the art committers, is graphics/3D context → [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]] (Senior 3D Graphic Designer). "**Eula**" ≈ [[wiki/people/yulia.md|Yulia]] (art team). "**Nesta**" is unresolved — likely a garble of "Nastya"/[[wiki/people/anastasia.md|Anastasia]] (art team) but not forced; queued. [[wiki/people/andrey-bosik.md|Andrei Bosik]] (DevOps; registry spelling "Andrei Bosik") and [[wiki/people/aaron.md|Aaron Bockelie]] as usual.

## Sources

- [[raw/application of GitHub for graphic design team.md]]
