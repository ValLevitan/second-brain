---
type: decision
title: One company second brain feeds an AI project manager for Jira — Val's direction; the design goes to homework for a Tuesday meeting
date: 2026-09-25
aliases: [AI project manager for Jira, AI проджект менеджер, AI Project Manager, company second brain, одна компании секунд брейн, Karpathy method, JIRA management AI, conservative framework, 20 people limit, ESL English prompt]
source-count: 2
status: active
open-commitments: 2
open-questions: 4
---

# One company second brain feeds an AI project manager for Jira

Set by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-25-ai-project-manager-for-jira.md|Sept 25 2026 "JIRA management AI" call]] (Russian), with [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/andrey-bosik.md|Andrey Bosik]] and [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]. It is a **direction**, not a design: how to build it was left to each person's homework.

## The problem Val named

- Work through Jira is not working: "Мы постоянно пытаемся… и у нас не получается нам очень тяжело." The main cause, in Val's words: "мы неправильно делали, кто что делает… Или паше за всех делает или Ирина за свою команду делает. Это неправ." [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]
- The team is small, and good tasks are hard to write. Jira is "очень большой пакет" for JVL, but "мы сейчас не сдвинемся с места" [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].
- There are not enough people to assign to, so Pavel ends up assigning tasks to himself [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].

## Val's three ideas

1. People should assign more and take less on themselves [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].
2. Kovalchuk or Bosik prepare daily reminder reports for everyone who has tasks — perhaps two, one in the morning and one around 12:00, before lunch [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].
3. "самое важное": AI project managers that, working from JVL's standards and the meeting transcripts, create the Jira tasks and write their descriptions themselves [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].

Bosik: points 1 and 2 "уже делаются" — a report already sends each person their own Jira information, and there is a similar mailing for GitHub. Val had seen the report, liked it, and said it will work only if tasks are assigned to the right people. See [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Sept-25 update) [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].

## The direction

> "**Да, давайте создадим одну.**" … "**Давайте Владимир компании секунд брейн.**" … "**По принципу Андрея карпатый.**" … "**И давайте дадим знания этому прочих менеджеру.**" … "**И давайте его направим на китхаб репозитории.**"
> [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]

*("Владимир" and "прочих" are speech-to-text garbles; the sense — one company second brain, and the project manager — is clear from the lines around them.)*

In plain terms:

- **One company second brain**, built the way Andrej Karpathy describes (Claude reads all the text and builds a wiki with indexes), in place of each person's own local knowledge base. Pavel raised the gap: "у каждого это база знаний, своя", so knowledge from meetings a person missed does not reach them. Pavel and Bosik confirmed they record their meetings [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].
- **The AI project manager** gets specific domain knowledge and is pointed at the **GitHub repositories**; it sees the transcripts, the repositories and all the tasks, and "может понять, чего не хватает" (Kovalchuk and Bosik) [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].
- **A conservative framework.** "Расскажем, что в компании работает только 20 человек. У нас есть лимит" [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].
- **ESL English.** The prompt must tell it to write in English for people for whom English is a second language; Val uses this himself and asks for replies of no more than 30 seconds of reading [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].

Pavel: "Ну да, выглядит." No one objected to the direction [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].

## Options discussed, none adopted

- **Assign Jira tasks straight to Claude** (Kovalchuk): Claude takes the task's context, goes to the repository, tries the work and opens a pull request. He said JVL once tried to connect this and it stalled. Bosik: the function exists "но он страшно". Irina: it must be set up perfectly first, or "он нас задушит". Val: review takes time too; a good step but "очень глубокий, нам её надо разобраться". Pavel: "Радикальный". Kovalchuk: he did not mean all tasks at once [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].
- **A person approves before Claude writes to Jira** (Val): Claude helps the responsible person draft the tasks, the person approves, then Claude puts them in Jira — "ещё одна… хьюман инстанция" [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].
- **Gaps confirmed by email** (Bosik): when the manager finds a gap, it emails the task owner; the owner replies which points to accept; then it creates the Jira task [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].
- **Gaps confirmed by pull request** (Val): the proposed text goes as a pull request; the responsible person approves it; the merged pull request is the trigger for the AI to change Jira. Original transcripts stay frozen in Obsidian ("Они замёрзшие лежа"); only the small summaries go to GitHub, where versions and approvals are easier to see. Kovalchuk: a pull request only changes the repository, and the AI still needs a command to process it; the data will be large and "очень очень дорого". Pavel: Git is "неподходящий инструмент для этого"; Bosik agreed; Kovalchuk pointed to Obsidian or similar [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].
- **How often it runs.** Pavel: at set times, reading, for example, the last day's meetings and finding missing tasks. Val: "Сутки это очень много" [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].
- **It is not a small project** (Bosik): the architecture must be designed first, and getting meeting transcripts out of Azure is hard — "Есть сложности". Val agreed that getting the transcripts and a real return will take time [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].

## What was agreed

- **Homework** (Kovalchuk's proposal, Val: "Хорошо договорились"): each person thinks how they would build the AI project manager — its functions, an algorithm, how it would work — for a group discussion [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]].
- **Next meeting Tuesday at 7:00.** Val offered Monday; Bosik asked for Tuesday; Val: "во вторник в 07:00" [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]. That Tuesday is Sept 29 2026 — the derived notes give this date; it was not spoken [[raw/Meeting_Notes_AI_Project_Manager_for_Jira-September-25-2026.md]].

## Open commitments

- [ ] Val Levitan, Pavel Frolov, Irina Shishko, Andrey Bosik, Dmitri Kovalchuk — each think through how to build the AI project manager (functions, algorithm, how it works) — due Tuesday Sept 29 2026, 7:00 (date worked out) — [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]
- [ ] Val Levitan — if the team wants it, have Claude write up how his own second-brain system is built ("Я могу, если хотите попросить") — due unspecified — [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]

## Open questions

- Where do approvals and versions live — pull requests in GitHub (Val) or Obsidian or similar (Kovalchuk; Pavel and Bosik: Git is the wrong tool)? — [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]
- How does the company get the meeting transcripts out of Teams/Azure (Bosik)? — [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]
- What does it cost to process that much data (Kovalchuk)? — [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]
- How often should it run — daily (Pavel) or more often (Val)? — [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]

## Related

- [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] — the Sept-17 move of planning off Pavel; this call looks for the same relief through AI. *(The link is an **inference**; neither source names the Sept-17 ruling.)*
- [[wiki/decisions/2026-09-09-planning-handed-to-bosik-and-kovalchuk-with-daily-recorded-sessions.md]] — the earlier plan to hand planning to Bosik and Kovalchuk with recorded sessions. *(Link is an **inference**.)*
- [[wiki/topics/transcript-knowledge-base-tooling.md]] — JVL's earlier attempts at a company-wide knowledge base.

**§15.8:** Val's personal praise of Pavel and his view of how much Pavel can manage are not recorded. No pay or other personal matters. **§15 #9:** clear.

## Sources
- [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]
- [[raw/Meeting_Notes_AI_Project_Manager_for_Jira-September-25-2026.md]]
