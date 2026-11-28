# Meeting Summary — Genadi: Flex-Port Suppliers and Costs
**Date:** November 27, 2026, 12:03 PM Eastern (about 1 hour 30 minutes)
**Attendees:** Val Levitan, Genadi Peari
**Platform:** Google Meet, recorded by Claude Meetings
**Raw transcript:** [[Meeting_Transcript_Genadi_FlexPort_GitHub_MSBC_Link_and_Vendor_Quote_Rule-November-27-2026]]
Source: Claude Meetings (project 01a21de8-4aba-728a-9967-5ae84145a1ef)

Held mostly in Russian, some English. Summary in English. Many lines are labelled "Room" (speaker not identified), so who said what is taken from context. Follow-up to [[Meeting_Notes_Genadi_FlexPort_BOM_Revision_2_and_Vendor_Data-November-26-2026]].

## Summary

**Assembly vs parts.** Val started from the Flex-Port part number PT1-M05-B10-12-01 ("PT1"). Genadi: the PO is not placed for the assembly; it is placed for all the parts under it. Today the BOM of this assembly has no link to GitHub; only the flat list of parts is linked.

**Keep the GitHub–MSBC link.** Val said the link between GitHub and MSBC must not be cut. Building an assembly from the flat list, freezing it and saving a copy in MSBC is "the wrong step"; it should be linked, not copy-pasted. If the link is cut, MSBC never learns about a new revision or a new supplier. One way: a check (for example when a PO is made) where Claude confirms the part numbers in the MSBC assembly match GitHub. GitHub is the base. Genadi had proposed a lock: unlock only with a reason (an ECN), change, lock again. Val did not yet know what "lock" would mean. Val noted that yesterday they had thought the link could be cut.

**What comes from where.** Val's split: from GitHub come the part number and the vendor name; from procurement@jvl.ca correspondence come contact details and pricing; from SharePoint come the bank details (by Val's existing standard). Mery chases anything missing through procurement@. MSBC is the executor, GitHub the lawmaker.

**Vendor in the data contract — not settled.** Genadi does not think GitHub should say where to buy. A JVL-designed part (for example a bent metal bracket from Hongzhou / Jintao) can be bought from ten vendors; lead time and price per vendor live in MSBC. He splits parts into two groups: designed by JVL, and standard off-the-shelf parts (screws). A standard part will never have a vendor in its data contract. Val: a standard part still needs a reliable data contract, to catch small differences; example: a screw that was almost the same but pierced the panel. Genadi said this has happened. Val: a different supplier means a different data sheet (for example the same panel with another mounting frame). They agreed the output must be a reliable data contract, but not who/where the vendor is recorded.

**Price breaks.** Genadi: vendors quote different prices for different quantities (for example a box of 7 monitors is the minimum). Val did not see how this applies today; JVL negotiates once and gets an MOQ. Left aside.

**What Claude found vs what MSBC shows.** Claude's table said 0 of 14 Flex-Port parts are ready, and no item card names a vendor. Genadi showed MSBC himself:
- SCN-BQCODE-01 scanner engine: item card unit cost 16.50, last direct cost 3.40. The Purchase Prices page has YIMATONG1 lines: min 10 at 17.00 and min 100 at 16.50, from 6/1/2026.
- MON-480X854-5I-TS-1 5" LCD: item card unit cost 4.34 (Genadi called it "garbage"). The Purchase Prices page has STARTEK1 lines for min 20, 30 and 100 at 22.18 and 24.30.
Genadi: the vendors exist in MSBC; the data is entered in the wrong place, or Claude reads the wrong tab. Val: Misha types these by hand, copy-paste from Excel. Genadi: there must be a clear rule for which tabs to write to, so everyone reads the same tabs.

**Where the $4.34 comes from.** Claude traced it to two receipts from JVLCAN01 (JVL Labs), an internal transfer cost, not a Startek price. The $24.30 is on PO P_ORD000000502, with no Startek quotation or invoice in procurement@. Val: the parts were sent with a fake price.

**Price rule (Val dictated it to Claude).** See Decisions. Claude rebuilt the dashboard on this rule: 0 of 14 parts have a vendor quotation in procurement@; 11 MSBC costs have none behind them. Val: maybe the emails just need to be pulled in.

**Dashboard and access.** Val shared the "Flex-Port Vendor Readiness" dashboard with Genadi with edit rights. Genadi could not open it at first; he had hit his Claude usage limit. Val told him to ask IT to raise it.

**GitHub work today.** Genadi added the scanners, monitors and boards to the data contracts this morning (PR 58 was about an hour before).

**Genadi's picture of the end state.** Tell the agent "50 sets of this"; it lists the parts with stock and on-order quantities, puts every part over about $15 apart so a person decides how many to order (order 100 now, more next week, by air), and can then print or bulk-issue the POs. Anyone without an engineering background could do it if the data is clean. Val agreed this is what it should be.

## Decisions Made

- **Price source of truth.** The only source of truth for a price is a direct vendor quote in the procurement@jvl.ca mailbox. A casual vendor email is an indicative price only, not final. A final price may enter MSBC only when backed by the vendor's quotation on their letterhead, emailed to procurement@jvl.ca. MSBC item costs, our own PO prices and receipts are never a source. If no quotation exists, there is no price in MSBC, and the gap is reported to Val. (Decided by Val)
- **The GitHub–MSBC link stays.** An assembly is not copied frozen into MSBC; it stays linked to GitHub, with GitHub as the base. (Val's position; how to build the link is open.)
- **Next step is merging supplier email.** Genadi's and Misha's supplier emails go into procurement@jvl.ca before anything else; Val reruns the table after. (Decided by Val; "Понятно. Будет." follows, speaker not identified)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Talk to Misha so he prepares his supplier emails for the merge | Nov 30, 2026 | High | Genadi said he had not done the email export yet |
| 2 | Genadi Peari | Call Dmitri Kovalchuk Monday morning to merge Genadi's and Misha's supplier emails into procurement@jvl.ca | Nov 30, 2026 | High | "The most important next step" |
| 3 | Val Levitan | Rerun the Flex-Port vendor table after the merge | Nov 30, 2026 | Normal | Monday morning |
| 4 | Val Levitan | Pull the vendor prices from email, have them confirmed, and enter them in the item card ("one to two days of work") | TBD | Normal | Owner confirmed by Val on Nov 27 after the meeting |

## Open Questions

- Does a data contract name the vendor (where we buy), or only the manufacturer? Genadi says no vendor in GitHub; Val's split has the vendor name coming from GitHub. (Genadi, Val)
- Which MSBC pages (item card, Purchase Prices, vendor catalog) hold vendor and price, so everyone and Claude read the same place? (Genadi)
- How is the GitHub–MSBC link built: a standing check, a lock/unlock with ECN, or something else? (Val, Genadi)
- How are quantity price breaks recorded? (Genadi)
- Do the MSBC Purchase Prices lines (Yimatong, Startek) have letterhead quotations behind them in procurement@? Not yet checked.

## Dispatch Log

- 2026-11-27 1:42 PM ET — Email draft created for: Genadi (items 1, 2), in Val's Outlook Drafts, not sent. Calendar reminders: 3 (items 1, 2, 3), Mon Nov 30 9:00 AM ET. Item 4 excluded (needs Val's confirmation).
- 2026-11-27 1:45 PM ET — Val approved; email to Genadi sent, confirmed in Sent Items.

---
*Processed from Claude Meetings transcript on November 27, 2026, 2:00 PM Eastern*
*Source meeting: Flex-Port Suppliers and Costs*
