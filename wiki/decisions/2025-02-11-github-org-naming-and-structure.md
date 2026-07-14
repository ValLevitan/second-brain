---
type: decision
title: GitHub org naming convention and the JVL enterprise org list
date: 2025-02-11
aliases: [GitHub org naming, JVL prefix, org naming convention, enterprise organizations, repo naming]
source-count: 3
status: active
---

# GitHub org naming convention and the JVL enterprise org list

**Decision (Feb 11 2025, Val + Aaron + [[wiki/people/andrey-bosik.md|Andrei]] + [[wiki/people/pavel.md|Pavel]]/[[wiki/people/alexander-biratka.md|Sasha]]):** JVL uses a **multi-organization GitHub enterprise** (confirming the prior day's direction), with a fixed naming convention and a finalized list of organizations. [[raw/Git_repo_structure_part_2_2025-02-11.md]] This builds on [[wiki/decisions/2025-01-20-github-orgs-mirror-value-streams.md]] (orgs mirror the Jira value streams).

## Naming convention

- **Organization names:** written in **plain English with capitals** and a **"JVL " prefix** (e.g. "JVL Platform"); GitHub then applies its own rules to form the URL slug (converting spaces to hyphens). Typing human-readable names lets GitHub enforce a consistent convention rather than engineers guessing hyphen-vs-underscore. Uppercase in the org URL is deliberately accepted for readability (Aaron overrode the GitHub docs' lowercase recommendation). [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- **JVL prefix agreed** for org names (Andrei/Sasha wanted uniqueness; org names are globally unique on GitHub). Aaron argued for JVL **at the front** (sorts by the next letters); Alex noted a suffix sorts better — front prefix was adopted. [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- **Repository names:** lowercase, hyphenated, **short and descriptive**, **no "JVL" prefix** and no "repo" suffix (e.g. `reels-math`, `shuffle-math`, `hold-and-spin`, `hal` for hardware-abstraction-layer). Aaron cited the Home Assistant org (100+ repos, minimal names) and warned that JVL-prefixing every repo would make the code hard to ever sell. Repo names are not globally unique (only org names are). [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- Example full URL agreed: `github.com/JVL-Core-Technology/hal.git`. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## The organization list (7), mirrored onto the Jira value streams

Named (all JVL-prefixed): **Games Production**; **Math & Game Mechanics** ("Games Math & Mechanics"); **Platform** (a.k.a. gaming/backend platform); **Observability Platform** (the CMS replacement, owned by [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — transcribed "Dima Chudinov"); **Core Technology / Core Tech** (holds Linux and the hardware-abstraction-layer HAL); **Systems Operations** (Andrei's — operating everything, kept separate from observability); and **Hardware & Firmware** (formerly "distribution infrastructure" — Flex, countertops, payment platform, progressive controller, device drivers; cabinets tracked separately). Pavel and Aaron agreed to restructure the Jira value streams to match. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

> The Observability-Platform owner (transcribed "Dima Chudinov") is [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], JVL's back-end architect (owner ruling 2026-07-13; his Belarusian spelling is Dzmitry Dudzinau) — a distinct person from the IT "Dima" (Kovalchuk). [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## History — how the list emerged (Feb 10 part-1 meeting)

The org list was hammered out the **previous day** ([[wiki/meetings/2025-02-10-github-repo-structure-part-1.md]]). [[wiki/people/alexander-biratka.md|Sasha]] opened proposing **one organization, "or probably two"** (one company-wide + one private for the math sources), arguing GitHub **groups** handle rights more flexibly than organizations and that mirroring Jira in orgs "didn't work out"; Aaron called one-org "short-sighted" and pressed the scaling question; by the end the group "naturally arrived" at **five organizations — game development; online + land-based platforms (one org); math; observatory and orchestration platform; core tools** (core tools then = TEST360, diagnostic and design tools). [[raw/github _structure-pavel-aaron-andrei.md]] Val then sketched **responsible owners per org** — game development: Lena; platforms: Sasha; math: Efim; observatory & orchestration: Dima Chudinov; core tools: Pavel — and proposed a **sixth org, "core technologies"** (Flex Payment Solution, hardware abstraction layer + firmware, and possibly the distribution infrastructure folded in), noting Pasha doesn't actually manage TEST360, the diagnostic tool or design tools like Miranda. [[raw/github _structure-pavel-aaron-andrei.md]] On submodules, Andrei said the team uses **GitHub Apps** rather than deploy keys ("we don't use deploy case [keys], because deploy case has some restrictions when we need to create pair case for main repository to sub-module repository") — adding "these GitHub applications work only in one organization," an argument for fewer orgs at that point; Aaron countered that submodules can be referenced from any accessible repo and warned against baking in GitHub-only dependencies (the GitLab portability test). The cross-org access solution came the next day ("I work with GitHub application. I found a solution how we can have access to submodules if needed to another organization"). [[raw/github _structure-pavel-aaron-andrei.md]] [[raw/Git_repo_structure_part_2_2025-02-11.md]] The next day's part-2 session confirmed multi-org and finalised the 7-org list above ("As we said yesterday…"; Sasha: "I agree with yesterday's solutions"). [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## Two more design orgs added (Feb 26)

On the Feb 26 designer-migration call, [[wiki/people/lena.md|Lena]] needed a home for design-stage work (initial comp art) and JVL agreed to **create two more organizations — "Game Concepts" and "Game Designs" (plural)** — so the GitHub orgs mirror the **three Jira stages: concept → design → production** ("JVL Games Production" already existed). [[wiki/people/andrey-bosik.md|Andrei]] is to create them and grant Lena repo-creation rights; a separate repository is also planned for the **Fortune 4 Progressive Sign** (a separate IP). See [[wiki/decisions/2025-02-26-designer-branching-workflow.md]]. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

## Sources

- [[raw/github _structure-pavel-aaron-andrei.md]]
- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
