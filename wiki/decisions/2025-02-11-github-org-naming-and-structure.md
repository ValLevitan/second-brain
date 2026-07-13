---
type: decision
title: GitHub org naming convention and the JVL enterprise org list
date: 2025-02-11
aliases: [GitHub org naming, JVL prefix, org naming convention, enterprise organizations, repo naming]
source-count: 1
status: active
---

# GitHub org naming convention and the JVL enterprise org list

**Decision (Feb 11 2025, Val + Aaron + [[wiki/people/andrei.md|Andrei]] + [[wiki/people/pavel.md|Pavel]]/[[wiki/people/alexander-biratka.md|Sasha]]):** JVL uses a **multi-organization GitHub enterprise** (confirming the prior day's direction), with a fixed naming convention and a finalized list of organizations. [[raw/Git_repo_structure_part_2_2025-02-11.md]] This builds on [[wiki/decisions/2025-01-20-github-orgs-mirror-value-streams.md]] (orgs mirror the Jira value streams).

## Naming convention

- **Organization names:** written in **plain English with capitals** and a **"JVL " prefix** (e.g. "JVL Platform"); GitHub then applies its own rules to form the URL slug (converting spaces to hyphens). Typing human-readable names lets GitHub enforce a consistent convention rather than engineers guessing hyphen-vs-underscore. Uppercase in the org URL is deliberately accepted for readability (Aaron overrode the GitHub docs' lowercase recommendation). [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- **JVL prefix agreed** for org names (Andrei/Sasha wanted uniqueness; org names are globally unique on GitHub). Aaron argued for JVL **at the front** (sorts by the next letters); Alex noted a suffix sorts better — front prefix was adopted. [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- **Repository names:** lowercase, hyphenated, **short and descriptive**, **no "JVL" prefix** and no "repo" suffix (e.g. `reels-math`, `shuffle-math`, `hold-and-spin`, `hal` for hardware-abstraction-layer). Aaron cited the Home Assistant org (100+ repos, minimal names) and warned that JVL-prefixing every repo would make the code hard to ever sell. Repo names are not globally unique (only org names are). [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- Example full URL agreed: `github.com/JVL-Core-Technology/hal.git`. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## The organization list (7), mirrored onto the Jira value streams

Named (all JVL-prefixed): **Games Production**; **Math & Game Mechanics** ("Games Math & Mechanics"); **Platform** (a.k.a. gaming/backend platform); **Observability Platform** (the CMS replacement, owned by "Dima Chudinov"); **Core Technology / Core Tech** (holds Linux and the hardware-abstraction-layer HAL); **Systems Operations** (Andrei's — operating everything, kept separate from observability); and **Hardware & Firmware** (formerly "distribution infrastructure" — Flex, countertops, payment platform, progressive controller, device drivers; cabinets tracked separately). Pavel and Aaron agreed to restructure the Jira value streams to match. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

> "Dima Chudinov" (owner of the Observability Platform / CMS-replacement org) may be distinct from [[wiki/people/dmitry-khandov.md|Dmitry Khandov]] — recorded in Owner Decisions, not merged. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## Sources

- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
