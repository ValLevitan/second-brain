---
type: decision
title: Bosik owns the AI project manager; the live meeting bot waits for MVP 2; the transcripts are collected and the company second brain is built first; drafts go to repository code owners with no human "responsible"; dry run before any Jira write; status on Friday at 7, not in a week or two (held Oct 2 — 318 transcripts collected; next status Tuesday Oct 6 at 7)
date: 2026-09-29
aliases: [Bosik owns the AI PM, AI PM MVP 2 bot, meeting bot to MVP2, second brain first, collect the transcripts first, drafts to code owners, no responsible for the AI PM, AI draft status, dry run no Jira writes, Friday at 7 status, никаких бонусов, это не бонус, AI PM does the work not writes to us]
source-count: 7
status: active
open-commitments: 3
open-questions: 1
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

## Update, Oct 2 2026 (7:32 AM) — the Friday checkpoint held: designed, 318 transcripts collected, the "Listener", and the next status on Tuesday at 7

The status meeting of §6 took place as the [[wiki/meetings/2026-10-02-ai-pm-status-listener-core-and-318-transcripts.md|"Design_AI-PM - status" call]] (Russian; Val, Bosik, Pavel late, Irina and Kovalchuk at the end) [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]. Against the rulings above:

- **§1 — Bosik owns it, and reported.** "Спроектировал всю систему, так как она выглядит на данный момент… И перешли уже реализовывать."
- **§2 — the bot still waits**, but is being tried on the side: "попросил [Клода], и он пытается сделать вот этот голосового участника… пока сложно." No change of plan.
- **§3 — the transcripts are collected: 318, from July 2025.** "мы собрали 318 расшифровок, они собрались с июля 25, потому что есть ограничения по хранению." The second brain is not yet built from them — "пока забрал, но ещё не храню, но они будут обрабатываться и будут храниться в [GitHub]". The glossary pass was not mentioned. **New, Bosik's own ruling:** MVP 1 uses the Teams transcripts as they are; Whisper re-transcription with the glossary goes to MVP 2 — [[wiki/decisions/2026-10-02-ai-pm-mvp1-uses-the-teams-transcripts-as-they-are-and-whisper-re-transcription-waits-for-mvp2.md]].
- **§4–5 — the drafting core exists, the dry run has not started.** "Базовое ядро… листонер это тот, кто будет превращать то, что было сказано на митингах в черновики задачи в джие… читает в том числе и русские расшифровки." Nothing on Jira writes or a dry run yet.
- **§6 — Friday at 7 happened (7:32), and the next one is Tuesday at 7.** Val: "Опять встретимся во вторник… на 07:00"; Bosik, after Kovalchuk and Irina converted it: "во вторник на 14 ноль ноль по Минску на 07:00. По вашему времени" — Tuesday Oct 6 2026 (worked out). The derived notes read the same [[raw/Meeting_Notes_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]].

The full status is on [[wiki/projects/ai-project-manager-and-company-second-brain.md]] (Oct 2).

## Update, Oct 8 2026 (8:31 AM) — a test Jira project now, real projects from Monday Oct 12

At the [[wiki/meetings/2026-10-08-ai-pm-listener-scope-draft-lifetime-and-october-12-go-live.md|Oct-8 AI-PM review]], against the rulings above [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]:

- **§1 — Bosik still owns it** and presented the status; the second brain itself is now being built by [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] ("Дима начал работу над… секонд брейн").
- **§2 — the bot still waits.** Voice presence is MVP 2. Val pressed that the end goal is a real-time participant and doubts the present one-agent design will carry it; he agreed to launch and change the architecture later if needed.
- **§5 — drafts in Jira with the "AI Draft" status, as planned; the dry run became a test project.** Features are created in a test Jira project now; live mode in the real projects starts Monday Oct 12 2026. A person moves each item to To Do or rejects it; untouched items are deleted after a window still being argued. The new rulings are on [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]].
- **§6 — the Tuesday checkpoint.** Bosik refers to changes agreed at "прошлом митинге"; the notes name it as an Oct 6 meeting [[raw/Meeting_Notes_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]. That meeting's own file is not in the wiki.

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — start studying and building the company second brain from the collected transcripts, in phases — due started; about a month of processing by Val's sizing — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]] — *Oct 2 2026: the 318 transcripts are pulled "но ещё не храню"; they will be processed and stored in GitHub; the brain itself is not reported built* — [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]] — *Oct 8 2026: the work has passed to Kovalchuk — "Дима начал работу над 2 мозгом над секонд брейн"; not finished* — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — while the second brain builds, prepare the AI PM's own architecture and character ("персона по сути надо сформировать"; Val: 2–3 days from his experience) — due unspecified — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]] — *Oct 2 2026: in progress — "личность то, что вы прислали… дописал немножко. Собрал ему знания немножко"* — [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]] — *Oct 8 2026: a Teams agent with a Microsoft account, a generated face and Val's books in its prompt is running, but gave no useful answer in its first test; Val wants it named* — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — run the task-drafting as a dry run with no Jira writes for a week or two before giving it Jira access — due after the pipeline exists — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]] — *Oct 2 2026: not mentioned; the "Listener" core exists but no drafting run is reported* — [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]] — *Oct 8 2026: instead of a run with no Jira writes, drafts are written to a test Jira project; real projects from Oct 12 (whether this counts as the dry run is for the owner)* — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]

## Open questions

- **How to keep the AI's output short.** Val: "я имею такую тенденцию очень много публиковать… здесь надо быть осторожным"; he limits sentence count and bans complex or technical language, "но всё равно это много читать" — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]

## History

- [x] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — the next status report on the AI PM — due Tuesday Oct 6 2026, 7:00 AM Eastern / 14:00 Minsk — [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]] — **discharged:** a review took place before Oct 8 (Bosik: the changes agreed "на прошлом митинге" are implemented); the Oct-8 notes name it as Oct 6 — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]] [[raw/Meeting_Notes_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- **Answered — where the AI PM runs.** Pavel: it must live on some server and stay current. Bosik: decide later — a Jira hook firing a GitHub action, a cloud service, a bought subscription "за адекватных денег", or a PC in the office — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]] **Answered Oct 8 2026:** the pipeline runs as GitHub Actions scripts ("это ничего не стоит нам"), the Teams part in a container; the AI calls run through Bosik's own account for now and are to move to the Anthropic API — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- **Answered — right after each meeting, or once a day.** Bosik raised it; Pavel: some tasks are urgent, others are still being discussed and tomorrow's continuation may change them. Val's preference — do it at once and ask for comments; the AI chases what is not commented ("самоизлечиваемая такая болезнь") — is stated, not ruled — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]] **Answered Oct 8 2026 in practice:** a script checks every 15 minutes for new recordings, so drafts follow each meeting closely (Bosik: "пока мы час разговариваем там как раз идёт процесс создания этих задач") — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [x] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — finish the architecture design "чтобы он был внятным" — due Fri Oct 2 2026 — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]] — **discharged Oct 2 2026:** "Спроектировал всю систему, так как она выглядит на данный момент… И перешли уже реализовывать" — [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]
- [x] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — set up collection of the meeting transcripts "с каждого пользователя" into one store — due about 1–2 days; status Oct 2 2026 — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]] — **discharged Oct 2 2026:** "мы собрали 318 расшифровок, они собрались с июля 25" (how the per-user access problem was solved is not said) — [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]
- [x] [[wiki/people/val-levitan.md|Val Levitan]] — book the status meeting for Friday Oct 2 2026 at about 7:00 — due Sept 29 2026 — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]] — **discharged:** the "Design_AI-PM - status" call took place Friday Oct 2 2026, 7:32–7:37 AM Eastern — [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]
- **Answered — what period of transcripts.** Irina asked on Sept 29; Val: "с января 2026", then "может, с января, может быть, с июня… вам виднее"; Bosik was to see what could be pulled — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]. **Oct 2 2026:** from July 2025, bounded by Microsoft's retention — "они собрались с июля 25, потому что есть ограничения по хранению" — [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]

**§15.8:** Val's remarks about how Bosik presents himself are personal judgements and are not recorded. No pay or personal matters. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- [[raw/Meeting_Notes_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- [[raw/Meeting_Transcript_Dev_Environments_AI_PM_Direction_Check-September-29-2026.md]]
- [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]
- [[raw/Meeting_Notes_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]
- [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [[raw/Meeting_Notes_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
