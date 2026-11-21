---
type: decision
title: The November 20 date for MVP 2_1 will not hold, and no new date is set (a weekend, or Monday, was floated); instead of reviewing live, every reporter cleans up their own MVP 2_1 capabilities, features and requirements (version, status, stale items) before a follow-up call the next day, with 2_2 left to the next week; CAP-267 (Flex IQ firmware management) was a placeholder and is closed, its TINTs and developer features moving into CAP-146; CAP-145's 20-plus unpublished requirements (on Anton Seregin) and the Port 13 terminal-update capability's stray tasks are to be sorted; no terminal is in the field yet — InComm registration is awaited (Nov 19 2026)
date: 2026-11-19
aliases: [MVP2_1 and MVP2_2 scope recap and review, Nov 19 MVP 2 clean-up call, MVP2_1 Reporter Cleanup and Release Date Slip, release date slip Nov 20, дата релиза 20 ноября нереально, reporter clean-up, по принципу репортера, CAP-267 closed, 267 мы закрываем и забываем про него, CAP-267 into CAP-146, Flex IQ firmware management, Flex-Port firmware update, CAP-145 requirements, больше 20 реквием к одной каполите, Anton Seregin requirements, Port 13 capability, порт 13, weekend release, Monday release, InComm registration wait, payment hub settlement review with Nathan]
source-count: 3
status: active
open-commitments: 5
open-questions: 3
---

# The Nov-20 date for MVP 2_1 will not hold; each reporter cleans up their own 2_1 items; CAP-267 is closed into CAP-146 (Nov 19 2026)

Agreed at the [[wiki/meetings/2026-11-19-andrei-mvp2-1-reporter-cleanup-and-release-date-slip.md|Nov 19 2026, 8:04 AM "MVP2_1 and MVP2_2 scope recap and review"]] (Russian, about 21 minutes), led by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], with [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau") and, for a few minutes, [[wiki/people/val-levitan.md|Val Levitan]] [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]. This is the clean-up call Klimovich proposed the day before — [[wiki/decisions/2026-11-18-first-installs-connect-aristocrat-through-the-bill-acceptor-not-aft-sas-data-and-new-reports-wait-for-mvp-3-and-the-cash-in-counter-gap-needs-acceptance-criteria.md]] (Nov-19 note). The release it is about was set on [[wiki/decisions/2026-11-12-mvp-2-splits-into-mvp-2-1-iq-and-port-and-mvp-2-2-web-services-lottery-becomes-goods-and-the-inspector-report-becomes-the-audit-report.md]] and dated on [[wiki/decisions/2026-11-05-mvp-2-is-kept-narrow-wi-fi-with-the-flex-iq-as-access-point-or-client-remote-flex-port-update-robust-installation-and-install-diagnostics-due-november-20-and-the-rest-goes-to-mvp-3-around-january-20.md]] (both have a Nov-19 note).

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word; garbles are kept as heard.)*

## The goal

Klimovich: go through "MP 21 в первую очередь, если останется времени время, то ещё MP 22"; make sure capabilities and requirements are "в актуальных статусах", answer open questions and gaps, then update release expectations, "потому что сегодня мы видим, что 21, например, ожидается завтра". He went through both versions the day before; every open question he could answer is answered, and the 2_1 capabilities are "в инпрогресс или септив" (heard; In Progress or Accepted) [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]].

## CAP-267 is closed; its content goes into CAP-146

- **Irina:** 267 "плейсхолдер короче это то, что должно быть под кап 146"; she has almost finished — 146 will hold "с тентами, которые были в 267 и с фичами разработчика"; "Поэтому 267 мы закрываем и забываем про него." 267 had only test items, no developer features [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]].
- **What the two are.** Pavel: 146 is "фермбаре апдейт флекс портов" (Flex-Port firmware update); 267 is "менеджмент прошивок флекса айкю" (Flex IQ firmware management) — "Может, именно поэтому они разделены" [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]].
- **Already done in MVP 1?** Klimovich: by its description 267 "у нас сделано в IP один" — remote updates to the IQ through the dashboard, controlled rollout, campaigns; he did not remember whether rollback exists. Chudinov: "Авто роллбек происходит автоматом… Система поняла, что не поднялась" [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]].
- **Server-side tests.** Pavel: the server-side tests were never automated — "они сделались исключительно это всё вручную"; they are "очень, очень сложно… Может быть, их вообще не стоит делать"; they need a test environment "который мы в лучшем случае только 22 с подымим", so the AWS services have a separate environment and all autotests run through it; on emulators that is very hard, and on a real device "это уже не автотест" [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]. The cloud test-environment thread is on [[wiki/decisions/2026-10-05-the-payment-hub-autotest-stand-is-not-mvp1-and-a-separate-meeting-with-andrei-designs-it.md]] (Nov-19 update).
- **The one feature inside.** Chudinov: it was "создана агентом по переделке наших этих билкин сталлеров [build installers]" into a simpler form, put under this capability by the agent "По какойто причине"; nothing to check, the build already works — "Она больше техническая инфраструктурная"; "Да оставляется можно закрывать." Irina: "я сейчас приведу её в порядок, ну закрою" [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]].

## CAP-145 — too many unpublished requirements (not settled)

- Klimovich opened "145 кэп": its requirements are "даже не в драфте не не впаблишьтся"; Pavel thought it was what "Андрей плотно нагенерировал"; Klimovich: "это всё числится за Антоном серёгиным, и они созданы месяц назад" — [[wiki/people/anton-seregin.md|Anton Seregin]]. Irina had published part of Andrei's reviewed ones, but "про 19 45 он ничего не писал" [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]].
- Klimovich: sort it out with Anton — remove them if not needed, or keep and move them on. Pavel: "весь этот список надо скормить к воду [Claude] и попросить его. Это более компактно сделать" — "больше 20 реквием к одной каполите", too many to grasp, "Не только человеком, но даже клоган" [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]].
- **Val stepped in:** "такие побило лежат на стороне продакт оно" (capabilities sit with the product owner) and "реглайменты с нами живут долго" (requirements live with us a long time); then "я должен взяться этот звонок" and he left [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]. Whether the list is shrunk with Claude was not settled.

## Port 13 — the terminal-update capability holds tasks that do not belong

Klimovich: the capability for "через терминал на порты получать апдейты" holds "Очень много всего". Pavel: tasks must come out — e.g. that "Евгений" should check "Качество сгенерированного кода для флекс портов выдать нам правила", so Claude follows them — "это явно не к обновлению имеет отношение"; "Это Что касается порт 13". Pavel is its reporter ("это я изначально создавал из древнейших задач"); its fix version shows 22 though it relates to a capability in 2_1 ("в 02:01"); Pavel: "надо сейчас вытянуть те задачи, которые не сделаны" [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]. Which Evgeny is meant is not said.

## The way of working — each reporter cleans their own items

Klimovich: "Я не уверен, что мы должны сейчас всё делать в режиме звонка. Мне кажется, это неэффективно." Everyone finds the capabilities, features and requirements "где они являются репортерами" and cleans what sits on 21 and 22 — wrong version, wrong status, out of date; "версия 21 и 22. У нас должно быть чистым и аккуратными и актуальными", "по принципу репортера". Irina: "Я предпочу сейчас проревью" (offline); Chudinov: "Нет, не сейчас", first see what Anton created and go through his own. Meet again tomorrow; Klimovich agrees the time with Val. 21 first — "22 мы можем уже на следующей неделе сделать. Сейчас главное 21 актуализировать." Pavel: "Всё занимаемся своими репортерами" [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]].

## The field

Chudinov asked if any terminal works yet. Klimovich: "В поле нет, мы всё ждём с инкомом. У нас проблема с регистрацией" — registration is due any moment, "Надеюсь, сегодня", then they can go install ("ехать восстанавливаться", heard); he no longer names a date; "Артвар [hardware] у нас есть весь на руках". Still open: with "нейтаном" ([[wiki/people/nathan-carver.md|Nathan Carver]], payment-hub context — **inference**) "что у нас ещё не сделано по пэймонт хабу"; Nathan wrote an email yesterday; "возможно, у нас ещё не всё для пеймэнт процессинга готово". Chudinov: on the hub or "по биллингу по по расчётам с двувой"; Klimovich: "по расчётам" (settlements; "двувой" is **unclear**) [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]. InComm: [[wiki/organizations/incom.md]].

## The November 20 date will not hold

- Klimovich: "У нас есть дата релиза 20 ноября это вообще как выглядит". Pavel: "Нереальность"; Irina: "Нет, нереально" [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]].
- Chudinov: the cornerstone tasks are done — "вайфай апдейты флэкспорта всё готово по симкартам получения данных завершаю сегодня"; "Помоему Сергей уже сделал эти азер гудс, которые на терминале" ([[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]]; "азер гудс" heard — perhaps "other goods", **unclear**). Left: "авто тесты и посмотреть, что там по мелочам и там ревью экранов"; "может, даже получится, что получится релиз на выходные" — "я аккуратно называю" [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]].
- Irina: "Я бы до понедельника да вот добить авто тесты… Кроме того, что написано, их же нужно ещё проверить." Pavel: the requirements found in the wrong state, if they turn out valid, may need more work [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]].
- **No new date was set** [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]. The same morning's Minsk stand-up was also pessimistic — Irina "до выходных", Samusenko "Вряд ли до выходных" without the cloud test environment — [[wiki/meetings/2026-11-19-daily-standup-cloud-test-environment-and-short-claude-messages.md]] [[raw/Meeting_Transcript_Daily_Standup_Cloud_Test_Environment_and_Short_Claude_Messages-November-19-2026.md]].

## How it sits against earlier rulings

- **Nov 5 / Nov 12 — evolution.** MVP 2 (then MVP 2_1) was due November 20 (Val: about the 23rd with normal delay); on Nov 19 the team says the 20th will not hold. The old date moves to History on the Nov-5 and Nov-12 pages.
- **Nov 12, recycler — contrast.** For the recycler Val ruled "scope is cut, the date never moves" — [[wiki/decisions/2026-11-12-the-recycler-gets-its-own-mvp-1-on-the-production-server-by-thursday-november-19-and-its-mvp-2-a-week-later-scope-is-cut-never-the-date.md]]. Whether that rule was meant for MVP 2_1 too is not said; here the date slips and scope is not cut (**inference** that the two differ).
- **Nov 18 — the call was held.** Klimovich's one-hour MVP 2_1 / 2_2 clean-up call ran on Nov 19 at 8:04 for about 21 minutes; "Сергей" was not on it.

## Open commitments

- [ ] Every MVP 2_1 reporter (Klimovich, Pavel, Irina, Chudinov and the team) — review their own 2_1 capabilities, features and requirements: fix version, status, remove stale items — due Nov 20 2026 (before the follow-up call) — [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — finish CAP-146 with the TINTs and developer features from CAP-267, tidy CAP-267 and close it — due Nov 19 2026 ("сейчас") — [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — pull the undone, unrelated tasks out of the Port 13 terminal-update capability — due unspecified — [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]
- [ ] Unassigned (with [[wiki/people/anton-seregin.md|Anton Seregin]]) — sort out the CAP-145 requirements: remove, or keep and publish — due unspecified — [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — review with Nathan what is still missing on the payment-hub side (settlements) after Nathan's Nov-18 email — due unspecified — [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]

(Klimovich agreeing the follow-up time with Val, and Chudinov finishing the SIM-card data that day, are logistics and status; not tracked.)

## Open questions

- What is the new MVP 2_1 release date — a weekend (Chudinov) or Monday Nov 23 (Irina)? Not set — [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]
- CAP-145: shrink its 20-plus requirements with Claude (Pavel), or keep them as product-owner material that lives long (Val)? — [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]
- Are the server-side firmware-update tests (CAP-267/146) worth automating at all, and only once a cloud test environment exists? — [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]

**§15.8:** clear — scope, dates and process only. **§15 #9:** clear — capability numbers only.

## Sources

- [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]
- [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Cloud_Test_Environment_and_Short_Claude_Messages-November-19-2026.md]]
