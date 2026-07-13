---
type: decision
title: Upgrade the Omni engine to Pixi 8.6 and update the engine yearly (2025-01-17)
date: 2025-01-17
aliases: [Pixi 8.6 upgrade, upgrade Pixi, Pixel engine upgrade]
source-count: 1
status: active
open-commitments: 1
open-questions: 0
---

# Upgrade the Omni engine to Pixi 8.6 and update the engine yearly (2025-01-17)

**Decision:** Val agreed JVL will upgrade its game engine to the latest Pixi (JavaScript "Pixi"/"Pixel" rendering engine), version 8.6, and adopts a standing policy of regularly pulling newer official Pixi (and other library) versions into the Omni platform rather than freezing at one version. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

**Decided by:** Val, prompted by Sasha and Dima Khandov. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Rationale

- JVL is on the 6th version of Pixi, which supports only Spine 4 (~4.2). A newer Spine format adds features (e.g. physics) the designers want, and needs Pixi 8.6 plus updated libraries. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- Val's principle: "we chose a beautiful engine" and must not freeze it — the tools move forward and the designers need that flexibility. The Git-based process should drive continuous, controlled updates (not "write a package lock and never look back"). See [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Open commitments

- [ ] Sasha (Alexander Biratka) — upgrade JVL to the new Pixi version (~a week of work) — due unspecified (imminent) — [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Sources

- [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
