---
type: topic
title: FlexPay mobile app and service advocates
date: 2026-07-12
aliases: [FlexPay mobile app, service advocate, service advocates, whale, whale UI, Incom]
source-count: 4
---

# FlexPay mobile app and service advocates

A JVL discussion (Jan 13 2025) about a planned FlexPay mobile app and a new user type — the "service advocate" — that the app should serve. The call was framed as building a persona profile so the product can target this role.

## What a service advocate is

- A service company (or an employee of one) hired to look after a master's machines across all brands: solve technical issues, source parts from manufacturers, and pass locations' needs and wants back to the master. [[raw/mobile_app_advocate_persona_profile_january_13_2025.md]]
- They don't make final purchase decisions, but they strongly influence what a master buys — advising what's "hot," what locations request, and which machines cause trouble. They can champion a machine or damage it (e.g. complaining about too many service calls or poor support from a manufacturer). [[raw/mobile_app_advocate_persona_profile_january_13_2025.md]]
- "What's hot" comes from what they hear at locations (e.g. "that machine is always full"), not from GFC reports. [[raw/mobile_app_advocate_persona_profile_january_13_2025.md]]

## Reporting and money flow

- Chain: a master hires a service company; the service company employs the advocates/techs who go to locations. Advocates report to the master via their operations manager. [[raw/mobile_app_advocate_persona_profile_january_13_2025.md]]
- Advocates generally do **not** buy parts under their own name or handle invoicing — JVL invoices the master directly. A rare exception: a company with its own LLC can be invoiced directly (e.g. "Diamond Services"), maybe one or two at most. There is no markup by advocates. [[raw/mobile_app_advocate_persona_profile_january_13_2025.md]]
- Example used in the call: "I got an invoice from Felipe for a CPU for $400" — [[wiki/people/felipe-miranda.md|Felipe Miranda]] is named on the JVL side that issues a parts invoice. The point was whether a service advocate could mark that up when charging the master (answer: no — advocates don't handle invoicing). Felipe's exact role/last name is not stated. [[raw/mobile_app_advocate_persona_profile_january_13_2025.md]]

## Product significance

- Service advocates were judged as important, or even more important, than masters for upselling the FlexPay mobile app and cross-selling generally. So the app is being designed with the service-advocate persona as a target user. [[raw/mobile_app_advocate_persona_profile_january_13_2025.md]]
- The speaker will draft/update the mobile document to include the service-advocate role and update "whale" (a new-user-profile tool or app, name unclear) with this persona. [[raw/mobile_app_advocate_persona_profile_january_13_2025.md]]
- No urgency: nobody will need a mobile app for a year or more; the work is subcontracted (no salaries), so JVL will move at a comfortable pace. South Dakota and Puerto Rico are the stated priorities instead. [[raw/mobile_app_advocate_persona_profile_january_13_2025.md]]

Unclear: "whale" (appears as "whale"/"wial") — a tool or profile system JVL uses; and whether the "Igor" it was "too early" to involve on the UI is the same Igor who handles Puerto Rico setup. Flagged.

## Note: FlexPay the payment product vs. the mobile app

The **FlexPay** payment product itself is confirmed progressing — the Jan 24 2025 call put the related **FlexPort** device's beta ~3 weeks out and described FlexPay validating tickets. That hardware is documented in [[wiki/topics/jvl-machine-lineup.md]]. However, the **mobile app** and the **service-advocate persona** that this page is about remain **single-source** (Jan 13) and stay FLAGGED until a second source confirms them. [[raw/flex_port_hardware_up-jan-24-2025.md]]

- **FlexPort ↔ FlexPay integration progressing (Feb 11):** the Feb 11 embedded standup advanced the FlexPort-module-to-FlexPay-kiosk connection (WebSocket, device registration before accepting money, PIN/ticket validation), with the payment processor **Incom** supplying the test server and a production contract awaiting Val's signature; **Felipe** ("Filippo") to host a multi-machine production test in his office. Details on [[wiki/topics/jvl-machine-lineup.md]] and [[wiki/meetings/2025-02-11-embedded-group-flexport-flexpay.md]]. This is the payment product/hardware, still not the mobile app. (Whether "Felipe"/"Filippo" is the same Felipe who issues JVL parts invoices is unclear — see Owner Decisions.) [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]

- **Embedded group progress (Feb 18):** the FlexPort↔FlexPay integration is being brought up on a real machine by [[wiki/people/evgeny.md|Evgeny]] ("Zhenya") for the first field locations. A "Dima" (software; not attributed — see Owner Decisions) is delivering a new FlexPay build that **bypasses the card dispenser**, and adding **server-side log hooks** so an internet-connected FlexPay's logs can be pulled directly for fast feedback. A gap was found: the protocol has **no command for FlexPort to signal it is in an error state** to FlexPay — to be added. The FlexPay **activation sequence** was documented: (0) switch the factory QR scanner from Serial/HID to CDC mode; (1) **registration** (scan a QR in setup → bind the device serial number in JVL's device-management system); (2) create a **license** on the server ("Лиза"/"license") and apply it via a QR round-trip (FlexPay need not be online); then fill the **Incom** card-provider fields (manually or via a QR). Val has an **Incom** contract in its final stage and must arrange a production-server test (the test environment worked; production couldn't connect). Timeline: at least another week; Val pushed for a two-week (~March 5) buffer. See [[wiki/meetings/2025-02-18-embedded-group-flexport-flexpay.md]] and [[wiki/topics/jvl-machine-lineup.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]

## Sources

- [[raw/mobile_app_advocate_persona_profile_january_13_2025.md]]
- [[raw/flex_port_hardware_up-jan-24-2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
