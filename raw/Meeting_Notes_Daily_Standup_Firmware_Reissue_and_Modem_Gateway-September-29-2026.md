# Meeting Summary — Daily Standup meeting
**Date:** September 29, 2026, 4:49 AM – 5:14 AM Eastern
**Duration:** About 25 minutes
**Attendees:** Pavel Frolov (chair, organizer), Alexander Biratko, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Dzmitry Chudzinau, Dmitri Kovalchuk, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026]]

## Summary

Held in Russian. The speech recognition is poor in places, so some task numbers below are uncertain.

**Re-release instead of a hack.** Pavel said Val ruled yesterday: no hack. The fix will go out as a **re-release**, as fast as possible, but likely not before tomorrow. Irina said only this one commit must go into the release. Evgeny's fix is almost ready (version 4.50.2). A library (broadcast) was also changed; Pavel said they will declare it as a connectivity change. Evgeny will tell Ivan when the build is ready. Ivan keeps his current build on the stand for autotests.

**Version table moved to main.** Evgeny moved the table that maps release versions to data centers and games into the main branch. The reason: Ivan's stand ran 4.50.1 while the team was on 4.60, and two data centers cannot look at the same game version. Now the table is always in main.

**Modem as default gateway.** Last night Pavel and others found that when the modem is on, it becomes the default gateway. Evgeny said the progressive link keeps dropping and reconnecting, so that network cannot be trusted for long connections. Pavel added that broadcast packets go to the modem first and create shadow traffic. He will try, on a machine, to send the progressive controller ports only to the internal network. Terminals have the same issue; it must be fixed properly later. This must be kept in mind for all transactional products.

**Flex IQ priority.** Anton planned a FlexPort feature. Pavel said the priority is the **Flex IQ emulator, and above all the FlexPort firmware update through Flex IQ**: the file transfer protocol and the commands to start the update. A very simple FlexPort emulation is optional. Anton will work on this today; Pavel will create a feature for it.

**EGM emulator.** Alexey cannot write some test scenarios because the EGM emulator cannot delay or hang. Pavel told him to add this himself, as a separate tab or panel of test cases (for example, "answer the next long poll 72 with a delay").

**Individual status.**
- **Alexander Biratko** — capability 134, three features, nearly done. Last step is a check on a real server, which does not support FlexPay yet. GSM task not started.
- **Alexey Khamin** — autotests for TINT-16 and TINT-79; adding scenarios for filed bugs. Plans to close two bug tasks and item 601 today. Advised Ivan to let Claude look at his machine-collection tests.
- **Anton Seregin** — rechecking stories Claude created by plan; moving the accumulator to Flex IQ; today the Flex IQ firmware update work.
- **Daniil Stauskiy** — game select feature (FAR-1483/1484). No select-screen assets yet, so it uses stubs (names only). Pavel agreed to go ahead with stubs.
- **Dzmitry Chudzinau** — closed two CAPs; finishing 152 on test stands, then a real device. Next: 176.
- **Evgeny Kharetski** — LGS-219 and LGS-217, plus new tasks for a service integration. Pavel made him a cable.
- **Irina Shishko** — learning how the autotests are set up and run.
- **Ivan Shpak** — main task is the modem fix: rebuild and verify. Wrote the instruction (PDF) yesterday; will send it by email.
- **Sergey Tsimanov** — finishing capability 156 (implementation done, testing on stand). Cannot flash with the programmer yet (no USB on the board); looking for a workaround. Next: capability 158 (zero balance); about half may already be done.
- **Vladimir Samusenko** — port tasks done. Starting autotests with TINT-41. Dmitri Kovalchuk gave him access to the integration repository.
- **Dmitri Kovalchuk** — the team is closing tasks; there is progress.

## Decisions Made

- **Fix ships as a re-release, not a hack; only this commit goes in.** — Val's ruling from yesterday, reported by Pavel; Irina set the one-commit rule. (Decided by Val Levitan, Irina Shishko)
- **Flex IQ emulator and FlexPort firmware update through Flex IQ come first; FlexPort emulation is secondary.** (Decided by Pavel Frolov)
- **Game select screen goes ahead with stubs.** (Decided by Pavel Frolov)
- **Alexey adds delay/hang test cases to the EGM emulator himself.** (Decided by Pavel Frolov)
- **Ivan sends the instruction by email.** (Decided by Irina Shishko)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Evgeny Kharetski | Finish the fix (4.50.2) and tell Ivan when the build is ready | Sep 29, 2026 | High | Re-release |
| 2 | Ivan Shpak | Rebuild and verify the modem fix | TBD | High | Re-release not before Sep 30 |
| 3 | Ivan Shpak | Send the instruction (PDF) by email | Sep 29, 2026 | Normal | Before the later meeting |
| 4 | Pavel Frolov | Test sending progressive controller ports only to the internal network | TBD | Normal | Modem default gateway |
| 5 | Pavel Frolov | Create a feature for checking FlexPort firmware transfer and control via Flex IQ | Sep 29, 2026 | Normal | |
| 6 | Anton Seregin | Work on FlexPort firmware update through Flex IQ | Sep 29, 2026 | High | |
| 7 | Alexey Khamin | Add delay/hang test cases to the EGM emulator | TBD | Normal | |
| 8 | Alexey Khamin | Close two bug tasks and item 601 | Sep 29, 2026 | Normal | |
| 9 | Sergey Tsimanov | Finish capability 156, then start 158 | Sep 29, 2026 | Normal | |
| 10 | Vladimir Samusenko | Start autotests with TINT-41 | TBD | Normal | |

## Open Questions

- How to stop broadcast traffic going to the modem, on machines and terminals (Pavel).
- Exact date of the re-release (Pavel: not before tomorrow).

## Dispatch Log

---
*Processed from Teams transcript on September 29, 2026*
*Source meeting: Daily Standup meeting*
