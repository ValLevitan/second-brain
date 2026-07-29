---
type: meeting
title: 2026-03-13 — Semantic Understanding transcription pipeline (Clayton/Aaron)
date: 2026-03-13
aliases: [Semantic Understanding March 13 2026, Clayton Aaron JVL March 13 2026, JVL whisperer, Russian transcription pipeline]
source-count: 1
---

# 2026-03-13 — Semantic Understanding transcription pipeline (Clayton/Aaron)

Thin stub. A ~56-minute working session (recording base "Clayton-Aaron-JVL-20260313_140034UTC", header 13 March 2026 2:00PM; [[wiki/people/clayton-chancey.md|Clayton Chancey]], [[wiki/people/lena.md|Lena Zhukova]], [[wiki/people/val-levitan.md|Val Levitan]]; [[wiki/people/aaron.md|Aaron Bockelie]] joined near the end, ~39 min in). This is the **first of the two "Semantic Understanding" sessions** that designed JVL's custom Russian/slang transcription pipeline — the design work that led to the Mar-27 hosted microservice and the Mar-31 live MCP. A separate 9:33pm Mar-13 Aaron↔Val ADR-storage call is a different meeting ([[wiki/meetings/2026-03-13-capabilities-requirements-adr-storage.md]]).

Substance lives on the topic/person pages:

- **Why Teams transcription fails, and Clayton's proposed low-effort Whisper pipeline** — Microsoft Teams and Copilot do not support Russian; the Minsk team's speech is ~30% code-switched English/slang, and even plain Russian transcribes badly, skewing the whole conversation. Clayton and Aaron had each built Whisper transcription tools ~a year earlier; Clayton proposed grabbing the Teams audio (via the Microsoft Graph API), re-transcribing it with JVL's taxonomy/glossary as Whisper prompt context, then having Claude clean it — storing the result on GitHub. Val's stance: keep JVL's own **slang-to-English document** (the taxonomy) and overlay it with Whisper rather than depend on a third-party tool. Lena's existing manual workaround (Turboscribe + taxonomy + Claude = "almost perfect") was the baseline to beat. → [[wiki/topics/transcript-knowledge-base-tooling.md]] (Mar-13, 2:00pm). [[raw/Clayton-Aaron-JVL-semantic-understanding-March-13-2026.md]]
- **The Jira MCP tool, sub-agents, and story-as-artifact** — the custom Atlassian MCP that turns a good transcript into a Jira feature/story hierarchy is working (tested in a sandbox); Clayton committed to add **sub-agents** to the MCP prompting to keep reasoning quality from degrading on long transcripts, and to have the tool **research the live Jira conventions** rather than hard-code them. Val restated the objective — turn a conversation into actionable Jira items at near-zero overhead ("good necessary bureaucracy" brought to ~0 cost) — and his shift from **story-as-to-do-list to story-as-deliverable/artifact**: a completed feature = a GitHub branch, a completed story = a versioned artifact, wired through the Jira↔GitHub CI/CD integration. → [[wiki/topics/ai-assisted-development.md]] (Mar-13). [[raw/Clayton-Aaron-JVL-semantic-understanding-March-13-2026.md]]

§15.8 clear — tooling / pipeline / MCP economics only; no named-person compensation.

## Sources

- [[raw/Clayton-Aaron-JVL-semantic-understanding-March-13-2026.md]]
