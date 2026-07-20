---
type: meeting
title: CMS / PayFlex block-diagram review — arc session 2 of 3 (Aug 22 2025)
date: 2025-08-22
aliases: [CMS Block Diagram Arch 082225, CMS PayFlex block diagram Aug 22, block diagram meeting Aug 22, reconciliation architecture Aug 22, fund persistence meeting]
source-count: 2
---

# CMS / PayFlex block-diagram review — arc session 2 of 3 (Aug 22 2025)

**Date:** 2025-08-22 (12:03 PM) · **Attendees:** [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/will-jones.md|Will Jones]], [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/pavel.md|Pavel Frolov]] (Juan's birthday). [[raw/CMS- Block Diagram_Arch 082225.md]]

The **second** of the three-part CMS block-diagram review arc (Aug 20 → **Aug 22** → Aug 27, all ~12 PM). Where Aug-20 was a PayFlex-ecosystem walkthrough and the "CMS as a separate cloud server" direction, Aug-22 worked into Juan's written **"first course of business" Flex-POS release requirements** (auto-configuration, an ACH agreement per location, daily ACH debit within 24 hours, and a reconcilable accounting report) and then into a deep debate on **where the money lives and how to survive an Internet or hardware failure without losing funds**. No decisions were locked; the group agreed the next step is Nathan's use cases feeding requirements.

Substance lives on the topic/project pages, not here:
- What advanced vs Aug-20, fund-persistence/fault-tolerance debate, reconciliation, the arc sequencer: [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]
- Flex-POS release requirements (auto-config, ACH, 24h debit, reconciliation reporting), e-wallet/TITO fund flows, SAS/bill-acceptor mimicking, FlexPort storage: [[wiki/topics/flexpay-business-architecture-payout-devices.md]]
- Georgia market / July-2026 gift-card deadline: [[wiki/projects/georgia-market-rollout.md]]; the InComm gift-card processor: [[wiki/organizations/incom.md]]

**Derived source (§12 family — folded, no separate stub):**
- [[raw/First course of business POS 082225.md]] — Val's written **Flex-POS release requirements note** ("First course of business: Release the Flex-POS + dispenser into the market"), the document Juan read through on screen in this meeting (its four points map one-for-one to Juan's agenda: auto-config out of the box, ACH agreement, 24-hour ACH debit, reconcilable accounting). Folded onto the FlexPay topic as the Flex-POS release requirements. [[raw/First course of business POS 082225.md]]

## Sources

- [[raw/CMS- Block Diagram_Arch 082225.md]]
- [[raw/First course of business POS 082225.md]]
