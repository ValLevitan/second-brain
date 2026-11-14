---
type: person
title: Ivan
date: 2025-02-19
aliases: [Ivan, Ivan Shpakov, Иван Шпаков, Ivan Shpak, Ваня]
source-count: 75
open-commitments: 17
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

- [x] Ivan — write the compatibility-test set-up instruction and attach the SAS emulator and the SAS commands document — due Mon Sept 28 2026 — [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]] — **written Sept 28 2026** ("я написал инструкцию вчера… [в] pdf формате"), with no links to the program yet on purpose; sending is a new commitment below (Sept 29) — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

## Sept 28 2026 — the latest Flex-Port on his machine, and the Georgia set-up document

- **At the 4:56 AM stand-up** ([[wiki/meetings/2026-09-28-daily-standup-log-traffic-and-nova-rename.md|Sept-28 Minsk stand-up]], Russian; label "Ivan Shpak"): he will put the latest Flex-Port version on his real machine ("Я к себе поставлю"). His priorities: an installation, the drafts sent on Friday, autotests, then the instruction — which will not be ready that day; Irina: a feature is needed for it. He keeps working on his draft autotest [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]].
- **At the 8:02 AM call** ([[wiki/meetings/2026-09-28-transactional-mvp1-remote-updates-and-october-15-target.md|Sept-28 8:02 AM MVP 1 call]]; in absentia): Irina said he finished one test-set feature and took the next, and is preparing a document, to send the next day, on how to set up the machine, port and SAS in Georgia [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].

## Open commitments (Sept 28 2026)

- [ ] Ivan — install the latest Flex-Port version on his real machine — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [x] Ivan — send the document on setting up the machine, port and SAS in Georgia — due Sept 29 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]] — *Sept 29: very likely the same PDF instruction he wrote on Sept 28 (**inference**); Irina told him to send it by email — see below* — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]] — **discharged Sept 29 2026:** sent that morning and walked through at the 8:06 AM call (Klimovich: "этот документ, который ты сегодня прислал") — [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]

## Sept 29 2026 — the modem fix to rebuild, the instruction by email, and the build he keeps

At the [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|Sept-29 Minsk stand-up]] (Russian; label "Ivan Shpak") [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]:

- **Main task.** "основная будет это фикс по модемам пересобрать всё сделать, проверить" — rebuild and verify the modem fix; Kharetski will tell him when the 4.50.2 build is ready. He checks the release before it goes (Irina: "ваня проверит"). See [[wiki/decisions/2026-09-29-the-fix-goes-out-as-a-re-release-not-a-hack-and-only-that-commit-goes-in.md]].
- **The stand.** Switching it to 4.50.2 may remove what his autotests need; "У меня бинт есть собранные, просто его не буду сносить" — he keeps his build.
- **Autotest.** It "дальше пишется"; he has a question for colleagues on why the tests do not pass cleanly — Khamin: let Claude look at Khamin's machine-collection tests. See [[wiki/topics/test-automation-strategy.md]] (Sept 29).
- **The instruction.** Written the day before, "[в] pdf формате выглядит вроде неплохо", no program links yet; Irina: send it by email, not into the group, so people can read it before the later meeting. See [[wiki/decisions/2026-09-24-written-records-go-by-email-and-chats-are-for-instant-matters.md]] (Sept-29 update).

## Open commitments (Sept 29 2026)

- [ ] Ivan — rebuild and verify the modem fix once Kharetski's 4.50.2 build arrives — due unspecified (re-release not before Sept 30 2026) — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]] — *Sept 30 2026: not mentioned; Kharetski reported the Georgia fixes finished* — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]] — *Oct 1 2026: he works "С Женей" (Kharetski, by context), and Pavel said the team's SIM "сейчас у Ивана тестируется. Как работает [gom в 3] с модемом" — a modem test is under way; the fix is not named* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]
- [x] Ivan — send the instruction (PDF) by email before the later meeting that day — due Sept 29 2026 — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]] — **discharged Sept 29 2026:** at the 8:06 AM call Klimovich called it "этот документ, который ты сегодня прислал" — [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]

## Sept 29 2026 (8:06 AM) — he walks the team through the set-up instruction, and it goes to Confluence with the SAS tool

On the [[wiki/meetings/2026-09-29-transactional-mvp1-setup-instructions-and-mikrotik-router.md|Sept-29 8:06 AM MVP 1 call]] (Russian; label "Ivan Shpak") he shared the instruction on screen ("Могу чуть уменьшиться так или плохо?") [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]:

- **What it covers.** A Flex-Port and Flex IQ already set up; the connections Flex-Port–machine and machine–PC, where the SAS emulator runs; the emulator set-up commands; and the Eclipse long-poll commands with what the machine should show for each ("допустим 1 команда, что мы блокируем машину вот такое должно быть на машине"). Screenshots "где можно", text where not. His key warning: the SAS checkbox on the machine must be on the port where the Flex-Port sits — "если её настроить не на том порту, то… флекспорт у нас работать не будет". Klimovich: "Отличная работа, Спасибо большое."
- **What is missing**, in his words: "как прошить флекспорт… и 2 это флекс IQ то же самое. Вот эти 2 документа." He prefers separate documents side by side, in order: Flex IQ set-up and install, Flex-Port set-up and install, then his machine-plus-port document.
- **Screenshots.** Pavel wanted screen captures, not photographs; Ivan: hard with two computers, "чуть дополнительный геморрой, поэтому я снимал на камеру[,] я не спорю".
- **Confluence.** He will put it in as separate pages. He had emailed the SAS tool zip to Elizabeth; Klimovich wants it reachable by all JVL staff with the link in the instruction; "Давай я попробую в [Confluence] залить… [е]сли нет что, то придумаем."
- See [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] (Sept-29 update) and [[wiki/topics/docs-as-code-and-atlassian-exit.md]] (Sept 29).

## Open commitments (Sept 29 2026, 8:06 AM)

- [x] Ivan — put the set-up instruction into Confluence as separate pages — due about Sept 30 2026 (Klimovich: "если у нас завтра всё готово") — [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]] — **discharged Sept 30 2026:** Klimovich found "рядом… лежала инструкция вани" in Confluence; the pictures broke and he restored them — [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [x] Ivan — try to attach the SAS tool zip to the Confluence instruction so all JVL staff can reach it; else find another place — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]] — **discharged Sept 30 2026 (inference):** "В [эмуляторе], который я скинул… Араровский архив, чтоб он копировался. Я в комментарии добавил… внизу" — the emulator goes as an archive in a comment at the foot of the page; read as the SAS tool ("аккумулятор" = emulator, as throughout) — [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]

## Sept 30 2026 — the remaining tests, Eclipse and "Alex", and the network-loss question

At the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian; label "Ivan Shpak") [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]:

- **Tests.** "Для протокола один 74, дальше без протокола" (garbled). "самый основной тест, который остался": "С прод с продсервером и должны были вытягивать инсталляцию и при этом… как тогда будет вести себя поиск прогресса в контроллер" (read as the progressive controller — **inference**); then "подключаю отдельную сеть" for the network tests. See [[wiki/topics/test-automation-strategy.md]] (Sept 30, 4:57 AM).
- **Eclipse.** "что мы тогда делаем с [Эклипсом]? Ждём пока моего ответа я сразу договариваюсь с Алексом" — he waits for an answer, then arranges with "Алекс" (**not resolved**); what the Eclipse item is, is not said. See [[wiki/organizations/eclipse-gaming-lab.md]] (Sept 30).
- **Network loss.** His reading — no tilt, collect allowed but fails with an error, a retry if the network returns, otherwise the credits stay on the machine — Pavel: "Да, я думаю что так." He does not set the "fault if SAS link down" checkbox: "никто не говорил, что нужно её ставить." See [[wiki/decisions/2026-09-24-a-flex-port-that-dies-holding-money-sends-it-to-unclaimed-and-one-without-a-gateway-goes-out-of-service.md]] (Sept-30 update).

## Open commitments (Sept 30 2026)

- [ ] Ivan — run the production-server install test with the progressive-controller behaviour, then the network tests on a separate network — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]

## Sept 30 2026 (8:03 AM) — the pictures in his instruction, restored; the emulator as an archive in a comment

On the [[wiki/meetings/2026-09-30-transactional-mvp1-instructions-complete-and-modem-supply.md|Sept-30 8:03 AM MVP 1 call]] (Russian; label "Ivan Shpak") his instruction showed "превью [unavailable]" to Klimovich and Khamin; "у меня с утра, когда я это всё вкинулся, было хорошо, а сейчас тоже проблема"; he posted a link in the group, and by the end: "Я картинки вернул, посмотрите, пожалуйста." Pictures added in the page body "почемуто вот такой ерундой страдают", so the emulator he posted goes as an archive in a comment at the foot — Klimovich: "на скачку пошёл картинки подсосались тоже вижу." See [[wiki/topics/docs-as-code-and-atlassian-exit.md]] (Sept 30) [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]].

## Oct 1 2026 — autotests "with Zhenya", and the team's one SIM is with him for a modem test

At the [[wiki/meetings/2026-10-01-daily-standup-sas-mode-flag-and-feature-status-rules.md|Oct-1 Minsk stand-up]] (Russian; label "Ivan Shpak") his whole report: "С Женей авто тесты и все остальное, что хотите от меня всё это делают" — autotests with Zhenya ([[wiki/people/evgeny-kharetski.md|Kharetski]], by context — inference; on Sept 29 Pavel spoke of "то, что сейчас женя делает с Иваном") [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]. At the [[wiki/meetings/2026-10-01-transactional-mvp1-status-slice-and-sas-command-logging.md|8:02 AM MVP 1 call]] (label "Ivan Shpak"; he said only "Счастливо") Pavel, asked for a SIM by Bosik: "Симку можно у Ивана будет забрать. Ну, он сейчас заканчивает" — not today; "Симка сейчас у Ивана тестируется. Как работает [gom в 3] с модемом" (the derived notes read "GOM V3" [[raw/Meeting_Notes_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]); Bosik will wait for "ванино". His Sept-30 test commitment above is not mentioned. See [[wiki/decisions/2026-09-04-north-america-modem-variant-and-ask-kore-for-the-apn.md]] (Oct-1 update) [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]].

## Oct 2 2026 — the files to Eclipse and build 43.33, Efim's South Dakota note (50 cents to 40), a RIS and no rebuild, and the South Dakota autotests in parallel

At the [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 Minsk stand-up]] (Russian; label "Ivan Shpak") [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]:

- **Eclipse.** "Сейчас отправлю этому в [Эклипс], в общем. Файле, к котором еще не обсуждали с тобой. Если все будет хорошо, то, по идее, сегодня драфты получше, они уже сертификаты… посмотрите глазами драфт, скажите там всё ок"; "Сам [билд], я ещё не закидывал, сейчас закинул" — "43, 33". Irina: give the build number and the amounts the certificate lists. See [[wiki/organizations/eclipse-gaming-lab.md]] (Oct 2).
- **South Dakota.** "у меня ефим вчера много чего писал я Ирине перекидывал. Это касательно [South Dakota]… Я так понимаю для математики?… где было 50 центов. Минимальная ставка сделали 40 или мне это сделать 40 самому пересмотреть нам уже как бы сдавать надо… либо пересобрать или чтото посмотреть… Возможно, сегодня тогда всё отдам, но это нужно после обеда"; "Ещё тогда [Жене] нужно будет. И наверное, это Антона зарелизить свою часть, если надо" (Anton **not resolved**); "это после митинга будем определять… Эти автотесты в параллели тут как могу, так и пишу"; "Пересобирать не надо, [коммитов] не было." ("ефим" = [[wiki/people/efim-podvoiski.md|Efim]], by context.) See [[wiki/projects/south-dakota-vlt-market.md]] (Oct 2).
- **Statistics.** Kharetski: "Вчера с ваней, я работал по статистике" (Ivan by context). Irina asked him, Vladimir and Khamin to mark their done items in Jira. His Sept-30 test commitment above is again not mentioned.

## Open commitments (Oct 2 2026)

- [ ] Ivan — send the files to Eclipse, upload the build, and give Irina the build number (43.33) and the certificate amounts — due Oct 2 2026 — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [ ] Ivan — create a RIS with the 40-cent minimum bet for South Dakota per Efim's note and check that the machine comes up; no rebuild — due Oct 2 2026 ("после обеда") — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]

## Oct 5 2026 — a new build onto the stick, then autotests in parallel; named with Kharetski to judge the SAS traffic

At the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian; label "Ivan Shpak") [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]: "Я собрал новую [сборку]. То есть сейчас уже записано флэшку поставлю, будем смотреть то что. Он тогда просил обновлённые эти минимальные данные… И дальше авто тесты в параллели" (who "он" is and which minimum data — **unclear**; the 40-cent South Dakota minimum of Oct 2 by context — inference). Chudinov, on the SAS traffic: "нормально, ненормально женя скажет ваня, я не знаю" ([[wiki/decisions/2026-10-02-sas-command-logs-are-collected-on-the-flex-iq-and-not-sent-to-grafana-by-default.md]], Oct-5 update). Eclipse and build 43.33 were not mentioned; his Oct-2 commitments above stand.

### Open commitments (Oct 5 2026)

- [ ] Ivan — put the new build on the stick, test it, then continue the autotests in parallel — due Oct 5 2026 — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Oct 6 2026 — South Dakota overnight, the critical error to re-check, and three battery cases

At the [[wiki/meetings/2026-10-06-daily-standup-ris-georgia-branch-and-critical-error-text.md|Oct-6 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]:

- South Dakota production minimum bets ran fine overnight; Igor's crash did not repeat ("Он один раз словился и всё"). If South Dakota holds for an hour, he will ask Kharetski to release the DC.
- He must first confirm whether the critical error still repeats — [[wiki/decisions/2026-10-05-the-critical-error-screen-shows-the-cause-and-fix-in-words-and-keeps-the-qr-code-in-mvp1.md]].
- Pavel set three battery cases with the machine off (see [[wiki/topics/ris-remote-install-and-machine-states.md]]). Ivan needs a device that sets the voltage; he has only a battery of about 3.2 V and a good one.

### Open commitments (Oct 6 2026)

- [ ] Ivan — run the three battery-swap cases with the machine off — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]

## Oct 7 2026 — yesterday's South Dakota issue, then hand over; the battery next

At the [[wiki/meetings/2026-10-07-daily-standup-test-coverage-first-and-ai-task-numbers.md|Oct-7 Minsk stand-up]] (Russian; label "Ivan Shpak") [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]: he puts South Dakota back on to look at yesterday's issue ("Ни бак я не знаю теперь что это недочёт" — not sure it is a bug), then hands South Dakota over; "приоритет 2 это с батарейкой разобраться" — the battery next. He told Pavel that Wi-Fi items in his story can be ignored, since Wi-Fi is still in development. See [[wiki/topics/test-automation-strategy.md]] (Oct 7).

### Open commitments (Oct 7 2026)

- [ ] Ivan — check yesterday's South Dakota issue and hand South Dakota over, then the battery work — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]

## Oct 8 2026 — the third rebuild, then TIN-13, then the battery

At the [[wiki/meetings/2026-10-08-daily-standup-lease-expiry-scenarios-and-flex-signal-quality.md|Oct-8 Minsk stand-up]] (Russian; label "Ivan Shpak") [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]: he is rebuilding the version a third time and hopes it is the last, done today. Then autotest TIN-13. Then the battery: he will come for the equipment in the afternoon; Pavel: the feature may be with "Жени" (which Zhenya is **unclear**) and a story for the experiment is probably needed — [[wiki/topics/test-automation-strategy.md]] (Oct 8).

### Open commitments (Oct 8 2026)

- [ ] Ivan — finish the rebuild, then TIN-13, then the battery work — due Oct 8 2026 for the rebuild ("сегодня") — [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]

## Oct 9 2026 — Elizabeth's SAS works (with Claude's help); the installation to send; TIN-11, 1250, then the battery

- At the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 stand-up]]: he found the machine they worked on and will create and send the installation; TIN-11's test in progress; looking at 1250; then the battery. The night before he helped Elizabeth from home get SAS working with the SAS test tool (link up, pings) — [[wiki/topics/test-automation-strategy.md]] (Oct 9) [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].
- On the [[wiki/meetings/2026-10-09-transactional-mvp1-test-machines-and-unclaimed-funds.md|Oct-9 Transactional MVP 1 call]] he told the story: a long fight, a wrong cable, then Claude on his work laptop "сделан по факту те же самые действия, что и я, и у него прокатил"; done by 9 PM Minsk time — [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] (Oct-9 update) [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]].

## Oct 12 2026 — autotests first, one a day to the 15th

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 stand-up]]: Irina keeps him on autotests ("Ваня сейчас занят он сначала авто тесты"), one a day to the 15th, so he does not test Kharetski's work — [[wiki/topics/test-automation-strategy.md]] (Oct 12) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].

## Oct 13 2026 — TIN-17 done but not merged; waiting on TIN-26; task 89 next

At the [[wiki/meetings/2026-10-13-daily-standup-video-decode-memory-and-release-task-type.md|Oct-13 stand-up]]: TIN-17 is not merged because of an error in main; he waits on answers to at least four TIN-26 questions from Pavel and starts task 89 — [[wiki/topics/test-automation-strategy.md]] (Oct 13) [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]].

## Oct 14 2026 — task 128 not reproduced; rebuild and rerun; then autotest 66

At the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 stand-up]] Pavel said his Claude ran about 400 transactions overnight on task 128 without reproducing the problem; Ivan will rebuild the port, install it and rerun (Irina: urgent), then take autotest 66 from Irina — [[wiki/topics/test-automation-strategy.md]] (Oct 14) [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

## Oct 15 2026 — no direct network access to the production FlexPort firmware; the test feature to Blocked

At the [[wiki/meetings/2026-10-15-daily-standup-offline-ris-fallback-and-nova-game-conversion.md|Oct-15 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]: Claude's port scan found no direct network access to the production FlexPort firmware; he will try himself. After Vladimir he checks Pavel's experimental build; Irina asked him to move the waiting test feature to Blocked — "Сейчас переведу" — [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 15). Kharetski sent the battery plan back to him for a hands-on check — [[wiki/topics/nova-platform-architecture.md]] (Oct 15).

## Oct 16 2026 — the 0x89 case after a DHCP change; PR 226; 66, then TIN 80

At the [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct-16 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] he described a test where a transaction right after a DHCP change of the machine's IP failed with 0x89 because the port had not registered yet; Pavel thinks it is not a real case, so Ivan will ask what the fix involves and skip it if not needed. He commented on PR 226, has another PR open, works on 66, then "тинт 80". He did not give out the previous day's release and does not know who did — [[wiki/topics/test-automation-strategy.md]] (Oct 16).

## Oct 19 2026 — battery replacement with Kharetski

At the [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct-19 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] he works with Evgeny Kharetski on battery replacement; Evgeny answered his 14 questions the day before — [[wiki/topics/test-automation-strategy.md]] (Oct 19).

At the [[wiki/meetings/2026-10-20-daily-standup-io-board-firmware-via-github-and-vp9-video-decode.md|Oct-20 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]] he works on the RIS performance tasks; little is left on the battery. He asked how hardware tracking now works with the passport window and will test without the checkbox first, then with it — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 20); [[wiki/topics/test-automation-strategy.md]] (Oct 20).

## Oct 20 2026 (8:31 AM, in absentia) — automated tests for bill-validator emulation mode

At the [[wiki/meetings/2026-10-20-third-party-egm-bv-emulation-mode-and-sas-data.md|Oct-20 8:31 AM third-party EGM call]] Pavel said most of the next week's work falls on QA — Irina "с командой лёша иван" — creating and starting the automated-test tasks for bill-validator emulation mode — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]] [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]] [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].

## Oct 21 2026 — checking the RIS work

At the [[wiki/meetings/2026-10-21-daily-standup-flex-port-mode-switch-and-sas-crc-fix.md|Oct-21 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]] he said he continues on RIS, checking what Kharetski did and what Tsymanov is doing; Tsymanov's part is not finished — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 21).

## Oct 22 2026 — RIS performance; "no change" is not an update

At the [[wiki/meetings/2026-10-22-daily-standup-flex-port-cashout-screens-and-native-engine.md|Oct-22 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] he first said "без изменений"; Pavel said the stand-up is written for the PM — [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-22 update). He works on RIS on the machine (Pavel: RIS performance); the machine side is mostly checked — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 22).

## Oct 23 2026 — SAS 21 is fast; overdue test dates and test plans

At the [[wiki/meetings/2026-10-23-daily-standup-bill-validator-lockout-and-atlanta-port-test.md|Oct-23 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]] he said the only checksum request he knows is SAS 21 (the ROM signature), which takes very little time even during play — [[wiki/organizations/intralot.md]] (Oct 23). He continues on RIS; he is to update the end dates of overdue tests and recount the test plans against the latest requirements — [[wiki/decisions/2026-10-20-the-ris-improvements-release-notes-are-settled-point-by-point-and-the-tasks-are-to-be-rewritten-to-match-them.md]] (Oct-23 note).

## Oct 27–28 2026 — the installer errors and keeping old RIS data

At the [[wiki/meetings/2026-10-27-daily-standup-cashout-merging-and-remote-updates.md|Oct-27 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]] he took Pavel's installer error-screen document to read and test — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 27). At the [[wiki/meetings/2026-10-28-daily-standup-flex-port-firmware-delivery-and-reopening-completed-features.md|Oct-28 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] he asked about the installer that keeps old RIS data and pointed Pavel to build 4353 (heard) on the 224 server — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 28).

## Oct 29 2026 — checking Pavel's installer; old RIS cannot be applied with linked progressives

At the [[wiki/meetings/2026-10-29-daily-standup-cash-out-progress-screen-and-pulse-mode-installs.md|Oct-29 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]] he said he built to check Pavel's installer changes and continues on RIS. Old RIS data are kept but cannot be applied, because the master controller does not know which to take; a short meeting at 12:40 follows — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 29).

## Nov 2 2026 — a RIS build with the modem installed on the Echo; STG only, not prod; Wednesday with Chudinov

At the [[wiki/meetings/2026-11-02-daily-standup-flex-port-release-build-and-rust-sound-library.md|Nov-2 stand-up]] (Russian; label "Ivan Shpak") [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]: "я продолжаю с рисом, я собрал билт, даже модем закинул. Распоставлено эхо" — a RIS build with the modem, installed on the Echo; Irina: check that the games run and the printer works on the Echo, and whether STG / RIS get through over the modem — "тодем живой"; otherwise the same as on an ordinary machine [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] — [[wiki/topics/echo-home-gaming-device.md]] (Nov 2–3) · [[wiki/topics/ris-remote-install-and-machine-states.md]] (Nov 2–3). On Chudinov's prod deploy: "прот не трогаю я только со стыгаю работаю" (prod untouched; STG only); he will check whether Tsymanov's work can go to prod — "Давай и в среду… поговорим более предметно" [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] — [[wiki/people/dmitri-chudinov.md]] (Nov 2), where the Wednesday commitment is tracked.

### Open commitments (Nov 2 2026)

- [ ] [[wiki/people/ivan.md|Ivan]] — test the RIS build with the modem on the Echo: games, the printer, the modem link to STG — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]

## Nov 3 2026 — what to check on the Echo: two SAS outputs, the bill validator, a Gen 2 / Nanoptix-class printer

At the [[wiki/meetings/2026-11-03-daily-standup-sim-traffic-alert-and-flex-iq-release-action.md|Nov-3 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] Pavel listed the checks: that the Echo machine on hand has two SAS outputs ("2 саса выведены"), else bring them out; connect the "ситолтовский" bill validator (heard; "Боевой 50" — the notes: BV-50 — through an adapter, on the table at the end, rarely connected) and check it works; and connect a "Ген 2", "День 5" (heard) or "ноктикс" (Nanoptix, heard) printer at least, to make sure nothing broke in protocol 2 ("по 2 протоколу общения") [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]. Ivan has an "Эпик 950" working — printed tickets, cash-out; Pavel: the customer wrote of an external printer, and for the Flex IQ JVL will use a TransAct printer in an external housing, so a printer in its own housing is likely here too; "Я проверю" [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] — [[wiki/topics/echo-home-gaming-device.md]] (Nov 2–3). He asked about the handpay bug: seen in release 1? [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]

### Open commitments (Nov 3 2026)

- [ ] (blocked-on: Echo-bill-acceptor) [[wiki/people/ivan.md|Ivan]] — on the Echo: confirm two SAS outputs, connect the bill validator ("BV-50" per the notes) through the adapter, and test a Gen 2 / Nanoptix-class printer on protocol 2 — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] — *Nov 4 2026: Pavel paused the Echo — "Эхо не надо… отложен проект" — until a bill acceptor that reads tickets is found; parked, not discharged* — [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]

## Nov 4 2026 — one more bug after Kharetski's fix; SAS needed to reproduce the field case; the Echo is paused for him; named release manager for the transactional release (in absentia)

At the [[wiki/meetings/2026-11-04-daily-standup-release-build-handoff-and-nad2-product-code.md|Nov-4 stand-up]] (Russian; label "Ivan Shpak") [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]: he checked what Kharetski fixed and "нашёл ещё один бак", which he wrote up; he waits for Kharetski's SAS tool — "нам нужно посмотреть, что один б, если мы перестанем отвечать по умолчанию" (heard) — so the field case can be reproduced, "пока что это невозможно"; Kharetski needs SAS access from him to finish, and asked that nobody take Ivan's machine without permission [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]. In the "Dakota" handpay bug he is the one who powers the machine off fully — "Я выключаю питание полностью. То есть принтер также выключается" — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Nov 4). He meant to look at the Echo next; Pavel: "Эхо не надо… отложен проект"; he stays on the printer problems — "они теперь у меня на паузе" — [[wiki/topics/echo-home-gaming-device.md]] (Nov 4) [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]].

At the [[wiki/meetings/2026-11-04-mvp1-transactional-release-definition-and-pilot-watch.md|Nov-4 MVP 1 release meeting]] (he was not present) Val named him the release manager, reporting to Irina — "Релиз менеджер у нас подчиняется Ирине… Толкнуть Ивана на релиз" — whose job is the Claude-written release notes, the compliance and exception reports and moving the capabilities to Closed [[raw/Meeting_Transcript_MVP1_Transactional_Release_Definition_and_Pilot_Watch-November-4-2026.md]] [[raw/Meeting_Notes_MVP1_Transactional_Release_Definition_and_Pilot_Watch-November-4-2026.md]]. This confirms, for the transactional release, the release-manager role he was given in the GitHub pipeline in Oct 2025 (above) — **evolution**. The commitment is tracked on [[wiki/decisions/2026-11-04-a-release-is-done-only-when-the-cleaned-build-is-on-the-production-server-under-a-number-ivan-is-release-manager-with-claude-written-release-notes-and-an-exception-report-and-request-review-leaves-the-feature-workflow.md]].

## Nov 5 2026 — the Georgia field bug reproduced: handpay pending raises SAS exception 51, the host never sends 94 or 1B, so the signature cannot be computed; only that case is confirmed to block counting; "we already have five separate meetings"

At the [[wiki/meetings/2026-11-05-daily-standup-new-engine-capabilities-and-georgia-handpay-tilts.md|Nov-5 stand-up]] (Russian; label "Ivan Shpak"; hard to hear at first): "повторили бак и с Ириной. То, что они в полях, скорее всего, получают то, что у них лонгпол 51… нету ответа он не снимается. И поэтому нельзя сигнатуру снять… Это должен хост слать либо 94, либо. Один б, чтобы снялся… escon 51 и тогда не будет этих ошибок. Не знаю, как это донести до интермота [heard]"; the entry point is a tilt dialog's Collect — "цеполог, к примеру, перегрелся" (CPU overheat, reproduced with Irina); forbidding Collect by setup would remove it on the V-deck too ("она на ведейке тоже пропадёт"); on checksums: "единственное, что проверено это если хэндпэй пендинг идёт у нас 51 эксепшн, то она не даёт посчитать. Во всех остальных случаях… оно давал… посчитать. Я пока не берусь делать утверждение"; to Chudinov's "separate meeting": "У нас уже 5 отдельных митингов на это на всё" — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Nov 5), [[wiki/organizations/intralot.md]] (Nov 5) [[raw/Meeting_Transcript_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]] [[raw/Meeting_Notes_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]]. This closes his Nov-4 "cannot reproduce the field case yet" — reproduced (**evolution**); the fix went to a separate meeting with Kharetski and Irina. His opening "я отвечаю вал" (heard) is **unclear**. He was not at the scope review; the MVP 1 release he is to manage is now planned for Monday — [[wiki/decisions/2026-11-05-mvp-1-is-planned-for-monday-november-9-internally-and-the-client-is-told-wednesday-and-the-pyramid-bill-acceptor-is-tested-remotely-on-an-echo-cabinet-in-georgia.md]].

## Nov 6 2026 — RIS and CMS review with Kharetski goes on; today he checks that the RIS is saved when Georgia machines run different software ("critical", never verified); Kharetski wrote that exception 51 is fixed, so he rebuilds his own machine to verify it, not the vertical one that carries the port

At the [[wiki/meetings/2026-11-06-daily-standup-modem-off-confirmation-capability-and-cap-287-in-mvp2.md|Nov-6 stand-up]] (Russian; label "Ivan Shpak") [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]: "Рис ц м с дальше смотрю то, что вот с Женей мы работаем всё ещё дальше, досматриваем. Я постараюсь сегодня, наверное, сразу же глянуть… если были разные у нас? Софты в пределах там ну джорджии раньше у нас рис не сохранялся и потом чтото сделал вроде должно сохраняться, но я до сих пор не проверил. Я проверю, потому что это критично. Женя мне ещё написал, что лонгпол 51, точнее esco 1 он тоже починил… проверю на своей же здесь этой машине просто пересоберу. Просто что не буду вертикально свою трогать, потому что там порт стоит" [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]] — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Nov 6), [[wiki/decisions/2026-11-05-a-tilt-is-a-tilt-collect-comes-off-critical-tilt-dialogs-exception-51-stops-when-the-dialog-closes-and-the-fix-ships-free-to-eclipse-november-16.md]] (the Nov-5 ruling he was not at; its commitment annotated). "Великолепно наконецто на стран тухри" (heard) at his opening is **unclear**. The Nov-4 "one more bug after Kharetski's fix" and the SAS tool were not mentioned.

### Open commitments (Nov 6 2026)

- [ ] [[wiki/people/ivan.md|Ivan]] — verify that the RIS is saved when Georgia machines run different software (the earlier fix was never checked) — due Nov 6 2026 — [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]
- [ ] [[wiki/people/ivan.md|Ivan]] — rebuild his own machine and verify Kharetski's exception-51 fix — due Nov 6 2026 — [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]

## Nov 9 2026 — GLI answers with Kharetski (one item likely to Metelski on the framework side); built with Kharetski's RIS-improvements changes and will check the delivered machine; the Nov 5–6 tasks; Andrei and the Git deletions

At the [[wiki/meetings/2026-11-09-daily-standup-due-date-rule-in-standard-and-update-dependency-map.md|Nov-9 stand-up]] (Russian; "Ван") [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]: "с Женей по[] джелай тут смотрели отвечали… Скорее всего к Игорю будет… со стороны фреймборка"; "Собрал бионс с изменениями жени по рискам проуменс от поставленную машину тоже посмотрю" — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Nov 9); Pavel: "эти вот задачи, которые там 5 6 ноября чтото с меня сделать" (whose tasks is unclear); at the end: "Там ещё Андрея надо попросить… в гите не удалялись" (Bosik by the Git context — **inference**) [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].

### Open commitments (Nov 9 2026)

- [ ] [[wiki/people/ivan.md|Ivan]] — check the delivered machine with the RIS-improvements build — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]

## Nov 10 2026 — waits for Metelski's GLI game fixes, then rebuilds and checks with Kharetski's changes and the modem work; tickets print empty when the machine boots — a fix from Pavel expected tomorrow

At the [[wiki/meetings/2026-11-10-daily-standup-flex-iq-single-screen-install-failure-and-mvp2-release-november-20.md|Nov-10 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]: "дождусь, ты игр поправят ещё раз пересоберу, посмотрю… жениной есть свои изменения… когда сделают этот автодемодем"; "от паши надо исправление, потому что у нас… [tickets] стали почему то пустыми печататься на подъёме машины… наверное завтра" — tracked on [[wiki/people/pavel.md]] (Nov 10) [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]].

## Nov 11 2026 — nothing new

At the [[wiki/meetings/2026-11-11-daily-standup-flex-pay-to-mvp3-and-sound-names-in-lua-scripts.md|Nov-11 stand-up]] (Russian; label "Ivan Shpak"): "Я сам с дотой занимаюсь [heard]… у меня ничего нового" [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]].

## Nov 11 2026 (8:31 AM) — called in as release manager: his release notes show 37 capabilities, 36 closed; build names go in the header; the Flex-Port label; he offers to shorten the text and is told not to

At the [[wiki/meetings/2026-11-11-mvp1-release-procedure-release-notes-and-product-sign-off.md|Nov-11 MVP 1 release meeting]] (Russian, label "Ivan Shpak"): "всего там 37 закрыто 36… Я досмотрю"; he puts the build names "в шапке" of the release notes; the port shows only "вы один" (heard) where the Flex IQ shows "206"; today he updates the release notes, and after Klimovich's green light moves all capabilities to Closed and releases the version in Jira — [[wiki/decisions/2026-11-11-mvp-1-is-released-after-klimovichs-go-no-go-on-the-release-notes-then-capabilities-close-and-the-jira-version-is-released-and-closed-capabilities-are-never-reopened.md]] [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

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
- [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Transactional_Release_Definition_and_Pilot_Watch-November-4-2026.md]]
- [[raw/Meeting_Notes_MVP1_Transactional_Release_Definition_and_Pilot_Watch-November-4-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]
- [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]
