---
type: decision
title: Migrate Efim's codebase from SVN to Git first, then continue Hollywood Bets
date: 2025-03-17
aliases: [SVN to Git migration, reversing code into requirements, Hollywood Bets, MathEngine repos, checkout all batch file]
source-count: 3
status: active
open-commitments: 1
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

## Progress — Mar 31 working session

On Mar 31 (the check-back Val booked on Mar 17) Aaron ran a working session with Val, [[wiki/people/igor-metelski.md|Igor Metelski]] and [[wiki/people/efim-podvoiski.md|Efim]] — see [[wiki/meetings/2025-03-31-rgs-git-migration-working-session.md]]. [[raw/rgs_git_migration-march-31-2025.md]]

- **RGS was cloned to Git that day** ("this one that we cloned today for RGS"), but its batch files reference loading external SVN pieces to build — "We are in the process now of making RGS whole on GitHub." [[raw/rgs_git_migration-march-31-2025.md]]
- **Repo mapping plan:** the SVN `Checkout All` batch file shows which SVN branches must become their own git repos — Aaron read off that one branch "will become its own git repo called MathEngine" and another "MathEngine External, and so forth"; he judged "at least these three branches in SVN will be additional git repos." Then git **submodules** defined inside RGS would recursively clone them, "eliminating the need to have this checkout all batch file at all." Aaron: rewriting the batch file for git is "literally 90% of the way there to just defining submodules anyway." [[raw/rgs_git_migration-march-31-2025.md]]
- **Build sequence:** first make it build fully **locally on a workstation** (Efim: "this builds on Windows right now" — Windows or Linux both acceptable to Aaron), verify all pieces exist, "pinch it into a singularity" on a dev workstation off Jenkins/SVN, then push back into GitHub as a functional piece. [[raw/rgs_git_migration-march-31-2025.md]]
- **Linux limitation:** Efim: building the math servers under Linux is blocked — "we don't have the binaries for Linux to build. We use source code to build mass servers" — and the math-engine source is access-restricted (see his page). The team starts with Windows, "as we used to do." [[raw/rgs_git_migration-march-31-2025.md]]
- **Ownership:** Aaron assigned Igor to "work with Andre and Afim" ([[wiki/people/andrey-bosik.md|Andrey Bosik]] + Efim) to map the remaining SVN repos over to git; Efim confirmed the parts visible in the batch file "we can easily migrate." [[raw/rgs_git_migration-march-31-2025.md]]
- **Deadline slip:** Igor "is afraid that he won't be ready for tomorrow," so the check-in moved to **Wednesday**. [[raw/rgs_git_migration-march-31-2025.md]]

## Progress — Apr 8 repo tour (submodules landed)

By Apr 8 the RGS repository was on GitHub with the plan above realised: [[wiki/people/andrey-bosik.md|Andrei Bosik]] gave Val a repo tour ([[wiki/meetings/2025-04-08-rgs-repository-structure-walkthrough.md]]) showing the **math artifacts migrated from SVN into the `External` folder and pulled in as git submodules** (`.gitmodules`), LFS configured via `.gitattributes`, and the ~15 microservice apps under `source`. Both build paths work — local Visual Studio and Jenkins. Full folder breakdown on [[wiki/topics/rgs-architecture-and-integration.md]]. [[raw/rgs_structure_github-april-8-2025.md]]

## Open commitments

- [ ] Igor Metelski — start an engineer's/discovery/findings log describing what it took to get the RGS to build correctly on a workstation — due Wednesday (moved from "tomorrow") — [[raw/rgs_git_migration-march-31-2025.md]]

## Sources

- [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]
- [[raw/rgs_git_migration-march-31-2025.md]]
- [[raw/rgs_structure_github-april-8-2025.md]]
