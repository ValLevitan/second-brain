# Meeting Summary — AI-PM agent - narrowed role review
**Date:** October 8, 2026, 8:31 AM – 9:44 AM Eastern
**Duration:** ~73 minutes
**Attendees:** Val Levitan, Andrei Bosik, Dmitri Kovalchuk, Pavel Frolov, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026]]
**Previous meeting:** [[Meeting_Notes_AI_PM_Agent_Narrow_Role_and_Nine_Task_Cap-October-6-2026]]

## Summary

Held in Russian. The first ~2 minutes were lost to audio problems.

**Status.** Andrei: all changes from the October 6 meeting are in. The agent collects and cleans meeting transcripts every 15 minutes (GitHub Actions scripts, no cost; Irina asked if that is too often). A listener role reads the cleaned transcript and creates Jira features with status "AI Draft", with a quote, a timecode and an assignee. It can comment on existing items. Anything it is unsure of goes into an internal "draft" document, used later to answer questions in Teams. It may delete only items it created; on others it only comments. Meeting titles with a "no AI" tag are skipped. Dmitri works on the Second Brain. Voice is MVP2.

**Whose meetings.** Pilot covers 6 people: Pavel, Irina, Andrei Klimovich, Lena, Dmitri, Andrei Bosik. Val asked to drop Lena (graphics team) for now, to avoid needless arguments until the tool has a track record. Andrei argued more context helps, then agreed.

**Architecture.** Val doubts the design: the listener does too much (listen, judge capabilities, write features, self-improve, audit) and will not scale to a real-time agent in MVP2–4. He saw a demo of a real-time meeting agent and knows it works. He suggested the listener only listens and adds to a vocabulary/taxonomy, and a separate agent does the processing. Andrei: it was built in a week for MVP1 and can be split later. Pavel: it works like a person who takes notes and then processes them, one linear flow. Val closed: launch it, and change the architecture if needed.

**Demo.** A feature created from the October 6 standup, linked to capability 259, was confirmed correct by Irina and Andrei. Real projects go live Monday, October 12.

**Draft lifetime.** AI Draft items not moved to To Do are deleted after a set time. Last meeting set 1 day. Andrei, Pavel and Dmitri wanted 2+ days (time zones, a morning report, force majeure). Val gave a long talk: a team that seeks the middle of all opinions makes a "watered-down soup"; better to hold one position, be wrong, and correct it; why keep garbage the team will discuss again anyway. Pavel: weekends — a Friday item must not be deleted before Monday; Andrei planned this but has not built it. The morning report will show AI Draft counts per person; Pavel suggested a filtered Jira link in it. No final value was clearly stated.

**Cost.** Prompts optimized: far fewer tokens, better choice of project and owner. Estimate ~$1 per meeting once on the Anthropic API (today it runs on Andrei's own account); catalog refresh ~$0.50. A local model is not worth it at these prices.

**Teams agent.** Has a real Microsoft account and a generated face (female). Knowledge: the internal drafts, cleaned transcripts, Jira, GitHub, and a project catalog rebuilt daily from Claude files and repo prose; Val's books are in its prompt. In the live test it answered that it found nothing. Val: not genderless — give her a name; he proposed "Dasha".

**Two kinds of draft.** Irina was confused. Andrei clarified: in Jira, everything the agent creates has status "AI Draft" and a person must move it to To Do or reject it. Separately, the internal "draft" document holds what did not go to Jira. Users learn of new items by Jira email and the morning report.

## Decisions Made

- **Lena's meetings are removed from the pilot for now.** Avoid arguments until the tool proves itself. (Val Levitan; Andrei Bosik agreed)
- **Launch with the current architecture; change it later if needed.** (Val Levitan)
- **Live mode in real Jira projects starts Monday, October 12.** (Andrei Bosik)
- **The agent deletes only items it created; on others it only comments, no edits.** (Andrei Bosik)
- **The agent is not genderless; it gets a name ("Dasha" proposed).** (Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Remove Lena from the pilot meeting list | TBD | Normal | |
| 2 | Andrei Bosik | Improve the Teams agent so it gives real answers | Oct 12 | High | Val will review Monday |
| 3 | Andrei Bosik | Switch on live mode in real Jira projects | Oct 12 | High | |
| 4 | Andrei Bosik | Set the AI Draft lifetime and skip weekends before deletion | TBD | Normal | Value not settled |
| 5 | Andrei Bosik | Add AI Draft counts per person to the morning report | TBD | Normal | Pavel: include a filtered Jira link |
| 6 | Andrei Bosik | Give the agent a name | TBD | Low | Val proposed "Dasha" |
| 7 | Dmitri Kovalchuk | Continue the Second Brain build | TBD | Normal | |

## Open Questions

- How long do AI Draft items live before deletion — 1 day (Val, last meeting) or 2+ days (Andrei, Pavel, Dmitri)? Not clearly settled. (Pavel Frolov, Dmitri Kovalchuk)
- Will the single listener design scale to a real-time agent in MVP2+? (Val Levitan)

## Dispatch Log

---
*Processed from Teams transcript on October 8, 2026*
*Source meeting: AI-PM agent - narrowed role review*
