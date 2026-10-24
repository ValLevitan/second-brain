---
type: decision
title: RAGE is finished — all new work is on NOVA; the first NOVA iteration of Dutch Mill is reviewed Wednesday Oct 21; a re-skin from a new theme abstract (Michael writes it, on Igor's spec) tests whether an artist can use the tools alone (Val, Oct 18 2026)
date: 2026-10-18
aliases: [Rage is closed, Rage закончился, ничего под рэйдж больше не делается, Dutch Mill on NOVA Wednesday, first iteration Dutch Mill NOVA, Dutch Mill re-skin, рискин дач мила, theme abstract, абстракт, technical spec for the abstract, техническое задание по написанию абстракта, Michael writes the abstract, three tool sets, Conversion Cycle Texas Rage Horizontal to Texas NOVA Vertical, question pause answer, вопрос пауза ответ, 15 hours per game]
source-count: 10
status: active
open-commitments: 6
open-questions: 4
---

# RAGE is finished; Dutch Mill reaches NOVA by Wednesday; a re-skin tests the tools

Set by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-10-18-dutch-mill-rage-to-nova-conversion-and-reskin-plan.md|Oct 18 2026, 8:04 AM session]] (Russian, about 40 minutes) with [[wiki/people/igor-metelski.md|Igor Metelski]] (presented), [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]]; [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] was present but only greeted [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]. It is the meeting with Val that Igor and Pavel asked for on Oct 16 — [[wiki/decisions/2026-10-08-texas-rage-games-convert-to-vertical-nova-unchanged-and-igor-ports-dutch-mill-first.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## What Igor showed — a vertical Dutch Mill on RAGE, in one week

- **The method.** As with Dragon Pays, he built the vertical version from the horizontal resources. Dragon Pays was easier — a new game with fairly modern art; the older games ("из нада") have more primitive art. He first assembled a master frame from the existing resources, fed it to ChatGPT and Gemini to bring it to an acceptable level, "и потом мы с клодом долго долго это всё пытались заанимировать" [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].
- **What is in it.** The base game, one Dutch Mill bonus, and one bonus shared by all games of the product. In the base game the sky, the mill, the girl and the background are animated. 4 symbols were redrawn because the old ones did not fit the new background style, and all 4 are animated. The help screen is new. The shared bonus got the least time "Остался, наверное, не самым красивым." [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- **On RAGE, not NOVA yet.** Irina asked; Igor: "Рейдж." He has not moved this game to NOVA but can [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].
- **Time.** "всё, что сделано, вот это сделано за неделю" [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].
- **Ready to start.** [[wiki/people/efim-podvoiski.md|Efim]] sent him a container with the maths, which he expects to run locally. "мне нужен только репозиторий для дач милой и все я готов начинать." [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- **Video loops** — the art detail is on [[wiki/topics/game-art-animation-production-pipeline.md]] (Oct 18).

## The estimate

- Of the Texas games, only Dutch Mill had fairly complex art with real-world objects; the others are more abstract and should take less than a week each. The move to NOVA itself: "я бы оценил не дольше, чем в 15:00" — per game. Read as 15 hours (the notes' reading — **inference**). Games live in their own repositories, so once the art is ready several can be moved in parallel; the procedure is worked out and "описаны все тонкие моменты, на которых… клод задерживался" [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].
- Val: "это мы говорим где-то день работы, да?" Igor: "Ну я бы заложил 15:00, потому что… мы же ещё тесты пишем сразу". Earlier: "лично я со своим плодом вот этот вот точмин принесу дня за 3, скорее всего" (with his Claude, about three days) [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].

## Can an artist do the whole job?

- **Val's aim.** Train someone like [[wiki/people/sergey-kleimenychev.md|Sergey]] to do it, while Igor keeps polishing the environment until "я могу вместо Сергея брать ещё одного такого же грамотного. График дизайнера", who can move games from one market to another. Igor: possible, "но это надо пробовать"; today the environment is "набор н д файлов" — md files, the prose, ADRs, contracts and comments in the repositories [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].
- **Who.** Pavel named [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] ("Антон клишкевич") and Daniil (who is freeing up and can give about 50% of his time); Sergey has much less working time (detail not recorded, §15.8 note below). Val prefers Sergey "потому что он график дизайна": he can make things prettier on the fly, a developer cannot. Pavel: "Да, верно." [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- **Val's wider picture.** With ADRs, contracts and prose written properly and linked to acceptance criteria, "мы создаём экосистему, в которой можно все игры разрабатывать даже с самого начала и тестировать" — swap the maths, swap the pictures; e.g. ask Sergey for ten more 3×3 games with other themes. He also spoke of a "Модуль LTV" where JVL does not need to pass any approving bodies and can go from one location to 5–6 and then 50 — what "LTV" names is **unclear** [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].
- **Secret for now.** "Пока это все секрет, я держу, но потом это можно раздать всем художникам" — under the VP and the design director (heard "VPO в геймсте", "дизайн и директор"; who is meant is **unclear**). Val says the change is "революционная" and people are nervous about it now [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].

## Three kinds of tool sets (Pavel)

(1) RAGE horizontal → RAGE vertical; (2) RAGE vertical → NOVA vertical; (3) from a finished NOVA game, new games "с новыми графическими ресурсами, с новой математикой да 10 новых игр". Igor: for RAGE work, Valentin left a detailed install instruction; Visual Studio is now optional — a compiler with the "140 первым" toolset is enough, and Claude can set up a local environment from an instruction [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].

## What Val decided

- **RAGE is finished.** Irina asked whether the re-skin is for RAGE or NOVA. Val: "Rade. Закончился. Ничего под рэйдж больше не делается, всё делается только под новом." [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- **The Wednesday milestone.** "В среду мы… Увидим… первую версию конвертации игры с рэйдж на нова именно вот domel." The notes date it Oct 21 [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].
- **A re-skin test.** Igor proposed that Sergey re-skin Dutch Mill — a thematically different game (Val: a base game plus two bonuses, with all the animation and transition videos Dutch Mill has, on other scenes) — without Igor's help, using only the scene generator and the OMNI converter, to see how well the tools are documented: "если это не просто, то значит, что нам надо доработать документацию". Pavel: as framed, "Для меня это утопия": Sergey will ask what theme is wanted; he has said he can work from comp art but is wary of inventing one. Igor: pick a theme from the library of "пятиста 2 игр" (about 502, some repeats or versions for other jurisdictions). Pavel: then it is not from scratch. Val: base it "не на арт сделанный, а просто на тему"; the art is made from scratch [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].
- **Michael writes only the abstract.** Val: ask "Майкла" ([[wiki/people/michael-gottlieb.md|Michael Gottlieb]], by context — game design) "Чтоб он создал новую тему, которая реплейсе с dutch mell но только… Со стороны абстракта". Pavel: "Да думаю, это рабочий вариант." [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- **Igor's spec comes first.** Before the abstract is asked for, Igor writes "техническое задание по написанию абстракта" — the scenes and the components on each. Pavel: Michael is told the game is described by scenes with placeholders to fill with his vision; Irina's examples: main elements, symbols, bonuses, trees, umbrellas, sky, ground. Val: everything is broken down by scenes and screen fields with JVL's own taxonomy, "А с этим мы ещё никого не ознакамливали." [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- **Michael's reaction.** Pavel warned Michael may say "с ног на голову всё поставили" when the spec comes from an implementer. Val: "Да безусловно, но я думаю что я смогу" make it happen [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].
- **A review at 11:00.** Val set a meeting "на 11:00 канадского времени" the same day to review the spec; Igor, Pavel and Irina will be available [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]. The notes log both invites as sent: Oct 18 11:00–11:30 AM ET and Oct 21 8:00–9:00 AM ET [[raw/Meeting_Notes_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].
- **Meeting rule.** When Igor and Irina talked over a question, Val: "не отвечайте на вопрос во время во время вопроса… я не успеваю… Вопрос пауза. Ответ." [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- **Next two weeks — asked, not taken.** Val: "я не хочу быть законодателем. Следующих инженерных. Действий"; he asked Pavel or Igor to lay out the next two weeks — undertakings for developers and artists and milestones to check. Only the Wednesday milestone was set [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].

## How it sits against earlier rulings

- **Restates Sept 17.** [[wiki/decisions/2026-09-17-no-more-games-on-rage-and-texas-is-built-on-nova.md]] stopped new games on RAGE; Oct 18 goes further in words — nothing more is done for RAGE (Oct-18 note there).
- **Continues Oct 8.** [[wiki/decisions/2026-10-08-texas-rage-games-convert-to-vertical-nova-unchanged-and-igor-ports-dutch-mill-first.md]] had Igor port Dutch Mill to vertical NOVA by Oct 19; the vertical is done on RAGE and the NOVA move is now due for review Oct 21 (Oct-18 update there).

## Update — Oct 18 2026, 11:02 AM: the spec is delivered and renamed; "re-skin" is dropped; Wednesday stays

- **The spec arrived.** At the [[wiki/meetings/2026-10-18-creative-direction-spec-review-and-game-design-voice-assistant.md|11:02 AM review]] Igor showed it as a Russian/English HTML page plus an md file for Claude; Val asked for changes — [[wiki/decisions/2026-10-18-igors-spec-becomes-a-creative-direction-specification-for-game-designers-and-the-word-re-skin-is-dropped.md]] [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **The word "re-skin" is banned.** Val: "Я, я прошу вас забыть слово рискин… Потому что направление резки нас наводят на неправильные мысли." The plan above still stands in substance; the word in this page's title is kept only as the 8:04 AM wording [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **Wednesday stays.** Val asked whether the Wednesday meeting is still needed. Pavel: "мы же все равно хотим новой игру получить"; Irina: "Пока мы только рейч получили." Val: "в среду мы всё равно встречаемся" [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]] [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]].
- **A new path for the abstract.** Val also started a voice AI assistant to guide the head of game design to a creative direction document — [[wiki/decisions/2026-10-18-evgeny-kharetski-owns-a-voice-ai-game-design-assistant-with-a-first-pass-reviewed-oct-25.md]] [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]. The ask of Michael below stays open.

## Open commitments

- [ ] Owner not named — give Igor access to the Dutch Mill repository — due before work starts — [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — ask Michael to write a new theme abstract replacing Dutch Mill (abstract only) — due after the spec review — [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — remove the intermediate RAGE scene step so art goes straight to the OMNI scene converter ("это как бы я сделаю") — due unspecified — [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- [ ] [[wiki/people/sergey-kleimenychev.md|Sergey Kleimenychev]] — keep trying AI video tools for clean looping animations (not present) — due unspecified — [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]

## Open questions

- Who lays out the next two weeks — steps, undertakings and milestones for developers and artists? Val asked Pavel or Igor; nobody took it — [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- Who does the re-skin — Sergey (little working time), Anton Leshkevich or Daniil? Not settled — [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]

**§15.8:** Pavel's statement of Sergey's working days and hours is engagement detail and is not recorded (as on Oct 8). No pay appears. **§15 #9:** none.

## Update, Oct 19 2026 — a second game is already on NOVA; Leshkevich is invited to the Wednesday review; did Efim make maths for all six games?

At the [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct-19 Minsk stand-up]] (Russian; Val absent) [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] reported Clover Fortune moved from RAGE to NOVA, playing vertical and horizontal — detail on [[wiki/topics/nova-platform-architecture.md]] (Oct 19) [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].

- **Bring him to Wednesday.** [[wiki/people/irina-shishko.md|Irina]]: on Wednesday Igor is to show Dutch Mill moved from RAGE to NOVA; Anton has already done "как раз то, что должен делать этот Игорь", so "может быть, есть смысл и тебя на тот митинг подтянуть" to discuss both results and the plans. Anton agreed [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].
- **The maths.** For Clover Fortune [[wiki/people/efim-podvoiski.md|Efim]] made the maths container almost in one day. Irina understood from Igor that Efim did it for all games ("это все 6"); Pavel remembered Igor saying he asked for one and does not know whether there are several. "Надо спросить у Игоря." [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- **On the open question "who does the re-skin".** Not taken up. *(Leshkevich now has a finished NOVA port of his own, which is why Irina wants him at the review — **inference** as to its bearing on that question.)*

### Open commitments (Oct 19 2026)

- [ ] Unassigned (Irina and Pavel raised it) — ask Igor whether Efim made the maths for all six games or only one — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]

### Open questions (Oct 19 2026)

- Did Efim make the maths containers for all six games or for one? Irina and Pavel remember Igor differently — [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]

## Update, Oct 20 2026 — Igor ported Dutch Mill to NOVA in one session of about six hours; Pavel: the ports can now go "on a conveyor"

At the [[wiki/meetings/2026-10-20-daily-standup-io-board-firmware-via-github-and-vp9-video-decode.md|Oct-20 Minsk stand-up]] (Russian; Val absent) [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]:

- **Dutch Mill is ported.** [[wiki/people/igor-metelski.md|Igor Metelski]]: "Я сделал… Порт дачмила", "фактически одной сессии в течение ну там часов 6". He has a number of graphic remarks on it. He will start a session to fix what he sees by eye and add each defect to the requirements list, so that on the next port such defects are caught by the harness and testing. That day he tests the port.
- **Other work.** Igor prepared the main scenes and symbols of a vertical Texas Midnight Money and will finish its scenes; he also mentioned vertical versions of Dutch Mill and Midnight Money ("из небраски 1", as heard — what he meant is **unclear**). He updated resources for Nebraska 2 as the designers sent them (in one game a bonus did not work) and must fix the spec written on Sunday to Val's requirements [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]] [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]. ("нато 2" as heard = Nebraska 2 — **inference** from context and the notes.)
- **Ready for a conveyor.** [[wiki/people/pavel.md|Pavel]]: over the last week everyone, Igor first, was asked whether anything still blocks moving the games over in production mode. Nobody answered directly, but he understands the answer is yes. It will be discussed "завтра" at the meeting: Igor took an entirely new game and ports it. Igor showed him Midnight Money the day before; "не хуже оригинала, а даже лучше". The remaining games must now be split among people, and the build side ("сборки всего") finished after that. [[wiki/people/irina-shishko.md|Irina]] asked who will write the tests [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]].
- **Leshkevich.** He fixed the vertical help screen in Clover Fortune, which "плюс минус" looks ready to him, and ported one Georgia game into Nebraska 2. He asked for the invite to the Wednesday meeting with Val; Irina forwarded it during the meeting ("Антон я тебя переслала") [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]] [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]].
- **A risk for the conveyor.** Multi-screen horizontal games stutter on the new board, and NOVA's VP8 videos may have no hardware decode there — detail on [[wiki/topics/nova-platform-architecture.md]] (Oct 20). Igor: it would be unpleasant if everything ported had to be redone later.
- **On the commitments.** Igor's Dutch Mill port exists before the Wednesday review; "first iteration with tests" is not confirmed, so his line stays open until the review. The question on Efim's maths was not taken up.

### Open commitments (Oct 20 2026)

- [ ] Unassigned (Pavel) — split the remaining game ports among the team — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]

### Open questions (Oct 20 2026)

- Who writes the tests for the game ports? (Irina) — [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]] [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]

## Update, Oct 21 2026 (8:02 AM) — the Wednesday review: Dutch Mill runs on NOVA with tests; a vertical Midnight Money built from a theme; the meeting turns to a native engine

At the [[wiki/meetings/2026-10-21-dutch-mill-on-nova-and-native-engine.md|Oct-21 review]] (Russian; Val, Igor, Leshkevich, Biratka, Pavel, Irina, Kharetski) [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]:

- **Dutch Mill on NOVA.** [[wiki/people/igor-metelski.md|Igor]]: "порт вертикального дачмила… На нова платформу готов… Все бонусы рабочие". The progressive bonus "было плохо сделано и в рейдже недоделать чутьчуть". From the port he wrote acceptance criteria and requirements linked to a capability — "пока всё ещё локально в виде черновика". A test harness and a test scenario are done; the harness did not start correctly the first time and needed a separate session. The port took about one session (garbled "примерно 06:01 сессия"; cf. about six hours on Oct 20), a parallel session of about the same time for the tests, and one more session of a couple of hours to fix what he saw by eye; all of it was added to the acceptance criteria and requirements, so the list grows port by port [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **A vertical Midnight Money from a theme.** In parallel Igor made a vertical version of the horizontal Midnight Money: screen geometry from Lion's Riches (the notes: "Lion's Rich"; "лайн рич"), the newest vertical from GCOAM 3, 5 reels × 3 symbols; theme and maths from Midnight Money; art generated — detail on [[wiki/topics/game-art-animation-production-pipeline.md]] (Oct 21). It runs on RAGE only so far. Texas now has three vertical versions: one on NOVA, two still RAGE only [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **Val's reading.** Igor played a designer who dictates a theme in words, and the game is built programmatically: "Проиграть роль дизайнера, который в принципе может продиктовать новую схему. И… Программчески это можно всё собрать." Igor: "А именно так." Val praised Igor's work [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]. *(This is the theme-to-game test the re-skin was meant to run, done by Igor himself on another game — **inference**; the Dutch Mill re-skin by Sergey and the abstract from Michael were not discussed.)*
- **Leshkevich's port.** [[wiki/people/anton-leshkevich.md|Leshkevich]] also converted Clover Fortune from Nebraska to NOVA "в качестве экстерза" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **Then the engine.** Leshkevich used the review to reopen the browser question; Val ruled to drop the browser for a native engine, set "no code before capabilities", and defined MVP1 as six Texas games on a stable NOVA — [[wiki/decisions/2026-10-21-nova-drops-the-browser-for-a-native-engine-no-code-before-capabilities-and-mvp1-is-a-stable-nova-releasing-six-texas-games.md]]; product owner and capability process — [[wiki/decisions/2026-10-21-vladimir-samusenko-is-invited-as-nova-product-owner-and-capabilities-are-drafted-one-file-per-person-before-grooming.md]].
- **On the commitments.** Igor's NOVA first iteration with tests is shown — discharged. His Oct-20 defect fixes are done and added to the criteria — discharged. Not taken up: the Dutch Mill repository access line, Michael's abstract, the intermediate RAGE scene step, Sergey's loops, the maths-for-six-games question, who splits the remaining ports, who writes the tests. They stay open.

## History

- [x] [[wiki/people/igor-metelski.md|Igor Metelski]] — move Dutch Mill from RAGE to NOVA, first iteration with tests — due Wed Oct 21 2026 review — [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]] — **discharged Oct 21 2026**: shown at the review, all bonuses working, with a test harness and scenario [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- [x] [[wiki/people/igor-metelski.md|Igor Metelski]] — fix the visible graphic defects of the Dutch Mill port and add each defect to the requirements list so the harness catches it next time — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]] [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]] — **discharged Oct 21 2026**: a session of a couple of hours fixed what he saw, and the acceptance criteria and requirements were extended [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]

- [x] [[wiki/people/irina-shishko.md|Irina Shishko]] — invite Anton Leshkevich to the Wednesday Dutch Mill review — due Wed Oct 21 2026 — [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] — *discharged Oct 20 2026: Irina forwarded him the invite during the stand-up* — [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]

- [x] [[wiki/people/igor-metelski.md|Igor Metelski]] — write and send the technical spec for the theme abstract (scenes, components, placeholders) — due Oct 18 2026, before the 11:00 AM ET review — [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]] — **done:** shown at the 11:02 AM review the same day [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- [[raw/Meeting_Notes_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- [[raw/Meeting_Transcript_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- [[raw/Meeting_Notes_Creative_Direction_Spec_Review_and_Game_Design_Voice_Assistant-October-18-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
