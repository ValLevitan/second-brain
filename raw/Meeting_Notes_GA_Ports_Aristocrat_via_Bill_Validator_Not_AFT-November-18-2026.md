# Meeting Summary — GA Ports connections to EGMs: 'partial AFT' VS 'all BV+Counters'
**Date:** November 18, 2026, 8:00 AM – 8:22 AM Eastern
**Duration:** ~22 minutes
**Attendees:** Andrei Klimovich (organizer), Pavel Frolov, Irina Shishko, Val Levitan
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026]]

## Summary

**The question.** Andrei: a port on a game machine has two jobs — transactions (money in and out) and game performance data. Today, depending on the maker, we do transactions through AFT or through bill validator + counter. Of all machines on the market, only Aristocrat and JVL support full AFT (maybe Novomatic; a machine will be borrowed on Friday to test). Should we drop AFT for transactions and use bill validator + counter on all machines, and SAS only for data?

**For AFT (Pavel).** With bill validator emulation, odd amounts need several operations. The bill validator link can lose connection and cause errors. SAS is more reliable: every packet has a checksum.

**Against AFT.**
- Pavel: most companies in the Georgia market did not implement AFT properly. AFT on non-JVL machines cannot be re-tested on every release; any change can break it.
- Andrei: at the United Gaming warehouse, 4 Aristocrat machines with identical settings — AFT worked on one and not on another; only reboots helped. Very unreliable.
- Irina: these machines already run with a bill validator in the field; we only plug in between. With a bill validator we know whether a problem is in our port or in their AFT.
- Andrei: for technicians, bill validator + counter is simpler — no machine settings, no RAM clear, minimal downtime. This matters when customers install ports themselves from our instructions.
- Pavel: own machines can use SAS/AFT; other makers' machines are safer on the bill acceptor. Val: that is what Andrei is saying.
- Irina: nothing new to build — we already support both modes.

**Scope gap: cash-in counter.** Pavel: in the bill-validator wiring, one wire was only used for cash-out. Cash-in is on the board but not supported in software, so money-flow reports on Flex IQ miss cash-in. Pavel already added it to tasks. Val: this needs a software upgrade and must be in the acceptance criteria. Val told Irina not to let anyone skip writing acceptance criteria. Pavel did not remember if it is in version 21 or 22; Irina will find out. Andrei: it should go with the report, which is MVP 2 only. Irina: 21 and 22 will likely ship as one build.

**Field release.** Andrei: nothing goes to the field until MVP 2 is tested. Val: as soon as approval comes, he will push installs at locations.

**Val's ruling on Aristocrat.** Connect Aristocrat through the bill acceptor, not AFT. Otherwise, at a location with untested Aristocrat software, the team will struggle and may have to reverse the install. Andrei: on Friday at the warehouse they will check the remaining brackets and connect an Aristocrat through the bill validator. Bill validator support covers all models on the market now. Val complimented Andrei for thinking this through.

**SAS data (later).** Pavel: through SAS we can read meters (money in/out, games played, wins, bets) and events (door open, tilt) on all machines; game-title data depends on each machine. The port already collects some of this, held out of the current release because it is not tested. Andrei: this is MVP 3, not earlier; reports must be designed to give real business value to operators and masters; Intralot data is inaccurate and hard to get (PDF downloads). Val: stop spending time on this now — customers will ask for it naturally once they see our reports. Focus now on MVP 2 implementation, then MVP 3 in steps (3.1, 3.2, …) with all reports.

**Next call.** Andrei: the team's MVP 2 focus is drifting. One-hour call tomorrow (Thu Nov 19), 8–9 AM, to clean up what is in 21/22. Val wants to attend. Invite Pavel, Irina, Dmitri, Sergey.

## Decisions Made

- **First installs connect Aristocrat machines through the bill acceptor, not AFT.** — AFT on non-JVL machines is unreliable and cannot be re-tested each release. (Decided by Val, on Andrei's proposal)
- **SAS data and extra reports wait for MVP 3, in steps.** — Focus now is MVP 2. (Decided by Val; Andrei agreed)
- **Cash-in counter gap must be covered with acceptance criteria.** — It is a software change. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | At the warehouse, check remaining brackets and connect an Aristocrat machine through the bill validator | Nov 20, 2026 | High | Also borrow a Novomatic machine to test |
| 2 | Andrei Klimovich | Set up a 1-hour MVP 2 scope call, Thu Nov 19, 8–9 AM, with Val, Pavel, Irina, Dmitri, Sergey | Nov 19, 2026 | High | MVP 2 focus is drifting |
| 3 | Irina Shishko | Find out if the cash-in counter fix is in version 21 or 22 | TBD | Normal | Pavel already added it to tasks |
| 4 | Irina Shishko | Make sure acceptance criteria are written for the cash-in counter work (no skipping) | TBD | Normal | Val's instruction |

## Open Questions

- Does Novomatic support full AFT? To test with a borrowed machine on Friday (Andrei).

## Dispatch Log

---
*Processed from Teams transcript on November 18, 2026*
*Source meeting: GA Ports connections to EGMs: 'partial AFT' VS 'all BV+Counters'*
