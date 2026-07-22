---
type: meeting
title: Statements & loans review, "2nd path" — EDS reversal, consolidation truth, forensic loan dig (Nov 6 2025)
date: 2025-11-06
aliases: [statements and loans review 2nd path, Nov 6 finance, EDS transaction reversal, consolidation Nov 6, shareholder loan control sheet Nov 6, 3.325 million USD discrepancy]
source-count: 1
open-commitments: 4
open-questions: 2
---

# Statements & loans review, "2nd path" — EDS reversal, consolidation truth, forensic loan dig (Nov 6 2025)

**Date:** 2025-11-06 (4:01 PM recording header) · **Duration:** 49m 38s · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/alka-sood.md|Alka Sood]], [[wiki/people/igor-donis.md|Igor Donis]]. English.

The follow-on session to the [[wiki/meetings/2025-11-04-finance-recurring-loans-consolidation.md|Nov-4 finance call]] — Igor's consolidation is done and Alka walks the corrections, then the two big open threads: **reversing the artificial EDS inventory-build transaction** so the consolidated statements tell the truth, and the **forensic rebuild of the shareholder-loan record**. Substance on [[wiki/topics/jvl-finance-back-office.md]] (Nov-6 section) and [[wiki/topics/jvl-corporate-loans-and-shareholder-financing.md]] (Nov-6 section).

Durable points (single source):

- **Consolidation corrected.** Igor finished the consolidated statement. Fixes: the **expense→cost-of-goods-sold reclass** (done earlier for tax reporting) and **eliminations that hadn't posted properly** (the source of stray negative numbers). The remaining issue is **inventory in transit** JVL→EDS→Systems: two of three transactions landed in the correct year, but the **last shipment** was recorded on the Systems side in **2025** instead of **2024** — a **~$488,000 CAD** timing issue. It does **not** touch the P&L; it understates Systems' inventory and payables, sitting on the balance sheet.
- **Reverse the whole EDS transaction (both sides).** The EDS sale was a **legitimate but non-revenue** transaction — its purpose was **building up inventory**, not creating revenue — yet it is inside the consolidated **2024 total revenue of $12.5M**. Val directed backing it out entirely (not just the pending piece): the machines move into **2025 inventory**, so 2025 becomes **revenue creation with no cash spent on purchases**. Alka: it's a journal entry both ways for JVL and JVL Systems; she'll do another pass. Scale referenced: ~**335 machines at ~$8,000** ("was three [million], right" — Alka), i.e. roughly **$3M US**. Net income currently sits ~**$2.3M**.
- **These are internal, not filed.** Alka: "These aren't filed … we just want reality … we want the truth." The consolidated set is an internal management document; the external accountants get the final trial balance and JVL can explain the EDS reversal if they query it.
- **Everything moved to SharePoint.** Alka linked her Explorer files to SharePoint (a trick learned from **Dmitri**) — shareholder documents now live in two places: a **management-reporting** area Val can access ("shareholder and related party loans" with a **control sheet**), and an **accounting** folder ("Shareholder Loans") holding the documents.
- **Loan control sheet + monthly upkeep.** The control sheet covers the **2011 (due-to-2011-680)** balance and the **840194 / 84019** shareholder loan, and now carries both the **book balance** (money in/out) and **accrued interest**. **Laura** is to update it **every month** so Val always has a running total of what's available. Val added: also **accrue interest on the $20M from 2011** — "we need to accrue interest from the moment we lend money" or lose track — Alka to delegate the recurring build to Igor (Laura does the legwork).
- **The 3.325M discrepancy.** Val believes ~**$3,325,052** is **USD** he lent the company separately; Alka's records treat it as **~$2.25M USD** carried in CAD as ~**$3.3M** through yearly exchange-rate revaluation. Val's arithmetic (2.2M × ~1.4 ≈ $3M, not $3.3M) flags a possible **~$300,000 error**. Resolution: match each **loan document → GL transaction → bank statement** and re-examine how the exchange rate was applied year-on-year.
- **Suspected legacy bookkeeping errors (2008–2016/17).** Example from **2014**: ~**$880,000** shown coming in, a ~**$246k** exchange adjustment, then **$1.1M** going out with a net difference of only ~**$6,000** — Alka reads this as entries posted to the wrong account, reversed, and re-posted, which the system treats as legitimate. Val wants a **forensic dig**, focused first on **2014 and 2015**. The full detailed transaction history (per account, 2008→2025) is quick for Igor/Laura to pull.
- **Fraud framing.** Val walked a hypothetical (money in $500k, booked $490k, $10k out elsewhere); Alka described real mechanisms — a **fake vendor with a fake invoice**, a **pre-authorized payment to self slipped into the register**, an approval given despite a missing invoice. Val: "we had a fraud like this for $6 million." He wants the odd movements (e.g. an unexplained **$52,500** withdrawal) traced to the bank statement.
- **Igor's after-note.** After Val left, Igor showed that from **2017** an account labeled **"note payable Ontario USD"** was revalued **manually on the general journal** — by a person the transcript renders **"Daniel M" (explicitly not Daniel Estrada)** — rather than by the automatic exchange-rate valuation, a likely source of the discrepancies.

## Open commitments

- [ ] Alka Sood / Igor Donis — do another pass reversing the **whole EDS transaction** on both JVL and JVL Systems (journal entry both ways) so the consolidated statements reflect reality; send Val a **preliminary report Monday night** — [[raw/Statements and Loans review - 2nd path.md]]
- [ ] Igor Donis / Laura — pull the **detailed per-account transaction history (2008→2025)** for the loan reconciliation and match documents→GL→bank, starting with **2014/2015** — [[raw/Statements and Loans review - 2nd path.md]]
- [ ] Alka Sood — add **accrued-interest tracking on the 2011 $20M** loan to the control sheet and set it to recur (delegated to Igor); have **Laura update the control sheet monthly** — [[raw/Statements and Loans review - 2nd path.md]]
- [ ] Alka Sood / Val — chase the **two years with no loan documentation**, obtain the specific documents, have **Val sign** them, and file them so the documents tally to the control-sheet amount — [[raw/Statements and Loans review - 2nd path.md]]

## Open questions

- Is the ~**$3.325M CAD** an accumulated exchange-rate revaluation of a **$2.25M USD** loan (Alka), or a **separate USD advance** Val made (Val's belief)? A ~$300k gap to resolve by matching documents→GL→bank. [[raw/Statements and Loans review - 2nd path.md]]
- Who is **"Daniel M"** (not Daniel Estrada) who manually revalued the "note payable Ontario USD" from 2017? Identity unclear — flagged. [[raw/Statements and Loans review - 2nd path.md]]

**§15.8:** clear — all content is **corporate / consolidation / shareholder-loan economics** (allowed). No named-person compensation figures appear (Igor's "two-three days" to build a spreadsheet is task effort, not pay). Nothing held.

**Next meeting:** Tuesday **Nov 11**, ~11:00 (Alka also to regroup with Igor at 4:00 PM Toronto that day).

## Sources

- [[raw/Statements and Loans review - 2nd path.md]]
</content>
