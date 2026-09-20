---
type: meeting
title: Hardware priorities — the TITO case and the street cabinet (Sept 14 2026, 12:04 PM)
date: 2026-09-14
aliases: [Hardware Priorities TITO Case and Street Cabinet, Alignment and scheduling, the 12:04 hardware call, Flex S priorities call, флекс эс это стрит машина, Sept 14 hardware walk-through]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Hardware priorities — the TITO case and the street cabinet (Sept 14 2026)

**Date/time:** September 14 2026, **12:04 – 12:42 PM Eastern** (~38 minutes) — the recording header; the source files head the slot as 12:00–13:00 with the recording inside it. **Series:** a Microsoft Teams session titled `Alignment and scheduling`. **Language: Russian** — the raw transcript is kept in Russian; the derived notes are an English gloss [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/pavel.md|Pavel Frolov]] [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**Purpose:** Val walks the hardware and firmware list item by item — Flex IQ changes, the rear screen in MVP 1, LTE modems, firmware update, FlexPay Slim, the card dispenser, the recycler, the street cabinet, the compute board, the TITO printer enclosure — and sets the order of work for the next two weeks. He opens with "**Давайте начнем**" and closes on the board shipment [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

## Reading warning — the notes are a gloss, not the source

The derived notes carry their own caveat: *"Transcription mangles many English technical words; where a term was unclear it is marked below."* That is accurate and it matters here. Many English product and component words arrive in the Russian transcript as garbles — "укора" (KORE), "минипис" (mini-PCIe), "у людей с" (LVDS), "найки" (on IQ), "фейервер" (firmware), "центов" (units), "синкотек", "тач интеллигент". Where the pages below read a garble, the reading is labelled an **inference** and the Russian string is kept. One correction is made against the notes outright: the firmware requirement is pings/verification/timer, not "verification, timer, confirmation" — see the firmware decision.

## Where the substance lives

- [[wiki/decisions/2026-09-14-tito-printer-cases-come-before-the-street-cabinet.md]] — Genadi's rejected standalone-peripherals proposal, the enclosure spec (external desktop power supply, RS-232 from outside, back-panel connectors, 400 tickets, no security), plastic-not-metal, and the **September 23** cabinet start date.
- [[wiki/decisions/2026-09-14-street-cabinet-main-screen-runs-on-lvds-not-a-controller.md]] — LVDS as the main output, the $15–20 saving, Full HD locked in, the 43-inch/4K constraint, and the $1,000 build target.
- [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]] — the RK3568's vertical-screen defect, the move to the RK3576 with 8 GB, the SDK and integration-repository work, and the Minsk shipment.
- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] — firmware update inside MVP 1, and the two-priority order.
- [[wiki/decisions/2026-09-04-north-america-modem-variant-and-ask-kore-for-the-apn.md]] (Sept-14 update) — Val's no-modem-no-deployment gate, the two modem form factors to order, and the SIM-versus-modem disagreement.
- [[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]] (Sept-14 12:04 update) — the loss case a dead printer *cannot* cover: a deliberate power cut once the barcode has started.
- [[wiki/topics/low-cost-street-machine.md]] (Sept 14) — the wooden monolithic body idea and the whole street-cabinet timeline.
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 14, 12:04) — FlexPay Slim drawings and BOM, the card-dispenser low-level sensor, and the recycler option-2 choice.
- [[wiki/people/genadi-peari.md]] and [[wiki/people/pavel.md]] (Sept 14, 12:04) — how each of them argued it.

## §12 note — five recordings, five events

This is the **fourth** of **five** recordings Val made on Sept 14 2026 (6:38, 7:37, 8:01, 12:04 and 12:51 ET). It is **not** the [[wiki/meetings/2026-09-14-competitor-field-reconnaissance-and-class-a-visits.md|12:51 PM call]] that follows it 47 minutes later: that one is in English, one-to-one with a US-side colleague, about Georgia site visits — different language, attendees and subject, its own recording. The other three are [[wiki/meetings/2026-09-14-texas-vertical-conversion-and-georgia-game-base.md|6:38]], [[wiki/meetings/2026-09-14-code-standards-main-branch-rule-and-alekseev-coaching.md|7:37]] and [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|8:01]].

The notes and the transcript are one **derived-document family** (§12) — one meeting, one stub, both cited.

## Names left unresolved (§4)

- **"саше" (Sasha)** — given the plastic enclosure to design. Fits no known person's role here; queued, not matched. See the TITO-cases decision.
- **"Андрей"** — testing SIM cards with Pavel. The corpus holds three distinct Andreis and none is a hardware/SIM tester; queued, not matched.
- **"это клипс"** — the older machine Val invokes as the wooden-body precedent. The derived notes read it as "the Eclipse machine"; the only "Eclipse" in this corpus is a **certification lab**, not a cabinet. No machine identity is asserted. See [[wiki/topics/low-cost-street-machine.md]].
- **"vivan sousend"** — the product the second modem form factor is for. Not interpretable; recorded as rendered.

## Sources

- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
