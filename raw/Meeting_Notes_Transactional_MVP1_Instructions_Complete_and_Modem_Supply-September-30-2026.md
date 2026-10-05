# Meeting Summary — Transactional MVP1 sync
**Date:** September 30, 2026, 8:03 AM – 8:24 AM Eastern
**Duration:** About 21 minutes
**Attendees:** Andrei Klimovich (organizer), Pavel Frolov, Irina Shishko, Dzmitry Chudzinau, Alexey Khamin, Ivan Shpak, Andrei Bosik, Alexander Biratko
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026]]

Held in Russian. Previous sync: [[Meeting_Notes_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026]].

## Summary

**FlexPort instruction in Confluence.** Alexey added the updated FlexPort instruction today. It sits inside the FlexPay technical space. Alexey said the FlexPort folder should be at the same level as FlexPay and Flex IQ, because it is a separate product. Andrei Klimovich agreed and will move it one level up. The folder was lost for a moment during the move, then found.

**Old firmware document.** Next to it is an older document, last revised January 2025. Andrei Klimovich thought it was out of date. Pavel said it describes the remote (not wired) firmware update protocol. Dzmitry said to leave it for now and sort it out at the next revision.

**Ivan's instruction images.** Pictures in Ivan's instruction showed "preview unavailable" for Andrei and Alexey. By the end of the meeting Ivan had restored them. Pictures break when added inside the page body, so he attached an archive as a separate comment at the bottom of the page.

**Flex IQ install instruction.** Andrei Klimovich posted the link to the old SD-card install instruction. It was in Confluence, not in Git as he thought yesterday. Dzmitry has taken it on. He will reuse some of Andrei's terminal pictures, explain where each part comes from, and send the link. He expects to finish today.

**Elizabeth can start tomorrow.** With all three instructions ready, Andrei Klimovich said Elizabeth can start the test setup in Georgia tomorrow. He proposed a Teams chat for her questions, with people who know FlexPort, Flex IQ and the game machine. Pavel named Alexey, himself, Dzmitry and Irina. Andrei Bosik suggested one contact person only. Irina disagreed: she already handles Elizabeth's questions and then looks for answers, and Elizabeth often writes in the evening when not everyone is available. A group chat lets whoever knows answer faster. Andrei Klimovich agreed on a shared chat.

**Autotests.** Irina said testing is going well. Everyone is writing tests, tests pass, and many receipts were printed. Pavel joked that printers should be taken away in favour of emulators. Irina said emulators are not convenient. The team shares one Flex IQ and people wait for it.

**Test devices.** Pavel said another Flex IQ could be built as bare boards on a table; that is enough for tests. The team talked about 3D-printing a FlexPay case. Pavel said the screen is bigger than the printer's bed. Alexander and Andrei Bosik said parts can be printed and glued. But the team has only one TV with the right resolution, so Alexander said there is no point for now. Pavel said there are 4 boards: 2 in Flex IQs, 1 in a FlexPay, and 1 unused. Alexander's board has one burned USB port. A couple more boards arrive soon, which should cover all test devices.

**Recycler.** The bill recycler chosen for the project has shipped to Minsk and should arrive in about two weeks. Alexander and Pavel said this belongs to the Flex Recycler project, probably MVP3.

**MVP2 scope.** Andrei Klimovich said that when he returns, MVP2 will focus on FlexPay in the slim form factor, with current screens and flow. Pavel said MVP2 only adds FlexPay, plus Wi-Fi connect. Support for two devices at one location is likely MVP3.

**Spare parts.** Andrei Klimovich will start an email to Genadiy and Val to update the set of parts in Minsk, so the team has what it needs. He will add Pavel, and Pavel asked to add Irina too. Pavel said a second FlexPay device would need another monitor like the one they bought. Alexander suggested ordering at least one original panel. Andrei asked to discuss this in the email.

**GSM modems.** Alexander asked which modem model will be used, and whether one or two. Andrei Bosik said Pavel told him Quectel, and he is writing code for that model, since modems show up differently in the operating system (USB, WLAN and others). Pavel said Genadiy is working with suppliers, including Sierra Wireless. Some have only 5 or 10 units; others want orders of 1,000. The models used so far are end of life, so new models are likely. Alexander said new modems must be tested; Pavel said this applies to game machines and transactional devices. Andrei Klimovich recalled Georgia had only 10 modems, enough for 10 game machines and 10 transactional devices. Pavel said Val ordered about 30 more of the same model, and they are being bought now. In parallel, work continues toward current models.

**Flex IQ sound.** Pavel said Dzmitry found a missed capability: sound feedback on Flex IQ. The Flex IQ has speakers inside. Andrei Bosik asked why sound is needed, since ATMs do not beep much. Andrei Klimovich said it will not be added to MVP1; he will put it in MVP2. He added that MVP2 must also define the LED "language" for FlexPay slim: which colors, and the logic behind them. Pavel said Alexander already has sounds working on FlexPay.

## Decisions Made

- **Move the FlexPort instruction folder up to the same level as FlexPay and Flex IQ** — it is a separate product. (Proposed by Alexey Khamin, agreed by Andrei Klimovich)
- **Elizabeth's questions go to a shared Teams group chat, not to one person** — she often writes in the evening, and whoever knows can answer. (Irina Shishko; agreed by Andrei Klimovich. Andrei Bosik's single-contact idea was not adopted.)
- **Flex IQ sound feedback goes to MVP2, not MVP1.** (Andrei Klimovich)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Move the FlexPort folder one level up in Confluence and post in the team chat where it now is | Sep 30, 2026 | Normal | |
| 2 | Dzmitry Chudzinau | Finish the Flex IQ SD-card install instruction and send the link | Sep 30, 2026 | High | Last of the three instructions Elizabeth needs |
| 3 | Andrei Klimovich | Create the Teams group chat for Elizabeth's Georgia setup questions (Alexey, Pavel, Dzmitry, Irina) | Before Elizabeth starts (Oct 1) | High | He said "I'll do it" right after the chat was agreed; the transcript does not name the chat in that sentence |
| 4 | Elizabeth Palomino | Start the test setup in Georgia using the three instructions | From Oct 1, 2026 | Normal | Not present; stated by Andrei Klimovich |
| 5 | Andrei Klimovich | Add Flex IQ sound feedback and the FlexPay slim LED color logic to MVP2 scope | TBD | Normal | "Okay, noted" |
| 6 | Andrei Klimovich | Start an email to Genadiy and Val to update the spare parts set in Minsk; include Pavel and Irina | TBD | Normal | Covers a second monitor or an original panel for FlexPay |

## Open Questions

- Which modem model will be used going forward, and one or two per device. Genadiy is still working with suppliers. (Alexander Biratko)
- Second monitor like the current one, or an original panel, for a second FlexPay test device. Moved to the parts email. (Pavel Frolov, Alexander Biratko)
- Where the old remote-firmware protocol document belongs. Left for the next revision. (Dzmitry Chudzinau)

## Dispatch Log

---
*Processed from Teams transcript on September 30, 2026 (meeting-watcher)*
*Source meeting: Transactional MVP1 sync*
