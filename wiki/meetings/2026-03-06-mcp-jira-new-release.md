---
type: meeting
title: Claude↔Jira MCP new release + requirements-by-domain (Mar 6 2026)
date: 2026-03-06
aliases: [MCP JIRA new release March 6 2026]
source-count: 2
---

# Claude↔Jira MCP new release + requirements-by-domain (Mar 6 2026)

Short English JVL-IT session in which [[wiki/people/aaron.md|Aaron Bockelie]] briefs [[wiki/people/val-levitan.md|Val Levitan]] (and [[wiki/people/andrey-bosik.md|Andrei Bosik]]) on the **refactored Jira plugin for MCP** and on how to attach requirements to work through Claude. Segment 1 (header 6 March 2026 03:29pm, ~1m35s; Val, Aaron, Andrei Bosik): Aaron explains the new MCP can use **any Jira custom field** (with caveats for complex ones like multi-dropdowns), but **only if the field carries a terse, well-written description** — an empty or poorly-written description makes the MCP deliberately ignore the field and degrades performance across everyone's MCP servers; also that people must add their **Jira auth token** to it. [[raw/MCP_JIRA_new_release_March-6-2026.md]] Segment 2 (header 03:43pm, ~2m24s; Aaron, Val): connect requirements to work **by requirements domain, not by project** (requirements are cross-project), e.g. "look at requirements for North Dakota specifically about math" — walk a domain, confirm each requirement is well-written and accepted/discussed, and route the un-accepted ones to whoever should decide, since legacy requirements that never reached acceptance will hurt product quality once code is attached to them. [[raw/MCP_JIRA_new_release_March-6-2026 (1).md]]

**§12 — two segments of ONE short meeting, both cited.** The two recordings are sequential (03:29pm then 03:43pm, ~14 minutes apart) with **low content overlap** — segment 1 is the custom-field-description brief, segment 2 is the requirements-by-domain workflow — so this is a continuation of the same short session, **not** a re-transcription or numbered-copy duplicate. Both are cited above (source-count 2).

Continues the Claude↔Jira MCP thread from [[wiki/meetings/2026-02-26-jira-planning-flex-dispenser.md|Feb-26]] (the MCP still immature; "~70 custom fields removed") and [[wiki/meetings/2026-02-27-jira-custom-fields-review.md|Feb-27]] (the deletion-matrix cleanup → 13-field keep list). Durable substance on [[wiki/topics/ai-assisted-development.md]] (Mar-6).

## Sources

- [[raw/MCP_JIRA_new_release_March-6-2026.md]]
- [[raw/MCP_JIRA_new_release_March-6-2026 (1).md]]
