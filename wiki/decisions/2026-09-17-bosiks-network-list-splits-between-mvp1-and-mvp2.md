---
type: decision
title: Bosik's network list is split requirement by requirement — the remote FlexPort master goes to MVP 2, and a USB stick does the job until then
date: 2026-09-17
aliases: [capability 144, capability 91, capability 141, requirement 1410, requirement 1411, requirement 1413, requirement 1418, requirement 1421, requirement 1431, requirement 1030, watchdog, FP10, MVP2 parking capability, placeholder capability, orphan requirements, обновляем 3000 машин с флешки, сиротливые реквайрменты, our reuse bucket, router approved in the United States, gateway replacement loses tickets]
source-count: 2
status: active
open-commitments: 4
open-questions: 3
---

# The network list is split item by item, and the remote FlexPort master leaves MVP 1

The second half of the [[wiki/meetings/2026-09-17-transactional-mvp1-skillpay-multi-product-and-device-network-security.md|Sept 17 2026 8:02 AM call]] (Russian) walked [[wiki/people/andrey-bosik.md|Andrey Bosik]]'s network and security document line by line, with [[wiki/people/irina-shishko.md|Irina Shishko]] driving the list and [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] ruling on each item. The firewall item that survived the sweep has its own page ([[wiki/decisions/2026-09-17-the-device-does-the-routers-job-firewall-nat-and-wan-lan-profiles-stay-in-mvp1.md]]); so does the route-priority item ([[wiki/decisions/2026-09-17-lte-is-the-default-route-and-the-manual-override-stays.md]]) and the signal-telemetry item ([[wiki/decisions/2026-09-17-signal-quality-in-mvp1-means-remote-visibility-not-a-screen.md]]).

## The headline — six FlexPorts off a USB stick is acceptable

**Capability 144** is, in Bosik's own description, a master that lets the Flex-Ports "**отправлять их телеметрию, обновлять их ф[ё]рв[а]ры и идентифицировать их как[-]то… в клауде**" — send telemetry, update their firmware, and be identified in the cloud. [[wiki/people/pavel.md|Pavel Frolov]] had moved it up into MVP 1 before the call: "**я это [капабилити] перенёс вверх и поставил ему MVP один**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

**Irina's argument is what turned it.** Bosik put the pain as "**6 игровых машин — это что[,] в 6 флекс[]портов пойти с флешки обновить? Ну это такое себе удовольствие**". Irina answered from the installed base: "**Обновить можно из флешки[,] 6 штук — это не проблема[;] мы 3000 машин обновляем с флешки**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

Klimovich's one correction sharpened rather than weakened it: "**обновляем не мы[;] обновля[ют] те техники владельцев машин**" — JVL is not the party walking round with the stick, the machine owners' technicians are — and he accepted it: "**[MVP] один согласен, это мы переживём**". Irina closed it: "**значит, убираем на MVP 2 и поехали дальше**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

**The condition attached is about logging, and it is the substantive part of the ruling.** Klimovich: "**нам просто надо [иметь] уверенность, что в [MVP] один вы будете видеть всё, что может быть связано с… не работает устройство[,] чтобы хотя бы была информация, что надо ехать с этой флешкой**" — MVP 1 logging must still be good enough to tell that a device is down and that somebody has to drive out to it [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

This reverses half of the [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md|Sept-14 firmware ruling]] — see the dated update there. **Flex IQ still updates itself in MVP 1**: asked directly, [[wiki/people/dmitri-chudinov.md|Chudinov]] said "**IQ в [MVP] один будет обновляться**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

## Where capability 144 itself ended up is left ambiguous on the recording

Irina's "**убираем на MVP 2**" is unambiguous about the *firmware-update* content. But the capability was then **thinned** rather than emptied — Bosik twice proposed "**прор[е]дить**" it (thin the rows out), several of its requirements were moved to the MVP 2 parking bucket during the call, and after the requirement-1410 exchange Bosik said of what was left "**144, окей, поехали следующий, то есть это идёт в MVP один**", to which Klimovich answered only "**Угу**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

**The source ends without a clean statement of capability 144's own fix version.** The derived notes assert flatly that "capability 144 … goes back out to MVP2" [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]; the transcript supports that for the remote-update content and contradicts it for the thinned remainder. **Recorded as unclear, not resolved either way** (open question below).

## The item-by-item result

| Item | What it is, as described on the call | Where it went |
|---|---|---|
| **Capability 144** | master for FlexPort telemetry, firmware update, cloud identification | remote firmware update → **MVP 2**; the capability's own label left ambiguous (above) |
| **Capability 91** | already delivered — "**сам кап 91 он выполнен**" | stays; **fix version was missing and Bosik set it live on the call**, at Irina's request, "чисто добавить версию" so the release contents are visible |
| **Requirement 1410** | Flex-Ports do not appear on the dashboard at all — "**в дэш[]борде вообще не показываются, не существуют**" | **Klimovich took it for the portal dashboard** he is building. He separately said the *device* screen can wait: "для MVP один переживём, если там их не будет показываться" |
| **Requirement 1411** | buffer FlexPort events when there is no signal; collect FlexPort telemetry and send it to Grafana | left with the logging work; Chudinov has no picture of it yet (below) |
| **Requirement 1413** | deliver updates via a master node, storing firmware where the Flex/kiosk images already live | **MVP 2** — Klimovich: "давай его [MVP] 2 в дамп закину пока… прилинкую к нашему этому паркингу" |
| **Requirement 1418** | no JVL device is a gateway for another; each reaches the internet through its own modem | **MVP 2** — in MVP 1 "**у нас только один гейтвей… и всё это — айкью**" |
| **Requirement 1421** | replacing the gateway (one Flex IQ swapped for another) at a location | **MVP 2**, with the risk accepted (below) |
| **Requirement 1431** | PIN-entry timeout | off Flex IQ entirely → **MVP 2 parking, and to be attached to FlexPay** (below) |
| **Requirement 1030** | the watchdog | **MVP 2** for kiosks and Flex IQ (below) |
| **Routers** | must be models "**одобренны[ми]… которые продаются в Соединённых штатах**" — approved and sold in the United States | stays; Bosik owns the choice and named tomorrow |

## Three of those need their own sentence

**Requirement 1418 — why it had to be settled at all.** Bosik: "**важно решить, потому что тогда возникает[:] кто D[H]CP сервер, кто какие шлюзы, кому даёт**". Pavel expected the master question to land "**на 2 или на 3 [MVP]**". Chudinov insisted the question is really two questions: "**разделяй бизнес[-]логику — через кого создать [е]волет или там транзакции — или через кого слать графа[ну], логи, секреты, бандлы, обновления… Это очень большая разница**". Klimovich resolved it for now by scope: in MVP 1 there is exactly one gateway and it is the Flex IQ; the DHCP/master question only arises with an IQ plus one or more kiosks [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

**Requirement 1421 — a known loss, knowingly deferred.** The case is one Flex IQ replaced by another at a location. Pavel: "**сейчас мы не синхронизируем эти самые тикеты… и по факту потеряются все тикеты, которые были выпущены**[,] но не отоварены" — every issued-but-unredeemed ticket is lost. Klimovich: "**если речь про это, то это в [MVP] 2 уезжает. Мы понимаем эти риски**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]. *(The derived notes list 1421 only as an orphan requirement with no capability and do not record what it is about or the accepted loss.)*

**Requirement 1030 — Val's watchdog rule, and why it does not fit.** Pavel identified it as a universal rule: "**Это универсальное требование для всех устройств. То, что вал тоже говорил, что во[тч]дог должен быть во всех устройствах. Если он вешается, он должен выходить в ребут и загружаться с нуля**". It is done on the gaming machines, but "**тут описание конкретное для фп 10[,] оно не подходит для IQ**" — the text is written for the FP-10 and does not transfer. *(Klimovich asked "**FP 10 это что?**" and the recording contains no answer; the conversation moved on.)* Klimovich parked it: "**в MVP один для IQ… ничего не будет связанного с во[тч]дог[ом]… но в MVP 2 и для киосков, и для IQ хотелось бы… заняться этой задачей**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

## Requirement 1431 does not belong on Flex IQ at all

Chudinov stopped the meeting to say so: "**я говорил, что 14[ ]31 — это ж время ввода пин[-]кода… за[че]м флекс[у] айк[ью] время ввода пин кода, если его там нет?**" His reading of what it actually covers: "**речь про пин[-]код[,] ожидани[е] времени ввода пин[-]кода на флекс[]порте, чтобы подтвердить, что это твой [е]волет**" — the wait for a PIN **at the Flex-Port**, to prove the wallet is yours. And where PINs do exist: "**на флекс[]пей у нас есть создание пин[-]кода; на флекс[е] [ай]к[ью] пин[-]кодов нету**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

Klimovich accepted both halves — "**это не M[VP] один**" and "**я поме[тил] 14[ ]31[;] я ему найду дом в MVP 2, чтобы он не болтался без [капа]билити**" — and Chudinov repeated the second half so it would not be lost: "**его надо привязать к fl[e]xpay**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

*(1431 was one of the requirements already pushed out of MVP 1 the previous day — see [[wiki/decisions/2026-09-16-anything-that-depends-on-the-cloud-leaves-mvp1.md]]. What is new here is the diagnosis of **why** it never fitted, and the FlexPay destination. Note also that earlier in this same call the team had linked 1431 to **capability 141** as "required by", which is the link Chudinov then objected to.)*

## The MVP 2 parking bucket — what Klimovich says it is, and what its number is not

Klimovich described creating it, with an apology in advance: "**Для [MVP] 2 на самом деле вчера я создал такой плейхолдер [капабилити]… за это наверное меня по рукам можно ударить, но всё[-]таки реальность другая[:] я туда скидываю вот как раз такие сиротливые рек[вайрменты]. Мы, когда займёмся [MVP] 2, мы всё равно всё будем грумить, приводить в порядок. И вот это наш бакет[,] переиспользован[ие]**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

**Its number is still not established, and this recording does not establish it either.** The only number spoken about it is Irina reading a note off the screen: "**там что[-]то написано[:] 14[ ]31 привязать кап 151[,] но он привязан к кап[,] там что[-]то 170 с чем[-]то**" — attached to a capability "something in the 170s". Klimovich confirmed only the function: "**Я уже привязал его[;] это вот наш паркинг для [MVP] 2**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]. The corpus carries **177** as provisional and explicitly not established ([[wiki/decisions/2026-09-16-anything-that-depends-on-the-cloud-leaves-mvp1.md]]); "something in the 170s" is consistent with it and proves nothing. **Not resolved.**

**A second uncertainty on top of that.** On Sept 16 Klimovich said he had created the MVP 2 **cloud** capability "yesterday" (Sept 15); here he says he created the **placeholder/parking** capability "yesterday" (Sept 16). Whether that is one capability doing both jobs or two separate ones is not stated anywhere in this source — see the open question below and the update on [[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]].

## Where the Flex-Ports can already be seen

Chudinov pushed back on the idea that nothing shows the ports today: "**на IQ терминале[,] в сетапе[,] в списке [флекс]портов будут показаны и те, что подключены, и те, что в сети**", and when Bosik read that as configuration-time only, he corrected it — "**в сетапе[,] в смысле[,] не режим кассира, а режим мастера[:] заходишь и смотришь[,] там будет вкладка девайс[:] есть л[]т[]е модем, а есть флекс[]порт[ы]**", listing everything present on the network. He added that **Sergei** is finishing the function to re-attach a Flex-Port to the terminal and that the requirement for it is already written [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]. *(§4: this "Сергей" is a developer on Pavel Frolov's Flex IQ side. He is not resolved to any Sergei already on file — neither [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] nor [[wiki/people/sergei-novitsky.md|Sergei Novitsky]] fits the context cleanly — and is deliberately left unresolved rather than forced.)*

Bosik's use case for wanting it visible is a field one: a technician arrives, opens the menu, "**я вижу здесь 5… а у него 6 должно быть портов… сфоткал их… на телефон и пошёл просто по серийникам нашёл, какой из 6 портов отвалился[,] на какой машине**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — choose the router model, approved and sold in the United States, and name it so a couple can be ordered from Amazon in time — due **tomorrow** (Sept 18 2026); he said "на завтра" — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — thin capability 144 down, removing the requirements that moved to MVP 2 — due unspecified; started during the call — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — link the orphan requirements 1431, 1030, 1413 and 1421 to the MVP 2 parking capability, and attach 1431 to FlexPay — due unspecified; 1431 and 1030 were linked during the call — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — take requirement 1410 into the portal dashboard work, so Flex-Ports and their serial numbers appear — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

## Open questions

- **What fix version capability 144 itself now carries.** Irina said "убираем на MVP 2"; after the capability was thinned, Bosik said of the remainder "это идёт в MVP один" and Klimovich only grunted assent. The derived notes assert MVP 2 flatly; the transcript does not settle it — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- **Whether the MVP 2 cloud capability and the MVP 2 parking capability are the same thing.** Klimovich describes creating one "yesterday" on both Sept 16 and Sept 17, for two different purposes, and no number is confirmed for either — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- **Whether a Flex IQ or kiosk may ever act as a router for the Flex-Ports.** Requirement 1418 says no device is a gateway for another, but Pavel asked "**а вдруг захотим сделать его маршрутизатором для флекс портов?**" and Bosik answered only "**ну тогда я переписываю**" — the question was left open — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**§15.8:** clear — Jira scope, device behaviour and field-service logistics only; no named person's pay, rate or performance judgement appears. **§15.9:** no serial number, licence number, credential or address value is stated anywhere — serial numbers are discussed as a *category* the technician would read off a screen, and none is quoted.

## Sources

- [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
