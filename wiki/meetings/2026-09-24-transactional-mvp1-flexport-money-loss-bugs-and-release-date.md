---
type: meeting
title: Transactional MVP 1 — two lost-money bugs get simple rules, cashier handling of unclaimed money goes to MVP 2, Val floats October 15 and October 1 stays (Sept 24 2026, 8:01–9:11 AM)
date: 2026-09-24
aliases: [Transactional MVP1 CAPs REQs UI/UX Sept 24, MVP1 FlexPort Money Loss Bugs and Release Date, day nine of the MVP1 series, Sept 24 8am transactional call, bugs 349 and 354, October 15 floated, the email-not-chat call]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Transactional MVP 1 — Flex-Port money-loss bugs and the release date (Sept 24 2026)

**Date/time:** September 24 2026, **8:01 – 9:11 AM Eastern** (about 1 hour 10 minutes), from the `**Date:**` header line [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]. **Series:** the Teams session "Transactional MVP1: CAPs, REQs, UI/UX" — the **ninth** morning call, the day after [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept 23]]. **Language: Russian.**

**Who spoke** (speaker labels): [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (shared his screen), [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak") and [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"; joined late) [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].

**Purpose.** Klimovich's final mock-up and two lost-money Flex-Port bugs; cashier screens and service-screen details; the autotest status; the integration repository and commit discipline; and the release date [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search found no other stub citing these files or covering this 8:01 session. The same day's [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|4:46 AM stand-up]] is a different meeting (Val absent, different content). It is a new meeting.

Substance lives on:

- [[wiki/decisions/2026-09-24-a-flex-port-that-dies-holding-money-sends-it-to-unclaimed-and-one-without-a-gateway-goes-out-of-service.md]] — bugs 349 and 354, Val's challenge of the 30-second timeout, cashier handling to MVP 2
- [[wiki/decisions/2026-09-24-written-records-go-by-email-and-chats-are-for-instant-matters.md]] — Val's email-not-chat rule and Klimovich's daily change log
- [[wiki/decisions/2026-09-09-first-transactional-installation-planned-for-october-1.md]] — Sept-24 update: October 15 floated, October 1 kept
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] — the MVP 1 series timeline (Sept 24, 8:01 AM entry)
- [[wiki/topics/test-automation-strategy.md]] (Sept 24, 8:01 AM) — capability features, the terminal test API, test hooks, the integration repository
- [[wiki/decisions/2026-09-15-a-timeout-sends-the-money-to-unclaimed-and-the-player-never-loses-it.md]] — Sept-24 update
- [[wiki/decisions/2026-09-23-open-requirements-are-settled-on-the-call-and-only-slow-ones-are-parked.md]] — Sept-24 (8:01 AM) update: two of the lost-money bugs get rules
- [[wiki/decisions/2026-09-14-main-branch-must-always-build-and-the-code-belongs-to-the-project.md]] — Sept-24 update: the 300-line commit rule
- [[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]] — Sept-24 update: ADRs in docs, Bosik owns the set-up
- [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]] — Sept-24 update
- [[wiki/decisions/2026-09-11-mvp1-goes-with-flex-iq-alone-and-one-kiosk-per-location.md]] — Sept-24 update: the date question
- People: [[wiki/people/val-levitan.md]] · [[wiki/people/andrei-klimovich.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/ivan.md]] · [[wiki/people/alexander-biratka.md]]

**§4 name calls** [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]:

- "Андрей" who shows the mock-ups and rules on the bugs = Klimovich, by context; "Андрей климович" and "климович" are named by Val. "Андрей босик" = Bosik (named in full).
- "дима", "Дима", "димы чудинова" = Chudinov (named; he answers). "Паша" / "Павел" = Pavel. "Ира" / "Ирина" = Irina. "ваня" = Ivan. "лёша" / "Алексей хамин" = Khamin. "саша пиратка" / "Пиратка" = Biratka (the speaker label fixes it).
- "Вера", whom Chudinov asks "сколько времени мы… полагаем?" — **not resolved**; no Vera is on the call, so it is read as a garble, not a person.
- "genadis hate", where Val tells people to push code — read as GitHub (**inference**: he says "китхаб" in the same passage). It is not [[wiki/people/genadi-peari.md|Genadi]].

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]):

1. **"4–5 features each".** The transcript has "кополлити 24 штуки на каждое по 45 фич" — either 4–5 or 45 per capability. **Unclear.**
2. **"FIG-56", "due today", "fixed during the call".** The transcript renders the task as "Фик фик 56", "Фик вам 56", "фиг 56" — the prefix is the notes' reading. Chudinov's "Он будет сегодня сделан?" is transcribed as a question. That he fixed the missing start dates on the call is **not clear** from the transcript ("Сейчас я посмотрю… сделаю").
3. **"Software version and serial number".** Pavel's words are "Снизу будет добавляться версия и serger" — "serial number" is the notes' reading (**inference**).
4. **The release date.** The notes' account holds. They omit Irina's estimate that full coverage is counted in weeks, and Val's "максимум 4 недели, правильно?", which she accepted.
5. **Omitted by the notes:** Chudinov's first, time-based rule for bug 349; Klimovich's option to lengthen the 30-second wait to one minute; Val's "Это очень хорошая" on Pavel's nearest-wallet idea; Klimovich's review of the NFR collection; Bosik's point that Flex IQ should show the build version only in service modes; Val's "Это может быть 10 раз в день" on commits.

**§15.8:** one passage withheld — at the start Pavel explained why a colleague was late; it concerns a personal legal matter and is not recorded. Val's joking lines about who "let the team down" over the date are banter, not a judgement, and are not recorded. No pay or rate appears. **§15 #9:** no corporate identifier appears. Bug numbers 349 and 354, task "56" and "Fort 47" are work references.

## Sources
- [[raw/Meeting_Notes_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
