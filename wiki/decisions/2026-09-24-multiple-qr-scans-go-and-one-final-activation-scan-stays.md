---
type: decision
title: The chain of up to six QR scans goes (use case 9), and one final activation scan stays for machines without a modem (use case 10)
date: 2026-09-24
aliases: [use case 9, use case 10, no more multiple QR code scans, six screens of lease scan, final QR code activation scan, scan and enter activation number, activation code, we're nixing it]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# Multiple QR scans go; one final activation scan stays

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-24-ris-serial-binding-and-factory-reset-focus.md|Sept 24 2026 7:02 AM RIS follow-up]], and confirmed by [[wiki/people/felipe-miranda.md|Felipe]] and [[wiki/people/sebastian.md|Sebastian]]. Both are new use cases, added to Val's list of eight. All quotations from [[raw/Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026.md]].

## The complaint (Felipe)

The final scan itself is not the problem: "I don't see a problem with that. What people are complaining about is that in the past with previous softwares, they would scan the lease once and go. Now we have up to six, I've seen six screens of lease scan." The same happens "with the one we're doing for mega hits where we take all the information."

## Why it grew (Val)

"this was done because we expanded the amount of information we were transferring out of the machine where QR code was the only means of transferring the information."

## Use case 9 — remove the chain

"No more multiple QR code scans… scan code one, code 2, code 3, code 5, code 6, and only after code 6 we send the activation." And: "So we're nixing it. We're no longer going to have it. We'll redesign it". He tied it to the modem: "we should… not have it available, especially now that we have the modem." Felipe: "Yes."

## Use case 10 — keep one final scan

"we will keep in place… The final QR code activation scan, which… Sends to JVL the… Finally applied settings… and will transmit the serial number of the machine that the setting was applied to, and will send back to the machine the activation code that an operator will have to enter on the screen." Felipe and Sebastian: "Yes." Val's reason for keeping it: "I still believe that enforcing QR code scan post installation is important."

**Only where there is no modem.** Pavel: "This is only for machines. We are no modem. If we have modem, it will be sent automatically." Val: "Yes, yes, yes, of course."

## Update — Sept 28 2026: capability 9, "Lease renew with one QR scan"

At the [[wiki/meetings/2026-09-28-ris-mvp1-capabilities-walkthrough-and-jira-handover.md|Sept-28 11:07 AM RIS review]], Felipe read it as the ninth RIS MVP1 capability: "Lease renew with one QR scan. That was one that was added. Remember how we have four, 5, 6 QR codes? We want to do it with just one QR code and be done with it." Pavel: "It's clear. It's okay." Irina: "Okay, it's simple." It goes into Jira with the other capabilities — [[wiki/decisions/2026-09-28-sebastian-takes-the-ris-mvp1-capabilities-into-jira-and-felipe-steps-back.md]]. [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]

## Related

The **statistics-scan** parameter on a factory reset (on today; Georgia might default it off) was raised by Irina at the earlier 5:41 AM engineers' review; Pavel was to ask about it — see [[wiki/decisions/2026-09-24-engineering-plans-to-switch-off-the-passport-check-for-georgia-builds.md]]. Whether that scan is one of the six Felipe described is **not stated**.

**§15.8:** clear.

## Sources

- [[raw/Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026.md]]
- [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]
