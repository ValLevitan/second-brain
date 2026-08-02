---
type: meeting
title: LTE Modem Jira Structure (July 20 2026)
date: 2026-07-20
aliases: [LTE Modem Jira Structure, Modem_JIRA, LTE modem Flex V1000, x86 platform SDK]
source-count: 2
---

# LTE Modem Jira Structure (July 20 2026)

**Date:** July 20, 2026, 6:06–6:22 AM ET (~16 min; Russian)
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]].

Val wants to add **LTE modem support to the Flex (V1000) machines** and set the work up in Jira using the team's documented planning standard. [[raw/Meeting_Notes_LTE_Modem_Jira_Structure-July-20-2026.md]] Dmitri confirmed the standard is written, unchanged, and in GitHub (link posted to the meeting chat); Pavel worked out that the durable way to add modem support is a **git-based build system** (a new x86 platform SDK repository, analog of the existing RK3568 platform SDK) rather than the quick one-off OS rebuild, and proposed the Jira structure — an LTE-modem **capability** under initiative IP-481 Nova Gaming Platform Land-based (under IP-90 Applications). [[raw/Meeting_Transcript_LTE_Modem_Jira_Structure-July-20-2026.md]] Val ended the recording so the transcript itself could serve as the working spec, to be turned into the Jira structure with Pavel at 2:00. This continues the [[wiki/meetings/2026-05-25-gsm-gps-modem-and-event-recorder.md|May-25 GSM/GPS modem thread]] and applies the June-16 JIRA-hierarchy standard.

Substance → [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (July-20 section — LTE modem for the Flex/V1000 devices, x86 platform SDK) and [[wiki/topics/github-release-management-pipeline.md]] (July-20 section — Jira planning structure, git-based build).

## Sources
- [[raw/Meeting_Notes_LTE_Modem_Jira_Structure-July-20-2026.md]]
- [[raw/Meeting_Transcript_LTE_Modem_Jira_Structure-July-20-2026.md]]
