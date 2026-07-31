# Meeting Summary — 3-Progressives GA-COAM Release Schedule Check
**Date:** June 10, 2026, 3:01 PM Eastern
**Duration:** ~16 minutes
**Attendees:** Val Levitan, Pavel Frolov, Igor Metelski, Lena Zhukova, Anton Liashkevich, Irina Shishko, Evgeny Kharetski

## Summary

Wednesday schedule check on the 3-Progressives release for the Georgia COAM market. Pavel walked the Jira board game by game. The release hinges on the Match 3 progressive bonus launching from every game.

**Match 3 bonus (Igor).** Igor finished the bonus restoration and added the bonus to all games, so a fresh build should show it everywhere. Yesterday it only launched from one game (Buy Riches). Igor said today's build should let Match 3 launch from all games. Open item: the bonus coin size. Games have different grids (3x3, 4x3, 5x3, 5x4), so Lena and Michael still need to decide whether the coin is oversized or fits inside the symbol's bounding box — they can't review this until the bonus launches from every game.

**Crash bug (Igor).** On the GA-COAM games, the machine crashes when Match 3 is played on any bet above the minimum. Igor believes it's on his side and is investigating. He is prioritizing this over the LED work because it matters more.

**Rodeo Queen (Anton).** Anton fixed most of the bonus and transition bugs. One problem remains — the transition where the girl throws the flag. Anton is on it and planned to finish today. Irina also flagged a crash on the game-select screen that Anton will look at.

**LED bet animations.** The Match 3 bonus needs LED light-strip animations like the other bonuses. Three colors are in play — red, blue, green — tied to the win levels, with soft transitions between them. Lena and Michael will choose the colors and send them (today or tomorrow). Igor then wires the events through the LED manager (about an hour to ninety minutes) and records a video with Michael for review. Context: David used to handle LED work on the machine; Michael reviews off-machine and doesn't see animations. Lena suggested an artist (Natasha or Artur) sit with Igor in the office to check how it looks on the real machine. Pavel will open a Jira feature for this; Igor said he needs a ticket to track it.

**Peach bonus.** Igor added the bonus to all games but not the special show entries yet. Selecting the peach bonus in any game should trigger Match 3. For now the win is set to random so the coin-size question can be closed; later the team needs to verify all three win levels (yesterday only the blue level kept winning).

**Backlog cleanup.** Lena confirmed the GA-COAM v2 features (e.g., Gypsy Spirit, Andrei's game) are archived and out of scope for this release. Pavel can delete them and their sub-tasks. No decision yet on whether they'll be built in a later version.

**Test plan / board hygiene.** Pavel and Irina reconciled the status of the "Fran 12:00" test plan — the tester only confirmed it works and takes it into full work tomorrow, so its current status was wrong. Val pushed for a clear status rather than vague "we can move it" wording. Set to 2 days.

**Schedule.** Lena said there are no big schedule problems. Next check stays Friday at the same time; Lena is off Friday but the team agreed to proceed without her.

## Decisions Made

- **Match 3 must launch from all games in today's build** — yesterday it only ran from Buy Riches; needed to unblock the coin-size review. (Igor)
- **Fix the crash bug before doing the LED animations** — the crash matters more; LED can be set at the last moment. (Igor, Lena)
- **Delete the archived GA-COAM v2 features and their sub-tasks** — out of scope for the nearest Georgia release. (Lena, Pavel)
- **Next schedule check stays Friday, same time** — proceed even though Lena is off. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Metelski | Fix the crash on the GA-COAM games when Match 3 is played above the minimum bet | ASAP (before LED work) | High | Blocks bonus testing across bet levels |
| 2 | Igor Metelski | Produce a build where Match 3 launches from every game | June 10 (same day) | High | Unblocks the coin-size review |
| 3 | Anton Liashkevich | Finish the Rodeo Queen transition (flag throw) and check the game-select-screen crash Irina flagged | June 10 (planned) | High | Last open Rodeo Queen items |
| 4 | Lena Zhukova / Michael | Send the LED colors (red/blue/green) and transition timing for the Match 3 bonus | June 10–11 | Normal | Feeds Igor's LED work |
| 5 | Igor Metelski | Wire LED bet animations through the LED manager and record a review video with Michael | After the crash fix | Normal | ~1–1.5 hrs; needs the Jira ticket from Pavel |
| 6 | Pavel Frolov | Open the Jira feature for the Match 3 LED animation; delete the archived GA-COAM v2 features and sub-tasks; set the "Fran 12:00" test plan to 2 days | June 10 | Normal | Board cleanup and tracking |
| 7 | Lena Zhukova | Arrange an artist (Natasha or Artur) to sit with Igor and review the LED look on the machine | Around the build | Low | Quality check on the animations |

## Open Questions

- Coin size for the Match 3 bonus — oversized or fit within the symbol bounding box? Pending Lena + Michael; can't be reviewed until the bonus launches from all games.
- All three win levels (blue/green/red) still need verification once the build is ready — yesterday only the blue level kept winning.
- Risk feature — not touched yet; Lena was told to leave it for now, possibly revisited around the 23rd.
- Whether the archived GA-COAM v2/v3 games (Gypsy Spirit, Andrei's game) will ever be built — deferred.

---
*Processed from Teams transcript on June 11, 2026*
*Source meeting: 3-Progressives release GA-COAM schedule check (June 10, 2026)*
