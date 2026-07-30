---
type: meeting
title: NOVA Platform Architecture Overview (May 12 2026)
date: 2026-05-12
aliases: [Overview services land-based platform, NOVA platform architecture overview, NOVA architecture session, land-based platform architecture, Omni to NOVA naming, Chief Architect appointment]
source-count: 4
---

# NOVA Platform Architecture Overview (May 12 2026)

**Date:** 12 May 2026 — Segment 1 12:20pm ET (~14m), Segment 2 12:56pm ET (~1h56m) (§11 recording header time; the `_082020` / `_085611` filename stamps are a different zone and are not the meeting time).
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/alexander-biratka.md|Alexander (Sasha) Biratko]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/anton-leshkevich.md|Anton Leshkevich]].

The founding architecture session for the JVL land-based gaming platform (§12: two transcript segments + two note segments → one stub). **Segment 1 (as-is)** was Sasha's whiteboard walkthrough of the current on-cabinet ("Omni" code-word) architecture — LGS as the central communication hub, Linux+HAL at the bottom, universal MathEngine+Arrange in Docker, and the known fragility that the system libraries (SoundLib/PrinterLib/BillLib/BoardLib) run as in-process Java-native modules whose errors crash all of LGS. **Segment 2 (to-be)** named the platform **NOVA**, appointed **Alexander Vladimirovich Biratko as Chief Architect**, and drove the to-be design. Substance and citations live on [[wiki/topics/nova-platform-architecture.md]] (the founding May-12 2026 session).

Headline decisions (all detailed on the NOVA topic page): platform name **NOVA**; **Biratka appointed Chief Architect**; library modules become **standalone services** communicating with LGS over **Unix sockets** (10 ms BillBoard reaction-time margin), each with its own repo, data contract, and a **virtual/demo mode** (~99% hardware emulation); a **hardware boundary** placing physical devices and firmware *outside* NOVA and HAL scripts *inside*; **games as packaged archives** (slot-based, updated via CMS→LGS→modem, not Docker containers); **12 base repositories** (or 11 pending Efim's Arrange-vs-MathEngine call) + per-game repos; a language stack of **Java + TypeScript/JavaScript + Rust** (services + JVL firmware migrating to Rust; C++ MathEngine to be re-written in Rust in a new repo) + shell (HAL) + C# (Miranda); **stay on the Pixie/Phaser browser engine for now** (Unity/Unreal/Godot deferred, not killed); **math secrecy relaxed** (Sasha gets MathEngine/Arrange access); **ADRs live as files inside each repo**, owned by the Chief Architect; **CMS↔NOVA protocol = AMQP-style messaging**, to be co-architected by Sasha and [[wiki/people/dmitri-chudinov.md|Dima Chudinov]] (~1 month out, CMS team overloaded); and a **use-case → requirement → capability** governance model whose "users" are internal JVL teams ([[wiki/people/anton-leshkevich.md|Anton]] the test-framework consumer, [[wiki/people/irina-shishko.md|Irina]] the use-case author, [[wiki/people/alexei-khamin.md|Kamin]] Anton's downstream customer). Val's closing rule: **no code until the requirements/capabilities/features model is in place.**

§15.8: platform / architecture / repo / tooling economics only; no named-person compensation. NOVA is the named successor of the "Omni" land-based platform code-word (see [[wiki/topics/omni-core-advancement-and-game-templating.md]]). The "Kamin (Alexey Kamin)" named as Anton's downstream user resolves by QA context to [[wiki/people/alexei-khamin.md|Alexei Khamin]] (JVL QA engineer) — spelling "Kamin" is a transcription variant, flagged for owner confirmation, not force-matched.

## Sources
- [[raw/Meeting_Transcript_nova_platform_architecture_overview-Segment_1-May-12-2026.md]]
- [[raw/Meeting_Transcript_nova_platform_architecture_overview-Segment_2-May-12-2026.md]]
- [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_1-May-12-2026.md]]
- [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_2-May-12-2026.md]]
