---
type: decision
title: After Nathan's first unguided spike assembled a power-supply sub-assembly through questions, the next spike is a self-learning supplier loop — the agent finds the part's existing supplier, asks it for the missing data sheet or details and chases it, updates the data contracts and the flat list, and tries to assemble again until it needs no human; all earlier answers and hints are erased; Genadi is asked only when a supplier is unknown, and only once; some part data is left missing on purpose; review Friday Nov 20 at 4 PM (Val, with Nathan Carver and Genadi Peari, Nov 18 2026)
date: 2026-11-18
aliases: [supplier data loop, supplier data-chase loop, BOM agents supplier data loop, AI-logic for assembling BOM continued, self-learning data contracts, data contracts have to be learning, self-defined data contract, chase the supplier, Mr. Supplier I am one of your clients, erase all the answers, Genadi is the last person, leave some data missing, don't hydrate all of it, 120 volts 60 hertz, three scoped agents, spec writer assembler auditor, simulated non-expert user, Nov 18 BOM spike result, Friday Nov 20 4 PM BOM review]
source-count: 2
status: active
open-commitments: 4
open-questions: 0
---

# The next BOM spike is a self-learning supplier loop (Nov 18 2026)

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-11-18-nathan-bom-agents-supplier-data-loop.md|Nov 18 2026, 4:36 PM call "AI-logic for assembling BOM — continued"]] (English, about 19 minutes) with [[wiki/people/nathan-carver.md|Nathan Carver]] and [[wiki/people/genadi-peari.md|Genadi Peari]] [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]] [[raw/Meeting_Notes_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]]. Nathan agreed. It follows the spike set two days earlier — [[wiki/decisions/2026-11-16-the-agents-build-the-bom-unguided-from-a-product-description-and-the-data-contracts-the-data-sheet-is-the-source-of-truth-and-nathan-spikes-a-simple-sub-assembly.md]] (Nov-18 update).

## What the first spike did (Nathan)

- **The agents.** He "ran at several simulations", with one agent playing "a non-expert asking to build something", and "that question-answer routine between the assembler agent and the user agent". There were "3 scoped agents… an auditor and an assembler and a spec writer" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]]. Val described the user agent as one that "emulates, I don't know, Genadi" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].
- **No technical direction.** "don't give it any technical direction on what to build, but tell it what interfaces you need for the sub-assembly"; Val: the interfaces "were taken from the data contracts" — Nathan: "Correct" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].
- **The prompt, as Val read it back.** The design purpose; "where the data contracts are"; "build a sub-assembly for me, which is a power supply"; "a flat list of parts. You didn't tell the agent that this part goes here". Nathan: "That's right." The assembler got "the limited information" — all the structures and which folders to look in — and "has access to all the files" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].
- **What came back.** The assembler asked questions; "we simulated answers for this". Asked by Genadi how it knew the power needed, Nathan: "the closest thing we got to that power question was… 120 volts, 60 hertz". It "identified contracts that it needs that are still missing"; the auditor agents "came back… with findings"; "it was able to iterate with the auditors" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].
- **Clean runs.** "this runs in a sandbox, so every run is blank. It doesn't have any… Persisting decisions or any… persistent prompts" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].

## How it was received

- **Val:** "I actually read every single sentence… I'm ecstatic about… the result. Am I being too optimistic?" Nathan: "No… it was asking good questions." Val: the questions came "because there wasn't enough information to begin with… if we had a better information, there would be no questions. It would just go out and build" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].
- **Genadi:** "more than half of the answers, they are in the product requirements"; at the end, "No, it's incredible" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]]. On Nov 16 he had called himself skeptical of an unguided BOM — [[wiki/decisions/2026-11-16-the-agents-build-the-bom-unguided-from-a-product-description-and-the-data-contracts-the-data-sheet-is-the-source-of-truth-and-nathan-spikes-a-simple-sub-assembly.md]].
- **Val's aim, restated.** A "clean, pure… flat library of data sheets, either from JVL as the source or from whoever a third party supplier is", with everything laid flat "Without a hint of where everything goes"; when a person adds an answer, "Genadi simply adds to the description. The description is saved once forever". And: "We could actually back into requirements and acceptance criteria from here." Nathan: "Yes, yeah, I think so" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].

## The ruling — the supplier loop

- **Not to Genadi.** "the assembler doesn't go to Genadi… Genadi is the last person that I want to take the attention from" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].
- **The loop.** "Who is the supplier?… What's the contact information for the supplier?… What are you looking from the supplier? Send a message to the supplier. Chase the supplier. Get the information, go back. Assemble. Identify what else is missing"; then "update flat list, update data contracts" and go round again [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].
- **Data contracts learn.** "Data contracts have to be learning… The whole point about data contract is not to say what the data contract is. It needs to be self-defined"; "a looping learning mechanism" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].
- **Genadi once.** "if supplier is not known, or certain information about a supplier is not known, get it from Genadi. But it will only take once" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].
- **No human help, no old hints.** The spike runs "until we totally, finally, without any sort of human involvement, assemble the sub-assembly"; "erase all the answers that you gave it… If you gave any hints, erase it". The only new input is "the information… about the supplier" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].
- **The message.** "Mr. Supplier, I am one of your clients… I'm missing data. I don't have this data sheet… Can you please supply it as soon as possible?" Then "inhale the data, update the data contract… Can you assemble it now? No. What are you missing now?… Let's go get that" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].
- **Same supplier, not a purchase.** Genadi: a generic part "goes by description" and can come from any supplier; a dedicated part number can also be bought from any supplier of that brand. Val: "we're not trying to purchase… go to the exact supplier that we had already chosen that you built into your bill of material" and ask for what is missing — data sheets, "opening holes", "fastening parameters", "connectors, whatever we're missing" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].
- **Missing data on purpose.** Val to Genadi: "make sure that you have supplier information in the file… Not the data, don't give any data… I actually like the fact that some data is missing." Nathan: "we won't hydrate all of it then… so we can… test with… building the agent that's going to go get that information" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].

In one line: **the agent's only way to new knowledge is the part's own supplier; it asks, chases, updates the data contract, and tries again until the sub-assembly is built with no person in the loop.**

## Later, not now

- Val: "when we have a solid data contract and it's fully assembled… let's go out in the market and look for a new supplier… here's the data contract. This is the data sheet. Who can supply this part for me?" — a loop that also verifies fit, checks the price and switches suppliers; sourcing data "cannot be put into the flat list without the supplier information" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]]. A future direction, not part of the next spike.
- Val had already floated "a fourth agent" that says "I couldn't find this data sheet, but I'm buying it from company ABC in China. Ask them"; Nathan: "it could automate… that message" [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]].

## How it sits against earlier rulings

- **Nov 16 — evolution.** Nov 16 ruled unguided assembly and set the spike; it is now done, and its "chase the supplier" idea becomes the next spike — [[wiki/decisions/2026-11-16-the-agents-build-the-bom-unguided-from-a-product-description-and-the-data-contracts-the-data-sheet-is-the-source-of-truth-and-nathan-spikes-a-simple-sub-assembly.md]] (Nov-18 update).
- **The data sheet is the truth** (Nov 16) carries over: the loop exists to get the right data sheet from the supplier.
- **The power supply.** The Oct-21 first spike was also a power-supply BOM — [[wiki/decisions/2026-10-21-hardware-parts-go-into-one-repository-with-subfolders-and-the-first-spike-builds-the-power-supply-bom-automatically.md]].

## Open commitments

- [ ] [[wiki/people/nathan-carver.md|Nathan Carver]] — run the next 2–3 day spike: the supplier data-chase loop that updates the data contracts and re-assembles the power-supply sub-assembly with no human answers; he sets the focus from this transcript — due Fri Nov 20 2026, 4 PM review — [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]] [[raw/Meeting_Notes_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — put supplier information (not the data) in the parts files — due before the Nov 20 review (the notes; not stated on tape) — [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]] [[raw/Meeting_Notes_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — book the Friday 4 PM meeting ("I will book the meeting") — due Nov 18 2026 — [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]] [[raw/Meeting_Notes_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — send the meeting transcript to Nathan and Genadi — due Nov 18 2026 — [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]] [[raw/Meeting_Notes_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]]

**§15.8:** clear. **§15 #9:** clear.

## Sources

- [[raw/Meeting_Transcript_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]]
- [[raw/Meeting_Notes_Nathan_BOM_Agents_Supplier_Data_Loop-November-18-2026.md]]
