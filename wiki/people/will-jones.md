---
type: person
title: Will Jones
date: 2025-03-20
aliases: [Will Jones, Will]
source-count: 5
open-commitments: 1
open-questions: 1
---

# Will Jones

(Surname **Jones** owner-confirmed 2026-07-15. Engagement form — consultant vs hire — **owner-deferred 2026-07-15: Val doesn't recall; resolve from future sources by context, do not wait on owner.**)

Will is a Class II (bingo-based slot) gaming expert working with Val on JVL's entry into Class II. His background: he worked "with the bingo system at SDG and Valley" (transcript spelling; "Valley"/"Bali" in this transcript are consistent with the gaming company Bally, of which SDG was a compartment — inference) and did installs at the Seminoles and other tribal properties. Surname not given in the source. [[raw/class_2_bingo_engine.md]]

## Role in the Class II effort (Mar 2025)

- Led the Class II bingo-engine explainer session — Class II standards history, the omission of bingo game rules, implied rules, accepted norms, and a candidate game-rule design worked out with the mathematician on the call. See [[wiki/topics/class-2-bingo-gaming-strategy.md]]. [[raw/class_2_bingo_engine.md]]
- Val asked him how long a schematic-level architecture design would take at 100% of his time: his answer — an architectural-level drawing "no more than a couple of weeks"; refining it to the real direction "might take eight weeks" at worst; from no design to the eventually-implemented one "is nothing more than… four week task tops," assuming help from JVL engineering. (He is outside the JVL engineering team — he says the work "does assume… the assistance of people, resources within the JVL organization.") [[raw/class_2_bingo_engine.md]]
- Advocates an outside legal review validating the game engine "is, in fact, bingo" before approaching the first customer, plus a patent search by outside specialists (he says he is "not great at searching for patent stuff"). [[raw/class_2_bingo_engine.md]]
- Contacts he offered: "Losh" (transcript spelling) — an attorney from the old SDG days with much Class II experience, now in his own business; and a friend in Boulder who used to work at SDG and "would know specifically people to call." [[raw/class_2_bingo_engine.md]]
- On architecture: prefers planning for cloud-hostable services without excluding on-premise ("private cloud") installs, and says two-or-three heads working the design beats one ("two heads are better than one… once you get past that, it's too many"). [[raw/class_2_bingo_engine.md]]

## Aug 14 2025 — HHR lead on the backend-architecture kickoff

By August Will is JVL's **HHR (Historical Horse Racing) lead** and a core member of the new backend-architecture working group. On the [[wiki/meetings/2025-08-14-backend-architecture-cms-transactional-hhr.md|Aug-14 kickoff]] he: [[raw/backend_architecture-august-14-2025.md]]

- Summarised the **HHR** state — Ainsworth partnership, a working terminal+server in the Georgia office, ~80–95% of requirements/user-stories defined, built on Omni, the 8-race bingo-card outcome model, and a likely on-prem/offline-tolerant HHR server. Full detail on [[wiki/topics/hhr-historical-horse-racing.md]]. [[raw/backend_architecture-august-14-2025.md]]
- Worked the CMS/back-end **requirement space** hard — pushing to identify integral functions vs optional features, flagging which components carry regulatory approval (the "red zone" on the device), and cataloguing the feature sets (terminal enablement/setup, operational management, accounting/3rd-party integration; no player tracking). He came at it "a little bit removed and now coming back in." [[raw/backend_architecture-august-14-2025.md]]
- In the phased plan (derived undertakings doc) Will **owns HHR**, which is **deferred to Phase 2** (requirements-gathering only for the Jan-2026 MVP), with an advanced HHR-server session set for Nov 15. He sets the Mon/Wed/Fri (6 AM) meeting rhythm, landing on **Wednesday + Friday**. See [[wiki/decisions/2025-08-14-backend-architecture-block-diagram-first-mvp.md]]. [[raw/backend_architecture_meeting_undertakings_august_14_2025.md]]

## Aug 20 2025 — CMS/PayFlex block-diagram review

On the [[wiki/meetings/2025-08-20-cms-payflex-block-diagram.md|Aug-20 block-diagram review]] (session 1 of 3) Will — introduced to Nathan and being brought up to speed on PayFlex — worked the requirement/architecture questions from his regulated-gaming background: he probed the SAS host modes (controlling vs listening-only) and confirmed JVL sits on the **secondary SAS** (Intralot holds primary), pressed on player-anonymity/federal money-laundering concerns (none apply — these are anonymous prepaid cards), and pushed the transition strategy — "you can't wipe out an ecosystem and rewrite" it; keep the legacy as "baggage," start with what's new, choose the right data store per service, and probe the cloud/B2B-with-InComm design. [[raw/CMS- Block Diagram_Arch.md]]

## Sept 9 2025 — executive-developer alignment 1:1 (back-office/transactional)

On a [[wiki/meetings/2025-09-09-back-office-architecture-will-jones.md|Val↔Will 1:1]] (12:20 PM) Val cast Will as an **executive** who helps define the requirements/capabilities for the whole transactional back-office and acts as a **two-way conduit** between the executive level and the developers (facilitating/mentoring Pavel; content translated to Russian for Minsk). Will prefers **user stories** over use cases and pushed the **piece-by-piece** migration philosophy — solve the biggest business problem first, treat the **B2B InComm connection hosted in Azure** as the one definitively-new priority piece, and keep the future architecture as a guiding vision rather than uprooting the legacy CMS at once. He framed the operator-non-payment exposure (JVL owes InComm before it holds the location's cash) as a functional requirement: JVL must quickly identify any operator who didn't settle by ~3–4 AM. Substance on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Sept-9 section). [[raw/back-office_architecture-will_jones-september-9-2025.md]]

## Open commitments

- [ ] Will — capture the session's extra ideas (golden-ball / must-hit-by, progressive segmentation) with his notes ("I wrote down what we were talking about there too, so I'll make sure they get captured") — due unspecified — [[raw/class_2_bingo_engine.md]]

## Open questions

- What is Will's surname and his formal engagement with JVL (consultant vs employee)? Not stated in the source. — [[raw/class_2_bingo_engine.md]]

## Sources

- [[raw/class_2_bingo_engine.md]]
- [[raw/backend_architecture-august-14-2025.md]]
- [[raw/backend_architecture_meeting_undertakings_august_14_2025.md]]
- [[raw/CMS- Block Diagram_Arch.md]]
- [[raw/back-office_architecture-will_jones-september-9-2025.md]]
