# Meeting Summary — Low-Cost Street Machine Design
**Date:** June 8, 2026, 9:48 PM Eastern
**Duration:** ~30 minutes
**Attendees:** Val Levitan, Genadi Peari
*(Spoken mostly in Russian; summarized in English.)*

## Summary

Val wants to design a stripped-down "street" gaming machine because street prices have dropped a lot. The target: build the whole device for under **$2,000 including the bill acceptor**. He counts the bill acceptor at ~$800, so the machine itself must come in around **$1,200**.

Business model: sell cheap, then charge a recurring connection/subscription fee — about **$3 a day**, or **~10%** of revenue for operators who prefer that. Val would justify the fee with constant software updates and "intelligence" (service data, statistical/accounting data). He floated a sale price of **$5,000–6,000** but said those numbers are rough guesses. The aim is to sell far more machines at a lower margin plus recurring fees.

Design direction Val wants:
- **Single 43-inch monitor.** Either a bare touchscreen on the monitor, or a plain 43" monitor plus a small VDEC touchscreen. Genadi thinks the small-screen option is cheaper (a 15" touchscreen runs about $45).
- Make it flat and simple — "as cheap as an iPhone."
- **One door only**, for the bill acceptor and cassette. No other access, no stand, no open/close light fixtures. Cut cost in many small places — "it adds up."

Cost work (Genadi, rough): starting from the current **Flex** machine, moving the main board to a **Rockchip** platform and dropping the amplifier, light board, light controller, counters board and VDEC saves roughly **$500–600 in parts** before touching the cabinet. The metal cabinet itself is only about $300, so there's little to save there. Genadi noted parts prices are rising (Rockchip doubled, memory up 4x).

One cost lever has a catch: cutting the non-volatile memory down to "records only" (dropping game-state storage) saves money but runs into **jurisdictional compliance** — flagged, not resolved.

Val's main new idea: **build the bill-path "nose"/bezel ourselves** instead of buying the $35 plastic one, and **integrate a QR-code reader** into it, plus either a small info screen or lit tactile buttons. That would let them strip the complex player-tracking port and its screen down to something simple. Genadi liked the QR-in-the-nose idea ("brilliant") but is cautious about fitting it into other makers' cabinets, where the bill acceptor sometimes sits too low. He'll work it out and check.

Next step: Val meets **Piratka and Pavel tomorrow (June 9) at 8:00** to get their read on whether the direction is feasible. *(Names as spoken — Piratka is a nickname; Pavel is likely Pavel Frolov.)*

## Decisions Made

- **Target a sub-$2,000 all-in device** (~$1,200 machine + ~$800 bill acceptor). Street prices have dropped. (Val)
- **Pair the low price with a recurring fee (~$3/day or ~10%)**, justified by constant updates and service/statistical data. (Val)
- **Move the main board to Rockchip and remove the amplifier, light board, light controller, counters board, and VDEC** — ~$500–600 parts savings. (Genadi's costing, endorsed by Val)
- **Strip the cabinet** to one bill-acceptor/cassette door, single 43" monitor, no stand or light fixtures. (Val)
- **Pursue a self-built bezel/"nose" with an integrated QR-code reader**, replacing the $35 plastic nose and the complex player-tracking port. (Val; Genadi to develop)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Gather reference images of low-cost cabinet designs to test whether the cheap-machine direction is viable | Before Jun 9 meeting | Normal | Val wants to confirm the direction can exist before detailing it |
| 2 | Genadi Peari | Develop the integrated bezel/"nose" concept — built-in QR reader + bill path + small info screen or lit buttons — and check it fits common cabinets | TBD | Normal | Replaces the $35 plastic nose and the player-tracking port; Val's main cost idea |
| 3 | Genadi Peari | Check whether modern projected-capacitive touchscreens hide the ITO grid line | TBD | Low | Decides if a bare touchscreen on the 43" looks clean without painting |

## Open Questions

- Ticket printer: include one or not? Left to discuss.
- Compliance vs. memory savings: cutting non-volatile memory to "records only" saves cost but may break jurisdictional compliance — unresolved.
- Touchscreen line visibility (undertaking 3) — needs checking before committing to a bare touchscreen.
- Will the integrated nose fit other makers' cabinets where the bill acceptor sits low? Genadi's concern, unresolved.

---
*Processed from Teams transcript on June 8, 2026*
*Source meeting: Street_Machine-June-8-2026*
*Initiative: Street Machine Design Direction*
