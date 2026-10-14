---
type: decision
title: Ten JVL machines go into Intralot's lab (ten ports) and testing starts now, without waiting for the Lottery's formal answer; Intralot also scans the whole field for JVL machines
date: 2026-10-13
aliases: [ten machines to Intralot, fill up the ten ports, we have ten ports, we are going to start immediately, Intralot lab test, scan the whole field, lockout lab test, edge cases at Intralot]
source-count: 2
status: active
open-commitments: 3
open-questions: 2
---

# Ten JVL machines go into Intralot's lab now

Agreed at the [[wiki/meetings/2026-10-13-intralot-machine-lockouts-test-lab-and-route-partnership.md|Oct 13 2026 meeting at Intralot]]. Proposed by [[wiki/people/bill-avgeris.md|Bill]] of [[wiki/organizations/intralot.md|Intralot]], accepted by [[wiki/people/val-levitan.md|Val Levitan]], and agreed by the Georgia Lottery's representative (read as [[wiki/people/chris-boncek.md|Chris Boncek]] — **inference**). Quotes from [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].

## Why

JVL machines sometimes lock and sit out of service, and JVL does not hear about it. Val: "**our machines are just… Sometimes go out of service, out of commission, and just sit there, and we don't know about it**". He wants to find JVL's own edge-case faults — timing and negative cases — which, he says, lab certification does not test: "**The way they test is they test an ideal case without marginal cases or without negative cases.**" He wants "**to hook up the machine to your system… I'm sending a signal. I'm watching the the time that it takes**". The lock itself, and JVL's build test for it, are on [[wiki/decisions/2026-10-12-build-4333-is-tested-in-the-office-on-the-sas-simulator-for-the-intralot-lock-unlock-problem.md]].

Bill's first answer was that random field cases are hard to reproduce, and access to the test environment is for the labs and the Lottery only. Then he changed course.

## The ruling

- **Bill:** "**Wait for Val to send the lottery and waiting for the lottery. We are going to start immediately.**" (just after "We are not going to", which sits under Speaker 4's label) and "**We have ten ports. Let's install ten machines.**"
- **Val:** "**we'll send ten machines in here. Install different software into ten machines. They don't have to be brand new machines.**" And: "**it's better that they're not all brand new, right? Some couple of vertical, couple of horizontal. Send maybe one Altera just in case. Okay. Fill up the ten ports and let's start this.**" ("Altera" as transcribed; not interpreted.)
- **The Lottery representative:** "**Yeah, I'm comfortable moving ahead with that now… It's a pressing problem, obviously.**" And later: "**when you guys get the games here, you know, we can set it up and try and reproduce that scenario.**"
- **Val will staff it:** "**I will bring people here. I'll bring engineers. I'll bring my test people.**"

## The field scan that goes with it

JVL says many cases; Intralot sees two or three. Bill: "**you have raised a concern, a valid concern. Okay, we can ask our engineer to scan the field, the whole field for for your machine.**" His reason: if a machine drops off the site controller at once, "**the machine is not sending anything to us**". The Lottery representative: "**let's scan the field. Maybe we identify that a certain set is the culprit**."

## How it sits against earlier items

- **Sept 10.** The Lottery wanted an updated JVL cabinet at Intralot's lab — [[wiki/decisions/2026-09-10-the-transactional-equipment-demonstration-goes-to-intralot.md]]. On Oct 13 it repeated that the prototype there is "**the old tabletop**". The ten machines go further: a test bench, not one display unit (**evolution**).
- **Sept 9.** JVL had already ruled that negative cases come first in its own testing — [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]]. Val's edge-case argument here is the same idea, now asked of Intralot (**inference**, link only).
- **The parallel letter.** Val still writes to the Lottery for a site controller of JVL's own — [[wiki/decisions/2026-10-13-val-asks-the-lottery-in-one-letter-for-a-site-controller-or-testing-at-intralot.md]].

## Open commitments

- [ ] [[wiki/people/val-levitan.md|Val Levitan]] / JVL — send ten machines (mixed vertical and horizontal, not all new, different software) to Intralot's lab — due unspecified — [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]
- [ ] Intralot engineers — scan the whole field for JVL machines that lock or are disabled — due unspecified — [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]
- [ ] [[wiki/people/bill-avgeris.md|Bill]] (Intralot) — investigate the lock case and get back to JVL "**by Friday**" — due Fri Oct 16 2026 — [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]

## Open questions

- Who staffs the play? Bill: "**you must have people on top playing daily on all the machines**"; Val said he would bring engineers and testers. How many and for how long is not stated — [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]
- When do the machines ship? No date was set — [[raw/Meeting_Notes_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]

**§15.8:** clear.

## Sources

- [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]
- [[raw/Meeting_Notes_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]
