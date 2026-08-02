# Meeting Summary — Game_Development
**Date:** Friday, July 24, 2026, 2:00–2:57 PM (Eastern)
**Duration:** ~57 minutes
**Attendees:** Val Levitan, Michael Gottlieb, Lena Zhukova, Efim Podvoiski, Juan Martinez
**Raw transcript:** [[Meeting_Transcript_Game_Production_Schedule_Georgia_V3-July-24-2026]]

## Summary

**Georgia V3 release.** The main topic was when to submit Georgia V3 to Eclipse. Juan's ideal date is Monday, August 17 — the Georgia show runs Tuesday August 18 to Friday August 21, and Eclipse approvals have been averaging five business days or less, so an August 17 submission could be approved by the end of the show. Michael wants more time than that if needed: V2 was submitted aggressively, shipped with bugs, and field deployment had to be stopped several times. He wants Ivan to QA V3 thoroughly before submission. Juan agreed. Michael expects Twin Bison and Lions Riches to be ready to show at the Georgia show in a couple of weeks either way.

**V3 contents.** V3 adds 7 new games to the 8 already released in V2, for a package of 15 total — the largest release the team has ever done (more than double the usual). The 7 new games: Twin Bison, Lions Riches, Ruby Power, Tropical Paradise, Crescent City Carnival, Ollero, and Fire Jewels. Golden Rose is not part of the release (it was a stale entry on Val's Jira view). Operators will enable roughly 6–8 games at a time from the package.

**Twin Bison status.** The game just got up and running with real spinning a few days ago. Assets are on track for August 11; QA and engineering dates are open. Michael is play-testing the math now and wants to drop the 10 symbol and shift the pays so animal symbols hit more often than royals — Efim agreed the change is straightforward. Michael and Efim still need to review the statistics on locked-bison frequency. The big-symbol block (full-screen square) is the wrong size in Lions Riches; the team is fixing it next week. The reel-bundle pointer arrows fade into the background — the team will try golden arrows with a sparkle idle animation first, and add pay-line numbers only if that isn't enough. Visual cues matter most because Georgia, South Dakota, and Nebraska venues run with sound nearly off.

**Liquid glass.** Val questioned why liquid glass took ~45 days when it was "done" in V2. Lena explained: the V3 vertical home screen is a new two-row layout (up to 6 games showing), which required a full template redo plus per-game work (fake liquid glass uses pre-rendered effects that depend on what is behind each element, plus attraction videos per game). The new vertical template now covers all layout combinations, so future games need only ~1–3 days each, and most of that is render time, not people time.

**Mega Hit Blaze.** Felipe requested a family name for the games for his brochures. The team chose "Mega Hit Blaze" as the evolution of the old Mega Hits brand, with a liquid-glass logo. Michael, Juan, and Lena had already aligned; Val loves it; Michael declared it approved. Dima starts on the graphics next week; the logo was due to be finished the day of the meeting.

**South Dakota (D27 VLT2).** Development is done and the release is in QA. It includes two kenos (Black Hills Keno and Cool Cat Keno) plus liquid glass. One open issue: handling the case where free spins must stop because a progressive was won and the $1,000 win cap was reached — Julia replied yesterday; Efim and Juan will write a proper requirement Monday and brief Igor (a few days of work if he hasn't started). Lonnie is allowing pre-testing now that the Scientific Games system is in hand: hardware returns from South Dakota to the Georgia office, Minsk validates, then Lonnie is notified and the release goes to GLI — all within the next few weeks. The customer already saw a keno demo (Denis brought in MG Oil) and raved about it. Juan renamed the Jira release to D27 VLT2 during the meeting.

**Other pipeline.** South Dakota vertical (6 games) leaves the concept stage Monday/Tuesday; Georgia vertical concepts are on hold for now, after which Michael and Juan focus on Mega Hits D27 Blaze 01. Nebraska (10 games with liquid glass) finishes game design next week; production would take about 1.5–2 months with Julia, but Julia is leaving and Natalia takes over templates, so timing needs replanning.

**Build tool technical debt.** Michael raised that the build tool has degraded: it now requires a Docker step for multiple progressives, load times are much longer, game select/deselect no longer works (all games load every time), and a progressive hit triggers a "see attendant" error. Lena confirmed she builds 3–4 times a day and a failed build costs ~15 minutes of Docker teardown and setup. Val said the problem is well known and discussed weekly, but there is no quick or elegant fix, and vacations are compounding it. He asked Michael not to route this through Efim; instead, Michael should record 3–7 short videos of his prioritized asks and send them to Val, who will take it from there. Michael's top ask: restore the ability to deselect games and run a single game.

**Release roadmap and breather.** Working assumption: Georgia V3 mid-August, South Dakota to market ~September 1, Nebraska mid-October. After those, nothing is pressing — the remaining verticals (South Dakota, Nebraska, Texas) are not customer-driven — so the team can slow down and put more time into technical debt. The transactional product should also be released by then.

## Decisions Made

- **Aim to submit Georgia V3 around Monday, August 17, but only after thorough QA** — V2 shipped with bugs and had field deployments stopped; approval by the show's end (Aug 21) is the goal, not a hard deadline. (Decided by Juan and Michael, with Val present)
- **Mega Hit Blaze name and logo approved** — evolves the old Mega Hits branding for Felipe's brochures. (Decided by Michael, Juan, and Lena; Val endorsed)
- **Twin Bison math: drop the 10 symbol and shift the pays over** so animal symbols hit more often than royals. (Michael proposed, Efim agreed; details to be worked out between them)
- **Reel-bundle pointers: try golden arrows with sparkle first; add pay-line numbers only if needed.** (Lena and Michael)
- **South Dakota release renamed to "D27 VLT2" in Jira.** (Val requested; Juan made the change in the meeting)
- **Build-tool feedback goes to Val via recorded videos, not through Efim.** (Decided by Val)
- **After Nebraska (~mid-October), the team slows down and allocates time to technical debt** — remaining verticals are not customer-driven. (Val, with Michael and Juan agreeing)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Efim, Juan | Write the proper requirement for stopping free spins when a progressive is won and the $1,000 win cap is reached (South Dakota), and make sure Igor understands what's expected | Mon, Jul 27, 2026 | High | Blocks South Dakota QA completion; a few days of dev work if Igor hasn't started |
| 2 | Michael | Record 3–7 short videos of his most important build-tool asks, in priority order, and send them to Val | TBD | Normal | Val will take it from there; top ask is single-game loading |
| 3 | Michael | Finish South Dakota vertical game concepts (6 games) | Tue, Jul 28, 2026 | Normal | "Monday, Tuesday, I should be done" |
| 4 | Lena (team) | Fix the big-symbol block size (full-screen square) in Lions Riches | Fri, Jul 31, 2026 | Normal | "It will be fixed next week" |
| 5 | Lena | Make reel-bundle pointer arrows golden with sparkle idle animation in Twin Bison; evaluate if numbers are needed | TBD | Normal | Visual cue for 5-lines-per-reel-bundle in free spins |
| 6 | Michael, Efim | Review Twin Bison math together: drop the 10, shift pays, and check locked-bison frequency statistics | TBD | Normal | Michael is play-testing now |
| 7 | Juan | Get the Scientific Games hardware back from South Dakota to the Georgia office, run validation with Minsk, notify Lonnie, then submit to GLI | Next few weeks | Normal | Path to South Dakota release (~Sep 1 to market) |
| 8 | Lena | Replan Nebraska production timing with Natalia in charge of templates (Julia leaving) and report a detailed estimate | TBD | Normal | Baseline was 1.5–2 months with Julia |

## Open Questions

- Exact Georgia V3 submission date — August 17 is the ideal, but Michael wants QA to gate it. (Raised by Michael)
- How long Nebraska production will take with Natalia instead of Julia. (Raised by Lena)
- Whether Igor already started the South Dakota win-cap work — Efim was away and doesn't know. (Raised by Efim)

## Dispatch Log

## Sources
- Teams meeting transcript, retrieved via Microsoft Graph on July 24, 2026

---
*Processed from Teams transcript on July 24, 2026, 6:05 PM Eastern (scheduled watcher run)*
*Source meeting: Game_Development (July 24, 2026, 2:00 PM)*
