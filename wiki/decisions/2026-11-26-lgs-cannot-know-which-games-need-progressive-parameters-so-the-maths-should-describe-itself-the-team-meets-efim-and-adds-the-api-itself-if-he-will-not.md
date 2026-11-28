---
type: decision
title: LGS must now pass progressive parameters to the games' maths at start-up, but only where they are needed — and LGS cannot know where; Efim built it his own way (his match-3 maths is in the last build but needs his new approach, which the team does not accept), so the maths should describe itself through an API ("who are you, which version, which games, which parameter template") — the team meets Efim the same day, and adds the API itself if he will not; Kharetski's three-game ISO is tested on the existing stand, then the same drive on a touch machine; Igor's game loading drops from 10–12 seconds to about 2; tagged integration autotests are proposed (NOVA stand-up, Nov 26 2026)
date: 2026-11-26
aliases: [progressive parameters, параметры прогрессива, progressive settings to the maths, LGS passes progressive parameters, maths info API, математика ты кто, who are you which version, maths self-description, Efim new approach, extend the maths API, мы сами добавим, MCP for the maths, rebuild maths for one game, Efim meeting Nov 26, three-game ISO, ISO with 3 games, touch machine test, faster game loading, 2 seconds loading, shared resources in memory, touch support, movable vertical machine, stand on wheels, tagged autotests, test tag per pull request, integration repository tests, SAS tool in integration repository, LFS files not pushed, run a game from the brief, run game from the studio]
source-count: 2
status: active
open-commitments: 7
open-questions: 3
---

# Progressive parameters: the maths should tell LGS what it needs — a meeting with Efim; the three-game ISO goes on a machine (Nov 26 2026)

Agreed at the [[wiki/meetings/2026-11-26-nova-standup-faster-game-loading-and-efim-progressive-parameters.md|Nov 26 2026 NOVA stand-up]] (Russian, 6:28 AM Eastern, 19 minutes), led by [[wiki/people/pavel.md|Pavel Frolov]] with [[wiki/people/alexander-biratka.md|Alexander Biratka]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] and [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]. Val was not present. The day before: [[wiki/decisions/2026-11-25-one-game-one-merge-into-the-nova-integration-branch-the-studio-stays-single-user-with-fixed-steps-for-now-and-the-brief-must-describe-the-help-screens.md|the Nov-25 NOVA ruling]]. Context: [[wiki/topics/nova-platform-architecture.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word; garbles are kept as heard.)*

## 1. Progressive parameters — LGS cannot know where they go

- **The old chain.** [[wiki/people/evgeny-kharetski.md|Kharetski]]: before, Igor put a field in the game or framework saying the game must initialise the maths with the progressive parameters; seeing that flag, the game asked for the parameters and passed them to the maths. "Сейчас этой цепочки нет. Сейчас LGS при инициализации игры должен отдать эти параметры. Но только туда, где они должны быть"; "Но элджесс не знает, нужны они там или не нужны пока что." [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
- **Efim's way.** Kharetski proposed to [[wiki/people/efim-podvoiski.md|Efim]] the simplest fix — send the parameters everywhere and let the maths decide — "Но он сказал, что он подумает, а потом сделал так, как удобно ему": send them only where needed. "я не знаю где они нужны, а где нет. И мне эту информацию, что взять неоткуда." [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
- **Ask the maths.** Igor: "Самый логичный было, если можно было бы в математике спросить". Pavel: a common interface where we ask "ты кто? Она говорит, я математика такой версии", which games it serves, and for a game "какой у тебя шаблон" of parameters. Kharetski: "это было бы максимально удобно." He has no access to the maths code — "мне его никто не даст"; Pavel has. Pavel ran a Claude query: "похоже, что там крайне мало что из математики можно получить", though "контракты там есть" [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]].
- **The ruling.** Kharetski: extending the API should be no problem for Efim. Biratka: "Но если он против, мы сами Добавим." Pavel: "как минимум у меня доступ уже есть, но у Антона, наверное, тоже." Biratka meets Efim the same day [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]].

## 2. Efim and the match-3 maths

- Irina: asked when he gives Igor the NOVA match-3 maths, Efim said "я 1 раз об этом слышу"; Kharetski and Biratka got the same answer. Igor: more than a week ago Efim told him it was not ready, so Igor made a different game [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]].
- Kharetski: Efim held the maths back "потому что мы не умели прокидывать параметры туда"; what he gave the day before is "Уже в белде есть, но чтобы его пронициализировать, нужно поддержать его новое решение, но с которым мы не согласны" — so Kharetski built his ISO without that game (heard "фен базен" / "твинбайзен" — the game name is **unclear**). "условия он выполнил, причем эээ достаточно быстро, за что ему спасибо", though the day before Efim said he does not like working in several branches [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]].

## 3. The meeting with Efim

- Biratka sets up "с ефимом митинг… маленький"; Irina asked to join (Pavel: "как optional"); Leshkevich wants to raise an MCP for the maths — Biratka: "Мы бы могли сами там добавлять TMCP"; Pavel wants Efim to explain the general maths set-up — he has access and wants to "подправить быстренько пересобрать для какихто отладочных целей под одну игру". Attendees named: Biratka, Kharetski, Pavel, Leshkevich, Igor. About 45 minutes, "через часик"; Biratka asked Pavel to create it — "Ну давай давай" [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]].
- This is the general call with Efim that Pavel and Kharetski wanted on Nov 25.

## 4. Faster game loading and the three-game ISO

- **Igor.** All games cannot be held in memory at once. After a game was picked, the loading screen used to take "где то 10 12 секунд"; now "грузится быстрее там в течение 2 секунд условно"; resources shared by all games stay in memory. He also added touch — "У меня клод сказал, что он начал поддерживать" [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]].
- **Where to test.** Kharetski: an ISO with three games is ready — "Несколько игр, ей уже готова с 3" — but the current stand has no touch panel. Irina offers the two vertical machines behind her, kept for such experiments. Pavel's plan: "1 ставишь на ту машину, которая есть это 22 минуты. Эту же флешку вставляешь в другую машину, мы сразу проверяем." ("на вы 1000" — which machine is **unclear**.) [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
- **One more test machine.** Pavel: build another movable vertical machine — buy "треногу, которая… на колёсиках" [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]].

## 5. Tests — not enough hands; tagged autotests

- Irina asked how much work Igor has before he can write the tests Biratka wants; Biratka: first the tasks from the requirements he made, then tests. Irina: "просто физически у нас не хватает рук." Kharetski: the new integration repository "готов к написанию тестов", with the SAS tool connected, so SAS and LGS tests can be written. Biratka's student comes in mid-December. Pavel: even just creating test tasks for features helps. Irina asked to wait until Monday [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]].
- **Tagged autotests (Kharetski).** He will have his Claude list what the integration repository and the others need so that a pull request in any component creates a tag for tests, and the integration repository runs "не все тесты, а те, которые отмечены этим тегом" — otherwise one waits "02:00" (two hours) on every pull request. Biratka reviews it; then it becomes a task [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]. Thread: [[wiki/topics/test-automation-strategy.md]] (Nov 26).

## 6. Studio and LFS

- Leshkevich is adding a way to run a game straight from the studio, partly done. Some LFS files had never been pushed — Biratka could not check out the engine and framework; Igor: they stayed "У меня и у Антона". Leshkevich re-uploaded them from his laptop and added guards that check the files are present. Biratka: "чтоб любой мог выкачать и запустить." Leshkevich's goal: by the end of the week a game can be launched from the brief [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]].

## How it sits against earlier rulings

- **Nov 25 — match-3 maths and the Efim call: evolution.** On Nov 25 the match-3 progressive maths was missing and a general call with Efim was wanted; on Nov 26 Efim had delivered it, but tied to his own way of passing the parameters, and the call is set for the same day — [[wiki/decisions/2026-11-25-one-game-one-merge-into-the-nova-integration-branch-the-studio-stays-single-user-with-fixed-steps-for-now-and-the-brief-must-describe-the-help-screens.md]] (Nov-26 note).
- **Sept 3 — the NOVA integration repository.** The repository now holds the SAS tool and is ready for integration tests — [[wiki/decisions/2026-09-03-module-contracts-and-nova-integration-repository.md]].

## Open commitments

- [ ] [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] — install the three-game ISO on the existing stand, then test the same drive on a touch machine — due Nov 26 2026 — [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — create the meeting with Efim (about 45 minutes, about an hour after the stand-up) — due Nov 26 2026 — [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
- [ ] [[wiki/people/alexander-biratka.md|Alexander Biratka]] — settle with Efim how progressive parameters reach the maths and whether he extends the maths API — due Nov 26 2026 — [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
- [ ] Pavel Frolov — build another movable vertical test machine (buy a stand on wheels) — due unspecified — [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
- [ ] Evgeny Kharetski — have Claude list what the repositories need for tagged autotests; give it to Biratka to review; make it a task — due unspecified — [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
- [ ] [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] — run a game from the brief in the studio — due end of the week of Nov 23 2026 — [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — plan the test tasks — due after Monday Nov 30 2026 — [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]

## Open questions

- How will LGS know which games need progressive parameters? To settle with Efim — [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
- Will Efim extend the maths API so it describes itself, or does the team add it? — [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
- Does the three-game ISO run with touch on a vertical machine? — [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
- [[raw/Meeting_Notes_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026.md]]
