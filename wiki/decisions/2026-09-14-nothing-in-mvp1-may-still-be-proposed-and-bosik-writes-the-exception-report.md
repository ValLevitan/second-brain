---
type: decision
title: Nothing in MVP 1 may still sit in "Proposed" — Val fixes the Jira status chain (Accepted → To Do with features → In Progress with a linked feature branch) and asks Bosik for an automated exception report
date: 2026-09-14
aliases: [nothing in MVP1 can be Proposed, sell the capabilities to the developers, exception report, эксепшн репорт, feature branch linked, To Do must have features, capability linked to requirements, requirements must have acceptance criteria, Kovalchuk changed the workflow, every author cleans their own, shared requirements filter, requirement 1454 back to Draft, daily capabilities report, around eighty items classified as blockers, report arrives every morning by email, To Do is the working floor]
source-count: 6
status: active
open-commitments: 3
open-questions: 1
---

# Nothing in MVP 1 may still be "Proposed"

[[wiki/people/val-levitan.md|Val Levitan]] closed the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|Sept 14 2026 8:01 AM call]] with process rather than product: "здесь ещё пару организационных вопросов." What follows is the Jira hygiene rule for the October-1 release [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## The rules, as Val stated them

1. **No MVP 1 item may still be in "Proposed".** "[У] нас мы не можем сейчас быть уже в состоянии [Proposed;] если это MVP один, то [Proposed] уже не может быть"; and again, sharper: "**на сегодняшний день [Proposed] в [MVP] один существовать уже не мог**." The minimum status is **Accepted** — "[Proposed] то как минимум [Accepted]." The negotiation over each one sits "между Андреем Климовичем и Павлом" — between [[wiki/people/andrei-klimovich.md|Klimovich]] and [[wiki/people/pavel.md|Pavel Frolov]].
2. **Anything already in To Do must have features under it.** "[В]се вещи, которые находятся уже в [To Do], должны иметь в себе [features]."
3. **Features being worked on must be In Progress and carry a linked feature branch.** "[Ф]ичер[ы], над которыми работают, должны быть [In Progress,] и иметь в себе… [link to] feature branch."
4. **A capability in progress cannot be unlinked from its requirements, and a requirement cannot be without acceptance criteria.** "[К]ейпобилити, которые уже [In Progress,] не могут быть не привязаны [к] ре[к]ва[йментс]. [Р]иквайрменс не могут не иметь в себе [acceptance criteria]."

[[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

These sit directly on the chain settled four days earlier — capability → requirements (living in the regulation) → features — see [[wiki/decisions/2026-09-11-acceptance-criteria-live-in-the-regulations-not-the-capabilities.md]] and [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]].

## Irina's stricter version, which Val accepted

[[wiki/people/irina-shishko.md|Irina Shishko]] put the gate one step earlier: a capability should only be **Accepted** once it already holds all its requirements — "[capability is] акцепт[ed], если он содержит всё[ ре]гламент[ы]… то есть над ними уже поработали, его приняли, и дальше можно разрабатывать" — and requirements themselves should change status when they are approved: "[т]оже требования, когда приняты, они должны поменять свой статус." Val conceded the principle while keeping his own floor: "**[н]у в общем[-]то да… [н]у хотя бы если уже [In Progress,] то это вообще ни в какие рамки не заходит**" — an In-Progress item failing the rule is beyond excuse [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Whose job it is

Val put the whole left-hand side of the chain on Klimovich, in a phrase worth keeping: the requirement statuses "**Андрей[,] управляете вы. Всё, что находится со стороны кейпо[]билети, это ваша задача. И вы должны протолкнуть, чтоб они ушли со статуса [Proposed]… [т]о есть ваша задача [Proposed] в кавычках продать… [девелоперам]**" — his job is to *sell* the capabilities to the developers. Only then "нам нужно смотреть, чтоб на это стали [features;] эти [features] включили в [schedule]" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

Pavel's closing task, set by Val: make sure everything In Progress is actually scheduled — "Павел, ваша задача, чтобы всё то, что в прогрессе, было [scheduled]", with Val conceding it probably already is: "в принципе, оно не может быть не [scheduled], но на всякий случай" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## The automated exception report

Val asked [[wiki/people/andrey-bosik.md|Andrey Bosik]] — twice, once per half of the rule set — to build a routine that checks the logic and mails only the mismatches: "Андрей Босик, вы можете написать на это [exception] репорт?… [т]о[,] что не совпадает[ с] правил[ом]." Distribution: Val, **Pavel and Klimovich**. Bosik agreed and asked for thinking time: "[н]адо подумать, я думаю, что можно, но надо подумать, как это реализовать", and separately thought something similar may already exist — "да, нужно[;] по[-]моему, есть такое у нас." His own summary of the plan: "[т]ак я просто сделаю такой отчёт[,] и он будет всем приходить" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

*(This is **Andrey Bosik** the DevOps engineer, not Andrei Klimovich. Val addresses both men as "Андрей" throughout the meeting; each instance here is resolved by the surname Val speaks — "Андрей Босик" for the report, "Андрей Климович" for the capability work — and by role.)*

## The unresolved bit of ground under all of it

Val opened the block by asking whether [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] had changed the capability workflow. Bosik: "[н]асколько знаю, да, поменял." Pavel saw evidence it had not taken effect — "[п]осле [Proposed] Accept это он зелёненьким остался" — Accepted still showing green after Proposed. Nobody resolved it on the call, and Val proceeded as though the change had landed [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**One correction inside the exchange, worth keeping straight:** Val's first phrasing swept In-Progress items into the "must move to Accepted" rule, and Pavel stopped him — "не так[:] те, которые [In Progress,] это уже после [Accepted]", with Irina adding "это уже их реализовывает девелопер." Val accepted the correction and restated that he meant **Proposed** only [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Update, Sept 16 2026 — Klimovich has cleaned his own items, and hands the rest back to their authors

Klimovich opened the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept-16 8:01 AM call]] with the status sweep as his first item: "я почистил [ка]п[а]билити [и] ре[кваймент]с, которые были [в] неподходящих статусах. Теперь все, за которые я отвечаю, они все переведены в актуальные статусы" — everything he authors is now in a current status [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**He explicitly did not touch anyone else's, and pushed the obligation outward:** "те [ка]п[а]билити[с и] ре[кваймент]с, чьим автором я не был, я не трогал. Я советую каждому автору посмотреть и актуализировать их" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. That converts one commitment into five: the four requirement authors named on this recording are Klimovich, [[wiki/people/dmitri-chudinov.md|Chudinov]], [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] — Pavel's own count of who writes them: "часть Андре[й] создавал, часть Дим[а], часть [Ир]а, часть я" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**The status discipline was exercised live twice on the same call**, in the opposite direction to the usual push forward: requirement **1454** was moved *back* from Published to Draft because the error catalogue it depends on does not exist yet, and requirement **1451** was taken off Published as well (the target status is garbled in the transcript) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Pavel's process proposal, not yet built:** a filter showing the live requirements from all four authors, so the team walks one shared list instead of one person's — "может нам сейчас сделать какой[-]то фильтр, который показывает актуальные [реквайрментс]… и иметь этот общий список у всех". [[wiki/people/andrey-bosik.md|Bosik]] agreed ("да я тоже так думаю"); the meeting used Irina's list for the day instead [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Update, Sept 18 2026 — the exception report is built, running and mailing every morning, and it opened the meeting

**Bosik's report exists and is in daily operation.** The [[wiki/meetings/2026-09-18-transactional-mvp1-capability-cleanup-and-the-monday-deadline.md|Sept-18 8:03 AM call]] opened on it, with Klimovich reading that morning's edition: "**пришёл новый репорт по поводу [капабилити]с[,] [реквайрментс,] их состояни[й]. У нас там по[-]прежнему… около 80 в состоянии, которое они считаются завершёнными. Классифицируют их как бло[к]еры. Это не очень хорошо, так не должно быть[.] Что мы с этим можем сделать в ближайшее время?**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**Bosik confirmed the mechanism when Irina asked where the reports were:** "**на почту там каждое утро… приходит отчёт[,] да[,] по тем критериям, которые…**" — it arrives by email every morning, against the agreed criteria. Asked whether it covers everything, he scoped it: "**Нет, MVP один только**", and again "**100% [MVP] один**". Klimovich approved the scope — "**Надеюсь, что [MVP] один, только[;] мы ж пока про MVP 2 не говорим**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**The commitment is therefore discharged — with one gap worth flagging.** The Sept-14 distribution list was Val, Pavel Frolov and Klimovich. [[wiki/people/irina-shishko.md|Irina Shishko]] is not on it, and said so: "**Почему я его не видела?**" She drives the capability board in practice and is the person who would act on the report [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**The ~80 figure is recorded as the report's own output, and its sense is unclear.** The transcript says the 80 items sit "**в состоянии, которое они считаются завершёнными**" — in a state in which they count as *completed* — while the derived notes gloss the same sentence as "states that count as **incomplete**" [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]. Opposite senses; the "blockers" classification fits the notes' reading better, but it is not what the source says. **Recorded as spoken and flagged unclear.** The whole capability-cleanup sweep that followed was Klimovich's answer to his own question — see [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]].

**The working status floor was restated in practice.** Klimovich asked which status means a capability is thought through and ready to work — "**Какой нижний статус?**" — and Irina answered "**В прогрессе или в туду**". He then filtered for everything **below In Progress or To Do**, plus everything unassigned. Requirements were moved along the parallel chain: Irina, of a requirement stuck in Draft, "**эктив — это как раз из драфта в эктив**", with review and Publish after it [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

*(**Still unmentioned:** whether [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]'s change to the capability workflow actually landed — the open question below — and Pavel's shared cross-author requirements filter. Neither was raised on Sept 17 or Sept 18.)*

## Open commitments

- [ ] All four requirement authors — [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] — review and update the status of every capability and requirement they authored, as Klimovich has done for his own — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — build the shared filter showing the live requirements from all four authors, so the team walks one list — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — make sure everything In Progress is scheduled, ahead of the next morning's meeting — due Sept 15 2026; **partly advanced Sept 18** — he set schedules for his own features (165, FlexPort 9 and 10, 173; 160 was also named as his) during the planning half of that call — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## History

- [x] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — build a routine that checks the Jira status rules and sends a short exception report — only what does not match — to Val, Pavel Frolov and Andrei Klimovich — due unspecified. **Discharged by Sept 18 2026:** the report is built and arrives by email every morning against the agreed criteria, scoped to MVP 1, and Klimovich reads it to open the daily call. **[[wiki/people/irina-shishko.md|Irina Shishko]] is not on the distribution and has not seen it** — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [x] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — push every MVP 1 capability out of "Proposed" status — due immediately; Val: nothing in MVP 1 can still be Proposed today. **Discharged for his own items on Sept 16 2026** ([[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]); items authored by others were deliberately left to their authors — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## Open questions

- **Did the capability workflow change actually land?** Bosik believes Kovalchuk changed it; Pavel sees the old Proposed → Accepted colouring still in place — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

*(The derived notes carry the same four rules, the same "selling them to the developers" framing, and the same exception-report request to Andrei Bosik.)* [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

**§15.8:** clear — process and tracking only; no performance judgement of any named person is recorded, and none was excluded.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
