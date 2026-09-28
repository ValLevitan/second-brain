---
type: decision
title: A capability is one short, high-level line ("Replace battery without factory reset"), and the product owner states what he wants but does not tell the engineers how to build it
date: 2026-09-28
aliases: [replace battery without factory reset, you do not want to engineer the product, capability is a high level, capability requirement move on, the capability closes the requirement lives, product owner does not engineer, don't build an essay around this]
source-count: 3
status: active
open-commitments: 0
open-questions: 0
---

# A capability is one high-level line, and the product owner does not engineer

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-28-ris-battery-replacement-capability-framing.md|Sept-28 10:33 AM RIS review]], when [[wiki/people/felipe-miranda.md|Felipe]] began reading his first use case in full detail. [[wiki/people/pavel.md|Pavel Frolov]] agreed. Val repeated and extended it at the [[wiki/meetings/2026-09-28-ris-mvp1-capabilities-walkthrough-and-jira-handover.md|11:07 AM second try]].

## What Felipe first read out

"use case number one, battery replacement without critical error": a Flex machine detects a low battery, "automatically saves meters, game settings, RIS, and state to save memory, and shows battery low, safe to replace, keeps playing. Days later, the battery is so low that the machine crashes and powers off, and it will pop up with battery dead, replace battery. But all recovery data is already saved." [[raw/Meeting_Transcript_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]]

## The ruling (10:33 AM)

- **The capability line.** Val: "I would suggest simplifying it." It "Should say something like… Replace battery without factory reset." Pavel: "Yeah, I agree." [[raw/Meeting_Transcript_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]]
- **Capability and requirement.** "capability is a high level. Requirements attached to this capability explains how this capability is executed." [[raw/Meeting_Transcript_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]]
- **Do not engineer.** "you do not want to engineer the product. What you're doing now is… you're telling the engineers how to do it. You're telling them the battery saved data retention, clock recovery… The warnings… you're now engineering a product. You're not an engineer." [[raw/Meeting_Transcript_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]]
- **Negotiate instead.** "You then enter into negotiation with engineers… and you can ask a question. So… will you retain meters? Will the clock stay?… But you will let the engineers write it out." And: "as a product owner, you should refrain… from telling engineers how to do it." [[raw/Meeting_Transcript_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]]
- **Stop and rework.** Felipe asked for "10 minutes"; Val: "let's take half an hour… Instead of wasting time, I'm going to save the recording… I'm going to put the recording into the meeting notes… I assume you will go through Claude." He would shorten the meeting "to 15 minutes and I will book another meeting". [[raw/Meeting_Transcript_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]]

## Sept 28, 11:07 AM — the roles, stated again

- **Product owner.** "somebody who understands the market and can clearly state in the form of a capability what does he want the product to be capable of doing. The capability is supported by a set of requirements which explains how the capability works." [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]
- **A capability closes; a requirement lives.** "When developed by the engineers, it closes, it collapses… taken off of the board." "The requirement is something that lives. It continues with the product." Acceptance criteria "are written simplistically" and allow "the QA department to test the product." [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]
- **Who drives.** Pavel "will drive the meeting from an engineering perspective. He will demand that the capabilities be clear, simplistic, and very high level." Felipe asks questions until "you find your alignment between product ownership and the engineering group." [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]
- **Keep it short.** "Capability, requirement, move on." "Don't build an essay around this." "English is second language for them." [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]
- **It worked.** Felipe then read "The EGM shall allow CPU battery to be replaced without causing a critical error, a factory reset, or a hard reset." Pavel: "Okay, this particular case is clear. Let's switch to next one." [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]

## Related

- The chain use case → capability → requirement → acceptance criteria → Pavel's features was set on Sept 25: [[wiki/decisions/2026-09-25-felipe-acts-as-product-owner-for-the-ris-rework.md]].
- Earlier capability-writing rules: [[wiki/decisions/2026-09-15-capability-requires-requirement-and-dates-sit-on-the-lowest-level.md]], [[wiki/decisions/2026-09-11-acceptance-criteria-live-in-the-regulations-not-the-capabilities.md]].
- The nine capabilities themselves: [[wiki/topics/ris-remote-install-and-machine-states.md]] (Sept 28).

The derived notes record this as a decision by Val with Pavel agreeing, which matches the transcript [[raw/Meeting_Notes_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]].

**§15.8:** clear. Method only; Val's sharper remarks on Felipe's presenting at 11:07 AM are not recorded.

## Sources

- [[raw/Meeting_Transcript_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]]
- [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]
- [[raw/Meeting_Notes_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]]
