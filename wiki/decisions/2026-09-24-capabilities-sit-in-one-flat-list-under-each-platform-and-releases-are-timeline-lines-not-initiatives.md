---
type: decision
title: Capabilities sit in one flat list under each platform, views come from filters, and releases are Jira timeline lines — not initiatives
date: 2026-09-24
aliases: [one long list of capabilities, flat capability list, releases are vertical lines, no release-named initiatives, Core value stream, Core and Tools rename, Galaxy Platform, remove the product IP layer, Games Core Hardware value streams, IP-1204 Core, IP-738 Tools, IP-481 NOVA Gaming Platform Land-based, IP-1199 IP-1202 MVP split]
source-count: 2
status: active
open-commitments: 4
open-questions: 2
---

# Capabilities sit in one flat list under each platform; releases are timeline lines, not initiatives

Taken by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-24-nova-galaxy-jira-hierarchy-cleanup.md|Sept 24 2026 10:00 AM "NOVA and GALAXY state of affairs" call]] (held in **Russian**), after a long debate with [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], [[wiki/people/alexander-biratka.md|Alexander Biratka]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] and [[wiki/people/andrey-bosik.md|Andrey Bosik]] [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]. It applies the [[wiki/topics/github-release-management-pipeline.md|June-16 hierarchy standard]] (Value Stream → Initiative → Capability; Project = repository) to NOVA and Galaxy, which were still filed the old way.

## The starting state

- **NOVA work sat under the old layout.** Pavel: the tasks sit under **IP 90 Applications**, in the initiative **IP 481** "NOVA Gaming Platform Land-based" — "Она сейчас организована, да неправильно" [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].
- **No Galaxy work at all.** Pavel: "ни обсуждений, ни работы, ни репозиториев, ничего" [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].
- **Projects already match repositories.** Kovalchuk: "отношение один к одному все репозитории соответствуют проектам в жире". Jira also has older extra projects; Val: they will be closed and fade away [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].
- **The transactional team had split MVPs by initiative.** Irina: the day before they made **IP 1202** beside **IP 1199**, to separate the two releases, so they could see that "1 закончится 1 октября, а 2 закончит с 29 октября". Pavel: this was done "вчера" [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].

## The debate

- **Val first wanted the architecture in the hierarchy.** Under the NOVA platform he wanted the platform's logical parts — LGS, math, framework — so it is clear where a change lands ("здесь затрагивается только математика") [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].
- **Chudinov objected.** Most work crosses repositories: "Я почти уверен, что 90% работ идут взаимодействие. Более одного репозитория." Scrolling by repository is awkward; on the cloud servers there will be close to 20. He liked grouping by planned release, as in MVP 1 [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].
- **Pavel's worry was copies and length.** If each part (LGS, math, a game) is its own initiative, the same capability must be copied into each. His only gain from splitting would be not having about 100 capabilities in one list [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].
- **Kovalchuk's point.** Every task is already created in its own project, so a project is already a grouping; a capability is an abstract view on top [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].

## What was decided

- **One long, flat list of capabilities under the platform. Views come from filters.** Val: "Один большой список типа белотис, которыми работаешь работаешь." … "Ты закрываешь?" — then filter by release date, MVP, status, assignee or project. Pavel: "Ну хорошо, я думаю, что это в принципе всех устраивает такой подход." Biratka: then only capabilities sit under the platform, nothing else [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].
- **A release is not part of the hierarchy.** Val: "релиз это не часть хайяры хаяраки." He is "категорически против" the release-named initiatives made the day before. Releases are "вертикальные вот эти линии" on the timeline. Kovalchuk: one can filter by release, pick MVP 1 and see only MVP 1. Pavel showed a release filter on screen; Val: "Это мне нравится" [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].
- **Every project must carry the same release, and features must be tagged.** Pavel: the same release has to exist in every project; capabilities are already marked with releases, features are not [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].
- **The top value stream is Core; the old "Core" becomes Tools.** Val: "Этот вал ее стрим должен называться кор" with the NOVA platform and Galaxy under it, and "IP 481 должен идти под 738". Pavel: IP 738 "Корпус [Core] это совсем не то… вспомогательные инструменты". Val: "Просто просто назовите их тул тогда". Pavel: "Давайте." … "Назовем это кор." *(Which Jira item finally carries the name Core is not clear from the transcript; the notes read it as IP 1204 = Core and IP 738 = Tools — an inference.)* [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]] [[raw/Meeting_Notes_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
- **Transactional: one initiative, products seen through filters.** Val disliked the current initiative name. Pavel: it holds FlexPort and FlexPay, not only Flex IQ, and splitting by product forces the same capability into two or three IPs. Val: "Тогда я предлагаю оставить только транзакцию" with the capabilities under it; FlexPort has its own repository, so it is a project filter [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].
- **Remove the product IP layer.** FlexPort, IQ, Dispenser and similar are already repositories, so they should not also be IPs. Old features under them move to existing or new capabilities, and the IPs close. Pavel, Chudinov and Kovalchuk said "Да" to IQ and Dispenser being their own repositories. Val: "клад код с этим очень справится" (Claude Code can do much of it) [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].
- **Three top-level value streams are clear to Val: "Геймс кор и харвар"** (Games, Core, Hardware). The game production / design / concept IPs are parked [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].

**Chudinov's reservation.** "Давайте сначала сделаем, а потом посмотрим" — he wants to see how the filters work when moving a capability from one MVP to another [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].

**Val's framing of a value stream.** "Стрим всегда рассматривалась как или. Профицентр или экспенцентр" — viewed like accounts, by how much money is spent there. This matches the June-16 standard's "accounting line" [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]].

## Relation to earlier rulings

- It carries forward the [[wiki/decisions/2026-09-10-per-product-components-and-mvp-fix-versions-on-the-capability-project.md|Sept-10 per-product components and MVP fix versions]]: the release (= fix version) is the MVP marker, not an initiative. See the Sept-24 update there.
- It keeps [[wiki/decisions/2025-04-07-recarve-gaming-platform-into-six-product-repos.md|the 2025 "repository = product" rule]]; IP481 is still the NOVA/gaming platform initiative, now to move under Core.

## Open commitments

- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — groom Jira: remove the product IP layer, attach its features to existing or new capabilities (with Claude), then create the releases (MVP 1, MVP 2) as timeline lines; say by Tuesday how long it will take ("Давайте во вторник") — due Tuesday (Sept 29 2026 by calendar — inference) — [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
- [ ] [[wiki/people/alexander-biratka.md|Alexander Biratka]] — move all NOVA features under the right capabilities; create missing capabilities and link requirements — due "за завтра за утром" (Sept 25 2026, morning) — [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] and [[wiki/people/alexander-biratka.md|Alexander Biratka]] — move their own capabilities themselves, so Pavel does not act as secretary — due Sept 25 2026, morning — [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
- [ ] Attendees — tag the features they work on with the release, so release filters work in every project (Pavel's proposal: "давайте дадим задание всем присутствующим свои фичи"; no explicit assignment followed) — due unspecified — [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]

## Open questions

- **Galaxy: its own platform under Core, or one platform with NOVA?** Val wants "Transactional Galaxy" renamed Galaxy Platform and IP 1095 under Core. Chudinov: server and machine capabilities belong together — either all under Galaxy or all under NOVA. Pavel: the transactional server and the NOVA server barely overlap ("слабы между собой пересекаются"). Not settled — [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
- **Where do games and game design live** — under IP 90 or a Games value stream? Irina asked; Val parked it ("я бы это запарковал бы") — [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]

**§15.8:** clear — Jira structure and process only. **§15 #9:** IP numbers are Jira work references, not corporate identifiers.

## Sources
- [[raw/Meeting_Notes_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
