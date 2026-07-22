---
type: meeting
title: Flex-OS-installer manifest and final-image artifact assembly (Oct 22 2025)
date: 2025-10-22
aliases: [flex os installer, platform flex os installer, artifact assembly, manifest file, component checksum, LFS storage, artifacts assembly GitHub]
source-count: 1
---

# Flex-OS-installer manifest and final-image artifact assembly (Oct 22 2025)

**Date:** 2025-10-22 · **Attendees:** [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrey-bosik.md|Andrei Bosik]]. ~7m. Russian.

**Dating note (§11):** the filename says `october-21`, but the recording header dates the session **2025-10-22** (recording stamp `20251022_094447`; the header's typed time reads "01:44pm" while the stamp reads 09:44 — an AM/PM ambiguity that does not affect the date). Header/recording date (Oct-22) is taken as the meeting date over the filename. Recording title: `process_releases_organization_GitHub`.

A short walkthrough continuing the Oct-21 release-management thread. Substance rolls up to [[wiki/topics/github-release-management-pipeline.md]]. §15.8: no compensation material.

Durable points (single source):

- **The `platform flex os installer` project does the final assembly.** [[wiki/people/pavel.md|Pavel]] showed the project that assembles all components into the **final installable image** for a machine. It holds a **manifest file** (still an early "зачаток"/seed of the manifest) that declares **which components make up the final product**. This is the "platform flex back end" installer layer named in the Sept-2025 repo-taxonomy work (see [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]]). [[raw/artifacts_assembly_GitHub-october-21-2025.md]]
- **Per-release version pinning; components vary by package.** On release, [[wiki/people/ivan.md|Ivan]] must fill in the manifest with the **specific version of each component** for that build (e.g. the July build). Components are *not* always identical: a single game reuses the same components, but a **Georgia multi-game package** lists a distinct component per game (Val: likely including the **multi-game screen** as one component, plus e.g. six games, each with its own checksum). [[raw/artifacts_assembly_GitHub-october-21-2025.md]]
- **Checksum-guarded assembly.** A line in the manifest can specify the **checksum of a binary artifact**; if the build can't find that artifact by checksum, it **errors** — so if the source components are placed on the agreed "shelf," the game assembles correctly. [[raw/artifacts_assembly_GitHub-october-21-2025.md]]
- **There is an existing industry methodology to adopt.** Val was confident a well-developed release-management methodology/standard already exists (designers place things on a shelf, the release manager takes from it) — JVL just needs to read and adapt it; he asked what standard to look at, and recorded the session so he could be pointed to one. [[raw/artifacts_assembly_GitHub-october-21-2025.md]]
- **Open item — where large graphic files (LFS) live.** Val recalled agreeing to pull big graphic files from separate cloud storage (he floated Azure / "blob") to avoid cluttering GitHub; [[wiki/people/andrey-bosik.md|Andrei]] said **LFS is part of the GitHub repository** (for large files). The two accounts diverge on whether LFS assets stay in GitHub or move to separate storage — left unresolved. (Relates to the artifact/large-file-storage question on [[wiki/topics/jfrog-artifactory-artifact-management.md]].) [[raw/artifacts_assembly_GitHub-october-21-2025.md]]

## Sources

- [[raw/artifacts_assembly_GitHub-october-21-2025.md]]
