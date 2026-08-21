---
type: decision
title: Math-as-a-service — build the math Docker container from a game list at the integration-build step (one container per game set / market)
date: 2026-08-18
aliases: [math container per game set, math as a service packaging, math Docker container build, per-market math container]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
---

# Math-as-a-service — build the math Docker container from a game list at the integration-build step

On the [[wiki/meetings/2026-08-18-rage-nova-migration-experiment-review.md|Aug 18 2026 RAGE→NOVA review]] the team settled how math should be packaged now that it runs as a **service in a Docker container** on the NOVA platform. Discussed by [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] (math owner), [[wiki/people/pavel.md|Pavel Frolov]], and [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/irina-shishko.md|Irina Shishko]]. This is a NOVA architecture detail; the platform is on [[wiki/topics/nova-platform-architecture.md]]. [[raw/Meeting_Notes_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]] [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]

## What was decided

- **Build the math container from a game list passed in during the integration-build step**, so each release package gets a container built for its specific set of games — one container per game set / market. The build step feeds a generated config / list of games into a branch of the math repository, and the same job that builds the release assembles the correct container. Efim called this the "sound compromise," to be refined in practice. (Efim, Pavel, Evgeny.) [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- **Rejected alternative — one giant container holding every game.** Efim resisted keeping "everything in one endlessly large heap," because adding one game for one market would change what ships to other markets. [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- **Rejected (as premature) — a fully self-configuring container** that inspects whichever games are installed on the machine and configures itself. Evgeny floated it; Efim judged it "turns things on their head," breaks the container's self-sufficiency, and needs much more thought before adopting. [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]

## Facts and nuances

- **Math is treated as a service** running in a Docker container, **per machine** (each machine runs its own container; the server version was only a development convenience). Math is kept in a **separate, secured environment**, historically not accessible to others. [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- The container should hold **at least what the product contains**, and typically **fewer containers than products** — near-identical products that overlap ~90% can share a single math package; clones reduce the count (e.g. ~13 math sets for ~15 games if two are clones). [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- **Certification expects per-game checksums.** Val: if a submission is not signed, the lab (GLI) has the right to verify it and JVL pays for that verification; today they confirm sameness by checksum rather than re-running full math tests, but they retain the right to re-check. So the packaging must expose **per-game checksums of the critical math files/configs** (as JVL did online) so an unchanged game need not be re-verified. [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]

## Open questions

- Exact **build mechanics** for assembling the per-package math container from the game list — how the integration build injects the game list and produces the correctly-scoped container — were left to be worked out in practice. (Efim, Pavel, Evgeny.) [[raw/Meeting_Notes_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]

## Sources
- [[raw/Meeting_Notes_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
