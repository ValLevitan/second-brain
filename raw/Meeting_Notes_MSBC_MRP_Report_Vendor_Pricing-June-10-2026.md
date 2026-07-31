# Meeting Summary — MSBC MRP Report: Vendor & Item Pricing
**Date:** June 10, 2026, 2:39 PM Eastern
**Duration:** ~19 minutes
**Attendees:** Val Levitan, Mikhail Perelman (Misha), Lev Rudky
*(Referenced, not present: Nathan Carver — built/demoed the report; Aaron Bockelie — re: BC licence)*

## Summary

The goal is to get Nathan's Material Requirement Planning (MRP) report in Microsoft Business Central (MSBC) to the point Misha can run purchasing from it. Two things are missing: vendor prices on many parts, and Misha's trust in the system.

**Pricing data.** Roughly 800–1,000 items still need vendor prices. Some prices exist in the old Navision system and can be exported, but they need validating — nobody knows which are still current. The rest must be keyed in by hand. Lev raised that hand-entry is the real bottleneck, and that some items carry tiered pricing (samples, 100/300/500 units), so it isn't a single clean list.

**Who enters the data.** Val wants to use Erica, the woman who worked for them in the Mexico office, for manual entry. JVL has a spare Business Central seat: Nathan's account holds a second licence with lower permissions, and Lev can attach Erica to it and hand her credentials. (Aaron also has a licence but doesn't use it; Lev excluded it long ago.)

**The pricing argument.** Val first proposed seeding every un-priced item with the lowest historical price, so a PO could be issued and the vendor would either accept or renegotiate. Misha pushed back: he wouldn't be able to tell which prices he personally negotiated from auto-filled ones, and he'd end up issuing POs at prices that no longer exist. They agreed on Misha's alternative instead (see Decisions).

**Excel vs. Business Central.** The core friction: Misha runs everything in a parallel Excel sheet — pulls a snapshot out of Navision, then tracks PO issued / PO signed / shipped and makes his decisions there. Val pushed hard that this is two competing "sources of truth" that conflict, that it only ever worked with constant import/export and a dedicated person, and that Misha can now do the same status tracking and queries directly in Business Central (including via the MCP integration). Misha stayed skeptical — he's never used BC hands-on — but agreed to try, his real question being whether BC will genuinely beat what he can do in Excel. Val: "a million percent," because the whole company works in one system, not just him.

**Report build-out.** Nathan's demo showed only the core columns. Both Val and Lev agree even that core already helps with inventory, which is a current pain point. More columns can be added on request at no real cost; the bigger value comes when Nathan does the BOM breakdown to the lowest level. Computed columns — payables ("платежки") and Misha's PO-status/comment fields — are deferred to a later phase. The report is considered usable now even if not perfect.

## Decisions Made

- **Un-priced items get $0, not a guessed price.** Correct prices fill in organically as POs are issued; target ~6 months to close the gap. (Misha proposed, Val accepted.)
- **Business Central is the single source of truth.** Misha moves his status/comment tracking out of Excel and into BC. (Val pushed; Misha agreed but skeptical.)
- **Payables and computed/comment columns deferred** to a later phase of the report. (Val, Lev.)
- **Erica to be onboarded** on the spare BC seat for manual data entry. (Val, Lev.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Mikhail Perelman | Run a physical inventory count | TBD | High | Both Val and Misha called this critical |
| 2 | Mikhail Perelman | Work the un-priced items: leave at $0, enter correct prices as POs are issued; do PO status/comment tracking in BC, not Excel | Ongoing (~6 mo) | High | The agreed way of working; ends the Excel/BC split |
| 3 | Lev Rudky | Set Erica up with credentials on the spare BC seat (Nathan's 2nd licence) for hand-entering vendor + price data | TBD | Normal | ~800–1,000 items need prices; manual entry is the bottleneck |
| 4 | Lev Rudky | Export existing Navision prices to seed BC, and flag which are still current | TBD | Normal | Some prices exist in old Navision but need validating |
| 5 | Lev Rudky / Misha | Tell Nathan which extra columns to add to the MRP report | TBD | Normal | Demo showed only core columns |
| 6 | Nathan Carver | Extend the report: add requested columns, build the BOM breakdown to the lowest level (later phase: payables + PO-status/comment columns) | TBD | Normal | Nathan was not in this meeting — needs briefing |

## Open Questions

- How Misha's per-part status tracking (PO issued, PO signed or not, shipped or not) gets represented in BC — shipping status in particular isn't entered today.
- Exactly which additional columns Nathan should add.
- When the physical inventory count happens and who runs it.

---
*Processed from Teams transcript on June 11, 2026*
*Source meeting: Vendor_Card_Items_MSBC — 20260610_103942*
