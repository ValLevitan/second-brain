---
type: decision
title: No freeze is allowed inside a game — a game's bonus and feature videos are decoded when the game is entered and kept, not on the way into a feature
date: 2026-10-14
aliases: [no stutter inside a game, decode videos at game entry, в пределах одной игры подтормаживание не должно быть, bonus video micro-freeze, half-second micro-freeze, decode at game entry and keep, 5 games in 8 GB]
source-count: 5
status: active
open-commitments: 0
open-questions: 1
---

# No freeze inside a game: decode a game's videos when the game is entered

Set at the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 Minsk stand-up]] (Russian) by [[wiki/people/pavel.md|Pavel Frolov]], citing "Саша" from the day before; Daniil Stauskiy (no page) agreed. It is about new games on the cheap ARM board, the RK3576 — see [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]] [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

## The problem

- Daniil: the board's decoder did not support VP8, so he re-encoded the videos to VP9 with alpha built in ("по 8 у нас декодор не поддерживал, я просто перекодировал и по 9 с Альфа и встроенной") [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].
- Still open: when to decode a video — on entry into the game, or on entry into a feature. Entering a feature such as the bonus "везёт микрофриз какой то на полсекунды, типа это терпимо нетерпимо" — a micro-freeze of about half a second; is it acceptable? [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]

## The ruling

- **Pavel:** "как саша вчера говорил, что нет у нас в пределах одной игры подтормаживание не должно быть." If a new game needs bonuses loaded, "то при входе в игру, по идее их можно подгружать, но не не на ходу, не на переходе на какуюто фичу или на какой то бонус" [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].
- **Daniil:** "по входе в игру все видео, которые относятся к данной игре, декодировать сразу и держать их просто тогда" — decode all of a game's videos when the game is entered, and keep them [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].
- The notes list it as a decision by Pavel, citing Alexander, with Daniil agreeing [[raw/Meeting_Notes_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

**Who "Саша" is.** On Oct 13 [[wiki/people/alexander-biratka.md|Alexander Biratka]] said "с тормозами в самой игре мы не можем терпеть", and a small delay on entering a game can be tolerated if there is no other way — see [[wiki/topics/nova-platform-architecture.md]] (Oct 13). So "Саша" is Biratka by that record (**inference**) [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]].

## The cost

Memory. Daniil: "для 8 игр может и не хватит, но какихнибудь 5 игр, наверное, хватит 8" — 8 games may not fit, but about 5 probably fit in the 8 GB [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]. This links to the plan for a library of about 5 games on the RK3576 — [[wiki/topics/nova-platform-architecture.md]] (Oct 14).

## How it sits against Oct 13

On Oct 13 the question was whether to free decoded feature video after each feature (a small freeze) or keep it (about 3 GB more per game). Oct 14 settles the freeze part: keep the video, decoded at game entry. This is **evolution**. Daniil's Oct-13 idea — decode the chosen game's videos at the select screen and free them on return — is the same direction.

## Open questions

- How many games fit in 8 GB on the RK3576 when all of each game's video is decoded at game entry — about 5? (Daniil) — [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]

**§15.8:** clear.

## Note, Oct 23 2026 — entering a game takes about 2 seconds for one game and about 10 for another

At the [[wiki/meetings/2026-10-23-daily-standup-bill-validator-lockout-and-atlanta-port-test.md|Oct-23 Minsk stand-up]] (Russian; Val absent) Daniil Stauskiy checked a game's start when only that game's videos are decoded on entry: "ковер фортуна около 2 секунд, а вот колле еще около 10 секунд, что как я понимаю слишком долго для входа" ("ковер фортуна" read as Clover Fortune and "колле" as Calle Ocho — both **inference**). On memory: "рам будет хватать уже под даже наверное игр 8", and the processor and GPU will be the limit — how fast a game loads and whether it freezes. [[wiki/people/pavel.md|Pavel]]: the game ran on a board with 4 GB, with a large reserve; "Наверное, 4 игры запустятся" even on that board. Which board is not said [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]. This bears on the open question below (Daniil's Oct-14 estimate was about 5 games in 8 GB); it does not settle it.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]
