---
type: meeting
title: Daily stand-up — the kiosk cannot yet switch a Flex-Port between SAS and bill-validator mode, and the port-side command is built now without waiting for Alekseev; Pavel's SAS CRC fix makes the port stable on IGT and Banilla; the settings QR needs one design for Flex-Port, Flex Pay and Flex IQ; the no-SAS mode needs capabilities and tests (Oct 21 2026, 4:46–5:15 AM)
date: 2026-10-21
aliases: [Daily Standup meeting Oct 21 2026, Daily Standup Flex-Port Mode Switch and SAS CRC Fix, Oct 21 stand-up, Flex-Port mode switch stand-up, SAS CRC fix, FP-1364, NGCO-1, PNC-4]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — Flex-Port mode switch and SAS CRC fix (Oct 21 2026)

**Date/time:** October 21 2026 (a Wednesday), **4:46 – 5:15 AM Eastern**, about 28 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel. The previous stand-up is [[wiki/meetings/2026-10-20-daily-standup-io-board-firmware-via-github-and-vp9-video-decode.md|Oct 20]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]. Val was not present.

**Purpose.** Round-the-table status. The main threads: the Flex-Port mode switch from the kiosk, Pavel's SAS fix and the statistics read from another maker's machine, the settings QR across all devices, and the no-SAS mode's missing capabilities [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]] (Oct-21 update) — the kiosk-to-port mode command is missing and is built now; the mode is kept in EEPROM; the SAS CRC fix; the Banilla statistics; the no-SAS mode needs capabilities, requirements and tests.
- [[wiki/decisions/2026-10-01-sas-or-no-sas-is-set-per-flex-port-on-the-flex-iq-set-up-screen-and-sent-at-registration-with-the-pin-code.md]] (Oct-21 update) — the switch exists on the Flex IQ, but the port does not act on it.
- [[wiki/decisions/2026-09-07-wi-fi-provisioning-by-encrypted-qr.md]] (Oct-21 update) — Seregin's spike; the Flex Pay QR is temporary; one design across Flex-Port, Flex Pay and Flex IQ.
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 21) — Biratka's Flex Pay vs Flex IQ analysis and 8–10 tasks; the Flex Pay built with its screen upside down.
- [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-21 update) — the agent's comparison task that did not reach Jira; Pavel's story under the AI Draft.
- [[wiki/topics/test-automation-strategy.md]] (Oct 21) — tests moving to hardware through CI; the new integration repository has one reviewer; Irina's port, machine and bill-validator tests.
- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 21) — Irina rewrites the RIS requirements; Ivan checks Kharetski's and Tsymanov's work; Tsymanov's passport and software-update roles.
- [[wiki/topics/nova-platform-architecture.md]] (Oct 21) — Leshkevich on Nebraska 2 and RAM; Daniil's two games on one board.
- Also: [[wiki/decisions/2026-10-20-flex-port-mvp1-needs-only-an-easy-release-build-and-the-usb-update-and-alekseev-writes-stm32-freertos-rules-for-claude-review.md]] (Oct-21 note), [[wiki/decisions/2026-10-20-the-ris-improvements-release-notes-are-settled-point-by-point-and-the-tasks-are-to-be-rewritten-to-match-them.md]] (Oct-21 note), [[wiki/decisions/2026-10-05-epic-950-is-the-terminal-printer-tested-first-and-all-models-stay-supported.md]] (Oct-21 note).
- People: [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/evgeniy-alekseev.md]] (in absentia) · [[wiki/people/andrei-klimovich.md]] (in absentia, by inference)

- **Follow-up:** the "8:00 meeting" Leshkevich named is the Dutch Mill review at 8:02 AM the same day, where he showed his RAM results — [[wiki/meetings/2026-10-21-dutch-mill-on-nova-and-native-engine.md]].

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "October-21-2026" and "2026-10-21" found no page citing either file and no stub for this session.
- **§4 name calls.** "Саша" = Biratka (he answers). "Лёша" / "Алексей" = Khamin; "Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (surname spoken). The first "Антон" (Nebraska 2, memory) = Leshkevich; the second (FP-1364) = Seregin, by speaker label. "Даниил" / "Данил" = Daniil Stauskiy. "Женя" = Kharetski (speaker label). "Иван" = Ivan. "Ира" = Irina. "Сергей" = Tsymanov. "Дима" who speaks = Kovalchuk (label). The "Андрей" who showed the upside-down Flex Pay and whose team is at the trade show, and the "Андрей" who raised third-party statistics as a market need, fit [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (away at a trade show Wednesday–Thursday per the Oct-20 call) — **inference**. The "Андрей" whom Kharetski will ask to change the repository review rules is not named in full — [[wiki/people/andrey-bosik.md|Andrey Bosik]] fits by role (**inference**, queued). The "Игорь" proposed as reviewer is not named in full — [[wiki/people/igor-metelski.md|Igor Metelski]] fits by role (**inference**, queued). The "дима" Pavel names among those who wrote the port's SAS commands is **not identified**.
- **Garbles kept as heard.** "флекс pays fex IQ" = Flex Pay and Flex IQ; "Дело таско фич" — tasks/features, **unclear**; "побилите" / "копопили" / "capelity" = capability; "рекламенты" / "реклайменты" = requirements; "по тире сета" = rulesets (**inference**); "Финклям пи 13 64" = the spike FP-1364 (the notes: "heard"); "PRPNC 4 и н джи ц о один" = PRs for PNC-4 and NGCO-1 (the notes: "heard"); "2 игру фортун" — a second game, "Fortune", **unclear** which; "жить р тайп" — the SAS command type, **unclear**; "cr c" / "ц р ц" = CRC; "аристократии" = Aristocrat; "ig t" = IGT; "banila" / "банилой" = Banilla (the notes read it as Bally); "эффекторе ресет" = factory reset; "nos" / "no sas" = the no-SAS (bill-validator) mode; "айдрафт один" = an AI Draft (cf. the Oct-20 stub); "Агент уже 70. Мозги прикручевы" — Kharetski on his agents, **unclear**.
- **Where the notes and the transcript differ.** The notes write "Bally (heard 'banila')"; the wiki keeps Banilla, as on the Oct-16 and Oct-20 pages. The notes say Daniil runs "two games (Fortune)"; the transcript says he connected "2 игру фортун" — kept vague. The notes put "Andrei's team" on the upside-down Flex Pay; the transcript says Andrei showed it and "они" assembled it.
- **Skipped as logistics or chatter.** Who was late, the clock jokes, greetings and goodbyes.
- **§15.8:** clear. Nobody's pay or rate appears. **§15 #9:** clear; the numbers are Jira keys and an epic number.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
