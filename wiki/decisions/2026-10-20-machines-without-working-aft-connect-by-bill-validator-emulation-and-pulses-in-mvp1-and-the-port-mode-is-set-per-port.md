---
type: decision
title: Other makers' machines whose AFT does not fully work connect through bill-validator emulation (money in) and pulses (money out), and this mode is in MVP 1; the mode is set per port in the gateway, not detected; SAS (6.0 and up) is kept apart from AFT, for data that may become a paid product; MVP 1 release on a Wednesday and first install about November 2 (Oct 20 2026)
date: 2026-10-20
aliases: [bill validator emulation mode, BV emulation mode, режим билвалидатор эмуляции, pulses for cash-out, AFT for transactions SAS for data, SAS 6.0 and higher, not a hybrid mode, случайный режим, accidental mode, SAS data as a paid product, analytics of competitor machines, 30 to 50 dollars a month, promotional credits only on AFT machines, port mode per port in the gateway, no auto-detection of AFT, ID-003, four bill validators, report every spin, HTT dongle, machines back on Friday, MVP1 release Wednesday, first install November 2, ошибочное решение]
source-count: 2
status: active
open-commitments: 8
open-questions: 3
---

# Machines without working AFT connect by bill-validator emulation and pulses in MVP 1; the mode is set per port

Settled at the [[wiki/meetings/2026-10-20-third-party-egm-bv-emulation-mode-and-sas-data.md|Oct 20 2026, 8:31 AM third-party EGM call]] (Russian, about 33 minutes) between [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]. The notes list four decisions: the bill-validator mode in MVP 1 (Val, Pavel), SAS kept apart from AFT (Klimovich, approved by Val), the per-port mode (Pavel, Klimovich), and the dates (Val) [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## Where the integrations stand (Pavel)

- **Only JVL and Aristocrat.** "Живел и аристократ. Молодцы." The others "пока не тянут на… Современный рынок Джорджия" [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **So the others go to bill-validator emulation.** Machines that work only partly with AFT transactions must be connected "в режиме билвалидатор амулейшн для зачисления денег и palses для снятия денег" — bill-validator emulation for money in, pulses for money out [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **JVL can already do it.** Klimovich asked whether the logic exists. Pavel: "это мы умеем". Val: "мы с этого начали нашу карьеру… Это была начальная идея" [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Val: the SAS-only call was a mistake.** Pavel: when JVL moved to SAS, it was decided that MVP 1 goes only on SAS. Val: "Вот это было ошибочное решение." Pavel kept the old code as an extra parameter instead of removing it; about two weeks earlier it worked on a JVL machine. He thinks the Flex IQ already lets you pick mode one or two [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **But QA has not tested it lately.** "кюэ этот режим последние 2 недели не проверяли", so new tests are needed for this mode, run through all the new test cases [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].

## AFT for transactions, SAS for data

- **The question.** Pavel: do we still want to take some information over SAS while working by bill validator? If so, plan a "гибридный режим" for MVP 2 — money by bill validator and pulses, statistics and status over SAS. Klimovich: "Обязательно" [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Klimovich's case.** Operators could analyse each game title's performance and money in and out. JVL could sell it through its operational dashboard as a subscription: "за это вы заплатите там 30 40 $50 сверху в месяц" — a new revenue flow for JVL, a competitor-machine analytics product for the operator [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Val's doubt.** If an operator lacks this on the other machines but has it on JVL's, he will push those makers to add it. Pavel agreed Val raised the right point: give more on JVL and Aristocrat machines, and leave the half-done foreign machines "в даунгрейде". Klimovich: price decides, operators will keep buying cheap Banillas; "это не так однозначно" [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Not "hybrid".** Val: do not call it that — "давайте про это говорить как случайный режим". It is not a documented implementation but "какаято случайная Находка"; the makers may change it, and JVL would be chasing them forever. Either the machine has SAS "6.0 и выше", or "мы подключаемся через пульсы". Pavel: IGT reports SAS version 6.03, yet AFT does not work [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Klimovich splits the two.** "нам стоит разделять одно это поддержка со с протокола отдельно это AFT." AFT is the logic block for transactions; SAS is the block for data, and SAS sends a great deal of it. Val: "Замечательно"; "Да хороший вопрос правильно поставлен… Очень, очень умно." [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- **The wording Val approved.** Klimovich: "Для транзакции мы используем, билвалидатор и аккаунтеры через пульс и на всех машинах на рынке, у которых хоть в какомто виде есть с аз протокол 60 и выше. Мы можем данные забирать и превратить это в наш продукт. За который брать дополнительные деньги." Val: "Да, мне нравится, что вы говорите, это это правильно сказано." [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]] The notes record no final product decision on selling the data [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Promotional credits.** Val: later JVL wants to give promotional credit; then of six machines at a location "только джил и аристократ может получить" it. Klimovich: that is thanks to AFT support [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].

## How a port knows its mode

- **Klimovich's problem.** A technician fits a port on an Aristocrat (SAS only) and the same port on an IGT (bill validator, pulses, and SAS for data). The port must know how it does transactions — a new settings element [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Val: detect it.** If a bill acceptor is connected to the port, there is no AFT. **Pavel: not reliable.** A machine may answer the AFT capability query "у меня всё есть", take money and still not pay out; a second Light & Wonder machine says AFT is registered but all AFT options are zero. And a bill acceptor "может быть не запитан, может оборваться"; a broken pulse line cannot be detected at all — "мы просто деньги не принимаем" [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Set it per port in the gateway.** Pavel: the current firmware needs nothing new — change a parameter through the console, or, he thinks, on the Flex IQ devices screen there is a switch between bill acceptor and SAS. Klimovich: then connect all the ports, go into the gateway, which sees them all, and mark each one AFT or non-AFT [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].

## Bill acceptors

- **Swapped in the field.** Klimovich: a technician may replace a broken bill acceptor with one of another make. Pavel: JVL connects at the base — the connector fixed to the cabinet, which stays when the acceptor is pulled; a compatible acceptor plugs into it. Nobody at a location is likely to re-run wires for an acceptor [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Which makes.** The borrowed machines have four different bill validators. Pavel named "Джей сиен" (read as JCM — **inference**) and a second make Alekseev once did ("Меи", read as MEI — **inference**), which needs its own cable and was never checked. Irina thinks that one is not popular in Georgia. Pavel: the ID-003 protocol "должен работать универсально"; check alternative acceptors with the same connector. Klimovich: "Мы можем сейчас проверить на тех 4" [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]] [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].

## SAS commands seen on the borrowed machines

- **Pavel checked three machines, not the Banilla.** A limited set: they all report the handpay state; some report door open and close; Light & Wonder answers how many credits are on the machine, and IGT probably too [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Irina:** certified machines must support a set of about 20 commands, "иначе им бы не выдали сертификаты". **Pavel:** they must give statistics on the primary SAS port, but not necessarily on the secondary; check each machine [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Every spin.** Light & Wonder has a SAS setting to report every spin — the bet, and probably the game. Pavel has not seen it elsewhere; JVL has no such setting. Trying it needs a factory reset of the machine [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Keys and dongles.** Irina: Georgia required machines without special keys. Pavel: other makers' machines still have their own. Klimovich: the dongle for the "HTT" (read as IGT — **inference**) is taken back that day; it costs a lot, and without it the settings cannot be reset or changed [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].

## This week's plan

- **The machines go back on Friday** (Oct 23 2026 — the meeting was on a Tuesday), though more can be borrowed later. Klimovich and [[wiki/people/sebastian.md|Sebastian]] are away on Wednesday and Thursday at a trade show; [[wiki/people/elizabeth.md|Elizabeth]] is there [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Connect by pulses and bill validators** on all machines except the Banilla. Pavel: SAS stays on everywhere; AFT is turned off on the secondary port so it does not get in the way. Look at the other machines' settings too ("на ig t там минимум настроек"). The Banilla stays as it is, with SAS and AFT; Pavel checks which commands it supports [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- Klimovich was glad "этот протокол… нон сасовский" works, and wants to see how compatible it is [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].

## The MVP 1 dates (Val)

- **Fix MVP 1 now.** Val asked to set the final MVP 1 and look at the schedule at this meeting. Pavel had done nothing yet on the tasks from the morning meeting with Alekseev. Val: all that is needed is "чтобы компилировалась программа" — Pavel: "Выпускать продакшн рейти софт?" Val: "Да." Irina: Khamin writes the story for Alekseev. Pavel: good if Alekseev does it over the coming weekend [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Release on a Wednesday.** Val: "вам протестировать надо? Да, значит, давайте на на среду… На среду сделаем релиз." Which Wednesday is not stated; the notes say so too. Since Pavel spoke of the coming weekend, the Wednesday after it (Oct 28) fits best — **inference** [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]] [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **What the release needs.** Pavel: QA must test as many bill-validator-emulation cases as possible, in parallel with real machines in Georgia. Val, partly garbled: MVP 1 "Включает… Плюс. Пульсы" — it now includes the pulses — and the tasks must be added. Klimovich asked what "production server" means here; Val: to release the product easily and stably — not yet continuous integration, "1 шаг" toward it [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **First install about November 2.** Val: "1 установка это гдето 2 ноября… Это понедельник." Klimovich: "при условии, если у нас всё остальное… Есть в наличии." Val: of course, if those conditions hold [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].
- **Requirements first, then tests.** Val: Klimovich makes the capability for pulses and moves it into MVP 1, tied to requirements with acceptance criteria, so Irina's team can add test requirements; then "Алексей" (Khamin, by context — **inference**) takes the requirements and acceptance criteria and runs Claude to write the tests. Irina: "только не лёша. Ну ладно." Pavel hopes most existing tests work in this mode. Irina asked Klimovich to approve the reworked requirements in a comment — Claude keeps flagging that they wait for his approval; then they are final [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].

## How it sits against earlier items

- **Reverses the Sept-7 "drop the flexible connection".** On Sept 7 Val dropped the bill-acceptor/counter connection and went with SAS — [[wiki/decisions/2026-09-07-flex-port-goes-sas-and-jvl-drops-the-old-machine-segment.md]]. Now he calls the SAS-only MVP 1 call a mistake, and the bill-validator/pulse connection is in MVP 1 for machines without working AFT — **evolution**. It reached engineering first through Val's Sept-13 email and the Sept-14 selection capability — [[wiki/decisions/2026-09-14-flex-port-sas-mode-is-a-selection-capability-not-a-long-lived-branch.md]].
- **The mode switch.** On Oct 1 the mode was set per port on the Flex IQ set-up screen, and Pavel said MVP 1 would not ship in two modes — [[wiki/decisions/2026-10-01-sas-or-no-sas-is-set-per-flex-port-on-the-flex-iq-set-up-screen-and-sent-at-registration-with-the-pin-code.md]]. Now both modes are in MVP 1 — **evolution**.
- **Gaps become requirements.** Val's request that the pulse capability be tied to requirements with acceptance criteria applies his Oct-18 rule — [[wiki/decisions/2026-10-18-every-gap-found-on-another-makers-machine-becomes-requirements-and-the-machine-emulator-keeps-a-mode-per-maker.md]].
- **The dates.** The first-ten-locations plan started from November 1, and the owner ruled November 1 the transactional MVP 1 release date — [[wiki/decisions/2026-10-14-the-first-ten-transactional-locations-go-in-from-november-1-on-stock-monitors-ports-without-wi-fi-and-hand-made-harnesses.md]] (Oct-20 note). A first install on Monday Nov 2 (Nov 1 is a Sunday) fits that; a release on a Wednesday before it is not said to replace it.

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — write the capability for the bill-validator + pulses mode, move it into MVP 1, and tie it to requirements with acceptance criteria — due Oct 20 2026 ("Сделаем сегодня") — [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]] [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — go through the reworked requirements and approve them in a comment, so they become final — due Oct 20 2026 — [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]] [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — ask Sebastian to connect the ports through bill validators and counters on all borrowed machines except the Banilla — due Oct 20 2026 (machines go back Friday) — [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — send the list of bill validators on all the machines and check the machines' settings — due Oct 20 2026 ("Сейчас мы это сделаем") — [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]] [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — check which SAS commands the Banilla supports (left as it is) — due unspecified — [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — create the tasks for testing with the third-party machines — due unspecified — [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] with [[wiki/people/alexei-khamin.md|Alexei Khamin]] and [[wiki/people/ivan.md|Ivan]] — create and start the automated-test tasks for bill-validator emulation mode — due the coming week — [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]] [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — write the story for Alekseev to make the Flex-Port build production-ready — due unspecified — [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]] [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]

## Open questions

- Should JVL read SAS data from other makers' machines at all, and sell it? Klimovich proposed it; Val doubted, then liked the wording; no product decision — [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]] [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- Do replacement bill acceptors of other makes fit the same cabinet connector and work with JVL's port? To be checked on the four on hand — [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- Which Wednesday is the MVP 1 release? Not stated — [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]

**§15.8:** clear — the $30–50 a month is a product price. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
