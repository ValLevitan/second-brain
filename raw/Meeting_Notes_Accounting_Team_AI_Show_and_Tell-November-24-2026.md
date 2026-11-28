# Meeting Summary — Claude demos by the accounting team
**Date:** November 24, 2026, 1:05 PM Eastern
**Duration:** ~58 minutes (57m 36s)
**Attendees:** Val Levitan, Mery Villavicencio, Laura Escorcia, Igor Donis, Cris Nacarino, Erika Gonzalez
**Language:** Mostly Spanish; Val in English (live translation)
**Raw transcript:** [[Meeting_Transcript_Accounting_Team_AI_Show_and_Tell-November-24-2026]]

## Summary

**Format set by Val.** This is a regular "show and tell" on AI only. Each person gets about 12–15 minutes to show how they use AI, with no interruptions. Val wants honesty: "I don't use AI" is fine today, but if someone still says that two weeks from now, they are probably not for JVL. Val will feed the transcript to his Claude to make a short "next level" lesson for the team each week.

**Before Val joined (team talk).** Mery asked if the vendor bank details standard says she must enter bank details on the vendor card in Business Central. Cris read her an older text (probably the email): Mery receives the data, confirms by phone, saves it in SharePoint, and enters it in Business Central. Mery thinks purchasing should not fill the vendor card, because one wrong entry is costly. *Checked after the meeting:* the standard in GitHub (version 1.4, Nov 24; the change was made in 1.2, Nov 20) already agrees with Mery. Lev Rudky (MIS Manager) enters and approves the bank details. Mery only saves the vendor's documents in SharePoint and never enters, approves or pays. The team was reading an outdated version. Laura and Igor said a second person checks the work (double control). Laura and Mery also said the standards miss real cases and the people who use them should give input.

**Demos:**

- **Mery (procurement, payroll):**
  - Hong Jin shipment: gave Claude the supplier invoice and HS codes. Claude built an Excel table with duty and tax rates and FedEx air freight. DDP by Hong Jin = 1,790 USD; doing it ourselves ≈ 1,800 USD; she said the difference is 66.56 in Hong Jin's favour. Her answer: use DDP with Hong Jin. *Superseded the same day:* in the 3:57 PM meeting Val showed that the vendor's tariff code (steel articles, about 80%) was wrong; JVL imports these parts under HTS 9504.30.00.60, about 20% all-in. See [[Meeting_Notes_Mery_Hongjin_DDP_Costs_and_Slot_Parts_Tariff_Code-November-24-2026]].
  - Gave Claude the GitHub standards and asked if they cover a PO created with the wrong G/L account (Anton's PC, bought by Mikhail on a credit card, booked to materials instead of an expense account). The standards do not cover it. Igor gave the right account and it was fixed at the accounting level.
  - Claude drafted the letter that asks each vendor for full bank details.
  - Used Claude to learn WSIB (transcript says "West AI B") — rates, duties, filing dates.
- **Erika (collections, 6-month role):**
  - Downloads Bancolombia daily movements by hand (Claude has no bank access), and Claude formats them to Val's standard and checks for errors; she uploads to the SharePoint folder Val gave her.
  - Also uses Claude for: task priorities, collection letter templates, a customer payment calendar, sorting email into folders by customer, the ACH format, a morning brief linked to her email, and a job search for after her contract. She never lets Claude send or apply without her review.
- **Igor (financial controller):**
  - Projects: Systems tax return analysis, vendor credit applications, consolidated cash forecast, state sales tax filings.
  - Sales tax: compares Avalara reports (Cris holds the login) with Business Central, then Claude simulates the return per state rules. His last Georgia return matched the DOR portal. States: Georgia, Nebraska, South Dakota, Texas (Texas still under review); the live status report also listed Florida.
  - Live demo of a bank reconciliation: RBC CAD and USD, October, statements vs Navision (JVL Labs), done per the standard. Claude matched items and listed open items. Igor picked this month on purpose because some bank items are not yet booked.
- **Cris:**
  - Works in single sessions, not projects.
  - Exported POs from Business Central; Claude split them into Excel tabs: received, partly received, not received. Many POs are still open in BC; she will use this to close them.
  - Had Claude translate and explain the vendor bank details standard and make a one-page PDF.
  - Main daily use: translating and writing English emails.
- **Laura (AR):**
  - Business Central AR reports are hard for customers to read, so she uses a Claude project ("ARC") to build simple AR reports, customer statements and collection letters, with Erika and Felipe, for about 2–3 months.
  - Once or twice a week she exports from BC, adds manual columns, and checks sales from the last 2–3 days against customer credit limits; she raises problems with Felipe.
  - Also asks Claude which G/L account to use, based on the chart of accounts, and to explain and answer English emails.

**Val's closing teaching:**
- Two tricks: ask for the summary "in ESL English" (shorter sentences, simpler words), and say "chew it up for me" (break it down).
- The team uses Claude as an "instruction processor." Next step: use MCPs (for example the Business Central MCP — talk to BC in plain language). If the MCP lacks something, write a use case and a developer adds it. Later: build agents.
- Igor asked if an artifact is the same as an agent. Val: an artifact is the final output; an agent is like a server you give a mission to, and it needs skills and guardrails.
- He does not expect them to know these terms next week. They can learn from Spanish YouTube videos.

## Decisions Made

- **Weekly AI show-and-tell for the accounting team** — each person shows how they use AI, about 12–15 minutes each; Val's Claude makes a "next level" lesson from each transcript. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Post this meeting transcript in the team chat | Nov 24, 2026 | Normal | Team can summarize it in their own Claude |
| 2 | Val Levitan | Have Claude make a "next level" lesson from this transcript and send it to the team | Before next meeting (~Dec 1, 2026) | Normal | Test whether Claude can pace the team's learning |
| 3 | Accounting team (Mery, Laura, Igor, Cris, Erika) | Start learning MCP, use cases and agents (e.g. Spanish YouTube); try the Business Central MCP | TBD | Normal | Val will keep repeating the terms |
| 4 | Accounting team | Try new tricks this week and share results next week (ESL summary, "chew it up") | Next meeting | Low | |
| 5 | Igor Donis | Learn how to use artifacts | TBD | Low | Igor said he does not know them yet |

## Open Questions

- The standards do not say what to do when an approved or received PO has the wrong G/L account: cancel and reissue the PO, or fix it only in accounting? (Mery, Laura). Val asked Lev to write a standard (see Dispatch Log).
- *Closed:* who enters vendor bank details. The standard (1.4) says Lev, not Mery.
- *Closed:* Mery's DDP numbers. Replaced by the 3:57 PM meeting the same day (tariff code 9504.30.00.60).

## Dispatch Log

- 2026-11-24 5:04 PM ET — Email draft (not sent) to Lev Rudky, Cc Vaselisa: please write a standard on fixing a purchase order approved with the wrong account and file it in GitHub; Vaselisa to follow up.
- 2026-11-24 5:24 PM ET — Same draft rewritten after Val's rulings in chat (still not sent): (1) add to the purchase order standard: nobody changes a purchase order after Val approves it; only the person who issued it may cancel it; the CFO and COO are told of every cancelled purchase order; the controller decides the right account and the AI CFO verifies it; no Business Central click steps in the standard. (2) New short standard: standards do not duplicate application user manuals; for "how do I" questions, people point their own AI at the application's online user manual first, then ask MIS or IT.
- 2026-11-25 3:16 PM ET — Val sent the email to Lev (Cc Vaselisa).
- 2026-11-25 4:46 PM ET — Undertaking #1 done: transcript (.docx) posted in the meeting's Teams chat at Val's request. File in Val's OneDrive "Microsoft Teams Chat Files", view-only link for the five attendees.

---
*Processed from Teams transcript (.docx export) on November 24, 2026*
*Source meeting: Claude demos by the accounting team*
