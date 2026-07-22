---
type: meeting
title: Practice release of Calle Ocho — dry-run the Omni build with Ivan, keep Nexus local for now (Oct 22 2025)
date: 2025-10-22
aliases: [Calle Ocho practice release, Kaya Ocho build, practice release GitHub, Ivan Shpakov, two build actions, sources to binary to ISO, local Nexus artifacts]
source-count: 1
---

# Practice release of Calle Ocho — dry-run the Omni build with Ivan (Oct 22 2025)

**Date:** 2025-10-22 · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/pavel.md|Pavel Frolov]]. ~6m. Russian.

**Dating note (§11):** the filename says `october-21`; the recording header dates the session **2025-10-22** (recording stamp `20251022_095156`; the header's typed time reads "01:51pm" while the stamp reads 09:51 — an AM/PM ambiguity that does not affect the date). Header/recording date (Oct-22) is taken over the filename. Recording title: `process_releases_organization_GitHub`.

The plan-of-attack for a **practice release** of the Omni game **Calle Ocho** (transcribed "какая очередь"/"Kaya Ocho"), continuing the release-management thread. Substance rolls up to [[wiki/topics/github-release-management-pipeline.md]]. §15.8: no compensation material.

Durable points (single source):

- **The exercise: assemble Calle Ocho at framework level, driven by Ivan, not Pavel.** Val wants the Omni Calle Ocho game assembled in whatever condition it is in today — but done by **"Иван шпаков" ([[wiki/people/ivan.md|Ivan Shpakov]])**, with [[wiki/people/pavel.md|Pavel Frolov]] standing aside to answer questions and check whether the physical repositories are organised correctly. This is a deliberate dry-run of the release-manager flow. [[raw/practice_release_calle_ocho-github-october-21-2025.md]]
- **Two build actions.** (1) Build the **binary files from text/source files** — done by the developer during assembly of game pieces; specialists like **[[wiki/people/irina-makarych.md|Irina Makarych]]** help. (2) Assemble the **ISO game image from the binary files**. Val confirmed the two-stage understanding with Andrei and Pavel. [[raw/practice_release_calle_ocho-github-october-21-2025.md]]
- **Ivan marks the release candidate after full tests.** Pavel's correction: any developer can build sources locally or via an action and download the artifact, but **finally marking an artifact as field-ready must be done by [[wiki/people/ivan.md|Ivan]]** — he marks it, or runs a separate build action with **deeper testing (the full test list)**; only after all tests pass is the build marked a **release candidate**. [[raw/practice_release_calle_ocho-github-october-21-2025.md]]
- **Artifacts sit on a local Nexus server — decision to keep it local for now.** Pavel's one dissatisfaction: build artifacts are currently stored on JVL's **local Nexus server**, and most actions would need rewriting to put binary artifacts in the cloud. Val's ruling: **stay on local Nexus for now** — moving Nexus to its cloud version needs a financial commitment JVL isn't sure it needs; accept that the actions will have to be rewritten later when JVL migrates to cloud. (Feeds the artifact-repository question on [[wiki/topics/jfrog-artifactory-artifact-management.md]].) [[raw/practice_release_calle_ocho-github-october-21-2025.md]]
- **Next step:** Val gave the team a week to walk this path and scheduled a meeting **next Wednesday** to review how the Calle Ocho build is done and where everything lives; he will **invite Ivan**. [[raw/practice_release_calle_ocho-github-october-21-2025.md]]

## Sources

- [[raw/practice_release_calle_ocho-github-october-21-2025.md]]
