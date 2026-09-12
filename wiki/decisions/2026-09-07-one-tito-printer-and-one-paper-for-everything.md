---
type: decision
title: One TITO printer and one paper for everything — wallet tickets, receipts and short regulator reports — and the TITO ticket printer is kept over the ordinary roll printer Genadi argued for
date: 2026-09-07
aliases: [one printer one paper, TITO printer kept, roll printer rejected, receipt paper is bad, barcode in the safe zone, like a hundred dollar bill, 24 volts, long reports go by email, 3D-printed enclosure]
source-count: 2
status: active
open-commitments: 1
open-questions: 0
---

# One TITO printer and one paper for everything

Two rulings from the printer segment of the [[wiki/meetings/2026-09-07-gacs-show-setup-flex-iq-flex-ports-and-the-e-wallet.md|Sept 7 2026 8:00 AM call]] (Russian): what the single printer beside the Flex-IQ has to print, and whether it should be a TITO ticket printer at all.

## One printer, one paper, three jobs

[[wiki/people/andrei-klimovich.md|Andrei Klimovich]] separated the jobs: "одно дело — это [carry] наш тикет, его надо распечатывать, а [второе] — это ре[си]т[ы]: подтверждение активаци[и] карты, подтверждение завершения транзакции… мы могли бы использовать тот же самый тито[-]принтер для распечатки и этих реситов тоже[?] Тогда нам нужен только один принтер." [[wiki/people/val-levitan.md|Val]] answered three times over — "Конечно, конечно, конечно" — and added the second half himself: "Притом на одной и той же бумаге" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

Klimovich then named a third job he expects to arrive: "распечатка отчётов. Коротких отчётов по требованию регулятора." Val: "На том же принтере и на той же бумаге." Klimovich flagged that nobody yet knows the data volume; Val set the fallback: "пока мы делаем это шорт, а потом… если это лонг, мы говорим — мы можем отправить по email" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

On whether a report can run across several tickets, [[wiki/people/pavel.md|Pavel Frolov]] and Val said it can ("Можно"; "Любой принтер этого умеет"), but [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] and [[wiki/people/genadi-peari.md|Genadi Peari]] pointed out the practical catch — each ticket has to be taken out before the next prints, "и только после него ты можешь узнать, что там заканчивается что-то." Pavel's characterisation of the device stands as the design constraint: "он в принципе заточен печатать шаблонные какие-то документы, где в определённом месте какое-то поле" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

## Genadi's challenge, and why the TITO printer was kept

- **His question, asked twice:** "откуда пришло требование, что нам нужен именно ticket[-]принтер на лак[ейшне]? Почему обычный ролл[-]принтер, который уже стоит, не может быть и [для e-]вол[етов]?" His reasons: the roll printer is already installed at the location; the TITO unit "немножко нестандартная вещь"; it needs its own supply — "нужен отдельный пауэр[-]с[а]плай… потому что они **24 вольта**"; everyone else prints QR codes on ordinary roll printers; and the tickets are awkward in a wallet — "вот эти тикеты в кошельке не очень удобно держать, они длинные" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **The defence, from three people at once.** Pavel on the paper: "у него бумага не очень качественная, она прозрачна, она плохо сканируется, она легко рвётся, уничтожается," and later "тут обычная чековая бумага засовывается… Я никогда не видел нормальной[,] в рулоне[,] толстой бумаги… под эти чековые принтеры." Val on the physical form: "[Сгибается], плюс она закручена и выходит как колбаса… как падающая штука," and "он не для того, чтобы держать в кошельке или в руках." Chudinov on durability: "Стирается быстро текстом" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **The two answers to the folding objection.** Pavel on the size: the tickets are "как… $100[,] ровненько" — wallet-sized, like a hundred-dollar bill. Klimovich on the barcode placement: "у нас в центре не будет баркода, у нас баркод как раз по бокам, в безопасной зоне[.] Там он никогда не пере[гибается]," and Pavel added "их 2 у нас[,] запасно[й]" — two barcodes, one spare. Val closed it: "и даже не в том дело[ —] никто их сильно держать не будет[,] этикет[ы]" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **The ruling:** "тогда мы пока ездим на одном тито[-]принтере" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]

*(Pavel also recalled seeing the thin-paper approach used and abandoned — a parking QR code scanned on exit — "работало, но потом от него отказались." Where is not resolvable: the transcript renders the place as "в данном олл." Recorded as unclear.)* [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]

## The enclosure for the show

Klimovich did not want the printer simply lying next to the Flex-IQ on the stand — "это не очень красиво, согласитесь[,] то есть нам нужен какой-то кейс." Val handed it to Genadi and told him to stop there: "Геннадию сделать этот кейс — это проще пареной репы. Это можно отпечатать… на 3D[-]принтере… сделайте простой[,] самый тупой [enclosure] — и едем дальше" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

Klimovich's supporting anecdote: a competitor they had seen **on the Friday** had shipped exactly that — "там тоже на 3D[-]принтере этот кейс распечатан, и очень некачественно. Но они это в продакшн запустили в таком виде." *(The competitor's name is rendered "elinks" in the transcript and is not resolvable; the derived notes say only "a competitor they saw on Friday." Not asserted.)* Val drew the lesson: "Все торопятся сегодня покорить рынок, кто сделает… тот будет контролировать" — *the middle of that sentence is garbled beyond reconstruction ("большим столещем")*. [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]

## Open commitments

- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — 3D-print the simplest possible enclosure for the TITO printer that sits beside the Flex-IQ on the stand — due before the show — [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]

**§15.8:** clear — device and consumable choice only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
