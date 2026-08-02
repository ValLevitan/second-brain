# Meeting Summary — Game_Development
**Date:** July 17, 2026, 2:00 PM – 2:58 PM Eastern
**Duration:** ~58 minutes
**Attendees:** Val Levitan, Michael Gottlieb, Juan Martinez, Efim Podvoiski
**Raw transcript:** [[Meeting_Transcript_Game_Design_Stages_Georgia_Data-July-17-2026]]

## Summary

The weekly Game_Development meeting covered two main topics: bad data in the Georgia Intralot report, and how the game concept and design stages should work.

**Georgia COAM data problems.** Juan pulled an Intralot report for July 6–16, filtered to the current software release (V43/V2). The numbers are clearly wrong. Games installed only 4–8 days ago show hundreds of "active days" (e.g., 419) and impossible totals — Rodeo Spins shows $17 million wagered on a handful of machines, and the games-played count (about 50,000) does not match the wagered amount. The group sees at least two separate problems. First, re-released games keep the same pay table ID because the math never changed, so Intralot appears to be co-mingling old (legacy) data with new data for titles that existed before (Bayou Riches, Crazy Cult, Queen of Luxor look "dirty"; brand-new titles look clean). Second, even combined legacy data can't explain some totals, so something else is wrong too — possibly Intralot's filters, or how they pull data. Juan raised whether GLC really relies 100% on SAS1 as its source of truth; Val said supposedly yes, but he's not certain. Juan suggested assigning a unique pay table ID (e.g., adding a suffix) to re-released themes in Georgia V3 to keep the data clean — a theory to test, not yet decided. Juan will check with Pavel and Irina about pay table IDs and go back to Intralot. Val reaffirmed that JVL relies only on its own QR code data, not this report; first QR scans are expected next week, and Juan will keep updating Georgia performance as they come in. Juan noted 12 machines are now installed in Georgia.

**Game concept and design stages.** Val walked Michael through how the stages should work now that comp art has moved out of the concept stage (a change Val directed two weeks ago, which Michael confirmed he is executing). The agreed model: the concept stage produces abstracts only — versioned drafts (v1, v2) that can evolve — and filters roughly 80% of bad ideas at minimum cost. The design stage is where Lena adds initial comp art (base game, free spins, bonus art), and the comp art deliverable — the first deliverable of the design stage — is the go/no-go gate: nothing else moves forward until Michael and Juan approve it. Michael and Juan are the final arbiters of go/no-go; Val gives input but is "an audience." Val also observed that the design stage really carries two purposes that shouldn't be mixed: (1) the go/no-go decision and (2) "art direction" — writing the spec/contract of deliverables for the graphic design team. Michael agreed with the framing. Michael confirmed the preliminary game list for the next Georgia release (new D27 Blaze cabinet) is already in Jira under IP 535; one theme on it (Dutch Mill) is a placeholder that probably won't survive. Roughly 80% of concepts are variants of proven games (a day or two per abstract); ~20% are original ideas that can take up to two weeks of elapsed time. Examples discussed: Twin Bison stays for Georgia; for South Dakota it becomes "Dakota Bison" using Lions Riches math (5x3), since 3x3 games perform worst there and Lions Riches is the top performer.

**Lena as a bottleneck.** Val questioned why Lena does all the comp art. Answer: she's the best fit — fast, knows slot machines and symbol hierarchy, and works in near-shorthand with Michael. Anastasiya did the Keno comp art (Black Hills Keno) adequately but much more slowly. No change was made.

**Closing remark from Val:** the per-task workflow should get simpler — most tasks should just be To Do / In Progress / Done; he's not sure the Review step works. A remark, not a decision.

## Decisions Made

- **Comp art stays out of the concept stage and is the first deliverable (and go/no-go gate) of the design stage** — keeps investment minimal before killing bad ideas; abstracts get version numbers and evolve. (Confirmed by Val and Michael; originally directed by Val two weeks ago)
- **JVL's own QR code data remains the only source of truth for Georgia game performance** — the Intralot report data is visibly corrupt. (Val, agreed by Juan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Juan | Check with Pavel and Irina how pay table IDs are created/retained across re-releases | TBD | Normal | Needed to confirm the data co-mingling theory |
| 2 | Juan | Go back to Intralot about the impossible report numbers (active days, wagered totals) | TBD | Normal | Report filters may not be working |
| 3 | Juan | Keep updating Georgia performance reporting as QR code scans come in | Ongoing, starting ~week of July 20 | Normal | First QR scans expected next week |

## Open Questions

- Does GLC really rely 100% on SAS1 as its source of truth? (Raised by Juan; Val unsure)
- What is the second data problem beyond pay-table co-mingling — Intralot filters, data pulling method, something else? (Raised by Val/Efim; unresolved)
- Should Georgia V3 re-released themes get new unique pay table IDs to keep data clean? (Juan's proposal — experiment to consider, not decided)

## Dispatch Log

---
*Processed from Teams transcript on July 17, 2026, 4:05 PM Eastern (scheduled watcher run)*
*Source meeting: Game_Development (recurring weekly)*
