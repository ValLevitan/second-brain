---
type: meeting
title: Transactional MVP 1 — Elizabeth's SAS works after long work with Ivan (and Claude); first borrowed operator machines for October 15–16; re-used terminals wipe their secrets (red section in the instruction); a real production transaction before the first location; Klimovich back and in Georgia from Tuesday; InComm broker approval still pending; the Georgia show around Oct 21–22; the bootloader on new boards; collect money lost to a port crash goes to unclaimed in MVP 1 (Oct 9 2026, 8:01–8:25 AM)
date: 2026-10-09
aliases: [Transactional MVP1 sync Oct 9, Transactional MVP1 Test Machines and Unclaimed Funds, day sixteen of the MVP1 series, Oct 9 8am transactional call, borrowed machines October 15-16, wipe secrets press each letter 4 times, real transaction in production, InComm broker approval, Georgia show 21 22, Flex Pay Slim card dispenser show, bootloader on new boards, collect after port crash unclaimed]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Transactional MVP 1 — test machines and unclaimed funds (Oct 9 2026)

**Date/time:** October 9 2026 (a Friday), **8:01 – 8:25 AM Eastern** (about 24 minutes), from the `**Date:**` header line [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]. **Series:** the Teams session "Transactional MVP1 sync" — the **sixteenth** morning call, the next after [[wiki/meetings/2026-10-05-transactional-mvp1-port-screens-unclaimed-money-and-printer-models.md|Oct 5]] (day fifteen). **Language: Russian.** This is the Friday sync Klimovich promised on Oct 5.

**Who spoke** (speaker labels): [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (chair), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"), [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"). Val was not present.

**Purpose.** Where Georgia testing stands after Elizabeth's set-up, when machines can be borrowed from other makers, what Klimovich picks up on his return, and one money case: collect money lost to a port crash.

Substance lives on:

- [[wiki/decisions/2026-10-09-first-borrowed-operator-machines-are-arranged-for-october-15-16.md]] — Oct 15–16; "MVP 1 development is formally finished"; Irina's doubt
- [[wiki/decisions/2026-10-09-a-terminal-registered-before-must-wipe-its-secrets-and-the-install-instruction-says-so-in-red.md]] — the four-presses hack and the red section
- [[wiki/decisions/2026-10-09-all-web-services-go-to-production-before-the-weekend-instead-of-waiting-for-georgia.md]] — Chudinov deploys production over the weekend
- [[wiki/decisions/2026-10-09-a-real-transaction-is-run-in-production-on-the-new-version-before-the-first-real-location.md]] — Bosik's point, Klimovich's yes
- [[wiki/decisions/2026-09-24-a-flex-port-that-dies-holding-money-sends-it-to-unclaimed-and-one-without-a-gateway-goes-out-of-service.md]] — Oct-9 update: collect money after a port crash goes to unclaimed; auto-send to a known wallet is later
- [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] — Oct-9 update: Elizabeth's SAS works
- [[wiki/decisions/2026-09-04-north-america-modem-variant-and-ask-kore-for-the-apn.md]] — Oct-9 update: the KORE SIM payment is fixed; the Minsk SIM thread is revived
- [[wiki/organizations/incom.md]] (Oct 9) — still waiting for approval of JVL as broker
- [[wiki/projects/georgia-market-rollout.md]] (Oct 9) — the show around Oct 21–22; the SAS set-up; modems
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 9, 8:01 AM) — the day-sixteen entry: Klimovich's return, Flex Pay Slim for the show, the bootloader on new boards
- People: [[wiki/people/andrei-klimovich.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/ivan.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/elizabeth.md]] (in absentia) · [[wiki/people/felipe-miranda.md]] (in absentia, inference) · [[wiki/people/sebastian.md]] (in absentia) · [[wiki/people/genadi-peari.md]] (in absentia) · [[wiki/people/evgeniy-alekseev.md]] (in absentia, inference)

**§12 — one meeting, two files.** The notes and the transcript share date, time and title and link each other. A corpus-wide grep for both filenames, "Test_Machines_and_Unclaimed", "2026-10-09" and "Transactional MVP1 sync" found no page citing either file and no other Oct-9 MVP 1 stub. The same morning's [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|4:46 AM stand-up]] is a different meeting. It is a new meeting.

**§4 name calls.** "Дима" = Chudinov. "Паша" = Pavel. "Ваня" = Ivan (Irina corrects Pavel's "Лёша"). "Ира" / "Ирина" = Irina. "Саша" = Biratka. "Лёша", asked about the bootloader = Khamin (he answers). "Андрей" whose questions Klimovich re-pinged = Bosik by context (Bosik: "Я видел" — **inference**). "Филипп" = [[wiki/people/felipe-miranda.md|Felipe Miranda]] by context (**inference**). "себастьян" = [[wiki/people/sebastian.md|Sebastian]]. "Геннадий" = [[wiki/people/genadi-peari.md|Genadi Peari]]. "Клод" / "клуб" = Claude, the AI tool. "алексеевым", who made the firmware memory changes = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] by context (embedded firmware, the bootloader hand-over of Sept 29 — **inference**). "нейтона" — Nathan Carver's payment hub by earlier context (Sept 2: "сделано [Нейтоном]") — **inference, unclear**. "анклей" / "anclaint" / "анкэйм" = unclaimed. "мутагуз" — **unclear** (perhaps MudaGoose).

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]):

1. **How long Ivan worked.** The notes say "many hours". The transcript: "мы 15:00 боролись" — a garbled figure (perhaps 15 hours). Kept as "a long time".
2. **SIM cards and Minsk cards.** The notes list "SIM card payment fixed" and "ordering cards for Minsk" as two items. Klimovich's words run together: "по поводу симкарт коровских у нас там была проблема с оплатой вроде по фикселе… насчёт заказа карточек для Минска… мы уронили эту переписку. Я сегодня подниму". By the Oct-1 context the Minsk "cards" are KORE SIM cards — **inference**.
3. **Undertaking 2's date.** The notes give "Oct 9 or Oct 12". The transcript: "сегодня или в понедельник" — matches.

**§15.8:** clear — product and schedule only. Klimovich's travel is a work schedule fact. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
