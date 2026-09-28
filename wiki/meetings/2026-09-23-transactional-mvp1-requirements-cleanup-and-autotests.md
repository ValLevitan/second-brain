---
type: meeting
title: Transactional MVP 1 — the UI/UX package lands in Jira, open requirements are settled live, and the first autotests come back half manual (Sept 23 2026, 8:00–9:18 AM)
date: 2026-09-23
aliases: [Transactional MVP1 CAPs REQs UI/UX Sept 23, MVP1 Requirements Cleanup and Autotests, day eight of the MVP1 series, Sept 23 8am transactional call, the symlink to dev null call, REQ-753 deleted]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Transactional MVP 1 — requirements clean-up and autotests (Sept 23 2026)

**Date/time:** September 23 2026, **8:00 – 9:18 AM Eastern**, from the `**Date:**` header line [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]. **Series:** the Teams session "Transactional MVP1: CAPs, REQs, UI/UX" — the **eighth** morning call, the day after [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept 22]]. **Language: Russian.**

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]] (shared the requirement list), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin") and [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak") [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

**Purpose.** Four blocks: Klimovich's UI/UX package in Jira; a live pass over about 12–13 requirements that still carried open questions; the result of the one-hour autotest set the day before; and a last Jira pass on the new capabilities [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. The same day's other transactional stub, [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md]], is a different meeting (4:48 AM stand-up, Val absent, different content). A corpus-wide search found no other stub citing these files or covering this 8:00 session. It is a new meeting.

Substance lives on:

- [[wiki/decisions/2026-09-23-open-requirements-are-settled-on-the-call-and-only-slow-ones-are-parked.md]] — the requirement rulings (REQ-753, disconnect timeouts, PIN lockout, CAP-173, REQ-1550, plain-English rule, forfeit wallet)
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] — the MVP 1 series timeline (Sept 23, 8:00 AM entry)
- [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]] — Sept-23 update: what the micro-step produced
- [[wiki/topics/test-automation-strategy.md]] (Sept 23, 8:00 AM) — the symlink method, the money-crediting test, where tests live
- [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]] — Sept-23 (8:00 AM) update: 234, 235, 180, 230, 231, 173
- [[wiki/decisions/2026-09-17-jvl-supports-multiple-incomm-products-not-a-fixed-pair.md]] — Sept-23 update: 178 still being planned
- [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]] — Sept-23 update: the status flow restated
- [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] — Sept-23 (8:00 AM) update: the FlexPay emulator is to be copied for Flex IQ
- [[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]] — Sept-23 update: the file-naming standard
- [[wiki/decisions/2026-09-23-capability-118-is-split-by-product-and-two-devices-keep-two-repositories.md]] — Sept-23 (8:00 AM) update: Irina's report of the split
- People: [[wiki/people/val-levitan.md]] · [[wiki/people/andrei-klimovich.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/ivan.md]]

**§4 name calls** [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]:

- "Андрей" who shows the UI/UX capabilities, rules on PIN lockout and owns the status flow = Klimovich. "Андрей босик", named in full by Irina and Val as author of the long requirements = Bosik.
- "дима" / "Дима" = Chudinov (he answers). "Саша" = Biratka. "Лёша" / "Алексей" = Khamin. "Иван" / "ваня" = Ivan (label "Ivan Shpak"; no surname spoken).
- "Антон", who is finishing the FlexPay emulator = [[wiki/people/anton-seregin.md|Anton Seregin]], **inference** — same work he reported at the 4:48 stand-up that day. Not a speaker here.
- "Владимир", who gets the Flex-Port capability = [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], **inference** — he took the Flex-Port screen redraw on Sept 22.
- "Сергей", who "делает" the Flex-Port switching work (REQ-1413) — **not resolved**; no surname.
- "свалом Геннадием и Дмитрий ковальчуком" — Pavel reading names quoted inside REQ-1550's text (Val, Genadi, Dmitri Kovalchuk). They are names in a document, not attendees.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]):

1. **Fluent Bit and 500 MB.** The notes say "Fluent Bit with a default buffer of roughly 500 MB". The transcript has "Влюньбит дефолтная настройка. Я не помню сколько там мегабайт помоему 500 или сколько". Reading the garble as Fluent Bit is an **inference**; the size is Chudinov's uncertain recollection.
2. **"Server capacity".** The notes say the real ceiling on Flex-Ports per terminal is server capacity. The transcript has "сколько оплата потянет" — garbled; what the limit is was **unclear**. Only "отдельный стресс тест" is clear.
3. **"A developer must not close it".** The transcript has "Без разрешения к и родок точно не должен это сделать" — garbled. The notes' reading is plausible but an **inference**.
4. **REQ-1550 "decided by Andrei Bosik".** In the transcript Bosik states the need ("наш терминалы смотрят в интернет, соответственно, они должны быть защищены"); Klimovich asked whether a minimal set could come first, and got no clear answer.
5. **Omitted by the notes:** Irina's report that two capabilities mixing FlexPay and Flex IQ were split, FlexPay going to MVP 2; REQ-1412 (per-Flex-Port log data), which Bosik said "можно вообще просто убрать"; Pavel's remark that the Flex IQ side of 230/231/234 will be ready but "серверная часть это, наверное, уже будет после… м в п один"; Chudinov's preference to close one business topic at a time (card activation) rather than split work across products; Bosik's point that tests will live in the integration repository and that the standards answer half of Khamin's questions.

**§15.8:** two passages withheld. (a) Val's criticism of one named engineer for not asking for help — a personal performance judgement; only the team-level instruction ("не работайте в вакууме") is recorded. (b) A sharp exchange between Val and Klimovich about progress ("медали") — interpersonal; not recorded. No pay or rate appears. **§15 #9:** no corporate identifier appears. Capability, requirement and repository references (CAP-144, 173, 178, 180, 230, 231, 234, 235; REQ-753, 1412, 1413, 1416, 1429, 1550, 1560–1565, 1603) are work references. No phone number was spoken.

## Sources
- [[raw/Meeting_Notes_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
