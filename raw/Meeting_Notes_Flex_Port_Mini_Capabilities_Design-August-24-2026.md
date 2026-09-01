# Meeting Summary — Flex-Port-Mini_capabilities (Design)
**Date:** August 24, 2026, ~10:06–11:34 AM Eastern
**Duration:** ~1 hour 27 minutes
**Segment:** Segment 2 of 2
**Attendees:** Val Levitan, Genadi Peari, Pavel Frolov
**Raw transcript:** [[Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026]]

## Summary

The team designed a new, stripped-down, low-cost port called **Flex-Port-Mini** and the business model to sell it.

**The product.** The Mini connects to a gaming machine only through the machine's second SAS port. Because of that, it does not need the heavy bill-acceptor / MudaGoose in-line wiring, which Pavel and Genadi called the most problematic part of today's port. Cash still enters the machine through the operator's existing bill acceptor as before; the Mini only handles loading credits (via SAS) and reading vouchers. The team wants the build cost as low as possible. Val pushed for ~$25-30; Genadi said ~$40-45 is realistic once you count the scanner module (~$11-15), its interface board, and memory. They agreed on ~$45 as the working budget. Today's full Flex-Port is roughly $140-210; its board alone was $45 before flash-memory prices rose.

**Screen.** Val wanted no screen. Genadi argued for a very cheap, non-touch information display (~$1-5) so the unit can show simple messages such as a cashout prompt. Val accepted a minimal screen at that price.

**Player use-case (voucher / eVoucher).** A player gives the cashier, say, $20 and receives a QR code — printed on a ticket, sent to the phone, or shown on screen for the player to photograph. The player presents the QR to any machine's optical scanner and all the money loads onto that machine at once (no partial loading; on cashout, all money comes off at once). Val wants to drop the PIN code that today protects the voucher. Pavel explained the PIN protected against a duplicated barcode; Val argued that since the original is consumed and a code can only be used once, the PIN is unnecessary — the same trust model as a TITO ticket. Pavel proposed a useful extra: embed a URL to JVL's cloud server inside the QR so that scanning it registers the transaction centrally. Playable-vs-redeemable money is only split at an intelligent device (Flex Recycler / Flex IQ), not at the port. The server can also grant promo credits (playable-only) per location.

**Networking (the main open problem).** The ports need a local network to reach Flex IQ / the server so vouchers can be validated. Options discussed:
- **Wired CAT5 / RS-485** — favoured. Reuse the wiring already run for MudaGoose. Genadi wants daisy-chain support so the operator just unplugs from MudaGoose and plugs into JVL. Protocol likely the existing WSS or a Modbus-style protocol (Modbus would need an encryption layer added).
- **WiFi** — Val rejected it: jammable, needs an antenna per machine, and an ESP32 module (~$10) breaks the budget.
- **Bluetooth mesh** — Pavel raised it for reliability and future use; nobody has experience with it, so it can't be estimated yet.
- **LTE / cellular modem per port** — too expensive (~$15-20 each).
They also discussed and rejected reverse-engineering MudaGoose's RS-485 protocol; better to build JVL's own board and use SAS, which is more reliable than the fledgling electromagnetic-counter signals.

**Business model.** Give the operator everything (Flex-Port-Mini + Flex IQ) for free. Charge a fixed monthly fee between $60 and $90 (Val referenced $65). The operator keeps the per-transaction income dollar that JVL takes today. Market math: ~42,000 machines across ~7,400 locations, ~5.9 machines per location (~6 ports). Hardware ~$120-180 in ports plus ~$200 for Flex IQ ≈ $320-380 per location; payback ~5-6 months at $65/month. Across 7,000 locations at $65 that is ~$455K/month.

**Two-stage rollout.** Stage 1 is the Mini + Flex-Port with wired CAT5 to each machine on the existing protocol. Stage 2 (future, not committed) would drop Flex IQ entirely and use any mobile device with a cashier app to issue vouchers — but that would need a modem in each SMIB port, raising cost back up.

## Decisions Made

- **Build Flex-Port-Mini connecting only via the machine's 2nd SAS port** — drops the bill-acceptor / MudaGoose in-line wiring, the most problematic part. Machines without a 2nd SAS (~15-20% of the market, ~10-15K units) are out of scope and expected to disappear within 2-3 years. (Val; Genadi and Pavel agreed)
- **Include a minimal, cheap, non-touch info display (~$1-5)** for simple prompts/messages. (Proposed by Genadi; accepted by Val)
- **Working build-cost budgets: Flex-Port-Mini ~$45; full Flex-Port ~$250.** (Val)
- **Stage-1 networking: individual wired CAT5 / RS-485 to each machine, reusing the existing WSS / Modbus-style protocol; wireless (WiFi / Bluetooth mesh) deferred to a later experiment; WiFi rejected for now.** (Val, Pavel, Genadi)
- **Do not cooperate with or reverse-engineer MudaGoose's RS-485; build JVL's own board and connect via SAS** (more reliable). (Pavel; Val agreed)
- **Business model: give the operator all hardware free; charge a fixed ~$60-90/month (~$65); operator keeps the per-transaction income dollar.** (Val)
- **Drop the PIN code from the eVoucher flow.** (Val decided; Pavel flagged the security trade-off)
- Considered and deferred: eliminating Flex IQ entirely in favour of a mobile cashier app + per-port modem — treated as a possible Stage 2, not decided now.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Write up the player use-case and the operator / master-operator business case in plain writing, using the ~$45 (Mini) / ~$250 (Flex-Port) budget assumptions, then have Claude produce the capabilities document; team to reconvene | TBD | High | Val stated he would do this and then "ask Claude to write the capabilities" |
| 2 | Genadi Peari | Source/spec a cheap non-touch info display and confirm flash/memory sizing so the Mini lands near the ~$40-45 build cost | TBD | Normal | Needed to confirm the budget is achievable |
| 3 | Pavel Frolov | Work out the Stage-1 local-network design — wired CAT5 / RS-485 (daisy-chain) on the existing WSS / Modbus-style protocol with an encryption layer; note Bluetooth mesh as a later experiment | TBD | Normal | Local network is required for voucher validation |

## Open Questions

- Is the ~$40-45 build cost actually achievable? Memory/flash sizing is unconfirmed (Genadi to check); Val is skeptical of $30 and landed on ~$45.
- Bluetooth-mesh viability is unknown — no prior experience, cannot be estimated yet.
- If an operator refuses to disconnect MudaGoose, new CAT5 wiring may still be required.
- The Stage-2 mobile-app approach needs a modem in each port, which raises cost back up — unresolved.

## Dispatch Log

---
*Processed from Teams transcript on August 24, 2026 (scheduled meeting-watcher run).*
*Source meeting: Flex-Port-Mini_capabilities-August-24-2026*
