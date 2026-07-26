# Ways — Disclosed Capabilities

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

## 1. Context Injection

**1.1 Automatic pattern-matching injection**
Ways monitors the conversation in Claude Code and automatically injects the relevant way when conversational content matches a way's configured patterns — closely or loosely.
> *"In the conversation with a coding agent, if any of these patterns match even closely or loosely, this way is injected into the context of the conversation for the agent."*
> *(part-2)*

**1.2 Multiple simultaneous injections**
Multiple ways can fire at the same time. When a trigger phrase matches more than one way, all matching ways are injected together.
> *"As soon as you say 'let's make a release' — the make way gets injected, the GitHub way gets injected."*
> *(part-2)*

**1.3 Silent, invisible injection**
The injection happens inside the context without the developer seeing it.
> *"This is the Waze stuff getting added in the secretly in the background and you don't even see it happening because it's being injected inside of the context."*
> *(part-3)*

**1.4 Auditable injection**
The injection can be audited when needed.
> *"I'll show you how to audit it in a second."*
> *(part-3)*

**1.5 Zero-run operation**
Once set up, Ways requires no manual invocation. It runs automatically on every session.
> *"No, you never have to run it once it's set up right. It just works. It just exists."*
> *(part-3)*

**1.6 Injection position control (prepend/append via macros)**
Ways supports macros that can be set to inject either at the beginning or the end of the context window.
> *"Macros says: execute any macros for this way at the beginning rather than the end of the context."*
> *(GitHub_Ways)*

---

## 2. Scope Management

**2.1 User-scope ways**
Ways stored in the user's home `~/.claude/` directory apply to every project that developer touches, regardless of whether they have write rights to that project.
> *"These are user scope, meaning every project you interact with, whether you have rights to do it or not — it's going to kind of do that."*
> *(GitHub_Ways)*

**2.2 Project-scope ways**
Ways stored in a project's `.claude/` directory apply only to that specific repository.
> *"dot Claude in a project directory is project scope."*
> *(GitHub_Ways)*

**2.3 Simultaneous dual-scope operation**
Both user-scope and project-scope ways are read and applied together in every session.
> *"Waze is what incorporates both. It reads both."*
> *(GitHub_Ways)*

**2.4 Project-specific ways that never enter user scope**
When converting a repo, Ways creates project-specific ways that are scoped only to that repo and explicitly not incorporated into user scope.
> *"We've created some specific ways for this project that I never want to incorporate into my user scope because it's specific for this project. So we have a build way, a front end way, and a micro front end way for this."*
> *(part-3)*

**2.5 Three-scope architecture**
Aaron distinguishes three scopes in total: repo scope, project scope, and user scope.
> *"There's repo scope ways, there's project scope and there's user scope."*
> *(part-3)*

---

## 3. Macro System

**3.1 Programmatic, runtime-responsive prompt generation**
Macros execute at runtime and generate context dynamically based on current conditions, not fixed text.
> *"It's a programmatic, responsive, deterministic prompt that creates things on the fly."*
> *(GitHub_Ways)*

**3.2 ADR tooling detection macro**
The ADR way has a macro that detects whether ADR tooling exists in the current project. If it does not exist, it injects a message telling Claude: "Tooling declined for this project. Remove the no cloud tooling flag to enable."
> *"This macro is going to detect whether the tooling exists in a project and tell it in the way when you talk about ADR as to whether it's ready to go and tell it tooling declined for this project."*
> *(GitHub_Ways)*

**3.3 GitHub user count macro**
The GitHub way has a macro that calls the GitHub CLI to count the number of collaborators in the repository, then determines whether the project is a solo or multi-user project and injects that determination into the context.
> *"A macro that looks at the project scope. It counts. It uses the GitHub command line tool to count the number of users in there and figures out whether it's a solo project or a collaborative project and tells that to the tool."*
> *(GitHub_Ways)*

**3.4 Repository health scoring macro**
The GitHub macro evaluates repository health across several dimensions and injects the health status into context.
> *"It also gives the repository help. Is it well configured or poorly configured... Has a license, has description, topic, code of conduct."*
> *(GitHub_Ways)*

**3.5 Persistent repo quality enforcement**
For multi-user projects that are poorly configured, the GitHub macro actively pressures the agent to raise this as an issue.
> *"It will eventually harass the coding agent a lot if it's a multi-user project that's poorly configured and say you should probably think about fixing this."*
> *(GitHub_Ways)*

---

## 4. Known Ways (Domains Disclosed)

Aaron disclosed the following specific ways by name or description:

**4.1 GitHub way**
Covers all GitHub interactions across all projects. Encodes why pull requests are always used (even on solo projects), pull request review practices, and repository health standards. Has both a base text file and the GitHub macro (user count, repo health).
> *"Here's the way for the general way for GitHub, for all GitHub, for all projects. Works this way."*
> *(GitHub_Ways)*

**4.2 ADR way**
Covers how architectural decision records should be created and maintained. Has a macro that detects whether ADR tooling is present in the project.
> *"Here's the way for ADR."*
> *(GitHub_Ways)*

**4.3 SSH way**
> *"If I go into SSH, here's the way for SSH."*
> *(GitHub_Ways)*

**4.4 Release way**
Encodes the release versioning policy: major for breaking changes, minor for features, patch for fixes and docs. Also mandates a changelog. This is the governance document for releases — it ensures every developer who uses Ways has consistent release behavior injected when they discuss releasing.
> *"I want to keep a changelog. I want a version bump where features and breaking changes — any breaking change is major. Any feature is a minor and fixed docs is patch versions."*
> *(part-2)*

**4.5 Documentation way**
Encodes the standard for how documentation is written: Markdown, language-appropriate docstrings in code, Mermaid for diagrams.
> *"Here's the documentation way. We write this in markdown, we use language appropriate docstrings and code, and we use Mermaid for diagrams. They're not arbitrary choices."*
> *(part-2)*

**4.6 Design way**
Encodes the reasoning and standard for how design work is done within Claude Code.
> *"Here is the way we do design work. When we start thinking about how to design something within Claude Code by creating a design, an architecture, something like that — this is the way we do it."*
> *(part-2)*

**4.7 Code review way**
Exists as a named way that was loaded into the knowledge graph for querying.
> *"We have a code review way that you've seen it. It's a file that's in there."*
> *(Knowledge Graph, part-1)*

**4.8 Build way / Front End way / Micro Front End way (project-scope)**
These are project-specific ways created during the live repo conversion demo. They capture webpack federation patterns and micro front end specifics for a particular repo and are never promoted to user scope.
> *"We have a build way, a front end way, and a micro front end way for this."*
> *(part-3)*

**4.9 Webpack federation way**
A specific way that fires when anyone mentions Webpack, remote entries, or related concepts.
> *"This is a very specific way to webpack federation. Short and sweet, it has the match for what we're looking for. So if anybody talks about Webpack or remote entries or whatever, it's going to get injected."*
> *(GitHub_Ways)*

**4.10 Legal ways (disclosed as available activation group)**
> *"You could deactivate the software engineering ways group and enable the legal or the finance ways if you wanted to."*
> *(GitHub_Ways)*

**4.11 Finance ways (disclosed as available activation group)**
> *(same reference as 4.10)*

**4.12 Technology/framework-specific way (Spring example)**
Any technology or framework used in a project can have its own named way. Aaron live-creates a "Spring way" alongside a "Spring skill" as a paired example. The way encodes why the team uses Spring (consistency, repeatability, compatibility with existing code); the skill encodes how to write Spring code correctly. Both get injected into context automatically via their respective trigger mechanisms.
> *"I could create a Spring way in here... We use Spring because it simplifies the framework... the two combos of this get injected into the context automatically while you're working on stuff."*
> *(Claude_Code-Dzmitry.md)*

---

## 5. Repository Setup and Conversion

**5.1 Instant repo conversion from a single prompt**
Aaron can clone a repo and, with a single prompt, trigger the full Waze setup process. The result is a fully configured project.
> *"I could clone this and instantly change this to work with Waze."*
> *(part-3)*

**5.2 Multi-agent simultaneous repo analysis**
When initiating Waze setup, multiple concurrent coding agents are spawned to review the repo simultaneously.
> *"We get 123 different coding agents simultaneously reviewing the repo and looking at the ways."*
> *(part-3)*

**5.3 Automatic ADR domain detection**
Ways queries the actual project content and proposes which ADR domains make sense for that specific repo.
> *"What ADR domains make sense for this front end monorepo? The template ships with this. I'd suggest domains that reflect the actual decision space here. Is it front end focused on the architecture, shared dependencies, patterns, UI framework, theming components? We have core front end infrastructure and integration."*
> *(part-3)*

**5.4 Conversion of existing CLAUDE.md into the Waze system**
An existing monolithic CLAUDE.md file can be decomposed and redistributed into focused, topical Ways files.
> *"The current Claudmd is doing everything. Architecture, docs, import conventions, webpack patterns, MF set guides. Should we restructure it? Yes, we're going to slim down and move to the Waze system."*
> *(part-3)*

> *"We've taken apart the original Claude document that you have and put it into Waze."*
> *(part-3)*

The problems this solves (as stated by the system during the demo):
- Flat guidance: all context was loaded regardless of what you're working on
- No decision trail: past architectural choices weren't recorded with reasoning
- Onboarding friction: new contributors got a wall of text rather than contextual, relevant guidance

**5.5 Uplift of existing ad-hoc commands into Ways**
Commands that a developer has manually committed in a `.claude` directory can be "uplifted" into proper Ways.
> *"We can take his ways and uplift them in or his commands and uplift them into ways."*
> *(part-3)*

**5.6 Gitignore configuration**
Ways automatically configures the gitignore to commit Ways files while excluding developer-local files (to-do lists, etc.).
> *"Commit Ways, ignore developer local files... This way you keep your local to-do's and the Ways make it into the repo."*
> *(GitHub_Ways)*

**5.7 Inaugural ADR creation**
On setup, Ways creates the first ADR documenting the adoption of the Waze system itself as an architectural decision.
> *"Did we write an inaugural ADR documenting that the Waze adoption itself, it's meaningful architectural process decision worth recording? Yes, absolutely."*
> *(part-3)*

**5.8 ADR tooling and domain directory creation**
> *"It's gonna copy in ADR tools. It's gonna create the different domains of ADRs for us."*
> *(part-3)*

**5.9 Proactive commit and push offer**
Once setup is complete, Ways causes Claude to offer to commit and push to GitHub for review — behavior that out-of-the-box Claude Code does not exhibit.
> *"Do you see how it offers to commit this and push so you can review in GitHub? Pod code out-of-the-box doesn't do this. It just sits there and waits for the next thing for you to tell it what to do."*
> *(part-3)*

---

## 6. Code Review and Pull Request Capabilities

**6.1 Automatic self-review of setup changes**
After conversion, Ways runs a code review focused on the ADR set and documentation changes it just made, checking three things: is it set up correctly, is it well structured, does it still make sense.
> *"Let me run a code review focused on the ADR set and documentation changes."*
> *"Your review focus is — is it set up, second is, is it well structured, third is, does it still make sense."*
> *(part-3)*

**6.2 PR creation with intent declaration**
Ways generates a pull request with a structured description of intent and a summary of what was done.
> *"The intent of this PR is to adopt ADR driven development and a ways system for contextual guidance. Here's what was done: tooling was installed, the first ADR written about ADRs, the local project Waze was created, Cloud MD was refactored, gitignore was updated and we created the first index."*
> *(part-3)*

**6.3 PR inspection and commentary**
With Waze baseline configured, a developer can direct Claude to inspect a pull request, add commentary based on the developer's stated concerns, and post that commentary to the PR on their behalf.
> *"You could also, as a second thing, literally while you're reading it with your own eyes and inspecting it — if you have your cloud configuration baseline set up, you could have Cloud inspect the PR as well and add some commentary as to what it finds."*
> *(part-3)*

**6.4 Multi-perspective PR synthesis**
Ways enables a workflow where multiple developers (in different languages) add their own perspective to a PR, and the context of both perspectives is merged through Claude.
> *"I can look at what you wrote, which is an amplification of what your intentions were, and I can incorporate all of your stuff into my things since I have my perspective as well, and we'll come up with a synthesis of both of our perspectives."*
> *(part-3)*

---

## 7. Governance and Traceability

**7.1 PR-gated Ways changes**
Changes to Ways go through pull request review, making the team's collective approval the gate for any change in Claude's injected behavior.
> *"Now when you're changing the ways you can incorporate — you have a form of governance."*
> *(part-2)*

**7.2 Consistent cross-developer behavior enforcement**
All developers with the same Ways installed get the same guidance injected into their sessions, creating team-wide consistency.
> *"If you have this one on everybody's computer cloned with this exact document and people are regularly pairing with their coding agent... those managing releases will have a consistent messaging about how releases are done injected into their work."*
> *(part-2)*

**7.3 Regulatory compliance chain**
Ways can encode the full chain from a regulatory framework (e.g., SOC 2, state gaming law) down to a prompt injection, creating a traceable audit trail.
> *"You can build this system out to allow that Waze guidance to be based on SOC 2. You can take SOC 2 in its entirety. You can extract the relevant pieces that are control requirements... create the policy document about that... the policy document is distilled, compiled, revised into a way of guidance, and then it's injected into the agent."*
> *(part-2)*

**7.4 Full provenance traceability**
The chain from injection → way → policy → requirement → regulatory framework is traceable.
> *"We can say that this gets injected in this repo, which was called at this point, which was called at this policy, which was called here, which was called from here."*
> *(part-2)*

**7.5 Queryable as a layer alongside ADRs and governance controls**
Claude can query the repo's Ways, ADRs, and governance controls as a coherent, readable layer during analysis.
> *"There's nothing in the project's ADRs, ways, governance controls, or lint configuration that sets file size or line count thresholds."*
> *(Claude_Code-Dzmitry.md — demonstrated by Claude's live output during an Aaron session)*

---

## 8. Activation and Deactivation Control

**8.1 Domain group activation/deactivation**
Entire sections of Ways can be turned on or off. A developer can disable the software engineering ways group and enable a legal or finance ways group instead, targeting the system to a different professional domain.
> *"You can activate and deactivate sections of way sub-areas. So if you could deactivate the software engineering ways group and enable the legal or the finance ways if you wanted to."*
> *(GitHub_Ways)*

---

## 9. Integration with Other Systems

**9.1 Works alongside Claude Code Skills**
Ways is designed to complement Skills. Skills handle how (procedure, commands). Ways handle why (reasoning, standards). Together they create a complete workflow.
> *"As soon as you say those words... the make way gets injected, the GitHub way gets injected... And then you have the tools and the skills — it knows exactly what commands to run."*
> *(part-2)*

**9.2 GitHub CLI integration (in macros)**
The GitHub macro actively calls the GitHub CLI to count users and evaluate repository configuration. Ways calls external tooling, not just static text.
> *"It uses the GitHub command line tool to count the number of users in there."*
> *(GitHub_Ways)*

**9.3 Knowledge graph integration**
All Ways files can be loaded as a corpus into a knowledge graph system. Once loaded, they form a queryable ontology called "Hooks and Ways" that can be reasoned over independently of Claude Code sessions.
> *"I loaded all the ways. I took all of those ways, those files and loaded them into the graph system."*
> *"We have an ontology called Hooks and Ways. The second is literally all the hooks and ways from cloud code that I had talked about."*
> *(Knowledge Graph, part-1)*

**9.4 Knowledge graph query against Ways**
Once loaded into the graph, Ways can be queried with cross-referencing questions — for example, connecting a specific way to an enterprise operating model.
> *"Can you tell me how the code review way might be supported by the graph as an operating model?"*
> *(Knowledge Graph, part-1)*

**9.5 Documentation pointer pattern (for generative doc updates)**
Rather than putting documentation text directly in the `.claude` directory, Ways can use pointers to documentation in the repo itself. This enables generatively-maintained docs (from docstrings and other tools) to automatically keep the Ways guidance current.
> *"By using pointers to point to the documentation in the repo rather than in the dot cloud directory itself, it makes it more flexible because now if you were to set up docstrings and other tools to generatively create the documents procedurally from code, then all the instructions will just update all the time."*
> *(Claude Code integration - continued.md)*

**9.6 ADR prerequisite relationship**
Getting Waze configured is stated as the prerequisite for being able to use ADR-driven development effectively.
> *"Once you can get the Waze configured, we'll be able to leverage architectural decision records and either back-port them into the code base or begin creating new ones."*
> *(Claude Code integration - continued.md)*

**9.7 Amplifier-correction function**
A coding agent amplifies whatever patterns already exist in a codebase. If those patterns are wrong, the amplification is wrong. Ways provides the corrective intentions that shape what gets amplified — preventing the agent from propagating incorrect architectural patterns. Aaron frames this as: without written intentions in place, the agent reads the existing code base and produces "an amplified version of whatever is already there." Ways corrects the steering.
> *"it's an amplifier... you end up with literally an amplified version of whatever is already there... We have to step back and think, why is it saying no, not like that — because the code patterns themselves are incorrect... we need to start treating the tracking of intentions as almost another piece of the code base."*
> *(Claude_Code-Dzmitry.md)*

**9.8 Ways-defined conventions as test generation foundation**
When coding conventions are documented as Ways, those written intentions become the baseline from which unit tests can be generated. The agent can produce tests that verify adherence to the Way's stated conventions without the developer manually reading the code.
> *"if you have them written down, you have the foundation upon which all tests can be written... Dmitri wrote all of these ways we actually want to code our code and we can write our tests to verify that."*
> *(Claude_Code-Dzmitry.md)*

**9.9 Static analysis closed loop with Ways-defined intentions**
Ways-documented coding conventions can be cross-verified by static analysis tools and linters. The coding agent runs these tools against the live code and checks adherence to the stated intentions, creating a self-correcting loop that is faster and more consistent than manual code review.
> *"We can look for those injection patterns. We can lint the code. We can find these things and flag them. And the coding agent can run the linting and the static analysis and checks incredibly fast and see all the output instantly — steering from intention rather than trying to read all the code directly."*
> *(Claude_Code-Dzmitry.md)*

---

## 10. Organizational Deployment Model

**10.1 Forkable for organizational customization**
Ways is designed to be forked by an organization. The fork becomes the organization's own version, which can diverge from Aaron's base version and be extended with organization-specific ways.
> *"You guys should change the ways when you fork it to make it your release way of course."*
> *(part-2)*

**10.2 Individual developer fork for personal ways**
Within an organization, individual developers can add their own ways to their personal fork.
> *"You can correct it by creating your own way for it. You say 'actually this is the way we do it' and I need to add this way. You add this way to your local installation, which is a git repo clone of the Waze system."*
> *(part-2)*

**10.3 Upstream sync mechanism needed**
The design assumes a mechanism for keeping team forks up to date with Aaron's base version. Aaron stated this as a requirement.
> *"This is why I was telling you how important it is that you keep your forked copy of the whole Waze grant repo up to date because this is the user scope Waze. This is how you have a consistent expectation of what a developer should do at JVL."*
> *(GitHub_Ways)*

**10.4 Consistent professional standards across all developers**
When all developers in a team run the same user-scope Ways, it enforces a consistent development standard across every project, regardless of which repo is being worked in.
> *"If you guys are using the AI tools across everybody — this is how you have a consistent expectation of what a developer should do at JVL."*
> *(GitHub_Ways)*

**10.5 Opt-in non-developer configurations**
Ways groups can be configured for non-developer roles (legal, finance). The system is not restricted to software engineering.
> *"You can activate and deactivate sections of way sub-areas... enable the legal or the finance ways if you wanted to."*
> *(GitHub_Ways)*

**10.6 Ways system enables self-instruction for new team members**
Once a team's Ways system is fully built and defined, the system itself can be used to teach new developers how to use it — through AI-led instruction. The content of the Ways becomes the curriculum, and the coding agent becomes the instructor.
> *"One of the really amazing superpowers of this whole loop is that you can use the very system that you build to teach the people how to use it as well. If you've got it defined, you can literally set up a program to have people be led through it with the AI tool to teach them themselves."*
> *(Claude_Code-Dzmitry.md)*

---

## 11. Continuous Evolution

**11.1 Daily iterative improvement**
Aaron commits to Ways on a daily basis as he discovers gaps, failures, or new needs across projects.
> *"About every day I'm making commits — 4th, 5th, 6th, 9th, 11th. I'm constantly tuning and adjusting this against all of the other projects and work I'm doing."*
> *(part-2)*

**11.2 Failure-driven updates**
When Claude does something wrong in a session, the fix goes into Ways as a new or updated way.
> *"When you catch that thing doing the wrong thing, you have to pause and fix the problem right there... That is likely the next thing you're going to fix in your context."*
> *(Claude Code integration - continued.md)*

**11.3 Prompt evolution (Claude Code changes require Ways changes)**
As Claude Code itself is updated rapidly, Ways prompts must be updated to match. Aaron explicitly noted that a six-month-old CLAUDE.md was outdated because "Claude Code has changed and we're using Waze and some other stuff."
> *"Just like how software is changing over time with new versions, we can think that active development on tools like Claude Code are rapid and move really really fast and so these prompts have to get changed."*
> *(part-3)*

---

## Summary Count

| Category | Number of Capabilities Disclosed |
|---|---|
| Context Injection | 6 |
| Scope Management | 5 |
| Macro System | 5 |
| Known Ways (Domains) | 12 |
| Repository Setup and Conversion | 9 |
| Code Review and PR | 4 |
| Governance and Traceability | 5 |
| Activation/Deactivation Control | 1 |
| Integration with Other Systems | 9 |
| Organizational Deployment | 6 |
| Continuous Evolution | 3 |
| **Total** | **65** |
