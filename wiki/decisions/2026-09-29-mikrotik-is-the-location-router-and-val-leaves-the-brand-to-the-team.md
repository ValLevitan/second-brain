---
type: decision
title: MikroTik is the location router — Linksys will not boot without internet, Netgear cannot be tested in Belarus, and Val leaves the brand to the team under his "no Chinese equipment" rule
date: 2026-09-29
aliases: [MikroTik router, микротик, Linksys does not boot without internet, Netgear not in Belarus, TP-Link routers used now, no Chinese equipment, китайским оборудованием, everything is made in China today, $40 to $100 router, router plus switch, switch brand, PoE switch, power over Ethernet for the ports, можем с микротиком дальше двигаться, они в состоянии решать эти вопросы, router brand decision]
source-count: 2
status: active
open-commitments: 1
open-questions: 2
---

# MikroTik is the location router; Val leaves the brand to the team

Settled at the end of the [[wiki/meetings/2026-09-29-transactional-mvp1-setup-instructions-and-mikrotik-router.md|Sept-29 8:06 AM MVP 1 call]] (Russian). [[wiki/people/andrey-bosik.md|Andrey Bosik]] brought the report, [[wiki/people/val-levitan.md|Val]] set the constraint, and [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] closed it [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]].

**What it decides.** The external router at a transactional location — the one specified on [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]] and to be tested under [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] — is a **MikroTik**. Bosik picks a model and tests it in Minsk.

## Bosik's report

He had looked at what home-class routers are available ("маршрутизаторов мы обсуждали… там туда сюда 5 10") [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]:

- **Linksys is out.** "Линксист не подойдёт" — it is a Cisco sub-brand for the home segment, and "лимсисты не подымаются без наличия интернета" — it does not come up without an internet connection. He knows this from his own use (not recorded further).
- **That leaves Netgear or MikroTik.** "у нас остаётся выбор, либо нет гиргир, либо микротик." Netgear "в Белоруссии особо не купишь, и если с нетгиром будут какието проблемы, то мы не сможем здесь его протестить" — it cannot be bought in Belarus, so it cannot be tested there. "Вот поэтому остается, по сути, микротики."
- **The MikroTik caveat.** "они как бы компания… Зарегистрирован в литвеле в Латвии. Я точно не помню где… но производство понятно, что всё равно китайское. Скорее всего" — registered in Lithuania or Latvia (he did not remember which), production most likely Chinese, and whether sanctions will ever touch them "большой вопрос". *(On Sept 7 he had said "Литва" — see the Sept-7 decision. The country is inconsistent in the sources; both are recorded as spoken.)*
- **His first suggestion was to not bother.** "просто поставить, как вот ставили там те это полинки" — keep the TP-Link routers in use now — "потому что, как сказал мне клод[,] [в]сё, что куплено до введения какихто документов считается как бы куплено в разрешённом… [п]о законодательству" — his AI had told him that equipment bought before any restriction counts as lawfully bought.

## Val's constraint

"**Мы не можем пользоваться китайским китайским оборудованием. Это… будет дисконтен по в Америке**" — JVL cannot use Chinese equipment; the last word is garbled and is read as "discontinued" (**inference**). Bosik asked how MikroTik, a European company with Chinese production, looks "в перспективе". Val: "**Я думаю, что сегодня всё производится в Китае**" [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]. This restates the Sept-7 rule that router brands must be American or allied ([[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]]) and the Sept-9 "No Chinese manufacturer… stay away from Cisco" ([[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]]).

## Why MikroTik, and what it costs

Bosik: "Давайте тогда остановимся на микротиках" — it can be bought in Minsk, so "я микротик здесь подключу посмотрел потестил", and if JVL wants to add features he can make a config and roll it out to the routers. Val asked the price: "самый простой там в районе долларов 40"; later, "от 40 до $100… в зависимости от возможности" — like any home-use router. Val did not know the brand ("Я не слышал никуда такого названия"); Bosik: a maker like Cisco, Linksys, TP-Link and D-Link (as spoken, "пылинк дэлинг"), well known in IT though "не как циска", and he posted the name in the chat [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]. [[wiki/people/pavel.md|Pavel]] asked whether the Wi-Fi has an external antenna; Bosik: a line of about a thousand devices, any form can be found [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]].

## The ruling

Klimovich: "По поводу всётаки роутера нам надо принять решение… Вал за вами вопрос… вам надо подумать и решить." Val: "**Что мне надо решать, они в состоянии решать эти вопросы.**" Klimovich: "если вы не против микротика…" Val: "**Я же сказал что я… сколько раз надо говорить. Я же сказал чётко.**" Klimovich: "**Окей Андрей, тогда можем с микротиком дальше двигаться.**" Bosik: "Да, хорошо" [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]. The derived notes read Val's lines as "the team can decide this, and he had already said it clearly" [[raw/Meeting_Notes_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]].

**Who decided (inference).** Val did not name the brand. He set the constraint and refused the choice; Klimovich and Bosik made it. Recorded as a team decision under Val's rule.

## A switch as well

Klimovich asked whether the router should take ten connections directly "или мы будем через свич какойто работать". Bosik: routers usually have four ports, newer ones three; the model is "воткнули кабель интернет… выткнули кабель сетевой в какойто коммутатор и всё оборудование подключается к коммутат[ору]". Klimovich: so a switch is needed too, laid out neatly "и не надо было 100 500 кабелей". Pavel: the same switch model should be picked in Minsk, because [[wiki/people/dmitri-chudinov.md|Chudinov]] once had devices that did not see each other through a switch — Chudinov: he built a local network and "на обычном [switch]… не заработала, не видел девайсы друг друга и надо будет разбираться, почему". Bosik: a switch is a simple thing and the brand matters less, but if it must be bought in Belarus it should be a maker sold there and "не китайские… А у нас наверное, все китайские, если честно" [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]].

## Power over Ethernet — future only

Pavel raised PoE switches ("коммутаторы, с которые раздают питание"; Bosik: "Есть 12… 24 вольта"): in theory the Flex-Ports could be powered from the switch rather than the machine, "[и] даже если выключают машину… наши порты оставались на связи". Bosik: the Flex-Port hardware would have to support it — "это аппаратная часть… на аппаратном уровне надо реализовать". Pavel: "Сейчас нет" — raised only so "если на будущее понадобятся какието [capabilities]… чтоб мы все знали про это". Price: Bosik, a PoE switch is "в 02:03 раза дороже обычного"; Pavel, from his own experience, "может быть на $5 дороже" [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]].

## What it changes

- The Sept-9 unassigned item "source and test routers from two different manufacturers, no Chinese brands, avoiding Cisco" now has a brand and an owner — see [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] (Sept-29 update). Only one manufacturer is chosen; the Sept-9 "two manufacturers" ask was not mentioned.
- The Sept-25 plan to connect borrowed machines "to the MikroTik" in the office (Klimovich) is consistent with this; the Georgia office router whose drops Bosik saw in his logs on Sept 22 is not named here.
- Capability 145 (Flex-Port Wi-Fi link) stays MVP 2 ([[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]], Sept-28 update); nothing here moves it.

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — go ahead with MikroTik: pick a model, buy and test it in Minsk, and prepare a config that can be rolled out — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]

## Open questions

- MikroTik's production is most likely Chinese; whether that conflicts with Val's "no Chinese equipment" rule was not settled beyond his "сегодня всё производится в Китае" — [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]
- Which switch model, and why Chudinov's devices did not see each other through an ordinary switch ("надо будет разбираться, почему") — [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]

**§15.8:** clear — vendor and brand selection and market prices only; no named person's pay, rate or performance. Two remarks about home equipment are not recorded. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]
