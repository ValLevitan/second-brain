---
type: meeting
title: NOVA and GALAXY state of affairs — capabilities go into one flat list, releases become timeline lines, the product IP layer is removed, and "omni" repositories become "nova" (Sept 24 2026, 10:00–11:31 AM)
date: 2026-09-24
aliases: [NOVA and GALAXY state of affairs, NOVA GALAXY Jira Hierarchy Cleanup, Sept 24 10am hierarchy call, Core value stream call, omni to nova repo rename]
source-count: 2
open-commitments: 0
open-questions: 0
---

# NOVA and GALAXY state of affairs — Jira hierarchy clean-up (Sept 24 2026)

**Date/time:** September 24 2026, **10:00 – 11:31 AM Eastern** (about 91 minutes), from the `**Date:**` header line [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]. **Language: Russian.**

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]] (shared the Jira screen), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko") and [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik") [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].

**Purpose.** Val called it to check that Jira for NOVA and Galaxy follows the agreed standards, and to fix where the team drifts [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. The day's other stubs (4:46 AM stand-up, 5:41 AM Georgia hard resets, 7:02 AM RIS, 8:01 AM transactional MVP 1) are different meetings with different times and content. No wiki page cited these files before. It is a new meeting.

Substance lives on:

- [[wiki/decisions/2026-09-24-capabilities-sit-in-one-flat-list-under-each-platform-and-releases-are-timeline-lines-not-initiatives.md]] — the rulings, the debate, the undertakings and the open Galaxy question
- [[wiki/topics/github-release-management-pipeline.md]] (Sept 24 2026 section) — the hierarchy-standard thread
- [[wiki/topics/nova-platform-architecture.md]] (Sept 24 2026 section) — no Galaxy work yet, the omni→nova repository rename, LGS prose without requirements, the NOVA product-manager question
- [[wiki/decisions/2026-09-10-per-product-components-and-mvp-fix-versions-on-the-capability-project.md]] — Sept-24 update: MVPs are releases, not initiatives
- [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] — Sept-24 update: grooming handed to Kovalchuk
- [[wiki/decisions/2026-08-26-pavel-irina-own-nova-capabilities-to-jira-through-september.md]] — Sept-24 update: Biratka and Chudinov move their own capabilities
- [[wiki/decisions/2025-04-07-recarve-gaming-platform-into-six-product-repos.md]] — Sept-24 update: where IP481 now sits
- People: [[wiki/people/val-levitan.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/evgeny-kharetski.md]] (in absentia)

**§4 name calls** [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]:

- "дима Ковальчук" (named in full by Val) = Kovalchuk. "дима чудинов" / "дыма" / "Дима" in the cross-repository argument = Chudinov. "Саша" / "Александр" / "биратко" = Biratka. "Андрей босик" (named in full by Val) = Bosik. "Паш" / "Павел" = Pavel.
- "женя", who will write the manifest in the integration repository = [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], **inference** by context: he took the lead on populating the NOVA integration repository on Sept 3. Not a speaker here.
- "Даниил" (a build a rename may touch), "Лена" (the game team found a per-product view useful) and "нэйтан" (who fixes only billing) — named in passing; not linked, no substance recorded.
- "Андрей" inside Bosik's made-up bug example ("Андрей говорит, вот там на этом экране…") is a hypothetical, not a person reference.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]):

1. **Deadline weekday.** The notes give Biratka's and Chudinov's deadline as "Thu Sep 25, 2026 (morning)". The transcript says "за завтра за утром" (tomorrow morning). Sept 25 2026 is a **Friday**, not a Thursday.
2. **Kovalchuk's report date.** The notes say "by Tue Sep 29". In the transcript Val asked for Monday evening ("отпишите нам в понедельник") and Kovalchuk answered "Давайте во вторник." Only the weekday is spoken; the Sept 29 date is a calendar inference.
3. **"Pavel — rename IP-481 / IP-1204".** Not stated as an undertaking in the transcript. Pavel edited items live during the call ("Так и я тогда вот это." … "Удаляю."); Irina moved items herself during the call ("Всё, они все там").
4. **"All attendees tag features with the release".** In the transcript this is Pavel's proposal only ("давайте дадим задание всем присутствующим"); no clear assignment follows.
5. **Core and Tools.** The notes say plainly that IP-1204 becomes Core and IP-738 becomes Tools. In the transcript Val first said to destroy 1204 ("Если вы уничтожите 12, 04") and later "IP 481 должен идти под 738"; Pavel objected that 738 is helper tools; Val said to call them Tools; Pavel said "Назовем это кор". Which item ends up named Core is not fully clear.
6. **Omitted by the notes:** Val's view of a value stream as a profit or expense centre; Val's idea that LGS, the framework and each game be Jira components (Pavel: they are already projects); Kovalchuk's note that Jira now calls projects "spaces"; Bosik's forward-fix point (a hot fix outside a planned release); Chudinov's remark that Claude reads Jira well for MVP 1; Val's remark that CMS leaves and Galaxy "приходит на её место" (transcript "SMS", read as CMS — inference).
7. **"IP-1096 set".** The transcript has "IP которая 10 30 96" — garbled. The notes' reading "1096" is plausible but an **inference**.

**§15.8:** two passages withheld. (a) Val's remarks on who would or would not make a good NOVA product manager — personal suitability judgements about named people; only the organisational point ("NOVA needs a product manager; for now probably Pavel") is recorded. (b) Banter about Val's shirt — not recorded. No pay or rate appears. **§15 #9:** no corporate identifier appears; IP numbers are Jira work references.

## Sources
- [[raw/Meeting_Notes_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
