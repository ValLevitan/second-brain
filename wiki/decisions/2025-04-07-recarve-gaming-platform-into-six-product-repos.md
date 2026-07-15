---
type: decision
title: Re-carve the "Gaming Platform" Jira initiative into six product-repos (OmniCore, OmniLandBaseFramework, OmniOnlineFramework, LGS, RGS, OmniMath)
date: 2025-04-07
aliases: [six products, gaming platform recarve, IP481 products, OmniLandBaseFramework, OmniOnlineFramework, OmniMath, product per repository, LGS RGS split]
source-count: 2
status: active
open-questions: 3
---

# Re-carve the "Gaming Platform" Jira initiative into six product-repos

**Decision (Val, with [[wiki/people/alexander-biratka.md|Sasha]], [[wiki/people/pavel.md|Pavel]] and [[wiki/people/andrey-bosik.md|Andrei Bosik]], Apr 7 2025):** keep the Jira initiative name **"Gaming Platform" (IP481)** but re-carve the products under it into **six products, each its own repository** — **OmniCore, OmniLandBaseFramework, OmniOnlineFramework, LGS, RGS and OmniMath**. This is the origin of the product/repo structure the Apr 15–17 Omni dailies then executed (see [[wiki/topics/omni-core-advancement-and-game-templating.md]]). [[raw/github_jira_reshuffling_products-april-7-2025.md]]

The meeting is Russian, with Val, Sasha and Pasha; Andrei is present for the diagram work. The transcript internally duplicates its own content (the same discussion is transcribed two–three times); facts recorded once. [[raw/github_jira_reshuffling_products-april-7-2025.md]]

## Why re-carve — "confused between beauty and the fundamental truth"

- The trigger was Sasha's git-submodule pain: **Omni-Core** is a shared submodule inside **Omni-LandBase** and **Omni-Online**, so a change made in Omni-Core forces a manual commit of a new submodule reference into the parent repo, and creating feature branches across submodules constantly produces merge conflicts ("постоянно приходится эти конфликты разбирать"). Working in main/dev is fine; branching is where it breaks. [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- Digging into it, the group realised the "Omni platform" had been **over-stretched**: they had forced LGS, RGS and an HHR overlay screen under one "Gaming Platform" product, but **LGS is a different application/language, RGS attaches to online (not land-based) games, and the HHR overlay is a standalone product**. Val: "we are confused between beauty and the fundamental truth." The *real* Omni is narrower — Omni Framework / Engine + Miranda Asset Loader (graphics/render/game reuse); its benefit is **reuse of common code (Pixi engine, loaders) and game resources** across online and land-based, with shared **math** (same container/Docker image tested once for both). A land-based game still needs rework vs online (heavy video resources vs small). [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- The machine's shipped software is a **"package"** (Val floated "land-based game package" / "online game package") assembled from independent products — Linux system, games, LGS, libraries, hardware layer, math, Omni Framework — **each its own repository, released (almost) independently**. [[raw/github_jira_reshuffling_products-april-7-2025.md]]

## The rules confirmed

- **Repository = product** (settled: "репозиторий это продукт"). A product has capabilities; a capability is a **demonstrable ability of the product**; multiple **features** satisfy one capability; a feature is narrow (~one sprint). Example given: **"support for a new RIS version" is one capability that touches several modules → several features** (ties to [[wiki/decisions/2025-04-03-license-software-per-operator-not-machine.md]]). [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- **Sync between Jira and GitHub happens at the capability↔feature boundary:** in Jira, features sit under capabilities under a product; in GitHub, feature branches open in the product's repository; a feature that must change two products gets a matching feature entered under each product. [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- Renamed **LGS → Omni LGS** for naming uniqueness/sync (org/repo names must be unique; the Bitbucket migration carried old "2 years ago" commit dates). Product IDs referenced: **Omni Framework = IP 416; Omni LGS = IP 94; Gaming Platform initiative = IP481.** [[raw/github_jira_reshuffling_products-april-7-2025.md]]

## Action list

- In Jira, keep initiative **Gaming Platform (IP481)**; replace its products with the six named above. [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- **Describe each product** (Val's method: draft the description in Russian with ChatGPT, then translate to English); breaking each into capabilities is a later step. [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- Existing **residual code** moves straight into `main` of its own repository (Sasha refused to retroactively open feature branches over already-written code — "это обманный маневр," it would misrepresent which code the branch holds); **new** work goes via feature branches. [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- **Andrei Bosik** to make the GitHub repositories a mirror image of the decided structure and link the architecture diagrams under the correct project in Confluence and Jira; Val also wants the diagram referenced in the repo README files. [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- Follow-up meeting set for the **following Wednesday** for a redone layout. [[raw/github_jira_reshuffling_products-april-7-2025.md]]

## Apr 8 2025 — executing the carve in Jira Plans + GitHub

The next working session ([[wiki/meetings/2025-04-08-github-jira-product-repo-naming.md]], Val / Pavel / Andrei Bosik / Sasha; internally duplicated §12) went product-by-product through the Jira Plans list to make each name match its GitHub repository exactly. Rulings: [[raw/github_jira_structure_repositories-april-8-2025.md]]

- **Prefix everything "Omni"** for grouping/searchability (Val's marker). **RGS → Omni RGS** (Pavel had created a new "OmniRGS" alongside old RGS; the old one is not kept). LGS-content repo (still on Bitbucket, empty on GitHub) renamed to **Omni LGS Setup Screens**. IP names must be **identical to the repo name, same letter-case**; IP416 uses a **dash, not underscore**. [[raw/github_jira_structure_repositories-april-8-2025.md]]
- **Omni LGS Setup Screen stays a separate product** — it is the LGS Graphic-User-Interface piece, written in a different language by different developers, built and versioned independently (an LGS can pair with a different setup-screen version). [[raw/github_jira_structure_repositories-april-8-2025.md]]
- **Miranda Asset Tools is NOT a separate product** — it is only the **Miranda integration/asset-loader module** that lives inside the platform; its code lives in OmniCore now, so its features fold into OmniCore and the product is closed (marked "Asset Loader"). [[raw/github_jira_structure_repositories-april-8-2025.md]]
- **HHR → "Omni HHR Land Based Overlay"** — a **standalone application** (its own repo) covering horse-movement, help screens and the handicap menu; the regulator **recommended isolating it** so game changes don't force re-review of the betting/overlay screens. It ships as a **version-pinned built artifact** (example: overlay v1.3) pulled into the top-level package. Whether it also serves online is unknown (small mobile screen; no prior implementation — "we would be first on the market"). [[raw/github_jira_structure_repositories-april-8-2025.md]]
- **Vivien needs its own repository** — it has never been in the Jira repos and never will be code-wise; it currently exists only as a **feature ("Vivien DataSync") under IP24**. (See [[wiki/projects/vivien-application.md]].) [[raw/github_jira_structure_repositories-april-8-2025.md]]
- **OmniMath sits in a separate GitHub org** ("JVL Game Math Engine Mechanics", transcribed variants) created for **restricted access** to the math; that org does not line up with a Jira value stream. The **template-repo** mechanism was confirmed — "create new repository from template" (green button) — and Val asked that a **GitHub link be added to every Jira IP**. [[raw/github_jira_structure_repositories-april-8-2025.md]]

## Open questions

- **GitHub organizations vs Jira value streams (opened Apr 8):** three linked questions Val left open — (a) how to map GitHub orgs at all; (b) whether to parallel org names to Jira value streams (Andrei's original proposal; Aaron pushed to merge game concept/design/production into one "games development" org); (c) whether **OmniMath** belongs under Gaming Platform or should move to Game Concepts. Sasha's view: orgs are a GitHub-only construct (Bitbucket/Azure have no equivalent) used only for access control — JVL may simply ignore them for Jira purposes. Deferred. [[raw/github_jira_structure_repositories-april-8-2025.md]]
- **Keep git submodules, or drop them for a monorepo / versioned-artifact libraries?** Deferred — Val wants to read up before deciding ("давайте тему сабмодуля поднимем в другой раз"); Sasha leans toward dropping them because feature-branching across submodules is error-prone. Options aired: keep submodules but don't branch inside them (main/dev only); a monorepo with two builders; versioned libraries that emit artifacts (the old online way). [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- **Sprint length:** raised whether to lengthen the sprint from two weeks to **three or four** so more than one feature lands per sprint; deferred (Val elsewhere caps it at +1 week). [[raw/github_jira_reshuffling_products-april-7-2025.md]]

## Sources

- [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- [[raw/github_jira_structure_repositories-april-8-2025.md]]
