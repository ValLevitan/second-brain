---
type: person
title: Efim Podvoiski
date: 2026-07-13
aliases: [Efim Podvoiski, Efim, Yefim, Ifim, EFIM, Podvoiski, Athim, Athene, Athena, Ethan, Epheme, Afim]
source-count: 75
open-commitments: 11
open-questions: 0
---

# Efim Podvoiski

Efim Podvoiski is the JVL engineer who **owns the RGS** (remote game server) for the online-games business — he wrote its API and describes himself as a **mathematician**, not an architect (Val notes he did not design or program the RGS platform itself). Correct name confirmed by Val as **Efim Podvoiski**; the transcripts spell the first name inconsistently (Yefim / Efim / Ifim / "EFIM"), kept as aliases for search. [[raw/Aaron_Val_2025-02-11.md]] [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]

## Role

- Authored the **RGS API** (~four calls) and its documentation, and integrated JVL's RGS to platforms both by reverse and direct integration. He keeps the **math container** as the one thing to protect and holds that everything else can be documented and published. See [[wiki/topics/rgs-architecture-and-integration.md]]. [[raw/Aaron_Val_2025-02-11.md]]
- In the Feb 11 RGS-API meeting, Val (with Aaron) pressed him on making the RGS easier for outsiders to integrate; the exchange was tense — Val said he had to "force things out of" Efim, and Efim said Val kept interrupting him. Efim ended the call needing to educate himself and regroup. [[raw/Aaron_Val_2025-02-11.md]]
- The RGS source is in **SVN** ("RSVN"); Efim had **no plan** to move it to Git and wanted to keep "EFIM"/the team out of that plan for now, but agreed RGS is a real production project he must migrate himself (a multi-day job) as **step 2** of the migration. See [[wiki/decisions/2025-02-11-git-migration-sequence.md]]. [[raw/Aaron_Val_2025-02-11.md]] [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## The math-repo isolation debate (late Jan–early Feb)

On the docs-in-Git-vs-Confluence session ([[wiki/meetings/2025-02-01-docs-in-git-vs-confluence.md]]; Efim discussed, not present): [[raw/the_importance_of_storing_artifacts_in_git.md]]

- His math sources live in **a separate repository that only he knows the organization of** — "for security reason, only Efim knows organization of this repository. I've never seen this" (Val, describing the setup); the games consume "only library made from the sources." [[raw/the_importance_of_storing_artifacts_in_git.md]]
- Working pattern: Val believes "Efim does not longer write a code," but an engineer on the call corrected him (speaker not labelled — Pavel or the attending "Dimitri") — for new math "he definitely writes his own code" and commits it to his restricted repository; he then gives an XML file / math description to **[[wiki/people/irina-makarych.md|Irina Makarych]]**, who "will create XML file for game, understandable for our framework." [[raw/the_importance_of_storing_artifacts_in_git.md]]
- **Bus factor named:** Val — "the closest person right now is [[wiki/people/anton-leshkevich.md|Anton Leshkevich]]" (not Irina); "the biggest secret of the company is the math," so access stays dangerous to widen; Aaron's answer: same commit rules, restricted visibility, plus compensating controls for one-party information. [[raw/the_importance_of_storing_artifacts_in_git.md]]
- The Confluence document Val used as the exhibit was **written by Efim** — a "Jackpot Rush Georgia" game-mechanics/math concept that will become mathematics/framework/code. [[raw/the_importance_of_storing_artifacts_in_git.md]]
- On the Feb 10 GitHub part-1 meeting Val sketched Efim as the responsible owner of the **math organization** ("Математика Ефим"). See [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]]. [[raw/github _structure-pavel-aaron-andrei.md]]

## Game math / RTP (Feb 19)

- On the Feb 19 alignment call, the South Dakota RTP submission is flagged for a **future conversation between Val, Efim, and "Michael"** and the regulator: JVL's partner misinformed them on which RTPs the regulator would accept, so only one was submitted; after go-live JVL may tweak the math on existing games to offer an additional ~92% RTP the regulator will accept. ("Michael" is unclear — see Owner Decisions.) See [[wiki/projects/south-dakota-vlt-market.md]]. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Game math and the progressive debate (Feb 21)

- On the Feb 21 Fortune Foo Paws review, Efim (transcribed **"Athim"/"Athene"/"Athena"** — inferred to be Efim from context: he owns the game math and did the help screens) reported finishing the help screens and being mid-way through a rules/calculation change. He is the one who **explained how JVL's progressive works** — the displayed value is the same at every bet; only the *probability* scales with the bet — and defended the probability method against Val's push to make the incentive visible. He noted awarding no progressive at min bet would be "a major change in the game logic." See [[wiki/topics/slot-game-design-principles.md]]. [[raw/game_design_meeting_february_21_2025.md]]
- He is a play-tester for the Miranda→math ("mass") test tool and confirmed his **HHR** work is at the "starting to work on architecture / touching things" stage. [[raw/game_design_meeting_february_21_2025.md]]

## HHR progress and the GDD (Feb 28)

- On the Feb 28 game-design review Efim (again transcribed **"Athene"**) reported the **HHR** work is progressing slowly — the team meets ~twice a week, populating stories for the HHR screens/gameplay and working on architecture and **sequence diagrams**. [[raw/Game design part 1 - Feb-28-2025.md]]
- On the Feb 28 Git check-in, Efim and [[wiki/people/michael-gottlieb.md|Michael]] are jointly writing the **Game Design Document (GDD)** for Fortune Foo Paws (in Confluence, work in progress) — Val agreed not to commit it into the repo yet. See [[wiki/topics/docs-as-code-and-atlassian-exit.md]]. [[raw/Git_progress_check_in_2025-02-28.md]]

## Nebraska skill market (Mar 14)

- Efim (transcribed "Yefim"/"Efim") pressed on Nebraska's **skill vs chance** definitions — arguing the outcome is determined by a **chance event** and that a player "can only use negative skill to lose a win," not win by skill, and questioning the "predetermined win-loss" and "unwinnable games" language. Val **dismissed** these legal-interpretation questions as "a swamp" and directed that JVL not research them (submit to the authority and let it judge). Efim also read Juan's Confluence regs and noted they give no explanation of how the game outcome should be determined, only that an RNG must be GLI-11 compatible — so JVL must explain its skill approach to the regulator. See [[wiki/projects/nebraska-skill-market.md]]. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]

## SVN→Git migration and Hollywood Bets (Mar 17)

- On the Mar 17 "reversing/distilling code into requirements" call, Val decided Efim's codebase moves **off SVN to Git first**, then continues the **Hollywood Bets** integration (due ~end of April). Efim's concern was disruption — the Jenkins builders pull from SVN, so ~5 days of build downtime — which Val judged acceptable (citing "Ratko"'s smooth Omni move; name unclear). The bulk of the migration falls to [[wiki/people/andrey-bosik.md|Andrei Bosik]]; his colleague [[wiki/people/igor-metelski.md|Igor Metelski]] was on vacation until the following Monday. Aaron framed the exercise as understanding/documenting the code (static analysis) to cut the bus-factor risk that only Efim and Igor can work on it. See [[wiki/decisions/2025-03-17-migrate-rgs-codebase-svn-to-git.md]]. [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]
- Build setup noted: dozens of applications are built individually from this codebase on **Jenkins** and auto-deployed to dev/test cloud (not prod). [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]

## The RGS diagram walkthrough for Val (~Mar 26)

~75-min Russian one-on-one where Efim walked Val through the RGS architecture diagram end to end (see [[wiki/meetings/2025-03-26-rgs-architecture-explainer.md]]; date inferred from transcription stamp): [[raw/Explain RGS.md]]

- On protection he drew the line precisely: **"МASS ENGINE и RNG SERVICE лучше не показывать"**, and the RNG is "не секретный, а защищённый" — protected from tampering, not secret; everything inside "работают, в общем-то, с деньгами" and must be protected. [[raw/Explain RGS.md]]
- On the first direct-integration documentation: **"Практически я один ее делал"** — he wrote it largely alone and hopes each next one improves; a direct wallet integration is "в размерах где-то месяца," so ~10 wallets ≈ "работа на год приблизительно." [[raw/Explain RGS.md]]
- New game features don't touch the RGS ("подставляешь только новый математический контейнер") unless money operations are involved; when Val recalled the Aristocrat buy-in game he had discussed with Michael ("Нужно было тратить. 250 долларов"), Efim classified a buy-in as "разновидность бета" (a variety of bet). [[raw/Explain RGS.md]]
- On automating new-game distribution: the Golden Matrix container insertion was manual ("подсунуть его в их гид… нажать какие-то там 10 кнопок"); "если мы с Андреем подумаем… наверное, мы придем к какому-то решению… нажатием кнопки" (which Andrei — [[wiki/people/andrey-bosik.md|Bosik]] or [[wiki/people/andrei-klimovich.md|Klimovich]] — is not stated; queued). [[raw/Explain RGS.md]]

## Val's standard for keeping him (stated Mar 26)

- In the Gottlieb one-on-one Val used Efim as his exhibit for tolerating character while someone contributes: "he has been good for the past 26 years. Talks the same way. I have the same arguments with him. I cut him off. Same thing, nothing changes for 26 years. But I ask myself the same question… Can I replace Efim? And I'm honestly asking the same question of everyone. And if I can replace, I will replace." [[raw/michael_gottlieb_val_meeting-26-2025.md]]

## RGS migration session — math-engine access and the dev/prod wall (Mar 31)

On the Mar 31 working session (see [[wiki/meetings/2025-03-31-rgs-git-migration-working-session.md]]): [[raw/rgs_git_migration-march-31-2025.md]]

- **Math-engine access is restricted to Efim alone:** on building the math servers under Linux — "there is a little question about availability of mass.engine [math engine] to everyone, because right now I am the only one who has the rights to see it." He clarified what the batch files pull "is a package, it's not actually a repository," proposed starting with the Windows local build "as we used to do," and deferred "what we do with actual mass.engine repository" to later. When Aaron said that source "you're going to need to get that on GitHub too," Efim: "Yeah, yeah, okay... Obviously I will." [[raw/rgs_git_migration-march-31-2025.md]]
- **The dev/prod "artificial wall" exchange:** Aaron called JVL's hard line between dev and production environments "unusual to me to see that"; Efim defended it — "I think it's the right thing to do, not the bad thing to do" — and asked to sit with Aaron to discuss "how we want to run MGS [likely RGS — transcript unclear] in the future," taking into account partner integrations and testing. They agreed to book a one-on-one that week based on Aaron's availability; Efim: "I'll send you some time." [[raw/rgs_git_migration-march-31-2025.md]]
- He confirmed the easy part: "we can easily migrate the parts that you see now in this batch file. And this will allow you to build local build under Windows." [[raw/rgs_git_migration-march-31-2025.md]]
- Later that day Aaron told Val that Efim and Igor "were totally unaware... had no curiosity either" about the AI-tooling work; on Val's OpenRouter account Efim's token use read as **~$55** ("It looks like Efim used $55"). [[raw/vector_meeting_db-march-31-2025.md]]

## Class II bingo math (~Mar 20 2025, date inferred — identity inference, queued)

On the Class II bingo-engine session ([[wiki/meetings/2025-03-20-class-2-bingo-engine-call.md]]) the mathematician participant is transcribed as "**Ethan**" — by context (he built the probability spreadsheet with Will and speaks to matching a slot game's pay distribution to bingo outcomes; the same transcript also renders "Ifim") this is **consistent with Efim** — recorded as an **inference, queued Tier A**, not asserted. What that participant said: the ball-index scoring approach "allows to have a lot of very fine events in bingo, with very, very, very small probabilities," groupable to "reproduce the pay distribution of a slot game practically… exactly"; a fill-the-card game-ender at ~30 balls is too improbable ("The game will never end") — more balls or more winning patterns needed; simultaneous progressive hits are handled by queueing game requests. Separately, Will reported he and "Ifim" had discussed on-site vs cloud services, and Val closed with "I will conference with Efim tomorrow and we'll get back to you [Will] on Monday" about pairing him on the Class II architecture. See [[wiki/topics/class-2-bingo-gaming-strategy.md]]. [[raw/class_2_bingo_engine.md]]

## GLI RNG rework + Val's read on him (Apr 15 2025)

- Efim returned from a ~2-week vacation on Apr 15; the **HollywoodBets** integration and the online **GLI certification** wait on him — GLI requires an **RNG rework**, which he understood after Val "помог ему правильно спросить вопросы в GLI" ("Ефим об этом уже знает. Он знает, что нужно сделать конкретно"). See [[wiki/topics/gli-certification-bottleneck.md]]. [[raw/andrei _klimovich_update-apr-15-2025.md]]
- Val's characterization to Klimovich (recorded as Val's stated view): "Ефим математик. Он не бизнесмен" — good at integration itself, weak at planning other people's time, not to be made a manager; and "по своему складу очень байнарный человек. Он говорит, что он знает, когда он уже сделал" — he won't give time estimates before something is done. Val also called it "ridiculous" that Efim had told Klimovich all developers were busy — "разработчик на интеграцию свободен." [[raw/andrei _klimovich_update-apr-15-2025.md]]
- Cross-thread: the Omni/CMS manifests product depends on "математику Ефима" (the math side must describe itself to the server), and the Calle Ocho Omni port needs his math moved into **container** form for land-based + online. [[raw/cms_github_svn-apr-15-2025.md]] [[raw/daily_omni_progress-apr-15-2025.md]]

## History — online-vision / RGS scaling (Nov 12 2024)

An older source (staged 2025-03-29, internally dated **Nov 12 2024**, earlier than everything above) records Efim among the engineers Val briefed on scaling the RGS from ~150 to ~1,000 directly-integrated casinos and releasing one online game per week. The engineers flagged that the current RGS assumes tens of accounts, not thousands, and needs re-architecting. See [[wiki/meetings/2024-11-12-online-vision-and-rgs-scaling.md]] and [[wiki/topics/rgs-architecture-and-integration.md]]. [[raw/online_vision_efim_2025-03-29.md]]

## Open commitments

- [ ] Efim — write the white paper for GLI on how the math and RNG are built and called in the new Omni framework ("So, Yefim, this is an undertaking for you") — due unspecified — [[raw/Meeting_Transcript_GLI_Omni_Platform_Certification_Kickoff-January-28-2026.md]]
- [ ] Efim — move his codebase out of SVN into Git (migration step 2, after Omni/Miranda/FlexPay), then finish the Hollywood Bets integration; Val prioritised it for the week of Mar 24 — due ~end of April — [[raw/Git_repo_structure_part_2_2025-02-11.md]] [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]
- [ ] Efim — produce a **Postman collection** and/or an **OpenAPI** document for the RGS API so tools can read the endpoints directly — due unspecified — [[raw/Aaron_Val_2025-02-11.md]]
- [ ] Efim — keep improving the RGS integration documentation from the questions each integrator asks — due unspecified — [[raw/Aaron_Val_2025-02-11.md]]
- [ ] Efim — propose times and book the one-on-one with Aaron on how to run "MGS" (likely RGS) in the future / the dev-vs-prod separation — due that week (afternoon, per Aaron's availability) — [[raw/rgs_git_migration-march-31-2025.md]]

- **Class II / bingo-engine math (owner-confirmed 2026-07-15):** the mathematician on the ~Mar-20 Class-II bingo-engine call — transcribed "**Ethan**" — is Efim. He is the one mapping a slot game's pay distribution onto bingo outcomes for the Class-II engine. See [[wiki/topics/class-2-bingo-gaming-strategy.md]] and [[wiki/meetings/2025-03-20-class-2-bingo-engine-call.md]]. [[raw/class_2_bingo_engine.md]]

## Apr 16 2025 — math container ready ~May 1

Val reported (Omni daily) that he spoke with Efim about the math: nothing needs to change, it will take about **two weeks to make it a container**, and the **math will be ready May 1**. Efim is to align the details with Alexander (Biratka) and feed the result into planning. [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]

## Math emulator play-testing (May 1 2025)

On the [[wiki/meetings/2025-05-01-game-design-review.md|May-1 game-design review]] Efim (transcribed "Athene") reported the first playable **math emulator** build — buggy but letting him and Michael play the Fortune-Foo-Paws bonuses — and discussed the CoinTrio-aligned bonus tuning (false-hit vs real-hit ratios from competitor parse sheets). He confirmed the emulator is monolithic, built in Unity/C#, and not reusable as-is for other games. See [[wiki/topics/slot-game-design-principles.md]]. [[raw/game_design_review-may-1-2025.md]]

## May 8 2025 — Mass Fortune Football math; HHR math

On the [[wiki/meetings/2025-05-08-game-design-review.md|May-8 review]] Efim (transcribed "Epheme"/"Athim"/"Afim") presented a new version of **Mass Fortune Football** and worked with Val the **math-vs-choreography** principle (the ~4–6-hit sweet spot on the "burning dots" ladder — see [[wiki/topics/slot-game-design-principles.md]]); he also explained why the games carry **no multi-denomination** (everything shown in cash). He owns the **HHR Math** (nothing else in HHR game design yet). [[raw/game_design-may-8-2025.md]]

## May 15 2025 — the Malibu math tool; flatten-and-feed for Nebraska

On the May-15 game-design review ([[wiki/meetings/2025-05-15-game-design-nebraska-south-dakota.md]]) Efim (transcribed "Athene"/"Athim"/"Afim") said it is easier to retune the Georgia predetermined-outcome games than Class-3 — "I can do whatever I want with **Malibu**" (his math tool: "you want top win to be 300 bets, you got it"). He'd flatten pay tables and feed the removed top-wins into a randomly-hitting Swift/Golden-Fast bonus (~70% of games convertible), and flagged wanting games with **hit rate ~4/5/6** so the new skill slider isn't triggered almost every spin. He was firmly **against nudge**. Detail on [[wiki/topics/slot-game-design-principles.md]] and [[wiki/projects/nebraska-skill-market.md]]. [[raw/game_design_nebraska_south_dakota-may-15-2025.md]]

## May 29 2025 — SD math + Nebraska bonus economics ([[wiki/meetings/2025-05-29-games-design-recap.md]])

On the games recap (transcribed "Athim/Athene") Efim reported working with [[wiki/people/lena.md|Lena]] on the **Queen of Luxor** math for South Dakota — a pick bonus triggered on **reel three** (1/2/3 "onks" set the number of picks), on top of free spins on reels 1–3. He drove the **Nebraska Golden Husk bonus** math questions: how much **RTP** to allocate (Georgia uses **5%**, hitting **1 in 600 games**, bonus EV ~15 bets; considering 6–7% and 1-in-300) and the base **progressive value** (Georgia Peach starts at **$2,400**; base progressive RTP ~1%). He also asked the Nebraska bet expectations (mostly $0.25–$3 max). Detail on [[wiki/topics/slot-game-design-principles.md]] and [[wiki/projects/nebraska-skill-market.md]]. [[raw/games_design_recap-may-29-2025.md]]

## June 12 2025 — game priorities: Jackpot Rush Class-3 → Nebraska skill

On the [[wiki/meetings/2025-06-12-games-design-priorities-review.md|June-12 priorities review]] Efim's sequence was set: finish **Jackpot Rush for Class 3** (Florida — "a little more work than I thought," done by end of next week), then switch to **Nebraska skill** (Golden Husk compact/wind-meter nearly ready; the hard part is the secondary skill game). He flagged the **Nebraska "per-game / per-machine progressive"** requirement (JVL doesn't usually do per-game progressives) and argued the **104%** secondary-skill ceiling is immaterial because perfect play already pushes total RTP well over 100%. He agreed to send a **win-profile comparison** of the Revision-3 at-any-bet Florida Jackpot Rush vs the Georgia version. See [[wiki/topics/slot-game-design-principles.md]] and [[wiki/projects/nebraska-skill-market.md]]. [[raw/games_design-june-12-2025.md]]

## June 19 2025 — games review

- On the [[wiki/meetings/2025-06-19-games-design-nebraska-market.md|June-19 games review]] (transcribed "a theme"/"Anna"/"Yefim") Efim reported **finishing the Jackpot Rush math** (~next day) and gave the Nebraska class-3 conversion timeline (~10 days assets, then the 6 Georgia-derived titles toward end-July). He confirmed the games are **class-3 math** with tuning to keep progressives ≤ $2,500. See [[wiki/topics/slot-game-design-principles.md]]. [[raw/Games_design-june-19-2025.md]]

## June 23 2025 — Nebraska math for the six games

On the [[wiki/meetings/2025-06-23-nebraska-game-design-planning.md|Nebraska design + planning session]] Efim ("Afim") confirmed he "has everything he needs for now" to do the **math for all six** Golden Husk games; the plan was reviewed and agreed. Adjustments captured: **Crazy Spins** needs an additional wild symbol; **Midnight Money** was tuned so there aren't too many free spins; **RNG** drives the secondary pattern randomness; fractional wins round up (ceiling). He'll document the changed math in his "mass" features. See [[wiki/projects/nebraska-skill-market.md]] and [[wiki/topics/slot-game-design-principles.md]]. [[raw/NE_game_design_and_planning-june-23-2025.md]]

## July 8 2025 — the Class-3 hold problem + the Fiery-Ice progressive dig

On the [[wiki/meetings/2025-07-08-games-design-mathematician-debate.md|July-8 weekly]] (transcribed "Athene/Atheem/Epheme/Afim/Rafim") Efim is the mathematician at the center of Val's "is the Class-3 math the problem?" question — Val floated adding an **outside industry mathematician as a sounding board** for Efim (Michael: "a raw math guy we already have in [Efim]… we need the industry guy"). Efim is running the **Fiery Ice Link / Jackpot Rush progressive investigation**: he suspects the progressives may have **awarded more than expected** and is pulling **raw progressive-controller data** (he never uses **Tableau**, which is down on a 30-day timeline — "Dimitri" extracts the raw data manually) via Pavel's **"Arrow Admin"** tool. His stated constraint on the copied Aristocrat/Lightning-Link math: the par sheet "gives the math only for prime/basic/bonus but doesn't indicate the peaks and valleys." See [[wiki/topics/slot-game-design-principles.md]]. [[raw/games_design-july-8-2025.md]]

## ~July 18 2025 — the progressive-overpay hypothesis (Efim's counter) + math-test estimate

On the [[wiki/meetings/2025-07-18-progressive-overpay-alignment.md|~July-18 alignment call]] (Val, [[wiki/people/juan-martinez.md|Juan]], Efim; Efim joined mid-call from a **2-day vacation in Fenelon Falls, Ontario**), Val put the hypothesis that JVL games **overpay because the progressive is double-counted into the base RTP**. Efim **pushed back**: the increments pay **exactly** what they should, the progressive is **in-game** (an in-game event triggers it) and has **nothing to do with the progressive controller / frequency**, and the **mass-test already produces a correct result** on a single machine; he called the idea "very, very stretched" but conceded "everything is possible." He agreed to set up a **single-machine progressive at 0 contribution** and to have **[[wiki/people/anton-leshkevich.md|Anton]]** adapt the mass-test to run with **fluctuating bets** — his estimate **~20 days** ("somebody has to do it… Anton, maybe"). Recorded as an **open disagreement** (not resolved). Full detail on [[wiki/topics/slot-game-design-principles.md]]. [[raw/Overall_alignment.md]]

## Jul 31 2025 — amusement-games revival

With [[wiki/people/val-levitan.md|Val]] and [[wiki/people/lena.md|Lena]], Efim assessed reviving the ~150 legacy amusement games: the old C++ games must be **rebuilt whole** (idea reusable, not assets); the hardest was **poker / Texas Hold'em** (outdated); JVL can port C++ physics libraries but should avoid real 3D; ~**2 years for ~50 games**, at best ~1 game / 2 weeks. In the parallel Pavel session Efim is named the **math / standby** resource for the physics-heavy games. Full substance: [[wiki/topics/amusement-games-revival.md]]. [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]] [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]

## Aug 7 2025 — commissions the Player Behavior Simulator (+ ≈Aug-8 engineering discussion)

On the [[wiki/meetings/2025-08-07-player-behavior-simulator.md|Aug-7 meeting]], Efim presented his Fiery Ice analysis — **actual RTP ≈ 92.43% vs expected ≈ 91.72%** and **77 major progressive events vs ~64 expected** (≈7% probability, "quite normal") — and argued the ~25-30% negative days are a **feature of the math, not a bug** (his random-bet simulation reproduced ~25-26% negative days). He agreed to **build the Player Behavior Simulator in ~4 days in Python**: the tool holds **no math** — he first runs **~100M games in his math simulator**, writes each outcome's frequency to a file, and the simulator consumes that file to play sessions; parameters in a file/batch, results in a readable good-vs-bad-session report; [[wiki/people/anton-leshkevich.md|Anton]] only needed for a GUI. He also undertook to try to extract real player-session boundaries from the ~1M-game progressive-controller dataset, and — with [[wiki/people/michael-gottlieb.md|Michael]] — to stand ready to build a **less-volatile Fiery Ice math model** (same RTP). Notably he had told Val he is **not sure the Diamond-Link-derived mechanic can be made less volatile while staying interesting** (the remark that convinced Val the mechanic itself may be wrong). He described himself as "just a mathematician… I was an apprentice"; Val insisted he is part of game design, not just math. [[raw/Player_behavior_simulator.md]]

On the smaller [[wiki/meetings/2025-08-08-player-simulator-engineering-discussion.md|≈Aug-8 Val+Efim+Anton session]] (Russian) he repeatedly re-framed Val's player-behaviour use case as a math/product test (Val pushing back that he wants to emulate the *player*, not the math), and proposed the name "player station simulator." [[raw/player_emulator.md]]

## Jan 28 2026 — the GLI Omni kickoff: the math/RNG white paper

On the [[wiki/meetings/2026-01-28-gli-omni-platform-certification-kickoff.md|GLI kickoff]] Val gave Efim the math/RNG white paper for GLI (see Open commitments). When GLI's Dan Lewis asked to test from JVL's own ecosystem, Efim checked his understanding: "you are looking for something like a scale, say, I push these numbers, and I want to see this set of numbers after they are used." Dan agreed. See [[wiki/topics/gli-certification-bottleneck.md]] (Jan 28 2026). [[raw/Meeting_Transcript_GLI_Omni_Platform_Certification_Kickoff-January-28-2026.md]]

## Feb 12 2026 — shader realism; the single-programmer South Dakota risk

On the [[wiki/meetings/2026-02-12-game-development-review.md|Feb-12 review]] (segment 1). [[raw/Game_Development-February-12-2026-1.md]]

- **Flagged that [[wiki/people/igor-metelski.md|Igor Metelski]] is away ~2 months** and asked whether South Dakota can finish "with a single programmer." (The team is scoping [[wiki/people/anton-leshkevich.md|Anton]] inheriting Igor's assignments.) [[raw/Game_Development-February-12-2026-1.md]]
- On the liquid-glass debate, gave the engineering realism: a custom glass shader "we don't know how to do, we'd have to experiment, and it might not run on our hardware," and pressed the process point — **"put the horse before the cart: do we even need it?"** — before spending on a real-time-recolour background feature. See [[wiki/topics/slot-game-design-principles.md]] (Feb-12). [[raw/Game_Development-February-12-2026-1.md]]

## Feb 19 2026 — Games Design Meeting: dynamic progressive frequency; ADR-vs-requirement

On the [[wiki/meetings/2026-02-19-games-design-meeting.md|Feb-19 Games Design Meeting]]. [[raw/Game_Development_transcript_schedule_review-February-19-2026.md]]

- **Progressive math (session 1).** Efim explained the new GC-351 progressive is a **predetermined outcome**, so he can **dynamically adjust hit frequency per level** via the RTP allocated to each level — base level ≈ **1 in 10,000 spins at $1** (~once every 10–15 days at a typical ~1,000–1,200-pull location). He needs the team to agree a **~2–3% total base-level progressive RTP** (he leans ~2.5%, increment ~1%) before finalizing game math, and will share the **Fiery Ice** progressive parameters as a baseline. He stressed base-level RTP and increment RTP are **two separate things**. See [[wiki/topics/slot-game-design-principles.md]] (Feb-19). [[raw/Game_Development_transcript_schedule_review-February-19-2026.md]]
- **ADR vs requirement (session 2).** Asked by Val whether the progressive decisions are Architectural Design Records, Efim ruled they are **product requirements, not ADRs** — they originate from Juan/Felipe market observations and get translated into JVL's technical answer by the team. He also asked Val the conclusion on the single-programmer South Dakota risk (answer: a ~one-month schedule extension for [[wiki/people/igor-metelski.md|Igor Metelski]]'s military camp). [[raw/Game_Development_transcript_game_review-February-19-26.md]] [[raw/Game_Development_transcript_schedule_review-February-19-2026.md]]

## Feb 27 2026 — game-development review: random coin placement; secondary-skill statistics

On the [[wiki/meetings/2026-02-27-game-development-review.md|Feb-27 game-development review]]. [[raw/Game_Development-February-27-2026.md]]

- **Insisted the dual-box coin placement be random.** Efim pushed that the larger coin **randomly toggle** left/right rather than always sitting on the right — otherwise players learn the pattern, auto-click, lose, and get upset. Michael updated the abstract to specify random presentation. See [[wiki/topics/slot-game-design-principles.md]] (Feb-27). [[raw/Game_Development-February-27-2026.md]]
- **Flagged the missing secondary-skill statistics.** He noted JVL has no data on how often players use the secondary Simon-Says feature or how much they lose by missing the primary skill — "nice to have, not necessary" for this release (Juan agreed to skip it). [[raw/Game_Development-February-27-2026.md]]
- **Raised a Jira-taxonomy question.** He has no dedicated IP for his math-engine feature work when the feature isn't tied to a specific game not yet in production — deferred to a separate one-on-one with Val. [[raw/Game_Development-February-27-2026.md]]

## Mar 4 2026 — game-development review (attended)

On the [[wiki/meetings/2026-03-04-game-development-schedule-review.md|Mar-4 game-development review]] Efim attended the dual-box / production walk-through; he agreed the South Dakota result was a genuinely good week and confirmed the go-ahead on the production items. (No new distinct design position beyond his [[#feb-27-2026--game-development-review-random-coin-placement-secondary-skill-statistics|Feb-27 random-coin-placement and secondary-skill-statistics points]], which carry into this build.) See [[wiki/topics/slot-game-design-principles.md]] (Mar-4). [[raw/Game_Development_Schedule_Review-March-4-2026.md]]

## Mar 13 2026 — weekly game-dev review (attended; Twin Bison math parameters)

On the [[wiki/meetings/2026-03-13-game-development-review.md|Mar-13 game-development review]] Efim mostly listened. His only work item at this point was a **concept task** — he **prepared the math ("mass") parameters for the "twin bison"** and attached a small discussion document to the abstract, but had **not yet built a special feature** for it. Val deferred the integration question (how Efim's work fits with everyone else's) to a **separate conversation**, out of this meeting. Efim would also join [[wiki/people/lena.md|Lena]]/[[wiki/people/michael-gottlieb.md|Michael]] in playing the final Calle Ocho-Omni build for the timing pass. Design detail on [[wiki/topics/slot-game-design-principles.md]] (Mar-13). [[raw/Game_Development-March-13-2026.md]] [[raw/JIRA_Schedule_review-March-13-2026.md]]

## Mar 20 2026 — Omni show-mode virtual-screen mapping; SR&ED project list

Two Mar-20 calls. On the **[[wiki/meetings/2026-03-20-game-development-schedule-review.md|game-development schedule review]]** Efim's durable contribution was on the **Omni "show mode"** need — he framed it as being able to **flexibly arrange/map virtual screens into actual windows** on the bench (matching the multi-screen Rage environment), part of the release-loading architecture Val took as an undertaking. See [[wiki/topics/slot-game-design-principles.md]] (Mar-20). On the **[[wiki/meetings/2026-03-20-sred-progress-review.md|SR&ED progress review]]** he was present as the RGS/math R&D lead while the team compiled the 2025 project list (Val to draft it by Wednesday). See [[wiki/topics/sred-tax-credit.md]] (Mar-20). [[raw/JIRA_schedule_review_Game_Development-March-20-2026.md]] [[raw/SREDs_progress_review-March-20-2026.md]]

## Mar 26 2026 — the languages / design-standards architecture debate (with Val)

A sharp one-on-one written Q&A / debate with [[wiki/people/val-levitan.md|Val]] (see [[wiki/meetings/2026-03-26-debate-with-efim-system-languages.md]]) over whether spreading the machine's software across **multiple programming languages** is itself a reliability/design-standards risk. Efim is the architecture/math-engine voice against Val's "more languages = more standards = more incompatibility" concern — the debate establishes that the OMNI **Math Engine is C++, ~50k lines, the same engine as RAGE/RGS** (C++ by path dependency; Java or Rust "could be a better choice from scratch" but C++-with-Java-LGS is "not" an architecture problem — "a clear no"), and that in RAGE the Math Engine talks to Framework directly while Framework↔DC and DC↔Setup go over HTTP (DC is **Java**, not JS). Consistent with Val's read of him as "very binary" and the "same arguments for 26 years." Substance on [[wiki/topics/omni-core-advancement-and-game-templating.md]] (Mar-26-2026). (Fine-grained line attribution is unclear in the source and not asserted.) [[raw/debate_with_Efim-March-26-2026.md]]

## Mar 27 2026 — weekly game-dev review: keno demo-mode gap

On the [[wiki/meetings/2026-03-27-game-development-review.md|Mar-27 game-development review]] Efim attended the schedule/production walk-through and flagged the **keno demo-mode gap**: because Cool Cat Keno is JVL's first keno, there was no template or rules for a demo mode, so he was building one on the fly to let QA work with the game (the keno tasks weren't broken down in detail up front). He also gave design input on the Twin Bison free-spins/precog mechanic. [[raw/Meeting_Transcript_game_development_March-27-2026-1.md]] [[raw/Meeting_Transcript_game_development_March-27-2026-2.md]] [[raw/Meeting_Notes_game_development_March-27-2026.md]]

## Mar 30 2026 — reported to have agreed to the math→Rust migration (OMNI 2)

Second-hand, via Val on the [[wiki/meetings/2026-03-30-omni-architecture-biratka.md|Mar-30 Biratka call]]: Val says he "mentally won Efim over" and that Efim agreed to **become a Rust expert within ~three months and migrate all the math code to Rust** as part of the OMNI 2 three-language plan (Rust/TypeScript/Java, dropping C/C++). The C/C++ migration splits into two projects — **math → Efim**, HAL → Anton — and Val describes both as having signed on. This evolves the Mar-26 position in which Efim defended the C++ math engine as not an architecture problem: the language change is now agreed. (Reported by Val, not Efim directly.) Substance on [[wiki/topics/omni-core-advancement-and-game-templating.md]] (Mar-30). [[raw/Meeting_Notes_OMNI_Architecture_Biratko-March-30-2026.md]] [[raw/Meeting_Transcript_OMNI_Architecture_Biratko-March-30-2026.md]]

## Apr 27 2026 — Multi-Progressive scoping call (garbled source)

On an Apr-27 one-on-one with [[wiki/people/val-levitan.md|Val]] ([[wiki/meetings/2026-04-27-efim-progressives-discussion.md|Efim Progressives Discussion]], 8:38pm) the two framed a **"Multi-Progressive"** offering as a new game category and worked through where progressives sit in the requirements → capabilities → features methodology. Efim referenced JVL's existing progressive work (including a **three-level progressive** structure) and pushed back at points on the capability/requirements categorisation, so alignment was not complete. **Source caution:** the Teams transcript was in Russian and auto-translated to near-nonsense — only the topical structure is reliable; no decision or commitment was recoverable, and fine-grained attribution is not asserted. The multi-progressive framing is captured on [[wiki/topics/slot-game-design-principles.md]] (Apr-27 subsection). [[raw/Meeting_Notes_efim_progressives_discussion-April-27-2026.md]] [[raw/Meeting_Transcript_efim_progressives_discussion-April-27-2026.md]]

## Aug 14–21 2026 — planned absence from Sept 15; the RAGE math on Rust; Dragon Pays math; Match-3 for Nebraska

- **A planned absence from Sept 15 2026 (a Tuesday)** — a durable scheduling fact. Efim expects to be out for the end of that week and unable to work properly afterward for a while; Val's instruction: "**do your math before September 15**." [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- **NOVA wishlist (Aug 14).** As math owner Efim asked for a **better, faster prototype path** (get a game up and playable with placeholder assets without waiting ~2 weeks for a Windows build) and named his "holy grail": seeing **individual player behaviour** at the machine, not just averages — while conceding it needs backend/player-tracking that doesn't exist in current markets. He also agreed to work with Michael on quickly prototyping gameplay/mechanics. See [[wiki/topics/nova-platform-architecture.md]] (Aug-14). [[raw/Meeting_Transcript_NOVA_Capability_Wishlist-August-14-2026-Part_2.md]]
- **RAGE→NOVA experiment review (Aug 18).** Efim has already **partly ported the RAGE math to Rust**. The horizontal-migration experiment is blocked because **Dragon Pays' math is missing from the remote math server** (only Calle Ocho's was set up); Efim agreed to supply it (~a day's work, Thu–Fri outside date) so [[wiki/people/igor-metelski.md|Igor]] can run the game logic. He also drove the **math-as-a-service Docker container packaging** decision (build the container from a game list at the integration-build step, one per game set/market; he resisted the all-in-one and fully self-configuring options as premature) — [[wiki/decisions/2026-08-18-nova-math-container-per-game-set.md]]. [[raw/Meeting_Notes_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]] [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- **Match-3 for Nebraska (Aug 21).** Efim will build the **Match-3 progressive for Nebraska** (replacing Golden Husk), ~3 weeks, before a planned absence, logged in Jira as a capability. See [[wiki/projects/nebraska-skill-market.md]]. (These commitments are tracked on the NOVA topic and Nebraska project pages.) [[raw/Meeting_Notes_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]

## Sept 4 2026 — "Convention was there, but it was inadequate"

At the [[wiki/meetings/2026-09-04-naming-convention-standards-and-nova-conversion.md|Sept-4 afternoon game-development meeting]] Efim supplied the formulation that ended the naming-convention argument and the explanation that ended the branch one [[raw/Meeting_Notes_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]].

- **The formulation:** "**Convention was there, but it was inadequate.**" See [[wiki/decisions/2026-09-04-asset-naming-convention-must-be-written-down.md]]. [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **He explained branching to Juan from first principles:** branches exist in the source-control tool so that "changes that made for other products or for improvement… don't contaminate the current development"; because JVL's products go different ways and sometimes return or move jurisdiction, "you have to make a decision from what… snapshot… you start your product, and… that's the branch." Why it is hard: "you have similar product, but very old code base with old bugs and no features in data center… and you have newer products, but different games and what to choose. It's not always very clear where to start." He agreed with Lena's working rule — the branch closest to the current requirements. [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **He defended the developers' judgement** in the Florida-branch incident: "they made the decision that they thought was right, for some reason… but then people forgot to fix the assets. And in Michael's mind, these assets are already there, but they are not." Val's reply: "if you rely on your memory, you're bound to forget something." [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **He blocked the credits-on-buttons change on maths grounds:** "we cannot do it like this, because unfortunately the ma[ths] is done in… such a way that there are different denominations in some games, not one [cent] denomination." He named **Crazy Spins** as a top game when Val asked what could be pulled. [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **He asked the question nobody could answer about the V-deck theory:** "do we know that aristocrat or whoever has the mechanical buttons and start with dollar… [has an] average bet… higher than ours significantly? … They make more money, but… is it due to high number of plays? … do they also have a higher average bet? Because if they don't, then… probably doesn't work." He proposed testing a partial hardware swap on some machines within one release; Michael killed it as "a very expensive test." His concession: "At least if you are making a mistake in this direction, it's mistakes that everybody will be making soon." [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **He explained the game-loading limit** as memory for graphical assets rather than maths: "We want almost everything build ready when you [press the button], otherwise you have loading time." [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **Val's account of Efim's own work, given the same morning to the engineering meeting:** "ефим переписал свой си плюс плюс математику свою на[ ]раст" — he has rewritten his C++ maths in Rust. The **maths server is now being opened up** and needs its own data contract, with access granted to the framework side; Val: "у нас нету почти тайны в математике." See [[wiki/decisions/2026-09-04-data-contracts-closed-every-repository-by-september-11.md]]. [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]

## Open commitments (Sept 4 2026)

- [ ] Check the denomination mix across the Georgia titles to establish whether a credits-only button display is possible at all — due unspecified — [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [ ] A data contract for the maths server, with access opened to the framework and DataCenter side — due unspecified — [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]] *(Sept 30 2026: on the repo-standards call he named the maths-engine repository and a data contract in one breath; whether the contract is written is unreadable — not discharged [[raw/Meeting_Transcript_Repo_Standards_Walkthrough_with_Efim-September-30-2026.md]])*

## Sept 8–9 2026 — told to change the maths on two games and put credits on the buttons

[[wiki/people/val-levitan.md|Val]] decided on the evening of **Sept 8 2026 at 9:00 PM** and wrote to Efim that night; he reported it the next morning at the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept-9 7:02 AM call]]: "[р]ешение… было принято вчера в 21:00[.] Я ему написал, чтобы он делал математику." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

The change: currency on the buttons is replaced by credits, and the maths on **two games** changes — "[Е]фим сказал, что ему нужно поменять математику на 2 играх и сказал, что это **14[ часов] работы**." On that basis Val expects it with the team by **Sept 11**: "до 11 числа он должен вам сдать." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

**Note the mismatch of understanding:** [[wiki/people/irina-shishko.md|Irina]] reported that Efim had told her the decision was not yet taken — "[о]н сказал, что решение ещё не принято" — which Val overrode on the call. Full record on [[wiki/decisions/2026-09-08-credits-not-currency-on-the-buttons-and-two-games-remathed.md]]. [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]] [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

## Sept 11 2026 — his argument decides the platform, and he books time away

At the [[wiki/meetings/2026-09-11-rage-sunset-and-class-a-on-nova.md|Sept-11 1:00 PM game-development call]] Efim's intervention is what turned Val's preference into a settled decision. [[raw/Meeting_Notes_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

- **He sided with Val against Michael on the Class A platform, and gave the reason that carried:** "**I agree with Val in this case. We… don't see all the changes that we need to do in the framework, but they might be substantial and doing anything in this rage framework, something new, it will. Be a lot of work that will be wasted**" — with the conversion evidence, "**the conversion of the assets is proven that it is proven that this can be done relatively easily**", and the long view, "**we will have a more solid product and more life in future for this efforts.**" He was candid about the confidence level: "**it might be wrong, it might be fifty-fifty.**" See [[wiki/decisions/2026-09-11-georgia-class-a-v43-is-built-on-nova-not-rage.md]]. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **He is the one who has to specify Class A behaviour, and he is blocked.** Michael asked him to write up "credits in, awards out, awards not usable for betting" for the programmers; Efim agreed but wants to understand the **party time** feature, the **streak** and the **three spins** first, expecting information in "**Two, 3 weeks**", and insisted "**before it, no programmers will touch this.**" See [[wiki/topics/georgia-class-a-machines.md]] (Sept 11). [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **On the home-screen game count he gave a number and disclaimed it:** "**12 is not optimal already**… **my guess is optimum is about like 6 to 9 somewhere and 12 is acceptable**", then "**I cannot confirm it in any way, scientifically.**" He also agreed with Michael that a new-game badge does not matter — a passer-by "**might try it**" whether the swap was that day or a week earlier. See [[wiki/decisions/2026-09-11-no-new-game-badge-and-two-titles-per-category-stand.md]]. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **Away from Tuesday Sept 15 2026.** Out **Tuesday through Thursday**, reachable **by phone only for emergencies**, with a gradual return to work after. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

**§15.8:** clear — role and product content only.

*(Personal matters removed — owner ruling 2026-09-28.)*

**Open commitments (Sept 11 2026)**

- [ ] Write up Class A behaviour (money in gives credits; wins give awards; awards cannot be bet) so programmers can start thinking about it — due after the party-time and streak mechanics are understood; he expects information in two to three weeks — [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

**Open commitments (Sept 8 2026)**

- [ ] Replace the currency on the buttons with credits and change the maths on two games (his own estimate: about 14 hours) — due Sept 11 2026 — **still outstanding as of Sept 11 2026, 1:00 PM:** [[wiki/people/michael-gottlieb.md|Michael]] reported that day "**We still need to get this currency switched over to credits on the VDEC implemented**", and the derived notes list it unassigned. The maths half is not mentioned either way. Not discharged — [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]] [[raw/Meeting_Notes_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]] — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]] [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]


## Sept 22 2026 (in absentia) — waiting on the Nebraska settings

At the [[wiki/meetings/2026-09-22-multi-game-screen-layout-and-game-count.md|Sept-22 2:45 PM multi-game screen call]], [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] said "**Efim needs answers**" on Nebraska progressive settings and bet levels, and that he would start giving them himself rather than leave Efim waiting. See [[wiki/projects/nebraska-skill-market.md]] (Sept 22). *(The transcript renders his name "a theme" in two lines.)* [[raw/Meeting_Transcript_Multi_Game_Screen_Layout_and_Game_Count-September-22-2026.md]]

## Sept 25 2026 — the RIS spot check, and the Class A math without nudge

At the [[wiki/meetings/2026-09-25-georgia-progressives-and-class-a-lions-riches.md|Sept-25 2:32 PM game-development call]] [[raw/Meeting_Transcript_GA_Progressives_and_Class_A_Lions_Riches-September-25-2026.md]]:

- **Val asked him to spot-check the RIS actually installed** on a Georgia machine, after the V2 machines went out at 96.5%. Commitment on [[wiki/projects/georgia-market-rollout.md]] (Sept 25, 2:32 PM). He also joins Michael to check the V3 release on a live machine. See [[wiki/decisions/2026-09-25-georgia-machines-go-out-at-92-percent-and-the-progressive-tops-are-2400-2400-1500.md]].
- **He backed the progressive values** as "**something in the middle**", since there is no data to go far in any direction.
- **Class A math.** Lions Riches Georgia is a nudge game, so he must redo the math for Class A. His challenges: the **$50 cap**, free spins, party time, and the number of math files. His idea: pay the part of the distribution above $50 through party time — "**maybe 10, 15, 20% of RTP**". See [[wiki/topics/georgia-class-a-machines.md]] (Sept 25).
- **Nebraska software**: "**It's basically class 3, yes, I think**" (with the dual box added).
- Asked by Val whether his "**rust… portion**" is done: "**Yes, it's ready for use.**" What "rust" means here is unclear.

*(Personal matters removed — owner ruling 2026-09-28.)*

## Open commitments (Sept 25 2026)

- [ ] Efim Podvoiski — work out the Class A Lions Riches math without nudge ($50 cap, free spins, party time) — due unspecified — [[raw/Meeting_Transcript_GA_Progressives_and_Class_A_Lions_Riches-September-25-2026.md]] — **Oct 8 2026:** one free-spins answer agreed with Michael (party time may follow on the next paid spin); whether payouts below $50 are used is still to be checked in the maths — [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]]

## Sept 30 2026 (11:07 AM) — walked through the repo standards by Val; topic words only

A 13-minute one-on-one with Val ([[wiki/meetings/2026-09-30-repo-standards-walkthrough-with-efim.md]]; per the notes spoken mostly in Russian but transcribed as English, so almost nothing is readable) [[raw/Meeting_Notes_Repo_Standards_Walkthrough_with_Efim-September-30-2026.md]]. What survives [[raw/Meeting_Transcript_Repo_Standards_Walkthrough_with_Efim-September-30-2026.md]]:

- **Val pointed him at the repo standards in GitHub** — "I pointed I pointed you to a repo standards", "standards, material", "it's for GitHub" — and ran through subjects: "repository organ zone [organisation]… zero trust… data contract repository", "ADRs", "discussion", "Pull request pull request", "Claude Reviewer is to cache the pull request" (verb **unclear**), "Local computer". This is the Sept-4 standing instruction ([[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]], Sept-30 update) applied to him in person.
- **His own words, as fragments:** "Repository mass engine… data contract. But the robot is Nova" — the maths-engine repository, a data contract, NOVA; "Excel file… result of the test of mathematics" — an Excel file with maths test results. No status, undertaking or decision is readable; the Sept-4 data-contract commitment above is not discharged by this.
- Val near the end: "we committed", "lines of code", "I encourage you", "Proser [prose — **inference**] defines standard, but the most of principle, but not defined" — sense not recoverable.

**§15.8:** Val's opening "you're doing remarkably well" has no readable subject and is held, not recorded either way. Nothing on pay or performance is recorded. **§15 #9:** none.

## Oct 2 2026 (in absentia) — his written note on the South Dakota maths: the minimum bet from 50 cents to 40

At the [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 Minsk stand-up]] (Russian; he was not on it) [[wiki/people/ivan.md|Ivan]]: "у меня ефим вчера много чего писал я Ирине перекидывал. Это касательно [South Dakota]… Я так понимаю для математики?… где было 50 центов. Минимальная ставка сделали 40" — a written note from "ефим" (this page, by context — the South Dakota maths; inference) on Oct 1 changing the minimum bet from 50 cents to 40, handled by Irina and Ivan as a RIS with the 40-cent minimum and no rebuild. See [[wiki/projects/south-dakota-vlt-market.md]] (Oct 2) [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]. The note itself is not in the corpus.


## Oct 8 2026 — party time after free spins, the Nebraska configuration review, and a touch-area idea turned down

At the [[wiki/meetings/2026-10-08-game-design-class-a-party-time-and-dual-box.md|Oct-8 12:00 PM game-design meeting]] (English) [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]]:

- **Class A.** With Michael he came up with the rule that the paid spin after free spins may trigger party time; he will explain Class A behaviour to the developers in Russian at the kickoff — [[wiki/decisions/2026-10-08-class-a-party-time-may-start-on-the-paid-spin-after-free-spins-and-lions-riches-is-the-single-target.md]]
- **Nebraska.** His review of the configuration page found "a couple of things that needed to get adjusted"; he and Michael argued out the progressive reset levels to a baseline — [[wiki/projects/nebraska-skill-market.md]].
- **Select-a-coin.** He suggested a smaller touch box for the wrong coin; Michael refused — [[wiki/decisions/2026-10-08-dual-box-for-nebraska-class-a-and-georgia-five-reel-and-no-smaller-touch-area-for-the-wrong-coin.md]]

### Open commitments (Oct 8 2026)

- [ ] Efim Podvoiski — explain Class A behaviour to the developers in Russian at the Class A kickoff — due kickoff (date not set) — [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]]

## Oct 15 2026 (in absentia) — Clover Fortune added to the maths server

At the [[wiki/meetings/2026-10-15-daily-standup-offline-ris-fallback-and-nova-game-conversion.md|Oct-15 stand-up]] Leshkevich said he had asked "ефима" to add Clover Fortune to the maths server "который сейчас л джи смотрит" (the notes: GLI [[raw/Meeting_Notes_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]), so the converted game runs on real data — [[wiki/topics/nova-platform-architecture.md]] (Oct 15) [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]].

## Oct 16 2026 (in absentia) — the Dutch Mill maths in a container

At the [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct-16 stand-up]] Igor Metelski: "мне ефим собрал в контейнере математику подчмил… для о мни короче формата" — the Dutch Mill maths packed in a container for the OMNI format; Igor asked for one game and will run the server locally [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] — [[wiki/decisions/2026-10-08-texas-rage-games-convert-to-vertical-nova-unchanged-and-igor-ports-dutch-mill-first.md]] (Oct-16 update).

## Oct 19 2026 (in absentia) — the Clover Fortune maths container

At the [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct-19 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] Leshkevich said Efim made the maths container for Clover Fortune almost in one day. Whether he made it for all six games or one is open; Igor is to be asked — [[wiki/decisions/2026-10-18-rage-is-closed-dutch-mill-reaches-nova-by-wednesday-and-a-reskin-from-a-new-theme-tests-the-tools.md]] (Oct-19 update).

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Notes_Repo_Standards_Walkthrough_with_Efim-September-30-2026.md]]
- [[raw/Meeting_Transcript_Repo_Standards_Walkthrough_with_Efim-September-30-2026.md]]

- [[raw/Meeting_Notes_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- [[raw/Meeting_Transcript_NOVA_Capability_Wishlist-August-14-2026-Part_2.md]]
- [[raw/Meeting_Notes_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- [[raw/Meeting_Notes_Multiplayer_Cabinet_Concepts_NOVA_Strategy-August-21-2026.md]]

- [[raw/Meeting_Transcript_efim_progressives_discussion-April-27-2026.md]]
- [[raw/Meeting_Notes_efim_progressives_discussion-April-27-2026.md]]
- [[raw/Meeting_Notes_OMNI_Architecture_Biratko-March-30-2026.md]]
- [[raw/Meeting_Transcript_OMNI_Architecture_Biratko-March-30-2026.md]]
- [[raw/Meeting_Transcript_game_development_March-27-2026-1.md]]
- [[raw/Meeting_Transcript_game_development_March-27-2026-2.md]]
- [[raw/Meeting_Notes_game_development_March-27-2026.md]]
- [[raw/debate_with_Efim-March-26-2026.md]]
- [[raw/JIRA_Schedule_review-March-13-2026.md]]
- [[raw/Game_Development-March-13-2026.md]]
- [[raw/Game_Development_Schedule_Review-March-4-2026.md]]
- [[raw/Game_Development-February-27-2026.md]]
- [[raw/Game_Development_transcript_schedule_review-February-19-2026.md]]
- [[raw/Game_Development_transcript_game_review-February-19-26.md]]
- [[raw/Game_Development-February-12-2026-1.md]]
- [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]]
- [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- [[raw/Overall_alignment.md]]
- [[raw/games_design-july-8-2025.md]]
- [[raw/NE_game_design_and_planning-june-23-2025.md]]
- [[raw/games_design_recap-may-29-2025.md]]
- [[raw/online_vision_efim_2025-03-29.md]]
- [[raw/games_design-june-12-2025.md]]
- [[raw/the_importance_of_storing_artifacts_in_git.md]]
- [[raw/github _structure-pavel-aaron-andrei.md]]
- [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- [[raw/Aaron_Val_2025-02-11.md]]
- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- [[raw/game_design_meeting_february_21_2025.md]]
- [[raw/Game design part 1 - Feb-28-2025.md]]
- [[raw/Git_progress_check_in_2025-02-28.md]]
- [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]
- [[raw/Explain RGS.md]]
- [[raw/rgs_git_migration-march-31-2025.md]]
- [[raw/vector_meeting_db-march-31-2025.md]]
- [[raw/michael_gottlieb_val_meeting-26-2025.md]]
- [[raw/class_2_bingo_engine.md]]
- [[raw/andrei _klimovich_update-apr-15-2025.md]]
- [[raw/cms_github_svn-apr-15-2025.md]]
- [[raw/daily_omni_progress-apr-15-2025.md]]
- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- [[raw/game_design_review-may-1-2025.md]]
- [[raw/game_design-may-8-2025.md]]
- [[raw/game_design_nebraska_south_dakota-may-15-2025.md]]
- [[raw/Games_design-june-19-2025.md]]
- [[raw/Player_behavior_simulator.md]]
- [[raw/player_emulator.md]]
- [[raw/JIRA_schedule_review_Game_Development-March-20-2026.md]]
- [[raw/SREDs_progress_review-March-20-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [[raw/Meeting_Transcript_GLI_Omni_Platform_Certification_Kickoff-January-28-2026.md]]
- [[raw/Meeting_Transcript_Multi_Game_Screen_Layout_and_Game_Count-September-22-2026.md]]
- [[raw/Meeting_Transcript_GA_Progressives_and_Class_A_Lions_Riches-September-25-2026.md]]
- [[raw/Meeting_Notes_GA_Progressives_and_Class_A_Lions_Riches-September-25-2026.md]]
- [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
