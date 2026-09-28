---
type: meeting
title: Flex-Port development sync — what the PORT 9 branch holds, a Telnet debug console, and the GUI harness (Sept 26 2026, 9:36 AM)
date: 2026-09-26
aliases: [Flex-Port development sync, FlexPort Telnet Console and GUI Harness, Sept 26 Flex-Port sync, PORT 9 branch, GUI harness, гуй харнес, Telnet console on Flex-Port]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Flex-Port development sync — the PORT 9 branch, a Telnet console, and the GUI harness (Sept 26 2026)

**Date/time:** Saturday September 26 2026, **9:36 – 9:45 AM Eastern** (about 9 minutes), from the `**Date:**` header [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]. Teams title *Flex-Port development sync*. **Language: Russian.**

**Attendees** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (ran it), [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/irina-shishko.md|Irina Shishko]] (brief acknowledgements only) [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]].

**Purpose:** Pavel walked the group through what the Flex-Port "порт 9" branch now contains and the debug tools on the board, and how to run the GUI harness page [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]].

## Where the substance lives

- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 26) — the branch contents, the Telnet console, the screenshot service and the GUI harness, the new boards.
- [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]] (Sept-26 update) — part of the ESP32-C6 Wi-Fi work is in the branch; the module's built-in WebSocket not tried.
- [[wiki/decisions/2026-09-14-flex-port-sas-mode-is-a-selection-capability-not-a-long-lived-branch.md]] (Sept-26 update) — a console command switches SAS / no-SAS mode.
- [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-26 update) — the firmware simulator is not ready.
- [[wiki/topics/test-automation-strategy.md]] (Sept 26) — Khamin's Flex-Port autotests through the board's hooks.
- People: [[wiki/people/pavel.md]], [[wiki/people/evgeniy-alekseev.md]], [[wiki/people/alexei-khamin.md]].

## Notes on the sources

- **§12 — a new meeting.** No page cited either file; grepped the wiki for "September-26-2026", "Telnet", "GUI harness"/"гуй харнес", "PORT 9", "8073" and "Flex-Port development sync". No other Sept-26 stub exists. One stub, two sources (notes + transcript).
- **Notes vs transcript — the wiki follows the transcript:**
  - The notes say the Wi-Fi firmware's name "is not clear". The transcript has "Прошивка эти команс. Есп есп отеля да проекты". "эти команс" is read as **AT commands** (inference), the same reading the Sept-7 notes gave; the project name stays unclear. [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]] [[raw/Meeting_Notes_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]
  - The notes leave out a short garbled line from Pavel ("Вы, значит, свое продолжается сса? Флэш памятью") just before the simulator remark; its meaning is unclear and nothing is recorded from it. [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]] [[raw/Meeting_Notes_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]
  - The notes say Khamin's tests include "the link with the machine". In the transcript Pavel says "Связь с flexpen, правильно?" and Khamin answers "Ну и с машиной, да?" — "flexpen" is unclear. [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]] [[raw/Meeting_Notes_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]
  - The notes' new-board count ("2 new ones of 2 types, and 3 more") matches the transcript's garbled "2 этот новых да 2 типа ещё 3 дороги"; the wiki records no count. [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]] [[raw/Meeting_Notes_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]
  - The notes assign "test the new boards" to Alekseev; the transcript's "поиспитываем" is "we'll test", subject not stated. [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]] [[raw/Meeting_Notes_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]
- **§4 names.** "Лёша" = [[wiki/people/alexei-khamin.md|Khamin]] (he answers). Alekseev is the speaker label; the Zhenya-cluster call is not needed. Irina = [[wiki/people/irina-shishko.md|Irina Shishko]] (speaker label). [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]
- **§15.8:** clear. **§15 #9:** none — the numbers are network ports on a test board (23, 8073, "5000-something"), not corporate identifiers.

## Sources

- [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]
- [[raw/Meeting_Notes_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]
