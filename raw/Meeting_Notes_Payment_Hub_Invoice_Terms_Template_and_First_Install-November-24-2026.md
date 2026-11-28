# Meeting Summary — RE: Payment Hub - the email that sends the invoice, and one support address for customers
**Date:** November 24, 2026, 11:16 AM Eastern
**Duration:** 25 minutes
**Attendees:** Val Levitan, Andrei Klimovich, Nathan Carver, Lev Rudky
**Raw transcript:** [[Meeting_Transcript_Payment_Hub_Invoice_Terms_Template_and_First_Install-November-24-2026]]

## Summary

**Ready to install.** Andrei said the test card activations work and nothing blocks the first installation. One thing is still being finished: the transfer from his account to Dwolla and from Dwolla to JVL. It worked last time. Email settings and layout can be done in parallel. Val: make the first installation and polish as we go.

**Invoice terms.** The invoice from JVL to a location now shows net 10 days. Val: the invoice must say payment is due upon use of service. No days at all. If JVL takes the money a few days later, that is JVL's issue, not the customer's.

**Interest.** Nathan: Business Central uses the terms field to know when to apply interest, so the internal value can differ from what the customer sees. Val, from memory: interest starts after 7 days. Nathan: BC is set to 10 now and can be changed to 7. The customer must not see "7 days". Andrei proposed to remove the terms field from this invoice type. Val agreed. Lev is not sure BC can apply interest some days after the invoice is posted. He will check.

**Bounced payment.** Lev asked what happens if the withdrawal fails. Nathan: for now the customer pays by credit card or another way with JVL. Later the system may retry.

**Invoice template.** Andrei showed yesterday's test invoice. The terms field must go. The footer must show the approved interest numbers (Andrei said 45% a year). The logo has no slogan and must have one. Nathan found the layout in BC: sales invoice report 53001, in RDLC format. BC can use RDLC or Word layouts. A new report ID can be given to COAM customers only, so machine-sale invoices do not change.

**Val's instruction on templates.** Val thinks the template is hard-coded in BC. It must come out. The template reference must live in GitHub (the knowledge base standards repo), with revisions, and a different template per product. Each PDF template needs a part number, made by the part number standard that Genadi keeps. The daily transaction invoice uses its own part number, different from hardware sales.

**Install date.** Andrei meets Felipe today. If the location is ready, they install tomorrow (November 25). If not, the next chance is Friday November 27 or, better, Monday November 30. Val: use the current template for the first location, and get it perfect on that one location.

## Decisions Made

- **Do the first installation now and polish in parallel.** (Decided by Val)
- **The location invoice says "due upon use of service". No number of days is shown to the customer.** (Decided by Val)
- **Interest starts 7 days after the invoice. This is an internal BC setting. The terms field is removed from the Payment Hub invoice.** — Val set 7 days from memory; Lev still has to confirm BC can do it. (Decided by Val)
- **The invoice template comes out of BC. Its reference lives in GitHub, with a part number per template.** (Decided by Val)
- **The first location uses the current template.** (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lev Rudky | Report what the invoice template is and whether BC can start interest some days after the invoice | Nov 24, 2026 (Val checks at 4 PM) | High | Lev asked for a couple of days; Val said today |
| 2 | Lev Rudky | Work with the BC consultant to take the template out of BC and reference it from GitHub | TBD | High | Val's instruction |
| 3 | Andrei Klimovich | Send Lev the SVG logo with the slogan; update the template: slogan under JVL, correct footnotes | TBD | High | |
| 4 | Andrei Klimovich | Give each invoice PDF template a part number by the part number standard | TBD | Normal | Val's instruction |
| 5 | Andrei Klimovich | Meet Felipe and set the installation date; tell Val | Nov 24, 2026 | High | Target Nov 25, else Nov 27 or Nov 30 |
| 6 | [Unassigned — needs clarification] | Change BC terms from 10 to 7 and make the Payment Hub report layout for COAM customers | TBD | Normal | Nathan said "we can"; he asked who updates the template and got no direct answer |

## Open Questions

- Can BC apply interest automatically 7 days after posting? (Lev to confirm)
- Annual interest rate: Andrei said 45% in this meeting. The November 20 note recorded 35% a year. Not resolved here.
- Is the template really hard-coded in BC? Val is about 90% sure. Nathan said it looks like a default layout.

## Dispatch Log

---
*Processed from Teams transcript on November 24, 2026, ~6:25 PM Eastern*
*Source meeting: RE: Payment Hub - the email that sends the invoice, and one support address for customers*
