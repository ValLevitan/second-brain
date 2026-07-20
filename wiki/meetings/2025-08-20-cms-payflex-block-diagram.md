---
type: meeting
title: CMS / PayFlex block-diagram review — arc session 1 of 3 (Aug 20 2025)
date: 2025-08-20
aliases: [CMS Block Diagram Arch, CMS PayFlex block diagram, block diagram meeting Aug 20, back-office architecture Aug 20]
source-count: 4
---

# CMS / PayFlex block-diagram review — arc session 1 of 3 (Aug 20 2025)

**Date:** 2025-08-20 (12:04 PM) · **Attendees:** [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/will-jones.md|Will Jones]], [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/pavel.md|Pavel Frolov]]. [[raw/CMS- Block Diagram_Arch.md]]

The **first** of a three-part CMS block-diagram review arc (Aug 20 → Aug 22 → Aug 27, all ~12 PM; the Aug-22 and Aug-27 sessions are pending a later batch). Juan walked the group through the Georgia PayFlex/FlexPay ecosystem and the legacy CMS, and the meeting agreed to formalise Juan's rough block diagram, treat the future CMS as a **separate cloud server** starting with payment-device management, and keep the legacy CMS running in parallel. HHR was reaffirmed as a standalone system separate from CMS. [[raw/CMS- Block Diagram_Arch.md]]

Substance lives on the topic pages, not here:
- CMS-modernization direction (separate cloud server, legacy parallel, operator self-administration portal, the arc sequencer): [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]
- PayFlex device catalog, protocols (Mother Goose / e-wallet / SAS-TITO), master-operator model, and **Val's follow-up terminology corrections**: [[wiki/topics/flexpay-business-architecture-payout-devices.md]]
- Georgia market / July-1-2026 gift-card deadline: [[wiki/projects/georgia-market-rollout.md]]; the InComm gift-card processor: [[wiki/organizations/incom.md]]

**Derived sources (§12 family — folded here, no separate stubs):**
- [[raw/CMS_PayFlex_Block_Diagram-08-20-2025.md]] — an executive-overview meeting summary explicitly "prepared from the transcript CMS-Block_Diagram_Arch.md" (same attendees, same content); confirmed a derived summary of this Aug-20 session. [[raw/CMS_PayFlex_Block_Diagram-08-20-2025.md]]
- [[raw/back-office_architecture-august-20-2025.md]] — an AI-generated "Meeting notes" recap of this same Aug-20 session (identical attendees Juan/Will/Nathan/Pavel and topics — July-1-2026 gift-card rule, InComm processor, three device-communication models, cloud migration, master-operator model, Passport, HHR separation); the "back-office architecture" filename is misleading — content is the Aug-20 CMS/PayFlex meeting, not a distinct back-office session. [[raw/back-office_architecture-august-20-2025.md]]
- [[raw/val_comments_to_CMS_Block_Diagram_Arc.md]] — Val's async written commentary on this meeting's notes, correcting the FlexPay/FlexTower product definitions and the master-operator scope (folded onto the FlexPay topic as "Val's follow-up terminology corrections"). [[raw/val_comments_to_CMS_Block_Diagram_Arc.md]]

## Sources

- [[raw/CMS- Block Diagram_Arch.md]]
- [[raw/CMS_PayFlex_Block_Diagram-08-20-2025.md]]
- [[raw/back-office_architecture-august-20-2025.md]]
- [[raw/val_comments_to_CMS_Block_Diagram_Arc.md]]
