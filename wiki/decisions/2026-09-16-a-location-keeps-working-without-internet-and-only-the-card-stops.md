---
type: decision
title: A location keeps working when the internet is down — only card issuance and redemption are blocked, a device may run 24 hours without the server, and lease expiry is the only thing that blocks
date: 2026-09-16
aliases: [requirement 1383, capability 118, offline operation, twenty-four hours, 24 hours, no internet at boot, lease expiry versus internet loss, вернитесь завтра, come back tomorrow, pre-generated validation IDs, we print money not tickets, synchronisation point, cloud eWallet 2027 2028, you cannot allow a location not to work, local wallet creation]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# A location keeps working without internet — only the card stops

The central ruling of the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16 2026 8:01 AM call]] (Russian), and the only argument in this series so far that [[wiki/people/val-levitan.md|Val]] has reversed outright on business grounds. It grew out of requirement **1383** under **capability 118**, which [[wiki/people/dmitri-chudinov.md|Chudinov]] reduced to one sentence: "если нет связи, может ли работать терминал?" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

## How the lease actually behaves today

Chudinov described the implemented behaviour, which no page in the corpus had yet stated [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **[Ф]лекс[ IQ и] флекспей… на старте… получают коннект, получают свежую дату лиз[ы]. И дальше[,] если коннект, например, потерян, [устройство] всё равно мониторит последний ли[з], который был получен… если ли[з] за[э]кспарился в этот момент[,] даже если был дисконнект, он уйдёт в [блок] и заблокируется. Соответственно, разблокировка будет, как только появится коннект[:] он увидит свежую дату.**
>
> *(Flex IQ and FlexPay get a connection at start-up and fetch a fresh lease date. After that, even if the connection is lost, the device keeps monitoring the last lease it holds; if that lease expires while disconnected, it blocks itself anyway, and it unblocks as soon as a connection returns and it sees a fresh date.)*

That is the device-side mechanism behind the lease-blocking policy on [[wiki/decisions/2026-09-11-lease-blocking-reaches-the-flex-ports-and-is-never-automatic.md]].

## Chudinov's position, and why he held it

He argued that Flex IQ was specified never to run offline — "на флекс[ ]айк[ью] было жесткое требование[:] если нет интернет и связи с нашими серверами[,] в принципе смысла ему работать нет" — and grounded it in a control requirement the team itself had set two meetings earlier [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **[М]ы в любой момент должны уметь заблокировать терминал. Сами. Если… оператор может просто пойти, выдернуть кабель и продолж[ить] работать, соответственно, мы этим терминалом управлять не можем. И мы нарушаем требования, которые [сами] установили.**
>
> *(We must be able to block a terminal at any moment. Ourselves. If an operator can simply go and pull the cable and carry on trading, then we cannot control that terminal — and we are breaking the requirement we set.)*

He also had a boot-time reason: on start-up the device must fetch current state, because "возможно[,] мин[ы]-макс[ы]… сервис фе[и] поменялись, возможно, терминал сменил лакейшн" — limits or service fees may have changed, the terminal may have moved location [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. [[wiki/people/pavel.md|Pavel Frolov]] took a middle line: require internet at boot for the parameter check, then tolerate short losses and raise a tilt after a timeout — "какой[-]то тайм[-]аут 5 минут[,] 15 минут" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Val's reversal

Val asked how tickets would be validated with no connection, was told they would not be — [[wiki/people/andrei-klimovich.md|Klimovich]] and Chudinov both landing on a disabled button and a "no connection" pictogram — and then refused the premise entirely [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **Мы же знаем, что часто будет такой, что интернета нету… Нету интернета, но… лакейш[н]ы… будут продолжа[ть] оперироваться. Они хотят, чтобы игроки играли, вкладывали деньги.**
>
> *(We know perfectly well that there will often be no internet… There is no internet, but the locations will go on operating. They want players playing and putting money in.)*

And, to Klimovich as product owner, the sentence the ruling rests on: "**с точки зрения [про]дакт[-]о[у]нера, вы не можете позволить, чтобы лакейш[н] не работал**" — from a product owner's point of view, you cannot allow a location not to work. When Klimovich said he had been saying the same thing, Val's answer was "ну слабо говорит[е]" (then you are saying it too weakly), and Klimovich's: "хорошо, буду более агрессивно говорить" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

His commercial framing was blunter still — "нас выгонят с лакейш[н]ов" (we will be thrown out of the locations) — and he restated the endpoint of the whole business [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **Конечный итог должен быть тот, что мы печатаем деньги. Ни тикеты[,] а деньги. Нам нужна кеш[,] как мой кеш заработал.**
>
> *(The end result has to be that we print money. Not tickets — money. We need cash, so my cash works.)*

## The settlement

Klimovich restated it and Val approved the direction on the spot ("вот сейчас… толковый разговор идёт. Мне нравится это направление, логика работает") [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

- **Without internet the location keeps working.** Wallets are created locally, money is loaded onto them, players move from machine to machine and play — "они могут создавать [е]волят[ы], загружать их деньгами. Они могут ходить от машины к машине".
- **The one thing that cannot happen offline is the card** — issuance and redemption, which need [[wiki/organizations/incom.md|InComm]]. The button is disabled with a clear no-connection message and the player is told to come back: "**это нормально[:] вернитесь завтра**".
- **The player loses nothing**, because the e-wallet stays in his hands — Irina: "его [е]в[олет] остаётся" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- **Lease expiry and internet loss are two different things** and were being run together. Irina made the separation that unlocked the argument: "есть[,] когда блокировка [придёт] — то есть закончилась лиза[ —] мы блокируем[;] это одно. А когда там нет интернета… это уже 2[-]й вопрос, и мы договорились, что мы работу не блокируем… игрок играет, единственное[ —] мы не можем выпустить карточку" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. **Only lease expiry blocks.**
- **No internet at boot no longer prevents start-up**, as long as the lease is still valid — Pavel: "на подъёме устройства нам не надо требовать, чтоб был интернет обязательно"; Irina: "устройство… знает, когда у [него] [э]кспайр[ится] дейт по лиз[е]" — the device already holds its own expiry date [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## The 24-hour window, and how contested it is

Pavel asked for an acceptance criterion saying the device continues to work with no internet at start-up; Val asked the obvious follow-up — for how long [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

The engineers wanted no bound: Pavel said "пока лиза не закончится" (until the lease expires) and Klimovich went further — "мы продолжаем работать неограниченное количество времени. Я не вижу проблем" (unlimited; I see no problem). Val refused: "нет, нет, нет, нет… конечно нет" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

He then set the figure himself, listing the alternatives out loud — "или 6, или 12, или 24?" — and landing on **24 hours as a working number**, explicitly not a decision [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **Окей, пока не принято это решение. Давайте 24… Я согласен, что 24 может быть ту[ ]лон[г][;] если у кого[-]то есть какие[-]то критические взгляды на это, пожалуйста[,] я опен[;] если ни у кого нету[ —] 24 и поехали дальше.**
>
> *(OK, the decision is not taken yet. Let us say 24… I accept that 24 may be too long; if anyone has a critical view on it, please, I am open; if nobody does, 24 and we move on.)*

**Val's own doubt runs the opposite way to the engineers'** — he thinks 24 may be too *long*, they wanted it unbounded — which is the shape to keep in mind when the number is revisited. Chudinov's earlier framing of what the window is *for* was much shorter: "интернет пропал на какие[-]то там 5[-]10 минут… мы даём это окно и ничего не блокируем", because JVL cannot tell a pulled cable from a real fault — "мы ж не знаем, там реальный кабель вы[дер]нули, чтобы нас игнорировать, либо это реально какие[-]то технические проблемы[:] модем[,] да[,] глушилка" (a modem, or a jammer) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Val's offline-validation idea, refused by the engineers

Val floated issuing something offline anyway — a validation ticket, or pre-generating a batch "например[,] 100 [в]алида[й]шн на эти[х] тикет[ах] заранее" (about a hundred validation IDs in advance) so that a payout could still be made [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Both engineers refused it. Chudinov: "с точки зрения технической, инженерной это очень плохой кейс… не поддержит тут ни Андрей[,] никто[;] это мы просто создаём себе проблемы на ровном месте" (we would simply be manufacturing problems out of nothing). [[wiki/people/alexander-biratka.md|Biratka]]: "это решение очень не очень хорошее" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Val's counter-complaint is worth keeping as a standing pattern in how he argues with engineers: "**я уже много раз сталкивался… с таким разговором[:] ни один инженер никогда ещё не доказывал, какие проблемы**" — he has had this conversation many times and no engineer has ever demonstrated what the problems actually are [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. The idea was not adopted.

## Biratka's question that shrank the problem

Biratka asked the question nobody had asked: why move the e-wallet into the cloud at all — "почему мы хотим переместить [е]в[олет] в облако, для чего?" The answers given [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

- Val: **central validation of all tickets**, and the ability to consolidate and give bonuses — "центральная система валидации всех тикетов[,] возможность обобщать, давать бонусы".
- Klimovich: **kiosk replacement** — "в случае замена киоска на локации[:] мы привезли новый киоск[,] поставили".

Biratka's own candidate — cashing the same e-wallet at a different kiosk — was refused by Val outright ("нет[,] нету[,] нету"), and with that gone Biratka reassessed the whole difficulty [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **[Т]огда проблема, наверное, не такая большая, как как я сразу подумал… нужна нам нужна точка синхронизации[;] если… больше никто не будет пытаться обновить наш тикет на облаке, тогда… немного возникнет сложностей.**
>
> *(Then the problem is probably not as big as I first thought… what we need is a synchronisation point; if nothing else is going to try to update our ticket in the cloud, then few difficulties arise.)*

Val agreed and generalised it: JVL's operating conditions should not be real-time communication — "условия работы наши должны быть не… рилтайм коммуникейшн" (the phrase he reached for next is garbled and is not reconstructed here) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. Pavel added the one caveat that survives: if cloud tickets are ever shown in a phone app, a wallet updated at the location will not appear updated on the phone until the kiosk and the cloud synchronise [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Val then shut the topic down on schedule grounds**: "мы говорим про релиз в 2027[,] в 28 год[у]. Мы не говорим про сегодняшний релиз 1 октября… мы будем сейчас 2 [часа] потратим на это и никуда не придём" — the cloud e-wallet is a 2027–2028 release and will not be designed in detail now [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. Klimovich accepted with one reservation: the subject does have to be thought through for release 2, "но не во всех тех глубоких деталях, которые мы сейчас проговаривали" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — add to the boot requirement that the device continues working with no internet at start-up while the lease is valid, up to the agreed window — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

## Open questions

- **Is 24 hours the right offline window?** Set as a working figure; Val said it may be too long, Pavel wanted it bounded only by lease expiry, Klimovich wanted no bound, and Chudinov's own framing was 5–10 minutes. Val explicitly invited objections — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

**§15.8:** clear — product behaviour, network assumptions and release scope only; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground. Val's remarks about how engineers argue are directed at a pattern of discussion, not at any individual's performance. **§15.9:** no licence, registration, tax or account number appears in this material.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
