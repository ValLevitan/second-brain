# Meeting Summary — Bank of America (CashPro): API capabilities for Business Central reconciliation and payment initiation

**Date:** September 8, 2026, 12:30 PM – 1:05 PM Eastern
**Duration:** ~34m 10s
**Attendees:** Val Levitan (JVL), Nathan Carver (JVL, drives the technical side), Brooks Darnell (Bank of America, runs the engagement), Connie Burke (Bank of America, API/treasury specialist), Linda Hernandez (Bank of America, relationship manager for JVL — on the line), "Lennon" (Bank of America, handles account coding — name spelling unconfirmed, see note)
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar match:** paired with the Outlook event **"JVL SYSTEMS INC/ Treasury needs review"**, 12:30–1:30 PM Eastern, organized by brooks.a.darnell@bofa.com. Two-key rule satisfied — time overlap plus "Brooks" and "Bank of America" both spoken in the transcript.

**Raw transcript:** [[Meeting_Transcript_Bank_of_America_CashPro_API_Integration-September-8-2026]]

## Summary

**What JVL is trying to do.** Nathan set out a two-stage goal. Short term is reconciliation: a daily API call that pulls balances and cleared transactions so JVL can verify money actually moved and match it inside Business Central. Not a month-end job — a daily check. Longer term is initiating money movement from JVL's own systems: today ACH debits run through a third-party provider that abstracts the NACHA layer away, and Nathan wants to know what it looks like to bring that in-house with Bank of America. Val added the other side of it — JVL pays suppliers, many in China, by wire, always in US dollars.

**The reporting piece is straightforward.** Bank of America already has prior-day and current-day balance and transaction APIs. The prior-day call typically runs around 7 AM, pulls the previous day's balances and transactions, and Business Central handles the matching rules from there. Nathan confirmed prior-day covers the immediate need and he sees no current-day requirement.

**Everything runs through CashPro, and CashPro has to exist first.** That is the gating item. The API conduit is the CashPro system: it must be implemented, users entitled, and one specific user granted access to the prior-day reporting API. A designated primary administrator — Connie recommends at least two — requests sandbox access through the API Developer Studio, then production access later. Authentication is OAuth token-based and runs system-to-system rather than as a named person, but an active CashPro user still has to sit behind the connection as the conduit. Customer ID and secrets come during setup.

There is a pre-CashPro option: a "pseudo sandbox" a developer can reach with an IP whitelist and no CashPro credentials, useful just to look at what APIs exist. Sandbox access has to be requested again once CashPro is live. Nathan decided he does not need it — documentation first, so he can ask better questions.

**The real constraint: Bank of America has no API for ACH debits.** This is the finding that shapes the architecture. Credits out have an API. International wires have an API. Debiting customers does not — that has to be a NACHA file, either transmitted over secure SFTP or uploaded manually into CashPro Online, with an approval step before it goes downstream. Connie's practical advice was the hybrid many of her clients land on: API for reporting, file for payments. She also noted that if JVL is already producing a NACHA file for its third-party provider, that same file can be transmitted to Bank of America instead.

**Details that will matter when this is built:**

- **Lead times.** ACH is next-day availability as standard, with one-day or two-day lead options. Same-day ACH is possible if the file arrives before roughly 2:30 PM Eastern — Connie explicitly said not to quote her on the cutoff. ACH is a US-only rail.
- **You cannot mix file-in with API-status-out.** Send a file, you get a file status back or alerts and statements inside CashPro. Send via API, you get status APIs and webhooks. There is no hybrid on a single transaction.
- **Remittance detail favours the file.** API credits carry no addenda at all — no invoice number, nothing telling the recipient why they were paid. A NACHA file carries up to 80 characters on a CCD+ or PPD+, or up to 9,999 characters on a CTX. If JVL wants invoice references travelling with payments, that argues for the file.
- **Returns and NSF.** Bank of America sends a returns notification, but it is mostly a visual in CashPro — PDF or text. Connie thinks a NACHA-format return may be available to parse back into Business Central and will confirm. File acknowledgements show up to about twenty rejects with reason lines, again as a visual rather than something machine-parsed.

**Volumes.** Brooks had JVL listed at 25–30 wires a month. Val said about ten and roughly $150,000 a month, then clarified he was thinking only of China and that the 25–30 includes domestic. He was candid that he had not sat down and calculated it — his words, the numbers are approximations and a placeholder. Connie's read either way: at that volume wires are manageable through CashPro Online with per-vendor templates, no API needed.

**Where it goes next and how long it takes.** Brooks will put together a pricing proposal covering all the services — he aimed for the same day but flagged he was booked back-to-back until 5:30, so realistically the next day. Val said there is no urgency. Once Val approves the pricing, the sequence is: account coding by Lennon, three to five business days, call it a week; then repapering the account, another week; then implementation, three to five weeks, depending on how responsive things are and including training and entitlement setup. That is roughly five to seven weeks from approval before the system is usable.

Val stated at the top that he was attending only for executive decisions and would otherwise stay silent — Nathan owns the technical conversation.

## Decisions Made

- **Immediate scope is prior-day reporting only.** Nathan confirmed prior-day covers the need; no current-day requirement was identified.
- **Payments will be a hybrid architecture.** ACH debits must go by NACHA file because no debit API exists. Credits and wires can go either way — API or file — and the choice is open.
- **No pre-CashPro sandbox request.** Nathan takes documentation first and requests sandbox access once CashPro is implemented.
- **CashPro implementation is the gating dependency** for every API path discussed.
- **No urgency on the pricing proposal** — Val told Brooks the next day is fine.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Brooks Darnell (BofA) | Send Val the CashPro pricing proposal listing all services | Target Sep 8, realistically Sep 9 | High | Gates the whole implementation; Val's approval is the trigger |
| 2 | Connie Burke (BofA) | Send API documentation, step-by-step connection guide and JSON tips, routed via Brooks and Lennon | Open | High | Nathan's stated next step depends on this |
| 3 | Val | Approve the pricing proposal to start implementation | Open | High | Nothing moves until this happens |
| 4 | Connie Burke (BofA) | Confirm what happens to a file whose effective date falls on a non-banking day — held to the next window, or rejected | Open | Normal | Connie made herself a note; matters because JVL uploads daily including weekends |
| 5 | Connie Burke (BofA) | Confirm whether returns/NSF can be delivered in NACHA format for parsing into Business Central rather than only as a CashPro visual | Open | Normal | Determines whether failure handling can be automated |
| 6 | "Lennon" (BofA) | Account coding once pricing is approved | 3–5 business days after approval | High | First step of implementation |
| 7 | Nathan Carver | Review API documentation, then request sandbox access after CashPro is set up | Open | Normal | Deliberately sequenced after docs |
| 8 | Brooks Darnell (BofA) | Reconcile the wire volume figure for pricing (25–30/month domestic + international vs Val's ~10 China-only) | Open | Low | Val flagged his own numbers as a placeholder |

## Open questions

- **Non-banking-day file handling** — held or rejected. Unanswered; Connie is checking.
- **Can NACHA-format returns feed Business Central**, or is failure handling stuck as a manual read of a CashPro PDF? This decides how automated the daily run can actually be.
- **Actual wire and ACH volumes.** Val's figures are self-declared approximations, and pricing is being built on them.
- **Whether to bring ACH debits in-house at all.** The third party currently absorbs the NACHA complexity while JVL stays accountable for NACHA rules. Moving to a Bank of America file trades one integration for another, and no decision was taken.
- **API vs file for credits and wires.** Connie laid out both; consistency argues for file, immediacy argues for API. Left open.

## Note on the transcript

Plaud labelled four speakers. Speaker 1 is Brooks Darnell, Speaker 2 is Val, Speaker 3 is Connie Burke, Speaker 4 is Nathan Carver — all confirmed by content, not by label. Two glossary fixes were applied on the way in (**JBL → JVL**, 2 occurrences).

**Possible mis-transcriptions — not in the glossary, for Val to confirm:**

- **"Lenin" (01:23), "Linen" (32:00), "Lyndon" (33:46), "Brookton" (06:33)** — all one Bank of America person who handles account coding. Plaud's own summary rendered it **Lennon**. Worth confirming the real spelling and adding a glossary rule, since this name will recur through the implementation.
- **"Notchup", "Notch of", "Nacho", "Notch", "notecard instructions" (throughout)** — all **NACHA**. Frequent enough to deserve a glossary rule once confirmed.
- **"Casper" (06:33, 12:58), "Cast Pro" (30:03), "Cash App online" (16:42), "Capstone" (18:57)** — all **CashPro**. Also a good glossary candidate.
- **"Just to add to what Dayton said" (04:47)** — Val referring to **Nathan**.
- **"a TBD plus or a CCD plus" (23:49)** — almost certainly **PPD+**, the standard consumer counterpart to CCD+.
- **"as much automation as recently possible" (02:35)** — almost certainly **reasonably**.
- **"Then it sounds like in New York, in the Bank of America's current state" (22:26)** — probably **in other words**.
- **"Could the system actually say the system advancements?" (18:39)** — garbled; meaning not recoverable from context.
- **"MSD"** is used throughout for Microsoft Dynamics / Business Central. It reads as the speakers' own shorthand rather than an error, so it was left alone.
