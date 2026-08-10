---
type: decision
title: Do not migrate RAGE games to NOVA en masse; fully port the South Dakota product (~6 months)
date: 2026-08-03
aliases: [no en-masse Rage to Nova migration, South Dakota full Nova port, do not certify Kali Ocha]
source-count: 2
status: active
---

# Do not migrate RAGE games to NOVA en masse; fully port the South Dakota product (~6 months)

On the [[wiki/meetings/2026-08-03-rage-nova-migration-experiment.md|Aug 3 2026 RAGE→NOVA experiment sync]], after reviewing [[wiki/people/igor-metelski.md|Igor Metelski]]'s successful AI-assisted conversion of a RAGE game onto NOVA, [[wiki/people/val-levitan.md|Val]] pushed the team on *why* migrate RAGE games to NOVA at all and rejected the "build a park of migrated games" rationale. [[raw/Meeting_Notes_Rage_to_Nova_Migration_Experiment-August-3-2026.md]] [[raw/Meeting_Transcript_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]

## What was decided (Val)

- **Do not migrate RAGE games to NOVA en masse just to have a library on hand.** Instead, port the common NOVA environment (liquid-glass frame, GamesElectScreen, setup screens) so the toolchain is ready, build **new** games on the new tools, and keep a conversion plan on hand to jump on only when a specific market/jurisdiction demands it. Val's reasoning: the existing RAGE games are already sold and can be fixed on the old system if a bug is found, and new games can be built directly on NOVA — so mass pre-migration wastes time. [[raw/Meeting_Transcript_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]
- **The South Dakota product will be fully ported from RAGE to NOVA.** The earlier idea of leaving South Dakota on RAGE (because it is the hard, Class-III-regulated case) was dropped. Plan: certify and release the *current* RAGE version now so it goes to market; in parallel, fully port the South Dakota product to NOVA (the new revision with liquid glass, new floats, keno added — ~10 games, likely +4 more → ~12), and do a full certified replacement in **about six months** (~3 months to transition + ~3 months polishing). [[raw/Meeting_Transcript_Rage_to_Nova_Migration_Experiment-August-3-2026.md]] [[raw/Meeting_Notes_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]
- **Do not finish or certify the standalone Kali Ocha game** (Val, rejecting Igor's suggestion to finish it). [[raw/Meeting_Transcript_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]
- **The next experiment targets a horizontal game and logic migration** (not another vertical re-skin) — candidate "Nikena," a regular South Dakota game ("Crescent City Carnival" floated as an alternative because its spin-bonus math differs) — and should also run on target hardware (RK3568 "76" board and/or V1000). The group reconvenes **August 17, 2026** to assess it (this superseded an Aug 13 date proposed mid-meeting). [[raw/Meeting_Transcript_Rage_to_Nova_Migration_Experiment-August-3-2026.md]] [[raw/Meeting_Notes_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]

## Why it matters

The experiment showed resource migration is fast (a vertical re-skin dropped from ~1.5 days of clean work to ~3 hours once Claude's reusable scripts existed; [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] estimated ~80% of games could migrate with little pain), but **game logic migration has not been attempted** and is the real unknown — which is why Val wants a proof on a harder game before committing a budget-per-game. [[raw/Meeting_Notes_Rage_to_Nova_Migration_Experiment-August-3-2026.md]] [[raw/Meeting_Transcript_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]

This refines the platform direction tracked on [[wiki/topics/nova-platform-architecture.md]] and the market plan on [[wiki/projects/south-dakota-vlt-market.md]].

## Sources
- [[raw/Meeting_Notes_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]
- [[raw/Meeting_Transcript_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]
