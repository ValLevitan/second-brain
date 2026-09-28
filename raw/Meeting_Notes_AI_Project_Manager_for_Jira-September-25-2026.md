# Meeting Summary — JIRA management AI
**Date:** September 25, 2026, 7:33 AM – 8:02 AM Eastern
**Duration:** About 29 minutes
**Attendees:** Val Levitan (organizer, chair), Pavel Frolov, Irina Shishko, Andrei Bosik, Dmitri Kovalchuk
**Raw transcript:** [[Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026]]

## Summary

Held in Russian. Speech recognition is poor in many places, and Val's audio dropped several times in the first 6 minutes and again near minute 28.

**The problem Val raised.** The team keeps trying to run work through Jira, and it is very hard. Val sees one main cause: work is not assigned to the right people. Either Pavel does it for everyone, or Irina does it for her own team. Val said this is wrong. The team is small, and it is also hard to create good tasks. Val said Jira is a very large tool for a company this size, but the company is in the middle of work now and cannot move off it.

**Val's three improvement ideas.**
1. People should take on less themselves and assign more.
2. Dima (Dmitri) or Andrei should prepare daily reminder reports for everyone who has tasks. Maybe two a day: one in the morning and one around 12:00, before lunch.
3. The most important: set up **AI project managers** that use the company standards and meeting transcripts to create Jira tasks and write the descriptions themselves.

**Reports already exist.** Andrei said points 1 and 2 are already done. There is a report that sends each person their own Jira information. There is a similar mailing for GitHub. Pavel said Dima made it yesterday or today. Val said he saw the report, likes it, and it led him to call this meeting. He said it will only work if tasks are assigned to the right people.

**Assigning tasks directly to Claude.** Dmitri said two problems are mixed: "no one to assign to" and "nothing to assign" (tasks are not created). He proposed assigning some Jira tasks directly to Claude. Claude would take the task context, go to the repository, try to do the work, and open a pull request. Andrei said this function exists but is risky. Irina said everything would need to be set up perfectly first, or it would overwhelm the team. Val said review also takes time. Pavel called it "radical." Val said it is a good but deep step that needs study. Dmitri said he did not mean all tasks at once.

**Human-approved task creation.** Val proposed that Claude helps the person responsible build the tasks from transcripts and standards, and that person approves before Claude puts them in Jira. Pavel said he already does this: after a meeting he asks Claude to compare the discussion with existing tasks and suggest (not create) new ones. The result is written better than a person writes, but it takes about the same time. Andrei said Claude often over-complicates and adds things the team does not need. Val said the prompt must set firm limits: tell it the facts are the transcript and the standards, that the company has **20 people**, that resources are limited, and how many tasks it may create. He said the prompt must be polished over time.

**Shared company knowledge base.** Dmitri said topics cross between meetings, so Claude may get confused if it reads one meeting alone. He suggested a server with a large knowledge base, like a second brain, for example Obsidian. Val said he uses Obsidian as the holder of original transcripts, and builds a **second brain by the Andrej Karpathy method**: Claude reads all text and builds a wiki-style encyclopedia with indexes and summaries. His own covers transcripts from January 1, 2025. Pavel said each person now has their own local knowledge base, so knowledge from meetings they did not attend is missing. Pavel and Andrei confirmed they record their meetings.

**Val's direction.** Val said: let us create **one company second brain** by the Karpathy method, give the AI project manager specific domain knowledge, point it at the **GitHub repositories**, and give it a conservative framework (20 people, limits). It must write in **ESL English** (English as a second language), and Val said he tells his own prompt to keep replies to no more than 30 seconds of reading for an ESL reader.

**How it would run.** Pavel said the manager should run at set times, read the latest meetings, and find missing tasks or gaps. Val said once a day is too slow. Andrei said the architecture is not simple. He said access to Teams/Azure meeting transcripts is hard to get. Val agreed that getting transcripts and real results will take time, maybe a month. Andrei suggested that when the manager finds a gap, it emails the task owner, who replies which points to accept, and then it creates the Jira task. Val preferred that changes go as **pull requests** approved by the responsible person, and a merged pull request is the trigger for the AI to change Jira. Dmitri said a pull request only changes the repository, and the AI still needs a command to process it. He also said the data volume could be very large and expensive. Pavel and Andrei said Git is not the right tool for this. Val explained: Obsidian holds the frozen original transcripts; only the small summaries go to GitHub, where versioning and approvals are easier. Val offered to have Claude write up how his own second-brain system is built, if the team wants it.

**Next step.** Dmitri proposed homework: each person thinks how they would build the AI project manager (its functions, an algorithm, how it works), then the group discusses together. Val agreed. Val proposed Monday; Andrei asked for Tuesday; Val agreed to **Tuesday at 7:00**.

## Decisions Made

- **Direction: build an AI project manager for Jira on one shared company second brain** (Karpathy method, pointed at the GitHub repositories, conservative limits, ESL English) — current work split causes Pavel and Irina to carry Jira alone, and each person's knowledge base is separate. Technical design is not decided; it goes to homework. (Decided by Val Levitan; Pavel agreed)
- **Each person prepares their own design idea before the next meeting** — to compare approaches together. (Proposed by Dmitri Kovalchuk; agreed by Val Levitan)
- **Next meeting Tuesday, September 29, 2026, at 7:00** — Andrei asked for Tuesday instead of Monday. (Decided by Val Levitan)
- Considered and not adopted now: assigning Jira tasks directly to Claude to code and open pull requests (Dmitri) — seen as risky and "radical"; Val said it needs deeper study.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | All attendees (Pavel, Irina, Andrei, Dmitri, Val) | Each think through how to build the AI project manager for Jira: its functions, an algorithm, and how it would work | Sep 29, 2026 (Tuesday 7:00 meeting) | High | Homework proposed by Dmitri |
| 2 | Val Levitan | Have Claude write up how Val's second-brain system is built, to share with the team | TBD | Normal | Offered "if you want" [Needs Val's confirmation] |

## Open Questions

- Where approvals and versioning should live: Val proposed GitHub pull requests as the trigger; Pavel and Andrei said Git is not the right tool; Dmitri suggested Obsidian. Not resolved.
- How to get access to Teams/Azure meeting transcripts for all company meetings (raised by Andrei).
- Cost of processing a very large amount of data (raised by Dmitri).
- How often the manager should run: Pavel said once a day; Val said a day is too slow. Not resolved.
- Whether the manager should confirm gaps by email with the task owner (Andrei) or by pull request (Val).

## Dispatch Log

---
*Processed from Teams transcript on September 28, 2026 (meeting-watcher recovery sweep)*
*Source meeting: JIRA management AI*
