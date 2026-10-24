# Meeting Summary — Review - Dutch Mill on NOVA, first iteration
**Date:** October 21, 2026, 8:02 AM – 9:35 AM Eastern
**Duration:** about 1 h 32 min
**Attendees:** Val Levitan, Igor Metelski, Anton Leshkevich, Alexander Biratko, Pavel Frolov, Irina Shishko, Evgeny Kharetski
**Raw transcript:** [[Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026]]

Held in Russian. Some names and terms are garbled in the transcript.

## Summary

**Dutch Mill on NOVA.** Igor showed the vertical Dutch Mill ported to NOVA. All bonuses work. The progressive bonus was weak in the Rage version and is still a little unfinished. Igor wrote acceptance criteria and requirements linked to a capability (still a local draft). He built a test harness and test scenario; the harness needed a second session to run. Work took about one session for the port, a parallel session for tests, and about 2 hours to fix defects he saw. Requirements grow with each port.

**New vertical game for Texas (Midnight Money).** In parallel Igor made a vertical version of the horizontal Midnight Money. He used the screen layout of Lion's Rich (GCOAM 3, 5 reels × 3 symbols) and the theme and math of Midnight Money. Art (night forest, moon, wolf) was generated: Claude wrote prompts, ChatGPT made images, then segmented and animated. Symbols were regenerated; free spins were redone. About 1 day for art and half a day for symbols. It runs on Rage only so far. Texas now has 3 vertical games: one on NOVA, two on Rage only. Val: the point is that a designer can describe a theme in words and the game is built by software. Val asked why ChatGPT and suggested trying Grok. Pavel noted OpenRouter rankings for image tools.

**Drop the browser: native engine.** Anton Leshkevich (who also converted Clover Fortune from Nebraska to NOVA) raised the architecture. NOVA runs in a browser, a legacy of online games. He rewrote part of NOVA in Rust locally, with a small renderer for Spine and Miranda assets; LGS integration stays. Same speed (60 fps cap). RAM use is about half; with compressed images about 700 MB against 2,700 MB today. Measured on his laptop only. On the RK3576 board video and system share one memory, so memory may be the bottleneck. Val, Alexander and Pavel support removing the browser. Alexander: the browser blocks video work and video sync. Nobody wants to keep a browser build next to the native one.

**Rule before code.** Val: no code until capabilities, requirements and acceptance criteria exist; then architecture that Val can read; then features and code. Anton, Evgeny, Igor and Alexander agreed out loud.

**What Val wants in the new platform.** Drop Unity/Miranda. Comfortable tools for designers (they describe a design in words and see the build). A layer that breaks a competitor game (from video) into geometry, motion and timing, and keeps growing. A CI/CD layer that pushes a game through NOVA to the machine without errors and audits it. Remote upgrade of machines in the field, with proof the upgrade is 100% correct. Keep using Rage experience. First steps: remove the browser and Pixi; add the tested download flow with GLI signature checks.

**Remote game updates.** Pavel: new math most likely needs regulator notice; a new version of the same game (new art, same math and settings) may not. Irina: in Georgia only SAS/LGS is certified; Intralot must still know. Val wants a chatbot that deals with Intralot and wants Andrei Bosik aimed at it.

**MVP1.** Val: MVP1 = a stable NOVA on which JVL releases 6 games for Texas. Take a step-by-step path, not a radical one. Val gives 10 days at most; Anton said this is optimistic.

**Engine needs (first list).** Alexander: skeletal animation, images, video, text and fonts; later particles. Alexander proposed shaders on still images instead of heavy video; Igor wants a test first (can be tried in Pixi). Igor asked whether a full designer editor is needed or scenes could be built through a chatbot; Alexander wants the AI to take screenshots and debug itself. Pavel takes the update part.

**Product owner.** Val wants a product owner who does not code on this project (product owner and developer are conflicting roles), and who thinks, not only administers. Andrei Klimovich is the model. Alexey Khamin was raised; Pavel disagreed. Andrei Klimovich has no time. Val: Vladimir Samusenko is the best candidate (back Monday, Oct 26); he needs a written persona of the role and support. Backup: Alexander Biratko as more of an architect (Val: not a good idea).

Val praised Anton, Alexander and Igor.

## Decisions Made

- **Remove the browser from NOVA and move to a native engine; no browser build kept.** — Lower memory, more control on the target board. (Val, Anton, Alexander; Pavel agreed)
- **No code before capabilities, requirements, acceptance criteria, then readable architecture.** — Val's rule. (Val; Anton, Evgeny, Igor, Alexander agreed)
- **No separate board test in Minsk of Anton's prototype.** — Val already ordered the board for Anton and the outcome is known. (Val; Alexander agreed)
- **NOVA MVP1 = stable NOVA that releases 6 Texas games; step-by-step transition, not radical.** (Val)
- **Vladimir Samusenko is invited as product owner; Pavel prepares the role description and meets him.** (Val)
- **Capability drafts go first into one file per person in a new repo, then grooming, then AI merges into Jira.** — Pavel's method; Val agreed. Local work only a couple of hours, then push. (Pavel, Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Write the product owner role description and hold a meeting with Vladimir Samusenko to invite him | Mon Oct 26, 2026 | High | Samusenko back from vacation Oct 26 |
| 2 | Anton, Igor, Alexander, Evgeny, Pavel, Irina | Each write own use cases, personas and capabilities for the new NOVA engine and platform, one file each in a new repo | Mon Oct 26, 2026 | High | Push after a couple of hours of local work |
| 3 | Pavel Frolov | Write capabilities and requirements for the game update part | TBD | Normal | Pavel volunteered |
| 4 | Anton Leshkevich | Ask Andrei for a repository and upload the Rust prototype | TBD | Normal | Code lives only on his disk now |
| 5 | Team with Samusenko | Groom the capabilities for NOVA MVP1 | Tue Oct 27, 2026 | High | |
| 6 | [Unassigned — needs clarification] | Create the new repo / project for the capability files | Before Oct 26 | Normal | Pavel proposed it; owner not named |
| 7 | Andrei Bosik | Chatbot that deals with Intralot | TBD | Low | Val's wish; Andrei was not in the meeting |

## Open Questions

- Does the rule "Nebraska 2 is the last product on Rage" still stand? (Igor) Val only said NOVA will come fast.
- Can shaders on still images replace heavy video? Needs a test. (Alexander, Igor)
- Keep the old scene structure, or a new one? (Igor, Alexander)
- Full designer editor, or scenes built through a chatbot? (Igor, Alexander)
- How to update games remotely when math changes, and what each regulator requires? (Pavel, Irina)
- Who is product owner if Samusenko does not work out? (Val)

## Dispatch Log

---
*Processed from Teams transcript on October 21, 2026*
*Source meeting: Review - Dutch Mill on NOVA, first iteration*
