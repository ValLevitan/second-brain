# Meeting Summary — Update on Games Conversion

**Date:** September 20, 2026, 7:04 AM - 8:03 AM Eastern
**Duration:** approximately 60 minutes
**Attendees heard:** Igor Metelski, Pavel Frolov, Irina Shishko, Val Levitan
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026]]
**Source meeting:** Update on Games Conversion — Microsoft Teams

## Summary

Igor showed the geometry standard he wrote for vertical game screens, and Val turned the meeting into a decision about where that work has to live and what shape it must take.

**The geometry document.** Igor took the GKM3 product as the base, because its art is the newest, and from its games he wrote requirements for the geometric parameters of a vertical screen. Claude's review says 66 scenes have to be built in vertical format, plus about 60 symbol scenes if the symbols are also redone. The screen is split into zones: a 1920x1080 vertical background video, the frame area for the reels, the logo, an accent element (for example the woman in Crest City Carnival), a frame for progressives, and the dashboard area. Each element has a written position and size, in text, in a table, and in drawings. He covered layouts 3x5 and 3x3, and the main screens — base game, free spins, messages, transitions, pre-win recognition, anticipation, pay table, and help.

**Bonus screens had no reference.** The NATO product has bonuses with no equivalent in GKM3 — the Dutch Mill plate-picking bonus, the Clover Fortune bonus, the Gem Brilliant bonus. Because there was no vertical original to copy, Igor asked Claude to propose vertical layouts from the two-screen horizontal ones. The documents describe the bonuses without naming the games on purpose, so the standard is not tied to a single title.

**Transitions.** Igor also wrote the timing rules: the transition starts transparent over the base game, the base screen dissolves, the transition art shows, then the transition art dissolves into the bonus screen. Pavel pushed back on the alpha graph in the document — he wants the base screen and bonus screen curves drawn under the alpha curve so the hand-off is visible. Igor agreed the AI-generated chart is wrong and has to be redrawn; an earlier draft was clearer.

**Liquid glass effect — the technical finding.** Today the designers bake the semi-transparent frames (dashboard, progressive frames, symbol backing) into the background video. Igor rebuilt that effect in a shader so the framework draws it on top of a clean video. He demonstrated it over an animated background: the programmatic frame refracts the moving picture correctly. Pavel called it the right approach — changing a game from three progressive levels to two would no longer mean remaking video. Irina had not realised the two were fused. Performance is not expected to be a problem: the GPU is not heavily loaded and the effect is a post-process shader. One limit found: the effect is baked into the background video material, so it does not apply to elements from other scenes; the engine has an unfinished piece of code (a placeholder) that would remove that limit if ever needed.

**Val's intervention on where this lives.** Igor had put the documents in the NATO project repository in SVN, with copies in the GKM3 branch. Val said that is wrong. He argued this is the first time in twenty years the company has approached visual game development correctly — with a real glossary and real definitions instead of "a bit blue, a bit orange" — and he wants that starting point sealed in GitHub, detached from any framework, as the beginning of the new development culture. Pavel's position was that the experiment stays where it is and only a game actually being made for Texas or Nebraska moves to a new GitHub repository; Val overruled it.

**What Val wants in GitHub.** Glossary, standards, and above all ADRs (architecture decision records) — he was explicit that the ADRs will dictate every later architectural decision. He told Igor to run Claude over the existing meeting transcripts to pull the ADRs out, discard the false ones, and keep the rest. He also asked for two additions to the glossary: a mathematical description of colour selection (Pantone-to-Pantone over a stated time or frame count, not a description of every gradient), and a description of materials and movement physics — even if incomplete, because that is where AI is heading. Igor's own term, "frameless integration" of objects, Val wants recorded as a defined term, extended to frameless integration of backgrounds.

**The stopwatch experiment.** Val wants to measure how long Claude takes to convert a finished horizontal Rage game into a working vertical Nova game, given the standards and glossary as input. Igor said end-to-end testing is unfinished and the full flow has to be complete before the measurement means anything. Val agreed on sequence: first organise everything in GitHub, second finish end-to-end testing, third run the conversion experiment.

**Designers stay out.** When Irina said the designers' source scenes (houses without frames) could be retrieved, Val was blunt that he does not want to share any of this approach with the designers — they would be frightened and would get in the way. Raw video is to be pulled from storage without involving them, or Sergey Klimenchuk can produce new art.

**Deadline.** Igor asked for a week to be safe; Val set Thursday and will book a one-hour meeting at 8:00 AM Eastern.

## Undertakings

| # | Who | What | Due | Priority | Context |
|---|-----|------|-----|----------|---------|
| 1 | Igor Metelski | Move and organise the geometry standard, glossary, and ADRs into GitHub as a self-contained starting point, detached from any framework | Thursday, September 24 | High | Val: "while everything is fresh in your head" |
| 2 | Igor Metelski | Add a glossary to the document, in Russian and English | Thursday, September 24 | High | Currently Russian only, written with Claude |
| 3 | Igor Metelski | Extract ADRs from the existing meeting transcripts with Claude, discard the false ones, and file them with the code | Thursday, September 24 | High | Val: ADRs are the most important part |
| 4 | Igor Metelski | Add "frameless integration" of objects and of backgrounds to the glossary as defined terms with their physics | Thursday, September 24 | Normal | Val asked for the term by name |
| 5 | Igor Metelski | Add a mathematical approach to colour — Pantone to Pantone over a stated time or frame count | Thursday, September 24 | Normal | To stop "a bit blue, a bit orange" descriptions |
| 6 | Igor Metelski | Redraw the transition alpha diagram so the base-screen and bonus-screen curves are visible under the alpha curve | Not set | Normal | Pavel's objection; the AI-generated chart is wrong |
| 7 | Igor Metelski | Finish the end-to-end auto-testing work so a full flow exists | After GitHub organisation | High | Stage two of Val's three stages |
| 8 | Igor Metelski | Run the stopwatch experiment: convert a horizontal Rage game to a vertical Nova game using the standards, and measure the time | After end-to-end testing | High | Stage three |
| 9 | Pavel Frolov | Carry the standard into the Nova framework as part of the unified skeleton, with a standard way for every game to call it | Not set | Normal | Val wants it repeatable and error-free |
| 10 | Val Levitan | Book the follow-up meeting for Thursday, 8:00 AM Eastern, one hour | Same day | Normal | Review of the GitHub consolidation |

## Decisions

- The geometry standard, glossary, and ADRs go into GitHub, treated as an experiment in a vacuum with no framework ownership — not into the NATO or GKM3 SVN repositories. Val overruled Pavel's proposal to leave it in place until a market game starts.
- ADRs are the priority artefact; they will drive later architectural decisions and must sit with the code in the repository.
- Liquid glass frames move out of the baked background video and are drawn programmatically by the framework, so video does not have to be remade when the layout or progressive count changes.
- The background video stays as few video streams as possible at run time (each video is a decoder and costs performance), but the source elements stay separate before baking so the composition can be changed.
- The alpha channel stays optional — it is not added where nothing happens, to avoid an extra Full HD decoder.
- The designers are not to be involved in this work. Raw source video is retrieved from storage directly; new art, if needed, comes from Sergey Klimenchuk.
- Work order is fixed: organise GitHub first, then finish end-to-end testing, then run the horizontal-to-vertical conversion measurement.
- The documents describe bonuses generically rather than by game name, so the standard is not tied to specific titles.

## Open Questions

- How far the colour glossary should go — Val said not every gradient needs a formula, and some things may stay descriptive; the question stays open as the work develops.
- Whether the materials and movement physics can be defined now at all, or only partially as a placeholder for later AI capability.
- Whether Claude can re-cut a static horizontal background by moving the horizon point, as Val believes, or whether the background has to be broken into separate elements first, as Igor argued. To be tested — Igor said it is cheap and can run in the background.
- Whether the transition overlay video should itself carry a calculated alpha, or whether that only adds load.
