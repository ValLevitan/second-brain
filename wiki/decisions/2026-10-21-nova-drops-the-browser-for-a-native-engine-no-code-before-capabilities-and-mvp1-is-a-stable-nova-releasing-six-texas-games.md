---
type: decision
title: NOVA drops the browser (and Pixi) for JVL's own native engine, with no browser build kept; no code before capabilities, requirements, acceptance criteria and an architecture Val can read; MVP1 is a stable NOVA on which JVL releases six Texas games, reached step by step (Val, Oct 21 2026)
date: 2026-10-21
aliases: [drop the browser, native engine, NOVA native engine, Rust engine prototype, Leshkevich Rust prototype, убрать браузер, no code before capabilities, никто не начинает строчить код, rule before code, MVP1 six Texas games, стабильное ново MVP один, NOVA 2, Super NOVA, супер нова, remove browser and Pixi, download flow with GLI signature check]
source-count: 5
status: active
open-commitments: 5
open-questions: 5
---

# NOVA drops the browser for a native engine; no code before capabilities; MVP1 = six Texas games on a stable NOVA

Decided at the [[wiki/meetings/2026-10-21-dutch-mill-on-nova-and-native-engine.md|Oct 21 2026 Dutch Mill review]] (8:02 AM, Russian) by [[wiki/people/val-levitan.md|Val Levitan]], with [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/alexander-biratka.md|Alexander Biratka]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]. It reverses [[wiki/decisions/2026-09-04-browser-pixi-stack-concern-closed.md]], where the same browser concern from Leshkevich was argued and closed "for now".

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## Leshkevich's case — a native prototype in Rust

- **Why raise it now.** The ports are about to go "на поток", and after that change gets harder: "если мы сейчас начнём этот конвейер, то потом будете тяжелее чтото менять." He called it the last time he would raise architecture; Val: the question must be raised "всегда" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **The browser is a legacy.** NOVA is "основан на браузере. Это наследие онлайн игр и нашей первоначальной цели сделать единый примор для 2 рынков"; JVL left online, so the browser is "просто leege, который добавляет over had". The cheap boards now being tested (the RK3576) may have limited resources [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **What he built.** Locally, he rewrote part of NOVA ("Не всю платформу, а там частично, просто чтобы игру поиграть") in Rust. He chose no graphics engine; he wrote small renderers that draw the Spine and Miranda resources, so the designers' work and what Igor converted are not lost. The LGS integration stays. The native app runs Calle Ocho ("калиочио") with most of its main features [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]. He said the work took "за 02:00" (read as about two hours — **inference**, by the same reading as "15:00" on Oct 18).
- **The numbers.** Speed about the same — FPS is capped at 60 and the prototype does not drop below it. The big gain is RAM: without the browser, with resources as they are, "Почти в 2 раза меньше оперативной памяти"; compressing the images halves GPU memory again. Best so far, Rust plus compressed images: "чтото около семиста мегабайт. Против 2 700 на текущей". Measured on his laptop only — he has no RK board [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **Why memory matters.** The RK board has no separate video memory — one memory for the system and the video chip — so memory may be "Сильным ботлэк"; the less memory the games use, the more can be deployed on the board. His main takeaway: the browser "никогда в жизни не даст такой гибкости и возможности оптимизировать под конкретные железяки" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **On the board today.** Pavel: that morning he, Sasha and Daniil looked at Calle Ocho on the board, optimized "по максимуму, что можно выжать из браузера"; it works, but with a few stutters [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].

## Who backed it

- **Val.** "Я лично полностью за… я не вижу смысла… в браузере." It was done for universality, which is not needed now: "Это была ошибочная, ошибочный danaxin. Сейчас время поправить, я поддерживаю Антоном в этом" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **Pavel.** The old premise was that JVL must take a third-party engine, from before AI; "а сейчас вот он, Антон может за неделю этот движок перегенерировать" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **Biratka.** "браузер у нас узкое место": it blocks video optimization, and syncing two videos is a big problem because the browser unloads and loads memory as it likes. He asked Leshkevich for a CPU-load comparison under a heavy object count [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]. He had floated dropping the browser before, but it always ran into having to tie JVL to someone else's engine; now it can be done fast [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **No browser build kept.** Pavel asked whether NOVA is thrown out or a universal solution builds either a browser or a native version. Biratka: "Зачем нам браузерная версия?… мы будем постоянно спотыкаться на то, что у нас вот врасти работает, а в браузере нет"; Irina: then both must be tested [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]. The notes record the decision as "no browser build kept" [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **No separate board test in Minsk.** Pavel proposed sending Leshkevich an RK3576 at once, then building his code for ARM in Minsk. Val: "Я уже заказал" the board for Anton; "Не надо… тратить время… мы знаем, что это будет лучше, чем сейчас… мы всё равно знаем, что мы отказываемся от браузера. И мы все равно хотим отказаться от миранты." Pavel: they could get the answer earlier and see which modules need work; Biratka: it would not move things forward much [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].

## Val's rule — no code before capabilities

- **The handshake.** When Biratka began on an editor, Val stopped it: "давайте все договоримся и пожмём руки виртуально. Мне нужны кейпобилотис реклайс эксептон никто не начинает строчить. Код до тех пор, пока это не сделано, когда это сделано 2 этапом делается архитектура." It must be readable — "мы можем все прочитать это" — and only then features and code. He asked each to agree in words: Anton "Yes да", Evgeny "Так точно", Igor "Да", Alexander "Конечно" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]. He repeated it later: "вы не начинаете строчить на акиборде до тех пор, пока нету кейпатис и архитектуры" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **Start from use cases.** Val: requirements should start from use cases, with personas; Biratka: for the engine these are technical requirements only. They are written down formally — Irina: otherwise "как я буду себя принимать всё?"; from the Transactional work they must be exact, with values stated, or Claude will send them back when writing tests [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **Architecture "для пятиклассников".** Val is not an engineer and needs the architecture explained simply [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **Tests.** Acceptance criteria exist so tests can be automatic; Claude should write them, with short end-to-end runs constantly after commits — "Это тоже надо обдумать" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].

## What Val wants the new platform to be

- **Comfortable for designers, testers and developers.** He sees a couple of designers left who say in words, in any language, how they see the design, and watch the build in real time; "Нам нужно ассигновать огромный эфрой на то, чтобы сделать дизайнеров очень комфортабельный" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **Drop Unity/Miranda.** "Мне очень нравится идея отказаться от… Миранды"; Pavel: "От юнити как среды разработки". Val: Unity-Miranda "это утопия было" — much money went into it, "Но мне будет приятно это потерять" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **A layer that breaks down a competitor's game.** Take video of a competitor game that plays well and break it into elements, as Igor did — geometry, motion physics, timing diagrams — through some translator; the layer must keep growing as competitors move. "Я не понимаю, как его сделать" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]. He also wants the game-breakdown standards ("раскройки игр") kept up and described in detail, with an assistant to manage that information and support artists and designers; he sees this between Metelski and Leshkevich [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **A CI/CD layer.** A finished game is pushed through NOVA to the machine "Безошибочно всегда", with an audit that the game installed correctly: "если мы делаем игры быстро. Мы не можем их загнать на машину?… это все… бесполезно" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **Upgrade machines in the field.** "Нам нужно на лету делать апгрейд машин", and know "что апгрейд на 100% правильно стал" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **Keep the RAGE experience.** Biratka: some RAGE parts were worked out over years and should be used; Val: do not cut them at once — first introduce something new the artists like more [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **First steps (Val, "непрофессиональная взгляд").** Remove the browser and Pixi; add the well-tested download flow and the GLI check that the components' signature is correct. Biratka: that is what Leshkevich's prototype did [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].

## MVP1 — six Texas games, step by step

- **Step by step.** Val: "Я предлагаю вам сделать мвпи 123. Немножко более плавный переход… менее радикальное… Займет дольше, но ошибок будет меньше." It can run on Texas or Georgia, with upgrades sent constantly [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **The target.** Biratka: so the MVP1 result is a game, not an editor? Val: "Да, цель игра… нам нужно стабильное ново MVP один, на которое мы можем выпустить 6 игр для Техаса" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **The time.** Answering Igor's question on Nebraska 2 and RAGE, Val said the new NOVA "появится быстро" and could be ready "на следующей неделе"; Leshkevich: "это очень оптимистично" — verification is iterative and the designers' assets are a big piece. Val: "10 дней я вам даю максимум" [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **The name.** Val: "Назовем ее нова 2"; Biratka: "Супер нова". Later Val said NOVA itself will keep progressing, so "нова 2 это будет что то там другое" — which name sticks is **unclear** [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **Who and when.** Each writes capabilities by Monday; grooming with the product owner starts Tuesday Oct 27 — [[wiki/decisions/2026-10-21-vladimir-samusenko-is-invited-as-nova-product-owner-and-capabilities-are-drafted-one-file-per-person-before-grooming.md]].

## Engine needs and open design points (first list)

- **What the engine must draw (Biratka).** Skeletal animation, images, video, text and fonts ("большой кусок работы"); later perhaps particles [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]].
- **The other pieces** — layers, scenes, shaders, an editor or a chatbot, AI self-debugging — are on [[wiki/topics/nova-platform-architecture.md]] (Oct 21, 8:02 AM).
- **Remote game updates.** Pavel: new maths on a machine most likely needs a regulator to be told; a new version of the same game (new art, same maths and button settings) may not. Irina: in Georgia only SAS/LGS is certified, games do not affect it, but Intralot must still know. Val wants a chatbot that deals with Intralot, built by Andrey Bosik — [[wiki/organizations/intralot.md]] (Oct 21) [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]. Pavel takes the update part — below.

## How it sits against earlier rulings

- **Reverses Sept 4.** [[wiki/decisions/2026-09-04-browser-pixi-stack-concern-closed.md]] closed the browser/Pixi concern on the argument "build the pipeline first; the engine is one block". Leshkevich's prototype and the RK3576 memory limit reopened it, and Val ruled for the native engine (update there).
- **Rests on Sept 17 and Oct 18.** NOVA is the only platform for new work — [[wiki/decisions/2026-09-17-no-more-games-on-rage-and-texas-is-built-on-nova.md]], [[wiki/decisions/2026-10-18-rage-is-closed-dutch-mill-reaches-nova-by-wednesday-and-a-reskin-from-a-new-theme-tests-the-tools.md]].

## Open commitments

- [ ] [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] — ask Andrei (Bosik, by role — **inference**) for a repository and upload the Rust prototype, which lives only on his disk — due unspecified — [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — write the capabilities and requirements for the game-update part — due unspecified — [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — build a chatbot that deals with Intralot (Val's wish; not present) — due unspecified — [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] *(9:57 AM the same day: Val formally made Bosik the developer of a Georgia commissioning chatbot, with Pavel Frolov as product owner — tracked on [[wiki/decisions/2026-10-21-pavel-frolov-is-product-owner-of-the-georgia-commissioning-chatbot-and-andrey-bosik-develops-it.md]] [[raw/Meeting_Transcript_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]])*
- [ ] Team (no single owner named) — have the new NOVA ready ("это будет готово"; the notes place it under MVP1) — due within 10 days of Oct 21 (Val's "максимум"; Leshkevich called it optimistic) — [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- [ ] [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] — optimize his variant, which runs slow — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]

## Open questions

- Does "Nebraska 2 is the last product on RAGE" still stand? Igor asked; Val answered only that the new NOVA will come fast — [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- Can a still image with a shader replace heavy background video? Biratka is sure; Igor wants a test first (possible in Pixi) — [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- Keep the OMNI scene structure in the new engine, or a new one? — [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- A full designer editor, or scenes built through a chatbot? — [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- How are games updated remotely when the maths changes, and what does each regulator require? — [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]] [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]

**§15.8:** clear. **§15 #9:** clear.

## Note, Oct 22 2026 — Pavel restates the ruling to the team; Leshkevich's variant runs slow

At the [[wiki/meetings/2026-10-22-daily-standup-flex-port-cashout-screens-and-native-engine.md|Oct-22 Minsk stand-up]] (Russian; Val absent) [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]:

- [[wiki/people/pavel.md|Pavel]] told the stand-up that at the previous day's meeting "Антон предложил отказаться от браузера, написать свой angen" in Rust ("На нарасте"; the notes: Rust, heard). It is "новая такая идея, которая будет прорабатываться", and the team will now decide its requirements; it saves about half the memory, maybe other resources too — "глобальный переворот"; "для этой платформы наверно другого пути и не будет" [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]].
- Pavel ran "твой вариант" ([[wiki/people/anton-leshkevich.md|Leshkevich]]'s) that morning: "Тормозит, короче, тебе придётся там посмотреть, как его оптимизировать." Which build and on what hardware is not said [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]. (Val had declined a separate board test in Minsk; whether this run was one is **unclear**.)
- Leshkevich said he is writing release notes for Gennadiy (as heard, "рекларс для genadingo"; the notes: release notes, heard) [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]. Board shipments: [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]] (Oct-22 update).

## Sources

- [[raw/Meeting_Transcript_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- [[raw/Meeting_Notes_Dutch_Mill_on_NOVA_and_Native_Engine-October-21-2026.md]]
- [[raw/Meeting_Transcript_Pavel_Frolov_Commissioning_Chatbot_Product_Owner-October-21-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]
