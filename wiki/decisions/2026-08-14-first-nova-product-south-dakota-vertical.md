---
type: decision
title: Aug-14 NOVA release sequencing — first-NOVA-product claim SUPERSEDED (owner ruled South Dakota VLT-2 on 2026-09-01); Nebraska stays on Rage, Georgia V3 on the current platform
date: 2026-08-14
aliases: [NOVA release sequencing, South Dakota Vertical 01 first Nova product, first Nova product, Calle Ocho to GLI]
source-count: 3
status: active  # titular first-NOVA-product claim SUPERSEDED by the owner ruling of 2026-09-01 (= South Dakota VLT-2); the rest of this decision still stands — see the dated Updates
open-commitments: 2
open-questions: 0
---

# Aug-14 NOVA release sequencing — first-NOVA-product claim superseded; Nebraska stays on Rage, Georgia V3 on the current platform

> **Superseded in part (owner ruling, 2026-09-01):** the first NOVA product is **South Dakota VLT-2**, not South Dakota Vertical 01. See [[wiki/decisions/2026-09-01-first-nova-product-south-dakota-vlt-2.md]]. Everything else below still stands.

On the [[wiki/meetings/2026-08-14-nova-migration-release-sequencing.md|Aug 14 2026 NOVA migration-plan session]] the game team decided how and in what order to move games from the current V1000 / Rage platform onto FP7 / NOVA. This refines the platform direction on [[wiki/topics/nova-platform-architecture.md]] and the ~6-month South Dakota port ruled on [[wiki/decisions/2026-08-03-no-en-masse-rage-to-nova-migration.md]]. Attendees: [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/michael-gottlieb.md|Michael Gottlieb]], [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/lena.md|Lena Zhukova]], [[wiki/people/efim-podvoiski.md|Efim Podvoiski]]. [[raw/Meeting_Notes_NOVA_Migration_Release_Sequencing-August-14-2026.md]] [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]

## What was decided

- **The first product to launch on NOVA / FP7 will be South Dakota Vertical 01, targeted ~March 2027.** Chosen as the lowest-risk first NOVA product: if it slips, the existing South Dakota D27 (with the Keno games) keeps performing, so a slip of a week or two is survivable. (Verbalized by Michael, agreed by Val and Juan.) [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]] [[raw/Meeting_Notes_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- **Nebraska D2702 stays on Rage / the current platform** and releases toward the end of 2026 — it is NOT moved to NOVA. Val's earlier suggestion to do Nebraska on NOVA was dropped after Juan and Lena warned it would add a 2–3 month delay (porting is ~1 week/game plus the learning curve and bugs, on top of new-game development). [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- **Georgia's V3 release stays on the current platform, targeting September 1.** NOVA would be a later Georgia release — "more like V4 than V3." [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- **Submit "Cayocho" (Calle Ocho), which already runs on NOVA, to GLI to test and certify the NOVA platform** — in parallel, starting with a single game (possibly one per category plus Liquid Glass). A Keno submission was judged not important. (Decided by Val, agreed by Michael, Lena, Efim.) See [[wiki/decisions/2025-04-14-calle-ocho-first-omni-framework-game.md]]. [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]] [[raw/Meeting_Notes_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- **Lena develops NOVA games in parallel while NOVA keeps changing.** Peripheral/API/Rust changes to the platform don't affect how she builds games, so platform maturation and game-making run in parallel, not in sequence (Val: proven because Calle Ocho already runs on NOVA). [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]

## Rationale and facts established

- NOVA / FP7 runs only on **new hardware and cabinets**; the V1000 will no longer be manufactured. There is **no forced hardware upgrade on the installed base** — new offerings go on new cabinets, and Georgia's large installed base gives runway to keep selling software on existing V1000/D27 cabinets. [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- **No value in porting old or failed games.** The group rejected Val's opening idea of converting the entire South Dakota library (old + new): there is no logic to porting the non-liquid-glass South Dakota, or dead titles (**Dutch Mills**, **Liberty Spins**). They confirmed a **single game** can be ported, not only a whole ISO package. [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- **The Peach bonus is dead** — games move onto **Liquid Glass** and away from the Peach bonus (the Peach *titles* are reimaginable). Val treats games as reimaginable life-cycle items ("like a James Bond movie"). [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- Georgia's coming **"Blaze"** release is a "best of" hybrid: ported and updated older titles on Liquid Glass (Enhanced Nudge, Match-3 Progressive) plus new **Jackpot Rush** and **Fiery Ice** titles (neither has run on D27 in Georgia before). [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- **Regulatory gates by market:** South Dakota carries **GLI** approval risk (the big gate); Nebraska has no GLI approval; Texas is minor (via **Eclipse**). [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- **South Dakota Vertical needs three brand-new games** — **Solar Keno, Aaron's Pub, Dakota Bison** — that must be **built, not converted**, because they never existed in vertical. [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]

## Open commitments

- [x] Engineering team — submit Calle Ocho on NOVA to GLI to certify the NOVA platform (start with one game; aim approval ~January) — due TBD — **CANCELLED by owner ruling 2026-09-01: Calle Ocho is "no more" the certification vehicle** (see [[wiki/decisions/2026-09-01-first-nova-product-south-dakota-vlt-2.md]]) — [[raw/Meeting_Notes_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- [ ] [[wiki/people/lena.md|Lena Zhukova]] — build the South Dakota Vertical games (Solar Keno, Aaron's Pub, Dakota Bison) new for vertical in NOVA, once Nebraska is finished — due after the Nebraska release — [[raw/Meeting_Notes_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- [ ] [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] — finish his math work before his planned Sept 15 2026 absence — due before Sept 15 2026 — [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]

## Note on later evolution

Four days later, the [[wiki/meetings/2026-08-18-rage-nova-migration-experiment-review.md|Aug-18 review]] framed a more aggressive NOVA timeline — deliver the first NOVA platform version (targeted at the South Dakota "Salta Cota" machine) to GLI by ~Nov 1, using the horizontal Dragon Pays migration experiment rather than Calle Ocho as the certification vehicle — while keeping the South Dakota Vertical full release ~March 2027 and leaving the Rage release calendar unchanged. Val flagged that as "the plan, not yet a hardened schedule." Tracked on [[wiki/topics/nova-platform-architecture.md]].

### Update — Aug 26 2026: Val reopened the titular question himself

On the [[wiki/meetings/2026-08-26-alignment-planning-nova-september-releases.md|Aug-26 alignment call]] Val stated outright that he is **not sure what the first NOVA release should be** — "здесь я немножко не совсем уверен… Я понимаю, что будет являться первым релисом на ново" — and asked for **two tracks in parallel**: (a) **South Dakota VLT-2 as a direct Rage→NOVA migration**, and (b) **a new Georgia COAM version on NOVA built on D27, explicitly not vertical** ("только на ди 27 не на не вертикально") — a rework of the popular games rather than new ones. **Neither track is the South Dakota Vertical 01 of this decision's title**, and neither **Calle Ocho** nor the Aug-18 **~Nov 1 GLI** target is mentioned on the Aug-26 call or on the [[wiki/meetings/2026-08-28-dragon-pays-nova-conversion-review.md|Aug-28 review]]. [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

What is *confirmed* rather than reopened: the sequence itself is unchanged — deliver the two Sept-1 items, spend September narrowing capabilities to MVPs in Jira, and start developers on NOVA from about **October 1** ("Ориентировочно с 1 октября"). Pavel named the cost of running two tracks — QA parallelisation, and designers having to support vertical *and* horizontal cabinets for one and the same game. [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]

**Status handling (§3):** recorded as **evolution, not contradiction** — Val reopened an open question in his own words; the sources do not assert two incompatible facts about the same period, so nothing is filed under `## Open contradictions`. The decision stays `active` because its non-titular elements (Nebraska on Rage, Georgia V3 on the current platform, Lena building in parallel, the three new vertical games) still stand, **but the titular claim "First NOVA product = South Dakota Vertical 01" is no longer settled** — do not read the title as current state without this Update. Queued for the owner as LIVE OPEN #29 in [[wiki/overview.md]].

### Update — Sept 1 2026: owner ruled the first NOVA product is South Dakota VLT-2

Asked directly which product is first on NOVA, Val answered **"SD VLT-2"** — selecting the direct Rage→NOVA South Dakota migration track he had floated on Aug-26, **not** the South Dakota Vertical 01 this decision's original title named. The titular claim above is therefore **superseded**; the decision's other elements (Nebraska on Rage, Georgia V3 on the current platform, Lena building in parallel, the three new vertical games) are unaffected. Full ruling on [[wiki/decisions/2026-09-01-first-nova-product-south-dakota-vlt-2.md]]. Owner ruling — its own citation per §16, no raw source.

**Certification, ruled 2026-09-01 (same day):** Val ruled **Calle Ocho is "no more"** the GLI certification vehicle — the bullet above naming it is superseded — and clarified the two GLI items: **September 1 2026 is the schedule for the RAGE-based South Dakota VLT-2 submission (not NOVA)**, which slipped ~2 days in execution (actual ≈ Sept 3) — a slip, not a re-plan — while **NOVA has no GLI date yet**, so the Aug-18 ~Nov-1 platform target has lapsed with nothing replacing it. See [[wiki/decisions/2026-09-01-first-nova-product-south-dakota-vlt-2.md]].

## Sources
- [[raw/Meeting_Notes_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- [[raw/Meeting_Transcript_NOVA_Migration_Release_Sequencing-August-14-2026.md]]
- [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
