---
type: decision
title: A terminal that was registered before must have its old secrets wiped at install — press each letter on the final player screen four times — so it re-enters registration and gets new cloud-update certificates; the install instruction carries this as a separate red section
date: 2026-10-09
aliases: [wipe secrets, зачистить секреты, press each letter 4 times, каждую букву нажать 4 раза, re-registration mode, режим регистрации, new certificates for cloud update, red section in the install instruction, выдели красным, terminals registered before, same number is fine]
source-count: 2
status: active
open-commitments: 1
open-questions: 0
---

# A re-used terminal wipes its secrets, and the instruction says so in red

**Decided** by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] on the [[wiki/meetings/2026-10-09-transactional-mvp1-test-machines-and-unclaimed-funds.md|Oct-9 Transactional MVP 1 call]] (Russian), on [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]'s explanation.

## The rule

Chudinov, for terminals "которые уже у вас были. Регистрировались ранее", if the same environment is still there: "там надо зачистить секреты… когда через с д карту ставишь в конце на экранчике этого игрока плеера… надо… каждую букву нажать 4 раза друг за другом. Такой вот такой вот хак он сотрёт старые секреты." [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]

- **Why.** Otherwise the terminal "считает себя зарегистрированным, и тогда мы не создадим новые сертификаты для. Обновление через облако." The wipe puts it into registration mode [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]].
- **Then.** Register the terminal again — "можно с тем же номером не критично" [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]].
- **Pavel's check.** Is this a factory reset that wipes the disks and forces re-registration? Bosik: "Терминал, а не машины тут." [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]

## The instruction

Klimovich: "Выдели красным как отдельную секцию с пометкой, что на случай, если эта установка идёт на машины, которая ранее регистрировались." Later Chudinov: "Я я уже я уже поправил." [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]] Klimovich will then ask [[wiki/people/elizabeth.md|Elizabeth]], today or Monday, to connect the Flex IQ, install the latest builds with the secrets wipe, and join it to the full set-up [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]].

This touches the cloud update of [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] and the Georgia set-up of [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]].

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — ask Elizabeth to connect the Flex IQ, install the latest builds with the secrets wipe, and join it to the full set-up — due Oct 9 or Monday Oct 12 2026 ("сегодня или в понедельник") — [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]

## History

- [x] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — put the secrets wipe in the install instruction as a red section — discharged on the same call ("я уже поправил", Oct 9 2026) — [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]

**§15.8:** clear. **§15 #9:** none; no secret or certificate values appear.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
