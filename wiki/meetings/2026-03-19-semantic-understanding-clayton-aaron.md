---
type: meeting
title: 2026-03-19 — Semantic Understanding pipeline as a service (Clayton)
date: 2026-03-19
aliases: [Semantic Understanding March 19 2026, Clayton Aaron JVL March 19 2026, transcript microservice, semantic understanding as a service]
source-count: 1
---

# 2026-03-19 — Semantic Understanding pipeline as a service (Clayton)

Thin stub. A ~1h3m working session (recording base "Clayton-Aaron-JVL-20260319_140335UTC", header 19 March 2026 2:03PM; [[wiki/people/clayton-chancey.md|Clayton Chancey]], [[wiki/people/lena.md|Lena Zhukova]], [[wiki/people/val-levitan.md|Val Levitan]]). Despite the "Clayton-Aaron" recording label, [[wiki/people/aaron.md|Aaron]] does **not** attend this one. This is the **second "Semantic Understanding" session**, a week after [[wiki/meetings/2026-03-13-semantic-understanding-clayton-aaron.md|Mar-13]]: Clayton demos the built dual-source pipeline and Val reframes it as a reusable service. It leads directly into the Mar-27 hosted microservice and the Mar-31 live MCP.

Substance lives on the topic/person pages:

- **The dual-source pipeline, built** — Clayton demoed the working pipeline: **raw audio** (good content, no speaker identity) + the **bad Teams transcript** (correct diarization/timestamps) → Whisper transcription with a taxonomy **preprocessor** (only the call-relevant glossary terms are injected, working around Whisper's ~200-word prompt limit) → **Claude** merges accurate text with accurate speakers and normalizes to English. Live test on a game-dev meeting: speaker attributions correct, mixed English/Chinese/Russian game names largely right. Issues found: the **participants list wrongly included people merely *mentioned*** (e.g. the taxonomy codename "Vladimir Avdev"), and some game names mis-rendered ("Fortune #4"). → [[wiki/topics/transcript-knowledge-base-tooling.md]] (Mar-19). [[raw/Clayton-Aaron-JVL-semantic-understanding-March-19-2026.md]]
- **"Set it up as a service" — Val names the initiative** — Val asked to set up this "semantic understanding" pipeline **as a service** on GitHub, callable by anything (API → MCP → automation), and told Clayton to run it by [[wiki/people/andrey-bosik.md|Andrei Bosik]], who had already started the setup and "has to be incorporated." Val's guiding rulings: output must be **precisely literate, grammatically correct English with no transliteration annotations** (input may be Russian — the native tongue gives better prompts — but JVL is attracting non-Russian devs, so output must be universally readable); the **improved transcript is an improved *source*, not the knowledge base**; transcripts are small (~2–10 KB markdown) and belong in GitHub; **UTC timestamps** so meetings sequence correctly; and the eventual pipeline should extract ADRs / requirements / capabilities / features while still **referencing the source transcripts** so the AI can interpret past disagreement. → [[wiki/topics/transcript-knowledge-base-tooling.md]] (Mar-19) and [[wiki/topics/ai-assisted-development.md]] (Mar-19). [[raw/Clayton-Aaron-JVL-semantic-understanding-March-19-2026.md]]

Next steps set: package the pipeline as an API, wrap it as an **MCPB** single-file MCP server, then coordinate with Andrei for Microsoft Graph API secrets to auto-post improved transcripts for every recorded Teams meeting. (The Windows Cowork "can only reach the home/desktop folder, not the D drive" limitation was raised again; Clayton noted he had just been accepted as an **Anthropic partner** and might raise it.) Next meeting set for Tuesday.

§15.8 clear — tooling / pipeline / service architecture only; no named-person compensation.

## Sources

- [[raw/Clayton-Aaron-JVL-semantic-understanding-March-19-2026.md]]
