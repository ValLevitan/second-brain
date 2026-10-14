---
type: decision
title: Cover the code with tests first — the next CI steps (runs on real hardware by IP address, and hooking the test system into the product repositories) wait
date: 2026-10-07
aliases: [test coverage first, покрытие сделать тестами в первую очередь, CI hardware runs wait, прогоны с железом, product repository hookup waits, подключение этой системы на других репозиториях, Khamin moves to writing tests, behind on test count, отстаём]
source-count: 3
status: active
open-commitments: 1
open-questions: 1
---

# Cover the code with tests first; the CI hardware runs and the product-repo hookup wait (Oct 7 2026)

Ruled by [[wiki/people/pavel.md|Pavel Frolov]], with [[wiki/people/irina-shishko.md|Irina Shishko]] agreeing, at the [[wiki/meetings/2026-10-07-daily-standup-test-coverage-first-and-ai-task-numbers.md|Oct-7 Minsk stand-up]] (Russian), on a question from [[wiki/people/alexei-khamin.md|Alexei Khamin]]. The wider testing picture is on [[wiki/topics/test-automation-strategy.md]].

## What was asked

Khamin reported the repository rules done ("С правилами в общем, репозитории закончил в целом") and prose "90 плюс точно процентов". The CI work is at the report stage ("на стадии… формирование отчётов"). He then asked about the next two steps [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]:

- **Runs on real hardware.** Since not all emulators exist yet, the system would be set up "чтобы мы могли вводить там айпишники для железа" — enter hardware IP addresses so it runs the tests on devices.
- **Hooking it into the products.** "отдельный шаг это подключение этой системы… на других репозиториях на продуктах уже. Чтобы… в продукт запускались тест."
- "Это вот мы сейчас будем делать или это отложить?"

## The ruling

Pavel: "Ну сейчас это, наверное, не стоит, но вообще… правильно говоришь, но лучше сейчас покрытие сделать тестами в первую очередь." Irina: "Да нужно это самое подтянуть… Отстаём всётаки както за счёт Того, что ты сейчас этим занимаешься. То есть ты как человекодень полностью выпал, а как Клода день вообще от тебя много выпало. Из количества тестов" — the team is behind on test count because Khamin (and his Claude time) went to this work. Khamin: "Да, тогда завершаешь с тем, чтобы можно было запускать руками… и к тестам тогда перехожу. Написание." Pavel: "Хорошо" [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]].

In one line: **finish what is needed to run the tests by hand, then write tests; the hardware runs and the product-repository hookup are later work.** Pavel called the idea itself right ("правильно говоришь"), so it is deferred, not rejected.

The derived notes record the same ruling, decided by Pavel and Irina [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]].

## How this sits against earlier items

- On Oct 5 Khamin said he would start writing tests "с 7 числа" (from the 7th) — see [[wiki/topics/test-automation-strategy.md]] (Oct 5). On Oct 7 he had not yet started; this ruling moves him there after the manual-run step (**evolution**).
- The prose figure continues the Oct-6 "46% → 87%" on [[wiki/decisions/2026-09-04-data-contracts-closed-every-repository-by-september-11.md]].

## Open commitments

- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — finish the manual-run step, then move to writing tests — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]

## Open questions

- When do the CI hardware runs and the product-repository hookup start? Not set — [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]

**§15.8:** clear — work priorities only. **§15 #9:** none.

## Update, Oct 12 2026 — Khamin is bringing the tests up on pull requests and on real hardware; the port route is set

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 Minsk stand-up]] (Russian) [[wiki/people/alexei-khamin.md|Khamin]]: "оживляю тесты, чтобы они прогонялись на. При создании пиар и на. При запуске на железы на реальном"; "Что то они пока все дохлые"; two sets now pass on pull requests. He will add a rule so the needed CI parameters are written at once [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]. For the Flexport the route is now fixed — CI on real ports through the internal runner: [[wiki/decisions/2026-10-12-flexport-ci-tests-run-on-real-ports-through-the-internal-runner-and-no-port-emulator-is-built-for-now.md]]. This takes up the step deferred above (**evolution**). The open question below is partly answered: the hardware runs are under way for the port; the product-repository hookup is not mentioned.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
