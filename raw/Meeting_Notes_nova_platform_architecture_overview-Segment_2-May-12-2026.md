# Meeting Summary — NOVA Platform Architecture Overview (Segment 2: To-Be Design, Naming, Chief Architect)
**Date:** May 12, 2026, 12:56 PM Eastern
**Duration:** 1h 56m 16s
**Segment:** 2 of 2
**Attendees:** Val Levitan, Alexander (Sasha) Biratko, Irina Shishko, Anton Leshkevich

> **Initiative cross-reference:** This is the foundational meeting for the **NOVA Gaming Platform**. The platform is named during this session. **Alexander Vladimirovich Biratko is appointed Chief Architect.** Canonical initiative record: `obsidian-jvl/Initiatives/NOVA Platform Architecture/`. Major ADRs from this meeting are expected to land as files inside each of the 12 NOVA repositories per Val's directive.

## Transcript Quality Note

Conducted in Russian; summary in English. The session was paired with active whiteboard editing — the structural conclusions are clear in the verbal record, but specific box positions, arrow directions, and the final diagram are only fully captured in the live whiteboard / Miro link Sasha dropped into chat (referenced as "GP architecture" page in the diagram, since renamed to NOVA root).

## Summary

This long working session (~2 hours) followed immediately after the as-is walkthrough of Segment 1. It accomplishes three foundational things for the platform initiative:

1. **Names the platform: NOVA.** After a long detour through candidate names ("Gaming Platform" / "GP" / "JVL Gaming Platform" / "JGP" / "ABV" / "BAV" etc.), Val and the team land on **NOVA** as the codename. The diagram root element is renamed accordingly.
2. **Appoints Sasha (Alexander Vladimirovich Biratko) as Chief Architect of NOVA.** Formally declared on the recording: *"Alexander Vladimirovich Biratko is appointed Chief Architect of this project."* Sasha accepted with a deadpan: *"of the one that doesn't yet have a name."*
3. **Drives a long set of to-be architecture decisions** — services decomposition, repository layout, language stack, communication protocols, hardware boundary, game lifecycle, and the requirements/capability/feature governance model that will sit on top.

### 1. Naming the platform — NOVA

The session opened with Anton pushing "JVL Gaming Platform" as his favourite from a candidate list. Discussion ranged over:
- **"Gaming Platform"** — Sasha preferred this in English; in Russian "игровая платформа" felt more like a games console (Xbox-style).
- **"JGP" / "JVL Gaming Platform"** — Val: "I really like *gaming platform*. I'd shorten it to JGP." Used as a working handle for ~40 minutes mid-session.
- **"ABV" / "BAV"** — Irina's joking suggestion based on Sasha's initials (Alexander Vladimirovich Biratko). Briefly held as candidates.
- **"NOVA"** — Val proposed late in the session. *"Provisional codeword: NOVA."* Sasha renamed the diagram root element to "NOVA"; the dependent diagram page was renamed "NOVA architecture." Everyone accepted.

### 2. Chief Architect appointment

Val formally declared the appointment on the record. Sasha's full name was confirmed for the transcript: **Александр Владимирович Биратко / Alexander Vladimirovich Biratko**. The role explicitly carries authority to make architectural decisions ("I as architect will decide that we'll have separate repositories for each, I can do that"). Sasha used this authority several times during the session to settle internal debates (e.g., per-service repo split vs monorepo — see below).

### 3. The to-be design — what NOVA actually is

**3a. Browser-engine question — stay on Pixie/Phaser or move to Unity/Unreal.**

Anton raised: now that the online side has been deprioritised, do we stay on the browser stack (Pixie / Phaser HTML5 engines)? His concern: these engines won't deliver the graphics quality of Unity or Unreal long-term.

Sasha agreed in principle: Unity / Unreal / Godot would be more native and performant, and would also let dev cycle stay end-to-end inside Unity (Miranda already lives there). But the engine choice was historically driven by **free licensing**, which remains a hard constraint. Godot doesn't yet handle video well; Unity / Unreal are paid; "no free engine currently supports all our needs."

**Val's call: stay on the current engine for now.** Migration to Unity would be "a huge restructuring" — not feasible at this moment. Sasha: *"OK, then we stay on this engine."* Worth tracking as a deferred-but-not-killed possibility.

**3b. Library modules → standalone services.**

The headline to-be architectural change: each in-process Java-native library (SoundLib, PrinterLib, BillLib, BoardLib, IRILib, LetLib, etc.) becomes a **standalone service** — its own executable application with its own interface, runnable independently, restartable independently, and unable to crash LGS when it errors.

**Service definition (Sasha):** *"A service is a separately-executable application with an interface, performing a defined function. It has its own repository, runs in the OS as an independent application, can be restarted without affecting anything else. It is either on-and-available or off-and-unavailable to others — but its failure does not affect other applications."*

**Communication mechanism between services and LGS:** **Unix sockets.** Anton supported this. Sasha justified: the bottleneck is BillBoard — fast persistence is required so that on a button press, the system can quickly save state, reboot, and know the button was pressed. Reaction time must be under ~10 ms. Unix sockets give *more than enough* throughput at that latency.

**Service substitutability — virtual / fake-mode operation.** Each service can be substituted with a "demo / virtual" implementation that exposes the same interface to LGS but runs without the underlying hardware. Sasha gave the printer example: a virtual printer that LGS treats as real, but with additional control APIs (e.g., "throw an error" → LGS sees the error). Useful for testing the platform end-to-end without all the physical hardware. Coverage estimate: **99% of real hardware behaviour can be emulated**; the last 1% is fine mechanical details that aren't worth fully simulating.

**3c. Data contracts and the API layer.**

Each service has its own **data contract** with LGS. Each service has its own API. The data contract defines what LGS and the service exchange over the unix socket interface.

**3d. Hardware boundary.**

A core conversation: what's *inside* the NOVA platform vs. what's *outside*. After back-and-forth, the team settled:

- **Hardware components (monitors, touchscreens, speakers, amplifier, button panel, counter board, candle light, LED controller, printer hardware itself, bill validator hardware itself, etc.) live OUTSIDE the NOVA boundary** — they are the EGM's physical layer, not the software platform. Drawn in a different colour (blue) on the diagram.
- **Firmware (board firmware, BillBoard firmware) lives OUTSIDE NOVA** — it's flashed onto hardware boards and doesn't run on the Linux OS. Even where JVL writes the firmware (e.g., BillBoard, board driver), the *firmware itself* is hardware-layer, not platform-layer. Sasha conceded after Val's pressing: *"OK, I agree — it doesn't run on the machine's own hardware processor with Linux; it runs on the dedicated board."*
- **Linux OS, kernel, HAL scripts, services, LGS, Setup UI, Arrange, MathEngine, Progressive Controller, Miranda, TS-360, CMS link, Flex-Pay, Flexport — INSIDE NOVA.**

**HAL placement and ownership.** Even though Linux itself is excluded from JVL's responsibility, the HAL scripts written *by* JVL (startup scripts, monitoring scripts, launching scripts for LGS / SoundService / PrinterService / BBService / etc.) **stay inside NOVA**. HAL acts as the entry point for the platform — the script kicks off LGS and the services in sequence.

**3e. Connectivity additions.**

- **Modem + GPS (combined device, sold as one)** added to the diagram as an external device with its own Linux driver. Purpose: remote OTA game loading / replacement.
- **Wi-Fi module** added separately. Critical use case: when multiple machines are on a location, only one machine carries the active GSM modem (cost: only pay for one). The other machines connect via Wi-Fi to that lead machine. *"Like the MBD progressive controller story — one machine becomes 'master' for connectivity, others discover and connect."* The leader-election mechanism needs designing — explicitly flagged as a future work item.

**3f. Games as data, not applications.**

Anton asked: how do games live on the machine? Sasha:
- **Games today are directories** of files on disk.
- **Games in NOVA will be packaged archives** — a set of files wrapped in one archive for network delivery. Paving Pasha's existing system, which already packages games into **chunks** with checksums per chunk.
- **Each game gets a reserved "slot" on the machine** (slot 1, slot 2, ...). A configuration limits the total number of game slots (Sasha used "12 slots" as an illustrative number).
- **Game updating is a CMS-triggered LGS operation.** CMS tells LGS *"replace the game in slot N with the new game at this URL."* LGS downloads via the GSM modem into the free slot or replaces the existing slot, deleting the prior game.
- **Games are not active applications under Linux.** A game is a script running inside the browser. If a game throws an error, only the browser surfaces the error and restarts; the OS is unaffected. So Docker-containerising each game is unnecessary — Sasha's architectural call: *"as architect, I say a Docker wrapper for the games is excessive."*
- **Game sandbox check sums** maintain certification (each game has its own checksum / signature). Irina raised the Florida-style "whole image" certification case — Sasha acknowledged that for jurisdictions with a single image-level checksum, game replacement requires recertification. A potential **Updater** service was floated as an alternative for that case — a separate app that handles updates and talks to a different service than CMS. Not yet decided.

**3g. Repository structure.**

After enumeration, **NOVA = 12 repositories total**:
- 11 base repositories (each yellow box on the diagram is one repo).
- 1 game repository (the games container).
- Plus: each game also gets its own repo.

Specific repo questions raised:
- **Arrange + MathEngine: one repo or two?** Sasha to confirm with Efim. Arrange is "very small," may not warrant its own repo. If so, NOVA becomes 11 repos; if Efim wants the split, it's 12. (Sasha will return a decision.)
- **Hard services (sound, printer, BB, board): per-service repos or one consolidated repo?** Anton suggested consolidating if there's "a lot of common code," similar to how MathEngine and Arrange share. Sasha pushed back on releaseability and versioning grounds and **used his architect authority to decide: separate repos per service.** Anton accepted.

**3h. Languages on the diagram.**

Each box now has a language tag added during the session:
- **Java** — LGS, In-Setup UI, Setup UI, TS-360, Progressive Controller (and SignageProgressiveController).
- **TypeScript / JavaScript** — game framework and games (Sasha treats TS and JS as the same technology — TS compiles to JS; "if you know one, you know the other"; a few specific services within the framework use raw JS rather than TS for browser-native performance reasons).
- **C++** — MathEngine (current — to be rewritten in Rust).
- **Rust** — new direction. Services to be rewritten in Rust (sound service, printer service, BillBoard service, board service, IRILib service, etc.). Also: **firmware written by JVL** (BillBoard firmware, driver firmware) **to be migrated to Rust** where the controller hardware supports it. Anton flagged some old STM32-class controllers may not support Rust well; Sasha: that's fine, those stay where they are.
- **C# / Unity scripting** — Miranda. (Also a small amount of JavaScript inside Miranda.)
- **Shell script / bash** — HAL scripts.

**Total languages on NOVA: 3 primary (Java, TS/JS, Rust) + utility (shell + C# for Miranda).**

**3i. ADR governance model — every NOVA repository owns its ADRs.**

Val locked the discipline: **all architectural decisions ("ADR — architectural decision records") for NOVA are owned by the Chief Architect (Sasha).** Sasha asked: *"the result of my ADRs should be files inside each repository?"* Val confirmed: yes, ADRs live as files inside the repository they describe. They will overlap and cross-reference each other ("they intersect with the data contract"); but each repo holds its own.

**3j. Math secrecy is relaxed.**

Sasha noted he doesn't currently have access to the MathEngine / Arrange repositories (historically held closely by Efim). Val: *"we are moving away from the secrecy. The math is very complex and we are opening it up."* Sasha will get repo access. He will write the math-related ADR file in the **new Rust-based MathEngine repository** (which will be a *new* repo, not the existing C++ one; the C++ repo is left alone).

**3k. Requirements / capabilities / features hierarchy for NOVA.**

A long stretch toward the end of the session worked through how requirements + capabilities + features map onto this platform — because NOVA has no traditional "operator" or "player" persona in the same way game features do. Val's resolution:

- **For NOVA, the users are the *internal* JVL teams who consume the platform.** Specifically:
  - **Anton** (test framework / TS-360) is a *user* of NOVA. He needs hooks, APIs, test harnesses from games, LGS APIs, hardware-service APIs.
  - **Irina** writes test cases for the QA team. Those test cases convert to use cases, which convert to requirements, which convert to capabilities.
  - **Kamin (Alexey Kamin)** is Anton's downstream user — Kamin is the customer Anton is delivering for.
- **The chain:** Use case ← Requirement ← Capability. Use case = *why* something must be done (and for whom). Requirement = *how* it functions. Capability = *what* must be done (at the platform level).
- **For NOVA specifically:** Anton looks at his requirements, splits them into features that need to be implemented in the test rig. When he needs a hook or API that doesn't exist yet, he tells Sasha *"I need capability X-Y-Z."* Sasha (as architect) translates that capability into the features he must deliver. Each feature is a feature branch — when complete, merge into main.
- **Without that demand chain, Sasha has no client.** Val: *"Sasha doesn't write features unless someone asks for them. Anton is Sasha's customer; Kamin is Anton's customer."*

**3l. The first practical Rust port — pick a service, start there.**

Sasha closed the architectural section: *"we need to start with one of the services we're going to rewrite in Rust."* Val agreed but deferred the *which* and *when* until **Pavel is back in the office** and consulted. The Sound Service, Printer Service, or BillValidator Service are all candidates.

**3m. CMS communication freeze — month-long timeout.**

Val explicitly excluded one meeting from happening soon: a working session with the CMS team to align communication-protocol architecture. Reason: *"CMS is buried right now. They need about a month to come up for air."* Defined here: **the protocol will be AMQP-style messaging.** Architecture lead on the CMS side will be **Dima Chudinov**. *"When the two architects (Sasha and Dima) sit down to talk, it'll be fantastic."*

**3n. Closing direction from Val.**

> "Consult with Pavel, think about the name, decide if it works for you or propose another. If it works, no meeting needed. Then we start building. We need to build a set of development features. Use cases convert to requirements, requirements convert to capabilities. Anton starts producing his features; when he sees what features he needs, he understands what requirements he needs from Sasha. Then Sasha can ask Anton for his requirements, and Sasha will know what to do. Until then, don't start writing anything on the keyboards yet."

Meeting ended at the 1h 56m mark.

## Decisions Made

- **Platform name: NOVA.** Codename, may evolve. (Val, accepted by all.)
- **Chief Architect of NOVA: Alexander Vladimirovich Biratko.** Formal appointment on the record. (Val.)
- **Stay on current browser engine (Pixie / Phaser stack) for now.** Migration to Unity / Unreal / Godot deferred — performance and graphics-quality benefits acknowledged, but free-engine constraint remains. (Val, Sasha.)
- **Library modules become standalone services** with their own repositories and Unix-socket communication to LGS. Each service is independently startable/restartable; service errors do not crash LGS. (Sasha, with Val.)
- **Service-to-LGS communication = Unix sockets.** Performance margin verified for the 10 ms BillBoard reaction-time requirement. (Sasha, supported by Anton.)
- **Each service has its own data contract.** (Sasha.)
- **Service substitutability via demo/virtual implementations** — each hardware-backed service has a corresponding virtual mode that LGS treats as real, ~99% coverage. (Sasha.)
- **Hardware boundary: monitors, touchscreens, speakers, amplifier, button panel, IO board, counter board, candle light, LED controller, printer/billvalidator hardware, board hardware — all OUTSIDE NOVA.** Firmware also outside. HAL scripts INSIDE. (Sasha + Val.)
- **Modem + GPS combined as one external device with Linux driver.** Inside the connectivity layer. (Sasha.)
- **Wi-Fi module added separately** to enable lead-machine connectivity sharing at multi-machine locations. Leader-election design needed. (Val + Sasha.)
- **Games are packaged archives, not Docker containers, not active Linux apps.** Slot-based on disk (e.g., 12 slots). Updated remotely via CMS → LGS → modem download. (Sasha.)
- **For Florida-style whole-image-certified jurisdictions, game replacement triggers recertification.** Potential dedicated Updater service if needed. Not yet decided. (Sasha + Irina.)
- **NOVA = 12 base repositories** (or 11, pending Efim's call on Arrange-vs-MathEngine repo split) + per-game repositories.
- **Hard-services architecture: one repository per service** (sound, printer, BB, board, etc.). Per Sasha as Chief Architect — Anton's monorepo suggestion rejected on versioning/releaseability grounds.
- **Languages: Java + TypeScript/JavaScript + Rust + utility shell + C# (Miranda).** Rust is the new direction for services + firmware migration.
- **MathEngine: existing C++ repo unchanged; new Rust-based repo created as the future state.** (Sasha.)
- **ADRs live as files inside the repository they describe.** Owned by the Chief Architect. (Val + Sasha.)
- **Math (MathEngine / Arrange) secrecy relaxed.** Sasha will get repo access. (Val.)
- **CMS communication-protocol architecture: AMQP-style messaging.** Sasha + Dima Chudinov to architect together — but the meeting cannot happen for ~1 month while CMS team is overloaded. (Val.)
- **Use case → Requirement → Capability hierarchy applies to NOVA, with internal teams (Anton, Irina, Kamin) as the users.** Sasha's clients are internal team members who declare capability needs against the platform. (Val.)
- **No code yet — finish requirements/capabilities/features model first.** (Val's closing directive.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Consult Pavel on the NOVA name and the overall to-be architecture; confirm or counter-propose | When Pavel is back in office | High | Val: "if it works for you, no meeting needed" |
| 2 | Alexander Biratko | Confirm with Efim whether Arrange and MathEngine are one repo or two | Soon | Normal | Determines whether NOVA has 11 or 12 base repos |
| 3 | Alexander Biratko | Write ADR files inside each NOVA repository capturing the architectural decisions made in this session | Ongoing | High | Per Val's directive — ADRs live in-repo |
| 4 | Alexander Biratko | Create the new Rust-based MathEngine repository (separate from the existing C++ repo) | When ready to start Rust port | High | New repo lets the old C++ repo stay untouched |
| 5 | Alexander Biratko | Get repo access to MathEngine / Arrange now that math secrecy is relaxed | Soon | Normal | Required to write the math-side ADR |
| 6 | Alexander Biratko | Decide on the first service to port to Rust (Sound, Printer, BillValidator are candidates) — after consulting Pavel | After Pavel consultation | High | First practical Rust deliverable |
| 7 | Alexander Biratko | Design the leader-election mechanism for multi-machine Wi-Fi connectivity sharing (analogous to MBD progressive controller leader logic) | TBD | Normal | Avoids paying for multiple GSM modems on the same location |
| 8 | Anton Leshkevich | Begin producing his test-framework features based on the use cases that already exist (test cases convert to use cases, then to requirements, then to capabilities) | Once Sasha consults Pavel | High | Anton is the first internal "user" of NOVA |
| 9 | Anton Leshkevich | When his work hits a missing hook/API/capability, declare it explicitly to Sasha (numbered capability list) | Ongoing | High | Sasha needs the demand signal to know what features to write |
| 10 | Irina Shishko | Convert existing test cases to use cases; convert use cases to requirements; map requirements to capabilities | Ongoing | High | Foundational input for Anton and Sasha both |
| 11 | Val Levitan | Schedule the eventual NOVA ↔ CMS architecture meeting between Sasha (Chief Architect, NOVA) and Dima Chudinov (architect, CMS) | ~1 month out | High | CMS team currently overloaded; protocol will be AMQP-style |
| 12 | Team | No code written until the requirements / capabilities / features model is in place | Through the start of the next phase | High | Val's hard rule |

## Engineering Signals

### Confirmed Signals

- **ADR — Platform name: NOVA.** Replaces the working "Omni" codename.
- **ADR — Chief Architect of NOVA: Alexander Vladimirovich Biratko.**
- **ADR — Library-to-service decomposition.** All SoundLib/PrinterLib/BillLib/BoardLib/IRILib/LetLib become standalone services with independent lifecycles. Eliminates the in-process Java-native fragility where any library crash takes down LGS.
- **ADR — Service-to-LGS communication via Unix sockets.** Performance-validated for the ~10 ms BillBoard reaction-time requirement.
- **ADR — Per-service data contracts.** Each service exposes its own API and data contract to LGS.
- **CAP — Virtual/demo mode for every hardware-backed service.** ~99% emulation coverage. Enables end-to-end platform testing without all physical hardware.
- **ADR — Hardware boundary: NOVA is software running on the EGM's main processor under Linux.** Monitors, touchscreens, speakers, amplifier, IO board, counter board, candle light, LED controller, printer, bill validator, all firmware → outside NOVA. HAL scripts written by JVL → inside NOVA.
- **CAP — Modem + GPS combined external device** with Linux driver, for OTA game delivery + location services.
- **CAP — Wi-Fi module + leader-election** for multi-machine location-level connectivity sharing. One active modem per location; others connect via Wi-Fi.
- **ADR — Games are packaged archives with checksums, NOT Docker containers, NOT active Linux processes.** Each game has a reserved slot on disk; updates via CMS-instructed LGS download + replace.
- **CAP — Game-replacement update flow:** CMS → LGS → modem download → swap slot. Browser-level error containment (game error doesn't crash the platform).
- **ADR — One repository per hard service.** Decided by Chief Architect (Sasha) over Anton's monorepo suggestion. Versioning + release-ability rationale.
- **CAP — NOVA repository count: 11 base + 1 games container + per-game repos.** (Or 12 base if Arrange/MathEngine split confirmed.)
- **ADR — Language stack: Java (LGS, Setup UI, In-Setup UI, TS-360, Progressive Controllers) + TypeScript/JavaScript (game framework + games) + Rust (services + JVL-written firmware where controller supports it) + C# (Miranda) + shell scripts (HAL).** C++ MathEngine to be ported to Rust in a new repo.
- **ADR — Stay on Pixie/Phaser browser engine for now.** Unity / Unreal / Godot migration deferred but explicitly not killed. Driver: free-engine constraint + Godot's video gap.
- **ADR — Math secrecy relaxed.** Sasha (Chief Architect) gets access to MathEngine / Arrange repos.
- **ADR — CMS communication protocol = AMQP-style messaging.** Sasha + Dima Chudinov to co-architect when CMS team is available (~1 month).
- **ADR — ADR governance pattern.** ADR records live as files inside the repository they describe. Owned by the Chief Architect. Cross-references between ADRs across repos are expected (they intersect with the data contracts).
- **CAP — Use case → Requirement → Capability hierarchy for NOVA.** Internal JVL teams as the "users." Anton consumes capabilities; Irina drafts use cases; Sasha delivers features against declared capability needs. Without an upstream declaration, the architect doesn't write features.

### Suspected Signals

- **Possible ADR — Updater service for image-certified jurisdictions (Florida-style).** Floated by Sasha as an alternative path for game updates when the whole-image checksum model is in play. Not decided. — *Worth tracking as a phase-2 capability once a Florida-style deployment becomes concrete.*
- **Possible CAP — Phased Rust migration sequencing.** First service to port has not been picked. Order matters for risk and learning. — *Should there be a documented sequencing principle (e.g., "start with the least-dependent service") or is the choice purely opportunistic?*
- **Possible REQ — Wi-Fi leader-election protocol.** Sasha noted "similar mechanism to MBD progressive controllers." Worth designing-out before any multi-machine NOVA deployment. — *Defer until first multi-machine NOVA scenario is concrete?*
- **Possible REQ — Florida / image-certified jurisdiction game-replacement constraint.** Game updates trigger full image recert. The architectural implication may be: maintain a separate "image-cert" build pipeline alongside the slot-based update pipeline.
- **Possible ADR — Firmware migration to Rust where controller supports it.** Anton/Sasha confirmed compatible boards. Older STM32-class boards stay where they are. — *Worth tracking which controllers are Rust-eligible.*

## Open Questions

- **Final name — is NOVA actually staying?** Val explicitly framed it as a "codeword." Sasha to consult Pavel and confirm or propose alternatives.
- **Arrange + MathEngine: one repo or two?** Sasha to confirm with Efim.
- **Which service ports to Rust first?** Sound / Printer / BillValidator are all candidates. Pavel consultation gates this.
- **Updater service for Florida — exists or doesn't?** Architectural placeholder, no decision.
- **CMS protocol architecture details beyond "AMQP-style"?** Sasha + Dima to design in ~1 month.
- **Wi-Fi leader-election protocol** — not designed yet.
- **Signage progressive controller status in NOVA** — carried over from Segment 1 unresolved.
- **Flex-Recycler / Flex-Dispenser / Flex-POS integration into NOVA** — known-pending but not architected yet.

---
*Processed from Teams transcript on May 22, 2026*
*Source meeting: Overview_services_land-based_platform-May-12-2026 (20260512_085611) — Segment 2 of 2*
