---
type: project
title: The AI project manager and the company second brain — Val's direction (Sept 25 2026), the design and plan of work (Sept 29 2026), owned by Andrey Bosik
date: 2026-09-25
aliases: [AI PM, AI project manager, AIPM, AI проджект менеджер, Design_AI-PM, company second brain, JVL second brain, одна компании секунд брейн, second brain for JVL, Karpathy method at JVL, AI draft tasks in Jira, meeting bot, AI PM persona, transcript collection, глоссарий Лены]
source-count: 6
open-commitments: 0
open-questions: 0
---

# The AI project manager and the company second brain

A JVL initiative, set in direction by [[wiki/people/val-levitan.md|Val Levitan]] on Sept 25 2026 and given a design, an owner and an order of work on Sept 29 2026. Its aim, in Val's words on Sept 29: an AI project manager that "**с нас снимает работу**" — takes work off the team — by creating "таски проперные, без ошибок… в лимитированном количестве… [с]огласно нашим стандартам", fed by one company second brain built from the meeting transcripts [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]. **Owner: [[wiki/people/andrey-bosik.md|Andrey Bosik]]** (Sept 29). **Next checkpoint: Friday Oct 2 2026, about 7:00 AM** (Val will book it) [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

The rulings are on [[wiki/decisions/2026-09-25-one-company-second-brain-feeds-an-ai-project-manager-for-jira.md]] (the direction) and [[wiki/decisions/2026-09-29-bosik-owns-the-ai-pm-the-meeting-bot-waits-and-the-second-brain-is-built-first.md]] (the plan). This page keeps the whole picture in one place and will carry the timeline as the work moves.

## Timeline

- **Sept 25 2026 (7:33 AM)** — [[wiki/meetings/2026-09-25-ai-project-manager-for-jira.md|"JIRA management AI"]]: Val names the problem (Jira work is stuck because tasks do not reach the right people) and the direction — "Да, давайте создадим одну… компании секунд брейн… По принципу Андрея карпатый… И давайте дадим знания этому [проджект] менеджеру… И давайте его направим на китхаб репозитории." Homework for everyone; meeting Tuesday at 7:00 [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]] [[raw/Meeting_Notes_AI_Project_Manager_for_Jira-September-25-2026.md]].
- **Sept 29 2026 (6:02 AM)** — [[wiki/meetings/2026-09-29-ai-pm-architecture-and-second-brain-plan.md|"Design_AI-PM"]]: Val's picture and Bosik's slides (about 70 % overlap); Bosik takes ownership; the live meeting bot goes to MVP 2; transcripts are collected first and the second brain built from them; drafts go to repository code owners after a dry run; status on Friday [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]] [[raw/Meeting_Notes_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **Sept 29 2026 (10:31 AM)** — a one-minute direction check at the end of the [[wiki/meetings/2026-09-29-dev-environments-rk3568-sdk-amd-spike-and-ai-pm-direction-check.md|"Dev_environments" call]]: Val, to Pavel and Irina, "Мне кажется, мы на правильном пути мне понравился этот разговор. У вас есть какието резерве по этому поводу? Вы считаете, что мы неправильно идём?" Pavel: "Нет, я уверен, что мы идем правильно. Это может казаться, что это ж нереальное, но нам год назад казалось, что [AI] это чисто помощник… если мы гдето даже во чтото упрёмся то чего сейчас будет нереально, то оно через через полгода станет реально." Irina: "А теперь ещё кто кого ведёт?" No reservations from either; nothing new decided [[raw/Meeting_Transcript_Dev_Environments_AI_PM_Direction_Check-September-29-2026.md]] [[raw/Meeting_Notes_Dev_Environments_AI_PM_Direction_Check-September-29-2026.md]].

## What the AI PM is meant to be (Val, Sept 29)

- **A role like his AI-CFO.** Val uses an AI-CFO "каждый день… [д]овольно успешно"; the more he uses it "тем точнее она сама выполняет функции", it talks with the accounting department and has begun to give him directions ("derchins" — garbled). It is "должность, которая опирается только на факты", and it can be given specialised knowledge. The AI PM would have firm knowledge of Atlassian and of PM "учебники" (textbooks, "не книжки") [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **A member of staff.** It "будет подключаться к тимс на каждом митинге… как… полноценный [employee]"; it listens, "может говорить в натуральном голосе" (ElevenLabs — the notes' reading of "ileevon labs"); it has "свой имя", its own mailbox, and "должен присутствовать на митинге как член компании". People "сможете с ним общаться как с нормальным [employee]" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **Its own vocabulary.** "у нас… смешанный… язык англорусский" — it needs a special vocabulary of products, code names, Jira projects and ticket codes, people's names and nicknames, team slang and short forms, mixed English-Russian — and "Лена сделала хорошую работу на эту тему": the glossary already exists ([[wiki/people/lena.md|Lena Zhukova]], by context; see the Mar-2026 taxonomy work on [[wiki/topics/transcript-knowledge-base-tooling.md]]) [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **Narrow knowledge on purpose.** "я бы делал бы дизайн там где знания[.] [о]чень суженная… только из джира… canfluence… какието учебники как быть PM… [к]омпания… [н]е давать… никакой другой философии… наши стандарты… доступ к коду и к прозе." Bosik's list as he wrote it down: Jira, GitHub code plus prose, PM standards, the standards, meeting transcripts. Val struck "knowledge base" from the list — "я говорю про секонд [брейн]" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **Prepared, and asking questions live.** It "приходит подготовлены" (reads the agenda, looks the topics up), takes notes and catches decisions, and — the part Val most wants — "может спрашивать вопросы… [in] rial time". At first "пока он ещё не подготовленные… будут дурацкие. С этим надо пожить немножко" and tell it which question is wrong and why; later "начинает спрашивать очень хорошие вопросы", especially "если ему не разрешают выйти за рамки его" narrow area. Val's acquaintance runs this live, with voice, in his own business on Grok (unnamed) [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **Daily chores.** Keeps a wiki "как Андрей карпаты ведёт свой секонд брей[н]", adds new words to the vocabulary, every day "файнс [stale] tikets" and chases politely; other duties can be added [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **Close to today's code.** Because prose that correctly describes the code is starting to work (as Val heard from Pavel and Irina), the AI PM must "сильно облакачиваться на тот код и на ту прозу, как и на те [ADR], [к]оторые уже находятся в [GitHub]"; "задачи… должны недалеко отходить от фактической работы, которая проходит сейчас… [н]ам не надо планировать фьючер, который далеко уходит" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **It does the work; it does not write to people.** "нельзя делать… такую архитектуру, чтобы AIPM писал нам. Это нехорошо. Надо, чтобы AI[PM] за нас сделал работу." And the danger he sees in himself: "я имею такую тенденцию очень много публиковать… этот [AI] только дай писать он будет писать без остановок" — so output must be limited [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

## Bosik's proposal (Sept 29)

- **Use what exists.** "У нас есть отчеты, которые формируются ежедневно" — the daily reports can be data for the PM; "3 отчёта у нас получается есть"; plus the glossary (to be extended), the standards and the transcripts [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **Draft tasks within half an hour of a meeting.** Transcript ~10 min, processing 10–15 min → "через полчаса максимум… черновик [з]адач" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **"AI draft" in Jira, accepted or rejected by a person.** Tasks appear in Jira with a draft status, assigned or reported per the scheme; the person corrects, cancels or accepts. The accepting mechanism must be as simple as "согласен, не согласен… чутьчуть отредактировал". Email replies would be "такое себе удовольствие"; a Teams option was his second idea [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **To the code owners.** Each repository has its Jira project and its code owners, so drafts are assigned or reported to them rather than left hanging [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **Cite the transcript time.** Each proposed task should say when in the transcript the topic was discussed, "если вдруг человек захочет сам… [р]еференс посмотреть". Val: good [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **Dry run first.** A week or two with no Jira writes; then write to Jira for a few projects; then widen [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **Where it runs — later.** His first idea was a Jira hook firing a GitHub action; if it is a bot, that needs study. Cloud, a ready subscription or an office PC: "будем решать по ходу действия" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

## The second brain, as the team now understands it

- **Val's distinction.** The archive "это не нолыч[-]бэйс… а это [second brain]". A knowledge base is "те нолочь, которые мы накапливаем… [с]писок знаний"; a second brain is "[ф]актически… [р]азговоры, которые происходили в компании… эти факты… никогда не меняются. И на них строится уже индекс" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **The team's reading.** Pavel could not separate the two; Bosik: the second brain "опирается… на [knowledge base]… более верхний уровень абстракции, где появляются… граф" that finds intersections between topics; Pavel: a classic knowledge base is a database of records, and the second brain adds "хороший индекс, который легко может между разными записями перемещаться". Pavel also reported that an AI says Karpathy's system is a wiki, "совсем не обсидиан"; Bosik: the same thing — indexed text files, with Obsidian adding a graph; Val: Karpathy throws any information in, whereas JVL "пользуемся это как [с]формированный [knowledge base]… нам нужны эти факты". Pavel: Obsidian is "одна из реализаций векторной базы данных" — Val: yes [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **Storage, per Val's Claude.** The sources — "живые транскрипты, которые никогда не меняются" — are kept and accumulated in Obsidian; "местные индексные data" are attached because the files become many, with "лёгкие [database]… [л]окальный" recommended (Val can advise which); the summaries then go to GitHub. Val: "Я могу повторить архитектуру, которая у меня работает на больших файлах". Bosik's counter: Obsidian can use GitHub as its storage anyway [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **Val's own brain, in numbers.** Transcripts over "18 месяцев" (the years are garbled on tape — read as Jan 2025 to June 2026, matching his Sept-25 "с 1 января 2025"; **inference**); processing them took "около месяца" and "около $7000"; from existing transcripts the AI's own work is "гдето неделя", but "[у] меня заняло месяц". It is run in phases, and "каждый квартал я читал формировку [а]нализа этого second b[r]ain, что он понимает, моя компания делает" — a quarterly read of what the brain thinks the company does, which he had to confirm [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]. *(This wiki is that brain; recorded here as a JVL fact like any other, from the tape.)*

## The blocker: nobody can collect the transcripts

- **Where they are.** Pavel assumed all recordings land on the Microsoft server and Bosik, as admin, can reach them. Bosik: "**[о]ни кладутся к владельцу митинга, у тебя доступ только к твоим расшифровкам**"; as admin "**у меня как [админа] их тоже нету**" — Val, Irina, he and Dima each see only their own. "[н]ам надо построить механизм, чтобы мы могли доставать расшифровки митингов у каждого пользователя, а сейчас из коробки такого механизма не существует." Pavel: SharePoint belongs to the company — surely the admin can? Bosik: the admin "не должен нарушать границы конфиденциальности" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].
- **The old repository does not work.** There is "готовый репозиторий, где сохранялись транскрипты митингов раньше" made by Lena, on GitHub, "но сейчас не актуально, оно не работает, это создавалось… и потом перестала работать" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]. *(The Mar-31-2026 pipeline on [[wiki/topics/transcript-knowledge-base-tooling.md]] is the likely referent — an inference; the tape names only Lena.)*
- **Size is not the issue.** Bosik: transcripts as markdown "ничего не весят… 3 килобайта" [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]].

## Order of work (agreed Sept 29)

1. Collect every user's transcripts into one store (Bosik; Val's sizing 1–2 days).
2. Build the second brain from them, in phases — the longest and most expensive step, started first (about a month).
3. In parallel, design the AI PM's architecture and persona (Val: 2–3 days for the persona).
4. Then the glossary pass: the brain lists the terms it does not understand; the glossary confirms them.
5. Dry run of task drafting with no Jira writes; then "AI draft" tasks in Jira for a few projects; then widen.
6. The live meeting bot (listening, speaking, asking in real time) — MVP 2.

[[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]

## Open items

Commitments and open questions are held on the two decision pages, not duplicated here: [[wiki/decisions/2026-09-29-bosik-owns-the-ai-pm-the-meeting-bot-waits-and-the-second-brain-is-built-first.md]] (Bosik's four work items, Val's booking, the dry run; the transcript period, where it runs, output length, timing) and [[wiki/decisions/2026-09-25-one-company-second-brain-feeds-an-ai-project-manager-for-jira.md]] (Val's offer to have Claude write up his set-up; approvals/versions; cost).

## Related

- [[wiki/topics/transcript-knowledge-base-tooling.md]] — the long ancestry: Aaron's 2025 tools, the Feb-2026 knowledge-graph platform, the Mar-2026 Clayton/Lena transcription pipeline, the Sept-25 ruling.
- [[wiki/projects/jvl-insights-knowledge-base.md]] — the 2024 "JVL Insights" proposal, the earliest ancestor.
- [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] — the daily Jira reports Bosik wants to feed the PM.
- [[wiki/topics/ai-assisted-development.md]] (Sept 29) — Val's two-AI "teacher and implementer" method.

**§15.8:** clear — roles, process and tool economics only; Val's personal remarks to Bosik are not recorded. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]
- [[raw/Meeting_Notes_AI_Project_Manager_for_Jira-September-25-2026.md]]
- [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- [[raw/Meeting_Notes_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]
- [[raw/Meeting_Transcript_Dev_Environments_AI_PM_Direction_Check-September-29-2026.md]]
- [[raw/Meeting_Notes_Dev_Environments_AI_PM_Direction_Check-September-29-2026.md]]
