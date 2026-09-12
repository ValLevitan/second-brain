# Meeting Summary — Transactional products management (From Caps-Reqs to Work Done+AutotestsByAccptance)

**Date:** September 10, 2026, 5:31 AM – 5:56 AM Eastern
**Duration:** approximately 25 minutes
**Attendees:** Pavel Frolov, Irina Shishko, Alexander Biratko, Dmitri Kovalchuk, Dzmitry Chudzinau, Andrei Bosik
**Raw transcript:** [[Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026]]

## Summary

Pavel called the meeting to work out how to optimise development so that the most work gets done in the least time, and so that the result is easy to test. Easy to test means testing costs less time than development did, which means as much of it automated as possible. The whole meeting was in Russian.

**The workflow everyone has already agreed to.** Pavel restated it: start from a capability, which carries a set of requirements, and the requirements carry the acceptance criteria; features are created under the requirements. If a feature is closed and satisfies the acceptance criteria tied to its requirement, Claude can verify that automatically. Pavel added the caveat himself — this only works if all the capabilities are written and all their requirements are written. Where they are not, there is a hole that automated tests will not cover. He said 100% is not achievable and requirements cannot be written in fine detail, but if roughly 80% of the general functionality is covered by capabilities and requirements, the tests will cover a large share of how the device or system behaves, and that is a big block of work taken off a manual tester.

Dzmitry Chudzinau asked what happens when nobody knows up front how to check something. Pavel's answer: the acceptance criterion gets written in general terms, which leaves work for the future but at least covers it with some description.

**Who should be writing requirements.** Chudzinau raised the wider objection: requirements come from the business level, so why should the reporter be able to leave a capability without requirements and engineers then stop their own work to fill his in. Pavel agreed it is a fair question and said it can be raised the same day. His proposal was to hold a meeting with Andrei Klimovich and walk through every capability out loud, discussing it from the requirements side — because part of the requirements will be set by the business, and the engineers can say immediately where something is impossible or not achievable in the current situation. The non-functional requirements, Pavel said, will be written by the engineers regardless — himself, Andrei, the two Dmitrys, or Irina.

**What to do first.** Pavel said the first stage, before anyone tries to create and implement features, is to go through the capabilities created in the last seven days, work out which are no longer relevant, and create the matching requirements with the requirements written into them. Andrei Bosik proposed a different order — first decide what goes into MVP 1 and MVP 2, then work out how to automate testing of those features. Pavel corrected the sequence: requirements are step two, the MVP split and automation come after.

Pavel also said some of these capabilities belong to MVP 2 rather than MVP 1. MVP 1 is what they want done by October 1; MVP 2 is what they want by November 1. He noted November 1 could easily become October 21, because of the next expo in Georgia.

**Which projects are in scope.** Pavel named FlexPay, Flex IQ and FlexPort; Andrei Bosik said transactional is wider than that and that he had linked Flex Recycler in as well, since it also has a WiFi module. Pavel ruled Recycler out — it is not MVP 1 and not even MVP 2.

**Dates.** Irina pushed on the schedule so nobody relaxes: after the 18th they want a version they can hand to Andrei Klimovich to install on his own devices and see what comes out. Pavel put it at a week — a version of FlexPay and FlexPort for Klimovich to start testing and say what does or does not satisfy him. Irina then worked backwards from the field deployment on the 1st: about a week is needed for Eclipse to issue certificates, and the machine itself has to go for certification with about a week for that, so the machine must be handed over by the 24th at the latest. Andrei Bosik questioned whether this is being certified at all; Irina said she had been told it would be but thought that answer might have been a mistake.

**The filtering problem, and what was decided about it.** Pavel put a JIRA filter on screen showing the recently created capabilities. Irina complained that all the requirements and capabilities are dumped in one pile, and that the filter only works by reporter. Chudzinau said from an outside view he would either add markers or use consistent naming so FlexPay and Flex IQ can be told apart — reading a capability about a controller, you cannot tell which product it belongs to. Alexander Biratko asked whether there is a component column that could mark what each capability relates to. Dmitri Kovalchuk confirmed components do not exist yet in the capability project and have to be created.

The team settled it: Kovalchuk creates the components, the others post the component list into this meeting's chat so he can create them quickly, and Irina will then go through the capabilities and tag them, roughly an hour later. The components are per product — FlexPay, Flex IQ, FlexPort, and a Terminal Hub. Cloud services are not being broken out separately for now. Chudzinau's guidance settled where a capability hangs: put it on the product project, Flex IQ or FlexPay, and let the engineers decide afterwards which repository the change belongs in and whether it is even possible. Pavel asked whether more than one component can be selected on an item; Irina did not know.

Separately, Pavel said he would create the fix versions for MVP 1 and MVP 2. Irina noted earlier in the meeting that capability 145 — the WiFi link location network work — sits alongside everything else even though it is not MVP, and asked whether status could be used to hold it back. Pavel said that hanging capabilities off fix versions is the only clean way he sees to separate MVP from non-MVP, and that the versions have to be named per product rather than just "1.0". He noted capability 145 is a hardware implementation and there is no telling when it will be ready.

**How to record disagreement.** Alexander Biratko pressed for a mechanism: if he reads a capability and does not agree with it, what is he actually supposed to do. Irina said comments can be left on the capability itself. Pavel said a comment is fine but the item still has to land on some list that needs discussion. Andrei Bosik suggested simply writing in the chat, and the group agreed on this meeting's chat as the place, with comments on the capability as well where a discussion is useful. Biratko also asked what the result of the review should be; Pavel answered: say what you disagree with, what is missing, spot the obvious mistakes, and note where a requirement is linked, where the linked one is inadequate, and where none exists and has to be created.

**Closing.** Pavel's plan for the rest of the day: everyone studies the capabilities, then he tries to get Andrei Klimovich into a meeting to go through them by voice, and Claude drafts the requirements from that. Andrei Bosik and Dmitri are to do the studying so the others are not pulled off their work, and Alexander Biratko is to look at the FlexPay capabilities discussed that morning.

## Decisions Made

- **The capability → requirements → features workflow stands** — features are created under requirements, and Claude verifies automatically that a closed feature satisfies the acceptance criteria attached to its requirement. Accepted despite not covering 100% of functionality, on the basis that around 80% coverage still removes a large block of manual testing. (Pavel Frolov, with the group)
- **Requirements come before features** — the first stage is to go through the capabilities created in the last seven days, drop the ones no longer relevant, and write the requirements. The MVP split and the test automation come after. Pavel corrected Andrei Bosik's proposed order to put requirements second. (Pavel Frolov)
- **MVP 1 targets October 1; MVP 2 targets November 1** — and November 1 may move to October 21 because of the Georgia expo. (Pavel Frolov)
- **Flex Recycler is out of scope for both MVPs.** (Pavel Frolov, overruling Andrei Bosik's inclusion of it)
- **Components will be created in the capability project, per product** — FlexPay, Flex IQ, FlexPort and Terminal Hub. Dmitri Kovalchuk creates them; the team posts the list in the meeting chat; Irina tags the capabilities afterwards. (Dmitri Kovalchuk, Irina Shishko, Pavel Frolov)
- **Cloud services will not be split out as a separate component for now.** (Pavel Frolov)
- **A capability hangs on the product project — Flex IQ or FlexPay — and the engineers decide the repository afterwards.** (Dzmitry Chudzinau, accepted by Pavel Frolov)
- **Fix versions will be created for MVP 1 and MVP 2, named per product rather than just by number** — Pavel's view that this is the only clean way to separate MVP from non-MVP. (Pavel Frolov)
- **Disagreements about capabilities go into this meeting's chat**, with comments on the capability itself where a discussion is useful — rather than a separate tracked list. (Andrei Bosik and Irina Shishko proposed; Pavel Frolov and the group agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dmitri Kovalchuk | Create the components in the capability project: FlexPay, Flex IQ, FlexPort, Terminal Hub | September 10, 2026 | High | Asked for the list in the chat so he can create them quickly |
| 2 | Irina Shishko | Post the component list into the meeting chat, then tag the capabilities with their components | September 10, 2026 (about an hour after the components exist) | High | She said she is on something else right now |
| 3 | Pavel Frolov | Create the fix versions for MVP 1 and MVP 2 in JIRA | September 10, 2026 | High | The mechanism agreed for separating MVP from non-MVP |
| 4 | Pavel Frolov | Call a meeting with Andrei Klimovich to walk through every capability by voice and agree the requirements, including the question of who writes them | September 10, 2026 | High | Chudzinau's objection is to be raised in that meeting; Claude drafts the requirements from the result |
| 5 | Andrei Bosik + Dmitri | Study the capabilities created in the last seven days before the Klimovich meeting, and flag disagreements, gaps and missing requirement links | September 10, 2026 | High | Assigned to these two so the rest of the team is not pulled off their work |
| 6 | Alexander Biratko | Review his own FlexPay capabilities, the ones discussed that morning | September 10, 2026 | Normal | |
| 7 | Whole team | Read the capabilities before the meeting with Andrei Klimovich | September 10, 2026 | Normal | Pavel said this has to happen in any case before that meeting |
| 8 | Pavel Frolov | Hand a version of FlexPay and FlexPort to Andrei Klimovich so he can install it on his devices and test | September 17, 2026 (a week out; Irina wants it after the 18th) | High | Irina raised the date; Pavel put it at a week |

## Open Questions

- Whether the business or the engineers should write the requirements, and whether a reporter should be able to leave a capability with no requirements attached. Raised by Dzmitry Chudzinau; Pavel is taking it to the meeting with Andrei Klimovich.
- Whether this work is being certified at all. Andrei Bosik questioned it; Irina had been told it would be but suspects that answer was a mistake.
- Whether more than one component can be assigned to a single capability. Pavel asked; Irina did not know.
- When capability 145 — the WiFi link location network — will be ready. Pavel said it is a hardware implementation and there is no telling.

## Dispatch Log

---
*Processed from Teams transcript on September 10, 2026*
*Source meeting: Transactional products management (From Caps-Reqs to Work Done+AutotestsByAccptance)*
