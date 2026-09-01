---
type: decision
title: Author one prose-writing standard from the best of the existing variants and place it in the standards repository; owners Vladimir Samusenko and Evgeny Kharetski
date: 2026-08-24
aliases: [prose-writing standard, single prose standard, prose standard in the standards repository, normalize existing prose with Claude, prose document structure]
source-count: 2
status: active
open-commitments: 4
open-questions: 2
---

# One prose-writing standard, authored by Vladimir and Evgeny, placed in the standards repository

At the [[wiki/meetings/2026-08-24-nova-lgs-prose-standard-checkpoint.md|Aug 24 2026 NOVA/LGS prose checkpoint]] (Russian), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] named the gap: JVL has a standard for writing **capabilities** and a rule that prose and ADRs live next to the code, but no standard for **how the prose itself is written** — "нету… Единого какогото стандарта, как мы пишем прозу и как мы пишемка били." [[wiki/people/val-levitan.md|Val]] agreed the standard is missing and said he is the wrong person to write it [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].

## What was decided

- **Pick the best of the existing prose variants and write it up as the standard.** Val's undertaking: "давайте тогда мы решим и возьмём как андритекинг, чтобы из всех вариантов прозы вы выбрали… Тот вариант, который вас больше всего устраивает и описали его… В стандарте" [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].
- **Place it in the standards repository, and point Claude at it thereafter.** Val: "Засеивали этот стандарт. При позитории… стандартов и в последующем мы всегда будем поинт клод. На этот стандарт он всегда просто будет писать одинаковый" [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].
- **Owners: Vladimir and Evgeny, with Dima Chudinov consulted.** Val: "я тогда могу оставить этот андротейкин для вас Владимир и для Евгения… вы, наверное, както соберётесь, наверное, привлёте диму чудинова, наверно, у него тоже есть какието мнения." [[wiki/people/pavel.md|Pavel]]: "чем больше людей здесь скажут свои замечания, тем лучше" [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].
- **Timeline: within a couple of days, and Val will be watching.** Val: "я тогда буду рассчитывать, что в течение пару дней стандарт прозы будет помещен в репозитории стандарта. Я за этим буду следить." Evgeny proposed meeting locally the next day: "мы завтра локальный митинг соберём, например, да вот выведем стандарт" [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].
- **Then run Claude over the existing prose to bring it in line.** Evgeny's plan: after the standard is set, take all the prose and capabilities already committed and "наталить клод на… стандарт… чтоб он их причесал, привёл к нужному виду," after which the standard can be handed to everyone who writes prose "чтобы у всех всё было одинаково." He wanted the standard first specifically to avoid doing the work three times: "чтоб сразу ну не делать 3 раза эту работу" [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].
- **Merge the two overlapping capability sets afterwards, not now.** Vladimir raised it: he and Evgeny described the same area from the front-end and back-end sides, so "сейчас они будут не пересекаться, а конфликтовать." Evgeny: standard first, "Дальше мы с тобой уже както… За колабём… Решим. Что куда, зачем и почему?" Irina and Val settled the shape: two prose documents, **one** capability set — Val: "просто будет 2 акипа будет один… побилась и будет одна, конечно да," because a capability later splits into front-end and back-end features. Val expects Claude can do the merge in "может быть не больше, чем полчаса" once it understands there are two sides [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].

## What the standard has to answer

Evgeny's list of open shape questions, which is what the standard is for [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]:
- "Нужны ли технические какието детали в прозе или не нужны?" — do technical details belong in prose or not?
- "Структура документа с прозе какая должна быть?" — what document structure? (Irina named the same thing: "Структура документа с прозой.") His reason: if each document is asked for separately the structures diverge; the code will still be understood, "но мне кажется лучше, чтоб всё было под одну ребёнку."
- "Как из этого потом правильно извлекать capolites" — how to extract capabilities from it consistently.
- Evgeny counted "условно 34 может даже 5 вариантов" — three, four, maybe five existing variants (Val's, Dima's, Vladimir's, Evgeny's) that can be reviewed to pick one [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].

## Val's position on writing it himself

- "Я с удовольствием буду придерживаться стандарта, но я мне кажется неправильный человек. Если попросить меня написать стандарт прозы, я, наверное, неправильно сделаю." Earlier: "я даже не знаю, как сделать из этого стандарт." Pavel offered a working definition — "это повествовательное, какоето написание, описание функционала" — and Val: "именно и есть слово проза написано как проза" [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].
- Val distinguished what already exists: for **capabilities** "помоему, у нас есть стандарт" (though he did not remember it well); for prose, "у нас стандарта, написание прозы нету" [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].

## Adjacent rulings restated in the same meeting

- **No code is committed without matching prose.** Val: "мы не можем камид код без Того, что сделано дейт прозы," and if code changes the earlier prose is replaced by new prose. Evgeny: "Такой план." Pavel refined the enforcement point — "Мы, мы можем кормить, но мы не можем пьер сделать" (you can commit, but you can't open the PR). Val agreed the CLAUDE.md file must state it. This hardens the existing prose-on-PR standard rather than creating it — see [[wiki/topics/github-release-management-pipeline.md]] [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].
- **Prose lives in a `docs/prose` folder in every project.** Pavel: "эта папка dox слэш проус… во всех проектах в папке док лежал папка проус," with the structure below it following the project's modules; Val agreed [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].
- **Capabilities and requirements (регламенты) live in parallel, not in a hierarchy; features sit under capabilities.** Val: "рекламенты живут параллельно они не живут в hy rark… Они не организованы по ступенькам." Pavel's practical consequence: "без копобилите мы не можем фичи отобразить на плане, а без регламентов можем" — without capabilities you cannot show features on the plan; without requirements you can. Val will press the product managers to attach requirements to capabilities ("я надавлю на продакменеджерсе") [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].
- **Bugs found while writing prose are recorded in place, not fixed now.** Val: "давайте сейчас не будем лезть в баки… мы не должны фокусировать наш ещё на… На багах" [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]].

## Open commitments

- [ ] Vladimir Samusenko, Evgeny Kharetski — meet locally to agree one prose-writing standard — due Aug 25 2026 ("завтра") — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [ ] Vladimir Samusenko, Evgeny Kharetski — place the agreed prose standard in the standards repository — due ~Aug 26 2026 ("в течение пару дней"); Val will monitor — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [ ] Vladimir Samusenko, Evgeny Kharetski — run Claude over the existing prose and capabilities to normalize them to the new standard, then merge the overlapping backend and frontend capability sets into one — due after the standard is set — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [ ] Evgeny Kharetski — work out with "Andrei" whether a repository rule can block a PR that changes code but carries no updated prose folder — due unspecified — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Open questions

- Can a repository rule actually block such a PR? Evgeny: "я не уверен, кстати, что такие ролса можно делать на репозит проведение, но это мы разберёмся." He also proposed testing it on one repository first — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **Which Andrei** is to be consulted on the PR rule is not stated. Irina said the docs-folder idea came from "Андрей" as its initiator and Pavel confirmed "Андрей там был," but no surname is given; the derived note flags the same ambiguity ("Which Andrei — Bockelie or Klimovich — is not clear from the transcript"). Left unresolved per §4 — [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]] [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Sources
- [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
