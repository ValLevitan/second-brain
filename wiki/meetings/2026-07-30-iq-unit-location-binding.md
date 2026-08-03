---
type: meeting
title: IQ unit-to-location binding — verifying a unit is physically where it is registered
date: 2026-07-30
aliases: [IQ Unit Location Binding, Spec_gaps, unit-location verification gap]
source-count: 2
---

# IQ unit-to-location binding — verifying a unit is physically where it is registered

**Date:** July 30, 2026, 10:01–10:25 AM ET (~23 min). Teams meeting "Spec_gaps," organized by Val.
**Attendees:** [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/juan-martinez.md|Juan Martinez]].

Andrei raised a **design gap** in the IQ / Flex-IQ rollout: the system cannot verify that a given IQ unit is **physically at the location it is registered to**. Binding is done manually in the payment hub today, so nothing stops an operator moving a unit from a registered location A to an unregistered location B — cards issued at B would still pass and be billed to A. The group weighed keeping manual binding versus pushing binding onto the operator (Val preferred operator-driven), floated an LTE-modem triangulation + Mutha Goose serial read to "quietly" listen to a unit's location, and touched a related collections angle (registering credit against a company's title). Val's ruling: **do not over-engineer in a vacuum** — the gap is not important for the 5-machine pilot, so **park it**, get to a real pilot, gather real cases and revisit. This relates to the IQ-binding thread from the [[wiki/meetings/2026-07-21-unbind-vs-freeze-and-offline-transactions.md|Jul-21 unbind-vs-freeze]] and [[wiki/meetings/2026-07-21-escrow-model-and-owned-network-vision.md|Jul-21 escrow-model/owned-network]] meetings. [[raw/Meeting_Notes_IQ_Unit_Location_Binding-July-30-2026.md]] [[raw/Meeting_Transcript_IQ_Unit_Location_Binding-July-30-2026.md]]

Substance lives on:
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Jul-30) — how registration and the InComm secret-key check work, the manual-vs-operator-driven binding options, the LTE-triangulation + MG-serial location read, the title-registration collections idea, the InComm decommissioning gap, the "park it for the pilot" decision, and the minimum-monthly-charge idea. [[raw/Meeting_Notes_IQ_Unit_Location_Binding-July-30-2026.md]]

## Sources

- [[raw/Meeting_Notes_IQ_Unit_Location_Binding-July-30-2026.md]]
- [[raw/Meeting_Transcript_IQ_Unit_Location_Binding-July-30-2026.md]]
