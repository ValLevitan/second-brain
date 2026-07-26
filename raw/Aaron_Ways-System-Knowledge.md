# Aaron's "Ways" System — Knowledge Document

**Source:** February 2026 meeting transcripts
**Transcripts referenced:**
- `GitHub_Ways-February-11-2026.md`
- `Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md`
- `Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md`
- `Claude_set-up_GitHub_Front_End-February-11-2026-part-4.md`
- `Claude_Code-Dzmitry.md` (February 9)
- `Claude Code integration - continued.md` (February 3)
- `Introduction to Knowledge Graph Tool-part-1-February-2-2026.md` (February 2)

---

## 1. What "Ways" Is

Ways is an extension to Claude Code that Aaron built. In his own words:

> *"This is an extension to Cloud Code that I've built."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

The core purpose of Ways is to supply the **why** — the reasoning, philosophy, and standards behind decisions — which is the context that is otherwise absent from default Claude Code behavior.

> *"When we talk about ways, the way we do something — this is the way we do design work. This isn't how, which is what a skill is. This is why we do it. And this guidance is the context that's missing in most cases to steer agents in a predictable manner."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

---

## 2. Ways vs. Skills — A Critical Distinction

Aaron draws a clear line between Skills and Ways:

- **Skills** (a first-class feature built into Claude Code) = describe **how** to do something. Example: "Explain code with visual diagrams and analogies."
- **Ways** (Aaron's extension) = describe **why** we do something that way.

> *"This is built into Claude. What is not built into Claude is why we explain code this way. Why do we do this this way? What is the point of explaining code this way? Well, there's a way we do it. And this is what Waze covers."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

Example he gives of a Way (the GitHub way for pull requests):

> *"We always do pull requests. We use PR pull requests for all changes, including solo projects, and a pull request without reviewers still has value. It's a decision record, a continuous integration gate, and a muscle memory for when the project grows. Working solo without pull requests is like doing research without keeping notes."*

Then he explains:

> *"See, this doesn't tell Claude how to do a pull request. It tells why we do a pull request. You see the difference?"*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

---

## 3. What a Way Is Made Of

A Way has two components:

1. **The way itself** — a plain text file. Aaron describes it as:

   > *"The way, which is just the text file, right? It's just a — it's a prompt injection, just like a skill is in Cloud Code."*
   > *(GitHub_Ways-February-11-2026.md)*

2. **Macros** — programmatic additions to the way that execute dynamically. Macros can be set to **prepend** (inject at the beginning of context) or **append** (inject at the end).

   > *"Macros says: execute any macros for this way at the beginning rather than the end of the context."*
   > *(GitHub_Ways-February-11-2026.md)*

   Macros are not static — they inspect the environment and create conditional, responsive output:

   > *"It's a programmatic, responsive, deterministic prompt that creates things on the fly."*
   > *(GitHub_Ways-February-11-2026.md)*

   **Example — the ADR macro:** Detects whether the relevant tooling exists in a project. If not, it tells the way to inject: *"Tooling declined for this project. Remove the no cloud tooling flag to enable."*

   **Example — the GitHub macro:** Uses the GitHub CLI to count the number of users, determines whether it's a solo or collaborative project, evaluates repository health (has license, description, topic, code of conduct), and injects all of that as context.

   > *"It will eventually harass the coding agent a lot if it's a multi-user project that's poorly configured and say you should probably think about fixing this."*
   > *(GitHub_Ways-February-11-2026.md)*

---

## 4. How Ways Are Triggered (Injection Mechanism)

Ways are not manually invoked. They are matched against what the developer says and injected automatically and invisibly into the context of the conversation:

> *"In the conversation with a coding agent, if any of these patterns match even closely or loosely, this way is injected into the context of the conversation for the agent."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

For example, when saying "let's do a release":

> *"As soon as you say those words — you say 'let's make a release' — this gets injected, the make way gets injected, the GitHub way gets injected. It has all of this understanding of the way we do it, and you don't have to type any of this stuff in because it's there already. And then you have the tools and the skills — it knows exactly what commands to run and how to run them for your particular release cycle."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

The developer does not see the injection happening:

> *"Out-of-the-box [Claude Code] doesn't do this. It just sits there and waits for the next thing for you to tell it what to do. This is the Waze stuff getting added in the secretly in the background and you don't even see it happening because it's being injected inside of the context."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md)*

Aaron notes you can audit the injection if needed.

---

## 5. Technical Architecture and Location

**In user scope (`~/.claude/`):**

> *"Waze is not directly in here because of the way Claude has to execute. Waze is in... hooks. So Ways exists as a submodule of hooks."*
> *(GitHub_Ways-February-11-2026.md)*

Under the Waze folder in hooks, there are all the scripts that make Waze work — executing and running under the hood with all the hooks. Under Waze itself, there are sub-modules for different domains of ways (e.g., `software dev`, `SSH`, `ADR`, `GitHub`).

**In project scope (`.claude/` in each repository):**

> *"In the root of each repository, or technically in the root of every directory you want guidance in, you have a `.claude` directory in your repo. And the `.claude` repo directory is where project scope ways can exist and are sensed and used."*
> *(GitHub_Ways-February-11-2026.md)*

**The gitignore pattern Aaron uses:**

> *"Commit Ways, ignore developer local files... We're gonna get Waze in here, but we're gonna ignore these things. This way you keep your local to-do's and the Ways make it into the repo."*
> *(GitHub_Ways-February-11-2026.md)*

---

## 6. The Scope Model: User, Project, and Repo

Aaron maps Ways directly to the scoping model that Anthropic built into Claude Code:

> *"Anthropic has set up this perspective of user scope and project scope. dot Claude in your home directory is your user scope. dot Claude in a project directory is project scope."*
> *(GitHub_Ways-February-11-2026.md)*

And Waze works on both:

> *"There's repo scope ways, there's project scope and there's user scope — just the same as Claude has user scope and project scope instructions. Waze works on project scope and user scope as well."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md)*

**User scope Ways** encode a developer's consistent professional standards that apply across *every* project they touch:

> *"These are user scope, meaning every project you interact with, whether you have rights to do it or not — it's going to kind of do that, because as a professional software engineer, I hate working in GitHub repos that aren't well configured, and so I'm forcing Claude to take on my way of doing things. And my way is the user way."*
> *(GitHub_Ways-February-11-2026.md)*

**Project scope Ways** are specific to a given repository and layer on top of user scope:

> *"Waze is what incorporates both. It reads both."*
> *(GitHub_Ways-February-11-2026.md)*

Both are injected into the session together.

---

## 7. Ways as Governance

Aaron explains that Ways, managed through pull requests, become a form of governance for the team:

> *"When you're changing the ways, you can incorporate — you have a form of governance."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

The **release way** is his concrete example of governance in action:

> *"If we have a single place where we can define the release way, it's right here... I want to keep a changelog. I want a version bump where features and breaking changes — any feature is a minor and fixed docs is patch versions. That's my rules. They're very simple. This is a form of governance because if you have this one on everybody's computer cloned with this exact document... those that are managing releases of some kind will have a consistent messaging about how releases are done injected into their work."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

When someone finds a behavior from Claude that the team doesn't like, the resolution is to write a new way:

> *"You can correct it by creating your own way for it. You say 'actually this is the way we do it' and I need to add this way. You add this way to your local installation, which is a git repo clone of the Waze system."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

---

## 8. The Regulatory Provenance Chain

Aaron describes a full traceability chain from regulatory frameworks all the way down to prompt injection:

> *"The very beginning of any of the way you do things is based usually on regulatory perspectives. It's based on a specification."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

The chain he describes, step by step:

1. **Regulatory framework** (external — e.g., SOC 2, or a state law requiring SAS protocol for gaming machines)
2. **Control requirements** extracted from that framework
3. **Policy document** written to satisfy those requirements
4. **Way** — the policy distilled and compiled into guidance
5. **Context injection** — the way is injected into the agent when relevant patterns appear in conversation

In his words:

> *"I've worked from the regulatory level, the regulatory framework, all the way to context injection for doing work. And it's traceable now. Because we can say that this gets injected in this repo, which was called at this point, which was called at this policy, which was called here, which was called from here."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

He also notes:

> *"This call stack is very deep, and it's paralyzingly deep. No regular developer thinks about this whole stack every single time they're implementing software. But what we have is the beginning of the framework to be able to truly actually run traceability analysis on the prompts that we're putting inside of our code that end up in commits to be able to know what we're doing."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

He applies this explicitly to JVL's gaming context:

- Regulatory framework: a US state law requiring SAS (Slot Accounting System) protocol
- Requirement: "must run SAS"
- Policy: "all software interacting with the accounting system must speak SAS"
- Way: "any configuration tools — the way we do this is we use this library"
- Agent context: "when implementing communication functions, use this library"

---

## 9. Ways as an Overlay — What It Does and Doesn't Change

Ways is an overlay on top of a default Claude Code install. It doesn't replace Claude Code; it shapes how Claude Code behaves:

> *"If you begin to understand how this is an overlay on top of default install of Claude Code, you realize that this actually becomes a way to influence everybody who uses Claude Code in a consistent manner."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

Aaron also uses an analogy to draw the boundary of responsibility clearly:

> *"You are responsible for accepting the output of this because it's on you. Machines are not accountable."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

And on ownership:

> *"You wouldn't let Andrei manage your VS Code preferences or your compiler directive preferences, right? The language model is a type of compiler. And pretty much every software engineer ever doesn't let the IT department manage their compiler configuration."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

---

## 10. Activating and Deactivating Sections of Ways

Ways can be segmented by domain, and specific sections can be turned on or off:

> *"You can activate and deactivate sections of way sub-areas. So if you could deactivate the software engineering ways group and enable the legal or the finance ways if you wanted to."*
> *(GitHub_Ways-February-11-2026.md)*

---

## 11. How Aaron Maintains and Updates Ways

Aaron makes commits to Ways continuously:

> *"About every day I'm making commits — 4th, 5th, 6th, 9th, 11th. I don't know when it was cloned, but there's a lot of changes... I'm constantly tuning and adjusting this against all of the other projects and work I'm doing."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

He is explicit that it is not finished or perfect:

> *"I'm not saying it's perfect and I'm not saying it's the one true way. But I'm saying this is the first one."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

And from the Feb 9 session:

> *"If you want to adopt the Waze system I have for cloud code, make sure that's working well. I'm updating it constantly and kind of improving it as I go. Doesn't mean you have to grab it every day, but just, you know, start running that tool as yours."*
> *(Claude_Code-Dzmitry.md)*

---

## 12. How the Team Should Adopt Ways

Aaron's instructions to the JVL team:

1. **Fork the Ways repo** — each developer must maintain their own fork. Nobody can passively receive it from IT.

   > *"You can't just assume it's installed and configured. You have to know it exists."*
   > *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

2. **Keep it up to date** — the version at any given time may be outdated relative to what Aaron has:

   > *"I know it's outdated because I daily fix this thing and improve it as I learn and create stuff. It is dynamic and happening."*
   > *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

3. **Modify it for your context** — the release way and other ways should be adapted to JVL's practices:

   > *"You guys should change the ways when you fork it to make it your release way of course."*
   > *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

4. **Contribute to it through PRs** — adding a new way goes through the same PR process as code:

   > *"Now when you're changing the ways, you can incorporate — you have a form of governance."*
   > *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

5. **User scope = shared from Aaron's repo; project scope = per repo.** Pavel's initial misunderstanding was that project ways would be injected into the user layer. Aaron corrected this:

   > *"Project ways go into the project layer."*
   > *(GitHub_Ways-February-11-2026.md)*

6. **Understand the system, not just use it:**

   > *"The sooner you can sort of reproduce what I'm saying and essentially say and believe what I'm saying, or your own flavour of it — now you can codify all of this in git repos in ways of work in examples that you own."*
   > *(Claude_Code-Dzmitry.md)*

---

## 13. Ways and Knowledge Graphs

On February 2, Aaron demonstrated loading the entire Ways document corpus into a knowledge graph:

> *"You know the ways from the Cloud Code config that I talked about last week? I loaded all the ways. I took all of those ways, those files and loaded them into the graph system. I also took a whole discussion about operating the enterprise as a graph and some other conceptual ideas too."*
> *(Introduction to Knowledge Graph Tool-part-1-February-2-2026.md)*

The knowledge graph system has a dedicated ontology called **"Hooks and Ways"** that holds all hooks and ways from Claude Code. This allows the Ways corpus itself to be queried as a knowledge base — for example: *"Can you tell me how the code review way might be supported by the graph as an operating model?"*

---

## 14. Ways as a Prerequisite for ADR-Driven Work

Aaron treats getting Ways configured as the necessary condition for being able to leverage Architectural Decision Records (ADRs) effectively:

> *"Once you can get the Waze configured, we'll be able to leverage architectural decision records, and either back-port them into the code base or begin creating new ones and sort of evolve this a little bit so you can begin to use these tools more effectively without having to type stuff in all the time."*
> *(Claude Code integration - continued.md)*

When Aaron converted a repo live to the Waze system in part-3 of the Feb 11 session, the first action the system took was to write an ADR for the adoption of Ways itself:

> *"Did we write an inaugural ADR documenting that the Waze adoption itself, it's meaningful architectural process decision worth recording? Yes, absolutely."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md)*

Claude also queried the repo (from Claude_Code-Dzmitry.md) and reported:

> *"There's nothing in the project's ADRs, ways, governance controls, or lint configuration that sets file size or line count thresholds."*

This shows that Ways, ADRs, and governance controls are treated as a coherent, queryable layer that Claude Code can inspect and reason about.
