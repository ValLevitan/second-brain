---
type: meeting
title: 2026-03-30 — Black Horse Entertainment Invoice-Payment Review (AR / Machine Collections)
date: 2026-03-30
aliases: [Black Horse invoice payment review, Black Horse Entertainment AR review, Black Horse machines invoice review]
source-count: 2
---

# 2026-03-30 — Black Horse Entertainment Invoice-Payment Review (AR / Machine Collections)

Thin stub. A two-segment Teams call on 30 March 2026 — Part 1 (~33m, 08:32pm; [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/igor-donis.md|Igor Donis]], [[wiki/people/felipe-miranda.md|Felipe Miranda Giorgi]]) and Part 2 (~9m20s, 09:24pm; Val + Felipe). Val reviews the outstanding machine invoices for **Black Horse Entertainment** — an operator/customer that bought machines on terms — pulled from Business Central, then uses it to teach a credit-and-collections discipline. Part 2 pivots to the machine-freeze bug fix and a question about Andrei Klimovich's new role.

**§12 — two segments → ONE stub, source-count 2.** Part 1 [[raw/Meeting_Transcript_Black_Horse_invoice_payment_review-1-March-30-2026.md]] and Part 2 [[raw/Meeting_Transcript_Black_Horse_invoice_payment_review-2-March-30-2026.md]] are the same meeting recorded in two parts; both cited.

Black Horse Entertainment is described inline as the example account — the durable knowledge is Val's collections discipline, not the customer entity, so no separate organization page was created.

Substance lives on the topic/person pages:

- **AR / collections discipline** — 12-month terms are a *privilege* (must be run by Val, not granted on a handshake); payments applied to the oldest invoice skew the aging picture; the retroactive credit-application / references / signed-contract / lien-against-property program with a Georgia corporate attorney to verify legal standing; the new delinquency rule Val gives Igor (letter + 15 days, then lock the account against new invoices past 45 days delinquent until 100% current); the controller as the "bad guy" so the salesperson never enforces the relationship; lease-expiry-on-nonpayment as a control; delinquencies "a couple of hundred thousand"; full Navision→Business Central migration confirmed. → [[wiki/topics/jvl-finance-back-office.md]] (Mar-30). [[raw/Meeting_Transcript_Black_Horse_invoice_payment_review-1-March-30-2026.md]]
- **Machine-freeze bug — cause + fix rollout (Part 2)** — the freeze is a **Linux kernel 4.5** incompatibility with a particular microprocessor that both freezes the processor and disables its internal watchdog timer (so the machine cannot self-reset); fix = new Linux kernel plus a second hardware watchdog timer that revives a fully-dead machine. Reproducible on demand in Minsk; Pavel testing; Eclipse approval expected within a day or two; available ~2 weeks; customers to be compensated case-by-case; Val frames the fix as "a source of pride, not shame." Continues the same-day-era Georgia overnight-freeze thread. → [[wiki/topics/omni-core-advancement-and-game-templating.md]] (Mar-30). [[raw/Meeting_Transcript_Black_Horse_invoice_payment_review-2-March-30-2026.md]]
- **Andrei Klimovich's role confirmed** — Felipe asked; Val confirmed Andrei is appointed **product & market manager for transactional products** (defining program requirements, shaping market strategy, representing JVL across Nebraska/Georgia/Texas) and owns all marketing, but is **not selling**. → [[wiki/people/andrei-klimovich.md]] (Mar-30). [[raw/Meeting_Transcript_Black_Horse_invoice_payment_review-2-March-30-2026.md]]

§15.8 clear — invoice/AR/machine-collections economics and deal terms are allowed; no named-person compensation appears.

## Sources

- [[raw/Meeting_Transcript_Black_Horse_invoice_payment_review-1-March-30-2026.md]]
- [[raw/Meeting_Transcript_Black_Horse_invoice_payment_review-2-March-30-2026.md]]
