# Meeting Summary — Version 4119 Upgrade Failures and Touchscreen Loss Blocking ARC Roll-out
**Date:** July 15, 2026, 11:01 AM Eastern
**Duration:** ~26 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko

## Summary

Philippe emailed a list of machines where touchscreens stop working after the version 4119 upgrade, blocking the ARC roll-out. He said he has raised this before and been ignored.

Most of the meeting was Val coaching Pavel and Irina on how to triage incoming problems. Val's point: when a complaint arrives, Pavel and Irina must "triage" it themselves first — form theories about root cause, decide what to test and how to isolate — before handing it to a specialist. Delegating without analysis just moves the problem. The earliest moment is the cheapest moment to solve it; techs arrive at 9:00 and the clock is ticking.

What was done so far: Irina saw Philippe's email first, brought it to Pavel, and they judged it urgent. First theory was touchscreen firmware version — a similar issue years ago was fixed when Gennadiy had someone reflash problem touchscreens via laptop. Dima was tasked to collect firmware versions on the listed machines. Result: firmware versions (recorded in each machine's passport) match other working machines, so the firmware theory is likely wrong. Reproduction was attempted on three machines and failed.

Second theory (Pavel): touchscreens on some machines may be plugged into the wrong USB port; old software tolerated it, but the new version may have changed port detection, breaking the touchscreen-to-display mapping. Pavel knows how the mapping works and doesn't yet see how new software would affect it. He suggested feeding the mapping script to an AI and asking what changed between the old and new Linux versions.

Val pushed back on the reproduce-first method: physically reproducing on machines is labor- and time-consuming. Talk through the theories first, check the mapping in the software itself, and consult people who worked on this area. He also noted firmware isn't delivered through the software/ISO package — updating touchscreen firmware requires a laptop at the machine; no capability exists today to flash firmware during software install (Pavel: possibly an easy feature now, unexplored).

## Decisions Made

- **Firmware-version theory set aside** — passport data shows the same firmware as working machines. (Pavel, Irina)
- **Issue treated as urgent**, ahead of test/dev work. (Pavel, Irina)
- **Process change: Pavel and Irina must triage and theorize root cause themselves before delegating**, and engage earlier when complaints first surface. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel + Irina | Stop trial-and-error reproduction; develop and discuss root-cause theories (incl. with others who worked on this) before the follow-up call | July 15, 2026, ~12:30 PM ET | High | Blocking ARC roll-out |
| 2 | Pavel | Analyze the touchscreen mapping in the software itself — e.g., give the mapping script to AI and ask what changed between old and new Linux versions | July 15, 2026 | High | Leading remaining theory (USB port detect / mapping) |
| 3 | Val | Rejoin the call at "9:00" (in ~1.5 hours) to review theories | July 15, 2026 | Normal | — |

## Open Questions

- Actual root cause of touchscreen loss on 4119 — firmware ruled out, mapping/USB theory unproven, reproduction failed on 3 machines.
- Whether touchscreen firmware could be flashed automatically during software install (no such capability today; Pavel thinks it may now be feasible).

---
*Processed from Teams transcript on July 15, 2026*
*Source meeting: Version 4119 Upgrade Failures and Touchscreen Loss Blocking ARC Roll-out (July 15, 2026, 11:01 AM)*