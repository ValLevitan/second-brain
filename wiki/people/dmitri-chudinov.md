---
type: person
title: Dmitri Chudinov
date: 2026-07-13
aliases: [Dmitri Chudinov, Dmitry Chudinov, Dima Chudinov, Dzmitry Dudzinau, Dzmitry, Dzmitry Chudzinau, Dima]
disambiguation: "Back-end architect / Java (Belarusian spelling Dzmitry Dudzinau; the "Dzima" backend). Dima/Dmitry cluster (3, owner-ruled): [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]=IT / [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]]=Senior 3D designer / [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]=back-end. Resolve by context; queue if none."
source-count: 27
open-commitments: 3
open-questions: 0
---

# Dmitri Chudinov

Dmitri Chudinov is a JVL **back-end architect / Java developer** (owner ruling 2026-07-13). Backend, Java, and server-architecture contexts resolve to him. His name also appears in the Belarusian spelling **Dzmitry Dudzinau** — the same person; canonical is **Dmitri Chudinov**, with Dzmitry Dudzinau / Dzmitry / "Dima Chudinov" / Dima kept as aliases. (Owner correction is its own citation.)

## Role

- Owns the **"Observability Platform" GitHub org** — the CMS-replacement backend — in the Feb 11 2025 repo-structure session, where the transcript renders his name as "Dima Chudinov." See [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]]. [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- **Legacy-CMS requirements lead (Mar 23 2025):** the "Dima" who produced the whiteboard **CMS legacy block diagram**, and who (with [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]]) drafts the CMS requirements and proposes the microservices/repo architecture. Context (CMS/backend/architecture) resolves this "Dima" to Chudinov. See [[wiki/decisions/2025-03-23-migrate-legacy-cms-svn-to-github-by-features.md]] and [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]. [[raw/cms_persona_requirements-march-23-2025.md]]
- **FlexPort back-end debugging (Mar 25 2025):** on the embedded standup the transcript names "Чудинов" (Chudinov) as the one to pair with [[wiki/people/eugine-yavorski.md|Yavorski]] on FlexPort logs. Notably, Val describes this Dima as **moonlighting** — he has a day job and can only work FlexPort around it (reachable ~7–11am Toronto time), which Val treats as a scheduling constraint. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-03-25.md]]

- **FlexPay backend author (stated Mar 27 2025):** on the English scope-gap meeting Pavel described the FlexPay software stack as "backend introduced by Dima, and frontend implemented by Igor Hrybko and Anton Seregin" (HTML5/JavaScript GUI) — backend context resolves this Dima to Chudinov; he would add/extend the small ticket-number server for the TITO MVP. See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- **FlexPay TITO scope-gap (Mar 28 2025):** on the TITO meeting the transcript names "Дима Чудинов"; he takes part in the SAS-server / WSS-protocol design (e.g. that the SAS test-tool functionality can be reused) and is tasked to **send Eugine the list of SAS commands** to implement first. See [[wiki/decisions/2025-03-28-flexpay-support-tito-non-jvl-locations.md]]. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## The back-office monolith one-on-one (~Mar 19 2025, date inferred)

A Russian one-on-one with Val (see [[wiki/meetings/2025-03-19-back-office-architecture-chudinov.md]]), triggered by a **QR-code failure**, in which Chudinov explained and defended the back-office server he owns: [[raw/back_office_next_step_forward_dzima_chudinov.md]]

- **How the QR flow works:** scanning the QR turns the picture into a URL-style request carrying the machine's address, identity, and statistics; the server checks the machine exists, saves the statistics, verifies the machine still has a working **"Лиза"** (lease/license), and if so issues a new apply-code back to the machine — a small piece of information travelling from machine, through the user's phone, encrypted. [[raw/back_office_next_step_forward_dzima_chudinov.md]]
- **Why it broke:** hard to say — the server uses third-party application libraries he called "morally outdated"; this error had never occurred before and can't even be handed to QA to reproduce. [[raw/back_office_next_step_forward_dzima_chudinov.md]]
- **The monolith:** "99%" of the work today is **one application on one server with one database** ("MainJVL Server" on his diagram) that does everything — issues leases, saves statistics, machine creation/installation/remote setup and more — so any update or outage takes *all* functions down (QR and online lease issuance, statistics, registration). His proposed direction: **break the monolith into functional services**, starting with the most business-critical (leases and statistics), with DevOps-level parallel service redundancy later. [[raw/back_office_next_step_forward_dzima_chudinov.md]]
- **The diagram fight:** he had drawn a current/future diagram in **Mermaid** (25 minutes' work, after checking with an Andrei about the Confluence whiteboard — see the meeting stub for the unresolved Andreis); Val was angry that his emailed instruction to move diagrams to **Confluence** (which has a whiteboard) had been set aside, and that no proper as-is architecture diagrams exist at all. Chudinov said his Miro exports are saved and he'll transfer them when time frees up; his position was that the architecture hasn't changed so redrawing the as-is has little point — Val insisted the as-is must be drawn before any move-forward can be assessed, and Chudinov agreed. [[raw/back_office_next_step_forward_dzima_chudinov.md]]
- **Workload:** he protested being asked for a full solution in a 20–30-minute slot while carrying a "burning FlexPay" (горящий FlexPay); he asked to finish the FlexPay work first. Estimate for assembling the architecture schemas: **"a couple of days… maybe by the end of next week."** Val said he would schedule a **two-hour architecture meeting on Thursday at 8 am**. [[raw/back_office_next_step_forward_dzima_chudinov.md]]
- Val's method suggestion to him: **record yourself on audio narrating the architecture diagram**, feed it to **ChatGPT**, and let it produce a concise story and diagram to rework before showing the group. Chudinov agreed. [[raw/back_office_next_step_forward_dzima_chudinov.md]]

*(Note: by Mar 23 a "CMS legacy block diagram" whiteboard by Dima existed — see [[wiki/decisions/2025-03-23-migrate-legacy-cms-svn-to-github-by-features.md]] — which may be this deliverable or part of it; the sources don't connect them explicitly, so the commitment below stays open.)*

## CMS requirements-review follow-up (~Mar 25 2025, date inferred)

On the Russian follow-up ([[wiki/meetings/2025-03-25-cms-requirements-review-workflow.md]]) the "Dima" is the legacy-CMS co-owner (backend context → Chudinov): [[raw/cms_requirements_development-dzima-sergei-andrei.md]]

- He is one of the **two people the legacy CMS rests on** — Val: everything "держится на честном слове" between him and Sergey; "Если сегодня вас, Дима, нет, и я даже не знаю, что с этим делать." [[raw/cms_requirements_development-dzima-sergei-andrei.md]]
- **Pushed back on the rebuild path:** adapting the current CMS to new requirements would be "гораздо быстрее" than a new separate system; asked what happens if Omni ships first and they become incompatible; noted his honesty angle ("Если бы я был плохим разработчиком, конечно, мне выгоднее 10 лет что-то делать"). Val disagreed "в корне" — see [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]. [[raw/cms_requirements_development-dzima-sergei-andrei.md]]
- Scope points he raised, ruled in-platform by Val: **прогрессив и розыгрыш** are part of the CMS platform; some long-unused functionality (e.g. **Italy**) can be dropped in the move. [[raw/cms_requirements_development-dzima-sergei-andrei.md]]
- Committed (with Sergey) to re-review the AI-generated overview/use cases/requirements and add the missing **таксоны** (taxonomies) by the booked Thursday meeting. [[raw/cms_requirements_development-dzima-sergei-andrei.md]]

**Distinct people (do not merge), all sometimes called "Dima":** [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] (IT), [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]] (Senior 3D Graphic Designer), and [[wiki/people/andrew-khandov.md|Andrey/Andrew Khandov]] (Miranda developer). Resolve every bare "Dima" by context, never by name alone.

## History

- **SQL/OLAP architecture, part 2 (~2024, likely Q4):** provisionally, the "Dima" Val introduces with "Dima and Sergei are designing back office solutions, back office architecture" — the back-office/architecture context fits Chudinov (who later leads the CMS-replacement backend with the same Sergey), but [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] (the MS-SQL Dima) is also plausible; **flagged, not certain**. Part 1 also notes a "Дима" should join "по поводу флэкспей, портов флэкспей" — consistent with Chudinov's later FlexPort role, likewise flagged. See [[wiki/meetings/2024-sql-olap-visualization-architecture-2.md]]. [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]] [[raw/architecture_sql_olap_visualization_1_2025-03-29.md]]

## FlexPay/TITO protocol work (Apr 1–7, "Дима" by context — inference)

- **Apr 1:** the standup's "Дима" (backend context — consistent with the Mar-25/Mar-28 attributions) reported his protocol document ready ("немножко там подфикшу"), sized taking it into work at **~a week of full load**, proposed **mirroring all SAS traffic onto FlexPay** for per-machine debugging ("Дима это будет всю базу писать" — he writes the FlexPay base for it), and was to write up the **stories** with Pavel (cash-out + SAS-command logging commands for the WSS protocol); interface changes with "Игорь" possible "по мере поступления." Alekseev studying "документы, которые Дмитрий приготовил" also evidences the Mar-28 SAS-command-list commitment delivered (moved to History below). See [[wiki/meetings/2025-04-01-flexport-flexpay-dev-update.md]]. [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- **Apr 7:** on the architecture meeting the WSS protocol commands between SMIB and FlexPay were "probably… already done in terms of implementing the commands. I assume by Dima, right? Okay, great" — pending testing/interoperability with Evgeny. [[raw/flex_pay_tito_smib_port-april7-2025.md]]

## Open commitments

- [ ] Dima Chudinov — assemble and properly format the back-office architecture schemas (as-is + future) for the Thursday 8 am architecture meeting — due "a couple of days… maybe end of next week" — [[raw/back_office_next_step_forward_dzima_chudinov.md]]
- [ ] Dima Chudinov (with Sergey Tsymanov) — re-review the AI-generated CMS overview/use cases/requirements and add the missing taxonomies — due by the booked Thursday meeting (~Mar 27, inferred) — [[raw/cms_requirements_development-dzima-sergei-andrei.md]]
- [ ] Dima Chudinov — take the SAS/protocol document into work (~a week of full load) and write the stories with Pavel (cash-out + SAS-command logging over WSS) — due week of Apr 1 2025 — [[raw/flex-port_pay_dev_update-april-1-2025.md]]

## History (discharged)

- [x] Dima Chudinov — send Eugine the minimal list of **SAS commands** to implement first for the TITO/SAS-server work — **evidenced delivered by Apr 1** (Alekseev had studied "документы, которые Дмитрий приготовил"). [[raw/scope_gap_tito_flex_pay-march-28-2025.md]] [[raw/flex-port_pay_dev_update-april-1-2025.md]]

## RIS software-licensing enforcement (Apr 3)

On the RIS ↔ Business Central licensing meeting ([[wiki/meetings/2025-04-03-ris-business-central-licensing.md]]) the transcript names "Дима" as the backend owner of the **RIS-manager** side of license enforcement; Val named the two responsible parties as **Lev Rudky** (Business Central export) and **Dima Chudinov** (RIS side). Backend/architecture context resolves this Dima to Chudinov. See [[wiki/decisions/2025-04-03-license-software-per-operator-not-machine.md]]. [[raw/ris_business_central_integration-april-3-2025.md]]

## CMS migration verdict + manifests priority (Apr 14–15)

- Led the developer side of the Apr 14–15 CMS sessions ([[wiki/meetings/2025-04-14-cms-svn-github-product-repos.md]], [[wiki/meetings/2025-04-15-cms-migration-staged-decision.md]]): argued that splitting the legacy monolith across repos "будут очень болезненные процессы, очень долгие … мы можем упереться во многие проблемы и просто застрять," that the CMS is really ~10 modules plus a big Core and a **monolithic database** best not split, and proposed migrating **as-is** — the position that became the team verdict behind [[wiki/decisions/2025-04-15-cms-staged-migration-plan.md]]. Scope he listed: ~15 SVN repositories. [[raw/cms_svn_github-april-14-2025.md]] [[raw/cms_github_svn-apr-15-2025.md]]
- His live workstreams named on Apr 15: software-licence work for clients, and ongoing **FlexPay server-side tweaks** — "по FlexPay, я постоянно веду некоторые доработки, чтобы иметь возможность получать логи и смотреть … работоспособности терминала." He owns initiating the **manifests-product** meeting (with Pasha and "всеми заинтересованными") and, with Tsymanov, sizing the SVN→GitHub transfer against Val's five-day rule. [[raw/cms_github_svn-apr-15-2025.md]]

## Apr 15 2025 — the mini SAS server

On the SMIB weekly ([[wiki/meetings/2025-04-15-embedded-group-smib-sas-printer.md]]) "Дима Чудинов" is building the **mini SAS server** on the FlexPay kiosk — it generates the barcode validation that the SMIB requests when a player prints a ticket. Targeted, with the temporary SMIB (a screenless FlexPort board) and the FlexPort firmware-update path, for the **end-of-April** TITO milestone. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/weekly_embedded_group_flex_port_progress-apr-15-2025.md]]

## May 8 2025 — SAS protocol owner on the TITO standup

On the [[wiki/meetings/2025-05-08-flexport-flexpay-tito-standup.md|May-8 FlexPort standup]] Dima Chudinov is named as the author of the **protocol commands** Yavorski works against ("Дима Чудинов вам предоставил в этом протоколе"); Val asked "Дима и Паша" to think through what remains for the **final delivery** of Yavorski's FlexPort project beyond the daily action list. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex_pay_hardware_update-may-8-2025.md]] [[raw/flex_pay_port_hardware_update-may-8-2025.md]]

## May 10 2025 — the escalation contact for the FlexPort protocol bug

On [[wiki/people/eugine-yavorski.md|Yavorski]]'s weekend debug update ([[wiki/meetings/2025-05-10-flexport-flexpay-debug-update.md]]) Yavorski said that if his own side proves clean, he'll write "**Диму**" (Dima) — and phone him — for help on the FlexPort↔FlexPay protocol error ("ticket null, code 0"). Backend/protocol context resolves this Dima to Chudinov. [[raw/flex-port_flex-pay_update-may-10-2025.md]]

## May 12 2025 — owns the Java-app side of the ActiveMQ / White Area Host fix

On the ActiveMQ security-upgrade call ([[wiki/meetings/2025-05-12-activemq-white-area-host-upgrade.md]]) Dima Chudinov (Java/back-end context) owns the JVL application ("White Area Host" / CASWH) that carries the vulnerable ActiveMQ broker; he explained the RAM-only botnet exploit, laid out the three fix options (upgrade + split; Docker isolation; deferred third), and scoped the work — assigning the hands-on ActiveMQ/OS work to an engineer transcribed "Sergei Sandriev" (with Andrei Bosik on the OS layer). See [[wiki/decisions/2025-05-12-upgrade-activemq-split-from-white-area-host.md]] and [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/activeMQ_upgrade-may-12-2025.md]]

## May 15 2025 — partial-redemption-to-card + machine-info field

On the May-15 FlexPay/FlexPort progress meeting ([[wiki/meetings/2025-05-15-flexpay-flexport-progress.md]]) Chudinov owns completing **partial redemption to card** on the FlexPay kiosk in the May-27 window, and reported he had added a machine-info field to FlexPay carrying what little SAS exposes (machine number + protocol version). Detail on [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-pay_flex-port_update-may-15-2025.md]]

## May 20 2025 — FP256 negative cases; remote-update; Dropbox rejected

On the [[wiki/meetings/2025-05-20-flexport-flexpay-smib-action-review.md|May-20 SMIB action review]] Chudinov's **FP256 partial-redemption-to-card** positive cases were done (May 16), negatives in progress (~May 21); he must provide the **API** for the new amount-selection UI screen [[wiki/people/ihar-hrybko.md|Igor Hrybko]] is drawing, and was newly assigned the **simultaneous-dual-architecture connection protocol** (Temporary Wallet + TITO). He begins **remote firmware update** with [[wiki/people/eugine-yavorski.md|Yavorski]] on May 21. His plan to store firmware on **Dropbox was flatly rejected by Val** in favour of a proper artifact store (Nexus/Azure). His FlexPay-Tito work was also referenced on the same-day [[wiki/meetings/2025-05-20-flexpay-flexport-test-plan.md|test-plan meeting]]. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-port_flex-pay_smib_update-may-20-2025.md]] [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]

## May 29 2025 — e-Wallet/TITO action-list review

On the implementation review ([[wiki/meetings/2025-05-29-ewallet-tito-flexpay-implementation.md]]) Chudinov confirmed **partial redemption is done** (in beta, with the API for [[wiki/people/ihar-hrybko.md|Ihar Hrybko]]'s FlexPay UI). His action item: change the E-Wallet software-update transfer from **64KB → 8KB packets** (Yavorski found 64KB "hangs stably"; 8KB works), then sequence the ~8000 fragments with acknowledgements. He confirmed the packet-size change is no problem; Val/Pavel pushed him to deliver a test build (a couple of known-structure 8KB packets) by the weekend so Yavorski can test Monday — but Yavorski still needs help loading firmware onto a kiosk. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]

## Aug 14 2025 — backend-architecture kickoff (present; CMS knowledge-holder)

Chudinov attended the [[wiki/meetings/2025-08-14-backend-architecture-cms-transactional-hhr.md|backend-architecture kickoff]] (transcribed as the transcription owner "**Dzmitry Chudzinau**") as the team's back-end/CMS tribal-knowledge holder. He was largely a listener, but Val repeatedly named him as the person who can produce the CMS block diagrams/schematics on request ("if I ask Dima where is the block diagram… it most likely exists"); Aaron and Pavel framed the whole exercise as extracting the CMS's purpose/architecture from Dima's head into documented repositories so others can extend it. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]. [[raw/backend_architecture-august-14-2025.md]]

## Nov 5–10 2025 — ACH-module spec author + back-end lead on the payment hub

Across the three ~7 AM ACH-module spec-review sessions (transcribed "Dzmitry Chudzinau") Chudinov is the back-end engineer who **authored the ACH-module requirement documents** the team walked through — invoice-state requirement (FR106), the Dwolla adapter (FR101), payment-processor/provider routing, and the terminal/passport/location-registration write-ups — and who will produce the module and adapter schemas/state diagrams. He drove the open architecture questions: how to route/assign an ACH provider per location during a switch, and how a customer's bank account attaches to the internal location entity (favouring the **Plaid**-hosted approach so no bank numbers are stored). *(The ~7 AM meeting slot fits his known moonlighting availability window.)* Substance on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Nov 5–10 ACH-spec arc). [[raw/Payment HUB_ACH module specification_05.11.25 .md]] [[raw/Payment HUB_ACH module specification_06.11.25.md]] [[raw/Payment HUB_ACH module specification_10.11.25.md]]

## Sources

- [[raw/Payment HUB_ACH module specification_05.11.25 .md]]
- [[raw/Payment HUB_ACH module specification_06.11.25.md]]
- [[raw/Payment HUB_ACH module specification_10.11.25.md]]
- [[raw/backend_architecture-august-14-2025.md]]
- [[raw/architecture_sql_olap_visualization_1_2025-03-29.md]]
- [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]
- [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]]
- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [[raw/cms_persona_requirements-march-23-2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-25.md]]
- [[raw/back_office_next_step_forward_dzima_chudinov.md]]
- [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- [[raw/cms_requirements_development-dzima-sergei-andrei.md]]
- [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- [[raw/flex_pay_tito_smib_port-april7-2025.md]]
- [[raw/cms_svn_github-april-14-2025.md]]
- [[raw/cms_github_svn-apr-15-2025.md]]
- [[raw/ris_business_central_integration-april-3-2025.md]]
- [[raw/weekly_embedded_group_flex_port_progress-apr-15-2025.md]]
- [[raw/flex_pay_hardware_update-may-8-2025.md]]
- [[raw/flex_pay_port_hardware_update-may-8-2025.md]]
- [[raw/flex-port_flex-pay_update-may-10-2025.md]]
- [[raw/activeMQ_upgrade-may-12-2025.md]]
- [[raw/flex-pay_flex-port_update-may-15-2025.md]]
- [[raw/flex-port_flex-pay_smib_update-may-20-2025.md]]
- [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]
