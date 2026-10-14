---
type: decision
title: All web services go to production now, before the weekend, instead of waiting until Elizabeth starts bringing machines up in Georgia — Chudinov deploys the production web service over the weekend and tries a terminal against it
date: 2026-10-09
aliases: [roll out web services before the weekend, раскатить веб сервисы все, production web service over the weekend, продакшн вебсервис, dev stacks only, дэвенные стеки, it is time, пора, no bot task for this, пометка для бота не создавай]
source-count: 6
status: active
open-commitments: 5
open-questions: 0
---

# All web services go to production now, before the weekend

**Decided** at the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 Minsk stand-up]] (Russian, a Friday). Proposed by [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), agreed by [[wiki/people/pavel.md|Pavel Frolov]]. Restated the same morning on the [[wiki/meetings/2026-10-09-transactional-mvp1-test-machines-and-unclaimed-funds.md|8:01 AM Transactional MVP 1 call]].

## What was said

- **The trigger.** Pavel: "Нам надо пушнуть… скорее всего, сегодня Элизабет. Чтобы они ставили софт на флекс? Порт. Во флексайтю" — push [[wiki/people/elizabeth.md|Elizabeth]] today to install the software on Flexport and Flex IQ [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].
- **The proposal.** Chudinov: "с учётом Того, что выходные, может нам уже. Раскатить наоборот, веб сервисы все. Чтоб потом не ждать последнего момента, когда там Элизабет начнёт всё поднимать, а у нас пока всё развернуто на дэвенные стеки." Everything runs only on dev stacks today [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].
- **Agreed.** Pavel: "Да. Да да ты прав. Типа да пора." and "Да, хорошо, это важный момент." [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- **The weekend check.** Chudinov: "Я может тогда ещё за выходные подымем этот терминал наш… посмотрим, чтобы он там подключился. Можно даже [payout — reading]… проверим, чтобы работает." The notes read the garbled word as "maybe with a payout" [[raw/Meeting_Notes_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].
- **No bot task.** Chudinov: "Сразу сразу пометка для бота не создавай на этой задачи. А то он там уже создает." — a note to the AI PM agent not to create a task from this [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]. See [[wiki/projects/ai-project-manager-and-company-second-brain.md]].
- **The 8:01 AM restatement.** Chudinov to [[wiki/people/andrei-klimovich.md|Klimovich]]: "на выходных я планирую уже подготовить, развернуть продакшн вебсервис, и чтобы потом время на это не тратить, попробовать… Протовский… Смотри, какой он там взлетит, так что будем готовы по максимуму." [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]

## Why

Services deploy fast; Georgia's machine set-up is the slow part. Not waiting for the last moment avoids a scramble when Elizabeth brings machines up [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]. The first real transaction in production follows: [[wiki/decisions/2026-10-09-a-real-transaction-is-run-in-production-on-the-new-version-before-the-first-real-location.md]].

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — deploy the production web services and try the production environment — due the weekend of Oct 10–11 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — maybe bring up the team's terminal over the weekend and check it connects ("я может", tentative) — due Oct 10–11 2026 — [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Update, Oct 12 2026 — production prep with Andrei; location billing goes out as it is

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 Minsk stand-up]] (Russian) [[wiki/people/dmitri-chudinov.md|Chudinov]] reported [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]:

- **The weekend.** A mass deploy on STG "с Андреем" ([[wiki/people/andrey-bosik.md|Andrey Bosik]] by context — **inference**): pods fall over, and on a terminal the assets went inactive after a delete, with "сервер недоступен". He is fixing it and will roll a new update "через часик".
- **Production.** "готовимся с Андреем этот к проду. Сделали уже сертификат. Я сегодня собрал свежий продбил… на сегодня надо ещё сделать раскатку вебсервисов напрот" — certificate done, a fresh production build today, web services to production today.
- **Location billing.** "Не знаю только что делать с lom belling там нейтан всё закончил, не всё закончил" — [[wiki/people/nathan-carver.md|Nathan]] has not finished everything. Pavel: "Я думаю да… То, что есть" — roll out what exists. Chudinov: "на MV pay это никак не влияет, белинг там может жить своей жизнью" (it does not affect MVP 1, reading "MV pay" as MVP — **inference**).
- [[wiki/people/sergey-tsymanov.md|Tsymanov]] asked whether Nathan added the location-billing API "помните давным давно обсуждали", and whether JVL owes a button on its side. Pavel: "Надо посмотреть, что мы с ним до чего дошли". Not answered.

The derived notes record "Roll location billing to prod as it is now" as Pavel's decision [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].

### Open commitments (Oct 12 2026)

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — fix the STG pod and asset problem and roll a new update — due Oct 12 2026 — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — with Andrei, roll the web services and location billing (as it is) to production — due Oct 12 2026 — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [ ] Unassigned (Pavel, Tsymanov) — check what Nathan added for the location-billing API and whether JVL needs a button — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
