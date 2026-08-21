---
type: decision
title: Cabinet direction — back-to-back two-player slant-top; multi-play killed but NOVA keeps the headroom
date: 2026-08-21
aliases: [back-to-back two-player cabinet direction, slant-top cabinet direction, kill multi-play, dual-station cabinet decision]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
---

# Cabinet direction — back-to-back two-player slant-top; multi-play killed but NOVA keeps the headroom

On the [[wiki/meetings/2026-08-21-multiplayer-cabinet-concepts-nova-strategy.md|Aug 21 2026 strategy call]] ([[wiki/people/val-levitan.md|Val]], [[wiki/people/michael-gottlieb.md|Michael Gottlieb]], [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/efim-podvoiski.md|Efim Podvoiski]]) the team settled the physical cabinet direction that the [[wiki/meetings/2026-08-14-nova-capability-wishlist.md|Aug-14 wishlist]] had opened. The full concept, vocabulary and the one-machine/SAS obstacle are on [[wiki/topics/multiplayer-cabinet-concept.md]]. [[raw/Meeting_Notes_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]] [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]

## What was decided

- **Direction: a back-to-back two-player slant-top cabinet** — a single monitor plus a VDEC per player, with a triangular / 45-degree angled topper so the unit can sit against a wall and still be seen from the floor. Val said the engineers confirmed the **FP7 can drive it** (four monitors total, no special design). Target market: Georgia gas stations, where floor space is tight. (Val, with Michael/Juan input; Efim endorsed back-to-back.) [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]
- **Do NOT build "multi-play" (one player, four simultaneous games / Wonder 4).** Graphically confusing (tiny symbols) and mathematically discouraging (a $4 bet often returning cents); it has not performed for Aristocrat. But NOVA should still be **specified with enough graphics / CPU / memory headroom to add it in future** — so the team never has to say "we never asked for that capability." (Michael, Juan, Efim, Val all agreed.) [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]
- **Drop the shared-single-screen two-player concepts** (the 55-inch shared vertical screen, and Juan's wraparound convex screen). Back-to-back — each player on their own screen — is the chosen physical direction, and it also resolves the ergonomic "whose money / whose meter" disputes JVL hit at Bally with "Dual Vision." (Efim proposed killing the dead ideas; group agreed.) [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]

This complements the [[wiki/topics/nova-platform-architecture.md|Aug-14 platform decision]] that NOVA should *support* simultaneous multi-game play (up to four games / four reel-bundles, LGS spinning them milliseconds apart) as a latent capability, even though it is not being built now.

## Why it matters

The commercial prize is getting regulators to treat the back-to-back unit as **one machine (one serial number, two positions)**, letting a location capped at 5–7 machines add more play positions. That is blocked by the SAS protocol (see the open question), but even without one-machine certification the back-to-back design saves floor space and is worth building (Efim). Precedent for one-machine treatment: electronic roulette / craps tables (Interblock, Alpha Street), per Juan. [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]

## Open questions

- Can the back-to-back cabinet be certified as **ONE machine / one serial number**? The SAS protocol assumes sequential game start/finish per position; two independent, time-overlapping players do not fit cleanly. May require consulting GLI and Eclipse for a workaround. (Efim, Juan — no owner assigned.) Tracked on [[wiki/topics/multiplayer-cabinet-concept.md]]. [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]

## Sources
- [[raw/Meeting_Notes_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]
- [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]
