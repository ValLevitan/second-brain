---
type: decision
title: Testing starts September 15 with the negative cases first, and Flex-Ports must be proved in borrowed non-JVL machines — fake-commissioned, tracked as a separate Jira item from JVL-machine testing
date: 2026-09-09
aliases: [negative cases first, door open, borrow a machine fake commission it, Aristocrat and Light and Wonder, at least one or two machines, two separate records, two different router manufacturers, no Chinese manufacturer, stay away from Cisco, ten port router, storm through the test, bracket drawings to Genadi]
source-count: 6
status: active
open-commitments: 7
open-questions: 2
---

# Negative cases first, in borrowed non-JVL machines, from September 15

Stated in both Sept 9 2026 meetings. The **why** is the same in each: SAS behaves differently on other manufacturers' machines, and that is where the programme will break.

## The date

- **Rollout meeting:** "in order for us to physically install by first of October, we need to **start experimenting with it here on the fifteenth of September**. Next week" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]].
- **Engineering call:** "**15 сентября**[,] в Джорджии должен быть работающий прототип" — a working prototype in Georgia by September 15 [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. See [[wiki/projects/georgia-market-rollout.md]].

## Negative cases come first

- "[T]he first thing that we should be testing **are negative cases**… For example, **door open**. That's the behavior. I don't want to go into granular details. I just want to stay on generalized" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]].
- In the engineering call Val put the same case in SAS terms: "[с]ас посылает какую[-]то команду и [Flex-Port] должен отреагировать на это" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. The door-open and machine-blocked flags are the same ones [[wiki/people/pavel.md|Pavel]] wants built as a Flex-Port feature — see [[wiki/decisions/2026-09-09-three-more-flex-port-features-onto-capability-165.md]].
- Val's general instruction on ordering positive before negative work is on [[wiki/decisions/2026-09-07-error-recovery-and-non-functional-requirements-come-first.md]]; this is the field-test expression of it.

## Non-JVL machines: borrow, fake-commission, fake-test

- **What is needed:** "we need to install our flex ports into **non-JVL machines, at least one or two machines. I prefer Aristocrat and Light and Wonder**, if possible, **even for one day**" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]].
- **They cannot be bought or properly commissioned:** "we're not buying… we need to **borrow** it. We need to bring it here. I don't know. Can we even commission them? Here, we cannot. But can we test them? **Fake commission.** So we have to fake commission it and fake test it" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]].
- **A machine, not boards:** "Not boards, **a machine**. You don't want to fuck around with anything else. You want to bring the machine here for a couple of hours, test it" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]].
- **[[wiki/people/felipe-miranda.md|Felipe]] arranges them:** "of course, Felipe, you have to arrange the machines" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]].
- **In Russian, the same requirement:** "мы должны взять машины у других [саплаеров]… подключить флекс[-]пор[т] к сасу"; "хотя бы ещё одну машину должны иметь" [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. The derived notes flag that Val never named who obtains the machine in that call [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

## Track the two test populations separately

Pavel's ask, and the reason for it: "эти вот кейсы их надо отразить в виде **2 разных записей**[:] что мы в какой[-]то момент начинаем тестировать нашими машинами и у нас в каком[-]то виде транзакции идут. И **2 пункт[ —] это с чужими машинами**. Я думаю, мы здесь можем поймать сразу же с[ъ] лёта проблему" — he expects third-party machines to throw a problem immediately [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

## Brackets: the drawings have to come from the machine makers

"**Brackets.** You have to get the drawings from **Light and Wonder, IGT, Banilla, and [Aristocrat]**, and **they must release it to you. They will**… Just get the drawings and give it to [[wiki/people/genadi-peari.md|Gennady]]" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]. *(The fourth name is rendered "Arista Products" in the transcript; Val had said "Aristocrat" five minutes earlier in the same meeting, and the derived notes read it as Aristocrat [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]. "Banilla" is as spoken. No owner is named for fetching the drawings.)* The bracket production path itself is on [[wiki/decisions/2026-09-04-brackets-and-harnesses-from-china-and-a-metal-order-for-one-hundred.md]].

## Routers

- **Two manufacturers, and two exclusions.** "you have to test at least **two different manufacturers**… And you need two types, two different manufacturers. **Try to stay away from Cisco. Crazy money. No Chinese manufacturer**" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]].
- **Port count and borrowing constraint.** "It would be hard pressed to find a **10 port router**"; "you can only borrow it for a day or two. Nobody will give it to you… So you have to set everything up and **storm through the test**" [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]].
- The external router is the one specified on [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]].

## Update, Sept 22 2026 — other makers' machines not yet tested, and expected next month

At the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 8:01 AM MVP 1 call]] Pavel described the state of Flex-Port testing: "Мы, мы сейчас работаем в окружении с нашими машинами"; how SAS works on others' machines "Мы не знаем, мы это узнаем только по факту подключения". Tests of real Flex-Ports "подключенных к чужим машинам, например, в Джорджия офисе… скорее всего, растянется ещё на следующий месяц" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

[[wiki/people/val-levitan.md|Val]] agreed there will be problems there, and set the order: first end-to-end tests on JVL's own equipment, the rest later. See [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]]. **The Sept-15 start in borrowed non-JVL machines had not happened by Sept 22** on this evidence; the rule itself was not withdrawn. Felipe's machine-borrowing commitment below was not mentioned.

## Open commitments

- [ ] [[wiki/people/felipe-miranda.md|Felipe Miranda]] — arrange one or two non-JVL machines to borrow for Flex-Port testing (Aristocrat and Light & Wonder preferred, even for a single day) — due Sept 15 2026 — [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]] [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [ ] Unassigned (the source names no owner) — get the bracket drawings released by Light & Wonder, IGT, Banilla and Aristocrat and pass them to Genadi Peari — due unspecified — [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [ ] Unassigned (the source names no owner) — source and test routers from two different manufacturers, no Chinese brands, avoiding Cisco; they are borrowable for a day or two only — due Sept 15 2026 — [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]] [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — record the Flex-Port SAS testing as two separate items, JVL machines and other suppliers' machines — due unspecified — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

**§15.8:** clear.

## Update, Sept 25 2026 — how the test is set up: office not warehouse, JVL machines first, after October 1

At the [[wiki/meetings/2026-09-25-transactional-mvp1-flexport-third-party-egm-compatibility-testing.md|Sept-25 8:05 AM MVP 1 call]] (Russian) [[wiki/people/andrei-klimovich.md|Klimovich]] raised it as not yet discussed: "Что мы будем делать с тестированием… на сас с разными моделями машин разных производителей?" [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]

- **The machines.** Klimovich: JVL has "предварительная договорённость с несколькими большими операторами" who will let JVL into their warehouse or lend a few machines for "день 2" (read as a day or two). The test would most likely be done by [[wiki/people/elizabeth.md|Elizabeth]], perhaps with a local technician, who need "понятный воркфлоу" and a manual. Once Minsk gives the signal, the local team contacts the operators and sets dates [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]. *(The Sept-9 commitment put the borrowing on Felipe; on Sept 25 Klimovich speaks for "мы" — the local team. Whether the job moved is not said.)*
- **Pavel's set-up — two SAS ports.** Bring the machine to the office and connect it to the internal network Minsk can reach. "Нам надо подключать 2 сасса": on the first, the SAS accumulator [[wiki/people/ivan.md|Ivan]] works with, which sends commands such as lock, unlock and accounting requests — ideally every command InComm and Intralot send; on the second, the Flex-Port. Check that no function breaks under third-party commands, and that Flex-Port can pass money, take money, track the machine's state and show it [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]].
- **Record the raw SAS traffic.** [[wiki/people/dmitri-chudinov.md|Chudinov]] proposed that IQ and the port send the SAS commands the machine sends to a website, so JVL's machine and another's can be compared directly, not through logs. Pavel had a similar "дампер" idea and asked whether it should run in production — all SAS commands except pings. Chudinov: "Да я я бы собирал, потому что будет полезно." Klimovich noted this data holds money in and out down to each game title. Pavel: "это явно… не один это может быть MVP 23" — not MVP 1; Klimovich agreed [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]].
- **Office, not warehouse.** Biratka asked whether a warehouse is better, since the owner's staff can help. Irina: "нам туда не будет доступа"; Chudinov: network access is needed. Pavel's hybrid: take one or two machines first; if all works, "уверенно ехать в в любой варихаус" until a problem shows. Val first asked why location matters if there is a modem, then said he had misunderstood. Pavel: a remote modem is another network and needs a wrapper; Chudinov: modem access is "отдельная задача… Сложная" [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]].
- **What the site needs** (Ivan): the right cables; a computer for the SAS emulator with a COM port, best from the motherboard — USB-to-COM works but gives problems; at least two cables, one from the Flex-Port and one from the emulator; and the IGT SAS host simulator he uses (transcript "Ig t sхозсемолета"; reading from the notes). Klimovich: "сейчас ни у кого ничего нету" — it all goes in the manual [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]].
- **Which commands.** [[wiki/people/irina-shishko.md|Irina]]: there is a document with every command a machine must support, used for certification — go through it. Ivan: the risk is a maker adding something new [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]].
- **JVL's own machines first.** Irina: "сначала бы на наших машинах пройти эту процедуру", with a near-final port and IQ; Elizabeth checks on a JVL machine, then repeats it on another maker's. Klimovich: "Поддерживаю" [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]. This is the order Val set on Sept 22 (above).
- **After October 1.** Klimovich asked whether testing can start without IQ, which is not ready. Pavel: a machine emulator exists and an IQ emulator is coming. Chudinov: "Не будет акмулятора к 1 числу"; he would test with the terminal and add the SAS capture first. Klimovich: "Ну хорошо, тогда после 1 октября." Biratka: nothing stops the instruction starting now [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]].
- **Tracked in Jira.** Klimovich will create a capability from the transcript. Pavel's wording: "флекспорт должен иметь возможность работать с cota EGMS" ("cota" unclear as spoken); first task, describe the procedure and equipment; Flex-Port changes may follow once real machines are tried. Irina: Ivan writes the instruction and attaches the emulator and the commands document. Ivan: "Я к понедельнику постараюсь всё это сделать." Pavel on the task: "Создаем, конечно" [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]].
- **The site's kit.** Klimovich: "у нас есть все девайсы, у нас есть все харнесы"; missing parts arrive in a couple of days; there are Flexes of all kinds and Alters [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]].

**Against the Sept-9 rule.** The rule stands and gets a method. The Sept-15 start did not happen; on this evidence third-party testing now waits until after October 1 (evolution, not a contradiction). A separate capability for other makers' machines moves toward Pavel's Sept-9 ask for two separate records, but the JVL-machine item is not mentioned, so his commitment stays open.

### Open commitments (Sept 25 2026)

- [ ] [[wiki/people/ivan.md|Ivan]] — write the set-up instruction for the compatibility test (hardware, cables, COM port, SAS emulator) and attach the emulator and the SAS commands document — due Mon Sept 28 2026 ("постараюсь") — [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — create the capability for Flex-Port working with other makers' machines, from the transcript — due unspecified — [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]
- [ ] Klimovich and the local team — once the set-up arrives, contact operators, borrow machines, bring them to the office and connect them to the MikroTik — due after October 1 — [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]

### Open questions (Sept 25 2026)

- Should Flex IQ record all SAS commands (except pings) in production? Chudinov: yes; Pavel: not MVP 1. Not settled — [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]
- Can the SAS accumulator send every command InComm and Intralot send? Pavel's "в идеале"; not answered — [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]

## Sources
- [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]
