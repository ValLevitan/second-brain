---
type: meeting
title: NOVA-2 follow-up (Friday check) — Anton shows his agent converter for turning Nebraska Rage games into NOVA games, Lions Riches first; his OpenRouter tokens ran out; Val sets "done" as a CI-built image from the production server running in a machine; LGS is not yet runnable on a machine and the old Data Center idea is dropped; Texas first, then probably Georgia; the first ISO is targeted for Tuesday; Kharetski's design agent waits; Claude Code run locally could save about $15,000 a month (Nov 13 2026, 7:01–8:11 AM)
date: 2026-11-13
aliases: [NOVA-2 follow-up - Friday check, NOVA-2 Agent Converter Demo and First ISO by Tuesday, Nov 13 NOVA 2 meeting, Friday NOVA 2 follow-up]
source-count: 2
open-commitments: 0
open-questions: 0
---

# NOVA-2 follow-up — agent converter demo and first ISO by Tuesday (Nov 13 2026, 7:01 AM)

**Date/time:** Friday November 13 2026, **7:01 – 8:11 AM Eastern**, about 70 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_NOVA-2_Agent_Converter_Demo_and_First_ISO_by_Tuesday-November-13-2026.md]] [[raw/Meeting_Notes_NOVA-2_Agent_Converter_Demo_and_First_ISO_by_Tuesday-November-13-2026.md]]. Teams title: "NOVA-2 follow-up - Friday check". **Language: Russian.** It follows the [[wiki/meetings/2026-11-11-nova-2-mechanics-placement-one-studio-tool-and-game-metrics.md|Nov-11 7:31 AM NOVA-2 follow-up]].

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]] (host), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik") [[raw/Meeting_Transcript_NOVA-2_Agent_Converter_Demo_and_First_ISO_by_Tuesday-November-13-2026.md]].

**Purpose:** Anton presents his agent converter; the group checks whether NOVA works and plans the first ISO [[raw/Meeting_Notes_NOVA-2_Agent_Converter_Demo_and_First_ISO_by_Tuesday-November-13-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-11-13-nova-is-done-only-when-a-ci-built-image-from-the-production-server-runs-on-a-machine-the-first-iso-is-built-tuesday-texas-first-then-georgia-and-the-design-agent-waits.md]] — the converter; the three steps; Igor's work and the art question; the "done" ruling; the production download screen; Val's parallel flow; LGS readiness and the old Data Center dropped; Texas then Georgia; the Tuesday ISO plan; AI cost; all commitments and questions.
- [[wiki/decisions/2026-11-11-nova-2-gets-one-tool-from-brief-to-game-igors-scene-flow-goes-into-the-studio-the-ai-model-is-a-replaceable-setting-a-tuesday-demo-and-where-mechanics-live-stays-open.md]] (Nov-13 note) — Igor's tools in the shared repository; Kharetski's Tuesday design-agent work moved.
- [[wiki/decisions/2026-11-04-a-release-is-done-only-when-the-cleaned-build-is-on-the-production-server-under-a-number-ivan-is-release-manager-with-claude-written-release-notes-and-an-exception-report-and-request-review-leaves-the-feature-workflow.md]] (Nov-13 note) — the same "done" test for NOVA.
- [[wiki/decisions/2026-09-01-first-nova-product-south-dakota-vlt-2.md]] (Nov-13 update) — Texas first, then probably Georgia.
- Topics: [[wiki/topics/nova-platform-architecture.md]] (Nov 13) · [[wiki/topics/ai-assisted-development.md]] (Nov 13)
- People: [[wiki/people/val-levitan.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/pavel.md]] · [[wiki/people/igor-metelski.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/sergey-tsymanov.md]] (all Nov 13)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "Agent_Converter", "Friday check" and "First ISO" found no page citing either file. No other Nov-13 meeting is stubbed.
- **Time.** The header says 7:01 AM Eastern; the transcript's inner line "13 November 2026, 12:01pm" is a different zone and is not used.
- **Microphone echo.** Kharetski sat in the room with Metelski (Igor: "ты у меня возле меня сидишь"); many lines under his label repeat Biratka or Metelski. The notes say so; only his own lines are used as his.
- **§4 name calls.** "Антон" = Leshkevich; "Игорь" = Metelski; "женя" / "Евгений" = Kharetski (he answers on LGS and the build); "Саша" = Biratka; "Андрей" (OpenRouter, CI/CD) = Bosik; "Паша" = Pavel Frolov; "дима" / "Димой чудиновым" = [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (the server screen, CI/CD — back-end by context and by name); "Сергей цимонов цыманов" / "Сергеем цыманом" = [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]]. "Liashkevich" vs "Leshkevich" — same person, per the notes.
- **Garbles kept as heard.** "лайн Ричард" / "lines Ричарда" = Lions Riches (per the notes); "Львов" / "любы" next to it — **unclear**; "nat 2" / "NAD 2" = Nebraska NAD-2; "rade" / "рейдж" / "речь" = Rage; "open rowter" / "open rutter" / "опен раутер" = OpenRouter; "нанобанану" = nano banana; "IPIK" = API key (inference); "р к" = RK; "35 76" = RK3576; "с 3" / "stri" = S3; "транзак" = transactional; "андрэтейкинг" = undertaking; "лжес" / "элджис" / "lg s" = LGS; "дотацентр" / "дета центр" = Data Center; "сас" = SAS; "I so m" / "высо" / "айсоч" / "ICOI mac" = ISO; "акшинс" = actions; "CICD" = CI/CD; "Джорджилтеямадем" / "алто я мадам" = Georgia LTE modem (per Val after the meeting, in the notes); "Б м п один" — **unclear**; "Клатр регион" = Claude Code (per the notes); "нюкин" — **unclear**; "23 игры" = 2–3 games (the notes' reading). **Unclear and skipped:** the English-sounding garble at 1:06:02–1:06:53 ("Sastrani Igor Giorgi", "The Voya") — the notes call it garbled.
- **Notes vs transcript.** The notes say Val ruled both Georgia work and the ISO "in parallel"; the transcript line is "А мы параллельно не можем оба сделать" with no punctuation, readable as a question. The notes' $15,000 figure is "15000 в месяц" on the transcript; "Claude Code commit expenses" is Val's after-meeting reading, in the notes only.
- **Skipped as chatter.** The screen-zoom talk, the "wet finger" jokes, the praise round at the end, Val's coffee remark.
- **Not recorded:** personal matters not recorded.
- **§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_NOVA-2_Agent_Converter_Demo_and_First_ISO_by_Tuesday-November-13-2026.md]]
- [[raw/Meeting_Notes_NOVA-2_Agent_Converter_Demo_and_First_ISO_by_Tuesday-November-13-2026.md]]
