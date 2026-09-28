---
type: decision
title: Felipe acts as product owner for the RIS rework — he grooms the meeting into use cases, capabilities and requirements for review on Monday Sept 28, 10 AM
date: 2026-09-25
aliases: [you're acting as a product owner, groom everything that we said in the meeting, product owner vs product manager, handing it over to Sebastian, Monday 10 o'clock RIS review]
source-count: 4
status: active
open-commitments: 2
open-questions: 0
---

# Felipe acts as product owner for the RIS rework

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the close of the [[wiki/meetings/2026-09-25-ris-mvp1-factory-reset-reduction-plan.md|Sept-25 10:31 AM RIS follow-up]]. All quotations from [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]].

## Why

After [[wiki/people/pavel.md|Pavel]] read out his numbered list, Val said: "I need to organize these thoughts that Pavel outline by numbers… Because right now, kind of, I cannot comprehend what needs to be done… It's like, I almost need another meeting to groom the final ideas."

## What was decided

- **The task.** Val to [[wiki/people/felipe-miranda.md|Felipe]]: "groom everything that we said in the meeting. Into. Tiny, small. written in the ESL type of English… Compressed. Summary. of the changes that need to be done and then from there we need to create. New use cases. Positive use cases. and break those down into new capabilities." Felipe: "Okay. Yes, I will do that. Absolutely."
- **The role.** Val first said "You're acting as a product manager now", then corrected himself: "no, you're acting as a product owner." His definition: "Product owner is an individual who participates in the beginning of the spec in the design and gets it out of the engineering hands into the field and hands it over to a product manager who then manages the product in the field." Felipe hands over to [[wiki/people/sebastian.md|Sebastian]], "And Sebastian will then manage the product in the field."
- **Whose role it normally is.** "which would be one's responsibility normally. We obviously regret that Juan is not here." *(Probably [[wiki/people/juan-martinez.md|Juan Martinez]] — inference.)*
- **The chain.** "You need to start with use cases. Use cases first lead you into capabilities. Then you explain how the capability works through a set of requirements… each requirement will have a set of acceptance criteria. You will hand over the package to Pavel." Pavel "will hand assign resources to it and negotiate, internally negotiate a set of features for each of the capability. A feature becomes a… Feature branch in Github". This is the same chain Val set on Sept 7 — see [[wiki/decisions/2026-09-07-andrei-bosik-drives-the-wi-fi-work-and-the-process-chain.md]] (Sept-25 update).
- **The review.** "So I'm expecting a meeting invitation for Monday the 28th for 10 A.m. Eastern Time… our objective for the meeting will be to review those in the meeting."

*(Inference: this is an interim fix for the gap Val named on Sept 22 — "we don't have product manager" — while a Minsk transfer to the US is arranged; see [[wiki/people/val-levitan.md]] (Sept 22, 2:45 PM). The Sept-25 source does not link the two.)*

The derived notes list the product-owner role and the Monday review as decisions by Val, which matches the transcript [[raw/Meeting_Notes_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]].

## Update — Sept 28 2026: the review is held, twice, and the work passes to Sebastian

- **10:33 AM, first try.** The review met as "RIS Rework MVP1 – Use Cases, Capabilities & Requirements Review" (the recording starts at 10:33 AM, not 10:00). Felipe began reading use case 1 in full detail; Val stopped him: "Replace battery without factory reset" is the capability, and "you're now engineering a product. You're not an engineer." He gave Felipe half an hour to rework it. See [[wiki/decisions/2026-09-28-a-capability-is-one-high-level-line-and-the-product-owner-does-not-tell-engineers-how.md]] and [[wiki/meetings/2026-09-28-ris-battery-replacement-capability-framing.md]]. [[raw/Meeting_Transcript_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]]
- **11:07 AM, second try.** Val restated the product-owner role — "somebody who understands the market and can clearly state in the form of a capability what does he want the product to be capable of doing" — and said "you're playing the role now. It's not your primary role." Felipe read out nine capabilities; Pavel answered for engineering. See [[wiki/topics/ris-remote-install-and-machine-states.md]] (Sept 28) and [[wiki/meetings/2026-09-28-ris-mvp1-capabilities-walkthrough-and-jira-handover.md]]. [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]
- **The hand-over.** Val then gave the Jira work to Sebastian — "You're taking over from now. I want to free up Felipe for other things." See [[wiki/decisions/2026-09-28-sebastian-takes-the-ris-mvp1-capabilities-into-jira-and-felipe-steps-back.md]]. [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]

## Open commitments

- [ ] Val Levitan — post the meeting transcript for the team ("I'm going to post the transcript here") — due Sept 25 2026 — [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]
- [ ] Felipe Miranda — confirm that clearing the meters always needs decommissioning ("I need to confirm, but I am pretty sure") — due unspecified — [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]

## History

- [x] Felipe Miranda — groom the meeting into a short summary of changes in ESL English, then positive use cases, capabilities, and requirements with acceptance criteria — due Mon Sept 28 2026, 10:00 AM — [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]] — **discharged Sept 28:** he presented the use cases at 10:33 AM and, after a half-hour rework, nine capabilities at 11:07 AM [[raw/Meeting_Transcript_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]] [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]
- [x] Felipe Miranda — send the meeting invitation for Mon Sept 28, 10:00 AM Eastern ("Book the meeting with us") — due before Sept 28 2026 — [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]] — **discharged Sept 28:** the review was held (recording from 10:33 AM); who sent the invitation is not stated [[raw/Meeting_Transcript_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]]
- Pavel Frolov — once Felipe's package is in, assign resources and negotiate the features for each capability — **carried forward Sept 28** in Val's words "Pavel will create features and schedule resources and work"; now held on [[wiki/decisions/2026-09-28-sebastian-takes-the-ris-mvp1-capabilities-into-jira-and-felipe-steps-back.md]] [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]

**§15.8:** clear. Role assignment only; no judgement of anyone's performance.

## Sources

- [[raw/Meeting_Notes_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]
- [[raw/Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026.md]]
- [[raw/Meeting_Transcript_RIS_Battery_Replacement_Capability_Framing-September-28-2026.md]]
- [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]
