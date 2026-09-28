---
type: meeting
title: Daily stand-up — the kiosk emulator gets a new priority one, and capability 118 is split by product (Sept 23 2026, 4:48–5:16 AM)
date: 2026-09-23
aliases: [Daily Standup meeting Sept 23 2026, Terminal Emulator and Capability Split, Sept 23 stand-up, CAP-118 split, bill validator emulator, STG certificate problem]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — terminal emulator and the capability split (Sept 23 2026)

**Date/time:** September 23 2026, **4:48 – 5:16 AM Eastern** (about 28 minutes), from the recording header [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.**

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (ran it), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (the student developer; no page), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov") and [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]. Val was not present.

**Purpose.** The Minsk team's round-the-table stand-up. Two items took most of the time: what the kiosk emulator must do next, and capability 118, which mixed two products [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search found no other Sept-23 stand-up stub. The previous day's stand-up ([[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md]]) is a different session with different content. It is a new meeting.

Substance lives on:

- [[wiki/decisions/2026-09-23-capability-118-is-split-by-product-and-two-devices-keep-two-repositories.md]] — the split, and why the two devices stay in two repositories
- [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] — Sept-23 update: the emulator's new priority one
- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] — Sept-23 update: Flex-Port firmware named as the emulator's most critical use
- [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]] — Sept-23 update: 137, 152, and new items nobody had discussed
- [[wiki/topics/test-automation-strategy.md]] (Sept 23) — how transactional autotests should be organised; Ivan as a Claude operator
- People: [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/evgeniy-alekseev.md]] · [[wiki/people/andrei-klimovich.md]] · [[wiki/people/andrey-bosik.md]]

**§4 name calls** [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]:

- "Антон" who reports on the emulator = [[wiki/people/anton-seregin.md|Anton Seregin]], by **speaker label**. The unnamed "Антон" building a FlexPay emulator on Sept 22 is **very likely the same man (inference)** — same work, next day.
- "демоном… который вот Антон писал" — a *different* Anton who wrote the validator daemon. **Not resolved.**
- "Евгению Алексееву" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], named in full (Flex-Port firmware; fits his registry role).
- "женя" called on by Pavel = [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] (he answers; speaker label).
- "Саша" = Biratka. "дима" = Chudinov (he answers). "Сергей" = Tsymanov. "ира" = Shishko.
- "Андрей" who should have created the GUI capability (Irina: "180") and who created new requirements = [[wiki/people/andrei-klimovich.md|Klimovich]], **by context** (he writes the capabilities and owns 180). "Андрей" whom Chudinov will see about the STG cluster, and who had argued the shared setup saves money = [[wiki/people/andrey-bosik.md|Bosik]], **inference** — he runs the cloud side. Neither is named with a surname.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]):

1. **"Production will not have this problem."** The transcript has "Добро вроде как такой проблемы не будет". Reading "Добро" as "прод" (production) is an **inference**.
2. **Omitted by the notes:** Chudinov's remark that Andrei had argued the shared cluster "мы экономим кучу денег"; Chudinov's "на меня flexpay не вешайте"; Irina archiving the old requirements; Pavel deleting the wrongly created IP-1201 before the meeting; Vladimir's new feature "Фпорт 52".
3. **Daniil's report.** The notes say he "moved the panel games across". The transcript is garbled ("Перенёс видок панеллис игры во Франк"). What he moved is **unclear**; only his next step (a second copy of a game to test switching and paid-game limits) is clear.
4. **Vladimir's work.** The notes say "review GUI for the board". The transcript has "ревор гуи для борта". Given his Sept-22 screen redraw, "rework" is the likelier reading (**inference**).

**§15.8:** clear. Work status, Jira and tooling only. No pay, rate or personal judgement appears. **§15 #9:** no corporate identifier appears. Capability, requirement and ticket numbers (118, 137, 152, 180, FP-1249, FP-1250, FP-1251, REQ-1460, IP-1201, requirement 743) are work references. No phone number was spoken.

## Sources
- [[raw/Meeting_Notes_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
