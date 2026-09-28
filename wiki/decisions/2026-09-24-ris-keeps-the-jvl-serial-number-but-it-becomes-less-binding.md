---
type: decision
title: A RIS stays linked to the machine's JVL serial number, but the link becomes less binding — kept in the background for the record
date: 2026-09-24
aliases: [less binding not less relevant, keep it for the record, RIS serial binding, use case 2, several RIS files on one USB stick, one RIS for many machines, this is not for this machine, multi-machine RIS parameter]
source-count: 1
status: active
open-commitments: 0
open-questions: 1
---

# A RIS keeps the JVL serial number, but binds less

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-24-ris-serial-binding-and-factory-reset-focus.md|Sept 24 2026 7:02 AM RIS follow-up]], on use case 2 of his eight. All quotations from [[raw/Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026.md]].

## The question

Val: "Can we have this RIS built for multiple machines?"

- **Several files on one stick already works.** [[wiki/people/pavel.md|Pavel]]: nothing prevents creating "multiple RIS files, each for each machine, but place it on one USB stick. It works right now… It works last four years, I assume." He preferred this to one file for all machines: "you can either put all the files on one stick or split it to several."
- **The field had not been told.** [[wiki/people/felipe-miranda.md|Felipe]]: "I is the first time I hear that… in the instructions is very clear that there could only be one file". [[wiki/people/sebastian.md|Sebastian]] had done it: "When we did installations here in Florida, actually one copy, for example, 8 files onto one USB and apply one by one in each machine."
- **Each file is still tied to a serial number.** Asked, Sebastian and Pavel both said "Yes."

## How operators name machines (Felipe)

"some large companies have asset numbers… Some others go by the column ID, not many. And very, very few even have JVL serial number and record." The "column ID" / "call MID" of the transcript is read as the **COAM ID** (**inference**). It cannot anchor a RIS: "call my ID changes every time the machine is commissioned… at least in Georgia". An asset-number field already exists "in the SAS tab… but they never use it."

## The ruling

Val's scenario against unlinking: one operator buys another and merges 15 machines "under one roof" — does he want to know "which serial number of machines he purchased"? Then:

> "we could continue monitoring, but make it less relevant… less binding, I should say, not less relevant, but less binding… should we record it and keep it in the background just in case somebody needs it… I think that's exactly what we should do. I kind of talked myself into it. We should still continue recording this, but make it less binding on… the setup. Just keep it for the record purposes and that's it. In the background."

Felipe's view, before the ruling: "if I'm a technician, and I don't have to worry about that, that's ideal."

## How it could work — two options, none chosen

- **A warning.** Pavel: if the RIS on the stick is not for this machine, "We can provide message, this is not for this machine. Still use this RIS", and apply it if the technician confirms. Felipe: "it's saying this is not supposed to go here, but if you want to do it, you're on your own."
- **A server-set parameter.** Pavel: "Parameter could be added within the RIS file that will allow this particular RIS file to use on several machines", controlled from the server when the RIS is created for several machines.
- **What JVL still learns.** Val: the passport is still scanned and the serial number still captured, so the database can say where a RIS was installed. Pavel: "We do not know exactly on which machine", especially with a USB stick and no final QR scan — which is why Val kept the final scan (see [[wiki/decisions/2026-09-24-multiple-qr-scans-go-and-one-final-activation-scan-stays.md]]).

## The limit Val set the same meeting

Loosening the serial link does **not** mean any RIS on any machine. Applying dual-screen settings to a vertical machine gives "a crooked setting", and Felipe agreed "machine will still be out of service". Val: "Okay, so restricted. Do not allow." The passport-to-hardware match stays — see the Sept-24 update on [[wiki/decisions/2026-09-11-the-passport-is-preserved-and-jvl-is-using-the-bindings-wrongly-in-this-market.md]].

## Open questions

- Which mechanism carries a RIS to several machines — a warning with confirmation, or a server-set multi-machine parameter? — [[raw/Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026.md]]

**§15.8:** clear. **§15 #9:** clear — Felipe's example machine serial number is not recorded.

## Sources

- [[raw/Meeting_Transcript_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026.md]]
