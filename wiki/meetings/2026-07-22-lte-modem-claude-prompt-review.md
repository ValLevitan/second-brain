---
type: meeting
title: LTE Modem Claude Prompt Review (July 22 2026)
date: 2026-07-22
aliases: [LTE Modem Claude Prompt Review, LTE modem AI prompt review, V1000 LTE modem persona flow, modem jira claude code prompt, LTE modem agent test July 22 2026]
source-count: 2
---

# LTE Modem Claude Prompt Review (July 22 2026)

**Date:** July 22, 2026, 7:03–7:28 AM Eastern (~25 min; Russian)
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]].

Val and Pavel reviewed progress on the **AI prompt / agent approach** applied to the **V1000 LTE modem** work — i.e. running the engineering-prompt / "Constitution" method (from the [[wiki/meetings/2026-07-21-ai-engineering-prompt-review.md|July-21 engineering-prompt walkthrough]]) against the LTE-modem task set up in Jira on the [[wiki/meetings/2026-07-20-lte-modem-jira-structure.md|July-20 LTE-modem Jira-structure meeting]]. [[raw/Meeting_Notes_LTE_Modem_Claude_Prompt_Review-July-22-2026.md]] Pavel had written up points 6 and 8 of the prompt, had AI generate universal versions plus a series of agents and a skill, and ran a live test that spawned subagents (one analyzing Jira, one Git) which found capabilities for the modem already exist in JVL's Jira structure. Val and Pavel agreed the up-front work is real but shrinks over 1–3 months, settled that for the V1000 the AI must **not** be pointed at code (SVN, a dead end) and must follow a **persona-driven flow** (personas → use cases → capabilities → requirements → features), and that when information is missing the AI should **ask a question, not dig for truth** in sources. [[raw/Meeting_Transcript_LTE_Modem_Claude_Prompt_Review-July-22-2026.md]]

The AI-method substance (prompt/agents/skill progress, meetings-as-source-of-truth limits, Obsidian-is-source-of-truth, ask-don't-dig, point-10 roles, run-and-compare) → [[wiki/topics/ai-assisted-development.md]] (Jul-22 section). The device/engineering substance (V1000 persona-driven flow, don't-look-at-code-for-V1000, ~50 personas, Pavel's Jira agent test) → [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Jul-22 section). §11 header time (7:03 AM start). §12: both raws new — uncited elsewhere and not skip-ledgered; one new meeting. §15.8: clear — LTE-modem / AI-prompt / persona-flow economics only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_LTE_Modem_Claude_Prompt_Review-July-22-2026.md]]
- [[raw/Meeting_Transcript_LTE_Modem_Claude_Prompt_Review-July-22-2026.md]]
