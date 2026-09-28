---
type: meeting
title: The hardware repo as the BOM's source of truth, the street-cabinet layout, and a FlexPort enclosure (Sept 24 2026, 4:38 PM)
date: 2026-09-24
aliases: [Alignment on mechanical drawings repo and street machines design, Hardware Repo BOM Source of Truth, Street Machine Cabinet Layout and FlexPort Enclosure, Val and Genadi alignment Sept 24, BOM in BC automatically from GitHub, test BOM on the new Slim, floating FlexPort]
source-count: 4
open-commitments: 0
open-questions: 0
---

# The hardware repo as the BOM's source of truth, the street-cabinet layout, and a FlexPort enclosure (Sept 24 2026)

**Date/time:** September 24 2026, **4:38 PM – 5:37 PM Eastern**, recorded in two segments: **4:38–5:20 PM** ("Segment 1 of 2") [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]] and **5:20–5:37 PM** ("Segment 2 of 2") [[raw/Meeting_Transcript_Street_Machine_Cabinet_Layout_and_FlexPort_Enclosure-September-24-2026.md]] (both from the `**Date:**` header lines). Teams title *Alignment on mechanical drawings repo and street machines design*. Language: English for the first few minutes, then **Russian** [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]].

**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/genadi-peari.md|Genadi Peari]]. Genadi asked whether [[wiki/people/nathan-carver.md|Nathan]] was joining; Val: "No, Nathan is not joining." [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]

**Purpose:** the follow-up to Sept 23 on where the bill of materials lives (Val's written note on GitHub and MSBC), then the street-cabinet agenda item — the TransAct TITO product, LTE/5G modems, the cabinet layout — and a reminder about a FlexPort enclosure revision [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]] [[raw/Meeting_Transcript_Street_Machine_Cabinet_Layout_and_FlexPort_Enclosure-September-24-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-09-23-the-bom-source-of-truth-is-the-latest-design-in-github-and-sync-runs-one-way.md]] (Sept-24 update) — Val reads out his written rule; the BOM is built in BC automatically from GitHub data; research and a test BOM on the new Slim.
- [[wiki/topics/business-central-erp-implementation.md]] and [[wiki/topics/github-release-management-pipeline.md]] (Sept 24, 4:38 PM) — the same thread against the Aug-12 design.
- [[wiki/decisions/2026-09-23-jvl-stops-building-its-own-tito-desktop-box-and-uses-jcm-or-transact-for-now.md]] (Sept-24 update) — Genadi's TransAct meeting and a standard DB9 serial connector.
- [[wiki/decisions/2026-09-04-north-america-modem-variant-and-ask-kore-for-the-apn.md]] (Sept-24 update) — LTE modules hard to buy, 5G quoted, a firmware-update USB stick.
- [[wiki/topics/low-cost-street-machine.md]] (Sept 24) — the cabinet layout: scanner, port panel, video deck, play panel, printer and bill acceptor.
- [[wiki/decisions/2026-09-16-street-machine-electronics-move-to-eye-level-and-the-monitor-opens-like-a-cupboard-door.md]] (Sept-24 update) — Genadi's pull-out shelf and hanging TV; Val "can be persuaded".
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 24, 4:38 PM) — the enclosed, "floating" FlexPort on posts.
- People: [[wiki/people/genadi-peari.md]], [[wiki/people/igor-starovoytov.md]], [[wiki/people/mikhail-perelman.md]], [[wiki/people/pavel.md]], [[wiki/people/nathan-carver.md]].

## Notes on the sources

- **One meeting, not two (§12 finding).** The two recordings share one Teams title and one pair of attendees, and their times touch at 5:20 PM. Segment 1 ends mid-sentence in the street-cabinet item, with Genadi on modems ("Короче я, я просто сегодня уже."); Segment 2 opens mid-conversation in the same item ("Спереди… То есть монитор будет приподнят"). Genadi's line in Segment 1 that he must deal with the Chinese suppliers again tonight ("сегодня опять чтото разбираться с китайцами") matches his closing line in Segment 2 ("мне ещё ночью надо в Китай посидеть"). One stub, four sources. A few words may be lost at the seam. [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]] [[raw/Meeting_Transcript_Street_Machine_Cabinet_Layout_and_FlexPort_Enclosure-September-24-2026.md]]
- **Corpus-wide check:** no wiki page cited any of the four files, and no stub carried this meeting (grepped the wiki for "September-24-2026", "Hardware_Repo_BOM", "Street_Machine_Cabinet_Layout", "test BOM", "Slim" + "BOM", "FlexPort" + "posts"). The Sept-24 same-day stubs are different meetings (other attendees and subjects). It is a different event from the [[wiki/meetings/2026-09-23-texas-flex-slim-release-street-cabinet-and-bom-source-of-truth.md|Sept 23 alignment call]], which it continues, and from the [[wiki/meetings/2026-08-12-hardware-github-standard-bc-sync-design.md|Aug 12 design session]].
- **Notes vs transcript — the wiki follows the transcript:**
  - The notes say "**the street machine** gets a standard DB9 serial connector for the Transact printer." In the transcript the question is how TransAct's product talks "с нашим IQ", and Genadi's DB9 idea is tied to the Mudagoose connection ("если у нас мутогуз исчезла, я бы у нас поставил бы обычный дебинайн стандартный сериальный коннектор"). The street machine is not named. The wiki records a JVL-side DB9, device not stated (IQ by context — inference). [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]] [[raw/Meeting_Notes_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
  - The notes say RS-232 with "three wires". The transcript renders it "Обычная расти сортир 33 проволочки". The wiki keeps "ordinary serial (RS-232, as the notes read it)" and does not state a wire count. [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
  - The notes say Misha bought "about 8–10" LTE modules. The transcript is "миша там 10 чтото там купил длина 8 там" — unclear; no count is recorded. [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
  - The notes put the scanner "about 10 cm **from the player**". The transcript says the scanner must be 10 cm higher ("Сканер должен выше его быть на 10 см"); the player is not mentioned. [[raw/Meeting_Transcript_Street_Machine_Cabinet_Layout_and_FlexPort_Enclosure-September-24-2026.md]]
  - The notes write the competitor as "Lighting Wonder". The transcript says "Лайтон вондер"; read as **Light & Wonder**, the competitor named elsewhere in the wiki (inference).
  - The notes say the FlexPort tubes are moulded into the cover "with four holes". In the transcript the four holes are in the machines' own panels ("4 дырочки у них панели, они прикрутились той стороны"), and Genadi speaks of two tubes. [[raw/Meeting_Transcript_Street_Machine_Cabinet_Layout_and_FlexPort_Enclosure-September-24-2026.md]]
  - The notes leave out two things the transcript has: Val's line that his note says "each module gets one plain text file", and Genadi's question about Val's AI agent, which Val waved off ("Забудьте моего агента… считайте, что я руками это делаю"). [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
  - The notes say Igor's surname was not given. The wiki reads him as [[wiki/people/igor-starovoytov.md|Igor Starovoytov]] by the cabinet-design context, as on Sept 23 (inference).
- **Names (§4):** "Mikhail" (a user of Genadi's part-number Excel, and one of the people who can mark a new revision) and "Misha" (who bought LTE modules) are read as [[wiki/people/mikhail-perelman.md|Mikhail Perelman]] by the procurement/parts context (inference). "Lev" is read as [[wiki/people/lev-rudky.md|Lev Rudky]] and "Felipe" as [[wiki/people/felipe-miranda.md|Felipe Miranda]] (inference). "Павел" is [[wiki/people/pavel.md|Pavel Frolov]]. A name rendered "Элизабет" sits in a garbled passage about flagging a revision; it may be [[wiki/people/elizabeth.md|Elizabeth Palomino]] (parts), but it is **not matched** and not added to her page. The strings "Giorgi", "Mandy" and "андрейкин" in Val's lines are read as garble, not people.
- **§15.8:** Val's remarks that Genadi had not read his note, and a remark about Igor's working style, are personal judgements and are **withheld**. Module, deck and build-cost prices are company economics and are recorded.
- **§15 #9:** clear — no corporate identifiers. "V43" is a product configuration code Genadi used as an example.

## Sources

- [[raw/Meeting_Transcript_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- [[raw/Meeting_Notes_Hardware_Repo_BOM_Source_of_Truth-September-24-2026.md]]
- [[raw/Meeting_Transcript_Street_Machine_Cabinet_Layout_and_FlexPort_Enclosure-September-24-2026.md]]
- [[raw/Meeting_Notes_Street_Machine_Cabinet_Layout_and_FlexPort_Enclosure-September-24-2026.md]]
