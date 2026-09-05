---
type: decision
title: The Flex-Port family splits at touch vs non-touch — the SAS variant is universal, the port must carry a scanner, and the cheap SAS SMIB board cannot be re-flashed remotely
date: 2026-09-02
aliases: [Flex-Port touch vs non-touch, SAS variant universal, scanner on the port, 10% of the market without a second SAS, flash-once board, 2 MB flash, remote firmware update threshold, two ports]
source-count: 2
status: active
open-commitments: 2
open-questions: 2
---

# The Flex-Port family splits at touch vs non-touch, and the SAS variant is universal

The engineering constraints that closed the strategic half of the [[wiki/meetings/2026-09-02-flex-iq-pre-pilot-updates-after-the-show.md|Sept 2 2026 Flex-IQ pre-pilot call]]. It refines, and does not overturn, [[wiki/decisions/2026-08-24-flex-port-mini-via-second-sas-only.md]].

## What was decided

- **JVL goes with the SAS variant as universal and does not chase machines without a second SAS.** [[wiki/people/pavel.md|Pavel Frolov]]: "мы идём в сас вариант. Котор[ый] нам универсальный и не будем пытаться закрыть там 10% рынка где нету 2 сасса." [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]: "Всё так" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]. *(Note: on Aug 24 Val put that same excluded segment at "гдето 15 20% рынка" — see Open contradictions on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. Both figures are recorded; neither is resolved here.)*
- **The port — or the Flex SMIB — gains the ability to connect a scanner.** Pavel: "мы ставим на флекс. Порт или на флекс сми возможность подключения сканера." He drew it as a consequence of the wallet direction: "если [и]волит это наше основное направление… [то] на фле[к]спорт должен содержать в себе [баркод]сканер. То есть вот этой вот платы будет недостаточно… которая сасовская сасовский сми[б]. Ну, либо сделать новую ревизию этой платы, у которой будет возможность подключения сканера." [[wiki/people/val-levitan.md|Val]]: "Да, конечно" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **There will be two ports, and the boundary is touch vs non-touch.** Val: "Я вижу, что у нас будет 2 порта. Это как бы… [Флек]спорт сегодняшний, который широкий. И флекс порт [слим] такой" — adding "сми плохое слово, но назовём его [так]". Andrei offered the cleaner line and Val took it: "Может у нас разница между флекспорт[ом] тач и флекспорт[ом] Нот тач, то есть вот здесь лежит граница по большому счёту" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **A simple non-touch screen closes all the tasks — unless a PIN is required.** Andrei had prepared "матрицу 3 вариантов реализации [флекс]экспорта с точки зрения наличия или отсутствия экрана," mapped "по всем возможным интерациям и информационному обмену с игроком," while admitting "я думаю, что это не полная матрица." His verdict: the needs could technically be met with **no screen at all**, "на уровне [диодов]… диодная коммуникации и [пре]принятый [инструкции]," but "мне кажется, это откат в прошлое" — emotionally a step backwards. "Поставить простой экран не тачскрин… И это закроет все наши задачи. При условии, если пин код не нужен… как только появляется требования пин кода… это тачскрин или какаято физическая панель с кнопками" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **A small touchscreen is probably cheaper than a keypad.** Pavel: "сейчас физическая панель будет стоить, наверное, дороже, чем… Экран с тачскрином маленький… там не сем[ь] инчей… там 4 [инча] будет, наверное, дешевле стоить, чем панель с кнопк[ами]." Andrei accepted it and named the commercial cost: "тут у нас, конечно, вот это флексиби[лити]… уже несколько страдает… мы не можем прийти к оператору и сказать вам нужен пинкод[?] он скажет да[,] ну тогда вот только тачскрин, к сожалению" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **The PIN survives as a switchable per-location option.** Val: "Я бы пинкод не убивал, но я б[ы] сделал бы как фичер"; Pavel supplied "Option" and reported Andrei's written position: "Андрей там написал, что пинкод это опция, которая может включаться для лакейшна или выключаться в зависимости от Того, как захотят операторы." Andrei added the boundary case: "если [e]оля создаётся на IQ… там кассиром[,] то никакого пинкода здесь быть не может. То есть это уже без пинкодовая система тогда" — a wallet created on IQ by a cashier is PIN-less by definition. This updates [[wiki/decisions/2026-08-24-drop-pin-from-evoucher-flow.md]] [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].

## The memory constraint that shapes the cheap board

- **The cheap SAS SMIB board cannot support remote firmware update.** Pavel: "вот этот вот вариант, который сас смибовский… Он не сможет поддерживать [ремоут] фирм[вар] апдейт. У него просто нет памяти лишней, он использует встроенную… [с]рам… это вариант тогда такой, который один раз прошили и всё" — a flash-once part [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **The numbers, as spoken.** The cheap board has, Pavel thinks, "2 мегабайта флэш памяти. Всего лишь." For the full Flex-Port he was unsure of the figure — "я там не знаю, сколько сейчас памяти это помоему 128 чтото такое было" (unit not stated, and he flagged his own uncertainty) — but was clear on why it can be re-flashed: "там стоит внешняя микросхема флэш и внешняя микросхема ещё [с]рам памяти. И… За счет этого есть возможность прошивки" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **Adding remote update raises the cost "significantly".** Andrei asked "Насколько удорожа[е]т сам флекспорт[,] если мы добавляем ему возможность удалённого [фирмвар] апдейта"; Pavel: "Значительно, как показывает практика, сейчас даже вот просто ставишь память там флаш[ — это] Значительную часть от стоимости платы." He cited the live counter-example: "Геннадий сейчас там занимается с алексеевым тем, чтобы заменить одну микросхему на другую[,] Там в 4 раза меньше памяти[,] она значительн[о]… экономит деньги" — [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] are swapping one chip for another with four times less memory to save money [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **Val's read: 2 MB → 4 MB is insignificant money.** "если здесь всего 2 мегабайта памяти… даже если нужно чтото обновить… На 2 процента увеличится[,] на 5% увеличится… На 20%… На 50[?]" and earlier, plainly: "Вот эти 2 мегабайта, даже если их расширить на 4 мегабайта, это ж незначительн[ые]… деньги." Pavel: "Скорее всего так" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **Fallbacks if remote update is dropped.** Pavel: "прийти с лэптопом, подключиться и прошить — это самое такое в лоб решение[,] оно будет работать для самого дешёвого варианта." Chudinov: "Может, даже быстрее будет приехать с готовым. Заменить" — and Pavel agreed, "может быть проще заменить, тогда приехать, заменить парк… Портов. Если они легко устанавливаются туда" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].

## Val's method: work out what could need updating, and the frequency follows

Rather than guess the update frequency, Val redirected: "Разговор нужно повернуть в другое русло. Если… есть такой [кейпэбилити] как [firmware update,] то, что конкретно можно[?] Если мы знаем, что конкретно можно [апдейтить], тогда можно себе представить, как часто это, скорее всего, возникнет" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]. Working the examples on the call:

- **Scanner driver:** Val — "Поменяется ли какой то драйвер на[…] Скэн[ер]"; Pavel — "Нет, никогда не поменяется, я думаю" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **SAS itself:** Chudinov thought a change to SAS unlikely and JVL-side implementation more likely: "скорее не поменяется, скорее мы решим доимплементировать недостающие команды" — for instance new statistics or counters. "любой новый [эквипмент] и новая [капабилити]" would need an update, and "любое движение в будущее" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- Andrei's summary of the value of the exchange: "отлично, что этот вопрос подсветили" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].

## Open commitments

- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — answer at what memory size remote firmware update becomes possible, and whether that can be set as a requirement; Pavel referred the question to them ("это мы можем переадресовать этот вопрос геннадию и Евгению алексееву… Я этим вопросом не занимался") — due unspecified — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]] [[raw/Meeting_Notes_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — send the team his three-variant Flex-Port screen matrix ("я сейчас скину вас после звонка") — due right after the call — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Open questions

- At what flash size does remote firmware update become possible, and what does it add to the port cost? Referred to Genadi Peari and Evgeniy Alekseev; Pavel could not price it ("По цене сейчас не смогу") — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- Is the SAS SMIB board simply insufficient for the wallet direction, or does it need a new revision with scanner support? Pavel put both; Val agreed with the conclusion but the branch was not chosen — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Sources
- [[raw/Meeting_Notes_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
