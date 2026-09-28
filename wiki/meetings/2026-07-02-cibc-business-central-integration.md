---
type: meeting
title: CIBC / JVL account structure & Business Central integration (July 2 2026)
date: 2026-07-02
aliases: [CIBC Business Central integration, aggregator payment account, ZBA account structure, CIBC ACH account architecture, ACH receiving-account architecture, Banking Architecture Pivot]
source-count: 3
---

# CIBC / JVL account structure & Business Central integration (July 2 2026)

**Date:** July 2, 2026, 11:07 AM ET (~22 min) [[raw/Meeting_Transcript_CIBC_ACH_Account_Architecture-July-2-2026.md]]
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]]; Michael Hill (CIBC); Sanjay Vishwanathan (CIBC); a third voice ("Speaker 3") whose identity is unclear — possibly Sanjay, while one set of notes calls this person an unnamed advisor. [[raw/Meeting_Transcript_CIBC_ACH_Account_Architecture-July-2-2026.md]] [[raw/Meeting_Notes_CIBC_Business_Central_Integration-July-2-2026.md]]

A CIBC call on how to set up JVL's CIBC accounts to receive third-party ("aggregator") payments, and on connecting those accounts to Microsoft Business Central. Val walked through his zero-balance-account design; CIBC explained its zero-balance account sweeps only at end of day; Val chose to try a single account first. [[raw/Meeting_Transcript_CIBC_ACH_Account_Architecture-July-2-2026.md]]

**One meeting, three files (§12).** The notes-only file first stubbed here and the later-staged transcript + notes pair ("ACH Account Architecture") describe the same call: same date, same ~22 minutes, same two CIBC bankers, same design debate and outcome. The transcript is the source of record.

**Notes vs transcript.** Where the derived notes differ, the wiki follows the transcript: (1) the older notes said a **money-market** operating account was "agreed" — in the transcript Val says "No, no, that's an operational account", i.e. a checking account; (2) the newer notes name "Nathan's lane" as Val's tech person and call the ZBA "later in production" — neither is in the transcript; (3) the older notes say Monica was "already in the process" of enabling the link — the transcript only says she had Michael's directions and "may have already initiated this". [[raw/Meeting_Transcript_CIBC_ACH_Account_Architecture-July-2-2026.md]] [[raw/Meeting_Notes_CIBC_Business_Central_Integration-July-2-2026.md]] [[raw/Meeting_Notes_CIBC_ACH_Account_Architecture-July-2-2026.md]]

Substance:
- Banking / account-structure and aggregator-payment facts → [[wiki/organizations/cibc.md]] (July-2 section).
- The Business Central integration / reconciliation side → [[wiki/topics/business-central-erp-implementation.md]] (July-2 section).
- Monica's role in turning on the link → [[wiki/people/monica.md]] (July-2).

§15 #9: no account or routing numbers appear in the transcript. The older notes file carries an email-thread update (July 6–13) that is out of scope per §1 and is not used here.

## Sources
- [[raw/Meeting_Transcript_CIBC_ACH_Account_Architecture-July-2-2026.md]]
- [[raw/Meeting_Notes_CIBC_ACH_Account_Architecture-July-2-2026.md]]
- [[raw/Meeting_Notes_CIBC_Business_Central_Integration-July-2-2026.md]]
