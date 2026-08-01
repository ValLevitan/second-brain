# Meeting Summary — BC Single Source of Truth & MRP Data Discipline
**Date:** June 25, 2026, 6:11 PM Eastern
**Duration:** ~40 minutes
**Attendees:** Val Levitan, Lev Rudky, Mikhail Perelman

## Summary

Val laid out a non-negotiable position: Business Central (BC) is the single source of truth for all financial and operational data. No Excel workarounds, no parallel systems.

The core problem: Mikhail works with Excel exports from BC, hides columns he knows contain incorrect data, and applies his own institutional knowledge to compensate. This makes Mikhail the exclusive holder of accurate information — the rest of the company can't see what he sees or reproduce his conclusions. Val used the term "exclusive knowledge owner" repeatedly.

Val explained MCP as a tool that lets users query BC in natural language without engineering knowledge. But MCP or any other tool will only return accurate results if the underlying BC data is clean. If the data is "garbage," every tool — Excel, MCP, or manual — will return garbage.

A concrete example emerged around engineering drawings. Currently, Gena (an engineer) emails drawings to Mikhail, who manually attaches them to purchase orders sent by email. Val wants drawings stored directly in BC, attached to items, so that purchase orders can only be issued through the system with the correct drawing automatically included. If no drawing exists in BC, no PO can go out. This eliminates the email side-channel and forces drawing discipline.

Lev agreed with the single source of truth principle but raised a concern: the approach should not create excessive maintenance overhead, especially for situational data that changes rapidly during active procurement (revision back-and-forth, delays, exceptions). Val acknowledged some items will need workarounds for JVL's unique processes but insisted the foundation must be one source of truth.

Georgia warehouse inventory was discussed briefly. A physical recount was done last Thursday/Friday. Corrections are being entered. Val estimated the numbers will be fully accurate within 2–3 weeks, though he said 3 months conservatively. Some areas of the warehouse will need to be recounted again.

Val closed by telling Mikhail directly: "We will not go the road you want. I hope you can adapt. I will help you with everything." Mikhail accepted, saying he just needs reliable reports — if BC can produce them, he's fine without Excel.

## Decisions Made

- **Business Central is the single source of truth for all company data.** No Excel workarounds will be permitted going forward. (Val — non-negotiable)
- **Engineering drawings must be stored in BC, attached to items/purchase orders.** POs should only be issuable through the system, with drawings attached automatically. Email-based POs with manual drawing attachments will be phased out. (Val)
- **Georgia warehouse inventory reconciliation will continue** with additional recounts until numbers are fully accurate. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Help Mikhail learn BC workflows and provide training to replace Excel-based process | TBD | High | Mikhail accepted the direction but needs hands-on support to transition |
| 2 | Val / Lev | Configure BC so purchase orders can only be issued through the system with drawings attached | TBD | High | Eliminates email side-channel for POs and enforces drawing discipline |
| 3 | Georgia team | Continue warehouse inventory recount and enter corrections into BC | ~July 16 (2-3 weeks) | High | Physical recount started last week; some sections need to be recounted again |

## Open Questions

- How to handle situational/transient data during active procurement (revision negotiations, delays, exceptions) without creating excessive maintenance burden in BC. Lev raised this; no resolution reached.
- Who will organize the migration of existing engineering drawings (~1,000) into BC. Mikhail flagged the volume; Val said it's an organizational task, not extra work.

---
*Processed from Teams transcript on June 26, 2026*
*Source meeting: MSBC_MRP*
*Initiative: [[Procurement MCP Adoption]]*
