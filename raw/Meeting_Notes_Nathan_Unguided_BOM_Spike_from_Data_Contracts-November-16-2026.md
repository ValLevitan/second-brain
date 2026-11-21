# Meeting Summary — AI-logic for assembling BOM
**Date:** November 16, 2026, 4:40 PM – 5:02 PM Eastern
**Duration:** ~22 minutes
**Attendees:** Val Levitan, Nathan Carver
**Language:** English
**Raw transcript:** [[Meeting_Transcript_Nathan_Unguided_BOM_Spike_from_Data_Contracts-November-16-2026]]

## Summary

**The question.** Val had just spoken to Genadi. He asked Nathan whether there is logic to assemble a bill of material from data sheets and data contracts. How does one bracket "know" it fits another bracket, with a PC board on top, without being told?

**Nathan's first answer.** Nathan has logic. He is working on the BOM structure in GitHub, then running it on the contracts; syncing to MSBC is already possible. Contracts must define interfaces, for example screw size and thread, and the board's mounting standard. His plan was a programmatic function that matches contracts, with the agent used only for search and edge cases.

**Val's vision.** Val wants no template and no guidance from Genadi or Nathan. The only input is a short verbal description of the product (for example, "an ATM machine"). A group of agents reads the data contracts and assembles flat parts into subassemblies: a spec writer, an auditor and an assembler, with a learning loop. When the build fails, the agents must point to the cause: a missing or wrong data sheet, and then chase the supplier. The data sheet is the entry point and the source of truth; the data contract is the exit. Pretend the product never existed in MSBC. Goal: substitute parts and work with suppliers in minutes, not with Genadi in 3D design. Val said developers no longer guide agents, and wants to show Genadi it works.

**Agreement.** Nathan said this answered a question he and Genadi had been going back and forth on. He had already had an agent write contracts from design materials with no help. He expects the agent to ask clarifying questions and maybe offer alternatives; a human then refines.

**Spike.** Val wants a spike on any easy subassembly (power supply was his example). Nathan aims for Wednesday, or Thursday at the latest, and will send a note or book a meeting when ready.

## Decisions Made

- **BOM assembly is unguided: the agents get only a general product description and the data contracts; no template or assembly logic from Genadi or Nathan.** — Val wants free agents that expose missing data. (Val; Nathan agreed)
- Considered and superseded: a programmatic function that matches contracts, with the agent used only for search — replaced by the unguided agent approach above.
- **When a build fails, the answer must trace to the data sheet (right or wrong data sheet); the data sheet is the source of truth.** (Val; Nathan agreed)
- **Start with a spike on a simple subassembly.** (Val; Nathan agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver | Spike a workflow: ask the agents for a simple build from a description only and let them assemble a subassembly from data contracts | Nov 18, 2026 (Nov 19 at latest) | High | First view for Val |
| 2 | Nathan Carver | Send Val a note and book a meeting when the spike is ready | Nov 18–19, 2026 | Normal | Val does not want a meeting before it is ready |

## Open Questions

None.

## Dispatch Log

---
*Processed from Teams transcript on November 18, 2026 (scheduled meeting-watcher)*
*Source meeting: AI-logic for assembling BOM*
