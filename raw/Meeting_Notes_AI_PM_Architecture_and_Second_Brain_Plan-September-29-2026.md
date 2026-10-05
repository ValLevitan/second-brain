# Meeting Summary — Design_AI-PM
**Date:** September 29, 2026, 6:02 AM – 6:56 AM Eastern
**Duration:** About 53 minutes
**Attendees:** Val Levitan (organizer), Andrei Bosik, Pavel Frolov, Irina Shishko, Dmitri Kovalchuk
**Raw transcript:** [[Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026]]

## Summary

Held in Russian. The speech recognition is poor in places.

**Val's vision.** Val wants an **AI PM** that works like the AI CFO he uses every day. It relies only on facts. It joins every Teams meeting, reads the agenda, takes notes, can ask questions in real time, and later can speak in a natural voice (ElevenLabs). It has its own name and mailbox and works like a normal employee. Its knowledge is narrow on purpose: Jira, Confluence, GitHub code and prose, PM textbooks, company standards, meeting transcripts, and the mixed Russian-English glossary Lena made. Val stressed: **the AI PM must do the work, not write to people.** Its tasks must be correct, limited in number, follow standards, and stay close to today's code and prose.

**Andrei's proposal.** Andrei Bosik prepared slides that overlap about 70% with Val's. He added: use the three existing daily reports as data; after a meeting, create **draft tasks in Jira with an "AI draft" status**; a person accepts, edits or rejects them. First a **dry run** of one to two weeks with no Jira writes. Each repository maps to a Jira project, so drafts go to the **repository code owners**. Tasks should cite the transcript time where the topic was discussed.

**Concerns.** Val fears too much text will overwhelm people. Pavel said drafts may get lost deep in the Jira tree; Dmitri suggested a special issue type that shows at the top. Pavel noted 50 tasks split across owners is about 8 per person, which Val found fine. On timing (right after a meeting or once a day), Val prefers right away and asking for comments; the AI will chase what is not done.

**Second brain vs knowledge base.** Val said a second brain is built from **frozen facts** (transcripts that never change) plus an index. A knowledge base is a collected list of knowledge. Pavel and Andrei saw the second brain as a knowledge base with a better index and graph.

**Transcripts.** Andrei said an old transcript repository (made by Lena) no longer works. Transcripts sit with each meeting organizer; even an admin cannot read them. A way to collect them from every user is needed. Val estimated collection at 1–2 days and building the second brain at about a month; his own took about a month and about $7,000 for 18 months of transcripts. Start it first because it is the longest step. The glossary comes after: the second brain lists terms it does not understand. For storage, Val (per his Claude) keeps raw transcripts in Obsidian with a light local index, and summaries in GitHub.

**Order of work.** Andrei found the meeting bot the most interesting part. Val moved the bot to **MVP 2**: first build what saves work now, then add steps; in about a month there should be a working system. The team does not want to add people. While the second brain builds, the team designs the AI PM's persona (Val: 2–3 days).

**Working method.** Val described using two AIs, a "teacher" and an "implementer", and copying between them. He advised: act as if you know nothing and do not set the tone.

**Next meeting.** Andrei proposed meeting in one or two weeks and called this a bonus task. Val refused: it is not a bonus. Val will book a meeting **Friday around 7:00 AM**.

## Decisions Made

- **Andrei Bosik owns the AI PM project.** (Agreed by Val Levitan, Andrei Bosik)
- **The live meeting bot moves to MVP 2; quick wins first.** — The team needs relief now. (Decided by Val Levitan)
- **First step: collect all transcripts in one place and build the second brain.** — It is the longest step. (Val Levitan, agreed by Andrei Bosik)
- **Draft tasks go to repository code owners; no human "responsible" for the AI.** (Val Levitan, Andrei Bosik)
- **Dry run first, no Jira writes until the output looks right.** (Proposed by Andrei Bosik; no objection)
- **Status review on Friday (Oct 2), about 7:00 AM, not in 1–2 weeks.** (Decided by Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Finish the AI PM architecture design so it is clear | Oct 2, 2026 | High | Status at Friday meeting |
| 2 | Andrei Bosik | Set up collection of meeting transcripts from every user into one store | Oct 2, 2026 | High | Admin cannot read them today |
| 3 | Andrei Bosik | Start building the second brain from the transcripts | TBD | High | About a month of processing |
| 4 | Andrei Bosik | Design the AI PM persona (character) | TBD | Normal | Val: 2–3 days |
| 5 | Val Levitan | Book the follow-up meeting Friday about 7:00 AM | Oct 2, 2026 | Normal | |

## Open Questions

- What period of transcripts to use: Val suggested from January 2026 (maybe June); the team will see what can be pulled.
- Where the AI PM runs (cloud, a bought service, or an office machine) (Pavel, Andrei).
- How to limit the amount of text the AI writes (Val).
- Tasks right after each meeting or once a day (Andrei).

## Dispatch Log

---
*Processed from Teams transcript on September 29, 2026*
*Source meeting: Design_AI-PM*
