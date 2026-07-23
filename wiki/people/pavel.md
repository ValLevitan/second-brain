---
type: person
title: Pavel
date: 2026-07-12
aliases: [Pavel, Pasha, Pavel Frolov]
disambiguation: "JVL Minsk engineering director (Pavel Frolov). Pavel cluster (2): [[wiki/people/pavel.md|Pavel Frolov]]=JVL Minsk engineering director / [[wiki/people/pavel-studio-owner.md|Pavel]]=external Ukrainian outsourcing-studio owner. Resolve by context; queue if none."
source-count: 87
open-commitments: 7
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

## Sources

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
