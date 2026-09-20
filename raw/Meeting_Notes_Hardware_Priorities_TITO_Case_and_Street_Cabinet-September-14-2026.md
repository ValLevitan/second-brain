# Meeting Summary — Alignment and scheduling
**Date:** September 14, 2026, 12:00–13:00 PM Eastern (recording 12:04–12:42)
**Duration:** ~38 minutes
**Attendees:** Val Levitan, Genadi Peari, Pavel Frolov
**Raw transcript:** [[Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026]]

*Spoken in Russian. Transcription mangles many English technical words; where a term was unclear it is marked below.*

## Summary

A hardware and firmware priority walk-through with Genadi and Pavel. Val went item by item and set the order of work for the next two weeks.

**Flex IQ changes.** Val asked where the changer/reader placement change and the removal of the rear screen stand. Genadi: Elizabeth received 10 covers, and 10 units can be done by hand because the boards are already changed. The screens cannot simply be taken off — he still has to order a cover this week and issue a permanent change. Not done yet.

**Rear screen in MVP1.** Val told Pavel the screen must still show something in MVP1, even a standard image. Pavel said they planned a promo screen ("you can collect your winnings here") that stays on the display; the dialogue with the player is removed and everything else stays.

**LTE modems.** Val was blunt: if the cell modem does not work, not a single unit goes into the field — it has to work perfectly. Pavel wants to order KORE modems now, in two different sample form factors: M.2 slot and mini-PCIe. In parallel he and Andrei will try the same SIM cards to see how they behave. Genadi said the modem worked on Flex IQ immediately and the problem is SIM incompatibility. Pavel would not accept that yet — it has to be tested with that SIM, it could be anything. Both agreed a different SIM worked straight away.

**Firmware over-the-air update.** Val said MVP1 must include remote firmware upgrade — IQ, kiosk or FlexPort — and it has to be perfect: verification, timer, confirmation. Pavel's order: priority 1 is Flex IQ and FlexPay updating themselves; priority 2 is those units distributing and flashing FlexPort firmware. Dzmitry Chudzinau will first work on the Flex IQ ↔ FlexPort protocol from his side and may improve it; Alekseev may be needed and already has a task on this.

**FlexPay Slim.** Drawings are released and the Chinese supplier took the metal into work last week, shipping Friday, for the 10 units in hand. Genadi planned to release the full bill of materials and the complete drawing set the same day — including new harnesses for the card dispenser — so that a request for about 50 units could be issued the next day.

**Card dispenser level.** Val wants to know the card level mechanically, not by counting issued cards. Pavel: counting does not prove nobody removed cards; at least one dispenser model has a sensor set to a chosen depth that signals at 20, 30 or 40 cards remaining. Val said order the dispensers with that option. Pavel warned the sensor polling did not work on one model and must be re-checked. Genadi proposed Sinkotek (name uncertain in transcript) — cheaper, better, and it had a low-level indicator. Pavel agreed to test it.

**Recycler.** The validator arrived with Elizabeth and Misha is organising the shipment to Belarus. It is very big, so only one will be ordered; the pad differs, everything else is the same. The bill acceptor is removed, the optical sensor and printer stay. Genadi has not checked whether the dispenser still fits — if it does, only at the very bottom. They will take option 2, the variant that keeps the dispenser. Integration starts when it reaches Minsk. Pavel brought good news: the recycler's documentation includes an ARM library, which saves about a week of development.

**Street cabinet (Flex S).** Val's idea is a monolithic wooden rear housing, not split into base and top, like the older Eclipse machine with a wooden body and a fibreglass front. Genadi has ideas already written down and wants to simplify both the body and the electronics. On the screen, going to 43" and taller means 4K, which the current board cannot drive, and touchscreen prices jump sharply above 43" (next size is 49"). Target build cost is $1,000. Pavel asked how the screens connect. Genadi's initial plan is the main monitor via the controller, the second screen the same way as on IQ using their own adapter. They then considered making LVDS the main output to save the controller: controller $35 against their own cable and adapter at $15–20, so a saving of roughly $15–20. Genadi called that not very efficient, but Val said once a direction is chosen it will not be changed, so decide now — go with LVDS as the main, and the optional second screen over HDMI with a controller.

**Board choice.** Val recalled a report that the RK works well on a horizontal screen and badly on a vertical one. Pavel confirmed it, and said the Chinese documented it — it is specifically the RK3568. Genadi said that is why they are sending the RK3576, about $15 more with 8 GB, and it is the target board for this machine. Pavel will first get one game running on it and then judge memory use; the SDK for the 3576 board still has to be reworked, and the integration repository he has described before still has to be built.

**Standalone TITO printer.** Genadi said his remaining priority was to release a standalone TITO printer and standalone card dispenser as peripherals. Val rejected that ordering — the cabinet comes first. Genadi argued a TITO printer has to sit next to the IQ anyway and at least the wiring must be ordered. Val agreed it is needed but said such cases will be few: first the IQ goes out, then it is added to. After the detail discussion, Val set the sequence explicitly — finish the TITO cases, then move to the street machine. The enclosure needs a special harness, a proper box with connectors on a back panel, and a separate external desktop power supply with RS-232 coming in from outside rather than AC inside. Genadi asked whether to provision 200 or 400 tickets; Val said design the back slightly bigger so 400 always fits. Security is not needed — it is only a printer.

**Ticket printing failures.** Val pressed on what happens if printing breaks part way: the player has paid and must get the ticket, so JVL has to be able to say the transaction failed and return the money or complete it. Pavel: their libraries read the printer state, unplugging triggers a tilt immediately and plugging back clears it. Up to a point the money can come back, but once the barcode is printed the money is taken off the machine. The sensor confirming the ticket fully exited is already inside the printer. The unsolved case is a deliberate power cut once the barcode has started printing — that ticket is real, can be redeemed, and the money cannot be returned. Genadi asked whether the printer reprints an incomplete ticket; Pavel said no.

**Enclosure work for Sasha.** Val asked Genadi to hand the box to Sasha. Genadi preferred to work out the details first — bezel, whether they build their own electronics or buy, how it opens, where access is needed, the wiring — then hand over; bent metal is a one-day job not worth delegating. Val said no metal: 3D print first, then order a production tool for plastic. A metal object on a desk is not a modern approach. Genadi agreed Sasha can take the plastic box design once the details are prepared.

**Cabinet start date.** Genadi will finish IQ, then Slim, then IQ again, then the printer this week, and can start the street cabinet the following week — the 23rd. Val confirmed the date.

**RK3576 shipment.** Val wants the delivery to Minsk pushed urgently and believes Misha Perelman controls it. Genadi looked it up: supplier "Touch Intelligent" (name uncertain), amount around $300 plus shipment, 2 samples at $150 each and about $65 freight to Minsk.

## Decisions Made

- **MVP1 keeps a promo screen on the rear display; the player dialogue is removed.** Val required something on the screen; Pavel's promo-screen plan satisfied it. (Val Levitan, Pavel Frolov)
- **Order KORE modems now in two form factors — M.2 and mini-PCIe.** One type for each product line; nothing ships unless the modem works perfectly. (Pavel Frolov, Val Levitan)
- **Remote firmware update is in MVP1.** Priority 1: Flex IQ and FlexPay update themselves. Priority 2: they distribute and flash FlexPort firmware. (Val Levitan, Pavel Frolov)
- **Card dispensers will be ordered with the low-level sensor option, and Sinkotek will be tested.** Counting issued cards is not enough — Val wants mechanical verification. (Val Levitan, Genadi Peari, Pavel Frolov)
- **Only one recycler will be ordered, in the variant that keeps the card dispenser (option 2).** The unit is large and the bill acceptor is dropped. (Genadi Peari, Val Levitan)
- **Street cabinet main screen goes over LVDS with JVL's own cable and adapter; the optional second screen goes over HDMI with a controller.** Saves roughly $15–20 per unit, and Val wanted the direction fixed now because it will not be changed later. Target build cost $1,000. (Val Levitan, confirmed back by Pavel Frolov)
- **The new platform uses the RK3576, not the RK3568.** The RK3568 performs badly on a vertical screen, which the supplier documented. (Genadi Peari, Pavel Frolov)
- **Work order: finish the TITO printer cases, then start the street cabinet.** Genadi's proposal to release standalone TITO printer and card dispenser peripherals first was rejected; after the discussion Val set this sequence. (Val Levitan)
- **Genadi starts the street cabinet on September 23.** After finishing IQ, Slim and the printer this week. (Val Levitan, Genadi Peari)
- **The TITO enclosure uses an external desktop power supply and RS-232 from outside, with connectors on a back panel, sized for 400 tickets.** No AC inside the box; security is not required. (Genadi Peari, Val Levitan)
- **Enclosures are 3D printed first, then tooled in plastic — not metal.** (Val Levitan)

Considered and superseded: releasing the standalone TITO printer and standalone card dispenser as peripherals ahead of the street cabinet — replaced by TITO cases first, then the cabinet.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Order the Flex IQ cover and issue the permanent change for the rear-screen removal | Week of Sep 14 | High | Boards already changed; 10 units can be done by hand |
| 2 | Genadi Peari | Release the full bill of materials and complete drawing set for FlexPay Slim, including the new card-dispenser harnesses | Sep 14 | High | So a request for ~50 units can be issued Sep 15 |
| 3 | Pavel Frolov | Order KORE modems — two samples, M.2 and mini-PCIe | ASAP | High | Blocking: no field deployment until the modem works |
| 4 | Pavel Frolov, Andrei | Test the same SIM cards on the Flex units to confirm whether the fault is the SIM or the modem | TBD | High | Genadi says SIM incompatibility; Pavel not convinced |
| 5 | Dzmitry Chudzinau | Work the Flex IQ ↔ FlexPort firmware-distribution protocol from his side and improve it if possible | TBD | Normal | Feeds priority 2 of the OTA update work |
| 6 | Pavel Frolov | Verify that the Sinkotek card-dispenser low-level sensor actually reports | TBD | Normal | Sensor polling failed on an earlier model |
| 7 | Genadi Peari | Check whether the card dispenser fits alongside the recycler, and order the option-2 unit | TBD | Normal | Not yet checked; fits only at the very bottom if at all |
| 8 | Genadi Peari | Design the standalone TITO printer enclosure — back-panel connectors, external desktop power supply, RS-232 from outside, sized for 400 tickets | Before Sep 23 | High | Precedes the street cabinet in the work order |
| 9 | Genadi Peari | Start the street cabinet | Sep 23 | High | After IQ, Slim, printer and the TITO cases |
| 10 | Genadi Peari | Hand the plastic enclosure design to Sasha once the details are worked out | TBD | Normal | 3D print first, plastic tooling later |
| 11 | Pavel Frolov | On arrival of the RK3576, launch at least one game and report memory usage; rework the SDK for the 3576 board and build the integration repository | TBD | High | No game has run on the current version yet |
| 12 | Misha Perelman | Push the RK3576 shipment to Minsk — 2 samples at ~$150 plus ~$65 freight | Urgent | High | [Needs Val's confirmation] — Val named Misha as the owner; Genadi looked up the vendor details but ownership of the action was not stated aloud |

## Open Questions

- Does the card dispenser physically fit in the recycler variant of FlexPay Slim? Genadi has not checked.
- Does the Sinkotek dispenser's low-level sensor polling work? Pavel recalls a model where it did not.
- No answer to a deliberate power cut once a ticket's barcode has started printing — the ticket is redeemable and the money cannot be returned. Raised by Pavel, left unresolved.
- Exact status of the RK3576 invoice and shipment — Genadi did not know whether it had gone out.
- Whether LVDS can in fact drive the main screen; agreed as the direction, still to be proven.

## Dispatch Log

---
*Processed from Teams transcript on September 15, 2026*
*Source meeting: Alignment and scheduling*
