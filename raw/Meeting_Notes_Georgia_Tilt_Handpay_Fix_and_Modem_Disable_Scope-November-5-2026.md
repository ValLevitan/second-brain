# Meeting Summary — Convo by the coffee machine
**Date:** November 5, 2026, 12:03 PM – 12:48 PM Eastern
**Duration:** ~46 minutes
**Attendees:** Val Levitan (organizer), Pavel Frolov, Irina Shishko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Georgia_Tilt_Handpay_Fix_and_Modem_Disable_Scope-November-5-2026]]

## Summary

**Georgia machines blocked by Intralot — root cause confirmed.** Sebastian's logs confirmed the guess from the last few days: the machine falls into a false handpay state. Critical tilts (lease expired, CPU high temperature) show a dialog with a Collect button. If the player presses it, a handpay dialog opens and the machine starts sending SAS exception 51 (handpay pending) to the host. It keeps sending 51 even after the dialog is closed. When Intralot later asks for the checksum, the machine is still busy with the pending poll and does not answer, so Intralot blocks the machine. Centre-type machines (Florida, South Dakota) are fine because their SAS host clears the handpay with long poll 1B or 94; Intralot never sends those, because Georgia has no handpay.

**Fix.** Two fixes, both agreed: remove the Collect button from the critical-tilt dialogs, and stop sending exception 51 once the handpay dialog is closed. Val first objected to removing the button, then understood it is the Collect button inside the tilt dialog, not the normal collect, and agreed.

**Val's rule: a tilt is a tilt.** When a critical tilt happens the machine does nothing else until the tilt is cleared and the machine is back to normal; only then does the money cycle continue. Letting the player take the money during a tilt was a wrong interpretation (the amount may be wrong, the player may have just won big, or may be cheating). Irina noted centre-type machines deliberately added collect-during-tilt; Val said that was wrong too. This is the standard for all machines, not only Georgia, and Val wants it written down.

**Release path.** The fix goes into the RIS improvements release, which most of the current software gets. Val: give the RIS improvements and this rule to the market for free, without changing the games — same Peach 1, Peach 2, Peach 3 packages, games and framework untouched; only the RIS and the setup screens change. Irina: 1.14 installs update in place with the new DC; the old 1.17.76 and 1.20/1.21 installs (about 5 years old, old RAS file format) need a full reinstall. The build was planned for November 9; it will not be ready then. Irina must talk with Evgeny about the test effort (many combinations: ICMS, machine, lease, passport reset) and expects the end of next week.

**Modem on Georgia Flex machines.** Pavel's proposal (discussed with Dima and Evgeny): keep the modem option always on and remove the operator on/off screen. If the machine cannot send data (no traffic), it just retries and sends when a connection returns, over the modem or wired internet; no real overhead. Val liked it but added one rule: an operator who does not want the modem must be able to disable it on purpose. If the manufacturer forces a modem that cannot be turned off and the operator's data later leaks (for example after the machine is resold and the new owner turns the modem on), that is negligence and a legal risk for JVL. An operator who sells a machine without clearing it is responsible himself. Agreed routine: the operator scans a QR code, the server records the event and returns an activation code (short, 2 characters, or the 4-character one used for the lease), and only then the modem is disabled. Pavel's idea to send a "modem disabled on purpose" packet before switching off stays. This widens the scope: Evgeny on the machine side, Dima on the server (Sergey is busy), maybe Anton Seregin for the QR code; about 3 days if the backend goes first.

**Why the modem now.** Irina: it was not planned for this release. Val: this is the ideal moment to put the modem on every machine, because every operator wants remote updates, and the fix above ships with it.

**Dates.** Val: hand the build to Eclipse on November 16 (the 15th is a Sunday). Eclipse needs about 4 days, so the market build should be available around November 20.

**Echo.** Irina: Echo needs a certified build, so it should ride this release. Val: Echo is not needed before February 1. Pavel: if the bill acceptor connected in Georgia arrives in time and tests fine, include it; the release will not wait for it. Val moved the bill acceptor test to February.

**Class A.** Val explained why: what JVL does for Georgia today is Class B. Class A is amusement machines under a 40-year-old law (max $50 win per wager, a loose definition of a game cycle, a big loophole). Val wants Class A machines on the market first, around January; the games are being pushed now and will run on the same Flex machines for now. Class A matters more than testing one bill acceptor.

## Decisions Made

- **Fix the Georgia Intralot block two ways: remove the Collect button from critical-tilt dialogs, and stop sending SAS exception 51 after the handpay dialog closes.** — The false handpay state blocks the checksum reply. (Decided by Val, Pavel, Irina)
- **Standard for all machines: during a tilt the machine does nothing except resolve the tilt; no money collection until it is back to normal.** — The amount may be wrong or the player may be cheating. (Decided by Val)
- **The fix ships in the RIS improvements release, free to the market, without changing games or framework.** — Same Peach packages; only RIS and setup screens change. (Decided by Val)
- **Modem on Georgia Flex machines is always on; the operator can disable it only through a deliberate routine (QR code, server event, activation code).** — Avoids a forced modem the operator cannot switch off, which is a legal risk. (Decided by Val, on Pavel's proposal)
- **Build to Eclipse on November 16; market availability around November 20.** (Decided by Val)
- **Echo / bill acceptor test moves to February; not needed before February 1; the release does not wait for it.** — Class A machines are more important. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov, Irina Shishko | Put the two tilt/handpay fixes into the RIS improvements build | November 16, 2026 | High | Remove Collect on critical-tilt dialogs; stop exception 51 after the dialog closes |
| 2 | Irina Shishko | Talk with Evgeny about the test effort and give a date for the RIS improvements build | TBD | Normal | She expects the end of next week; many combinations to test |
| 3 | Pavel Frolov | Add the modem-disable routine (QR code, server event, activation code) to the release scope and assign it | TBD | High | Evgeny (machine), Dima (server), maybe Anton Seregin (QR code); about 3 days |
| 4 | Pavel Frolov, Irina Shishko | Hand the certified build to Eclipse | November 16, 2026 | High | Market around November 20 |

## Open Questions

- Will the bill acceptor connected in Georgia arrive and test in time to ride this release? (Pavel) — the release does not wait for it.
- Exact date of the RIS improvements build — pending Irina's talk with Evgeny.

## Dispatch Log

---
*Processed from Teams transcript on November 5, 2026, 2:10 PM Eastern*
*Source meeting: Convo by the coffee machine*
