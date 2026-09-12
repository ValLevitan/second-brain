# Meeting Summary — Technician Complaints and New Capabilities Workshop

**Date:** September 11, 2026, 10:33 AM - 10:52 AM Eastern
**Duration:** approximately 19 minutes
**Attendees:** Val Levitan (organiser), Pavel Frolov, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026]]
**Source meeting:** Technician complaints from the field — re-design ideas — Microsoft Teams

## Summary

Val opened by explaining where the material came from: he is spending a lot of time talking to customers directly, and to him a technician is a business owner. The deepest irritations are in Georgia, because Georgia is JVL's main market, though the same complaints appear in other markets too. He had written them up in a document and deliberately included only the ones that repeat constantly and are raised by everyone. He then gave the room a few minutes to read it — a silent stretch of about four minutes on the recording.

**Where the changes land.** Val's first conclusion was that no changes should be made in RAGE Studio. Everything goes onto the OMNI platform. He noted they had already agreed changes are needed in the remote and setup area, and that the modems now being fitted will widen those possibilities further.

**Why the system is not at fault.** Val was careful about how the team should read the complaints. Today's system is built correctly — correctly against the requirements that existed when it was built. What changed is the requirements, radically. He said this is visible in the capabilities he provided: he wrote the prose, did a broad and deliberately shallow architecture design, and drew the capabilities out of it, but stopped there and never got to the regulations, simply for lack of time. He did it that way because he wanted to know how it is done today and what needs to change. He was explicit that he does not want the team landing in a position of "what did we miss, why didn't we do it properly" — the work was right for the regulations of ten years ago, and the market's regulations have moved.

**What the technicians actually object to.** Pavel's read was that technicians dislike having remote and network setup at all and would rather work manually. Val rejected that flatly — twice. They like that remote setup exists. What he himself likes is that some restriction elements force a call to Felipe; what they object to is having to call Felipe to get a new RIS done when it would be better if they could do it themselves. He drew a firm line between RIS and passport, saying the two must not be confused: they like that the passport exists, and they do not have the problems JVL had in Latin America, where the rule was that a bill acceptor could not be changed without JVL's permission. Here the system can instead simply record that a bill acceptor was changed, or flag that unit 17 changed its bill acceptor on a given date, or say that a bill acceptor needs a modification or a firmware upgrade. His verdict: the bindings themselves are good, JVL is using them wrongly in this market. The passport must not be killed — it must be preserved.

Pavel added the implementation constraint: the current passport update only works for people entered in the CMS, and moving to the new CMS implementation means letting the operator nominate the people who can do it. Val agreed, with the qualification that an operator who does not want that responsibility can say so.

**What Val actually wants built.** His main point was that JVL needs to write a new set of regulations describing how the passport and RIS should work. He judged the most efficient route to be a working meeting of the people who influence this and can think about it, naming himself, Felipe, Pavel, Irina and Dima Chudzinau. In an hour they can talk through about 70% of what is needed; take the transcript, turn it into capabilities, hand it to Andrei Bosik to help convert it, and reach roughly 75%. The remaining stretch to about 90% would be covered by the three of them in one further session.

He proposed the working meeting for Monday at 9:30 and asked the attendees to keep the question somewhere at the back of their minds in the meantime. He said he would take this meeting's transcript, draft an email from it, and send it to the people identified for Monday so they think about it too.

**Quick wins that do not have to wait.** Pavel agreed most of this belongs on the new platform, but pointed out that some changes could go into the upcoming RAGE releases without serious engineering work. His example was the "device not found" message — an ancient message still shown on the black screen — which could be made to say the IO board or counter board is not found, at maybe half an hour of work. Val accepted the principle and set the sequence: once the new capabilities are drafted, they will identify which ones can be carried back into RAGE.

## Decisions Made

- **No changes go into RAGE Studio — everything lands on the OMNI platform.** (Val Levitan)
- **The existing system is treated as correct for the requirements it was built against**; the requirements changed, not the engineering. No retrospective fault-finding. (Val Levitan)
- **The passport is preserved, not removed** — the bindings are good and are simply being used wrongly in this market. (Val Levitan)
- **Restrictions that force a call to Felipe for a new RIS are the problem** — technicians should be able to do it themselves. Remote and network setup itself stays. (Val Levitan)
- **Under the new CMS implementation, the operator nominates who may update the passport** — and an operator who does not want that can decline. (Pavel Frolov / Val Levitan)
- **A new set of regulations is to be written describing how the passport and RIS should work.** (Val Levitan)
- **Working meeting set for Monday at 9:30** with Val, Felipe, Pavel, Irina and Dima Chudzinau. (Val Levitan)
- **Method: talk it out for an hour, take the transcript, convert it to capabilities with Andrei Bosik's help**, expecting about 75%, then close the gap to roughly 90% in a further session. (Val Levitan)
- **Back-porting to RAGE is decided after the new capabilities exist**, not before. (Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Draft an email from this meeting's transcript and send it to the Monday attendees so they arrive having thought about it | Before Monday, September 14, 2026 | High | He said he would do it immediately after the call |
| 2 | Val Levitan | Hold the working meeting Monday at 9:30 with Felipe, Pavel, Irina and Dima Chudzinau | September 14, 2026, 9:30 | High | Target is 70–75% of the new capabilities in one hour |
| 3 | Pavel Frolov, Irina Shishko | Think through how they see the new capabilities ahead of Monday | September 14, 2026 | Normal | Val asked for it to sit at the back of their minds |
| 4 | Andrei Bosik | Help convert the Monday transcript into capabilities | After September 14, 2026 | Normal | Named by Val; Bosik was not on this call |
| 5 | [Unassigned — needs clarification] | Improve the "device not found" black-screen message to name the IO board or counter board | Upcoming RAGE release | Low | Pavel put it at about half an hour of work; sequencing depends on undertaking 6 |
| 6 | [Unassigned — needs clarification] | Once the new capabilities are drafted, identify which can be carried back into RAGE | After the Monday session | Normal | Val set this as the gate for any RAGE back-port |

## Open Questions

- **Whether Val's capabilities document will be carried through to regulations by him or by the team.** He said he wrote the prose, the shallow architecture design and the capabilities, but stopped before the regulations for lack of time; Monday's session is aimed at the regulations, but who owns writing them up was not stated.

## Notes on the transcript

The recording is in Russian with English technical vocabulary, and the Teams transcription garbles most product terms. Readings that are near-certain from context but appear distorted in the raw file: "реййд студию" = RAGE Studio, "омни платформу" = OMNI platform, "кейпобилитис / кипа билоти" = capabilities, "рекламенты / регламенты" = regulations, "рис / риз" = RIS, "паспорт" = passport, "врач / рейч" = RAGE. The raw transcript is preserved unchanged.
