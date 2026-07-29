---
type: meeting
title: 2026-03-31 — Transcripts MCP Setup with Lena (Clayton pipeline)
date: 2026-03-31
aliases: [Transcripts MCP setup Lena, MCP transcripts pipeline setup, Clayton Aaron JVL March 31 2026]
source-count: 2
---

# 2026-03-31 — Transcripts MCP Setup with Lena (Clayton pipeline)

Thin stub. A ~1h14m working session (recording base "Clayton-Aaron-JVL-20260331_140027UTC", header 31 March 2026 2:00PM; [[wiki/people/clayton-chancey.md|Clayton Chancey]], [[wiki/people/lena.md|Lena Zhukova]], [[wiki/people/val-levitan.md|Val Levitan]]). [[wiki/people/aaron.md|Aaron]] is referenced repeatedly but is **not present**. Clayton walks Lena through connecting her Claude MCP to the new transcripts pipeline; the setup is repeatedly derailed by Windows MCP instability, and the session opens up into an extended source-of-truth and hallucination discussion. Continues the Clayton/Aaron automation thread from the [[wiki/meetings/2026-03-27-automation-progress-review.md|Mar-27 automation-progress review]].

**§12 — transcript + derived notes → ONE stub, source-count 2.** The transcript [[raw/Meeting_Transcript_Transcripts_MCP_setup_Lena-March-31-2026.md]] and the "# Meeting Summary — Clayton-Aaron-JVL" derived notes [[raw/Meeting_Notes_Transcripts_MCP_Setup_Lena-March-31-2026.md]] are the same meeting (§3 derived-document family); the notes are folded in. (The bundle's `README.md` is a manifest, not content — ledgered in [[wiki/skipped.md]].)

Substance lives on the topic/person pages:

- **The transcripts MCP pipeline is live end-to-end** — Teams recording → a Microsoft Power Automate script ([[wiki/people/andrey-bosik.md|Andrei Bosik]]) that fires after any meeting → Clayton's JVL microservice, which pulls the latest **glossary** from GitHub and produces a refined ("JVL speak") transcript → a **GitHub transcripts repository** organized by date → the **JVL Atlassian MCP** server (two new tools, `list transcript` / `get transcript`, authenticated by a GitHub **PAT** with **SSO**) → Claude cross-references Jira and proposes a game backlog. Confirmed working in a live test (resolved "Dragon Pays" correctly by cross-checking Jira; auto-enriched feature descriptions with meeting-notes comments). Val's **source-of-truth ADR**: a transcript is *not* truth — it is raw material; the only sources of truth are **ADRs and Requirements** ("everything else is speculative conversation"); the repo must be **SSO-managed, not wide-open**. Next step: interleave Teams **chat** messages into the pipeline (chat carries requirement links). → [[wiki/topics/transcript-knowledge-base-tooling.md]] (Mar-31). [[raw/Meeting_Transcript_Transcripts_MCP_setup_Lena-March-31-2026.md]] [[raw/Meeting_Notes_Transcripts_MCP_Setup_Lena-March-31-2026.md]]
- **Clayton's hallucination thesis + game-creation-as-three-loops + the Mac-mini decision** — Clayton (differing with Aaron): a large language model has no category of truth/untruth, so a "hallucination" is a *user* category arising from the human's excess context; you reduce it not by better models but by engineering the context/tools so the model converges on what humans hold true — currently Lena is the "ontological filter" hitting execute. Val: game creation is three loops (idea generation / game design / **game production**); Clayton and Lena are on loop 3, which Val calls an **assembly line** to be fully automated with minimal creativity ("get rid of useful bureaucracy" — Aaron's phrase). Because MCP tooling is unstable on Windows (repeated connect/disconnect on Lena's machine), Val ordered a **Mac mini** for Lena live on the call — a targeted fix, NOT a team-wide OS migration; team leads **Anastasia** and **Julia** also need it (they manage stories); Lena's custom graphical tools won't run on Linux but work on Mac. → [[wiki/topics/ai-assisted-development.md]] (Mar-31). [[raw/Meeting_Transcript_Transcripts_MCP_setup_Lena-March-31-2026.md]] [[raw/Meeting_Notes_Transcripts_MCP_Setup_Lena-March-31-2026.md]]

A separate session was booked for Val to set up his own MCP transcripts access.

§15.8 clear — tooling / pipeline / hardware only; no named-person compensation.

## Sources

- [[raw/Meeting_Transcript_Transcripts_MCP_setup_Lena-March-31-2026.md]]
- [[raw/Meeting_Notes_Transcripts_MCP_Setup_Lena-March-31-2026.md]]
