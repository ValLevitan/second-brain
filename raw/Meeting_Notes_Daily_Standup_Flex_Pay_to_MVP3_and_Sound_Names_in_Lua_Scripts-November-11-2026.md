# Meeting Summary — Daily Standup meeting
**Date:** November 11, 2026, 6:17 AM – 6:33 AM Eastern
**Duration:** ~16 minutes
**Attendees:** Pavel Frolov (led), Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Dzmitry Chudzinau, Evgeny Kharetski, Igor Metelski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026]]

## Summary

Short standup (15 minutes, another meeting followed).

**Release plan.** Alexander asked about the MVP meeting with Andrei. Pavel said it is about MVP 2. Flex-Pay goes to MVP 3, at the start of next year, January 20. Pavel thinks the recycler will probably go there too, but not for Georgia.

**Status by person:**
- **Alexander:** closed his task. He extended the GCM bill validator service to support the recycler and released a new version; next builds of the services will use it. He continues on recycler tasks.
- **Alexey:** closed TIN-93 (CI setup for hardware autotests) and opened TIN-194 with dates and a forecast.
- **Anton Leshkevich:** worked on documentation. With Andrei he discussed security with a camera and made first steps on it.
- **Igor:** for Nebraska (requests from Michael and Efim) he grouped lines in spins when showing winning lines, changed symbol ordering for the designers, fixed the overlay in autospins, updated resources, did work for Dakota and finished changes for GLI requirements. For NOVA 2 he finished porting his scene tool to the engine. He must merge it with main after pulling Anton's latest changes, and he wants Anton to review it, because custom shaders were added to the engine. A custom-shaders feature already exists on Igor; Dmitri asked him to edit its description, and he agreed.
- **Daniil:** added sound support in his branch, calling the sound library directly, with sounds on spins and reels. It plays in time. Some engine parts are not finished yet. He asked where sound names should live so the engine is not rebuilt. Anton Leshkevich: keep the sounds and their names in the Lua scripts; the engine plays a sound by name. Daniil will do it that way and finish tomorrow.
- **Anton Seregin:** closed FIQ-83. Still to do: verify the emulator can push firmware to a real port. Some autotest cases are not covered by the emulator. Pavel: do not emulate the cloud service; make the emulator able to fetch firmware from dev or STG instead.
- **Dzmitry:** closed the machine statistics export, made the release and wrote to Val that it is ready. Today he looks at MVP 2 bugs and at Flex-Pay tasks needed before the next release.
- **Evgeny:** worked on the agent and the LTE task.
- **Sergey:** Wi-Fi on the port is implemented. He also made changes requested by Sergey for the other side.
- **Vladimir:** working on test 105, waiting for a free run. Next 111 and maybe 114 in parallel if Wi-Fi works on the terminal. Pavel: the terminal given to Sergey has working Wi-Fi; the one with Anton does not. Vladimir said machine 82 has Wi-Fi.
- **Ivan:** nothing new.

**SD-card flashing from factory firmware.** Alexey asked who looks at terminals that do not flash from the SD card. Pavel closed it on Monday: the MVP 2 firmware installs fine over JVL's old firmware. But on a board with factory firmware, booting from the SD card works only with an HDMI monitor connected. This is a hardware issue on the board and cannot be fixed. In future releases the first firmware will most likely be flashed by cable, as for RK3576. The task is closed; a new production document on how to flash boards will be written. Dzmitry asked about an HDMI dummy plug; Pavel said maybe resistors could work, but he has not thought about it.

**Pavel's own items:** tonight he looks at a printer problem and at the modem for Georgia.

## Decisions Made

- **Flex-Pay moves to MVP 3, planned for January 20, 2027.** (Stated by Pavel)
- **Sound files and their names live in the Lua scripts; the engine plays sounds by name.** (Anton Leshkevich; Daniil agreed)
- **The emulator does not emulate the cloud firmware service; it can be set to fetch firmware from dev or STG.** (Pavel)
- **First firmware on factory boards (no HDMI) will be flashed by cable in a future release; a production flashing document will be written.** (Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Metelski | Merge the NOVA 2 scene tool with main after pulling Anton's changes and open a pull request | TBD | Normal | Custom shaders added to the engine |
| 2 | Anton Leshkevich | Review Igor's scene-tool merge request | TBD | Normal | Igor asked for it; Anton did not confirm in the meeting |
| 3 | Igor Metelski | Edit the description of the custom-shaders feature | TBD | Low | Dmitri asked; Igor agreed |
| 4 | Daniil Stauskiy | Finish sound playback with names kept in Lua scripts | Nov 12, 2026 | Normal | "Tomorrow I'll finish" |
| 5 | Anton Seregin | Verify the emulator can push firmware to a real port | TBD | Normal | Fetch from dev or STG, no cloud emulation |
| 6 | Dzmitry Chudzinau | Look at MVP 2 bugs and Flex-Pay tasks needed for the next release | Nov 11, 2026 | Normal | Today's plan |
| 7 | Vladimir Samusenko | Run test 105, then 111 and maybe 114 | TBD | Normal | Needs Wi-Fi on a terminal (machine 82) |
| 8 | [Unassigned — needs clarification] | Write a production document on flashing boards with factory firmware | TBD | Normal | Pavel said "we will write"; no owner named |
| 9 | Pavel Frolov | Look at the printer problem and the Georgia modem | Nov 11, 2026 (evening) | High | Pavel's own words |

## Open Questions

- Does the recycler also go to MVP 3, and not for Georgia? (Said in passing by Pavel; not confirmed)
- Could an HDMI dummy plug or resistors let factory boards boot from SD card? (Raised by Dzmitry)

## Dispatch Log

---
*Processed from Teams transcript on November 11, 2026 (scheduled meeting-watcher)*
*Source meeting: Daily Standup meeting*
