---
type: meeting
title: Call with Genadi Peari — digital-amplifier standalone device + POS audio design requirements (Nov 19 2025)
date: 2025-11-19
aliases: [Genadi Peari Nov 19, digital amplifier standalone USB device, hot-pluggable amplifier, Flex speaker design, leave design to professionals]
source-count: 2
---

# Call with Genadi Peari — digital-amplifier standalone device + POS audio design requirements (Nov 19 2025)

**Date:** 2025-11-19 (recording headers 8:40 PM and 8:44 PM) · **Duration:** 2m 17s + 5m 4s ≈ 7½ min total · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]]. Russian.

A brief hardware one-on-one on the **digital audio amplifier** for the Flex platform and on how JVL should write its POS **audio/design requirements**. Substance lives on [[wiki/people/genadi-peari.md]] (Nov-19); part of the FlexPay/POS payout-device hardware arc ([[wiki/topics/flexpay-business-architecture-payout-devices.md]]).

**§12 — one call in two recording segments (not two meetings).** Both raw files share the recording base name **"Call with Genadi Peari"**; segment 1 ([[raw/Call_Genadi-November-19-2025-1.md]]) starts 8:40:39 PM and runs 2m17s (ends ≈8:42:56), segment 2 ([[raw/Call_Genadi-November-19-2025-2.md]]) starts 8:44:23 PM (≈1½-min gap). Segment 2 opens "**another note on what we just discussed**" ("Ещё один ноут то, что мы сейчас проговорили…") — a direct continuation of the same conversation, same two participants, same audio/amplifier topic. Treated as **one brief call in two segments → one stub, facts recorded once**, both files cited inline per §3 (multi-source stub). Corpus-wide `qmd update`+grep: neither filename is cited anywhere but `log.md`; confirmed new.

Durable points:

- **The digital amplifier must become a standalone, hot-pluggable device.** Today the amplifier is baked into the framework, so if its connection drops "the whole system, the whole game falls," because it is wired into the framework (data-base and all). Genadi restated the earlier plan to break it out as a **standalone USB device** that is **hot-pluggable** — if it randomly disconnects the system must **not crash**; it should recognise the amplifier fell off, return a defined error/"procedure error" response, and be able to **re-attach on the fly and keep working**. Only then can JVL use it fully — a serious cabinet without a **digital amplifier** won't produce adequate sound. [[raw/Call_Genadi-November-19-2025-1.md]]
- **Ties to the Flex model's new speaker design.** Val added that JVL wants to move to the **Flex model with a new speaker design** (no old enclosure/"grille"), which needs a 3-way / talented speaker setup and doesn't come immediately. [[raw/Call_Genadi-November-19-2025-1.md]]
- **For the POS/dispenser devices: provide a speaker, an audio hub and a monitor switch, then leave the design to professionals.** Val listed the audio components the POS devices need (a speaker, some kind of audio hub that can transmit, a monitor switch) to fold into the design requirements. [[raw/Call_Genadi-November-19-2025-2.md]]
- **Val's design philosophy — hand the graphics/UX to the specialists.** Val explained (as he was taught, and accepts) that because he is **not an engineer** and can't influence everything without running out of time, the right approach is to **specify the available building blocks** ("here is the optic, here is the speaker — please design as you see fit") and hand the graphics / user-experience work to the professionals who know how to convey effect, mood or "pressure," rather than dictate it. If he tries to influence everything he'll miss things, so he'd rather say nothing and give the designers the components and freedom. [[raw/Call_Genadi-November-19-2025-2.md]]
- **One design constraint he does impose: speaker placement.** When writing the speaker requirement, it must be positioned so it is **not on top / cannot have anything spilled on it** — that placement is a design/reliability rule the designers must respect. [[raw/Call_Genadi-November-19-2025-2.md]]
- **Add these to the design requirements; Val is recording and will forward it.** Genadi agreed to open the design and add the feature; Val noted he is recording the call and will send it on (mentioning forwarding to a colleague — name garbled) so the requirement is easier to capture. [[raw/Call_Genadi-November-19-2025-2.md]]

**§15.8:** clear — hardware/audio design content only; no compensation.

## Sources

- [[raw/Call_Genadi-November-19-2025-1.md]]
- [[raw/Call_Genadi-November-19-2025-2.md]]
