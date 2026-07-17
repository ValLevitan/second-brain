---
type: decision
title: Release the e-wallet MVP first (Georgia QAM), build TITO in parallel — and implement full SAS with no truncation
date: 2025-05-27
aliases: [e-wallet MVP release, e-wallet first, full SAS no truncation, version 17b freeze, Georgia QAM release, e-wallet vs TITO architecture]
source-count: 4
status: active
open-commitments: 4
---

# Release the e-wallet MVP first (Georgia QAM), build TITO in parallel — and implement full SAS with no truncation

On May 27 2025, across two same-day meetings — a long derailed FlexSport/FlexPay dev review ([[wiki/meetings/2025-05-27-flexpay-flexport-dev-review.md]]) and a focused e-wallet release-planning session ([[wiki/meetings/2025-05-27-ewallet-release-planning.md]]) — [[wiki/people/val-levitan.md|Val]] locked the near-term FlexPay release strategy. Two intertwined rulings:

## Ruling 1 — the e-wallet architecture ships first; TITO is built in parallel

- JVL now has **two mutually exclusive architectures**: the **e-Wallet** architecture (also "Electronic Wallet" / "Temporary Wallet") built from **FlexPort + FlexKiosk (FlexPay)**, with essentially **no SMIB**; and the **TITO** architecture built from **FlexPort, SMIB** plus future hardware (**FlexTower, FlexPOS, FlexTitoServer**). "Две архитектуры в одной существовать не могут" — an operator picks one per location; a single transaction cannot take e-wallet on one side and TITO on the other. [[raw/dev_review_flex-pay_flex-port-may-27-2025.md]]
- The **e-wallet architecture is development-complete and about to go to beta tests**; the TITO architecture is still "в очень сырой форме" (very raw). So JVL releases the e-wallet MVP first while developing TITO in parallel. [[raw/dev_review_flex-pay_flex-port-may-27-2025.md]]
- **May-30 sharpening (evolution, not contradiction):** on the QA-plan call Val restated it more bluntly — the Temporary-Wallet architecture "далеко не пойдет" (won't go far) and "я не буду делать из нее MVP" ("I won't make it *the* MVP"): he's "using it so [the money-cycle] gets built in," consistent with the reusable-money-cycle rationale above. Terminological tension only ("release e-wallet MVP first" = ship it first as the money-cycle vehicle, NOT treat it as the true market product). [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]
- **Rationale — the reusable money-cycle.** Val expects the e-wallet architecture "скорее всего, на рынке не проживется" (probably won't survive in the market), **but** the financial-transaction cycle being built for it "нам понадобится в любом случае" — running a short working e-wallet feature through the full money cycle now makes the later TITO in-house test easy. [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- **The hard deadline (the whole point):** "Если у нас не будет продукта в ноябре месяце, то считайте, что мы весь этот effort, весь год, даже полтора... мы провалились, притом очень сильно провалились" — a **November 2025** product deadline; missing it wastes ~1.5 years of work. [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- **What "release" means here — an In-House Full/Life Cycle Test:** money must actually pass through both the **Incom Bank and the JVL Bank** (real deposit), not just a lab demo; Val budgets "не меньше, чем месяц" for the full testing cycle. Debug environment (resettable Incom debug cards) first, then production credentials. [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]] Incom (via Juan → "John from Incom") agreed to enable an **in-house test location at [[wiki/people/felipe-miranda.md|Philippe]]'s Georgia office** — an unusual permission ("вообще они такое не делают"). [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]

### MVP sub-decisions (the release-planning meeting)

- **Freeze the version and name it properly.** Stop calling the FlexPort build "17b"; give it a proper release version and correct artifact naming/numbering in the repositories for both FlexPort and FlexPay — "Это является релизом, и мы пишем тест-кейсы под этот релиз." No new functionality added to FlexPort now; only bug fixes. [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- **One bill validator only for the first release: JCM UBA.** "в сокращенном варианте мы используем только JCM, UBA-валидаторы"; other validators (and MEI) come later — no time spent testing them now. [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- **All development goes into the repositories from now on** (no more informal beta-version sharing). FlexPort and SMIP repos already exist on JVL GitHub; the **FlexPay Bitbucket→GitHub migration is accelerated to ~1 week** (was mid-June) so production versions build under one naming/numbering scheme via GitHub Actions. [[raw/dev_review_flex-pay_flex-port-may-27-2025.md]] [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- **Defer to a later release:** FlexPort firmware-update-over-the-air and extra FlexPort logging — keep the working **USB firmware-update** for now and pass the full money cycle instead of stalling on these. [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- **Meeting cadence raised to twice a week** given the "very acute stage of release." [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- **Hardware to stage at the Georgia office:** two fully-configured **FlexPay** units (UBA validator, scanner, printer, **Linetech** card dispenser — the previous/original dispenser, not the new one) and **five FlexPorts** — three active (two on non-JVL brands, one on a JVL Flex) plus two spares, with brackets and harnesses. Both debug and production **Incom** card types requested. [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]] [[raw/e-wallet_release_meeting_summary-may-27-2025.md]]

## Ruling 2 — implement the FULL SAS protocol, with no truncation

- Val ruled that JVL must **implement the entire SAS protocol without any truncation or abbreviation** — "решение, которое мы должны сделать, это то, что мы имплементируем весь САС протокол без Truncated." Whether a given SAS capability (e.g. AFT) is *used* now is a separate question; the *architecture and hardware* must assume full SAS. [[raw/dev_review_flex-pay_flex-port-may-27-2025.md]]
- **Why:** all major Class III manufacturers now on the Georgia COAM market — **Light & Wonder, IGT, Bally, Novomatic, Konami** — ship the full SAS implementation including **AFT** ("Advanced Funds Transfer"), and "they do not truncate their SAS commands." The earlier assumption that JVL could use a truncated SAS created an "artificial scope gap" that would have crippled FlexPort's use as an AFT display. Full SAS supports AFT, and to a non-engineer an "AFT display" looks much like a FlexPort. [[raw/dev_review_flex-pay_flex-port-may-27-2025.md]]
- **MVP still applies:** JVL implements only the SAS/MVP commands needed for the Georgia QAM launch now, but designs so the rest can be completed later — "с точки зрения delivering продуктов по MVPs, наша схема не меняется." [[raw/dev_review_flex-pay_flex-port-may-27-2025.md]]
- **Dissent noted (Pavel Frolov):** at the close, [[wiki/people/pavel.md|Pavel]] stated his own view that JVL "никогда не понадобится полная поддержка САС" — no player-tracking / switchboard vendor ever supports full SAS; they implement only the player-facing commands they need, and AFT is only required if JVL wants card-based money-in/out. Val's ruling (implement all of SAS regardless of current use) stands over this; recorded as a genuine engineering disagreement, resolved by Val's ruling, not an unresolved contradiction. [[raw/dev_review_flex-pay_flex-port-may-27-2025.md]]
- This continues the Mar 27–Apr 7 scope-gap arc — see [[wiki/decisions/2025-03-28-flexpay-support-tito-non-jvl-locations.md]] and [[wiki/decisions/2025-04-07-flexsmib-modern-flexport-legacy.md]]; the TITO/Flex-family device catalog is on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] and the engineering thread on [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]].

## Open commitments

- [ ] Dmitri Chudinov — finish the FlexPay **partial-redemption** feature (frontend done; builds/tests) and the ticket-report screen — due ~May 28 — [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- [ ] Pavel Frolov — coordinate the Incom in-house test at Philippe's Georgia office (debug then production credentials), keeping tight proactive contact with Juan/"John" at Incom — due this week (first priority) — [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- [ ] Evgeny's team — migrate FlexPay from Bitbucket to GitHub with proper release versioning/imaging — due ~1 week (was ~June 15) — [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- [ ] Someone (was owed by "Sasha") — produce the document laying out all the architectures so the e-wallet-vs-TITO split is unambiguous — due unspecified — [[raw/dev_review_flex-pay_flex-port-may-27-2025.md]]

## Sources

- [[raw/dev_review_flex-pay_flex-port-may-27-2025.md]]
- [[raw/release_e-wallet_flex-pay_flex-port-may-27-2025.md]]
- [[raw/e-wallet_release_meeting_summary-may-27-2025.md]]
- [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]
