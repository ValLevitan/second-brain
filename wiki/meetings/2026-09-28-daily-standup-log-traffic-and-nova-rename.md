---
type: meeting
title: Daily stand-up — log traffic of about 3 GB a month, the Omni-to-NOVA rename, Syncotek first, and "name your CAP and feature" (Sept 28 2026, 4:56–5:29 AM)
date: 2026-09-28
aliases: [Daily Standup meeting Sept 28 2026, Daily Standup Log Traffic and NOVA Rename, Sept 28 stand-up, log traffic, 120 MB a day, three gigabytes a month, Omni renamed NOVA, try Syncotek first, capability 235 engineering menu requirement, Dragon Rain]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — log traffic and the NOVA rename (Sept 28 2026)

**Date/time:** September 28 2026 (a Monday), **4:56 – 5:29 AM Eastern** (about 33 minutes), from the `**Date:**` header line [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up.

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (ran it), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], and [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"; joined at the end) [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]. Val was not present.

**Purpose.** Round-the-table status, then two short announcements: Kovalchuk on the Jira reports, and Bosik on the Omni-to-NOVA rename [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search found no page citing either file and no other Sept-28 stand-up stub. The same day's [[wiki/meetings/2026-09-28-transactional-mvp1-remote-updates-and-october-15-target.md|8:02 AM MVP 1 call]] is a different meeting (different time, chair and content). It is a new meeting.

Substance lives on:

- [[wiki/topics/nova-platform-architecture.md]] (Sept 28) — everything named Omni is now named NOVA; pull requests wait for the repository maintainers
- [[wiki/decisions/2026-09-17-signal-quality-in-mvp1-means-remote-visibility-not-a-screen.md]] — Sept-28 update: logs and metrics use about 120 MB a day, a bit over 3 GB a month; junk logs can be cut
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 28, 4:56 AM) — card dispenser tries Syncotek first; the engineering menu goes under capability 235; the latest Flex-Port build goes on a real machine
- [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] — Sept-28 update: two daily Jira reports; say the exact CAP and feature at stand-ups
- [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] — Sept-28 update: Seregin's plan to move the emulator to Flex IQ
- [[wiki/topics/test-automation-strategy.md]] (Sept 28, 4:56 AM) — the cash-out autotest, the deposit test barely started, quick endpoint tests in the build
- [[wiki/decisions/2026-09-17-jvl-supports-multiple-incomm-products-not-a-fixed-pair.md]] — Sept-28 data point (a garbled capability number)
- People: [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/ivan.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/alexei-khamin.md]]

**§4 name calls** [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]:

- "саши" / "саша" = Biratka. "Алексей" = Khamin. "Антон" called on = Seregin (he answers). "Даниил" = Daniil Stauskiy. "зима" called on after Daniil = Chudinov (garble of "Дима"; he answers). "женя" called on = Kharetski (he answers). "ира" = Irina. "ники иван" / "ванино" = Ivan. "Сергей" = Tsymanov. "Владимир" = Samusenko. "дима" at the end = Kovalchuk (he answers).
- "с Андреем" (Chudinov aligned product-terminal names for updates with him) = [[wiki/people/andrey-bosik.md|Bosik]], **by context** (builds and updates are DevOps work). "Андрею сказать" (whom Chudinov will tell about the log traffic) — **not resolved** (Bosik or Klimovich). "Мне Андрей чтото там кап какойто вроде кидал" (Ivan, about his instruction) = [[wiki/people/andrei-klimovich.md|Klimovich]], **by context** (on Sept 25 Klimovich was to open a capability and Ivan to write the set-up instruction).
- "дима 50 на 50" (Kovalchuk: only Sasha named his CAP; "Dima" half did) = Chudinov, **inference** (he gave capability numbers in his report).
- "Игорь", who has a game-select screen and makes games that are "не класс 3" — **not resolved** between the Igors. "Антон", who fixed service gaps for Kharetski — **not resolved** (Seregin or Leshkevich). Both queued, not forced.
- "аккумулятор" in Seregin's and Khamin's reports is read as the emulator ("эмулятор") — **inference**, from the Sept-23 to Sept-25 emulator plan on Seregin's page.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]):

1. **Kharetski's move.** The notes say he "moved the data center to LGS over the weekend". The transcript has "за выходные справился" but then "Сейчас я закончу с переносом и буду внедрять дальше сервисы" — he will finish the move, then add services. So it is not fully done. "Дотацентра" and "за 3 года" are **unclear** words.
2. **Sergey's next task.** The notes say its name is not clear. The transcript has "создания воли через… Экспорт"; the [[wiki/meetings/2026-09-28-transactional-mvp1-remote-updates-and-october-15-target.md|8:02 AM call]] the same day places Sergey on wallet creation on the Flex-Port, so that is the reading (**inference**).
3. **Ivan's second priority.** The notes say "review drafts sent on Friday, certificates expected today". The transcript has "драфты посмотреть по виквау… должны сертификаты сегодня дать по gom 3" — the names are **unclear**; not interpreted.
4. **Omitted by the notes:** Chudinov's line on the card dispenser ("Ардиспенсерфлекса кю не будет это осталось на бутагусе" — garbled); and a capability number in his report, "с продуктами вы побежите 2 с 78" (**unclear** — see the capability-178 page).

**§15.8:** clear. Work status and process only. Nobody's pay, performance or personal matters are recorded. **§15 #9:** no corporate identifier appears. Capability numbers (133, 134, 137, 235, 237), feature numbers (1284–1286), task 16 and the task type TPT-INT are work references.

## Sources
- [[raw/Meeting_Notes_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
