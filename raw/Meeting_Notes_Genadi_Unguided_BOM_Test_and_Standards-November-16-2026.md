# Meeting Summary — Alignment call
**Date:** November 16, 2026, 4:05 PM – 4:33 PM Eastern
**Duration:** ~28 minutes
**Attendees:** Val Levitan, Genadi Peari
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Genadi_Unguided_BOM_Test_and_Standards-November-16-2026]]

## Summary

**Why Val called.** Val's main worry is procurement and the BOM integration: can a bill of material be built from data contracts and put into Microsoft Business Central? He cannot tell, from Nathan or from Genadi, whether this works.

**Procurement vs BOM.** Genadi said these are two different things. Procurement does not care how the BOM is made, only that it is correct and stable. He urged Val to run the AI-COO at full power now, even if not complete, so it can watch inventory and catch errors.

**Split of work.** Val agreed but said he already has that in hand. He split the work in two: Val owns the administrative side of procurement and helping the AI-COO; Genadi owns specs and data sheets so the BOM is correct. Example of the admin problem: purchase orders (for example a bill acceptor) are issued without a G/L account, so the cost goes to expenses instead of inventory. Then cost of goods is wrong and units are not counted. Val said Daniel, Michael and Lev set this up badly, and he is now fixing it himself.

**AI executives.** Val said an AI-CFO also exists. AI executives need narrow guardrails and exact references; a wide persona writes its own theories and Val cannot oversee it. Start narrow and widen slowly. Fixing one or two errors a week adds up over a year.

**Standards.** Val writes standards into the standards repo in the new GitHub space. The AI-COO, AI-HR and the project manager agent all read it. He asked Genadi to put any standard he has there, even two sentences, written by Claude in markdown.

**The BOM test.** Genadi said his agent sorts data contracts by category and adds the documentation; about 50% of parts are in the hardware repo, in category folders (folders, not repos, as Andrei proposed). Written standards for the folder layout and part numbers exist and are in the standards repo. He tells the MSBC agent to export a category's part numbers to GitHub per the standard, and it asks for missing data. Val described the test he wants: export everything from MSBC to GitHub, polish it to standard, remove the old BOM from MSBC as if it never existed, ask the AI to build the BOM from the data contracts, then compare the two BOMs. Genadi said part numbers work both ways, but on the BOM he does not know: he handed everything to Nathan, who said he would check it. Val's point: do not tell the AI how to build the BOM; ask it to build one from the data contracts. Genadi is skeptical and does not see what logic the AI would use, but called it a great idea with many nuances. Val said if he is wrong, only time is lost.

## Decisions Made

- **Work is split: Val owns procurement administration and the AI-COO; Genadi owns specs and data sheets for a correct BOM.** — Val said he needs no help on the AI-COO side. (Val; Genadi agreed)
- **Test whether AI can build a BOM from data contracts without being told how, then compare it with the MSBC BOM.** — Val wants to prove the theory outside software development. (Val; Genadi agreed but is skeptical)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Send Val the link to the repo where everything is stored; send it to the AI-COO too, with a copy to "Yuro" | TBD | Normal | Name "Yuro" unclear in transcript; Genadi: it is one repository |
| 2 | Genadi Peari | Put any standard he has (even two sentences) into the GitHub standards repo, written by Claude in markdown | TBD | Normal | Val's request |
| 3 | Nathan Carver | Check BOM creation from the data Genadi prepared | TBD | High | Per Genadi: "the ball is with Nathan"; Nathan not present |
| 4 | Val Levitan | Fix the procurement admin gaps (e.g. purchase orders without a G/L account) | TBD | Normal | Val took this on himself |

## Open Questions

- Can AI build a BOM from data contracts with no guidance on the logic? (Val's theory; Genadi skeptical)
- Genadi wanted to go over several small items; Val postponed them.

## Dispatch Log

---
*Processed from Teams transcript on November 18, 2026 (scheduled meeting-watcher)*
*Source meeting: Alignment call*
