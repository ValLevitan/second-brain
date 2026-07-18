---
type: decision
title: FlexPay to support TITO at non-JVL locations via a FlexPort-hosted SAS server
date: 2025-03-28
aliases: [FlexPay TITO decision, TITO support, SAS server on FlexPay, FlexServer, non-JVL location TITO]
source-count: 4
status: active
---

# FlexPay to support TITO at non-JVL locations via a FlexPort-hosted SAS server

On the Mar 28 2025 scope-gap meeting, JVL agreed the business requirement and an MVP technical approach for **FlexPay to issue and validate TITO (ticket-in/ticket-out) tickets** at locations that contain **no JVL machines**. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

> **Refined Apr 7 2025 (evolution, still active):** the "FlexPort simplified into a SMIB" device concept split into **two products** — a screenless **FlexSMIB** board for modern dual-SAS machines and the screened **FlexPort** for legacy machines (which can't display errors to the player). The SAS-server/WSS-proxy approach here stands. See [[wiki/decisions/2025-04-07-flexsmib-modern-flexport-legacy.md]]. [[raw/flex_pay_tito_smib_port-april7-2025.md]]

## The business requirement and use case

- **Requirement (Val):** FlexPay must be able to **issue and validate TITO tickets** — not just JVL's own kiosk tickets. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- **Driving use case:** a location of **five gaming machines, none of them JVL machines**, where the operator installs FlexPay and runs on the TITO principle. A player inserts (e.g.) $20 into a machine's **bill acceptor**, plays, and prints a TITO ticket; carries it to a second machine and inserts it; before accepting it, that machine must check with a **local server** whether the ticket may be taken. A local (or centralized) server decides which ticket number to issue and holds the ticket's value. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- **How TITO validation differs from JVL's current tickets:** the machine's validator reads only the **ticket number** and asks the server for the amount — the validator itself does not know the sum. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## The hardware problem (why it isn't trivial)

- To speak SAS to a **non-JVL machine**, the setup needs SAS on the machine side. The cheapest option floated by Pavel was an **Ethernet-to-RS232 adapter** (under $10 each) in every machine, wired via Cat5/Cat6 into the FlexPay network, implementing SAS over Ethernet. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- **Blocker:** SAS requires **9-bit** serial operation, and virtually all cheap adapters only do **8-bit**; 9-bit-capable devices are very rare ("they go straight in the trash"). Pavel's own tested adapter did 8-bit easily but not 9-bit. Raspberry Pi / Banana Pi + TTL-to-RS232 adapters were rejected as unreliable in an industrial environment. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- A kiosk also physically can't host enough COM ports (one or two, vs many needed); network ports scale, COM ports don't — reinforcing a network-based design. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## The MVP approach chosen

- **First stage:** use the existing **FlexPort** device mounted **inside** each machine (not externally): connect FlexPort to the machine's **SAS port on the CPU** on one side, and a **CAT6** cable to a **router** on the other; the router connects to **FlexPay**. Effectively FlexPort is simplified into a **SMIB (Slot Machine Interface Board)**. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- Implement a **"Flex SAS server"** application (a software proxy) that talks SAS to the machine and the existing **WSS protocol** to FlexPay, converting **SAS ↔ VCC/WSS**. The application (called **"FlexServer"**) is **split** — part added to FlexPort, part to FlexPay. It registers machines, validates TITO tickets, and generates TITO ticket numbers. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- The current WSS protocol between FlexPay and the port needs **at least one new command** — to register/issue a new ticket; registration and validation stay largely the same. More commands (e.g. per-machine statistics) will be added in later releases. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## Effort (complexity, not calendar promises)

- Pavel estimated the proxy/SAS-server base at **~2–3 weeks**, slightly more than the in-machine "linear" variant because of the Ethernet comms; a base app is achievable in **~1.5–2 sprints**, reusing JVL's existing **SAS test-tool** functionality. Eugine estimated the WSS-protocol implementation at **~2 weeks** after reading the protocol over the weekend (to report Monday). [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## Legal / money-handling constraints (recorded, not new)

- **Only winnings** ("выигрыш") may be converted to a card — **not** "Money In" (money inserted but not played). On a TITO ticket, **all money that has passed through the machine becomes redeemable/cashable**. When a ticket carries both playable and winning money, the system must eat the ticket, allow withdrawing the withdrawable portion, and print a new ticket for the remainder. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- **Ticket security:** a barcode alone is insufficient (it can be copied); full validation happens at the **bill validator**. The existing **PIN-code** system for self-created kiosk tickets stays. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## Open commitments

- [ ] Eugine Yavorski — read the WSS protocol over the weekend and report Monday how long the implementation will take, then implement it — due Monday (report) — [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- [ ] Dima Chudinov — send Eugine the list of SAS commands to implement first (the minimal set to make TITO work) — due unspecified — [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- [ ] Pavel — send Eugine the IGT utility (a SAS-server emulator that pings SAS; the machine's green light confirms SAS works), and arrange a test machine setup so Eugine "isn't fumbling in the dark" — due unspecified — [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- [ ] Val — write the meeting summary + undertakings and schedule the follow-up for Tuesday 7:00 am Eastern — due after the meeting — [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- [ ] Minsk team — make as much progress as possible on Monday — due Monday — [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## History

- **The gap was discovered the day before (Mar 27), in an English meeting:** Val learned FlexPay cannot stand alone at a third-party-machine location (FlexPort has no SAS software; "we only have RS232 connector"), called it "a huge, huge scope gap," dictated the MVP ("FlexPay must support Tito operation in a location" — a local 24-hour-expiry validation database), rejected partnering with a third-party SMIB provider (EasyLink), and named **Evgeniy Alekseev + Evgeniy Yavorsky, "nobody else"** for the make-do mini-server. The SMIB/"REV-B FlexPort" idea formalized here originated there. See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]] and [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- The core design was **prefigured in a ~2024 architecture meeting**: Pavel presented the same two options (third-party SAS host vs. a JVL-proprietary SAS host in/beside the kiosk, preferred as cheaper for the operator), the WSS link to FlexPay, and the **9-bit serial** converter blocker ("we need to use 9 bits operation… quite different"), with converters to be bought and tested. See [[wiki/topics/olap-power-bi-architecture.md]] and [[wiki/meetings/2024-sql-olap-visualization-architecture-2.md]]. [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]]

## Open questions

- Whether a reliable **9-bit Ethernet-to-RS232 adapter** can be sourced (which would cheapen the hardware) — otherwise a local TITO server must be built on the kiosk or a chosen board regardless. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- Who sets up Eugine's test machine and identifies which RS-232 port it uses — Pavel to instruct remotely; **"Ira"** ([[wiki/people/irina-makarych.md|Irina Makarych]] — Shishko or Makarych unclear from source; per 2026-07-18 roles) or **"Vlad"** (unclear) to help. Flagged. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## Sources

- [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]]
- [[raw/flex_pay_tito_smib_port-april7-2025.md]]
