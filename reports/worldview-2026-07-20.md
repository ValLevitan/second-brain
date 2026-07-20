# The world as this second brain currently sees it — 2026-07-20 (essay #4)

*Written fresh from the wiki pages only, at the August-close boundary (through ~end of August 2025 of the ingested timeline — roughly the first two-thirds of 2025, batch ~69). Numbered paragraphs for reference. Interpretation is labelled; open contradictions are named, not resolved. Written without leaning on essays #1–3.*

## The world in one page

¶1. JVL is a slot-machine company that, over the summer of 2025, **narrowed itself to a single bet with a hard deadline**. The corporate frame is unchanged — **JVL Labs** (Canadian parent, Inna Levitan ~91%) over US operating entities **JVL Systems** and **JVL Gameworks**, plus Colombia, a closing Mexico, a written-off Peru, and a Canadian manufacturing arm now scheduled to **stop existing by ~November–December 2025** (production moving to Georgia/Louisville). But the strategic story is no longer "two engines running at once." Val has made an explicit **decision to exit the online-gaming/RGS business** (mid-July: "я принял решение от онлайн отойти") and pour everything into **transactional products** — the FlexPay/FlexPort payout ecosystem — plus the small-but-steady **ECHO amusement** device sold on Amazon.

¶2. The forcing function is now singular and dated: **Georgia's cash-out-to-gift-card mandate on July 1, 2026.** After that date, COAM winnings must move onto MasterCard gift cards — "legally no allowable cash processing." Everything transactional (Flex-POS, the card dispenser, FlexPort, the CMS payment hub, InComm integration, ACH) is being built to be in-market by that date. This is the spine the whole company now bends around.

¶3. Underneath sits a still-deepening engineering + tooling rebuild — GitHub/Jira restructured around "capabilities," games consolidating on the **Omni** framework, an **ARM/Rockchip** embedded board shared across Flex-POS/dispenser/tower, **Keeper** now chosen for secrets (superseding the Delinea trial), **Business Central** as ERP — and, most tellingly, a **methodology turn** that explains why this wiki exists at all (¶13).

## The most central people

¶4. **Val** remains the single center of gravity — ruling on architecture, hardware, pricing, hiring geography, game math, and finance, in nearly every meeting. His concentration of authority is, if anything, more visible now that the strategy has narrowed to his personal conviction about transactional products.

¶5. On engineering/tooling: **Aaron Bockelie** (AI/tooling partner, now articulating a whole "two cultures / collective exceptionalism" operating model and an "AI-as-SRE" serverless direction); **Pavel Frolov** (engineering director, being pushed toward a feature-lead role); **Nathan Carver** (Code Carver — risen fast to technical-product-manager, owns the GitHub "capability/FR" dashboard and the transactional-products MVP); **Efim Podvoiski** (RGS/math, the "Ethan"); the **Khandov** father-son pair; **Anton Leshkevich**, **Alexander Biratka**, **Eugine Yavorski / Evgeniy Alekseev / Evgeny Kharetski** (the three-person Evgeny cluster) on Omni/embedded. Testing/QA runs through **Irina Shishko** (VP Engineering + Director of QA), distinct from game-developer **Irina Makarych**.

¶6. On commercial/field/finance: **Juan Martinez** (now central to the transactional rollout — CMS, InComm, ACH, personas); **Felipe Miranda** (Georgia sales/demos, the GACOAM show); **Will Jones** (elevated to **HHR lead**); **Andrei Klimovich** (ECHO/Amazon commerce and marketing). Finance runs through **Alka Sood** with **Igor Donis** (controller). A recurring American FlexPay/Georgia colleague, **"Bob,"** is *still* unidentified after ~69 batches — the single most persistent blank in the network.

## State of play at ~end of August 2025

¶7. **The transactional architecture converged into a phased plan.** Across a dense July–August arc (e-wallet deep-dive → message-queue replication → CMS block-diagram sessions Aug-20/22/27) the shape settled: a **payment-hub-first** build (~2 months), Flex-POS supported on the **legacy CMS (Mother-Goose schema)** so locations can be set up **from Jan 1, 2026**, with a new cloud CMS built in parallel. Event-driven message-queue replication replaced the earlier "clustering" idea; the CMS is a separate cloud server (AWS now, "Azure later — not decided"); FlexPort is a strict slave device; the stack is Linux/MySQL/Java/React. The e-wallet ticket carries two counters (playable vs redeemable). Hardware is the shared ARM board (~$35 assembled).

¶8. **A block-diagram-first, spec-driven discipline was imposed.** The Aug-14 backend-architecture decision mandates "the overall block diagram… what needs to be done rather than how," targeting a Jan-2026 MVP. On Aug-22 a "Spec-Driven Development Process v2.0" formalized "no code without specification, no specification without requirements," wired into JIRA↔GitHub with a `/specifications/CAP-XXX` layer.

¶9. **Games/markets:** the **Player Behavior Simulator** (commissioned Aug-7) responds to a real problem — Fiery-Ice-Link/"Gayocho" negative-win-days at three Florida casinos — a tool to "emulate the player, not the math." **HHR (historical horse racing)** emerged as a new standalone product line (Will Jones lead; Ainsworth's HHR server, operational since 2018; Omni-based, ~95% the same CMS). The **GACOAM trade show** (~500 attendees) produced competitor intel and a distributor-commission (~20%) go-to-market. **Georgia** remains the anchor; Class-B countertop machines price ~$6.5–8k.

¶10. **ECHO/Amazon** is the retained consumer arm: B2B pivot at $3,300, a website launch ~Aug-10, Instagram 70→2,500-follower ambitions, and Val pushing for ≥100 machines/month into 2026. **Finance:** the ~$14M loss carry-forward and loan-book restatement persist; a cash forecast now runs to 2027; banking/ACH mechanics (debit locations within 24h, credit InComm) are being formalized.

## Through-lines

¶11. **Legislation is still product strategy** — the entire transactional build is a race to beat Georgia's July-1-2026 gift-card mandate, exactly as earlier moves raced Class-II/skill-vs-gambling law.

¶12. **Narrowing and build-to-throw-away.** The summer's defining move is *subtraction*: exit online, wind down Canadian manufacturing, ship the e-wallet knowing it may fail (for the reusable money-cycle), one ARM board across devices, current-CMS-first then replace. Val repeatedly frames focus and reuse as leverage.

¶13. **AI is now the operating model, not just a tool.** The Aug-26 turn is the clearest statement yet: Val concludes JVL **cannot reliably author user stories** ("chaos… fantasies and hallucinations") and **drops that layer entirely**, replacing it with **AI-interpreted specifications distilled from recorded developer conversations.** The Aug-28 Omni-animation call was *recorded expressly to generate a spec.* This is the second brain's own ancestor, stated in the sources: the company is reorganizing its engineering around AI reading its meetings — which is exactly what this wiki is.

## What changed since essay #3 (mid-June)

¶14. Three things hardened. (1) **Strategy narrowed** from "two engines" to "transactional + ECHO, exit online." (2) **The deadline became the spine** — July-1-2026 now dates nearly every engineering commitment, with a concrete Jan-1-2026 location-setup milestone. (3) **AI moved from obsession to operating method** — the user-story drop is a structural change, not an enthusiasm. Secrets settled (Keeper). Canadian manufacturing got an end date. Nathan Carver rose to own the MVP.

## Honest uncertainty (what this brain understands least well)

¶15. **"Bob" is still unidentified** after ~69 batches — a genuinely central American FlexPay/Georgia node the wiki cannot name.

¶16. **Can the transactional stack actually ship by July-1-2026?** The plan is now explicit and phased (payment hub ~2 months, Jan-1 location setup, current-CMS-first), but it is a plan; the wiki can see the architecture far better than any shipped product. The ACH provider is unchosen (Stripe is only a modelling example), and the new CMS is being built in parallel with a legacy-CMS stopgap — classic execution risk.

¶17. **The Amazon/ECHO commerce entity is now a FOUR-way open contradiction** (owner-held discovery test): sources variously place Amazon commerce under **JVL Systems**, **JVL Gameworks**, **"Cheil Games,"** and **"Game Brokers."** Correctly left unresolved; but it means the wiki cannot yet say which entity actually books the ECHO revenue.

¶18. **Profitability and burn remain invisible by design** (§15.8). Revenue anchors exist ($10M/30% from earlier; a 2027 cash forecast now referenced) but margin, burn, and whether the narrowed bet is affordable before July-2026 are unknown.

¶19. **Coverage is heavily engineering/architecture-weighted** for the summer — FlexPay/CMS/Omni/Git standups dominate; the actual Georgia installed base, real ECHO sales numbers, and the online business being wound down are comparatively thin. Two files were even mis-sorted by month (a June-4 decision meeting and a May SD-operator list surfaced only when the September folder was swept), a reminder the record's completeness depends on filing discipline.

¶20. The five questions this brain would most want answered: (1) **Who is Bob?** (2) Does the transactional stack ship — payment hub, Flex-POS on legacy CMS, Jan-1 location setup — before July-1-2026? (3) Which entity actually runs Amazon/ECHO commerce (Systems / Gameworks / Cheil Games / Game Brokers)? (4) Is the narrowed company profitable, or is the build outrunning the money before the deadline? (5) Does the "AI-interpreted spec instead of user stories" method actually produce shippable software — i.e., does the operating-model bet work?

*Interpretation throughout (emphasis, "narrowing," "the deadline is the spine," "AI as operating model") is mine as synthesizer, for the owner to correct; underlying facts trace to wiki pages. Where the wiki holds an open contradiction it is named, not resolved.*
