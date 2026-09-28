---
type: decision
title: The games-conversion experiment closes in a couple of days — standards go to the knowledge repository, ADRs sit with the code, and the converter gets its own Jira project and repository
date: 2026-09-25
aliases: [experiment closes, свернуть законсервировать, converter own repository, конвертер имеет файнайт срок жизни, finite life converter, tools folder, каталог тулз, ADRs next to code, standards folder in knowledge, RAGE to NOVA conversion capability, NOVA Gaming Platform Land-based initiative, two projects game conversion and geometry standard, repositories first then Jira project, раньше яйца потом куры, retroactive capabilities, acceptance criteria only basis for E2E tests, zero trust autonomous repository, data contract, Wednesday Sept 30 7:00]
source-count: 2
status: active
open-commitments: 7
open-questions: 3
---

# The games-conversion experiment closes; the converter gets its own project and repository

Set at the [[wiki/meetings/2026-09-25-games-conversion-repos-jira-capabilities.md|Sept 25 2026, 9:02 AM session]] (Russian), chaired by [[wiki/people/val-levitan.md|Val Levitan]], on questions [[wiki/people/igor-metelski.md|Igor Metelski]] brought from his RAGE→NOVA and horizontal→vertical experiments. It carries on from [[wiki/decisions/2026-09-20-the-vertical-geometry-standard-glossary-and-adrs-go-to-github-outside-any-framework.md]] [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

*(Quotes are from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## What Igor brought

From the experiments he made a glossary, a list of ADRs, and a document of art requirements — "по геометрии элементов и по тайминго таймингам элементов". Claude also wrote tools along the way: a converter (for the Dragon Pays experiment it "лежит в dronpass") and small scripts such as one that takes screenshots. His question: the standard says a repository's documents describe that repository only, but the conversion work must point at RAGE data [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

## What was decided

**1. Glossaries and standards go to the standards folder of the `knowledge` repository.** Val: "Стандарты, голоссарии, стандарты нужно вложиться… стандарт репозиторий"; Bosik named it ("К ноу ли черепозиториям называется"), and Val: the repository is "нолочь" with a folder "Которая называется стандарты". Pavel: for Claude it is simpler in one place — "он не будет распылять свой мозг" [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

- **The geometry standard too — Val's view, not certain.** Pavel: "он выглядит как отдельная какаято группа… я не не уверен на 100%". Val: "я тоже не уверен на 100%, но чувства у меня что это стандарт". He would not add another folder: "лучше переборщить стандарта, чем разбавить", and "я довольнотаки гибкий"; consult internally [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].
- **Keep it in Markdown.** Igor planned to split text (md) from graphics (HTML). Val: "я вам не советую… я бы вам просто графику посоветовал перевести в момент" ("в момент" read as md; **inference**) — easier for Claude, and Markdown converts to any format. Igor: "Хорошо" [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

**2. ADRs sit next to the code.** Bosik: documentation "не должна быть оторвана от от продукта"; what concerns one game goes into that game's repository, with links to its SVN repository. Val: "Татьяна татьяры должны лежать рядом с кодом" — read as "ADRs must lie next to the code" (**inference** from a garble). What concerns the NOVA framework — and, Bosik and Pavel agreed, the conversion procedure — goes into the framework repository. Pavel: put a link to SVN in the ADR, "а в с в н ничего не комитить только в гид" [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

**3. The converter gets its own Jira project and its own repository.** Igor first wanted it inside each converted game's repository, since games differ; Bosik agreed and Pavel disliked a separate repository for a tool that changes per game. Irina asked whether the converter is needed after a game is converted; Igor: no. Bosik: if 10% is reusable it is not universal, if 90% it is; Irina: "80 70 это тоже достаточно универсально". Val's ruling [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]:

- "конвертор имеет файнайт… Срок жизни"; it should not tangle with the main code "во фрейнборке".
- "я это труит как отдельный дочер под отдельным номером проекта с отдельным репозитором… удобно работать, и нам это удобно потом похоронить." (a separate item under its own project number with its own repository)
- Pavel agreed: a developer on a new game tells Claude where the conversion repository is, "и всё он скачает всё".

**4. Small scripts go in a `tools` folder of the repository they serve.** Igor did not want a repository per script. Pavel: "я создавал каталог тулз"; Bosik: "я тоже туз сделал каталог". Igor: "тогда вопрос снимается" — the screenshot script lives in the converter's tools [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

**5. The experiment closes.** Val: "эксперименты себя доказали положительно"; "Еще как бы пару дней, и он закончится. И всё надо свернуть законсервировать" — spread the results into the right repositories, document them, add the new standards, write prose. Converting real games is "совершенно другого рода" work: a separate project with a schedule of tasks, assigned resources and a calendar. Igor: one item is left, the end-to-end tests built on the capabilities; Val: "Безусловно, Я согласен" [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

**6. Capabilities are closed retroactively, from today's code and prose.** Igor has draft capabilities locally, not yet in Jira, which may need updating. Val's order: write prose for the code, go back to the capabilities, attach requirements with acceptance criteria (including non-functional), and close the capabilities as done "задним числом" — "Как обычно". Igor: "Мы хотим это честно сделать в джире"; Val: "Конечно". Acceptance criteria are "Единственная точка опоры для автоматических and n тестов" (read as end-to-end), and prose "хорошо очень интегрируется" with them [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

**7. One initiative, one capability, two projects.** Val admitted "я лично путаюсь" on initiative vs project. [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]]: "Проект равно репозиторию"; reading the standard, an initiative is a long direction with several releases and "будет объединять несколько проектов"; initiative → capabilities → features, and "фичи… лежат в проектах". Pavel pointed to the existing initiative "снова геймин платформ лэндбэйст" (NOVA Gaming Platform Land-based) and, under it, the capability "речь что нового конвершен" (RAGE to NOVA conversion). Val: under it, two projects — game conversion ("как конвертировать с этого на это") and "новый стандарт разработок, опираясь на геометрическое расположение объектов на экране". Igor asked about a third, RAGE-to-NOVA project; Val kept all conversion in one [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

**8. Repositories first, then Jira projects.** Val: Kovalchuk opens the two projects, Andrei the repositories (by context Bosik; **inference**). Kovalchuk: "Сначала репозитории создаем. Потом проект", because Jira project names match repository names. Val asked for this to go in the standard ("Раньше яйца, потом куры"); Pavel: "Она внесена уже" [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

**9. Each repository stands alone.** Val: "припозитории должен быть зеротраст и полностью автономный" and carry its contract — Pavel: "ДЕЙТА controtroct" (data contract). Prose lives in the repository, next to the code [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

**Next meeting: Wednesday Sept 30 2026 at 7:00** (time zone not stated). Igor asked for a week; Val: "неделя больше не считаю" — "В среду в 07:00", checking "среда, это что? А это 30". Igor asked for a point-by-point list; Val will put the transcript in the meeting for Claude to parse [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

## Relation to earlier rulings

- **Sept 20** put the work "in a vacuum", outside any framework. Sept 25 keeps standards and glossary outside the frameworks, but places framework and conversion-procedure ADRs in the NOVA framework repository and game ADRs in game repositories. This refines the Sept-20 ruling; see its Sept-25 update.
- **Sept 3** gave a standard one location, the standards folder of `knowledge` — [[wiki/decisions/2026-09-03-prose-standard-into-knowledge-repository.md]]. Point 1 applies the same rule.
- **Sept 24** said capabilities sit in one flat list under each platform — [[wiki/decisions/2026-09-24-capabilities-sit-in-one-flat-list-under-each-platform-and-releases-are-timeline-lines-not-initiatives.md]]. The initiative Pavel named is the one kept there as the NOVA land-based platform.
- **Aug 28** asked Igor to reverse-engineer requirements and acceptance criteria from Dragon Pays — [[wiki/decisions/2026-08-28-reverse-engineer-acceptance-criteria-and-automate-qa-dragon-pays.md]]. Point 6 is the same method, now for Jira.

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] (by context) — create the repositories for the two projects, including the converter's — due before Wed Sept 30 2026 — [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — open the two Jira projects under the RAGE-to-NOVA conversion capability, named to match the repositories — due after the repositories exist — [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — split his one ADR list by topic (tools, framework, specific game) and commit each part to its repository — due Wed Sept 30 2026 — [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — commit the glossary and standards, including the geometry standard with its graphics in Markdown, to the `knowledge` standards folder — due Wed Sept 30 2026 — [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — write prose in each repository next to the code — due Wed Sept 30 2026 — [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — update the draft capabilities, put them in Jira with requirements and acceptance criteria (including non-functional), close them retroactively, and finish the flow up to E2E tests — due Wed Sept 30 2026 — [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — put the transcript into the meeting so the team can have Claude list what must be ready — due unspecified — [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]

## Open questions

- Is the geometry document a standard (standards folder) or a group of its own? Pavel and Val are both "не уверен на 100%"; left for internal consultation — [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
- The names of the two projects and their repositories were not set on the call — [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
- Is "repositories first, then Jira projects" already in the standard? Pavel says yes; Val asked for it to be added — [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]

*The derived notes give the same rulings; where they differ (the early converter positions, the repository owner, "omni") the transcript is followed — see the meeting stub [[raw/Meeting_Notes_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].*

**§15.8:** personal remarks withheld (see the stub). **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
- [[raw/Meeting_Notes_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
