---
type: decision
title: Once one terminal registers in production on the new version, a real transaction is run there — as the three were done before — before JVL goes to its first real location, likely the week of October 12
date: 2026-10-09
aliases: [real transaction in production, реальную транзакцию, first real location, первую реальную локацию, three transactions as before, 3 транзакции мы сделали, production test transaction]
source-count: 4
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

## Note, Nov 20 2026 — PROD test 2 is being prepared; the first test's invoice is still stuck

At the [[wiki/meetings/2026-11-20-andrei-prod-test-2-billing-runbook-and-invoice-terms.md|Nov-20 ~10:02 AM "PROD test 2 with InComm kickoff" call]] (English), Klimovich called the next step "our prod test 2 and actually the going live with our first real location", hoping to go to the location "next week, let's say Wednesday or Thursday". [[wiki/people/nathan-carver.md|Nathan Carver]]: the invoice "from our first test run" is still stuck and must be recovered by runbook before "another test"; Pavel's team reviews the runbooks with him on Saturday Nov 21 at 9 AM [[raw/Meeting_Transcript_Andrei_PROD_Test_2_Billing_Runbook_and_Invoice_Terms-November-20-2026.md]]. When the first test ran is not said here. The commitment above stays open. Detail: [[wiki/decisions/2026-11-20-the-location-invoice-is-due-on-its-date-with-35-percent-simple-daily-interest-from-day-7-and-the-monthly-connection-fee-is-a-recurring-invoice-to-the-master-net-15-with-interest-from-day-31.md]].

## Note, Nov 24 2026 — test card activations work; the first install is set for this week

At the [[wiki/meetings/2026-11-24-payment-hub-invoice-terms-template-and-first-install.md|Nov-24 11:16 AM Payment Hub call]] (English) Klimovich said "as far as we see the test activation of those cards, how it goes, there is nothing that holds us from the installation. So actually we are ready"; the transfer "from my account to Dwola, from Dwola to JVL" is still to be finished, "because it worked the last time." Val: "Let's make our first installation and polish things as we go along"; target "tomorrow" (Nov 25) [[raw/Meeting_Transcript_Payment_Hub_Invoice_Terms_Template_and_First_Install-November-24-2026.md]]. Whether these test activations ran on the new version in production is not said, so the commitment above stays open. Detail: [[wiki/decisions/2026-11-24-first-transactional-install-now-invoice-due-upon-use-of-service-interest-from-day-7-internal-and-the-invoice-template-moves-out-of-business-central-into-github.md]].

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- [[raw/Meeting_Transcript_Andrei_PROD_Test_2_Billing_Runbook_and_Invoice_Terms-November-20-2026.md]]
- [[raw/Meeting_Transcript_Payment_Hub_Invoice_Terms_Template_and_First_Install-November-24-2026.md]]
