# Meeting Summary — LTE_V-1000_GA-COAM
**Date:** August 10, 2026, 9:34–9:57 AM Eastern
**Duration:** ~23 minutes
**Attendees:** Val Levitan, Pavel Frolov
**Raw transcript:** [[Meeting_Transcript_LTE_Modem_V-1000_Georgia_COAM-August-10-2026]]
*(Meeting held in Russian; summary in English.)*

## Summary

Val asked Pavel what is needed to get the LTE cellular modem working on the V-1000 machines for Georgia COAM (and Nebraska).

**Software side — mostly done.** Pavel said development is essentially complete. What remains is to assemble the build for Georgia and Nebraska and QA-test it. On the Linux/system side they added new kernel modules, scripts to run modem commands, and utilities for two modem types. The datacenter GUI now has controls to enable/disable the modem, a manual mode to enter modem and network parameters, and connect/disconnect with a status view; a later stage adds downloading over the modem. The main setup screen and diagnostics screen show signal strength, connect/not-connected, and a ping test (e.g., to Google). The datacenter will probably need to be rebuilt for Georgia.

**Fold it into GA-COAM V3.** Pavel suggested carrying the modem support inside the GA-COAM V3 build that has to go to the lab anyway — the modem becomes a "free addition" in that submission rather than a separate firmware release.

**Physical installation is the hard part.** The modem is a card that plugs into a mating connector on the V-1000 motherboard. To install: open the CPU box, likely remove the IO board to reach the connector, insert the modem, and insert the SIM card (its slot sits under the modem). The antenna is about 30 cm and must be routed through an opening. The cabinet is all metal and the screen is shielded, so antenna placement is a problem. Options discussed: mount internally toward the front / plastic areas; use an external antenna through a hole in the rear; or add a small, discreet black plastic box on the rear of the cabinet to hold the modem, which keeps the standard 30 cm cable short and reliable. Connecting cables can be found in longer lengths, but the antennas themselves cannot be extended. Pavel will raise the mounting approach with Genadi.

**Real-hardware testing required.** The software was so far tested only on the "South Dakota" build; it must be tested on the specific Georgia (V3) build and on real Georgia machines with a real modem, because the same vendor's modem for different markets can be incompatible. If a chip or processor differs, they may need to connect to the Georgia machine remotely and add support, as was done with Flex IQ.

**Preparation tasks.** Val stressed sourcing the mountable plastic box first (shipping takes time even by air), then sending the box + modem + SIM to Georgia — or ordering the correct modem, antenna, and cable length locally in Georgia — and pre-ordering a SIM card so it is on-site. The full disassembly → SIM → modem → power-on sequence should be verified.

**Timeline.** Val asked whether it can be ready by August 18. Pavel is not sure V3 ships by the 18th. He checked with Ira: designer tasks (new resources and per-game demo/attract videos) are scheduled through August 25, and attract videos for all games run roughly August 17–25. They may ask the designers whether games can be shown without attract videos. Realistic landing is end of August. Separately, Val sent Pavel another request/spec to review and possibly implement — respond in writing, not urgent.

## Decisions Made

- **Carry the LTE modem support inside the GA-COAM V3 build** (which must go to the lab regardless); the modem is a free addition in that build. (Pavel, agreed by Val.)
- **Test on real Georgia machines with a real modem**, not just the office/South Dakota build. (Pavel.)
- **Target readiness is end of August;** August 18 is not firm because designer tasks run to August 25. (Val, Pavel.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Discuss antenna mounting — the discreet rear plastic-box approach — with Genadi | Aug 10 (today) | High | Cabinet is all-metal / shielded; 30 cm antenna |
| 2 | Pavel Frolov | Assemble the Georgia and Nebraska build with modem support and QA-test it | TBD | High | Development essentially done |
| 3 | Val Levitan / team | Source and ship the mountable plastic box + correct modem + antenna (right cable length) + SIM to Georgia; pre-order the SIM so it is on-site | TBD | High | Shipping takes time even by air |
| 4 | Pavel Frolov | Confirm with Ira a firm GA-COAM V3 ready date | Aug 10 (today) | Normal | Designer tasks currently run to Aug 25 |
| 5 | Pavel Frolov | Reply in writing to Val's separate request/spec on whether it can be implemented | TBD (not urgent) | Low | Val: not needed now |

## Open Questions

- Can GA-COAM V3 (with the modem) be ready by August 18, given designer tasks running to August 25? Likely end of August instead.
- Can the games be shown without attract videos? (To be asked of the designers.)
- What is the final antenna-mounting solution given the all-metal cabinet? (Pending Pavel/Genadi.)

## Dispatch Log

---
*Processed from Teams transcript on August 10, 2026 (scheduled meeting-watcher sweep)*
*Source meeting: LTE_V-1000_GA-COAM*
