# Meeting Summary — MSBC - Description and Attributes
**Date:** November 25, 2026, 12:31 PM Eastern
**Duration:** about 1h 14m of speech (recording 1h 32m)
**Attendees:** Val Levitan, Lev Rudky, Genadi Peari
**Raw transcript:** [[Meeting_Transcript_MSBC_Item_Attributes_vs_Description_and_Part_Revisions-November-25-2026]]

Held in Russian (a few lines in English). Summary in English.

## Summary

**Description vs attributes.** Val wants to stop packing configuration details into the item description in Microsoft Business Central (MSBC). It is hard to explain on invoices and hurts sales. His example: the IQ1 description today lists screen size, colour, scanner, no card reader. Val wants the description to say only the product (for example "Flex IQ Share Terminal"). Everything else (one or two screens, scanner, card reader, modem) goes into MSBC item attributes. Val read that MSBC supports many attributes per item (text, number, date and so on). It fits JVL's flat list of items in GitHub: each item has a data sheet, and an agent can pull attributes from the data sheets and data contracts into MSBC.

**Is it enabled?** Lev said attributes are probably usable, but he cannot confirm in two minutes. He wants to test first on a simple assembly in a test company. He wants to check that attributes cause no problems in purchase orders, invoices and other documents. Genadi can already see attribute fields in MSBC. The default attributes (material, model, colour) are not enough. JVL will need its own (bill validator, printer, extra devices).

**Part revision.** Genadi asked to add part revision as an attribute or a field. MSBC has no revision today. He types the revision into the description by hand, which is what Val wants to avoid. A revision is used when a part changes but stays backward compatible (for example a monitor bracket with extra holes for a new controller board). Not backward compatible means a new part number. Val will think about it.

**No configuration table.** Genadi keeps a GitHub table of final Flex product numbers and their differences (for example the South Dakota cable for the Light & Wonder controller). He asked how sales (Felipe) and Elizabeth (production orders) will pick the right product number without it. Val's answer: they ask Claude, which matches the configuration they need to a part number by its attributes. Val is against tables. A table must be kept up to date by hand and lives in one person's memory. The only source of truth is the requirements: legislative, non-functional and functional. They are already in GitHub for South Dakota, Nebraska, Georgia and Texas. If a requirement is missing, it cannot be tested or ordered. Genadi was not convinced. He worries about human error, such as a configuration that does not exist or the wrong bill validator.

**Sub-assemblies without a manufacturing module.** Val said JVL does not need the MSBC manufacturing module. With Genadi and Nathan, it was tested that a sub-assembly (the power supply) can be built from data sheets and kept as its own part number with its own assembly. Lev's Claude can read MSBC data but has limited write access. Val explained that missing functions get added to Nathan's MCP. You ask Claude to write a use case and send it to Nathan (or Dima Kovalchuk) through GitHub and Jira.

**Lev on assembly shortages.** Assemblies hit about 40 shortages, mostly small items (tape, labels, packaging). Lev ignores small ones and re-posts. He suggested Nathan load the components into the assembly order and check the drawings first. Then Elizabeth could post assemblies herself.

**Missing AC warning label.** Genadi said a cheap high-voltage warning label must go on every AC power supply plate. He said procurement does not buy it, it is not applied in assembly, and small items get dropped. He warned that this is a legal risk. His only control is the BOM.

**Other process topics (Lev).** Outside labour (for example coating), when the result does not come back to stock, should be set up as a resource, not an item. A purchase order for a resource does not touch inventory. Lev will document this. He also needs a cut-over process for BOM revision changes (for example 7 old boards and 13 new ones in a 20-machine build). Genadi has no instructions for this today.

## Decisions Made

- **Item description holds only the short product name; configuration details move to MSBC item attributes.** Genadi agreed attributes are needed for all part numbers. (Decided by Val; Genadi agreed)
- **Test attributes first in a test company on the power-supply assembly, made three levels deep, before using them in the live company.** (Decided by Lev, agreed by Val and Genadi)
- **No configuration lookup table; product configurations come from requirements and data contracts.** Val's position. Genadi was not convinced (see Open Questions). (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lev Rudky | Test MSBC item attributes in a test company on the power-supply assembly and check purchase orders, invoices and other documents | Nov 27, 2026 | High | Val: "in a day or two we will know about attributes" |
| 2 | Genadi Peari | Make the power-supply assembly three levels deep in the test company and send Lev the relevant attributes | TBD | Normal | Genadi put the number in the chat during the call |
| 3 | Val Levitan | Decide how to handle part revision (attribute or separate field) | TBD | Normal | Genadi needs it; today typed into description by hand |
| 4 | Lev Rudky | Write instructions for the BOM revision cut-over (old and new boards in one build) | TBD | Normal | Genadi asked for instructions |
| 5 | Lev Rudky | Document outside labour (for example coating) as a resource, not an item, including the coating round trip | TBD | Low | Lev has no answer yet for the round-trip case |

## Open Questions

- How will sales and production pick the exact final product number without Genadi's table, and how is human error prevented? Raised by Genadi. Val's answer: Claude, from attributes. Genadi still unsure.
- Can custom attributes be added, and can revision be one of them? Raised by Genadi. Waits for Lev's test.
- The AC power supply warning label is reportedly not bought or applied. Raised by Genadi. No owner was set.

## Dispatch Log

---
*Processed from Teams transcript on November 25, 2026, 4:10 PM Eastern*
*Source meeting: MSBC - Description and Attributes*
