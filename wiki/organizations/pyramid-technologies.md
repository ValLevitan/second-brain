---
type: organization
title: Pyramid Technologies (ticket printers and acceptors)
date: 2026-01-08
aliases: [Pyramid, Pyramid Technologies, Pyramid printer, pyramid printers, пирамид принтер, пирамидовские принтеры]
source-count: 9
open-commitments: 4
open-questions: 2
---

# Pyramid Technologies (ticket printers and acceptors)

Pyramid Technologies (name from the Jan-8 notes title) makes the ticket printers JVL meets in the Texas market. [[raw/Meeting_Notes_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]] Its team works in **Mesa, Arizona**, with mechanical, electrical and software work "all under one roof". Pavel told the call that Pyramid printers are widely used in the kiosks of the Texas market. [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]

**Contacts:** "Jonathan" (who made the introduction) and "Kerry". [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]] Surnames Jonathan Durst and Kerrie Nollette appear only in the notes' Outlook-invite pairing. [[raw/Meeting_Notes_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]] **Tomislav Jeras** handled the NDA on Pyramid's side on Jan 22 2026. [[raw/Meeting_Transcript_Pyramid_Tomislav_Jeras_NDA_Scope_and_QR_Prior_Art-January-22-2026.md]]

## Jan 8 2026 — the introduction call

Stub: [[wiki/meetings/2026-01-08-pyramid-technologies-printer-integration-intro.md]]. JVL side: [[wiki/people/val-levitan.md|Val]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/genadi-peari.md|Genadi Peari]].

- **Why JVL called.** Pavel tied it to the Texas market: Pyramid printers "are widely used in the kiosks" there, and JVL is "going to repair the machines" (garbled passage); Val added "As an initial stage." Val also said JVL has "an expanded line of transactional equipment" coming to market later in the year and sees itself as a direct competitor to "Banilla" (as transcribed). [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]
- **Ticket look.** Pavel shared screen images of existing kiosk tickets (a "Banilla kiosk") and asked whether JVL should produce tickets that look like them; a "Yes." follows inside his own turn, so who answered is unclear. [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]
- **Connection and the QR code.** On a serial connection Pyramid pointed to its **ESC/POS** documentation and a "db9" cable or "rj4" (as transcribed). The **QR code on the ticket is generated automatically** from the payload JVL sends to the printer — JVL sends the data, the printer encodes it. [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]
- **Ticket configurations.** Some tickets (for example duplicates) may not need to be printed the same way; there are configurations to set up first, which Pyramid called "pretty industry standard". The passage is garbled. [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]
- **Kit.** A Pyramid speaker said Pyramid had sent a kit, with a mobile app / browser tool, so JVL can generate and test tickets. [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]
- **CAD file asked.** Val asked Kerry whether Pyramid can release a **mechanical CAD file** of the printer so JVL need not hand-measure it for integration into its machine, and asked that it go to Genadi (whom he introduced as director of the electromechanical department, in Toronto). Who confirmed is unclear in the transcript (the notes say Kerry did). [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]] [[raw/Meeting_Notes_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]

## Jan 8 2026 (afternoon) — the Texas side, heard at the Rich Winley lunch

The same afternoon, [[wiki/people/val-levitan.md|Val]] discussed the Pyramid set-up with Texas operator [[wiki/people/rich-winley.md|Rich Winley]] ([[wiki/meetings/2026-01-08-rich-winley-miami-lunch-texas-distribution-pitch.md]]). All from the transcript [[raw/Meeting_Transcript_Rich_Winley_Miami_Lunch_Texas_Distribution_Pitch-January-8-2026.md]]:

- **Where Pyramid sits in Texas.** Rich: game rooms "either run a pyramid system, or they're running a TITO system"; convenience stores, smoke shops and gas stations "run a pyramid system". JVL games could not yet join a Texas kiosk set-up: "You all aren't complying with the pyramid yet."
- **Timing Val gave.** "Pyramid printer, that's for the machine part. Yes, I think that will be ready within I'm gonna say 30 days by the end of the month. We actually had a call today."
- **What the tickets are for.** Val asked; Rich: "Just so the ticket prints out, they go scan in the kiosk and get cash", and some operators also use "count R" to read meters for audit. Val: "So for this test anyways, for the three machines, all I need to implement is the QR code."
- **The security worry.** Rich had heard from "a couple operators" that "people were taking pictures of the QR code. And the QR code starts to say 001, and they just keep scanning it until it gets to 100, so they're robbing the machine". Val: "This was my question when I saw this particular architecture… I don't understand their answer"; "I don't think it's a good system" — Rich: "I don't think so either." Val: "right now, I don't have to be a judge of the system. I just need to prove my machines", and JVL could "easily switch" if needed ("cheetah system" as transcribed — the notes read "cheaper system", an inference).

## Jan 22 2026 — the NDA scope call and Val's prior-art disclosure

Stub: [[wiki/meetings/2026-01-22-pyramid-tomislav-jeras-nda-scope-qr-prior-art.md]]. The derived notes overstate one point — they record a narrowed NDA as agreed; the transcript shows it only requested (see the stub). [[raw/Meeting_Notes_Pyramid_Tomislav_Jeras_NDA_Scope_and_QR_Prior_Art-January-22-2026.md]] [[wiki/people/val-levitan.md|Val]] alone with Tomislav Jeras; "John"/"Jonathan" named as the go-between. All from the transcript [[raw/Meeting_Transcript_Pyramid_Tomislav_Jeras_NDA_Scope_and_QR_Prior_Art-January-22-2026.md]]:

- **The use case, as Val put it.** A Texas customer's machines probably have Pyramid printers. JVL wants to sell him its kiosk, which houses a **Fujitsu cash dispenser**. The machine prints a winning ticket with a QR code; the player presents it at the JVL kiosk, which reads it and pays cash. Val assumed Pyramid controls the rule that turns the QR code into a value — "a handshake", decoded "with a key, a private key" — and wants that decoding built into the kiosk. Tomislav: "You've summarized it fairly."
- **Who is the buyer.** Tomislav asked whether JVL buys the technology or passes responsibility to the end customer. Val: "we are not operating locations. We will be selling the kiosk to a local operator", and "it will be a complete solution" — the operator is not expected to integrate it himself.
- **Val's NDA condition.** He will sign, but wants the NDA "narrow enough to protect your particular application" and not touch technologies that are "common knowledge" or that JVL "already developed". He does not want to "get into litigation" over prior art. He asked outright: "Do you want to narrow your MDA [NDA] to precisely what you're disclosing to me."
- **Pyramid's reason for the NDA.** To stop anyone "reverse engineering our tech, timesharing our technology with some sort of a cloud server" or using it "nefariously"; and to protect Pyramid from liability once JVL builds the "decryption into your kiosk" (the example: a customer "has lost, you know, 500 bucks, and it's your fault"). Tomislav offered to "go back to our legal team" to narrow it.
- **The prior-art disclosure — the core of the call.** Val stated, "full disclosure", that JVL already has "a very similar technology" shown at trade shows: a device with a screen that connects inside the machine and generates QR codes in front of the player (no printer); the QR can also be printed on "a regular TITO printer" instead of a barcode; and a player can generate an initial QR at the kiosk and use it "as a temporary e-wallet in the location", walking "from machine to machine". His point: "You're copying me. I'm not. I'm telling you that I already have it, and I have been showing it in trade shows." (the first sentence voices what Pyramid might one day claim).
- **The brochure.** Tomislav asked for a brochure or marketing material to put in Pyramid's "vault or file… kind of like a timestamp". Val: "Well, yeah, if you sign an NDA." Tomislav: "I see, I see. Okay."
- **Not a competitor in hardware.** Val: "I have no plans of manufacturing a printer or going into bill acceptor business. I've done that before."
- **Tone.** Tomislav: "I'm good with this conversation. I'll document it accordingly, and I think we move forward." He added that Pyramid "does not litigate in these regards" — in its "25 years", very few cases "actually went to litigation". He was to talk to someone "this afternoon at 3 o'clock my time" (who is unclear), circle back with John, and have "another discussion point tomorrow".

## History — before the call

- **Dec 16 2025.** Pavel proposed giving Evgeniy an investigation task on the Pyramid printer; Val answered "not now — let's sort out what exists now." [[raw/Flex-Port, Flex-POS sync and scheduling.md]] Three weeks later (Jan 8) Val himself led the introduction call — a change of course, not a contradiction. [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]

## Later in the corpus (pointers)

- **Feb 12 2026** — Pyramid's "platinum" acceptor reads barcode tickets (ECHO printer question). See [[wiki/topics/echo-home-gaming-device.md]]. [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- **Feb 25 2026** — Val describes the Texas scheme (Pyramid printer in the machines, Fujitsu in the kiosk) and refuses the broad agreement and the Pyramid "monopoly" it would bring. *(Five weeks after the Jan-22 call where he said he would sign a narrowed NDA — a change of stance over time, not a contradiction; no source in this wiki yet shows what Pyramid's legal team sent back.)* See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/Call_Genadi_Peari-February-25-2026.md]]
- **May 13 2026** — the IP 1007 dispenser's printer technology moves from Pyramid printers to Flex Port + Telekt. See [[wiki/projects/georgia-market-rollout.md]]. [[raw/Meeting_Notes_Schedule_Review-May-13-2026.md]]

## Open commitments

- [ ] Pyramid (Kerry, per the notes) — send the printer's mechanical CAD file to Genadi Peari — due unspecified — [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]
- [ ] Tomislav Jeras (Pyramid) — take the NDA back to Pyramid's legal side and to John, to "truncate" it to fit both sides — due "tomorrow" (Jan 23 2026) for a follow-up discussion — [[raw/Meeting_Transcript_Pyramid_Tomislav_Jeras_NDA_Scope_and_QR_Prior_Art-January-22-2026.md]]
- [ ] Tomislav Jeras (Pyramid) — document Val's prior-art disclosure ("I'll document it accordingly") — due unspecified — [[raw/Meeting_Transcript_Pyramid_Tomislav_Jeras_NDA_Scope_and_QR_Prior_Art-January-22-2026.md]]
- [ ] (blocked-on: signed-NDA) Val — give Pyramid a brochure / marketing material on JVL's QR solution, only once an NDA is signed — due unspecified — [[raw/Meeting_Transcript_Pyramid_Tomislav_Jeras_NDA_Scope_and_QR_Prior_Art-January-22-2026.md]]

## Open questions

- What final NDA language did Pyramid's legal team send, and did the follow-up call promised for Jan 23 2026 happen? — [[raw/Meeting_Transcript_Pyramid_Tomislav_Jeras_NDA_Scope_and_QR_Prior_Art-January-22-2026.md]]
- Which ticket types does JVL actually need to support in Texas? Val is to ask JVL's Texas connection and revert to Pavel. — [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]
  - *Partly answered the same afternoon for the three Texas test machines only: "all I need to implement is the QR code" (Val, after asking Rich Winley). Whether Rich is the "Texas connection" meant is an inference, and the wider Texas answer stays open.* [[raw/Meeting_Transcript_Rich_Winley_Miami_Lunch_Texas_Distribution_Pitch-January-8-2026.md]]

## Sources
- [[raw/Meeting_Notes_Pyramid_Tomislav_Jeras_NDA_Scope_and_QR_Prior_Art-January-22-2026.md]]
- [[raw/Meeting_Transcript_Pyramid_Tomislav_Jeras_NDA_Scope_and_QR_Prior_Art-January-22-2026.md]]
- [[raw/Meeting_Notes_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]
- [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]
- [[raw/Flex-Port, Flex-POS sync and scheduling.md]]
- [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- [[raw/Call_Genadi_Peari-February-25-2026.md]]
- [[raw/Meeting_Notes_Schedule_Review-May-13-2026.md]]
- [[raw/Meeting_Transcript_Rich_Winley_Miami_Lunch_Texas_Distribution_Pitch-January-8-2026.md]]
