# Meeting Summary — MVP2 Transactional planning
**Date:** November 12, 2026, 8:33 AM – 9:21 AM Eastern
**Duration:** ~48 minutes
**Attendees:** Pavel Frolov (organizer), Val Levitan, Andrei Klimovich, Andrei Bosik, Dzmitry Chudzinau, Irina Shishko, Alexander Biratko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_MVP2_Capability_Review_Goods_Category_Master_Role_and_Release_Split-November-12-2026]]

## Summary

**Goal.** Andrei Klimovich wanted every MVP 2 capability moved from Proposed to Accepted, or its problems flagged. He already gets comments (from Dzmitry) and fixes requirements as they come.

**Purpose of design.** Val asked that every capability discussion start from the "purpose of design": why we do it and what problem it solves. Andrei explained MVP 2: faster, cheaper installs with Wi-Fi from port to gateway; remote port firmware updates instead of site visits; better monitoring (alerts, SIM data use, port status); money reporting to operators and location owners; and a report printed on Flex IQ. Val added: Wi-Fi is the preferred option, but wired install stays because Wi-Fi may not work everywhere; for updates wired and Wi-Fi are the same. Val asked Andrei to rewrite this text as prose, at most two paragraphs, simple ESL English, a business "why", not a technical "how". Pavel asked to keep numbering; Val said no.

**Audit report.** "Inspector report" is the wrong name, even internally. It is now "Audit report".

**SIM data.** Pavel: in this release we only send SIM information and link it to the location; reporting is done later on the server. Val agreed: once release 2 is at a location, the server must be able to grow without any change on the IQ.

**"Lottery" becomes "Goods".** CAP-159 adds a "Lottery" product: the cashier can split a payout between lottery, gift card or ticket. Andrei noted that since July 1, 2026 winnings may only be paid as lottery tickets or gift cards. Val rejected the name: locations need flexibility to call the category what they want. Configurable categories come in MVP 3; MVP 2 has one fixed category with a generic name, "Goods". Colors or a special screen for it can wait.

**Other review points.**
- Machine names: a requirement already covers naming a machine in port settings on IQ, including machine and port swaps. Dzmitry will read it.
- CAP-312: a port cannot report "not connected to master", since it has no other link. Andrei already answered Dzmitry's comments.
- Reports: requirement 2066 is the audit report (printed or emailed from IQ); requirement 2069 is the operations dashboard.
- Roles: "master" in business terms is the Georgia master license holder (operator); the location owner holds a location license. The "master" on IQ is just an admin settings login. MVP 2 adds a Master role on the web (CAP-367): linked by master license number, sees all its locations. Without it masters see nothing of installed locations.
- Alerting will be set up in Grafana. That is a task, not a feature.

**Release split.** Dzmitry said the IQ and port work is ready and the server work does not block it. Agreed to split MVP 2: first IQ + port (Wi-Fi, remote port update, payout split, audit report), priority 1; web services second. Named MVP 2_1 and MVP 2_2; Pavel creates them now. Val: only Irina or Pavel create releases, not Andrei. Capabilities are sorted after the review: any capability with a port or IQ feature goes to 2_1. Team finishes the full review in the remaining days this week; comments in Jira, tag Andrei.

**Recycler.** Originally Flex-Pay Slim was planned for MVP 3 in January; now the recycler comes first. Recycler MVP 1 is planned for the end of next week (Thursday, November 19). Base it on Flex-Pay with the recycler in place of the validator and coin dispenser. Design language stays, layouts may change. Andrei prepares updated recycler capabilities by Sunday. Meeting Sunday at 8 AM Eastern (4 PM Minsk) with Andrei K, Irina, Alexander, Pavel and Val. Pavel already created the recycler version with three capabilities.

**Closing.** Val reminded Andrei Bosik of CI/CD for the recycler for Thursday. Val asked Andrei K to email Elizabeth that a recycler must be ready Thursday; Andrei said one is in the demo room with the old validator; Val said a JCM validator should also be there.

## Decisions Made

- **Purpose of design is written as prose, at most two paragraphs, simple English, business reason; no numbering.** (Val; Pavel's numbering idea declined)
- **"Inspector report" is renamed "Audit report" everywhere.** (Val; Andrei agreed)
- **MVP 2 sends SIM data and links it to the location; reporting is built on the server later without IQ changes.** (Pavel, Val)
- **The "Lottery" product is renamed to a generic "Goods" category; MVP 2 has one fixed category, configurable categories in MVP 3.** (Val; Andrei agreed)
- **MVP 2 splits into MVP 2_1 (IQ + port, priority 1) and MVP 2_2 (web services, priority 2).** (Andrei, Pavel, Dzmitry, Irina)
- **Releases are created only by Irina or Pavel.** (Val)
- **Recycler MVP 1 targets Thursday, November 19, built on current Flex-Pay screens without a design change.** (Alexander, Pavel; Andrei agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Rewrite the MVP 2 purpose of design as two-paragraph prose | TBD | High | Right after the call |
| 2 | Andrei Klimovich | Replace "inspector" with "audit report" in all texts | TBD | Normal | |
| 3 | Andrei Klimovich | Rename "Lottery" to a generic "Goods" category | TBD | Normal | |
| 4 | Pavel Frolov | Create releases MVP 2_1 and MVP 2_2 | Nov 12, 2026 | High | "Doing it now" |
| 5 | Dzmitry Chudzinau, Pavel Frolov, Irina Shishko, Alexander Biratko | Finish the full MVP 2 capability review; comment in Jira, tag Andrei | Nov 13–15, 2026 | High | "Remaining days this week" |
| 6 | Irina Shishko | Write autotests for accepted requirements | TBD | Normal | |
| 7 | Dzmitry Chudzinau | Read the machine-naming capability | TBD | Normal | |
| 8 | Andrei Klimovich | Prepare updated recycler capabilities and requirements | Nov 15, 2026 | High | Before Sunday meeting |
| 9 | Andrei Klimovich | Book Sunday recycler meeting (Irina, Alexander, Pavel, Val) | Nov 15, 2026, 8 AM ET | High | Val asked to be included |
| 10 | Andrei Bosik | CI/CD for the recycler | Nov 19, 2026 | High | Val's reminder |
| 11 | Andrei Klimovich | Email Elizabeth that a recycler must be ready Thursday | Nov 19, 2026 | Normal | One is in the demo room |

## Open Questions

- Is a JCM validator unit in the demo room, or only the old one? (Val thought JCM was received)

## Dispatch Log

---
*Processed from Teams transcript on November 12, 2026 (scheduled meeting-watcher)*
*Source meeting: MVP2 Transactional planning*
