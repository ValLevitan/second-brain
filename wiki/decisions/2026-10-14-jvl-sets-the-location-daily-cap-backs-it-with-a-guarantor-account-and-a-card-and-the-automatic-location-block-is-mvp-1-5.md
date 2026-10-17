---
type: decision
title: JVL sets each location's daily cap because it guarantees the money to InComm — every location needs a back-up account and a card, low funds escalate by SMS and email to the secondary account and the master, and the automatic location block at the end of that chain moves to "MVP 1.5"
date: 2026-10-14
aliases: [Daily Cap устанавливаем мы, JVL sets the daily cap, we are the guarantor for InComm, guarantor account and credit card, balance checks every hour, secondary account then master then auto-block, automatic location block, автоблокировка локации, MVP 1.5, MVP один с половиной, a couple of locations without auto-block, operator and location contracts, sign-up master then locations, five-day payment window with InComm]
source-count: 2
status: active
open-commitments: 1
open-questions: 3
---

# JVL sets the daily cap and backs it; the automatic location block is "MVP 1.5"

Worked out at the [[wiki/meetings/2026-10-14-transactional-mvp1-launch-plan-brackets-daily-caps-and-mvp2-scope.md|Oct-14 3:49 PM launch-plan meeting]] (Russian) between [[wiki/people/val-levitan.md|Val]] and [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]. Val said he had pitched this "экспроптом и free ball" to a customer that afternoon; now "нужно… продумать и сделать это системно" [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]. The afternoon pitch is on [[wiki/topics/georgia-prize-card-processor-economics.md]] (Oct 14, 2:26 PM).

## Who sets the cap

- Val: "Daily Cap устанавливаем мы, потому что мы responsible for InComm, мы являемся гарантом для InComm в деньгах. InComm doesn't care." And: "Неважно, кто устанавливает дейли лимит. К примеру, мы согласуемся с Инком на один и тот же дейли лимит." [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- This sits on the open contradiction on [[wiki/organizations/incom.md]] (who sets a location's cap — InComm or JVL); it adds a second Val statement on JVL's side.

## The payment window with InComm

Val has started talks with InComm to widen it: "Сейчас, по-моему, мы согласились на три дня, а в контракте у нас стоит, по-моему, один день. Но нам нужно это сделать на пять дней." [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]

## The back-up for each location

- **A guarantor account and a card.** The operator or the location (or both) needs "гарантор аккаунт, с которого можно снять деньги, если мы перешли через лимит, и… кредитную карту", for a pre-check on the transaction. Today the sign-up has no such screens; Klimovich: "У нас есть только ACH" [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].
- **Balance checks.** "Duala дает нам такую возможность проверить баланс" (the name as heard). The operator contract should say that if a check finds too little money, JVL checks again every two hours, with a charge, "например, пятьдесят центов за каждую проверку". Later Val gave the daily example: at 10 a.m. JVL knows what it must draw for the day before; if it must draw $10,000 and only $9,000 is there, "мы начинаем проверять тогда каждый час… по моему, это стоит двадцать сан" [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]. ("Duala" may be [[wiki/organizations/dwolla.md|Dwolla]] — **inference** from the sound and the ACH role.)
- **Check, then draw.** "Попытка снять деньги и наличие денег на аккаунте – две разные вещи." Check the balance, draw what is there, then go to the secondary account [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].

## The escalation chain

- Klimovich's summary, which Val built on: if the location's primary ACH fails, try the secondary; if that fails, try the master; "Если мастер раунд, то дальше идет автоблокировка локейшн" [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].
- Val: before a block, send notices to the location and the master "и дать им возможность recover". His timeline example is in hours: 10 a.m. low funds found, a message to deposit now; 11 a.m. a "second notice"; by noon the money is drawn from the secondary account. Notices by SMS and email; an automatic phone call later, which needs the customer's opt-in [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].
- **The block covers the Flexports.** Val: "Автоблокировочный раз. Локации, это значит и флекс порты тоже." [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]

## The ruling: auto-block is "MVP 1.5"

- Klimovich: "Помните… когда планировали МВП один… Мы договорились, что автор блокировки пока у нас не будет." Val: "давайте назовем это MVP один из половины. Да, конечно… Пару машин можно поставить без этого. Извиняюсь, пару лакейшнок." [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- The derived notes: "Location auto-block moves to 'MVP 1.5'; a couple of locations may start without it." [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- This plans a change to Val's Sept-11 rule "автоматически мы никогда не блокируем" — see [[wiki/decisions/2026-09-11-lease-blocking-reaches-the-flex-ports-and-is-never-automatic.md]] (Oct-14 update). For MVP 1 the manual-only rule still holds.

## Contracts and sign-up

- **No templates yet.** Klimovich: "у нас нет шаблона, который мы готовы были подписывать, будь то с оператором или с локацией." Likely an operator contract for the equipment and the monthly fee, and a location contract giving access to its bank account. Val: "Это очень комплексная вещь, которая требует другого митинга." [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- **Val takes the contract architecture; Klimovich reviews.** "Это я на себя беру… Просто архитектором я хочу." [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- **Sign-up model (Klimovich).** A master account with basic data and ACH or card details; locations linked to it, each with its own financial details and a secondary card. "Мастер… будет видеть свои локации, а локации будут видеть только себя." For now done by hand [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].
- **Reports.** Val: the accounting reports may need to extend to masters and locations [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].

## Open commitments

- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — the contract architecture and templates (operator, location), with Klimovich reviewing — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]

## Open questions

- Can JVL see the limit on a back-up credit card? Klimovich asked; Val: "По моему, по моему, мы не можем." Not settled — [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- What is the contract structure for operators and locations? — [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- Is the balance check priced at about $0.20 or $0.50 per check? Val gave both — [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]

**§15.8:** clear — company fees and contract terms only. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
