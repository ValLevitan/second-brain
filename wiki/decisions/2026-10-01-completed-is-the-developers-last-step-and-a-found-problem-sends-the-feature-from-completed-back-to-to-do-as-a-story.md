---
type: decision
title: "Completed" is the developer's last step on a feature; a problem found while development is still going sends the feature from Completed back to To Do (not In Progress) with a Story, not a Bug — and every feature links to the requirements it covers
date: 2026-10-01
aliases: [Completed to To Do, из комплект в туду, Completed is the developer's final step, финальной степ для разработчика, story not bug, пока ты разрабатываешь нет бага, Request Review was for Lena's team, реквест ревью был только для лениных, FP-85 story under a closed feature, feature linked to requirements, autotests are written on requirements, мы пишем на требования, Kovalchuk adds the transition, Хорошо я добавлю, reopen a Completed feature]
source-count: 7
status: active
open-commitments: 2
open-questions: 1
---

# "Completed" is the developer's last step, and a found problem sends the feature back to To Do as a story

Settled at the end of the [[wiki/meetings/2026-10-01-daily-standup-sas-mode-flag-and-feature-status-rules.md|Oct-1 Minsk stand-up]] (Russian) by [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]], with [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] taking the Jira change [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].

## The case that started it

[[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] got one of Kovalchuk's discipline emails: "у меня паром то уже закрыты, а эти нереализованные" — his parent item is closed with unrealised children. Under "фпорт 85" (read as FP-85 — the derived notes' reading) "Владимир создал… story", created "после Того, как я закрыл вот эту задачу, если посмотреть время" — [[wiki/people/vladimir-samusenko.md|Vladimir]]'s story landed under a feature Tsymanov had already closed. Irina: "в процессе… нужно было переоткрыть себе фичу, чтоб ты её доработал. Потому что когда Владимир писал, нашлось что[-то]" — writing the autotest found something [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].

## The argument

- **Which status a developer ends on.** [[wiki/people/dmitri-chudinov.md|Chudinov]]: "Мы говорили, что разработчик делает комплект, но не делает клоуз"; "мы 2 митинга назад обсуждали"; "У нас сейчас все фичи висят в комплиты"; "всё было в голос, сказали клоус. Нельзя надо комплитат я все… перевёл в комплитор. Сейчас уже оказывается реквест". Irina: it "не могла быть комплектов, потому что она не проверена… она должна была висеть в реквест ревью". Kovalchuk: "Реквист ревью вроде только для ковапелити обсуждали" [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].
- **Pavel's first answer — Request Review until the autotest passes.** "у нас есть статус реквест. Помоему он как раз очень хорошо… комплекта станет только после Того, когда отработает автотест. Ну автотест готов, и он проходит." Kovalchuk: "То есть [из] прогресса, потом переводится в [реквест ревью]" [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].
- **Can QA check a feature at all?** Chudinov: "кюя вообще не проверяют фичики проверяют, капубилити"; "Вы не можете проверить фичу?… потому что нету интерфейсов"; "сделаю фичу на вест кластере, ну ты туда даже не подлезешь". Pavel: "Авто теста пишется под фичию". [[wiki/people/evgeny-kharetski.md|Kharetski]]: "почему прозвучало, что мы пишем автотесты на фичи? Может быть, на [требования] должны были писать." Irina: "**Мы пишем не на фичи, мы пишем на требования. Которая находится в [capability]**… фича, либо реализует правильно это требование, либо там есть проблема. Если есть проблема, значит фичу нужно доработать." One feature can cover a piece or all of a capability's requirements, "но фичи… не должна создаваться на чтото просто пустое, чего нет в требованиях" [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].
- **Story, not bug.** Chudinov: "Разработчик перевёл свою фитча [в Request Review], её откуда там появится истории ни с Того ни с сего." Irina: "А как на это самое написать то что у тебя проблема? Куда бак мы не можем писать? Стори, потому что чтото недоделано, то есть тебе не говорят что ты сделал бак. Ты в рамках этой фичи чтото не доработал." Chudinov: "Тогда надо переоткрывать." Irina: "Его нужно переоткрыть… то, что фича оказалось не переоткрыто это было неправильно." Later, to Tsymanov's "что описывать, если проблема в виде стори?": "**Пока ты разрабатываешь нет бага ты просто чтото не доработал. Поэтому стори**" [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].
- **Pavel's rule.** "правило, у нас там есть такое, что да, мы не можем переоткрывать клост [фичи] но если комплитэт процесс разработки ещё идёт, мы ничего не зарелизили. Ну да, почему не вернуть её в работу с новой [стори]. Вроде как логично" [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].
- **Request Review's origin.** Irina, to Kovalchuk: the flow shows In Progress, Completed, Request Review — "Я бы либо комплект, либо реклавью… непонятно зачем". Kovalchuk: "**Вообще этот рекластью был только для лениных**… для лены создавался у них там есть такая штука, когда Майкл проверял. То, что нарисовали и переводил дальше, то есть у нас для разработчиков такое не использовалось" — a status made for [[wiki/people/lena.md|Lena]]'s team, where Michael (read as [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] — inference) checked the drawings [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]].

## The ruling

Pavel: "**Хорошо, тогда давайте так и сделаем. Ну пусть будут комплиты тогда всётаки типа финальной степ для разработчика, но если там чтото находится.**" Kovalchuk: "он закончил свою работу, да он перевёл в комплект". Irina: "**Только из комплект в туду.**" Kovalchuk: "**Хорошо, я добавлю.**" Irina's reason for To Do and not In Progress: "сейчас в инпрогресс, но это не инпрогресс, мы не знаем. Сегодня возьмёт разработчик прямо сейчас или через [14:00 — garbled] возьмёт работу эту фичу обратно." Kovalchuk: "Давайте и Добавим." [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]

In one line: **To Do → In Progress → Completed (the developer's last step). A problem found while development is still going → a Story under the feature, and the feature goes Completed → To Do.** Nothing is reopened from Closed.

**Finding the feature.** Chudinov: "как вы будете решать, под какой фичей проблема?… под [capability] может быть там… 10 фич." Irina's answer closed the stand-up: "**когда создаётся фича, она должна создаваться на какие то требования и при линковываться. И если не прошёл акцептонс критерий по данному требованию, то достаточно легко найти по какой фичи… была проблема.**" Pavel: "Ага. Да." [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]

## Where it sits

- It applies the Aug-4 principle on [[wiki/decisions/2026-08-04-bug-only-against-closed-feature.md]] — a bug exists only against a closed, released feature; what is found during development is scope, not a bug — to the Jira transitions.
- It answers the Sept-24 question on [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]] ("does a developer set Completed or Closed?"): **Completed**. Who checks before Closed is still not ruled on.
- It is the "problem found in the field" counterpart of [[wiki/decisions/2026-08-11-capability-amendment-post-release-bug.md]], which Kovalchuk named during the argument: "[Capability Amendment] это если бак какой то был найден в полях… а [capability] типа уже закрыт".
- Feature-to-requirement linking restates [[wiki/decisions/2026-09-15-capability-requires-requirement-and-dates-sit-on-the-lowest-level.md]] at feature level (link is context, not a citation).
- The discipline email that started it is Kovalchuk's daily report — [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Oct-1 update).
- The derived notes record the same ruling and the same attribution (Pavel and Irina; Kovalchuk to configure) and add that problems during development are Stories, not Bugs [[raw/Meeting_Notes_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]. They omit Pavel's first position (Request Review until the autotest passes).

## Update, Oct 2 2026 — the reopened feature shows as overdue, and "whoever takes a feature into work updates its schedule with Pavel or Irina"

At the next morning's [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 stand-up]] (Russian) the rule met its first side effect [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]. [[wiki/people/pavel.md|Pavel]] to [[wiki/people/sergey-tsymanov.md|Tsymanov]]: "Просьба посмотреть на вот эти вот красные таски, которые просроченные… Вот с 15 сентября 29 сентября 1 октября." Tsymanov: "это не просроченное это закрыть надо. Я просто брал вчера задачу. На неё Владимир создал [story]. Вот и я их фиксел. Получается мне переоткрыли эту фичу. И [фичу] но но дату не поменяли." Pavel: "Давай поменяем." [[wiki/people/vladimir-samusenko.md|Vladimir]]: "я их не назначал на исполнителя, ты их сам себе забрал" — "Да." [[wiki/people/irina-shishko.md|Irina]]'s rule: "**Никто из [QA] не может тебе назначить дату. Поэтому, если какуюто фичу берёшь в работу, получается, её нужно обновлять расписание. Либо. К паше подойти либо ко мне.**" Pavel: "Угу." The derived notes record it as a decision by Irina [[raw/Meeting_Notes_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]].

So the Oct-1 flow gains a step: **a feature that comes back from Completed to To Do with a story gets its dates refreshed by the developer who takes it, through Pavel or Irina** — otherwise it shows red in Kovalchuk's report. Kovalchuk's transition change below was not mentioned.

## Update, Oct 5 2026 — the rule climbs to the capability and becomes automatic

At the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian) [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] reported four weekend automations — "если все дочерние фичи в статусе. Комплект то [капабилити] должна будет автоматически перевестись [в] реквист ревью" — and [[wiki/people/dmitri-chudinov.md|Chudinov]] asked for the mirror of this rule one level up: a story created under a Completed feature should send "в туду и тот и тот" — the feature and its capability. Irina: "пускай будет всё в [туду] и сам переведёшь в [In Progress], когда возьмёшь эту сторию в работу"; Kovalchuk: "[фичу] из комплитов в [To Do] переводим… Из [Request Review] туда" [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]. Ruling and quotes: [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]]. The Oct-1 feature rule stands unchanged inside it (**evolution**, not contradiction). Chudinov's "Как минимум фичу я могу в туду сам перевести" suggests the Oct-1 transition is already in the workflow — **inference**; nobody said so.

## Update, Oct 7 2026 — Claude was opening bugs during development; Pavel: those are stories

At the [[wiki/meetings/2026-10-07-daily-standup-test-coverage-first-and-ai-task-numbers.md|Oct-7 Minsk stand-up]] (Russian) Pavel asked [[wiki/people/alexander-biratka.md|Biratka]] why he has "уже вообще 14 задач им прогресс". Biratka: while he builds a feature, "находится там какойто бак… клод говорит… бак заводит", so one feature collects several bugs, and they close when the feature closes. Pavel: "нет смысла это заводить как баги, потому что сейчас баги это будет что то, пришедшее из извне. Пока идет разработка это просто… какая то стория. Подработки." Biratka: "По типу таска тогда буду говорить, чтоб истории заводились" — he will tell Claude to open stories [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]. The derived notes record it as Pavel's decision [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]. This restates the Oct-1 rule (and the Aug-4 principle) for problems Claude itself finds — **no change to the rule**.

## Open commitments

- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — add the Completed → To Do transition to the feature workflow in Jira — due unspecified ("Хорошо, я добавлю") — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]] — *Oct 2 2026: not mentioned* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]] — *Oct 5 2026: Chudinov can already move a feature to To Do himself (so the transition seems in place — inference); the automated version, with the capability, is his new commitment on the Oct-5 decision page* — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [ ] [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] — update the dates on the feature reopened by Vladimir's stories (Pavel: "Давай поменяем") — due Oct 2 2026 — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]

## Open questions

- **Does Request Review stay in the feature workflow at all?** Irina wanted either Completed or Request Review, not both; Pavel first wanted Request Review to hold a feature until its autotest passes; Kovalchuk said the status was made for Lena's team and never used for developers. The ruling made Completed the last step and left Request Review where it is — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]] — *Oct 5 2026: Request Review now has a use for **capabilities** (all child features Completed → the capability goes there by itself); the feature-level question is still open* — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

**§15.8:** clear — Jira process only. Irina's "почему ты решил, что твой клод… наш клод глупее" is banter, not recorded. **§15 #9:** none; FP-85 is a work reference.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
