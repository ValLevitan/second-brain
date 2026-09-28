# Meeting Summary — Modem on V-1000: Capabilities of the initial release
**Date:** September 24, 2026, 11:46 AM – 12:04 PM Eastern
**Duration:** About 18 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_V-1000_Modem_Current_Use_Cases-September-24-2026]]

## Summary

Held in Russian. The transcription quality is poor in places, so Jira numbers below are as heard in the transcript.

**Purpose.** Val wanted to see which capabilities the modem on the V-1000 has in its first release. He wants each capability attached in Jira, its features closed (even if only one or two), and the work aligned with a project and a repository, then marked done.

**Capability 109.** Irina found two capabilities: 109 and 172. Capability 109 sits under IP-747. Pavel said 109 is in fact everything that was built. Val asked if it can be called closed, and then said it is closed. The reporter was not Andrei Klimovich; Pavel said he had to set someone other than himself. Val said in such cases to set himself or Bosik (part of his answer is unclear in the transcript). Pavel suggested Irina, because she will then see what was done. Val agreed.

**Where the code is.** Pavel said this work is in SVN, and releases are made from there. Val complained about SVN; Irina said "we still have to live with it."

**Capability 172.** Irina said 172 is for Texas, a second item after what was released. It is still open and sits under IP-1061. Pavel asked why it is under GA-COAM. Irina said the Texas plan is unclear; if it is released soon, it can stay there. Val reminded them that all these IPs are being reformatted.

**Flex IQ modem work in Jira.** This work is already in GitHub. Pavel said it was done under an IP, not a capability, and can be converted to a capability now. Val agreed and told them to collapse the old IPs and use a bulk change. Pavel and Irina moved items during the meeting (977 moved; a new parent under IP-1199; capability 238). Pavel said the move was too rough: some features do not belong to this capability and must be moved out. Irina said that means one more capability. Val left the rest of the Jira cleanup to them after the meeting.

**What the modem does today (Pavel):**
1. **RIS pass-through.** After a factory reset or a software install, if a RIS exists on the server for this machine, the machine can pass the RIS step automatically at initial setup.
2. **Lease update.** If the machine's lease renews on a schedule (every two weeks or monthly), it updates automatically. If a lease was cancelled, the update arrives and the machine stops working when the term ends.
3. **Statistics.** Game-play data now collected by QR scans should also come through the modem. Val asked if this means all meters plus service statistics. Pavel said in theory both service statistics and accounting meters, but **nobody has tested this on the modem yet.** Sync is sent several times a day. The data goes into JVL's database, with the service messages. Pavel did not remember if it reaches the reporting server; this needs checking.
4. **Software updates.** None. The modem does not do this today.

**Next step (Val).** Use this transcript to write the current use cases properly, then write the capabilities the module has today under them. After that, write new capabilities for the modem and check what can and cannot be done.

## Decisions Made

- **Capability 109 is closed.** It covers what was built. (Val)
- **When the builder cannot be the reporter, set Irina** (Val first named himself or Bosik). (Pavel proposed Irina; Val agreed)
- **The Flex IQ modem IP becomes a capability**; old IPs are collapsed and moved by bulk change. (Pavel proposed; Val agreed and set the method)
- **The current modem use cases are documented from this transcript first**, then today's capabilities, then new capabilities. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov, Irina Shishko | Finish the Jira cleanup for the modem: move out features that do not belong to the capability, create another capability if needed, fix parents | TBD | Normal | Val left this to them after the meeting |
| 2 | Pavel Frolov | Check whether modem statistics reach the reporting server | TBD | Normal | Pavel: "need to look, I don't remember" |
| 3 | [Unassigned — needs clarification] | Write the current modem use cases from this transcript, then the capabilities under them | TBD | Normal | Val said "we can take these use cases"; no owner named |

## Open Questions

- Do all meters and service statistics actually arrive over the modem? Not tested yet. (Val asked; Pavel answered)
- Where does capability 172 (Texas) belong — under GA-COAM IP-1061 or elsewhere? Depends on the Texas release plan. (Pavel, Irina)

## Dispatch Log

---
*Processed from Teams transcript on September 24, 2026, 2:10 PM Eastern*
*Source meeting: Modem on V-1000: Capabilities of the initial release*
