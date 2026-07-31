# Meeting Summary — Game Development

**Date:** May 29, 2026, ~2:00 PM Eastern
**Duration:** ~39 minutes
**Attendees:** Val Levitan, Michael Gottlieb, Lena Zhukova, Efim Podvoiski
*(Juan invited but did not attend; Anton referenced but not present.)*

## Summary

The main topic was **Solar Keno**, JVL's first vertical-screen Keno game. Lena redesigned the layout to use the vertical screen aggressively: the Keno board is made as large as possible, and the pay table and information panels — normally placed left and right — were moved above the board into a "tower" that fills with green as the player hits. There is a promotional message and a planet-hit tracking box on the left, plus a large, high-contrast marked-hit win and total multiplier. Val strongly approved the oversized card and the vertical layout.

Efim flagged that cash amounts with decimals (e.g. 1,000.00) could crowd the pay table. Lena will widen that section to fit. Lena will also send Felipe's existing vertical reference image (the Georgia vertical build) to Michael and Juan so Juan can run it on a real machine and judge the ergonomics — arm reach, line of sight, and eye strain on a vertical screen.

The longest discussion was the **planet bonus feature**. Players place planets on the Keno board; drawn numbers that fall inside a planet box count as hits. Three spots on a planet pays 2x, and uncovering all spots triggers free games. The feature was inspired by a popular IGT game. In Lena's design the planets start grayed/covered and get uncovered as they are hit. Val objected strongly to the covering idea — the planets (Saturn, Jupiter, Mars) are beautiful, and covering them hides that beauty. He wants progress shown through motion, size, brightness or glow instead of a cover. Lena and Efim pushed back that they still need a clear way to show how many of the four sections are hit.

The group converged on a solution: don't start dark and dingy — go from a medium state to a bright/hot state instead of dark to medium, and use the **planet's border** as the progress indicator (each border section turns from gray to the planet's color as that section is hit). Val endorsed the border idea. Michael will keep only a light, non-objectionable filter over the planet so the unlit state is still clear.

Val also asked to make the card "lighter": remove the dark charcoal square inlays (they force the digits smaller), make the digits slightly larger, bring the liquid-glass look (already used on the bottom buttons) up into the top info banner, and add subtle motion or sparkle behind it instead of a static banner. He wants the V-deck and the word "Solar" (with a fire/sizzle animation) to stand out.

For **Cool Cat Keno**, Lena will try both a traditional side-panel layout and the repurposed approach, because on a vertical screen putting information on both sides shrinks the Keno card too much (there are also three cats on top, so the composition needs to stay symmetrical). Michael reported he worked with Anton on Cool Cat Keno timings and they are close, having agreed a common per-hit timing approach; he praised Anton. Lena's next focus is Giorgi V2 — she will share the first Windows build for review as soon as it is ready.

Efim gave a short status on the **Rust conversion**: it is not moving faster than planned. Three weeks ago he estimated 10 more weeks, and he still estimates 10 more weeks. He is satisfied but not ahead of schedule.

Val previewed an upcoming decision to put an **event recorder ("black box") with a built-in LTE modem** (and possibly GPS) into every machine. Because it transmits continuously, it can send effectively unlimited data, and the main interest is player-behavior data rather than just technical fault data. Michael suggested capturing which games players choose, bet levels, play-session/bankroll behavior, time on device, and spin timing (especially for Keno, where the chosen speed across three settings would help set the default). Val noted the technical fault data is already planned and known; the open part is the player-behavior wish-list. He asked everyone to write down their data-collection requirements, because there is no definitive list yet.

## Decisions Made

- **Solar Keno will be JVL's first vertical Keno product, using Lena's oversized-board vertical layout.** Val likes the direction; Michael endorsed it. (Val, Michael)
- **Planet progress will be shown via the border (gray → planet color per section) plus a medium-to-bright state change, not by heavily covering the planet.** Reason: covering hides the artwork; the border reads clearly. (Converged: Val, Michael, Lena, Efim)
- **Drop the ticker on Solar Keno** and shift the layout down to free space for animation around the logo. Reason: redundant information adds confusion, not clarity. (Lena, Michael)
- **Widen the pay-table section to fit cash amounts with decimals.** Reason: 1,000.00 would otherwise crowd the table. (Lena, Efim)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lena | Rework the planet feature: start uncovered/light, use the border (gray → color) as the progress indicator, go medium-to-bright, add motion/glow | TBD | High | Main design feedback from Val this meeting |
| 2 | Lena | Lighten the card — remove charcoal inlays, enlarge digits slightly, extend liquid glass into the top info banner, add subtle motion/sparkle behind it | TBD | Normal | Val wants the card less "heavy" |
| 3 | Lena | Send Felipe's vertical reference image (Georgia vertical build) to Michael and Juan so Juan can test ergonomics on a real machine | TBD | Normal | Check reach, line of sight, eye strain on vertical |
| 4 | Lena | Widen the Solar Keno pay-table section to accommodate cash decimals | TBD | Normal | Raised by Efim |
| 5 | Lena | Remove the ticker on Solar Keno and shift layout down for logo animation | TBD | Normal | Frees vertical space |
| 6 | Lena | Try both layouts for Cool Cat Keno (traditional side panels vs. repurposed) | TBD | Normal | Vertical layout shrinks the card too much otherwise |
| 7 | Lena | Produce the first Windows build of Giorgi V2 and share it for review | TBD | Normal | Next focus area |
| 8 | Michael | Continue Cool Cat Keno timing work with Anton (close to done) | TBD | Normal | Common per-hit timing approach agreed |
| 9 | Michael, Efim, Lena (all) | Write down their requirements for what the event recorder should collect (player-behavior data) | TBD | High | No definitive list yet; Val wants it on paper to design better |
| 10 | Efim | Continue the Rust conversion | ~10 weeks | Normal | Not ahead of plan; ~10 weeks remaining |

## Open Questions

- Whether the event recorder will include GPS (Val: "maybe, maybe not — I'll see").
- Final visual treatment of the planet feature — the border approach is agreed, but the exact filter/glow/brightness levels still need tuning.
- For Cool Cat Keno, which layout wins (side panels vs. repurposed) — Lena to prototype both.
- The definitive list of event-recorder data requirements is not yet written; pending input from Michael, Efim, and Lena.

---
*Processed from Teams transcript on May 29, 2026. Filed for historical record only — no follow-up actions dispatched.*
*Source meeting: Game_Development-20260529_140024-Meeting Recording*
