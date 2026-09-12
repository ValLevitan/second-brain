# Meeting Summary — Alignment on Production schedule for Flex-Slim Ports and IQ (Flex Slim First Ten Build and FlexPort SAS)
**Date:** September 4, 2026, 12:29 PM – 1:49 PM Eastern
**Duration:** ~80 minutes
**Attendees:** Val Levitan, Genadi Peari, Evgeniy Alekseev, Eugine Yavorsky, Elizabeth Palomino (joined briefly), Pavel Frolov (joined from his car)

**Raw transcript:** [[Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026]]

## Summary

Mostly in Russian. The call covers three things: getting the first ten Flex-Slim units built, the commercial offer Val is building around them, and getting the SAS protocol working on Flex-Port.

**Building the first ten Flex-Slim units.** Val opened by restating the target for the transcript: the first ten Flex-Slim units with card dispenser, front-load bill acceptor, printer and the optical parts. He had been told four weeks and wanted a faster path. Genadi Peari walked through what physically exists. Eight units are somewhere in the ocean in transit; they were supposed to ship in mid-July and he is trying to establish where they are. New plastics have already arrived in Georgia, twenty pieces. That produced the first friction of the call: the plastics arrived and are not in the system, and Genadi said that apart from him nobody currently knows they are there. Val said he understands that problem, knows how to fix it, and that it cannot be fixed instantly.

On card dispensers, Genadi confirmed JVL bought ten of one type, then found a cheaper and better one, and Pavel had confirmed both versions are supported in software. Four are already installed in Flex-Pay units, and there should be roughly six more in stock, which is about enough for ten machines at around $380 each. Genadi was reworking brackets so the dispenser can be pulled out from the back to load cards, and expected to release drawings for three brackets that day or the next. Val was openly sceptical that it would happen that day.

For manufacturing the brackets, Genadi raised making them in China through Michael, roughly a week to make plus air freight, so about two weeks in the best case. Val was clear: China is fine, but push them, because their standard lead times are not acceptable and they will accommodate a rush if asked directly. He rejected the local alternative outright.

Val also gave Genadi a direct instruction about working with Elizabeth Palomino: do not write to her, because a written message means she looks at it in an hour, thinks about it in two, and starts it in three. Call her on Teams, tell her to go and check, have her point the camera at it and show him while he waits. Genadi then did exactly that, bringing Elizabeth on to find the dispensers physically in stock, matching the item already installed in the Flex-Pay units.

On metal, Val instructed that once the brackets are finalised the order should be placed for a hundred units, since the metal is not expensive. He pushed back on ordering thicker metal, saying 14 gauge is already sufficient. Genadi confirmed monitors (twelve in stock), the interface board for printer and card dispenser, and set wires are all covered; the RK3568 is the standard board on Slim.

**The commercial offer.** Val explained the reasoning behind the urgency, and asked Genadi to write the numbers down. Georgia has about 47,000 machines across roughly 7,400 locations, which is about 5.9 machines per location. Only about 20 percent of locations have any kind of card system, and the other 80 percent were given free PAX terminals that work badly. Off the back of the show, where JVL launched and tested the 15-game machine, Val raised the machine price from $13,500 to about $15,750. The offer he is building: buy one machine, and JVL gives one Flex-Slim, one Flex-IQ and five more Flex-Ports free. At retail those are $795 per port, $895 for the IQ, and $7,950 for the Flex-Slim, which totals $12,820 of product against a $2,930 increase in what the operator pays. Against an Aristocrat machine at around $20,000, the operator buys JVL at about $16,000 and gets everything free. There is a subscription of about $90 a month on top. Val's stated intent is to take the market with this offer, and that is why he is pushing so hard on tooling: build samples, and if the samples work, move straight to tooling.

**SAS on Flex-Port.** Genadi raised that Pavel had questioned whether Flex-Port is even needed, suggesting a version without a screen. Val rejected that: the screens are needed and there is no time to redesign, because he expects demand to be very high given everything is being given away free.

Evgeniy Alekseev joined and clarified the actual state. The SAS protocol is implemented on SMIB, not on Flex-Port. The software module exists on SMIB and is agreed with the Wave protocol side; it needs to be carried across to Flex-Port. He estimated a couple of days rather than half an hour, and said Eugine Yavorsky is needed. Eugine joined and explained that a demo version was built on Flex-Port hardware for the trade show with minimal functionality, and that some fixes were made after the show, but nothing has been started on the newer boards. Evgeniy's view was that the right move is not to polish the demo but to take that SAS work and merge it into the main branch.

Val laid out the sequence explicitly: restore the working environment; find the document Dzmitry Chudzinau published, most likely in Confluence, describing the commands he wants supported over SAS; test that the environment works; test those commands; restore any that do not work; and only at the very end ask what is missing, treating anything genuinely new as fresh development to be estimated. Evgeniy said he could start over the weekend, inserting and connecting things and possibly checking some of it. Eugine is away at a cottage for the long weekend and returns Monday evening, so he starts Monday evening. Val also pushed back on the idea of the weekend being protected, saying holidays and weekends were cancelled, framed as an order from above. Evgeniy raised that a Jira ticket needs creating for this and Val agreed.

On duration, Eugine estimated two weeks, possibly three, possibly a month, and asked for Pavel to narrow the scope of which SAS commands to start from since the full protocol would take a year. Evgeniy's counter was that the scope already exists in Dzmitry's document and the correct action is to have it extended if it is insufficient. After the others left, Genadi told Val privately that Yavorsky's two weeks means at least two months, that he drags, and that nothing will work without Pavel.

Pavel then joined from his car with about half an hour before he got home. The audio quality of this stretch is very poor and the transcript is largely unusable, but the substance that survives is Pavel's proposal for a second stage: debug hooks, logging of data packets, and a proper development environment, because without those you can spend a very long time fixing errors blind. He described what he had already built for himself: an emulator of the gaming machine that does not reproduce it fully but covers most of the workflow much faster than real hardware, plus a full debug console with commands and logs, on an STM32 743. Val asked whether this was like the environment Aaron built for the RK3568; Pavel corrected him, saying Aaron only assembled a set of scripts to build the modules and root filesystem, and that for STM the vendor already supplies libraries. What is missing is the surrounding environment: a Flex-Pay connected, a machine on the network, one or several Flex-Ports connected, an ST-Link debugger, and a description of what is connected where and where each unit's code lives, so Claude can find things and say what needs correcting. Pavel said he had already done most of this and had shown it to Khamin that day, and Khamin can take it for his own testing.

Val asked how to write this up as capabilities and repositories. Pavel's answer was that Dzmitry's document described the flow rather than his own, so the scheme needs to be talked through out loud on Monday with the interested people, and then Claude can propose the capabilities. His rough guess: one capability to make Flex-Port work in SAS mode for transactions, a second for the existing use on Flex-Port, and a supporting one for the debug environment (console and emulator), which could alternatively be features inside the other capabilities.

Val closed by scheduling: engineers meet Monday at 7:00, before the 8:00 meeting Andrei Klimovich had already planned on Flex-Port development. Val said he would send the invitation.

## Decisions Made

- **Brackets and harnesses are the critical path for the first ten Flex-Slim units, and they are to be made in China through Michael with a rush request.** The local alternative was rejected outright. (Val)
- **Once brackets are finalised, place the metal order for 100 units.** Metal is cheap and the lead time is long. (Val)
- **Stay at 14 gauge; do not order thicker metal.** (Val, against Genadi's report that thicker had been suggested)
- **Flex-Port keeps its screen. The no-screen variant Pavel floated is rejected** — no time to redesign, and demand is expected to be high. (Val)
- **SAS support is ported from SMIB to Flex-Port, not rebuilt.** The existing trade-show SAS work is merged into the main branch rather than polished in place. (Evgeniy Alekseev, accepted by Val)
- **Scope for SAS commands comes from Dzmitry Chudzinau's existing document.** If it is insufficient it gets extended; it is not renegotiated from scratch. (Evgeniy Alekseev's position, adopted over Eugine Yavorsky's request to narrow scope)
- **Sequence agreed: restore environment, find Dzmitry's document, verify the environment works, test the listed commands, restore any that fail, and only then ask what is missing.** Anything genuinely new is treated as fresh development requiring an estimate. (Val)
- **Evgeniy Alekseev starts over the weekend; Eugine Yavorsky starts Monday evening on his return.** (Val, agreed by both)
- **A Jira ticket is created for the SAS-on-Flex-Port work.** (Evgeniy Alekseev raised it, Val agreed)
- **Engineers meet Monday at 7:00, ahead of Andrei Klimovich's 8:00 Flex-Port meeting.** Val sends the invitation. (Val)
- **Commercial offer confirmed as the reason for the schedule pressure:** machine price raised to about $15,750, bundled with one Flex-Slim, one Flex-IQ and five Flex-Ports free, about $12,820 of retail product against a $2,930 increase, plus about $90 a month subscription. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Release the drawings for the three brackets | Same day or next | Critical | Val was sceptical it would be same-day; it gates everything else |
| 2 | Genadi Peari | Get the brackets and two or three harnesses made in China through Michael, with a rush request, and delivered within a week | About one week | Critical | Val: push them, they will accommodate a rush if asked |
| 3 | Genadi Peari | Place the metal order for 100 units once brackets are finalised | After brackets | High | Metal is inexpensive; long lead time is the risk |
| 4 | Elizabeth Palomino | Physically locate the card dispensers in stock, matching the item installed in the Flex-Pay units | Immediately | High | Genadi called her on Teams during the meeting rather than writing |
| 5 | Elizabeth Palomino | Enter the twenty received plastics into the system | Not fixed | High | They arrived and are not in the system; only Genadi knows they are there |
| 6 | Evgeniy Alekseev | Merge the trade-show SAS work into the main branch and restore the working environment, over the weekend | Weekend | High | He estimated a couple of days, not half an hour |
| 7 | Eugine Yavorsky | Rebuild his working environment and take up the SAS port on Flex-Port | From Monday evening | High | Away at a cottage over the long weekend |
| 8 | Evgeniy Alekseev | Create the Jira ticket for the SAS-on-Flex-Port work | Not fixed | Normal | He raised it, Val agreed it is required |
| 9 | Pavel Frolov | Think over the capability breakdown across the weekend and bring it to Monday | Monday | High | Rough shape: SAS transactions on Flex-Port, existing Flex-Port use, debug environment |
| 10 | Val Levitan | Send the invitation for the Monday 7:00 engineers' meeting | Before Monday | High | Sits ahead of Andrei Klimovich's 8:00 Flex-Port meeting |
| 11 | Genadi Peari | Establish where the eight in-transit units are and when they land | Ongoing | Normal | Shipped around mid-July, still at sea |

## Open Questions

- How long the SAS port actually takes. Eugine Yavorsky said two weeks, possibly three or a month. Genadi told Val privately afterwards that two weeks from Yavorsky means at least two months and that it will not happen without Pavel.
- Whether Dzmitry Chudzinau's command list is sufficient, which is only answerable after the environment is restored and the listed commands are tested.
- Where exactly Dzmitry's document lives. Believed to be in Confluence, not confirmed in the call.

## Note

A stretch of this recording (roughly 00:52 to 01:03) is Pavel Frolov speaking from his car and the transcription is badly degraded, with many words rendered as nonsense. The substance recorded above from that stretch is what could be read reliably; anything finer should be taken from the audio rather than the transcript.
