---
type: topic
title: Graphics team Git workflow (PR discipline, CI tickets, deploy pipeline)
date: 2025-03-12
aliases: [designer git workflow, graphics PR discipline, pull request discipline, contact sheet action, assets deploy pipeline, fork from template, help desk CI tickets, performative pull request, pull request back to template, template per game type]
source-count: 3
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

## Template repo check-in (Mar 26 2025)

A follow-up "GitHub commits" check-in where [[wiki/people/andrey-bosik.md|Andrei]] demoed the working **template repository** (with [[wiki/people/val-levitan.md|Val]], [[wiki/people/lena.md|Lena]], [[wiki/people/dmitri-kovalchuk.md|Dima Kovalchuk]], and an "Igor" whose identity is unresolved — see Owner Decisions). [[raw/github_commits-march-26-2025.md]]

- The template can be **instanced with one button** into a new repo (a variable/repo with a single initial commit, all pre-structured) and carries **predefined GitHub Actions** for contact sheets, sprites, and **migrating/updating pull requests**. Val's forward idea: on instancing, an Action does **word-replacement across the docs** so a new project's README/files are auto-named. [[raw/github_commits-march-26-2025.md]]
- **Close the loop back to the template (Val's main point):** there was **no process to return improvements to the parent template**. Val pushed hard on the *culture*: when a game produces something worth keeping, feed it back into the template **via a pull request** ("I request you to pull my good changes into your thing"), so the template doesn't go stale — you'd **fork** the template, incorporate changes from the working repo, and PR them back. Use Git terms, not "I'll just edit it by hand." [[raw/github_commits-march-26-2025.md]]
- **Signals it's time to update the template** (Val's coaching, with Lena): a **new reusable script** useful across all games; or finding yourself **repeatedly adding the same things** after cloning each new project. [[raw/github_commits-march-26-2025.md]]
- **Templates per game type (Lena):** the current base template just holds shared structure; in future JVL will have separate templates for **Georgia / Omnia framework games**, **Persistence games**, and **classical games**, each with a more appropriate structure per game mechanic. [[raw/github_commits-march-26-2025.md]]
- **Follow-up:** GitHub-commits check-in set for **April 9, 9:30am Eastern** (later merged with the MCP test — see [[wiki/meetings/2025-03-26-mcp-unity-visualcode.md]]). [[raw/github_commits-march-26-2025.md]]

## Moving art-asset evolution out of Jira into GitHub (stated Mar 26)

In the Val–Gottlieb one-on-one (same day as the template check-in above), Val stated the review flow itself is changing: "as of this moment, we already experimenting with **not putting it into Jira**, because Jira has multiple reiterations. We want to have only one asset… and an account of this evolution" — moved into **GitHub**, where each person works in a local **sandbox** and pushes when ready, so reviewers see the final with a **"differential evolution"** (rollback shows what changed — "purple was changed to green"). Val's claims for it: educational replay for young designers ("these are the errors that you're making"), and instant **scale-up/scale-down** of outside hires with no learning curve. He added that Jira/GitHub can now be driven by a **human-language interface** ("we don't even need to know GitHub") and predicted JVL can eventually "push away from Jira." Gottlieb noted the team had put everything **into** Jira under Val's own earlier direction — recorded as evolution of that instruction, not a contradiction. See [[wiki/meetings/2025-03-26-gottlieb-val-one-on-one.md]]. [[raw/michael_gottlieb_val_meeting-26-2025.md]]

## Sources

- [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- [[raw/github_commits-march-26-2025.md]]
- [[raw/michael_gottlieb_val_meeting-26-2025.md]]
