---
type: topic
title: GitHub release management and the CI/CD release pipeline
date: 2025-10-21
aliases: [release management, release pipeline, CI/CD, GitHub Actions pipeline, release artifacts, ISO image release, release manager role, continuous delivery, flex os installer, manifest, release candidate]
source-count: 3
open-questions: 1
---

# GitHub release management and the CI/CD release pipeline

How JVL turns committed code into a certifiable, shippable release inside GitHub — the repository lineage, the automated lint→test→build→release pipeline, the artifact/manifest model, and the human **release-manager** role ([[wiki/people/ivan.md|Ivan]]) that carries a build through to **GLI** certification. This is the "new ecosystem" replacing the legacy Jenkins/Dropbox flow for Omni games. Worked out across three late-October 2025 sessions (Val, [[wiki/people/aaron.md|Aaron]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/pavel.md|Pavel Frolov]]). This topic is the **sequencer** for that thread; the individual meeting stubs stay thin.

It sits downstream of the repo-structure decisions ([[wiki/decisions/2025-02-21-separate-game-and-design-repos.md]], [[wiki/decisions/2025-03-12-fork-game-repos-from-generic-template.md]], [[wiki/decisions/2025-04-07-recarve-gaming-platform-into-six-product-repos.md]]) and the Jira↔GitHub mapping ([[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]); artifact storage overlaps [[wiki/topics/jfrog-artifactory-artifact-management.md]].

## The repository lineage: concept → design → production

- A single **game-concept repository** holds every game concept ever, and **lives forever** — JVL keeps adding to it. When a concept is promoted, JVL **sparsely forks just the one directory** for that game into a new **game-design repository** (the path is carried over so lineage is visible), and the design work is built out there. [[raw/releases_github-october-21-2025.md]]
- The **production repository** is created from a **master production template** (a generic template "with no colors in it"); the design work is attached to it as a **git submodule** — a reference/symbolic link back to the still-standing design repo, so nobody commits a separate copy and traceability runs production→design→concept. (Andrei noted JVL's practice is to create the production repo from a clean template rather than fork the design repo, since it doesn't need most of the design history — either way is fine; Aaron's priority is clean separation + traceability.) [[raw/releases_github-october-21-2025.md]]

## The automated pipeline (GitHub Actions)

- The production repo carries a `.github/actions` directory of actions that **watch for pushes**. On every commit the pipeline runs in order: **linting** (fails fast and stops everything else) → **tests** (run on every commit) → **build** (rebuilds on every source change) → and, if all pass, **deploy/release**. [[raw/releases_github-october-21-2025.md]]
- **Artifacts are separate from the action pipeline.** GitHub stores release artifacts (gzip/zip, ISO image, EXE, etc.). A release can bundle **multiple artifacts simultaneously**, all tagged with the **same version** — e.g. an EXE, an ISO, a zip, a **PDF instruction book compiled from the markdown docs**, and a link to an online-play build. [[raw/releases_github-october-21-2025.md]]
- **Every release is an immutable, uniquely-tagged version.** Each artifact ties to a commit hash / version tag that can never be reproduced-and-altered (re-running the action reproduces the identical checksum; any change changes the checksum). Aaron showed **OBS Studio** and **RustDesk** GitHub release pages as the model for what JVL's game releases should look like. [[raw/releases_github-october-21-2025.md]]
- **Continuous delivery via cascading integrator repos.** Each piece (a game, the Linux OS, the back-end/CMS) is individually runnable and has its own releases; an **integrator repository** watches for new release tags from the pieces and auto-assembles them into the bigger ISO. A new release tag on one game ripples up the assembly chain automatically — Aaron's "north/south assembly line" and factory-sub-assembly analogy. [[raw/releases_github-october-21-2025.md]]

## What a "release" is (worked examples)

- A **release is a collection of artifacts** answering an initiative. For a **Class-3 single game**, that is one game — **Calle Ocho** (the first Omni game; transcribed "Kaya Ocho"/"Kayocho"/"Calle Ocean"). For **Georgia**, the release is a **multi-game package**: a **multi-game selection screen** component plus several games (Val's example: six games), each with its own checksum, all under one version number. [[raw/releases_github-october-21-2025.md]]
- The final deliverable is an **installable ISO image** built from many constituent artifacts (game(s), OS, drivers, etc.) — not the same as a lightweight EXE that Michael/Juan double-click to preview a single game. [[raw/releases_github-october-21-2025.md]]

## The final-image installer and its manifest (Oct 22)

- The **`platform flex os installer`** project performs the final assembly of all components into the installable machine image. It holds a **manifest file** (still an early seed) declaring **which components make up the final product**. This is the installer layer of the "platform flex back end" system. [[raw/artifacts_assembly_GitHub-october-21-2025.md]]
- On each release, [[wiki/people/ivan.md|Ivan]] fills the manifest with the **specific version of each component** for that build. Components vary by package: a single game reuses the same components; a Georgia multi-game package lists a distinct component per game (likely including the multi-game screen). [[raw/artifacts_assembly_GitHub-october-21-2025.md]]
- The manifest can pin the **checksum of each binary artifact**; if the build can't find an artifact by checksum, it **errors** — so components placed on the agreed "shelf" assemble deterministically. [[raw/artifacts_assembly_GitHub-october-21-2025.md]]
- Val's view: a mature release-management **methodology/standard already exists** in industry (designers put artifacts on a shelf, the release manager takes from it) — JVL just needs to read and adapt it. [[raw/artifacts_assembly_GitHub-october-21-2025.md]]

## The two build actions and the release-candidate gate (Oct 22 practice run)

- JVL distinguishes **two build actions**: (1) build **binary files from text/source files** — done by the developer during assembly of game pieces (specialists like [[wiki/people/irina-makarych.md|Irina Makarych]] help); (2) assemble the **ISO game image from the binaries**. [[raw/practice_release_calle_ocho-github-october-21-2025.md]]
- **Marking a build field-ready is [[wiki/people/ivan.md|Ivan]]'s job.** Any developer can build sources and download the artifact, but Ivan marks the artifact — or runs a separate build action with the **full test list** — and only after all tests pass is the build tagged a **release candidate**. [[raw/practice_release_calle_ocho-github-october-21-2025.md]]
- A **practice release of Calle Ocho** was planned as a dry-run: assemble the game in its current state, driven by Ivan (not Pavel), with Pavel checking the repo organisation; a review meeting was set for the following Wednesday with Ivan invited. [[raw/practice_release_calle_ocho-github-october-21-2025.md]]

## The release-manager role (Ivan) and the GLI handoff

- [[wiki/people/ivan.md|Ivan]] watches for a release that passed lint/test/build, judges whether it is genuinely ready, hands the candidate to human game-play testing, then packages the exact tagged version and takes it to **GLI** for certification (a manual email/phone process). He is the **liaison** between JVL and GLI and manages the **cost of each submittal**. Aaron noted **Eclipse** is an organisation similar to GLI. Ivan's old habit of tracking release numbers in Jira plans is being dropped — he now references GitHub. [[raw/releases_github-october-21-2025.md]]

## Legacy vs new ecosystem

- JVL runs **two parallel ecosystems**: a **legacy** one (games built on **Jenkins**, previews shared via **Dropbox**) and the **new** one where Omni games are compiled *and* distributed in GitHub. Dropbox was "a gut measure" until GitHub is implemented; **Jenkins goes away** once all production moves to GitHub. Val's rule for these discussions: define the new ways only — the old ways will "live themselves out of relevance." [[raw/releases_github-october-21-2025.md]]

## Open questions

- **Where do large graphic files (LFS) live for releases?** Val recalled agreeing to move big graphic assets to separate cloud storage (he floated Azure / "blob") to avoid cluttering GitHub; [[wiki/people/andrey-bosik.md|Andrei]] stated **LFS is part of the GitHub repository**. Accounts diverge; unresolved. Related: artifacts currently sit on a **local Nexus server**, and Val ruled to **keep Nexus local for now** (cloud Nexus needs a financial commitment JVL isn't sure it needs), accepting a later action-rewrite when JVL migrates to cloud. [[raw/artifacts_assembly_GitHub-october-21-2025.md]] [[raw/practice_release_calle_ocho-github-october-21-2025.md]]

## Sources

- [[raw/releases_github-october-21-2025.md]]
- [[raw/artifacts_assembly_GitHub-october-21-2025.md]]
- [[raw/practice_release_calle_ocho-github-october-21-2025.md]]
