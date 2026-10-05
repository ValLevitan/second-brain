# Meeting Summary — Dev_environments
**Date:** September 29, 2026, 10:06 AM – 10:20 AM Eastern
**Duration:** About 14 minutes
**Segment:** 1 of 3
**Attendees:** Val Levitan (organizer), Pavel Frolov, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_Dev_Environments_RK3568_SDK_and_Pavel_Bottleneck-September-29-2026]]

Held in Russian. Next segments: [[Meeting_Notes_Dev_Environments_AMD_SDK_Spike_and_RK3576_Plan-September-29-2026]], [[Meeting_Notes_Dev_Environments_AI_PM_Direction_Check-September-29-2026]].

## Summary

**The problem.** Val said the company now has two development environments to support: one for RK (Rockchip) and one for the AMD ecosystem. Both must be easy for developers to use. His concern is the bottleneck around Pavel. Irina added: Pavel is the only source of hardware knowledge. Val said this is dangerous and the company cannot work this way.

**The RK3568 SDK today.** Pavel said that at first nobody else could join the RK3568 work because of missing knowledge. But the work was done with Claude and was well documented. Other developers already worked in the platform SDK RK3568 repository: Dima (automatic updates) and Sasha. Dima's last work cleaned the repo so it is universal. It was first made for FlexPay; now it can build both FlexPay and a machine on RK3568 (though the processor is weak for a machine).

**AMD.** The AMD side is built differently. Pavel suggested making both SDKs as close as possible, so an application on top (games, kiosks, other uses) can move between platforms. A NOVA game started on AMD should then move to the other platform easily, ideally with no extra work.

**Documentation and capabilities.** Val asked if the RK repo has correct prose, ADRs and capabilities in Jira. Pavel said capabilities were created from some point on, but the work began without them, so some may be missing. He checked during the meeting: the prose is current, files are fresh, 13 prose sections, in the new structure (made by Andrei).

**Testing.** Val asked if the dev environment needs testing like other work. Pavel said it is tested through the integration repository inside other tasks. The one useful direct test he sees: check that the built image boots in an emulator. Anything more is logic of a specific device.

**Next idea.** Val said that if no extra testing is needed and the environment mostly works, the repo only needs to match today's standard, which should be easy with Claude. He then asked if the RK environment could be copied as a skeleton for the AMD processor. Pavel said yes, it can be built on the same principles with Claude (continued in Segment 2).

## Decisions Made

No formal decisions recorded in this segment.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|

None in this segment (Pavel checked the RK3568 prose during the meeting and found it current).

## Open Questions

- Which capabilities are missing for the RK3568 SDK, since the work began before capabilities were used? (Pavel)
- Pavel and Irina mentioned a reply from Alexeev about 8 MB SDRAM not working; not discussed further.

## Dispatch Log

---
*Processed from Teams transcript on September 29, 2026 (meeting-watcher)*
*Source meeting: Dev_environments, Segment 1 of 3*
