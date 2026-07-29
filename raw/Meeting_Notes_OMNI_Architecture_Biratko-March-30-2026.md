# Meeting Summary — OMNI Architecture with Biratko
**Date:** March 30, 2026, 2:16 PM Eastern
**Duration:** ~37 minutes
**Attendees:** Val Levitan, Alexander Biratko

## Summary

**Language consolidation for OMNI 2.** Val opened the meeting with a direct statement of intent: OMNI 1 is to be retired and replaced by OMNI 2. The current OMNI codebase spans approximately five programming languages, with C and C++ being particularly difficult to manage. Val wants to consolidate down to two or three languages. His target stack is **Rust and TypeScript**, eliminating C/C++ entirely.

Val has already secured commitments from two team members. **Efim** (who owns the math modules, currently written in C++) agreed to become a Rust expert within three months and begin migrating all math code to Rust. **Anton** reviewed the HAL (hardware abstraction layer) codebase and agreed to rewrite it in Rust, estimating the rewrite itself would be quick.

Alexander noted that AI-assisted coding works particularly well with Rust due to its strict, unambiguous syntax — the language's specificity gives AI good context for generating correct code.

The discussion then turned to **Java**. LGS (the game server) is written in Java. Val asked whether it could be rewritten in TypeScript. Alexander said no — TypeScript cannot manage native device interactions, which LGS requires. Val then asked about replacing Java with Rust instead. Alexander said it's technically possible but would be a large project, and Java is significantly easier to maintain and debug from a human perspective. Alexander also noted Java has excellent AI tooling support — on par with or better than TypeScript due to its strict typing. Val accepted this reasoning, and they settled on a **three-language target: Rust, TypeScript, and Java**.

Val emphasized this is **confidential** — he explicitly asked Alexander not to discuss OMNI 2 plans with the wider team, as it would "cause a whole panic."

**Containerization strategy.** The conversation moved to containerization. Alexander explained the math module already runs in a container — it originated from a Julia container that they realized could run directly on the target system. Val found this approach compelling and asked about extending containerization to games.

Alexander explained that games are written in TypeScript and run inside a browser, so they're already platform-independent. However, containerizing games would provide **QA value**: testers could download a Docker image and test a production-like build without assembling a full machine. Val saw this as a significant win — enabling parallel testing while development continues on other components.

The work to containerize games would be "small," per Alexander. He proposed two approaches: either creating a separate game server (decoupled from LGS) that runs inside a Docker container, or auto-mounting the Docker container as a filesystem directory that LGS reads directly. Alexander offered to **discuss the auto-mount approach with Pasha** to see if it's feasible.

**Peripheral abstraction and automated testing.** This was the most technically involved discussion. Val proposed creating a **standard communication protocol** for all peripherals, with each device connecting through a protocol layer rather than native libraries. The goal: enable automated testing without physical hardware. Val described the current QA pain in stark terms — shipping devices to Belarus requires routing through China, costs $600 in taxes per shipment, and takes 1–1.5 months. The cycle is "absolutely not sober" (impractical).

Alexander raised the **iBoard as the critical concern**. The iBoard uses a high-speed USB-connected memory chip (specifically chosen by Dima Pikuley for its speed) that stores game state. When a player presses "Spin," the bet state must be persisted to storage instantly. Any protocol layer between LGS and the iBoard could introduce latency that prevents state from being saved before a power loss. Alexander estimated the overhead at roughly 10ms for network requests, which he acknowledged might be acceptable — but wasn't certain.

For all other peripherals — printers, validators, bill dispensers, buttons — Alexander confirmed speed is irrelevant. These are inherently slow devices where additional latency has no impact.

Val asked Alexander to think about this not just from a technical perspective, but from a **business and QA efficiency perspective**. He specifically framed the cost: the bureaucracy of physical testing "shamelessly strips profit that could go into your pocket." He left this as an open undertaking for Alexander to consider.

Alexander noted a related challenge: the cash dispenser he's currently implementing has documentation that's "half in Japanese, half in English" with a complex protocol, and he can't fully validate the implementation without physical hardware. Val acknowledged that new peripheral adaptation would take longer under an abstraction model (possibly 4 months instead of 1) but argued the long-term testing benefits justify it.

**Confluence documentation update.** Val raised a separate issue: the Confluence documentation for OMNI architecture is outdated. Pages reflect the "progression of thinking" over time but don't represent the current state of the system. Val wants a **snapshot of how things work today** — accurate, concise, in Russian, using proper terminology.

Val will send Alexander an **MD file** of the current architecture document. Alexander should review it, correct the diagrams and descriptions (using AI tools is encouraged), and produce an updated version that accurately describes the system as it exists now. Alexander can use voice dictation with AI to describe the system and generate a corrected document. When satisfied, Alexander sends it back to Val, who will update Confluence. **Deadline: April 4, 2026.**

Alexander noted that existing diagrams drawn by a previous author "don't really reflect" the actual architecture. Val agreed they need correcting — the document must be accurate before any OMNI 2 changes begin.

## Decisions Made

- **OMNI 2 will target three languages: Rust, TypeScript, and Java** — eliminating C, C++, and any other legacy languages. C/C++ code splits into two migration projects: math (Efim) and HAL (Anton). Both have agreed. (Decided by Val)
- **Java stays for LGS** — TypeScript can't handle native device interaction, and rewriting LGS in Rust would be too large a project with diminishing returns given Java's maintainability. (Decided by Val and Alexander)
- **Games will be containerized** — primarily for QA testing benefit. The work is small. (Decided by Val and Alexander)
- **OMNI 2 plans are confidential** — not to be discussed with the wider team yet. (Directed by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Think through the peripheral abstraction/containerization approach from a QA efficiency and business perspective — evaluate whether a standard protocol layer between LGS and peripherals is viable, considering iBoard latency concerns and testing benefits | April 4, 2026 | High | Val wants to eliminate the expensive physical-device QA cycle (shipping through China, $600/shipment, 1-1.5 month delays). This is a strategic architecture decision for OMNI 2 |
| 2 | Alexander Biratko | Review and correct the OMNI architecture MD document that Val will send. Use AI tools to describe how the system works today — accurate, concise, in Russian with proper terminology. Correct diagrams. Send corrected version back to Val | April 4, 2026 | High | Must be completed before any OMNI 2 changes begin. Current Confluence docs are outdated and inaccurate |
| 3 | Alexander Biratko | Discuss with Pasha whether Docker game containers can be auto-mounted as filesystem directories for LGS to read directly | April 4, 2026 | Normal | Simplest path to game containerization — avoids writing a separate game server |

## Engineering Signals

### Confirmed Signals

- **ADR: OMNI 2 target language stack — Rust, TypeScript, Java.** Val stated the decision explicitly. C and C++ are being eliminated. Efim takes math module migration to Rust (3-month ramp-up), Anton takes HAL rewrite to Rust. Java remains for LGS because TypeScript can't handle native device interaction and rewriting in Rust would be too large.

- **ADR: Game containerization for QA testing.** Val and Alexander agreed to containerize games (TypeScript) in Docker images so QA can test production-like builds independently. Alexander confirmed the work is small.

- **ADR: Peripheral abstraction layer with standard protocol.** Val proposed replacing direct native library calls to peripherals with a standard protocol layer, enabling emulated/containerized testing. Alexander raised the iBoard latency concern (~10ms overhead) but acknowledged most peripherals would be unaffected. Val directed Alexander to evaluate feasibility from a business and QA efficiency perspective. The architectural direction is set; implementation details pending Alexander's assessment.

- **ADR: Automated regression testing without physical hardware.** Val described the prohibitive cost of physical QA cycles (shipping through China, $600/shipment, 1–1.5 month delays) and framed automated testing as a core OMNI 2 goal. The peripheral abstraction layer and game containerization both serve this objective. The intent is to enable full regression testing using emulators and containerized components without physical devices.

## Open Questions

- **iBoard latency tolerance:** Can the iBoard protocol afford ~10ms of network overhead for state persistence? Alexander suggested experimenting. No resolution yet.
- **Docker auto-mount for games:** Pasha needs to evaluate whether Docker containers can be mounted as filesystem directories for LGS. Alexander will follow up.
- **Peripheral protocol design:** What would the standard protocol look like? What happens for new device types (e.g., cash dispenser) that require extending the protocol?

---
*Processed from Teams transcript on March 30, 2026*
*Source meeting: OMNI Architecture with Biratko*