# Meeting Summary — Daily Standup meeting
**Date:** October 23, 2026, 4:49 AM – 5:37 AM Eastern
**Duration:** ~48 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026]]

## Summary

Held in Russian. Some names, ticket numbers and words are unclear in the transcript and are marked "heard".

**Flex-Port testing on the third-party machines in Atlanta — top priority today.** Alexey: today is the last normal day the third-party machines are in Atlanta, and the people there will do nothing unless told. Pavel: priority number one is the ports. Alexander should merge his Flex-Port work into main and release it. Pavel will look at PORT-138 (heard) and maybe merge it too. Then the team gives the build to the site to test the mode. A release build (RC) of Flex IQ is also needed; Pavel adds nothing more to it. Irina: for the bill validator mode nothing changed on IQ, so the current IQ should work and only the port needs to be installed. Andrei and Sebastian should be on site today. Test from all sides.

**When to block the bill validator (BV mode).** Alexander works on PORT-162, 163 and 164 (BV mode messages). He now shows "cash-in disabled" when, for example, the door is opened. Question: when does "out of service" still show? Pavel: for errors of Flex-Port's own devices (for example the scanner) and for connection problems with Flex IQ / Flex Pay. In BV mode the port can only read the BV enable/disable signal, and the only way to stop the machine is to block the bill acceptor; the machine keeps playing. Alexander proposed: any port problem blocks the bill validator, or money is taken and not processed. Pavel was not sure and said not every "out of service" should block it; he suggested asking Andrei. Irina then checked the requirements (with Claude, during the meeting): **the bill validator is blocked only when the port is locked from the IQ side ("locked by host"). If the connection is just lost, the screen shows "out of service" and the bill validator stays available.** Irina has new autotests for this. Pavel accepted ("good, clear"). Pavel also named a case to check in autotests: if the port is blocked because the location is blocked, the device must unblock. Alexey checked this about 3 weeks ago.

**Georgia machines and the Intralot checksum email.** Irina raised an Intralot email: machines in Georgia sometimes send something wrong; the email also mentions the bill validator and handpay. Sebastian should open a ticket. Pavel's guess: Intralot asks for a checksum while the game is busy, and the machine does not answer within 2 minutes. Ivan: the only checksum request he knows is SAS 21 (ROM signature); it takes very little time even during play, and the team already checked it. Evgeny also knows only 21. Pavel: in the past a whole partition was hashed and that was slow; now only one binary file is. So it is not clear where the problem is. Irina sent the email thread to Evgeny, Ivan and Sergey. Sergey will try to find which machine is at the address given (by coordinates). Pavel will re-read the email. Who works on it (Pavel or Evgeny) is not decided.

**Remote firmware update for Flex-Port (MVP-2).** Sergey finished his printer task and the spike. Pavel: his next part is delivering firmware from Flex IQ to Flex-Port. Alekseev (heard) works on the update itself on the port side. Pavel split the work in three: deliver the firmware to Flex IQ; deliver it from Flex IQ to Flex-Port; and a protocol where Flex IQ tells the port, when it connects, that new firmware is waiting. The port asks Flex IQ for the file, not the other way. Dima built an older file transfer protocol in Flex Pay; when Pavel tried it, only part of the transfer worked. It needs a full review. Irina: this is MVP-2, not MVP-1. Pavel and Irina agreed to split CAP-146: the USB update part stays separate from the remote update. PORT-131 (heard) sits in an MVP-1 capability and is blocked; Alexey should check it.

**Flex-Port firmware size.** Alexey: in Alekseev's (heard) branch the update binary dropped from about 65–70 MB to 14 MB. The partition size is set to 14 MB so the GUI fits; it now uses about 8.5 MB. Pavel: good, 4 times less to transfer. Next for Alekseev: run our latest Flex-Port build with the Flex IQ emulator and confirm Wi-Fi works; then remote update. Alexey noticed the LEDs do not blink during an update. Pavel: do not load Alekseev with this now; the team can add it later.

**Engine and games.** Daniil updates dependencies and converts textures. Decoding video only when entering a game: one game (heard "Cover Fortune") takes about 2 seconds, another about 10 seconds, which is too long. RAM may be enough for about 8 games; CPU and GPU will be the limit. Pavel: the game ran on a board with 4 GB, with a large reserve. Pavel will share in the chat the list of improvements made for the Rust implementation. Alexander: decide whether Daniil keeps working on the browser version, and if not, what new-framework tasks he gets. Pavel agreed; Daniil can help define what the new engine needs. Pavel: give Daniil the transcript of the earlier meeting (Pavel, Alexander, Anton, Zhenya, Val) so he knows what was discussed.

**Other updates.**
- Pavel: last night he finished the Flex IQ fixes, mainly modem and network cases found by Vladimir (ticket heard "35 608"). All committed to main. To build, first build and reset the system, then rebuild Flex IQ (heard). Today he closes overdue Flex-Port tasks.
- Alexey Khamin: making tests run with simulators. Tests that use the printer need a printer simulator in the IQ emulator, or instructions; this depends on Anton. Flex-Port update passes for him; he will run the main games, then tell Alekseev he can merge.
- Anton Leshkevich: wrote many requirements and asked where to put them online. Pavel: in the docs folder of the NOVA project repo (project name unclear in transcript), maybe in a "for review" subfolder; everyone adds there, then the team merges and discusses.
- Anton Seregin: redrew the registration scenarios from the earlier meeting and sent the docs. Andrei asked to rename "kiosk" to "terminal" in the emulator images. He is moving Jira items so the Flex-Port firmware capabilities can close. Emulation will be a separate task after the real product is done.
- Evgeny Kharetski: three projects. The game agent will be ready by Saturday: it is a game assistant that answers questions on game documents and math and creates game briefs. Waiting for information from Irina on a tab (heard "titles"). LGS integration: pull requests now run autotests in the integration repo, and results show in the PR. Merge blocking on main is not on yet; Evgeny and Andrei will run it for 2 weeks first. He is adding Progress (heard) and wants to run only tests for changed and nearby features, maybe via the Anthropic API.
- LGS and services: the latest LGS works with IO board, counter board, printer and BV services. Some old hardware-access code (heard) may still be in use, for example checksum checks. Evgeny: the goal is to remove it fully; Anton split part of it out earlier. Pavel: analyze what is left.
- Irina: the Sunday meeting at 3:00 (time zone not stated) still stands. Felipe went quiet after reviewing one requirement. All RIS requirements (about 6 capabilities) are rewritten; Evgeny should check that all are done to their latest state, without waiting for Felipe. Irina will ping Felipe today.
- Ivan Shpak: continues RIS. Update end dates on overdue tests (heard "15/21"). Irina asked him to recount the test plans against the latest requirements.
- Dmitri Kovalchuk: some people ignore due dates; he will message each person privately with their tasks.

## Decisions Made

- **The bill validator is blocked only when the port is locked from the IQ side; on a lost connection the screen shows "out of service" and the bill validator stays available.** — This is what the requirements say; Irina checked them during the meeting. (Irina Shishko; Pavel Frolov accepted.) Considered and superseded: Alexander's rule "any port problem blocks the bill validator".
- **Priority today: test Flex-Port on the third-party machines in Atlanta.** Alexander merges and releases Flex-Port; a Flex IQ RC build is made. (Pavel Frolov)
- **CAP-146 is split: USB update separate from remote update (MVP-2).** (Pavel Frolov, Irina Shishko)
- **Anton Leshkevich's requirements go in the docs folder of the NOVA project repo, maybe in a review subfolder.** (Pavel Frolov)
- **LED blinking during update is not given to Alekseev now.** (Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Merge Flex-Port work into main and release it for the Atlanta test | Oct 23 | High | Last day with third-party machines |
| 2 | Pavel Frolov | Review PORT-138 (heard) and merge to main if ready | Oct 23 | High | |
| 3 | [Unassigned — needs clarification] | Make a Flex IQ RC release build | Oct 23 | High | Pavel adds nothing more |
| 4 | Pavel Frolov | Close overdue Flex-Port tasks | Oct 23 | Normal | |
| 5 | Sebastian | Open a ticket for the Intralot Georgia checksum email | TBD | Normal | Named by Irina; not at the meeting |
| 6 | Pavel Frolov | Re-read the Intralot email and decide who handles it (him or Evgeny) | TBD | Normal | |
| 7 | Sergey Tsimanov | Find which machine is at the address in the Intralot email | TBD | Normal | Irina sends the address |
| 8 | Sergey Tsimanov | Work on firmware delivery Flex IQ → Flex-Port; fully review the old Flex Pay transfer protocol | TBD | Normal | MVP-2 |
| 9 | Irina Shishko | Split CAP-146 into USB update and remote update | TBD | Normal | |
| 10 | Alexey Khamin | Check PORT-131 (heard): what it says and when it can close | TBD | Normal | Blocks an MVP-1 capability |
| 11 | Alexey Khamin | Run main games on Flex-Port, then tell Alekseev he can merge | Oct 23 | Normal | |
| 12 | [Unassigned — needs clarification] | Ask Alekseev to run our Flex-Port build with the Flex IQ emulator and confirm Wi-Fi | TBD | Normal | Next step: remote update |
| 13 | Pavel Frolov | Share in the chat the Rust implementation improvements list | Oct 23 | Normal | |
| 14 | [Unassigned — needs clarification] | Give Daniil the transcript of the earlier engine meeting; decide his next tasks | TBD | Normal | Browser version may stop |
| 15 | Anton Leshkevich | Put his requirements in the NOVA repo docs folder | TBD | Normal | |
| 16 | Evgeny Kharetski | Check all RIS requirements are done to their latest state | TBD | Normal | Do not wait for Felipe |
| 17 | Irina Shishko | Ping Felipe on the RIS requirements | Oct 23 | Normal | |
| 18 | Ivan Shpak | Update end dates of overdue tests; recount test plans for the latest requirements | TBD | Normal | |
| 19 | Dmitri Kovalchuk | Message each person privately about their overdue tasks | TBD | Normal | |
| 20 | Evgeny Kharetski | Finish the game agent | Oct 24 | Normal | "By Saturday" |

## Open Questions

- What is really wrong on the Georgia machines in the Intralot email? SAS 21 is fast, so the 2-minute checksum theory does not fit. (Pavel, Ivan, Evgeny)
- Who owns the Intralot issue — Pavel or Evgeny? (Irina)
- Does Alekseev's side expect a file push or a pull for the firmware transfer? Pavel says the port pulls. (Sergey)
- Should Daniil stop the browser version, and what does he do next? (Alexander)
- What old hardware-access code is still used by LGS, and where does it move? (Pavel, Evgeny)
- How should printer tests run in the IQ emulator? (Alexey)

## Dispatch Log

---
*Processed from Teams transcript on October 23, 2026*
*Source meeting: Daily Standup meeting*
