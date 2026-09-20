---
type: decision
title: The Flex-Port idle screen loses its buttons and its scanner never sleeps, language becomes a top-right toggle that switches on the fly, error and block states share one screen with maintenance and lockout as two distinct signals, and the port mirrors the machine's own state even when the block comes from the Georgia Lottery
date: 2026-09-15
aliases: [idle screen, always-on scanner, scan your ticket or insert money, language toggle, service button top right, maintenance versus lockout, under maintenance, out of service, unified error screen, port mirrors the machine, door open cannot accept money, Georgia Lottery block, Spanish support, two SAS ports tilt test, вайдал скрин, аут оф сервис, requirement 1454, requirement 1469, requirement 852, error catalogue back to Draft, collect timeout thirty seconds]
source-count: 4
status: active
open-commitments: 4
open-questions: 2
---

# The Flex-Port idle screen never sleeps, and the port mirrors the machine

The Flex-Port half of the UI/UX walkthrough at the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept 15 2026 8:03 AM call]] (Russian) — the screens [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] had owed since the previous day. He asked the group not to argue the visual design: "это ворк энд прогресс… я бы хотел, чтобы мы сейчас с вами не цеплялись за дизайн… давайте мы просто пробежимся с вами по воркфлоу" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## The idle screen loses its buttons

Today the idle screen carries two buttons — start game, and a Spanish one. Klimovich's objection: "мне не очень то нравится, потому что от игрока это требуют плюс одно действие[ —] выбери сначала условно язык, а потом сканируй тикет" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

- **The optical scanner runs permanently in the idle state.** "**Я за то, чтобы у нас оптический сканер работал всегда[ — ]в режиме ожидания**", with the screen saying only "просканируй тикет или загрузи деньги в бил[л ]валидатор" — scan your ticket, or put money in the bill validator. "И от игрока требуется только просканировать и всё" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **Language moves to a service button in the top right and switches on the fly.** "выбор языка уходит в правый верхний угол[,] становится сервисной кнопкой такой же, как везде… испанско[-]английск[ое] переключение, которое переключает язык на лету на любом экране, где находится пользователь" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**A permanently-live scanner is not a hardware problem**, confirmed from three directions. [[wiki/people/dmitri-chudinov.md|Chudinov]]: "**вот уже год стоят наши включены, не отключаются и работают**" — JVL's own units have run that way for a year. [[wiki/people/andrey-bosik.md|Bosik]]: "в магазинах же прайсчек[еры] тоже висят в режиме ожидания" — supermarket price checkers do the same. [[wiki/people/val-levitan.md|Val]] named the part that actually wears and why it survives: the illumination, which motion detection keeps off until something approaches — "так что перегорает[ —] это подсветка". [[wiki/people/pavel.md|Pavel]] described the mechanism: "он просто постоянно снимает перед собой картинку без подсветки. Если видит изменения, он тогда включает подсветку и начинает… обрабатывать", and [[wiki/people/alexander-biratka.md|Biratka]] confirmed JVL's own unit does the same — "наше то же самое… моушен… детекшн" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. Klimovich's conclusion: "если у нас есть… детект[ор] какойто, то мы можем держать всё время… в состоянии сканер".

**The mock-ups must be redrawn at the real screen resolution.** Pavel's design note, accepted: "**ты можешь вот это вот всё, что ты здесь нарисовал[,] рисовать в реальном разрешении экрана флекспорта**, потому что здесь у тебя все тексты влазят, они большие, красивые[,] кнопки маленькие… но если сюда разместить кнопку, на которую реально палец помещается, то кнопка вот этот вот Эспаньол[ —] она будет четверть экрана занимать" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. Klimovich accepted it and blamed the tool: "мы вчера с [Клод]ом не поняли друг друга[;] я хотел именно того, что ты говоришь, он пошёл [сво]им путём[;] мы сегодня добьёмся этого".

## Spanish is needed, but not necessarily by October 1

Klimovich: "**мы должны будем добавить поддержку испанского, потому что мы, разговаривая с некоторыми операторами, прямо некоторые говорили, что у нас есть локации стопроцентно испаноязычные**" — some operators run locations that are entirely Spanish-speaking. He explicitly did not date it to the release: "я не говорю, что это прямо важно… чтобы успеть к 1 октября" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. The October-1 date is [[wiki/decisions/2026-09-09-first-transactional-installation-planned-for-october-1.md]].

- **The gaming machines themselves are not translated.** "а в игровых машинах[,] по моему, никто не переводит, и нам это делать не надо" — the translation matters where money moves and the player needs plain instructions.
- **Both languages at once was proposed and rejected.** Biratka suggested printing both on these simple screens; Irina thought it would fit. Klimovich refused on friction grounds: "мне кажется, это засоряет экран. Это создаёт сложность восприятия. **Думаете о наших игроках как очень простых людях[;] их надо за ручку[,] минимальным фрикшеном[,] провести через этот новый для них опыт**… чем меньше им надо информации анализировать[,] тем лучше" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. Pavel's caution was practical: check it on the small screen, "потому что здесь на большом оно, конечно, всё влезет."

## One error screen, but two distinct signals

Klimovich: the error states will share one screen with different texts — "скорее всего экран ошибок будет унифицированный, просто будут разные тексты в зависимости от состояния" — and the same for a blocked location, where the port must be blocked too and the scanner may even be switched off: "никакого следующего шага быть не должно" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

Bosik asked what happens during planned maintenance of the terminals and the back-end platform — the same screen, or a different one? Klimovich wanted a separate "under maintenance" for brand reasons: "аут[о ]сервис это чтото пошло не так[,] у нас чтото не работает. Ан[дер ]мейнтен[е]нс[ — ]всё под контролем, мы занимаемся этим вопросом." Pavel would have used one screen with a reason line beneath. **Val settled it as two signals, not one:** "**и ещё надо нам 2 сигнала… [maintenance]**… и… **[lock]out**… **2 разные вещи**" — maintenance, and lockout for a blocked location [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

*(Two passages here are lightly garbled: Val's rendering of the maintenance word is "imanters … не андертонс", and the lockout as "Lock aute". The two-signal ruling itself is unambiguous — he says "2 разные вещи" and Klimovich confirms he means location blocking.)*

## The Georgia Lottery block — Val's position, and the reversal

[[wiki/people/pavel.md|Pavel]] raised the harder case: a block from the state, not from JVL. Val described the mechanism: "**они наш[у] систему не блокируют, они пользуются первым са[с-]портом[,] блокируют машины**" — the [[wiki/organizations/georgia-lottery-corporation.md|Georgia Lottery]] locks the machine over SAS port 1, leaving JVL's own system running [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

His first position was that this is not JVL's problem — "**это это не моя проблема**". Pavel refused it flatly, three times: "Не не, не, это неправильно. Это это неправильно, вау[,] совсем неправильно", and then stated the rule that was adopted [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

> **Мы должны синхронизироваться, мы должны синхро[флек] синхронизировать с машиной максимально, то есть если машина заблокирована, мы должны здесь тоже сказать[ —] она заблокирована[;] если дверь открыта, мы должны сказать[ —] дверь открыта. Мы не можем принимать сейчас деньги.**

Klimovich supplied the ownership argument: "**да[,] вал[,] мы отвечаем за [e-]волет[,] JVL отвечает за [e-]волят. И если игрок загрузит деньги с [e-]волит и не сможет их не вернуть, не поиграть[ — ]это… наша проблема**". Val conceded in one line [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

> **Согласен. Вы вы более гуманитарные люди, чем я.**

**The code for it already exists but is untested in the two-port configuration.** Pavel: "это уже в той версии, что я вчера Андрею отдал, она уже работает" — it works in the build he handed Klimovich the previous day. Biratka asked whether it had been checked with two SAS ports connected; Pavel had not: "нет, нет, нет, это вот я сегодня Ир[ин]е говорил, что надо проверить, что если по 1 сас[у] пришла блокировка, то мы это увидим", adding "скорее всего будет работать". Biratka named the precondition — tilt transmission has to be enabled on the machine side ("на машине должн[о] [быть] включен[о]… передача т[и]лтов [по] сас") — and Pavel asked for his field experience to build the test cases: "**Саша[,] надо будет твой экспириенс, чтобы придумать тест кейсы для этого… мы даже по имплементации не можем это всё предвидеть без вот твоих знаний**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. The single-versus-dual SAS support position is [[wiki/decisions/2026-09-09-jvl-supports-both-dual-sas-and-single-sas-and-not-mudagoose.md]]; lease blocking reaching the ports is [[wiki/decisions/2026-09-11-lease-blocking-reaches-the-flex-ports-and-is-never-automatic.md]].

## Smaller screen-flow rulings from the same walkthrough

- **The scan-balance step is unchanged, with one addition:** if the wallet balance is below the offered amount, that button is disabled — "если у него баланса недостаточно, чем там предлагаемые $20, то мы эту кнопку должны сделать неактивной" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **Collect becomes a two-way waiting state.** After collect, the port waits: scan a valid wallet and the money goes to it, or press the get-a-ticket option and [[wiki/topics/flexpay-business-architecture-payout-devices.md|Flex IQ]] prints a carrier for a newly created wallet. That is the Sept-14 collect fork ([[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]]) drawn as a screen.
- **Irina found the emphasis backwards** on that screen — the big button pushes the player to take a new ticket rather than scan the one he holds: "ты заставляешь игрока нажать в первую очередь получить новый тикет… надпись теряется, а большая кнопка[ — ]получ[ить] тикет". Klimovich agreed: "**акцент должен быть на просканиру[й]**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **The countdown appears late, not throughout.** Chudinov: "тайм[-]аут, наверное[,] лучше включать, когда там чтото остаётся до конца[;] когда постоянный тайма[ут,] сразу заставляешь немножко нервничать". Klimovich: "согласен… да[,] слишком тайм[-]прессинг" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. What happens *when* it expires is [[wiki/decisions/2026-09-15-a-timeout-sends-the-money-to-unclaimed-and-the-player-never-loses-it.md]].
- **The error list is not final.** Klimovich could not explain his own error codes on the mock-up — "я не помню[,] почему у меня разные [error] ид[ы], чем они принципиально отличаются? Я пересмотрю" — and expects to add more: "наверное, это не все ошибки, мы их добавим" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Update, Sept 16 2026 — the error catalogue gets a Jira consequence, and the collect timeout gets a number

At the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept-16 8:01 AM call]] the incomplete error list stopped being only a to-do and became a status change. Requirement **1454** (capability not named on the call) carries the error handling, and Klimovich conceded the catalogue does not exist: "здесь нам нужно просто каталог этих всех ошибок создать… это надо сделать[,] это тоже задача". [[wiki/people/irina-shishko.md|Irina]] had its status moved **back from Published to Draft** until it does — "паблиш для этого [реквайрмента] поменяй на[…] драфт" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. The commitment below is therefore **not discharged**; it now has a visible marker in Jira.

**The Flex-Port collect timeout is 30 seconds** (requirement 1469), universal rather than per-location — see [[wiki/decisions/2026-09-16-the-mvp1-timing-numbers-two-hundred-milliseconds-and-thirty-seconds.md]]. Klimovich's read of the value that was there before was "по ощущениям секунд 15", an impression rather than a figure [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**The two-SAS-port question was touched and not settled.** Requirement **852** — an older requirement about the Flex-Port and SAS — came up at the end. [[wiki/people/pavel.md|Pavel]]: "это требование к машинам[:] наши машины мы знаем, что они 2 порта поддерживают, а… чужие[ —] это как повезёт" (JVL's own machines support two ports; other manufacturers' are luck of the draw). [[wiki/people/dmitri-chudinov.md|Chudinov]] said the current protocol treats the second port as a reserve it does not know about, and Irina closed it with "мы ж не будем на ходу ничего переключать" — nothing will be switched over on the fly. **No ruling was made**, and the standing corpus contradiction over how many machines carry a second SAS port is untouched by this [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — redraw the Flex-Port mock-ups at the port's real screen resolution, with finger-sized buttons — due before the next review — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — review the Flex-Port error identifiers he could not explain, and create the full catalogue of errors behind the unified error screen — due unspecified; **still outstanding on Sept 16 2026**, with requirement 1454 moved back to Draft until it exists — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — test that a block arriving over one SAS port is seen by the Flex-Port when two ports are connected — due unspecified; untested in the build handed to Klimovich on Sept 14 — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] [[wiki/people/alexander-biratka.md|Alexander Biratka]] — help Pavel build the test cases for machine tilt and block handling over SAS, using his field experience — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## Open questions

- **Whether Spanish makes the October 1 release.** Needed, and explicitly not promised for the date — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- **Whether the port can switch its scanner off at all when a location is blocked.** Klimovich left it conditional — "можем отключить даже сканеры, если мы умеем это делать" — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

**§15.8:** clear — screen design and device behaviour only; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
