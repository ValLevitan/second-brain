# Meeting Summary — Daily Standup meeting
**Date:** October 20, 2026, 4:46 AM – 5:36 AM Eastern
**Duration:** ~51 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Evgeny Kharetski, Igor Metelski, Irina Shishko, Ivan Shpak, Sergey Tsimanov
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026]]

## Summary

Held in Russian. Some ticket numbers are unclear in the transcript and are marked "heard".

**IO board firmware now released from GitHub (Alexander Biratko).** As agreed with Pavel yesterday, IO board firmware is now built and released on GitHub, and the HAL build pulls the release version. Alexander is checking the chain: build a fresh release, install it on a kiosk. He needed Andrei to connect the app key to the repo. The printer has no firmware of ours (templates live in the service library). We own firmware only for our boards. Later, the HAL build for gaming machines will pull the right firmware versions from GitHub releases.

**Flex-Port firmware update is MVP2.** Updating Flex-Port through Flex IQ / Flex Pay is not built. Dima made a version about 5 months ago, but it does not work now. Alekseev is changing the bootloader. First we must prove a firmware update works at all. Pavel: **MVP1 counts as released only when update by USB stick works; remote update is MVP2.** USB-stick update is not yet tested on current software. Meeting with Alekseev today at 2:00 PM; Pavel will bring Irina. Irina tags the related tasks as MVP2 (CAP-137, CAP-122, CAP-146).

**Terminal Hub spoofing fix (Alexander).** A fake kiosk could push out a real one by knowing the protocol. Fix is almost done: checked on dev, stg left. Release with Andrei possibly today. Flex Pay is close to Flex IQ in communication, but screens for user and operator are not reviewed. Port communication changed (for example, port mode: SAS or bill acceptor protocol). Pavel: after the build, ask Claude for all Flex IQ commits about port communication, to see what to bring into Flex Pay. A new feature is fine when it comes from an unmet or new requirement; a capability in Review can go back to In Progress.

**Capability statuses (Irina).** Developers move a capability to Review; Irina checks and moves it to Completed when autotests exist. Closed only at release. She is cleaning up all MVP1 capabilities.

**Autotests (Alexey Khamin).** Added Flex IQ SSH login/password to repo secrets, same as stg. Pavel preferred keys without password; accepted as is ("matter of taste"), easy to change later.

**Games (Anton Leshkevich, Igor Metelski, Daniil Stauskiy).** Anton fixed the vertical help in Clover Fortune and ported one Georgia game for Nebraska 2. Meeting with Val on Wednesday. Pavel: games are ready to go "on a conveyor"; Igor ported Midnight Money and it looks as good or better than the original. Work must be split for the remaining games. Hardest open point: no system yet for the ARM board (RK3576). Linux: Debian everywhere; kernel 6.18 for x86 (FPS Even), likely 6.12 for the RK board. Igor finished the Dutch Mill port in about one 6-hour session; he will fix visible graphic defects and add them to the requirements list so the harness catches them next time. He also prepared Texas vertical Midnight Money scenes and must fix the Sunday spec per Val's requirements.

**Video decode risk.** Dragon Pays horizontal (4 screens) stutters at the auto-spin transition. Igor's Claude thinks too many videos play at once and VP8 has no hardware decode. Daniil's board supports only VP9 hardware decode; he converted the videos and they look fine. Pavel: confirm VP9 plays our videos smoothly on the board; x86 may have CPU headroom, the board does not. Clover Fortune is horizontal too and may have the same issue. Not production-ready until solved.

**Encrypted settings QR spike.** Anton Seregin made spike FP-1364 (heard "13 604" / "13 64") from yesterday's meeting. The AI PM also made a duplicate, a day late, assigned to Sergey Tsimanov (keyword match). Kept to see how the AI PM performs; moved to Sergey; Anton links his task. Pavel stated the requirement for the AI PM: create a task in Product Requirements — device settings (Wi-Fi, password, other parameters) for Flex IQ, Flex Pay, Flex-Port are passed securely; the QR is generated on the server (Location Manager) and given to the device by an operator or technician; each device decodes it. CAP-142 is still proposed, not active.

**Other updates.**
- CAP-243 (Anton Seregin) has mixed statuses; Irina will split out FIQ-80/81/87 to the right capabilities.
- Daniil: game on the board on a big screen; video stutters; needs a dependency-version feature and a Diamond Bonus progress image; needs repo access to Clover Fortune from Dima.
- Evgeny: AI agent work; Georgia MVP1 fixes; RIS performance; tasks (heard) 1262, 1263, 1259 — Pavel asked him to move them to In Progress.
- Ivan: RIS performance; battery nearly done. With hardware tracking off, nothing changes; with it on, RIS cannot be applied with an unregistered passport and server logic depends on it. Ivan will test without the checkbox first.
- Sergey Tsimanov: passport task; adding permissions to the update authorization service. Printer task (Epson-type "950" printer) — likely a printer issue with our template; he starts today, end date moves past the 22nd.
- Vladimir is on vacation.
- Test environment with Terminal Hub and Location Manager that Andrei promised weeks ago: ask Andrei.
- Dmitri: self-hosted runner shows no problems in monitoring; Anton's pipeline ran fine during the meeting.

## Decisions Made

- **MVP1 is released only when Flex-Port firmware update by USB stick works; remote update is MVP2** — restated by Pavel. (Pavel Frolov)
- **Debian on all platforms** — regular updates, unlike Slackware; easier porting between ARM and x86. (Pavel Frolov)
- **Keep the AI PM duplicate spike, move it to Sergey Tsimanov, and link Anton Seregin's task** — to see how the AI PM performs. (Pavel Frolov, Irina Shishko)
- **Keep login/password for Flex IQ SSH in autotest secrets for now** — can change to keys later. (Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Build fresh IO board firmware release, install on kiosk, verify chain | TBD | Normal | GitHub release → HAL |
| 2 | Alexander Biratko | Finish Terminal Hub spoofing fix on stg; release with Andrei | Oct 20 (possibly) | High | |
| 3 | Alexander Biratko | Ask Claude for all Flex IQ port-communication commits; list differences for Flex Pay | After build | Normal | |
| 4 | Irina Shishko | Tag Flex-Port firmware update tasks (CAP-137, CAP-122, CAP-146) as MVP2 | Oct 20 | Normal | |
| 5 | Pavel Frolov | Bring Irina to the Alekseev meeting on USB firmware update | Oct 20, 2:00 PM | High | Blocks MVP1 |
| 6 | Irina Shishko | Send Anton Leshkevich the invite to Wednesday's meeting with Val | Oct 20 | Normal | Done in meeting (forwarded) |
| 7 | Anton Seregin | Link his spike to the AI PM task FP-1364 (heard); team checks its content | TBD | Normal | |
| 8 | Irina Shishko | Split CAP-243: move FIQ-80, 81, 87 to fitting capabilities | TBD | Normal | |
| 9 | Daniil Stauskiy | Confirm VP9 plays our videos smoothly on the board; test Clover Fortune on board | TBD | High | Video decode risk |
| 10 | Dmitri Kovalchuk | Give Daniil repo access to Clover Fortune | TBD | Normal | |
| 11 | Igor Metelski | Fix Dutch Mill port graphics and add defects to requirements list; finish Midnight Money scenes; fix Sunday spec per Val | TBD | Normal | |
| 12 | Evgeny Kharetski | Move his current tasks to In Progress | Oct 20 | Low | |
| 13 | Pavel Frolov | Review his features; run modem-related tests | Oct 20 | Normal | |
| 14 | Sergey Tsimanov | Start the printer service task today | Started Oct 20; end after Oct 22 | Normal | |
| 15 | Irina Shishko, Alexey Khamin | Ask Andrei about the Terminal Hub test environment | Oct 20 | Normal | |

## Open Questions

- Who writes tests for the game ports? (Irina)
- No system yet for the ARM RK3576 board. (Pavel)
- Will VP9 decode on the board handle multi-screen games like Dragon Pays? (Igor)

## Dispatch Log

---
*Processed from Teams transcript on October 20, 2026*
*Source meeting: Daily Standup meeting*
