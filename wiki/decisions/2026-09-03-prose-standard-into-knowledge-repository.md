---
type: decision
title: The prose standard has exactly one location — it moves out of the LGS repository into the `knowledge` repository's standards folder, and the prose skills move into the Claude Code configuration
date: 2026-09-03
aliases: [one location for a standard, prose standard in knowledge repo, knowledge repository standards folder, prose skills into Claude Code config, Val's single-location rule]
source-count: 4
status: active
open-commitments: 3
open-questions: 1
---

# A standard has exactly one location: the prose standard moves into the `knowledge` repository

The [[wiki/decisions/2026-08-24-single-prose-writing-standard.md|Aug-24 ruling]] asked [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] and [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] to author one prose-writing standard and put it in the standards repository. At the [[wiki/meetings/2026-09-03-nova-prose-standard-skills-and-module-contracts.md|Sept 3 2026 follow-up]] Vladimir reported the standard was written — and that it was sitting in the LGS repository. Val's reaction was the sharpest moment of the call [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].

## What was built (and where it was)

Vladimir assembled a single standard "из митингов из обсуждений из работ, который делал я женя Антон" — from the meetings, the discussions, and the work he, Zhenya ([[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]]) and Anton had done — plus prose already written (the transcript garbles what that prose was for: "из розы, которую для лудимы"; the derived note renders it as the prose written for LGS). His stated test: a standard "который бы устраивал всему тому, что мы обсуждали, что мы находили и что делали" — one that satisfies everything the team had been discussing, finding and doing [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]] [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].

Asked directly by Val whether it was already in GitHub, Vladimir answered: "Пока он есть в репозитории, пока л г с, потому что л г с пока как пилотный проект для прозы… На нём проводились большинство экспериментов" — it is in the LGS repository, because LGS is the pilot project for prose and most experiments ran there [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].

## What was decided

- **A standard has exactly one location, however unfinished it is.** Val: "Если на сегодняшний момент у нас есть какоголибо стандарта, даже если он слабенький, он не закончены в какойто начальной форме, у него может быть только единственный loation, единственный он не может гдето лежать в стороне сбоку сзади в другом репозитории мне удобно, мне неудобно" — it cannot sit off to the side in another repository because that is convenient for someone. And: "Да, он будет развиваться. Да он будет меняться, Я согласен с этим. Но в другом месте он не может лежать" [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].
- **The repository is `knowledge`, with standards as a folder inside it — Pavel's correction, accepted.** Val had named the "standards" repository; Pavel: "поправка репозитора не называется. Нестандарты репозитории называются нолич. И там есть папка стандарт" (the repository is not called standards, it is called *knowledge*, and there is a standards folder in it). Val: "Спасибо за поправку, согласен с этим" [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]. This corrects the loose "standards repository" wording carried on the [[wiki/decisions/2026-08-24-single-prose-writing-standard.md|Aug-24 decision]] and the [[wiki/decisions/2026-08-28-reverse-engineer-acceptance-criteria-and-automate-qa-dragon-pays.md|Aug-28]] standing rule.
- **Company-wide access to `knowledge` is to be granted.** Vladimir does not expect to have write rights ("если у меня есть права на Добавление или запрашиваю"); Pavel agreed he probably does not, and took the action: "надо Андрею написать письмо, что дать компани вайт акцесс всем. В репозиторию ноль[ич]." Val offered to write it himself; Pavel: "давайте я напишу." Irina offered Vladimir the link ("Я тебе сброшу это самое ссылку") [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].
- **The prose skills move into the Claude Code configuration when Vladimir finishes**, so every developer runs the same version and everyone receives updates. Vladimir, reporting a conversation with "Андреем" the previous day: "вынесем в конфликт кода так, чтобы все разработчики пользовались одной и той же версией скилла и в случае доработок… все получали обновления и все пользовались одной той же описанием." Val added the standard to the same rule: "И обновлялся стандарт. Если мне чтото меняется" — Vladimir: "Да конечно" [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].

## Val's framing of why this keeps happening

He named it as a recurring pattern rather than a one-off mistake: "просто всеми фибрами своей души меня это раздражает"; "Я извиняюсь, если я разговариваю немножко раздражённо, но я действительно раздражён этим походом"; "И он постоянный, я никак его не могу поломать. Это уже в корне както зарыто" — the approach is constant, he cannot break it, it is buried at the root. The behaviour he is attacking is the one he stated back: "Мы не можем так думать, что вот у нас пока сегодня это не финальный вариант, и я пока не буду ложить. Я стесняюсь что может быть там чтото не доработано" [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].

## Aug-24 commitments this settles

- The **authoring** commitment is discharged (late against its ~Aug 25–26 due date, and the plan of record is unchanged — the standard exists as of Sept 3).
- The **placement** commitment is *not* discharged: the standard went into the LGS repository instead, and is re-tasked here to the `knowledge` repository's standards folder, blocked on write access.

## Open commitments

- [ ] [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] — move the prose standard out of the LGS repository into the `knowledge` repository's standards folder — due promptly; blocked on write access — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — send Vladimir the link to the `knowledge` repository — due immediately — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [ ] [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] — move the prose skills into the Claude Code configuration so all developers share one version and receive updates, with the standard updating alongside them — due on finishing — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]] [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## History

- [x] [[wiki/people/pavel.md|Pavel Frolov]] — write to "Andrei" asking for company-wide access to the `knowledge` repository — **DISCHARGED the next day.** At the [[wiki/meetings/2026-09-04-rage-nova-conversion-readiness.md|Sept-4 morning meeting]] Pavel posted the repository link into the meeting chat and noted Andrei was supposed to have given everyone access; Val confirmed it was done and checked person by person — "[Андрей] всем дал и проверил каждого аксес… он мануально сам всё это проверил **39 аксис**" (39 accesses, verified manually). [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]

## Open questions

- **How many prose skills there are.** On [[wiki/meetings/2026-09-01-nova-prose-qa-automation-check.md|Sept 1]] Pavel reported second-hand that Vladimir had built "3 разных скила" — three different skills for Claude — while describing two functions. On Sept 3 Vladimir, first-hand, said "самое ценное, считаю сделано 2. Скилла для клауд код" — two skills. Both recorded; not reconciled — [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]] [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Sources
- [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
