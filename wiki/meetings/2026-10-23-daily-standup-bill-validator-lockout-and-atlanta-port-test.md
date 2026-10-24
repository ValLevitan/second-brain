---
type: meeting
title: Daily stand-up — in bill-validator mode the bill validator is blocked only when the host locks the port; the last day with the borrowed machines in Atlanta, so Biratka releases the Flex-Port and a Flex IQ RC build is made; an Intralot email on Georgia checksums; remote port update is MVP 2 and capability 146 is split; the Flex-Port update shrinks to 14 MB (Oct 23 2026, 4:49–5:37 AM)
date: 2026-10-23
aliases: [Daily Standup meeting Oct 23 2026, Daily Standup Bill Validator Lockout and Atlanta Port Test, Oct 23 stand-up, BV lockout stand-up, Atlanta port test, Intralot checksum email, CAP-146 split, PORT-131, PORT-138]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — bill-validator lockout and the Atlanta port test (Oct 23 2026)

**Date/time:** October 23 2026 (a Friday), **4:49 – 5:37 AM Eastern**, about 48 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel. The previous stand-up is [[wiki/meetings/2026-10-22-daily-standup-flex-port-cashout-screens-and-native-engine.md|Oct 22]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]. Val was not present.

**Purpose.** Round-the-table status. Main threads: the bill-validator lockout rule, the last day with the borrowed machines, an Intralot email, remote port update, the engine work and RIS requirements [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-10-23-in-bill-validator-mode-the-bill-validator-is-blocked-only-when-the-host-locks-the-port-and-a-lost-connection-shows-out-of-service-with-cash-in-still-open.md]] — the new lockout rule; Biratka's BV messages (PORT-162/163/164).
- [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]] (Oct-23 update) — the last day with the borrowed machines in Atlanta; Flex-Port release and Flex IQ RC build; the Oct-22 contradiction not settled.
- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-23 update) — Tsymanov's delivery work in three parts; the port pulls; MVP 2; capability 146 split; the 14 MB update.
- [[wiki/organizations/intralot.md]] (Oct 23) — the Georgia checksum email.
- [[wiki/decisions/2026-10-21-nova-drops-the-browser-for-a-native-engine-no-code-before-capabilities-and-mvp1-is-a-stable-nova-releasing-six-texas-games.md]] (Oct-23 note) and [[wiki/decisions/2026-10-14-no-freeze-inside-a-game-so-a-games-videos-are-decoded-when-the-game-is-entered.md]] (Oct-23 note) — Daniil's game-entry timings and his next tasks.
- [[wiki/decisions/2026-10-21-vladimir-samusenko-is-invited-as-nova-product-owner-and-capabilities-are-drafted-one-file-per-person-before-grooming.md]] (Oct-23 note) — where the requirement files go.
- [[wiki/decisions/2026-10-18-evgeny-kharetski-owns-a-voice-ai-game-design-assistant-with-a-first-pass-reviewed-oct-25.md]] (Oct-23 note) — the game agent by Saturday.
- [[wiki/decisions/2026-10-20-the-ris-improvements-release-notes-are-settled-point-by-point-and-the-tasks-are-to-be-rewritten-to-match-them.md]] (Oct-23 note) — RIS requirements rewritten; Felipe quiet.
- People: [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/sergey-tsymanov.md]] · in absentia: [[wiki/people/sebastian.md]] · [[wiki/people/andrei-klimovich.md]] (by inference) · [[wiki/people/evgeniy-alekseev.md]] · [[wiki/people/eugine-yavorski.md]] (by inference) · [[wiki/people/felipe-miranda.md]]

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "October-23-2026" and "2026-10-23" found no page citing either file and no stub for this session.
- **§4 name calls.** "Саша" = Biratka. "Лёша" / "Алексей" = Khamin; "Алексеев" = Evgeniy Alekseev (surname spoken). The "felipe" who "будет дальше заниматься прошивкой непосредственно этого файла" on the port side is read as Alekseev, as the notes do (**inference**; Felipe Miranda does no firmware). "Антон" asking where to put requirements = Leshkevich (speaker); "Антон" on the printer-in-emulator question is not identified. "Женя" = Kharetski (speaker label, LGS context). "Ваня" = Ivan. "Сергей" = Tsymanov. "Дима" who built the old Flex Pay transfer protocol is not identified (on Oct 20–22 the away "дима" was read as Chudinov — **inference** only). "евроски", who said his side was nearly ready, fits [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] (FlexPort/FlexPay integration software, §4 — **inference** by sound and role). "Андрей" to be asked about the lockout and to be on site, and who asked Seregin to rename "kiosk" to "terminal", fits [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (**inference**); the "Андрей" running the LGS autotests with Kharetski for two weeks is **not identified**. "Филипп" = [[wiki/people/felipe-miranda.md|Felipe Miranda]] (RIS requirements). "Себастьян" = [[wiki/people/sebastian.md|Sebastian]]. "Владимир", who found the modem cases, is not resolved.
- **Garbles kept as heard.** "35 608" — a ticket, **unclear**; "fort 138" — PORT-138 (the notes, heard); "порт 13" / "порт 131" — PORT-131 (the notes, heard); "кап 146" = capability 146; "ковер фортуна" — read as Clover Fortune (**inference**); "колле" — read as Calle Ocho (**inference**); "Ad jobell games" / "энджи нова" — the NOVA project's repository name, **unclear**; "х в эксцесс" / "хосс" — old hardware-access code (the notes: heard); "вкладки Титов" — **unclear**; "15/21" — **unclear**; "сигнича farleys", "СМИ проект" — **unclear**.
- **Skipped as logistics or chatter.** Greetings; the Sunday 3:00 meeting time.
- **§15.8:** clear. **§15 #9:** clear; the numbers are Jira keys.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]
