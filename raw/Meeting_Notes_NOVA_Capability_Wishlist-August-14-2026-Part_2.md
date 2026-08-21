# Meeting Summary — NOVA Capability Wishlist (Segment 2 of 2)
**Date:** August 14, 2026, 2:09 PM ET
**Duration:** ~91 minutes (main recording session)
**Segment:** Segment 2 of 2
**Attendees:** Val Levitan, Michael Gottlieb, Juan Martinez, Lena Zhukova, Efim Podvoiski
**Raw transcript:** [[Meeting_Transcript_NOVA_Capability_Wishlist-August-14-2026-Part_2]]

## Summary

The main brainstorm on what each discipline wants from the Nova platform, followed by a wide-ranging machine-design discussion. (Opening in [[Meeting_Notes_NOVA_Capability_Wishlist-August-14-2026|Segment 1]].)

**Wishlists by discipline:**
- **Michael (product):** math templates / a sandbox that loads pre-existing math models so behaviors and parameters (e.g. free-spin frequency) can be tried on the fly without touching a programmer; a modular ("Lego") code base so features can be unplugged and swapped instead of becoming spaghetti; better debug tools and logging (ability to see what happened a few cycles before a crash); and remote Wi-Fi login to view a machine's performance — even just a percentage breakdown of which games are most/least played.
- **Lena (visual/design):** a properly working Miranda design environment with manifest; toppers included in the build; a much more advanced show mode; finished framework dialogues; and — most important to her — integrating the math game launcher into the design environment so artists can run real spins and change art assets inside Miranda and see results immediately, before making a build (turning experiments that need a build into half-hour tweaks).
- **Efim (math):** a better, faster prototype path; and the "holy grail" of seeing individual player behavior at the machine (not just averages) — while acknowledging this needs backend/player-tracking that does not exist in current markets.
- **Juan (5 written points, to be emailed):** game recovery via a constantly-written backup memory so a crashed game can be recovered in any state without a full reinstall (which today means wiping data, alerting the regulator, and delayed payouts); modular device compartments so one device failure (e.g. a printer) doesn't take down the whole cabinet; a jurisdictional layer separated from the base game; and RAS "evolving" so a local operator can make manual setting changes (e.g. time zone) without needing a new file from JVL.

Val reframed the exercise as open "what if" thinking (his Elon Musk / buy-a-Texas-town framing) and pushed people to state desired outcomes rather than engineering solutions.

**Machine-design run-through (Val polling for direction):**
- 3D no-glasses toppers — parked (not needed for street focus; 3D historically makes people sick).
- Promo credits in street locations — parked (needs player tracking and raises jurisdictional issues; "not all business is good business" — free play draws non-customers who crowd out regulars, per the Treasure Island and Hard Rock examples).
- At-home machine as a dumb terminal to a legal offshore server for real money — parked (huge project; needs player tracking and state-by-state approval; plus social/psychological risks).
- Camera / player identification — interesting but parked over regulatory and privacy concerns; the anonymous alternative is posting a screenshot of the machine's own jackpot lockup screen (no human in frame).
- Social-media win sharing — rejected (players are private about money).

## Decisions Made

- **Killer application (agreed, pursue as soon as possible): a dual-station single cabinet.** One cabinet with two curved screens back-to-back on opposite sides, one CPU board, two players with separate balances and separate bill validators, sold as ONE machine with one serial number, and a shared/tournament bet between the two stations. Juan confirmed regulators accept this (same premise as electronic roulette/craps tables). Val: "Bravo, that's the killer application."
- **The platform will support simultaneous multi-game play** — up to four games (same or different) on one split screen, and up to four reel-bundles running simultaneously within one game (Twin Bison Quad / Aristocrat "Wonder Four" style). The LGS spins them milliseconds apart rather than truly in parallel. The system should support it, though it isn't being built immediately.
- **Hardware: go with the higher-capability CPU/graphics package and a new cabinet; scrap the cheaper board; unrestricted design capability.** (Moore's Law logic — don't ship an 8-year-old CPU.)
- **Mechanical buttons over a VDEC** — spend the money on the CPU/motherboard, not the VDEC; competitors and street markets do fine without it.
- **Toppers: removable/optional**, seamlessly joined to the top monitor, never a permanent fixture, so extra height never costs a sale.
- **Perimeter lights: yes — a definitive-line perimeter light tied to game activity** (celebratory "carnival" lighting); avoid garish two-inch Light-&-Wonder-style strips and avoid distracting lighting around the VDEC.
- **No wedge machines / LCD-screen wedges** — waste of money and space in street rows of 4–7 machines.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Juan Martinez | Email his 5 platform points (game recovery, modular device compartments, jurisdictional layer, RAS evolution), renumbered in MVP order, to the group | TBD ("shortly") | High | He said he has them written up |
| 2 | Michael Gottlieb | Collate a library of reusable math templates (e.g. Twin Bison double-reels) as starting points for new games | TBD | Normal | Foundation for faster prototyping |
| 3 | Efim Podvoiski | Work with Michael on a way to quickly prototype gameplay/mechanics | TBD | Normal | Goal: cut math-change turnaround from ~2 weeks to ~half a day |

## Open Questions

- How player behavior/data could be tracked in current markets (Georgia and others) where no player-tracking system exists.
- Whether and where at-home real-money terminals could be hosted and approved (parked).

## Dispatch Log

---
*Processed from Teams transcript on August 14, 2026 (scheduled meeting-watcher run).*
*Source meeting: Game_Development (NOVA Capability Wishlist) — August 14, 2026, Segment 2 of 2*
