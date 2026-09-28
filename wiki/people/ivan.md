---
type: person
title: Ivan
date: 2025-02-19
aliases: [Ivan, Ivan Shpakov, Иван Шпаков, Ivan Shpak, Ваня]
source-count: 8
---

# Ivan

Ivan handles JVL's **release scheduling and certification paperwork** — the release-manager role Val wants driving proactive coordination with GLI. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Role

- On the Feb 19 alignment call, Val told Pavel to "put Ivan on it" to **start scheduling with GLI ahead of time** (GLI needs scheduling, JVL has PO-signing to do), and stressed the "looping" discipline — repeatedly checking back that the scheduled work is actually happening. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- Ivan sends the paperwork to GLI; Val noted costs can be kept low by detailing exactly what changed so GLI doesn't retest untouched code — the **release notes** (generated from Jira stories, with ChatGPT wording that must be checked) plus Irina's separate **diffs document**. See [[wiki/projects/georgia-market-rollout.md]] and [[wiki/projects/south-dakota-vlt-market.md]]. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

**Surname (Oct 22 2025):** in the Calle Ocho practice-release session Val named the release-manager Ivan as **"Иван Шпаков" (Ivan Shpakov)** — same release/build-marking role, so recorded as this Ivan's transcribed surname. [[raw/practice_release_calle_ocho-github-october-21-2025.md]] (Distinct from any "Ivan" greeted in the Puerto Rico contacts — see Owner Decisions.)

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

## Sources

- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- [[raw/andrei _klimovich_update-apr-15-2025.md]]
- [[raw/sas_51_52_requirement_interpretation-april-14-2025.md]]
- [[raw/releases_github-october-21-2025.md]]
- [[raw/artifacts_assembly_GitHub-october-21-2025.md]]
- [[raw/practice_release_calle_ocho-github-october-21-2025.md]]
- [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
