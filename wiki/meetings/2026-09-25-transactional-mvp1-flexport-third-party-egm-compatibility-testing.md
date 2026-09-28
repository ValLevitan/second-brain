---
type: meeting
title: Transactional MVP 1 — how Flex-Port will be tested in other makers' machines, the TransAct printer, and autotests after October 7 (Sept 25 2026, 8:05–8:50 AM)
date: 2026-09-25
aliases: [Transactional MVP1 CAPs REQs UI/UX Sept 25, MVP1 FlexPort EGM Compatibility Testing, day ten of the MVP1 series, Sept 25 8am transactional call, third-party EGM compatibility test, cota EGMS capability, transactional distribution list]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Transactional MVP 1 — Flex-Port compatibility testing with other makers' machines (Sept 25 2026)

**Date/time:** September 25 2026, **8:05 – 8:50 AM Eastern** (about 45 minutes), from the `**Date:**` header line [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]. **Series:** the Teams session "Transactional MVP1: CAPs, REQs, UI/UX" — the **tenth** morning call, the day after [[wiki/meetings/2026-09-24-transactional-mvp1-flexport-money-loss-bugs-and-release-date.md|Sept 24]]. **Language: Russian.**

**Who spoke** (speaker labels): [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (chair), [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]] (shared the Jira plan), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak") and [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin") [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]].

**Purpose.** Klimovich's daily update and a mailing list for his report; how Flex-Port is tested with other makers' machines; the Monday build and the printer; Klimovich's week away; the Jira plan; the autotests [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search found no page citing either file. The same day's [[wiki/meetings/2026-09-25-daily-standup-engineering-menu-and-jira-discipline.md|Minsk stand-up]], [[wiki/meetings/2026-09-25-ai-project-manager-for-jira.md|7:33 AM Jira-AI call]] and [[wiki/meetings/2026-09-25-games-conversion-repos-jira-capabilities.md|9:02 AM games-conversion call]] are different meetings (different times, people and content). It is a new meeting.

Substance lives on:

- [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] — Sept-25 update: the test set-up, office not warehouse, JVL machines first, after October 1, Ivan's instruction
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] — the MVP 1 series timeline (Sept 25, 8:05 AM entry)
- [[wiki/topics/test-automation-strategy.md]] (Sept 25, 8:05 AM) — autotests after October 7, the test API works, the test repository structure
- [[wiki/decisions/2026-09-23-jvl-stops-building-its-own-tito-desktop-box-and-uses-jcm-or-transact-for-now.md]] — Sept-25 update: the TransAct unit with an Epic 950 inside, Val's approval of Genadi's board change
- [[wiki/decisions/2026-09-09-first-transactional-installation-planned-for-october-1.md]] — Sept-25 update: development planned to October 7
- [[wiki/decisions/2026-09-17-jvl-supports-multiple-incomm-products-not-a-fixed-pair.md]] — Sept-25 data point: 178 still on the Jira plan
- People: [[wiki/people/andrei-klimovich.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/ivan.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/elizabeth.md]] (named as the likely tester) · [[wiki/people/val-levitan.md]]

**§4 name calls** [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]:

- "Андрей" who gives the update, and to whom Bosik will send the list name ("я тебе Андрей скину") = Klimovich, by context. "Андрей в отпуске" (Chudinov) = Klimovich.
- "дима" in the Jira review ("дима когда возьмётся", "А это на диме") and in Khamin's "Это вот дима делал" (the test API) = Chudinov, **by context** (the test API is his task from Sept 24).
- "ваня" / "Ваня" = Ivan. "лёша" = Khamin. "саша" = Biratka. "Паш" = Pavel.
- "Элизабет" = [[wiki/people/elizabeth.md|Elizabeth]], the Georgia technician, by context. "геназию" / "Геннадием" = [[wiki/people/genadi-peari.md|Genadi Peari]].
- For the mailing list: "Сергея цимонова" = [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]]. "Владимир" read as [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] (**inference**; Flex-Port front-end work). **"Антон" is not resolved** — none of the three Antons clearly fits. **"женя"**, added so he can answer machine-side questions ("Со стороны машины"), is **not resolved** between the Zhenyas; Bosik said "женя ш вроде транзакционной не занимается". Both queued, not forced.
- "Татьяна у нас", said once during the Jira review — no Tatyana is on the call; read as a garble, not a person.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]):

1. **"2 days".** Klimovich says operators may lend machines "на. День 2" and "нам надо день 2" — read as "a day or two" (день-два). The notes write a flat "2 days".
2. **The capability's wording.** Pavel said "флекспорт должен иметь возможность работать с cota EGMS". The notes write "third-party EGMs". "cota" is **unclear** as spoken; "other makers' machines" is the meaning by context (**inference**).
3. **Capability 178.** The notes omit Irina's "Так а 178 кудато?" and "А это на диме" in the Jira review.
4. **The printer.** The notes omit Val's "У них уже готовый taybeltop" (read as table-top; **inference**).
5. **Decisions list.** The notes list "office, not warehouse" as a group decision. In the transcript it is Pavel's proposal plus a hybrid (one or two machines first, then warehouses), and Klimovich's summary to bring machines to the office and connect them to the MikroTik. No vote was taken.
6. **The Monday build.** Chudinov said "наверное, в понедельник" (probably Monday); the notes drop the "probably".

**§15.8:** clear. Opening small talk and jokes about Klimovich's trip are not recorded. That he is away next week is recorded only as work availability. No pay, rate or personal matter appears. **§15 #9:** no corporate identifier appears. Jira numbers 67, 156 and 178 and the printer model are work references.

## Sources
- [[raw/Meeting_Notes_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]
