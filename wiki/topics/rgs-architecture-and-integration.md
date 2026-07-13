---
type: topic
title: RGS architecture and operator integration
date: 2025-02-01
aliases: [RGS, remote game server, RGS API, math container, direct integration, reverse integration, Golden Palace, Digitain, Hub88, BetConstruct, Comtrade Gaming, Postman, OpenAPI]
source-count: 3
open-questions: 2
---

# RGS architecture and operator integration

How JVL's **RGS** (remote game server) is built and how JVL connects it to online-casino operators and platforms. This is the technical/engineering side of the online-games business; the commercial/market side lives in [[wiki/topics/online-games-rgs-distribution.md|Online games / RGS distribution]]. Owned technically by [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] (the RGS author). [[raw/Aaron_Val_2025-02-11.md]]

## What the RGS is (Efim's description)

- The RGS sits **between the online game (running in the browser) and the wallet**, and connects the game to its **math container**. Its two jobs: connect the game UI to the math, and connect the game to the wallet so real-money bets and wins work. It does **not** hold game mechanics itself — mechanics live in the browser game and the math lives in the math container. [[raw/Aaron_Val_2025-02-11.md]]
- Internally it is a **set of containers orchestrated by Kubernetes**, with a transaction database of current sessions; described as a "temporary storage and transport framework." Nothing in it is secret except the **math**; the protocols/tables could be shared if the database were protected. [[raw/Aaron_Val_2025-02-11.md]]
- The **math container is the only dynamically changing part**: to add a game you drop in a new math container; the RGS and its API do not change. [[raw/Aaron_Val_2025-02-11.md]]
- The API is **very narrow — roughly four calls** (start session/get player parameters, bet, win, plus roll-back/repeat-win); a few optional operator→RGS calls are used to synchronise/check wins and show games in a back office. [[raw/Aaron_Val_2025-02-11.md]]

## Two ways to integrate

- **Reverse integration** — the RGS implements the API the platform dictates (JVL adapts to them). [[raw/Aaron_Val_2025-02-11.md]]
- **Direct integration** — JVL dictates which API the platform uses (the operator adapts to JVL's API). [[raw/Aaron_Val_2025-02-11.md]]
- Efim says JVL's API is no more complicated than the APIs JVL itself integrated with by reverse integration, and integrators reading the document have not called it unusual or hard. [[raw/Aaron_Val_2025-02-11.md]]

## Current integrations (as of Feb 1 2025)

- **Digitain** — the **first** integration; it was **reverse** (JVL integrated to them) and is **complete**. [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- **Golden Palace** — the **first Direct integration**; JVL gave them documentation for JVL's API. As of Feb 1 it is **still in progress** (Efim believes they have no more integration questions, but no formal "integration complete / start rolling out games" green light had been given). JVL has no shared task board with the operator, so visibility into their progress is limited. [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- **Hub88** and **BetConstruct** (transcribed "Bad Construct") — aggregators JVL is integrated with via its RGS; connecting through Hub88's API reaches the wallets Hub88 supports without integrating each wallet separately. [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- **EveryMatrix** — the aggregator the land-based/online games reach operators through (see [[wiki/topics/online-games-rgs-distribution.md]]). [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- **Comtrade Gaming** and others (Intzimmer, Chromatic, Intergame — spellings as transcribed) — named by Aaron as example remote-gaming-server vendors that publish specifications, examples, and known capabilities, held up as the pattern JVL should follow. [[raw/Aaron_Val_2025-02-11.md]]

## Where the source lives and the Git migration

- The RGS source is in **SVN** ("RSVN"), not Git, and there was **no plan yet** to move it (Feb 11). Aaron pushed that it must move to Git before any real analysis can start. [[raw/Aaron_Val_2025-02-11.md]]
- In the Feb 11 repo-structure meeting, moving RGS to GitHub was sequenced as migration **step 2** (after Omni, Miranda and FlexPay), because Efim said it is a real production project and a multi-day job. See [[wiki/decisions/2025-02-11-git-migration-sequence.md]]. [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- The RGS deploys on a **Kubernetes cluster** in JVL's cloud (three AWS regions: Canada, Europe, Singapore); JVL also runs its online application from a hosted Kubernetes cluster. [[raw/JFrog transcript - February-6-2025.md]] [[raw/Aaron_Val_2025-02-11.md]]

## The "easy-integration" goal (Aaron and Val)

- Aaron pressed that JVL should be able to hand an operator a **Postman collection** for the RGS API and/or expose it as an **OpenAPI** document, so tools can read the endpoints directly — the basic hygiene needed before offering integration to outsiders. Efim had not used Postman. [[raw/Aaron_Val_2025-02-11.md]]
- Val's larger vision (his "dream integration"): an operator self-serves on a JVL website — reviews/marks-up/signs the contract online — and then RGS integration happens almost automatically, "like downloading an installer," instead of engineer-to-engineer Skype threads. Val cited having connected Atlassian and GitHub via MCP through VS Code (done for him by an IT person in ~45 minutes) and Cline's new MCP marketplace as proof such near-automatic connection is possible. See [[wiki/topics/online-games-rgs-distribution.md]] (marketplace). [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- Efim's counter-view: the important thing to protect is the math container (plus 2–3 nodes); everything else can be documented and published, and each integration makes the docs better. Val respects but does not fully accept this — he notes Efim is a mathematician, not an architect, and did not design/program the RGS. (Recorded as differing views, not a contradiction between sources.) [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]

## Open questions

- Can the near-automatic "installer-magic" RGS integration actually be achieved, given that JVL cannot control the (varying) API quality on the operators' side? — [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- Is the Golden Palace direct integration actually finished? (Efim thinks the questions are done; no formal completion confirmation was seen.) — [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]

## Sources

- [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- [[raw/JFrog transcript - February-6-2025.md]]
- [[raw/Aaron_Val_2025-02-11.md]]
