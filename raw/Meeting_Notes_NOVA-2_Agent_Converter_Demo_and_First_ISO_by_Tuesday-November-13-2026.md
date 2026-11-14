# Meeting Summary — NOVA-2 follow-up - Friday check
**Date:** November 13, 2026, 7:01 AM – 8:11 AM Eastern
**Duration:** ~70 minutes
**Attendees:** Val Levitan, Anton Leshkevich, Pavel Frolov, Igor Metelski, Irina Shishko, Evgeny Kharetski, Alexander Biratko, Andrei Bosik
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_NOVA-2_Agent_Converter_Demo_and_First_ISO_by_Tuesday-November-13-2026]]

Note: Evgeny sat in the same room as Igor. Many "Evgeny" lines in the transcript are a mic echo of Alexander or Igor. Only lines that differ are counted as Evgeny's.

## Summary

**Anton: the agent converter (diagram).** Anton showed his Rust app "Automated Converter" (studio "Lions Riches Studio"). Each box is an agent with its own tools (box names taken from the shared screen):
- **Interfaces** — Anton plus Claude. They are outside the system and give tasks to Builder.
- **Builder** — takes each task and sends work to **Scene**, **Play**, **RAGE Converter**, **Art**, **Game Scripting** and **Issues**. There is also a set of **Shared tools** that every agent has.
- When a tool is missing or slow, an agent logs an issue. After each run, Claude (with Anton) reads the logs and issues, fixes the code and rebuilds the app. Most of the app was written by Claude this way.
- The agents do not improve themselves. Claude improves them from outside. Anton called it "supervised learning".
- The user has only two buttons: Autonomous mode on/off and Pause.

**Goal and plan.** The final goal is an autonomous builder of slot games for NOVA-2. Step 1: convert Nebraska NAD-2 RAGE games to NOVA. Lions Riches is first; Claude reports 16 of 17 tasks done, but Anton has not played the new build yet. Step 2: convert 2–3 more games to make the tools general. Step 3: make games from a design brief, with no source game. Later boxes: autotest, LGS integration, deploy to the target board. Irina: in the brief stage, a brief-design converter replaces the RAGE Converter box. Anton agreed.

**Where Igor's work went.** Igor's RAGE-to-NOVA pipeline became the RAGE Converter agent. His scene tool became the Scene agent. All of his tools are in the shared repo. The Art agent is only a layer to image and video generators through OpenRouter (nano banana). It has no style guide or wiki. It looks at the RAGE scenes and writes its own art guideline. Igor said his last commits had a skill with JVL's style. Val asked why the team does not just reuse what Igor already built. This was not settled.

**Tokens.** Anton's OpenRouter tokens (corporate account) ran out at about 1 AM. He spent about $60 in about 10 hours. Options: a direct Anthropic API key, or OpenRouter (a few cents fee, but any model, including art models). Anton built analytics of tokens and dollars. Andrei said an earlier $100 was used up fast and asked what this will cost per hour or day. Val said the meeting time costs more than $60. Andrei later looked at the OpenRouter usage and has ideas to cut cost.

**Does NOVA work?** Alexander said NOVA is in the repo and Claude reads how it works. Val was surprised and wanted proof. Anton: the graphics engine works, and games run on Windows. They do not run on RK hardware yet. Pavel: he once rebuilt Anton's source for the RK3576 and it ran, but there was no math (same outcome every spin). Val asked how we know the NOVA code Claude reads is good. Anton: the Play agent will launch the game and play it, first locally, later on target hardware.

**Definition of done.** Val: the only proof is a build made by CI/CD actions, put on the production server, downloaded by link, put on a USB stick, and the machine runs. Pavel: a quick local build can show early if performance on RK is too low, which can save a week. Val and Alexander: this does not conflict with Val's rule. Pavel: NOVA works only when all components build into one ISO, even without some parts (e.g. no progressive controller), and it runs on a machine or RK3576 in test mode.

**Getting builds off the production server.** Pavel: the production server is S3. Today only payment-terminal builds go there, with auto-update through the terminal hub screen. A NOVA build put on S3 has no download screen; only Andrei can get it through an admin panel. Val: extend today's screen so it can show new products. Andrei: it should be a separate portal, like the one for Transactional. Val: the projects were split only to share the work. The screen was built by Dima Chudinov and Sergei Tsimanov. Andrei: many questions, not for this meeting. Val: take the undertaking anyway; details later.

**Val's idea: agents asking NOVA for features.** Val asked for a parallel flow: the game agent finds a missing NOVA capability and sends a request to NOVA's own agents, who build it. Anton: this is roughly what happens now, but the NOVA side is done by hand (Claude and Anton). It can be automated later. He wants to finish this part first. Val pointed out that Igor and Evgeny (Zhenya) need work. Anton: first finish Lions Riches, then refactor the repo. Today it is a "zoo" of tools and languages and is hard to work in.

**Igor: LGS integration.** Igor asked how ready NOVA is for LGS integration. Anton: the protocols have not changed, but he has not done the integration. Igor: rendering is only part of it. In RAGE, saving state to the data center is synchronous in the main thread and can take up to 8 ms, which is half a frame at 60 fps. The team must decide about threads and sync or async calls to the data center. He asked for an LGS agent in the flow. Anton agreed. Igor: an engine is not a game. The RAGE framework is much bigger than the engine. He doubts Claude can pull all needed framework features out of RAGE games. Pavel: Anton is growing the NOVA framework on top of the engine, driven by the games Claude analyzes.

**Old Data Center instead of LGS?** Alexander suggested using the old Data Center. Pavel, Andrei, Evgeny and Igor objected: new LGS is modular, with separate device services and a new interface and API. The old Data Center does not talk to the math server. Alexander withdrew the idea.

**LGS readiness (Evgeny).** LGS should work in general; problems will show in testing. SAS never connected to it. The integration repo is getting an autotest platform (contract tests, autotests), including protocol tests with the new tool. Direct answer: an LGS that runs on a machine with a game does not exist yet. There is no build yet. Integration with hardware services is not ready, and hardware services are not in the ISO yet. LGS talks to peripherals in theory and in autotests, but not on a real machine, because there is no image. LGS works with remote math; pointing it to local math is easy. LGS can run a mystery progressive. LGS builds as a Docker container on every PR and main. Evgeny expected a compose file to run all services on any PC, with hardware emulated; it does not exist yet. Pavel: an installer could start all services and LGS with no game, to test the components on real hardware and walk the setup screens.

**First markets.** Igor recalled the first NOVA product was to be Dakota (mystery progressive). Irina and Pavel: Dakota certification is too slow for a first product; start where fixes do not need two or three labs. Val: first Texas, second probably Georgia.

**How the ISO is made.** Val described the future flow: a person talks through a game idea → a brief → the agent makes the game → it goes to a repo → actions build an ISO. Pavel: the ISO comes from a separate integration repo. It takes the game sources, or a released game artifact, runs tests, and packs it with the math and LGS.

**Plan to Tuesday.** Val: math is ready and LGS is ready to some degree, so why not build now? Anton will have a game Monday. Evgeny: he said LGS will work, not that the build is ready. The build needs actions in the integration repo to finish the full cycle. It might be ready Tuesday. Val: then build the first ISO on Tuesday. Evgeny asked whether everyone except the urgent Georgia work moves to this. The urgent Georgia work is adapting the LTE mobile modem for the GA-COAM release (confirmed by Val after the meeting). Val said both must be done in parallel. Evgeny's game-design agent moves to the next plan. Andrei: he cannot help with the build; that is Evgeny and Pavel. CI/CD comes after the build process, with Dima Chudinov or Sergei Tsimanov. Evgeny asked whether the game repo will be ready Monday with contracts. Anton: the game will run, but contract compliance was not confirmed (the transcript is garbled here). Val: he is fine if they promise and miss. Andrei and Pavel expect hidden problems.

**Other.** Andrei and Alexander praised Anton. Val asked Andrei about his email on running Claude Code locally ("Клатр регион" in the transcript). Claude Code commit expenses average about $15,000 a month (confirmed by Val after the meeting), and running it locally could save that. Andrei had not read it. Pavel thinks it is likely true and asked how it is set up on GitHub.

## Decisions Made

- **Definition of done for NOVA builds** — built by CI/CD actions, on the production server, downloaded by link, put on USB, the machine runs. A quick local performance build is allowed as an extra step. (Decided by Val; Pavel and Alexander agreed)
- **First ISO with a game targeted for Tuesday, Nov 17** — Anton's game Monday, Evgeny's build actions by Tuesday. Missing the date is acceptable. (Decided by Val; Evgeny agreed)
- **Evgeny's game-design agent moves to the next plan** — to free him for the build. (Decided by Val)
- **Build process first, CI/CD after** — CI cannot be built before the build exists. (Andrei; Val accepted)
- **Market order: Texas first, then probably Georgia** — Dakota is not first because certification is slow. (Val, with Irina and Pavel)
- **Undertaking taken: make the production download screen show new products** — how (extend today's screen or a separate portal) is still open. (Val)
- Considered and dropped: using the old Data Center instead of LGS — it lacks the modular services, the new API and the math server link. (Alexander withdrew)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Anton Leshkevich | Finish the Lions Riches conversion and deliver a game repo that runs | Mon Nov 16, 2026 | High | Input for the first ISO |
| 2 | Anton Leshkevich | Play the new build and share results with the team | Fri Nov 13, 2026 | Normal | "Today I will try to finish and share" |
| 3 | Evgeny Kharetski | Write the integration repo actions that build a full ISO (LGS, services, math) | Tue Nov 17, 2026 | High | "Might be ready Tuesday" |
| 4 | Evgeny Kharetski | Add Anton's game repo to the build and produce the first ISO | Tue Nov 17, 2026 | High | Pavel supports the build |
| 5 | Andrei Bosik | Top up the corporate OpenRouter account | Nov 13, 2026 | High | He had trouble logging in to the site |
| 6 | Andrei Bosik, Anton Leshkevich | Call to cut OpenRouter costs | TBD | Normal | Andrei's ideas from the usage analytics |
| 7 | Andrei Bosik | Read Val's email about running Claude Code locally (Claude Code commits average ~$15K/month) and report | TBD | Normal | Pavel asked how the local setup works on GitHub |
| 8 | Andrei Bosik | Build CI/CD after the first build, with Dima Chudinov or Sergei Tsimanov | After Nov 17 | Normal | |
| 9 | [Unassigned — needs Val's confirmation] | Make the production download screen show NOVA builds; hold a separate meeting on extending vs a new portal | TBD | Normal | Screen built by Dima Chudinov and Sergei Tsimanov |
| 10 | Anton Leshkevich | Refactor the repo to a standard stack before giving tasks to Igor and Evgeny (Zhenya) | TBD | Normal | After Lions Riches |

## Open Questions

- LGS integration: threads, sync or async saves to the data center (8 ms per save in RAGE), and an LGS agent in the flow. (Igor)
- Does the Art agent use Igor's JVL style skill, or only its own guideline from RAGE scenes? (Val, Igor)
- Will Anton's game follow the LGS contracts by Monday? Not confirmed. (Evgeny)
- Hardware services are not in the ISO, and peripherals were tested only in emulation. (Evgeny)
- Installer that starts all services and LGS with no game, to test hardware early — not decided. (Pavel)
- Compose file to run the full stack on any PC with emulated hardware — not built. (Evgeny)
- Automating NOVA capability requests from the game agents (Val's parallel flow) — manual for now. (Val, Anton)
- Direct Anthropic API key vs OpenRouter. (Anton)
- Who gives work to Igor and Evgeny (Zhenya) now. (Val)
- Resolved by Val after the meeting: "Клатр регион" = his email on Claude Code commit costs (~$15K/month); "Джорджилтеямадем" / "алто я мадам" = adapting the LTE mobile modem for the GA-COAM release. "Liashkevich" and "Leshkevich" are the same person; this vault uses Leshkevich, as Teams shows.

## Dispatch Log

---
*Processed from a Teams transcript (.docx export) on November 13, 2026*
*Source meeting: NOVA-2 follow-up - Friday check*
