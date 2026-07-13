# The world as this second brain currently sees it

*Worldview essay #1 — written 2026-07-13 from the wiki pages only (ingested timeline: Jan 2 – Mar 11, 2025; ~7% of the backlog). An owner comprehension check, not a wiki page. Paragraphs numbered for reference.*

¶1 — JVL is a group of companies that designs and builds gambling machines — "video lottery terminals" and amusement/gaming cabinets — and, increasingly, the software and online games around them. The wiki records at least three entities (JVL Systems in the US/Florida, JVL Labs in Canada, a Gameworks arm), engineering concentrated in Minsk, a Mexico warehouse, and sales into several US route markets plus Latin America. You, Val Levitan, are the decision-maker in every meeting; your wife Ina is recorded as the 91% owner.

¶2 — The machines go into "route" markets — bars, stores, gas stations — not big casinos, with Georgia as the core established market and Florida, South Dakota, and Puerto Rico as expansion fronts. Alongside the physical business runs an online-casino games business (the "RGS," remote game server) that distributes JVL's game math to online operators, plus a brand-new consumer product, ECHO, a home gaming device.

¶3 — Across the pages, what you appear to be trying to accomplish (interpretation) is to modernize a hand-built engineering shop into a disciplined software company — Git, automated pipelines, AI tooling, real documentation — while pushing hard into new markets and product lines under constant cost pressure. The tension between "ship the next market now" and "rebuild how we work" runs through nearly everything.

¶4 — The most central person after you is **Aaron (Bockelie)**, an outside software architect/consultant driving the whole engineering modernization: the move off Jenkins to a Git-native pipeline, GitHub adoption, AI-assisted development, docs-as-code, and retiring Atlassian. You note he should be used as a consultant, not an employee. The wiki reads as you and Aaron jointly re-educating the Minsk team.

¶5 — On the commercial/field side, **Juan Martinez** is your right hand: GLI dealings, the South Dakota and Puerto Rico expansions, game creative direction, JIRA product requests. **Pavel (Frolov)** is your engineering director — the build pipeline ("DTP-53"), drivers, printer support, the FlexPort/FlexPay payment hardware. **Genadi Peari** is the hardware lead (the FP7 board, cabling, printers).

¶6 — The Minsk bench is deep and easy to confuse in the transcripts: **Efim Podvoiski** owns the RGS and its game math (he guards the "math container"); **Lena Zhukova** leads game art/design; **Dmitry Khandov** does design/video and tooling; **Andrei Bosik** is being groomed to own DevSecOps and the GitHub migration; **Alexander Biratka** ("Sasha") runs hardware/performance and pipeline work. **Michael** is a game producer working with Juan on slot design.

¶7 — A distinct commercial figure is **Andrei Klimovich**, who runs the online-games/RGS business and the ECHO Amazon push — kept separate in the wiki from Andrei Bosik the engineer. The relationship texture the wiki captures best is you as a forceful, non-technical chairman "throwing ideas at" engineers to extract information; one recorded exchange with Efim over opening up the RGS was openly tense.

¶8 — Outside JVL the recurring players are **GLI** (the certification lab that gates every release), **Elevate** (a specialty lender), **Incom** (a payment processor for the Georgia prize-card kiosk), **CIBC** (US banking), and freight vendors. Per the owner ruling on the Elevate page, Elevate is a **lender** that took a pledge on the machines financing a Colombian operator — not a customer.

¶9 — State of play, mid-March 2025. The **software modernization** has real momentum and is the most thoroughly documented part of the wiki: Git-native build, GitHub-over-Bitbucket, private-by-default repos, a three-layer continuous-delivery architecture, and a staged repo migration are all decided and underway, with the graphics team onboarding to Git LFS.

¶10 — **Hardware** is settled but constrained: after testing, the FP7 board is CPU-bound, so the decision was to optimize rather than upgrade, with a stronger 8000-processor board promised around March 1 and the Omni engine upgraded to Pixi 8.6.

¶11 — The **market rollouts** are the pressured front. Georgia (your core revenue) ships in four staged "Peach" packages under your explicit warning of a ~40% revenue drop there from two new competitors — you named payroll as at risk. South Dakota is in lab testing (Epic 950 printer, release "SDVLT 1.11.5") but slipped from February to early March. Puerto Rico is in licensing outreach as the Peru office closes.

¶12 — The **payment products** (FlexPort hardware ↔ FlexPay kiosk, with Incom) are in active bring-up: by March 11 the integration is near feature-complete, a two-machine office test is planned, firmware-update and bill-acceptor cabling still pending. On the **design** side, games must now be signed off on final assembled machines from Georgia (triggered by a "Kai-Ocho" stutter bug), and whether progressives should scale by denomination is an open debate.

¶13 — The through-lines recur month after month: **GLI certification** as the master bottleneck on cost and speed; **money pressure** (the Georgia warning, cost-conscious tool decisions, "no test tool this year"); **regulators everywhere** (GLI, state gaming boards, the Puerto Rico Gaming Commission); and the **engineering-discipline crusade** — Git, "the only source of truth is what's in git," AI tooling, killing tribal knowledge.

¶14 — A softer through-line is your management style: the wiki is full of you coaching, pushing, and overruling, with Aaron as co-teacher. Persona-driven design, feature-branch discipline, and JIRA hygiene appear as things you are trying to instill, not things that exist yet.

¶15 — A commercial through-line is diversification away from dependence on any single market: land-based route markets, online RGS distribution, and the ECHO home device are three distinct bets — you name ECHO a near-term priority and insist online games be built fresh from land-based mechanics, not ported.

¶16 — What changed. The **Elevate relationship was re-understood**: an early (Jan 14) framing of Elevate as a customer financed through EDC was corrected by a Jan 15 call and, on your ruling, recorded as a lender that took a pledge — the EDC role now uncertain. It's the clearest case of the wiki revising an early belief.

¶17 — The **hardware story flipped** too: FP7 was first simply "adopted," then, after bottleneck testing, reframed as a ceiling to optimize against rather than a win. And much early ambiguity was **name/identity resolution** — several people were first recorded under garbled names (now corrected to Biratka, Efim Podvoiski, Genadi Peari, Juan Martinez, Felipe Miranda), and several look-alikes were split into distinct people (two Antons, two Andreis, two Khandovs).

¶18 — **Honest uncertainty.** The largest caveat dwarfs the rest: this is only Jan 2 – Mar 11, 2025 — under 7% of the material — so everything above is the opening chapters, not the book. Anything called "central" here is central *so far*; emphasis will shift as ~900 more transcripts land.

¶19 — Coverage is uneven. The **software/engineering** world is richly documented; **money and corporate structure** are thin — the wiki asserts entities and an ownership split but has almost no real financial picture and barely sketches how the JVL entities divide the business. The **online-games commercial** side (Andrei Klimovich, ECHO, the "Marketplace") is thinner than its apparent importance, resting on a few recap meetings.

¶20 — Some things look important but are underdocumented. A recurring **"Dima"** appears across GitHub-admin, IT-structure, observability, and embedded contexts and has deliberately *not* been merged into one person — the wiki does not know how many Dimas there are. Whether **Michael the game producer is "Misha" the retrofit lead** is open. The **FlexPay mobile app** (distinct from the FlexPay payment hardware) is single-source and flagged. One personal/tax matter was deliberately excluded as out of scope.

¶21 — The five questions the wiki would most want answered: (1) Who are the distinct "Dima"s, and is any of them Dmitry Khandov? (2) What is the real money flow — who funds what, and what are JVL's revenues and obligations? (3) How do the JVL entities (Systems, Labs, Gameworks) actually divide the business? (4) Is Michael = Misha, and who are the half-dozen still-single-source people who keep recurring? (5) Is the FlexPay *mobile app* a live initiative or an early idea that faded? Answering these would move the wiki from "understands JVL's engineering" toward "understands JVL."
