---
type: decision
title: The company second brain is the one knowledge source for all current and future AI agents — agents keep only their logic, each gets only the data it needs, limited both in the second brain and in the agent; the game design agent sees game knowledge only (old-game wikis, Efim's maths turned into mechanics, game rules), not transactional data or meetings (Bosik proposed; Val, Oct 29 2026)
date: 2026-10-29
aliases: [one brain for all agents, один мозг на агентов, база знаний была одна у всех, second brain as the agents' knowledge source, источником данных будет выступать всегда секонд брейн, per-agent access limits, ограничено с 2 сторон, game design agent scope, what the game design agent may see, second brain as MCP server, forbidden-context test]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
---

# One second brain feeds every AI agent; the game design agent sees game knowledge only

Set at the [[wiki/meetings/2026-10-29-ai-game-design-assistant-review-one-knowledge-base-and-a-full-cycle-test.md|Oct 29 2026 game design agent review]] (6:59 AM, Russian). [[wiki/people/andrey-bosik.md|Andrey Bosik]] proposed it the day before to [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], who raised it; [[wiki/people/pavel.md|Pavel Frolov]] agreed with a condition; [[wiki/people/val-levitan.md|Val Levitan]] set the game design agent's limits [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]] [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]. The second brain it means is the one built for the AI project manager — [[wiki/projects/ai-project-manager-and-company-second-brain.md]] (Bosik: "для пьем агента seconbrain", read as the PM agent's second brain — **inference**).

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## The proposal

- **Kharetski.** "Андрей вчера предложил. Использовать один. Мозг наа. Агентов… чтоб база знаний была одна у всех." [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]
- **Bosik.** The agents hold only the logic of how they handle information and work with the user; "источником знания у всех агентов может быть секонд бренд. Мы и так храним, там уже часть информации." Then the agents need not store their source data themselves [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **What it holds today (Bosik, answering Val).** Converted meeting transcripts; data from the GitHub repositories — it reads the prose and the CLAUDE.md files ("читает клод. Инди файл") and builds a so-called card per repository; and Jira. Not the old games' code: "Нет, пока старых игра." [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]
- **One source for all.** Bosik: the point is not what it gives game design but that "у нас появляется один источник данных для всех. Текущих будущих. Агента." Kharetski: it becomes a global knowledge base; data is taken in portions, only what is needed at that moment [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **Later, maybe an MCP server.** Bosik: technically the second brain could later serve as an MCP server, for example for Claude Code ("клип кода", read as Claude Code — **inference**, as the notes read it) on a user's computer — "это совсем далеко есть уже фантазировать" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]] [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].

## Access is limited per agent

- **Pavel's condition.** Useful "при условии, что агент будет ограничен": game repositories may help a game designer; "Всё, Что касается транзакшенвисов… это только засорение контекста." Kharetski: the same for Jira — only certain projects [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **Two sides.** Bosik: "это будет ограничено на стороне самого секэндбрейн и это будет ограничено ещё на стороне самого агента." [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]
- **How to know the context is clean.** Val asked how to make sure, since a mistake would never be seen. Kharetski: each agent has a set of tests; one test can feed it context that is forbidden for it. Bosik: a question-and-answer test cycle checks whether the answer is right, carries the needed information or rubbish, and whether it invents. Kharetski's own tests are automatic; the day before, his agent "почему то решил, что он женщина, хотя у него было написано, что он мужчина" — the autotests found it and it was fixed [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **Indexed, not searched.** Bosik: for the second brain to work fast, the maths and wikis must be loaded as indexed pages or cards. Kharetski: so that, asked about Clover Fortune, the agent goes straight to that game's maths file instead of going through all the maths — "мапинг или индексация"; global, not local, in the second brain's case [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].

## What the game design agent may see (Val)

- **Val's line.** "Я не думаю, что дизайнеру можно давать чтото. В дополнение…": the wikis of past games "которые мы выберем", plus all of Efim's maths "разобрана с математики. В механику", plus a description of the game rules [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]. Only what concerns the games themselves: no access to equipment transactions, and no access to "наши митинги" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **Designer meetings.** Kharetski asked why not connect the designers' meetings; Val: they are most likely just pollution ("загрязнения"); Bosik agreed [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **Competitor mechanics.** Kharetski suggested adding competitor-mechanics analysis; Val: "в дальнейшем, конечно" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **Val's earlier support.** Repositories and maths he supports — for example old games' code with prose, "сейчас её нету, но она создастся" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].

## Kharetski's recap (Val asked for it)

The agent now leads a designer who does not know what he wants; then "это будет централизованный secand brain, но с правами доступа для каждого из агентов определёнными"; and Igor's old-game wiki is accepted and will be loaded into that second brain. Bosik added: the maths too, in some form [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]. The wiki job: [[wiki/decisions/2026-10-24-code-not-confluence-is-the-source-of-truth-and-claude-builds-a-wiki-per-old-game-from-the-svn-code.md]] (Oct-29 update). The agent: [[wiki/decisions/2026-10-18-evgeny-kharetski-owns-a-voice-ai-game-design-assistant-with-a-first-pass-reviewed-oct-25.md]] (Oct-29 update).

## How it sits against earlier rulings

- It widens [[wiki/decisions/2026-09-25-one-company-second-brain-feeds-an-ai-project-manager-for-jira.md]] — one company second brain for the AI PM — to every agent (**inference** — the link is not drawn in the meeting).

## Open questions

- How is maths turned into mechanics for the second brain, and who does it? Val wants Efim's maths "в механику"; nobody present understands Efim's Excel files — see [[wiki/decisions/2026-10-18-evgeny-kharetski-owns-a-voice-ai-game-design-assistant-with-a-first-pass-reviewed-oct-25.md]] (Oct-29 update) — [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]
- [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]
