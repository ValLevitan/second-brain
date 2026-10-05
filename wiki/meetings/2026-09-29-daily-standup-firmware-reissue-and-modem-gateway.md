---
type: meeting
title: Daily stand-up — "no hack, we re-release", the version table moves to main, the modem as default gateway breaks the progressive link, and Flex IQ firmware update comes first (Sept 29 2026, 4:49–5:14 AM)
date: 2026-09-29
aliases: [Daily Standup meeting Sept 29 2026, Daily Standup Firmware Reissue and Modem Gateway, Sept 29 stand-up, re-release not a hack, перевыпускать, 4.50.2, version table in main, modem default gateway, shadow traffic, теневой трафик, Flex IQ firmware update first, EGM emulator delay cases, game select stubs, TINT-41]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — "no hack, we re-release", and the modem as default gateway (Sept 29 2026)

**Date/time:** September 29 2026 (a Tuesday), **4:49 – 5:14 AM Eastern** (about 25 minutes), from the `**Date:**` header line [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up; the connection dropped for everyone once, near minute 15 ("все отвалились") [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (ran it), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"; joined late), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]. Val was not present; "Игоря не вижу" — an Igor was absent (not resolved).

**Purpose.** Round-the-table status, then three items from Pavel: Val's ruling of the day before that a fix goes out as a re-release and not a hack; the finding of the previous evening that the modem, when it is the default gateway, breaks the progressive link; and Kovalchuk's note that the team is closing its Jira tasks [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. A corpus-wide grep for both filenames, "Firmware_Reissue", "September 29, 2026, 4:49" and "перевыпускать" found no page citing either file and no other Sept-29 stand-up stub. The same morning's [[wiki/meetings/2026-09-29-ai-pm-architecture-and-second-brain-plan.md|6:02 AM "Design_AI-PM" call]] is a different meeting (Val's call, other attendees, other subject). It is a new meeting.

Substance lives on:

- [[wiki/decisions/2026-09-29-the-fix-goes-out-as-a-re-release-not-a-hack-and-only-that-commit-goes-in.md]] — Val's ruling as Pavel reported it; Irina's one-commit rule; the 4.50.2 build and the library change
- [[wiki/topics/github-release-management-pipeline.md]] (Sept 29) — Kharetski's version table (release version → data centre → games) moved into main, and why
- [[wiki/decisions/2026-09-17-lte-is-the-default-route-and-the-manual-override-stays.md]] — Sept-29 update: with the modem as default gateway the progressive link keeps reconnecting and broadcast packets leak to the modem
- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] — Sept-29 update: Pavel puts the Flex-Port firmware update through Flex IQ first for Seregin
- [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] — Sept-29 update: the Flex IQ emulator before any Flex-Port emulation; Khamin adds delay and hang cases to the EGM emulator himself
- [[wiki/topics/test-automation-strategy.md]] (Sept 29) — Khamin's TINT tests, Ivan's tests placed by Claude, Vladimir starts on TINT-41, Irina learns the set-up
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 29, 4:49 AM) — Chudinov's capabilities, Tsymanov's wallet through the Flex-Port (156) and zero balance (158), Biratka's 134 waiting on a real server
- [[wiki/topics/nova-platform-architecture.md]] (Sept 29) — the game-select screen goes ahead with stub names
- [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] — Sept-29 update: "ребята молодцы… есть динамика"
- [[wiki/decisions/2026-09-24-written-records-go-by-email-and-chats-are-for-instant-matters.md]] — Sept-29 update: Ivan's instruction goes by email, not into the group chat
- People: [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/vladimir-samusenko.md]]

**§4 name calls** [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]:

- "саша" = Biratka (speaker label "Alexander Biratko"; he answers when he appears). "Алексей" / "Лёша" (none spoken as Лёша here) = Khamin. "Антон" called on = Seregin (he answers). "Даниил" = Daniil Stauskiy. "Дима" called on after Daniil = Chudinov (label "Dzmitry Chudzinau"; he answers). "Женя" = Kharetski (he answers). "Ира" = Irina Shishko. "иван" / "ваня" / "ванины тесты" = Ivan (label "Ivan Shpak"). "Сергей" = Tsymanov. "Владимир" = Samusenko. "дима" at the very end = Kovalchuk (he answers). "паш" = Pavel. "вал" = Val Levitan, reported, not present.
- "мы с Димой так быстро глянули" (Tsymanov, on the zero-balance tasks under 158) = Chudinov, **by context** (Flex IQ backend) — inference.
- "Игоря не вижу" — which Igor is **not resolved**; queued, not forced.
- "Аксен" in Pavel's greeting, "Томск" in Daniil's report and "таммар 64" in Tsymanov's — **unclear** words, not interpreted.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]):

1. **"Version 4.50.2".** The notes give "4.50.2". The transcript has "502", "4504502", "3 этот 4502", "64502" — read as 4.50.2 against "4501" (4.50.1) and "460" (4.60). The reading is an **inference**; the spoken forms are kept on the decision page.
2. **The library.** The notes say "a library (broadcast)". The transcript word is "Бракаст" — **unclear**; "broadcast" is the notes' reading only.
3. **Evgeny's tasks.** The notes give "LGS-219 and LGS-217". The transcript: "Л джес 212 19 и л джи с 12:17" — garbled; LGS-219 / LGS-217 is a reading. His new task is "росссервиса для сити толка" — **unclear**, not interpreted (the notes say "a service integration").
4. **Daniil's feature.** The notes give "FAR-1483/1484". The transcript: "28 фичи far 1483" and "фараум 1484" — the prefix is garbled.
5. **Omitted by the notes:** Kharetski's remark that the broadcast-library change was made "чтоб… править нормально и подстраховаться на будущее"; Pavel's "давайте тогда с Алексеем" because Sasha was not yet visible; and Pavel's line that he made Kharetski a cable ("я тебе кабель сделал").
6. **"Val ruled yesterday".** Both files say so. No Sept-28 raw in the corpus carries the ruling; it is recorded here as reported by Pavel.

**§15.8:** clear. Work status and process only; Kovalchuk's "ребята молодцы" is recorded as a team-level status remark. Nobody's pay, performance or personal matters are recorded. **§15 #9:** no corporate identifier appears. Capability numbers (134, 150, 152, 156, 158, 176, 230), task keys (TINT-16, TINT-41, TINT-79, 601, LGS-219 / 217 as read) and version numbers (4.50.1, 4.50.2, 4.60) are work references.

## Sources
- [[raw/Meeting_Notes_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
