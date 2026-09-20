---
type: meeting
title: Transactional MVP 1 — clearing the open questions out of the requirements, and the ruling that a location keeps working when the internet does not (Sept 16 2026, 8:01–9:37 AM)
date: 2026-09-16
aliases: [Transactional MVP1 CAPs REQs UI/UX, Transactional MVP1 Open Questions and Offline Operation, the offline operation call, Sept 16 8am transactional call, the open-questions cleanup call, day three of the MVP1 series]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Transactional MVP 1 — open questions and offline operation (Sept 16 2026)

**Date/time:** September 16 2026, 8:01 – 9:37 AM Eastern (~1 hour 36 minutes) — the recording header. **Series:** the Microsoft Teams session titled `Transactional MVP1: CAPs, REQs, UI/UX`, third consecutive morning. **Language: Russian** — the raw transcript is kept in Russian; the derived notes are an English gloss [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Organised by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]; attendees [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (speaker-labelled "Dzmitry Chudzinau"), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (speaker-labelled "Alexander Biratko") and [[wiki/people/andrey-bosik.md|Andrey Bosik]] (speaker-labelled "Andrei Bosik") — the same seven people as the two preceding mornings [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Purpose.** Irina had tried to start on the non-functional requirements and hit a wall: about half of the MVP 1 requirements contain an unanswered open question, and the moment the AI assistant is asked to work with one, the open question comes straight back. The meeting walked her list requirement by requirement and did one of three things with each — answer the question, move the requirement to MVP 2, or delete it. The offline-operation argument grew out of one of those items and took roughly a third of the call [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**A derived-document family, not two meetings (§12).** The notes and the transcript are the same 8:01 AM session; the notes' own header carries the same date, time and duration and links the transcript. One stub, both cited. **September 16 2026 is an eight-recording day** in `raw/` (8:01, plus seven other sessions with different participants and subjects); a corpus-wide comparison against the Sept-14 and Sept-15 sessions in this same series confirms this is a distinct third meeting, not a re-transcription of either.

Substance lives on:

- [[wiki/decisions/2026-09-16-a-location-keeps-working-without-internet-and-only-the-card-stops.md]] — the meeting's titular ruling, and Val reversing the engineering position outright
- [[wiki/decisions/2026-09-16-anything-that-depends-on-the-cloud-leaves-mvp1.md]] — "be honest with yourselves", applied down the whole list
- [[wiki/decisions/2026-09-16-fifteen-flex-ports-in-mvp1-and-the-system-designed-for-ninety-nine.md]]
- [[wiki/decisions/2026-09-16-the-mvp1-timing-numbers-two-hundred-milliseconds-and-thirty-seconds.md]]
- [[wiki/decisions/2026-09-16-incomm-returns-no-daily-cap-error-so-the-call-comes-to-jvl-first.md]]
- [[wiki/decisions/2026-09-16-there-is-no-cash-on-flexpay-in-any-form.md]]
- [[wiki/decisions/2026-09-16-a-kiosk-is-de-enrolled-from-a-location-never-from-the-cloud-database.md]]
- [[wiki/decisions/2026-09-16-a-self-service-ticket-is-collected-at-the-service-kiosk-with-a-four-digit-pin.md]] — an MVP 2 direction stated here
- [[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]] — the MVP 2 cloud capability now exists; see the Sept-16 update
- [[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]] — what is blocking the non-functional-requirements work
- [[wiki/decisions/2026-09-11-lease-blocking-reaches-the-flex-ports-and-is-never-automatic.md]] — lease blocking and internet loss separated here
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] — the product thread and its dated timeline
- [[wiki/people/andrei-klimovich.md]] · [[wiki/people/val-levitan.md]] · [[wiki/people/pavel.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/andrey-bosik.md]]
- [[wiki/organizations/incom.md]] — the daily cap and velocity limits, and the error InComm does not return

**§4 name resolution on this recording — the high-risk case, again.** Two men named Andrei were in the room: **[[wiki/people/andrei-klimovich.md|Andrei Klimovich]]** (organiser, transactional product owner, sharing his screen and editing the requirements live throughout) and **[[wiki/people/andrey-bosik.md|Andrey Bosik]]** (DevOps). Every bare "Андрей" was resolved by context, and in two places by the answering voice:

- Val's "Андрей я[,] Андрей[,] простите… как вы ведете митинг", "Андрюша поехали", "Андрей климович, ваша задача толкать митинг" and "Андрей клим[о]вич, заводите ваши факторы" → **Klimovich** (Val twice uses the surname) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- Chudinov's "я планирую доработать эти критерии, исходя из Того, что мы сейчас с Андреем получаем" (capability 122, the requirements work he is doing jointly) → **Klimovich**, who answers in the next line [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- Chudinov's "Не поддержит тут ни Андрея никто" (rejecting Val's pre-generated-validation-ID idea on engineering grounds) → **Klimovich**, the product owner whose backing the idea would need [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- Chudinov's "Может Андрей бы подсказал цифёрку?" — asked about network round-trip timings — → **Bosik**, who is the voice that answers it ("она ж может зависеть от чего угодно… у самого провайдера может что[-]то быть [с] сетью") [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- Chudinov's closing "Андрей[,] помет[ь] еще одно требование… 14[ ]30… ты там говорил, что создашь [ка]п[а]бил[ити] под неё" → **Klimovich**, who replies "14[ ]30[,] хорошо[,] я гляну" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Bosik's own two substantive contributions on this recording are both network-side, which is the context signature that separates him: identifying the ambiguous "channel" in requirement 1379 as "в общем, внешний канал связи" (the external communication channel), and declining to give a timeout number because it depends on the provider's network [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Every "Дима"/"Дмитрий" on this recording is **[[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]** — the back-end/Java voice, answering on lease behaviour, local storage, InComm documentation and load testing; neither [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] (IT) nor [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]] (3D) was present. "Паша" = Pavel Frolov, "Ир[а]"/"Ирина" = Irina Shishko. No other short form required resolution, and nothing on this recording fit no known person.

**On the transcript.** Teams garbles nearly every English product and technical term spoken inside Russian speech, and the numbers are spoken rather than spelled. Readings used on the pages above, all near-certain from context: "MVP один / МВП один / эмби один / MBP / ВП один / ЮВИ П один / NVIP 2 / MIP 2 / эмпи пи 2" = MVP 1 / MVP 2; "к[а]побилити / копобилити / capoility / capaбилити / кобилити / повелитель" = capability; "рекламент / реклаймент / реквайменс / рекламу" = requirement; "иволит / его лет / волет / уволят / волят" = e-wallet; "тикет / стикет" = ticket; "флекс айкью / флексакью / айкью / IQ" = Flex IQ; "флекспей / flixpay / flaxpay / фелспей" = FlexPay; "флекспорт / флекс порты / экспорты / лекс порт" = Flex-Port; "лиз / лиза / лис / лес" = lease; "инком / ИНКОМ / пинком" = InComm; "дейли кап / дели кап / del capp / dea cap" = daily cap; "велосити / велосисе / авилосит" = velocity; "клауд / клаузе / Клаус сервис" = cloud; "дэн ролд / дейн ролд / dand" = de-enrolled; "ресит / рисит" = receipt; "клод / Клода / Клауден" = Claude, the AI assistant the team writes requirements with; "опен квэщен / опен иттом / опыт найт" = open question / open item; "драфт / паблиш" = Draft / Published (Jira statuses); "хэнд[ ]сплэд / hend splead" = hand-paid; "сас / Sass" = SAS; "нагрузочное тестирование" = load testing; "фактор[е] ресет" = factory reset; "20 04:00" = 24 hours (Val's own list in the same breath is "06:00 или 12 или 24"). The raw files are preserved unchanged.

**Where the derived notes and the transcript diverge.** Three places, all minor, all flagged on the pages that carry them:

1. The notes say the team confirmed there is "no goal of cashing the same eWallet **at a different location**". Biratka's actual words are "в другом киоске" — at a different **kiosk**. The location-versus-kiosk distinction was never drawn sharply on the call, and Val's follow-on line ("оператор говорит про другое, он говорит, пойти на другой ещё") is too damaged to settle it [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
2. The notes present the 24-hour offline window as a working figure Val invited objections to. That is right, but they omit that **Val himself said it might be too long** in the same breath — "Я согласен, что [24 часа] может быть ту[ ]лон[г]" — and that the alternative the engineers wanted was the opposite direction: Klimovich proposed no limit at all and Pavel proposed "пока лиза не закончится" (until the lease expires) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
3. The notes do not record that requirement **1451**'s status was also taken off Published at Irina's instruction, alongside the deliberate decision to leave its open question in place ("Поменяй паблиш на…"); her following words are garbled and the target status is not recoverable [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Otherwise the notes track the transcript closely on this recording: no back-imported prior-day material, no speaker inversions, and no "ping" glossed into "confirmation" of the kind seen in earlier batches.

**§15.8:** clear — product requirements, timeouts, network behaviour and Jira process only. No named person's pay, rate, bonus or performance judgement appears in either source; nothing was excluded on that ground. The opening minute contains office banter (a joke about a salary and about who raised their hand) which is not durable knowledge and is not recorded. **§15.9:** no licence, registration, tax or account number appears in this material.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
