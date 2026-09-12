---
type: decision
title: MVP 1 never has MudaGoose — confirmed on the record — and ripping the supporting code out is assigned to MVP 3, not MVP 1
date: 2026-09-11
aliases: [MVP 1 never has MudaGoose, I would like you to confirm it for the transcript, I prefer to rip the code out, code that stays always crawls back, removal assigned to MVP 3, two of fourteen twenty percent of the time, we live in main]
source-count: 2
status: active
open-commitments: 1
open-questions: 0
---

# MVP 1 never has MudaGoose — and the code comes out at MVP 3

Ruled by [[wiki/people/val-levitan.md|Val]] at the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept 11 2026 8:04 AM call]]. Two separate questions were decided: whether MVP 1 *uses* MudaGoose, and whether the code that supports it *stays on disk*.

*(MudaGoose is the wiki's canonical name for the legacy payment mode; this transcript renders it "мутагуз / мотогус / мудагуз" and the derived notes render it "Moto-guse". Same thing.)*

## The confirmation Val asked for explicitly

> **Val:** "M[VP] один мы решаем, что у нас никогда нету мутагуз… [п]равильно[?] Я бы хотел бы для транскрипта, чтоб вы подтвердили." [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

He got it. This is consistent with, and hardens, [[wiki/decisions/2026-09-09-jvl-supports-both-dual-sas-and-single-sas-and-not-mudagoose.md]] (said to a customer two days earlier) and [[wiki/decisions/2026-09-07-flex-port-goes-sas-and-jvl-drops-the-old-machine-segment.md]].

## The argument about the code itself

[[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] offered the cheap version of compliance — "для нас это подтверждаемо[:] не выпиливать код, а просто сделать так[,] чтоб он… не работал" — and [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] agreed nothing needed removing ("не надо ничего выпиливать"), floating two product versions or branches as an alternative. Chudinov rejected branching on principle: "[н]у так не делается[;] мы живём[,] это git[,] мы живём в мейне" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

**Val pushed for removal, and gave his reason:**

> "[Я] предпочитаю выпиливать [к]од… [я] знаю, что всегда, когда код остается, он всегда потом вылезает каким[-]то образом и мешает… [е]сли это занимает день[,] 2, я бы на это пошёл." [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

**The cost was then put on the table and it was bigger than a day or two.** Chudinov's objection was time, not difficulty — "[е]сли б была только эта задача[,] без проблем, но я бы предпочел сосредоточиться на более важном" — and he had already prepared the switch-the-mode variant: "я уже подготовил вариант[,] мы просто переключаем режим". [[wiki/people/pavel.md|Pavel Frolov]] put a number on it: "это 2 из 14… это 20% времени" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. *(Two out of fourteen. The source does not say two of fourteen **what**; "20% of the time" is Pavel's own gloss and is quoted as such.)*

## The ruling

Val took the cost and moved the removal out rather than dropping it: "[т]ак хорошо, давайте тогда это на M[VP] 3" — and restated it plainly a minute later, "убрать [к]од, который поддерживает м[у]дагуз" is MVP 3. Chudinov agreed and said it would not get in the way of the work meanwhile: "я уверен, что нам это в работе никак не помешает" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

**So the MudaGoose code stays in main through MVP 1 and MVP 2, switched off, and is deleted at MVP 3.** It is also the base the lease-blocking feature was built on and is being reused from — see [[wiki/decisions/2026-09-11-lease-blocking-reaches-the-flex-ports-and-is-never-automatic.md]], which is the concrete case of Val's "code that stays always crawls back."

*(The exchange was conducted half in jest — Chudinov suggested they might yet want MudaGoose in Pennsylvania and Val threatened to fire him and Klimovich for the suggestion, then said "шутки [в] сторону" and put it on MVP 3. Recorded because the joke is where the ruling actually lands, not as a personnel matter.)* [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — remove the code supporting MudaGoose, at MVP 3 — due MVP 3, undated — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

**§15.8:** clear — scope and codebase only.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
