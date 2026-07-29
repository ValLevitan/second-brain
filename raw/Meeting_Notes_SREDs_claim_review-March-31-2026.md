# Meeting Summary — SR&ED 2025 Claim Review
**Date:** March 31, 2026, 7:12 PM Eastern
**Duration:** ~25 minutes
**Attendees:** Val Levitan, Efim Podvoiski, Genadi Peari, Lena Zhukova

## Summary

This meeting was a follow-up review of the SR&ED 2025 claim preparation, continuing from the March 20 kickoff and the V1.6 candidate project list distributed on March 22. The primary objectives were to establish claim ownership for each of the 22 candidate projects, capture descriptions of additional claims not on Val's original list, and agree on next steps for consolidating the master list.

### Claim Ownership Status

The meeting opened with a quick tally of claims taken from Val's original list of 22 candidate projects. In the initial count, six claims were reported as assigned: Efim took one from the list (plus one of his own not on the list), Lena took two, and Genadi took two from the list (referencing items #3 Flex-Port Bill Validator Interface and #4 Flex-Port Hardware Design) plus three additional claims of his own.

A significant portion of the meeting (~4 minutes) was conducted in Russian, during which the team discussed specific contractor assignments — particularly which claims could be attributed to Evgeny Yavorski and Evgeny Alexeyev. The Teams auto-transcription captured this section poorly, rendering much of the Russian dialogue unintelligible. However, the outcome of this discussion fed into the detailed per-claim review conducted later in the meeting.

### Detailed Per-Claim Review

The team walked through all 22 claims from the V1.6 list, assigning ownership or marking them undecided:

| # | Project | Status | Assignee(s) |
|---|---------|--------|-------------|
| 1 | Test-360 Automated Game Testing | Assigned | Alexeyev, Yavorski (contractors) |
| 2 | Flex-POS RK3568 Firmware/OS | Assigned | Evgeny Alexeyev, Evgeny Yavorski |
| 3 | Flex-Port Bill Validator Interface | Assigned | Evgeny Alexeyev, Evgeny Yavorski |
| 4 | Flex-Port Hardware Design | Assigned | Genadi Peari, Evgeny Alekseev |
| 5 | Payment HUB Cloud Platform | Assigned | Alexeyev, Yavorski |
| 6 | Flex-POS Terminal Application | Assigned | Alexeyev, Yavorski |
| 7 | Keno Math Engine | Assigned | Efim Podvoiski |
| 8 | OMNI Game Framework Engine | Undecided | — |
| 9 | Progressive Controller System | Undecided | — |
| 10 | LGS Game History Module | Undecided | — |
| 11 | EGM Initial Setup / Remote Config | Undecided | — |
| 12 | Control Server Cloud Platform | Undecided | — |
| 13 | Manifest-Based Asset Reconstruction | Assigned | Lena Zhukova, Andrei Handov, Dimo Handov |
| 14 | EGM Printer/Ticket Subsystem | Assigned | Alexeyev, Genadi Peari |
| 15 | Game Performance on FP7 | Undecided | — |
| 16 | Pattern Match Consolation Game | Undecided | — |
| 17 | Multi-Product EGM Support | Undecided | — |
| 18 | Kubernetes Platform Engineering | Undecided | — |
| 19 | Cisco ASA Modernization | Undecided | — |
| 20 | MCP/AI Jira Analytics | Undecided | — |
| 21 | AD Modernization | Undecided | — |
| 22 | Game Art / Visual Design | Assigned | Lena Zhukova, Dimo Handov |

**10 claims assigned, 12 undecided** from the original list.

Efim initially suggested #12 (Control Server) could go to Yavorski, but corrected himself to "undecided." He also commented that not all 22 items are clearly SR&ED material, specifically questioning consolation games (#16). Regarding #13 (Manifest), Efim suggested Andrei Handov could also contribute to Liquid Glass (#22) and be "more heavily on manifest."

**Discrepancy on #15:** When Val asked Lena about additional claims, she responded "only 15 and 22" — suggesting she considers herself assigned to #15 (Game Performance on FP7). However, during the numbered review, Efim called #15 "undecided" and Val accepted. This needs clarification.

### Additional Claims Not on Val's List

Four additional claims were identified beyond the original 22:

**Genadi Peari — 3 new claims:**

1. **Flex S Concept Evolution Design** — The evolution of the Flex S product line: redesigning monitors and cabinet for a modern look, improved audio, configurability with more monitors including new graphical elements, and new industrial design. The technological challenge was how to combine all these features into a cohesive product.

2. **43-Inch Curved Monitor for Flex S** — Development of a curved monitor version using smart plastic design with integrated lights around the monitor that visually increase the perceived curvature — avoiding expensive chemically-aged curved LCD panels. Challenges included plastic design with lighting, using curved TFT alternatives, and integrating a curved touch screen.

3. **New Audio System for Flex S** — An audio system without a large subwoofer that still produces low frequencies. The design eliminates visible speaker grills by bleeding sound under the monitors. Work involved acoustic simulations, prototype production, and ordering specially-developed speakers for better space utilization.

**Efim Podvoiski — 1 new claim:**

4. **Volatility & Financial Risk Modeling Framework** — Efim read his full technical write-up during the meeting. The project addresses the mismatch between traditional volatility metrics and real-world operator expectations for slot-based casino games. An operator in Florida reported concerns about perceived excessive volatility that standard deviation metrics didn't capture.

   - **Problem:** Standard deviation assumes near-normal distributions, but slot outcomes are highly skewed and heavy-tailed due to jackpots and bonus features. Standard metrics don't describe frequency of negative revenue days or perceived risk from an operator perspective.
   - **Technological uncertainty:** (1) Whether a model could accurately represent heavy-tailed distributions while preserving key statistical properties; (2) Whether a significantly faster approach than millisecond-per-spin Monte Carlo simulation could work without sacrificing fidelity.
   - **Approach:** Large-scale outcome sampling (100M+ spins to build empirical distributions), distribution-based abstraction (replacing full game logic with random draws from precomputed distributions), and aggregated simulation.
   - **Key innovation:** Decoupling spin-level simulation from higher-level modeling — a shift from process-based simulation to distribution-based stochastic modeling. Additional innovation: inverse stochastic modeling for game design — defining target outcome distributions before full game design is finalized.
   - **Results:** Simulation speed improved by several orders of magnitude. Ability to evaluate daily casino outcomes, player sessions, and impact of betting distributions. Direct alignment with operator concerns about perceived volatility.

### List Consolidation

Val asked Efim to restructure the master candidate list using Claude: remove the 12 undecided claims, retain the 10 assigned ones, and add the 4 additional claims (1 from Efim, 3 from Genadi). Efim agreed. Val emphasized that since the meeting is being transcribed, Genadi's verbal descriptions can be used by Claude to generate proper claim narratives.

Note: Val referenced "two of Gennadi's" additional claims during this ask, but Genadi described three. The restructured list should include all three.

## Decisions Made

- **10 claims retained from the original 22** — assignments confirmed as listed above. (Decided by Val, Efim, Genadi, Lena)
- **12 claims marked undecided** — remain unassigned; not all may qualify as SR&ED material. (Decided by consensus)
- **4 additional claims identified** — 3 from Genadi (Flex S hardware projects) and 1 from Efim (volatility modeling). (Decided by Val with input from Genadi and Efim)
- **Efim to restructure master list** — using Claude to produce a new consolidated candidate list. (Decided by Val, accepted by Efim)
- **Transcript-based claim generation** — Val will use meeting transcripts + Claude to generate claim write-ups, particularly for Genadi's verbal descriptions. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Efim Podvoiski | Restructure the SR&ED candidate list: reduce Val's original 22 to the 10 assigned claims, add Efim's 1 additional claim and Genadi's 3 additional claims, producing a new consolidated candidate list using Claude | TBD | High | This produces the working version of the claim list that all subsequent write-up work will reference |
| 2 | Val Levitan | Clarify #15 (Game Performance on FP7) assignment — Lena indicated she's on it, but the per-claim review marked it undecided | TBD | Normal | Ensures no claim is orphaned or double-counted |
| 3 | Val Levitan | Resolve the 12 undecided claims — determine which to drop and which to assign | TBD | Normal | Some may qualify (#8 OMNI Framework, #9 Progressive Controller) while others were flagged as borderline |

## Engineering Signals

No engineering signals detected in this meeting. The discussion was administrative — planning and assigning SR&ED tax credit claims based on previously completed work rather than making new technical decisions.

## Open Questions

- **#15 assignment:** Is Lena assigned to #15 (Game Performance on FP7) or is it truly undecided?
- **Undecided claims:** What happens to the 12 undecided claims? Dropped from filing or will ownership be sought?
- **Dennis review:** Efim mentioned "Dennis will give it better name maybe" regarding claim naming — is Dennis (the SR&ED consultant?) expected to review and refine claim names?
- **Genadi's count discrepancy:** Val said "two of Gennadi's" when asking Efim to restructure, but Genadi described three additional claims. The restructured list should include all three.
- **Yavorski and Alexeyev narratives:** Several claims (#1, #2, #3, #5, #6) are assigned to them. Are they writing their own narratives or is someone else writing on their behalf?

## Output

This meeting resulted in the production of **V1.7 of the SR&ED Candidate Projects list**, which:
- Retains 10 assigned claims from V1.6 (renumbered 1–10)
- Adds 4 new claims (numbered 11–14): 3 from Genadi, 1 from Efim
- Drops 12 undecided claims from V1.6
- Adds Claim Owner field to every project
- Includes full SR&ED-format narratives for new claims (drafts for Genadi's, detailed for Efim's)

See: [[SRED_2025-Candidate_Project_V1.7-March-31-2026]]

---
*Processed from Teams transcript on March 31, 2026*
*Source meeting: SRED Review Meeting*