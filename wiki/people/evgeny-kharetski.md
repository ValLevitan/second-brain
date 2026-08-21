---
type: person
title: Evgeny Kharetski
date: 2025-07-10
aliases: [Evgeny Kharetski, Evgeny Kharetsky, Evgeny Khoretsky, Kharevsky, Yauheni Kharetski, Kharetsky, Koretski, Koretsky, Korecki, Khorvatsky, Корецкий, Хорватский, Халецкий]
source-count: 13
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
