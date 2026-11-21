---
type: meeting
title: Call "PROD test 2 with InComm kickoff" — Klimovich walks the open items before PROD test 2 and the first real location; Nathan's two runbooks (deployment check, recovery of the stuck first-test invoice) go to a Saturday 9 AM review with Pavel's team; QA cannot test real money; CIBC reconciliation not built; the location invoice is due on its date with 35% simple daily interest from day 7, standard Business Central layout, test invoice "in one hour"; the monthly connection fee becomes a recurring invoice to the master, net 15, interest from day 31 (Nov 20 2026, ~10:02–~10:35 AM)
date: 2026-11-20
aliases: [PROD test 2 with InComm kickoff, Andrei PROD Test 2 Billing Runbook and Invoice Terms, Nov 20 billing call, Nov 20 10:02 AM call, prod test 2 kickoff]
source-count: 2
open-commitments: 0
open-questions: 0
---

# PROD test 2 with InComm — billing runbooks and invoice terms (Nov 20 2026, ~10:02 AM)

**Date/time:** Friday November 20 2026, **~10:02 – ~10:35 AM Eastern** (recording), about 33 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Andrei_PROD_Test_2_Billing_Runbook_and_Invoice_Terms-November-20-2026.md]] [[raw/Meeting_Notes_Andrei_PROD_Test_2_Billing_Runbook_and_Invoice_Terms-November-20-2026.md]]. Teams title: "PROD test 2 with InComm kickoff". **Language: English**; Igor Donis spoke partly in Spanish and Felipe translated. It followed the [[wiki/meetings/2026-11-20-andrei-mvp2-1-release-november-25-and-master-role-in-2-2.md|9:02 AM MVP 2_1 / 2_2 call]] the same morning.

**Who spoke** (speaker labels): [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (called and led the call), [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/igor-donis.md|Igor Donis]], [[wiki/people/lev-rudky.md|Lev Rudky]], [[wiki/people/felipe-miranda.md|Felipe Miranda]] (label "Felipe Miranda Giorgi") [[raw/Meeting_Transcript_Andrei_PROD_Test_2_Billing_Runbook_and_Invoice_Terms-November-20-2026.md]].

**Purpose:** close, item by item, the open points before PROD test 2 and going live at the first real location — each with "exact date and responsible person" (Klimovich) [[raw/Meeting_Transcript_Andrei_PROD_Test_2_Billing_Runbook_and_Invoice_Terms-November-20-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-11-20-the-location-invoice-is-due-on-its-date-with-35-percent-simple-daily-interest-from-day-7-and-the-monthly-connection-fee-is-a-recurring-invoice-to-the-master-net-15-with-interest-from-day-31.md]] — the go-live target, Nathan's runbooks, QA limits, the stuck invoice, CIBC reconciliation, the invoice terms and interest, the layout, the monthly connection fee; all commitments and questions.
- [[wiki/decisions/2026-09-17-the-ninety-dollar-fee-is-drafted-from-the-location-not-paid-by-the-master.md]] (Nov-20 note) — the master as default payer.
- [[wiki/decisions/2026-10-09-a-real-transaction-is-run-in-production-on-the-new-version-before-the-first-real-location.md]] (Nov-20 note) — PROD test 2.
- [[wiki/organizations/incom.md]] (Nov 20, 10:02 AM) · [[wiki/topics/business-central-erp-implementation.md]] (Nov 20)
- People: [[wiki/people/andrei-klimovich.md]] · [[wiki/people/nathan-carver.md]] · [[wiki/people/pavel.md]] · [[wiki/people/igor-donis.md]] · [[wiki/people/lev-rudky.md]] · [[wiki/people/felipe-miranda.md]] · [[wiki/people/dmitri-chudinov.md]] and [[wiki/people/sergey-tsymanov.md]] (in absentia) · [[wiki/people/monica.md]] (in absentia) (all Nov 20)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share date, time and title and link each other. A corpus-wide grep for both filenames, "PROD_Test_2", "Billing_Runbook" and "10:02" found no page citing either file. The 9:02 AM call the same day is a different recording.
- **Identity.** The filename says "Andrei"; the speaker label is Andrei Klimovich, and the product-owner context fits him (§4 Andrei cluster).
- **§4 name calls.** "Dima" / "Serge" and the heard "Tsimanov Chudzinau and Tsimanov" = [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] and [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (**inference** — back-end context and the 9:02 AM call's labels); the notes write "Dzmitry, Sergey". "Igor" = Igor Donis (finance; he speaks). "Monica" = [[wiki/people/monica.md|Monica]] (**inference**, contracts role). "Lev" / "Blev" / "lever" = Lev Rudky.
- **Garbles kept as heard.** "income" / "incomes" / "Incom" = InComm; "Duala" / "Diwala" / "dual" = Dwolla; "MSPC" = MSBC (Microsoft Business Central); "location building" = location billing; "puddle" = Pavel; "90 days divided by the number of days" = $90 (reading); "subject for less confirmation" = Lev's confirmation (**inference**); "business type agnostic" kept as said (the notes: "payer-type agnostic"). Igor's Spanish lines are garbled by the speech-to-text; only Felipe's English translation is used.
- **Notes vs transcript.** They agree on the terms. The notes leave out the $90 figure Klimovich named (Val: "The amount depends on what we charge"). The notes list Nathan's "net 10 vs immediate" question as an open undertaking; the call itself answered it for the location invoice.
- **Skipped as chatter.** Waiting for Lev, Val's "his bioenergy is very strong" joke, link hunting, goodbyes.
- **Not recorded:** none; no personal passage.
- **§15.8:** clear — customer billing terms only. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Andrei_PROD_Test_2_Billing_Runbook_and_Invoice_Terms-November-20-2026.md]]
- [[raw/Meeting_Notes_Andrei_PROD_Test_2_Billing_Runbook_and_Invoice_Terms-November-20-2026.md]]
