---
type: decision
title: Transactional MVP 1 counts as released only when the end-to-end tests on the acceptance criteria pass — no separate product-team test pass now; field and beta tests come after
date: 2026-10-14
aliases: [MVP1 released only after end-to-end tests, end-to-end tests on acceptance criteria, end-to-end тесты согласно acceptance criteria, только после этого можно считать продукт выпущенным, no product-team test pass, waste of time, field tests after end-to-end, user experience is minutes not days]
source-count: 4
status: active
open-commitments: 0
open-questions: 0
---

# Transactional MVP 1 counts as released only when the end-to-end acceptance tests pass

Ruled by [[wiki/people/val-levitan.md|Val]] at the [[wiki/meetings/2026-10-14-transactional-mvp1-launch-plan-brackets-daily-caps-and-mvp2-scope.md|Oct-14 3:49 PM launch-plan meeting]] (Russian) with [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].

## What Klimovich proposed

- The product team should test MVP 1 on Flex IQ by hand — not deep edge-case testing, but "пройтись по всем прямым кейсам, по основным" [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].
- His estimate: nine areas of function, about ten tests each, about ten minutes a test — "мне надо день - полтора на тест с IQ". The result would be a list of bugs and improvements [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].
- The developers were still shipping: "Сегодня, например, за день у нас было накатано три обновления, три новые сборки" [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].

## What Val ruled

- **Not now.** "Я думаю, что не на этом уровне. Потому что сейчас это будет waste of time." [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- **The release test.** "Нам нужно пройти end - to - end тесты согласно acceptance criteria, которые есть в requirements. Только после этого можно считать продукт выпущенным." [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- **Then the human tests.** Field tests or "бета-имплементаций-тесты" can start only after the end-to-end tests pass [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].
- **User experience is quick and subjective.** "Буквально нужно час, чтобы проочувствовать user experience"; "я вижу минуты, часы, не неделя, не дни". Later some of it can become numbers in requirements — his example, "touch to action time должен быть не больше чем там, например, 50 миллисекунд" — "но не сейчас" [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].
- **No locations before that, in the ideal case.** "пока нет несделанных end-to-end тестов на acceptance criteria… ставить на локейшены быть не может" (garbled; read as: while end-to-end tests are not done, nothing goes to locations) [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].

The derived notes record it as a decision: "MVP1 is released only when the end-to-end tests on acceptance criteria pass; no separate product-team test pass now." [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]

## The date Val half-remembered

Val had seen "девятого ноября" that morning at five as the end date, but "я у них не спрашивал… поэтому я могу быть не прав"; later: "сегодня это индекей где-то на девятом ноября" [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]. The same morning the Minsk stand-up moved an MVP 1 to about November 8 or 9; the owner ruled on Oct 15 that this was the RIS improvement MVP 1, not the transactional one — [[wiki/decisions/2026-10-14-mvp1-is-extended-to-about-november-8-or-9-and-the-mvp2-marked-tasks-are-done-inside-it.md]]. **Owner ruling 2026-10-18:** the "November 9" Val half-remembered here is the **RIS MVP 1** date, not a transactional date. No transactional release date was set in this meeting.

## Where it sits

- It sharpens the release meaning of the October-15 date on [[wiki/decisions/2026-09-28-october-15-replaces-october-1-as-the-mvp1-date.md]] (Oct-14 3:49 PM update): the release is a test result, not a calendar day.
- The first-location date of November 1 was held in the same meeting — [[wiki/decisions/2026-10-14-the-first-ten-transactional-locations-go-in-from-november-1-on-stock-monitors-ports-without-wi-fi-and-hand-made-harnesses.md]]. How the two fit (Nov 1 installs against a possible Nov 9 end of tests) was not settled in words. *(Inference: Val's "в идеале" may mean the rule bends for the first locations.)*
- It follows the e2e-test line of [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]].

## Update, Oct 15 2026 — the end-to-end autotests finish "tomorrow"; the one gap is the Flex-Port USB-stick update

At the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian) [[wiki/people/irina-shishko.md|Irina]] reported the autotests for Flex IQ, the port, the machine and card issue: "мы закончим завтра писать"; they are run all the time as they are written. Val checked: autotests "на базе [acceptance criteria]", end-to-end — Irina and Pavel: "Да." Val: "если протестировано. Значит можно выпускать." Irina: "У нас апдейта нет" — the Flex-Port update. Val's recap: the autotests are done and run, the bugs found are fixed (Irina: "в общемто да можно сказать так"); this covers the capabilities planned for MVP 1 except the USB-stick update for the Flexports, which should take "от трёх до 5 дней" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. The count Irina gave first ("3 из 70… фичи не тронута") is garbled and not used. Detail of the USB gap: [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-15 11:04 AM update) [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

**On the open question below:** answered — not about November 9; the end-to-end tests on the acceptance criteria were due to finish on Oct 16, and release then waits only on the USB-stick update (about 3 to 5 days, Val's estimate). Andrei Klimovich had asked Val for the release date the day before; Pavel and Irina are to tell him — see [[wiki/decisions/2026-10-15-mvp2-is-flex-iq-wi-fi-remote-update-diagnostics-and-galaxy-reporting-and-flex-pay-moves-to-mvp3.md]].

## Open questions

- ~~When do the end-to-end tests on the acceptance criteria finish — about November 9, as Val half-remembered?~~ **Answered Oct 15 2026:** writing finishes Oct 16; the only gap is the Flex-Port USB-stick update, about 3 to 5 days — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] — — [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
