---
type: decision
title: Bank of America scope — prior-day reporting by API; ACH debits can only go by NACHA file
date: 2026-09-08
aliases: [prior-day reporting only, no ACH debit API, hybrid API-and-file payments, CashPro gating]
source-count: 4
status: active
open-questions: 1
---

# Bank of America scope — prior-day reporting by API; ACH debits can only go by NACHA file

**Decided:** September 8 2026, on the [[wiki/meetings/2026-09-08-bank-of-america-cashpro-api-capabilities.md|Bank of America CashPro API call]] (12:30–1:05 PM Eastern). [[raw/Meeting_Notes_Bank_of_America_CashPro_API_Integration-September-8-2026.md]]
**By:** [[wiki/people/nathan-carver.md|Nathan Carver]] for the technical scope; the debit constraint is Bank of America's, stated by its specialist Connie Burke, not a JVL choice. [[wiki/people/val-levitan.md|Val]] attended for executive decisions only.

## What was decided

- **The immediate API scope is prior-day reporting only.** Nathan: "the immediate need is definitely prior day covers what we need as we'll be looking back in as transactions clear… I don't see an immediate current day need." Bank of America offers a current-day API too; it was set aside. [[raw/Meeting_Transcript_Bank_of_America_CashPro_API_Integration-September-8-2026.md]]
- **ACH debits cannot use an API — they must be a NACHA file.** "At this time, Bank of America does not have an API for ACH debits." The file goes either over a secure SFTP connection or by manual upload into CashPro Online, with an approval step before the bank sends it downstream. Credits out and international wires *do* have APIs, so only the debit leg is forced onto a file. [[raw/Meeting_Transcript_Bank_of_America_CashPro_API_Integration-September-8-2026.md]]
- **The shape that follows is a hybrid: API for reporting, file for payments** — the pattern Connie said many of her clients land on. Whether credits and wires go by API or by file was left open: consistency argues for putting everything on one file, immediacy argues for the API. [[raw/Meeting_Transcript_Bank_of_America_CashPro_API_Integration-September-8-2026.md]]
- **No pre-CashPro sandbox request.** A developer can reach a "pseudo sandbox" via an IP whitelist without CashPro credentials, but Nathan declined it and asked for documentation first: "I don't really need a sandbox outside of Cash Pro being set up." He will request sandbox access once CashPro exists. [[raw/Meeting_Transcript_Bank_of_America_CashPro_API_Integration-September-8-2026.md]]
- **CashPro implementation gates everything.** Whatever the API, "the conduit for that is our Cash Pro system" — it must be implemented, the users entitled, and one specific user granted access to the reporting API. None of the above can start before that. [[raw/Meeting_Transcript_Bank_of_America_CashPro_API_Integration-September-8-2026.md]]

## Why it matters

Two consequences follow from the missing debit API. First, JVL cannot fire an API call per transaction as debits arise; each debit has to be added to a batched file — the point Nathan restated back to Connie and she confirmed ("You got it"). Second, remittance detail lives on the file, not the API: API credits carry no addenda at all, while a NACHA file carries up to 80 characters (on "a TBD plus or a CCD plus" — the transcript's first term is garbled) or up to 9,999 on a CTX. If JVL wants invoice references travelling with its payments, that argues for the file. [[raw/Meeting_Transcript_Bank_of_America_CashPro_API_Integration-September-8-2026.md]]

Nothing here is committed yet: the whole path is downstream of Val approving Brooks Darnell's pricing proposal, and Val said there was no urgency. Full detail on [[wiki/organizations/bank-of-america.md]] (Sept 8). [[raw/Meeting_Transcript_Bank_of_America_CashPro_API_Integration-September-8-2026.md]]

## Oct 13 2026 update — ACH starts with manual NACHA file upload

On the [[wiki/meetings/2026-10-13-bank-of-america-cashpro-business-central-source-of-truth-and-customer-ach-portal.md|Oct 13 CashPro call]] Brooks Darnell restated the order of work from Connie — CashPro first, then the sandbox, then the API team gives next steps — and that the main priority from Sept 8 is still API reporting of "prior day balances and transactions" [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]. On ACH he gave the choices: import a NACHA file from the accounting software, upload it into CashPro and approve it there; or transmit files over a secure connection, which costs more. Val: "that's exactly how we're planning to start" — the manual upload. Brooks: "We can always change that" if volume grows [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]. The notes record it as decided by Val [[raw/Meeting_Notes_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]. **Evolution, not contradiction:** Sept 8 left the file route open between SFTP and manual upload; Oct 13 picks manual upload to start. Wires and the vendor-data rule are on [[wiki/decisions/2026-10-13-business-central-is-the-only-source-of-truth-for-vendor-bank-details-and-wires-take-them-from-it-every-time.md]].

## Open questions

- Whether JVL brings ACH debits in-house to Bank of America **at all** was explicitly not decided — Nathan called it "worth exploring… as the future, future possibilities." The third party currently absorbs the NACHA work while JVL stays "accountable for all the Notch [NACHA] rules." [[raw/Meeting_Transcript_Bank_of_America_CashPro_API_Integration-September-8-2026.md]]

## Sources

- [[raw/Meeting_Notes_Bank_of_America_CashPro_API_Integration-September-8-2026.md]]
- [[raw/Meeting_Transcript_Bank_of_America_CashPro_API_Integration-September-8-2026.md]]
- [[raw/Meeting_Notes_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
- [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
