# Meeting Summary — GitHub-MSBC integration and supplier migration – Val, Genadi, Nathan

**Date:** October 19, 2026, 5:36 PM – 5:50 PM Eastern
**Duration:** ~14 minutes
**Segment:** Segment 2 of 2
**Attendees:** Val Levitan, Genadi Peari, Nathan Carver
**Raw transcript:** [[Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026]]
**Previous segment:** [[Meeting_Notes_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026]]

## Summary

**Goal.** Mery is not an engineer, unlike Michael. She needs an easy administration environment inside Business Central. Val: stop building special reports. Mery should ask questions through MCP, in Spanish or English, and get answers.

**What is needed in MSBC.** Nathan must add more MSBC endpoints so inventory control is covered end to end. Nathan agreed the current set is limited.

**Data and process gaps.** Genadi said the material requirements data is mostly there and only the counts are not exact. Val disagreed: the count is now more or less fine; the real problem is that purchase invoices are not handled correctly. Examples:
- A vendor asks for a prepayment on a purchase order. Today the prepayment does not register against the invoices.
- The vendor's "ready" and "shipping" notices are only emails between Michael and the vendor. The system must know when a vendor has shipped, so lead time (for example 25 days by boat plus 15 by truck, about 40 days) can be tracked.
- Genadi listed the steps that all need confirming: PO approval, PO deposit, invoicing, payment, shipping, lead time.
- Val needs to meet Lev to learn the payment flow and how purchase invoices are administered.

**AI COO.** Val wants an AI Chief Operating Officer agent that scans Business Central (the source of truth) and emails, and flags misses such as "we did not make a payment" or "the supplier should have sent a shipping notice". Genadi added that it should pull vendor replies from emails into the matching line, as Michael wanted for his notes.

**Flow.** Val writes use cases, use cases become capabilities, capabilities go to Nathan, and Nathan adds the endpoints. Nathan agreed.

**Genadi's part.** Once the repositories exist, Genadi loads clean engineering data (drawings, data sheets, monitor connectors, agreed resolutions). If the data is buried in his emails, an agent can be set up to pull it out.

**Next steps.** Val asked for results by Wednesday and a follow-up call Wednesday at about 4–5 PM; Nathan is available. Genadi asked Nathan for 15 minutes tomorrow to walk through one repository. Val suggested a morning meeting with Andrei included (in Minsk; he writes GitHub Actions and can configure it).

## Decisions Made

- **Mery gets answers from Business Central through MCP queries, not special reports.** (Val)
- **Nathan adds MSBC endpoints driven by AI COO use cases** (use cases → capabilities → endpoints). (Val; Nathan agreed)
- **Follow-up call Wednesday, October 21, about 4–5 PM.** (Val; Nathan available)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Write a first set of AI COO use cases (up to about 10) for tracking material management, and send them to Nathan and Genadi | Oct 19 | High | Val: "I will get on it today" |
| 2 | Nathan Carver, Genadi Peari | Review Val's use cases | On receipt | Normal | |
| 3 | Nathan Carver | Add more MSBC endpoints for end-to-end inventory control, from the use cases | TBD | High | Current endpoints are limited |
| 4 | Val | Meet Lev to learn the payment and purchase invoice flow | TBD | Normal | Needed to fix prepayment and invoice handling |
| 5 | Genadi Peari | After the repositories exist, load clean drawings and data sheets | After repos exist | High | |
| 6 | Genadi Peari, Nathan Carver | Walk through one repository together (about 15 minutes), with Andrei if possible | Oct 20 morning | Normal | Andrei is in Minsk |
| 7 | Val | Send the invitation for the Wednesday follow-up call | Oct 19 | Normal | Wed Oct 21, about 4–5 PM |
| 8 | Val, Genadi Peari, Nathan Carver | Have something achieved by Wednesday | Oct 21 | High | |

## Open Questions

- Exact time of Wednesday's call (4 or 5 PM). (Val)
- Whether Genadi's useful data sits in his emails and needs an agent to extract it. (Val)

## Dispatch Log

---
*Processed from Teams transcript on October 19, 2026*
*Source meeting: GitHub-MSBC integration and supplier migration – Val, Genadi, Nathan*
