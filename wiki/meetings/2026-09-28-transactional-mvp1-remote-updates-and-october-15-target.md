---
type: meeting
title: Transactional MVP 1 — October 15 becomes the working date, remote Flex-Port update comes back into MVP 1, the update dashboard is shown, and "no private chats" (Sept 28 2026, 8:02–8:45 AM)
date: 2026-09-28
aliases: [Transactional MVP1 sync Sept 28, MVP1 Remote Updates and October 15 Target, day eleven of the MVP1 series, Sept 28 8am transactional call, October 15 is the real date, no private chats, личных чатов нету, terminal management Updates tab, PORT-13 stays with Alekseev, FlexPort brackets for Aristocrat]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Transactional MVP 1 — remote updates and the October 15 target (Sept 28 2026)

**Date/time:** September 28 2026 (a Monday), **8:02 – 8:45 AM Eastern** (about 43 minutes), from the `**Date:**` header line [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]. **Series:** the Teams session "Transactional MVP1 sync" — the **eleventh** morning call, after [[wiki/meetings/2026-09-25-transactional-mvp1-flexport-third-party-egm-compatibility-testing.md|Sept 25]]. **Language: Russian.**

**Who spoke** (speaker labels): [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (chair), [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"; shared the dashboard), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin") and [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik") [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].

**Purpose.** Chudinov's card-activation cases and a PIN question; Irina's status on requirements and autotests; the release date; remote update of the Flex-Port and of Flex IQ in Georgia; MVP 2 questions [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search found no page citing either file and no other Sept-28 MVP 1 stub. The same day's [[wiki/meetings/2026-09-28-daily-standup-log-traffic-and-nova-rename.md|4:56 AM stand-up]] is a different meeting. It is a new meeting.

Substance lives on:

- [[wiki/decisions/2026-09-28-october-15-replaces-october-1-as-the-mvp1-date.md]] — the date moves; autotests may run to October 23; a trial batch of about 10 locations
- [[wiki/decisions/2026-09-09-first-transactional-installation-planned-for-october-1.md]] — Sept-28 update: retitled and superseded
- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] — Sept-28 update: remote Flex-Port update comes back into MVP 1; PORT-13 stays with Alekseev
- [[wiki/decisions/2026-09-24-written-records-go-by-email-and-chats-are-for-instant-matters.md]] — Sept-28 update: no private chats; long-term questions by email in one thread
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] — the MVP 1 series timeline (Sept 28, 8:02 AM entry): the PIN question, the update dashboard, brackets, MVP 2
- [[wiki/topics/test-automation-strategy.md]] (Sept 28, 8:02 AM) — autotests to about October 23; Vladimir joins; tests written with Claude
- [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]] — Sept-28 update: Pavel does the Wi-Fi software, about 90%; capability 145 stays MVP 2
- [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] — Sept-28 update: Anton's emulator sits inside FlexPay and must move to Flex IQ
- People: [[wiki/people/andrei-klimovich.md]] · [[wiki/people/val-levitan.md]] · [[wiki/people/pavel.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/evgeniy-alekseev.md]] (discussed, not present) · [[wiki/people/elizabeth.md]] (discussed, not present) · [[wiki/people/ivan.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/anton-seregin.md]]

**§4 name calls** [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]:

- "Андрей" to whom Chudinov will send the negative-case document, and who asks about Georgia = Klimovich, by context; Chudinov also says "климович Андрей" once. "Андрей, сможешь Элизабет зайти через центр" = Bosik (he answers).
- "дима" = Chudinov (Pavel addresses him; he answers). "Паша" = Pavel. "Лёша" = Khamin. "Ваня" = Ivan. "саша" = Biratka. "Владимира" = [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], by context (autotests; the stand-up plan the same day).
- "Сергей", working on wallet creation on the Flex-Port = [[wiki/people/sergey-tsymanov.md|Tsymanov]], by context (his stand-up report the same day). "Андреева Сергея" / "Сергей, если роли уже внедрил" (who knows the dashboard roles) — **not resolved**; nothing ties it to Tsymanov.
- "Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (surname; firmware and Wi-Fi hardware fit his registry role). "Элизабет" = [[wiki/people/elizabeth.md|Elizabeth]], the Georgia technician. "Антон", who builds the emulators = [[wiki/people/anton-seregin.md|Anton Seregin]], **inference** (the emulator work on his page).

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]):

1. **Who proposed "always ask for a PIN".** The notes credit Chudinov. In the transcript Klimovich first proposed it: with two active gateways at a location, "при создании нового волета на порте в любом случае запрашиваем пин код". Chudinov then proposed to fix it as a rule for every wallet.
2. **The hidden PIN.** The notes give "1111". Pavel said "4 единицы, например там всегда 1234", and later "вводится 4 единицы" — both forms were spoken.
3. **"MVP1 date is now October 15."** The notes list this as settled. No one declared it in those words. Pavel: "Мы MVP один, например, сдвигаем на 15 октября"; Klimovich: 15 is the real date and October 1 is not achievable; Val asked for "final state 15 октября, если это возможно". Recorded as the new working date, with the wording as spoken.
4. **Autotests vs development.** The notes omit Irina's point that October 23 is for autotests, not development: "это авто тесты это не разработка… она должна закончиться раньше."
5. **Val on email.** The notes omit Val saying Claude can collect all the MVP 2 emails even without a common subject line.
6. **The dashboard.** The notes omit that the device list shows "наши 2 минских терминала флекса айкио".
7. **Val's "47. Ошибки".** Omitted by the notes; the meaning is **unclear** (possibly a count of errors).

**§15.8:** clear. That Klimovich is away until the 12th and Vladimir goes on leave after about 8 days are recorded only as work availability. No pay, rate or personal matter appears. **§15 #9:** no corporate identifier appears. Capability numbers (145, 146), the story PORT-13 and the board name RK3576 are work references.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
