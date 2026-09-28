---
type: meeting
title: Daily stand-up — how firmware reaches the device is still open, the Flex IQ emulator is copied from FlexPay, and capabilities get a Req Review status (Sept 24 2026, 4:46–5:23 AM)
date: 2026-09-24
aliases: [Daily Standup meeting Sept 24 2026, Firmware Delivery and Capability Statuses, Sept 24 stand-up, Req Review status, Completed versus Closed, Georgia MD file 15 games, firmware delivery spike]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — firmware delivery and capability statuses (Sept 24 2026)

**Date/time:** September 24 2026, **4:46 – 5:23 AM Eastern** (about 37 minutes), from the recording header [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.**

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (ran it), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (the student developer; no page), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov") and [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]. Val was not present.

**Purpose.** The Minsk team's round-the-table stand-up. Three longer threads: how firmware gets to the devices, the Georgia game list for the lab, and new Jira statuses for capabilities [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search found no other Sept-24 stand-up stub. The Sept-23 stand-up ([[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md]]) is a different session with different content. It is a new meeting.

Substance lives on:

- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] — Sept-24 update: the delivery method is not defined, and a spike is proposed
- [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] — Sept-24 update: the Flex IQ emulator is the FlexPay one, moved across
- [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]] — Sept-24 update: Req Review, the grey Accept status, Completed versus Closed
- [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] — Sept-24 update: To-Do dates, and the report goes out by email
- [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]] — Sept-24 update: features raised, capability 237, new Flex-Port screens out of MVP 1
- [[wiki/decisions/2026-09-23-open-requirements-are-settled-on-the-call-and-only-slow-ones-are-parked.md]] — Sept-24 update: the lost-money bugs are linked to 231 and stay in the team
- [[wiki/topics/test-automation-strategy.md]] (Sept 24) — who checks before Closed, Ivan's write access, stale docs
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 24) — Flex-Port screens, the collect button, the Flex IQ wallet task
- [[wiki/projects/georgia-market-rollout.md]] (Sept 24) — the lab file lists all 15 games
- People: [[wiki/people/pavel.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/ivan.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/andrei-klimovich.md]] · [[wiki/people/eugine-yavorski.md]] · [[wiki/people/evgeniy-alekseev.md]]

**§4 name calls** [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]:

- "Антон" on the emulator and the spike = [[wiki/people/anton-seregin.md|Anton Seregin]], by **speaker label**.
- "Антона", who reworked the package naming so all of Kharetski's libraries load at once — **not resolved** (possibly Seregin; not asserted).
- "дима чудинов" = [[wiki/people/dmitri-chudinov.md|Chudinov]] (named in full). "Дима" called on after Daniil = Chudinov (he answers). "Дима" at the end = [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] (he answers). "дима Ковальчука" = Kovalchuk (named). "дима" who will add an API for Khamin — **not resolved** (the notes say Kovalchuk).
- "Климович" / "климой" = [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (surname). "Андрей" who created new capabilities, whose design Vladimir follows, and who gets Sergey's questions = Klimovich, **by context** (he writes the capabilities and the screens).
- "яворский" = [[wiki/people/eugine-yavorski.md|Eugine Yavorski]]. "Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (surnames; registry roles fit).
- "Игорь", who made another FaceBoard game — **likely** [[wiki/people/igor-metelski.md|Igor Metelski]] (**inference**, from the Sept-22 game-conversion work). "жени", to join the PariSys talk — **not resolved** (Kharetski was present; not asserted). "Ефрем", whom Chudinov asks about as a checker, "Алексу", whom Ivan briefed, and "Татьяна" — **not resolved**.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]):

1. **"Same protocol and contracts."** The notes give this to Anton. In the transcript Anton asks it as a question, and Pavel confirms: "Протокол общения с портами у них одинаковый". Anton's own point is that he emulates device behaviour, not screens.
2. **The spike.** The notes list it as agreed. In the transcript Pavel proposes it; Chudinov's reply is unclear; Anton says he will first move the emulator across "за сегодня".
3. **Kharetski's tickets.** The transcript has "12 18 я сделал 12, 21 в работе 20, 19 и 17". The notes drop the "20". "22 интеграции" is unclear and is not interpreted.
4. **Chudinov's last report.** The notes say "a firmware change". The transcript has "добиваю уже последние фиксы по апрейтам… Смена всётаки январтов" — what changed is **unclear**. Only "на одном терминале прошла хорошо… на другом какието проблемы" is clear.
5. **Omitted by the notes:** Chudinov saying "вал говорил тогда клоуз" at some recent meeting; Ivan naming both Intralot and Eclipse ("между интерлотом и клипсом"); Anton saying the emulator runs only on his machine and is pointless to run in the cloud; the new capability 237 having been created "13:00 назад".
6. **"прозу".** The notes guess OpenAPI or spec docs. The wiki reads it as JVL's own "prose" docs (**inference**), the term used since August.

**§15.8:** clear. Work status and Jira process only. Kovalchuk named three colleagues whose To-Do tasks lack dates; this is recorded as a process point, and the names are not recorded. No pay or personal judgement appears. **§15 #9:** no corporate identifier appears. Capability and ticket numbers (137, 152, 231, 236, 237, 12-17 to 12-21, 12-50, 12-51, 13-49, 14-85) are work references.

## Sources
- [[raw/Meeting_Notes_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
