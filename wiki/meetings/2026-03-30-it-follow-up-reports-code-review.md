---
type: meeting
title: 2026-03-30 — IT Follow-Up Reports & Code Review (Val ↔ Andrei Bosik)
date: 2026-03-30
aliases: [Follow-up IT Tasks March 30 2026, IT Follow Up Reports and Code Review]
source-count: 2
---

# 2026-03-30 — IT Follow-Up Reports & Code Review (Val ↔ Andrei Bosik)

Thin stub. A ~39-minute Russian call ([[wiki/people/val-levitan.md|Val Levitan]] ↔ [[wiki/people/andrey-bosik.md|Andrei Bosik]], recording base "Follow_up-IT_Tasks", header 30 March 2026 11:02am). A working walk-through of Andrei's new automated reporting site and a follow-up on open IT tasks — continues the **enforcement-loops / dashboards / GitHub-reporting** thread (Mar-6/9/10/17/26).

**§12 — transcript + derived summary → ONE stub, source-count 2.** The transcript [[raw/Meeting_Transcript_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]] and the "# Meeting Summary — Follow-up IT Tasks" derived notes [[raw/Meeting_Notes_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]] are the same meeting (§3 derived-document family); the notes are folded in.

Substance lives on the topic/person pages:

- **Automated compliance + branch-audit reporting** now consolidated into one GitHub repo, auto-generated as web pages (beta): a **daily compliance report** (commits-to-main / PR-vs-direct-push / PR size 400-line threshold / days-since-activity / reviewed-by-other) and a **weekly Monday branch-audit report** (three "improper-branch" categories + sanctioned/active branches). Val's reformatting direction: rename "garbage"→"improper" branches, split into a red **non-sanctioned** block (top) and green **sanctioned** block (bottom), and question single-week trend "dynamics." → [[wiki/topics/github-release-management-pipeline.md]] (Mar-30). [[raw/Meeting_Transcript_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]] [[raw/Meeting_Notes_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]]
- **Claude Code Review expansion + its economics** — expand from 3 repos (Flex POS, Flex Dispenser, Miranda) to all active repos, starting with Flex Sport POS; cost ~$50/PR, deemed cheap even at 75% effectiveness; better documentation and dropping C/C++ will improve review quality. Plus the parked **documentation-as-microservices / AI "software-architect role"** idea. → [[wiki/topics/ai-assisted-development.md]] (Mar-30). [[raw/Meeting_Transcript_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]] [[raw/Meeting_Notes_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]]
- **Andrei's open items** — reformat + regenerate the branch-audit report for Val's review; create a main-project Jira ticket for **release-process documentation** and start that conversation with [[wiki/people/ivan.md|Ivan Shpak]] and [[wiki/people/aaron.md|Aaron]]. → [[wiki/people/andrey-bosik.md]] (Mar-30). [[raw/Meeting_Transcript_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]] [[raw/Meeting_Notes_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]]

Named developers reviewed in the report (all by context): [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] and [[wiki/people/evgeny-kharetski.md|Zhenya Koretsky (= Evgeny Kharetski)]] shown clean; [[wiki/people/igor-metelski.md|Igor Metelski]] and [[wiki/people/anton-leshkevich.md|Anton (Leshkevich)]] flagged for improper branches; [[wiki/people/eugine-yavorski.md|Yavorski]]'s repo left untouched by prior agreement. A Clayton linguistics/transcription microservice demo was booked for later the same day (see [[wiki/people/clayton-chancey.md|Clayton Chancey]]).

§15.8 clear — tooling/reporting/code-review cost economics only; no named-person compensation.

## Sources

- [[raw/Meeting_Transcript_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]]
- [[raw/Meeting_Notes_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]]
