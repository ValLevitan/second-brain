# Meeting Summary — Scheduling resources for September

**Date:** September 9, 2026, 7:02 AM – 8:38 AM Eastern
**Duration:** approximately 1 hour 36 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026]]

## Summary

The meeting reviewed the September schedule and resource allocation for the transactional products in JIRA. Val called it to find out when FlexPort will actually work and how to speed the whole programme up.

**Note on the transcript.** The first twelve minutes are badly mis-transcribed — the engine turned Russian speech into nonsense English words. Nothing in this summary is drawn from that stretch. Coherent speech starts at about 00:12:08.

**When FlexPort will be ready.** Val asked when he can put FlexPort at a location. Pavel said not September 11, and most likely not September 18 either. His best case is September 25. Pavel called FlexPort the bottleneck: until a piece of FlexPort works, the matching FlexPay function cannot be checked.

**Whether to write requirements up front.** Pavel said the logical way is to write everything down first, the way it was started with Nathan, where requirements were written, discussed and finalised over several months before features were created. He said there is no time now to spend two months on that. Val pushed back hard: if manual testing takes less time than writing the requirements plus automating the tests, why write at all. Irina answered that manual testing costs time every single round, while automating costs time once and then runs fast. Pavel added that the trade-off only favours manual work if a project is built once and never changed, and gave Flex IQ with the Mutagus tie-in as an example where roughly 30% of the code is being thrown away. Val ended the exchange by parking the question — he said he has to think about it himself.

**Leaning on Bosik and Kovalchuk for planning.** Val pointed at the large batch of capabilities and requirements Andrei Bosik had just created off meeting transcripts, and said Pavel should lean on Bosik and Dmitri Kovalchuk to organise JIRA rather than doing the planning himself. The pattern Val described: Pavel talks the work through, the meeting is recorded, and Bosik and Kovalchuk turn the transcript into capabilities and requirements — good enough for 75–80%. He told Pavel these meetings must be daily, or the corrections will not land, and to give them small tasks: first the full picture, then one narrow piece at a time. Val asked to be added to the invitations so he can pull the transcripts, though he will not attend. Pavel agreed to try it and see where it leads.

Pavel wanted one check first: Irina and Alexey Khamin should look at Bosik's requirements and roughly judge how much of the scope they cover. Pavel expects about 5% of kiosk behaviour at best, and only the new functionality discussed in the meetings. Val looked at REQ-1404 during the call and said the acceptance criteria are written as positive cases but Claude will easily derive the negative cases from them. Val added his own view that Claude works better from general descriptions than from very detailed ones, because detail suppresses its own reasoning.

**Capability and feature structure.** The FlexPort e-wallet and SAS support work sits under capability 165. Pavel listed further features that belong there: an optional PIN code; reading flags from the machine over SAS so FlexPort reacts correctly when the machine is blocked or its door is open; and remote logging, because today FlexPort logs can only be pulled onto a USB stick and not retrieved remotely. Pavel also said the wallet transfer piece should be its own capability, since it touches the server side as well.

**How to separate MVP 1 from MVP 2 in JIRA.** Pavel argued for fix versions on the capability project, global across all products and named per product (for example "FlexPort 1.0") so capabilities can be filtered by release. Irina suggested using the capability status instead, and warned that capabilities belonging to a later release will otherwise drag the product's timeline out. Pavel noted that when this was discussed before, they settled on fix versions inside each repository, which keeps the versions below the capability level. He said the decision still has to be taken properly. As an interim measure he offered to push later capabilities down the graph and treat everything above a marker line as release 1.

**Resources.** Alexeev already has current WiFi tasks plus finishing the firmware update — a week's work at least. Pavel wants the log-transfer work given to Alexeev if he can carry it. Pavel took the SAS work himself, partly out of interest, but mainly because he has Khamin and Irina beside him and several machines to run cases on, while Alexeev would come back with a roughly one-day delay on every request. Val said he can ask Alexeev to take this on at his current job or move him to full time. Val also asked whether Biratko, Koretsky and Khamin can work more; Pavel said Sasha Biratko keeps strict hours and would have to be asked about a Saturday specifically, and that Khamin can carry more once the V3 GA-COAM testing is finished. Irina said the SAS documentation work is this week only, and after that transactional is everyone's priority. Pavel proposed parallelising: Irina and Alexey write up the negative cases as acceptance criteria while the positive cases are being worked, which lets Claude write its own tests and modify the code fairly autonomously.

**Val's commercial case and the volume ambition.** Val explained why the pressure is on. JVL is currently the only company that makes both the gaming machine and the transactional equipment itself — Flex IQ, FlexPay Slim and the FlexPorts. The market has only just opened to transactional equipment, vertical machines are scarce, and the V43 with 15 games is new and proven to earn. The offer he is already pitching to customers: buy one V43 machine with 15 games and get five FlexPorts, one IQ and one FlexPay free. Val stressed this window is unique and short and could be switched off in a day, so he wants people mobilised to the maximum from now until December, will pay for all overtime, and expects rest at the end of December.

Val laid out the volume he is aiming at: one installation on October 1, ten installations during October, 200 from November 1, and 500 during November. He said the numbers are deliberately overstated to convey intent, that they count units of equipment rather than locations, and that he does not yet know which unit of measure to settle on.

**Engineering fork on the bundle.** Pavel flagged a serious fork. FlexPay and Flex IQ can both be adapted fairly quickly to work with FlexPorts, but only one of them per location — an IQ and a FlexPay cannot be installed at the same location in the first iteration. Multiple units per location comes in the second iteration together with WiFi. Val accepted that, and said he can run the parallel wiring for the WSU protocol now. On priority, Val said WiFi is second in urgency and is what can be sacrificed for other functionality, because he is counting on the installation rate to grow — the first ten installations will take as long as the following hundred.

**What the October 1 installation has to do.** Val described the target case. FlexPay must be ready with bill acceptor, card dispenser and ticket printer, working in self-service mode: the player inserts a bill into FlexPay or into the machine, gets a wallet, walks to the machine and plays; the payout prints at FlexPay. The wallet can be generated either at the start of play or after it, and the player can then move between machines or exchange the wallet for a card. Pavel confirmed this is the case planned for October 1.

**Hardware and modems.** Pavel confirmed the modems connected to the RK3568 are working, and that both FlexPay and Flex IQ will be built on the RK.

**Georgia and certification.** Val set September 15 for a working prototype in Georgia, with FlexPort connecting over SAS on machines from other suppliers as well as JVL's own, which is where he expects the negative cases to bite. Pavel wants those recorded as two separate items — testing on JVL machines and testing on other suppliers' machines — and said problems will show up immediately with third-party machines. Val also said the Eclipse submission is due around September 15, which means the V3 product must be thoroughly tested by then.

**Game maths.** Val said the decision was taken the previous evening at 9:00 PM and he told Yefim to start: replace the currency shown on the buttons with credits, and change the maths on two games, which Yefim estimated at about 14 hours of work. Irina had understood the decision was still open; Val confirmed it is made. On that basis it should reach the team by September 11.

**Next step agreed.** Pavel will build the work schedule on the assumption of one installation on October 1 and have it ready by Friday, and will meanwhile start the planning conversations with Bosik and Kovalchuk. Val and Pavel meet Friday to work through the schedule.

## Decisions Made

- **FlexPort is the bottleneck for the transactional programme** — FlexPay functions cannot be verified until the matching FlexPort functionality exists. (Pavel Frolov)
- **FlexPort will not be ready for a location on September 11, and most likely not September 18; best case September 25** — Pavel's estimate, accepted as the working assumption for planning. (Pavel Frolov, Val Levitan)
- **First iteration supports only one transactional unit per location — either Flex IQ or FlexPay, not both** — multiple units per location moves to the second iteration with WiFi. Val accepted the limitation and will pre-run the parallel wiring for the WSU protocol. (Val Levitan, Pavel Frolov)
- **WiFi migration for FlexPort and FlexPay is second in urgency** — it is the piece to sacrifice for other functionality. (Val Levitan)
- **Planning and JIRA organisation moves to Andrei Bosik and Dmitri Kovalchuk, under Pavel's direction, with daily meetings** — Pavel keeps direction and review but does not do the planning by hand; Val is to be added to the invitations so he can pull transcripts. Pavel agreed to try the approach. (Val Levitan, Pavel Frolov)
- **The V43 bundle offer Val is pitching:** one V43 machine with 15 games, plus five FlexPorts, one IQ and one FlexPay free. (Val Levitan)
- **Both FlexPay and Flex IQ will be built on the RK3568** — the modems connected to it are working. (Pavel Frolov)
- **The game maths decision is made, not open** — currency on the buttons is replaced by credits and the maths on two games changes; Val instructed Yefim the previous evening at 9:00 PM. (Val Levitan)
- **Overtime will be paid** — Val committed to compensating everyone for the push from now to December. (Val Levitan)
- Considered and parked: **whether to invest in writing capabilities and requirements up front versus testing manually.** Val stopped the debate and said he has to think about it himself; no ruling was made in this meeting.
- Considered and not settled: **how to separate MVP 1 from MVP 2 in JIRA.** Pavel wants global fix versions on the capability project; Irina suggested using status. Pavel said the decision still has to be taken. The interim measure is to push later capabilities down the graph and treat everything above a marker line as release 1.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Build the work schedule on the assumption of one installation on October 1 | September 11, 2026 | High | Val set Friday as the deadline; the Friday meeting works through it |
| 2 | Pavel Frolov | Start the planning sessions with Andrei Bosik and Dmitri Kovalchuk, including Irina, so they can generate cases and requirements | September 11, 2026 | High | To be running before the Friday schedule meeting |
| 3 | Pavel Frolov | Hold these planning meetings daily and add Val to the invitations | Ongoing from September 9, 2026 | High | Val will not attend but wants the transcripts |
| 4 | Irina Shishko + Alexey Khamin | Review the requirements Andrei Bosik created and roughly assess how much of the scope they cover | TBD — before the Bosik/Kovalchuk session | High | Pavel's precondition; he expects about 5% coverage of kiosk behaviour |
| 5 | Pavel Frolov | Forward Bosik's email with the capability and requirement numbers to Irina | September 9, 2026 | Normal | Done during the meeting — Pavel confirmed he had forwarded it |
| 6 | Pavel Frolov | Add the missing FlexPort features to capability 165: optional PIN code, reading SAS flags from the machine (door open, machine blocked), and remote log retrieval over SAS/WSU | TBD | Normal | Pavel said he can create the placeholders immediately |
| 7 | Pavel Frolov | Create a separate capability for the wallet transfer work | TBD | Normal | It touches the server side as well as FlexPay |
| 8 | Irina Shishko + Alexey Khamin | Write up the negative cases as acceptance criteria, in parallel with the positive-case work | TBD | Normal | Pavel's proposal to parallelise and let Claude write its own tests |
| 9 | Yefim | Replace currency with credits on the buttons and change the maths on two games (about 14 hours of work) | September 11, 2026 | High | Val instructed him September 8 at 9:00 PM; Irina thought the decision was still open |
| 10 | Pavel Frolov | Have at least one working stand ready — FlexPay or Flex IQ with FlexPorts on new firmware working over SAS, most likely FlexPay | September 16, 2026 (middle of next week) | High | Pavel's own commitment; Val had asked for September 15 |
| 11 | Pavel Frolov | Get the full setup working in the office, however roughly, at least two weeks before the October 1 installation, so Andrei Klimovich can start testing | Week of September 14, 2026 | High | Val's requirement |
| 12 | Pavel Frolov | Record FlexPort SAS testing as two separate items: testing against JVL machines, and testing against other suppliers' machines | TBD | Normal | Pavel expects problems to appear immediately with third-party machines |
| 13 | [Unassigned — needs clarification] | Obtain at least one machine from another supplier for the FlexPort SAS testing | TBD | Normal | Val said "we must take machines from other suppliers" and "we must have at least one more machine" — he did not name who does it |
| 14 | Val Levitan + Pavel Frolov | Meet Friday to work through the schedule | September 11, 2026 | High | Val said he had set the appointment specifically |

## Open Questions

- Whether to invest the time in writing capabilities and requirements up front, or accept manual testing. Raised by Val; he parked it explicitly and said he must think it through himself.
- How MVP 1 and MVP 2 should be separated in JIRA — global fix versions on the capability project (Pavel) or capability status (Irina). Pavel said the decision still has to be taken.
- Which unit of measure Val's installation targets count. Val said units of equipment rather than locations, but said he does not yet know which measure to settle on.
- Whether Alexeev can be moved to full time or take this work on at his current job. Val raised it; not resolved.
- Whether Biratko, Koretsky and Khamin can work more hours. Val raised it; Pavel said Biratko would have to be asked about a specific Saturday, and Khamin is still finishing V3 GA-COAM testing.

## Dispatch Log

---
*Processed from Teams transcript on September 10, 2026*
*Source meeting: Scheduling resources for September*
