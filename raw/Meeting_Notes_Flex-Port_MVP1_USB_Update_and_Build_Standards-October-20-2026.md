# Meeting Summary — Flex-Port Firmware: MVP1 Release Readiness
**Date:** October 20, 2026, 7:01 AM – 8:09 AM Eastern
**Duration:** ~68 minutes
**Attendees:** Val Levitan, Pavel Frolov, Evgeniy Alekseev, Irina Shishko, Alexey Khamin
**Raw transcript:** [[Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026]]

## Summary

Held in Russian. About 00:31–00:44 of the recording came out as garbled English (transcription error), so that part cannot be read. Val left at about 00:47; the rest was Pavel, Evgeniy, Irina and Alexey.

**What MVP1 needs.** Pavel: for the first release, Flex-Ports in the field must be updatable from a USB stick, so nobody has to reflash them with a programmer. All builds should run through GitHub Actions, because testing depends on it and it gives every developer one build and test setup.

**Who must be able to build.** Val said a non-developer must be able to run the GitHub Actions build. That only works if the repository holds correct architecture, Prose and data contracts. He does not want the company to depend on one developer. He asked for the system to be documented so that Claude, or an outside person, can build the image and the USB update without Evgeniy. He said he will pay for this work. Evgeniy said only a developer can set the build parameters correctly, and that such documentation can take longer than the project itself. Pavel said the build rule is written once and then anyone can start it; a release action can also block a release when tests, Prose or contract checks fail. Pavel said this project already has Prose and data contracts committed; the update and bootloader part is poorly covered.

**Release build dispute.** Evgeniy said nobody had built the release configuration before and that he fixed the build parameters over the weekend; the build now works. Pavel said Alexey had built a release from GitHub and ran the main app on hardware (without the prod loader); the update and bootloader work was left to Evgeniy on purpose. Evgeniy's work sits in branch HFM-663 (version 0.0.84), not yet in main.

**Code quality.** Evgeniy, with a Claude report, said many later changes break multithreading rules. Example: the double beep is called directly between threads; it should be its own thread using events or queues. Pavel said the same issues already exist in Evgeniy Yavorsky's older branch. Pavel asked Evgeniy to write down these rules as a development standard for STM32 projects on FreeRTOS, so Claude review can use them. Evgeniy agreed.

**Scope.** Val: for MVP1, the only goal is to make a new release easy to compile. Evgeniy said this is already done. Val: then check it, put it in MVP1, open 10 locations and start testing. Pavel expects the code-quality rework to go to MVP2 at least. Val: no schedule until the transcript is broken into tasks, standards are checked and Evgeniy estimates each task.

**After Val left.** Evgeniy's app goes into a hard fault in the main loop. To reach the "scan your ticket" screen for testing, his build uses a define that turns off the WS protocol and comments out the loop functions. Alexey built from the branch: the USB update passed on the second try, but after removing the stick the main app beeps all the time. Next step: Alexey builds a second update file with a different version to test the bootloader update. Evgeniy finds the hard fault and moves the beeper to its own thread. Irina asked to keep this in two branches; Evgeniy said it all stays in one branch. Pavel will give Evgeniy access to the Flex IQ (Flex POS) emulator. Remote update is the next task when Dima is back next week.

## Decisions Made

- **For MVP1, only make the new release easy and stable to compile and update by USB; verify it and include it in MVP1, then open 10 locations for testing.** — Rest of the cleanup waits. (Val)
- **Evgeniy writes the STM32 / RTOS coding rules as a development standard that Claude review will use.** — Rules must exist before the code is judged. (Pavel, Evgeniy, agreed by Val)
- **No schedule for Evgeniy's work until the transcript is split into tasks and he estimates each one.** (Val)
- **The update fix, the hard-fault fix and the beeper thread stay in one branch.** — Considered and superseded: two separate branches (Irina). (Evgeniy)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Send the meeting transcript to Pavel | Oct 20, 2026 | Normal | Pavel asked; Val said "sending now" |
| 2 | Pavel Frolov | Break the transcript into tasks and give Evgeniy the task descriptions | TBD | High | Basis for Evgeniy's estimates |
| 3 | Evgeniy Alekseev | Write the STM32 / FreeRTOS best-practice rules as a development standard for Claude review | TBD | Normal | |
| 4 | Alexey Khamin | Build a second update.bin with a different version from branch HFM-663 and test USB update of the main app and the bootloader | TBD | High | MVP1 blocker |
| 5 | Evgeniy Alekseev | Find and fix the hard fault in the main loop and move the beeper to its own thread, in the same branch | TBD | High | Evgeniy asked for a Jira ticket first |
| 6 | Pavel Frolov | Create the Jira ticket for Evgeniy's hard-fault work | TBD | Normal | Val requires a Jira item for every task |
| 7 | Pavel Frolov | Give Evgeniy access to the Flex IQ (Flex POS) emulator | TBD | Normal | |
| 8 | Evgeniy Alekseev | Give time estimates for each task once tasks exist | TBD | Normal | |

## Open Questions

- Who on the team can build and release without Evgeniy? Val wants a non-developer to be able to; Evgeniy disagrees. Not settled.
- Where the hard fault comes from. Raised by Evgeniy.
- Why the app beeps all the time after the USB update. Raised by Alexey.
- What was said between 00:31 and 00:44 (transcript garbled).

## Dispatch Log

---
*Processed from Teams transcript on October 20, 2026*
*Source meeting: Flex-Port Firmware: MVP1 Release Readiness*
