# Meeting Summary — RAGE-NOVA_migration

**Date:** August 3, 2026, 8:00 AM ET
**Duration:** ~52 minutes (recording 08:03–08:55 ET)
**Attendees:** Val Levitan, Pavel Frolov, Igor Metelski, Irina Shishko, Alexander Biratko, Evgeny Kharetski
**Raw transcript:** [[Meeting_Transcript_Rage_to_Nova_Migration_Experiment-August-3-2026]]

## Summary

The team synced on experiments to convert existing **Rage-platform** games onto the **Nova** platform using Claude (AI) to do most of the work, and Val used the meeting to decide the strategy behind that migration. The meeting was held in Russian.

**Igor's experiment.** Igor took a playable Nova game ("Kali Ocha") as the reference and used Claude to convert a Rage game with the same math, "Dragon's Reign," into Nova — several scenes: symbols, the main game scene, the free-spins scene, and a few dialogs. He asked Claude to reuse the Rage resources directly (e.g. take the existing video and act on it). The result now looks visually like Dragon's Reign inside the Nova game.

**Problems found.**
- **Composition mismatch.** Nova's dashboard is thicker, so the symbol field sits higher and the symbol frame overlaps some background elements. The dragon background is a single large video (dragon + logo + progressive frames), so it can't simply be shifted. Claude offered two paths: reuse the reference positions from the existing Nova game, or recalculate symbol positions from the Rage layout.
- **Dashboard branches differ.** Some branches still have the old dashboard (pre-liquid-glass); the liquid-glass branch is missing elements such as the credit/denomination button.
- **Helps ("хелпы") are a separate task.** Nova uses pre-rendered images in two languages; Rage composes scenes with text pulled from dictionaries across several languages. Localized resources (rendered textures vs dictionary text) will need their own handling — open question whether Claude can render localized video from dictionary text.
- **Diamond symbols** are implemented differently (PNG sequence in Nova vs video in Rage); Claude can split the video into frames and build the PNG sequence.

**What worked well.** Claude handled the alpha-channel video (lightning effects) correctly and wrote the needed shaders. Shared bonuses do not need migrating — if a bonus already exists for the reference game, other games reuse it, so Igor skipped bonuses. Claude also writes reusable scripts that speed up subsequent conversions.

**Effort.** The reference conversion took roughly 1.5 days of clean work; with the scripts now built, a similar re-skin could take about 3 hours. Evgeny estimated ~80% of games could migrate with little pain. Resource migration is fast; **game logic has not been attempted yet** and is the real unknown. The team was confident Claude works fine with C++ (Igor is already using it for Dakota release tasks). Idea raised: use a second Claude to verify the first Claude's logic work rather than testing everything by hand.

**Hardware.** A later experiment should run on target boards. Discussed the RK3568 "76" board (16 GB; GPU like the "68", core count like the "88") — not yet supported by the SDK, unlike the "88" — plus the V1000, on which the software should install. FPS/performance was not seen as a risk.

**Strategy (Val's direction).** Val pushed the team on *why* migrate Rage games to Nova at all. The team's rationale: build a cross-platform game library that runs on multiple boards (V1000, FP-SV7, RK3568) via their SDKs, and reduce the temptation to keep cutting new products from the ~25 existing Rage branches. **Val rejected migrating games en masse just to have a "park."** Instead: port the common Nova environment (liquid-glass frame, GamesElectScreen, setup screens) so the toolchain is ready, build **new** games on the new tools, and keep a conversion plan on hand to jump on only when a specific market/jurisdiction demands it.

**South Dakota.** The earlier idea of leaving South Dakota on Rage (because it is hard) was dropped. Plan: certify and release the current Rage version now so it goes to market; in parallel, fully port the South Dakota product (~10 games, new revision with liquid glass, new floats, keno added; likely +4 more → ~12) to Nova, and do a full certified replacement in about six months (~3 months to transition + ~3 months polishing). Val also told Igor **not** to bother finishing/certifying the standalone Kali Ocha.

**Next experiment.** Igor to attempt a harder migration: a **horizontal** game (more screens) from the South Dakota product — candidate "Nikena" (a regular game; "Crescent City Carnival" was also floated because its spin bonus math differs) — this time also porting **logic**, not just resources, and possibly a Georgia-product variant. The group reconvenes to measure success.

## Decisions Made

- **Do not migrate Rage games to Nova en masse.** Port the common Nova environment (liquid-glass frame, GamesElectScreen, setup screens) and build new games on the new tools; migrate old games only on-demand for a specific market. (Val)
- **The South Dakota product will be fully ported from Rage to Nova.** Current Rage version is certified/released now; a full certified Nova replacement follows in ~6 months. (Val)
- **Do not finish or certify the standalone Kali Ocha game.** (Val, rejecting Igor's suggestion)
- **Target timeline ≈ 6 months** for the South Dakota Nova replacement (~3 months transition + ~3 months polishing). (Val)
- **The next experiment targets a horizontal game and logic migration**, not another vertical re-skin. (Agreed)
- **Reconvene August 17, 2026** to assess the horizontal South Dakota migration. (Val — this superseded an earlier Aug 13 proposal made mid-meeting.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Metelski | Run the next migration experiment: convert a **horizontal** South Dakota game (candidate "Nikena"; "Crescent City Carnival" alt) to Nova, this time also porting game **logic**, not just resources | Aug 17, 2026 | High | Harder than the vertical re-skin; more screens |
| 2 | Igor Metelski | Load the converted resources onto the actual machine running the reference game and measure appearance + performance on target hardware (RK3568 "76" and/or V1000) | Aug 17, 2026 | Normal | Agreed as the next verification step |
| 3 | Val Levitan | Reconvene the group to review success of the horizontal migration | Aug 17, 2026 | Normal | Val's own follow-up (owner — no correspondence draft) |

## Open Questions

- Whether the liquid-glass ("ликвид глаз") resources are shareable across games or game-specific — Irina noted designers may have built per-game custom backgrounds; **Anton** is the person who knows this approach and should be asked. (Irina / Pavel)
- Whether Claude can render localized video from dictionary text to preserve Nova's localization approach, versus reverting to Rage's dictionary method. (Igor / Alexander)
- How Claude will handle horizontal games with more screens and no clear scene-to-scene correspondence. (Igor)
- Real performance of migrated games on target hardware (RK3568 "76", V1000) — not yet measured. (Alexander)

## Dispatch Log

- 2026-08-04 07:08 ET — Booked "RAGE-NOVA_migration — review" for Aug 17, 2026, 8:00–9:00 AM ET (Teams) with Igor M., Pavel, Irina, Alexander, Evgeny; invitation body contains the Aug 3 summary, decisions, undertakings, and open questions (covers undertaking #3, Val's reconvene).

---
*Processed from Teams transcript on August 3, 2026 (scheduled meeting-watcher run)*
*Source meeting: RAGE-NOVA_migration*
