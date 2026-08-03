# Meeting Summary — IQ pilot updates discussion
**Date:** July 28, 2026, 10:30 AM – 11:30 AM Eastern (recording 10:33 AM, 41 min 22 sec)
**Duration:** ~41 minutes
**Attendees:** Val Levitan, Andrei Klimovich, Pavel Frolov, Dzmitry Chudzinau
**Raw transcript:** [[Meeting_Transcript_IQ_Pilot_Release_Priorities-July-28-2026]]

## Summary

Val called the meeting because too much detail was arriving in writing for him to follow, and he wanted to talk through the pilot directly. The meeting was held in Russian.

**Release priorities were re-ordered.** Andrei had formalized last week's changes with Val and Juan, written them as short plain-language descriptions any non-engineer can read, and updated the matching requirements in Jira — changing requirements that contradicted the new logic and adding ones that were missing. He shared those descriptions plus the affected requirements with the team the same day. His original priority list had ticket pass-through first. Val and Andrei agreed to move **remote software update to first place**. Val was firm: he will not put a unit on a location if remote update does not work. Pavel had only read up to part 7 of the material, so detailed sequencing waits on him and Dzmitry finishing it.

**Pending transactions stay on the machine.** Pending transactions are held only locally until they finalize with an issued card — nothing is written to a database beforehand. This creates the hard requirement that a remote software update must not wipe them. Pavel confirmed a remote application update leaves the database alone; only a full SD-card reimage erases everything. The team accepted the risk that if a kiosk itself fails, pending transactions not yet in the cloud are lost.

**Ticket printing is unconditional.** Dzmitry walked through the flow to confirm it: the terminal sits between the game machine and the printer, passes the message through, and the ticket always prints — offline, payment hub unreachable, licence expired, or terminal not functional for the operator. The terminal intercepts and stores the data and later shows it to the cashier.

**Delivery split into stages.** Rather than force everything into August 1, Val split priority 1 into 1a (August 1), 1b (August 20) and 1c (end of September). For 1a the accepted mechanism is manual: push the build to each unit, then ask the location to power the terminal off and on so the update installs on next boot. Val said this is fine even at 5 or 20 units — inconvenient, not a problem. 1b would be a real system that tracks every terminal's version and pushes to a chosen terminal, ideally on a location working schedule so updates land outside business hours.

**Where builds are hosted is unresolved.** Pavel builds in GitHub Actions and hands Andrei a direct release link. Val asked why GitHub cannot host the firmware; Pavel said it would mean putting credentials on every terminal, which is insecure. Pavel floated Dropbox as fastest; Val rejected it outright as wrong in principle, saying he would sooner do it over the SIM card. Pavel and Dzmitry will settle it with Sergei.

**InComm is the pilot blocker.** Registering a production location needs master and location licence numbers, which JVL does not have. InComm is working on a workaround. Andrei wants the full path proven end to end — register location, issue cards, receive invoice.

**Process discipline.** Val pushed back on discussing solutions ahead of written requirements, and asked the team not to write requirements ahead of need: changes should rest on requirements and acceptance criteria, and engineers should not act without them. Yesterday's LTE/SIM failure was raised as an example — Pavel found and fixed the cause (the modem reported the wrong error in Val's specific case) and a new build follows today.

The call ended abruptly when Val's connection froze.

## Decisions Made

- **Remote software update becomes priority 1, ahead of ticket pass-through** — Val will not deploy a unit to a location without it. (Decided by Val Levitan, Andrei Klimovich)
- **A remote software update must not overwrite pending transactions held locally** — they only exist on the machine until a card is issued. (Decided by Andrei Klimovich, Pavel Frolov)
- **Accepted risk: pending transactions are lost if a kiosk fails** — they are not stored in the cloud beforehand. (Decided by Andrei Klimovich, Pavel Frolov)
- **Tickets always print automatically in every state** — including offline, payment hub unreachable, or expired licence. (Decided by Andrei Klimovich, Dzmitry Chudzinau)
- **Priority 5 (pending-transaction logic) moves ahead of or alongside priority 2** (Decided by Val Levitan, Andrei Klimovich)
- **Transactions belong to the location, not the terminal** (Decided by Andrei Klimovich)
- **Priority 1 is split into 1a (Aug 1), 1b (Aug 20), 1c (end of September)** — 1a is a manual per-unit push plus a power cycle by the location. (Decided by Val Levitan)
- **Dropbox is rejected for hosting firmware; GitHub credentials on terminals is also rejected** — hosting location still to be decided. (Decided by Val Levitan, Pavel Frolov)
- **The yellow-flag / GenPay interface improvement is deferred to releases after the pilot** (Decided by Andrei Klimovich)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Hand Andrei the new build containing the LTE/SIM fix | July 28, 2026 | High | Build was in progress during the call |
| 2 | Pavel Frolov, Dzmitry Chudzinau | Finish reading Andrei's change descriptions and requirements, then confirm what is achievable by August 1 and what becomes MVP | July 29, 2026 (morning) | High | Pavel had reached only part 7 |
| 3 | Andrei Klimovich | Hold the follow-up call with Pavel and Dzmitry to go through their questions in detail | July 29, 2026, 9:30 AM Eastern | High | Andrei offered 4:30 PM his time |
| 4 | Pavel Frolov, Dzmitry Chudzinau | Decide with Sergei where firmware builds will be hosted for terminal download | TBD | High | Dropbox and GitHub-with-credentials both ruled out |
| 5 | Pavel Frolov | Create the Jira tasks for the agreed changes and assign them to Sergei and Dzmitry | July 29, 2026 | Normal | Always-print tickets goes to Sergei; pending statuses and removing voids also queued |
| 6 | Andrei Klimovich | Write the product-level description of the terminal and update management board, without engineering or architecture | TBD | Normal | Val asked him to keep it minimal and not run ahead |
| 7 | Andrei Klimovich | Keep pressing InComm for the workaround to register the production location without master and location licence numbers | TBD | High | Blocks proving the full path to invoice |

## Open Questions

- Where firmware builds will be hosted for terminals to download — GitHub (credentials on device) and Dropbox both rejected, nothing chosen. Raised by Pavel Frolov and Dzmitry Chudzinau.
- Whether a full SD-card reimage will ever be needed in the field, and how to do it across many locations without losing pending transactions. Raised by Dzmitry Chudzinau; Andrei flagged the cost of physically visiting hundreds of locations.
- How a terminal reboot is triggered for an update to install — for August 1 it is a manual power cycle by the location, with no remote control. Raised by Andrei Klimovich.
- Whether the cashier dashboard should show successful activations (amount and card issued); Andrei says it is specified for the last 24–72 hours per location. Raised by Dzmitry Chudzinau.

## Dispatch Log

---
*Processed from Teams transcript on July 28, 2026, 12:55 PM Eastern*
*Source meeting: IQ pilot updates discussion*
