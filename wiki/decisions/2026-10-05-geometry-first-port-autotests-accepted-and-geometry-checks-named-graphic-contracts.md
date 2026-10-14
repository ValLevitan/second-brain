---
type: decision
title: Geometry-first autotests for the Dragon Pays port are accepted for same-format ports, and the geometry checks will be called "graphic contracts" (Oct 5 2026)
date: 2026-10-05
aliases: [geometry-first port tests, geometry and timing tests, геометрия и тайминги, port autotests Dragon Pays, Test 360 vs new approach, mutation testing, мутационное тестирование, мутейшн джиэс, transition test, free-spins transition defect, lantern transition, epic big win with transition out, graphic contracts, графические контракты, никаких замечаний у меня нету]
source-count: 2
status: active
open-commitments: 1
open-questions: 3
---

# Geometry-first autotests for the Dragon Pays port are accepted, and geometry checks become "graphic contracts"

Set at the [[wiki/meetings/2026-10-05-rage-nova-port-autotests-and-horizontal-to-vertical-layout.md|Oct 5 2026, 7:01 AM review]] (Russian), chaired by [[wiki/people/val-levitan.md|Val Levitan]], after [[wiki/people/igor-metelski.md|Igor Metelski]] showed how he tests the Rage-to-NOVA port of Dragon Pays. It continues the QA experiment set on [[wiki/decisions/2026-08-28-reverse-engineer-acceptance-criteria-and-automate-qa-dragon-pays.md|Aug 28]] [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## What Igor built

- **The test game.** Dragon Pays from the South Dakota product. In Rage it is horizontal; his NOVA port is horizontal too, with "4 фулл эйч ди экрана" (a main screen, an extra screen, the topper, and a fourth the transcript garbles as "видек") [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **Measured geometry.** He took the position and size of elements on the original Rage game's screens: base game and free spins, overlays such as anticipation and recognition, the win meter, balance meter, current bet, buttons, and the upper screen with the pay table. He skipped the topper, because it "практически всегда занимает, какоето видео" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **Measured timings.** How alpha and content change in transition animations, and reel spins with anticipation and recognition animations [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **Two formats of the same documents.** "MD для Клода httm для человека" — Markdown for Claude, HTML for a person. He shared them in the chat in Russian and English [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **Geometry defined.** Pavel asked what "geometry" means. Igor: "Это взаимное расположение и размеры элементов экрана" — the relative position and size of screen elements. Irina added that Igor ports from D27 to D27, so the port must look the same as the original [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

## How the tests run

1. **Geometry first.** Scripts check that each element sits in its expected area of the screen. This matters for a correct port, and later tests need to know which screen area holds which value [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
2. **Then game scenarios.** Credit is added to the balance and spins are made. During a spin the tests check that buttons such as play are disabled. After the reels stop they check the balance, the current win, the tickers and the highlighting of the pay lines [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

**How it differs from Test 360.** Test 360 knew the scene's internal names and looked elements up by name. The new tests look at the screen areas where elements must be — "тестовый сценарий видят то, что видят, видят человек" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]. Pavel did not see the difference at first; Irina explained it: Test 360 used element names "неважно, где они там бы отображались", while Igor first checks that everything is in place and then that it works [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

**Not covered yet.** Many criteria are still open, because some cannot be tested yet: moving between games, and sound, "подхода к которому у нас как бы пока нету" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

## The transition test that does not catch the defect

- **The defect.** In the free-spins transition the screen darkens, a hanging object appears (Irina: "фонарик", a lantern), and it should burn away upward while the background alpha fades in step. In the port "альфаканал уходит быстрее, чем анимация". Igor sees it by eye; the tests do not [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **His plan: mutation testing.** Put known defects into the code or the data on purpose and check that the tests find them — so the tests do not just give "зелёные галочки" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **Not yet checked.** He started on the transition "вчера". Claude "утверждает, что он его реализовал" and has a script ("мутейшн джиэс"). Val asked how he knows; Igor will give the script to an independent Claude session and ask what it does [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **One real port defect was caught.** An "эпик бигвин" animation started at the same time as the transition out of the bonus. The test saw an extra animation, and Claude asked whether it was planned or a port defect [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

## What Val ruled

- **Approved for same-format ports.** "Замечательно, никаких замечаний у меня нету… я очень рад." Later: "С горизонтальной на горизонтального с вертикальной вертикального. У меня вопросов по этому поводу нету." [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- **Why he likes it.** It moves away from building screens and timings "Глазом художника" toward a mathematical description; "Я считаю, что это очень правильный подход." Igor recalled Val's old complaint about elements moved "на пару пикселей туда сюда" and constant re-exports [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **The name "graphic contracts".** Pavel said geometry must also be checked for new games, not only ports. Igor: a game-creation project would check that the game meets the geometry requirements. Evgeny: "типа контрактов графических, так называемых". Val: "Но они так и будут называться графические контракты." [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- Horizontal-to-vertical was **not** settled here — see [[wiki/decisions/2026-10-05-horizontal-to-vertical-conversion-runs-in-parallel-with-the-port-autotests.md]].

## Open commitments

- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — continue the Dragon Pays port autotests, get a test that catches the wrong free-spins transition, and check what Claude's mutation script really does — due Thu Oct 8 2026 review — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]] [[raw/Meeting_Notes_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]

## Open questions

- Does Claude's mutation script work? Igor has not checked it — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- How will moving between games and sound be tested? No approach yet — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- Should the geometry check also run in the NOVA integration repository before release? Igor: it can stay out ("проверку диаметрии в интеграционной репозитории можно не тащить"); Pavel: "я наверное не соглашусь" — geometry must be checked when games are released — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
