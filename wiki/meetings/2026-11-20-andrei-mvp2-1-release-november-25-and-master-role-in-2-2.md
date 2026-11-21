---
type: meeting
title: Call "MVP2_1 and MVP2_2 review, pt2" — Klimovich's follow-up to the Nov-19 clean-up call; MVP 2_1 is frozen (development done, autotests left) and its Jira date moves from November 23 to Wednesday November 25; task 399 (Alekseev's firmware that flashes the Wi-Fi module) moves from 2_2 into 2_1; no central rollback to an older build — fix forward with a same-day patch; MVP 2_2 is the master (operator) role and reporting, its date named only after a scope freeze; SAS statistics in bill-validator mode go to MVP 3; Val asks what the law requires when a location changes master; the MVP 3 offline-versus-always-online question is parked, Val backing always-online (Nov 20 2026, ~9:02–~10:01 AM)
date: 2026-11-20
aliases: [MVP2_1 and MVP2_2 review pt2, Andrei MVP2_1 Release November 25 and Master Role in 2_2, Nov 20 MVP 2 call, Nov 20 9:02 AM call]
source-count: 2
open-commitments: 0
open-questions: 0
---

# MVP 2_1 / 2_2 review, part 2 — release November 25 and the master role in 2_2 (Nov 20 2026, 9:02 AM)

**Date/time:** Friday November 20 2026, **~9:02 – ~10:01 AM Eastern** (recording), about 59 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Andrei_MVP2_1_Release_November_25_and_Master_Role_in_2_2-November-20-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Release_November_25_and_Master_Role_in_2_2-November-20-2026.md]]. Teams title: "MVP2_1 and MVP2_2 review, pt2". **Language: Russian.** It is the follow-up set at the [[wiki/meetings/2026-11-19-andrei-mvp2-1-reporter-cleanup-and-release-date-slip.md|Nov-19 8:04 AM clean-up call]].

**Who spoke** (speaker labels): [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (led; organizer per the notes), [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov") [[raw/Meeting_Transcript_Andrei_MVP2_1_Release_November_25_and_Master_Role_in_2_2-November-20-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Release_November_25_and_Master_Role_in_2_2-November-20-2026.md]].

**Purpose:** close the open MVP 2_1 items and set its date, then open MVP 2_2 [[raw/Meeting_Transcript_Andrei_MVP2_1_Release_November_25_and_Master_Role_in_2_2-November-20-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-11-20-mvp-2-1-is-set-for-wednesday-november-25-task-399-moves-into-2-1-no-central-rollback-fix-forward-and-mvp-2-2-is-the-master-role-and-reporting.md]] — the date, task 399, rollback, the master role, location changes and the law, the 2_2 plan, SAS stats to MVP 3, the parked offline debate; all commitments and questions.
- [[wiki/decisions/2026-11-19-the-november-20-mvp-2-1-date-will-not-hold-each-reporter-cleans-up-their-own-2-1-items-before-a-follow-up-call-and-cap-267-is-closed-into-cap-146.md]] (Nov-20 note) — the new date answers its open question.
- [[wiki/decisions/2026-11-12-mvp-2-splits-into-mvp-2-1-iq-and-port-and-mvp-2-2-web-services-lottery-becomes-goods-and-the-inspector-report-becomes-the-audit-report.md]] (Nov-20 note) · [[wiki/decisions/2026-11-05-mvp-2-is-kept-narrow-wi-fi-with-the-flex-iq-as-access-point-or-client-remote-flex-port-update-robust-installation-and-install-diagnostics-due-november-20-and-the-rest-goes-to-mvp-3-around-january-20.md]] (Nov-20 note) — the date and the master role.
- [[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]] (Nov-20 update) — the cloud-wallet / offline question for MVP 3.
- [[wiki/organizations/incom.md]] (Nov 20) — a terminal registered at one location must not work at another; master changes told to InComm by hand.
- People: [[wiki/people/andrei-klimovich.md]] · [[wiki/people/val-levitan.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/evgeniy-alekseev.md]] (in absentia) (all Nov 20)

## Notes on the sources

- **§12 — new meeting.** The notes and transcript share date, time and title and link each other. A corpus-wide grep for both filenames, "November-20-2026", "2026-11-20" and "9:02" found no page citing either file. The Minsk stand-up at ~3:44 AM the same day is a different recording ([[wiki/meetings/2026-11-20-daily-standup-firmware-rollback-and-manual-only-autotests.md]]).
- **Identity.** The filename says "Andrei"; the speaker label is Andrei Klimovich, and the MVP / product-owner context fits him (§4 Andrei cluster).
- **Notes vs transcript.** They agree. The notes' "~2 weeks after 2.1" for the 2_2 scope freeze is "У нас, наверное, занимает ещё 13:02 на. Скоуп фриз 2 и 2" on tape — the length is a garble, so "~2 weeks" is the notes' reading. The notes' "Val suggested moving very large capabilities out (2.2 → 2.3)" is "Я вам советую отказаться от таких папило… Если такие победа очень большая, сделать это 2.2, а 2.2 перенесите на 2.3" — garbled; the notes' reading is kept as such. The notes' "Release 2.1 date moved from Nov 23" matches "у нас стоит сейчас дата 23 ноября".
- **§4 name calls.** "Алексеев" (task 399) = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (firmware context — **inference**; not in the call); "гена" / "Геннадием" = [[wiki/people/genadi-peari.md|Genadi Peari]] (**inference**; "гена сказала" is a speech-to-text gender slip); "дима" = Chudinov; "Сергей" = Tsymanov; "Андрей босик" (named by Chudinov for Grafana alerting) = [[wiki/people/andrey-bosik.md|Andrey Bosik]]; "вал" = Val; "ира" = Irina; "Паша" = Pavel.
- **Garbles kept as heard.** "21" / "02:01" / "2 и 2" / "22" = MVP 2_1 / 2_2; "MP один с половиной" / "релиз 1.5" = a 1.5 release; "рекларс" / "рекламент" / "эквариментов" = requirements; "capoбити" / "каполите" / "копыбили" / "папило" / "победа" = capability; "Азы гудсати ну вместо лотере" = Goods instead of lottery; "маяк майнер чен" = minor change; "лакейшн" / "лакей" = location; "мастер лайнс намбер" / "м л" / "млч код" = master licence number; "lackation andrei" / "lakation oner" = location owner; "marti" / "martine arovin" — the master list in the admin (**inference**); "ИНКОМ" / "инкол" = InComm; "ураган" / "уранаус" / "wargause" / "рехаус" = warehouse; "партишино" = partition; "андроиде вайос" = Android, iOS; "halles чек" = health check; "icran" = screen; "билаксатор" / "сас" = bill acceptor / SAS; "графании алёртингов" = Grafana alerting; "волитов" = wallets; "Тесла антенну" — kept as heard (a satellite antenna is **inference**); "sellober communication" = cellular communication; "callo bity" = scalability (**inference**); "дерпменсе" — **unclear**.
- **Idiom, not personal.** Val's "дима же не может быть чутьчуть быть беременным" is the Russian idiom "you can't be a little bit pregnant" (no half-measures) about Chudinov's architecture stance.
- **Skipped as chatter.** Screen sharing, "Похоже на коммунизм" (Pavel), Val's "Тогда" interruptions, the goodbyes. The last minute mentions a next call with Val "про инкомовский этот тест" — logistics.
- **Not recorded:** none; no personal passage.
- **§15.8:** clear. **§15 #9:** clear — the master and location licence numbers are named as fields only; no value.

## Sources

- [[raw/Meeting_Transcript_Andrei_MVP2_1_Release_November_25_and_Master_Role_in_2_2-November-20-2026.md]]
- [[raw/Meeting_Notes_Andrei_MVP2_1_Release_November_25_and_Master_Role_in_2_2-November-20-2026.md]]
