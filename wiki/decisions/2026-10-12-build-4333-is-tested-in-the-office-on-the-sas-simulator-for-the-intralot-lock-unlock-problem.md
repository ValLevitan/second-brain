---
type: decision
title: Build 4333 — which carries a lock/unlock fix — is tested in the office on the IGT SAS simulator to see whether a machine still stays locked after Intralot unlocks it; Pavel investigates the lock behaviour
date: 2026-10-12
aliases: [Intralot lock unlock, lottery lock, machine stays locked, locked by accounting system, build 4333 lock fix, Megahits build 4333, IGT SAS simulator, test lock unlock in office, build 3866, Peach vertical build]
source-count: 2
status: active
open-commitments: 4
open-questions: 1
---

# Build 4333 is tested in the office for the Intralot lock problem

Agreed by [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/felipe-miranda.md|Felipe Miranda]], with [[wiki/people/irina-shishko.md|Irina Shishko]] finding the build number, at the [[wiki/meetings/2026-10-12-ris-mvp2-scope-and-release-timing.md|Oct-12 RIS MVP 2 call]] (English). Quotations from [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]].

## The problem (Felipe)

"sometimes machines are disconnected from Intralot for any reason from the server, from their SAS, RS232 port." When they come back, "we stay locked by accounting system until someone manually goes out of service, operational, out of service, operational, exit". Meanwhile "the lottery is not able to unlock the machine from their server because our machine stays in locked."

Pavel restated it: after Intralot locked and then unlocked the machine, "Our machines still left in the state of locked until you manually switch it to unlock." Felipe: "Right… you have to go from locked to out of service to operation."

What the lottery told Felipe: "when they are locked by the lottery, you are not supposed to unlock it manually… There shouldn't be that possibility. If it's locked, it's locked. But because they unlock it, you can". "But… it doesn't do it automatically. That is a problem."

Felipe has evidence: "I took logs and I sent to lottery and I sent to you at to Juan at some point, so I have all the history of this." He will forward the exchange with Juan and the lottery, and "I believe that Juan was working on this with you guys, but… I will find out."

Felipe: "we have a meeting with Val tomorrow at Intralot in the morning, and I think it's something that he wants to discuss there" (tomorrow = Oct 13 2026).

## Which build has the fix

Pavel: a fix "related to lock-unlock" was introduced in the latest software. Felipe first took it to be the last build sent to the lab: "Peach vertical… build. 3866. I believe." Irina looked it up; Pavel: "4333 version." Felipe: "Oh no, this is just released. This is Megahit Hits. This is the new version that is not even installed."

## The ruling

Felipe: "we have the IGT SAS simulator here. We could try to simulate locking, unlocking, locking, unlocking, see what happens." Pavel: "in Office, we can do this testing right now, I think." Pavel: "Testing in office this version 4333. You give us some more information about locked and unlocked." Felipe: "Okay, 4333, got it." Pavel: "we will observe and understand if it actually fix or probably we need to continue fixing." Pavel also: "At least we will need to make an investigation related to lock and lock behavior."

## How it sits against earlier items

- **Oct 5.** Felipe raised the same lock at the RIS MVP 1 review; Val: "It cannot be Mvp one right now", for a separate meeting, and Felipe was to share his email thread with Val — [[wiki/decisions/2026-10-05-ris-improvement-mvp1-is-five-jira-capabilities-in-one-release-due-october-19.md]]. Oct 12 adds the detail, the build with a fix, and the Intralot meeting (**evolution**).
- **Build 4333.** On Oct 5–6 Felipe called 4333 the new Georgia V3 build, approved on Monday Oct 5, and said earlier machines would be upgraded to it — [[wiki/decisions/2026-10-06-the-ten-arc-machines-are-released-this-week-with-modems.md]]. On Oct 12 he calls it the new "Megahit Hits" build, not yet installed. Mega Hit is a Georgia game title in the corpus, so these are read as the same build (**inference**, no conflict).
- The lottery side is on [[wiki/organizations/georgia-lottery-corporation.md]] (Oct 12).

## Open commitments

- [ ] [[wiki/people/felipe-miranda.md|Felipe Miranda]] — test build 4333 in the office on the IGT SAS simulator (lock, unlock, repeat) and report what happens — due unspecified — [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]
- [ ] [[wiki/people/felipe-miranda.md|Felipe Miranda]] — forward the email exchange with Juan and the lottery on the lock to the team — due unspecified — [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]
- [ ] [[wiki/people/felipe-miranda.md|Felipe Miranda]] — find out whether Juan was working on the lock with the developers — due unspecified — [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — investigate the lock/unlock behaviour — due unspecified — [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]

## Open questions

- Why does the machine stay locked after Intralot unlocks it, and does build 4333 fix it? Felipe: "I don't know why that happens" — [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]

**§15.8:** clear. **§15 #9:** none; 3866 and 4333 are software build numbers.

## Sources

- [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]
- [[raw/Meeting_Notes_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]
