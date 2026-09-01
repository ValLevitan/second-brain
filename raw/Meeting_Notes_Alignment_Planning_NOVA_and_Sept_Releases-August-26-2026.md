# Meeting Summary — Alignment_planning
**Date:** August 26, 2026, 7:40–8:36 AM (Eastern)
**Duration:** ~55 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026]]

## Summary

Val called from the Georgia office after the trade show. The meeting was in Russian and covered pricing strategy, the two September 1 releases, the NOVA migration plan, a staffing/succession problem, and test-bench setup.

**Georgia show and pricing theory.** Val said JVL machines look as good as or better than Light & Wonder and Aristocrat on the floor, but the competitors earn more. His theory: JVL runs a high RTP (about 92–93% including progressive) and a low minimum bet (25¢), so during peak hours — when all machines are occupied — JVL cannot make the same netwin, even if the machines are popular. Pavel corrected the math (loss per spin is 0.25 × (1 − RTP), about 2.5¢, not 25¢). Operators have long told Val that JVL does very well in the periphery but is weaker in Atlanta's core. Val's proposed fix, once the September mods allow location-based approval: a kind of geo-fencing — in urban/Atlanta locations lower RTP toward ~90–91% and raise the minimum bet (e.g. 30¢, keep 25¢ only as a starter game); in the periphery keep 25¢ on most games with a couple at 40¢. Pavel offered an alternative: during peak hours, hide/disable the lowest bet button (new functionality). Val liked it but **parked both** for the game-design team — no decision made.

**Transaction OCR / Recycler + Flex Port.** The transaction recycler demo was a hit at the show; Georgia lottery's chief legal counsel was reportedly excited (and, per Andrei's account, it caused a stir — JVL cannot sell the kiosks yet but promised a legal version soon). A possible Texas install is emerging: a recycler plus 25 Flex ports at a location currently running Pyramid printers. Genadi is sourcing a larger-capacity recycler (CPI, likely a BNR model); Pavel warned the vendor library will not be compatible and the team will have to reverse-engineer it as they did on the ARM platform — no ready solution, and remote work on it is hard. Ideas raised: a better/remote development station, and bringing in Sebastian (a more technical hire relocating from Miami, starting in about a week).

**NOVA migration plan.** Val said the move to NOVA is proving easier than expected because Claude handles much of it and the team is engaged. Resources free up around October 1. Sequence: deliver the September 1 items first (SALTA/VLT2 and V3 Georgia COAM), then use September to narrow capabilities to MVPs, sketch them in Jira, and distribute the work, with developers starting on NOVA from ~Oct 1. Val is unsure what the first NOVA release should be and wants two tracks in parallel: (1) SALTA/VLT2 as a direct Rage→NOVA migration, and (2) a D27 Georgia COAM NOVA version reworking popular games and moving from the peach progressive to the new "Match 3" progressive. Designers would have to support the same game on both vertical and horizontal cabinets. The open concern is splitting QA resources across both tracks.

**Igor Metelsky conversion demo.** Pavel reported Igor has converted a game and is nearly ready to show results (he wanted to get progressive spins working fully). Val scheduled a review meeting during the call.

**Juan Martinez — health and succession (sensitive).** Val disclosed that Juan is seriously ill and the illness has turned for the worse; he does not think Juan can be relied on going forward (at most through the end of the year). This is a major gap for capabilities knowledge and for "pushing" GLI/lottery submissions with authority. Michael Gatlif independently suggested Andrei Klimovich as a long-term candidate for Juan's role; Val sees Klimovich as the only internal person who could eventually grow into it, with support from Efim and Michael, though not a near-term replacement. On who can "push" submissions now, the team felt Ivan can communicate and get submissions done but not push with Juan's force; no one internal fully covers it. No decision — parked. Val urged Pavel and Irina to work intensively with Juan while he is still available.

**Capabilities → MVP → Jira ownership.** Val placed responsibility for polishing the capabilities set, extracting the MVPs, sketching them in Jira, and aligning across the whole company on Pavel and Irina, for September, with developers starting Oct 1. He pushed them hard to communicate and document more actively and to stop thinking in terms of "Minsk vs the rest" — the company now works as one virtual team.

**September 1 releases.** Irina raised that to lower the percentage on the 15 Georgia games (currently 90/92/94% plus ~2–2.5% progressive) they likely need an 88% option that does not yet exist for some games; Efim would have to add it. Val agreed this should be done and folded into the release; he expects it to be quick for Efim. Both products are near-ready; South Dakota (SALTA/VLT2) is almost finished and on track for September 1 if nothing else surfaces.

**Submissions and cc discipline.** Ivan should start the SALTA/VLT2 (South Dakota) submission conversation now and keep Val and Juan copied on all correspondence, so Val can step in with a call if he sees the schedule slipping.

**L&W SAS test bench.** The certifier (Lonnie) previously required buying the Light & Wonder test station; it was shipped from the closed South Dakota office to Georgia. Elizabeth needs to set up the bench so the team can run the tests the certifier used to run — done thoroughly, to keep the trust that lets JVL self-test (otherwise Lonnie reverts to a slower, costlier process). Pavel proposed additionally using Claude to capture how the L&W player-tracking/SAS system behaves and build a full emulation on VMs in Minsk, to add to the automated test suite and to diagnose field issues. Sebastian and Anibal (relocated from Peru) can help with the technical testing.

**Georgia–Minsk network link.** Pavel proposed that IT (Andrei and Dima) create a direct channel joining the Georgia office LAN to the Minsk network so remote operations feel local. Val fully agreed and asked Pavel to raise it with Andrei Tekin.

*Note: several names are phonetic from Russian speech-to-text and may be spelled approximately.*

## Decisions Made

- **Add a lower (~88%) RTP option to the 15 Georgia COAM games and include it in the release** — needed to reduce the percentage; Efim to implement. (Val, agreeing with Irina)
- **Target September 1 for both releases — SALTA/VLT2 (South Dakota) and V3 Georgia COAM** — both near-ready; South Dakota almost finished. (Val, Irina)
- **Pavel and Irina own the capabilities → MVP → Jira-sketch process through September and must align it across the whole company; developers begin NOVA work ~Oct 1.** (Decided by Val)
- **Ivan to open the SALTA/VLT2 submission conversation now, with Val and Juan cc'd on all correspondence.** (Decided by Val)
- **Pursue a direct Georgia–Minsk network link** so remote work behaves like local; Pavel to raise with IT (Andrei Tekin). (Val, Pavel)
- **Set up the L&W SAS test bench in the Georgia office** (Elizabeth) and test thoroughly to preserve the certifier's trust. (Val, Pavel)
- **Genadi to source a larger-capacity recycler (CPI/BNR) and ship it to Minsk** for reverse engineering. (Val, Pavel)
- **Meeting scheduled during the call:** SDVL T2 / NOVA conversion review, Friday Aug 28, 9:00 AM ET, inviting Igor Metelsky and Horetski. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Efim | Add the lower (~88%) RTP option to the 15 Georgia COAM games and hand off for testing | Before Sept 1 release | High | Some games lack an 88% option today |
| 2 | Irina | Contact Efim today about the percentages; put SALTA/VLT2 on test | Test ~next week; release target Sept 1 | High | South Dakota almost done |
| 3 | Elizabeth | Set up the L&W SAS test bench (SD VLT) in the Georgia office | ASAP | High | Test kit already shipped to Georgia; Val on-site to oversee |
| 4 | Ivan | Open the SALTA/VLT2 (South Dakota) submission conversation with the certifier, cc Val and Juan on everything | Start today/tomorrow | High | Certification process takes time; start early |
| 5 | Pavel + Irina | Polish the capabilities set, extract MVPs, sketch in Jira, align across the company | Through September (dev start ~Oct 1) | High | Core responsibility Val assigned to both |
| 6 | Pavel | Raise the direct Georgia–Minsk network link with IT (Andrei Tekin) | Today | Normal | Enables local-feeling remote operations |
| 7 | Genadi | Source a larger-capacity recycler (CPI/BNR) and ship to Minsk for reverse engineering | TBD | Normal | Already ordering; vendor library not compatible |
| 8 | Pavel | Prepare/present Igor Metelsky's conversion result at the Friday meeting | Fri Aug 28, 9:00 AM ET | Normal | Igor's converted game nearly ready |
| 9 | Val | Work with the game-design team on the Georgia pricing strategy (geo-fencing vs peak-hour bet blocking) | TBD | Normal | Parked pending design-team input |

## Open Questions

- **Pricing strategy** — location-based RTP + minimum-bet changes (geo-fencing) vs disabling the lowest bet button during peak hours. Parked for the game-design team; no decision. (Val proposed; Pavel offered the alternative)
- **First NOVA release and running two migrations in parallel** (SALTA→NOVA and D27 Georgia COAM) — how to split QA resources across both. Unresolved. (Val, Pavel, Irina)
- **Juan Martinez succession** — who covers capabilities knowledge and who can "push" submissions with authority. No decision; Andrei Klimovich floated as a long-term candidate. (Val)
- **Recycler remote development** — how to make reverse-engineering the new recycler reliable when the device sits remotely. (Pavel)

## Dispatch Log

---
*Processed from Teams transcript on August 26, 2026 (scheduled meeting-watcher run)*
*Source meeting: Alignment_planning*
