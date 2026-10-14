# Meeting Summary — RIS MSVP2 Meeting
**Date:** October 12, 2026, 11:29 AM – 12:02 PM Eastern
**Duration:** ~33 minutes
**Attendees:** Felipe Miranda Giorgi, Pavel Frolov, Irina Shishko, Sebastian Cortes
**Raw transcript:** [[Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026]]

## Summary

**Recording started late.** Felipe restated the topic: MVP 2 RIS improvements. Pavel was setting a fixed start date and a fixed release date for MVP 2.

**Send MVP 1 to the lab, or wait for MVP 2?** Pavel asked if it is worth resubmitting, because changes go into three different builds. Felipe's view: MVP 1 changes fix some areas but not the biggest customer pain points. Paying the lab for an MVP 1 build, then asking customers to upgrade again about a month later, after all the past upgrades, "will be complicated." He said he does not know what Val wants. Pavel: "I will save this for now."

**Biggest customer pain points (Felipe; Sebastian agreed).** A hard reset for every problem on a JVL machine (boot loop, wrong version). The passport scan. Software mismatch. Some MVP 2 items address hard-reset causes; MVP 1 items (for example, only one QR scan) do not. Example: adding or removing a printer needs a hard reset, new settings and a new file from Elizabeth or someone at JVL for each configuration, which costs time and resources.

**Capabilities reviewed (Pavel shared Jira capabilities):**
- **251 and 253** — server-side (Pavel said "related to Sierra, looks like"). These can be added after the release, for an already submitted version, without submitting again.
- **250 — add printer.** A developer already built it, "by mistake," not even for MVP 1. If a printer is connected to a machine whose RIS has no printer, it appears in the system. The setup screen gets a "use printer" check mark. If checked, the printer joins the list of cash-out devices, before hand pay but after AFT. Not tested yet. Some server-side work may be needed; it can come after submission, but it is better to release it together.
- **248 — upgrade software without creating a new RIS.** The hardest item. Needs both a local gaming server fix and server-side work. Felipe: "that is MVP 2 for sure." Pavel: the first part may be possible in MVP 1 — reuse reserved areas so that, after a factory reset on the same version, initial setup can select a pre-saved RIS without a USB stick. The next part reuses the RIS with newer, suitable software (same games, same number of lines).
- **Recover from boot loop without hard reset.** Pavel does not know how to do it yet; it needs a lot of experiments first. Most critical errors come from wrongly written data in storage. Some cases might be fixed by clearing the last game status, but the Gaming Commission may already have the last records, and the last game status would be lost — "not so good." Felipe: boot loops often follow storms or power peaks; it needs more technical investigation; he is not sure it relates to missing parts of the ISO.

**Cash-out-only screen.** Felipe asked for a screen with cash-out logs only (ticket cash-out, not TITO). Today the transaction history has 81 pages mixing bets, wins and deposits, and a past cash-out is overwritten fast if play continues. He discussed it with Juan, who said it was in progress. Pavel: Sebastian will write the capability; adding it to MVP 2 is "not a big deal."

**Intralot lock/unlock problem.** When a machine loses its SAS (RS-232) connection to the Intralot server, it can stay locked by the accounting system after it reconnects. The lottery cannot unlock it from their server. Someone must manually go out of service, operational, exit. The lottery told Felipe a machine locked by them should not be unlockable by hand. Felipe has logs, already sent to the lottery and to Juan. Felipe has a meeting with Val at Intralot tomorrow morning (October 13), and Val wants to raise this there. Pavel: a lock/unlock fix went into the latest build. Felipe first named Peach vertical build 3866 ("I believe") as the last one sent to Eclipse. Irina found the build with the fix: **4333**, the new Megahits build, just released and not yet installed. Felipe: the office has an IGT SAS simulator to test lock/unlock cycles. Agreed to test 4333 in the office and observe.

**No printer, but the RIS requires one (Sebastian, capability 250).** Today an RIS with a printer cannot be applied if no printer is installed. Pavel: initial setup should show a message that the RIS needs a printer. Felipe: it should let you continue, since you can uncheck the printer later. Pavel wrote the case down. His position at the end: installation can continue; the machine then shows a tilt until a printer is installed, or until the printer is unchecked in setup.

**TITO in without TITO out.** Customers want ticket-in on the bill acceptor but no printer in the machine (they print behind the counter). The TITO menu for secure enhanced configuration only appears when a printer exists. Pavel: does not know yet; maybe not a big change; maybe the on-the-fly printer fix will enable the TITO page. He will discuss with developers.

**Timeline.** Pavel: not much machine-side work is left — mainly the two RIS reuse features; server side can be released afterwards. Most work can close in about two weeks (not sure about boot loop), plus about one week of testing. Irina: until about November 1. Felipe: then about five days at Eclipse, so release around November 9–10. That is about one more week of delay. Felipe: "let's see what Val thinks." Felipe said he would be much happier with all the MVP 2 fixes than with only the MVP 1 fixes. Pavel agreed it brings a lot of convenience for technicians.

## Decisions Made

- **Capabilities 251 and 253 (server side) can be added after submission, without resubmitting the build.** — server part can follow the release. (Decided by Pavel Frolov; Felipe accepted)
- **Sebastian writes a capability for a cash-out-only log page, to be considered for MVP 2.** — current 81-page history is overwritten fast. (Decided by Pavel Frolov)
- **Test build 4333 (Megahits) in the office for the Intralot lock/unlock behavior.** — the build contains a lock/unlock fix; observe whether it works. (Decided by Pavel Frolov and Felipe Miranda Giorgi)
- **RIS that requires a printer, on a machine with no printer: installation continues; machine tilts until a printer is installed or the printer is unchecked in setup.** — Pavel's working position; the case was written down "to think about." (Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Felipe Miranda Giorgi | Get Val's input: send MVP 1 to the lab now, or add the MVP 2 changes and release later (~Nov 9–10) | [Needs Val's confirmation] | High | Felipe prefers all MVP 2 fixes |
| 2 | Sebastian Cortes | Write the capability for a cash-out-only log page | TBD | Normal | Asked by Pavel |
| 3 | Felipe Miranda Giorgi | Forward the Juan / lottery email exchange on lock/unlock to the team | TBD | Normal | Includes logs and history |
| 4 | Felipe Miranda Giorgi | Find out if Juan was working on lock/unlock with the dev team | TBD | Normal | "I will find out" |
| 5 | Felipe Miranda Giorgi | Test build 4333 in the office (IGT SAS simulator), lock/unlock cycles; observe | TBD | High | Build not yet installed |
| 6 | Pavel Frolov | Investigate lock/unlock behavior | TBD | High | Intralot issue |
| 7 | Pavel Frolov | Decide the "no printer, RIS requires printer" case with developers | TBD | Normal | Raised by Sebastian, cap. 250 |
| 8 | Pavel Frolov | Discuss with developers how to allow TITO in without TITO out (TITO config page without printer) | TBD | Normal | Customer request |
| 9 | Pavel Frolov | Finish MVP 2 machine-side features (~2 weeks) plus ~1 week testing | ~November 1, 2026 | High | Boot loop item not included in estimate |
| 10 | Pavel Frolov | Experiment on boot loop recovery without hard reset | TBD | Normal | Approach unknown |

## Open Questions

- Send MVP 1 to the lab now, or wait for MVP 2 (release ~November 9–10, one more week of delay)? Needs Val. (Felipe Miranda Giorgi)
- How to recover from a boot loop without a hard reset? Clearing last game status may lose records the Gaming Commission expects. (Pavel Frolov)
- Why does the machine stay locked after Intralot unlocks it, and does build 4333 fix it? (Felipe Miranda Giorgi, Pavel Frolov)
- How to configure TITO in without TITO out when there is no printer? (Felipe Miranda Giorgi)
- Should an RIS that requires a printer apply on a machine with no printer? (Sebastian Cortes)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-14*
*Source meeting: RIS MSVP2 Meeting*
