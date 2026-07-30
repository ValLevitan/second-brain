# Meeting Summary — CAS Cloud Migration — ex-CMS Grooming Follow-up
**Date:** Thursday, May 7, 2026, 12:59 PM Eastern
**Duration:** 19 min 50 sec
**Attendees:** Val Levitan, Dzmitry (Dima) Chudzinau, Andrei Bosik, Dmitri Kovalchuk, Sergey Tsimanov

## Summary

The meeting opened with Val pointing to the attached Documentation Readiness Report (`doc-readiness-2026-05-07.html`, 11 repositories under JVL-Core, average doc-quality 90.4%, average Java doc coverage 80.3% up from 73.0%) as pre-read material — explicitly asking participants not to repeat what was already documented and to move directly into substantive discussion. He invited Dima Chudzinau and Dima Kovalchuk to lead.

**Documentation grooming status.** Dima Chudzinau confirmed the team is on the home stretch of finalizing documentation across the remaining repositories per the prior meeting's commitment. Three repositories still need to be processed plus one that is currently still hosted under SVN and needs to be migrated. Val noted the visible progress as significant. Per the readiness report two repositories remain at zero or near-zero scores: `infrastructure-casino_management_system-frontend` (5%) and `infrastructure-casino_management_system-data_importer` (0%) — Dima flagged that the frontend repository specifically will require Anton, the frontend specialist, before it can be groomed.

**Core architectural debate — sequencing of the cloud migration.** This was the centerpiece of the meeting. Dima Chudzinau opened by asking Val to confirm the planning capability — i.e., what the team should expect as scope. Dima's framing of the agreed-upon Phase 1 was: containerize everything onto AWS (Amazon EC2), migrate the database away from Microsoft SQL Server (which carries very high licensing costs) onto PostgreSQL, but leave the broader architecture intact. Andrei Bosik supported this position, noting that even Phase 1 alone delivers three substantive wins independent of architectural change: (1) decoupling from the existing local CBS infrastructure, (2) significantly improved security — Andrei cited prior incidents where vulnerabilities in the old software stack were exploited for malicious injections, and (3) improved fault tolerance. Andrei also clarified that, while not a full microservices decomposition, the move would necessarily involve some service-level decomposition because the existing P-key components cannot be deployed as-is and would have to be partially containerized and developed as services.

Val pushed back on this sequencing. His position: the team understands two things — they must move to cloud, and they must materially reduce annual cloud cost. Achieving the cost reduction (a preliminary analysis suggests a 3x to 5x reduction is possible) requires changing more than the database; it requires changing the broader tech stack. Val argued against doing a "blunt" lift-and-shift first and then a second architectural migration later, because in his framing the right sequence is: define the new architecture and tech stack first, then migrate to it directly, avoiding throwaway intermediate work.

Dima Chudzinau countered that to define the new architecture the team needs visibility into long-term plans and KPIs — specifically, whether this same platform is intended to host the next generation of Omni machines or whether the team will be building something separate. Without that visibility, he warned, the project risks getting stuck — neither moving to cloud nor finishing the architecture. Dmitri Kovalchuk added a related point: the new architecture should make the system "constructor-like," allowing individual components to be swapped or upgraded easily, which the current architecture does not support and which Phase 1 (as defined by Dima/Andrei) would not deliver either.

**Resolution on sequencing.** Val acknowledged the legitimate concern about getting stuck and reframed his position: he wants the team to first establish the capability set (he estimated ~60% of capabilities are knowable within a week, given the team's existing understanding), and then on the basis of that capability set drive the architecture and tech-stack discussion. The new architecture, once agreed, becomes the foundation for Features which the engineering team will define; Val will simultaneously drive the Capabilities list from the experience/brand side, and the two streams must marry. Only after architecture and stack are agreed does the migration get planned.

**Timeline.** Val acknowledged the team has been heavily loaded with current work and could not previously give grooming sufficient attention. Dima committed to finishing the remaining 3 repositories "next week." Val proposed framing the team's availability as constrained until June 1, after which more architectural-thinking bandwidth is available. The immediate near-term plan: documentation grooming finishes by Thursday, May 14, 2026; Val will book a meeting on May 14 at 8:00 AM Eastern to begin the tech-stack discussion, using as the starting reference point the architectural proposal Val previously generated via Claude and shared with the team. Val was explicit that he is not the architect and the document is only an "anchor point" — engineering must take ownership and produce their own counter-proposal.

**Tableau license renewal.** Dmitri Kovalchuk raised that the team's Tableau license expires May 23, 2026. Anatoly's departure removed one seat, bringing the renewal cost to USD $900 per year. Val approved an annual renewal without hesitation, noting the cost is trivial relative to the tool's value.

**Meeting artifact.** Val asked Andrei to save the doc-readiness HTML and drop it into the chat (not as a link, as the actual file) so Val can keep it as a record of the conversation. Andrei agreed.

## Decisions Made

- **Tableau license renewed annually at USD $900.** Cost considered trivial vs. value. (Val Levitan, after Dmitri Kovalchuk raised the May 23 expiry)
- **Sequencing: capabilities → architecture → tech-stack → migration, not lift-and-shift first.** Engineering will not perform an interim Phase-1 cloud migration on the legacy stack. Instead, after documentation grooming completes (target May 14), the team will define ~60% of capabilities, then settle architecture and tech stack, then plan the migration. (Val Levitan, with Dima Chudzinau accepting on condition that long-term capability/KPI input is provided)
- **May 14, 2026 at 8:00 AM Eastern is the kickoff meeting for tech-stack / architecture discussion.** Val's prior Claude-generated architectural proposal serves as the anchor document, not as the answer. (Val Levitan)
- **Doc-readiness HTML retained as meeting artifact.** Andrei to attach the file (not a link) to the meeting chat. (Val Levitan, agreed by Andrei Bosik)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dzmitry Chudzinau | Finish documenting the remaining 3 repositories via Claude grooming, plus address the SVN-hosted repository that still needs to be migrated. The two zero-scoring repos in the readiness report are `infrastructure-casino_management_system-frontend` and `infrastructure-casino_management_system-data_importer`. | Thursday, May 14, 2026 | High | Hard prerequisite for the May 14 tech-stack meeting; documentation needs to be at ~85%+ before the architecture conversation can productively start. |
| 2 | Andrei Bosik | Save the Documentation Readiness Report as an HTML file and post the actual file (not a link) into the meeting chat for Val. | Same-day (May 7) — committed in meeting | Normal | Val wants a durable record of today's discussion artifact alongside the recording. |
| 3 | Val Levitan | Schedule the tech-stack / architecture kickoff meeting for May 14, 2026 at 8:00 AM Eastern with Dima Chudzinau, Andrei Bosik, Sergey Tsimanov, and Dmitri Kovalchuk. | Before May 14 | High | The whole post-grooming workstream depends on this meeting landing on the calendar. *Booked May 7, 2026 — invite sent.* |
| 4 | Dzmitry Chudzinau and Sergey Tsimanov | Review Val's Claude-generated architectural proposal as a starting reference point, and come to the May 14 meeting prepared to articulate (a) where they agree, (b) where they disagree and want to change, and (c) what they would substitute. Verbalize the proposed tech stack at that meeting. | May 14, 2026 (the meeting itself) | High | Engineering must take ownership of the architecture; Val explicitly disclaimed the architect role. |
| 5 | Dzmitry Chudzinau | Once architecture is agreed, begin drafting Features that flow from the agreed architecture — i.e., what engineering sees as needed for implementation. | After May 14 meeting | Normal | Features must marry with Val's Capabilities list; this is the hand-off point between the two streams. |
| 6 | Val Levitan | Begin driving the Capabilities-from-experience-brand list, to be merged with engineering's Features. | After May 14 meeting | Normal | Capabilities + Features = the working scope for migration planning. |
| 7 | Dmitri Kovalchuk | Renew the Tableau license on annual terms at USD $900 (one fewer seat after Anatoly's departure). | Before Saturday, May 23, 2026 | Normal | Avoid lapse of the Tableau license. |

## Engineering Signals

### Confirmed Signals
- **ADR (process — sequencing):** Capability definition (~60% target) must precede architecture; architecture must precede tech-stack selection; tech-stack must precede the migration plan. The team will not perform a lift-and-shift migration on the legacy stack as Phase 1. Decided by Val with Dima accepting on condition of capability input.
- **ADR (target cloud):** AWS (Amazon EC2 was named directly) is the target cloud platform for the migrated CAS. Discussed as already-agreed framing — not re-debated in this meeting.
- **ADR (database migration):** Microsoft SQL Server → PostgreSQL. Driver: MS SQL licensing cost. Discussed as already-agreed; will be revisited in context of new architecture.
- **ADR (containerization):** All services to be containerized (Docker named). Discussed as already-agreed framing.

### Suspected Signals
- **Possible REQ:** New platform must serve as the host for the next generation of Omni machines and must coexist via LANbase with the existing legacy machines on the floor. Raised by Dima Chudzinau as a precondition for architecture work.
- **Possible CAP:** "Configurator" capability — the system should be architected such that individual components/details can be swapped or upgraded with minimal effort. Raised by Dmitri Kovalchuk; Dima confirmed neither current nor Phase-1 architecture supports this.
- **Possible ADR:** Move toward service-oriented decomposition (Andrei's caveat: "not microservices, but at least services") as a forced consequence of containerization. Not formally decided.
- **Possible REQ (security/decoupling):** Decouple from existing local CBS infrastructure; resolve known software-vulnerability exposure (Andrei cited prior injection incidents); achieve fault tolerance. These are migration drivers but were stated as system-level requirements that survive any sequencing decision.

## Open Questions

- Long-term KPIs and platform-vs-separate-product decision for the next-generation Omni machines — Dima flagged this as a blocker for committing to architecture; needs an answer from Val before or at the May 14 meeting.
- Anton (frontend specialist) availability for the `casino_management_system-frontend` repository grooming — not addressed.
- Dima noted the team will "still be busy after May 15" and planning past that point hasn't been done; Val pegged June 1 as the realistic point at which architectural-thinking bandwidth opens up. Bandwidth between May 15 and June 1 is undefined.

## Attached Artifact

- [[doc-readiness-2026-05-07.html]] — Documentation Readiness Report snapshot, JVL-Core × 11 repos, generated for this meeting.
- [[CAS_Cloud_Migration_ex-CMS_Grooming_Follow-up-May-7-2026.docx]] — Raw Teams transcript (source for this summary).

---
*Processed from Teams transcript on May 7, 2026*
*Source meeting: CAS Cloud Migration — ex-CMS Grooming Follow-up*
