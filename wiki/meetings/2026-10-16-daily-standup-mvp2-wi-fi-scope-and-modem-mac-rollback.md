---
type: meeting
title: Daily stand-up — MVP 2 is now only Wi-Fi and remote port update through Flex IQ (Flex Pay is MVP 3); the modem-MAC commit is rolled back; AI Draft tasks live 24 hours; the payment hub waits for RIS (Oct 16 2026, 4:46–5:20 AM)
date: 2026-10-16
aliases: [Daily Standup meeting Oct 16 2026, Daily Standup MVP2 WiFi Scope and Modem MAC Rollback, Oct 16 stand-up, MVP 2 two tasks, modem MAC rollback stand-up, FP 1335, capability 138, LGS 1226, LGS 1228, PR 226, TIN 80]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — MVP 2 scope and the modem-MAC rollback (Oct 16 2026)

**Date/time:** October 16 2026 (a Friday), **4:46 – 5:20 AM Eastern**, about 33 minutes, from the `**Date:**` header line. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel. The previous stand-up is [[wiki/meetings/2026-10-15-daily-standup-offline-ris-fallback-and-nova-game-conversion.md|Oct 15]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]]. Val was not present. [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] was on vacation.

**Purpose.** Friday round-the-table status. Pavel also passed on what the previous day's coordination meeting had set for MVP 2.

## Where the substance lives

- [[wiki/decisions/2026-10-15-mvp2-is-flex-iq-wi-fi-remote-update-diagnostics-and-galaxy-reporting-and-flex-pay-moves-to-mvp3.md]] (Oct-16 update) — MVP 2 is "исключительно" two tasks; Flex Pay renamed MVP 3; three weeks; capabilities to check; Sergey's Stripe experiment waits for RIS; a scope question opened against Val's Oct-15 list.
- [[wiki/decisions/2026-10-16-the-flex-iq-commit-that-sets-the-modem-mac-at-boot-is-rolled-back-and-the-shared-mac-stays.md]] — new: the modem-MAC rollback and Vladimir's modem that comes back only after a reboot.
- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-16 update) — remote port update through Flex IQ is MVP 2; Biratka's loader task FP 1335; Khamin's feature for Alekseev's branch.
- [[wiki/decisions/2026-10-15-flex-iq-gets-a-switch-between-its-own-access-point-and-an-external-router-and-mvp2-starts-on-the-router.md]] (Oct-16 note) — Wi-Fi on the Flex-Ports and Flex IQ is half of MVP 2.
- [[wiki/decisions/2026-09-15-every-device-carries-its-own-lte-modem-and-sim.md]] (Oct-16 note) — the modem pointers.
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 16) — Biratka's FP 1335, capability 138 and the bezel lights, the Terminal Hub parameters; "yesterday's release".
- [[wiki/topics/test-automation-strategy.md]] (Oct 16) — Khamin's hardware CI; Seregin's printer scenarios and the paper jam; Ivan's 0x89 case; Vladimir's Galaxy autotests.
- [[wiki/topics/nova-platform-architecture.md]] (Oct 16) and [[wiki/decisions/2026-10-08-texas-rage-games-convert-to-vertical-nova-unchanged-and-igor-ports-dutch-mill-first.md]] (Oct-16 update) — Clover Fortune's vertical layout; a Georgia game into Nebraska 2; NAD 2; the vertical Dutch Mill; Efim's maths container; the blocked video account; Daniil's board.
- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 16) — Kharetski's RIS analysis; Tsymanov's RIS task.
- [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-16 update) and [[wiki/projects/ai-project-manager-and-company-second-brain.md]] (Oct 16) — AI Draft lives 24 hours; AI Draft in the dashboard To Do column; LGS 1226 / 1228; tasks with no parent and a grooming step.
- People: [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/igor-metelski.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/dmitri-chudinov.md]] (in absentia) · [[wiki/people/andrey-bosik.md]] (in absentia) · [[wiki/people/sergey-kleimenychev.md]] (in absentia) · [[wiki/people/genadi-peari.md]] (in absentia) · [[wiki/people/evgeniy-alekseev.md]] (in absentia) · [[wiki/people/efim-podvoiski.md]] (in absentia) · [[wiki/people/lena.md]] (in absentia) · [[wiki/people/nathan-carver.md]] (in absentia) · [[wiki/people/val-levitan.md]] (in absentia)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "October-16-2026", "2026-10-16", "FP 1335", "capability 138", "0x89", "LGS 1226" and the MAC terms found no page citing either file and no stub for this session. The other Oct-16 raws (Klimovich / Vysotski; David Villari; Lev Rudky; the third-party EGM Flex-Port tests) have different titles and content. The "coordination meeting on the transactional product" the day before is not identified in the corpus; the Oct-15 11:04 AM Wi-Fi meeting is a candidate, but Pavel's account differs from it (**inference**; see the MVP 2 page).
- **§4 name calls.** "Саша" = Biratka (he answers). "Алексей"/"Лёша" = Khamin (he answers; the AI made "2 лёши" tasks). The first "Антон" (games) = Leshkevich and the second (printer) = Seregin, by speaker label; the "Антон" with one AI task and the "Антон" working with Igor on NAD 2 = Leshkevich by context (**inference** for the AI task). "Даниил" = Daniil Stauskiy. "дима что в отпуске" and "дима из отпуска вернётся только через неделю" = Chudinov (the notes write "Dzmitry Chudzinau"; Kovalchuk was present). The "Дима" who made the MAC commit with Pavel is not named — Chudinov likely (**inference**). "Дима" asked to put AI Draft on the dashboard = Kovalchuk (he answers). "Женя" = Kharetski (speaker label; RIS fits him). "Алексеева ветка" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]. "гений" = [[wiki/people/genadi-peari.md|Genadi Peari]] (notes: Genadi). "Лена с дизайнерами" = [[wiki/people/lena.md|Lena]]. "ефим" = [[wiki/people/efim-podvoiski.md|Efim Podvoiski]]. "Сергея льёныча" and "Сергея климёновича" = [[wiki/people/sergey-kleimenychev.md|Sergey Kleimenychev]] (notes: "Sergey Klimenovich"; video work fits him). "Андрея босика" is named in full = [[wiki/people/andrey-bosik.md|Bosik]]; the "Андрей" who looked into accounts the day before is the same by context (**inference**). "нейтану" = [[wiki/people/nathan-carver.md|Nathan Carver]]. The "Андрей" to be shown the payment-hub screens with Val is **not identified** — Klimovich is likely (**inference**). "Сергей" = Tsymanov (speaker label).
- **Garbles kept as heard.** "ф п 13 35. Этот лодер для ivда" (the notes: FP 1335, a loader, board name unclear); "кап обилите 138"; "бизели/базели" (bezels); "один 93" (the notes: "193" as heard); "хип оф памяти"; "отлор форча" (Clover Fortune per the notes); "калёчо из джорджии" (a Georgia game; Calle Ocho by sound — **inference**); "надом 2"; "gpra", "фил игра"; "подчмил" (Dutch Mill); "о мни" (OMNI); "фейки 102 103 129"; "serronty"; "ноль икс 89"; "пиару 226"; "тинт 80"; "в течение 20 04:00" (the notes: 24 hours); "НАТО 2" (NAD 2 per the notes); "LGS 12 26 LGS 12 28"; "Приватизации подключения" (read as connection priority); "Это для пинг агента?" (Kovalchuk's question on the Terminal Hub task — perhaps "PM agent", unclear).
- **Where the notes and the transcript differ.** None of substance. The notes add "Igor and Pavel think a meeting with Val is needed"; Igor asked whether they need to meet Val and Pavel said "Похорошему надо, я думаю".
- **Vacation dates.** On Oct 15 Pavel said Chudinov and Samusenko are away "ближайшие 2 недели как минимум"; on Oct 16 Chudinov "вернётся только через неделю", and Samusenko attended and planned weekend work. See the Chudinov and Samusenko pages.
- **Skipped as chatter.** Greetings, "Повзрослели да?", goodbyes.
- **§15.8:** clear. Nobody's pay. Vacations are availability facts. Stripe's fees are vendor economics. **§15 #9:** clear; the numbers are Jira keys, task, PR and error codes. No MAC address value was spoken.

## Sources

- [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
