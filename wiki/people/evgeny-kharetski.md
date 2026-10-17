---
type: person
title: Evgeny Kharetski
date: 2025-07-10
aliases: [Evgeny Kharetski, Evgeny Kharetsky, Evgeny Khoretsky, Kharevsky, Yauheni Kharetski, Kharetsky, Koretski, Koretsky, Korecki, Khorvatsky, Корецкий, Хорватский, Халецкий]
source-count: 51
open-commitments: 12
disambiguation: "LGS developer (payroll "Kharetski Yauheni"), this page. Evgeny/Zhenya cluster — EXHAUSTIVE at THREE per owner (2026-07-20; Zhenya = Evgeniy = Evgeny = Eugine, one name): [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] = FlexPort/FlexPay integration software (alias Egorsky); [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] = embedded code + hardware-adjacent work (boards/redesigns/electronics, esp. Genadi Peari's projects); [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] = LGS/Omni backend (payroll "Kharetski Yauheni"; garble-aliases Koretski/Khorvatsky). Resolve by context: FlexPort/FlexPay integration software → Yavorski; embedded/hardware-adjacent & Genadi's projects → Alekseev; LGS/Omni backend → Kharetski. NO fourth Zhenya exists — a mention fitting none clearly is a mis-heard non-Zhenya (cf. Ethan/Efim), so treat as garble/mishearing and queue; NEVER create a new Zhenya."
---

# Evgeny Kharetski

Evgeny Kharetski is a **Minsk Omni/LGS game developer** on JVL's engineering team. His name is transcribed many ways (Kharetsky, Khoretsky, Kharevsky); the [[wiki/topics/minsk-staff-roster.md|Minsk staff roster]] resolves him to the canonical **Yauheni Kharetski**.

He is a distinct third person from the two other "Zhenya" contractors ([[wiki/people/eugine-yavorski.md|Yavorski]], [[wiki/people/evgeniy-alekseev.md|Alekseev]]) — the three-member split is **owner-confirmed (2026-07-19)**. He appears across the Omni schedule reviews as a game developer on game-history/LGS work (see [[wiki/topics/omni-core-advancement-and-game-templating.md]]).

## What is known

- **Test-automation infrastructure (July 10 2025).** In the [[wiki/meetings/2025-07-10-autotests-sync.md|autotests sync]] he drove the test-environment configuration plan: build configurable JSON objects/sectors, provide the JSON structure to [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] (who builds the JSON builders), and provide an endpoint for submitting RIS; he argued for proper unified tooling from the start rather than an incremental approach. [[raw/autotests_sync_meeting.md]]

## Feb 3–4 2026 — Claude Code rollout (participant + PR-review example)

- **Feb 3.** He attended the [[wiki/meetings/2026-02-03-claude-code-integration-continued.md|Claude Code integration workshop]] as one of the Minsk engineers being onboarded (Aaron's "AI sandwich" teaching + the live LGS-monorepo run). [[raw/Claude Code integration - continued.md]]
- **Feb 4.** Val cited Kharetski (garbled "Корецкий"/"хорватским"/"Халецкий" — §4 registry) as the reviewer in a demonstrated **Claude-Code PR-review loop**: [[wiki/people/ihar-hrybko.md|Hrybko]] opened a pull request to main; Kharetski got the signal from the hub, opened the PR, ran his **local Claude Code**, committed the resulting comments, and Hrybko then made the file commit to master. See [[wiki/topics/test-automation-strategy.md]] (Feb-4). [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]

## Feb 6 2026 — back-end owner of the LGS repo

On the [[wiki/meetings/2026-02-06-ui-claude-code-adaptation.md|Feb-6 UI/Claude-Code session]] Evgeny **shared his screen** to walk Aaron through the LGS repo's README/docs, and was identified as the **back-end (Java) owner** on the repo (Aaron's Claude analysis: "Evgeny is the Java developer"). This is consistent with his LGS/Omni back-end role. See [[wiki/topics/ai-assisted-development.md]] (Feb 6). [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]

## Feb 11 2026 — ways-versioning question (via Pavel)

On the [[wiki/meetings/2026-02-11-github-front-end-waze-setup.md|Feb-11 front-end Waze session]] (Kharetski **not present**), Pavel relayed his question (garbled "Evgeniy Kereski"): he had tried to build his own way to validate logs on a remote machine and upload the updated version, and asked why the team should always pull the latest ways from GitHub rather than each project committing its own ways. [[wiki/people/aaron.md|Aaron]]'s answer: Kharetski doesn't have the latest Waze, and it already does that — there is a **local per-project Waze** as well as user scope. Val asked to set up a **separate ~15-minute meeting** with Kharetski (garbled "Haletsky"/"Haritsky"). Consistent with his LGS/back-end + interest-in-the-tooling role. See [[wiki/topics/ai-assisted-development.md]] (Feb-11). [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-4.md]]

- **The follow-up happened the same afternoon (3:20 PM).** The dedicated ~11m49s session Val asked for took place with Kharetski **present** ([[wiki/meetings/2026-02-11-github-ways-repository-structure.md]], with Aaron and Pavel): Aaron answered the where-do-ways-live question — a `.claude` directory in each repo root for project scope, a `.claude` in home for user scope, Waze reading both — and explained the macro component of a way and the JVL synced-ways-repo plan. Kharetski was largely quiet (mostly acknowledgements) with Pavel driving the discussion. See [[wiki/topics/ai-assisted-development.md]] (Feb-11 GitHub-ways follow-up). [[raw/GitHub_Ways-February-11-2026.md]]

## Mar 18 2026 — named as a Ways trusted-stage-user candidate

On the [[wiki/meetings/2026-03-18-setting-up-jvl-ways-on-github.md|Mar-18 JVL-Ways-on-GitHub session]] (Kharetski **not present**; Aaron/Val/Andrei Bosik) [[wiki/people/aaron.md|Aaron]] said the Ways pipeline's **stage** layer needs trusted users who understand Ways and write code with Claude Code daily. After Aaron rejected [[wiki/people/dmitri-kovalchuk.md|Dima]] as a candidate, [[wiki/people/val-levitan.md|Val]] named **Kharetski** — "Haretsky is very good — let's deploy him." Consistent with his back-end-developer + interest-in-the-tooling role (cf. his Feb-11 ways-versioning question). See [[wiki/topics/ai-assisted-development.md]] (Mar-18). [[raw/Setting up JVL ways on GitHub-March-18-2026.md]]

## Mar 26 2026 — owns the setup-mode freeze fix

On the [[wiki/meetings/2026-03-26-initiative-priority-schedule.md|Initiative Priority Schedule]] meeting (referred to as "Женя"/Zhenya from the developers, not clearly present) Evgeny Kharetski is named to take the **setup-mode kernel-crash "freeze" fix** — starting on the South Dakota task first, then moving to the next market. (Resolved to Kharetski per §4: LGS/Omni-backend "Zhenya" → Kharetski; the folded meeting-notes name him "Evgeniy Kharetski" explicitly.) See [[wiki/topics/github-release-management-pipeline.md]] (Mar-26). [[raw/Meeting_Transcript_initiative_priority_schedule-2-March-26-2026.md]] [[raw/Meeting_Notes_initiative_priority_schedule-March-26-2026.md]]

## Aug 2026 — AI-adoption exemplar; the ~80% migration estimate

- **Aug 3 2026** (RAGE→NOVA experiment sync): after seeing Igor's conversion result, Evgeny said it was a big surprise how much easier it was than expected and estimated ~**80%** of games could migrate with little pain. See [[wiki/topics/nova-platform-architecture.md]] (Aug-3). [[raw/Meeting_Transcript_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]
- **Aug 6 2026** (Val→Genadi, about Evgeny): Val held up "**Khoretsky** in Minsk" as the model of an engineer who embraces the AI tooling — he now runs ~**10 agents** across **3 projects** and is asking for a **second computer** — contrasting him with reliable people who won't adopt the new way of working. (A performance/adoption observation, not compensation.) See [[wiki/topics/ai-assisted-development.md]] (Aug-6). [[raw/Meeting_Transcript_AI_Engineering_Workflow_and_Hardware_CxO-August-6-2026.md]]
- **Aug 18 2026** (RAGE→NOVA experiment review): Evgeny helped settle the **math-container packaging** (build from a game list at the integration-build step — [[wiki/decisions/2026-08-18-nova-math-container-per-game-set.md]]) and raised the main **risk against Val's NOVA timeline**: significant LGS-side work remains — **SAS has not yet run on NOVA**, **multiprogressive** needs porting, and the **NOVA platform-service repo has diverged ~six months** from the old RAGE center repo. See [[wiki/topics/nova-platform-architecture.md]] (Aug-18). [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]] [[raw/Meeting_Notes_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]

## Aug 24 2026 — the LGS prose result, ~26 modules, 30-plus bugs found, and the missing-standard call

On the [[wiki/meetings/2026-08-24-nova-lgs-prose-standard-checkpoint.md|Aug-24 prose checkpoint]] (Russian) Evgeny reported on running the code→prose→capability method across the LGS back end. Method detail on [[wiki/topics/ai-assisted-development.md]] (Aug-24); the ruling is [[wiki/decisions/2026-08-24-single-prose-writing-standard.md]]. [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

- **Result: "в целом у меня… Вышло неплохо."** He treated it as a repeatable **cycle over ~26 modules** — first agree a rule set and a document shape with Claude, after which "один модой, 2 модуль, 3 модель ничем друг от друга не отличались." He had completed roughly **10 modules** with **16 left**, at one to two per day. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **He named the gap that produced the standard.** JVL has a capabilities standard and a prose-lives-next-to-code rule, but "нету… Единого какогото стандарта, как мы пишем прозу и как мы пишемка били" — no standard for the prose document itself: whether technical detail belongs in it, what structure it takes, and how capabilities are extracted from it consistently. He counted three-to-five incompatible variants in the wild and proposed distilling one, then running Claude over the existing prose to normalize it. He volunteered to convene the standard meeting the next day. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **He is skeptical prose is strictly necessary.** "у меня есть ощущение, что поберите можно и без прозы вывести. Чистые скода" — capabilities could be derived straight from code. Val did not dispute feasibility but ruled it out: "может быть это можно, но я не хочу это делать." Evgeny also noted prose compresses hard: a ~10,000-line module reduces to a few general sentences. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **The bug harvest.** Claude "нашел достаточно большое количество багов" while writing the prose; rather than stopping, "мы их просто записывали прямо в эти же документы." As of the previous Friday there were "гдето 30 с чемто… подозрения" across modules. His plan: extract them all afterwards and fix them in separate, minimal-context sessions. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **He is the one who insisted on automation.** "80% из написания кода будет забыто обновление прозы" without it, and he proposed a per-repository prose folder plus a rule that fails a PR carrying code without an updated prose folder — while admitting "я не уверен… что такие ролса можно делать на репозит проведение." [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **His prose is already committed inside the LGS repository** ("прям прям в репозитории л JS они там лежат то, что я сделал"), unlike Vladimir's. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Aug 28 2026 — the performance read on the Dragon Pays port, and the "relative layout" objection

Val invited him to the [[wiki/meetings/2026-08-28-dragon-pays-nova-conversion-review.md|Aug-28 Dragon Pays review]] on the [[wiki/meetings/2026-08-26-alignment-planning-nova-september-releases.md|Aug-26 alignment call]] two days earlier, alongside [[wiki/people/igor-metelski.md|Igor Metelski]] — transcribed there as "Хорецки". [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

- **He supplied the only independent performance read of the port.** Having watched Igor's screen directly rather than through the meeting stream, he reported "Все очень плавно на винде" — everything very smooth on Windows — and that the screen-share showed only "процентов 30 от плавности." The one exception: "под лаги были на какомто бигвине, где очень, очень много монеток. А Так в принципе стабильная 60 кадров." [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- **He sided with Pavel against pixel-level acceptance criteria.** When Val argued that frame-by-frame behaviour must be expressible in requirements and acceptance criteria because the code expresses it, Evgeny answered "Нет, нет" and offered the alternative framing: "Может быть относительная какаято верстка" — perhaps a relative layout rather than absolute positions. See [[wiki/topics/test-automation-strategy.md]] (Aug-28). [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- **He is one of the three names in Val's knowledge-spread rationale** for porting a second game in parallel: "У нас тогда будет хорецкие метельские вишкевич" — Kharetski, Metelski and [[wiki/people/anton-leshkevich.md|Leshkevich]] would all carry the Rage→NOVA conversion knowledge. See [[wiki/decisions/2026-08-28-reverse-engineer-acceptance-criteria-and-automate-qa-dragon-pays.md]]. [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]

## Sept 3 2026 — he asked what prose is *for*, then found the two gaps that block automated testing

At the [[wiki/meetings/2026-09-03-nova-prose-standard-skills-and-module-contracts.md|Sept-3 follow-up]] (Russian) Evgeny made the two most consequential interventions of the call. Val's closing thanks named him: "Евгений[,] хороший [input]." [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]] [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

- **He challenged the purpose of prose outright.** Reverse-engineering to derive capabilities is fine, but "написали код по этим [капабилити] и прозу к этому коду? И что мы дальше[?]… зачем она нужна?… сейчас это выглядит просто, как будто она ну лежит, чтобы она там лежала и всё." He wanted the payoff discussed — "Это там помощь в автотестах, например" — before the team committed. When Val answered that end-to-end tests are the first and most important reason, Evgeny: "если бы вы это не сказали, сказал бы я." See [[wiki/decisions/2026-09-03-acceptance-criteria-settled-by-experiment.md]]. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He relocated the difficulty from the test to the harness.** "Написать тест не проблема… Кусок работы это новый тестовый [harness]," because so much is new — particularly the separate services — and a real run needs the LGS game plus a bill-validator service standing up together. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **Then he named the two blockers: no module contracts, and no NOVA machine-side integration repository.** "у нас контрактов… на взаимодействие нового валидатора… с [LGS]… нет"; "У нас нет интеграционного репозитория на новую платформу… на часть, которая устанавливается на машины… он есть на IQ." And the coupling: "интеграционный репозиторий без контрактов работать не будет." Val: "Это очень хороший поинт… это хорошо замечено. Спасибо." Full decision on [[wiki/decisions/2026-09-03-module-contracts-and-nova-integration-repository.md]]. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He took the LGS contracts himself** — "Скорее всего, этим буду заниматься я" — counting devices, the game, SAS, and external server / player control as the entry points, and noting LGS only relays math without processing it ("[LGS] является трансфером просто… транслирует данные, он никак не обрабатывает"). He also volunteered to lead populating the integration repository. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He was candid about his load.** "изза Того, что сейчас тут много работы. Я не уверен, что я сделаю всё, но я постараюсь… сделать максимум[,] там к следующей пятнице." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **He insisted the module links be technical files, not prose** — "какието более технические файлы типа джинсонок… Как вот ты объявляешь переменную в коде… потому что иначе Клод может… отойти [от] задуманного" — and Irina and Pavel accepted it. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **On adoption he took the mechanical view and Val overruled the framing.** Evgeny: developers "в любом случае будут подписаны. Это репозитория будет настроена так, что им нужно будет писать прозу"; Val: "людей не заставишь," and someone who refuses "просто… не вписывается в коллектив." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- He had been ill in the days before ("Я заболел просто"), which is why he had been absent. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Open commitments (Aug 24 – Sept 3 2026)

- [ ] With [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]]: run Claude over the existing prose to normalize it to the new standard and merge the overlapping backend/frontend capability sets into one — due after the standard is placed; **the standard-authoring half was delivered by Vladimir on Sept 3** — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]] [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [x] Finish prose and capabilities for the remaining ~16 LGS modules at one to two per day — due ~1–2 weeks from Aug 24 2026 — **done: at the Sept-3 follow-up Val asked whether LGS was fully documented and Vladimir answered "Да, на данный момент да"; the LGS prose is in main** — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]] [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [ ] Work out with "Andrei" (which Andrei is not stated) whether a repository rule can block a PR that changes code but carries no updated prose folder; test it on one repository first — due unspecified — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [ ] Write the LGS contracts — devices, the game, SAS, external server / player control — due aim end of the week of Sept 7 2026 — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [ ] Lead the populating of the NOVA machine-side integration repository (module-link JSON, contract references, Claude working rules), with everyone connected to the contracts committing — due the two-week milestone from Sept 3 2026 — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Sept 4 2026 — he forced the contracts question, and got a dated answer

At the [[wiki/meetings/2026-09-04-rage-nova-conversion-readiness.md|Sept-4 morning meeting]] Evgeny reopened the blocking point he had raised the previous day: the automated test pipeline "не будет работать без контрактов с каждой из сторон, которые задействованы на машине со стороны новой," and "мы не можем приступать к написанию авто[тестов пока это] не сделано" [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]] [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]].

- **He walked Val through what a contract is**, on the LGS example — entry and exit points, written as OpenAPI or similar, describing what each side emits and accepts, with the match between the two being what makes good autotests possible. [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He held his position that module linkage must be structured, not prose:** "это не должно быть проза[,] это должно быть… хардкодом структурированны[м]" — and answered Pavel's worry that a new linking standard would be needed with "у нас уже есть стандарт паш. У нас же интеграционный репозиторий работают на IQ." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **His versioning answer to Dzmitry Chudzinau:** all module and contract versions are baked at release and can be restored; and you release the whole product, not an individual module — "ты релизишь не отдельно модуль авторизации[,] ты релиз[ишь] продукт полностью." He conceded the machine's contracts with CMS and the account host are harder: "Он с этим сложнее, но я думаю, это решаемо." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He explained zero trust to Igor:** Igor's is an input contract, the two of them agree any change and each describes their own side, "тебе пофиг[,] кто тебе эти данные даст[,] элджис или какойнибудь другой сервис." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He flagged his own schedule risk and got 80% accepted.** "к пятнице я, возможно, не успею, потому что у меня самый большой кусок. У меня слишком много контрактов на один репозитор[ий]. Я постараюсь" — Val: "если будет 80% сделано хорошо, если 100 лучше." Ruling on [[wiki/decisions/2026-09-04-data-contracts-closed-every-repository-by-september-11.md]]. [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **A side disclosure:** he had privately tried porting **Calle Ocho** off Pixi onto **Godot** about a month earlier — "я просто сильно не заморачивался, но у меня что то получилось" — hitting scene-composition problems with misplaced buttons. See [[wiki/decisions/2026-09-04-browser-pixi-stack-concern-closed.md]]. [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **On human QA in the finished pipeline, he was the most absolute voice in the room:** asked whether any human validation survives, "Минимальную. Либо никакая, либо минимальная." Val agreed: "Желательно нет." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]

## Open commitments (Sept 4 2026)

- [ ] Place the data contracts beside the code in his repository, which carries the largest number of contracts — due Sept 11 2026 (80% acceptable; he warned he may not make it) — [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]

## Sept 9 2026 — named among the three Val asked to work more hours

At the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept-9 7:02 AM call]] [[wiki/people/val-levitan.md|Val]] asked about extra capacity from three people — "[с]колько люди сейчас работают[:] [Б]иратка, **[К]орецкий**, Хам[и]н[?] Их можно, чтоб они больше работали?" — and [[wiki/people/pavel.md|Pavel]] answered only for Biratka and Khamin; **nothing was said about him**, and the question is left unanswered in the source. [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

*(Resolution note: "Корецкий" is one of this page's recorded garble-aliases per the §4 owner-ruled registry. The context — a list of Minsk engineers Val can ask for more hours — fits and nothing in the source contradicts it, but he is named only in passing.)* **§15.8: hours only; no compensation.** [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

## Sept 14 2026 — he inherits the Flex-Port collect-timing problem after Pavel failed at it

At the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|Sept-14 8:01 AM transactional call]], Klimovich asked whether the money is genuinely gone from the machine the moment collect is confirmed and cannot come back within that operation. [[wiki/people/pavel.md|Pavel Frolov]] answered that they are working on exactly this, do not know whether it can behave differently, and that he had tried and failed — "я пробовал сделать, чтоб было по[-]другому[,] у меня не получилось. **Сейчас эту задачу отдал Жене Харецкому**" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]. The derived notes carry the same hand-over [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

This is his **first transactional / Flex-Port task in the corpus** — his recorded work to date is LGS/Omni backend and the RAGE→NOVA migration experiments. The task matters beyond its size: the whole ticket-recovery design on [[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]] exists because the money leaves the machine immediately, and it is his answer that would tell the team whether that premise is fixed.

*(§4 note: the transcript renders the name "женихарецкому" — "Жене Харецкому", the full surname, not a bare "Zhenya". No cluster resolution was needed.)*

## Open commitments (Sept 14 2026)

- [ ] Evgeny Kharetski — determine whether collect money can stay on the machine instead of moving to the Flex-Port the instant collect is confirmed; handed over by Pavel Frolov after his own attempt failed — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## Sept 22 2026 — a re-release, and the contract work

At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 stand-up]] (Russian), he said the team re-released the new version the day before ("перелиживали новую версию"), "Вроде пока тихо", so he is on the contract — under LGS-1185, as Pavel confirmed ("В рамках л джи с 11 85") [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].


## Sept 23 2026 — still on the contract

At the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]] (Russian), called on as "женя", he said he is working on the contract and needs to talk to Pavel about it in person — "сейчас приеду, поговорить надо". Which contract is not said (on Sept 22 it was under LGS-1185). [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]


## Sept 24 2026 (5:41 AM) — the store of every RIS, and "in principle yes"

At the [[wiki/meetings/2026-09-24-georgia-hard-reset-remedies-and-passport-removal.md|Sept-24 5:41 AM hard-reset review]] (Russian; called "Женя") [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]:

- **Passport switch-off.** Asked whether removing the passport check for the Georgia build is hard: "Но в целом да… Я уже говорю что в целом да." See [[wiki/decisions/2026-09-24-engineering-plans-to-switch-off-the-passport-check-for-georgia-builds.md]].
- **The hidden RIS history.** "у нас есть файл сторож, который мы храним. Все рисы, которые когдалибо были применены на машине" — a mechanism "мало кто знает"; the latest is picked by file number, not by time. The catch is progressives. See [[wiki/topics/ris-remote-install-and-machine-states.md]] (Sept 24).
- **He pushed on scope:** is the list "здесь и сейчас", or gathered "чтоб это всё обработать и сделать красиво в будущем"? He doubted the soft reset ("Слишком много ситуаций надо обработать"), raised the lost-money case, and said that with services a printer could be found and added to the payout order on the fly.

## Sept 24 2026 (10:00 AM, in absentia, by inference) — the integration-repository manifest

At the [[wiki/meetings/2026-09-24-nova-galaxy-jira-hierarchy-cleanup.md|Sept-24 10:00 AM NOVA/Galaxy call]], Pavel said "женя" will work on a task in the integration repository: a manifest that ties versions of different repositories into one build, ending in an artefact like an ISO. Read as this Zhenya by context — he leads the NOVA integration repository since Sept 3. **Inference.** Not present. [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]

## Sept 25 2026 — his queue: CI/CD, a regression repository, and a one-step build for non-technical staff

At the [[wiki/meetings/2026-09-25-daily-standup-engineering-menu-and-jira-discipline.md|Sept-25 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]:

- **Now.** Integration work and "Партнер сервис плюс"; he is waiting on a task he gave to an Anton, and moving commits across. Some words and his task number are garbled and are not interpreted.
- **Next, in order.** The same with the progressive controller; CI/CD for the progressive controller, then for "прото"; then a regression repository ("дегрессионный репозиторий", garbled); then a build that someone without technical knowledge — "например, художником" — can run in very simple steps, with games and progressives already chosen; then autotests.

## Sept 28 2026 — the move to LGS, nearly done

At the [[wiki/meetings/2026-09-28-daily-standup-log-traffic-and-nova-rename.md|Sept-28 Minsk stand-up]] (Russian; he answers to "женя") he said he worked through the weekend on a move to LGS ("С переносом… в LGS"; the object, "Дотацентра", is **unclear**). "Антон" — **not resolved** between the Antons — fixed gaps in the services for him. "Сейчас я закончу с переносом и буду [в]недр[ять] дальше сервисы." So the move is not fully finished [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]].

## Sept 29 2026 — the version table into main, the 4.50.2 fix, and "that network cannot be trusted for long connections"

At the [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|Sept-29 Minsk stand-up]] (Russian; speaker label; called on as "Женя") [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]:

- **The bug, and the table.** He is on a bug whose number he forgot. He "очень долго воевал" the day before because he had to rework the release ("Англия" — **unclear**): the table matching centre versions to the games they commit into "[п]ришлось переносить в мэйн" — triggered by Ivan's stand on 4.50.1 against the team's 4.60, since one game version cannot serve two data centres. Then a test started failing. "[С]ейчас я уже почти готов [с] [фиксом]". See [[wiki/topics/github-release-management-pipeline.md]] (Sept 29).
- **The re-release.** The fix can be checked on 4.60 now or "на 502" if re-released; the commit also changes a library ("Бракаст" — unclear), which he changed "[ч]тоб… править нормально и подстраховаться на будущее"; he will write to Ivan when the build is ready. See [[wiki/decisions/2026-09-29-the-fix-goes-out-as-a-re-release-not-a-hack-and-only-that-commit-goes-in.md]].
- **His main work.** "Л джес 212 19 и л джи с 12:17" (read as LGS-219 and LGS-217 — the notes' reading) plus new tasks on "росссервиса для сити толка" and its integration (**unclear**, not interpreted).
- **The modem.** He corrected Pavel on the progressive: it does not stop, "[о]н постоянно реконнектится"; "на эту сеть полагаться для каких то коммуникаций долгосрочных нельзя". See [[wiki/decisions/2026-09-17-lte-is-the-default-route-and-the-manual-override-stays.md]] (Sept-29 update).
- Pavel made him a cable: "я тебе кабель сделал" — "Ну супер шикарно."

## Open commitments (Sept 29 2026)

- [ ] Evgeny Kharetski — finish the fix, build 4.50.2 with that one commit, and write to Ivan when it is ready — due Sept 29 2026 — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]] — *Sept 30 2026: "я вчера закончил с этими с правками для джорджии"; whether that is this fix, and whether the build went to Ivan, is not said* — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]

## Sept 30 2026 — the Georgia fixes done, the queue fix that does not show, CC talk closed, and the LED service

At the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian; called on as "женя") [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]:

- **Georgia.** "я вчера закончил с этими с правками для джорджии". One thing is left: he needs logs ("[о]твалишелоги, я ему попросил" — garbled; from whom is unclear), because the queue fix Pavel asked for — "чтоб ты всегда последний был" — "почемуто визуально это не так", "хотя клод утверждал, что там и так он всегда последний"; he will look.
- **CC talk.** "[сиси] толк сделал да, но я чтото потерял задачу" — found with Pavel as "сети 58 58" (the notes: CT-5858), in the backlog — Pavel: "А потому что она в бэклогии?"; "я её сегодня тоже закрываю". ("сиси толк" / "сити толк" — the same unresolved item as Sept 29.)
- **Help.** "Дон много чего доделал по моим просьбам… все эти вот задачи… [н]у почти все" — "Дон" is **not resolved** (no such person on file).
- **Next.** "буду дальше интеграцией заниматься теперь вроде как всё готово для этого" — "лджес 20, 19. И 12, 17" (garbled; Sept 29 heard the same pair as LGS-219 / 217).
- **The LED service.** Pavel: "женя там уже давал замечание Антону, он уже фиксел это"; he is moving the data-centre side onto that service ("женя сейчас это делает"). See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 30, 4:57 AM).
- **The SAS-link checkbox.** "у нас… галочка… [п]оказывает [fault], если [SAS] линк даун… никто не запрещает ей ставить". See [[wiki/decisions/2026-09-24-a-flex-port-that-dies-holding-money-sends-it-to-unclaimed-and-one-without-a-gateway-goes-out-of-service.md]] (Sept-30 update).

## Open commitments (Sept 30 2026)

- [ ] Evgeny Kharetski — get the logs and find out why the "always last" queue fix does not show on screen — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [ ] Evgeny Kharetski — close the CC-talk task (heard as "сети 58 58"; the notes read CT-5858) — due Sept 30 2026 — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]

## Oct 1 2026 — "вчера зарядили версию", the IO board, LEDs and counter board, Anton's daily fixes at Claude's prompting, and statistics that do not work

At the [[wiki/meetings/2026-10-01-daily-standup-sas-mode-flag-and-feature-status-rules.md|Oct-1 Minsk stand-up]] (Russian; called on as "Женя") [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]:

- **A version loaded.** "Она вчера зарядили версию" — a version was loaded on Sept 30; which build and for which machine is not said (see [[wiki/decisions/2026-09-29-the-fix-goes-out-as-a-re-release-not-a-hack-and-only-that-commit-goes-in.md]], Oct-1 annotation).
- **His work.** "дальше занимался l gs 12. 19 это и [IO board]. И ледами. [Counter board] ещё доделать" — the LGS number is garbled again (Sept 29 "212 19", Sept 30 "20, 19" — not resolved); the IO board, the LEDs and the counter board are the derived notes' readings [[raw/Meeting_Notes_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]. Biratka said that morning that Kharetski already has the IO board working on the service ("Женя сказал, что у него уже работает" — Kharetski by context).
- **The loop with Anton.** "У нас каждый день Антон чтото доделывает. По моим просьбам в сервисах… Я. Прошу Клода посмотреть, что у нас есть всё, чтобы отказаться от [мотива — unclear]. Он смотрит и говорит, блин, тут ещё вот это вот надо сделать, без этого не можем. Я даю Антону Антон делает говорю, ну теперь то всё посмотри такой. Да Ну вот ещё нашёл момент." "Антон" — the same unresolved service-side Anton as on Sept 23, 28 and 30 (not forced).
- **Statistics.** "Сейчас мы что то со статистикой подвисли, непонятно, что там как [шлёца — unclear] вообще работает, оно не работает. Так что сейчас план это на локальный хост подключиться через интернет и через интернет в локальной сети, посмотреть, что там. Все сообщения долетают как надо. Может у нас гдето в логике чтото у когото сломалось."
- **In the status argument.** "почему прозвучало, что мы пишем автотесты на фичи? Может быть, на [требования] должны были в писать" — Irina: on requirements; "То есть одна фича одно требование" — not necessarily. See [[wiki/decisions/2026-10-01-completed-is-the-developers-last-step-and-a-found-problem-sends-the-feature-from-completed-back-to-to-do-as-a-story.md]].
- His Sept-30 commitments above (the logs for the queue fix; the CC-talk task) were not mentioned. Ivan said he works "С Женей" on autotests that morning (Kharetski by context).

## Open commitments (Oct 1 2026)

- [ ] Evgeny Kharetski — find why the statistics are not being sent: connect to the local host over the internet and over the local network and check that all messages arrive — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]] — *Oct 2 2026: "Вчера с ваней, я работал по статистике" — worked on, not declared fixed* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]

## Oct 2 2026 — statistics with Ivan, the LEDs and the IO board to be closed today: LGS-12, 17, 19 and CC Talk "58"

At the [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 Minsk stand-up]] (Russian; called on as "женя") [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]: "Вчера с ваней, я работал по статистике. Леды добивал. Я даю сегодня закрою. Есть [поврек — unclear]. Вот ну и вот [IO board] добью. Сегодня тоже. Ну короче все 3 задачи сегодня будут закрыты [LGS] 12, 17, 19" — Pavel: "[CC Talk] тоже сегодня да" — "Где 58? 58 да?" ("ваней" = [[wiki/people/ivan.md|Ivan]], by context — inference.) The LGS numbers are clearer than on Sept 29 – Oct 1 (then "212 19", "20, 19", "12. 19"); the derived notes read LGS-12, LGS-17, LGS-19 and "CC Talk (58)" [[raw/Meeting_Notes_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]. Pavel then had Kovalchuk fix a due date, by position in the round on his items (inference): "Дью дэйт чуть не движок… Сегодня заканчивается начало, поставь неделю назад". Ivan said Zhenya may need to release his part for South Dakota ("Ещё тогда [Жене] нужно будет") — [[wiki/projects/south-dakota-vlt-market.md]] (Oct 2). The unresolved service-side "Антон" was not mentioned.

## Open commitments (Oct 2 2026)

- [ ] Evgeny Kharetski — close LGS-12, LGS-17 and LGS-19 (the LEDs, the IO board) and the CC Talk task ("58") — due Oct 2 2026 ("сегодня") — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]] — *Oct 5 2026: "закрыл там. Интеграции прошлые там [лет]… [IO] борду там чутьчуть" (the LED and board integrations closed — reading); CC Talk "сейчас… заинтегрирую" — in progress; the task numbers spoken ("12, 37… 12 3 24") do not match Oct 2's and are unclear* — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Oct 5 2026 — CC Talk being integrated, prose and contracts for the integration repository, another separate service, and "релиз должен в файле запекать какие версии были включены"

At the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian; called on as "женя") [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]: "Я сейчас [CC Talk] заинтегрирую и одновременно на [тэтоцентр — unclear] в GT, который [трейдский — unclear]. Там прозы всякие контракты… закрыл там. Интеграции прошлые там [лет — LEDs, reading], [аккаунты борт — unclear] но по [IO] борду там чутьчуть… отдельный сервис сделали ещё один. Его тоже надо. Сделать… 12, 37 на очереди 12 3 24 чтото там ещё добавится новый." To Pavel's manifest question: "Не обязательно, что ты укажешь для сборки то и будет… я рассчитываю сделать. [GitHub Page]… галочку релиз… Без [снапшотов]… художникам… нужны [—], где разрабатываются или для автотестов также нужны [снапшоты]"; "главное, что релиз должен в какомто файле. Типа. Запекать. Какие версии? Были. Включены в этот релиз. Чтоб потом это можно было отслеживать всё." Chudinov named him (or Ivan) to say whether the SAS polling / handpay traffic is normal. Ruling: [[wiki/decisions/2026-10-05-a-release-bakes-a-file-of-the-component-versions-it-contains-into-the-artifact.md]]; see also [[wiki/decisions/2026-09-03-module-contracts-and-nova-integration-repository.md]] (Oct-5 update).

### Open commitments (Oct 5 2026)

- [ ] Evgeny Kharetski — make the release bake a file of the included component versions into the artifact; later the GitHub Page with release / snapshot selection — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Oct 5 2026 (7:01 AM) — "graphic contracts", conversion tests vs game scenarios, an integration repository with no structure yet, and "feed this meeting to Claude"

At the [[wiki/meetings/2026-10-05-rage-nova-port-autotests-and-horizontal-to-vertical-layout.md|Oct-5 7:01 AM Rage-to-Nova review]] (Russian) [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]:

- He gave the geometry checks their name — "типа контрактов графических, так называемых" — and Val adopted it — [[wiki/decisions/2026-10-05-geometry-first-port-autotests-accepted-and-geometry-checks-named-graphic-contracts.md]].
- **Where tests live:** autotests that check a conversion belong to the conversion project, not NOVA; game scenarios belong in the NOVA integration repository, which exists but has no structure yet ("скоро появится"). Separate, independent structures are the norm — [[wiki/decisions/2026-10-05-conversion-tools-and-tests-leave-the-local-computer-now-and-claude-proposes-the-repository-layout.md]].
- **His proposal, which Val liked:** "я бы на самом деле вот этот митинг скормил клоду… наши стандарты" and get a proposal for this non-standard case. Until then Igor can put the game scenarios in his current repository "чтобы их не потерять".

## Oct 5 2026 (11:00 AM, in absentia) — the one engineer free for RIS improvement MVP1

At the [[wiki/meetings/2026-10-05-ris-mvp1-scope-and-peach-packaging.md|Oct-5 11:00 AM "RIS changes review"]] Pavel said "we can involve, for example, Evgenyk Kharetski right now, but we cannot take Dima and Serge right now" — so he is the available resource for the two-week RIS MVP1. See [[wiki/decisions/2026-10-05-ris-improvement-mvp1-is-five-jira-capabilities-in-one-release-due-october-19.md]]. [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]

## Oct 6 2026 — the urgent RIS work for Georgia comes first

At the [[wiki/meetings/2026-10-06-daily-standup-ris-georgia-branch-and-critical-error-text.md|Oct-6 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]:

- He closed work on the DC and tests "для сиситолока" (the notes say SAS log tests; **unclear**), and is cleaning GitHub per Val's email.
- Pavel put the urgent RIS changes ahead of his own plans: CAP-252, 255, 246, 254, mostly LGS, Georgia only, on the 1.14 line — [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]]. He confirmed the carousel is dropped and statistics come only when scanned.
- On the critical-error text he asked how anyone can know all causes are covered, and suggested walking back from where the exception happens — [[wiki/decisions/2026-10-05-the-critical-error-screen-shows-the-cause-and-fix-in-words-and-keeps-the-qr-code-in-mvp1.md]].
- Ivan will ask him to release the DC if South Dakota runs an hour without trouble.

## Oct 7 2026 — error handling first, then the QR and statistics out

At the [[wiki/meetings/2026-10-07-daily-standup-test-coverage-first-and-ai-task-numbers.md|Oct-7 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]: he went over his tasks with Claude, which advised starting with error handling — "Принципе, наверное, сделано". Next, by Pavel's summary, "выпили кюар и статистике" (remove the QR and the statistics); the task numbers he read are garbled. A release went out the day before; a question from Ivan is to be handled later — [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] (Oct-7 update).

## Oct 8 2026 — task 1239 for the old GA COAM, and "conversion must be predictable and approved"

- **Stand-up (4:58 AM).** At the [[wiki/meetings/2026-10-08-daily-standup-lease-expiry-scenarios-and-flex-signal-quality.md|Oct-8 Minsk stand-up]] he said he is on task 1239 (the notes' reading), a new lease for the old GA COAM; server-side decisions were taken the day before; the old release cannot move to Git because it depends on Nexus; he fixed a tab that did not show and re-released — [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] (Oct-8 update) [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]].
- **Rage-to-Nova review (7:04 AM).** At the [[wiki/meetings/2026-10-08-rage-nova-dragon-pays-vertical-port-and-symbol-distortion.md|Oct-8 7:04 AM Rage-to-Nova review]] he agreed with Claude-built scenes, and explained the saving as the scene-assembly step. He said the converted pay table looks wrong to him and that conversion must be predictable and approved by the game owners, "Майкл Лена"; for existing games a designer should draw a vertical comp from the existing art, for new games universal resources and two comps — [[wiki/decisions/2026-10-05-horizontal-to-vertical-conversion-runs-in-parallel-with-the-port-autotests.md]] (Oct-8 update), [[wiki/decisions/2026-10-08-game-scenes-are-assembled-by-developers-with-claude-from-designer-resources-not-by-designers.md]] [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

## Oct 9 2026 — task 1238; Tsymanov has the server side; the old RIS at factory reset is planned, not scheduled

At the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 stand-up]]: on "12 38" (the notes: 1238, lease work for the old software); the server side is Tsymanov's task; Pavel offered the old-RIS-at-factory-reset option as next work, "в планах" but not scheduled; he does not load his plan far ahead because priorities change — [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] (Oct-9 update) [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].

## Oct 12 2026 — near the end of "1241"; he tests it himself; "до 22"

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 stand-up]]: almost done with 1241 (number unclear); testing should start, and with Ivan on autotests he will test it himself; "до 22 мы хотим выпустить" — [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] (Oct-12 update) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].

## Oct 13 2026 — closing 1241; testing MVP 1 himself, with stories under the feature

At the [[wiki/meetings/2026-10-13-daily-standup-video-decode-memory-and-release-task-type.md|Oct-13 stand-up]]: he will close 1241 now — [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] (Oct-13 update); he tests MVP 1 himself while Ivan is busy and opens stories under the feature for each test — [[wiki/topics/test-automation-strategy.md]] (Oct 13) [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]].

## Oct 14 2026 — passport work done; battery test (task 246); then MVP 2 tasks; doubts on boot-loop recovery

At the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]:
- Passport work finished and tested on a real machine; some devices show as missing only after work; device logic left as is; battery test under task 246 — [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] (Oct-14 update).
- In his turn Pavel extended MVP 1 to about November 8 or 9 with the MVP 2 tasks inside; he asked whether the old version is still delivered — yes — [[wiki/decisions/2026-10-14-mvp1-is-extended-to-about-november-8-or-9-and-the-mvp2-marked-tasks-are-done-inside-it.md]].
- Asked to study boot-loop recovery from the data-center side, he doubted it and proposed a recovery mode; not in MVP 1 — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 14).

## Oct 15 2026 — a saved RIS on the machine when there is no network; battery check done; LGS 1243 next; NAD 2 in parallel

At the [[wiki/meetings/2026-10-15-daily-standup-offline-ris-fallback-and-nova-game-conversion.md|Oct-15 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]: his new plan — with no network, or a server refusal, the machine offers the person a previously saved RIS; asked how many, "Сколько угодно нет ограничений. Может быть 100" — moved to an after-lunch meeting — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 15). The battery check works, and a new event is logged when the battery is replaced; he sent the plan back to Ivan for a hands-on check. Next is LGS 1243, front and back end. He could do the NAD 2 data-center work in parallel; Igor said it is not a priority — [[wiki/topics/nova-platform-architecture.md]] (Oct 15).

## Oct 16 2026 — RIS analysis

At the [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct-16 stand-up]] ("Женя", speaker label) [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] he began analysing RIS the day before and settled one question with Tsymanov; Pavel: if not fully sure of an answer, discuss it all together — [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 16).

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026.md]]
- [[raw/Meeting_Transcript_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]
- [[raw/Meeting_Transcript_AI_Engineering_Workflow_and_Hardware_CxO-August-6-2026.md]]
- [[raw/Meeting_Transcript_initiative_priority_schedule-2-March-26-2026.md]]
- [[raw/Meeting_Notes_initiative_priority_schedule-March-26-2026.md]]
- [[raw/Setting up JVL ways on GitHub-March-18-2026.md]]
- [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]
- [[raw/autotests_sync_meeting.md]]
- [[raw/Claude Code integration - continued.md]]
- [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-4.md]]
- [[raw/GitHub_Ways-February-11-2026.md]]
- [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
