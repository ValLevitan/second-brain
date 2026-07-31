# Meeting Summary — Game Development (Inna Progressive Bonus Review)
**Date:** May 22, 2026, 2:30 PM Eastern
**Duration:** 18 min
**Attendees:** Val Levitan, Juan Martinez, Michael Gottlieb, Lena Zhukova, Efim Podvoiski

## Summary

Val opened by confirming he'd already reviewed the schedule that morning and had no questions on it. Michael asked Lena to walk through the Match-3 progressive bonus celebration art for Inna, showing where the team currently stands on screens and choreography.

**Inna Match-3 progressive bonus art.** Lena demoed the basic bonus screens, which are already in development — table, meters, and report title are done, and the resources are ready to hand to programmers. The win choreography: after the player hits the third coin of a level, an effect shoots up from the third coin, the three coins highlight for a beat, then the screen transitions to a "Winner" message with a color-coded particle effect (red for Grand, blue for Minor) before transitioning back to the game. Michael explained that they chose the word "Winner" rather than naming the progressive level (Grand/Major/Minor) because he felt repeating the level name on the win screen was redundant — the level was already visible from the highlighted row.

**Digit alignment debate.** Val pushed back on the right-justified alignment of the progressive digits within their frames, saying it looked off — his preference was left-justified so the dollar signs would line up. Lena explained that right-justification is the industry-standard way to compare digit magnitudes across progressive levels (so a Grand visually reads bigger than a Minor). Juan confirmed that historically JVL's jackpot rush displays were also right-justified, not left-justified. Val accepted the team's position ("OK, I don't know") and moved on.

**Digit-growth handling.** Efim asked what happens when a Minor grows past 100 and acquires an additional digit — would the frames remain aligned? Lena confirmed each progressive level (Grand, Major, Minor) has reserved space for one extra digit horizontally; frames will not expand, and digits are centered within their boxes. She noted it's not aligned pixel-to-pixel today either because digit sizes differ across levels, but it remains visually aligned within the reserved space. A Minor reaching multi-thousands was deemed not a realistic scenario.

**Cool Cat Keno + Black Hills.** Michael has been working with theme on the bonus description and help text verbiage for the Inna bonus, and with Anton on Cool Cat Keno draw-speed timings. Timings are getting closer to where they should be, but Michael emphasized the need to get Black Hills and Cool Cat Keno in front of a player sooner rather than later. Juan referenced an earlier message about issues with the sample build — the dev team is working on it. Juan said he'll get back to the group on Keno shortly.

**South Dakota demo mode.** Lena finished the demo mode for South Dakota — attraction sequence with game logos and full-screen demo videos per game. She asked Ivan to produce a review image with all games (not just Inna), so Michael and the team can review the full attraction flow. Efim flagged a bug in the demo: the Keno attract video shows a paytable win greater than 1000, which is not achievable — Michael acknowledged this was the bug he'd called out the day before (it's a Max-bet × multiplier display issue showing a win amount that exceeds the actual maximum win). Lena will re-record the demo video once the Kino bug is fixed; she asked the team to ignore the digit values in the current preview and focus on flow timing. Juan noted the team won't be able to demo this to the customer this coming week — they have one week to fix it, with a target of being ready the following week.

**Attraction-mode trigger logic.** Lena raised a separate concern: the demo/attract loop currently only triggers when a player inserts money or when the machine has zero credits. In the real world, players routinely leave a few cents on the machine and walk away rather than cash out — so the machine stays on the last game played and never enters the multi-game attract loop. Juan agreed this is a common operator pain point and a missed sales opportunity (operators want the attract to play to draw in the next player). Michael suggested a threshold approach: enter attract if credit balance is below one minimum-bet credit. Efim recalled the legacy system used time-delay logic — longer delay when credits remained, shorter delay at zero credits. Juan said he doesn't remember that setting in RIS and will check; Efim will also verify.

The meeting closed with a Memorial Day weekend social exchange (Michael's mouse-in-the-BBQ story).

## Decisions Made

- **Winner-screen text reads "Winner" rather than the progressive-level name** — to avoid redundancy with the highlighted row. (Michael)
- **Inna progressive frames reserve space for +1 digit per level, no frame expansion** — Minor unlikely to exceed multi-digit range realistically. (Lena, accepted by team)
- **Right-justified digit alignment stays** — industry-standard for cross-level magnitude comparison. (Val raised concern, team disagreed, Val accepted)
- **South Dakota attract demo video will be re-recorded** — after the Keno max-win paytable bug is fixed.
- **Cool Cat Keno + Black Hills demo will not go to customer this coming week** — one-week fix window, target the following week.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Michael | Fix Keno max-win paytable display bug in attract video (Max bet × multiplier shows win > actual max) | TBD (within ~1 week) | High | Blocks SD demo to customer |
| 2 | Lena | Re-record South Dakota attract mode demo video once Keno bug fixed | After bug fix | Normal | For customer demo following week |
| 3 | Michael | Continue working with Anton on Cool Cat Keno draw-speed timings | Ongoing | Normal | Needed to get Black Hills + Cool Cat Keno in front of player |
| 4 | Juan | Get back to team on Keno status | Shortly after meeting | Normal | — |
| 5 | Juan + Efim | Verify RIS settings for attract-loop trigger logic (time delay + credit threshold below min bet) | TBD | Normal | Attract rarely fires today because players leave change on machine |
| 6 | Ivan | Produce review image with all games (not just Inna) for SD attract flow review | Done (per Lena) | — | Completed |
| 7 | Michael | Continue with theme on Inna bonus description + help text verbiage | Ongoing | Normal | — |

---
*Processed from Teams transcript on 2026-05-25*
*Source meeting: Game_Development (May 22, 2026, 2:30 PM Eastern)*
