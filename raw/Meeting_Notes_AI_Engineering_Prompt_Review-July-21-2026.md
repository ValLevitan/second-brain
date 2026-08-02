# Meeting Summary — Alignment Schedule Review (AI Engineering Prompt Walkthrough)
**Date:** July 21, 2026, 12:48 PM Eastern
**Duration:** ~36 minutes
**Attendees:** Val Levitan, Pavel Frolov
**Raw transcript:** [[Meeting_Transcript_AI_Engineering_Prompt_Review-July-21-2026]]

## Summary

Val and Pavel walked through Val's engineering "prompt" (the instruction document / Constitution for the AI-driven development loop) paragraph by paragraph. Val recorded the call so that, afterward, Claude could rewrite the document from the transcript. Val's stated goal: make the workflow self-running — a system that does the work by itself and keeps building on itself so he doesn't have to repeat instructions each time.

The prompt is meant to drive an AI agent (or a group of agents — Val suggested roles like executer, controller, proposer, engineering expert) that reads a brief plus the repos and Jira, and proposes capabilities, features, and stories following the existing JVL standards and the 5-level Jira hierarchy. Standing rules in the prompt: the agent works inside Jira / Confluence / Cloud CAD read-only via MCP (propose only, do not create or move issues); use current engineering practices, not old ones; check the knowledge base before asking; do not invent facts; when not confident or when it hits a conflict, ask for clarification rather than guess or assume; and correspond by email to Pavel (engineering questions) with follow-ups.

Val flagged that the capability/feature information currently in Jira and Confluence is vague and poorly formatted, so he expects the agent to raise many questions.

They stopped at paragraphs 6, 8, 9, and 10 as the ones needing rework. Pavel's recurring critique: several paragraphs are written too concretely — they should be abstract instructions for the AI, with the concrete content moved into an attached reference document supplied each time the agent runs. Val agreed and asked Pavel to take ownership of the engineering-specific paragraphs. Val will have Claude rewrite paragraph 10 into that abstract, agent-oriented form, and add two things: a directive that Claude write to Val in simple, succinct language (no fancy or long prose), and a paragraph specifying where outputs go.

## Decisions Made

- **One email = one subject (not one question).** The prompt currently says one email per question; Pavel noted a subject can hold several questions, so the rule should be one subject per email. Val agreed and will fix the wording. (Decided by Val and Pavel)
- **Capability placement in Jira is settled.** Flex-1000-related capabilities live under IP-747; Nova-related capabilities live under IP-480. Pavel has already created and sorted them there. Paragraph 8 will be updated to state these concrete entry points. (Decided by Pavel; confirmed with Val)
- **Paragraph 10 (the deliverable) will be reformatted into abstract, agent-oriented instructions** describing a self-organizing, multi-agent environment rather than the current concrete content. (Decided by Val and Pavel)
- **Output destinations for the loop:** proposals written as draft `.md`; final capabilities/features go into Jira; code and the standards they develop go into GitHub (common product repo / knowledge base); no changes are made without approval. (Stated by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Fix prompt wording: one email = one subject (not one question) | TBD | Normal | Pavel's correction, accepted |
| 2 | Pavel | Rework paragraph 6 into abstract AI instructions — how topic meetings should be structured (constraints, benefits, possible solutions, brainstorm) feeding into ADRs/decisions; move the current concrete content to an attached reference doc | TBD | High | Only Pavel can shape it to his satisfaction |
| 3 | Pavel | Polish paragraph 8 — state concrete entry points (capabilities under IP-747 for Flex-1000, IP-480 for Nova), decide the kernel (Val suggests staying on 5.15), and cover the separate modem/driver handling | TBD | High | Engineering decisions only Pavel can make |
| 4 | Pavel | Review paragraph 9 closely (the reporting / "find index and propose" business instructions) — Val is unsure these are correct | TBD | Normal | Val explicitly asked for a close look |
| 5 | Val / Claude | Rewrite paragraph 10 from the transcript into abstract multi-agent instructions; add a "write to Val in simple, succinct language" directive; add a paragraph specifying output destinations (draft .md → Jira → GitHub, no changes without approval) | TBD | Normal | Val's post-call action |

## Open Questions

- Kernel choice for paragraph 8 — Val suggests staying on 5.15 but leaves the decision to Pavel.
- Whether paragraph 9's instructions are correct (raised by Val).
- Repository targeting for some proposals (e.g., Flex IQ vs Flex Risa) — Pavel wants the agent to surface these as explicit open questions for Val to answer rather than guessing.

## Dispatch Log

- Jul 21, 2026 — Email SENT to Pavel (items 2, 3, 4 — paragraphs 6, 8, 9), English, approved by Val. No calendar reminders (all deadlines TBD). Val's own items (1, 5) not dispatched.

---
*Processed from Teams transcript on July 21, 2026*
*Source meeting: Alignment_Schedule_review_July-21-2025-20260721_084839-Meeting Recording*


- July 21, 2026, 10:10 AM ET — Consolidated email draft created for Pavel covering items 2, 3, 4 (rework para 6, polish para 8, review para 9). Draft in Outlook Drafts, not sent. No calendar reminders (all deadlines TBD). Items 1 and 5 are Val's own — no email. Dispatch initiated from the segment-1 capture (AI Working Method Overview).
