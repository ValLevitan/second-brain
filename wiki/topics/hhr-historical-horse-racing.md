---
type: topic
title: HHR (Historical Horse Racing) product
date: 2025-08-14
aliases: [HHR, Historical Horse Racing, Ainsworth HHR, Omni HHR Land Based Overlay]
source-count: 2
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

## Project digest (written artifact — architecture/requirements phase)

A written **"JVL HHR Project — Executive Digest"** (§3 non-transcript artifact; undated, but its content self-describes the **architecture/requirements phase (Q1 2025)** with **implementation slated June/July 2025**, "delayed due to Omni platform priorities" — so it captures the phase *before* the Aug-14 kickoff above; recorded here as project color, not current state). It synthesizes the team's HHR design debate — the [[wiki/people/efim-podvoiski.md|Efim]] / [[wiki/people/will-jones.md|Will]] / [[wiki/people/juan-martinez.md|Juan]] quotes indicate it was distilled from an HHR working session. [[raw/jvl-hhr-executive-digest.md]]

- **Partner + platform.** JVL is developing HHR terminals via a partnership with **Ainsworth**, adapting JVL's gaming framework to Ainsworth's HHR **server infrastructure (operational since 2018)**. The central engineering challenge: **reconciling three parallel state machines** while preserving the player experience during system failures. [[raw/jvl-hhr-executive-digest.md]]
- **Strategy = fault-tolerance / player-experience-first.** Unlike competitors who lock machines during connection issues, JVL aims to **keep gameplay running on cached race tickets** (soft tilts, not hard locks). Architecture is **dual-layer**: a legal-compliance layer (historical races determine all outcomes) hidden behind an entertainment/slot-style presentation layer. [[raw/jvl-hhr-executive-digest.md]]
- **Caching + comms.** **10 race tickets cached per bet level** enable offline play during server outages, with **graceful degradation** (disable an individual bet level, not the whole machine); asynchronous message handling with a **critical-message queue** and **heartbeat monitoring** (configurable timeout tolerances). [[raw/jvl-hhr-executive-digest.md]]
- **The open decision points the team was wrestling.** Ten named struggles: (1) the **state-machine paradox** (three parallel processes resist a single clean diagram — Efim); (2) the exact **"when can players play?"** conditions ("a lot of conditions" — Efim); (3) **connection-loss philosophy** — Efim favors continuity (don't re-register after a 1-min drop) vs Will favors consistency; (4) **extra-winnings trigger** (pool-based vs pattern-based — "we put a question mark"); (5) **progressive-jackpot offline behavior** (Juan: continue until tickets depleted; Will: configurable per jurisdiction); (6) **critical-message hierarchy** (blocking vs non-blocking); (7) **manual handicapping** needing a synchronous server response in an async system; (8) **power-loss recovery** of mid-game state; (9) **race-ticket depletion strategy** (disable whole machine vs just that bet button — Juan prefers keeping other levels playable); (10) **game-history storage depth** (regulator wants 50 games, but multi-stage games could need **2,500+ records**). [[raw/jvl-hhr-executive-digest.md]]
- **Lockup rule (corrected).** A large-win lockup occurs only when **BOTH** conditions hold: win **≥ $600 AND** win **> 300× the bet** — not either independently. [[raw/jvl-hhr-executive-digest.md]]
- **Documentation-first posture.** The team documents extensively before implementation (Will: within ~4 weeks he doubts he'll have more user stories to write). Not-yet-created at digest time: the formal **state-machine diagram** (Efim committed to it) and the **progressive-translation layer** (HHR progressive → standard progressive-controller format); waiting on **Ainsworth** for reconnection/re-registration requirements and the extra-winnings algorithm. [[raw/jvl-hhr-executive-digest.md]]

## Open questions

- The **Ainsworth terminal + server in the Georgia office keeps crashing / corrupting / interfering with the office Internet** after being left on overnight, so it has been turned off in favour of the office's own connectivity — unclear whether the fault is Ainsworth, the AT&T Internet service, or something else; Val's fix was to simply add a second ~$100/month Internet connection. [[raw/backend_architecture-august-14-2025.md]]

## Sources

- [[raw/backend_architecture-august-14-2025.md]]
- [[raw/jvl-hhr-executive-digest.md]]
