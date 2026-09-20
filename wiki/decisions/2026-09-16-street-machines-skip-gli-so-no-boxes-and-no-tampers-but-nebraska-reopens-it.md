---
type: decision
title: Street machines do not go through GLI, so there are no enclosure boxes and no tampers — then Val partly walked it back over Nebraska
date: 2026-09-16
aliases: [no GLI for street machines, надо ли нам проходить GLI для стрит машин, no tampers, никаких тамперов не нужно, no enclosure box, без всяких коробочек, door monitoring setup and audit, дверь мониторить сетап аудит, Nebraska parameters, Eclipse wanted a local box, я гребу обратно]
source-count: 2
status: active
open-commitments: 1
open-questions: 2
---

# Street machines do not go through GLI — so no boxes and no tampers, unless Nebraska says otherwise

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-16-street-machine-board-spec-and-georgia-class-a-order.md|Sept 16 2026 12:35 PM ET alignment call]] (held in **Russian**), then **partly reopened by Val himself** four minutes later. Applies to the [[wiki/topics/low-cost-street-machine.md|street machine]].

## The question, and the answer

[[wiki/people/pavel.md|Pavel Frolov]] had asked it once while Val was away from the call and got only "**[надо] спросить … не знаю**" back from [[wiki/people/genadi-peari.md|Genadi Peari]]. He re-asked it the moment Val returned:

> **Pavel:** "**[GLI] — надо ли нам проходить [GLI] для стрит машин?**"
> **Val:** "**Нет.**"
> **Pavel:** "**Не надо[,] окей?**"
> [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

See [[wiki/organizations/gli.md]].

## What follows from it: no boxes, therefore no tampers

Genadi had already drawn the consequence while Val was off the call — "**никаких тамперов не нужно[,] потому что [Вал] сказал без всяких коробочек**" — and restated it to Val's face: "**[т]ак как мы делаем всю электронику без коробочки, то нам не нужно тампер[ы] в принципе**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**What is still required is three things, and only three:** "**[т]амперы точно не должны быть[;] все, что нам нужно … [д]верь мониторить. И с[е]тап. И аудит**" — door monitoring, setup, audit [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

Genadi immediately spotted the knock-on and asked it out loud: "**если нет тамперов, что будет делать лоу [пауэр] [мод]?**" Pavel's answer was door state only — that someone "**открывал дверь … в выключенном состоянии**", or opened the bill-acceptor access door [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]. The low-power-mode outcome is on [[wiki/decisions/2026-09-16-one-fram-chip-instead-of-six-and-low-power-mode-laid-in-but-not-populated.md]].

## And then Val partly walked it back — over Nebraska

Four minutes after answering "no", Val reopened his own ruling unprompted:

> "**[у] меня такое чувство, что это стрит[-]машина получится обалденно классная. И, может быть, мы захотим её поставить в [Н]ебраск[е]. А в [Н]ебраск[е] я не помню[,] я сделал[] или нет. Я знаю[,] что мы там [через Eclipse] проходим, но я не знаю[,] какие там [требования;] по[-]моему[,] они какие[-]то вялые такие.**"
> [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

And then, explicitly, why his first answer was what it was: "**я озвучил сначала, что не став[им] коробку, потому что я думал, что дела не будет. Ну сейчас я как[-]то [гребу] обратно**" — I said no box because I thought there would be none of this; now I am rowing back [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**Genadi's institutional memory cuts against the no-box design**, and it is the only evidence in the room:

- "**[Eclipse] всегда хотели коробочку для электроники локал[ьную;] мы помним[,] мы им посылали[,] даже что[-]то меняли**" — the lab always wanted a local box for the electronics; JVL sent them things and even changed something [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].
- On tampers, twice and in opposite directions inside a minute: "**И [тамперы] не хотят**", then "**[т]амперс … надо [поддерживать]. Хотя бы… [е]сли понадобится этот кей[с] … [э]то должно быть мониториться**", then "**Кстати, [Eclipse] не требует это мониторить … [п]о[-]моему**". **His own recollection is not self-consistent and is recorded as spoken.** [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

**Val's conclusion was to go and ask:** "**С ними, скорее всего, стоит связаться и спросить [про] [Н]ебраск[у] — какие параметры?**" — no owner was named aloud [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**§4 — the lab.** The transcript renders the lab as "**клипс**" / "**клипсе**" throughout. Read as **[[wiki/organizations/eclipse-gaming-lab.md|Eclipse]]**, JVL's certification lab, on strong corpus support: Eclipse is the lab JVL uses for **Nebraska** specifically (see the June 2025 Nebraska testing-requirement review) and for Georgia. The reading is an **inference from context**, not a literal string in the source. Note that the same garble family was left **unresolved** in a different context two days earlier — on Sept 14 "**это клипс**" referred to an older *machine*, and no machine identity was asserted there; that remains open. See [[wiki/topics/low-cost-street-machine.md]].

## Open commitments

- [ ] (owner unnamed — Val said it should be done, named nobody) — contact the certification lab and ask what Nebraska's parameters are for the electronics box and tampers — due unspecified — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

## Open questions

- **Was the street machine ever certified for Nebraska?** Val: "**я не помню[,] я сделал[] или нет**", and he does not know the requirements. Nothing in this source answers it. [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]] See [[wiki/projects/nebraska-skill-market.md]].
- **Does the lab require a local electronics box, and does it want tampers?** Genadi's recollection points both ways inside the same exchange. Unresolved. [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

**§15.8:** clear — certification and product-compliance economics only; no named-person compensation.

## Sources

- [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
