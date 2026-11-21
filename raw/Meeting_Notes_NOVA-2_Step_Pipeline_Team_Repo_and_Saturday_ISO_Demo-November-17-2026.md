# Meeting Summary — NOVA-2 follow-up - Tuesday check
**Date:** November 17, 2026, 8:04 AM – 9:33 AM Eastern
**Duration:** ~88 minutes
**Attendees:** Val Levitan, Anton Leshkevich, Igor Metelski, Pavel Frolov, Irina Shishko, Evgeny Kharetski, Alexander Biratko, Andrei Bosik
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_NOVA-2_Step_Pipeline_Team_Repo_and_Saturday_ISO_Demo-November-17-2026]]

## Summary

**Anton: what he learned.** Anton's tool built Lions Riches, but badly (symbols overlap, not sorted). Three problems: (1) big tasks are done poorly; (2) big tasks burn many tokens, because agents get confused, take each other's tasks and go in circles, especially the central Builder agent; (3) Igor's tools and Anton's tools were glued together with old paths and prompts, so he polishes each agent as he adds it. Small tasks work well: a button fix took about 10 minutes and 20 cents. Over the weekend he tried a model with an 83% discount; a cheap Chinese model (DeepSeek) could not call the right agent, Claude Sonnet plans well. Val asked if he tried Fable; he has not. He is adding analytics tools to see where agents get stuck and where tokens go.

**Val: quality first, cost later.** Val said: do not focus on a cheaper model now. First make it work well and correctly with any model, whatever the cost. Then work on the economics. Anton accepted.

**New approach: step-by-step pipeline.** Anton wants to remove the central agent that runs all others and build a more deterministic, step-by-step pipeline. Example: step 1 load the brief; step 2 create symbols with Igor's tools; and so on. Between steps either save and move on, or put a required human review. Known parts (reels, symbols, paytable, logo, background, free spins) can follow templates; agents are used for art and new features. Some steps can run in parallel. Val accepted: this lets the team merge steps or add AI checks as AI grows, until full automation. Igor: his old slot-art tool already worked step by step (main scene art → accept or reject with a reason → layers → paytable → reel frame). Igor: Anton's game breaks style, but follows all JVL geometry rules (paytable, character, logo, symbols in the right place). That is a good result.

**Review by AI, style book, references.** Pavel: the review block can be shared: two AI networks rate each result and a human makes the final call; the networks then learn why things are rejected. Val: criteria can grow all the time. Evgeny: load JVL's style book so games look like past JVL games. Val agreed and added there can be several style books (e.g. a more cartoon style, as competitors moved to). Andrei: artists use reference pictures about 80% of the time. Evgeny: his brief agent takes references; they go with the brief into the GitHub repo. Igor: image generation is a large separate task. Of ChatGPT, Midjourney, Grok and Google's model, only ChatGPT followed "all art in the top half" for a vertical game.

**From solo work to team work.** Val praised Anton's breakthrough and asked to move from "single combat" to "academic rowing" (team work) so Igor and Evgeny join. Anton: the converter lives in the engine repo, which is wrong. He will make a new repo with clean code for team work, and talk with Igor and Evgeny (Zhenya) tomorrow. Igor asked Anton to organize the repos so people do not block each other. Name of the tool was not fixed ("NOVA builder", "game constructor", "studio"; Alexander: "Unity plus Miranda").

**Igor: Twin Bison on NOVA-2.** Igor asked Claude, on a separate branch, to port Georgia game Twin Bison to the current NOVA-2 engine. It worked well. The game talks to a locally running LGS over WebSocket and gets game outcomes. Claude can see the screen through a local port, take screenshots and check screen elements. Alexander: keep the engine (driven by any AI) separate from the game-building system. Anton: in his tool, LGS is not integrated yet; all mocks.

**What is the artifact.** Igor: the ISO is the full product put on the machine (game, LGS, peripheral libraries, printer, bill validator, maybe a local progressive controller). Evgeny's ISO already builds and installs with math, but has no game. A game is a runner (Lua script player, one Linux executable) plus Lua scripts plus assets. Pavel: each game is a signed package, mounted at boot; the launcher loads it. An update swaps one package for another. Igor: the game list must also match on the LGS/SAS side. Pavel: keep this in one place, not several files as in RAGE.

**System messages.** Alexander: put Igor's game in Evgeny's ISO, run it, and see what is missing, mainly system messages. Igor: Claude has not been able to pull everything useful out of RAGE. Irina: RAGE has dictionaries with all messages; give them to Claude. Alexander suggested going back to the old comms system to add the missing messages fast. Igor objected (he prefers WebSocket; RAGE syncs to the data center in the main thread, 8 ms per save). Val: build a proper, standard message library, the same way Igor did the other layers. Evgeny: NGS is about 4 months behind; about 90% of the RIS/promo work is "crutches" and should be redone later, after everything is built and works.

**Languages.** NOVA-2 is in Rust and Lua. LGS and progressive stay in Java; JavaScript for the front end. Val asked someone to send him the name in chat.

**Test builds and production downloads.** Andrei: CI is built correctly but has nowhere to publish yet. Evgeny: test builds stay on a local office computer; downloading about 3 GB from Amazon for each test build is too slow. Val agreed: local is for testing; he means production. Andrei: production needs Dima Chudinov to write an app that registers machines. Val suggested extending the screen Dima is building (for Flex PaySlim). Andrei objected: machines are a separate product with their own portal, not the transactional portal, as agreed before; this needs its own meeting. Val gave in.

**Source of truth for requirements.** Alexander and Irina proposed acceptance criteria. Val first said they must come from prose. Igor: prose written from NOVA-2 games only proves NOVA-2 works like NOVA-2. The only source of truth is the RAGE engine and games (a working product). So write prose from RAGE and pull capabilities and requirements for NOVA-2 from it. Val: then that code must come out of SVN into GitHub. Andrei and Alexander: only the prose is needed; it can be generated locally. After a vote, Irina takes it: Claude writes, Irina checks what is right.

**Next milestones.** Pavel: next, make the same build for RK3576 (ARM), so all tests pass on any platform; this is more like 2–3 weeks. Services (bill validator, IO board) must build for ARM as on x86 (FP7). Evgeny will do all build and service work himself. Pavel: RK has only one HDMI output; there is one two-monitor stand (at Daniil's desk); more are needed, or Evgeny takes Daniil's. Val asked for RK this Saturday; Evgeny and Andrei said no, x86 must be finished first. Val: Wednesday then. Pavel: next milestone is an RK build with services and no game. Pavel's estimate for real results: about Dec 4. Alexander: confirm dates again on Saturday. Pavel: idea of multi-arch Docker containers (x86 and ARM binaries in one image); Igor asked why use containers on machines; Evgeny: same environment everywhere; RK is the target, if containers lag, they go.

**End of year and the plan to March.** Val: by year end the design team should be able to make games the new way. Andrei: a demo of the workflow is certain; designers will have many comments. Val asked to keep all of this confidential and warned about talks with Lena: if the design team gets an unfinished platform, they will find a way to reject it and the company stops. Val (confidential, "nobody knows"): a known industry producer starts January 15 under contract. From Jan 15 the team gives him a working product (CI/CD, ISO on a machine with a mobile modem). Jan 15 – Mar 15: polish the system. From Mar 15: hand it to Lena and the team. Math must then be finished.

## Decisions Made

- **Quality first, cost later** — make the tool work well with any model; optimize cost after. (Val; Anton accepted)
- **Builder becomes a step-by-step pipeline with human review between steps** — automate steps later as AI grows. (Proposed by Anton; accepted by Val)
- **Anton's work becomes team work** — new clean repo for the converter, Igor and Evgeny join. (Val; Anton proposed the repo, no objections)
- **Next meeting Saturday Nov 21, 10 AM – noon Eastern** — moved from Friday at Igor's request; show the first ISO artifact (x86, "on crutches"). (Val)
- **Build a proper standard system-message library** — not a return to the old comms system. (Val; Alexander's revert idea dropped after Igor objected)
- **Test builds stay on a local office computer; production goes to S3/Amazon later.** (Evgeny, Andrei; Val agreed)
- **Machine builds get their own portal, separate from the transactional portal** — Val withdrew his idea to extend Dima's screen; a separate meeting is needed. (Andrei; Val gave in)
- **NOVA-2 requirements come from prose written from the RAGE engine and games**, not from NOVA-2 games; Irina verifies. (Igor, Alexander, Andrei; voted, Val accepted)
- **RK3576 not this Saturday; next milestone Wednesday Nov 25: RK build with services, no game.** (Val, after Evgeny and Andrei; Pavel)
- Considered and dropped: going back to the old comms system for messages (Alexander).

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Anton Leshkevich | Move the converter out of the engine repo into a new repo with clean code for team work; build the first step-by-step pipeline prototype | TBD | High | |
| 2 | Anton Leshkevich | Call with Igor and Evgeny (Zhenya) to show the new setup | Wed Nov 18, 2026 | Normal | "Tomorrow" |
| 3 | Igor Metelski | Set up CI for games and put Twin Bison into the ISO so it runs on a machine | Sat Nov 21, 2026 | High | For the Saturday demo |
| 4 | Evgeny Kharetski | Continue the ISO build (x86, FP7) and support Igor so the build includes a game | Sat Nov 21, 2026 | High | |
| 5 | Evgeny Kharetski | Make the services (bill validator, IO board) and the build work on RK3576 (ARM) | Wed Nov 25, 2026 | High | Pavel: full result ~Dec 4 |
| 6 | Alexander Biratko | Build the system-message library through Daniil (guide and check him) | TBD | Normal | Covers tilts and all non-game messages |
| 7 | [Unassigned — needs Val's confirmation] | Invite Daniil to the Saturday meeting, if he wants to come | Sat Nov 21, 2026 | Low | He works mornings and studies |
| 8 | Irina Shishko | Have Claude write prose from the RAGE engine and games, pull NOVA-2 capabilities and requirements, and check them | TBD | Normal | Voted by the team |
| 9 | Pavel Frolov | Get more two-monitor RK stands, or give Daniil's stand to Evgeny | Wed Nov 25, 2026 | Normal | RK has one HDMI output |
| 10 | Alexander Biratko | Re-confirm the RK milestone dates at the Saturday meeting | Sat Nov 21, 2026 | Normal | |
| 11 | [Unassigned — needs Val's confirmation] | Hold a meeting on the production download portal for machines (separate from transactional) | TBD | Normal | Needs Dima Chudinov |

## Open Questions

- Who sends Val the name of the scripting language (Lua) in chat. (Val)
- Multi-arch Docker containers on machines, or not. (Pavel, Igor)
- How game patches and the game list are kept in one place across launcher, LGS and SAS. (Igor, Pavel)
- Does the WebSocket link to LGS still run in the main thread? (Anton asked; Igor did not know)
- Name of Anton's tool. (Val, Alexander, Igor)
- Name check: "фаббул/фейбл" in the transcript = Fable (model); "Twin Bison" read from "твинбайс / thind bys".

## Dispatch Log

---
*Processed from Teams transcript on November 18, 2026*
*Source meeting: NOVA-2 follow-up - Tuesday check*
