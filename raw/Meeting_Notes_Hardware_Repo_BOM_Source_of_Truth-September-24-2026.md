# Meeting Summary — Alignment on mechanical drawings repo and street machines design - September-24-2026
**Date:** September 24, 2026, 4:38 PM – 5:20 PM Eastern
**Duration:** About 42 minutes
**Segment:** Segment 1 of 2
**Attendees:** Val Levitan, Genadi Peari
**Raw transcript:** [[Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026]]

## Summary

Started in English, then moved to Russian. The transcription is poor in places (about 10:00–13:30 is mostly unreadable), so some points below are marked as unclear. This continues the September 23 BOM talk ([[Meeting_Notes_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026|Sep 23]]). Nathan Carver did not join.

**Val's document on GitHub and MSBC.** Val asked if Genadi had read his write-up on linking the bill of materials, GitHub and MSBC. Genadi said he has no problem keeping parts, drawings and documentation in GitHub. What he does not understand is how the bill of materials can live in GitHub.

**The Excel file.** Genadi showed the Excel file that Lev, Felipe, Mikhail and sales use to find a part number (for example, V43 for South Dakota). Val said this file is a finished product made by hand. Val can make files like this on the fly from GitHub. All he needs from Genadi is to organize GitHub.

**BC is not the source of truth.** Genadi showed the Flex machine in Business Central: modules (base, monitors) and the full BOM with top assembly and parts, and said this is what would have to move to GitHub. Val said this is wrong: nothing is transferred from BC. The source of truth starts from Genadi's drawings. Val read the rule from his document:
- One source of truth for product structure: the latest released design in the GitHub hardware repo.
- Business Central holds a copy of that structure, plus everything commercial.
- Data flows one way only, GitHub to BC. Nothing flows back.
- If the two systems disagree, GitHub is right and BC is corrected.

**Engineering BOM vs manufacturing BOM.** Val said Genadi owns the engineering BOM. The manufacturing BOM is then built automatically and adds vendors, prices, lead times, packaging, labor and consumables. Those commercial fields come from BC. Design items and drawings live in GitHub. Val said GitHub gives revision history, storage, and one place for drawing files.

**Genadi's concerns.** Genadi said about 30% of parts come from SolidWorks and the rest are bought (he also said the product is about 50% mechanical, 50% electronics). The Flex has about 15 variants (printer, vertical or horizontal, buttons) from one SolidWorks file. BC is a strong ERP that already keeps these BOMs. He cannot see how to keep "a thousand files" in GitHub, and he does not yet see the gain. Val said it is not a thousand files: one export, and variants pull different links.

**Revisions.** Genadi said today a new revision goes into the BOM with quantity zero, old stock is used up, then the new one takes over. Several people coordinate this. Val said in his model the new revision is active as soon as it is entered, new orders use it, and old parts can still be used while stock lasts. Today three or four people must agree by email; in Val's model that is not needed.

**Two open questions, as Val summed them up:**
1. How to build one BOM for a product with many modules, when about half the parts come ready-made from vendors and are not in SolidWorks.
2. When a revision happens, how stock of the old component is used up, and how this is marked in inventory control.

Genadi added a third point: how the BOM is built from GitHub. Val said he does not think the BOM is built in GitHub. GitHub holds the source data; the BOM is built in BC, automatically, from GitHub as the source of truth. The research question is: **how to create the BOM in BC automatically, with GitHub as the source of truth for all components.** Val will work through this with Claude and come back. He suggested an experiment with a test BOM; Genadi proposed using the new Slim, and Val agreed.

**Modem example.** Genadi showed adding a modem to a kit in BC through the edit list. Val asked what the source of truth for the modem is: if its manufacturer, source or design changes, that must change in the source of truth. The same method applies to metal made by a supplier in China, modems, buttons, PCBs, displays and harnesses. Genadi confirmed he makes harness drawings; the supplier makes technical drawings, and Genadi approves connectors, length and wire gauge.

**Street cabinet agenda item (start).** Genadi said he spent the day on modems and is confused.
- **Transact printer.** Genadi met Transact about a printer product. They sell it only with new printers, have some stock, and a new type comes next year. It talks to the IQ over plain RS-232 (three wires, a normal modem cable). Genadi wants to fit a standard DB9 serial connector so a normal cable always plugs in. **Val agreed to this change.** Genadi asked Transact to sell one unit for the Georgia office; no answer yet (they have a new sales person). Val was copied and saw the email.
- **LTE modems.** The LTE module chosen with Pavel works after a firmware upgrade. The problem: LTE modules are now hard to buy locally; Misha bought a small number (about 8–10, unclear). 5G modules from China were quoted at about $150 (Val said $160). Val does not know the difference between 5G and LTE beyond speed; if 5G works better at locations, take 5G. He doubts the price, since these parts are in every phone, and thinks the supplier may be wrong. Genadi said it is a laptop module, not a phone module, and wants to research the market. Val said he needs to deploy machines and has already sent the quantities.
- **Firmware USB.** Genadi and Pavel agreed an hour earlier that Pavel will prepare a USB stick. Plugged into the machine, it upgrades the modem firmware automatically, because bought modules come with different firmware.

The segment ends here; the meeting continues in [[Meeting_Notes_Street_Machine_Cabinet_Layout_and_FlexPort_Enclosure-September-24-2026|Segment 2]].

## Decisions Made

- **The GitHub hardware repo (latest released design) is the one source of truth for product structure. BC holds a copy plus commercial data. Data flows one way, GitHub to BC. If they disagree, GitHub wins.** — Val restated his written rule. Genadi said he does not argue with it but does not yet see the gain. (Val)
- **The BOM is built in BC automatically, from GitHub source data, not in GitHub.** — Val's position at the end of the discussion. How to do it is still open research. (Val)
- **The street machine gets a standard DB9 serial connector for the Transact printer.** (Genadi proposed; Val agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Research, with Claude, how to build the BOM in BC automatically from GitHub; answer the two questions (multi-module BOM with bought parts; using up stock on a revision) and come back to Genadi | TBD | High | Val: "let me work through this with Claude and I will come back to you" |
| 2 | Val Levitan, Genadi Peari | Run a test BOM on the new Slim to see how it is built | TBD | Normal | Val suggested a test BOM; Genadi proposed the Slim; Val agreed |
| 3 | Genadi Peari | Make the harness and fit a DB9 serial connector for the Transact printer | TBD | Normal | Val agreed to the change |
| 4 | Genadi Peari | Get one Transact printer unit for the Georgia office | TBD | Normal | Asked Transact; no answer yet |
| 5 | Genadi Peari | Research the LTE / 5G modem market and prices; work with the Chinese suppliers tonight | TBD | High | LTE hard to buy locally; Val needs machines deployed |
| 6 | Pavel Frolov | Prepare a USB stick that upgrades the modem firmware automatically when plugged in | TBD | Normal | Agreed between Genadi and Pavel before this meeting (reported by Genadi) |

## Open Questions

- How to build one BOM for a multi-module product when about half the parts are bought ready-made and not in SolidWorks. (Genadi; Val to research)
- On a revision, how old stock is used up and how it is marked in inventory control. (Genadi; Val to research)
- 5G vs LTE for the street/Flex modem, and whether ~$150–160 per 5G module is a real market price. (Genadi, Val)

## Dispatch Log

---
*Processed from Teams transcript on September 24, 2026, 5:45 PM Eastern*
*Source meeting: Alignment on mechanical drawings repo and street machines design - September-24-2026*
