---
type: meeting
title: Payment Hub GL Account Structure & Sales Tax (May 12 2026)
date: 2026-05-12
aliases: [Payment Hub Report and GL Account Structure, Payment Hub GL sales tax, GL account codes Payment Hub, Avalara sales tax reconciliation, Payment Hub taxability]
source-count: 1
---

# Payment Hub GL Account Structure & Sales Tax (May 12 2026)

**Date:** 12 May 2026, 6:01pm ET (~54m) (§11 recording header time). Notes-only — no transcript captured.
**Attendees:** [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/igor-donis.md|Igor Donis]], [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/sean-riley.md|Sean Riley]], [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/lev-rudky.md|Lev Rudky]] (late join).

Working session to get the **GL account codes Payment Hub needs to post into Business Central** and to settle how **sales tax** is handled. Nathan needed five new GL codes (two sales-invoice, one customer-payment, two AR-dimension); [[wiki/people/sean-riley.md|Sean]] approved the revenue/cost-of-sales accounts as shown in [[wiki/people/igor-donis.md|Igor]]'s spreadsheet, and Igor committed to creating them in both the BC sandbox and production by end of day. The dominant topic was sales tax: a single consolidated sales-tax GL account already exists, with **Avalara** (a BC add-on) capturing tax at transaction time by ZIP and producing state-by-state filing reports — but there is no cross-check back to the GL, and Georgia's county-based rates (6–9%) plus master-level tax-exempt COAM customers sharpen the need for state/ZIP granularity. The **architectural ruling**: Payment Hub does **not** decide taxability — it requests an invoice from the accounting host (BC + Avalara), which decides taxable/non-taxable per line from the customer default with a line-level override; Payment Hub may pass an explicit non-taxable signal where a business rule requires (e.g. the player win-payout leg). Val named this a **scope gap in the original Payment Hub design**. Reconvene in one week (May 19) with Lev invited.

Substance and citations live on [[wiki/topics/jvl-finance-back-office.md]] (May-12 2026 — Payment Hub GL codes + sales-tax reconciliation) and [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (May-12 2026 — Payment Hub taxability re-architecture). §15.8: GL / sales-tax / accounting-configuration economics only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_Payment_Hub_GL_Sales_Tax-May-12-2026.md]]
