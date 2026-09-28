# Meeting Summary — Daily Standup meeting
**Date:** September 23, 2026, 4:48 AM – 5:16 AM Eastern
**Duration:** ~28 minutes
**Attendees:** Pavel Frolov, Irina Shishko, Alexander Biratko, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Dzmitry Chudzinau, Evgeny Kharetski, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026]]

## Summary

Pavel ran the usual round of "who is doing what". Two topics took most of the time: what the kiosk emulator must do next, and a capability that mixes two products.

**Kiosk / terminal emulator (Anton).** Anton extended the bill validator emulator. The old one could not change currency or bill denominations, did not raise a bill-cheating error, and had no fail pause — events fired instantly, so the kiosk skipped steps and its logic broke. He added escrow cases and the disconnect case where a bill is taken but the transaction does not complete. Pavel said the most critical use of the emulator is FlexPort firmware updates, so it can be handed to Evgeny Alekseev. Anton said FlexPort is not supported at all — that device does not exist in the emulator. Pavel first called full FlexPort protocol emulation priority one, then narrowed it: the real priority is a terminal emulator that works against a **real Flex IQ device**, not against another emulator. FlexPay comes second. Anton will merge his branch into main and then clone the work for Flex IQ. Sergey has a local FlexPort emulation from an earlier task (never in a repository) that can be reused.

**Capability split (Irina, Dzmitry, Sergey, Pavel).** CAP-118 mixes FlexPort and FlexPay/Flex IQ work, and the team got stuck: items done for Flex IQ cannot be closed because FlexPay is not ready. Dzmitry repeated his earlier warning not to mix products in one capability. Sergey asked why the two products are not one repository built two ways; Dzmitry said that brings more conflicts now (native library transfer, C++ mode switching) and Pavel recalled the earlier decision that two devices means two repositories. Pavel agreed to split. Irina started the split during the meeting.

**STG certificate problem (Dzmitry).** Dzmitry took capability 152 (card activation) and began installing on STG. The STG and DEV clusters sit in one region and one group, so a terminal registered on DEV collides with STG — the certificate has to be unbound. Production will not have this problem. For STG the choice is either extra functionality to keep unbinding certificates, or changing the thing-name to include the environment. Dzmitry does not like either option and is taking it to Andrei.

**Other reports.** Alexander Biratko created three features under capability 137; FP-1249 (kiosk update) is almost done and installed for checking, plus a logging bug where information was not written; FP-1250 and FP-1251 are also update work. Alexey Khamin moved the pull requests into branch 9 and deleted dead branches; Irina told him to drop the rest and write the autotest, and Alexey raised that how transactional tests are organised needs to be thought through, not improvised. Daniil Stauskiy moved the panel games across and built a screen; he will add a second copy of a game to test switching between games and paid-game limits. Sergey Tsimanov is on metrics and wants to tidy the overlays. Vladimir Samusenko is doing the review GUI for the board; Pavel has no time to review the contract today or tomorrow, so Vladimir will merge and they will correct it later. Ivan Shpak is trying himself as a Claude operator writing autotests. Irina will clean up requirements, add missing acceptance criteria, and close what can be closed. Pavel also spotted new capabilities and requirements created by Andrei that the team has not discussed (REQ-1460 on card programs; a multi-card item accepted but assigned to nobody) and parked them for a later meeting the same day.

## Decisions Made

- **Priority one is a terminal emulator that works with a real Flex IQ device, not with another emulator.** The emulator is needed so firmware update work can be handed over; FlexPay is second in line. (Decided by Pavel Frolov, with Anton Seregin)
- **Anton merges his emulator branch into main, then clones the work for Flex IQ.** The working part is already in a dedicated branch and can be merged. (Decided by Pavel Frolov and Anton Seregin)
- **CAP-118 is split so FlexPay has its own capability, separate from FlexPort / Flex IQ.** Mixing two products in one capability blocked closing finished Flex IQ items. (Decided by Pavel Frolov, after Dzmitry Chudzinau and Irina Shishko pressed for it)
- **Two devices stay in two separate repositories for now.** One shared repository built two ways was considered and rejected for the present — more conflicts, native library transfer and C++ mode switching problems. Possible later once things stabilise. (Decided by Pavel Frolov and Dzmitry Chudzinau; raised by Sergey Tsimanov)
- **Vladimir merges the board GUI documentation without Pavel's review.** Pavel has no time today or tomorrow, it cannot break the build, and mistakes get fixed in a later commit. (Decided by Pavel Frolov and Vladimir Samusenko)
- **Considered and superseded:** full FlexPort communication protocol emulation as priority one — replaced within the same discussion by the real-device Flex IQ terminal emulator.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Anton Seregin | Merge the emulator branch into main, then clone the emulator work for Flex IQ and build the terminal emulator that talks to a real device | TBD | High | Named priority one by Pavel |
| 2 | Irina Shishko | Clone and split CAP-118: FlexPort keeps the FP item Sergey did; 12-03 and 12-04 move to the FlexPay capability | TBD | High | Started during the meeting |
| 3 | Irina Shishko | Send Pavel the comments Claude produced on the four requirements, including the contradictions found in requirement 743 | TBD | Normal | Irina finds them hard to judge herself |
| 4 | Pavel Frolov | Review requirement 743 and say whether the contradictions matter | TBD | Normal | Requested by Irina |
| 5 | Irina Shishko | Clean up requirements — add missing acceptance criteria, close what can be closed, break up the one that is all lumped together | TBD | Normal | |
| 6 | Dzmitry Chudzinau | Settle the STG certificate problem with Andrei — either constant certificate unbinding or an environment-based thing-name | TBD | High | Blocks installing capability 152 on STG |
| 7 | Dzmitry Chudzinau | Tidy up and assign his tasks in the tracker | TBD | Normal | |
| 8 | Alexander Biratko | Finish FP-1249 (kiosk update) and the logging bug, then continue with FP-1250 and FP-1251 | TBD | Normal | FP-1249 already installed on the kiosk for checking |
| 9 | Alexey Khamin | Stop the pull-request cleanup and write the autotest | TBD | High | Irina told him to drop the rest |
| 10 | Daniil Stauskiy | Add a second copy of the game and check game selection, switching and paid-game limits | TBD | Normal | |
| 11 | Vladimir Samusenko | Merge the board review GUI documentation | TBD | Normal | Going ahead without Pavel's review |
| 12 | Evgeny Kharetski | Talk with Pavel about the contract | TBD | Normal | Evgeny said he is coming over |
| 13 | Pavel Frolov | Read the new capabilities and requirements Andrei created (REQ-1460 card programs, the unassigned multi-card item) and discuss them at the later meeting the same day | September 23, 2026 | Normal | Parked from this standup |

## Open Questions

- How the transactional autotests should be organised — Alexey Khamin said it needs thinking through rather than dumping tests anywhere; Irina Shishko agreed.
- Whether FlexPay and Flex IQ can eventually live in one repository built two ways — Sergey Tsimanov raised it, Dzmitry Chudzinau said maybe later once things stabilise.
- Which of the two STG options to take (constant certificate unbinding vs environment in the thing-name) — Dzmitry Chudzinau dislikes both; Pavel Frolov suggested moving the cluster instead.
- What the new items Andrei created actually cover — Pavel Frolov did not recognise them and has not read them yet.

## Dispatch Log

---
*Processed from Teams transcript on September 23, 2026*
*Source meeting: Daily Standup meeting*
