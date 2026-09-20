---
type: topic
title: GA-COAM V3 game-crash bug ("Tilt-1")
date: 2026-08-11
aliases: [Tilt-1, Tilt-1 analysis, tilt one, Hero Safari error 1, GACOAM 2 crash, GA-COAM crash bug, new-family game crash, Max Bet bug, V.43 bugs]
source-count: 7
open-commitments: 2
open-questions: 3
---

# GA-COAM V3 game-crash bug ("Tilt-1")

A bug thread in the new GA-COAM game family (variously called the "V3" games / "V.43" version-two cabinets) on the ten field/trial machines, tracked here as the anchor for a storyline that plays out across several August 2026 meetings. It is the same reproduced fault the [[wiki/projects/georgia-market-rollout.md|Georgia rollout]] work refers to as troubling the second-wave trial cabinets. **"Tilt one" turned out to be a broad catch-all name QA uses for any unknown bug, not one defect** — by Aug 13 it had resolved into three separate bugs, and by Aug 14 the field fault's root cause was pinned to a Max-Bet timing conflict and fixed. (Source terms V2 / V3 / V.43 are used loosely across the calls; kept as spoken, not forced into one label.)

## Aug 11 2026 — the crash is reproduced

On a short call ([[wiki/meetings/2026-08-11-tilt1-game-crash-reproduction.md|Tilt-1 analysis]], 12:06 PM ET, in Russian; [[wiki/people/val-levitan.md|Val]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/pavel.md|Pavel Frolov]]) Irina and Pavel reported they can **reliably reproduce** a game crash. [[raw/Meeting_Notes_Tilt-1_Game_Crash_Reproduction-August-11-2026.md]]

- **The failure.** When a specific set of symbols lands on screen (a non-winning combination, shown in an image posted to the group chat), pressing **Spin** crashes the game immediately. Irina's spoken description of the error, as transcribed, is **"Hero Safari error 1"** (rendering uncertain — flagged, not a confirmed product/error name). Irina suspects a symbol is appearing in a position where it should not. [[raw/Meeting_Notes_Tilt-1_Game_Crash_Reproduction-August-11-2026.md]] [[raw/Meeting_Transcript_Tilt-1_Game_Crash_Reproduction-August-11-2026.md]]
- **The game and who built it.** The affected game is **GACOAM 2**, on which — per Irina — "Anton did most of the work." (Which Anton is not stated; by engineering context this is most likely [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], paired here with [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] — not owner-confirmed, flagged.) [[raw/Meeting_Notes_Tilt-1_Game_Crash_Reproduction-August-11-2026.md]] [[raw/Meeting_Transcript_Tilt-1_Game_Crash_Reproduction-August-11-2026.md]]
- **Reproducing it is treated as good news.** On the same-day [[wiki/meetings/2026-08-11-ga-coam-pipeline-trial-forecast.md|GA-COAM pipeline call]] Val called the reproduction "a positive sign" and set the response: immediately disable the problematic game if it can be isolated, fix the bug, and push the fix to fielded and second-wave machines; removing the game is a last resort. [[raw/Meeting_Notes_GA_COAM_Pipeline_Trial_Forecast-August-11-2026.md]]

## Aug 13 2026 — "tilt one" is really three bugs

On a short briefing call ([[wiki/meetings/2026-08-13-tilt1-bug-analysis-v43-coam.md|Tilt-1 bug analysis]], 9:05 AM ET; [[wiki/people/val-levitan.md|Val]], [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]]) Irina reported that when her Minsk QA team tried to reproduce the field "tilt one," they found **three separate bugs**, not one. Irina explained that "tilt one" is a **broad catch-all label** the team uses for any unknown bug, so it is not descriptive. [[raw/Meeting_Notes_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026.md]] [[raw/Meeting_Transcript_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026.md]]

- **Bug 1 — tilt when all games in a group are switched off.** The field can block a machine by sending a separate "disable" command per game (Irina said this is how it is done in South Dakota / Light & Wonder) rather than one block-the-whole-machine command. Because the product has three game groups and the system cannot show a group with no games, disabling every game in a group throws tilt one. [[raw/Meeting_Notes_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026.md]]
- **Bug 2 — an out-of-service workaround un-blocks a regulator-blocked machine.** A machine blocked by Interlock (the regulator) can be returned to operation by a technician going into setup, setting it out of service, exiting, coming back, and setting it to operation — the regulator's block is circumvented, which should not be possible. [[raw/Meeting_Notes_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026.md]]
- **Bug 3 — a blocked game returns after a power cycle.** A disabled game reappears and can be played on boot after the machine is powered off and on, even though it should stay disabled. As Juan put it, the power-on overrides the disable command possibly sent by the regulator. [[raw/Meeting_Notes_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026.md]]
- **Caveat and decision.** Val stressed that until the logs pulled from the actual field machine are read, no one can be sure the three QA-reproduced bugs are the same "tilt one" seen in Georgia. He **paused all implementation** (a display-side discussion about showing a blocked game as a greyed-out icon or a blank card, per a South Dakota screenshot Inna shared, was explicitly deferred) and made **investigating the field machine now in Felipe's Georgia office the most acute priority** — Felipe connects it to the internet, Pavel remote-accesses it (started the day before with [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]) and pulls logs. Val also asked, for the record, that in [[wiki/topics/nova-platform-architecture.md|NOVA]] the tilt be narrowly focused per function rather than a broad catch-all. [[raw/Meeting_Notes_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026.md]] [[raw/Meeting_Transcript_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026.md]]

## Aug 14 2026 — root cause found (Max Bet), fixed by Anton, shipping to the 10 machines

The next day ([[wiki/meetings/2026-08-14-tilt1-maxbet-bug-fix.md|Tilt-1 Max Bet bug fix]], 11:30 AM ET; [[wiki/people/pavel.md|Pavel]], [[wiki/people/irina-shishko.md|Irina]], [[wiki/people/juan-martinez.md|Juan]], [[wiki/people/val-levitan.md|Val]]) the team confirmed the field fault's root cause. [[raw/Meeting_Notes_Tilt-1_MaxBet_Bug_Fix-August-14-2026.md]] [[raw/Meeting_Transcript_Tilt-1_MaxBet_Bug_Fix-August-14-2026.md]]

- **Root cause — a Play/Max-Bet double-bet.** Dumps and reports showed a bet value that did not match what the player set: a player tried to play at 50 cents but the transaction history recorded a $3 bet. Irina reproduced it — **pressing Max Bet immediately after Play can register two bets in a row** (first the small bet, then the large max bet). After a reboot the game math and the submitted bet no longer agree, producing the bet/math conflict. Logs from the test machine matched production, and transaction-history screenshots (pulled with Elizabeth the day before) confirmed it; the conflict sits between Play and Max Bet. (This differs from the Aug-11 description of a crash on a non-winning symbol combination at Spin — the investigation converged here; the earlier symbol-combination account is kept as the team's earlier read, not a competing current claim.) [[raw/Meeting_Notes_Tilt-1_MaxBet_Bug_Fix-August-14-2026.md]]
- **Fix and how it ships.** Anton had already fixed the bug; Irina is compiling the fixed version. Pavel said the fix can be **injected on the current ISO** and is the one bug worth urgent delivery. **Decision (Val):** do it now — get [[wiki/people/felipe-miranda.md|Felipe]] to switch the fix onto the **10 field machines right away** (Val's concern is those 10 over the weekend); everything else is groomed, tested, and grouped with the **V3 release through Eclipse**, with new sales going to V3 and **V2 retired**. Deployment needs an ISO reinstall (same array assessments reusable); Juan cautioned a full install means a new co-MID requiring a call to Intralot, and customers may not permit changes on a Friday — Val agreed it probably won't happen Friday but wants the fix in hand regardless. [[raw/Meeting_Notes_Tilt-1_MaxBet_Bug_Fix-August-14-2026.md]] [[raw/Meeting_Transcript_Tilt-1_MaxBet_Bug_Fix-August-14-2026.md]]

## Open commitments

- [ ] Pavel Frolov — build/produce the fixed ISO carrying Anton's Max-Bet fix — due Aug 14 2026 (out the following two days) — [[raw/Meeting_Notes_Tilt-1_MaxBet_Bug_Fix-August-14-2026.md]]
- [ ] Felipe Miranda — switch the Tilt-1 fix onto the 10 field machines over the weekend once the ISO is ready — due weekend of Aug 15–16 2026 — [[raw/Meeting_Notes_Tilt-1_MaxBet_Bug_Fix-August-14-2026.md]]

## Open questions

- Bugs #2 (out-of-service workaround un-blocks a regulator-blocked machine) and #3 (blocked game returns after a power cycle) from the Aug-13 analysis still need fixing — deferred into the V3 release through Eclipse. [[raw/Meeting_Notes_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026.md]]
- How a blocked/unavailable game should appear on the game-select screen — greyed-out icon, blank card, or placeholder — deferred until after the field-machine investigation. [[raw/Meeting_Notes_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026.md]]
- Will customers permit a software install on a Friday? A full install requires a new co-MID via Intralot. [[raw/Meeting_Notes_Tilt-1_MaxBet_Bug_Fix-August-14-2026.md]]

## History

- **Aug 11 2026 (discharged) — Irina Shishko** was to send the reproduced-crash logs to Anton and Efim to find the root cause; discharged by Aug 14 (Anton fixed the bug; the root cause was the Max-Bet double-bet). [[raw/Meeting_Notes_Tilt-1_Game_Crash_Reproduction-August-11-2026.md]] [[raw/Meeting_Notes_Tilt-1_MaxBet_Bug_Fix-August-14-2026.md]]

## Sources
- [[raw/Meeting_Notes_Tilt-1_Game_Crash_Reproduction-August-11-2026.md]]
- [[raw/Meeting_Transcript_Tilt-1_Game_Crash_Reproduction-August-11-2026.md]]
- [[raw/Meeting_Notes_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026.md]]
- [[raw/Meeting_Transcript_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026.md]]
- [[raw/Meeting_Notes_Tilt-1_MaxBet_Bug_Fix-August-14-2026.md]]
- [[raw/Meeting_Transcript_Tilt-1_MaxBet_Bug_Fix-August-14-2026.md]]
- [[raw/Meeting_Notes_GA_COAM_Pipeline_Trial_Forecast-August-11-2026.md]]
