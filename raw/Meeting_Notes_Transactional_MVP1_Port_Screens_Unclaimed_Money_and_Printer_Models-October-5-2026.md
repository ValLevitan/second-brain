# Meeting Summary — Transactional MVP1 sync
**Date:** October 5, 2026, 8:01 AM – 8:22 AM Eastern
**Duration:** ~21 minutes
**Attendees:** Andrei Klimovich, Irina Shishko, Dzmitry Chudzinau, Andrei Bosik, Pavel Frolov, Alexey Khamin, Ivan Shpak, Val Levitan
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026]]

## Summary

Held in Russian. Organized by Andrei Klimovich.

**Gap documents.** Dzmitry shared documents on gaps between requirements and mockups. They list decisions he made with Claude where requirements were silent, a full set of tilts, and all negative card-activation cases (servers down, timeouts). These are the base for future autotests. There are no blockers. Andrei Klimovich has not read them yet and will try today.

**Port and transaction screens (capability 141).** There are no mockups for the master/setup screens, so Dzmitry designs them himself. The Flex Port screen already exists and is being refined: which machine is on which port, status, IP addresses. Dzmitry builds the screen for money moving between machine and Flex IQ today. Andrei: these settings belong under the admin role, not the cashier. Use the existing port display in the Recycler (built by Vladimir) as the reference.

**Unclaimed money.** Money that does not reach the machine is kept and passed to the IQ, but the cashier had no place to see it. Andrei said the cashier Records screen already has an unclaimed status. Dzmitry will flag it there. For now nothing is done with this money; the cashier can see it but cannot pay it out ("call JVL"). Andrei also said machine-to-port transactions should already be in Records as deposit and collect types; Dzmitry will check, because Claude told him they are missing.

**Progress.** Unclaimed money is the last core task; Dzmitry expects to finish it today. The rest are small tasks, done in a day or two.

**Remote update** works and is rolled out to a terminal. On one terminal the TITO printer stops printing. It is not clear if the update causes it or the print daemon sleeps after a day. It happened twice, not since last week.

**Georgia.** No reply yet on setting up per the instructions. Andrei will ping Elizabeth today. Over the weekend all SAS commands from machine to port to IQ started going to Grafana, so the team can see what other makers' machines send. The goal: Georgia sets up and tests with JVL machines first, then other manufacturers.

**Printer models.** Alexey: requirements do not list supported printers, and emulators already exist. Pavel: Genadi contacted TransAct about printers with a housing; inside is an Epic 950, priority one. Dzmitry: printers do differ. The longer Flex IQ ticket made printing slower, and the 5-second timeout was too short on one printer; it was raised and printing now works. Pavel: test both Epic 950 and Epic Edge, and support all models, but test only the 950 actively for now. Val: Pavel must write the requirement.

**Print queue.** Alexey: if a ticket is still in the printer, a Flex Port "get ticket" creates the electronic ticket but does not print it. Should there be a queue? Dzmitry: a queue gets complex (for example after a reboot). Val told Andrei Klimovich to pick one option for MVP1 and move the rest to MVP 2 or 3. Andrei: MVP1 goes without a queue; every transaction is in Records and can be printed or reprinted from there. Dzmitry: it already works that way. Self-service Flex Pay printing is not MVP1 (Val).

**Val's direction.** Release the MVP1 machines. MVP 2 writing starts when Andrei is back from vacation. Hold all other questions and focus on testing, to release on October 15 if possible. Next meetings focus on MVP1.

Andrei is away Tuesday to Thursday. The regular meetings go on without him; he will send an invite for a Friday sync. He flies back on the 12th.

## Decisions Made

- **Flex Port and connection settings screens go under the admin role, not the cashier**; the Recycler port display is the reference. (Decided by Andrei Klimovich)
- **Unclaimed money is shown in cashier Records; no action on it for now.** (Decided by Andrei Klimovich, Dzmitry Chudzinau)
- **MVP1 ships without a print queue**; tickets are printed or reprinted from Records. (Decided by Andrei Klimovich, at Val Levitan's request)
- **Epic 950 is the priority printer and the only one tested actively for now; all models stay supported, Epic Edge included.** Pavel first said to test both 950 and Edge, then narrowed it. (Decided by Pavel Frolov)
- **Other questions are held; the team focuses on testing for an October 15 release.** (Decided by Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Read Dzmitry's requirements/mockup gap documents | Oct 5, 2026 | Normal | "I'll try to find an hour today" |
| 2 | Dzmitry Chudzinau | Build the machine-to-Flex IQ money transaction screen (setup mode) | Oct 5, 2026 | Normal | No mockups exist |
| 3 | Dzmitry Chudzinau | Flag unclaimed money in the cashier Records screen | TBD | Normal | |
| 4 | Dzmitry Chudzinau | Check that deposit/collect transaction types are in Records | TBD | Normal | Claude said they are missing |
| 5 | Dzmitry Chudzinau | Finish the unclaimed money core task, then the remaining small tasks | Oct 7, 2026 | High | Core today; rest in 1–2 days |
| 6 | Andrei Klimovich | Ping Elizabeth so Georgia sets up and starts testing | Oct 5, 2026 | High | No reply from Georgia yet |
| 7 | Pavel Frolov | Write the requirement for supported printer models | TBD | Normal | Val's instruction |
| 8 | Andrei Klimovich | Send the invite for the Friday sync | Oct 9, 2026 | Normal | Away Tue–Thu |

## Open Questions

- Does the TITO printer stop because of the remote update or because the print daemon sleeps? (Raised by Dzmitry Chudzinau)

## Dispatch Log


---
*Processed from Teams transcript on October 5, 2026*
*Source meeting: Transactional MVP1 sync*
