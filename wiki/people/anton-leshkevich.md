---
type: person
title: Anton Leshkevich
date: 2025-01-21
aliases: [Anton Leshkevich, Anton, Antoine, Anton Dmishkevich, Дмишкевич, Дмишкевичем, Liashkevich, Anton Liashkevich, Lishkevich, Anton Lishkevich, Лишкевич, Rishkevich, Anton Rishkevich, ришкевич, Vishkevich, вишкевич, брижке]
disambiguation: "Minsk engineer (Omni/RGS), this page. One of THREE Antons (owner-ruled): Anton Leshkevich (Minsk engineer, Omni/RGS; transcript-garble alias "Dmishkevich" → wiki/people/anton-leshkevich.md), Anton Seregin (Minsk payroll / React-TS front-end → wiki/people/anton-seregin.md), Anton (SMM) (Meta-ads contractor, ECHO marketing → wiki/people/anton-smm.md). Resolve by context: Omni/RGS engineering → Leshkevich; front-end/setup UI → Seregin; ad campaigns/SMM → the contractor; queue anything fitting none."
source-count: 31
open-commitments: 4
open-questions: 0
---

# Anton Leshkevich

Anton Leshkevich is a JVL Minsk engineer. He knows the Omni framework and RGS codebases well and acts as a bridge between the Russian-speaking Minsk team and the English-speaking advisers (Aaron, Jason). His surname is given on the Jan 21 continuous-delivery call. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

**Owner ruling (2026-07-13):** distinct from [[wiki/people/anton-seregin.md|Anton Seregin]] (Minsk payroll) — shared given name only — and from the [[wiki/people/anton-smm.md|SMM ad contractor "Anton"]]. (Earlier batches folded "Anton" into the AI-assisted-development topic without a person page; this page splits him out — see [[wiki/topics/ai-assisted-development.md]].)

## Role

- Participated in the Jan 14 AI-assisted-development workshop; his repo access worked throughout and he received an OpenRouter API key. Aaron suggested he try the AI tools on the **RGS** codebase. See [[wiki/topics/ai-assisted-development.md]]. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- On the Jan 21 continuous-delivery architecture call he advocated an MVP approach — start with a simple "Git triggers build" pipeline and trim everything unnecessary. He defined the standalone test tool's three essential blocks (test management, test authoring, test runner). See [[wiki/topics/continuous-delivery-pipeline-architecture.md]]. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- He said he can write the **environment** definition for the Omni framework himself (he used to work with that codebase); noted he recently could not set up the LGS environment because of missing dependencies and had to ask Alexander for help — used as evidence the reproducible-environment approach is worth doing. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- Val repeatedly used Anton as the check on whether an explanation had landed ("Anton, do you understand this?"), positioning him as the team member who must be able to re-tell the plan. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

- **Closest person to Efim's math (late Jan–early Feb):** on the docs-in-Git session Val named him the nearest thing to redundancy on the company's most guarded asset — "I think the closest person right now is Anton Leshkevich" (to [[wiki/people/efim-podvoiski.md|Efim]]'s math work); Aaron's takeaway: then at least one other person can review what Efim commits. See [[wiki/meetings/2025-02-01-docs-in-git-vs-confluence.md]]. [[raw/the_importance_of_storing_artifacts_in_git.md]]

## DevOps container approach for Omni (Mar 24–25 2025, dates inferred)

- On the two-day Miro session he presented the artist-files pipeline, translated between Aaron and Alexander, and supplied the key technical corrections: the framework is a Git repository used as a **submodule** — no release artifact — with **git tags** on master marking versions ("this is framework version 1.2.3"); breaking API changes flow dev-branch→master as the de-facto release. He recalled splitting Omni into repositories with submodules/branches/tags ("я поэтому в Omni пытался разбить на репозитории") and that Omni's current game work (he names "Dragon's Array") links everything into the game directly — no template exists yet. His one-button goal: an ISO image from a manifest of repos+tags, in small per-product iterations. He raised sound-asset validation and designers' Git-friction; took the action to name the pipelines/repos on the board. See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/devops_container_approach_for_omni.md]] [[raw/devops_container_approach_for_omni_3.md]]

## Open commitments

- [ ] Anton — name the pipelines/repos on the Miro board ("these become repos that we can actually point our finger on") — due unspecified — [[raw/devops_container_approach_for_omni.md]]

## History

- **Test-360 progress review (Fri Jul 5 2024, date inferred; pre-window, queued):** owned the first unit-test push on the Omni framework — test environment set up, ~**9%** of the Omni Engine covered using **Jest**, light refactoring (deleting never-executed code found via coverage reports; consulting Alexander Biratka before non-obvious refactors); wrote the first testing requirements (CI/CD on every merge, automated testing in the pipeline, every change linked to a ticket) and emailed them plus Confluence docs to developers for votes; estimated 30–60 calendar days to cover the existing code. He confirmed the RGS codebase already ran the commit-triggered unit-test approach, and that P1000 has no tests ("a historical artifact"). Transcribed once as "Antoine." See [[wiki/topics/test-automation-strategy.md]] (History). [[raw/test-360_progress_review_meeting.md]]
- **JVL Insights (~2023–24):** named **"Anton Leshkevich (Sr. Programmer) - Consultant"** in the JVL Insights knowledge-base proposal — to develop/integrate AI algorithms in **Python**, build front-ends in **JavaScript**, and ensure compatibility with existing **Java** applications. (Note the draft labels him a consultant; 2025 sources treat him as a JVL Minsk engineer — both recorded.) Compensation figures withheld (§15.8). See [[wiki/projects/jvl-insights-knowledge-base.md]]. [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]

## Integration tests for the Calle Ocho Omni port (Apr 15)

- Val on the Omni daily: "Вам в этот разговор еще нужно подтягивать Антона … Саша, вы с Антоном должны вплотную начинать работать, чтобы Антон делал интеграционные тесты" — Anton builds the integration tests for the first Omni game ([[wiki/decisions/2025-04-14-calle-ocho-first-omni-framework-game.md]]). Attribution to Leshkevich by Omni/test-automation context (consistent with his Mar-24 auto-testing role), labeled inference. [[raw/daily_omni_progress-apr-15-2025.md]]

## Apr 16 2025 — trains QA on integration tests (changed decision)

Val changed his earlier plan: rather than Anton writing the integration tests himself, Anton is to **train JVL's QA engineers** to write them ("Я не хочу, чтобы вы сами руками писали эти тесты … начинали учить наших QA-инженеров"). He is to prepare a presentation and run a kickoff meeting with Irina and Pavel — Val offered to attend Friday **6:30 am**. Anton had also been doing the game-history screenshot work on the Omni framework. [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]] See [[wiki/decisions/2025-04-16-replace-testers-with-test-engineers.md]].

## Apr 22 2025 — Calle Ocho feature assignment

On the scheduling session ([[wiki/meetings/2025-04-22-calle-ocho-omni-feature-scheduling.md]]) "Anton" was assigned the game-integration features — **Free Spins (FRAM 664)**, **Mass Engine (FRAM 2)**, **Bonus Game (FRAM 699)** and **Pick Your Fortune Dialog (FRAM 693)** — plus the matrix symbol-sorting under FRAM 478 (~2 days, done before on the online side), run at ~70% so he can also begin QA tests. See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/omni_calle_ocho_scheduling-apr-22-2025.md]]

  - **Identity note — OWNER-CONFIRMED (2026-07-15):** the transcript surname "**Антоном Дмишкевичем / Anton Dmishkevich**" is a **transcription garble**, positively this Anton Leshkevich (not a distinct person). The garble variants are recorded in his aliases so future occurrences auto-resolve. [[raw/omni_calle_ocho_scheduling-apr-22-2025.md]]

## Apr 24 2025 — demos the first Omni integration test; trains QA engineers

On the Omni integration-tests onboarding ([[wiki/meetings/2025-04-24-omni-integration-tests-qa-onboarding.md]]) Anton demoed the **first Omni init-setup integration test** — **Selenium + TypeScript on Node.js** (chosen over Playwright, which was harder to fit into JVL's custom automation framework) — run against a local **LGS docker + LGS-UI** repo via `Yarn Start`. Tests live in the Git repo beside the code, each with a unique key (for future X-Ray integration). Consistent with the [[wiki/decisions/2025-04-16-replace-testers-with-test-engineers.md|Apr-16 decision]] that Anton **trains the QA engineers** to write integration tests rather than writing them himself; Val named him (with [[wiki/people/alexander-biratka.md|Alexander Biratko]]) as a TypeScript-learning source. Detail on [[wiki/topics/test-automation-strategy.md]]. [[raw/integration_tests-apr-24-2025.md]]

## May 5 2025 — the trigger for the feature-granularity conversation

- On the [[wiki/meetings/2025-05-05-feature-granularity-aaron.md|feature-granularity session]], Val used "Anton" as the running example: he was working a **story (LGS196, "Data center UI… leave save mechanism")** under feature **LGS-14 (LGS Configuration GUI)** and had **opened a GitHub branch** on it, but the item was really feature-scale. Val's characterization: Anton "doesn't challenge the authority… knows precisely what to do, but he largely ignores what is written." Aaron used it to argue features must be broken down to demonstrate in ~2 weeks. (Anton by LGS/Omni-engineer context.) Detail on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]. [[raw/feature_granularity_definition_aaron-may-5-2025.md]]

## June 26 2025 — Omni grooming (bonus integration, game history)

On the [[wiki/meetings/2025-06-26-omni-schedule-grooming.md|Omni schedule grooming]] Anton ("Антон"/"Антонио ляшки девич" = Leshkevich) owns the feature **integration** work entirely (bonus, target the 3rd–4th) and the **game history** (LGS side ~done, framework side to finish once scenes exist). Bonus/mass-parser work partly waits on Zhenya's decomposed History. See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. *(Separately, the "Anton" tapped for the Nebraska primary-skill-meter code on June 23 is likely this Anton by context — inference, recorded on [[wiki/projects/nebraska-skill-market.md]], not asserted as a source here.)* [[raw/OMNI_schedule_grooming-june-26-2025.md]]

## July 11 2025 — test-automation 1:1 (pace, the dev-writes-hooks idea, Nebraska work)

On a 1:1 with [[wiki/people/val-levitan.md|Val]] ([[wiki/meetings/2025-07-11-anton-testing-1on1.md]]; Russian) Anton reported test-integration into the game framework is **~70–80% done**; the **test-infrastructure** question (a configurable data-center per product/setting) is still open, with **Zhenya** to add the LSS hooks and Anton the test-framework interface — but it is **not top priority** given his workload. He and Val agreed covering all of Omni with tests at the current pace is **"years, not a year"** — unrealistic, and "you can't solve it with more people" because new hires would need training on JVL's game specifics. Anton's proposal (the core idea): the **developer who adds a new feature should also add its test hooks**, shrinking the chain from **three links** (developer → hook-writer → tester) to **two**, via a **plugin-per-feature** design so testers can drive each new bonus/feature from their side. His own current work: the **22 Nebraska skill games** (one done, one ~80%) and a **bonus rework after the math changed**. See [[wiki/topics/test-automation-strategy.md]]. [[raw/update_anton-july-11-2025.md]]

- **Irina Makarych = game developer (corroboration).** Val listed the people who write game-level implementation code as "**Irina Makarych**, or you [Anton], or Metelski — those three" (plus Igor and Alexander on the framework) — consistent with the owner ruling that the game-dev "Irina" is [[wiki/people/irina-makarych.md|Makarych]] (distinct from QA director [[wiki/people/irina-shishko.md|Irina Shishko]]). [[raw/update_anton-july-11-2025.md]]

## Aug 7 2025 — Fiery Ice code-side progressive check + simulator UI (+ ≈Aug-8)

On the [[wiki/meetings/2025-08-07-player-behavior-simulator.md|Aug-7 Player Behavior Simulator meeting]], at [[wiki/people/michael-gottlieb.md|Michael]]'s request Anton compared the **Diamond Link Deluxe (DLKD)** vs **Fiery Ice** software to see how progressives fire off. His finding: the only code difference is that the framework later added **partial-win progressives**, which **don't qualify in Fiery Ice**, so there's no material difference; he walked through how a progressive win is reported (math engine reports a **base value**, the software then requests the **increment** from the server and adds base + increment). He flagged one **to-check hypothesis** — that increment values might be added multiple times — as worth debugging. He would build the **GUI** for [[wiki/people/efim-podvoiski.md|Efim]]'s Python simulator only if a graphical interface is wanted. [[raw/Player_behavior_simulator.md]] Anton was also present in the smaller [[wiki/meetings/2025-08-08-player-simulator-engineering-discussion.md|≈Aug-8 Val+Efim+Anton session]]. [[raw/player_emulator.md]]

## Aug 27–28 2025 — the spec / tribal-knowledge thread

- **Aug 27 (written Q&A with [[wiki/people/val-levitan.md|Val]] — [[wiki/meetings/2025-08-27-anton-val-spec-tribal-knowledge.md]]).** Anton corroborated Val's premise that a developer cannot code without a spec (even an unwritten in-mind one), so JVL's undocumented specs are **tribal knowledge**. Concrete cost he gave: on the **NAD** project he unknowingly re-wrote code that already existed because a **math-engine-message** sub-module lacked docs after **Valentin** left, and he chose not to risk extending the critical existing code without documentation. He agreed his "going away to think HOW" is itself an in-mind spec, and that recording him explaining the HOW to **Biratka** and having AI format it would reach a usable first-draft spec over a few iterations. Detail on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]. [[raw/transcript_anton_val_spec-august-27-2025.md]]
- **Aug 28 (recording with [[wiki/people/alexander-biratka.md|Biratka]], 1:02 PM — [[wiki/meetings/2025-08-28-omni-animation-architecture-biratka.md]]).** Anton executed the method: he opened the call by saying it was **being recorded to generate a technical specification**, then had Biratka explain Omni's animation architecture (Spine/video/Unity-native animations, the Unity→JSON exporter, spinner elements, the animation-controller state machine and its transition events). Substance on [[wiki/topics/omni-core-advancement-and-game-templating.md]]. (Filename spells him "Liashkevich" — a transcription variant of Leshkevich, added to aliases.) [[raw/Anton_Liashkevich_Alexander_Biratko_about_OMNI-august-28-2025.md]]

## Feb 12 2026 — shader feasibility; inheriting Igor Metelski's South Dakota work

On the [[wiki/meetings/2026-02-12-game-development-review.md|Feb-12 review]] (segment 1) Anton was called in for the liquid-glass **shader question**: custom shaders are **not used in H Studio**, but were possible in the online/"big CGS" engine (he once wrote a symbol-shadow shader) — though a glass-refraction shader is far more complex; he couldn't say for Omni ("ask Alexander"). See [[wiki/topics/slot-game-design-principles.md]] (Feb-12). Separately, with [[wiki/people/igor-metelski.md|Igor Metelski]] away ~2 months, **Anton is to scope inheriting Igor's South Dakota assignments** — he needs 2–3 days to size the work, and (with Pavel/Irina) plans to reach Igor to learn where he stopped. [[raw/Game_Development-February-12-2026-1.md]]

## May 12 2026 — first internal "user" of the NOVA platform

On the founding NOVA architecture session ([[wiki/meetings/2026-05-12-nova-platform-architecture-overview.md]]) Anton was present through both segments and cast as **the first internal user of NOVA** — his test framework (TS-360) consumes the platform's hooks, APIs, and hardware-service interfaces. Under the use-case → requirement → capability governance model, Anton declares capability needs ("I need capability X") to Chief Architect [[wiki/people/alexander-biratka.md|Sasha]], who translates them into features; without that demand signal the architect has no client, and [[wiki/people/alexei-khamin.md|Kamin]] is Anton's own downstream customer. In the design debate he **supported Unix sockets** for service↔LGS communication, raised the games-on-disk question (resolved to packaged archives, not Docker), and suggested a consolidated repo for the hard services — which Sasha overruled in favour of per-service repos. Substance on [[wiki/topics/nova-platform-architecture.md]]. §15.8 clear. [[raw/Meeting_Transcript_nova_platform_architecture_overview-Segment_2-May-12-2026.md]] [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_2-May-12-2026.md]]

## Aug 18 2026 — Rust peripheral services (printer service + build validator)

On the [[wiki/meetings/2026-08-18-rage-nova-migration-experiment-review.md|Aug-18 RAGE→NOVA review]] Pavel reported that Anton (transcript "Антон лишкевич" / **Anton Lishkevich** — another garble of Leshkevich, added to aliases) **took the printer service and the build validator and rewrote them in Rust**, and tested the printer (tickets print on Gen2/Gen5; he lacks an Epic unit to test that one). This is early evidence NOVA's per-service Rust migration is moving faster than expected. Val asked Pavel to send him the services. See [[wiki/topics/nova-platform-architecture.md]] (Aug-18). [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]] [[raw/Meeting_Notes_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]

## Aug 28 2026 — assigned the parallel second Rage→NOVA game port (a line game)

At the [[wiki/meetings/2026-08-28-dragon-pays-nova-conversion-review.md|Aug-28 Dragon Pays review]] (Anton **not present**) [[wiki/people/pavel.md|Pavel]] proposed taking a second game onto NOVA so the two could later be joined behind a game-select screen, and named Anton as the person with the capacity: "Сейчас Антон лишкевич не занят на 100%, то есть я ему там давал задачи, которые там на раз переписать, а вот ему дать в параллель с тем, что он делает вот какуюто ещё одну игру." Val agreed and pushed it further — if he is free, port it straight to NOVA rather than doing anything on the old platform: "Все переводить, как будто мы мы решили и идем вперед." The ruling is [[wiki/decisions/2026-08-28-reverse-engineer-acceptance-criteria-and-automate-qa-dragon-pays.md]]. [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]

- **Which game: a line game, not keno.** [[wiki/people/irina-shishko.md|Irina]] asked that the second game also be a line game "не кена" (not keno); Val agreed — "я бы сейчас я бы делал бы лайн с геймс" — noting keno will get converted eventually either way, and that Anton has already done keno ("вишкевич сделал кино"). [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- **He inherits Igor's groundwork, and is expected to add to it.** Pavel: "те наработки, которые Игорь сделал их какимто образом передать Антону." Val treated that as a feature rather than overhead — "Антон внесет свои новшества еще в то, что Игорь сделал… а потом поделиться ещё раз опытом. У нас тогда будет хорецкие метельские вишкевич" — putting Anton alongside [[wiki/people/evgeny-kharetski.md|Kharetski]] and [[wiki/people/igor-metelski.md|Metelski]] as the three people who will carry the conversion knowledge. [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]

## Sept 3 2026 — his Rust modules each need prose, a capability and a contract; he takes the device-side contracts

At the [[wiki/meetings/2026-09-03-nova-prose-standard-skills-and-module-contracts.md|Sept-3 prose/contracts follow-up]] (Anton **not present**; transcribed "Антон ришкевич" and "Антона брижке" — two further garbles of Leshkevich, added to aliases). [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

- **His Rust modules are the unit of the next block of work.** Pavel: "есть модули, которые Антон ришкевич писал вот на[ ра]сте. Для каждого из этих репозито[риев] нам надо сейчас пройти и создать[:] проза плюс capobility. И вместе с этим создать для… этого модуля контракт." Count: "Наверное 5 или 6 на данный момент," after which "этих 5[–]6 компонентов надо будет уже встраивать в интеграционн[ый] репозитори[й] и сборки игры." Val: "это является ядром следующего [undertaking]." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **[[wiki/people/evgeny-kharetski.md|Evgeny]] assigned him the device-side contracts and called it the easy part** — "он контракт… напишет… это самое лёгкая часть… он это сделает, да, без проблем и лучше это ему делать" — with Evgeny taking the LGS side himself: "Антон, сделай там со своей стороны[,] с[о] стороны девайсов." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He was also floated for the games-side contracts** (Irina: "либо Антон, либо… Игорь… да Данил"), which was not settled. See [[wiki/decisions/2026-09-03-module-contracts-and-nova-integration-repository.md]]. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **Val expanded the next day's (Sept 4) meeting to include him**, alongside Vladimir, Evgeny and a "Dima": "я расширил этот митинг. Я ещё пригласил диму и Антона брижке[вича]." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Open commitments (Aug 28 – Sept 3 2026)

- [ ] [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] — port a second (line) game from Rage/South Dakota to NOVA in parallel, building on Igor Metelski's converter work, so the multi-game game-select screen can be tested — due unspecified (parallel to Igor's QA experiment) — [[raw/Meeting_Notes_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]] [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- [ ] Write prose + a capability + a contract for each of his 5 or 6 Rust device modules — due the two-week milestone from Sept 3 2026 — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]] [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Sept 4 2026 — a scene-validation tool, and the technology-stack objection nobody else was making

At the [[wiki/meetings/2026-09-04-rage-nova-conversion-readiness.md|Sept-4 morning meeting]] Anton did two things: showed a tool he had built and raised the one structural objection in the room [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]].

- **The scene-validation tool.** Reading Igor's port notes he picked out two large gaps — launching a game from LGS with maths, and scene validation after conversion, which today only checks that a file exists ("просто проверяется наличие файла"). His tool "использует омни[ и] непосредственно загружает сцену в память", runs under Linux and Windows, validates scenes from the command line, and could be incorporated into an asset-migration pipeline. He described it as an evolution of a tool Sasha began "пару лет назад" and finished it to "какого[-]то плюс[-]минус рабочего состояния" that week, then asked whether it was wanted at all — "насколько нам нужна такая т[ула] и… насколько я[м] будут пользоваться люди?" The answers were positive from Pavel (Claude can use it), Alexander Biratko (designers can view scenes in the new engine; and could it do automatic screenshot comparison?) and Igor (very useful for a human; Claude can work without it, but it would have helped greatly on Calle Ocho). Detail on [[wiki/topics/test-automation-strategy.md]] (Sept-4). [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **His rationale for it: break the long port cycle into atomic sub-tasks.** "весь цикл порта это ресурсы, код[,] потом вот эти проблемы с LGS и математикой[,] и тогда можно запустить что то посмотреть, то есть цикл достаточно длинный, а в этом случае можно… сначала сфокусироваться на ас[с]ета[х]… потом перейти к коду… задача немножко дробится на более атомарные подзадачи." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **The technology-stack objection.** He argued JVL is repeating the Rage mistake by building on a custom browser-based stack that will age out, and would prefer a compiled application. He had surveyed alternatives — Unity, Unreal (royalty terms he quoted from memory), and free engines generally — and named the maintenance cost of reviving JVL's OGRE-based engine. The exchange, and Val closing it, is on [[wiki/decisions/2026-09-04-browser-pixi-stack-concern-closed.md]]. He accepted the close: "Пожалуй, да пока пока." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **His unaddressed second point:** that optimising the AI's own cost is part of the job — "наша задача это оптимизировать его работу и сделать так, чтобы он работал дешевле[,] сжо[г] не так много токенов." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **His Rust work is already landing.** Val, listing evidence that October 1 has effectively started, was told by Irina that Anton wrote "навигатор[,] принтер" in Rust, and Alexander Biratko added that the printer library is already being integrated into Flex-Pay. [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]

## Open commitments (Sept 4 2026)

- [ ] Continue the scene-validation tool; the screenshot-comparison extension Alexander Biratko proposed is wanted but unscheduled — due unspecified — [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]

## Sept 14 2026 — confirmed as a builder of both the Nebraska/Texas games and the last Georgia COAM

Anton was pulled into the [[wiki/meetings/2026-09-14-texas-vertical-conversion-and-georgia-game-base.md|Sept-14 6:38 AM ET session]] (Russian) because Val expected the Texas conversion to need him; in the event he spoke little, and Val apologised for the early start — "я извиняюсь, я вас поднял рано утром" — to which he answered "Ничего страшного." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]] [[raw/Meeting_Notes_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

- **He worked on the Nebraska product on RAGE.** Val: "Антон, вы занимались техасом, да? Ну небраской… На реййд[,] да." Anton: "Когда-то давно мне кажется да" and "Техаса наверное уже нет, но [не]брас[кой] точно занимался." [[wiki/people/irina-shishko.md|Irina]] then said "Техас из небраски" and Val confirmed the two are the same thing. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **He built the last Georgia COAM jointly with [[wiki/people/igor-metelski.md|Igor Metelski]]** — Igor, asked who did it: "Мы вдвоём с Антоном." That matters here because those Georgia games are the donor set for the vertical Texas route ([[wiki/decisions/2026-09-14-vertical-texas-starts-from-the-georgia-coam-vertical-games.md]]). [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **Asked by Irina to recall whether that product carries a mystery progressive**, his replies are garbled in the recording and no answer is recoverable; recorded as unclear rather than guessed. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

*(§4: this is Anton Leshkevich by context — Minsk engineer, RAGE/Omni game work with Igor Metelski — not [[wiki/people/anton-seregin.md|Anton Seregin]] or the SMM contractor.)*

**§15.8:** clear — engineering content only.

## Sources

- [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

- [[raw/Meeting_Notes_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- [[raw/Meeting_Transcript_nova_platform_architecture_overview-Segment_2-May-12-2026.md]]
- [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_2-May-12-2026.md]]
- [[raw/Game_Development-February-12-2026-1.md]]
- [[raw/transcript_anton_val_spec-august-27-2025.md]]
- [[raw/Anton_Liashkevich_Alexander_Biratko_about_OMNI-august-28-2025.md]]
- [[raw/update_anton-july-11-2025.md]]
- [[raw/OMNI_schedule_grooming-june-26-2025.md]]
- [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- [[raw/feature_granularity_definition_aaron-may-5-2025.md]]
- [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- [[raw/the_importance_of_storing_artifacts_in_git.md]]
- [[raw/devops_container_approach_for_omni.md]]
- [[raw/devops_container_approach_for_omni_3.md]]
- [[raw/test-360_progress_review_meeting.md]]
- [[raw/daily_omni_progress-apr-15-2025.md]]
- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- [[raw/omni_calle_ocho_scheduling-apr-22-2025.md]]
- [[raw/integration_tests-apr-24-2025.md]]
- [[raw/Player_behavior_simulator.md]]
- [[raw/player_emulator.md]]
- [[raw/Meeting_Notes_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
