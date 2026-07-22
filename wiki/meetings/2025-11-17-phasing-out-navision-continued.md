---
type: meeting
title: Phasing out Navision (continued) — closing/freezing Navision and the Labs→BC approach (Nov 17 2025)
date: 2025-11-17
aliases: [Phasing out Navision continued, Navision decommission, freeze Navision, copy Systems chart of accounts to Labs, Navision open-order close-out]
source-count: 1
open-commitments: 3
---

# Phasing out Navision (continued) — closing/freezing Navision and the Labs→BC approach (Nov 17 2025)

**Date:** 2025-11-17 (6:22 PM recording header) · **Duration:** 38m 54s · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/lev-rudky.md|Lev Rudky]], [[wiki/people/mikhail-perelman.md|Mikhail Perelman]] (released early — "we don't need Misha for this"). Russian.

A continuation of the Navision→Business Central migration thread that the [[wiki/meetings/2025-11-04-finance-recurring-loans-consolidation.md|Nov-4 finance call]] made the priority. Val and Lev work through **how to close out the open items still living in Navision** and how to stand up **JVL Labs on Business Central** — landing on a new, simpler approach (copy the JVL Systems chart of accounts, adapt it to Canada, run both systems in parallel). Substance on [[wiki/topics/business-central-erp-implementation.md]] (Nov-17) and [[wiki/topics/jvl-finance-back-office.md]] (Nov-17); ties to the [[wiki/decisions/2025-06-17-implement-then-replace-business-central.md|finish-then-replace-BC]] ruling.

**§12 corpus-wide cross-check — distinct meeting.** Ran `qmd update` and searched the whole wiki: the filename "Phasing out Navision continued" is cited nowhere but `log.md`. It is a **Nov-17 6:22 PM** Val/Lev/Perelman working call — separate from the Nov-4 recurring finance call (Val/Alka/Igor, 2:10 PM, which *set* the migration plan) and the Nov-6 "2nd path" consolidation call. Different date, attendees and content (the open-order close-out mechanics + the copy-Systems-chart approach are new). The word "continued" in the title implies an earlier "Phasing out Navision" session, but no such transcript is in `raw/` — noted, not invented.

Durable points (single source):

- **Close the open Navision items mechanically, do not investigate how each was paid.** Old open purchase orders / invoices sit unresolved in Navision; Val wants them **closed by brute force under the assumption everything was received and paid**, ignoring small discrepancies, rather than reconstructing each. He specifically does **not** want the "paid" step to trigger accounting into investigating *which method* each invoice was paid by — "that would drag on for months." Lev agreed but warned the close-out still surfaces credit/debit nuances and must be done by **someone who understands the finances**, not casually.
- **Orders moved to BC were duplicated, not migrated — delete them soon.** Some still-open orders (from J Labs) were carried into Business Central, but they were **duplicated** (a copy also sits in an archive), **not yet deleted in Navision** — so they must be deleted quickly to avoid duplicates, "while Misha still actively remembers what these orders are."
- **Who can do the close-out.** Val floated giving access to [[wiki/people/alka-sood.md|Alka]] (who has Navision access); Lev doubted she knows the system and named **Cris** and **[[wiki/people/igor-donis.md|Igor]]** as capable (Igor "for sure"). Cris is ~85% busy. **Erica** (the Mexico accountant) still has Navision access and is a bookkeeper; between Alka, Igor and Erica they should find a way. The task "will take less time than this whole conversation for someone who knows how."
- **Val wants a full list of open orders (back to ~2017) to freeze Navision closed.** ~70 open orders exist, some dating back to ~2017; Lev to produce the full-period list and post it to SharePoint (transcribed garbled) for Val to work from. Goal: **freeze/"conserve" Navision in a fully-closed state** with nothing left hanging.
- **The audit tension.** Lev raised that freezing Navision cleanly may require it to **pass an audit first** — accounting periods (yearly and monthly) must reconcile; you can't have inventory appearing from nowhere, and large-sum manipulation is risky. Left as a caution, unresolved.
- **New approach for standing up Labs on BC — copy Systems, adapt to Canada, run in parallel.** Instead of building the Labs chart of accounts from scratch, Val proposed **copying the JVL Systems chart of accounts**, adapting only the **general ledger and the Canadian tax/taxable side** (Systems is built on US principles — some accounts unneeded, some new, currencies changed to Canadian), and **running Navision and BC in parallel from Jan 1**. Navision would then "fade fast — each month less and less, and within half a year we won't return to it," leaving only the question of how to close it properly. Both agreed this is easier than Val's original from-scratch plan. Lev caution: it is **not a straight copy** — each vendor/customer card carries accounting-classification fields that must reconcile with the posting setup, and some accounting steps were originally done by **Daniel** (whom Val will not re-engage), so Lev "can do it but slowly" and must copy what he hasn't done before from the existing companies.
- **Copy setup without transactions; possibly via the external consultant.** Lev noted that copying a company would drag along its transactions — he'd either strip all transactions or **copy only the setup/definitions without transactions**. Val thought the **external BC consultant** could do the data move; the consultant was in the US last week and is traveling home, so Lev will reach out.
- **The daily-BC accountants are trained.** Val's comfort with the parallel-run: the people working in BC daily — **Laura** (Colombia), **Cris**, and **Igor** (in Mexico, on AP/error control) — already know the system, so copying the Systems chart won't materially raise their workload; if they need to open a vendor or customer they understand how. **Mary** and **Elizabeth** are noted as *not* accountants.
- **Timing pressure — do it before Jan 1.** Val wants this done before Jan 1; he referenced **Alka's availability ending ~Feb 28** (transcribed "Алко … на сухое 28 февраля" — garbled; read as Alka's engagement end date) as a reason to move now, with Alka and Igor doing it together.
- **Anatol question.** Val asked whether **Anatol** (by context [[wiki/people/anatol-strekalov.md|Anatol Strekalov]], the Sr. Excel/SQL programmer) could raise/handle the Navision close-out himself; Lev needed at least a day to answer and, at the close, said yes Anatol is needed. Follow-up set for **Wednesday at 12**.

## Open commitments

- [ ] Lev Rudky — produce the **full list of open Navision orders** (~70, back to ~2017) and post it to SharePoint for Val — due before the Wednesday follow-up — [[raw/Phasing out Navision continued.md]]
- [ ] Lev Rudky — contact the **external BC consultant** about moving the data (copy setup without transactions) and about whether Anatol can take the close-out — due ~next day — [[raw/Phasing out Navision continued.md]]
- [ ] Val + Alka + Igor — close out / freeze Navision and stand up JVL Labs on BC (copy Systems chart, adapt to Canada, parallel run) — target **before Jan 1** — [[raw/Phasing out Navision continued.md]]

**§15.8:** clear — ERP-migration, chart-of-accounts and vendor/order economics only; no per-person compensation figures. (Alka's ~Feb-28 end date is a relationship/status fact, not compensation; recorded as garbled.)

## Sources

- [[raw/Phasing out Navision continued.md]]
