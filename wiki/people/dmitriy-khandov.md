---
type: person
title: Dmitriy Khandov
date: 2026-07-13
aliases: [Dmitriy Khandov, Dmitry Khandov, Dima Khandov, Dima, Jim, Dima Handoff, Dima Khandrov]
disambiguation: "Senior 3D Graphic Designer (graphics/3D/video). Dima/Dmitry cluster (3, owner-ruled): [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]=IT / [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]]=Senior 3D designer / [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]=back-end. Resolve by context; queue if none."
source-count: 25
---

# Dmitriy Khandov

Dmitriy Khandov (called "Dima") is JVL's **Senior 3D Graphic Designer** (owner-confirmed 2026-07-13), working with Lena on the game art and video side. Canonical spelling **Dmitriy Khandov**; transcript variants (Dmitry, Dima) kept as aliases. He is a **distinct person** from [[wiki/people/andrew-khandov.md|Andrey (Andrew) Khandov]] — same surname, different people — and is **not** the IT "Dima" ([[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]).

## Role

- Produced the 13 simultaneously running HD videos used as the test scene for the FP7 hardware performance test that Alexander Biratka ran. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Explained that the V-Deck videos are actually full HD (only visually half), and pointed out that "spine" objects ran smoothly without the delays seen in the video files. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Described the animation-controller feature in "Miranda" that can swap objects without needing programmers, and discussed the extra effort of combining spine animation with video effects. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Agreed with Lena that putting the Fortune Fu Paws game on the FP7 board is doable but with a lot of optimization effort. [[raw/fp-7_performance_analysis_january_13_2025.md]]

## Game design and the FP7 asset manifest (Jan 16–17)

- On the Jan 16 game-design review, Dima's team works on integrating math into bonuses (using placeholder image folders in Miranda to run and playtest the math). [[raw/game_design_january_16_2025.md]]
- On the Jan 17 FP7 bottleneck meeting, Val tasked Dima Khandov with writing the **asset-creation "manifest"** (due Feb 15) — the guideline telling graphic designers how to build video/spine assets within the FP7 platform's limits. That undertaking is tracked on [[wiki/decisions/2025-01-17-remain-on-fp7-hardware-ceiling.md]]. See [[wiki/topics/fp7-hardware-platform.md]]. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Git-LFS / VS Code onboarding (Feb 18)

- On the Feb 18 onboarding session, Aaron coached him hands-on through VS Code setup (Git Graph / Actions plugins, signing into Copilot) and committing via the source-control view. The WEBVTT speaker labels name him **"Dmitriy Khandov,"** confirming that *this* meeting's "Dima" is this design/video engineer (Val groups "Lena and Dima" as the graphics-team pair to onboard for LFS commits). A separate attendee, [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], is present too — a distinct person. See [[wiki/meetings/2025-02-18-git-lfs-vscode-onboarding.md]]. [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]

## Graphics onboarding + math test tool (Feb 21–26)

- **Onboarding lead (Feb 21):** Dima wrote the artists' Git/VS Code onboarding **instructions** (first in Russian, to translate to English), which Val praised ("Dima did a great job"). Val tasked him to put **Nastia and Julia** onto GitHub Monday/Tuesday and act as the artists' first point of help. He committed a first comp-art file to demonstrate. See [[wiki/decisions/2025-02-21-separate-game-and-design-repos.md]]. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- **Core-four designer (Feb 26):** one of the four (with Lena, [[wiki/people/yulia.md|Yulia]], [[wiki/people/anastasia.md|Anastasia]]) being made comfortable with the branching workflow before Juan/Michael are rolled in. See [[wiki/decisions/2025-02-26-designer-branching-workflow.md]]. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- **Math/mass test tool (Feb 21):** Dima and [[wiki/people/andrew-khandov.md|Andrey]] Khandov are building a primitive playable game version connecting **Miranda to the math ("mass") server**, so Michael and Efim can play-test the real math with placeholders. See [[wiki/topics/slot-game-design-principles.md]]. [[raw/game_design_meeting_february_21_2025.md]]

## Mostly on Miranda + the Miranda catch-up PR (Mar 12)

- On [[wiki/people/lena.md|Lena]]'s Mar 12 animation walkthrough, she confirmed Dima "lately not doing a lot of game graphics, he is mostly focused on **Miranda**," and that he **worked on integrating the math into Miranda** so games can run with comp-art placeholders for fast play-testing (and, with Andrey, is finishing the math/mass-server integration for **Miranda 9**). See [[wiki/topics/game-art-animation-production-pipeline.md]]. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
- On the Mar 12 GitHub graphic-design check-in, Dima's **~940-file Miranda catch-up commit** was the pull request Yulia approved in an hour — cited as the legitimate "special case" for a giant PR. He is also named as someone Lena can give access to "fake the review" of new-game commits. See [[wiki/topics/graphics-team-git-workflow.md]]. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- On the Mar 12 Gottlieb call, Michael's model for parallel work had **"Dmitri develop animations"** while Lena imagines them — a mention of Dima on the animation-production side. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## Miranda product-ownership coaching (Mar 2025)

- On the 3-part Miranda session ([[wiki/meetings/2025-03-21-miranda-explainer-and-product-ownership.md]]; date inferred from transcription stamp), Aaron coached "Dimitri" — resolved by context to this page (the Miranda-focused Khandov; cf. Lena's Mar 12 "mostly focused on Miranda" and Val's Feb 10 "Dima Khandov comes to me… let's design this feature in Miranda") — to act as **Miranda's product owner**: "you're in control of releasing it… negotiating it with JVL… talking with Pavel and Arena [garbled — Irina? Lena?] and others to develop it further… the negotiator for this product." [[raw/Even more on Miranda.md]]
- The same coaching refers to "your dedicated developer for Miranda", working with him on it. *(Inference: that developer is [[wiki/people/andrew-khandov.md|Andrew Khandov]], the owner-confirmed C# Miranda developer. Not stated by name in the source.)* [[raw/Even more on Miranda.md]]
- Aaron's asks: think in backlog order ("the timeline view in JIRA is the actual backlog"), plan around the developer's real capacity (vacations, fatigue), and replace the "flat wall" Confluence feature lists with roadmap + storytelling. See [[wiki/topics/miranda-authoring-tool.md]]. [[raw/Even more on Miranda.md]]

## Proposed move to the core-technology team (Mar 24–25 2025, dates inferred — proposal, not enacted)

- On the DevOps-container sessions Val proposed: "**Dima Khandov… should be transferred from graphic design team to core technology team**. And he should be driving the core technology… the requirement. Like he should always be saying, I want, I want, I want" — covering core software *and* hardware technologies — with [[wiki/people/alexander-biratka.md|Sasha (Alexander)]] as the implementer who "doesn't do anything without any requirements." Aaron agreed ("the more people you bring into this, the better"). Val's illustration: "if Dima says… I'm developing a new trick up my sleeve and I want it to be done a certain way, please provide me a technological runway for it" — negotiated requirements with dates. Recorded as a **proposal**; no enactment visible in the sources. See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/devops_container_approach_for_omni_3.md]]

Note: the transcript once addresses him as "Jim" ("What do you think, Jim?") — likely a transcription slip for Dima. His involvement is strictly the design/video side. The separate "Dima" in the Jan 20 GitHub/DevSecOps meetings, the GitHub admin seat, the Jan 22 Minsk IT-structure app-support role, and the "Observability Platform" org — all **IT-context** — is **[[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]**, JVL's IT person (owner ruling 2026-07-13), NOT this designer.

*(Personal matters removed — owner ruling 2026-09-28.)*

## Calle Ocho port plan + the sources/assets convention (Apr 15, "Dima" by graphics context — inference)

- The designer "Dima" on the Apr 15 Omni daily (attributed here by graphics context) laid out the Calle Ocho port order (base game → dashboard → "видег" → tilts → big wins), flagged the math-container question for Efim, and defined the working convention: "ассет это что-то финальное, что идет грубо говоря к Саше. Исходник это исходник" — sources live in the designers' sandbox repo, finished assets are exported into the game repo. See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/daily_omni_progress-apr-15-2025.md]]

## Apr 16 2025 — Omni framework stories (bonus/free-spins)

In the Omni daily "Dima Khandov" worked the framework's game-content features with Sasha — he had coded the bonus skeleton scene (a scene where each symbol is revealed, reused across Coin/GPRF/Diamond/DLT bonuses) and discussed the free-spins "lock symbols" / symbol-overlay effects. Val briefly forgot to send his invite and apologized ("Вы очень важный для нас человек"). Dima + Sasha to write stories/descriptions for the listed features by the next day. [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]

## Apr 17 2025 — the Calle Ocho asset-port middle approach

On the Apr-17 Calle Ocho session ([[wiki/meetings/2025-04-17-calle-ocho-asset-redesign-omni.md]]) Dima proposed the adopted **middle approach** between Lena's fast re-export and Sasha's full rebuild: port as-is what can be, but **properly rework only what recurs across many future games** (e.g. the "pigwin"/penguin effect, a flexible BigWin and Dashboard), and export symbols into **Spine containers** without redrawing them. He is to own the **templates** and the hardest fixes while others parallelize. See [[wiki/topics/game-art-animation-production-pipeline.md]]. [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]

## Apr 28 2025 — Miranda GitHub versioning; commit hygiene coaching

On a short Miranda GitHub session ([[wiki/meetings/2025-04-28-miranda-github-versioning.md]]) Val reviewed Dmitriy Khandov's repo and found a single **"V8" commit of ~12,000 files** ("we asked him to, with all fairness"), stale branches open two months, and commits straight to `main` — "no organizational skills related to keeping a clean, planned release." Versions are to be **Git release tags**, not Jira. A next-day meeting (8 am ET) was set to coach continuous commits. Separately (Apr 30), Val wants Dmitriy's **Unity license placed into GitHub CI** (via the secrets platform) so **Miranda can be built in CI**. See [[wiki/topics/miranda-authoring-tool.md]]. [[raw/miranda_github-apr-28-2025.md]] [[raw/secrets_server-apr-30-2025.md]]

## May 1 2025 — Miranda organizing action list

Following the Apr-28 review, [[wiki/people/aaron.md|Aaron]] met Dmitriy (~Apr 29) and, on the [[wiki/meetings/2025-05-01-organizing-miranda-github.md|May-1 recap with Val]], set him an action list to organise the Miranda repo: create a `.gitignore`, purge logs/libraries, delete stale branches, adopt a packaging/zip strategy, then open a feature branch to integrate the math emulator (which may move to its own repo/product — undecided). Aaron was unsure Dmitriy had fully understood the asks. See [[wiki/topics/miranda-authoring-tool.md]]. [[raw/organizing_miranda_github-may-1-2025.md]]

## May 6 2025 — Miranda cleanup done; "sell me on Miranda"

- On the [[wiki/meetings/2025-05-06-miranda-github-organization.md|Miranda GitHub follow-through]], Dima had executed the May-1 cleanup: reworked the repo so it **rebuilds after a Git checkout**, added a `.gitignore` and `cleanMirandaTool.config`, cut a **V8.1 release**, and built a drag-and-drop **Unity package**. [[wiki/people/aaron.md|Aaron]] coached him on packaging (NuGet/MSI via Andre + Dima K), a README "TLDR", capability docs modeled on Unity's, more verbose PRs, deleting the merged branch, and rebasing to purge the ~782k-line history. Detail on [[wiki/topics/miranda-authoring-tool.md]]. [[raw/miranda_organization_github-may-6-2025.md]]
- On [[wiki/meetings/2025-05-06-the-reason-for-miranda.md|"the reason for Miranda"]], Val asked Dima to "sell me on Miranda" if Unity is embedded; Dima's answer: **Pixie is a light engine, Miranda is a plugin to set data for Pixie**, and Miranda can still play games (spin reels) without it; visual quality "comes from the game designers," not the engine. He described **Unity as "a C++ engine… quite heavy on production"** (conflicts with Sasha's May-1 "C#" — recorded as an open contradiction on the Miranda topic). [[raw/the_reason_for_miranda-may-6-2025.md]]

## May 7 2025 — AI tool adaptation

On the games-design tools session ([[wiki/meetings/2025-05-07-games-design-ai-tools-adaptation.md]]) "Dima Khandov" (transcribed "Dima Khandrov"/"Handoff") had barely started with the new MCP (little time), using Cline mainly for Git; [[wiki/people/aaron.md|Aaron]] suggested his Unity tooling experience (like Miranda) could let him build or clone JVL's own MCP servers. See [[wiki/topics/ai-assisted-development.md]]. [[raw/tools_adaptation_games_design_department-may-7-2025.md]]

## May 8 2025 — MCP-builder candidate; graphics work paused

- On the [[wiki/meetings/2025-05-08-capability-compass-mcp-aaron-session.md|May-8 MCP session]] [[wiki/people/aaron.md|Aaron]] tied his "aha moment" about internal MCP servers to **"Dima Handoff"** (this designer, garble — consistent with the May-7 note that his Unity tooling experience could let him build/clone JVL MCP servers), while clarifying he wasn't saying Dima "should be developing MCP servers." See [[wiki/topics/ai-assisted-development.md]]. [[raw/mcp_servers_for_jvl-may-8-2025.md]]
- On the [[wiki/meetings/2025-05-08-game-design-review.md|May-8 game-design review]], Lena reported Dima's game-graphics work (incl. the math emulator) is **paused** because "Dima is working with **Peryatka** on **Couch** only" (both transcribed, unclear referents — flagged) on more urgent work; he returns to the emulator after a major in-browser push. See [[wiki/topics/game-art-animation-production-pipeline.md]]. [[raw/game_design-may-8-2025.md]]

## June 26 2025 — Omni grooming (bonus tasks; GitHub-planning)

On the [[wiki/meetings/2025-06-26-omni-schedule-grooming.md|Omni schedule grooming]] Dima's side (with [[wiki/people/yulia.md|Yulia]]) has the **bonus** mostly ready (already split, still in process); he's the requirements/visual-features driver who wants the more-powerful **FP-7 board** ("any platform, we max out"). Val's push to move story-level planning into **GitHub Issues** landed on him ("I've never done it… I know where it is but never used it"). §15.8: a joked figure tied to him ("$100,000… that you keep promising") is **held**, not recorded here. See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/OMNI_schedule_grooming-june-26-2025.md]]

## Nov 11 2025 — the Miranda scene-manifest export (graphics spec for testing)

On the Nov-11 graphics-specification call ([[wiki/meetings/2025-11-11-graphics-specification-for-testing.md]]; Val + [[wiki/people/pavel.md|Pavel]] + [[wiki/people/irina-shishko.md|Irina Shishko]], "Dima" by Miranda context = this designer) Pavel said that **when Dima returns from vacation he will extract from the Miranda project the full scene structure** — every component's coordinates, size and nesting (parent/child) — and generate it in a usable form to become QA's layout **reference**. Consistent with his Miranda ownership; the risk flagged was that a wrongly-built scene would propagate an error, so each export must be verified once against a correct game. See [[wiki/topics/game-art-animation-production-pipeline.md]] (Nov-11). [[raw/Specs_graphics.md]]

## Sources

- [[raw/Specs_graphics.md]]
- [[raw/OMNI_schedule_grooming-june-26-2025.md]]
- [[raw/fp-7_performance_analysis_january_13_2025.md]]
- [[raw/game_design_january_16_2025.md]]
- [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- [[raw/game_design_meeting_february_21_2025.md]]
- [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
- [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- [[raw/Even more on Miranda.md]]
- [[raw/devops_container_approach_for_omni_3.md]]
- [[raw/daily_omni_progress-apr-15-2025.md]]
- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]
- [[raw/miranda_github-apr-28-2025.md]]
- [[raw/secrets_server-apr-30-2025.md]]
- [[raw/organizing_miranda_github-may-1-2025.md]]
- [[raw/miranda_organization_github-may-6-2025.md]]
- [[raw/the_reason_for_miranda-may-6-2025.md]]
- [[raw/tools_adaptation_games_design_department-may-7-2025.md]]
- [[raw/mcp_servers_for_jvl-may-8-2025.md]]
- [[raw/game_design-may-8-2025.md]]
