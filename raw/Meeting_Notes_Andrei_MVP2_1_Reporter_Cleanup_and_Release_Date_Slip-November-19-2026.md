# Meeting Summary — MVP2_1 and MVP2_2 scope recap and review
**Date:** November 19, 2026, ~8:04 AM – ~8:25 AM Eastern
**Duration:** ~21 minutes
**Attendees:** Andrei Klimovich (led, organizer), Pavel Frolov, Irina Shishko, Dzmitry Chudzinau, Val Levitan (briefly; left for a phone call)
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026]]

## Summary

**Goal.** Andrei: walk through MVP 2.1 first, then 2.2 if time allows. Make sure capabilities, features and requirements have current status, answer open questions and gaps, and update release expectations, because 2.1 is due tomorrow (Nov 20). Andrei went through both versions yesterday; all open questions he could answer are answered.

**CAP-267 (Flex IQ firmware management) — close it.** Irina: 267 was a placeholder with only test items and no developer features. She is almost done moving its TINTs plus the developer features into CAP-146; then 267 is closed. Pavel: 146 is Flex Port firmware update, 267 is Flex IQ firmware management. Andrei: by description, 267 (remote update from the dashboard, controlled rollout, campaigns) looks done in MVP 1. Dzmitry: auto-rollback happens by itself when the system does not come up. Pavel: the server-side tests were never automated (done by hand); they are very hard and need a separate cloud test environment, at best in 2.2; maybe not worth doing. Dzmitry: the one feature inside was created by an agent for simplifying build installers — infrastructure, nothing to test; it can be closed. Irina will tidy and close it.

**CAP-145 — too many unpublished requirements.** It holds 20+ requirements, not even in draft/published state. They belong to Anton Seregin and were created a month ago. Pavel offered to feed the list to Claude and make it compact. Val stepped in: capabilities are on the product owner's side, and requirements live with us a long time. Val then left for a call. Not settled.

**Port 13 terminal-update capability.** Holds tasks that do not belong (e.g., Evgeny's task to review generated Flex Port code quality and give coding rules). Pavel is the reporter; he agreed the unrelated tasks must be pulled out. Its fix version shows 22 while the capability is in 2.1.

**Way of working.** Andrei: doing this live on the call is not efficient. Everyone reviews the capabilities, features and requirements where they are the reporter, for 2.1 first (2.2 can wait until next week): wrong version, wrong status, or stale → clean it. Irina and Dzmitry agreed. Meet again tomorrow; Andrei agrees the time with Val.

**Field status.** No terminal in the field yet. Waiting for InComm registration — hoped for today; install follows. All hardware is in hand. Andrei must still review with Nathan what is left on the payment hub side (settlement with the other party); Nathan wrote an email yesterday.

**Release 2.1 date (Nov 20).** Pavel and Irina: not realistic. Dzmitry: the hard tasks are done — Flex Port Wi-Fi updates ready; SIM card data finishing today; Sergey likely did the terminal part. Left: autotests, small items, screen review. Maybe a weekend release. Irina: Monday, to finish and check the autotests. Pavel: stale requirements, if found still valid, may add work. No new date set.

## Decisions Made

- **Close CAP-267; its TINTs and developer features go into CAP-146.** — 267 was a placeholder; the only feature is infrastructure. (Irina, agreed by Andrei and Dzmitry)
- **Reporter clean-up is done offline, not on the call; MVP 2.1 first, 2.2 next week.** — Live review is not efficient. (Andrei; Irina, Dzmitry agreed)
- **The Nov 20 release date for 2.1 will not hold.** — Autotests not done and checked. No new date fixed. (Pavel, Irina)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Irina Shishko | Finish CAP-146 with the TINTs from 267 and developer features; tidy and close CAP-267 | Nov 19, 2026 | Normal | |
| 2 | All 2.1 reporters (Andrei K, Pavel, Irina, Dzmitry and team) | Review own capabilities/features/requirements for MVP 2.1: fix version, status, remove stale | Nov 20, 2026 | High | Before tomorrow's meeting |
| 3 | [Unassigned — needs clarification] (Anton Seregin's items) | Sort out the CAP-145 requirements with Anton: remove or publish | TBD | Normal | Created by Anton a month ago |
| 4 | Pavel Frolov | Pull unrelated tasks out of the Port 13 terminal-update capability | TBD | Normal | He is the reporter |
| 5 | Andrei Klimovich | Agree the time for tomorrow's follow-up meeting with Val | Nov 19, 2026 | Normal | |
| 6 | Andrei Klimovich | Review with Nathan what is still missing for payment processing (payment hub / settlement) | TBD | Normal | Nathan's email of Nov 18 |
| 7 | Dzmitry Chudzinau | Finish SIM card data collection | Nov 19, 2026 | Normal | |

## Open Questions

- CAP-145: shrink the 20+ requirements with Claude (Pavel), or keep them as product-owner material (Val)? Not settled.
- New release date for MVP 2.1: weekend (Dzmitry) or Monday Nov 23 (Irina)?
- Server-side update tests for CAP-267/146: worth doing at all, and only once a cloud test environment exists? (Pavel)

## Dispatch Log

---
*Processed from Teams transcript on November 19, 2026*
*Source meeting: MVP2_1 and MVP2_2 scope recap and review*
