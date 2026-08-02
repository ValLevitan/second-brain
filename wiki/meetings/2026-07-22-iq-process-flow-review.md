---
type: meeting
title: IQ Process Flow Review (July 22 2026)
date: 2026-07-22
aliases: [IQ Process Flow Review, Flex-IQ process flow review, IQ process flow update, Juan process-flow concerns, manual-entry reopening, keep-memory reopening, IQ process flow July 22 2026]
source-count: 2
---

# IQ Process Flow Review (July 22 2026)

**Date:** July 22, 2026, 5:00–5:59 PM Eastern (~58 min)
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/andrei-klimovich.md|Andrei Klimovich]].

[[wiki/people/juan-martinez.md|Juan]] walked through the **new Flex-IQ process flow** — the one built that morning on the [[wiki/meetings/2026-07-22-mg-iq-escrow-transaction-flow.md|9:00 AM MG↔IQ escrow-transaction-flow call]] with Pavel and Dmitry, architected by Val — and raised his concerns point by point. [[raw/Meeting_Notes_IQ_Process_Flow_Review-July-22-2026.md]] Juan accepted the points he agreed with (MG always prints and IQ does not suppress the ticket; "failed" not "voided"; Business Central posting unaffected because Nathan's flow only depends on successful transactions; automatic device decommissioning; sub-$7 intercepts ignored but a cashier notification required) and pushed back hard on the **store-nothing / no-memory** design with real edge cases — large wins where the player returns later, a dead IQ losing pending transactions, partial redemptions leaving fractional balances — proposing a temporary cloud store (3–5 days) plus manual entry under an administrator PIN held by the master. Andrei objected that manual entry destroys the fully-automated advantage over PAX; Val explained his memory-less reasoning (JVL as a guest on someone else's network) but conceded there is no technical barrier and that he has swung "like a pendulum." No decision was forced; Val took it overnight and the group booked a follow-up for July 23 at 8:30 AM. [[raw/Meeting_Transcript_IQ_Process_Flow_Review-July-22-2026.md]]

Durable substance (Juan's edge cases, the manual-entry / keep-memory reopening, the accepted points, automatic decommissioning + multi-device cap, PAX as the true competitor, the overnight deferral) → [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Jul-22 process-flow-review section). This is **Part 1 / the review** of the flow; a July-23 "IQ Process Flow Part 2" follows. §11 header time (5:00 PM start). §12: both raws new — uncited elsewhere and not skip-ledgered; one new meeting distinct from the morning MG-IQ escrow call. §15.8: clear — Flex-IQ process-flow / device / transaction / market economics only ($7/$1,000 thresholds, $2 per-transaction fee are product economics); no named-person compensation.

## Sources
- [[raw/Meeting_Notes_IQ_Process_Flow_Review-July-22-2026.md]]
- [[raw/Meeting_Transcript_IQ_Process_Flow_Review-July-22-2026.md]]
