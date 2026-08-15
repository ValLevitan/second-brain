# Meeting Summary — Bug_Tilt-1 (Tilt-1 Max Bet Bug Fix)
**Date:** August 14, 2026, 11:30 AM ET
**Duration:** ~9 minutes
**Attendees:** Pavel Frolov, Irina Shishko, Juan Martinez, Val Levitan
**Raw transcript:** [[Meeting_Transcript_Tilt-1_MaxBet_Bug_Fix-August-14-2026]]

## Summary

The team confirmed the root cause of the Tilt-1 bug and agreed how to ship the fix.

**Root cause.** Dumps and reports showed a bet value that did not match what the player set. A player tried to play at 50 cents, but the transaction history recorded a $3 bet. Irina reproduced it: if you press Max Bet immediately after pressing Play, the machine can register two bets in a row — first the small bet, then the large max bet. After a reboot the game math and the submitted bet no longer agree (the game has one math, a different math gets submitted), and that produces the bet/math conflict. Logs from the test machine matched production, and screenshots from the transaction history (pulled yesterday with Elizabeth) confirmed it. The conflict sits between Play and Max Bet.

**Fix status.** Anton has already fixed the bug. Irina is compiling the fixed version.

**How to ship it.** Pavel said the fix can be injected on the current ISO, and this is the one bug worth implementing and delivering urgently. Juan agreed that if it resolves the Tilt-1 software error it is the highest priority. Val said to do it now: get Felipe to switch the fix onto the 10 machines right away — his concern is those 10 machines over the weekend. Everything else should be groomed, tested, grouped with the V3 release, and taken through Eclipse. New sales go into V3; V2 is finished.

**Deployment mechanics.** Juan asked whether customers just re-download a new RIS/installation file, or whether the ISO must be reinstalled. Pavel said the ISO needs to be reinstalled, but the same array assessments can be reused. Pavel will produce the ISO today because he is out tomorrow and the day after. Juan cautioned there is no guarantee customers will allow changes on a Friday — a full software install means a new co-MID, which requires calling Intralot and going through the whole process. Val agreed it probably won't happen Friday, but wants the fix ready in hand regardless.

**Flex Recycler.** At the end Val asked Pavel for a Flex Recycler update. Pavel suggested joining with Andrei, and Val said he would organize a separate team call (the Flex-Recycler alignment meeting that followed).

## Decisions Made

- **Deploy Anton's Tilt-1 fix urgently by injecting it on the current ISO.** It is the only bug worth immediate delivery; the rest are deferred. (Decided by Val, agreed by Pavel and Juan)
- **Felipe to switch the fix onto the 10 machines right away**, given the weekend concern. (Decided by Val)
- **Bundle the remaining bug fixes with the V3 release through Eclipse; new sales go to V3 and V2 is retired.** (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Irina | Finish compiling the fixed Tilt-1 version | TBD (today) | High | Anton's fix |
| 2 | Pavel | Build/produce the fixed ISO | Today (Aug 14) | High | Out tomorrow and the day after |
| 3 | Pavel | Message Juan when the ISO is ready | Today | High | Juan will forward to Felipe |
| 4 | Juan | Once ISO is ready, make sure Felipe gets it | TBD | High | For the 10-machine rollout |
| 5 | Felipe | Switch the fix onto the 10 machines | This weekend | High | Val's main concern |
| 6 | Val | Organize a separate team call for the Flex Recycler update (with Andrei) | Today | Normal | Followed immediately after |

## Open Questions

- Will customers permit a software install on a Friday? A full install requires a new co-MID via Intralot and the full process. Raised by Juan; Val said probably not, but keep the fix ready in hand. Unresolved.

## Dispatch Log

---
*Processed from Teams transcript on August 14, 2026, 12:02 PM ET*
*Source meeting: Bug_Tilt-1-August-14-2026*
