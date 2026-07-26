# Aaron's Architectural Thinking Behind "Ways"

**Source:** February 2026 meeting transcripts only
**Transcripts referenced:**
- `GitHub_Ways-February-11-2026.md`
- `Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md`
- `Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md`
- `Claude_set-up_GitHub_Front_End-February-11-2026-part-4.md`
- `Claude Code integration - continued.md` (February 3)
- `Claude_Code-Dzmitry.md` (February 9)
- `Introduction to Knowledge Graph Tool-part-1-February-2-2026.md` (February 2)

---

## The Problem Aaron Was Actually Solving

To understand the architecture of Ways, you first have to understand the problem Aaron diagnosed. He is not solving a configuration problem. He is solving a **context gap** problem.

He describes the situation clearly: Claude, for all its capability, knows nothing about you.

> *"While it might have been trained on all of humanity's information, it actually knows nothing of your life. It does not know that Irina has worked in the games industry for 20 plus years. It does not know that Igor does UX design for back-end platforms. It does not know that Sasha focuses on game engine frameworks... They are just systems that predict information."*
> *(Claude Code integration - continued.md)*

And more sharply:

> *"You are in a way like the adult in the room, understanding the real problem at hand. It is a financial, social, political problem that is being solved. It has nothing to do with tech at some point."*
> *(Claude Code integration - continued.md)*

So Aaron's starting point is: the human brings the intent, the history, the professional judgment. The machine brings the execution speed. The gap between them is **context** — specifically, the standing, persistent, structured context that should be present in every session without the human having to re-explain it every time.

Ways is the answer to that gap.

---

## The Mental Model: A Language Model as a Compiler

Aaron builds his entire architectural thinking on a specific analogy that he returns to repeatedly: **the language model is a compiler for natural language**.

He lays this out formally:

> *"A language model is a machine that compiles natural language into source code. Natural language into source code is something that's never been able to be done before."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

> *"It takes input that you speak naturally in your own language... and builds an intermediate representation of what you spoke about, optimises what you're thinking, and emits structured output. It's not deterministic, it's probabilistic, and there's no formal correctness guarantees."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

This matters architecturally because it defines how Aaron thinks about *what goes in* to Claude. If the machine is a compiler, then the input has to be prepared the way you'd prepare input for a compiler — clean, structured, purposeful, unambiguous where possible. And just as you don't hand-optimize machine code every time you run a program, you don't want to hand-type your professional standards and preferences into Claude every session.

He makes the compiler analogy explicit when he talks about ownership:

> *"You wouldn't let Andrei manage your VS Code preferences or your compiler directive preferences, right? The language model is a type of compiler. And pretty much every software engineer ever doesn't let the IT department manage their compiler configuration."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

This single analogy explains: why Ways is each developer's personal responsibility (not IT's), why it must be forked and individually owned, and why it must be kept current.

---

## The Core Architectural Distinction: Why vs. How

Once Aaron establishes that Claude is a compiler that needs prepared input, the next architectural question is: what kind of input does it already have, and what is missing?

His answer is that Claude Code already handles *how* via Skills — a built-in feature. What is missing is *why*.

> *"Skills are essentially a description of how to do something... What is not built into Claude is why we explain code this way. Why do we do this this way? What is the point of explaining code this way? Well, there's a way we do it. And this is what Waze covers."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

> *"This guidance is the context that's missing in most cases to steer agents in a predictable manner."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

The distinction is not cosmetic. It is the foundational design decision. Skills are procedural (steps, commands, sequences). Ways are principled (reasoning, values, standards, professional judgment). Aaron explicitly says:

> *"See, this doesn't tell Claude how to do a pull request. It tells why we do a pull request. You see the difference?"*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

The pull request Way he cites: *"A pull request without reviewers still has value. It's a decision record, a continuous integration gate, and a muscle memory for when the project grows. Working solo without pull requests is like doing research without keeping notes."* — this is reasoning, not procedure.

---

## The Prompting Maturity Model

Before designing the mechanism for Ways, Aaron describes a maturity curve for prompting. This reveals why he chose automatic injection over manual prompting.

He describes three levels:

1. **Lowest — static prompt:** "Just type it in." Full burden on the human. Unpredictable output.
2. **Medium — dynamic prompt:** "Go to Jira and read the user story, then do it for me." Reduced burden, but still requires active steering.
3. **Mature — framework-carried context:** The tooling framework, tests, linters, doc strings, ADRs, Ways — all carry the context for the human. You type: "Add a users endpoint." It already knows everything it needs to know.

He describes this explicitly:

> *"Add a slash users endpoint. It's already known — the context is there. You already have linters, you have docstrings, you have potentially REST API docs in there, type checks, integration tests — so the framework carries the context rather than the person carrying the context."*
> *(Claude Code integration - continued.md)*

And on the investment required to reach that state:

> *"You have to actually put the work into the tools that you need to make to steer it before you can actually use it in a way that makes sense."*
> *(Claude Code integration - continued.md)*

Ways is the architectural embodiment of that third level. It removes the human as the carrier of standing context and transfers that responsibility to the system itself.

He also describes the bootstrapping logic explicitly — what he calls preparing the tools to build the tools:

> *"You're starting by sharpening your knives. You don't butcher the meat with dull knives... You're starting by sharpening your knives, you don't butcher the meat with dull knives. We're going to make all these tools work first."*
> *(Claude Code integration - continued.md)*

> *"Make a test script that does this thing, set up a make file, give me a linting configuration, write a pipeline — you're preparing the tools to build the tools to build the tools. You know what I mean by this? There's a recursion here."*
> *(Claude Code integration - continued.md)*

Ways itself is built through this same logic — it is a tool for building tools, and it must exist before the development workflow it enables can function.

---

## Thinking Like a Data Scientist: Signal-to-Noise Architecture

Aaron's second major framing — which he calls as important as everything else — is that developers must think like data scientists when designing what goes into the context machine.

He states this as a governing principle:

> *"You have to maximize the signal-to-noise ratio. This means that everything you say is information. Everything."*
> *(Claude Code integration - continued.md)*

This leads directly to design decisions about what Ways contains and how it is organized. Specifically:

**Clean before feeding:**
> *"You can't just take the raw data... you have to structure your raw data in certain ways. You need to create this into architectural decisions, requirements. You can structure this into tests."*
> *(Claude Code integration - continued.md)*

**Label your data:**
> *"You need to use a labeling structure that makes sense. When you write down architectural decisions, when you write down documentation, you use labels."*
> *(Claude Code integration - continued.md)*

**Separate by purpose:**
> *"You can't talk about the back end and the front end in the same conversation... You need to separate by purpose."*
> *(Claude Code integration - continued.md)*

**Iterate and correct:**
> *"When you catch that thing doing the wrong thing, you have to pause and fix the problem right there... That is likely the next thing you're going to fix in your context. You've got to write a bug, literally write a bug for your context management to make sure that you cover that gap next time."*
> *(Claude Code integration - continued.md)*

These are not abstract principles — they are the design constraints of the Ways system. Ways files are short and topically focused (not monolithic). They are labeled (matched by keyword pattern). They are separated by domain (software dev, ADR, GitHub, release, etc.). And they are iteratively improved as Aaron encounters failures.

He also makes the developer role explicit:

> *"You are not a developer anymore, only — you are a data engineer for your AI teammate."*
> *(Claude Code integration - continued.md)*

---

## The Burn Barrel: Why Input Preparation Is the Core Job

Aaron uses an analogy about fire and a burn barrel to explain why the *preparation* of context is the central engineering task:

> *"We can think of the AI agent as the burn barrel. It's the fire where we're dealing with things and we have to process this. We have to cut it to the right size. We have to curate our data... you can't throw the whole tree into the fire pit. You can't give it incorrectly processed stuff. You have to feed it properly prepared information."*
> *(Claude Code integration - continued.md)*

> *"Fire doesn't care how big your tree was, it only cares what you feed it, and it's the prep work for this that makes it useful... fire is stupid. It can just do the wrong things when incorrectly used. An AI machine processing of intelligence is stupid and can do absolutely the wrong thing when improperly used."*
> *(Claude Code integration - continued.md)*

The architectural implication: you cannot fix Claude's behavior by complaining about the output. You fix it by changing what you feed it. Ways is the system for engineering what gets fed in — reliably, consistently, and without manual effort each session.

---

## The Scope Architecture: Mirroring Claude's Own Model

One of Aaron's deliberate architectural choices is to mirror the scope model that Anthropic itself built into Claude Code. This is not accidental.

Anthropic's model: user scope (home `~/.claude/`) and project scope (`.claude/` in each repo).

Aaron's Ways extends this same model:

> *"Anthropic has set up this perspective of user scope and project scope. dot Claude in your home directory is your user scope. dot Claude in a project directory is project scope. A lot of the consistency of ways actually lives in user scope."*
> *(GitHub_Ways-February-11-2026.md)*

> *"There's repo scope ways, there's project scope and there's user scope — just the same as Claude has user scope and project scope instructions. Waze works on project scope and user scope as well."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md)*

The reasoning behind this choice:

- **User scope** = professional identity. The standards, preferences, and reasoning a developer brings to *every* project they touch. Aaron describes this as "my way of doing things" that he "forces" Claude to adopt as the user way.
- **Project scope** = project-specific specialization. The decisions, constraints, and practices that are specific to a given codebase.

By mirroring Anthropic's scope model, Aaron ensures that Ways is immediately coherent to anyone who understands how Claude Code itself works. The architecture doesn't introduce new concepts — it extends existing ones.

---

## The Mechanism: Pattern-Matched Automatic Injection

The most consequential architectural decision in Ways is the **injection mechanism**: Ways files are not called manually. They are matched against conversational content and injected automatically.

> *"In the conversation with a coding agent, if any of these patterns match even closely or loosely, this way is injected into the context of the conversation for the agent."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

> *"As soon as you say 'let's make a release,' this gets injected — the make way gets injected, the GitHub way gets injected. It has all of this understanding of the way we do it, and you don't have to type any of this stuff in because it's there already."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

The developer does not see this happening:

> *"Out-of-the-box [Claude Code] doesn't do this. It just sits there and waits for the next thing for you to tell it what to do. This is the Waze stuff getting added in the secretly in the background and you don't even see it happening because it's being injected inside of the context."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md)*

This design decision flows directly from the maturity model. If the goal is to reduce human burden — to get from "type everything every session" to "add a users endpoint" — then the injection must be automatic. A system that requires the developer to manually invoke a Way defeats the purpose.

---

## Macros: Making the Injection Responsive

Static text injection has a limit: it cannot respond to the current environment. Aaron solves this with macros.

> *"Waze also supports macros... macros says: execute any macros for this way at the beginning rather than the end of the context. It's a programmatic, responsive, deterministic prompt that creates things on the fly."*
> *(GitHub_Ways-February-11-2026.md)*

The architectural purpose of macros is to make the injected context *aware of the project it is being injected into*. Two examples Aaron describes:

1. **ADR macro:** Detects whether ADR tooling exists in the project. If it does, it injects "ready to go." If it doesn't, it injects: "Tooling declined for this project. Remove the no cloud tooling flag to enable." The Way becomes project-aware without the developer doing anything.

2. **GitHub macro:** Uses the GitHub CLI to count users, determines if the project is solo or collaborative, evaluates repository health (license, description, topics, code of conduct). The Way then injects appropriate guidance based on actual conditions rather than assumptions.

On the ambition of the GitHub macro:

> *"It will eventually harass the coding agent a lot if it's a multi-user project that's poorly configured and say you should probably think about fixing this."*
> *(GitHub_Ways-February-11-2026.md)*

Macros are the architectural answer to the problem that fixed text can become stale or inapplicable. The macro layer makes the system adaptive without requiring human intervention.

---

## The Governance Architecture

Aaron frames Ways changes through the same pull request process used for code. This is an intentional architectural choice, not a workflow suggestion.

> *"When you're changing the ways, you can incorporate — you have a form of governance."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

The reasoning: if Ways is the system that governs how Claude behaves for your team, then changes to Ways must themselves be governed. Using PRs for Ways changes creates a feedback loop where:

1. A developer encounters Claude doing something wrong.
2. They create a new Way or modify an existing one.
3. The change goes through PR review.
4. The team collectively approves the new behavior.
5. The approved behavior is now consistent for everyone.

He makes the governance implication concrete with the release way example:

> *"If we have a single place where we can define the release way, it's right here... This is a form of governance because if you have this one on everybody's computer cloned with this exact document and people are regularly pairing with their coding agent... those that are managing releases will have a consistent messaging about how releases are done injected into their work."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

---

## The Regulatory Provenance Chain

Aaron's most architecturally ambitious thinking is about traceability — the ability to trace from a prompt injection all the way back to a regulatory requirement.

He describes a full chain:

1. **Regulatory framework** (external standard, e.g., SOC 2, or a state gaming law requiring SAS protocol)
2. **Control requirements** extracted from that framework
3. **Policy document** written to satisfy those requirements
4. **Way** — the policy distilled into guidance
5. **Automatic injection** when relevant patterns appear

> *"I've worked from the regulatory level, the regulatory framework, all the way to context injection for doing work. And it's traceable now. Because we can say that this gets injected in this repo, which was called at this point, which was called at this policy, which was called here, which was called from here."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

He acknowledges this is aspirational, not finished:

> *"This call stack is very deep, and it's paralyzingly deep. No regular developer thinks about this whole stack every single time they're implementing software. But what we have is the beginning of the framework to be able to truly actually run traceability analysis on the prompts that we're putting inside of our code that end up in commits to be able to know what we're doing."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

> *"I'm not saying it's finished. I'm just working on it."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

The architectural implication: Ways is not just a developer convenience. In its intended final form, it is a **compliance and audit system** for AI-assisted software development. Every prompt injection is traceable to a policy, every policy to a requirement, every requirement to a framework.

---

## The Living System: Why Aaron Commits to It Daily

Aaron is explicit that Ways is not a finished product to be deployed once. It is a living system he actively develops:

> *"About every day I'm making commits — 4th, 5th, 6th, 9th, 11th... I'm constantly tuning and adjusting this against all of the other projects and work I'm doing."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

> *"I'm updating it constantly and kind of improving it as I go."*
> *(Claude_Code-Dzmitry.md)*

> *"I'm not saying it's perfect and I'm not saying it's the one true way."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

The reason for this approach: Aaron applies the same iterative feedback loop to Ways that he advocates for all AI-assisted work. When Claude does something unexpected or wrong on a project, the diagnosis goes into the Ways system as a fix. He describes this explicitly as the correct response to Claude misbehaving:

> *"When you catch that thing doing the wrong thing, you have to pause and fix the problem right there... That is likely the next thing you're going to fix in your context."*
> *(Claude Code integration - continued.md)*

Ways is therefore the permanent record of accumulated corrections — a system that gets better the more it is used, and that carries the full history of what has been learned.

---

## What Ways Is Not

Two things Aaron is careful to distinguish:

**Ways is not a substitute for the human:**
> *"You are responsible for accepting the output of this because it's on you. Machines are not accountable."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

**Ways is not a replacement for Claude Code — it is an overlay:**
> *"If you begin to understand how this is an overlay on top of default install of Claude Code, you realize that this actually becomes a way to influence everybody who uses Claude Code in a consistent manner."*
> *(Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md)*

---

## The Architectural Idea, Condensed

Working entirely from Aaron's own words, his architectural thinking for Ways can be stated as:

The LLM is a natural language compiler. Like any compiler, it produces output proportional to the quality of its input. The human is the adult in the room who holds the real intent, the professional history, the regulatory constraints — none of which Claude knows. The gap between human intent and consistent, predictable agent behavior is a context gap. That context gap must be closed not by the human typing more, but by a persistent, structured, auto-injecting, scope-aware, pattern-matched system that carries the professional reasoning — the *why* — into every session automatically. That system must be personally owned (not managed by IT), PR-governed (so the team controls what it encodes), iteratively improved (it gets better as failures are discovered), and traceable all the way back to the regulatory and professional standards it encodes. That system is Ways.
