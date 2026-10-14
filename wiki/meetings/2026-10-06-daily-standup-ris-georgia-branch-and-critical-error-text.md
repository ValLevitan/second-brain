---
type: meeting
title: Daily stand-up — the urgent RIS changes go to Georgia only on the 1.14 line, the critical-error screen in plain words, MudaGoose removed from the code, prose coverage at 87%, and the Jira warning triangle kept (Oct 6 2026, 4:54–5:41 AM)
date: 2026-10-06
aliases: [Daily Standup meeting Oct 6 2026, Daily Standup RIS Georgia Branch and Critical Error Text, Oct 6 stand-up, RIS Georgia branch, 1.14 branch, carousel for Liza, карусель для лизы, MudaGoose removal, мутагусь, PORT-82, PORT-91, FIT-127, FIX-135, FQ-67, FQ-112, test 69, prose 46 to 87 percent, warning triangle, battery swap cases, log size and update partition]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — RIS Georgia branch and critical-error text (Oct 6 2026)

**Date/time:** October 6 2026 (a Tuesday), **4:54 – 5:41 AM Eastern**, from the `**Date:**` header line. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel.

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/anton-seregin.md|Anton Seregin]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"; joined briefly at the start), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), Daniil Stauskiy (no page), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"). Val was not present.

**Purpose.** Round-the-table status. Pavel gave Kharetski the urgent RIS work for Georgia; the team also talked about the critical-error text, removing MudaGoose from the code, prose and contracts in the repositories, work already built without requirements, and Jira statuses.

## Where the substance lives

- [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] — CAP-252, 255, 246, 254 to Kharetski first; Georgia only; the 1.14 line; the carousel dropped.
- [[wiki/decisions/2026-10-05-ris-improvement-mvp1-is-five-jira-capabilities-in-one-release-due-october-19.md]] — Oct-6 update.
- [[wiki/decisions/2026-10-05-the-critical-error-screen-shows-the-cause-and-fix-in-words-and-keeps-the-qr-code-in-mvp1.md]] — Oct-6 update: plain words a technician understands; Ivan first checks that the error still repeats.
- [[wiki/decisions/2026-10-06-mudagoose-is-removed-from-the-code-entirely-and-git-history-is-the-way-back.md]] — Chudinov removes MudaGoose fully.
- [[wiki/decisions/2026-09-09-jvl-supports-both-dual-sas-and-single-sas-and-not-mudagoose.md]] — Oct-6 update.
- [[wiki/decisions/2026-10-06-built-capabilities-without-requirements-get-a-review-session-and-the-developer-adds-missing-texts-for-andrei-to-approve.md]] — Irina's question and the answer.
- [[wiki/decisions/2026-09-04-data-contracts-closed-every-repository-by-september-11.md]] — Oct-6 update: prose coverage 46% → 87%, the front-end contract.
- [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]] — Oct-6 update: the warning triangle and the status flow stay.
- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 6) — the RIS branch and the three battery cases.
- People: [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/igor-metelski.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/anton-leshkevich.md]] (in absentia)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide grep for both filenames, "October-6-2026", "2026-10-06", "мутагусь", "PORT-82" and "FIX-135" found no page citing either file and no other Oct-6 stub. The previous stand-up is [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct 5]].
- **§4 name calls.** "Саша" = Biratka (he answers). "Алексей" = Khamin. "Антон" called on = Seregin (he answers). "Даниил" = Daniil Stauskiy. "Зима"/"дима" called on after Daniil = Chudinov (he answers). "Женя" = Kharetski. "Игорь" = Metelski (speaker label). "Ира" = Irina. "Иван" = Ivan. "Сергей" = Tsymanov. "дима" called on last = Kovalchuk (he answers). "Андрей" at the start (the branch report) = Bosik (speaker label). "Антон вишкевич" (the daemon change for the emulator) = [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] by his recorded alias "Vishkevich". "Андрей" who sent the text map and approves texts (Vladimir's test 69) — **not resolved**; queued. "Лиза" (the carousel) — **not resolved**; queued. "дима апдейт делал" (Tsymanov's terminal update) — the notes say Dzmitry (Chudinov); kept as the notes' reading. "с Антоном ефимовскую" (Metelski's maths) — the notes read "Anton Efimovsky's math"; **unclear**, not resolved. "вал" / "Овал" = Val.
- **Where the notes and the transcript differ** [[raw/Meeting_Notes_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]:
  1. The notes call it a "Tuesday standup" — Oct 6 2026 was a Tuesday; correct.
  2. Kharetski's closed work: the notes say "SAS log tests"; the transcript says "тестами для сиситолока" — elsewhere in the corpus "сиси толк" is read as CC Talk. **Unclear**; kept as spoken.
  3. Igor's "NOVA 2" and "NOVA center" are the notes' readings of "над 2" and "надо центр". Kept as the notes' readings.
  4. The third battery case: the transcript says "22 с половиной вольта" for a battery "которая у нас репортится как... проблемная"; the notes say "a low 'problem' voltage". The number is garbled; not recorded.
  5. The undertaking deadline "~Oct 16 (end of next week)" is the notes' date; Pavel said "2 недели даже наверное чуть меньше уже да до конца следующей".
- **§15.8:** clear. A joke about being fired if MudaGoose comes back is banter and is not recorded. Nobody's pay or personal matters are recorded. **§15 #9:** clear. CAP/PORT/FIT/FIX/FQ/FP numbers are Jira keys.

## Sources

- [[raw/Meeting_Notes_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
