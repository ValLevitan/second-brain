# Meeting Summary — NOVA-2
**Date:** November 6, 2026, 10:33 AM – 11:42 AM Eastern
**Duration:** ~68 minutes
**Attendees:** Val Levitan (host), Anton Leshkevich, Efim Podvoiski, Igor Metelski, Evgeny Kharetski, Alexander Biratko, Pavel Frolov, Irina Shishko, Andrei Bosik
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_NOVA2_Studio_Engine_Demo_and_Agile_Merge_Plan-November-6-2026]]

## Summary

**Purpose.** Merge meeting called at the morning AI teardown review: how Anton's engine and studio, Igor's scene tools and Evgeny's design agent fit together into NOVA 2. Efim joined for the first time; Val explained this is one of a series of spikes, this one on leaving the HTML/browser engine (Pixi) for our own engine in Rust.

**Anton's demo: engine and studio.** Games are self-contained modules, like plugins in Rage: a small Rust file that pulls modules from the framework plus its own resources. Anton wrote the requirements and capabilities yesterday. New spike: a studio (editor). Architecture: an engine (graphics, LGS communication, sound, game state) and two repositories, framework and games, written in Lua scripts so changes run without recompiling. The studio is in Rust, links the engine, and has an embedded agent connected through OpenRouter so the model can be swapped; Anton uses Claude Haiku for cheap fast iterations. The agent has tools for resources, games and the framework (early), reads Confluence and works with git. The studio and the framework each have an MCP server, so an outside agent such as Claude Code can drive them; remote control works through MCP; a phone-style remote session does not exist yet. Demo: a Jira ticket with Clover Fortune assets; the agent imported the assets, wrote the game by copying Cali Fortune, and showed it playing. One leftover picker element was removed on request; a bonus artifact remained. The workflow is iterative chat, then commit and pull request. Engine: Rust on OpenGL. It supports the Miranda-exported asset format because that is what Anton had; Miranda itself is not required.

**Scene format and Rage.** Alexander: keep the scene data contract from the Omni/Pixi era as our working format, simplified (less stretch and positioning logic), and build scenes with AI; Unity and Miranda are not needed. Val asked, from an administrative view, whether we formally leave Rage. Answer from Efim, Igor and Anton: there is no Rage in this; staying on Rage would mean keeping its scene contracts and 3ds Max for designers, which makes no sense. LGS stays and is better than the old data center.

**Math for the agent.** Anton wants an MCP server to the math engine so the agent gets example messages when adding a bonus. Efim: data contracts are JSON schemas and do not capture the semantics; the simplest working source is the test result files from his math runs (thousands of games), already available locally. Igor did this for the Rich Igor ports. Efim and Anton will talk.

**Agile, not a big spec.** Val worried that NOVA turns into months of writing use cases. Efim: go agile; build, look, add; dry specs nobody reads. Val agreed: code first, then write the prose, capabilities and use cases back from the code and find the gaps. Pavel: agile still means writing capabilities, just small pieces at a time.

**Igor: scene generation without designers.** Develop on placeholder scenes, then form the scene contract and generate the real scene. He showed the Aristocrat-style bonus built from Evgeny's description with no assets (shown at the morning meeting), later with generated art; no real math yet. Designers as integrators are not needed if we have a scene generator for Anton's engine; Val: designers can describe things in words. Igor's tools today target the Rage format with a converter to the new format; the goal is to generate placeholder scenes directly in the new engine's format.

**Evgeny: design agent and second brain.** An agent turns a conversation with a game designer or artist into a specification usable for graphics and integration; a couple of hours from talk to a playable game in theory. It uses the math as a source of truth, plus a wiki of our games (already generated for GA-COAM 3, 15 games) and competitor mechanics in the second brain. A procedure generates a full brief from a repository (screens, mechanics, animation timing) because Confluence is stale; code and resources are the single source of truth. Efim: the speed is a little frightening.

**Pace and confidentiality.** Val: a game from first conversation to lab submission in about a week; Igor: not yet tried with real math. Efim: a pipeline could make four games a month. Val asked that this stays within the people on the call for now.

**Class A play test.** Efim is working on Class A games, a new thing with no experience; he wants a play test and asked Anton for a day or so to build a prototype so he and Michael can play it; HTML would take two weeks. Anton and Efim meet Monday. Michael will not be told where it came from.

**How it assembles.** Andrei Bosik: everything shown is parts of one machine to package. Pavel: the integration repository (Evgeny) runs tests of the components in the ISO; Evgeny has not added Pixi games to it while waiting for the new engine; hardware, progressive and LGS are there with end-to-end tests, and adding a new-engine game is easy once its repository exists. Flow agreed in discussion: designer and agent produce a brief; a game repository is created from a template (GitHub template repo, Andrei); scenes are built in that repo with Igor's skills; the engine is pulled from its own repo; the studio is installed locally; the main repository builds the ISO. Igor's web tools move into Anton's studio (Slint native UI, not web); Igor's skills port to the studio agent, which is deliberately less powerful than Claude Code and gets tools as needed. Browser/HTML runtime: not needed (Igor, Alexander, Andrei Bosik); Pavel accepted.

**Repositories and tooling.** Val: create corporate repositories and get all of this off personal computers; Andrei Bosik oversees. Anton has two repos (engine plus studio; framework plus games) and sends their descriptions to Andrei for naming by convention. Andrei offered the auto-update mechanism he and Evgeny designed for another app (Tauri-based there); Evgeny explains it to Anton. Evgeny loads the second brain with Igor's wikis and Efim's math; Igor said Fanat is in poor shape, give Dakota instead.

**Math side.** Val wants Efim connected so that Claude develops the math from a mechanic description. Efim: Claude writes code from his words today, not from a mechanic description; code and calculations are separate things; we will move toward it.

**Schedule.** Three working days (Saturday, Monday, Tuesday); next meeting Wednesday morning. Igor: postpone the planned full port of a competitor game from its help screens until the new-engine development scheme works; Val agreed.

## Decisions Made

- **Rage is finished; NOVA 2 is Anton's Rust/OpenGL engine with Lua-scripted framework and games; LGS stays** — (Val, Efim, Igor, Anton, Alexander)
- **Miranda and Unity are not needed; the Omni/Pixi scene data contract is kept as the working format, simplified, and scenes are built by AI** — (Alexander, Igor, Val)
- **Agile: code first in small pieces, then capabilities and use cases written back from the code; no big up-front NOVA spec** — (Val, Efim, Pavel)
- **All work moves off personal computers into corporate repositories now; Andrei Bosik oversees** — (Val)
- **No browser/HTML runtime for the engine or the development environment** — (Igor, Alexander, Andrei Bosik)
- **The competitor-game full port experiment is postponed until the new-engine scheme works** — (Igor, Val)
- **Next meeting Wednesday morning** — (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Anton Leshkevich | Upload all engine, studio, framework and game code to corporate repositories with notes on what to look at | Nov 7, 2026 | High | "By Saturday morning" |
| 2 | Anton Leshkevich | Finish the refactoring (factories), then prepare for integration with Igor's and Evgeny's tools; add notes and skills so the architecture holds with many developers | Nov 11, 2026 | High | Three working days |
| 3 | Anton Leshkevich | Send Andrei Bosik the descriptions of his two repositories for naming | Nov 7, 2026 | Normal | |
| 4 | Anton Leshkevich | Create the group chat for this topic | Nov 6, 2026 | Normal | |
| 5 | Igor Metelski | Study Anton's project and integrate his skills and web tools into the studio; generate placeholder scenes directly in the new engine format | Nov 11, 2026 | High | Has a Rage-to-new-format converter |
| 6 | Evgeny Kharetski | Load the second brain with Igor's game wikis and Efim's math (Dakota, not Fanat) | Nov 11, 2026 | Normal | |
| 7 | Evgeny Kharetski | Define the design-agent output: brief plus files for a new game repository created from a template | Nov 11, 2026 | Normal | Agent does not create repos itself |
| 8 | Evgeny Kharetski | Explain the auto-update mechanism to Anton | TBD | Low | Tauri-based in their app |
| 9 | Andrei Bosik | Create the corporate repositories (names from Anton's descriptions) and the GitHub template repository for new games; oversee the move off personal PCs | Nov 11, 2026 | High | |
| 10 | Efim Podvoiski, Anton Leshkevich | Meet Monday on the Class A play-test prototype and on math message examples for the agent | Nov 9, 2026 | Normal | |
| 11 | Val Levitan | Schedule the Wednesday morning follow-up | Nov 6, 2026 | Normal | |

## Open Questions

- How does the studio agent get math message examples: MCP to the math engine, or Efim's test result files? (Anton, Efim)
- Can Claude produce math from a mechanic description, and how? (Val, Efim)
- Studio auto-update: Anton's studio is not Tauri; which mechanism fits? (Andrei Bosik, Evgeny)

## Dispatch Log

---
*Processed from Teams transcript on November 6, 2026, 12:15 PM Eastern (scheduled meeting-watcher)*
*Source meeting: NOVA-2*
