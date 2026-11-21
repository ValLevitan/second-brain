# Meeting Summary — Call with Genadi Peari
**Date:** November 20, 2026, ~3:09 PM – ~3:25 PM Eastern (recording)
**Duration:** ~15 minutes
**Attendees:** Val Levitan, Genadi Peari
**Language:** Russian
**Source:** Ad-hoc Teams call (no calendar invite)
**Raw transcript:** [[Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026]]

## Summary

**Data sheets in GitHub.** Val wants all drawings and data sheets for every part we buy or build in GitHub — own designs exported from SOLIDWORKS, purchased parts with full supplier information. It looked to him as if new data stopped coming in. Genadi: drawings are almost all there; for this one cabinet assembly all data sheets are loaded (TVs, power supplies, main parts); for other parts he has not gone in yet. Val: without data sheets there are no data contracts and no bill of materials; he wants to be sure Nathan is not faking the assembly. Both agreed: if something is missing, the agent should say so, and it can find a data sheet from the part number faster than a person.

**Focus: BOM with Nathan, not procurement.** Genadi spent the day on procurement because he understood Val asked for it. Val: he was specific — do not work on procurement; work only with Nathan on the bill of materials.

**Procurement example.** Genadi asked a supplier for 50 sets of modification parts (monitor covers) for IQ assembly; the supplier quoted $1,500 air freight for about three boxes and included parts that should come by ocean. Procurement only asked "why so expensive" instead of using the packing list (volume, weight) to get its own quote and removing parts that do not need air. Genadi thinks it should cost far less.

**Val's plan: standards plus agents.** Val knows about such cases and fears Genadi will burn out doing this by hand; overpaying is better than losing him. Plan: Val writes a standard from this transcript and files it in the knowledge base (standards repository); AI executives read the standards before acting. Genadi should do the same: write his knowledge as standards in GitHub, and build his own agent that once a day checks all POs against the standards and lists mismatches, so he can tell each person what to fix. Nathan's MSBC MCP covers only part of MSBC; when the agent lacks access, it drafts a use case for Nathan, puts it in GitHub, Nathan adds it to the MCP — a closed loop.

## Decisions Made

- **Genadi works only with Nathan on the BOM; no procurement work.** (Val)
- **Purchasing knowledge goes into written standards in GitHub, checked by agents, not done by hand.** (Val; Genadi agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Write a standard from this call (freight quotes from packing lists) and file it | TBD | Normal | |
| 2 | Val Levitan | Send Genadi the transcript | TBD | Low | |
| 3 | Genadi Peari | Load drawings and data sheets for all parts into GitHub | TBD | High | Needed for data contracts |
| 4 | Genadi Peari | Write his procurement knowledge as standards in GitHub | TBD | Normal | |
| 5 | Genadi Peari | Build an agent that checks all POs daily against standards and lists mismatches | TBD | Normal | MCP gaps go to Nathan as use cases |

## Open Questions

- Is Nathan's BOM assembly really built from data sheets? Val wants to confirm. (Val)

## Dispatch Log

---
*Processed from Teams ad-hoc call transcript on November 20, 2026, ~10:40 PM Eastern*
*Source meeting: Call with Genadi Peari*
