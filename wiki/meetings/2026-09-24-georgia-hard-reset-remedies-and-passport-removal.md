---
type: meeting
title: Hard reset issues in Georgia — the engineers review Felipe's cases, plan to switch off the Passport check for Georgia builds, and propose restoring the last RIS (Sept 24 2026, 5:41–6:26 AM)
date: 2026-09-24
aliases: [Hard reset Issues in Georgia, Georgia Hard Reset Remedies and Passport Removal, Sept 24 hard reset review, three kinds of factory reset, restore the last RIS, disable the passport check for Georgia builds]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Hard reset issues in Georgia (Sept 24 2026, 5:41 AM)

**Date/time:** September 24 2026, **5:41 – 6:26 AM Eastern**, from the `**Date:**` header line; about 45 minutes. The Teams recording line inside the transcript reads "9:41AM" — that is the UTC time (the recording name ends `094139UTC`), not the Eastern time. Teams title "Hard reset Issues in Georgia". **Language: Russian** [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (ran it), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] (called "Женя"), [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"). Val was not on the call; Irina said during it that Val was messaging to talk about "новый Galaxy" and that she would tell him they were in a meeting [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]].

**Purpose.** Pavel's case-by-case pass over [[wiki/people/felipe-miranda.md|Felipe]]'s list of Georgia hard-reset complaints (a PDF attached to the meeting), sorting quick fixes from medium-term work. It is the review Pavel promised on Sept 23, done before the 7:02 AM follow-up with Val [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]].

## Where the substance lives

- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Sept 24, 5:41 AM) — each case and the answer given; the three kinds of factory reset; the stored history of every RIS; leases on sold machines; the critical-error screen.
- [[wiki/decisions/2026-09-24-engineering-plans-to-switch-off-the-passport-check-for-georgia-builds.md]] — Pavel's plan, the server flag it needs, and the near-term / medium-term split.
- [[wiki/decisions/2026-09-11-the-passport-is-preserved-and-jvl-is-using-the-bindings-wrongly-in-this-market.md]] — Sept-24 update (the plan sits against this ruling).
- [[wiki/projects/georgia-market-rollout.md]] (Sept 24, 5:41 AM) — most Georgia machines are bought outright; most locations have no network.
- People: [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/ivan.md]] · [[wiki/people/felipe-miranda.md]]

## Notes on the sources

- **§12 — one meeting, two files.** The notes and the transcript share date, time and title and link each other. A corpus-wide grep ("Hard reset Issues", "Georgia_Hard_Reset", "restore the last RIS", "Ivan Shpak" on Sept 24) found no other stub for it. The .docx original is already ledgered in [[wiki/skipped.md]]. It is a different event from the [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|4:46 AM stand-up]] (different content) and from the [[wiki/meetings/2026-09-24-ris-serial-binding-and-factory-reset-focus.md|7:02 AM follow-up with Val]] (different attendees). New meeting.
- **§4 name calls.** "Женя" = [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] by speaker label (LGS/Omni back end fits). "Филипп/Филиппа" = [[wiki/people/felipe-miranda.md|Felipe Miranda]]. "Паша" = Pavel. "хуан", who had also asked for a soft reset, is probably [[wiki/people/juan-martinez.md|Juan Martinez]] (**inference**, from his Feb-2026 RIS override requests; not asserted). "Борис", in Irina's line "Я пишу, что у нас локальный митинг, Борис", is **not resolved** (possibly a garble).
- **Notes vs transcript — the wiki follows the transcript** ([[raw/Meeting_Notes_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]):
  1. **The lease-user question.** The notes say Ivan's idea (hand out the web lease user) was answered "no, internal only". In the transcript the "only for our internal use" words sit inside Ivan's own turn, and the replies are Pavel "Можно." and Irina "Да." Who rejected what is **unclear**.
  2. **The printer/TITO request "goes into NOVA".** The notes state it as Evgeny's decision. The transcript has "поэтому мы его внова реализуем" — this can be "в NOVA" or "вновь/заново" (anew). Pavel had just said "не знаю, это для рейдж или для нова". The NOVA reading is **possible, not certain**.
  3. **"A bit cheeky."** The notes give the word to Evgeny. Pavel said it first ("начинают наглеть"); Evgeny repeated it: "как ты сказал, типа немножко наглый".
  4. **Omitted by the notes:** Pavel's remark that the soft-reset request had come before, "не только из джорджии. Это ещё хуан спрашивал".
- **§15.8 — withheld.** Mid-meeting Pavel took a short personal phone call about a family and legal matter. It is not recorded anywhere in the wiki. Nothing else touches pay or personal judgement.
- **§15 #8 / #9.** Ivan named an internal web account used to scan leases. The name is **not recorded** (it may be a credential). No corporate identifier appears.

## Sources

- [[raw/Meeting_Notes_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]
- [[raw/Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026.md]]
