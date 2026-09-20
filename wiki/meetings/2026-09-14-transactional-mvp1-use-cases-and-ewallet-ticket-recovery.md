---
type: meeting
title: Transactional MVP 1 — the use cases walked one by one, and recovering a ticket that never printed (Sept 14 2026, 8:01–9:03 AM)
date: 2026-09-14
aliases: [Transactional MVP1 CAPs REQs planning, Transactional MVP1 Use Cases and eWallet Ticket Recovery, MVP1 use case walkthrough, the Monday use-case call, Sept 14 8am transactional call]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Transactional MVP 1 — the use cases walked one by one, and recovering a ticket that never printed (Sept 14 2026)

**Date/time:** September 14 2026, 8:01 – 9:03 AM Eastern (~1 hour 2 minutes) — the recording header. **Series:** a Microsoft Teams session titled `Transactional MVP1: CAPs, REQs, planning`. **Language: Russian** — the raw transcript is kept in Russian; the derived notes are an English gloss [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

Organised by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]; attendees [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (speaker-labelled "Dzmitry Chudzinau"), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (speaker-labelled "Alexander Biratko") and [[wiki/people/andrey-bosik.md|Andrey Bosik]] (speaker-labelled "Andrei Bosik") [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**Purpose, in Klimovich's own words:** "цель митинга пройтись по MVP один сейчас. Я считаю, что MVP один полностью сформирован на уровне [кейпа]билети… Единственное, что нужно мне сегодня добавить. Это UIUX экраны, все эти тексты финальные" — walk MVP 1 end to end; he considers it fully formed at capability level, with only the UI/UX screens and final texts still to add. He had collected the use cases on a separate Confluence page, "очень высокоуровневые, но достаточно, чтобы нам понять, что вот то, что мы хотим увидеть и уметь делать в MVP один." A second agenda item was how builds get delivered [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**Three back-to-back Val recordings that morning, three separate events (§12).** Val recorded five sessions on Sept 14; this is the **8:01** one. It is NOT the 6:38 [[wiki/meetings/2026-09-14-texas-vertical-conversion-and-georgia-game-base.md|Rage-Nova conversion call]] nor the 7:37 [[wiki/meetings/2026-09-14-code-standards-main-branch-rule-and-alekseev-coaching.md|code-standards call]] — different organisers, attendee sets and subjects, each with its own recording. It is also a separate event from the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept 11 8:04 AM capability-priorities call]], which it repeatedly refers back to ("в ходе прошлого… созвона в понедельник"). Each event carries its own stub.

Substance lives on:

- [[wiki/decisions/2026-09-14-nobody-downloads-and-installs-builds-thirty-day-target.md]]
- [[wiki/decisions/2026-09-14-ewallet-ttl-defaults-to-thirty-days-and-is-set-per-location.md]]
- [[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]]
- [[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]]
- [[wiki/decisions/2026-09-14-one-report-must-make-mvp1-cards-issued-for-a-georgia-lottery-inspection.md]]
- [[wiki/decisions/2026-09-14-capabilities-are-written-against-the-published-sas-standard.md]]
- [[wiki/decisions/2026-09-14-nothing-in-mvp1-may-still-be-proposed-and-bosik-writes-the-exception-report.md]]
- [[wiki/decisions/2026-09-11-one-card-at-a-thousand-dollars-and-the-rest-stays-on-the-ticket.md]] — extended here with the redemption floor
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] — the product thread and its dated timeline
- [[wiki/people/andrei-klimovich.md]] · [[wiki/people/val-levitan.md]] · [[wiki/people/pavel.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/andrey-bosik.md]]
- [[wiki/organizations/incom.md]] — daily caps, velocity and the error library
- [[wiki/organizations/georgia-lottery-corporation.md]] — the inspection scenario that forced the one MVP 1 report

**On the transcript.** Teams garbles nearly every English product and technical term spoken inside Russian speech. Readings used on the pages above, all near-certain from context: "MVP один / VP один / BMWP один / мвпи один / MUP один / NBP / IVP один" = MVP 1; "и волят / иволит / уволит / его лет / вольт" = e-wallet; "Кэрри / karier / Керри" = carrier (the printed ticket); "тикет / стикет / cicket / secet" = ticket; "флекспорт / флегспорт / фекспорт" = Flex-Port; "IQ / айкью / ikeunter" = Flex IQ; "флекспей / lpем / лексп" = FlexPay; "ИНКОМ / инкома / инкомовская" = InComm; "рекламент / реклармент / ириквайменс" = requirement; "капбилити / кейпобилети / копеллити / беллиси / экобилети" = capability; "юскейс / дискейсов / yсам" = use case; "рыденшн / рыбшн / reedamtion" = redemption; "ресит / рисито / resit" = receipt; "репринт / repsint" = reprint; "лиишью / лишь / регишь / Russia" = reissue; "анклейм / анкл то" = unclaimed; "тилт / телтов" = tilt (printer fault code); "дейли кап / day cap" = daily cap; "велосиси" = velocity; "плейбл / дима был" = playable / deposited balance; "мутагуз / мутэнта / мотобус / смыф" = MudaGoose; "дашборт / даш борт / дажбо" = dashboard; "клод" = Claude; "лакейшн блок инфорс" = location block enforce; "терминал лиз энд ремоут дизэйбл" = terminal lease and remote disable; "сас / sass / с. А. стандарт" = SAS; "AFT / IFT / по FT" = AFT (SAS funds transfer); "j паблош stander / j li stendart / часы gamy Stand red surgi" = the Gaming Standards Association and its published standard; "пропост / прополз / Полоз" = Proposed (Jira status); "эксептенс / аксептон скрейтинг" = Accepted / acceptance criteria; "инпрогресс / инфограз" = In Progress; "фетрус / фьючерс / печи бранч" = features / feature branch; "схедюл / скетживать" = schedule; "жени харецкому" = Evgeny Kharetski; "ковальчуку" = Kovalchuk. The raw files are preserved unchanged.

**MudaGoose spelling.** The derived notes render the existing product as "Moutagouz" and flag the name as a guess from the audio. The transcript's own renderings are "мутагуз / мутэнта / мотобус"; the corpus records this product as **MudaGoose**, so that is the form used in the wiki's own voice and "Moutagouz" survives only as a notes-side garble [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**§15.8:** clear — product design, Jira process and market/standards knowledge only. No named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
