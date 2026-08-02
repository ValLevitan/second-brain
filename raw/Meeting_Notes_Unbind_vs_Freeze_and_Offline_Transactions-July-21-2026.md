# Meeting Summary — Call with Andrei Klimovich (Unbind vs Freeze and Offline Transactions)
**Date:** July 21, 2026, 5:15 PM Eastern
**Duration:** ~44 minutes
**Attendees:** Val Levitan, Andrei Klimovich
**Raw transcript:** [[Meeting_Transcript_Unbind_vs_Freeze_and_Offline_Transactions-July-21-2026]]

## Summary

The call was in Russian. It covered two topics: how a unit is detached from a location, and what happens to transactions stored on an offline unit.

**Unbind vs. Freeze.** Andrei described the operations dashboard as forcing a sequence: a unit must be frozen first, and only then can it be taken online or unbound. Val disagreed firmly. He said unbind and freeze are two separate, independent functions and there is no reason to route one through the other. Freeze is an operational, reversible action — stop a unit for a business reason (for example the location did not pay), and it can be reactivated later, possibly automatically once payment arrives. Unbind is a different event: detaching a unit from a location.

Val's core rule: a unit bound to a location is always at that location. If it goes offline and later reconnects at a different location, that is an alarm and possible fraud — it must never silently rebind. A removed unit can never return to its old location either; any reuse always requires a fresh connection at a new location. Val argued this simplicity solves the scaling problems and removes the need for a manual "unbind then rebind" procedure, which he sees as unnecessary labor. On replacement: physically you unplug the old unit, box it, and ship it; a reappearance somewhere else is the trigger to act, not a manual dashboard step.

**Offline / local transactions.** Andrei said that today, per old requirements, an offline unit still receives transactions from MuthaGoose and stores them locally in a pending state; while offline the only completion is a printed ticket, no card is issued. Val insisted a card can only be issued at the moment the button is pressed while online; if offline, print a ticket only, and the ticket closes the transaction. They agreed pending transactions can pile up locally (could be ~10). If the unit is then frozen or decommissioned, those transactions can never finalize, so both agreed they are invalid and should be deleted (hard reset) at some point in the unit's lifecycle.

Val then raised the harder question: to avoid storing anything, the unit must be able to tell MuthaGoose it did not process a transaction. He floated an escrow-style idea — MuthaGoose holds the transaction until IQ validates and accepts it — but said this depends on MuthaGoose's command protocol, which he does not have in front of him. That is a question for Pavel. Val had an America meeting starting and offered to continue later; the conversation resumed in the 7:05 PM call.

## Decisions Made

- **Unbind and Freeze are two separate, independent functions** — no forced freeze-before-unbind sequence. (Val's direction; Andrei agreed.)
- **A unit never automatically rebinds to or returns to a previous location** — reappearance at a different location is an alarm/fraud condition, and reuse requires a fresh connection. (Val's direction.)
- **Offline units issue no cards** — offline transactions can only be completed as printed tickets. (Val; agreed.)
- **Invalid pending transactions on a detached/decommissioned unit should be deleted (hard reset).** (Both agreed.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Continue the discussion with Andrei after the America meeting | July 21, 2026 | Normal | Done — resumed in the 7:05 PM call the same day |
| 2 | Pavel | Confirm whether MuthaGoose's command protocol supports an escrow-style hold | TBD | High | Val does not have the protocol; carried into the 7:05 PM call and the planned Pavel/Dmitry call |

## Open Questions

- Can MuthaGoose hold a transaction in escrow (not deliver it as processed) until IQ validates? Needs Pavel, who knows the MuthaGoose protocol. (Raised by Val.)

## Dispatch Log

---
*Processed from a provided .docx transcript on July 21, 2026.*
*Source meeting: Call with Andrei Klimovich (recording 20260721_131553)*
