---
type: meeting
title: Val ↔ Aaron — retiring the JIRA acceptance-criteria custom field (Feb 16 2026)
date: 2026-02-16
aliases: [acceptance criteria custom field migration, JIRA custom field retirement, Val Aaron Feb 16]
source-count: 1
---

# Val ↔ Aaron — retiring the JIRA acceptance-criteria custom field (Feb 16 2026)

**Date:** 2026-02-16 (recording header "16 February 2026, 01:12pm") · **~1m20s** · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/aaron.md|Aaron Bockelie]]. English.

**Purpose:** A short clip in which [[wiki/people/aaron.md|Aaron]] gives [[wiki/people/val-levitan.md|Val]] a safe method to retire JIRA's **"acceptance criteria" custom field without losing the data already entered in it** — have Claude write a script to enumerate every issue with the field populated (including closed ones), download it, process offline, then transform in batches by appending each issue's acceptance-criteria content to the end of that issue's main description, verify against a local checklist, and only then delete the custom field.

Substance lives on [[wiki/topics/ai-assisted-development.md]] (Feb-16 section). This is the antecedent of the later Feb-27 2026 "Review_custom_fields_JIRA" work (future batch). §15.8: clear — JIRA tooling/process only; no named-person compensation.

## Sources

- [[raw/Val—Aaron.md]]
