# Ways — Capabilities Derived from Architectural Decisions

**Purpose:** For each architectural decision Aaron made when designing Ways, this document identifies the capabilities that decision makes possible.
**Basis:** February 2026 JVL meeting transcripts — source-only, no invention.
**Companion document:** `Aaron_Ways-ADR.md` (the decisions themselves)

---

## How to Read This Document

Each section corresponds to one architectural decision from the ADR. Under each decision, the capabilities it enables are listed — things the system can do *because* that decision was made. The connection between decision and capability is stated explicitly.

---

## Decision 1: Build an Overlay, Not a Replacement

*Ways is built on top of a default Claude Code installation without modifying it.*

**Capabilities this decision enables:**

**Works on any Claude Code installation without setup friction.**
Because Ways sits on top of the platform rather than inside it, any developer with Claude Code installed can adopt Ways by cloning a repository and configuring hooks. There is nothing to patch or replace.

**Survives Claude Code updates.**
Because Ways does not modify Claude Code's internals, updates to Claude Code do not break Ways. The two evolve independently.

**Distributes via personal fork, not via IT deployment.**
Because it is an overlay on each developer's own Claude Code installation, each developer controls their own instance. This is by design — Aaron draws the direct analogy to compiler configuration:
> *"Pretty much every software engineer ever doesn't let the IT department manage their compiler configuration."*

**Can be adopted incrementally.**
A developer can adopt Ways on their user scope without any changes to any repository. They can add project-scope Ways to a single repo without affecting others. The overlay model allows partial, incremental adoption.

---

## Decision 2: Separate "Why" from "How" — Ways Carries Only Reasoning

*Ways encodes only reasoning and principles. Procedure belongs in Skills.*

**Capabilities this decision enables:**

**Context stays focused and non-redundant.**
By excluding procedure from Ways, each Way stays short and topically tight. A Way for pull requests explains why PRs matter; it does not duplicate the steps the PR skill already handles.

**Ways remain valid across tool changes.**
Principles outlast procedures. If the GitHub CLI changes its flags, the pull request Skill must be updated. The pull request Way — which encodes *why* pull requests matter — needs no update because the reasoning does not change when the tool does.

**Skills and Ways co-trigger for full context coverage.**
Because they are maintained separately and triggered through different mechanisms, both can fire simultaneously without conflict. The developer gets the *why* from a Way and the *how* from a Skill in a single session:
> *"You don't have to type any of this stuff in because it's there already. And then you have the tools and the skills — it knows exactly what commands to run."*

**New ways can be written for any technology or domain.**
Because Ways are pure reasoning, they can be written for anything — Spring, Webpack, SAS protocol, release versioning, code review philosophy — without entangling procedure. Aaron demonstrates this live by creating a Spring Way that explains why the team uses Spring (consistency, compatibility), paired with a Spring Skill that says how to write Spring code correctly.

**Ways can span non-engineering domains.**
Legal reasoning, finance reasoning, and professional standards for any domain can be encoded as Ways by activating the appropriate domain group. The separation of reasoning from procedure is what makes this cross-domain portability possible.

---

## Decision 3: Use Hooks as the Delivery Substrate

*Ways is a submodule of hooks inside `~/.claude/hooks/ways/`.*

**Capabilities this decision enables:**

**Operates within Claude Code's own extension architecture.**
Using Anthropic's hook system places Ways inside the designed extension points of the platform. Ways scripts execute at the right moment in Claude Code's processing pipeline — not before, not after, but at the point where context injection is expected and handled.

**Executes automatically on session start.**
Hooks are triggered by Claude Code's own session lifecycle. This is the technical mechanism behind the "zero manual invocation" capability — the hook system calls Ways without any developer action.

**Supports domain sub-grouping within the hooks tree.**
The hooks/ways directory tree organizes domains (software dev, SSH, ADR, GitHub, legal, finance) as sub-directories. Activation and deactivation of domain groups maps directly to this tree structure.

---

## Decision 4: Mirror Anthropic's Scope Model

*User scope at `~/.claude/`; project scope at `.claude/` in each repo.*

**Capabilities this decision enables:**

**User-scope Ways follow the developer everywhere.**
Because user scope applies to every project a developer touches, a developer's professional standards — their commitment to ADRs, their GitHub conventions, their documentation philosophy — are injected into every session without any per-project configuration.
> *"Every project you interact with, whether you have rights to do it or not — it's going to kind of do that."*

**Project-scope Ways stay in the project.**
Repository-specific Ways — webpack federation patterns, micro front end conventions, build-specific guidance — exist only where they belong. They never bleed into other projects.

**Both layers always operate together.**
The dual-scope architecture means every session carries both the developer's professional identity (user scope) and the project's specific context (project scope) simultaneously. Neither replaces the other:
> *"Waze is what incorporates both. It reads both."*

**Team consistency enforced through shared user-scope Ways.**
When all developers on a team clone the same user-scope Ways repository, they all receive the same professional baseline injected into their sessions across every project they work in. This is the mechanism for team-wide behavioral consistency.

**Per-project Ways committed to the project repo.**
Project-scope Ways are committed to the project's `.claude/` directory. Any developer who clones the repo gets the project-specific Ways automatically. This was Aaron's direct response to Evgeny Kereski's question about whether Ways should live with the project:
> *"It already does that. I just showed you guys that it does that. There's a local Waze per project that exists."*

---

## Decision 5: Pattern-Matched Automatic Injection — Not Manual Invocation

*Ways match conversational content and fire without developer action.*

**Capabilities this decision enables:**

**Zero cognitive overhead during sessions.**
The developer never has to remember which Way to invoke, what it is called, or when it is relevant. The system handles all of that. The developer states their intent; Ways handles the context.

**Relevant context arrives at the right moment.**
Because injection is triggered by what the developer is currently discussing, the injected Way is always contextually appropriate. Discussing a release? Release Way fires. Mentioning webpack? Webpack federation Way fires.

**Multiple relevant contexts arrive simultaneously.**
When a session involves multiple topics that each have a configured Way, all matching Ways inject together. The developer gets compound context without compound effort:
> *"As soon as you say 'let's make a release' — the make way gets injected, the GitHub way gets injected."*

**The workflow is uninterrupted.**
Because injection is silent and invisible, it does not create a pause, a confirmation dialog, or a visible system message. The developer's flow is not broken.

**The injection can be verified when needed.**
While invisible by default, the injection is auditable. Aaron notes this explicitly — the system is transparent on demand.

**Once configured, it just works.**
> *"No, you never have to run it once it's set up right. It just works. It just exists."*

---

## Decision 6: Two-Part Way Structure — Text File and Macro

*Each Way has a static text file (the why) and an optional runtime macro.*

**Capabilities this decision enables:**

**From the text file:**

The static text file provides reliable, human-readable, version-controlled reasoning. Any developer can read what is being injected. The text is auditable, diffable in git, and reviewable in PRs. This is the plain truth of what Claude is being told.

**From the macro:**

**Environment-aware injection.**
The macro knows which project it is running in. An ADR Way can detect whether ADR tooling is installed in the current project and inject different content accordingly — "ready to go" versus "tooling declined." The injected guidance is never blindly assumed.

**Live data integration.**
The GitHub macro calls the GitHub CLI during session startup. It reads the actual collaborator count, the actual repository configuration, and injects a description of current conditions:
> *"It uses the GitHub command line tool to count the number of users in there and figures out whether it's a solo project or a collaborative project."*

**Conditional guidance based on project state.**
For poorly configured multi-user repositories, the macro actively escalates — it injects pressure on the agent to raise the configuration gap as an issue. The same Way behaves differently depending on the project it is running in.

**Controllable injection position.**
Macros can be configured to prepend (inject at the beginning of context) or append (inject at the end). This gives the designer control over where in the context window the Way's content lands.

---

## Decision 7: PR-Gated Governance for All Ways Changes

*Changes to Ways go through pull request review.*

**Capabilities this decision enables:**

**Changed agent behavior requires team approval.**
No individual can change what Claude is instructed to do without it going through the PR review process. The team, not any single developer, controls the evolution of their collective agent guidance.

**Audit trail for all guidance changes.**
Every change to a Way has a commit hash, a PR description, a reviewer, an approval date, and a diff showing exactly what changed. The history of how the team has instructed Claude is fully preserved.

**Behavior correction is propagated to the whole team.**
When a developer discovers Claude consistently doing something wrong and writes a corrective Way, that Way — once PR-approved — is available to every developer on the team. The fix is shared:
> *"When you're changing the ways, you can incorporate — you have a form of governance."*

**Release behavior is consistent across all developers.**
The release Way, shared through the team's Ways repository, ensures that every developer managing releases receives the same versioning policy and changelog mandate injected into their sessions:
> *"Those that are managing releases of some kind will have a consistent messaging about how releases are done injected into their work."*

**Regulatory compliance chain is auditable.**
Because Ways are PR-governed, the complete chain from regulatory requirement to injected prompt can be reconstructed from the git history. Each Way can reference the policy it implements; each policy references the regulatory requirement it satisfies. The audit path exists in the commit record.

---

## Decision 8: Design for Full Regulatory Provenance Traceability

*The chain from regulatory framework to context injection is designed to be traceable.*

**Capabilities this decision enables:**

**Agent behavior traceable to organizational policy.**
Because each Way can reference the policy document it implements, it is possible to answer: "Why is the agent doing this?" and trace the answer back to a written organizational policy.

**Policy traceable to regulatory requirement.**
Because each policy references the regulatory control it satisfies, and each control references the framework it comes from, the full chain is recoverable:
> *"This gets injected in this repo, which was called at this point, which was called at this policy, which was called here, which was called from here."*

**Ways suitable for regulated industries.**
The traceability architecture makes Ways applicable in environments where software behavior must be demonstrably connected to regulatory requirements — gaming, finance, healthcare, and similar industries where Aaron applies this logic directly (JVL's SAS protocol requirement is the concrete example).

**The "call stack" of a prompt injection can be audited.**
Aaron describes this as a very deep call stack — from a specific context injection, back through the Way, to the policy, to the requirement, to the framework. No regular developer thinks about this entire stack in real time. But the architecture means it exists and can be inspected when needed:
> *"What we have is the beginning of the framework to be able to truly actually run traceability analysis on the prompts that we're putting inside of our code that end up in commits."*

**Compliance verification without manual investigation.**
Because the chain is encoded structurally (Way references policy, policy references control, control references framework), compliance can in principle be verified programmatically rather than by manual audit.

---

## Cross-Decision Capabilities

Some capabilities emerge from the combination of multiple decisions rather than from any single one:

**Ways as an amplifier-correction mechanism** *(Decisions 2 + 5 + 7)*
A coding agent amplifies the patterns it finds in a codebase. Without correct intentions injected, it amplifies wrong patterns. Ways — by carrying the correct *why* (Decision 2), injecting it automatically when relevant (Decision 5), and keeping it current through PR-governed updates (Decision 7) — provides the corrective steering that shapes what the amplifier produces.
> *"It's an amplifier... you end up with literally an amplified version of whatever is already there."*

**Ways as a test generation foundation** *(Decisions 2 + 4)*
When coding conventions are written as Ways (Decision 2) and committed at project scope (Decision 4), those written intentions become the baseline from which unit tests can be generated. The agent can produce tests that verify adherence to stated conventions without the developer manually reading the code.
> *"If you have them written down, you have the foundation upon which all tests can be written."*

**Static analysis closed loop** *(Decisions 2 + 5)*
Ways-documented conventions can be verified by linting and static analysis. The agent runs those tools against the Ways-stated intentions (Decision 5 triggers the verification automatically; Decision 2 provides the intentions being verified), creating a self-correcting loop.
> *"The coding agent can run the linting and the static analysis and checks incredibly fast and see all the output instantly — steering from intention rather than trying to read all the code directly."*

**Self-teaching onboarding** *(Decisions 1 + 4 + 7)*
Because Ways is an overlay (Decision 1) distributed through the repo (Decision 4) and governed through PRs (Decision 7), a fully built Ways system contains enough structured reasoning that the system itself can be used to onboard new team members — the agent reads the Ways corpus and guides the new developer through it.
> *"You can use the very system that you build to teach the people how to use it as well."*

**Knowledge graph integration** *(Decisions 1 + 2)*
Because Ways are plain text files (Decision 2) in a standalone directory structure (Decision 1), the entire Ways corpus can be exported and loaded into a knowledge graph as a queryable ontology — enabling reasoning across all Ways independently of any active Claude Code session.
> *"I loaded all the ways. I took all of those ways, those files and loaded them into the graph system."*
