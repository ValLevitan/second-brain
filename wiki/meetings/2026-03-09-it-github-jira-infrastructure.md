---
type: meeting
title: IT — Jira↔GitHub enforcement loops (Mar 9 2026)
date: 2026-03-09
aliases: [Call with Andrei Bosik March 9 2026, IT GitHub JIRA infrastructure March 9 2026]
source-count: 1
---

# IT — Jira↔GitHub enforcement loops (Mar 9 2026)

Short Russian call (~3m8s, recording header 9 March 2026 03:58pm; file "Call with Andrei Bosik") in which [[wiki/people/andrey-bosik.md|Andrei Bosik]] walks [[wiki/people/val-levitan.md|Val Levitan]] through the automated Jira↔GitHub checking "loops" JVL wants to build: (1) any task marked in-progress must have a branch created, run nightly at 21:00 Toronto time, emailing the task's assignee; (2) a Jira-timeline check — if a story's start date has arrived but it (or its parent) is not moved to in-progress, notify the assignee, plus a paired check for a GitHub branch that has no matching Jira work (Val's "ghost branches" that carry code with no issue linkage). Bosik said the loops would run in a Docker container on JVL's own Docker machines in the Toronto office data centre, not on Amazon (no reason to pay for it). Val cut the recording as the talk turned to retiring the Toronto server room.

The design Bosik describes here is what [[wiki/people/aaron.md|Aaron]] critiques later the same day (see [[wiki/meetings/2026-03-09-jira-github-enforcement-aaron.md|the 7:14pm call]], where Aaron argues for a per-repo GitHub Action instead of a container). Durable substance on [[wiki/topics/github-release-management-pipeline.md]] (Mar-9); cross-links [[wiki/topics/ai-assisted-development.md]]. Target project/IP numbers in the recording were garbled and are not asserted.

## Sources

- [[raw/IT_GitHub_JIRA_infrastructure-March-9-2026.md]]
