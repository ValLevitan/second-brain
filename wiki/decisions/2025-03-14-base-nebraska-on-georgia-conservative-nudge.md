---
type: decision
title: Base Nebraska on existing Georgia software with the conservative nudge
date: 2025-03-14
aliases: [Nebraska software decision, no-hands Georgia build, revert nudge for Nebraska, conservative nudge, nudge abandoned]
status: active
source-count: 3
open-commitments: 2
open-questions: 0
---

# Base Nebraska on existing Georgia software with the conservative nudge

On the Mar 14 2025 call, [[wiki/people/val-levitan.md|Val]], [[wiki/people/juan-martinez.md|Juan]], [[wiki/people/efim-podvoiski.md|Efim]], [[wiki/people/lena.md|Lena]], [[wiki/people/pavel.md|Pavel]] and [[wiki/people/irina-makarych.md|Irina]] agreed how JVL will build for the **Nebraska** skill market. Full context on [[wiki/projects/nebraska-skill-market.md]]. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]

## What was decided

- **Base = existing Georgia "Peach" software**, not the in-progress Georgia updates; present the **"no hands" version** (the "hands" is part of the common UI and is simply removed). **Peach 4 is excluded** (being redesigned); base on **Peach 1, 2, 3**. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- **Method (Irina's recommendation, adopted):** take the **latest version 1.14 (already in VDEC)** and **revert the nudge to its old/conservative presentation**, rather than modifying the old software — easier and more reliable since everything else is already in VDEC. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- **Keep** the new Georgia enhancements: **dual-SAS**, **TITO**, the **VDEC button changes** (flame the highest three bet buttons only) and the **touch-area** changes. **Remove** the **hands** dependency and the **enhanced nudge** feature. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- **Release in four packs of six games**, as in Georgia. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- **Progressives:** standalone per-device/per-game only (no links); same limit as Georgia (~3,000); use the **lower Georgia top-award numbers** given Nebraska's small locations (4–15 machines). **No SWIFT bonus progressive** (linked), though the RGS/RIS SWIFT parameter can be enabled per machine if needed. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- **Submission path:** send the machine to the **Nebraska Department of Revenue** first (GLI's recommendation) before the lab; **prefer Eclipse** as the lab (to parallel Georgia approvals) pending Juan confirming the DoR accepts it. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- **Documentation:** write a **full detailed Jira requirement** listing all enhancements (for traceability), not a "take latest Peach and back things out" shortcut. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]

## Rationale

- Nebraska is close to Georgia but more favorable (no hands, TITO allowed), so the fastest, most reliable path is to reuse the proven Georgia build and strip the hands + advanced nudge rather than build fresh. Reverting nudge on the already-integrated v1.14 avoids re-integrating all the other new features. The advanced ("Georgia 2") nudge is deferred to Nebraska only as it rolls out for Georgia — acceptance risk is lower than depending on it from launch. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]

## Update (May 8 2025) — the nudge choice was reversed

On the [[wiki/meetings/2025-05-08-game-design-review.md|May-8 game-design review]], after [[wiki/people/juan-martinez.md|Juan]]'s Nebraska market trip, [[wiki/people/val-levitan.md|Val]] **reversed the conservative-nudge element** of this decision: JVL will launch Nebraska on the **enhanced/new nudge** (the same as Georgia), because the incumbent competitor **Vanilla** already runs a nudge and the **regulator confirmed it is not an issue** — "I'll adjust the rec where I said we wouldn't do that. We should do it." The rest of this decision (base on the Georgia "Peach" software, "no hands," keep TITO/dual-SAS, release in packs of six) still stands. See [[wiki/projects/nebraska-skill-market.md]]. [[raw/game_design-may-8-2025.md]]

## Update (May 15 2025) — the nudge is abandoned entirely

On the [[wiki/meetings/2025-05-15-game-design-nebraska-south-dakota.md|May-15 game-design review]], after [[wiki/people/juan-martinez.md|Juan]]'s Nebraska site visit, the Department of Revenue **attorney** (boss of the JVL contact [[wiki/people/brittany-walker-bell.md|Brittany]], who "was not qualified" to have blessed the game) ruled that **nudge does not qualify as skill** — because a wrong nudge can make a winning outcome unwinnable. Val: "Nudge is done… no longer a topic of discussion for this market." This **supersedes both** the original conservative-nudge ruling here **and** its May-8 reversal to the enhanced nudge: **all nudge is dropped**, to be replaced by a Vanilla-style **power-slider skill overlay** (design still open — Lucky Rainbow vs Bullseye). The rest of this decision still stands and is in fact reinforced — base on the Georgia "Peach" software, no hands, keep TITO/dual-SAS, release in packs of six — with the added direction to **flatten pay tables** and feed removed top-wins into a randomly-hitting Swift bonus. Full context on [[wiki/projects/nebraska-skill-market.md]] and [[wiki/topics/slot-game-design-principles.md]]. [[raw/game_design_nebraska_south_dakota-may-15-2025.md]]

## Open commitments

- [ ] Juan — confirm with the **Nebraska Department of Revenue** whether **Eclipse** is an acceptable testing lab (the regulations name GLI) — due unspecified — [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- [ ] Juan/Lena — write the **full detailed Jira requirement** for the Nebraska build (all enhancements, hands removed, nudge reverted) for traceability — due unspecified — [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]

## Sources

- [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- [[raw/game_design-may-8-2025.md]]
- [[raw/game_design_nebraska_south_dakota-may-15-2025.md]]
