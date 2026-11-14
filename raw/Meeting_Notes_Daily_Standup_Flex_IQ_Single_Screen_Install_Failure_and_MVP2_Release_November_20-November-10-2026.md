# Meeting Summary — Daily Standup meeting
**Date:** November 10, 2026, 6:15 AM – 6:46 AM Eastern
**Duration:** ~31 minutes (25 minutes of talk)
**Attendees:** Dmitri Kovalchuk (ran the round, Pavel absent), Irina Shishko, Daniil Stauskiy, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Dzmitry Chudzinau, Evgeny Kharetski, Igor Metelski, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026]]

## Summary

Pavel was absent; Dmitri Kovalchuk ran the round.

**Sound in memory (Daniil).** Finished sound tasks 4 and 5 (heard); NENG-26 passed to him. Long sounds took too much RAM, so each sound is now a FLAC file: anything over three seconds loads only its first second into memory and the rest streams from disk. Checked on the board: no gaps, loops do not break. RAM dropped from about 400 MB to 35 MB. Engine-to-LGS link: only a thin layer is needed. Anton: define which messages the engine handles so they do not go to the presentation layer. Volume change: Alexander and Anton agreed the script calls a change-volume API and the engine core itself tells LGS, which stores the value; the websocket stays for feedback. FRAM-1496 (sound drop on LGS) does not reproduce and sound no longer goes through LGS; Irina: close it as rejected with the reason.

**Alexander Biratko.** FPORT tasks (224 heard) nearly final, part already merged, still testing. Irina: once the port is rebuilt she can run tests on a newer build, and the latest main can now go on the IQ. Next FPORT-26/27 (heard). In parallel he moves all Flex-Pay changes to the Flex-Recycler, which turned out fairly current. Done: the Flex-Pay update through our app works. Irina asks him to review CAP-368 features (FPORT-169) and say if work is still needed. Validator screen bug: Irina waits to check on the IQ, which was busy with the production update.

**Flex IQ production install (Alexey, Dzmitry).** Yesterday Alexey and Dzmitry installed production on the Flex IQ and found the install fails with one monitor. Dzmitry: at the hardware level, if the second HDMI screen is not connected, the board treats it like an unmounted SD card: the installer fails, and if the screen is not connected at the start the board boots but raises no network interface, a black box. Pavel made a fix, but after talking to Andrei Klimovich the fix is not applied now: release with two screens connected and discuss later. If it is a board defect, all boards from China can be installed only with a second screen or a plug. Alexey continues hardware autotests and rebuilds the Flex-Port; Irina: write the MVP 2 tests whenever free.

**Irina.** Keeps sorting the MVP 2 capabilities (Andrei updates requirements), writes test stories for the MVP 2 requirements. **MVP 2 release is November 20.**

**Anton Leshkevich.** Yesterday: security updates for the engine (GitHub found about ten vulnerabilities in libraries). He scrapes the internet for slot mechanics so the framework supports as many as possible. Igor: this overlaps with Evgeny's video analysis; Igor and Anton call right after the standup. Dmitri: the agent created a draft task for Anton to accept or reject.

**Anton Seregin.** Closed CORIFE-10, checked on the phone; terminal interaction that Sergey built works. The firmware accumulator PR is open; he rechecks, closes, then looks at the autotests and whether the scenarios are current.

**Dzmitry Chudzinau.** Statistics export: comparing with the board so the numbers match; if good, closes the tasks today and emails how to check. The same deploy carried Sergey's lease and passport changes, to be rechecked. With Andrei Bosik the graph logic is done; he checks what else can be sent. Irina: new MVP 2 capabilities are all on him and sit without features; he takes them after the board, may hand some out.

**Evgeny Kharetski.** RIS improvements MVP 1 fixes with the agent, a couple of NOVA commits; the SAS tool is done, it grows with needs. He loads Dmitri's new standards into Claude and starts the LTE modem switch-off capability. Irina: who does the server side, Sergey or Dzmitry, and when? Release plans were November 16, so it must be done now; MVP 2 (Transactional) is due by the 20th too. Dzmitry: plan testing right away, his hands do not reach the server. Irina: testing depends on when it is built.

**Igor Metelski.** Fixed gamble in Black Seal for Dakota (GLI remark), now the gamble for Cool Cat (heard); fixed the GLI remark on game recovery; committed. Nebraska work; moved his web animation tools to NOVA 2.

**Ivan Shpak.** Waits for Igor's game fixes, rebuilds and checks, then builds with Evgeny's changes; checks the modem work when ready. Needs a fix from Pavel: tickets print empty when the machine boots; wrote to Pavel, expects it tomorrow.

**Sergey Tsimanov.** Finished the port firmware on the portal; now the QR task for Wi-Fi registration.

**Vladimir Samusenko.** TINT-105 took long; security items are moved to the future, not MVP 1 or MVP 2. With Irina a new capability CAP-370 describes terminal and port behaviour with several terminals and a master; the master-switch and multi-terminal scenarios move under it. Finishing TINT-105.

**Dmitri Kovalchuk.** Sent the new version of the standard as a draft; comments welcome. The Knowledge repository gets many updates and is now the place where team information lives; watch it.

## Decisions Made

- **Long sounds: first second in memory, the rest streams from disk** — RAM 400 MB to 35 MB. (Daniil)
- **Volume change: the script calls a change-volume API and the engine core tells LGS, which stores the value** — (Anton Leshkevich, Alexander, Daniil)
- **FRAM-1496 is closed as rejected: sound no longer goes through LGS** — (Irina, Daniil)
- **Flex IQ single-screen install: no installer fix now; release with two screens connected** — passed on from Pavel after talking to Andrei Klimovich. (Dzmitry)
- **MVP 2 release date is November 20** — (Irina)
- **TINT-105 security scenarios move to the future, not MVP 2** — (Vladimir, Irina)
- **Master-switch and several-terminal scenarios go under CAP-370** — (Vladimir)
- **The Knowledge repository is the place to keep team information** — (Dmitri Kovalchuk)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Daniil Stauskiy | Close FRAM-1496 as rejected with the reason | TBD | Low | |
| 2 | Alexander Biratko | Review CAP-368 features (FPORT-169) and say if work is still needed | TBD | Normal | Irina reassigns |
| 3 | Alexander Biratko | Finish and rebuild the port so Irina can test on the newer build | TBD | Normal | |
| 4 | Alexey Khamin | Rebuild the Flex-Port; MVP 2 tests when free | TBD | Normal | |
| 5 | Anton Leshkevich | Call Igor after the standup to avoid overlapping work; accept or reject the agent's draft task | Nov 10, 2026 | Normal | |
| 6 | Anton Seregin | Recheck and close the firmware accumulator PR, then review the autotests | TBD | Normal | |
| 7 | Dzmitry Chudzinau | Check the statistics export against the board, close the tasks, email how to check | Nov 10, 2026 | Normal | |
| 8 | Dzmitry Chudzinau | Review the new MVP 2 capabilities on him and hand out work | TBD | High | They sit without features |
| 9 | Evgeny Kharetski | Start the LTE modem switch-off capability | TBD | High | Release was planned Nov 16 |
| 10 | Pavel Frolov | Fix tickets printing empty when the machine boots | Nov 11, 2026 | Normal | Ivan wrote to him |
| 11 | Irina Shishko | Check the validator screen bug on the IQ | TBD | Normal | |

## Open Questions

- Flex IQ boards from China fail install with one screen: board defect or a workaround with a plug? (Dzmitry, Irina)
- Who does the server side of the LTE modem switch-off, Sergey or Dzmitry, and when? Release on the 16th needs it now. (Irina)

## Dispatch Log

---
*Processed from Teams transcript on November 10, 2026, 7:40 AM Eastern (scheduled meeting-watcher)*
*Source meeting: Daily Standup meeting*
