---
type: person
title: Vladimir Samusenko
date: 2026-02-04
aliases: [Vladimir Samusenko, Vladimir, Vlad, Владимир, Самусенко]
source-count: 9
open-commitments: 4
---

# Vladimir Samusenko

Vladimir Samusenko is a **new React developer** on JVL's Minsk front-end team, who as of early February 2026 **owns the machine setup screens**. (Name transcription — surname supplied by Pavel as "Самусенко" — is uncertain; Tier-B queued for owner confirmation.)

## New setup-screen developer (Feb 4 2026)

- On the [[wiki/meetings/2026-02-04-figma-react-export-workflow.md|Feb-4 figma→React session]] [[wiki/people/irina-shishko.md|Irina Shishko]] introduced him as "the new one who deals with the setup" — JVL **moved [[wiki/people/anton-seregin.md|Anton Seregin]] off setup**, so Seregin now acts as a **consultant over setup** rather than its main developer, and Samusenko is the primary developer. He works **in React** (confirmed by [[wiki/people/pavel.md|Pavel]]). [[wiki/people/val-levitan.md|Val]] said he would invite Vladimir to the Friday figma→React working session ("уже пригласил" — already invited). [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]

## Feb 6 2026 — confirmed front-end developer on the LGS repo

On the [[wiki/meetings/2026-02-06-ui-claude-code-adaptation.md|Feb-6 UI/Claude-Code session]] Vladimir attended and was the **"unnamed front-end developer"** Aaron's Claude analysis initially found in the commit history — he identified himself ("I think it's me"). His commits were characterised as **front-end work** (login/denomination/printed-ticket screens, battery-health, refactoring, improving front-end architecture) — corroborating his React front-end role on the setup screens. [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]

## Feb 11 2026 — front-end developer; repo to be Waze-converted next

On the [[wiki/meetings/2026-02-11-github-front-end-waze-setup.md|Feb-11 GitHub front-end Waze setup]] Val had Pavel introduce Vladimir; Pavel corrected the framing that he is a replacement for "Igor" — **"Igor is a UI/UX designer, but Vladimir is mostly a front-end developer"** (the "Igor" being [[wiki/people/ihar-hrybko.md|Ihar Hrybko]] by role, UX/UI). Aaron asked him to speak in his own language (Russian). He works on the setup screens / "local games" (transferring the old setup design to a new Figma-based design). Aaron told him "this process equally applies to the repos that you will be working in too," and the agreed next step is for Vladimir to **convert his own repo to the Waze system the same way**, opening a pull request in a branch that Anton, Pavel and Aaron review together. [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-1.md]] [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md]] [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-4.md]]

## Aug 24 2026 — the frontend prose experiment: 29 capabilities and a cross-validation proof

On the [[wiki/meetings/2026-08-24-nova-lgs-prose-standard-checkpoint.md|Aug-24 prose checkpoint]] (Russian) Vladimir reported the front-end half of the code→prose→capability experiment. Method detail on [[wiki/topics/ai-assisted-development.md]] (Aug-24); the ruling is [[wiki/decisions/2026-08-24-single-prose-writing-standard.md]]. [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

- **His method.** He instructed Claude to describe the code "фактически то как он есть. Не пытаясь чтото исправлять или додумывать," in language a person would understand and without technical terms, and he wrote the prose **per screen** rather than per file because "в моём случае файлы не самодостаточные, не описывают картину." He tuned the output on one small example first, then ran the whole project; several passes were needed to get Claude writing correctly without him. He did not read every line — the file runs to close to **2,000 lines**. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **The proof he devised.** The LGS codebase holds an old implementation and a new one doing the same thing, "но описан категорически поразному," one written **ten years ago**. He required the capabilities recovered from the prose to be identical in both cases; they were — "Что я таким способом подтвердил жизнеспособность такого способа." **He got 29 capabilities out of the experiment.** [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **He disagreed with Val on needing to feed the architecture first.** Val reported that prose from code alone had failed for him and [[wiki/people/andrey-bosik.md|Andrei Bosik]], and that supplying the product architecture first worked; Vladimir's answer was that Claude "уже знает и понимает" the overall architecture from the project context, and that what he supplied was scope. He noted JVL's ADRs and product architecture are not complete, but he can explain the architecture or answer Claude's questions, and "здесь архитектура не сказать, что сложная." [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **He treated Claude's suspected defects as questions, not bugs** — "Я не стал однозначно считать дефект дефектом, когда он указывает" — because with that much context Claude can simply miss something; the answers either enrich the capability or lead to a fix. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **He deliberately has not committed his prose next to the code yet**, "потому что пока я не подтвердил у вас у нас, пока мы не решили, как мы делаем" — his and Evgeny's work would conflict until the approach is agreed. He built on the prose Val had sent to [[wiki/people/dmitri-chudinov.md|Dima Chudinov]], using it as the basis for his own. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **He raised the overlap problem** between his front-end capability set and Evgeny's back-end set — "сейчас они будут не пересекаться, а конфликтовать" — which the meeting settled as two prose documents and **one** capability set, merged after the standard exists. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- He accepted Val's point that once new code is added to written prose, the changed part of the prose must always be read. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Sept 3 2026 — he delivered the standard and two Claude Code skills, and took Val's sharpest correction of the month

At the [[wiki/meetings/2026-09-03-nova-prose-standard-skills-and-module-contracts.md|Sept-3 follow-up]] (Russian) Vladimir presented the work. Method detail on [[wiki/topics/ai-assisted-development.md]] (Sept-3); the repository mechanics on [[wiki/topics/github-release-management-pipeline.md]] (Sept-3). [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

- **He authored the single prose standard** from the meetings, the discussions, and the work he, Zhenya ([[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]]) and Anton had done, plus prose already written — "из всего этого собрал стандарт[,] который бы устраивал всему тому, что мы обсуждали, что мы находили и что делали." This discharges the authoring half of the [[wiki/decisions/2026-08-24-single-prose-writing-standard.md|Aug-24 commitment]]. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He had put it in the LGS repository, and Val objected in the strongest terms** — LGS "пока как пилотный проект для прозы… На нём проводились большинство экспериментов," which Val rejected as a reason: a standard has exactly one location. Vladimir agreed to move it, subject to write access he probably does not have. See [[wiki/decisions/2026-09-03-prose-standard-into-knowledge-repository.md]]. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He built two Claude Code skills, which he called the most valuable output** — "самое ценное, считаю[,] сделано 2. Скилла для клауд код": one that initialises prose for a project that never had any (studying the repository's dependency tree, proposing the prose unit, asking clarifying questions, writing a reviewable index/mapping document that also stores the conversation context), and one called simply "prose" that handles ongoing change. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He named the update path as the hardest problem** — "над одной прозой могут работать… 2 разработчика… Вот этот процесс самый сложный" — and solved it by never writing prose directly: change artifacts go into a `pending` folder and a GitHub action merges them on merge to main, failing loudly rather than losing text. His statement of the underlying risk: "основная проблема проза[—] то, что мы можем чего то не написать и потом никогда не узнаем, что его там не было." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **Results he reported:** LGS fully documented and its prose already in main; the skills also tested successfully on the Recycler; **54 capabilities** generated for LGS and **34** for the Recycler; and on the Recycler branch, linking prose to existing capabilities gave "покрытие… процентов 80[–]95," verified on several capabilities with an "Alexander" (which Alexander is not stated). [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He agreed with "Андрей" the previous day that the skills move into the Claude Code configuration** once he finishes, so all developers share one version and receive updates. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- Val closed the meeting thanking him first: "Владимир, большое спасибо." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Open commitments (Aug 24 – Sept 3 2026)

- [x] With [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]]: agree and author one prose-writing standard — due Aug 25–26 2026 — **done: reported written at the Sept-3 follow-up ("из всего этого собрал стандарт"), late against the planned date** — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]] [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [ ] Move the prose standard out of the LGS repository into the `knowledge` repository's standards folder — due promptly (Sept-3); blocked on write access — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [ ] Move the prose skills into the Claude Code configuration so every developer shares one version and receives updates — due on finishing (Sept-3) — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [ ] With Evgeny: run Claude over the existing prose to normalize it to the new standard — due after the standard is placed — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [ ] With Evgeny: merge the overlapping backend and frontend capability sets into one after the standard is set — due unspecified — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Sources

- [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]
- [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-1.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-4.md]]
- [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
