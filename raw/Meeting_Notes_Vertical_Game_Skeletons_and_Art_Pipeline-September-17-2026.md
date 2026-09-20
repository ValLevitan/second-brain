# Meeting Summary — Game_Conversion_progress

**Date:** September 17, 2026, 12:19 PM - 12:43 PM Eastern
**Duration:** approximately 23 minutes
**Attendees heard:** Val Levitan, Igor Metelski, Pavel Frolov, Irina Shishko, Anton Leshkevich
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026]]
**Source meeting:** Game_Conversion_progress — Microsoft Teams

## Summary

Igor showed the vertical game he built from Anton's video, and the call then turned into Val setting the direction for the whole conversion pipeline.

**What Igor showed.** He took an existing game and put Anton's video (made yesterday) into it as the scene. Symbol positions are calculated from the video's proportions, so each symbol lands in its own cell. The game plays. He worked inside the existing branch instead of cutting a separate one; if the product goes ahead the changes can be moved to a fresh branch later.

Val asked why the picture looked squashed. Igor said it is his own monitor layout or the screen share, not the scene. Pavel asked him to squeeze the shared window to roughly 9:16 and the proportions then looked right. Val confirmed it is a debugging matter and not something to worry about.

The pay table part was cut out of the horizontal pay table by hand, going around the mechanism they built earlier, because the horizontal scene came with its own background and did not fit. It shows in the correct position. The old horizontal scene was not touched and still breaks — picking something there drops into the steal scene — but Igor has not worked on it yet.

**Val's main point: get rid of the guesswork.** Val said the artists' hand-waving is of no use to him. He wants to know exactly how their intent turns into hard mathematics — geometry and motion physics. Once he has that, he can build a template from the numbers and ask AI to give the game different tones. He asked what milestone gets them there, so the rest becomes routine work that one competent universal graphic designer can do with AI help.

Igor said this is technically no problem. The hard geometry is written in a file inside each scene, and they already have parsers in their tools that read existing geometry — Anton's video was itself generated partly by parsing an existing vertical 3x3 game. He can also point AI at the game directories and get back the list of scenes and what each needs, and can generate prose and build the list from that.

**How the code is organised.** A scene is a folder in the game directory. Each folder holds one scene, the game decides which scene is shown, and this exists for every game they have ever made. Scenes that need vertical versions: the main game scene, free spin, transitions, messages, and any separate bonus (the touch-wheel plate was the example).

**The skeleton.** Val's picture: a fixed vertical skeleton per game format, a set of artifacts, geometry known, motion physics known from other games, with only screen-size parameters recomputed. Pavel and Irina pushed back that the pay table is laid out differently in every game and cannot sit in a fixed skeleton. Anton suggested a game template with plain grey squares plus tools that generate on the fly; Pavel said that is essentially the same skeleton, and that if pay table frames existed in advance they could generate the video and then ask Claude to lay those frames over each frame and regenerate it. Igor confirmed they can build a skeleton that tells any designer where to place what.

His open question was what to use as the reference, since this game has no vertical layout folder. Val answered: take the layout of another vertical game they already have.

**What Igor committed to.** He will take about six horizontal game formats — 3x3, 3x5, 4x5 — and build the vertical skeletons for them: reels here, pay table elements here, and so on. Asked how long, he said a couple of days, so tomorrow or Monday.

**Meeting time.** Val flies tomorrow and offered Saturday. Igor would rather not work Saturday and offered Sunday or Monday, while agreeing to Saturday if Val wants it. Val left it to Igor to pick and write to him tomorrow. Val may also be free from the airport tomorrow if he gets there early.

Val closed by praising the result. Irina and Pavel pointed out the video was Anton's work. Val then asked Pavel and Irina to stay on for a separate call.

## Undertakings

| # | Who | What | Due | Priority | Context |
|---|-----|------|-----|----------|---------|
| 1 | Igor Metelski | Build vertical skeletons for about six horizontal game formats (3x3, 3x5, 4x5), using an existing vertical game's layout as the reference | Monday, September 21 (he said "a couple of days, tomorrow, Monday") | High | Reels, pay table elements and the rest placed in the skeleton |
| 2 | Igor Metelski | Pull the hard geometry and motion physics out of the existing scene files with the parsers they already have, so every artifact is described in numbers | Not set | High | Val's central request on this call |
| 3 | Igor Metelski | Point AI at the game directories and produce the list of all scenes across all games, with the artifacts each scene needs | Not set | Normal | He said this will not take long |
| 4 | Igor Metelski | Write the technical requirements for an outside graphic designer — video format, aspect ratio, which resources are needed | Not set | Normal | So the art work can be handed out |
| 5 | Igor Metelski | Write to Val tomorrow with the day he prefers to meet — Saturday, Sunday or Monday | Friday, September 18 | Normal | Val flies tomorrow; may be free from the airport |

## Decisions

- **The reference layout for a vertical conversion is another vertical game JVL already has** — not the game's own horizontal layout. This answered Igor's open question.
- **Igor builds vertical skeletons for the roughly six horizontal game formats** (3x3, 3x5, 4x5), targeted for Monday.
- **Hard geometry and physics come from the existing scene files**, read with the parsers already written, rather than from an artist's description.
- The target shape of the pipeline: a fixed skeleton plus known geometry and physics, then one universal graphic designer working with AI fills in the art.
- The squashed picture in the demo is a local display artifact, not a defect — no work spent on it.
- Igor keeps working in the existing branch; the changes get moved to a fresh branch later if the product goes ahead.

## Open Questions

- **How the pay table fits the skeleton.** Pavel and Irina say it is laid out differently in every game. Anton's grey-square template and Pavel's idea of overlaying pre-made frames on the generated video were floated but nothing was settled.
- **When Val and Igor meet** — Saturday, Sunday or Monday. Igor writes tomorrow.
- The old horizontal scene and the steal scene still break; nobody has been assigned to them yet.

---
*Processed from Teams transcript on September 17, 2026, 1:12 PM Eastern*
*Source meeting: Game_Conversion_progress*
