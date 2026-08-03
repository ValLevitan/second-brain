# Meeting Summary — IQ Pilot updates Q&A
**Date:** July 29, 2026, 9:30–11:00 AM Eastern (recording 9:33–10:04 AM)
**Duration:** ~31 minutes
**Attendees:** Val Levitan, Andrei Klimovich, Dzmitry Chudzinau (Dima), Pavel Frolov, Sergey Tsimanov, Ivan Shpak
**Raw transcript:** [[Meeting_Transcript_IQ_Pilot_MVP_Listen_Only_Reversal-July-29-2026]]

## Summary

Pavel pulled the team together to lock what goes into the nearest FlexIQ MVP. Ivan was there to scope what needs re-testing; Sergey as the main implementer. The meeting produced two significant reversals of earlier decisions, plus a clear priority call.

**Capability structure.** Pavel had put the terminal work under a product-level feature grouping (IP 902 FlexIQ) rather than under FlexIQ capabilities. Val objected hard: the capability model that he and Andrei invest heavily in — personas → use cases → capabilities → requirements → features, laid out in GitHub — must be used, not sidelined. He said he spends about half his day getting that structure right and it is the single serious project where JVL is trying to adopt it. Andrei clarified that what is written in Confluence is a "change," not a feature: a change is a body of logic that can be covered by several capabilities, and one capability can spawn several features (not the reverse). Pavel accepted that his AI-assisted pass had wrongly mapped items one-to-one as features and agreed to redo it.

**Mutha Goose connection — reversed to listen-only.** Dima raised edge cases about the MG printer being offline (disconnected, out of paper) while IQ sits "in break" between the MG board and the MG printer. Val cut this off: IQ must have zero influence on the Mutha Goose install. He declared the earlier "in-break" decision wrong and said the team had already agreed to revert it (Pavel noted they had not actually reverted yet). New scheme: the MG printer connects directly to the MG system as it did before JVL was involved; IQ does not sit in the middle, does not print MG tickets, does not print its own receipts, and does not touch their system. IQ only listens on the side — if it receives a validation signal, it shows the ticket on the IQ screen and offers a button to issue a card. No intrusion. Val framed this as a deliberate strategic choice so no one can point fingers at JVL if MG's own equipment fails. Later, once JVL installs its own bill acceptors (SMBs) and a recorder device, it can layer on validation and services and offer real capabilities — but not now.

**Consequence — cables.** The current cables were built for the in-break connection and won't work for listen-only. Two cables are needed; they can be re-soldered / re-pinned or an adapter added. Andrei confirmed cables are easy to source or rebuild quickly in Minsk. This becomes a question for Genadi Peari on the hardware side, plus a software change to drop IQ's own ticket printing.

**Remote software update — top priority.** Pavel flagged the remote software-update / device-fleet-management capability as the most important and least-defined MVP item, being built from scratch. He studied Eclipse hawkBit — a cloud tool that manages a fleet of devices, monitors their versions and statuses, and pushes software updates. Dima and Andrei are evaluating alternatives in parallel; the architecture still needs to be settled. Val stressed it must be polished because there will be many terminals: if updates go smoothly the other rough edges slide by, but if updates are hard, every problem becomes painful and visible.

**Schedule discipline.** Val was firm: do not treat Aug 1 (Saturday) as a hard deadline, no Friday release, and no installation at any location before Tuesday. "Hurry slowly." It is a raw beta release and many problems will surface; JVL needs only one harness/sample and the minimal set of capabilities, with an operator who understands it is unfinished.

**Scope freeze.** Val told Andrei to stop sending new capability documents and ideas to the developers during the MVP crunch — every document pulls four pairs of eyes off delivery. The PIN-per-location / location-change idea Andrei had circulated is deferred to a separate meeting. Val reiterated that he alone directs scope for the JVL project and nothing is to be assigned to anyone without him.

## Decisions Made

- **Revert the Mutha Goose connection to listen-only.** IQ stops sitting "in break"; the MG printer reconnects directly to the MG system; IQ does not print MG tickets or its own receipts and does not touch MG's system — it only listens for the validation signal and offers card issuance on its own screen. (Decided by Val)
- **Restructure FlexIQ work under the capability model.** Create a new IP-level FlexIQ epic and attach Andrei's documented capabilities to it; stop treating Confluence "changes" as one-to-one features. (Decided by Val; Pavel to execute)
- **No location installation before Tuesday (Aug 4); Aug 1 is not a hard deadline; no Friday release.** (Decided by Val)
- **Remote software update is the top MVP priority and must be polished.** (Val / Pavel)
- **Freeze new scope during the MVP; defer the PIN-per-location / location-change idea to a separate meeting.** (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Restructure FlexIQ tasks: create the IP-level FlexIQ epic, attach Andrei's documented capabilities, and redo the AI-assisted mapping that wrongly treated changes as 1:1 features | TBD (soon) | High | Val insists the capability model be used, not sidelined |
| 2 | Pavel Frolov + Andrei Klimovich | Talk to Genadi Peari to produce / re-solder the two new cables required for the listen-only connection scheme | Before any install (install not before Tue Aug 4) | High | Current cables were built for the in-break scheme |
| 3 | Pavel Frolov / Sergey Tsimanov | Update terminal software — remove IQ's own ticket printing, keep only native Mutha Goose tickets; replan the terminal tasks | ~Jul 30 (next day) | High | Follows from the listen-only reversal |
| 4 | Dzmitry Chudzinau (Dima) + Andrei Klimovich | Continue evaluating the remote software-update / device-fleet-management options (Eclipse hawkBit vs alternatives) and settle the architecture | TBD | High | Flagged as the most critical, least-defined MVP item |
| 5 | Andrei Klimovich | Stop distributing new capability docs / ideas to developers during the MVP; hold the PIN-per-location idea for a separate meeting | Ongoing | Normal | Val: every new doc pulls four pairs of eyes off delivery |

## Open Questions

- Which remote-update / fleet-management tool wins — Eclipse hawkBit or one of the alternatives Dima and Andrei are studying — and the architecture around it (raised by Pavel; unresolved).
- The PIN-per-location behaviour on terminal location change (raised by Andrei via a circulated doc) — parked for a dedicated meeting.

## Dispatch Log

---
*Processed from Teams transcript on July 29, 2026 (scheduled meeting-watcher sweep)*
*Source meeting: IQ Pilot updates Q&A*
