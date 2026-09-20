---
type: decision
title: The device has to do the router's job — firewall, NAT and WAN/LAN profiles stay in MVP 1, and the traffic bill is the argument that settles it
date: 2026-09-17
aliases: [requirement 1556, device network security, firewall on the device, NAT, WAN LAN profiles, public private profile, advanced firewall, DDoS protection, ping from the internet, bots pinging the device, CloudFront hides our IPs, dynamic IPs, мы платим за мегабайты, хороший счет за трафик, no router in front of the device, Claude writes the firewall, branch and pull request]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# The operating system has to do what a router does — and it stays in MVP 1

Raised in the first two minutes of the [[wiki/meetings/2026-09-17-transactional-mvp1-skillpay-multi-product-and-device-network-security.md|Sept 17 2026 8:02 AM call]] (Russian) by [[wiki/people/andrey-bosik.md|Andrey Bosik]], argued again at the end, and confirmed into MVP 1 by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] in the last four minutes. The requirement is **1556** — the number [[wiki/people/irina-shishko.md|Irina Shishko]] read off the screen as "15, 56", sitting under capability 144 [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]. *(Bosik once read the same line back as "2056"; that is a misreading of his own note and is not used. The ID is recorded as Shishko spoke it, with this caveat.)*

## The problem in one sentence

Every JVL transactional device looks straight at the internet through its own LTE modem, with nothing in front of it. Bosik: "**через л[]т[]е модем сам[о] устройство… смотрит в интернет, то есть нет маршрутизатора, нету на[т]о, нету файрвола на этих маршрутизаторах, то есть нам на самой операционке… надо, чтобы работали вещи, которые обычно выполняет маршрутизатор именно с точки зрения секьюрити. То есть это файрвол, это на[т]о. Профили — у нас будет ва[н]/ла[н] профиль**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

This is the direct consequence of the architecture fixed two days earlier — every device carries its own modem and SIM ([[wiki/decisions/2026-09-15-every-device-carries-its-own-lte-modem-and-sim.md]]) and no device is a gateway for any other ([[wiki/decisions/2026-09-17-bosiks-network-list-splits-between-mvp1-and-mvp2.md]]). There is no shared router to hide behind because there is no shared route.

## Why it cannot be solved on the carrier's side instead

[[wiki/people/pavel.md|Pavel Frolov]] proposed the obvious alternative first — ask **KORE**, the SIM provider, whether their network can confine the devices to JVL's own hosts: "**у них какие[-]то настройки внутри сети есть[;] возможно, что там можно как[-]то ограничить, что наши девайсы работают только… в наших… сетях**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]. *(The transcript renders the provider as "кор"/"корни"; Klimovich identifies it as "сим карта, которую мы будем устанавливать" — the SIM JVL is installing — which is KORE, already established in the corpus, see [[wiki/decisions/2026-09-04-north-america-modem-variant-and-ask-kore-for-the-apn.md]].)*

**Bosik closed that route on the spot, and the reason is JVL's own cloud shape:** "**у клауда[,] Паша[,] миллиард IP адресов, и они динамические. Притом мы используем ещё кл[ауд]фронт, котор[ый] скрывает наши реальные IP адреса, то есть симки должны видеть весь интернет по факту**" — the cloud has an enormous, dynamic address range, and CloudFront sits in front hiding the real addresses, so the SIMs have to be allowed to see the whole internet. An allow-list at the carrier is therefore not available, and the hardening has to happen on the device [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

*(This passage is the strongest architectural fact on the recording and it is **absent from the derived notes**, which record the firewall decision without the reason it is unavoidable.)*

## What is actually being asked for

Bosik's fuller description, later in the call [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]:

- **Two interface profiles** — "**2 профиля[,] ва[н]/ла[н] профиля, ну или там public[/]при[ва]т… как угодно их назовите**" — so the device knows "**какой стороной он смотрит в интернет, какой в сети**", which side faces the internet and which faces the local network.
- **A basic firewall on the internet-facing side** — "**базовая[:] это ф[айрвол], котор[ый] разрешает какие[-]то порты внутри сети[,] какие[-]то… в интернете эти порты запрещает**".
- **NAT** — "**на[т], которые транслируют адреса**".
- **Some "advanced firewall" minimum** — "**защита от де[]дос[ов], от пингов… вот таких нехороших вещей**".

Klimovich asked what exists today and got a plain answer: "**Всего этого сейчас нету**" — none of it — and Bosik agreed: "**Я и предполагаю, что наверно нет**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

## The argument that decided it — not security, cost

Klimovich asked which part is "**самая критическая… без чего вообще нельзя выходить наружу**" — what cannot ship without. What settled it was Bosik's money argument rather than a threat model [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]:

> "**самая простая штука, которая случается всегда — это если устройство пингуется из интернета… его начинают просто боты бесконечно пинговать, и у тебя как минимум объём трафика вылетает на мобильном интернете… у нас там[,] Андрей[,] не анлим на этих сим картах**"

Klimovich confirmed the billing model — "**Мы платим… за килобайты там или за мегабайты**" — and Bosik landed it: "**если он будет пинговаться, у нас будет хороший счет за трафик**". Klimovich closed immediately: "**Всё, всё, мы решили, оставляем в [MVP] один**" — which the derived notes record as the decision "Firewall, NAT and WAN/LAN profiles on the device stay in MVP1" [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

Earlier in the same exchange he had already said "**Окей, тогда это в MVP один**", with Bosik answering "**я считаю, что да, целиком**" — the whole of it, not a part [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

## How it gets built — and the worry about breaking the OS

Bosik does not want to write it by hand and does not want to own the operating system if it breaks. His proposal: "**могу я попросить в паш[ин]… репозитории, создам, наверное, ветку и попрошу потом сделать по[л]л[ ]реквест; вот либо Паша сам может попросить [Клода] это сделать, я не знаю как лучше поступить… потому что я боюсь сломать операционн[ую систему]**" — Claude writes it into [[wiki/people/pavel.md|Pavel]]'s repository as a **branch and a pull request** [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

**Testing it is the open problem, and nobody claimed to have an answer.** Pavel: "**Я не представляю, как это протестить**". Three ideas were floated and none was adopted [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]:

- [[wiki/people/dmitri-chudinov.md|Chudinov]] — have the assistant attack it: "**будем умолять Клод[а] ломать и искать уязвимости**"; Klimovich backed the idea from the week's news — "**по последним новостям, они неплохо с этим справляются взломами**".
- Bosik — at minimum a code review that asserts the change actually closes the holes: "**хотя бы сделать проверку кода и сказать, что да, этот код действительно закрывает нас от уязвимостей**".
- Chudinov — the honest version of the test: "**Для честного теста я бы сделал тот, который с изменениями и без[:] сможет он всё-таки сломать или нет**" — run the attack against a build with the changes and one without, and compare.

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — get the firewall / NAT / WAN-LAN-profile work written by Claude into Pavel Frolov's repository as a branch and a pull request (requirement 1556, MVP 1) — due with MVP 1; no date set — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

## Open questions

- **How the firewall change gets tested without breaking the operating system.** Pavel said outright he does not know how; the ideas floated (have Claude attack it; a code review asserting the fix; comparing a build with and without the change) were discussed and none was chosen or assigned — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**§15.9 — checked explicitly, because this is a security session.** No credential, key, certificate, token, APN, SIM identifier, IP address or port number was spoken anywhere in this material. The whole discussion stays at the level of *categories* — firewall, NAT, WAN/LAN profile, ping, DDoS — and the one address-related statement is that JVL's cloud addresses are numerous and dynamic and sit behind CloudFront, with no value given. Nothing required routing to the Corporate Registry, and nothing was redacted.

**§15.8:** clear — platform and traffic economics only (the per-megabyte SIM billing model is product/platform economics, not a person's pay). No named person's compensation or performance judgement appears.

## Sources

- [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
