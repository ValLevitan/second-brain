---
type: decision
title: Open MVP 1 requirement questions are settled on the call — REQ-753 deleted, no fixed disconnect timeouts, no PIN lockout on Flex IQ, CAP-173 reopened, REQ-1550 kept with an ADR — and only a question that takes more than a minute is parked
date: 2026-09-23
aliases: [REQ-753 deleted, requirement 753, graveyard, кладбище, one-minute rule, park anything that takes more than a minute, no fixed timeouts, show the disconnect as fast as possible, keep retrying the device, no PIN lockout, REQ-1429, CAP-173 back to In Progress, capability 173 reopened, REQ-1550, external traffic protection, ADR for traffic protection, REQ-1413, Flex-Port switching, nine Flex-Ports default twenty, REQ-1603, buffering, REQ-1416, router purchasing, European or American routers, REQ-1412, ESL English for Claude, limit sentence count, forfeit wallet, lost money wallet, open questions are not a blocker]
source-count: 4
status: active
open-commitments: 6
open-questions: 2
---

# Open requirement questions are settled on the call

Settled at the [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept 23 2026 8:00 AM MVP 1 call]] (Russian). [[wiki/people/irina-shishko.md|Irina Shishko]] walked the requirements that still carried open questions — "около 15 ну чуть меньше может 12 13" — and Val asked that they be settled there and then: "Я предлагаю все вопросы есть сейчас" [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

## The rule — decide what can be decided; park only the slow ones

The first item, **REQ-753**, mixed products in one text ("порты сми п и пэй и айкю"). [[wiki/people/andrei-klimovich.md|Klimovich]] first proposed sending it to the MVP 2 parking backlog, because it "не добавляет нам ничего Того, чего у нас нету уже". Val objected: "Мы сейчас начинаете кладбища строить". [[wiki/people/dmitri-chudinov.md|Chudinov]]: "этот рекламу не нужен… Непродуктовый, он абстрактный". Klimovich then set the rule [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]:

> "любой рекламент, который потребует больше, чем одна минута на то, чтобы принять по нему решение… Я предлагаю парковать куданибудь сразу не удалять. Здесь решение можно сразу принять."

REQ-753 was **deleted** on the call — Irina: "мы его удаляем"; Pavel, Klimovich and Chudinov agreed [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

**Open questions are not a blocker.** Chudinov: some answers need a spike or appear "только когда ты приступил"; Klimovich agreed it "не должно быть каким то блокером". Chudinov's condition: "Главное не оставить их открытыми по завершении". Pavel: "согласен" [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

## The rulings, requirement by requirement

- **Device disconnects — no fixed times (REQ-1560 and about four more).** The open item was how long to wait before showing an error when a device drops — bill validator, SAS, QR scanner, the Flex IQ–Flex-Port link, "WS". [[wiki/people/alexander-biratka.md|Biratka]]: the SAS standard "описывает работу машины, а не хаста, а мы в данном случае хостом работаем"; losing SAS means "мы дальше работать не можем". [[wiki/people/alexei-khamin.md|Khamin]]: do not wait for the player to press something. Pavel's wording, which Irina took for all these devices: "не будем здесь никакие времена указывать… при пропадании связи с любым из устройств мы максимально быстро отображаем эту информацию на экране пользователя. И постоянно делаем попытку пересканирования", because "лучше раньше дать игроку знать" [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].
- **No PIN lockout on Flex IQ (REQ-1429).** Klimovich: "нам не нужно блокировать IQ, если они ввели там 3 раза подряд, не тот пин ничего страшного." Pavel: "Да до бесконечности." [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- **CAP-173 goes back to In Progress.** It showed as finished while its requirements were still active. Klimovich: "Она не может быть комплект"; Khamin: it cannot be in review while requirements have open items. Klimovich: "Значит, она остается в инпрогресс" — the requirements are updated and moved through their statuses first. Irina: Pavel reviews requirements **60, 63, 65** under it (read as 1560, 1563, 1565), adds the engineering answers, and they move to Accepted [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].
- **External-traffic protection stays in MVP 1 and needs an ADR (REQ-1550).** [[wiki/people/andrey-bosik.md|Bosik]]: an ADR describing the protection mechanism must be written in the repository first, and "это нужно реализовать, потому что… наш терминалы смотрят в интернет, соответственно, они должны быть защищены." Klimovich asked whether a minimal set could come first; no clear answer is on record [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].
- **Requirements are written short, in plain English.** Pavel: REQ-1550 has "столько слов, столько букв, что ну человеку невозможно это прочитать". Val: "Вам нужно к лоду сказать, чтобы было не больше там какогото определённого количества предложений в нём, и он пользовался e sl. Типом английского языка"; "я всё всегда читаю… я трачу свою энергию"; "отсылайте то, что вы бы сами читали". Irina: rewrite with "только главную суть" [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].
- **Router and modem purchasing stays, if testable (REQ-1416).** Bosik kept it because equipment must come from "европейских или американских производителей не китайских". Irina asked how to test it. Klimovich: if the acceptance criteria are testable, "нормальный рекламент может жить"; Biratka: look at the purchased router. Chudinov's reason it matters: otherwise unsupported kit turns up at a location "и мы будем долго разбираться" [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

## Answers given, no scope ruling

- **Flex-Port switching (REQ-1413, under CAP-144).** Chudinov: one screen shows active Flex-Ports and those present on the network, and an active one can be moved to another device. Pavel: "это относится к MVP 2 скорее". Chudinov: useful in development, in production and at a trade show. Limits: "в джорджии 9 машин соответственно, у нас может быть максимум 9 флекс портов, но мы там ставили сейчас дефолт с запасом 20"; the future ceiling needs "отдельный стресс тест" (what the ceiling is was garbled). Compare the Sept-16 ruling, 15 for MVP 1 and a design for 99: [[wiki/decisions/2026-09-16-fifteen-flex-ports-in-mvp1-and-the-system-designed-for-ninety-nine.md]]. **MVP 1 vs MVP 2 was not ruled**; Bosik will rewrite the requirement from the transcript [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].
- **Buffering when the external link drops (REQ-1603).** Chudinov: "Это уже работает" — a default setting (rendered "Влюньбит", read as Fluent Bit — **inference**), size "помоему 500 или сколько" megabytes; it sends everything once the link returns. Bosik will turn the open questions into acceptance criteria [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].
- **Gateway reporting and per-Flex-Port log data (REQ-1412 and a related item).** Chudinov: the Flex-Port sends only logs and transactions, shown in Grafana; there is no cloud view of connected Flex-Ports and their problems "в MVP один". Alerts can be built in Grafana. Bosik on REQ-1412: "можно вообще просто убрать" [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

## Also ruled — lost money becomes a "forfeit" wallet

[[wiki/people/alexei-khamin.md|Khamin]] raised five open Flex-Port bugs where money is lost — for example a second collect from the machine while the Flex-Port shows a cash-out, or a scanned ticket no longer in the database. Klimovich: "Я предлагаю создавать его лет и с отдельным статусом там форфайт" — the money "лежат, но с ними пока ничего сделать нельзя, но они существуют" *("его лет" read as "wallet" — **inference**, matching the notes)*. Chudinov had already created **capability 231** for it; the five bugs go there [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]] [[raw/Meeting_Notes_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

## Update, Sept 24 2026 — the lost-money bugs are linked to 231, and the team fixes them itself

At the [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|Sept-24 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]:

- **Done.** [[wiki/people/alexei-khamin.md|Khamin]]: "я слинковал всё под кап 231". [[wiki/people/andrei-klimovich.md|Klimovich]] checked them for relevance and added comments. Who fixes them was still open.
- **Who fixes them.** Pavel: "Мы будем фиксить, я думаю." Irina: "Да я даже уверена… Что кто то из наших". Pavel: waiting for [[wiki/people/eugine-yavorski.md|Yavorski]] is out — "яворский точно не будет с нами" — and waiting for [[wiki/people/evgeniy-alekseev.md|Alekseev]] to do it at weekends "тоже не вариант". No person was named.

## Update, Sept 24 2026 (8:01 AM) — two of the lost-money bugs get rules

Three hours after the stand-up, on the [[wiki/meetings/2026-09-24-transactional-mvp1-flexport-money-loss-bugs-and-release-date.md|8:01 AM MVP 1 call]], [[wiki/people/andrei-klimovich.md|Klimovich]] brought bugs **349** and **354** and called "вот эти 5 багов очень хорошие баги классные" [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]. Two rules were agreed: a Flex-Port that dies holding money keeps the transaction and sends it to unclaimed when it comes back; a Flex-Port with no gateway link goes out of service and the money stays on the machine. He will add both to the requirements that day. Full ruling on [[wiki/decisions/2026-09-24-a-flex-port-that-dies-holding-money-sends-it-to-unclaimed-and-one-without-a-gateway-goes-out-of-service.md]]. *(That these two are among the five linked to capability 231 is an **inference**.)* The Sept-23 "forfeit" status was not mentioned on the call.

## Open commitments

- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — apply Pavel's "no fixed time, show at once, keep retrying" wording to the device-disconnect requirements (she noted minute 24 of the call) — due unspecified — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — review requirements 1560, 1563 and 1565 under CAP-173, add the engineering answers, and move them to Accepted — due unspecified — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — rewrite REQ-1413 with the Flex-Port switching answers from the transcript — due unspecified — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — turn the open questions in REQ-1603 into acceptance criteria — due unspecified — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — rewrite REQ-1550 short, keeping only the essence, and write the ADR for the external-traffic protection mechanism — due unspecified — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — make the acceptance criteria of REQ-1416 (router and modem purchasing) testable — due unspecified — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [x] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — attach his five lost-money Flex-Port bugs to capability 231, "первым делом" — due Sept 23 2026 — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]] — **discharged Sept 24 2026:** "я слинковал всё под кап 231" — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [x] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — move the IQ operator tilts and alerts into a separate text collection with codes — due Sept 23 2026 ("Я хочу сегодня ещё дожать") — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]] — **closed differently Sept 24 2026:** he finalised the IQ tilt logic with a code for each error but kept the tilts inside the main text library — "Я решил не выносить селты в отдельный документ… заставляет редактировать 2 документа" — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [x] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — review Irina's full NFR list with Claude for conflicts with product logic — due Sept 23 2026 ("постараюсь сегодня") — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]] — **discharged Sept 24 2026:** "проревэл всю коллекцию, нон фанш эквайменс против бизнес и фанкшена логики" and fixed the differences in Jira — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]

## Open questions

- **Where non-development requirements (such as hardware purchasing) should live.** Irina: "это нужно решить, что мы должны с такими требованиями делать"; Bosik suggested a "not development" capability; nothing was settled — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- **Whether bugs attached to a capability show in the portfolio view.** Pavel suspects they will be visible only inside the linked task; to be checked when Khamin attaches the first five — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]

**§15.8:** clear — requirement and product rulings only. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [[raw/Meeting_Notes_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
