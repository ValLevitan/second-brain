---
type: decision
title: Biratka's old updater repository is archived — it is not used in Flex IQ or Flex Pay, USB-stick updates still work through RAUC, and a full reinstall is by micro-SD card
date: 2026-10-09
aliases: [archive the updater repo, за архивировать репозиторий, old updater, апдейтер, RAUC, раук, USB update, прошиться с USB стика, micro SD full reinstall, микроэздешка]
source-count: 2
status: active
open-commitments: 1
open-questions: 0
---

# The old updater repository is archived

**Decided** by [[wiki/people/pavel.md|Pavel Frolov]] at the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 Minsk stand-up]] (Russian).

- **Biratka's finding.** [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"): the updater he wrote "не используется сейчас не в… флекс айкью ни в [флекс пей]. Я так понимаю, что репозитории можно удалять." [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- **USB is not lost.** Pavel: "То есть мы удаляем возможность прошиться с USB стика." Biratka: "Нет, она осталась" — the code moved inside the project, and it works like the remote update, only the source is the USB stick. [[wiki/people/dmitri-chudinov.md|Chudinov]]: "раук тоже позволяет через [USB]". Biratka: "Он сейчас работает через раук… Я прям проверил на [flex pay] на железе." [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- **Chudinov's caveat.** He built it on IQ with room for USB, but did not build bundle download from the server for the stick; bundles are rolled out remotely [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].
- **Update vs reinstall.** Biratka: the stick does an update of a running system; a full reinstall is "через микроэздешку" (micro-SD). Pavel: "Да пожалуй." [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- **The ruling.** Pavel: "Хорошо, значит тогда можно будет этот репозиторий за архивировать." Biratka: "Да я тогда Андрею скажу" [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]. "Андрей" = [[wiki/people/andrey-bosik.md|Andrey Bosik]] by context (he runs the GitHub/DevOps side — **inference**).

Context: the update design of [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]].

## Open commitments

- [ ] [[wiki/people/alexander-biratka.md|Alexander Biratka]] — ask "Андрей" to archive the old updater repository — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
