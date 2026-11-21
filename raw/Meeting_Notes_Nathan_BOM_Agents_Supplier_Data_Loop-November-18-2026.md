# Meeting Summary — AI-logic for assembling BOM-continued-November-18
**Date:** November 18, 2026, 4:36 PM – 4:54 PM Eastern
**Duration:** ~19 minutes
**Attendees:** Val Levitan, Nathan Carver, Genadi Peari
**Language:** English
**Raw transcript:** [[Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026]]

## Summary

**Spike result.** Nathan ran several simulations with three scoped agents — spec writer, assembler, auditor — plus a simulated non-expert user (playing Genadi). The assembler got no technical direction: only the design purpose, where the data contracts are, a flat list of parts, and the interfaces needed. It built a power-supply sub-assembly. It asked good questions over several rounds, found contracts that are still missing, and iterated with the auditors' findings. The closest it got to a power figure was 120 V / 60 Hz. Each run is in a sandbox and starts blank.

**Reactions.** Val read every sentence of Nathan's report and is "ecstatic". The questions came up because information was missing; with better data there would be no questions. Genadi: more than half of the answers are already in the product requirements. He called the result incredible.

**Next spike (Val's direction).** Do not send the assembler's questions to Genadi. Build a loop:
1. Find who the supplier is and their contact details.
2. Work out what is missing (data sheet, holes, fastening, connectors, etc.).
3. Message the supplier ("I am your client, I am missing this data sheet, please send it"), chase it.
4. Take in the data, update the data contract and the flat list.
5. Try to assemble again; ask what is still missing; repeat — until the sub-assembly is built with no human help.
Ask Genadi only when the supplier itself is unknown, and only once. Data contracts must be a self-learning loop. Later, with solid data contracts, the same loop can look for new suppliers that fit.

**Genadi's point.** Generic parts can come from any supplier; branded part numbers too. Val: we are not buying — we go back to the exact supplier already in the BOM to get missing data.

**Data setup.** Genadi will add supplier information (not data) to the parts files. Val likes that some data is missing — it tests the chasing agent. Nathan will not fill in all the data.

**Next meeting.** Friday Nov 20 at 4 PM; Val books it. Nathan will take this transcript and set the focus for a 2–3 day spike. After the call Genadi asked Val for a few minutes; Val said he would call him separately within 5 minutes.

## Decisions Made

- **Next spike: an agent loop that finds the supplier, requests and chases missing data, updates data contracts, and re-assembles until done; no answers or hints from people.** — To make data contracts self-learning. (Decided by Val; Nathan agreed)
- **Genadi is asked only when a supplier is unknown, once.** — To save his time. (Decided by Val)
- **Leave some part data missing on purpose; give supplier info only.** — To test the chasing agent. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver | Run the next spike: supplier data-chase loop that updates data contracts and re-assembles the sub-assembly | Nov 20, 2026 | High | Review Friday 4 PM |
| 2 | Genadi Peari | Add supplier information (no data) to the parts files | Nov 20, 2026 | High | Needed before the spike can chase suppliers |
| 3 | Val Levitan | Book the Friday Nov 20, 4 PM review meeting | Nov 18, 2026 | Normal | |
| 4 | Val Levitan | Send this transcript to Nathan and Genadi | Nov 18, 2026 | Normal | |

## Open Questions

None.

## Dispatch Log

---
*Processed from Teams transcript on November 18, 2026*
*Source meeting: AI-logic for assembling BOM-continued-November-18*
