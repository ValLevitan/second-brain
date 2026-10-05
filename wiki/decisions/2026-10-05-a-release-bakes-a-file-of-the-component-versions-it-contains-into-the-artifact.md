---
type: decision
title: A release bakes a file listing the component versions it contains into the release artifact, so it can be traced later — the integration repository's manifest need not pin release versions (artists and autotests need snapshots), and Kharetski plans a GitHub Page with a "release" tick to pick versions
date: 2026-10-05
aliases: [release bakes component versions, релиз должен в файле запекать какие версии были включены, versions file in the release artifact, в виде отдельного файла класть в артефакт, integration repository manifest, манифест версии компонентов, GitHub Page release tick, Китха Пейдж галочка релиз, snapshots for artists and autotests, не обязательно на релизных версиях, traceability of releases, CC Talk integration, another separate service]
source-count: 2
status: active
open-commitments: 1
open-questions: 2
---

# A release bakes a file of the component versions it contains into the artifact

Agreed between [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] and [[wiki/people/pavel.md|Pavel Frolov]] at the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian), in Kharetski's status round [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]. It is the first concrete shape of the machine-side NOVA integration repository decided on [[wiki/decisions/2026-09-03-module-contracts-and-nova-integration-repository.md]].

## Kharetski's status

"Я сейчас [CC Talk] заинтегрирую и одновременно на [тэтоцентр — unclear] в GT, который [трейдский — unclear]. Там прозы всякие контракты, вот это вот всё… закрыл там. Интеграции прошлые там [лет — LEDs, reading], [аккаунты борт — unclear] но по [IO] борду там чутьчуть… Короче, отдельный сервис сделали ещё один. Его тоже надо. Сделать… занимаюсь сейчас. Вот же 12, 37 на очереди 12 3 24 чтото там ещё добавится новый. Новых [фич]." The task numbers are as spoken; the derived notes read them as "LGS-12-37 now, 12-3-24 next" and the new service as "a new separate IO board service" — readings only [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]].

## Pavel's picture of the integration repository

"там в интеграционном репозиторе. Правильно ли я понимаю это будет какойто манифест, который указывает. Версии компонентов ну сами компоненты версии их. И там репозитории, откуда они берутся и оттуда будут на этапе сборки забираться релизные версии, скачиваться и запекаться в [имидж] какойто да." [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Kharetski's correction — not only release versions, and a page to pick them

"Не обязательно, что ты укажешь для сборки то и будет. Ну я рассчитываю пока что… До этого ещё, конечно, далековато, но я рассчитываю сделать. [GitHub Page], в котором… ты можешь выбирать? Типа, если ты хочешь [релиз], например, да, то ты там выбираешь условно галочку релиз, да и у себя доступна только версии, которая. Ну. Без [снапшотов], так скажем… в целом… твой посыл правильный, но сборки, то есть они не обязательно будут на релизных версии, может быть. Допустим, художникам нужно там, ну им же не нужны релизы им нужны там [—], где разрабатываются или для автотестов также нужны [снапшоты]. Вот для тестов и то и то надо." Pavel: "если это делается в рамках [экшена], то это сложно сделать. Да, если сделать [Page], то там можно всё, что угодно навернуть." [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## The ruling

Kharetski: "**главное, что релиз должен в какомто файле. Типа. Запекать. Какие версии? Были. Включены в этот релиз. Чтоб потом это можно было отслеживать всё.**" Pavel: "Ну в виде отдельного файла класть в артефакт, да?" Kharetski: "О да чтоб он к релизу был [приатачен] именно твой, то есть ты вот [в релиз] заходишь и у тебя там сразу есть вот. И сборка вся и. И [файлик — unclear]." Pavel: "Хорошо, да все правильно. Всё правильно сходится наше представление." [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

In one line: **every release carries, as a separate file inside its artifact, the list of component versions that went into it; the integration repository's manifest may point at snapshots as well as releases, because artists and autotests need development builds; a GitHub Page with a "release" tick is Kharetski's planned way to choose.** The derived notes record the same decision and the same two names [[raw/Meeting_Notes_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]].

## Where it sits

- It fills in the machine-side integration repository of Sept 3 ([[wiki/decisions/2026-09-03-module-contracts-and-nova-integration-repository.md]], Oct-5 update): module links as technical files, now with versions and sources, and a baked version list per release.
- It is the NOVA counterpart of the release-artifact and manifest ideas on [[wiki/topics/github-release-management-pipeline.md]] (Oct 5) and of the May-27 "manifest registry" where each piece of machine software publishes what it is ([[wiki/topics/nova-platform-architecture.md]], May 27 2026) — links are context, not citations.

## Open commitments

- [ ] [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] — make the release bake a file of the included component versions into the artifact; later, the GitHub Page with release / snapshot selection ("До этого ещё… далековато") — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Open questions

- Which repository "GT" is, and what "тэтоцентр… трейдский" means — the integration repository Kharetski writes prose and contracts for is named only by these garbles — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- What the new "отдельный сервис" is — the notes read "IO board service"; the transcript has "[аккаунты борт]… по [IO] борду" — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

**§15.8:** clear — build tooling only. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
