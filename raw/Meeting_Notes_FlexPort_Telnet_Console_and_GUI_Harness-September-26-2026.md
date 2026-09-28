# Meeting Summary — Flex-Port development sync
**Date:** September 26, 2026, 9:36 AM – 9:45 AM Eastern
**Duration:** About 9 minutes
**Attendees:** Pavel Frolov (organizer, chair), Evgeniy Alekseev, Alexey Khamin, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026]]

## Summary

Held in Russian. Speech recognition is poor in places. Some words and names are unclear.

**What is in the PORT-9 branch.** Pavel repeated what the "PORT 9" work contains:
- **SAS support**, taken from the earlier SAS project.
- **AFT commands** for direct talk with SAS.
- **Part of the Wi-Fi module work (ESP32-C6).** It exists in some form now. The next pull requests, **PORT 51 and PORT 68**, will be committed into this branch too.
- The Wi-Fi module is flashed with an ESP firmware project (the name is not clear in the recording).

**WebSocket.** Evgeniy asked if they tried a WebSocket connection. Pavel said the WebSocket that is built into this Wi-Fi firmware was not tried. WebSocket is used on the **STM32**. The code is now unified for Ethernet and Wi-Fi: all packets are built the same way. Over Wi-Fi they go through the module's own commands. Over Ethernet they go directly. Evgeniy started to ask if Wi-Fi should be built into the WebSocket, then said "this is for later."

**Telnet debug console.** This branch has a **Telnet server** on the board. You can connect to the board by Telnet. It has many debug commands: SAS channel state, Wi-Fi, Ethernet, IP address, and switching between **SAS mode and "no SAS" mode**. Typing "help" lists all commands. The same console works over **UART** (the 3-pin connector), but with no pictures.

**Screenshot service and web page.** A separate port runs a service that takes **screenshots** of what the Flex-Port shows. There is a web page to see the Flex-Port screen and to emulate actions, for example **scan a ticket** or **set a Wi-Fi network**.

**GUI harness (how to run it).** Evgeniy wanted this page for himself. Pavel showed it in the project **tools** folder:
- **"GUI harness"** is a Python script. You give it the Flex-Port IP address.
- In the latest firmware, the **IP address shows on the screen**.
- The script starts a local web server. Default port is **8073** (open localhost:8073).
- It uses two channels: **Telnet on port 23**, and a second port (about 5000-something) that returns a raw image. The server converts it to PNG and puts it on the page.
- The picture refreshes on click, not all the time, because one picture takes about **half a second** to download.

**Simulator.** Pavel said the **simulator for firmware is not ready yet**. It will probably not be ready today or tomorrow.

**Automated tests.** **Alexey (Lesha) is writing automated tests for the Flex-Port**, including the link with the machine. The board has **hooks** that give access to its internal state. The tests use these hooks to check money state: **was money transferred or not, did it hang, error state**, and so on. Evgeniy said this is useful.

**New boards.** Evgeniy said **new boards arrived**: 2 new ones of 2 types, and 3 more (exact meaning unclear). He said they will test them. Pavel said he saw the photo.

Pavel closed: keep working in the same direction.

## Decisions Made

No formal decisions recorded.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexey Khamin | Continue writing automated Flex-Port tests that use the board hooks to check money transfer, hangs and error states | TBD | Normal | Work in progress |
| 2 | [Unassigned — needs clarification] | Commit pull requests PORT 51 and PORT 68 (Wi-Fi module work) into the PORT-9 branch | TBD | Normal | Pavel said "they will be committed here" |
| 3 | [Unassigned — needs clarification] | Finish the firmware simulator | TBD (probably not by September 27, 2026) | Normal | Pavel: not ready, probably not today or tomorrow |
| 4 | Evgeniy Alekseev | Test the new boards that arrived | TBD | Normal | "We will test them" — who exactly is not clear [Needs Val's confirmation] |

## Open Questions

- Should Wi-Fi use the WebSocket built into the Wi-Fi module firmware? Raised by Evgeniy Alekseev; he said "this is for later."
- The built-in WebSocket of the Wi-Fi firmware was not tested yet (Pavel).

## Dispatch Log

---
*Processed from Teams transcript on September 28, 2026 (meeting-watcher recovery sweep)*
*Source meeting: Flex-Port development sync*
