# Meeting Summary — Alignment Schedule Review (AI Working Method Overview)
**Date:** July 21, 2026, 12:33 PM Eastern
**Duration:** ~15 minutes
**Segment:** Opening segment — followed by [[Meeting_Notes_AI_Engineering_Prompt_Review-July-21-2026|the paragraph-by-paragraph prompt walkthrough]] recorded right after.
**Attendees:** Val Levitan, Pavel Frolov
**Raw transcript:** [[Meeting_Transcript_AI_Working_Method_Overview-July-21-2026]]

## Summary

This is the opening of the Alignment Schedule Review call. Val spends it explaining, mostly as a monologue, the AI working method he has built for himself, before he and Pavel move on to review the actual engineering prompt (segment 2). Pavel mainly listens.

Val's main points:

- **X (Twitter) MCP for Claude.** X released a developer MCP for Claude on June 30. The developer subscription is free; usage is pay-per-use, capped for someone like him at roughly $100/month. It lets him prompt Claude to pull the best statements of a chosen thinker (Boris Cherny, Andrej Karpathy, Elon Musk, or anyone he wants to follow) on a given topic over a given period.
- **Library of frontier thinkers.** He has built a personal library of leading industrialists/thinkers — Boris Cherny, Karpathy, Musk, Warren Buffett and others — and keeps adding their sayings. When building a prompt he asks Claude to draw on that library ("do it the way Karpathy would, combine it with Buffett's ethic," etc.).
- **He no longer writes prompts himself.** He describes the problem and what output he wants (e.g. a compact table). He uses Fable 5 to write the prompt, then hands it to a cheaper model — Opus 4.8 or Sonnet 5 — to execute. He notes that Karpathy and Boris Cherny are saying engineers no longer write code directly; they write loops and agents that write or control code.
- **Second brain (~50% built).** He is building a second brain in Obsidian + GitHub, with a local free MCP indexing all his files. It is being built from his transcripts starting January 1, 2025 (about a year and a half). It self-indexes in a self-learning way and writes him a "world view" report every 15% of progress (currently ~45%), so he can watch it learn.
- **Philosophy: industry breaking from dogma.** The old model of being handed a fixed recipe (in school, for building a UI or a knowledge base) is breaking. With ~20 developers and designers, rather than telling everyone one prescribed way, he wants each person to build their own knowledge base however works best for them — the only requirement being that their knowledge base is addressed to a shared **Constitution** (the "whys"). Letting people build their own knowledge base produces more creative solutions. The common thread: everyone stops executing by hand and instead writes self-discovering, self-correcting agents; productivity starts slow, then rises exponentially once the agents self-progress.
- **Why MODAM as the pilot.** As a concrete step, they want to draft a scope/sketch for how to integrate MODAM. Val chose MODAM because it is a small, contained topic — a good low-risk experiment: if it goes wrong he can throw it out, and it gives him good learning. He works with two parallel Claude sessions: one he calls the "proposer/critic" (fact-based, builds the prompt), the second an "executor" that then works with the prompt. He spent the morning (started ~6:00, took ~2 hours) producing the prompt he wants to share, and proposes they spend this call critiquing, implementing, or adding to it — which is what segment 2 does.

## Decisions Made

No formal decisions in this segment. It is the framing/context for the prompt walkthrough that follows in segment 2.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel | Consider building his own AI working method / knowledge base along the lines Val described, and bring ideas back to Val to discuss | TBD | Low | Open recommendation from Val, not a firm commitment |

*The concrete action items from this meeting live in segment 2 — see [[Meeting_Notes_AI_Engineering_Prompt_Review-July-21-2026]] (Pavel to rework paragraphs 6 and 8, review paragraph 9; Val/Claude to rewrite paragraph 10, etc.). Dispatch from that note to avoid duplicates.*

## Open Questions

None in this segment.

## Dispatch Log

---
*Processed from Teams transcript on July 21, 2026*
*Source meeting: Alignment_Schedule_review_July-21-2025-20260721_083356-Meeting Recording*


- July 21, 2026, 10:10 AM ET — "Draft everything" selected. Consolidated Pavel draft (segment-2 items 2, 3, 4) created in Outlook Drafts, not sent. No calendar reminders (deadlines TBD). Segment-1 undertaking #1 (soft recommendation to Pavel) not dispatched. Full details logged in [[Meeting_Notes_AI_Engineering_Prompt_Review-July-21-2026]].
