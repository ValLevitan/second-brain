# Meeting Summary — Call with Lev Rudky
**Date:** April 7, 2026, 5:25 PM Eastern
**Duration:** ~15 minutes (recorded portion of a ~2-hour meeting)
**Attendees:** Val Levitan, Lev Rudky

## Summary

This meeting was part of a longer (~2-hour) session focused on the Accounts Payable payment scheduling workflow in Microsoft Business Central (MSBC). The conversation was circular and extended, with the core issue only becoming clear after sustained questioning by Val.

**The Core Issue: Wrong Add-On for Payables**

JVL uses two add-on modules from AP Commerce for payment scheduling in Business Central:

1. **Installment Payment** — designed for Accounts Receivable (A/R). This module is already installed, configured, and working well for the receivables side of the cycle.
2. **Progress Payment** — designed for Accounts Payable (A/P). This module has not been installed or configured.

Lev had been attempting to use the Installment Payment add-on (the A/R tool) for the payables side of the accounting cycle. It did not work for this purpose — the module is not designed for A/P workflows. The recorded transcript captures the moment where Val was drilling into the mechanics of how Purchase Orders flow to Purchase Invoices and how payment terms are handled, trying to understand why the process seemed broken and manual.

**How It Unfolded**

The conversation went through extensive back-and-forth about Purchase Orders versus Purchase Invoices, how payment terms carry from one to the other, and why certain steps appeared to require manual intervention that shouldn't be necessary in a properly configured system. Val pressed repeatedly on the logic: if payment terms are set on the Purchase Order, why aren't they flowing through automatically on the payables side the way they do on receivables?

Lev initially explained the workflow as if the manual steps were standard BC behavior — that Purchase Invoices require manual posting, that payment term codes are entered by hand, and that this is how the system works. Val challenged this, pointing out that no modern accounting system should require re-keying information that already exists elsewhere in the system, and that manual entry creates unacceptable error risk.

After extended questioning, Lev acknowledged that the reason the A/P side wasn't behaving like the A/R side was because the wrong tool was being applied. The Installment Payment module (A/R) cannot serve the payables scheduling function. The correct module — Progress Payment from AP Commerce — needs to be installed and configured for the A/P cycle.

Lev had realized this late in the process but hesitated to pivot until Val's drilling made the gap undeniable. By the end of the two-hour session, Lev committed to installing and configuring the Progress Payment add-on.

**Secondary Topics**

The recorded portion also touched on:
- The distinction between Purchase Orders and Purchase Invoices as separate documents in BC
- The posting process (PO → Purchase Invoice → GL/AP entries) and where manual button presses are required
- How payment term codes are custom-created and selected on Purchase Orders
- The general question of separation of duties between procurement (Misha) and accounting for invoice posting

These topics are secondary to the main outcome and were largely part of the diagnostic conversation that led to identifying the add-on mismatch.

## Decisions Made

- **Install and configure the AP Commerce "Progress Payment" add-on for Accounts Payable.** The existing "Installment Payment" add-on (A/R) cannot serve the payables scheduling function. Lev acknowledged this after extended discussion and committed to the pivot. (Decided by Val Levitan, accepted by Lev Rudky)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lev Rudky | Install and configure the AP Commerce "Progress Payment" add-on in Business Central for the Accounts Payable payment scheduling workflow | April 14, 2026 | High | The A/R "Installment Payment" add-on cannot serve A/P needs; this is the correct module for payables scheduling and unblocks proper payment term automation on the purchase side |

## Engineering Signals

### Confirmed Signals

- **ADR: Progress Payment add-on required for A/P scheduling.** Val identified that Lev was using the wrong AP Commerce module (Installment Payment, designed for A/R) for the payables cycle. After a two-hour discussion, Lev confirmed the Progress Payment add-on is the correct tool and committed to installing it. This is a confirmed architectural decision for the BC configuration.

### Suspected Signals

- **Possible REQ:** Payment terms on Purchase Orders should flow through to Purchase Invoices automatically via the Progress Payment module once configured — needs verification after installation. *"Val, once Progress Payment is installed, should we track automated payment term flow as a formal requirement to validate?"*

## Open Questions

- What is the full scope of configuration needed for the Progress Payment add-on? (Lev to determine during installation)
- Will the Progress Payment module integrate cleanly with the existing Installment Payment module on the A/R side, or are there conflicts?
- What testing/validation is needed before going live with Progress Payment?

---
*Processed from Teams transcript on April 8, 2026*
*Source meeting: Call with Lev Rudky*
