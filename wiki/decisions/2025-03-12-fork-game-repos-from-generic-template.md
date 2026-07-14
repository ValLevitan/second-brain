---
type: decision
title: New game repos fork (not clone) from a generic template; enable fork-from-template
date: 2025-03-12
aliases: [fork from template, generic template repo, fork not clone, enable forking]
status: active
source-count: 1
open-commitments: 1
open-questions: 0
---

# New game repos fork (not clone) from a generic template

On the Mar 12 2025 "GitHub for graphic design" check-in, [[wiki/people/val-levitan.md|Val]] ruled how the design team creates a repository for a new game. Full workflow context on [[wiki/topics/graphics-team-git-workflow.md]]. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## What was decided

- [[wiki/people/andrey-bosik.md|Andrei Bosik]] is to build a **generic base template** repository (today only a **Fortune Fupa / FFP-specific** template exists). [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- New game repos are created by **forking** the generic template, **not cloning** it — Val's reason: a fork becomes its own project, so designers cannot **accidentally push back** to the template repository (a clone pushes back to the original). [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- Andrei had **disabled** fork-from-template "for security reasons"; Val overrode this (his "paper door lock" argument — a fork is no less secure than a clone for copying to a public space), and Andrei **enabled the right to fork from template repos for all repos** during the call. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Rationale

- The team needs to spin up a new game repo (e.g. **Cache Kittens**) from a known-good base without risk of contaminating the template. Forking gives an independent project; the disabled fork setting was blocking that for no real security gain. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Open commitments

- [ ] Andrei — build a **generic base template** repo (from the Fortune Fupa template) that new game repos fork from — due unspecified — [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Sources

- [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
