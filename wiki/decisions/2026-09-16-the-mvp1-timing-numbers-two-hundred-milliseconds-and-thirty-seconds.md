---
type: decision
title: The MVP 1 timing numbers — 200 ms between screens under load, 30 seconds to wait for an activation answer, 30 seconds for a player to collect at the Flex-Port, and a silent InComm leaves a pending transaction
date: 2026-09-16
aliases: [requirement 1435, requirement 1437, requirement 1438, requirement 1469, capability 151, 200 milliseconds, 30 seconds, thirty second timeout, collect timeout, activation timeout, pending transaction, no answer at all, retry later, universal not per-location, 200 миллисекунд это стандарт]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# The MVP 1 timing numbers

Four requirements on [[wiki/people/irina-shishko.md|Irina Shishko]]'s open-question list at the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16 2026 8:01 AM call]] (Russian) were all versions of the same unanswered question — *how long*. Three of them ended on the same number [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## 200 ms between screens under load — requirement 1435 (capability 151)

Neither [[wiki/people/andrei-klimovich.md|Klimovich]] nor [[wiki/people/pavel.md|Pavel Frolov]] could work out what the requirement was for; [[wiki/people/dmitri-chudinov.md|Chudinov]] supplied the scenario: "например, 10 [флекс]портов одновременно шлёт какие[-]то сообщения[,] терминал получил нагрузку ощутимую[;] ты нажал кнопку… хочу активировать карту[,] и твой экран загрузился не практически сразу, а… на минуту подвис" — ten Flex-Ports all messaging at once, the terminal under real load, and the cashier's screen hanging for a minute after a button press [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. The requirement exists so that "[з]адержк[а] был[а]… не критичен".

The number was not negotiated. Chudinov: "**200 миллисекунд[ —] это стандарт, ну мировой**" — 200 ms is the standard, the world standard — for the cashier's wait on an operation or a transition between screens. Klimovich accepted it as written ("меня устраивает"), and the open-question wording was struck out at Irina's instruction, leaving the number itself in place [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Chudinov also observed in passing that 1435 reads as a non-functional requirement rather than a functional one; Irina's answer was that this changes nothing about the obligation — "это не отменяет, что вопрос нужно снять. Ответить" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. It is the same distinction [[wiki/people/val-levitan.md|Val]] put a date on the day before ([[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]]).

## 30 seconds to wait for an activation answer — requirements 1437 and 1438

Chudinov set out the shape of it first. Every error InComm actually returns is shown immediately, "ну понятно[,] там какой[-]то дел[ей] есть". The exception is a service that is simply unreachable, where a wait has to be configured — "как обычно, вот браузер ждёт… мы можем выставить, например, там 30 секунд, либо минуту. Если за минуту [от] сервера не получили ответа… пишем… повторите операци[ю] позже" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Klimovich rejected a minute by feel — "одна минута точно нет. По ощущениям это очень долго" — and floated ten seconds. [[wiki/people/andrey-bosik.md|Bosik]], asked directly for a figure, declined to give one on the grounds that it depends on conditions outside JVL: "она ж может зависеть от чего угодно… у самого провайдера может что[-]то быть [с] сетью" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. Pavel supplied the human constraint — "обычно это не сильно долго, чтобы человек не подумал, что это вечно… полминуты[,] максимум минута" — and Chudinov proposed half a minute. Klimovich closed it [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **Давайте зафиксировали[,] давайте 30 секунд[.] Опытным путём придём к другой возможно цифре[,] а возможно[,] убедимся, что 30 — это хорошее число.**
>
> *(Let us fix it: 30 seconds. By experience we may arrive at a different figure, or we may satisfy ourselves that 30 is a good number.)*

Requirement 1438 turned out to be the same question asked again, with the AI assistant explicitly offering a choice — Klimovich: "[э]то автор[ом] сгенерированное, и он хочет, чтобы мы выбрали между 30 секундами [и минутой]… ну вот мы выбираем 30" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**The case with no answer at all.** Chudinov named a failure mode he has never seen in the field and could not dismiss: "когда [ИН]КОМ не отдал никакой ответ и непонятно, что он сделал[ —] запрос отправили, ответа не получили, и неизвестно[,] активирована карта[,] не активирована… такое… ни разу ещё не ловил" — the request goes out, nothing comes back, and JVL cannot tell whether the card was activated. He credited the AI assistant with raising it: "Клод подсказывает, что такое может быть" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. **The ruling: such an operation is parked as awaiting an answer** — "такая операция будет помещена как ожидающий ответ[,] и ответ получим… ИНКОМ в будущем скажут, что с эти[ми] транзакци[ями] произошло" — and stays pending until [[wiki/organizations/incom.md|InComm]] later says what happened. Everything else is handled in real time [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**The second half of requirement 1437 was deleted as over-engineered.** Nobody in the room could work out what it was asking — Chudinov: "я в принципе не могу понять вопроса"; Pavel: "к чему этот вопрос?… на что он влияет?"; Chudinov again: "даже ни критерий, ни проверка никакая" — and it went. Irina's verdict on the author: "**ну перестарался клод**" (Claude overdid it), Klimovich's: "перестраховался" (over-hedged) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## 30 seconds for the player to collect at the Flex-Port — requirement 1469

The state being timed is the Flex-Port sitting in its collect fork: credits taken off the machine, the screen offering *scan your ticket or create a new wallet*. Klimovich: "он… висит в этом ожидании. Вот сколько мы там хотим висеть?" The value already in the requirement struck him as far too short — "по ощущениям секунд 15 было где[-]то", his impression, not a read figure [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. *(Irina wondered whether the short number was actually the machine-to-port confirmation timing — "возможно, это про 8 секунд, которые между машиной и портом" — offered as a guess and not resolved.)* [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

Irina framed the test as a human one — how long does a person need to get the ticket out of a pocket — and Klimovich set 30 seconds: "нормальное время, чтобы сообразить[:] а тикета у меня нету, а он тут ещё пишет о том, что можно создать новый". Irina added the reading time — "ещё надо же успеть прочитать то, что предлагают" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**It is universal, not a per-location parameter.** Pavel asked for it to be configurable per location and was refused: "нет, точно не для локации… мне сложно представить локаци[ю,] где… люди не успевают просканировать… это универсальная. Без проблем[,] мы будем наблюдать. Ну если мы убедимся[,] [что] 30 секунд слишком мало, мы везде поменяем это значение" — one value everywhere, changed everywhere at once if observation says so [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. That is the same collect fork described on [[wiki/decisions/2026-09-15-the-flex-port-idle-screen-never-sleeps-and-the-port-mirrors-the-machine.md]], and the timeout's consequence — the money going to unclaimed rather than being lost — is [[wiki/decisions/2026-09-15-a-timeout-sends-the-money-to-unclaimed-and-the-player-never-loses-it.md]].

**§15.8:** clear — timing standards and error handling only; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground. **§15.9:** no licence, registration, tax or account number appears in this material.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
