# Meeting Summary — Transactional MVP1 sync
**Date:** September 29, 2026, 8:06 AM – 8:31 AM Eastern
**Duration:** About 25 minutes
**Segment:** 2 of 2
**Attendees:** Andrei Klimovich (organizer), Val Levitan, Irina Shishko, Ivan Shpak, Pavel Frolov, Dzmitry Chudzinau, Alexey Khamin, Alexander Biratko, Andrei Bosik
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026]]

Held in Russian. Segment 1 (small talk): [[Meeting_Notes_Transactional_MVP1_Pre_Meeting_Draniki_Chat-September-29-2026]].

## Summary

**New tilts and errors.** Andrei Klimovich has still not received the document with the new tilts and errors. He asked for it by email. Dzmitry said he is finishing this task and will send it.

**Autotests.** Irina said Vladimir started on autotests today. Alexey and Ivan continue writing tests. Irina is also setting up her own environment to write some tests.

**Ivan's setup instruction.** Ivan showed his document. It covers an already set up FlexPort and Flex IQ, the cables from PC to machine and FlexPort to machine, the SAS setup on the machine, the SAS emulator setup, and the Eclipse long-poll commands with what the machine should show for each. Ivan said the SAS checkbox on the machine must be set on the port where the FlexPort is connected, or the FlexPort will not work. Pavel explained the FlexPort SAS icon: red means nothing is connected, yellow means SAS commands are flowing, and blue means registration is done.

**What is still missing so Elizabeth can build the setup alone.** Ivan said two documents: how to flash the FlexPort, and how to install Flex IQ. Alexey noted that the diagram does not show required devices such as the printer and bill validator; they must be on site too. Pavel asked for real screenshots, not phone photos of the screen. Ivan said this is hard with two computers.

**Confluence.** Alexey suggested putting the instructions in Confluence. Andrei Klimovich recalled a plan to stop using Confluence. Val said to use Confluence freely for now. JVL will move away from it later, and all files will then be moved to a new place, so the team should not worry about it now.

**Flex IQ install instruction.** Dzmitry said no Flex IQ instruction exists yet. Yesterday he and Sergey checked that Elizabeth can see the Updates tab. The instruction needs screenshots of where to download the build, how to write it to an SD card, and what to press. He suggested also adding how to wipe the secrets on a terminal, in case it does not work at once. Andrei Klimovich said an older, detailed SD-card install instruction exists; he will find the link so it can be used as the base.

**Which build to install.** Dzmitry said always install the latest build from the list. A large release comes today, so tomorrow is the better day to install.

**Plan.** Andrei Klimovich restated it: prepare all instructions; Elizabeth builds the full setup in Georgia by these instructions; once it works, the team is ready to bring other makers' machines to the warehouse. Irina said the first check is Flex IQ and FlexPort on JVL's own machine. Alexey mentioned the FlexPort bootloader firmware from Alekseev; Pavel will ask Alekseev if it is ready. Irina asked about the SAS tool computer and cables. Andrei Klimovich said everything is already in Georgia, including a dedicated laptop for flashing. Ivan emailed the SAS tool zip to Elizabeth. Andrei Klimovich asked that it be stored where all JVL staff can reach it, with the link in the instruction. Ivan will try to attach it in Confluence.

**MVP2.** Alexander has nothing urgent. He will write emails as agreed.

**Test dates.** Pavel said the test tasks in the schedule show end dates of yesterday but are still in progress, and asked that the dates be corrected. Irina agreed.

**Router brand.** Andrei Bosik reported on home-class routers. Linksys (a Cisco sub-brand) does not start without internet. That leaves Netgear or MikroTik. Netgear is hard to buy in Belarus, so it cannot be tested there. MikroTik is registered in Latvia, but production is likely in China, and future sanctions are unclear. He suggested maybe just using the TP-Link routers used now. Val said JVL cannot use Chinese equipment, because it will be discontinued in America. Asked about MikroTik, Val said today everything is made in China. Andrei Bosik proposed MikroTik: it can be bought in Minsk, and he can test it and roll out a config. Price is about $40–$100. Val did not know the name, so Andrei Bosik posted it in the chat.

**Switch.** A router has only 3–4 ports, so a switch is also needed. Pavel said the same switch model should be in Minsk, because Dzmitry had a problem where devices did not see each other through a switch. Andrei Bosik said the switch brand matters less, but it should not be Chinese; he added that most probably are.

**Power over Ethernet (future idea).** Pavel raised powering the ports from a PoE switch, so they stay online when the machine is off. Andrei Bosik said the FlexPort hardware would need to support it; it does not today. Pavel raised it only for future capabilities.

**Brand decision.** Andrei Klimovich said Val must decide the router brand. Val said the team can decide this, and that he had already said it clearly. Andrei Klimovich then told Andrei Bosik to go ahead with MikroTik.

## Decisions Made

- **Use Confluence for the setup instructions for now** — JVL will move away from Confluence later and will migrate the files then. (Decided by Val Levitan)
- **Install the latest Flex IQ build from the list** — newer builds have more features and fixes; tomorrow is better because of today's large release. (Proposed by Dzmitry Chudzinau, accepted by Andrei Klimovich)
- **Go ahead with MikroTik routers** — Linksys needs internet to start, Netgear cannot be tested in Belarus, and Val said JVL cannot use Chinese equipment. (Val left the choice to the team; Andrei Klimovich and Andrei Bosik agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dzmitry Chudzinau | Email Andrei Klimovich the document of new tilts and errors | TBD | Normal | "In process, finishing this task" |
| 2 | Ivan Shpak | Put his setup instruction in Confluence and try to attach the SAS tool zip there | Sep 30, 2026 | High | Andrei: if all is ready tomorrow, Elizabeth can build the setup |
| 3 | Alexey Khamin | Update his older FlexPort flashing instruction to the current state, in the same style, in Confluence | Sep 30, 2026 | High | Irina asked; Alexey: "I'll do it in parallel" |
| 4 | Andrei Klimovich | Find and share the link to the old Flex IQ SD-card install instruction | TBD | Normal | Base for the new Flex IQ instruction |
| 5 | [Unassigned — needs clarification] | Update the Flex IQ install instruction in Confluence (Updates tab download, SD card, secrets wipe) | Sep 30, 2026 | High | Andrei: "someone will pick it up" |
| 6 | Pavel Frolov | Ask Alekseev if the FlexPort firmware (bootloader) is ready | TBD | Normal | |
| 7 | Andrei Klimovich | Send the instructions to Elizabeth so she can build the setup in Georgia | After items 2, 3, 5 | Normal | Then other makers' machines can come to the warehouse |
| 8 | [Unassigned — needs clarification] | Correct the end dates of the in-progress test tasks in the schedule | TBD | Low | Pavel asked; Irina agreed |
| 9 | Andrei Bosik | Proceed with MikroTik: pick a model and test it in Minsk | TBD | Normal | |

## Open Questions

- Which switch to use, and why some devices did not see each other through a switch in Dzmitry's test. (Pavel, Dzmitry)
- MikroTik is likely made in China; whether this conflicts with Val's "no Chinese equipment" rule was not settled beyond Val's remark that everything is made in China today. (Andrei Bosik)
- PoE for FlexPort — future only; needs hardware support. (Pavel)

## Dispatch Log

---
*Processed from Teams transcript on September 29, 2026 (meeting-watcher)*
*Source meeting: Transactional MVP1 sync, Segment 2 of 2*
