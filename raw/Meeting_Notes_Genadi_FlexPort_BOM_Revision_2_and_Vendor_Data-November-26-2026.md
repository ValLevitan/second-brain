# Meeting Summary — Genadi: FlexPort BOM Revision 2 and Vendor Data
**Date:** November 26, 2026, 3:30 PM Eastern (about 35 minutes)
**Attendees:** Val Levitan, Genadi Peari
**Platform:** Google Meet, recorded by Claude Meetings
**Raw transcript:** [[Meeting_Transcript_Genadi_FlexPort_BOM_Revision_2_and_Vendor_Data-November-26-2026]]
Source: Claude Meetings (project 01a21989-e921-713a-8908-d6e15e162bbc)

Held mostly in Russian, some English. Summary in English. Many lines are labelled "Room" (speaker not identified), so who said what is taken from context. Follow-up to the 2:31 PM call: [[Meeting_Notes_Genadi_Components_Repo_Structure_and_Monitor_Sourcing_Savings-November-26-2026]].

## Summary

**Val's experiment.** Val told Claude there are only two sources of truth for FlexPort: (1) a general, non-engineering description of the product, which Claude wrote from Confluence and Jira; (2) the data contracts under `components` in GitHub. "Nothing else. Ignore everything else." From these Claude built a bill of materials and listed what is missing.

**Gaps Claude found.** Main board, touch screen and scanner board: document filed but no data contract. Main board: "review which revision is released" — Genadi said the new Wi-Fi revision must still be entered with an updated contract, and the main board comes first. Scanner engine: no part number. Network link to Flex IQ: flagged. Genadi admitted he had not yet gone through FlexPort.

**What is not in the BOM.** Val told Claude that brackets and external harnesses to peripheral devices are not part of the BOM. They are stocked in quantity, each under its own part number, as single inventory items. Genadi agreed.

**Site differences.** Genadi warned that FlexPort installations differ by location and cabinet, with many nodes; Andrey tracks them in a large Excel file, plus verbal knowledge. Val: these will be human, business-level nuances that he and Genadi resolve; no custom software from Nathan is needed. Genadi writes all data contracts himself.

**Locking a BOM.** Genadi wants a generated BOM locked after human review, so nobody (not even Claude) changes it. A variant (same machine, "other buttons" for a customer) becomes a second saved BOM that the person ordering picks from, without regenerating. Val agreed but said he is optimistic better options exist. One option: after review, give the BOM a dated revision number and send it to Business Central (MSBC) through MCP — that part needs Nathan.

**Vendor data.** Engineering sends part and vendor name to MSBC. The vendor card (bank details, terms, address, contacts) is filled by finance and procurement, separately. The two must merge in MSBC — to be discussed with Nathan, less with Lev. Val: Lev is careful and wants manual entry; "by hand we will do something only in three years. I would rather allow mistakes."

**Vendor history from email.** First quotes and correspondence sit in Genadi's mailbox. Val's plan: Genadi uses a Claude prompt to find the vendor emails for parts in GitHub `components` and move them to a separate "procurement export" folder. That folder then goes into the procurement mailbox, gets groomed, and Claude extracts vendor attributes and a negotiation history per vendor. Genadi wants full line-by-line quotation history to spot price jumps ("everyone loses this"). New parts always go through procurement today; existing GitHub parts are already being bought. BC data is "a big mess" and needs grooming.

**Vendor attributes.** Genadi wants the attribute list agreed first, after Lev finishes his current work. Val will have Claude list the vendor-profile fields MSBC already offers so the team can mark what is needed. Genadi has tested MSBC item attributes (a "revision" attribute works). Val: part attributes are badly needed too.

**Ordering now.** Stock of Flex IQ and FlexPort is zero. Val: order 50 IQ and 300 Ports. Genadi: the existing BOM in MSBC already has quantities, Mery only needs to place orders — no data contracts needed. Agreed as two parallel jobs: Mery orders from the current BOM (treated as revision 1); Genadi completes data contracts so revision 2 can be loaded into MSBC and used from then on. Genadi said revision 1 is fully up to date; Val wants to run the loop once and see what changes. Misha will show Mery how to order; Genadi should focus on data contracts.

## Decisions Made

- **Only two sources of truth for a product BOM:** the general product description, and the data contracts under GitHub `components`. (Val)
- **Brackets and external peripheral harnesses are not in the BOM;** stocked as single items under their own part numbers. (Val; Genadi agreed)
- **Genadi writes the data contracts; no custom solution from Nathan for them.** (Val; Genadi agreed)
- **The current MSBC BOM is revision 1; the full loop produces revision 2,** which is loaded into MSBC and used from then on. (Val)
- **Order 50 Flex IQ and 300 FlexPort now from revision 1,** in parallel with the revision 2 work. (Val; Genadi agreed)
- **Locked, dated BOM revisions sent to MSBC via MCP — tentative.** Val is open to better options. (Val, Genadi)
- **If MSBC lacks suitable vendor attributes, adapt to how MSBC handles vendor details.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Enter the new Wi-Fi main board revision with an updated data contract (main board first) | TBD | High | Claude flagged "which revision is released" |
| 2 | Genadi Peari | Review all data contracts under components, find the missing ones for FlexPort and Flex IQ, complete BOM revision 2 in GitHub | Started Nov 26 | High | Genadi: "two or three days" to get Ports and Flex ready for MSBC |
| 3 | Genadi Peari | Use a Claude prompt to find vendor emails for GitHub component parts and move them to a "procurement export" folder | TBD | Normal | Then moved into procurement mailbox |
| 4 | Nathan Carver | Build the MCP loading of locked BOMs into MSBC with vendor data | TBD | Normal | Val: "there we need Nathan" — not yet told to Nathan in this call |
| 5 | Mery | Order 50 Flex IQ and 300 FlexPort from BOM revision 1 in MSBC | TBD | High | Stock is zero |
| 6 | Val Levitan | Ask Misha to show Mery how to order parts for FlexPort and Flex IQ | TBD | High | Genadi to focus on data contracts instead |
| 7 | Val Levitan | Have Claude list the vendor-profile fields MSBC already offers | TBD | Normal | So the team marks which are needed |
| 8 | Val Levitan | Revisit part numbering (Claude now assigns part numbers itself) | Later | Low | Val: "I will come back to part numbers" |
| 9 | Val, Genadi, Nathan (and Lev) | Agree the vendor attribute list and how vendor admin data and engineering data merge in MSBC | After Lev's current work | Normal | Before the email folder work |

## Open Questions

- Which main board revision is released?
- How does site-specific installation knowledge (Andrey's Excel, verbal) get into the source of truth?
- Manual entry into MSBC (Lev's preference) or automated loading (Val's preference, accepting some errors)?

## Related

- [[GitHub_to_MSBC_BOM_Hub]]
- [[Meeting_Notes_MSBC_Item_Attributes_vs_Description_and_Part_Revisions-November-25-2026]]
- Earlier call the same day: [[Meeting_Notes_Genadi_Components_Repo_Structure_and_Monitor_Sourcing_Savings-November-26-2026]]
