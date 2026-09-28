# Meeting Summary — Transactional MVP1: CAPs, REQs, UI/UX
**Date:** September 23, 2026, 8:00 AM – 9:18 AM Eastern
**Duration:** About 1 hour 16 minutes
**Attendees:** Andrei Klimovich, Pavel Frolov, Irina Shishko, Val Levitan, Dzmitry Chudzinau, Andrei Bosik, Alexander Biratko, Alexey Khamin, Ivan Shpak
**Raw transcript:** [[Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026]]

## Summary

**Product package for UI/UX is in Jira.** Andrei Klimovich created two capabilities, 234 for Flex IQ and 235 for FlexPort. Each holds the mockups, the text library and the requirements that describe the screens. He wrote them in a technical style so Claude can work from them. One limit: Claude's Jira connection cannot download attachments by itself, so he put a note inside each capability telling Claude to ask a person to download the attachment and feed it in. He owns keeping the mockups and the text library current, updating the capability text when they change, and telling the team.

Dzmitry asked Andrei to put a date in mockup file names so versions can be compared. Pavel said JVL already has a file-naming standard in the repository and will send the link. Andrei agreed to use it.

**Requirements clean-up.** Irina walked the group through about 12–15 requirements that carried open questions.

- REQ-753 mixed FlexPort, SMIB, Pay and IQ in one text and added nothing new. Andrei first proposed moving it to the MVP2 backlog. Val said that builds a graveyard. Dzmitry said the requirement is abstract and not a product requirement. It was deleted during the call.
- Several requirements (1560, 1561 and about four more) were missing exact timeout values for device disconnects — SAS, bill validator, QR scanner, WS, and the Flex IQ to FlexPort link. Alexander Biratko explained the SAS specification governs the machine, and JVL runs as the host, so if the SAS link is lost the port cannot continue. Pavel proposed dropping fixed times altogether: when the link to any device drops, show it on the player screen as fast as possible and keep retrying to find the device. The group accepted that wording.
- Open questions inside a requirement are not a blocker. Dzmitry and Andrei agreed some answers only appear once work starts. The rule is that no open question may still be open when the task is finished.
- CAP-173 was marked Complete while its requirements were still active. It goes back to In Progress. Pavel will review requirements 1560, 1563 and 1565 under it, add the engineering answers, then move them to Accepted.
- REQ-1413 (CAP-144) covers moving a FlexPort from one device to another. Dzmitry explained one screen shows active FlexPorts and those present on the network, and an active one can be switched between devices. Pavel thought this was MVP2; Dzmitry said it is useful in development, at trade shows and in production. Georgia allows 9 machines, so 9 FlexPorts maximum; the default is set to 20 for headroom. The real ceiling is server capacity and needs a separate stress test.
- REQ-1603 asked what happens when the external channel drops. Dzmitry said buffering already works — Fluent Bit with a default buffer of roughly 500 MB, which sends everything once the link returns.
- REQ-1429 asked how many wrong PIN attempts before lockout. Andrei Klimovich ruled there is no lockout on Flex IQ.
- A requirement about gateway reporting time does not fit MVP1. Dzmitry said FlexPort only sends logs and transactions to Grafana; there is no cloud view of connected FlexPorts and their problems in MVP1. Alerts can be built in Grafana.
- REQ-1550 (external traffic protection) stays in MVP1 because the terminals face the internet, and it needs an ADR in the repository. Pavel said the text is so long that a person cannot read it. Val told the team to instruct Claude to limit sentence count and write in simple ESL English. He said he reads every message, and long text costs him energy because he has to ask Claude to simplify it.
- REQ-1416 covers buying routers and modems from European or American makers, not Chinese. It is not a development item. Andrei Klimovich said it can stay as long as the acceptance criteria are testable — you can look at the purchased router and check it, plus details like supported connection count. Dzmitry warned that unsupported hardware turning up at a location causes long debugging.

**Autotests.** Ivan Shpak wrote 8 tests for the machine-to-FlexPort/Flex IQ connection. Four run on their own; four still need someone to unplug something by hand, because he found no way to disable the SAS cable from software. Val said that is wrong — if half the tests need a person, something in the approach is wrong. Pavel gave the answer on the call: on the machine every port is a symbolic link to a device, so the test can repoint the link to /dev/null and the channel disappears. Ivan will rewrite the tests.

Val then made a wider point: Ivan could have asked and finished the same day, but Minsk engineers work in a vacuum and do not talk to each other, and that costs a full day per cycle. Pavel answered that sending every problem to him is not a good solution either; Val agreed and said there are about 20 other people in Minsk to ask. Irina said the goal was an experiment, it produced progress in a couple of hours, and Val accepted that.

Alexey Khamin did not finish his autotest. It covers crediting money to the machine, which involves the terminal, FlexPort and the EGM. Claude offered only manual options, which he rejected, and he found no open API. Dzmitry advised pointing Claude at the relevant code. Alexey is now building a tool or instruction set so Claude knows where to look and can generate the test itself while checking the balance.

Pavel said Anton is finishing a Flex Pay emulator and a task must be raised to replicate it for Flex IQ, roughly a couple of days of work. The emulator runs the same backend as the real machine but with fake devices, inside a Docker container, so tests can run without hardware.

**Jira housekeeping at the end.** Pavel assigned the new capabilities — Flex IQ to Dzmitry, FlexPort to Vladimir. Capabilities 178, 230, 231, 234 and 235 still need planning. A screen-rework feature sitting under CAP-180 moves to the new CAP-235. Pavel believes most of 230, 231 and 234 is already built and only filters on the card reports and card search may be missing.

The status flow was confirmed: Andrei Klimovich moves a capability to Accepted; the assignee pulls it to To Do, moves it to In Progress when work starts, then to Review when all features are done; a developer must not close it — QA/product moves Review to Complete. Repository names: FlexPort is FORT, Flex Pay is FP, Flex IQ is FIQ, and the server side is DTP (BIP is the old one).

Alexey raised 5 open FlexPort bugs where money is lost — for example a second collect from the machine while FlexPort shows a cash-out, or scanning a ticket that is no longer in the database and getting a receipt with the money gone. Andrei Klimovich said the wallet should still be created but with a separate status such as "forfeit": the money sits there, cannot be used, but exists. Dzmitry already created CAP-231 for this, and the bugs go there.

The group meets again tomorrow at the same time.

## Decisions Made

- **REQ-753 deleted, not parked** — it mixed several products, added nothing new, and was not a product requirement. (Decided by Val Levitan, Dzmitry Chudzinau, Irina Shishko, Andrei Klimovich, Pavel Frolov) *Considered and superseded: moving it to the MVP2 backlog — Val objected that this builds a graveyard.*
- **No fixed timeout values in the device-disconnect requirements** — on losing the link to any device, show it on the player screen as fast as possible and keep retrying. An earlier time value helps the player more than an exact number does. (Proposed by Pavel Frolov, accepted by the group)
- **No PIN lockout on Flex IQ** — wrong PIN entries do not block the terminal. (Decided by Andrei Klimovich, agreed by Pavel Frolov)
- **CAP-173 goes back to In Progress** — a capability cannot be Complete while its requirements are still open. (Decided by Andrei Klimovich, agreed by Irina Shishko and Alexey Khamin)
- **Anything that takes more than a minute to decide gets parked, not deleted** — decisions that can be made on the spot are made on the spot. (Decided by Andrei Klimovich)
- **External-traffic protection (REQ-1550) stays in MVP1 and needs an ADR** — the terminals face the internet and must be protected. (Decided by Andrei Bosik, agreed by Andrei Klimovich and Pavel Frolov)
- **Requirements must be written short and in plain ESL English** — Claude is to be told to limit sentence count. (Decided by Val Levitan, agreed by Pavel Frolov)
- **The screen-rework feature moves from CAP-180 to the new CAP-235.** (Decided by Andrei Klimovich and Pavel Frolov)
- **Lost money creates a wallet with a "forfeit" status** — the money exists and is recorded but cannot be used. Covered by CAP-231. (Decided by Andrei Klimovich)
- **Capability status flow confirmed** — Klimovich moves it to Accepted, the assignee takes it to To Do, then In Progress, then Review; QA/product closes it to Complete, never the developer. (Decided by Andrei Klimovich, Pavel Frolov, Alexey Khamin)
- **Mockup and attachment file names follow the JVL file-naming standard, with the date.** (Decided by Pavel Frolov and Dzmitry Chudzinau, accepted by Andrei Klimovich)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Post to the team chat the collection of capability and requirement changes made yesterday, so features can be updated | September 23, 2026 | High | Said he would do it right after the call |
| 2 | Andrei Klimovich | Move the IQ operator tilts and alerts into a separate text collection with codes | September 23, 2026 | Normal | Keeps them out of the main IQ UI text library |
| 3 | Andrei Klimovich | Decide whether the confirmation screen is needed when creating or loading a wallet | September 23, 2026 | Low | Said it needs about 10 minutes |
| 4 | Andrei Klimovich | Review Irina's full NFR list for conflicts with product logic | September 23, 2026 | Normal | Plans to do it with Claude |
| 5 | Andrei Klimovich | Make the home-screen icons using the kiosk design language | TBD | Low | Current icons are temporary; will try to generate them with AI |
| 6 | Pavel Frolov | Send Andrei Klimovich the link to the file-naming standard in the repository | September 23, 2026 | Normal | |
| 7 | Pavel Frolov | Review requirements 1560, 1563 and 1565 under CAP-173, add the engineering answers, then move them to Accepted | TBD | High | Blocks closing CAP-173 |
| 8 | Pavel Frolov | Raise a task for Anton to replicate the Flex Pay emulator for Flex IQ | TBD | Normal | Pavel estimates a couple of days of work; autotests depend on it |
| 9 | Pavel Frolov | Create a feature under CAP-178 for supporting an additional card type | TBD | Normal | |
| 10 | Irina Shishko | Apply Pavel's "no fixed time, show immediately and keep retrying" wording to the device-disconnect requirements | TBD | Normal | She noted minute 24 of the meeting to find the wording again |
| 11 | Irina Shishko | Create the autotest features under the MVP1 capabilities | TBD | Normal | |
| 12 | Andrei Bosik | Rewrite REQ-1413 with the FlexPort switching answers given in this meeting | TBD | Normal | Will take them from the transcript |
| 13 | Andrei Bosik | Turn the open questions in REQ-1603 into acceptance criteria | TBD | Normal | Buffering already works via Fluent Bit |
| 14 | Andrei Bosik | Rewrite REQ-1550 short and in plain English, keeping only the essence, and write the ADR for the external-traffic protection mechanism | TBD | High | Current text is too long to read |
| 15 | Andrei Bosik | Make the acceptance criteria of REQ-1416 (router and modem purchasing) testable | TBD | Normal | |
| 16 | Ivan Shpak | Rewrite the 4 manual autotests using the symlink-to-/dev/null method so they run without hands | TBD | High | Pavel gave the method during the call |
| 17 | Alexey Khamin | Attach his 5 lost-money FlexPort bugs to CAP-231 | September 23, 2026 | High | Andrei asked him to do it first thing so the group can check they appear |
| 18 | Alexey Khamin | Build the tool or instruction set so Claude can generate the money-crediting autotest and check balances automatically | TBD | Normal | |
| 19 | Dzmitry Chudzinau | Create the features under capabilities 230, 231 and 234 | September 24, 2026 | High | Pavel asked for it by tomorrow |

## Open Questions

- Where non-development requirements such as hardware purchasing should live. Irina raised it; Andrei Bosik suggested a "not for development" capability, but nothing was settled.
- Whether newly created bugs will show in the portfolio view or only inside their task. Pavel suspects they will not be visible at portfolio level. To be checked once Alexey attaches the first 5 bugs.
- How QA/product will handle moving a capability from Review to Complete. Andrei Klimovich said it needs more thought and the process will be worked out during this MVP.

## Dispatch Log

---
*Processed from Teams transcript on September 23, 2026*
*Source meeting: Transactional MVP1: CAPs, REQs, UI/UX*
