# Meeting Summary — Dev_environments
**Date:** September 29, 2026, 10:20 AM – 10:31 AM Eastern
**Duration:** About 11 minutes
**Segment:** 2 of 3
**Attendees:** Val Levitan (organizer), Pavel Frolov, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_Dev_Environments_AMD_SDK_Spike_and_RK3576_Plan-September-29-2026]]

Held in Russian. Previous segment: [[Meeting_Notes_Dev_Environments_RK3568_SDK_and_Pavel_Bottleneck-September-29-2026]]. Next: [[Meeting_Notes_Dev_Environments_AI_PM_Direction_Check-September-29-2026]].

## Summary

**AMD on the same base.** Pavel said the AMD environment can now be rebuilt from the same repository approach, on Debian. He did not know why the old choice was made 25 years ago. Val said this does not matter and the team will not look into it. Val said this was good news.

**RK3576.** Pavel raised the RK3576 processor. It now lives as a branch in the RK3568 repo, and he found differences. It can stay in one repo: then new tools, libraries or network filters added once work for both 3568 and 3576. The 3576 cannot boot from an SD card, so the first load must always be flashed by cable from a computer. Otherwise the repo is about 95% the same. Val wants to standardize the two development environments first, then develop further. RK and AMD stay separate repositories.

**The plan.** Pavel proposed a spike: move the SDK into a new repository and adapt it for AMD processors. The bootloader and installer will be completely different; the root file system and kernel build are the same, maybe even the same kernel version. An x86 emulator exists and is good; the RK3568 emulator is weaker. Val noted RK will move faster and more aggressively.

**MVP 1 scope** (Pavel): kernel build, root file system build, installer build, bootloader build. A boot splash screen is likely MVP 2.

**Owner and time.** Pavel said only he can take it now, and he agreed to take it. Val guessed about 2 weeks; Pavel expects 80% in the first week, then additions. Val gave 10 days and will book a follow-up meeting on the 8th (October 8).

## Decisions Made

- **Standardize the two development environments first, then develop them further** (RK3576 comes after). (Decided by Val)
- **RK and AMD stay in separate repositories.** (Pavel; not disputed)
- **Pavel does a spike to move the SDK into a new repository and adapt it for AMD; MVP 1 = kernel, root file system, installer, bootloader.** (Pavel proposed, Val agreed)
- **Deadline 10 days; follow-up meeting on October 8.** (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Spike: move the SDK into a new repository and adapt it for AMD (kernel, root file system, installer, bootloader) | Oct 8, 2026 | High | ~80% expected in the first week |
| 2 | Val Levitan | Book the follow-up meeting on the dev environments | Oct 8, 2026 | Normal | "8 числа я назначу митинг" |

## Open Questions

- Keep RK3576 in the RK3568 repo or in its own repo? Pavel said "need to think how best." (Pavel)
- Boot splash screen for the machine: likely MVP 2, not decided. (Pavel)

## Dispatch Log

---
*Processed from Teams transcript on September 29, 2026 (meeting-watcher)*
*Source meeting: Dev_environments, Segment 2 of 3*
