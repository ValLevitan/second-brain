---
type: meeting
title: BOM Invoicing in Business Central (Apr 6 2026)
date: 2026-04-06
aliases: [Treatment of BOM in MSBC, BOM Invoicing in Business Central, bill of materials invoicing]
source-count: 2
---

# BOM Invoicing in Business Central (Apr 6 2026)

**Date:** April 6 2026, 2:33 PM Eastern (transcript header, recording "Treatment of BOM in MSBC") · ~17 min · Russian
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/lev-rudky.md|Lev Rudky]]

How bills-of-material are invoiced in Microsoft Business Central. The current modular-matrix BOM breaks at invoicing — BC shows each sub-block as its own line, so the team fakes single-price invoices in Excel, which corrupts the sales/AR record. Fix agreed: a **top-level parent part number per machine configuration** that appears as one invoice line at one price while the sub-blocks stay internal. Target go-live April 13 2026. [[raw/Meeting_Transcript_BOM_Invoicing_in_Business_Central-April-6-2026.md]] [[raw/Meeting_Notes_BOM_Invoicing_in_Business_Central-April-6-2026.md]]

Substance (the workaround problem, the top-level-BOM solution, naming convention, timeline) on [[wiki/topics/business-central-erp-implementation.md]] (Apr-6-2026); the Excel-invoice AR-integrity angle cross-links [[wiki/topics/jvl-finance-back-office.md]]. §15.8 clear — BOM/invoicing/machine economics only; no named-person compensation.

## Sources
- [[raw/Meeting_Transcript_BOM_Invoicing_in_Business_Central-April-6-2026.md]]
- [[raw/Meeting_Notes_BOM_Invoicing_in_Business_Central-April-6-2026.md]]
