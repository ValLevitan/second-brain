# Meeting Summary — RIS_features
**Date:** September 23, 2026, 9:30 AM – 10:19 AM Eastern
**Duration:** About 48 minutes
**Attendees:** Val Levitan, Felipe Miranda Giorgi, Pavel Frolov, Irina Shishko, Sebastian Cortes
**Raw transcript:** [[Meeting_Transcript_RIS_and_Passport_Hard_Reset_Burden-September-23-2026]]
**Source document:** [[Felipe_Miranda_Hard_Reset_Impact_Analysis-September-22-2026.pdf]] — Felipe's written analysis, the document he presented in this meeting

## Summary

**Why the meeting was called.** Val opened by saying clearly that RIS is not a bad idea and is not designed badly. The problem is that RIS was designed when JVL was an operator in Latin America. Those requirements changed; the design did not. The result is now an emergency: technicians and service people who work for the operators refuse to work on JVL machines, and they tell their bosses not to buy JVL machines. Val has told those technicians and their bosses that JVL cannot fix this overnight, but will redesign the feature step by step and finish within one year. He thinks visible progress will keep them "pacified, not satisfied". He does not want to take a full year, because JVL cannot sell machines while this resistance lasts. The problem gets worse as JVL enters Texas and re-enters Nebraska — driving from one end of Texas to the other takes 10 hours.

Val set the method for the meeting: Felipe describes how it works today (the negative cases), the group decides what to throw away and what to keep, and what is kept becomes a new capability with a positive use case.

**Felipe's analysis: Passport is a symptom, the hard reset is the cause.** Passport creates friction because the technician needs JVL's help — JVL must scan the QR code before he can continue. But the real question is how many different conditions force a hard reset, and what a hard reset then obliges the customer to do.

A technician needs three things to get through a hard reset: the correct software version on a USB stick, the RIS file on a USB stick, and the passport code. Any peripheral change, such as a bill acceptor, forces a new passport. If he is missing any one of the three, his skill does not matter — the length of the outage is decided by what he happened to bring with him, not by his ability to fix the fault. JVL has about 15 to 17 different software versions across its history, and the software cannot be emailed: the old one is about 7 GB, the new one more than 9 GB. Felipe tells customers to leave the RIS file on a USB stick inside the machine, but JVL cannot control that — the technician can take it and it is gone.

**What a hard reset costs.** The machine must be decommissioned with Intralot before the repair. The technician calls the hotline, gives the location ID, address and port number, and waits. Decommissioning alone often takes 8 to 15 minutes. After the repair he must call again to commission the port, give the software version, and wait 10 to 20 minutes if everything matches — or an hour or two if it does not. Failure responses include "fail with no alarm", "cannot find software" and "wrong game", and then he power-cycles the site controller and the machine and calls again. If the hard reset was done before the call, Intralot must force the decommission, which now needs supervisor consent.

**The eight cases Felipe documented:**

1. **Battery replaced with the machine powered off.** There is a warning screen and a QR code telling the technician to scan before changing the battery, and technicians routinely ignore it. The machine boots straight into critical error, which nothing else can clear. Workaround found: replace the battery with the machine powered on — the machine shows "no battery" but keeps running normally. A five-minute job becomes a full decommission and recommission cycle.
2. **Software upgrade and reinstall.** JVL builds a new RIS file one at a time, per machine. For 20 machines that is 20 files. The customer drives to JVL to collect the RIS files and USB sticks, then drives to the location. On top of that, error code 2 or error code 3 appears during install across all software versions. The frequency rose after the new install flow was introduced, the one that asks the technician to confirm by pressing spin. The USB stick and the hardware have been ruled out — the same stick works on one machine and fails on another. Felipe reported it and no clear answer has come back.
3. **Software crash, freeze or software error tilt.** The tilt survives an ordinary power cycle. A clean reload of the exact software version is the only fix, and only if the technician happens to be carrying it.
4. **Peripheral configuration change** — adding or removing a printer, which now happens because TITO is being introduced for the transactional products. JVL builds a brand new RIS for that serial number, the machine is decommissioned, software reinstalled, and the passport screen is guaranteed to appear because the machine is not recognised without the printer. The QR goes to JVL, JVL returns the code, the technician enters it. **A JVL employee must be at a computer at that moment**, because the lease only becomes active after the machine is recognised.
5. **Boot loop.** Unexplained. It happened this week after an electrical problem at a location. The machine reaches the loading page and restarts. Only a hard reset clears it. At Diamond Amusement two machines in the same location boot-looped at the same time.
6. **Critical error from a hardware fault** — IO board failure, IO board not reading the counter board, a failing USB connection to the counter board, or a badly connected data chip. Repairing the board does not clear the error; a hard reset is still needed.
7. **RIS and lease mismatch at renewal.** JVL prepares RIS files machine by machine for, say, 20 cabinets. Sometimes one or two machines are not updated. When the lease expires the scan fails, and the only fix is a hard reset with the correct RIS or software — after waiting for JVL to supply it.
8. **The critical error screen itself tells the technician nothing.** A yellow screen with a large triangle and the words "critical error". Scanning the code only returns a message saying the information was sent to JVL customer support, and the word "information" is misspelled on it. The technician does not know whether it is the board, the battery or something else.

**The money, from Val.** A technician costs about $30 an hour, and a service provider charges the operator at least $60 an hour. Five hours of work is $300 out of the operator's pocket. So the operator often leaves the machine out of service for a day or two until a second visit. Locations average six machines, so when a JVL machine earns nothing the location starts asking for it to be removed. Service providers bill a master roughly $160 a month per location, so frequent visits make them lose money and they tell the master not to buy JVL. Technicians run five or six calls a day and cannot spend more than an hour per location including driving — if it is not fixed in 20 minutes they leave. Val added that in Georgia he has never driven less than one hour one way.

Val is expecting a utilization report from a large operator who collects, by his own account, nine million data points a day. Val's hypothesis is that JVL machines perform well when they run, but are down around 20% of the time, and the report should show the days with zero revenue.

**Val's proposed direction.** If a surgical fix is possible, do it. If not, disable the features entirely: a new software release that never references Passport and never references RIS, does not complain, does not ask for a QR code. Keep RIS only for the initial machine configuration, and make that load unrestricted — one load usable on many machines, with no reference to a machine number or passport number. He called this a step back, but the only sensible thing achievable in reasonable time. RIS would be redesigned properly later, for Omni.

**Pavel's response.** He raised two points. First, a factory reset has existed for more than ten years and, in about 95% of cases, does the same as reinstalling the software, without needing the USB stick — which would fix the "wrong software version in his pocket" case. Felipe said he is not comfortable using factory reset for a software error and would rather reload the software; Pavel accepted that a hard-drive error still needs a reinstall. Felipe also pointed out that a factory reset still needs decommission and recommission, because the meters go to zero, and Pavel agreed. Second, Pavel said Passport should not be requested after a reinstall if no device changed — but Felipe countered that changing a bill acceptor is very common and does force it.

Pavel pushed back on switching the services off outright: JVL does not support applying settings manually today, so Passport and RIS cannot simply be turned off. Val clarified that he still wants RIS for loading settings and only wants the other seven cases disconnected. On that narrower version Pavel said a next software version with the passport check disabled entirely is very likely and "not so difficult". He asked to go through Felipe's report point by point and estimate what is simple and what is not.

**One piece of good news.** Felipe said the team tested Megahit yesterday and the settings load through the modem — no RIS file needed. If every machine had that, it would solve a large part of the problem.

Val left the meeting at that point and asked the team to think overnight.

## What Felipe's Written Report Adds

The document is *Hard Reset Impact Analysis — Use Cases Requiring Improvement*, prepared by Felipe Miranda (Senior Sales Director and General Manager) for Val, dated September 22, 2026, marked "for executive review". It is filed next to this note. These points are in the report but were not said out loud in the meeting:

- **The scope is stated:** the Georgia COAM fleet, about **1,500 active JVL units across roughly 252 locations**.
- **The cost per event is stated:** a hard reset costs the customer **30 minutes to 2 hours** in normal conditions, and several hours or a second day when anything goes wrong. UC-7 (RIS and lease mismatch) is frequently a **multi-day** outage.
- **RIS means Remote Initial Settings.** The report points out the irony that a file with that name requires a physical round trip to JVL for every machine.
- **Intralot identifies machines by port, not by serial number**, and the game signature must match **Georgia Lottery** records at commissioning.
- **JVL's customers may be doing more work than Intralot requires.** The *Intralot COAM Hard Reset (RAM Clear) Procedure v1.0* defines a shorter path for a malfunction reset — call Intralot, perform the reset, call again to complete the RAM clear, run a coin test. In practice customers run a full decommission and recommission on every hard reset whatever the cause. Where a software or RIS reload changes the game signature the recommission is genuinely needed; where it does not, the customer is absorbing a longer process than the documented procedure requires.
- **UC-2:** the on-screen failure is "Deploy Failed", Error Code 2 or Error Code 3. The previous install flow loaded automatically with no user interaction. The investigation was requested from **engineering in Minsk**. Customers say plainly that software used to be loadable over the internet, and the report calls that visible regression damaging to JVL's credibility.
- **UC-4:** the manual JVL step is specifically that a JVL employee returns to **CMS** and starts the production lease, which cannot be activated until the passport code has been entered. The report's conclusion: **JVL becomes the bottleneck on the customer's own investment.**
- **UC-6 and UC-8:** the chip is the **Dallas chip (DSKey)**. The report lists four known causes of Critical Error, none of which the screen identifies — Dallas chip not seated properly, counter board connected to the wrong CPU port or disconnected, bad I/O board, and battery changed while the machine was powered off.
- **UC-7:** JVL can and does email RIS files, but it rarely helps in the field. Technicians do not carry a laptop to locations and do not want to; they want the file prepared and handed to them ready to use.
- **The report's closing finding, which the meeting did not discuss:** several of these conditions **need no engineering work on the cabinet at all**. They are procedural, documentation and messaging issues, and fixing those is the fastest available reduction in customer downtime.

## Decisions Made

- **Passport and RIS enforcement is to be removed from the current product line, keeping RIS only for the initial settings load** — the load must be unrestricted, usable on many machines, with no reference to a machine number or passport number. Val called it a step back but the only thing achievable in reasonable time. (Decided by Val Levitan; Pavel Frolov accepted the narrowed version after objecting to switching the services off completely)
- **Every blocker in Felipe's report gets its reference removed** — tilts, QR code prompts, whatever the report shows as a blocker. (Decided by Val Levitan)
- **Pavel and Irina will work through the report case by case, propose a solution for each and estimate difficulty**, rather than answering on the spot. (Decided by Pavel Frolov, accepted by Val Levitan)
- **RIS will be properly redesigned later, for Omni** — not now, and the capabilities will be discussed carefully at that time. (Decided by Val Levitan)
- **Follow-up meeting tomorrow at 7:00 AM Eastern.** *Considered and superseded: 9:30 AM, then 10:00 AM — both dropped because Felipe is showing the transactional product to ARC at 10:00.* (Decided by Val Levitan, Pavel Frolov and Felipe Miranda Giorgi)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Felipe Miranda Giorgi | Post the RIS and hard-reset report in the chat | September 23, 2026 | High | He said he would do it immediately |
| 2 | Pavel Frolov, Irina Shishko | Go through Felipe's report point by point, propose a solution for each case and estimate what is simple and what is not | September 24, 2026 | High | This is the main input for tomorrow's meeting |
| 3 | Pavel Frolov | Confirm whether a next software version can ship with the passport check disabled entirely | September 24, 2026 | High | He called it very likely and "not so difficult" |
| 4 | Val Levitan | Book the follow-up meeting for 7:00 AM tomorrow | September 23, 2026 | High | |
| 5 | Pavel Frolov, Irina Shishko | Translate Felipe's report into Russian for the team if useful | TBD | Low | Val suggested it, left to them |
| 6 | Val Levitan | Get the JVL utilization report from the operator who collects nine million data points a day | TBD | Normal | Expected to show the days with zero revenue |
| 7 | [Unassigned — needs clarification] | Investigate error code 2 and error code 3 during software install | TBD | High | Felipe reported it, ruled out the USB stick and hardware, and has had no clear answer to date |

## Open Questions

- Can the Passport and RIS problems be fixed surgically, or must the features be disabled wholesale? Pavel will advise tomorrow, after the point-by-point review.
- Is a factory reset a safe substitute for reinstalling the software? Pavel puts it at 95% of cases; Felipe is not comfortable with it for software errors. Not resolved.
- What causes error code 2 and error code 3 during install? Still unexplained. The USB stick and the hardware have been ruled out.
- What causes the boot loops? Felipe called it unexplainable; it follows electrical problems at the location, but the mechanism is unknown.
- Whether the Megahit modem settings load can be extended to every machine, and how quickly. Raised by Felipe, not discussed further.

## Dispatch Log

---
*Processed from Teams transcript on September 23, 2026*
*Source meeting: RIS_features*
