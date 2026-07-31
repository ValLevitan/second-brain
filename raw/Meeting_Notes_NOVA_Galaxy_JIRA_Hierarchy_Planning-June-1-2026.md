# Meeting Summary — Scheduling NOVA / Galaxy Work (JIRA Hierarchy Planning)
**Date:** June 1, 2026, 3:34 PM Eastern
**Duration:** ~1h 17m
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko

## Summary

**The big picture being planned.** A large machine release is coming under three umbrellas: FP7 (new hardware/processor), NOVA (platform), and Galaxy (web services). The new machines were previously labelled "Flex Slim"; industrial design is done and now needs real implementation. The shift is big: new FP7 machines, new platform, Galaxy web services, new cabinet design, plus a move off C++ to Rust. One service still doesn't run smoothly and needs polishing. A game library of some depth is needed — they can't launch on one game. Everything has to land on a single day, so they can't stop to do other work until then.

**NOVA hardware stack.** NOVA goes on the FP7 board. They add an LTE modem and a data collector ("blackbox"). Val now sees the data collector as much bigger — a self-contained device that collects detailed player-session data. The box sits with a data amplifier and the new speaker set Gennady built (already done), on the new industrial design posted in Confluence. NOVA talks to the gaming side.

**Transaction Galaxy.** Ships July 1 in beta. It runs on a Rockchip RK3568 platform — an assembled OS with utilities/scripts (currently runs Flex IQ; Recycler is next). That OS/SDK bundle still needs a proper name (currently "platform-SDK-3568"). Transaction Galaxy is the set of web services that connect to it.

**The core problem — JIRA hierarchy.** None of this is laid out in JIRA yet, and the current hierarchy doesn't fit. Today's products sit in separate folders, so it's hard to pull everything to one release date. Capabilities don't drop cleanly into the timeline view. There's also a standing disagreement: Dmitri Kovalchuk (Dima) wants Galaxy tied to a *platform*; the designers want it tied to the *game* (they care when a game ships). Val wanted the group's read on what can and can't be changed before they start writing it all up — because breaking the live hierarchy means manual re-linking.

**The model they worked out (to prototype, not yet locked).** Move to **Product → Capability → Feature**, with Requirements *linked* (for reference/audit), not nested. Features stay the unit of work; requirements never close. The old Value Stream / Initiative / Hardware levels go away; ~3–4 levels removed, one added (Capability).

- **Top-level streams** (the former "value streams"): **NOVA**, **Gaming Galaxy**, **Transaction Galaxy** — running in parallel.
- **Under Transaction Galaxy:** Flex IQ Cabinet (hardware merged into the product level), Payment Hub, Billing Orchestration, Authentication, and other services → each with Capabilities → Features.
- **Under NOVA:** LGS, Progressive, Sound, the individual games (GCOAM, Kaiocho, Dragunov Rain, Polar Bear, etc.), and a **Framework** product for capabilities common to all games → Capabilities → Features.
- Game **Concept / Design / Production** collapse into Production (link to ready artifacts for concept/design). Game production effectively becomes NOVA.
- **Capabilities are driven by market/jurisdiction** (Georgia, Florida, Texas) — legal and market requirements get linked to the capabilities.

**Next step.** Prototype all of this in the JIRA sandbox Dima already built, before touching the live hierarchy. Working session set for June 2 at 8:00 AM ET with Val, Pavel, Irina, and Dmitri (Lena excluded for now — she'll try it once it's ready).

## Decisions Made

- **Keep the name "Galaxy"** for the web-services platform. (All three agreed — Val wanted one settled name.)
- **Split Galaxy into two parallel streams: Transaction Galaxy and Gaming Galaxy.**
- **Adopt Product → Capability → Feature**, with Requirements linked, not nested. (Reason: lets them parallelize features and tie work to market requirements without breaking the timeline view.)
- **Top-level streams = NOVA, Gaming Galaxy, Transaction Galaxy.**
- **Merge the hardware level into the product level** (e.g., "Flex IQ Cabinet"); drop the standalone "Initiative" and "Hardware" levels.
- **Collapse game Concept/Design/Production into Production**, folding into NOVA.
- **Prototype in Dima's sandbox first**, before changing the live JIRA hierarchy. (Reason: changing live means manual re-linking and risk of breaking existing links.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Run the sandbox working session to build the new hierarchy live; invite already sent | June 2, 2026, 8:00 AM ET | High | Validate the model before touching live JIRA |
| 2 | Dmitri Kovalchuk (Dima) | Bring and demo the JIRA sandbox he built; lead the hands-on modeling of the capability hierarchy | June 2, 2026 | High | Sandbox exists but no one has used it yet |
| 3 | Val, Pavel, Irina, Dmitri | Model the agreed hierarchy in the sandbox (top streams → products/services → capabilities → features; requirements linked) | June 2, 2026 | High | Lena excluded for now |

## Open Questions

- What "platform" actually means — the Dima-vs-designers disagreement (tie Galaxy to a platform vs. to the game). The two-stream split helps but doesn't fully settle it.
- A proper name for the Rockchip RK3568 OS/SDK bundle (currently "platform-SDK-3568").
- Whether a dedicated **Framework** product is needed under NOVA (Pavel leans yes).
- How designers will track the concept/design phases once those levels are collapsed into Production.
- When to bring Lena into the modeling (now vs. once it's working).

---
*Processed from Teams transcript. Source meeting: Scheduling_NOVA_Galaxy_work — June 1, 2026.*
