---
type: person
title: Pavel
date: 2026-07-12
aliases: [Pavel, Pasha, Pavel Frolov]
disambiguation: "One of TWO Pavels: Pavel Frolov (JVL Minsk → wiki/people/pavel.md, this page) and the external Ukrainian outsourcing-studio owner Pavel (wiki/people/pavel-studio-owner.md). Resolve by context; queue if unclear."
source-count: 29
open-commitments: 1
open-questions: 0
---

# Pavel

Pavel (called "Pasha") is a JVL engineer on the Minsk team who works on system/driver and pipeline matters. On the Jan 17 DTP-53 call Aaron refers to him as an **engineering director** whose job is now to write specifications, not code. [[raw/dtp-53_action_builder_pipeline_definition_of_features_january_17_2025.md]]

## Role

- On the FP7 review, Val noted Pavel may need to search for more optimized Linux drivers, and gave Pavel and Alexander the undertaking to run further tests (with a measurement tool to find the performance bottleneck) before a follow-up meeting. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Pavel proposed the further testing needs a measurement tool or logs from browsers to show where video frames drop. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Attended the Jan 14 AI-assisted-development workshop. Aaron noted Pavel had built a couple of CI/CD YAML files by hand but is not yet fluent in them; Pavel had trouble cloning the repo and getting the AI tool's terminal working during the session. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- Pavel wrote the pipeline-problem document that Aaron used as the seed input for the AI workshop demo. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]

## Build-pipeline decision meeting (Jan 15)

- Pavel agreed with (and helped shape) the move to a Git-native build system. His key requirement: any build's config must be saved in Git so a shipped production build can later be rebuilt — e.g. as a debug build to investigate a problem. He argued games should be Docker volumes (mounted), not standalone images, to avoid overhead. [[raw/parameterization_in_the_development_pipeline_part_2_january_15_2025.md]] [[raw/parameterization_in_the_development_pipeline_part_3_january_15_2025.md]]
- Pavel favours submitting a non-instrumented build to GLI plus a procedure to install the instrumentation. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

## DTP-53 feature and FP7 testing (Jan 16–17)

- **DTP-53 (Jan 16–17):** Pavel owns the Git-native pipeline work as JIRA feature DTP-53. He first framed it as several separate per-model pipelines; Aaron then coached him to write proper customer-focused feature descriptions (installer pipeline, long-term artifact storage, GitHub configuration). His homework is to rewrite them as features (see the commitment on [[wiki/topics/build-pipeline-parameterization.md]]). [[raw/dtp-53_feature_planning_meeting_january_16_2025.md]] [[raw/dtp-53_action_builder_pipeline_definition_of_features_january_17_2025.md]]
- **FP7 bottleneck testing (Jan 17):** with Alexander, ran the deeper video-stream tests, translated between the Russian- and English-speakers, and concluded the bottleneck is the CPU. Pavel argued the key question is *where* the bottleneck is, and pushed to switch to the new Pixi engine version and to define which Omni components need continuous updates. His undertaking: check for a better Linux driver and revisit the Omni architecture (see [[wiki/decisions/2025-01-17-remain-on-fp7-hardware-ceiling.md]]). [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## South Dakota software and FlexPort beta (Jan 22–24)

- **South Dakota (Jan 22):** Pavel handles the Minsk software for the SD lab machine — the FutureLogic Gen 5/Gen 2 printer behaviour, the erroneous game-shutdown countdown, CRC validation, and printing via the Minsk SAS emulator. Val told him to contact Light & Wonder for logs but not to wait for them — to find the shutdown-trigger cause himself. See [[wiki/projects/south-dakota-vlt-market.md]] and [[wiki/decisions/2025-01-22-support-epic-950-printer-for-south-dakota.md]]. [[raw/sd_vlt_recap-jan-22-2025.md]]
- **FlexPort beta (Jan 24):** the FlexPort beta (~3 weeks out) and its assembled testing with FlexPay are attributed to Pavel's group; ticket validation is handled by FlexPay. See [[wiki/topics/jvl-machine-lineup.md]]. [[raw/flex_port_hardware_up-jan-24-2025.md]]

## Freed for critical development + the part-1 debate (Feb 7–10)

- **Feb 7:** Val excluded Pavel from the GitHub-structure meetings "from now until March 1st" — "we have some critical development that we need Pavel for… I'd like to exclude you from these meetings… just let you be." See [[wiki/meetings/2025-02-07-github-homework-and-bitbucket-transfer.md]]. [[raw/GitHub repository structure.md]]
- **Feb 10 (part 1):** he attended anyway as translator/participant. Val sketched him as the **core-tools org owner** while noting "Pasha doesn't handle everything. He doesn't handle test 360… has some influence on diagnostic tool… doesn't manage design tools. Miranda, for example." Val summarised Pavel's position as: "if Pasha is right, and a platform is just a facilitation, a duplicatable process of making games, then fine… cookie cutter" — reskins are copy/change-resources/release, while special effects or bonuses still need programming ("That's Miranda. Probably"). (The "you cannot create games without programmers" passage in the same meeting has no clear speaker label and is not attributed here.) Val criticised him for yielding his questions to Alexander too easily ("you're lacking persistence in your questioning"). See [[wiki/meetings/2025-02-10-github-repo-structure-part-1.md]]. [[raw/github _structure-pavel-aaron-andrei.md]]
- **Docs-in-Git debate (late Jan–early Feb):** on the "culture of courtesy" session Pavel probed what documentation belongs in Confluence vs the repo; Aaron used him as the example of PR discipline — "Pavel's not allowed to just commit it to the main branch… your code… must be in a development branch first and then pulled into main." See [[wiki/meetings/2025-02-01-docs-in-git-vs-confluence.md]]. [[raw/the_importance_of_storing_artifacts_in_git.md]]

## GitHub repo structure (Feb 11)

- On the Feb 11 org-structure session Pavel ("Pasha") pushed the naming details (e.g. replace "OmniEngine" with the hardware-abstraction-layer "HAL"), agreed to restructure the Jira value streams to match the GitHub orgs, and confirmed he wants "as close an integration as possible" between Jira and GitHub. He flagged that the **FlexPay** project should be added to the first migration batch (Omni + Miranda). See [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]] and [[wiki/decisions/2025-02-11-git-migration-sequence.md]]. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## GitHub check-in and market alignment (Feb 12, Feb 19)

- **GitHub check-in (Feb 12):** attended as a reviewer ("Pasha") on Andrei's DevOps-repo pull requests and the repository-access discussion. See [[wiki/meetings/2025-02-12-github-check-in.md]]. [[raw/Check_in_on_GitHub_2025-02-12.md]]
- **Outstanding-subjects alignment (Feb 19):** Pavel is the technical owner across the market releases. He is injecting **Epic 950** printer support into the SD software (~end of next week) and will judge whether Epic Edge can be added; he taught Val the correct taxonomy — a printer's **firmware** sits on the printer, while JVL's side is a **hardware-abstraction-layer library**; the third printer connector is a **harness** (not a jumper); printer library types split into Gen 2 / Gen 5 (JCM) + nano-optics vs Epic. He proposed defaulting/relabelling the third COM port so operators can't misassign SAS ports. Val also pressed him on the English precision of "it seems to be working." See [[wiki/projects/south-dakota-vlt-market.md]] and [[wiki/projects/georgia-market-rollout.md]]. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Embedded group — connection debugging (Feb 25)

- On the Feb 25 embedded standup Pavel ("Pasha") is debugging why the FlexPort↔FlexPay **connection drops even though his ping-pong keepalive runs every second** and is received — cause unknown; he asked the JVL side to investigate, and noted the pings aren't showing in the logs. Val turned it into a design point: **detailed comms logging should be a formal requirement** (an enable-able log mode, as with Bally/Konami AFT); Pavel was cautious about always-on logs (too voluminous) but agreed a toggle-able mode is needed. See [[wiki/meetings/2025-02-25-embedded-group-flexport-flexpay.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]

## The "Pavel replacement" automation idea (Feb 21)

- In a Feb 21 call Aaron used Pavel as the example of a role to automate: the step-by-step deployment/build flow Pavel performs could be baked into an MCP so an AI orchestrates it. See [[wiki/topics/ai-assisted-development.md]]. [[raw/Call_with_Aaron_Bockelie_2025-02-21.md]]

## Flex card reader, Incom, and game engineering (Feb 27–28)

- **Flex V42/C credit-card reader (Feb 27):** the full-insert credit-card reader is a **USB device**; Pavel already has a sample; it needs a **software** (not firmware) upgrade to drive it. See [[wiki/decisions/2025-02-27-flex-street-cabinet-design-direction.md]]. [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]
- **Incom commissioning (Feb 27):** Val named Pavel as JVL's **Director of Engineering** and the engineering point of contact for the Incom payment-processor integration (with [[wiki/people/juan-martinez.md|Juan]] as first point of contact). See [[wiki/organizations/incom.md]]. [[raw/incomm_commissioning_plan_february-27-2025.md]]
- **Progressive per denomination (Feb 28):** Pavel's engineering group confirmed it is easier to add a progressive level **by denomination** on the **HG-6** CPU kits, removing the max-denom-only limit; committed to have it in ~2–3 weeks with an individual progressive per denomination. See [[wiki/decisions/2025-02-28-hg6-individual-progressive-by-denomination.md]]. [[raw/Game design part 1 - Feb-28-2025.md]]

## Nebraska skill market (Mar 14)

- On the Nebraska call, Pavel ("Pasha") is the engineer who needs a **clear instruction on where to commit** the changes — Val observed that Pavel was "confused on what we're trying to commit," which the team resolved by settling the software approach (revert nudge on the v1.14 VDEC build, remove hands). See [[wiki/projects/nebraska-skill-market.md]]. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]

## Open commitments

- [ ] Pavel — produce image files (e.g. an ext2/ext4 partition or a Docker/Docker-Compose image) that collect the modules for local deployment; full ISO assembly deferred to a later milestone — due by the next meeting (Monday) — [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

Note: "Pasha" and "Sasha" are sometimes confused in the transcripts; "Pasha" maps here to Pavel, "Sasha" to Alexander Biratka. See [[wiki/people/alexander-biratka.md]]. His surname is given once as **"Frolov"** in the Jan 17 FP7 meeting ("Pavel Frolov has to see if there is a better Linux driver"). [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Puerto Rico product line (Mar 21)

- On the Mar 21 Puerto Rico product-matrix call, Pavel owned the software side: he took the task to plan adding the **old counter-board's button key codes into the HG6 XML file** so one software supports both legacy and new panels (rather than firmware changes [[wiki/people/genadi-peari.md|Genadi]] proposed), and to work out how **Megahit on Flex** copes with physical buttons and fewer monitors. He confirmed retrofit machines and kits use the cabinet board while Flex-S uses V1000, and that all machines use an **IMG file** (not ISO). See [[wiki/topics/puerto-rico-product-configuration.md]] and [[wiki/decisions/2025-03-21-hg6-support-legacy-and-new-button-panels.md]]. [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]

## FlexPay scope-gap discovery (Mar 27)

- On the English scope-gap meeting Pavel delivered the news that broke Val's assumptions: **FlexPay cannot work standalone** with third-party machines ("FlexPay will not work in such a scenario when there are five third-party machines installed without FlexPort") — he had understood FlexPay would only ever pair with JVL machines or FlexPort-equipped ones, and **FlexPort has no SAS software implementation** ("we only have RS232 connector and that's all"). Against Val's five-day estimate for a make-do local SAS mini-server he answered "**Months. Two months. Three months**" — there is no SAS-server implementation ready to go. [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- He described the FlexPay software stack (backend by Dima; frontend HTML5/JavaScript by Igor Hrybko and Anton Seregin), first argued the mini-server belongs on FlexPort (only FlexPort can talk SAS to the machine) before agreeing FlexPay is the ticket-issuing brain, proposed keeping the **screen** on the SMIB-ized FlexPort for flexibility (Val refused — the screen is "60% of the cost"), and took the action to **determine the minimal set of SAS commands** FlexPort must support. See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]

## FlexPay TITO scope-gap (Mar 28)

- On the Mar-28 TITO meeting Pavel ("Pasha") was the engineer who designed the MVP: mount **FlexPort inside** a non-JVL machine as a **SMIB**, wire it to the machine's **SAS port** and via CAT6/router to **FlexPay**, and run a **"Flex SAS server"** proxy (split between FlexPort and FlexPay) that converts **SAS ↔ the existing WSS/VCC protocol** and issues/validates TITO ticket numbers. He explained why cheap **Ethernet-to-RS232 adapters** are unreliable (SAS needs **9-bit** operation, adapters mostly do 8-bit), estimated the proxy base at **~2–3 weeks**, and undertook to send Eugine the **IGT SAS-emulator utility** and arrange a test-machine setup. See [[wiki/decisions/2025-03-28-flexpay-support-tito-non-jvl-locations.md]]. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## GitHub-Jira alignment (Mar 31)

- Pavel attended the Mar 31 Russian-language meeting on making GitHub and Jira hierarchy levels match (with Val, Irina, Andrey, and an unresolved "Yura") — the continuation of his Feb 11 "as close an integration as possible between Jira and GitHub" position. The org-level question (initiative vs value stream) went to homework with a Wednesday-7 a.m. follow-up; individual speakers in the debate are not attributable from the transcript. See [[wiki/meetings/2025-03-31-github-jira-alignment.md]] and [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]]. [[raw/github_jira_alignment-march-31-2025.md]]

## History — ~2024 SQL/OLAP architecture sessions

- On the ~2024 (likely Q4) architecture meetings Pavel already authored the SAS designs he would later formalize in the Mar-28 2025 TITO decision: he presented the **two SAS-host options** (connect to a third-party SAS host vs a **JVL-proprietary SAS host run inside the FlexPay kiosk** — his preferred, "cheaper solution… with minimal hardware overhead"), described field practice (serial→Ethernet converters, per-machine Windows micro-PC player-tracking units), and flagged the **9-bit serial** blocker ("we need to use 9 bits operation… quite different") plus the Azure time-limit caveat on SAS-to-cloud. See [[wiki/topics/olap-power-bi-architecture.md]] and [[wiki/meetings/2024-sql-olap-visualization-architecture-2.md]]. [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]] [[raw/architecture_sql_olap_visualization_1_2025-03-29.md]]

## Sources

- [[raw/GitHub repository structure.md]]
- [[raw/github _structure-pavel-aaron-andrei.md]]
- [[raw/the_importance_of_storing_artifacts_in_git.md]]

- [[raw/architecture_sql_olap_visualization_1_2025-03-29.md]]
- [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]]
- [[raw/fp-7_performance_analysis_january_13_2025.md]]
- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_2_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_3_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- [[raw/dtp-53_feature_planning_meeting_january_16_2025.md]]
- [[raw/dtp-53_action_builder_pipeline_definition_of_features_january_17_2025.md]]
- [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- [[raw/sd_vlt_recap-jan-22-2025.md]]
- [[raw/flex_port_hardware_up-jan-24-2025.md]]
- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [[raw/Check_in_on_GitHub_2025-02-12.md]]
- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- [[raw/Call_with_Aaron_Bockelie_2025-02-21.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]
- [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]
- [[raw/incomm_commissioning_plan_february-27-2025.md]]
- [[raw/Game design part 1 - Feb-28-2025.md]]
- [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- [[raw/product_matrix_puerto_rico-march21-2025.md]]
- [[raw/requirements_puerto_rico-march-21-2025.md]]
- [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- [[raw/github_jira_alignment-march-31-2025.md]]
