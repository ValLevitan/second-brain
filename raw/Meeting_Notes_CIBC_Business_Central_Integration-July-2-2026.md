# Meeting Summary — CIBC / JVL Account Structure & Business Central Integration
**Date:** July 2, 2026 (~22 min)
**Attendees:** Val; Michael Hill (CIBC); Sanjay Vishwanathan (CIBC); one unnamed advisor asking questions on Val's behalf

## Summary

The call was about how to set up CIBC accounts to receive third-party ("aggregator") payments for JVL.

**Val's original design.** One account that always stays at zero ("funding account"). When money arrives, take an electronic reading (an API call — "how much is in the account now?"), then trigger a *forced* transfer of that exact amount into a second accumulation/operating account. Each event gets a date-and-time stamp and the amount. Val wants the account brought back to zero only on command, never automatically, and wants exact purity between what is received and what is moved.

**CIBC's answer (Michael).** Their zero-balance account does not work that way. It sweeps automatically at end of day, not on command. The only two options are: (1) manual transfers Val does himself, or (2) automatic end-of-day sweep. There is no API-triggered on-command force transfer. Val said frequent manual transfers would be too much overhead. Converting to this account type would also change JVL's fee structure — JVL currently has small-business / business-banking accounts, not analysis accounts.

**The counter-suggestion.** Michael and the advisor questioned whether the API-approval step is needed at all. Every deposit is already visible in the account with its own timestamp. Between start and end of day the accountants can see all credits and reconcile them against the aggregator's report/invoices. If there's a mismatch, Val raises it with the aggregator. Simpler than building an API layer at the bank.

**Val reconsidered.** He accepted the original architecture may have been over-thought and decided to try a single-account approach first before opening a second account.

**Integration.** Accounts are run electronically (online or via a tool through an API). CIBC used QuickBooks as an example; Val uses **Microsoft Business Central**. CIBC confirmed it has clients integrating Business Central and that the connection just needs to be "turned on." Monica (working with Michael) was already in the process of enabling this "open access" API — Michael had sent her instructions. Most of the integration work happens on the Business Central side, not CIBC's.

## Decisions Made
- **Do not open the second account yet.** Sanjay offered to send paperwork Monday; Val told him to hold. (Decided by Val) — *Note: reversed on July 7, see Update below.*
- **Try the single-account approach first** — one operating account integrated with Business Central, with reconciliation done by the accountants against the aggregator's report, instead of the API-force-transfer design. (Val, taking Michael's suggestion) — *Note: superseded on July 7, see Update below.*
- **Operating account should be a money-market account** so it earns cash back / interest. (Raised by advisor, agreed)
- **Contact protocol:** Val reaches Michael through Sanjay.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Confirm with Monica whether she has already turned on the CIBC "open access" API / Business Central connection | TBD | High | If already done, no further setup needed |
| 2 | Val | Work with Monica and his tech person to enable the Business Central integration on the existing account | TBD | High | Val called this urgent |
| 3 | Val | Verify the currently-open account can receive ACH deposits and access Business Central | TBD | High | Wants to start on one account |
| 4 | Val | Arrange a follow-up call (Monica + CIBC via Sanjay, plus his tech guy if needed) | TBD | Normal | Only after checking Monica's progress |
| 5 | Sanjay (CIBC) | Hold off on opening the second JVL account — do not send Monday paperwork | — | Normal | Val paused it (later resumed, see Update) |
| 6 | Monica | Complete turning on the open-access / Business Central integration (if not already done) | TBD | High | Michael already sent her directions |

## Open Questions
- Has Monica already enabled the open-access API, or is it still pending?
- Does CIBC have native Business Central integration, or is all the work on the Business Central side?
- Will single-account reconciliation fully replace the original API-force-transfer design, or is the second zero-balance account still needed later?

---

## Update — Email thread "JVL/CIBC ACH payment processing" (July 6–8, 2026)

The email thread that followed the call resolves the open questions above and **reverses two of the July 2 decisions.**

**Participants:** Monica Levitan (JVL, Director of Corporate Compliance); Michael Hill (CIBC); Val; Nathan Carver (JVL developer); Sanjay Vishwanathan (CIBC).

**What was agreed:**
- **ZBA auto-sweep accepted.** With a zero-balance account, funds move to the designated secondary account automatically — the API does not (and cannot) trigger the transfer; it is a built-in ZBA function. Val: *"THIS IS ACCEPTABLE. NO ISSUES."* The original API-forced-transfer design is dropped.
- **Account upgrade approved.** JVL's accounts must be upgraded to "analysis accounts" to enable the ZBA feature and batch-payment visibility. Val: *"AGREED — PLEASE, GO AHEAD."* This reverses the July 2 "don't open the second account / try one account first" position.
- **API role is now reconciliation only.** After each auto-sweep the payment is reconciled to confirm sender name, date, and amount.
- **Nathan Carver owns the API/reconciliation work** and will be looped in once the analysis account is open. He asked Michael to share documentation beforehand.

**Confirmed flow (per Michael's recap):**
1. Third-party vendor sends all received payments to a ZBA account at CIBC.
2. Each payment sits in the ZBA, then auto-sweeps to the designated secondary CIBC account.
3. After transfer, the payment is reconciled (sender name, date, amount).

**July 8 developments (resolving the open items above):**
- **Timeline given.** Sanjay's team has submitted the request to open the new account; the signature documents "should be available for signature within the next couple of days" (Michael, July 8).
- **Nothing needed from Monica yet.** Michael confirmed nothing needs to be completed on Monica's end at this time — once the account is open there will be "a couple of docs" for her to sign. Monica acknowledged and will watch for the documents.
- **Nathan's request acknowledged.** Michael replied "Will do!" to Nathan's ask to be looped in for the ZBA + batch-read setup and to receive documentation beforehand.

**Still open:**
- Sanjay's team to **open the account** (docs expected for signature within a couple of days of July 8).
- Once open, **Monica signs** the account docs; **Michael loops Nathan in** and shares documentation for ZBA + batch-read setup.
- Nathan then wires up **reconciliation in Business Central**.

---
*Processed from Teams transcript (July 2, 2026 call) and Outlook thread "JVL/CIBC ACH payment processing" (July 6–8, 2026), on July 9, 2026.*
*Source meeting: CIBC / JVL Account Structure & Business Central Integration*




---

## Update — Email thread continued (July 9–13, 2026)

**The account is now LIVE.**

- **New account opened and live.** Sanjay confirmed (July 13): *"The new account went live last week. The account number is [account # — held in Corporate Registry]. All the other details (ABA) etc. remain the same."* → **New account #: [account # — held in Corporate Registry]**; ABA/routing and all other details unchanged.
- **Signature docs completed (July 9).** Monica signed and returned the account-opening documents. The exchange hit repeated snags — the PDF arrived corrupted / damaged several times and once was missing signatures; Sanjay ultimately asked Monica to snip the signature page and paste it into the email body. Resolved same day — Sanjay confirmed July 9: *"The account will go live today."*
- **Monica's July 13 check-in.** Monica emailed Michael and Sanjay asking (1) whether the account was set up and if anything else needs to be signed, and (2) whether Nathan has been given the information he needs to integrate the API. Sanjay's reply confirmed the account is live and details unchanged; the API-info question to Nathan was **not explicitly answered** in his reply.

**Now resolved (from the July 8 "Still open" list):**
- ✅ Account opened — live as of ~week of July 6; account # [account # — held in Corporate Registry].
- ✅ Monica signed the account docs (July 9).

**Still open:**
- **Confirm Nathan has the integration details** — Monica's question about whether Nathan received the API info was not directly addressed in Sanjay's reply. Follow up so Nathan can begin the ZBA + batch-read setup.
- **Michael loops Nathan in** and shares ZBA / batch-read documentation.
- Nathan wires up **reconciliation in Business Central** against the account (# [account # — held in Corporate Registry]).

*Processed from Outlook thread "JVL/CIBC ACH payment processing" (July 9–13, 2026), on July 13, 2026.*
