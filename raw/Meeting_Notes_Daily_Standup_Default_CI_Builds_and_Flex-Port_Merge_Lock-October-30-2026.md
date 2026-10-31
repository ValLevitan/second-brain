# Meeting Summary — Daily Standup meeting
**Date:** October 30, 2026, 4:45 AM – 5:31 AM Eastern
**Duration:** ~45 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Dzmitry Chudzinau, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026]]

## Summary

Held in Russian. Audio is poor in places. Unclear names, numbers and words are marked "heard".

**Standup time.** Pavel proposed moving the standup 1.5 hours later from next week, so Anton Leshkevich does not have to wake so early. Anton said it would suit him better.

**CI builds must work with defaults.** Alexey's Flex IQ build failed again. There are about 80 parameters and he should not need to study them to get a build. Sergey: a cache conflict — the last build was made for dev, so the parameter has to be switched to the branch. Dzmitry: the parameters exist for a reason; he runs builds through Claude Code. **Pavel's rule: the default action with default parameters must build for its target environment. A separate action with many parameters can exist for Claude and special cases.** Alexey also reported a version conflict: after a build from a branch, the next main build takes a version that already exists. Dzmitry asked for a Jira task with clear priorities instead of chat requests.

**Yegorsky (heard) and the Flex-Port repo.** Yegorsky keeps messaging Alexey about tasks. Val said earlier he is not on the project. Pavel will raise with Val whether work with him is closed. Dmitri Kovalchuk: Jira access was given for FPORT only. Irina and Alexey worry his commits could break the tested code. **Pavel asked Dmitri to stop Yegorsky from merging into main in the Flex-Port repo (pull requests still allowed). Alekseev keeps his access.** Anton Seregin suggested a fork; Pavel said no, it would never merge back. Pavel will not merge his Wi-Fi work into main before the port release (today or tomorrow).

**Engine spike.** Anton Leshkevich is splitting the prototype into modules. He added Dutch Mill (heard) and moved game math into separate modules, so a game loads only what it needs. Half done. There is no Jira task — Pavel: "no task, no work." Anton will ask the PM agent to create one. Alexander asked Anton to move the engine requirements into Jira today; Anton agreed.

**Sound library (FMOD).** Daniil finished NFL1 (heard). The audio uses FMOD, a closed binary library. He found no free library with full support for its curves and parameters; 13 FSB sound files are used. Pavel suggested a popular AI reverse-engineering tool and asking Vlad what he really used. Alexander wants to keep the existing sound library without redoing it; he will talk to Daniil, then Vlad if needed.

**Other updates.**
- Pavel: dual-screen support now works in the custom Linux kernel (SDK task 3576, heard); next sound, the graphics accelerator and peripherals. Also Wi-Fi access point mode on Flex IQ and its setup screens (tasks from Anton Seregin).
- Pavel: the new device integration task still waits for a package (about a month); he will ask again; likely for Alexander.
- Alexander: last Flex-Port task with BV mode (port 188, heard); Irina will give him tasks from Andrei's updated requirements; Flex Pay capability 165 — SAS logging to Grafana.
- Alexey: hardware autotests continue.
- Anton Seregin: generated capabilities and features brought to standard; BEP and Flex Pay Jira repos moved to the current schema; acceptance criteria generated for requirements ("a requirement without acceptance criteria is empty" — Irina). Pavel: mark these capabilities MVP-2 Transactional. Next: server UI page for Wi-Fi settings and QR code generation; encryption to discuss; ADR 503 (heard) to check.
- Dzmitry: created capabilities and features for the report with Excel export; RIS/passport migration dates removed.
- Evgeny: regulation done; two feature requirements; preparing for the competitor teardown meeting.
- Irina: reviewing Andrei's requirements; sent 22 (heard) to Alexander; tests must be adapted.
- Ivan: Gela (heard) says the BV and printer do not show — the install was show mode without devices; he will do a new install. CMS/RIS work continues.
- Sergey: port firmware changes done, testing; will split the feature into capabilities per repository.
- Vladimir: closed 3507 and LGS 44 as duplicates; FREIK 3 (heard, audit screen) unclear — checking with Alexander; studying capabilities.
- Andrei's port 107 (heard) item: after a machine reboot the port may not return to idle. Alexey (or Ivan) will recheck with a reboot and separate power.
- Irina asked Dzmitry to review Andrei's edited requirements; items 1815 and 917 (heard) to be filed on Dzmitry and Vladimir.

## Decisions Made

- **Default CI build action must build with default parameters for its target environment** — a separate many-parameter action may exist for Claude and special cases. (Pavel; Alexey agreed)
- **Yegorsky (heard) blocked from merging into main in the Flex-Port repo; pull requests still allowed; no fork.** (Pavel)
- **No Wi-Fi work merged into main before the port release.** (Pavel)
- **New generated capabilities are marked MVP-2 Transactional.** (Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Create a Jira task for Dzmitry to revise CI/CD (simple defaults, branch/main version conflict) | TBD | High | Builds fail without expert knowledge |
| 2 | Dmitri Kovalchuk | Block Yegorsky (heard) from merging into main in the Flex-Port repo | Oct 30, 2026 | High | Release this week |
| 3 | Pavel Frolov | Ask Val whether work with Yegorsky (heard) is closed | TBD | Normal | |
| 4 | Anton Leshkevich | Get a Jira task created (via the PM agent) for the engine modularity spike | Oct 30, 2026 | Normal | "No task, no work" |
| 5 | Anton Leshkevich | Move the engine requirements into Jira | Oct 30, 2026 | Normal | Alexander asked |
| 6 | Anton Seregin | Mark the generated capabilities as MVP-2 Transactional | TBD | Normal | |
| 7 | Alexander Biratko | Talk to Daniil, then Vlad if needed, about replacing FMOD while keeping the sound library | TBD | Normal | |
| 8 | Daniil Stauskiy | Keep researching FMOD alternatives / reverse engineering and report back | TBD | Normal | |
| 9 | Pavel Frolov | Ask again about the device package for the new integration | TBD | Low | Waiting about a month |
| 10 | Alexey Khamin | Recheck port return to idle after machine reboot (reboot + separate power) | Oct 30, 2026 | Normal | Ivan if Alexey cannot |
| 11 | Ivan Shpak | Do a new install for Gela (heard) and check the BV/printer issue | Oct 30, 2026 | Normal | |
| 12 | Dzmitry Chudzinau | Review Andrei's edited requirements and file items on himself / Vladimir | TBD | Normal | Irina asked |

## Open Questions

- Standup moves 1.5 hours later from next week — proposed, not confirmed as final. (Pavel)
- Whether FMOD's curves/parameters are really needed for the existing sounds. (Alexander, Pavel)

## Dispatch Log

---
*Processed from Teams transcript on October 30, 2026*
*Source meeting: Daily Standup meeting*
