---
type: meeting
title: MVP 2 capability review — Klimovich wants every capability moved from Proposed to Accepted; the purpose of design read out and Val's rules for it (prose, two paragraphs, the business "why", no numbering); "inspector report" becomes "audit report"; SIM data tied to the location, reporting later on the server; "Lottery" (CAP-159) becomes one generic "Goods" category; machine names, CAP-312, requirements 2066 and 2069; two kinds of "master" and a Master role (CAP-367); alerting in Grafana; MVP 2 split into 2_1 (IQ and port) and 2_2 (web services); only Irina or Pavel create releases; recycler MVP 1 on November 19 on the Flex-Pay base and a Sunday meeting (Nov 12 2026, 8:33–9:21 AM)
date: 2026-11-12
aliases: [MVP2 Transactional planning, MVP2 Capability Review Goods Category Master Role and Release Split, Nov 12 MVP 2 review, MVP 2 capability review]
source-count: 2
open-commitments: 0
open-questions: 0
---

# MVP 2 capability review — Goods, the Master role and the release split (Nov 12 2026, 8:33 AM)

**Date/time:** Thursday November 12 2026, **8:33 – 9:21 AM Eastern**, about 48 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_MVP2_Capability_Review_Goods_Category_Master_Role_and_Release_Split-November-12-2026.md]] [[raw/Meeting_Notes_MVP2_Capability_Review_Goods_Category_Master_Role_and_Release_Split-November-12-2026.md]]. Teams title: "MVP2 Transactional planning". **Language: Russian.** It is the MVP 2 review the [[wiki/meetings/2026-11-11-mvp1-release-procedure-release-notes-and-product-sign-off.md|Nov-11 release meeting]] moved to "tomorrow", and the meeting with Andrei the [[wiki/meetings/2026-11-12-daily-standup-recycler-rust-service-and-no-features-before-capability-review.md|Nov-12 stand-up]] was waiting for (**inference**).

**Who spoke** (speaker labels): [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (ran it), [[wiki/people/pavel.md|Pavel Frolov]] (organizer per the notes), [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik") [[raw/Meeting_Transcript_MVP2_Capability_Review_Goods_Category_Master_Role_and_Release_Split-November-12-2026.md]].

**Purpose (Klimovich):** "пройтись по MVP 2" so every capability goes from Proposed to Accepted or has its problems flagged [[raw/Meeting_Transcript_MVP2_Capability_Review_Goods_Category_Master_Role_and_Release_Split-November-12-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-11-12-mvp-2-splits-into-mvp-2-1-iq-and-port-and-mvp-2-2-web-services-lottery-becomes-goods-and-the-inspector-report-becomes-the-audit-report.md]] — purpose of design, audit report, SIM data, Goods, machine names, CAP-312, reports, the Master role, Grafana, the 2_1 / 2_2 split, who creates releases; commitments.
- [[wiki/decisions/2026-11-12-the-recycler-gets-its-own-mvp-1-on-the-production-server-by-thursday-november-19-and-its-mvp-2-a-week-later-scope-is-cut-never-the-date.md]] (the 8:33 section) — recycler MVP 1 on November 19, the Flex-Pay base, Sunday's meeting, Bosik's CI/CD, Elizabeth and the demo-room unit.
- Earlier decision annotated: [[wiki/decisions/2026-11-05-mvp-2-is-kept-narrow-wi-fi-with-the-flex-iq-as-access-point-or-client-remote-flex-port-update-robust-installation-and-install-diagnostics-due-november-20-and-the-rest-goes-to-mvp-3-around-january-20.md]] (Nov-12 8:33 note).
- Topics: [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Nov 12) · [[wiki/topics/github-release-management-pipeline.md]] (Nov 12)
- People: [[wiki/people/andrei-klimovich.md]] · [[wiki/people/pavel.md]] · [[wiki/people/val-levitan.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/andrey-bosik.md]] (all Nov 12, 8:33 AM) · in absentia: [[wiki/people/elizabeth.md]]

## Notes on the sources

- **§12 — new meeting.** The notes and transcript share date, time and title and link each other. A corpus-wide search for both filenames, "MVP2_Capability_Review", "MVP2 Transactional planning" and "8:33" found no page citing either file. It follows the [[wiki/meetings/2026-11-12-flex-recycler-slim-mvp1-by-thursday-and-20-dollar-promo-bonus.md|6:53 AM recycler meeting]] and is a different session.
- **Notes vs transcript.** The notes' "CAP-367" is Pavel's "кап 367" and Klimovich's "Это 37 каб" (heard). The notes' "requirement 2066 / 2069" are "рекламент 20 66" / "реклаймент 20 69". The notes' "MVP 2_1 and MVP 2_2" are "2 подчеркивания", "2 в 02:01" and "22" (heard). The notes' "Thursday, November 19" rests on Irina's "почему 19?" and Pavel's "Четверг четверг звучал". The notes' "8 AM Eastern (4 PM Minsk)" is "8" and "04:00 будет по Минску". The notes' "Dzmitry" comments are Chudinov's; the notes' "remaining days this week" is "оставшиеся пару дней на этой неделе".
- **§4 name calls.** "дима" (comments, Claude reading the code base) = Chudinov (he answers); "Андрей" running the meeting and "продактона" = Klimovich; "Андрей босик" = Bosik; "Андрей климорович" = Klimovich; "ира" / "иру" = Irina; "саша" / "сашу" = Biratka; "пара" (Val: who creates releases) = Pavel (Паша, **inference**); "Элизабет" = [[wiki/people/elizabeth.md|Elizabeth]]; "Борис" ("готов по Борис", "копо билетия Бориса сайтеру") — heard; read as "recycler", not a person (**inference**). "Таня" (Chudinov, once) — **unclear**, not a person on the call.
- **Garbles kept as heard.** "белитись" / "копобилити" / "capelity" = capabilities; "пропост в асептед" = Proposed to Accepted; "процесс оф дизайн" / "корпус, оф дизайн" / "пропусок, дизайн" / "пропресовый дизайн" = purpose of design; "бескрепщен" / "дискрепшен" = description; "IVP" / "MGP 2" / "pm p 3" / "мг т п и 3" = MVP; "одитрепорт" = audit report; "лотари" / "лоцари" / "лотере" = lottery; "гуц" / "гус" / "гутс" / "гуть" = goods; "oation desbord" / "душ морда" = operations dashboard; "лакейшн" = location; "posus" / "сассу" = SAS; "графана" = Grafana; "Алиса" (Val: "Алиса может создать только Ирина или пара") = релиз (release), as the notes read it; "арендатором" = validator; "Jc валидатором" = JCM validator (the notes' reading); "ICD" = CI/CD; "Сансгот" — **unclear**; "матч бриллиант юрафул налаживается класс лабер" — **unclear**.
- **Skipped as chatter.** The greetings; Val's long aside on why the category must stay abstract (kept only as the reason recorded on the decision page); remarks on working hours; the goodbyes.
- **Not recorded:** personal matters not recorded.
- **§15.8:** clear. **§15 #9:** clear — CAP and requirement numbers only.

## Sources

- [[raw/Meeting_Transcript_MVP2_Capability_Review_Goods_Category_Master_Role_and_Release_Split-November-12-2026.md]]
- [[raw/Meeting_Notes_MVP2_Capability_Review_Goods_Category_Master_Role_and_Release_Split-November-12-2026.md]]
