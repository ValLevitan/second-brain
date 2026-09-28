---
type: decision
title: Autotest features go inside the existing MVP 1 capabilities, not a separate one — and the first end-to-end test is a one-hour micro-step, run by the next day
date: 2026-09-22
aliases: [autotests inside existing capabilities, E2E micro-step, one-hour test, микрошаг, first end-to-end test, Flex-Port connection test, cable in cable out test, telnet hook, capability 173 test, test your own ecosystem first, the Texas two-machine case, developers help write E2E tests, symlink to dev null, four manual tests]
source-count: 4
status: active
open-commitments: 4
open-questions: 2
---

# Autotests go inside the existing capabilities, and the first E2E test is a one-hour micro-step

Settled at the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept 22 2026 8:01 AM MVP 1 call]] (Russian). [[wiki/people/val-levitan.md|Val]] asked for it; [[wiki/people/pavel.md|Pavel Frolov]] shaped it; everyone agreed [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

## What forced it

No end-to-end tests exist for MVP 1. [[wiki/people/irina-shishko.md|Irina Shishko]]: "Нет, потому что их ещё не писали", and "Этим пока у нас никто не занимался". She also said the team would release "независимо от того, будут тесты написаны или нет", and called that "неправильно в этом релизе". Val's answer: the only way to release on the 2nd "это если девелоперы помогут написать [энд-ту-энд] тесты или хотя бы… курировать" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]. The debate that led here is on [[wiki/topics/test-automation-strategy.md]] (Sept 22, 8:01 AM).

## Ruling 1 — autotests live inside the capabilities being built

Irina asked whether the autotest features go into the capabilities developers are working on, or into a separate capability. [[wiki/people/dmitri-chudinov.md|Chudinov]] first said a separate one was better. Pavel: "Я бы встраивал в те, которые есть сейчас, потому что, чтоб мы в дальнейшем не разделяли работу по написанию автотестов от основной работы". Val backed it and allowed for error: "Нету требования такого, чтоб мы в 1 раз сделали правильно" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

[[wiki/people/andrei-klimovich.md|Klimovich]] added a way to start: take a capability whose code is already done and "на ней потренируемся" — make the first batch of autotests there [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

## Ruling 2 — one micro-step by tomorrow

Val: "Я хочу микрошаг до завтра… выберите любой шаг, на который нужно час работы" — create one test, run it, and see the result. His reason: without trying, "у нас постоянно будет эта дилемма", and every release gets taken "штурмом". He asked for hands; Irina: "Согласна" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

**The test chosen.** Chudinov floated a connection test (Flex-Port to machine, or Flex-Port to Flex IQ). Pavel made it concrete: the current Flex-Port firmware already connects to Flex IQ and to the machine over SAS; with the cable in it should report connected, with the cable out not connected; the state "можно прочитать через хук, который сделан через telnet". He expects "Лёша" ([[wiki/people/alexei-khamin.md|Alexei Khamin]]) to write it "за час… или за 2", mostly learning rather than coding. Irina filed it under **capability 173** [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]. *(The derived notes give the test to Pavel alone; the transcript shows Chudinov floated the idea first. They also name the writer "Alexey Khamin"; the recording says only "Лёша" here, and Val names "Алексея Хамина" at the end.)* [[raw/Meeting_Notes_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]

**The check.** Val closed the call: tomorrow check whether at least one E2E flow worked, then plan the schedule for the rest, perhaps with Ivan and Alexei Khamin [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

## The scope Val set: JVL's own ecosystem first

Pavel warned that JVL only tests the Flex-Port with its own machines, and "Как сас работает на чужих машинах? Мы не знаем". Val agreed and ruled on order: "1 проблема это… тестирование с нашим оборудованием"; other machines come later. His example is a live business case — people who want "2 машины с нашим диспенсером… В Техас… всё наше вся экосистема наша" — while saying "Я знаю, что у нас ещё нету диспенсера" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]. The Sept-9 rule to test in borrowed non-JVL machines still stands; see [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] (Sept-22 update).

## Who writes the tests

Pavel would not give up Chudinov or Biratka ("Я диму и сашу на это не отдам"). His list: "у нас есть женя, у нас есть лёша, у нас есть иван, у нас есть ира. Вот эти все люди должны писать… тесты. С помощью клодов." Val asked that at least Ivan and Alexei be put on the schedule for this work: "в скетжуле есть скоп. На него никто сейчас не смотрит, но выпуск от этого зависит" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]. Names are resolved on the meeting stub.

## Update, Sept 23 2026 — what the micro-step produced: eight connection tests, half of them manual

Checked the next morning at the [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept-23 8:00 AM call]], as Val had asked [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

- **Ivan's result.** [[wiki/people/ivan.md|Ivan]] wrote tests for the machine-to-Flex-Port connection: "Пока что 8 тестов, которые проверяют это эти коннекты из этих 8 тестов у нас есть 4, которые надо всё равно делать руками." He found no way to disable the SAS wire in software: "не нашел вариантов, как отключить провод сас с машины или с флекспорта" [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].
- **Val: that cannot be right.** "Невозможно, это неправильно чтото… Значит неправильное… чтото архитектура сделана". His yardstick: leading companies do "все программные разработки хотя бы на 70% через клод"; tests where 50% need human action do not fit [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].
- **Pavel's answer, on the call.** "на машине все порты это символические Ссылки на какоето устройство" — if the test points the link somewhere else, "канал связи пропадёт". Pavel and Bosik: point it at "Деф нул" (/dev/null). Ivan: "Ну значит надо переписывать тест?" [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- **Khamin's test is not finished.** His test credits money to the machine, a chain of terminal, Flex-Port and EGM. Claude offered only manual options, which he refused, and he found no open API. On Chudinov's advice he is building a tool or a stored instruction so Claude "знал, куда лезть и как смотреть", to generate the test itself while checking the balance [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].
- **Verdict.** Irina: the goal was to see if it works; "прогресс есть", done "за пару часов". Pavel: "Цель достигнута в больше побольшому." Val: "я должен с этим согласиться" — but repeated the team-level rule: "Не работайте в вакууме, пожалуйста. Общайтесь друг с другом". Pavel added that bringing every problem to him "тоже не самое хорошее решение"; Val: "Есть еще 20 человек, которые в Минске работают" [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].
- **Next.** Irina will create autotest features under the MVP 1 capabilities; Khamin and Ivan continue, with the FlexPay emulator expected to make it easier ([[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]], Sept-23 8:00 AM update). Tests go in the integration repository (Bosik) [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

*(§15.8: Val's remarks to one named engineer about not asking for help are a personal performance judgement and are not recorded; only the team-level instruction is.)*

## Update, Sept 24 2026 — features nearly all raised, the manual tests fixed, and a test API on the terminal

At the [[wiki/meetings/2026-09-24-transactional-mvp1-flexport-money-loss-bugs-and-release-date.md|Sept-24 8:01 AM call]] (Russian) [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]:

- **Irina's features.** She is creating the autotest features capability by capability — "Сегодня, завтра… я всё закончу" — after which they are planned and taken one by one. There are 24 capabilities, "на каждое по 45 фич" (4–5 or 45 each — **unclear**).
- **Unattended tests need a test API.** [[wiki/people/alexei-khamin.md|Khamin]]: "Нашли мы вариант как автотест вообще без… участия человека могут ходить, для этого нужно… [д]обавить тест [API] на терминал". It is [[wiki/people/dmitri-chudinov.md|Chudinov]]'s task, read out as "Фик фик 56"; Chudinov: "В работе", and "Он будет сегодня сделан" (transcribed as a question). Khamin expects his tooling ready that day and to start filling in tests the next day.
- **Ivan's manual tests are fixed.** [[wiki/people/ivan.md|Ivan]]: "то, что у меня вчера было, что надо было руками это исправлено, то есть нужно было внести камиты в прошивку самого". He checks connections between Flex-Port and machine against a 20-second budget, and next wants to run the negative cases. Whether he used the symlink method is not stated.
- **Val: "это экстрим и импортный для нас… Всем сконцентрироваться на этом. Включая Андрей климович".** His reason: when a device comes back from the field, an end-to-end test could show where the problem most likely sits ("когда приходит девайс fredy field"). Argument and the hook rule on [[wiki/topics/test-automation-strategy.md]] (Sept 24, 8:01 AM).

## Open commitments

- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — write and run the first E2E test: Flex-Port connection state to Flex IQ and to the machine, read through the telnet hook, under capability 173 — due Sept 23 2026 (Val: check it "завтра") — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]] — **Sept 23 2026:** the connection tests came from Ivan (8, half manual); Khamin's own money-crediting test is not finished — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — create the autotest features under the existing capabilities and plan them — due Sept 22 2026 ("Давайте сегодня я сделаю фичи") — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]] — **Sept 23 2026:** restated, still to do ("я создам фичи под этими") — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]] — **Sept 24 2026:** in progress; she expects to finish all capabilities that day or the next — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] — put Ivan and Alexei Khamin on the test work in the schedule — due unspecified (Val asked for it on the call) — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [x] [[wiki/people/val-levitan.md|Val Levitan]] and the team — at the next call, check whether the one E2E flow worked, then plan the schedule for the remaining tests — due Sept 23 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]] — **discharged Sept 23 2026:** checked on the 8:00 AM call (above); no test schedule was set — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [x] [[wiki/people/ivan.md|Ivan]] — rewrite the four manual connection tests so they drop the channel by repointing the port symlink to /dev/null — due unspecified — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]] — **discharged Sept 24 2026:** "что надо было руками это исправлено" (it needed commits into the firmware; the method is not stated) — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — build the tool or instruction set so Claude can generate the money-crediting autotest and check balances — due unspecified — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]] — **Sept 24 2026:** he expects the tooling ready that day, depending on the terminal test API — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]

## Open questions

- **How to test the cloud platform at all.** Chudinov: testing it "сильно отличается от машины" — clusters, a cloud structure, environments to raise and deploy, it cannot be isolated "в отдельном докер контейнере", and it needs Andrei (Bosik, by context — inference). No approach was agreed — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- **When testing on other makers' machines happens.** Pavel expects it to stretch into next month; no plan was set — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]

**§15.8:** clear — test scope and assignment only. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
