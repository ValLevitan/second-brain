---
type: person
title: Anton Seregin
date: 2026-07-13
aliases: [Anton Seregin, Seregin, Anton Seryogin, Серёги, Серёгин]
disambiguation: "Minsk payroll / React-TS front-end dev, this page. One of THREE Antons (owner-ruled): Anton Leshkevich (Minsk engineer, Omni/RGS; transcript-garble alias "Dmishkevich" → wiki/people/anton-leshkevich.md), Anton Seregin (Minsk payroll / React-TS front-end → wiki/people/anton-seregin.md), Anton (SMM) (Meta-ads contractor, ECHO marketing → wiki/people/anton-smm.md). Resolve by context: Omni/RGS engineering → Leshkevich; front-end/setup UI → Seregin; ad campaigns/SMM → the contractor; queue anything fitting none."
source-count: 41
open-commitments: 9
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

- [ ] Anton Seregin — work on the Flex-Port firmware update through Flex IQ (file-transfer protocol, start/allow commands) in the Flex IQ emulator, under the feature Pavel creates — due started Sept 29 2026 — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]] — *Sept 30 2026: in progress — he found nothing in Flex IQ for Flex-Port updates and untested FlexPay code; "не донимаю, что мне нужно будет сделать"* — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]] — *Oct 1 2026: not mentioned; his report was the emulator verification* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]

## Sept 30 2026 — printer and scanner emulation fit Flex IQ; the dispenser is out, the LTE modem is out, and the Flex-Port side is empty

At the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]:

- **Checked.** "Проверял ticket принтер эмулятор. Если баркот скайнер, как оно согласуется с флексом IQ? Там как бы она работает." The card dispenser: Chudinov and Pavel — not used. Something "ещё предлагает делать… подсветку… симулировать… на ивенты" (LED backlight on events; who proposes is unclear). The LTE modem: Pavel — "не трогать".
- **The Flex-Port.** "В этом флексе [IQ] как бы ничего нет эти обновления"; FlexPay code is written but "Дима говорил, что он еще не тестировал его никак"; "Мне не донимаю, что мне нужно будет сделать". See [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Sept-30 update) and [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-30 update).
- **An instruction.** "скинул в чат этот [эмулятор]. Большую инструкцию, если интересно" ("аккумулятор" read as emulator — **inference**). He had to leave for about an hour (logistics, not recorded further). Pavel noted he kept dropping off the call.

## Oct 1 2026 — FP-60 closed, three kiosk bugs to capability 140, and verifying the Flex IQ emulator against the device

At the [[wiki/meetings/2026-10-01-daily-standup-sas-mode-flag-and-feature-status-rules.md|Oct-1 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]:

- **Closed.** "Я закрыл FP 60… там было 3 бага. Продукте самого киоска… я их перетащил. [В capability] 140. На будущее".
- **The emulator.** On Flex IQ he is at the verification stage: compare a scenario ("положить деньги, распечатать тикет… клиента забрал") on the emulator and the device and check the logs for extra or missing events; a register of which device model and firmware each emulator version was verified against — "[Клод]… предлагает… Вести такой типа регистр. Он как бы уже сделал, просто он не заполнял"; the printer daemon "ноль ноль 8 версия… И ноль ноль 6. Fix pay… не поднимали версию. Вот но есть какието отличия". Pavel: no full match needed; one instance per device — "Оно единственный экземпляре одна"; "попробуй за за сегодня это всё. Закрыть"; next, someone else (Khamin, Vladimir or Irina) brings his environment up elsewhere — "Угу". See [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Oct-1 update) and [[wiki/topics/test-automation-strategy.md]] (Oct 1, 4:48 AM). ("акмулятор" / "мегатора" read as emulator — inference, as throughout.)

## Open commitments (Oct 1 2026)

- [ ] Anton Seregin — finish the Flex IQ emulator verification (the scenario comparison and the register of verified device models and firmware) and look for further cases — due Oct 1 2026 — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]] — *Oct 2 2026: in progress — scenarios "102 103" build the diffs, then the real device; "мне устройство бы еще проверить на устройстве"* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]] — *Oct 5 2026: the emulator side closed (FAQ-105–108); the device side — printer scenarios, barcode scanner — remains (see the Oct-5 commitments)* — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [ ] Anton Seregin — next, have his emulator environment brought up by Khamin, Vladimir or Irina in a different set-up, for example against a real Flex IQ — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]] — *Oct 2 2026: in motion — Khamin: "Антон попросил ещё этот [эмулятор] попробовать… Можно наверно сегодня"* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]

## Oct 2 2026 — scenarios 102 / 103 and the diffs, then the real device; "if the tests pass, you are done"

At the [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 Minsk stand-up]] (Russian; called on as "кантон") [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]: "Над 102 103. Я поставил и не загружается контент остановиться" (garbled); "такие типа сценарии, которые. Строять дифы… а потом, ну после этого надо будет с реальным устройством. Прогнать на нём сценарий? И вот он сравнит как бы. То, что [на эмуляторе] и то что [на устройстве]. Их логически это тот же самый процесс." Irina, in the weekend round: "Антон, у нас один с симулятором. В принципе, если тесты пройдут нормально, то ты закончил." Seregin: "Но мне устройство бы еще проверить на устройстве… пробовать можно уже по крайней мере." Khamin said Anton had asked him to try the emulator. Ivan's "это Антона зарелизить свою часть" on the South Dakota release is **not resolved** between the Antons. See [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Oct-2 update) and [[wiki/topics/test-automation-strategy.md]] (Oct 2).

## Oct 5 2026 — FAQ-105 to 108 closed, the printer scenarios still to run on a real device, a FlexPay-derived task "вообще блок надо", how the emulator is built, and "kiosk" → "terminal"

At the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]: "позакрывал стори. Для. Верификация… fa q 105 106 107 108 закрывал"; what is left — "для принтера осталось это свериться с реальным устройством… бумага замялась фейл самого принтера. Типа дисконнект принтера… Вот тогда можно их пометить, что [верифицированы]. И для [баркод-сканера]… попроще"; "Пришлось еще вот это эмулировать [привязку к локейшн]"; "осталось как бы физическое сравнение вот этих 2 разных путей." On a task hanging since Oct 2: "это, скорее всего, вообще блок надо, потому что это с флекс [пэем] мы так ничего не поняли… На этом невозможно ничего [инаследовать]." To Khamin on the emulator: "собираешь там есть скрипты внутри [репозитория]? По дефолту там берётся из мейна… можно уже готовый образ… Они на основе готовых уже собранных докера имиджа"; "Там долго эта сборка… образ это как бы и деньги компании"; "если ты меняешь код самого терминала, это одно, если ты меняешь код эмулятора это 2 вариант"; on the kiosk name: "Транслировалось этого с флекспэя мы сюда перенеслась ну поправимся." See [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Oct-5 update) and [[wiki/decisions/2026-09-30-an-autotest-task-that-cannot-finish-goes-to-blocked-not-closed.md]] (Oct-5 annotation). ("акмулятор" / "аккумулятор" read as emulator — inference, as throughout.)

### Open commitments (Oct 5 2026)

- [ ] Anton Seregin — run the printer scenarios (success, paper jam, printer failure, disconnect) and the barcode-scanner ones on a real device, compare the two paths, then mark them verified — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [ ] Anton Seregin ("ну поправимся"; not assigned by name) — change "kiosk" to "terminal" in the Jira feature names and descriptions, not in commits — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Oct 6 2026 — FQ-67 done, prose for the SDK UI kit, and the front-end contract question

At the [[wiki/meetings/2026-10-06-daily-standup-ris-georgia-branch-and-critical-error-text.md|Oct-6 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]:

- FQ-67 accuracy work is done; he needs a terminal for a few hours to check it.
- He added prose and ADRs to the SDK UI kit (it was at zero) and to the Flex IQ Pay dispensers repository.
- He asked what a contract means for a front-end app; Pavel's answer is on [[wiki/decisions/2026-09-04-data-contracts-closed-every-repository-by-september-11.md]].
- Vladimir asked him to look at FQ-112 (bringing Anton Leshkevich's daemon change into the emulator). He will tidy his Jira.

### Open commitments (Oct 6 2026)

- [ ] Anton Seregin — look at FQ-112 (Anton Leshkevich's daemon change into the emulator) — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]

## Oct 7 2026 — Jira cleaned, three repositories for prose and contracts, emulator fixes in parallel

At the [[wiki/meetings/2026-10-07-daily-standup-test-coverage-first-and-ai-task-numbers.md|Oct-7 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]: he cleaned his Jira and closed one item and its story (the number is garbled); took three repositories for prose and contracts, most of it done; works on emulator fixes in parallel ("я и так это делаю параллельно"); a story from Khamin, and maybe one from Vladimir, is still to do. See [[wiki/topics/test-automation-strategy.md]] (Oct 7).

## Oct 8 2026 — feature 67 nearly closed; three stories need a real terminal; prose and contracts in review

At the [[wiki/meetings/2026-10-08-daily-standup-lease-expiry-scenarios-and-flex-signal-quality.md|Oct-8 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]: he closed the rest of feature "67"; three stories remain that need a real terminal, done today if he can get one. Prose and contracts are generated and in pull-request review; the same for Flex Pay; Flex IQ prose and contracts finished yesterday. He set dates on closed items so the report matches. Chudinov asked him for a couple of edits on screen task F-52 — [[wiki/topics/test-automation-strategy.md]] (Oct 8), [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 8).

### Open commitments (Oct 8 2026)

- [ ] Anton Seregin — run the three remaining stories on a real terminal — due Oct 8 2026, if a terminal is free — [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [ ] Anton Seregin — make a couple of edits for Chudinov's screen task F-52 — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]

## Oct 9 2026 — emulator task 146 done, 147 today

At the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 stand-up]]: emulator task 146 (PIN codes and serials for technicians) done; on 147, so the terminal runs in emulator mode against real services; Vladimir may send him a version stub for review — [[wiki/topics/test-automation-strategy.md]] (Oct 9) [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].

## Oct 12 2026 — 147 closed; 150 and 151 to re-check; one more terminal for him

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 stand-up]]: closed 147 (the STG cloud profile, so it registers as a normal terminal), closed 150 and 151 (Vladimir's) and will re-check them; Pavel will build one more terminal so he can run a scenario — [[wiki/topics/test-automation-strategy.md]] (Oct 12) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].

## Oct 13 2026 — 150 and 151 closed; card creation failed on firmware; the flash-drive boot order resets

At the [[wiki/meetings/2026-10-13-daily-standup-video-decode-memory-and-release-task-type.md|Oct-13 stand-up]]: he closed 150 and 151 (the Oct-12 re-check is done); a firmware try could not create cards; the boot order from a flash drive seems to reset on reboot; a story for Pavel (number garbled) — [[wiki/topics/test-automation-strategy.md]] (Oct 13) [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]].

## Oct 14 2026 — Flex IQ tasks wait on the terminal; a changed installer

At the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 stand-up]] his Flex IQ tasks ("67… все 3 задачи") all wait on the terminal; he now has access rights, changed the installer and will build an image and try to install it — [[wiki/topics/test-automation-strategy.md]] (Oct 14) [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

## Oct 15 2026 — USB-stick loading task closed; printer scenarios and a "10-minute" rule

At the [[wiki/meetings/2026-10-15-daily-standup-offline-ris-fallback-and-nova-game-conversion.md|Oct-15 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]: he closed the USB-stick loading task and split out the installer; a boot-order change waits in a pull request, because his board's SD card does not work and Claude warned it might not boot. Scanner scenarios passed; printer scenarios are in progress. Claude wrote a scenario where a ticket not taken within about 10 minutes becomes invalid, a rule nobody knows; he is to find its source — [[wiki/topics/test-automation-strategy.md]] (Oct 15).

## Oct 16 2026 — 102, 103, 129 today; scanner and printer together; a paper jam seen only at the next print

At the [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct-16 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] he will close 102, 103 and 129; he moved to a terminal where the scanner and the printer work together and found a paper jam is known only at the next print, while the screen looks normal — Tsymanov: alerts show only on certain screens. He finishes the printer scenarios today — [[wiki/topics/test-automation-strategy.md]] (Oct 16).

## Oct 19 2026 — printer scenarios done; a plain Wi-Fi QR does nothing; the encrypted settings QR task comes to him

At the [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct-19 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] he finished the printer scenarios and closed a task from Vladimir; other device emulations (LTE modem, LED strip lights, Wi-Fi QR and one more) sit in the backlog. A Wi-Fi QR on a bank scanner beeps but is not processed — [[wiki/topics/test-automation-strategy.md]] (Oct 19). Pavel will create the server-side task for the encrypted settings QR for him — [[wiki/decisions/2026-09-07-wi-fi-provisioning-by-encrypted-qr.md]] (Oct-19 update).

At the [[wiki/meetings/2026-10-20-daily-standup-io-board-firmware-via-github-and-vp9-video-decode.md|Oct-20 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]] he reported the encrypted-settings-QR spike he made from the Oct-19 meeting (FP-1364 as heard), with branch, commits and documentation; the AI PM's duplicate was kept and he links his task to it — [[wiki/decisions/2026-09-07-wi-fi-provisioning-by-encrypted-qr.md]] (Oct-20 update); [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-20 update). His capability 243 has mixed statuses and is being split — [[wiki/topics/test-automation-strategy.md]] (Oct 20).

## Oct 21 2026 — the settings spike: one design across all devices

At the [[wiki/meetings/2026-10-21-daily-standup-flex-port-mode-switch-and-sas-crc-fix.md|Oct-21 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]] he reported on the FP-1364 spike (as heard): terminal registration covered, questions to agree on, and a proposal to reuse the Flex Pay Wi-Fi QR in a common part. Pavel said that QR is temporary and asked him for a careful user flow and one registration-and-settings architecture across Flex-Port, Flex Pay and Flex IQ, then a joint review with Pavel, Biratka and Irina — [[wiki/decisions/2026-09-07-wi-fi-provisioning-by-encrypted-qr.md]] (Oct-21 update).

## Oct 22 2026 — four registration scenarios

At the [[wiki/meetings/2026-10-22-daily-standup-flex-port-cashout-screens-and-native-engine.md|Oct-22 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] he reported about four scenarios written in the documentation (registration without internet, a mini router, a change of location) and asked for a review with everyone involved to split MVP 2 from MVP 3; Pavel asked for an architecture first, then the capabilities — [[wiki/decisions/2026-09-07-wi-fi-provisioning-by-encrypted-qr.md]] (Oct-22 update).

## Oct 23 2026 — scenarios redrawn; "kiosk" becomes "terminal" in the emulator

At the [[wiki/meetings/2026-10-23-daily-standup-bill-validator-lockout-and-atlanta-port-test.md|Oct-23 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]] he said he fed the earlier meeting in ("Скормил наш митинг" — to the AI, **inference**), redrew the registration scenarios and sent the documents. Andrei (Klimovich, by context — **inference**) asked him to rename things in the images the emulator builds so that "kiosk" appears nowhere and "terminal" is used everywhere. He is moving Jira items so the Flex-Port firmware capabilities can close; emulation will be a separate task, after it is built in the real product.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
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
- [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]
