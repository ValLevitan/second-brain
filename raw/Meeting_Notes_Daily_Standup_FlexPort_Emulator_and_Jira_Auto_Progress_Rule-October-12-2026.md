# Meeting Summary — Daily Standup meeting
**Date:** October 12, 2026, 4:56 AM – 5:42 AM Eastern
**Duration:** ~46 minutes
**Attendees:** Pavel Frolov, Irina Shishko, Dmitri Kovalchuk, Dzmitry Chudzinau, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Evgeny Kharetski, Alexander Biratko, Sergey Tsimanov, Vladimir Samusenko, Ivan Shpak
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026]]

## Summary

Monday standup run by Pavel. Held in Russian. Some task numbers are garbled in the transcript.

**Claude bot balance.** Alexey said the Claude bot is badly missed for his test work. Pavel: Andrei wrote yesterday that the card has no money to extend it, and wrote to Inna. Dmitri Kovalchuk: he tried to top up today; some $100 payments were refused and some went through. About 300 CAD is on the balance now. He thinks the bank's security blocks some payments. He is waiting for an answer. He could use a Canadian card, but not without approval. Irina: do not do it without permission. 300 CAD is about 20 pull requests (PRs are checked 2–3 times on average); about 700 was used up in half a day over the weekend.

**Video alpha and FPS (feature 1343).** Daniil re-encoded all videos to VP8 so hardware decoding works. FPS holds at 55–59 on almost all scenes; he will measure memory and send a report. With alpha as a separate parameter, Chromium decodes on the processor; on the board FPS drops to 25–30. Now alpha is built into the video stream. Alexander: find the fastest method, in the stream or not. One option is the old Rage approach: one video plus a light shader (a channel used for blend/multiply), which was faster than two stacked videos. Pavel recalled an old problem with the min/max alpha value; Alexander: that came from mixing the old shader method with the new one. They will ask Igor today how he solved alpha and blend modes. Designers may also be consulted.

**Flexport emulator vs real hardware.** Alexey asked about a Flexport (port) emulator. Pavel: nobody planned one; the port is an STM32 processor with many hardware interrupts. A real STM32 emulator would be needed, and the known ones are likely not good enough. Sergey suggested a container emulator built from the port code, without hardware. Alexey expects Val wants testing on live code. Pavel: real ports with the hooks already built give the most reliable tests, and there are enough ports. Irina: real ports do not block us; tests can run overnight. Final: port CI runs on real hardware through the internal self-hosted runner. Pavel: a study of STM32 simulators can happen later — not MVP1, likely not MVP2. Pavel: the Flex IQ emulator can run in Docker on the internal runner so it sees the hardware.

**Flex IQ version numbers.** Dzmitry: each environment (STG, prod) has its own version counter, set by GitHub automatically, so prod starts again from 1.0.0. Pavel does not like it. Dzmitry: not a blocker for MVP1. Pavel: a task after MVP1 to find the right solution.

**Jira auto "In Progress" rule.** Sergey asked why task port 118 moved to In Progress on him when he did not open it. Dmitri Kovalchuk: an automation opens a task when a branch, commit or PR mentions it. Vladimir made the commit; his commit text named the port task though the work was for another task (TIN-30). Vladimir: Jira finds task keys anywhere in the text, so commits must not name unrelated tasks. Pavel proposed: only the first word of the commit message counts. Irina proposed: match the repository to the project key. Dmitri: Jira has no such flexible rules; he said "let's turn off this rule." Not confirmed by others.

**Tasks 118–122.** Irina: 4 tasks were opened yesterday from Vladimir's long list of questions, after review by two Claude instances. People must now decide if they are needed. All are on Sergey. Pavel: Sergey should review them with his Claude; they should be rewritten in clear Russian.

**AI Draft tasks start today.** Dmitri Kovalchuk: from today the AI agent creates tasks. From tomorrow morning the team reviews tasks with status "AI Draft" by filter. If a task is not needed, choose Reject and pick a resolution; a text comment can be added.

**Other.**
- Alexander: capability 117 — card activation and issuing through Payment Hub works over the weekend. Fixed wrong card dispenser codes. One task left on failure responses. Will create questions for MVP2 flows.
- Alexey: reviving autotests on PRs and on real hardware; 2 test sets now pass on PRs. Will add a rule so needed CI parameters are written at once. Cannot take extra features today or tomorrow.
- Anton: closed 147 (STG cloud profile, so it registers as a normal terminal). Closed 150 and 151 (Vladimir's); will re-check. Wants a free terminal to run a scenario. Pavel: build one more terminal for him; parts should be enough. Irina asked about 3D-printed parts; Pavel: half the parts could be printed.
- Daniil: finished task 1057.
- Dzmitry: closed all stories on mockup gaps. Brought the machine (EGM) emulator close to the SAS standard; real machines differ. Could not reproduce the Flex IQ SD card install problem in about 20 installs; rewrote the error text and added logging. Mass deploy on STG: pods fail and assets go inactive after delete; fix and new update in about an hour. Small Payment Hub edits to cut requests to InComm and Hong Kong. Prepping prod with Andrei: certificate done, fresh prod build today, web services roll to prod today. Location billing: Pavel — roll out what Nathan has. Location billing does not affect MVP1.
- Sergey: asked if Nathan added the location billing API and a button on our side; Pavel: need to check. Finishing STG deploy with CMS changes; closing story tasks.
- Pavel: asked Dzmitry and Irina to review PR 169 (port 111), which touches Flex IQ (status when registration is lost). Took port 110. Will look at port 117.
- Evgeny: finishing 1241 (number unclear); requests are done, Sergey may finish the rest. Testing should start. Ivan is busy with autotests, so Evgeny will test himself. Release target October 22.
- Irina: autotests split between Ivan and Vladimir, one per day, to finish by October 15. Many tests she took from Alexey. Flag any test that cannot be automated (cloud, manual only). Flex IQ remote firmware update tests are left to the very end.
- Vladimir: autotests; lottery answers came back. Reviewing all blocked tasks today to move as many as possible.

## Decisions Made

- **Flexport port tests in CI run on real hardware through the internal self-hosted runner; no port emulator now.** — reliable, hooks exist, enough ports. STM32 simulator study is not MVP1, likely not MVP2. (Decided by Pavel Frolov, Irina Shishko)
- **Per-environment Flex IQ version numbers are not an MVP1 blocker; find a solution after MVP1.** (Decided by Pavel Frolov)
- **Roll location billing to prod as it is now.** — Nathan's work is not complete; billing does not affect MVP1. (Decided by Pavel Frolov)
- **Build one more terminal for Anton.** (Decided by Pavel Frolov)
- **No Claude bot top-up with another (Canadian) card without approval.** (Decided by Irina Shishko)
- **From October 13 the team reviews "AI Draft" tasks; unneeded ones are Rejected with a resolution and optional comment.** (Decided by Dmitri Kovalchuk)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dmitri Kovalchuk | Get the bank answer on refused Claude bot top-ups | TBD | High | ~300 CAD left |
| 2 | Alexander Biratko | Finish card failure-response task; create questions for MVP2 flows | TBD | Normal | Capability 117 |
| 3 | Alexey Khamin | Make autotests pass on PRs and real hardware; add CI parameter rule; wire Flexport CI through the runner | TBD | High | |
| 4 | Anton Seregin | Re-check and close 150 and 151; run scenario on a terminal | TBD | Normal | |
| 5 | Pavel Frolov | Build one more terminal for Anton | TBD | Normal | |
| 6 | Daniil Stauskiy | Measure FPS and memory; send report; find the fastest alpha method | TBD | Normal | Feature 1343 |
| 7 | Pavel Frolov, Alexander Biratko | Ask Igor how he solved alpha and blend modes | Oct 12 | Normal | |
| 8 | Dzmitry Chudzinau | Fix STG pod/asset issue; roll new update | Oct 12 | High | "In about an hour" |
| 9 | Dzmitry Chudzinau | Roll web services and location billing (as is) to prod with Andrei | Oct 12 | High | Prod prep |
| 10 | [Unassigned — needs clarification] | Check what Nathan added for the location billing API and our button | TBD | Normal | Pavel, Sergey |
| 11 | [Unassigned — needs clarification] | Task after MVP1: shared Flex IQ version numbering across environments | After MVP1 | Low | |
| 12 | Dzmitry Chudzinau, Irina Shishko | Review PR 169 (port 111) for Flex IQ impact | TBD | Normal | |
| 13 | Pavel Frolov | Look at port 117 | TBD | Normal | |
| 14 | Evgeny Kharetski | Finish 1241 and test it himself | Oct 22 | High | Release target |
| 15 | Ivan Shpak, Vladimir Samusenko | Write autotests, one per day | Oct 15 | High | |
| 16 | All developers | Flag tests that cannot be automated to Irina | Ongoing | Normal | |
| 17 | Sergey Tsimanov | Review tasks ~118–122 with Claude; rewrite clearly in Russian | TBD | Normal | |
| 18 | Vladimir Samusenko | Review all blocked tasks and move as many as possible | Oct 12 | Normal | |
| 19 | All team | Review "AI Draft" tasks each morning | From Oct 13 | Normal | |

## Open Questions

- Should the Jira automation that moves a task to In Progress on any branch/commit/PR mention be turned off? Dmitri Kovalchuk suggested it; not confirmed. (Sergey Tsimanov, Vladimir Samusenko, Pavel Frolov, Irina Shishko)
- How did Igor solve alpha and blend modes in the old Rage videos? To be asked today.
- Is the Flex IQ SD card install problem really fixed? Not reproduced in ~20 installs.

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-14*
*Source meeting: Daily Standup meeting*
