# Meeting Summary — Behind the Port SAS issues
**Date:** October 18, 2026, 7:00 AM – 7:30 AM Eastern
**Duration:** ~29 minutes
**Attendees:** Val Levitan, Pavel Frolov
**Raw transcript:** [[Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026]]

## Summary

Held in Russian.

**How the Flex-Port SAS work was done (Pavel).** About 3 weeks ago Pavel built a reference SAS client, a machine emulator. The team first made Flex-Port load and cash out money against this emulator; that took about 3 days. Then they connected a JVL machine instead. It did not work at once, and they had to adapt to how the JVL machine behaves. Now the same is happening with third-party machines: SAS works a bit differently on each machine. Evgeny Kharetski's emulator from 1–2 years ago was a different thing: an emulator of the SAS host (the other side). That host side now runs, in a different form, on the Flex-Port.

**Aristocrat.** Needed only a small fix (timing and the correct order of events). It was fixed quickly.

**IGT.** Did not work yesterday. In the evening Pavel found that the IGT machine seems not to handle the SAS "lock" command correctly. Normal flow: first lock the machine, then ask for the money. IGT seems to just queue the cash-out request. Pavel expects IGT to work today if Flex-Port does not send the lock command.

**Emulator and requirements discipline (Val).** Val said that under the development culture everyone signed up for, every gap found on a machine must become new or corrected requirements with acceptance criteria, plus code and prose in the repository. The emulator must be kept current with every gap found, so it can act "like IGT" or "like Aristocrat". Otherwise the only way to test a future Flex-Port change is to borrow machines again, or to rely on people's memory. Pavel agreed; he and Irina had discussed the same idea yesterday. Pavel thinks about 80% of tests can run on the emulator, but final tests must still run on all machines. Val partly disagreed: a final test on a live machine is good to have, but work should always start on the emulator, which holds the latest knowledge.

**Who enforces the culture.** Val said he does not want to be the leader and enforcer for the engineers. He wants Pavel and Irina to set and enforce the development culture every day, or it will fall apart over time. Pavel said he understands.

**Setup screens of third-party machines.** On Friday in Atlanta, Val opened the machines and saw full operator setup screens on each machine (Aristocrat, Light & Wonder, IGT). He asked that all of these screens be photographed. Pavel asked Andrei the same yesterday; this is a rare chance to capture other makers' screens. The screens are captured with a 4K capture adapter between the CPU and the monitor. The old one broke; Val bought a new one that arrives Monday. Val will be back in Atlanta on Monday.

**Idea to ask AI how to set up the machines.** Val suggested giving AI the Flex-Port description (or the emulator) and all the setup screens, and asking how to set up each machine. He thinks an optional setting, not a maker's bug, may explain cases like the lock command. Pavel said the AFT settings are about 55 checkboxes and only about 2 really matter; checking them by hand is not hard and builds experience for whoever runs these machines later. He does not think AI adds much for AFT settings. AI could compare all setup screens with JVL's own setup for user experience. Val closed the topic: it is up to the team. The screens will still be collected and sent to them as a record.

**Other machines and tools.** For the remaining machines the team needs access to their settings to change them and see how the port reacts; this is planned for today and tomorrow. Val said Aristocrat and IGT together cover about 70% of the market, but Light & Wonder and other machines are still required. Val asked if an oscilloscope must be rented. Pavel said not for now: on the third machine SAS is connected and commands flow, and all Flex-Port activity is logged to Grafana, which gives a lot of information.

**AI PM.** It creates few tasks so far (a handful of useful ones this week) and sends each person questions from the meeting in chat. It was set up to be conservative on purpose. Some people now ask for the meeting transcript to create their own tasks. Pavel suggested letting each person call the AI PM privately. Val disagreed: private talks would break the shared group discussion, and others would not hear mistakes. Pavel agreed. Val prefers that the AI PM speaks at the meeting itself: a short summary at the end and clarifying questions to each person. It can also look back over the last 2 weeks and flag topics raised 2–3 times with no task. Val recalled that Andrei is working on voice and promised it by about November 8.

**Igor and Texas conversion resources.** Pavel has no fresh news from Igor; Igor wanted to show something on Friday but Pavel had no time. Pavel said resources are available: Igor works on moving games to NOVA; Anton Leshkevich took a game (from South Dakota, as Pavel recalls) to convert from horizontal to vertical with Igor's scripts and has made some progress, not shown yet. The bottleneck is designers who regenerate video. Sergey Klimenovich has given nothing yet: his OpenRouter AI access did not work, and Andrei fixed it on Thursday. Pavel will check on Monday. They agreed to meet again in half an hour.

## Decisions Made

- **Every gap found on a third-party machine becomes new or corrected requirements with acceptance criteria, plus code and prose; the emulator is kept current per machine.** — so future Flex-Port changes can be tested without borrowing machines. (Decided by Val Levitan; Pavel Frolov agreed)
- **Pavel and Irina own and enforce the development culture, not Val.** (Decided by Val Levitan)
- **No private calls with the AI PM; the direction is for the AI PM to speak at the meeting (summary + clarifying questions, and topics raised over 2 weeks with no task).** — private talks break the shared discussion. (Decided by Val Levitan; Pavel Frolov agreed)
- **AI analysis of the setup screens is optional and left to the team; the screens are still collected and sent to the team.** (Decided by Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Get IGT cash-out working by not sending the SAS lock command | Oct 18, 2026 | High | IGT seems to mishandle "lock" |
| 2 | Pavel Frolov / team | Add the gaps found on Aristocrat and IGT as new or corrected requirements with acceptance criteria, code and prose; add per-machine modes to the emulator | TBD | High | Val's development-culture rule |
| 3 | Val Levitan + Atlanta team [who takes the photos is unclear in the transcript] | Photograph every setup screen on the Aristocrat, Light & Wonder and IGT machines with the new 4K capture adapter, and send them to Pavel's team | From Oct 19, 2026 (adapter arrives Monday) | Normal | Rare chance to capture other makers' screens |
| 4 | Pavel Frolov / team | Get access to the settings on the remaining machines and test how the port reacts | Oct 18–19, 2026 | High | |
| 5 | Pavel Frolov | Check whether Sergey Klimenovich made progress on video generation | Oct 19, 2026 | Normal | OpenRouter access fixed Thursday |
| 6 | Andrei (Bosik) | Voice for the AI PM | ~Nov 8, 2026 | Normal | As Val recalled; Andrei not present |

## Open Questions

- Do the remaining machines (Light & Wonder and others) need an oscilloscope? Pavel thinks not for now; Val will rent one if the team says so. (Raised by Val)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-18*
*Source meeting: Behind the Port SAS issues*
