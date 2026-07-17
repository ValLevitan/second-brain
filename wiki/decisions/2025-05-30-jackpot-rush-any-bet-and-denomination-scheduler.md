---
type: decision
title: Remove max-bet-required progressives on Jackpot Rush; build a denomination-scheduler capability across games
date: 2025-05-30
aliases: [Jackpot Rush any bet, JPRE any bet, progressive at any bet, remove max bet required, denomination scheduler, denom scheduler, day-of-week bet levels, Interblock denom scheduler]
source-count: 1
status: active
---

# Remove max-bet-required progressives on Jackpot Rush; build a denomination-scheduler capability across games

**Decision (Val, [[wiki/people/juan-martinez.md|Juan Martinez]] and [[wiki/people/michael-gottlieb.md|Michael Gottlieb]], May 30 2025):** two related rulings on the **Jackpot Rush** ("JPRE") title and JVL's bet-configuration approach. [[raw/game_design_review_jpre-may-30-2025.md]]

## 1. Remove the max-bet requirement for Jackpot Rush progressives

- **The problem (Michael).** Jackpot Rush requires **max bet** (~$3 / 480 credits at 1¢, 300 at 5¢) to be progressive-eligible, but observed average bets are only ~**$1.20–$1.40** (Juan: $1.87 / $1.70) — so most players never see the progressive **meters** running; they get a **static credit tower**, "an inferior experience." JVL has **never had a jackpot hit on any Jackpot Rush game.** Michael framed his earlier casual concern as "a design mistake with JPRE relative to [the] market it has been deployed in." [[raw/game_design_review_jpre-may-30-2025.md]]
- **The ruling.** Make progressives eligible **at any bet** (remove the max-bet-required condition), rather than merely lowering the max bet from $3 to $2. Juan agreed and preferred removing the requirement over altering bet levels ("gets us more bang for the buck"); the Georgia version of Jackpot Rush is **already at-any-bet**, so this brings the Class-3 (Florida) version in line. This requires a **math redesign** for the Florida version. [[raw/game_design_review_jpre-may-30-2025.md]]
- Val's minimum-bet philosophy was also aired (he "goes nuts for the first button" — a 40¢-vs-60¢ min bet is a ~50% revenue difference), but was kept separate from the max-bet-removal ruling. Detail on [[wiki/topics/slot-game-design-principles.md]]. [[raw/game_design_review_jpre-may-30-2025.md]]

## 2. Build a denomination-scheduler capability across games

- **The capability.** A machine that changes its **bet levels / denominations by time of day and day of the week** — a "chameleon" that offers a cheaper first button to the weekday value crowd (Mon–Wed, ~1–5 pm) and steps up for the weekend high-volume crowd. Val: "day dependent or hour dependent settings." [[raw/game_design_review_jpre-may-30-2025.md]]
- **Precedent.** Juan had **Interblock** build a "**Denom scheduler**" for him years ago (it removed the 25¢/50¢ bets after 5 pm daily and "was phenomenal"). Mechanically it submits **two part-sheets to GLI** with one enabled/disabled by schedule — "this box contains two games in one." [[raw/game_design_review_jpre-may-30-2025.md]]
- **The ruling.** Design the scheduler **across the board**, not just for specific titles (Val: "you need to design it across the board"). Michael raised a possible **patent/IP** concern (Bally once refused it on IP grounds; he doubts it), and Val committed his **staff lawyer** to research it, adding they could use a random-number trigger instead of the calendar to work around any patent. Action items: **Michael** drafts the scheduler requirements; **Val** runs the legal research; **Juan** provides market analysis on optimal bet levels by time period. [[raw/game_design_review_jpre-may-30-2025.md]]

Relates to [[wiki/topics/slot-game-design-principles.md]], [[wiki/projects/georgia-market-rollout.md]] and [[wiki/people/juan-martinez.md]].

## Sources

- [[raw/game_design_review_jpre-may-30-2025.md]]
