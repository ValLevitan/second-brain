# Meeting Summary — 3rd part EGMs Port connection sync
**Date:** October 20, 2026, 8:31 AM – 9:04 AM Eastern
**Duration:** ~33 minutes
**Attendees:** Andrei Klimovich, Pavel Frolov, Val Levitan, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026]]

## Summary

Held in Russian. Follow-up to the October 16 third-party EGM tests.

**Where integrations stand.** Pavel: only JVL and Aristocrat work fully. The other machines work only partly with AFT transactions. They must be connected in bill validator emulation mode to add credit, and through pulses to cash out. JVL can already do this (it was the original design; Pavel kept the code as a setting). QA has not tested this mode for two weeks, so new tests are needed.

**SAS data from other machines.** Andrei wants to read SAS data (game-title performance, money in and out) and sell it as an analytics add-on, about $30–50 per month. Val asked why. He said calling it a "hybrid mode" is wrong: it is an undocumented, accidental behaviour of other makers, and following it means chasing them forever. Either the machine has AFT, or JVL connects through pulses. Andrei split it in two: AFT is for transactions; the SAS protocol is for data. Final wording, which Val approved: transactions run through bill validator and counters (pulses); on every machine with SAS 6.0 or higher, JVL can read data and turn it into a paid product. Val noted future promotional credits will work only on AFT machines (JVL, Aristocrat).

**How a port knows its mode.** Val asked to detect the mode automatically (bill acceptor connected = no AFT). Pavel said this is not reliable: a bill acceptor can lose power, and a broken pulse line cannot be detected. Andrei: set the mode per port in the gateway.

**Bill acceptors.** Technicians may swap a bill acceptor for another make. JVL connects at the fixed connector on the cabinet. Pavel thinks ID-003 should work across makes; test with the four bill acceptors in the office.

**SAS commands seen.** Pavel checked three machines (not Banilla): a limited set, handpay state, door open/close; Light & Wonder answers credit queries. Irina: certified machines must support about 20 commands. Pavel: statistics are required on the primary SAS port, not always on the secondary. Light & Wonder has a setting to report every spin; trying it needs a reset. The HTT setup dongle is being taken back today.

**Plan this week.** Machines must be returned Friday. Andrei and Sebastian are away Wednesday and Thursday (trade show); Elizabeth is available. Connect ports through pulses and bill validators on all machines except Banilla. Keep SAS on; turn off AFT on the secondary port. Leave Banilla as it is; Pavel checks its commands.

**Schedule.** Val asked to set the final MVP1 now. Alekseev must make the build production-ready. Val: release on Wednesday (exact date not stated). QA must test as many bill-validator-emulation cases as possible, in parallel with real machines in Georgia. Val: first installation around November 2 (a Monday), if all other conditions are met. Andrei agreed on that condition.

## Decisions Made

- **Machines without working AFT connect in bill validator emulation (credit in) plus pulses (cash out); this mode is part of MVP1.** — Most third-party machines do not support AFT fully. (Val, Pavel)
- **SAS is treated separately from AFT: AFT for transactions, SAS 6.0+ for data, which may become a paid product.** — Considered and superseded: calling it a "hybrid mode" (Val rejected the term). (Andrei, approved by Val)
- **Port mode is set per port in the gateway, not detected automatically.** — Auto-detection by bill acceptor is unreliable. (Pavel, Andrei)
- **MVP1 release on Wednesday; first installation around November 2, 2026, if all other conditions are met.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Write the capability for bill validator + pulses and move it into MVP1, tied to requirements with acceptance criteria | Oct 20, 2026 | High | Needed before Irina's team can write tests |
| 2 | Andrei Klimovich | Review the requirements with proposed changes and give approval in comments | Oct 20, 2026 | High | Irina's request; Claude flags them as waiting for Andrei |
| 3 | Andrei Klimovich | Ask Sebastian to connect ports through bill validators and counters on all machines except Banilla | Oct 20, 2026 | High | Machines return Friday |
| 4 | Andrei Klimovich | Send the list of bill validators on all machines; check machine settings | Oct 20, 2026 | Normal | Irina's request |
| 5 | Pavel Frolov | Check which SAS commands the Banilla supports (left as is) | TBD | Normal | |
| 6 | Pavel Frolov | Create tasks for testing with third-party machines | TBD | Normal | |
| 7 | Irina Shishko | Create and start automated test tasks for bill validator emulation mode (with Alexey, Ivan) | Next week | High | |
| 8 | Alexey Khamin | Write the story for Alekseev to make the build production-ready | TBD | Normal | Per Irina |

## Open Questions

- Should JVL read SAS data from competitor machines at all, and sell it? Andrei proposed; Val doubted, then liked the wording. No final product decision.
- Do replacement bill acceptors of other makes use the same connector? Raised by Andrei.
- Which Wednesday is the MVP1 release? Not stated.

## Dispatch Log

---
*Processed from Teams transcript on October 20, 2026*
*Source meeting: 3rd part EGMs Port connection sync*
