# Meeting Summary — Daily Standup meeting
**Date:** October 1, 2026, 4:48 AM – 5:26 AM Eastern
**Duration:** About 38 minutes
**Attendees:** Pavel Frolov (organizer), Irina Shishko, Alexander Biratko, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Dzmitry Chudzinau, Dmitri Kovalchuk, Evgeny Kharetski, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026]]

Held in Russian. Previous standup: [[Meeting_Notes_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026]].

## Summary

**SAS / no-SAS mode for FlexPort.** Pavel said each port must be told which mode it runs in: SAS, or no-SAS (the old bill acceptor emulation). Dzmitry asked who decides this, and said it is not in the MVP1 requirements and is being added at the end of the release. Pavel said it is a small task. For now the switch goes on the Flex IQ setup screen, in the tab of connected FlexPorts: one toggle per device. This lets one location run some machines on SAS and some not. A server-side switch can come later (MVP2 or 3), when the server shows port status. Dzmitry asked what happens if the mode changes during a transaction. Pavel said the port only switches when it has no transaction and no money on it. Pavel named the modes "SAS AFT" and "no SAS" (a plain SAS mode without AFT may come later). Dzmitry will add the flag. It goes with the PIN-code capability, sent at terminal registration (Dzmitry or Sergey).

**Feature status rules.** Sergey got an email that his closed feature had unfinished work. Vladimir had created a story under FP-85 after Sergey closed it. This started a debate on statuses. Dzmitry said the team agreed two meetings ago that developers set Completed, not Closed or Request Review. Dmitri Kovalchuk said Request Review was only meant for Lena's design team. Irina said a problem found during development is a Story, not a Bug, because the developer did not finish something. The final agreement: **Completed stays the developer's last step. If a problem is found, the feature goes back from Completed to To Do** (not In Progress, since nobody knows when a developer will pick it up). Dmitri Kovalchuk will add that transition. Irina added that each feature must link to the requirements it covers, so a failed acceptance criterion points to the right feature.

**Printer library on FlexPay.** Alexander moved the LED/IO board to a service (Evgeny says it works on his side) and switched the libraries and services to pull from GitHub. The latest printer library did not print vouchers on the Gen 5 printer on FlexPay. The cause was a change Vladimir made for the Epic 950 printer. Alexander's Claude made a fix and it prints now, but it needs a check that nothing broke for the other printer. Sergey is also building a new voucher template, which will be tested on all printers. This work is under capability 136.

**Alexander's next work.** His main FlexPay tasks are ending. Pavel asked him to go through all open capabilities and close the ones that are done. Alexander already has a comparison of Flex IQ and FlexPay capabilities.

**Emulator check (Anton).** Anton closed FP-60 and moved three kiosk bugs to capability 140. He asked how to prove the Flex IQ emulator behaves like the real device (same logs, no missing or extra events). Pavel said the goal is not a full match; differences are fixed when found. Anton said Claude proposed a register of which device model and firmware each emulator version was checked against. Pavel said one emulator instance per device type is enough for now, so people can start using it soon. Anton will try to finish today. Pavel's next priority for him: have someone else (Alexey, Vladimir or Irina) bring up his environment in a different setup, for example with a real Flex IQ.

**Game conversion (Daniil).** Daniil has converted almost everything to NOVA. Pavel said adding the dock panel and game icons can be a separate story under the same feature. Daniil doubts the selection-screen converter will fit future packages, so he asked if it is worth committing. Pavel said to ask Igor, and to test the converter on another game package with a very different selection screen.

**Dzmitry.** Closed capability 152 (card activation) and put a new build on Alexey's terminal. Finishing 175 (records), done in part. Next: capability 241, information about the machine connected to the port and forwarding of command logs.

**Statistics not working (Evgeny).** Evgeny is on LGS 12.19, the IO board, LEDs and counter board. Anton adds service changes each day that Evgeny's Claude says are still needed. Sending statistics does not work now. Plan: connect to localhost over the internet and over the local network, and check that all messages arrive.

**Support phone on the voucher (Sergey).** Sergey finished leftover screen work. The new voucher has a support phone field. He asked whether to use the existing contact phone from location setup or add a new field. Pavel said the contact phone is the right one. Dzmitry noted the server side is still stubbed. Sergey will forward the existing contact phone.

**Others.** Alexey: autotests and PR reviews; repo structure changes still needed. Irina: autotests, then moving capabilities to FlexPay. Ivan: autotests with Evgeny. Vladimir: finished a test task and is on a location task. Dmitri Kovalchuk: due dates slipped on some tasks, and some are overdue.

## Decisions Made

- **SAS / no-SAS mode is set per device on the Flex IQ setup screen, not on the server, for now** — fastest path; server control can come in MVP2 or 3. (Pavel Frolov; accepted by Dzmitry Chudzinau and Sergey Tsimanov)
- **A port switches mode only when it has no transaction and no money on it.** (Pavel Frolov)
- **Use the existing location contact phone as the support phone on the voucher.** (Pavel Frolov)
- **Completed is the developer's last status; a feature with a found problem goes from Completed back to To Do.** Problems found during development are logged as Stories, not Bugs. (Pavel Frolov, Irina Shishko; Dmitri Kovalchuk to configure)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dzmitry Chudzinau | Add the SAS AFT / no-SAS mode flag, sent with the PIN code at terminal registration | TBD | Normal | Dzmitry or Sergey, with the PIN-code capability |
| 2 | Dmitri Kovalchuk | Add the Completed → To Do transition to the Jira workflow | TBD | Normal | "Хорошо, я добавлю" |
| 3 | Alexander Biratko | Go through all open capabilities and close the ones that are done | TBD | Normal | Pavel's main task for him |
| 4 | [Unassigned — needs clarification] | Re-check the printer library fix so the Epic 950 change and Gen 5 voucher printing both work | TBD | Normal | Alexander asked for a re-check; nobody took it |
| 5 | Anton Seregin | Finish the Flex IQ emulator verification work | Oct 1, 2026 | Normal | "попробуй за сегодня" |
| 6 | Anton Seregin | Have Alexey, Vladimir or Irina bring up his environment in a different setup (e.g. with a real Flex IQ) | TBD | Normal | Pavel's next priority |
| 7 | Daniil Stauskiy | Ask Igor whether to commit the selection-screen converter; test it on a different game package | TBD | Low | |
| 8 | Evgeny Kharetski | Find why statistics are not sent: test over internet and local network | TBD | High | Stats sending broken now |
| 9 | Sergey Tsimanov | Forward the location contact phone as the voucher support phone | TBD | Normal | |

## Open Questions

- Whether MVP1 needs to ship in both SAS and no-SAS modes. Dzmitry asked; Pavel answered "no", and the mode toggle is still being added. Not fully clear. (Dzmitry Chudzinau)
- What other parameters a device needs at start-up. Pavel raised it and left Wi-Fi for MVP2. (Pavel Frolov)
- What a non-SAS mode beyond "no SAS" should be called. (Dzmitry Chudzinau)

## Dispatch Log

---
*Processed from Teams transcript on October 1, 2026 (meeting-watcher)*
*Source meeting: Daily Standup meeting*
