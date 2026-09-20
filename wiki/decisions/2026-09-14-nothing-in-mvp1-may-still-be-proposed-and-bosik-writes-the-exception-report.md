---
type: decision
title: Nothing in MVP 1 may still sit in "Proposed" — Val fixes the Jira status chain (Accepted → To Do with features → In Progress with a linked feature branch) and asks Bosik for an automated exception report
date: 2026-09-14
aliases: [nothing in MVP1 can be Proposed, sell the capabilities to the developers, exception report, эксепшн репорт, feature branch linked, To Do must have features, capability linked to requirements, requirements must have acceptance criteria, Kovalchuk changed the workflow]
source-count: 2
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

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — build a routine that checks the Jira status rules and sends a short exception report — only what does not match — to Val, Pavel Frolov and Andrei Klimovich — due unspecified; he agreed and needs to work out how — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — push every MVP 1 capability out of "Proposed" status — due immediately; Val: nothing in MVP 1 can still be Proposed today — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — make sure everything In Progress is scheduled, ahead of the next morning's meeting — due Sept 15 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## Open questions

- **Did the capability workflow change actually land?** Bosik believes Kovalchuk changed it; Pavel sees the old Proposed → Accepted colouring still in place — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

*(The derived notes carry the same four rules, the same "selling them to the developers" framing, and the same exception-report request to Andrei Bosik.)* [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

**§15.8:** clear — process and tracking only; no performance judgement of any named person is recorded, and none was excluded.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
