# Meeting Summary — Daily Standup meeting
**Date:** November 4, 2026, 6:15 AM – 7:20 AM Eastern
**Duration:** ~55 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dzmitry Chudzinau, Evgeny Kharetski, Igor Metelski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko, Dmitri Kovalchuk
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026]]

## Summary

Held in Russian. Audio is poor in places. Unclear names, numbers and words are marked "heard".

**Release builds were not handed to Toronto.** Pavel asked whether anyone sent the Flex IQ release to Filipp and Elizabeth. Nobody had. Irina had sent Pavel the Flex-Port builds for that purpose. Agreed: Alexey writes one email to Toronto with the links to the released Flex IQ and Flex-Port builds and duplicates it in the release chat. Pavel: release links must go into the chat where release versions are posted, not through side channels. Pavel will also go through every Jira project and mark the "MVP1 Transactional" release.

**Where release notes and artifacts live.** Irina wants one place that records what was released and which IQ build goes with which port build. Pavel: releases are GitHub tags with descriptions; could be mirrored to Confluence. Dzmitry: the server already has the firmware store with download links; a document with what each version contains can be generated into it; a Claude step could produce the review. Pavel: GitHub also keeps the tagged release builds; the S3 build number links back to the build. For now: give download links through the dashboard GUI for Flex IQ; Flex-Port appears there only in the next version.

**Old HFM feature closed.** Alexander closed about 10 of 20 tasks moved to him. HFM-354 (negative transactional scenarios, already done on Flex IQ and Flex Pay) and HFM-460 are obsolete; Pavel closed them. The old feature can be closed; the two remaining tasks move under a capability. Alexander still has Flex Pay update tasks (Sergey's server work) to take. He asked whether the Recycler starts and under which MVP. Pavel: clarify with the business whether Flex Pay MVP 3 or a Recycler MVP comes first; the Recycler is for Texas, not Georgia (cash out is not allowed there; the InComm card route is not approved). Libraries exist for x86 and ARM.

**Dakota handpay printer bug (Evgeny).** If the key is turned while the printer re-aligns its markers and Ivan powers the machine off, after power-up the SAS host asks to print the ticket and the printer prints two handpay tickets in audit-ticket orientation. Nothing to fix on the JVL side; question is whether to fix at all. Evgeny created a group chat on it. He is also building a new SAS tool (remote control, Claude-driven) for autotests; it will go to GitHub as a repository. Pavel: investigation can run under service ticket CS-492 (heard), but any change needs a task; spikes need a capability, which probably does not exist yet. Evgeny is also reviewing a 48-minute video for Friday.

**NAD 2 product code (Igor).** Igor made HTML pages describing all GCM3 games, finished the bonus description from Evgeny's competitor videos, added transitions to his Claude tool, and will profile locally on NAD 2 (GCM3 had performance problems; NAD 2 adds a second full-HD monitor). Designers plan to release NAD 2 in December. Igor: NAD 2 needs its own product code because it is multi-product (Jackpot Rush, Phil (heard), lines, match, progressions) and Georgia settings may differ from Nebraska. Pavel: the server and data centre need tasks to support NAD 2 as a multi-product; longer term the framework should not carry jurisdiction checks. Igor: the framework has many "if Georgia" branches that will stop matching a new product code. Pavel: that is a behaviour flag, not a jurisdiction flag; think about the architecture later. Igor to sync with the designers on dates. Igor can close the Conversion task and the old performance bug; the QR autoplay crash task stays open (extra logging added, not reproduced).

**Jira dashboard filter.** Dzmitry's observability tasks (IP-435) do not show on the Kanban dashboard. Dmitri Kovalchuk will add the missing projects (CMS-H, CMS-FE, SMS-C, heard).

**Echo paused.** Pavel: no known bill acceptor for Echo reads ticket barcodes; without one Echo is not needed. Unless Genadi finds one, nobody will take Echo. Ivan stops Echo work and stays on the printer problems.

**MVP 2.** Pavel: MVP 2 is discussed today at 4:00 with Andrei. Main direction is Wi-Fi for Flex-Ports and Flex IQ. Ports without Wi-Fi modules need modules installed; Flex IQ needs antennas (old media boxes have some). Acceptance criteria on existing MVP 2 features are probably not reviewed; Irina will check as she goes.

**Other updates.** Alexey: hardware tests continue; Flex-Port flashed with the release version; an instruction is needed for installing on factory firmware via update.bin. Anton Leshkevich: reviewed the first version of the new Nebraska game, sends comments today; editor prototype should be working by end of week; his boards arrived, may need extra wires. Daniil: pull request open for the Rust sound repository; NC-1 can be closed (Pavel agreed); he has no tasks; Pavel and Alexander will find him something tomorrow. Anton Seregin: CF-8 and CF-9 done (Wi-Fi settings UI, QR code page, mockups); scanner test page TINT-102 (heard) showed a dense QR may not scan, so CF-10 should get a zoom-out button. Dzmitry: host and server reporting (server done, host in progress). Irina: finishing MVP 2 features and tests; 3–4 tests wait on an IQ change; Alexey will create a task for someone. Ivan: found one more bug after Evgeny's fix; needs SAS so one-bit responses can be stopped to reproduce the field case; Evgeny needs SAS access too. Irina will check Sergey's server-side work so Dzmitry can release; Sergey: passport deploys too if approved. Sergey: QR for ports; port update tasks closed; two MVP 2 tasks done, dates set. Vladimir: autotests; drafts of LGS documentation; got repository access. Dmitri Kovalchuk: Alexander now has the most tasks without dates; the agent now writes to 10 people.

## Decisions Made

- **Alexey emails Toronto the Flex IQ and Flex-Port release links and duplicates them in the release chat.** (Irina, Pavel, Alexey)
- **HFM-354 and HFM-460 closed as obsolete; the old HFM feature is closed.** (Pavel, Alexander, Dzmitry)
- **Download links go through the dashboard GUI for now; Flex-Port appears there in the next version.** (Pavel, Dzmitry)
- **NC-1 can be closed.** (Pavel)
- **Echo work is paused until a bill acceptor that reads tickets is found.** (Pavel)
- **NAD 2 gets its own product code; server and data-centre support tasks are needed.** (Pavel, Igor)
- **Investigation may run under service ticket CS-492 (heard); any code change needs a task under a capability.** (Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexey Khamin | Email Toronto the released Flex IQ and Flex-Port build links; duplicate in the release chat | Nov 4, 2026 | High | Filipp, Elizabeth |
| 2 | Pavel Frolov | Mark the "MVP1 Transactional" release in every Jira project | TBD | Normal | Started yesterday |
| 3 | Alexander Biratko | Move the 2 remaining tasks under a capability, close the old feature; take the Flex Pay update tasks; set dates on his tasks | TBD | Normal | |
| 4 | Pavel Frolov | Clarify with the business: Flex Pay MVP 3 first or a Recycler MVP (Texas) | TBD | Normal | |
| 5 | [Unassigned — needs clarification] | Write the instruction for installing on factory firmware via update.bin | TBD | Normal | Alexey raised the need; no owner named |
| 6 | Alexey Khamin | Create a task for the IQ change that blocks Irina's tests | TBD | Normal | |
| 7 | Dzmitry Chudzinau | Describe and show the dashboard download links for Flex IQ | TBD | Normal | |
| 8 | Anton Leshkevich | Send Nebraska game comments; editor prototype; connect the boards | Nov 6, 2026 | Normal | "end of week" |
| 9 | Daniil Stauskiy | Close NC-1 | TBD | Low | |
| 10 | Pavel Frolov, Alexander Biratko | Give Daniil a new task | Nov 5, 2026 | Normal | |
| 11 | Anton Seregin | Add a zoom-out button for the QR code (CF-10, heard) | TBD | Normal | |
| 12 | Dmitri Kovalchuk | Add the missing projects (IP-435 and CMS projects) to the Kanban dashboard filter | TBD | Normal | |
| 13 | Evgeny Kharetski | Finish the new SAS tool and put it in a repository with a Jira project; create a capability and spike for the service-ticket work | TBD | Normal | |
| 13a | Evgeny Kharetski | Review the 48-minute machine video and prepare for Friday | Nov 6, 2026 | Normal | |
| 14 | Igor Metelski | Profile on NAD 2; close Conversion and the old performance bug; sync with designers on NAD 2 December timing | TBD | Normal | |
| 15 | Pavel Frolov | Create tasks for NAD 2 multi-product support (server, data centre) | TBD | Normal | |
| 16 | Irina Shishko | Finish MVP 2 features and tests; check Sergey's server-side work so Dzmitry can release | TBD | High | |
| 17 | Dzmitry Chudzinau | Release the server-side work (and passport, per Sergey) once Irina confirms | TBD | Normal | |
| 18 | Team | Install Wi-Fi modules on ports and antennas on Flex IQ for MVP 2 testing | TBD | Normal | No owner named |

## Open Questions

- Whether to fix the Dakota double handpay ticket after power-off (Evgeny: nothing to fix on JVL side).
- Where release notes live long term: GitHub tags, Confluence, or a generated document in the firmware store. (Irina, Pavel, Dzmitry)
- Framework jurisdiction checks ("if Georgia") vs product code for NAD 2. (Igor, Pavel)
- Who installs Wi-Fi modules and antennas.

## Dispatch Log

---
*Processed from Teams transcript on November 5, 2026*
*Source meeting: Daily Standup meeting*
