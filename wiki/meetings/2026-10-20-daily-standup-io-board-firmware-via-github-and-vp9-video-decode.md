---
type: meeting
title: Daily stand-up — IO board firmware is released from GitHub; MVP 1 still waits on the Flex-Port USB-stick update and remote update is MVP 2; Debian on every platform; VP8 videos may have no hardware decode on the board, so VP9 must be proven; the AI PM's late duplicate is kept to watch it (Oct 20 2026, 4:46–5:36 AM)
date: 2026-10-20
aliases: [Daily Standup meeting Oct 20 2026, Daily Standup IO Board Firmware via GitHub and VP9 Video Decode, Oct 20 stand-up, VP9 video decode stand-up, FP 1364, FP 13 604, CAP-243]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — IO board firmware via GitHub and VP9 video decode (Oct 20 2026)

**Date/time:** October 20 2026 (a Tuesday), **4:46 – 5:36 AM Eastern**, about 51 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]] [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel. The previous stand-up is [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct 19]]. The next is [[wiki/meetings/2026-10-21-daily-standup-flex-port-mode-switch-and-sas-crc-fix.md|Oct 21]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]. Val was not present. Pavel noted Vladimir is on vacation.

**Purpose.** Round-the-table status. The main threads: firmware release paths and the MVP 1 gate, the game-port conveyor and its video-decode risk, and the AI PM's handling of the settings-QR spike [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-20 update) — IO board firmware released on GitHub and pulled by the HAL build; our firmware is only for our boards; remote Flex-Port update is MVP 2 and MVP 1 waits on the USB-stick update; capabilities 137, 122, 146 marked MVP 2; the 2:00 PM Alekseev meeting.
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 20) — the Terminal Hub kiosk-spoofing fix; Flex Pay against Flex IQ; features from found gaps.
- [[wiki/topics/nova-platform-architecture.md]] (Oct 20) — Debian on every platform, kernels 6.18 (x86) and likely 6.12 (RK board); no system yet for the RK3576; the Dragon Pays stutter and VP8 vs VP9 hardware decode; Daniil's board.
- [[wiki/decisions/2026-10-18-rage-is-closed-dutch-mill-reaches-nova-by-wednesday-and-a-reskin-from-a-new-theme-tests-the-tools.md]] (Oct-20 update) — Dutch Mill ported in about six hours; the ports go "on a conveyor"; Leshkevich gets the Wednesday invite; who writes the port tests?
- [[wiki/decisions/2026-09-07-wi-fi-provisioning-by-encrypted-qr.md]] (Oct-20 update) and [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-20 update) — Seregin's spike, the AI PM's duplicate kept and moved to Tsymanov, Pavel's requirement spoken for the agent; CAP-142 still proposed.
- [[wiki/topics/test-automation-strategy.md]] (Oct 20) — Flex IQ SSH login in the CI secrets; Review → Completed → Closed; capability 243 split; the Terminal Hub test environment; the self-hosted runners.
- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 20) — the hardware-tracking checkbox and the passport; Tsymanov's permissions work; Kharetski's tasks to In Progress.
- People: [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/igor-metelski.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/evgeniy-alekseev.md]] (in absentia)

- **Follow-up:** the Wednesday meeting with Val ("завтра") took place on Oct 21 at 8:02 AM — [[wiki/meetings/2026-10-21-dutch-mill-on-nova-and-native-engine.md]].

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "October-20-2026", "2026-10-20" and "FP 1364" found no page citing either file and no stub for this session. The other Oct-20 raws (Flex-Port MVP 1 USB update; Pavel alignment; third-party EGM emulation) have different titles and content; the 2:00 PM meeting with Alekseev named here is not in this pair; it is most likely the [[wiki/meetings/2026-10-20-flex-port-mvp1-usb-update-and-build-standards.md|7:01 AM Eastern Flex-Port firmware meeting]] (2:00 PM in Minsk — **inference**), stubbed separately.
- **§4 name calls.** "Саша" = Biratka (he answers). "Алексей" = Khamin; "Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (surname spoken). The first "Антон" (games) = Leshkevich and "Антон серегин" = Seregin. "Даниил" = Daniil Stauskiy. "Женя" = Kharetski (speaker label). "Ваня"/"Иван" = Ivan. "Игорь" (Dutch Mill, Midnight Money) = Metelski by speaker label. "Ира" = Irina. "Сергей" = Tsymanov. "Владимир" on vacation = [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] — **inference**. The "Андрей" who connects app keys, keeps the runners and owes a test environment is not named in full — Andrey Bosik fits by context (**inference**, queued). The "Дима" who made a firmware-transfer API about five months ago and the "Дима" who changed Flex IQ protocols are not named in full — **not identified**. The "Дима" asked for repository access is Kovalchuk per the notes.
- **Garbles kept as heard.** "i ibarda" / "айлборт" = IO board; "хаус" / "хал" = HAL; "airbort gonder bort", "airbord caunter bord all e debord" = our boards (IO board, counter board and one more); "Кап." = capability; "FP 13 604" / "Эф пи 13 64" = the spike (the notes: FP-1364, heard); "aid драфт" = AI Draft; "пием" / "пима" = the AI PM; "Мерлин" — a joke or a name, **unclear**; "дебиан" / "дебилом" / "девиан" = Debian; "саквари" / "слоквари" = Slackware; "в п 8" / "в п 9" = VP8 / VP9; "дорганпейс" / "драгон пейс" = Dragon Pays; "кловер порчу" / "к ловерфорту" = Clover Fortune; "дачмил" = Dutch Mill; "мид найтмани" = Midnight Money; "нато 2" = Nebraska 2 (**inference**); "ф п с эвен" (the notes: "FPS Even"); "харвари трекинг" = hardware tracking; "клот" / "клод" = Claude; "селф кост и транер" / "селхоста транер" = self-hosted runner.
- **Where the notes and the transcript differ.** The notes call the "950" printer "Epson-type"; the transcript does not name a maker — not recorded. The notes give the spike as FP-1364; the transcript has both "13 604" and "13 64". The notes put Pavel's "matter of taste" on keys vs password; the transcript agrees ("вкусовщина").
- **Skipped as logistics or chatter.** The 11:45 vs 12:00 stand-up time (not moved), who presses the start button, Irina's remarks about the Alekseev meeting, the jokes about naming the agent beyond the point recorded, greetings and goodbyes.
- **§15.8:** clear. Nobody's pay or rate appears. **§15 #9:** clear; the numbers are Jira keys, capability numbers, kernel versions and a printer model number. The SSH login and password were only mentioned as stored in repository secrets; no value was spoken.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
