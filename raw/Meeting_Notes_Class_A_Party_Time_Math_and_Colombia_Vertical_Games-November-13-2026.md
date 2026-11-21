# Meeting Summary — Game_Development
**Date:** November 13, 2026, 12:10 PM – 1:41 PM Eastern
**Duration:** ~91 minutes
**Attendees:** Val Levitan (organizer), Michael Gottlieb, Efim Podvoiski, Lena Zhukova
**Language:** English
**Raw transcript:** [[Meeting_Transcript_Class_A_Party_Time_Math_and_Colombia_Vertical_Games-November-13-2026]]

## Summary

**Class A math: predetermined, not random.** Val asked if Georgia COAM math is predetermined or random. Efim and Michael said predetermined. It lets the team force specific outcomes (for example, a minimum win in free spins). Michael gave the example of Liberty Spins in South Dakota: South Dakota allows only random math, the predetermined model was converted to random, and the game ended last in the rankings. Rodeo Spins for South Dakota has big changes. Val summed up: JVL prefers predetermined math where the law permits. Michael said Class A uses a dual box instead of Nudge, so 5-reel games will look and play like Class 3 games. Fiery Ice and Jackpot Rush are not in Class A yet, because there are no progressives.

**Class A party time testing (Jira IP 1190 / IP 1193 / IP 1197).** Concept work is done for South Dakota D27 / NOVA and for Georgia Class A V43. Michael and Efim use Efim's simulator to test party time in each game. They check three parts: base game, free spins and party time, so no part kills the others. Lions Riches is done: party time about 1 in 240 spins, 10x to 60x the bet (at the $3 max bet, about $30 to $180). Free spins are about 1 in 120. Rodeo Spins is next; it is harder (single line, 5x multiplier on reel 4, re-spin feature), so party time will be added after the re-spin feature, like after free spins. Efim said the first 3 or 4 games need close work; the rest can follow the pattern. Efim showed a win distribution chart, compared with a well-accepted game. Val asked for JVL house rules for hit frequency. Michael said it varies by game, but about 1 in 120 for free spins and 1 in 240 for party time. Base game uses a win distribution curve, not one number.

**Jira schedule did not show the math work.** Val read the schedule and thought Class A design was done or ahead of schedule. The math tasks sit as a capability under IP 1197, and Lena and Michael cannot see capabilities in their Jira view. Efim moved IP 1197 to In Progress during the meeting. Efim said he did not add all the next tasks; he now expects about four. Val asked the group to make sure the schedule is correct before the meeting, not found at the meeting.

**Class A timing.** Production for Class A is not scheduled. Lena said it starts after Nebraska, in January 2027, on NOVA. She is talking with Igor and Anton Leshkevich about the new AI-assisted flow; she expects a clear picture in December and will schedule then. Efim hopes to finish Class A production math by New Year; not less than four weeks.

**Market view (Val).** The Class A market is not growing. Primero is failing. Operators hesitate because Class A is not regulated and they do not want legislators to think operators use a loophole. Val has operators willing to try it, and believes JVL should take the shot because it needs another product. Three new players are coming into Class B, including AGS.

**Georgia COAM V4 (Class B).** Michael has a game list and early designs. He will schedule it next week. He is focused on Nebraska and Class A math now.

**Nebraska (IP 1143).** Only the production stage is open. The game count is 11, not 15 (Val counted 15 items in Jira, but some are not games, like the liquid glass home screen). It runs on Rage Studio, liquid glass style. Changes: graphic updates, bonus moves from the golden husk to Match 3, Jackpot Rush and Fiery Ice are added, Wildfire Ranch is new. Version 2 is dual screen with 5 new games. Lena said all games will be integrated in the build by end of December, but not all tested; some games are done already and can be tested now. Moving the diamond bonus to dual screen is hard; first insertion maybe next week.

**Players press category labels.** Val saw players press the large category labels (for example the Fiery Ice Link bar) as if they were buttons, and get frustrated. Ideas: extend the touch area of nearby game icons (Michael), flat text with no border (Efim), more transparent labels (Lena). Val does not know how big the issue is; he parked it with Michael.

**Colombia Class 3 games.** Michael still waits for some feedback from Martha but has a preliminary list. The popular games now are "perceived persistence" games: objects above the reels (firecrackers, pots, chests) and a simple cartoon art style, not photorealistic. One such game is like 6 to 8 regular games in work (many animations, false hits, about 30 help pages). Three planned games: Fly Me to the Moon (based on Aristocrat's Midnight Train, for Georgia), a Colombian carnival game for Barranquilla (three firecracker strands, based on Aristocrat's Baozu Festival, for Colombia), and Treasure Island (gems, universal). Val said he does not care about dual screen. The games will be vertical; Val said converting the hardware (D27) is easy. Lena said vertical assets can also be used for Georgia. Lena will start design images after Michael finishes the concept and she finishes the South Dakota designs.

**Other.** Before Val joined, Lena said a fresh build with an adjusted pay table is coming; if good, Vitaliy records a demo video. Michael will be in Chicago Nov 30 to Dec 4, available with his computer.

## Decisions Made

- **Predetermined math is JVL's preference wherever the law permits; Class A uses predetermined math.** — It allows forced outcomes; the random conversion of Liberty Spins for South Dakota failed. (Val, agreed by Efim and Michael)
- **The Colombia perceived-persistence games will be vertical, not dual screen.** — Vertical suits these games; hardware is easy to convert. (Val; confirmed by Michael)
- **Class A production is scheduled later, not now.** — It starts after Nebraska, in January 2027 on NOVA, once the new flow is clear. (Lena; accepted by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | All (Efim for the math tasks) | Put all Class A math tasks in the Jira schedule and check the schedule before each meeting | Before next meeting | High | Val's group undertaking; math sat under capability IP 1197 |
| 2 | Lena Zhukova | Ask IT why she and Michael cannot see capabilities in Jira | TBD | Normal | Val thinks it is a view setting, not access |
| 3 | Michael Gottlieb, Efim Podvoiski | Continue party time tests with Rodeo Spins, then the next games | TBD | Normal | Lions Riches done |
| 4 | Efim Podvoiski | Finish Class A production math | Dec 31, 2026 (hope) | Normal | Not less than four weeks |
| 5 | Lena Zhukova | Schedule Class A production once the NOVA flow is clear | December 2026 | Normal | Talking with Igor and Anton Leshkevich |
| 6 | Michael Gottlieb | Schedule Georgia COAM V4 (Class B) | Week of Nov 16, 2026 | Normal | |
| 7 | Michael Gottlieb | Schedule the Colombia perceived-persistence games in game concept | Week of Nov 16, 2026 | Normal | After Nebraska and Class A math |
| 8 | Lena Zhukova | Nebraska version 2: all games integrated in the build | Dec 31, 2026 | Normal | Not all tested by then |
| 9 | Lena Zhukova | First insertion of the diamond bonus on dual screen | Week of Nov 16, 2026 (maybe) | Low | |
| 10 | Lena Zhukova | Send fresh build with adjusted pay table; if good, Vitaliy records demo video | TBD | Normal | Said before Val joined |
| 11 | Michael Gottlieb | Think about a fix for players pressing category labels | TBD | Low | Parked with Michael by Val |
| 12 | Michael Gottlieb | Send Val the Baozu Festival name in chat and share the competitor game zip files | TBD | Normal | Val asked for everything in the chat |
| 13 | Lena Zhukova | Start design images for the new Colombia games | After concept stage | Normal | After South Dakota designs |

## Open Questions

- How big is the category-label pressing problem? (Val; not measured)
- Should all Class A games share one party time hit frequency? (Val; Michael: no, varies by game, roughly 1 in 200 to 300)
- New AI game-assembly flow on NOVA is not yet clear. (Lena)
- Remaining feedback from Martha on Colombia. (Michael)

## Dispatch Log

---
*Processed from Teams transcript on November 18, 2026 (scheduled meeting-watcher)*
*Source meeting: Game_Development*
