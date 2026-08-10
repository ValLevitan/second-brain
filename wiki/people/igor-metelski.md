---
type: person
title: Igor Metelski
date: 2026-07-14
aliases: [Igor Metelski, Igar Miatselski, Miatselski, Igor, Igor Mitelsky, Мительский, Mitsierski, Igor Mitsierski]
disambiguation: "RGS engineer on Efim Podvoiski codebase (= payroll Igar Miatselski). One of FIVE Igor-named people (owner-ruled): Igor Donis (Financial Controller → wiki/people/igor-donis.md), Igor (Ihar) Nazarenka (mobile-app, owner-confirmed 2026-07-14 → wiki/people/igor-nazarenka.md), Igor Starovoytov (contractor industrial designer → wiki/people/igor-starovoytov.md), Igor Metelski (RGS engineer, = payroll Igar Miatselski → wiki/people/igor-metelski.md), Ihar Hrybko (UX/UI → wiki/people/ihar-hrybko.md). Resolve by context: finance/corporate → Donis; mobile app/UI + new-market ops → Nazarenka; cabinet/industrial design → Starovoytov; RGS/online-integration code → Metelski; queue anything fitting none."
source-count: 11
open-commitments: 1
---

# Igor Metelski

Igor Metelski is a JVL engineer who works on the codebase [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] owns (the RGS / online-integration code). He is named "**Igor Metelski**" on the Mar 17 2025 "reversing/distilling code into requirements" call. [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]

- On that call, [[wiki/people/aaron.md|Aaron]] named Igor (alongside Efim) as one of the two engineers whose knowledge is currently locked in their heads — the point of moving the code to Git and documenting it is to make the code "functional and usable without you guys necessarily present" (a bus-factor concern). [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]
- [[wiki/people/val-levitan.md|Val]] noted Igor was **on vacation until the following Monday** (the week of the 24th) and asked Efim to make the SVN-to-Git migration a priority that week. See [[wiki/decisions/2025-03-17-migrate-rgs-codebase-svn-to-git.md]]. [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]

## RGS Git-migration assignment (Mar 31)

- On the Mar 31 working session (see [[wiki/meetings/2025-03-31-rgs-git-migration-working-session.md]]) Aaron gave Igor the core task: "I need you to work with Andre and Afim [i.e. [[wiki/people/andrey-bosik.md|Andrey Bosik]] + [[wiki/people/efim-podvoiski.md|Efim]]] to get the remaining... SPN [SVN] repos mapped over to git," and to fully build the freshly-cloned RGS **locally on a workstation** first (Windows or Linux, his pick). [[raw/rgs_git_migration-march-31-2025.md]]
- Aaron asked whether he knew git **submodules**; Igor: "No, not really" — Aaron then taught the concept (a repo reference that recursively clones dependent repos, replacing the SVN `Checkout All` batch file). Igor's practical focus: "tomorrow we just need to build the whole project locally," asking whether Andrei and Yefim could migrate the math engine ("mass.engine") to git by then. [[raw/rgs_git_migration-march-31-2025.md]]
- Igor "is afraid that he won't be ready for tomorrow," so the check-in moved to **Wednesday**. [[raw/rgs_git_migration-march-31-2025.md]]
- Later the same day Aaron told Val that Efim and Igor "were totally unaware... had no curiosity either" about the AI-tooling work Val demonstrated; on Val's OpenRouter account an "Igor" is the **top JVL token user at ~$155** — context (same-day RGS session, listed alongside Efim) suggests this Igor, recorded as an **inference**, not certain (could be another Igor). [[raw/vector_meeting_db-march-31-2025.md]]

## Open commitments

- [ ] Igor — start an engineer's/discovery/findings log of what it took to get the RGS to build correctly on a workstation — due Wednesday — [[raw/rgs_git_migration-march-31-2025.md]]

**Identity notes.** One of five Igor-named people (see the §4 registry; Igor Donis = finance; the mobile-application Igor; Igor Starovoytov = industrial designer) — resolved by context (embedded/RGS code, works with Efim). **Owner-confirmed (2026-07-14):** he is the same person as the Minsk-payroll "**Igar Miatselski**" — "Metelski" is the Belarusian rendering of the Russian form; **Igor Metelski** is canonical, **Igar Miatselski** an alias. The payroll cross-reference in [[wiki/topics/minsk-staff-roster.md]] is now resolved. Separately, the Mar 17/18 embedded-group call mentions an "Igor" who worked on the FlexPort graphical interface and language support — unclear whether that is this Igor, the mobile-app Igor, or another (flagged; not attributed here).

## Apr 16 2025 — to be pulled into Omni feature development

In the Omni daily, when asked who besides Sasha/Anton/Hrybko would develop the framework features, Val named that both **Kharetsky** (LGS) and **Miatselski** should be involved. [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]

## Apr 22 2025 — Calle Ocho feature assignment

On the scheduling session ([[wiki/meetings/2025-04-22-calle-ocho-omni-feature-scheduling.md]]) Igor Metelski ("Игорь Мительский") was assigned the **Denomination Selector screen (FRAM 1 Messages)**, the **debug outcome-selection menu (FRAM 652)**, **Checkpoint Messages**, the **Game Dashboard (FRAM 672 + counters 673–677)** and **Help Screen Integration** for the Calle Ocho Omni port. See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/omni_calle_ocho_scheduling-apr-22-2025.md]]

## June 26 2025 — Omni grooming (free spins, topper integration)

On the [[wiki/meetings/2025-06-26-omni-schedule-grooming.md|Omni schedule grooming]] Metelski ("Игорь"/"Игорю метельному") finished the **free spins** scenes and is assigned the **topper integration** next week (plus an **LED-highlight** task, since he can read the old code). See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/OMNI_schedule_grooming-june-26-2025.md]]

## Jul 31 2025 — cited as the programmer archetype for the amusement revival

On the [[wiki/meetings/2025-07-31-amusement-games-revival-pavel.md|amusement-games revival session]], Pavel described the programmer profile the project needs — "**someone like Igor Metelski**," writing **TypeScript** (no C++) — using Igor as the reference archetype. See [[wiki/topics/amusement-games-revival.md]]. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]

## Feb 12 2026 — away ~2 months in a military training camp

On the [[wiki/meetings/2026-02-12-game-development-review.md|Feb-12 game-dev review]] [[wiki/people/efim-podvoiski.md|Efim]] reported that "**Igor Mitsierski**" is **away for two months in a military training camp** (with **limited internet and only a few hours a day of phone access**) — a risk to finishing the South Dakota release with a single programmer. Plan: [[wiki/people/anton-leshkevich.md|Anton]] is to reach Igor to learn where he stopped, then take **2–3 days to scope the assignments he will inherit** from Igor; Pavel/Irina involved. ("Mitsierski"/"Igor Mitsierski" is another transcription garble of Metelski — added to aliases.) [[raw/Game_Development-February-12-2026-1.md]]

## Aug 3 2026 — ran the RAGE→NOVA migration experiment; next: horizontal South Dakota game

At the [[wiki/meetings/2026-08-03-rage-nova-migration-experiment.md|Aug-3 experiment sync]] Igor presented his AI-assisted RAGE→NOVA conversion (the Jul-20 spike): using a playable NOVA game ("Kali Ocha") as reference, he had **Claude** convert a same-math RAGE game, **"Dragon's Reign,"** into NOVA — symbols, main scene, free-spins scene, dialogs — reusing RAGE resources directly. The reference conversion took ~**1.5 days** of clean work; with Claude's reusable scripts a similar re-skin could take ~**3 hours**. He is also using Claude for the current **Dakota release** tasks and reports it works fine with **C++**. Pavel called Igor "the biggest pessimist in the company," so his positive read carried weight. He was assigned the next, harder experiment: convert a **horizontal** South Dakota game (candidate **"Nikena"**) porting **logic** too, and load it onto the reference machine to check appearance/performance on target hardware (RK3568 "76" / V1000) — reviewed **Aug 17**. Detail on [[wiki/topics/nova-platform-architecture.md]] (Aug-3) and [[wiki/decisions/2026-08-03-no-en-masse-rage-to-nova-migration.md]]. [[raw/Meeting_Transcript_Rage_to_Nova_Migration_Experiment-August-3-2026.md]] [[raw/Meeting_Notes_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]

## Sources

- [[raw/Game_Development-February-12-2026-1.md]]
- [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- [[raw/OMNI_schedule_grooming-june-26-2025.md]]
- [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]
- [[raw/Meeting_Notes_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]
- [[raw/Meeting_Transcript_Rage_to_Nova_Migration_Experiment-August-3-2026.md]]
- [[raw/minsk_staff_roster_2025_names-only.md]]
- [[raw/rgs_git_migration-march-31-2025.md]]
- [[raw/vector_meeting_db-march-31-2025.md]]
- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- [[raw/omni_calle_ocho_scheduling-apr-22-2025.md]]
