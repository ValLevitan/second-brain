# Meeting Summary — Nova-2 follow up
**Date:** November 21, 2026, 10:01 AM – 11:36 AM Eastern
**Duration:** ~95 minutes
**Attendees:** Val Levitan, Anton Leshkevich, Igor Metelski, Evgeny Kharetski, Alexander Biratko, Pavel Frolov, Irina Shishko, Andrei Bosik, Genadi Peari, Daniil Stauskiy
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_NOVA-2_Studio_Demo_First_ISO_and_Texas_February_Target-November-21-2026]]

## Summary

**Anton: the studio (game pipeline) demo.** The system is a conveyor. It takes a game brief (game description, sample art, other material) and guides one person through building the game, with all tools in one place. It is called "game pipeline" for now; Anton expects the names to change. The brief is version 1 and is based on the briefs from Evgeny's Teams agent. Anton added brief versions and migration, because the brief format will change as the pipeline grows.

- The core is a runtime with libraries. Steps plug into it. Each step holds its own tools, user screen, tests and review flow, so several developers can work on different steps without touching the whole code base. Each step has an `agents.md` file.
- Two steps are built so far: (1) import and review of the brief, (2) symbols.
- The app is a desktop app (Electron). It is designed so it can move to a web version later.
- Demo: Anton imported a brief made from the Wild Fire game for the Nebraska release. The review screen showed the theme, colours, features, and open questions (no background description, no picture for the jackpot coin). Open questions do not block the work.
- Symbols step: 12 symbols. Each gets a standard animation, controls, tests, then Approve. A small assistant changed a rotation angle on request and re-ran the tests. For the symbol with no picture, the tool wrote a prompt and generated the image. Symbols keep versions.
- Animations today are shader only, because Anton ported what was in Igor's slot-art tool.
- When all symbols are approved, the tool packs them for the NOVA-2 engine (format and atlases). The studio keeps its own workspace with in-between files.
- The studio talks to the engine through tools and MCP, so a developer can also run the same tools from Claude without the studio.
- Anton attached a handoff document to the meeting chat for any developer who starts on the project.

**What the team asked for in the studio.**
- Import of existing symbols (for example made in Unity, or common royals reused across games). Anton has it on his list; not built.
- Import and export, so an artist can fix a detail in Photoshop and bring it back (Andrei B.). Anton agreed it is important.
- Save to the repository at any time, so another person can pick up the work (Andrei B., Pavel).
- Web base and shared work: share, comment (Val: "very important").
- Three animation types: shader, frame-by-frame, skeletal (Spine) (Alexander).
- Anton's goal stays: one person, one game, one week. Shared work is a step on the way.

**Repositories.** Andrei B.: the old agreement was two repositories per game, one with art sources and one with game code and finished atlases. Igor agreed that work-in-progress art should not sit in the game repository. Not settled in detail.

**Shader or PNG sequence.** Igor: keep all options open and decide after performance is measured on the machines, especially on the RK platform. Alexander agreed.

**Evgeny: first image with a NOVA-2 game.** From the nova integration repository Evgeny built an ISO image with all services and one game on the new engine (the carnival game). LGS is integrated. It was installed from a USB stick on a test stand and the game plays.

- The ISO builder picks a version of each part (LGS, printer, counters, engine, framework, games), from main or from a release. Only branches with green CI can be picked.
- Idea: contract tests between parts run before the build if that pair of versions was not tested.
- All services run in Docker containers. The engine runs in a container too; games are mounted from disk. Each game sits in a folder named by its game ID, in a fixed layout for LGS and the framework. Evgeny expects new games can be dropped in and loaded later (remote update). Changing a game version will most likely need a controlled restart (no money, no game in progress).
- Load: the stand has 32 GB of RAM. Without the browser, the whole system with one game takes a bit over 3 GB. The RK platform has 8 GB. Docker memory use dropped by 2–3 GB after Evgeny changed how images are kept.
- The engine uses two full CPU cores (about 210%). Pavel: that is not little. Igor: they will look at it.
- The install flow needs work (the USB stick must be pulled out fast after install).

**Disk and containers.** Pavel: containers write temp files to the same disk; in the old platform the main partition with games was read-only. Genadi: check the GLI rules before deciding what goes in containers, and writing loads the disk. Pavel wants an external SSD on the RK3576 so the soldered eMMC is not worn out; the database should be on the external disk; eMMC is good for the secure checks. Pavel has already connected and tested an external disk. Evgeny: there is time to also try running the services without Docker. Andrei B.: build images on a light Linux such as Alpine.

**Val: dates and the end goal.**
- By January 15, 2027: a studio environment that a non-developer can work with alone, remotely, and submit comments. A new producer starts January 15. Pavel and Irina mentioned the 17th/18th; the exact day was not fixed.
- About February 1, 2027: start operating in Texas on the new platform with old games ported to it. Texas needs no certificate. Vertical cabinet. Val would prefer NAD2 and two platforms but will take what the team can give. The point is to see what breaks, at low risk.
- April 15, 2027 at the latest: get the new system approved (Val's word in the transcript is unclear; it sounds like GLI).
- Another option Val offered: Georgia Class A, which needs no approval. Math is not ready; Efim said about a week to 10 days more. The Class A game designs are in Confluence at concept stage, with no production yet.
- Val described the end goal: machines with a modem report which games, math and themes work in each region; JVL makes a new game in a week, sends it to the lab, pushes it to the machines by modem, checks the signature, collects data for a month, and repeats, per group of regions and per state. Genadi starts a new hardware machine next year; Val is willing to add sensors that the industry avoids today.

**Val on the art team.** Today production alone for 6 games takes 30–45 days with no art rework and 3–4 months with rework; concept and design take another 30–45 days. Val does not want to give the game-design agent to the designers yet. He wants to show them a finished, proven project first. He does not expect the art team to stay as it is.

**Requirements.** Irina: the Jira requirements project already has about 1,500 requirements and they must be read through. Requirements for the engine, framework and games are reused from the old platform; the studio is a new tool with its own requirements. Val: every requirement needs a group of tags; use Claude to tag them.

**Igor: Blender-to-video and 3D model.** Igor showed a short transition video. He set up a scene and camera path in Blender (Claude did it), then gave that reference clip to a video generator. The result follows the camera path closely, so the output is more predictable. He also showed a 3D wolf model made from one picture by a model tool; it came out with a wrong number of legs. Val and Anton praised the work.

## Decisions Made

- **Alexander Biratko becomes architect and coordinator of the NOVA-2 engine and games** — one owner at the top level, who also takes part in capabilities and requirements. Proposed by Pavel, put to the room by Val, no objections. (Decided by Val)
- **Two meeting streams** — the morning standup stays for transactional and other topics; a separate daytime NOVA meeting at a time good for Anton. Val is to be invited to all of them. (Proposed by Pavel, agreed by Val)
- **One new closed Jira project for all NOVA work** — existing NOVA projects are folded into it. Only the people in this meeting plus Alexei (11 people) may see it. (Decided by Val)
- **No work without capabilities and requirements.** (Decided by Val)
- **The studio must get: web base, shared work with comments, and the three animation types** (shader, frame-by-frame, skeletal). (Decided by Val)
- **Brief templates go in their own repository with versions**; the agent reads the latest from there. (Proposed by Evgeny, agreed by Val)
- **Shader vs PNG sequence is decided later**, after performance is measured on the machines. (Igor, Alexander agreed)
- **Next step is Georgia games on the RK platform** — convert the Georgia games (they are in production and easiest), build them into one image, run on RK, measure performance. Show on Friday. (Proposed by Evgeny and Igor, agreed by Val)
- **Class A briefs go through Evgeny's agent** — feed the Confluence pages to the agent, send Val the list of what is missing, Val gets it from the designers. (Proposed by Igor, agreed by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Anton Leshkevich | Finish Daniil's open pull requests and merge Daniil's sounds into the engine | Nov 23, 2026 | Normal | He said Sunday, then "by Monday" |
| 2 | Igor Metelski, Anton Leshkevich, Alexander Biratko and the developers | Hold an internal developers' meeting to bring the branches together and set one starting point | Nov 23, 2026 | High | Igor's game work and Anton's studio live in separate branches with different dependency versions |
| 3 | Andrei Bosik (with Dima) | Open the new closed Jira project, limit access to the 11 people, move the existing NOVA projects and new capabilities into it | TBD | High | Andrei: "we will organize it" |
| 4 | Irina Shishko | Bring Alexei into these meetings | TBD | Normal | He will write the automatic tests |
| 5 | Irina Shishko | Push Efim to give the math for the games being ported | Nov 27, 2026 | High | Igor had no math for Twin Bison; needed for Friday |
| 6 | Evgeny Kharetski | Build the pack of converted games into one image, update the LGS part, run it on the RK platform and measure performance | Nov 27, 2026 | High | LGS is behind for multi-product |
| 7 | Igor Metelski | Convert the Georgia games to NOVA-2 (he named 4 + 4 games) | Nov 27, 2026 | High | He has two done |
| 8 | Alexander Biratko and the team | Make the schedule for MVP1 and MVP2 that fits Val's dates, with the features possible in that time; tell Val if it does not fit | TBD | High | |
| 9 | Pavel Frolov | Set up the separate daytime NOVA meeting and invite Val to all meetings | TBD | Normal | |
| 10 | Evgeny Kharetski | Create the brief templates repository and point the agent at it | TBD | Normal | |
| 11 | Team (Igor, Evgeny, Irina) | Feed the Class A game pages from Confluence to the brief agent and send Val the list of missing information | TBD | Normal | Val passes it to the designers |
| 12 | Val Levitan | Get the missing brief information from the designers and return it to the team | TBD | Normal | After item 11 |
| 13 | Igor Metelski | Send Anton material on the Blender-to-video method | TBD | Low | |
| 14 | Irina Shishko | Tag the requirements in Jira (with Claude) so they can be sorted | TBD | Normal | Val's direction; Irina and Dima are still thinking how to sort |

## Open Questions

- One repository per game, or per release? And where do work-in-progress art files live? (Alexander, Andrei B., Igor)
- Docker or plain services on the RK platform? Evgeny wants to test both. (Evgeny, Pavel, Alexander)
- Do the GLI rules allow the disk writes that containers make? (Genadi)
- Is two full CPU cores for the engine acceptable, and can it be reduced? (Evgeny, Pavel)
- How long will game resources take to load when switching games? (Alexander)
- Texas on February 1: which product exactly — NAD1 or NAD2, one platform or two, how many games? Val will take what the team gives. (Igor, Pavel, Irina)
- The exact January date for the studio (15th, 17th or 18th).
- Agenda for the Friday meeting beyond the Georgia games on RK. (Igor)

## Dispatch Log

---
*Processed from Teams transcript on November 23, 2026*
*Source meeting: Nova-2 follow up*
