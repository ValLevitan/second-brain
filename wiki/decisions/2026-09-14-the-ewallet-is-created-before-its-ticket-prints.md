---
type: decision
title: The e-wallet is created the moment the player presses "print new" — before the ticket prints — so a printer failure cannot lose the money; the cashier recovers it from the transaction list
date: 2026-09-14
aliases: [create new then print, wallet created before printing, the painful scenario, carrier that did not print, ticket recovery, reissue versus reprint, print-carrier command, unclaimed money on the terminal, collect fork, блок номер 5 и блок номер 6]
source-count: 4
status: active
open-commitments: 1
open-questions: 4
---

# The e-wallet is created before its ticket prints

Settled at the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|Sept 14 2026 8:01 AM call]]. [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] called the failure it protects against "**самый болезненный сценарий**" — the most painful scenario — and said he had added the covering logic the previous day (Sept 13): "буквально вчера это было добавлено… вот этот блок номер 5 и блок номер 6" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## The fork that creates the problem

The **collect fork** on Flex-Port came out of the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|previous Monday's call]]; Klimovich called it "отличное требование, в общем, решает многие задачи." When the player presses collect on the machine, Flex-Port offers a choice: "**или просканируй свой [c]arrier прямо сейчас, и тогда деньги перенесутся на этот [e-]волет, или нажми кнопку [print new]**" — in which case IQ prints a ticket for a newly created wallet on its own printer, and the player walks to the cashier for it. What he does then is his own business, "возвращается к машинам или хочет ре[де]мшн сделать" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

[[wiki/people/pavel.md|Pavel Frolov]] confirmed the mechanics: "если он выбирает кейс[,] напечатай мне новый, то мы сразу… печатаем и транзакцию закрываем, то есть всё[;] у него на машине[,] уже на [Fl]ex порте ничего не остаётся… [а] тикет лежит у кассира" — the transaction closes at once and nothing stays on the port [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## The rule

**The wallet is created at the button press, not at the print.** Klimovich: "[в]олит создаётся, как только он нажал[, ] да, создай новый[;] мы создаём волет и грузим на него тот [game] cre[d]it баланс, который был на игровой машине[;] всё это закрыто, то есть **уже денежки сохранились**." If the ticket then fails to print "по какой[-]либо причине[ —] полностью умер принтер, нет бумаги, джем или ещё что[-]то" — the transaction must still be visible to the cashier [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

This is the concrete form of the framing rule Klimovich opened the meeting with: if a transfer fails midway in either direction, "**у нас всегда должна быть возможность сохранить эти деньги на одном из направлений изначальных, то есть не должно быть потери денег где[-]то при переносе**" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Why the port cannot just hold the money

[[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] explained how FlexPay does it today: wallet creation sits inside the output transaction, "то есть если принтер не работает, мы и не создаём это [e-]волят. Он не создастся" — no printer, no wallet, and the person is told why. [[wiki/people/alexander-biratka.md|Alexander Biratka]] pointed out that this cannot be carried over to the port, because there the money has already left the machine: "он на порте говорит, что я хочу создать [new] волет, и… он не может его создать[,] и получается, деньги… должны остаться на порте[,] до определённого момента, когда починят." [[wiki/people/irina-shishko.md|Irina Shishko]]'s instinct — "а хорошему они вообще на машине должны остаться" — runs into the same wall: "но они же не остаются на машине, они переходят на порт" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**Current Flex-Port behaviour, as Klimovich tested it.** On collect the machine balance is written down to zero at once and the money sits pending on the port; if nothing happens the wait expires — "[т]ам есть какой[-]то тайм[-]аут… тоже конфигурируемый… **но сейчас он что[-]то в районе 30 секунд**" — and the money disappears from view. Pavel: they are working on exactly this, do not know whether it can behave differently, tried and failed, "**[с]ейчас эту задачу отдал Жене Харецкому**" — handed to [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]]. Money not scanned in time "попадают там в [un]cla[imed]… на терминале их можно будет найти[;] вопрос, что с ними дальше делать" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## What the cashier gets — the firm part

Klimovich stated the non-negotiable outcome twice, and nobody disputed it: "**факт[ ]то[,] что да[,] нам надо кассиру показать транзакцию, показать[,] дать ему возможность её выбрать, идентифицировать и отправить команду[:] напечатай [c]arrier**… в случае, если он не был напечатан автоматом по какой[-]либо причине" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

A whole block of transaction capabilities carries it: on the IQ screen, "должна быть вся история транзакци[й —] созданны[е] [e-]волят[ы,] выпущенные карточки[,] любые операции", filterable. The worked scenario: the player says he played machine 3, the cashier filters the collect transactions, finds the one matching that machine and time, and issues the carrier [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**Identification stays verbal.** "Идентификация будет происходить на словах точно так же, как это сейчас происходит в случае [MudaGoose]. Да, это был я, это была… машина номер 3 и там было $50." Earlier in the call Biratka had asked how two players from different machines are told apart; Klimovich's answer was that the machine is not printed on the ticket, but the IQ transaction shows which machine it came from and the ticket carries a transaction or wallet identifier, so the cashier matches two tickets against the IQ screen [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Reissue versus reprint — argued, then parked

Klimovich had specified the recovery as a **reissue**: "не репринт, сохраняя этот, а сделать [reissue —] стар[ый] [e-]волят, котор[ый] только что был создан, закрывается[;] его баланс переносится на новый [e-]волят, и к нему печатается [ticket]." Two reasons: it preserves one wallet / one carrier, and it blocks a fraud where the player holds a photocopy of the current ticket [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

He was pushed back on from three sides:

- **Pavel:** a copy is not the threat, because "с одного тикета деньги можно один раз снять" — money comes off a ticket once. "Даже если 2 раза он распечатал, он один раз может только."
- **Klimovich himself conceded the symmetry:** "это то же самое, что если мы не создаём копию, а просто репринт делаем[ —] то же самое же может получиться[:] кто[-]то подошёл, сказал[, ] вот это я был на машине номер 3, мы делаем репринт[, ] и он забрал себе [c]arrier."
- **Biratka:** impersonation cannot be stopped at all here — "защититься от копирования тикета это практически нереально[, ] если мы не используем пин[-]код"; **Chudinov** closed that door: the reprint is done by the cashier, "там в принципе не может быть пин[-]кодов[;] тут уже они сразу отпадают."
- **Chudinov's alternative:** no new number at all — the wallet is created with a status, and pressing print moves it out of the unclaimed block: "он будет создан с определённым статусом, и как… нажима[ешь] распечатать[, ] он автоматически… меняется статус… [и] не надо ничего перепечатывать." Pavel agreed on the key point: "но под новым[,] под новым номером не надо."

Klimovich could not reconstruct his own reasoning — "**Да[,] я не помню[,] почему я пришёл к решению именно делать [reissue]**… может там есть какие[-]то подводные камни[;] я не помню, может быть[,] я передумал[,] слишком сложно сделать" — and parked it for both sides to re-read: "давайте пока подвесим этот вопрос" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Priority, if not everything lands

Klimovich accepted that the whole transaction-search block may not be finished for MVP 1 — "[д]опускаю, что не всё из этого может быть успето… это ничего страшного, но есть там приоритизация" — and gave the order: **first** showing the created transaction so a carrier can be produced, **then** the history of issued cards, which feeds the audit report [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

A small convenience sits in the same block: scanning the player's carrier on IQ filters the transaction list down to that wallet — "[и]грок даёт свой [c]arrier[, ] мы его сканируем на IQ[;] транзакции… в этом интерфейсе должны быть [от]фильтрованы по этому [e-]волиту" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Sept 14 2026, 12:04 PM — the same day, the same problem from the printer end, and the loss case this rule does *not* cover

Four hours later Val put the printing failure to [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/pavel.md|Pavel Frolov]] at the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|12:04 PM hardware call]] (Russian). He was asking about the standalone TITO printer enclosure, and the same money-must-not-be-lost principle came straight back [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]:

> "**человек же заплатил, он заплатил, ему надо получить свой этот тикет. Если что[-]то по дороге оборвалось — мы должны иметь возможность сказать: транзакция не прошла, отдать ему обратно деньги, или обратно подключиться, догнать транзакцию обратно.**"

**What the machine already does.** Pavel: "**мы своими этими библиотеками это читаем — если принтер отключить сейчас на машине, сразу тил[т] срабатывает; если его воткнуть обратно, тил[т] снимается**" — their libraries read the printer state; unplugging raises a tilt at once and plugging back in clears it. And the sensor Val asked for already exists: "**этот [сенсор] внутри принтера уже есть… если тикет полностью выехал, то мы это состояние имеем**" — the printer itself confirms the ticket fully exited [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**Where the money crosses over, and stops being recoverable.** "**если он не до конца допечатал — до какого[-]то момента ещё эти деньги могут вернуться назад. Но если уже баркот напечатал[ся] — деньги уже с машины снимутся.**" Up to a point the money can come back; once the barcode has printed, it has left the machine [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**The unsolved case — and it is deliberate, not accidental.** Pavel: "**скользкий момент здесь в том, что вот если уже тикет начинает выезжать, баркот на нём напечатался, и кто[-]то специально вырубает питание. Это тикет достанут. Он будет реально, его можно будет отоварить. Но при этом… мы не можем возвращать деньги обратно в такой ситуации.**" A deliberate power cut mid-print leaves a **real, redeemable ticket**, and the money cannot be put back [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

Pavel asked whether this was about the street machine's TITO variant; **Val said no — it is the TITO-printer-as-wallet flow**, i.e. exactly the flow this page governs: "**Нет, там, где мы пользуемся тито принтером, как и [wallet]**." Pavel then made the window **worse, not better**, for that case: "**мы только начинаем печатать — у нас уже есть баркод, который рабочий, вот на самом краю. Даже если чуть[-]чуть напечаталась — то уже всё. [Э]тот тикет просто достанут и будут использовать**" — a working barcode exists from the very start of printing, so even a sliver is enough [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**And the obvious hardware escape is closed.** Genadi asked whether these ticket printers reprint an incomplete ticket themselves — "**нет в этих тикет[-]принтерах… [что] он сам перепечатывает, если он не допечатал?**" Pavel: "**Нет.**" Genadi withdrew it: "**С чем[-]то путаю**" [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**How this sits against the 8:01 AM rule.** The two are not in conflict; they cover opposite directions of the same transfer. The morning rule protects the **player** — the wallet exists before the print, so a dead printer cannot swallow his money. The midday exchange exposes the **house** side: a ticket that partly printed is redeemable and the debit has already happened, so a bad actor can take the ticket *and* leave JVL unable to reverse. **Nothing in either source resolves the second case**, and no one proposed a mitigation. Recorded as a new open question below, not as a contradiction.

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — re-read the reissue capability and settle whether MVP 1 reissues the wallet or simply reprints the carrier — due unspecified, parked on the call — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## Open questions

- **Reissue or reprint?** Parked with three people arguing against reissue and its author unable to recall why he chose it — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- **Can collect money stay on the machine** instead of moving to the port the instant collect is confirmed? Pavel tried and failed; with [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- **A ticket whose barcode started printing before a deliberate power cut is redeemable, and the money is already off the machine — what stops that?** Raised by Pavel on the Sept-14 12:04 PM call and left with no answer; the printer cannot reprint an incomplete ticket — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- **What the cashier actually does with money sitting in "unclaimed"** — reprint a ticket, or something else. Pavel named it as the open part: "вопрос, что с ними дальше делать… кассир должен что[-]то выбрать" — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

*(The derived notes record the same rule — "the eWallet is created the moment the player presses 'create new' and the machine's game credit is loaded onto it, so the money is already saved" — and the same parked reissue-versus-reprint question. The notes render the print option as "print new" / "create new"; the transcript's rendering of the button is garbled, so no exact button text is asserted here.)* [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

**§15.8:** clear — money-flow design only; the "$50" is an illustrative player balance, not anyone's pay.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
