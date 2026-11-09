---
type: decision
title: When a modem is present its connection is forced on, and opting out is an intentional, multi-stage cycle — not a voluntary flag; fixing this scope gap means another re-approval and a software reinstall, and deliveries continue meanwhile
date: 2026-11-04
aliases: [modem configuration scope gap, modem connect flag, voluntary modem configuration, forced modem connection, opt-out cycle intentional and multi-stage, modem flag re-approval, reinstall the software for the modem, jam connected]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
---

# When a modem is present, its connection is forced on; opting out is intentional and multi-stage (Nov 4 2026)

Stated by [[wiki/people/val-levitan.md|Val Levitan]] to [[wiki/people/felipe-miranda.md|Felipe Miranda]] on the [[wiki/meetings/2026-11-04-felipe-igt-trade-in-approach-and-arc-delivery.md|Nov-4 10:27 AM call]] (English), after Felipe said the ten machines leaving for ARC that day all have modems [[raw/Meeting_Transcript_Felipe_IGT_Trade_In_Approach_and_ARC_Delivery-November-4-2026.md]].

## What Val found

- **A scope gap, found the day before.** Val: "yesterday I discovered a scope gap in how models [modems] are configured. So the modems are working, but the configuration of the modem is incorrect. Because now configuration is voluntary, where I want, if modem is present, then to be forceful" [[raw/Meeting_Transcript_Felipe_IGT_Trade_In_Approach_and_ARC_Delivery-November-4-2026.md]]. (Nov 3 by the calendar; where he found it is not said.)
- **The rule.** Val: "you could opt out of a modem, but it has the opt-out cycle has to be intentional and multi-stage. And the way it is now, it's just a flag. And if you forget the flag or if you change the flag, it, you know, it doesn't work" [[raw/Meeting_Transcript_Felipe_IGT_Trade_In_Approach_and_ARC_Delivery-November-4-2026.md]].
- **The field view.** Felipe: "on the on the jam tab [heard], yeah, but they this 10 were configured with jam connected. Of course, if there's a hard reset, they might not do it, so we might run into that problem" [[raw/Meeting_Transcript_Felipe_IGT_Trade_In_Approach_and_ARC_Delivery-November-4-2026.md]]. What "jam" is, is **unclear** (the notes read it as the "connect" setting).
- **The cost.** Val: "this is a severe issue for me and it will trigger another re-approval and we will have to reinstall the software." And: "of course, continue delivering machines. I just want you to be cognizant… to the subject." Felipe: "Understood" [[raw/Meeting_Transcript_Felipe_IGT_Trade_In_Approach_and_ARC_Delivery-November-4-2026.md]] [[raw/Meeting_Notes_Felipe_IGT_Trade_In_Approach_and_ARC_Delivery-November-4-2026.md]].

## How it sits against earlier rulings

- The commercial rule — every machine ships with a modem, customers may opt out of the service by message — is [[wiki/decisions/2026-10-06-every-machine-ships-with-a-modem-and-customers-are-told-reports-are-free-for-a-limited-time-with-an-opt-out.md]]. Nov 4 is about the machine's own configuration: the software must force the connection on when a modem is present, and an opt-out must be a deliberate multi-step action, not a flag that a hard reset or a forgotten setting can undo. **Evolution** (the product rule now matches the commercial one) — **inference** on the link; Val did not name the Oct-6 ruling.
- Hard resets and software reinstalls in Georgia are the burden tracked on [[wiki/topics/ris-remote-install-and-machine-states.md]].

## Open questions

- Who fixes the modem configuration, in which build, and when does the re-approval go in? Not said; no engineer or task was named on the call — [[raw/Meeting_Transcript_Felipe_IGT_Trade_In_Approach_and_ARC_Delivery-November-4-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Felipe_IGT_Trade_In_Approach_and_ARC_Delivery-November-4-2026.md]]
- [[raw/Meeting_Notes_Felipe_IGT_Trade_In_Approach_and_ARC_Delivery-November-4-2026.md]]
