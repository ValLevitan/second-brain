# Meeting Summary — Game_Development

**Date:** September 11, 2026, 1:00 PM - 2:08 PM Eastern
**Duration:** approximately 68 minutes
**Attendees:** Val Levitan, Michael Gottlieb, Lena Zhukova, Efim Podvoiski
**Raw transcript:** [[Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026]]
**Source meeting:** Game_Development — Microsoft Teams

## Summary

The weekly game development call. It opened on build status, spent most of its middle on design arguments Val raised and lost, and ended with the decision that matters: Rage Studio stops after Nebraska, and Georgia Class A moves to Nova.

**Build status.** Michael reported a good week on the Georgia build — one last bug to confirm fixed, and from a game standpoint they are where they need to be. The currency-to-credits switch on the VDEC still has to be implemented. Lena raised two items: she needs the Rodeo demo video to show the final version rather than the attraction video with the logo, since Vitaliy re-recorded it; and Ivan found a new bug where winning a progressive in Jackpot Rush or Fiery Ice Link does not show the progressive win on the topper. That bug had been invisible because progressives cannot be won in the Windows build and show mode has no setting to force one. Natalia and Igor work it Monday; it may need progressive-sign assets reworked.

**Nebraska.** Michael described it as the vertical Georgia work reimagined in D27 format — a similar game selection screen to Georgia V3, seven lines-and-ways games, two Jackpot Rush, two Fiery Ice, eleven in total, with Wildfire Ranch added and the golden husk progressive replaced by the match 3 progressive. Each category shows its own progressive during attraction mode. Nebraska stays on Rage. Lena confirmed everyone except Natalia switches to Nebraska production from Monday.

**The progressive placement argument.** Val asked why the progressive meters stay on the second screen when a topper is fitted, given the two sit so close together physically. Michael called that an extremely bad idea and held the line: the second-screen meters are for the player sitting at the machine, the topper is for the person walking past ten or twenty feet away, and the placement trains the player that JVL progressives always sit at the top of the screen — the same position they occupy inside the game. He added that JVL has always done this, but the old cluttered pay table made it less noticeable; the simplified pay table now puts the focus on progressives because they are being sold aggressively. Val said he understood being covered when there is no topper but not the duplication when there is, then accepted the disconnect was his and moved on. No change was directed.

**How many games on the home screen.** Val probed whether V3 could show all fifteen games, saying Pavel and Irina see no memory issue, against Efim's view that it should be tested but most likely cannot. Michael rejected the idea outright: Juan has said repeatedly he needs unenabled games held back for flexibility, because locations react differently and a game can be swapped out for a refresh — plus the paradox of choice. Val pushed back on how categorical that was, offering six to twelve as a tested range and questioning whether two games per category is enough, suggesting four. Michael argued that would burn titles for no reason, since the Jackpot Rush titles are too similar to differentiate and the same is true of Fiery Ice; better to ship two, watch earnings, and rotate a weak title out. He cited seeing the same game in a different colour earn three times as much at Bally. Val closed it with "let's go with that — I don't know whether it's right or wrong."

**The new-game badge.** Val asked whether a swapped-in game should be flagged to the player, at least for the first three days. Michael said no as a matter of opinion, not oversight: players do not care whether a game is new, they care whether it has progressives and whether it pays. He put it in terms of marketing simplification and limited screen real estate. Efim agreed the timing does not matter much. Val said plainly that he disagrees, and equally plainly that he does not direct the design, so it stands as it is.

**Jira housekeeping.** Val asked Lena to mark IP-1061 done when it is done, saying he lives and dies by Jira. He raised IP-887 and IP-1180 as apparent duplicates and proposed fully retiring 887, plus opening a new IP for vertical Nova design. Michael and Lena pushed back — there is real design work buried under those items, including Dakota Bison (IP-1131), a Keno game, and Cool Cats material under GD-918 that Val could not see because he had not opened the subcategories. The group settled instead on renaming IP-887 to V43 so the two South Dakotas are not confused, keeping it in backlog, and archiving only once the work has migrated. Val asked Lena to use the current light workload to clean out the loose items, preserving what has value, noting the team is moving away from IP-type items toward capabilities and more work into GitHub.

**The platform decision.** Lena said Georgia COAM Class A would be built on the current Georgia V3 release, adapting the existing six slot games, and that she had already started on dashboard changes and extra dialogues. Val stopped it: he does not want it done on Rage. Rage development has to end, supporting two platforms is not possible, and some hardware-related issues are very hard to fix there. Michael objected — his understanding was to get a Class A version of Georgia V43 out as fast as possible, and migrating a single derivative of finished work to Nova looked like wasted effort. Efim sided with Val: the framework changes needed are unknown and possibly substantial, anything new built in Rage is work that will be thrown away, and asset conversion has already been proven to go relatively easily. Val added that the Nova team works at a speed he could never have visualised — hours, not weeks. Michael conceded: "No objections, then let's get the first six lines and ways games brought over to Nova." Val asked for the concept and game design descriptions to be updated to say Nova, and Michael confirmed he had already updated the game concepts.

**Sequencing and date.** Val first named January 1st for Class A on Nova. Lena said Nebraska would then not finish by year end, and that she would rather complete Nebraska with the full team before moving everyone to Nova — she needs about 101 days on Nebraska alone, with several people on vacation and a replacement hire let go and yet to be re-interviewed. Val agreed to that sequencing and moved the date to February 1st. Lena accepted it as a goal rather than a commitment, and will give a firmer read once the asset transition is better understood. In parallel with Nebraska, she will start on the new Nova workflow with Alexander Biratko and the developers once Dima is back from vacation, and begin experimenting with asset transition. Michael asked that this not stay theoretical and proposed using Line Switches as the live Class A test bed on Nova; Lena said that is what she intends to do.

**Class A groundwork.** Michael asked Efim to write up Class A behaviour — money in gives credits, wins give awards, and awards cannot be bet — so programmers can start thinking about it even before anyone touches code. Efim agreed but wants to understand the party time feature and how the streak and three spins work first, which he expects to take two or three weeks. What they lack is video of a Class A machine showing free spins and party time. Val's answer was to put Michael in front of a machine in Georgia next week and let him record whatever he needs.

**Logistics.** [Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.] Michael travels to Georgia next week, arriving 6 PM Monday; Val arrives around 10–11 PM Monday, will arrange a Tesla 3 at the arrival level, and has Michael at the same hotel. Dress is slacks and a jacket, nothing formal.

## Decisions Made

- **Georgia COAM Class A V43 will be built on Nova, not Rage.** Rage development has to end, two platforms cannot be supported, and work put into Rage now would be thrown away. (Val Levitan, supported by Efim Podvoiski; Michael Gottlieb objected, then withdrew the objection)
- **Nebraska is the last release on Rage Studio.** (Val Levitan, confirmed by Lena Zhukova, Michael Gottlieb and Efim Podvoiski)
- **Nebraska takes precedence** — the team finishes it with full resources before moving to Nova projects. (Lena Zhukova, accepted by Val Levitan)
- **February 1st is the goal for Class A on Nova**, replacing Val's initial January 1st, and held as a goal rather than a commitment until Lena can evaluate the asset transition. (Val Levitan / Lena Zhukova)
- **Line Switches is the test bed for Class A on Nova** rather than working it out in theory. (Michael Gottlieb, accepted by Lena Zhukova)
- **Two games per category stands** — the remaining titles stay unenabled for location-level rotation, instead of putting all fifteen on the home screen. (Michael Gottlieb, accepted by Val Levitan)
- **No "new game" flag in the menu.** Michael's position that players care about progressives and payouts, not novelty, stands. Val disagreed on the record and declined to overrule the design group. (Michael Gottlieb; Val Levitan dissenting)
- **Progressive meters stay on the second screen even when a topper is fitted** — no change directed. The duplication is deliberate: second screen for the seated player, topper for passers-by, and consistent placement between the selection screen and the game. (Michael Gottlieb; Val Levitan questioned it and did not press)
- **Considered and superseded: fully retiring IP-887.** Val proposed it; the group settled instead on renaming IP-887 to V43, keeping it in backlog, and archiving only after the design work migrates. (Michael Gottlieb / Lena Zhukova)
- **Concept and game design descriptions are updated to name Nova.** (Val Levitan; Michael Gottlieb confirmed game concepts already done)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lena Zhukova | Fix the bug where a progressive win in Jackpot Rush or Fiery Ice Link does not show on the topper | September 14, 2026 | High | Found by Ivan; Natalia and Igor work it Monday, may need progressive-sign assets reworked |
| 2 | Lena Zhukova | Check the final messaging and make sure the Rodeo demo video shows the final version, not the attraction video with the logo | TBD | Normal | Vitaliy re-recorded it |
| 3 | Michael Gottlieb | Confirm the last outstanding Georgia build bug is fixed | TBD | High | The only game-side item left before Georgia is where it needs to be |
| 4 | Michael Gottlieb | Finish the Keno game concepts | September 11, 2026 | Normal | Said he should finish them that day, then works through the rest of the games |
| 5 | Michael Gottlieb | Record video of a Class A machine — free spins and the party time feature — while in Georgia | Week of September 14, 2026 | High | Val is putting him in front of a machine in a location; blocks undertaking 6 |
| 6 | Efim Podvoiski | Write up Class A behaviour — credits in, awards out, awards not usable for betting — so programmers can start thinking about it | After the party time and streak mechanics are understood | Normal | He expects to need two to three weeks for information on how the streak and three spins work |
| 7 | Lena Zhukova | Bring the first six lines-and-ways games from Georgia V3 over to Nova for Class A | Goal February 1, 2027 | High | Starts after Nebraska; date is a goal pending her evaluation |
| 8 | Lena Zhukova | Use Line Switches as the Class A Nova test bed and do the design work on dialogues and dashboard | Not stated | Normal | Design is the same for Nova and Rage Studio, so it is not wasted |
| 9 | Lena Zhukova | Start on the new Nova workflow with Alexander Biratko and the developers, and begin asset transition experiments, in parallel with Nebraska | Once Dima is back from vacation | Normal | Deliberately working ahead of the platform switch |
| 10 | Lena Zhukova | Give a firmer read on whether February 1st is achievable once the asset transition is understood | TBD | Normal | She accepted the date as a goal only |
| 11 | Lena Zhukova | Mark IP-1061 done in Jira when it is actually done | When complete | Normal | Val: "I live and die by Jira" |
| 12 | Lena Zhukova | Rename IP-887 to V43, keep it in backlog, and archive it only once the design work has migrated | TBD | Normal | So the Nova D27 South Dakota and the Rage V43 are not confused |
| 13 | Lena Zhukova | Clean out the loose IP items while the workload is light, preserving anything of value | TBD | Normal | Team is moving from IP items to capabilities and more work into GitHub |
| 14 | Val Levitan | Arrange the car (Tesla 3, arrival level) and hotel for Michael's Georgia trip, and try to move his flight earlier | September 14, 2026 | Normal | Michael lands 6 PM Monday; Val currently arrives 10–11 PM |
| 15 | [Unassigned — needs clarification] | Implement the currency-to-credits switch on the VDEC | TBD | Normal | Raised by Michael as still outstanding; no owner named |

## Open Questions

- **Whether fourteen or fifteen games fit in memory.** Val reported Pavel and Irina see no issue; Efim said it should be tested but most likely cannot. Not resolved, though moot now that the home screen stays as it is.
- **Whether February 1st is achievable for Class A on Nova.** Lena holds it as a goal only until she sees how well assets convert.
- **How the party time feature, the streak and the three spins actually work.** Efim is waiting on this before the Class A write-up; he expects information in two to three weeks.
- **Whether a separate IP is needed for vertical Nova design.** Val raised it when proposing to retire IP-887; the group kept 887 in backlog instead and the question was not returned to.

## Notes on the transcript

The Teams transcription garbles most product and proper nouns. Readings that are near-certain from context but appear distorted in the raw file: "Jetpot Rush" / "jet for trash" / "John Patras" = Jackpot Rush; "Fiery Ice Link" / "Fire AI's link" / "fire wrestling" = Fiery Ice Link; "Wild Power Ranch" / "wildfire ranch" = Wildfire Ranch; "Rodio Spin" = Rodeo; "Giorgi V3" = Georgia V3; "Ridge" / "Rich Studio" / "rage" = Rage Studio; "no" / "NOAA" / "novel" / "lower" / "Inna Nova" = Nova; "Potash" = topper; "Kinos" = Keno; "Lev and Games" = eleven games; "D2702" / "D2703" = D27; "Biratko" = Alexander Biratko; "Jima" = Dima (Dzmitry). Phrases worth confirming with Val before being treated as fact: the failed "Monica 40 game format" he referenced, "Queen of Luxor is on GLP-1", "solar key" as a game name, and "Shkapcova games" as the converted title set. The raw transcript is preserved unchanged.

## Dispatch Log

*(empty — captured by the scheduled meeting-watcher sweep, no dispatch)*

---
*Processed from Teams transcript on September 11, 2026, 2:26 PM Eastern*
*Source meeting: Game_Development*
