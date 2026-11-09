# Meeting Summary — Daily Standup meeting
**Date:** November 6, 2026, 6:15 AM – 6:45 AM Eastern
**Duration:** ~29 minutes
**Attendees:** Pavel Frolov (host), Irina Shishko, Alexey Khamin, Ivan Shpak, Dmitri Kovalchuk, Igor Metelski, Evgeny Kharetski, Daniil Stauskiy, Alexander Biratko, Anton Leshkevich, Anton Seregin, Dzmitry Chudzinau, Sergey Tsimanov, Vladimir Samusenko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026]]

## Summary

**Sound on the RK3576 board (Daniil).** Sound now plays on two speakers through the new library, but quietly. The amplifier itself works. Daniil can boost the signal in PulseAudio but does not know whether the amplifier should do that instead. Pavel: on the old Flex cabinets a master volume slider sat at about 85%. The old crash (sound card dropped when another board was unplugged) looks fixed: Daniil pulled the USB and power from the sound board and sound came back on reconnect. Pavel: that is what we need. One old case cannot be fixed fully: a too-loud start could overload the amplifier, the USB device disappeared and only a reboot brought it back. Pavel wants to think about detecting an audio-path shutdown from overload and reinitializing it; without the USB device nothing can be done, unless an external watchdog.

**Flex-Port update (Alexander).** Checked the Flex-Port update through the Flex-IQ: data goes through and the port flashes. Left: check the port itself on dev. Then he creates the Flex-Recycler integration tasks and moves to them. He needs the recycler library sources; Pavel downloaded them from a link and will give them to him.

**Hardware autotests (Alexey).** Full run done: about 66% start and pass, about 30% do not start yet. Some failures are real bugs that must go into the tests. Irina: the port tests need periodic fixes because requirements changed. Alexey fixes small things himself, otherwise finds the author.

**Engine prototype (Anton Leshkevich).** Reached the point where the scenario plays end to end: the studio agent takes a Jira ticket, pulls the resources and adds a new game to the platform automatically. He sent a status video. Until the next meeting he does refactoring and bug fixes.

**Anton Seregin.** CORIFE-8 closed yesterday and checked with the server. CORIFE-9 is close and should close today. He also took the firmware emulation feature (number heard as 81) with its stories: emulation, tests, documentation.

**Dzmitry.** Working with Andrei on the move to the new stack (heard as Rust).

**New capability — confirmed machine actions (Pavel).** Pavel will create the capability discussed with Dzmitry: some actions on a game machine, for example switching the modem off, must go through a procedure. Either the server is told over the network that the modem is being switched off in settings, or, if the server is unreachable, through a QR code and a 4-character activation code, as was done for the lease. The capability covers both the CMS server side and the machine side.

**Evgeny.** RIS work goes back and forth; RIS improvements move forward. The autotest stand reached what was wanted and is now being extended. Video analysis: one game recorded with the capture card (no bonuses, that machine had no show mode) and one filmed on a phone yesterday. Claude parsed the phone video well; quality suffered because it went through Telegram and some help text was misread. With the original file it should be much better. He has three artifacts for the teardown meeting: the capture-card game analysis, the phone-video game analysis, and a note on phone-recording drawbacks.

**Igor.** Nebraska 2: inserting designer resources as they arrive; made a feature for another game yesterday.

**Irina.** Keeps running the port tests and fixing them; sorting the capabilities, features and requirements for MVP 2: what can be automated and what is missing. Pavel pointed to two requirement drafts; Irina takes them (all requirements now go to her).

**Ivan.** RIS and CMS review with Evgeny continues. Today he checks that RIS is saved when Georgia machines run different software (earlier it was not saved; a fix was made but never verified; critical). Evgeny wrote that exception 51 is fixed; Ivan will rebuild his own machine to verify it (not the vertical one, the port is on it).

**QR code and the updates banner (Sergey).** QR generation on the web-services side is done; next is the Flex-IQ side and passing it to the terminal hub. This morning Andrei Klimovich wrote that the updates banner was visible to customers on prod because the feature had no authorization when deployed; Sergey fixed it before the deploy today. The Flex-Port view is deployed on STG; Alexey has not checked it yet. A QR can be generated on dev but cannot be applied anywhere yet: the port needs parsing code, and the Flex-IQ side is not done.

**Autotests waiting on the MVP2 build (Vladimir).** Took TIN-105 and TIN-111 (heard). TIN-111 has Wi-Fi tests on the IQ, but the build on machine 84 is MVP1 and has no Wi-Fi yet. He is waiting for information on the cloud services needed for testing and takes no other tasks. Irina asked which cloud services MVP2 needs for Flex-IQ and Flex-Port; Vladimir: almost all. Pavel: MVP2 new work is what Sergey does now (location manager, terminal hub). The Wi-Fi work on Flex IQ is committed: Linux changed to support the module, access-point mode works, the connection script changed. It has nothing to do with QR reading from a phone, which is not done yet. Pavel offered his Flex IQ for testing. Irina: once Alexey's run finishes, update the Flex IQ to the new build; the old tests must still pass.

**Remote updates meeting.** Pavel: Vladimir is invited to today's 4:00 meeting on remote updates for NOVA.

**Pavel.** SDK for the RK3576: the main functionality is done. In free time he will try to flash all components to eMMC so the board is fully ready with our images.

**Jira report (Dmitri Kovalchuk).** Showed the report: it never looked this good. Leaving out Alexey's tasks and Andrei Khandov, all dates are set. Also: Pavel asked the agent for a capability, but the agent cannot create capabilities yet, only comments, requirements and features.

**Which capabilities belong in MVP 2 (Irina, Sergey).** Irina wants to avoid creating features for test capabilities that are not in MVP 2, naming CAP-287. Sergey explained CAP-287: the QR shown on the phone is read and decoded by the port, which then connects; plus a button in the Flex IQ setup that gives the QR to any user. Pavel: the QR work is a precondition for Wi-Fi setup. Conclusion: CAP-287 goes fully into MVP 2. Irina will sort out the others (CAP-145, Wi-Fi link, location board module).

## Decisions Made

- **CAP-287 (QR and Wi-Fi delivery to the Flex-Port) is fully in MVP 2** — the QR flow is a precondition for Wi-Fi setup. (Sergey, Pavel, Irina)
- **Pavel creates a capability for confirmed machine actions (e.g. modem off): server notification, or QR plus 4-character activation code when offline; covers CMS and machine** — (Pavel)
- **Vladimir joins today's 4:00 remote-updates meeting for NOVA** — (Pavel)
- **After Alexey's hardware test run, the test Flex IQ gets the new MVP2 build; old tests must still pass** — proposed by Irina, no objection. (Irina)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Check the Flex-Port update on dev, then create the Flex-Recycler integration tasks | TBD | Normal | Gets the recycler library sources from Pavel |
| 2 | Pavel Frolov | Give Alexander the recycler library sources | TBD | Normal | Downloaded from a link |
| 3 | Alexey Khamin | Get the remaining ~30% of hardware autotests to start; fix small port-test issues himself | TBD | Normal | |
| 4 | Alexey Khamin | Check the Flex-Port view Sergey deployed on STG | TBD | Normal | Asked by Irina; Alexey said not checked yet |
| 5 | Anton Seregin | Close CORIFE-9 today, then the firmware emulation feature | Nov 6, 2026 | Normal | |
| 6 | Pavel Frolov | Create the capability for confirmed machine actions (modem off via server or QR + activation code) | TBD | High | CMS and machine sides |
| 7 | Irina Shishko | Take the two requirement drafts Pavel flagged; decide which capabilities (e.g. CAP-145) are not needed in MVP 2 | TBD | Normal | |
| 8 | Ivan Shpak | Verify RIS is saved when Georgia machines run different software | Nov 6, 2026 | High | Critical, never verified |
| 9 | Ivan Shpak | Verify Evgeny's exception 51 fix on his own machine | Nov 6, 2026 | Normal | Rebuild his machine |
| 10 | Sergey Tsimanov | Flex-IQ side of the QR flow and hand-off to the terminal hub | TBD | Normal | Web-services side done |
| 11 | Vladimir Samusenko | Run the TIN-111 Wi-Fi tests once the MVP2 build is on the test IQ | TBD | Normal | Waiting on build and cloud services |
| 12 | Pavel Frolov | Invite Vladimir to today's 4:00 remote-updates meeting | Nov 6, 2026 | Normal | |
| 13 | Pavel Frolov | Flash all RK3576 components to eMMC from JVL images | TBD | Low | Free time |
| 14 | Daniil Stauskiy | Sort out the quiet sound on the RK3576 (PulseAudio boost or amplifier) | TBD | Normal | See open question |

## Open Questions

- Quiet sound on RK3576: boost in PulseAudio or should the amplifier do it? (Daniil)
- How to detect an amplifier overload and reinitialize the audio path without the USB device? (Pavel)
- Which cloud services do the MVP2 autotests need for Flex-IQ and Flex-Port? (Irina, Vladimir)
- Which capabilities, such as CAP-145, are not needed in MVP 2? (Irina)
- Irina proposed moving the standup 15 minutes earlier; not settled.

## Dispatch Log

---
*Processed from Teams transcript on November 6, 2026, 10:05 AM Eastern (scheduled meeting-watcher)*
*Source meeting: Daily Standup meeting*
