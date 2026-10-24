# Meeting Summary — Review - technical spec for the Dutch Mill theme abstract
**Date:** October 18, 2026, 11:02 AM – 12:01 PM Eastern
**Duration:** ~59 minutes
**Attendees:** Val Levitan, Igor Metelski, Pavel Frolov, Irina Shishko, Evgeny Kharetski
**Raw transcript:** [[Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026]]

## Summary

Held in Russian.

**Igor's spec.** Igor showed his spec as an HTML page in Russian and English (with a language switch), plus an md file to feed to Claude. It lists general rules, screen settings, element layout, which elements animate and how, and then each screen (base game first) with element positions.

**Val's changes to the spec:**
- **Rename it.** Not a "re-skin" document. Name it a specification for creative direction for game designers, for the vertical screen on the NOVA platform. Remove the word "re-skin" everywhere, including folder and archive names. Val: "forget the word re-skin"; it leads people to the wrong ideas.
- **Positions in pixels and percent.** Abstract-thinking people do not think in pixels. Add an intro paragraph that explains how positions are given, with an example. Then show every measure in two columns: pixels and percent of the screen. Igor added normalized coordinates during the meeting.
- **Taxonomy table.** Put all the terms in one table with meanings. Say that the team is open to suggestions on the terms.
- **Write it out fully in Russian first.** Several points (item 4 on the base game, item 6 on the reel center, item 7 on frames) are too short; the English translation is not clear to an English-only reader. Igor should describe each point fully and in detail in Russian (he may record himself), then translate. Do not shorten. Val suggested Igor give Claude this meeting's transcript to rewrite item 4.

**Irina's AI test.** Irina gave the spec to Claude and asked it to invent a theme and build to the spec. It chose fantasy and drew screens, but missed some placements and the accent elements Igor described. Igor: the document is not yet clear enough. Val: that is because the document is too short. Igor must finish the document, then run Irina's test again.

**Evgeny's test.** Val asked Evgeny to act as VP of game design and use the spec to write a creative direction for Dutch Mill. Evgeny had Claude do it and shared the result. Val said it works.

**Crazy Spins vertical in about 2 hours.** Igor showed the vertical version of Crazy Spins (a Texas / Nebraska game, more abstract than Dutch Mill). He gave Claude the instructions and got the result in about 2 hours; art was filled in with ChatGPT where needed. Val was very pleased and said he takes back his earlier "a game in a month". Pavel: about 14 hours per game, of which about 1.5 days is testing (as heard).

**Free-spin layout.** Igor added a free-spins screen layout to the spec, though Dutch Mill has none. Later, someone like Sergey could add free spins to Dutch Mill from a math version that has them.

**New project: AI Game Design Assistant (voice).** Val wants a voice-to-voice AI assistant that talks with the head of game design. It asks guiding questions and pulls out everything not yet said: theme first, then background, symbols, transitions. The output is a creative direction document that follows Igor's spec. The next step, later, is turning that text into code. First pass: voice to text and text to voice (ElevenLabs gives voice tools); then voice to voice. Andrei Bosik must be brought in, since he already works on voice for the AI PM. Pavel added that the AI could make sketches between calls and show them at the next call for feedback. Val mentioned putting a strong local computer (with Kimi, as heard) to generate files on the spot, but said to start without it and experiment with Sergey on any game he has. Until this works as a system, the team keeps making games for Texas.

**Owner.** Evgeny takes the project as owner and works with Igor, who checks that the output is right. Evgeny asked for one week. New Jira project and repository; Val named it "Game Design Assistant" (as heard). Evgeny will first talk to Andrei Bosik.

**Change games on a machine.** Val asked if, on a machine with a NOVA module (Texas), the team can erase a game and write a new one. Pavel: not now, but not hard. The system stays untouched; a second partition holds game files; each NOVA game is separate with its own checksum. It needs an architecture design. Val asked Pavel to make that design and plan the work for people.

**Wednesday stays.** Val asked if the Wednesday meeting is still needed. Pavel and Irina: yes, the team still needs the NOVA game; so far only the Rage version exists. The Wednesday meeting stays.

## Decisions Made

- **The spec is renamed to a creative direction specification for game designers (vertical screen, NOVA); the word "re-skin" is removed everywhere.** (Decided by Val Levitan)
- **Positions are given in pixels and in percent of the screen, with an intro and example; a taxonomy table is added.** (Decided by Val Levitan)
- **Igor rewrites each point fully in Russian first, then translates; no short forms.** (Decided by Val Levitan)
- **New project: AI voice Game Design Assistant that guides the head of game design to a creative direction document; Evgeny owns it, Igor supports; new Jira project and repository.** (Decided by Val Levitan; Evgeny accepted)
- **Review of the assistant's first pass next Sunday, Oct 25.** (Decided by Val Levitan)
- **Wednesday Oct 21 review of Dutch Mill on NOVA stays.** (Val, after Pavel and Irina)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Metelski | Rename the spec and files; remove "re-skin" everywhere | TBD | High | |
| 2 | Igor Metelski | Add pixel + percent columns with intro and example, and a taxonomy table | TBD | Normal | Partly done in the meeting |
| 3 | Igor Metelski | Rewrite each point fully in Russian, then translate; fix items 4, 6, 7 | TBD | High | |
| 4 | Igor Metelski | Re-run Irina's AI test on the finished spec | After item 3 | Normal | |
| 5 | Evgeny Kharetski | Build first pass of the AI voice Game Design Assistant (voice to text, text to voice), with Igor | Oct 25, 2026 | High | Evgeny asked for one week |
| 6 | Evgeny Kharetski | Talk to Andrei Bosik about voice technology | Before item 5 | Normal | |
| 7 | Evgeny Kharetski | Create the new Jira project and repository "Game Design Assistant" | TBD | Normal | Name as heard |
| 8 | Pavel Frolov | Architecture design to erase and write games on a NOVA machine in the field; plan the work for people | TBD | Normal | |
| 9 | Val Levitan | Set meeting next Sunday to review the assistant | Oct 25, 2026 | Normal | Done — see Dispatch Log |

## Open Questions

- Sergey's role in the assistant tests (Val suggested starting experiments with him). Not settled.

## Dispatch Log

- 2026-10-18 12:23 PM ET — Teams invite sent on Val's request (item 9) to Evgeny, Igor, Pavel, Irina, Andrei Bosik: "Review - AI voice Game Design Assistant, first pass" Oct 25 8:00–9:00 AM ET. Wednesday Oct 21 review already booked earlier today.

---
*Processed from Teams transcript on 2026-10-18*
*Source meeting: Review - technical spec for the Dutch Mill theme abstract*
