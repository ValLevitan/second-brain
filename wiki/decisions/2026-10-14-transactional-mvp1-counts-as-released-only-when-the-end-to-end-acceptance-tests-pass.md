---
type: decision
title: Transactional MVP 1 counts as released only when the end-to-end tests on the acceptance criteria pass — no separate product-team test pass now; field and beta tests come after
date: 2026-10-14
aliases: [MVP1 released only after end-to-end tests, end-to-end tests on acceptance criteria, end-to-end тесты согласно acceptance criteria, только после этого можно считать продукт выпущенным, no product-team test pass, waste of time, field tests after end-to-end, user experience is minutes not days]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
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

Val had seen "девятого ноября" that morning at five as the end date, but "я у них не спрашивал… поэтому я могу быть не прав"; later: "сегодня это индекей где-то на девятом ноября" [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]. The same morning the Minsk stand-up moved an MVP 1 to about November 8 or 9; the owner ruled on Oct 15 that this was the RIS improvement MVP 1, not the transactional one — [[wiki/decisions/2026-10-14-mvp1-is-extended-to-about-november-8-or-9-and-the-mvp2-marked-tasks-are-done-inside-it.md]]. Whether Val's "November 9" here is the same date carried over is **unclear**.

## Where it sits

- It sharpens the release meaning of the October-15 date on [[wiki/decisions/2026-09-28-october-15-replaces-october-1-as-the-mvp1-date.md]] (Oct-14 3:49 PM update): the release is a test result, not a calendar day.
- The first-location date of November 1 was held in the same meeting — [[wiki/decisions/2026-10-14-the-first-ten-transactional-locations-go-in-from-november-1-on-stock-monitors-ports-without-wi-fi-and-hand-made-harnesses.md]]. How the two fit (Nov 1 installs against a possible Nov 9 end of tests) was not settled in words. *(Inference: Val's "в идеале" may mean the rule bends for the first locations.)*
- It follows the e2e-test line of [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]].

## Open questions

- When do the end-to-end tests on the acceptance criteria finish — about November 9, as Val half-remembered? — [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
