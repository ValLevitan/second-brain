# Meeting Summary — Alignment by the coffee machine
**Date:** November 23, 2026, ~11:46 AM – ~12:18 PM Eastern (recording)
**Duration:** ~32 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko
**Language:** Russian
**Source:** Teams meeting (Val organizer)
**Raw transcript:** [[Meeting_Transcript_Pavel_Irina_LTE_Modem_Build_Rev_2_Boards_and_WiFi_Updates-November-23-2026]]

## Summary

**Team mood.** Pavel: the mood is positive, people are inspired. Sasha took the work given to him gladly and moves fast. Irina: Sasha and Igor do not hand work to AI blindly; they think it through and get a planned result. Others should learn from them. Her worry is how the rest will keep up.

**Cell modems on machines.** Val asked when the modems will work reliably. Pavel: no direct answer. The modems come from internet sellers, with different firmware and different carrier locks, so almost each modem needs its own tuning. The test tool Val asked for last week is released, with a description. After that, it depends on which modems we buy and where.

**Georgia build with modem.** Val asked for one release with the modem and the RIS change for Georgia. Irina: today she gave a build with all fixes and the modem to test; build number 4377. Ivan checked it this morning and a production build was made. Elizabeth and Sebastian must take it and test it on different modems, following the steps in the documentation, before it goes to the lab.

**First transactional installation.** Val asked for the date. Pavel: Andrei did not say. Irina: on Friday or Saturday he said he was waiting for answers (the transcript says Intralot; Val said InComm). No date was given.

**South Dakota.** GLI finished testing the first build today. They have not answered two points. The rest is fixed; Efim also adjusted the math, and Irina is not sure it is in the build. Ivan goes back to the South Dakota build tomorrow to recheck all remarks.

**Next priority: transactional version (MVP 2.1 / 2.2) with Wi-Fi and updates.** Alexeev answered today: he finished his part, so the regular firmware also updates the Wi-Fi module. The team cannot test this in Minsk, only on the new boards in Georgia. Pavel asked Alexeev to test it on his side; Alexeev said he will check tonight and write back. Then the full chain exists: an update flashes both the Wi-Fi module and the port.

**How a Flex-Port is updated.** Two ways: a USB stick with the firmware, or over the internet — the firmware goes to Flex IQ and Flex IQ passes the same file to the selected ports. Delivery from the server to Flex IQ has an autotest and it passes. The port update itself is not covered by autotests; only the protocol between Flex IQ and the port is. Pavel: there is no good STM32 emulator, so this test runs on real hardware.

**Revision 2 boards and the multiplexer.** Val: revision 1 = 3 working boards; revision 2 = 20 boards; revision 3 is what Alexeev makes now and takes 10–15 days after ordering. Pavel: software cannot fix revision 2; the program already talks to the printer port directly. Alexeev proposed a hardware fix (remove one chip, bridge two pins). Andrei and Sebastian tried it once and it did not work; Pavel does not know if they finished. Removing the multiplexer fully is probably too hard for them. Val: do not dig; pack the 20 boards and send them back to Alexeev to fix. About 5 working days round trip, so back about Tuesday next week. Pavel offered a half-hour experiment first; Val said no.

**Updates must be reliable.** Val: for version 2 of the transactional equipment the two most important things are remote updates and Wi-Fi setup, and he does not feel they are solid. Pavel: there is a problem. Over the weekend Anton Seregin wrote autotests and the update that does not use the stick or ST-Link did not work. Alexey Khamin looks first, then Simonov joins. Pavel thinks it is not serious. Irina: today it does not work like clockwork; it must be brought there. Sergey Simonov made the last update; Alexeev started the work.

**Wi-Fi setup as built.** Ports can join an existing access point, or Flex IQ becomes the access point and ports connect to it directly. Network name and password are set per location on the cloud server. The technician does not need them: he makes a QR code on his phone from the dashboard, or from the Flex IQ engineering menu, and shows it to each port.

## Decisions Made

- **Send the 20 revision 2 boards back to Alexeev to fix; no more experiments on site.** — The proposed pin fix did not work and the full fix is too hard for the field team. (Decided by Val; Pavel agreed). Note: the call with Genadi later the same day reopened this — see [[Meeting_Notes_Genadi_Rev_2_Boards_Monitor_Controller_Sourcing_and_Data_Contracts-November-23-2026]].
- **Georgia build 4377 (fixes + modem) is tested by Elizabeth and Sebastian on different modems before it goes to the lab.** (Irina, Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Elizabeth Palomino, Sebastian Cortes | Test build 4377 on different modems, following the documented steps | TBD | High | Before release to the lab |
| 2 | Alexeev [Needs Val's confirmation — likely Evgeniy Alekseev] | Test the Wi-Fi module firmware update on his side and write back | Nov 23, 2026 (evening) | High | Team cannot test it in Minsk |
| 3 | Ivan | Recheck all GLI remarks on the South Dakota build | Nov 24, 2026 | High | |
| 4 | Alexey Khamin, then Sergey Simonov | Find why the update without stick or ST-Link failed in Anton Seregin's autotest | TBD | High | Pavel: "probably" Khamin first |
| 5 | [Unassigned — needs clarification] | Pack and ship the 20 revision 2 boards to Alexeev | Nov 23, 2026 | High | Val: "send them now"; no name given |

## Open Questions

- When is the first transactional system installed? No date; Andrei waits for answers. (Val)
- Did Andrei and Sebastian finish the pin-fix experiment on a revision 2 board? (Pavel)
- Is Efim's math change in the South Dakota build? (Irina)
- GLI has not answered two points on South Dakota. (Irina)

## Dispatch Log

---
*Processed from Teams transcript on November 23, 2026, ~2:15 PM Eastern*
*Source meeting: Alignment by the coffee machine*
