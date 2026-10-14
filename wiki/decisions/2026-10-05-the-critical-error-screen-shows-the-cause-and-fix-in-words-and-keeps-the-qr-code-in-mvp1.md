---
type: decision
title: In RIS improvement MVP1 the critical-error screen shows the real cause and the fix in words and keeps the QR code; the QR data goes to JVL's database, and real-time data for technicians is a later MVP
date: 2026-10-05
aliases: [critical error screen, we adding the description along the QR code, the QR code is for JVL, technician will not get anything by scanning, for class 3 we need it, Mvp 27, real cause of a critical error]
source-count: 3
status: active
open-commitments: 2
open-questions: 2
---

# The critical-error screen: cause and fix in words, plus the QR code (MVP1)

Settled by [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/pavel.md|Pavel Frolov]] at the [[wiki/meetings/2026-10-05-ris-mvp1-scope-and-peach-packaging.md|Oct-5 11:00 AM "RIS changes review"]], after questions from [[wiki/people/felipe-miranda.md|Felipe]]. Quotations from [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]].

## Felipe's question

The release summary said the QR code "also sends the error code, serial number, and software version to the technician and to Jvl." Felipe: "Who in Jvl will get that code?" Reading the "third capability": "today the screen only says critical error and the QR code gives a message with the spelling mistake. The technician arrives without knowing the cause or which parts to bring. After this release the screen. and the QR show the real cause and the fix." He named the kind of causes he wants shown: "Is it that is not reading the Dallas chip? Is it that the counter board is in?" — and, from the description, "a bad IO board".

## The answers

- **Pavel.** "it will be a QR code just to send this information to to our server to register this event on server side. Actually, we can assign any person within Jvl to get" it, but the messages say "not so much information about the reason. And so it can be used by our developers only." He expects the critical messages to be split into useful ones, "For example, Passport can't be read or data storage corruption". "nothing will change on server side".
- **Why the QR stays.** Val: "I was going to suggest that we need to depart from the concept of using QR code, but that's incorrect because for class 3 we need it. We're not going to have a Modem." Felipe: "And we're not going to have a Modem on all games in Georgia either."
- **The screen.** Val: "The screen. Will. Show it the real cause cause of the error. Yes. And the suggested fix." "it will have both the description of the error and the QR code".
- **Where the QR data goes.** Val: "right now, it's not assigned, so it arrives… to a database. The database is not real-time database… There is also very poor processing between raw data and the usable data. So that part has not been improved yet." "But we do receive the code."
- **What the technician gets.** Felipe: "The technician will not get anything from scanning the QR code." Val: "Right now, in the Mvp one, the technician will not get anything by scanning. But as we continuously improve the product, Our goal is to have the technician receive the data in the real-time."
- **The ruling.** Val: "Mvp one, we adding the description along the QR code. So we have a QR code and we have a description."
- **Fix the text, not the meeting.** Val: "If you do not understand something here, that means the description and the capability is not written correctly. That means we have to go back to the source and rewrite it". [[wiki/people/sebastian.md|Sebastian]] (who wrote the descriptions "with Pavel support"): "I will review it with review them and modify some things."

## How it sits against Sept 28 — evolution

On Sept 28 Val moved this capability ("Show the real cause of a critical error", capability 8) to MVP 2: "We, we don't need it right now" — [[wiki/decisions/2026-09-28-showing-the-real-cause-of-a-critical-error-moves-to-mvp2.md]]. On Oct 5 the capability is in the MVP1 release summary and Val rules on what MVP1 delivers. The newer ruling is current; the Sept-28 decision is marked superseded. No source says why it came back. *(Inference: the Oct-5 version is narrower — words on the screen plus the QR, with the real-time data for technicians left for later MVPs.)*

Pavel's Sept-28 doubt — "In most cases, we do not know beforehand… what was the reason of this crash" — is not answered on Oct 5. Felipe: "this capability won't work unless the machine is able to tell exactly what the problem is. I don't know how hard that is to do."

The derived notes match the transcript [[raw/Meeting_Notes_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]].

## Oct 6 2026 — plain words a technician understands; first check that the error still repeats

At the [[wiki/meetings/2026-10-06-daily-standup-ris-georgia-branch-and-critical-error-text.md|Oct-6 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]:

- **What the text says.** Pavel: find which errors cause a critical error and show them "на жёлтом экране" as text — the cause. "если у тебя эксепшен произошёл в модуле, который читает Даллас, ну значит написать что вот Даллас не могу прочитать там. Не просто джава ресепшн." Irina: "Техник должен понять, что написано." This matches the Oct-5 ruling.
- **First, does it still happen?** Pavel: "сначала надо, чтобы иван. Подтвердил, что это у нас повторяется, потому что может быть, это на какомто старом печь один только было такое поведение."
- **How to know all causes are covered.** Kharetski: "как я пойму, что клод действительно нашёл все места", and some places cannot be reproduced. Irina: what cannot be reproduced stays for the field. Pavel: one Claude does it, a second checks; handle the errors at a higher level. He left the method for when the task starts.

### Open commitments (Oct 6 2026)

- [ ] Ivan — confirm whether the critical error still repeats, before the error-text work — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]

### Open questions (Oct 6 2026)

- How will the team check that every source of a critical error is covered? Asked by Kharetski; left for when the task starts — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]

## Open commitments

- [ ] Sebastian Cortes, with Pavel Frolov — review and rewrite the capability descriptions, including the critical-error QR text (the technician gets nothing from scanning in MVP1) — due unspecified — [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]

## Open questions

- Who at JVL reads the critical-error QR data? Pavel: "Anybody, if you want"; Val: "right now, it's not assigned" — [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]

**§15.8:** clear.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]
- [[raw/Meeting_Notes_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]
