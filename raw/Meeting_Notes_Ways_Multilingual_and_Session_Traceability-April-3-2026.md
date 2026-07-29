# Meeting Summary — Val & Aaron: Ways Multilingual & Session Traceability

**Date:** April 3, 2026, 12:23 PM Eastern
**Duration:** ~22 minutes
**Attendees:** Aaron Bockelie, Val Levitan

## Summary

Aaron demoed several new Ways features and tools to Val, starting with **abtop** (Agent B-top), a process monitor for Claude sessions that lists all running Claude sessions and their child processes — similar to a system process monitor but specific to Claude Code.

Aaron then showed the **Ways session visualization tool**, now compiled into a single fast Rust binary. The visualization displays a real-time animation of how Ways steers a Claude Code conversation — showing which Ways get triggered at each turn, how many turns have elapsed, and predictions for the next Ways likely to fire. Aaron played back a 2-hour-42-minute session recording to demonstrate the pattern of decisions Ways makes as it drives through a conversation. He showed how a session starting with "we have an open issue we wrote to ourselves about multilingual stubs" caused the GitHub delivery software Way to fire, followed by the commits Way and delivery Way simultaneously at epoch 4, then the tasks Way when Aaron asked about task lists. The visualization makes every turn traceable to which Way was triggered, providing an audit trail that proves guidance was followed.

The major new feature Aaron presented was **multilingual support for Ways**. He showed the list of supported languages, which includes Russian — directly relevant to Val's team. The system uses a local multilingual embedding model (approximately 120 megabytes of neural weights) that can relate words across languages. Aaron was about to kick off Claude building all the translation stubs for the supported languages, generating Way triggers and descriptions in each language via parallel agents. The supported languages include Japanese, German, Spanish, and others, covering both symbolic character languages (Chinese, Japanese) and Latin-root languages.

Aaron explained the key technical difference: **the multilingual embedding runs entirely locally on the computer's CPU**, not via API calls. This is critical for reliability — if Ways had to make an API call to an internet connection on every tool call or turn, a single network failure would hang the entire Claude Code conversation. The local execution ensures high performance and no internet dependency.

Val asked how this differs from what **Lena and Clayton** are building through microservices. Aaron clarified that Lena and Clayton are building a **generalized universal language translation service** usable anywhere, not specific to Claude Code. Ways multilingual is highly specific to Claude Code, contained within it, and optimized for local high-performance execution. Clayton's service is a generalized API you connect to for translation requests, which isn't as fast as Ways' local approach.

Aaron requested that once the multilingual build is pushed, **Andrei should verify it runs correctly**, and then **all Russian-speaking team members using Ways should submit feedback** — pull requests, notes, or messages — about what's correct, what's wrong, what to add or remove in the Russian Way translations, so Aaron can tune the detection beyond what machine translation provides.

Aaron briefly showed the **governance framework** in Ways (Val calls it "constitution"). While not yet heavily populated for the current project, it allows adding governance rules — potentially by jurisdiction. Aaron gave a hypothetical example: if a theme company fully adopted Claude Code for writing gaming math models, they could add per-jurisdiction math rules and game-style-specific governance (finite math vs. infinite math), then write Ways about how code should be written in that space. This creates full traceability from rule → Way → code output.

Val observed that Aaron's workflow is self-reinforcing: as Aaron works on different projects, the Ways he develops persist and keep accelerating his work. Aaron no longer has to re-explain his preferences to Claude every session — the Ways encode his working style and inject it automatically. Aaron confirmed this was exactly the origin of the project: he got tired of re-entering the same instructions. He started by keeping a directory of text files in his documents folder describing how he wanted to commit work, his writing style, and other preferences. This evolved into a user-scope CLAUDE.md, but it grew too large and started consuming too much context, causing Claude to forget things. When Anthropic introduced hooks, Aaron started matching keywords to inject guidance just-in-time during sessions, and that condensed into the structured Ways system.

Aaron shared the **Ways philosophy statement**: "Prescriptive, not proscriptive guidance triggered by context but not requested by intent and then injected just in time before tools execute."

Aaron mentioned he plans to **rename the repository** from "claude-code-config" to "agent-ways" and is working on making Ways compatible with **any turn-based coding agent that has hooks**, not just Claude Code.

## Decisions Made

- **Multilingual Ways will include Russian support natively.** Russian-speaking team members will be able to type in Russian and trigger the same Ways as English. (Decided by Aaron)
- **Ways multilingual runs locally, not via API.** The embedding model executes on the local CPU to avoid internet dependency and ensure reliability. (Decided by Aaron)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Verify the multilingual Ways build runs correctly after Aaron pushes it | TBD (after push) | High | Gate for team-wide Russian language tuning; nothing can be tuned until Andrei confirms it works |
| 2 | Russian-speaking team (via Andrei) | Submit feedback on Russian Way translations — PRs, notes, or messages to Aaron about what's correct, wrong, or missing | TBD (after Andrei verifies) | Normal | Machine translation is the starting point; human tuning needed for slang, activity-specific terms, and accuracy |

## Engineering Signals

### Confirmed Signals

- **CAP — Ways session traceability:** Aaron demonstrated that every turn in a Claude Code session is traceable to which Way was triggered. This creates an audit trail proving that guidance was followed during code generation. Aaron stated: "You could look at every single decision made during the turns... and actually then prove that you were at least following the guidance that was written."

- **CAP — Ways multilingual support via local embedding model:** A ~120MB multilingual neural embedding model runs locally on CPU to match intent across languages without API calls. Supports both symbolic (Chinese, Japanese) and Latin-root languages.

- **ADR — Local execution over API calls for Ways language detection:** Aaron explicitly chose local CPU execution over internet API calls for the multilingual embedding: "What you don't want to be stuck with is making an API call to an Internet connection on every single tool call, turn or whatever, because the one time it doesn't work, then your whole Claude Code conversation would hang."

### Suspected Signals

- **Possible CAP — Governance/constitution framework in Ways:** Aaron showed a governance model that can encode rules by jurisdiction or domain and connect them to Ways for full traceability (rule → Way → generated code). Not yet populated for current projects but the framework exists.

- **Possible ADR — Rename repository to "agent-ways" and decouple from Claude Code:** Aaron mentioned plans to rename the repo and make Ways work with any turn-based coding agent with hooks. This would be an architectural scope change.

## Open Questions

- When will Aaron push the multilingual build for Andrei to verify?
- How will team members submit Russian tuning feedback — via pull requests to the Ways repo, Teams messages, or another channel?
- Timeline for making Ways agent-agnostic (working with any coding agent, not just Claude Code)?

---
*Processed from Teams transcript on 2026-04-04*
*Source meeting: Val & Aaron — April 3, 2026*