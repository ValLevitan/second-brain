---
type: decision
title: The Georgia LTE modem failure is treated as a source-and-firmware mismatch — buy the North-America variant and, in parallel, ask KORE for the recommended modems and the APN
date: 2026-09-04
aliases: [7455 modem, modem firmware mismatch, North America modem variant, KORE APN, ask KORE which modems, AliExpress modem Minsk, $16 Amazon modem, two antennas on the module, antenna in an opening]
source-count: 4
status: active
open-commitments: 7
open-questions: 2
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

## Open commitments (Sept 14 2026)

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — order modems from KORE now: two samples, M.2 and mini-PCIe — due as soon as possible; nothing deploys until the modem works — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] and "Андрей" (unresolved, §4) — put the same SIM cards into the Flex units and establish whether the fault is the SIM or the modem — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Open commitments

- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — email KORE: which modems do they recommend, and will they supply the modem configuration parameters and the APN — due right after this call — [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]] [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — order the North-America-variant modems (~$16 on Amazon) and ship them to Georgia — due within about two days — [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]] [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [ ] [[wiki/people/elizabeth.md|Elizabeth Palomino]] — install the replacement modems in Georgia when they arrive — due on arrival — [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — upload the software remotely to the new modems and verify they hold a connection; if a good modem does not work on the existing software, connect remotely and find the cause — due after installation — [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — rework the antenna placement so the antenna sits in an opening rather than glued to the metal enclosure — due unspecified — [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]] [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]

Val's own undertaking from this call — to check his message history for when he first asked for the modem work, rather than assert the timing from memory — sits on [[wiki/people/val-levitan.md]].

## Open questions

- Does the second modem version now going into the Georgia units behave any better than the first? Genadi reported **two types, five of each** received, with the second version going in for Pavel to look at. *(The transcript renders the count as "22 вида модемов по 5 штук"; the derived notes read it as two types of five, which is what is recorded.)* — [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]] [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- Will KORE supply modem recommendations and the APN? That answer decides between buying new hardware and reconfiguring what is already in the field — [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]

**§15.8:** clear — component pricing (~$16 per modem) and vendor/carrier economics only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
