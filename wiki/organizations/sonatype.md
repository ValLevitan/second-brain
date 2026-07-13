---
type: organization
title: Sonatype (Nexus Repository)
date: 2025-02-12
aliases: [Sonatype, Sonotype, Nexus, Nexus Repository, StoneTech, Stone Tech]
source-count: 1
---

# Sonatype (Nexus Repository)

Sonatype makes **Nexus Repository**, the artifact-repository software JVL already uses (self-hosted) and evaluated for a cloud (SaaS) upgrade. Discussed in a Feb 12 2025 sales/discovery call with two Sonatype reps, attended by [[wiki/people/val-levitan.md|Val]] and [[wiki/people/andrei.md|Andrei]]. [[raw/sonotype_meeting_feb-12-2025.md]] (The transcript spells it "Sonotype"; a rep also said "Stone Tech," likely a mis-transcription — kept as aliases.)

## The reps

- **Johnny Berry** — account manager, five years at the company. [[raw/sonotype_meeting_feb-12-2025.md]]
- **Alex Patel** — senior solutions architect (technical demos, deep dives, proof of concept). [[raw/sonotype_meeting_feb-12-2025.md]]
- Home base Maryland; a remote company (Knoxville, Tennessee; New Hampshire). [[raw/sonotype_meeting_feb-12-2025.md]]

## JVL's current use and what it wants

- JVL runs **Nexus OSS (community) as its artifact repository, self-hosted, version 3.17** (well behind the current ~3.78). It uses Jenkins to push, ~15 people (mostly via Jenkins) pushing/pulling; ~15 graphic designers + ~7 developers. [[raw/sonotype_meeting_feb-12-2025.md]]
- JVL wants a **cloud SaaS** artifact repository ("SaaS is very important for us") as it migrates its new omni-platform initiative off SVN/local servers to a cloud environment — see [[wiki/topics/jfrog-artifactory-artifact-management.md]]. Val also flagged that large graphic files / **LFS** likely fall outside Nexus's scope. [[raw/sonotype_meeting_feb-12-2025.md]]

## What Sonatype offered

- Sonatype's own **Nexus SaaS** general-market release is **July 1 2025**; before that they only offer self-hosted Pro. Interim option: a **partner** (named **Saltworks**) hosts a Pro SaaS instance for ~3 months, then Sonatype migrates it to its own SaaS on July 1 with no disruption to JVL. [[raw/sonotype_meeting_feb-12-2025.md]]
- SaaS **requires Pro** (SaaS needs support and features like external Postgres for HA/zero-downtime; there is no "community SaaS"). [[raw/sonotype_meeting_feb-12-2025.md]]
- Price: **~$10,000/year** for the Sonatype-hosted SaaS instance after July 1, plus a to-be-quoted charge for the 3-month partner-hosted interim. JVL wants a **one-year** term (to try first), never 3–5 years. [[raw/sonotype_meeting_feb-12-2025.md]]
- Val insisted the next step is a **technical alignment** between Andrei and the rep to match advertised features to JVL's actual requirements ("they don't always match"), rather than a business/pricing meeting. Johnny to send a written recap with partner options, timelines, and one all-in price. [[raw/sonotype_meeting_feb-12-2025.md]]

## Sources

- [[raw/sonotype_meeting_feb-12-2025.md]]
