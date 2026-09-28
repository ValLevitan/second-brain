# Meeting Summary — Transactional MVP1 sync
**Date:** September 28, 2026, 8:02 AM – 8:45 AM Eastern
**Duration:** about 43 minutes
**Attendees:** Andrei Klimovich, Val Levitan, Pavel Frolov, Dzmitry Chudzinau, Irina Shishko, Alexander Biratko, Alexey Khamin, Andrei Bosik
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026]]

Held in Russian.

## Summary

**No private chats.** Dzmitry offered to send Andrei a file of new negative cases and terminal errors for card activation. Val said this must not be a one-on-one talk, and Dzmitry agreed to post it in the common chat. Andrei said Pavel had sent him Wi-Fi QR-code material in a private chat over the weekend, and he will forward it to the common chat. Val asked that there be no private chats. Everyone agreed.

**Card errors and requirements.** Andrei asked the team to send the new tilts and card-related errors to the common chat after the call. He hopes to update the requirements, the errors and the text library by tomorrow's call.

**PIN code (future, not MVP1).** Dzmitry raised a future case: Flex IQ needs no PIN, but Flex Pay does. With two devices at one location, a ticket made without a PIN may need to be redeemed on Flex Pay. Dzmitry proposed that the port always asks for a PIN when a wallet is created. Pavel proposed a hidden fixed PIN (for example 1111), as the current FlexPort already does with the old Flex Pay. Andrei said this is not MVP1. Alexander said it is a technical question, not a business one. No decision. For MVP1, Flex IQ cannot create a ticket with a PIN (confirmed to Alexey).

**Status (Irina).** All MVP1 capabilities and requirements are reworked. All autotest features are created. Alexey and Ivan are writing the tests. Ivan is preparing a document, to be sent tomorrow, on how to set up the machine and port for SAS in Georgia. Vladimir joins autotests from Wednesday for about 8 days, then goes on vacation. With him, autotests finish about **October 23**, but Irina needs a couple of days to judge the real speed.

**Release date.** Val said this means MVP1 cannot ship before October 23. Pavel said a trial batch of about 10 locations could go out earlier, if remote update of Flex IQ works. Val confirmed MVP1 starts with Flex IQ installs only, not Flex Pay.

**Remote FlexPort update moved into MVP1.** Earlier the plan was to update Flex IQ remotely in MVP1 but FlexPort only in MVP2 (by USB stick on site). Pavel said that with MVP1 now at October 15, FlexPort remote update can also be done by then. Andrei agreed, and said honestly October 15 is the real date, not October 1. Val agreed to add it to MVP1 (capability 146). Pavel offered to take the firmware-delivery story PORT-13 from Alekseev, who works only on weekends. Val said to leave it with Alekseev. Pavel is waiting for the RK3576 board this week.

**Wi-Fi.** Alekseev did only the hardware. Pavel is doing the Wi-Fi software and says it is about 90% done. It stays in MVP2 (capability 145).

**Repository.** Val asked if the work follows the repository standard. Pavel said yes: the Flex-Port platform repository holds the code, prose and contracts. He said Claude finds and fixes bugs while updating the prose.

**Remote update of Flex IQ in Georgia.** Andrei suggested testing remote update on the Flex IQ in Georgia that has remote access and a KORE SIM. Dzmitry said older terminals cannot be updated remotely. They must first get the new software by SD card, and will likely ask to re-register because of new certificates. After that, remote updates work. Dzmitry showed the terminal management dashboard: an Updates tab with the device list (OS and app versions), builds (SD installers), and update campaigns with per-terminal status. New builds come out daily. Install the latest build. Dev, staging and prod are separate; a staging terminal can move to prod only by SD card. Alexey suggested installing the previous build, then updating remotely to the newest. Dzmitry will check with Sergey whether Elizabeth needs a role to download builds. Andrei will ask Elizabeth to install the build by SD card and report back.

**Brackets.** Val remembered that FlexPorts need mounting brackets for other makers' machines (for example Aristocrat). Val will take this on and asked to be reminded.

**Flex Pay updates.** Alexander said the server has no update support for Flex Pay yet, which blocks him. Dzmitry said this will wait until MVP1 is closed; it is a future capability, with a Flex Pay tab next to Flex IQ.

**Val's request.** Val asked the team to finish autotests and reach final state by **October 15** if possible; 95% done would be fine. Irina said she needs a couple of days to judge. Val noted the tests are written with Claude, so the current estimates are likely conservative.

**MVP2.** Alexander said MVP2 capabilities are rough and nobody is working on them. Andrei agreed they are out of date and need a business scope first. Andrei returns on the 12th and will then work on MVP2; he cannot promise much before that. Alexander will collect business questions (example: a card is dispensed but the player does not take it) and bring them to these calls. Val said longer-term topics go by email, urgent ones by chat. Irina asked that they stay in one email thread, not separate emails.

**Emulators.** Alexey asked who builds emulators for testing. Irina said Anton. Anton made a card dispenser emulator inside Flex Pay and should move it to Flex IQ.

## Decisions Made

- **No private chats for project work** — work material goes to the common chat. (Val; agreed by all)
- **Remote FlexPort update is added to MVP1** — MVP1 date is now October 15, so there is time. (Val, with Pavel and Andrei)
- **PORT-13 (firmware delivery to FlexPort) stays with Alekseev** — Pavel offered to take it; Val declined. (Val)
- **MVP2 business questions go by email, in one thread, and are raised on these calls.** (Val, Andrei, Irina)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dzmitry Chudzinau | Post the card-activation negative cases and terminal errors file in the common chat | Sep 28, 2026 | High | Val said no one-on-one |
| 2 | Andrei Klimovich | Forward Pavel's Wi-Fi QR-code material from private chat to the common chat | Sep 28, 2026 | Normal | |
| 3 | Andrei Klimovich | Update MVP1 requirements with new errors and the text library | Sep 29, 2026 (tomorrow's call) | High | "good chance" |
| 4 | Ivan | Send the document on setting up the machine and port with SAS commands in Georgia | Sep 29, 2026 | Normal | Reported by Irina |
| 5 | All (autotest team) | Finish autotests and reach final state by Oct 15 if possible (95% is fine) | Oct 15, 2026 | High | Val's request |
| 6 | Irina Shishko | Re-estimate the autotest finish date after a couple of days | ~Sep 30, 2026 | Normal | |
| 7 | Dzmitry Chudzinau | Check with Sergey which role Elizabeth needs to download builds from the dashboard | TBD | Normal | |
| 8 | Andrei Klimovich | Ask Elizabeth to install the latest build by SD card on the Georgia Flex IQ, then report back so remote update can be tested | TBD | Normal | Dzmitry needs terminal numbers |
| 9 | Val Levitan | Arrange FlexPort mounting brackets for other makers' machines (e.g. Aristocrat) | TBD | Normal | Asked to be reminded |
| 10 | Alexander Biratko | Collect MVP2 business questions and send them by email in one thread; raise them on these calls | Ongoing | Normal | |
| 11 | Andrei Klimovich | Bring MVP2 capabilities and business scope up to date | After his return on the 12th | Normal | |
| 12 | Anton | Move the card dispenser emulator from Flex Pay to Flex IQ | TBD | Low | Not present; reported by Pavel |

## Open Questions

- PIN code design for Flex Pay when two devices are at one location: always ask for a PIN on the port, or use a hidden fixed PIN (Dzmitry vs Pavel). Not MVP1.
- Whether autotests can move from October 23 to October 15 (Val, Irina).
- Whether Alekseev can finish PORT-13 in time (Pavel).

## Dispatch Log

---
*Processed from Teams transcript on September 28, 2026 (meeting-watcher)*
*Source meeting: Transactional MVP1 sync*
