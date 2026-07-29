---
type: meeting
title: 2026-03-30 — Genadi Peari OMNI Board Communication
date: 2026-03-30
aliases: [Call with Genadi Peari March 30 2026, OMNI Board Communication Genadi]
source-count: 2
---

# 2026-03-30 — Genadi Peari OMNI Board Communication

Thin stub. A very short (~1m24s), heavily garbled Russian/English call ([[wiki/people/val-levitan.md|Val Levitan]] ↔ [[wiki/people/genadi-peari.md|Genadi Peari]], recording base "Call with Genadi Peari", header 30 March 2026 9:51pm). An informational one-question call: Val asked why the board-to-board link that [[wiki/people/dima-pikulev.md|Dima Pikulev]] built in the OMNI hardware stack uses the chip it does.

**§12 — transcript + derived summary → ONE stub, source-count 2.** The transcript [[raw/Meeting_Transcript_Genadi_OMNI_Board_Communication-March-30-2026.md]] and the "# Meeting Summary — Call with Genadi Peari" derived notes [[raw/Meeting_Notes_OMNI_Board_Communication_Genadi-March-30-2026.md]] are the same meeting (§3 derived-document family); the notes are folded in.

Substance:

- **Board-to-board USB link — Full Speed chosen over High Speed on purpose.** Genadi confirmed they intentionally fitted a **USB Full Speed** chip rather than a **USB High Speed** one for the iBoard-to-mainboard communication, because the extra speed wasn't needed for the use case; there is an option to increase bandwidth later if required (the transcript is very garbled on exact figures — Full Speed vs High Speed USB are the standard 12 Mbit/s vs ~480 Mbit/s tiers). The exact board/component names could not be reliably reconstructed from the transcript. → [[wiki/people/genadi-peari.md]] (Mar-30). [[raw/Meeting_Transcript_Genadi_OMNI_Board_Communication-March-30-2026.md]] [[raw/Meeting_Notes_OMNI_Board_Communication_Genadi-March-30-2026.md]]

This is the hardware side of the **iBoard high-speed memory-chip / state-persistence latency** point [[wiki/people/alexander-biratka.md|Biratka]] raised earlier the same day — see [[wiki/meetings/2026-03-30-omni-architecture-biratka.md]] and [[wiki/topics/omni-core-advancement-and-game-templating.md]] (Mar-30).

§15.8 clear — hardware/board-selection only; no named-person compensation.

## Sources

- [[raw/Meeting_Transcript_Genadi_OMNI_Board_Communication-March-30-2026.md]]
- [[raw/Meeting_Notes_OMNI_Board_Communication_Genadi-March-30-2026.md]]
