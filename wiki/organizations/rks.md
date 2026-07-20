---
type: organization
title: RKS (Mother Goose board maker)
date: 2025-07-09
aliases: [RKS, RTS, Mother Goose, Mutha Goose, Mutagoose, Muda Goose, Mutable, Mutabus, Jim RKS]
source-count: 2
---

# RKS (Mother Goose board maker)

RKS is the third-party maker of the **Mother Goose** board (transcribed variously "Muda Goose," "Mutagoose," "Mutabus," "Mutable"), the payout/print controller that sits at the end of the machine daisy-chain in Georgia COAM locations. JVL's Flex-POS strategy centres on capturing the Mother Goose ticket signal, so RKS is a recurring counterparty. JVL's contact there is **Jim**. [[raw/Flex-POS Mid-Iteration Sync.md]] [[raw/Flex-POS Iteration Planning 2025-07-14.md]]

## What RKS makes and how it wires up

- In each machine a **yellow board** (from RKS) is daisy-chained over **RS-485** to the Mother Goose; the Mother Goose then talks to the ticket printer over **serial (RS-232)** — two different protocols. Genadi explained this wiring to the group on Jul 9. [[raw/Flex-POS Mid-Iteration Sync.md]]
- There are **two older Mother Goose versions plus a new one** whose docs are not yet on RKS's website. The new board is **FTP-upload based** — it sends the ticket data as a file to an FTP server (no serial interaction needed), which JVL would pull from. It costs **$466, one board per location (not per machine)** and would require replacing the existing board in the field. [[raw/Flex-POS Mid-Iteration Sync.md]]
- Printers seen in RKS documentation: a **Citizen 33541** for all their documentation, and an **Epson** model. Jim confirmed the print signals are **all ASCII** (tab spaces, characters, line breaks), so printer type shouldn't affect JVL's interception. [[raw/Flex-POS Mid-Iteration Sync.md]] [[raw/Flex-POS Iteration Planning 2025-07-14.md]]

## Relationship & posture (Jul 2025)

- Jim was **receptive** to JVL and willing to help — he can share the ticket **"confidence number"** hash (a hash of the whole ticket data) and is writing more robust documentation on intercepting the print signal. Val's read: RKS built the FTP board defensively "because they're losing the market" ahead of the June-1-2026 legislation, not to sell JVL new hardware. [[raw/Flex-POS Mid-Iteration Sync.md]]
- JVL will **buy four sets** of Mother Goose + accessory parts directly from RKS (rather than sourcing free from masters, to save time), shipping to Toronto; **Felipe** coordinates. The team wants old and new Mother Goose versions plus assorted printers to test against. [[raw/Flex-POS Mid-Iteration Sync.md]]
- Val is skeptical the RS-485 protocol will ever be shared (RKS guards it so their board can't be replaced), so JVL focuses on the **RS-232 printer protocol** and is confident Evgeny/Yavorski can reverse-engineer the signals if needed. Nathan (not Pavel/Genadi) owns the Jim interaction — same time zone, "culturally more compatible." [[raw/Flex-POS Mid-Iteration Sync.md]]
- A second Mother Goose competitor, **Omega Games**, exists but is mainly for their own operations and is **less than 1% of the market** (Felipe has never seen one in use) — JVL will focus on RKS only. [[raw/Flex-POS Mid-Iteration Sync.md]]

## Sources

- [[raw/Flex-POS Mid-Iteration Sync.md]]
- [[raw/Flex-POS Iteration Planning 2025-07-14.md]]
