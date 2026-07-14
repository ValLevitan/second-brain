---
type: topic
title: Game production throughput strategy (Val's "much faster" push)
date: 2025-03-12
aliases: [developing games faster, production throughput, game a month, game a week, parallel tracks, disjoint animation, zero to GLI, production time, scaling game output]
open-questions: 1
source-count: 1
---

# Game production throughput strategy (Val's "much faster" push)

[[wiki/people/val-levitan.md|Val]]'s drive to compress how long it takes JVL to produce a game, and the approach he and [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] worked through on Mar 12 2025. Distinct from the design principles ([[wiki/topics/slot-game-design-principles.md]]) and the art pipeline ([[wiki/topics/game-art-animation-production-pipeline.md]]) it is trying to accelerate; overlaps the AI/automation and pipeline themes ([[wiki/topics/ai-assisted-development.md]], [[wiki/topics/build-pipeline-parameterization.md]]). [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## The goal

- Val's stated target: produce **at a minimum a game a month** (land-based) **plus a game a week for online**. To do it he wants **two separate teams** — one for land-based games, one for online. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- He is not chasing a 10% gain — he repeatedly framed it as wanting to be **"50, 60, 70 percent" faster**, achieved by breaking every process into small steps and asking how each can be done differently ("nothing should be left to convention"). [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- Val wants to **scale with the same or fewer people**, not hire a larger team — "be more nimble… as compressed as we could possibly" in decisions. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## Michael's reality check on speed

- Michael said he **cannot design or even copy a game per week**; when he did online games before, they were producing **a game every four to six months**. He had no template for a weekly cadence. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- He explained that going from Val's vision to the approved comp art is only about **"six or 7% of the entire game"** — the real heavy lift is the **massive amount of assets** (symbol animations, base-game animations, transitions, mechanic behaviours). The **iteration** loop is fast (8–10 tweaks in a single day) and is *not* the bottleneck. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- The mechanic drives the art: e.g. an **expanding-wild** symbol must be designed so it makes sense expanded (a palm tree that grows into a full palm tree), and whether a "wild" word repeats when it expands. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## Where Val wants to squeeze — the two big time savings

Val defined "output" narrowly as **production time from requirement to commit** ("zero to GLI"). The two levers: [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

1. **Get from vision/concept to an approved comp art in the first try.** [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
2. **Disjoint animation from comp art** — have the animations done **in parallel by different people** while Michael reviews — and **assemble the game for Michael's first view** (reels up and spinning, with placeholders and the math already implemented) in **days, not months**. Michael today has to "design blind," imagining the game in his head because it takes so long to get from comp art to reels spinning. If a game reuses the **same mechanics and same math** (a clone), the math should "drop right in" immediately. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## Serial → parallel, and Miranda

- Development today is **serial** (game mechanics → math → comp art → integration). Val wants to put mechanics/math on **parallel tracks** to comp art. Michael pushed back that on Fortune Foo Paws math and comp art already ran simultaneously. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- **Miranda 8** is deployed; **Miranda 9** will "play all the math in real time," which Val expects to expedite dramatically. He floated **contracting out the math** (or the game mechanics) so a stable mechanic is just "branched out." [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## Eliminating the engineering bottleneck

- Val argued the recent slowdown was **not** the departure of **Valentin** (a strong **C++** programmer on the *old* framework, not an integration engineer) but the **migration from the C++ platform to an HTML platform** plus broken/crashing builds and bad commits — a **development-pipeline** problem he intends to **automate** (commits automatically tested when made). [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- He predicted that **"programmers will no longer be necessary 12 months from now"** and that with the new framework JVL **"will not need integration developers"** — only "one or two people, one and a half" whom it employed for that, not expensive. He said he writes scripts himself through a "human interface" knowing nothing about programming. The combination of **Miranda + the new framework + the changed deployment cycle** is what removes the integration programmers. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- **Just-in-time testing:** testing moves *into* integration (write test scripts from the requirements, forward-load environments) instead of a serial pass at the end; testers are kept, redeployed mid-process. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## The art-team scaling debate (parked)

- Val proposed running **Anastasia and Julia** as art directors in parallel to **Lena**, each dedicated to a market (Georgia, South Dakota, a junior on Puerto Rico), leaving Lena for class-three — to multiply output. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- Michael resisted: **Lena consistently makes better decisions**, her sensibility is "outstanding," and handing a whole game to a junior risks **a month of rework** (14–16 revisions) against hard deliverable dates. He denied Lena is a control freak — she gives **top-line direction and lets the team run** (the **Crescent City Carnival** fireworks and the "precognitions" were the team's ideas, not Lena's) — but insisted she must at least **review** everything. They agreed to **test the theory** by assigning a Mexican-theme comp art (the **"5X Peppers"**, or turning **Pink Princess** into **"La Rosa"**) to Anastasia. See [[wiki/people/lena.md]] and [[wiki/people/michael-gottlieb.md]]. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## Related

- Michael's blunt "online is unwinnable" assessment from the same call is captured on [[wiki/topics/online-games-rgs-distribution.md]] (Val's "Netflix for games" counter-idea too). [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- The Peach 3/4 "finished but not deployed" exchange is on [[wiki/projects/georgia-market-rollout.md]]. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## Open questions

- Nothing was decided — Val closed with "I'm going to think about it. We'll have another conversation on this." Whether JVL adopts the two-team split, the parallel-track/disjoint-animation model, or the junior-art-director experiment is unresolved. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## Sources

- [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
