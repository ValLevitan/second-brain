---
type: decision
title: The horizontal Texas games on RAGE are converted to vertical NOVA games with Igor's 20% method, with no change to maths or function; Igor ports Dutch Mill first and Sergey Kleimenychev only makes the video (Oct 8 2026)
date: 2026-10-08
aliases: [Texas blind conversion, в тупую слепую, Texas Rage to Nova vertical, перевозим их на нова вертикальные, 20 percent stretch, symbols 20% taller than wide, Dutch Mill first port, дач мил, Kleimenychev video only, looping topper video, keep it confidential, держим конфиденцию, Games convert horizontal to vertical, one feature per game under capability 240, рейчту новым migration]
source-count: 15
status: active
open-commitments: 9
open-questions: 5
---

# The horizontal Texas games on RAGE go to vertical NOVA, unchanged; Igor ports Dutch Mill first

Taken at the [[wiki/meetings/2026-10-08-dragon-pays-vertical-accepted-and-dutch-mill-port-plan.md|Oct 8 2026, 10:02 AM session]] (Russian), the follow-up Val had set at the [[wiki/meetings/2026-10-08-rage-nova-dragon-pays-vertical-port-and-symbol-distortion.md|7:04 AM review]] the same morning. [[wiki/people/val-levitan.md|Val Levitan]] set the scope; [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] argued who does the first game, and Val agreed with them [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## What made it possible — the 20% method

[[wiki/people/igor-metelski.md|Igor Metelski]] showed a new vertical Dragon Pays [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]:

- **The idea.** The horizontal version already sent for production had symbols stretched sideways — about 20% wider than tall. Igor moved the same distortion to the vertical: "символ примерно на 20% выше, чем шире". His first try that morning (square symbols) left the reel frame too small.
- **How.** He told Claude to stretch the reel frame across the full screen width, worked out the symbol size, and made the frame three symbols high: "мы пересчитали размеры символов, умножили на 3, получили размеры рамки." Then he made the comp, built the scene and moved it to NOVA. The game runs on it.
- **Before, it was 40%.** Pavel asked what the earlier stretch was; Igor: "40%". Pavel: "Выглядит значительно лучше." Val: "всё получилось."
- **Time.** "ровно полтора часа", including 40 minutes to generate two videos (main game and free spins).
- **Small items.** Pavel did not like the turtle symbol; Igor can make that one symbol square and fill the rest with transparency. A gap between the logo and the pay table is reserved for bonus descriptions, as in the new vertical games; those pictures are not rendered yet. The sky on top was filled by simple extrapolation.

The notes call it accepted: "Igor's 20% vertical stretch is acceptable; conversion target is Nova vertical" [[raw/Meeting_Notes_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]].

## What Val decided

- **Target is NOVA, not RAGE.** Igor asked which; Val: "На новый." [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- **Which games.** "Мы берем текст игры, которые сейчас на рейч они горизонтальные… Пользуясь вашим подходом… Перевозим их на нова вертикальные." ("текст" = Texas, by context.) [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- **Nothing else changes.** Irina: "Мы ж не меняем функционал." Val: "Мы ничего не меняем, ни математику, ни функционал… Мы только переводим с горизонтальным на вертикальную в тупую слепую." [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- **Igor does the first game.** Val first wanted [[wiki/people/sergey-kleimenychev.md|Sergey Kleimenychev]] to convert the Texas games with this method, "с минимальным участием метельского", and to measure the time. Pavel: Sergey should only prepare video; he needs training, and his working time is limited. Pavel and Irina: if Igor does the first game he can fix the game code himself; otherwise work goes back and forth ("перебрасывание"). Val: "Да я Я согласен с вами да?" [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- **The first game is Dutch Mill.** Pavel asked Igor which game he liked; Igor: Dutch Mill has bonuses, good. Pavel: "Давайте дачу ему. И на ней попробуем экспериментировать." [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- **Keep it inside the group.** "Это мы все держим конфиденцию, чтобы это не разошлось по компании, чтобы не было никаких испугов. И никаких комментариев." [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]

## The art step — a looping video from a static topper

Dakota games have new resources and an empty sky area, so Igor says they can go vertical. Some older games (transcribed "над" — **unclear** what this names) have old static toppers with no video. Dutch Mill is one: it is not in the Dakota product, so it has no animated topper. Val: ask Claude or ChatGPT to make a video from the static picture. Pavel: it must loop — "1 кадр должен с последним совпадать" — about 10 seconds. The "Dragon Pays" title should be its own video, not baked into the topper. Igor can add a "liquid glass" reel frame; Pavel: plain video first. For Dutch Mill, Pavel's brief: take the static picture "с барышней" and ask the AI to add movement — blink, move the hands [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]].

Pavel first proposed giving the video work to [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] ("Лескевич") with Sergey; Val turned it toward Sergey [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]. More on the art method: [[wiki/topics/game-art-animation-production-pipeline.md]].

## The port starts with the maths

Igor: LGS has no mystery-progressive support. He added it on his own machine only, to run the game; it is not production code, and LGS "это не мой проект" — he does not want to commit to it. The port "должна начинаться с математики". Pavel will check with [[wiki/people/efim-podvoiski.md|Efim]] how to build the container with the Texas maths (see [[wiki/decisions/2026-08-18-nova-math-container-per-game-set.md]]). Igor added that when he asked for the Dakota Dragon Pays maths to be added ("котовский дроган пэйс"), it was done the same day by evening — the person is "его", read as Efim by context. Free-spin and bonus videos are also needed (Dutch Mill, Clover Fortune and others). The game selection screen is left for later; Pavel: Daniil already did some work on one for Calle Ocho [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]].

## How long — the estimate Val did not accept

Igor: about two weeks for one game with the port and its tests ("недели 2"), because hardware testing is not finished; if the tests were ready, about a week "с текущими темпами". Val accepted that waiting for resources and finishing the tests take time, but: "Но если и то и то готово. То сама работа… Ну помоему это ни неделю нет." Pavel: "Ну мы мы для этого и хотим сделать замер." [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]

**The calendar Val set:** Sergey gets his task on Friday (Oct 9) and should have one video by Monday; Pavel tells Val on Monday the 12th whether graphics came; Igor finishes testing and reports at a meeting on Thursday the 15th; then the Dutch Mill port, which Val expects ready "Понедельник, 19 число" [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]].

## Relation to earlier rulings

- **Supersedes the Sept-14 route.** [[wiki/decisions/2026-09-14-vertical-texas-starts-from-the-georgia-coam-vertical-games.md]] took the vertical Georgia COAM games as the starting material and ruled out converting the horizontal Texas games with the current art; it also had the maths redone. Oct 8 converts the horizontal Texas games themselves and keeps their maths. Later ruling, same subject — evolution; the Sept-14 page is marked superseded.
- **Follows Sept 17.** [[wiki/decisions/2026-09-17-no-more-games-on-rage-and-texas-is-built-on-nova.md]] put Texas on NOVA; Oct 8 is consistent and answers its open question about the conversion work in flight.
- **Closes the Oct-5/Oct-8 experiment.** [[wiki/decisions/2026-10-05-horizontal-to-vertical-conversion-runs-in-parallel-with-the-port-autotests.md]] — Igor's retry is the method used here.
- **Uses the Sept-17 hire.** [[wiki/decisions/2026-09-17-kleimenychev-is-hired-from-monday-onto-texas-and-class-a-in-full-secrecy.md]] — the secrecy rule is repeated here.

## Open commitments

- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — prepare the technical task for Sergey Kleimenychev (resources, sizes, steps) — due Fri Oct 9 2026 (Sergey gets the work Friday) — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — send the needed resources or links, and a list of games with their bonuses and videos — due unspecified — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- [ ] [[wiki/people/sergey-kleimenychev.md|Sergey Kleimenychev]] — make a looping video from a static topper (Dutch Mill first), about 10 seconds — due Mon Oct 12 2026 (not present; assigned in the meeting) — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — tell Val whether graphics for any Texas game came from Sergey — due Mon Oct 12 2026 — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — check with Efim how to build the container that supports the Texas maths — due unspecified — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — finish the testing work and report its status — due Thu Oct 15 2026 meeting — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]

## Open questions

- How does LGS get mystery-progressive support for the Texas games, when Igor will not commit to that project? — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- Can the older games with static toppers (Igor's "над") go vertical as easily as the Dakota games, once AI videos replace the static pictures? — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]

**§15.8:** Pavel's statement of how many hours a day Sergey works is engagement detail and is not recorded. No pay or rate appears. **§15 #9:** none.

## Update, Oct 15 2026 — one Jira feature per converted game; a second converter; Dragon Pays serves both layouts

At the [[wiki/meetings/2026-10-15-daily-standup-offline-ris-fallback-and-nova-game-conversion.md|Oct-15 Minsk stand-up]] (Russian; Val absent) [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]:

- **A second person converts.** [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] used Igor's tools to start on Clover Fortune (the notes' name [[raw/Meeting_Notes_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]); horizontal first, then vertical, by the end of the week. This is the RK3576 game-library work Pavel set on Oct 14 ([[wiki/topics/nova-platform-architecture.md]], Oct 15), not the Texas list — the link to this page is the method and the Jira rule below.
- **Tracking rule (Pavel).** Each conversion gets its own feature under capability 240 ("рейчту новым migration" as heard), like the Dragon Pays conversion, so the AI PM can follow it. The notes list it as Pavel's decision: "NOVA conversions: one feature per game under capability 240" [[raw/Meeting_Notes_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]].
- **Both layouts in one game.** [[wiki/people/igor-metelski.md|Igor]]: Dragon Pays picks vertical or horizontal resources by the cabinet type passed in the URL. Its vertical is probably not merged into main yet.
- **"над" again.** Igor called the games the designers are now drawing "текущий над 2", not Dakota. What "над" names is still **unclear**; see the open question above on the older games.
- **Not reported here:** the Dutch Mill port or Igor's testing status (due "Thu Oct 15" per the commitment above). The stand-up is not that meeting; status unknown.

## Update, Oct 16 2026 — the vertical Dutch Mill has all its scenes; Efim's maths container; the background video is stuck on a blocked account

At the [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct-16 Minsk stand-up]] (Russian; Val absent) [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]:

- **Dutch Mill.** [[wiki/people/igor-metelski.md|Igor]] continues the vertical version: "в принципе, у меня как бы всё готово… все сцены игры созданы по большому счёту". He asked whether to call and agree on the next steps. [[wiki/people/efim-podvoiski.md|Efim]] packed the Dutch Mill maths in a container for the OMNI format ("для о мни короче формата"); Igor asked him for one game only and has not yet looked at what is inside; he expects to run that server locally. Nothing else blocks him: "У нас ничего больше не сдерживает. Ну у меня всё есть, я всё сделал."
- **The topper video.** Pavel: what holds things back is the background videos asked of [[wiki/people/sergey-kleimenychev.md|Sergey Kleimenychev]]; his account on the video-generation tools is blocked, and "Андрей" looked into accounts the day before (Bosik, by context — **inference**). Igor tried free video tools and found them limited; he made generated art with programmatic animation instead and offered to show it. Pavel: in parallel, write a request for the video needed and try from the static start screen.
- **A meeting with Val.** Igor: "надо нам с валом собираться типа"; Pavel: "Похорошему надо, я думаю". No date was set.

On the commitments above: the Dutch Mill port (due Oct 19) is near done but not reported finished; Sergey's looping video (due Oct 12) is not delivered — his account is blocked; Pavel's check with Efim about the Texas-maths container now has a Dutch Mill container from Efim — whether that settles it is not said. All stay open.

### Open commitments (Oct 16 2026)

- (discharged Oct 18 2026 — moved to History below)

## Update, Oct 18 2026 — the vertical Dutch Mill is shown on RAGE; the NOVA move is reviewed Wednesday; Igor's estimate is about 15 hours a game

At the [[wiki/meetings/2026-10-18-dutch-mill-rage-to-nova-conversion-and-reskin-plan.md|Oct-18 8:04 AM session]] (Russian) — the meeting with Val asked for on Oct 16 — [[wiki/people/igor-metelski.md|Igor]] showed the vertical Dutch Mill: base game, its own bonus and the product's shared bonus, with sky, mill, girl and background animated, 4 redrawn and animated symbols and a new help screen, made in one week. It runs on RAGE; the NOVA move has not started. Val: RAGE is finished; the first NOVA iteration is reviewed on Wednesday (the notes: Oct 21). Igor's estimate for the move: "не дольше, чем в 15:00" per game with tests (read as 15 hours — **inference**). Full record and the new commitments: [[wiki/decisions/2026-10-18-rage-is-closed-dutch-mill-reaches-nova-by-wednesday-and-a-reskin-from-a-new-theme-tests-the-tools.md]] [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].

Earlier the same morning, on the [[wiki/meetings/2026-10-18-flex-port-sas-igt-lock-and-emulator-requirements.md|7:00 AM call]], Pavel told Val the resources exist: Igor works on moving games to NOVA, and [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] took a game ("из сауз дакоты по моему") to turn from horizontal to vertical with Igor's scripts and has done something in a couple of days, not yet shown. The bottleneck is designers to regenerate video. Sergey Kleimenychev has delivered nothing yet; his OpenRouter AI access did not work and "Андрей" fixed it on Thursday; Pavel will check on Monday [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]. At 8:04 Igor said Sergey's access "настроили сегодня" and that Sergey is sending new videos for the bonus [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]].

On the commitments above: Igor's Oct-16 item (show the generated art; meet Val) is discharged — moved to History. The Dutch Mill port (due Oct 19) is re-aimed at the Oct-21 review of a first NOVA iteration; it stays open. Sergey's looping video (due Oct 12) is still not delivered as such; his access now works and new bonus videos are coming; it stays open. On the estimate question: Igor now says about 15 hours per game for the move, and about three days for Dutch Mill himself with Claude — still an estimate, not the measurement; the question stays open.

## Update, Oct 21 2026 — Dutch Mill runs on vertical NOVA; the measurement

At the [[wiki/meetings/2026-10-21-dutch-mill-on-nova-and-native-engine.md|Oct-21 review]] (Russian) [[wiki/people/igor-metelski.md|Igor]] showed the vertical Dutch Mill on NOVA with all bonuses working, a test harness and a test scenario, and acceptance criteria and requirements linked to a capability (still a local draft). His measurement: about one session for the port (garbled in the transcript; about six hours per the Oct-20 stand-up), a parallel test session of about the same time, and a couple of hours to fix the defects he saw. He also built a vertical Midnight Money from its theme, on RAGE so far [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]. Full record: [[wiki/decisions/2026-10-18-rage-is-closed-dutch-mill-reaches-nova-by-wednesday-and-a-reskin-from-a-new-theme-tests-the-tools.md]] (Oct-21 update). The same meeting decided to drop the browser under NOVA and set MVP1 as six Texas games on a stable NOVA — [[wiki/decisions/2026-10-21-nova-drops-the-browser-for-a-native-engine-no-code-before-capabilities-and-mvp1-is-a-stable-nova-releasing-six-texas-games.md]].

On the commitments and questions above: the Dutch Mill port is done (two days after Val's Oct-19 target) — moved to History. The "how long does a port take" question is answered by that measurement — moved to History.

## Note, Nov 12 2026 — Val wants Metelski's horizontal-to-vertical conversion for the Texas V43 line running in GitHub with CI/CD; he calls it "рейч горизонтальная на рейч вертикальный" and is "не уверен" Rage is left behind; who writes the CI/CD is open

At the end of the [[wiki/meetings/2026-11-12-flex-recycler-slim-mvp1-by-thursday-and-20-dollar-promo-bonus.md|Nov-12 6:53 AM recycler meeting]] (Russian; Igor absent) [[wiki/people/val-levitan.md|Val]], "хотя это не является частью этого митинга": he wants [[wiki/people/igor-metelski.md|Igor Metelski]]'s program "которая переводит. Рейч горизонтальная на рейч вертикальный. Чтоб уже это бежало в гидхабе" — "вся эта линия то, что вот будем выпускаться в 43 для Техаса"; Igor had told him "день 2 работы" [[raw/Meeting_Transcript_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]]. [[wiki/people/pavel.md|Pavel]]: the actions to build everything must be redone too, and "Тут вся сиди будет в разы дольше, чем чем сами игры перенести, потому что они тянут за собой там и прогрессивы, и хал, и сборку i so"; Val: "давайте мы сразу это сделаем… Потому что я не знаю, сколько будет длиться этот рейч Техас в рейдж… я ещё не не уверен, что мы от него от рейч отошли и забыли", and later "я не сказал, давайте останемся с речи" [[raw/Meeting_Transcript_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]]. Val's plan: Igor creates the working environment in GitHub and writes the actions, "И естественно, Андрей босик создал CICD pasvay. На Техас вифори фри [V43] вот эти игры"; Pavel: "Может быть Алексей хамин?" — the old CI/CD "был на сервере в виде скриптов", now to be committed, modified, into the Rage game projects, plus "отдельно интеграционную репозитории" [[raw/Meeting_Transcript_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]]. Val did not choose between them [[raw/Meeting_Notes_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]].

**Tension flagged, not resolved.** This page (Oct 8) has the Texas games going to **vertical NOVA**, and Rage was declared finished on Oct 18 and Nov 6; on Nov 12 Val speaks of Rage-vertical games for the Texas V43 line and is not sure Rage is left behind. It is not a new ruling — he says he did not say to stay with Rage — so it is recorded here as an open question, not a contradiction (**inference**) [[raw/Meeting_Transcript_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]].

### Open commitments (Nov 12 2026)

- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — set up the build environment and actions in GitHub for the Texas V43 conversion — due unspecified (Igor's own estimate to Val: about two days) — [[raw/Meeting_Transcript_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]] [[raw/Meeting_Notes_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] (Val) or [[wiki/people/alexei-khamin.md|Alexei Khamin]] (Pavel's suggestion) — the CI/CD pipeline for the Texas V43 games — due unspecified — [[raw/Meeting_Transcript_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]] [[raw/Meeting_Notes_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]]

### Open questions (Nov 12 2026)

- Do the Texas V43 games ship on Rage (converted to vertical) or on NOVA, as ruled on Oct 8? Val on Nov 12: "я ещё не не уверен, что мы от него от рейч отошли" — [[raw/Meeting_Transcript_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]] — *Nov 13: the stand-up worked on the Rage variant (see the note below); no ruling by Val.*

## Note, Nov 13 2026 (6:16 AM) — six Texas games already converted to vertical on Rage as a first version, with AI art nobody approved; nothing goes out; the needed parts are planned onto GitHub, then a CI/CD integration repository that builds a Rage ISO

At the [[wiki/meetings/2026-11-13-daily-standup-vertical-rage-games-for-texas-and-agent-date-moves.md|Nov-13 Minsk stand-up]] (Russian; Val absent) [[raw/Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]]:

- **The question.** [[wiki/people/pavel.md|Pavel]]: "вал вчера говорил по поводу над… Вертикальных с горизонтальных на вертикальную машину. Что это всё ещё актуально в варианте рейдж?" [[raw/Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]]
- **Why.** Pavel: horizontal machines came in from somewhere ("горизонтальные ей откудато пришли"); for the Texas market a vertical machine would be more useful, and the idea is that "если быстренько переделать эту машину на вертикальную и поставить туда правильный софт. У нас будет готовый продукт для Техаса" [[raw/Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]].
- **Which games.** [[wiki/people/igor-metelski.md|Igor]] first spoke of the few games that never had a vertical version, then asked "или ты имеешь в виду 1 над?"; Pavel: "Наверно 1 над"; [[wiki/people/irina-shishko.md|Irina]]: "Наверное, игры, которые были в Техасе их сделать вертикальными"; Igor: "Вот эти вот 6 игр, которые я сделал." What "1 над" names is kept as heard (the notes: "the Texas games, NAD 1") [[raw/Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]].
- **Their state.** Igor: "они в каком то виде есть, но это же это это не генерированный арт, который как бы ни с кем не согласован, это надо показывать кому то"; "я думал это всё эксперимент. Я не думал, что мы хотим это ну типа в продакшн куда то пускать." Pavel noted for himself that "какаято 1 версия переконвертированной рейд игры из горизонтальной вертикально готова 6 игр", and further steps need a go-ahead. They live on Igor's experiment branch: "у меня есть ветка один 27… эта ветка находится фактически в актуальном состоянии" [[raw/Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]].
- **Creative briefs.** For games that never had a vertical version, the layout of the top half is a design question: "например, там какойнибудь джеманте, вот у нас вообще никогда не было вертикальной версии"; "мы переносим это в таком же виде как есть или нам надо придумать как организовать вот эту вот верхнюю половину экрана" — "нужны вот эти вот креатив, ну типа брифы креативные". Doing it on Rage "совсем не проблема будет" [[raw/Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]].
- **Nothing goes out; GitHub first.** Irina: "там ещё речь шла о том, чтобы это всё в гид перенести"; Pavel: "Да и сборку всю." Igor said he could technically build a Windows build and give the games to Michael or anyone, to learn whether the AI art ("нейрорт") is acceptable; Irina: "Пока мы ничего никому не отдаём" [[raw/Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]].
- **Pavel's plan.** "можно из этих задач будет запланировать. Перенос необходимых компонентов на гид"; next "сделать CICD, то есть какоето интеграционный репозиторий для сборки именно рейдж игр", which pulls sources from other repositories, or, if each component is released separately, takes their artifacts, and builds an ISO ("сошку", heard) "как мы собирали для рэйдшi". Igor already builds locally in containers. Igor and Pavel would talk after the meeting [[raw/Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]].

This is the stand-up acting on Val's Nov-12 wish (the note above), on the Rage side. It is a working plan, not a new ruling by Val; the Rage-or-NOVA question stays open (**inference**). At the 7:01 AM NOVA-2 follow-up the same morning the art question came up again for NOVA — [[wiki/decisions/2026-11-13-nova-is-done-only-when-a-ci-built-image-from-the-production-server-runs-on-a-machine-the-first-iso-is-built-tuesday-texas-first-then-georgia-and-the-design-agent-waits.md]].

### Open commitments (Nov 13 2026)

- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] and [[wiki/people/pavel.md|Pavel Frolov]] — plan the tasks to move the needed Rage components to GitHub, then the CI/CD integration repository that builds the Rage ISO; talk after the stand-up — due unspecified (talk Nov 13 2026) — [[raw/Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]]

### Open questions (Nov 13 2026)

- How should the top half of the screen look for games that never had a vertical version — moved as is, or newly designed? Igor needs creative briefs — [[raw/Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]]
- Is Igor's AI-generated art for the six vertical games acceptable? Nobody has approved it — [[raw/Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]]

## History

- [x] [[wiki/people/igor-metelski.md|Igor Metelski]] — port Dutch Mill to vertical NOVA — due Mon Oct 19 2026 (Val's target) — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]] — **discharged Oct 21 2026**: shown running on NOVA with tests [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- Answered question: how long does one port really take once tests and resources are ready? — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]] — **answered Oct 21 2026**: about one session for the port plus a parallel test session and a couple of hours of fixes [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]

- [x] [[wiki/people/igor-metelski.md|Igor Metelski]] — show Pavel the generated art with programmatic animation; set up a meeting with Val on the next steps — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] — **discharged Oct 18 2026**: the meeting with Val took place and Igor showed the art [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]

## Sources
- [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- [[raw/Meeting_Notes_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Transcript_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- [[raw/Meeting_Notes_Dutch_Mill_Rage_to_NOVA_Conversion_and_Reskin_Plan-October-18-2026.md]]
- [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]
- [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- [[raw/Meeting_Transcript_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]]
- [[raw/Meeting_Notes_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026.md]]
