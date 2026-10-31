---
type: decision
title: Confluence is not a source of truth for the game agent — only code is; old games get a one-time Claude-built wiki page each, made from the real SVN code and sized to answer Igor's specification; the old SVN code itself is not moved into GitHub or the agent, and universality is built step by step in new, clean code; on Oct 29 Igor showed the method on Clover Fortune and the wikis are to be loaded into the company second brain (Oct 24 2026)
date: 2026-10-24
aliases: [code is the source of truth, Confluence is not a source of truth, конфлюенс не является source of truth, SVN to wiki, per-game wiki from SVN code, old games wiki, Karpathy wiki for old games, no SVN in GitHub, clean code step by step]
source-count: 4
status: active
open-commitments: 1
open-questions: 2
---

# Code, not Confluence, is the source of truth; Claude builds a wiki per old game from the SVN code

Set at the [[wiki/meetings/2026-10-24-ai-game-design-assistant-first-pass-and-code-as-source-of-truth.md|Oct 24 2026 first-pass review of the AI game design agent]] (Russian). [[wiki/people/andrey-bosik.md|Andrey Bosik]] proposed the wiki job; [[wiki/people/val-levitan.md|Val Levitan]] agreed; [[wiki/people/pavel.md|Pavel Frolov]] agreed on the old code [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]] [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]]. The agent it serves: [[wiki/decisions/2026-10-18-evgeny-kharetski-owns-a-voice-ai-game-design-assistant-with-a-first-pass-reviewed-oct-25.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## Part 1 — the old SVN code stays out (about 00:24–00:28)

- **Why it came up.** [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]]: Val had mentioned connecting the game repositories to the agent's "brain", but NOVA has almost no games yet, and the older games cannot be reached — the agent is in the Amazon cloud and the games sit in SVN on the local network [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]].
- **The size.** Val thought converting SVN to GitHub is not that big. [[wiki/people/igor-metelski.md|Igor Metelski]] keeps a local git copy of the SVN repository; Claude set it up for him in about half an hour. Its size: "6 55" — 6.55 GB, for six games (Irina: "На 6 игр"). Val: even 50 games would be about 30 GB [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]] [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]].
- **Not needed now.** Pavel: "Я думаю мы мы быстрее наполним гитовские репозитории новыми играми" and Claude does not need the old code. [[wiki/people/irina-shishko.md|Irina]]: "больше мусора будет." Bosik worried about making a mess. Kharetski: he does not yet see why the agent should know game code — that comes when the new engine has a flexible MCP so agents can assemble scenes themselves [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]].
- **Val's ruling.** "давайте не разводить мусор, давайте в новом и постепенно достигнем степени универсальности… в чистом коде, чтобы мы понимали, откуда ноги растут". Pavel and Bosik: "Да" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]].

## Part 2 — Confluence is not a source of truth (about 00:35–00:41)

- **Val's point.** While the agent was answering from the Confluence game cards, Val stopped the demo: "конфликт не является сорсов… Сорсов чувств это, в общемто код исполнения игры. И математика." Kharetski: Confluence at least describes a game's style. Val: it carries big errors; "Наши дизайнеры не поддерживают конфунс настолько скрупулезно, сколько код"; a replaced symbol not changed in Confluence goes unnoticed. "Код это сортов чус, ничего другого не существует." [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]] (The speech-to-text renders "Confluence" as "конфликт", "конфунс" and similar.)
- **Igor's caution.** Moving SVN to git would be good, but the Rage framework is "такой большой Монолит" holding all bonuses and rules; a game is a small set of files using it, and from the code alone it is not always clear what a game takes from the framework — it may also depend on settings that come from the data center. "я не не могу гарантировать, что… существующий [Rage] игры… могут быть достаточным… источником истины… для агента." [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]]
- **Val.** Confluence can be "абстрактный рефресс" (an abstract reference), not a source of truth; Igor: "Просто нас получается другого нету." Val: he is not arguing, only noting for the meeting that Confluence is not the source of truth; "мы так и систему строим, что для нас сорсу это только код" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]].

## Part 3 — the one-time wiki job (about 00:41–00:45)

- **Bosik's proposal.** "мы не хотим грузить с в н в гетхаб ни в коем случае"; instead ask Claude, on its own, to go into the SVN and build a document for each existing game, then load that pack into the agent — so it rests "не напрямую на код, но на описание, которое было сформировано, исходя из реального кода игры." [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]]
- **Like Karpathy's wiki.** Val: "это типа… как… Андрей карпаты строит свой вики." Bosik: "Да." [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]]
- **Compare or drop Confluence?** Pavel: generate prose per game and compare it with Confluence to show where Confluence is wrong. Bosik: do not compare — remove Confluence as a knowledge source and keep only what is built from the SVN games. Val: "Я бы тоже так сделал" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]]
- **Form and scope.** Bosik: not necessarily prose — Claude picks its own format per game, a folder with a text description and any pictures or scenes it needs. It is done once, because no more games will be released on SVN/Rage ("я так понимаю"), giving a wiki archive of all old games and products [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]].
- **Val's test for the output.** It must answer Metelski's specification: "ты должен иметь информацию, которая может ответить на митейского спецификации… Тогда у нас были правильные размеры, правильная геометрия, правильные… Sambells [symbols]." [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]] The spec: [[wiki/decisions/2026-10-18-igors-spec-becomes-a-creative-direction-specification-for-game-designers-and-the-word-re-skin-is-dropped.md]].
- **A scope gap, found early.** Kharetski: this changes the direction a little and the job has to be done first. Val: "мы не поменяли направления мы нашли… скоб гад [scope gap] который потом бы нам… Повредил бы, а сейчас нормально." For the rest of the demo they treated Confluence as if it were right [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]].

## How it sits against earlier rulings

- It applies the long-held "only what is in git is the source of truth" line ([[wiki/topics/docs-as-code-and-atlassian-exit.md]]) and the code-to-prose method ([[wiki/decisions/2026-10-08-an-ai-chief-system-architect-maps-galaxy-and-nova-from-code-prose-and-data-contracts-to-find-gaps-as-bosiks-next-objective.md]]) to the game agent's knowledge of old games (**inference** — the link is not drawn in the meeting).
- "No more games on SVN/Rage" was Bosik's understanding, said in passing; the Rage closure itself is [[wiki/decisions/2026-10-18-rage-is-closed-dutch-mill-reaches-nova-by-wednesday-and-a-reskin-from-a-new-theme-tests-the-tools.md]].

## Update, Oct 29 2026 (6:59 AM) — Igor's Clover Fortune test; the wikis go into the second brain

At the [[wiki/meetings/2026-10-29-ai-game-design-assistant-review-one-knowledge-base-and-a-full-cycle-test.md|Oct-29 second review of the game design agent]] (Russian) [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]:

- **The experiment.** [[wiki/people/evgeny-kharetski.md|Kharetski]]: after the last meeting [[wiki/people/igor-metelski.md|Igor]] ran an experiment showing that the same design document the agent produces can be built "по… Любой старой игре", with the palette and graphics pulled from the game's repository; so instead of moving heavy Rage into git, "мы просто можем в вике и библиотеку собрать из таких документов по всем играм, которые нас интересуют старым" and load it into the second brain or into a GitHub repository connected to it [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **What Igor did.** He showed Claude the brief Kharetski's tool had generated and asked for the same brief for the existing Clover Fortune. Claude broke down the game's idea, tone and style, palette and motifs, wrote the screen parameters to the specification, and pulled out references that really sit in the game's repository [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]. A gap in one cell was the expanding symbol, which is a video; Claude did not take the video apart, but would have if asked. Symbol cells looked uneven because Claude took the real texture sizes, while in a Rage scene the scale is set on the cell object [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **Layouts for the wiki.** Igor: the new-game brief uses vertical layouts, but in the repository the game is horizontal, so for the wiki that would mislead; Claude can be set to measure the real scenes and show the actual layouts. Kharetski: "для вики это честнее"; a vertical version can be made later from the wiki document [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **The full screen.** Igor: the screens are taken apart one by one, but Claude can be asked to assemble the full game screen, as the instructions are there. Val: "Да, я бы собрал, но весь экрал [экран]" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]. No one took this on in words; the notes list it for Igor, flagged as needing Val's confirmation [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **The run.** Kharetski: an automated process "запускается одним бронтом [промтом]" and runs "там день"; Igor: only the template — what the document should show — must be set; Kharetski: "Отладить промт". Claude can fetch the SVN locally for the time it needs and then delete it, so SVN need not be downloaded first. Kharetski on run time per game: "это скорее может Игорь сказать" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **Why it is current.** Igor: it will be like Confluence, but whether Confluence was kept up "уже никто не вспомнит", while the SVNs hold the production versions of games, "поэтому их состояние ну по любому актуальное" — the game code, the action graphs used for animations, and the resources: textures, screens and the rest [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **Which games.** Kharetski: pick a package of games actually needed — "например, нам нужны все гекамы" (as heard; **unclear**) — and not the very old ones; "Алгоритм у Игоря есть он уже это делал" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]. Val: the wikis of past games "которые мы выберем" go into the game design agent's second brain — [[wiki/decisions/2026-10-29-the-company-second-brain-is-the-one-knowledge-source-for-all-ai-agents-with-access-limited-per-agent-and-the-game-design-agent-sees-game-knowledge-only.md]].
- **Recorded as a decision.** The notes: build the old-game wiki from SVN code with Igor's method and load it into the second brain (Kharetski's recap, no objection) [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]. Still no owner and no date.

## Open commitments

- [ ] Unassigned (Bosik proposed; Val agreed; no owner named) — one-time job: Claude builds a wiki page per old game from the SVN code, sized to answer Igor's specification; Confluence is then removed as the agent's knowledge source — due unspecified — [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]] [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]] — *Oct 29 2026: method shown by Igor on Clover Fortune; the output is to be loaded into the company second brain; still no owner* — [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]

## Open questions

- Can old Rage game code alone fully describe a game, when the framework is a monolith and behaviour also depends on data-center settings? (Igor) — [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]]
- Who runs the SVN-to-wiki job, and which games go in? No owner was named on Oct 24; on Oct 29 Kharetski said to pick a package of needed games and that Igor has the algorithm, but still no owner and no list — [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]] [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]]
- [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026.md]]
- [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]
- [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]
