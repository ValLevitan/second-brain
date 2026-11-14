---
type: decision
title: A task moved to To Do must carry a due date, set by whoever moves it (not necessarily the doer) — the rule goes into the Jira standard so every developer's Claude sets it; the creator does not put a new task straight into To Do; Jira gets no hard block on an empty date (a next-day notice instead); due dates are needed at least at feature level, and small features need not be split into stories
date: 2026-11-09
aliases: [due date rule in the standard, due date when moving to To Do, давайте это просто впишем стандарт, Claude sets the due date, no hard block on empty due date, запрет перевода в статус ту ду, creator does not put a task straight into To Do, создающий не должен эту задачу сразу в туду, whoever moves it to To Do sets the date, due date at feature level, хотя бы на уровне фич, 30 tasks without a due date, Friday report missed 30 tasks]
source-count: 6
status: active
open-commitments: 2
open-questions: 0
---

# A task moved to To Do gets a due date from whoever moves it; the rule goes into the standard; no hard block in Jira (Nov 9 2026)

**Where and who.** End of the [[wiki/meetings/2026-11-09-daily-standup-due-date-rule-in-standard-and-update-dependency-map.md|Nov-9 Minsk stand-up]] (Russian), raised by [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] and ruled by [[wiki/people/pavel.md|Pavel Frolov]], with [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].

## What started it

- Kovalchuk said he was wrong to be pleased with Friday's report: "порядка 30 задач" had dropped out of it — "Их почемуто отчёт не смог… пересмотреть, так что завтра ждите по ним, Сообщение" [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].
- He offered a hard block: "могу сделать этот запрет перевода в статус ду в инпрогресс и прочее, если не заполнена" — the field "как будто становится обязательным" [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].
- Chudinov proposed a default instead: "какойнибудь дефолт типа на на неделю, а потом уже исполняющий подправит" [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].

## The objections

- **Kharetski** rarely uses To Do: his Claude takes a task from the backlog and "сразу в эн прогресс ставить", and "чаще всего задача закрывается. Ну за день" — so at today's speed the due date "не имеет смысла вообще", "в 98 процентах это вообще не надо, как по мне"; his field work ("с полей джелай эклипс бак в поле" — GLI, Eclipse, field bugs) cannot be planned; and he has a daily job after the PM report that "автоматическая джоба просто проставляет doy dat попозже" [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]. Irina: a task cannot go to In Progress without To Do, so it is really two steps; Kharetski agreed [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].
- **Chudinov** sets a due date only when he takes the task into work; tasks others create for him cannot be dated before priorities are set [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].
- **Kovalchuk** on Kharetski: "Но я наверное же не соглашусь. То есть если это не речь про какойто прям сильное планирование, то наверно да", and later "женя женя правильно говорит" — his position is **unclear** (the notes read it as disagreement for real planning). On notices: judging by the last month, everyone has long stopped paying attention to them [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].

## Why Pavel wants dates

"Есть месяц, мы хотим сделать релиз через месяц набора каких то продуктов… Если мы заранее оценим… и выставим каждому дьюдэй… будет видно, какой список задач мы можем за этот месяц сделать." Asked who plans: before it was mainly Pavel and Irina; now it is spread out — "и ты этим занимаешься, и дима этим занимается, и Саша этим занимается" [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].

## The ruling

1. **No hard block.** Pavel: "обязательно мне мне подход не нравится" — he would let the move happen and send "натификация на следующий день" [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].
2. **Dates at least at feature level.** "Давайте хотя бы на уровне фич. Дью дэйта ставим." For something done within a day the date loses its point. Features need not be split into stories "если они достаточно… Небольшие" [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].
3. **A step on the move to To Do.** "как только ты его переводишь в туду… хотя бы deudate автоматически проставлять на следующий день" [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].
4. **Into the standard.** Kharetski's Claude was trained on the standard of two weeks before (Kovalchuk: "Он после этого не менялся"); it enforces "нельзя без задач работать" and branch naming but sets no due date. Pavel: "Давайте это просто впишем стандарт. Я думаю, она закрывает проблему у у всех клоды начнут по стандарту работать и выставлять duday." Kovalchuk: "давайте я изменю стандарт сегодня добавлю эту точку… Надо всем направить." Kharetski: it only works for those whose Claude points at the standard [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].
5. **The creator does not put a task straight into To Do.** Chudinov: "надо с пометкой, что создающий не должен эту задачу сразу в туду вставить"; Pavel: "Да да Да да." Pavel's example: tasks taken over from [[wiki/people/eugine-yavorski.md|Yavorski]], created four months ago and left in To Do "когда у тебя возникнет время", with no due date [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].
6. **Whoever moves it sets the date.** Irina: is it only the doer who moves to To Do? Pavel: "Нет, не обязательно." Irina: "если… я перевожу в ту до, то я должна поставить время"; Pavel: "Да" [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].

## How it sits against earlier rulings

- It narrows the Oct-7 practice on [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]] that anything created for MVP 1 went straight to To Do even with no date (Nov-9 update there).
- It continues Kovalchuk's date drive: [[wiki/people/dmitri-kovalchuk.md]] (Nov 3 and Nov 6 sections).
- It relies on Claude reading the standards first: [[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]]; branch naming is [[wiki/decisions/2026-10-26-claude-made-branches-carry-a-jira-key-and-are-deleted-when-the-task-closes-and-claude-is-never-a-commit-co-author.md]].

## Open commitments

- [x] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — change the standard that day (due date required on the move to To Do; the creator does not move to To Do) and send it to everyone — due Nov 9 2026 — [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] — *done Nov 10 2026: "я разослал новую версию стандарта стандарт в статусе черновик, так что любые комментарии… приветствуются"* — [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]
- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — send the message on the ~30 tasks the Friday report missed — due Nov 10 2026 — [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]

## Note, Nov 10 2026 — the new standard sent as a draft; Kharetski loads it into Claude

At the [[wiki/meetings/2026-11-10-daily-standup-flex-iq-single-screen-install-failure-and-mvp2-release-november-20.md|Nov-10 stand-up]] Kovalchuk sent the new version of the standard "в статусе черновик", comments welcome, "и смотрите сроки"; Kharetski: "Сейчас я подключу этот. Кладу вот то, что дима скинул новые новые эти. Стандарты" [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]. Whether the draft contains exactly this rule is not said in the sources.

## Note, Nov 12 2026 — Kovalchuk's Gantt: almost nothing overdue or open more than 14 days, but many tasks have no date; the Jira agent has no right to set a date; Samusenko builds a plugin that loads the standard into Claude

At the [[wiki/meetings/2026-11-12-daily-standup-recycler-rust-service-and-no-features-before-capability-review.md|Nov-12 stand-up]] [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] showed the Gantt chart ("грант", heard): "Целом неплохая картина. Просроченных задач практически нету. Те, которые открыты больше 14 дней, тоже практически нету"; some open features have closed parents and must be checked; "очень много сдач, которые у которых нету сроков… Нужно поставить" [[raw/Meeting_Transcript_Daily_Standup_Recycler_Rust_Service_and_No_Features_Before_Capability_Review-November-12-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Recycler_Rust_Service_and_No_Features_Before_Capability_Review-November-12-2026.md]]. [[wiki/people/vladimir-samusenko.md|Samusenko]] is building "Плагином, который будет подключать стандарт… и клод будет ориентироваться на. То, что в стандарте при работе" (Kovalchuk) [[raw/Meeting_Transcript_Daily_Standup_Recycler_Rust_Service_and_No_Features_Before_Capability_Review-November-12-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Recycler_Rust_Service_and_No_Features_Before_Capability_Review-November-12-2026.md]]. [[wiki/people/alexei-khamin.md|Khamin]] asked whether the agent adds a date; Kovalchuk: "он не может, у неё нет разрешения на установку даты"; Khamin: "он просто не предупреждает, поэтому она улетает. Я даже не знал" [[raw/Meeting_Transcript_Daily_Standup_Recycler_Rust_Service_and_No_Features_Before_Capability_Review-November-12-2026.md]]. Which agent ("Этот IPM", heard) is **unclear**. Who sets the missing dates was not named [[raw/Meeting_Notes_Daily_Standup_Recycler_Rust_Service_and_No_Features_Before_Capability_Review-November-12-2026.md]].

### Open commitments (Nov 12 2026)

- [ ] Unassigned (Kovalchuk's Gantt finding; no owner named) — set due dates on the tasks that have none, and check the open features whose parents are closed — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Recycler_Rust_Service_and_No_Features_Before_Capability_Review-November-12-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Recycler_Rust_Service_and_No_Features_Before_Capability_Review-November-12-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Recycler_Rust_Service_and_No_Features_Before_Capability_Review-November-12-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Recycler_Rust_Service_and_No_Features_Before_Capability_Review-November-12-2026.md]]
