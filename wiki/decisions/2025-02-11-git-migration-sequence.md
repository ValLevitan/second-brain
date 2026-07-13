---
type: decision
title: Git migration sequence — Omni/Miranda/FlexPay, then RGS, then map the rest
date: 2025-02-11
aliases: [repo migration order, Bitbucket to GitHub, SVN migration, repo inventory]
source-count: 4
status: active
---

# Git migration sequence — Omni/Miranda/FlexPay, then RGS, then map the rest

**Decision (Feb 11 2025, Val + Aaron + [[wiki/people/andrey-bosik.md|Andrei]] + [[wiki/people/pavel.md|Pavel]] + [[wiki/people/alexander-biratka.md|Alexander]] + [[wiki/people/efim-podvoiski.md|Efim Podvoiski]]):** JVL migrates its repositories into the new GitHub organizations in three stages. [[raw/Git_repo_structure_part_2_2025-02-11.md]] Depends on [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]].

## The three stages

1. **Omni, Miranda, and FlexPay** move first (from Bitbucket / SVN to GitHub). Miranda was already committed into Bitbucket by Dima; Omni to move immediately. Andrei estimated ~**1 hour** to create the orgs and move current repos. [[raw/Git_repo_structure_part_2_2025-02-11.md]]
2. **RGS** second — Efim's real production project, still in SVN, a multi-day job, so done as its own step. See [[wiki/topics/rgs-architecture-and-integration.md]]. [[raw/Git_repo_structure_part_2_2025-02-11.md]]
3. **Inventory and map everything else** — make a spreadsheet of all Git and all SVN repos with old name → new name → location, and migrate only the ones worth keeping (there had been "fast and loose" repo creation in Bitbucket). Bitbucket cleanup to be discussed in a separate meeting with the internal team. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## Execution note (Feb 18–26)

- **Feb 18:** onboarding of the **graphics department to Git + Git LFS** began: Aaron ran a hands-on VS Code / Copilot / LFS session for [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]], with Andrei to set up [[wiki/people/lena.md|Lena]] and write a handout so the rest of the graphics team can commit large assets themselves. See [[wiki/meetings/2025-02-18-git-lfs-vscode-onboarding.md]]. [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- **Feb 21:** the LFS work produced the game-repo/design-repo split (comp art → LFS design repo via submodule; build doesn't need it — see [[wiki/decisions/2025-02-21-separate-game-and-design-repos.md]]), and Dima Khandov wrote the artists' onboarding instructions (Russian→English) to put Nastia/Julia onto GitHub. Confluence content for Fortune Foo Paws was exported into an initial GitHub docs branch (see [[wiki/topics/docs-as-code-and-atlassian-exit.md]]). [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- **Feb 26:** the design team was coached on the branching workflow ([[wiki/decisions/2025-02-26-designer-branching-workflow.md]]); two new orgs (**Game Concepts**, **Game Designs**) were added to the structure; Juan/Michael are held out ~30 days until the core four designers are comfortable. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

## Sources

- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
