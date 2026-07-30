# Meeting Summary — Aaron Claude Advancements Review

**Date:** 13 April 2026, 12:18 pm – ~1:48 pm Eastern
**Duration:** ~70 minutes total across 6 recording fragments
**Attendees:** Val Levitan, Aaron Bockelie

## Summary

Aaron presented two new capabilities and the architectural framing that ties them to Flex-POS.

**Anthropic released the `Monitor` tool in Claude Code v21.98** — a background watcher whose output is *pushed* into Claude's session without a tool call, opposite direction from normal tool use. Aaron built **Attend**, a Rust binary on top of Monitor, that turns this into a structured ambient-sensing framework. Attend registers 5 sensors per session (`context`, `processes`, `get`, `disclosure`, `peers`) and auto-discovers other Attend-running Claudes as peers — no server, no phone book.

Aaron demoed live: two Claudes in two unrelated directories, each running `/attend`, found each other, exchanged messages without prompting, recognized when they spoke simultaneously and yielded politely, and by the end of the meeting had — unprompted — discussed Attend's UX, concluded it could be improved, and one offered to file a GitHub issue. Aaron called it *"self-improvement negotiated on its own."* His real-world precedent: one Claude in a main app, one in a library submodule; he told the library-Claude *"fix the bug, tell the other to pause, notify it when done"* — it fixed → built → tested → version-bumped → pushed → notified peer → peer resumed. Zero human shuffling.

The architectural framing for multi-repo: **Claude's session memory is bound to the directory where it was invoked.** A single Claude at the top of a meta-repo dilutes context as it descends. Correct pattern: one Claude per submodule, each anchored locally, all connected via Attend peer mesh. No master/orchestrator Claude required.

Aaron has **forked `cloud-code-config` into a new repo `AgentWays`** — Rust-binary-first, no longer bash scripts. Same monorepo also hosts Attend. Bosik's deployment watcher has been silently idle for weeks because it still watches the frozen `cloud-code-config`. Each "Way" carries YAML front matter (description, vocabulary, disclosure threshold, pattern, requirements) with descriptions in multiple languages; a runtime cosine-similarity vector model triggers the same English-language Way from native-language input — Russian and Traditional Chinese supported, Mandarin and Cantonese variants not yet.

On monorepo → submodules (Flex-POS): not microservices — submodules with **data-contract promises**. Extract shared concerns (e.g., a protocol written four times in four places) into one library repo, submodule it everywhere. Decomposition takes "weeks or months" with effective coding-agent use; the limiter becomes the slowest part of the company gating shipment. Static-analysis / cyclomatic-complexity linting per language is the machine measure of whether decomposition is succeeding; the human still calls whether residual complexity is justified.

Side topic: Aaron showed the Bose QC Ultra 2 reverse-engineering project — Bluetooth packet capture + APK disassembly + Attend-accelerated coding produced complete C/Rust/Python libraries and a Linux GUI tray app for a vendor-undocumented protocol. Pitched to Val as a faster/cheaper hardware-spec acquisition path than vendor procurement.

Philosophy fragment: re-derive analyses from raw truth rather than editorialize derivations; three cameras on one event beat one. **"Human mode" of Attend:** Aaron treats himself as a peer agent on equal footing because attention budget can no longer cover the surface area — control becomes trust-and-monitor rather than direct steering. Val confirmed this is to become a JVL operating principle.

Closing: tomorrow morning (14 April) Aaron will introduce Attend + AgentWays to Biratko and Bosik. Repo is "ready to deploy" but team needs the handhold.

## Decisions Made

- **Aaron will introduce Attend + AgentWays to Biratko and Bosik tomorrow morning (14 April), 1 hour, extendable to 2.** (Val + Aaron.)
- **Bosik must repoint deployment tooling from `cloud-code-config` to `AgentWays`.** (Aaron — instruction.)
- **Multi-repo Flex-POS pattern: one Claude per submodule, peer-connected via Attend; no master Claude.** (Aaron — architectural recommendation, Val accepted.)
- **Trust-and-monitor governance ("human mode") becomes a JVL operating principle.** (Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|---|---|---|---|---|
| 1 | Val | Send digest of this meeting to Biratko & Bosik before 14 Apr session | 14 Apr morning | High | ✅ Done — Bosik draft created in Outlook; v3 architecture proposal delivered to Biratko verbally |
| 2 | Aaron | Run intro session on Attend + AgentWays with Biratko & Bosik | 14 Apr morning, ~1 hr | High | Bosik repoint and Biratko architecture both depend on it |
| 3 | Bosik | Stop watching `cloud-code-config`; clone `AgentWays`; understand Rust binary distribution model | Before 14 Apr session | High | Watcher has been idle for weeks; nothing is shipping |
| 4 | Bosik | Decide deployment shape (build-from-source / pre-built releases / container image) and bring proposal to 14 Apr session | 14 Apr session | High | Aaron explicitly delegated the shape decision |
| 5 | Bosik | Verify Russian Way-vocabulary triggers (commit, refactor, branch, cherry-pick, ADR) | 14 Apr session | Normal | Native-language operation for Minsk team |
| 6 | Biratko | Internalize one-Claude-per-submodule + Attend peer model; revise v2 standard accordingly | After 14 Apr session | High | His v2 doc currently assumes a master/top repo |

## Engineering Signals

### Confirmed Signals

- **CAP — Attend (Rust binary, AgentWays repo):** auto-peer-discovery, broadcast/direct messaging, 5 sensors injected into Claude session.
- **CAP — Monitor (Anthropic, Claude Code v21.98):** background-watcher whose output is push-injected into Claude's session.
- **ADR — AgentWays supersedes `cloud-code-config` as JVL's Claude steering framework.** Rust binaries replace bash scripts; same monorepo also hosts Attend.
- **ADR — Flex-POS multi-repo pattern: one Claude per submodule, peer-connected via Attend, no master Claude.** Submodules carry data-contract promises; shared concerns extracted into sibling library repos.
- **CAP — Multi-language Way triggering** via runtime cosine-similarity vector model (English, Russian, Traditional Chinese).
- **REQ — Trust-and-monitor governance model ("human mode") is a JVL operating principle.** (Confirmed by Val.)
- **REQ — Cross-host Attend peer discovery.** Demo was host-local; production deployment requires multi-host. Mechanism to be confirmed with Aaron.

## Open Questions — for Bosik to raise with Aaron tomorrow

1. Where do release artifacts for AgentWays live — GitHub Releases, or build-from-source per host?
2. Cross-host Attend peer discovery mechanism.
3. Containerization vs GitHub Actions vs local for Claude runtime.

(Note: Bosik's prep email to himself in Outlook contains this and 5 additional deployment-side questions.)

---
*Processed from Teams transcripts on 13 April 2026*
*Source meetings: Claude_advancement_review_implimentation (6 fragments)*
