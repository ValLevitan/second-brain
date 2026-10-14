---
type: meeting
title: Transactional MVP 1 — port and transaction screens go under the admin role, unclaimed money shows in cashier Records with no action, no print queue in MVP 1, Epic 950 is the printer tested first, and Val holds all other questions to release on October 15 (Oct 5 2026, 8:01–8:22 AM)
date: 2026-10-05
aliases: [Transactional MVP1 sync Oct 5, Transactional MVP1 Port Screens Unclaimed Money and Printer Models, day fifteen of the MVP1 series, Oct 5 8am transactional call, capability 141, капбилити 141, FAQ 37, unclaimed in Records, анклейм в рекордах, позвоните JVL, no print queue, без очереди, Epic 950 and Epic Edge, эпик 950, TITO printer stops printing, print daemon sleeps, SAS commands to Grafana, focus on MVP1]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Transactional MVP 1 — port screens, unclaimed money and printer models (Oct 5 2026)

**Date/time:** October 5 2026 (a Monday), **8:01 – 8:22 AM Eastern** (about 21 minutes), from the `**Date:**` header line [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]. **Series:** the Teams session "Transactional MVP1 sync" — the **fifteenth** morning call, the next after [[wiki/meetings/2026-10-01-transactional-mvp1-status-slice-and-sas-command-logging.md|Oct 1]]. **Language: Russian.**

**Who spoke** (speaker labels): [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (chair), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik", two broken lines only), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/val-levitan.md|Val Levitan]].

**Purpose.** Chudinov's gaps documents and the port and transaction screens of capability 141; where the cashier sees unclaimed money; the remote update and a TITO printer that stops; Georgia's silence; which printer models the terminal supports; whether a print queue is needed; and Val's call to stop opening questions and release.

**§12 — one meeting, two files.** The notes and the transcript share date, time and title and link each other. A corpus-wide grep for both filenames, "Port_Screens_Unclaimed", "2026-10-05" and "Transactional MVP1 sync" found no page citing either file and no other Oct-5 MVP 1 stub. The same morning's [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|4:54 AM stand-up]] is a different meeting (Pavel's chair, other time). It is a new meeting.

Substance lives on:

- [[wiki/decisions/2026-10-05-flex-port-and-connection-settings-screens-live-under-the-admin-role-not-the-cashier.md]] — the port and transaction screens: admin role, the Recycler's port display as the model
- [[wiki/decisions/2026-09-24-a-flex-port-that-dies-holding-money-sends-it-to-unclaimed-and-one-without-a-gateway-goes-out-of-service.md]] — Oct-5 update: unclaimed money is shown in cashier Records, nothing is done with it, "call JVL"
- [[wiki/decisions/2026-10-05-mvp1-has-no-print-queue-and-tickets-print-or-reprint-from-records.md]] — Val asks Klimovich to pick one option; no queue in MVP 1
- [[wiki/decisions/2026-10-05-epic-950-is-the-terminal-printer-tested-first-and-all-models-stay-supported.md]] — the printer models; Pavel writes the requirement
- [[wiki/decisions/2026-09-28-october-15-replaces-october-1-as-the-mvp1-date.md]] — Oct-5 update: Val holds every other question; testing for October 15; MVP 2 writing waits for Klimovich
- [[wiki/decisions/2026-10-01-mvp2-capabilities-biratka-ports-flex-iqs-to-flexpay-and-writes-no-new-ones-until-klimovich-defines-the-flows.md]] — Oct-5 update: Val says MVP 2 writing starts when Klimovich is back
- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] — Oct-5 update: the remote update works on a terminal; the TITO printer question
- [[wiki/decisions/2026-10-02-sas-command-logs-are-collected-on-the-flex-iq-and-not-sent-to-grafana-by-default.md]] — Oct-5 note: Chudinov says the SAS commands now go to Grafana (open contradiction with the Oct-2 rule)
- [[wiki/decisions/2026-09-30-elizabeths-georgia-set-up-questions-go-to-a-shared-teams-chat-not-one-person.md]] and [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] — Oct-5 updates: still no word from Georgia; Klimovich pings Elizabeth again
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 5, 8:01 AM) — the day-fifteen entry
- People: [[wiki/people/andrei-klimovich.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/pavel.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/val-levitan.md]] · [[wiki/people/elizabeth.md]] (discussed, not present) · [[wiki/people/vladimir-samusenko.md]] (discussed, not present)

**§4 name calls.** "Дима" = Chudinov. "Паша" / "Павел" = Pavel. "Элизабет" = Elizabeth. "Владимир", who built the port display in the Recycler = [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], by context — the only Vladimir in the corpus, and he has worked on the Recycler (inference). "Геннадий" = Genadi Peari. "Сергея нет" (Chudinov, on the printers) = Sergey Tsymanov, by context (inference). "Андрей сделал… макап… для флекса айкью" = Klimovich, by context (inference). "Клод" / "лод" = Claude, the AI tool. "капбирите 141" = capability 141; "эфэйкю 37" — the notes do not give it; read as feature 37 (unclear). "анклы" / "andland" / "and cleamt" = unclaimed. "мвпи" / "MBP" / "MPA" = MVP.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]):

1. **The Epic Edge.** The notes say Pavel narrowed testing to the 950 after first naming both. In the transcript Ivan said "Только 950 эдже не будет" and later "пока что эдж идет от 50, хорошо?" — both garbled. Pavel: "Я за то, чтобы все все поддерживать, но просто сейчас не активно не тестировать это." What "это" is (the Edge, or other models) is not fully clear.
2. **Klimovich's return.** The notes say he flies back on the 12th. The transcript: "Я 12 прилетаю только я мог бы 13" — the 13th is his first possible day, which fits the Oct-1 "до 13 октября".
3. **Undertaking 5's date.** The notes give "Oct 7" for the small tasks. Chudinov said "завтра послезавтра" — Oct 6 or 7.

**§15.8:** clear — product and schedule only. Klimovich's absence is a schedule fact; where he goes is not recorded. **§15 #9:** none; 141 and 37 are work references.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
