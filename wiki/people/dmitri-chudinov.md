---
type: person
title: Dmitri Chudinov
date: 2026-07-13
aliases: [Dmitri Chudinov, Dmitry Chudinov, Dima Chudinov, Dzmitry Dudzinau, Dzmitry, Dzmitry Chudzinau, Dima]
disambiguation: "Back-end architect / Java (Belarusian spelling Dzmitry Dudzinau; the "Dzima" backend). Dima/Dmitry cluster (3, owner-ruled): [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]=IT / [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]]=Senior 3D designer / [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]=back-end. Resolve by context; queue if none."
source-count: 63
open-commitments: 29
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

## Sept 2 2026 — the Flex-IQ pre-pilot code owner and the remote-update builder

Present on the [[wiki/meetings/2026-09-02-flex-iq-pre-pilot-updates-after-the-show.md|Sept-2 Flex-IQ pre-pilot call]] (Russian) under the speaker label **"Dzmitry Chudzinau"** — a Belarusian-spelling variant already carried in his aliases. Backend/terminal-software context resolves it to him. [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

- **He carries all three pre-pilot IQ changes in code.** "по всем трём задачам с точки зрения кода мы можем сделать это вот буквально даже до конца недели. Единственный момент… С железом" — hardware is the only sticking point; his fallback is to build a version and let Andrei run it on a test terminal [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **He raised the objection that shaped the barcode ruling** — that the barcode carries no card number "в привычном понимании пользователя," so the last-four-digits convention used by Visa/Mastercard would be unavailable and incident investigation hampered. Andrei's answer (same barcode on card and envelope; the player calls InComm, not the location) settled it; Chudinov: "Хорошо." See [[wiki/decisions/2026-09-02-activate-incomm-cards-by-barcode-on-flex-iq.md]] [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **He had already proved the scan works** — a test application scanning JVL's test cards, "всё работает" — leaving only "Доработать функционал вместо свайпа сканирования" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **He owns the remote software update, and reported it harder than expected** because the team chose to go through Amazon, pulling in terminal-side and Kubernetes work "по всем слоям." CI publishes builds to Amazon storage with fast download and no GitHub access needed; an operator role on JVL's transactional dashboard lists terminals and what is installed, selects terminals and the latest or a chosen bundle, deploys online, and forces or schedules a reboot, "зачастую ночью." He built it deliberately extensible to future terminals "типа flex pay, [recycler]," and will test rollback. Detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept-2) [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]] [[raw/Meeting_Notes_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **He named wallet storage as the one open design question blocking him:** "Локальное хранение [и]летов, либо глобальное облачное, потому что все остальные решения у нас так или иначе уже есть" — printer and Flex-Port work exist and only need integrating. See [[wiki/decisions/2026-09-02-e-wallets-move-to-the-cloud.md]] [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **On firmware-update frequency** he judged a change to SAS itself unlikely and JVL-side implementation more likely — "скорее мы решим доимплементировать недостающие команды" — with any new statistics, counters, equipment or capability requiring an update [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Open commitments (Sept 2 2026)

- [ ] Implement all three Flex-IQ pre-pilot changes in code — barcode activation, ticket-receipt printing, flow/screen cosmetics — due end of week — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [ ] Finish the remote software update and begin testing it, rollback to the last working version included — due finish end of week, test the following week — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [ ] Design the wallet-storage system for the cloud model — due unspecified — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Open commitments

- [ ] Dima Chudinov — assemble and properly format the back-office architecture schemas (as-is + future) for the Thursday 8 am architecture meeting — due "a couple of days… maybe end of next week" — [[raw/back_office_next_step_forward_dzima_chudinov.md]]
- [ ] Dima Chudinov (with Sergey Tsymanov) — re-review the AI-generated CMS overview/use cases/requirements and add the missing taxonomies — due by the booked Thursday meeting (~Mar 27, inferred) — [[raw/cms_requirements_development-dzima-sergei-andrei.md]]
- [ ] Dima Chudinov — take the SAS/protocol document into work (~a week of full load) and write the stories with Pavel (cash-out + SAS-command logging over WSS) — due week of Apr 1 2025 — [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- [ ] Dima Chudinov (with [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]]) — produce the **production-side migration estimate** for moving the CMS/CASS codebase to cloud (framework version bumps, SQL/stored-procedure conversion, LDAP→Entra auth rewrite), straight-line, no optimization — due next Monday (~Mar 30 2026) — [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]

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

## Feb 5 2026 — the Flex-Pay kiosk + backend owner (responsibility-split briefing)

A JIRA-sourced briefing prepared for [[wiki/people/aaron.md|Aaron]] ([[wiki/meetings/2026-02-05-flexpay-flexport-wss-responsibility-briefing.md]]) mapped the FlexPay↔FlexPort WSS responsibility split. Chudinov (named "Dzmitry Chudinov") owns the **Flex-Pay** end. [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]

- **Primary domain:** the **Flex-Pay kiosk application software** (the payment terminal the player uses). He **implements the WSS protocol on the Flex-Pay side** and expanded it for **SAS Cashout, SAS Ticket-In, and SAS logging** (**FP-250, FP-251, FP-252**). [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]
- **Cash:** processes incoming WSS cash messages on the kiosk, manages transaction confirm/cancel logic, and handles payment-processor integration (**InComm, Pyramid**). **Firmware:** triggers/manages remote firmware-update delivery from the server/kiosk side (**FP-181, FP-208**). **Logging:** receives/stores Flex-Port logs on the kiosk and exports them for support (**FP-210**); builds backend ticket/report history (**FP-270**). **Security:** encrypted WSS on the kiosk side (**FP-9**). **TITO:** full kiosk integration — ticket creation/validation/redemption, HandPay/JackPot support (**FP-253, FP-255, FP-267, FP-268**). [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]
- **Server/backend (his alone):** Payment Hub API, server registration, time sync, CMS/orchestration integration, InComm parameter management (**BEP-2644, BEP-2213, BEP-2257**). [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]
- **Status:** **7 To Do** (including API expansion for negative Flex-Port scenarios due **2/9**, TITO SAS integration, remote firmware triggering); **21 Closed / 2 Done** — a strong delivery track record on WSS-protocol expansion and kiosk features; recent bug fixes completed (**FP-516, FP-517, FP-518** — incorrect transaction status, cash balance after cancel, cash-category distribution). [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]
- The briefing frames him as the **kiosk application developer** taking [[wiki/people/eugine-yavorski.md|Yavorski]]'s protocol messages and implementing them on the Flex-Pay terminal plus all server/backend integration — dependent on Yavorski for the protocol specification (see the single-point-of-knowledge note on [[wiki/people/eugine-yavorski.md]]). [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]

## Feb 9 2026 — Claude Code onboarding + the company-wide-conventions push

- **Onboarding session** ([[wiki/meetings/2026-02-09-claude-code-onboarding-chudinov.md]], 1h46m, transcribed "Dzmitry Chudzinau", [[wiki/people/pavel.md|Pavel]] translating): Chudinov had used Claude Code to generate a **Flex-POS server-connection feature** (a client connecting to the server from a non-registered terminal; environment built with **Docker**) — Claude generated the code + tests, he reviewed it by hand and had **ChatGPT/OpenAI compare his approach against Claude's** (OpenAI judged his own approach better), and had not yet opened a pull request. [[wiki/people/aaron.md|Aaron]] coached him on treating language models as "the new compiler layer" (curate intentions/specs; build linter/static-analysis/test guardrails; capture conventions as Claude Code "ways" and "skills"), and generated a **spring-coding-conventions** doc from Chudinov's constructor-dependency-injection / Spring best-practice preferences. Substance on [[wiki/topics/ai-assisted-development.md]] (Feb-9). [[raw/Claude_Code-Dzmitry.md]]
- **Internal debrief** ([[wiki/meetings/2026-02-09-claude-code-chudinov-internal-debrief.md]], 12m, no Aaron): Chudinov argued the coding-conventions/rules document should live **"one level higher" as a company-wide JVL standard** shared across the ~ten Spring applications in development (not copied project-to-project, "otherwise one person won't follow it and it diverges"), to be worked out with **Andrei**; and that the team should try to build the framework themselves and escalate to Aaron only with a concrete question and a structured plan. [[raw/Claude_Code-Dzmitry (1).md]]

## Mar 23 2026 — data-access strategy; owns the production-side migration estimate

On the data-access-strategy / CMS-cloud-migration call ([[wiki/meetings/2026-03-23-data-access-strategy-cms-cloud-migration.md]], 1:34pm, Russian, transcribed "Dzmitry Chudzinau"; with [[wiki/people/val-levitan.md|Val]], [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]], [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]], [[wiki/people/andrey-bosik.md|Andrei Bosik]]) Chudinov is the back-end/architecture voice: he surfaced MCP's ergonomic limits (no dropdown/no remembered selection vs an app), the Excel-file credential-security problem, and — for a full cloud migration — the technical checklist (codebase mostly modern, framework version bumps; SQL scripts/stored procedures to convert; LDAP auth replaced by Azure/Entra; migrate as-is first). He proposed **PostgreSQL** as the cheaper alternative to MS SQL. Val assigned him (with [[wiki/people/sergey-tsymanov.md|Sergey]]) the **production-side migration estimate** — straight-line, no optimization. Substance on [[wiki/topics/olap-power-bi-architecture.md]] and [[wiki/topics/ai-assisted-development.md]] (Mar-23). [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]

## Apr 15 2026 — legacy CMS docs check: migration ~99%, `cass_wah` last; docs are the rework foundation

On the [[wiki/meetings/2026-04-15-legacy-cms-documentation-progress-check.md|Apr-15 legacy-CMS docs check]] Chudinov (transcript "Dzmitry Chudzinau") confirmed the SVN→GitHub migration is ~99% complete with one small repo remaining — `cass_wah`/Casino WAH — to be moved and documented last in the same cycle, and argued the documentation pass **is** the foundation for the rework decisions: without it the team can't see what to delete, redo cheaply, or preserve, and the eventual rework must be surgical so as not to break what works. Substance on [[wiki/topics/docs-as-code-and-atlassian-exit.md]] (Apr-15). [[raw/Meeting_Notes_Legacy_CMS_Documentation_Progress_Check-April-15-2026.md]]

## Aug 24 2026 (reported) — holds prose that nobody has verified; busy and then on vacation

On the [[wiki/meetings/2026-08-24-nova-lgs-prose-standard-checkpoint.md|Aug-24 prose checkpoint]] (Russian; Chudinov **not present**) three things about him were established. [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

- **He holds prose Val produced.** Val: "все прозы, которые я сделал и всякий побился, я отправил диме чудина у и Сергею циманову." Val believes Dima never placed it next to the code — "дима её не… Положил. Рядом с скотом" — though "я у димы давно это спрашивал. Я не уверен, что сейчас." [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] used that same prose as the basis for his own front-end work. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **Nobody has confirmed that prose still matches the code.** [[wiki/people/pavel.md|Pavel]]: "нам надо подтвердить, что проза которую там есть сейчас судимые, что она соответствует действительности, уже ктото с этим поработал." [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **The work was reassigned away from him on availability grounds.** [[wiki/people/irina-shishko.md|Irina]]: "дима сейчас занят, потом дима в отпуск, а Сергей пускай сейчас этим занимается" — busy now, then on vacation, so [[wiki/people/sergey-tsymanov.md|Sergey Tsimanov]] takes it. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **He is to be consulted on the prose-writing standard.** Val, handing the standard to Vladimir and Evgeny: "вы, наверное, както соберётесь, наверное, привлёте диму чудинова, наверно, у него тоже есть какието мнения по этому поводу." His prose variant is one of the three-to-five the standard is to be distilled from. See [[wiki/decisions/2026-08-24-single-prose-writing-standard.md]]. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Sept 4 2026 — the contract-versioning problem, raised as "Dzmitry Chudzinau"

He appears in the [[wiki/meetings/2026-09-04-rage-nova-conversion-readiness.md|Sept-4 morning meeting]] attendee list under the Belarusian rendering **Dzmitry Chudzinau**, and was the meeting's most persistent sceptic on the data-contracts plan [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]].

- **The question nobody had answered:** "контракты мы везём, у нас пишется open [API;] но… мне никто пока не открывает глаза. Что делать с **версионностью**? Которые появляются после 1 же релиза." The transaction repository is single, and something must reconcile a machine already in the field against a server that has moved ahead. [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He pushed twice more.** Who releases the transaction repository on every release — "давай возьмём транзакцию флекс айкью[;] тут уже **12 репозиториев** и у каждого есть свои контракты… сейчас начнётся просто волна релизов" — and the boundary case Evgeny could not answer: "у машины… есть такой же контракт с [legacy] CMS[, с] аккаунтным хостом. Это тоже часть продукта, они тоже запекаются[?]" His own view was that they must: "ты часть всей общей системы[,] и обратно… если ктото за чтото правит там на уровне ролей, значит запекаться должн[ы]… игры." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He backed Igor's underlying question and did not accept the answer:** "Если мы это делаем для Клода, почему ему недостаточно репозитариев? Я всё равно… не понимаю." Val closed the discussion rather than answering it — see [[wiki/decisions/2026-09-04-data-contracts-closed-every-repository-by-september-11.md]]. [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **Galaxy is his, quietly.** Val, turning to him: "То же самое должно быть… сделано под Galaxy [platform;] для тех людей, которые не знают слово Galaxy, это в принципе **бывшая CMS**… дима чтото там на заднем плане ковыряется. Я не знаю, что он сделал, но когда мы придём к октябрю месяцу[,] мы начнем вплотную говорить про галакси платфо[рму]." Val also asked aloud what "дима может сделать с Сергеем Пацанова" — a name that does not cleanly match any page; by context (the CMS requirements pair) it is most likely [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]], **labelled as inference, not asserted**. See [[wiki/topics/nova-platform-architecture.md]] (Sept-4). [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]

## Sept 4 2026 — his SAS command document becomes the scope of record for the Flex-Port port (he was not on the call)

On the [[wiki/meetings/2026-09-04-flex-slim-first-ten-and-flex-port-sas.md|Sept-4 midday production call]] Chudinov's own document — the list of SAS commands he wants supported, mirroring what he supports on the WSS side — was made the scope boundary for porting SAS onto Flex-Port, over [[wiki/people/eugine-yavorski.md|Yavorsky]]'s request to narrow the task. [[wiki/people/evgeniy-alekseev.md|Alekseev]]: "есть документ, который делал… Дмитрий… И просто нужно, если этого недостаточно[,] просто чтоб дописали, какие ещё команды необходимо реализовать"; everything in it is already implemented on SMIB. Val restated it as step two of the sequence: "найти документ, который был опубликован Димой Чудиновым, которые, скорее всего, находятся в [Конфлюенс]." **Where the document lives was not confirmed** — both Val and Alekseev hedged on Confluence. Ruling: [[wiki/decisions/2026-09-04-port-the-smib-sas-module-into-the-flex-port-main-branch.md]] [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

- **Open commitment (conditional):** extend the SAS command document if the implemented set proves insufficient — named jointly with [[wiki/people/pavel.md|Pavel Frolov]] ("чтоб там Дмитрий или Павел добавил"); contingent on the stage-one test [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

## Sept 7 2026 — "implemented, but not verified", and the AFT command document lands on him

At the [[wiki/meetings/2026-09-07-sas-aft-on-flex-port-and-remote-update.md|Sept 7 10:02 engineers' alignment]] (Russian), credited in the recording as "Dzmitry Chudzinau".

- **He raised the Georgia protocol question that produced the AFT ruling:** "протокол будет в [Джордже] — это через a[ ]ft мы будем проводить?" — and asked for the PIN to be made optional, which Pavel turned into the requirement [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He gave the single most useful correction of the call.** Alekseev said the error handling and handshakes were all implemented; Chudinov: **"но реализовано, но не проверялось"** — [[wiki/decisions/2026-09-07-error-recovery-and-non-functional-requirements-come-first.md]] [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He is asked to produce the AFT command document**, matching the earlier TITO/SAS one he made, and proposed letting Claude do it across two projects at once — he named them as Flex-IQ and Flex-Port [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **The Flex-IQ barcode-activation build promised for Monday was ready:** "Готова[,] сегодня залил." He had checked it on his own terminal but preferred staging, "потому что там более правдивые данные будут" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He is finishing the remote-update system for Flex-IQ**, "к моменту релиза уже сможем," with rework still needed — the release in question was never pinned down [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He offered the pragmatic fallback for the test environment:** "проще будет запустить как… в докер[е] либо… в каком-нибудь режиме дем[о]на[,] [с] симуляцией некоторых данных" — Pavel preferred full ARM emulation and put Docker second [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He asked the question that reopened MudaGoose:** does the whole Flex-IQ flow still make sense "если мы уходим от системы [Муда]г[уз]" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]

## Open commitments (Sept 7 2026)

- [ ] Produce an AFT command document for Flex-Port matching the earlier TITO/SAS document — due unspecified, high — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] Send Andrei Klimovich the link to the new barcode-activation Flex-IQ build, preferably on staging — due Sept 7 2026 — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]

## Sept 10 2026 — he raises the requirements-ownership objection, and settles where a capability hangs

At the [[wiki/meetings/2026-09-10-capability-requirements-workflow-and-mvp-split.md|Sept-10 2026 5:31 AM transactional call]]. The speaker labels render his name "Dzmitry Chudzinau". [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

- **The objection, which is the sharpest thing said on the call.** Why should a reporter be able to file a capability with no requirements, and why should engineers stop their own work to fill his in: "можно сразу поднимать вопрос глобальнее, чтобы репортер не мог за[вод]ить cap[ab]iliti без рекла[мент]ов? В чём мы сейчас за него будем делать работу?… требования выносят[ся на] уровень бизнеса. Почему сейчас… [и]нженеры должны отвлекаться от своей работы и заполнять его работу." [[wiki/people/pavel.md|Pavel]] called it a good question and deferred it to a meeting with [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]. It is carried as an open question on [[wiki/decisions/2026-09-10-requirements-come-first-and-the-recycler-is-out-of-both-mvps.md]]. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He asked what happens when nobody knows up front how to test something** — "[а] если никто изначально не знает, как это проверить?" — producing the ruling that the acceptance criterion is written in general terms. See [[wiki/topics/test-automation-strategy.md]] (Sept 10). [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He diagnosed the filing problem from outside:** either markers or consistent naming, because the capability text alone does not say which product it belongs to — "читаешь[,] там[:] контроллер работает[; в]от к чему это [капа]билит[и] идёт[?]" [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **And he settled where a capability hangs,** which the group adopted: on the product project — Flex-IQ or FlexPay — with the repository chosen afterwards by the engineers, "и можно ли и возможно ли это изменять." See [[wiki/decisions/2026-09-10-per-product-components-and-mvp-fix-versions-on-the-capability-project.md]]. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

## Sept 11 2026 — he is the MVP-1 Flex-IQ developer, argues to keep the MudaGoose code, and takes the weekend

Rendered "Dzmitry Chudzinau" in the speaker labels of the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept-11 8:04 AM call]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

- **He is named as the Flex-IQ developer for MVP 1** — Pavel: "всё, что бы сейчас в первую очередь делать[,] дима[,] он будет делать [во] флекс айкью". [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He raised the structural objection to merged per-product capabilities** (reopen an old capability a year later, or create a new one?) — which Irina dissolved by pointing at the regulations, and he accepted at once: "а я не… знал о[б]… последних обновлениях, извините." See [[wiki/decisions/2026-09-11-acceptance-criteria-live-in-the-regulations-not-the-capabilities.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He argued against ripping the MudaGoose code out**, on time rather than difficulty — "я бы… предпочел сосредоточиться на более важном" — and had already prepared the switch-the-mode variant. He also refused the branch alternative on principle: "мы живём в мейне." Val moved the removal to MVP 3 rather than dropping it. See [[wiki/decisions/2026-09-11-mudagoose-never-in-mvp1-and-its-code-comes-out-at-mvp3.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He raised the lease-blocking gap that produced Val's ruling** — MudaGoose mode blocked only the terminal; do the Flex-Ports get blocked too? Val: yes, and players cannot play. See [[wiki/decisions/2026-09-11-lease-blocking-reaches-the-flex-ports-and-is-never-automatic.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He got the player PIN out of MVP 1** by pointing out that a cashier will not enter a PIN for a player, so Flex IQ has no player PIN screen at all. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He drew the line between remote update and remote config**, arguing there is nothing defined to configure yet — "[н]ечего закладывать" — which is why remote config went to MVP 2. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He is working the weekend**, paid as extra money rather than time off, on the services needed for Flex-Port / Flex-IQ communication and card activation on the e-wallet path. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Sept 11 2026 (10:33, in absentia) — named to the Passport/RIS regulations meeting

He was not on the [[wiki/meetings/2026-09-11-technician-complaints-and-new-capabilities-workshop.md|10:33 AM technician-complaints workshop]], but Val listed him as one of five people for the Monday Sept-14 9:30 working meeting that is to write the new Passport and RIS regulations — spoken as "Дима чудина" and rendered "Dima Chudzinau" in the derived notes, the same Belarusian form the speaker labels use for him elsewhere. He is the only back-end architect in the group, alongside Val, [[wiki/people/felipe-miranda.md|Felipe]], [[wiki/people/pavel.md|Pavel]] and [[wiki/people/irina-shishko.md|Irina]]. See [[wiki/decisions/2026-09-11-new-regulations-for-the-passport-and-ris-talked-out-monday-and-converted-from-the-transcript.md]]. [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]] [[raw/Meeting_Notes_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]

## Open commitments (Sept 11 2026)

- [ ] Dmitri Chudinov — attend the Monday working meeting on the new Passport/RIS regulations — due Sept 14 2026, 9:30; **assigned in his absence** — [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- [ ] Dmitri Chudinov — work the weekend on the services needed for Flex-Port / Flex-IQ communication and card activation on the e-wallet path — due Sept 12–13 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] Dmitri Chudinov — extend the existing firmware-dissemination mechanism to all FlexPay and Flex IQ devices (step one of the three-step staging) — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] Dmitri Chudinov — remove the code supporting MudaGoose, at MVP 3 — due MVP 3, undated — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Sept 14 2026 (8:01 AM) — the man who caught four things nobody had said out loud

At the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|8:01 AM use-case call]] he supplied most of the corrections, and did it by asking small practical questions rather than arguing scope.

- **The play-through rule.** "[К]ак[-]то не прозвучало ни разу, но вроде как подразумевается[:] у нас же остаётся режим[ —] деньги на [e-]волет положили, но их надо проиграть, прежде чем вывести." Klimovich's reply was "да, чёрт возьми, это важный момент", and he retracted a contrary comment he had made a minute before [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].
- **Requirement 1538 versus local MVP 1**, including the first recorded instance of the AI assistant mis-closing a capability because its requirement demands a cloud balance — "клод начинает с ума сходить… я начинаю создавать эти фичи." See [[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]].
- **What the TTL means for an already-printed ticket** when a location changes its setting — the question that produced the "printed tickets are not reprinted" rule ([[wiki/decisions/2026-09-14-ewallet-ttl-defaults-to-thirty-days-and-is-set-per-location.md]]).
- **The cashier needs a view of wallets created but never printed** — "кассиру нужен даш[б]орт, например, тикетов, которые были созданы, но не напечатаны" — which Klimovich answered by revealing he had added exactly that block the day before ([[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]]). He also supplied the alternative design that is now competing with Klimovich's reissue: create the wallet with a status, let the print action change the status, and keep the same number.

**On InComm errors he is the owner of record.** Everything InComm documents is handled and interpreted — "мы их все обрабатываем и как[-]то интерпретируем" — a bare "error" on screen means the response could not be recognised, he returns interpretations rather than codes while logging the codes, and the Spanish comes from a hard-coded collection: "[з]ашита[;] мы ещё не попали на следующий уровень" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]. He also stated the FlexPay precedent that framed the printer-failure debate: there, wallet creation sits inside the output transaction, so "если принтер не работает, мы и не создаём это [e-]волят."

**He ruled the e-wallet movement reporting out of MVP 1 himself** — a separate group of work, better done together with the move to cloud — and Klimovich accepted: "договорились, согласен" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

*(Irina addressed him about **capability 115**, which she said he is working on inside MVP 1; the exchange is too garbled to record a conclusion.)*

## Open commitments (Sept 14 2026)

- [ ] Dmitri Chudinov — send Klimovich the library of InComm errors with the interpretation texts currently in use, for a wording review — due "when he has time"; he agreed with "без проблем" — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## Sept 14 2026 (12:04 PM, in absentia) — given the Flex IQ ↔ Flex-Port protocol, and licence to improve it

He was not on the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|12:04 PM hardware call]], but [[wiki/people/pavel.md|Pavel Frolov]] put him first in the chain for remote firmware update: "**сначала её сейчас дима чудинов проработает со своей стороны. Может быть, как[-]нибудь там улучшить протокол? Общение между флекса IQ и портами**" — Chudinov works it from his side first, and may improve the Flex IQ ↔ Flex-Port communication protocol. [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] may be needed on the same task. See [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

*(The derived notes render his name in the Belarusian spelling "**Dzmitry Chudzinau**", already an alias on this page; the transcript says "**дима чудинов**".)* [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Open commitments (Sept 14 2026, 12:04 PM call)

- [ ] Dmitri Chudinov — work the Flex IQ ↔ Flex-Port firmware-distribution protocol from his side, and improve it if he can — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Sept 15 2026 (8:03 AM) — he wins two arguments on the audit trail, and is cut off for saying the requirements are not written

At the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept-15 8:03 AM call]] (Russian) he was again the one who asked what happens when something breaks [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**He kept the two internal balances.** Against a single displayed total, his case was recovery: "**с нашей стороны с инженерной всё равно остаются плейбл у редимого, потому что есть дилеммы[ —] откуда брать деньги и куда их возвращать?**" — if a transfer to the port is refused, the engine must know which side to return the money to, "иначе он попадёт в какойто абстрактный тотал… поэтому формально баланса 2". He also set the withdrawal priority: playable first, then redeemable, then refusal. Klimovich: "прекрасно. Я поддерживаю." See [[wiki/decisions/2026-09-15-balance-is-total-playable-only-and-redeemable-everywhere.md]].

**He closed reissue versus reprint.** Two carriers with identical barcodes protects against nothing a photograph can already defeat, and reissue's real cost is the investigation trail: "**потом усложняет [инвестигацию — ]что происходило в истории, что куда[-]то перевели на другой, с 2 на 3**". Klimovich had already switched the design to reprint. Out of the same scenario came the redemption freeze rule. See the Sept-15 update on [[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]].

**He pinned the MVP 1 cloud scope to two items** — "**не фантазируй[,] давай на MVP один**… девайсы оператора подключены[,] онлайн… и даш[б]орт по выпущенным карточкам. Все остальное… на MVP 2[ или ]3" — with billing continuing as it works today. See the Sept-15 update on [[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]].

**He was also the one who raised machine statistics as an operator product** — "у нас же теперь есть возможность собирать с машины… статистику[;] мы могли бы предоставлять какую то статистику оператору по машинам" — which Val called "наш гвоздь программы" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**And he was cut off.** Asked by Val how devices reconnect and how JVL learns they dropped, he answered with what exists: "**могу сказать, что требования не прописанные, но у нас реализована система графана, где в будущем возможны настройки на алерты**". Val: "я устал. Мне надоедает слушать, что мы знаем, но это не прописано… если это не написано, этого нету." He is first of the five named owners of the non-functional requirements. See [[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]].

**Two smaller contributions:** the countdown should appear only near the end rather than running throughout ("постоянный тайма[ут] сразу заставляешь немножко нервничать"), and the records list needs a direction filter for money moving to and from the machine, which the first FlexPay implementation had [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Open commitments (Sept 15 2026)

- [ ] Dmitri Chudinov — hand Klimovich the first version of Flex IQ in wallet mode so he can see which screens already exist — due the same day (Sept 15 2026) — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] Dmitri Chudinov (with [[wiki/people/andrey-bosik.md|Andrey Bosik]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] and [[wiki/people/pavel.md|Pavel Frolov]]) — write the non-functional requirements for FlexPay, Flex-Port and Flex IQ — due Monday Sept 21 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## Sept 16 2026 (8:01 AM) — he supplies the implemented truth four times, loses the offline argument, and settles a requirement by reading the API documentation live

The third MVP 1 morning call ([[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16 2026 8:01 AM call]], Russian). His role on this recording is consistent: he is the person who says what the code actually does, against what the requirement assumes.

- **The lease, device-side:** Flex IQ and FlexPay fetch a fresh lease date at start-up, then keep monitoring the last lease they hold and block on expiry "даже если был дисконнект", unblocking when a connection returns [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- **Storage:** contradicting Klimovich's assumption that locally-created wallets would later replicate to the cloud — "**не… в текущей реализации. Текущая реализация[ —] только локал стор[идж]. Конкретного мастера устройства**" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- **Cash:** "**нету никакого кэша на fl[e]xpay. Ни в каком виде**" — not by a recycler, not by a cashier, because the kiosk is purely for the player ([[wiki/decisions/2026-09-16-there-is-no-cash-on-flexpay-in-any-form.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- **Retention:** indefinite while the image stands, total erasure on a re-install — "при переустановке нового инсталлера будет полное затирание[,] с потерей всех данных" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- **Registration:** "[считай], что зарегистрировано, зарегистрировано навсегда… без практики[,] с методологи[ей] ничего не удаляется" ([[wiki/decisions/2026-09-16-a-kiosk-is-de-enrolled-from-a-location-never-from-the-cloud-database.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**He argued the offline case hardest and lost it.** His position — "на флекс[ ]айк[ью] было жесткое требование[:] если нет интернет и связи с нашими серверами[,] в принципе смысла ему работать нет" — rested on the control rule the team itself set: "**мы в любой момент должны уметь заблокировать терминал. Сами**". [[wiki/people/val-levitan.md|Val]] called the approach too categorical ("дима очень категорично к этому подходит") and Chudinov conceded the reading he was working from: "я слышу[:] в любой момент[;] для меня это сигнал[ —] в любой момент" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. See [[wiki/decisions/2026-09-16-a-location-keeps-working-without-internet-and-only-the-card-stops.md]].

**He closed one requirement by going and reading the documentation during the call.** Asked whether InComm returns an explicit daily-cap error, he checked and came back with "я посмотрел [доку]ментаци[ю]… [про] дейли кап нет. Соответственно и ошибок никаких не будет" — which deleted requirement 1533 and reshaped JVL's support path ([[wiki/decisions/2026-09-16-incomm-returns-no-daily-cap-error-so-the-call-comes-to-jvl-first.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**He named a failure he has never seen and would not dismiss:** InComm answering nothing at all, leaving JVL unable to tell whether a card activated — "такое… ни разу ещё не ловил" — and credited the AI assistant with raising it, "Клод подсказывает, что такое может быть". The ruling that followed parks such an operation as pending ([[wiki/decisions/2026-09-16-the-mvp1-timing-numbers-two-hundred-milliseconds-and-thirty-seconds.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. He also supplied the 200 ms screen-response standard: "200 миллисекунд[ —] это стандарт, ну мировой" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Open commitments (Sept 16 2026)

- [ ] Rework the acceptance criteria for capability 122 himself, off the back of the requirements work he is doing with Klimovich — due unspecified; he asked for it to be skipped on this call — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [ ] Find the FlexPay capability that requirement 1431 (ticket PIN) should hang off, now that he has unlinked it from Flex IQ capability 141 — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [ ] Review and update the status of every capability and requirement he authored, as Klimovich has done for his own — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

## Sept 17 2026 (8:02 AM) — he designs the multi-product answer on a shared screen, and twice refuses a framing rather than a request

The fourth MVP 1 morning call ([[wiki/meetings/2026-09-17-transactional-mvp1-skillpay-multi-product-and-device-network-security.md|Sept 17 2026 8:02 AM call]], Russian). [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**The design of the day is his.** Told that InComm now has two card products with independent settings, he asked for the screen and reshaped the location record live: today the location holds a single UPC field, but "**по факту [U]PC — это продукт**", so the field becomes a collection — add product, name it, enter the UPC InComm gives, set that product's own limits and fees. Two consequences he spelled out: the card's barcode already carries the UPC alongside the card number, so "**[при] скан[ировании] карты мы всегда знаем, какой UPC идёт**"; and the check is server-side, the **location manager** answering whether that location supports that UPC, otherwise "**отклоняем[:] вам продукт недоступен**". He put the build cost low. See [[wiki/decisions/2026-09-17-jvl-supports-multiple-incomm-products-not-a-fixed-pair.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**He lost the UI argument and kept arguing it anyway.** His position — amount and product on one screen, because the amount decides which products are possible, and "**иначе мы будем плясать от экрана к экрану вперёд и назад**" — was not adopted; [[wiki/people/andrei-klimovich.md|Klimovich]] parked the whole question overnight. [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**Two refusals, both of framing rather than of work.** He would not let signal telemetry be described as something a person can look at — "**это просто лог информации… показывать никому не сможем**" — and instead specified the mechanism (periodic metrics, automatic send, buffer to file offline, flush on reconnect, Grafana on top) and split it into two tasks, collect and then notify ([[wiki/decisions/2026-09-17-signal-quality-in-mvp1-means-remote-visibility-not-a-screen.md]]). And he would not let the gateway/master question be treated as one question: "**разделяй бизнес[-]логику — через кого создать [е]волет или там транзакции — или через кого слать графа[ну], логи, секреты, бандлы, обновления… Это очень большая разница**". [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**He stopped the meeting to correct a requirement nobody else had read properly.** Requirement 1431 is a PIN-entry timeout **on the Flex-Port**, "**чтобы подтвердить, что это твой [е]волет**"; Flex IQ has no PINs at all, FlexPay does — so it must come off capability 141 and attach to FlexPay. Klimovich took both points. [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**And he supplied the implemented truth twice**, as on the previous mornings: the Flex IQ setup screen in master mode already lists the Flex-Ports present on the network, and **Sergei** is finishing the function that re-attaches one; and Flex IQ will still update itself remotely in MVP 1 — "**IQ в [MVP] один будет обновляться**" — even after the Flex-Port half moved out. [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**Status he gave on his own requirements work:** all open questions on **capability 122** closed, some new requirements added, plus a couple of non-functional network requirements; the logging and Grafana requirements are "**запланировано, оно ещё не сделал**" — planned, not written. [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

## Open commitments (Sept 17 2026)

- [ ] Finish the logging work and write the Grafana / metrics requirements, including periodic signal metrics with offline buffering — due unspecified; nothing written yet — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [ ] Send the InComm error list and JVL's own on-screen messages ("no internet", "lease expired") into the meeting chat for Klimovich's Flex IQ text collection — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]


## Sept 18 2026 (8:03 AM) — he brings the contradiction that started the day, kills the rollback requirement, and becomes the plan's single dependency

The [[wiki/meetings/2026-09-18-transactional-mvp1-capability-cleanup-and-the-monday-deadline.md|fifth and final MVP 1 morning call]] before the Monday gate (Russian). Asked what was blocking the team, he answered with a live blocker: starting his next feature the day before, he found a capability whose requirements demanded a PIN for the wallet even though the team had dropped the PIN — "**есть требования, где нужен пин код[,] и требования, где пинкод не нужен. Возникло противоречие[,] конфликт[,] естественно, бло[к]ер**". [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**So he ran the whole release through Claude looking for conflicts** — "**я прогнал весь наш [MVP] один по теме флекса ай кю, флекс[]порт и работа с клаудом на поиск различных блокеров, противоречий и конфликтов**" — put the resulting document in the meeting chat, and handed it to [[wiki/people/andrei-klimovich.md|Klimovich]] as a working base. His recommendation for the future is a process one: write and link the requirements by hand, **then** run the set through the tool. What he actually wants next is a **specification document** for how MVP 1 works, readable end to end — and his reason for saying it cannot be produced today is the whole argument in a sentence: it would say both that a PIN must be entered and that it must not. See [[wiki/decisions/2026-09-18-nothing-is-closed-until-the-conflict-findings-are-worked-back-in.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**He then froze all closures**, and the mechanism is his: the sweep pushed new requirements onto capabilities whose existing features already closed the old ones, so "**надо будет открывать ещё одну фичу, поэтому… Пока ничего не закрывается**". It cost him capability 122, which he was ready to close after a weekend test run. [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**The technical ruling of the day is also his.** He named the rollback-to-a-previous-build requirement (requirement **1367** under capability **122**) as the one he could not deliver, and the reason is the database, not the firmware: the schema moves with the code, so the old build meets a structure that does not match — his example being a wallet table dropped for the cloud move, after which going back brings the system up empty. The proper answer is to re-cut the wanted version as a new one, raising the needed commits and dropping the rest. See [[wiki/decisions/2026-09-18-no-rollback-to-a-previous-build-and-the-team-rolls-forward-only.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**He ends the meeting as the bottleneck.** His capabilities — 148, 149, 150, 151, 163, 174, 175, 176, 152 and the location-block capability — carry no features, and [[wiki/people/irina-shishko.md|Irina]] closed the session on it: "**по [MVP] один мы… больше ничего не распланируем, пока Дима не сделает фичи**". He refused to invent dates in the meeting — "**я как сейчас с головы дату возьму?**" — and agreed to walk them with Irina afterwards. [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**His two named blockers, given when Klimovich asked him to prioritise:** the reworked window designs, and the requirements split across two products and two cards — "**они визуально… сильно меняют логику значительно**". Both are Klimovich's to clear, and neither is. [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## Open commitments (Sept 18 2026)

- [ ] Dmitri Chudinov — create features under all of his capabilities, which are currently bare, then tell the others so planning can continue; **the rest of the MVP 1 plan is blocked behind this** — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] Dmitri Chudinov — run the tests on capability 122 over the weekend and close it if they pass — due the weekend of **Sept 19–20 2026** — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] Dmitri Chudinov — finish reworking his own team's share of the conflict-sweep findings; only part was done — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] Dmitri Chudinov and [[wiki/people/irina-shishko.md|Irina Shishko]] — meet after the call and walk his capabilities and features to set real dates — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## Sept 21 2026 (8:02 AM) — he backs Irina on the printer, draws the payment-hub line, and takes the main IQ flow

On the [[wiki/meetings/2026-09-21-transactional-mvp1-flexport-and-iq-ux-design.md|Sept-21 8:02 AM call]] (Russian; speaker label "Dzmitry Chudzinau"):

- **Payment hub = card only.** "на терминале, наоборот, все балансы и создания по вольтам идут локально. Карточка это пхаб" — and he asked everyone to mark it so in future reviews [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]].
- **No printer, no wallet — at the counter.** "принтер бросил ошибку, всё значит не напечатано и воли инвалидный"; one transaction with confirmations. See [[wiki/decisions/2026-09-21-at-the-counter-no-printer-no-wallet-at-the-port-the-wallet-goes-to-unclaimed.md]].
- **Tilts:** he proposed the red exclamation mark that opens a list, which replaced Klimovich's banners [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]].
- **Barcode:** "на баркозе юпис плюс карткод"; he proposed the clickable card picture for the cashier [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]].
- **Work split:** he takes the main Flex IQ flow, because it ties to the business logic, and Vladimir the smaller pieces [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]].

## Open commitments (Sept 21 2026)

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — extend the Flex-Port ↔ machine protocol to pass the asset number as well as the serial number — due unspecified — [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]

## Sept 22 2026 (4:48 AM stand-up) — he argues the capability, not the feature, is what gets tested

At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 stand-up]] (Russian; label "Dzmitry Chudzinau") [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]:

- **Work status.** On updates: "Почти всё замерзло" (probably "merged" — unclear); the kernel is rebuilding from the SDK; he is deploying a new build to STG in parallel. He will merge one feature with main and then close the open features of capability 152 in order [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **Testing.** He does not close a capability until it is tested or test plans exist. He argued features cannot be tested alone — "Все эти фичи это какието промежуточные точки от а до б" — and that acceptance criteria hang on requirements. He named the case no one could answer: screens in one capability, balance and wallets in others. See [[wiki/topics/test-automation-strategy.md]] (Sept 22) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **Time.** "мы не успеем все до 1 числа", and he doubted the MVP 2 line would hold: "каждый день мы получаем новый список" [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

## Sept 22 2026 (8:01 AM) — MVP 1 is clear to him, 122 is closed, and the cloud is a different test problem

On the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 8:01 AM MVP 1 call]] (Russian) [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]:

- **MVP 1 is clear.** He reviewed it for Flex IQ and the Flex-Port: "критичных расхождений нету".
- **Capability 122 (Flex IQ remote updates) closed that day** — [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Sept-22 update).
- **The Jira pass.** He wanted capability 157 removed ("Я бы ее убирал"), named 148 as the wallet-issue capability, backed moving 115 to MVP 2, scheduled FIQ-34, and took the feature dates under 152 ([[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]], Sept-22 update).
- **How he builds features with Claude** — capability plus linked requirements, Claude picks the scope — and the payment-hub incident that made him insist on clean requirements: [[wiki/topics/ai-assisted-development.md]] (Sept 22).
- **On the date:** clarifying requirements still to meet, plus new functions "типа блокировки [Flex-Port]".
- **On tests:** the cloud platform "сильно отличается от машины" and cannot sit in one Docker container; he first preferred a separate capability for autotests. See [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]].
- **On dependency updates:** "Это не автоматический апдейт… Это должно быть контролируемо."

## Open commitments (Sept 22 2026, 8:01 AM)

- [ ] Dmitri Chudinov — set the feature dates under capability 152 — due Sept 22 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]


## Sept 23 2026 — "I told you not to mix products", and a certificate clash on STG

At the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]] (Russian; label "Dzmitry Chudzinau") [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]:

- **His earlier warning came true.** "я вам говорил не мешать в одной капубилике продукты". He told Sergey one shared repository for FlexPay and Flex IQ may work later, not now. See [[wiki/decisions/2026-09-23-capability-118-is-split-by-product-and-two-devices-keep-two-repositories.md]].
- **Capability 152 (card activation) on STG.** The DEV and STG cluster share one region and group, so a DEV-registered terminal clashes with STG and its certificate must be unbound. He dislikes both fixes and will take it to Andrei (Bosik, by inference). See [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]] (Sept-23 update).
- **Scope.** "на меня flexpay не вешайте." He will tidy and assign his own tasks.


## Sept 23 2026 (8:00 AM) — REQ-753 is "abstract", buffering already works, and he takes the Flex IQ capability

On the [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept-23 8:00 AM MVP 1 call]] (Russian; label "Dzmitry Chudzinau") [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]:

- **Requirements.** REQ-753 "Непродуктовый, он абстрактный" — deleted. Open questions are fine while work runs, "Главное не оставить их открытыми по завершении". Buffering when the link drops "уже работает"; no cloud view of Flex-Ports in MVP 1, only logs in Grafana. See [[wiki/decisions/2026-09-23-open-requirements-are-settled-on-the-call-and-only-slow-ones-are-parked.md]].
- **Flex-Port limits.** Georgia has 9 machines, so at most 9 Flex-Ports; the default is set to 20; the ceiling needs a stress test. See [[wiki/decisions/2026-09-16-fifteen-flex-ports-in-mvp1-and-the-system-designed-for-ninety-nine.md]] (Sept-23 update).
- **Capabilities.** The Flex IQ UI/UX capability goes to him; he had already created 231 for lost money. See [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]] (Sept-23 8:00 AM update).
- **Mock-ups.** He asked Klimovich to date the files so Claude can compare versions.

## Open commitments (Sept 23 2026, 8:00 AM)

- [ ] Dmitri Chudinov — create the features under capabilities 230, 231 and 234 — due Sept 24 2026 — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Notes_Legacy_CMS_Documentation_Progress_Check-April-15-2026.md]]
- [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]
- [[raw/Claude_Code-Dzmitry.md]]
- [[raw/Claude_Code-Dzmitry (1).md]]
- [[raw/Aaron_Briefing_FlexPay_FlexPort_WSS-February-5-2026.md]]
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
- [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Notes_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Notes_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Notes_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
