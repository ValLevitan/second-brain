---
type: decision
title: Once one terminal registers in production on the new version, a real transaction is run there — as the three were done before — before JVL goes to its first real location, likely the week of October 12
date: 2026-10-09
aliases: [real transaction in production, реальную транзакцию, first real location, первую реальную локацию, three transactions as before, 3 транзакции мы сделали, production test transaction]
source-count: 2
status: active
open-commitments: 1
open-questions: 0
---

# A real transaction runs in production before the first real location

**Raised** by [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik") and **agreed** by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] on the [[wiki/meetings/2026-10-09-transactional-mvp1-test-machines-and-unclaimed-funds.md|Oct-9 Transactional MVP 1 call]] (Russian).

- **Bosik:** "нам надо на пророде когда. Реально хоть один терминал зарегистрируется в прод на новой версии надо прогнать, наверное, реальную транзакцию, какуюнибудь." [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- **Klimovich:** "Да, как мы делали это тогда? Под [мутагуз — garbled] 3 транзакции мы сделали обязательно сделаем то же самое здесь, прежде чем выходить в какую то первую реальную локацию. Я думаю, мы за следующую неделю мы это сделаем." [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]] *("мутагуз" may be MudaGoose / Mutha Goose — **inference**; when and where the earlier three transactions ran is not stated here.)*
- The notes record the same decision [[raw/Meeting_Notes_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]].

**Context.** It follows the production roll-out of [[wiki/decisions/2026-10-09-all-web-services-go-to-production-before-the-weekend-instead-of-waiting-for-georgia.md]].

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (with the team) — run a real transaction in production on the new version — due the week of Oct 12 2026, before the first real location — [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
