# Meeting Summary — Street Cabinet Design Direction
**Initiative:** Street Cabinet
**Date:** June 16, 2026, 4:53 PM Eastern
**Duration:** ~40 minutes
**Attendees:** Val Levitan, Genadi Peari

## Summary

Val walked Genadi through functional requirements for a new low-cost street cabinet aimed at non-casino locations (bars, convenience stores, route locations). Target: vertical-screen machine selling at $5,000, production ~1,000 units/month.

**Physical design concept.** Val proposed a monolithic plastic back cavity (shell) as the structural frame, with a 43–49 inch HD vertical touchscreen (Gorilla Glass) bonded to the front — not field-serviceable, like an iPhone. Genadi pushed back early, asking Val to separate functional requirements from design decisions. Val agreed he was crossing into design territory but said his intent was to describe the machine functionally, not dictate engineering.

**Peripheral layout.** Val wants to eliminate the traditional dashboard panel between screen and lower VIDEK area. All peripherals (bill validator, printer, QR scanner) move underneath the VIDEK lip. Everything sits on a slide-out metal-frame drawer that pulls out the back for servicing, with a single cable connection to the display. Speakers integrate into the front plastic panel below the VIDEK.

Genadi initially questioned how a bill validator could fit under the VIDEK, but once Val clarified the lip/shelf concept (shallow tray with slots for bill insertion and receipt output), Genadi understood and agreed the approach works — especially since removing player tracking frees substantial space in the old dashboard area.

**Lighting.** Three zones — perimeter light (around screen edge), transition radius, and "washing" lights on the front panel — all controlled by game designers through the API as a unified perimeter.

**Back cavity debate.** Genadi raised concerns: mold tooling ~$150K (needs 5,000+ units to break even), ABS softens in heat (would need carbon fiber or nylon reinforcement, eliminating savings), and it may cost more than metal. Val argued that because the screen mounts monolithically and nothing disassembles, the plastic depth is only ~4 inches with ~2-inch ribs — not truly load-bearing. Val estimated ~$100 vs. current ~$300 metal cabinet. Genadi remained unconvinced but said he'd think about it.

**Market context.** Val is in Omaha (was in Texas yesterday). He visited route locations in both states. Texas alone has ~200,000 machines in the grey/illegal market. Operators care about cost and revenue share, not brand. JVL needs to hit a price point where even Chinese competitors can't match. Val referenced the ECO cabinet — designed for 3–5 year life, still running after 25 years — as proof that simple construction lasts.

**Assembly strategy.** Local assembly from individual component suppliers, not Chinese semi-finished imports. Reasons: maintain credit terms from each supplier separately, avoid shipping dependencies, potentially qualify for local tax benefits. Assembly can distribute to sub-shops (Georgia, Texas).

## Decisions Made

- **Vertical HD screen, 43–49 inches** — HD resolution sufficient; exact size depends on cost. (Val)
- **No player tracking or flag support** for street model — never needed. (Both confirmed)
- **Eliminate the dashboard panel** — lower the screen, move all peripherals under the VIDEK lip. (Val; Genadi agreed after clarification)
- **Slide-out drawer for all hardware** — bill validator, printer, harness, SBC on one metal-frame drawer with single cable to display. (Both agreed)
- **Perimeter + washing lights controllable by game designers via API.** (Val)
- **Support for 2 displays** — vertical main + deck. (Both)
- **Slam button on right side** of VIDEK panel. (Val)
- **Single rear connection** to external controller. (Val)
- **Target sell price: $5,000.** (Val)
- **Production target: ~1,000 units/month** (12,000/year). (Val)
- **Local assembly only** — no Chinese semi-finished imports. (Val; Genadi accepted the reasoning)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Evaluate plastic back cavity concept — mold cost, material options (ABS + reinforcement), thermal behaviour, total cost vs. current metal construction | TBD | High | Core design decision; Val estimates $100 vs $300 metal, Genadi skeptical |
| 2 | Genadi Peari | Develop a cost-optimized design concept for the street cabinet based on the functional requirements discussed | TBD | High | Val needs this machine fast; once Transaction Management work wraps, street cabinet becomes top priority |
| 3 | Genadi Peari | Message Val with any questions — Val back in ~2 hours from meeting end | June 16, 2026 | Normal | Val leaving for another meeting in Omaha |

## Open Questions

- **Plastic vs. metal back cavity:** Not resolved. Val believes the math favours plastic; Genadi sees cost and thermal risks. Needs a concrete cost comparison.
- **Bill validator type and placement:** Back-load vs front-load orientation within the drawer discussed; exact solution deferred to design phase.
- **Printer service access:** Val wants printer on the drawer too; Genadi said they'd figure out the most convenient approach — "not a matter of principle."
- **Exact screen size:** 43–49 inch range set, final pick depends on cost sourcing.

---
*Processed from Teams transcript on June 16, 2026*
*Source meeting: Street Cabinet Design Direction*