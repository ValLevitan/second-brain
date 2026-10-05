---
type: decision
title: MVP 1 of the AI project manager works from Microsoft's own Teams transcripts as they are; re-transcribing the audio through Whisper with the glossary waits for MVP 2 (too much volume, too slow, real money); the 318 transcripts are processed and stored in GitHub, with a real database maybe later
date: 2026-10-02
aliases: [Whisper to MVP 2, AI PM MVP1 uses Teams transcripts, готовые расшифровки митингов, виспер MVP 2, transcripts stored in GitHub, repository as the base for the project manager, SQLite or vector later, 318 transcripts in GitHub, перевёл всё в MVP 2]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# MVP 1 uses the Teams transcripts as they are; Whisper waits for MVP 2; the transcripts go to GitHub

Stated by [[wiki/people/andrey-bosik.md|Andrey Bosik]], owner of the AI PM since Sept 29, at the [[wiki/meetings/2026-10-02-ai-pm-status-listener-core-and-318-transcripts.md|Oct-2 "Design_AI-PM - status" call]] (Russian), with [[wiki/people/val-levitan.md|Val Levitan]] listening and not objecting [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]. It narrows the Sept-29 plan on [[wiki/decisions/2026-09-29-bosik-owns-the-ai-pm-the-meeting-bot-waits-and-the-second-brain-is-built-first.md]]; the whole picture is on [[wiki/projects/ai-project-manager-and-company-second-brain.md]].

## 1. Teams transcripts now; Whisper later

Bosik: "Я думал сначала брать аудиозаписи, прогонять их через виспер и потом вместе с гласарем обрабатывать это в транскрипте, потому что это будет более качественный транскрипты, чем Майкрософт. Но я подумал, наверное, что это будет очень большой объём, это будет занимать долго по времени и вероятнее всего будет стоить достаточно приличных денег, потому что через [—] Виспер это всё придётся гонять. Вот я, по крайней мере это перевёл всё в MVP 2, так сказать. На MB один пока что будем использовать готовые расшифровки, митингов и [Teams]." No figure for the cost or the volume was given [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]].

*(This is the Whisper-with-glossary route of the May-2026 pipeline on [[wiki/topics/transcript-knowledge-base-tooling.md]], set aside for the first version — inference; the call names only "виспер" and "гласарь".)*

## 2. What was collected

"Мы смогли собрать все доступные нам историю встреч… Мы смогли забрать расшифровки. Митингов [Teams] с майкрософта"; "мы собрали 318 расшифровок, они собрались с июля 25, потому что есть ограничения по хранению соответственно" — 318 transcripts, from July 2025, bounded by Microsoft's retention [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]. This answers the Sept-29 question "what period of transcripts" (Val: "с января 2026… может, с июня… вам виднее") — the period is what retention allows, and it reaches further back than either of Val's guesses.

## 3. Stored in GitHub; a real database maybe later

Val: "Где вы их храните?" Bosik: "Я их, я их пока забрал, но ещё не храню, но они будут обрабатываться и будут храниться в [GitHub]. Там есть такое. У нас вот этот репозиторий будет использоваться как база для последующего проджект менеджера, по крайней мере в начале. Возможно, в будущем мы эти расшифровки переведём в какуюто реальную базу данных, типа там [SQLite — the notes' reading of "is lite"] или в какуюто векторную. Вот но для старта этого вполне достаточно." Val asked no more [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]. This is Bosik's Sept-29 position ("Obsidian can use GitHub as its storage anyway"; keep the transcripts in a repository as plain storage) carried out; Val's own Obsidian-plus-local-index pattern was not raised on this call.

The derived notes record the same two rulings and attribute the Whisper deferral to Bosik [[raw/Meeting_Notes_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]].

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — process the 318 transcripts and store them in the GitHub repository that will be the project manager's base — due unspecified; next status Tuesday Oct 6 2026 — [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]

## Open questions

- When, and on what measure, does the transcript store move from the GitHub repository to a real database (SQLite or a vector database)? "для старта этого вполне достаточно" — [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]

**§15.8:** clear — tooling, scope and tool economics only (no figure given). **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]
- [[raw/Meeting_Notes_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]
