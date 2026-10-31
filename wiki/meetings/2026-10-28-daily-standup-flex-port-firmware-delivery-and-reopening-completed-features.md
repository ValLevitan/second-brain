---
type: meeting
title: Daily stand-up — Tsymanov takes the firmware-transfer protocol to the Flex-Port (the port writes to flash, checks the checksum and switches boot sector); a story under a Completed feature does not reopen it automatically; game video should be VP9, not VP8; Biratka absent with the port work unfinished; Yavorski on HFM-692 again (Oct 28 2026, 4:50–5:28 AM)
date: 2026-10-28
aliases: [Daily Standup meeting Oct 28 2026, Daily Standup Flex-Port Firmware Delivery and Reopening Completed Features, Oct 28 stand-up, firmware transfer to the Flex-Port, reopening completed features, VP9 not VP8, HFM-692]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — Flex-Port firmware delivery and reopening completed features (Oct 28 2026)

**Date/time:** October 28 2026 (a Wednesday), **4:50 – 5:28 AM Eastern**, about 37 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]. The stand-up was moved to 12:00 (Minsk time, per the notes) and began about 14 minutes into the recording. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel. The previous stand-up is [[wiki/meetings/2026-10-27-daily-standup-cashout-merging-and-remote-updates.md|Oct 27]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]. [[wiki/people/alexander-biratka.md|Alexander Biratka]] was absent. Val was not present.

**Purpose.** Round-the-table status, then two process questions from Kovalchuk [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-28 update) — the Flex IQ firmware arrives and its signature is checked; Tsymanov takes the transfer protocol to the Flex-Port; the port's flash-checksum-switch step.
- [[wiki/decisions/2026-10-28-a-story-under-a-completed-feature-does-not-reopen-it-automatically-and-the-storys-creator-moves-the-feature-or-picks-another-parent.md]] — Pavel's ruling on stories under Completed features; the Core Technology projects; a draft closed as a duplicate.
- [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]] (Oct-28 update) — the automatic reopen is dropped.
- [[wiki/decisions/2026-10-27-flex-port-counts-meter-pulses-from-30-to-150-ms-and-a-repeat-cash-out-inside-the-timeout-joins-the-pending-one.md]] (Oct-28 update) — does the multi cash-out add up to one ticket on SAS.
- [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]] (Oct-28 update) — Biratka absent with the port work unfinished; Andrei's list of findings.
- [[wiki/decisions/2026-10-21-nova-drops-the-browser-for-a-native-engine-no-code-before-capabilities-and-mvp1-is-a-stable-nova-releasing-six-texas-games.md]] (Oct-28 note) — VP9, not VP8; formats from Miranda are fine for now.
- [[wiki/projects/nebraska-skill-market.md]] (Oct 28) — Sparkle Seven ported; Igor rebuilds with the new maths.
- [[wiki/people/eugine-yavorski.md]] (Oct 28, in absentia) — HFM-692 and the reviewer list.
- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 28) — the installer that keeps old RIS data.
- [[wiki/topics/test-automation-strategy.md]] (Oct 28) — the modem retest is green; the cloud terminal hub question.
- People: [[wiki/people/pavel.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/igor-metelski.md]] · [[wiki/people/ivan.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/evgeny-kharetski.md]] · in absentia: [[wiki/people/alexander-biratka.md]] · [[wiki/people/evgeniy-alekseev.md]] · [[wiki/people/eugine-yavorski.md]]

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "October-28-2026" and "2026-10-28" found no page citing either file and no stub for this session.
- **§4 name calls.** "Саша" = Biratka (absent). "Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (surname spoken; port-side firmware). "яворский" / "егорский" = [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] (surname spoken; "Egorsky" is a registered alias). "Женя" = Kharetski (speaker). "Ира" = Irina. "Сергей" = Tsymanov. "Дима" who returns the next day is not identified (Kovalchuk was present). The "Дима" who could remove Yavorski from the reviewers is not identified; Kovalchuk fits the GitHub-admin role (**inference** only). The "Андрей" given the production update by Tsymanov fits [[wiki/people/andrey-bosik.md|Andrey Bosik]] (DevOps — **inference**). The "Андрей" whose evening list of findings Irina must go through, and who updated the requirements in HFM-692, fits [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (**inference**). "каймове", who really owns one IQ text task, is **unclear** (notes: "Kaimov", heard) — not resolved to anyone.
- **Garbles kept as heard.** "х ф м 692" = HFM-692 (heard); "кортехнолоджи и бэп" — Core Technology and "BEP" (the notes: heard); "7 нас переехал тоже на день" — **unclear**; "UP форматы из миранды" — formats from Miranda (the notes' reading); "в п 9" / "в п 8" = VP9 / VP8; "н с 6", "н ф л один" — NC6 and NFL1 (heard); "IP 1113" — a board report (heard); "Пиемом" — read as "by the PM agent" (**inference**); "капбили" — read as capabilities (**inference**; notes: "cap bill", heard); "queflex pay" — **unclear**; "43 53" — build 4353 (heard); "224" — a server (heard); "рейч продуктов" — **unclear**; "тг собирается" — **unclear**.
- **Skipped as logistics or chatter.** The move to 12:00; headset and sound checks; who is away.
- **§15.8:** clear. **§15 #9:** clear; the numbers are Jira keys, a build number and a server number.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]
