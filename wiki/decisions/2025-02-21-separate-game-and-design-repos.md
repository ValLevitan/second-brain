---
type: decision
title: Split each game into a "game" repo and a "design" repo (composition art via LFS + submodule)
date: 2025-02-21
aliases: [game repo, design repo, comp art repo, composition art repository, git submodule, two repos per game]
source-count: 2
status: active
---

# Split each game into a "game" repo and a "design" repo

**Decision (Feb 21 2025, [[wiki/people/aaron.md|Aaron]] proposing, [[wiki/people/val-levitan.md|Val]] + [[wiki/people/lena.md|Lena]] + [[wiki/people/andrey-bosik.md|Andrei (Bosik)]] + [[wiki/people/dmitriy-khandov.md|Dima Khandov]]):** each game gets **two repositories**, not one — a **game** repo and a **design** repo (e.g. "Fortune Foo Paws game" and "Fortune Foo Paws design"). [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]

## Why two repos

- Lena raised that the large **composition-art ("comp art") files** are big, numerous, and change rarely, and that Git cannot diff them — committing them into the game repo would slow the game build, because comp art is not a build asset. She needed a dedicated place to commit them and rules on how often / how large. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- Aaron's answer: put the big Git-LFS composition-art files in the **design** repo (a reference store), and keep the **game** repo clean for development work. The game repo can pull the design repo in as a **git submodule** for the full package, so someone who wants everything can `clone --recursive` and grab the comp art too; normally nobody clones the submodule to do game-development work. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- **The build does not need the composition art.** Aaron declined to decide this unilaterally and asked Andrei to check with [[wiki/people/alexander-biratka.md|Sasha]]; the answer was that building the full game does **not** require the composition-art repo to be included. That confirmed the split. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]

## Naming and layout

- The two repos are simply named **"game"** and **"design"** per game — Aaron and Lena both judged that "obvious and straightforward." Under the games-production space you then see "Fortune Foo Paws game", "Fortune Foo Paws design", and so on down the list. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- On the design side, Lena immediately created her branch and a `comparts` folder and committed one file (main-scene final comp art); the plan was to create the separate design repo and commit the comp art there instead. She still had open questions on how often to commit and the maximum committable file size — unresolved in this call. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]

The Feb 26 follow-up extended the structure with two **new GitHub organizations** (Game Concepts, Game Designs) and a separate repo for the Fortune 4 Progressive Sign — see [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]] and [[wiki/decisions/2025-02-26-designer-branching-workflow.md]]. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

## Sources

- [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
