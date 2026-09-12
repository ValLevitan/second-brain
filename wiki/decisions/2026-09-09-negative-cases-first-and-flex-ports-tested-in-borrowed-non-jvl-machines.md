---
type: decision
title: Testing starts September 15 with the negative cases first, and Flex-Ports must be proved in borrowed non-JVL machines — fake-commissioned, tracked as a separate Jira item from JVL-machine testing
date: 2026-09-09
aliases: [negative cases first, door open, borrow a machine fake commission it, Aristocrat and Light and Wonder, at least one or two machines, two separate records, two different router manufacturers, no Chinese manufacturer, stay away from Cisco, ten port router, storm through the test, bracket drawings to Genadi]
source-count: 4
status: active
open-commitments: 4
open-questions: 0
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

## Open commitments

- [ ] [[wiki/people/felipe-miranda.md|Felipe Miranda]] — arrange one or two non-JVL machines to borrow for Flex-Port testing (Aristocrat and Light & Wonder preferred, even for a single day) — due Sept 15 2026 — [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]] [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [ ] Unassigned (the source names no owner) — get the bracket drawings released by Light & Wonder, IGT, Banilla and Aristocrat and pass them to Genadi Peari — due unspecified — [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [ ] Unassigned (the source names no owner) — source and test routers from two different manufacturers, no Chinese brands, avoiding Cisco; they are borrowable for a day or two only — due Sept 15 2026 — [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]] [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — record the Flex-Port SAS testing as two separate items, JVL machines and other suppliers' machines — due unspecified — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

**§15.8:** clear.

## Sources
- [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
