# Meeting Summary — RIS_features follow-up
**Date:** September 24, 2026, 7:02 AM – 7:59 AM Eastern
**Duration:** About 57 minutes
**Attendees:** Val Levitan, Felipe Miranda Giorgi, Pavel Frolov, Irina Shishko, Sebastian Cortes
**Raw transcript:** [[Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026]]

## Summary

This was meeting two on the RIS and hard-reset problem, after [[Meeting_Notes_RIS_and_Passport_Hard_Reset_Burden-September-23-2026|yesterday's meeting]]. Val had turned yesterday's transcript into **8 use cases** and circulated them. The plan was to go through them one by one. The meeting got pulled into design ideas, and Val stopped it near the end.

**Use case 2 — one RIS for many machines.** Pavel said several RIS files, one per machine, can already sit on one USB stick, and this has worked for years. Felipe had never heard of it; the instructions say one file only. Sebastian confirmed they did exactly this in Florida installs (8 files on one stick). Each RIS is still tied to the machine's JVL serial number.

**Should RIS stay tied to the serial number?** Val gave a scenario: two operators with different settings, one buys the other and merges 15 machines. Felipe said operators identify machines in different ways — some large operators use their own asset numbers, a few use the COAM ID, very few keep the JVL serial. The COAM ID changes every time a machine is commissioned (at least in Georgia), so JVL cannot link to it. There is already an asset number field in the SAS tab, but operators do not use it. Val "talked himself into" the answer: **keep recording the JVL serial number, but make it less binding** — keep it in the background for the record only.

Pavel offered two ways to do this: show a warning "this RIS is not for this machine" and let the technician confirm; or add a parameter inside the RIS file, set on the server, that allows one file on several machines.

**QR codes.** Val said the final QR scan after install still matters, because it sends JVL what was applied. Felipe said the real complaint is different: technicians now scan **up to six QR screens** in a row before they get the code (for lease and for Megahit data). Val explained this happened because QR was the only way to move a growing amount of data out of the machine. Two new use cases were added and confirmed by Felipe and Sebastian:
- **Use case 9:** remove the multiple QR scans.
- **Use case 10:** keep one final activation scan. It sends JVL the applied settings and the machine serial number, and returns an activation code the technician enters on screen. Pavel noted this is only for machines without a modem; with a modem it happens automatically.

**Installing any RIS on any machine.** Felipe asked how to stop a technician installing the wrong file. Val argued the passport scan is what makes RIS safe: JVL knows the CPU, IO board, monitors, topper, and MDEC or VDEC. Applying dual-screen/VDEC settings to a vertical/MDEC machine gives a broken setup and the machine stays out of service. His words: "when we are trying to kill a good thing, we might be killing an innocent person."

**Use case 11 — who scans the passport, and when.** Pavel said today only JVL staff can scan and update the passport, and asked if third-party technicians should be allowed. Val framed the question: scan only at the machine's "birth" (what other makers do), or rescan after hardware changes. His view: rescanning on first power-up after a change, updating JVL's database and sending a validation code is "a great feature" and not an issue. Pavel suggested external users could be limited to basic changes (printer, bill acceptor, monitor), without switching model type (vertical/horizontal, VDEC/MDEC). Sebastian asked whether a technician could scan the passport and get the code without logging into CMS.

**Hardware vs settings.** Felipe wants peripherals (bill validator, monitor, topper, printer) separated from software settings, with a yes/no screen during initial setup before the passport step. Pavel agreed some parameters could be made selectable during initial setup (printer and its order, bill acceptor), like Juan's earlier request to select games. Val asked to **add a picture of the machine** to the CMS installation flow, because not everyone knows what D27 or V43 means.

**Restore the last RIS after a factory reset.** Pavel said newer software keeps a copy of the applied RIS on the machine. After a factory or hard reset, the technician could choose to reuse it, with no USB stick for software or for RIS. Felipe called it a great solution for most cases (anything short of a software version change). Val agreed and called it an additional positive use case. Pavel added that machines on a local-area progressive network could already request RIS from another machine on the network. Val compared it to how an iPhone shares Wi-Fi settings.

**Val refocused the meeting.** The purpose was to find the low-hanging fruit that bothers technicians most. About **2,500 machines** are in the field, most without a modem, and modems will take time. The biggest issue is the time to recommission after a factory reset. If only one thing could be fixed: **reduce the number of factory resets.** He called it urgent and immediate. Felipe agreed. Pavel said the factory-reset case must be split into several cases. Val closed the meeting and set a third meeting for tomorrow at 7 AM on this one narrowed subject.

## Decisions Made

- **Keep the JVL serial number linked to each RIS, but make it non-binding** — record it in the background for reference only. (Val)
- **Use case 9 added: remove multiple QR code scans.** (Val; confirmed by Felipe and Sebastian)
- **Use case 10 added: keep one final activation QR scan** for non-modem machines — sends applied settings and serial number, returns an activation code. (Val; confirmed by Felipe and Sebastian)
- **Do not allow a RIS to be applied freely over mismatched hardware** — keep the passport-to-hardware matching. (Val)
- **Add a picture of the machine to the CMS installation flow** as a requirement. (Val)
- **"Restore previously applied RIS after factory reset, no USB" is an additional positive use case.** (Pavel proposed; Val and Felipe agreed)
- **Next meeting narrows to one issue: reduce the number of factory resets.** Urgent. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Schedule the follow-up meeting for 7:00 AM tomorrow on reducing factory resets | Sep 24, 2026 | High | Meeting three |
| 2 | Val Levitan | Add use cases 9, 10 and 11 and the "restore last RIS" case to the use case list | TBD | Normal | Val owns the circulated list — [Needs Val's confirmation] on owner |
| 3 | [Unassigned — needs clarification] | Add a requirement: picture of the machine in the CMS installation flow | TBD | Normal | Val asked "for the transcript"; Pavel asked where |
| 4 | Pavel Frolov | Split the factory-reset case into several separate cases for the next meeting | Sep 25, 2026 | High | Pavel's own point at close |

## Open Questions

- Use case 11: should third-party technicians be allowed to scan and update the passport, and should a rescan be required after hardware work? (Pavel, Val)
- Can a technician scan the passport and get the activation code without logging into CMS? (Sebastian)
- Which initial-setup parameters (printer, bill acceptor, topper, games) should technicians be allowed to change? (Pavel, Felipe)
- How to allow one RIS on many machines: warning plus confirm, or a server-set "multi-machine" flag inside the RIS? (Pavel)

## Dispatch Log

---
*Processed from Teams transcript on September 24, 2026, 10:20 AM Eastern*
*Source meeting: RIS_features follow-up*
