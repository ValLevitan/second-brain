---
type: decision
title: Bosik owns the AI project manager; the live meeting bot waits for MVP 2; the transcripts are collected and the company second brain is built first; drafts go to repository code owners with no human "responsible"; dry run before any Jira write; status on Friday at 7, not in a week or two
date: 2026-09-29
aliases: [Bosik owns the AI PM, AI PM MVP 2 bot, meeting bot to MVP2, second brain first, collect the transcripts first, drafts to code owners, no responsible for the AI PM, AI draft status, dry run no Jira writes, Friday at 7 status, никаких бонусов, это не бонус, AI PM does the work not writes to us]
source-count: 3
status: active
open-commitments: 6
open-questions: 4
---

# Bosik owns the AI PM; the bot waits; the second brain comes first

Set on the [[wiki/meetings/2026-09-29-ai-pm-architecture-and-second-brain-plan.md|Sept 29 2026 "Design_AI-PM" call]] (Russian), chaired by [[wiki/people/val-levitan.md|Val Levitan]], with [[wiki/people/andrey-bosik.md|Andrey Bosik]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]. It carries out the [[wiki/decisions/2026-09-25-one-company-second-brain-feeds-an-ai-project-manager-for-jira.md|Sept-25 direction]]. The whole picture is on [[wiki/projects/ai-project-manager-and-company-second-brain.md]]; this page holds the rulings.

## 1. Bosik owns the project

Val: "давай кто кто за ответственный за этот проект." Bosik: "**Нет, видимо я наверное буду.**" Earlier he had said "Я могу взять на себя, попробовать это реализовать" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

## 2. The live meeting bot goes to MVP 2; what relieves work today comes first

Bosik found the bot the most interesting part — "самое интересное здесь это создать бота" — and did not yet know how to run one. Val: "**я бы это бы перенёс бы на 2 может быть [MVP], а пока имплементировал то, что сегодня может [облегчить] работу.**" His reasons: "**нам тяжело. Мы не хотим наращивать количество людей. Скорость мы хотим повысить. И у нас не хватает времени, чтобы администрировать все таски.**" So: "**давайте мы имплементируем сегодня то, что легко заработает**" — parts that start working within a couple of days, then one step added after another, so that "в течение, например, месяца у нас образуется чтото такое[,] [с]истемно работающая" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

## 3. Collect the transcripts into one store, then build the second brain — the longest step starts first

Bosik's first step: "автоматизировать процесс получения расшифровок из митингов". Val: "прежде всего надо построить секонд [брейн]"; the two then found they meant the same thing — the raw transcripts are gathered first, and the second brain is built from them. Val's sizing: gathering, moving to one store and making it "единственным хранилищем" is "**около дня. 2 дней, но это приблизительно**"; the resulting "200 500" transcripts take "**около месяца**" to process — "**самый длинный процесс во всем процессе. Этот процесс нужно запустить первым**", also the most voluminous and "самый дорогой". Everything else runs in parallel while it cooks; it is launched "только по фазам", and each phase is steered [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

Bosik's three stages — get the raw transcripts; convert them with the glossary; the second brain processes them — were reordered by Val: "**Нет, нет, [глоссарий] делается потом. Сначала нужно сделать секонд брейн**"; it will contain some wrong items and compile "большой список [терминов], который… [AI] не понимает", and that list is run through the glossary, which confirms the terms [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

## 4. Drafts go to the repositories' code owners; there is no human "responsible" for the AI PM

Kovalchuk's dilemma, "как определить ответственного". Val: "**Я бы не делал бы ответственного. Это… должна быть автономная роль, которая действительно работает в компании. Это… единственный полноценный про[джект] менеджер**." The point of it: "**Я не хочу чтобы AIPM нам писал, я хочу чтоб это был рабочий AIP[M], который с нас снимает работу. Его задача [создавать] таски проперные, без ошибок. И в лимитированном количестве. Согласно нашим стандартам.**" Bosik's mechanism: every repository maps to a Jira project, so "зная… коды оунеров каждого репозитория… эти задачи… либо [ассайнить], либо репортить" to the repository owners. Val: "Так точно Да да" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

Kovalchuk's worry — a code owner absent from the meeting gets a pile of tasks and must ask Pasha or Irina — was answered by Bosik ("коды [оунеры]… всегда есть на митинге… [э]то исключительная ситуация") and Pavel (rare; he sees the tasks anyway; links to the meeting notes should be in them). Pavel's own arithmetic settled the volume fear: 50 tasks a day across owners "будет там 8 задач на человека" — Val: "Это нормально" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

## 5. Drafts in Jira with an "AI draft" status, after a dry run with no Jira writes

Bosik: after a meeting the transcript takes about 10 minutes and the processing 10–15, "то есть через полчаса максимум… могли бы получать черновик [з]адач"; they appear in Jira with a status like "драфт" / "AI draft", assigned or reported per the scheme, and a person "может их либо сам корректировать, либо [о]тменить… либо принять целиком". Val: "я с вами полностью согласен" — his own slide said big actions need a human OK and everything is logged (the English on tape is garbled). Before any of that: "**какоето время, его погоняем без жиры драйверан… прежде чем пускать ему доступ. Писать в джиру**" — a week or two of dry run, after which they may even "уйдём от этой схемы" back to email. Nobody objected. Kovalchuk's answer to Pavel's "drafts get lost in the Jira tree": a dedicated task type or project that shows at the top of the plan [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

## 6. Friday at 7, not "in a week or two"

Bosik: "Через недельку, через 2 встречаемся." Val: "**Нет, нет, нет… у меня нету стоков времени, так это не работает.**" Bosik: at least a week, there are other tasks, "Это так бонус." Val: "**Вам это никакой не [бонус], это никаких бонусов здесь нету. Давайте в пятницу встретимся… В пятницу я назначу митинг гдето на 07:00.**" That Friday is Oct 2 2026 (worked out, not spoken) [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

## Update, Sept 29 2026 (10:31 AM) — a direction check with Pavel and Irina: no reservations

Four and a half hours later, at the end of the [[wiki/meetings/2026-09-29-dev-environments-rk3568-sdk-amd-spike-and-ai-pm-direction-check.md|"Dev_environments" call]], Val asked [[wiki/people/pavel.md|Pavel]] and [[wiki/people/irina-shishko.md|Irina]] whether they had "какието резерве" about the AI project manager "как мы сегодня говорили". Pavel: "Нет, я уверен, что мы идем правильно… что сейчас будет нереально, то оно через через полгода станет реально." Irina: "А теперь ещё кто кого ведёт?" Nothing here changes; the rulings above stand [[raw/Meeting_Transcript_Dev_Environments_AI_PM_Direction_Check-September-29-2026.md]].

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — finish the architecture design "чтобы он был внятным" — clear enough for the AI itself to know its direction — due Fri Oct 2 2026 (status meeting) — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — set up collection of the meeting transcripts "с каждого пользователя" into one store (no out-of-the-box mechanism exists; even an admin cannot read others' transcripts) — due about 1–2 days by Val's sizing; status Oct 2 2026 — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — start studying and building the company second brain from the collected transcripts, in phases — due started; about a month of processing by Val's sizing — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — while the second brain builds, prepare the AI PM's own architecture and character ("персона по сути надо сформировать"; Val: 2–3 days from his experience) — due unspecified — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — run the task-drafting as a dry run with no Jira writes for a week or two before giving it Jira access — due after the pipeline exists — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — book the status meeting for Friday Oct 2 2026 at about 7:00 — due Sept 29 2026 — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]

## Open questions

- **What period of transcripts.** Irina asked; Val: "с января 2026", then "может, с января, может быть, с июня… вам виднее"; Bosik will first see what period can be pulled — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- **Where the AI PM runs.** Pavel: it must live on some server and stay current. Bosik: decide later — a Jira hook firing a GitHub action, a cloud service, a bought subscription "за адекватных денег", or a PC in the office — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- **How to keep the AI's output short.** Val: "я имею такую тенденцию очень много публиковать… здесь надо быть осторожным"; he limits sentence count and bans complex or technical language, "но всё равно это много читать" — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- **Right after each meeting, or once a day.** Bosik raised it; Pavel: some tasks are urgent, others are still being discussed and tomorrow's continuation may change them. Val's preference — do it at once and ask for comments; the AI chases what is not commented ("самоизлечиваемая такая болезнь") — is stated, not ruled — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]

**§15.8:** Val's remarks about how Bosik presents himself are personal judgements and are not recorded. No pay or personal matters. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- [[raw/Meeting_Notes_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- [[raw/Meeting_Transcript_Dev_Environments_AI_PM_Direction_Check-September-29-2026.md]]
