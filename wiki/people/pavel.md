---
type: person
title: Pavel
date: 2026-07-12
aliases: [Pavel, Pasha, Pavel Frolov, Павел Фролов]
disambiguation: "JVL Minsk engineering director (Pavel Frolov). Pavel cluster (2): [[wiki/people/pavel.md|Pavel Frolov]]=JVL Minsk engineering director / [[wiki/people/pavel-studio-owner.md|Pavel]]=external Ukrainian outsourcing-studio owner. Resolve by context; queue if none."
source-count: 159
open-commitments: 69
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
- [ ] Pavel — contact Juan Martinez for the Bally-SMIB capability list ("homework для этой недели") — due week of Apr 1 2025 — [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- [ ] Pavel — consult SAS experts on technical feasibility (possibly a preliminary flow diagram), and with Irina document the minimum fields for TITO ticket generation — due ASAP (Apr 2) — [[raw/SMIB_FlexPay_Action_Items_April_2_2025.md]]
- [ ] Pavel — after the Apr-8 shipping push, email Val/the team that the initial JVL business architecture is implemented and the product is ready to ship to Georgia — due Apr 8 2025 — [[raw/flex_pay_tito_smib_port-april7-2025.md]]
- [ ] Pavel + Nathan Carver — schedule the Dwolla ACH integration and reflect it in the Jira plans for the next Flex weekly — due ~Oct 2025 — [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]
- [ ] Pavel — once Dwolla opens its dev-support channel, confirm the ACH mechanics parked Nov-6 (Dwolla wallet vs direct funding-source; who creates the customer/funding-source) and produce the verified-customer onboarding business-flow diagram — due after Dwolla agreements resolve — [[raw/Payment HUB_ACH module specification_06.11.25.md]]
- [ ] Pavel — consult Dwolla on sandbox test-account hooks for QA and on API query limits (to avoid the $3,500-per-occurrence over-query penalty) — due when Dwolla support opens — [[raw/Payment HUB_ACH module specification_10.11.25.md]]

Note: "Pasha" and "Sasha" are sometimes confused in the transcripts; "Pasha" maps here to Pavel, "Sasha" to Alexander Biratka. See [[wiki/people/alexander-biratka.md]]. His surname is given once as **"Frolov"** in the Jan 17 FP7 meeting ("Pavel Frolov has to see if there is a better Linux driver"). [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Puerto Rico product line (Mar 21)

- On the Mar 21 Puerto Rico product-matrix call, Pavel owned the software side: he took the task to plan adding the **old counter-board's button key codes into the HG6 XML file** so one software supports both legacy and new panels (rather than firmware changes [[wiki/people/genadi-peari.md|Genadi]] proposed), and to work out how **Megahit on Flex** copes with physical buttons and fewer monitors. He confirmed retrofit machines and kits use the cabinet board while Flex-S uses V1000, and that all machines use an **IMG file** (not ISO). See [[wiki/topics/puerto-rico-product-configuration.md]] and [[wiki/decisions/2025-03-21-hg6-support-legacy-and-new-button-panels.md]]. [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]

## Jira components cleanup (~Mar 19, date inferred)

- On the components-objectives fragment Pavel confirmed he is — "in many cases" — the person who designs/architects **remote initial setup (RIS)**, and asked whether RIS could be treated as a Jira component (like Neighbor). Val's ruling: RIS is not a component but "an incorrect or incomplete initiative name" — really a many-featured piece of **Slot Links**, "a large initiative that we should entertain," under which the RIS elements will be redistributed. See [[wiki/meetings/2025-03-19-jira-components-cleanup.md]]. [[raw/components_objectives_for_a_follow_up_meeting.md]]

## FlexPay scope-gap discovery (Mar 27)

- On the English scope-gap meeting Pavel delivered the news that broke Val's assumptions: **FlexPay cannot work standalone** with third-party machines ("FlexPay will not work in such a scenario when there are five third-party machines installed without FlexPort") — he had understood FlexPay would only ever pair with JVL machines or FlexPort-equipped ones, and **FlexPort has no SAS software implementation** ("we only have RS232 connector and that's all"). Against Val's five-day estimate for a make-do local SAS mini-server he answered "**Months. Two months. Three months**" — there is no SAS-server implementation ready to go. [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- He described the FlexPay software stack (backend by Dima; frontend HTML5/JavaScript by Igor Hrybko and Anton Seregin), first argued the mini-server belongs on FlexPort (only FlexPort can talk SAS to the machine) before agreeing FlexPay is the ticket-issuing brain, proposed keeping the **screen** on the SMIB-ized FlexPort for flexibility (Val refused — the screen is "60% of the cost"), and took the action to **determine the minimal set of SAS commands** FlexPort must support. See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]

## FlexPay TITO scope-gap (Mar 28)

- On the Mar-28 TITO meeting Pavel ("Pasha") was the engineer who designed the MVP: mount **FlexPort inside** a non-JVL machine as a **SMIB**, wire it to the machine's **SAS port** and via CAT6/router to **FlexPay**, and run a **"Flex SAS server"** proxy (split between FlexPort and FlexPay) that converts **SAS ↔ the existing WSS/VCC protocol** and issues/validates TITO ticket numbers. He explained why cheap **Ethernet-to-RS232 adapters** are unreliable (SAS needs **9-bit** operation, adapters mostly do 8-bit), estimated the proxy base at **~2–3 weeks**, and undertook to send Eugine the **IGT SAS-emulator utility** and arrange a test-machine setup. See [[wiki/decisions/2025-03-28-flexpay-support-tito-non-jvl-locations.md]]. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## GitHub-Jira alignment (Mar 31)

- Pavel attended the Mar 31 Russian-language meeting on making GitHub and Jira hierarchy levels match (with Val, Irina, Andrey, and an unresolved "Yura") — the continuation of his Feb 11 "as close an integration as possible between Jira and GitHub" position. The org-level question (initiative vs value stream) went to homework with a Wednesday-7 a.m. follow-up; individual speakers in the debate are not attributable from the transcript. See [[wiki/meetings/2025-03-31-github-jira-alignment.md]] and [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]]. [[raw/github_jira_alignment-march-31-2025.md]]

## FlexPay TITO — dev kickoff and the 30-day turnaround (Apr 1–7)

- **Apr 1:** ran the SAS-kickoff standup's action summary (Yavorski multi-machine bus test + log transfer; Alekseev low-level SAS project; stories with Dima for cash-out + SAS-command logging over WSS) and took the homework to get the Bally-SMIB capability list from Juan Martinez. See [[wiki/meetings/2025-04-01-flexport-flexpay-dev-update.md]]. [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- **Apr 7:** on the architecture-settling meeting his TITO estimate stood at **30 days** — down from the Mar-27 "months — two, three" ("Did I miss something or did Pavel have more time to bring down his previous estimate of three months down to 30 days? Pavel is a miracle worker") — and Val put him **in command of the Georgia shipment**: hardware-team meeting 7:30 am, then loading terminals with Serge Novitskiy and Arkady ("you should assume command and you should push everybody"), 9 am FlexPay recap. See [[wiki/decisions/2025-04-07-flexsmib-modern-flexport-legacy.md]]. [[raw/flex_pay_tito_smib_port-april7-2025.md]]

## History — ~2024 SQL/OLAP architecture sessions

- On the ~2024 (likely Q4) architecture meetings Pavel already authored the SAS designs he would later formalize in the Mar-28 2025 TITO decision: he presented the **two SAS-host options** (connect to a third-party SAS host vs a **JVL-proprietary SAS host run inside the FlexPay kiosk** — his preferred, "cheaper solution… with minimal hardware overhead"), described field practice (serial→Ethernet converters, per-machine Windows micro-PC player-tracking units), and flagged the **9-bit serial** blocker ("we need to use 9 bits operation… quite different") plus the Azure time-limit caveat on SAS-to-cloud. See [[wiki/topics/olap-power-bi-architecture.md]] and [[wiki/meetings/2024-sql-olap-visualization-architecture-2.md]]. [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]] [[raw/architecture_sql_olap_visualization_1_2025-03-29.md]]

## FlexPay Evolution strategy stance (Apr 8–11)

- In the Apr 8/11 business-architecture sessions ([[wiki/topics/flexpay-business-architecture-payout-devices.md]]) Pavel argued **against basing the cheap payout devices on the embedded FlexPort** — "MBED is a difficult solution … not predictable in terms of development time" — preferring a standard cheap x86 board + ~10-inch touchscreen at "the same money"; he estimated a FlexPort-master device at ~3 months of embedded work, sized FlexPay's BOM against the tower idea, proposed the dual-dispenser cheap-kiosk variant and the (rebuffed) **NFC-card** idea, and confirmed the master/slave failover exists "in our embedded progressive." He also supplied the pulse-security rebuttal line: the pulses "live only within a cabinet up to Flexport. We do not move the signal outside the cabinet." [[raw/flex_pay_evolution-april-8-2025.md]] [[raw/evolution_flex_pay-april-11-2025.md]]
- On the Apr 8 recap he explained the two-counter temporary-wallet mechanics (playable vs cashed value; no value printed on the ticket) and the router requirement (all FlexPorts + FlexPay on one router, dynamic IPs). [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]]

## Early-April operational calls (Apr 3–7)

- **RIS ↔ Business Central licensing (Apr 3):** on the Russian licensing-alignment meeting ([[wiki/meetings/2025-04-03-ris-business-central-licensing.md]]) Pavel initially argued the software licence should bind to the machine; Val and [[wiki/people/dmitri-chudinov.md|Dima Chudinov]] ruled it binds to **software per operator by count**. Pavel is where the resulting atomic requirements land — he "folds them into a sprint." See [[wiki/decisions/2025-04-03-license-software-per-operator-not-machine.md]]. [[raw/ris_business_central_integration-april-3-2025.md]]
- **SD Epic printer + MH1 settings (Apr 3):** Pavel confirmed he had tested only the **Epic 950**, not the **Epic Edge** (which scrambled the audit-ticket text) — so JVL owes a new software build; he explained the MH1 same-max-bet limit is really a per-button **multiplier**, not a hard rule, and a minor data-center change. See [[wiki/projects/south-dakota-vlt-market.md]] and [[wiki/meetings/2025-04-03-sd-printer-and-mh1-settings.md]]. [[raw/tech_and_settings_issues-juan_martinez-april-3-2025.md]]
- **GitHub–Jira product reshuffle (Apr 7):** with Sasha and Val (and Andrei on diagrams), Pavel is the one whose sprint the six re-carved products feed into; he raised lengthening the sprint to 3–4 weeks. See [[wiki/decisions/2025-04-07-recarve-gaming-platform-into-six-product-repos.md]]. [[raw/github_jira_reshuffling_products-april-7-2025.md]]

## Apr 16 2025 — runs the Omni planning daily; barcode reader tested

Pavel (Pasha) ran the Omni daily as meeting secretary, walking the Jira feature list (IP 416 Omni Land Base Framework / IP 610 Omni Core) and creating features/stories; he is weighing lengthening the sprint from two weeks to three (maybe four), which Val capped at +1 week. Val nudged him to shift planning to smaller groups so he stops being "секретарь митинга." [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]] Separately, on the Genadi hardware call, Val reported Pavel had tested the TITO-barcode reader — he inverted the image black/white "и потом он читает все" — confirming the scanner works after a settings reprogram. [[raw/fkex_pay_evolution-apr-16-2025.md]]

## Apr 22–23 2025 — Omni scheduling + the FlexPort/TITO-server architecture

- **Omni feature scheduling (Apr 22):** Pavel presented the Jira board and split the Omni Game Framework features for the Calle Ocho port across Sasha, Anton and Igor Metelski, and drove the prune (deleting the Transition-Scene-Integration feature, deferring the topper). See [[wiki/topics/omni-core-advancement-and-game-templating.md]] and [[wiki/meetings/2025-04-22-calle-ocho-omni-feature-scheduling.md]]. [[raw/omni_calle_ocho_scheduling-apr-22-2025.md]]
- **Architecture evolution (Apr 23):** on the FlexPort/SMIB/TITO meeting Pavel argued firmly for a **Linux** local TITO server over STM32/embedded (embedded is a "monolithic software block," Linux is modular/tested with more available specialists incl. himself), and won the ruling to make the **TITO server its own standalone industrial-Linux device**; he also worked the barcode-distance verification undertaking and the two POS forms. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] and [[wiki/decisions/2025-04-07-flexsmib-modern-flexport-legacy.md]]. [[raw/evolution_flex_port-apr-23-2025.md]]

## May 8 2025 — FlexPort TITO standup; partial-cash-out scoping

On the [[wiki/meetings/2025-05-08-flexport-flexpay-tito-standup.md|May-8 FlexPort standup]] Pavel ("Паша") reviewed Yavorski's action list, sequenced the MoneyOut→MoneyIn→two-machine→QA plan (QA to start Monday), and led the design discussion on the **partial cash-out** feature request (write a new requirement + feature; handle the remaining balance by printing a new ticket) and on adding **SAS-command logging to FlexPay** before the firmware-update work. Val asked "Дима и Паша" to plan the project's final delivery. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex_pay_port_hardware_update-may-8-2025.md]]

## May 12 2025 — ActiveMQ / White Area Host upgrade

On the ActiveMQ security-upgrade call ([[wiki/meetings/2025-05-12-activemq-white-area-host-upgrade.md]]) Pavel (Pasha) takes part in the live Jira product-hierarchy cleanup (moving/deleting stale items around RGS and the White Area Host) alongside Dima Chudinov and Andrei Bosik as they scope the ActiveMQ upgrade + split. See [[wiki/decisions/2025-05-12-upgrade-activemq-split-from-white-area-host.md]]. [[raw/activeMQ_upgrade-may-12-2025.md]]

## May 20 2025 — SMIB action review + test-plan philosophy

- **SMIB action-list review** ([[wiki/meetings/2025-05-20-flexport-flexpay-smib-action-review.md]]): Pavel is Val's engineering co-driver through the action list — he articulated the logging requirement (bridge all SAS commands to FlexPay), asked for **SAS-command logging before** the firmware-update work, and is made **responsible for creating separate GitHub repos per product** (SMIP/FlexPort/WSS/FlexPay) and the Bitbucket→GitHub FlexPay migration (~June 15). See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-port_flex-pay_smib_update-may-20-2025.md]]
- **Test-plan strategy** ([[wiki/meetings/2025-05-20-flexpay-flexport-test-plan.md]]): with QA lead [[wiki/people/irina-shishko.md|Irina]] (re-attributed per owner ruling 2026-07-18: QA/engineering → Shishko) and [[wiki/people/evgeniy-alekseev.md|Alekseev]], Pavel argued the FlexPay system can't be tested part-by-part and that one FlexPay software should support both schemes while each is **tested separately**. See [[wiki/topics/test-automation-strategy.md]]. [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]

## May 28 2025 — jackpot/meter call

Present ("Pasha"/"Pablo") on the jackpot-treatment call ([[wiki/meetings/2025-05-28-jp-jackpot-class3-georgia-coam.md]]) working the jackpot-limit / key-to-credit / hand-pay behaviour with Vlad Gurin, Juan and Val; he pressed the hand-pay-clearing and key-to-meter scenarios. Substance (Val's Class-3-constitution ruling) on [[wiki/projects/georgia-market-rollout.md]] and [[wiki/decisions/2025-05-28-class3-meters-constitution-georgia-parallel-logic.md]]. [[raw/jp_treatment-may-28-2025.md]]

## May 29 2025 — GitHub repos for the e-Wallet release

On the e-Wallet/TITO review ([[wiki/meetings/2025-05-29-ewallet-tito-flexpay-implementation.md]]) Pavel Frolov confirmed the **SMIB and FlexPort GitHub repos are done** (firmware incrementing, Alekseev committing artifacts); the **FlexPay Bitbucket→GitHub migration** is now targeted **~June 7** (was mid-June). He pushed for documentation (incl. SAS PDFs) to live in the repos in Markdown, and asked Chudinov to deliver his 8KB-packet change as a matter of priority rather than waiting on Yavorski. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]

## May 29 2025 — Jira Plans maturity ([[wiki/meetings/2025-05-29-jira-plans-maturity.md]])

Pavel ("Pasha") worked the Jira/GitHub maturity session with Val and Irina: he surfaced the disconnect that developers commit to **feature branches** while sprints held only stories, and (with Val) landed the split — **Jira = product domain** (capability/feature/story), **GitHub = engineering domain**. Val walked him through **enabling GitHub Issues** per repo (the "Omni LAN-based framework" repo had it off) and creating a "stale branch" issue for **FRAME-476** as a practical example, and setting up test-code → **X-Ray** linkage. Val booked a June 5 demo. See [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]] and [[wiki/topics/test-automation-strategy.md]]. [[raw/jira_plans_maturity-mat-29-2025.md]]

## May 30 2025 — FlexPay partial-payout test; QA rollout plan

- **Games-performance review** ([[wiki/meetings/2025-05-30-games-performance-review-juan.md]]): Pavel delivered new **FlexPay** software that allows a **partial payout** (keep some of the balance) and ran an informal test at Felipe's — it **failed to connect to the Incom server** (a dispenser error; Felipe left early to move house), so it wasn't a formal test. [[raw/games_performance_review_juan_martinez-may-30-2025.md]]
- **QA/rollout plan** ([[wiki/meetings/2025-05-30-qa-flexport-flexpay-plan.md]]): Pavel presented what's **completed** (money transaction to Temporary Wallet on FlexPort + FlexPay; money acceptance; Temporary Wallet issuance/calculations/validations; Incom card issuance; USB firmware update) and what's **pending** (firmware update via remote/download; WSS logging FlexPort↔FlexPay; TITO-architecture functionality; bill validators beyond **JCM UBA**). Val put **Pavel in charge of verifying the full money cycle remotely** (won't delegate it), and offered to send "one of the Evgenys" to Georgia if an on-site engineer is needed. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]

## June 10 2025 — jackpot/meter scope-gap reconvene

- On the jackpot/meter reconvene ([[wiki/meetings/2025-06-10-jackpot-meter-sas-scope-gaps.md]]) Pavel ("Pasha") took part in working the key-to-meter / jackpot-limit logic and the design question of whether to fix it once (independent, higher-settable key-to-meter + partial transfer) under proper Class-3-then-Georgia logic. See [[wiki/projects/georgia-market-rollout.md]]. [[raw/meter_sas_function-june-10-2025.md]]

## June 12 2025 — Omni schedule review + QA direction review

- **Omni schedule (7 am)** ([[wiki/meetings/2025-06-12-omni-schedule-review.md]]): Pavel ("Паша") ran the LGS feature walkthrough with Sasha and Kharetsky, tracking Game History / Game State / PayTable / LED features and reassigning **LGS 474 (LED)** to [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] to parallelize; he also managed the backlog pruning (cutting the likely-obsolete LGS 12 / DESAP task). See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/schedule_review_omni-june-12-2025.md]]
- **QA direction review** ([[wiki/meetings/2025-06-12-qa-engineering-direction-aaron.md]]): present as the dev-side lead; he argued for **keeping tests with the code they test** (UI tests in the UI repo, LGS tests in the LGS repo) — which would force LGS tests into Java — versus Anton's single cross-cutting framework (left unresolved), and noted the developers are "quite ahead of QA in development." See [[wiki/topics/test-automation-strategy.md]]. [[raw/qa_engineering_direction_review_aaron-june-12-2025.md]]

## June 18–19 2025 — the FlexPOS / GA-COAM redemption architecture

- On the [[wiki/meetings/2025-06-18-gcoam-ticket-redemption-workflow.md|June-18 ticket-redemption session]] Pavel (rendered "Pavel" and "Pablo") was the engineering voice on the Tito/Mother-Goose redemption workflow — the barcode-only Tito validation, the SMIB-vs-FlexPort retrofit by SAS-port count, and the parallel-printer Mutagoose POS wedge. [[raw/about_tickets_redemption-gcoam-june-18–2025.md]]
- On the [[wiki/meetings/2025-06-19-flex-pos-use-case-design.md|June-19 Flex POS session]] Pavel authored the **FlexPOS Mutagoose capabilities** doc (committed to the FlexPOS repo docs; 10-inch touchscreen + magnetic reader; setup/work modes), raised the **device-security** requirement (PIN / QR / magnetic card / per-day PIN), specified the **Incom three-call API** (authenticate → pre-authorize → issue), and used **Mermaid** diagrams for the POS Mutable schema. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/flex_POS-use_case_architecture_requirements-june-19-2025.md]] [[raw/flex-POS_design-june-19-2025.md]]

## June 23 & 26 2025 — InComm alignment; Omni grooming (topper, FP-7)

- **Jun 23 (InComm):** the JVL technical voice on the [[wiki/meetings/2025-06-23-incomm-jvl-nebraska-georgia-alignment.md|InComm alignment call]] — probed the card **dispensing** details (magnetic-stripe read at dispensing vs barcode on POS/tower; whether a SkillPay card needs a barcode or magnetic validation) and the **manual-activation / per-machine terminal registration** questions. See [[wiki/organizations/incom.md]]. [[raw/incomm_jvl_alignment-june-23-2025.md]]
- **Jun 26 (Omni grooming):** ran the [[wiki/meetings/2025-06-26-omni-schedule-grooming.md|Omni schedule grooming]] — walked the backlog/task reshuffle, presented the **topper-as-separate-application** benefits (deterministic main game, independent horse-racing, future linked-progressive, no re-cert), owns the **mass-engine Docker/math integration** and the **production image** (no simple-password access, no exposed ports), and is to talk to [[wiki/people/genadi-peari.md|Genadi]] about preparing new **FP-7 boards** for the Omni-on-FP-7 migration. Restated Val's push to move story-level planning to GitHub Issues + Kanban. See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/OMNI_schedule_grooming-june-26-2025.md]]

## ~July 14–15 2025 — OMNI schedule review + alignment-planning catch-up

- **OMNI schedule review** (with Val + [[wiki/people/alexander-biratka.md|Alexander Biratko]]): Pavel drove the Jira-plans walkthrough — the VDEC/bonus-scene status, handing the bonus to [[wiki/people/ihar-hrybko.md|Igor Hrybko]] since Anton is on Nebraska, the untested progressive spinner, keeping the old LGS UI, and splitting the Omni Gaming Platform into land-based/online/core. See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/OMNI schedule review.md]]
- **Alignment-planning catch-up** (with Val + [[wiki/people/irina-shishko.md|Irina Shishko]]): Pavel argued the **POS hardware-platform / "harbor"** tradeoffs — a ready board vs a module on JVL's own board vs the current platform (~$50/$60/$80), keep dev in-house for now, and **Linux beats embedded** for internet-facing security (ready SSL/NTP libraries). He also detailed the **PixiJS v6→v8 video-decode regression** (11 → ~2 parallel videos) as a framework blocker. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] and [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/alignment-planning-catch-up.md]]

## Jul 29–31 2025 — transactional-architecture arc + amusement-games framework

- **Jul 29 / Jul 31 transactional-architecture deep-dive** (with Val, Nathan, Juan, Genadi): Pavel argued the processing/server application should run as **software on any device** (kiosk/POS) with **Flexports as slave devices**; backed the move from clustering to **event-driven message-queue replication**; and named the on-device **tech stack — Linux / MySQL / Java / React**. He preferred cloud snapshots + never-delete over Val's weekly-overwrite retention rule. Full substance: [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/Transactional-Architecture-Discussion-2025-07-29.md]] [[raw/transactional_architecture-july-31-2025.md]]
- **Jul 31 amusement-games revival** (with Val): Pavel worked the engineering side of reviving the legacy C++ amusement games — old Rage-Studio format unrecoverable; rebuild on **Pixi** (works with JVL designers' scenes) + Miranda scenes; a **TypeScript** programmer per game; an "open-as-a-platform" API kit (would pull in [[wiki/people/alexander-biratka.md|Sasha]]); x86-vs-ARM platform; the platform **can't be made cheaper** (tied to the motherboard). See [[wiki/topics/amusement-games-revival.md]]. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]

## Aug 2025 — Flex-POS iteration + backend-architecture kickoff

- **Aug 6 Flex-POS sync + Prize-Card chat:** on the [[wiki/meetings/2025-08-06-flex-pos-mid-iteration-sync.md|mid-iteration sync]] Pavel drove the point that the capability set is Mother-Goose-schema-specific and a Tito/e-wallet POS will differ, and that Tito vs e-wallet tickets differ (one carries a value, one doesn't) — motivating the split of ticket data schemas into separate folders. In the same-day Prize-Card thread he raised the barcode-vs-magnetic-stripe card-format question (leaning to a swipe reader on Flex-Port, later dropped once John confirmed barcodes). See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/2025-08-06_Flex-POS-Mid-Iteration-Sync.md]] [[raw/Flex-Port-use_case-August-6-2025.md]]
- **Aug 14 backend-architecture kickoff** ([[wiki/meetings/2025-08-14-backend-architecture-cms-transactional-hhr.md]]): Pavel argued it is **easier to start new development for the transactional product** on a new server (independent of existing machines); identified the **common reusable modules** (passport, RIS, lease, user/operator/location management, analytics/reporting); called for a **separate cloud payment-processing server** living independently of the orchestration platform; described the on-location **master/slave** device model; and flagged that **automatic device-to-location assignment isn't reliable without a confirmation step**. He reframed the effort as **capabilities-driven** and noted much CMS documentation sits on obsolete Confluence pages. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] and [[wiki/decisions/2025-08-14-backend-architecture-block-diagram-first-mvp.md]]. [[raw/backend_architecture-august-14-2025.md]]
- **Aug 20 CMS/PayFlex block-diagram review** ([[wiki/meetings/2025-08-20-cms-payflex-block-diagram.md]], session 1 of 3): Pavel gave the engineering picture — the legacy CMS **Flexpay Manager** tab (kiosk key/lease-date/software-version/MAC/status; the internal JVL admin screen he built), remote access limited to a **WSS API + log retrieval** to the on-location master device, and future **firmware-update push** (FlexPort/FlexMIB). He proposed the **new CMS as a separate cloud server** starting from payment-terminal management (device dashboard + per-operator client portal), the legacy SQL CMS kept in parallel with selective export/import, and a protocol-stability approach (never-change or add-only endpoints). He explained **Passport** (hardware+firmware fingerprint validation) and confirmed the Flex-POS moves to an **ARM CPU**. He undertook to prepare current-implementation schematics (Miro-board exports) for the next session. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] and [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/CMS- Block Diagram_Arch.md]]

## Sept 2025 — cashier-admin staging, hardware-board defence, top-level architecture method

- **Sept 3** ([[wiki/meetings/2025-09-03-flex-capabilities-weekly-ach-dispute-pos-design.md]]): laid out **staged cashier login/PIN administration** — stage 1 (by Jan 1) creates PIN codes centrally on the server and assigns them to a POS/location; later stages use a location admin magnetic card or an operator-mobile-generated admin QR/barcode; credentials attach to the **location, not the device**, so a hot-swapped device pulls settings from the server. Also flagged only **3 of many InComm API endpoints are enabled** for JVL's gift-card types. See [[wiki/organizations/incom.md]] (Sept-3). [[raw/Flex Capabilities Weekly Update-september-3-2025.md]]
- **Sept 9 (top-level architecture, 2:41 PM)** ([[wiki/meetings/2025-09-09-top-level-backend-architecture.md]], with Val): proposed the ~6-month phasing — a near-independent **cloud InComm payment hub** first, **extend the legacy Flexpay/Flex-POS dashboard** to register Flex-POS for Jan-1, new architecture built in parallel — and taught Val the requirements→block-diagram→decompose method. Undertook to stand up a **repository** then produce a **top-level block diagram**; Tuesday ~4 PM follow-up booked. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Sept-9). [[raw/top_level_architecture_back-end-september-9-2025.md]]
- **Sept 9 (POS spatial, 3:18 PM)** ([[wiki/meetings/2025-09-09-pos-spatial-hardware-board-planning.md]], with Genadi): defended the **main-board + cheap interface-board** split against full one-board consolidation; floated **LVDS daisy-chain / dual-mode** to drive both monitors off one connector (a Rockchip/Alekseev question). [[raw/POS_spatial_planning-september-9-2025.md]]
- **Sept 10 (fast-pacing alignment stand-up, 3:31 PM)** ([[wiki/meetings/2025-09-10-fast-pacing-alignment-standup.md]], with Val; the **series opener**): gave the dev status pass — new auto-tester (Playwright vs Selenium) working with Anton; Nebraska/Texas release slipped a couple days; **Evgeniy Yavorski** promised his first update; the **payment-hub architecture** (independent Amazon-deployable cloud app; FlexPay to be re-pointed *through* the hub, not directly to InComm) with a Tuesday top-level-view review. Received Val's directive that Pavel + [[wiki/people/irina-shishko.md|Irina]] institute **spec-driven development** — the spec as the developer↔QA "touchstone" in the branch, "reverse Omni" into a spec, tests written per spec, via recorded 2-hour module-walk sessions turned into specs by AI. See [[wiki/topics/test-automation-strategy.md]] (Sept-10). [[raw/fast-passing-general-alignment_stand-up-september-10-2025.md]]
- **Sept 16 (payment-hub blueprint review, 1:03 PM)** ([[wiki/meetings/2025-09-16-backend-blueprint-payment-hub-review.md]], with Val + Nathan + Aaron, English): presented the CMS/Flex-POS blueprint and drove the payment-hub build — extend the legacy **Flexpay Manager** GUI to configure Flex-POS, move terminal→InComm comms into a cloud **payment hub**, config bound to location not terminal. Set the tech stack with Nathan — **Java** API service + **Postgres**, ACH API not a blocking dependency ("we can do anything using Java"). Undertook the deeper payment-hub architecture (with "Dima"/[[wiki/people/dmitri-chudinov.md|Chudinov]]) then the payment-hub↔terminal and payment-hub↔control-server APIs; a Monday spec session booked. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Sept-16). [[raw/back-end_architecture_blueprint_review.md]]

- **Sept 22 (specification-standards review, 12:06 PM)** ([[wiki/meetings/2025-09-22-specification-standards-review-aaron.md]], with Val + Aaron, English): proposed starting specs with Flex POS + payment hub; Val overruled — **Omni first**. Pavel is made **leader/mediator of the improvised Omni-spec working group** ("Lena Cima" [garbled] / [[wiki/people/irina-shishko.md|Irina]] / Pavel, as the missing product owner): explains "the rules of the game," enforces written-first collaboration, mediates rather than participates. Weighed two spec scopes (framework-only → few tests; whole EGM-on-FP7 → end-to-end tests). Runs this week's recorded [[wiki/people/alexander-biratka.md|Sasha]] interviews (raw transcript kept in git, un-AI-processed); owes Val a short calendar. See [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]] (Sept-22). [[raw/specification_standards_review-september-22-2025.md]]

## Oct 8 2025 — Flex capabilities weekly (Dwolla onto the dev path)

On the [[wiki/meetings/2025-10-08-flex-capabilities-ach-vendors-fednow.md|Oct-8 Flex capabilities weekly]] (12:05 PM, with Nathan + Val) Pavel was the engineering voice as [[wiki/people/nathan-carver.md|Nathan]] walked the ACH vendor-readiness table. He confirmed the payment-hub Jira schedule — **IP632** (~9 features, into early December), the **ACH API adapter (BEP 2656)** where Dwolla fits, a rough ~2-week integration finishing **~Nov 12** (caveat: Dwolla API docs not yet read, so the estimate is rough) — and that the **Spring Boot** job scheduler Nathan needs is already in the Java tech stack. Took the joint undertaking with Nathan to schedule the Dwolla integration in Jira. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Oct-8). [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]

## Nov 5 2025 — Dwolla onboarding kickoff (sandbox → production)

On the [[wiki/meetings/2025-11-05-jvl-dwolla-onboarding-kickoff.md|Nov-5 Dwolla kickoff]] Pavel was the JVL engineering lead learning the platform hands-on: he had already worked out (via API, ~10 minutes before the call) how to create/verify customers in the sandbox, and drove the practical questions — one JVL bank account to receive funds vs many location customers to debit; whether all locations must be created in the list. Dwolla clarified JVL uses the **unverified customer** object (created via API, not the dashboard), with a **verified bank funding source**, on the **receive flow**. Nancy will consolidate JVL's **5 separate sandbox accounts** onto one admin (Pavel) with a shared API key. This is the vendor-facing follow-through of the Oct-8/22 decision to build on Dwolla. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Nov-5). [[raw/JVL_Dwolla-november-5-2025.md]]

## Nov 5–10 2025 — payment-hub ACH-spec-review arc (named driver)

Across the three ~7 AM ACH-module spec-review sessions ([[wiki/meetings/2025-11-05-payment-hub-ach-spec-review-states-provider-routing.md|Nov-5]], [[wiki/meetings/2025-11-06-payment-hub-ach-spec-review-registration-onboarding.md|Nov-6]], [[wiki/meetings/2025-11-10-payment-hub-ach-spec-review-undertakings-plaid-qa.md|Nov-10]]) Pavel drove the screen-share and the requirement walk-through — provider routing (one adapter at a time but two in parallel during a switch), the passport-vs-terminal registration split, the funding-source-ID money model (no Dwolla wallet, in his read), and the location-onboarding/web-interface design. On Nov-10 Val named him the **driver** of these meetings ("it's your bulldozer now") and asked him to run the AI-undertakings meeting-prep discipline. Substance on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Nov 5–10 ACH-spec arc). [[raw/Payment HUB_ACH module specification_05.11.25 .md]] [[raw/Payment HUB_ACH module specification_06.11.25.md]] [[raw/Payment HUB_ACH module specification_10.11.25.md]]

## Feb 3–4 2026 — Claude Code rollout (architectural voice; excused from the figma sessions)

- **Feb 3 (Claude Code workshop).** On the [[wiki/meetings/2026-02-03-claude-code-integration-continued.md|Feb-3 session]] Pavel gave the substantive engineering push-back — in the **whiteboard-photo debate** he argued the original photo may be safer than a pre-digested version (you can lose information processing it), and he reframed Aaron's "intentions" as **business requirements** that translate into architectural-decision requirements and tasks. [[raw/Claude Code integration - continued.md]]
- **Feb 4 (figma→React).** On the [[wiki/meetings/2026-02-04-figma-react-export-workflow.md|Feb-4 session]] Pavel gave the architectural read on the figma→React pipeline (partial automation only — no business logic / data-binding in Figma yet; component-kit frameworks React may not know; AI can propose back-end correspondence/improvements once it sees the implementation). Val **deliberately keeps Pavel out of these figma working meetings** to reduce his load ("я специально вас на эти митинги не приглашаю… избавить вас от этого"); Pavel: "if interested, I'll watch the video" — continuing the Aug-2025 "narrow Pavel to a tighter box" theme. See [[wiki/topics/test-automation-strategy.md]] (Feb-4). [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]

## Feb 6 2026 — engineering read on RIS modernization

On the [[wiki/meetings/2026-02-06-ris-modernization-operator-flexibility.md|Feb-6 RIS modernization meeting]] Pavel gave the engineering assessment (substance on [[wiki/topics/ris-remote-install-and-machine-states.md]]):

- A **full manual mode** (entering every screen by hand) "will be very difficult and long a project"; the cheap path is to keep the **same RIS screens** and **enable editing on a small set of top fields** (e.g. progressive value, RTP per game). He and Val converged on a **flexible flag marking which screens are editable vs locked**. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- He raised the **sold-machine lease dilemma**: issue the lease **per machine** (a new software install then needs a new lease) or **per machine for any software until ~2029** — "a dilemma," not resolved. He also flagged that for a new owner to change settings without a manual mode, they'd need **access to JVL's cloud/server areas**. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- On reinitialisation after a **RAM clear**, he confirmed the machine's irrevocable ID relates to the **Dallas one-wire "cube" that holds the passport information** on the CPU board — the anchor that lets JVL restore a machine only to the state it was officially sold at. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]

## Feb 9 2026 — Claude Code onboarding (translator) + Val's "intelligence center" mandate

- On [[wiki/people/dmitri-chudinov.md|Chudinov]]'s Claude Code onboarding ([[wiki/meetings/2026-02-09-claude-code-onboarding-chudinov.md]], 1h46m) Pavel was the English↔Russian translator between [[wiki/people/aaron.md|Aaron]] and Chudinov, and endorsed the "one more layer of abstraction" framing. Val gave him a durable **corporate mandate**: build and **own** an "intelligence center" — an intelligent system sitting on top of every developer's and designer's GitHub giving a **daily per-person productivity summary** ("put out my tentacles into everybody's GitHub"); Val is building it so he can "step aside while the company functions." Val told him these Aaron sessions must become **Pavel's** meetings — he schedules them, keeps them efficient, cuts them toward **half an hour**, drives the agreed items, and identifies one or two engineering **leaders**. Substance on [[wiki/topics/ai-assisted-development.md]] (Feb-9). [[raw/Claude_Code-Dzmitry.md]]
- In the same-day internal debrief ([[wiki/meetings/2026-02-09-claude-code-chudinov-internal-debrief.md]], 12m, no Aaron) Val directed Pavel to lean **less** on the expensive Aaron consultation — split internal coaching between Chudinov and [[wiki/people/alexander-biratka.md|Biratka]], involve Andrei and Bosik, use a cheaper AI for dilemmas, define his own "ways," and build his own GitHub-monitoring tool; next meeting set for the 16th, 9:15–10:00. [[raw/Claude_Code-Dzmitry (1).md]]

## Feb 11 2026 — GitHub front-end Waze setup (translator/lead)

On the [[wiki/meetings/2026-02-11-github-front-end-waze-setup.md|Feb-11 front-end Waze session]] Pavel was Aaron's English↔Russian translator and steered the front-end team ([[wiki/people/anton-seregin.md|Seregin]], [[wiki/people/vladimir-samusenko.md|Samusenko]]) through the compiler-stack / ways teaching, then **left partway** to help translate for another team. He is responsible for making sure the developers get the ongoing updated Waze version and relayed [[wiki/people/evgeny-kharetski.md|Evgeniy Kharetski]]'s question about ways-versioning. He also described the current front-end work: Vladimir transferring the old machine-setup design to the new Figma design, Anton building the **Flex POS** server-part / registration / location-management front end. Substance on [[wiki/topics/ai-assisted-development.md]] (Feb-11). [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md]] [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md]]

## Feb 12 2026 — Genadi's JIRA-task partner; owner of the memory-adapter fix

On the two Feb-12 [[wiki/people/genadi-peari.md|Genadi Peari]] calls:
- Val wants **Genadi to write his JIRA tasks with Pavel**, using the recorded-conversation → AI-drafts-the-tasks method Val says "I and Pavel and Irina found" (talk it through, draft, correct, finalize, then have Claude open the tasks in Jira — "Pavel is excellent at this already"). [[raw/Call_Genadi_Peari-February-12-2026-1.md]]
- On the memory-adapter design decision (mount the SD as SATA, never through a PCIe adapter), Val will email the transcript to **Pavel** (and Pyramid + Ivan) to open a ticket, and **Pavel is to spec/implement the small Linux change** so the device is read as SATA. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Feb-12). [[raw/Call_Genadi_Peari-February-12-2026-2.md]]

## Feb 26 2026 — Flex-dispenser JIRA planning (runs it; owns the FP-505 rework)

On two same-day calls with Val and [[wiki/people/genadi-peari.md|Genadi Peari]] ([[wiki/meetings/2026-02-26-tasks-planning-alignment.md]] 2:35pm, [[wiki/meetings/2026-02-26-jira-planning-flex-dispenser.md]] 3:18pm) Pavel ran the JIRA housekeeping and the software-side planning for the Fujitsu-dispenser Flex device:

- Set the anti-sprawl discipline Val endorsed 100%: when a v1 becomes a **v2**, open a **new task** (~2 weeks out) rather than stretch the original. [[raw/tasks_planning_alignment-February-26-2026.md]]
- Worked the e-wallet-generation constraint — FlexPay is the money-carrier, and a machine "prints its own ticket and knows nothing about the e-wallet format," so a FlexPort in the machine can't make it print an e-wallet; the loop only closes by generating the e-wallet **in the kiosk** with a bill acceptor added. Substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Feb-26). [[raw/JIRA_Planning-February-26-2026.md]]
- Took ownership (Val: "I think you should take this on") of reworking feature **FP 505** — strip every "pyramid style redemption" reference from its description and name, re-specify it for the market using **FlexPort** — plus breaking down **IP 1014** and its stale/duplicate tasks, writing the missing stories under IP 1007/1014, and building a **JIRA filter on IP 1007 + IP 1014** for Val to review the next morning. He noted Claude "worked very badly with Jira" the day before (see [[wiki/topics/ai-assisted-development.md]] Feb-26). Tracked as an open commitment on the FlexPay topic. [[raw/JIRA_Planning-February-26-2026.md]]

## Feb 27 2026 — Nebraska release-schedule call (owns the features + sprint scheduling)

On the [[wiki/meetings/2026-02-27-nebraska-release-schedule.md|Feb-27 1:02pm Nebraska schedule call]] (with Val, Juan, [[wiki/people/irina-shishko.md|Irina Shishko]]) Pavel is the engineering owner of turning the three Nebraska requirements into work. [[raw/Schedule_Nebraska-February-27-2026.md]]

- **Explained the requirements→features workflow** to Val (who saw "two parallel inventories"): a published requirement isn't worked until someone creates a **feature** and schedules **stories** under it, linked via the "linked work item" field — "in many cases, me." Confirmed Claude could create a feature from a well-written requirement. See [[wiki/topics/ai-assisted-development.md]] (Feb-27). [[raw/Schedule_Nebraska-February-27-2026.md]]
- **Marching orders:** create the Jira features linked to REQ-998 / 1007 / 1010, schedule them into the **next sprint (starting Thursday)**, and complete development within that cycle so JVL can rush the Eclipse approval. Handled the audit-ticket UI design (a separate attendant-screen pop-up, distinct from the game pop-ups) and worked the whole-dollar-rounding + last-bet-risk behaviour with Juan and Irina. See [[wiki/projects/nebraska-skill-market.md]] (Feb-27). [[raw/Schedule_Nebraska-February-27-2026.md]]

## Mar 4 2026 — schedule review (runs it; picks Biratka; kanban advocate)

On the [[wiki/meetings/2026-03-04-schedule-review.md|Mar-4 schedule review]] (with Val and [[wiki/people/irina-shishko.md|Irina Shishko]]) Pavel ran the Minsk board walk-through. [[raw/Schedule_review-March-4-2026.md]]

- **Picked [[wiki/people/alexander-biratka.md|Sasha Biratka]] to take over [[wiki/people/eugine-yavorski.md|Yavorski]]'s FlexPort application (IP 10-13)** over [[wiki/people/dmitri-chudinov.md|Dima Chudinov]] — Chudinov is stretched across the Flex-Q terminal and server-side services and shouldn't be redirected for a month; Sasha is finishing the cash-dispenser task (~1–2 weeks) and can then pick it up. [[raw/Schedule_review-March-4-2026.md]]
- **Advocated moving from sprints to kanban** — JVL's sprints are never ideal because urgent unplannable tasks always bump planned work; kanban absorbs the churn. Action: talk to [[wiki/people/dmitri-kovalchuk.md|Dima Kovalchuk]] about reconfiguring the Jira board (sprint→kanban) and about the feature→GitHub-branch link field. See [[wiki/topics/github-release-management-pipeline.md]] (Mar-4). [[raw/Schedule_review-March-4-2026.md]]

## Mar 5 2026 — Nebraska release schedule review (attends the JIRA walk-through, leaves early)

On the [[wiki/meetings/2026-03-05-nebraska-schedule-review.md|Mar-5 4:13pm Nebraska schedule review]] (Russian; with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/irina-shishko.md|Irina Shishko]]) Pavel ("Pasha") is the "+1 other" on the recording — he walks Val through where features live in JIRA (core / game-production / application) and how tasks are linked, then **leaves partway through** ("мне надо убегать") to another commitment, handing the remaining walkthrough to Irina. As the engineering owner he is where the Nebraska feature/story assignments land (dual box → Yulia, then Anton's implementation story). See [[wiki/projects/nebraska-skill-market.md]] (Mar-5). [[raw/Schedule_review_Nebraska-March-5-2026.md]]

## Mar 5 2026 — the North America ↔ Minsk communication breakdown (with Val)

On a Mar-5 exchange with [[wiki/people/val-levitan.md|Val]] about the North-America↔Minsk feedback problem, Pavel largely **agreed with the diagnosis** but added important context: on genuinely contentious issues Minsk does not stay silent (it initiates live meetings), and roughly **90% of decisions on services and the GUI went through Val, Juan and the team over several iterations** — so two-way dialogue exists but is not systematic. He reframed the structure: feedback loops **do** exist but are **fragmented by level** (an executive loop; developer/QA/Pavel-Irina loops) with signals travelling poorly between segments in a hierarchical model that filters at each layer. He conceded the sharpest gap is **architectural decisions percolated in Minsk being usually undocumented**, and that small local decisions accumulate into changes later read as deviations from requirements. He expressed genuine willingness to improve and simplify processes and add transparency. Full substance on [[wiki/topics/minsk-team-communication.md]]. See [[wiki/meetings/2026-03-05-communication-breakdown-minsk.md]]. §15.8 clear. [[raw/communication_break_down_Minsk-March-5-2026.md]] [[raw/Mutual_standing-Communication_breakdown_Minsk.md]]

## Mar 26 2026 — Initiative Priority Schedule (owns the kernel + freeze fix)

On the two-segment [[wiki/meetings/2026-03-26-initiative-priority-schedule.md|Initiative Priority Schedule]] meeting (with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/irina-shishko.md|Irina Shishko]]) Pavel is the engineering owner: he **reproduced the machine freeze** with a deliberate kernel-hang function (always a kernel crash / hung screen), diagnosed likely **GPU-related kernel bugs** in the current 4.19 kernel, and argued for the **kernel-panic auto-reboot parameter (Option 4)** plus the shipped CPU watchdog over an external watchdog chip (Option 2 — differs per board revision, edge-case-prone). He owns the **kernel 5.15 build**, config-parameter tuning and integration (~2–3 days build + up to ~2 weeks testing), with [[wiki/people/andrey-bosik.md|Andrey Bosik]] mirroring the kernel sources to GitHub in parallel. He also drove the Maple-refit engineering (buy 2 test TVs locally). See [[wiki/topics/github-release-management-pipeline.md]] (Mar-26) and the dedicated [[wiki/topics/egm-freezing-investigation.md]] (Pavel is the lead engineer across the Mar-9→13 investigation). [[raw/Meeting_Transcript_initiative_priority_schedule-1-March-26-2026.md]] [[raw/Meeting_Transcript_initiative_priority_schedule-2-March-26-2026.md]] [[raw/Meeting_Notes_initiative_priority_schedule-March-26-2026.md]]

## Mar 27 2026 — Review of Engineering Guides + the OMNI Architecture Challenge call

Pavel attended the [[wiki/meetings/2026-03-27-review-of-engineering-guides.md|Review of Engineering Guides]] (11:02am, with Val, [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] and [[wiki/people/andrey-bosik.md|Andrei Bosik]]): he raised the ADR-vs-requirement trigger question (ADRs will drive ~80–90% of feature creation), proposed the practical Jira restructure (rename Initiatives→Products, Products→Capability Tickets to preserve links rather than inserting a level and breaking ~1,700 relationships), argued to keep audio off GitHub (text transcripts only) and to move onboarding out of the per-project guide, and — crucially — was given the undertaking to **document the current OMNI system architecture** (only he has the depth) as the foundation ADRs will build on (~April 10). Then on the immediately-following [[wiki/meetings/2026-03-27-omni-architecture-challenge.md|OMNI Architecture Challenge]] call (1:58pm, one-on-one with Val) he heard Val's TypeScript/JavaScript + Rust stack proposal (accepting TS/JS, flagging the HAL-in-Rust rewrite as "a big piece of work"), reported his partly-done two-week sprint sketch (Linux 5.15 tasks in Jira), agreed Ira should own the Maple Jira Features, and requested ~6 days' vacation in early May. Substance on [[wiki/topics/ai-assisted-development.md]] + [[wiki/topics/omni-core-advancement-and-game-templating.md]] (Mar-27). [[raw/Meeting_Transcript_Review_of_Engineering_Guides-March-27-2026.md]] [[raw/Meeting_Transcript_OMNI_Architecture_Challenge-March-27-2026.md]]

## Apr 15 2026 — Flex POS Alpha-1 status + HAL microservicing; asked to author the OMNI 2 outcome statement

On the [[wiki/meetings/2026-04-15-flex-pos-alpha-and-omni-2-architecture.md|Flex POS Alpha & OMNI 2 alignment]] (with Val and [[wiki/people/irina-shishko.md|Irina]]) Pavel reported Flex POS device-side near **Alpha-1** on the ARC 35-68 board (SDK/dev-infra now in git as IP 977; speakers + top-light still open), proposed splitting the monolithic **HAL into per-device microservices** (Step 1 in C, Step 2 Rust later), filed **HFM-532** (wireless interfaces support), and raised the Minsk dispenser/recycler logistics and the **Flex Pay ICOM → ICOM-in-cloud** refactor. Val tasked him to write a desired-outcome statement for **OMNI 2** and to lead the architecture-first design loop (with Lishkevich, Metelsky, Khoretsky). Substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] + [[wiki/topics/omni-core-advancement-and-game-templating.md]] (Apr-15). [[raw/Meeting_Notes_Flex_POS_Alpha_and_OMNI_2_Architecture-April-15-2026.md]]

## Aug 18 2026 — RAGE→NOVA experiment review: Rust services momentum

On the [[wiki/meetings/2026-08-18-rage-nova-migration-experiment-review.md|Aug-18 review]] Pavel ran the meeting, reported that [[wiki/people/anton-leshkevich.md|Anton (Lishkevich)]] had **rewritten the printer service and build validator in Rust** and tested the printer, and worked the math-container packaging question with [[wiki/people/efim-podvoiski.md|Efim]] and [[wiki/people/evgeny-kharetski.md|Evgeny]] (build the container from a game list at the integration-build step — [[wiki/decisions/2026-08-18-nova-math-container-per-game-set.md]]). He agreed to **send Val the Rust services** Anton built. See [[wiki/topics/nova-platform-architecture.md]] (Aug-18). [[raw/Meeting_Notes_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]] [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]

## Aug 24 2026 — two sessions in one morning: the prose-standard checkpoint, then the Flex-Port-Mini design

Pavel was in both Aug-24 meetings — the [[wiki/meetings/2026-08-24-nova-lgs-prose-standard-checkpoint.md|8:42 AM prose checkpoint]] and the [[wiki/meetings/2026-08-24-flex-port-mini-capabilities.md|10:06 AM Flex-Port-Mini design session]] (both Russian).

**Prose checkpoint.** [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]] [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **He supplied the enforcement mechanism the group adopted.** On making the no-prose-no-commit rule real: "Мы, мы можем кормить, но мы не можем пьер сделать" — you can commit, but you cannot open the pull request. Val: "мне кажется то, что Павел предложил… Окей да, Я согласен"; Irina agreed too. See [[wiki/topics/github-release-management-pipeline.md]] (Aug-24).
- **He fixed the prose folder location:** "эта папка dox слэш проус… во всех проектах в папке док лежал папка проус и всё," with substructure following the project's modules; Val agreed. He gave the working definition of prose that Val endorsed: "это повествовательное, какоето написание, описание функционала."
- **He drew the planning consequence of the capability/requirement split:** "без копобилите мы не можем фичи отобразить на плане, а без регламентов можем."
- **He proposed reassigning the backend/CMS prose to [[wiki/people/sergey-tsymanov.md|Sergey Tsimanov]]** (back from vacation), noting [[wiki/people/anton-seregin.md|Anton Seregin]] had written prose and capabilities from the graphical-user-interface side, and asked that the prose Val gave [[wiki/people/dmitri-chudinov.md|Dima Chudinov]] be verified against the current code.
- He also endorsed widening the standard's authorship: "чем больше людей здесь скажут свои замечания, тем лучше," and defended the exercise on the bug-finding evidence alone: "как минимум уже по этой причине мы не зря делали прозу."

**Flex-Port-Mini design.** [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- **He identified the wiring that the 2nd-SAS-only design removes** as "самая проблемная часть здесь" — the most problematic part — and explained the current in-line bill-acceptor connection uses two RS-232 converters that "в принципе да ничего не стоят."
- **He argued for the PIN, lost, and named the residual risk** (a copied barcode used before the real player arrives) — see [[wiki/decisions/2026-08-24-drop-pin-from-evoucher-flow.md]].
- **He contributed the QR-carries-a-server-URL idea** so scanning registers the transaction centrally, plus per-location promo credits that are playable but not withdrawable — accepted by Val as "очень очень важно."
- **He owns the networking problem.** He established that a local validation server is unavoidable ("у нас должен быть локальный сервер… Чтобы иметь единую систему валидации"), that WSS will not run over daisy-chained RS-485 ("там будет уже какойнибудь протокол типа модбас") and would need an encryption layer, that an RS-485 chain breaks entirely on any break or unpowered node, and that a per-port LTE modem costs at least $15. He raised **Bluetooth mesh** for reliability while conceding "мы с этим никогда не работали" and "Нет никаких идей, как это оценить даже," and cited having read that certain Chinese chips use a protocol he recalled as **ESP-NOW** with ~500 m line of sight.
- **He recommended wires for launch:** "провода самый надежный способ, конечно, здесь может быть нам пока пойти с проводами даже для запуска всего," with mesh as a later experiment.
- **He argued against cooperating with Mutha Goose at all** — "Нам лучше с ним не кооперироваться вообще" — because JVL's own board over SAS is more reliable than the electromagnetic-counter cash-in/cash-out signals, which are "очень ненадёжны по сравнению с тем, что сас нам даёт."
- **He also floated the stage-2 mobile-cashier-app idea** that would drop Flex IQ entirely, and then named its cost trap (a modem in every SMIB board) — see [[wiki/decisions/2026-08-24-free-hardware-fixed-monthly-fee-model.md]].
- One analogy he offered was rejected: comparing the flow to "эти пирамидовские принтеры" (Pyramid printers) with their QR-validating app — Val: "Нет, это нет. Пирамидовские принтеры, не так."

## Aug 26 2026 — the arithmetic correction, the peak-hour alternative, and the recycler reverse-engineering problem

On the [[wiki/meetings/2026-08-26-alignment-planning-nova-september-releases.md|Aug-26 alignment call]] (Russian) Val handed Pavel and [[wiki/people/irina-shishko.md|Irina]] joint ownership of the September capabilities→MVP→Jira work — [[wiki/decisions/2026-08-26-pavel-irina-own-nova-capabilities-to-jira-through-september.md]]. Pavel's own contributions on the call: [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

- **He corrected Val's per-spin arithmetic on the spot.** Val had said JVL loses about 25¢ per spin on a 25¢ bet; Pavel: "нам надо для потери ноль 25 умножить на единица минус RTP, то есть на самом деле не ноль 25 мы теряем 0,025, то есть 2 с половиной цента." Detail on [[wiki/topics/slot-game-design-principles.md]] (Aug-26). [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **He offered the alternative to Val's location-based RTP plan:** rather than geo-fencing the RTP and the minimum bet, "Просто в часы пик блокировать. Ну то есть не показывать самую минимальную кнопку" — hide/disable the lowest bet button during peak hours. Irina noted it is new functionality; Val liked it ("который мне очень нравится") but parked both options for the game-design team. [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **He owns the new-recycler problem and expects to repeat the ARM reverse-engineering.** He had spoken to [[wiki/people/genadi-peari.md|Genadi]] the day before about the larger CPI unit — "это какойто b nr или BNP помоему модель BNR" — and Genadi had already said "это будет несовместим с нашей библиотекой," with the vendor promising the needed library. Pavel told him to order it shipped straight to Minsk. His precedent: on the ARM platform "Мы полностью переписали то, что они нам прислали… Полностью сделали реверс инжиниринг," so "нам готового решения не будет." He added that reverse engineering with Claude "идёт быстро и его легко… Проверять," but "Проблема удалённо с этим сложно работать" — putting a person next to the device to insert bills and count notes is possible but is "лишний человек… Робота у нас нету удалённого." Detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Aug-26). [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **He named the constraint on running the two NOVA migration tracks in parallel:** not the developers — "С точки зрения fronbork и разработчиков то да" — but "как нам распараллели эти ресурсы QA," and the fact that designers would have to support the same game on both vertical and horizontal cabinets. [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **He proposed the Minsk emulation of the Light & Wonder SAS / player-tracking system** and the direct Georgia ↔ Minsk network link (see below and [[wiki/topics/minsk-team-communication.md]], Aug-26). [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- **On the succession gap he was blunt about the limits of the internal bench:** asked whether anyone can push submissions the way [[wiki/people/juan-martinez.md|Juan]] does, "Ну нет, у нас исполнители здесь в этом плане" — we are executors in that respect — and he thought a business-side successor would have to come from the gaming-machine business. He was also the one who first suggested asking [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] what he sees in the capabilities set. [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

## Aug 28 2026 — "bottleneck", and the event-by-event comparison proposal

At the [[wiki/meetings/2026-08-28-dragon-pays-nova-conversion-review.md|Aug-28 Dragon Pays review]] (Russian) Pavel opened by handing the floor to [[wiki/people/igor-metelski.md|Igor]] and framing what to report ("что было сделано… С чем столкнулся, какой вывод из этого?"), then supplied the two positions the meeting turned on. [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]

- **He supplied Val's missing word — "Боттлмек"** — when Val argued that all the speed gained on the port is worth nothing if QA cannot keep up. See [[wiki/topics/test-automation-strategy.md]] (Aug-28). [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- **His "rough idea" for verifying an AI-done port:** "мы можем просто оригинальную игру запускать на реальной машине, давать клоду к ней доступ. И чтобы он там ну не покадрово, а по крайней мере по событийно сравнивал то, что у него на машине с тем, что он сделал для новой платформы" — run the original on a real machine, give Claude access, and compare event-by-event rather than frame-by-frame. He offered it as the crude version: "прям в лоб наверняка есть более элегантные… идеи." [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- **The determinism objection behind it.** Prose and capabilities will never say what pixel belongs in frame 1, 2 and 3, and neither will the requirements; and the code itself does not guarantee it: "кот, он всего лишь воспроизводит видео, причём он не гарантирует, что он отобразит вообще 2 кадр… если я не успел, я этот кадр пропускаю… Это не детерминированная система." [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- **What he does think is fully automatable:** "любые поведенческие тесты можно и 100% покрыть… там чтото произошло, есть какойто отклик… по статусам всё это можно покрывать тестами 100%." (Irina supplied "функциональные".) [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- **He proposed the parallel second game and named the person** — [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], not fully loaded — and undertook to hand Igor's converter work over to him. He also pushed for an actual hardware build ("если действительно хотим сделать сборку для Того, чтобы запустить на машине и посмотреть? Тогда да, есть смысл, звук, правильность, да подлаживать"), having judged the on-screen FPS counter "не показатель." [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]

## Sept 1–3 2026 — the RK3568 rationale, the correction Val thanked him for, and the requirements-quality warning

- **Sept 1** ([[wiki/meetings/2026-09-01-nova-prose-qa-automation-check.md|prose/QA check-back]]): he announced Alexander Biratko's Flex-Pay→RK3568 assignment and gave the reason — a complete build system, service registration, payment-hub operation and a nearly finished software-update path, keeping Flex-Pay level with Flex-IQ ([[wiki/decisions/2026-09-01-flex-pay-onto-rk3568.md]]). He also reported second-hand what Vladimir Samusenko had built, split the NOVA prose ownership three ways (Vladimir = setup screens, Kharetski = local game server front and back end, Sasha the candidate for games), flagged the first-phase QA-coverage gap Val accepted, and described the gap-closing loop: ask the AI for the missing test *and* the matching requirement at the same time. [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- **Sept 3 — he corrected Val on the repository name and was thanked for it.** Val had ordered the standard into a repository "названн[ый] стандарт[ы]"; Pavel: "поправка[:] репозитор[ий] не называется… стандарты[;] репозитории называются [knowledge]. И там есть папка стандарт." Val: "Спасибо за поправку, согласен с этим." He also took the action of writing to "Andrei" for company-wide access. See [[wiki/decisions/2026-09-03-prose-standard-into-knowledge-repository.md]]. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He is running the skills as his own controlled comparison.** Before the meeting he launched them on the RK3568 SDK project, where prose and capabilities had previously been produced "просто простым разговором с Клодом, не используя стандарт[…] на прозу," so he can diff the standard-driven result; he also wants a bare repository with no prose as the second test. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He defended the LGS capability count against Irina** — "lg s действительно огромный проект, и там много составляющих. Может быть 50 это и нормально для такого проекта." See [[wiki/decisions/2026-09-03-capabilities-consolidated-by-administrative-direction.md]]. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **His estimate of the existing Jira requirements is brutal:** "из всех них хорошо, если один процент будет написан правильно… прямо в дискрипшене будет написан акцептно[c]ть критерий, потому что… последние гдето, наверное, полтора месяца только начали в таком формате писать." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He named the real long pole against Val's Oct-1 target:** not the capabilities but the adequacy of the requirements, because "каждый регламент должен быть прочитан человеком" — each one must be read by a person, not generated by Claude and skimmed afterwards. On tests he was blunt: "вряд ли мы закроем 50% тестов[ ]к октябрю… очевидно меньше 50." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He proposed [[wiki/people/alexei-khamin.md|Alexey Khamin]] for the requirements/acceptance-criteria work** (with Ivan as capacity allowed), which Val cut to a single owner; and Val left him the assignment of all the meeting's tasks. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Sept 2 2026 — the engineering constraints on the Flex-IQ pre-pilot and the port family

On the [[wiki/meetings/2026-09-02-flex-iq-pre-pilot-updates-after-the-show.md|Sept-2 Flex-IQ pre-pilot call]] (Russian) Pavel supplied most of the hard limits the design had to bend around. [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

- **He named the printer switcher as non-existent work.** "вот этот вот свич, который про который говорил Андрей, его надо будет реализовать[,] его нету и его надо продумать. Как сделать управление переключением портов?" — and said it will have to be done remotely, because the boards arrive "плюс там 34 недели" after Genadi gets them. His fix: build a bench, "Возможно, кстати, в джорджии потому что мы сейчас инициировали прямой VPN канал из [Джорджии] к нам сюда в офис." See [[wiki/decisions/2026-09-02-implicit-consent-and-mandatory-printed-receipt.md]] [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **He noted the receipt-printing code already exists and is simply not enabled** — "Он просто пока что не за[э]нэбл[ен]" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **He drew the wallet→scanner consequence that reshaped the port.** "если [и]волит это наше основное направление… [то] на фле[к]спорт должен содержать в себе [баркод]сканер. То есть вот этой вот платы будет недостаточно… Ну, либо сделать новую ревизию этой платы." Val: "Да, конечно." He also fixed the SAS-universal scope — "не будем пытаться закрыть там 10% рынка где нету 2 сасса." See [[wiki/decisions/2026-09-02-flex-port-sas-universal-with-scanner-touch-vs-non-touch.md]] [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **He raised the memory ceiling on the cheap board** — ~2 MB of flash, built-in RAM, "один раз прошили и всё" — priced remote firmware update as "Значительно" more expensive, and referred the threshold question to [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]: "Я этим вопросом не занимался… По цене сейчас не смогу." He also judged a small ~4-inch touchscreen probably cheaper than a physical button panel [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **He argued the cloud case for e-wallets and won it.** "это должно быть в клауде, потому что это потом легко будет распространяться на мобильные телефоны. Но что без клауда это будет невозможно" — and offered the later "friendly locations" server flag so wallets could be shared between locations. See [[wiki/decisions/2026-09-02-e-wallets-move-to-the-cloud.md]] [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **His two rejected/deferred proposals.** A stack of pre-printed carrier tickets at the location (Andrei rejected it on loss, damage and restocking grounds) and angling the scanner slightly forward for wider items (Andrei deferred it) [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **He forced the go-to-market question before anyone travels:** "Нам надо чётко тогда иметь уже сейчас видение. С какой схемой мы туда идём?… Именно [и]вол[ет,] не [TITO]" — which produced Val's "Сегодня… [и]волет[ы]." He also supplied the line "Вместо отпуска" when Val pushed Andrei to go to Texas immediately [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **He reported the payment hub deployed** — "там всё что было сделано [Нейтоном] оно за[]деплоино" — and took the API re-run so the stuck transactions retry ACH the next morning [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **He proposed scoping the [[wiki/organizations/island-park.md|Island Park]] API to what each customer opens up**, and judged a batch-file transfer "уже устаревший вариант" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Open commitments (Sept 2 2026)

- [ ] Re-run the payment-hub API request so the stuck/errored transactions move to pending and retry ACH the next morning — due right after the Sept-2 meeting — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [ ] Design the port-switching control for the printer signal on the new board — due unspecified; likely remote, possibly against a bench in Georgia over the new VPN link — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Open commitments (Sept 3 2026)

- [ ] Write to "Andrei" (by context [[wiki/people/andrey-bosik.md|Andrey Bosik]] — inference) requesting company-wide access to the `knowledge` repository — due promptly — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [ ] Assign all the tasks arising from the Sept-3 meeting, ready for the Sept 4 session — due Sept 4 2026 — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [ ] With [[wiki/people/irina-shishko.md|Irina Shishko]] — tidy the capabilities, move them into Jira and build the new Jira structure (LGS a candidate next project) — due September 2026 — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]] [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Open commitments (Aug 26–28 2026)

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — take forward the direct Georgia-office ↔ Minsk network link, which he proposed and Val accepted in full ("Абсолютно согласен с этим полностью поставьте себе это надо"); Pavel's own framing was that "Андрей с Димой" in IT (which Andrei and which Dima are not stated) should propose the joining option — due unspecified — [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — assess the Light & Wonder SAS / player-tracking system with [[wiki/people/elizabeth.md|Elizabeth]] and, if tractable, build a full VM emulation of it in Minsk — due unspecified — [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — hand [[wiki/people/igor-metelski.md|Igor Metelski]]'s Rage→NOVA converter work to [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] and assign him the parallel second (line) game port — due unspecified — [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]

**Naming note (Aug-26 / Aug-28).** Val closed the network-link item with "Павел это это ваш Андрей текин." The derived Aug-26 notes read that garble as a person and record the undertaking as "raise it with IT (Andrei Tekin)" [[raw/Meeting_Notes_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]. The **identical garble recurs in the Aug-28 transcript** — "андротейкинг следующий" and "Значит, Андрей текин понятен" — where it can only be the English word *undertaking* [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]. So no person named "Andrei Tekin" is recorded in this wiki; per §4 the mention fits no known person and is treated as a mis-hearing. Flagged for owner review.

## Open commitments (Aug 24 2026)

- [ ] Work out the stage-1 local-network design for Flex-Port-Mini: wired CAT5 / RS-485 with daisy-chain support on the existing WSS or a Modbus-style protocol plus an encryption layer; note Bluetooth mesh as a later experiment — due unspecified — [[raw/Meeting_Notes_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- [ ] With [[wiki/people/irina-shishko.md|Irina Shishko]]: schedule daily team time to fill in capabilities and open questions against already-written code, drive the whole team to catch up, and assign Sergey Tsimanov to the backend/CMS prose and to verifying Dima's prose — due end of September 2026 — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Sept 4 2026 — the anti-anchoring rule, the September task plan, and the standards link posted in chat

At the [[wiki/meetings/2026-09-04-rage-nova-conversion-readiness.md|Sept-4 morning meeting]] [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]]:

- **He proposed evaluating Test 360 from a clean Claude session that has never seen Igor's acceptance criteria**, because a session that has seen them gets "замыленный взгляд" and keeps referring back to them; he also allowed that Claude might judge the current path a dead end and propose something better. Igor accepted. See [[wiki/topics/test-automation-strategy.md]] (Sept-4). [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He framed the goal Val then corrected.** Pavel: many people converting games with Claude will produce a finished product fast, but full behavioural testing in the cabinet with different switch settings will be impossible, so "кувей будет ботлнек… на многие месяцы вперёд"; automated checks from Claude would free QA and let JVL release faster. Val: "это почти правильное описание нашего объект[ива]. Но это не на 100%" — and laid out the fuller pipeline ([[wiki/topics/nova-platform-architecture.md]], Sept-4). [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He supplied the ramp for winding QA down:** compare Claude's verdict against the QA department's on the first game, give QA less time on the second, "и смотрим, что… продукт вышел[,] замечаний с полей нету, значит, тем меньше и меньше и меньше надо вкладываться в [QA]." With the caveat he repeats: "мы[-]то делаем[.] Продукт для человека[;] его будет в конце концов потреблять человек, а не искусственный интеллект." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He corrected the premise on repository ownership** — Andrei only creates the repository name, the content is filled in by Igor — and then named the real problem: the Calle Ocho repository's directory structure "была независимо сделана от… Того, что обсуждалось," which is what triggered Val's "у нас есть написанный стандарт." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He posted the standards-repository link into the meeting chat** "чтобы потом никто не говорил, что я не знаю, где у нас стандарты лежат. Вот пользуйтесь этой ссылкой" — see [[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]]. [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He argued the deferral that closed Anton's stack objection:** changing engine later means replacing "только один блочок там из 20," with the test pipeline staying roughly the same. [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **Val gave him the September task plan for the whole team:** "Я прошу Павла[.] Расписать задачу на всех людей[.] На сентябрь месяц[.] Чтобы в конце сентября у нас это было сделано." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]

## Sept 4 2026 (midday) — the modem post-mortem he did not accept, and the debug environment he had already built

Two back-to-back calls the same midday, and Pavel comes out of them very differently.

**The modem call (12:10–12:29 PM ET),** [[wiki/meetings/2026-09-04-lte-modem-firmware-mismatch-and-kore-settings.md|LTE modem firmware mismatch]]. He reported the position plainly — the 7455 fitted in Georgia does not work, the cause is not fully clear, two days of experiments with Elizabeth Palomino could not configure a stable link — and explained the Minsk pass as a case of too many differing inputs: "другой провайдер, другая версия прошивки[,] на другой рынок модем рассчитан." **He rejected [[wiki/people/genadi-peari.md|Genadi]]'s "mistake number one" framing outright** ("Я не согласен… какая ошибка[?] Где ошибка?") and rejected Val's too ("Не не не так не так"), holding that testing in Minsk on the same model was a valid test. He then supplied the idea that could solve the whole thing cheaply — ask KORE for the modem configuration parameters, the APN in particular, and hard-code it ([[wiki/decisions/2026-09-04-north-america-modem-variant-and-ask-kore-for-the-apn.md]]). The accountability exchange is on [[wiki/topics/jvl-operating-principles.md]] (Sept 4); it ended with him saying "Хорошо[,] я вас услышал. Ещё больше расстроился" and Val suggesting he think it over across the weekend. Genadi's read minutes later: Pavel "был в шоке от моего комментария и уехал, расстроенный домой" (Val's words) — and Val decided to leave him alone until Monday [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]] [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

**The production call (12:29–1:49 PM ET),** [[wiki/meetings/2026-09-04-flex-slim-first-ten-and-flex-port-sas.md|Flex-Slim / Flex-Port SAS]], which he joined late from his car — "I need about half an hour to… get to your home." Reported in his absence: he had told Genadi that SAS integration into the port was not being worked on and asked "а вообще зачем нам flexport?", proposing a screenless SMIB variant instead — **rejected by Val** ([[wiki/decisions/2026-09-04-flex-port-keeps-its-screen.md]]). On the call itself, with the transcription badly degraded, what survives is his stage-2 proposal: debug hooks and packet logging, a machine emulator and a full debug console (built on an **STM32 743**), and a described physical environment — Flex-Pay connected, a machine on the network, one or several Flex-Ports, an **ST-Link** debugger, and a written map of what is connected where and where each unit's code lives — so Claude can find things and say what needs correcting. He had already built most of it and **shown it to [[wiki/people/alexei-khamin.md|Khamin]] that day** for his own testing. He also corrected Val on [[wiki/people/aaron.md|Aaron]]'s RK3568 work: Aaron "никакую среду не подымал," he assembled a set of build scripts. Detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 4) [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

He also confirmed, per Genadi, that **both card-dispenser versions are supported in software** ("боус v[e]rsi[o]ns работает, поддерживается software") [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

**Genadi's private assessment of the SAS work, given to Val after the engineers left:** "без Павла это не пройдёт" — it will not happen without Pavel. Recorded as Genadi's judgement [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

## Open commitments (Sept 4 2026)

- [ ] Lay out September tasks for all the people so the documentation work (repositories to standard, data contracts placed, prose finished, capabilities in Jira and closed, requirements with acceptance criteria) completes by month end — due September 2026 — [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [ ] Think the Flex-Port capability breakdown over the weekend and bring it to the Monday 7:00 engineers' meeting — SAS AFT transactions on Flex-Port, the existing Flex-Port use, and a supporting debug-environment capability — due Monday Sept 7 2026 — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [ ] Upload the software remotely to the replacement Georgia modems and verify they hold a connection; if a good modem does not work on the existing software, connect remotely and find the cause — due after installation — [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]

## Sept 7 2026 — the Monday he absorbs the Flex-Port work: Wi-Fi provisioning designed, SAS/AFT taken on, the emulator finally scoped

Across both Monday meetings ([[wiki/meetings/2026-09-07-wifi-on-flex-port-and-qr-provisioning.md|9:08 Wi-Fi]] and [[wiki/meetings/2026-09-07-sas-aft-on-flex-port-and-remote-update.md|10:02 SAS/AFT]], Russian) Pavel is the person who turns each of Val's directions into a mechanism — and the person Val is explicitly trying to unload.

- **He designed the Wi-Fi provisioning flow**, including the security point nobody else raised: the QR must not be the plain phone network-sharing code, "он в незашифрованном виде отдаёт название сети и пароль," so "этот пароль всё таки надо каким то образом шифровать и уже потом на флекс па[р]те расшифровывать" — see [[wiki/decisions/2026-09-07-wi-fi-provisioning-by-encrypted-qr.md]] [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **He named the jamming risk on Val's behalf** — "вайфай легко зафлудить… у нас вся сеть сразу же ложится" — and separately doubted the on-module antenna would radiate out of "железный огромный корпус и чуть чуть пластмаск[и], которая торчит" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **He supplied the one-firmware-by-configuration answer** when Alekseev asked how three machine interfaces can be served: a SAS-configured port simply does not load the EBDS and identifier code, and counters become statistics, "не считаем их как элемент вывода денег" — [[wiki/decisions/2026-09-07-flex-port-goes-sas-and-jvl-drops-the-old-machine-segment.md]] [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He had already run the AFT experiment, on the Friday**, on the SAS firmware "которую Евгений, 2 Евгения делали," and wants it finished so the minimal command set can be written down. He then took the larger part of the SAS/AFT implementation himself, on the reasoning that Alekseev is on vacation, has Wi-Fi, and can only work weekends — while SAS parallelises locally "потому что у нас несколько машин и несколько портов" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He accepted the reverse-engineering burden**: prose and a retrospective capability list onto the Flex-Port code that already exists, working with what [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] is building [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He pushed the virtual test system to its most ambitious form** — full ARM emulation running the production build, simpler options only as fallback "потому что… более простые варианты… не покрывают весь функционал" — see [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]]. He would not accept Val's "50 % готово" characterisation of what he already has: "не готова, у меня какие-то наработки есть… я пока не уверен, что они готовы к тому, чтобы их отдать" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **Val's stated motive for appointing a driver was Pavel's load:** "На Павла ложится очень много работы… я бы хотел, чтобы с Павла это ушло" — and the driver named was [[wiki/people/andrey-bosik.md|Andrei Bosik]] [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]

## Open commitments (Sept 7 2026)

- [ ] Build the Wi-Fi provisioning screens on Flex-Pay and Flex-IQ and the encrypted-QR handoff to the Flex-Ports, diagnostic screens included — due unspecified — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] Extend the cloud logging to capture connection/installation telemetry, with store-and-forward when there is no internet — due unspecified — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] Verify the Flex-IQ side of the Wi-Fi work, at Val's explicit request — due unspecified — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] Finish the AFT experiment (test credits and cashouts over AFT) so the minimal command set can be documented — due unspecified, high — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] Take the larger part of the SAS/AFT implementation — due unspecified — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] Reverse-engineer prose and a retrospective capability list onto the existing Flex-Port code, plus the changes needed now and the new ones — due unspecified — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] Break the capabilities into features and open the feature branch — due unspecified — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] Attempt the ARM-emulation virtual test system with simulated devices; Docker/daemon-mode is the fallback — due within a week or two — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] Talk to [[wiki/people/alexander-biratka.md|Alexander Biratka]] and [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] about standing up the Flex-Pay emulator side quickly — due unspecified — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] Find out what remains for "Сергей" on the Flex-IQ screen changes; he thinks it should finish that day — due Sept 7 2026 — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]

## Sept 9 2026 — names Flex-Port the bottleneck, takes the SAS work himself, and is told to stop planning by hand

On the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept-9 7:02 AM resource-plan call]] (Russian, with Val and [[wiki/people/irina-shishko.md|Irina Shishko]]) Pavel did three things that shape the rest of the transactional programme.

- **He gave the readiness estimate and would not gild it.** Not Sept 11, "[с]корее всего, нет" for Sept 18, "в лучшем случае это 25" — and he refused to be more precise until testing begins: "[ко]гда начнём тестировать[,] станет понятнее, насколько много недоработок возникает по ходу." Detail on [[wiki/decisions/2026-09-09-flex-port-readiness-slips-to-september-25-and-stays-the-bottleneck.md]]. [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **He named Flex-Port the bottleneck** — "пока не сделается какой[-]то функционал в[о] флекспорте[,] дальше проверить на flexpay какой[-]то функционал будет невозможно" — and took the SAS work himself, giving both reasons openly when Val asked whether he was assigning it to himself because it interests him: "[д]а, мне это интересно," and then the resource argument (Khamin and Irina beside him, many machines to run cases on, against Alekseev's roughly one-day latency). [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **He flagged the engineering fork** that limits a location to FlexPay *or* Flex-IQ in the first iteration — [[wiki/decisions/2026-09-09-one-transactional-unit-per-location-until-the-wi-fi-iteration.md]]. [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

**Val's instruction to him** was to stop doing the Jira planning by hand and lean on [[wiki/people/andrey-bosik.md|Bosik]] and [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] in daily recorded sessions — see [[wiki/decisions/2026-09-09-planning-handed-to-bosik-and-kovalchuk-with-daily-recorded-sessions.md]]. Pavel took it as an experiment rather than a conviction: "[х]орошо, давайте начнём так… [с]мотрим, к чему приведёт." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

Two exchanges worth keeping for the working relationship. Pavel, on being told he is hard to talk to: "есть только моё мнение и неправильное мнение[,] вы про это" — Val corrected him: "[н]ет, я говорю, что с толковыми людьми всегда тяжело говорить… они не ведутся ни на что… [я] вас обосрал[,] [и сделал] комплимент заодно." And on his own hours: "я[-]то работаю почти круглосуточно тоже сейчас." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

**Open commitments (Sept 9 2026)**

- [ ] Have at least one working stand ready — FlexPay or Flex-IQ with Flex-Ports on the new firmware, over SAS — due mid-week of Sept 14 2026 (his number: the 16th; Val asked for the 15th) — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] Get the full setup working in the office at least two weeks before the October 1 installation so Klimovich can start testing — due week of Sept 14 2026 — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]] [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] Build the October-1 work schedule and have it ready for the Friday meeting with Val — due Sept 11 2026 — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]] [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] Start the daily planning sessions with Bosik and Kovalchuk, with Irina, and put Val on the invitations — due from Sept 9 2026 — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] Create the three placeholder features under capability 165 and a separate capability for the wallet transfer — due unspecified — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] Record the Flex-Port SAS testing as two separate items (JVL machines / other suppliers' machines) — due unspecified — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

## Sept 10 2026 — he chairs the transactional planning call, and sets the order of work

Pavel called and ran the [[wiki/meetings/2026-09-10-capability-requirements-workflow-and-mvp-split.md|Sept-10 2026 5:31 AM transactional call]] (Russian, 25 minutes, no Val). He opened it with the purpose — optimise development so the most work is done in the least time and the result is cheap to test — and spent it setting sequence and filing rules. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

- **He restated the capability → requirements → features chain as already agreed**, with the caveat attached: it only works where all the capabilities and their requirements are written, otherwise "у нас возникает дыра, которая не будет закрыта автоматическими тестами." His sufficiency bar is ~80%. Full text on [[wiki/decisions/2026-09-10-requirements-come-first-and-the-recycler-is-out-of-both-mvps.md]] and on [[wiki/topics/test-automation-strategy.md]] (Sept 10). [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He overruled [[wiki/people/andrey-bosik.md|Bosik]] on the order of work** — MVP split is step three, requirements step two: "[н]у это это это 3 шаг[;] 2 шаг это всё[-]таки рекла[мен]с." [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He ruled the Flex-Recycler out of both MVPs** — "[р]исай[к]лер это не MVP один и не MVP 2 даже" — against Bosik's argument that it belongs in transactional scope because it too has a Wi-Fi module. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He set the MVP dates:** MVP 1 by October 1, MVP 2 by November 1, with November 1 likely moving to October 21 for the next Georgia expo. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He deferred the requirements-ownership question rather than answering it**, routing [[wiki/people/dmitri-chudinov.md|Chudinov]]'s objection about business-vs-engineer requirement writing into a voice walkthrough with [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — "[д]а[,] [Д]има[,] хороший вопрос." [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He took the fix versions himself**, and named what a capability review must produce: what you disagree with, what is missing, the obvious errors, and where requirements are linked, inadequate or absent. See [[wiki/decisions/2026-09-10-per-product-components-and-mvp-fix-versions-on-the-capability-project.md]] and [[wiki/decisions/2026-09-10-capability-review-feedback-goes-into-the-meeting-chat.md]]. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He redirected the Sept-9 Bosik/Kovalchuk planning delegation** to capability review instead — "мне кажется, сейчас вот я подумал… [н]ам на текущий момент как раз нужно… [д]ругая работа." See [[wiki/decisions/2026-09-09-planning-handed-to-bosik-and-kovalchuk-with-daily-recorded-sessions.md]]. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

## Open commitments (Sept 10 2026)

- [x] Pavel Frolov — create the MVP 1 and MVP 2 fix versions in Jira — due September 10 2026 — **discharged Sept 11 2026**: two releases, Transactional MVP 1 (Oct 1) and Transactional MVP 2 (Oct 30), created in the product-capability space — [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] Pavel Frolov — call a meeting with [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] the same day to walk through every capability by voice and agree the requirements, including who writes them — due September 10 2026 — [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [ ] Pavel Frolov — hand a version of FlexPay and FlexPort to Andrei Klimovich so he can install it on his own devices and test — due about a week out (Irina's marker: after the 18th) — [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

## Sept 11 2026 — he brings the releases to the Friday meeting, defines MVP 1, and takes the weekend

Pavel is the reason the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept-11 8:04 AM call]] happened — [[wiki/people/andrei-klimovich.md|Klimovich]] convened it "[п]о просьбе Павла" — and it is the Friday schedule meeting Val booked on Sept 9. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

- **He arrived with the work done.** Two releases created and dated — "транзакш[е]н MVP один и транзакш[е]н [M]VP 2… [окто]ба 1 и [окто]ба 30" — capabilities already being linked to MVP 1 and features created underneath. That discharges both Sept-9 commitments on [[wiki/decisions/2026-09-09-first-transactional-installation-planned-for-october-1.md]] and the Sept-10 fix-version commitment above. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He gave MVP 1 its definition:** "MVP один работает через линкед[ ]этот самый нетворк… [и] на лакейш[н]е может стоять один киоск, либо IQ, либо flexpay[,] всё, а всё остальное идёт в M[V]P 2." [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He supplied the answer that beat Klimovich's card-splitting proposal** — issue one card at $1,000 and leave the remainder on the player's ticket. See [[wiki/decisions/2026-09-11-one-card-at-a-thousand-dollars-and-the-rest-stays-on-the-ticket.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He set the work split:** Chudinov on Flex IQ, [[wiki/people/alexander-biratka.md|Biratka]] on Flex-Port and porting into FlexPay, [[wiki/people/sergey-tsymanov.md|Tsymanov]] on the FlexPay server side. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He named machine compatibility as the live MVP-1 risk** — Flex-Port compatibility implemented for some cabinet models and not others, possibly needing per-cabinet work after MVP 2 — and made the Georgia VPN a hard dependency of the compatibility-testing window: "нам к этому времени 100% нужно… VPN в Джорджия офис." See [[wiki/projects/georgia-market-rollout.md]] (Sept 11). [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He laid out the three-step firmware-distribution staging** and held USB update of the Flex-Ports as the absolute fallback. See [[wiki/decisions/2026-09-11-mvp1-boundary-bill-escrow-and-pin-out-remote-update-and-master-device-in.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He proposed the weekend work and took it himself too.** Chudinov Saturday and Sunday on the Flex-Port / Flex-IQ services and card activation on the e-wallet path, "не за… выходной день, а за дополнительные деньги"; Pavel on Flex-Port and the bill-validator question. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Sept 11 2026 (9:30) — he identifies the regulatory hole in remote game updates

Twenty minutes after the transactional call, on the [[wiki/meetings/2026-09-11-nova-game-change-regulatory-procedure.md|NOVA game-change call]], Pavel supplied the substance of the meeting. He corrected [[wiki/people/juan-martinez.md|Juan Martinez]]'s belief that Georgia uses no bin file — it does, once, at submission, and [[wiki/people/ivan.md|Ivan]] sends it — explained that the Georgia bin file carries only SAS-operation data and "**is not directly relates to game sets**", and drew the consequence: "**if we are releasing a new game, but we do not change anything related to local gaming server or data center… adding a new game will not change a bin file. And in this approach, Lottery will not know anything about new games. That could be a problem.**" Juan agreed that is the core of the regulatory issue. See [[wiki/decisions/2026-09-11-the-game-change-question-goes-to-gli-as-a-paid-consultation.md]]. [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]] [[raw/Meeting_Notes_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]

## Sept 11 2026 (10:33) — he misreads the field complaints, and supplies the constraint that matters

At the [[wiki/meetings/2026-09-11-technician-complaints-and-new-capabilities-workshop.md|10:33 AM technician-complaints workshop]], the third meeting of his morning, Pavel read Val's complaints document and drew the wrong conclusion from it — that technicians dislike remote and network setup and would rather work manually ("Технином не нравится то, что всё таки у нас есть ремонт и нишевал setap, что они бы лучше бы работали вручную"). Val rejected it twice, flatly [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

- **What he contributed instead was the implementation constraint nobody else raised:** a passport update today can only be performed by people entered in JVL's CMS, so moving to the new CMS implementation means "мы должны давать оператору назначать людей, которые могут это делать" — the operator must be allowed to nominate who may do it. Val accepted it. See [[wiki/decisions/2026-09-11-the-passport-is-preserved-and-jvl-is-using-the-bindings-wrongly-in-this-market.md]]. [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- **He also pushed back on the "nothing into RAGE" rule and got a sequence rather than a no** — his example being the ancient black-screen "device not found" message, which could name the IO board or counter board at about half an hour of work. Val's answer: back-ports get chosen after the new capabilities exist. See [[wiki/decisions/2026-09-11-no-changes-in-rage-studio-everything-lands-on-omni.md]]. [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- **He is named to the Monday Sept-14 9:30 working meeting** on the new Passport/RIS regulations, and asked to think it through over the weekend — on top of the weekend Flex-Port work he had already taken. See [[wiki/decisions/2026-09-11-new-regulations-for-the-passport-and-ris-talked-out-monday-and-converted-from-the-transcript.md]]. [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]

## Open commitments (Sept 11 2026)

- [ ] Pavel Frolov — think through how he sees the new Passport/RIS capabilities, and attend the Monday working meeting — due Sept 14 2026, 9:30 — [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- [ ] Pavel Frolov — finish linking capabilities to MVP 1 and MVP 2 and creating the features underneath — due week of Sept 14 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] Pavel Frolov — work the weekend on Flex-Port and establish whether the bill validator can be disabled through SAS when a location is blocked — due Sept 12–13 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] Pavel Frolov — move the Flex-Port remote-firmware-update capability so the master-device half sits in MVP 1 — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] Pavel Frolov — move the Flex and FlexPay capabilities into the E-wallet Operations initiative and rename the bucket off "FlexPort", which Val called too narrow — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Sept 14 2026 (6:38 AM) — he proposes the Georgia base, and gives the honest state of the NOVA build

At the [[wiki/meetings/2026-09-14-texas-vertical-conversion-and-georgia-game-base.md|Sept-14 6:38 AM ET session]] (Russian) Pavel did two things: he supplied the way out of a dead end, and he answered Val's question about the NOVA build without softening it. [[raw/Meeting_Notes_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

- **He proposed taking the vertical Georgia games as the base for a vertical Texas product**, crediting a conversation with [[wiki/people/igor-metelski.md|Igor Metelski]] the day before: "Вчера ещё вот мы с Игорем общались… может быть нам логичнее взять вертикальную игру для джорджии и её конвертировать в вертикальную игру для Техаса. Что это возможно, будет гораздо дешевле." Val adopted it — [[wiki/decisions/2026-09-14-vertical-texas-starts-from-the-georgia-coam-vertical-games.md]]. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **He also floated, and immediately doubted, an AI layout idea** — let AI stretch the top background and place the auxiliary blocks itself — "но по-моему всё равно оно будет слишком разрежено и слишком много занимать места именно вспомогательная информация, а не рилы." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **Asked whether NOVA is at the state where the new architecture and tech stack can be used: "Ну до конца нет, мы не довели."** One or two games run on the FP7; the HAL library integration is unfinished; the shared-object build still is not done the new way, and the integration repository "мы это обсудили, но мы это не делали вообще." The build comes out of the game repository pulling hand-made artefacts — "на коленке без помощи искусственного интеллекта" — via a Linux snapshot, a kernel build baked into a separate image, then games, HAL and maths in Docker containers, output as an ISO. Full detail on [[wiki/topics/nova-platform-architecture.md]] (Sept 14). [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **His definition of doing it properly:** rebuild that repository on the same Linux used for RK — "там[,] что мы дебиан по-моему брали", the hedge his own — so everything sits in one development system; a small piece of work so the existing RK kernel builds for the LAN-based machines; and create the integration repository that collects artefacts from the separate repositories. On RK the work is already possible today, but RK needs its integration repository too, from which they would take the build made for the RK SDK that exists now for Transactional — "тут даже чуть-чуть меньше работы возможно." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **He closed Igor's OmniCore objection with current information:** "Игорь[,] это уже не актуально. Уже на днях саша с даниилом уже всё это объединили в один репозиторий." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **He tried to raise a topic involving "Юрий Валентинович" and finding a group of people** at the close — "прежде чем искать какую-то группу людей" — and Val cut it out of this meeting into a separate call. The topic is not described further in either source. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

**§15.8:** clear — engineering and build content only.

## Sept 14 2026 (7:37 AM) — he is the only objection to the main-branch rule, and it is turned back on Val

An hour later, at the [[wiki/meetings/2026-09-14-code-standards-main-branch-rule-and-alekseev-coaching.md|7:37 AM code-standards call]] (Russian), Pavel is one of the two addressees of Val's code-standards email and the only person who argues with it at length.

- **He accepted the main-branch rule only "in general"** — "**Инженерал все правильно инженерал**" — and Val deliberately kept the hedge rather than pressing for an absolute [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **His objection is the long-lived development branch:** "**за исключением тех случаев, где мы хотим от мэйна держать ещё какойто девелопмент бранч… на какое то время становится мейнстримом**". His live example is his own — he branched off the **Flex-Port** platform project to add the **SAS / AFT** work [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **He proposed promoting his branch to main and tagging the old version as release one**, and Val refused it: "**Чтото я так не вижу**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **The example he produced to defend the branch is what defeated it.** Val had written the day before that Flex-Port must also work on machines **without SAS** — "**вчера вы написали… Это как бы немножко ломает то, что я уже сделал. И то есть надо обратно возвращаться в мэйн и иметь возможность переключать, либо мы работаем так, либо так, но кодовая база одна**". Val agreed it was a good example, took the specification gap as his own, and ruled the split a selection capability inside main rather than a branch — [[wiki/decisions/2026-09-14-flex-port-sas-mode-is-a-selection-capability-not-a-long-lived-branch.md]] [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **His own restatement is the requirement that came out of the call:** "**у нас должна быть возможность задавать режим работы для флекспорта… либо на этапе сборки либо… на собранном девайсе каким то параметр[ом]**" — build time or a device parameter; neither chosen [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **He gave the October 1 capability counts** — "**30**" across all systems, corrected by [[wiki/people/andrey-bosik.md|Bosik]] to fewer for the port, then "**Ну 10**" unchecked; the Friday meeting he refers to is Sept 11 [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **He confirmed Val's account of [[wiki/people/evgeniy-alekseev.md|Alekseev]]'s "tell me and I will implement it" rule** — "**Это было примерно так**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

## Open commitments (Sept 14 2026)

- [ ] Pavel Frolov — treat the Flex-Port SAS / no-SAS split as a selection capability inside main, with one code base and a way to set the operating mode, instead of a long-lived branch — due unspecified; no Jira item named in the call — [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]

## Sept 14 2026 (8:01 AM) — the cheap answer, the correction, and the offer to put the product manager on a real machine

At the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|8:01 AM use-case call]] he played the role he usually plays: the shortest defensible answer, delivered without argument.

- **Why empty wallets are simply kept.** Val questioned holding an empty wallet for 30 days; Pavel answered on build cost, not policy — "[н]ам проще его держать, чем придумывать отдельную логику работы с пустыми тикетами" — and Val closed the point with "это хороший ответ." See [[wiki/decisions/2026-09-14-ewallet-ttl-defaults-to-thirty-days-and-is-set-per-location.md]].
- **He corrected the remote-update optimism in real time.** Against Bosik's "почти готово", Pavel named the gap — "пока что мы не умеем обновлять Флекс[-]порт… придётся пока что скачивать и ставить, как ставили раньше" — which is what turned Val's complaint into a dated target ([[wiki/decisions/2026-09-14-nobody-downloads-and-installs-builds-thirty-day-target.md]]).
- **He dismantled the photocopy-fraud argument** with one observation — "с одного тикета деньги можно один раз снять… [д]аже если 2 раза он распечатал, он один раз может только" — and backed Chudinov's no-new-number alternative: "но под новым номером не надо" ([[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]]).
- **He offered Klimovich the port firmware** so he could install it, connect over SAS and walk the new workflow himself — the offer that led, two minutes later, to Val's ruling on the published SAS standard ([[wiki/decisions/2026-09-14-capabilities-are-written-against-the-published-sas-standard.md]]). It was also Pavel who answered Klimovich's "how will this work on a third-party machine?" with two words: "**Это стандарт**" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].
- **His verdict on the list:** the use cases were clear — "всё очевидно" — and a large part of the capability list "выглядит как почти сделано, или сделанное, но не покрыт[о]… автотестами", needing corrections and some added reports. He then found the two things missing from it: the audit report, and the capability 171 / 118 overlap [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].
- **He corrected Val on his own process rule**, without hedging: Val's phrasing swept In-Progress items into the move-to-Accepted demand and Pavel stopped him — "не так[:] те, которые [In Progress,] это уже после [Accepted]" — and Val accepted it [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Open commitments (Sept 14 2026, 8:01 AM call)

- [ ] Pavel Frolov — give Klimovich the current Flex-Port firmware so he can install it, connect over SAS and walk the new workflow himself — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [ ] Pavel Frolov — make sure everything In Progress is scheduled, ahead of the next morning's UI/UX meeting — due Sept 15 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## Sept 14 2026 (12:04 PM) — his fourth call of the day, and the one where he refuses a diagnosis and then supplies the unsolvable case

At the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|12:04 PM hardware call]] (Russian; with Val and [[wiki/people/genadi-peari.md|Genadi Peari]]) he does three distinct things. [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

- **He refuses Genadi's modem diagnosis, in the same words as ten days earlier.** Genadi said the modem is fine and the SIM is incompatible; Pavel: "**Я бы так не говорил однозначно, Гена — это надо с этой симкой пробовать коннектиться, может быть всё что угодно**." He then proposed the test that would settle it — putting the same SIMs into the Flex units, with an "Андрей" (§4 unresolved) — and wants to **order modems from KORE now**, in two form factors, M.2 and mini-PCIe. See [[wiki/decisions/2026-09-04-north-america-modem-variant-and-ask-kore-for-the-apn.md]] (Sept-14 update).
- **He sets the firmware-update order himself**, after Val demands it be in MVP 1: priority one is Flex IQ and FlexPay updating themselves, priority two is those units distributing and flashing Flex-Port firmware, with [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] on the IQ↔port protocol first and [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] possibly needed. See [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]]. This is the same gap he had named himself at 8:01 that morning ("пока что мы не умеем обновлять Флекс[-]порт") now turned into a plan.
- **He names the loss case nobody can close.** Pressed by Val on what happens when printing breaks part-way, he described the boundary precisely — up to a point the money can come back, "**но если уже баркот напечатал[ся] — деньги уже с машины снимутся**" — and then volunteered the case that defeats it: a deliberate power cut once the barcode has begun leaves a redeemable ticket and the money cannot be returned. For the TITO-as-wallet flow he made it worse: a working barcode exists "**вот на самом краю. Даже если чуть[-]чуть напечаталась — то уже всё**." Recorded on [[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]].

**His one piece of good news all call**, and he offered it unprompted: the recycler's documentation ships an **ARM library** — "**сэкономит, я думаю, неделю разработки точно**" — about a week of development saved [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**And the honest state of the new board**, matching the honesty he showed on the NOVA build that morning: on the RK3576 "**мы вопервых должны запустить хотя бы одну игру… [н]а текущих версиях мы ни разу не доходили до этого**" — they have never once got a game running on the current versions — with the 3576 SDK still to be reworked and the integration repository still to be built. See [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]] [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**§15.8:** clear — product, component and task content only.

## Open commitments (Sept 14 2026, 12:04 PM call)

- [ ] Pavel Frolov — order modems from KORE: two samples, M.2 and mini-PCIe — due as soon as possible — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] Pavel Frolov (with "Андрей", §4 unresolved) — test the same SIM cards in the Flex units to establish whether the fault is the SIM or the modem — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] Pavel Frolov — verify that the card dispenser's low-level sensor actually reports — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] Pavel Frolov — on arrival of the RK3576, get at least one game running and report memory use — due on arrival — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] Pavel Frolov — rework the SDK for the RK3576 board and build the integration repository — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] Pavel Frolov — deliver firmware update in MVP 1 to a production standard, with pings, verification and a timer — due with MVP 1 — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Sept 15 2026 (8:03 AM) — he refuses Val's position on a state-issued block, and supplies three design corrections

At the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept-15 8:03 AM call]] (Russian) he was the most-corrected-into-the-design voice of the meeting [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**He overruled Val on the Georgia Lottery block.** Told it was not JVL's problem, he said so three times — "не не, не, это неправильно. Это это неправильно, вау[,] совсем неправильно" — and stated the rule that was adopted: "**мы должны синхронизировать с машиной максимально[;] если машина заблокирована, мы должны здесь тоже сказать… если дверь открыта, мы должны сказать[ —] дверь открыта. Мы не можем принимать сейчас деньги**". The behaviour already works in the build he handed Klimovich the previous day; it is untested with two SAS ports connected. See [[wiki/decisions/2026-09-15-the-flex-port-idle-screen-never-sleeps-and-the-port-mirrors-the-machine.md]].

**Three design corrections, all accepted.** He gave the balance display its final form — total in large type, the two components small beneath ("и у игрока не будет вопроса, на какие деньги играть?"); he required the mock-ups be redrawn at the Flex-Port's real screen resolution, because a finger-sized button makes the Spanish toggle "четверть экрана"; and he argued the top-up receipt should be optional rather than automatic, on paper volume — "иначе ты представь[,] сколько мы тикетов будем печатать? Просто вот пришёл человек[,] $5" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**He disagreed with Klimovich on where money actually enters.** Klimovich expects the bill validator to dominate; Pavel: "**так это 100% случаев**" for the cashier route, and pinned the vocabulary — "билл валидатор это флекс[пей,] кассир это флекс айкью" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**He asked for Biratka's field experience rather than guessing:** "Саша[,] надо будет твой экспириенс, чтобы придумать тест кейсы для этого… мы даже по имплементации не можем это всё предвидеть без вот твоих знаний". And on Wi-Fi resilience he supplied the fact that a machine already has two channels — Flex-Port and modem — so the server can still be told something when Wi-Fi fails [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

He is one of the five owners of the non-functional requirements due Monday Sept 21 ([[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]]).

## Open commitments (Sept 15 2026)

- [ ] Pavel Frolov — test that a block arriving over one SAS port is seen by the Flex-Port when two ports are connected — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] Pavel Frolov — remind [[wiki/people/genadi-peari.md|Genadi Peari]] that the magnetic stripe reader stays in Flex IQ — due at his next conversation with Genadi — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] Pavel Frolov — book a meeting with [[wiki/organizations/gli.md|GLI]] on unclaimed money if [[wiki/people/juan-martinez.md|Juan Martinez]] cannot cover it — due after Klimovich's call with Juan — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] Pavel Frolov (with [[wiki/people/andrey-bosik.md|Andrey Bosik]]) — work out whether the per-device LTE modems can back each other up when Wi-Fi drops — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] Pavel Frolov (with [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], [[wiki/people/andrey-bosik.md|Andrey Bosik]], [[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/alexander-biratka.md|Alexander Biratka]]) — write the non-functional requirements for FlexPay, Flex-Port and Flex IQ — due Monday Sept 21 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## Sept 16 2026 (8:01 AM) — two of the requirements under review are his, and he supplies the wording that fixes one of them

The third MVP 1 morning call ([[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16 2026 8:01 AM call]], Russian). Klimovich identified requirement 1378 as his — "это авторство Павла" — and requirement 1382 as his too, and Pavel wrote the replacement wording for the first live on the call: "[en]rolled kios[k] can be d[e-]en[]rol[le]d from [the] location but never from the cloud [database]" ([[wiki/decisions/2026-09-16-a-kiosk-is-de-enrolled-from-a-location-never-from-the-cloud-database.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**His process proposal, not yet built:** a filter showing the live requirements from all four authors — "может нам сейчас сделать какой[-]то фильтр, который показывает актуальные [реквайрментс], котор[ые] часть Андре[й] создавал, часть Дим[а], часть [Ир]а, часть я… и иметь этот общий список у всех" — so the team walks one shared list instead of one person's. [[wiki/people/andrey-bosik.md|Bosik]] agreed; the meeting used Irina's list for the day [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Design corrections he supplied:**

- On requirement 1382, the end states that actually exist: the player gets the card, or hits a card error, "тогда у него деньги остались на его [во]лет[е]" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- Escrow scope on FlexPay: "эскроу только… на одну последнюю купюру", and then the consequence he spotted himself — "после 1 купюры мы уже можем печатать ticket" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- On the receipt: not every top-up should create one [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- The capacity constraint is strictly per network, not per location — "если мы разделяем лакейшн на саб[-]нетворк[и], то там эта проблема снимется" — though a centralised terminal is still needed, so the qualifier buys no escape ([[wiki/decisions/2026-09-16-fifteen-flex-ports-in-mvp1-and-the-system-designed-for-ninety-nine.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- The failure case nobody had raised: a player pressing *generate ticket* on a Flex-Port while a different player stands at the FlexPay the ticket would emerge from ([[wiki/decisions/2026-09-16-a-self-service-ticket-is-collected-at-the-service-kiosk-with-a-four-digit-pin.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Two things he asked for and did not get.** He wanted the Flex-Port collect timeout configurable per location and Klimovich refused it as universal; and he wanted the day's running card total visible to the cashier, on the argument that InComm's first question will be how many cards went out today and "он скажет[:] не знаю. Сейчас я возьму калькулятор, посчитаю" — Klimovich refused to show an unofficial number to an operator ([[wiki/decisions/2026-09-16-incomm-returns-no-daily-cap-error-so-the-call-comes-to-jvl-first.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**On offline operation he took the middle position** — internet required at boot for the parameter check, short losses tolerated with a tilt after "5 минут[,] 15 минут" — and then, once Val had reversed the premise, drew the consequence that carried: "**это приводит к тому, что на подъёме устройства нам не надо требовать, чтоб был интернет обязательно**" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Open commitments (Sept 16 2026)

- [ ] Build the shared filter showing the live requirements from all four authors, so the team walks one list — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [ ] Review and update the status of every capability and requirement he authored, as Klimovich has done for his own — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

## Sept 16 2026 (12:35 PM) — the AI-conversion experiments, and the cost work on the boards

His fifth recorded appearance of the day. At the [[wiki/meetings/2026-09-16-street-machine-board-spec-and-georgia-class-a-order.md|12:35 PM alignment call]] Pavel did two distinct jobs [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**He reported the AI game-conversion experiments** — two of them, both running: generating a background video from a written description of a horizontal game's video, and rebuilding a different game with different maths for a different market under an existing vertical layout (Georgia's layout, Texas's maths). Val pressed for a unit — "**измеряется в днях[,] не в неделях**" — and **Pavel would not sign up to it**: "**можно будет это утверждать, когда … первую игру … сделаем, закроем все баги**". What he *would* state flatly is that the asset-development stretch of the pipeline "**сократится точно**". Detail on [[wiki/decisions/2026-09-14-vertical-texas-starts-from-the-georgia-coam-vertical-games.md]] (Sept-16 section).

**He drove the memory cut on the board**, and his framing of it is the record of the trade: one FRAM chip instead of six, the per-game statistics moved out to an SD card or the eMMC, and the consequence accepted out loud — "**рассчитывать, что она не всегда может быть корректно записана**". He twice flagged that the whole cut depends on a requirement nobody could confirm: "**опять[-]таки надо посмотреть по требованиям**". See [[wiki/decisions/2026-09-16-one-fram-chip-instead-of-six-and-low-power-mode-laid-in-but-not-populated.md]].

**He lost the identity argument and closed it himself.** He wanted the machine identified by the processor board — fewer parts, better fault tolerance — and when Genadi's supplier-risk counter landed, he said "**давайте тогда зафиксируемся и будем идентифицировать [по I/O борту]**" rather than press it. He then asked the question nobody could answer: what the board-change procedure is. See [[wiki/decisions/2026-09-16-machine-identity-moves-off-the-cabinet-passport-onto-jvls-own-io-board.md]].

**His unresolved position on board mounting** is on [[wiki/decisions/2026-09-16-street-machine-electronics-move-to-eye-level-and-the-monitor-opens-like-a-cupboard-door.md]]: the board fixed to the back of the TV so the LVDS is connected once and never moves, because "**[LVDS] он умрёт после 10 открытия**". Genadi did not dispute the ten-openings figure but wanted both boards together; Pavel's hinge-only-the-centre-section compromise was declined without comment.

**He also re-asked the GLI question** that had gone unanswered while Val was off the call, the moment Val returned — and got the answer. See [[wiki/decisions/2026-09-16-street-machines-skip-gli-so-no-boxes-and-no-tampers-but-nebraska-reopens-it.md]].

## Open commitments (Sept 16 2026, 12:35 PM call)

- [ ] Pavel Frolov — extend the development environment and build a new SDK targeted at the new board. Val instructed it; Pavel's read-back: "**нам надо под новую плату делать свой SDK … именно заточен[ный] под новую плату**" — due unspecified — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [ ] Pavel Frolov — finish the first AI-converted game, close its bugs, then confirm how fast conversion really is — due unspecified — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [ ] Pavel Frolov — confirm what must still be written to FRAM once the per-game statistics move out, and size the single chip accordingly — due unspecified — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

## Sept 17 2026 (8:02 AM) — he loses the capability he promoted, wins the one about basements, and finds nothing in Jira

The fourth MVP 1 morning call ([[wiki/meetings/2026-09-17-transactional-mvp1-skillpay-multi-product-and-device-network-security.md|Sept 17 2026 8:02 AM call]], Russian). [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**He had promoted capability 144 into MVP 1 before the call** — "**я это [капабилити] перенёс вверх и поставил ему MVP один**" — and watched [[wiki/people/irina-shishko.md|Irina Shishko]] take the remote-firmware half back out with the 3,000-machines argument ([[wiki/decisions/2026-09-17-bosiks-network-list-splits-between-mvp1-and-mvp2.md]]). [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**The argument he did win is the one about the field.** Against [[wiki/people/andrey-bosik.md|Bosik]]'s push for automatic route priority: "**для каких[-]то лакейш[е]нов может быть л[]т[]е вообще не работает. Вот в подвале где[-]то… А если у тебя эта [логика] прибито гвоздями, ты ничего не сделаешь**" — some locations have no LTE at all, and a hard-wired priority leaves the technician nothing to do. The manual override survived ([[wiki/decisions/2026-09-17-lte-is-the-default-route-and-the-manual-override-stays.md]]). [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**On the cashier UI he argued for fewer screens, not more.** "**зачем нам кнопку здесь нажимать?**" — show the products side by side with their fees and what each can do, wait for the scan, and let the barcode route the flow; "**Зачем континиу?**" His position was not adopted and the whole question was parked overnight ([[wiki/decisions/2026-09-17-jvl-supports-multiple-incomm-products-not-a-fixed-pair.md]]). [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**A product fact he volunteered:** he has already added cents to the Flex-Port — "**я на всякий случай в флекс[]порт сейчас добавил центы, потому что по [ACH] транзакции мы можем любую сумму туда[-]сюда загнать**" — because ACH can carry any amount even though a player can neither insert nor withdraw a fraction of a dollar. Klimovich backed it for portability ("если IQ потом куда[-]нибудь в Техас поедет"). [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**He is the one who raised KORE**, proposing JVL ask the SIM provider whether their network could confine the devices to JVL's own hosts, and separately that their API might give a direct debug channel to the devices. Bosik had never heard of KORE; Klimovich explained it and undertook to add him to the chain. Bosik's answer closed the network-side option and is why the firewall work landed on the device ([[wiki/decisions/2026-09-17-the-device-does-the-routers-job-firewall-nat-and-wan-lan-profiles-stay-in-mvp1.md]]). [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**And he searched Jira live and came up empty:** "**Я пересмотрел по логированию на клауд[-]сервер… ничего не нашёл, надо будет через Клода поспрашивать**". He also stated plainly that he does not know how to test the firewall change — "**Я не представляю, как это протестить**". [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**Val's watchdog rule is quoted by him, in Val's absence:** "**вочдог должен быть во всех устройствах. Если он вешается, он должен выходить в ребут и загружаться с нуля**" — and he identified why requirement 1030 does not transfer to Flex IQ: "**тут описание конкретное для фп 10**". [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

## Open commitments (Sept 17 2026)

- [ ] Find or create the Jira capability covering logging to the cloud server; nothing was found on the call — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [ ] Finish reworking the non-functional Flex-Port requirements with Irina Shishko and send the list to Andrei Klimovich — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

## Sept 17 2026 (10:14 AM and 12:19 PM) — he raises the one objection to the skeleton, and supplies the method that might defeat it

Both `Game_Conversion` sessions that day ([[wiki/meetings/2026-09-17-game-conversion-vertical-scene-progress.md]], [[wiki/meetings/2026-09-17-vertical-game-skeletons-and-the-art-pipeline.md]]). He chaired the four-minute stand-up and closed it on the judgement that Anton would have nothing new; on the longer session he was the only person who pushed back on Val's plan [[raw/Meeting_Transcript_Game_Conversion_Vertical_Scene_Progress-September-17-2026.md]] [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]:

- **The objection:** the pay table is laid out differently by the designer in every game and does not repeat, "**то есть вот это мы в скелет [засунуть] никак не сможем**" — that part cannot go into a skeleton. [[wiki/people/irina-shishko.md|Irina Shishko]] backed him. Val did not rule on it, and it is the open question on [[wiki/decisions/2026-09-17-hard-geometry-from-the-scene-files-and-a-vertical-skeleton-per-game-format.md]].
- **The reframing:** a grey-square game template is **comp art**, and comp art is already the skeleton — "**компарт — это по сути то и есть вот этот вот скелет, да, с положением чего-то**". This is the clearest link in the corpus between Val's new skeleton idea and the comp-art vocabulary JVL already uses ([[wiki/topics/game-art-animation-production-pipeline.md]]).
- **The possible fix, hedged:** if the pay-table frames existed in advance and positioned, generate the video first, then ask **Claude** or another AI to overlay those frames on every frame and regenerate the video with them — "**Ну так это работает, наверное.**"
- **Two small things that show how he reviews.** He had Igor squeeze the shared window until the sides were about **9:16** before accepting that the demo's proportions were a display artifact; and the one product note he volunteered was that he would have found the video more interesting with **windows lighting up and going dark in different places in the little houses** — Igor: "**если это на видео есть, то будут**".

**§15.8:** clear — engineering content only.

## Sept 17 2026 (12:45 PM) — planning is taken off him, and he raises the double-conversion problem

Two minutes after the 12:19 PM session ended, the [[wiki/meetings/2026-09-17-kleimenychev-hire-nova-direction-and-planning-handover.md|12:45 PM "General alignment" call]] took a standing job away from him and gave him a different one. [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]

- **Planning comes off him.** Val, directly: "**Паша с вас нужно снять.**" … "**Планирование.**" Plan *administration* moves to a proposed application administrator ([[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], not yet asked); Pavel and [[wiki/people/irina-shishko.md|Irina Shishko]] keep talking the plans through and correcting them, in recorded sessions. Pavel agreed in the room — "**Давайте да**", "**Хорошо**". Full record on [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]].
- **What he gets instead.** Val's stated purpose is that Pavel stops doing the work and instead "**приедете сюда в атланту и начнёте заниматься… Чемто серьёзно**" — comes to Atlanta and takes on something serious. No date.
- **The engineering point he raised, which changed the platform.** He pointed out that the running experiment converts **RAGE horizontal into RAGE vertical**, so the same games would need converting into NOVA afterwards — "**возможно, нам потом понадобится конвертация рейч тех же самых игр речь в нова**". Val's answer was to stop building games in RAGE altogether and do Texas on NOVA ([[wiki/decisions/2026-09-17-no-more-games-on-rage-and-texas-is-built-on-nova.md]]). Pavel did not respond to the ruling; Val took the silence as agreement.
- **He set the terms for the secret experiment before it was staffed.** "**Мы не знаем, стопроцентный ли получится результат или нет, то эксперимент провести можно**" — the experiment can be run provided nobody expects a guaranteed result — and the scale limit he had already given the candidate: "**мы не собираемся делать 20 игр, а потом сказать, что всё плохо и всё в мусорку**".
- **He is the channel to the new hire.** Every one of the candidate's questions reached Val through him.

**§15.8 — held on this call.** Val's stated reasons for removing planning from Pavel were a **personal assessment of Pavel** and are **not ingested**, here or anywhere. What is recorded is the change of duties and its stated purpose. No compensation material appears in either source.

## Open commitments (Sept 17 2026, 12:45 PM call)

- [ ] Pavel Frolov — with Irina Shishko, persuade Dmitri Kovalchuk to come in as application administrator — due unspecified — [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]
- [ ] Pavel Frolov — with Irina Shishko, hire [[wiki/people/sergey-kleimenychev.md|Sergey Kleimenychev]] from Monday onto the Texas and Class A direction, and keep the work in full secrecy with no consultation of [[wiki/people/lena.md|Lena]] — due Monday / ongoing — [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]
- [ ] Pavel Frolov — come to Atlanta and take on more serious work once planning is off him — due unspecified — [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]

## Sept 18 2026 (8:03 AM) — he supplies the cuts, the cost arguments and the one amendment that stops empty capabilities

The [[wiki/meetings/2026-09-18-transactional-mvp1-capability-cleanup-and-the-monday-deadline.md|fifth and final MVP 1 morning call]] before the Monday gate (Russian). He shared the board for the feature-planning half and did most of the scope-cutting.

**He is the one who says out loud that capability 144 will not fit:** "**он выглядит как отдельный проект, который явно в [MVP] один… не будет сделан[,] по крайней мере в полном его объёме**" — which is what prompted [[wiki/people/irina-shishko.md|Irina]]'s cloning method. He then found the one requirement [[wiki/people/andrey-bosik.md|Bosik]] had judged all still necessary and killed it: a master-board change must lose no money and be documented, "**но… у нас сейчас нету клауд[-]версий тикетов[,] то они… не переносятся на новое устройство… это не MVP один, значит**". [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**He asked the two-environments question and then argued the answer on testing cost.** The question — must the Flex-Port support both a SAS connection and a bill-acceptor/counter-emulation connection in MVP 1 — came out of the MudaGoose scope item being struck from capability 151; he first asked it about Flex IQ and corrected himself inside the same turn. When [[wiki/people/andrei-klimovich.md|Klimovich]] proposed dual SAS only, Pavel's support was concrete: "**поддерживать оба — это почти икс 2 тестирования**", and he attached the price — automate the tests now so the second environment can be covered quickly later. See [[wiki/decisions/2026-09-18-mvp1-supports-dual-sas-only-and-locations-are-chosen-to-match.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**His amendment on empty capabilities is the process contribution.** Where a capability describes functionality that already works, what goes under it is not a feature but **test executions**: "**то, что уже работает[ —] нам там надо добавить будет тест[-]экзекушен[ы]… и эти самые автоматизированные тесты. Тогда [у] нас не будет пуст[ых капа]билити**". [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**Three more calls of his** [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]:

- **He took capability 180 off a developer.** "**на Александре[ —] вот это вот на Александре неправильно висит**", then "**Перевесь на меня лучше тогда**".
- **He priced the single-product fallback for 178 as small:** "**со стороны сервера это можем очень легко сделать[,] в интерфейс добавить для оператора**", needing card data from InComm and a graphical check.
- **He raised the audit ticket** — the daily audit printout at a location — which turned out to be Klimovich's own unfinished capability, and he chased the **receipt format** after Klimovich had left the call: "**конкретный ор[дер], что там печатать[,] это от Андрея**", who "**до сих пор не сказал**". The team can print fields by its own judgement; the order and content are the product owner's.

**On his own features** he planned 165, FlexPort 9 and 10 and 173 — 160 was also named as his, without a scheduling action recorded — and found one in-progress feature with no commit against it — "**Комитет тут есть? Нет**" — which he has to trace to a branch before deciding whether to close it as a duplicate: "**[в] какую ветку оно [в]мерж[ило]сь**". [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**He is working Sunday**, per Irina's answer for both of them. [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## Open commitments (Sept 18 2026)

- [ ] Pavel Frolov — plan his own features (165, FlexPort 9 and 10, 173; 160 was also named as his) and check which branch the in-progress feature with no commit against it merged into, before deciding whether to close it as a duplicate — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] Pavel Frolov and [[wiki/people/irina-shishko.md|Irina Shishko]] — walk the non-functional requirement list together, Flex-Port side first — due unspecified, intended before the Monday gate — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]
- [[raw/Meeting_Notes_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]
- [[raw/Meeting_Transcript_Game_Conversion_Vertical_Scene_Progress-September-17-2026.md]]
- [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]
- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]

- [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Notes_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- [[raw/Meeting_Notes_Flex_POS_Alpha_and_OMNI_2_Architecture-April-15-2026.md]]
- [[raw/communication_break_down_Minsk-March-5-2026.md]]
- [[raw/Mutual_standing-Communication_breakdown_Minsk.md]]
- [[raw/Meeting_Transcript_Review_of_Engineering_Guides-March-27-2026.md]]
- [[raw/Meeting_Notes_Review_of_Engineering_Guides-March-27-2026.md]]
- [[raw/Meeting_Transcript_OMNI_Architecture_Challenge-March-27-2026.md]]
- [[raw/OMNI_Architecture_Challenge-March-27-2026.md]]
- [[raw/Meeting_Transcript_initiative_priority_schedule-1-March-26-2026.md]]
- [[raw/Meeting_Transcript_initiative_priority_schedule-2-March-26-2026.md]]
- [[raw/Meeting_Notes_initiative_priority_schedule-March-26-2026.md]]
- [[raw/Schedule_review_Nebraska-March-5-2026.md]]
- [[raw/Schedule_review-March-4-2026.md]]
- [[raw/Schedule_Nebraska-February-27-2026.md]]
- [[raw/tasks_planning_alignment-February-26-2026.md]]
- [[raw/JIRA_Planning-February-26-2026.md]]
- [[raw/Call_Genadi_Peari-February-12-2026-1.md]]
- [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md]]
- [[raw/Claude_Code-Dzmitry.md]]
- [[raw/Claude_Code-Dzmitry (1).md]]
- [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- [[raw/Claude Code integration - continued.md]]
- [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]
- [[raw/JVL_Dwolla-november-5-2025.md]]
- [[raw/Payment HUB_ACH module specification_05.11.25 .md]]
- [[raw/Payment HUB_ACH module specification_06.11.25.md]]
- [[raw/Payment HUB_ACH module specification_10.11.25.md]]
- [[raw/specification_standards_review-september-22-2025.md]]
- [[raw/back-end_architecture_blueprint_review.md]]
- [[raw/fast-passing-general-alignment_stand-up-september-10-2025.md]]
- [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]
- [[raw/CMS- Block Diagram_Arch.md]]

- [[raw/2025-08-06_Flex-POS-Mid-Iteration-Sync.md]]
- [[raw/Flex-Port-use_case-August-6-2025.md]]
- [[raw/Flex Capabilities Weekly Update-september-3-2025.md]]
- [[raw/top_level_architecture_back-end-september-9-2025.md]]
- [[raw/POS_spatial_planning-september-9-2025.md]]
- [[raw/backend_architecture-august-14-2025.md]]
- [[raw/Transactional-Architecture-Discussion-2025-07-29.md]]
- [[raw/transactional_architecture-july-31-2025.md]]
- [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- [[raw/OMNI schedule review.md]]
- [[raw/alignment-planning-catch-up.md]]
- [[raw/incomm_jvl_alignment-june-23-2025.md]]
- [[raw/OMNI_schedule_grooming-june-26-2025.md]]
- [[raw/jira_plans_maturity-mat-29-2025.md]]
- [[raw/games_performance_review_juan_martinez-may-30-2025.md]]
- [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]
- [[raw/GitHub repository structure.md]]
- [[raw/jp_treatment-may-28-2025.md]]
- [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]
- [[raw/github _structure-pavel-aaron-andrei.md]]
- [[raw/the_importance_of_storing_artifacts_in_git.md]]
- [[raw/meter_sas_function-june-10-2025.md]]

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
- [[raw/components_objectives_for_a_follow_up_meeting.md]]
- [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- [[raw/flex_pay_tito_smib_port-april7-2025.md]]
- [[raw/SMIB_FlexPay_Action_Items_April_2_2025.md]]
- [[raw/flex_pay_evolution-april-8-2025.md]]
- [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]]
- [[raw/evolution_flex_pay-april-11-2025.md]]
- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- [[raw/fkex_pay_evolution-apr-16-2025.md]]
- [[raw/ris_business_central_integration-april-3-2025.md]]
- [[raw/tech_and_settings_issues-juan_martinez-april-3-2025.md]]
- [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- [[raw/omni_calle_ocho_scheduling-apr-22-2025.md]]
- [[raw/evolution_flex_port-apr-23-2025.md]]
- [[raw/flex_pay_port_hardware_update-may-8-2025.md]]
- [[raw/activeMQ_upgrade-may-12-2025.md]]
- [[raw/flex-port_flex-pay_smib_update-may-20-2025.md]]
- [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]
- [[raw/schedule_review_omni-june-12-2025.md]]
- [[raw/qa_engineering_direction_review_aaron-june-12-2025.md]]
- [[raw/about_tickets_redemption-gcoam-june-18–2025.md]]
- [[raw/flex-POS_design-june-19-2025.md]]
- [[raw/flex_POS-use_case_architecture_requirements-june-19-2025.md]]
- [[raw/Meeting_Notes_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Notes_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- [[raw/Meeting_Notes_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [[raw/Meeting_Notes_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Notes_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
- [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
- [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- [[raw/Meeting_Notes_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
