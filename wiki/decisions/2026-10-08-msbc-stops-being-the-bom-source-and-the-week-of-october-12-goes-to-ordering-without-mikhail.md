---
type: decision
title: The BOM will not stay in MSBC — MSBC keeps only financial and administrative data per vendor; the week of Oct 12–20 goes to making Nathan's BOM system work so JVL can order without Mikhail Perelman; the Texas BOM goes into BC now
date: 2026-10-08
aliases: [we will not leave it, MSBC stops being the BOM source, clean out MSBC, ordering without Misha, week of October 12, Texas BOM in BC, ten minutes, Hangzhou quote 100 300 1000, BOM standard pull request, part-number release standard]
source-count: 7
status: active
open-commitments: 7
open-questions: 3
---

# The BOM will not stay in MSBC; the week of Oct 12–20 goes to ordering without Mikhail (Oct 8 2026)

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-10-08-genadi-bom-standard-flex-slim-metal-mikhail-hand-over-and-data-contracts.md|Oct 8 2026 3:59 PM alignment call]] (Russian) with [[wiki/people/genadi-peari.md|Genadi Peari]]. It is the next step on the thread sequenced at [[wiki/decisions/2026-09-23-the-bom-source-of-truth-is-the-latest-design-in-github-and-sync-runs-one-way.md]], after the Oct-5 rulings [[wiki/decisions/2026-10-05-hardware-follows-the-developer-repo-model-one-jira-project-one-repo-zero-trust-data-contracts-no-monorepo.md]] and [[wiki/decisions/2026-10-05-nathan-carver-runs-the-flex-pay-slim-bom-reverse-spike-and-flex-port-follows.md]].

## What was ruled

- **Genadi's offer: start now with the BOM in BC.** "Смотрите, райт нау, это уже все может работать. Автоматически. Если… не переносить белых материал из би си, если оставить как есть… Ничего не надо делать." Moving the BOM into GitHub "можно сделать степс." Later again: the system "бьютифули может работать автоматически. Если мы пока оставим в покое этот" [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]].
- **Val: no.** "Я не хочу с вами спорить, но мы не оставим. Это неправильно." Genadi: "я не говорю оставить. Я говорю, что можно уже запустить." Val: "Но это неправильно… Я просто не хочу спорить на эту тему" [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]].
- **Where MSBC ends up.** After the data contracts are done: "Потом мы вычистим мсбиси… Мы перестанем пользоваться им как сорсов для Белов материал. Мы туда загоним… Административно финансовые детали. Каждого из бендокс" — each vendor's administrative and financial details [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]].
- **The week of Oct 12–20.** Val: "Я хотел бы, чтоб мы сосредоточились на вот этой неделе, которая идёт. Чтобы закончить с нейтоном… Чтобы заработал весь этот биломатериал, как я хочу." And: "12 числа… 20 все усилия приложим к тому, чтобы заработало вот эта вот идея." Genadi's part is to test what Nathan builds and find what does not work [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]].
- **The goal of that week: ordering without Mikhail.** "Нам нужно попробовать подтянуть всё, вот это дело, чтобы мы без миши могли заказывать" — see [[wiki/decisions/2026-10-08-mary-takes-over-mikhail-perelmans-ordering-role-with-training-from-october-19.md]]. Genadi: "У нас все есть, Кроме билов, материал сорсов… Нам нужен иметь репорт?" Val: to have the report, "нужно, чтобы все правильно заработало" [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]].
- **One exception: the Texas BOM goes into BC now.** Val read out that the Texas BOM does not exist in BC ("Он говорит, что текст из боб… в бесси не существует" — who "он" is, is not said; likely the AI tool he was using, inference); Genadi: "Я сделал только на тот ресайк[лер]." Val first said not to add it, because "мы очень быстро сделаем то, что нэйтан делает. Вы будете просто зря тратить время?" Genadi: "это мне 10 минут." Val: "Окей, если у вас 10 минут" [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]].

## What exists now (Genadi's account)

- **A BOM standard.** "Стандарт я сделал там я вам послал пиар" — a standard for building bills of materials for products, sent to Val as a pull request. Next he wants a standard for releasing part numbers: "как выпускать партнам… как исайн новые номера" [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]. This answers the Sept-30 question whether there should be a written BOM standard (see the sequencer).
- **Drawings in GitHub.** All drawings are ready and "уже все лежат в гетхабе"; by a part number you get the drawings, all revisions and the BOM. The place: "джевел кор, и там хардворнифек есть репозитори" — read by the notes as the JVL-Core organization, hardware-manufacturing repo. Genadi said he committed the Flex Pay Slim BOM that day with a table; "есть номер и всё из этого номера. Автоматически можно брать все" [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]] [[raw/Meeting_Notes_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]].
- **Mikhail's report.** Genadi calls it the one tool Mikhail works with: enter a product number and a quantity, and it gives the product's flat structure, with on hand, on order, in shipment and the shortage to order — "Это самое главное… единственное, что с чем он работает" [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]. (On Oct 5 Genadi had said Mikhail "до сих пор нету репорта" — see [[wiki/people/mikhail-perelman.md]]; the two lines may describe different reports. **Unclear.**)
- **How drawings go to suppliers today.** Mikhail sends them by email: the report lists the files and Genadi can put them in one email from GitHub; "он просто делает форвард" [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]].

## The Hangzhou quote — Val practises himself

Val wants to send the Flex Slim sheet-metal drawings to the Hangzhou supplier himself — "джимтао и таратан" are in the system — "Ну я хочу потренироваться сам лично. Чтоб я понимал, когда со мной нэйтан… какие нюансы есть." Genadi's method [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]:

- **Decide the quantities first** — for example 100 Slim sets for Georgia and some for Texas. The cabinet is the same; the inside differs (Texas uses a recycler).
- **Put the two BOM numbers into the system** to get a flat list with the quantity of each part; copy that list to Hangzhou.
- **Ask for 100, 300 and 1,000** at once, "чтобы не делала эту работу 3 раза"; "мы же можем будем в следующем году тысячами заказывать."
- **Hinges go to another supplier** that only does hinges.
- **Prices go into BC, not GitHub** — Genadi, recalling Val's rule: "они в гетхаб не должны идти… Беси их надо туда внести."

Val at first said sorting Georgia from Texas was not worth it — "Это будет на $200 дороже. Дешевле, чем мне сейчас сидеть сортировать?" — but he wants Texas included [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]].

## Why

- **The BOM in BC is "wrong" in Val's model** — the same reason as Sept 23 to Oct 5: GitHub is the source, MSBC holds the result and the commercial side (inference from the thread).
- **One person should not hold the company's ordering.** Genadi: even if it all works, "компания вперёд не не продвинется за счёт этого." Val: it will, "значительно", because Mikhail is leaving; in a company that depended more on one person "это было бы трагедия" (the sentence is partly garbled) [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]].

## Oct 9 2026 update — Nathan is out the week of Oct 12; the Georgia Slim BOM is due end of October

At the [[wiki/meetings/2026-10-09-github-msbc-agent-bom-assembly-and-pay-slim-first-test.md|Oct 9 11:37 AM "GitHub-MSBC" meeting]] (English; Nathan, Genadi, Val mostly by chat) [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]:

- **MSBC is not the starting point.** Nathan, reading Val's chat: "Val doesn't want Msbc as a starting point." Genadi: GitHub provides the BOM, it is exported into MSBC, and each change exports a new revision. This restates today's ruling from the other side — see [[wiki/decisions/2026-10-09-the-georgia-flex-pay-slim-bom-is-built-forward-from-genadis-github-source-by-agent-and-script-with-human-approval-by-end-of-october.md]].
- **The week moves.** Nathan: "I am out next week, but then that Val, you want this done. End of month, so I will… Jump on that when I'm back." So the Oct 12–20 push does not run with Nathan; his Georgia Flex Pay Slim BOM is due end of October (the notes: October 31) [[raw/Meeting_Notes_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]].
- **The ordering actions are downstream.** Genadi said the five actions Val texted (placing orders, connecting the suppliers and others; the full text is not on tape) "all comes from Msbc" and could be done "tomorrow"; Nathan: they work "with the existing BOM… current inventory in… BC and the list of suppliers in BC." This is the "ordering without Mikhail" goal from today, now framed as downstream of a solid BOM.

## Oct 13 2026 update — vendor data in MSBC, and the report split from the BOM

On the [[wiki/meetings/2026-10-13-github-msbc-ai-bom-control-gate-and-msbc-only-reports.md|Oct 13 "GitHub-MSBC" meeting]] Val restated the MSBC end state from the vendor side: "Административнофинансовая Информация на каждого вендера" — bank, contacts, administration — should come from the vendor itself into MSBC in a format that can be loaded directly, while the parts, semi-finished goods, products or services bought from that vendor come from GitHub. "Что сегодня не работает это совмещение" of the two for the same vendor. Genadi: the format must be worked out with Nathan; he stores files in the repositories by project today, and Nathan should say how to organise or tag them [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]. Val also said the GitHub–MSBC BOM sync and the MSBC report are "2 разные вещи" — see [[wiki/decisions/2026-10-13-procurement-reports-come-only-from-msbc-and-the-excel-export-report-goes-away.md]] and [[wiki/decisions/2026-10-13-the-agent-builds-the-bom-as-a-control-gate-taught-by-data-contracts-not-cad-and-genadi-finds-why-it-is-wrong.md]] [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]].

## Open commitments

- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — test Nathan's work as soon as it is ready, and find what does not work — due week of Oct 12–20 2026 — [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]] *(Oct 9: Nathan is out that week; the work to test is now the Georgia Flex Pay Slim BOM, due end of October [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]])*
- [ ] Genadi Peari — add the Texas BOM to BC — due Oct 8 2026 ("10 минут") — [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]
- [ ] Genadi Peari — write the standard for releasing / assigning new part numbers — due unspecified — [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]
- [ ] Genadi Peari — send Val the link to the Flex Pay Slim in the hardware-manufacturing repo — due Oct 8 2026 — [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]] *(Oct 9: he said he will send Nathan the Pay Slim link; whether Val got his is not said [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]])*
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — prepare a quote request to Hangzhou for the Flex Slim sheet metal, Georgia and Texas, himself — due unspecified — [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]
- [ ] Owner not named ("[Needs Val's confirmation]" in the notes) — order the IQ parts and boards to reach 100 units — due unspecified (Val: "Порты на IQ это всё нужно заказывать") — [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]] [[raw/Meeting_Notes_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]

- [ ] Genadi Peari and [[wiki/people/nathan-carver.md|Nathan Carver]] — agree the format for each vendor's administrative and financial data into MSBC, and how files in the repositories are organised or tagged — due unspecified — [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]

## Open questions

- What else is not ordered for the Flex Slim and its peripherals? Genadi: "Надо проверить, что они заказаны эти детали"; who checks is not set — [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]
- How are Alekseev's online board orders paid without a PO? Genadi: Alekseev places the order and Mikhail pays, "По моему, если не ошибаюсь"; Val: "как это можно оплатить без прочессоры?"; Genadi: "я не знаю" — [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]
- How are the quote quantities split between Georgia and Texas? Genadi's example: about 100 for Georgia, maybe 10 recycler sets for Texas — not set — [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]

## History

- [x] Nathan Carver — show progress on the BOM system — due Monday Oct 12 2026 ("Он должен показать… чтото в понедельник"; stated by Val, Nathan absent) — [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]] — **discharged Oct 9 2026, ahead of Monday:** he showed his agent BOM experiment to Genadi and Val [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- *Answered Oct 9 2026:* "Is Nathan available the week of Oct 12?" [[raw/Meeting_Notes_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]] [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]] — no: "I am out next week… Jump on that when I'm back… following week" [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]

**§15.8:** clear — component, quantity and cost talk only. **§15 #9:** clear — no part number or identifier is spoken.

## Sources
- [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]
- [[raw/Meeting_Notes_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]
- [[raw/Meeting_Notes_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- [[raw/Meeting_Transcript_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- [[raw/Meeting_Notes_GitHub_MSBC_Agent_BOM_Assembly_Pay_Slim-October-9-2026.md]]
- [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]
- [[raw/Meeting_Notes_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]
