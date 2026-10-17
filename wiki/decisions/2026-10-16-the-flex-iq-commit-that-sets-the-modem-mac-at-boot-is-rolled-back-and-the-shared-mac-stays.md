---
type: decision
title: The Flex IQ commit that sets the modem's MAC address at boot is rolled back — it breaks the modem link — and the one MAC address shared by all modems stays as "the lesser evil"; a modem that does not come back after a connection-priority change is a bug to fix
date: 2026-10-16
aliases: [modem MAC rollback, Flex IQ MAC commit rolled back, same MAC on all modems, одинаковый mac адрес на всех модемах, меньшее зло, the lesser evil, неправильный фикс mac адреса, modem does not come up after connection priority change, modem up only after reboot]
source-count: 2
status: active
open-commitments: 2
open-questions: 1
---

# The Flex IQ modem-MAC commit is rolled back; the shared MAC stays

Said by [[wiki/people/pavel.md|Pavel Frolov]] at the [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct-16 Minsk stand-up]] (Russian; Val was not there) [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]].

## What the commit did

- **The problem it tried to fix.** All the modems carry the same MAC address: "макадрес одинаковый на всех модемах" [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]].
- **The change.** Pavel made it with "Дима": when Flex IQ boots and sees a modem of this model, it sets a MAC address on it — "он выставляет mac, привязанный к интернету" [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]. Which Dima is not said. Kovalchuk was in the meeting, and Chudinov was on vacation; Chudinov is likely (**inference**).
- **Why it fails.** "Это не работает. Более того, это ломает вообще работу модема." The MAC does change, but the modem then checks something inside and the modem link drops [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]].

## The ruling

- **Roll it back.** "на флекса айкью надо будет откатить один camit" — Pavel takes the task himself: "Убрать вот этот вот неправильный фикс mak адреса" [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]].
- **Why a shared MAC is acceptable.** "одинаковый mac адрес на всех модемах это не проблема. Сеть продолжает в таком режиме работать… это меньшее зло." [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] The notes record it as Pavel's decision [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]].

## The same morning — a modem that does not come back

[[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] opened a story, so far in the backlog: after the connection priority is changed, the modem does not come up until a reboot — "после перезагрузки он поднимается, но автоматически нет" [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]. Pavel: "выглядит то, что так не должно быть. Да что надо надо фиксить." Vladimir will show it and move the story on once Pavel confirms [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]].

## Where it sits

- Each device carries its own LTE modem and SIM — [[wiki/decisions/2026-09-15-every-device-carries-its-own-lte-modem-and-sim.md]]. This page is about how those modems behave on Flex IQ.
- Wi-Fi on the Flex-Ports and Flex IQ is now half of MVP 2 — [[wiki/decisions/2026-10-15-mvp2-is-flex-iq-wi-fi-remote-update-diagnostics-and-galaxy-reporting-and-flex-pay-moves-to-mvp3.md]] (Oct-16 update).

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — roll back the Flex IQ commit that sets the modem MAC at boot — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [ ] [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] — show Pavel the modem that does not come up after a connection-priority change, and move the story out of the backlog once confirmed — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]

## Open questions

- Who fixes the modem that comes back only after a reboot, and when? Pavel said it needs a fix but named no owner — [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]

**§15.8:** clear — device behaviour only. **§15 #9:** clear — no MAC address or other identifier value was spoken.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
