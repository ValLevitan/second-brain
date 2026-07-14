---
type: decision
title: Base Nebraska on existing Georgia software with the conservative nudge
date: 2025-03-14
aliases: [Nebraska software decision, no-hands Georgia build, revert nudge for Nebraska, conservative nudge]
status: active
source-count: 1
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

## Open commitments

- [ ] Juan — confirm with the **Nebraska Department of Revenue** whether **Eclipse** is an acceptable testing lab (the regulations name GLI) — due unspecified — [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- [ ] Juan/Lena — write the **full detailed Jira requirement** for the Nebraska build (all enhancements, hands removed, nudge reverted) for traceability — due unspecified — [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]

## Sources

- [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
