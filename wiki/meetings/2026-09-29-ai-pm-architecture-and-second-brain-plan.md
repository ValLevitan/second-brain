---
type: meeting
title: "Design_AI-PM" — Val's picture of an AI project manager, Bosik's draft-tasks-in-Jira proposal, second brain vs knowledge base, transcripts nobody can collect, and "no bonus — Friday at 7" (Sept 29 2026, 6:02–6:56 AM)
date: 2026-09-29
aliases: [Design_AI-PM, AI PM Architecture and Second Brain Plan, Sept 29 AI PM call, AI PM design meeting, AI project manager architecture, second brain plan, AI draft status in Jira, dry run without Jira, meat proxy, мясное прокси, teacher and implementer, учитель и имплементор, Friday at 7 status]
source-count: 2
open-commitments: 0
open-questions: 0
---

# "Design_AI-PM" — the AI project manager's architecture and the second-brain plan (Sept 29 2026)

**Date/time:** September 29 2026 (a Tuesday), **6:02 – 6:56 AM Eastern** (about 53 minutes), from the `**Date:**` header line [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]. Teams session "Design_AI-PM". **Language: Russian**, with many English terms spoken and badly rendered. This is the Tuesday-7:00 follow-up that the [[wiki/meetings/2026-09-25-ai-project-manager-for-jira.md|Sept-25 "JIRA management AI" call]] set (it started at 6:02, not 7:00, by the header).

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]] (organizer; ran it), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"; presented his own slides), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

**Purpose.** Val: "чтобы мы обсудили поверхностно архитектуру, как будет работать… AI PM" — a first pass at how the AI project manager will work; everyone had homework from Sept 25. Bosik had prepared a presentation that "пересекается на процентов 70" with the file Val sent, and walked through the differences [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. A corpus-wide grep for both filenames, "Design_AI-PM", "6:02 AM" and "мясное прокси" found no page citing either file and no other stub for this call. The same morning's [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|4:49 AM Minsk stand-up]] is a different meeting (Pavel's stand-up, other attendees, other subject). It is a new meeting.

Substance lives on:

- [[wiki/projects/ai-project-manager-and-company-second-brain.md]] — the project page: the picture, Bosik's proposal, the plan of work and its order, who owns what
- [[wiki/decisions/2026-09-29-bosik-owns-the-ai-pm-the-meeting-bot-waits-and-the-second-brain-is-built-first.md]] — the rulings of this call
- [[wiki/decisions/2026-09-25-one-company-second-brain-feeds-an-ai-project-manager-for-jira.md]] — Sept-29 update: homework delivered; the open questions moved on
- [[wiki/topics/transcript-knowledge-base-tooling.md]] (Sept 29) — second brain vs knowledge base; where the transcripts are and why nobody can collect them; Obsidian vs GitHub; Val's own second brain in numbers
- [[wiki/topics/ai-assisted-development.md]] (Sept 29, 6:02 AM) — Val's "teacher and implementer" way of working with two AIs, and "act as if you know nothing"
- People: [[wiki/people/val-levitan.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/lena.md]] (discussed, not present)

**§4 name calls** [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]:

- "Андрей" = Bosik (speaker; the only Andrei on the call). "Паша" / "Павла" = Pavel Frolov. "Ирины" / "Ирина" = Irina Shishko. "дима" ("то, что дима озвучил") = Kovalchuk (speaker; he raised the point). "Лена" — who made the glossary ("Лена сделала хорошую работу") and the earlier transcript repository ("раньше лены") = [[wiki/people/lena.md|Lena Zhukova]], **by context** (the Mar-2026 taxonomy/glossary work on her page and on the transcript-tooling topic) — inference.
- "Андрей карпаты" / "карпаты" = Andrej Karpathy, the outside AI researcher — **not a JVL person**.
- "мой товарищ в своём бизнесе" — Val's acquaintance who runs a live voice bot with Grok — **unnamed**; not recorded as a person.
- Product names as heard: "эйсиэфо" = AI-CFO (Val's own executive persona); "Грок" = Grok; "антропик" / "клод" / "клот" / "плод" = Anthropic / Claude; "ileevon labs" / "leven лабс" = ElevenLabs (the notes' reading; **inference**); "атлас" = Atlassian (**inference**); "обсидиан" / "обсидин" = Obsidian; "гетхаб" / "китхаб" / "в Китае" = GitHub; "жира" / "джира" / "Джерри" = Jira. "rics oo chipary ofs" (what Val says he is now setting up for himself) — **unclear**, not interpreted.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]):

1. **"18 months of transcripts".** The notes say Val's own brain took "about a month and about $7,000 for 18 months of transcripts". The transcript's years are garbled — "с 2003 года… с января 2005… июнь месяц 2006… за 18 месяцев"; the 18-month span is spoken, the years are read as January 2025 to June 2026 (**inference**, matching his Sept-25 "с 1 января 2025").
2. **"Collection 1–2 days".** The notes give it as Val's estimate; so does the transcript ("около дня. 2 дней, но это приблизительно").
3. **"Status review on Friday (Oct 2)".** The transcript has "В пятницу я назначу митинг гдето на 07:00"; the date is worked out (Sept 29 2026 is a Tuesday), not spoken.
4. **Omitted by the notes:** Val's closing instruction to the transcript itself — "для транскрипта я попрошу, чтобы не обращать внимание на то, что было сказано раньше по поводу как применять [AI]" — asking that what he had said about how to apply AI (the two-AI method) be left out. Recorded here so the owner can rule; the method is kept, in short, on [[wiki/topics/ai-assisted-development.md]] because it is his standing practice (see Problems).
5. **Omitted by the notes:** Pavel's point that an AI reports Karpathy uses a wiki, not Obsidian, and the exchange that followed; and Val's remark that the AI PM "должен иметь свой мейл бакс" is in the notes, but Pavel's "И в отпуск мы тоже будем отпускать" and the persona banter that followed are chatter and not recorded.
6. **"Val estimated collection… his own took about a month".** Both files agree; the transcript also has Val first saying the second brain from existing transcripts "займет гдето неделя. Просто неделя самого [AI]" and then "У меня заняло месяц" — both figures are recorded on the project page.

**§15.8:** withheld — Val's remarks on how Bosik presents himself ("Вы хотите показать, что вы всё знаете") and his general aside on "умных людей" are personal judgements and are not recorded; his political aside is not recorded. The method point ("act as if you know nothing; do not set the tone") is recorded. No pay or personal matters. **§15 #9:** no corporate identifier appears; "$7,000" is Val's own tool spend, a cost figure, not an identifier.

## Sources
- [[raw/Meeting_Notes_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
