---
type: decision
title: Migrate Efim's codebase from SVN to Git first, then continue Hollywood Bets
date: 2025-03-17
aliases: [SVN to Git migration, reversing code into requirements, Hollywood Bets]
source-count: 1
status: active
---

# Migrate Efim's codebase from SVN to Git first, then continue Hollywood Bets

On the Mar 17 2025 call ([[wiki/people/val-levitan.md|Val]], [[wiki/people/aaron.md|Aaron]], [[wiki/people/efim-podvoiski.md|Efim Podvoiski]], [[wiki/people/igor-metelski.md|Igor Metelski]]), Val decided to **move the codebase Efim owns off SVN to Git before continuing the Hollywood Bets integration**. This is the concrete execution of the step-2 migration flagged back on Feb 11 (see [[wiki/decisions/2025-02-11-git-migration-sequence.md]]). [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]

## What was decided

- **Git first, then Hollywood Bets.** Val's ruling: "definitely move it to Git first, and then move on with Hollywood Bets" — doing the integration work *in* Git is good practice that builds the team's Git experience. He estimated the switch "should not be more than five days." [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]
- **The goal is understanding, not rewriting.** Aaron framed the initiative as static analysis + documentation to *understand* the code (not change the source), improving its commercial viability, enabling faster integration work, and reducing the bus-factor risk that only Efim and Igor can work on it. [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]
- **Staged Jenkins→GitHub migration:** stage 1 — move the codebase to Git; stage 1.5 — repoint Jenkins at the Git repo instead of SVN (possibly the fastest way to keep building); stage 2 — rip-and-replace: recreate the Jenkins recipes as **GitHub Actions** (initially "black-boxed" — a container that just runs the existing build scripts), then fully divorce from Jenkins and SVN. Later stages are optional / done only where active. [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]
- **Ownership and timing:** the bulk of the migration work falls to [[wiki/people/andrey-bosik.md|Andrei Bosik]]; Igor Metelski is on vacation until the following Monday (week of the 24th), so Efim is to prioritise it that week. Val booked himself to check back on **Mar 31**. [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]

## Context / rationale

- Efim's concern was disruption: the current Hollywood Bets integration is due ~end of April, and switching source systems could leave ~5 days where the Jenkins builders (which pull from SVN) can't build. Val judged this not painful, citing that "Ratko" (name unclear) had moved his entire **Omni** to Git with little issue. [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]
- Current build setup: dozens of applications are built individually from this codebase on **Jenkins** and deployed automatically to dev/test cloud environments (not prod). [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]

## Sources

- [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]
