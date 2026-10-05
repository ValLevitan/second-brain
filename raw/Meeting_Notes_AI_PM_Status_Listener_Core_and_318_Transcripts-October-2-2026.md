# Meeting Summary — Design_AI-PM - status
**Date:** October 2, 2026, 7:32 AM – 7:37 AM Eastern
**Duration:** ~5 minutes
**Attendees:** Andrei Bosik, Val Levitan, Pavel Frolov, Irina Shishko, Dmitri Kovalchuk
**Raw transcript:** [[Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026]]

## Summary

Short status from Andrei Bosik on the AI Project Manager build. Held in Russian.

**Done so far.** The whole system is designed as it stands today, and coding has started. The team pulled every Teams meeting transcript Microsoft still holds: 318 transcripts, going back to July 2025 (older ones are gone because of the retention limit). Andrei built the base core he calls the "Listener". It turns what was said in meetings into draft Jira tasks. It reads Russian transcripts too.

**Transcription choice.** Andrei first wanted to take the audio recordings, run them through Whisper with a glossary, and get better transcripts than Microsoft's. He dropped that for now: too much volume, too slow, and it would cost real money. That work is moved to MVP 2. MVP 1 uses the ready Teams transcripts.

**Storage.** Val asked where the transcripts are kept. Andrei: pulled but not stored yet. They will be processed and stored in GitHub. That repository will be the base for the project manager, at least at the start. Later they may move to a real database (SQLite or a vector database).

**Other work.** The persona prompt Val sent was extended with some knowledge. Andrei asked Claude in parallel to build a "voice participant" for meetings. That is hard and not working yet. Literature was loaded into the PM repository with Claude. The agent's knowledge base is Jira, GitHub, and the Jira-discipline reports Dmitri Kovalchuk sends. This was in the design from the start. Claude was writing code while the meeting ran.

**Scheduling.** Pavel joined late. Andrei will send him the transcript. Next status meeting is Tuesday at 7:00 AM Eastern, which is 14:00 Minsk.

## Decisions Made

- **Whisper re-transcription deferred to MVP 2; MVP 1 uses the Teams transcripts.** — Too much volume, time and cost for now. (Decided by Andrei Bosik)
- **Next status meeting Tuesday October 6, 7:00 AM Eastern / 14:00 Minsk.** — Val set the slot; Andrei confirmed the time conversion with Irina and Dmitri. (Decided by Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Send Pavel the transcript of this meeting | TBD | Low | Pavel missed the first part |
| 2 | Andrei Bosik | Process and store the 318 transcripts in the GitHub repository and continue MVP 1 build; report Tuesday | 2026-10-06 | Normal | Storage answer to Val's question |

## Open Questions

- Long-term storage of transcripts: GitHub repository now, a real database (SQLite or vector) later. Raised by Val, answered provisionally by Andrei Bosik.
- Voice participant for meetings: Claude is attempting it; Andrei calls it a hard task with no result yet.

## Dispatch Log

---
*Processed from Teams transcript on October 5, 2026*
*Source meeting: Design_AI-PM - status*
