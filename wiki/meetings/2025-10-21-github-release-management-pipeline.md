---
type: meeting
title: GitHub release management — the concept→design→production repo lineage and the CI/CD release pipeline (Oct 21 2025)
date: 2025-10-21
aliases: [release management Oct 21, release pipeline, GitHub Actions releases, Ivan release manager, GLI handoff, concept design production lineage, submodule production repo, Kaya Ocho release]
source-count: 1
---

# GitHub release management — repo lineage and the CI/CD release pipeline (Oct 21 2025)

**Date:** 2025-10-21 (12:49pm) · **Attendees:** [[wiki/people/aaron.md|Aaron Bockelie]], [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrey-bosik.md|Andrei Bosik]]. 55m. English.

The core meeting where Aaron lays out how a JVL release is produced and managed inside GitHub — the repository lineage from concept to production, the automated build/release pipeline, and where [[wiki/people/ivan.md|Ivan]]'s release-manager job fits. Substance is synthesised on [[wiki/topics/github-release-management-pipeline.md]]; the repo-lineage rulings this builds on live on [[wiki/decisions/2025-02-21-separate-game-and-design-repos.md]] and [[wiki/decisions/2025-03-12-fork-game-repos-from-generic-template.md]]. §15.8: no compensation material.

Durable points (single source — see the topic page for the full synthesis):

- **Repository lineage: concept (eternal) → design (sparse fork) → production (from template + submodule).** A single **game-concept repository** holds every game concept and lives forever; when a concept is promoted, JVL **sparsely forks just that one directory** into a **game-design repository** and builds the design there; the **production repository** is created from a **master production template** and the design work is attached as a **git submodule** (a reference/"symbolic link" back to the still-standing design repo, giving traceability concept→design→production). [[raw/releases_github-october-21-2025.md]]
- **The automated pipeline: lint → test → build → release.** In the production repo a `.github/actions` directory holds actions that watch for pushes; on each commit the pipeline runs **linting** (stops everything if it fails) → **tests** → **build** → and if all pass can **deploy/release**. [[raw/releases_github-october-21-2025.md]]
- **A release is a bundle of artifacts tagged to one immutable version.** Artifacts (ISO, EXE, zip, and a **PDF instruction book compiled from the markdown docs**, plus links to an online-play build) are stored as GitHub release artifacts, each tagged to a **unique, immutable commit hash / version** that can never be reproduced-and-changed. Aaron showed **OBS Studio** and **RustDesk** GitHub releases pages as "the vision." [[raw/releases_github-october-21-2025.md]]
- **Ivan's release-manager role.** [[wiki/people/ivan.md|Ivan]] watches for a viable release that has passed lint/test/build, decides whether it is really ready, hands the candidate to human game-play testing, then packages the exact tagged version and sends it to **GLI** for certification (a manual email/phone process). Ivan is the **liaison** between JVL and GLI and manages the **cost** of each submittal (his old habit of putting release numbers in Jira plans is being dropped — he now references GitHub). Aaron: **Eclipse** is an organisation similar to GLI. [[raw/releases_github-october-21-2025.md]]
- **Two parallel ecosystems; Dropbox and Jenkins are legacy stopgaps.** Val stressed JVL runs a **legacy ecosystem** (games built on **Jenkins**, EXEs shared via **Dropbox**) alongside the **new ecosystem** — new Omni games are compiled *and* distributed in GitHub. He forbade modifying the old ways for this conversation; Dropbox was "a gut measure" until GitHub is implemented; Jenkins goes away when all production moves to GitHub. [[raw/releases_github-october-21-2025.md]]
- **Release = collection of artifacts (worked example).** For a Class-3 single game, the release is one game (**Kaya Ocho** / "Calle Ocho" — the first Omni game). For **Georgia** the release is a **multi-game** package: a **multi-game selection screen** component plus (e.g.) six games, each with its own checksum, all under one version number (Aaron's "version 6.5"). Aaron's assembly-line picture: each piece (game, Linux OS, back-end/CMS) is individually runnable, and an **integrator repo** watches for new releases of the pieces and auto-assembles the ISO — "continuous delivery," the DevOps approach. [[raw/releases_github-october-21-2025.md]]
- **Andrei's open questions (carried into the Oct-22 sessions).** What exactly is the *final* artifact (an installable ISO image built from many artifacts), how release **documentation** attaches to an artifact (a PDF built from markdown), and who assembles the final image ([[wiki/people/pavel.md|Pavel]] knows which components/hardware **drivers** must be included — manifests per hardware/build target). Val asked to trace **Kaya Ocho** through a real GLI submission, but Andrei said he could not point to where Ivan should look — deferred to the Oct-22 walkthrough with Pavel. [[raw/releases_github-october-21-2025.md]]
- Val's candid framing: "I am not an engineer… I don't understand 70% of what's been said," but trusts Aaron and uses Aaron/Andrei to orient where to push the team. [[raw/releases_github-october-21-2025.md]]

## Sources

- [[raw/releases_github-october-21-2025.md]]
