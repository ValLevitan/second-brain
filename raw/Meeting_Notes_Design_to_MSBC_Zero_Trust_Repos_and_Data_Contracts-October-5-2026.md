# Meeting Summary — Design-to-MSBC_Organization_repositories_
**Date:** October 5, 2026, 1:19 PM – 1:53 PM Eastern
**Duration:** About 34 minutes
**Attendees:** Val Levitan, Genadi Peari
**Raw transcript:** [[Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026]]

Teams meeting organized by Val. Starts in English, then Russian from about 21:00. From about 08:00 to 21:00 the transcript is badly garbled (Russian speech transcribed as English), so that part is not summarized. Continues the flat-BOM discussion: [[Meeting_Notes_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026]], [[Meeting_Notes_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026]]. Follow-up the same afternoon: [[Meeting_Notes_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026]].

Initiative: [[GitHub to MSBC BOM]] (hub: [[GitHub_to_MSBC_BOM_Hub]]).

## Summary

**The developer model.** Val explained how code repos work, so Genadi can see the same model for hardware. Each repo equals one Jira project. Repos have "zero trust": no repo refers to or trusts another. Each repo holds code, prose, ADRs and, most important, a **data contract** — an .md file that describes only what the repo can output. From this, Claude Code can put the whole product together and run end-to-end tests.

**Applied to hardware.** Val said this is proven for development and he is about 70% sure it will work for electromechanical design. With prose, zero trust and data contracts, Claude should be able to build the bill of materials. Manual BOM work would go away; substitutions and versioning would be automatic. A supplier substitution would only need a new revision in GitHub.

**Source of truth.** Genadi said that once a BOM is pushed to MSBC, it should stay there as the reference for production, and asked why it should be regenerated each time. Val said the source of truth is always GitHub, and it is a **flat list of parts, not a BOM**. The BOM is generated from GitHub when needed. His comparison: GitHub Actions builds the code into an ISO, the ISO lives in Azure until something changes, and where it lives (Azure or MSBC) does not matter. Genadi asked if the build is the same every time. Val said yes, because builds are signed with checksums.

**Genadi's doubts.** Genadi said the difference between jurisdictions in production may be three harnesses that change in four minutes. Val said there are many links (money transfer, knowledge base), and the code side has 12 people while Genadi works alone. Genadi said he feels the plan is a little detached from reality: Mikhail Perelman still has no report to work with. Val said Mikhail's problem is real but separate and must be solved in parallel. Example from today: a monitor count showed 57 by hand vs 65 in the system, and 65 was right. Val is setting up an AI COO persona that will push weekly spot checks. Val said Mikhail is taking a position ("give me a report first").

**Next step.** Genadi asked to break the work into simpler steps. Val agreed Genadi cannot do this alone. Val said he will call Nathan Carver right after this meeting, explain the concept, and ask him to implement it on the **Flex Pay Slim** and demonstrate it; then Genadi can review it.

**Genadi's condition.** Genadi asked not to lose what was agreed earlier: first build the **flat list of parts in GitHub correctly** — with numbering that continues JVL's current system, clear rules, and defined places to pull revisions and drawings from ("the bricks"). Only then build upward. After that it can be used for orders. Val said this is simple and he sees no problem.

Val closed by saying this technology is about two years old at most and 90% of companies do not even talk about it yet.

## Decisions Made

- **Nathan Carver will implement the concept and demonstrate it on the Flex Pay Slim.** — Genadi cannot build it alone; Nathan can pick it up easily. (Decided by Val)
- **GitHub stays the source of truth, as a flat list of parts; the BOM is generated from it.** — Same as code builds; where the output lives does not matter. Genadi said "OK" but still has doubts. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Call Nathan Carver, explain the concept, ask him to implement and demo it on the Flex Pay Slim | 2026-10-05 | High | Done the same day — see the Nathan call |
| 2 | Nathan Carver | Build the concept and demo it on the Flex Pay Slim for Genadi to review | TBD | High | Assigned through Val |
| 3 | [Needs Val's confirmation] | Build the GitHub flat list of parts first: numbering that continues the current system, rules, sources for revisions and drawings | TBD | High | Genadi's condition; Val agreed; owner not named |

## Open Questions

- Genadi: how is the multi-level production BOM in MSBC formed from a flat GitHub list, and why not keep the pushed BOM in MSBC as the reference? (Raised by Genadi; Val answered in principle, Genadi not fully convinced)
- Genadi: Mikhail Perelman still has no report or BOM to work from. (Raised by Genadi; Val says it is a parallel issue)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-05 3:05 PM ET*
*Source meeting: Design-to-MSBC_Organization_repositories_*
