# Meeting Summary — Additional Capabilities for Flex-IQ
**Date:** August 27, 2026, 11:46 AM – 11:53 AM Eastern
**Duration:** ~7 minutes
**Attendees:** Val Levitan, Andrei Klimovich
**Raw transcript:** [[Meeting_Transcript_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026]]

## Summary

Val asked for a new capability in Flex-IQ: when a device (an IQ or a later device) is registered, the system should offer a choice of which clearing house handles the clearance, not just InComm. Val expects InComm to face competition and wants the option to switch to another provider to be built in and clearly visible to technicians.

Andrei tested his understanding with a use case the team discussed the day before: at some locations there is more than one card provider (for example Fiery Pay alongside InComm). If a player wins $8,000 and one provider hits a daily cap (say $5,000 through InComm), the location could still pay out the remaining $3,000 through Fiery Pay. Val said the point is to *have* the choice, but he is not saying the location must be the one that chooses — who makes the selection is a separate question to settle later.

Val fixed the wording: multiple clearing houses should be selectable, either set in the settings or changed on the fly, and the setting should be **per device, not per location**. The key requirement is that switching providers must be easy and must not require re-approving or redesigning the software.

Val was clear this does not have to be in the MVP, and the team is not contacting other clearing houses yet — the work now is only to build the switching capability so it is ready if needed. Andrei will capture it as a capability (or small set of capabilities), kept minimal for now.

Separately, Val asked for a follow-up meeting later the same day on the additional features Andrei is proposing for the printer and dispenser. Andrei offered 4:00 PM; Val agreed and said he sent the invite.

## Decisions Made

- **Flex-IQ will support multiple clearing houses, selectable per device** — either in settings or on the fly; must not require re-approval or redesign to switch. (Decided by Val)
- **Not part of the MVP** — build the capability so it is ready, but it is not required for the first release. (Decided by Val)
- **Do not approach other clearing houses yet** — InComm is fine for now; only the switching capability is needed at this stage. (Decided by Val)
- **Follow-up meeting on printer/dispenser features set for 4:00 PM today.** (Agreed by Val and Andrei)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Capture the multiple-clearing-house selection as a capability (or small set), per device, selectable in settings or on the fly; keep it minimal so it is not lost | TBD | Normal | Flex-IQ / InComm registration; not MVP |
| 2 | Val Levitan | Send the 4:00 PM meeting invite for the printer/dispenser additional features | Aug 27, 2026 | Normal | Val stated he already sent it |

## Open Questions

- Who ultimately selects the clearing house — the location or a central decision — was left unresolved by Val.
- Whether to turn the capability into formal requirements now, or just record it so it is not lost — Andrei raised this; Val's answer was not clearly stated on the recording.

## Dispatch Log

---
*Processed from Teams transcript on August 27, 2026 (scheduled watcher run)*
*Source meeting: Additional Capabilities for Flex-IQ*
