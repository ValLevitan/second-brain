# Meeting Summary — Hard reset Issues in Georgia
**Date:** September 24, 2026, 5:41 AM – 6:26 AM Eastern
**Duration:** About 45 minutes
**Attendees:** Pavel Frolov (chair), Irina Shishko, Evgeny Kharetski, Ivan Shpak
**Raw transcript:** [[Meeting_Transcript_Georgia_Hard_Reset_Remedies_and_Passport_Removal-September-24-2026]]
**Source:** Teams transcript export supplied by Val
**Related:** [[Meeting_Notes_RIS_and_Passport_Hard_Reset_Burden-September-23-2026]], `Day Prep/RIS_hard_reset_meeting_2_prep_pack-September-24-2026`, `Felipe_Miranda_Hard_Reset_Impact_Analysis-September-22-2026.pdf`

## Summary

Spoken in Russian. Pavel worked down the list of complaints Felipe collected from Georgia operators, case by case, against a PDF attached to the meeting. The purpose was to separate what can be fixed in the next releases from what is medium-term.

**The core problem.** JVL machines sit idle too long in Georgia, because bringing a downed machine back up is a heavy procedure. A factory reset means decommissioning and commissioning with Intralot, which takes time, and that is the small part. The bigger cost is everything that follows.

**Bill acceptor swaps trigger the passport.** Operators change bill acceptors often and do not need to decommission to do it. JVL does not have the "monitor" flag set on that, so the passport only demands an update the next time software is reinstalled or a factory reset is done. That is the first case.

**The software and RIS file on a USB stick.** To do a factory reset the technician must have the correct software version, and the stick may not be at the location, so someone has to travel or be called. Irina's point: instead of a factory reset they do a full installation. Pavel's answer is that an ordinary factory reset keeps the version that was already there, so this is easily solved. Ivan added that no key is needed, just run the reset and press the button.

On RIS files, Felipe gives every machine its own USB stick with its own RIS. They should be told **one USB can carry the RIS files for the whole bank**, inserted in turn. Ivan asked why it is not pulled over the network; most locations have no network or internet. Pavel confirmed RIS can be downloaded over the network where there is one, and once the modem goes into new machines this problem disappears.

**The passport QR is the worst of it.** After a factory reset a screen appears that the technician cannot get past. He has to photograph the QR, send it to the JVL representative, and wait for a reply, which has to come back within about 15 minutes before work can continue. Ivan asked whether the lease user on the web could simply be handed out so they can scan it themselves; the answer was no, that is internal only and external people must not have it. He then suggested a user with rights limited to scanning the passport.

**Pavel's decision was to remove it instead: disable the passport check for Georgia builds.** Evgeny said that in general it is doable. Irina raised the consequence on the server: when RIS is created the server only offers machines that match the passport, checking things like bill acceptor and printer, so removing the passport will cause conflicts. The answer agreed was a server flag meaning "do not filter, show all machines". Irina also confirmed RIS creation already offers only machines originally registered in Georgia.

Irina added a second parameter to check: whether technicians must scan statistics during a factory reset. There are two separate things, the secure factory reset (which requires the flash drive) and the QR scan. The parameter exists and is currently on, and for Georgia it could default to off, which makes the factory reset lighter again. Pavel will ask about it today.

**Battery replacement.** Operators say that if the battery is changed with the machine powered on, everything continues normally, but if it is changed with the machine off and then powered on, they get a yellow screen. Felipe reported it as the CPU battery; Pavel thinks it is the I/O board battery. Pavel asked whether the old "replace I/O board" handling has been broken for a long time. Ivan will test it on the vertical Georgia machine behind Irina that still has the bad battery. Pavel and Irina both said the low-voltage error is beside the point: by the operators' description, any swap with the power off should produce the yellow screen.

**Three kinds of reset.** Pavel's idea was to offer choices on the factory-reset window rather than one full wipe. Evgeny said a hidden mechanism already exists that few people know about: a file store holding **every RIS ever applied to the machine**, where the latest is identified by file number, not by time. So the machine could restore the last RIS without the full procedure. The complication is progressives: if it was not self-hosted, the machine needs to know what to connect to. Pavel's point is that this removes the whole "someone must fetch the right RIS file" problem even if the technician still clicks through the steps and picks the progressive.

The three cases Pavel wrote down:
- **A — full factory reset**, as today.
- **B — factory reset restoring the last RIS** from the stored history; still click through some steps.
- **C — soft reset**, clearing meters and state only.

Evgeny pushed back on C, asking what it is for, and said there are too many situations to handle. Irina explained the original intent: keep everything and clear only the part the bug touches.

**Money on a soft reset is unresolved.** Evgeny raised a stuck transfer or money error: someone walks away from $5, the machine errors, the technician does a factory reset and the money vanishes. Asked how it is handled today, Irina said either he fixes it or he does a factory reset with reinstallation. Pavel described a second soft variant that clears the money error but keeps all other meters and games, then asked aloud whether the money stays on the machine or is taken off. No answer was reached.

**Progressive controller.** Irina reported that Felipe believes JVL does not send RIS with the progressive, which means he configures it by hand. Her suggestion: if there is only one machine in the progressive controller, do not make the technician press three times; select it and move on. Evgeny objected that the technician may need another one that is not shown, for example after a machine went away for a network card repair. Irina narrowed it: that applies when there are several machines in a bank, not when RIS is for a single machine pointing at itself with default values only.

**A single game crash.** Irina asked what happens when one game falls and today the answer is a full factory reset. Evgeny asked whether she wanted the machine to analyse on startup which game crashed, read the logs and disable it. She said she is still thinking, and that it is for the future, not today. Evgeny said he liked the idea of disabling games on the fly.

**Retrofitting a printer as TITO.** Operators want to insert a printer into a machine that is already configured and have it work as TITO, which today needs RIS again. Evgeny asked who writes these requests; they come from customers through Felipe. Irina stressed these are the real people running the machines. Pavel's proposal was to modify the RIS system on the machine so some parameters that arrived with RIS can be changed by hand: do the factory reset with RIS restore, then at the payout order step add the printer and set its position.

That is where Evgeny put the framing question: **is this list to be built now, or gathered and done properly later**, in the Rust services or the current ones. Pavel's split: removing the passport is easy and takes out a big chunk of the problems, and RIS restore from backup also looks simple, so both can go into the nearest releases. Soft resets and partially manual init are medium-term. He was not sure whether that belongs to RAGE or to NOVA, possibly both. Evgeny's own answer on the printer request was clearer: with services you can ask a device on the fly whether the printer is connected and splice it into the payout order, so **that request goes into NOVA**.

**Init and missing devices.** Pavel asked how init works now. Evgeny corrected him: at init all processes start and the machine tries to discover the available printer, bill validator and so on, precisely so init cannot pass when RIS asks for a printer that is not connected. Pavel asked whether passing init without the device should be allowed; Evgeny said the machine would then sit in tilt. Pavel recalled Felipe wanting to pass init in the office and fit the printer at the location, but judged it artificial and risky: people click through, leave, and the machine still does not work.

**Installer error messages.** The installer reports that it cannot find the card. Pavel wants that split into "cannot find I/O board" and "cannot find counter board" so technicians can act on it. He called it an easy fix and mostly his own question.

**Lease mismatch, and a bigger question underneath it.** A bank of six machines gets an installation; the technicians reinstall software on the four that were down and leave the two that kept working. Weeks later, when RIS needs updating, they scan the lease and are told the software is wrong. Evgeny asked why they would reinstall on four and not six; nobody knows, and the machines are usually not on a shared network. Ivan said if they want to do that, they should reinstall on all of them.

Irina's view is that if the factory resets are made easier this becomes rare, maybe twice in a thousand machines. But the discussion then turned to **why purchased machines carry a lease at all**. Georgia machines are mostly bought outright, Irina said 90 to 100 percent. Ivan noticed that some fully paid machines have the lease-scan box crossed, meaning they were installed with no lease, so the mechanism may already exist; but many fully paid machines did have leases running to September 22. Either someone maintains it by hand or there is an automatic mechanism, and nobody in the room knew which. Agreed: review it on the server and turn leases off where the machine is sold.

**The critical error screen tells nobody anything.** When the technician scans it, the only message is that information was sent to customer support. No description of the problem. Irina's point: nobody knows where that support sits, what the problem is, or why the yellow screen appeared. Pavel recalled discussing a common explanation tool on the server about three years ago; Evgeny said it was more like six. The idea raised now is to keep a database of the QR strings and use AI to parse them and name the likely problem. Evgeny said it needs separate thought and would not be solved that day.

Pavel closed with his read on the whole list: **the short-term fixes alone probably close about 70 percent of the problems.**

Val messaged during the meeting wanting to discuss the new Galaxy immediately. Irina replied that they were in a local meeting.

## Decisions Made

- **Disable the passport check for Georgia builds.** Pavel said the work is not hard, it should just be planned and done, and it removes a large share of the complaints. Evgeny agreed in general. (Decided by Pavel Frolov)
- **Add a server flag to stop filtering machines by passport at RIS creation.** Required because removing the passport otherwise causes conflicts against bill acceptor and printer checks. (Decided by Pavel Frolov, after Irina Shishko raised it)
- **Add "restore the last RIS" as a factory-reset option**, using the existing store of every RIS ever applied, chosen by file number. This is case B of three. (Decided by Pavel Frolov, mechanism confirmed by Evgeny Kharetski)
- **Passport removal and RIS restore go into the nearest releases; soft resets and partially manual init are medium-term.** (Decided by Pavel Frolov)
- **The printer and TITO retrofit request is implemented in NOVA, not now.** Evgeny called the request a bit cheeky and said services make it far easier. (Decided by Evgeny Kharetski)
- **Init will not be allowed to pass with a missing device.** Pavel judged the office-init idea artificial and risky; Evgeny said the machine would sit in tilt. (Decided by Pavel Frolov and Evgeny Kharetski)
- **Split the installer's "cannot find card" message into I/O board and counter board.** (Decided by Pavel Frolov)
- **Review leases on the server and remove them where the machine is sold.** (Decided by Irina Shishko, agreed by Evgeny Kharetski)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Ivan Shpak | Test the battery case on the Georgia machine with the bad battery: power on, let it sit, power off, swap to a known-good battery, power on, and confirm the yellow screen | Today (Sep 24, 2026) | High | He said he would do it right after the call |
| 2 | Pavel Frolov | Ask today about the statistics-scan parameter on factory reset, and whether Georgia can default it off | Today (Sep 24, 2026) | High | Separate from the secure factory reset parameter |
| 3 | Pavel Frolov | Plan and schedule the removal of the passport check from the Georgia build | TBD | High | He called it the single biggest easy win |
| 4 | [Unassigned — needs Val's or Pavel's confirmation] | Add the server flag that stops filtering machines by passport | TBD | High | No owner was named in the meeting |
| 5 | Irina Shishko | Review on the server whether leases are needed on purchased machines, find out what regulates the lease-scan flag, and remove where not needed | TBD | Normal | Georgia is 90 to 100 percent purchased |
| 6 | Pavel Frolov | Split the installer's "cannot find card" error into I/O board and counter board | TBD | Normal | He called it his own question and an easy fix |
| 7 | [Via Felipe Miranda Giorgi] | Tell the Georgia operators that one USB stick can hold the RIS files for the whole bank | TBD | Normal | Today each machine gets its own stick |
| 8 | [Unassigned] | Consider auto-selecting the progressive controller when only one machine is in it with default values | TBD | Low | Irina's suggestion; Evgeny raised the multi-machine objection |

## Open Questions

- **On a soft reset that clears a money error, does the money stay on the machine or come off?** Pavel raised both; no answer was reached.
- **What happens when a single game crashes?** Today it is a full factory reset. Irina is still thinking; explicitly not for today. Evgeny liked disabling games on the fly.
- **Does this work belong to RAGE or to NOVA?** Pavel said he does not know, possibly both.
- **Why do technicians reinstall software on some machines in a bank and not others?** Evgeny asked directly; nobody knew.
- **What actually maintains the lease-scan flag on fully paid machines?** Either a person or an automatic mechanism; nobody in the room knew. Needs asking on the server side.
- **Is the battery yellow screen related to low voltage at all?** Pavel and Irina both doubt it.
- **A common explanation tool for the critical error QR.** Raised three to six years ago and never built. Evgeny said it needs separate thought and would not be solved that day.

## Notes on the transcript

Russian, kept verbatim, from a Teams transcript export. Frequent mis-transcriptions; readings used above come from context:
- **"фэктори ресет" / "fectery" / "эфэр" / "фро" / "fre" / "froлись"** — all **factory reset (FR)**.
- **"рис" / "риса" / "рисом"** — **RIS**. **"интролот"** — **Intralot**. **"тито"** — **TITO**.
- **"паспорт"** — the **passport** check. **"лиза" / "лиз" / "лизу"** — **lease**. **"фули пэйт" / "фулипы" / "folipay"** — **fully paid**.
- **"белоксептор" / "билаксептор" / "пилосептору"** — **bill acceptor**. **"каутерборд" / "гантербург" / "counter bort"** — **counter board**. **"ай борт" / "i obord" / "ii bobort"** — **I/O board**.
- **"ни цитап" / "ни шестапа" / "иницитап" / "не цитат"** — **init setup**. **"паяут ордер" / "тордер"** — **payout order**. **"в силте" / "в сил"** — **tilt**.
- **"мани эрор" / "мани эр"** — **money error**. **"митеры" / "митаров" / "метров"** — **meters**. **"кюар" / "q rку" / "qар"** — **QR code**.
- **"рейдж"** — **RAGE**. **"нова" / "внова"** — **NOVA**. **"растовских"** — **Rust** services.
- **"Филиппа" / "Филипп"** — **Felipe** (Miranda Giorgi). **"джвелевскому"** — **JVL**.
- **"прозу"** appears in the same sense as in the Sep 24 standup and is left as transcribed.
- One passage renders an idiom crudely ("либо снимите крестик, либо трусы оденьте"); it is Pavel saying the operators cannot have it both ways. Left verbatim.

## Dispatch Log

---
*Processed from Teams transcript export on September 24, 2026*
*Source meeting: Hard reset Issues in Georgia*
