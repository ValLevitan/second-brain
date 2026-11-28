---
type: decision
title: MVP 2_1 does not close until Evgeniy Alekseev confirms that the board update also flashes the Wi-Fi module (capability 399, with an added definition-of-done item — after the update the module at least scans the network) and the remaining autotests finish (end of the week), so the November 25 date does not hold; the 2_1 scope stays fixed — Flex-Ports on Wi-Fi to the IQ, remote update of all Flex-Ports, split goods, support phone numbers (the inspector/audit report is 2_2); Minsk gives Andrei Klimovich an alpha build on Saturday morning Eastern to test what does not need Wi-Fi; Seregin writes Alekseev an instruction for the Flex IQ emulator; Val sends Minsk full assembled new-revision Flex-Ports with the Wi-Fi module from China; the requirements-conflict process and Chudinov's release-specification idea go to a separate meeting; the location onboarding email fix goes into 2_2, which has no schedule yet (Nov 25 2026)
date: 2026-11-25
aliases: [MVP2_1 release sync, MVP2_1 Release Sync WiFi Firmware Test Alekseev, 2_1 cannot close without the Wi-Fi test, 21 мы не можем закрывать, один из сдерживающих факторов, capability 399, feature 258, afort 258, scans the network, сканирует сеть, definition of done, дефиниш оно дан, alpha build Saturday, альфа версия, бинт альфу, split goods, сплит гудс, сплит гуд, support phone numbers, new TITO ticket small barcode, Flex IQ emulator instruction, аккумулятор флекса айкью, full assembled Flex-Port to Minsk, собранный порт, полную сборку, release specification, спецификация на релиз, conflict-check agent, location onboarding email, 2_2 no schedule, MVP 2_1 Jira filter, MVP 2_1 release name, capability 145 Wi-Fi tests]
source-count: 2
status: active
open-commitments: 10
open-questions: 3
---

# MVP 2_1 closes only after Alekseev's Wi-Fi-module test and the autotests; scope stays fixed; an alpha build for Andrei on Saturday (Nov 25 2026)

Agreed at the [[wiki/meetings/2026-11-25-mvp2-1-release-sync-wifi-firmware-test-alekseev.md|Nov 25 2026, 9:51 AM "MVP2_1 release sync"]] (Russian, about 46 minutes), organised by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], with [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"; left at about 15 minutes) and [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov") [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]] [[raw/Meeting_Notes_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]. It is the release day set on [[wiki/decisions/2026-11-20-mvp-2-1-is-set-for-wednesday-november-25-task-399-moves-into-2-1-no-central-rollback-fix-forward-and-mvp-2-2-is-the-master-role-and-reporting.md|Nov 20]]; that date did not hold.

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word; garbles are kept as heard.)*

## 1. The Wi-Fi module update cannot be tested in Minsk

- **Irina's worry.** "мы не можем здесь проверить, это вот этот вот апдейт вай фай" — the Wi-Fi module "будет обновляться вместе с прошивкой порта" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].
- **Why.** Pavel: the board is "новая оплата, которая есть в джордже, которая есть у Евгения Алексеева. Последняя ревизия флекспорта" with the Wi-Fi module soldered on. Minsk checks the module's function, "но просто он у нас прошит внешними средствами"; on the real board it is wired to the processor, and [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] made the main-processor update flash the Wi-Fi module at the same time. Pavel gave him the firmware and the description: "Проверь сейчас мяч на его стороне" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].
- **Help for Alekseev.** Val would send him an IQ connected to the cloud server; Pavel: "его для этого IQ пока наверное не надо". Pavel: Minsk has a Flex IQ emulator ("аккумулятор флекса айкью" — emulator, the notes' reading) that can send firmware; Alekseev must learn to use it. [[wiki/people/anton-seregin.md|Anton Seregin]] used it most, "как разработчик и как тестировщик"; Chudinov: "Инструкцию сможет подготовить подробно." Pavel: "это андертенг для нас, чтобы завтра максимум послезавтра сделать, потому что у Алексея больше всего времени в выходные будет" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].
- **Boards he has.** Klimovich: "мы от Алексеева на прошлой неделе получили 6 бортов, которые он сделал ручную поставил туда вай фай модули"; Pavel: he still has some [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].

## 2. 2_1 does not close without that test and the autotests

- Val: "мы не можем имплементировать MVP 2 до тех пор, пока Алексеев это не протестируют, правильно?" Pavel: "по факту это один из сдерживающих факторов, то есть пока мы не подтвердим, что у нас есть возможность обновления. Плат, включая вайфай модуль ну 21 мы не можем закрывать." The second factor is "оставшиеся авто тесты" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].
- Irina, after talking with "Владимиром и с Антоном": for the 2_1 autotests "До конца этой недели нам ещё точно надо время" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]. "Владимир" and "Антон" are read as [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] and Anton Seregin (**inference** — the test team; the notes give no surnames).
- **Alekseev's task in Jira.** Pavel: "его задача стоит до сегодняшнего дня капобилити 399", a feature under it heard as "afort 258", in progress. The feature describes the update procedure; its definition of done has 3 items. Pavel added one: "проверь, что модуль по крайней мере сканирует сеть"; Val: "Это это не задача, просто надо добавить"; Pavel: "Все добавил дополнительный пункт дефиниш оно данных." Pavel contacts Alekseev and the schedule changes with the result: "если у него сразу всё заработает… времени на на его проверку 5 минут", maybe "завтра с утра" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].

## 3. The 2_1 scope is fixed

- Pavel: "нас уже зафиксировано, вряд ли мы будем что то убирать или добавлять." Irina: "по 20 по один уже нет никаких вопросов", except how to test the Wi-Fi and finishing the autotests [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].
- **Klimovich's summary for Val.** "Фрекс порты соединяются с IQ по вайфаю. Все экспорты могут обновляться удалённо." Inside the IQ: "сплит гудс, то есть можно было направлять деньги не только на дебит карту, но ещё. Отдельно, другим путём", and support phone numbers. He added "репорта для инспектора"; Irina: "Репортов 22." Klimovich: "главное 3 постулата… Вай фай удалённое обновление портов и сплит гуд" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].
- **Val's Claude list.** Val showed a list his Claude made from Jira. Klimovich: "Да, все верно подтверждаю… заголовки жирные по заголовкам, там всё корректно"; Tsymanov: "1 2 это помоему один и тот же пункт" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].

## 4. Remote update without Wi-Fi, and the alpha build

- Klimovich: the Wi-Fi link to the IQ must be tested "именно на том хардве, который мы устанавливать в локациях планируем." Pavel: "для нас эти платы дойдут. Там прошло, если через 3 недели"; until then Alekseev checks, and Georgia can then flash "с помощью удалённой прошивки или через USB". Current boards without Wi-Fi must also update remotely; Klimovich: "Вот это мы сможем протестировать на на текущих платах" — Pavel: "Да" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].
- **Alpha build.** Pavel proposed an intermediate "Альфа версия" to test what is not tied to Wi-Fi: remote updates, "сплит бутс" on the Flex IQ, "Новые экраны", and "новый формат тито тикета да с маленьким баркодом". Klimovich: "в пятницу мы должны устанавливать первую локацию, если всё пойдёт, как запланировано"; "если вы в субботу утром по восточному времени сможете отдать какойто бинт альфу, то я смогу его в субботу протестировать." Pavel: "Без проблем" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]. The first install: [[wiki/decisions/2026-11-24-first-transactional-install-now-invoice-due-upon-use-of-service-interest-from-day-7-internal-and-the-invoice-template-moves-out-of-business-central-into-github.md]].

## 5. Hardware to Minsk

- Val: JVL will send Minsk the hardware from China. Pavel: "Нам только в новый флекс порты нужны ique нам, в общемто. Не нужно." Val: "Нас уже идет счет на тему" (the notes: already being invoiced); "Но это будет месяц идти" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]] [[raw/Meeting_Notes_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].
- Val took the list on himself ("это я возьму на себя"). Pavel: "Флекс флекспортплату новую новой ревизии. С вай фай модером"; as "Собранный порт… с экраном с тачскрином. Со сканером ну лучше полную сборку, иначе это потом могут быть проблемы." Klimovich's name for it in Business Central was heard as "402 2 а" — **unclear** [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].

## 6. Conflicting requirements — to a separate meeting

- **Irina:** one cause of the delays is "недостаточность или конфликтность в наших требованиях", which the team must rewrite during the work. The requirements' owner is Klimovich; she cannot rewrite them (Pavel: "Без согласования, по крайней мере") [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].
- **Val:** Klimovich should groom the requirements all the time, as a cycle — an agent "который читает все требования, говорит, здесь наверно конфликтная. Или здесь повторения?" — and "это должно быть сделано до Того, что Ирина поймала" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].
- **Klimovich:** each day he handles the team's overnight comments "через агента"; most come from developers working on a requirement, and "такие вещи я не могу отловить заранее без присутствия разработчиков"; when he edits, "у меня всегда стоит проверка на новые конфликты." Val: "Конфликт между разработчиком и продактонором он хелси… Это это продуктивно." Pavel wants an agent that "автоматически пробегает, например, по всем капбилити по всем связанным требованиям" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].
- **Chudinov's release specification.** A release is "подтверждение списка всех требований, которые он должен был реализовать. Их уже нельзя редактировать никогда в будущем"; he is preparing a document, may review it with Sergey, and wants a separate meeting. Val: "Я согласен, что на это должен быть другой митинг… под отдельным уже зонтиком другой темы" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]. This continues the Nov-24 stand-up route — [[wiki/decisions/2026-11-24-a-pull-request-may-not-merge-while-a-claude-review-red-mark-stands-developers-lose-operating-system-access-to-the-production-accounting-host-and-the-requirements-sprawl-goes-to-a-separate-meeting-before-val.md]].
- **Klimovich's undertakings.** "я пересмотрю своего ещё раз агента, который на конфликты"; before 2_2 planning "там всё должно быть чисто"; after MVP 1 and 2_1 are out, "мейк сенс сделать полноценный митинг на тему. Что нам изменить в процессе?" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- Chudinov, leaving: "по 21 вопросов нет"; on 2_2 he answered Klimovich's comments and waits — "ревью 22 идёт" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].

## 7. Jira dates

- The Jira end date of 2_1 was "25" (Irina). Val read his filter as everything leading to capability 146; Pavel: "все капобилити, которые в состоянии реквест или инпрогресс, они все одинаково вершина айсберга." The filter was wrong — Irina: the release is "мвп пробел 2 подчеркивания один"; capabilities "159 234 289 371" should also show; "242 это 21, не имеет отношения" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].
- Pavel: capability 397 — "я обновил это уже дима только что закаметил", date set to today ("дима" = Chudinov, who opened the call saying he had merged his part — **inference**). The latest date shown was the 30th, on capabilities 145 and 287; Pavel: "145 это тесты по вай фай." Irina: "ну они все 5 вот этих побилити они все да зависят от автотестов"; "их сегодня не закончили, поэтому им всем нужно новую дату" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].

## 8. MVP 2_2

Val showed his Claude's summary of 2_2. Klimovich: "Да выглядит корректно"; he will add the location onboarding email he sent the day before — "нужно поправить адресатом и всякие дисплеймеры." Irina asked for the time frame: "от этого реально зависит, что мы успеем." Pavel: some 2_2 dates are not set and some proposals carry old dates. Val: "Это не скетжил даже" [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].

## How it sits against earlier rulings

- **Nov 20 — the November 25 date: evolution.** On Nov 20 the 2_1 Jira date moved to Wednesday November 25. On Nov 25 the release does not close until Alekseev's test and the autotests (end of the week); the five capabilities need new dates and the latest shown is November 30. The Nov-20 page is annotated — [[wiki/decisions/2026-11-20-mvp-2-1-is-set-for-wednesday-november-25-task-399-moves-into-2-1-no-central-rollback-fix-forward-and-mvp-2-2-is-the-master-role-and-reporting.md]]. The Nov-25 morning stand-up had already said the release "Сегодня… Но его не будет" — [[wiki/decisions/2026-11-25-nothing-new-goes-into-the-bep-jira-project-each-repository-uses-its-own-prefix-old-project-changes-get-a-new-capability-and-the-power-loss-during-update-report-is-proposed-out-of-the-requirement.md]].
- **Nov 23 — Alekseev's check.** On Nov 23 he was to check the Wi-Fi-module update that evening; on Nov 25 it is still not confirmed — [[wiki/decisions/2026-11-23-the-20-revision-2-boards-go-back-to-alekseev-for-repair-build-4377-with-the-modem-is-field-tested-on-different-modems-before-the-lab-and-remote-updates-and-wi-fi-setup-are-the-two-must-haves.md]].
- **Nov 12 — the audit report.** The Nov-12 split listed the audit (inspector) report in 2_1; on Nov 25 Irina places it in 2_2 — **evolution**, noted on [[wiki/decisions/2026-11-12-mvp-2-splits-into-mvp-2-1-iq-and-port-and-mvp-2-2-web-services-lottery-becomes-goods-and-the-inspector-report-becomes-the-audit-report.md]].

## Open commitments

- [ ] [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — test that the port firmware update also flashes the Wi-Fi module (capability 399, feature "afort 258"), including that the module then scans the network — due Nov 25 in Jira; Pavel: maybe Nov 26 morning or the weekend — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- [ ] [[wiki/people/anton-seregin.md|Anton Seregin]] (named by Pavel and Chudinov) — write Alekseev a detailed instruction for the Flex IQ emulator — due Nov 26–27 2026 ("завтра максимум послезавтра") — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — contact Alekseev and change the schedule by the result — due unspecified — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- [ ] Pavel Frolov and the Minsk team — deliver an alpha build (remote updates, split goods, new screens, new TITO ticket) — due Sat Nov 28 2026, morning Eastern — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — test the alpha build — due Sat Nov 28 2026 — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] and the test team — finish the 2_1 autotests and set new dates on the five capabilities — due end of the week of Nov 23 2026 — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — send Minsk full assembled new-revision Flex-Ports with the Wi-Fi module (touchscreen, scanner) from China — due unspecified (about a month in transit, per Val) — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- [ ] Andrei Klimovich — review his conflict-check agent; requirements clean before 2_2 planning — due before 2_2 planning — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- [ ] Andrei Klimovich — add the location onboarding email fix (addressee, disclaimers) to 2_2 — due unspecified — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — finish the release-specification document and set up the separate meeting on it — due unspecified — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]

## Open questions

- What is the real 2_1 release date? Jira said the 25th; the autotests need the rest of the week; the latest capability date shown is November 30 — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- What is the 2_2 time frame? Irina needs it to know what fits; there is no schedule yet — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- Who is "Артём" on capability 145 (the Wi-Fi tests)? Heard once; no surname — [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]

## Open contradictions

- **When the new boards reach Minsk.** Val: the shipment from China "будет месяц идти"; Pavel, later in the same call: the boards reach Minsk "через 3 недели". Both Nov 25 2026, same call; not resolved [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]].

**§15.8:** clear — no pay amounts; "счёт" is a shipment invoice with no figure. **§15 #9:** clear — capability and feature numbers only.

## Sources

- [[raw/Meeting_Transcript_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
- [[raw/Meeting_Notes_MVP2_1_Release_Sync_WiFi_Firmware_Test_Alekseev-November-25-2026.md]]
