# Meeting Summary — Alignment (Transactional Hardware Platform)
**Date:** 29 May 2026, 11:33 AM Eastern
**Duration:** ~9 minutes
**Attendees:** Val Levitan, Genadi Peari, Pavel Frolov

## Summary

The team settled how to build the transactional devices — recycler, dispenser, and paystation — and which computer platform to use.

These were first put together on the **V-1000** platform — an aging AMD-based processor that is almost out of circulation. Val said there's no point staying on it: it was always just a starting point, and keeping it only wastes money. Everyone agreed. The whole transactional category moves to the **Rockchip** platform.

Genadi and Pavel had already talked the day before and reached the same view — no point building an in-between version:
- **Recycler** — build on Rockchip from the start. No temporary version.
- **Dispenser** — can't switch quickly. Leave the current sample as it is for now, and move it to Rockchip as the next step.

Genadi can't finish the Rockchip build today. The wiring he needs (the same wiring planned for Flex) isn't done, and he's waiting on an interface adapter board that Alexeev is making. He'll assemble what he can, make it easy to retrofit later, and write a short list of what's left so others can finish connecting it.

On the paystation size — bulky versus slim — Val chose not to decide. Some buyers want a wider unit, some want slim. He said JVL is in a comfortable position and can let the product exist in more than one form factor, and let the market decide.

Genadi raised a concern: there's a big gap between the technology the team designs and how things are actually built on the floor in Georgia. He said the assembly is makeshift and the place needs better working culture. Val agreed.

## Decisions Made

- **Move the whole transactional category (recycler, dispenser, paystation) to Rockchip.** The V-1000 (AMD-based) was always temporary and is aging out of circulation; staying on it wastes money. (Decided by Val; agreed by Genadi and Pavel.)
- **Recycler: build on Rockchip from the start** — no in-between version. (Genadi/Pavel, endorsed by Val.)
- **Dispenser: keep the current V-1000 sample for now, move to Rockchip next.** It can't be switched quickly. (Pavel; accepted by Val.)
- **Paystation form factor stays undecided on purpose.** Let it exist in both bulky and slim versions; let the market decide. (Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi | Assemble as much of the recycler as possible now, built so it can be retrofitted to Rockchip easily | TBD | High | Full Rockchip build is blocked today by missing wiring and the adapter board |
| 2 | Genadi | Leave the dispenser sample on the V-1000 as a working unit; have a second ready if needed for shipping | TBD | Normal | Dispenser moves to Rockchip as a later step |
| 3 | Genadi | Write a short punch list of what's left on the dispenser so the team can connect it themselves | TBD | Normal | Lets others finish without him |

## Open Questions

- No date set for moving the dispenser to Rockchip — it's the "next step" but unscheduled.
- Genadi is blocked on Alexeev's interface adapter board and the Flex wiring before he can finish the Rockchip build.
- Quality/culture on the Georgia assembly floor — Genadi flagged it; no action assigned.

---
*Processed from Teams transcript on 29 May 2026*
*Source meeting: Alignment-20260529_073303 (Teams recording)*
