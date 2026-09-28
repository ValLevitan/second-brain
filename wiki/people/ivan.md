---
type: person
title: Ivan
date: 2025-02-19
aliases: [Ivan, Ivan Shpakov, Иван Шпаков, Ivan Shpak, Ваня]
source-count: 16
open-commitments: 4
disambiguation: "JVL release manager (GLI submittals, release-candidate marks). Not the bank representative Ivan of the Sept-25-2026 CIBC call (surname Lucic per the notes) — see wiki/meetings/2026-09-25-cibc-ivan-lucic-600k-transfer-post-dated.md. Resolve by context: releases/GLI → this page."
---

# Ivan

Ivan handles JVL's **release scheduling and certification paperwork** — the release-manager role Val wants driving proactive coordination with GLI. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Role

- On the Feb 19 alignment call, Val told Pavel to "put Ivan on it" to **start scheduling with GLI ahead of time** (GLI needs scheduling, JVL has PO-signing to do), and stressed the "looping" discipline — repeatedly checking back that the scheduled work is actually happening. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- Ivan sends the paperwork to GLI; Val noted costs can be kept low by detailing exactly what changed so GLI doesn't retest untouched code — the **release notes** (generated from Jira stories, with ChatGPT wording that must be checked) plus Irina's separate **diffs document**. See [[wiki/projects/georgia-market-rollout.md]] and [[wiki/projects/south-dakota-vlt-market.md]]. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

**Surname (Oct 22 2025):** in the Calle Ocho practice-release session Val named the release-manager Ivan as **"Иван Шпаков" (Ivan Shpakov)** — same release/build-marking role, so recorded as this Ivan's transcribed surname. [[raw/practice_release_calle_ocho-github-october-21-2025.md]] (Distinct from any "Ivan" greeted in the Puerto Rico contacts — see Owner Decisions.)

**Not the bank's Ivan.** The "Ivan" who calls Val on Sept 25 2026 about a CAD 600,000 transfer is a bank representative ("it's Ivan calling you for Premium Edge"), not this Ivan — see [[wiki/meetings/2026-09-25-cibc-ivan-lucic-600k-transfer-post-dated.md]]. [[raw/Meeting_Transcript_CIBC_Ivan_Lucic_840914_600K_Transfer-September-25-2026.md]]

## Release-manager role in the GitHub pipeline (Oct 21–22 2025)

The late-October release-management sessions ([[wiki/topics/github-release-management-pipeline.md]]) made Ivan's job concrete in the new GitHub flow:

- **He gates and ships releases.** Ivan watches for a build that has passed the automated **lint → test → build** pipeline, judges whether it is genuinely ready, hands the candidate to human game-play testing, then packages the exact **immutable tagged version** and takes it to **GLI** for certification (a manual email/phone process). He is the **liaison** between JVL and GLI and manages the **cost of each submittal**. Aaron noted **Eclipse** is an organisation similar to GLI. His old habit of tracking release numbers in Jira plans is dropped — he now references GitHub. [[raw/releases_github-october-21-2025.md]]
- **He owns the release-candidate mark and the manifest versions.** Any developer can build and download an artifact, but **marking an artifact field-ready is Ivan's job** — he runs (or triggers) a build action with the **full test list**, and only after all tests pass is the build tagged a **release candidate**; on each release he fills the **flex-os-installer manifest** with the specific version of each component for that build. [[raw/practice_release_calle_ocho-github-october-21-2025.md]] [[raw/artifacts_assembly_GitHub-october-21-2025.md]]
- **Calle Ocho practice release:** Val wanted the Omni Calle Ocho build assembled **by Ivan** (with Pavel standing aside to answer questions) as a dry-run of the release-manager flow, and scheduled a follow-up the next Wednesday with Ivan invited. [[raw/practice_release_calle_ocho-github-october-21-2025.md]]

## Machine-settings support flow (Apr 15 2025)

- Klimovich's working example of a flow that needs no Val involvement: operator requests for machine settings ("установку определенных настроек для min, max, bet") go to Ivan via a support ticket — "я знаю по процессу, что эту задачу будет делать Ваня, Иван. Потому что он отвечает за настройку и проверку" — and he turns them around in ~3 days with an estimate first. [[raw/andrei _klimovich_update-apr-15-2025.md]]

## Eclipse-lab liaison on the SAS 51/52 issue (Apr 14 2025)

- Ivan is the person who "communicated the most with **Steve**" at the **Eclipse** lab on the Georgia COAM **SAS event 51/52** (hand-pay / hand-pay-reset) compliance question — he holds Steve's written question ("I used to do this test, now I can't, did you change something?"). See [[wiki/meetings/2025-04-14-sas-51-52-georgia-coam-interpretation.md]] and the thread on [[wiki/projects/georgia-market-rollout.md]]. [[raw/sas_51_52_requirement_interpretation-april-14-2025.md]]

## Georgia submission: he sends the bin file (stated Sept 11 2026)

At the [[wiki/meetings/2026-09-11-nova-game-change-regulatory-procedure.md|Sept-11 2026 regulatory call]], [[wiki/people/pavel.md|Pavel Frolov]] corrected [[wiki/people/juan-martinez.md|Juan Martinez]]'s belief that Georgia uses no bin file. It is used, once, at submission, and Ivan is the one who sends it — "**During submission, Ivan is doing this**" [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]].

The Georgia bin file carries only SAS-operation data, not game sets, which is the reason a new game can ship without the Lottery learning of it — see [[wiki/organizations/georgia-lottery-corporation.md]] (Sept 11) [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]].

## Sept 22 2026 — he chases an overdue CMS release

At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 stand-up]] (Russian; label "Ivan Shpak"), he asked for the release of changes requested the day before: "до сих пор нету. Сделайте, пожалуйста, сегодня это прям кровь из носу надо". Pavel gave it to [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] — "Компонентов, которые менялись для CMS сервера" [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]. Irina said Ivan ("Ваня") was installing a version in which a maths error surfaced; she will work it with him (see [[wiki/people/irina-shishko.md]], Sept 22) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

## Sept 22 2026 (8:01 AM, in absentia) — named for the end-to-end test work

On the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 8:01 AM MVP 1 call]], Pavel listed "иван" among those who should write the end-to-end tests with Claude, and Val asked for "Ивана и Алексея" to be put on the schedule for it. No surname is spoken; he is matched to this page by context (the roster "Shpak, Ivan", and the test role he shares with Alexei Khamin). See [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

## Sept 23 2026 — trying Claude as an autotest writer

At the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]] (Russian; label "Ivan Shpak"): "Пробуя себя в виде оператора Клода, который умеет писать автотест." See [[wiki/topics/test-automation-strategy.md]] (Sept 23). [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]

## Sept 23 2026 (8:00 AM) — eight connection tests, four still manual

On the [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept-23 8:00 AM MVP 1 call]] (Russian; label "Ivan Shpak") he reported 8 tests for the machine-to-Flex-Port connection; 4 run on their own and 4 still need a hand on the cable, because he found no way to disable the SAS wire in software. Pavel gave the method on the call — repoint the port's symbolic link to /dev/null — and Ivan will rewrite the tests. See [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]] (Sept-23 update) [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

## Open commitments (Sept 23 2026, 8:00 AM)

- [x] Ivan — rewrite the four manual connection tests using the symlink-to-/dev/null method — due unspecified — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]] — **discharged Sept 24 2026:** "что надо было руками это исправлено" (it needed commits into the firmware; the method is not stated) — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]

## Sept 24 2026 — the Georgia lab file for 15 games, and write access he did not ask for

At the [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|Sept-24 Minsk stand-up]] (Russian; label "Ivan Shpak") [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]:

- **Georgia.** He made the MD file for Georgia COAM V3 (inference) with all 15 games, though only 10 run at once, and warned of possible delays in Intralot's tests. See [[wiki/projects/georgia-market-rollout.md]] (Sept 24).
- **The cashout button.** He pointed to the RIS screen-cashout parameter that hides the cashout button. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 24).
- **Write access.** He said he does not need write rights; Irina ruled he gets them. See [[wiki/topics/test-automation-strategy.md]] (Sept 24).

## Open commitments (Sept 24 2026)

- [ ] Ivan — tell Kovalchuk which repository needs write access, and take the rights — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]

## Sept 24 2026 (5:41 AM) — the battery test, and whether a lease user could be shared

At the [[wiki/meetings/2026-09-24-georgia-hard-reset-remedies-and-passport-removal.md|Sept-24 5:41 AM hard-reset review]] (Russian; label "Ivan Shpak") [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]:

- **Battery.** He offered to test the power-off battery swap on the Georgia machine behind Irina that still has the bad battery. See [[wiki/topics/ris-remote-install-and-machine-states.md]] (Sept 24).
- **A limited user.** He asked about the internal web user used to scan leases, and suggested a user "у которого будут права только отсканить паспорт". The account name is not recorded.
- **Leases.** He noticed some fully paid machines have the lease-scan box crossed, while many had leases "до 22 сентября". See [[wiki/projects/georgia-market-rollout.md]] (Sept 24, 5:41 AM).

## Open commitments (Sept 24 2026, 5:41 AM)

- [ ] Ivan — test the battery swap with the power off on the Georgia machine with the bad battery, and confirm whether it gives the yellow screen — due Sept 24 2026 ("Я сейчас с батарейкой ещё посмотрю") — [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]

## Sept 24 2026 (8:01 AM) — the manual tests are fixed, and the commit rule lands on his local work

On the [[wiki/meetings/2026-09-24-transactional-mvp1-flexport-money-loss-bugs-and-release-date.md|Sept-24 8:01 AM MVP 1 call]] (Russian; label "Ivan Shpak") [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]:

- **Tests.** What needed hands the day before is fixed — it needed commits into the firmware. He checks Flex-Port-to-machine connections against a 20-second budget and next wants the negative cases. See [[wiki/topics/test-automation-strategy.md]] (Sept 24, 8:01 AM).
- **Local only.** The work was "только локально на компьютере никуда не комичено", which drew Val's rule: commit several times a day, no more than 300 lines held locally. See [[wiki/decisions/2026-09-14-main-branch-must-always-build-and-the-code-belongs-to-the-project.md]] (Sept-24 update).
- **Bug 349.** He noted machines and Flex-Ports start up at different speeds. See [[wiki/decisions/2026-09-24-a-flex-port-that-dies-holding-money-sends-it-to-unclaimed-and-one-without-a-gateway-goes-out-of-service.md]].

## Open commitments (Sept 24 2026, 8:01 AM)

- [ ] Ivan — commit his local connection-test work to GitHub — due Sept 24 2026 (Irina: "вечером он закомтил") — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]

## Sept 25 2026 (8:05 AM) — he takes the set-up instruction for third-party machine tests

On the [[wiki/meetings/2026-09-25-transactional-mvp1-flexport-third-party-egm-compatibility-testing.md|Sept-25 8:05 AM MVP 1 call]] (Russian) [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]:

- **What the test site needs**, in his words: the right cables; a computer for the SAS emulator with a COM port, best from the motherboard ("USB tome это плохая идея, но… реализуемая"); at least two cables; and the IGT SAS host simulator he works with. Irina: nobody knows it better, so he writes the instruction. "Я к понедельнику постараюсь всё это сделать." See [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] (Sept-25 update).
- **His tests.** Irina: his tests worked the day before; he and Khamin are merging the work. He opened a pull request in the transactional platform repository. See [[wiki/topics/test-automation-strategy.md]] (Sept 25, 8:05 AM).
- He had been left off Klimovich's report by mistake — the reason for the new mailing list.

## Open commitments (Sept 25 2026, 8:05 AM)

- [ ] Ivan — write the compatibility-test set-up instruction and attach the SAS emulator and the SAS commands document — due Mon Sept 28 2026 — [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]

## Sources

- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- [[raw/andrei _klimovich_update-apr-15-2025.md]]
- [[raw/sas_51_52_requirement_interpretation-april-14-2025.md]]
- [[raw/releases_github-october-21-2025.md]]
- [[raw/artifacts_assembly_GitHub-october-21-2025.md]]
- [[raw/practice_release_calle_ocho-github-october-21-2025.md]]
- [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]
- [[raw/Meeting_Transcript_CIBC_Ivan_Lucic_840914_600K_Transfer-September-25-2026.md]]
