---
type: person
title: Evgeny Kharetski
date: 2025-07-10
aliases: [Evgeny Kharetski, Evgeny Kharetsky, Evgeny Khoretsky, Kharevsky, Yauheni Kharetski, Kharetsky, Koretski, Koretsky, Korecki, Khorvatsky, Корецкий, Хорватский, Халецкий]
source-count: 17
open-commitments: 3
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

## Open commitments (Aug 24 2026)

- [ ] With [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]]: meet locally to agree one prose-writing standard, place it in the standards repository, then run Claude over the existing prose to normalize it and merge the overlapping backend/frontend capability sets into one — due Aug 25–26 2026 for the standard — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [ ] Finish prose and capabilities for the remaining ~16 LGS modules at one to two per day — due ~1–2 weeks from Aug 24 2026 — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [ ] Work out with "Andrei" (which Andrei is not stated) whether a repository rule can block a PR that changes code but carries no updated prose folder; test it on one repository first — due unspecified — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Sources

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
