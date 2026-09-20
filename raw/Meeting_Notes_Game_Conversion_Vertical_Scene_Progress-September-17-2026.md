# Meeting Summary — Game_Conversion-September-17-2026

**Date:** September 17, 2026, 10:14 AM - 10:18 AM Eastern
**Duration:** approximately 3 minutes
**Attendees heard:** Igor Metelski, Pavel Frolov, Irina Shishko, Anton Leshkevich
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_Game_Conversion_Vertical_Scene_Progress-September-17-2026]]
**Source meeting:** Game_Conversion-September-17-2026 — Microsoft Teams

## Summary

A short stand-up on converting a game to the vertical screen. Only Igor had something to show.

**Igor's progress.** He fitted the symbols to the cells. The stretch he applied is temporary — the real symbols come from a horizontal layout, so they had to be pulled a little, and this will not be needed once the proper symbols arrive. The game runs in some form and can already be launched. One defect remains: the pay table sits on a separate camera, which squashes the main scene. He is building a scene that puts the pay table on the upper part of the screen; once that is done the distortion goes away and it should look like a real vertical game. He estimated another half hour to an hour to finish that scene.

Launching in vertical mode was not itself a problem. What broke were small things: font names that do not match in some scenes, and elements missing from the dashboard.

**What is left.** Pavel called it almost a full workflow. Igor said he still has to walk through every scene that needs replacing — at minimum the game scene, plus the shared ones, including the steal / nudge scene, which also has to be made vertical. He added that the steal scene may not need rebuilding at all — changing its camera would be enough, because at that scale it covers the lower part correctly.

**Irina's note on the extra games.** She interrupted to say the aim was the opposite of pretty: the additional games in the Texas product were meant to be unattractive on purpose, so players would not want to play them. Igor accepted it.

Pavel closed the call, saying Anton was unlikely to have anything new today.

## Undertakings

| # | Who | What | Due | Priority | Context |
|---|-----|------|-----|----------|---------|
| 1 | Igor Metelski | Finish the scene that puts the pay table on the upper part of the screen, removing the squashed main view | Same day (he said half an hour to an hour) | Normal | Then it should look like a real vertical game |
| 2 | Igor Metelski | Walk through every scene that needs replacing — the game scene at minimum, plus the shared scenes including steal / nudge | Not set | Normal | Steal scene may only need a camera change |
| 3 | Igor Metelski | Fix the mismatched font names in some scenes and the missing dashboard elements | Not set | Low | Small defects found when launching vertical |

## Decisions

- The stretched symbols are a placeholder; no work is spent on them because the real vertical symbols will replace them.
- The pay table moves onto the upper part of the screen in its own scene rather than staying on a separate camera.
- The steal / nudge scene is likely handled by a camera change instead of being rebuilt.
- The additional Texas games stay deliberately unattractive — that was the original intent, not a defect.

## Open Questions

- None raised on this call.
