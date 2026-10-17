---
type: decision
title: For MVP 2, Biratka reviews the existing capabilities, drops the outdated or wrong ones and ports Flex IQ's to FlexPay by analogy — but writes no new ones until Klimovich, back on October 13, has thought through the user and administrator flows
date: 2026-10-01
aliases: [MVP 2 capabilities method, Biratka ports Flex IQ capabilities to FlexPay, по аналогии с флекса IQ, no new capabilities without business confirmation, user and admin flows, со стороны юзера и администратора, Klimovich back October 13, до 13 октября, оптимальный подход, Biratka MVP 2 cleanup]
source-count: 7
status: active — Oct 15 2026: Val takes Flex Pay out of MVP 2 (to be retagged MVP 3), so the Flex Pay porting serves MVP 3; see the Oct-15 update
open-commitments: 2
open-questions: 1
---

# For MVP 2, Biratka ports Flex IQ's capabilities to FlexPay and writes no new ones until the flows are defined

Agreed between [[wiki/people/alexander-biratka.md|Alexander Biratka]] and [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] at the [[wiki/meetings/2026-10-01-transactional-mvp1-status-slice-and-sas-command-logging.md|Oct-1 8:02 AM MVP 1 call]] (Russian), in its MVP 2 part [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]].

## Biratka's method

[[wiki/people/pavel.md|Pavel]] opened the MVP 2 part: "саша сегодня говорил, что у него задачи заканчиваются. Ему только надо навести порядок с [capabilities]" — Biratka had said at the morning stand-up that his main FlexPay tasks are ending. Biratka, asked for MVP 2 questions: "Ну у меня нету." Then the method [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]:

- **Review and drop.** "если Андрей как бы сейчас не занимается [capabilities] сами, я как бы просто просмотрю то, что у нас сейчас сделано… которое я считаю, что оно как бы не актуальное или вообще ошибочное. Да я могу его отбросить просто."
- **No new ones.** "**новых я особо писать не хочу, потому что они получатся такие незаконченные, без, так сказать, подтверждения со стороны бизнеса.**"
- **Port by analogy.** "То, что у нас… во флекса IQ сделано и то, что относится к флекспею, то есть я это всё переношу и… создаю [capability] по аналогии с флекса IQ. Это все нормально идет так как… там бизнесмодель продумана."
- **The business flows are the gap.** "Бизнес флот, так сказать, он же ж ещё не проработал… надо. Чтоб Андрей со стороны юзера, там и со стороны там администратора продумал вот эти вот все пути."

## Klimovich's endorsement, and the dates

"по датам расклад такой что я до своего возвращения до 13 октября реально не смогу ничего толком писать. И Более того, на следующей неделе со вторника по четверг исключительно я даже на дейликах не смогу быть полную полное отсутствие. Да, поэтому то, как ты сейчас двигаешься, это оптимальный подход… что можно реализовывать вперёд." Biratka: "Да да я реализую." [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]

## Where it sits

- It continues the Sept-28 arrangement that Biratka collects MVP 2 business questions by email ([[wiki/decisions/2026-09-24-written-records-go-by-email-and-chats-are-for-instant-matters.md]], Sept-28 update) and the Sept-30 shape of MVP 2 — FlexPay in the slim form factor — on [[wiki/decisions/2026-09-09-one-transactional-unit-per-location-until-the-wi-fi-iteration.md]] (Sept-30 update).
- The "no capability without business requirements" line is Chudinov's Sept-10 objection on [[wiki/decisions/2026-09-10-requirements-come-first-and-the-recycler-is-out-of-both-mvps.md]], now applied by Biratka to his own work.
- The derived notes record the same decision and attribute it to Biratka, "endorsed by Andrei Klimovich" [[raw/Meeting_Notes_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]].

## Update, Oct 5 2026 — Val: MVP 2 writing starts when Klimovich is back

At the [[wiki/meetings/2026-10-05-transactional-mvp1-port-screens-unclaimed-money-and-printer-models.md|Oct-5 8:01 AM MVP 1 call]] (Russian), [[wiki/people/val-levitan.md|Val]]: "Когда Андрей выйдет из отпуска, тогда он начнет писаться мвпи 2. Все остальные вопросы придерживаем" — consistent with this decision. [[wiki/people/andrei-klimovich.md|Klimovich]]: "Я 12 прилетаю только я мог бы 13" [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

## Update, Oct 14 2026 — Klimovich, back, starts the MVP 2 talk with Val; Val's priority list

At the [[wiki/meetings/2026-10-14-transactional-mvp1-launch-plan-brackets-daily-caps-and-mvp2-scope.md|Oct-14 3:49 PM launch-plan meeting]] (Russian), [[wiki/people/andrei-klimovich.md|Klimovich]] opened MVP 2 "высокоуровнево" [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]:

- **His frame.** MVP 2 means slim dispensers working together with the Flex IQ, at a location that has a Flex IQ and a display. The slim's interface logic is "большая работа, которая от меня сейчас зависит", and must go to the developers.
- **[[wiki/people/val-levitan.md|Val]]'s list.** "я бы на MPP2 обязательно бы сделал бы Wi-Fi"; finish connection and diagnostics, with a screen where the location sees what does not connect; a basic inspector report (Klimovich: there is none now); cash-out split into up to nine categories the location defines — "Ларовые тикет, бензин, гросериз" — "Почему девять? Потому что это самое большое однозначное число"; remote update and reconnection "отполировано" for Flexport and Flex IQ, first in line if one more improvement fits; optional features made configurable (the TIN code is the example); low-funds notices to operators by SMS; and signing of all contracts through DocuSign, Dropbox or similar — Klimovich named PandaDoc — from templates, with tracking of each contract's stage and reminders.
- **Not now.** "Я бы пока другую интеграцию не трогал" — no new card integrations.
- **Pace.** Val: MVP 1, 1.5 and 2 together, the first fifty locations will take "Месяца три".

The derived notes list the same items under "MVP2 scope (discussed)" [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]. *(This is a priority list from Val, not yet written capabilities; it gives Klimovich's Oct-1 flows work its starting content — **inference**.)* A per-unit cloud backup was agreed in the same talk — [[wiki/decisions/2026-10-14-the-first-cloud-step-is-a-backup-of-each-flex-iq.md]].

## Update, Oct 15 2026 — Val takes Flex Pay out of MVP 2

At the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian), asked by Irina whether MVP 2 is Flex IQ or Flex Pay ("flex pay идёт как [MVP] 2"), [[wiki/people/val-levitan.md|Val]] said "Андрей" (Klimovich, by context — **inference**) had argued for Flex Pay, but he would leave it out: MVP 2 = Flex IQ, Wi-Fi configuration, remote update for the Flexports and Flex IQ, diagnostics, and Galaxy transactional brought up to reporting and dashboards, plus the location shortfall paid by card. Pavel will take the MVP 2 mark off Flex Pay and relabel it MVP 3. Val is still polishing the list "с Андреем", after which Andrei starts with the team; "Андрей может написать только [функциональные requirements]" — the rest must come from the engineers. Full record: [[wiki/decisions/2026-10-15-mvp2-is-flex-iq-wi-fi-remote-update-diagnostics-and-galaxy-reporting-and-flex-pay-moves-to-mvp3.md]] [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

**What it means here (inference).** Biratka's Oct-1 work of porting Flex IQ capabilities to Flex Pay now serves MVP 3, not MVP 2. Klimovich's flows commitment below stays open; its subject is now Val's MVP 2 list.

## Open commitments

- [ ] [[wiki/people/alexander-biratka.md|Alexander Biratka]] — go through the MVP 2 capabilities: drop the outdated or wrong ones, port the Flex IQ capabilities that apply to FlexPay by analogy, write no new ones — due while Klimovich is away (until Oct 13 2026) — [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — think through the MVP 2 user and administrator flows so new capabilities can be written — due after Oct 13 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]

## Open questions

- The MVP 2 user and administrator flows themselves — "ещё не проработал" — [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]

**§15.8:** clear — work method and dates only; Klimovich's absence is recorded as a schedule fact, nothing more. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
