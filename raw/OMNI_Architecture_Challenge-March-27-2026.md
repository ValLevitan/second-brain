# Meeting Summary — OMNI Architecture Challenge

**Date:** March 27, 2026, 1:58 PM Eastern
**Duration:** ~8 minutes
**Attendees:** Val Levitan, Pavel Frolov

## Summary

Val opened the call with three items to cover, stating he would move quickly through his conclusions.

**1. Tech Stack Direction — TypeScript/JavaScript + Rust**

Val proposed a radical change to the OMNI tech stack: adopt TypeScript/JavaScript and Rust. Rust would replace C++ and C currently used for the Hardware Abstraction Layer (HAL) and math-intensive components. Val emphasized that this conclusion came from extensive reading and internal debates that occurred outside of meetings with Pavel, so the decision appears fast but is backed by considerable prior analysis. Pavel acknowledged that TypeScript/JavaScript makes sense, but noted that replacing the hardware abstraction layer with Rust would be "a big piece of work." Val agreed and said he would "park" this topic for now but would continue the conversation with Pavel going forward.

**2. Sprint Planning and Maple Conversion**

Val reminded Pavel about the two-week planning sketch he was supposed to produce. Pavel reported he had partially completed it — tasks related to Linux 5.15 are already in Jira. However, Pavel had not made progress on the Maple rework question. He noted that Ira had worked on it that morning — they discussed it together but did not create Jira tasks yet.

Val praised Ira's work highly, calling it "class." He considered using Claude (AI) to automatically push Ira's analysis into Jira but expressed concern about introducing errors he couldn't catch. Pavel advised against that approach. Val then said he doesn't want Pavel doing this Jira entry work either — he wants Ira herself to complete it, use Claude to create the Jira items, and distribute the results to all participants for review. Val acknowledged Ira might be hesitant to use Claude given her working style, but said he would push her to adopt it.

**3. Andrei Klimovich — New Role Announcement**

Val announced that Andrei Klimovich, currently in sales/marketing for the music product, is being reassigned. His new title will be Product Manager and Marketing for Transactional Payments. He will be added to "Espace Blanc" (white-label) and will have dual reporting to Ilana and Val, with direct interaction with Pavel. Val spoke very highly of Klimovich — describing him as an engineer by education, extremely honest, organized, and smart. He said Klimovich has proven himself from all angles and will raise the team's level. He will begin his new duties very soon and Pavel should expect contact from him.

**4. Pavel's Vacation Request**

Pavel asked to plan a short vacation — approximately 6 working days at the end of April or beginning of May. Val recommended beginning of May as the better timing. Val cautioned that a POS release is approaching around that period — while the tools may not be fully ready, the release build, integration, and fitting work will be happening at that time. Additionally, recycling will be entering marketing beta. Val urged Pavel to plan his time off carefully around these milestones.

## Decisions Made

- **Tech stack direction: TypeScript/JavaScript + Rust** — Val has concluded (based on prior analysis) that the OMNI platform should move to TS/JS and Rust. Confirmed as an ADR candidate. Parked for further detailed discussion with Pavel. (Decided by Val)
- **Ira to create Jira tasks for Maple rework** — Val directed that Ira (not Pavel, not automated Claude) should use Claude to create the Jira Features from her analysis and distribute to participants. No Capabilities needed — go directly to Features. (Decided by Val)
- **Andrei Klimovich reassigned to Product Manager & Marketing for Transactional Payments** — Dual reporting to Ilana and Val, direct interaction with Pavel. (Decided by Val)
- **Pavel's vacation: beginning of May preferred** — Val suggested early May over late April, citing POS release and recycling marketing beta. (Decided by Val)
- **JIRA Plans restructured** — New Initiative IP-1045 "Transactional" created under IP-106 "Hardware". Products IP-955, IP-1014, IP-579, IP-578 moved from IP-760 (Compact) to IP-1045 (Transactional). (Post-meeting action by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Ira | Complete Maple rework analysis, create Jira Features using Claude, and distribute to all participants for review | TBD | High | Blocks sprint planning for Maple conversion; Val specifically wants Ira to own this, not Pavel |
| 2 | Pavel | Continue populating Jira with remaining sprint planning tasks (beyond the Linux 5.15 items already entered) | TBD | Normal | Two-week planning sketch was partially done; remaining items still needed |
| 3 | Pavel | Plan vacation dates carefully around beginning of May, accounting for POS release and recycling marketing beta | TBD | Normal | POS release integration and recycling beta coincide with late April / early May |

## Engineering Signals

### Confirmed Signals

- **ADR: Tech stack shift to TypeScript/JavaScript + Rust** — Val explicitly proposed replacing C/C++ with Rust for HAL and math, and adopting TS/JS. Confirmed by Val as an ADR to be formally recorded.

### Suspected Signals

No additional suspected signals.

## Open Questions

- What is the full scope of replacing the HAL with Rust? Pavel flagged this as a large effort — no timeline or feasibility study discussed yet.
- What are the specific dates for the POS release and recycling marketing beta in late April / early May?
- When does Andrei Klimovich officially start in his new role?

---
*Processed from Teams transcript on March 27, 2026*
*Source meeting: Call with Pavel Frolov — OMNI Architecture Challenge*
