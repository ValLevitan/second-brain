---
type: decision
title: SAS is carried across from SMIB into Flex-Port and merged into the main branch, not polished in place — scope comes from Chudinov's existing command document; Alekseev starts over the weekend, and from Sept 7 2026 Pavel Frolov takes the larger part while Yavorsky is removed
date: 2026-09-04
aliases: [SAS on Flex-Port, port SAS from SMIB, merge into main branch, Chudinov's SAS command document, restore the environment first, no weekends, SAS AFT transactions, Monday 7 o'clock engineers meeting, Yavorsky on Monday evening]
source-count: 6
status: active
open-commitments: 3
open-questions: 2
disambiguation: "Status note: the core ruling (carry SAS across from SMIB, merge into main, scope from Chudinov's command document) stands and is active. The titular 'Yavorsky on Monday evening' element is DEAD — on Sept 7 2026 Val took tasks off Yavorsky and Pavel Frolov took the larger part of the SAS/AFT implementation. See the Update section."
---

# SAS is ported from SMIB into Flex-Port and merged into the main branch

The engineering half of the [[wiki/meetings/2026-09-04-flex-slim-first-ten-and-flex-port-sas.md|Sept 4 2026 midday call]] (Russian, 12:29–1:49 PM ET). [[wiki/people/val-levitan.md|Val]] asked a simple question — has SAS been done on Flex-Port? — and the answer took the rest of the hour. It follows directly from [[wiki/decisions/2026-09-04-flex-port-keeps-its-screen.md]].

## Where the work actually is

- **SAS is implemented on SMIB, not on Flex-Port.** [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], asked whether the protocol is implemented at software level: "Нет, на[ ]смиб сделан… сейчас значит на сми[бе] там реализована… базовая функциональность сас. И она согласована с этим [WSS]. Просто надо взять этот софт[вер] модуль из СМИ[Б], перевести во флэкспорт" — take the software module out of SMIB and carry it across to Flex-Port [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]. *(The protocol is spelled out by Alekseev as "дабл ю с. С." — W-S-S — and rendered elsewhere in the transcript as "дабл вис"; Val says "WS" once. Recorded as **WSS**, the protocol already established for this device family on [[wiki/topics/flexpay-business-architecture-payout-devices.md]].)*
- **It is not half an hour's work.** Val: "И эта работа на полчаса." Alekseev: "Ну не думаю, что на полчаса… на пару тройку дней наверное. Там надо еще Женю чтоб был" — a couple-three days, and [[wiki/people/eugine-yavorski.md|Eugine Yavorsky]] is needed [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].
- **What exists on Flex-Port today is a trade-show demo.** Yavorsky, brought onto the call: "на флэкспортах мы сделали демоверсию на базе железа флекс портов, а те, которые ты новые борты сделал, мы ещё даже не начинали ничего" — nothing has been started on the newer boards. The demo "для выставки была сделана… она там минимально функциональность имела… мы там даже чтото подправляли… по итогам этой выставки" — minimal functionality, with some fixes made after the show, and he was not sure what state it is in: "я не уверен, что она там, как сильно хорошем состоянии, но как минимум… какуюто коммуникацию делала" [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

## What was decided

- **Merge, do not polish.** Val's instinct was "Сейчас надо только ее отполировать" — just polish that version. Alekseev corrected him and Val took the correction: "Но не отполировать, скорее взять этот сас и добавить в основной этот мейн[-]бранч, ну то есть соединить" — take the SAS work and merge it into the main branch [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].
- **Scope comes from the existing command document, and is extended if short — not renegotiated.** Yavorsky wanted the scope narrowed first: "надо наверное с Павлом связаться, чтобы он… пытался поставить задачу[,] сузить немножко," because he does not know how large the protocol is — "весь его полностью… это будет там на год работы реализовывать." Alekseev refused that framing: "Не не сузить… сейчас нужно[:] есть документ, который делал… Дмитрий… И просто нужно, если этого недостаточно[,] просто чтоб дописали, какие ещё команды необходимо реализовать." Everything described in the document is already implemented — "Ну то, что было описано в документе, мы всё реализованы" [*sic*] — and if more is needed, "[пусть] Дмитрий или Павел добавил." Val adopted Alekseev's position [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]. The document is [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]'s.
- **The sequence Val laid out, step by step.** "восстановить [development environment]… потом мы говорим найти документ, который был опубликован Димой Чудиновым, которые, скорее всего, находятся в [Конфлюенс], котор[ый] описывает команды, которые он хочет, чтоб вы поддерживали через са[с] протокол, которые он в своей роли поддержива[я] через WS протокол… потом нужно протестировать… убедиться в том, что [environment] работает… потом протестировать вот эти вот команды… если нет, то восстановить их… И в последнюю очередь [с]просить, чего не хватает? Если чегото не хватает, тогда это будет… новый абсолютно девелопмент, который нужно [эстимировать]." Alekseev's amendment: "Ну не новые[,] добавления просто команд." Val called it "1 этап" — stage one [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].
- **Alekseev starts over the weekend; Yavorsky on Monday evening.** Val: "вы приступаете, Евгений, вы приступите к работе сейчас? А Евгений Яворский по возвращению в понедельник вечер[ом]?" — both agreed. Alekseev: "я могу на выходных это всё вставить, соединить и возможно, чтото проверить"; Yavorsky: "в понедельник вечером я… начинаю заниматься." Yavorsky was away at a cottage for the long weekend — "на лонг уикенд уехал[,] я сейчас не дома, а на коттедже" [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].
- **A Jira ticket is created for the work.** Alekseev: "и джиру бы надо создать." Val: "Обязательно обязательно" [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].
- **Engineers meet Monday at 7:00, ahead of [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]'s 8:00 Flex-Port meeting.** Pavel confirmed Klimovich had already planned a Monday meeting "как раз на тему развития флекс портов"; Val: "давайте тогда соберёмся с инженерами до митинга с Климовичем… Митинг с Климовичем назначен на 08:00? Так давайте тогда на 07:00… Я назначу митинг" [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]. *(When Val asked whether "Андрей" was needed, Pavel offered the choice — "Ты Бусик[?] Или Андрей Климович?" — and Val picked Климович. [[wiki/people/andrey-bosik.md|Andrey Bosik]] is not on this thread.)*

## The estimate, and Genadi's private read of it

Asked how long, Yavorsky: "пару недель, наверное… 2[–]3 недели[,] там может месяц." Genadi pushed back — "2 недели или месяц это огромная разница" — and Yavorsky conditioned it: two weeks if nothing new appears beyond what is already written, longer if more must be implemented. Alekseev asked to defer the estimate entirely: "Давайте по времени говорить после Того, как я это всё попытаюсь вставить, проверить. Может он будет… уже работает[ь] в достаточном объёме" [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

After the engineers dropped off, Val said "Это был продуктивный разговор" and Genadi shook his head. His private assessment: "Надо Павла подключить[.] [Е]горский, когда говорит 2 недели[,] это это 2 месяца минимум… Он тянет… в любом случае без Павла это не пройдёт" — Yavorsky's two weeks means at least two months, he drags, and nothing will work without Pavel. **Recorded as Genadi's judgement, not as fact** [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

## "There are no weekends"

Asked to do it over the long weekend, Alekseev raised the obvious. Val's answer: "Нету праздников[,] выходных[,] уикендов. Это я всё отменил… Этот заказ сверху пришёл, да, никаких выходных" — holidays and weekends are cancelled, framed (half-jokingly, alongside "это религиозная") as an order from above. Alekseev: "я то не против" [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]. The wider pattern is on [[wiki/topics/jvl-operating-principles.md]] (Sept 4).

Both engineers named the same real obstacle, separately: rebuilding a working environment. Yavorsky: "всегда проблема заново пересобрать рабочее место[,] там всё… очень капризно… обычно нужно… помучиться, чтобы оно всё заработало," and he asked for help from Pavel or someone to restore his SMIB setup. Alekseev: "мне тоже надо опять всё собирать" [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]. That is what makes Pavel's stage-2 debug-environment proposal (same call) the natural successor — see [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 4).

## Update — what happened on the Monday (Sept 7 2026)

The Monday this decision pointed at was Sept 7 2026, and it produced two meetings: [[wiki/meetings/2026-09-07-wifi-on-flex-port-and-qr-provisioning.md|9:08–9:55 on Wi-Fi]] and [[wiki/meetings/2026-09-07-sas-aft-on-flex-port-and-remote-update.md|10:02–10:33 on SAS/AFT]], both organised by Val [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

- **The meetings happened — at 9:08 and 10:02, not at the 7:00/8:00 slots discussed on Sept 4.** A **schedule slip, not a change of decision**: the engineers' alignment took place with Val as organiser, as planned. Neither Sept-7 source explains or even mentions the time change, so nothing is asserted about why [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **The weekend merge is NOT reported as done.** Alekseev never reports the result of it; what he does say is "эту неделю я в отпуске не могу… там вай фай же ж ещё надо" — on vacation this week and with the Wi-Fi work on top. Pavel's read: "Евгений… только в выходные сможет этим заниматься" — Alekseev can only work on this at weekends. **The commitment stays open** [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **The SAS work moved forward anyway, through Pavel.** He ran his own experiment on the Friday, on the firmware "которую Евгений, 2 Евгения делали… сасовскую," trying to add AFT to it, and then said "я наверное на себя возьму большую часть работы… по сас имплементации." SAS can be parallelised locally "потому что у нас несколько машин и несколько портов" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **Yavorsky is off.** Pavel reported the remote-update task still sitting with him and not started; Val's response was general — "я бы не хотел на Яворского иметь какие-то таски[;] с ним что-то я не умею с ним работать" — so the Sept-4 "Yavorsky from Monday evening" element is dead. Detail on [[wiki/decisions/2026-09-07-remote-firmware-update-mandatory-and-taken-off-yavorsky.md]] [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **Scope grew in a known direction: Georgia needs AFT, and the existing command document does not cover it.** "Это другие команды, не те, которые были реализованы… в тестовой прошивке — там поддерживался режим тит[о]… а нам сейчас надо реализовать режим AFT." A matching AFT command document was asked of Chudinov, who agreed and proposed letting Claude do it across two projects at once. See [[wiki/decisions/2026-09-07-flex-port-goes-sas-and-jvl-drops-the-old-machine-segment.md]] [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **The environment problem both engineers named on Sept 4 became a decision of its own:** [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]].

## Open commitments

- [ ] [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — over the weekend, restore his working environment and merge the trade-show SAS work into the main branch, connecting it up and checking what he can — due the weekend of Sept 5–7 2026 — **still open: no result reported at the Sept-7 meeting, and he is on vacation that week with the Wi-Fi work ahead of SAS** — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]] [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — create the Jira ticket for the SAS-on-Flex-Port work — due unspecified; not reported on Sept 7 — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] or [[wiki/people/pavel.md|Pavel Frolov]] — extend the SAS command document if the implemented set proves insufficient — **sharpened Sept 7 2026 into a request for a separate AFT command document from Chudinov** — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]] [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]

## Update — Sept 9 2026: the code is confirmed to be in git, and Pavel owns the SAS work

At the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept-9 7:02 AM call]] [[wiki/people/irina-shishko.md|Irina Shishko]] asked whether anything was still sitting outside the repository — "[по] флекс[-]пор[ту] тоже[,] этот Яворский уже всё должен был в ги[т] выложить[,] у него ничего не должно было нигде ж остаться, насколько я понимаю" — and [[wiki/people/pavel.md|Pavel Frolov]] confirmed it twice: "Да. Да… **Вся работа в [гите]**" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

That closes the worry running through this page since Sept 4 — that [[wiki/people/eugine-yavorski.md|Yavorsky]]'s material existed only on his own machine. **It does not discharge the merge commitment below**, which is about [[wiki/people/evgeniy-alekseev.md|Alekseev]] getting the trade-show SAS work into the main branch; no Sept-9 source reports on that.

What Sept 9 does settle is ownership: Pavel took the SAS work himself and explained why — see [[wiki/decisions/2026-09-09-flex-port-readiness-slips-to-september-25-and-stays-the-bottleneck.md]], which also carries his readiness estimate (best case **Sept 25**) and his naming of Flex-Port as the programme bottleneck.

## Discharged and superseded

- [x] [[wiki/people/val-levitan.md|Val Levitan]] — send the invitation for the Monday engineers' meeting. **Discharged Sept 7 2026:** both Monday meetings took place with Val as organiser; the times slipped from the 7:00/8:00 discussed to 9:08 and 10:02 — [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- ~~[[wiki/people/eugine-yavorski.md|Eugine Yavorsky]] — rebuild his working environment and take up the SAS port on Flex-Port from Monday evening~~ — **SUPERSEDED Sept 7 2026.** Val: "я бы не хотел на Яворского иметь какие-то таски." Pavel took the larger part of the SAS/AFT implementation instead — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]

## Open questions

- **How long the port actually takes.** Yavorsky says two weeks, possibly three, possibly a month; Genadi privately says at least two months and not without Pavel; Alekseev wants the estimate deferred until stage one is tested. *(Genadi's "it will not work without Pavel" read is the one Sept 7 bore out, though no source says so.)* — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- **Where the document actually lives.** Val and Alekseev both said Confluence, both hedging ("скорее всего", "помоему"); not confirmed on the call, and not raised again on Sept 7 — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]

*(Answered Sept 7 2026: "Is Chudinov's command list sufficient?" — **no, not for Georgia.** The existing document covers the TITO mode the test firmware supported; Georgia runs AFT, "это другие команды", and a separate AFT command document was requested. [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]])*

**§15.8:** clear — engineering scope and scheduling only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
