# Meeting Summary — Transactional MVP1: CAPs, REQs, UI/UX
**Date:** September 25, 2026, 8:05 AM – 8:50 AM Eastern
**Duration:** About 45 minutes
**Attendees:** Andrei Klimovich (organizer, chair), Val Levitan, Pavel Frolov, Irina Shishko, Andrei Bosik, Dzmitry Chudzinau, Alexander Biratko, Ivan Shpak, Alexey Khamin
**Raw transcript:** [[Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026]]

## Summary

Held in Russian. Speech recognition is fair in most parts. It is poor in the Jira schedule review (about minute 25 to 33), where the screen was shared and people spoke in short fragments.

**Andrei Klimovich update.** All changes from the Sep 24 meeting are done. Jira and the mockup are updated. Questions sent to him during the day are answered and in Jira. He emailed the daily report yesterday. He picked the people by hand and missed Ivan. He asked for a mailing group for the report, ideally per product or stream, so people who work only on gaming machines do not get it.

**Distribution list.** Andrei Bosik will create a distribution list for the transactional system and send the name to Andrei Klimovich. Names raised: Pavel, Sergei Tsimonov, front-end developers, Anton, Vladimir, Sergei, Ivan, and Zhenya (Irina: so Zhenya can answer machine-side questions and stay informed). Irina suggested it could be all Minsk developers except the artists.

**FlexPort compatibility testing with other makers' EGMs (main topic).**
- Andrei Klimovich: JVL has an early agreement with several large operators. They will let JVL into their warehouse, or lend a few machines for **2 days**. The testing will likely be done by **Elizabeth**, maybe with another local technician. They need a clear workflow and a manual. Once Minsk gives the signal, the local team will contact operators and agree dates.
- **Pavel's setup:** bring the machine to the office and connect it to the internal network that Minsk can reach. Use **two SAS ports**. Port 1: the SAS accumulator that Ivan works with. It sends commands (lock, unlock, request accounting data). Ideally it can also send all command types that InComm and Intralot send. Port 2: FlexPort. Check that no FlexPort function breaks because of third-party commands. Check the main flow: FlexPort can send money, take money, track machine status, and show the right status.
- **Dzmitry:** add a function on FlexIQ and FlexPort that sends the raw SAS commands from the machine to a website. Then the team can compare our machine and a third-party machine (machine numbers, asset numbers) without reading logs. Pavel had a similar "dumper" idea. Pavel asked if this should run in production (all SAS commands except pings). Dzmitry said yes, it will be useful.
- Andrei Klimovich: the SAS data includes money in / money out and statistics down to each game title on a multi-game cabinet. Operators want this per machine. Pavel: this is **not MVP1; maybe MVP2 or MVP3**. Andrei agreed it is not MVP1.
- **Warehouse vs office:** Alexander Biratko asked if the warehouse is better (operator staff can help). Irina and Dzmitry said Minsk needs network access, and there would be none at a warehouse. Pavel proposed a hybrid: test 1 or 2 machines first. If all works, then go to warehouses with more confidence.
- Val first asked why location matters if there is a modem. He then said he misunderstood. Pavel explained: the key is the third-party machine. With a remote modem it is a different network and needs a wrapper to pass data. Dzmitry: access through a modem is a separate and hard task.
- **Ivan's requirements:** check the right cables exist. The SAS emulator runs on a computer with a COM port, best from the motherboard. USB-to-COM works but can cause problems. At least 2 cables: one from FlexPort, one from the SAS emulator. Ask if the site has the IGT SAS host simulator he uses. Pavel: installing it is not a problem. Andrei Klimovich: nobody has anything yet; all this must go in the manual.
- Irina: there is a standard document with all SAS commands a machine must support (used for certification). Go through that list. Ivan: the risk is that a maker adds something new.
- Irina: first run the procedure on **JVL's own machines**, with a near-final FlexPort and FlexIQ. Elizabeth tests on our machine, then repeats on a third-party machine.
- Andrei Klimovich asked if testing can start without FlexIQ, since FlexIQ is not ready and the deadline is **October 1**. Pavel: there is a machine emulator, and an IQ emulator soon, so in principle yes. Dzmitry: there will be no accumulator by the 1st. He would test with the terminal and add the SAS command capture first. FlexIQ is not 100% ready but it works. Andrei Klimovich: "then after October 1." Alexander Biratko: nothing blocks starting the instruction now; FlexIQ is good enough to test much of what is needed.
- **Task setup:** Andrei Klimovich will create a capability from this transcript. Pavel's wording: "FlexPort must be able to work with third-party EGMs." First task: describe the procedure and the equipment. More FlexPort changes may come once real machines are tested. Irina: **Ivan** will write the instruction for the hardware and SAS emulator setup, and attach the emulator and the SAS commands document. Ivan: he will try to finish **by Monday**. The team will create the Jira task and add requirements (acceptance criteria for the instruction).

**Test site equipment.** Ivan asked if all devices are on site. Andrei Klimovich: all devices and all harnesses are there. Missing parts can be ordered and arrive in a couple of days. All Flex types and Alters are there.

**Build for Monday.** Dzmitry will give Andrei a build on Monday to install on FlexIQ, with the printer set up and connected. On Monday the ticket print, wallet flow and FlexPort run can be checked. Card activation does not yet have all screens, but the main flow works.

**Printer.** Andrei Klimovich emailed Val and Gennadi to move the printer process. Pavel: yesterday there was a meeting with Gennadi and the printer maker. **Transact** has a printer with a housing and power supply, with **our Epic 950** inside. They discussed how to order this version as fast as possible. Val: Gennadi wants a small board change to add a standard connector. Val said he gave approval and the question is almost closed. For the current board, Pavel said a cable can connect to the black 10-pin connector; likely 2 wires need re-soldering.

**Andrei Klimovich away next week.** He will not be on site. Elizabeth knows how to install builds; send builds anyway. Dzmitry asked what to do if conflicts between requirements and CAPs come up while Andrei is on vacation. Andrei: it must not block development. He will be in Vilnius, almost the same time zone. He will keep the daily syncs at the same time all next week and answer in Teams.

**Jira schedule review** (poor audio). Pavel shared the Jira plan. Val asked about item 156 and its status / dates. Pavel said the start date must be fixed. Pavel said CAP 67 seems to miss a testing task, which should move its end date. Irina: testing tasks are not planned yet; 67 is done but tests must be written. Irina: without autotests, development is planned until **October 7**. Pavel confirmed.

**Autotests.**
- Irina will finish the features (test feature list) "tomorrow", then split them between Ivan and Alexey. On Monday the team can see the plan. Val asked if autotests fit inside the Oct 7 schedule. Irina: **no, it is physically impossible; autotests will be written after October 7.**
- Val: the goal is a schedule where QA tests in parallel. What is happening now is big progress, but not where we want to be. He asked for no action now; it is a note for the future and a compliment. Andrei Klimovich: it will be easier when the product team delivers capabilities and requirements about 1.5 versions ahead of development.
- **Alexey Khamin:** Ivan cleaned his tests and made a pull request in the transactional platform repository. Alexey is not merging yet. Open points: the right repository structure for tests, and tags so CI runs on a merge to main of one product also run tests for related products (contracts). He expects a clear repo structure **on Monday**, and he will add Claude instructions in the repo with the test standards.
- About 20 minutes before the meeting, a FlexIQ version with a **test API** (made by Dzmitry) was installed. Alexey's test worked almost at once with Claude. Demo steps: check device availability and machine balance, create a wallet on the terminal, scan it on FlexPort, pick an amount, check the machine balance matches. Pavel: there are hooks on FlexPort and FlexIQ to trigger actions. Pavel's Claude also pressed the machine's Play button by itself using generated button presses. Alexey will fill the repo with tests over the next two days and then start setting up CI, for now with manual start.
- Val asked if Ivan has the same progress. Irina: Ivan's tests worked yesterday; now they are merging it together.

**Close.** Andrei Klimovich will set up next week's meetings for this group. Next meeting Monday.

## Decisions Made

- **Create a distribution list for the transactional system daily report** — manual picking missed people (Ivan). (Decided by Andrei Bosik, Andrei Klimovich)
- **Compatibility testing will be done on machines brought to the office and connected to the network Minsk can reach, not at a warehouse first** — Minsk needs network access. Test 1 or 2 machines first, then go to warehouses if all works. (Decided by Pavel Frolov, Irina Shishko, Dzmitry Chudzinau, Andrei Klimovich)
- **Run the test procedure first on JVL's own machines, then repeat on third-party machines** — FlexPort and FlexIQ should be near-final first. (Decided by Irina Shishko; supported by Andrei Klimovich)
- **Third-party machine testing happens after October 1; the setup instruction starts now** — FlexIQ and the accumulator are not ready by the 1st, but nothing blocks the instruction. (Decided by Andrei Klimovich, Alexander Biratko)
- **Ivan Shpak writes the test setup instruction; a new capability "FlexPort must be able to work with third-party EGMs" and a Jira task are created** — so the work is not lost. (Decided by Irina Shishko, Pavel Frolov, Andrei Klimovich)
- **Transact housed printer with Epic 950 inside, with Gennadi's small board change for a standard connector** — Val gave approval; he said the question is almost closed. (Decided by Val Levitan)
- **Daily syncs continue at the same time next week while Andrei Klimovich works from Vilnius** — his absence must not block development. (Decided by Andrei Klimovich)
- **Autotests will be written after October 7, not inside the current schedule** — Irina said it is physically impossible within the week. Val noted parallel QA as a future goal but asked for no action now. (Stated by Irina Shishko)
- Considered and deferred: capturing all SAS commands in production (money in/out, per-title stats) — Pavel said this is MVP2 or MVP3, not MVP1; Andrei Klimovich agreed.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Create a distribution list for the transactional system; send the name to Andrei Klimovich | Sep 25, 2026 (so today's report uses it) | Normal | Andrei K wanted today's report sent to the group |
| 2 | Andrei Klimovich | Send the daily Jira report to the new distribution list | Sep 25, 2026 onward | Normal | |
| 3 | Ivan Shpak | Write the instruction for the compatibility test setup (hardware, cables, COM port, SAS emulator); attach the emulator and the SAS commands document | Sep 28, 2026 (Monday; "will try") | High | Irina and team add anything missing |
| 4 | Andrei Klimovich | Create the capability "FlexPort must be able to work with third-party EGMs" from this transcript | TBD | High | |
| 5 | [Unassigned — needs clarification] | Create the Jira task for Ivan's instruction and add its requirements (acceptance criteria) | TBD | Normal | Pavel: "we create it"; Andrei K: team adds requirements |
| 6 | Andrei Klimovich / local team | Once Minsk sends the setup, contact operators, borrow machines, bring them to the office, connect to the MikroTik | After the setup instruction is received | Normal | Testing after Oct 1 |
| 7 | Dzmitry Chudzinau | Give Andrei a FlexIQ build with the printer set up and connected | Sep 28, 2026 (Monday) | High | Ticket print, wallet flow, FlexPort run |
| 8 | Irina Shishko | Finish the autotest features, split them between Ivan and Alexey, and plan them | Sep 26, 2026 ("tomorrow"); plan shown Sep 28 | High | |
| 9 | Alexey Khamin | Define the test repository structure and test tags for CI; add Claude instructions with test standards to the repo | Sep 28, 2026 (Monday) | Normal | PR from Ivan not merged yet |
| 10 | Alexey Khamin | Fill the repository with tests, then start CI setup with manual start | Sep 26–27, 2026 ("tomorrow, day after") | Normal | |
| 11 | Andrei Klimovich | Set up next week's daily meetings for this group at the same time | Before Sep 28, 2026 | Normal | He will be in Vilnius |
| 12 | Pavel Frolov | Fix the start date of Jira item 156 | TBD | Low | Poor audio [Needs Val's confirmation] |

## Open Questions

- Should all SAS commands be captured and kept in production (except pings)? Raised by Pavel. Dzmitry said yes; treated as MVP2/MVP3. Not settled for scope.
- Can the SAS accumulator send all command types that InComm and Intralot send? Raised by Pavel. Not answered.
- Does the test site have the IGT SAS host simulator and a computer with a motherboard COM port? Raised by Ivan. Andrei K: nobody has it yet; goes into the manual.
- CAP 67 seems to miss a testing task that would move its end date. Raised by Pavel. Irina: testing tasks are not yet planned.
- How to handle conflicts between requirements and CAPs while Andrei Klimovich is away. Raised by Dzmitry. Andrei: reach him in Teams; no formal process set.
- Does Ivan have the same test progress as Alexey? Raised by Val. Irina: his tests worked yesterday and they are merging; Val's follow-up was not answered clearly.

## Dispatch Log

---
*Processed from Teams transcript on September 28, 2026 (meeting-watcher recovery sweep)*
*Source meeting: Transactional MVP1: CAPs, REQs, UI/UX*
