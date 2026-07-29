---
type: meeting
title: IP-106 alignment / scheduling + GA-COAM freezing scope (Mar 10 2026)
date: 2026-03-10
aliases: [IP-106 alignment scheduling, Freezing GA-COAM scope IP-106, Flex Recycler planning Mar-10]
source-count: 2
---

# IP-106 alignment / scheduling + GA-COAM freezing scope (Mar 10 2026)

**Date:** 2026-03-10 (header times 1:01pm + 1:47pm local; recording base `IP-106_alignment_scheduling-20260310`, segment stamps `_090106` + `_094750`).
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/genadi-peari.md|Genadi Peari]] (Russian, garbled).

One meeting in **two segments**: segment 1 (45m11s) is the **freezing discussion**, segment 2 (48m35s) is **JIRA scheduling / product planning**. Val opens seg 2 by saying "part 2 of the meeting is about sketch-glow and planning." [[raw/IP-106_alignment_scheduling-March-10-2026-seg2.md]]

**§12 two-segment evidence:** identical recording base `IP-106_alignment_scheduling-20260310`; seg 1 starts `_090106` (~9:01am, runs 45m to ~9:46) and seg 2 opens `_094750` (~9:47am) — contiguous, one meeting. [[raw/Freezing_GA-COAM-scope_IP-106-March-10-2026-seg1.md]] [[raw/IP-106_alignment_scheduling-March-10-2026-seg2.md]]

- **Freezing (seg 1)** → substance on [[wiki/topics/egm-freezing-investigation.md]]: Val presses the engineers off ad-hoc guessing toward a **controlled, measurable test harness**; agrees to try a stronger/weaker CPU on the same architecture (not the FPS board), to put the "38xx" build back on machines that stopped freezing, and to hand the problem to **Anton Leshkevich** — explaining the *problem*, not dictating the *solution*. Georgia sales noted down from ~50 machines/month to one last month; freezes cluster in bonus rounds (heavy video). [[raw/Freezing_GA-COAM-scope_IP-106-March-10-2026-seg1.md]]
- **Scheduling / product planning (seg 2)** → substance on [[wiki/topics/github-release-management-pipeline.md]] + [[wiki/topics/flexpay-business-architecture-payout-devices.md]]: a walk of the JIRA gantt under value-stream **IP-106** (products IP-760 Compact, IP-955 Flex POS, IP-579 Flex, IP-1014 Flex Cash Dispenser; HFM-401 Flex Pay), Val teaching Genadi to **set the "sketch"/timeline bar so tasks roll up** (HFM-437 cabinet prototype dated 7 Mar → ~6 Apr; Val takes the action to talk to **Mikhail Perelman** on the prototype). Key decision: **move the Flex Cash Recycler / Dispenser onto the ARM RK3568 platform** (write a new HAL in Java rather than C, create a new "Cash Recycler" product IP under IP-744, reuse the FlexPay/FlexPOS codebase), while **FlexPay/FlexPort ship now on the existing V1000 ("Vivian Thousand") platform**; a simple **interface board** (open/close doors, audit, bill-validator pass-through, QR scanner) to be built by **Evgeny Alekseev**. Backend/HAL work routed to Sasha Piratka (=Biratka), Dima Chudinov (~80% of the current FlexPay cash logic), Sergey Tsymanov and Evgeny Kharetski. [[raw/IP-106_alignment_scheduling-March-10-2026-seg2.md]]

§11 header date 2026-03-10 (local header times, not the recording UTC stamp). §15.8 clear — machine/BOM/market economics and JIRA scheduling only, no named-person compensation ($250 ARM-vs-V1000 port cost delta is a component price, allowed). [[raw/IP-106_alignment_scheduling-March-10-2026-seg2.md]]

## Sources
- [[raw/Freezing_GA-COAM-scope_IP-106-March-10-2026-seg1.md]] — segment 1 (freezing).
- [[raw/IP-106_alignment_scheduling-March-10-2026-seg2.md]] — segment 2 (scheduling / product planning).
