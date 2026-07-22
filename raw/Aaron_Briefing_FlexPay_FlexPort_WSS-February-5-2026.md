**BRIEFING FOR AARON**

Flex-Pay / Flex-Port / WSS Protocol — Responsibility Split

_Prepared: February 5, 2026 | Source: JIRA (HFM, FP, BEP projects)_

# Quick Overview

The Flex-Pay and Flex-Port systems communicate over a **WebSocket Secure (WSS) protocol**. Think of it as two ends of a phone line — Yavorski builds and maintains the Flex-Port end (the embedded hardware inside the gaming machine), and Chudinov builds and maintains the Flex-Pay end (the kiosk software that players interact with). The WSS protocol is the shared language they speak over that line.

# Responsibility Matrix

|   |   |   |
|---|---|---|
|**Area**|**Evgeniy Yavorski (Flex-Port)**|**Dzmitry Chudinov (Flex-Pay)**|
|**Primary Domain**|Embedded firmware on the Flex-Port board (STM32-based hardware inside the EGM slot machine)|Flex-Pay kiosk application software (the payment terminal the player uses)|
|**WSS Protocol Role**|Designs, defines, and implements the protocol on the Flex-Port side. Owns the protocol specification and message formats.|Implements the protocol on the Flex-Pay side. Expanded WSS for SAS Cashout, SAS Ticket-In, and SAS logging (FP-250, FP-251, FP-252).|
|**Cash-In / Cash-Out**|Handles bill validator (ID-003) communication, EGM cash-out forwarding, Redeemable vs. Playable message tagging (HFM-338, HFM-340, HFM-343).|Processes incoming WSS cash messages on the kiosk, manages transaction confirmation/cancel logic, handles payment processor integration (InComm, Pyramid).|
|**Firmware / Updates**|Builds firmware update mechanisms (flash stick, WSS over Ethernet), bootloader, and production support tools (HFM-215, HFM-216, HFM-279).|Triggers and manages remote firmware update delivery from the server/kiosk side (FP-181, FP-208).|
|**Logging & Diagnostics**|Implements on-device logging, local transaction storage (NVS/SQLite), and log transfer to Flex-Pay (HFM-209, HFM-210, HFM-278).|Receives and stores Flex-Port logs on the kiosk, exports them for support (FP-210). Builds backend ticket/report history (FP-270).|
|**Security**|Encrypted WSS implementation, TrustZone evaluation on STM32 (HFM-211).|Encrypted WSS communications on the kiosk side (FP-9).|
|**Server / Backend**|Not involved — embedded-only scope.|Payment Hub API, server registration, time sync, CMS/orchestration integration, InComm parameter management (BEP-2644, BEP-2213, BEP-2257).|
|**TITO Integration**|Supports TITO at the hardware/protocol layer via Flex-SMIB handoff (HFM-263).|Full TITO integration on kiosk — ticket creation, validation, redemption, HandPay/JackPot support (FP-253, FP-255, FP-267, FP-268).|

# Current Status (as of today)

## Yavorski — Active / Open Items

- 4 items In Progress: Log transfer to Flex-Pay, bill validator Box Full fix, stability testing, incremental crediting UI
- 7 items To Do: Including firmware update support (due 2/9), double-trigger prevention (due 2/15), ID-003 wake-up investigation (due 2/24)
- Key risk: Several items have Feb 2026 due dates clustering together

## Chudinov — Active / Open Items

- 7 items To Do: Including API expansion for negative Flex-Port scenarios (due 2/9), TITO SAS integration, remote firmware triggering
- 21 items Closed / 2 Done: Strong track record of delivery on WSS protocol expansion and kiosk features
- Recent bug fixes completed: Incorrect transaction status, cash balance after cancel, cash category distribution (FP-516, FP-517, FP-518)

# Key Takeaway for Aaron

**Yavorski is the protocol architect and embedded specialist** — he defines what the WSS messages look like and implements them on the hardware board inside the slot machine. **Chudinov is the kiosk application developer** — he takes those same protocol messages and implements them on the Flex-Pay payment terminal, plus handles all server/backend integration. The WSS protocol is the contract between them. This is why the ongoing knowledge transfer is critical: if only Yavorski fully understands the protocol specification, Chudinov (and the broader team) are dependent on a single point of knowledge.