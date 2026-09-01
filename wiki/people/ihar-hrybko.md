---
type: person
title: Ihar Hrybko
date: 2024-01-01
aliases: [Ihar Hrybko, Igar Hrybko, Hrybko, Gribkov, грибков]
source-count: 12
disambiguation: "UX/UI (payroll Igar Hrybko; JVL Insights-era consultant). One of FIVE Igor-named people (owner-ruled): Igor Donis (Financial Controller → wiki/people/igor-donis.md), Igor (Ihar) Nazarenka (mobile-app, owner-confirmed 2026-07-14 → wiki/people/igor-nazarenka.md), Igor Starovoytov (contractor industrial designer → wiki/people/igor-starovoytov.md), Igor Metelski (RGS engineer, = payroll Igar Miatselski → wiki/people/igor-metelski.md), Ihar Hrybko (UX/UI → wiki/people/ihar-hrybko.md). Resolve by context: finance/corporate → Donis; mobile app/UI + new-market ops → Nazarenka; cabinet/industrial design → Starovoytov; RGS/online-integration code → Metelski; queue anything fitting none."
---

# Ihar Hrybko

Ihar Hrybko appears in the **JVL Insights** knowledge-base proposal (~2023–24) as a **consultant**, titled **Sr. UX/UI Specialist** — scoped to design user-friendly interfaces, ensure accessibility/usability across devices, and work with the programmers on UI/UX integration. [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]

- The Minsk payroll roster lists a names-only "**Hrybko, Igar**" ([[wiki/topics/minsk-staff-roster.md]]); the same rare surname makes this **very likely the same person** (Belarusian spelling Igar ↔ Ihar), though the roster lists him on Minsk payroll while the JVL Insights draft labels him a "Consultant" — both recorded, not resolved. [[raw/minsk_staff_roster_2025_names-only.md]] [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- Compensation details in the source are withheld (§15.8). See [[wiki/projects/jvl-insights-knowledge-base.md]]. [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]

## FlexPay frontend (stated Mar 27 2025)

- On the FlexPay scope-gap meeting Pavel described the FlexPay kiosk software as "backend introduced by Dima, and **frontend implemented by Igor Hrybko and Anton Seregin** from Graphic User Interface. HTML5, HTML-based JavaScript." — the first transcript statement of Hrybko's concrete product work, consistent with his Sr. UX/UI title below. See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]

## Active on machine setup screens (Apr 15 2025)

- First 2025-transcript sighting in an operational role: Val on the Omni daily — "на следующий митинг я приглашу Игоря Хребко, который занимается этими сетапами" (rendered "Хребко"; matched to Hrybko by the rare surname + setup/UI context, labeled inference). He owns the machine **setup screens** work that the Calle Ocho Omni port needs in full for GLI (history, reports, settings — old screens can't be reused); Pavel to start working with him so his features are written up for Calle Ocho Omni; initial-setup is "на подходе," the main setup "там совсем ничего нет." [[raw/daily_omni_progress-apr-15-2025.md]]

## Apr 16 2025 — present all setup screens for the June-1 GLI machine

In the Omni daily Val put "tomorrow's attention" on Igor Hrybko: walk **all machine screens** (those already working on the new machine and those still needed) — the machine goes to **GLI June 1**. Screens are ready "в формате лоялта" but the business logic isn't implemented yet. A Florida-casino consultant can list competitor screens, and OneMartinus/Juan works with them daily, so Hrybko can source screens through them. [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]

## Apr 24 2025 — setup-screens scope, UI kit, multi-language feature

On the setup-screens review ([[wiki/meetings/2025-04-24-omni-setup-screens-june-scope.md]]) Igor Hrybko (UI/UX designer, "I'm not a senior front-end developer") explained his year's work: transferring the **Figma mockups into React layouts / components (a UI kit)** with a **shared library between the FlexPay setup and the initial setup**, plus the FlexPay GUI and a Docker dev environment; the remaining task is porting business logic from the legacy **XJS (2008)** framework. Val assigned him the new **LGS 630 (6.3.0) multi-language feature** for the initial setup (May 3–17). See [[wiki/decisions/2025-04-24-omni-first-release-legacy-plus-remote-setup-screens.md]]. [[raw/set_up_screen_omni-apr-24-2025.md]]

## May 20 2025 — freed for the FlexPay partial-redemption screen

On the [[wiki/meetings/2025-05-20-flexport-flexpay-smib-action-review.md|May-20 SMIB action review]] Igor Hrybko ("Игорь Хребко") was reported freed up and assigned the new **user-facing UI screen** letting a player choose how much to move to a card (part of **FP256** partial-redemption-to-card), with [[wiki/people/dmitri-chudinov.md|Chudinov]] supplying the API — targeted ~May 23. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-port_flex-pay_smib_update-may-20-2025.md]]

## May 29 2025 — partial-redemption UI API delivered

On the e-Wallet/TITO review ([[wiki/meetings/2025-05-29-ewallet-tito-flexpay-implementation.md]]) it was confirmed [[wiki/people/dmitri-chudinov.md|Chudinov]] provided Ihar (as "Игорь Хребков") the **API to build the FlexPay partial-redemption user interface** — the front-end side of the now-complete partial-redemption feature. (Continues the May-20 FP256 amount-select screen assignment.) [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]

## Aug 19 2025 — figma-to-development debate (the "Igor" who makes the mock-ups)

On the [[wiki/meetings/2025-08-19-figma-to-development-testing.md|Aug-19 figma-to-development working session]] Ihar Hrybko is **addressed throughout as "Igor"** (Pavel: "Igor, can you export CSS?" / "Igor, do you use material-UI components?"; Aaron: "I will tell you Igor…") — the answering speaker label is consistently *Ihar Hrybko*, confirming this is him (registry: UX/UI, payroll "Igar Hrybko"). He is the UX/UI designer building the setup-screen mock-ups. His position: **Figma cannot auto-generate integration tests or production-ready React** for JVL's complex app — Figma is for mock-ups + interactive usability prototypes; JVL builds screens fast from a paid **Joy UI**-style component kit (recreated manually) whose React components are already tested, then **hand-crafts** the actual React layout using Figma only as a reference. Auto-export plugins produce landing-page-grade code, unusable for maintainable production. See [[wiki/topics/test-automation-strategy.md]]. [[raw/figma_to_testing_development .md]]

## Feb 3 2026 — ran the live Claude Code exploration of the LGS monorepo

- On the [[wiki/meetings/2026-02-03-claude-code-integration-continued.md|Feb-3 Claude Code workshop]] "Igor" (Ihar Hrybko) was the engineer at the keyboard for Aaron's **live Claude Code run**: he opened the **"platform local gaming server"** monorepo in VS Code (front end in the `LGSUI` React-components package he works in; the rest back end), launched Claude Code in WSL/bash, and let it spin up three Explorer sub-agents to traverse the repo and auto-write a `docs/` tree (README, architecture overview + Mermaid diagram, API data-contracts, test scaffolding). The run hit Windows/WSL tooling problems (crashes, broken hooks). See [[wiki/topics/ai-assisted-development.md]] (Feb-3). [[raw/Claude Code integration - continued.md]]

## Feb 4 2026 — figma→React layout hand-off; the Claude-review PR loop

- On the [[wiki/meetings/2026-02-04-figma-react-export-workflow.md|Feb-4 figma→React session]] Pavel noted the **design→layout** work (Figma → React) has historically been done mostly by [[wiki/people/anton-seregin.md|Anton Seregin]], with **Hrybko doing part of it** recently because Seregin was overloaded. Val set the **first branch hand-off as Hrybko → Seregin**. Val also cited a demonstrated **Claude-Code review loop** between Hrybko and [[wiki/people/evgeny-kharetski.md|Kharetski]]: Hrybko opened a PR to main; Kharetski reviewed it with his local Claude Code, committed the comments; Hrybko received them and made the file commit to master. See [[wiki/topics/test-automation-strategy.md]] (Feb-4) and [[wiki/topics/graphics-team-git-workflow.md]]. [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]

## Feb 6 2026 — Figma→React workflow explainer + "metacoding"

On the [[wiki/meetings/2026-02-06-ui-claude-code-adaptation.md|Feb-6 UI/Claude-Code session]] "Igor" (Hrybko) was the front-end voice explaining the actual workflow (substance on [[wiki/topics/ai-assisted-development.md]] Feb 6):

- He corrected Aaron's framing that Figma auto-decomposes to software: JVL uses Figma for **prototyping / interactive prototypes and user-flow**, but has **no button to export layouts directly to React**. The team **hand-builds components from a tested UI kit — MUI, via its fork Joy UI — with a "JVL theme"**; or he feeds **Claude Code a screenshot + prompt** to generate a new layout on an existing pattern and then **supervises** the generated source. LGS layouts are "almost completely created except some screens." [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]
- He coined **"metacoding"** (vs "vibe coding") — using an LLM + IDE while **supervising/controlling the architecture from engineering knowledge**; Aaron praised the term. [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]

## Sources

- [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]
- [[raw/Claude Code integration - continued.md]]
- [[raw/Irina_Pavel_Figma_React-February-4-2026.md]]
- [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]
- [[raw/figma_to_testing_development .md]]
- [[raw/minsk_staff_roster_2025_names-only.md]]
- [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- [[raw/daily_omni_progress-apr-15-2025.md]]
- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- [[raw/set_up_screen_omni-apr-24-2025.md]]
- [[raw/flex-port_flex-pay_smib_update-may-20-2025.md]]
