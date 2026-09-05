---
type: decision
title: Consolidate over-granular capabilities by giving Claude an administrative direction (roughly twenty capabilities per product, ~8 requirements and ~8 features each) — not an architectural one
date: 2026-09-03
aliases: [administrative direction to Claude, 54 capabilities for LGS, capability granularity, twenty capabilities per product, consolidate capabilities in five minutes]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# Consolidate capabilities by giving Claude an administrative direction

At the [[wiki/meetings/2026-09-03-nova-prose-standard-skills-and-module-contracts.md|Sept 3 2026 follow-up]], [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] reported the capability counts his skill produced and [[wiki/people/irina-shishko.md|Irina Shishko]] objected that they are not capabilities at all. Val's answer was procedural rather than architectural [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].

## The numbers, and the objection

- **LGS produced 54 capabilities; the Recycler, 34.** Vladimir: "Для LGS у меня получилось набор из 54 кополити"; and "для рисайклера проекта, который… меньше л г с[,] тополити 34 на данный момент то есть разница не такая большая." Pavel's immediate reaction: "Немало" (that is not few); Irina's: "У меня были такие же глаза" [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].
- **Irina: 54 is over-granular, and these are not capabilities.** "то, как сейчас написаны каппобилити. Вот их как сказали 54 это что то очень сильно разбитое. Эт это не копобилити." Her worked examples: "выдать и перепечатать бумажный ваучер это как побилити или погасить вставленный ваучер это кай побилити ну это же не как побилите" — issuing and reprinting a paper voucher, or redeeming an inserted voucher, are not capabilities in her view [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].
- **Pavel's counter: LGS really is that big.** "lg s действительно огромный проект, и там много составляющих. Может быть 50 это и нормально для такого проекта." Vladimir said the same of LGS's size; Irina attributed the Recycler's count to an "Андрей" having broken it down very finely when he wrote it ("Андрей уж очень размельчил, когда писал") — which Andrei is not stated, left unresolved per §4 [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].

## What was decided

- **Give Claude an administrative direction, and it will consolidate.** Val had hit the same problem writing his own prose (correcting himself mid-sentence about the authorship: "И не я это писал, а клод давайте. Правильно будем называть вещи своими именами" — Claude wrote it, let us call things by their proper names). "У меня тоже получилось 1 раз, много кей побил эти[,] я специально потом вернулся и рассказал клоду. Наш поход, как мы работаем административно" — he went back and explained how JVL works administratively [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].
- **The direction he gave, verbatim in shape:** capabilities sit "довольно высокого уровня"; "я к лоду сказал, что я приблизительно ожидаю описать продукт гдето в двадцатикейтис" (the transcript runs "twenty capabilities" together as one token); "на каждый ей побед им будет приблизительно, с одной стороны, 8 реклайментов в среднем… и со стороны девелопера будет где то 8 фьючерс. Плюс минус" — about twenty capabilities per product, roughly eight requirements and about eight features per capability, plus or minus. Result: "Стекло построился очень удобно" [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].
- **He named the kind of instruction it is.** "вы можете к лоду запросто запросто поставить вот такой административные дирекшен… и описать его как… не архитектурный подход, а административный подход" — an administrative approach, not an architectural one [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].
- **The consolidation is cheap.** "даже хьюман может то же самое взять 54 кей победить и тоже сузить это, а для Клода это просто вот… 5 минут работы" — five minutes of work for Claude [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].
- **The tidied capabilities then move into Jira, and the new Jira structure is built.** Irina: the capabilities currently sit in a document in GitHub "но мы их хотим видеть в жира… их причесать и нужно переносить вот[в] жира." She placed it in the sequence started earlier: "мы какое то время начали уже в джири там создавать новую структуру, копобилити, привязка рекламентов… Ну гдето там дима ушёл в отпуск, наверно к этому можно возвращаться… под новую структуру джиры строить, и это LGS может быть следующим проектом." Val agreed but rejected her framing as too soft: "вы очень както мягко к этому подошли. Я как бы более жёстко на это смотрю, что без этого невозможно" — he sees it as impossible without [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]. (Which "Dima" started the Jira structure is not stated — left unresolved per §4.) This continues the ownership set on [[wiki/decisions/2026-08-26-pavel-irina-own-nova-capabilities-to-jira-through-september.md]].

## Note on a derived-note conflation

Val used *two different* capability counts in the same meeting, in two different arguments, and they should not be merged:

1. In his **illustrative walkthrough of the correct business order** (see [[wiki/decisions/2026-09-03-acceptance-criteria-settled-by-experiment.md]]) he used **ten** capabilities: "вот этот продукт… имеет вот 10 кейпопилотис… у нас есть 80 рекламенс, которые подсоединены к этим 10 по пилатис" — ten capabilities, ~8 requirements each, ~80 requirements [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].
2. In the **administrative direction he actually gave Claude** he used **about twenty**: "описать продукт гдето в двадцатикейтис" (the transcript runs "twenty capabilities" together as one token) with ~8 requirements and ~8 features each [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]].

The derived meeting note merges these into a single "twenty capabilities… roughly eighty requirements" [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]. The transcript figures above are the ones recorded here.

## Open commitments

- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/pavel.md|Pavel Frolov]] — tidy the capabilities, move them into Jira and build the new Jira structure, with LGS as a candidate next project (resuming the structure "Dima" began before his holiday) — due September 2026 — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]] [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Open questions

- Whether 54 capabilities for LGS is over-granular (Irina) or reasonable for a project that size (Pavel, Vladimir). Val's administrative-direction instruction is the proposed remedy, not a settled answer — [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]] [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Sources
- [[raw/Meeting_Notes_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
