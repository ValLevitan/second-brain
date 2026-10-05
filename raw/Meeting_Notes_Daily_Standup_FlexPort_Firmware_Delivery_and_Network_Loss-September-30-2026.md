# Meeting Summary — Daily Standup meeting
**Date:** September 30, 2026, 4:57 AM – 5:28 AM Eastern
**Duration:** About 30 minutes
**Attendees:** Pavel Frolov (chair, organizer), Alexander Biratko, Anton Seregin, Daniil Stauskiy, Dzmitry Chudzinau, Dmitri Kovalchuk, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026]]

## Summary

Held in Russian. The speech recognition is poor in places, so some task numbers below are uncertain. The Teams recording ran for almost 2 hours, but the transcript covers only the first 30 minutes of speech.

**FlexPay modem capability.** Alexander created a new capability (247) for the modem in FlexPay, with features under it. Most features are done; only checks remain. He got a SIM card from Pavel this morning and the network already connects. He expects to finish the capability today.

**LED strip and the LED service.** Alexander analysed the LED strip work. The HAL library already has an LED strip implementation, but the APIs are not exposed. FlexPay still runs on the HAL. The LED service exists in two copies: Pavel's early test version (in the firmware project) and Anton's version, which has a Java wrapper. Evgeny is already moving the data center to Anton's service. Alexander will switch to working with the service and not fight the HAL. LEDs and the switch to the service are his next work.

**New motherboard SDK.** Pavel took task ACT-5780 (number uncertain): a full SDK for the new motherboard with the AMD processor, so the kernel and file system build completely.

**Flex IQ emulator scope.** Anton checked the ticket printer emulator and barcode scanner against Flex IQ. Dzmitry and Pavel said the card dispenser is not used. Pavel said not to touch the LTE modem in the emulator; it is too specific. Anton said Flex IQ has nothing for FlexPort updates yet, and FlexPay code for it is written but not tested.

**FlexPort firmware delivery.** Pavel is not sure the firmware transfer to FlexPort can be done by the end of the week. Dzmitry said time is short; maybe with the weekend. They discussed the business logic:
- Pavel: the server should be able to send a command to a kiosk to take a given firmware version, set per location.
- Dzmitry: the server must also show which FlexPort firmware runs on each terminal, and the time to apply an update must be set.
- In the earlier version, the operator opened the port list and pressed a button to apply the firmware. Pavel said they could keep that: the operator or JVL remotely presses "apply".
- Dzmitry said the task is big and he does not want to rush it with the last update. Pavel suggested at least working out the delivery method first; who triggers the update and the feedback (did the ports receive it) come next.
- Pavel: "Let's talk tomorrow."

**Dzmitry's work.** Capability 152 (activation) is finishing; some problems were found. Capability 175 (record press) is in progress and will need more features. He added features to capability 241 (Andrei created it, no one was assigned): machine connected / disconnected status, out-of-service with a list of reasons, and SAS logs sent to the server (not pings). He can write the protocol on the Flex IQ side first and Pavel adapts to it; he can start this today. Pavel asked him to set a start date on FIQU-86 (Pavel had set the 28th). Dzmitry wants to raise the sounds topic at today's meeting.

**Daniil.** Finished features 1384 and 1385 yesterday. Today: capability 228, new feature 1486, converting the select screen and game icons for NOVA. Pavel said he can ask Igor or Alexander Biratko for help.

**Evgeny.** Finished the Georgia fixes yesterday. He still needs logs: his queue fix ("always last") does not look right on screen, although Claude said it was already last. CC talk is done (task CT-5858 was in the backlog, so it looked lost); he closes it today. Don completed almost all tasks Evgeny gave him. Next: integration (tasks 2019 and 1217).

**Anton.** Posted a long battery instruction in the chat. He must leave for about an hour.

**Ivan — tests and FlexPort network loss.** Ivan's remaining main test is the install pulled from the production server and how the progressive controller behaves; then network tests on a separate network. For Eclipse he waits for an answer and will arrange with Alex. He asked how a machine behaves if FlexPort loses its network:
- Ivan: the machine does not tilt; Collect is allowed but ends in an error because there is nowhere to cash out. There is a retry; if the network comes back, the cash-out completes. Otherwise the credits stay on the machine.
- Pavel: yes. An error is better than sending to the port, where after a 30-second timeout the vouchers are marked unclaimed and come back at the next collect.
- Irina: if the port loses its link to Flex IQ, it goes out of service. The machine keeps playing through the bill validator, but money cannot be cashed out. Without a bill validator, the machine should also lock.
- Pavel: network loss is expected to be short, so why lock the machine for that time. The key question is how a third-party machine behaves.
- Evgeny noted a checkbox that shows a fault if the SAS link is down; Ivan does not set it yet, as no one asked for it.

**Sergey.** Finished the task to create a wallet through FlexPort. Capability 158 has four tasks; some can be dropped (for example payment hop 5, because wallets stay on the terminal for now). Much is already built; he is finding what is missing. Plans to close one today and take the next.

**Vladimir — blocked task.** He did task 41 (expired permission) autotests and logged about 3 defects and some improvement tasks. He cannot cover all scenarios, so he cannot close it. He asked what to do with the task and the unfinished code branch. Pavel: set it to **Blocked** and raise it at the next meeting. Next he picks a task that is closer to ready (maybe 148; also one with an overdue date) and moves dates as needed. Irina: he can take any unassigned task.

**Dmitri Kovalchuk.** Watch your dates and statuses. Create tasks in the repositories you work in; the repository name must match. Pavel agreed and said he must check his own.

## Decisions Made

- **Vladimir's partly-finished autotest task goes to Blocked status**, not closed, and is raised at the next meeting to check if it is unblocked. (Decided by Pavel Frolov)
- **The Flex IQ emulator will not simulate the LTE modem.** Too specific. (Decided by Pavel Frolov)
- **Alexander moves to the LED service instead of the HAL library.** (Agreed by Alexander Biratko and Pavel Frolov)

FlexPort firmware delivery design was discussed but not decided; Pavel moved it to tomorrow.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Finish checks and close FlexPay modem capability 247 | Sep 30, 2026 | Normal | SIM card already connects |
| 2 | Alexander Biratko | Work on LEDs and switch FlexPay to the LED service | TBD | Normal | Next task after 247 |
| 3 | Pavel Frolov | Build the full SDK for the new AMD motherboard (ACT-5780) | TBD | Normal | Kernel + file system |
| 4 | Dzmitry Chudzinau | Set a start date on FIQU-86 | Sep 30, 2026 | Low | So Jira shows correct dates |
| 5 | Dzmitry Chudzinau | Start the capability 241 protocol on the Flex IQ side (connect status, out-of-service reasons, SAS logs) | Sep 30, 2026 | Normal | Pavel adapts to it |
| 6 | Dzmitry Chudzinau | Raise the sounds topic at today's meeting | Sep 30, 2026 | Normal | |
| 7 | Pavel Frolov, Dzmitry Chudzinau | Continue the FlexPort firmware delivery discussion | Oct 1, 2026 | High | Delivery method first; trigger and feedback next |
| 8 | Evgeny Kharetski | Get logs and check why the queue fix does not show "always last" on screen | TBD | Normal | Georgia fixes |
| 9 | Evgeny Kharetski | Close CC talk task CT-5858 | Sep 30, 2026 | Low | |
| 10 | Ivan Shpak | Run the production-server install test and progressive controller test, then separate-network tests | TBD | Normal | |
| 11 | Ivan Shpak | Arrange Eclipse next steps with Alex once the answer arrives | TBD | Normal | |
| 12 | Sergey Tsimanov | Close the next capability 158 task today and take the next one | Sep 30, 2026 | Normal | Drop payment hop 5 |
| 13 | Vladimir Samusenko | Set task 41 to Blocked; pick the next autotest task that is closer to ready and fix its dates | Sep 30, 2026 | Normal | Maybe 148 |
| 14 | All team | Check dates and statuses; create tasks in the matching repositories | TBD | Normal | Dmitri Kovalchuk's reminder |

## Open Questions

- How should FlexPort firmware updates work: who triggers them (server, operator, per location), when they apply, and how the ports report back? (Pavel, Dzmitry) — moved to tomorrow.
- Should a machine without a bill validator lock when FlexPort is out of service? (Irina raised; Pavel doubts it for short outages)
- How does a third-party machine behave when FlexPort loses its network? (Pavel)
- Should the "fault if SAS link down" checkbox be set? (Evgeny raised; not asked for yet)

## Dispatch Log

---
*Processed from Teams transcript on September 30, 2026, 8:15 AM Eastern*
*Source meeting: Daily Standup meeting*
