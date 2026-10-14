# Meeting Summary — Rage to Nova port review - progress since Monday
**Date:** October 8, 2026, 7:04 AM – 7:58 AM Eastern
**Duration:** ~55 minutes
**Attendees:** Val Levitan, Igor Metelski, Pavel Frolov, Irina Shishko, Evgeny Kharetski
**Raw transcript:** [[Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026]]

## Summary

Held in Russian. Follow-up to the October 5 meeting. Topic: a vertical version of the horizontal game Dragon Pays on the Omni engine.

**What Igor built.** He measured the 5x3 game screen, generated a vertical scene with Claude, and plugged it into his horizontal port. Base game, messages, transition to free spins and free spins all work. Problem: horizontal symbols are wider than tall. In the vertical layout they came out slightly taller than wide, so the symbols look stretched. A second option keeps symbols undistorted and fits the reel frame to them, but then the rest of the screen must be filled with something. The reel frame itself stretches easily (Claude did the linear math). To fill empty areas Igor extended the art (sky, tree, lanterns) and generated the strip under the pay table. His view: the result looks like a game, but nobody would sell it. Horizontal art fits direct conversion poorly.

**Proposal for future games — one resource set for both layouts.** Master background video 1920x2160 (two Full HD screens stacked). Horizontal: cut in half for top and bottom screens. Vertical: cut a strip and scale to 1080x1920. Transitions: an accent plus a fading alpha channel; the accent must fit inside the vertical strip. Pay table: one line above the reels if few symbols, else the top screen. Progressive meters: 1–3 levels in a strip; 4 levels as a two-row pyramid; more than 4 as a column on top, with the accent video removed and the logo moved up. Messages, help and win animations cover the reel frame. Igor also proposed that developers (with Claude) assemble scenes from designer resources, following the designer's comp, instead of designers assembling them in 3ds Max. Pavel: cropping video at build time is simple, even with a script.

**Val's position.** He fully agrees and insists on Claude-built scenes. Designers take about 2 weeks to reach a final comp and about 3 months of production; Claude does it in hours. Irina, Evgeny and Pavel agreed. But Val said the team drifted from the task: convert existing horizontal games to vertical. That goal is not reached, because symbols are distorted. He asked if a math fit could avoid this.

**Next try.** Igor: the symbol art has some slack (the round shapes are really flattened ovals). He can ask Claude to fill the most area without significant distortion. About 30 minutes for art only; longer with video. Val: try it. If it works, two comps per game are not needed and conversion can be done on the fly.

**Approval and layout.** Evgeny: the pay table looks wrong to him. Conversion must be predictable and approved by the people who own games (Michael, Lena). For existing games, a designer should draw a vertical comp from the existing horizontal art; for new games, universal resources and two comps. Pavel liked Igor's two-row meter variant. Val: the new vertical style keeps the pay table to thin strips and gives more space to the main character. Igor: every game has a clean topper, a good source for the main character art. Val questioned what is saved if designers still make every resource; Evgeny: the saving is scene assembly; for conversion the saving is obvious.

## Decisions Made

- **Scenes will be assembled by developers with Claude from designer resources, to a spec — not by designers.** Claude is far faster. (Val Levitan insisted; Irina, Evgeny, Pavel agreed)
- **The original task — convert an existing horizontal game to vertical — is not yet achieved; Igor tries a no-distortion fit before the team decides more.** (Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Metelski | Ask Claude to fit Dragon Pays to vertical, filling most area without significant symbol distortion | Oct 8 (~2 h) | High | Art first; video takes longer |
| 2 | Val Levitan | Set a follow-up meeting with Igor in about 2 hours to review the result | Oct 8 | Normal | Calendar shows "Games convert horizontal to vertical", 10:00 AM |
| 3 | Val Levitan | Move the AI-PM meeting 30 minutes | Oct 8 | Low | Agreed with Pavel and Irina |

## Open Questions

- For existing games, who draws and approves the vertical comp from existing horizontal art (Michael, Lena)? (Evgeny Kharetski)
- How should the pay table be laid out in the vertical version? (Evgeny Kharetski, Pavel Frolov)

## Dispatch Log

---
*Processed from Teams transcript on October 8, 2026*
*Source meeting: Rage to Nova port review - progress since Monday*
