# Meeting Summary — Transactional MVP1: CAPs, REQs, UI/UX

**Date:** September 18, 2026, 8:03 AM - 9:11 AM Eastern
**Duration:** approximately 1 hour 8 minutes
**Attendees:** Andrei Klimovich (organiser), Pavel Frolov, Dzmitry Chudzinau, Irina Shishko, Alexander Biratko, Andrei Bosik
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026]]
**Source meeting:** Transactional MVP1: CAPs, REQs, UI/UX — Microsoft Teams

**Note:** Val did not speak on this call. He took part by writing in the meeting chat, and the team read his messages out loud twice ("Val wrote: remove it from MVP1", "178 — must be MVP1").

## Summary

The daily MVP1 call, and a working session rather than a discussion. Two things happened: the team walked the whole MVP1 capability list one by one and cleaned it, and then walked it a second time to plan the features. A hard date was set — **Monday** — by which every capability, feature and non-functional requirement must exist, be thought through, sit in a proper status and have an owner.

**The opening problem.** Klimovich said the daily capabilities report still shows about 80 items in states that count as incomplete, and they are classified as blockers. That should not be the case. He asked the team directly what is stopping them from building features.

**Chudzinau's answer — the requirements contradict each other.** Starting the next feature yesterday, he hit a blocker: the requirements on one capability demanded a PIN code for the wallet, even though the team had dropped the PIN. The list ended up holding both requirements that need a PIN and requirements that do not. That led him to run the whole MVP1 set — Flex IQ, FlexPort and the cloud work — through Claude looking for conflicts, contradictions and blockers. It produced a document, which he shared in the chat; his own team has since reworked part of it, not all. His recommendation for the future: after the requirements are written and linked by hand, run them through the tool to find conflicts. His ideal next step is to ask for a **specification document** describing how MVP1 actually works, because reading it end to end would show at a glance whether it is what was intended — today it would say both that a PIN must be entered and that it must not.

**Firmware rollback — dropped.** The first capability opened was the one requiring the ability to roll back to a previous build. Chudzinau explained why it does not work for their software: the database structure changes over time, so rolling back to an older build leaves a schema that does not match. The system may fail to come up, or come up empty. His example was deleting a wallet table when moving to the cloud, then wanting to go back — the structure has changed and the data is gone. The proper answer is to issue a **new** version resembling the wanted one, raising the needed commits and dropping the rest; there is then no database conflict and the wanted behaviour is reproduced. He added a second objection: nobody is there to supervise such a rollout, and a control-panel operator would not know the details. Klimovich pressed with the real-life case — a bad build is pushed to the IQs in locations, what do we do? The answer: if the build will not boot at all, the previous one will not boot either; if something merely displays wrongly, it is faster to ship an update. Bosik backed it strongly — there are different development styles, forward and backward, and the team should always hold to **forward**: find a bug, release the next version, update, carry on. Val wrote in the chat to remove it from MVP1, and it was removed.

**Capability-by-capability cleanup.** Klimovich then filtered for anything sitting below "in progress" or unassigned, and the team worked through it:

- **178 (InComm card configuration — multiple products)** — yesterday's subject. Klimovich was not ready to move it forward: either it goes to MVP2 or it stays in a severely cut-down form. Val's chat message said it must be in MVP1. Klimovich's near-final position is that **two products will not be built for MVP1**, but support for **one** product — SkillPay — is possible, since everything already works. Pavel said the server side is easy and the operator interface can be added; what is needed is the card data and a graphical check. Klimovich is finishing the windows for it.
- **144 (Bosik's)** — Pavel said it looks like a separate project that plainly will not be delivered inside MVP1, at least not in full. Irina's fix was adopted: **clone the capability**, keep three or four requirements in the MVP1 copy and let the rest live in the clone parked on MVP2, rather than moving items one at a time and losing them. Bosik read the remaining requirements and initially said all were still needed; Pavel then challenged the last one — that a master board change must not lose money and must be documented. With no cloud version of tickets, an un-cashed ticket does not transfer to a new device, so it is not MVP1. Bosik removed it. He owns the capability: rewrite the description to match what is left, clean it, move it to the next status, **today**.
- **117, 79, 80, 116, 156** — all FlexPay items sitting in MVP1 by mistake. Moved to MVP2 and put on Biratko. 156 stays with Chudzinau for the implementation, which Biratko will then port across — Pavel described it as essentially a copy.
- **151 (Flex IQ in the port environment)** — the cloud and MG-environment wording removed. This opened the bigger question below.
- **163 (access to the eWallet)**, **the location-block enforcement capability**, **174 (reprint)**, **176 (how money is withdrawn)**, **148, 149, 150** — all assigned to Chudzinau. On 176 the FlexPay references in the text are to be removed. **150** is the balance display: gaming-machine agnostic, the balance must be shown on any machine. Klimovich says something exists but not in the form the requirements describe, and this is a release version, so it has to be shown to people in a properly human-readable way. Pavel expects the gap will turn out to be design only.
- **175 (wallet records — creation, balance updates, ACH, cloud)** — Irina called it MVP2 and flagged it as a possible duplicate of reporting already discussed elsewhere. Klimovich will **not** move it yet: first he has to confirm that the logic described here, which currently references the cloud, is described somewhere else too. Assigned to Chudzinau in the meantime.
- **180 (FlexPort session life — waiting mode, inactivity timeout)** — previously scattered in pieces, now collected into one capability. It was assigned to Biratko, which Pavel and Irina both called wrong: requirements should not be hung on a developer. Reassigned to Pavel.
- **The audit ticket** (the daily audit printout at a location) — Klimovich's own, unfinished. Irina told him to mark it so it does not drift out of MVP1; he confirmed it stays and will be completed.

**Two environments or one.** Coming off 151, Pavel asked whether FlexPort must support two environments in MVP1 — one connected through SAS, one through bill-acceptor and counter emulation. Klimovich proposed focusing MVP1 on **dual SAS only**, noting this is still an open business question (some operators say dual SAS covers all their machines, others do not). Pavel supported it for a practical reason: supporting both is close to double the testing. The agreement was dual SAS only for MVP1, with **MVP1 locations chosen so they are fully equipped with dual-SAS machines**, and the testing effort put into automation so the second environment can be covered much faster later.

**Nothing gets closed yet.** When the team started marking finished capabilities as complete, Chudzinau stopped it. The Claude conflict run may have pushed new requirements into capabilities whose existing features already closed the old ones — in which case another feature has to be opened. Until that is worked through, nothing is closed.

**The Monday deadline.** Klimovich restated the deadline put to the team: by Monday all capabilities, all features and all non-functional requirements are created, thought through, in the right statuses, with nothing unassigned. He will close everything that sits on him. From Monday the team starts building and **nothing more may fly into MVP1** — a rule he said applies to himself as well. Chudzinau named what would block him most: the reworked **window designs**, and the requirements split across two products and two cards. He is waiting on designs for several capabilities, otherwise the team keeps returning to the same questions.

**Non-functional requirements.** Most are created — Irina and Pavel covered FlexPort, Chudzinau covered Flex IQ, Klimovich his own side. Chudzinau thinks a significant part is definitely covered with details outstanding. Irina and Pavel will sit together and walk the list. Irina also wants a second pass over the **acceptance criteria** on every MVP1 requirement; they are present everywhere, but she wants to confirm nothing is half-written.

**Feature planning (second half).** Pavel shared the board and the three of them walked it:

- **122** — Chudzinau will run tests over the weekend and close it if they go well.
- **118** — features exist and look ready; moved from backlog to To Do, on Chudzinau, with a feature still to be planned.
- **165 / FlexPort 9 and 10** — Pavel to plan his own; one in-progress feature has no commit against it, so he has to check which branch it merged into before deciding whether to close it as a duplicate.
- **173** — the last of Pavel's to be scheduled.
- **152** — Chudzinau's; he and Irina will meet and walk his features rather than guess dates in the meeting.
- **Receipt printing** — the template is ready. The receipts are the same on both sides; only the printing logic differs (at the FlexPay the cashier chooses, in self-service the player chooses the language). The **receipt format — which fields are printed** — has to come from Klimovich and still has not been given. The team can print fields by their own judgement, but the actual order and content is his.
- Nothing more can be planned for MVP1 until Chudzinau creates his features. He does that, tells the others, and the three of them plan the rest.

**Cadence.** Klimovich confirmed the daily call continues Monday through Friday at the same time. He is reachable all weekend and asked people not to wait until Monday with questions — which he openly described as a gentle hint that the weekend is workable. Irina and Pavel will be working on Sunday.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Rework capability 144 — remove the master-board/lost-money requirement, rewrite the description to match what is left, move it to the next status | Today (Sep 18), end of day | High | He said he would do it straight after the meeting |
| 2 | Andrei Klimovich | Finish the reworked window designs, starting with capability 178 | By Monday (Sep 21) | High | Named by Chudzinau as his single biggest blocker |
| 3 | Andrei Klimovich | Give the receipt format — which fields are printed and in what order | Not set | High | Outstanding for some time; blocks the printing features |
| 4 | Andrei Klimovich | Confirm that the logic in capability 175 that references the cloud is described elsewhere, then decide whether 175 moves to MVP2 | Not set | Normal | He refused to move it before checking |
| 5 | Andrei Klimovich | Take Chudzinau's Claude conflict document as the base and rework the remaining findings while adding new capabilities | Not set | High | Blockers closed, discrepancies remain |
| 6 | Andrei Klimovich | Finish the daily audit-ticket reporting capability and keep it inside MVP1 | By Monday (Sep 21) | Normal | Irina asked him to mark it so it does not drift |
| 7 | Andrei Klimovich | Close everything assigned to him — capabilities, features, non-functional requirements — in correct statuses | By Monday (Sep 21) | High | His own commitment against the team deadline |
| 8 | Dzmitry Chudzinau | Create features under all of his capabilities — they are currently bare — then tell the others so planning can continue | Not set (blocks everything else) | High | The whole MVP1 plan waits on this |
| 9 | Dzmitry Chudzinau | Run the tests on capability 122 over the weekend and close it if they pass | Weekend of Sep 19–20 | Normal | He offered it |
| 10 | Dzmitry Chudzinau, Irina Shishko | Meet after the call and walk his capabilities and features to set real dates | Not set | Normal | Dates were not to be invented in the meeting |
| 11 | Pavel Frolov | Plan his own features — 165, FlexPort 9 and 10, 173 — and check which branch the uncommitted in-progress feature merged into | Not set | Normal | May turn out to be closable as a duplicate |
| 12 | Pavel Frolov, Irina Shishko | Walk the non-functional requirements list together, FlexPort side first | Not set | Normal | Chudzinau covers the Flex IQ side |
| 13 | Irina Shishko | Second pass over the acceptance criteria on every MVP1 requirement to confirm nothing is half-written | Not set | Normal | They exist everywhere; completeness unverified |
| 14 | Alexander Biratko | Port Chudzinau's implementation of 156 to FlexPay once it is done, and set his dates after Chudzinau's | After Chudzinau delivers | Normal | Pavel described it as essentially a copy |
| 15 | Team | Build automated tests so the second (bill-acceptor / counter emulation) environment can be covered quickly after MVP1 | Not set | Medium | The price of deferring it to MVP2 |

## Decisions

1. **Firmware rollback is removed from MVP1.** The development policy is roll forward only — find a bug, release the next version. A rollback is unsafe because the database schema changes between builds and data can be lost.
2. **MVP1 supports dual SAS only.** The bill-acceptor and counter emulation environment is deferred, and MVP1 locations will be chosen so they are fully equipped with dual-SAS machines. Reason: supporting both nearly doubles the testing.
3. **Two InComm products will not be built for MVP1.** Klimovich called this almost final. Support for a single product (SkillPay) is the fallback, against Val's chat instruction that 178 must be in MVP1.
4. **Capability 144 is cloned** — a trimmed MVP1 copy keeps three or four requirements, the clone holds the rest on MVP2. Cloning replaces moving items one by one, which risked losing them.
5. **All FlexPay capabilities (116, 117, 79, 80, 156) move to MVP2** and go to Biratko.
6. **Capability 180 is reassigned from Biratko to Pavel Frolov.** Requirements are not hung on developers.
7. **Monday is the MVP1 scope freeze.** Everything created, statused and assigned by then; after that nothing new enters MVP1, Klimovich included.
8. **Nothing is closed** until the conflict findings from the Claude run are worked back into the capabilities — a closed feature may no longer cover the requirements now attached to it.
9. **The daily MVP1 call continues Monday to Friday** at the same time. Weekend contact is open, and Irina and Pavel will be working Sunday.

## Open items

- The dual-SAS versus dual-environment question is settled for MVP1 but remains an **unresolved business question** — operators disagree on whether dual SAS covers their fleets.
- Whether 175 duplicates reporting already covered elsewhere is unverified.
- Val's chat instruction that 178 must be in MVP1 sits against Klimovich's near-final position that two products will not be delivered. Not reconciled on this call.

---
*Source meeting: Transactional MVP1: CAPs, REQs, UI/UX — Microsoft Teams, September 18, 2026*
*Raw transcript: [[Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026]]*
