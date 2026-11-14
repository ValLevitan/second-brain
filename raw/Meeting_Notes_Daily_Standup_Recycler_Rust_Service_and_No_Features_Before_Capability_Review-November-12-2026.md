# Meeting Summary — Daily Standup meeting
**Date:** November 12, 2026, 6:14 AM – 6:48 AM Eastern
**Duration:** ~34 minutes
**Attendees:** Pavel Frolov (led), Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Dzmitry Chudzinau, Evgeny Kharetski, Igor Metelski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Recycler_Rust_Service_and_No_Features_Before_Capability_Review-November-12-2026]]

## Summary

**Sounds in the new engine.** Daniil added a mode button and sound switching in the Studio and will commit and open a pull request. He asked where the old LGS sounds should live, since the engine now plays all sound. Alexander: game sounds stay in the game, system sounds go to the framework. Pavel: clicks inside the setup screens stay in setup; for the speaker test, setup sends a command to the framework to play the sound. Daniil agreed.

**Recycler.** Alexander is working on the recycler. He raised the bill-validator Rust service to version 0.7 and checked it on Flex-Pay. The vendor's library was used only as a reference; the needed recycler commands were added to JVL's own Rust service, so it builds for x86 and ARM. Pavel said he, Alexander, Irina and Andrei must start reviewing the recycler capabilities and find gaps. Irina said Val set a meeting on it for 14:45 Minsk time.

**MVP 2 capabilities.** Dzmitry reviewed the MVP 2 capabilities and fixed product codes. He needs Efim to confirm whether presets per progressive stay the same. Some requirements need clarification and some cannot be built. He will comment on each capability with a link and Andrei answers. He will not create features until the review is done, because changed requirements would make them stale. Irina noted no meeting with Andrei was booked yet; Pavel said Andrei promised one today. Vladimir needed report-page features (capability 315) for his test TINT-182; Pavel said creating them now is premature, so Vladimir takes another task.

**Status by person:**
- **Alexey:** TIN-194, fixing test scenarios for real hardware. Did Ivan's request to change the release tag name. Found a mismatch with requirements and wrote to Andrei. Andrei asked whether the mode should be hard or soft; Pavel must answer, but does not remember what was agreed. Also asked Anton Seregin to look at FIQ-218 (add to the emulator).
- **Anton Leshkevich:** Studio and engine; added Igor's work yesterday. He may have chosen the wrong engine for the agents and will fix it today.
- **Anton Seregin:** working on 129. Needs access to repositories. Questions Sergey asked earlier are still not answered by Pavel.
- **Dzmitry:** main work with Andrei on a video mock-up; maybe a first deploy today.
- **Evgeny:** agent — load wiki and math, test service-ticket creation. RIS performance: Ivan found and fixed bugs. LTE on/off tasks (97, 98, 99) are still in planning.
- **Igor:** Nebraska resources. Fixed builds of old branches that Monica needs for video recording. With Ivan, trying to make GLI's patch run on Windows; their data center did not start, Java version to check. Pushed his tool commits into Anton's projects, fixed review comments, now adding symbol tools.
- **Irina:** reviewing the current project's capabilities and started writing tests.
- **Ivan:** Pavel's fix works in a quick check. Continues RIS performance; builds production after lunch, to give to Felipe. Asked when the LTE modem work will finish. Asked Pavel to come by after lunch about a printer behaviour question.
- **Sergey:** finishing the Wi-Fi QR validation protocol between port and terminal. Getting the QR through the terminal (online and offline) is already done. Open cases: a fully offline terminal with no network at all, and slow firmware transfer from terminal to port over Wi-Fi. Pavel: discuss separately; Wi-Fi speed can likely be raised about 4 times.
- **Dmitri Kovalchuk:** Gantt chart looks good — almost nothing overdue or open over 14 days. Some open features have closed parents. Many tasks have no due date and need one. Vladimir is building a plugin that loads the standard into Claude.

**LTE modem.** Dzmitry owns the LTE modem on/off event and activation code; he will do the GUI himself. Pavel: the Georgia LTE build works only with some modems; in the field, Elizabeth reflashes modems before handing them out. That should be built in. Pavel must check whether those fixes are in the build.

## Decisions Made

- **Setup click sounds stay in setup; the speaker test is played by the framework on a command from setup.** (Pavel; Daniil agreed)
- **Features for MVP 2 capabilities are created only after the capability review is done.** (Dzmitry, Pavel agreed; Vladimir moves to another task)
- **Dzmitry does the LTE modem GUI himself; Anton is not needed.** (Dzmitry, Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Daniil Stauskiy | Commit the Studio sound work and open a pull request | TBD | Normal | |
| 2 | Pavel Frolov, Alexander Biratko, Irina Shishko, Andrei Klimovich | Review recycler capabilities and find gaps | TBD | High | Pavel's words |
| 3 | Pavel Frolov | Answer Andrei's hard/soft mode question from Alexey's task | TBD | Normal | Pavel does not remember the agreement |
| 4 | Anton Leshkevich | Fix the engine choice for the agents | Nov 12, 2026 | Normal | |
| 5 | Dzmitry Chudzinau | Comment on MVP 2 capabilities with links for Andrei to answer | TBD | High | |
| 6 | Efim Podvoiski | Confirm whether presets per progressive stay the same | TBD | Normal | Dzmitry needs it; Efim not present |
| 7 | Ivan Shpak | Build production after lunch and give it to Felipe | Nov 12, 2026 | Normal | Irina's request |
| 8 | Pavel Frolov | Visit Ivan after lunch about the printer behaviour question | Nov 12, 2026 | Normal | |
| 9 | Pavel Frolov | Check whether the field modem fixes are in the build | TBD | Normal | |
| 10 | Dzmitry Chudzinau | LTE modem on/off event, activation code and GUI | TBD | Normal | Ivan: "don't drag it out" |
| 11 | Anton Seregin | Look at FIQ-218 (add to emulator) | TBD | Low | Alexey's request |
| 12 | [Unassigned — needs clarification] | Set due dates on tasks that have none | TBD | Normal | Dmitri K's Gantt review |

## Open Questions

- How does a fully offline terminal (no internet, no LTE) get on the network? (Sergey; to be discussed separately)
- Slow firmware transfer over Wi-Fi from terminal to port. (Sergey; separate discussion)
- Hard or soft mode for the case Alexey raised. (Andrei, waiting on Pavel)

## Dispatch Log

---
*Processed from Teams transcript on November 12, 2026 (scheduled meeting-watcher)*
*Source meeting: Daily Standup meeting*
