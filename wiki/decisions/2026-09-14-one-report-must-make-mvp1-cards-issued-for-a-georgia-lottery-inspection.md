---
type: decision
title: Exactly one report has to make MVP 1 — cards issued over a period, on one button, for a Georgia Lottery inspection, copied from a competitor's report Klimovich already holds
date: 2026-09-14
aliases: [one report one button, audit report, cards issued over a period, Georgia Lottery inspection report, аудит тикет, competitor report reproduced, TITO printer width]
source-count: 2
status: active
open-commitments: 2
open-questions: 1
---

# One report must make MVP 1: cards issued, for an inspection

Set by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] at the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|Sept 14 2026 8:01 AM call]], and immediately checked by [[wiki/people/pavel.md|Pavel Frolov]] against the capability list, where it did not yet exist.

## The scenario that forces it

> "**Конкретный сценарий: на локацию приходит проверка из лотереи Джорджия, да, которая контролирует весь этот рынок, и говорит: покажите мне отчёт по выпущенным карточкам за последние икс время. И у кассира должна быть возможность нажать одну кнопку простую где[-]то и получить этот отчёт.**" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

An inspection from the [[wiki/organizations/georgia-lottery-corporation.md|Georgia Lottery]] — which Klimovich describes as controlling the whole market — turns up at a location and asks for a report of cards issued over a given period. The cashier presses one button and gets it.

## Scope

Klimovich scoped it tightly and put it inside MVP 1: "**[о]тчёт. Пока только один нужен. Я думаю, что его надо успеть сделать в [MVP] один. Я добавлю это к[а]пбилити.**" It rests on the issued-card history he had just ranked second in the transaction-block priority order — "история по карточкам выпущенным… напрямую связана с возможностью построить отчёт" (see [[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]] for that ordering) [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**He is not designing it from scratch:** "у меня есть пример такого отчёта, который делает один из наших конкурентов. Я думаю, мы его просто воспроизведём" — he holds a competitor's version of the same report and intends to reproduce it. *(The competitor is not named on the call.)* The open design work is what goes on it and how it fits the ticket printer: "[ч]то именно в нём указывается, как нам его уместить на наш [TITO —] вот этим я займусь тоже сегодня" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Pavel caught that it was not in the list

Pavel, going back over the capability list: "ты сейчас говорил про [audit ticket,] да[?] [Н]о я не вижу в списке [capabilities]." Klimovich confirmed the gap and named the window: "**нету[,] нету[;] я это добавлю… сегодня[-]завтра я буду только этим заниматься[ —] добавить репортинг, вот этот аудит… одна кнопка, один репорт**" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]. *("аудит тикет" is the transcript's rendering of what Pavel called the item; recorded as heard.)*

This is one of three things Klimovich listed as owing from the meeting, alongside the dual-balance logic and moving requirement 1538 — see [[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]].

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — add the capability for the one-button audit report (cards issued over a period), modelled on the competitor report he holds — due "today or tomorrow" from Sept 14 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — settle what the report shows and how it fits the ticket-printer format — due Sept 14 2026, promised for the same day — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## Open questions

- **What goes on the inspection report, and how it fits the printer width.** Undecided on the call — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

*(The derived notes record the same scenario, the same one-button requirement and the same competitor-report basis.)* [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

**§15.8:** clear — regulatory reporting and product scope only. **§15.9:** no licence or registration number appears in either source, and none is recorded here.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
