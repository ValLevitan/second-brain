---
type: person
title: Irina Shishko
date: 2025-05-01
aliases: [Irina Shishko, Irina Shyshko, Iryna Shyshko, Irina Shishkova, Ирина Шишко]
disambiguation: "Vice Director of Engineering & Director of QA (owner-confirmed 2026-07-18), this page. Two Irinas (owner-confirmed 2026-07-18, genuinely two people): [[wiki/people/irina-shishko.md|Irina Shishko]] = Vice Director of Engineering + Director of QA (engineering management, QA, testing; = payroll Shyshko Iryna); [[wiki/people/irina-makarych.md|Iryna Makarych]] = game developer. Resolve by context: engineering-management / QA / testing / test-plans → Shishko; game development → Makarych; queue if genuinely unclear."Irina" mentions are genuinely ambiguous — queue rather than force. Owner to confirm the distinction or fold into one cluster."
source-count: 83
open-commitments: 16
---

# Irina Shishko

Irina Shishko is JVL's **Vice Director of Engineering and Director of QA** (owner-confirmed 2026-07-18) on the Minsk side — the person who runs QA/test engineering, owns the test process, and interprets meter/SAS certification behaviour. She reconciles to the Minsk-payroll name **"Shyshko Iryna"** (see [[wiki/topics/minsk-staff-roster.md]]). She is distinct from [[wiki/people/irina-makarych.md|Irina Makarych]] (game developer).

> **Re-attribution note (owner ruling 2026-07-18).** The owner confirmed there are genuinely two Irinas and that all engineering-management / QA / testing / test-plan / test-framework / meter-and-SAS-certification-interpretation "Irina" mentions are **Shishko**, not Makarych. Many such mentions were routed to Makarych in earlier batches and have been moved here. Rule: QA / testing / engineering-management → Shishko; game development → Makarych.

## Workshop / engineering resourcing (May 1)

- On the May-1 dispensing-tower design call, [[wiki/people/val-levitan.md|Val]] told [[wiki/people/genadi-peari.md|Genadi]] that to get the Minsk workshop to prepare a working station for [[wiki/people/evgeniy-alekseev.md|Evgeny]] (machines, printers, bill acceptors, spare parts) the person to contact is Irina Shishko — describing her as the one who "**глотку перегрызет и сделает что нужно**" (will bite through throats and get it done), in contrast to the helpful-but-passive [[wiki/people/alexei-khamin.md|Khamin]]. Consistent with a Vice Director of Engineering who marshals engineering resources. [[raw/flex_tower_spacial_design_review-may-1-2025.md]]

## QA / test-engineering arc

- **Test-process enforcement (Test-360 review, Jul 2024, date inferred).** Val named "Irina" as the person who would have to enforce the test process "with an iron fist," predicting she "will adapt a binary decision that we make without really opining on it" once Alexander and Anton set the rule. (re-attributed per owner ruling 2026-07-18: QA/engineering → Shishko) [[raw/test-360_progress_review_meeting.md]]
- **Test architecture (Jan 15).** The test-automation consultant proposed she attend the upcoming testing-architecture meeting alongside Pavel, Anton and Aaron; Val wanted to "nail the architecture of testing" first via that ~2-hour meeting. [[raw/integration_and_testing_procedures_january_15_2025.md]]
- **QA verification of a new tool (Feb 21).** Val wanted QA ("Ivan or Irina") to go through and verify the brand-new Miranda↔math play-test tool, since it is a different product from the shipping game. [[raw/game_design_meeting_february_21_2025.md]]
- **"No test, no pull" (Apr 3).** Val invited "Ирина" to the GitHub/Jira structure lecture precisely because a feature must be testable — when a feature opens she reads it and says "I will test it this way, and I can write an automatic test." His goal: the engineers under her write the tests themselves, run in the pull into main. See [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]. [[raw/github_jira_setup-april-3-2025.md]]
- **Drive the test cases (Apr 14).** On the Omni framework MVP review Val told "Ирина" to push "нагло и беспощадно" for how it works so she can develop the tests; a feature can't ship without integration tests, and she "должна проверять тестами." See [[wiki/meetings/2025-04-14-omni-framework-mvp-calle-ocho.md]] and [[wiki/decisions/2025-04-14-calle-ocho-first-omni-framework-game.md]]. [[raw/omni_progress-april-14-2025.md]]
- **Replace testers with test engineers (Apr 16).** When Val announced JVL will replace manual testers with Test Engineers, "Ирина" confirmed she already has "3-4" (then "пять") new people ready to bring in "даже завтра," and is to co-run the Friday 6:30 am QA integration-test training kickoff with Anton and Pavel. See [[wiki/decisions/2025-04-16-replace-testers-with-test-engineers.md]]. [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- **QA-engineer onboarding (Apr 24).** On the integration-tests kickoff, her job was framed as raising the QA engineers "на этот уровень с девелоперами"; the team could talk directly with Anton, Irina and Pavel. She described the test-case↔mock-up-code model. See [[wiki/meetings/2025-04-24-omni-integration-tests-qa-onboarding.md]]. [[raw/integration_tests-apr-24-2025.md]] [[raw/ci_cd_qa_structure-apr-24-2025.md]]
- **Setup-screens settings verification (Apr 24).** On the Omni setup-screens/June-scope review, "Ирина права — все, что нужно делать, это проверить варианты" (verify the setting variants for Calle Ocho). Testing/verification of settings. See [[wiki/meetings/2025-04-24-omni-setup-screens-june-scope.md]]. [[raw/set_up_screen_omni-apr-24-2025.md]]
- **Test-status reality check (May 14).** After the schedule crew left, Val continued the Omni test-status segment "с Ириной" (and Pasha) — a candid check on where Omni testing actually stands. See [[wiki/topics/test-automation-strategy.md]]. [[raw/omni_test_status_review-may-14-2025.md]]
- **Writing tests in small fragments (May 16).** On the FlexPay commissioning call Irina was named a proactive-information recipient and told that when she starts writing all the tests, "вам нужно писать в очень маленьких фрагментах." [[raw/commission_flex-pay-may-16-2025.md]]
- **FlexPay/FlexPort test plan (May 20).** Chaired by Val with QA lead "Ира," she argued (Val agreed) that FlexPay and FlexPort don't work standalone — testing must cover the whole chain — and walked the test-case/test-plan state; the split-into-separate-plans direction was set. See [[wiki/meetings/2025-05-20-flexpay-flexport-test-plan.md]]. [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]
- **First Selenium/web tests demoed (May 21).** "Это говорит Ирина Шишко" wrote two working tests on the init-setup configuration page (footer buttons; language button launching a new page), inside Anton's POM + LGS-abstraction framework. See [[wiki/meetings/2025-05-21-test-engineering-progress.md]]. [[raw/test_engineering_progress_report-may-21-2025.md]]
- **Jira-plans maturity (May 29).** As QA lead she confirmed the QA team had no Jira tasks for its TypeScript work yet and worked through the X-Ray-test-cases-in-Jira ↔ test-code-in-GitHub model; "Irina could be having her QA team investigate something," and a setup-screen example (toggle a switch → Irina writes the test) illustrated the cadence. See [[wiki/meetings/2025-05-29-jira-plans-maturity.md]]. [[raw/jira_plans_maturity-mat-29-2025.md]]
- **FlexPay QA plan (May 30).** As QA lead ("Ира") she walked the X-Ray test-plan structure — test cases in the FlexPayment project, QRM for test docs/releases, three plans (FlexPort 8 cases, FlexPay 27+, combined) that must pass to certify the e-Wallet variant. See [[wiki/meetings/2025-05-30-qa-flexport-flexpay-plan.md]]. [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]
- **QA-engineering demo to Aaron (June 12).** The QA engineer who demoed the in-house OmniTest360 TypeScript framework (Jira test cases linked to auto tests by shared ID, results into X-Ray) — "Irina." Consistent with the May-21 demo. See [[wiki/meetings/2025-06-12-qa-engineering-direction-aaron.md]]. [[raw/qa_engineering_direction_review_aaron-june-12-2025.md]]
- **Director of QA / priority contact (June 12).** On the games-design priorities review Val described her: "all the QA people work under her… very organized… a bulldozer type of attitude," "programming now as well," and the priority contact for product priorities. (The transcript renders the surname "Makarych" here, but the described role — Director of QA, all QA under her — is Shishko per the owner ruling.) See [[wiki/topics/test-automation-strategy.md]], [[wiki/projects/south-dakota-vlt-market.md]]. [[raw/games_design-june-12-2025.md]]

## SAS meter / certification-interpretation arc

- **Printer testing (Jan 22).** On the South Dakota recap the FutureLogic Gen 2 printer was said to have been tested "per Pavel and Irina." See [[wiki/projects/south-dakota-vlt-market.md]]. [[raw/sd_vlt_recap-jan-22-2025.md]]
- **Outstanding-subjects alignment (Feb 19).** "Irina" confirmed the printer testing status ("it's working" on the last build given to Juan), reviewed the **Bally iview** logs for the Georgia Peach1234 work (JVL sends the correct data but Bally's final report is wrong), and prepares the **diffs document** for GLI — QA/certification/release work Val praised as essential. See [[wiki/projects/georgia-market-rollout.md]] and [[wiki/projects/south-dakota-vlt-market.md]]. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- **SAS 51/52 hand-pay (Apr 14).** "Irina" (software, translated by Pavel) explained JVL always submitted the hand-pay conditions as "not applicable" for Georgia; the concrete bug: the machine issues 51 but never sends 52 and keeps re-sending 51. Meter/certification-test interpretation. See [[wiki/meetings/2025-04-14-sas-51-52-georgia-coam-interpretation.md]]. [[raw/sas_51_52_requirement_interpretation-april-14-2025.md]]
- **SAS 51/52 resolution (Apr 24).** Follow-up after Eclipse flagged JVL's "Peach One" submission; resolution to supply two RIS files plus a hand-pay software fix. See [[wiki/meetings/2025-04-24-ga-coam-sas-51-52-eclipse-resolution.md]]. [[raw/ga-coam_error_51_52-apr-24-2025.md]]
- **Class-3 meters "two steps back" (May 21).** As QA lead she raised — and Val had privately shared — the deeper doubt that even JVL's Class-3 meters may be interpreted incorrectly; the group agreed to redefine/verify the Class-3 meters against the protocol first. See [[wiki/meetings/2025-05-21-ga-coam-class3-meters-seminole-retest.md]]. [[raw/sas_intricacies_ga-coam-may-21-2025.md]]
- **Jackpot / Class-3 constitution (May 28).** On the jackpot-treatment call the transcript's attendee line names "Irina Shishko"; she is in a jackpot-meter/QA-interpretation role, and Val asked Irina and Pavel to think the ruling over. (Owner-confirmed 2026-07-18: meter/QA interpretation → Shishko.) See [[wiki/meetings/2025-05-28-jp-jackpot-class3-georgia-coam.md]] and [[wiki/decisions/2025-05-28-class3-meters-constitution-georgia-parallel-logic.md]]. [[raw/jp_treatment-may-28-2025.md]]
- **Key-to-meter scope gaps (June 10).** "Irina" defended the key-to-meter-limit-as-forced-lower-than-jackpot-limit as correct; Val/Juan ruled it a scope gap (the two must be independent values). Meter/SAS interpretation. See [[wiki/meetings/2025-06-10-jackpot-meter-sas-scope-gaps.md]]. [[raw/meter_sas_function-june-10-2025.md]]
- **Jackpot/meter flowchart (June 12).** "Irina" walked Vlad's future-state flowchart of Class-3 jackpot / key-to-meter behaviour. (Owner-confirmed 2026-07-18: meter interpretation → Shishko.) See [[wiki/meetings/2025-06-12-jackpot-meter-flowchart-review.md]]. [[raw/jp_meters-june-12-2025.md]]
- **Class-3 meter tests (June 17).** "Irina" translated Vlad's Class-3 SAS meter test results; per her instruction the casino could not run test 3 (remote hand-pay clearing disabled for security). See [[wiki/meetings/2025-06-17-class3-meters-georgia-qam-flow.md]]. [[raw/Metering_class_3-june-17-2025.md]]

## FlexPay / e-Wallet QA & release process

- **First on the dev review (May 27).** From QA, "Irina Shishko" joined the FlexPay/FlexPort dev review for the first time; QA is to file FlexPay/FlexPort bugs in Jira with concrete version references. She also attended the same-day e-wallet release-planning session. See [[wiki/meetings/2025-05-27-flexpay-flexport-dev-review.md]] and [[wiki/meetings/2025-05-27-ewallet-release-planning.md]]. [[raw/dev_review_flex-pay_flex-port-may-27-2025.md]] [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- **e-Wallet / TITO action-list (May 29).** "Ирина Шишко" raised correct firmware-version naming, **test-vs-production folders** on GitHub, and using a sub-version number instead of a build number — a QA/release-process role. See [[wiki/meetings/2025-05-29-ewallet-tito-flexpay-implementation.md]]. [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]
- **Progress review (June 2).** Named on the recurring action-list review (e-Wallet rollout to testing, FlexPay→GitHub migration and versioning, the e-Wallet live-test cycle). See [[wiki/meetings/2025-06-02-flexpay-flexport-progress-review.md]]. [[raw/flex-pay_flex-port_progress_review-june-2-2025.md]]

## ~July 15 2025 — alignment-planning catch-up (QA/release-process voice)

- On the [[wiki/meetings/2025-07-15-alignment-planning-catch-up.md|mid-July alignment-planning catch-up]] (with Val + [[wiki/people/pavel.md|Pavel Frolov]]), Irina Shishko surfaced the **Salt-Corp certification lesson** — JVL had casually swapped software changes into a build the operator ("Larry Corporation" / a Latvia location) was certifying, so the operator pulled its approval and the **training slipped ~3 weeks**; her point was that JVL must feed operators **more complete information up front** about what's being approved. She also flagged the HHR schedule slipping to **September** ("pessimistically") given Nebraska progressive/At-Any-Bet work still outstanding, and named **Irina Makarych** as a possible builder of the math emulator. See [[wiki/topics/omni-core-advancement-and-game-templating.md]] and [[wiki/topics/slot-game-design-principles.md]]. [[raw/alignment-planning-catch-up.md]]

## July 28 2025 — online-games interactive-bonus confirmation

- On the [[wiki/meetings/2025-07-28-media-tax-credit-examiner-coaching.md|Media Tax Credit coaching call]] Irina Shishko ("Irina Shishkova") is named as the authority Lena/JVL **confirmed with** that the special land-based golden-frame interactive bonus was **never implemented in the online games** (designed and math'd, but never deployed). See [[wiki/topics/ontario-media-tax-credit.md]]. [[raw/media_tax_credit_team_coaching-july-28-2025.md]]

## Nov 3 2025 — production-QC process (Georgia machine release)

On the [[wiki/meetings/2025-11-03-machine-qc-checklist-release-form.md|Nov-3 QC meeting]] (with Val + [[wiki/people/genadi-peari.md|Genadi Peari]]) Irina took the production-QC/inspection angle on the loose-speaker defect — the physical verification that everything screwed-in is actually done, whether ports can be tested without devices, and how a visual sub-assembly inspection would have caught the loose speaker. She co-owns (with Genadi) the undertaking to compile the list of missing QC steps/documents/tools by process stage. Consistent with her engineering-management / QA role. See [[wiki/topics/slot-machine-production-test-procedure.md]] (Nov-3). [[raw/Machine Quality Control Checklist and a Release form.md]]

## Nov 5–10 2025 — QA on the payment-hub ACH module

Across the three ~7 AM ACH-module spec-review sessions Irina is the QA/test-engineering voice (with QA engineer [[wiki/people/alexei-khamin.md|Alexei Khamin]]): she pressed how invoice state changes would be tested, how test data (accounts/locations/cards) would be generated, and the need for a **state-machine diagram** so QA can point to a state and emulate it. On Nov-5 she and Alexei were asked to specify the **testing-hook requirements** for verifying invoice state transitions. Consistent with her Director-of-QA role. Substance on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Nov 5–10 ACH-spec arc). [[raw/Payment HUB_ACH module specification_05.11.25 .md]] [[raw/Payment HUB_ACH module specification_10.11.25.md]]

## Nov 11 2025 — graphics-specification for automated testing

On the Nov-11 graphics-spec call (with Val + [[wiki/people/pavel.md|Pavel Frolov]]) Irina drove the QA angle: to test a game's on-screen layout automatically she needs each component's **coordinates, size and label** plus a **reference ("эталон") screenshot** to pixel-compare against — the information the art team ([[wiki/people/lena.md|Lena]]) has not been delivering in a usable form. She and Pavel worked out that the reference will come from [[wiki/people/dmitriy-khandov.md|Dima Khandov]]'s **Miranda scene-manifest export**, and that each manifest must be verified once against a correct game before it becomes the regression reference. Consistent with her Director-of-QA role. See [[wiki/topics/game-art-animation-production-pipeline.md]] (Nov-11). [[raw/Specs_graphics.md]]

## Feb 3–4 2026 — Claude-assisted test-planning (figma → Jira → autotests)

- **Feb 3 (Claude Code workshop).** On the [[wiki/meetings/2026-02-03-claude-code-integration-continued.md|Feb-3 session]] Irina described her own Claude workflow for the setup screens: she had **Claude analyse the Figma prototypes** — rather than pulling them apart by hand, Claude **extracted the sections/divisions** from the prototypes — then Claude advised her to **create features and stories in Jira for writing the autotests**, and she created the stories in Jira (e.g. for the setup sections) and assigned owners/deadlines. Aaron framed her as the "test director" who must identify her data sources (Figma prototype, API contracts, Jira test management, the React repo). See [[wiki/topics/ai-assisted-development.md]] (Feb-3). [[raw/Claude Code integration - continued.md]]
- **Feb 4 (figma→React QA point).** On the [[wiki/meetings/2026-02-04-figma-react-export-workflow.md|Feb-4 figma→React session]] Irina pressed the QA-entry question — "at what point do we enter, and what do we write tests on?" — and synthesised the answer: the setup = **Figma screens + per-screen requirement/acceptance-criteria descriptions**; tests are written to those screen-level acceptance criteria; once Figma → React → server → back-end renders the final result, the automated runner executes the test. See [[wiki/topics/test-automation-strategy.md]] (Feb-4). [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]

## Open commitments

- [ ] Irina Shishko (with Alexei Khamin) — specify the QA testing-hook requirements for verifying invoice state changes in the payment-hub ACH module — due unspecified — [[raw/Payment HUB_ACH module specification_05.11.25 .md]]

## Feb 6 2026 — attended the UI/Claude-Code session

On the [[wiki/meetings/2026-02-06-ui-claude-code-adaptation.md|Feb-6 UI/Claude-Code session]] Irina attended; Val observed she was "a little bit struggling" with the pace/English and suggested the team **huddle and go over it together afterward** (noting Evgeny Kharetski "gets everything"). See [[wiki/topics/ai-assisted-development.md]] (Feb 6). [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]

## Feb 27 2026 — Nebraska release-schedule call (QA/testing + attendant-screen screenshots)

On the [[wiki/meetings/2026-02-27-nebraska-release-schedule.md|Feb-27 1:02pm Nebraska schedule call]] (with Val, Juan, [[wiki/people/pavel.md|Pavel Frolov]]) Irina Shishko took the QA/testing and UI-reference role on the three Nebraska requirements. [[raw/Schedule_Nebraska-February-27-2026.md]]

- She is the one who **has to test** the whole-dollar-rounding behaviour (REQ-1007), so Val ruled Juan must describe the operation — including the last-bet/risk feature — until **Irina** understands it; she asked for the risk behaviour to be added to the requirement description. She confirmed the period-meter-clearing already exists for the audit ticket (REQ-998) and undertook to **supply screenshots of the existing attendant screens** so Juan/Pavel can design where the manual audit-ticket print button appears. Consistent with her Director-of-QA / certification-interpretation role. See [[wiki/projects/nebraska-skill-market.md]] (Feb-27). [[raw/Schedule_Nebraska-February-27-2026.md]]

## Mar 4 2026 — schedule review (QA voice on the Jira↔GitHub workflow)

On the [[wiki/meetings/2026-03-04-schedule-review.md|Mar-4 schedule review]] (with Val and [[wiki/people/pavel.md|Pavel Frolov]]) Irina Shishko participated in the Jira-workflow discussion — questioning the **purpose and timing of the proposed GitHub-branch field** on features (when it should appear — at first commit vs before development) and drawing the analogy to how commit↔Jira linking worked under the old SVN setup. See [[wiki/topics/github-release-management-pipeline.md]] (Mar-4). [[raw/Schedule_review-March-4-2026.md]]

## Mar 5 2026 — Nebraska release schedule review (QA/testing voice)

On the [[wiki/meetings/2026-03-05-nebraska-schedule-review.md|Mar-5 4:13pm Nebraska schedule review]] (Russian; with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/pavel.md|Pavel Frolov]], who left partway) Irina Shishko walked Val through where each Nebraska feature sits in JIRA and who owns it, and gave the QA/testing read on the two remaining big features. She stressed that the **audit ticket** (REQ-998) can't be treated as "just check a button" because **every printer handles the audit/print ticket differently**, so the auditing must be exercised across all printers (she framed the broader test as hers, with [[wiki/people/ivan.md|Ivan]]), and she asked for the **whole-dollar-rounding + risk feature** (REQ-1007) behaviour to be spelled out. Consistent with her Director-of-QA / certification-interpretation role. See [[wiki/projects/nebraska-skill-market.md]] (Mar-5). [[raw/Schedule_review_Nebraska-March-5-2026.md]]

## Mar 26 2026 — Initiative Priority Schedule (release/test coordination)

On the two-segment [[wiki/meetings/2026-03-26-initiative-priority-schedule.md|Initiative Priority Schedule]] meeting (with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/pavel.md|Pavel Frolov]]) Irina Shishko took the QA/release-management angle: she pressed that fixing the priorities isn't enough — the team must decide **which product versions ship, in what order** — and gave the testing read (a kernel upgrade means re-testing hardware across printers, validators, SAS and games, so ~2 weeks; she also confirmed the setup-mode freeze bug is **not** QR-code-related). She is named for testing coordination and release management, and can ask [[wiki/people/elizabeth.md|Elizabeth]] to do on-site testing once builds are ready. Consistent with her Vice-Director-of-Engineering / Director-of-QA role. See [[wiki/topics/github-release-management-pipeline.md]] (Mar-26). [[raw/Meeting_Transcript_initiative_priority_schedule-1-March-26-2026.md]] [[raw/Meeting_Transcript_initiative_priority_schedule-2-March-26-2026.md]] [[raw/Meeting_Notes_initiative_priority_schedule-March-26-2026.md]]

## Mar 27 2026 — to own the Maple Jira work via Claude (OMNI call; referenced as "Ira")

On the [[wiki/meetings/2026-03-27-omni-architecture-challenge.md|Mar-27 OMNI Architecture Challenge]] call (Val ↔ [[wiki/people/pavel.md|Pavel]]), Val referred to **"Ира"/"Ira"** — resolved here as Irina Shishko by context (engineering/release work alongside Pavel, following the same-day-prior Maple/release thread of [[wiki/meetings/2026-03-26-initiative-priority-schedule.md|Mar-26]]) — who had worked on the **Maple** (Texas refit) rework that morning. Val praised her analysis and directed that **she herself** finish it, **use Claude to create the Jira Features** (going directly to Features), and distribute to all participants for review — explicitly not Pavel and not an automated push by Val. (The "Ira" resolution is by context; if the owner reads it as a different Irina, flag for correction.) Substance on [[wiki/topics/ai-assisted-development.md]] (Mar-27). [[raw/Meeting_Transcript_OMNI_Architecture_Challenge-March-27-2026.md]] [[raw/OMNI_Architecture_Challenge-March-27-2026.md]]

## Apr 15 2026 — Flex POS testing "stopper": the UI graphical layer must land this week

On the [[wiki/meetings/2026-04-15-flex-pos-alpha-and-omni-2-architecture.md|Apr-15 Flex POS Alpha & OMNI 2 alignment]] Irina (QA/release voice) objected forcefully that Flex POS testing is blocked — "we need it now, we cannot test anything, we have a stopper" — because the **UI graphical-layer services aren't deployed** (backend is live on AWS). Val backed her: no weekends in principle, but [[wiki/people/anton-seregin.md|Anton Seregin]] (starting Apr 16, likely Saturday) must finish the UI so end-to-end testing can begin next week. Substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Apr-15). [[raw/Meeting_Notes_Flex_POS_Alpha_and_OMNI_2_Architecture-April-15-2026.md]]

## May 12 2026 — QA use-case author for the NOVA platform

On the founding NOVA architecture session ([[wiki/meetings/2026-05-12-nova-platform-architecture-overview.md]]) Irina's place in the governance model was defined: she **converts existing QA test cases into use cases, then into requirements, then maps them to capabilities** — foundational input for both [[wiki/people/anton-leshkevich.md|Anton]] (test framework) and Chief Architect [[wiki/people/alexander-biratka.md|Sasha]]. In the as-is walkthrough she argued there is **no signage in scope** for this platform (Sasha kept the signage progressive-controller box on the diagram anyway — left unresolved). Substance on [[wiki/topics/nova-platform-architecture.md]]. §15.8 clear. [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_1-May-12-2026.md]] [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_2-May-12-2026.md]]

## Aug 24 2026 — owns the prose catch-up schedule, and reassigns the CMS prose to Sergey Tsimanov

On the [[wiki/meetings/2026-08-24-nova-lgs-prose-standard-checkpoint.md|Aug-24 prose checkpoint]] (Russian) Val handed Irina and [[wiki/people/pavel.md|Pavel]] the sequencing of the prose/capabilities catch-up. [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

- **Val explicitly delegated the schedule to her and Pavel.** "я не буду лезть в ваш следжил, я это оставлю для Ирины с Павлом. Они знают все наши приоритеты" — they know the priorities; the target is that the whole team is caught up by the end of September with clean repo↔Jira linkage. See [[wiki/topics/nova-platform-architecture.md]] (Aug-24). [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **Her estimate of the remaining work:** "нам нужно наверно неделей, и это на проекты. Нужно посмотреть, то есть Владимиру там немножко осталось женя тоже" — about a week, project by project, with Vladimir and Evgeny each nearly done. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **She made the reassignment call on the CMS prose.** After Pavel raised that the prose Val gave [[wiki/people/dmitri-chudinov.md|Dima Chudinov]] needs verifying: "Ну её тогда отдать Сергею. Потому что дима сейчас занят, потом дима в отпуск, а Сергей пускай сейчас этим занимается" — give it to [[wiki/people/sergey-tsymanov.md|Sergey Tsimanov]], because Dima is busy and then on vacation. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **She named the missing artifact precisely.** When Evgeny described the gap, Irina's formulation was "Структура документа с прозой" — the structure of the prose document — which Evgeny confirmed as exactly it. She also corroborated that the docs-folder idea came from an "Андрей" as its initiator (which Andrei is not stated). [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **She backed Pavel's PR-gate over Evgeny's alternative:** "то что Паша сказал." And she framed the reason capability closure matters, raising Vladimir's un-deployed setup work as the case where code exists but the capability cannot close. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **A working constraint she flagged:** she cannot open Claude artifact links without the VPN, but "не хочется в п н включать, потому что тогда плохо работает симс" — the VPN degrades CMS access for her. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Open commitments (Aug 24 2026)

- [ ] With [[wiki/people/pavel.md|Pavel Frolov]]: schedule daily team time to fill in capabilities and open questions against already-written code and drive the whole team to catch up — due end of September 2026 — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [ ] With Pavel: assign [[wiki/people/sergey-tsymanov.md|Sergey Tsimanov]] to write prose and capabilities for the backend/CMS and to verify the prose Val gave Dima Chudinov — due unspecified — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Aug 26 2026 — the 88% RTP catch on the Georgia release, and the Sept-1 readiness call

On the [[wiki/meetings/2026-08-26-alignment-planning-nova-september-releases.md|Aug-26 alignment call]] (Russian) Irina was the one who turned Val's Georgia pricing theory into a concrete release problem. [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

- **She supplied the current Georgia RTP figures and the gap.** "это игры 90, 92, 94 процента плюс 2 процента, либо 2 с половиной процента у прогрессива" — and if JVL wants a lower percentage, "нам, возможно, для игр нужны, например, 88%, которых нет." Her fix: get [[wiki/people/efim-podvoiski.md|Efim]] to finish that percentage "на вот эти 15 игр, где есть, где нету" and only then release. Val agreed and folded it into the release — [[wiki/decisions/2026-08-26-add-88-percent-rtp-option-to-georgia-coam-games.md]]. [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **Her readiness read on both September 1 products:** "оба продукта, они уже достаточно… готовые, то есть там осталось минимально. Да проверять и всё," and "сауз Дакота у нас почти закончена… если ничего не вылезет, то к 1 сентября." Her plan for the added percentage: Efim adds it, it goes on test, "максимум… Следующая неделя будет через неделю." [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **She dated the cabinet Val had photographed in the field.** Against Val's 10-button panel with a 25¢ minimum on every game, Irina identified it as the original Peach — "это пич, который мы 5 лет назад выпускали" — and said the machines were later redone to "5 тире 8 кнопок," also a long time ago. Detail on [[wiki/topics/slot-game-design-principles.md]] (Aug-26). [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **She named the design cost of the two parallel NOVA tracks.** Porting South Dakota needs almost nothing from designers; the Georgia COAM rework does — "Почему я спросила, что новые игры это нужны, будут полностью вовлечены эти дизайнеры?" She also supplied the name of the progressive Val could not recall: "Матч 3". [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **On whether Ivan can replace Juan's push with certifiers: "наверное так 50 на 50 я б сказала."** She distinguished doing the submission from driving it — "Именно так с напором" — and said Juan operates at another level: "он знает, о чём он разговаривает, с кем он разговаривает, что нужно сказать." See [[wiki/people/juan-martinez.md]] (Aug-26). [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **She raised the pre-test question that produced the test-bench decision** — how the coming South Dakota submission gets pre-checked, recalling that last time Lonnie ran JVL through several correction passes before the lab. See [[wiki/decisions/2026-08-26-self-test-on-lw-sas-bench-in-georgia-plus-minsk-emulation.md]]. [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

## Aug 28 2026 — the most optimistic completeness estimate, and the "what we don't have is requirements" point

At the [[wiki/meetings/2026-08-28-dragon-pays-nova-conversion-review.md|Aug-28 Dragon Pays review]] (Russian): [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]

- **She put the port at 95%** where [[wiki/people/pavel.md|Pavel]] said "85 наверное" and [[wiki/people/igor-metelski.md|Igor]] warned of a fair remaining divergence from the Rage games. On the missing risk feature she argued it is not per-game work: "это общая фича для всех игр это на один раз её делаешь и всё." [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- **She named what the QA experiment is actually missing.** Not the prose — "нам нужны Требования с аксептомс критериями. Ну то есть то, чего нет сейчас" — requirements with acceptance criteria do not exist today; code and prose do. Val's answer was to reverse-engineer them back through the overall architecture. See [[wiki/topics/test-automation-strategy.md]] (Aug-28). [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- **She backed Pavel's animation objection** — that frame-accurate behaviour will not appear in requirements either ("И в рекламинт этого не будет") — and asked that the second parallel port be a line game rather than keno. [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]

## Sept 1–3 2026 — the capability-granularity objection, and the acceptance-criteria argument she won

- **Sept 1** ([[wiki/meetings/2026-09-01-nova-prose-qa-automation-check.md|prose/QA check-back]]): she supplied the framing question about whether prose is for the framework or the platform (Val corrected the word to "platform"), proposed bringing Danil in under Sasha's supervision on the games prose, noted that the end-to-end tests Danil had looked at on Calle Ocho were written by Sasha, and pressed Pavel on what AI-managed tests would mean in practice — "что значит[,] писал[?] писал и забывал[?]" She agreed with Val's read that nobody would return to the frozen old tests: "Уже никто туда не пойдёт." [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- **Sept 3 — she rejected the generated capabilities as over-granular.** "то, как сейчас написаны каппобилити… 54[—] это что то очень сильно разбитое. Эт[о] это не копобилити," with worked examples: issuing and reprinting a paper voucher, or redeeming an inserted voucher, are not capabilities. Pavel countered that LGS is genuinely huge; Val's remedy was an administrative direction to Claude — see [[wiki/decisions/2026-09-03-capabilities-consolidated-by-administrative-direction.md]]. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **She won the acceptance-criteria argument against Val.** Against his position that acceptance criteria must fit narrowly to the code in the repository today, she argued the requirement survives the platform change — "или ре[йдж] или нова, вот у нас есть машина, на которой стоит игра, принимает деньги, достаёт деньги, поэтому требование оно остаётся[,] тоже просто реализовано на другом языке" — and then made the decisive point: deriving acceptance criteria from the code means "все сойдется. Все будет правильно," so nothing is ever found. Val conceded and proposed settling it by experiment. See [[wiki/decisions/2026-09-03-acceptance-criteria-settled-by-experiment.md]]. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **She restated the role boundary and Val endorsed it 100%:** requirements are written neither by QA nor by the developer — "не он пишет регламент[,] не QA… точно так же, как и не девелопер пишет рекларменсы… Они их реализуют и проверяют." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **She pushed the Jira structure back onto the agenda** — the tidied capabilities must move into Jira and the new Jira structure be built, resuming what "Dima" started before his holiday, with LGS a candidate next project. Val agreed but said she had put it too softly: "вы очень както мягко к этому подошли. Я как бы более жёстко на это смотрю, что без этого невозможно." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- Val's closing thanks named her contribution: "Ирина[,] хороший [comment]." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Sept 2 2026 — stops the Flex-IQ call from skipping the delivery plan

On the [[wiki/meetings/2026-09-02-flex-iq-pre-pilot-updates-after-the-show.md|Sept-2 Flex-IQ pre-pilot call]] (Russian) Irina made one intervention, and it is the reason the call produced dates at all. When [[wiki/people/pavel.md|Pavel]] moved to close the pre-pilot punch list and go to strategy, she stopped him: "нет, подожди Паш… Я про то, что мы не определили план, когда мы… Реализуем первую часть." [[wiki/people/andrei-klimovich.md|Andrei]] backed her — "я бы хотел тоже это проговорить ещё раз зафиксировать" — and the exchange produced [[wiki/people/dmitri-chudinov.md|Chudinov]]'s end-of-week code commitment and Andrei's Tuesday test. [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

- She also pressed on the hardware dependency ("когда появится это всё железо у тебя") and, at the close, restated the third punch-list item so it was not lost; she protected Chudinov's week from interruption when the Friday follow-up was floated: "у Диме… не надо[,] как по срочному доделать[?] Вот что планирует до конца недели… Чтобы… Не отвлекать." [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- On the printer path she checked her own understanding of the switcher design out loud — "мы, принтер всё равно через IQ подключен к [Mutha Goose]" — and Andrei confirmed it, with bypass if IQ is dead. [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- She accepted the barcode-reconciliation answer on behalf of the room: "Всё это и хотели услышать." [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Open commitments (Sept 3 2026)

- [ ] Send [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] the link to the `knowledge` repository — due immediately — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [ ] With [[wiki/people/pavel.md|Pavel Frolov]] — tidy the capabilities, move them into Jira and build the new Jira structure (LGS a candidate next project) — due September 2026 — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]] [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Open commitments (Aug 26 2026)

- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — contact [[wiki/people/efim-podvoiski.md|Efim]] about the Georgia RTP percentages (the ~88% option) and put South Dakota VLT-2 on test — due same day for the Efim contact; test ~the following week, release target Sept 1 2026 — [[raw/Meeting_Notes_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]] [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — keep Val and [[wiki/people/juan-martinez.md|Juan]] copied on all of Ivan's South Dakota (South Dakota VLT-2) submission correspondence, and call Val directly if she sees the schedule slipping — ongoing from Aug 26 2026 — [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

## Sept 4 2026 — in both meetings: the acceptance-criteria direction question, and the branch that was cut from Florida

**Morning, engineering** ([[wiki/meetings/2026-09-04-rage-nova-conversion-readiness.md|Sept-4 9:04 AM]]) [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]]:

- **She challenged Val's formulation of what an acceptance criterion is.** Val had said criteria "должны описывать то, что исполняет код"; Irina: "акцептон[с] критерии должны описывать код или это должно быть наоборот, код… реализовывает аксептон[с] требования[?]" Val said the distinction did not land in his Russian — "у меня слабый русский язык[;] для меня это звучит практически одинаково, но, наверное, есть какойто нюанс, который вы вцепились" — and did not resolve it. Irina restated the correct order for new work: "Есть требования, есть аксеп[танс] критерии[,] есть [capability;] ещё не[т] кода[,] не[т] фич[,] ничего нет. Я говорю про правильный путь." The unresolved version of this is on [[wiki/decisions/2026-09-03-acceptance-criteria-settled-by-experiment.md]]. [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **She asked whether Igor's work was in Git**, which is what started the exchange leading to Val's "у нас есть написанный стандарт." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **She defined what she wants from the developer side for tests:** hooks, so tests can be written before the game exists — "чтобы как сбросить деньги, как сделать спин и так далее" — naming the framework the team had used as "play riot" and not recalling the language. Her worked example of this week's test: "Запустил[] игру, открыл хелп, сверил, что все хелпы соответствуют тому, что написано в… одном из [capability]." Val added: "но не глазами." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- She also noted a second, reworked version of Test 360 exists, done "с Сашей, который не работает" — which Sasha is not stated, and this is left unresolved. [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]

**Afternoon, game development** ([[wiki/meetings/2026-09-04-naming-convention-standards-and-nova-conversion.md|Sept-4 2:07 PM]], joined for part): Val switched to Russian to question her directly about which branch the Georgia V3 Jackpot Rush was cut from; that stretch of the transcript is poorly captured. Lena's account in the same meeting was that "**Irina decided with somebody else that we are going to cut it from Florida branch**" without consulting her. See [[wiki/decisions/2026-09-04-asset-naming-convention-must-be-written-down.md]] — Val explicitly refused to pursue fault: "I actually don't really care what, who is at fault. My goal is to determine that it never happens again." [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]] [[raw/Meeting_Notes_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]

## Sept 9 2026 — makes the automation case, proposes status-based release separation, and audits what Bosik generated

On the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept-9 7:02 AM call]] (Russian; Val and [[wiki/people/pavel.md|Pavel Frolov]]):

- **She answered Val's "why write anything down at all" challenge with the cost argument**: "[т]естировать руками — это будет постоянно много занимать[;] автоматизировано 1 раз займёт время, а потом это будет быстро, потому что тесты будут готовые. И руками не надо тестировать." Full exchange on [[wiki/topics/test-automation-strategy.md]] (Sept 9). [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **On separating MVP 1 from MVP 2 in Jira she proposed using the capability status**, not fix versions — "это статусом можно как[-]то регулировать, то есть [капабилити] принято, но она будет у нас в следующем релизе" — and warned that later-release capabilities otherwise push the whole product's timeline out. Pavel disagreed; unsettled. See [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]] (Sept 9 2026). [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **She pressed Pavel for the concrete numbers** so she could audit Bosik's output — "[д]ай хоть один номер, который он сделал, я не могу найти" and "[п]ерешли мне, пожалуйста[,] письмо" — and got the forward on the call. She then attributed the Wi-Fi capabilities (145, 143, 142, 140) and spotted that a capability carried no requirements at all: "здесь совсем нет требований никаких." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **She checked whether Flex-Port code was still sitting outside the repository** — "этот Яворский уже всё должен был в ги[т] выложить[,] у него ничего не должно было нигде ж остаться" — and Pavel confirmed all the work is in git. [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **Capacity:** the SAS documentation work runs this week only, "[а] дальше у нас транзакшн… в приоритете у всех" — the derived notes read the same line as "the SAS documentation work is this week only, and after that transactional is everyone's priority." *(The transcript renders it «рекламы suss docota»; the §4 South-Dakota garble family makes "Dakota" an alternative reading — flagged, not resolved.)* [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]] [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **She also asked Val for a release date** — "[м]ы хотим какой[-]то дат[ой] это выпустить?… не так, что вот чем быстрее, тем лучше" — and Val said he could put a date down but did not yet know what to attach it to: "я не понимаю, на что дату надо ставить. Я пока не могу прочувствовать, что я могу получить." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

**Open commitments (Sept 9 2026)**

- [ ] With [[wiki/people/alexei-khamin.md|Alexei Khamin]] — review Bosik's generated requirements and grade how much of the scope they cover — due before the Bosik/Kovalchuk session — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] With Khamin — write the negative cases up as acceptance criteria in parallel with the positive-case work — due unspecified — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

## Sept 10 2026 — she works the certification schedule backwards, and owns the capability tagging

At the [[wiki/meetings/2026-09-10-capability-requirements-workflow-and-mvp-split.md|Sept-10 2026 5:31 AM transactional call]]. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

- **She pushed the schedule so nobody relaxes.** After the 18th they want a version to hand [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] to install on his own devices — "[п]осле 18 числа… мы хотим иметь какую[-]то версию, которую мы можем отдать [А]ндрею, чтоб он начал ставить у себя на девайсах и смотреть, что получается." [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **Then she worked backwards from the field deployment on the 1st.** About a week for [[wiki/organizations/eclipse-gaming-lab.md|Eclipse]] to issue certificates "если они только нами занимаются", plus about a week for the machine's own certification — "неделя на сертификацию[,] значит[,] 24 мы должны максимально отдать машину[,] туда[,] даже если мы это не сертифицируем." [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **But the premise is shaky and she said so.** Asked by [[wiki/people/andrey-bosik.md|Bosik]] whether this is certified at all, she answered "[в]роде сказали[,] да[,] какие[-]то се[ртификаты]… не знаю[,] почему[-]то вам сказал[и;] может быть[,] это он просто ошибся." Carried as an open question on [[wiki/decisions/2026-09-10-requirements-come-first-and-the-recycler-is-out-of-both-mvps.md]]. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **She named the filing problem** that produced the components decision — "[в]от это вот очень неудобно, что все эти… требования[ и капа]билити в одной куче свалены" — and took the tagging work, about an hour out because she was on something else. See [[wiki/decisions/2026-09-10-per-product-components-and-mvp-fix-versions-on-the-capability-project.md]]. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

## Open commitments (Sept 10 2026)

- [ ] Irina Shishko — post the component list into the meeting chat, then tag the capabilities with their components — due September 10 2026, about an hour after the components exist — [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

## Sept 11 2026 — she fixes the sorting criterion, settles the acceptance-criteria rule, and will not let the status question go

Irina was in both Sept-11 meetings. In the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|8:04 transactional call]] she made three interventions that shaped the outcome. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

- **She corrected the MVP-1 sorting criterion on the spot:** "мвп один это то, что мы должны к 1 октября сделать, а не потому, что его понял или не понял Паша" — the deadline sorts it, not anyone's comprehension. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **She settled the capability-versus-regulation question** that had stalled Bosik's Wi-Fi clean-up: "акцепт[анс] критери[и] только в [регламента]х живут[;] cap[abi]l[i]t[y] это просто общее описание… [о]ни в [регламентах], которые никуда не деваются, остаются жить." [[wiki/people/dmitri-chudinov.md|Chudinov]] accepted it and said he had not known. See [[wiki/decisions/2026-09-11-acceptance-criteria-live-in-the-regulations-not-the-capabilities.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **She asked, twice, who moves a capability to In Progress and when** — "[и]н[ ]прогресс кто переведёт?… [и] в какой момент?" — refusing the answer that somebody sits and watches. That pressure is what produced [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]]'s automation offer. See [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **She stated the priority order** — "[м]ашина[,] порт[,] айкью", then "машина[,] порт[,] [пэй]", both before October 1 — before Val's later ruling narrowed October 1 to Flex IQ alone; and she is the one who put that narrowing into words for the record. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **She got the Eclipse scope answered:** asking whether the machine alone is certified through Eclipse, Val answered "[т]олько машину" — closing her own Sept-10 open question. See [[wiki/organizations/eclipse-gaming-lab.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **She has no edit rights for release names in the tool** — "я хотела сделать, а у меня нет прав" — and had the release renamed to put "Transactional" first. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **In the [[wiki/meetings/2026-09-11-nova-game-change-regulatory-procedure.md|9:30 regulatory call]]** she made the software-side version of Pavel's point: everything is connected and a game the Lottery did not know about cannot simply be added — "[к]ак бы каждый софт с этим соединён[,] нельзя просто так добавить игру… не знал лот[е]ри[я] об этом." [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]

### Sept 11 2026 (10:33) — one line, and it is the framing line

She was also in the third meeting of the morning, the [[wiki/meetings/2026-09-11-technician-complaints-and-new-capabilities-workshop.md|technician-complaints workshop]], where she says almost nothing. Her one substantive contribution reframes what a complaints list is: with Val explaining that the market's demand is not defined but the market's irritations are, Irina supplied the category — "**Требования чего не должно быть**" — requirements for what must *not* be there. Val's own line either side of it: "запроса рынка сегодня не дефайнд. Но на рынке есть комплей[нты], что им уже не нравится" [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

She is named to the Monday Sept-14 9:30 working meeting on the new Passport/RIS regulations and asked to think it through beforehand — see [[wiki/decisions/2026-09-11-new-regulations-for-the-passport-and-ris-talked-out-monday-and-converted-from-the-transcript.md]] [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

## Open commitments (Sept 11 2026)

- [ ] Irina Shishko — think through how she sees the new Passport/RIS capabilities, and attend the Monday working meeting — due Sept 14 2026, 9:30 — [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- [ ] Irina Shishko — schedule the automated-test features for the e-wallet use cases and assign them, with [[wiki/people/alexei-khamin.md|Alexei Khamin]] as the named owner — due week of Sept 14 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] Irina Shishko — request edit rights for release names in the tool — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Sept 14 2026 (6:38 AM) — she argues the layout question on its merits, and is answered with a production constraint

At the [[wiki/meetings/2026-09-14-texas-vertical-conversion-and-georgia-game-base.md|Sept-14 6:38 AM ET session]] (Russian) Irina was the only person pushing to save the horizontal→vertical conversion by rearranging the scene rather than changing the source game. [[raw/Meeting_Notes_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

- **Her proposal:** leave the top screen at its current size and enlarge the main game field instead — "нам нужно main экран увеличивать, а не верхний. То есть этого достаточно информации, и он не нужен больше" — keep the pay table as it is, "потому что он достаточн[ой] высоты [и] ширины", then see what is left at the top for the logo. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **She interrogated the geometry before arguing**, checking whether the three areas were equal and pinning Igor down to numbers ("не просто говоришь, 1080, 1000"), and asked whether the dashboard area could be separated out and played with independently. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **The answer she got is a production fact, not a refusal:** the reel frame and the logo are baked into the background video, so "замена фона это фактически замена все[й] сцены" — see [[wiki/topics/game-art-animation-production-pipeline.md]] (Sept 14). She conceded the point by moving to the economics: "переделать фон или… одну игру доработать, это всё-таки меньше, чем с нуля сделать там все игры." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **When [[wiki/people/igor-metelski.md|Igor]] deflected with "мы с вами… не художники[,] дизайнера… и не [ге]й[м] продюсер", she did not accept it:** "Я чисто по расположению… Мы люди с опытом." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **She is the one who asked what progressive Texas currently runs** — "А у нас Техас мистери сейчас?" — and put the same question to [[wiki/people/anton-leshkevich.md|Anton]] ("Антон, напомни, разве там мистери прогрессив?"). Neither answer was clear in the recording, and Val then ruled the question aside. She also flagged early that a different game base means different maths: "Ну математика будет другая." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **She stated that Texas and Nebraska are the same thing** — "Техас из небраски" — which Val confirmed: "Да, это одно [и] то же." See [[wiki/projects/texas-used-machine-distribution.md]] (Sept 14). [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

**§15.8:** clear — engineering and product content only.

## Sept 14 2026 (7:37 AM) — she was left off the code-standards email, and Val cut her off mid-point

At the [[wiki/meetings/2026-09-14-code-standards-main-branch-rule-and-alekseev-coaching.md|Sept-14 7:37 AM code-standards call]] (Russian), an hour after the session above:

- **She did not receive the email the meeting was about.** Val asked whether everyone had it; [[wiki/people/alexei-khamin.md|Khamin]] said yes; Irina said "**У меня нет**" and then "**Интересно, а почему меня не хочет меня присылать? Ну ладно**" — interesting, why won't it send to me; never mind. Val asked whether she was copied and nobody established it. **Not followed up in the call.** [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]] A distribution gap on a company standard addressed to engineering, with the Director of QA off it — recorded as an open question on [[wiki/decisions/2026-09-14-main-branch-must-always-build-and-the-code-belongs-to-the-project.md]].
- **She tried to enter the branch argument and was held back.** As Pavel was proposing to tag the no-SAS version as release one and promote his own branch to main, she began "**Паша, ну мне кажется что это…**"; Val stopped her — "**подождите, Ирина, дать им закончит[ь]**" — and she did not return to the point [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. Her view on the tag-versus-branch question is therefore **unrecorded**.
- She agreed with the main-branch rule as read ("**Ну должно**") and, on the coaching question, supplied the one-word answer "**Научит**" — he will teach him [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

## Sept 14 2026 (8:01 AM) — she names the port interaction a dialogue, and keeps pushing the status question

An hour after being cut off on the code-standards call, she was back in the transactional [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|8:01 AM use-case call]] and her contributions were taken up each time.

- **The framing that stuck.** On Klimovich's rule that the port must show the balance and wait for confirmation, she supplied the description everyone then used: "**то есть диалог должен произойти между игроком и портом**." Klimovich agreed and folded it into the requirement [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].
- **The release-legibility argument** that justified moving requirement 1538 rather than editing every capability: "мы выпустим 1 октября[ —] как ты закроешь эти [capabilities], что мы выпустим, чтобы понимать, что вот в этом релизе мы сделали вот это, а теперь мы будем делать следующее" ([[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]]).
- **The printer question that opened the whole failure scenario:** with no paper or a dead printer, "а как [IQ] после создания [e-]лет[а] распечатает [carrier] этот?" That is the question the Sept-13 transaction-recovery block turned out to answer ([[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]]). She offered the machine-side tilt list on the spot — "я могу тебе их… которые на машине дать" — and named low paper and no paper; the head error and the general error came from Pavel.
- **The top-up gap.** She pointed out the wallet can also be topped up at the counter — "[e-]лет на IQ пополняемый" — and Klimovich conceded there is no use case for it although the capability exists. She also flagged that capabilities 148, 149 and 150 had been treated as already implemented, needing only automated tests [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].
- **She would not let the status question go, again.** As on Sept 11, she pressed that a capability should only be Accepted once it holds all its requirements, and that requirements themselves must change status when approved. Val conceded the principle ([[wiki/decisions/2026-09-14-nothing-in-mvp1-may-still-be-proposed-and-bosik-writes-the-exception-report.md]]).
- A lighter moment, recorded because it dates the standard: she put SAS 6.02 at "уже лет 20", was talked down to about ten by Pavel and Biratka, and accepted it — Val: "Ирина[,] что[-]то вы нас на скрипке сыграли сейчас" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Open commitments (Sept 14 2026)

- [ ] Irina Shishko (with [[wiki/people/alexander-biratka.md|Alexander Biratka]] confirming it is the same printer) — send Klimovich the list of printer tilts handled on the machine — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## Sept 15 2026 (8:03 AM) — she corrects the link direction, and puts promo money out of the release

At the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept-15 8:03 AM call]] (Russian) she made three interventions that changed outcomes [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**She corrected the Jira link direction.** She named Klimovich's habit before he described it — "**я знаю, что ты всегда ставишь [implemented by requirements]**… мне кажется, это неправильная" — and gave the reasoning: a *feature* is what gets implemented; a capability is *based on* requirements. The agreed form became "capability requires requirement", and Klimovich took the cleanup across every link. See [[wiki/decisions/2026-09-15-capability-requires-requirement-and-dates-sit-on-the-lowest-level.md]].

**She put promotional money out of MVP 1 in one sentence:** "**давайте, если мы хотим до 1 числа и промо деньги нам не до 1 числа, мы это сделаем MVP 2[ или ]3, потому что там всё очень сложно с этим**". Klimovich parked it and thanked her by name. See [[wiki/decisions/2026-09-15-balance-is-total-playable-only-and-redeemable-everywhere.md]].

**She found the emphasis backwards on the collect screen** — the big button pushes the player to take a new ticket rather than scan the one in his hand — and Klimovich agreed the emphasis must move to scanning [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

Her position on the balance naming was consistent with the outcome from the start: "баланс это полностью баланс… это всё, что есть[,] неважно[,] играемо[е] или выводимая", which is what "Total" came to mean. She is one of the five named owners of the non-functional requirements due Monday Sept 21 ([[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]]).

## Open commitments (Sept 15 2026)

- [ ] Irina Shishko (with [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], [[wiki/people/andrey-bosik.md|Andrey Bosik]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] and [[wiki/people/pavel.md|Pavel Frolov]]) — write the non-functional requirements for FlexPay, Flex-Port and Flex IQ — due Monday Sept 21 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## Sept 16 2026 (8:01 AM) — she calls the meeting, drives it from her own list, and makes the separation that ends the offline argument

The third MVP 1 morning call ([[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16 2026 8:01 AM call]], Russian) exists because of her. She had started on the non-functional requirements [[wiki/people/val-levitan.md|Val]] ordered the previous evening and could not proceed [[[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]]:

> **[Я] стара[ла]сь поработать с требованиями… нон фан[кшнл,] и столкнулась с тем, что у нас половина требований имеют открытые вопросы, и как только Клода просишь с этим поработать, мы тут же получаем[:] "у тебя там открытый вопрос"… нам нужно вот эти все требования почистить[:] либо дать ответ, либо… убрать этот вопрос.**

She had the AI assistant build her the list — capabilities whose requirements carry open questions — and then navigated Klimovich through it for ninety minutes, number by number [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Her single most useful contribution was a distinction.** With the offline argument circling, she split the two things that had been run together: "**по[-]моему[,] мы тут 2 вещи… в одну свалили[:] есть[,] когда блокировка [придёт] — то есть закончилась лиза[ —] мы блокируем[,] это одно. А когда там нет интернета… это уже 2[-]й вопрос, и мы договорились, что мы работу не блокируем… игрок играет, единственное[ —] мы не можем выпустить карточку. И говорим, приходи завтра**" — which is the settlement the meeting adopted ([[wiki/decisions/2026-09-16-a-location-keeps-working-without-internet-and-only-the-card-stops.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. Earlier in the same exchange she had already pushed back on Chudinov's framing: "мы ничего не блокируем, мы только не можем выпустить карточку" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Release legibility is again her argument for moving things rather than rewording them:** "как нам делить, что сделано, что не сделан[о]? Есть capability 116. По нашим требованиям это всё должно работать к 1 октября, но не будет работать" ([[wiki/decisions/2026-09-16-anything-that-depends-on-the-cloud-leaves-mvp1.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**She enforced status discipline in the direction people avoid.** Requirement 1454 was moved *back* from Published to Draft because the error catalogue behind it does not exist — "паблиш для этого [реквайрмента] поменяй на… драфт" — and requirement 1451 was taken off Published too [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. She also flagged the practical cost of the team's AI-assisted workflow: an open item deliberately left in place "нужно будет как[-]то обозначить для Клода", or the assistant keeps tripping on it [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Open commitments (Sept 16 2026)

- [ ] Review and update the status of every capability and requirement she authored, as Klimovich has done for his own — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

## Sources

- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Notes_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [[raw/Meeting_Notes_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Notes_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_1-May-12-2026.md]]
- [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_2-May-12-2026.md]]
- [[raw/Meeting_Notes_Flex_POS_Alpha_and_OMNI_2_Architecture-April-15-2026.md]]
- [[raw/Meeting_Transcript_OMNI_Architecture_Challenge-March-27-2026.md]]
- [[raw/OMNI_Architecture_Challenge-March-27-2026.md]]
- [[raw/Meeting_Transcript_initiative_priority_schedule-1-March-26-2026.md]]
- [[raw/Meeting_Transcript_initiative_priority_schedule-2-March-26-2026.md]]
- [[raw/Meeting_Notes_initiative_priority_schedule-March-26-2026.md]]
- [[raw/Schedule_review_Nebraska-March-5-2026.md]]
- [[raw/Schedule_review-March-4-2026.md]]
- [[raw/Schedule_Nebraska-February-27-2026.md]]
- [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]
- [[raw/Claude Code integration - continued.md]]
- [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]
- [[raw/Specs_graphics.md]]
- [[raw/Payment HUB_ACH module specification_05.11.25 .md]]
- [[raw/Payment HUB_ACH module specification_10.11.25.md]]
- [[raw/Machine Quality Control Checklist and a Release form.md]]
- [[raw/media_tax_credit_team_coaching-july-28-2025.md]]
- [[raw/alignment-planning-catch-up.md]]
- [[raw/flex_tower_spacial_design_review-may-1-2025.md]]
- [[raw/test-360_progress_review_meeting.md]]
- [[raw/integration_and_testing_procedures_january_15_2025.md]]
- [[raw/game_design_meeting_february_21_2025.md]]
- [[raw/sd_vlt_recap-jan-22-2025.md]]
- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- [[raw/github_jira_setup-april-3-2025.md]]
- [[raw/omni_progress-april-14-2025.md]]
- [[raw/sas_51_52_requirement_interpretation-april-14-2025.md]]
- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- [[raw/integration_tests-apr-24-2025.md]]
- [[raw/ci_cd_qa_structure-apr-24-2025.md]]
- [[raw/set_up_screen_omni-apr-24-2025.md]]
- [[raw/ga-coam_error_51_52-apr-24-2025.md]]
- [[raw/omni_test_status_review-may-14-2025.md]]
- [[raw/commission_flex-pay-may-16-2025.md]]
- [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]
- [[raw/sas_intricacies_ga-coam-may-21-2025.md]]
- [[raw/test_engineering_progress_report-may-21-2025.md]]
- [[raw/dev_review_flex-pay_flex-port-may-27-2025.md]]
- [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- [[raw/jp_treatment-may-28-2025.md]]
- [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]
- [[raw/jira_plans_maturity-mat-29-2025.md]]
- [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]
- [[raw/flex-pay_flex-port_progress_review-june-2-2025.md]]
- [[raw/meter_sas_function-june-10-2025.md]]
- [[raw/games_design-june-12-2025.md]]
- [[raw/jp_meters-june-12-2025.md]]
- [[raw/qa_engineering_direction_review_aaron-june-12-2025.md]]
- [[raw/Metering_class_3-june-17-2025.md]]
- [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Notes_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
- [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- [[raw/Meeting_Notes_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
