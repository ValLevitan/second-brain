---
type: decision
title: Capabilities are written against the published SAS standard, not invented — and JVL targets SAS 6.02 rather than the newest 6.03, because some machines in the field were never updated
date: 2026-09-14
aliases: [SAS 6.02, SAS 6.03, Gaming Standards Association, published AFT standard, AFT window on third-party machines, IFT transfer menu, do not invent the capability, sass specification, с. А. стандарт]
source-count: 2
status: active
open-commitments: 2
open-questions: 1
---

# Capabilities are written against the published SAS standard — target 6.02

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|Sept 14 2026 8:01 AM call]], after an exchange in which [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] discovered that the funds-transfer screens he thought were JVL's own are in fact an industry standard.

## How it came up

[[wiki/people/pavel.md|Pavel Frolov]] offered Klimovich the current Flex-Port firmware so he could install it, connect to a machine over SAS and walk the new workflow himself — "[м]ожет быть тебе попробовать дать текущую прошивку порта? Ты бы его поставил, попробовал подключить к машине по [SAS,] и прош[ё]лся по новому [work]flow, который уже сасовский вариант… [и] посмотр[ел], что на экране отображается, какие сообщения." The new build also analyses error cases and reports them: SAS not connected, Flex-Port not connected, "[AFT] не настроен" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

Pavel then said any credit or withdrawal now shows in the machine's own transfer menu — "любое зачисление, снятие денег ты увидишь в меню [AFT] трансфер на машине." Klimovich assumed that was a JVL screen: "но только на нашей машине[ —] как это будет работать со сторонни[ми]?" Pavel: "[н]а чужих то же самое будет." [[wiki/people/alexander-biratka.md|Alexander Biratka]] checked it was mandatory; Pavel answered in two words — "**Это стандарт**" — and Klimovich's reaction was "**[н]ичего себе**" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

*(The transcript renders the transfer mechanism as both "AFT" and "IFT" in the same passage. Reading it as **AFT** — the SAS funds-transfer feature JVL has been building the Flex-Port against since early September — is an inference from context, not a spelling the source settles.)*

## Val's ruling

> "**[К]огда вы пишете к[е]побил[ити,] вы должны [использовать] этот SAS [s]tand[a]rt[,] а мы не просто с головой выдумываем. Это уже разработано… [Gaming Standards Association]. И опубликовано через SAS 6.02.**" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

Val named the publisher himself — the transcript garbles it as "j паблош stander", "j li stendart" and "часы gamy Stand red surgi", which is the **Gaming Standards Association** — and offered to obtain the specification directly if nobody on the call sent it: "если ребята не отправят, то я могу… вас познакомить" *(the organisation he names for the introduction is garbled as "чиллаи"; not guessed at here)* [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

Biratka confirmed the document is public and volunteered to send it: "вообще это [SAS] спецификаци[ей] описано уже… [в]сё описано в [SAS] стандарте… [н]о открытый он[,] в принципе, в интернете можно открыто." He added what the standard actually does for them: it says "какие обязательные из этих вещей должны быть на машине, а какие необязательные" — which parts are mandatory on a machine and which optional [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## The version argument

Pavel and Biratka both reached for **6.02** to download; Val interrupted with a number the transcript garbles ("[н]ет, мы должны взять 6 точка…"), and when Biratka asked why, gave the reason plainly: "**потому что на некоторых машинах они не сделали апдейт ещё на 6.02**" — machines in the field lag. Biratka argued the point was moot — "[н]о[,] по[-]моему[,] там по [AFT] не было изменений, насколько я помню" — and Val's answer was a rule rather than a fact: "**[н]у[,] было или не было[ —] вы не можете брать самый последний релиз и сказать**". Pavel confirmed the newest is **6.03** ("[с]амый последний 603"). Val landed on **6.02**: "[н]у хорошо, давайте 602 хотя бы", and stated it again as the published baseline a moment later [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**How old 6.02 is — settled on the call.** [[wiki/people/irina-shishko.md|Irina Shishko]] said "[в] 6.02 уже лет 20"; Pavel and Biratka both cut it down — "не 20… лет 10 точно" — and Irina accepted 10. Biratka dated it from his own arrival: "я приходил[ —] как раз был [6.0]2[;] и вот буквально недавно [6.0]3 вышел" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## What Klimovich took on

"Понял, ну давайте я займусь этим[;] пока для меня это новая область знаний[,] я освою, и потом буду понимать, тогда о ч[ё]м речь[ —] пока я не очень понимаю. Я быстро разберусь." SAS is new ground for the man writing the transactional capabilities [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Open commitments

- [ ] [[wiki/people/alexander-biratka.md|Alexander Biratka]] — send Klimovich the SAS specification (public; the version Val ruled on is 6.02) — due unspecified; Val offered to obtain it himself if nobody sends it — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — give Klimovich the current Flex-Port firmware so he can install it, connect over SAS and walk the new workflow himself — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## Open questions

- **Whether the 6.02-versus-6.03 choice actually matters for AFT.** Biratka believes AFT did not change between the versions; Val ruled on 6.02 regardless, on the principle that you cannot assume the newest release is what the field runs. Unresolved on the call — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

*(The derived notes record the same ruling — "the standard is published by the Gaming Standards Association as SAS, it is public, and capabilities must be written against it rather than invented", with Val insisting on 6.02 over 6.03.)* [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

**§15.8:** clear — industry standards and product engineering only.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
