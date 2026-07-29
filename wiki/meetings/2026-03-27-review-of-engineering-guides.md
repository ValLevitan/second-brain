---
type: meeting
title: 2026-03-27 — Review of Engineering Guides (ADRs, Jira hierarchy, transcript pipeline)
date: 2026-03-27
aliases: [Review of Engineering Guides March 27 2026, Engineering Guides review]
source-count: 2
---

# 2026-03-27 — Review of Engineering Guides (ADRs, Jira hierarchy, transcript pipeline)

Thin stub. A ~1h29m review ([[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/pavel.md|Pavel Frolov]], recording base "Review of Engineering Guides", header 27 March 2026 11:02am, Russian) of Val's **"Engineering Guides"** document — the deliberately-minimum engineering-documentation standard for JVL. This continues the Ways / ADR-storage thread: the [[wiki/meetings/2026-03-16-release-procedure-and-eng-documentation-flow.md|Mar-16]] / [[wiki/meetings/2026-03-17-jvl-ways-on-github-setup.md|Mar-17]] Ways-on-GitHub work and the [[wiki/meetings/2026-03-13-capabilities-requirements-adr-storage.md|Mar-13]] ADR-storage ruling. Aaron was **not** present.

**§12 — transcript + derived notes → ONE stub, source-count 2.** The transcript [[raw/Meeting_Transcript_Review_of_Engineering_Guides-March-27-2026.md]] and the "# Meeting Summary — Review of Engineering Guides" derived notes [[raw/Meeting_Notes_Review_of_Engineering_Guides-March-27-2026.md]] are the same meeting (§3 derived-document family); the notes are folded in.

Substance lives on the topic pages:

- **Engineering workflow, ADRs and the Jira hierarchy** — the agreed **Capability Tickets → ADRs → Features** chain (engineers create ADRs during technical discussion, then write Features linked to both the ADRs and the capability tickets; ADRs drive ~80–90% of feature creation, not business requirements); the proposed Jira hierarchy restructure (**Value Stream → Product → Capability Ticket → Feature**, with Stories/Tasks moved to **GitHub** kanban); the "architecture-overview black hole" (JVL has an undocumented architecture — ADRs are "a drop in the ocean" without a master document, illustrated by the Georgia unattended-machine freeze); the ADR-vs-architecture folder debate; the Engineering Guides document going to **v6.3** (remove the onboarding section, add a concrete step-by-step workflow example); the ~1,700 broken parent-child links if a level is inserted (Dima to prepare an Excel comparison table); and enforcing a GitHub-branch link before a feature goes In-Progress (notifications, not hard blocks) → [[wiki/topics/ai-assisted-development.md]] (Mar-27). [[raw/Meeting_Transcript_Review_of_Engineering_Guides-March-27-2026.md]] [[raw/Meeting_Notes_Review_of_Engineering_Guides-March-27-2026.md]]
- **The automated transcript-to-documentation pipeline** — the [[wiki/people/clayton-chancey.md|Clayton]]/[[wiki/people/lena.md|Elena Zhukova]] pipeline that, after each meeting, captures a WAV audio format and a "dirty" Teams transcript, runs the audio through a lexicon module on GitHub to produce a clean document, and auto-*proposes* (not imposes) ADRs; text-only storage on GitHub (no audio), tied to projects; target ~2 weeks (≈April 10); Dima + Bosik to prepare the repository structure → [[wiki/topics/transcript-knowledge-base-tooling.md]] (Mar-27). [[raw/Meeting_Transcript_Review_of_Engineering_Guides-March-27-2026.md]] [[raw/Meeting_Notes_Review_of_Engineering_Guides-March-27-2026.md]]

**Recorded here (procedural):** Val stressed that the documentation initiative must become **company culture** (spread by visible reporting, not prohibitions) and that meetings should open by referencing a Jira ticket / capability / feature so discussion starts from a concrete anchor rather than a vacuum; participants should come prepared with objectives and allocated time. A developer nicknamed "Piratka" was cited as the case where Features don't map to how the engineer works. [[raw/Meeting_Transcript_Review_of_Engineering_Guides-March-27-2026.md]]

§15.8 clear — engineering documentation, Jira/GitHub tooling and machine-reliability economics only; no named-person compensation.

## Sources

- [[raw/Meeting_Transcript_Review_of_Engineering_Guides-March-27-2026.md]]
- [[raw/Meeting_Notes_Review_of_Engineering_Guides-March-27-2026.md]]
