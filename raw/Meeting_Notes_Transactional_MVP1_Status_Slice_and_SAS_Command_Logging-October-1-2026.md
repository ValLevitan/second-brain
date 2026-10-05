# Meeting Summary — Transactional MVP1 sync
**Date:** October 1, 2026, 8:02 AM – 8:18 AM Eastern
**Duration:** About 16 minutes
**Attendees:** Andrei Klimovich (organizer), Pavel Frolov, Irina Shishko, Dzmitry Chudzinau, Andrei Bosik, Alexander Biratko, Alexey Khamin, Ivan Shpak
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_Status_Slice_and_SAS_Command_Logging-October-1-2026]]

Held in Russian. Previous sync: [[Meeting_Notes_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026]].

## Summary

**MVP1 status as of October 1.** Pavel showed the Jira board. MVP1 starts at CAP-122. The top capabilities are in Request Review: developers closed all their features, and only testing and autotest tasks remain. Still open (In Progress or To Do): CAP-165 to CAP-174. Andrei Klimovich asked about due dates of October 22–23. Dzmitry said those include autotests, since development and tests are mixed. Irina will give the testing update tomorrow.

**What is left in development.** Dzmitry said the main work is ending. Left: reprint (simple), records, and a new capability: receive all SAS commands from machines, ours and others, and log them. The goal is to see how each machine answers our commands and what it expects. Pavel said this builds statistics on which SAS commands other machines support, so the team knows which ones to implement. It must be tested on a real game machine. With weekend work, Dzmitry expects everything done by Sunday or Monday. Pavel said that looks about right.

**Mockups vs requirements.** Dzmitry has a set of documents on contradictions and gaps (missing tests, negative cases). He will review it and send it within an hour or two, as a new email to the Transactional mailing group. He and Sergey work from mockups first, because the requirements are abstract. He asked Andrei Klimovich to update the requirements. Andrei said he ran Claude to match mockups and requirements, but it surely missed some things.

**Firewall on the terminal (Andrei Bosik).** Bosik pushed (and merged yesterday) firewall changes that cut outside network access to the terminal. He needs a SIM card to test it. Dzmitry put a fresh build on terminal 84 today, so the change should be there. The only SIM is with Ivan, who is testing the GOM V3 with a modem. Pavel offered his own SIM for a short time. Bosik will wait for Ivan's SIM and then have Claude run the test cases.

**More SIM cards.** Pavel had asked KORE (transcribed "кору") to send more SIMs to Minsk. They said "no problem," but nothing followed. Andrei Klimovich said the contract covers all US states; use abroad is an open question. He will pick up the request. Bosik's own unanswered email to them is no longer needed.

**Georgia test setup.** Andrei Klimovich gave Elizabeth the task in Teams yesterday. She has not replied. He will ping her today for a start date. Everything needed to test the full setup with JVL's machine is ready.

**MVP2 (Alexander).** Alexander has no questions. He will review the existing capabilities and drop the outdated or wrong ones. He will port the Flex IQ capabilities that apply to FlexPay, by analogy. He does not want to write new ones without business confirmation; Andrei Klimovich must first think through the user and admin flows.

**Andrei Klimovich away.** He cannot write anything until he returns on October 13. Next week, Tuesday to Thursday, he will miss even the dailies. Irina said the team still needs its own sync; they also sync at 3:00 at their local daily. Val is on those meetings and can read everything. Agreed: no MVP sync Tuesday to Thursday next week; meet tomorrow and on Monday.

**Hot items.** Elizabeth must check the test build in Georgia. By Monday, client features should be ready to deploy and test user flows. Autotests are still awaited.

## Decisions Made

- **No Transactional MVP sync Tuesday–Thursday next week (Oct 6–8); meet Oct 2 and Monday Oct 5.** (Andrei Klimovich; agreed by Pavel Frolov and Irina Shishko)
- **For MVP2, Alexander ports existing Flex IQ capabilities to FlexPay and drops wrong ones, but writes no new ones until the business flows are defined.** (Alexander Biratko; endorsed by Andrei Klimovich)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dzmitry Chudzinau | Review and send the mockups-vs-requirements gaps document to the Transactional mailing group | Oct 1, 2026 | Normal | "within an hour or two" |
| 2 | Andrei Klimovich | Update the requirements from Dzmitry's gaps document | TBD | Normal | Away until Oct 13 |
| 3 | Dzmitry Chudzinau | Finish reprint, records and SAS command logging for MVP1 | Oct 5, 2026 | High | "by Sunday or Monday" |
| 4 | Andrei Bosik | Test the terminal firewall with Claude once Ivan's SIM is free | TBD | Normal | |
| 5 | [Needs Val's confirmation] Pavel Frolov or Ivan Shpak | Tell Andrei Bosik when Ivan no longer needs the SIM | TBD | Normal | Bosik said "let me know"; the transcript does not show to whom |
| 6 | Andrei Klimovich | Follow up with KORE on more SIM cards for Minsk | TBD | Normal | |
| 7 | Andrei Klimovich | Ping Elizabeth for a start date on the Georgia test setup | Oct 1, 2026 | High | |
| 8 | Irina Shishko | Give the MVP1 testing status update | Oct 2, 2026 | Normal | |
| 9 | Alexander Biratko | Review MVP2 capabilities: drop wrong ones, port Flex IQ ones to FlexPay | TBD | Normal | |

## Open Questions

- Can KORE SIM cards be used outside the US (in Minsk)? (Andrei Klimovich)
- User and admin flows for MVP2 are not defined yet. (Alexander Biratko)

## Dispatch Log

---
*Processed from Teams transcript on October 1, 2026 (meeting-watcher)*
*Source meeting: Transactional MVP1 sync*
