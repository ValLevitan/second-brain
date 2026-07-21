---
type: meeting
title: Flex-POS alignment & scheduling — the January POS deliverable (Sept 15 2025)
date: 2025-09-15
aliases: [Flex POS alignment scheduling, POS January schedule, Nathan return alignment, POS three-month schedule]
source-count: 1
---

# Flex-POS alignment & scheduling — the January POS deliverable (Sept 15 2025)

**Date:** 2025-09-15 (6:06 PM) · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/juan-martinez.md|Juan Martinez]]. English.

A short realignment on [[wiki/people/nathan-carver.md|Nathan]]'s return from time off, to re-engage the team on the one critical deliverable: **the POS system for January**. Continues the flexpay/transactional POS thread (Sept-3 [[wiki/meetings/2025-09-03-flex-capabilities-weekly-ach-dispute-pos-design.md|Flex weekly]], Sept-9 [[wiki/meetings/2025-09-09-top-level-backend-architecture.md|top-level back-end]] / [[wiki/meetings/2025-09-09-pos-spatial-hardware-board-planning.md|POS hardware]], Sept-10 [[wiki/meetings/2025-09-10-minimum-architecture-pos-deployment.md|minimum-architecture]]); substance folds into [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept-15 section).

Durable points (single source):

- **The deliverable + the tight clock.** To install the POS in January JVL needs both the **hardware (the POS itself)** and a **back-end system**. Val framed the runway as "extremely tight": only **October, November, December** (~three months) usable, with **half of December a write-off** and a **week in January when Minsk is off**.
- **Hardware ~80–90% done (Genadi).** Design, material selection, spatial planning and component selection are 80–90% complete; next is designing the **plastic enclosure** and moving into **tooling**. Genadi's estimate: **new boards done ~mid-November**, **mechanics design ~early November**; in January JVL can build **rapid prototypes** (not full molds) and reach **mass production right after Chinese New Year** (~February). He judged **rapid prototyping "very durable, same like a mold"** — citing the curved-cabinet sound system he built and tested that way — with the only limitation that the finish won't be as glossy (paintable to look similar), and cheap for 5–10 pieces.
- **Pavel's architecture plan.** Implement the **InComm Cloud Payment Hub cloud application by end of October**, together with the **Flex-POS module that communicates via this payment hub**; by **January 1**, a first Flex-POS application that can process **Mutha Goose** commands, save them internally in the Flex-POS database, and **redeem a card** using the payment hub.
- **Use cases (Nathan).** Nathan judged ~**90%** of the use cases already known; he will hammer out the rest (first version), targeting **end of next week**, handing them to Pavel and Juan for review to iterate. He will prioritize the software fields that **unblock** software work (device provisioning first), aiming to have enough done in ~2 weeks for software to start consuming, all done within ~4 weeks.
- **Val's priority order: payment hub first, then ACH.** Requirements focus on the payment hub first; Val added that **ACH processing is an absolute showstopper**. Nathan had already identified **one or two specialty shops for ACH processing** — Val directed him to start a relationship immediately, get their **API** and discuss terms of business as the **first priority** (ahead of other requirements), ideally "today afternoon."
- **Next step:** Val will use the transcript to draft an initial schedule and send it to Nathan and Juan for review; the team "quarterbacks" it.

## Open commitments

- [ ] Nathan Carver — contact the identified ACH-processing specialty shop(s) immediately, obtain their API and discuss terms of business (first priority, ahead of other requirements) — due ~same day (Sept 15) — [[raw/Flex-POS-alignment-scheduling-september-15-2025.md]]
- [ ] Nathan Carver — finish the first version of the remaining Flex-POS use cases and hand them to Pavel and Juan for review — due ~end of the following week — [[raw/Flex-POS-alignment-scheduling-september-15-2025.md]]
- [ ] Pavel Frolov — implement the InComm Cloud Payment Hub cloud application (by end of October) and the first Flex-POS app (Mutha Goose commands → internal DB → card redemption via the hub) — due Jan 1 2026 — [[raw/Flex-POS-alignment-scheduling-september-15-2025.md]]
- [ ] Val Levitan — draft the initial POS schedule from this transcript and send it to Nathan and Juan for review — due unspecified — [[raw/Flex-POS-alignment-scheduling-september-15-2025.md]]

## Sources

- [[raw/Flex-POS-alignment-scheduling-september-15-2025.md]]
