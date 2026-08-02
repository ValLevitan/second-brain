# Meeting Summary — GACOAM New Software Load: Touchscreen Investigation Check-Back
**Date:** July 15, 2026, 3:01 PM Eastern
**Duration:** ~15 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko

> Afternoon check-back following the 11:01 AM triage. See [[Meeting_Notes_Version_4119_Touchscreen_Loss_Triage-July-15-2026]].

## Summary

This was the follow-up on why touchscreens stop working after the new software load (version 4119), which is blocking the roll-out.

**Findings since the morning call:**

- **USB port-mapping theory tested and dropped.** Pavel's idea was that the new kernel might map USB ports differently than the old version. He asked an AI, which first said it was possible but not something to rely on. He then had the AI compare a machine on the old version against one on the new version; the AI reversed itself — the mapping is identical, no alternative mapping should occur. Theory not confirmed.
- **New difference found: duplicate mouse-emulation devices.** On the new version, each of the two touchscreens gets an extra duplicate device that emulates (or captures) mouse events. They asked whether the second device could interfere with the first. The AI said it cannot and explained why. No reliable code- or script-level cause has been found yet.

**Field log collection (via Philippe):** Philippe keeps installing the software himself, so it's easy for him to capture data. On a machine where he hits the touchscreen fault, he'll boot with two USB sticks and collect the logs, then send them to the team to see the actual USB port distribution and how the scripts ran. Note: logs only work once the machine reaches the init stage — they do **not** run during install mode.

**"Peripheral device fail" install failure.** One cause of failed installs is a "peripheral device fail" message. Philippe explained it appears when the iBoard or counter-board isn't found; both are mandatory for the install to continue. A device that worked before but fails on reinstall points to a suspect: during install the boards are also **flashed** (iBoard, LED controller, counter-board can all be reflashed at that point).

**Installer shows nothing about the background flashing.** Val asked why the installer gives no feedback on the board flashing/validation. Pavel: it runs in the background, deliberately kept off the user-friendly screen; only the installer checksums (disk 1 / disk 2, validated against the values in the joy letters) are shown. Extended logs exist but require plugging a keyboard into the machine. Val called this a weak, lazy decision but said they won't redesign the installer now — the priority is finding the bug faster.

**Key experiment agreed (Pavel's idea):** flash **old** firmware onto the boards on their own controlled machines, install the old software version, then install the new version on top — to test whether the background flashing of all boards during install is what causes the intermittent failures. Val's supporting logic: board flashing takes time, and the machine may have already progressed past a point where it stops reading the boards. Use at least 3 boards (counter, LED, iBoard). For a clean test, pick an old version (17.76 / 17.70, or a 19.x). Estimated ~1 day, maybe 1.5. Pavel recalls the "passport" mapping changed significantly after 17.76.

**Irina's AI analysis:** the AI told her the set-touchscreen-parameters script changed and a new screen was added between versions, with large changes claimed; cabinets were added in the 19.40/41/90 range. She'll send Pavel the AI's write-up of the differences between the two ISOs for his professional review.

## Decisions Made

- **USB port-mapping theory set aside** — AI comparison of old vs. new machine showed identical mapping. (Pavel)
- **Duplicate mouse-emulation device interference ruled out** — per AI analysis. (Pavel)
- **Run the old-firmware-flash experiment** on controlled machines to test the background board-flashing hypothesis. (Pavel, endorsed by Val)
- **Do not redesign the installer screen now** — prioritize root-cause hunt over installer feedback improvements. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel | Run the old-firmware experiment: flash old firmware onto ≥3 boards (counter, LED, iBoard), install an old version (17.76/17.70 or 19.x), then install the new version on top; check if background board flashing causes the install failure | July 16–17, 2026 (~1–1.5 days) | High | Leading root-cause theory for the touchscreen/install failures |
| 2 | Pavel | Clarify and document what the "R2 / P2" items mean more specifically (term garbled in transcript) — from the call with Gennadiy and Philippe | July 15, 2026 | Normal | Follow-up from Gennadiy/Philippe call |
| 3 | Pavel | Verify whether machines can be reached remotely while in installation mode — start a software install on an office machine and test connectivity (Pavel suspects the network isn't up during install) | July 15, 2026 | Normal | Needed to inspect stalled machines / pull logs |
| 4 | Philippe | On a machine exhibiting the touchscreen fault, boot with 2 USB sticks, capture the logs, and send them to the team (USB port distribution + script run) | TBD | High | Real-machine data to find the cause — *external, via Val/team* |
| 5 | Irina | Send Pavel the AI analysis of the differences between the two ISOs (touchscreen scripts, added screen) for his professional review | July 15, 2026 | Normal | Feeds Pavel's investigation |
| 6 | Val | Stay informed of results | Ongoing | Normal | — |

## Open Questions

- Root cause of the touchscreen loss is still unknown — the USB-mapping and duplicate-device theories are both ruled out.
- Does the background firmware flashing of boards during install cause the "peripheral device fail" / touchscreen loss? (experiment pending)
- Is remote connectivity to machines available during install mode? (unverified — Pavel suspects not)

---
*Processed from Teams transcript on July 15, 2026*
*Source meeting: check-back_GACOAM_new_software_load (July 15, 2026, 3:01 PM)*
