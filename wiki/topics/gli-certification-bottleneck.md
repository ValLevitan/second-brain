---
type: topic
title: GLI certification cost and speed (the scaling bottleneck)
date: 2026-07-12
aliases: [game certification, GLI approval, math testing, GLI automation, RiskCherry, certification cost]
source-count: 4
---

# GLI certification cost and speed (the scaling bottleneck)

Getting each game approved by the testing lab GLI is slow and expensive. Val sees this as the single biggest thing that could stop JVL from scaling up game production, even if everything else goes to plan.

## The core problem

- JVL wants to publish about one game a week; even at that pace (before any real growth), the cost of approving each game through GLI is described as "ridiculously expensive." [[raw/gli_visit-jan-7-2025.md]]
- Val's point: even if JVL reaches the production scale it hopes for, if games can't get through GLI quickly and cheaply, "all the scalability is nothing." Each game becomes a bottleneck shipped to GLI at, for example, 20 hours at $170/hour. [[raw/gli_visit-jan-7-2025.md]]
- The 2025 strategic plan frames the same idea as a speed-to-market advantage JVL is trying to build, and lists a "robust virtual tool between us and GLI" as a goal. [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]]

## Math testing is the expensive part

- Math testing is the most labour-intensive stage of Class 3 approval — Dan at GLI measures it at close to 20 hours. [[raw/gli_visit-jan-7-2025.md]]
- Val's argument: math is a science, "purely binary" — you test inputs and outputs, not formulas — so the odds are the same whether the game is land-based or online. Approving the math should therefore be one action at one cost, regardless of the on-screen presentation. [[raw/gli_visit-jan-7-2025.md]]
- JVL proposes to prepare and submit the math data (RNG/RTP ranges) in whatever format GLI needs, so GLI can feed it straight into its computer and skip the slow data-creation step. [[raw/gli_visit-jan-7-2025.md]]

## What Val is asking GLI for

- A shared **taxonomy**: break down Class 3 billing into named stages, show how many hours go into each, then tackle automating the most labour-intensive stages first. Val says he cannot get this breakdown out of GLI despite asking many times. [[raw/gli_visit-jan-7-2025.md]]
- A clear answer on **tooling/automation**: either GLI accepts JVL's own automation tooling (which GLI would then verify and certify), or GLI tells JVL to build its own and GLI charges for verifying it — but Val cannot get GLI to commit to either path. [[raw/gli_visit-jan-7-2025.md]]

## The "base approval / transfer" idea

- A game approved once to the GLI-11 standard could move to other markets as a cheaper "transfer," paying only for each market's extra local rules; for online the relevant standard is "19." A book of GLI-11-approved games would then only cost the transfer fee per new market. [[raw/gli_visit-jan-7-2025.md]]

## Why GLI is guarded ("proprietary")

- As an independent, accredited lab, GLI must not coach a client on how to pass its tests. That neutrality is why GLI pulls back and calls things "proprietary" — not the ordinary trade-secret meaning. [[raw/gli_visit-jan-7-2025.md]]

## Build approach to ease GLI review

- Under the new build system, JVL plans to submit a **non-instrumented** build to GLI plus a documented procedure for installing the instrumentation — so GLI can do a lighter review and inspect the instrumentation only if it wishes. See [[wiki/decisions/2025-01-15-reduce-build-variants-with-post-build-instrumentation.md]]. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

## Alternative labs and certification economics (Jan 30, online games)

- **RiskCherry** — an alternative certification lab evaluated for the online-games side. Its total cost came out about the same as GLI (slightly cheaper); its pitch is speed — ~2 weeks for a pack of 10 games versus GLI's ~3. Val's takeaway: certification prices are just "what the market is" right now. [[raw/Recap with Andrei Klimovich - January 30, 2025.md]]
- **Val's payback rule:** a per-game certification spend (~$2,500/game for online) must pay back in ~3–5 months, not a year; because cert cost can't be spread across other markets, it must be recovered from that one game in that one market — driving the push to re-negotiate revenue share (~5% up toward 8–10%) in regulated markets. See [[wiki/topics/online-games-rgs-distribution.md]]. [[raw/Recap with Andrei Klimovich - January 30, 2025.md]]

## Sources

- [[raw/gli_visit-jan-7-2025.md]]
- [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]]
- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- [[raw/Recap with Andrei Klimovich - January 30, 2025.md]]
