---
type: meeting
title: Review, Dutch Mill on NOVA (first iteration) — Igor shows Dutch Mill on NOVA with tests and a vertical Midnight Money built from a theme; Leshkevich's Rust prototype drops the browser; Val's rule "no code before capabilities"; MVP1 is a stable NOVA for six Texas games; Samusenko is asked to be product owner (Oct 21 2026, 8:02–9:35 AM)
date: 2026-10-21
aliases: [Review - Dutch Mill on NOVA first iteration, Dutch Mill on NOVA and Native Engine, Oct 21 Dutch Mill review, Wednesday Dutch Mill review, native engine meeting, drop the browser meeting]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Review — Dutch Mill on NOVA, first iteration (Oct 21 2026)

**Date/time:** October 21 2026 (a Wednesday), **8:02 – 9:35 AM Eastern**, about 1 h 32 min, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]. Teams meeting "Review - Dutch Mill on NOVA, first iteration". **Language: Russian.** This is the Wednesday review Val set on Oct 18, and the "8:00 meeting" Leshkevich named at the [[wiki/meetings/2026-10-21-daily-standup-flex-port-mode-switch-and-sas-crc-fix.md|Oct-21 stand-up]] that morning.

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/igor-metelski.md|Igor Metelski]] (presented), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] (presented), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"; joined after about 19 minutes), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].

**Purpose.** See the first NOVA iteration of Dutch Mill. The meeting then turned to the engine under NOVA, the rule for how the new work starts, MVP1, and a product owner [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-10-21-nova-drops-the-browser-for-a-native-engine-no-code-before-capabilities-and-mvp1-is-a-stable-nova-releasing-six-texas-games.md]] — the native-engine prototype and its memory numbers, the browser dropped, Val's rule, what Val wants in the new platform, MVP1, remote game updates, the engine needs list.
- [[wiki/decisions/2026-10-21-vladimir-samusenko-is-invited-as-nova-product-owner-and-capabilities-are-drafted-one-file-per-person-before-grooming.md]] — the product-owner debate, Samusenko, and Pavel's one-file-per-person method.
- [[wiki/decisions/2026-10-18-rage-is-closed-dutch-mill-reaches-nova-by-wednesday-and-a-reskin-from-a-new-theme-tests-the-tools.md]] (Oct-21 update) — Dutch Mill on NOVA shown; Midnight Money from a theme; commitments discharged.
- [[wiki/decisions/2026-10-08-texas-rage-games-convert-to-vertical-nova-unchanged-and-igor-ports-dutch-mill-first.md]] (Oct-21 update) — the Dutch Mill port is done; how long a port takes.
- [[wiki/decisions/2026-09-04-browser-pixi-stack-concern-closed.md]] (Oct-21 update) — the browser question reopened and reversed.
- [[wiki/topics/nova-platform-architecture.md]] (Oct 21, 8:02 AM) — the engine layers, scenes, shaders, AI self-debugging.
- [[wiki/topics/game-art-animation-production-pipeline.md]] (Oct 21) — Midnight Money art from a theme with Claude and ChatGPT.
- [[wiki/organizations/intralot.md]] (Oct 21) — remote game updates in Georgia; Val wants a chatbot for Intralot.
- People: [[wiki/people/igor-metelski.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/val-levitan.md]] · [[wiki/people/vladimir-samusenko.md]] (in absentia) · [[wiki/people/andrei-klimovich.md]] (named) · [[wiki/people/alexei-khamin.md]] (named) · [[wiki/people/andrey-bosik.md]] (named)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "Dutch_Mill_on_NOVA", "Native_Engine" and "2026-10-21" found no page citing either file and no stub for this session. The 4:46 AM stand-up the same day is a separate meeting.
- **§4 name calls.** "Саша" = Biratka (he answers). "Игорь" / "метельским" = Metelski. "Антон" / "лишкевич" = Leshkevich. "Евгений" / "Женя" = Kharetski (speaker label; "проект, над которым работает Женя" = his voice game-design assistant — **inference**). "Андрей климович" = [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (surname spoken); "Андрея босика" = [[wiki/people/andrey-bosik.md|Andrey Bosik]] (surname spoken). The "Андрей" Leshkevich will ask for a repository fits Bosik by role (DevOps/GitHub — **inference**). "Алексей камин" / "хамен" = [[wiki/people/alexei-khamin.md|Alexei Khamin]]. "Влад… фронт энд" / "Владимир" / "Самусенко" / "Самовсянка" / "Овсянка" = [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]]. "Ваня шпак" = [[wiki/people/ivan.md|Ivan]]; "дима хандов" = [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]] (both named by Igor as possible product owners; not taken up). "Себастьяну" = [[wiki/people/sebastian.md|Sebastian]] (by context — Irina's question about the capabilities he was asked to write; **inference**). "Даниил" = Daniil Stauskiy (no page). "пиратко" / "либератка" = Biratka.
- **Garbles kept as heard.** "дачмил" = Dutch Mill; "миднайтмани" = Midnight Money; "лайн рич" / "лайонс что то" = Lion's Riches (the notes: "Lion's Rich"); "гкам 3" = GCOAM 3 (the notes); "клауэр farn" = Clover Fortune (the notes); "калиочио" = Calle Ocho; "р к 3576" / "арка 35 76" = the RK3576 board; "раст" = Rust; "пикси" / "pixy" = Pixi; "чат г б т" / "чаджи" = ChatGPT; "джимин" / "GMI" = Gemini; "игрок" / "круг" = Grok (the notes); "квен и матч 2.1 турбо" — Qwen and a second model, **unclear**; "кейпобилотис" / "копобилити" = capabilities; "реклайс эксептон" = requirements and acceptance criteria; "prodactoner" / "продактонор" = product owner; "dan lott fre" = download flow (the notes); "jel i" = GLI (the notes); "интролот" / "центролотом" = Intralot; "в gri" — Pavel's "new project", read by the notes as a new repo; "нова 2" / "супер нова" — a working name, **unclear** (see the engine decision); "Оператор наверно возьмет на себя часть, чтобы убрать браузер" — who "оператор" is, **unclear**.
- **Where the notes and the transcript differ.** The notes do not mention that Leshkevich's native prototype runs Calle Ocho, or that Pavel saw Calle Ocho stutter on the board that morning; the transcript says both. The notes give the Dutch Mill port as "about one session"; the transcript's "примерно 06:01 сессия" is garbled (the Oct-20 stand-up said about six hours).
- **Skipped as chatter.** Jokes about the wolf, haircuts, "young stallions", the Hunger Games quote, Val's rude remarks about Intralot's office, greetings and goodbyes.
- **§15.8:** clear. No pay or rate appears; Val's remark that he put much money into Unity/Miranda is a company cost with no figure. **§15 #9:** clear. **§15.1:** Samusenko's short vacation is recorded only as an availability date (back Monday Oct 26); nothing personal.

## Sources

- [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
