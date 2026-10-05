---
type: decision
title: The fix goes out as a re-release, not a hack on a production machine — as fast as possible, and only that one commit goes in
date: 2026-09-29
aliases: [no hack we re-release, перевыпускать, хак делать не будем, re-release 4.50.2, 4502, one commit only, только этот коммит, connectivity change, Бракаст library, modem fix rebuild, фикс по модемам]
source-count: 2
status: active
open-commitments: 3
open-questions: 2
---

# The fix goes out as a re-release, not a hack — one commit only

Reported by [[wiki/people/pavel.md|Pavel Frolov]] at the [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|Sept 29 2026 Minsk stand-up]] (Russian) as a ruling [[wiki/people/val-levitan.md|Val Levitan]] gave the day before: "**вал вчера сказал что мы этот хак делать не будем. Мы что, мы будем перевыпускать?**" [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]. No Sept-28 recording in the corpus carries the ruling itself; it is recorded here second-hand, as Pavel gave it.

## What "the hack" was

The alternative Pavel had discussed the day before: take [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]]'s fix, once built, and "**как вчера договаривались просто на вот эту продакшн машину подложить и проверить**" — slip it onto the production machine and check it there. That is read as the hack Val refused (**inference**; Pavel does not spell out the word's referent) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].

What the fix is for is not fully stated. [[wiki/people/ivan.md|Ivan]]'s main task that day is "**фикс по модемам пересобрать всё сделать, проверить**" — rebuild and verify the modem fix — and Pavel later refers to "машины, то, что сейчас женя делает с Иваном", so Kharetski's fix and Ivan's modem rebuild concern the same machine work (**inference**) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]. Which product and market the release serves is not said.

## The ruling, as spoken

- **Re-release, as fast as possible.** Pavel: "**Да как можно быстрее. Ну не сегодня понятное дело. Ну скорее всего не раньше завтра**" — not today, probably not before tomorrow (Sept 30). Kharetski: "Прям сейчас перевыпускать" [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].
- **Timing depends on engineering and on Ivan's check.** [[wiki/people/irina-shishko.md|Irina Shishko]]: "**от вас зависит, когда вы что отдадите и когда мы ну не мы а ваня проверит**" [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].
- **Only this commit.** Irina: "**Нам нужно, чтобы пошёл Только этот камит туда и больше ничего**" — a very fast release carrying one commit [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].
- **The build number.** Kharetski: the fix can be checked "на 4 6" (4.60) now, or "точнее на 502" if they re-release — the re-release build is spoken as "502", "4504502" and "3 этот 4502", read as **4.50.2** against Ivan's stand on "4501" (4.50.1) and the team's "460" (4.60) (**inference** on the dotted form; the derived notes read it the same way) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].

## The library change inside it

Kharetski: the commit is "не совсем" one change — a library was changed ("Бракаст" — **unclear**; the notes read it as "broadcast"). "**я думаю, что им пофиг на то, что там библиотека менялась. Ну они ж не видят этого**" — whoever receives the release will not see it. Pavel: "**мы это заявим, что у нас изменения с связанные с коннективити**" — it will be declared as a connectivity change. Irina asked why the library changed; Kharetski: "**надо было так её поменять. Быть править нормально и подстраховаться на будущее**" — to fix it properly and hedge for the future [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]. Who "они" are (a lab, a customer) is not said.

## Side effect on the autotest stand

Kharetski: switching the stand from 4.60 to 4.50.2 removes "это питерство, которое ваме нужно для автотестов" (the word is garbled; something Ivan needs for his autotests), so it may have to be switched back and forth. Ivan: "**У меня бинт есть собранные, просто его не буду сносить, да и всё**" — he has a build and will not tear it down. Irina: or store it somewhere [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].

Kharetski will tell Ivan when the build is ready: "**я ване напишу тогда как будет готов**" [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].

## Open commitments

- [ ] [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] — finish the fix ("сейчас я уже почти готов"), build 4.50.2 with that one commit, and write to Ivan when it is ready — due Sept 29 2026 — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
- [ ] [[wiki/people/ivan.md|Ivan]] — rebuild and verify the modem fix — due unspecified (the re-release "не раньше завтра", Sept 30 2026) — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — issue the re-release, declared as a connectivity change — due as fast as possible, not before Sept 30 2026 — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

## Open questions

- What the fix is for and which product/market the re-release serves — the sources say only "фикс по модемам" and "продакшн машина" — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
- The exact re-release date (Pavel: not before tomorrow) and whether the library change passes as "a connectivity change" with whoever receives the release — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

## Related

- [[wiki/decisions/2026-09-14-main-branch-must-always-build-and-the-code-belongs-to-the-project.md]] — the branch discipline this release runs under (link is context, not a citation).
- [[wiki/topics/github-release-management-pipeline.md]] (Sept 29) — the version table Kharetski moved into main the same morning.

**§15.8:** clear — release process only. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
