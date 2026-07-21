---
type: meeting
title: Game-concept-stage workflow prep — GitHub repos, universal Backlog/ToDo/In-Progress/Done, Obsidian for abstracts (Oct 7 2025)
date: 2025-10-07
aliases: [objectives workflow Oct 7, game concept workflow prep, Obsidian game abstracts, feature branch is a repository, universal workflow naming]
source-count: 1
open-commitments: 1
---

# Game-concept-stage workflow prep — GitHub repos, universal workflow, Obsidian for abstracts (Oct 7 2025)

**Date:** 2025-10-07 (3:02 PM) · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrey-bosik.md|Andrey Bosik]]. Russian.

A short prep call: Val briefs Andrey ahead of **tomorrow's (Oct-8) meeting** on organizing the workflow and the GitHub repositories for the **game-concept stage**. Substance ties to [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]] (Jira↔GitHub mapping, workflow states) and [[wiki/topics/docs-as-code-and-atlassian-exit.md]] (the Confluence→Obsidian move). The Oct-8 game session's own attendees are named as Michael, Efim and Lena; Val also referred to "tomorrow's meeting with **Iran**" — an unclear name / likely ASR garble, left unresolved. §15.8: no compensation material.

Durable points (single source):

- **The Jira→GitHub handoff for game concept.** In Jira, the last stage is the **feature**; after feature, work moves to GitHub where all the work is done. Andrey and Val's working mapping: a **feature = a branch** in some repository, and the **product level = a repository**. The **game-concept stage has 3 features** (Val thinks of a feature as a physical artefact/deliverable). Michael must write an **abstract** for a game inside a feature branch. [[raw/objectives_workflow_meeting-october-7-2025.md]]
- **"Done" = the pull-request merged.** When a feature branch is pulled into main (PR reviewed/approved) and the branch closes, GitHub sends the message back and the Jira feature workflow moves to **Done**. Later GitHub-side stages (staging deployment, close, archive — e.g. year-end cleanup) represent the physical movement of artefacts and are driven from GitHub, not Jira. Andrey was unsure Jira auto-updates status from GitHub automatically; to be checked. [[raw/objectives_workflow_meeting-october-7-2025.md]]
- **Universal workflow naming across value streams.** Val wants **Backlog → To-Do → In-Progress → Done** kept everywhere as the minimum ("program minimum") — the workflow Val had accepted. Andrey argued for **universality**: game production will need a *wider* workflow, but the shared action names (e.g. "In Progress", "Backlog") should not change between value streams, so an engineer moving between streams isn't disoriented ("the break happens in the mind"). Val agreed — a wider game-production workflow may add extra stages, but the minimal shared ones stay; extra stages are the exception. Val admitted the earlier workflow he'd drawn was probably wrong because he'd focused on describing each station rather than holding to universal naming. [[raw/objectives_workflow_meeting-october-7-2025.md]]
- **Replace Confluence with Obsidian for game abstracts (MDX in the repo).** Val wants the game team to stop using **Confluence** ("compliance"/"conference" as transcribed) and instead write abstracts physically in **Obsidian**, in a data/MDX format, so the abstract can later be reused to give an easy graphical UI. Obsidian pulls documents in easily and gives a light format straight into the repo; alternatively just put the docs directly in GitHub via MDX. Andrey noted some **Python scripts** are used to process this and would need templating/replicating per repository, and asked to check with the author how it works under the hood. [[raw/objectives_workflow_meeting-october-7-2025.md]]
- **Every feature physically described + committed to git.** Val's emphasis: under every product in any value stream, each feature should be a **definite, physically-delivered artefact** — a drawing/sketch/spec/blueprint or a piece of code — something physically placed into git, with a concrete acceptance point on the repository. [[raw/objectives_workflow_meeting-october-7-2025.md]]

## Open commitments

- [ ] Andrey Bosik — for tomorrow's meeting, work out how to correctly **create/name the game-concept-stage repositories** (review the agreed naming table, propose naming options and access model) — due Oct 8 2025 — [[raw/objectives_workflow_meeting-october-7-2025.md]]

## Sources

- [[raw/objectives_workflow_meeting-october-7-2025.md]]
