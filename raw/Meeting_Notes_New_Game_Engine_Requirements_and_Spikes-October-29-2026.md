# Meeting Summary — Engine to replace HTML and PixiJS, and how we move forward
**Date:** October 29, 2026, 11:59 AM – 1:04 PM Eastern
**Duration:** ~64 minutes
**Segment:** Segment 2 of 2
**Attendees:** Val Levitan, Anton Leshkevich, Alexander Biratko, Pavel Frolov, Irina Shishko, Igor Metelski, Evgeny Kharetski, Andrei Bosik
**Raw transcript:** [[Meeting_Transcript_New_Game_Engine_Requirements_and_Spikes-October-29-2026]]

## Summary

Held in Russian. Some words are unclear in the transcript and are marked "heard".

**What Anton has done.** Anton used AI to collect capabilities from the existing platforms (Rage, Rage Studio, NOVA and others) into the framework repository, as a toolbox. The goal is to keep the good solutions built over 20–30 years, not to copy everything. He then continued his engine requirements list from the last meeting.

**New engine requirements (Anton).**
- Screenshots of a full screen, a full scene, or a single object.
- Sound inside the engine, so LGS no longer manages sound. The current sound library's license does not allow casino games out of the box. Anton recommends Kira (Rust, MIT license, free).
- Video replay for players. Two options: a rolling buffer of the last seconds, or rebuild the video from saved round data (like game history). Buffer is a problem for games with up to 400 spins and means large uploads from the machine. Alexander and Pavel prefer saved state. Pavel: Daniil already did a spike — the state goes to a server-side service that rebuilds the video, so the machine keeps playing and the player gets it on the phone.
- Shaders supported from the start.
- Platforms: Linux on both x86 and ARM (the RK boards), plus Windows so designers can run games locally. Windows is only for internal testing, never for final builds.
- Future, not MVP 1: compile to WebAssembly for browsers. Andrei and Alexander think full browser support is too much; Alexander said trying it costs little.
- An inspector toolkit for scenes, animations and properties. The engine and framework must work well with AI: the inspector and an AI API use the same module. Andrei noted Unity has built-in MCP support; Alexander: build the API first, then MCP on top.
- Modularity: math games and bonuses as modules; the game itself is a module that can be loaded and unloaded. The framework should work like a constructor. Alexander: this is the base architecture.
- Evgeny asked about a "Play" button editor like Unity. Anton: a full editor is not version 1. Alexander proposed a requirement to add resources to a scene on the fly without reload — about half of an editor, and it lets AI build scenes live.
- Language: Rust. Anton's prototype is in Rust.

**Val's tip.** Ask Claude for a short executive summary in prose (max two paragraphs) of an engine — what it can and cannot do — then ask Claude's opinion on whether it fits.

**How designers will work.** Anton: version 1 uses the existing Miranda assets, so the designer workflow does not change; an editor comes later. Alexander: AI can now assemble scenes; designers keep animations. Pavel described a designer tool with voice commands where AI places resources through MCP and replays the scene. Val: talk to it with words and pictures. Alexander: the engine is installed on the designer's PC and Claude talks to it through MCP — this must be in MVP 1. AI can also take its own screenshots to check its work.

**The full pipeline (Evgeny and Igor presented).**
- Evgeny: a Teams agent with access to the Second Brain. It holds a wiki of old games (one spec per game, with graphics references and element layout); math will be added. The agent interviews a designer and outputs a full game spec for a given reel layout. This spec goes to Igor's tools.
- Igor: a Claude plugin takes the brief. Steps: full-screen background art for all scenes; approve; add frames and elements (the comp art); approve; cut the art into animatable layers (characters, sky, etc.); animate with generated video or with shaders; a tool converts all of this to a YAML scene format. Two options for the engine: baked full-HD video, or shaders where possible and video only where needed. This needs measuring on real machines.
- Val: after that, the game goes to GLI for approval, then to the production server, then to each machine.
- Evgeny and Igor: the engine and framework sit between Igor's step and Val's step. Andrei and Irina added CI/CD, auto-tests, and the link to the CMS and RIS.

**Process order (Val).** Anton wanted to start coding this week. Val said no. Order: describe the full engine with all wishes; split into MVP 1, 2, 3; make an overall schedule; make an exact schedule for MVP 1; build a test environment that can test during development; then write code.

**Team.** Andrei: Igor's tool should become part of Anton's system (as the editor). Val: Anton must not do this alone — Anton, Igor and Alexander work on the engine together. Anton guessed MVP 1 could take a few days to a week. Irina: the MVP 1 scope is not known yet. Alexander: if MVP 1 is "render a scene plus MCP for Claude", it is quick; the modular load/unload architecture will take longer.

**Creative leader.** Val: the creative director (a new person who never worked this way) must find the system smooth. Evgeny's tool must steer him back when he goes the wrong way. Val said this must be part of MVP 1, or no game can be made. Alexander: the engine layer underneath is also MVP 1. The first game will be slow, because the framework (reel spin, buttons, tickers, rich text) must be ported to Rust from Omni or Rage. Daniil's capabilities describe this framework work.

**Text.** Igor: Rage cannot put a texture or even a simple gradient on text; this must be an engine requirement. Anton will add it. Irina: go through the capabilities to see what should move into the engine.

**Capabilities review.** Pavel: Daniil's capabilities should be read by senior people, not the young specialist, since Daniil's team wrote them. Readers: Alexander, Igor, Anton (and Pavel). Val: read, comment, agree among yourselves, delete what is not needed and write what is missing, by Monday morning (Val's time). Alexander may work Sunday. Alexander asked Anton to put his requirements into Jira so capabilities can be built from them; Pavel: mark them with the NOVA component for filtering. Anton agreed. Tests come after the capabilities are groomed.

**Next meeting:** Monday, November 2, 8:00 AM (Val's time).

## Decisions Made

- **Process order before coding** — full engine description with all wishes, split into MVP 1/2/3, overall schedule, exact MVP 1 schedule, test environment, then code. Anton does not start coding now. (Decided by Val)
- **Player video replay uses saved round state rebuilt on a server**, not a buffer on the machine — smaller data, machine keeps playing. (Proposed by Alexander Biratko and Pavel Frolov; Anton agreed)
- **Target platforms: Linux x86 and Linux ARM; Windows only for internal and designer testing.** (Alexander Biratko, Pavel Frolov)
- **Anton, Igor and Alexander build the engine together.** (Decided by Val)
- **Engine on the designer's PC with MCP access for Claude is in MVP 1**, and the creative-leader workflow must be part of MVP 1. (Alexander Biratko; Val)
- **Daniil's capabilities are reviewed by Alexander, Igor and Anton (plus Pavel)**, not by the junior specialist. (Proposed by Pavel; agreed by Val)
- **Engine requirements go into Jira with the NOVA component.** (Alexander Biratko, Pavel Frolov; Anton agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Anton Leshkevich | Spike: architecture for game modularity, so the framework works as a constructor for each game | Nov 2 | High | Report at Monday meeting |
| 2 | Igor Metelski | Spike: test shaders vs video on real machines (a 1000-series machine and ARM, browser version if needed) | Nov 2 | High | Decides video vs shader approach |
| 3 | Alexander Biratko, Igor Metelski, Anton Leshkevich (and Pavel Frolov) | Read Daniil's capabilities, comment, delete unneeded ones, write missing ones, split by MVP | Nov 2 (Val's morning) | High | May meet Sunday |
| 4 | Anton Leshkevich | Extend the requirements with an editor, based on today's wishes; add textured/gradient text requirement | Nov 2 | Normal | |
| 5 | Anton Leshkevich | Put engine requirements into Jira, component NOVA | TBD | Normal | Base for capabilities |
| 6 | Anton Leshkevich | Post the link to the requirements repository in the chat | Oct 29 | Low | Irina asked |

## Open Questions

- Sound library choice: Anton recommends Kira; not formally decided. (Anton)
- WebAssembly / browser build: kept as a future idea; value unclear. (Anton, Andrei, Alexander)
- Exact MVP 1 scope and timeline. (Irina, Alexander)
- Where the line sits between Igor's tool and Anton's engine/editor. (Andrei)

## Dispatch Log

---
*Processed from Teams transcript on October 29, 2026*
*Source meeting: Engine to replace HTML and PixiJS, and how we move forward*
