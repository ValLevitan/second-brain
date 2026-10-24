---
type: decision
title: A voice AI "Game Design Assistant" that questions the head of game design and produces a creative direction document to Igor's spec — Evgeny Kharetski owns it with Igor; new Jira project and repository; first pass (voice to text, text to voice) reviewed Sunday Oct 25 (Val, Oct 18 2026)
date: 2026-10-18
aliases: [Game Design Assistant, AI Game Design Assistant, геймдизайн IS astond, creative direction design assistant, кредит в дирекшен дизайн assistend, voice to voice AI assistant, войс ту войс эй ассистент, AI design assistant, ai дизайна asisnate]
source-count: 4
status: active
open-commitments: 3
open-questions: 1
---

# A voice AI Game Design Assistant; Evgeny Kharetski owns it

Set by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-10-18-creative-direction-spec-review-and-game-design-voice-assistant.md|Oct 18 2026, 11:02 AM review]] (Russian), after Evgeny's AI test of Igor's spec worked; [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] accepted [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]] [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]. The spec it serves: [[wiki/decisions/2026-10-18-igors-spec-becomes-a-creative-direction-specification-for-game-designers-and-the-word-re-skin-is-dropped.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## What Val wants

- **A conversational tool.** Val wanted to group Kharetski with Metelski on a tool for when the VP of game design writes a creative direction: it asks questions or repeats back when something is unclear — "Я тебя правильно понял?… Чуть чуть налево чуть чуть направо… чуть темнее чуть светлее" [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **The output is a document, not a game.** Evgeny asked whether the end of the cycle is a finished game. Val: "Ну конечно нет… все, что выходит, это документ, который описывает creative docien. Но описывает правильно, который соответствует метельского спецификации." The assistant's "наводящие вопросы" pull out "все вещи, которые ещё не договорены". The next stage, later, is "Перевод словесного языка в код" [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **Voice to voice.** Val restated it, partly in garbled English, as a voice-to-voice AI design assistant that can guide the head of game design to put his design intent into words ("verbal lies der desine intent", as heard), set out as a design direction resting on Metelski's spec. Evgeny and Irina confirmed: the assistant asks by voice and answers by voice [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **The order of questions.** Pavel: the agent could show the screen template and ask, position by position — progressive here, background there. Val: first the theme, then the background, then the symbols, then the transitions. He expects the first session to be hard: the VP of game design will say he cannot picture it — "Это будет ужас." [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- **Sketches between calls.** Pavel: after one pass the AI could go offline, generate sketches, and at the next call ask whether they match. Val mentioned putting a powerful local computer with "кими" (Kimi, as heard) to generate files on the spot; Pavel doubted it can do video. Val: "Попробуем сначала сделать без них", and experiment with Sergey (**inference**: [[wiki/people/sergey-kleimenychev.md|Sergey Kleimenychev]]) — any game in front of him, described in Russian. Until it works as a system the team keeps making games for Texas ("под текст", read as Texas by the notes) [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]] [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **Evgeny had started something similar** that was put aside; Val said it was put aside because he already understood it would work, and that now the point is a creative design that fully matches Metelski's spec, "в разговорном языке" (details **unclear**) [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].

## The technology

- **Bring in Bosik.** Val: "надо подтянуть сюда Андрея босика. Он уже делает войство войск для прочих менеджера" — [[wiki/people/andrey-bosik.md|Andrey Bosik]], who is building voice for the AI project manager ([[wiki/projects/ai-project-manager-and-company-second-brain.md]]). Pavel: Bosik's is an agent on his local computer that talks in text through chat now and will later be a character one can call [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **Known tools.** Val: the Grok chatbot already talks live; ElevenLabs ("leven labs") "предоставляют войс MCP. Бесплатно для использования", voice-to-text and text-to-voice, with a delay of a couple of seconds — "Её просто нужно чутьчуть адаптировать для нас." [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- **Two steps.** "1 проход это голос, текст текст голос, а потом голос голос." [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]

## Owner, time and name

- **Owner.** Val asked Metelski or Kharetski. Igor: interested, but Evgeny has the better background. Evgeny: very interested but has many tasks; he will need Igor's advice to check the output, so they work as two. Irina: the question is only who is responsible. Evgeny: "давайте я буду." [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- **One week.** Evgeny: "давайте возьмём неделю"; he has not yet talked to Bosik. Val: "Поехали неделю, значит это следующее воскресенье" — a meeting on Sunday [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]. The notes log the invite as sent: "Review - AI voice Game Design Assistant, first pass", Oct 25 8:00–9:00 AM ET, to Evgeny, Igor, Pavel, Irina and Andrei Bosik [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **Jira and repository.** Evgeny asked whether to make a new Jira project and repository. Val: "Конечно", code goes there; "проект называется геймдизайн IS astond" — Game Design Assistant (name as heard) [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]] [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].

## Note, Oct 19 2026 — Kharetski starts the agent

At the [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct-19 Minsk stand-up]] (Russian) [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] said he is starting "этот новый проджект… агент дизайнера" (the notes: the AI game designer agent [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]). [[wiki/people/pavel.md|Pavel]]: "это нам надо ещё в джире завести проекты для него." Evgeny: "Своем репозитории да всё, как полагается". Evgeny will work three directions at once: NOVA, Ivan's tests and the agent [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]. The notes list creating the Jira project as unassigned [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]; it stays on Evgeny here, as set on Oct 18.

## Open commitments

- [ ] [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] (with [[wiki/people/igor-metelski.md|Igor Metelski]] checking the output) — first pass of the Game Design Assistant, voice to text and text to voice — due Sun Oct 25 2026 review — [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]] [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- [ ] [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] — talk to Andrey Bosik about the voice technology — due before the first pass — [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- [ ] [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] — create the new Jira project and repository "Game Design Assistant" (name as heard) — due unspecified — [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]] — *Oct 19 2026: not yet done; Pavel said a Jira project is needed and Evgeny said it gets its own repository and features, "всё, как полагается"* — [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]

## Open questions

- What is Sergey's role in testing the assistant? Val suggested starting experiments with him; not settled — [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
