---
type: topic
title: HHR (Historical Horse Racing) product
date: 2025-08-14
aliases: [HHR, Historical Horse Racing, Ainsworth HHR, Omni HHR Land Based Overlay]
source-count: 1
open-questions: 1
---

# HHR (Historical Horse Racing) product

**Historical Horse Racing (HHR)** is a class of gaming where outcomes are derived from the results of previously-run (historical) horse races rather than a live RNG — a compliance path used in several US markets. JVL is building an HHR product on the **Omni** framework, led by [[wiki/people/will-jones.md|Will Jones]]. This page collects the durable HHR facts; the Aug-14 2025 backend-architecture kickoff is the fullest source to date. Earlier appearances (navigation only): the Apr-8 six-product carve named it "**Omni HHR Land Based Overlay**" ([[wiki/decisions/2025-04-07-recarve-gaming-platform-into-six-product-repos.md]]); the Jul-3 games weekly sequenced "adapt Omni to HHR" after Kaio-Ocho ([[wiki/meetings/2025-07-03-game-development-weekly.md]]); ~Jul-15 HHR "slipped to Sept" ([[wiki/meetings/2025-07-15-alignment-planning-catch-up.md]]); the ~Aug-1 weekly review noted "Omni HHR starts Aug-7" ([[wiki/meetings/2025-08-01-flex-pos-weekly-review.md]]).

## State of play (Aug 14 2025)

Will Jones summarised where the HHR effort stands on the [[wiki/meetings/2025-08-14-backend-architecture-cms-transactional-hhr.md|backend-architecture kickoff]]: [[raw/backend_architecture-august-14-2025.md]]

- **Partner: Ainsworth.** JVL opened conversations with **Ainsworth**, who helped define expectations for both the integration and the final product. A **working terminal and server are now in the Georgia office** — though Juan noted a caveat (below). [[raw/backend_architecture-august-14-2025.md]]
- **Requirements ~80–95% defined.** Over the prior six months the team compiled a requirements list and **user stories** from the player / casino / regulator perspective; Will estimates the "what" is defined to "somewhere 80% up to 90 or even 95%," with a few gaps to fill along the way. [[raw/backend_architecture-august-14-2025.md]]
- **Built on Omni.** Direction was already set that HHR lives in the **Omni framework**; discussions dwelled heavily (~50/50 what-vs-how) on how the pieces lay out within the current game, with [[wiki/people/efim-podvoiski.md|Efim]] and [[wiki/people/pavel.md|Pavel]] deciding accommodation. [[raw/backend_architecture-august-14-2025.md]]
- **How the game works.** HHR uses a set number of **races** — Will believed **8 for Ainsworth** (Juan concurred "it's 8 I think") — where the horses the player picks (or the game auto-picks by horse ranking) and the race results produce a **hit/miss pattern "like a bingo card"**; that pattern determines the payout for the player's wager. The **integration point is the game engine** — where the game uses a third-party service to determine actual outcomes, which is integral to when the game is played and how much the player is paid. [[raw/backend_architecture-august-14-2025.md]]
- **On-prem server, offline-tolerant.** Prior architectural discussions concluded the HHR server is **most likely on-premise**, with the system able to keep functioning for some period when **disconnected** from the HHR server (the source of race-ticket sets) — judged more complicated but more resilient. [[raw/backend_architecture-august-14-2025.md]]
- **Next step:** turn the use-case/requirements work into a concrete plan (who/when/what), close the remaining ~10–15% of detail with Ainsworth, and confirm they understand the functions JVL needs. In the Aug-14 phased plan, HHR was **deferred to Phase 2** (Will owns requirements-gathering only for now) with an advanced HHR-server session set for **Nov 15 2025**. See [[wiki/decisions/2025-08-14-backend-architecture-block-diagram-first-mvp.md]]. [[raw/backend_architecture-august-14-2025.md]]

## Open questions

- The **Ainsworth terminal + server in the Georgia office keeps crashing / corrupting / interfering with the office Internet** after being left on overnight, so it has been turned off in favour of the office's own connectivity — unclear whether the fault is Ainsworth, the AT&T Internet service, or something else; Val's fix was to simply add a second ~$100/month Internet connection. [[raw/backend_architecture-august-14-2025.md]]

## Sources

- [[raw/backend_architecture-august-14-2025.md]]
