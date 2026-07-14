---
type: topic
title: Graphics team Git workflow (PR discipline, CI tickets, deploy pipeline)
date: 2025-03-12
aliases: [designer git workflow, graphics PR discipline, pull request discipline, contact sheet action, assets deploy pipeline, fork from template, help desk CI tickets, performative pull request]
source-count: 1
---

# Graphics team Git workflow (PR discipline, CI tickets, deploy pipeline)

The working practices JVL's design team follows on GitHub, as coached by [[wiki/people/val-levitan.md|Val]] and [[wiki/people/aaron.md|Aaron]] on the Mar 12 2025 "GitHub for graphic design" check-in with [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/lena.md|Lena]], [[wiki/people/yulia.md|Yulia]], [[wiki/people/anastasia.md|Anastasia]] and [[wiki/people/dmitriy-khandov.md|Dima Khandov]]. Builds on the earlier design-team decisions ([[wiki/decisions/2025-02-21-separate-game-and-design-repos.md]], [[wiki/decisions/2025-02-26-designer-branching-workflow.md]]) and the docs-as-code direction ([[wiki/topics/docs-as-code-and-atlassian-exit.md]]). [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## The PSD-commit conflict complaint

- The team reported that committing new **PSD files** produces merge conflicts when two people open pull requests to `main` at nearly the same time (Andrei/Lena/Anastasia hit it). Andrei diagnosed the cause: the **auto-generated `index.md`** for the contact sheet contains a **"generated on" date/time line** that changes every run, so he proposed **deleting that line** to stop the conflicts. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- Aaron's framing: work on **separate feature branches** with separate files shouldn't truly conflict; the contact-sheet **Action just runs twice on `main`** after two merges, and if that breaks you fix the script rather than debug it live in a meeting with eight people. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Report tooling/CI problems as help-desk tickets, not in meetings

- Val/Aaron's rule: when the art team's tools or CI **Actions** break, they should open a **ticket in the help desk (`help.jvl.ca`)**, not save it for a meeting. The support team (Andrei's group, able to dispatch to **Anton**, **Sasha** or **Pavel**) then commits the fix connected to the pull request / commit — treating a broken contact-sheet feature as "just another feature." "Everybody is made the same" — support people make features and improvements in the same repos as everyone else. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## The assets → game deploy pipeline

- Artists commit to the **production source game assets** repo (with production manifests). A **GitHub Action automatically archives and deploys to the game repo** — producing a zip archive / "complete assets bundle artifact." A next step is meant to **trigger an Action in the game-mechanic-logic repo**, but **that step did not work yet** as of this meeting ("about that step we speak only today"). Game assets and game-mechanic logic are **separate repositories**. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Pull-request discipline (Val's coaching)

- The assets repo had **one branch (`main`)** and **29 closed pull requests**. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- **Reference the Jira ticket** in every PR (the test PR "UDE dev environment added for main FFP game" had none, because it was a test; all future ones will). [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- **Assign the PR** (an assignee, not just reviewers). [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- **No giant PRs:** Julia had **approved a ~940-file PR** ("did you really review 940 files in an hour?") — it was **Dima's Miranda catch-up** commit, a legitimate special case (technical debt), but a PR should never have ~1,000 files unless it is that kind of special catch-up. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- **Make PRs "performative":** Val's lesson — write descriptive commentary explaining your **intention** so people **outside** the tight team can understand what happened; a PR is "stop, review this, acknowledge its existence, commit" — not a wink or a note slid across the hallway. "A year from now… you'll thank yourself." [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## When to create a repo for a new game — "fake the review"

- [[wiki/people/lena.md|Lena]] asked at what stage to create a repo for a new game (e.g. **Cache Kittens**), since Michael, Juan and Yefim aren't on Git yet and early design still happens in **Zephyr** — so no one could approve her commits. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- Answer (Aaron/Val): **start the repo now and "fake the review"** — give **Julia/Anastasia or Dima Khandov** access to approve. Practice what you preach; build incremental successes and enroll the others later. Val isn't ready to bring Michael/Juan/Yefim onto Git yet. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Generic template + fork workflow

- Lena has a **Fortune Fupa (FFP)-specific** template; Andrei is to build a **generic base template** repo. New games are created by **forking (not cloning)** from the generic template so designers can't accidentally push back to it. Andrei had **disabled** fork-from-template "for security reasons"; Val overrode this (his "paper door lock" analogy — a fork is no less secure than a clone for copying to public space) and Andrei **enabled fork-from-template for all repos**. Captured as [[wiki/decisions/2025-03-12-fork-game-repos-from-generic-template.md]]. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Side note — current design workload

- The team is **not full-time on Fortune 4 (FFP)** this period; **Heat Game 6** and **Georgia** are the urgent side projects, and **Natasha** is continuing Georgia while Lena returns to FFP. The next check-in was set for the **26th** (Wednesday, two weeks out); Val books these meetings for **30 minutes or less**. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Sources

- [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
