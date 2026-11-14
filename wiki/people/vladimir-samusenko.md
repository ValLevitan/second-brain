---
type: person
title: Vladimir Samusenko
date: 2026-02-04
aliases: [Vladimir Samusenko, Vladimir, Vlad, Владимир, Самусенко]
source-count: 68
open-commitments: 17
open-questions: 1
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

## Sept 7 2026 — his prose skills and plugin become the tool for reverse-engineering Flex-Port

At the [[wiki/meetings/2026-09-07-sas-aft-on-flex-port-and-remote-update.md|Sept 7 10:02 engineers' alignment]] (Russian), accepting Val's process chain, [[wiki/people/pavel.md|Pavel Frolov]] named what he would use to apply it to code that already exists: "мне надо будет сделать реверс[-]инжиниринг… на готовый код… то, что уже есть в[о] Флекс[-]Порт[е]… с тем, что Владимир делает — скиллы и плагин для создания прозы," producing retrospectively a list of the capabilities that relate to Flex-Port [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]

Vladimir was not on the call. This is the first recorded use of his Sept-3 deliverable on a different team's codebase — see [[wiki/decisions/2026-09-03-prose-standard-into-knowledge-repository.md]] and [[wiki/decisions/2026-09-07-andrei-bosik-drives-the-wi-fi-work-and-the-process-chain.md]].

## Sept 11 2026 — tidying the Flex-IQ screens

At the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept-11 8:04 AM call]], arguing that the split-payout work is not a bottleneck, [[wiki/people/pavel.md|Pavel Frolov]] said the back end is done and so is the front end — "[В]ладимир сейчас причесывает все экраны", Vladimir is tidying up all the screens now [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

*(Identified as Samusenko by context — he is the Minsk React developer who owns the machine/setup screens — not by surname in the source.)*

## Sept 21 2026 — named for the smaller Flex IQ screen pieces (by context)

On the [[wiki/meetings/2026-09-21-transactional-mvp1-flexport-and-iq-ux-design.md|Sept-21 8:02 AM call]], Pavel suggested "По IQ, я думаю, что Владимир может", and Chudinov settled the split: he takes the main flow and "он уже посмотрит какиенибудь кисички" — the smaller pieces [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. *(No surname is spoken; this page is chosen because he is the only Vladimir in the corpus and tidied the Flex-IQ screens on Sept 11. Inference, queued.)*

## Sept 22 2026 (4:48 AM stand-up) — the Flex-Port contracts, and the Flex-Port screen redraw

At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]:

- **Contracts.** He worked on the Flex-Port contracts; the tool chosen is rendered "синкапе" (unclear). He lacks the expertise to verify it himself and will send a pull request to Pavel. He raised that Daniil had no access to the knowledge repository, and that two parallel efforts gave two results. See [[wiki/decisions/2026-09-04-data-contracts-closed-every-repository-by-september-11.md]] and [[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]] (Sept-22 updates) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **The screen redraw is his.** He objected to design delivered as an HTML page rather than Figma with design tokens — as a rule for the future — and accepted the job: "Окей скидывай я стал я буду заниматься". See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 22) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

## Open commitments (Sept 22 2026)

- [ ] Vladimir Samusenko — install TouchGFX Designer, pull the Flex-Port project, import it and report what can be worked with — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [x] Vladimir Samusenko — review his Flex-Port contract tests once more and send the pull request to Pavel — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]] — **overtaken Sept 23 2026:** Pavel had not looked at it and has no time today or tomorrow, so Vladimir merges it himself (see Sept 23 below) — [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]


## Sept 23 2026 — he merges the contract documentation without Pavel's review

At the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]:

- **Board GUI.** He is doing "ревор гуи для борта" — probably the rework of the board GUI he took on Sept 22 (**inference**; the notes say "review").
- **The contract.** He asked if Pavel had looked at it. Pavel: no time "сегодня, завтра". Vladimir: "это не сборку не поломает эта документация, я тогда мержу, а потом разберёмся." Pavel agreed; mistakes get fixed in a later commit.
- He also created feature "Фпорт 52", with Pavel telling him to add stories under it himself if needed.

## Open commitments (Sept 23 2026)

- [ ] Vladimir Samusenko — merge the board GUI contract documentation without waiting for Pavel's review — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]


## Sept 23 2026 (8:00 AM, in absentia, by inference) — the Flex-Port UI/UX capability

On the [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept-23 8:00 AM MVP 1 call]], Chudinov asked Pavel to put the Flex-Port UI/UX capability (235) "на Владимира", and the screen-rework feature already on him under 180 moves to 235. Only "Владимир" is said; that it is Vladimir Samusenko is an **inference** from his Sept-22 screen redraw. See [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]] (Sept-23 8:00 AM update) [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

## Sept 24 2026 — the Flex-Port design task closes, and the missing screens become new tasks

At the [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|Sept-24 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]], he said the Flex-Port idle screen, element positions, buttons and shortcuts are updated and can go to testing; pixel-for-pixel is not possible now. Screens with no implementation become new tasks, which Pavel said are **not MVP 1**. He will close the task, open the pull request and log the missing screens. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 24).

## Open commitments (Sept 24 2026)

- [ ] Vladimir Samusenko — close the Flex-Port design task, open the pull request, and log tasks for the screens with no implementation — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]] — *Sept 25: the missing screens already have tasks under capability 156; closing and the pull request not yet reported* [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]

## Sept 25 2026 — the missing screens all have tasks, and an engineering menu to sketch

At the [[wiki/meetings/2026-09-25-daily-standup-engineering-menu-and-jira-discipline.md|Sept-25 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]:

- **Screens.** He finished the Flex-Port fixes. Every missing screen already has a task under capability 156; the collector and claim screens wait for Flex-Port tasks 14, 15, 63 and 64. All his commits go into the "порт 9" branch, so the tasks ship together. This covers the "log the missing screens" part of his Sept-24 commitment below (the tasks exist); closing the design task and the pull request are not reported yet.
- **Out of work soon.** He expected to finish "в течение… часа полутора" and then need new work. Pavel asked him to sketch an engineering menu for technicians in TouchGFX. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 25).
- **An artifact for Pavel.** He will send Pavel the artifact describing all this, for Pavel's Claude or to read.

## Open commitments (Sept 25 2026)

- [ ] Vladimir Samusenko — sketch an engineering menu (network, last transactions, recent errors) for discussion — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]
- [ ] Vladimir Samusenko — send Pavel the artifact describing the missing screens and their tasks — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]

## Sept 28 2026 — the service menu goes under capability 235, then autotests

- **At the 4:56 AM stand-up** ([[wiki/meetings/2026-09-28-daily-standup-log-traffic-and-nova-rename.md|Sept-28 Minsk stand-up]], Russian): he is building the Flex-Port service menu and found no capability for it. Pavel will add a requirement under capability 235 for diagnostic screens; Vladimir agreed ("Давай так"). He and Irina will agree after the meeting when he can help with autotests [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]].
- **At the 8:02 AM call** ([[wiki/meetings/2026-09-28-transactional-mvp1-remote-updates-and-october-15-target.md|Sept-28 8:02 AM MVP 1 call]]; in absentia): Irina said he finishes his design implementation work and joins the autotests "со среды" for about 8 days, then goes on leave [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].

## Sept 29 2026 — port tasks done; he starts on the autotests with TINT-41

At the [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|Sept-29 Minsk stand-up]] (Russian; speaker label): "С задачами по порту закончил. Сейчас смотрю, что происходит с автостерами." He confirmed with Pavel that the autotests "живут в интеграционном репозитории", requested access — [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] granted it during the stand-up ("Владимиру я доступа дал уже на репетитории тинты") — and will start with "тинт 41 задачу. Она самая понятная, на мой взгляд." This overtakes the Sept-28 plan to settle his start with Irina. See [[wiki/topics/test-automation-strategy.md]] (Sept 29) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]. *(Whether the Flex-Port design task was closed and its pull request opened — his Sept-24 commitment — is not said; "с задачами по порту закончил" suggests so, but is not read as discharge.)*

## Open commitments (Sept 29 2026)

- [x] Vladimir Samusenko — start on the autotests with TINT-41 in the integration repository — due started Sept 29 2026 — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]] — **discharged Sept 30 2026:** "Я сделал этот 41 задачу" — written, about three defects filed; the task goes to Blocked — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]

## Sept 29 2026 (8:06 AM, in absentia) — "he started working today"

On the [[wiki/meetings/2026-09-29-transactional-mvp1-setup-instructions-and-mikrotik-router.md|Sept-29 8:06 AM MVP 1 call]] (Russian; he was not present) Irina reported: "мы подтянули Владимира, он начал работать уже сегодня… он уже там вник[ает]… [н]ачинает писать, ну будут ещё с его стороны вопросы" — a day earlier than the "со среды" of Sept 28; consistent with his own stand-up report above. Matched to this page by context (autotests) [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]. See [[wiki/topics/test-automation-strategy.md]] (Sept 29, 8:06 AM).

## Sept 30 2026 — task 41 done as far as the defects allow; it goes to Blocked; the next task is the one closest to ready

At the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]:

- **What he did.** "Я сделал этот 41 задачу с [экспайдная примешен]" ("expired permission" is a reading); "[з]авёл… по результатам выполнения там 3 или сколькото дефектов и несколько задач на… доработку". He linked the blocking tasks and left a comment.
- **His question.** "фактически я её не закончил, потому что… не могу сделать для всех сценариев сейчас"; and the unfinished autotest branch — "через пару дней мне начнут писать эти письма о том, что… у вас там бранч висит". "Как поступать с такими задачами?"
- **The answer.** Pavel: Blocked, raised at the next meeting; next, the task "более в готовом состоянии" (he thinks "один 48"), with dates moved; Irina: any unassigned task on Ivan or Khamin can be taken. His readiness measure: some tasks "из 10 4 сценария я не могу пройти", others "из 18 2 сценария я могу пройти". "Тогда окей, будем считать с этим закончил и возьму следующий." See [[wiki/decisions/2026-09-30-an-autotest-task-that-cannot-finish-goes-to-blocked-not-closed.md]] and [[wiki/topics/test-automation-strategy.md]] (Sept 30, 4:57 AM).

## Open commitments (Sept 30 2026)

- [ ] Vladimir Samusenko — set task 41 to Blocked with the defects linked, raise it at the next meeting, and pick the next autotest task closest to ready (probably 148), moving its dates — due Sept 30 2026 — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]] — *Oct 1 2026: "Сегодня ещё прошёлся по 7 41 задачи со своим уже портом и [эмулятором SAS]. Один [блокер] снимался, доделал" — a blocker lifted and the task worked further; whether it is in Blocked, and which task he took next, is not said* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]

## Oct 1 2026 — TINT-40 finished, task 41 worked again with his own port and the SAS emulator, and his Epic-printer change in the shared library

At the [[wiki/meetings/2026-10-01-daily-standup-sas-mode-flag-and-feature-status-rules.md|Oct-1 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]:

- **Status.** "[тинт] 40. Вчера закончил" (read as TINT-40). "Сегодня ещё прошёлся по 7 41 задачи со своим уже портом и [эмулятором SAS]. Один [блокер] снимался, доделал и чего я там активно ещё закинул 34 лакейшн блок тейкс" (the last phrase garbled; the derived notes read "a location task" [[raw/Meeting_Notes_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]). "Задачей занимаюсь сейчас." See [[wiki/topics/test-automation-strategy.md]] (Oct 1, 4:48 AM).
- **The printer library.** Pavel: the new ticket type that stopped the e-wallet ticket printing on FlexPay was his — "это Владимир Владимир делал, но он, наверное, делал только для этого. Для 950, да для эпика"; Vladimir: "Для эпика" — the Epic 950 printer. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 1, 4:48 AM).
- **The story under FP-85.** Tsymanov's discipline email was about a story Vladimir created under Tsymanov's already-closed feature "фпорт 85"; Irina: "когда Владимир писал, нашлось что[-то]" — the autotest found something. The ruling it led to is on [[wiki/decisions/2026-10-01-completed-is-the-developers-last-step-and-a-found-problem-sends-the-feature-from-completed-back-to-to-do-as-a-story.md]]. He did not speak in that argument.

## Oct 2 2026 — reviewing Khamin's work and finishing task 34, "I am not in the context" of the stories he creates, the Claude plugin's repository, and the three stories Tsymanov took

At the [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]:

- **Status.** "занимаюсь тем, что ревью лёша. Доделываю. 34 34 задачу с этой блокировками. Сейчас там не все сценарии проходят, я до разберусь с этим. Отмечу, что нужно. Какие задачи на это влияют и буду брать что то следующее" (Khamin's review; task 34 — the derived notes read "task 34 (blocks)" [[raw/Meeting_Notes_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]).
- **His question.** "у меня есть к [стори — unclear], который я завожу. Я вчера попытался в них вникать, и это ну, типа относительно меня тормозит, потому что я не в контексте происходящего… просто заводить и вы разбирайтесь там правильно, это неправильно… у меня много сил времени и калорий занимает разобраться, куда там порт должен слать, куда не должен слать. Какие [capabilities]? Он должен выполнять? Я не абсолютно не представляю… Этот вопрос только в моей эффективности и скорости." Pavel: talk it through with Irina or Khamin first; "Если… 23 там 5 тасков. Кажется, что все понятно. Ну тогда уже можно будет и самому." — "Окей." See [[wiki/topics/test-automation-strategy.md]] (Oct 2).
- **The plugin.** On Chudinov's Claude-found issues: "[плагин] есть репозитория, которая там подключаешь и если в плагине есть баги заводите [issue] к этому репозиторию… Да просто скажи ему, он сходи в репу, заведи её на всем доступно… сейчас скину, окей?" (the prose skills of Sept 1–3 above by context — inference). See [[wiki/topics/ai-assisted-development.md]] (Oct 2).
- **The three stories.** Tsymanov fixed "3 истории от Владимира" that reopened his feature; Vladimir: "я их не назначал на исполнителя, ты их сам себе забрал." See the Oct-1 decision (Oct-2 update).
- In the weekend round he answered "Не знаю, давай после [—] последим… Думаю. Потом." Irina asked him, Khamin and Ivan to mark their done items in Jira. His Sept-30 commitment above (task 41 in Blocked; the next task) is not resolved by this.

## Open commitments (Oct 2 2026)

- [ ] Vladimir Samusenko — finish task 34 (the blocks), work out why not all scenarios pass, note which tasks affect it, then take the next task; talk through the stories he creates with Irina or Khamin first — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [ ] Vladimir Samusenko — send Chudinov the Claude plugin repository's link in the chat, for filing issues — due Oct 2 2026 ("сейчас скину") — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]

## Oct 5 2026 — task 769, screens and texts

At the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]: "Занимаюсь это тестами сейчас 7 69. Там задача с проверкой экранов и текстов. Там задача будет на меня [подработки — unclear] сравнивать правильно. Ну и там всё в принципе." Task 34, task 41 and the stories under Tsymanov's feature were not mentioned; Tsymanov named "Владимира" in a garbled line about a task of his. His commitments above stand. See [[wiki/topics/test-automation-strategy.md]] (Oct 5).

## Oct 6 2026 — test 69, missing texts, and built work without requirements

At the [[wiki/meetings/2026-10-06-daily-standup-ris-georgia-branch-and-critical-error-text.md|Oct-6 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]:

- Text gaps are easy; missing design and translations are the problem. For test 69 he will add the missing texts himself and open a ticket for "Andrei" to approve. He will list built items that lack requirements for a review session — [[wiki/decisions/2026-10-06-built-capabilities-without-requirements-get-a-review-session-and-the-developer-adds-missing-texts-for-andrei-to-approve.md]].
- He asked Seregin to look at FQ-112 and Pavel at PORT-91, which blocks his task 34. Pavel moved his FIT-127 to the backlog.

## Oct 7 2026 — tasks 40 and 41 rerun on a fresh Flexport

At the [[wiki/meetings/2026-10-07-daily-standup-test-coverage-first-and-ai-task-numbers.md|Oct-7 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]: he rechecked tasks "41, 40" where the blockers were removed; installed Flexport that morning; will rerun everything and log defects if they are confirmed, then look for other tasks freed from blockers or take something new. See [[wiki/topics/test-automation-strategy.md]] (Oct 7).

### Open commitments (Oct 7 2026)

- [ ] Vladimir Samusenko — rerun tasks 40 and 41 on Flexport and log defects if confirmed — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]

## Oct 8 2026 — task 62 and a requirement contradiction; the lease regulation; two scenarios

At the [[wiki/meetings/2026-10-08-daily-standup-lease-expiry-scenarios-and-flex-signal-quality.md|Oct-8 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]: he is on task 62, where he found a small contradiction in the requirements; blocked tasks and 42 are moving, others had requirement problems partly resolved the day before — [[wiki/topics/test-automation-strategy.md]] (Oct 8). On leases he summarised the regulation: expired lease → out of service with the reason; revoked lease → out of service without a reason; per Claude, the code does this. He proposed two scenarios: lease expired (any cause) and terminal unlinked from the location — [[wiki/decisions/2026-09-11-lease-blocking-reaches-the-flex-ports-and-is-never-automatic.md]] (Oct-8 update).

### Open commitments (Oct 8 2026)

- [ ] Vladimir Samusenko — clear task 62 and the blocked tasks as the requirements are fixed — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]

## Oct 9 2026 — autotests 42, 23 and 62 closed; 73 and the version stub; TIN-56 needs the cloud; 769 and the 33 screens

At the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 stand-up]]: closed 42, 23 and 62; 21 to Khamin for review; 73 unclear (the Payment Hub link); an emulator version stub he may add himself; then 30, 60 and 70. TIN-56 needs the cloud — "дай бог, если половину теста". On 769: requirement 1813 has 33 screens in the design, "Как будто бы надо 32" — [[wiki/topics/test-automation-strategy.md]] (Oct 9) and [[wiki/decisions/2026-10-09-tests-to-october-15-follow-80-20-and-port-machine-and-iq-tests-come-before-cloud-tests.md]] [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].

## Oct 12 2026 — his commit linked an unrelated task; blocked tasks reviewed today

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 stand-up]]: his commit text named port task 118 though the work was for TIN-30, so Jira moved 118 to In Progress; "нельзя указывать задачи, не относящиеся к… тому, куда ты комидишь" — [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]] (Oct-12 update). One autotest a day to the 15th; he reviews all blocked tasks today — [[wiki/topics/test-automation-strategy.md]] (Oct 12) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].

## Oct 13 2026 — fixing Irina's changes; why GUI port tasks 122 and 52 are on him

At the [[wiki/meetings/2026-10-13-daily-standup-video-decode-memory-and-release-task-type.md|Oct-13 stand-up]]: he is still on the unblocked tasks and adding tests; he asked why GUI port tasks 122 and 52 were put on him, and Irina said to pass them on if wrong — [[wiki/topics/test-automation-strategy.md]] (Oct 13) [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]].

## Oct 14 2026 — autotests to Done; "one-line requirements work badly"

At the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 stand-up]] part of his autotests moved to Done; 31 waits on requirement numbers, 71 and 72 on the port; he argued that one-line requirements lack criteria — [[wiki/topics/test-automation-strategy.md]] (Oct 14) [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

## Oct 15 2026 — TIN 32 closed; 71 and 72 out of Blocked; questions on 33

At the [[wiki/meetings/2026-10-15-daily-standup-offline-ris-fallback-and-nova-game-conversion.md|Oct-15 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]: TIN 32 closed; 71 and 72 out of Blocked with the port fixes; 27 waits for review; 33 has questions on how the terminal and port reach the network, for Pavel. Then 57, 63 and 56; Pavel: at least remove the October 15 date — [[wiki/topics/test-automation-strategy.md]] (Oct 15).

## Oct 15 2026 (11:04 AM, in absentia) — away for at least two weeks

At the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian) Pavel: for at least the next two weeks "Владимир самусенко в отпуск" — an availability fact for MVP 2 planning — [[wiki/decisions/2026-10-15-mvp2-is-flex-iq-wi-fi-remote-update-diagnostics-and-galaxy-reporting-and-flex-pay-moves-to-mvp3.md]] [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Oct 16 2026 — Galaxy autotests; a modem that comes back only after a reboot; tasks with no parent

At the [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct-16 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] he closed Galaxy autotests 71 and 72, has 71 and 31 waiting for a hardware run and a PR on 33, with 57 and 63 next, maybe over the weekend — [[wiki/topics/test-automation-strategy.md]] (Oct 16). His backlog story — the modem does not come up after a connection-priority change until a reboot — Pavel says must be fixed — [[wiki/decisions/2026-10-16-the-flex-iq-commit-that-sets-the-modem-mac-at-boot-is-rolled-back-and-the-shared-mac-stays.md]]. He proposed allowing Jira tasks with no parent — [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-16 update).

*Availability note.* On Oct 15 (11:04 AM) Pavel said "Владимир самусенко в отпуск" for at least the next two weeks [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]; on Oct 16 he attended and planned weekend work [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]. When his vacation starts is **unclear**.

## Oct 21 2026 (in absentia) — invited to be product owner of the new NOVA

At the [[wiki/meetings/2026-10-21-dutch-mill-on-nova-and-native-engine.md|Oct-21 Dutch Mill review]] Val named him "самый лучший кандидатура" for product owner of the new NOVA — a thinking owner who writes no code on it, modelled on Andrei Klimovich. Pavel thought him a better candidate than Khamin; Irina said he came into recent work carefully and then quite actively. He is back from a short vacation on Monday Oct 26; Pavel writes the role description and meets him then, and grooming of the MVP1 capabilities starts Tuesday Oct 27. Val wants him given a written persona of the role and support so he does not fail — [[wiki/decisions/2026-10-21-vladimir-samusenko-is-invited-as-nova-product-owner-and-capabilities-are-drafted-one-file-per-person-before-grooming.md]] [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].

## Oct 22 2026 (in absentia, inference) — two LGS set-up-screen tasks

At the [[wiki/meetings/2026-10-22-daily-standup-flex-port-cashout-screens-and-native-engine.md|Oct-22 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] Pavel said a "Владимир" (this Vladimir, by his set-up-screen role — **inference**) had moved two LGS set-up-screen tasks (LGS-1040 and LGS-1042, as heard) to him because the LGS side was not built; Irina unlinked them from their closed parent — [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-22 update).

## Oct 27–28 2026 — port bugs closed; the modem retest is green

At the [[wiki/meetings/2026-10-27-daily-standup-cashout-merging-and-remote-updates.md|Oct-27 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]] he closed port bugs 136, 37 and 34 (heard) and planned to retest them with the modem in one run. At the [[wiki/meetings/2026-10-28-daily-standup-flex-port-firmware-delivery-and-reopening-completed-features.md|Oct-28 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] the port fixes were done and the modem test green; two IQ text tasks wait on a text library that does not exist — [[wiki/topics/test-automation-strategy.md]] (Oct 27, Oct 28).

## Oct 29 2026 — backlog review; a text-id for autotests; the new-engine requirements page

At the [[wiki/meetings/2026-10-29-daily-standup-cash-out-progress-screen-and-pulse-mode-installs.md|Oct-29 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]] he said he is going through backlog tasks ("127 142", heard). One low-priority item: a data text-id for autotests, so tests compare by a key library rather than by text, to avoid failures on duplicates. Pavel asked Leshkevich to send him the one-page new-engine requirements list to read — [[wiki/decisions/2026-10-21-nova-drops-the-browser-for-a-native-engine-no-code-before-capabilities-and-mvp1-is-a-stable-nova-releasing-six-texas-games.md]] (Oct-29 stand-up note).

## Oct 29 2026 (10:32 AM, in absentia) — interested in trying the product-owner role

At the [[wiki/meetings/2026-10-29-minsk-team-reorganization-and-staffing-review.md|Oct-29 10:32 AM call with Val and Irina]] (Russian) [[raw/Meeting_Transcript_Minsk_Team_Reorganization_and_Staffing_Review-October-29-2026.md]] Pavel said the old front-end role is no longer needed, so they try people in other directions. Vladimir was tried in autotests, where he showed perhaps the best results of all. Pavel had talked with him about taking on product-owner duties; "он заинтересовался" — he wants to try ([[raw/Meeting_Notes_Minsk_Team_Reorganization_and_Staffing_Review-October-29-2026.md]]: "agreed to try a product owner role") — [[wiki/decisions/2026-10-21-vladimir-samusenko-is-invited-as-nova-product-owner-and-capabilities-are-drafted-one-file-per-person-before-grooming.md]] (Oct-29 note).

## Nov 2 2026 — tests fixed after Andrei's answers; "202" filed from the updated test library

At the [[wiki/meetings/2026-11-02-daily-standup-flex-port-release-build-and-rust-sound-library.md|Nov-2 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]: he filed "202" purely on the tests, after "Андрей прислал обновленную библиотеку тестов"; it is closed [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]. After Andrei's answers on the requirements some were corrected; he pulled the tests that need small fixes — "5 или 6 тестов" Andrei commented on — and will finish and commit that day; Irina will check his in-progress list against her weekend runs [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]. "Андрей" here is the requirements author, read as [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] as on Oct 30 (**inference**). He proposed moving the stand-up to 3:00 PM [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]].

## Nov 3 2026 — port tasks 142 and 193; Flex-Port can be merged; NOVA 2 onboarding begins

At the [[wiki/meetings/2026-11-03-daily-standup-sim-traffic-alert-and-flex-iq-release-action.md|Nov-3 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]: port task "142" done after Andrei's comments; Andrei added the texts for the task on adding text — not super urgent; port task "193" done but not committed — "Мейн жду разрешения… влевать мэйн"; Pavel: Flex-Port can be merged now ("Эфпорт можно уже вливать?… Угу"); the test goes in too — "лёша уже посмотрел, уже опробовал" [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]. Next: "перехожу к бурдингу нованова 2" (heard; the notes: NOVA 2 onboarding) — he has pulled out the meetings and correspondence and is assembling them "в какуюто единую картину" [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] — [[wiki/decisions/2026-10-21-vladimir-samusenko-is-invited-as-nova-product-owner-and-capabilities-are-drafted-one-file-per-person-before-grooming.md]] (Nov-3 note).

### Open commitments (Nov 3 2026)

- [ ] [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] — merge port task 193 (and its test) into Flex-Port main, then start the NOVA 2 onboarding — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]

## Nov 4 2026 — on the autotests; LGS documentation drafts; access to the service repositories

At the [[wiki/meetings/2026-11-04-daily-standup-release-build-handoff-and-nad2-product-code.md|Nov-4 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]: "мне уже насовали тентов" — he takes autotests; part of the documentation work he spoke of — "документацию в л д с" (heard; LGS by context — **inference**) — is drafted; he now has access to the service repositories ("принтера… интеграшенной репозиторию") and reads their documentation to build the full picture, as time allows; when the draft is final he will publish or agree it; "Пока занимаюсь тентами" [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]. Pavel then noted the MVP 2 acceptance criteria are probably unreviewed, which matters for the autotests — [[wiki/decisions/2026-10-15-mvp2-is-flex-iq-wi-fi-remote-update-diagnostics-and-galaxy-reporting-and-flex-pay-moves-to-mvp3.md]] (Nov-4 update) [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]. The NOVA 2 onboarding he began on Nov 3 was not mentioned.

## Nov 5 2026 — back on the autotests; nearly all open ones need the cloud services (portal, terminal hub); his per-scenario service document shared in the chat; autotests for features not yet written; a fourth meeting wanted, "not a priority"

At the [[wiki/meetings/2026-11-05-daily-standup-new-engine-capabilities-and-georgia-handpay-tilts.md|Nov-5 stand-up]] (Russian): "Меня перекинули на forteste [autotests] написание очередной раз начал их разбирать и втыкаюсь в то, что… всем практически, за исключением трёх или 4 задач, которые сейчас в колонке тоду висят в принципе нужны… Облачные сервисы, работа с ними. С порталом с термином алхабом [terminal hub]"; he talked to several people yesterday about a meeting on how and when that will be ready; "я собрал в один документ… скину сейчас в чат этот артефакт, где… по сервисам по сценариям расписано там для какого сценария, какой сервис нам может понадобится? Какой сервис, что должен отдавать, что должен уметь принимать"; and a second question — autotest tasks whose features are not created or closed, where the test cannot yet be written (his example: where and how a port's disconnection from the master is recorded "Мы этого не знаем"); Irina: the feature must say how; he: "вопрос творческий где то можно где то нет"; he wants "4 митинг с с обсуждением облачных сервисов и контуротстового [the test contour]"; Pavel: maybe tomorrow morning; Irina: not a priority — [[wiki/topics/test-automation-strategy.md]] (Nov 5) [[raw/Meeting_Transcript_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]] [[raw/Meeting_Notes_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]].

## Nov 6 2026 — TIN-105 and TIN-111 (heard); the Wi-Fi tests cannot run because machine 84 carries the MVP 1 build; waiting for word on the cloud services and taking no other tasks; "almost all" MVP 2 autotests need them; invited to the 4:00 NOVA remote-update meeting

At the [[wiki/meetings/2026-11-06-daily-standup-modem-off-confirmation-capability-and-cap-287-in-mvp2.md|Nov-6 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]: "Я вытащил работу тин 105 тин 111" (heard; the notes: TIN-105, TIN-111); "по 111 там есть часть тестов, связанная с вайфаем на IQ. Я понимаю, тот билд, который сейчас стоит на 84 машине. В нём работа с вайфаем ещё нет"; "Пока жду. Какойто информацией, планов по поводу. А облачных сервисов для тестирования. Остальные задачи в работу пока не беру"; Irina: which cloud services does MVP 2 need for the Flex IQ and Flex-Port — "Почти все"; on the Wi-Fi: "Оно оно в комичено да, но сколько я понял разговора с Алексеем вчера на face IQ сейчас стоит билл из MBP один, и он тестируется… когда закончится тестирование м п один можно будет прогонять тест и смотреть, что происходит уже по м и п 2"; Pavel: "у нас там сегодня в 04:00 будет тебя туда позвать по поводу обсуждения обновлений, удалённых для. Онова" — [[wiki/topics/test-automation-strategy.md]] (Nov 6), [[wiki/decisions/2026-11-05-mvp-2-is-kept-narrow-wi-fi-with-the-flex-iq-as-access-point-or-client-remote-flex-port-update-robust-installation-and-install-diagnostics-due-november-20-and-the-rest-goes-to-mvp-3-around-january-20.md]] (Nov-6 note), [[wiki/decisions/2026-10-30-nova-remote-update-is-nova-only-and-texas-first-and-the-full-architecture-is-written-before-the-mvp-split.md]] (Nov-6 note). This continues his Nov-5 "nearly all open autotests need the cloud services"; the fourth meeting he wanted is still not scheduled in the sources.

### Open commitments (Nov 6 2026)

- [ ] (blocked-on: MVP2-build-on-the-test-IQ) [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] — run the TIN-111 Wi-Fi tests once the MVP 2 build is on the test Flex IQ and the cloud services are known — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]

## Nov 9 2026 — TINT-115 (heard) near its end; the TINT-111 Wi-Fi access-point test waits for the firmware; which Flex-Ports have Wi-Fi; TINT-101/102 back to him; his LGS capabilities draft

At the [[wiki/meetings/2026-11-09-daily-standup-due-date-rule-in-standard-and-update-dependency-map.md|Nov-9 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]: TINT-115 (heard "тотарствами 115") needs a test API at the final stage; TINT-111 and the Wi-Fi module ports — [[wiki/decisions/2026-11-05-mvp-2-is-kept-narrow-wi-fi-with-the-flex-iq-as-access-point-or-client-remote-flex-port-update-robust-installation-and-install-diagnostics-due-november-20-and-the-rest-goes-to-mvp-3-around-january-20.md]] (Nov-9 note); "Так какие порты с вайфаем подскажешь?" — Pavel could not recall the numbers; TINT-101/102 — [[wiki/topics/test-automation-strategy.md]] (Nov 9); "доделал черновик ка[па]бил[ити] для LGS. Пересмотрю глазами и потом… заводить их джира буду" — in which status and on whom, to discuss at the next meeting [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].

### Open commitments (Nov 9 2026)

- [ ] [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] — review his LGS capabilities draft and enter it in Jira — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]

### Open questions (Nov 9 2026)

- Which Flex-Ports have the Wi-Fi module (Pavel recalled one in his room and one "у вас", numbers unknown)? — [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]

## Nov 10 2026 — TINT-105 took long: its security items go to the future, not MVP 1 or MVP 2; a new capability 370 with Irina for several terminals and a master

At the [[wiki/meetings/2026-11-10-daily-standup-flex-iq-single-screen-install-failure-and-mvp2-release-november-20.md|Nov-10 stand-up]] (Russian) — [[wiki/decisions/2026-11-05-mvp-2-is-kept-narrow-wi-fi-with-the-flex-iq-as-access-point-or-client-remote-flex-port-update-robust-installation-and-install-diagnostics-due-november-20-and-the-rest-goes-to-mvp-3-around-january-20.md]] (Nov-10 note); [[wiki/topics/test-automation-strategy.md]] (Nov 10); "Часто заканчиваю 7 105 и дальше надо ковыряться" [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]].

## Nov 11 2026 — test 105 waits for a free run; 111 and maybe 114 next on a Wi-Fi terminal (machine 82)

At the [[wiki/meetings/2026-11-11-daily-standup-flex-pay-to-mvp3-and-sound-names-in-lua-scripts.md|Nov-11 stand-up]] (Russian) — [[wiki/topics/test-automation-strategy.md]] (Nov 11; the commitment is tracked there) [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]].

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

- [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]
- [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-1.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-4.md]]
- [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
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
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]]
- [[raw/Meeting_Transcript_Minsk_Team_Reorganization_and_Staffing_Review-October-29-2026.md]]
- [[raw/Meeting_Notes_Minsk_Team_Reorganization_and_Staffing_Review-October-29-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]
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
