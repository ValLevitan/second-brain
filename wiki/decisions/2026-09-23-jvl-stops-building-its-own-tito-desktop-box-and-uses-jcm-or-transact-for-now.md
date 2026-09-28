---
type: decision
title: JVL stops building its own TITO desktop box for now — it connects JCM's or TransAct's to the IQ and offers both
date: 2026-09-23
aliases: [TITO desktop, DB9 serial connector, дебинайн, TransAct meeting Sept 24, тито десктоп, nobody needs it, никому не нужно, own TITO box stopped, GCM TITO desktop, TransAct TITO desktop, two options on IQ]
source-count: 5
status: active
open-commitments: 3
open-questions: 3
---

# JVL stops building its own TITO desktop box for now

Settled at the [[wiki/meetings/2026-09-23-texas-flex-slim-release-street-cabinet-and-bom-source-of-truth.md|Sept 23 2026 11:05 AM alignment call]] (Russian) between [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/genadi-peari.md|Genadi Peari]] [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]].

## What Genadi found

- He had started the review of the TITO desktop design ("А тито десктоп?… Я начал этим заниматься, то есть начал ревью") and saw large plastic parts — "это большие пластики, то есть это довольно дорого будет сделать это всё" [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]].
- So he checked the market first: "GCM и транзакт у них есть уже решение готовое… GCM у них есть это называется тито десктоп и у транзакта уже есть это тито дестоп". He had posted them in the chat. "Это помоему экзак ли то что?… То, что мы строим сейчас?" Val: "Абсолютно." [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]
- *(Reading: "GCM" is read as **JCM**, the wiki's established reading of that rendering — see [[wiki/organizations/jcm.md]]; "транзакт" is read as **TransAct**, the printer maker named elsewhere in the wiki. Both are inferences from the rendering.)*

## The ruling

- **Val: "Никому не нужно, никому не нужен, никому не нужен."** [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]
- **Short run: use the existing product; decide the long run later.** "если такие опции есть, то пока на короткий тираж я бы это применял бы. А дальше я бы сделал бы решение, как с ним, как с этим обходиться." [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]
- **Connect it to the IQ and offer two options.** "давайте это подключим к IQ и предложим 2 варианта или тот или тот." [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]
- **No development on JVL's own box — for now.** Genadi: "Девелопмен там не заниматься этого." Val: "Нет… до коробочки не заниматься нет. Пока." [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]
- **The reason, in Val's words:** "И деньги, и время самое главное. Нету время." [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]

## What JVL gives up

Genadi said JVL's own box would have been better: "она бы была более конвинента она бы принимала любой принтер. Потому что эти наверно будут только свои брать." He also thought TransAct probably holds much of the market. He agreed it is better not to put money in [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]].

## How it sits against Sept 14

On Sept 14 Val put the **TITO printer enclosure** in front of the street cabinet, to be 3D-printed then tooled in plastic ([[wiki/decisions/2026-09-14-tito-printer-cases-come-before-the-street-cabinet.md]]). *(Inference: the "TITO desktop" reviewed here is that same enclosure — both are a TITO printer in its own box next to the IQ. The Sept-23 source does not say so.)* If so, the own-design part of that work is now paused, while the other half of the Sept-14 ruling — start the street cabinet on the 23rd — held: the cabinet was started on this call. [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]

## Sept 24 2026 — Genadi meets TransAct; a standard DB9 serial connector agreed

On the [[wiki/meetings/2026-09-24-hardware-repo-bom-source-of-truth-and-street-cabinet-layout.md|Sept 24 4:38 PM alignment call]], in the street-cabinet agenda item, [[wiki/people/genadi-peari.md|Genadi]] reported a meeting with TransAct ("С транзактом мы сделали митинг") about the product (transcript "продукт dasto принтер тито" — read as their TITO desktop printer product; inference). [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]

- **How TransAct sells it.** "они продают только с новыми принтерами"; they have some stock now, and "в новом году там будет… Новый тип". [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- **How it talks to the IQ.** Val asked "как эти принтеры коммьюнике с нашим IQ?" Genadi: an ordinary serial link with a normal modem cable (transcript "Обычная расти сортир 33 проволочки, обычный на лмод кейбл"; the notes read it as RS-232; the wire count is garbled and not recorded). [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]] [[raw/Meeting_Notes_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- **A standard DB9 on JVL's side — agreed.** Genadi: the harness just needs preparing, but "если у нас мутогуз исчезла, я бы у нас поставил бы обычный дебинайн стандартный сериальный коннектор, чтоб всегда в него втыкали обычным модом кейбл." Val: "Хорошо договорились, вы можете сделать эту модификацию." *(The device that gets the DB9 is not named; by context it is the IQ side of this link, with "мутогуз" read as Mudagoose — both inferences. The derived notes put the DB9 on "the street machine"; the transcript does not say that.)* [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]] [[raw/Meeting_Notes_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- **The Georgia sample.** Genadi asked TransAct to sell one unit for the Georgia office; no answer yet — "там у них новый sales". He copied Val; Val had seen the email. [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]

## Open commitments

- [ ] Genadi Peari — get the documentation for connecting the JCM / TransAct TITO desktop to the IQ ("нету никакой документации, как там подключить к IQ") — due unspecified — [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]] — *Sept 24: TransAct's unit talks to the IQ over an ordinary serial cable (per Genadi); a JVL-side DB9 is agreed* [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- [ ] Genadi Peari — order a sample for Georgia ("какой то сам полна у Джорджия, чтобы привезли заказать"; Val: "Безусловно") — due unspecified — [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]] — *Sept 24: he asked TransAct for one unit for the Georgia office; no answer yet* [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- [ ] Genadi Peari — work out how to connect it to the IQ so the customer can be offered two options — due unspecified — [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]

## Open questions

- Which JVL device gets the DB9 serial connector, and does it replace the Mudagoose connection? The transcript does not say. [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- Who pays for the bought TITO desktop, and how is it priced — sold separately, or bundled with the maker's printer? Genadi: "Я не знаю кто за это платит сколько это стоит"; Val said he would not worry about it yet. [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]
- Will the bought boxes take only their maker's printer? Genadi thinks so; not checked. [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]] *Sept 24: TransAct sells its product "только с новыми принтерами" — only with new printers; whether it takes other makers' printers is still not stated.* [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]

*The derived notes call this "the most consequential finding of the call" and record it as a decision by Val on Genadi's market review [[raw/Meeting_Notes_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]].*

**§15.8:** clear — product and market only.

## Sept 25 2026 — the TransAct unit has "our Epic 950" inside, and Val approves Genadi's connector change

On the [[wiki/meetings/2026-09-25-transactional-mvp1-flexport-third-party-egm-compatibility-testing.md|Sept-25 8:05 AM MVP 1 call]] (Russian) [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]:

- **Klimovich pushed it.** "Это я написал письмо вал вам и геназию да, чтобы этот процесс двинуть… мы ждём какойто корпус там."
- **What TransAct has.** [[wiki/people/pavel.md|Pavel]]: the day before there was a meeting "с Геннадием и с производителем вот этих вот эпиков"; "У транзакта у них уже есть… принтер, который с корпусом уже, а внутри стоит наш эпик 950", with the power supply inside. They talked about how to order exactly that version as fast as possible. Val had met them too. Val: "У них уже готовый taybeltop" (read as table-top; **inference**).
- **Val's approval.** Val: "Геннадий хочет сделать небольшую поливозку на плате, чтобы поставить стандартный дебильной коннектор" — a small board change for a standard connector ("дебильной" read as the DB9 agreed on Sept 24 — **inference**). Val: "я дал санкцию… Этот вопрос практически закрыт."
- **With today's board.** Klimovich asked how to connect the printer now. Pavel: make a cable to the black 10-pin connector; "Скорее всего, надо будет перепаять 2 провода".

This moves the Sept-23 ruling on (use TransAct's or JCM's unit, not JVL's own box): TransAct's housed version is the one the team wants to order fast. Genadi's sample order stays open — no order is confirmed here.

## Sources

- [[raw/Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]
- [[raw/Meeting_Notes_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026.md]]
- [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- [[raw/Meeting_Notes_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]
