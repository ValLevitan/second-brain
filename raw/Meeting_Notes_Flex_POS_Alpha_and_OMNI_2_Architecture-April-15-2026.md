# Meeting Summary — Pavel/Val/Irina Alignment (Flex POS Alpha + OMNI 2 Architecture + Minsk Dispenser/Recycler)
**Date:** April 15, 2026, 10:02 AM Eastern
**Duration:** ~51 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko
**Language:** Russian (summarized in English per Val's standard)

## Summary

Wide-ranging engineering alignment covering Flex POS Alpha-1 readiness on the new ARC 35-68 SoC, the bottleneck blocking JVL's Flex POS test cycle, Val's strategic push to restart architecture work as **OMNI 2** (with Claude-Code-driven development discipline), HAL microservicing, the Minsk dispenser/recycler logistics problem, and the Flex Pay ICOM-module refactor. Closing item from Irina on Gekam (Georgia) delivery.

### Nire — inventory control still unclear

Pavel: software is practically ready; the last open fix is the touchscreen-calibration trigger landing on the correct screen, to be validated with Elizabeth today. Genadi has raised an inventory-management concern that Pavel and Genadi discussed yesterday: it's unclear whether Elizabeth uses "the plan" (the task-tracking tool — Microsoft Planner, presumably) to mark items as taken into work and finished, AND more fundamentally whether Elizabeth has a complete grasp of inventory control — what components are on hand, in what quantity. Genadi will follow up with Elizabeth directly. Val emphasized this is a two-layer problem: tooling-use is one question; whether she's actually owning inventory control end-to-end is the deeper one. Needs to be clarified.

### Flex POS hardware on ARC 35-68 — Alpha-1 nearly ready

Pavel reported Flex POS device-side is also "near the finish." Lyosha is installing software. Hardware integration confirmed: the IO board (small "P-shaped" auxiliary IO board, T2-style) is in hand; the harness (referenced as "Kharkiv" — i.e., the Kharkiv-sourced harness) is in place; the screens are in place.

The SDK / BSP development infrastructure is now in JVL's git as IP **977** (the development infrastructure IP). Pavel: it's not 100% complete, but it's complete enough to be used now. Open items:
- **Speakers are not yet working.** Pavel deferred — first attempt didn't work, and it's not MVP for Alpha. The device has audio interactivity already (the card reader makes sound when swiped; the QR scanner makes sound), so the kiosk isn't silent.
- **Top light over the swipe reader** has not yet been activated — needs to be brought up.

Once those two items are addressed, "Alpha 1 of Flex POS is ready" in Pavel's words. Val's qualifier: he doesn't want to be standing next to the device for 5 songs, so the speakers do need to be addressed in the short term.

### Production-grade security work — encrypted bootloader

For production rollout of Flex POS, Pavel flagged the next major task: security work using the CPU's built-in mechanisms — specifically encrypted bootloader. He estimates this is a multi-week task, possibly longer. Owner candidates: Pavel himself, or Aaron. Could in principle be assigned to Sasha Beratko, but the Linux bootloader work would be difficult for him. For an early pilot run, the team can ship without it.

### HAL microservicing — split the monolith

Pavel raised the Hardware Abstraction Layer (HAL) as the next-step structural rework. Today HAL is a monolith — when one device fails (e.g., the sound card), the whole HAL stack fails, the application crashes, and the machine reboots in the best case (black screen in the worst). Pavel proposes breaking HAL into independent microservices, one per device class (IO board, printer, bill acceptor, accounter board, etc.), each running independently with its own communication channel. Benefits:
- Independent reboot of any one service if its device crashes
- Independent updates per service
- Independent end-to-end testing per device (e.g., dedicated test for printer ↔ LGS)

Val initially read this as "we need to rewrite in Rust" — Pavel corrected: "Step 1 is just to split the HAL into separate microservices, still in C. Step 2 (later, if needed) is to rewrite individual services in Rust or another language." Val confirmed his understanding: the HAL has two ends — one that talks to the data center (this is the side Pavel wants to split into modules), and one that talks to peripheral devices (this side could be assigned to Lishkevich to write).

### IO board cost — push for new layout for FlexPOS

Val pushed back on using JVL's current standard IO board for Flex POS — he believes it's expensive ("smehnye den'gi" — silly money). He argued JVL should design a new IO board layout specifically for FlexPOS, taking advantage of the modern era of easy IO board layouts. Pavel agreed this is a discussion to have with Genadi.

### Cellular modem + GPS — Val's earlier write-up; HFM-532 filed

Val reminded Pavel of his prior detailed write-up: a mobile-cellular module + GPS with battery-backed monitoring, capable of running unpowered for some time so the unit can be tracked during transport. Pavel filed feature **HFM-532 — Wireless Interfaces Support** today. The full battery-backed-GPS-during-transport scope is not currently included in the dev infrastructure — Pavel said this is probably a separate IP / project. Val emphasized that turnkey on-board solutions already exist on the market: you buy a ready integrated module with all the sensors (cellular, GPS, IMU/orientation, etc.) in one component — start with cellular working, then GPS, then the orientation algorithm.

### Flex POS testing — Anton Seregin must finish this week

Pavel reported the testing/launch of Flex POS depends heavily on backend services. Backend services are deployed and running on AWS. The missing piece is the **UI graphical layer** — Anton Seregin starts on those tasks tomorrow (April 16). Pavel's plan was a ~April 14 deployment milestone, with UI ready next week, full deployment by end of next week.

**Irina objected forcefully:** "We need it now, we cannot test anything, we have a stopper." Val backed Irina up — no weekends in principle, but conceded Anton may need to work Saturday. The team will push Anton to finish this week so that next-week UI work can actually proceed and full end-to-end testing becomes possible.

### OMNI 2 — architecture-first, no more code yet

Val pivoted to the strategic core of the meeting. He has invested enormous time pressuring the organization to figure out how repos should be structured — pushing Beratko in particular (Sasha Beratko) to write a document, which is now evolving to v3. **Sasha Beratko has deeply internalized this; Khoretsky also; Khariadky less so.** The repo-organization question pulls deployment along with it ("razvyortyvaniye produkta na tselevoy arkhitekture" — product deployment to target architecture). Val now understands repo organization clearly; the deployment-infrastructure side is the next thing he wants to learn — strictly the *release stage* (knowing what's in which repo and how to assemble the product up to the point of pushing it out), not the per-target deployment mechanics.

Andrei is currently trying to lay this out simply. Flex POS is the first product Val wants done by this proper method — and that is exactly why a bottleneck has formed there.

The deeper objective: **everything written via Claude Code, everything tested via Claude Code — human hands never touch the code.** Val: "Otherwise it doesn't make sense — if humans have to test it manually, this won't work." That target requires:
- The OMNI architecture to be redone — explicitly: **"RAGE is over. We need to make OMNI 2. That's the codename."**
- Repos restructured
- Testing rethought from scratch
- Stack choice locked: TypeScript + Rust + Java/JavaScript backend ("chao kak bekend" — possibly Tauri or similar). Pavel confirmed.

**Igor Metelsky's return:** Val does not want Metelsky on coding right now (no game/progressive routine work needs it). He wants Metelsky **on testing — specifically end-to-end test architecture**, which is the actual bottleneck. Val proposes folding Lishkevich, Metelsky, and Khoretsky into the architectural definition phase: have them physically build block diagrams, specs, document the data stream flow, module layout, test plan, repo build, deploy pipeline — present those to Pavel; Pavel only corrects ("no, not like that, like this; let's try this; let's test this; how does the watchdog timer fire here?"). Iterate in **very short cycles** — Val invoked the Russian "первый блин комом" idiom (first pancake's a flop, second is better, third is good, fifth is perfection). Long iterations make people drift into the weeds; tight iterations require constant pull.

Val's commitment to himself: don't write any code now. Build the diagrams, specs, texts; have everything in his hands page-by-page; understand the whole picture; then assign work. He asked Pavel to write his own desired-outcome statement ("delal autkam") so they can converge on what they're aiming for — without an outcome target, it becomes "Ivan Susanin wandering through the swamp." Pavel agreed.

### Khoretsky — growing into the role

Val mentioned he is now in close contact with Khoretsky and likes what he sees. Pavel: "Человек вырос. Повзрослел." (He grew up. Matured.) Val agrees.

### Flex Pay / Dispenser / Recycler — Minsk logistics

Pavel pivoted to Flex Pay site, dispenser, and recycler.

**Dispenser:** Physically en route to Minsk. Genadi confirmed yesterday it's coming. Sasha was glad to hear this — without the physical device you can't validate negative scenarios; only positive (happy-path) testing is possible without it. After Sasha finishes the documents (Repa's documents that he's currently on), he will pick up dispenser implementation. Until the device arrives, he'll work blind.

**Recycler:** Will be in Canada within a week, but Pavel doesn't see how it gets to Minsk in even a few weeks — a month, probably. Val agreed they don't have a month for implementation. Remote control (developer-side) on the recycler is "not what we'd want," but no clear alternative. The pain: tight remote-debug loops are very heavy — Sasha can't shove a banknote in or pull it out remotely; he has to coordinate verbally with Sergey on-site to insert/extract notes while he watches the debugger.

**Why not just ship through China, or build sample units in China?** Val explained the economics:
- The China-built samples (recycler + dispenser) on a skid weigh ~100 kg. Air shipment from China at $12/kg US = ~$1,200, plus taxes, ~$2,000 total. Worth it for speed but the time math doesn't close — the Mexican recycler arrives in ~45 days minimum, by which time the dispenser has progressed enough that doing them in series isn't a disaster.
- **Routing existing Japanese dispensers or Mexican recyclers through China is prohibitively expensive** because of the non-recoverable Chinese import duties. You can't reclaim them when re-exporting. Just exporting freshly bought Chinese product is fine, but transit-through is not.
- **MEI (a candidate Chinese supplier) had two recycler units in stock; JVL took both.** They're now sold out and won't sell more.
- **Val personally invented the recycler concept** for this industry — first to talk about it and bring it to market. Then he ran a partner business at Tashko ("Tashko / cash school" — TSC, the company where Val was co-owner) and built one of the first industry recyclers there. Yavorsky and Aleksey know recyclers deeply because they worked on it at Tashko.

### Flex Pay ICOM module refactor — align with Flex Pay Trans

Pavel raised that Flex Pay's existing software (on the Vivan Sousen platform — motherboard side) has the ICOM-module code on the kiosk itself. Flex POS, by contrast, has the ICOM module in the cloud (AWS). Pavel wants Dima or Sergey, when they free up, to **refactor the Flex Pay / Flex Pay Dispenser ICOM module to align with the Flex Pay Trans architecture** — same ICOM-in-cloud design across all products. Big shared codebase, big reuse benefit.

### Test stack — $80K/yr decision waiting

Val raised the test-stack choice with Dima and Sergey. The two candidate stacks have a roughly $100K vs $18K annual cost — an **$80K/year delta**. Dima and Sergey haven't worked with the new (cheaper) stack; migrating them onto it will require ramp-up. Val: this can't be ignored, and it's tied to the same repo-organization and deployment questions that haven't been settled yet — "we haven't even gotten there."

### CMS replacement — must be designed jointly with new POS

Val flagged the larger architectural reframe: **JVL can no longer look at CMS in a vacuum.** It is now "ex-CMS plus new POS." Both must be redesigned together — on paper first, then implemented. Dima and Sergey have just finished POS↔ICOM connection, which enables an **Alpha release**, but starting today the architecture conversation has to begin in parallel — not after Alpha. The cloud-services architecture (POS, CMS-equivalent, OMNI 2) all converge at a single point at the top of the pyramid.

### Constant Diamond Loop — Val's persistent context system

Val described the personal system he has built: a "Constant Diamond Loop" — a Claude-driven persistent knowledge loop ("vot etot vot constant diamond loop") on his computer where he accumulates progress, thinking, decisions. Today's conversation will go into it. Val recommended Pavel set up something equivalent so the two of them can synchronize through their loops rather than starting from scratch in each meeting. Claude organizes it for Val.

### Closing — Irina, Gekam (Georgia)

Irina noted that she has handed Gekam (Georgia) the latest CMS-15 changes that were previously delivered to Texas. (Cut off at end of recording.)

## Decisions Made

- **Flex POS Alpha 1 readiness criteria locked:** SDK on IP 977 is usable; outstanding items are speakers (Pavel deferred — short-term work) and top-light activation. Alpha-1 declared ready once those two are done. (Decided by Pavel; endorsed by Val with the speaker-must-still-happen qualifier.)
- **HAL → microservices, in two steps.** Step 1: split into independent device-level microservices in C. Step 2 (later): rewrite individual services in Rust or other languages as needed. Independent reboot/update/test per service. (Decided by Pavel; endorsed by Val.)
- **OMNI 2 is the codename for the architectural redesign.** "RAGE is over." All future architecture work is OMNI 2. (Decided by Val.)
- **Architecture-first for OMNI 2 / Flex POS / new CMS.** No code is written until block diagrams, specs, deploy pipeline, test architecture, and repo organization are all on paper and agreed. (Decided by Val.)
- **Igor Metelsky goes on testing, not coding.** End-to-end test architecture is the bottleneck. (Decided by Val.)
- **Architectural-design participants:** Pavel, Lishkevich, Metelsky, Khoretsky — they build diagrams; Pavel reviews and corrects in tight iteration loops. (Decided by Val.)
- **Stack for OMNI 2: TypeScript + Rust + Java/JavaScript backend ("chao" backend).** (Decided by Val and Pavel jointly.)
- **No team weekends in principle, but Anton Seregin will likely work Saturday** to unblock UI work this week. (Decided by Val with Pavel's backing; Irina's pressure was the trigger.)
- **Flex Pay ICOM module to be refactored to align with Flex Pay Trans architecture** (ICOM-in-cloud). Dima or Sergey to pick up when they free up. (Decided by Pavel; endorsed by Val.)
- **CMS redesign cannot be considered in isolation** — must be designed jointly with the new POS architecture, on paper, before any implementation. (Decided by Val.)
- **Recycler implementation in Minsk will proceed remotely until the physical unit arrives** (~45 days from Mexico, best case). Acknowledged this is suboptimal but unavoidable. (Decided by Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi | Follow up with Elizabeth on inventory control — both tool usage (Planner) and conceptual ownership of inventory state | TBD | High | Open question on whether Nire inventory is actually controlled |
| 2 | Pavel Frolov + Elizabeth | Validate the touchscreen-calibration fix on a real machine today | Apr 15 (today) | High | Last open fix before Nire is "practically ready" |
| 3 | Pavel Frolov | Bring up Flex POS top light (over swipe reader) | TBD | Normal | Required for Alpha-1 declaration |
| 4 | Pavel Frolov | Resolve speaker support on Flex POS | After Alpha-1 | Normal | Deferred from MVP but Val wants short-term resolution |
| 5 | Pavel Frolov | Drive HAL microservicing — design + implement Step 1 (split into per-device services in C) | TBD | High | Unblocks independent test/reboot/update; tied to Flex POS production readiness |
| 6 | Pavel Frolov OR Aaron | Encrypted bootloader using CPU built-in mechanisms (multi-week task) | Production rollout | High | Required for production; not for pilot |
| 7 | Pavel Frolov | Write a desired-outcome statement ("my ideal outcome") for OMNI 2 architecture work — what done looks like — so the team can converge | TBD | High | Val explicitly asked; gates the architectural-design loop |
| 8 | Pavel Frolov | Set up his own equivalent of Val's "Constant Diamond Loop" so they can synchronize through accumulated context | TBD | Normal | Val's recommendation |
| 9 | Pavel Frolov | Lead the architecture-first design loop for OMNI 2 with Lishkevich, Metelsky, Khoretsky — block diagrams, specs, repo plan, deploy pipeline, test architecture; tight iteration cadence | Ongoing | High | The actual bottleneck for Flex POS production and OMNI 2 |
| 10 | Anton Seregin | Complete Flex POS UI services (graphics layer) — likely Saturday work | End of this week (~Apr 18) | High | Currently the testing stopper per Irina |
| 11 | Sasha (presumably Beratko) | Implement dispenser support — initially blind, then with physical unit when it arrives in Minsk | TBD | High | After he finishes Repa documents; physical unit en route per Genadi |
| 12 | Dima or Sergey | Refactor Flex Pay / Flex Pay Dispenser ICOM module to match Flex Pay Trans architecture (ICOM-in-cloud) | TBD | Normal | Big shared-code reuse opportunity |
| 13 | Dima or Sergey | Migrate to the cheaper test stack (~$18K/yr vs $100K/yr) | TBD | Normal | $80K/yr at stake; ramp-up needed |
| 14 | Val Levitan | Discuss with Genadi a custom IO-board layout for FlexPOS | TBD | Normal | Cost reduction vs JVL's standard expensive board |
| 15 | Val Levitan | Lead the parallel CMS-redesign architecture conversation alongside OMNI 2 | Starting now | High | Cannot ship Alpha and then start; both must converge from now |
| 16 | Pavel Frolov | Track HFM-532 (wireless interfaces support) — and integrate the on-board cellular+GPS+battery-backed module per Val's prior write-up | TBD | Normal | Val's earlier spec is the authoritative reference |
| 17 | Irina Shishko | Closing item — confirm Gekam (Georgia) has the CMS-15 changes that Texas got earlier | (Already done, confirming) | Normal | Operational handoff |

## Engineering Signals

### Confirmed Signals

- **ADR — RAGE is end-of-life; OMNI 2 is the platform forward.** Val: *"Реджжер закончился. Нам нужно сделать OMNI 2. Это кодовое название."* All future architecture work targets OMNI 2.
- **ADR — OMNI 2 stack: TypeScript + Rust + Java/JavaScript backend ("chao" backend).** Val and Pavel converged on this in the meeting.
- **ADR — Architecture-first discipline: no code until repos, deploy pipeline, test architecture, and module diagrams are on paper.** Val: *"Я бы не строчил никакой код. Я бы делал бы систематически луп."*
- **ADR — Claude-Code-driven development and testing as the target operating model.** "Цель заключается в том, чтобы человеческие руки никогда не трогали код." Implies all production code authored and tested via Claude; gates the move to OMNI 2.
- **ADR — HAL split into per-device microservices, Step 1 in C, Step 2 (later) potentially Rust per service.** Pavel: each device class becomes an independently restartable, independently testable, independently updateable service.
- **CAP — Flex POS Alpha-1: SDK in IP 977 + ARC 35-68 platform + IO board (T2-style P-shaped) + harness + screens + card-reader audio + QR-scanner audio.** Outstanding for Alpha: top-light activation. Speakers and encrypted bootloader explicitly deferred from Alpha.
- **CAP — Cellular modem with GPS and battery-backed transport monitoring (HFM-532 filed today).** Onboard turnkey solution preferred per Val.
- **REQ — Flex POS testing requires UI services live by end of week** (per Irina's hard objection to slipping into next week).
- **REQ — Flex POS IO board: cost-driven redesign rather than reuse of standard JVL IO board.** (Val.)
- **Solution — Flex Pay/Dispenser ICOM module refactored to ICOM-in-cloud (AWS), aligning with Flex Pay Trans architecture for code reuse.** (Pavel.)
- **Solution — Recycler implementation in Minsk proceeds without physical unit until ~45 days from Mexico arrival.** Acknowledged-suboptimal compromise.

### Suspected Signals

- **Possible REQ — Inventory control system for Nire requires a single owner who actually understands the conceptual scope, not just tool usage.** Genadi/Val flagged this — does this need to become a formal process requirement? *(Val — REQ candidate?)*
- **Possible CAP — Microservice-level end-to-end tests per peripheral device (printer ↔ LGS, IO board ↔ LGS, etc.)** as a derived capability of HAL microservicing. Pavel implied but didn't formalize. *(Val — CAP candidate?)*
- **Possible ADR — Backend stack identifier "chao":** the spelling/pronunciation in Pavel's Russian was unclear; could be "Tauri", "Chao", or another option. Should be locked unambiguously in the OMNI 2 stack ADR. *(Confirm with Pavel.)*

## Open Questions

- Does Elizabeth genuinely own inventory control for Nire end-to-end, or only narrow tool usage? Genadi to investigate; result feeds back to Val.
- What is the actual on-the-ground cost of JVL's standard IO board vs a Flex-POS-specific custom layout? Genadi/Val to scope.
- Encrypted-bootloader owner: Pavel, Aaron, or Sasha Beratko (with the latter being harder)? Open assignment.
- Recycler in Minsk: any way to get a unit there sooner than ~45 days? Pavel speculated whether China has an off-the-shelf recycler — Val confirmed no (MEI was sold out, won't reorder). No alternative identified.
- "Chao" backend — what exactly is the framework name? (See Suspected Signals.)
- How tight should the architecture-design iteration cadence be? Val said "very small" but didn't specify weekly/twice-weekly/etc.
- What does Anton Seregin's Saturday-work expectation translate into in practice? Irina pushed for completion this week; Pavel said "we'll ask Anton to work Saturday if needed."

---
*Processed from Teams transcript on 2026-04-25*
*Source meeting: Alignment_session-April-15-2026 (Teams recording)*
*Stale-meeting processing — no email drafts, no calendar reminders, no follow-up actions dispatched per Val's standing feedback (Apr 15 → Apr 25 = 10 days).*
