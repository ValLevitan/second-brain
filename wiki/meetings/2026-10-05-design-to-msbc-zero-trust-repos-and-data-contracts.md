---
type: meeting
title: Val and Genadi — the developer repo model (zero trust, data contracts) applied to the BOM; GitHub keeps a flat list; Genadi's doubts; the work goes to Nathan (Oct 5 2026, 1:19–1:53 PM)
date: 2026-10-05
aliases: [Design-to-MSBC_Organization_repositories_, Design to MSBC Zero Trust Repos and Data Contracts, Oct 5 Genadi BOM meeting, zero trust repos, data contracts for hardware]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Val and Genadi — zero-trust repos and data contracts for the BOM (Oct 5 2026, 1:19 PM)

**Date/time:** October 5 2026, **1:19 – 1:53 PM Eastern**, from the `**Date:**` header line. Teams title "Design-to-MSBC_Organization_repositories_", organized by Val. **Language:** English at first, then Russian; per the notes, roughly minutes 8 to 21 are badly garbled (Russian rendered as English) and are not summarized [[raw/Meeting_Notes_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]].

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/genadi-peari.md|Genadi Peari]].

**Purpose.** Val explained how code repos work for developers — one Jira project per repo, zero trust, prose, ADRs and a data contract — so Genadi could see the same model for the bill of materials. Genadi asked why a BOM already in MSBC must be regenerated, doubted the plan against today's problems, and asked for simpler steps. Val handed the build to Nathan Carver, to be shown on the Flex Pay Slim.

**§12 — one meeting, two files; separate from the 1:58 PM call.** The notes and transcript share title, date and time and link each other. A corpus-wide search for both filenames, "Zero_Trust_Repos", "Design-to-MSBC" and "October 5" + "1:19 PM" found no page citing them and no other stub in this slot. The [[wiki/meetings/2026-10-05-nathan-carver-flex-pay-slim-bom-reverse-spike.md|1:58 PM call with Nathan]] five minutes later is a **separate meeting**: a different recording and title, a different counterpart (Nathan, not Genadi), and this meeting ends with Val saying he will call Nathan "сейчас". It continues the [[wiki/meetings/2026-09-30-github-to-msbc-bom-flat-list-bridge.md|Sept 30]] and [[wiki/meetings/2026-10-01-genadi-io-board-chips-flat-bom-pilot-and-street-cabinet-panel.md|Oct 1]] meetings on the same thread. New meeting.

Substance lives on:

- [[wiki/decisions/2026-10-05-hardware-follows-the-developer-repo-model-one-jira-project-one-repo-zero-trust-data-contracts-no-monorepo.md]] — the model, "70% sure" for hardware, flat list not a BOM, the ISO-in-Azure comparison, Genadi's reaction
- [[wiki/decisions/2026-10-05-nathan-carver-runs-the-flex-pay-slim-bom-reverse-spike-and-flex-port-follows.md]] — the hand-over to Nathan, and Genadi's condition: the flat list built right first
- [[wiki/decisions/2026-09-23-the-bom-source-of-truth-is-the-latest-design-in-github-and-sync-runs-one-way.md]] (Oct-5 update) — the thread sequencer
- [[wiki/people/mikhail-perelman.md]] (Oct 5, in absentia) — "У миши до сих пор нету репорта"; the 57-versus-65 monitor count
- [[wiki/topics/ai-assisted-development.md]] (Oct 5) — the AI COO persona and "90% of companies do not talk about this"
- People: [[wiki/people/genadi-peari.md]] · [[wiki/people/val-levitan.md]] · [[wiki/people/nathan-carver.md]] (in absentia)

**§4 name calls:**

- "миша" / "Мишина проблема" = [[wiki/people/mikhail-perelman.md|Mikhail Perelman]], **by context** (procurement reports, the BOM and stock count; the notes name him in full) [[raw/Meeting_Notes_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]].
- "Нейтан" = [[wiki/people/nathan-carver.md|Nathan Carver]] (the notes name him; the next call is with him).
- "Андрей деспотии чек сам" (who gives the build checksum) is read as [[wiki/people/andrey-bosik.md|Andrey Bosik]], DevOps, **by context** — inference; the line is garbled.
- "лёвы" (one possible cause of Mikhail's problem) = [[wiki/people/lev-rudky.md|Lev Rudky]], **by context** (inventory and BC loads) — inference.
- "Она посчитала 57" — the person who counted is not named. "Dr. Vosto", "Полина" and the garbled English stretch (8–21 min) are not read as people.

**Where the notes and the transcript diverge** (transcript followed): (1) the notes say the code side "has 12 people while Genadi works alone"; the transcript line is garbled ("Ты был управки, работает 12 человек. А вы работаете один?") — kept as the notes' reading. (2) the notes' "AI COO persona" is a reading of "завожу себе co о… эта персона будет толкать человека на спад чек недельный" — kept as the notes' reading. (3) the notes omit Val's "I haven't tried it yet" and the checksum exchange.

**§15.8:** Val's evaluative words about Mikhail's stance ("становится в позу" and a sharper line after it) are held; the substance — Mikhail has no report, and Val says it is a parallel problem — is recorded. Nobody's pay or performance rating is recorded. **Personal matters not recorded** (none met). **§15 #9:** clear.

## Sources
- [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]
- [[raw/Meeting_Notes_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]
