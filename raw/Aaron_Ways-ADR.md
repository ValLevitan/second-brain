# Ways — Architectural Decision Records

**Author:** Aaron Bockelie (reconstructed from transcripts)
**Status:** Active — iterated continuously
**Basis:** February 2026 JVL meeting transcripts — source-only, no invention
**Primary sources:**
- `GitHub_Ways-February-11-2026.md`
- `Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md` (parts 2, 3, 4)
- `Claude_Code-Dzmitry.md` (February 9)
- `Claude Code integration - continued.md` (February 3)

**Note:** These ADRs are reconstructed from Aaron's disclosed reasoning in the February 2026 transcripts. They represent the architectural decisions he made when building Ways, stated in the ADR format he uses himself.

---

## ADR-001: Build Ways as an Overlay on Claude Code

**Status:** Accepted

### Context

Claude Code is a sophisticated, rapidly evolving platform built by Anthropic. The question at the start of designing Ways was whether to modify Claude Code itself, work against it, or build on top of it.

Additionally, the system needs to be owned by individual developers — not centrally deployed. Any architecture that requires modification of the platform would create fragility, maintenance burden, and dependency on Anthropic's update cycle.

### Decision

Ways is built as an overlay on a default Claude Code installation. It does not replace or modify Claude Code; it shapes how Claude Code behaves by working within its designed extension points.

> *"If you begin to understand how this is an overlay on top of default install of Claude Code, you realize that this actually becomes a way to influence everybody who uses Claude Code in a consistent manner."*

### Consequences

**Positive:**
- Compatible with all Claude Code updates — Ways does not break when Claude Code releases new versions
- Adoptable on any Claude Code installation without platform changes
- Individually owned and maintained by each developer (analogous to compiler preferences — not managed by IT)
- Incrementally adoptable — user scope can be adopted without any project changes; project scope can be added one repo at a time

**Constraint:**
- Each developer must actively install and maintain their own Ways instance; it cannot be passively assumed to be present

---

## ADR-002: Ways Carries Only "Why" — Procedure Belongs in Skills

**Status:** Accepted

### Context

Claude Code already has a first-class feature called Skills that describes *how* to do things — specific procedures, commands, and sequences. There was a design choice about whether Ways should also carry procedure, or be restricted to something different.

The problem Ways was built to solve is a reasoning gap, not a procedure gap. Claude Code does not know *why* a team does things the way it does — the philosophy, the professional standards, the principled reasoning behind decisions. That is the missing context.

### Decision

Ways encodes only the *why* — reasoning, standards, and philosophy behind decisions. Procedure belongs in Skills. The two are complementary and work together but are maintained separately and triggered through different mechanisms.

> *"This is the way we do design work. This isn't how, which is what a skill is. This is why we do it. And this guidance is the context that's missing in most cases to steer agents in a predictable manner."*

The distinction, shown with the pull request example:
> *"See, this doesn't tell Claude how to do a pull request. It tells why we do a pull request. You see the difference?"*

The pull request Way: *"A pull request without reviewers still has value. It's a decision record, a continuous integration gate, and a muscle memory for when the project grows. Working solo without pull requests is like doing research without keeping notes."*

That is reasoning, not procedure.

### Consequences

**Positive:**
- Ways stay short and topically focused — no procedural content inflates them
- Ways remain valid across tool changes — reasoning outlasts procedure; when the GitHub CLI changes flags, the PR Way doesn't need updating
- Skills and Ways can evolve independently without conflict
- Skills and Ways can fire simultaneously, delivering both procedure and principle in one session
- Ways can be written for any domain — technology, regulatory, professional — because the restriction to reasoning makes them universally applicable

**Constraint:**
- Requires discipline in authorship — the temptation to include "how" in a Way must be actively resisted

---

## ADR-003: Ways Is Implemented as a Submodule of Hooks

**Status:** Accepted

### Context

Ways needs a delivery mechanism — a way to execute scripts and inject context into Claude Code sessions automatically. The question was where within Claude Code's architecture to anchor this.

Anthropic built a hook system into Claude Code as a designed extension point. Ways requires execution at the session lifecycle level — before or during the active conversation context.

### Decision

Ways is implemented as a submodule of hooks, residing inside `~/.claude/hooks/ways/`. All the scripts that make Ways work execute and run under the hood as hooks.

> *"Waze is not directly in here because of the way Claude has to execute. Waze is in... hooks. So Ways exists as a submodule of hooks."*

Under the Ways folder in hooks, there are sub-modules for different domains (software dev, SSH, ADR, GitHub, etc.).

### Consequences

**Positive:**
- Ways operates within Claude Code's own extension architecture — it uses the designed extension points rather than working against the platform
- Scripts execute at the right moment in Claude Code's session lifecycle
- The hooks tree provides a natural directory structure for organizing domain groups, enabling activation and deactivation by folder
- Compatible with the hook system's security model

**Constraint:**
- Ways execution is tied to the hook system's timing and behavior — any changes Anthropic makes to how hooks work affect Ways directly

---

## ADR-004: Scope Architecture Mirrors Anthropic's Own Model

**Status:** Accepted

### Context

Ways needs to work across projects consistently while also allowing project-specific customization. There was a design choice about how to structure scope — whether to invent a new scoping model or align with something already established.

Anthropic already defined two scopes for Claude Code: user scope (`~/.claude/`) and project scope (`.claude/` in each repository). Developers who understand Claude Code already understand these scopes.

### Decision

Ways mirrors Anthropic's scope model exactly:

- **User scope** (`~/.claude/hooks/ways/`) — applies to every project the developer works in, regardless of write rights. Encodes the developer's personal professional standards.
- **Project scope** (`.claude/ways/` in each repository root) — applies only to that specific repository. Encodes repo-specific conventions.

Both scopes are read and applied together in every session. They layer — neither overrides the other.

> *"Anthropic has set up this perspective of user scope and project scope. dot Claude in your home directory is your user scope. dot Claude in a project directory is project scope. A lot of the consistency of ways actually lives in user scope."*

Project-scope Ways never get automatically promoted to user scope. Project-specific conventions stay where they belong.

> *"There's repo scope ways, there's project scope and there's user scope — just the same as Claude has user scope and project scope instructions. Waze works on project scope and user scope as well."*

### Consequences

**Positive:**
- Developers already understand the mental model — no new concepts to learn
- User-scope Ways follow the developer across every project they touch, carrying their professional standards everywhere
- Project-scope Ways are committed to each repo, so any developer who clones the repo gets the project Ways automatically
- Both layers always operate together — professional identity (user scope) and project context (project scope) are both present in every session
- When all team members share the same user-scope Ways repository, team-wide behavioral consistency is enforced across all projects

**Constraint:**
- Project-scope Ways only benefit developers who clone the project; they do not exist outside the repo
- User-scope Ways require each developer to maintain their own fork — they are not centrally pushed

---

## ADR-005: Injection Is Automatic via Pattern Matching — Not Manual

**Status:** Accepted

### Context

Ways needs a trigger mechanism. The alternatives were: (1) manual invocation by the developer, or (2) automatic pattern-matched injection. The choice between them is the difference between two levels of the prompting maturity ladder Aaron described:

- **Manual invocation** = the developer remembers to call the right Way at the right time. This is a sophisticated form of static prompting — lower maturity, higher cognitive overhead.
- **Automatic injection** = the system monitors the conversation and injects the relevant Way without any developer action. This is framework-carried context — the mature operating mode.

The core purpose of Ways is to remove the human as the carrier of standing context. A system requiring manual invocation defeats that purpose.

### Decision

Ways monitors the conversational content of every Claude Code session and automatically injects the relevant Way into the agent context when the content matches a Way's trigger patterns — closely or loosely. The developer does not invoke Ways and does not see the injection.

> *"In the conversation with a coding agent, if any of these patterns match even closely or loosely, this way is injected into the context of the conversation for the agent."*

> *"This is the Waze stuff getting added in secretly in the background and you don't even see it happening because it's being injected inside of the context."*

The injection is auditable on demand. Multiple Ways can fire simultaneously when multiple patterns match.

> *"No, you never have to run it once it's set up right. It just works. It just exists."*

### Consequences

**Positive:**
- Zero cognitive overhead — the developer does not need to know what Ways exist or when to invoke them
- Relevant context always arrives at the right moment — the trigger is what is being discussed
- Multiple Ways fire simultaneously when multiple topics are active in the same session
- Developer workflow is uninterrupted — injection is silent
- Framework-carried context: the mature prompting mode where the developer states intent and the system supplies the context

**Constraint:**
- Pattern matching must be well-tuned — too loose and irrelevant Ways inject; too strict and relevant Ways don't fire
- The developer cannot easily see in real time what was injected (though it is auditable)

---

## ADR-006: Each Way Has Two Components — Text File and Optional Macro

**Status:** Accepted

### Context

A Way needs to deliver two types of content: static reasoning (what the Way always says) and responsive context (what varies based on current project conditions). Pure static text cannot detect whether ADR tooling is installed, cannot count GitHub collaborators, and cannot evaluate repository health. But adding execution to every Way would be unnecessary complexity.

### Decision

Every Way consists of two components:

1. **Text file** — plain text encoding the *why*. Human-readable, version-controlled, always injected when the Way fires.
2. **Macro** (optional) — programmatic additions that execute at runtime, generating context dynamically based on current conditions. Macros can call external tooling. They can be configured to prepend or append to the context window.

> *"The way, which is just the text file, right? It's just a — it's a prompt injection, just like a skill is in Claude Code."*

> *"It's a programmatic, responsive, deterministic prompt that creates things on the fly."*

The text file is the minimum viable Way. Macros are optional enhancements for Ways that need to respond to the current environment.

Specified macros:
- **ADR tooling detection macro** — detects whether ADR tooling is present; injects "tooling declined" if absent
- **GitHub user count macro** — calls the GitHub CLI, counts collaborators, determines solo vs. multi-user, evaluates repository health (license, description, topic, code of conduct)
- **Repository health pressure macro** — for poorly configured multi-user repos, actively prompts the agent to raise the configuration gap as an issue

### Consequences

**Positive:**
- Static text provides reliable, auditable, human-readable reasoning — any developer can read what is being injected
- Macros enable project-aware injection — the same Way can behave differently in a solo vs. team repository
- Macros enable live data integration — the GitHub state is read fresh at session startup
- Injection position (prepend vs. append) is controlled through macro configuration
- The minimum viable Way (text file only) is trivially simple to author

**Constraint:**
- Macros introduce runtime dependencies — if the GitHub CLI is unavailable, the GitHub macro fails
- Macros must be deterministic — the same environment inputs must always produce the same output

---

## ADR-007: All Ways Changes Are Governed Through Pull Requests

**Status:** Accepted

### Context

Ways governs how Claude behaves for every developer on the team in every session. If a single developer can change Ways unilaterally and immediately, there is no check on what the agent is being told to do. This creates a governance gap equivalent to allowing any developer to change shared production configuration without review.

The same PR process used for code is already understood by the team. It provides review, approval, audit trail, and rollback.

### Decision

All changes to Ways go through pull request review, using the same process as all other code changes. The PR is the governance gate for any change in Claude's injected behavior.

> *"When you're changing the ways, you can incorporate — you have a form of governance."*

When a developer discovers Claude doing something the team does not want, the corrective response is to write or revise a Way and submit it as a PR. The change becomes a team decision, not an individual workaround.

### Consequences

**Positive:**
- Changed agent behavior requires team review — no individual can unilaterally alter what Claude is instructed to do
- Complete audit trail: every change to Ways has a commit hash, PR description, reviewer approval, and diff
- Approved changes propagate to the whole team: once merged, the corrected Way is distributed to every developer who updates their fork
- Release behavior is consistent: all developers managing releases get the same versioning policy and changelog mandate injected
- Regulatory provenance: the chain from regulation to context injection can be audited through the git history

**Constraint:**
- PR review slows down Ways updates — a quick correction requires going through the full review process
- Requires that team members actively pull updates to their fork; changes do not self-distribute

---

## ADR-008: Design for Full Regulatory Provenance Traceability

**Status:** Active (foundation established; not fully complete)

### Context

In regulated industries — Aaron applies this explicitly to JVL's gaming regulatory context — the question is not only "what is Claude doing?" but "why is Claude instructed to do that, and what is that instruction based on?" Without provenance, agent behavior is ungoverned from a compliance perspective regardless of how well the Ways text is written.

No regular developer thinks about the entire regulatory stack every time they implement software. But the architecture needs to support the ability to trace through it when required.

### Decision

Ways is architected to support a complete, traceable chain from regulatory frameworks to context injection. Each level references the level above it:

```
Regulatory Framework  (e.g., US state law requiring SAS protocol for gaming machines)
  ↓
Control Requirements  (extracted from the framework — e.g., "must run SAS")
  ↓
Policy Document       (written to satisfy those requirements — e.g., "all software
                       interacting with the accounting system must speak SAS")
  ↓
Way                   (policy distilled into guidance — e.g., "when implementing
                       communication functions, use this library")
  ↓
Context Injection     (automatically fired when relevant patterns appear in session)
```

> *"I've worked from the regulatory level, the regulatory framework, all the way to context injection for doing work. And it's traceable now. Because we can say that this gets injected in this repo, which was called at this point, which was called at this policy, which was called here, which was called from here."*

Aaron acknowledges this is the beginning of the framework, not its completion:

> *"This call stack is very deep, and it's paralyzingly deep. No regular developer thinks about this whole stack every single time they're implementing software. But what we have is the beginning of the framework to be able to truly actually run traceability analysis on the prompts that we're putting inside of our code that end up in commits to be able to know what we're doing."*

### Consequences

**Positive:**
- Agent behavior is traceable to organizational policy, and policy is traceable to regulatory requirement
- The audit path exists in the commit record — Ways PRs reference the policy they implement
- Ways becomes applicable in regulated industries where software behavior must be demonstrably connected to regulatory requirements
- Compliance can in principle be verified programmatically rather than by manual audit — the chain is structural, not narrative

**Constraint:**
- The full traceability chain requires discipline at every level — if policy documents are not written, or if Ways do not reference them, the chain breaks
- Aaron is explicit that this architecture is currently the *beginning* of the framework, not a finished compliance system
- The depth of the call stack means most developers will never think about the full chain during normal work — it requires deliberate effort to construct and maintain
