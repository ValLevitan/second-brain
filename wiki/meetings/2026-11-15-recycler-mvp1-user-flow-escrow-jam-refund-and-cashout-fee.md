---
type: meeting
title: MVP-1 recycler capabilities and requirements review — Klimovich's player screens and flows for Thursday; capability 341 fixed to the 4-drum RQ; Cancel / Print / timeout; a jammed ticket cancels and refunds; Texas one balance; a per-location cash-out fee on the redemption screen; power loss and frozen payout money; RIS and Passport before the first live install; one note or a bundle still to check (Nov 15 2026, 8:01–8:57 AM)
date: 2026-11-15
aliases: [MVP-1 Recycler CAPs/REQs review, Recycler MVP1 User Flow Escrow Jam Refund and Cashout Fee, Sunday recycler meeting Nov 15, Nov 15 recycler review]
source-count: 2
open-commitments: 0
open-questions: 0
---

# MVP-1 recycler review — player flow, jams, cash-out fee (Nov 15 2026, 8:01 AM)

**Date/time:** Sunday November 15 2026, **8:01 – 8:57 AM Eastern**, about 56 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Recycler_MVP1_User_Flow_Escrow_Jam_Refund_and_Cashout_Fee-November-15-2026.md]] [[raw/Meeting_Notes_Recycler_MVP1_User_Flow_Escrow_Jam_Refund_and_Cashout_Fee-November-15-2026.md]]. Teams title: "MVP-1 Recycler CAPs/REQs review". **Language: Russian.** This is the Sunday 8 AM meeting set at the [[wiki/meetings/2026-11-12-mvp2-capability-review-goods-category-master-role-and-release-split.md|Nov-12 MVP 2 review]].

**Who spoke** (speaker labels): [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (organizer per the notes; he ran it), [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]]. One short line has no speaker label [[raw/Meeting_Transcript_Recycler_MVP1_User_Flow_Escrow_Jam_Refund_and_Cashout_Fee-November-15-2026.md]].

**Purpose.** Walk through the recycler MVP 1 player screens and flows and Klimovich's emailed questions before the Thursday Nov 19 target.

## Where the substance lives

- [[wiki/decisions/2026-11-15-recycler-mvp-1-player-flow-cancel-refunds-a-jammed-ticket-cancels-texas-shows-one-balance-and-a-location-cash-out-fee.md]] — every ruling, the $100-bill advice, the bundle question, commitments and open questions.
- [[wiki/decisions/2026-11-12-the-recycler-gets-its-own-mvp-1-on-the-production-server-by-thursday-november-19-and-its-mvp-2-a-week-later-scope-is-cut-never-the-date.md]] (Nov-15 note) — what MVP 1 means for Thursday.
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Nov 15) — the recycler thread.
- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Nov 15) — RIS and Passport before the first live recycler install.
- [[wiki/organizations/jcm.md]] (Nov 15) — the RQ vs RT model, one note or a bundle.
- [[wiki/decisions/2026-11-12-the-texas-twenty-dollar-promo-bonus-is-one-dollar-per-twenty-with-machines-at-ninety-percent.md]] (Nov-15 note) — promo credits and the Georgia handpay reminder.
- People: [[wiki/people/andrei-klimovich.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/val-levitan.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] (all Nov 15) · in absentia: [[wiki/people/genadi-peari.md]]

## Notes on the sources

- **§12 — new meeting.** The notes and transcript share date, time and title and link each other. A corpus-wide search for both filenames, "Recycler_MVP1_User_Flow", "Nov 15" and "8:01" found no page citing either file.
- **Notes vs transcript.** The notes' "admin screens follow tomorrow" is "я добью, там до завтра". The notes' "RQ model with 4 drums" reads "arq" / "arqq" / "аркэ" (heard). The notes' "Gennady's emails with JCM" is "переписку Геннадия с дрессемом" (heard). The notes omit that Biratka first said the RQ "все равно выдавать не умеет" a bundle, from taking it apart, before agreeing to check. The notes record the left-over-amount rule as staying on the wallet; Klimovich first called it "наш заработок чистой воды" — the wallet version is what Biratka and Pavel described. The notes call the payout-power-loss question "not settled"; the transcript agrees.
- **§4 name calls.** "саша" = Biratka; "Паша" = Pavel; "Андрей" = Klimovich; "вал" = Val; "Ирина" / "ира" = Irina; "Геннадия" / "гену" = [[wiki/people/genadi-peari.md|Genadi Peari]] (**inference**); "Дим дима это проектировал" (who designed the IQ ticket logic) — **unclear** which Dima.
- **Garbles kept as heard.** "риса айклера" / "resicler" / "ресайтер" / "рисайлэр" = recycler; "копеллиция" / "кокабеллис" / "Какобилице" = capability; "модель арте" / "RT" = RT; "джимовского" / "GCM" / "JCRM" = JCM; "анклейтмани" / "анклэнт" = unclaimed money; "форфид" = forfeit; "fp" = Flex-Pay; "его лет" / "волят" / "уоллет" = wallet; "плейхаз" / "хэнс" / "хэнцы" / "генс" = handpay / handle; "reed demable" = redeemable; "промо крадэс" = promo credits; "физ" / "фи" = fees; "сэтафи" / "set апмоут" = setup; "armack" = armored car (**inference**); "айхью" / "IQ" = Flex IQ; "remond innation setup" = Remote Installation Setup; "Даллас чип" = Dallas chip; "airbort" — **unclear** (a board); "gel licurmand" / "adial arecarment" = GLI requirement; "call ai leven" / "g li lever" = GLI-11; "хагвар мод" — **unclear** (a hardware module); "в ке школе" — **unclear**; "Рекстация" / "рексация" — **unclear** (Val agreeing).
- **Skipped as chatter.** The opening, screen sharing, the side remark on Iran's fake hundreds beyond the advice itself, Biratka leaving "в 05:00", the goodbyes.
- **Not recorded:** none beyond the chatter; no personal passage in either file.
- **§15.8:** clear — fees, the $65 a month and note amounts are market and product economics. **§15 #9:** none — 341 is a Jira capability number.

## Sources

- [[raw/Meeting_Transcript_Recycler_MVP1_User_Flow_Escrow_Jam_Refund_and_Cashout_Fee-November-15-2026.md]]
- [[raw/Meeting_Notes_Recycler_MVP1_User_Flow_Escrow_Jam_Refund_and_Cashout_Fee-November-15-2026.md]]
