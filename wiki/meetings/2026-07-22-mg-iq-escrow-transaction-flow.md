---
type: meeting
title: MG-IQ Escrow Transaction Flow
date: 2026-07-22
aliases: [MG IQ escrow, MuthaGoose IQ escrow transaction flow, MG escrow answered no, Flex-IQ escrow transaction flow, store-nothing liability model, IQ commissioning no decommission, above-limit cash-out not processed, MG IQ escrow July 22 2026]
source-count: 2
---

# MG-IQ Escrow Transaction Flow — July 22 2026

**Date:** July 22 2026, ~9:00 AM Eastern (recording opens at the meeting start); ~40 minutes, in Russian. [[raw/Meeting_Transcript_MG_IQ_Escrow_Transaction_Flow_Complete-July-22-2026.md]]

**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], [[wiki/people/pavel.md|Pavel Frolov]], and [[wiki/people/dmitri-chudinov.md|Dzmitry Chudzinau]] (Dmitri Chudinov). [[raw/Meeting_Notes_MG_IQ_Escrow_Transaction_Flow_Complete-July-22-2026.md]]

The call Andrei convened (with Pavel and Dmitry, as agreed) to answer the open question left by the July-21 escrow discussion: **can MuthaGoose (MG) act as an escrow that holds a cash-out until Flex-IQ validates it?** **Pavel's answer was an immediate no** — MG has no such capability; Val said he expected that. The meeting then designed the **escrow-transaction flow** for the MG↔Flex-IQ integration without it: MG's ticket always prints and IQ runs in parallel, validating through the cloud and issuing a card only after full validation; JVL stores nothing on IQ and records only completed card-issued transactions, keyed to the location — deliberate liability protection. It also settled above-/below-limit cash-out handling, the LTE-only August-1 launch, and the go-ahead to resume SMIB. [[raw/Meeting_Notes_MG_IQ_Escrow_Transaction_Flow_Complete-July-22-2026.md]]

Durable substance (the answered escrow question, the print-ticket-then-validate-in-parallel flow, the store-nothing/know-nothing liability model, IQ commissioning with no decommission, the master-operator dashboard, above-/below-limit cash-out handling, the LTE-only launch, requirements-are-living, and the SMIB resume) → [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Jul-22 section). Directly continues the two July-21 calls — [[wiki/meetings/2026-07-21-escrow-model-and-owned-network-vision.md|the 7:05 PM escrow-model / owned-network call]] and [[wiki/meetings/2026-07-21-unbind-vs-freeze-and-offline-transactions.md|the 5:15 PM unbind-vs-freeze call]] — and the escrow/transaction-flow theme of the [[wiki/meetings/2026-07-17-iq-down-printer-bypass.md|July-17 IQ-down printer-bypass]] design.

§12: this meeting exists as two recordings of the SAME ~40-minute session. The `_Complete` pair (transcript 00:00–40:33, opening at the meeting start) is the full recording and the source of record; the two bare (non-`_Complete`) raws are a truncated partial captured mid-meeting (first ~31 minutes only) that the `_Complete` note itself marks superseded → §12-skipped (skipped.md Batch 213), not cited. §15.8: clear — IQ/escrow/MG/transaction-flow/device/market economics only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_MG_IQ_Escrow_Transaction_Flow_Complete-July-22-2026.md]]
- [[raw/Meeting_Transcript_MG_IQ_Escrow_Transaction_Flow_Complete-July-22-2026.md]]
