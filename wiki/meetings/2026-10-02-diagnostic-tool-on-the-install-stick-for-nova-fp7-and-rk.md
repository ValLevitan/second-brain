---
type: meeting
title: EGMs diagnostic tool for NOVA / FP-7 — Pavel's idea to put the diagnostic tool on the installation USB stick and keep it in the SDK repository, Genadi's security question, Val's modem question from the chat, and "both variants, RK and FP-7" (Oct 2 2026, 9:01–9:15 AM)
date: 2026-10-02
aliases: [EGMs diagnostic tool - NOVA-FP-7, Diagnostic Tool on Install Stick NOVA FP7 and RK, diagnostic tool on the install stick, диагностик тул на флешке, диагностик тул вместе с SDK, Oct 2 diagnostic tool call 9:01, sell mode modem question, RK is step 2, оба варианта и RK и FP-7]
source-count: 2
open-commitments: 0
open-questions: 0
---

# "EGMs diagnostic tool — NOVA / FP-7": the diagnostic tool on the install stick (Oct 2 2026, 9:01 AM)

**Date/time:** October 2 2026 (a Friday), **9:01 – 9:15 AM Eastern** (about 14 minutes), from the `**Date:**` header line [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]. Teams title "EGMs diagnostic tool - NOVA-FP-7". **Language: Russian.**

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (presented) and [[wiki/people/genadi-peari.md|Genadi Peari]] [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]. [[wiki/people/val-levitan.md|Val]] was present but has no spoken lines; Pavel relays his questions from the chat — "Вал спрашивает, можем ли мы использовать sell mode?" and "Вал если ну вопросов да пишите, мы сразу же их. Запишем озвучим" [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]. The derived notes say the same: "Val Levitan present, asked questions in chat only" [[raw/Meeting_Notes_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]].

**Purpose.** Pavel put forward one idea for the new platform — "возникла идея, поскольку сейчас работаю над SD[K] для новой платформы… Нова. Фреймворк и новые материнские платы. По базе там икс 86" — put the diagnostic tool on the USB stick the software is always installed from, and keep it in the SDK repository so it stays current; took Genadi's security question and Val's modem question; and closed with "будем прорабатывать… оба варианта и RK и [FP-7]" [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. A corpus-wide grep for both filenames, "Diagnostic_Tool_on_Install_Stick", "EGMs diagnostic", "диагностик тул", "install stick" and "October-2-2026" found no page citing either file and no other stub for a 9:01 AM call on Oct 2. The same day's [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|4:50 AM stand-up]] and [[wiki/meetings/2026-10-02-ai-pm-status-listener-core-and-318-transcripts.md|7:32 AM AI PM status call]] are different meetings (other times, participants and content). The wiki knew an earlier "IP-688 diagnostic tool" from the Georgia freeze work ([[wiki/topics/egm-freezing-investigation.md]], Mar 2026) — that is the "текущем диагностик тул" Pavel refers to, not this meeting. It is a new meeting.

Substance lives on:

- [[wiki/decisions/2026-10-02-the-diagnostic-tool-goes-onto-the-installation-stick-and-lives-in-the-sdk-repository-both-rk-and-fp7-are-worked-out.md]] — the ruling: one stick for install and diagnostics, the tool kept in the SDK repository, read-only and so safe, modem use cases later, both the RK and the FP-7 variants worked out
- [[wiki/topics/nova-platform-architecture.md]] (Oct 2, 9:01 AM) — where the tool sits in the platform; the two products "for the record": RK (ARM, street machines) and FP-7 (x86, mainly casinos)
- [[wiki/topics/fp7-hardware-platform.md]] (Oct 2 2026) — FP-7 named as the x86 platform "в основном для казино"
- [[wiki/decisions/2026-09-29-the-amd-environment-is-rebuilt-from-the-rk3568-sdk-pavels-ten-day-spike-and-the-rk3576-waits.md]] — Oct-2 (9:01 AM) note: the SDK work Pavel is on, and "RK… степ 2"
- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 2, 9:01 AM) — the install errors "с непонятным описанием" that Felipe raised, which the tool is meant to answer
- People: [[wiki/people/pavel.md]] · [[wiki/people/genadi-peari.md]] · [[wiki/people/val-levitan.md]] (in the chat) · [[wiki/people/felipe-miranda.md]] (in absentia)

**§4 name calls** [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]:

- "Гена" = Genadi Peari (speaker label; he answers). "Вал" / "вал" = Val, in the chat. "Филиппа" / "от Филиппа" = [[wiki/people/felipe-miranda.md|Felipe Miranda]], **by context** (the install errors reported from the field — his RIS thread of Sept 23–28). "Андрея" ("может прийти из разных источников, в том числе от вас вал. Вот Андрея может быть от Филиппа") — **not resolved** between [[wiki/people/andrey-bosik.md|Bosik]] and [[wiki/people/andrei-klimovich.md|Klimovich]]; both could supply modem use cases; queued, not forced. "Владимира" ("Того же Владимира… чтобы график юзер интерфейс сделать") = [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], **by context** (the one Vladimir on the Minsk team; freed "после транзакшнл"). "Клодом" / "с клодом" = Claude, the AI tool.
- **Garbled words, with the reading used or none:** "ю с bстика" / "ю с б стик" = USB stick; "диагностик тул" / "диагностик тыл" = the diagnostic tool; "вас детей" = the SDK (reading); "прошивки Далласа" = a Dallas firmware section (as spoken; the notes read "Dallas firmware"); "айбор" = the IO board (reading); "билаксептер" = bill acceptor; "не переставляя с овца" — **unclear** (the notes read "without touching the software"); "**sell mode**" — most likely "cell modem" (Pavel's next sentences are about sending diagnostics "через модем"; **inference**); the notes keep "sell mode"; "серверную страну" = the server side (reading); "Это 2." — **unclear**; "консоренс" = concerns; "Модным да модным" / "через моды" = the modem (reading); "юск кейсы" = use cases; "за флай" = on the fly; "транзакшнл" = Transactional; "ф п с севен" / "ф п seven" / "paseven" = FP-7; "Фикс ремонт ли?" — **unclear** (an answer to something in the chat); "фу р к" / "RK bayst" = RK, RK-based; "Кардуя" — **unclear**; "Ники, в принципе, понятно" — **unclear** (an answer to the chat).
- **"RK" is not expanded on the call.** The RK-based ARM platform for street machines is, by the wiki's record, the RK3576 street-cabinet board ([[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]]) — **inference**; only "RK" and "арм платформе… для стрит машин" were spoken.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]):

1. **"Sell mode and modem".** The notes keep "sell mode" as a thing of its own. The transcript's "sell mode" is read here as "cell modem" (inference); the question is one question about the modem.
2. **"Decided by Pavel Frolov, no objections from Genadi Peari".** The transcript has Pavel: "Хорошо, если нет замечаний, тогда будем прорабатывать… оба варианта" and Genadi: "Очень хорошо. Спасибо" — assent, not a vote.
3. **"For RK the back end will differ by 50–60 percent".** The transcript: "не полностью переписываться, но процентов на 50, 60, наверное, будет отличаться от график юзаинтерфейс, наверное, может быть на 100% переиспользован" — the 50–60 % is about the tool as a whole on the RK platform; "the back end" is the notes' word. Kept as spoken on the decision page.
4. **Omitted by the notes:** Pavel's "Это 2." and "Фикс ремонт ли?" (answers to the chat, unclear); the Dallas section was "наверное, даже не разрешали" (probably not even enabled — the notes say "probably never enabled", the same); Pavel's remark that each SDK Linux build is used on every game build and every release, "и тем самым мы будем держать актуальным сам диагностик тул" (the notes have it).

**§15.8:** clear. A product idea and its scope only; nobody's pay, performance or personal matters are recorded. **§15 #9:** no corporate identifier appears.

## Sources
- [[raw/Meeting_Notes_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]
- [[raw/Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026.md]]
