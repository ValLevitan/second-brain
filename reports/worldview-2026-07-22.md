# The world as this second brain currently sees it — 2026-07-22 (essay #5)

*Written fresh from the wiki pages only, at the **all-of-2025-complete** boundary (through end-December 2025 — the full year ingested, ~batch 94, 502/967 files, ~667 content pages). Numbered paragraphs for reference. Interpretation is labelled; open contradictions are named, not resolved. Written without leaning on essays #1–4.*

## The world in one page

¶1. By the end of 2025, JVL is **a slot-machine company that has bet the house on becoming a payments company**, under the near-total personal direction of its owner **Val Levitan**. The corporate frame at year-end: **JVL Labs** (Canadian parent, Inna Levitan ~91%) over US operating entities **JVL Systems** and **JVL Gameworks**; Colombia active; **Mexico and Peru closed**; and — the year's biggest structural change — **Canadian manufacturing wound down** (facility closing Nov/Dec 2025, production consolidated to Georgia under Elizabeth). Finance ran on RBC/BDC, with a year-end consolidation putting **2024 revenue at ~$12.5M** and **2025 net income around $2.3M** (interpretation: these are the visible anchors; margin/burn remain largely §15.8-dark).

¶2. **The whole company now points at one deadline: Georgia's cash-out-to-gift-card mandate in 2026** (sourced as June-1 in some sessions and July-1 in others — an evolving date the owner has ruled is not yet worth pinning). Everything transactional — **FlexPort** (the in-machine device), **FlexSMIB**, **Flex-POS** (the ARM/Rockchip payout terminal), the **payment hub** (Java/Postgres cloud service with a **Dwolla** ACH adapter and **Plaid** account verification), and **InComm** gift-card rails — is being built to be in-market by then, with a **January 2026 beta / go-live** as the near-term forcing function.

¶3. Underneath, 2025 was the year JVL **rebuilt how it builds**: consolidated ~11 GitHub orgs toward ~2, stood up a formal release-management pipeline and docs-as-code, migrated finance from Navision to **Business Central** (Jan-1-2026 go-live), and — most distinctively — **turned AI into its operating model**: dropping human-authored user stories in favor of **AI-interpreted specifications distilled from recorded engineering conversations**. That method is the literal ancestor of this wiki.

## The most central people

¶4. **Val** is the center of gravity to a degree the record makes almost uncomfortable — he rules on hardware partitions, ACH vendors, game math, loan reconciliation, UI button colors, and hiring geography, personally, in nearly every meeting.

¶5. **Engineering/tooling:** **Aaron Bockelie** (AI/tooling architect — spec-driven method, GitHub/release pipeline, Rockchip board bring-up); **Pavel Frolov** (engineering director, the "bulldozer"); **Nathan Carver** (Code Carver — technical-product-manager, payment-hub/capability owner); **Efim Podvoiski** (RGS/math); the **three Evgenys/Zhenyas** — **Yavorski** (FlexPort integration software), **Alekseev** (embedded + boards, in Genadi's orbit), **Kharetski** (LGS/Omni backend) — an owner-ruled, exhaustive-at-three cluster; **Dmitri Chudinov** (FlexPay back-end); **Andrei Bosik** (DevOps); **Ivan Shpakov** (release/GLI); **Irina Shishko** (VP Engineering + QA), distinct from game-developer **Irina Makarych**.

¶6. **Hardware/product/commercial:** **Genadi Peari** (hardware/industrial, board manufacturing); **Michael Gottlieb** (SVP Game Design) with **Lena Zhukova**'s art team (**Anastasia**, **Yulia**, **Sergey Kleimenychev**); **Juan Martinez** (product/markets, payment-hub personas); **Felipe Miranda** (Georgia sales); **Andrei Klimovich** (ECHO/Amazon). **Finance/back-office:** **Alka Sood** (controller, winding down ~Feb-2026) with **Igor Donis**, **Lev Rudky** (BC), **Monica**, and **Mikhail Perelman** (procurement).

¶7. And a genuinely central node the wiki *still cannot name*: **"Bob"**, the recurring American FlexPay/Georgia colleague — unidentified across the entire year.

## State of play at end-2025

¶8. **The payment hub is specified and entering build.** A Nov 5–10 ACH-module-spec arc settled the architecture: Dwolla adapter (no secrets stored; Plaid verifies accounts; ~$5k/mo + penalties), a reconciliation module as the "primary core," provider-switchable adapters, KYC over $10k, and a unified "POS registration procedure." The Dec FlexPort/SMIB syncs pushed into implementation — multi-denomination cash-out emulation, a new WSS "cancel-transaction" command, and a **long-term stability test running all four machines** over the holidays, reconvening Jan-5.

¶9. **Hardware converged on the Rockchip ARM board with a "no-China-dependency" goal.** Aaron demoed a from-source Buildroot/U-Boot image on the "blue" board; the field-update mechanism (partition-only app update, boot-time USB script, backup/rollback, a 15-minute no-reconnect alert) was designed; the own-STM-board option was deferred (~3 months) to keep shipping.

¶10. **The engineering operating-model shift is real and institutionalized.** "Reverse Omni into a spec," recorded interviews → AI requirements → AI specs → features + acceptance criteria → Ivan's test cases; ChatGPT wired to Atlassian via MCP; "if it isn't written, it doesn't exist." Business Central replaces Navision Jan-1; GitHub org consolidation and a release pipeline (lint→test→build→release, artifact bundles) are in flight.

¶11. **Games and markets** kept moving but as a supporting act to the transactional bet: Omni-framework consolidation, a **10:1 cloning** production strategy (e.g. La Rosa = Lion's Riches reskin), Cool Cat Keno / Black Hills Keno, and market work across **Georgia** (anchor; ~35k machines / 6.5k locations), **South Dakota** (iVizion firmware approved; #1 win-per-unit on six games), **Nebraska** (approval ~Dec-1), and **Texas** (skill-game strategy; 2025 ban died → next 2027). The **online/RGS business was formally exited** (July) to focus on transactional + **ECHO** amusement (Amazon B2B, influencer marketing, a website relaunch).

## Through-lines

¶12. **Narrowing to one bet.** The 2025 story is subtraction — exit online, close Mexico/Peru, wind down Canadian manufacturing, ship a reusable money-cycle — all to fund and field the transactional products before the Georgia deadline.

¶13. **Legislation as product strategy**, still: the gift-card mandate, KYC/ACH compliance, Georgia dual-SAS, skill-vs-gambling law in Nebraska/Texas.

¶14. **AI as the organizing principle**, now operational rather than aspirational: the company reorganized its engineering around AI reading its own meetings — which is what this brain is.

## What changed across the full year

¶15. Early 2025 read as a slot company with a payments side-project and a rich, engineering-heavy meeting record (Q1–Q2 dominate the coverage curve — Apr/May alone are ~130 meetings). By year-end it is a payments company with a slot heritage, a hard 2026 deadline, a rebuilt toolchain, and a deliberately AI-driven operating model. The coverage thins sharply in Q4 (Oct 15, Dec 3 meetings) — interpretation: either recording discipline relaxed or the work concentrated into fewer, longer working sessions (the Dec syncs are hour-long weeklies).

## Honest uncertainty (what this brain understands least well)

¶16. **"Bob" is still unidentified** after the entire year — the single most persistent blank.

¶17. **Can the transactional stack ship before the 2026 deadline?** At year-end the payment hub is specified and entering build, the board is in bring-up, and a Jan-2026 beta is the target — but nothing is shown shipped, the ACH build is early, and the deadline's exact date is itself unsettled.

¶18. **The Amazon/ECHO commerce entity is a FOUR-way open contradiction** — JVL Systems / Gameworks / "Cheil Games" / "Game Brokers" — held open by owner design as a discovery test; the wiki cannot yet say which entity books ECHO revenue.

¶19. **Profitability is only partly visible.** 2024 ~$12.5M revenue and 2025 ~$2.3M net income are anchors, but §15.8 holds all compensation, so the largest cost line and the true margin/burn of the transactional build remain dark.

¶20. The five questions this brain would most want answered: (1) **Who is Bob?** (2) Does the transactional stack (payment hub + Flex-POS + board) ship and clear GLI before the 2026 Georgia deadline? (3) Which entity actually runs Amazon/ECHO commerce? (4) Is JVL profitable once the transactional build's full cost is counted? (5) Does the "AI-interpreted spec instead of user stories" operating model actually produce shippable, GLI-certifiable software — the bet the whole engineering org now rests on?

*Interpretation throughout (emphasis, "bet the house," "narrowing," "AI as operating model," the coverage-curve reading) is mine as synthesizer, for the owner to correct; underlying facts trace to wiki pages. Where the wiki holds an open contradiction it is named, not resolved. This closes the 2025 record; 2026 (the final ~440 files) is next.*
