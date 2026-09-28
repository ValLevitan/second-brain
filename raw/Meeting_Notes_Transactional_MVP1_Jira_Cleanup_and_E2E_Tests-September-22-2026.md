# Meeting Summary — Transactional MVP1: CAPs, REQs, UI/UX

**Date:** September 22, 2026, 8:01 AM - 9:23 AM Eastern
**Duration:** approximately 82 minutes
**Attendees heard:** Val Levitan, Andrei Klimovich, Pavel Frolov, Dzmitry Chudzinau, Irina Shishko, Andrei Bosik, Alexander Biratko
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026]]
**Source meeting:** Transactional MVP1: CAPs, REQs, UI/UX — Microsoft Teams

## Summary

Four blocks: Andrei's screen design, a live clean-up of the MVP1 capability list in Jira, the October 2 date, and the missing end-to-end tests. The last one took most of the meeting and ended with a one-hour micro-step for tomorrow.

**Screen design.** Andrei Klimovich finished the design logic for the IQ screen, laid out the same way he did for FlexPort — all zones described, how controls are drawn and where they land. He has started rebuilding the mockups to that logic and needs three to four more hours today to finalise it and load it into Jira, for both IQ and FlexPort. In parallel he is adding product selection to the Redeem screen for two-product support; while there is only one product the field stays informational and cannot be selected. He also removed every mention of "cloud" from MVP1 — the version is now agnostic about where the wallet is stored and verified.

Val's two wording corrections: the fee line should read **maximum $1000, and the player gets $2 less**, not "$1000 max minus $2" — Andrei accepted and will show price pay minimum $5, maximum $1000, fee $2, with the freed area used for errors. And the English word "empty" is wrong; the right word is **"blank"**.

Val said openly he had not gone deep into the screens — he missed two meetings, Andrei has the most up-to-date knowledge from client presentations, and Val treats Andrei's requirements as dogma for now; even if mistakes slip in Val would probably have missed them too. Andrei added a disclaimer: he insists the next IQ version follows his UX and workflow proposal, but for visual design he proposes reusing the existing IQ design language rather than drawing anything from scratch.

**Texts and localisation.** Andrei wants an English–Spanish text collection that anyone responsible, not only a developer, can change, published to a library the next client build picks up. Val said Andrei Bosik should own it, that the standard is strictly mandatory, and pointed at the standards repo — standards must be simplistic and single-purpose, hundreds of small .md files that keep growing. Pavel posted the path where the FlexPort translations already live: an XML format, English text then Spanish text with IDs, compiled into the software at build time. Irina noted that path covers FlexPort only, not FlexIQ. Andrei agreed to convert his library to that format; the correction flow is a pull request, and the text reaches the machine at the next build. Dzmitry raised server-side over-the-air text updates; Andrei said he would be happy to get there but does not need it for MVP1 or even MVP2.

Val pushed back that this was mixing an architectural decision with a business requirement. Andrei argued it is an operational or product requirement, not architecture — he may say how he wants it to work and the engineers decide how to build it. Val: "not how you would like it, but what the market requires," citing Steve Jobs on not running market surveys. Andrei accepted it as semantics and moved on.

**Jira clean-up (live, with Pavel sharing his screen).**
- **CAP-178** (SkillPay / price pay setup, multi-product support) is the only MVP1 capability still in Proposed. Andrei will move it to Accepted today with the right requirements and mockup links, and will add two design capabilities straight in Accepted.
- **CAP-115** (FlexPay registration) — Irina argued a FlexPay capability has no place in MVP1, because FlexPay is not checked or released in MVP1. Val agreed with Irina; Dzmitry agreed; it moves to MVP2.
- **CAP-157** — Dzmitry said it is written abstractly, duplicates other capabilities, is partly implemented already, and there is nothing to create features from; he would remove it. Andrei defended it: it describes creating a new wallet at the FlexPort collector moment, with behaviour differing by gateway type — on IQ a ticket is created and printed, on self-service kiosks there is no auto-print and the logic runs through a claim code. Val closed the argument: this dispute is not needed, requirements can always be moved to another capability. REQ-1473 is already attached to CAP-156 (FlexPort), so CAP-157 ends up empty. Pavel removed it from MVP1 and moved it to MVP2; Andrei will look later at whether it survives at all.
- **CAP-148** was identified as the capability covering wallet issue on FlexIQ.
- **CAP-180** (FlexPort Player Session Lifecycle) — Andrei will fill it with the design content rather than create a new capability, and move it to To Do so its green Accepted colour stops reading as "done". Pavel noted a task on this was already given to Dmitri Kovalchuk and it still went green, so it needs another pass. Andrei and Irina also noted the visual problem: Accepted is green and To Do is grey, which makes To Do look like a more advanced state.
- **FIQ-34** was put into the backlog by Dzmitry during the call.
- Irina's non-functional requirements list — Andrei has not got to it; at most a preview tomorrow.

**How Claude builds features.** Andrei asked how the developers work. Dzmitry: he points Claude at a capability with its linked requirements and asks it to write the features; Claude already knows the repositories and decides the scope itself — the better everything is written, the less confusion. Andrei asked whether Claude reads "related" links or only "required by"; Pavel and Irina both believe it takes all link types. Andrei was worried about cascading analysis drifting away; Dzmitry said the focus still stays on the current capability's own text. Dzmitry recalled the failure that made him ask for the linkage to be fixed: Claude started creating wallet-behaviour features in a repository where none should be created.

Andrei will send a separate change list of the capabilities where he adds new requirements, so the team can ask Claude to re-read them. Pavel called that very useful — today such features are found too late, at implementation. Dzmitry suggested resetting status to flag it; Irina corrected him — To Do or Accepted, never In Progress, since In Progress means a feature is already being worked. Andrei will keep it to a plain change list for the next day or two and think about the process later.

**Schedule.** Pavel showed the MVP1 work ending roughly October 2. The view was polluted by MVP2 items, so Irina proposed splitting the initiative in two — one covering FlexIQ, one covering FlexPay, which is MVP2. Val liked it and Pavel created it during the call. Val objected to the naming: he does not want the kiosk described as "kiosk" — it should be **FlexPay**, because "we need to be consistent with our standards."

Val then challenged the date: most of the work is done, so why another 10 days? Pavel: "because before that there were 2 years." Dzmitry: there is completed functionality but also clarifying requirements that still have to be satisfied, plus genuinely new functionality such as FlexPort blocking. Val asked twice for a more honest answer. Pavel said nobody wants to delay the dates, everyone is interested in the opposite. Val agreed the group is honest and there is no dispute — but he **left the date question open and said he wants to see different dates.**

**Acceptance criteria and end-to-end tests.** Irina estimated 60–70% of the requirements have acceptance criteria that she and Claude reviewed and that all pass; the rest are still missing, and Andrei creates more today. No end-to-end tests are written at all — nobody has done this work. Irina said they would release whether or not the tests exist, and that this is not right for this release. Val said the only way to release on the 2nd is if developers help write the E2E tests, or at least supervise. Pavel refused to release Dzmitry and Alexander, and offered Evgeny (Zhenya); Anton is building a FlexPay emulator that QA will need, so he stays where he is.

Dzmitry warned that testing this platform is nothing like testing a machine: Kubernetes clusters, cloud structure, environments that have to be raised and deployed, and it cannot simply be isolated in a Docker container — it is a separate product and needs Andrei. Pavel narrowed it: the machine ↔ FlexPort ↔ FlexIQ part can be tested now, and most errors will sit there. What will stretch into next month is testing real FlexPorts connected to other manufacturers' machines, for example in the Georgia office, since JVL only knows how SAS behaves on its own machines.

Val's answer: there is no time, and Klimovich can confirm the commitments being made. In theory — and he repeated that he is not an engineer — with well-described requirements and acceptance criteria, features, code in the right repositories and prose written, Claude should manage it. He gave a concrete business case: a customer in Texas wants two machines with JVL's own dispenser — two machines, two ports, JVL dispenser, the entire ecosystem JVL's — so the E2E tests can be written against JVL's own ecosystem. He accepted Pavel's point that other people's machines will bring further problems later, and asked to solve the first problem first.

The group agreed to build the autotest features **inside the existing capabilities** (Pavel's position) rather than in a separate one, so test writing does not get separated from the main work. Val asked for a **micro-step by tomorrow**: pick any single test needing about an hour, create it, run it, and see the result — otherwise the same dilemma repeats on every release. Everyone agreed. Pavel specified the first test: the current FlexPort firmware already connects to FlexIQ and to the machine over SAS, so test that it returns "connected" with the cable in and "not connected" with it out; the FlexPort state can be read through the telnet hook. He expects Alexey (Lyosha) to write it in one to two hours. Irina attached it under CAP-173. Val also asked to put Ivan Shpak and Alexey Khamin on the test work in the schedule, pointing out that the schedule has a scope nobody is looking at although the release depends on it.

**Dependency updates.** Val asked whether the products they build on need regular updates. Dzmitry explained the Java platform and frameworks release new versions, and raising a version is a deliberate decision that requires recompiling, not an automatic update. Alexander Biratko narrowed it to two cases: a vulnerability in a library JVL uses that actually affects them, or missing functionality a newer library would provide — otherwise no. Pavel: any update, like on a phone or a computer, is one more chance to break everything. Val closed the question. Andrei Bosik added that the cloud side is different — AWS pushes changes constantly, he gets the notices, reviews them roughly every two weeks and changes code where an API is affected; it cannot be automatic, and modules must be updated in dependency order. Pavel added that GitHub Actions are warning about the Node version moving from 20 to 24 and will have to be brought up to date across all repositories.

**KORE SIM in IQ.** Andrei Klimovich recalled that the modem in the IQ differs from the one in the game machine, and the KORE SIM was only brought up on the game machine — but IQ in MVP1 has to work over LTE on the KORE SIM. Pavel asked him to put the KORE SIM into the IQ, switch it on and leave it online so they can work with it remotely. Andrei will do it today and report. Andrei Bosik noted the Georgia office router keeps dropping despite Elizabeth's assurance that it would not; Andrei Klimovich thinks the office power goes off in the evening.

The meeting ended when Irina's Claude froze while she was creating the feature. Val closed it: tomorrow they check whether the one E2E test flow worked, and plan the schedule for the remaining tests.

## Decisions Made

- **CAP-115 (FlexPay registration) moves from MVP1 to MVP2** — FlexPay is not verified or released in MVP1, so a FlexPay capability does not belong there. (Irina Shishko proposed, Val agreed, Dzmitry Chudzinau agreed.)
- **CAP-157 is removed from MVP1 and moved to MVP2; its requirements attach elsewhere** — it duplicates other capabilities and REQ-1473 already sits on CAP-156. Andrei will decide later whether it is needed at all. (Val ruled, Pavel executed.)
- **The new screen design goes into CAP-180, not a new capability, and CAP-180 moves to To Do** — avoids duplication, and stops a green Accepted state reading as finished. (Pavel and Andrei Klimovich.)
- **The initiative is split in two — FlexIQ and FlexPay — so the schedule shows MVP1 correctly.** (Irina proposed, Val approved, Pavel created it in the call.)
- **The kiosk is called FlexPay, never "kiosk"** — consistency with JVL's own standards. (Val.)
- **Texts move into the existing FlexPort XML format at the path Pavel shared, updated by pull request and compiled at the next build; Andrei Bosik owns the text library.** Over-the-air text updates are not required for MVP1 or MVP2. (Val, Andrei Klimovich, Pavel.)
- **Autotest features are created inside the existing capabilities, not in a separate capability** — so test writing is not split off from feature work. (Pavel proposed; Val agreed and said getting it wrong the first time is acceptable.)
- **One micro-step by tomorrow: create and run a single E2E test** — FlexPort connection state to FlexIQ and to the machine, read through the telnet hook, filed under CAP-173. Everyone agreed. (Val asked for it, Pavel specified it, Irina filed it.)
- **Screen wording: "maximum $1000 and the player gets $2 less", and "blank" instead of "empty".** (Val; Andrei accepted both.)
- **Dependency updates stay manual and deliberate** — only for a vulnerability that affects JVL or for functionality JVL needs. (Dzmitry, Alexander Biratko, Pavel; Val closed the question.)
- **Not decided: the October 2 date.** Val explicitly left the question open and said he wants to see different dates. He accepted that nobody is padding the estimate.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Finalise the IQ and FlexPort screen design and load it into Jira | September 22, 2026 | High | He estimated 3-4 hours |
| 2 | Andrei Klimovich | Move CAP-178 (SkillPay / two-product support) to Accepted with requirements and mockup links | September 22, 2026 | High | He estimated about 2 more hours; the only MVP1 capability still in Proposed |
| 3 | Andrei Klimovich | Fill CAP-180 (FlexPort Player Session Lifecycle) with the design content and move it to To Do | September 22, 2026 | Normal | So it stops showing as done |
| 4 | Andrei Klimovich | Convert his text collection to the FlexPort XML format Pavel shared | TBD | Normal | Pavel posted the path in the chat |
| 5 | Andrei Klimovich | Send the team a change list of capabilities where he added new requirements | September 24, 2026 | Normal | He said "in the next day or two"; lets the team ask Claude to re-read them |
| 6 | Andrei Klimovich | Install the KORE SIM in the IQ, activate it, leave it online for remote access, and report back | September 22, 2026 | High | IQ in MVP1 must work over LTE on the KORE SIM |
| 7 | Andrei Klimovich | Preview Irina's non-functional requirements list | September 23, 2026 | Low | He said a preview is the most he can do tomorrow |
| 8 | Irina Shishko | Create the autotest features under the existing capabilities and plan them | September 22, 2026 | High | Agreed approach is features inside existing capabilities |
| 9 | Alexey Khamin | Write and run the first E2E test — FlexPort connection state to FlexIQ and the machine, read through the telnet hook, under CAP-173 | September 23, 2026 | High | Pavel named "Lyosha" and expects one to two hours; Val wants the result checked tomorrow |
| 10 | Irina Shishko | Start with Evgeny (Zhenya) as the developer helping write tests | September 23, 2026 | Normal | Pavel would not release Dzmitry or Alexander; Anton stays on the FlexPay emulator |
| 11 | Pavel Frolov / Irina Shishko | Put Ivan Shpak and Alexey Khamin on the test work in the schedule | September 23, 2026 | Normal | Val: the schedule has a scope nobody is looking at, and the release depends on it |
| 12 | Dzmitry Chudzinau | Set the feature dates himself under CAP-152 | September 22, 2026 | Normal | He said he had already started one ten minutes earlier |
| 13 | Pavel Frolov | Remove CAP-157 from MVP1 and re-point its requirements; create the second initiative for the schedule | September 22, 2026 | Normal | Done live during the meeting |
| 14 | Pavel Frolov | Revisit CAP-180 with Dmitri Kovalchuk — the earlier task on it still left the capability green | TBD | Low | Raised when the status colour problem came up |

## Open Questions

- **The October 2 release date.** Val left it open and wants different dates. Raised by Val; Pavel and Dzmitry defended the current plan.
- **How to test real FlexPorts on other manufacturers' machines.** Pavel expects this to stretch into next month; only JVL's own machines can be tested now. No plan set.
- **How to test the cloud platform at all.** Dzmitry says Kubernetes clusters and cloud environments make it a separate product needing Andrei; no approach agreed.
- **Whether Claude follows "related" links as well as "required by" when generating features.** Pavel and Irina believe it takes all link types; Dzmitry was not ready to answer. Unresolved.
- **How to flag a capability whose requirements changed.** Dzmitry floated a status; Irina ruled out In Progress; Andrei parked it and will start with a plain change list.

## Dispatch Log

---
*Processed from Teams transcript on September 22, 2026 (scheduled meeting-watcher sweep)*
*Source meeting: Transactional MVP1: CAPs, REQs, UI/UX*
