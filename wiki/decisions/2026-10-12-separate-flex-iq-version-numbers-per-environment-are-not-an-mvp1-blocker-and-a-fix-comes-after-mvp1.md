---
type: decision
title: Each environment (STG, production) keeps its own Flex IQ version counter for now — production starts again from one; not an MVP 1 blocker, and finding a shared numbering is a task after MVP 1
date: 2026-10-12
aliases: [Flex IQ version numbers per environment, у каждого инвамента свой набор, production starts from one, начнёт с единички, GitHub sets the version, version numbering after MVP1, не блокер, shared version numbers]
source-count: 2
status: active
open-commitments: 1
open-questions: 0
---

# Separate Flex IQ version numbers per environment: not an MVP 1 blocker

Raised by [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau") and ruled by [[wiki/people/pavel.md|Pavel Frolov]] at the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 Minsk stand-up]] (Russian). Quotations from [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].

## What Chudinov said

"Были все в курсе, текущая реализация, текущая реализация такая. У каждого инвамента свой пока набор" (of versions) — each environment has its own set of version numbers, so production "начнёт с единички" (starts from one). The number is reserved in a storage that is unique per environment, so he has no idea yet how to share it; "может хранить там на гите". "Пока это не блогер" (read as блокер, not a blocker); the number "всегда можно будет поднять".

Pavel: "Хм это да, это нехорошо." He checked the scope: "Это мы говорим сейчас про версию флекса [IQ]. Который будет распространяться через раук, да, то есть удалённое обновление." Chudinov agreed (RAUC; see [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]]).

## The idea that did not fit

Pavel proposed fixing the first three numbers in GitHub and letting only the fourth differ. Chudinov: the fourth number is the build number, "она инкриминируется гетхабом", and GitHub sets the first three automatically too — "Иначе разработчик будет забывать постоянно". Pavel: "Тогда… это чтото странное, честно говоря." Chudinov: "это ж не блокер для MVP."

## The ruling

Pavel: "Задача будет тогда. После [MVP] один подумать, как правильно с этой задачей. Найти решение." So: **leave it for MVP 1; a task after MVP 1 finds the right numbering.**

The derived notes record the same ruling, by Pavel [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]. The release-version file idea of Oct 5 is related: [[wiki/decisions/2026-10-05-a-release-bakes-a-file-of-the-component-versions-it-contains-into-the-artifact.md]].

## Open commitments

- [ ] Unassigned (Pavel's "задача будет") — after MVP 1, find a shared Flex IQ version numbering across environments — due after MVP 1 — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
