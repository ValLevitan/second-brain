---
type: person
title: Alexei Khamin
date: 2025-04-22
aliases: [Alexei Khamin, Aliaksey Khamin, Alexey Khamin, Khamin, Хамин, Khanin, Ханин, Kamin, Alexey Kamin, Lyosha, Лёша]
source-count: 31
open-commitments: 17
---

# Alexei Khamin

Alexei Khamin is a JVL **Minsk engineer** who helps bring machines up in the shop / walks colleagues through machine-setup procedures. He reconciles to the Minsk-payroll name **"Khamin Aliaksey"** (see [[wiki/topics/minsk-staff-roster.md]]), gaining a page here on appearing in transcripts.

## Role

- **Apr 22 2025:** on the FlexPort TITO-mode debug standup, Khamin (with "Vlad") was to walk [[wiki/people/eugine-yavorski.md|Yavorski]] through the Factory-Reset → passport-scan → RIS → Enable-SAS procedure to enable the printer/TITO on his red countertop rig. See [[wiki/meetings/2025-04-22-flexport-tito-machine-setup-debug.md]]. [[raw/flex_port_update-apr-22-2025.md]]
- **May 1 2025:** on the dispensing-tower design call [[wiki/people/val-levitan.md|Val]] characterised him as "**хороший … выполнительный**" (good, executive/compliant) but "**очень пассивный**" (very passive) — he "won't push work through," so for organising the shop-floor resourcing Val preferred [[wiki/people/irina-shishko.md|Irina Shishko]]. [[raw/flex_tower_spacial_design_review-may-1-2025.md]]
- **QA engineer (Nov 2025).** On the payment-hub ACH spec-review sessions Val identifies Khamin explicitly as "our QA engineer" / "in the QA department" — working QA on the ACH module alongside [[wiki/people/irina-shishko.md|Irina Shishko]] (Director of QA). This refines the earlier shop/machine-setup framing: by late 2025 his named role is QA engineering (consistent with sitting under Shishko's QA org). [[raw/Payment HUB_ACH module specification_06.11.25.md]] [[raw/Payment HUB_ACH module specification_10.11.25.md]]

## Nov 5–10 2025 — QA on the payment-hub ACH module

Across the three ACH-module spec-review sessions Khamin raised the QA questions: how to generate test bank accounts/locations (Dwolla sandbox accounts, reused per test), how to force/emulate invoice states for testing (needs a state-machine diagram), how to test large transaction volume without physical cards (simulated), and duplicate-invoice / negative-case testing. On Nov-5 he and Irina were asked to specify the **testing-hook requirements** for verifying invoice state changes. Substance on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Nov 5–10 ACH-spec arc). [[raw/Payment HUB_ACH module specification_05.11.25 .md]] [[raw/Payment HUB_ACH module specification_10.11.25.md]]

## May 12 2026 — Anton's downstream "customer" in the NOVA governance model (spelling flagged)

On the founding NOVA platform architecture session ([[wiki/meetings/2026-05-12-nova-platform-architecture-overview.md]]) the notes name **"Kamin (Alexey Kamin)"** as [[wiki/people/anton-leshkevich.md|Anton]]'s downstream user — the customer Anton's test framework delivers for. Resolved to Khamin **by QA context** (Anton builds the test framework; Khamin is the JVL QA engineer under [[wiki/people/irina-shishko.md|Shishko]]), consistent with his existing garble aliases (Khanin/Ханин); the "Kamin" spelling is a transcription variant, **flagged for owner confirmation, not force-matched**. Substance on [[wiki/topics/nova-platform-architecture.md]]. §15.8 clear. [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_2-May-12-2026.md]]

## Sept 3 2026 — given sole ownership of attaching requirements to capabilities and auditing the acceptance criteria

At the [[wiki/meetings/2026-09-03-nova-prose-standard-skills-and-module-contracts.md|Sept-3 prose/contracts follow-up]] (Russian; Khamin **not present**) [[wiki/people/pavel.md|Pavel]] proposed him for the work Val had just specified — build and test the skills that attach every existing requirement to the capabilities, propose the missing ones, and audit the acceptance criteria against the code. Pavel: "я вижу 1 человека которому можно дать это задание[:] это Алексей хамин," adding [[wiki/people/ivan.md|Ivan]] as capacity allowed once South Dakota and V3 Georgia ship. **Val cut it to one owner:** "Давайте одного[,] давайте не 2[,] давайте хами[на] над этим." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

Irina and Pavel then disagreed about what he inherits: Irina wanted the capabilities finished and the requirements attached before he starts ("чтобы… для лёши готова" — Lyosha being the short form of Alexey), while Pavel argued that determining how far the requirements diverge from what was intended is precisely his job. Not settled on the call. Full decision on [[wiki/decisions/2026-09-03-acceptance-criteria-settled-by-experiment.md]]. §15.8 clear — assignment only, no compensation. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Open commitments (Sept 3 2026)

- [ ] Build and test the skills that attach requirements to capabilities, propose the missing requirements, and audit the acceptance criteria against the code — due unspecified — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]] [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Sept 4 2026 — handed Pavel's debug environment for his own testing

On the [[wiki/meetings/2026-09-04-flex-slim-first-ten-and-flex-port-sas.md|Sept-4 midday call]] [[wiki/people/pavel.md|Pavel Frolov]] described the debug environment he has built for the Flex-Port work — a gaming-machine emulator, a full debug console with commands and logs on an STM32 743, and a described physical rig — and said he had **shown it to Khamin that same day**: "Большую часть я уже сделал… И показал это [Хамину] сегодня. Он может это взять, по крайней мере для своего тестирования. То, что там не работает, он может легко сказать [Клоду] и Клод ему поправит это… уже на реальной машине." Consistent with his QA role and with the Sept-3 ownership Val gave him. Detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 4) [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

## Sept 9 2026 — given the requirements audit and the negative cases, once GCOAM V3 testing clears

At the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept-9 7:02 AM call]] [[wiki/people/pavel.md|Pavel]] made him and [[wiki/people/irina-shishko.md|Irina Shishko]] the gate in front of the new planning arrangement: "пусть Ира с Лёшей посмотрит те реклам[енты], которые получились у [Б]осика[,] и хотя бы грубо оценить, насколько они покрывают весь [скоуп]" — Pavel's own expectation being 5% coverage of kiosk behaviour at best. [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

He is also half of the parallelisation Pavel proposed — Irina and "Алексею" writing the negative cases up as acceptance criteria while the positive cases are worked, so Claude can then write its own tests. See [[wiki/topics/test-automation-strategy.md]] (Sept 9). [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

**Capacity:** Val asked whether he could be pushed harder — "может быть, его тоже можно поднапрячь[,] или он не потянет эти вещи?" — and both answered that he can ("[п]отянет, потянет"; Irina: "[в]сё потянет"); the constraint is the unfinished **GCOAM V3** testing, "есть незавершённые работы по тестированию там [ГК]ам в 3." Pavel also counts him as one of the resources that makes taking the SAS work himself faster: "у меня есть там Лёша под боком." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

**Open commitments (Sept 9 2026)**

- [ ] With Irina Shishko — grade how much of the scope Bosik's generated requirements cover — due before the Bosik/Kovalchuk session — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] With Irina Shishko — write the negative cases up as acceptance criteria in parallel with the positive-case work — due unspecified — [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

## Sept 11 2026 — named owner of the e-wallet autotests, and added to the capability project

At the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept-11 8:04 AM call]] Val agreed to write automated tests for the e-wallet use cases, and [[wiki/people/pavel.md|Pavel Frolov]] proposed assigning the resulting features to Khamin — "[т]ам на Алексея например". [[wiki/people/irina-shishko.md|Irina Shishko]] made it unconditional — "можно сразу его[,] в любом случае[,] это на лёшу, а если что[-]то нужно, [пусть] дима просто предоставит" — and Pavel did it on the call: "[в]от я перевел на Алексея." Pavel then asked [[wiki/people/andrey-bosik.md|Bosik]] to have [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] add "Алексея хамина" to the capability project, which was done during the meeting [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

Coverage is honestly scoped: Pavel said automated testing will cover "только… какая[-]то маленькая часть, связанная с флекс IQ" for now. See [[wiki/topics/test-automation-strategy.md]] (Sept 11) [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

*(A separate "лёша" is named in the same call as the person checking and fixing the firmware-dissemination mechanism. The source does not say which Alexey that is, and it is **not** attributed to Khamin here.)* [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Open commitments (Sept 11 2026)

- [ ] Alexei Khamin — write the automated tests for the e-wallet use cases on Flex IQ — due unspecified, ahead of Oct 1 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Sept 14 2026 — he is the named test of whether main is healthy, and he corrects the branch premise

At the [[wiki/meetings/2026-09-14-code-standards-main-branch-rule-and-alekseev-coaching.md|Sept-14 7:37 AM code-standards call]] (Russian) Khamin is used twice as the concrete person the main-branch rule exists for.

- **Val states the failure test in his name.** "**если Алексей берет этот код и не может установить его, просто взять и установить на машину. Это значит, что код не работает или релиз ноут неправильный. Или проза неправильная… приоритет должен быть на то, чтобы это работало**" — if Khamin takes the code from main and simply cannot install it on a machine, then either the code, the release note or the prose is wrong, and fixing it takes priority. See [[wiki/decisions/2026-09-14-main-branch-must-always-build-and-the-code-belongs-to-the-project.md]] [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- **He corrected Val's premise about branches.** Val argued that QA only ever checks main — "**Он же не ваш бранч проверяет**" — and Khamin's one technical contribution to the call was the opposite: "**Да, есть возможность собрать из ветки и проверить**" — yes, it is possible to build from a branch and check it. See [[wiki/decisions/2026-09-14-flex-port-sas-mode-is-a-selection-capability-not-a-long-lived-branch.md]] [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]

*(He confirmed at the start of the call that he had received Val's code-standards email — "**Да это есть**" — unlike [[wiki/people/irina-shishko.md|Irina Shishko]].)* [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]

## Sept 22 2026 — moving pull requests to test, and the "stabilisation" stage

At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 stand-up]] (Russian; label "Alexey Khamin"), he said he would look at pull requests "от вёрского" (name garbled) and move them into a branch to test. In the status debate he named the missing stage after In Progress: "это стабилизация больше идёт… Чтобы было понятно, что разработка… закончилась"; Kovalchuk: "Клеша правильно говорит". See [[wiki/topics/test-automation-strategy.md]] (Sept 22) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

## Sept 22 2026 (8:01 AM, in absentia) — he gets the first end-to-end test

Not on the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 8:01 AM MVP 1 call]], but named there. Pavel: "лёша, я думаю напишет это за час… или за 2" — the Flex-Port connection test (cable in reports connected, cable out not connected, read through the telnet hook), filed under capability 173. Val asked that he and Ivan be put on the test work in the schedule, naming "Алексея Хамина" in full. See [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

## Open commitments (Sept 22 2026)

- [ ] Alexei Khamin — write and run the first E2E test (Flex-Port connection state, telnet hook, capability 173) — due Sept 23 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]] **Update (Sept 23 2026):** he is dropping other work to write it; not yet reported done — [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]] — **8:00 AM the same day:** not finished; the connection tests came from Ivan — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]

## Sept 23 2026 — he drops the pull-request cleanup for the autotest

At the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]] (Russian; label "Alexey Khamin"), he said he moved the pull requests into branch 9 and deleted dead branches, and is now dropping the rest to write the autotest. He raised that how the transactional tests are organised needs thinking through, "а не ляпать просто лепёшкой непонятно куда". See [[wiki/topics/test-automation-strategy.md]] (Sept 23). The Sept-22 test commitment above stays open. [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]

## Sept 23 2026 (8:00 AM) — his money-crediting test is not finished, and five lost-money bugs go to 231

On the [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept-23 8:00 AM MVP 1 call]] (Russian; label "Alexey Khamin") [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]:

- **The test.** It credits money to the machine through terminal, Flex-Port and EGM. Claude offered only manual options, which he refused; he found no open API. On Chudinov's advice he is building a tool or instruction set so Claude can generate the test and check the balance. See [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]] (Sept-23 update).
- **Lost-money bugs.** He raised five open Flex-Port bugs where money disappears; Klimovich ruled a "forfeit" wallet, and the bugs go to capability 231. See [[wiki/decisions/2026-09-23-open-requirements-are-settled-on-the-call-and-only-slow-ones-are-parked.md]].
- **Capability status.** A capability cannot be in review while its requirements are open; the developer moves it to Review when all features are done.

## Open commitments (Sept 23 2026, 8:00 AM)

- [x] Alexei Khamin — attach his five lost-money Flex-Port bugs to capability 231, "первым делом" — due Sept 23 2026 — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]] — **discharged Sept 24 2026:** linked under 231 — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [x] Alexei Khamin — build the tool or instruction set so Claude can generate the money-crediting test and check balances — due unspecified — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]] — **Sept 24 2026:** he expects the tooling ready that day, depending on the terminal test API — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]] — **discharged Sept 25 2026:** on the new test API his test "Заработал почти сразу"; Claude created a wallet, scanned it on the Flex-Port, chose an amount and checked the machine balance — [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]

## Sept 24 2026 — the lost-money bugs are linked, and stale docs confuse Claude

At the [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|Sept-24 Minsk stand-up]] (Russian; label "Alexey Khamin") [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]:

- **Bugs linked.** "я слинковал всё под кап 231" — this discharges his Sept-23 commitment below. Klimovich checked them. The team fixes them, not an outside developer. See [[wiki/decisions/2026-09-23-open-requirements-are-settled-on-the-call-and-only-slow-ones-are-parked.md]] (Sept-24 update).
- **Autotests.** Mostly autotests; he waits for an API. The screens changed but the prose docs did not, so Claude could not follow. See [[wiki/topics/test-automation-strategy.md]] (Sept 24).

## Sept 24 2026 (8:01 AM) — tests that run with no person, written with Claude

On the [[wiki/meetings/2026-09-24-transactional-mvp1-flexport-money-loss-bugs-and-release-date.md|Sept-24 8:01 AM MVP 1 call]] (Russian; label "Alexey Khamin") [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]:

- **Unattended tests.** He found a way for autotests to run with no person; it needs a test API on the terminal (Chudinov's task). The rest of the test already exists. Tooling that day, tests from the next. "[П]ишу [с] клодом, но… с тем условием, чтобы тесты проходили без его [участия]." See [[wiki/topics/test-automation-strategy.md]] (Sept 24, 8:01 AM).
- **Repository.** Val told him to point his Claude at the repository standard and consult Bosik. See [[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]] (Sept-24 update).
- **Unclaimed.** He suggested the cashier could replay the withdrawal to the port; deferred with the rest to MVP 2. See [[wiki/decisions/2026-09-24-a-flex-port-that-dies-holding-money-sends-it-to-unclaimed-and-one-without-a-gateway-goes-out-of-service.md]].

## Open commitments (Sept 24 2026, 8:01 AM)

- [ ] Alexei Khamin — finish the test tooling, then start filling in tests — due Sept 25 2026 — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [ ] Alexei Khamin — point his Claude at the repository standard and consult Bosik on the test repository — due unspecified — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]

## Sept 25 2026 — tests may set the PIN and the lease, and a meeting with Alekseev

At the [[wiki/meetings/2026-09-25-daily-standup-engineering-menu-and-jira-discipline.md|Sept-25 Minsk stand-up]] (Russian; label "Alexey Khamin") [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]:

- **Status.** Mostly autotests; he waits for an API from a "Дима" (not resolved). His Sept-24 tooling commitment below is not reported as done.
- **Test settings.** He asked that a test can set a cashier PIN and a lease directly on a terminal, for virtual terminals. Chudinov agreed, as long as the server may overwrite them. See [[wiki/topics/test-automation-strategy.md]] (Sept 25).
- **His pull request.** It is still waiting. Pavel told him to request a meeting with [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]; Irina: include Pavel.

## Open commitments (Sept 25 2026)

- [ ] Alexei Khamin — request a meeting with Evgeniy Alekseev about his waiting pull request, and include Pavel — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]

## Sept 25 2026 (8:05 AM) — the first test runs on the test API, and the test repository needs a shape

On the [[wiki/meetings/2026-09-25-transactional-mvp1-flexport-third-party-egm-compatibility-testing.md|Sept-25 8:05 AM MVP 1 call]] (Russian) [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]:

- **It works.** A Flex IQ version with Chudinov's test API went in about 20 minutes before the meeting, and his test "Заработал почти сразу". Claude ran a demonstration end to end: devices and machine balance, a wallet created on the terminal and scanned on the Flex-Port, the balance checked.
- **The repository.** He is not merging Ivan's pull request yet: first, where tests go and how they are tagged so CI on one product's merge also runs related products' tests. Structure by Monday, with Claude instructions for the test standards; tests over the next two days; then CI with manual start. See [[wiki/topics/test-automation-strategy.md]] (Sept 25, 8:05 AM).
- **Scope question.** He asked who would run the third-party machine tests and what result to expect: "надо бы сначала человека научить".

## Open commitments (Sept 25 2026, 8:05 AM)

- [ ] Alexei Khamin — settle the test-repository structure and test tags, and add Claude instructions with the test standards — due Mon Sept 28 2026 — [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]
- [ ] Alexei Khamin — fill the repository with tests, then start CI with manual start — due about Sept 27 2026 — [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]

## Sept 26 2026 — Flex-Port autotests through the hooks

At the [[wiki/meetings/2026-09-26-flex-port-telnet-console-and-gui-harness.md|Sept-26 Flex-Port development sync]] (Russian; label "Alexey Khamin"), Pavel said "лёша" is writing the Flex-Port autotests, including the link "с машиной" (Khamin's words), using the board's hooks to check whether money was transferred, hung, or ended in an error state. He had no questions. See [[wiki/topics/test-automation-strategy.md]] (Sept 26). *(His Sept-25 test-repository commitments are not reported done.)* [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]

## Sept 28 2026 — the cash-out test, and "who builds the emulators?"

- **At the 4:56 AM stand-up** ([[wiki/meetings/2026-09-28-daily-standup-log-traffic-and-nova-rename.md|Sept-28 Minsk stand-up]], Russian): he wants to close the cash-out autotest that day and will spread Ivan's autotests across the repository by the new rules. Task 16 (deposit to the EGM) has one scenario written. Ports sit on two or three machines, "Одна по центру ванино и и моя" [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]].
- **At the 8:02 AM call** ([[wiki/meetings/2026-09-28-transactional-mvp1-remote-updates-and-october-15-target.md|Sept-28 8:02 AM MVP 1 call]]): he confirmed that in MVP 1 Flex IQ cannot create a ticket with a PIN. He suggested installing the previous build in Georgia and updating remotely to the newest. He asked who builds emulators; Irina: Anton [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].

## Open commitments (Sept 28 2026)

- [x] Alexei Khamin — close the cash-out autotest, and spread Ivan's autotests across the repository by the new rules — due Sept 28 2026 — [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]] — **Sept 29 2026:** Ivan's tests were placed by Claude "так как нужно"; closing the cash-out test is not reported — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

## Sept 29 2026 — TINT-16 and TINT-79, Ivan's tests placed by Claude, and the EGM emulator cases he takes himself

At the [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|Sept-29 Minsk stand-up]] (Russian; label "Alexey Khamin") [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]:

- **Tests.** His main work is "тесты… Тинт… 16 и тинт 79"; he adds scenarios for filed bugs with comments on how it should work, and tests for things not yet implemented. He will close "2 задачи" on bugs and, if nothing else turns up, item 601 that day.
- **Ivan's tests.** "вчера я добавлял ванины тесты и как бы клод хорошо понял систему и положил так как нужно, теггер оставил". He told Ivan to have Claude look at his machine-collection tests, partly in Git already; he will push the rest if needed.
- **The EGM emulator.** He cannot write some scenarios because the EGM/SAS emulator cannot delay or hang; he wrote three points the day before. Pavel: take it, as a separate tab or panel of test cases ("отвечать с задержкой на следующей… пакет там 72 лонгпола"). Khamin: it fits the existing design — "[в]ыставлять флаг какойто". See [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-29 update) and [[wiki/topics/test-automation-strategy.md]] (Sept 29).

## Open commitments (Sept 29 2026)

- [ ] Alexei Khamin — close two bug tasks and item 601 — due Sept 29 2026 — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
- [ ] Alexei Khamin — add the delay / hang test cases to the EGM emulator as a separate tab or panel — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

## Sept 29 2026 (8:06 AM) — the devices the diagram leaves out, Confluence, his old flashing instruction, and the bootloader

On the [[wiki/meetings/2026-09-29-transactional-mvp1-setup-instructions-and-mikrotik-router.md|Sept-29 8:06 AM MVP 1 call]] (Russian; label "Alexey Khamin") [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]:

- **Two remarks on Ivan's instruction.** The diagram does not show "доп устройства типа принтер, бил валидатор и так далее" — required equipment that must also be on site; and the document is better kept in Confluence "чтобы можно было редактировать". Val agreed Confluence can be used for now ([[wiki/topics/docs-as-code-and-atlassian-exit.md]], Sept 29).
- **His Flex-Port flashing instruction.** "У меня есть там инструкция тоже… может устаревшая там для [Flex-Port] как прошивать[,] ване скину, где она лежит". Irina: update it in the same style for the current state; "Да займусь параллельно."
- **The bootloader.** "вчера Алексеев тебе дал рабочую же версию, которая ставится [на] нормальное устройство[,] бут лодер… Говорил в понедельник буду готова, но если нет, значит… через костыли устанавли[ваем]… и обновляем" — Pavel will ask Alekseev. See [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] (Sept-29 update).

## Open commitments (Sept 29 2026, 8:06 AM)

- [x] Alexei Khamin — tell Ivan where the old Flex-Port flashing instruction is, and update it to the current state in the same style, in Confluence — due unspecified ("займусь параллельно") — [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]] — **discharged Sept 30 2026:** Klimovich: "Алексей сегодня добавил, прислал ссылку" — the updated Flex-Port instruction is in Confluence — [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]

## Sept 30 2026 (8:03 AM) — the Flex-Port instruction is in; "a separate product", so its folder goes up a level

On the [[wiki/meetings/2026-09-30-transactional-mvp1-instructions-complete-and-modem-supply.md|Sept-30 8:03 AM MVP 1 call]] (Russian; label "Alexey Khamin") his updated Flex-Port instruction was on screen, inside the FlexPay technical space. His point: "она должна располагаться… на одном уровне с [FlexPay] и [Flex IQ]. [Э]то отдельный продукт все таки" — Klimovich agreed to move it up. He too saw "С картинками проблема" in Ivan's instruction. He is one of the four Pavel named for Elizabeth's chat ("Лёшу"). See [[wiki/topics/docs-as-code-and-atlassian-exit.md]] (Sept 30) and [[wiki/decisions/2026-09-30-elizabeths-georgia-set-up-questions-go-to-a-shared-teams-chat-not-one-person.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]. His Sept-29 EGM-emulator and bug-task commitments were not mentioned.

## Oct 1 2026 — pull-request reviews and the repository structure as his main task; Chudinov's build on his terminal

At the [[wiki/meetings/2026-10-01-daily-standup-sas-mode-flag-and-feature-status-rules.md|Oct-1 Minsk stand-up]] (Russian; label "Alexey Khamin") [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]: "я в основном автотестами. Но больше сейчас почти не могу писать, потому что всё ещё у нас структура работает" (garbled — read as the repository structure still being reworked); "Плюс просматриваю [PR], которые ребята создают"; "[изменения] нужны, ну уже чтобы репозитории нормально работал" (garbled). Irina: "Это основная сейчас. Будет алёша." Chudinov put the new capability-152 build "на терминал, который у лёши" (Khamin's — by context). Pavel named him first among those who could bring up Seregin's emulator environment elsewhere ("с лёшей поработать"). See [[wiki/topics/test-automation-strategy.md]] (Oct 1, 4:48 AM). At the 8:02 AM MVP 1 call he spoke only to say goodbye. His Sept-29 commitments were again not mentioned.

## Open commitments (Oct 1 2026)

- [ ] Alexei Khamin — make the repository-structure changes so the test repositories work properly, reviewing the team's pull requests meanwhile — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]] — *Oct 2 2026: "сегодня ещё надо будет. Както прозу добавить"; weekend plan "привести [репозиторий в] порядок"* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]

## Oct 2 2026 — prose to add, Anton's emulator to try, and the repository in order over the weekend

At the [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 Minsk stand-up]] (Russian; label "Alexey Khamin") [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]: "В основном сейчас [привлекаю — unclear], занимаюсь. И сегодня ещё надо будет. Както прозу добавить. Думаю я Антон попросил ещё этот [эмулятор] попробовать… Можно наверно сегодня" (Anton = [[wiki/people/anton-seregin.md|Seregin]], by context — inference). Irina: "это у тебя таски [FIQU — reading]шные а?" In the weekend round: "Я буду надо привести [репозиторий в] порядок" — after Val's written message to put the repositories in order ([[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]], Oct-2 update). Vladimir is reviewing his work ("ревью лёша"); Irina asked him, Vladimir and Ivan to mark their done items in Jira. See [[wiki/topics/test-automation-strategy.md]] (Oct 2).

## Open commitments (Oct 2 2026)

- [ ] Alexei Khamin — try Seregin's emulator — due Oct 2 2026 ("Можно наверно сегодня") — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]] — *Oct 5 2026: not declared done; he asked how the emulator is built and kept in step with main, and will look at the scripts* — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [ ] Alexei Khamin — bring his repository into order over the weekend of Oct 3–4 2026 — due Oct 5 2026 — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]] — *Oct 5 2026: the weekend went on the rules, the pull-request review and CI/CD (3 of 5 steps); "repository in order" as such not declared done* — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Oct 5 2026 — the weekend's rules and pull-request review, CI/CD at 3 of 5 steps, tests from the 7th, the "Files changed" tab, and "откуда он собирается этот [эмулятор]?"

At the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian; label "Alexey Khamin") [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]: "За выходные… поправил правила… Плюс перепроверял все пиарки для Того, чтобы понять, какие ещё новые дополнительные правила стоит ввести, и CICD начал делать уже там. На 3 из 5 шагов… началось уже заполнение немножко прозы"; to Irina: "я сегодня [с ними] закончу очень надеюсь. И ещё день на прозу мне понадобится. Потом тест" — "то есть с 7 числа" — "Да." Irina named his card tests as the reason for the stand question. To Pavel's missing approve button: "Иди в файл с чейжит? Табу." At the end: "у нас есть сейчас [эмулятор] терминала так, а вот откуда он собирается?… как мы это на эмуляторе получим?"; "мне нужно, чтобы эмулятор соответствовал… коду основного приложения"; on an artifact per build: "не слишком ли это вес? Добавит сборкам"; "Посмотрю, что что есть"; and the letter on "киоск" → "терминал": "У нас и в [Jira] тоже эти фичи названы тоже с киоском. Такой себе." See [[wiki/topics/test-automation-strategy.md]] (Oct 5) and [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Oct-5 update). ("аккумулятор" / "акмулятор" read as emulator — inference.)

### Open commitments (Oct 5 2026)

- [ ] Alexei Khamin — finish the test rules today, one day on prose, then start writing the tests from Oct 7 — due Oct 7 2026 — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [ ] Alexei Khamin — look at the emulator's repository scripts and parameters and build it to match the main application's code — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Oct 5 2026 (8:01 AM) — two gaps the autotests found: no supported-printer list, and a ticket that does not print while the printer is busy

On the [[wiki/meetings/2026-10-05-transactional-mvp1-port-screens-unclaimed-money-and-printer-models.md|Oct-5 8:01 AM MVP 1 call]] (Russian) [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]: he asked that the supported printer models be written into the requirements, since emulators already exist — [[wiki/decisions/2026-10-05-epic-950-is-the-terminal-printer-tested-first-and-all-models-stay-supported.md]]; and whether a print queue is needed when a Flex-Port asks for a ticket while the last one is still in the printer — [[wiki/decisions/2026-10-05-mvp1-has-no-print-queue-and-tickets-print-or-reprint-from-records.md]] (no queue in MVP 1).

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

- [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_2-May-12-2026.md]]
- [[raw/flex_port_update-apr-22-2025.md]]
- [[raw/flex_tower_spacial_design_review-may-1-2025.md]]
- [[raw/Payment HUB_ACH module specification_05.11.25 .md]]
- [[raw/Payment HUB_ACH module specification_06.11.25.md]]
- [[raw/Payment HUB_ACH module specification_10.11.25.md]]
- [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]
- [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
