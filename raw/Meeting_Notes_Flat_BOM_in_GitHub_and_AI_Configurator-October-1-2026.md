# Meeting Summary — Various
**Date:** October 1, 2026, 5:02 PM – 5:39 PM Eastern
**Duration:** About 37 minutes
**Segment:** Segment 2 of 3
**Attendees:** Val Levitan, Genadi Peari
**Raw transcript:** [[Meeting_Transcript_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026]]

Teams meeting organized by Val. Held in Russian. Continues the Sep 30 BOM discussion: [[Meeting_Notes_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026]]. Other segments: [[Meeting_Notes_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026]], [[Meeting_Notes_Street_Machine_Cabinet_Dashboard_and_Printer_Access-October-1-2026]].

## Summary

**Why Val wants this.** Val said the goal is not just to export a bill of materials and keep orders and admin in MSBC. That view is too narrow and kills what he wants to build. He does not want to grow headcount. Good people are hard to find, the team works in different places, and he does not want a layer of C-level managers and bureaucracy under him. His replacement for that is AI executives: the AI CFO works well, he has started giving work to the AI COO, and the architecture for an AI project manager (which will sit in every meeting) is nearly done.

**SolidWorks is not the point.** Val said flat BOM export from SolidWorks, and marketplace tools that push a BOM straight into Business Central, have existed for years — but that is the old way and leaves no room for AI. Genadi said SolidWorks is only a design tool: at release maybe 30% of the BOM comes from it, and after that all sustaining changes have no link to SolidWorks. Val agreed.

**Supplier history must leave people's heads.** Val said much of the work is ongoing contact with suppliers (many still prospects, not finance suppliers): drawings, technical data, samples, versions from each supplier. Today this lives in email and chat, and only Genadi knows it. Val needs it moved into AI memory, with version history in GitHub. Genadi said he thought this was already agreed; Val said yes, there is no resistance.

**Split of roles.** After versioning is in GitHub, MSBC holds financial and administrative management per supplier. Only the finished BOM goes into MSBC. The configurator must be built outside MSBC, as AI logic.

**Genadi's doubts.** Genadi cannot see how a multi-level BOM tree in MSBC can be built from a flat GitHub structure, since BOMs must follow production steps and change on the fly. His example: special screws added for a bill acceptor connector — how would AI know to find or create that item? Val said categories (for example money devices: bill acceptor, printer, AFT) and the reasons recorded in each GitHub commit give AI the logic, and AI handles this better than a person. Genadi agreed all ECOs should be stored in GitHub and checked every time, but still does not see how the BOM is built. Val said he will not see it until he works with it.

**Pilot.** Val proposed a working session of about two hours on one flat BOM, where Val works with it in front of Genadi. They chose the **Flex Pay Slim** BOM; Genadi said Slim configurations are coming (Texas was mentioned). Val asked Genadi to put the exact MSBC part number in the chat. Genadi said the number he gave is the latest one, built for Georgia: it has all purchased components, a custom part that changes by jurisdiction, kits for bill acceptor and card dispenser, and correct subassemblies, but not small items such as screw counts. Val will take this transcript and the part number and ask Claude Code to build the structure: pull the part number as a flat list with all suppliers for every part, then work backward. Val said he is almost sure he can do this himself, and that he has needed this from Nathan for a long time.

**Genadi's first step.** Genadi suggested starting now with item cards in GitHub for every item bought today (data from MSBC), with revisions, vendor changes and records. Val said quotations do not belong in GitHub.

**No hybrid.** Genadi said a hybrid (MSBC builds the multi-level BOM, the rest elsewhere) seems realistic, and asked why MSBC cannot be the source of truth for quantities. Val said no: he wants an AI agent to watch the BOM, production, orders and shortages itself. Sources of truth are the flat BOM in GitHub, facts such as lead time and MOQ, the physical count, and the forecast. MSBC as a BOM tool is a poor form of what is possible today. Genadi suggested a quick module in GitHub to replace BOM building in MSBC.

The segment ended with side talk (Grok's new finance features; Claude fixing Genadi's wife's phone). Genadi then asked to discuss the Flexport layout for the street machine before giving a picture to Igor. Val said he was ready now (see Segment 3).

## Decisions Made

- **Only the finished BOM goes into MSBC; the configurator and BOM logic live outside MSBC as AI logic, with versions in GitHub — no hybrid.** — Val wants an AI agent to manage BOM, production, orders and shortages. Genadi still has doubts. (Decided by Val)
- **Pilot on the Flex Pay Slim BOM.** — Genadi agreed; it is the latest BOM he built. (Decided by Val and Genadi Peari)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Post the exact MSBC part number for the Flex Pay Slim BOM in the chat | Oct 1, 2026 | Normal | Genadi said he already gave a number; confirm it is in the chat |
| 2 | Val Levitan | Have Claude Code build the GitHub structure: Flex Pay Slim as a flat list with all suppliers for every part | TBD | Normal | Uses this transcript and the part number |
| 3 | Val Levitan, Genadi Peari | Hold a working session (about two hours) on the flat BOM | TBD | Normal | Val works with it in front of Genadi |

## Open Questions

- How multi-level BOM trees and production-order changes come out of a flat GitHub list. Raised by Genadi; not resolved.
- Whether Nathan's experiment (from Sep 30) is still needed, since Val said he can do it himself. Not resolved.

## Dispatch Log

---
*Processed from Teams transcript on October 1, 2026, 6:15 PM Eastern*
*Source meeting: Various*
