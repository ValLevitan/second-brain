---
type: project
title: Georgia market rollout (Peach1234 / DLKG)
date: 2025-02-19
aliases: [Georgia, Georgia co-op, Peach1234, DLKG, Georgia Lottery, GLC, Eclipse, dual SAS, third printer port, Peach 1, Peach 2, Peach 3, Peach 4, JPRE, curved monitor cabinet, flex curve]
source-count: 2
open-questions: 3
---

# Georgia market rollout (Peach1234 / DLKG)

JVL's core land-based market — the conventional **Georgia co-op / COAM** business — and the software releases (**Peach1234** and **DLKG**) needed to keep it and roll out the new payment-kiosk/printer support. Worked through on the Feb 19 2025 outstanding-subjects alignment call with [[wiki/people/val-levitan.md|Val]], [[wiki/people/pavel.md|Pavel]], [[wiki/people/irina-makarych.md|Irina]] and [[wiki/people/juan-martinez.md|Juan]]. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Why it matters (Val's revenue warning)

- Val expects a **~40% drop in JVL's conventional Georgia revenue** because two main competitors entered last year. If the main market's revenue falls and the new markets aren't rolled out, JVL "cannot pay wages" / sustain the company. He distinguished **rollout priority** (getting the product into the *marketplace* in Georgia, South Dakota, and Puerto Rico) from development priority — GLI and the Eclipse lab "don't care about timing," so a release manager must drive market rollout. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Dual SAS + third dedicated printer port

- Georgia previously required **dual SAS** (two independent SAS ports on two DB9 connectors, primary + secondary, with the primary controlled by the Georgia Lottery Corporation / "GLC") — implemented last year. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- Now that pay-kiosks (relying on the TITO model) need an on-board printer, JVL is adding a **third dedicated printer port**: a new DB9 connector (a **harness**, not a "jumper") inside the CPU box, driven by a **hardware-abstraction-layer library** (Pavel corrected Val that "firmware" is wrong — the printer's firmware sits on the printer; JVL's side is a HAL library). Two printer library types: **Gen 2 / Gen 5 (JCM) + nano-optics** share one communication language; **Epic** uses a different one. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- Design intent (Juan/Val): the third COM port is **always the printer**, defaulted so operators don't reassign SAS ports by mistake (SAS 1 must stay primary per Georgia rules; SAS 2 can be reassigned only on a COM 1 malfunction). Pavel to remove/relabel the printer connection in the SAS-port selection UI so the wrong port can't be picked. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Bally iview reporting mismatch (Peach1234)

- On the last test, **Irina** reviewed the **Bally iview** logs and found JVL is correctly matching and sending the right data to Bally, **but Bally's final report is not correct** — JVL doesn't understand how iview produces that report. Val doesn't fully trust the Bally reports (on the Georgia machine he can't select "secure enhance"/"system"). Path forward: build the software, get it to the **Eclipse** lab, and test with the system; Val to call Eclipse. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Peach1234 / DLKG shared build

- Peach1234 and DLKG will use the **same LGS version** to simplify submission to Eclipse, and the same **Progressive Controller** setup approach as the Florida "JPRE" market (an initial-setup screen picks the controller on the network; an **embedded progressive controller** works for a single machine, since Georgia locations usually have one machine). [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- **Felipe** has the current **Diamondlink** software that supports the printer; the printer work is urgent for him. See [[wiki/people/felipe-miranda.md|Felipe Miranda]]. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Release cadence — staged "Peach" packages (Mar 7)

- Georgia will be released in **four staged packages** — **Peach 1, Peach 2, Peach 3, Peach 4** — at roughly **six games at a time**, on ~one-to-two-week intervals, rather than all games at once. Staging is more expensive on **Eclipse** approvals but necessary because [[wiki/people/lena.md|Lena]]'s team is a bottleneck implementing changes across all games. [[wiki/people/felipe-miranda.md|Felipe]] confirmed the tests passed, so releasing can start. [[raw/game_design_meeting_march_7_2025.md]]
- **Sequencing:** Peach 1 and Peach 2 make up ~**80%** of what's installed in the field; Peach 3 has little install base and Peach 4 isn't installed yet. **Diamond Link** is to be "snuck in" right after Peach 2 (to help sell that machine), then Peach 3 and 4 follow. **Ivan** (release) needs ~**10 days** from starting with Eclipse to issuing a purchase order and submitting the FTP link; Val asked to add a 25% time buffer. [[raw/game_design_meeting_march_7_2025.md]]
- **Pay-table-ID risk:** JVL wanted operators to be able to check the **pay table ID**, but **United** said on a call they **can't** do that — so JVL must take a "leap of faith" that the E9 team's pay table IDs work. Val flagged he dislikes it. [[raw/game_design_meeting_march_7_2025.md]]
- **Old framework for Georgia:** **Jackpot Rush** (and **JPRE**) for Georgia stay on the **old framework** with the **curved-monitor cabinet** targeted for the **summer / gaming show (August)**; only new games go on the new "omni" framework, starting with the Fortune Foo Paws pilot. Keeping new product on the old framework means maintaining Rage Studio and the old stations longer, and the **nudge mechanic** needs updating — parked for a later meeting. [[raw/game_design_meeting_march_7_2025.md]]

## Open questions

- Was routing Jackpot Rush / JPRE for Georgia onto the **old framework** (curved cabinet) a deliberate plan or an oversight? Val said he didn't recall discussing it and parked it for a later meeting. [[raw/game_design_meeting_march_7_2025.md]]
- Why does the Bally iview final report disagree with the (correct) data JVL sends, and does the iview system need a protocol JVL can't currently select? [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- Will the third dedicated printer port become JVL's standard on all future machines? (Raised, not settled.) [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Sources

- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- [[raw/game_design_meeting_march_7_2025.md]]
