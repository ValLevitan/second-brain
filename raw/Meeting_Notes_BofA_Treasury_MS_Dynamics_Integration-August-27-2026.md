# Meeting Summary — JVL Systems / Bank of America treasury review: CashPro + Microsoft Dynamics 365 integration

**Date:** August 27, 2026, ~12:28 PM Eastern
**Duration:** approximately 85 minutes
**Attendees:** Val Levitan, Felipe Miranda Giorgi, Nathan Carver (engineer, raw "Speaker 5"); Bank of America — Brooks A. Darnell (raw "Speaker 1"), Lenin Hernandez (relationship manager). Inna invited.
**Raw transcript:** [[Meeting_Transcript_BofA_Treasury_MS_Dynamics_Integration-August-27-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "JVL SYSTEMS INC/ Treasury needs review", 12:30 PM ET (4:30 PM UTC), organiser Brooks Darnell (bofa.com), attendees Val, Inna, Nathan Carver, Lenin Hernandez. Confirmed.
**Context:** Ties to the JVL/CIBC ACH→Business Central automation thread (Nathan's API work) and the growing BofA relationship as JVL moves banking from Canada to the US.

## Summary

A needs-discovery call for expanding JVL Systems' Bank of America relationship, with a specialist deep-dive to follow. Val took a back seat and let Nathan lead the technical side. What JVL wants:

- **Incoming: reconcile ACH with Business Central.** A third-party ACH provider (the GA-COAM cash-out rail) sweeps multiple accounts, lands funds in JVL's account; JVL then wants payments to **read into the bank statement and reconcile against invoices in Microsoft Dynamics 365 Business Central** (many customers pay by ACH). JVL will build invoicing through Business Central. Current CIBC (small Chicago presence) lacks the technology capacity.
- **Outgoing (stage two): vendor payments.** Today JVL pays vendors by **manual wires, one at a time, ~20–30/month, mostly international (heavy China, some US, few Canada)** at ~$45/international wire. Val flagged this as a source of savings and wants outgoing payments run through Business Central / BofA's platform (**CashPro**).
- **The main frustration: access control.** JVL cannot set up bank-side roles/privileges ("a company within the company"), so **one senior person has to handle all wire setup and money movement**. Fixing multi-user approvals/privileges is the biggest pain point.

**Scale / context Val gave:** JVL is **moving banking from Canada to the US** (winding down Royal Bank of Canada, growing BofA); projecting roughly **$10M/yr revenue, ~$6–7M/yr payments (~$600–700K/month), ~$750K receivables, ~$250K cash**, ~20 transactions. JVL sends only ~20 invoices/month, below BofA's ~200/month AP-automation minimum — but Brooks said they can still help and that wires would be more efficient on CashPro. JVL still uses checks (not cash), largely because of the access-control limitation.

**Next step:** BofA will bring in a **CashPro / integration specialist** and schedule a technical session to scope the Microsoft Dynamics 365 integration and pricing.

## Decisions / Outcomes
- Proceed toward a **BofA CashPro + Microsoft Dynamics 365 Business Central** integration; schedule a specialist technical deep-dive. (mutual)
- **Stage 1** = incoming ACH ↔ BC invoice reconciliation; **stage 2** = outgoing vendor payments through BC. (Val/Nathan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | BofA (Brooks) | Bring in a CashPro/integration specialist; schedule the technical session; explain pricing | Days | High | Scope the BC integration |
| 2 | Nathan Carver | Lead the technical scoping of the ACH↔BC (and later vendor-payment) integration | With BofA | High | Same API work as CIBC ZBA thread |
| 3 | JVL | Consolidate wire activity onto CashPro (savings vs $45/intl wire) and fix multi-user access control | Ongoing | Normal | Main pain point |

## Possible mis-transcriptions
- "CastPro / CapPro / CashPro" — **CashPro** (BofA's treasury platform); "Mr. Bob / Mr. Vladimir" — likely Lenin Hernandez or Brooks, mislabelled; "Darryl / Darnell / Brooks" — the rep is **Brooks A. Darnell** (first name Brooks, surname Darnell).

## Dispatch Log

---
*Processed from Plaud recording on September 25, 2026 (backlog batch 8). Source: 08-27 Strategic Banking Integration Plan for BofA, Microsoft Dynamics 365 (Plaud).*
