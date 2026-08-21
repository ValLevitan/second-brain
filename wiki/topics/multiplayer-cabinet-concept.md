---
type: topic
title: Multiplayer / back-to-back two-player cabinet concept
date: 2026-08-14
aliases: [multiplayer cabinet, back-to-back cabinet, dual-station cabinet, two-player slant-top, back-to-back slant-top, Pacman-style table, one machine two positions, simultaneous play, multi-play, Wonder 4, Twin Bison Quad, tournament game]
source-count: 4
open-commitments: 0
open-questions: 2
---

# Multiplayer / back-to-back two-player cabinet concept

A new JVL cabinet direction that emerged across two August 2026 game-team meetings: a single cabinet with **two players seated back-to-back**, each with their own screen, meters and bill device, sold as **one machine (one serial number, two play positions)**. [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] set the vocabulary; [[wiki/people/val-levitan.md|Val]] drove the concept; [[wiki/people/juan-martinez.md|Juan Martinez]] supplied the regulatory precedent; [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] raised the accounting/SAS obstacle. The consolidated cabinet direction is on [[wiki/decisions/2026-08-21-back-to-back-two-player-cabinet-direction.md]].

## Vocabulary (Michael, Aug 21)

- **"Simultaneous play" / "multi-play"** = one player playing up to four games at once on a four-quadrant screen (Aristocrat's **Wonder 4**). [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]
- **"Multi-game"** = one cabinet offering several games for the player to choose from — an established industry term, so the team will not reuse it for anything new. [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]
- **"Multiplayer"** = more than one player playing one of JVL's cabinets at the same time — the term the group adopted for the back-to-back concept. [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]

## Aug 14 2026 — the "killer application": a dual-station single cabinet

In the [[wiki/meetings/2026-08-14-nova-capability-wishlist.md|NOVA Capability Wishlist]] session Val floated a two-sided cocktail/slant table (following Michael's "reimagine the form factor" prompt). The group converged on **one cabinet with two curved screens back-to-back on opposite sides, one CPU board, two players with separate balances and separate bill validators, sold as ONE machine with one serial number**, plus a shared/tournament bet between the two stations. Juan confirmed regulators accept this — the same premise as an electronic **roulette / craps** table ("I've done it 1000 times along with every major operator … treated as one machine"). Val: **"Bravo, that's the killer application"** — pursue it as soon as possible. [[raw/Meeting_Transcript_NOVA_Capability_Wishlist-August-14-2026-Part_2.md]]

Alongside it the group agreed the NOVA platform should **support simultaneous multi-game play** — up to four games (same or different) on one split screen, and up to four reel-bundles within one game (a "Twin Bison Quad", Aristocrat "Wonder Four" style) — with the [[wiki/topics/nova-platform-architecture.md|LGS]] spinning them milliseconds apart rather than truly in parallel. The system should support it, but it is not being built immediately. [[raw/Meeting_Transcript_NOVA_Capability_Wishlist-August-14-2026-Part_2.md]]

## Aug 21 2026 — back-to-back slant-top chosen; multi-play killed

The [[wiki/meetings/2026-08-21-multiplayer-cabinet-concepts-nova-strategy.md|Aug-21 strategy call]] narrowed the physical design. Val laid out three ideas: (1) the four-quadrant one-player concept, (2) a single 55-inch vertical screen shared by two players, and (3) a back-to-back "Pacman-style" slant-top where two players sit on opposite sides, each with their own screen, meters and bill devices. [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]

- **Chosen direction: the back-to-back slant-top**, especially for Georgia gas stations where floor space is tight. Back-to-back avoids the ergonomic problems Michael saw years ago at Bally with **"Dual Vision"**, where two players sat next to each other sharing a screen and argued over whose money and meters were whose. Each player gets a **single monitor plus a VDEC**; Val said the engineers confirmed the **FP7 can drive it** (four monitors total, no special design). Michael suggested a **triangular / 45-degree angled topper** so the unit can sit against a wall and still be seen from the floor — Val liked it. [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]
- **Dropped:** Juan's wraparound convex screen (distortion / focus / chromatic-aberration problems), and the shared-single-screen two-player ideas. [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]
- **"Multi-play" (one player, four simultaneous games) was killed.** Two reasons Michael gave: symbols become "infinitesimally small" and confusing on screen; and the math discourages players (a $4 total bet that often returns only cents feels punishing, like multi-hand poker). NOVA should still be **specified with enough graphics/CPU/memory horsepower to add it later** if it ever becomes popular — so the team never has to say "we never asked for that capability." [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]

## The "one machine" prize and the SAS obstacle

The commercial value is getting regulators to treat the back-to-back unit as **one machine** (one serial number, two positions): a location capped at, say, 5–7 machines could then install more play positions. Juan cited precedent (electronic roulette counted as one table; **Interblock, Alpha Street**). [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]

The blocker is accounting/regulatory. Efim studied the **SAS protocol** and found it **assumes games start and finish sequentially** ("starts and finishes, starts and finishes"), so two players playing independently and overlapping in time does not fit cleanly — two players means two balances, two histories. Efim: it is not disallowed in every implementation, but "if I would build a host, I would disallow it, and nobody would say I am doing it wrong." Juan pointed at the **online space** (GLI regulates concurrent play there) and suggested consulting **GLI and Eclipse** for a workaround; Efim cautioned they rarely recommend workarounds and the team may have to find its own. Efim's position: even if it cannot be certified as one machine, back-to-back is still worth building for the floor-space saving. [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]] [[raw/Meeting_Transcript_NOVA_Capability_Wishlist-August-14-2026-Part_2.md]]

## Tournament / personal-challenge mode (concept, parked)

Val is interested in a **tournament / personal-challenge mode** on the two-player slant-top — e.g. one player invites a second to sit down for a side bet; JVL manages it but the outcome is between the players. Juan sketched a trigger event that auto-qualifies both players into a shared bonus. Michael cautioned that anything interrupting a player's **"velocity" / flow** (side bets, second-screen content) has historically slowed play; he tied JVL's strong recent numbers to the **simplified nudge**, which speeds decisions. No decision — parked as a concept. [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]] [[raw/Meeting_Transcript_NOVA_Capability_Wishlist-August-14-2026-Part_2.md]]

## Open questions

- Can a back-to-back two-player cabinet be certified as **ONE machine / one serial number**? Blocked by the SAS protocol assuming sequential game start/finish per position (Efim). May require consulting GLI and Eclipse for a workaround. [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]
- Is there a viable **tournament / personal-challenge mode** on the two-player slant-top that does not hurt play velocity? (Raised by Val; Michael cautioned.) [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]

## Sources
- [[raw/Meeting_Notes_NOVA_Capability_Wishlist-August-14-2026-Part_2.md]]
- [[raw/Meeting_Transcript_NOVA_Capability_Wishlist-August-14-2026-Part_2.md]]
- [[raw/Meeting_Notes_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]
- [[raw/Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]
