---
type: decision
title: A capability moves itself to Request Review when all its child features are Completed (Kovalchuk's weekend automations), and a story added under a Completed feature sends the feature to To Do and its capability from Request Review to To Do — Kovalchuk automates it, the developer moves it to In Progress when he takes the story; every story must hang under a parent
date: 2026-10-05
aliases: [Jira reopen rules, four automations, 4 автоматизации, capability to Request Review automatically, все дочерние фичи комплект капабилити реквест ревью, story reopens feature and capability, фичу из комплитов в туду, капабилити в туду, пускай будет всё в туду, open story hiding inside a done tree, внутри сидит открытая история, stories without a parent, ряд оказались ни к кому, today's date no longer red, убрал сегодняшнюю дату]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
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

## Open commitments

- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — automate the reopen: a story created under a Completed feature moves the feature Completed → To Do and its capability Request Review → To Do — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Open questions

- What the other three of Kovalchuk's four weekend automations do — only the capability → Request Review one was described — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

**§15.8:** clear — Jira process only. Who left open stories under closed features was asked and deliberately not named ("у нас фамилии не называются"); nothing is recorded. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
