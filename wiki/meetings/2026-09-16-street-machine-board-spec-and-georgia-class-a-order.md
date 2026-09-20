---
type: meeting
title: Street machine board spec and the Georgia Class A order (Sept 16 2026, 12:35 PM)
date: 2026-09-16
aliases: [Street Machine Board Spec and Georgia Class A Order, Alignment call September 16 2026, the 12:35 alignment call, стрит машина board spec, Sept 16 alignment call, Genadi Pavel Val alignment 12:35]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Street machine board spec and the Georgia Class A order (Sept 16 2026)

**Date/time:** September 16 2026. The source header gives the slot as **12:30 – 13:00 PM Eastern** with the **recording running 12:35 – 13:41** — about **1 hour 6 minutes**, more than double the booked half-hour. The last cue lands at 01:05:38, which is consistent with the 12:35 start. **Series:** a Microsoft Teams session titled `Alignment call`. **Language: Russian** — the raw transcript is Russian throughout (696 cues); the derived notes are an English gloss [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]] [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/pavel.md|Pavel Frolov]]. Three speaker labels in the transcript, no others [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**Purpose:** the regular alignment call — short status round, then Val reports what he is hearing in the Texas and Georgia markets, and the rest of the hour is a working session on the cheap street machine: what its electronics must contain and what the cabinet should look like [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## §12 — a concurrent recording, not a duplicate: Val took a phone call mid-session

**This is a new situation for the corpus.** Another Sept-16 2026 recording, `Jamie_Georgia_Class_A_Opportunity_and_Market_Outlook`, runs **12:50 – 13:06** — **wholly inside** this one's 12:35–13:41 window. Every previous §12 overlap in this corpus involved recordings that touched or abutted; this one is fully concurrent. It is **not** a re-transcription and **not** a derived-document family member. The evidence, from this source alone:

- **At 00:15:01 — wall clock 12:50:01 — Val says he is picking up the phone:** "**Одну секунду[,] я уже взялся телефон.**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- **Val then says nothing for 16 minutes 31 seconds.** Genadi and Pavel carry on working without him through the whole gap — the button/counter board, whether low-power mode is needed, what the FRAM is for, chip sizing, the bill-acceptor protocols. The room does not stop [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].
- **At 00:31:32 — wall clock 13:06:32 — he comes back and apologises for exactly that:** "**Я извиняюсь[,] я извиняюсь. Я ожидал этот звонок уже много времени. Наконец[-]то мне этот человек позвонил, и я не мог отказать.**" — I had been waiting a long time for that call; the person finally rang and I could not refuse [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].
- **His absence, 12:50:01 → 13:06:32, matches the other recording's 12:50 – 13:06 window almost to the minute.**
- **No fourth voice appears anywhere in this file**, and nothing of the other conversation is audible inside it — the 12:50–13:06 stretch is Genadi and Pavel talking to each other about boards.

**Reading, stated as a finding and not as a merge:** Val stepped out of this Teams call to take an inbound phone call he had been waiting for, left the Teams session running, and that phone call was captured as its own recording. **Two concurrent recordings of two different conversations, sharing one participant — two meetings, two stubs.** Nothing about the other conversation is asserted here; it is **not** cited as a source on this page.

**Confirmed from the other side.** That call has now been ingested as [[wiki/meetings/2026-09-16-jamie-boyden-call-recycler-advice-and-class-a-recruitment.md|the 12:50 PM phone call with Jamie Boyden]], and its own sources support the reading independently: two voices only, no third party, nothing of this engineering room audible anywhere in it, and it opens and closes as a private phone call. **The two stubs stand separately; nothing is merged.**

**Val stepped out twice more.** At 00:41:16 ("**Ещё секунду**", back by 00:43:28) and, more substantially, at **00:45:21** — "**Нет, мне нужно общаться на звонок, продолжайте**", back at **00:54:42**, a second absence of 9m21s (wall clock ≈ 13:20 – 13:30). No other recording in the corpus is known to cover that window. Two of the call's outcomes were worked out by Genadi and Pavel *during* that absence and re-put to Val afterwards — see the identity and GLI decisions below [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

The notes and the transcript are one **derived-document family** (§12) — one meeting, one stub, both cited. A corpus-wide check found no earlier page citing either file and no other source covering a 12:35 PM Sept-16 session. This is the **fifth** of eight recordings Val made that day (6:11 AM, 8:01 AM, 10:12 AM, 11:31 AM, **12:35 PM**, 12:50 PM, 2:42 PM, 2:53 PM ET); the 11:31 AM one immediately before it is [[wiki/meetings/2026-09-16-games-conversion-and-ai-graphics-transcription-failed.md|the games-conversion call whose transcription failed]].

## Where the substance lives

- [[wiki/decisions/2026-09-16-the-street-machine-carries-two-boards-and-a-new-io-board.md]] — two boards, the new I/O board's full port list, ID003 + ccTalk with pulse ruled out, amplifier dropped, no electromechanical counters, cell modem and WiFi mandatory, and the board-price argument.
- [[wiki/decisions/2026-09-16-one-fram-chip-instead-of-six-and-low-power-mode-laid-in-but-not-populated.md]] — the money: six 256 FRAM chips down to one, the per-game statistics moved out to SD or eMMC, and Val's reversal on low-power mode.
- [[wiki/decisions/2026-09-16-street-machine-electronics-move-to-eye-level-and-the-monitor-opens-like-a-cupboard-door.md]] — eye-level electronics in a metal box behind the TV, the cupboard-door monitor at ≤90°, the technician recording Val holds, and the unresolved board-mounting argument.
- [[wiki/decisions/2026-09-16-machine-identity-moves-off-the-cabinet-passport-onto-jvls-own-io-board.md]] — the cabinet-bound passport component removed, identity bound to JVL's own board, and the unanswered board-change procedure.
- [[wiki/decisions/2026-09-16-street-machines-skip-gli-so-no-boxes-and-no-tampers-but-nebraska-reopens-it.md]] — no GLI, therefore no boxes and no tampers; then Val reopening it over Nebraska.
- [[wiki/topics/low-cost-street-machine.md]] (Sept 16) — the cabinet look, the lighting question, Genadi's read-back of the whole machine, and where this call sits in the street-machine timeline.
- [[wiki/topics/georgia-class-a-machines.md]] (Sept 16, internal) — what Val told the engineering team about the Class A order, and his own same-day correction to it.
- [[wiki/decisions/2026-09-14-vertical-texas-starts-from-the-georgia-coam-vertical-games.md]] (Sept 16 update) — Pavel's two AI game-conversion experiments and Val's "days, not weeks".
- [[wiki/people/genadi-peari.md]], [[wiki/people/pavel.md]], [[wiki/people/michael-gottlieb.md]] (Sept 16) — status, commitments and the Georgia field trip.

## What else was on the call

Short items that did not need their own page: Val's travel plan (Texas on the **2nd**, Nebraska on the **5th, 6th and 7th**, back in Georgia on the **12th** — **the month is not stated in the source**); Genadi's instruction to **release the IQ moulds and tooling**, which he said he would do "**сегодня[,] завтра же**"; the underside recess where a sticker sits, which Val wants replaced by a separate plastic piece rather than left "**[н]екрасиво**" — unsettled, and Genadi confirmed it does not affect the tooling; and **shipping to Belarus**, which goes through third countries — Turkey, China, Uzbekistan or Kazakhstan — with Poland ruled out by sanctions and nobody known in Uzbekistan to organise the parcel [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## Names and strings left unresolved (§4, §9.131)

- **"Сергей Клемёныч"** — the person Val said he wants to bring back to work in Minsk, to be taught the AI coding tool and paired with a programmer. **No person in this corpus matches**, and the rendering looks like a familiar patronymic rather than a surname. Not matched, not forced — queued for the owner. This item is **absent from the derived notes entirely**.
- **"склад код" / "склодам"** — the tool Val credits for making game conversion fast. The derived notes read it as **Claude Code**; recorded here as the notes' reading, **flagged as inference**, with the transcript string kept.
- **"рк 38 76"** (Val) against "**р к 35, 68 или р к там 35 76**" (Pavel) — the compute board. The Sept-14 RK3576 ruling is not contradicted, but the engineers were still naming both parts. See the two-boards decision.
- **"es de mi"** / **"зима"** — the main-monitor connector. Read as **HDMI** by context; inference, not a literal string.
- **"клипс"** — the certification lab. Read as **[[wiki/organizations/eclipse-gaming-lab.md|Eclipse]]** on corpus support (JVL's Nebraska and Georgia lab). Note this is the **opposite** call from Sept 14, where the same garble referred to an unidentified older *machine* and was left open.
- **"i ki … молды [и] tooling"** — read as the **IQ** moulds and tooling by context (IQ is a live JVL product line Genadi was working that week); inference.
- **Left as transcribed, not interpreted:** "**Франк лоу**" (something to be fitted alongside the peripheral printer), "**как на этих самых на альтерах**" (Pavel's comparison for the board-change procedure), "**м в д … бордовый**" (the board material Val could not name beside plywood), "**рисо/рисы**" (read as the underside recess; inference), "**[а]ппарат никогда с лэнтопом не будет**", "**21000**" (the current panel size, i.e. 21 inches).

## Notes ↔ transcript divergences found

Three, all recorded on the pages that carry the facts:

1. **"Number one" vs "number two."** The notes call the Georgia operator "the number-one company in Georgia"; the transcript has Val say "**намберту**" — **number two**. The corpus independently carries Val's own 2026-09-10 ruling that this operator is the state's **number two**. The transcript reading is used.
2. **The board price.** The notes state the team pays "around $600 a board today"; in the transcript Genadi corrects himself immediately — that was last year's price and he does not know today's.
3. **A whole passage is missing from the notes** — Val's plan to route the street-machine graphics work around JVL's graphics department, take one person in Minsk, and bring "Сергей Клемёныч" back. Recovered from the transcript and recorded on [[wiki/people/val-levitan.md]].

**§15.8:** hardware, board, cabinet, certification and operator/market economics are recorded. **One item was excluded** — a comparative remark by one engineer about a named colleague's board work. **§15.9:** no identifier values appear; the machine-identity decision records *how* an ID is anchored, never an ID.

## Sources

- [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
