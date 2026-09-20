---
type: decision
title: The Jira link between a capability and a requirement is reversed to "capability requires requirement", and planning dates always sit on the lowest level of work that exists so the roll-up never breaks
date: 2026-09-15
aliases: [capability requires requirement, required by, implemented by requirements, link direction, roll-up, planning dates lowest level, take the date off the capability, реквайред бай, ролл ап, Bosik report fields]
source-count: 2
status: active
open-commitments: 2
open-questions: 0
---

# Capability *requires* requirement; dates sit on the lowest level that exists

Two Jira-hygiene rulings from the opening ten minutes of the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept 15 2026 8:03 AM call]] (Russian), both triggered by the daily report [[wiki/people/andrey-bosik.md|Andrey Bosik]] now sends. They continue the planning discipline handed to Bosik and Kovalchuk on Sept 9 ([[wiki/decisions/2026-09-09-planning-handed-to-bosik-and-kovalchuk-with-daily-recorded-sessions.md]]) and the capability-project structure of [[wiki/decisions/2026-09-10-per-product-components-and-mvp-fix-versions-on-the-capability-project.md]].

## Dates go on the lowest level of work that exists

Bosik opened by saying he had interpreted some report fields his own way and wanted them checked — "надо тоже обсудить некоторые поля, потому что я их интерпретировал так, как я вижу" — and named the concrete one: not everything carries an end date, and the rule had changed before. "И вот вопрос, на что мы ставим дату?" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

[[wiki/people/val-levitan.md|Val]]'s answer began by denying there is a hard rule — "у нас нету жесткого правила, на что мы ставим" — and then stated one [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

> **мы хотим, чтоб был ролл[-]ап всегда, поэтому… мы планируем самый нижний [уровень] работы. Если там есть stor[ies], мы планируем stor[ies]. Если stor[ies] нету, мы планируем фьючерс[ / features].**

[[wiki/people/pavel.md|Pavel]] gave the same rule as a migration: "ставим… но только на 1 этапе. **Пока у нас нет под ней фич[ — ]как только появляются фичи, мы начинаем планировать фичи и убираем с ка[пa]билити**". Val restated it as a chain [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

> Планируем… только на самой низш[ем] статус[е]. Если кей[па]бил[ити] эт[о] самый низший статус, тогда мы планируем. Если под ней появляется фичер, мы дату убираем с [капабилити] и начинаем планировать фьючерс. Если появляется под ним ст[ори], мы убираем дату с [фичера] и начинаем планировать стор[ис]. **Чтобы постоянно был ролл[-]ап, иначе ролл[-]ап исчезает, и там начинается конфликт.**

Bosik accepted and said he would correct the report accordingly [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## The link direction was backwards, and Irina caught it

[[wiki/people/andrei-klimovich.md|Klimovich]] admitted he might be reading the relationship wrong — "видимо, я неправильно это понимаю" — and described what he had been doing: "в моём понимании… реква[йр]мент имплементс… [капабилити]" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

[[wiki/people/irina-shishko.md|Irina Shishko]] named the habit before he described it — "**я знаю, что ты всегда ставишь [implemented by requirements]**" — and said why it is wrong: "мне кажется, это неправильная… **моя логика, что реализуется, имплементируется фичи. Основывается на регламент[ах / requirements]**" — a *feature* is what gets implemented; a capability is *based on* requirements [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

Pavel supplied the Jira link type: "**мы склоняемся[,] что[-]то [required by] лучше подходит**". Klimovich worked it from inside the capability and landed on the agreed form — "**я же внутри к[а]п[абилити] нахожусь, то есть я ставлю связь, что этот к[а]п[абилити] [requires] какой[-]нибудь рек[вайрмент]**" — with Val confirming. So: **capability *requires* requirement**, and the requirement reads *is required by* the capability. Klimovich took the cleanup: "тогда я эт[и] все связи пробегусь[,] обновлю, чтобы у нас везде правильно стояло" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Val refuses to wait a day for a corrected report

Bosik's first offer was tomorrow's copy — "я этот момент немножко в отчёте поправлю[,] завтра там будет обновлённ[ый]" — because the report goes out once a day. Val: "**Почему надо это завтра? Почему сегодня не [c]дела[ть]?**" and "**мне всё нужно быстрее[,] медленно очень всё… мне всё нужно сейчас или вчера**". Bosik agreed to push an updated copy the same day [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

Val also cut off a broader review of the report — "мы не будем на это смотреть, давайте сейчас будем проходить быстро" — to protect the UI/UX agenda [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Two capability-bookkeeping facts from the same minutes

- **The dual-wallet capability now exists.** Klimovich: "я добавил кэп[абилити]… релиз [MVP] один[,] котор[ая]… регулиру[ет] эту логику двойного волета" — this discharges the Sept-14 commitment to get the dual-balance logic into the capabilities. *(Irina named a number — "176" — in the same breath, and Klimovich answered "верю, да, я по памяти", i.e. he was going from memory. The number is therefore recorded as **probable but not asserted**: the transcript does not state that 176 is that capability's identifier.)* [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- **Requirement 1538 has still not moved.** "рек[вайрмент] 15[ ]38[ — ]то, что вчера проговорили[ — ]ещё не вынес[,] вынесу. Сегодня оно должно будет уйти в новый к[а]п[абилити] для 2 MVP и тогда уберу оттуда." Val asked Bosik to prepare the ground for the status change to be made as soon as Klimovich finishes: "Андрей босик, готовьте пока почву, чтобы можно было перевести в… другой статус" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. See [[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]].
- **Statuses are to be brought current the same day**, off Bosik's report: "по поводу комментариев, что нужно все статусы актуальны[ — ]это надо сделать сегодня. Я сделаю это быстро, получил утром репорт у Андрея босика" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. The rule that nothing in MVP 1 may still sit in "Proposed" is [[wiki/decisions/2026-09-14-nothing-in-mvp1-may-still-be-proposed-and-bosik-writes-the-exception-report.md]].

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — go through every capability↔requirement link and unify it to "capability requires requirement" — due the same day (Sept 15 2026) — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — correct the report's date-field interpretation to the lowest-level-of-work rule and push an updated copy the same day rather than waiting for the daily cycle — due Sept 15 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

**§15.8:** clear — Jira process only; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
