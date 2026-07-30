# Meeting Summary — Game Development (Market Deployment & Texas Compliance)
**Date:** April 9, 2026, 6:31 PM Eastern
**Duration:** 15m 4s
**Segment:** 3 of 3
**Attendees:** Michael Gottlieb, Val Levitan, Lena Zhukova, Efim Podvoiski, Juan Martinez

## Summary

**Nebraska and South Dakota status.** Juan opened with deployment status: patch software for Nebraska is "right around the corner," and things are progressing well in both South Dakota and Nebraska. Michael noted the dual-box turnaround was fast.

**Texas market performance.** Juan asked Rich for new data on the Texas machines, including an update on the two machines Rich had not previously installed; no reply yet. Early numbers: one machine is running **$225 WPU (win per unit)** for the data timeframe available. A second machine is around **$83 WPU**, but that figure is distorted by one negative day out of four and is not yet representative. The customer stated he would be happy at **$100 WPU**. Juan expressed confidence they will easily clear $100 and exceed it, so he is not concerned about the Texas deployment.

**Reconditioned-machine strategy for Texas.** Val highlighted that Texas is a good market for reconditioned machines, and JVL has a large warehouse inventory of those. He framed it as converting a non-cash-producing asset into a cash-producing asset. Michael defended the quality of JVL's older hardware: "It still looks like a slot machine" compared to competitors' "ghetto cabinets," even when older. Val clarified he did not mean to disparage the product.

**Next product initiative — vertical dual-screen for South Dakota, Nebraska, and Texas.** Michael prompted Juan on what market to target with dual-screen vertical next. Juan said a vertical for South Dakota is needed to expand product sales. Val pushed for broader scope: vertical product should be available **everywhere**, and right now it is "not really on the map." Consensus landed on **vertical for South Dakota, Nebraska, and Texas**.

**Texas vs. Nebraska branch relationship.** Michael asked whether Texas gets anything special or whether the Nebraska release IS the Texas release. Juan clarified: currently **two distinct branches** with minor modifications, but ideally they should **re-merge** into a single codebase and be identical. Lena added that the Texas version keeps the score and scheme for bonus (golden husk) which is OK for Texas. Michael noted the flexibility to add regional flair (e.g., in Rodeo Spins they changed the belt buckle to say "Georgia rodeo" for the Georgia release) and suggested the same approach could be used to add Texas flair. Lena mentioned a Texas version with Texas stars had been done previously but the team decided not to release it.

**CRITICAL COMPLIANCE RULE — Texas content prohibitions.** Juan explicitly asked that this be on record "for our AI and meeting notes." The rule:

> **Texas branch software must always be Nebraska-based. The word "Texas", the state of Texas symbol, and the Texas flag must NEVER appear anywhere in the Texas branch of Nebraska software.** Cowboy-inspired content and general Americana are allowed. Anything specifically identifying Texas is not.

Michael explicitly confirmed ("Got it, OK"). Val suggested that if a truly Texas-specific game is ever wanted, the theme should be **wild boar hunting** (which is a major legal activity in Texas, including helicopter hunting with .50 caliber rifles targeting the invasive species). Juan half-joked the next game could be "Wolf Pack eating the boar."

**Extended industry-history tangent.** The second half of the segment was a long personal/industry conversation anchored on Michael's history at Midway and prior companies. Key names and facts mentioned: **John Rowe** and **Byron Cook** (the latter a Texan from Corsicana, TX, 45 minutes south of Dallas) — partners Michael worked for; **Leland Cook** (Tradewest coin-op side); **Dale Rodish** — Val disclosed he and Rodish were very close friends and claimed he "single-handedly put him on the map"; **Cinematronics** — acquired by John Rowe out of bankruptcy; early vector video games including **Star Castle** (Cinematronics' biggest hit), **Warrior**, and the laser-disc title **Dragon's Lair** (1983, Don Bluth, built on consumer-grade Pioneer laser-disc players that were not rated for commercial use — cigarette smoke fouled the optical lens, motors overheated, machines broke down); follow-up kit **Space Ace**; the laser-disc failure caused a major industry downturn in 1984. Both Michael and Val reminisced about the handshake-deal era of the coin-op industry — "word, word, word, no contract." Efim mentioned an upcoming trip to Mexico (Akumal Beach, where the sea turtles are); Juan and Lena discussed sargassum seaweed timing (bad Feb/March, better in December/early January).

**Meeting close.** Michael wrapped, everyone said goodbyes; Juan wished Efim a good trip.

## Decisions Made

- **Next vertical dual-screen initiative targets South Dakota, Nebraska, and Texas.** (Juan with Val and Michael)
- **Texas software branch must be Nebraska-based** — two distinct branches today, but should re-merge. (Juan; confirmed by Michael and Lena)
- **Texas-branded visual content is prohibited in the Texas branch:** no "Texas" word, no Texas state symbol, no Texas flag. General cowboy/Americana content remains acceptable. (Juan, on record; confirmed by Michael)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Juan Martinez | Follow up with **Rich** for new Texas performance data and an installation update on the two machines not yet installed | April 10, 2026 | Normal | Need data to represent the second machine's true performance (current $83 WPU figure is distorted by one negative day) |
| 2 | Juan Martinez | Scope next initiative: vertical dual-screen product for South Dakota, Nebraska, and Texas | TBD | High | Positioned as the "next project" coming out of this meeting |
| 3 | Development team (unspecified owner) | Plan re-merge of Texas and Nebraska branches into a single codebase with minor configuration differences | TBD | Normal | Two distinct branches today creates maintenance overhead; target is identical codebase |
| 4 | All developers / product owners / designers (team-wide) | **Comply with Texas content rule** — no "Texas" wording, no Texas state symbol, no Texas flag anywhere in the Texas branch of Nebraska software | Immediate / ongoing | High | Explicitly called out by Juan as a standing compliance rule for the AI/meeting-notes record; cowboy content is allowed |
| 5 | Juan Martinez | Monitor Nebraska patch software release progress | Ongoing (imminent) | High | Release is "right around the corner" — customer-facing delivery |

## Engineering Signals

### Confirmed Signals

- **REQ — Texas content prohibition:** Juan explicitly asked that this be on record. The Texas branch of the Nebraska software MUST NOT contain the word "Texas," the Texas state symbol, or the Texas flag. Cowboy-inspired and generic Americana content is allowed. This is a standing compliance requirement for every Texas-market build.
- **ADR — Texas and Nebraska software share a codebase; Texas is Nebraska-based:** Explicit architectural decision that the Texas branch must remain Nebraska-derived. Current state is two branches with minor differences; the target end state is a single codebase with regional configuration.
- **CAP — Regional flair via configuration (not forking):** Established pattern (precedent: Rodeo Spins' Georgia-specific belt buckle customization) that regional customization is done by configuration/asset swapping, not by code branching. The Texas content prohibition overlays on top of this capability.

### Suspected Signals

- **Possible REQ — Minimum Texas WPU target:** The customer's stated happiness threshold of $100 WPU is a de facto performance target for Texas installations.
- **Possible ADR — Reconditioned-machine product line for Texas:** Val's framing of Texas as a reconditioned-machine market creates a product-line-level architectural choice (reconditioned vs. new hardware SKU targeting).
- **Possible CAP — Vertical dual-screen as a cross-market capability:** Val pushed to make vertical "everywhere" rather than market-specific.

## Open Questions

- **Specific minor modifications that currently differ between Texas and Nebraska branches** — not enumerated; need inventory before re-merge. (Development team)
- **Whether the previously-created, unreleased Texas-stars version** has any salvageable content that complies with the new Texas content rule. (Lena Zhukova / Michael Gottlieb)
- **Whether a wild-boar-hunting-themed game is a real roadmap candidate** or banter. (Juan Martinez and Michael Gottlieb)

---
*Processed from Teams transcript on April 13, 2026*
*Source meeting: Game Development — Segment 3 (April 9, 2026, 6:31 PM)*
