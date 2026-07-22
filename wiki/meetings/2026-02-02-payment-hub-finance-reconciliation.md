---
type: meeting
title: Payment Hub finance sync — reconciliation model (Feb 2 2026)
date: 2026-02-02
aliases: [Payment Hub Finance Sync, payment hub reconciliation, payout report, Payment Hub is a transport]
source-count: 1
---

# Payment Hub finance sync — reconciliation model (Feb 2 2026)

**Date:** 2026-02-02 (8:02 PM recording header) · **Duration:** ~1h11m46s · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/nathan-carver.md|Nathan Carver]] (started transcription), [[wiki/people/alka-sood.md|Alka Sood]], [[wiki/people/sean-riley.md|Sean Riley]], [[wiki/people/juan-martinez.md|Juan Martinez]]. English.

**Purpose:** the finance/engineering group worked the hardest open question on the payment hub — how a single bulk Dwolla deposit into the JVL bank is broken back down and reconciled against the individual debit-card / gift-card invoices in Business Central. Val held the line that **Payment Hub is a "transport," not an accounting tool** and that reconciliation/posting must live in Business Central; Alka and Sean pushed for a daily **"payout report"** summary; the meeting ended with an undertaking to go back to Dwolla and InComm for an automated report that splits one total into per-card detail.

Substance and the payment-hub arc sequencer live on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Feb-2-2026 section); the Business-Central reconciliation angle is also noted on [[wiki/topics/business-central-erp-implementation.md]] (Feb-2-2026).

**§15.8:** clear — vendor/module economics and process only (the $0.48-per-transaction / "20 accountants" cost argument is a business-model point, not compensation).

## Sources

- [[raw/Payment_Hub_Finance-February-2-2026.md]]
