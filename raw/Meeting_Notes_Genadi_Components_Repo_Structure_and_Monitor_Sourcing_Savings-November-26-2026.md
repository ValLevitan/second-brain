# Meeting Summary — Genadi: Components Repository and Monitor Sourcing
**Date:** November 26, 2026, 2:31 PM Eastern (about 21 minutes)
**Attendees:** Val Levitan, Genadi Peari
**Platform:** Google Meet, recorded by Claude Meetings
**Raw transcript:** [[Meeting_Transcript_Genadi_Components_Repo_Structure_and_Monitor_Sourcing_Savings-November-26-2026]]
Source: Claude Meetings (project 01a21955-8d82-70fb-862b-45a15d85c459)

Held mostly in Russian, some English. Summary in English. Many lines are labelled "Room" (speaker not identified), so who said what is taken from context.

## Summary

**Purpose.** Val said the call was for his own understanding, "I'm asking for help, it's not a direction." He needed a sounding board.

**Manuals are not the flat view.** Val first opened the CM08 Flex Manual in GitHub. Genadi explained that manuals are daily production documents (kept in doc and PDF), not part of the flat view. Val leans toward PDF only but left it open.

**Components structure.** The flat view is the `components` folder, split into category folders. Inside a category: manufacturer, then contracts, then part numbers, so a second supplier can sit next to the first. Plastics are split per product (they do not overlap). Metal has folders for Flex Pay, Slim and Port. Electronics are under PCBA (FlexPort is FP01). Val: "this is much better, day and night."

**Data contracts.** Each part has a contract YAML file with mountings, holes and dimensions, built by Claude from the drawings or datasheet. Bought parts (for example the BOE monitor) carry the vendor datasheet, not a drawing; mounting dimensions are on the last pages (pages 28–29). The check already works: Genadi said Claude caught a real fit error three times that day when he entered new parts. Val: "what we are doing here has never been done."

**Monitor sourcing.** The Korean supplier raised prices sharply on monitor driver controllers. Genadi found alternative makers; on paper the saving is about $95 per machine, and these makers have long supply (less risk of obsolete parts). A 22" sample was sent free; two 43" samples (about $25 each) are on the way. Genadi is checking brackets and wiring for the change, and needs a few days for the transition plan and production instructions.

**Status.** The component list for current products is done; datasheets mostly done; some approved-vendor data is missing. Genadi still has to add the items Val sent the day before.

**Parts for production.** Genadi raised the production need (50 IQ and 300 Ports) and said the part list should be simple to derive from three product numbers and inventory. Val stopped the side discussion about Mery and Misha: he has his own plan. Val then had an idea to test and ended the call to experiment, saying he would call Genadi back.

## Decisions Made

- None formally made. Val accepted the components structure as is ("much better").

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Monitor transition: check brackets and wiring for the new suppliers, transition plan, production instructions | A few days | High | Saving about $95 per machine on paper |
| 2 | Genadi Peari | Check alternative monitor makers' datasheets against the data contract | Later stage | Normal | Already started |
| 3 | Genadi Peari | Add the items Val sent on Nov 25 to the components structure | TBD | Normal | Genadi: "not added yet" |
| 4 | Genadi Peari, Andrey | Compile the list of parts needed for the current production need | TBD | Normal | Genadi said they are doing it now |
| 5 | Val Levitan | Experiment with the BOM / ordering idea, then call Genadi back | Nov 26, 2026 | High | Done — follow-up call at 3:30 PM: [[Meeting_Notes_Genadi_FlexPort_BOM_Revision_2_and_Vendor_Data-November-26-2026]] |

## Open Questions

- Does production need manuals in both doc and PDF? Val leans to PDF only.
- Can the repository send documents to production and vendors automatically? (Genadi's suggestion)
- Can parts needed vs. inventory be worked out automatically from a few product numbers and quantities?

## Related

- [[GitHub_to_MSBC_BOM_Hub]]
- Follow-up call the same day: [[Meeting_Notes_Genadi_FlexPort_BOM_Revision_2_and_Vendor_Data-November-26-2026]]
