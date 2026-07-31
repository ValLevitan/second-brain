# Meeting Summary — Genadi General Alignment

**Date:** 2026-05-22, 3:32 PM Eastern
**Duration:** ~15 minutes
**Attendees:** Val Levitan, Genadi Peari
**Source language:** Russian (mixed with English terms); Teams transcription was heavily garbled — interpretations below reconstruct meaning from context, not verbatim quotes.

## Summary

A short 1:1 between Val and Genadi covering Genadi's current task load, his upcoming Georgia trip plan, parts and sourcing status, BOM gaps for the Prinzera build, and a tail-end realization by Val that something in the Flex POS release schedule looked off.

### Genadi's current task load

Genadi opened by enumerating what he is actively working on:
- **Plastic parts** — Andrei (Andriy) is writing/sending the relevant work right now.
- **INBC port numbers** — Genadi is finishing these so Andrei can play/test next week.
- **Slim build harness** — still needs the build-of-materials (BOM) and review harness for the Slim product, falling under what Genadi described as "complex and more or less minor instructions" still outstanding.

### Georgia trip plan (May 26–30, 2026)

Genadi laid out his itinerary in response to Val's question on timing:
- **Outbound:** Tuesday May 26 morning, arriving Tuesday afternoon.
- **Route:** going to Buffalo first, then on to the Georgia site.
- **Return:** Saturday May 30 morning — deliberately booked so he has a full working day on Friday May 29.

He flagged that he had spoken with Elizabeth and Filipp the prior day and they have a "whole list" of tasks for the visit. The principal items he intends to tackle on site:

1. **Assemble the Flex Cash Dispenser samples** — JVL received 2 sample units. Per a prior plan (Val confirmed), one is to be assembled as a Cash Dispenser and the second as a Recycler. The 2nd Recycler unit had been sent on to China; one of the returned units is the one to work with. Plan is to review, assemble, measure, and correct the build.
2. **Walk through assembly steps with the on-site team** — Genadi reviewed the steps with Elizabeth earlier (he showed her), but wants to walk through them in person on the floor to surface any concerns. Includes minor items raised by Chinese vendor / lens / office details that need on-site review.
3. **Maple assembly review** — verify the unit was put together correctly and wired/connected properly.
4. **Parts-finding / shop organization review** — Filipp had flagged that in Toronto, the setup made parts very easy to find, but the Georgia team appears to spend too much time looking for parts. Genadi doesn't know what Toronto did differently and wants to use the on-site visit to understand the gap and propose improvements. Also wants to observe how the team assembles machines to spot anything they may not understand or that could be improved.

### Val's optional suggestion — Satellite Vegas warehouse

Val recommended Genadi consider a side trip to the Satellite Vegas warehouse if time permits, but cautioned it is ~2 hours of driving each way and would consume an entire day. Genadi noted Elizabeth doesn't know that warehouse well. Val explained the warehouse mostly holds older machines — Maple and Altera — and said he has "serious hope" that inventory ends up shipping to Texas.

### Slim Station monitor sourcing

Genadi flagged that nobody else is actively driving the Slim Station monitor sourcing — he is. They have found a source but the price is too high. Genadi is currently negotiating with the Chinese vendor for a kit (monitor plus controller) at roughly **$60–$70 with controller**. The vendor's current quote is **$90**, which Genadi considers $20–$30 too expensive at the product level. He believes it is worth spending the time to fight the price. Misha is aware of all of this but is not in a position to drive this kind of sourcing work himself.

### Molds timeline check

Val asked when the molds would be ready. Earlier guidance had been July. Genadi reported Misha is now hearing **mid-June**, which is effectively ~3 weeks out.

### Prinzera parts and 10-unit build

Val asked whether parts were on hand to assemble 10 Prinzera units. Genadi answered no — not all parts are there. They need to:
- Order **3 PCBs**,
- Order some additional components.

He estimated this is roughly **1–2 hours of work** with Misha to finalize the BOM and place the orders. Val asked if Genadi could talk with Misha today. Genadi said he can't — Misha is tied up in a meeting until 2 PM (reviewing some report). Genadi committed to scheduling a Monday morning (May 25) session with Misha to walk through the BOM and component orders. Genadi has already prepared the BOM (Misha was supposed to, but Genadi did it himself and will help Misha through it).

### Schedule context — Flex POS release concern

Val provided context that the team had shipped today's Alpha release on schedule, and Beta is around July 1 (Val approximate, didn't have the exact date). Flex POS is releasing today. Mid-sentence, Val realized something looked off in the planning when he saw the Flex POS release land today, and decided to cut the meeting short to send a planning/scheduling email about it. He told Genadi he would send it within ~13 minutes.

The meeting ended with Genadi confirming and saying goodbye.

## Decisions Made

- **Georgia trip itinerary confirmed.** Genadi departs Tue May 26 morning, arrives Tue afternoon, returns Sat May 30 morning — leaving Friday May 29 as a full on-site day. (Decided by Genadi, acknowledged by Val.)
- **Sample assembly plan.** Of the 2 Flex Cash Dispenser samples received, one is assembled as Cash Dispenser, second as Recycler. (Reaffirmed jointly by Val and Genadi from a prior plan.)
- **BOM walkthrough scheduled for Monday May 25 AM** — Genadi will sit down with Misha to walk through the Prinzera BOM and finalize the component/PCB orders. (Decided by Genadi.)
- **Slim monitor sourcing — stay the course.** Genadi continues negotiating Chinese vendor down from $90 to ~$60–$70 for the monitor+controller kit. (Decided by Genadi; Val did not push back.)
- **Meeting ended early so Val could write a planning email.** Val identified an apparent gap in the Flex POS release planning and committed to following up via email within ~13 minutes.

## Undertakings (Historical Record — No Dispatch)

> Captured for the record only. Per Val's direction, no Teams messages, calendar reminders, or other follow-ups are dispatched from this note.

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi | Finish INBC port numbers so Andrei can use them next week to play/test | Before next week | Normal | Unblocks Andrei's test work on plastic parts |
| 2 | Genadi | Complete BOM and review harness for Slim product | Before/during Georgia trip | Normal | Outstanding piece of Slim build readiness |
| 3 | Genadi | Georgia trip (May 26–30): assemble 2 sample units (Cash Dispenser + Recycler), review Maple assembly, walk through parts-finding/shop organization with Elizabeth, address Chinese vendor / lens / office minor items | May 26–29, 2026 | High | Main reason for trip; multiple downstream products depend on getting these reviews and builds correct on site |
| 4 | Genadi (with Misha) | Monday-morning session to walk through Prinzera BOM and place orders for 3 PCBs plus the remaining components needed for 10-unit build | Mon May 25, 2026 AM | High | Blocks ability to assemble 10 Prinzera units |
| 5 | Genadi | Continue negotiating Chinese vendor on Slim monitor+controller kit; target $60–$70 vs current $90 quote | Ongoing | Normal | $20–$30 per-unit margin impact at product level |
| 6 | Val | Send planning email re: Flex POS release schedule concern | ~13 minutes after meeting end (May 22, 2026 ~3:50 PM ET) | High | Val noticed something looked mis-planned when reviewing release dates mid-meeting |
| 7 | Genadi (optional) | If time permits during Georgia trip, side-visit to Satellite Vegas warehouse to look at older Maple/Altera inventory | During trip window | Low | Val suggested; ~2hr each way, would consume a full day; tied to potential Texas shipment plan |

## Engineering Signals

No engineering signals detected. This was an operational/logistics alignment — assembly planning, sourcing negotiation, BOM scheduling, and trip coordination — with no ADR, requirement, capability, or solution-level architectural content.

## Open Questions

- **Flex POS release planning gap.** Val flagged that something looked off in the schedule but did not articulate the specific concern in-meeting; deferred to a follow-up email. Substance of that concern is not on record in this transcript.
- **Toronto vs Georgia parts-organization delta.** Filipp and Genadi both believe the Toronto shop makes parts easy to find, but neither knows what specifically Toronto did differently. To be discovered on-site during the trip.
- **Mid-June vs July molds.** Reconciliation between Misha's mid-June read and the original July guidance is implicit but not confirmed in writing.
- **Satellite Vegas → Texas.** Val voiced hope the older Maple/Altera inventory goes to Texas, but no decision or plan was discussed.

---
*Processed from Teams transcript on 2026-05-24.*
*Source meeting: General_alignment — May 22, 2026, 3:32 PM Eastern*
*Source file: General_alignment-May-22-2026.docx*
*Processed as historical record only — no dispatch of undertakings per Val's direction.*
