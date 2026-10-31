# Meeting Summary — AI-Game Design Assistant review
**Date:** Thursday, October 29, 2026, 6:59–8:19 AM ET
**Duration:** about 78 minutes (transcript 00:00–01:17). Held in Russian.
**Attendees:** Val Levitan, Evgeny Kharetski, Igor Metelski, Andrei Bosik, Pavel Frolov, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026]]
**Previous review:** [[Meeting_Notes_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026]]

## Summary

**Agent leads the designer.** Evgeny added a mode where the agent takes the lead when a designer is stuck. A designer can say only "I want to make a game", and the agent guides them step by step.

**One knowledge base for all agents (Andrei's proposal).** The agents keep only their logic. All knowledge comes from the Second Brain. Today it holds processed meeting transcripts, cards built from GitHub repositories (from prose and CLAUDE.md files), and Jira. Each agent gets only the data it needs. Access is limited on both sides: in the Second Brain and in the agent. Pavel supports it if the agent is limited. For example, transactional repositories would only pollute a game designer's context. Val asked how to know if the context is polluted. Evgeny and Andrei said each agent has automated question-and-answer tests, and one test can check for forbidden context. Evgeny's tests had already caught his agent calling itself a woman. Later, the Second Brain may also serve as an MCP server for Claude Code on users' computers. Andrei called this far off.

**Old-game wiki from code (Igor's experiment).** Igor gave Claude the brief that Evgeny's tool produces and asked for the same brief for the existing game Clover Fortune (spelling varies in the transcript). Claude broke down the idea, tone, style, palette, motifs and screen parameters, and pulled references from the game repository. Evgeny: this lets us build a wiki library of old games and load it into the Second Brain, instead of moving heavy Rage into Git. It is an automated process: one prompt, about a day of run time, plus a template to tune. The source is the production versions of games in SVN (code, action graphs, textures, screens), so it is current, unlike Confluence. Igor: for the wiki, use the real (horizontal) screen layouts, not the vertical layouts of a new-game brief. Val asked to also assemble the full game screen. Very old games are not needed. The team picks the set of games.

**Math to mechanics in prose.** Val asked whether Efim's math can explain a game's mechanics in words. Igor thinks so, but bonus behavior also depends on the framework and on each game's math settings and XML files. He proposed a test: let Claude work out a bonus alone, without being told how it works. Mechanics can be described. RTP statistics cannot be rebuilt from math alone; that is separate, large work. Pavel's idea of composing new mechanics or a target RTP from a library of all past mechanics would need deterministic algorithms, not only Claude. Nobody present understands Efim's Excel files.

**What the game-design agent may see.** Val's position: wikis of the chosen past games, plus Efim's math turned into game mechanics, plus game rules. Not transactional data, not meetings; designer meetings are likely pollution. Evgeny suggested competitor mechanics analysis; Val said later. Andrei: the data must be indexed so the agent goes straight to the right file.

**Igor's toolkit demo.** It is a plugin of Claude skills that starts from the creative brief:
- Claude writes art prompts. Igor pastes them into ChatGPT by hand; there is no API link yet.
- The art is split into layers. Python web tools let him move and scale layers, set paytable cells and symbol sizes, and set fonts, including the new message line on the paytable.
- An animation tool animates the layers in code where possible. Backgrounds use shaders instead of one full-HD video, and video is kept for characters (a pay-per-token video model; Igor did not name it clearly).
- Rejection reasons go back into the tool, so later prompts improve.
- The tool can export scenes into a Rage game. The game shown was built in one or two Claude sessions.
- Scenes are stored in a YAML format that Claude invented. Igor raised it as one option for the new engine's scene format.
- Not done yet: symbols tool, transitions. It needs testing by someone other than Igor. Andrei suggested an OpenRouter API key to compare image models.

**Val's concern: fast but approximate.** Val worries that AI iteration gives a game fast but without fine polish. A producer can ask for "a bolder smile", but it is unclear how that passes to a machine. Igor: background motion (cloud speed, shine, sway) is easy to set in code. Video models with key frames allow iteration on parts of a clip. Pavel: designers could regenerate frames 7–13 only. Val was not fully convinced.

**Goal: one full cycle.** Val asked whether we can take a brief to a finished game on the production server, ready to download to a machine. Evgeny: yes, that was the original idea. Val: "Let's do it." Andrei: first pass the whole cycle once, then automate.

**Engine question.** NOVA has no engine yet; HTML is already dropped. Evgeny: running the test on Pixi and then switching engines means doing the setup twice, but that is days, not months. The integration repository is ready, with 30 automated tests. Evgeny paused connecting games to it while the engine is open. Val suggested an MVP-1 engine with the same capabilities NOVA has today in Pixi plus HTML. Igor: Anton has already generalized this for Rage. A meeting on it happened Monday, and questions remain, such as whether to build for Windows. Val: Windows is needed because that is how designers see games. Evgeny would not base the engine on Miranda. Miranda is only a converter and not needed. Andrei agreed fully. Val: "OK, we threw out a lot." Evgeny: Rust is decided; a graphics shell must be written. Irina and Andrei: Anton has the expertise and must be in this.

## Decisions Made

- **The Second Brain is the single knowledge source for current and future agents.** Each agent gets only the data it needs, limited both in the Second Brain and in the agent. (Andrei proposed; Evgeny, Pavel and Val agreed)
- **The game-design agent sees game knowledge only:** wikis of chosen past games, Efim's math turned into mechanics, and game rules. No transactional data, no meetings. Competitor analysis comes later. (Val)
- **Build the old-game wiki from SVN code with Igor's method and load it into the Second Brain.** (Evgeny's recap, no objection)
- **Run one full cycle: brief to a finished game on the production server, ready to install on a machine.** (Val: "Let's do it")
- **Miranda is not the basis for the new engine.** It is only a converter. (Evgeny, Andrei; Val accepted)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Set the follow-up meeting with Anton on replacing HTML and Pixi, and the next steps | Oct 29, 10:00 | High | Val said he will set it |
| 2 | Igor | Add the full assembled game screen to the old-game brief | TBD | Normal | Val asked for it. [Needs Val's confirmation: no explicit commitment] |

## Open Questions

- Who builds the old-game wiki, and which games go in? (Evgeny: pick a package of needed games)
- Can Claude work out bonus mechanics from math plus framework code? Igor proposed the test; no owner or date.
- Do we run the full-cycle test on Pixi now, or wait for the new engine? Val asked; this goes to the Anton meeting.
- Can designers give precise enough notes for AI polish? (Val)
- Who tests Igor's toolkit besides Igor? (Igor)
- What is in Efim's Excel files? Nobody present knows. (Pavel, Igor)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-29*
*Source meeting: AI-Game Design Assistant review*
