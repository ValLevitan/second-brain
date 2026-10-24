---
type: decision
title: To sell in Georgia, JVL must win back the operators' technicians by making its machines easier to service — the lighter RIS release in November is step one, then tools for technicians, and every Minsk engineer is asked to think as a technician (Val, Oct 23 2026)
date: 2026-10-23
aliases: [technician loyalty, win back the technicians, technicians hate the JVL machine, научились ненавидеть нашу машину, кого нужно удовлетворять, the technician is the one to satisfy, think as a technician, если бы я был технишен, tools for technicians, self-diagnostics with a QR code, SSD SMART check, bill validator reject rate, messages to the technician's phone, setup lock when money is on the machine, галочка если есть деньги, RTP 95.5 vs 92]
source-count: 2
status: active
open-commitments: 2
open-questions: 1
---

# To sell in Georgia, JVL must win back the operators' technicians

Set out by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-10-23-technician-loyalty-and-developers-as-product-owners.md|Oct-23 "coffee machine" chat]] (Russian) with [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/andrey-bosik.md|Andrey Bosik]] [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]. The notes list it as a decision: the goal for Georgia is to win back technicians by making their work on JVL machines easier; first step, the lighter RIS release in November [[raw/Meeting_Notes_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## The old explanation: payout (Val)

- **Two years of worry.** "Этот разговор начался года 2 тому назад": the fear was that JVL machines in Georgia make less money than the competition, because the game design did not match the market. Not all of it was wrong — the skill-feature rework "Это было хорошо" [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].
- **His numbers.** JVL's average RTP "Последнем выпуске был 95 с половиной" (some games at 94, some at 96 and more); competitors set games "гдето на 92 максимум… 90, 92". With all machines busy, he said, JVL would need "на 40% больше" play to make the same money — "это невозможно" [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]. Which release "last release" means is not said. Since Sept 25 Georgia machines are to go out at 92% — [[wiki/decisions/2026-09-25-georgia-machines-go-out-at-92-percent-and-the-progressive-tops-are-2400-2400-1500.md]].
- **Players sit longer, they do not bet more.** Pavel: players see JVL machines pay more and should sit longer. Val: a player may sit an hour instead of 40 minutes, "Поэтому они больше, они больше ставок не делают." Pavel: the active time per machine stays about the same [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].

## The new explanation: technicians (Val)

- **What he now sees.** After two years and many releases: the technicians in the companies that work for the operators "Научились ненавидеть нашу машину" [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].
- **Why.** They hate sitting on the line with the lottery ("с интерлотом", [[wiki/organizations/intralot.md|Intralot]]) to commission a JVL machine: "Это занимает полчаса до 02:00" (half an hour to two hours). Other makers need it only after a factory reset, but JVL does factory resets far more often, because of RIS and the passport, which force a factory reset and re-commissioning on setting changes or a peripheral swap. Val: "Я не хочу, чтобы мы уничтожили это. Хочешь мы просто правильно дизайне." [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]] This repeats the Sept-24 ruling — [[wiki/decisions/2026-09-24-reducing-factory-resets-is-the-one-urgent-fix.md]] — and the Sept-11 view that the passport stays — [[wiki/decisions/2026-09-11-the-passport-is-preserved-and-jvl-is-using-the-bindings-wrongly-in-this-market.md]].
- **Who must be satisfied.** "У меня поменялось проспекты кого нужно sotos fie… Удовлетворять сложно, ты кнышинов." Irina: "Хозяин получает мнение от технишина." Val: that opinion is insistent — in effect, "не покупай больше это говно" [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].
- **Commissioning time.** Bosik: a voice bot calling the regulator would not shorten the time; the technician still waits on site. Pavel: "тут ключевой момент… все те кейсы, которые можно сделать без… комишонинг сделать их" — for example a printer change. Irina: today the bill validator and the printer are what force the factory reset [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]. The voice bot: [[wiki/decisions/2026-10-21-pavel-frolov-is-product-owner-of-the-georgia-commissioning-chatbot-and-andrey-bosik-develops-it.md]].

## The plan

- **Step one: the lighter RIS in November.** "1 шаг это естественно… с выпуска нового вот этого облегчённого араэс в ноябре месяце." Earlier Val said "с начала ноября мы вводим" many changes, not all done yet [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]. The release: [[wiki/decisions/2026-10-20-the-ris-improvements-release-notes-are-settled-point-by-point-and-the-tasks-are-to-be-rewritten-to-match-them.md]] and, for Diamond, end of November (tentative) — [[wiki/decisions/2026-10-20-diamond-gets-the-ris-improvements-first-on-p1-p2-and-p3-at-the-end-of-november-and-the-two-machine-trial-is-extended.md]].
- **Then keep going.** "здесь нельзя останавливаться, надо дать так нынешнюю. Инструменты, вещи, чтоб они себя чувствовали удобнее и лучше." Step by step, a few changes at a time — "по одному по 2" — through small MVPs; Val expects to deliver this "в течение пару лет" [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].
- **Everyone in Minsk thinks as a technician.** Val: "если каждый сделает предложение, если бы я был так нынешен что бы я хотел бы… И я просто приглашаю всех. В Минске все. Думать на эту тему." Near the end: "Давайте будем собираться комментарии и мечтать". He thinks Alexei "может много чего сказать" (read as [[wiki/people/alexei-khamin.md|Alexei Khamin]], QA — **inference**) [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].

## Ideas raised (not yet tasks)

- **Self-diagnostics (Val).** The machine finds its own problems and says which parts to order, with a QR code on the panel or screen. Val: "Я сейчас начинаю мечтать" [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]. Related: [[wiki/decisions/2026-10-05-the-critical-error-screen-shows-the-cause-and-fix-in-words-and-keeps-the-qr-code-in-mvp1.md]].
- **Disk health (Pavel).** Check the SSD by SMART diagnostics; when errors start to build up, prepare a disk and send it, and swap it "даже без. Декамишонен комишонин", because a disk does not affect the identifiers [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].
- **Bill-validator reject rate (Val).** Track rejects per machine: "раньше был 5%, потом стал 10, потом 15. А сейчас… около 30%" — and tell the technician [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].
- **Messages to the technician's phone (Val).** This would let JVL talk to the technician directly. Not "20 страниц почитать", but the right information at the right time, by where he is: at the machine, after he left the location, or before he comes tomorrow [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].
- **A modem in the machine (Bosik, Pavel).** Bosik: with a modem mode "у нас развязываются очень сильно руки" — SMS, email, messengers. Pavel: collect many metrics and analyse them with AI [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].

## The setup lock when money is on the machine (not decided)

- **The question.** Pavel: Irina asked, while they worked on adding a printer on the fly, which other setup settings blocked today should be opened; with money on the machine, a tilt often clears only by a factory reset. Irina: the checkbox "если есть деньги, ничего нельзя в сетапе менять, она себя изжила" [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].
- **Why it exists.** Irina: it is not a GLI rule (Pavel had suggested checking the GLI spec); it was added long ago against casino technicians changing progressives on a live machine. Today games, show mode and its combinations, limits and denominations cannot be changed in setup anyway, so the lock now blocks harmless changes, such as a device with SAS. Progressives come with RIS and stay locked; Pavel and Irina gave the example of a technician setting a top prize to just under its maximum, winning it, and setting it back [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].
- **Val.** "Я не знаю я боюсь сдавать какойто ответ… около кофемашины. Мы сейчас этот вопрос не решим." [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]] Irina said a careful pass over all settings is still needed; the notes mark it as needing Val's confirmation [[raw/Meeting_Notes_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]].

## Open commitments

- [ ] Minsk team (all) — think as a technician and propose tools and features that make JVL machines easier to service; collect comments — due unspecified — [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]] [[raw/Meeting_Notes_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — go carefully through all setup settings blocked by the "money on the machine" lock (the notes: needs Val's confirmation) — due unspecified — [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]] [[raw/Meeting_Notes_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]

## Open questions

- Keep, reduce or remove the setup lock when money is on the machine? Progressives stay locked either way; Val did not decide — [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]] [[raw/Meeting_Notes_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]

**§15.8:** clear — no pay for technicians or anyone else was discussed. **§15 #9:** clear.

## Sources

- [[raw/Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]
- [[raw/Meeting_Notes_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026.md]]
