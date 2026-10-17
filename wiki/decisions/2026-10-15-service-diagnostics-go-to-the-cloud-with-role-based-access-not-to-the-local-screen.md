---
type: decision
title: Service and diagnostic data are made available in MVP 2 in the cloud, not on the device's local screen, with role-based access (RBAC) — Grafana stays the staff view for now, and SSH access to any terminal is an MVP 3 idea
date: 2026-10-15
aliases: [diagnostics in the cloud, обязательно в клауд, nobody touches the local screen, service diagnostics MVP 2, role-based access control, RBAC, ролл бейсит аксес контрол, owner and operator access levels, Grafana dashboards for staff only, клиенты эти дашборды не видят, SSH access to every payment terminal, MVP 3 SSH console, Claude reads Grafana through MCP]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
---

# Service diagnostics go to the cloud, with role-based access

Ruled by [[wiki/people/val-levitan.md|Val]] at the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian) [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## The ruling

- **In MVP 2.** Val: "Теперь давайте все сервисные… диагностической сервисные элементы сделаем доступными [в MVP] 2." [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- **In the cloud.** [[wiki/people/andrey-bosik.md|Bosik]] asked: on the terminal screen or in the cloud? Val: "Хороший вопрос… это надо делать обязательно в клауд" — with it in the cloud "ты даже можешь рассылать SMS людям"; on the local screen "никто прикасаться не будет" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **With access levels.** Val wanted "доступ на разные [уровни] — хозяину свой доступ там оператору свой доступ"; the word he was looking for was given as roles, and Bosik spelled it: "ролл бейсит [access control]… rback сокращённо" — **RBAC** [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- The derived notes: "Service and diagnostic data go to the cloud, with role-based access… (Decided by Val)" [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## What exists today

- **Grafana, for staff.** [[wiki/people/pavel.md|Pavel]]: critical events on the payment terminals "уже отсылаются на клауд и складываются в графану". Bosik: everything JVL chose to log goes to Grafana, with dashboards built for developers and staff; "Клиенты эти даш[б]орды не видят и никогда в жизни не увидят." If customers need it, the data must be duplicated into JVL's own cloud dashboards — "я просто не знаю, надо ли её клиентам видеть" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **Claude reads it.** Pavel: Claude works very well through MCP; "дима", when he needed to understand a machine, got the information through Grafana even with the machine beside him (which Dima is not said) [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **RBAC is partly built.** Bosik: "Сергей ци[м]онов же это уже частично реализовал… это мы с Димой позавчера выкатили на прод" — [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] built part of it, and Bosik and "Дима" put it into production two days before; how deep it goes he does not know [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. *("Дима" is likely [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], who did production roll-outs with Andrei on Oct 12 — **inference**.)*

## Pavel's MVP 3 idea — the other direction

Pavel: in MVP 3, add to the firmware-management tool the ability for an operator, him or Andrei to open an SSH console on any payment terminal at any time and pull any logs or data "которые… изначально не были… спланированы". Val: "это прекрасно, но… это разговор в ту сторону, а я хочу, чтобы… разговор был в эту сторону от машины… через клауд" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Where it sits

- It extends [[wiki/decisions/2026-09-17-signal-quality-in-mvp1-means-remote-visibility-not-a-screen.md]] (remote, not a screen; Grafana as "task 2") from signal quality to all service and diagnostic data, and answers that page's open question for MVP 2: the data must reach a person, by role (Oct-15 update there).
- The Oct-14 MVP 2 list had asked for a screen where the location sees what does not connect ([[wiki/decisions/2026-10-01-mvp2-capabilities-biratka-ports-flex-iqs-to-flexpay-and-writes-no-new-ones-until-klimovich-defines-the-flows.md]], Oct-14 update). *Whether that screen is a cloud page or the device screen was not said on Oct 14; on Oct 15 Val ruled for the cloud — evolution, inference.*
- Power-loss and dropped-link alerts feed it — [[wiki/decisions/2026-10-15-payment-terminals-get-a-swappable-backup-battery-and-report-power-loss-so-service-can-be-called.md]].

## Open questions

- Should customers see the diagnostic dashboards? Bosik did not know; nobody ruled — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

**§15.8:** clear. **§15 #9:** clear — no address, key or credential was spoken.

## Sources
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
