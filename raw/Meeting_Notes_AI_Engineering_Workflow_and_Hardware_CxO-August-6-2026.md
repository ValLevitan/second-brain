# Meeting Summary — General alignment (Val & Genadi Peari)
**Date:** August 6, 2026, 4:32–5:47 PM (Eastern)
**Duration:** ~75 minutes
**Attendees:** Val Levitan, Genadi Peari
**Raw transcript:** [[Meeting_Transcript_AI_Engineering_Workflow_and_Hardware_CxO-August-6-2026]]

## Summary

This was a 1:1 check-in (in Russian) that turned into Val laying out his AI-driven way of working and asking Genadi to adopt it for the hardware side.

**Genadi's current work.** Genadi said the builds are almost finished with only small fixes left, and the units are close to production-ready. He works mainly with Andrei and Elizabeth. He uses Claude for analysis (for example, choosing a module/modem in minutes instead of the ~2 weeks it would have taken by hand), not for compilation. He said his SolidWorks PDM already manages files well — he loses no time on file organization and has never lost a file or a revision. He asked whether he needs a license or a daily-use file server.

**GitHub is not a file store.** Val corrected a recurring misunderstanding: GitHub is for artifacts and version control, not a storage warehouse. Engineering artifacts (drawings, specs, documents, code) belong in GitHub, organized by project — one project equals one repository. Games, code, drawings, illustrations and the GUI for a product all sit in that product's repository, in different feature branches.

**Val's AI ecosystem.** Val described the AI-CFO he built and connected to Microsoft Business Central (about 75% wired in). He built it with Claude Code Desktop by splitting the work into two parallel sessions — an "architect" session and an "engineer" session — guided by a "second brain." The second brain is his indexed archive of ~5 years of call transcripts (indexed from Jan 1, 2025 forward), linked to a wiki, which gives any AI agent full context on JVL. He gave the example that the AI-CFO recommended shrinking the JVL Systems chart of accounts from 800 accounts to 148, which Val then did in about 4 hours — versus the ~year outside professionals estimated and the 8 months Daniel took to build the original (poor) 800-account structure.

**People and AI adoption.** Val's point to Genadi: the people who embrace these tools grow, and those who don't become dead weight. He cited Khoretsky in Minsk, who now runs ~10 agents each across 3 projects and is asking for a second computer, versus honest, reliable people like Perelman and Strekalov who will not move to this way of working. He hopes Laura will grow into it. He also noted the AI executives operate under a "Constitution" that forbids them from inventing, flattering, or claiming things they don't know.

**Prose + ADR standard.** Val explained the newer standard: AI writes a prose description next to each artifact, and the prose grows as the artifact changes. Prose links the product owner (market-facing requirements, with acceptance criteria) to the engineer (features), grouped by project. Requirements → capabilities → features → feature branches are directly linked. ADRs (short, often one-sentence "ideals") are stored next to the code/drawings; the sum of the ideals is the architecture decision, and nobody hand-draws architecture schematics anymore.

**Automated testing / CI-CD for products.** Automated code review reads the code's semantics and generates unit, integration and end-to-end tests; the end-to-end tests are derived from the acceptance criteria written in prose. Nothing merges to main unless the tests pass. A change flows: feature branch → build via GitHub Actions → deploy to a production server on AWS → machines pull the new software. Val said work that used to take 18 months (e.g., a game) can now be produced in hours from requirements.

**Why it matters — field examples.** Georgia: machines were hanging on a Linux mismatch bug (which Genadi found) — the screen looked alive but buttons were dead and customers couldn't insert money; a street vendor seeing a $20 weekly collection wants the machine gone, which threatens JVL. After a mod and new software, those machines now earn ~$200 vs a market average of ~$108. Nebraska: JVL machines run a 25¢ minimum bet while a competitor runs 40¢ with the same number of games, and the competitor earns roughly twice as much — Val wants to detect and adjust this kind of thing on the fly, which an AI operations/finance officer would surface.

**What Val wants from Genadi.** Build a hardware "operational/product officer" AI (a CxO for hardware) with proper references. Two component types: BUY (market parts with part numbers — power supplies, PLAs, monitors) and MAKE. Engineering specs/artifacts go in GitHub next to code, prose and ADR, tied to the project repo; the order reference/part number lives in Business Central next to that reference (a cross-reference to the GitHub artifact, not a duplicate). The second brain (raw source data) is built in a tool like Obsidian; wiki and documents live in GitHub. Val offered to help set up the starting prompts and to build a second brain for Genadi's hardware CxO from Genadi's accumulated Outlook quotations, so the CxO can review prices/quantities and help automate sourcing. Val acknowledged the standard sounds bureaucratic but stressed JVL is small and Genadi works alone in his department, so he needs the simple version. Genadi noted 4–5 topics he wants to firm up as next steps. Val will send Genadi this transcript to use as a starting base.

**Asides.** Val subscribed to X (Twitter) as a developer and installed the X MCP for Anthropic; each week he asks Claude to review Boris Cherny's latest posts on the "second brain" and apply the learnings. He named Boris Cherny (Anthropic) and Andrej Karpathy as leading thinkers, and said physics/materials is one of AI's not-yet-conquered frontiers — he expects big changes in SolidWorks/mechanical design tools over the next 6–12 months. The meeting ended as Genadi raised a separate short topic; the recording stops there.

## Decisions Made

- **Engineering artifacts live in GitHub, organized by project (1 project = 1 repository).** Drawings, specs, documents and code sit together in the product's repo, in feature branches. Order references/part numbers live in Business Central as a cross-reference to the GitHub artifact, not a duplicate. (Stated by Val, agreed direction.)
- **Genadi will build a hardware "CxO" AI with proper references, in the simple (low-bureaucracy) form suited to a one-person department.** (Agreed direction; Val to help set it up.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Send Genadi this meeting transcript to use as a base for the next steps | TBD | Normal | Val said he will forward the transcript |
| 2 | Genadi | Spend a couple of days in conversation with AI to assess where SolidWorks/AI integration stands and how organized files across Business Central + SolidWorks + GitHub would help a hardware CxO | TBD | Normal | Val's suggested starting point |
| 3 | Genadi | Firm up the 4–5 topics he flagged as next steps and bring them back to define concretely | TBD | Normal | Genadi took notes during the call |
| 4 | Genadi | Structure the accumulated quotations from the past year so a CxO can review prices/quantities for sourcing | TBD | Normal | Depends on organizing/handing over the quotation emails |
| 5 | Val | Help Genadi set up the initial prompts and build a second brain (from Genadi's Outlook quotations) for the hardware CxO | TBD | Normal | Requires Genadi giving access to the quotation emails |

## Open Questions

- Does Genadi need a SolidWorks license and/or a daily-use file server for file exchange? Left unresolved — Val hasn't used SolidWorks and will read up on it.
- How far has SolidWorks/mechanical-design AI actually progressed? Both agreed it needs investigation before committing to specifics.

## Dispatch Log

---
*Processed from Teams transcript on August 6, 2026 (Scheduled Watcher run).*
*Source meeting: General alignment (Val Levitan & Genadi Peari), August 6, 2026*
