---
type: decision
title: The Georgia LTE modem failure is treated as a source-and-firmware mismatch — buy the North-America variant and, in parallel, ask KORE for the recommended modems and the APN
date: 2026-09-04
aliases: [7455 modem, firmware-update USB stick, 5G module, LTE hard to buy, modem firmware mismatch, North America modem variant, KORE APN, ask KORE which modems, AliExpress modem Minsk, $16 Amazon modem, two antennas on the module, antenna in an opening]
source-count: 10
status: active
open-commitments: 10
open-questions: 5
---

# The Georgia modem failure is a source-and-firmware mismatch — buy the North-America variant, and ask KORE for the APN

On the [[wiki/meetings/2026-09-04-lte-modem-firmware-mismatch-and-kore-settings.md|Sept 4 2026 midday modem call]] (Russian, 12:10–12:29 PM ET) [[wiki/people/pavel.md|Pavel Frolov]] reported that the LTE modem installed in Georgia will not hold a connection, [[wiki/people/genadi-peari.md|Genadi Peari]] named the cause, and [[wiki/people/val-levitan.md|Val]] set two routes running in parallel rather than choosing between them. This continues the LTE-modem thread opened at the [[wiki/meetings/2026-08-10-lte-modem-v1000-georgia-coam.md|Aug-10 V-1000 session]] and underpins the fitment ruling [[wiki/decisions/2026-08-21-cell-modem-on-every-machine-from-september-1.md]] and the [[wiki/topics/machine-data-repurchase-program.md|$337/year data-repurchase programme]] that rides on it.

## The position, as Pavel reported it

- **The modem that was fitted does not work, and the reason is not fully clear.** "Не работает тот модем, который вставили? 74 55 модель… Причина почему не работает не совсем ясна." His three candidate causes: "либо несовместимость с провайдером, может, не под тот рынок модем… Может слишком старая прошивка?" — carrier incompatibility, a modem built for another market, or firmware that is too old [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]. *(The part is named in the source only as a "**7455**" model number — no vendor or full part number is stated, and none is asserted here.)*
- **Two days of experiments in Georgia failed to configure a stable link.** "мы запустили тестирование с Элизабет и в результате двухдневных экспериментов выяснили, что не получается его настроить, чтобы он стабильно держал связь" — run with [[wiki/people/elizabeth.md|Elizabeth Palomino]] [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].
- **It had passed testing — in Minsk.** Asked by Val why, Pavel drew the distinction: "мы здесь протестировали в Минске такой же такой же самым… 74 55 слишком много разных входных данных, другой провайдер, другая версия прошивки на другой рынок модем рассчитан" — same model number, but too many differing inputs: different carrier, different firmware version, a modem intended for a different market. He put the Minsk test at two weeks earlier: "Мы это в Минске сделали 2 недели назад" [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].

## The diagnosis Genadi named, and Pavel's refusal of the framing

Genadi called it a strategic mistake rather than a technical one: "Мы взяли Павел заказал такой же модем 74, 55. На алиэкспресс получил в Минск. А Джорджия получили точно такой 74 55, но не с алиэкспресс… Разная версия феенбари [firmware]… То, что они разные, это это возможно. Это была ошибка номер один." Minsk's unit came from AliExpress; Georgia's was the same model number from a different source, with different firmware — "mistake number one" [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].

Pavel did not accept it: "Я не согласен, я не согласен какая ошибка стоп стоп какая ошибка. Где ошибка?" **Nothing on the call reconciles the two readings** — Val accepted Genadi's diagnosis and moved to remedies; Pavel's objection stands unanswered [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]. The accountability argument that followed is on [[wiki/topics/jvl-operating-principles.md]] (Sept 4).

## What was decided

- **Buy the North-America variant of the same modem and test that.** Genadi: "этот же модем… Но точно [ф]о[р] Норс Америка марки[,] это есть на амазоне, он там стоит **$16**… наверно там прошивка будет… Наверняка правильное" *(the transcript renders the phrase as "точно фонорс Америка марки")* — the same modem in a North-America variant is on Amazon at about $16, where the firmware is likely to be the right one, and the whole thing could be finished "Дня 2" — in about two days [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].
- **There is time for it.** Val: "у нас на это есть время, потому что ещё граф[ика] и [колласоц — garbled] не не готовы" — the graphics and another item (the second word is not readable) are not ready either [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].
- **Ask KORE which modems they recommend, rather than continuing to guess.** Val: "Давайте мы давайте мы спросим о кор какие модемы, они рекомендуют," having first asked whether modems can be bought from KORE directly — "А мы можем заказать фромкор модемы фромкор?" — and reasoning that "Они нам посоветуют, на каких модемах они протестировали и что у них работает" [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].
- **Ask KORE for the modem configuration parameters too, in particular the APN — which could solve it outright.** Pavel's addition: "Могут ли они дать параметры настройки модема? Потому что может быть просто… Этот самый [APN], они нам скажут и с этим [APN], если мы зашьём его жёстко, то наши модемы заработают. Тоже не исключено." If KORE supplies the parameters and JVL hard-codes them, the modems already in the field may simply start working. He expected most modems to connect automatically — "Большинство модемов должны работать в режиме автоматика подключения, но вдруг там какието специфические настройки?" [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]. *(The transcript renders the parameter as "IPN"; the derived notes of the same meeting read it as the **APN**, which is what is recorded here [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].)*
- **Antennas come out of the metal enclosure.** Two antennas are now fitted to the module — "подключили сейчас 2 антенны на модуль" — and Genadi wants the antenna placed into an opening rather than glued to the body: "ее лучше вставлять в opening… [не] приклеен[ную] ставить… на корпус, потому что все сигналы же уходят." Pavel relayed the same suspicion: an antenna glued to a metal enclosure shields badly and may need to sit further outside it [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]. This advances, but does not close, the Aug-10 antenna-mounting question on [[wiki/projects/georgia-market-rollout.md]].
- **The execution chain Val read back, and Pavel confirmed:** "Послал email [KORE]… Покупаем… другие модемы[,] эти модемы отсылаются в Джорджи[ю], там Элизабет их поставят и вы[,] Павел[,] ремо[утно] аплоут софт и проверите." Pavel: "Я надеюсь, что нормально[,] нормальный модем, он сразу же заработает на том софте, которые есть. Если нет, то мне придётся удалённо подключаться и пытаться найти причину" [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].

## Why an off-the-shelf modem is a gamble at all — Pavel's explanation

"Эти вот все модемы, которые свободно продаются через Amazon, они, как правило[,] взяты с какогото рынка, например, с деловских лэптопов… под деловский лэптоп[,] и выпустили партию там 5000 штук. Они каким то образом попали на рынок… [в] прошивке будет заложена поддержка какихто там операторов… А какието операторы будут игнорироваться и с этим модемом не могут не работать." Openly-sold modems are usually pulled from some other market — a batch made for **Dell laptops**, say — and their firmware may carry support for some carriers while ignoring others [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].

The SIM side compounds it. Pavel: "у них свои настройки на симкарте. И… эта сим карта может не работать с тем модемом" — KORE's own settings live on the SIM, and that SIM may not work with a given modem [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].

**On the network behind the KORE SIM:** asked which SIM cards go in, Genadi answered with a phrase the transcript does not render readably ("Ну коры то живорайзен ну") and then "Тот же самый да." **No carrier is asserted here** — the underlying network is not legible in the source [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].

## Sept 14 2026 — the gate Val put on it, two form factors to order, and a disagreement that did not close

Ten days later the same three people came back to it at the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|Sept-14 12:04 PM hardware call]] (Russian). [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

**Val turned it into a deployment gate, twice.** "**[Cell] мод[е]м мы не можем поставить это [в поле], притом это должно работать идеально**" — we cannot put this out, and it has to work **perfectly**. And, after the technical exchange: "**я просто говорю, что если он не заработает, мы не можем поставить. Даже ни одного [unit] там**" — if it does not work, not even one goes out. *(The transcript garbles two words in these lines — "**на волоке**" and "**ни одного июня**" ("June"); the derived notes read them as "in the field" and "a single unit". Recorded as **readings**, and the gate itself is unambiguous in either.)* [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]] [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

**Pavel wants to order from KORE now, in two form factors.** "**нам надо обязательно заказывать [у KORE] сейчас модемы, причём нам надо 2 разных образца модемов… [о]дни, которые [M.2] слот, а 2, которые [mini-PCIe]**" — two different samples, one M.2 and one mini-PCIe. This is the "**А мы можем заказать [modems] from [KORE]?**" route Val opened on Sept 4 being taken up as an order rather than a question. *(The transcript renders the vendor as "**укора**" — read as "[у] KORE", an **inference** supported by the whole Sept-4 KORE thread — and the second form factor as "**минипис**", read as mini-PCIe.)* [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

**Which product each form factor is for is only half legible.** "**[о]дни получаются идут для [vivan sousend], а 2 идут для… Флекс ай[ ]кю**" — one lot for a product rendered "**vivan sousend**", **which is not interpretable and is not identified here**; the other for **Flex IQ**. The derived notes skip the unreadable product and say only "one type for each product line". [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]] [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

**The diagnosis has moved — and the two engineers still do not agree.** Genadi now says the modem itself is fine and the SIM is the problem: "**[Ф]лекс[ ]айкью уже мод[ем] заработал сразу без всяких проблем — это симка какая[-]то [incompatibility]**." Pavel would not accept it: "**Я бы так не говорил однозначно, Гена — это надо с этой симкой пробовать коннектиться, может быть всё что угодно**" — it could be anything, and it has to be tried *with that SIM*. What they do agree on is the observation underneath: Genadi — "**у тебя же с другой симкой он сразу заработал**"; Pavel — "**Да, с другой симкой он сразу заработал**." A **different SIM worked immediately** [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

This is the **same shape as the Sept-4 exchange above** — Genadi naming a cause, Pavel refusing the framing, nothing reconciled — and it is again left unresolved in the source. The Sept-4 page's open question about the APN is untouched: **nothing in the Sept-14 source records KORE having answered.**

**The parallel test.** "**[п]араллельно с этим будем сейчас с Андреем пробовать… ставить эти же симки [в] Флекс [IQ] — смотреть, как оно работает**" — Pavel and an "Андрей" will put the same SIMs into the Flex units and watch. *(**§4 unresolved:** the corpus holds three distinct Andreis — [[wiki/people/andrey-bosik.md|Andrey Bosik]] (DevOps), [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (online games / product) and Andrew Khandov (C# Miranda) — and **none of them is a hardware or SIM tester**. Left unresolved and queued rather than force-matched.)* [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Sept 24 2026 — the chosen module works after a firmware upgrade, LTE is hard to buy, and a USB stick to flash the firmware

On the [[wiki/meetings/2026-09-24-hardware-repo-bom-source-of-truth-and-street-cabinet-layout.md|Sept 24 4:38 PM alignment call]] [[wiki/people/genadi-peari.md|Genadi]] said he had spent the day on modems and was confused ("я честно говоря уже конфьюз совсем с модом"). [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]

- **The module works after a firmware upgrade.** The LTE module chosen with Pavel is "хорошее нормальная китайский"; he then did an upgrade ("он потом сделал апвер") and "они тоже заработали." *(Who "он" is — Pavel, by context — is an inference.)* [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- **LTE is now hard to buy.** "Проблема что LTE сейчас очень уже тяжело купить… И локали." Misha ([[wiki/people/mikhail-perelman.md|Mikhail Perelman]], by the procurement context — inference) bought a small number; the count is garbled ("10 чтото там купил длина 8"). [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- **5G quoted from China.** Genadi: "в Китае… модули они сразу стоит $150." Val did not know the difference between 5G and LTE "Кроме скорости", but: "если, например, Файв ч работает лучше на лакешене чем LTI то конечно лучше брать". He doubted the price — "160 я еще не уверен… это стоит во всех телефонах, значит, у нас просто неправильно соплаер." Genadi: it is a laptop module, not a phone one ("модули, которые используются в лэптопах"), and he wants to research the market. [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- **Val's pressure.** "мне нужно выставлять машины", and he had already written the quantities. [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- **A USB stick that flashes the modem firmware.** Genadi and Pavel had agreed about an hour earlier that Pavel will prepare a USB stick: plugged into the machine, it upgrades the modem firmware automatically, because bought modules come with different firmware — "мы покупаем… мы не знаем, что там стоит, какой [firmware], они все продают с разными." It speaks to the firmware-mismatch cause named on Sept 4 (inference). [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]

*(Derived-notes check: the notes put the count at "about 8–10, unclear" and Val's figure at $160 against Genadi's $150; the wiki records the count as garbled and both prices as spoken.)* [[raw/Meeting_Notes_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]

## Sept 30 2026 — the supply picture: 100 asked for, 5 or 10 offered, 1,000 minimums, end-of-life models, about 30 more on order, and code written for one model

At the [[wiki/meetings/2026-09-30-transactional-mvp1-instructions-complete-and-modem-supply.md|Sept-30 8:03 AM MVP 1 call]] (Russian) [[wiki/people/alexander-biratka.md|Biratka]] asked the question nobody had answered: "GSM модемы у нас будут какого?… какой модели у нас будет 2 возможных подключённых или один всётаки. Никто не знает." [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]

- **The model in the code today.** [[wiki/people/andrey-bosik.md|Bosik]]: "Паша мне сказал что будет [кьюн какой то там адем]"; [[wiki/people/pavel.md|Pavel]]: "Квеэл вектелл" — a maker's name, **garbled** in both mouths (the derived notes read it as Quectel [[raw/Meeting_Notes_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]). Bosik's point: "разные модемы поразному в операционной системе определяются какието определяются как USB какието как в лан какието как ещё чтото и я сейчас пишу конкретно под вот этот который ты паше говорил" — modems show up differently in the OS, so his code is written for that one model.
- **Genadi and the suppliers.** Pavel: "гена активно работает с поставщиками [sere virles]" (a supplier name, **garbled**; the notes read Sierra Wireless), "потому что когда начали, реально вышли на рынок и сказали, **нам надо 100 модемов**. То ктото говорит не у нас только 5 или у нас только 10. А ктото говорит 1000 мы с вами не работаем, вы слишком маленькие для нас." [[wiki/people/genadi-peari.md|Genadi]] is working out which models that supplier will offer.
- **New models, most likely.** "скорее всего, нам придётся вообще какието абсолютно новые модели брать, потому что… те, с которыми мы работали до сих пор. Они уже [end of life]. Они уже давно перестали их производить, это продаются какието остатки." Biratka: new modems must be tested "чтобы они работали, это такая важная часть"; Pavel: "это относится и к игровым машинам, и к [транзакшн] продукции."
- **Georgia's stock and Val's order.** [[wiki/people/andrei-klimovich.md|Klimovich]]: "у нас в джорджии вообще было только 10 этих модемов… 10 инсталляций мы сможем сделать, причём это 10 игровых машин и 10 транзакционных устройств" (as spoken); "у нас нету пока заказов на новую партию?" Pavel: "в джорджии [Вал давал]… [в] команду купить помоему 30 новых. И они сейчас как раз покупаются" — about 30 more, "[т]акие же да как первые 10" — "Да да да" — the same, outdated, model; "параллельно… идёт работа над тем, чтобы всётаки выйти на те, которые [up to date]."

This continues the Sept-24 line that LTE is hard to buy and Genadi researches the market (his commitment below stays open — the work is reported as ongoing). The modem the Sept-4 and Sept-14 updates argue over is not named here either.

### Open questions (Sept 30 2026)

- Which modem model goes forward, and will a device carry one or two? Nobody knows; Genadi is with the suppliers; Bosik's code targets the one model Pavel named — [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]

## Update, Oct 1 2026 — one SIM for the whole Minsk team; KORE said "no problem" to more and nothing followed; the contract covers every US state; Klimovich picks it up

At the [[wiki/meetings/2026-10-01-transactional-mvp1-status-slice-and-sas-command-logging.md|Oct-1 8:02 AM MVP 1 call]] (Russian) the SIM, not the modem, was the shortage [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]:

- **One SIM.** [[wiki/people/andrey-bosik.md|Bosik]] needs a SIM in a terminal to test his firewall change; [[wiki/people/pavel.md|Pavel]]: "Симка сейчас у Ивана… тестируется. Как работает [gom в 3] с модемом" — not today. [[wiki/people/dmitri-chudinov.md|Chudinov]]: "может мы както подымем себе тему и заведём ещё симки, а то живём с большой семьёй на одну."
- **The KORE request.** [[wiki/people/andrei-klimovich.md|Klimovich]]: "Павел, ты инициировал вопрос кору о том, чтобы они выслали нам в Минск дополнительную партию симок, и они сказали no problem. Ну дальше дальше конкретика не пошла." Pavel: "Да… с с нашей стороны мы должны запросить там, пришлите нам или что?" Klimovich: "Давай я подхвачу эту беседу… запрос на симки в Минск, давайте я подниму." Bosik: his own unanswered email on it "не актуально" — Klimovich will not chase it.
- **Where the SIMs may be used.** Pavel: "С ними же договор только на работу в штате Джорджия правильно или?" Klimovich: "**Договор на USA на все Штаты там ограничения нету по Штатам. Если иностранные государства хороший вопрос.**" Bosik: ideally test with a KORE SIM ("коровскую"), "а здесь коровская симка или здесь нашего местного" — whether Minsk's SIM is KORE's or a local one is not answered.
- **Traffic.** Pavel offered his own modem's SIM "ненадолго, а то чтоб там большой трафик не уходил на неё"; "трафик, он должен быть копеечный, за исключением кейсов, когда идёт обновление прошивок." Bosik will wait for Ivan's.

("кору" / "коровская" is read as KORE — the derived notes read it the same way [[raw/Meeting_Notes_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]. Val's Sept-4 commitment to email KORE on modems and the APN is a different thread and was not mentioned.)

### Open commitments (Oct 1 2026)

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — pick up the request to KORE for an extra batch of SIM cards for Minsk, which stalled after KORE's "no problem" — due unspecified ("подниму") — [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]

### Open questions (Oct 1 2026)

- Can KORE SIMs be used outside the United States (in Minsk)? The contract covers all US states; abroad is "хороший вопрос" — [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]

## Open commitments (Sept 14 2026)

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — order modems from KORE now: two samples, M.2 and mini-PCIe — due as soon as possible; nothing deploys until the modem works — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] and "Андрей" (unresolved, §4) — put the same SIM cards into the Flex units and establish whether the fault is the SIM or the modem — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — prepare a USB stick that, plugged into a machine, upgrades the modem firmware automatically — due unspecified (agreed with Genadi on Sept 24, as Genadi reported) — [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — research the LTE / 5G module market and prices, working with the Chinese suppliers — due unspecified ("сегодня опять") — [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]] — *Sept 30 2026: ongoing — "гена активно работает с поставщиками"; the market answered 5, 10 or a 1,000 minimum to a request for 100* — [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — email KORE: which modems do they recommend, and will they supply the modem configuration parameters and the APN — due right after this call — [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]] [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — order the North-America-variant modems (~$16 on Amazon) and ship them to Georgia — due within about two days — [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]] [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [ ] [[wiki/people/elizabeth.md|Elizabeth Palomino]] — install the replacement modems in Georgia when they arrive — due on arrival — [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — upload the software remotely to the new modems and verify they hold a connection; if a good modem does not work on the existing software, connect remotely and find the cause — due after installation — [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — rework the antenna placement so the antenna sits in an opening rather than glued to the metal enclosure — due unspecified — [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]] [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]

Val's own undertaking from this call — to check his message history for when he first asked for the modem work, rather than assert the timing from memory — sits on [[wiki/people/val-levitan.md]].

## Open questions

- 5G or LTE for the machine modem, and is ~$150–160 a real market price for a 5G module? Val: take 5G if it works better at locations. — [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- Does the second modem version now going into the Georgia units behave any better than the first? Genadi reported **two types, five of each** received, with the second version going in for Pavel to look at. *(The transcript renders the count as "22 вида модемов по 5 штук"; the derived notes read it as two types of five, which is what is recorded.)* — [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]] [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- Will KORE supply modem recommendations and the APN? That answer decides between buying new hardware and reconfiguring what is already in the field — [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]

**§15.8:** clear — component pricing (~$16 per modem) and vendor/carrier economics only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- [[raw/Meeting_Notes_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]
