# Meeting Summary — Code Prep Plan
**Date:** April 1, 2026, 9:46 AM Eastern
**Duration:** ~14 minutes
**Attendees:** Val Levitan, Dzmitry Chudzinau, Andrei Bosik, Sergey Tsimanov

## Summary

Val opened the meeting by establishing that the entire codebase for what was formerly called "Back Office" — now renamed to the Observability Platform — has been migrated to GitHub. He stated that this code is poorly documented, both in general terms and specifically for working with AI tools. He asked Dzmitry to confirm that in order to use Claude Code (AI) effectively against the production codebase, the existing code needs to be cleaned up ("combed through") and properly documented. Dzmitry confirmed.

Val acknowledged this cannot be done in a single pass and that the team has other ongoing work. Dzmitry suggested approaching it modularly — either by module or by business feature. Val proposed a "semi-contract" arrangement: the team allocates **2 hours per day**, uninterrupted, dedicated exclusively to this code cleanup work, with no one else pulling them into other tasks during that time.

On timeline estimation, Val asked roughly how long the full cleanup would take. Dzmitry said it would certainly take more than a week and that precise estimates would only be possible once they start and observe their pace. Val estimated **30 to 45 days**. Dzmitry agreed that sounded more realistic, possibly faster.

Val asked about tracking progress visually. Dzmitry suggested committing documentation as they go, with a periodic script checking the repository for updates. **Andrei proposed creating a feature in Jira** with stories tied to each repository, marking completion as they go. Dzmitry noted the codebase contains **5 or 6 applications** — 2 of which are very large and complex, the remaining 4 being smaller and easier to document.

Val pushed back on the Jira approach for tracking. He outlined a different strategy: do a straightforward code cleanup via Claude Code first. Once Claude Code has ingested and understood the entire codebase, Val would then ask it to generate: (1) a set of features (as if building the product from scratch), (2) a set of capabilities, (3) a set of requirements, and (4) architectural block diagrams. He clarified that while he says "I'll do it," he means the development team will execute this — he doesn't have the technical knowledge.

Dzmitry agreed with the general approach but raised a concern about Claude Code getting confused with large code volumes. He also asked whether they should document **deprecated features that haven't been used in 10–15 years**, specifically mentioning "Italy" (a legacy module/feature). Val said yes — document everything, including unused code. His reasoning: the incremental cost of Claude Code processing it is minimal (maybe an extra day, ~$500 in tokens), and having everything documented gives the team the ability to clearly identify what to keep and what to discard. However, if the team is confident they can cleanly extract deprecated code without side effects, they can do so. If there's any doubt about hooks, dependencies, or bindings, it's better to document it and mark it for deletion rather than risk breaking something.

Dzmitry agreed to the approach: **document everything as-is, adding markers/annotations to deprecated code** that hasn't been used in 10–15 years, flagging it for deletion.

Val expressed his desire to stay aligned with the team throughout the process — not to contribute technically, but to see progress and feel the work moving forward. He asked **Andrei to create a transparent visual progress report** showing the entire repository scope and percentage completion of each section, updated as work progresses. Andrei said he'd need the team to complete at least a few items first before he could build a meaningful report.

Dzmitry suggested discussing whether to track via Jira or another method. **Val explicitly advised against Jira** for this effort — it would add unnecessary complexity. The goal is to clean up the repositories so the team can then comfortably plan the transition to a new architecture. Val said they'll discuss architecture and build together once the codebase is clean.

Andrei raised a question about a calendar item referencing an **"optimized Azure architecture" deadline of April 14**. Val said he hadn't specifically meant Azure — he may have misspoken when writing the invite. Andrei explained the fundamental dependency: the cloud architecture (Azure, AWS, or otherwise) depends entirely on what the development team can accomplish first. Specifically:
- If they can containerize everything in Docker → one architecture
- If some components can't be containerized → different architecture
- If they can migrate to PostgreSQL → one architecture
- If they can't migrate to PostgreSQL → different architecture

Until Dzmitry and Sergey provide concrete answers on these architectural decisions, Andrei cannot propose a cloud architecture. Val understood and agreed to:
1. Change the meeting invite wording from "Azure architecture" to "optimized architecture" (removing the cloud provider assumption)
2. Push the architecture review meeting back **30 days** (to ~May 1, 2026), with the option to push further if needed

Val closed by summarizing the agreements: Andrei will set up progress tracking, the team will reserve 2 hours daily, and they should start immediately. Dzmitry confirmed they would **start tomorrow (April 2, 2026)**. Sergey confirmed as well.

## Decisions Made

- **Document all code including deprecated features** — Even unused legacy modules (like "Italy") will be documented and annotated with deprecation markers rather than skipped. Rationale: low incremental cost via Claude Code, and gives the team clear visibility to make keep/discard decisions later. (Decided by Val, accepted by Dzmitry)
- **No Jira tracking for this effort** — Progress will be tracked via a custom visual report, not Jira, to avoid adding a layer of complexity. (Decided by Val)
- **Architecture review postponed 30 days** — The "optimized architecture" meeting is pushed to ~May 1, 2026. Cloud architecture cannot be determined until the team provides answers on containerization and database migration feasibility. (Decided by Val, based on Andrei's input)
- **Removed Azure assumption from architecture planning** — The meeting invite will be changed from "Azure architecture" to "optimized architecture" since the cloud provider depends on architectural decisions not yet made. (Decided by Val)
- **2 hours/day dedicated to code cleanup** — The team will block 2 hours daily in their schedule, uninterrupted, for this work. (Proposed by Val, accepted by team)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Create a transparent visual progress report showing the full repository scope, with percentage completion per section, updated as work progresses. Wait for the team to complete a few initial items before building the first version. | TBD (after initial progress) | High | Val needs visibility into cleanup progress; the team needs shared alignment on what's done vs remaining |
| 2 | Dzmitry Chudzinau, Sergey Tsimanov | Begin code cleanup and documentation work — allocate 2 hours/day blocked in schedule, starting April 2, 2026. Approach modularly. Document all code as-is including deprecated features, adding deprecation markers. | April 2, 2026 (start date) | High | Prerequisite for AI-assisted development with Claude Code and for future architecture planning |
| 3 | Val Levitan | Update the architecture review meeting invite — change wording from "Azure architecture" to "optimized architecture" and reschedule the meeting ~30 days out (~May 1, 2026) | April 1, 2026 | Normal | Corrects premature Azure assumption; gives dev team time to answer architectural questions first |
| 4 | Dzmitry Chudzinau, Sergey Tsimanov | Provide Andrei with concrete answers on architectural decisions: (a) Can all components be containerized in Docker? (b) Can the database be migrated to PostgreSQL? | TBD (as cleanup reveals answers) | High | Andrei cannot propose any cloud architecture until these questions are answered |

## Engineering Signals

No engineering signals detected in this meeting.

## Open Questions

- **What specific modules/applications are in scope?** Dzmitry mentioned 5–6 applications (2 large, 4 smaller) but didn't name them all. The scope needs to be enumerated.
- **What constitutes "done" for code cleanup?** No explicit definition of quality standard — is it comments in code, README files per module, API documentation, type annotations, or all of the above?
- **How will the visual progress report be delivered?** Andrei agreed to create it but the format (dashboard, spreadsheet, simple markdown) wasn't discussed.
- **What is "Italy"?** Dzmitry referenced it as a deprecated feature — its scope and entanglement with active code is unknown.

---
*Processed from Teams transcript on April 1, 2026*
*Source meeting: Code Prep Plan*