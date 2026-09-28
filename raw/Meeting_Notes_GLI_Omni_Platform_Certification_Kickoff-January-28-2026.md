# Meeting Summary — GLI: Omni platform certification kickoff

**Date:** January 28, 2026, 1:01 PM Eastern
**Duration:** approximately 28 minutes
**Attendees:** Val Levitan, Pavel Frolov, Juan Martinez, Efim Podvoiski (JVL); Deborah Oxnem and Dan Lewis (GLI — Gaming Laboratories International). Genadi Peari was invited (asked a question of him on mute); Patrick Cottingham double-booked.
**Raw transcript:** [[Meeting_Transcript_GLI_Omni_Platform_Certification_Kickoff-January-28-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "JVL - GLI", 1:00–2:00 PM ET, organiser Deborah Oxnem (gaminglabs.com), attendees Dan Lewis, Juan, Pavel, Genadi, Irina Shishko, Ivan Shpak. Deborah and Dan named; confirmed on both keys.

## Summary

The certification kickoff for the Omni platform — deliberately early: "I want to make sure that everybody understands the scope, the requirement, the objective… we have plenty of time right now."

**Val's platform history for GLI.** Until now GLI approved JVL products on the AMD V1000 processor with the Rage framework — Rage Studio being both the framework and the code name for a development ecosystem dating back ~15 years, when an entire infrastructure maintained the engine. The aging ecosystem plus JVL's online-market work pushed a new HTML-based framework capable of online and land-based. Now rolling out: the all-encompassing new framework — Unity-based graphic development, the linking application into the engine, Pixi riding inside, an internal database (within "Omnia") — on the new **FP7** hardware platform, housed in the existing approved cabinet (code name **Dash Super**). A sample game exists purely as GLI's test tie-in: **Calle Ocho** (not for market, doesn't need to function).

**Schedule of record (stated as estimates).** Lab submission ~**mid-May** (Pavel; contingent on setup implementation currently competing with other priorities), then **September 1: three games** and follow-on submission. "Is it possible that I made errors? Most likely, but that's where we sit."

**Technical scope discussed.** RNG: the mask+RNG used for online will be packaged into a container for land-based — "very close" to the previous platform's approach (Pavel). Hardware change is essentially the logic board; minor I/O changes tied to new printers as an optional device (per Gennady's updated hardification documents). Because the cabinet is already approved, electrical/discharge testing is not re-triggered by a logic-only change (a few hours at most); Juan confirmed no pre-screening needed — GLI does its own. Dan's testing approach: image-comparison tools that evaluate screens against reference images; deviations flag review.

**The white-paper method (the meeting's process decision).** Val pushed to minimise verbal discussion: JVL initiates white papers, GLI assesses and reflects back. Undertakings assigned in-meeting:
1. **Peripherals list** — all possible peripherals, marked "previously approved" vs new, so everything is tested at once ("always cheaper to test at one time") — Juan.
2. **Math/RNG architecture white paper** — how math and RNG are architected in the new framework, how the RNG is called — Efim.
3. **Ecosystem-integration white paper** — how GLI embeds its file and gets an output, enabling GLI to generate results from JVL's ecosystem rather than hand-building (Dan's ask; Efim's read-back: "I push these numbers and want to see this set of numbers"; a few hours per task once built).
4. **Setup-screens testing white paper** — practically every setup screen is changing; JVL to propose an automated way to submit/verify them.

**Commercials.** Deborah offered a proposal; Val deferred it until GLI has digested the white papers — "only then provide us with the proposal." Communication channel: through Val and Juan only ("my preference is not to pollute mailboxes").

## Decisions Made

- **Certification proceeds via JVL-initiated white papers, not verbal cycles.** (Val, accepted by Dan Lewis)
- **Schedule of record: mid-May lab submission; three games September 1.** (Pavel/Val, as estimates)
- **All peripherals tested in one pass; previously-approved items flagged to avoid re-testing.** (agreed)
- **GLI proposal deferred until white papers are understood.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Juan Martinez | Peripherals list with previously-approved annotations | TBD | High | One-pass testing |
| 2 | Efim Podvoiski | White paper: math + RNG architecture in the new framework | TBD | High | Named on the call |
| 3 | JVL (Efim) | White paper: GLI ecosystem integration (input→output verification) | TBD | High | Dan's automation goal |
| 4 | JVL | White paper: automated setup-screens testing | TBD | Normal | Every screen is changing |
| 5 | GLI (Deborah) | Proposal/scope — after white papers | Later | Normal | Explicitly deferred |

## Possible mis-transcriptions (not in glossary — confirm before fixing)

- "a jdl was called ridge" (00:01:30) — **at JVL was called Rage**; "Black Engine" (00:02:18) — garbled engine name; "Omnia" (00:04:11) — **Omni**; "Pixy" — **Pixi**; "framing server" (00:06:52) — garbled; "hardification" (00:12:27) — hardware-specification, garbled; "list of these employees" (00:15:29) — **list of these peripherals**; "Yefim/Eupheme" — **Efim**; "IQA testing" (00:19:25) — unclear; "it's not good" (00:22:48, Dan) — context says "it's not needed".

## Dispatch Log

---
*Processed from Plaud recording on September 24, 2026 (backlog batch 3)*
*Source recording: 01-28 Technical Alignment Meeting: JVL's New Gaming Platform Certification (Plaud)*
