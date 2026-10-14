---
type: decision
title: A capability moves itself to Request Review when all its child features are Completed (Kovalchuk's weekend automations), and a story added under a Completed feature sends the feature to To Do and its capability from Request Review to To Do — Kovalchuk automates it, the developer moves it to In Progress when he takes the story; every story must hang under a parent
date: 2026-10-05
aliases: [Jira reopen rules, four automations, 4 автоматизации, capability to Request Review automatically, все дочерние фичи комплект капабилити реквест ревью, story reopens feature and capability, фичу из комплитов в туду, капабилити в туду, пускай будет всё в туду, open story hiding inside a done tree, внутри сидит открытая история, stories without a parent, ряд оказались ни к кому, today's date no longer red, убрал сегодняшнюю дату]
source-count: 8
status: active
open-commitments: 2
open-questions: 3
---

# A capability moves itself to Request Review when its features are Completed; a new story sends feature and capability back to To Do

Settled at the end of the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian) by [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]. It extends the Oct-1 ruling on [[wiki/decisions/2026-10-01-completed-is-the-developers-last-step-and-a-found-problem-sends-the-feature-from-completed-back-to-to-do-as-a-story.md]] (Completed is the developer's last step; a problem found during development is a story and the feature goes Completed → To Do) up one level, to the capability, and makes both moves automatic.

## Kovalchuk's weekend automations

"Я и [из отчёта] убрал сегодняшнюю дату, чтобы вас не мучило что? То задачи сегодня стекают" — the red highlight on today's date is gone from his report (his Oct-2 commitment on [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]]). "А на выходных ещё написал 4 автоматизации, которые должны. Немножко помогать с очередями, то есть **если все дочерние фичи в статусе. Комплект то [капабилити] должна будет автоматически перевестись [в] реквист ревью.** Вот так что если кого то что то не будет работать, пожалуйста, сообщайте, будем смотреть." Only this one of the four is described [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]].

## Chudinov's remark — the open story hiding inside a done tree

"если вдруг заводится историей, там доделать [—] там либо чтото. Надо вопервых её, к какомунибудь [паренту — parent] при[вязать]; у меня ряд оказались ни к кому. Ну я там уже [Клодом] разобрал по этим. По связям, к чему относилась? Это надо тогда продумать, чтобы ну с[т]ори создали а фича комплитут [капабилити] в реквестту ревью надо её хотя бы тогда либо кодом, либо автоматом перевозить в туду и тот и тот. Как минимум фичу я могу в туду сам перевести, а [капабилити] только в [In Progress] можно." Why: "я смотрю свой свой репорт у меня всех [капабилити в ревью]. Я понимаю, что всё закрыл, оказывается, гдето там внутри сидит открытая история. И как вот про это узнать? Надо [Клодом] каждый раз пробегается по всему дереву." Irina: "Это ктото не досмотрел. Говори кто?" Chudinov: "Не у нас фамилии не называются." Irina: "Не потому, чтобы наказать… просто чтобы обратить внимание, это неважно кто." Chudinov: "Я говорю всем, и чтобы все принимали во внимание." (Nobody was named; nothing further is recorded.) [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## The ruling

Kovalchuk: "получается, [story] в туду стоит, и ты хочешь, чтобы фичи переводилась из комплитов в [In Progress]." Irina: "Конечно." Chudinov: "и [капабилити] тоже потом." Irina: "Нет… [Фича] в туду." Chudinov: "А [что с капабилити]?" Irina: "[Capability] можно в туду можно в in прогресс." Chudinov: "Она уже реквисту ревью стоит я её уже перевёл." Irina: "**Хорошо, пускай будет всё в [туду] и сам переведёшь в [In Progress], когда возьмёшь эту сторию в работу.**" Kovalchuk: "Получается [фичу] из комплитов в [To Do] переводим." Chudinov: "Да и соответственно ее, [капабилити] в [туду]." Kovalchuk: "Из [Request Review] туда." Chudinov: "Да." Irina: "Угу." Pavel: "Окей." [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

In one line: **all child features Completed → the capability goes to Request Review by itself; a story created under a Completed feature → the feature goes Completed → To Do and the capability goes Request Review → To Do, both automatically; the developer who takes the story moves them to In Progress himself; and a story must always hang under a parent.** The derived notes record the same ruling, credit Irina and Chudinov, and give Kovalchuk the implementation [[raw/Meeting_Notes_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]].

## Where it sits

- **Evolution of Oct 1, not a contradiction.** Oct 1 ruled the feature's move (Completed → To Do, by a story); Oct 5 adds the capability's move (Request Review → To Do) and the automation of both. Chudinov's "фичу я могу в туду сам перевести" suggests the Oct-1 feature transition is already in the workflow — **inference**; Kovalchuk did not say so.
- **Request Review now has a use for capabilities.** On Oct 1 Kovalchuk said the status "был только для лениных"; the new automation parks a capability there once its features are done. Whether Request Review stays in the *feature* workflow is still the Oct-1 open question (annotated there).
- It rides on Kovalchuk's report and discipline cadence ([[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]], Oct-5 update) and on the capability-requires-requirement chain of [[wiki/decisions/2026-09-15-capability-requires-requirement-and-dates-sit-on-the-lowest-level.md]] (link is context, not a citation).

## Oct 6 2026 — the warning triangle stays, and so does the status flow

At the [[wiki/meetings/2026-10-06-daily-standup-ris-georgia-branch-and-critical-error-text.md|Oct-6 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]:

- **The triangle.** Kovalchuk: when all features are Completed but the capability is still blue (In Progress or Request Review), Jira shows a warning triangle, because Jira reads only colours (grey, blue, green). He asked whether Request Review should be grey. Pavel: grey is bad and green is bad; "пусть лучше показывает жёлтый треугольник. Мы, по крайней мере будем это открывать, смотреть, почему она в инпрогрессе не закрыта? Надо ли тесты какието, если не надо будем закрывать."
- **The flow.** Kovalchuk asked whether Proposed, Accepted and To Do are all needed. Irina: Accepted means features will now be created. Pavel: To Do means planning has started and rough dates are set. Kovalchuk: "Но все тогда оставляем как есть."
- **Due dates.** Kovalchuk: watch your due dates. For closed items with no due date, Pavel: "закрыто, наверное уже не стоит"; Kovalchuk: if the report keeps flagging them, better fill them.

## Open commitments

- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — automate the reopen: a story created under a Completed feature moves the feature Completed → To Do and its capability Request Review → To Do — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Open questions

- What the other three of Kovalchuk's four weekend automations do — only the capability → Request Review one was described — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

**§15.8:** clear — Jira process only. Who left open stories under closed features was asked and deliberately not named ("у нас фамилии не называются"); nothing is recorded. **§15 #9:** none.

## Update, Oct 12 2026 — the "In Progress" automation fires on any mention of a task key; "turn it off" is not confirmed

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]:

- **What happened.** [[wiki/people/sergey-tsymanov.md|Tsymanov]]: port task 118, assigned to him, moved itself to In Progress though "Я её не переводил". [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]]: "сейчас настроен автоматизация. Если создана ветка, создан фулриквест либо comit, то задача автоматически открывается." The commit was [[wiki/people/vladimir-samusenko.md|Vladimir]]'s; Pavel: "указал он тинт 30. Он никак с этим не связан" (TIN-30).
- **Why.** Vladimir: "жиро ищет ключи задач" anywhere — even if the commit belongs to another task and is in another branch, a key named in its text links it. "в комментарии к комиту нельзя указывать задачи, не относящиеся к… тому, куда ты комидишь."
- **Fixes proposed.** Pavel: only the first word of the commit message, up to the first space, should count. Irina: match the task's project to the repository (a port task only from the port repository). Kovalchuk: "там, к сожалению, нету таких гибких правил" and "Давайте отключим это правило тогда." No one confirmed; the stand-up moved on.

This automation is a new item beside Kovalchuk's Oct-5 rules above; the sources do not say whether it was one of his four weekend automations. The derived notes list it as an open question [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].

### Open questions (Oct 12 2026)

- Should the Jira automation that moves a task to In Progress on any branch, commit or pull-request mention be turned off, or narrowed? Kovalchuk proposed turning it off; not confirmed — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]

## Update, Oct 13 2026 — an issue type for release work that has no code branches; not settled

At the [[wiki/meetings/2026-10-13-daily-standup-video-decode-memory-and-release-task-type.md|Oct-13 Minsk stand-up]] (Russian) [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] raised a gap [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]:

- **The problem.** "у димы чудинова сейчас ситуация, когда он делает релизные фичи… но на эти фичи не будет веток никаких. На это отчет будет ругаться что? Нету веток." Release work such as a deploy ([[wiki/people/dmitri-chudinov.md|Chudinov]]) has no code branch, so the report flags it.
- **Kovalchuk's options:** "либо ввести какойто тип задач, либо сделать это task, но task тогда надо будет поднять выше в иерархии, чтобы он цеплялся [к] капбилити."
- **Pavel:** "мне нравится идея иметь отдельный там ищи" (issue) "который по своему будет обрабатываться".
- **Tsymanov** asked why not cut a release branch. Pavel: "у тебя камитов не будет"; Chudinov: "Мы пока не режем их."
- **Kovalchuk** added that such a type might also serve tasks the PM agent creates, but asked whether it would become clutter ("не будет ли… это мусора какого нибудь"). Pavel: "над этим подумать". Nothing was decided.

### Open commitments (Oct 13 2026)

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — think through an issue type for release work with no code branches — due unspecified — [[raw/Meeting_Notes_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]

### Open questions (Oct 13 2026)

- Which issue type should release work with no code branches use — a new type, or a Task raised in the hierarchy to link to a capability — and would PM-agent tasks of that type become clutter? — [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]] — *Oct 14 2026: Kovalchuk and "Дима" agree Tsymanov was right that a release branch is likely, cut and marked as such; not ruled* — [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]

## Update, Oct 14 2026 — a release branch is likely after all

At the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 Minsk stand-up]] (Russian), going through the AI digest, [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] read the release-branch item and said: "Мы обсудили с Димой, что Сергей был прав, наверно, если наверно будет какаято заводиться всётаки ветка под релиз но всё равно должна както отрезаться это всё и помечаться что это релизная ветка." The "Дима" is likely [[wiki/people/dmitri-chudinov.md|Chudinov]], who had said "Мы пока не режем их" on Oct 13 (**inference**); "Сергей" = [[wiki/people/sergey-tsymanov.md|Tsymanov]], who asked on Oct 13 why not cut a release branch [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

This leans toward Tsymanov's release branch, but no ruling was made and Pavel did not speak to it. The Oct-13 question below stays open.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
