---
type: meeting
title: Daily stand-up — in bill-validator mode the Flex-Port takes money in but its cash-out screens misbehave, and the fixes go to Biratka; the borrowed machines leave after Friday and Elizabeth needs the latest build and the BV setting; the games target the RK3576 and two games already run on one board; Seregin's four registration scenarios lead to an architecture first; Tsymanov takes the port-update research while "Dima" is away (Oct 22 2026, 4:45–5:19 AM)
date: 2026-10-22
aliases: [Daily Standup meeting Oct 22 2026, Daily Standup Flex-Port Cashout Screens and Native Engine, Oct 22 stand-up, cash-out screens stand-up, out of service message, requirement 1838, LGS-1040, LGS-1042]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — Flex-Port cash-out screens and the native engine (Oct 22 2026)

**Date/time:** October 22 2026 (a Thursday), **4:45 – 5:19 AM Eastern**, about 34 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel. The previous stand-up is [[wiki/meetings/2026-10-21-daily-standup-flex-port-mode-switch-and-sas-crc-fix.md|Oct 21]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]. Val was not present.

**Purpose.** Round-the-table status. The main threads: the Flex-Port cash-out faults in bill-validator mode, the last days of the borrowed machines, games on the new board and the native engine, the registration scenarios, and Jira clean-up [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]] (Oct-22 update) — the cash-out faults in bill-validator mode go to Biratka; the mode switch works (Khamin, Biratka) or not (Irina); Elizabeth, Sebastian and the last two days with the borrowed machines; Pavel's SAS-command artifacts.
- [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]] (Oct-22 update) — three boards, the RK3576 chosen; Genadi to send boards; Daniil's memory estimate.
- [[wiki/topics/nova-platform-architecture.md]] (Oct 22) — Daniil's two games on one board and the decoders that hold memory.
- [[wiki/decisions/2026-10-21-nova-drops-the-browser-for-a-native-engine-no-code-before-capabilities-and-mvp1-is-a-stable-nova-releasing-six-texas-games.md]] (Oct-22 note) — Pavel restates the native engine to the team; Leshkevich's variant is slow.
- [[wiki/decisions/2026-09-07-wi-fi-provisioning-by-encrypted-qr.md]] (Oct-22 update) — Seregin's four registration scenarios; architecture first, then capabilities.
- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-22 update) — Tsymanov takes the port-update research now.
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 22) — Biratka's Flex IQ / Flex Pay tasks; the rotated-screen build was sent.
- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 22) — requirement 1838 for printers is final after Felipe; Ivan on RIS; Tsymanov's passport and update-authorization work.
- [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-22 update) — the stand-up is written for the AI PM; overdue tasks; LGS-1040 and LGS-1042 unlinked.
- [[wiki/decisions/2026-10-18-evgeny-kharetski-owns-a-voice-ai-game-design-assistant-with-a-first-pass-reviewed-oct-25.md]] (Oct-22 note) — Kharetski's agent takes images and maths files.
- Also: [[wiki/decisions/2026-10-20-the-ris-improvements-release-notes-are-settled-point-by-point-and-the-tasks-are-to-be-rewritten-to-match-them.md]] (Oct-22 note), [[wiki/decisions/2026-10-05-epic-950-is-the-terminal-printer-tested-first-and-all-models-stay-supported.md]] (Oct-22 note).
- People: [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/sergey-tsymanov.md]] · in absentia: [[wiki/people/elizabeth.md]] · [[wiki/people/sebastian.md]] · [[wiki/people/eugine-yavorski.md]] · [[wiki/people/genadi-peari.md]] · [[wiki/people/evgeniy-alekseev.md]] · [[wiki/people/vladimir-samusenko.md]] (by inference)

- **Follow-up:** Pavel set a meeting for 12:30 the same day and will send the invite (time zone not stated) [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]].

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "October-22-2026" and "2026-10-22" found no page citing either file and no stub for this session (the only other Oct-22 stub is the Felipe Miranda Echo call, a different meeting).
- **§4 name calls.** "Саша" = Biratka. "Лёша" / "Алексей" = Khamin; "Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (surname spoken). "Антон" (the variant that runs slow, the release notes) = Leshkevich; "Антон серегин" by name. "Даниил" = Daniil Stauskiy. "Женя" = Kharetski (speaker label; and the LGS tasks Pavel would give "на женю"). "Ира" = Irina. "Сергей" = Tsymanov. The "дима" who speaks is Kovalchuk (label); the "дима" who is away until Monday and owns the port-update work is **not the speaker** — read as Chudinov on the remote-update page (**inference**, as on Oct 20). "Яворский" / "ягурский" = [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] (FlexPort/FlexPay integration software, §4). "Гена" / "Геннадий" = [[wiki/people/genadi-peari.md|Genadi Peari]]. "Элизабет" = [[wiki/people/elizabeth.md|Elizabeth]]; "напишу у лиза" read as a note to her (the notes' reading). "Себастьян" = [[wiki/people/sebastian.md|Sebastian]]. The "Андрей" who asked Sebastian to check the pulses and who got the rotated-screen build fits [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (**inference**, as on Oct 21); the "Андрей" Biratka must ask about putting Flex Pay into the update is **not identified**. "Владимир", who moved the LGS set-up-screen tasks to Pavel, fits [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], who owns the set-up screens (**inference**). "Вал" = Val (in absentia).
- **Garbles kept as heard.** "проекте fort" — a Jira project, **unclear** which; "сяй запуск на железе" — the notes read SAS; read here as CI, as on Oct 21 (**inference**); "лиза" in Biratka's and Irina's lines = lease (**inference**, as the notes read it on Oct 6–8); "рекларс для genadingo" — the notes: release notes for Gennadiy (heard); "На нарасте" = in Rust (the notes: heard); "GT agent" — Kharetski's agent; "Антин миксавил с файлы мак" — the maths file format, **unclear**; "аутосервис" = "out of service"; "кэшин дизэйбл" = "cash-in disabled"; "14:00 назад" / "15:00 назад" — some time ago, **unclear** (the notes: two days); "гигабайт 100 висит" — the memory held by decoders, **unclear**; "Грация гейт энд пойнт из exxell bacon" — **unclear**; "тех пор 94" — **unclear**; "силу к 11" — **unclear**.
- **Where the notes and the transcript differ.** The notes say Khamin works on "SAS launch on hardware"; the wiki reads CI. The notes say Biratka's open item is "blocking the Flex-Port on a disconnect"; the transcript says "при отключении лиза" — on lease switch-off (**inference**). The notes list "LGS-1040 and LGS-1042" as heard; kept so.
- **Skipped as logistics or chatter.** Greetings, who can hear whom, goodbyes.
- **§15.8:** clear. Nobody's pay or rate appears; a board's relative price is equipment cost. **§15 #9:** clear; the numbers are Jira keys, requirement and task numbers.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]
