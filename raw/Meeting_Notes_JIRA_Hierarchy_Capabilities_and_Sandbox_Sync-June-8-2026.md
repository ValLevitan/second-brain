# Meeting Summary — JIRA New Config: Build Capabilities & Sync the Sandbox
**Date:** June 8, 2026, 11:35 AM (Eastern)
**Duration:** ~9 minutes
**Attendees:** Val Levitan, Irina Shishko, Pavel Frolov
**Initiative:** [[Initiatives/JIRA Hierarchy Standard/statement_of_purpose|JIRA Hierarchy Standard]]
**In series:** IQ Deployment Jira Structuring (June 5) → this (June 8) → Services, Versions & Where Bugs Live (June 11)

> Note: short Russian planning call, rough speech-to-text; proper nouns were garbled (capabilities, Flex IQ, FlexPay, Flex Recycler, GitHub) and are corrected here. Two "Dima"s appear — Dzmitry Chudzinau and Dmitri Kovalchuk — separated by context. (The in-transcript clock is UTC; the meeting was 11:35 AM Eastern.)

## Summary

A short call to line up the next test of the new JIRA hierarchy configuration. Val had lost track of where they left off, so the group reset the plan.

The blocker is **capabilities**. For the new configuration to lay onto the transaction platform cleanly, every product needs its capabilities defined. Transactional (Transaction Galaxy) already has them; the IQ side does not. Flex Recycler has its capabilities; Flex IQ, FlexPay, the dispenser and the port do not. Some IQ capabilities do exist, but they were written in GitHub by Nathan — and they describe the **services** IQ needs (e.g. card issuance), not the IQ terminal itself.

The plan they agreed:

- **Val** writes the missing capabilities directly in JIRA — terminal (Flex IQ), dispenser (a couple, of three cycles), port, and FlexPay — by Tuesday/Wednesday.
- **Dmitri Kovalchuk** moves the existing service-side capabilities out of GitHub into JIRA.
- Only once the capabilities are filled in does **Dzmitry Chudzinau** sync the sandbox to the current state of JIRA — late Wednesday evening. The sandbox is about a month stale (possibly more — Pavel found no server-service IPs in it).
- The sync must not clobber the Transaction Galaxy changes already made in the sandbox. A plain re-export would lose them, so Dzmitry needs to be told which projects to leave alone and to pull the existing changes back in. They'll first ask him whether the current sandbox can be updated in place; if not, they'll find another way.

Separately, Pavel wants Dzmitry to finish the updated handoff for Nathan (invoices by ticket / by card, ~a couple of days) before pulling him onto this work.

They set the next working session for **Thursday, June 11 at 7:00 AM** so Dzmitry has time to trial the fit beforehand.

## Decisions Made

- **Capabilities come first.** Nothing can be tested against the transaction platform until each IQ-side product has its capabilities defined in JIRA. (Pavel, Val)
- **Service-side capabilities move from GitHub into JIRA before any sandbox sync.** (Val)
- **The sandbox sync happens late Wednesday evening, after the capabilities are filled in,** and must preserve the Transaction Galaxy changes already in the sandbox. (Val, Irina, Pavel)
- **Next session: Thursday, June 11, 7:00 AM.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Write the missing capabilities in JIRA for the IQ-side products — terminal (Flex IQ), dispenser (a couple), port, FlexPay | Tue–Wed, June 9–10 | High | Gates the whole test; dependencies can't be built without them |
| 2 | Pavel Frolov / Irina Shishko | Ask Dmitri Kovalchuk to move the existing service-side capabilities (card issuance etc., written by Nathan) from GitHub into JIRA | Before the sync | Normal | The existing IQ capabilities live in GitHub, not JIRA |
| 3 | Pavel Frolov / Irina Shishko | Ask Dzmitry Chudzinau to sync the sandbox to current JIRA late Wed evening (June 10) — telling him which projects to leave untouched, and pulling the existing Transaction Galaxy changes back in so they aren't lost | Wed evening, June 10 | High | Sandbox ~1 month stale; a plain re-export would wipe their sandbox work |
| 4 | Pavel Frolov | Have Dzmitry first finish the updated handoff for Nathan (invoices by ticket / by card) before pulling him onto the hierarchy trial | ~Tue–Wed | Normal | ~2 days; then he's free to help |
| 5 | Val Levitan | Hold the follow-up session — Thursday, June 11, 7:00 AM | June 11 | Normal | So Dzmitry can trial the fit first |

## Open Questions

- **Can the current sandbox be updated in place,** or must a fresh export be made (which would lose the Transaction Galaxy changes)? To be asked of Dzmitry.
- **Exactly how stale is the sandbox** — about a month, but possibly more since Pavel found no server-service IPs in it. Dzmitry to confirm.

---
*Processed from Teams transcript on June 11, 2026.*
*Source meeting: JIRA_Plan_NEW_configuration-20260608_113555*
