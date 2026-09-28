# Meeting Summary — Daily Standup meeting
**Date:** September 24, 2026, 4:46 AM – 5:23 AM Eastern
**Duration:** About 37 minutes
**Attendees:** Pavel Frolov (chair), Alexander Biratko, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Dzmitry Chudzinau, Dmitri Kovalchuk, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026]]

## Summary

Spoken in Russian. Round-the-table status, then three longer discussions: firmware delivery, the Georgia game list, and Jira capability statuses.

**Firmware update for FlexPorts is the top priority, and the delivery path is not decided.** Pavel told Dmitri Kovalchuk to raise features for a **Flex IQ emulator**, built the same way as the Flex Pay one, because the firmware update protocol for FlexPorts is needed first. Anton said the two devices share the same protocol and contracts and differ only in workflow and screens, and since he emulates device behaviour rather than screens, the Flex Pay emulator will probably work on Flex IQ with little change. He will move it across today.

The unresolved part is how the firmware gets to the device. Dzmitry Chudzinau said he would rather revisit his scheme: it was never properly tested by anyone but him, he does not know whether the current port-to-IQ contract still holds, and the server side is definitely different now because of the Dropbox-style loading. Pavel's conclusion: **the delivery method to Flex IQ and Flex Pay is not defined and not built.** Agreed action: Anton takes a spike to assess whether the current contract covers what is needed. Dzmitry asked for an AI review of the work done first, to see whether it finds problems.

**Georgia, Intralot and the 15-game list.** Ivan Shpak wrote the MD file for Georgia (GUHAM 3). This is new territory: for the first time the number of games implemented on the machine does not match what he sets in RIS. **Of 15 possible games only 10 can run at once.** Nobody knows how Intralot handles that, so he built the file for all 15 games and warned the team there may be delays getting through Intralot's tests. Pavel said that should be fine: work done about two years ago gives every game in a build its own identifier, and those identifiers persist regardless of how many games are installed. Irina raised the related point that the RTP sheet holds all three percentages per game while RIS declares only one. Ivan said he pulls all of them through the list and asked the team only to be aware of the risk.

**Jira capability statuses.** Dmitri Kovalchuk added a "Req Review" status to capabilities and will build a rule today that moves a capability from In Progress to Req Review once all its features and stories are green, so it does not get lost manually. He also moved "Accept Capability" from green to grey To-Do, because green made Claude read it as a closed task.

That opened a debate on **Completed versus Closed**. Dzmitry asked which a developer should set and said different people do it differently. Dmitri's definition: Completed means the work is done but may come back; Closed means it is fully packed up and finished. Irina's version: Completed means you did it but nobody checked; Closed means it was checked and works. Dzmitry pushed twice on who actually does the checking and said he still had no answer. Pavel's answer was autotests, and that all features get clicked through before the capability is closed. Irina raised a known trap: the parent must not close before its children. Dmitri will check how the auto-rule behaves.

Dmitri also raised **To-Do dates**: many tasks belonging to Sasha, Ira and Andrei sit in To-Do with no end date. The rule agreed is that a date goes on as soon as the task is discussed, set forward in time, not only when it moves to In Progress. He finished the report today and **email notifications start tomorrow morning**.

**Individual status.**
- **Alexander Biratko** — closing a feature on CAP 137 (13-49). The next two, 12-50 and 12-51, are blocked by Amazon-side changes; new endpoints are needed before the app can update. He will then re-review the Flex Pay capability.
- **Alexey Khamin** — mostly autotests, waiting on Dmitri for an API. FlexPort status, picture and machine balance all read correctly. The screens changed and the project documentation was never updated, so Claude could not follow what was happening; the docs were simply stale. He linked the money-loss bugs under CAP 231; Klimovich reviewed them for relevance and commented, and who fixes them is still open. Pavel and Irina both said it will be their own team: Yavorsky will not be available and waiting for Alekseev to work weekends is not an option.
- **Anton Seregin** — closed the validator work and the tape-handling process; updating the printer daemon to a new version and reviewing the printer again.
- **Daniil Stauskiy** — on the game selection screen; buttons moved over. He wants a second FaceBoard game from Igor to test loading and LGS interaction. His open question on CAP 14-85: the collect button must be disabled when the machine cannot process hand pay. Pavel read it as covering the cases where the machine cannot pay out or has zero balance. Evgeny suggested looking for a "constant" parameter about whether a game can start on LGS. Ivan pointed to a `screen cashout` flag in RIS: disable it and the cashout button does not appear on the VDI at all, which may be what the criterion means.
- **Dzmitry Chudzinau** — raised features with dates and statuses for all of Andrei's new capabilities; continuing CAP 152 on card activations; finishing the last update fixes. A firmware change went cleanly on one terminal and has problems on another.
- **Evgeny Kharetski** — 22 integrations, two new service libraries (counter board and printer). Package naming problems had stopped all libraries being enabled at once; Anton reworked it. He finished 12-18, is on 12-21, then 12-19 and 12-17, and is working CAP 236.
- **Irina Shishko** — features marked up so tests can be written; many meetings. She and Pavel will take the PariSys discussion, probably with Evgeny.
- **Ivan Shpak** — also on autotests. He needs write access to the repository; he said he does not want it, Irina told him he will be writing there and that it is not up for discussion. Dmitri Kovalchuk needs to be told where to grant it.
- **Sergey Tsimanov** — finished the connection-state telemetry metrics, verified on Dmitri's new build. Took the Flex IQ wallet creation and funding task; the requirements have many contradictions, so he is preparing questions for Andrei.
- **Vladimir Samusenko** — FlexPort design update: idle screen, element positions, buttons and shortcuts are updated and ready for testing. Pixel-for-pixel matching is not achievable right now. Screens in Andrei's design that were never implemented become separate tasks. **Pavel stated plainly that those new screens are not MVP1 and are not guaranteed done and tested by October 1.** Vladimir will close the current task, raise the pull request, and log the new screens from a comparison he already made.

## Decisions Made

- **The Flex IQ emulator is built from the Flex Pay one, not from scratch.** Same protocol and contracts; only workflow and screens differ, and Anton emulates behaviour rather than screens. (Decided by Pavel Frolov and Anton Seregin)
- **The firmware delivery method to Flex IQ and Flex Pay stays undefined for now; a spike decides it.** Anton takes a spike to assess whether the current port contract covers the needed functionality. (Decided by Pavel Frolov)
- **The Georgia MD file lists all 15 games, not the 10 that run at once.** Every game in a build carries its own identifier regardless of how many are installed, so the full list is correct. (Decided by Pavel Frolov, after Ivan Shpak raised it)
- **The new FlexPort screens are out of MVP1.** They will be built, but no guarantee of being done and tested by October 1. Pavel said this explicitly so no expectation forms. (Decided by Pavel Frolov)
- **Capability In Progress moves to Req Review automatically once all features and stories are green.** (Decided by Dmitri Kovalchuk)
- **"Accept Capability" moves from green to grey To-Do**, because green made Claude treat it as closed. (Decided by Dmitri Kovalchuk)
- **A To-Do task gets an end date as soon as it is discussed**, set forward in time, not only when it moves to In Progress. (Decided by Dzmitry Chudzinau and Pavel Frolov)
- **The money-loss bugs under CAP 231 will be fixed by this team**, not by Yavorsky or Alekseev. (Decided by Pavel Frolov and Irina Shishko)
- **Ivan Shpak gets repository write access.** He said he did not want it; Irina ruled it is not up for discussion. (Decided by Irina Shishko)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dmitri Kovalchuk | Raise the features for the Flex IQ emulator, by analogy with Flex Pay, including the FlexPort firmware update protocol as its own feature | TBD | High | Pavel said the firmware protocol is needed first |
| 2 | Anton Seregin | Move the Flex Pay emulator over to Flex IQ | Today (Sep 24, 2026) | High | He offered the date himself |
| 3 | Anton Seregin | Take a spike: does the current port contract cover the needed firmware-update functionality, and what should change | TBD | High | Dzmitry wants an AI review of the existing work as part of it |
| 4 | Dmitri Kovalchuk | Build the rule moving a capability from In Progress to Req Review when all features and stories are green | Today (Sep 24, 2026) | Normal | |
| 5 | Dmitri Kovalchuk | Check how the auto-rule behaves when a capability closes, so parents do not close before their children | TBD | Normal | Irina flagged the trap |
| 6 | Dmitri Kovalchuk | Finish the To-Do report; email notifications begin | Tomorrow morning (Sep 25, 2026) | Normal | He said it was finished today |
| 7 | Vladimir Samusenko | Close the FlexPort design task, raise the pull request, and log tasks for the screens that have no implementation | TBD | Normal | He already has a comparison of what is missing |
| 8 | Daniil Stauskiy | Check the `screen cashout` parameter in RIS and the "constant" parameter against CAP 14-85 | TBD | Normal | Suggested by Ivan Shpak and Evgeny Kharetski |
| 9 | Daniil Stauskiy | Get a second FaceBoard game and a test screen from Igor | When Igor is in | Low | To test loading and LGS interaction |
| 10 | Sergey Tsimanov | Prepare the questions on the contradictory Flex IQ wallet requirements for Andrei | TBD | Normal | |
| 11 | Ivan Shpak | Tell Dmitri Kovalchuk where he needs write access, and take it | TBD | Normal | Irina ruled he gets it |
| 12 | The team | Read through the new capabilities Andrei created yesterday | TBD | Normal | Pavel: everyone interested needs to review them |
| 13 | Irina Shishko, Pavel Frolov, Evgeny Kharetski | Hold the PariSys discussion | TBD | Normal | |

## Open Questions

- **Who actually verifies a feature before it is closed?** Dzmitry asked twice and said he still had no answer. Pavel said autotests and clicking through before the capability closes; Irina and Dmitri gave two different definitions of Completed versus Closed.
- **How does Intralot handle a machine where only 10 of 15 games run at once?** Nobody knows. Ivan expects to find out today and warned of possible delays in their tests.
- **The RTP sheet holds three percentages per game, RIS declares one.** Irina thinks it is the same class of problem. Ivan said he pulls all of them and asked only that the team be aware.
- **Who fixes the money-loss bugs under CAP 231?** Agreed it stays in the team; not assigned to a person.
- **Does the current port-to-Flex IQ contract still hold?** Dzmitry does not know; that is what the spike is for.

## Notes on the transcript

Russian, kept verbatim. Plaud-style mis-transcriptions are frequent; the readings used above are from context:
- **"кобилли" / "капобилити" / "копобилити" / "каполити"** — **capability**. **"фичи"** — features. **"сторис"** — stories.
- **"флекс пэй" / "флекса айкью" / "флекспорт" / "фликспорт"** — **Flex Pay**, **Flex IQ**, **FlexPort**.
- **"прозу" / "опрозу"** — most likely **OpenAPI/spec docs** regenerated by a hook on pull request; the exact word is unclear and is left as transcribed.
- **"клод"** — **Claude**. **"рисе" / "рис"** — **RIS**. **"интролот" / "интерлотом"** — **Intralot**. **"элджиса" / "лгс"** — **LGS**. **"ведайке" / "видайке"** — **VDI**.
- **"дэнд пэй" / "dand pay"** — **hand pay**. **"cashooth" / "кэшаут"** — **cashout**.
- **"фейнборд"** — **FaceBoard**. **"эркаш"** — unclear, left as transcribed.
- **"парисус" / "парисус"** — read as **PariSys**; not confirmed.
- One passage contains a profanity that is Plaud mis-hearing ordinary speech (Ivan describing a field that can be disabled). Left verbatim.

## Dispatch Log

---
*Processed from Teams transcript on September 24, 2026*
*Source meeting: Daily Standup meeting*
