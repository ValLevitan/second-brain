---
type: decision
title: RIS improvement MVP1 is the top Jira capabilities (CAP-252, 255, 246, 250, 254) grouped into one release, due October 19 (date moved Oct 14 to about November 8–9, MVP 2 tasks folded in — inference, see update) — no non-functional requirements, no LTE modem, and the lottery lock left out
date: 2026-10-05
aliases: [RIS improvement MVP1, RIS improvement release MVP1, MVP1 RIS release, three capabilities in two weeks, CAP-252, CAP-255, CAP-246, CAP-250, CAP-254, release date set for 19th, no LTE modem, add four days]
source-count: 5
status: active
open-commitments: 3
open-questions: 2
---

# RIS improvement MVP1: five Jira capabilities, one release, October 19

> **Status note (Oct 14 2026):** the October-19 date no longer holds if the Oct-14 reading is right — Pavel extended "MVP 1" to about November 8 or 9 and put the MVP 2-marked tasks into it, in Kharetski's turn about the old-version branch. Which MVP 1 he meant is an **inference**; see [[wiki/decisions/2026-10-14-mvp1-is-extended-to-about-november-8-or-9-and-the-mvp2-marked-tasks-are-done-inside-it.md]] and the Oct-14 update below. The rest of this decision (the capability list, no LTE modem, the lottery lock left out) is not changed.

Ruled by [[wiki/people/val-levitan.md|Val Levitan]], with [[wiki/people/pavel.md|Pavel Frolov]] agreeing, at the [[wiki/meetings/2026-10-05-ris-mvp1-scope-and-peach-packaging.md|Oct-5 11:00 AM "RIS changes review"]]. Quotations from [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]] unless marked.

## The brief (Val)

"three capabilities that an operator will say. Not everything that I wanted, but... Great." "A reasonable time to me is 2 weeks. I don't want to go a month." "if you tell me I cannot do 3 capabilities within two weeks, I will ask you to reduce it to two capabilities. But deliver it in two weeks."

## The list

- **Where it lives.** Pavel: the capabilities were "Created by Sebastian, I reviewed them, changed the description. And market them with component RIS improvements. All of these capabilities right now lives under IP 90… and IP 747 Rage Gaming Platform."
- **Ranked.** Val asked Pavel to put the most wanted on top and move "those that you know for sure will take longer than two weeks on the bottom". Val proposed 252 first: "Replace a client without Passport" (read as "a part" — **inference**; the Sept-28 capability 6 was "Replace a part without a passport QR").
- **Felipe's view on 252.** A part can already be replaced without the Passport code; "The only reason why you would need to scan Passport QR is if you do a hard reset after that." He suggested "add or remove printer without hard reset" matters more.
- **Who is free.** Pavel: "we can involve, for example, Evgenyk Kharetski right now, but we cannot take Dima and Serge right now" ([[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]]; Dima and Serge not resolved).
- **The cut.** Val: "252? Can you do 255 as well?" — "Uh, yes." "Can you do 246 as well?" — "Looks like it's already implemented, but yes, at least check". "250 Can you do 254?" — "I think yes, and that's all." Pavel on 250: "to enable or disable printer during initial setup, it will be not so difficult, I assume, but This relates to regular setup."
- **Grouped.** Val: "group this into… RIS improvement Mvp 1 release." Pavel created the release in Jira (in Russian, on screen). Val then showed Felipe and Sebastian an AI summary of what the release will do, built from the capability descriptions.

*(The meaning of CAP-255 and CAP-254 is not stated in the sources. Which CAP number is the critical-error capability is not stated either.)*

## No non-functional requirements

Val: "Do we have non-functioning requirements?" Pavel: "No, no… For this particular 4 capabilities, I think we don't need. Non-functional requirement. Oh, probably, probably for the last one, but before to create something, we need to make some. Investigation first." Val then put up non-functional requirements Claude had suggested. Pavel: "Probably first point can be used, but seems that this is already written in form on functional requirement… All the rest looks like… not applicable." Val: "Okay, if it's not applicable, then let's go back to Felipe's questions."

## The date

Val: "Mvp 1 release will be October 16th." Pavel: "Val, release date set for 19th." Val: "Okay, 19th, sorry."

## Tests

Val asked: "Do we have acceptance criteria?" Pavel: "currently we don't have any test cases or test execution created." Asked whether all the capabilities have acceptance criteria, [[wiki/people/sebastian.md|Sebastian]]: "Yes, we do." Val: "Who's going to be writing tests? How is it going to be tested?" Pavel asked to give [[wiki/people/irina-shishko.md|Irina]] time to prepare an answer. Irina's reply is garbled. Val: "Add four, add four days to it."

## Left out

- **The lottery lock.** Felipe raised machines that stay "out of service and locked until someone manually does it" after the lottery accounting system locks them. Val: "that's exactly what I want to discuss. It cannot be Mvp one right now." Felipe: "I have a thread of emails about that. I will share that with you, Val."
- **The LTE modem.** Pavel: "Lte Modem." Val: "No, no Lte, Modem, no." Irina: "Паша, если мы туда Добавим л т модем, мы значит, переключаемся на новую диссиверсию, и там очень много всего получится" (if we add the LTE modem we switch to a new version, and a lot comes with it).
- **Already in Peach 1.** Val asked whether the timer and Linux are already in Peach 1 — Pavel: "Yes" — and "the skill stop also included, right? The… redesign" — Irina: "Yes, yes, yes".

## Next

Val: "can we come back in a week to plan Mvp too?" Pavel: "Very likely, yes", but "For some capabilities for Mvp 2, probably before estimating, need to discuss this with server side, with Dima search" (read as "Dima, Serge", as earlier in the call — **inference**) "I hope they will be not so busy one week later." Val: "Felipe, set up a meeting a week from now. Same time… planning for Mvp 2. RIS improvement. And send E-vite." Felipe: "Okay, will do."

## How it sits against Sept 25–28

On Sept 25 Val asked for one to three fixes that remove most factory-reset pain ([[wiki/decisions/2026-09-25-the-ris-rework-mvp1-is-for-flex-machines-only.md]]). On Sept 28 Felipe read nine capabilities and they went to Sebastian for Jira ([[wiki/decisions/2026-09-28-sebastian-takes-the-ris-mvp1-capabilities-into-jira-and-felipe-steps-back.md]]). Oct 5 cuts the Jira list to what fits two weeks. This is **evolution**. Flex-only scope was not mentioned on Oct 5 and is not changed. The critical-error capability, moved to MVP 2 on Sept 28, is back in MVP1 — see [[wiki/decisions/2026-10-05-the-critical-error-screen-shows-the-cause-and-fix-in-words-and-keeps-the-qr-code-in-mvp1.md]].

The derived notes match the transcript here, except that they list five capabilities where Pavel spoke of "4" [[raw/Meeting_Notes_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]].

## Oct 6 2026 — the work goes to Kharetski, for Georgia only

At the [[wiki/meetings/2026-10-06-daily-standup-ris-georgia-branch-and-critical-error-text.md|Oct-6 Minsk stand-up]] (Russian) Pavel gave Kharetski "252 255 246. 254" first, with "258" as the build, in "2 недели даже наверное чуть меньше" [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]. CAP-250 was not named. The branch is Georgia only, on the 1.14 line, with nothing else added — see [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]]. This is the first step of carrying out this release (**evolution**, no conflict).

## Open commitments

- [ ] Pavel Frolov — check whether CAP-246 is already implemented — due unspecified — [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]
- [ ] Pavel Frolov — talk to the server side (Dima, Serge) about MVP 2 capabilities before estimating — due before the MVP 2 meeting (about Oct 12) — [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]
- [ ] Felipe Miranda — share his email thread on lottery-locked machines with Val — due unspecified — [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]

## Open questions

- Who writes the MVP1 test cases and test executions, and how? Asked by Val; the answer is garbled — [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]
- Is the release four capabilities or five (is CAP-246 already done)? — [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]

**§15.8:** clear.

## Update, Oct 12 2026 — the MVP 2 meeting is held; whether MVP 1 goes to the lab at all now waits for Val

The MVP 2 planning call took place on [[wiki/meetings/2026-10-12-ris-mvp2-scope-and-release-timing.md|Oct 12 at 11:29 AM]] (Felipe, Pavel, Irina, Sebastian; Val absent) [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]:

- Pavel and Irina asked whether MVP 1 is worth sending to the lab, since changes go into three builds (Peach 1, 2, 3). Felipe: MVP 1 does not touch the biggest pain points, and another customer upgrade "maybe a month later" would be "complicated"; "I don't know what Val wants". Pavel: "I will save this for now." Felipe closed: "We still need Val input on. Do we want to send Mvp 1 to the lab and not wait for Mvp 2 or add the changes possible to Mvp 1".
- Pavel on timing: "we are going to release Mvp one. In 2 weeks, probably, with testing. If we add in one more week, probably we can release Mvp 2." MVP 2 work to about November 1 (Irina), then about five days at Eclipse — a release around November 9–10 (Felipe).
- So the Oct-19 MVP 1 release is **in question**, not cancelled: no one ruled. This is **evolution** (a newer plan under discussion), not a contradiction. Detail: [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 12).

## History

- [x] Felipe Miranda — set up the RIS improvement MVP 2 planning meeting a week out, same time, everyone invited — due about Oct 12 2026 — [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]] — discharged: the "RIS MSVP2 Meeting" took place on Oct 12 at 11:29 AM (who sent the invitation is not stated; Val did not attend) [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]

## Update, Oct 14 2026 — MVP 1 to about November 8–9, with the MVP 2 tasks inside (read as this release — inference)

At the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 Minsk stand-up]] (Russian) [[wiki/people/evgeny-kharetski.md|Kharetski]] reported the passport work done and the battery test (task 246) under way, then: "я как понимаю у нас VP он превратился в MB 2". [[wiki/people/pavel.md|Pavel]]: "надо будет MVP один расширить дату до… 8 наверное да или до 9 ноября. И это то, что там помечены задачи MVP 2 их сделать MVVP один на самом деле." Irina agreed. Kharetski checked that the team still delivers "старую версию"; Pavel and Irina: yes — the one first cut, with more time [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

- **Evolution.** On Oct 12 the Oct-19 release was in question. On Oct 14 Pavel moves the date to about November 8 or 9 and folds in the MVP 2 tasks — close to Felipe's Oct-12 "release would be like November 9th, 10th". This is **evolution**, if the reading holds — [[wiki/decisions/2026-10-14-mvp1-is-extended-to-about-november-8-or-9-and-the-mvp2-marked-tasks-are-done-inside-it.md]].
- **Val.** Whether Val agreed is not in this source.
- **CAP-246.** Kharetski is testing the battery under task 246, with a sub-task for the test. Whether 246 was "already implemented" (Oct-5 question below) is not said.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]
- [[raw/Meeting_Notes_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]
- [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
