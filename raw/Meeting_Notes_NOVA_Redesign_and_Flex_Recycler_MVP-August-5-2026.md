# Meeting Summary — NOVA redesign review + Flex-Recycler MVP for GA-COAM (Aug 15)
**Date:** August 5, 2026, 8:00 AM Eastern
**Duration:** ~43 minutes
**Attendees:** Val Levitan, Pavel Frolov, Alexander Biratko, Irina Shishko
**Language:** Russian (raw transcript verbatim; summary in English)
**Raw transcript:** [[Meeting_Transcript_NOVA_Redesign_and_Flex_Recycler_MVP-August-5-2026]]

## Summary

Two topics. Val opened by saying he wanted to keep both short.

**1. Georgia expo prep (GA-COAM show, Aug 15) — Flex-Recycler MVP demo.**
Val wants a simple graphical "fake" demo cycle for the booth: accept money → issue a QR code → walk the floor and play the machines using Flex Port → return to the recycler → and on screen show a faked graphical cycle (QR-code validation, fake card issuance, prepaid Mastercard, transfer from Mastercard to a price-point card, then recycle the price-point card back to cash). He stressed this is only a graphical mock-up — it does not have to validate against any real system.

Alexander said what's missing is the fake card-issuance screen. They already have a screen that shows money coming out; they'll repurpose it into one simple screen that shows the stages with arrows (deposit → transfer → dispense). For the show, the payout is capped: max win around $40, enforced by limiting a single recycler withdrawal to $40 — agreed as the simplest option. Real cash (not fake money) will be used in the recycler; tickets/vouchers the recycler takes go straight to its cashbox.

On the device side, the recycler had many flashing/configuration problems. Pavel wants Alexander to train someone to reflash and configure it; Val proposed Andrei (an engineer, easier to work with) instead of Elizabeth. Andrei also needs Gennady's account for the firmware-flashing software (the MII flashing tool). The team must meet with Andrei **today** so Andrei can write the minimum capabilities needed for the show, which then go into the Jira timeline as a feature with epics/stories.

Val restated his rough backlog-ratio guideline (as a guideline only, not a rule): capability→story ≈ 1:15, capability→feature ≈ 1:10, feature→story ≈ 1:15. He argued developers who don't break a feature down into stories tend to make more mistakes. Pavel noted the recycler capabilities are too many for the MVP and some mix MVP and non-MVP features, so they can't be cleanly closed — this needs restructuring with Andrei. Val mentioned Efim finished the math port (on RAGE).

**2. NOVA re-architecture — platform split into independent services.**
Val raised the redesign now because a successful experiment with Igor Metelsky suggests games can be ported faster than expected; a faster restart helps everyone, especially testing and letting designers view their changes. The direction (discussed since May) is to break the platform into independent services with a defined internal communication layer. Val is preparing a summary document of those decisions and said he already posted a document (in two languages) in the chat for the team to read.

Pavel described his experiment: a service that works with iBoard, generated on RAGE, which worked with iBoard's internal data on the first pass; there was a bridge to LGS that was nearly ready, but the correct design is for LGS to talk to the service directly with no extra layer. Alexander noted LGS is now on new Java, which implements a Unix socket; libraries (printer, iBoard, bill validator, counter board, all-LED board, sound) communicate through it. The bill validator (MII) is partially converted; in the recycler MII was moved to Java and talks to the validator natively with no intermediate service. A lever-scanner service may be needed if connecting directly to the machine.

Sound is the most serious rework. More broadly, every service must support transparent restart: if a service dies, the main LGS must not crash — it should detect the drop and wait for the service to come back. They want a health-check mechanism across all services, with critical alerts if a service doesn't recover within a timeout, and a single status screen showing all services as green dots. The modem should be a service too (scripts to launch the modem stack plus a control/status utility). Alexander and Pavel agreed all services should expose a common base interface / data contract that describes how to talk to the service, which also makes testing easy. Testing should be automatic and based on acceptance criteria.

Process: architecture decisions become ADRs stored in a design repo; each service gets its own repository, and each repo carries a PROSE tying a completed build to the capability it closes (capability and prose written in English) as a standard procedure. Participants: Alexander, Pavel, Irina, a QA engineer, plus frontend help (and Efim) for the health-status screen. Val will book the architecture meetings himself so the transcripts auto-feed his Second Brain; he asked the team to record every architecture discussion and circulate it to him. He noted he finished building his personal Second Brain (in the style of Karpathy) and recommended the team do the same.

Cadence: first architecture meeting on **Aug 10** (~1.5 hours), then 45-minute meetings on Aug 11, 12, 13 and 14, at 12:15 PM Minsk time (right after their daily, before the Americas wake up). By Aug 13–14 they should be assigning resources and have MVP pods giving ~2 weeks of work others can do without Alexander, who is on vacation for two weeks from Aug 17.

## Decisions Made

- **Show demo will be a graphical mock-up only** — the faked money cycle does not validate against any real system. (Val)
- **Recycler single-withdrawal limit set to $40 for the show**, chosen as the simplest way to cap payouts. (Alexander, agreed)
- **Andrei takes over recycler flashing/configuration** instead of Elizabeth, and writes the show's minimum capabilities. (Val)
- **Platform will be split into independent services** talking over the LGS Unix socket, each with a common base interface / data contract, transparent restart, and a health-check status screen. (Val, Pavel, Alexander)
- **Each service gets its own repository; architecture decisions recorded as ADRs in a design repo**, with a PROSE linking each build to the capability it closes. (Val, team)
- **Architecture meeting series: Aug 10 (~1.5h) then Aug 11–14 (45 min each) at 12:15 PM Minsk**, booked by Val so transcripts are captured. (Val, agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel, Alexander (+ Andrei) | Meet with Andrei to explain and have him write the minimum recycler capabilities needed for the show | Aug 5 (today) | High | Gates the show demo build |
| 2 | Alexander / Pavel | Get Gennady to give Andrei his account for the firmware-flashing software (MII flashing tool) | Aug 5 | High | Blocks Andrei from flashing the recycler |
| 3 | Alexander | Repurpose the existing money-dispense screen into one simple faked multi-stage screen (deposit → transfer → dispense, with arrows) for the booth | Before Aug 15 | High | The missing piece for the demo |
| 4 | Alexander | Set the recycler single-withdrawal limit to $40 for the show | Before Aug 15 | Normal | Caps booth payouts |
| 5 | Pavel, Alexander (+ Andrei) | Restructure recycler capabilities to separate MVP from non-MVP features so they can be closed cleanly | Before Aug 15 | Normal | Current capabilities mix MVP and non-MVP |
| 6 | Pavel, Alexander | Put the show capabilities into the Jira timeline as a feature with epics/stories | Before Aug 15 | Normal | Traceability for the MVP |
| 7 | Pavel, Alexander | Design the universal service interface (base API / data contract) for querying a service's info | Aug 10 (Monday) | High | Foundation for the architecture meeting |
| 8 | Val | Finish and circulate the architecture summary document (decisions since May); already posted a bilingual doc in the chat to read | Before Aug 10 | Normal | Input for the meeting series |
| 9 | Val | Book the architecture meeting series himself — Aug 10 (~1.5h), then Aug 11–14 (45 min) at 12:15 PM Minsk | Aug 5 | Normal | So transcripts are captured to the Second Brain |
| 10 | Pavel, Alexander, Irina | Involve a frontend developer and Efim for the health-status "all-green" screen, and a QA engineer for test design | Aug 10 series | Normal | Testing to be automatic, based on acceptance criteria |
| 11 | All | Record every architecture discussion on transcript and circulate to Val | Ongoing | Normal | Feeds Val's Second Brain; makes non-facts easy to extract |

## Open Questions

- Whether to use the current interface board (same as Flex IQ) or Gennady's new board for the show — Pavel to settle with Gennady; the new board may add work and they don't have it yet.
- Whether a separate lever-scanner service is needed if the recycler connects directly to the machine.
- Exact split of MVP vs non-MVP recycler capabilities (to be worked out with Andrei).

## Dispatch Log

---
*Processed from Teams transcript on August 5, 2026 (scheduled meeting-watcher run)*
*Source meeting: NOVA redesign review + Flex-Recycler MVP for GA-COAM (Aug 15)*