---
type: decision
title: Backend architecture — block-diagram first, then phased MVPs (transactional July-1-2026 priority)
date: 2025-08-14
aliases: [block diagram first, backend architecture MVP plan, transactional products MVP, architecture discovery team]
source-count: 2
status: active
---

# Backend architecture — block-diagram first, then phased MVPs

On the Aug-14 2025 backend-architecture kickoff ([[wiki/meetings/2025-08-14-backend-architecture-cms-transactional-hhr.md]]), [[wiki/people/val-levitan.md|Val]] set the working method and priority for integrating JVL's four back-end threads — the legacy **CMS**, the new **transactional products**, **HHR**, and the **Omni** framework. **Status: active.**

## The rulings

- **Everything moving forward is built on Omni.** The legacy system is "what we have today"; from now on Omni becomes an integral part of everything discussed. [[raw/backend_architecture-august-14-2025.md]]
- **Method: describe the block-diagram architecture of *what* the system does, not *how*.** Val's stated process out of the meeting: the team produces "the overall block diagram architecture that focuses on what needs to be done rather than how," then **define MVPs** from that diagram, then **use cases**, then narrow to the exact architecture (the "how") only on the MVP components. Aaron reinforced "don't create the solution while writing the specification" and pushed a capabilities-driven approach + IEEE-style architecture documentation (kept "as a framework, not a mandate" — Val judged the full doc set possibly "overwhelming for a company of our size"). [[raw/backend_architecture-august-14-2025.md]]
- **Transactional products are the *calendar* priority, not the *architectural* priority.** They must **hit the Georgia market by July 1 2026** (the legislative "turn the key" date) and start reaching it ~**January 2026** (beta at the Georgia warehouse/showroom). CMS technological/architectural debt and HHR are real but sequenced behind the transactional deadline. [[raw/backend_architecture-august-14-2025.md]]
- **Business requirements that drive the architecture** (Val, on the record): (1) a **non-technical person can hot-swap a broken device** — unpack a POS, power it, it auto-configures into the network, then boxes/labels the old one; (2) payment must be submitted to the processor within **two days**, so accounts are **ACH-swiped within one day** → immediate per-transaction reconciliation/P&L/reporting; (3) **immediate fraud lockout** on any suspected fraud. Val treats InComm's own fraud capability as "of no relevance" — "our own money, our own skin in the game." IT infrastructure must be modern/agile/scalable (July-1 "stampede" risk) with **no local servers to maintain** where possible. [[raw/backend_architecture-august-14-2025.md]]
- **Regular cadence + minimum group.** A recurring **Wednesday + Friday** engineering architecture meeting with the minimum group **Juan Martinez, Will Jones, Nathan Carver, Pavel Frolov**; every ~3 meetings a **broader recap** (adds Val + Aaron). Alex Biratka pulled in for HHR-specific sessions. Tools: **GitHub + Jira + Mermaid diagrams**, moving away from Confluence/Miro. Val attends the recaps as an optional observer; a follow-up review was set ~**a week and a half** out. [[raw/backend_architecture-august-14-2025.md]]

## Phased plan (from the derived undertakings doc)

The [[raw/backend_architecture_meeting_undertakings_august_14_2025.md|action-items/undertakings doc]] (a §12 derived summary of the same meeting) firms the above into a dated, owner-assigned plan. (These specifics — exact dates and named owners — appear in the derived doc, which is more prescriptive than the transcript; recorded as the meeting's undertakings.)

- **Architecture Discovery Team** — Nathan Carver, Juan Martinez, Will Jones, Pavel Frolov — runs a series of meetings over ~10 days to review CMS docs/codebase, HHR requirements (80–95% defined), and transactional-products requirements, and to define the MVP. [[raw/backend_architecture_meeting_undertakings_august_14_2025.md]]
- **Follow-up sessions:** architecture review with the full team **Aug 28–29 2025**; CMS-modernization deep-dive **Oct 15 2025**; advanced architecture (HHR server, reporting, migrations) **Nov 15 2025**. [[raw/backend_architecture_meeting_undertakings_august_14_2025.md]]
- **Phase 1 — MVP for January 2026:** Transactional Products (owner **Nathan Carver** with Juan) — basic **ACH single-day transfers**, Flex-POS + table-top card-dispenser transaction validation, transaction logging, minimal authentication. Minimal CMS support (owner **Pavel Frolov**) — device authentication only, location/terminal-ID management, daily email reports, defer legacy migration. HHR (owner **Will Jones**) — **deferred to Phase 2**, requirements-gathering only. [[raw/backend_architecture_meeting_undertakings_august_14_2025.md]]
- **Phase 2 (Oct 15):** full CMS modernization + Omni migration. **Phase 3 (Nov 15):** HHR server integration, advanced reporting/analytics, complex permissions, legacy migration. [[raw/backend_architecture_meeting_undertakings_august_14_2025.md]]
- **MVP architectural leanings:** minimal Omni usage, direct ACH (no complex orchestration), daily-email reporting, defer lease/RIS/advanced controls, rapid plug-and-play deployment. [[raw/backend_architecture_meeting_undertakings_august_14_2025.md]]

## Related

- CMS-modernization / observability-orchestration-platform substance: [[wiki/topics/persona-driven-design-and-orchestration-platform.md]].
- Transactional-device architecture (hot-swap provisioning, master/slave server-as-software, ACH, fraud lockout, separate payment-processing cloud server): [[wiki/topics/flexpay-business-architecture-payout-devices.md]].
- HHR: [[wiki/topics/hhr-historical-horse-racing.md]].
- Georgia July-1-2026 deadline / rollout: [[wiki/projects/georgia-market-rollout.md]].

## Sources

- [[raw/backend_architecture-august-14-2025.md]]
- [[raw/backend_architecture_meeting_undertakings_august_14_2025.md]]
