# Meeting Summary — Daily Standup meeting
**Date:** October 22, 2026, 4:45 AM – 5:19 AM Eastern
**Duration:** ~34 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026]]

## Summary

Held in Russian. Some names, ticket numbers and words are unclear in the transcript and are marked "heard".

**Flex-Port in bill validator mode: cash-out problems.** Pavel described a test run with Flex-Port switched to bill acceptor and pulses mode. Cash-in works: money comes in and is credited. Cash-out has several faults. When the player presses cash-out, the bill acceptor is disabled; the port sees this and the screen shows "out of service". This looks like a serious error. Pavel: rework the message in two languages, something like "cash-in disabled" — a statement, not an error. The screens that show the cash-out amount (for example $70) appear but disappear fast. Irina: they must stay like in normal mode — 30 seconds, with the last 15 seconds asking if the player is still there. After that the screen showed "present your wallet" as for cash-in, not for cash-out. Pavel: the screens are built; the timing logic is broken. Alexander offered to take the fix, since he already works on the port and Flex Pay. Pavel: all these tasks go in project "fort" (heard), assigned to Alexander Biratko. Pavel will first go through the Flex-Port tasks with Irina and set priority; if the work is quick he may do it himself (he thinks about one hour).

**Third-party machines and Elizabeth.** Alexey: today and tomorrow are the last days the third-party machines are in the shop. He asked to at least check that pulses work. Pavel: this was already asked two days ago (heard); Andrei asked Sebastian to do it, but Sebastian and Andrei were not there and nobody knows if Elizabeth or anyone checked. Last night Elizabeth asked for the latest Flex-Port version. Alexey re-checked the earlier mode-switch problem: it works. Pavel: Elizabeth must switch the devices to BV mode in the Flex IQ device menu before delivery. Alexey will write to Elizabeth today and offer help. Pavel: Elizabeth should ask Irina and Alexey first, because they know the latest build. Irina: wait until Alexey checks the new changes and maybe merges them, so Elizabeth gets the latest Flex-Port. Alexey asked to collect good logs while the machines are there. Pavel already collected the list of supported SAS commands during SAS debugging, as interactive artifacts; he will send them to Alexey.

**Games on the new board and a native engine.** Three boards are in play: 3568, 3576 and 3588. 3588 is the most powerful and most expensive; 3576 is mid-price. Pavel: it was decided to stop on 3576 and try to run the games on it. Gennadiy (heard "Gena") was told, through a message from Val (heard), to send both boards; he has a 3568 in stock (the weaker board used for our terminals) and will probably send that. Pavel ran Anton Leshkevich's variant this morning; it is slow, and Anton must optimize it. Daniil now runs two games on the board and switches between them. He is freeing the video decoders to save RAM. Two games, without decoders and rendering, take about 300 MB. With decoders freed, he thinks maybe 6 games could fit in 8 GB, and more with compressed textures. Pavel: at yesterday's meeting Anton proposed dropping the browser and writing our own engine in Rust (heard). It may save about half the memory and other resources. The team will now decide the requirements. Pavel: for this platform there is probably no other way.

**Device registration scenarios (Anton Seregin).** Anton wrote about 4 scenarios in the documentation: registration without internet, mini router, and change of location. They need a review with everyone involved, to decide what goes in MVP-2 and what moves to MVP-3. Example question: a terminal with no registration and no connection, where Wi-Fi will be used — do we need a screen that comes up with Wi-Fi and a hotspot for registration? Some parts can be reused from Lesha's (heard) work. Pavel: build the architecture from the scenarios first, agree on it, then decide which capabilities are really needed. The current capability (a rich mechanism to apply Wi-Fi settings on all devices) may need to be split into smaller ones. Review today with Irina at least, maybe Sergey; Anton also wants Alexander.

**Other updates.**
- Alexander Biratko: working on the differences between Flex-Port work with Flex IQ and with Flex Pay; now tasks 1380 and 1382 (heard). Many remain, for example blocking the Flex-Port on a disconnect (heard). He must talk to Andrei about putting Flex Pay into the update. Yesterday he sent Andrei a new build with the rotated screen; it seems it was not installed. Pavel: nobody was there to install it yesterday; they will install it today.
- Alexey Khamin: mainly SAS launch on hardware (heard). Today he checks Flex-Port work from Alekseev (heard) and will tell him if he can merge. Irina saw pull requests on Flex-Port from Yavorsky (heard) and does not know what they are. Pavel: one PR looks unrelated to current tasks, maybe from two months ago; it is not merged. Yavorsky also asked where to get the new Flex Pay version. Alexey: maybe Val (heard) must be reminded. Pavel closed stale branches from old projects yesterday; he did not touch Flex-Port. Alexey has already rebuilt.
- Anton Leshkevich: writing release notes (heard) for Gennadiy.
- Evgeny Kharetski: much progress on the game agent (heard "GT agent"). It now accepts images as references and math files, saves them to OneDrive, and links math to specific games. You can ask it about RTP. The first version only answered questions on scripts; now it is a full conversation and can help develop an idea, offer options, and produce a final output (heard). Pavel: very promising.
- Irina: corrected requirement 1838 (heard) for printers in Georgia. Felipe reviewed it yesterday and added to it; it is the latest approved version. Evgeny will do it as written. Irina will send it to Evgeny in the chat.
- Irina: she sent the RIS rules requirements to Felipe yesterday. So far he reviewed only 1838. He may still add to or rewrite others, mainly those linked to RIS. The printer one is final; battery and yellow screen are probably clear.
- Ivan Shpak: first said "no change". Pavel: the update is for the PM; "no change" would make it think Ivan can take more work. Ivan works on RIS machine performance and another item (heard). Pavel: Evgeny does the machine side, Sergey the server side.
- Sergey Tsimanov: finished authorization for updates and split it into features. Passport task done; asked if it can be tested on STG. Finishing the printer issue (why the form is not saved). Then he takes the research task on port update. Pavel: yes, take it now — Dima is away until Monday (Irina: 14 days from last Thursday, so Monday). Study what is done, try it with the port; expect changes in the transfer protocols. Pavel: when he tried the file transfer protocol from Flex Pay to Flex-Port, it did not work.
- Dmitri Kovalchuk: many tasks have no due dates; Pavel has 9 overdue. Pavel already reviewed and closed some today. LGS-1042 and LGS-1040 (heard) are open, but their parents are closed. Pavel: they are probably setup-screen tasks for LGS that Vladimir moved to him because the LGS side was not built. Pavel suggested unlinking them, keeping them in the backlog, and later giving them to Evgeny. Irina unlinked them from the parent and said they will come back to it after the capabilities work.
- Pavel: today he sorts out stuck Flex-Port tasks and overdue tasks. Irina will also check that nothing is lost.
- A follow-up meeting is set for 12:30 (time zone not stated); Pavel will send the invite.

## Decisions Made

- **Flex-Port bill validator mode cash-out fixes go into project "fort" (heard), assigned to Alexander Biratko.** The "out of service" message becomes a plain, two-language notice; cash-out screens must stay on screen with the normal timing. (Pavel Frolov, Irina Shishko)
- **Games target the 3576 board.** Reported by Pavel as already decided. (Pavel Frolov)
- **Registration scenarios lead to an architecture first; capabilities are chosen from that architecture.** (Pavel Frolov)
- **Sergey takes the port-update research task now, without waiting for Dima.** (Pavel Frolov)
- **Elizabeth should get the latest Flex-Port build through Irina and Alexey, after Alexey checks the latest changes.** (Pavel Frolov, Irina Shishko)
- **LGS-1040 and LGS-1042 (heard) are unlinked from their closed parent and kept for later.** (Irina Shishko)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Fix the Flex-Port bill validator mode cash-out issues (message, screen timing, wrong "present wallet" prompt) | TBD | High | Who creates the Jira tasks is unclear |
| 2 | Pavel Frolov | Go through Flex-Port tasks with Irina and set priority; sort out stuck and overdue tasks | Oct 22 | Normal | 9 overdue |
| 3 | Irina Shishko | Check that no Flex-Port task is lost | Oct 22 | Normal | |
| 4 | Alexander Biratko | Continue Flex IQ / Flex Pay difference tasks (1380, 1382 heard); talk to Andrei about Flex Pay in the update | TBD | Normal | |
| 5 | Alexey Khamin | Check Alekseev's (heard) Flex-Port work and tell him if he can merge | Oct 22 | Normal | |
| 6 | Alexey Khamin | Write to Elizabeth and offer help setting up BV mode | Oct 22 | High | Last days with third-party machines |
| 7 | Pavel Frolov | Send Alexey the supported SAS commands artifacts | TBD | Normal | |
| 8 | Anton Leshkevich | Optimize his variant; it runs slow on the board | TBD | Normal | |
| 9 | Daniil Stauskiy | Free video decoders and try texture compression to cut RAM use | TBD | Normal | |
| 10 | Pavel Frolov | Review Anton Seregin's registration scenarios with Irina (and maybe Sergey, Alexander) | Oct 22 | Normal | MVP-2 vs MVP-3 |
| 11 | Irina Shishko | Send requirement 1838 (heard) to Evgeny in the chat | Oct 22 | Normal | Printers, Georgia |
| 12 | Evgeny Kharetski | Review the changes in requirement 1838 and build it as written | TBD | Normal | Approved by Felipe |
| 13 | Sergey Tsimanov | Finish the printer form issue, then study and advance the port-update research task | Before Oct 26 | Normal | Dima back Monday |
| 14 | Pavel Frolov | Send the invite for the 12:30 meeting | Oct 22 | Normal | |

## Open Questions

- Who creates the Jira tasks for the cash-out fixes — Alexander, the PM, or Pavel? (Alexander, Irina, Dmitri)
- Did anyone (Elizabeth, Sebastian) check that pulses work on the third-party machines? (Pavel)
- What are Yavorsky's (heard) Flex-Port pull requests, and which Flex Pay version should he use? (Irina, Pavel)
- Which registration scenarios go in MVP-2 and which move to MVP-3? (Anton Seregin)
- Should LGS-1040 and LGS-1042 (heard) go to Evgeny later? (Pavel)
- Felipe may still change other RIS requirements. (Irina)

## Dispatch Log

---
*Processed from Teams transcript on October 23, 2026*
*Source meeting: Daily Standup meeting*
