---
type: decision
title: The horizontal Texas games on RAGE are converted to vertical NOVA games with Igor's 20% method, with no change to maths or function; Igor ports Dutch Mill first and Sergey Kleimenychev only makes the video (Oct 8 2026)
date: 2026-10-08
aliases: [Texas blind conversion, в тупую слепую, Texas Rage to Nova vertical, перевозим их на нова вертикальные, 20 percent stretch, symbols 20% taller than wide, Dutch Mill first port, дач мил, Kleimenychev video only, looping topper video, keep it confidential, держим конфиденцию, Games convert horizontal to vertical, one feature per game under capability 240, рейчту новым migration]
source-count: 6
status: active
open-commitments: 8
open-questions: 3
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
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — port Dutch Mill to vertical NOVA — due Mon Oct 19 2026 (Val's target) — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]

## Open questions

- How does LGS get mystery-progressive support for the Texas games, when Igor will not commit to that project? — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- How long does one port really take once tests and resources are ready — a week (Igor) or less (Val)? The Dutch Mill port is the measurement — [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
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

- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — show Pavel the generated art with programmatic animation; set up a meeting with Val on the next steps — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]

## Sources
- [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- [[raw/Meeting_Notes_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
