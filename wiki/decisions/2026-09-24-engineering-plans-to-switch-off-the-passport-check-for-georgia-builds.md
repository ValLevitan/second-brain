---
type: decision
title: The engineers plan to switch off the Passport check for Georgia builds, with a server flag so RIS creation stops filtering by Passport — near-term, alongside restoring the last RIS
date: 2026-09-24
aliases: [disable the passport check for Georgia builds, паспорт отключить для джорджевских билдов, выпиливание проверки паспорта, do not filter machines by passport, не фильтровать машину разрешать все, remove the passport from DC, nearest releases vs medium term]
source-count: 2
status: active
open-commitments: 3
open-questions: 1
---

# The engineers plan to switch off the Passport check for Georgia builds

**Status note:** active as an **engineering plan**, set by [[wiki/people/pavel.md|Pavel Frolov]] at the [[wiki/meetings/2026-09-24-georgia-hard-reset-remedies-and-passport-removal.md|Sept 24 2026 5:41 AM review]] with [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] and [[wiki/people/ivan.md|Ivan]]. **Val was not on the call.** At 7:02 AM the same morning Val defended the Passport scan (see Open contradictions below). No source yet says whether the plan goes ahead [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]].

## What was decided

- **The plan.** Pavel: "Я думаю, что нам надо сейчас просто принять решение, что паспорт на самом деле отключить для джорджевских билдов, наверное, несложно. И наверное, нам это просто надо запланировать и сделать" — we should simply decide now to switch the passport off for the Georgia builds; it is probably not hard; we just need to plan it and do it. Irina: "Да." [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]
- **Is it hard?** Pavel asked whether removing the passport check for the Georgia build is "в общемто несложно". Evgeny: "Но в целом да… Я уже говорю что в целом да." [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]
- **Where it is switched off.** Pavel wrote it down as "дата центр мы убираем. Паспорт. Из DC" — the passport comes out of the data center (read as the machine-side data store; **inference**). He also floated the alternative that the passport is still stitched in automatically but nothing is sent to the server. [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]
- **The server flag it needs.** Irina raised the consequence: when a RIS is created, "какието машины начнут… Не подхватываться" — a machine wanted with TITO while its passport says it has none — "И начнутся конфликты при создании риса." Pavel agreed ("да ира права") that at install the server shows only machines that match the passport, and set the fix: on the server, "галочку, которую говорит о том, что не фильтровать машину разрешать все" — a flag that says do not filter machines, allow all. Irina confirmed RIS creation already offers only machines "Первоначально… зарегистрированы в джорджии". [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]
- **The TITO check does not depend on it.** Irina worried that a machine that must have TITO would lose its check. Pavel: "Так это не в паспорте… если рис прошли с тито, а принтер потом отключили, но он будет ругаться, что принтер не найден. Это с паспортом… не связан." [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]

## Why

The passport forces an update after a factory reset whenever a bill acceptor was swapped, and operators swap bill acceptors often without decommissioning. The technician then meets a screen he cannot pass: he must photograph the QR code, send it to a JVL person, and wait for a reply "течение 15 минут" before work continues. Pavel: "Им это не надо." [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]

## Near-term and medium-term

Evgeny asked whether the list was for "здесь и сейчас" or for gathering and doing "красиво в будущем". Pavel's split [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]:

- **Nearest releases:** "выкосить этот самый паспорт это легко делается, а снимает, наверное, большой кусок проблем", and restoring the RIS from the backup "тоже, в общемто выглядит как несложно".
- **Medium term:** the soft resets and the partly manual initial setup — "среднесрочный этот планирование".
- **Which platform:** "Я не знаю, это для для рейдж или для нова, не знаю, может быть и так и так."
- **His estimate at the close:** the short-term fixes "могут закрыть, наверное, там 70%… Проблем такое чувство у меня."

The other cases and answers are on [[wiki/topics/ris-remote-install-and-machine-states.md]] (Sept 24, 5:41 AM).

## Open contradictions

- **Switch it off (engineers, 5:41 AM) vs keep it (Val, 7:02 AM), same morning.** This page's plan removes the passport check for Georgia builds [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]. Later the same morning Val said of the passport scan: "I think this feature is tremendous… And if you disable it, you're in a way you're losing", and on applying settings over mismatched hardware, "Okay, so restricted. Do not allow." [[raw/Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026.md]] The plan was not raised by name in the 7:02 AM meeting, and Val's Sept-11 ruling was that the passport "нужно сохранить" ([[wiki/decisions/2026-09-11-the-passport-is-preserved-and-jvl-is-using-the-bindings-wrongly-in-this-market.md]]). On Sept 23, Val himself had proposed a release with no reference to the passport ([[wiki/topics/ris-remote-install-and-machine-states.md]], Sept 23). **Recorded, not resolved.**

## Open commitments

- [ ] Pavel Frolov — plan and schedule the removal of the passport check from the Georgia build — due unspecified — [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]
- [ ] (owner not named) — add the server flag that stops RIS creation filtering machines by passport — due unspecified — [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]
- [ ] Pavel Frolov — ask "сегодня" whether technicians must scan the statistics QR during a factory reset, and whether Georgia can default it off (a separate parameter from the secure factory reset, which needs the flash drive; the parameter exists and is on) — due Sept 24 2026 — [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]

## Open questions

- Does the Georgia-build passport switch-off go ahead after Val's 7:02 AM defence of the passport scan? — [[raw/Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026.md]]

**§15.8:** clear — product design only.

## Sources

- [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]
- [[raw/Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026.md]]
