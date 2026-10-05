---
type: decision
title: An autotest task whose scenarios are stopped by defects goes to "Blocked", not closed, and is raised at the next meeting — and the writer picks the next task that is closest to ready and moves its dates
date: 2026-09-30
aliases: [task 41 Blocked, в блок положить, blocked autotest task, Blocked not closed, raise at the next meeting, разблокировалась ли эта задача, pick the task closer to ready, более в готовом состоянии, move the dates, take any unassigned task, expired permission autotests, TINT-41 blocked, branch hanging]
source-count: 4
status: active
open-commitments: 1
open-questions: 0
---

# An autotest task that cannot finish goes to "Blocked", not closed

Ruled by [[wiki/people/pavel.md|Pavel Frolov]] at the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian), in answer to [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]]'s question on his first autotest task [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]].

## The case

Vladimir had done "41 задачу с экспайдная примешен" (task 41 — "expired permission" is a reading; on Sept 29 he had chosen TINT-41 as "самая понятная") and, from the results, logged "3 или сколькото дефектов и несколько задач на… доработку". His problem: "фактически я её не закончил, потому что… не могу сделать для всех сценариев сейчас" — the defects stop him covering every scenario. And the code: an unfinished autotest branch — "ветки… через пару дней мне начнут писать эти письма о том, что… у вас там бранч висит" — he expects the branch-hygiene mails to start. "Как поступать с такими задачами?" [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]

He had already linked the blocking tasks: "Задача в задачи я линканул… созданные, которые типа блокирует выполнение… И коммент есть" [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]].

## The ruling

- **Blocked, not closed.** Pavel: "можно вот в блок ты его пока что положить"; then, to the question itself: "**это как раз блок поставить, чтоб мы видели, что вот она заблокирована на следующем митинге поднять его ну разблокировалась ли эта задача или нет**" — set it to Blocked so the team sees it, and raise it at the next meeting to check whether it has been unblocked. Vladimir: "Понял." [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- **The next task: the one closest to ready, dates moved.** Vladimir will re-read the list, "скорее всего, один 48" (read as 148), though one task has an expiring deadline (the number is garbled). His worry: in some tasks "из 10 4 сценария я не могу пройти", in others "из 18 2 сценария я могу пройти" — "Смысл какие брать?" Pavel: "**ты ещё раз пересмотри, что из них более в готовом состоянии… логично туда сроки просто переставить. Соответствующим образом**" [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]].
- **Any unassigned task is fair game.** [[wiki/people/irina-shishko.md|Irina Shishko]]: "ты можешь выбирать любую задачу из тех, которые на ванне алёша" (on Ivan and Khamin — by context) "просто забрал на себя и всё так как я сейчас делаю. То есть на мне нет задач, но я просто их… нашла. Забрала" [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]].

[[wiki/people/irina-shishko.md|Irina]]'s one aside — "ты типа блок, потому что нужен там этот да я думаю что сделают эту айпишку или что там быстрее чем" — reads as agreement that the block is short-lived because the fixes will come fast (garbled; **inference**) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]].

The derived notes record the same ruling — "set it to Blocked and raise it at the next meeting", next task "maybe 148" [[raw/Meeting_Notes_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]].

## Where it sits

- It is a status rule inside the Jira discipline [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] asked for the same morning — "Смотрите за датами статусами" — see [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Sept-30 update).
- It applies the "defects first" shape of the autotest work on [[wiki/topics/test-automation-strategy.md]] (Sept 30, 4:57 AM): the test is written, the defects it finds are filed and linked, and the task waits on them.
- The unfinished branch is not ruled on; the branch-hygiene mails Vladimir expects are the GitHub ones on [[wiki/topics/github-release-management-pipeline.md]] (link is context, not a citation).

## Oct 5 2026 — annotation: a FlexPay-derived task that "скорее всего, вообще блок надо"

At the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian) the same shape came up on [[wiki/people/anton-seregin.md|Seregin]]'s board. Pavel: "здесь что то висит вот до 2 октября тут надо либо сроки." Seregin: "это, скорее всего, вообще блок надо, потому что это с флекс [пэем] мы так ничего не поняли, как что там дальше делать?… там просто какоето описание было всё, что он нашёл. На этом невозможно ничего [инаследовать]"; the earlier FlexPay implementation "не [смержил] никуда. Вот какойто там ветки то ли что." Pavel: "Ладно." Whether it was set to Blocked is not said [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]. (Recorded here as a second case of the rule.)

## Open commitments

- [ ] [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] — set task 41 to Blocked with the blocking defects linked; raise it at the next meeting; pick the next autotest task that is closest to ready (probably 148) and move its dates — due Sept 30 2026 — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]] — *Oct 1 2026: at the next stand-up he reported "Сегодня ещё прошёлся по 7 41 задачи со своим уже портом и [эмулятором SAS]. Один [блокер] снимался, доделал" — a blocker was lifted and he worked the task further; whether it was set to Blocked, and which task he took next ("34 лакейшн блок тейкс" — garbled; 148 is not said), is not stated; nobody raised the task's status at the meeting* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]] — *Oct 5 2026: he reported task 769 (screens and texts); 41 and 148 were not mentioned* — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

**§15.8:** clear — Jira process only; no named person's pay, rate or performance judgement. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
