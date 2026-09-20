---
type: decision
title: Import duty gets its own tax category in Business Central, so a part is costed at what it lands for
date: 2026-09-17
aliases: [landed cost, import duty tax category, импорт дьютис, BOM plus 30 percent, bill of material excludes freight, FlexPort board 46 dollars, FlexPort board 60 dollars, Genadi confused about machine cost, repack and tricks, airport cost, 35 percent markup]
source-count: 2
status: active
open-commitments: 1
open-questions: 2
---

# Import duty gets its own tax category in Business Central, so a part is costed at what it lands for

**Decided:** September 17 2026, on the 1:54 PM segment ([[wiki/meetings/2026-09-17-flexpay-slim-lid-critique-and-flexport-landed-cost.md]]). **By:** [[wiki/people/val-levitan.md|Val Levitan]], raised by [[wiki/people/genadi-peari.md|Genadi Peari]]. **Language:** Russian. Three minutes, at the end of a hardware call.

## The gap Genadi put on the table

Genadi had priced the **electronic board for FlexPort** at quantity with [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]: "**Цена, скажем, электронный борт[.] На фл[е]кспорт… он стоит сегодня[ — ]я проверил на квонти[ти] с алексеевым**". The figure he gave at that moment is **garbled in the transcript** ("**там получилось Белов и доллар**") and is not asserted here. The two numbers that *are* literally in the source are the pair he drew immediately afterwards [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]:

> "**когда мы его будем заказывать? Он нам будет обходиться не… в $46, как должно быть, он нам будет обходиться в $60 изза этих таксов**"

— when we actually order it, it does not cost the **$46** it ought to, it costs us **$60**, because of the taxes. Val's reply was agreement that the current practice cannot continue: "**Да да да, мы не уйдём[.] Вот так всё[,] мы не уйдём вот так**" [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]].

*(The word Genadi uses is "**таксов**" — taxes. Val's answer names duties specifically. The transcript does not break the $14 gap into duty, freight and handling, and no rate, HTS/tariff classification or country is stated anywhere in this source. The derived notes' phrasing "because of taxes and duties" and "The component price is about $46" are **their reading of the same two lines**, not extra information.)* [[raw/Meeting_Notes_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]

## What was decided

**The bill-of-material price stays the component price; the difference is carried as a tax category inside Business Central.**

Genadi framed the split: "**мы ки[п]ы[ ]кост[,] как наш би[лл ]о[ф ]материал[,] то, что стоит компонент[,] мы должны… в BC**" — we keep the cost, as our bill of material, as what the component costs, [and the rest] in BC. Val supplied the mechanism [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]:

> "**Мы должны внести[,] завести категорию[,] налоговую категорию, которая называется… [и]мп[орт] [дью]рис**"

— we must enter, create a category, a tax category, called import duties. *(The name itself arrives garbled — "**Импульс импульрис**" — and **import duties** is a **reading** of the sound, taken with the derived notes; the Russian is kept. "BC" is expanded to **Business Central**, JVL's ERP, on the corpus-wide basis of [[wiki/topics/business-central-erp-implementation.md]], where BC is the established short form.)* [[raw/Meeting_Notes_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]

**No owner was named.** Val said "we must"; nobody on the call took the task, and the derived notes flag the same gap [[raw/Meeting_Notes_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]].

## Why Genadi raised it — he cannot answer "what does this machine cost"

This is the part of the exchange that is about Genadi's own position rather than about accounting [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]:

> "**вы меня[,] когда спрашиваете[:] Геннадий, сколько стоит мне эта машина? Я, честно говоря, confus[ed], потому что я смотрю… а потом я смотрю туда[,] и в[о] студии freen[t] [words]**"

— when you ask me what this machine costs me, I am honestly confused, because I look at one figure and then at another with freight in it. *(His closing words here are garbled; **freight** is read from "freen[t]" and from the surrounding sense, and is labelled an inference.)*

He named where he sees it — "**я вижу мазер борты, а электроника вся[,] мониторы**", motherboards, all the electronics, monitors — and gave the supplier mechanism and the warning [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]:

> "**пока мы работаем с этими [not sow mach][,] они перепаковывают[,] там они делают хитрости, но это хьюч[;] это чтобы вы не были мистейкенс с нашими ценами, потому что это зависит и прайсинг. Потом это в аэропорте.**"

— while we work with these ⟨garbled⟩, they repack, they do tricks, but it is huge; this is so that you are not mistaken by our prices, because pricing depends on it. And then there is the airport on top. *(The phrase "**not sow mach**" is **not interpretable** and no supplier is identified. The derived notes render it as "the current suppliers", which is **their inference**; it is not in the source and is not asserted here. "Потом это в аэропорте" is recorded as said — the notes' "airport cost" adds a word.)* [[raw/Meeting_Notes_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]

## Val's working markup on Genadi's numbers

Val stated it twice, unprompted and in the same words — "**Я я добавляю 30%**" and again "**Я добавляю 30%**" — and then explained what the number he asks Genadi for actually is [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]:

> "**Когда я вас спрашиваю[ про] м[атериал], это это без всяких[,] без Фре[йта][,] без… всего остального, а на самом деле я должен добавлять больше[ — ]я должен добавлять около 35%. На самом деле.**"

— when I ask you for the material [cost] it is without freight and without everything else, and in reality I ought to be adding more, about **35%**. He did not instruct anyone to change anything; the 35% is stated as the truer figure, not adopted [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]].

**Inference, labelled — do not merge these two thirties.** JVL's Apr-2025 **intercompany transfer price** is also "bill of material + 30%" ([[wiki/topics/tariffs-and-customs-compliance.md]]). That is a *declared customs value* between JVL Labs and JVL Systems; this one is Val's *private estimating rule* for reading Genadi's quotes. They may share an origin, but no source connects them and neither is here treated as evidence for the other.

Genadi's closing line on the size of it is garbled and partly contrary: "**Одно радует, что это все в такой ситуации, но это не так радует… Это это это огромная**" — the one consolation is that everyone is in this situation, but it is not much of a consolation; this is enormous. *(The derived notes compress this to "the size of it is not a happy thing", which drops the everyone-is-in-it-too half. The Russian is kept.)* [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]] [[raw/Meeting_Notes_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]

## How this sits against what the wiki already holds

- It is the **operational** end of the tariff thread on [[wiki/topics/tariffs-and-customs-compliance.md]]: that page holds JVL's classification, origin and HS-code strategy from 2025; this is the first source in the corpus where the duty shows up as a **per-part costing gap on a specific board** and a request for an ERP field to hold it.
- It is the same **"what things really cost" gap** Genadi has been the one to name before — the Sept-4 "received goods are invisible in the system" complaint on [[wiki/topics/business-central-erp-implementation.md]], and the Sept-16 board-price correction where he quoted "$600 за борт" and withdrew it inside two lines as last year's number ([[wiki/people/genadi-peari.md]]).
- It does **not** contradict any held figure. The Aug-24 2026 Flex-Port board price of about **$45 per 100** on [[wiki/people/genadi-peari.md]] is a component price for a different port variant at a different date; the $46/$60 pair here is the FlexPort board as ordered on Sept 17 2026. Both are recorded as-of their dates, neither supersedes the other.

## Open commitments

- [ ] Owner not named on the call — create an import-duties tax category in Business Central so landed cost is captured alongside the bill-of-material component price. Val: "**Мы должны внести[,] завести категорию**" — due unspecified — [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]

## Open questions

- Does Val's markup on Genadi's bill-of-material quotes move from **30%** to the **35%** he called the truer figure? He raised it and nothing was agreed. [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]
- What exactly makes up the **$46 → $60** gap on the FlexPort board — duty, freight, handling, or supplier repacking — and at what rate? The source names only "таксов" and "these duties"; no rate or classification is given. [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]

## §15 holds

**§15.8:** clear and deliberate — this page is component, freight, duty and supplier economics, which are in scope. No named person's pay, rate or performance judgement appears in the source or on this page. **§15.9:** no tax identifier, customs number, registration number, account or routing value appears in the source; none would be written here if it did.

## Sources

- [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]
- [[raw/Meeting_Notes_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]
