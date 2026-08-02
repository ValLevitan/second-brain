# Meeting Summary — alignment on various initiatives
**Date:** July 16, 2026, 10:00–11:00 AM Eastern
**Duration:** ~58 minutes (from transcript timestamps)
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_Galaxy_Nova_Platform_Strategy-July-16-2026]]

## Summary

Strategy session on how to move forward with the Galaxy transition, the move to GitHub, the Nova vs. Rage platforms, and where Miranda fits. Note: the meeting was mostly in Russian and the transcription garbles many product names (Rage appears as "рейч/речь", GitHub as "гетхаб/кидхап", Biratko as "пиратка/биратка"). Only clearly supported points are recorded. Personal names verified against the company directory (ms365, July 16): "Koretsky" = Evgeny (Zhenya) Kharetski; "Dima Khantov" = Dmitriy Khandov; "Shamanov/Tsmanov" = Sergey Tsimanov; "Chudinov" = Dzmitry Chudzinau; "Ilishkevich" = likely Anton Leshkevich.

**DataCenter move to GitHub.** Pavel reported that a task was created that day for Zhenya Koretsky to move the DataCenter repositories (all branches, from SVN) to GitHub and set up build actions. Val was surprised — he considered the decision still open and would have waited — but accepted it. Pavel's case: the move is relatively independent, the old builder can be adapted to pull sources from GitHub, and it brings the new workflow (commit history, feature branches, prose, testing). The cost is that it takes Koretsky away from potential Nova work.

**Why Rage is a dead end for designers.** Pavel explained that Rage's rendering engine (he believes it is Ogre, an old open-source 3D engine) has been unsupported for roughly 15 years; all improvements were made in-house. The designer tool versions are locked to the engine version. The old packages are unlicensed, can no longer be downloaded anywhere, and must run on offline machines. Moving the Rage framework and games to GitHub is also problematic because they are very large (video files, graphic scenes) — per Sasha and Igor.

**Resources.** Biratko is busy (currently on the 3-Sitler work), must still finish the Flex Dispenser if they want to show it in August, and wants vacation in about two weeks — so he is unavailable for extra tasks for about a month. The evaluation task of running a test Nova game on the RK3568 ARM board (planned to start around the 20th) may need to go to Igor Metelsky or to Zhenya instead. New, more powerful boards have not arrived; a package expected the next evening may contain them. Val proposed planning around August 15, when several developers free up (Koretsky, Dmitrievsky, Ilishkevich, Efim finishing the Rust math transition, Chudinov and Shamanov finishing transactional work; Irina noted South Dakota with GEK 3 wraps up around then) — then assign the Galaxy and Nova transition work.

**Miranda-for-Rage idea rejected.** Pavel floated building a Miranda-like design tool for Rage so designers could export scenes to either platform. All agreed it is a dead end: too big a project, and Rage's remaining life is too short — wasted resources.

**Preferred hybrid path.** Of the two hybrid options (new tool exporting scenes that run on Rage, vs. converting the ~100 existing Rage games to Nova), Pavel considers the more promising path to use the Nova framework, develop new games on it, and find a relatively easy way to convert old Rage games — reusing existing game resources but rebuilding scenes (possibly with AI help). Browser-based games would then behave the same on any new platform (ARM or x86), performance permitting. Val framed it as three questions: can Rage be split into its engine (replaced by PixiJS in the Nova scheme) and its development ecosystem (replaced by Miranda); can the second block be swapped to Miranda; and can scene rebuilds for ~50–100 games be automated. Pavel agreed with the framing but said it needs concrete block diagrams (old: Rage Studio + Ogre; new: Unity + Miranda + PixiJS; resources reusable if there is a simple conversion procedure).

**Timelines (Pavel's estimates).** Machine side: about 2 months. Galaxy side with new screens and minimal CMS/RAS support: at least 6 months. About 95% of new screens exist but have not been QA-verified (checked only by developers, not by Ira or Ivan). New RAS features (e.g., manual or partly manual setup passes over an applied RIS file) are not designed yet.

**Follow-up meeting.** Val will set up a meeting the next day (July 17) with Koretsky and Biratko (plus Pavel and Irina), focused on the Rage decomposition and game-conversion question — at 7:00 Val's time, earlier if possible per Irina's request. Dima Khantov is deliberately not invited yet; they want to hear Sasha's view first since he sees fewer limitations.

**Prose and requirements workflow.** Val laid out the working method: from code, generate prose; from prose, build an architecture block diagram; correct it; have Claude adversarially re-review the prose; then generate requirements with acceptance criteria that are unique and testable against the code, and only then capabilities. Narrowing straight to capabilities cuts off the path back to requirements. Pavel had tried prose generation on the RK3568 SDK with Claude and agreed to continue with this approach.

Side item: Irina will look into the mismatched sums on the screens Felipe sent pictures of (code 3 / unpacking after key press); she could not check during the meeting because her VPN was off.

## Decisions Made

- **DataCenter SVN-to-GitHub migration proceeds with Evgeny (Zhenya) Kharetski** — relatively independent move that unlocks the new GitHub workflow; Val accepted it despite preferring to have deliberated longer. (Assigned by Pavel Frolov; accepted by Val Levitan)
- **No Miranda-like design tool will be built for Rage** — Rage's remaining life is too short to justify the effort; resources would be wasted. (Raised and self-rejected by Pavel Frolov; Irina Shishko concurred; Val Levitan did not object)
- **Preferred direction: Nova framework plus conversion of existing Rage games** — reuse game resources, rebuild scenes, possibly automated with AI; better portability to new ARM/x86 platforms. To be detailed at tomorrow's meeting. (Pavel Frolov, agreed by Val Levitan)
- **Hold a focused follow-up meeting July 17 with Kharetski and Biratko; start without Dmitriy (Dima) Khandov** — hear Sasha's (likely Alexander Biratko's) less-constrained view first. (Val Levitan, Pavel Frolov)
- **Continue with the prose → architecture block diagram → requirements/acceptance-criteria workflow** — acceptance criteria must be unique and testable against code. (Val Levitan, agreed by Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Schedule the follow-up meeting with Kharetski, Biratko, Pavel, and Irina on Rage decomposition and game conversion (7:00 Val's time, earlier if possible) | July 17, 2026 | High | "Хорошо, я на завтра назначу от митинг" |
| 2 | Evgeny (Zhenya) Kharetski | Move DataCenter repositories (all SVN branches) to GitHub and set up build actions | TBD | Normal | Task created July 16; reported by Pavel. Transcribed as "Koretsky"; resolved via directory |
| 3 | Irina Shishko | Review the mismatched sums on the screens from Felipe's pictures (code 3 / unpacking after key press) | TBD | Normal | "Ну ладно я посмотрю" — VPN was off during the meeting |
| 4 | Pavel Frolov | Prepare block diagrams of the old (Rage Studio + Ogre) and new (Unity + Miranda + PixiJS) toolchains; Pavel to assign internally | TBD | Normal | Confirmed by Val July 16: assigned broadly to Pavel, who will delegate. Diagrams frame the July 17 follow-up discussion |

## Open Questions

- Who takes the RK3568 evaluation task (test Nova game on the ARM board) — Igor Metelski or Evgeny Kharetski — given Biratko is unavailable for about a month? (Raised by Pavel Frolov)
- Can scenes for the ~50–100 existing Rage games be rebuilt on existing resources in a largely automated way? (Raised by Val Levitan; main topic for the July 17 meeting)
- Whether the new, more powerful ARM boards are in the package arriving July 17 evening. (Raised by Val Levitan)

## Dispatch Log

---
*Processed from Teams transcript on July 16, 2026, 11:45 AM Eastern*
*Source meeting: alignment on various initiatives (July 16, 2026, 10:00 AM Eastern)*
