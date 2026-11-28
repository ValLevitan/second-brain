# Meeting Summary — Nova standup meeting
**Date:** November 25, 2026, 6:19 AM Eastern
**Duration:** 33 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Igor Metelski, Irina Shishko, Daniil Stauskiy, Evgeny Kharetski, Anton Leshkevich
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Nova_Standup_Four_Games_Efim_Math_and_RK_Image-November-25-2026]]

## Summary

**Capabilities and MVP 1 (Alexander).** Alexander made new capabilities from yesterday's meeting, some for the studio and some for LGS. All now carry the NOVA label. He has not set the release yet. He waits until Daniil and Pavel review their items; then the closed ones can get MVP 1. Pavel set his own to review; their child items are closed.

**Showing a game in MVP 1.** Alexander: the framework cannot be fully proven without a game (for example bonus and credit counting in the bonus). Pavel: we can show the base game. Igor: four games are ready, with bonuses. Irina: they spin, but nobody has checked them yet.

**Math for the games.** Igor: the Georgia games use three kinds of progression. Math exists for some; it must be checked with Efim. A week ago Efim said he had not yet made the math for the match-3 progressive games for NOVA. It is old math; Efim only has to move it into his project and handle the preset at start-up. Pavel: we can already connect to the remote math server, if Efim adds what is needed. Irina wrote to Efim during the meeting.

**Games (Igor).** Igor finished the four games and merged main into his branch; the build passes. Pavel: the integration branch now gets everything at once; it should be one game, one merge. Igor agreed. The old Dragon Pays game still sits in the NOVA repository. Andrei made repositories and Igor uploaded all games; Evgeny has the links. Next Igor checks several games running together through the game select screen, and memory use (unload resources of inactive games), locally first. The select screen needs rework: the game icon with the "liquid glass" effect will live in each game's repository. Igor starts this now. Alexander will make a capability for it if none exists; Pavel found a game select screen capability with a feature from Daniil.

**Engine (Daniil).** Daniil closed one feature and its stories. He is working on the machine-state feature (number heard as 1353). He will finish it tomorrow, then start showing the screens on the engine side. He is also checking Alexander's capabilities: what the engine already has and what not.

**RAGE and LGS.** A speaker (labeled Alexander Biratko, right after Pavel called on Evgeny) said: almost all NOVA Jira items for RAGE are closed; the RAGE data center is fully moved into LGS. Open points remain, for example the modem, which will move to a separate service. The GitHub page was updated to be easier to use. Igor's new games will be added next. LGS needs more changes so match and progressive settings go to Efim's math without the games.

**ARM builds and the RK image.** Pavel: all services now build for ARM. Evgeny agreed; he was not sure about math, and Pavel said he did the math build. Pavel wants to try an RK image with only LGS in setup, even without games. Evgeny can add this to the builder but needs Pavel's inputs. Pavel works today on whether the system is ready to go into an image. Evgeny expects it tomorrow.

**How to build the math.** Efim selects math with a config file, and an action builds that set. Pavel: maybe a page to pick the math on the fly. Evgeny: better to pick the games and pull their math in automatically, or put all current math into the image (even 1,000 games is not large), so games can be added later. Pavel: earlier there were blockers; this may suit debug builds, but how labs check production builds needs thought. Pavel and Evgeny want a general call with Efim on this.

**Studio (Anton).** Anton is finishing the base-game step and hopes to finish today. After a brief is imported, all symbols and base-scene parts are now made procedurally by default. They can then be redrawn one by one with AI. The aim: the game is playable right after import. Pavel suggested a lock button on the component controls; Anton agreed it makes sense.

**Effects and parallel work.** Igor proposed setting flight effects (point A to point B) with curves in the interface. Pavel: later. Alexander asked how the studio will offer ways to make such effects (sprite, video, shader, code, Spine). Anton will think about it. Alexander proposed scenes and resources made from templates, with the brief's plan showing which parts are done, so several people can work in parallel. Igor added that studio projects need a shared format for this. Anton: good for a future version. For now the studio stays single-user with a fixed order of steps, because it is easier to manage dependencies. A big rebuild has no time now. Igor: come back to it before about January 15. Anton will ask for a backlog item.

**Help screens.** Alexander added a studio step to create help screens. Igor: help text needs a format for symbol substitutions and text formatting. Evgeny: the brief agent asks only what is in the brief, and current briefs hold only line textures for help. The GDD will be generated from the brief (Irina, Pavel), so the brief must describe the help content. Pavel: check how Lua does string substitution.

## Decisions Made

- **One game, one merge into the integration branch.** — Not everything at once. (Proposed by Pavel; Igor agreed)
- **The studio stays single-user with a fixed order of steps for now. Template-based parallel work comes in a later version.** — No time for a big rebuild now. (Anton; Pavel)
- **The curve-based effect editor is postponed.** (Pavel)
- **The brief must describe the help screens**, because the GDD will be generated from the brief. (Alexander; Irina and Pavel agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Irina Shishko | Push Efim on the match-3 progressive math for NOVA | Nov 25, 2026 | High | She wrote to him during the meeting |
| 2 | Igor Metelski | Test several games together through the game select screen and profile memory, locally first | TBD | High | |
| 3 | Igor Metelski | Rework the select screen so each game repository carries its own icon | Nov 25, 2026 | Normal | "Starting now" |
| 4 | Alexander Biratko | Create a capability for the select screen work if none exists | TBD | Normal | Pavel found one with Daniil's feature |
| 5 | Alexander Biratko | Set the MVP 1 release on capabilities after review | TBD | Normal | After Daniil and Pavel review |
| 6 | Daniil Stauskiy | Finish the machine-state feature, then start engine-side screen display | Nov 26, 2026 | Normal | Also checks Alexander's capabilities |
| 7 | Pavel Frolov | Check if the system is ready to go into an RK image and give Evgeny the inputs for the builder | Nov 25, 2026 | High | |
| 8 | Evgeny Kharetski | Add the RK image build to the builder once Pavel's inputs arrive | Nov 26, 2026 | Normal | |
| 9 | [Unassigned — needs clarification] | Set up a general call with Efim on how the math is built and configured | TBD | Normal | Pavel and Evgeny both raised it |
| 10 | Anton Leshkevich | Finish the base-game studio step | Nov 25, 2026 | High | |
| 11 | Anton Leshkevich | Think how the studio offers ways to create effects; consider a lock button | TBD | Low | |
| 12 | Anton Leshkevich | Ask for a backlog item for template-based parallel studio work | TBD | Low | Revisit before about Jan 15 |
| 13 | [Needs Val's confirmation] | Add Igor's games to the GitHub page; change LGS to pass match and progressive settings to Efim's math | TBD | Normal | Speaker labeled Alexander Biratko; may be Evgeny |
| 14 | [Unassigned — needs clarification] | Add a description of the help screens to the brief | TBD | Normal | |

## Open Questions

- How will labs (GLI) check a production image that holds math for many games? (Pavel, Evgeny)
- Does math exist for all Georgia game types, especially match-3 progressive? Waiting for Efim. (Irina, Igor)
- Format for help text substitutions and formatting. (Igor)
- Heard unclearly: who gave the RAGE/LGS update (label says Alexander Biratko); task number "1353"; Daniil's closed feature number; "228".

## Dispatch Log

---
*Processed from Teams transcript on November 25, 2026, ~12:30 PM Eastern*
*Source meeting: Nova standup meeting*
