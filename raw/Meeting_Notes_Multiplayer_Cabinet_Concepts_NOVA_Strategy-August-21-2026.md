# Meeting Summary — Game_Development (Multiplayer Cabinet Concepts & NOVA Strategy)
**Date:** August 21, 2026, 1:54–2:47 PM Eastern
**Duration:** ~52 minutes
**Attendees:** Val Levitan, Michael Gottlieb, Juan Martinez, Efim Podvoiski
**Raw transcript:** [[Meeting_Transcript_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026]]

## Summary

This was a strategy call on new cabinet concepts, the move to the NOVA platform, and the Georgia market. Felipe and Andrei were not on this call; the team is waiting for their separate report on the Georgia V3 software from the trade show.

**Cabinet concepts.** Michael set the vocabulary. "Simultaneous play" (Aristocrat's Wonder 4) means one player plays up to four games at once on a four-quadrant screen. "Multi-game" means one cabinet offering several games to choose from — the industry already uses this term, so the team will not reuse it for anything new. Val laid out three physical ideas: (1) the four-quadrant one-player concept, (2) a single 55-inch vertical screen shared by two players, and (3) a back-to-back "Pacman-style" slant-top where two players sit on opposite sides, each with their own screen, meters, and bill devices.

The team converged on the **back-to-back slant-top** as the right direction, especially for Georgia gas stations where floor space is tight (locations are limited to a small number of machines). Back-to-back avoids the ergonomic problems Michael saw years ago at Bally with "Dual Vision," where players sat next to each other and disputes arose over whose money and meters were whose. Each player gets a single monitor plus a VDEC; Val said the engineers confirmed the FP7 can drive this (four monitors total, no special design). Michael suggested a triangular / 45-degree angled topper so the machine can sit against a wall and still be seen from the floor — Val liked this. Juan floated a wraparound convex screen; the group dropped it because of distortion and focus problems.

**One machine vs. two.** The big prize is getting regulators to treat the back-to-back unit as ONE machine (one serial number, two positions). That would let locations capped at, say, 5–7 machines install more play positions. Precedent exists (electronic roulette counted as one table; Interblock, Alpha Street). The blocker is accounting/regulatory: Efim studied the SAS protocol and it assumes games start and finish sequentially, so two players playing independently and overlapping in time does not fit cleanly. This is unresolved — the team may need to consult GLI and Eclipse for a workaround.

**What was killed.** The team agreed NOT to build "multi-play" (one player, four simultaneous games). Reasons: symbols become tiny and confusing on screen; and the math discourages players (a $4 total bet that often returns only cents feels punishing, like multi-hand poker). The only ask is that NOVA be specified with enough graphics/CPU/memory horsepower to add it later if it ever becomes popular — so the team never has to say "we never asked for that capability." Shared-single-screen ideas were also dropped.

**Tournaments.** Val is interested in a tournament / personal-challenge mode on the two-player slant-top — e.g., one player invites a second to sit down for a side bet, JVL manages it but the outcome is between the players. Michael cautioned that anything interrupting a player's "velocity" / flow (side bets, second-screen content) historically slowed play; he tied strong recent numbers to the simplified nudge, which speeds decisions. No decision — parked as a concept.

**Sales / Georgia color.** Val reported strong reception at the show for the Flex recycler positioned as a "redemption center with built-in ATM" — reframing bill acceptors/printers (a cost center) into a profit center with per-transaction ATM fees and recurring monthly revenue. One operator (Arc) pulled in its CEO and CFO mid-pitch. Val sees the combination of Flex IQ, Flexport, SMIBs, recycler/ATM, and the future back-to-back slant-top positioning JVL for substantial business in a ~45,000-machine market, and put JVL "within three years of a smashing success." He also noted the ongoing trial looks solid despite three bugs found, and wants LTE modems in every machine to feed service, performance, and player-preference intelligence.

**Nebraska.** Michael proposed replacing the Golden Husk progressive (a quick modification of the Peach progressive) with the Match-3 progressive that is doing well in Georgia — a visual upgrade. Val gave full support. Efim will do it (~3 weeks, has bandwidth). [Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.].

## Decisions Made

- **Do NOT build "multi-play" (one player, four simultaneous games / Wonder 4).** Graphically confusing and mathematically discouraging; hasn't performed for Aristocrat. NOVA should still be specified with enough graphics/CPU/memory headroom to add it in future. (Michael, Juan, Efim, Val all agreed.)
- **Drop shared-single-screen two-player concepts.** Back-to-back is the chosen physical direction. (Efim proposed, group agreed.)
- **Direction: back-to-back two-player slant-top cabinet, single monitor + VDEC per player, with a triangular/angled topper.** FP7 can drive it. Target market: Georgia gas stations. (Val, with Michael/Juan input.)
- **NOVA migration is the priority. October 1 = begin allocating resources to NOVA; September = polish the MVP capabilities for the first NOVA release.** Work must be written as capabilities / use cases / requirements with no room for engineer interpretation. (Val.)
- **Bring the Match-3 progressive to Nebraska, replacing the Golden Husk progressive.** To be logged in Jira as a product capability. (Michael proposed, Juan agreed, Val in full support.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Efim Podvoiski | Build the Match-3 progressive for Nebraska (replace Golden Husk); create the Jira task, described as a capability | ~3 weeks [Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.] | Normal | Match-3 is well received in Georgia; visual upgrade over Golden Husk |
| 2 | Juan Martinez | Create the Jira product-capability / requirement entry for the Match-3-to-Nebraska work | TBD | Normal | "I'll do a product capability in the requirement" |
| 3 | Engineering (NOVA) | Prepare NOVA MVP capabilities for polish through September; spec enough graphics/CPU/memory horsepower to support future multi-play | September (resources shift Oct 1) | High | No room for engineer interpretation; capability/use-case driven |

## Open Questions

- Can a back-to-back two-player cabinet be certified as ONE machine / one serial number? Blocked by SAS protocol assuming sequential start/finish per game (Efim). May require consulting GLI and Eclipse for a workaround. (Raised by Juan and Efim — no owner assigned.)
- What did Felipe, Andrei, or Sebastian observe in the Georgia V3 software at the show that might require engineering changes? Awaiting their report. (Raised by Juan.)
- Is there a viable tournament / personal-challenge mode on the two-player slant-top that does not hurt play velocity? (Raised by Val; Michael cautioned.)

## Dispatch Log

---
*Processed from Teams transcript on August 21, 2026 (scheduled meeting-watcher sweep)*
*Source meeting: Game_Development — August 21, 2026*
