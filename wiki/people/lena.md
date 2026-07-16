---
type: person
title: Lena
date: 2026-07-12
aliases: [Lena, Lena Zhukova, Laina, Elina]
source-count: 25
open-commitments: 1
---

# Lena

Lena leads JVL's game design / art team. She judges whether the visual quality of a game is good enough and decides how games are built (video vs. animation).

## Role

- On the FP7 hardware review, Val treats Lena and Dima Khandov as the people who form the opinion on whether test results are acceptable for the games JVL is trying to produce. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Lena speaks for the design side: she says JVL must find a balance between using "spine" animation and regular videos, and that combining the two takes extra effort from her team. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- She confirms her team will keep developing the Fortune Fu Paws game under the performance limits (video-count thresholds) established in the meeting. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- She raised the "plan B" question: if performance is a problem once the game is fully built, could signage be removed from that hardware? [[raw/fp-7_performance_analysis_january_13_2025.md]]

## FP7 sufficiency and signage idea (Jan 16–17)

- On the Jan 16 game-design review, Lena reported the tests show FP7 will work for the Fortune Football games, and repeated her proposal to treat the machine as three screens with a separate/autonomous signage controller. [[raw/game_design_january_16_2025.md]]
- On the Jan 17 bottleneck meeting, her minimum viable requirement was noted as ~4 videos; the test hit 8, twice her minimum. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Game-design review (Feb 6)

- Lena screen-shared her team's still-image mockups of a game with a **"Nico" cat** character on the topper — idle-with-meters → attraction mode with promo text and character animation → on-machine view — for Val's and Juan's feedback. (No animation yet; still compacts.) See [[wiki/topics/jvl-machine-lineup.md]]. [[raw/Game design meeting - February 6, 2025.md]]

## Val's restructuring plan and the "Chinese wall" (Feb 10)

On the GitHub-structure part-1 meeting Val named Lena the responsible owner for the **game-development GitHub organization**, described her current position as "not a producer… basically, manufacturing manager. The output manager," and stated his plan: "split Lena's responsibilities and move her to assistant or deputy game producer," appointing **Julia on land-based and Anastasia on online** in her current position — "so these two branches will start growing separately." He also drew the "Chinese wall": game production works only with the released, documented platform + Miranda — "Lena should have zero communication with you [Sasha]… I don't want Lena and you to socialize over anything"; Sasha agreed ("This is how it will be"). See [[wiki/meetings/2025-02-10-github-repo-structure-part-1.md]] and [[wiki/topics/game-production-throughput-strategy.md]]. [[raw/github _structure-pavel-aaron-andrei.md]] *(This is Val's stated plan on Feb 10, not an executed role change; by Mar 12 the same idea appears as the parallel-art-director test — see below.)*

## Git-LFS onboarding (Feb 18)

- On the Feb 18 VS Code / Git-LFS onboarding session, Val designated Lena for the graphics-team experiment: her computer is her "sandbox," but every commit she makes to a GitHub branch becomes JVL's possession. Val asked that a branch be made for her and that she make a **test LFS commit**; Andrei's homework is to set her up and hand her the onboarding steps. Val wants at least half the graphic department set up the same way (like Lena and Dima) to commit large assets themselves. See [[wiki/meetings/2025-02-18-git-lfs-vscode-onboarding.md]] and [[wiki/topics/ai-assisted-development.md]]. [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]

Her surname is given as **Zhukova** on the Feb 18 onboarding session (WEBVTT).

## Comp-art storage and game-design review (Feb 21)

- On the Feb 21 LFS session Lena raised the core storage problem: the large composition-art ("comp art") files are big, numerous, change rarely, and can't be diffed by Git, so committing them into the game repo would slow the build — she needed a dedicated place and rules on commit frequency/size. This drove the game-repo/design-repo split (comp art → LFS design repo, pulled as a submodule; build doesn't need it). She had created her branch + a `comparts` folder and committed one file. See [[wiki/decisions/2025-02-21-separate-game-and-design-repos.md]]. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- She pushed back that Markdown documentation would be inconvenient for Juan and Michael versus one-click Confluence; Aaron's docs-as-code answer (auto-rendered site) addressed it. See [[wiki/topics/docs-as-code-and-atlassian-exit.md]]. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- Same day she ran the **Fortune Foo Paws** design review (signage/V-Deck/toppers, help screens, the progressive-bet-incentive debate), and was tasked to present a **visual proposal on the bet-up incentive** the following Friday. See [[wiki/topics/slot-game-design-principles.md]]. [[raw/game_design_meeting_february_21_2025.md]]

## Designer branching workflow (Feb 26)

- On the Feb 26 coaching Lena is the designer drawing Photoshop comp art within a feature (with [[wiki/people/yulia.md|Yulia]] modelling and [[wiki/people/anastasia.md|Anastasia]] texturing). She questioned why PSD files need branch/PR discipline and worried about premature comments on unfinished cats — Aaron's answer: unfinished branch work is fine to show, and [[wiki/people/michael-gottlieb.md|Michael]] only comments at PR time. She asked Andrei/Dima to create a **design** space and separate repositories, including one for the **Fortune 4 Progressive Sign** (a separate IP). See [[wiki/decisions/2025-02-26-designer-branching-workflow.md]]. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

## Game-design review (Feb 28)

- Lena reported the **Fortune Foo Paws bonus topper** done (larger bonus-name text, promoting "win all three bonuses"). She is refining the **shiny cat texture** (matte looked "plasticky"; shadows lightened) and will insert the cat into the master file to judge in context; final color correction waits until the game runs on a real monitor. She confirmed the **HG-6 COAM nudge/button** modification is "not a NASA project" — within about a month for all games, exact estimate after production issues are created. She was tasked to prepare the **V-Deck visual proposal** (the bet-up flame effect on buttons 3/4/5) as a **visual storyboard by next Friday** (visuals, no animation yet). See [[wiki/topics/slot-game-design-principles.md]]. [[raw/Game design part 1 - Feb-28-2025.md]] [[raw/Game design part 2 - Feb-28-2025.md]]

## Git progress check-in (Feb 28)

- One of the three designers (with [[wiki/people/yulia.md|Yulia]] and [[wiki/people/anastasia.md|Anastasia]]) Aaron coached to put the repo-usage rules into the Fortune Foo Paws repo and keep making pull requests. See [[wiki/topics/docs-as-code-and-atlassian-exit.md]]. [[raw/Git_progress_check_in_2025-02-28.md]]

## Game-design review (Mar 7)

- Lena's team is the release **bottleneck** that drives the staged four-package "Peach" release plan for Georgia (she can't implement all game changes at once). She was working on the **denomination screen** and the V-Deck this week and will change the **"insert money"** warning on the no-credit screen. She is one of the **final sign-offs** (with Michael and Juan) — machines must be shipped to her from the Georgia assembly floor (office or home) so she validates the final assembled product, not a rack. The **V-Dec / GNOME (keynote) buttons** and future Georgia "flex curve" development are the next meeting's objectives. See [[wiki/decisions/2025-03-07-final-signoff-on-assembled-machines.md]] and [[wiki/projects/georgia-market-rollout.md]]. [[raw/game_design_meeting_march_7_2025.md]]

## Animation-process walkthrough (Mar 12)

- Lena gave Val a full step-by-step explanation of how JVL turns a concept into finished art and animation, as **art director**: she takes Michael's emailed vision, produces the **fundamentals** comp art first, then designs animations (**storyboards** for complex ones, **verbal descriptions** for simple ones), and only works on animation **after the final comp art** (it's a production, not a design, activity). She detailed the **3D→Blender / illustration→Spine** tool choice, the **After Effects** post-production, and assembly of placeholder and animated symbols inside **Miranda**. See [[wiki/topics/game-art-animation-production-pipeline.md]]. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
- She noted **Juan wants some symbols changed to Mexican symbols** in the Peach games (transcribed "Pitch 4") because there are many Mexican workers in Georgia — a "very important" cultural-market feedback she values. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]

## Art-team scaling debate (Mar 12, on the Gottlieb call)

- Val proposed making **Anastasia and Julia** parallel art directors alongside Lena to multiply output; Michael defended Lena as the one who **consistently makes better decisions** ("her sensibility is outstanding"), gives **top-line direction and lets the team run** (not a control freak), and must at least **review** all games. The compromise was to test the theory on a Mexican-theme comp art (5X Peppers / Pink Princess → "La Rosa"). See [[wiki/topics/game-production-throughput-strategy.md]]. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## GitHub for graphic design (Mar 12)

- Lena raised the **PSD-commit conflict** problem and asked **when to create a repo for a new game** (e.g. **Cache Kittens**) given Michael/Juan/Yefim aren't on Git yet (design still in **Zephyr**). Val/Aaron told her to **start the repo now and "fake the review"** via Julia/Anastasia or Dima Khandov, and to fork new games from a generic template Andrei will build. See [[wiki/topics/graphics-team-git-workflow.md]] and [[wiki/decisions/2025-03-12-fork-game-repos-from-generic-template.md]]. (Also confirmed **Heat Game 6** and **Georgia** are the urgent side projects, with Natasha continuing Georgia while Lena returns to FFP.) [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Nebraska skill market (Mar 14)

- Lena confirmed the **"hands" is part of the common UI** used in all games and can simply be removed for the no-hands Nebraska build, and helped work through the software approach (revert to conservative nudge, keep the other enhancements). See [[wiki/projects/nebraska-skill-market.md]]. (The transcript also renders a "Elina" in this call — inferred to be Lena or Irina; kept ambiguous.) [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]

## GitHub template check-in (Mar 26)

- On Andrei's template-repo demo, Lena gave the key **"when to update the template" signal**: when there's a **new reusable script** useful across all games. She also mapped the future to **per-game-type templates** — a base template now, then dedicated templates for **Georgia / Omnia framework games**, **Persistence games**, and **classical games**, each with structure appropriate to that game mechanic. See [[wiki/topics/graphics-team-git-workflow.md]]. [[raw/github_commits-march-26-2025.md]]

## Subject of the Val–Gottlieb Teams-visibility talk (Mar 26)

- Lena triggered the Mar 26 one-on-one by telling [[wiki/people/michael-gottlieb.md|Michael]] that Val wanted to be copied on their game-development Teams chats; per Michael, "she didn't tell me anything… She said this is what Val wants… she doesn't really contradict you. I think she's afraid of you." Val rejected the fear reading and cited history: **Lena has known him for 26 years**; "Lena has been loyal to me, and I have been loyal to Lena for two decades, to her and to her father." Michael described their working dynamic (she posts Jira links for symbol review; he can signal "let's try something different" without spelling out rejection) and his worry that CEO visibility would make her more conservative; he also said Val needs to plan for "what happens if Lena is not around," which both treated as a real continuity question. The **La Rosa** comp flow was shown as the example: Lena sends variant treatments → Michael picks one ("zoomed in tighter, base shown more prominently") → she refines → it goes to [[wiki/people/juan-martinez.md|Juan]]. See [[wiki/meetings/2025-03-26-gottlieb-val-one-on-one.md]]. [[raw/michael_gottlieb_val_meeting-26-2025.md]]

## Game-design review (Mar 28)

- As **art director** Lena presented and defended the Peach-4 reskin art: **La Rosa** (Pink Princess assets repainted — purse, pumps, luxury car, hacienda), noting the team reused Pink Princess's 3D models to save "a couple of weeks." She agreed to redo the male lead's haircut/face and pointed out how much rework a full symbol change ("paper game") would cost. She is implementing the **nudge animation-freeze** on Peach 2 and updating **FireEyes** attraction videos + single-game attraction mode. She is to decide the **5X Peppers vs 5X Pimentos** naming. Her team remains the release bottleneck. See [[wiki/topics/slot-game-design-principles.md]] and [[wiki/topics/jvl-machine-lineup.md]]. [[raw/games_design_meeting-march-28-2025.md]]

## Open commitments

- [ ] Lena — prepare a **visual storyboard** of the V-Deck bet-up incentive (escalating flame/particles on bet buttons 3/4/5) — due **next Friday** — [[raw/Game design part 2 - Feb-28-2025.md]]

## Apr 16 2025 — graphics priority change; comp-art via Cline

In the Omni daily Val flagged a separate task for "Лена Жукова" to change the graphic designers' priorities (especially the cladding/окление work) per the framework changes; he also noted Lena had made the earlier list of jackpot/feature "штуки." [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]] In the AI-tooling knowledge share, Lena described generating concept/comp-art images with ChatGPT (DALL·E) and now Cline as well — same model, sometimes different results. [[raw/mcp_experiences_tech-apr-16-2025.md]]

## Apr 17–18 2025 — Calle Ocho asset port + production-time estimation

- **Apr 17 Calle Ocho session** ([[wiki/meetings/2025-04-17-calle-ocho-asset-redesign-omni.md]]): Lena proposed the fast "plan A" (re-export the old Rage-Studio videos through Spine/Miranda to hit May 1) but flagged its flaw (reuses nothing for the next game); the group settled on Dima's middle approach. She drove the concrete asset rulings (new dashboard raises the reels, remove the "Lions," reposition-not-resize the matrix, Royals as Spine skins) and postponed detailed **Fortune Fu Paws** planning ~2 weeks. See [[wiki/topics/game-art-animation-production-pipeline.md]]. [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]
- **Apr 18 production estimation** ([[wiki/meetings/2025-04-18-games-production-time-estimation.md]]): Lena walked Val through the Miro game-production task list to estimate time per item (her reiteration rule of thumb ~2.5 on average), explaining the CompArt→detailing→production stages, the Fiery-Ice-Link common/progressive split, and why she priced only the non-substitutable critical resources (Dima/Nastya/Yulia, fully parallel) and not Anton (shared across games). See [[wiki/topics/game-production-throughput-strategy.md]]. [[raw/games_production-apr-18-2025.md]]

## Game-design review (May 1 2025)

On the [[wiki/meetings/2025-05-01-game-design-review.md|May-1 review]] Lena reported the Nebraska **Corn Husker bonus** progressing (toning down the corn stalks around the logo, building the second/topper bonus screens), and coordinated the **regulator video** (recorded by Vitaly Monday, one three-reel + one five-reel, sound processed by Vlad) and the **2D decks** for Diamond Link + JetPort Rush (Georgia) to finish next week. Omni work continues, on schedule. See [[wiki/topics/game-art-animation-production-pipeline.md]]. [[raw/game_design_review-may-1-2025.md]]

## Sources

- [[raw/github _structure-pavel-aaron-andrei.md]]

- [[raw/fp-7_performance_analysis_january_13_2025.md]]
- [[raw/game_design_january_16_2025.md]]
- [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- [[raw/Game design meeting - February 6, 2025.md]]
- [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- [[raw/game_design_meeting_february_21_2025.md]]
- [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- [[raw/Game design part 1 - Feb-28-2025.md]]
- [[raw/Game design part 2 - Feb-28-2025.md]]
- [[raw/Git_progress_check_in_2025-02-28.md]]
- [[raw/game_design_meeting_march_7_2025.md]]
- [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
- [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- [[raw/github_commits-march-26-2025.md]]
- [[raw/games_design_meeting-march-28-2025.md]]
- [[raw/michael_gottlieb_val_meeting-26-2025.md]]
- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- [[raw/mcp_experiences_tech-apr-16-2025.md]]
- [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]
- [[raw/games_production-apr-18-2025.md]]
- [[raw/game_design_review-may-1-2025.md]]
