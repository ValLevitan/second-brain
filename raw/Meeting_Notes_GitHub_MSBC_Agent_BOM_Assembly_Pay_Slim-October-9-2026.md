# Meeting Summary — GitHub-MSBC
**Date:** October 9, 2026, 11:37 AM – 12:33 PM Eastern
**Duration:** ~55 minutes
**Attendees:** Nathan Carver, Genadi Peari, Val Levitan
**Raw transcript:** [[Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026]]

## Summary

Val spoke very little (his audio was choppy). He sent his input as Teams chat messages during the call. The chat text is not in the transcript; only what Nathan and Genadi said about it is captured here.

**Nathan's experiment (PR).** Nathan used the MSBC dev instance. A script pulled an existing BOM out of MSBC and broke it into parts inside a repository. For now the future repos are only folders; later each would be a separate repo with its own tags and versions. Each part has an overview, a parts CSV, and a structured contract that defines its interface: what it provides, what it accepts, and notes for the agent. A new agent then read the standard, picked parts by contract, and a script built a new BOM in MSBC. The result came close to the original, but some "outlier parts" still need to be settled. The process also writes a trace report: reasoning, what it found, what it did not find, rejected parts.

**Genadi's view on value.** Building a BOM is not the time-consuming part. Design takes months; the BOM is built once and then maintained. An agent BOM will never be 100% right (maybe 90%), so a solid reference adjusted by hand must stay. BOM levels also follow how production likes to build sub-assemblies, not only the contracts. Some levels exist only for procurement convenience (for example assembly plus PC board, so a revision change spreads to all products).

**Downstream automation.** Genadi: once a solid BOM exists, procurement can be fully automated. Example: order 100 products, a part has two instances, so send an RFQ for 200; a daily report of need vs stock, what to order, lead time and arrival date. Genadi said the five actions Val texted are very important, cause many mistakes and effort, and could save the company a lot; he sees no reason they cannot be done "tomorrow". Nathan agreed they are reasonable and work from an existing BOM, current BC inventory and BC supplier list.

**Verification.** Nathan: trust and verify. The agent picks parts; a script checks that interfaces line up and sends problems back to the agent in a loop. An audit agent, even on a different model, could also review. The script check is the most consistent. A human review and approval stage comes at the end. Humans also review and update the agent instructions. Confidence grows over time, for example after about 30 BOMs in a row with no corrections.

**Source of truth.** Reading Val's chat, Nathan said Val does not want MSBC as the starting point; GitHub is the engineering source of truth and pushes into MSBC. Genadi: GitHub holds the engineering sources, linked by part number and revision; GitHub produces the BOM, it is exported to MSBC, and each change exports a new revision. Nathan had started a concept of the highest assembly point (the product) from Val's email of the day before. Scripts do not need an agent to validate or push to MSBC; the agent only speeds up decisions.

**Variants.** Genadi: near-identical BOMs are often needed for different jurisdictions or customers, sometimes one item different (for example a cable, a printer model, a bill acceptor). This is a new top part number and a new BOM in MSBC, so production sees the difference. The change may come from sales or production, not engineering. Final products have about 5 modules (money devices kit, printer, and others) and 6 to 10 final part numbers. Nathan: in the future a customer change could be fed to the agent to create the new BOM automatically. Genadi: possible, but a human touch-up and verification is still needed.

**Next step.** Genadi asked Nathan to take a flat parts list for one product and let the agent build the BOM without seeing the existing structure. Product: the Flex Pay Slim for Georgia, which deploys soon and needs quotations and parts. Nathan is out next week; Val wants it by end of month.

## Decisions Made

- **GitHub, not MSBC, is the engineering source of truth and the starting point; BOMs are pushed from GitHub into MSBC.** — Val wants it this way. (Decided by Val Levitan, in chat, as read by Nathan)
- **First real test: Flex Pay Slim for Georgia, starting from Genadi's GitHub source as a flat parts list; the agent builds the BOM without the existing structure.** — it deploys soon and needs quotes and parts. (Proposed by Genadi Peari, agreed by Nathan Carver)
- **Agent output gets script validation of interfaces and a final human review and approval stage.** — an agent BOM will never be 100% correct. (Nathan Carver, Genadi Peari)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver | Build the Flex Pay Slim (Georgia) BOM from Genadi's GitHub source with the agent + script workflow and push to MSBC; keep Val's chat requirements for the AI-CO in mind | October 31, 2026 | High | Val wants end of month; Nathan is out next week, starts week of October 19 |
| 2 | Genadi Peari | Send Nathan the GitHub link for the Pay Slim product source | [Needs Val's confirmation] | High | Said "I'll send the link" |
| 3 | Nathan Carver | Find a file format a human can review efficiently for BOM approval (for example CSV for Excel) | [Needs Val's confirmation] | Normal | Genadi asked how the BOM is visualized for approval |
| 4 | Nathan Carver | Set up time with Genadi on repository reshuffling, as needed | [Needs Val's confirmation] | Normal | Genadi offered to reshuffle repos |

## Open Questions

- How to verify agent output without taking more time than the manual way? (Nathan Carver)
- How do humans review near-identical BOM variants that differ by one part? (Genadi Peari, Nathan Carver)
- How should multi-level BOMs reflect production's sub-assembly logic? (Genadi Peari)
- The text of Val's five chat actions and AI-CO requirements is not in the transcript.

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-14*
*Source meeting: GitHub-MSBC*
