---
type: decision
title: Finish the TITO printer cases first, then start the street cabinet on September 23 — the standalone peripherals wait
date: 2026-09-14
aliases: [TITO cases then the street machine, standalone TITO printer, standalone card dispenser, кейсы для тито, стрит кабинет, September 23 start, 400 tickets, desktop power supply RS-232, no metal 3D print first, hand the box to Sasha]
source-count: 2
status: active
open-commitments: 4
open-questions: 1
---

# TITO printer cases first, then the street cabinet — starting September 23

Settled at the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|Sept 14 2026 12:04 PM call]] (Russian) between [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/pavel.md|Pavel Frolov]].

## The proposal Val rejected

[[wiki/people/genadi-peari.md|Genadi]] put his own remaining priority on the table: "**у нас остается пр[и]орити выпустить. Стенделон тито принтер, стэнделон кард[ ]диспенсер**" — release a standalone TITO printer and a standalone card dispenser (as separately sellable peripherals; the transcript's last words here, "**бос будут гдето peart sales**", are garbled and no channel is asserted) [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

Val refused the ordering flatly and said the cabinet comes first: "**Это это неправильно… [стрит] кабинет. После Того, что вы сейчас закончите вот это делать, то, что вы делаете. Сразу [переходите на] стрит кабин[ет]**" — the transcript garbles the verb, but the sense and the derived notes agree: after finishing what is in hand, go straight to the street cabinet. Genadi accepted it — "**А я думал надо быстро и пропустить окей?**" [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]] [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Genadi's counter, and the compromise that came out of it

He did not drop it, and his argument was about physical necessity rather than product strategy: "**нам надо рядом с [IQ] иметь тито принтер, чтобы работал**" — a TITO printer has to sit next to the Flex IQ and work — and "**хотя бы в[а]ринг надо заказать**" — at least the wiring has to be ordered [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

Val agreed it is needed and sized it down: "**Да… нам нужно, но смотрите. Таких кейсов будет немного. А подождите — да мы же сначала выставляем, мы сначала ставим айкью. А потом дорабатываем**" — there will not be many such cases; first the IQ goes out, then it is added to [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

He then set the sequence explicitly, after the detail discussion: "**после Того, что вы сделаете этот… Кейсы для тито. Вы переходите на… [стрит] машину**" — once the TITO cases are done, move to the street machine [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

So the standalone *peripherals* were deferred, while the *enclosure* for the TITO printer was pulled in front of the cabinet.

## The enclosure, as specified in the room

All of it Genadi's, agreed by Val [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]:

- **It plugs into the IQ's own connector.** "**в коннектор в тот же коннектор, в смысле в IQ**."
- **A separate desktop power supply, not AC inside the box.** "**нам надо будет там отдельно десктоп, наверно пауэр[ supply] и для принтера**", and the reasoning: "**не делать вот эти [AC] внутри, все эти проб[лемы] потом — и просто обычный десктоп[;] они его гдето бросят, [подключат] к нам. Снаружи воткнут р с 232 и всё**" — an ordinary desktop brick dropped wherever, with **RS-232 plugged in from outside**.
- **Connectors on a back panel, built properly.** "**панельку сделать такую сзади… [к]оннекшнс. Ну индустриальная, это как нормальная… мы ж не можем, чтобы это всё вболталось там**" — industrial, not left dangling.
- **Sized for 400 tickets, not 200.** Genadi asked "**сколько [тикетов] мы хотим провижн 200 или 400?**"; Val's answer: "**когда вы коробку будете дизайн[ить,] сзади чуть побольше… чтобы мы могли всегда поставить 400**" — design the back slightly bigger so 400 always fits. Genadi added that then "**никаких экстеншенс не надо**" — no extensions needed.
- **No security.** "**Нам не надо это се[кьюрити], это всего лишь принтер[]**", and later "**Тикеты же не должны быть лок[нуты], правильно, просто там же ничего нету**" — the tickets need not be locked away, there is nothing of value in there.

## Plastic, not metal — and 3D print before tooling

Val asked Genadi to hand the box off: "**Геннадий, вы можете отдать эту коробку, пластиковое дело, саше**". Genadi objected that they had said they would not do it in plastic, and that bending it out of metal is trivial anyway: "**если просто согнуть из металла — это очень быстро, это один день… нечего отдавать**" — one day's work, nothing worth delegating [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

Val overrode it on product grounds, not cost: "**Без металл[а]… нам лучше сделать 3[D печать]. А потом заказать [production] тул на пластик. Вы не можете поставить предмет из металла на стол? Это… не работает. Это не модерн[ый] подход**" — no metal; 3D print first, then order a production tool for plastic; you cannot put a metal object on a counter, it is not a modern approach [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**Genadi's condition for handing it over** — accepted by Val — is that the unknowns get resolved first: "**Я предпочитаю разобраться, что происходит… надо посмотреть базел, как включить в этот принтер… [м]ы свою электронику не хотим делать. Можем ли мы [найти] или надо покупать, а как это будет открываться, куда нужен а[кс]ес? [В]аринг нужно сделать под нас**" — the bezel, how the printer is incorporated, whether the electronics are found or bought, how it opens, where access is needed, and JVL-specific wiring. Plus "**сделать [PCB] маленький… для подключения**" — a small board for the connection. Val's readback, which Genadi confirmed with "**Ну да**": "**когда вы дадите ему все детали, тогда он сможет сделать коробку**" [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

## §4 — "Sasha" is left unresolved

The person Val names is "**саше**" (Sasha, the short form of Alexander), and the task is a **mechanical / industrial enclosure design**. The only Sasha in this corpus is [[wiki/people/alexander-biratka.md|Alexander Biratka]], an Omni/Pixi framework and build **software** engineer — which does not fit this task at all. Per §4 the mention is **left unresolved and queued rather than force-matched**; no page is created and no identity is asserted. *(The contractor industrial designer who works through Genadi on cabinets is [[wiki/people/igor-starovoytov.md|Igor Starovoytov]] — a different given name, so not a candidate either.)* [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## The start date

Asked "**когда можно рассчитывать, что вы приступите к кабинету?**", Genadi gave the order of work — finish **IQ**, then **Slim**, then **IQ** again, then the **printer**, all inside that week — and said he could start the cabinet the following week. Val put a date on it and Genadi confirmed: "**23 можете приступить к кабинету?**" — "**Думаю да**." **September 23 2026.** [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

*(The transcript inserts clock-like garbles inside that list — "потом 14:00 IQ, потом с [п]ринтером 14:03" — which are transcription artifacts, not times. The sequence is recorded as the derived notes read it and as the surrounding words support; no time of day is asserted.)* [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Open commitments

- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — design the standalone TITO printer enclosure: back-panel connectors, external desktop power supply, RS-232 in from outside, sized for 400 tickets, no security — due before Sept 23 2026 — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — resolve the enclosure unknowns (bezel, printer integration, electronics found-or-bought, how it opens, access points, JVL wiring, the small connection board), then hand the plastic box design to "Sasha" — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — finish IQ, Slim, IQ again and the printer this week — due week of Sept 14 2026 — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — start the street cabinet — due Sept 23 2026 — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Open questions

- **Who is "Sasha"?** Named as the recipient of the enclosure design; fits no known person's role in this corpus. Left unresolved (§4) — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## What is deferred, not killed

The **standalone TITO printer and standalone card dispenser as separately released peripherals** are behind the street cabinet in the queue. Nothing in the source cancels them, and Genadi's underlying need — a TITO printer working beside a Flex IQ — is met by the enclosure above rather than by the peripheral release. Recorded as deferred. [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

**§15.8:** clear — enclosure and work-sequencing content only; no named-person compensation appears in either Sept-14 12:04 file.

## Sources

- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
