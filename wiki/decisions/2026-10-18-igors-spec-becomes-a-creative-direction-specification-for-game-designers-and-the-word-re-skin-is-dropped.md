---
type: decision
title: Igor's spec becomes a "specification for creative direction for game designers" (vertical screen, NOVA); the word "re-skin" is dropped everywhere; positions in pixels and percent; a taxonomy table; each point written out fully in Russian first (Val, Oct 18 2026)
date: 2026-10-18
aliases: [creative direction specification, specification for creative direction for game designers, spec for creative direction, технический документ, спецификация, forget the word re-skin, забыть слово рискин, pixels and percent, нормализованные координаты, normalized coordinates, taxonomy table, таксономия, Irina's AI test, Evgeny's VP of game design test, free-spins layout]
source-count: 2
status: active
open-commitments: 4
open-questions: 0
---

# Igor's spec becomes a creative direction specification; "re-skin" is dropped

Set by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-10-18-creative-direction-spec-review-and-game-design-voice-assistant.md|Oct 18 2026, 11:02 AM review]] (Russian, about an hour) with [[wiki/people/igor-metelski.md|Igor Metelski]] (presented), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]] [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]. It reviews the spec Igor agreed that morning to write for a new theme abstract — [[wiki/decisions/2026-10-18-rage-is-closed-dutch-mill-reaches-nova-by-wednesday-and-a-reskin-from-a-new-theme-tests-the-tools.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## What Igor showed

- **The form.** An HTML page in Russian and English, plus an md file with the same content "чтобы скормить клоду". The page switches between the two languages at the top; Igor: "Я я бы сам до этого не додумался, это клод." [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- **The content.** General requirements, screen settings, the layout and position of elements, which elements are animated and that their kind of motion must be thought out, animation settings; then screen by screen, the base game first, with element positions and a short description. The top of the screen is kept for the progressive; this document is for a one-level progressive [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **Item 4 — messages.** When the paytable filled the whole screen, symbols that pay nothing or lead to a bonus had their own frame there. With the paytable redone, a screen area is kept where such messages are written as text (for example, that a symbol gives free spins or leads to a bonus). Igor: the approach is already used in new games and should become common [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **A free-spins layout.** Igor added a free-spins screen layout though Dutch Mill has none. Dutch Mill had many maths versions by jurisdiction, so later someone like Sergey ([[wiki/people/sergey-kleimenychev.md|Sergey Kleimenychev]] — **inference**) could add free spins to Dutch Mill "на базе. Математики, в которой они есть" [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].

## What Val decided

- **Rename it; forget "re-skin".** Val: "я бы не называл бы это ризхин"; the subject is a specification for creative direction for game designers, for the "вертикальный экран" and "для нова платформы". He had the word removed everywhere — page, file, archive and folder (Irina: rename the folder too). Later: "у вас везде проскальзывает слово рискин я хочу убить это в корне" and "Я, я прошу вас забыть слово рискин… Потому что направление резки нас наводят на неправильные мысли." [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]] [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- **Pixels and percent.** People used to talk about abstract things do not think in pixels — "что такое, например, 10 пикселей сверху?" Igor offered normalized coordinates (a 540 element on a 1080 screen = 0.5); Pavel: "или 50 50%"; Val: "Вот в процентах давайте да", and keep both. Add an intro paragraph that explains this with an example, then give every measure in two columns, pixels and percent. Igor added normalized coordinates and an explanation during the meeting [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **A taxonomy table.** All the terms JVL uses in one place, with what each means, and an invitation to suggest better terms "чтобы люди не думали" the terms are fixed [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **Write it out in full Russian first.** Item 4 is well said aloud "но в письменном виде 4 пункт не описан" — Val advised giving Claude this meeting's transcript to rewrite it. Item 6 (the reel centre, a Y coordinate) and item 7 (frames) are unclear; the English reads wrong to an English-only reader because the source was "Сокращённый русский язык". Val: describe each point "широко подробно", perhaps recording himself on a microphone, and do not shorten — "тогда и английский, и русский получится красиво, правильно" [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].

## Two AI tests of the spec

- **Irina's.** She gave the spec to Claude with "придумай сам… тему. Реализуй вот по этому документу"; it chose fantasy and drew screens. Igor: it did not see where some elements go and did not add the accent elements he described — "значит документ недостаточно понятный". Val: because it reads a shortened document. He wants Igor to finish the document, then run Irina's test again; going further before that "будет трата времени" [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **Evgeny's.** Val asked Evgeny to act as "Вицепрезидента по геймдизайн", with the whole creative team under him, and use the spec to give a creative direction for Dutch Mill. Evgeny fed the spec to Claude without reading the details and shared the result; he felt the time was too short. Val: "Срок нормальный, потому что я вижу, что это работает." [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- This led straight to the voice assistant — [[wiki/decisions/2026-10-18-evgeny-kharetski-owns-a-voice-ai-game-design-assistant-with-a-first-pass-reviewed-oct-25.md]].

## How it sits against earlier rulings

- **Renames the morning's plan.** At 8:04 AM the plan was a "re-skin" of Dutch Mill from a new theme abstract, on Igor's "техническое задание по написанию абстракта" — [[wiki/decisions/2026-10-18-rage-is-closed-dutch-mill-reaches-nova-by-wednesday-and-a-reskin-from-a-new-theme-tests-the-tools.md]]. The substance stands; the word "re-skin" is now banned (11:02 AM update there).

## Open commitments

- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — rename the spec and its files and folders; remove "re-skin" everywhere — due unspecified — [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — add the intro with an example, pixel and percent columns for every measure, and the taxonomy table (partly done in the meeting) — due unspecified — [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]] [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — write each point out fully in Russian, then translate; fix items 4, 6 and 7 — due unspecified — [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — run Irina's AI test again on the finished spec — due after the rewrite — [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
