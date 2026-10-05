---
type: person
title: Anton Seregin
date: 2026-07-13
aliases: [Anton Seregin, Seregin, Anton Seryogin, Серёги, Серёгин]
disambiguation: "Minsk payroll / React-TS front-end dev, this page. One of THREE Antons (owner-ruled): Anton Leshkevich (Minsk engineer, Omni/RGS; transcript-garble alias "Dmishkevich" → wiki/people/anton-leshkevich.md), Anton Seregin (Minsk payroll / React-TS front-end → wiki/people/anton-seregin.md), Anton (SMM) (Meta-ads contractor, ECHO marketing → wiki/people/anton-smm.md). Resolve by context: Omni/RGS engineering → Leshkevich; front-end/setup UI → Seregin; ad campaigns/SMM → the contractor; queue anything fitting none."
source-count: 18
open-commitments: 2
---

# Anton Seregin

Anton Seregin is on the JVL **Minsk payroll** (per the salary roster). His first substantive transcript appearance (Mar 27 2025, below) places him on the **FlexPay kiosk front-end (GUI)**. [[raw/minsk_staff_roster_2025_names-only.md]]

**Owner ruling (2026-07-13):** Anton Seregin and [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] are **two different people** (shared given name only). Also distinct from the [[wiki/people/anton-smm.md|SMM/Meta-ads contractor "Anton"]]. Resolve future "Anton" mentions by context; if the context fits none of the three clearly, **queue it rather than guessing**.

## FlexPay frontend (stated Mar 27 2025)

- First substantive transcript appearance: on the FlexPay scope-gap meeting Pavel described the FlexPay kiosk software as "backend introduced by Dima, and **frontend implemented by Igor Hrybko and Anton Seregin** from Graphic User Interface. HTML5, HTML-based JavaScript." — establishing Seregin as a **GUI/front-end** contributor on FlexPay. See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]

## Apr 24 2025 — front-end developer on Omni LGS setup screens

On the Omni setup-screens review ([[wiki/meetings/2025-04-24-omni-setup-screens-june-scope.md]]) Anton Seregin is the **front-end developer** on the setup screens (transcript "Anton Seryogin" / "Антон Серёги"), owning the in-progress features **LGS 554 / 564 / 561** (targeting ~May 4–7) and later the multi-language feature; he is to move the LGS-UI screens repo from **Bitbucket to GitHub** with [[wiki/people/andrey-bosik.md|Andrei Bosik]]'s help. This extends his Mar-27 FlexPay-GUI role to a concrete **React/TypeScript front-end developer** on the Omni initial-setup screens. See [[wiki/decisions/2025-04-24-omni-first-release-legacy-plus-remote-setup-screens.md]]. [[raw/set_up_screen_omni-apr-24-2025.md]]

## Feb 4 2026 — design→React layout lead; moved off setup

On the [[wiki/meetings/2026-02-04-figma-react-export-workflow.md|Feb-4 figma→React session]] Pavel confirmed Seregin as the person who does the **Figma design → React layout** work ("умеет это делать… знает, как это делается") and has historically done most of it (with [[wiki/people/ihar-hrybko.md|Ihar Hrybko]] taking part of it recently). Two changes: (1) JVL **moved Seregin off the machine setup screens** — a new React developer, [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], now owns setup and Seregin acts as a **consultant over setup** rather than the main developer; (2) Val set the **first branch hand-off as Hrybko → Seregin**, wanting to watch Seregin accept the branch and "lay it onto React" (TypeScript committed to GitHub) and set up the preview tool. Reinforces Seregin as a **React/TypeScript front-end (layout) developer**. See [[wiki/topics/test-automation-strategy.md]] (Feb-4). [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]

## Feb 6 2026 — front-end setup-UI code owner (LGS repo)

On the [[wiki/meetings/2026-02-06-ui-claude-code-adaptation.md|Feb-6 UI/Claude-Code session]] Aaron's Claude analysis of the LGS repo placed "Anton" as the **front-end setup-UI** code owner ("Anton's the front end set up UI"), and Hrybko named the front-end owner as Anton — consistent with his React/TypeScript front-end setup-screen role. He attended and asked what a "sub-agent" is. See [[wiki/topics/ai-assisted-development.md]] (Feb 6). [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]

## Feb 11 2026 — front-end repos converted to the Waze system

On the [[wiki/meetings/2026-02-11-github-front-end-waze-setup.md|Feb-11 GitHub front-end Waze setup]] Seregin is the lead front-end developer being onboarded to [[wiki/people/aaron.md|Aaron]]'s Waze/"ways" system (substance on [[wiki/topics/ai-assisted-development.md]] Feb-11). He confirmed he works on **Flex POS** (most pages complete) and is about to start actively developing the **infrastructure-orchestration-core front end** — a **Webpack module-federation** app serving multiple micro front-ends by access control, Docker-deployable. Aaron cloned that repo live and had Claude + Waze scaffold an ADR system, an inaugural ADR, local build/front-end/micro-front-end ways, and a slimmed CLAUDE.md (the run then stalled on auth/network problems). His homework: accept and "play with" the converted repo, then open his own pull request in a branch and share it via chat for Aaron's review. He develops on **Windows + WSL/Ubuntu** running Claude Code. [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md]] [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md]] [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-4.md]]

## Aug 24 2026 (reported) — wrote prose and capabilities for RIS from the graphical-user-interface side

On the [[wiki/meetings/2026-08-24-nova-lgs-prose-standard-checkpoint.md|Aug-24 prose checkpoint]] (Russian; Seregin **not present**) [[wiki/people/pavel.md|Pavel Frolov]] cited him as having already done the work JVL now wants extended to the backend: "у нас Антон серёгин писал… Прозу и капбилити для… со стороны график юзер интерфейс" — prose and capabilities from the graphical-user-interface side. [[wiki/people/irina-shishko.md|Irina Shishko]] identified the subject as **RIS**: "так для риса писал, если уже это проза." (The middle of Pavel's sentence is garbled in the transcript; the GUI-side attribution and Irina's RIS identification are clear.) Pavel's proposal was to give [[wiki/people/sergey-tsymanov.md|Sergey Tsimanov]] the parallel backend/CMS prose. See [[wiki/topics/github-release-management-pipeline.md]] (Aug-24). [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]] [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]


## Sept 23 2026 — the kiosk emulator: bill-validator cases, and the new priority one

At the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]] (Russian), by speaker label [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]:

- **He extended the bill-validator emulation** on top of an existing validator daemon: currency and denomination changes, a bill-cheating error, a fail pause (events had fired instantly and broken the kiosk's logic), escrow, and the disconnect case where a bill is taken but the transaction does not go through.
- **The Flex-Port is not in his emulator** — "такого как бы устройства даже нет".
- **Next:** merge his branch into main, then clone the work for Flex IQ and build a terminal emulator that works with a real device — Pavel's priority one. See [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-23 update).
- **Very likely the "Антон" building a FlexPay emulator on Sept 22** (inference — same work, next day).


## Sept 23 2026 (8:00 AM, in absentia, by inference) — the FlexPay emulator, to be copied for Flex IQ

On the [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept-23 8:00 AM MVP 1 call]], Pavel said "он заканчивает флекс певский эмулятор" and that a task is needed for him to copy it for Flex IQ — "пару дней наверно". Only "Антон" is named; that it is Anton Seregin is an **inference** from his emulator report at the 4:48 stand-up the same day. See [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-23 8:00 AM update) [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

## Sept 24 2026 — validator and printer, the emulator moves to Flex IQ, and a firmware spike

At the [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|Sept-24 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]:

- **Validator done.** He closed the validator work and the processing of the "подготовительные" tape (garbled). He is updating the printer daemon to a new version and will review the printer again.
- **The emulator.** He will move the FlexPay emulator across to Flex IQ "За сегодня". He emulates device behaviour, not screens, so it may work with little change. It runs only on his machine so far. See [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-24 update).
- **A spike, proposed for him.** Pavel proposed he check how the current contract covers firmware delivery. See [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Sept-24 update).

## Sept 25 2026 — progressive 12-60, conflicts with main, and the prose rule

At the [[wiki/meetings/2026-09-25-daily-standup-engineering-menu-and-jira-discipline.md|Sept-25 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]:

- **Progressive work.** He is on "прогрессив 12, 60". His branch is old and conflicts with main ("редко уже далеко ушло"); he is sorting it out so it lands cleanly.
- **Next.** He will write instructions for "IQ" to move a project across — "перетащил вот этому натор проект". Read as the emulator project, moving to Flex IQ (**inference**, from the Sept-24 plan below); the words are garbled.
- **Prose.** Pavel asked that the prose lands with it. His branch predates the prose tooling, so he may need an extra branch from main to generate it. Pavel then stated the rule for every merge; see [[wiki/topics/github-release-management-pipeline.md]] (Sept 25).

## Open commitments (Sept 25 2026)

- [ ] Anton Seregin — resolve the conflicts with main, then write the instructions to move the project across, with its prose — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]

## Sept 28 2026 — a plan to move the emulator to Flex IQ, and quick endpoint tests

- **At the 4:56 AM stand-up** ([[wiki/meetings/2026-09-28-daily-standup-log-traffic-and-nova-rename.md|Sept-28 Minsk stand-up]], Russian; speaker label): he finished a move on Saturday, then made a plan to move "аккумулятора" to Flex IQ (read as the emulator — **inference**, as on Sept 23–24). The first task seems done and he is checking it. A bridge takes contracts from both Flex IQ and the emulator. His AI tool set its own dates; Irina: "Но не до 21 октября явно." The tool writes quick endpoint tests that run in the GitHub Actions build. See [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-28 update) [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]].
- **At the 8:02 AM call** ([[wiki/meetings/2026-09-28-transactional-mvp1-remote-updates-and-october-15-target.md|Sept-28 8:02 AM MVP 1 call]]; in absentia): Irina said "Антон" builds the emulators; Biratka: his emulator sits inside FlexPay; Pavel: he must move it to Flex IQ. That this "Антон" is Seregin is an **inference** from the work [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].

## Sept 29 2026 — re-checking Claude's stories, and the Flex-Port firmware update through Flex IQ becomes his task

At the [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|Sept-29 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]:

- **Status.** "Фейки 67 и к 243" (garbled; a feature and a task number, not interpreted); "по сичии, как бы вроде всё закрыл" (CI, by context); he is re-checking "[в]се эти истории, которые клод заводил по плану" — the stories his AI tool created from the plan — and "[р]абота на флекс… [т]о, что переносил аккумулятор" (the emulator move; "аккумулятор" read as before — **inference**), in parallel with a check of "ведущего счёта" (garbled).
- **Redirected.** He planned a Flex-Port feature "[ч]тобы поизучать… [к]ак он будет [э]мулировать". Pavel: first "флекс айкью, [э]мулятор и особенно обновление прошивки флекспорта через флекс айкю" — the file-transfer protocol and the commands that start the flashing; a Flex-Port emulation only if "совсем просто". "Ну вот буду этим заниматься сегодня, значит?" — "Заведу" the feature Pavel names. See [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Sept-29 update) and [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-29 update). His Sept-25 commitment above is not reported done.

## Open commitments (Sept 29 2026)

- [ ] Anton Seregin — work on the Flex-Port firmware update through Flex IQ (file-transfer protocol, start/allow commands) in the Flex IQ emulator, under the feature Pavel creates — due started Sept 29 2026 — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]] — *Sept 30 2026: in progress — he found nothing in Flex IQ for Flex-Port updates and untested FlexPay code; "не донимаю, что мне нужно будет сделать"* — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]

## Sept 30 2026 — printer and scanner emulation fit Flex IQ; the dispenser is out, the LTE modem is out, and the Flex-Port side is empty

At the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]:

- **Checked.** "Проверял ticket принтер эмулятор. Если баркот скайнер, как оно согласуется с флексом IQ? Там как бы она работает." The card dispenser: Chudinov and Pavel — not used. Something "ещё предлагает делать… подсветку… симулировать… на ивенты" (LED backlight on events; who proposes is unclear). The LTE modem: Pavel — "не трогать".
- **The Flex-Port.** "В этом флексе [IQ] как бы ничего нет эти обновления"; FlexPay code is written but "Дима говорил, что он еще не тестировал его никак"; "Мне не донимаю, что мне нужно будет сделать". See [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Sept-30 update) and [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-30 update).
- **An instruction.** "скинул в чат этот [эмулятор]. Большую инструкцию, если интересно" ("аккумулятор" read as emulator — **inference**). He had to leave for about an hour (logistics, not recorded further). Pavel noted he kept dropping off the call.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

- [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]
- [[raw/minsk_staff_roster_2025_names-only.md]]
- [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- [[raw/set_up_screen_omni-apr-24-2025.md]]
- [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-4.md]]
- [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
