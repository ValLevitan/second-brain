---
type: topic
title: JFrog Artifactory and artifact/binary management
date: 2025-02-06
aliases: [JFrog, Artifactory, JFrog Connect, artifact repository, binary management, LFS, ISO image storage, SCA, software bill of materials, artifact storage dilemma, Sonatype, Nexus]
source-count: 2
open-questions: 1
---

# JFrog Artifactory and artifact/binary management

JVL's evaluation of **JFrog Artifactory** for managing binaries and build artifacts, part of the wider Git-migration + build-pipeline modernization. Discussed in a Feb 6 2025 sales call with a JFrog rep ("Eddie"), attended by Val and [[wiki/people/andrey-bosik.md|Andrei]]. [[raw/JFrog transcript - February-6-2025.md]]

## The GitHub + JFrog split (as pitched)

- **GitHub** = the experts in **source-code management / version control** and the build pipeline (GitHub Actions) — JVL's **first-party code**. **JFrog** = the experts in **binary / third-party management** — the ~80% of code that comes from **open-source libraries**. The two are pitched as complementary (there is a GitHub–JFrog partnership with OIDC integration), covering the flow from build to deploy-on-the-casino-floor hardware. [[raw/JFrog transcript - February-6-2025.md]]
- **Artifactory** caches open-source dependencies locally so GitHub Actions pulls them from Artifactory instead of the open internet on every build, then pushes the built deployable artifact back into Artifactory. [[raw/JFrog transcript - February-6-2025.md]]
- **JFrog Connect** can deploy software onto Linux hardware in the field and do over-the-air updates / fleet management at scale. For the online side, an artifact can be scripted straight into Kubernetes from Artifactory. [[raw/JFrog transcript - February-6-2025.md]]
- Security scanning is split: **GitHub Advanced Security** scans first-party code; JFrog's **SCA** (software composition analysis) + **software bill of materials** covers the third-party/open-source dependencies. [[raw/JFrog transcript - February-6-2025.md]]

## JVL's current (archaic) deployment and its constraints

- Today JVL pulls libraries into internal storage, packages on an internal server, writes the build to a **USB stick that is SHA-signature-protected**, and ships it to a **testing laboratory** for **legislative-compliance** sign-off (not code/QA testing); the same SHA key then goes to the casino floor. Val wants to change this — e.g. send the lab a link to burn their own USB rather than FedEx a stick — and wants to modernise every process. [[raw/JFrog transcript - February-6-2025.md]]
- JVL runs **three regulatory tiers**: (1) the hard, legislatively-restricted land-based machine business (no live updates); (2) online casinos (less restricted); (3) the **financial-processing hardware EFT module** on the machine (least controlled — could do live updates). [[raw/JFrog transcript - February-6-2025.md]]

## The three storage problems JVL still has

Val flagged these as real, separate issues to solve (artifact-repository choice being a recurring subject):

- **Artifact storage** — where to store build/deployable artifacts. [[raw/JFrog transcript - February-6-2025.md]]
- **LFS (large file storage)** — currently on **local drives**; JVL is unsure how to work with it. [[raw/JFrog transcript - February-6-2025.md]]
- **ISO-image archive** — every published slot-machine **ISO image must be preserved**, so JVL needs a repository/archive of every ISO it ever produced. Val wants to store ISO images on **Azure**. [[raw/JFrog transcript - February-6-2025.md]]

## Commercial terms discussed

- **Enterprise X** starting point ≈ **$21,000/year** for ~1 TB: **$9,000 license** + **$12,000 consumption** (consumption = storage + data transfer, billed at **$1/GB** at the 1 TB tier; data transfer can push it above $12k). Enterprise X includes **SSO** (GitHub OIDC or Entra ID), technical support, and SCA. [[raw/JFrog transcript - February-6-2025.md]]
- **Pro** is a credit-card subscription (no annual commitment): $150 for 25 GB included, then **$1.25/GB** (GB 26 → 1.2 TB). No SSO. Below 1 TB the Enterprise rate rises to ~$1.25–$1.56/GB; economy of scale only kicks in at Enterprise ≥1 TB. Rep's recommendation: try Pro for ~6 months to learn real consumption, then convert to an annual Enterprise agreement. [[raw/JFrog transcript - February-6-2025.md]]
- JVL's app sizes were estimated at roughly a **terabyte**. JVL wants hosting on **Azure** (aligning with GitHub/Microsoft), not the AWS default; its AWS is in Canada/Europe/Singapore, so this would be the Canada region if AWS. [[raw/JFrog transcript - February-6-2025.md]]

## Where it stands

- Val and Andrei made **no decision** — they said they already expected these capabilities and their real question is **which package** (Pro vs. Enterprise) and how the GitHub/JFrog pieces fit together. The rep (contact **Eddie**) is to send a written recap, the $21k proposal, and calculation details. Artifact-storage choice was explicitly parked for a separate meeting. [[raw/JFrog transcript - February-6-2025.md]]

## The Sonatype / Nexus alternative (Feb 12)

- JVL already runs **Nexus Repository OSS (community), self-hosted, v3.17** as its artifact repository (Jenkins pushes to it). On Feb 12 Val and Andrei took a **Sonatype** sales/discovery call to evaluate a **cloud SaaS** Nexus — the more-comfortable migration path from their current Nexus install. See [[wiki/organizations/sonatype.md]]. [[raw/sonotype_meeting_feb-12-2025.md]]
- Sonatype's own Nexus **SaaS is GA July 1 2025** (~$10k/yr); before that a partner (Saltworks) hosts Pro-SaaS for ~3 months, then Sonatype takes it over. SaaS requires Pro. JVL wants a one-year trial term. [[raw/sonotype_meeting_feb-12-2025.md]]
- So JVL is weighing two artifact-repository directions: **JFrog Artifactory** (universal binary management, GitHub+JFrog split) vs. staying on **Sonatype Nexus** but moving it to cloud SaaS. No decision on either. Val again noted large graphic files / **LFS** likely fall outside a Nexus-style artifact repo (and are being handled via Git LFS — see [[wiki/topics/ai-assisted-development.md]]). [[raw/sonotype_meeting_feb-12-2025.md]] [[raw/JFrog transcript - February-6-2025.md]]

## Open questions

- Which JFrog package does JVL actually need (Pro vs. Enterprise X), and where does the line fall between GitHub's and JFrog's capabilities? (Val's stated core confusion.) [[raw/JFrog transcript - February-6-2025.md]]
- JFrog Artifactory vs. Sonatype Nexus SaaS as JVL's artifact repository — no decision taken on either. [[raw/sonotype_meeting_feb-12-2025.md]]

## Sources

- [[raw/JFrog transcript - February-6-2025.md]]
- [[raw/sonotype_meeting_feb-12-2025.md]]
