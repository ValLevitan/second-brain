---
type: decision
title: The Flex IQ cashier flow is settled — login becomes selectable between a PIN and a magnetic stripe card and the reader stays in the hardware, Cancel is removed, redemption pre-fills the maximum and freezes the amount on continue, the activation receipt always prints while a top-up receipt is optional, and the records list gets date and direction filters
date: 2026-09-15
aliases: [Flex IQ cashier flow, PIN or magnetic stripe, selectable login, magstripe reader stays, remove the cancel button, four digit PIN, pre-filled redemption, freeze the amount, receipt optional on top-up, records filters, X and Z reports, card stock tracking, home screen three blocks, кассир пинкод, магнетик стрип]
source-count: 2
status: active
open-commitments: 3
open-questions: 2
---

# The Flex IQ cashier flow — login, redemption, receipts and records

The Flex IQ half of the UI/UX walkthrough at the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept 15 2026 8:03 AM call]] (Russian), driven by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] on his own screen. Flex IQ alone is the MVP 1 device ([[wiki/decisions/2026-09-11-mvp1-goes-with-flex-iq-alone-and-one-kiosk-per-location.md]]).

## Login — a PIN today, selectable tomorrow

Klimovich kept the PIN screen and removed a step: "я думаю, что нам надо убрать кнопку [cancel], сделать чуть проще жизни кассиру[ —] ты ввёл правильный пин код[,] тебя сразу логинит" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**The PIN stays four digits.** [[wiki/people/pavel.md|Pavel]] asked about six — "не хотим ли мы пинкод сделать больше символов[,] не 4, а, например[,] 6" — and both [[wiki/people/val-levitan.md|Val]] and Klimovich refused. Klimovich's reasoning is that the PIN is not access control at all [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

> **он находится в безопасной локации. Сам этот девайс он стоит у кассира, за чаще всего [бро]нированным стеклом… чтобы просто кто то случайно зашедший не мог получить доступ туда, и пин код это способ контроля кассиров. То есть вот кассир А[,] у него свой пин код[,] кассир Б[,] у него свой пин код… чтоб можно было потом трекать ответственность людей.**

**Val's own requirement, stated as a requirement and addressed to the back-end.** He agreed the PIN is weak — "**пин код это очень очень слабый а[кс]есс[-]контрол. Лучше иметь ма[г]не[т]ик стрип**" — and asked for the method to be a choice rather than a replacement: "**я хотел бы иметь или пользоваться валидацией пинкодом[,] или пользоваться валидацией магнетик стрип[ом]**… я хотел бы вложить вот этот вот селекшн как методологию для логин[а,] администрации[ —] или пинкодом[,] или карточка". He named the recipient: "**я говорю просто для димы чудинова, чтобы была логика, где ты можешь или пинкодом пользоваться, или**…" [[wiki/people/dmitri-chudinov.md|Chudinov]] answered "я согласен… это уже обсуждали ранее" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

- **Set up on the device first, moved to a phone later.** Val: "для меня лучше всего это делать в начале на самом девайсе, то есть войти в администрационн[ое]… [меню,] весь этот сет[ап] сделать[,] а потом перенести это всё на телефон? Но это потом[,] потом." Klimovich's reading — "хорошо[,] на усмотрение локации… при инсталляции мы скажем, какую хотите авторизацию" — went unchallenged.
- **Val treated it as booked.** "окей, тогда мы учли… моё требование[,] тогда давайте отразим это в кейпа билетис" — reflect it in the capabilities [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **Card-based login itself is a later MVP.** Asked how cards would be activated, Val: "не знаю, скорее всего это будет сделано в MVP… каком то последующем."

## The magnetic stripe reader stays in the hardware

Pavel's alarm: "нам сейчас надо главное остановить Геннадия, а то он сейчас магни[т]ик страйп ридер выбросит из флекс[ ай]к[ью]". Val had already spoken to him and says he is not dropping it — "я разговаривал с ним, он это не выбрасывает[;] всё, что мы уничтожаем в этом дизайне[ — ]это 2 экран… мы просто крышку делаем сверху" — the only thing being removed is the second, player-facing screen, and it is being covered over rather than taken out [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. That confirms the Sept-2 ruling retiring the second screen ([[wiki/decisions/2026-09-02-implicit-consent-and-mandatory-printed-receipt.md]]). "Геннадий" here is [[wiki/people/genadi-peari.md|Genadi Peari]], JVL's hardware lead. Val asked Pavel to remind him as a precaution: "если вы будете с ним разговаривать[,] ещё раз напомн[ите], что магне[т]ик стрип остаётся."

**The cards arrive pre-encoded — the reader reads, it does not write.** Klimovich asked whether a blank card could be encoded on the IQ to create a cashier account. Pavel: "[р]идер… нам не надо райт[,] нам рид достаточно, мы просто привяжем потом к новому пользователю." Biratka: "нет, она не работает на запись." Pavel: "есть, которые записывают, но нам… лучше предзаписанн[ые] давать." Klimovich accepted: "карточка может приехать предзаписанная" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

Pavel floated binding a cashier's own payment card instead — "вот у него платёжная карта есть[;] мы можем его же карту сюда привязать… если он не боится её сюда засовывать" — and Val agreed in principle with a barcode analogy: "это как штрих код на… сигаретной коробке[;] ты можешь пользоваться им[,] как [e-]воля[том — ]какая тебе разница?" Klimovich shut the door on it becoming work: "**сейчас все напряглись. В этот момент такого требования пока нет. Все можно выдохнуть. Это идея**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## The home screen and the wallet screen

Three routes from the cashier's home screen — "**3 главных направляющих на хом[ ]экране[ — ]это [create] wallet[,] посмотреть записи и какие[-]то репорты**" — create wallet, view records, reports — with the design language reused from the kiosks. The cashier can also scan a player's carrier straight from there, which opens that wallet directly: "мы здесь показываем просто актуальное состояние… [e-]воли[та —] сколько там денег, какие из них, что с ними можно сделать", with load and redeem as the options [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Redemption pre-fills the maximum, and freezes it on continue

- **Pre-fill.** "я думаю, что мы можем по дефолту сразу сумму указывать… и отказаться от этой странной кнопки… это лишнее действие[;] дефолтное состояние… **максимально возможн[ая] редим[абл] сумма с баланса игрока должна… подставляться по дефолту**" — in the mock-up on screen, $52.50 [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. The screen then shows the standard breakdown: how much came off the balance, how much lands on the card, and the fee.
- **Freeze, and the fraud it stops.** Chudinov raised it: a photographed barcode lets an accomplice load the same money onto a machine while the cashier redeems it — "**ты можешь выводить деньги, а твой там подельник будет в это время будет пытаться отсканировать и деньги на машину закинуть**" — and asked at what stage the amount is frozen. Klimovich's answer, which Irina had proposed a second earlier ("я бы[,] когда отсканировала"): at the moment the cashier has entered the amount and presses continue — "**мы сделаем снова запрос к [e-]вол[ету]… уточняем, что такая сумма по[-]прежнему есть на этом балансе. Если да, то мы её фризим, прям полноценно чуть ли не списываем и ждём завершения**", after which "если ктото параллельно хочет эти же деньги проиграть, то он не увидит этого баланса" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **The sub-millisecond race is acknowledged and not solved.** Klimovich: "всегда есть вот этот классический пример, что если доля миллисекунды происходит одновременно… кто 1[,] тот короче"; Irina: "здесь это очень сложно физически сделать" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. The underlying "every stored balance is a snapshot, re-read it before acting" rule is the Sept-14 one ([[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]] and the Sept-14 entry on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]).

## Receipts — always on activation, optional on a top-up

This narrows the Sept-2 mandatory-receipt ruling ([[wiki/decisions/2026-09-02-implicit-consent-and-mandatory-printed-receipt.md]]) rather than overturning it.

- **On card activation the receipt always prints, with no intermediate question.** Klimovich: "я за то, чтобы там всегда печата[ть]… [ресит] без промежуточных экранов[,] без вопросов. Это важно[:] на ресите есть вся информация для клейма… есть информация… сколько фи[з] списан[о], какая сумма ушла с баланса[,] и **ресит это наша единственная точка, где игрок сразу может увидеть, сколько у него осталось на [e-]волит[е]**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **For a counter top-up, or a wallet created at the counter, the cashier asks first.** Pavel's argument was paper volume — "иначе ты представь[,] сколько мы тикетов будем печатать? Просто вот пришёл человек[,] $5" — and Chudinov's line landed it: "на каждой[,] на каждые 5 баксов будем печатать ресит". Klimovich, who had assumed always ("изначально я думал, что всегда"), accepted a confirmation screen: "нам же не сложно проставить промежуточные экраны и оставить это на совесть игрока и кассира и сэкономить… немного бумаги, я соглашусь", and applied the same to a balance update on an existing wallet [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **When a carrier is created, both print.** "Если создаётся carr[ier], то печатается и carrier, и [ресит;] если у нас уже есть carr[ier], и мы просто обновляем[,] то только [ресит]" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **The receipt matters because the carrier does not change.** Klimovich's reason for wanting one at all on a top-up: "на Кэрри ничего не меняется[;] ему нужна какая[-]то обратная связь" — and where money is handed to a cashier, "кассир ему говорит[ — ]ну всё, зачислено[,] верь мне". He does not expect the counter route to be common — "я думаю, что игроки будут зачислять деньги через бил[л ]валидатор чаще всего" — and Pavel disagreed outright: "так это 100% случаев" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. Pavel also pinned the vocabulary: "билл валидатор это флекс[пей,] кассир это флекс айкью", with Klimovich confirming he meant the validator on the gaming machine.

## Records — every transaction at the location, with two filters

The cashier must see every transaction at the location, and Klimovich listed the types: wallet creation on both IQ and Flex-Port; a balance-update transaction (via the cashier, and when money comes out of a gaming machine); a redemption transaction; and the mirror transaction moving money from a wallet onto a gaming machine. He wants them all on screen despite the volume — "я понимаю, что таких тран[закций] в течение дня на живой локации будет очень много, но я за то, чтобы всё[-]таки показывать их" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

Two filters were asked for and both accepted in the same breath:

- **A date/period filter**, asked for by [[wiki/people/andrey-bosik.md|Bosik]]: "У тебя кнопку календарь надо добавить тогда, чтобы можно было выбирать, за какой день и период."
- **A direction filter**, asked for by [[wiki/people/dmitri-chudinov.md|Chudinov]], who said the first FlexPay implementation had it — money moving between machine and port "в одну сторону и в другую".

Klimovich: "да[,] Андрей, я согласен. Добавим фильтрацию по дням" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. *(§4 note: the date-filter request is Bosik's and the direction-filter request is Chudinov's; Klimovich's "Андрей" in the reply resolves to **Bosik**, whose ask it answers.)* Scanning a carrier filters the list to that wallet's history, and the issued-cards view carries over from [[wiki/topics/flexpay-business-architecture-payout-devices.md|MudaGoose]].

## Reports — one in MVP 1, two ideas for later

- **The one MVP 1 report is the Georgia Lottery one.** "быстрый репорт будет то, что нужно для Джорджия лотере[и;] я его сегодня[,] там[,] завтра доделаю" — see [[wiki/decisions/2026-09-14-one-report-must-make-mvp1-cards-issued-for-a-georgia-lottery-inspection.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **X and Z reports — Bosik raised them, Klimovich had not heard of them.** Bosik's route in was the fiscal board: in Belarus and, he believes, Russia, every cash-accepting device carries one — "во всех аппаратах, которые принимают наличные деньги, стоит фискальная плата, которая счётчик постоянно увеличивает". Pavel: the gaming machines have such counters, but "у нас на флекс п[орте] или на флекс [ай ти ю] такого нету… нет требований от регулятора конкретно для джорджии". Bosik then asked about the standard retail reports — "есть же стандартные торговые отчёты, там зет отчёт[,] икс отчёты… нужно нам их здесь как-то делать[,] или не нужно". Klimovich: "**я не знаю, что такое… икс[;] я погуглю, но если это чтото нам подходящее[,] то окей**", and Bosik posted a short explanation into the meeting chat during the call: "Я коротко кинул там в чате, что такое икс отчет[,] зет отчет… я не знаю, просто это здесь применимо или нет[ —] без понятия" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **Card-stock tracking, floated for MVP 2.** The cashier enters how many blank cards arrived ("мне на локацию пришло 150 карточек для активации, то есть кассиры вбивают число 150"), the system counts issuance down against it, and raises a signal on the IQ when stock runs critically low — "закажи карточки, пришло время заказать". Klimovich: "не[ ]MVP один, но где[-то в] MVP 2 мы добавили бы такую фи[чу;] это очень будет прикольно и от[личает] нас… от конкурентов" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **Who the reports are for.** Klimovich named three audiences — the lottery if it walks into the location, the operator, and the location itself — and said the location-versus-operator split still needs thought [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Administrative screens — likely MVP 2

Biratka asked for a missing screen showing tilts and how to resolve them ("у нас нет экрана с т[и]лтами… и описанием[,] как решить эту проблему[;] наверное, его стоит добавить"); Val agreed. Pavel listed an operator mode with binding a new cashier, changing PINs, setting the Wi-Fi network and diagnostics; Biratka added a screen listing the connected Flex-Ports, which Bosik said he had already written up for the cloud view. Klimovich pushed the whole administrative set out: "**эти все административные штуки, которые живут скорее не под кассиром, а под администратором[,] чуть ли не на [MVP] 2 отложили, потому что у нас на [MVP] один главное дать возможность кассиру работать с локацией, выпускать карточки[,] оперировать [e-]воли[тами]**" — and leaned on remote update to make it recoverable: "если у нас будет удалённые обновления, а мы на это рассчитываем, то потом это накатывать можно и улучшать". Pavel agreed [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. Remote update in MVP 1 is [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]].

Chudinov closed that thread with an offer that unblocks it: "**скорее всего, тебе сегодня подготовлю первую версию флекс[а ай кью с] волят[ным] режимом**… сможешь посмотреть, какие экраны сейчас… что переехало с [Flex]Pay… и дальше уже от этого можно будет отталкиваться, что переделать, что добавлять" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — remind [[wiki/people/genadi-peari.md|Genadi Peari]] that the magnetic stripe reader stays in Flex IQ — due at his next conversation with Genadi; Val's precaution — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] [[wiki/people/alexander-biratka.md|Alexander Biratka]] — add the missing Flex IQ screen showing tilts and how to resolve them — due unspecified; he raised it and Val agreed — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — hand Klimovich the first version of Flex IQ in wallet mode so he can see which screens already exist — due the same day (Sept 15 2026) — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## Open questions

- **Whether X and Z reports apply to Flex IQ at all.** Klimovich had not heard the term and will look it up against Bosik's chat note; Bosik himself says he does not know whether they apply — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- **What the location gets versus what the operator gets**, in report form. Named by Klimovich as needing thought and not answered — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

**§15.8:** clear — cashier-interface and device design only. The PIN-per-cashier point is about transaction traceability as designed, not a judgement about any named person, and no pay, rate or HR assessment appears in either source; nothing was excluded on that ground.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
