# Meeting Summary — GitHub_to_MSBC_BOM_Integration
**Date:** September 30, 2026, 10:00 AM – 10:51 AM Eastern
**Duration:** ~48 minutes of talk (recording 51 minutes)
**Attendees:** Val Levitan, Genadi Peari, Nathan Carver, Lev Rudky
**Raw transcript:** [[Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026]]

## Summary

**Goal set by Val.** Genadi must be able to update drawings and supplier specs at any time. When a changed part is in a bill of material (BOM), a new revision is made in GitHub, and the BOM and costs are then updated in MSBC. Supplier data (banking, address, contacts) lives only in MSBC. Engineering files (drawings, specs) live only in GitHub. Engineers never change MSBC; administration never changes GitHub. Val asked the team to raise concerns one by one and solve them, not reject the idea.

**Genadi's concern.** He fully supports keeping all engineering data in GitHub (parts, specs, drawings, PCB and mechanical designs). He cannot see how a structured, multi-level BOM (assemblies, sub-assemblies, modules) can be kept in GitHub, or how a flat list can be moved into MSBC, where production orders need sub-assemblies (for example a monitor assembly). He suggested keeping the part database and history in GitHub but building the BOM structure in MSBC.

**Val's position.** GitHub holds one flat list of every item — parts Genadi designs in SolidWorks and supplier parts he specs and approves (with the supplier's drawing). Revisions replace items in that flat list. The grouping into a structured BOM happens in MSBC, and the step between GitHub and MSBC should be automated, not manual. The design is the one source of truth; Val does not want a second one. New part numbers should come from a written part-number standard in the GitHub standards repo, applied by Claude, and pushed to MSBC once when the part is created. Genadi agreed to that part-number flow.

**Nathan's view.** Treat it like a build script: keep whatever structure is needed in GitHub, then an automated build step turns it into data MSBC can take. He needs real examples: current BOM structures, what the flat versions look like, and the MSBC structure. The more consistent the files are, the easier the automation. He can experiment in the development MSBC instances. Genadi's workflow should change little; mainly the files must be built consistently.

**Lev's caution.** A new item in BC needs more than engineering data: posting groups, dimensions, inventory type, units of measure. So a new part number has two inputs, engineering and accounting. It is worth experimenting, but there are open practical questions.

**Phasing.** Genadi proposed doing it in steps: first keep the item database in GitHub, then deal with BOMs. Nathan agreed to experiment in phases, items first. Genadi also asked to check how others do this before a deep investigation; Nathan agreed.

**How Genadi builds a BOM today.** SolidWorks holds only the parts JVL designs, not fasteners, locks, tape or wires (too heavy, needs a much stronger computer). Designed parts get a number in SolidWorks. After the project, he enters those numbers by hand in MSBC and adds standard parts with quantities (for example a washer x6).

**Meeting ended early.** Val said the meeting was not productive, released Nathan and Lev so their hours are not wasted, and moved to a separate meeting with Genadi.

## Decisions Made

- **Engineering data lives in GitHub; supplier and financial data lives in MSBC; neither side edits the other.** — Val's set rule for the business. (Decided by Val; Genadi agreed for engineering data.)
- **New part numbers come from a written standard in the GitHub standards repo, assigned by Claude, and pushed once to MSBC.** — Genadi agreed ("Perfect"). (Val, Genadi)
- **Nathan will explore the GitHub→MSBC bridge in phases, starting with items before BOMs.** — Genadi proposed, Nathan agreed. (Genadi, Nathan)

Considered and still open: whether the BOM structure is kept in GitHub (flat list) or built in MSBC. Val says flat in GitHub and automated grouping in MSBC; Genadi still does not see the benefit. Not resolved.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver | Experiment with the GitHub→MSBC item/BOM bridge in phases, items first, using the development MSBC instances | TBD | Normal | Needs example BOMs and flat lists |
| 2 | Genadi Peari | Provide Nathan with example BOM structures and flat lists as used today | TBD | Normal | Implied by Nathan's request; not an explicit commitment |
| 3 | Nathan Carver | Check how others handle engineering-to-BC BOM sync (best practice) before deep work | TBD | Low | Genadi's suggestion, Nathan agreed |
| 4 | Val Levitan | Hold a separate meeting with Genadi on how he gets from the design tool to a flat BOM | Sep 30, 2026 | Normal | Booked for 12:00 PM the same day |

## Open Questions

- How is a multi-level BOM (assemblies, sub-assemblies) formed in MSBC from a flat GitHub list, and by what rule, when every product is different? (Genadi)
- How are accounting fields for a new item (posting groups, dimensions, units of measure) supplied if the item starts in GitHub? (Lev)
- What is the real advantage over building the BOM directly in MSBC? (Genadi)

## Dispatch Log

---
*Processed from Teams transcript on 2026-09-30 12:20 PM Eastern*
*Source meeting: GitHub_to_MSBC_BOM_Integration*
