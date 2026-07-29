# Meeting Summary — Multi-Repository Project Management with Claude

**Date:** April 6, 2026, 12:02 PM – 1:07 PM Eastern
**Duration:** ~63 minutes (5 recording segments)
**Attendees:** Val Levitan, Aaron Bockelie, Dzmitry Chudzinau, Evgeny Kharetski, Alexander Biratko, Andrei Bosik, Sergey Tsimanov, Irina Shishko

## Summary

Val opened the meeting by presenting a problem the team had been encountering: when developers use Claude Code across JVL's multi-repository GitHub structure, Claude understands what is inside each individual repository but has no awareness of the overall product architecture connecting the repos. Evgeny confirmed this firsthand — Claude works well inside a single repo but begins "conditioning" (degrading in quality) when given too much cross-repo context. He observed Claude sometimes making unauthorized changes in unrelated repos, such as modifying frontend code when tasked with a backend fix. Dzmitry added that anomalous token consumption accompanies this behavior. Val reassured the team that token costs are management's concern, not theirs.

Val then revealed that he had taken a prior recording of the team discussing this issue and fed it into Claude, which produced a proposed infrastructure document. He distributed this document and a separate file (likely from Andrei Bosik's earlier suggestion about using "Ways" — a workspace configuration approach) for the team to review during a 5-minute reading pause. Evgeny's reaction: "It doesn't look like nonsense, it looks like an adequate solution, but until we try it, we won't know how convenient it is." Val emphasized repeatedly that he is not an engineer and depends on the team's judgment to validate or reject the proposal.

When discussion resumed, Sergey Tsimanov asked for clarification: the proposal is to create a shared repository that describes the full architectural context for a set of related microservices, so a new developer or Claude can clone it and understand what connects to what. Val confirmed the core insight: "The architecture of the product stays in our heads. It is undocumented." Each repo has its own local documentation, but there is no central document explaining how the repos within a product relate to each other, communicate, and depend on one another. Dzmitry stated this plainly: "Claude can't connect the dots across repos because there is no central repository describing the full architecture."

The team converged on a two-tier documentation model: each repository keeps its own detailed documentation (architecture, specs, timing diagrams), and a higher-level "Repository Zero" provides the connecting map describing how all repos in a product relate to each other. Sergey raised a collision concern — if multiple developers contribute to the architecture doc, how do they avoid breaking each other's sections? Val agreed this means the team must formally agree on the architecture and actively maintain it.

A sidebar on local development arose when Sergey questioned whether the full AWS infrastructure could be replicated locally. Andrei Bosik explained why local development containers are essential: deploying every change to AWS for testing would dramatically slow development. The standard workflow is: develop locally in containers, see changes immediately, then commit and push through the CI/CD pipeline (GitHub → build → infrastructure repo → AWS Kubernetes cluster). Val initially questioned why local infrastructure replication was needed at all — the team explained this is standard industry practice. Dzmitry pointed out a practical constraint: if two developers are working on the same product (e.g., Payment Hub), local containers let each work independently, whereas deploying to a shared cloud environment would create conflicts.

Alexander Biratko raised practical scope and structure questions. On scope: should the top-level repo cover all products, or just one? Val decided to start with Flex-POS — it is the next product release, its repos are already on GitHub (unlike games, which are still partly in SVN in Moscow), and it consists of approximately 5 constituent repos including Observability Platform, Payment Hub, and Flex-POS Station. On structure: Biratko proposed using a dedicated specification file (not CLAUDE.md) in the top-level repo that lists submodules and their locations. This gives Claude a structured entry point — it reads the spec file, learns the product topology, then dives into each submodule's own documentation for details. Dzmitry flagged the governance problem: when one repo's architecture changes, the central repo must be updated too. No mechanism for enforcing this was defined. Biratko also warned that Claude must be constrained to specific repos per task to prevent unauthorized cross-repo modifications.

Aaron Bockelie joined the call approximately 36 minutes in and Val briefed him on the situation. Aaron immediately identified that the repos originated from an SVN migration and that the old SVN directory-branch thinking still persists — mentally, the team treats GitHub the same way they treated one big SVN server. He cautioned against simply recreating SVN's monolithic structure.

Aaron introduced several foundational concepts. First, the **monorepo vs. microservice distinction**: a monorepo is a single repository containing all code for a concern; a microservice is a service that runs independently with its own data, interfaces, and ability to function alone. These are orthogonal concepts — a monorepo can contain a microservice, and multiple repos do not automatically mean you have microservices. He assessed that JVL currently has "macro-services" — large services bundled with particular domains (payment, database, billing) that have interdependencies.

Second, **data contracts**: Aaron identified the underlying root cause as undocumented inter-service communication. A data contract is a promise for how two services exchange data — API endpoints, message formats, bus protocols. He guessed (and Evgeny confirmed) that JVL's services have interdependencies without known data contracts, which is why developers need 3 repos (Biratko claimed up to 10) cloned simultaneously to complete a single task. Without defined contracts, developers must reverse-engineer how services talk to each other by reading the actual source code in adjacent repos.

Third, the **Meta Poly Repo pattern**: Aaron proposed creating a Git repository containing no functional code — only submodule definitions pointing to the actual repos, plus integration tooling and architectural context/documentation. When cloned recursively, it pulls down all constituent repos in a managed tree structure. The meta repo also holds the steering context and architectural descriptions the team had been describing.

Aaron delivered a critical warning: **the meta poly repo is a crutch, not a destination.** It is an intermediary step. The real work is establishing stronger data contracts between repos and progressively decomposing the current macro-service repos into smaller, truly independent concerns. The current repos are "not wrong" but have interdependencies that prevent independent work. Over time, repos should evolve toward true microservice boundaries where each can stand on its own — each owning its data, its interfaces, and its execution. He cautioned against breaking things into microservices where it doesn't make sense: "You should always be thinking about the data structure and the pools of data that you're managing, not the execution concerns of the software."

In his 2-minute closing segment, Aaron used SAS as a concrete example: SAS messaging is triggered in a specific contractual way — that's a data contract. The meta repo collects all submodules which collect all contracts needed to work on any piece of the platform. He framed this as an architectural thinking exercise: the team needs to wear "architecture hats" rather than just engineering/building hats. The underlying problem — "a not well-architected interaction of promises, of contracts between the software" — is why everyone has to clone everything, and why Claude struggles to create software and understand the platform.

## Decisions Made

- **Create a Meta Poly Repo for Flex-POS** — a Git repo with submodules, no functional code, containing architectural context and product topology. (Proposed by Aaron, endorsed by team)
- **Start with Flex-POS as the first product** — it is the next release, already on GitHub, and consists of ~5 repos. Games repos deferred because SVN migration is incomplete. (Decided by Val)
- **Two-tier documentation model** — each repo maintains its own detailed docs; a higher-level repo provides the connecting architectural map. (Team consensus)
- **Specification file, not CLAUDE.md, for product description** — a dedicated spec file in the meta repo that lists submodules and their locations. (Proposed by Biratko)
- **Local container development is the standard workflow** — confirmed as industry-standard practice, not questioned further. (Andrei, Dzmitry, Sergey)
- **Meta poly repo is explicitly transitional** — the long-term goal is stronger data contracts and progressive microservice decomposition. (Aaron's strong recommendation)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Team (unassigned) | Define the product-to-repo mapping for Flex-POS — identify all constituent repos (Observability Platform, Payment Hub, Terminal Hub, Flex-POS Station, others) | TBD | High | Andrei's "question zero" — must be answered before the meta repo can be created |
| 2 | Team (unassigned) | Schedule and conduct a follow-up architecture session — team sits together virtually, discusses architecture from each person's perspective, records transcript, and lets Claude draft first version of central architecture doc | TBD | High | Val's recommended approach for producing the first architecture document |
| 3 | Team (unassigned) | Create the first meta poly repo for Flex-POS — establish the Git repo with submodule definitions, steering context, and product specification file | TBD | High | Core deliverable from this meeting |
| 4 | Team (unassigned) | Define per-repo documentation standard — what architecture docs, data contracts, and interface specs each repo must carry | TBD | Normal | Prerequisite to central repo being useful; each repo's docs must be adequate first |
| 5 | Team (unassigned) | Inventory and formalize data contracts between Flex-POS services — API endpoints, message-bus formats, inter-service dependencies | TBD | High | Aaron identified this as the root cause of cross-repo coupling; without it, the meta repo is just a directory listing |
| 6 | Team (unassigned) | Define a maintenance process for keeping the central architecture repo in sync with individual repo changes | TBD | Normal | Dzmitry's governance concern — no mechanism currently exists |
| 7 | Team (unassigned) | Establish Claude constraint mechanism — rules/configuration to prevent Claude from modifying repos outside its assigned scope | TBD | Normal | Flagged by Biratko and Evgeny; risk of silent unauthorized cross-repo changes |

## Engineering Signals

### Confirmed Signals
- **ADR: Meta Poly Repo pattern for multi-product repository organization** — Aaron proposed and the team endorsed using a Git repo with submodules as the structural pattern. Aaron explicitly named it "meta poly repo" and defined it as containing no functional code, only submodule definitions and integration tooling. This is a significant architectural decision for JVL's GitHub organization.
- **ADR: Data contracts as the organizing principle for inter-service communication** — Aaron identified that JVL's services lack formalized data contracts and that this is the root cause of tight coupling. He recommended defining data contracts (API endpoints, message formats, bus protocols) as the path toward decoupling. "A data contract is a promise for exchanging data in a particular way."
- **ADR: Meta poly repo is transitional, not permanent** — Aaron explicitly cautioned: "This is not the final state of what you're going to work in. It is a crutch." The long-term direction is progressive decomposition toward true microservice boundaries.

### Suspected Signals
- **Possible REQ: Per-repo documentation standard** — The team discussed that each repo needs architecture docs, timing diagrams, and data-contract specifications, but no formal standard was defined.
- **Possible REQ: Claude scope-constraint mechanism** — Biratko and Evgeny flagged that Claude must be prevented from modifying repos outside its assigned scope. This could be a tooling requirement.

## Open Questions

- Who leads the architecture session for Flex-POS? Val suggested the team "sit in one room virtually" but did not assign an owner.
- What format should the specification file in the meta repo take? Biratko proposed a dedicated file, but no template or format was defined.
- How should games repos (LandBase) be handled when SVN migration completes? Deferred for now.
- Should the meta repo also contain integration tooling for local container development, or just documentation and submodule definitions?

---
*Processed from meeting transcript on April 8, 2026*
*Source meeting: Multi-Repository Project Management with Claude — April 6, 2026*
