# Meeting Summary — Bank of America CashPro: Business Central as source of truth, and a customer ACH portal
**Date:** October 13, 2026, 3:32 PM – 3:56 PM Eastern
**Duration:** ~24 minutes
**Attendees:** Val Levitan (JVL), Brooks Darnell (Bank of America, treasury), Lenin Hernandez (Bank of America, relationship manager). Nathan Carver and Inna Levitan were invited but did not join (Val: Nathan is on vacation).
**Raw transcript:** [[Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026]]
Source: Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar match:** paired with the Outlook event **"JVL SYSTEMS INC/ Treasury needs review"**, 3:30–4:00 PM Eastern, organized by Brooks A Darnell (bofa.com). Two-key rule met: time overlap, plus "Nathan" and "Lenin" (both on the invite) are spoken in the transcript.

## Summary

**Why Brooks called.** Brooks wants to finish the CashPro pricing. He repeated the order of work from Connie (the Bank of America API specialist): set up CashPro first, then the sandbox, then the API team gives the next steps. The main priority from the last meeting is still API reporting: prior-day balances and transactions. Bank of America cannot record the call; Val asked for written notes after it.

**ACH out (paying by file).** Choices: export a NACHA file from the accounting software, upload it into CashPro, and approve it there; or send files over a secure connection, which costs more. Val confirmed JVL will **start with manual NACHA file upload**. It can change later if volume grows.

**Wires.** Brooks has JVL at about 20–30 wires a month. Choices: enter wires by hand, use saved templates, or upload a CSV file. Brooks believes CSV upload is included in the base CashPro and does not need the upgraded platform; he will double-check with Connie. XML files need "CashPro Connect", which costs more. Wires can have a maker / approver split: one employee sets up the wire and a senior person approves it. Val said the platform cost matters less than the cost of Nathan's time.

**Val's rule: Business Central is the source of truth for vendor bank data.** Today, when a supplier changes bank details, staff change the template inside the bank and leave Business Central unchanged. Val does not accept this. He wants every wire to take the bank details from Business Central each time. He does not want templates to live in the Bank of America system. Manual entry for every wire is also not acceptable: "laborious and unacceptable." Brooks thinks Bank of America cannot pull the data from Business Central, but he is not sure. He will ask Connie. Val: if the base platform cannot do this, JVL will move to the more advanced system.

**ACH in (customers paying JVL).** Val wants customers to start their own ACH payments. JVL sends an agreement (for example $300 a month for 12 months). The customer signs it, logs in to a JVL payment page, and sets up a recurring payment against that agreement or invoice. Val does this today through QuickBooks and expects Bank of America to offer the same. He wants every payment option the bank has (ACH, wire, card), with the fee for each method told to the customer in advance and charged to the customer. Brooks understood this as a customer payment portal and will look for a solution.

**Auto loan (side topic, with Lenin).** Val said Inna had an approval for a $60,000 company car loan for JVL, and asked to raise it to $100,000 only if no new application is needed. Lenin: the application was taken more than a month ago and is no longer valid. After approval there are 30 days to submit for the vehicle and up to 45 days to complete. JVL must reapply, and the bank will run credit again. Val left it with Inna. Lenin will message her.

**Next step.** Brooks will meet Connie this week, then send one email with a recap, the solutions, and the pricing proposal. He hopes to send it by the end of this week. If Val agrees with the price, the setup process starts.

## Decisions Made

- **ACH payments out start with manual NACHA file upload into CashPro, with approval in CashPro.** Secure file transmission can come later if volume grows. (Val Levitan)
- **Business Central is the only source of truth for vendor bank details.** Wire data must come from Business Central every time. No templates kept in Bank of America, and no manual entry per wire. If the base CashPro cannot do this, JVL moves to the advanced platform. (Val Levitan)
- **Customers must start their own ACH payments through a portal, against a signed agreement, with recurring payments.** Offer every available payment method, with each method's fee disclosed in advance and passed to the customer. (Val Levitan)
- **The auto loan is Inna's to handle, not Val's.** (Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Brooks Darnell (BofA) | Confirm with Connie that CSV wire upload works on the base CashPro, without the upgraded platform | This week | High | Brooks: "I'll double check that" |
| 2 | Brooks Darnell (BofA) | Ask Connie if Bank of America can take wire bank details from Business Central automatically (no saved templates, no manual entry) | This week | High | Val's source-of-truth rule; decides base vs advanced platform |
| 3 | Brooks Darnell (BofA) | Find a solution for customer-initiated ACH: a portal for recurring payments against an agreement, with more payment options | This week | High | Val does this in QuickBooks today |
| 4 | Brooks Darnell (BofA) | Check the extra price for wire file transmission (CashPro Connect / XML) | This week | Normal | Only if needed |
| 5 | Brooks Darnell (BofA) | Send one email with recap, solutions and the pricing proposal | Hoped by end of week (Oct 16) | High | Val asked for something in writing |
| 6 | Lenin Hernandez (BofA) | Message Inna about reapplying for the auto loan | Open | Normal | Old application expired |
| 7 | Inna Levitan | Decide whether to reapply for the company car loan ($60,000, or $100,000) | Open | Normal | Val: "I will leave it with Ina" |

## Open Questions

- Does base CashPro really support CSV wire upload? Brooks is not fully sure.
- Can Bank of America take vendor bank details from Business Central with no person entering them? If not, what does the "advanced system" cost and include?
- Does Bank of America have a customer payment portal for recurring ACH, like QuickBooks has?
- Auto loan: Val believed the approval had no expiry date and was waiting to be drawn. Lenin says it expired. Who is right was not checked on the call.
- Val gave customer fees of "fifty dollars" per ACH and "X dollars" per wire as examples. The real fee numbers were not set.

## Notes on the transcript

Plaud speaker labels are mixed. Speaker 1 is mostly Val. Speaker 2 is Brooks Darnell (he talks about Connie and the pricing). Speaker 3 is Lenin Hernandez (the auto loan). Some lines are merged across speakers, for example at 00:00:22 and 00:19:13. No glossary fixes were needed (0 replacements).

**Possible mis-transcriptions — confirm with Val (not fixed):**
- "Mr. Bell" / "Bell" (00:00:01, 00:00:22, 00:22:52) and "Bob" / "Mr. Bob" (00:23:52) — probably **Val**.
- "Linda Fernandez" (00:00:01) — the relationship manager; probably **Lenin Hernandez**.
- "Tina is traveling… she's in Buffalo" (00:00:22) — name not clear; maybe **Inna**.
- "Ina" (00:06:31, 00:20:15, 00:22:29) — **Inna**.
- "cast pro" (00:01:01), "Cash Pro" (throughout) — **CashPro**.
- "RAPI" (00:01:01) — "our API".
- "Notch files" (00:02:00, 00:03:31) — **NACHA** files.
- "the ACA side" (00:03:31) — **ACH** side.
- "pull it from this essential" (00:13:48) — **Business Central**.
- "Per mile per second" (00:06:10) — meaning not clear.
- "sending their approval tonight" (00:07:03) — probably "send their approval".
- "Tony, once I figure out the pricing" (00:23:20) — name not clear.

## Dispatch Log

---
*Processed from Plaud recording on October 14, 2026*
*Source meeting: 10-13 Payments Architecture Decision: Enforcing Business Central as Source of Truth for ACH/Wires and Customer Portal, with CashPro Integration Options and Pricing*
