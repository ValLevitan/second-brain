---
type: decision
title: "Accepted" on a capability means reviewed and accepted, not taken into work — taken into work is the move to To Do when the release scope is set, and the transition will be automated from feature status
date: 2026-09-11
aliases: [the green status in the middle misleads, accepted is not taken into work, move to To Do when we say we are doing MVP 1, automate capability status from feature status, a feature going In Progress moves its capability, move all MVP 1 capabilities into To Do]
source-count: 3
status: active
open-commitments: 3
open-questions: 1
---

# "Accepted" means reviewed — taken into work is the move to To Do

Settled at the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept 11 2026 8:04 AM call]]. [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] was called into the meeting for this item alone — [[wiki/people/val-levitan.md|Val]]: "давайте позовём диму Ковальчука, чтобы он поправил [воркфлоу]" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## The complaint

[[wiki/people/pavel.md|Pavel Frolov]]: "у нас есть воркфлоу по cap[ab]ili[t]y[,] и вот этот вот в серединке зелёненький[,] он очень сильно сбивает. Кажется, что уже работа сделана, а на самом деле работа только начинается" — the green status in the middle of the capability workflow reads as work done when the work is only starting [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## The fix: the meaning, not the status

Kovalchuk's first instinct was to delete it — "я понял[,] его вообще убрать[,] да[,] получается[?]" — and Val said no: "[н]ет… [е]сли у нас есть про[по]с[ед], тогда у нас должен быть [ак]цепт" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

**Val then defined both ends of the boundary:**

> "[Т]ипа [кейпа]били[ти] когда предложили[ —] Павел его рассмотрел[,] с кем[-]то обсудил и сделал [ак]цепт. Но это не значит, что мы взяли его в работу."
> "[М]ы его взяли в работу, когда мы сказали[:] хорошо, сейчас мы делаем M[VP] один[;] вот эти кей[па]билитис мы берём в работу и поставили их в туду." [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

So **Accepted** = Pavel has reviewed it, discussed it and accepted it. **Taken into work** = the move to **To Do**, which happens when the team declares the release scope. [[wiki/people/irina-shishko.md|Irina Shishko]] had argued for exactly this shape a minute earlier — "может быть в туду[:] сначала его принять, а он должен находиться в туду, как только начали работать над этой [капабилити]" — and also floated collapsing the two, "то есть акцепт[ и] туду… соединить в одно"; Val's definition kept them separate [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## Who moves it to In Progress, and when

Irina asked, twice, and would not let it go: "[и]н[ ]прогресс кто переведёт?… [и] в какой момент?" — pointing out that the alternative is somebody sitting and watching: "то есть это тебе нужно сидеть и ждать[,] контролировать… вот кто[-]то взял в [ин]прогресс[ —] надо это бежать в [ин]прогресс брать" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

Pavel's manual answer was "когда хотя бы одна [ф]ича готова к реализации". **Kovalchuk's answer was to automate it:**

> "Мы это можем [за]автоматизировать[:] любая фича, которая начинается [в ин прогресс,] тогда переводит любой [капа]билити из туду в ин[ ]прогр[есс] тоже." — with [[wiki/people/andrey-bosik.md|Bosik]] adding "[п]ри этом можем назад" (and back again) [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

**He could not do it on the fly.** "Это займет некоторое время[,] надо… протестировать… [п]рям на лету не смогу." Val left it for Monday, together with moving all the MVP 1 capabilities into To Do: "давайте это оставим тогда на понедельник… дима, вы можете взять все M[V]P один… и перевести их в туду?" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Update, Sept 22 2026 — the other end of the workflow: a status after In Progress

The Sept-11 fix settled the front of the capability workflow. At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 Minsk stand-up]] the argument moved to the back: capability 122 sat In Progress with all its features closed, waiting on tests. [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] proposed a status "типа реквистест" (later, two statuses); [[wiki/people/irina-shishko.md|Irina]] wanted anything but In Progress; Pavel first objected to "слишком много статусов", then said a status "Скорее всего нужен", name open ("интегрейшн или ещё чтонибудь"). Nothing was set. Full debate on [[wiki/topics/test-automation-strategy.md]] (Sept 22) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

**A workflow snag.** Pavel could not move a story "Из реквест ревью… в комплитет", because of "особые настройки проекта h fm". Kovalchuk offered to look, now or later [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

## Open commitments

- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — automate the capability status transition from feature status (a feature going In Progress moves its capability To Do → In Progress, and back), after testing it — due after Monday Sept 14 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — move all MVP 1 capabilities into To Do — due Monday Sept 14 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — check why a story cannot move from Request Review to Complete in the "h fm" project settings — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]

## Open questions

- **What, if anything, has to happen between Accepted and To Do?** Klimovich asked directly — "что должно происходить с [капабилити,] для Того, чтобы он перешёл [из] [ак]септ[а] в туду[,] какой процесс[?]" — and the answer given was the release-scope declaration itself, with no intermediate step named — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

*(The derived notes record the same outcome — "the meaning was fixed rather than the status removed" — and attribute the automation to Kovalchuk.)* [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

**§15.8:** clear — Jira workflow only.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
