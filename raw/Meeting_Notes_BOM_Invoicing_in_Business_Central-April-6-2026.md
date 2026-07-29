# Meeting Summary — Treatment of BOM in MSBC
**Date:** April 6, 2026, 2:33 PM Eastern
**Duration:** ~17 minutes
**Attendees:** Val Levitan, Genadi Peari, Lev Rudky

## Summary

The meeting addressed a significant invoicing problem caused by how JVL currently structures its Bill of Materials (BOM) in Microsoft Business Central. Val opened by acknowledging that the existing matrix approach to product configuration — breaking machines into modular blocks — was conceptually sound, but creates a serious operational problem at the invoicing stage.

**The core problem:** When Business Central generates an invoice, it presents the BOM matrix as individual line items (options/modules). However, JVL sells machines as a single unit at a single price — they do not want and cannot afford to show customers the internal sub-block breakdown. To work around this limitation, the team has been creating invoices manually in Excel and sending those to customers instead of the system-generated ones. Customers believe these Excel invoices are the originals, but they are not. This means: (1) the system does not reflect that a machine was actually sold, (2) people start posting payments against the Excel-generated invoice rather than a real system invoice, and (3) the accounting trail breaks down.

Val cited a specific escalation where a customer (referenced as "Dakota") requested a single line item with total price for the full machine configuration, with all other components listed at zero price. This led to downstream problems: in Georgia, the sales rep (Philippe) had a customer questioning why items previously shown at $0 were now being charged at stock price. The sales rep had to explain it was a workaround for system limitations. In some cases, the workaround led to white sectors (a product module) being sold at $360 when the actual cost was $350 plus assembly at $390 — a money-losing transaction that went unnoticed because the real pricing was obscured by the manual invoice process. Val described this as a situation that must be stopped immediately and replaced with proper accounting controls.

**The proposed solution:** Genadi proposed creating a top-level part number (a parent BOM item) that encapsulates the 4 existing modular blocks (cabinet, bill acceptor, peripherals/printer, and customer-specific kit). This top-level item would be the only item that goes onto the sales order and invoice. Business Central would show a single line — e.g., "Flex D27" — with one description and one total price. The underlying 4 blocks remain in the system as sub-components of this top-level BOM for internal tracking, production, and cost accounting purposes, but they are invisible to the customer on the invoice.

Lev confirmed that Business Central natively supports multi-level BOMs — a top-level assembly item containing sub-assemblies. He noted that each unique configuration (e.g., machine with 4 modules vs. machine with 6 modules) would require its own top-level part number with a corresponding BOM. He recommended starting with the most common ("hot") configurations currently being sold, rather than trying to create part numbers for every possible permutation upfront. New configurations would get new part numbers as needed.

Genadi emphasized that the top-level part number should have a smart, semantic naming convention so that anyone looking at it can immediately understand the configuration (e.g., which printer is included, which bill acceptor). He referenced the existing matrix document that he had shared in the team chat with Lev, noting it already defines the 5 modular blocks that need to be encoded.

Val offered to help create good descriptions for the BOM items using an AI-assisted approach — he mentioned being able to generate descriptive part names and potentially build queries/lookups to help sales staff easily find the right top-level part number when creating sales orders.

**Implementation timeline:** Val asked whether this could be implemented by April 13, 2026. Lev confirmed it is a matter of days, not months, but noted that the main design question is how to encode the configuration into the part number itself. Genadi added that the Maple product line is already being set up in the new system. Lev said he doesn't see a reason why April 13 wouldn't work, though he and Genadi need to discuss the specifics between themselves first.

## Decisions Made

- **Adopt top-level BOM structure for invoicing:** Instead of showing modular sub-blocks on customer invoices, create a parent-level part number per configuration that appears as a single line item with one price. Sub-blocks remain as internal BOM components. (Decided by Val, confirmed by Genadi and Lev)
- **Stop the Excel invoice workaround:** The practice of generating manual invoices outside Business Central must end once the new BOM structure is in place. (Decided by Val)
- **Start with current high-volume configurations:** Create top-level part numbers for configurations currently being sold, not all possible permutations. (Proposed by Lev, agreed by all)
- **Target go-live: April 13, 2026:** The new BOM structure should be operational by this date. (Set by Val, confirmed by Lev)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lev Rudky | Implement top-level BOM parent items in Business Central for current high-volume machine configurations, with proper part number encoding that reflects the configuration contents | April 13, 2026 | High | Blocks the elimination of the manual Excel invoice workaround; accounting integrity depends on this |
| 2 | Genadi Peari | Work with Lev to define the semantic part number naming convention for top-level BOM items so each number is self-describing (indicates which cabinet, bill acceptor, printer, and kit are included) | Before April 13, 2026 | High | Naming convention must be finalized before Lev can create the part numbers; ensures sales staff can identify correct configurations |
| 3 | Lev Rudky & Genadi Peari | Meet separately to discuss and finalize the technical details of the BOM restructuring | ASAP (within days) | High | The April 13 deadline depends on them aligning on the design quickly |

## Open Questions

- What specific encoding scheme will be used for the top-level part numbers? (Lev and Genadi to determine)
- How many current configurations need top-level part numbers for the April 13 launch? (Depends on Lev's assessment of active sales configurations)
- Will the Maple product line follow the same structure, or is it already being handled differently? (Genadi mentioned Maple is already in the new system)

---
*Processed from Teams transcript on April 8, 2026*
*Source meeting: Treatment of BOM in MSBC*
