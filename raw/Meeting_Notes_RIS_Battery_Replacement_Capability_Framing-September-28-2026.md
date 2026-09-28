# Meeting Summary — RIS Rework MVP1 – Use Cases, Capabilities & Requirements Review
**Date:** September 28, 2026, 10:33 AM – 10:38 AM Eastern
**Duration:** about 5 minutes
**Attendees:** Val Levitan, Felipe Miranda Giorgi, Pavel Frolov, Irina Shishko, Sebastian Cortes
**Raw transcript:** [[Meeting_Transcript_RIS_Battery_Replacement_Capability_Framing-September-28-2026]]

## Summary

**Review method.** Val asked Felipe to go through the review one capability at a time: first the capability, then its requirements, questions from everyone, then move on. Keep a tight pace.

**Use case 1 — battery replacement.** Felipe started reading use case 1, "battery replacement without critical error". A Flex machine detects a low battery, saves meters, game settings, RIS and state, shows "battery low, safe to replace" and keeps playing. Later, when the battery dies, the machine powers off and shows "battery dead, replace battery", but the recovery data is already saved.

**Val's feedback: do not engineer the product.** Val said this is too detailed. The capability should be short and high level, for example **"Replace battery without factory reset."** Pavel agreed. Requirements under the capability explain how it is carried out. Val said Felipe is telling the engineers how to build it (data retention, clock recovery, warnings). As product owner he should not do that. He should state what he wants, then negotiate with the engineers and ask questions such as "Will you retain meters? Will the clock stay?" — and let the engineers write the how.

**Next step.** Felipe asked for time to rework the document. Val gave half an hour instead of wasting the meeting. Val said he will put this recording into the meeting notes for Felipe to use, and assumed Felipe will refine it with Claude. Val will shorten this meeting to 15 minutes and book another one.

## Decisions Made

- **Capabilities are written as short, high-level statements (e.g. "Replace battery without factory reset"); the product owner does not specify the engineering "how".** — Val said describing implementation details is the engineers' job; requirements explain how the capability is carried out, agreed through negotiation with engineers. (Decided by Val; Pavel agreed)
- **The review was paused so Felipe can rework the document; a new meeting will follow.** — More efficient than continuing now. (Decided by Val, agreed by Felipe)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Felipe Miranda Giorgi | Rework the RIS use-case document: high-level capabilities, requirements under each, no engineering detail | Sep 28, 2026 (about half an hour) | High | Val offered half an hour; Felipe suggested using Claude |
| 2 | Val Levitan | Put this recording into the meeting notes for Felipe to use | TBD | Normal | Done by this capture |
| 3 | Val Levitan | Shorten this meeting to 15 minutes and book another review meeting | Sep 28, 2026 | Normal | |

## Open Questions

None.

## Dispatch Log

---
*Processed from Teams transcript on September 28, 2026, 12:10 PM Eastern*
*Source meeting: RIS Rework MVP1 – Use Cases, Capabilities & Requirements Review*
