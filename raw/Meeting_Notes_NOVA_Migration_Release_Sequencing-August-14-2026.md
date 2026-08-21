# Meeting Summary — NOVA Migration Plan (Release Sequencing)
**Date:** August 14, 2026, 4:00 PM ET
**Duration:** ~49 minutes
**Attendees:** Val Levitan, Michael Gottlieb, Juan Martinez, Lena Zhukova, Efim Podvoiski
**Raw transcript:** [[Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026]]

## Summary

The meeting was about how to move JVL's games from the current V1000 / Rage platform to the new FP7 / Nova platform, and in what order to release across markets (South Dakota, Nebraska, Georgia, Texas).

Val reported that internal testing shows they can convert existing assets into Nova with impressive speed — roughly one week per game (later debated as closer to two weeks) — and that they cloned an actual working game in about a week. Michael stressed that timings and behaviors have to be converted, not just the art assets.

Val's opening idea was to convert the entire South Dakota library to Nova and leave Georgia, Nebraska and Texas untouched (only building new games there). The group pushed back and rejected it: there is no value in porting old or failed games (Dutch Mills, Liberty Spins) or the old non-liquid-glass South Dakota. They confirmed you can port a single game, not only a whole ISO package.

Key facts established:
- Nova / FP7 runs only on new hardware and cabinets. V1000 will no longer be manufactured. There is no forced hardware upgrade on the installed base — new offerings go on new cabinets.
- Georgia's V3 release stays on the current platform (target September 1). Nova would be a later Georgia release (more like V4 than V3).
- The Peach titles are "dead" — games move onto Liquid Glass and away from the Peach bonus. Val treats games as reimaginable life-cycle items ("like a James Bond movie").
- Georgia's coming "Blaze" release is a "best of" hybrid: ported and updated older titles on Liquid Glass plus new Jackpot Rush and Fiery Ice titles (neither has run on D27 in Georgia before).
- South Dakota carries GLI approval risk — the big regulatory gate. Nebraska has no GLI approval; Texas is minor (via Eclipse).
- South Dakota Vertical needs three brand-new games (Solar Keno, Aaron's Pub, Dakota Bison) that must be built, not converted, because they never existed in vertical.

## Decisions Made

- **The first product to launch on Nova / FP7 will be South Dakota Vertical 01, targeted March 2027.** — Chosen as the lowest-risk first Nova product: if it slips, the existing South Dakota D27 (with the Keno games) keeps performing. (Verbalized by Michael, agreed by Val and Juan.)
- **Nebraska D2702 stays on Rage / the current platform** and releases toward the end of 2026 — it is NOT moved to Nova. Val's earlier suggestion to do Nebraska on Nova was dropped after Juan and Lena warned it would add a 2–3 month delay.
- **Submit "Cayocho" (Kaya Ocho), which already runs on Nova, to GLI to test and get the Nova platform approved** — in parallel, starting with a single game (possibly one per category plus Liquid Glass). A Keno submission was judged not important. (Decided by Val, agreed by Michael, Lena, Efim.)
- **Lena develops games in Nova in parallel while Nova keeps changing** — peripheral/API/Rust changes don't affect how she builds games, so platform maturation and game-making run in parallel, not in sequence.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Engineering team | Submit Cayocho on Nova to GLI to get the Nova platform approved | TBD (aim approval ~January) | High | Gates the first Nova release; start with one game |
| 2 | Lena Zhukova | Build the South Dakota Vertical games (Solar Keno, Aaron's Pub, Dakota Bison) new for vertical in Nova, once Nebraska is finished | After Nebraska release | Normal | These never existed in vertical, so they must be built |
| 3 | Efim Podvoiski | Finish his math work before Sept 15 [Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.] | Before Sept 15, 2026 | Normal | Val: "do your math before September 15" — Efim out end of that week |

## Open Questions

- Which games are needed for the South Dakota Vertical release (Val was unsure of the list).
- Whether the Keno games will perform in South Dakota D27 — if not, plan B is firefighting a performing game on Rage.

## Dispatch Log

---
*Processed from Teams transcript on August 14, 2026 (scheduled meeting-watcher run).*
*Source meeting: NOVA_migration_plan-August-14-2026*
