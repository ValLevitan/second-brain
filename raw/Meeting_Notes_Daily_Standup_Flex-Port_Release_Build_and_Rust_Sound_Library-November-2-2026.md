# Meeting Summary — Daily Standup meeting
**Date:** November 2, 2026, 5:15 AM – 5:56 AM Eastern
**Duration:** ~41 minutes
**Attendees:** Pavel Frolov, Irina Shishko, Dzmitry Chudzinau, Alexander Biratko, Evgeny Kharetski, Sergey Tsimanov, Anton Seregin, Ivan Shpak, Vladimir Samusenko, Dmitri Kovalchuk, Daniil Stauskiy, Anton Leshkevich, Alexey Khamin, Igor Metelski
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026]]

## Summary

Held in Russian. Audio is poor in places. Unclear names, numbers and words are marked "heard".

**Standup time.** Val asked to move the standup one more hour later after the clock change. Irina: one hour later lands on the Minsk lunch break. Vladimir proposed 3:00 PM Minsk; Pavel and Evgeny said meetings with Val usually start at 3:00. **Agreed: standup at 2:30 PM Minsk time; people shift lunch 15 minutes earlier.**

**Flex-Port and Flex IQ release.** Pavel: today the team builds the Flex-Port production build, runs the remaining tests and releases it. Flex IQ releases its latest version after the fix. **Remote port firmware update is not in this release.** Sergey: only a build key for the port went into main; the port firmware transfer via Flex IQ lives only in his uncommitted branch and does not affect the release. Alexander confirmed the port ships without his partial port firmware change. Bugs: FIQ-201 (Sergey) and FIQ-202 (Vladimir, tests only, after Andrei's updated test library) are closed; FIQ-203 is on Dzmitry and is the last one. Irina: Flex-Port can be assembled for release now; Flex IQ waits for FIQ-203, then a recheck.

**Sergey, port firmware.** Over the weekend he finished the port firmware transfer. He sent Dzmitry an artifact describing what is implemented. He flashed port 156 (heard) through IQ 83 (heard) successfully. He added a firmware check on the port itself so a bad build cannot be slipped in through a USB stick. He waits for the release so main is free, then merges.

**Alexander.** Fixed Flex-Port bugs over the weekend; the export is close to release form. Reviewed the capabilities written for the Omni engine and added Anton's new-engine requirements; most of them belong to the framework, not the engine. The engine needs its own capabilities (renders, video, images). Took over the 30 tasks moved from Yavorsky; about 80% are already done and will just be closed; some bugs cannot be reproduced any more.

**Sound library spike (Daniil).** The sound repository is being rewritten in Rust. He dropped the Kira (heard) library: it cannot send sound to different speakers (top and bottom) and has no event system; it would save only about 200 lines. He uses PulseAudio instead. The result is one self-contained library that runs on Windows and ARM. A converter tool already exists: sound files go from FSB to FLAC, and the description becomes JSON instead of the old files. Alexander: the sound library lives in the engine, not in LGS; LGS controls it through an API (websocket inside the app). Daniil's work is to be in Rust so everything is in one language. Alexander has not spoken to Vlad; Vlad can keep working with his tools, we just convert the format. Anton Leshkevich thanked Daniil for testing Kira, which he had recommended without trying.

**Anton Leshkevich, engine spike.** Finished the modularity spike: on the new engine prototype, most functionality lives in the framework and games are small modules that override what they need. Now studying whether to add a scripting language to the engine, so an editor can change files without recompiling the game on every iteration. Friday he also worked on resources for "wallfirance" (heard).

**Anton Seregin, MVP-2 features.** Generated a feature for Wi-Fi settings in the location manager, a QR page, checked ADR 503 (heard), and moved the features into MVP 2. Pavel did the Wi-Fi setup screens on Flex IQ last week (in a branch, not main) and asked Anton to review them. Anton: the features are not assigned to anyone. **Pavel: a separate MVP-2 grooming meeting today at 3:00 PM Minsk with Anton Seregin, Dzmitry, Sergey and Irina — assign tasks and set dates.** Dzmitry objected that Anton created 7 features for Wi-Fi and location manager; he prefers one feature with many stories. Anton: the standard is one feature per repository. Pavel: if several features do the same thing in one repository there is no point splitting, unless testing differs or several repositories are involved. Dzmitry will review and clean up.

**Dzmitry.** Closed all FIQ bugs over the weekend; FIQ-203 is next. He needs to deploy the legacy CMS report to prod but Sergey's work from Dzmitry's vacation (RIS, passport, lease) was tested by Ivan and he does not know what was checked. Ivan: he only works on staging and has not checked prod. **They will talk on Wednesday; Dzmitry must report on Friday why it is not deployed.** The Flex IQ hang from the weekend stays for the next release. Proposal: merge the two UIs (work mode and setup mode) into one — the switch is a separate app with new web connections, it is slow, and tests stumble on it. Reverse SSH works only from one network through the MS box; Pavel: not for production at 50–100 IQs, better through AWS, but fine for about 10 locations for now. Dzmitry: Grafana logs need regular monitoring. A Flex IQ on Saturday got into a state where the kernel ate something and stopped sending data; nobody knows what Andrei did over SSH, and there are no logs to show how it got there. Pavel: if there are resources in the next two weeks, think about what logs are needed.

**MVP-2 for terminals (Pavel).** Remote port update via Flex IQ (almost ready, needs testing); Wi-Fi on ports and Flex IQ (almost ready); server side: the location manager sets the access-point password and generates a QR code, Flex IQ sets up the access point over LTE, ports join the network. Add Wi-Fi to the capabilities. Next one to two weeks.

**Evgeny.** Over the weekend prepared the progression repository: contracts described, dead code cleaned, so Igor's part can be merged. Not touching games. Did the modem for RIS "промбанс" (heard) for MVP 1 and gave it to testing; it is the same branch wanted for Echo. Pavel noted Val had earlier said no modem was needed; Irina: it stays. Pavel agreed. Next: recording videos for competitor analysis.

**Pavel.** Wi-Fi on Flex Pay / Flex IQ, setup screens; SDK for RK3576 — the new kernel had no GPU video decoding, so he pulled that in plus security. On this platform the machine could record what is on screen in good quality for debugging and AI analysis; streaming over the internet is too heavy.

**Other.** Alexey continues hardware autotests on the runner; two blockers from yesterday were resolved today with Andrei and Dima; PR review continues. Ivan built a RIS build with the modem and installed it on Echo; Irina: check games run, the printer works on Echo and the modem connection works. Igor is inserting resources into NOVA 2 (heard), made a bonus page from Evgeny's video analysis, and is preparing repositories to test shader backgrounds on the machine. Vladimir is fixing tests after Andrei's answers on requirements; done today. Irina will check his in-progress tasks to avoid duplicate work. Dmitri Kovalchuk asked the team to review the agent's output accumulated over the weekend and send feedback. Dzmitry asked that the agent not write Russian in descriptions; Dmitri: there is no written standard, Jira can be filled in Russian or English, English preferred (bilingual rule from an old meeting with Aaron).

## Decisions Made

- **Standup moves to 2:30 PM Minsk time (one hour later), starting now.** (Pavel; Irina agreed; Val asked)
- **Remote port firmware update is not in this Flex-Port / Flex IQ release.** (Pavel)
- **Sound library is rebuilt in Rust with PulseAudio and lives in the engine, not LGS; Kira (heard) dropped; FSB → FLAC + JSON.** (Pavel, Alexander, Daniil)
- **Flex IQ hang issue goes to the next release.** (Pavel, Dzmitry)
- **Modem support for RIS / Echo stays as an MVP 1 capability.** (Irina; Pavel agreed)
- **MVP-2 grooming meeting today at 3:00 PM Minsk.** (Pavel)
- **Reverse SSH through the MS box is acceptable for about 10 locations; AWS later at 50–100 IQs.** (Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Team (Pavel coordinating) | Build the Flex-Port production build, run remaining tests, release Flex-Port | Nov 2, 2026 | High | No single builder named |
| 2 | Dzmitry Chudzinau | Fix FIQ-203 (last Flex IQ bug) | Nov 2, 2026 | High | Flex IQ release waits on it |
| 3 | Irina Shishko | Recheck Flex IQ after FIQ-203 and release it | TBD | High | |
| 4 | Sergey Tsimanov | Merge the port firmware transfer branch into main after the release | TBD | Normal | Artifact sent to Dzmitry |
| 5 | Alexander Biratko | Close or transfer the 30 tasks moved from Yavorsky | TBD | Normal | ~80% already done |
| 6 | Anton Seregin | Review Pavel's Wi-Fi setup screens on Flex IQ (branch) | TBD | Normal | |
| 7 | Anton Leshkevich | Finish the scripting-language study for the engine and report results | TBD | Normal | |
| 8 | Daniil Stauskiy | Rewrite the sound library in Rust with PulseAudio; FLAC + JSON format | TBD | Normal | |
| 9 | Ivan Shpak, Dzmitry Chudzinau | Meet on Wednesday to confirm Sergey's RIS / passport / lease work can go to prod | Nov 4, 2026 | High | Dzmitry reports Friday |
| 10 | Ivan Shpak | Test the RIS build with modem on Echo: games, printer, modem connection | TBD | Normal | |
| 11 | Pavel Frolov | Hold the MVP-2 grooming meeting at 3:00 PM Minsk with Anton S, Dzmitry, Sergey, Irina | Nov 2, 2026 | Normal | Assign features, set dates |
| 12 | Dzmitry Chudzinau | Review and clean up the 7 Wi-Fi / location manager features | TBD | Low | |
| 13 | Pavel Frolov | Send the AI PM draft task to To Do for Dzmitry; Dzmitry sets the correct reporter | TBD | Low | |
| 14 | Vladimir Samusenko | Finish test fixes from Andrei's requirement answers and commit | Nov 2, 2026 | Normal | |
| 15 | Irina Shishko | Check Vladimir's in-progress tasks for overlap with her weekend test runs | TBD | Low | |
| 16 | Team | Review the agent's weekend output and send Dmitri Kovalchuk feedback | TBD | Normal | |

## Open Questions

- Merge the two Flex IQ UIs (work mode and setup mode) into one — proposed for the next release, not decided. (Dzmitry)
- What logs the Flex IQ needs so a hang can be traced. (Dzmitry)
- Jira language: no written standard; Russian or English allowed. (Dzmitry, Dmitri)
- "22 stories" on Dzmitry (heard) — unclear what Irina referred to.

## Dispatch Log

---
*Processed from Teams transcript on November 2, 2026*
*Source meeting: Daily Standup meeting*
