---
type: meeting
title: FlexPort / SMIB completion-scope alignment (Sept 17 2025)
date: 2025-09-17
aliases: [FlexPort completion scope, FlexSMIB scope, SAS Bridge, System validation, FlexPort finish tasks, WSS parameter config]
source-count: 1
open-commitments: 5
open-questions: 2
---

# FlexPort / SMIB completion-scope alignment (Sept 17 2025)

**Date:** 2025-09-17 (10:59 AM) · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]] (opens), [[wiki/people/eugine-yavorski.md|Eugine Yavorski]], [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/pavel.md|Pavel Frolov]]. Russian.

A scoping meeting to list everything remaining to **finish the FlexPort product** — the embedded/dev completion thread alongside the Sept POS-back-end work. On the flexpay/transactional arc: continues the [[wiki/meetings/2025-08-05-flexport-embedded-progress-review-update-mechanism-boards.md|Aug-5 embedded progress review]] and the [[wiki/meetings/2025-09-15-flex-pos-alignment-scheduling.md|Sept-15 POS alignment]]; substance folds into [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept-17 section).

**Product framing (Val).** FlexPort = **two devices**: the main **FlexPort** (with screen + touchscreen) and the **SMIB port** (a simple interface installed inside the machine). **FlexPort works with the e-wallet scheme; FlexSMIB works with the TITO scheme** (Pavel). FlexPort/e-wallet currently connects only to one CM type (garbled). [[raw/flex-port_alignmen-september-17-2025.md]]

Durable points (single source):

- **FlexPort remaining scope (Yavorski).** Board redesign — new boards to verify / test / connect (a "**Zhenya**" who did the board redesign is finishing / away this week — identity unresolved, queued); support **two bill/email validators** (two protocols, one transcribed "Jamoasi", the other unclear) while Val kept the **"M protocol" out of scope for now**; the **cashout negative scenario** (see below); **system-time synchronization** across components (almost done); **finalize logging** (basic version exists, needs guidance on content); a **Python utility to prepare the bin files** (the build emits a hex; a separate program compiles the `.bin` for updates); and the **over-the-air update mechanism** itself (started; a small hang after loading the memory program). Estimate **~3 months to finish both configurations**; Yavorski to resend the itemized list with per-item effort and priorities so a dated schedule can be agreed. [[raw/flex-port_alignmen-september-17-2025.md]]
- **The cashout negative scenario.** When a client cashes out but **walks away without taking the credit**, the credit currently **disappears**. [[wiki/people/juan-martinez.md|Juan]] asked for a **15-second delay** but gave no full recipe; the fix direction is to **pass the abandoned credit back to FlexPay** so it remembers the client left without it. Still to be designed. [[raw/flex-port_alignmen-september-17-2025.md]]
- **SMIB remaining scope (Alekseev).** Logging done (needs testing; on a Dmitri's advice all program changes were added to a block); an item ready in a separate project needs integrating into the single project (transcribed "Sodi Zero 3", unclear); the **new boards** (the summer "Zhenya" boards) are included but need a **continuous-run test** + internal-settings check + project migration; **pass-through protocols** — "**enhanced security mode**" is implemented, but "**System validation**" is **not yet** (to finish); **negative scenarios on the SMIB board** (cable disconnect, restarts) are **not yet addressed** (a big chunk); plus time-sync, logging and download carried over from FlexPort. [[raw/flex-port_alignmen-september-17-2025.md]]
- **"SAS Bridge" mode (deprioritized).** A transparent **1:1 relay of SAS commands** so the operator gets full control — sending SAS commands **through** the device to the gaming machine. [[wiki/people/pavel.md|Pavel]] pushed it out **~6 months (not before the new year)** given the FlexPay-support priority and limited resources, though Yavorski said it is **not hard on their side**. [[raw/flex-port_alignmen-september-17-2025.md]]
- **Interface-selection decision — extend the WSS protocol.** For choosing between the two interfaces (e-wallet vs the other), the group rejected a dedicated **service menu / DIP-switch / jumper** and rejected pure **auto-detect** (poll protocol 1, fall back to 2, else "nothing connected" — can error on differing formats). Resolution: **extend the WSS protocol** (FlexPort ↔ FlexPay), likely by extending the **device-registration command**, so extra parameters are set from **FlexPay's large screen** rather than on FlexPort itself. [[raw/flex-port_alignmen-september-17-2025.md]]
- **Industrial design (Genadi).** The single-board ("one board") solution is done; Genadi needs the **final layout** to order plastic + tooling, and the scanner integration needs an **external plastic part**. Val: the plastic cover installs **on the outside like an envelope/cover** over the rough assembly (the device mounts inside the machine; the cover goes outside), making it more elegant — and it must be finished **before mass production of the board**, since mounting holes / sizes / backlighting could still change. **Backlighting is required**: the barcode-reader backlighting is already planned, but Val wants the **whole surface/bezel** lit (not just the perimeter) — like a new "Lightning" machine he saw where the whole area glowed and shimmered "like an aura." The **SMIB port** also needs a **plastic enclosure with properly-labeled connectors** (electromechanical parts). [[raw/flex-port_alignmen-september-17-2025.md]]
- **Unsupported machine + Toronto-office logistics.** Genadi flagged a machine on the market **not yet supported** (an e-wallet variant); all machines must be supported by completion. [[wiki/people/evgeniy-alekseev.md|Alekseev]] is to **visit the Toronto office (~October)** to connect and test it — the **Toronto office is closing until December**, and the machines ship back to **Georgia ~November**. [[raw/flex-port_alignmen-september-17-2025.md]]
- **Process (Val).** Val will run the transcript through AI → a list of all points → hand it to Yavorski → Yavorski reviews/adds and drafts → discusses with Alekseev → posts the **new draft + a time-graph schedule** into the Teams chat for everyone to review. [[raw/flex-port_alignmen-september-17-2025.md]]

## Open commitments

- [ ] Eugine Yavorski — resend the itemized FlexPort task list with per-item effort estimates and priorities so a dated ~3-month schedule (both configurations) can be agreed — due ~soon after Sept 17 — [[raw/flex-port_alignmen-september-17-2025.md]]
- [ ] Eugine Yavorski / Evgeniy Alekseev — design the cashout-negative-scenario handling (pass an abandoned credit back to FlexPay; incorporate Juan's 15-second delay) — due unspecified — [[raw/flex-port_alignmen-september-17-2025.md]]
- [ ] Evgeniy Alekseev — visit the Toronto office (~October) to connect and test the currently-unsupported e-wallet machine before it ships to Georgia (~November) — due ~October — [[raw/flex-port_alignmen-september-17-2025.md]]
- [ ] Genadi Peari — finalize the FlexPort single-board plastic layout / external cover (with full-surface backlighting) and the SMIB plastic enclosure, and order plastic + tooling before mass production — due unspecified — [[raw/flex-port_alignmen-september-17-2025.md]]
- [ ] Val Levitan — turn the transcript into a point list + time-graph schedule and post it to the Teams chat for Yavorski/Alekseev to iterate — due ~soon after Sept 17 — [[raw/flex-port_alignmen-september-17-2025.md]]

## Open questions

- Does JVL need to support "System validation" at all, if every target machine supports enhanced-security mode (Pavel would just force enhanced-security)? — [[raw/flex-port_alignmen-september-17-2025.md]]
- Who is the "Zhenya" who did the FlexPort board redesign / made the summer boards, and is finishing/away this week? (Fits none of the three owner-ruled Zhenyas by context — hardware/boards; queued.) — [[raw/flex-port_alignmen-september-17-2025.md]]

## Sources

- [[raw/flex-port_alignmen-september-17-2025.md]]
