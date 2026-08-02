---
type: meeting
title: Flex-IQ down / printer-bypass fail-safe design — July 17 2026
date: 2026-07-17
aliases: [IQ down printer bypass, MG>Printer bypassing IQ if IQ is down, printer bypass fail-safe]
source-count: 2
---

# Flex-IQ down / printer-bypass fail-safe design — July 17 2026

**Date:** July 17, 2026, 9:00 AM ET (transcript 00:00:03–02:13:11, ~2h13m)
**Attendees:** [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/val-levitan.md|Val Levitan]] (joined ~23 min in)
**Purpose:** Work out what happens at a location when the **Flex-IQ** unit — which sits in-line between the Mutha Goose game controller and the ticket printer — goes down or unavailable, so the location keeps operating (the "IQ down / printer bypass" fail-safe). Held in Russian; the launch on Mutha Goose locations is **August 1, 2026** (5 devices at 5 locations). [[raw/Meeting_Notes_IQ_Down_Printer_Bypass_Complete-July-17-2026.md]] [[raw/Meeting_Transcript_IQ_Down_Printer_Bypass_Complete-July-17-2026.md]]

- **The bypass fail-safe.** When Flex-IQ is fully dead, Mutha Goose beeps within seconds ("printer lost"); the cashier unplugs IQ and connects the printer directly, and Mutha Goose prints its cached unprinted tickets — the location keeps working the old way. [[raw/Meeting_Notes_IQ_Down_Printer_Bypass_Complete-July-17-2026.md]] [[raw/Meeting_Transcript_IQ_Down_Printer_Bypass_Complete-July-17-2026.md]]
- **The final single flow (decided).** One default path — card issuance, no player-facing choice; only on card failure can the cashier retry or print a standard Mutha Goose ticket that returns settlement to the old system. IQ stops ingesting Mutha Goose's 25 stored historical tickets. [[raw/Meeting_Notes_IQ_Down_Printer_Bypass_Complete-July-17-2026.md]] [[raw/Meeting_Transcript_IQ_Down_Printer_Bypass_Complete-July-17-2026.md]]

Durable substance lives on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Jul-17 section) and [[wiki/projects/georgia-market-rollout.md]] (Jul-17 section).

## Sources
- [[raw/Meeting_Notes_IQ_Down_Printer_Bypass_Complete-July-17-2026.md]]
- [[raw/Meeting_Transcript_IQ_Down_Printer_Bypass_Complete-July-17-2026.md]]
