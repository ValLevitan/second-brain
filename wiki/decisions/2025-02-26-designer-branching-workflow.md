---
type: decision
title: Feature/story branch discipline for the design team (PR-only to main, branch-lifespan metric)
date: 2025-02-26
aliases: [designer branching, feature branch, story branch, pull request workflow, branch lifespan metric, PSD branching]
source-count: 1
status: active
---

# Feature/story branch discipline for the design team

**Decision (Feb 26 2025, [[wiki/people/aaron.md|Aaron]] + [[wiki/people/val-levitan.md|Val]] coaching [[wiki/people/lena.md|Lena]], [[wiki/people/dmitry-khandov.md|Dima Khandov]], [[wiki/people/yulia.md|Yulia]], [[wiki/people/anastasia.md|Anastasia]]):** JVL's graphic designers adopt the same Git branching workflow as the code teams — including for **Photoshop/PSD design files**, not just code. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

## The workflow

- **`main` is the single source of truth and must always be correct.** [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- Open a **feature branch** off `main` (e.g. an "animation" feature). Within a feature branch, each person opens a **story branch** off the feature for their own piece (Yulia → 3D model, Anastasia → texturing, Lena → Photoshop comp art). [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- Commit freely (multiple commits allowed) to your branch; **merge into `main` (or a feature branch) only via a pull request**, never directly — rules can be set to refuse a direct merge. When a pull request is approved it merges automatically and the working branch is deleted. Aaron pruned stale already-merged branches ("Lana Compart", "Symbol Rooster") to demonstrate. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- **Branches are named after the matching Jira feature** so everyone understands what is going on. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

## Branch-lifespan performance metric (Aaron's intended scoring)

Aaron said he will eventually **measure** how fast a feature branch is opened and closed: **3 days = amazing, 5 days = average, 7 days = getting bad, 10 days / two weeks = the baseline (worst acceptable), beyond 10 days = unacceptable.** A feature branch must close within two weeks or less. He stressed he is not measuring it yet, but that is how he will. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

## Unfinished work and when Michael comments

- It is fine for a designer's **unfinished** work to be visible to everyone in a non-`main` branch; it is **not** okay for [[wiki/people/michael-game-producer.md|Michael]] (or anyone) to criticise work still in a branch. Lena's objection — that she doesn't want comments on cats that "look completely unfinished" — was answered this way. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- **Michael's time to comment is at the pull request**: issuing a PR is literally the request to have the work reviewed. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

## Rationale (Val's framing)

Val framed Git as the tool that creates alignment, transparency and "buzz" in a fully-remote, multi-time-zone company where "there are no more coffee-machine meetings": commits show what everyone is doing, let the company measure pace, and identify non-performers versus contributors — "you can only win by saying factually, we were here before, we're here now, how do we go faster." [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

## Sources

- [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
