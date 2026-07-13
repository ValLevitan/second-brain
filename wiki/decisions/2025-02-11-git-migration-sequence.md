---
type: decision
title: Git migration sequence — Omni/Miranda/FlexPay, then RGS, then map the rest
date: 2025-02-11
aliases: [repo migration order, Bitbucket to GitHub, SVN migration, repo inventory]
source-count: 1
status: active
---

# Git migration sequence — Omni/Miranda/FlexPay, then RGS, then map the rest

**Decision (Feb 11 2025, Val + Aaron + [[wiki/people/andrei.md|Andrei]] + [[wiki/people/pavel.md|Pavel]] + [[wiki/people/alexander-biratka.md|Alexander]] + [[wiki/people/efim-podvoiski.md|Efim Podvoiski]]):** JVL migrates its repositories into the new GitHub organizations in three stages. [[raw/Git_repo_structure_part_2_2025-02-11.md]] Depends on [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]].

## The three stages

1. **Omni, Miranda, and FlexPay** move first (from Bitbucket / SVN to GitHub). Miranda was already committed into Bitbucket by Dima; Omni to move immediately. Andrei estimated ~**1 hour** to create the orgs and move current repos. [[raw/Git_repo_structure_part_2_2025-02-11.md]]
2. **RGS** second — Efim's real production project, still in SVN, a multi-day job, so done as its own step. See [[wiki/topics/rgs-architecture-and-integration.md]]. [[raw/Git_repo_structure_part_2_2025-02-11.md]]
3. **Inventory and map everything else** — make a spreadsheet of all Git and all SVN repos with old name → new name → location, and migrate only the ones worth keeping (there had been "fast and loose" repo creation in Bitbucket). Bitbucket cleanup to be discussed in a separate meeting with the internal team. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## Sources

- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
