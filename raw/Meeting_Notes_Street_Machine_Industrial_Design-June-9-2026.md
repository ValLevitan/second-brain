# Meeting Summary — Street Machine Design & Capabilities
**Date:** June 9, 2026, 1:29 PM Eastern
**Duration:** ~51 minutes
**Attendees:** Val Levitan, Genadi Peari
*(Spoken in Russian; summarized in English. Follows the June 8 low-cost street-machine session.)*

## Summary

Val walked through what's known and still open for the street machine: a single-screen unit with a vertical 43" HD display and a good black level. No topper, no static top — the whole design has to be self-contained on the one screen. The touchscreen must cover the full screen, not half, because skill features sit at the top and need to be touchable.

**Placement.** Machines should set up in clean formations — a straight line, back-to-back, or shapes (triangle, square). Backs need handles and wheels for moving. Floors won't be level (these aren't casinos), so the legs need a big adjustment range and must be levelable from the top, without reaching under the machine. Seating is unresolved: the panel won't stick out much, so where the player's knees go isn't clear yet.

**Service is the core of the business.** Val stressed this repeatedly. Front service access is mandatory, and every peripheral — bill validator, printer, buttons, screen — must have two-way feedback. That lets operators see status remotely (is the screen working, is a button dead), push software updates over the air, and pull service and accounting data. Without those recurring services, selling cheap machines alone is a hard business. The feedback hooks are what make the services sellable.

**Peripherals.** Leaning to a TITO ticket printer (cheapest); hide it in the door/bezel so the machine stays slim, with the printer still reachable for paper and service when the door opens. Paper comes pre-sized for the US region. Genadi noted the bill validator should also support TITO/rating tickets and a model still needs picking (JCM has options). Genadi proposed a back-load payload bill validator that drops down and opens together with the front-service door — Val agreed, said it keeps things flexible and makes Felipe happy: "make it a provision." Buttons: about 8, with one large spin button; the panel should flip from the back for easy button swaps.

**Lights.** Val prefers one perimeter light line — proven, industry-standard, nothing avant-garde, and not expensive; he won't cut $10 to make it worse. Genadi pushed two vertical strips or reusing the Flex light assembly; Val said vertical isn't enough. Halo light was discussed but Genadi noted it shows poorly in bright street locations (works in casinos). Not fully locked, but Val's clear lean is the single perimeter line.

**Build.** Cheapest body is sheet metal, and Val wants it monolithic — not split into a face plus extra parts. A cast/molded face would be limiting in metal, so a mold for that part suggests itself. The screen should be built into the cabinet (not hung outside like Flex), with a shallow panel — glass over a single metal cover/channel.

**Audio.** No amplifier and no subwoofer. Use the Rockchip board's built-in 3W/channel amp with two small fixed front-facing speakers. Saves about $20.

**Progressive.** When machines sit in a formation, link them through a cloud "progressive" control into a shared jackpot/bonus shown across screens — half-screen, third-screen, or the whole row's screens for a big bonus. Val thinks this is a strong feature.

**Next step — engage the industrial designer.** Val will write up everything discussed as a design task (not a spec) and send it to Genadi with this recording. Genadi will brief Igor in person to produce rough, radical hand-drawn concepts, and prepare a preliminary 3D model (~3 variants) to work with Igor or hand to a design agent. Val flagged Igor is slow and can't be rushed, so start now. Val will also re-confirm the bill-validator choice with Juan and recover the candidate list (an earlier recording was lost).

## Decisions Made

- **Single-screen unit, vertical 43" HD display, high black level; no topper or static top** — design self-contained on one screen. (Val)
- **Full-screen touchscreen** (not half) — skill features at the top must be touchable. (Val)
- **Screen integrated into the cabinet**, shallow panel, glass over one metal cover/channel — not hung outside like Flex. (Val)
- **Monolithic sheet-metal body** — not split into face + extra parts. (Val)
- **TITO ticket printer**, hidden in the door/bezel to keep the machine slim; bill validator must also support TITO tickets. (Val + Genadi)
- **Back-load payload bill validator that opens with the front-service door** — "make it a provision." (Genadi proposed, Val agreed)
- **No amplifier, no subwoofer** — built-in 3W/channel Rockchip amp + two small front speakers (~$20 saved). (Genadi, Val agreed)
- **One perimeter light line** — proven and cheap; don't over-invest. (Val's lean; not fully locked)
- **Two-way feedback on every peripheral + mandatory front service access** — the basis for recurring remote services and the business model. (Val, strong emphasis)
- **Cloud progressive linking machines in a formation** into a shared jackpot/bonus across screens — include it. (Val)
- **Keep building the passive Flex machine in parallel**; the street machine is a different principle. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Write the industrial-design brief (everything discussed today, framed as a design task, not a spec) and send it to Genadi with this meeting's recording | Right away | High | Gates Igor's work; Val said he'd do it immediately |
| 2 | Genadi Peari | Meet Igor in person and brief him to produce rough, radical hand-drawn concept sketches of the machine | Start ASAP | High | Igor is slow and can't be rushed; don't let him bottleneck |
| 3 | Genadi Peari | Prepare a preliminary 3D model (~3 variants) to work with Igor / hand to a design agent | TBD | Normal | Universal formats let any design agent iterate |
| 4 | Val | Re-confirm the bill-validator choice with Juan and recover the candidate list (earlier recording was lost) | TBD | Normal | Needed to lock the peripheral set |
| 5 | Val | Confirm button count and layout with Felipe and Juan (~8 buttons, one large spin button; Ivan already asked) | TBD | Normal | Drives the control-panel design |

## Open Questions

- **Coin validator type** — analog vs. other was raised earlier today; Val leans analog but isn't an engineer. Unresolved.
- **Skill/payline-style feature on the street machine** — Juan wants it (big sell on one device), Felipe disagrees, Val leans simple/no. Unresolved.
- **Player seating** — where the knees go, since the panel won't protrude much. Unresolved.
- **Front service-door mechanism** — acknowledged as perennially hard; Genadi to work the printer-in-bezel layout.
- **Cash-box / visual-inspection window** (a component Val called a "Kendall") — Val unsure if needed. *(Term unclear in transcript.)*

---
*Processed from Teams transcript on June 9, 2026*
*Source meeting: Street_machine_capabilites-June-9-2026*
*Initiative: Street Machine Design Direction*
