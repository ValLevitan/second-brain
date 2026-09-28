---
type: person
title: Lena
date: 2026-07-12
aliases: [Lena, Lena Zhukova, Laina, Elina, Liana, Leanna, Selena, Elena]
source-count: 70
open-commitments: 14
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

## May 7 2025 — AI tool adaptation (ComfyUI, MCP)

On the bi-weekly games-design tools session ([[wiki/meetings/2025-05-07-games-design-ai-tools-adaptation.md]]) Lena reported building **ComfyUI** workflows to generate a specific **golden-coin** asset (fixing the seed/parameters to keep results stable) and wanting JVL's own **LoRA** style; she raised the Cline/Confluence-MCP page-cloning failures and keeps **Confluence as the game-docs source of truth** (converting to Markdown via Spline). See [[wiki/topics/game-art-animation-production-pipeline.md]] and [[wiki/topics/ai-assisted-development.md]]. [[raw/tools_adaptation_games_design_department-may-7-2025.md]]

## May 8 2025 — Golden Cask/Husk production

On the [[wiki/meetings/2025-05-08-game-design-review.md|May-8 review]] Lena ("Liana"/"Lena" in the transcript — same person) reported the Nebraska **Golden Cask**/Golden Husk bonus production: finalising the game list, the corn **fan/scale transition** animation, adjusting the **Money Birds / Cash Cats** logos, and the first **Crazy Spins** video recording. She confirmed the graphic team **love Miranda**, and flagged the math-emulator stall (Dima pulled onto other work). See [[wiki/topics/game-art-animation-production-pipeline.md]]. [[raw/game_design-may-8-2025.md]]

## May 29 2025 — South Dakota six-pack art + Calle Ocho colors ([[wiki/meetings/2025-05-29-games-design-recap.md]])

On the games recap Lena ("Elena") reported the **South Dakota VLT** production moving: **Bioliches** in development and **Gypsy Spirit** concept/GDD done (production stories starting next day), with **Natalia** and **Vitaly** on feature systems; she's using **smaller gems**. She and [[wiki/people/efim-podvoiski.md|Efim]] work **Queen of Luxor**; some **Golden Husk/Golden Fast** Nebraska assets (illustrations, 3D models) are prepared but paused for SD priority. She supplied the **Photoshop colors** for the customer's life-size **Calle Ocho rooster** statue. Resources: **Dima and Andy** and **Igor Metelski** ("Mitevsky") are locked on Omni/Calle Ocho, so none free for Colombia. See [[wiki/topics/game-art-animation-production-pipeline.md]] and [[wiki/projects/south-dakota-vlt-market.md]]. [[raw/games_design_recap-may-29-2025.md]]

## June 12 2025 — next art work set

On the [[wiki/meetings/2025-06-12-games-design-priorities-review.md|June-12 priorities review]] Lena reported the last South Dakota game (**Rodeo Spin**) almost done (posting to Confluence), and was set on the next art: the two Rage-Studio **Fiery Ice Link** titles — start with **Glorosa** (evolve from approved materials), then **Havana Noches** — on the **V1000** cabinet, with the Glorosa free-spins experience still to be designed. She also pushed for South Dakota vertical art (already done) not to stall, and got QA-branch awareness assigned. See [[wiki/topics/game-art-animation-production-pipeline.md]] and [[wiki/projects/south-dakota-vlt-market.md]]. [[raw/games_design-june-12-2025.md]]

## June 19 2025 — games review

- On the [[wiki/meetings/2025-06-19-games-design-nebraska-market.md|June-19 games review]] Lena reported active work on **Coyote Omni** and **Golden Husk** (slot bonuses + progressive sign), the **South Dakota vertical** in production, and redesigning **La Rosa** from a 3×3 Georgia game into the **FireEyes Link** family (symbols discussed with Michael). She flagged the Golden Husk secondary bonus as "something completely new" needing scene-assembly time. See [[wiki/topics/slot-game-design-principles.md]]. [[raw/Games_design-june-19-2025.md]]

## June 23 2025 — Nebraska comp art for the six games

On the [[wiki/meetings/2025-06-23-nebraska-game-design-planning.md|Nebraska design + planning session]] Lena is producing the **comp art** for the six Golden Husk games (working with Michael this week, per Juan's direction). Method: present a comp for one game (no-DNOM button; with/without the pattern-match button) for Juan to confirm, then rinse-and-repeat; she needs a comp image per game because the many small adjustments can't be described. She was aware **Crazy Spins** needs an added wild symbol, and she can start the primary win-meter compact now. She uses **sprints** for design (Val recommended **Kanban**). See [[wiki/projects/nebraska-skill-market.md]]. [[raw/NE_game_design_and_planning-june-23-2025.md]]

## July 28 2025 — Media Tax Credit application lists

On the [[wiki/meetings/2025-07-28-media-tax-credit-examiner-coaching.md|Media Tax Credit coaching call]] Lena is the keeper of what counts as claimable **production labour** ("everything Lena considers a production") and of the **game lists** submitted to Ontario Creates — she supplied Val the list of 13 online games claimed as interactive. She and Michael confirmed the online-games **interactivity gap**: the special land-based golden-frame bonus was designed and math'd but never deployed online, and the three "China" games (Red Envelope feature) are passive, not interactive. She was to feed Michael her factually-correct firmware/hardware answers for him to reword. See [[wiki/topics/ontario-media-tax-credit.md]]. [[raw/media_tax_credit_team_coaching-july-28-2025.md]]

## Jul 31 2025 — amusement-games revival (team & scope)

With [[wiki/people/val-levitan.md|Val]] and [[wiki/people/efim-podvoiski.md|Efim Podvoiski]], Lena scoped **reviving JVL's ~150 aged amusement games** onto the HTML framework — a full redesign from assets to framework programming (concepts/scenes/character designs reusable, assets not), games assembled in **Miranda**, ~2 years for ~50 games; she proposed **outsourcing** the self-contained project and flagged its market as distinct from mobile/internet. In the parallel Pavel session she and Efim are named as the ones who "know the whole history" and can advise. Full substance: [[wiki/topics/amusement-games-revival.md]]. [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]] [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]

## Jan 23 & 27 2026 — her admin load, her Jira workflow, and meeting Clayton

- **Jan 23 (Val and Michael, about her).** On the [[wiki/meetings/2026-01-23-michael-gottlieb-art-production-roles-and-estimation.md|Val–Gottlieb call]] Val said: "Whatever Lena is busy right now in terms of administration, I intend to automate 95% of it this year in 2026." He counts supervision and "inputting tasks into JIRA" as necessary but "non-value producing" work. The hierarchy is Michael, then Lena; the open question was whether a role is needed under her. Michael described her part in estimating: she looks at the metric and the employee's own estimate, then gives "guidance and shortcuts" and can move a task to someone else. Val said he and Lena saw the uneven story sizing as an issue "about a year ago" but lacked the bandwidth. See [[wiki/topics/game-production-throughput-strategy.md]] (Jan 23 2026). [[raw/Meeting_Transcript_Michael_Gottlieb_Art_Production_Roles_and_Estimation-January-23-2026.md]]
- **Jan 27 — her role as Val stated it.** On the [[wiki/meetings/2026-01-27-clayton-lena-game-design-jira-orientation.md|Jan-27 orientation]] with [[wiki/people/clayton-chancey.md|Clayton Chancey]], Val introduced her as "a director of game design" who "reports directly to. The game producer", with a team of designers "located mainly in Europe, Portugal, Poland". She is present at game concept but that stage is mainly the product manager and producer; from design on, "this is where Lena is mainly running the show and she is pushing the production." [[raw/Meeting_Transcript_Clayton_Lena_Game_Design_Jira_Orientation-January-27-2026.md]]
- **Her Jira workflow.** Concept and design are managed by "me, VP product owner and game producer"; production by "me and art managers". Each game has a list of deliverables; each milestone is treated as a feature; stories sit inside, "we're trying to keep our stories not more than two days. It's not always two days". Her main problem: "the amount of issues you need to enter, and you need to do description." Two people help her — she called them art managers — but "they are game artists by themselves". Val's clarification: they are senior design people who help enter tasks and are not managers. *(§15.8: Val's personal judgements of the two are not recorded.)* [[raw/Meeting_Transcript_Clayton_Lena_Game_Design_Jira_Orientation-January-27-2026.md]]
- **Product cycles.** New complex games (several bonuses) can take about five months; adapting an existing game to another market is "a different cycle" whose length varies. [[raw/Meeting_Transcript_Clayton_Lena_Game_Design_Jira_Orientation-January-27-2026.md]]
- **Rage Studio risk.** "Rage Studio is based on 3 ds Max11, which is not supported already by Autodesk… we don't have a team to work on Rage… there are some risks that we are working on unsupported software." Val: her "prime bureaucratic swamp is on Rage Studio", and "I have a feeling that Lena is spending somewhere between 20 to 40 % of her productive time on bureaucracy" — he does not know which end. See [[wiki/topics/omni-core-advancement-and-game-templating.md]] (Jan 27 2026). [[raw/Meeting_Transcript_Clayton_Lena_Game_Design_Jira_Orientation-January-27-2026.md]]
- **Her AI experience so far.** She had not used Claude for tasks; "a couple of days ago" she tried a tool rendered "spline" (which one is unclear) and found it "helped a little bit", but it asks "so many questions on the way", everything must be rechecked, and it sometimes changes things "because he thinks it's better" when they are that way "because… There are some regulations on our market". The artists mostly use ChatGPT for art references and game concepts. Val noted she had not used Claude Desktop with a Jira MCP. See [[wiki/topics/ai-assisted-development.md]] (Jan 27 2026). [[raw/Meeting_Transcript_Clayton_Lena_Game_Design_Jira_Orientation-January-27-2026.md]]
- **Next step.** She agreed to join the next meeting ("the day after tomorrow") to judge Clayton's first tool; Val gave Clayton a direct line to her: "My main objective is to make, Your life personally easier to unload the bureaucracy on automation." [[raw/Meeting_Transcript_Clayton_Lena_Game_Design_Jira_Orientation-January-27-2026.md]]

## Jan 29 2026 — MCP-tools working session (requirements from the design side)

On the [[wiki/meetings/2026-01-29-jvl-working-session-mcp-tools-demo.md|working session]] where [[wiki/people/clayton-chancey.md|Clayton Chancey]] demoed his first JVL Jira MCP tool (with Val and [[wiki/people/aaron.md|Aaron]]), Lena spoke for the design side. The transcript tags her "Speaker 2" (an inference from context). Facts are from the transcript unless marked. [[raw/Meeting_Transcript_Clayton_Jira_MCP_Demo_and_Toolset_Direction-January-29-2026.md]]

- **Her verdict on the Game Status tool.** "It's definitely useful for a status review and very useful. I like it. I use it." To connect it she would need IT, since it uses a token. [[raw/Meeting_Transcript_Clayton_Jira_MCP_Demo_and_Toolset_Direction-January-29-2026.md]]
- **Val on her needs.** Val said she knows Jira status "by heart", so the status report helps him more than her; "What she spends a lot of time on is… entering tasks." He had shared his own status prompt (built on Aaron's MCP) with her. [[raw/Meeting_Transcript_Clayton_Jira_MCP_Demo_and_Toolset_Direction-January-29-2026.md]]
- **Images must reach the right story.** Her art is made with AI help but "it's never just raw AI-generated"; each game has its own layout, colours and scheme. Files are "JPEG and PNG, and PSD files". She asked that a create-game tool at least attach "proper image from my folder" to the proper story, by her file names — her example "La Rosa, a symbol, Goldenback" — and she would then add the animation notes by hand. [[raw/Meeting_Transcript_Clayton_Jira_MCP_Demo_and_Toolset_Direction-January-29-2026.md]]
  - The summary doc words this as embedding a set of images in the ticket descriptions, "still a research item". [[raw/Clayton_jvl-working-session-2-summary-January-20-2026.md]]
- **Cloning, from the art side.** When a game is cloned, the maths and game function carry over, "but for us we need to create all these assets". For Jira, a clone needs "the same structure but different names" — her example: "lion reaches" (read as Lion's Riches), themed on a savannah ("seen by sam savannah", garbled), now being cloned with the same issues, bonuses and function. Val's reply: cloning is "the essence of our business" (see [[wiki/topics/ai-assisted-development.md]], Jan 29 2026). [[raw/Meeting_Transcript_Clayton_Jira_MCP_Demo_and_Toolset_Direction-January-29-2026.md]]
  - The summary doc says she "prefers a single broad structure applied universally". The transcript does not show that; treat it as the summary's reading only. [[raw/Clayton_jvl-working-session-2-summary-January-20-2026.md]]
- **Her ChatGPT project and February 6.** She likes her ChatGPT project, which is "learning my style". She said: "starting from February 6th, we need to use something because our subscription is going to end", and asked for a recommendation. Clayton: "Nano Bananas. Yep, a Gemini tool." Aaron: "There are many kinds." No choice was made. Val called her "captured by an open AI ecosystem". (On Feb 6 Val approved a one-month ChatGPT extension — section below.) [[raw/Meeting_Transcript_Clayton_Jira_MCP_Demo_and_Toolset_Direction-January-29-2026.md]]
- **Her design knowledge.** Val: her work follows the game producer's spoken guidance, and "when lena leaves jvl the knowledge cannot escape" — so those talks should be recorded and turned into "JVL truth". See [[wiki/topics/ai-assisted-development.md]] (Jan 29 2026). [[raw/Meeting_Transcript_Clayton_Jira_MCP_Demo_and_Toolset_Direction-January-29-2026.md]]
- **Next session.** Clayton: next meeting "next tuesday at the same time", Lena shares her screen and they install Claude Code and the MCP server in the meeting; "come with a blank slate don't prepare at all". Lena: "should I prepare somehow" — no. The summary doc dates it "Tuesday, February 4", but February 4 2026 is a Wednesday; the date is unclear. [[raw/Meeting_Transcript_Clayton_Jira_MCP_Demo_and_Toolset_Direction-January-29-2026.md]] [[raw/Clayton_jvl-working-session-2-summary-January-20-2026.md]]
- *(§15.8: a remark by Aaron about her working style is not recorded.)*

## Feb 6 2026 — image-generation tooling; ChatGPT extension request

On the [[wiki/meetings/2026-02-06-game-development-review.md|Feb-6 2026 game-development review]] Lena walked the South Dakota VLT-2 and Georgia design status (attraction-mode home screen IP944, topper promo text, Lion Riches/Dragon Pays updates — see [[wiki/topics/slot-game-design-principles.md]]) and raised a tooling problem. [[raw/Game_Dev-February-6-2026.md]]

- **Image-generation quality gap.** The team moved onto **Claude AI**, but since it does not generate images itself they connected it to a node-based image interface the transcript calls **"Config UI" / "conf UI"** (very likely **ComfyUI** — inference) running **Stable Diffusion**. Image quality so far is **lower than what they achieve in ChatGPT**. Claude AI's recommendation is to download and **train LoRA modules** ("Low-Rank Adaptation") for specific styles — e.g. a LoRA trained on golden-coin images to produce casino-style symbols — which is time-consuming; they start next week. [[raw/Game_Dev-February-6-2026.md]]
- **ChatGPT-subscription extension — approved.** Lena asked Val to **extend the ChatGPT subscription one month** while the LoRA training ramps, noting they already have running ChatGPT "projects" (e.g. cat deviations for animation) working well. Val approved on the spot and asked her to put it in an email. [[raw/Game_Dev-February-6-2026.md]]

## Feb 12 2026 — the liquid-glass defense; Lion's Riches/Dragon Pays; scheduling

On the [[wiki/meetings/2026-02-12-game-development-review.md|Feb-12 review]] (segment 1). [[raw/Game_Development-February-12-2026-1.md]]

- **Defended the liquid-glass game-selection screen** against Val's push to recolour its background per game: the glass effect is a **faked, pre-rendered movie** (background + button reflections baked into one render; each button configuration is a multi-day render), so it can't be recoloured in real time. She proposed — and it was adopted — the **shrink-the-billboard-logo + main-screen-background-border** compromise. The exchange got sharp (Val: stop telling me "how hard/talented"; Lena: "less is more"), but landed on her original suggestion. See [[wiki/topics/slot-game-design-principles.md]] (Feb-12). [[raw/Game_Development-February-12-2026-1.md]]
- Walked the **Lion's Riches revised royals** and **Dragon Pays** updates, toppers (Cool Cat / Black Hills Keno), and the South Dakota production list (La Rosa, Rodeo Spins, Black Hills, Cool Cat, liquid-glass home screen). [[raw/Game_Development-February-12-2026-1.md]]
- **Jira hygiene:** Val flagged items in "request review" showing **no schedule dates**; Lena diagnosed that request-review status hides dates and undertook to investigate/fix, and to correct a feature that still carried feature-level dates after stories were added under it. Also coordinating the [[wiki/people/igor-metelski.md|Igor Metelski]] absence — she's talking to Pavel/Irina/Anton to scope the inherited work. [[raw/Game_Development-February-12-2026-1.md]]

## Feb 19 2026 — Games Design Meeting: progressive visuals, Lion's Riches/Twin Bison layout, SD queue

On the [[wiki/meetings/2026-02-19-games-design-meeting.md|Feb-19 Games Design Meeting]] (schedule-review session). [[raw/Game_Development_transcript_schedule_review-February-19-2026.md]]

- **Progressive coin + visuals in progress.** She has started the coin and progressive visuals for GC-351 (bonus visuals GC-360, in-game symbol GC-361) — blocked from finalizing only by the undecided "Pick 3" vs "Match 3" name that appears in the UI. [[raw/Game_Development_transcript_schedule_review-February-19-2026.md]] [[raw/Games_Design_Meeting_review_feb19_2026_v3.md]]
- **Lion's Riches / Twin Bison screen redesign ("a game of Tetris").** She and Michael must lay out the shrunk pay table, the scrolling instruction banner, and the large lion/bison canvas. [[raw/Game_Development_transcript_schedule_review-February-19-2026.md]]
- **South Dakota design/production queue.** Working through Wild Colt (IP-1017, nearly done) then Dragon Pays (IP-1018) design, with production actively on Black Hills Skinner, Cool Cat Keno, Liquid-Glass La Rosa, Rodeo Spins and the Lion's Riches update; she resisted closing **IP-877 (Calle Ocho)** despite all art being done, unsure whether developer tasks live under it. She confirmed she prepares multiple game-selection layouts as standard practice. See [[wiki/topics/slot-game-design-principles.md]] (Feb-19). [[raw/Game_Development_transcript_schedule_review-February-19-2026.md]] [[raw/Games_Design_Meeting_review_feb19_2026_v3.md]]

## Feb 27 2026 — game-development review: Nebraska reprioritization, MCP experiment, production queue

On the [[wiki/meetings/2026-02-27-game-development-review.md|Feb-27 game-development review]]. [[raw/Game_Development-February-27-2026.md]]

- **Absorbed the Nebraska reprioritization.** With Nebraska made #1 priority, Lena will drop other work to do the dual-box comp art (concept ~two days), and **extended the IP 1018 Dragon Face design deadline ~2 weeks**; she pushed to finish South Dakota and immediately start Georgia (which she flagged as urgent and warned would slip if a full Nebraska liquid-glass project were taken on). See [[wiki/topics/slot-game-design-principles.md]] (Feb-27). [[raw/Game_Development-February-27-2026.md]]
- **The transcript→Jira MCP experiment.** She plans to send the meeting transcript to consultant [[wiki/people/clayton-chancey.md|Clayton]] and, in their Tuesday session, test his updated MCP creating Jira issues from the transcript across concept/design/production spaces and attaching a comp-art image (a prior cross-space attempt had failed). See [[wiki/topics/ai-assisted-development.md]] (Feb-27). [[raw/Game_Development-February-27-2026.md]]
- **Production queue.** Walked the fresh build — La Rosa (gun-symbol animation toned down/approved), Black Hills Kino (help screens near complete, ball animation next build; audio created but not yet integrated), Rodeo Spins, plus line switches started. [[raw/Game_Development-February-27-2026.md]]

## Mar 4 2026 — presents the built dual-box + secondary-skill button

On the [[wiki/meetings/2026-03-04-game-development-schedule-review.md|Mar-4 game-development review]] Lena presented her **built** Nebraska work — the dual-box primary-skill screen (dimmed reels, desaturated left border, animated tracer, all-or-none) that Michael praised as turned around quickly, and the reworked secondary-skill trigger button (transparent, smaller desaturated text, border blended in, grayed box shrunk). She confirmed she will attach approved comp art to GC374/GC376, close the concept items, open production (IP 1023/1024, feature AA6485 assigned to [[wiki/people/yulia.md|Yulia]], two stories), and estimated **assets ~1 week (due ~March 12)**. See [[wiki/topics/slot-game-design-principles.md]] and [[wiki/projects/nebraska-skill-market.md]] (Mar-4). [[raw/Game_Development_Schedule_Review-March-4-2026.md]]

## Mar 13 2026 — weekly game-dev review: progressive visuals in progress; the "completed" JIRA stage chore

On the [[wiki/meetings/2026-03-13-game-development-review.md|Mar-13 game-development review]] Lena shared the schedule and drove the visuals — the **GC351** pick-3 progressive coin/layout design (with Michael) and **GC360** progressive visual for the "Pix 3" bonus **in progress**, the built **Dragon Pace** main screen (Asian-look royals, desaturated, dragon popping, liquid glass + new ticker) and the new reel-3 jackpot coin, and production items (IP459 South Dakota; IP984 liquid-glass home screen; IP988 La Rosa; rodeo/Dragon-Pace scheduling). She created **IP1028 (Georgia COAM)** as a backlog placeholder (not yet scheduled). Val gave her a **chore: write JVL IT to add a "completed" workflow stage before "done"** for features/IPs in game production, copying him. She defended showing "done" items as useful progress on recent projects (Val's 30-day filter accommodates it). Design/market detail on [[wiki/topics/slot-game-design-principles.md]] / [[wiki/projects/georgia-market-rollout.md]] (Mar-13). [[raw/JIRA_Schedule_review-March-13-2026.md]] [[raw/Game_Development-March-13-2026.md]]

## Mar 17 2026 — grooming the IP-89 game-production dashboard

On a short Russian call ([[wiki/meetings/2026-03-17-ip-89-dashboard-grooming.md]], 3:54pm; with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]) to clean up the **IP-89** dashboard, Lena pushed for **automation to archive a whole product plus all its child issues/stories in one move** (rather than by hand) and asked to standardize the Jira statuses/resolutions to match current work — the operational follow-through on her Mar-13 "add a completed stage before done" chore. See [[wiki/topics/github-release-management-pipeline.md]] (Mar-17). [[raw/Grooming Dashboard for IP-89-March-17-2026.md]]

## Mar 20 2026 — SD VLT production lead; the "waiting for Anton" clarification; SR&ED

Two Mar-20 calls. On the **[[wiki/meetings/2026-03-20-game-development-schedule-review.md|game-development schedule review]]** Lena reported production actively focused on **IP40059 South Dakota VLT** (Rodeo Spins/Clover Fortune done, La Rosa near done on the Gold Nugget presentation), that **Dragon Pays (IP997)** is her next assignment, and that assets for **Kulkitkinen / Cool Cat Kino** are ready and just await [[wiki/people/anton-leshkevich.md|Anton]] to assemble. Val pressed whether Anton was a **bottleneck**; Lena clarified he is **not a stopper** — she has plenty of other work, it was "a wrong expression." She is the designated **consent-holder for the 3–6-month JIRA backlog band** under Val's new grooming policy and voiced concern about deleting detailed shelved projects (e.g. Fortune Foo Paws). Design detail on [[wiki/topics/slot-game-design-principles.md]] and SD status on [[wiki/projects/south-dakota-vlt-market.md]] (Mar-20). On the **[[wiki/meetings/2026-03-20-sred-progress-review.md|SR&ED progress review]]** she was present as a game-design/R&D lead while the team compiled the 2025 project list — see [[wiki/topics/sred-tax-credit.md]] (Mar-20). [[raw/JIRA_schedule_review_Game_Development-March-20-2026.md]] [[raw/SREDs_progress_review-March-20-2026.md]]

## Mar 13 & 19 2026 — the "Semantic Understanding" transcription-pipeline sessions

Lena drove the domain-expertise side of two [[wiki/people/clayton-chancey.md|Clayton]]-led sessions ([[wiki/meetings/2026-03-13-semantic-understanding-clayton-aaron.md|Mar-13]], [[wiki/meetings/2026-03-19-semantic-understanding-clayton-aaron.md|Mar-19]]) building JVL's Russian/slang transcription pipeline. On Mar-13 she described her manual baseline (audio → **Turboscribe** → her **taxonomy vocabulary spreadsheet** + Claude = "almost perfect"), the security worry IT raised about Turboscribe, and gave detailed feedback on the Jira MCP's output (good feature/story structure, imperfect descriptions; the images-must-be-on-desktop limitation). On Mar-19 she validated Clayton's pipeline output as accurate on speaker attribution and game names, but flagged the two defects — the **participants list wrongly including mentioned-but-absent people** and a mis-rendered game name — and won the ruling to **drop transliteration annotations** (developers always write "IP"/"Spine" in English anyway). She agreed to record her next daily graphics meeting as a second test case. Detail on [[wiki/topics/transcript-knowledge-base-tooling.md]] (Mar-13 & 19). [[raw/Clayton-Aaron-JVL-semantic-understanding-March-13-2026.md]] [[raw/Clayton-Aaron-JVL-semantic-understanding-March-19-2026.md]]

## Mar 27 2026 — automation review: MCP feedback and chat-interleave idea

On the [[wiki/meetings/2026-03-27-automation-progress-review.md|Mar-27 automation progress review]] (with [[wiki/people/clayton-chancey.md|Clayton Chancey]] and [[wiki/people/val-levitan.md|Val]]) Lena reviewed Clayton's transcription microservice and **MCP**: she likes how the MCP works in her **sandbox** but, before rolling it to the wider art/dev team, wants the sync fixed to a **specific Windows folder** (not download-to-desktop) and the **Windows mounted-drive** issue resolved. She also suggested the transcription pipeline **interleave timestamped meeting chat content** (links, bullet points, requirement references shared in Teams chat) into the transcript, since important detail often lives in chat rather than speech — especially for screen-share-heavy sessions. See [[wiki/topics/ai-assisted-development.md]] (Mar-27). [[raw/Meeting_Transcript_automation_progress_review-March-27-2026.md]]

## Mar 27 2026 — weekly game-dev review: Twin Bison concept art + South Dakota production

On the [[wiki/meetings/2026-03-27-game-development-review.md|Mar-27 game-development review]] Lena presented the **GC363 Twin Bison** concept art (winter free-spins scene with the white-bison wild-reel lock; will add the 10 payline arrows and the shared liquid-glass nudge arrows) — approved, moving to design in parallel with Lions Riches — and reported South Dakota production: Black Hills Keno graphics nearly done, Cool Cat Keno assembly starting, La Rosa / Wild Gold / Dragon Pace status. She also flagged she lacks archive rights in Jira and will ask [[wiki/people/dmitri-kovalchuk.md|Dima]] about the archiving workflow. [[raw/Meeting_Transcript_game_development_March-27-2026-1.md]] [[raw/Meeting_Transcript_game_development_March-27-2026-2.md]] [[raw/Meeting_Notes_game_development_March-27-2026.md]]

## Mar 31 2026 — transcripts MCP setup: Lena as the "ontological filter"; a Mac mini for her

On the [[wiki/meetings/2026-03-31-transcripts-mcp-setup-lena.md|Mar-31 transcripts-MCP setup]] (with [[wiki/people/clayton-chancey.md|Clayton Chancey]] and [[wiki/people/val-levitan.md|Val]]) Clayton connected Lena's Claude to the live transcripts pipeline (PAT + SSO). The session was repeatedly derailed by **MCP instability on her Windows machine** (tools connecting/disconnecting; she noted the risk of a silent mid-query disconnect producing wrong answers, and that she sometimes has to reboot to recover), but the end-to-end test eventually worked — resolving "Dragon Pays" correctly via Jira and enriching feature descriptions with meeting-notes comments. Clayton framed Lena as the **"ontological filter"** — the human judging correct/incorrect before hitting execute; Lena corroborated that she catches Claude "fixing" her information and claiming its version is better. Val ordered a **Mac mini** for her live on the call (her custom graphical tools won't run on Linux but work on Mac); she noted team leads **Anastasia** and **Julia** also need it since they manage stories. See [[wiki/topics/transcript-knowledge-base-tooling.md]] and [[wiki/topics/ai-assisted-development.md]] (Mar-31). §15.8 clear. [[raw/Meeting_Transcript_Transcripts_MCP_setup_Lena-March-31-2026.md]] [[raw/Meeting_Notes_Transcripts_MCP_Setup_Lena-March-31-2026.md]]

## Apr 28 2026 — IP MCP model regression: the Opus-4.6 pin and the tools she still wants

On the [[wiki/meetings/2026-04-28-lena-ip-mcp-model-regression.md|Lena IP MCP Model Regression]] session (with [[wiki/people/clayton-chancey.md|Clayton Chancey]] and [[wiki/people/val-levitan.md|Val]], who joined mid-call), Lena re-tested Clayton's **IP MCP** JIRA-ticket tool after its prior failure. Reverting to **Opus 4.6** restored quality; a re-test produced 11 tickets with correct comp-art images, which she spot-checked as accurate ("same quality as the Dragon Base structure work"). She raised the long-term worry that Anthropic may eventually retire 4.6, and asked for **delete-issue** and **archive-issue** tools so she needn't switch to Aaron's separate MCP add-on (e.g. archive all IPs under a finished market like Georgia/South Dakota). She will test through the week — including generating stories under features — and aims to cut over to production Thursday Apr 30; propagation to her two team leads (on Windows) to be handled by Andrei. See [[wiki/topics/transcript-knowledge-base-tooling.md]] and [[wiki/topics/ai-assisted-development.md]] (Apr-28). §15.8 clear. [[raw/Meeting_Transcript_lena_IP_MCP_model_regression-1-April-28-2026.md]] [[raw/Meeting_Notes_lena_IP_MCP_model_regression-April-28-2026.md]]

## Aug 14 2026 — NOVA design-environment wishlist; Wildfire Ranch comp art; South Dakota vertical games

On the [[wiki/meetings/2026-08-14-nova-capability-wishlist.md|Aug-14 NOVA wishlist call]] Lena gave the visual/design wishlist for NOVA: a properly working **Miranda** design environment with manifest; **toppers in the build**; a much more advanced **show mode**; finished **framework dialogues**; and — most important to her — integrating the **math game launcher into the design environment** so artists can run real spins and change art assets inside Miranda and see results immediately, turning experiments that need a full build into ~half-hour tweaks ("I talked to Dima already"). Val coached her to state the desired *outcome* rather than the engineering solution. See [[wiki/topics/nova-platform-architecture.md]] (Aug-14). [[raw/Meeting_Transcript_NOVA_Capability_Wishlist-August-14-2026-Part_2.md]]

- **Wildfire Ranch comp art.** Lena will start the comp art for Michael's new **Wildfire Ranch** game once his abstract is finished. See [[wiki/projects/nebraska-skill-market.md]]. [[raw/Meeting_Notes_NOVA_Capability_Wishlist-August-14-2026.md]]
- **South Dakota vertical games (release sequencing).** On the same day's [[wiki/decisions/2026-08-14-first-nova-product-south-dakota-vertical.md|migration-sequencing decision]], Lena is to **build the South Dakota Vertical games — Solar Keno, Aaron's Pub, Dakota Bison — new for vertical in NOVA** (they never existed in vertical, so they must be built, not converted), after Nebraska is finished. She warned that doing Nebraska on NOVA would add a 2–3 month delay, so Nebraska stays on Rage; she can develop NOVA games in parallel because platform changes (peripherals/API/Rust) don't affect how she builds games. [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]

## Sept 4 2026 — "it was verbal agreement," and the artist shortage behind the Georgia V3 slip

At the [[wiki/meetings/2026-09-04-naming-convention-standards-and-nova-conversion.md|Sept-4 afternoon game-development meeting]] Lena carried most of the meeting's factual content and most of its friction [[raw/Meeting_Notes_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]].

- **She found and explained the asset-mismatch root cause:** Fire Island games were built first as single games, so assets share names with no game qualifier — "It's not specified that it's [La Rosa] big green talker or [Crescent City Carnival] big green talker." She resisted Val's naming-convention framing ("Product was changed, we are reusing… assets from a single games products") and described the fix actually made: every folder and export must now contain a unique game code name. Asked whether the new standard was documented: "**No, it wasn't [documented]. It was verbal agreement.**" See [[wiki/decisions/2026-09-04-asset-naming-convention-must-be-written-down.md]]. [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **She has such documents for Omni/NOVA but not for Rage Studio** — "we have this document for Omni[a], for Nova, when we started to develop games in Omni[a], like **Fortune Football** or **Ca[lle Ocho] Omnia**, but we don't have this document for… Rage Studio" — and asked to start after the release, citing "shortage of artists… we['re] in a big rush to finish this release." She confirmed in the closing block that the documents exist and "we just need to move it… in… proper… repository." [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **She confirmed the Queen of Luxor graphics decision was knowingly taken** and is what moved the date: "it was a decision which we made. We knew that it will take us extra time, and **this game is ready. We can submit this product without this new graphics, but we decided to update it.**" Remaining work she named: the Queen of Luxor assets, the wider touch area on the nudge arrows (six scenes re-exported, because the touch area is defined by a planar object in the 3D scene and there are six layout types), and the horse animation. All artists in her department are on Queen of Luxor. [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **She defended the horse animation Val rejected:** "you saw it, we approved it, it was already like released and everybody liked it" — Val: "No way. It's impossible to like… The physics is wrong." [[wiki/people/anastasia.md|Anastasiya]] does the rework after finishing her Queen of Luxor tasks. [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **She showed two mock-ups** — the dual-box skill feature on Lions Riches (she had previously tried a version covering the dashboard and rejected it herself), and the South Dakota D2703 game-selection screen, where "for D27, we can easily put six games in one line and it looks good because monitor is [wide]." She confirmed she can position up to 15 games with a squeeze, and that the attract sequence is already designed to be non-static (animated logo → full-screen game with bonus → back to game selection). Val praised the layout — "you nailed the screen" — and recalled the see-through-tile carousel she built on the amusement ECHO product ~20 years earlier. [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **She set the release calendar out loud:** Nebraska to New Year's, South Dakota VLT on NOVA from January, then one more Georgia release and probably Curve before the August show; her reasoning for keeping the team together — "It's better to allocate all team because it's a new, very important release." And two confirmations she pressed for: D2703 horizontal (not vertical) is the next product for concept and design, and **no move to 4K**. [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **On premium:** she argued a premium cabinet should come from the games, not the home screen — "they should be premium not only for the reason of difference in home screen, probably games different, like more premium games… some licensed games or whatever." [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]

## Sept 11 2026 — she pushes back on the date and gets the sequencing changed

At the [[wiki/meetings/2026-09-11-rage-sunset-and-class-a-on-nova.md|Sept-11 1:00 PM game-development call]] Lena was the one who converted Val's instruction into a schedule — and changed it in the process. [[raw/Meeting_Notes_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

- **She had already started the Class A work on RAGE** — "**I started to work on this, like all this changing in dashboard, adding like extra dialogues**" — and Val's ruling that it move to NOVA discarded that start. She accepted it: "**Okay, I see, I see your point.**" See [[wiki/decisions/2026-09-11-georgia-class-a-v43-is-built-on-nova-not-rage.md]]. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **She asked for a date, was given January 1, and moved it.** "**can you give me some sense of due date… Even if we can convert like symbols and backgrounds, it doesn't mean we can convert other elements**"; then the objection that carried — "**then Nebraska, we will not finish it by the end of the year if we will do it in parallel**", "**I would rather finish Nebraska and then move whole team to NOVA projects.**" Val agreed immediately and moved to February 1. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **And she refused to let February 1 harden into a commitment:** "**Let's keep it as a… goal**", until she can see how the assets convert and "**then I can give you more… educated evaluation.**" [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **Her capacity statement: 101 days** on Nebraska with the full team, with vacations (Dima, Anastasiya for two weeks, Natalia) and a replacement hire let go, so a fresh interview and learning curve are ahead. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **She is working ahead of the platform switch deliberately** — starting the new NOVA workflow with [[wiki/people/alexander-biratka.md|Alexander Biratko]] and the developers once Dima is back, plus asset-transition experiments "**before even… full development**", in parallel with Nebraska. She also took Michael's Line Switches test-bed proposal as already her plan: "**That's what I'm going to do.**" [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **Her argument that the design work is not wasted either way:** "**design will be the same for Nova, Rage Studio, I mean design of this dialogues and dashboard.**" [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **Build status she reported:** a new bug found by [[wiki/people/ivan.md|Ivan]] — winning a progressive in Jackpot Rush or Fiery Ice Link does not show the progressive win on the topper — invisible until now "**because we cannot win progressive in Windows build**" and "**we don't have settings in show mode to win progressive**"; Natalia and Igor (and possibly Anton) work it Monday and it may need progressive-sign assets reworked. She also flagged that the Rodeo demo video must show the final version rather than the attraction video with the logo, since **Vitaliy** re-recorded it. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **She defended the duplicated progressive meters on design grounds** before Michael did — the player sees them in the same place on the home screen and inside the game, "**We made [it] intentional.**" See [[wiki/topics/slot-game-design-principles.md]] (Sept 11). [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

## Open commitments (Sept 11 2026)

- [ ] Bring the first six lines-and-ways games from Georgia V3 over to NOVA for Class A — due **goal** February 1 [2027 — year inferred], starting after Nebraska — [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [ ] Use Line Switches as the Class A NOVA test bed and do the dialogue/dashboard design — due unspecified — [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [ ] Start the new NOVA workflow with Alexander Biratko and the developers, and begin asset-transition experiments — due once Dima is back from vacation — [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [ ] Give a firmer read on whether February 1 is achievable once the asset transition is understood — due unspecified — [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [ ] Fix the progressive-win-not-shown-on-topper bug in Jackpot Rush and Fiery Ice Link — due Sept 14 2026 (Natalia and Igor work it Monday) — [[raw/Meeting_Notes_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [ ] Make sure the Rodeo demo video shows the final version, not the attraction video with the logo — due unspecified — [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [ ] Rename IP-887 to V43, keep it in backlog, archive only after migration; clean out the loose IP items; and mark IP-1061 done when it is done — due unspecified — see [[wiki/decisions/2026-09-11-ip-887-renamed-v43-and-kept-in-backlog-not-retired.md]] — [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

## Open commitments (Sept 4 2026)

- [ ] Finish the Queen of Luxor graphics and the wider touch area on the nudge arrows (six scenes re-exported) — due before the September 10 submission — [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [ ] Document the asset folder structure and multi-game naming convention with Michael Gottlieb, and create the missing Rage Studio equivalent — due after the release — [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [ ] Move the existing Omni/NOVA naming documents into the Knowledge Base standards folder — due unspecified — [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [ ] All design screens for South Dakota Real Keno while developers are on Nebraska, then redo Solar from vertical to horizontal — due through October — [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]

## Sept 17 2026 (in absentia) — she is ruled out of a piece of work, in one word

At the [[wiki/meetings/2026-09-17-kleimenychev-hire-nova-direction-and-planning-handover.md|Sept-17 12:45 PM "General alignment" call]] — which she did not attend and is not told about in either source — [[wiki/people/val-levitan.md|Val]] hired a man onto a **secret** Texas / Class A assignment and ruled that Lena is **not to be consulted on it at any point**. [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]

The man asked, through [[wiki/people/pavel.md|Pavel Frolov]], whether he could come to her with questions during the work or whether it was fully secret work. Val: "**Даю ответ.**" … "**Что абсолютно нет.**" [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]

**One thing Val said that bounds the ruling is recorded**, because without it the ruling would read as something it is not: he opened his reasoning by asking the room not to misunderstand him and saying he does **not** think badly of her. This is a secrecy instruction, not a statement against her. Full record on [[wiki/decisions/2026-09-17-kleimenychev-is-hired-from-monday-onto-texas-and-class-a-in-full-secrecy.md]].

> **⚠ §15.8 — deliberate exclusion.** Val's **stated reasoning** for the ruling is a **personal assessment of Lena's mindset**, and it is **not ingested** — not here, not in paraphrase, not anywhere in the wiki. What is recorded above is the instruction and the limit Val himself put on it. No compensation material of any kind appears in either source.

**Note on standing:** nothing here reduces her role. Across the same period she continues to lead the game-design / art side, including the Class A work on NOVA ([[wiki/decisions/2026-09-11-georgia-class-a-v43-is-built-on-nova-not-rage.md]]). The exclusion is scoped to one secret assignment.


## Sept 22 2026 — the layout costs two weeks, and the product holds fifteen games

At the [[wiki/meetings/2026-09-22-multi-game-screen-layout-and-game-count.md|Sept-22 2:45 PM multi-game screen call]] [[raw/Meeting_Transcript_Multi_Game_Screen_Layout_and_Game_Count-September-22-2026.md]]:

- **She sized the layout change.** "**It will take at least two weeks to renew the whole layout.**" That moved the progressives-on-icons layout out of V3. See [[wiki/topics/slot-game-design-principles.md]] (Sept 22).
- **She reframed the game count.** "**the actual product has 15 games, we just show 10**". See [[wiki/decisions/2026-09-11-no-new-game-badge-and-two-titles-per-category-stand.md]] (Sept-22 update).
- **Frame zero of the idle screen** "**shows mega hit blaze**", but the current layout is broken, so she could not show it. She will send it to Val.

## Open commitments (Sept 22 2026)

- [ ] Lena Zhukova — fix the broken layout and send Val the idle screen's frame zero — due unspecified — [[raw/Meeting_Transcript_Multi_Game_Screen_Layout_and_Game_Count-September-22-2026.md]]

## Sept 25 2026 — the first Class A screens, and storyboards next

At the [[wiki/meetings/2026-09-25-georgia-progressives-and-class-a-lions-riches.md|Sept-25 2:32 PM game-development call]] [[raw/Meeting_Transcript_GA_Progressives_and_Class_A_Lions_Riches-September-25-2026.md]]:

- **She showed the Class A images** for Lions Riches: the reduced dual box, the party-time message, the cash-out confirmation and the continue / print dialog. See [[wiki/topics/georgia-class-a-machines.md]] (Sept 25).
- **Class A in Nova, after Nebraska.** "**that's what we agreed that this Class A is going to be done in Nova**"; the team is working "**with Dima, Sasha Biratko, and Igor on experimenting with assets transfer and how we are going to do liquid glass in Nova**"; full production "**after Nebraska**", not before "**December, January**". See [[wiki/decisions/2026-09-11-georgia-class-a-v43-is-built-on-nova-not-rage.md]] (Sept-25 update). *(Which Dima and which Igor is not stated.)*
- **Design is mostly done; storyboards are not.** "**design is basically already done**" for the visual parts, and she will "**close this feature… of graphical adaptation, and now I will create all storyboards**".
- **Felipe's praise**, relayed by Michael: Twin Bison, the revised Lions Riches, and the parrots in Tropical Paradise.

## Open commitments (Sept 25 2026)

- [ ] Lena Zhukova — close the graphical-adaptation feature and create all the Class A storyboards so the engineers understand the flow — due unspecified — [[raw/Meeting_Transcript_GA_Progressives_and_Class_A_Lions_Riches-September-25-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]
- [[raw/Meeting_Notes_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [[raw/Meeting_Notes_NOVA_Capability_Wishlist-August-14-2026.md]]
- [[raw/Meeting_Transcript_NOVA_Capability_Wishlist-August-14-2026-Part_2.md]]
- [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- [[raw/Meeting_Transcript_lena_IP_MCP_model_regression-1-April-28-2026.md]]
- [[raw/Meeting_Notes_lena_IP_MCP_model_regression-April-28-2026.md]]
- [[raw/Clayton-Aaron-JVL-semantic-understanding-March-13-2026.md]]
- [[raw/Clayton-Aaron-JVL-semantic-understanding-March-19-2026.md]]
- [[raw/Meeting_Transcript_game_development_March-27-2026-1.md]]
- [[raw/Meeting_Transcript_game_development_March-27-2026-2.md]]
- [[raw/Meeting_Notes_game_development_March-27-2026.md]]
- [[raw/Grooming Dashboard for IP-89-March-17-2026.md]]
- [[raw/JIRA_Schedule_review-March-13-2026.md]]
- [[raw/Game_Development-March-13-2026.md]]
- [[raw/Game_Development_Schedule_Review-March-4-2026.md]]
- [[raw/Game_Development-February-27-2026.md]]
- [[raw/Game_Development_transcript_schedule_review-February-19-2026.md]]
- [[raw/Games_Design_Meeting_review_feb19_2026_v3.md]]
- [[raw/Game_Development-February-12-2026-1.md]]
- [[raw/Clayton_jvl-working-session-2-summary-January-20-2026.md]]
- [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]]
- [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- [[raw/media_tax_credit_team_coaching-july-28-2025.md]]
- [[raw/NE_game_design_and_planning-june-23-2025.md]]
- [[raw/games_design_recap-may-29-2025.md]]
- [[raw/github _structure-pavel-aaron-andrei.md]]
- [[raw/games_design-june-12-2025.md]]

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
- [[raw/tools_adaptation_games_design_department-may-7-2025.md]]
- [[raw/game_design-may-8-2025.md]]
- [[raw/Games_design-june-19-2025.md]]
- [[raw/Game_Dev-February-6-2026.md]]
- [[raw/JIRA_schedule_review_Game_Development-March-20-2026.md]]
- [[raw/SREDs_progress_review-March-20-2026.md]]
- [[raw/Meeting_Transcript_automation_progress_review-March-27-2026.md]]
- [[raw/Meeting_Transcript_Transcripts_MCP_setup_Lena-March-31-2026.md]]
- [[raw/Meeting_Notes_Transcripts_MCP_Setup_Lena-March-31-2026.md]]
- [[raw/Meeting_Notes_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [[raw/Meeting_Transcript_Michael_Gottlieb_Art_Production_Roles_and_Estimation-January-23-2026.md]]
- [[raw/Meeting_Transcript_Clayton_Lena_Game_Design_Jira_Orientation-January-27-2026.md]]
- [[raw/Meeting_Transcript_Clayton_Jira_MCP_Demo_and_Toolset_Direction-January-29-2026.md]]
- [[raw/Meeting_Transcript_Multi_Game_Screen_Layout_and_Game_Count-September-22-2026.md]]
- [[raw/Meeting_Transcript_GA_Progressives_and_Class_A_Lions_Riches-September-25-2026.md]]
- [[raw/Meeting_Notes_GA_Progressives_and_Class_A_Lions_Riches-September-25-2026.md]]
