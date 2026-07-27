---
type: meeting
title: Val–Nathan Business-Central sync — MSBC API tested, per-transaction reconciliation, the design-integrity concern (Mar 11 2026)
date: 2026-03-11
aliases: [Val Nathan BC sync Mar 11, Nate Val Sync March 11, MSBC sandbox, MSBC load test, per-transaction reconciliation, design integrity logging, Dwolla integration start]
source-count: 1
---

# Val–Nathan Business-Central sync — MSBC API tested, per-transaction reconciliation, the design-integrity concern (Mar 11 2026)

**Date:** 2026-03-11 (2:01 PM recording header) · **Duration:** ~25m47s · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]] (started transcription), [[wiki/people/nathan-carver.md|Nathan Carver]]. English.

**Purpose:** a quick pre-meeting sync before the same-day finance meeting, continuing the payment-hub↔Business-Central reconciliation thread from the [[wiki/meetings/2026-02-11-val-nathan-jira-sync.md|Feb-11 Jira sync]] and the [[wiki/meetings/2026-02-18-val-nathan-business-central-sync.md|Feb-18 Business-Central sync]]. Since Feb-18, Nathan has done the direct MSBC-API work (BEP 2692 territory — creating/updating customers and invoices in Business Central) and reports it reliable; he is now down to configuring the MSBC sandbox with finance. Val raised three durable concerns — transaction **volume / load testing**, the **reconciliation trigger** (per-transaction vs per-invoice), and **back-end design integrity** (sequential audit logging) — and directed Nathan to open an email exchange to Pavel on the design-integrity question.

**§15.8:** clear — no compensation content.

Substance (MSBC API tested reliable, token-reauth as the only retry mode; the load-test plan; per-transaction reconciliation preference; the InComm-invoice-vs-per-transaction trigger debate; the design-integrity / sequential-logging / double-key traceability discussion; the email undertaking to Pavel; Dwolla/ACH integration started) lives on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Mar-11) and [[wiki/people/nathan-carver.md]] (Mar-11).

## Sources

- [[raw/Nate_Val_Sync-March-11-2026.md]]
