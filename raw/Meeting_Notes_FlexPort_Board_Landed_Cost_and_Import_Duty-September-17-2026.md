# Meeting Summary — Review Flex-Pay-Slim design and construction - September 17-2026

**Date:** September 17, 2026, 1:54 PM - 1:57 PM Eastern
**Duration:** approximately 3 minutes
**Segment:** Segment 2 of 2
**Attendees heard:** Val Levitan, Genadi Peari
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026]]
**Source meeting:** Review Flex-Pay-Slim design and construction - September 17-2026 — Microsoft Teams

## Summary

A short exchange about what a part really costs once it lands, and how that should be recorded.

**The gap.** Genadi said he checked the price of the electronic board for FlexPort with Alekseev at quantity. The component price is about $46. But when they actually order it, it does not cost $46 — it costs about $60, because of taxes and duties. Val agreed they cannot keep working the other way.

**How to record it.** Genadi's point was that the component price is the bill-of-material cost, and the rest has to be handled in Business Central. Val said they have to set up a tax category for import duties so the difference is captured.

**Why it matters.** Genadi said that when Val asks him what a machine costs, he is honestly confused, because he looks at one figure and then at another with freight added. He sees it on motherboards, all the electronics, and monitors. He said that while they work with the current suppliers, those suppliers repack and use tricks, and the effect is large — he wants Val not to be misled by their prices, because pricing depends on it, and then there is the airport cost on top.

**Val's rule of thumb.** Val said twice that he adds 30% to whatever bill-of-material number Genadi gives him, because the number he asks for is before freight and everything else. He then said that in reality he should be adding more — about 35%.

Genadi said the size of it is not a happy thing.

## Decisions Made

- **A tax category for import duties is to be set up in Business Central**, so landed cost is captured rather than only the bill-of-material component price. (Val)
- **Bill-of-material figures quoted by Genadi are understood to exclude freight and duty.** Val marks them up 30% today and stated the truer figure is about 35%. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | [Needs Val's confirmation] | Set up an import-duties tax category in Business Central | TBD | Normal | Val said "we must" set it up; no person was named on the call |

## Open Questions

- Whether Val's markup on bill-of-material quotes moves from 30% to the 35% he said is closer to the truth. He raised it but no change was agreed.

## Dispatch Log

---
*Processed from Teams transcript on September 17, 2026, 4:05 PM Eastern*
*Source meeting: Review Flex-Pay-Slim design and construction - September 17-2026*
