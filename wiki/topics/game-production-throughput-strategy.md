---
type: topic
title: Game production throughput strategy (Val's "much faster" push)
date: 2025-03-12
aliases: [developing games faster, production throughput, game a month, game a week, parallel tracks, disjoint animation, zero to GLI, production time, scaling game output]
open-questions: 2
source-count: 5
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

## Origin — the Feb 10 two-branch plan

The parallel-track idea predates the Mar 12 Gottlieb call: on the Feb 10 GitHub-structure meeting Val already stated the plan to "split [[wiki/people/lena.md|Lena]]'s responsibilities and move her to assistant or deputy game producer" and put "**Julia on LAN-based and Anastasia on online**… so these two branches will start growing separately," alongside "I am planning to put a lot of scaling into this" (a clean, separate game-development GitHub org he can drive "hard for efficiencies"). See [[wiki/meetings/2025-02-10-github-repo-structure-part-1.md]]. [[raw/github _structure-pavel-aaron-andrei.md]]

## The art-team scaling debate (parked)

- Val proposed running **Anastasia and Julia** as art directors in parallel to **Lena**, each dedicated to a market (Georgia, South Dakota, a junior on Puerto Rico), leaving Lena for class-three — to multiply output. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- Michael resisted: **Lena consistently makes better decisions**, her sensibility is "outstanding," and handing a whole game to a junior risks **a month of rework** (14–16 revisions) against hard deliverable dates. He denied Lena is a control freak — she gives **top-line direction and lets the team run** (the **Crescent City Carnival** fireworks and the "precognitions" were the team's ideas, not Lena's) — but insisted she must at least **review** everything. They agreed to **test the theory** by assigning a Mexican-theme comp art (the **"5X Peppers"**, or turning **Pink Princess** into **"La Rosa"**) to Anastasia. See [[wiki/people/lena.md]] and [[wiki/people/michael-gottlieb.md]]. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## Related

- Michael's blunt "online is unwinnable" assessment from the same call is captured on [[wiki/topics/online-games-rgs-distribution.md]] (Val's "Netflix for games" counter-idea too). [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- The Peach 3/4 "finished but not deployed" exchange is on [[wiki/projects/georgia-market-rollout.md]]. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## Apr 17–18 2025 — "never reach optimal" and estimate-per-person-first

- On the Apr-17 game-development conversation ([[wiki/meetings/2025-04-17-game-development-omni-port-strategy.md]]) Val added a **management caution** to the speed push: don't chase perfection at the cost of exhausting people — "sometimes companies get exhausted from perfection… in this business it's very dangerous to exhaust people, then you're gonna lose them." He puts a hard deadline on the Calle Ocho→Omni port (accepting throw-away work), offering a **contractor** as the escape valve ("hire a contractor… I don't mind paying") so the team isn't in overdrive for months. Michael backed the ship-imperfect-now stance with the **Sega Dreamcast 1995** precedent (shipped on one of two SH-2 processors, added the second later). [[raw/game_development_update-apr-17-2025.md]]
- On the Apr-18 Miro estimation call ([[wiki/meetings/2025-04-18-games-production-time-estimation.md]]) Val worked his throughput method concretely: estimate **time-per-person first**, then lay operations out on a **parallel** schedule to find the resource bottleneck ("if all done sequentially the game would take two years"). Lena confirmed the art critical-path (**Dima, Nastya, Yulia**) already runs fully parallel and independent. Detail on [[wiki/topics/game-art-animation-production-pipeline.md]]. [[raw/games_production-apr-18-2025.md]]

## Nov 11 2025 — the "generate games from a specification" endgame (told privately)

On the Nov-11 graphics-specification call ([[wiki/meetings/2025-11-11-graphics-specification-for-testing.md]]; Val, [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]]) Val revealed the *why* behind pinning down a graphics specification (the QA/testing mechanics are on [[wiki/topics/game-art-animation-production-pipeline.md]]): testing is not the real target — **learning to produce games automatically from a description** is. He told Pavel and Irina explicitly to **keep this to themselves** and not raise it with Lena's team ("it scares them… it doesn't help me get anywhere"). [[raw/Specs_graphics.md]]

- **The bet.** If JVL agrees a **taxonomy / set of specification elements** that the art team can easily hand over (and that JVL needs anyway for testing), then a game's initial layout, transitions and assembly can be described in a fixed, machine-readable form — and Val believes he "could put out a game within a month," graphics and assembly included. **Time transitions are part of the specification** and can be passed through the same manifest into testing. [[raw/Specs_graphics.md]]
- **Cloning is the volume play.** What Val wants is largely **game cloning** — he estimates roughly **9 different themes per mechanic** and "**10 to 1**": for each proven mechanic/math, spin up many reskins (a couple of Asian themes, a couple of American, a mid-western, animal themes — wolves/horses/buffalo/cowboys, etc.). [[raw/Specs_graphics.md]]
- **Repaint the aging catalog.** Symbols **age visually**; a game with good math but a dated look can be **repainted while keeping the exact mechanics and math**, "with very little effort," *if* JVL holds the precise **production specification** — Val's analogy: North American films remade every 30–40 years on the same story. [[raw/Specs_graphics.md]]
- **How.** Speculative AI angle only: feed an AI the comp art + the structured scene (components, hierarchy, positions) and have it generate/re-theme elements (e.g. re-skin a Chinese theme into a Western one at pixel level) — Val stressed this is a "wild idea… something turning in my head," not a committed method. [[raw/Specs_graphics.md]]

This extends the throughput doctrine on this page (serial→parallel, feature-level forecasting, ship-imperfect) from *making each game faster* toward *not hand-making most games at all*. Nothing was decided.

## Open questions

- Nothing was decided — Val closed with "I'm going to think about it. We'll have another conversation on this." Whether JVL adopts the two-team split, the parallel-track/disjoint-animation model, or the junior-art-director experiment is unresolved. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- Automated game generation / cloning from a specification (Nov-11): the taxonomy of specification elements JVL would need is not yet defined, and whether an AI-driven re-skin pipeline is feasible is unknown — Val deferred it. [[raw/Specs_graphics.md]]

## Sources

- [[raw/github _structure-pavel-aaron-andrei.md]]

- [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- [[raw/game_development_update-apr-17-2025.md]]
- [[raw/games_production-apr-18-2025.md]]
- [[raw/Specs_graphics.md]]
