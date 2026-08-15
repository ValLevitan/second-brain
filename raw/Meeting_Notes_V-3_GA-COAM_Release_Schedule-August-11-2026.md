# Meeting Summary — review_V-3_GA-COAM_schedule
**Date:** August 11, 2026, 5:00–5:21 PM Eastern
**Duration:** ~21 minutes
**Attendees:** Val Levitan, Juan Martinez, Michael Gottlieb, Lena Zhukova
**Raw transcript:** [[Meeting_Transcript_V-3_GA-COAM_Release_Schedule-August-11-2026]]

## Summary

Val reviewed the V3 GA-COAM release schedule ahead of the trade show. The release target is Tuesday, August 18. The show setup starts August 18 and the show opens August 19.

V3 will ship with 15 games available, but only 10 shown on screen at once, running on an LTE modem. The main open work is the attraction (idle) mode: a full-screen demo that plays a short recorded clip of each game. The team is recording an advertising/gameplay video for all 15 games — Felipe's request. In the attraction loop, MegaHit plays first, then each game's logo followed by a full-screen gameplay clip. Val had asked for the order to be reversed, so it now starts with Safari Iceland and Jackpot.

Lena expects all videos recorded by Friday (Aug 14). Vitaliy and Natalia are doing the recording (about 7 each, ~2 days). Igor will insert the videos — roughly one day of work, because the template is built and the build currently uses placeholder dummy video, so it is mostly a file swap rather than new code. Lena stretched the integration to Monday as a buffer. Val insisted the team work the weekend to make sure it is ready.

On Queen of Luxor: the game has an old look and a new graphical refresh was prepared, but it is not ready. Lena had already agreed that morning with Irina and Pavel not to hand the new assets to programmers; they will keep the existing stable Queen of Luxor for the show. Val endorsed this — drop the Queen of Luxor refresh for the show to keep the machines stable. The new assets will be finished and a later decision made on whether they go into V3 or the next release. With Queen of Luxor's update excluded, the August 18 target is realistic.

There was a QA disagreement. Val relayed that the testers told him they cannot start because the art keeps changing. Lena and Michael pushed back firmly: the changes at this stage are minimal, the game logic is done, and QA can test the pays now; art tweaks might introduce a graphical glitch but should not affect the logic. Val acknowledged the testers still burn setup hours each time something new is introduced, but did not want to dwell on it.

A demo build (ISO) for Felipe to show is hoped for Monday. Val questioned handing over an untested ISO; Juan said it is only for demonstration and acknowledged QA may still find errors. The team is still tracking down a crash bug and expects more information in the morning, working on it overnight.

Separately, Juan reported Jackpot Rush is doing well — 10 to 15 progressive hits — and has gone from Felipe not loving it to being one of the top games.

Val's overall direction: do not introduce anything new from here to the show; keep the machines stable.

## Decisions Made

- **Drop the Queen of Luxor graphical refresh for the show; keep the existing stable version.** The new assets are not ready and the priority is stable machines for the show. New assets will be finished, with a later call on V3 vs. next release. (Decided by Val; already aligned by Lena with Irina and Pavel.)
- **V3 release target stays Tuesday, August 18, excluding the Queen of Luxor update.** Judged realistic without that item. (Val, Lena)
- **No new features or art introduced between now and the show.** Keep the machines stable. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lena Zhukova (Vitaliy, Natalia recording) | Record advertising/gameplay videos for all 15 games | Friday, Aug 14 | High | ~7 videos each; needed for attraction mode |
| 2 | Igor | Insert the 15 videos into the build (placeholder swap) | Weekend → Monday, Aug 17 | High | Template built; ~1 day of work once videos are ready |
| 3 | Val | Have the team work the weekend to ensure readiness | Weekend of Aug 15–16 | High | Val committed to making the team work the weekend |
| 4 | Development team | Track down the crash bug; report findings | Morning of Aug 12 | High | Working on it overnight |
| 5 | Team | Deliver the demo build (ISO) for Felipe to show | Monday, Aug 17 (hoped) | High | Demonstration only; may still surface QA errors |
| 6 | Lena Zhukova (art team) | Finish the new Queen of Luxor assets (not for show) | TBD | Normal | Then decide V3 vs. next release |

## Open Questions

- Whether the finished Queen of Luxor refresh assets go into the V3 release or the next release — deferred. (Lena, Val)
- Whether QA will begin testing now: Val relayed testers won't start until the art is "finished," while Lena and Michael maintain the logic is done and testing can proceed. Unresolved.

## Dispatch Log

---
*Processed from Teams transcript on August 11, 2026 (scheduled meeting-watcher sweep)*
*Source meeting: review_V-3_GA-COAM_schedule*