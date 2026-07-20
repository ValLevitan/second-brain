---
type: organization
title: RKS (Mother Goose board maker)
date: 2025-07-09
aliases: [RKS, RTS, Mother Goose, Mutha Goose, Mutagoose, Muda Goose, Mutable, Mutabus, Jim RKS, Escape POS printer, Janka Labs]
source-count: 3
---

# RKS (Mother Goose board maker)

RKS is the third-party maker of the **Mother Goose** board (transcribed variously "Muda Goose," "Mutagoose," "Mutabus," "Mutable"), the payout/print controller that sits at the end of the machine daisy-chain in Georgia COAM locations. JVL's Flex-POS strategy centres on capturing the Mother Goose ticket signal, so RKS is a recurring counterparty. JVL's contact there is **Jim**. Interaction sequence in July 2025: **Jul 7** first Jim call (FTP-board deep-dive; [[wiki/meetings/2025-07-07-rks-mother-goose-ftp-board.md]]) → **Jul 9** internal FTP-vs-serial debate → **Jul 14** Jim confirms the confidence-number hash. [[raw/JVL-RKS-Mutha-Goose-Printer-1.md]] [[raw/Flex-POS Mid-Iteration Sync.md]] [[raw/Flex-POS Iteration Planning 2025-07-14.md]]

## Jul 7 2025 — first Jim call (the FTP replacement board)

On the first direct call ([[wiki/people/juan-martinez.md|Juan Martinez]] + [[wiki/people/nathan-carver.md|Nathan Carver]] with Jim) Jim walked through RKS's new **FTP-upload Mother-Goose replacement board** and how the legacy protocols work. [[raw/JVL-RKS-Mutha-Goose-Printer-1.md]]

- **It is a drop-in replacement for the Mother Goose master controller** — RKS built it to the "exact same footprint of the old board," so an operator "can just buy the board and slap it in the old case"; the operator "doesn't see anything different." One per **location** (it replaces the master controller, not a per-machine device); the location "still has to have a Mother Goose system in there." Price **$466** (Jim first said "455… 466"). [[raw/JVL-RKS-Mutha-Goose-Printer-1.md]]
- **How RKS's live gift-card implementation works today.** On a gift-card collect the board prints a normal Mother Goose voucher marked "gift card voucher" carrying a **QR code**; the player scans the QR at a kiosk to get the gift card. The board sends the collect data to a **secured FTP site** as a file named **`<UUID>.GC`** ("GC" = gift code); the **QR code contains only that UUID — no value**. The file itself holds the location name/number, the collect value and "just the data that would be on a normal ticket," currently in **UTF-8 ASCII** — and "can be encrypted if it needs to be." As soon as a valid upload lands, Jim **deletes it from the local server** (no backups) — so **all the data lives in that one file; there is no other lookup table** to fall back to. [[raw/JVL-RKS-Mutha-Goose-Printer-1.md]]
- **The legacy RS-485 protocol.** A **fixed-packet-size** protocol that "grew like a monster" over **25 years** of add-ons (multi-packets for bookkeeping, single packets for collects/remote-crediting) — Jim likens maintaining backward compatibility to "the Intel problem." A **collect is a single packet carrying the amount**, so it is "pretty simple to grab." Jim has **documented** the protocol and will share it — so JVL can either use his docs or reverse-engineer it. The printer is just the output device (an **Escape-POS printer**); "everything that goes on the RS-485 is completely different than what gets massaged out of it." [[raw/JVL-RKS-Mutha-Goose-Printer-1.md]]
- **Machine interface: legacy pulse vs a newer USB board.** The old way to talk to a machine was via **hard meters / pulses**; RKS now offers a **USB interface** giving "instant collect and instant data," "fully galvanically isolated" — a protocol "almost the same as an **ID003** dollar-bill acceptor" (Val confirmed ID003 "is the one we use as well"). Manufacturers targeting the USB board include **Novomatic** and "3 or 4" others (plus "the guy in Columbus"); **Light & Wonder opted not to** and sticks with isolated pulse boards (which Jim recommends in Georgia because of lightning). One board can **emulate up to 8 seats** — used on 8-player fish tables so an operator needn't buy a board per station (**Janka Labs** used it this way). [[raw/JVL-RKS-Mutha-Goose-Printer-1.md]]
- **JVL's read (Juan + Nathan, post-call).** The secured-FTP route is "way better than serial wires being intercepted" — the only attack would be to physically extract the credentials off the board. But because the file today is plain-text, JVL wants to add its own **encryption / hash handshake and fraud detection** ("this file doesn't look authentic"). JVL must also track each **site's unique UID** and **flag** it if a swapped-out Mother Goose changes it (the master can replace a failed unit without telling JVL). The $466 cost "may fall on the master" as a requirement to install Flex-POS. Juan had already downloaded almost all of RKS's manuals (free, no password, off RKS's website) and **moved them to Confluence** to share with the team. Val wanted "4 Mother Goose environments" to test against. [[raw/JVL-RKS-Mutha-Goose-Printer-1.md]]

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

- [[raw/JVL-RKS-Mutha-Goose-Printer-1.md]]
- [[raw/Flex-POS Mid-Iteration Sync.md]]
- [[raw/Flex-POS Iteration Planning 2025-07-14.md]]
