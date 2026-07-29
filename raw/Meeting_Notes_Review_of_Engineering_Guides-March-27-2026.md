# Meeting Summary — Review of Engineering Guides
**Date:** March 27, 2026, 11:02 AM Eastern
**Duration:** ~1 hour 29 minutes
**Attendees:** Val Levitan, Dmitri Kovalchuk, Andrei Bosik, Pavel Frolov

## Summary

The meeting focused on reviewing and discussing Val's "Engineering Guides" document — a minimum set of engineering documentation standards for JVL. Val opened by stating that he deliberately chose the absolute minimum documentation requirements given the company's size, noting that engineering companies of comparable scope typically maintain far more documentation than what he proposed.

### Meeting Recording & Transcript Pipeline

Dmitri raised the first concern: AI needs access to meeting recordings to produce documentation automatically. Val explained that this problem is already being solved — Clayton and Elena Zhukova are finalizing an automated pipeline. The process works as follows: after a meeting ends, the recording is automatically captured in two formats — an audio format (WAV) and a "dirty" format (Teams transcript with timestamps and speaker attribution). The audio goes through a lexicon module on GitHub that cleans it up and produces a clean document. From this clean format, the system will also automatically propose ADRs (Architectural Decision Records) and other engineering artifacts. Val emphasized these are *proposed*, not imposed.

Andrei asked whether transcripts should be stored in a single repository or tied to specific projects. He argued for project-level attachment so transcripts aren't disconnected from context. Pavel noted that storing audio on GitHub is a bad idea; Andrei clarified the proposal is text transcripts only, which are small files where Git versioning is actually beneficial.

Val shared his personal workflow since 2018: he categorizes things as "initiatives" (not yet in Jira — still in discussion phase) versus projects/products (once they land in Jira). He uses Obsidian vaults organized by business (JVL, real estate, personal) with monthly groupings. He expressed mild concern about dumping all raw transcripts into GitHub but acknowledged the files are small enough that versioning helps.

### ADRs, Requirements, and Their Relationship to Jira

Dmitri and Pavel raised concerns about ADRs potentially becoming disconnected from the rest of the workflow. Pavel added that if ADRs have statuses (proposed, accepted, deferred, etc.), this adds complexity — status changes would need to happen via pull requests modifying text files.

Pavel raised a critical workflow question: requirements trigger feature creation in Jira, but ADRs can *also* trigger feature creation. He estimated that 80–90% of the time, ADRs (which are more technical in nature) would be the actual trigger rather than business requirements. This means features in Jira might reference an ADR rather than a formal requirement.

Val agreed and provided context: the team has already discovered that features (as currently used in Jira) don't work well as an engineering planning tool. He cited the example of "Piratka" (a developer) who doesn't use features because they don't map to how he works. The team concluded that the workflow should be: **Capability Tickets → ADRs → Features**. An engineer reviews capability tickets, discusses architectural approaches, creates ADRs from those discussions, and then writes features linked back to both the ADRs and the capability tickets.

Pavel clarified the sequencing: developers can quickly identify *what* features are needed, but they can't plan *how* to implement them until ADRs are created. Features may be created before ADRs exist, but story-level planning definitely requires ADRs. The group debated whether this means features must wait for ADRs or can proceed in parallel, without reaching a definitive conclusion.

### Architecture Overview — The Missing Foundation

Val made a key point that the team may have overlooked: JVL already *has* an architecture — it's just undocumented. He described the current ADRs being created as "a drop in the ocean" compared to what a 42-year-old company should have in its documentation library. ADRs are merely additions to an architectural foundation — but that foundation doesn't exist on paper.

Pavel agreed: even taking all existing ADRs from current projects, you could partially reconstruct the system architecture, but there would be significant gaps because there's no master document describing the overall system.

Val called this the biggest "black hole" and said it probably can't be created backwards — it needs to be built going forward. He estimated it would require perhaps 10 detailed interview sessions with team members to create an initial architectural overview, after which ADRs would incrementally develop it.

Val illustrated the problem with a real business example: JVL's gaming machines on older frameworks have been experiencing mysterious freezes for years. Previously, machines operated in casinos with dedicated technicians who maintained them daily. Now machines operate at standalone locations (gas stations, etc.) with no on-site support. When machines freeze, the screen looks normal but all functions are dead — customers simply walk away and play a different machine. The result: JVL lost millions in revenue, operators stopped buying machines, and some locations ejected JVL.

Investigating the freezes revealed architectural questions with no documented answers: Why was C++ chosen for the framework? Why does the Java-based data center communicate directly with the C++ framework? Could Java hanging cause C++ to freeze? Why doesn't the watchdog timer work? Someone at some point made these architectural decisions without documenting them — and now there's no way to trace back through the reasoning.

Val contrasted this with a competitor's system ("Omni") where everything runs as separate containers communicating through HTTP protocol, allowing individual container restarts without bringing down the whole machine. He argued this kind of modular architecture discussion is exactly what should have been documented.

### Enforcing Documentation Culture

Val emphasized that the documentation initiative will only succeed if it becomes company culture, not a mandate. He's against outright prohibitions, preferring to spread the culture through visible reporting. For example, the team could enforce that moving a feature to "In Progress" in Jira requires a link to a feature branch in GitHub. Dmitri and Andrei confirmed this isn't yet implemented.

Pavel cautioned that some tasks are fire-fighting (on-call/support) and shouldn't be blocked by documentation requirements. He suggested sending notification emails about violations rather than hard blocks.

Val proposed that meetings should start with opening Jira and discussing tasks by ticket number — anchoring conversations to factual, trackable items rather than starting from a vacuum. Pavel agreed that at minimum, every meeting should reference a project, capability ticket, or feature.

Val stressed that developers need to be *required* to come to meetings prepared — with objectives, allocated time, and specific items to discuss. This needs to be pushed consistently until it becomes habit, especially since long-tenured employees have never been asked to work this way before.

### Jira Hierarchy Restructuring

The group discussed restructuring Jira's issue hierarchy. The current structure is: Value Stream → Initiative → Product → Feature → Story → Task (subtask). The proposed new structure:

- **Value Stream** (stays)
- **Product** (replaces Initiative)
- **Capability Ticket** (new level, replaces current Product)
- **Feature** (stays)
- Stories and Tasks → move to **GitHub** with kanban boards

Val expressed a strong preference for shorter cycles and stated that Value Stream, Product, Capability Ticket, and Feature are the essential levels. He wants stories and tasks managed in GitHub where developers already work with feature branches and pull requests.

Dmitri demonstrated the proposed changes live in Jira's sandbox, showing that renaming levels preserves existing relationships. However, inserting a new level (Capability Ticket) between existing levels would break ~1,700 parent-child links between Product and Feature.

Pavel suggested a practical approach: rename current Initiatives to Products, current Products become Capability Tickets, current Features stay as Features, and everything below Features moves to GitHub. Old items would live out their lifecycle under the old names while new items follow the new structure.

Dmitri offered to prepare a comparison table (current vs. proposed) for each hierarchy level, showing factual examples of what exists now and what it would become. Val asked for this in Excel format so he can work through it with AI assistance.

### Engineering Guides Document — Specific Feedback

Pavel recommended that the **onboarding section** be removed from the project-level document, as onboarding content belongs in a company-wide runbook, not per-project documentation. Val agreed and committed to revising the document.

Andrei questioned why the proposed directory structure separates "Architecture" and "ADRs" into different folders, arguing they cover similar ground. Pavel clarified that ADRs are specifically about *decisions*, while architecture also includes specifications, interface descriptions, protocol documentation, and module descriptions — not covered by ADRs alone. An overarching architecture document is needed to tie ADRs together.

### Workflow Example Request

Andrei requested that the Engineering Guides document include a **concrete, step-by-step workflow example** showing the full process: from a recorded meeting → transcript → AI processing → ADR extraction → repository storage → document revision. He emphasized it should be based on facts, with question marks where details are unknown rather than AI-generated speculation. Val agreed to produce this.

### Timeline and Assignments

Val stated the automated transcript processing pipeline (Clayton/Elena) should be ready within **2 weeks** (by approximately April 10, 2026). He asked the team to prepare the repository structure and working environment so that when the pipeline arrives, they can immediately begin using it.

## Decisions Made

- **Onboarding section to be removed from the per-project Engineering Guides document** — it belongs in a company-wide runbook instead. (Proposed by Pavel, agreed by Val)
- **Stories and Tasks to move to GitHub** — Jira will handle Value Stream, Product, Capability Ticket, and Feature levels; GitHub handles stories/tasks with kanban boards. (Proposed by Val, group consensus)
- **Engineering Guides document to be revised** — Val will process this meeting's transcript through AI and produce version 6.3 with incremental improvements. (Val)
- **Jira hierarchy renaming approach** — rename existing levels rather than insert new ones to preserve links; old items live out their lifecycle. (Proposed by Pavel, demonstrated by Dmitri)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dmitri Kovalchuk | Prepare a comparison table (Excel) showing current vs. proposed Jira hierarchy — for each level, show what exists now, what it maps to in the new structure, with factual examples and screenshots of current/proposed layouts | TBD | High | Val needs this to evaluate the Jira restructuring; can't proceed without visual comparison |
| 2 | Pavel Frolov | Collect and document the current architectural overview of the Omni system — what exists today, how components interact, key technical decisions | April 10, 2026 | High | Only Pavel has the depth of knowledge to produce this; it's the foundation that ADRs will build upon |
| 3 | Dmitri Kovalchuk & Andrei Bosik | Set up the repository structure and working environment for the automated transcript processing pipeline — ensure document storage locations, folder structures, and integration points are ready | April 10, 2026 | High | The Clayton/Elena pipeline will be ready in ~2 weeks; the team must be prepared to receive and process transcripts immediately |
| 4 | Val Levitan | Revise the Engineering Guides document to version 6.3 — remove onboarding section, incorporate meeting feedback as incremental improvements | TBD | Normal | Document is currently at version 6.2; needs to reflect today's discussion |
| 5 | Val Levitan | Add a concrete step-by-step workflow example to the Engineering Guides document — from recorded meeting through transcript processing to final document revision, fact-based with question marks where details are unknown | TBD | Normal | Andrei's request to make the document actionable with a real-world workflow illustration |

## Engineering Signals

### Confirmed Signals

- **ADR: Workflow chain — Capability Tickets → ADRs → Features:** The group explicitly agreed that the engineering workflow should flow from capability tickets through architectural decision records to feature implementation. Engineers review capability tickets, create ADRs during technical discussion, then write features linked to both ADRs and capability tickets. Val stated: "To fulfill a capability ticket, you need to create features. But to create those features, you need a series of architectural decisions."

- **REQ: Automated transcript-to-documentation pipeline:** Val confirmed that Clayton and Elena Zhukova are building an automated pipeline that captures meeting recordings in WAV and Teams transcript formats, processes the audio through a lexicon module on GitHub, and automatically proposes ADRs and other engineering artifacts. Expected delivery: ~2 weeks (by April 10, 2026).

- **ADR: Stories and tasks move from Jira to GitHub:** Val explicitly decided that stories and tasks should be managed in GitHub with kanban boards, not in Jira. Jira retains Value Stream, Product, Capability Ticket, and Feature levels. Rationale: developers already work in GitHub with feature branches and PRs; keeping granular work items there reduces context-switching.

### Suspected Signals

- **Possible ADR: Jira hierarchy restructuring (Value Stream → Product → Capability Ticket → Feature):** The group discussed renaming Jira levels extensively, but no final "go" was given — Val requested a comparison table first.

- **Possible REQ: Jira enforcement — require GitHub feature branch link before moving feature to "In Progress":** Val and the team discussed requiring a link to a GitHub feature branch when a Jira feature enters "In Progress" status. Not yet implemented. Pavel suggested notifications rather than hard blocks.

- **Possible REQ: Meeting preparation standards — participants must come with objectives, ticket references, and allocated discussion time:** Val emphasized this multiple times as essential to the documentation culture shift.

## Open Questions

- **How to create the initial architectural overview ("architecture overall")?** Val acknowledged this is a "black hole" — the company has architecture but no documentation. He suggested ~10 detailed interview sessions with team members. No concrete plan or owner for this beyond Pavel starting with the Omni system.
- **Should ADRs and Architecture share a folder or remain separate in the repository structure?** Andrei suggested combining them; Pavel argued they serve different purposes. No resolution reached.
- **How to handle the ~1,700 broken parent-child links if a Capability Ticket level is inserted between Product and Feature in Jira?** Dmitri flagged this; Pavel suggested renaming existing levels rather than inserting. Final approach pending the comparison table.
- **How should fire-fighting/on-call tasks be handled in the new documentation workflow?** Pavel raised that support tasks shouldn't be blocked by documentation requirements. No policy decided.

---
*Processed from Teams transcript on March 27, 2026*
*Source meeting: Review of Engineering Guides*
