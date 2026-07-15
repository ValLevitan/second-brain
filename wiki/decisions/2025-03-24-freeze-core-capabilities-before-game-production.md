---
type: decision
title: Game production works only with frozen core capabilities
date: 2025-03-24
aliases: [frozen capabilities rule, no engine changes during production, stable capabilities, golden rule of game production]
status: active
source-count: 2
---

# Game production works only with frozen core capabilities

**Decision (Val, with Aaron, ~Mar 24 2025 — date inferred, "Monday morning" content + Mar 25 transcription stamp):** a game production is cut from a tested core snapshot and **cannot request engine/framework changes during production** — "This game cannot possibly have… a feature that it doesn't have." New capabilities are developed on the core-advancement lines and picked up by later games (or pulled in early at known integration cost, only near a production's start). [[raw/devops_container_approach_for_omni.md]]

## What was decided

- Production "always works with stable features… stable capabilities"; all capabilities are frozen before game production starts. A game concept may *create requirements* for new framework capabilities — those are built on the core side, released, and used "not in this game." [[raw/devops_container_approach_for_omni.md]]
- Aaron's framing (next-day continuation), which matches Val's rule: an (air-quotes) **"golden rule"** — make sure you have all the capabilities you want **before** peeling off a game copy; letting someone add "actually we needed this thing" mid-production is "a huge time sink" of regression integration. [[raw/devops_container_approach_for_omni_3.md]]
- Consequence Aaron spelled out and Val accepted: the game-production cycle becomes **shorter**, at the price of no mid-production engine changes — and "Michael and Lynn [Lena] and everybody else" must be confirmed OK with that ("we need to set the rules in place"). [[raw/devops_container_approach_for_omni.md]]
- Alexander's supporting rule (Russian continuation): "Я предлагаю в игре запретить делать какие-то изменения во фреймворке" — no framework changes from inside a game. [[raw/devops_container_approach_for_omni.md]] Val's next-day corollary: teams can improvise visually with existing capabilities — "They simply cannot utilize a certain visual effect that they would love to have, but they could still make games." [[raw/devops_container_approach_for_omni_3.md]]

## Rationale

- Improvements are incremental, not exponential — Val: you won't notice v7→v8 of a visual effect, only v1→v10; with a mature engine/framework/LGS/SAS "there is nothing revolutionary" per game, so throughput comes from freezing and templating, not mid-flight change. [[raw/devops_container_approach_for_omni_3.md]]
- Val's experience of the current loose culture: "на практике у нас лебедь, рак и щука… Я знаю, что у нас это более loose" — discipline is the missing ingredient, not know-how. [[raw/devops_container_approach_for_omni.md]]

Full workflow context: [[wiki/topics/omni-core-advancement-and-game-templating.md]]. Stub: [[wiki/meetings/2025-03-24-devops-container-approach-omni.md]].

## Sources

- [[raw/devops_container_approach_for_omni.md]]
- [[raw/devops_container_approach_for_omni_3.md]]
