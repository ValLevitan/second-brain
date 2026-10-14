# Meeting Summary — Call with Nathan Carver (ad-hoc Teams call)
**Date:** October 5, 2026, 1:58 PM – 2:33 PM Eastern
**Duration:** About 35 minutes (two short breaks: Val took other calls, one with his lawyer)
**Attendees:** Val Levitan, Nathan Carver
**Raw transcript:** [[Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026]]

Ad-hoc Teams call started by Val, no calendar invite. Held right after the Genadi meeting: [[Meeting_Notes_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026]]. Earlier context: [[Meeting_Notes_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026]].

Initiative: [[GitHub to MSBC BOM]] (hub: [[GitHub_to_MSBC_BOM_Hub]]).

## Summary

**The idea.** Val described how the administrative side of the electromechanical BOM should work. It mirrors the development pipeline: one Jira project = one repo; repos have zero trust; each repo holds prose, ADRs and data contracts. For hardware, start from a **flat list of all parts in GitHub**. A data contract describes what a sub-assembly does, from the output side only. Claude should then assemble a BOM for a full machine or a sub-assembly, on the fly or through GitHub Actions. Val compared it to the ISO image built by a GitHub Action and posted to Azure: for hardware, that end product is the final BOM in MSBC.

**Nathan's view.** Nathan agreed. MSBC has a fixed BOM structure, so once the structure and input are known, the BOM can be built by a program, maybe without an agent. The GitHub side needs an organized structure of plain-text data files that people edit — "source code" that compiles into a BC BOM instead of an application.

**Data contracts as the logic.** Val said the assembly should come from data contracts: power comes from a power supply, which connects to the PC board with a harness; the monitor connects over HDMI; screw threads come from the supplier spec. Nathan said the terms differ between Genadi's world, GitHub and BC, but it is the same thing: how components interface.

**Hand the logic to AI.** Val wants a flat, linear source of truth. Swap one part for another with a compatible data contract and it works. If the contract changes, the system should say what else must change (screws, harness). Genadi spends about 30% of his time on design and 70% on assembly manuals, BOMs, descriptions and file names. Naming and filing conventions should let Claude do that work. Supplier finances stay on the administrative side (MSBC).

**Projects and repos.** Candidate projects: peripheral devices, monitors, PC boards, sheet metal, plastics, harnesses. Val thinks Genadi's part-number categories may already be the projects. Nathan suggested a monorepo to keep the repo count down. Val said no: Jira needs one project per repo, and a project is described by its capabilities. Val sees no problem with many repos; Nathan agreed agents will know where to go. Nathan added: each repo should have a project-level spec plus per-component interface detail, and should tell the agent how best to search its contents (for example, displays by size, connector, resolution). If a wrong machine is built, go back to the data contract and the spec.

**The spike.** Take the **Flex Pay Slim** BOM from MSBC, flatten it, put it in GitHub, then work backward: break it into projects, create repos, write data contracts, and let agents build ("compile") the BOM. Push the result into MSBC and compare it with the original. Val expects agents to find problems the team does not see today. Do not be bound by what exists in the current hardware repo — this is a freehand spike. Nathan proposed spiking a second product independently afterwards; Val suggested **Flexport** (fewer items, but still plastics, sheet metal, screen, touch screen, hardware, connectors).

**Jira home.** Nathan proposed his existing "hardware sync" item **DTP-1083**, under **IP-964** (modernization and improvements, value stream DevOps tools and processes). Val agreed, and said **IP-965** (Business Central application) is also fine.

Val will send Nathan this transcript. Nathan is on vacation next week and will try to hand over some of this before he leaves.

## Decisions Made

- **Spike on the Flex Pay Slim: reverse the existing MSBC BOM into a GitHub flat list, rebuild the BOM through projects, repos, data contracts and agents, then compare with the original.** — Proves the GitHub-to-MSBC model. (Decided by Val; Nathan agreed)
- **One Jira project = one repo; no monorepo.** — Projects are described by capabilities in Jira. (Decided by Val)
- **Freehand spike, not bound by the existing hardware repo.** — The current structure may not give the right picture. (Decided by Val)
- **A second product, Flexport, is spiked independently afterwards and compared.** (Proposed by Nathan; product chosen by Val)
- **Work lives under DTP-1083 (IP-964); IP-965 is also acceptable.** (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Send Nathan the call transcript | 2026-10-05 | Normal | An attachment was posted in the chat at 2:43 PM ET |
| 2 | Nathan Carver | Break the work into a project and capabilities in Jira under DTP-1083 (or IP-965) and start implementing | TBD | High | |
| 3 | Nathan Carver | Run the Flex Pay Slim spike: pull and flatten the MSBC BOM, set up projects, repos and data contracts, build the BOM with agents, push to MSBC, compare | TBD | High | |
| 4 | Nathan Carver | Spike Flexport independently and compare with the Flex Pay Slim result | TBD | Normal | After the first spike |
| 5 | Nathan Carver | Hand over first results before his vacation | 2026-10-09 | Normal | Out next week (Oct 12–16 per his Oct 1 chat) |

## Open Questions

- Which product categories become projects/repos? Val asked Nathan to help think it through; not settled. (Raised by Val)
- Is an agent needed to build the BC BOM, or can a program do it once the structure is known? (Raised by Nathan)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-05 3:05 PM ET*
*Source meeting: Call with Nathan Carver*
