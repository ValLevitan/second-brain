---
type: decision
title: Anton Leshkevich's online "creator platform" (reskins of JVL's certified games for outside developers) is not pursued — JVL is not in the online market; instead Val points to a loop where the machine on location measures what players like, JVL makes a new game, reskin or extra mechanic with little human work, GLI approves it, and the game goes straight to the machine and is enabled by matching checksums; judging what players like is the unsolved part (Val, Nov 10 2026)
date: 2026-11-10
aliases: [creator platform, JVL Creator Platform, платформа для разработчиков, reskin library of certified games, Stake Engine comparison, стейк энджин, telemetry-to-new-game loop, player telemetry game loop, щупальцы индикаторов, send games straight to the machine, отправлять прямо на машину, GLI approval by checksum, what players like is the unsolved problem, mechanic theme or math]
source-count: 4
status: active
open-commitments: 1
open-questions: 2
---

# The online creator platform is not pursued; JVL aims at a loop from player data on the machine to new games sent straight to it (Nov 10 2026)

Said by [[wiki/people/val-levitan.md|Val Levitan]] in reply to [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] at the [[wiki/meetings/2026-11-10-jvl-creator-platform-idea-and-player-telemetry-game-loop.md|Nov 10 2026, 5:16 PM call]] (Russian, two people) [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]] [[raw/Meeting_Notes_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].

*(Quotes are from an unpunctuated Russian speech-to-text transcript, kept word for word; garbles are marked "heard".)*

## Anton's idea — a creator platform

- **An idea, not a product.** "идея ни в коем случае не готовый продукт"; it grew from notes he kept "в процессе моей работы над текущей ново 2" [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].
- **The basis.** JVL "есть большая коллекция математики и игр… за последние 45 почти лет они все сертифицированы так или иначе", so it can be gathered into a library other people reuse for reskins — "когда мы игру просто берём и меняем арт"; as he understands certification, a reskin keeps the certified maths and framework and only the art changes, so GLI should not charge much for it [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].
- **The flow.** "Разработчик выбирает модель, описывает, что, как он хочет, чтобы эта модель выглядела"; an AI agent generates the visuals over several rounds the developer checks; the platform runs tests; the developer submits the reskin for certification, and once certified it is a finished game to ship — to a machine, or JVL could host it [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]] [[raw/Meeting_Notes_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].
- **Market and pricing.** He quoted a statistic that online casinos in the USA and Canada grew about seven times faster than land-based over some ten years, and a cut or subscription model — then: "Не обращайте внимания на цифры. Это всё абсолютно из головы выдумано" [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].
- **The closest product.** "самые близкие это стейк энджин" (Stake Engine, heard) — he registered the day before because Claude named it as the closest; it makes you upload your own maths and gives an SDK, so it needs more engineering than his mock-ups, where a developer starts "в один клип" (heard; read as "one click") [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].
- **His real aim.** He "вообще не хотел говорить про бизнес" — it interested him as engineering; even if the platform has no business value, "я всё равно хочу отсюда потянуть. Некоторые подходы для студий внова 2", e.g. agentic development and agent-to-user interaction [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].

## The ruling — not for JVL

Val thanked him ("я благодарю вас за то, что вы поделили своими мыслями") and gave "только свою точку зрения": JVL is not in the online market today (heard "JV lis not pozet сегодня онлайн маркет у нас"), "я никогда не не смог сделать деньги в онлайн рынке, поэтому… Для меня это не представляет интерес". It is not a bad idea — in other hands it might work — but given to others, "скорее всего, они быстрее свое сделают и обойдут нас" [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]]. The notes record it as decided by Val: the creator platform for the online market is not pursued [[raw/Meeting_Notes_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].

## Where Val is going instead

- **Why now.** The hardware JVL makes, its own module now on the machines ("Свой модуль на машины"), and the move away from the casino business to the street business ("ушли из казино бизнеса… Переключаемся на стрит бизнес") mean "Я хочу их отправлять прямо на машину" — Anton: the remote update the team is working on; Val: "Да" [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]]. Street means not in a casino: game rooms or bars [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].
- **The loop.** A machine on location should have enough "щупальниц индикаторов" (probes) that tell "Что пользуется популярностью? Что работает, а что не работает на текущей машине на текущем сетом"; the data goes to JVL, a new game is made automatically and sent to the machine "С минимальным участием… Людей". Example: eight games on a machine, with probes on which buttons the player uses and which features he likes — "даже есть такая мысль поставить, куда его глаза смотрят на экран" — plus maybe mathematical or physical methods. The result may be a reskin, or, if the player leans toward some mechanic, an experimental extra mechanic sent to the machine [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].
- **The GLI step.** Anton asked whether the game goes to GLI first. Val: yes; because there are different sectors (heard "разные секторы, которые подписаны его с игначу" — **unclear**), JVL tells GLI what changed, GLI approves for that sector, JVL receives the approval with its checksums and sends the game to the machine; the machine reports its checksums, they are checked against the approval, and the game is enabled — "это все естественно, должно делать автоматически" [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].
- **Already on the way.** The mock-ups "Игорь и женя" showed go partly in this direction, as does using AI to reskin games [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]]. Reading "Игорь и женя" as [[wiki/people/igor-metelski.md|Igor Metelski]] and [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] (their AI teardown and design-assistant work) is an **inference** by context.
- **"Вот это направление, которое я бы хотел бы освоить"**; "я бы хотел бы. Проработать вот эту вот архитектуру" [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].

## The unsolved part — what do players like?

"Одна из самых больших трудностей… как правильно оценить, что игроку нравится, что не нравится?" Val knows the bet level, "Но я не совсем понимаю, что с этим делать". Making a game, even its maths, is now possible "с минимальными затратами" in full or mostly automatic mode; what he does not know is which statistics to take and what they mean. Example: of eight games two are popular — is it the mechanic or the theme? If the same mechanic with another theme is not popular, is it the theme, the mechanic, "Или математика непопулярная"? "раньше думал, что сделать игру самое сложное"; now the hard part is the right statistics [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]]. Still, "я знаю, что мы двигаемся правильно": no one else can do it yet, because "машина должна иметь модом" (heard; the module) and the games must be made fast — "Пока не вижу, чтоб компашин мог это сделать" [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]].

## How it sits against earlier rulings

- **Online.** It repeats the July-2025 step back from online — [[wiki/decisions/2025-07-15-exit-online-focus-transactional.md]] · [[wiki/topics/online-games-rgs-distribution.md]] (Nov-10 2026 note).
- **Automatic games.** It carries Val's Nov-2025 "generate games from a specification" endgame one step further, from making games to choosing them from machine data — [[wiki/topics/game-production-throughput-strategy.md]] (Nov-10 2026 section).
- **Remote update.** The "send it straight to the machine" step is the remote-update work Anton named — [[wiki/decisions/2026-10-30-nova-remote-update-is-nova-only-and-texas-first-and-the-full-architecture-is-written-before-the-mvp-split.md]] (the link is drawn here — **inference**).
- **Certification.** The automatic GLI approval by checksum is a new idea against the GLI cost and delay theme — [[wiki/topics/gli-certification-bottleneck.md]] (Nov-10 2026 note).

## Open commitments

- [ ] [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] — look at what player statistics can be collected and how to process them for the telemetry-to-new-game loop ("Я ну посмотрю на досуге что можно собрать") — due unspecified — [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]] [[raw/Meeting_Notes_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]]

## Open questions

- From machine data, how does JVL tell whether the mechanic, the theme or the maths makes a game popular, and which statistics should it take? (Val: "не решённая проблема") — [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]] [[raw/Meeting_Notes_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]]
- How would GLI's per-sector approval with checksums work in practice (heard "секторы, которые подписаны его с игначу")? — [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]]

## Note, Nov 11 2026 (7:31 AM) — Val gives the loop to the whole NOVA 2 group and asks which metrics NOVA and Galaxy must collect

- **To the group, as confidential.** At the end of the [[wiki/meetings/2026-11-11-nova-2-mechanics-placement-one-studio-tool-and-game-metrics.md|Nov-11 NOVA-2 follow-up]] (Russian) [[wiki/people/val-levitan.md|Val]] asked everyone to keep it "довольно конфиденциал" and painted the same loop: machines with, say, "6 игр" report through the modem what is popular; "Дизайнеров нету. Игра делается сама"; the lab returns it with a checksum ("сам чек" — heard); it goes back to the machine and plays — "Это делается за неделю" [[raw/Meeting_Transcript_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026.md]] [[raw/Meeting_Notes_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026.md]].
- **The question for Tuesday.** "Какая статистика нужна для геймдизайнера?… Скорее всего, этот вопрос прежде всего ефим"; build NOVA and Galaxy so the data comes out in the needed form — "Какие сенсоры?" ([[wiki/people/pavel.md|Pavel]]: "Метрики я бы назвал это метрики") [[raw/Meeting_Transcript_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026.md]].
- **First ideas on the open question below.** Pavel: time in a game before the player switches. [[wiki/people/efim-podvoiski.md|Efim]]: relative popularity first, under equal conditions; retention matters most, but "мы не знаем, что это тот же человек вернулся"; collect many metrics and let a neural network look for correlations. Pavel's QR code on a win of "$20 и выше" to link a player's phone; Efim doubts players would use it [[raw/Meeting_Transcript_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026.md]]. The question stays open; details on [[wiki/decisions/2026-11-11-nova-2-gets-one-tool-from-brief-to-game-igors-scene-flow-goes-into-the-studio-the-ai-model-is-a-replaceable-setting-a-tuesday-demo-and-where-mechanics-live-stays-open.md]].

**§15.8:** clear — no named-person pay. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]]
- [[raw/Meeting_Notes_JVL_Creator_Platform_Idea_and_Player_Telemetry_Game_Loop-November-10-2026.md]]
- [[raw/Meeting_Transcript_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026.md]]
- [[raw/Meeting_Notes_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026.md]]
