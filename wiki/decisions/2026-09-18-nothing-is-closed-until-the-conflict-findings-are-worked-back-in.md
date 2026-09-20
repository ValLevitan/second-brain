---
type: decision
title: Nothing in MVP 1 gets closed until Chudinov's conflict run is worked back into the capabilities — a closed feature may no longer cover the requirements now attached to it
date: 2026-09-18
aliases: [nothing closes, пока ничего не закрывается, Claude conflict run, conflict and blocker sweep, PIN contradiction, requirements that need a PIN and requirements that do not, specification document for MVP1, прогнал весь MVP1 на поиск блокеров противоречий и конфликтов, run the requirements through Claude, capability 141 not closed, duplicate and contradiction sweep, run it for duplicates too]
source-count: 2
status: active
open-commitments: 4
open-questions: 2
---

# Nothing is closed until the conflict findings are worked back in

Two connected rulings from the [[wiki/meetings/2026-09-18-transactional-mvp1-capability-cleanup-and-the-monday-deadline.md|Sept 18 2026 8:03 AM call]] (Russian), both [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]'s: how the MVP 1 requirement set gets checked for self-contradiction, and the freeze on closing anything until that check has been absorbed.

## What started it — the requirements contradicted each other about the PIN

[[wiki/people/andrei-klimovich.md|Klimovich]] opened the meeting by asking, in effect, what is stopping you building: "**если сейчас… вопросы, связанные с [капабилити]с, которые в работе… что мешает вам создавать фичи и вести разработку?**" Chudinov answered with a concrete blocker he had hit the day before, starting the next feature *(the feature is rendered "**фиг 4**" and is not reconstructed — it recurs later in the same form against capability 148)* [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]:

> "**её требования на [капабилити]… требовали пин кода. Для [в]олет[а], хотя мы от него отказались. В итоге у нас там в списках оказалось, что есть требования, где нужен пин код[,] и требования, где пинкод не нужен. Возникло противоречие[,] конфликт[,] естественно, бло[к]ер.**"

That is the PIN decision ([[wiki/decisions/2026-08-24-drop-pin-from-evoucher-flow.md]]) having been taken but not swept out of the requirement set — the old PIN requirements were still sitting on a live capability.

## The sweep he ran, and what it produced

> "**Это навело меня на мысль[:] я прогнал весь наш [MVP] один по теме флекса ай кю, флекс[]порт и работа с клаудом на поиск различных блокеров, противоречий и конфликтов.**"

So the whole MVP 1 set, across **Flex IQ, Flex-Port and the cloud work**, was run through **Claude** looking for blockers, contradictions and conflicts. The output is a document he put into the meeting chat — "**Документик… я вас скину в чат[,] где [Клод] сказал, где что и как расходится**". Status of the findings, in his own words: "**мы сегодня внутренн[ей] команд[ой] успели частично это переработать, но не всё**", and then, more precisely, "**Блокера мы закрыли, но там остались некоторые расхождения**" — the blockers are closed, the discrepancies are not [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

*(The transcript renders Claude as "**кот**" in this passage and as "**клодом**" / "**клодом на поиск конфликтов**" / "**с плодом вместе**" later; the team's other Sept-2026 sessions establish the reading. See the rendering note on the meeting stub.)*

## The process rule he recommends going forward

> "**когда мы всё это составляем, там вручную линкуем[ —] прогоняем потом[,] запускать [Клодом] на поиск различных конфликтных ситуаций.**"

Write and link the requirements by hand first, then run the set through the tool to find the conflicts. Klimovich accepted the document as his working base without argument: "**Окей, да, за основу возьму его без вопросов**". Chudinov's reason for handing it over rather than grinding through it himself is throughput — "**Обработка по одной растягивается на очень продолжительное время[;] возможно, с [Клодом] вместе ты сможешь их быстрее обработать**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**The same instrument was pointed at duplicates later in the call.** When [[wiki/people/irina-shishko.md|Irina Shishko]] suspected capability 175 duplicated reporting already covered elsewhere, Chudinov's answer was the method rather than an opinion: "**Тогда делайте пометку. Я говорю, после запускайте на поиск дубликатов и противоречий**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

## What he actually wants next — a specification document

This is the ask the corpus should keep, because it is a new artifact nobody has committed to yet [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]:

> "**Наш идеальный вариант — это потом попросить[: ]сделай мне документ, спецификацию на то, как всё это будет работать в MVP один[.] Если потом по этот[му] документ[у] посмотреть, может[,] просто будет глазами понять[,] мы вообще это ожидали или нет?**"

And the reason it cannot be produced today, which is the whole argument in one sentence: "**если сделать это сейчас, то мы получим, что будет написано, что [в волет] надо вводить пинкод[,] и тут же будет написано, что… не надо вводить пинкод**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

## The freeze on closing — and what triggered it

In the feature-planning half of the meeting the team reached **capability 141**, whose tasks [[wiki/people/pavel.md|Pavel Frolov]] found already closed inside — "**Внутри закрытая задача**" — and Irina started to move it on. Chudinov stopped it [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]:

> "**Я говорю[,] задачи, которые прогонял [Клодом] на поиск конфликтов[ —] может получиться так, что в [капабил]ити долетело требование[;] эти фичи, которые мы уже выполнили, требования закрывают, а те, что долетели, ещё нет. Соответственно, надо будет открывать ещё одну фичу, поэтому… Пока ничего не закрывается.**"

The mechanism is exact: the conflict run pushed **new** requirements onto capabilities whose existing features already closed the **old** ones. A feature marked done may therefore no longer cover its capability's current requirement set, and a second feature has to be opened. Until the findings are absorbed, **nothing is marked complete.** Irina accepted it — "Окей" — and the walk-through continued without closing anything [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

*(Capability 141 is not mentioned in the derived notes at all, so the trigger for the freeze is invisible there. It is the same capability [[wiki/people/irina-shishko.md|Irina]] believed had wholly moved to MVP 2 on Sept 16 and Chudinov corrected — see [[wiki/decisions/2026-09-17-bosiks-network-list-splits-between-mvp1-and-mvp2.md]].)* [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**Cost of the freeze, stated on the same call:** capability 122 was ready to close pending a weekend test run, and did not; capability 141 was ready to verify, and did not.

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — take Chudinov's conflict document as the base and work the remaining discrepancies back into the capabilities while he adds the new ones — due unspecified; he agreed on the call — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — finish reworking his own team's share of the findings; only part was done — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — run capability 175 through the duplicate-and-contradiction check before deciding whether it moves, as Chudinov asked — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — run the tests on capability 122 over the weekend and close it if they pass — due the weekend of **Sept 19–20 2026**; he offered it, and it is blocked by this same freeze until the findings are absorbed — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## Open questions

- **Who writes the MVP 1 specification document, and whether it is written at all.** Chudinov described it as the ideal next step; nobody took it and it is not on the Monday list — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- **How the freeze is lifted.** No test was named for when the findings count as absorbed, and no date was set — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**§15.8:** clear — requirement hygiene and tooling only; no compensation, rate or performance judgement of any named person appears, and nothing was excluded on that ground. **§15.9:** no PIN value, credential or identifier is stated — the PIN is discussed only as a field that was dropped.

## Sources

- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
