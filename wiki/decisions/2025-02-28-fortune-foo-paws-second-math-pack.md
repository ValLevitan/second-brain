---
type: decision
title: Second math pack for Fortune Foo Paws (Chinese bet levels) to A/B test on the floor
date: 2025-02-28
aliases: [Fortune Foo Paws math pack two, Chinese bet levels, 88 to 888, math pack two]
status: active
---

# Second math pack for Fortune Foo Paws (Chinese bet levels) to A/B test on the floor

On the Feb 28 2025 game-design review, Val, [[wiki/people/juan-martinez.md|Juan]] and [[wiki/people/michael-gottlieb.md|Michael]] decided to produce a **second math program** for **Fortune Foo Paws** alongside the standard one, so JVL can try both bet configurations on the floor and see which performs. [[raw/Game design part 2 - Feb-28-2025.md]]

## What was decided

- Because these games' math is **specific to each bet**, you can't just change a multiplier to get different credit variants — a whole second set of math must be produced and approved. [[raw/Game design part 2 - Feb-28-2025.md]]
- The second pack uses the **Chinese "lucky-number" bet configuration — 88 up to 888** — in addition to the standard set (60/120/180/300/600). Both programs would be deployable; Val wants the alternative deployed in the **most competitive, highest-traffic location** to see how it lands. [[raw/Game design part 2 - Feb-28-2025.md]]
- Treatment: handle it as **"math pack two"** of the same game (same game, different math / pay-table ID / help screens), not as one math that can switch modes — the group felt switching math within one title would be confusing and there's no mechanism for it. This means a second GLI approval (or an approved additional package). [[raw/Game design part 2 - Feb-28-2025.md]]
- Rationale (Val): JVL isn't charging locations yet and lacks the depth of library/cabinets, so it can afford to experiment; the GLI overhead for the extra math is small. [[raw/Game design part 2 - Feb-28-2025.md]]

## Follow-up

- [[wiki/people/juan-martinez.md|Juan]] to write a **JIRA REQ** for the second math program with the Chinese bet levels; he has sample bets from competitors to fine-tune. [[raw/Game design part 2 - Feb-28-2025.md]]

## Sources

- [[raw/Game design part 2 - Feb-28-2025.md]]
