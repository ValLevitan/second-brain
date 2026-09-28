---
type: meeting
title: Transactional MVP 1 — the Flex-Port and Flex IQ screens are walked, the no-paper rule is split by flow, and there is no feature lock yet (Sept 21 2026, 8:02–8:54 AM)
date: 2026-09-21
aliases: [Transactional MVP1 CAPs REQs UI/UX, MVP1 FlexPort and IQ UX Design, day six of the MVP1 series, the Monday gate call, Sept 21 8am transactional call, UI/UX walkthrough Sept 21]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Transactional MVP 1 — Flex-Port and Flex IQ UX design (Sept 21 2026)

**Date/time:** September 21 2026, **8:02 – 8:54 AM Eastern** (about 52 minutes) — the recording header [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. **Series:** the Teams session `Transactional MVP1: CAPs, REQs, UI/UX`, the **sixth** morning call (after Sept 14, 15, 16, 17, 18), held on the **Monday Sept 21 gate day** [[raw/Meeting_Notes_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. **Language: Russian.**

**Who.** [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (drove it on his own screen), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (speaker label "Dzmitry Chudzinau"), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik") and [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"; speaks twice) [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. **[[wiki/people/val-levitan.md|Val Levitan]] has no speaker turn** and is not on the attendee list [[raw/Meeting_Notes_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]].

**Purpose.** Klimovich walked the finished UI/UX design for the Flex-Port and Flex IQ screens. He said the functional side is fixed and only small design edits remain; after the call he would load it into Jira [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript carry the same date, time and title and link each other. A corpus-wide check found no other Sept-21 stub and no earlier source for this session. The capability numbers (229; requirements 1514/1515/1516/1543), the no-paper argument and the screen walk are new here, so this is a distinct sixth session, not a re-transcription of Sept 14–18.

Substance lives on:

- [[wiki/decisions/2026-09-21-at-the-counter-no-printer-no-wallet-at-the-port-the-wallet-goes-to-unclaimed.md]] — the no-paper rule, split by flow
- [[wiki/decisions/2026-09-15-the-flex-iq-cashier-flow-login-redemption-receipts-and-records.md]] — the Flex IQ screens (Sept-21 update)
- [[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]] — the port rule, confirmed (Sept-21 update)
- [[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]] — the gate day itself: no feature lock yet
- [[wiki/decisions/2026-09-16-anything-that-depends-on-the-cloud-leaves-mvp1.md]] — capability 229 and the last cloud clean-up
- [[wiki/decisions/2026-09-17-jvl-supports-multiple-incomm-products-not-a-fixed-pair.md]] — the room still calls multi-product undecided
- [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]] — the window designs arrive
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] — the product thread and its dated timeline (Sept-21 entry)
- [[wiki/people/andrei-klimovich.md]] · [[wiki/people/pavel.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/felipe-miranda.md]]

**§4 name calls.** "Дима" / "Зима" = Chudinov (he answers each time; Klimovich also names "Дима" as the one who sent the InComm error list). "Паша" = Pavel. "Саша" = Biratka (he answers "Да, один"). "Андрей" addressed by Chudinov and Pavel = Klimovich (he answers). Andrey Bosik speaks only on the phone number and is not addressed by name. "Геннадий" = [[wiki/people/genadi-peari.md|Genadi Peari]] (screen sizes). "Филипп" = [[wiki/people/felipe-miranda.md|Felipe Miranda]] (alias on file). "Владимир" = [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] **by context only** — a React developer who tidied the Flex-IQ screens on Sept 11; no surname is spoken [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]].

**Where the notes and the transcript diverge** (transcript followed):

1. **Asset number.** The notes give Pavel the fact that the asset number is "one per machine regardless of how many SAS ports". In the transcript Pavel asks it as a question ("Саша ты помнишь асад намбер он же один на машину да") and **Biratka** answers "Да, один". Biratka also adds a condition the notes drop: "Но если она работает с AFT и принтером, то да." Pavel's claim that the lottery operator assigns it centrally was hedged: "Похоже", and "это я могу пофантазировать. Я не уверен в этом."
2. **"Gell".** The notes print a support contact "Gell". The transcript has "контакты gell и контакты инкома". The word is unclear. Reading it as "JVL" is an **inference only**.
3. **Features.** The notes say features cannot be created yet. In the transcript Irina first says features already exist ("на эту логику уже фичи есть"); Klimovich says probably not, he must load Jira first; Pavel says the capabilities exist and only need the right features under them. Klimovich's plan — one container capability for IQ and one for the port, with the rest carried by the HTML mock-up — is missing from the notes.
4. **Omitted:** the logout and inactivity-timer exchange; the comparison with MudaGoose machine lists; Pavel's alternative of showing tilts only on start screens; Pavel's "10 seconds then back to idle" for the technician QR menu.

**§15.8:** clear — screen design, device logic and Jira process only; no pay, rate or personal judgement appears. **§15 #9:** asset numbers, serial numbers, IP addresses and card codes are discussed only as fields; no value is spoken. The screen size 854 x 480 is a display spec, not an identifier.

## Sources
- [[raw/Meeting_Notes_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
