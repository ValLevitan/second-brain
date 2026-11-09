# Meeting Summary — Daily Standup meeting
**Date:** November 5, 2026, 6:15 AM – 7:15 AM Eastern
**Duration:** ~59 minutes
**Attendees:** Pavel Frolov (host), Irina Shishko, Alexander Biratko, Anton Leshkevich, Daniil Stauskiy, Alexey Khamin, Anton Seregin, Dzmitry Chudzinau, Sergey Tsimanov, Igor Metelski, Evgeny Kharetski, Ivan Shpak, Vladimir Samusenko, Dmitri Kovalchuk
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026]]

## Summary

**New game engine — capabilities and block diagram.** Alexander asked when the engine group meets again; nothing is scheduled. He wants one person (Anton Leshkevich) to set the base architecture in the repo, then split capabilities across people (Daniil could take a small piece once his sound tasks run out). Pavel asked Anton to generate the capability list from the requirements already discussed, plus a block diagram showing which blocks depend on each other and which are independent, so work can be divided by block. Anton will have capabilities, the diagram and a demo of the prototype ready for tomorrow; it is reviewed in a separate meeting, not in the standup.

**Anton's hardware list for the test boards.** Anton emailed a list of extra hardware for running boards (written by Claude). Pavel's review: a power supply is needed; the USB-A cable is only needed to restore a dead bootloader (board 76 cannot boot from USB or SD, only through that cable); ethernet cables, a gigabit switch and USB-to-serial will be needed; replace the "serial adapter, 2 mm pitch" line with wires or a breakout for the board's extra USB header; add an LTE modem for Georgia with its antenna, a Wi-Fi antenna (the on-board module has none) and a micro SD card. One HDMI monitor and headphones for now. Anton updates the list and sends a follow-up email for purchasing.

**Sound board (Daniil).** Left speaker and subwoofer work, right channel has no sound yet. Pavel's goal: when the sound card loses power and comes back, sound must return to games without rebooting the machine, unlike the old machine.

**Flex-Port / Flex-IQ status.** Alexander finished his last Flex-Port tasks (closing after tests) and started on the Flex-IQ update. Alexey is fixing hardware autotests and may enable the Flex-IQ emulator earlier for tests that need two terminals. Anton Seregin is finishing CORIFE-8 (backend integration, deploying to dev), CORIFE-9 is paused waiting on backend, then reports and CORIFE-11; he will also extend the Flex-IQ emulator so firmware-update packets pass through, for autotests. Sergey confirmed port firmware update through all channels was checked on dev, not on stage.

**Programmer firmware files.** Sergey's firmware dashboard (passports on dev) is missing a download for the programmer. Alexey clarified: the programmer package is the .hex (main application) plus the STLDR helper file; the .bin is not needed. The files and the flashing script are in the artifacts "manual flash" folder; Alexey will hand them to Sergey. Anything can be flashed through the programmer; our signature is only checked after the machine connects to the network.

**Server releases and logs are not MVP1.** Dzmitry proposed, since MVP1 slipped, to optimize the logs going to Grafana and to release all server applications. Pavel: neither goes into MVP1. Dzmitry's order is accounting host first, then a feature for server-service releases, then a feature for log optimization — both in MVP2. Grafana logs on DF CMS work; STG is today.

**Hardware-tracking checkbox.** Sergey: greying out the checkbox for new setups does not help, because technicians reuse existing setups (over 2,100) where the flag is on. Dzmitry proposed a soft-side parameter that forces hardware tracking off for new software whatever the setup says. Pavel: with the flag on, any hardware change sends the machine to the passport scan screen. Irina said from the start the two checkboxes should not have been mixed. Moved to a separate meeting (Pavel, Sergey, Evgeny).

**Modem connect-to-server default.** Pavel's urgent item for Evgeny: connect to our server must be on by default for machines with a modem. Irina: switch it on for everyone, modem or not; it was always on and locked before. Evgeny and Dzmitry: hide the tab entirely. Irina wants the server address to stay editable. Pavel: hide the tab in production, show it on debug machines. Moved to a separate meeting.

**Georgia handpay from tilt dialogs (Ivan, Irina).** Reproduced the field bug: a handpay-pending state raises SAS exception 51 and the host must send 94 or 1B to clear it, which Intralot (heard) never sends, so the signature cannot be computed. Georgia has no handpay (no key, no operator); handpay was removed, but tilt dialogs (CPU overheat, lease and other critical tilts) still have a Collect button that leads into handpay. Options raised: hide Collect for those dialogs in setup, route Collect to printer, port or board instead of handpay (Evgeny), or block cash-out entirely in those cases (Pavel). Ivan: only handpay-pending with exception 51 is confirmed to block counting. Moved to a separate meeting.

**Standup rule.** Pavel: any question that takes more than half a minute goes to a separate meeting. Three such meetings came out of this standup, all with Evgeny.

**Other updates.** Igor profiled Nebraska 2 and removed invisible animations; GCOAM 3 lost a little performance on video, not critical. Evgeny's test stand works and self-updates; next he connects it to the integration repo and merges the two repositories; he will film another competitor game with a phone (help screens, each bonus played through, about 20 games) since a capture card inside a third-party machine is not practical, and a GoPro in a casino is illegal. Irina tests Alexander's finished work and the autotest capabilities. Vladimir is back on autotests; nearly all open ones need cloud services (portal, terminal hub); he shared a document listing which service each scenario needs; a meeting on a test environment with all services may be tomorrow morning (Irina: not a priority). Dmitri Kovalchuk: do not close tasks while the build shows red; rerun the workflow with the same name so Jira sees green, and move dates.

## Decisions Made

- **Anton prepares the engine capability list, block diagram and prototype demo for tomorrow; reviewed in a separate meeting** — one architecture owner, then split by block. (Pavel, Alexander, Anton)
- **Server-application releases and Grafana log optimization are not in MVP1; both become MVP2 features, after the accounting host** — (Pavel, Dzmitry)
- **Programmer firmware package is .hex plus STLDR; no .bin** — (Alexey, Sergey)
- **Standup questions longer than half a minute go to a separate meeting** — (Pavel)
- **Three follow-up meetings today: hardware-tracking checkbox (Sergey, Evgeny), modem connect default (Evgeny), handpay from tilts (Evgeny, Ivan, Irina)** — (Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Anton Leshkevich | Generate the engine capability list, a block diagram of dependencies, and a demo of the prototype | Nov 6, 2026 | High | Separate meeting after standup |
| 2 | Anton Leshkevich | Update the test-board hardware list per Pavel's notes and send the follow-up email for purchasing | TBD | Normal | Power supply, USB breakout wires, LTE modem + antenna, Wi-Fi antenna, micro SD |
| 3 | Alexey Khamin | Give Sergey the programmer files (.hex, STLDR) and the flashing script | TBD | Normal | Artifacts "manual flash" folder |
| 4 | Sergey Tsimanov | Add programmer-firmware download to the Flex-Port firmware dashboard | TBD | Normal | Only the programmer package is missing |
| 5 | Anton Seregin | Extend the Flex-IQ emulator to pass firmware-update packets | TBD | Normal | For autotests |
| 6 | Dzmitry Chudzinau | Grafana logs on STG today; then create MVP2 features for server releases and log optimization after the accounting host | Nov 5, 2026 (STG) | Normal | |
| 7 | Daniil Stauskiy | Fix right-channel sound; make sound recover after sound-card power loss without reboot | TBD | Normal | |
| 8 | Evgeny Kharetski | Film another competitor game with a phone and analyze the mechanics | TBD | Normal | Help screens, bonuses, ~20 games |
| 9 | Pavel Frolov | Hold the three follow-up meetings (Evgeny, then Sergey) after the standup | Nov 5, 2026 | High | |
| 10 | Irina Shishko | Test Alexander's finished Flex-Port work and review the autotest capabilities | TBD | Normal | |
| 11 | Everyone | Do not close tasks with a red build; rerun the workflow and move dates | Ongoing | Normal | Dmitri's email of Nov 4 |

## Open Questions

- How to stop technicians reusing old setups with hardware tracking on — soft-side override or not? (Sergey, Dzmitry) — separate meeting.
- Modem tab: hide it entirely, keep the address editable, or show only on debug machines? (Irina, Evgeny, Pavel) — separate meeting.
- Georgia tilts: hide Collect, redirect cash-out, or block cash-out? Can checksums be computed while a tilt is pending? (Evgeny, Ivan, Irina) — separate meeting.
- When is the meeting on a test environment with all cloud services? (Vladimir) — maybe tomorrow morning.

## Dispatch Log

---
*Processed from Teams transcript on November 5, 2026, 10:10 AM Eastern*
*Source meeting: Daily Standup meeting*
