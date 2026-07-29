# Meeting Summary — Call with Genadi Peari
**Date:** March 30, 2026, 9:51 PM Eastern
**Duration:** ~1 minute 24 seconds
**Attendees:** Val Levitan, Genadi Peari

## Summary

Val asked Genadi to comment on the communication link that Dima Pikulik built between two boards in the OMNI hardware stack. Val noted that Dima used a very fast microprocessor chip that should enable high communication speeds between the boards.

Genadi clarified that they **intentionally placed a USB Full Speed chip (12 Mbps)** instead of a USB High Speed chip (~480 Mbps) for the board-to-board communication. The reason: they did not need such extraordinary speed for the use case.

Val confirmed this was exactly the information he was looking for.

> **Note on transcript quality:** The Teams auto-transcription handled the Russian/English technical mix very poorly, producing heavily garbled text. The specific board/component names referenced by Val and Genadi could not be reliably reconstructed from the transcript. These terms will be clarified in the follow-up meeting with Genadi and Biratko scheduled for April 1, 2026.

## Decisions Made

No formal decisions recorded. This was an informational query — Val seeking clarification on why USB Full Speed was chosen over High Speed for OMNI board communication.

## Undertakings

No action items were assigned. Val asked a question, Genadi answered it.

## Engineering Signals

### Confirmed Signals

- **ADR: USB chip selection for board-to-board communication** — A USB Full Speed chip (12 Mbps) was intentionally chosen over a USB High Speed chip (~480 Mbps) because the extraordinary speed was not needed for the use case. This directly relates to the peripheral communication protocol and latency discussion from the Biratko OMNI Architecture meeting earlier the same day, where ~10ms protocol overhead was flagged as a concern for touchscreen responsiveness. The April 1 meeting should clarify whether this chip selection needs to be revisited for OMNI 2.

### Connection to Biratko Meeting (March 30, 2026)

The [OMNI Architecture meeting with Biratko](../OMNI%20Architecture%20Biratko-March-30-2026/Meeting_Notes_OMNI_Architecture_Biratko-March-30-2026.md) discussed the peripheral abstraction layer, standard protocols, and the question of whether ~10ms protocol overhead would be acceptable for latency-sensitive peripherals like touchscreens. The fact that a 12 Mbps chip was **intentionally selected** because higher speed wasn't needed raises a key question for OMNI 2: does the peripheral abstraction layer and protocol overhead change the speed requirements, making a faster chip necessary?

**Follow-up meeting:** April 1, 2026, 8:00 AM EST — Val, Genadi Peari, and Alexander Biratko will discuss this subject together.

## Open Questions

- What are the exact board/component names? (garbled in transcript — to be clarified April 1)
- Does OMNI 2's peripheral abstraction layer and protocol overhead change the speed requirements, making a High Speed chip (~480 Mbps) necessary?
- What would swapping to a High Speed chip involve (cost, board redesign, firmware)?

---
*Processed from Teams transcript on March 30, 2026*
*Source meeting: Call with Genadi Peari*
