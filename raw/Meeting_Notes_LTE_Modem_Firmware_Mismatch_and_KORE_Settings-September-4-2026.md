# Meeting Summary — Modem integration September 4-2026 (LTE Modem Firmware Mismatch and KORE Settings)
**Date:** September 4, 2026, 12:10 PM – 12:29 PM Eastern
**Duration:** ~19 minutes
**Attendees:** Val Levitan, Pavel Frolov, Genadi Peari

**Raw transcript:** [[Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026]]

## Summary

A short call about the LTE modem that will not hold a connection in Georgia. The conversation runs in Russian and splits into two halves: a technical diagnosis, and Val's push on ownership.

Pavel Frolov reported the position plainly. The modem that was installed, a 7455, does not work, and the reason is not fully clear. His candidate causes: incompatibility with the carrier, a modem built for a different market, or firmware that is too old. He and Elizabeth Palomino ran two days of experiments in Georgia and could not configure it to hold a stable link. Val pressed on why it had passed testing before, and Pavel drew the distinction that matters: it was tested in Minsk, on the same model number, and it worked there. Too many input variables differ between the two places — different carrier, different firmware version, a modem intended for a different market.

Genadi Peari then named the actual mistake, and he named it as a strategic one rather than a technical one. Pavel had ordered his 7455 from AliExpress and received it in Minsk. Georgia received a 7455 too, but from a different source. Same model, different firmware. Genadi called that mistake number one. Pavel did not accept the framing and pushed back, asking where the mistake was, and said the Minsk test had been done two weeks earlier.

Val's response is the part of this call worth keeping. He told Pavel he understood how it looked from Pavel's side: a professional who tested his part, got a working result, and believes he is right. Val's argument is that the concept itself is wrong. "We tested it, it worked, and now it does not work" is not an acceptable explanation from someone at Pavel's level. If Pavel were twenty-five and new, Val said he would treat it as normal, but Pavel has been at JVL a long time and understands the nuances. Val had raised the modem question long before, and Pavel had enough time to design a correct test strategy: which modem to test, on what, and where. Val said he should not have to micromanage that for a person in Pavel's position, and that the right move would have been either to test in Georgia from the start, or to say up front that testing in Minsk was probably the wrong test. Pavel answered that this was exactly what had been done. Val's reply was that it should have been done much earlier.

Val then said he could not prove from memory when he first asked for the modem work, and undertook to go back and check his own messages rather than assert it without evidence. He closed the accountability part by saying he wants the team to treat their responsibilities preventively and to say in advance what might not work. Pavel said honestly that he was upset by the suggestion that they ignore this point. Val answered that his read is not that they ignore it, but that they do not take responsibility for decisions that turn out wrong, and suggested Pavel think it over across the weekend. Pavel said he had heard him and was more upset than before.

The technical plan for the remaining minutes: Genadi reported they have received two types of modem, five of each, and a second version is going in now for Pavel to look at. He also found the same modem in a North America variant on Amazon at about $16, where the firmware is likely to be the correct one, and thought the whole thing could be finished in about two days. Val confirmed there is time, because the graphics and related pieces are not ready yet either.

Val then asked the question that shaped the actions: which SIM cards go in, and can modems be bought from KORE directly. Pavel explained that modems sold openly through Amazon are usually pulled from some other market, for example a batch made for Dell laptops, and their firmware may carry support for certain carriers while ignoring others. Val's conclusion was to go to KORE and ask which modems they recommend. Pavel added a second question for KORE that could solve it outright: ask them for the modem configuration parameters, specifically the APN. If KORE supplies it and JVL hard-codes it, the existing modems may simply start working.

Val summarised the plan back to the group and Pavel confirmed it: email KORE, buy the other modems, ship them to Georgia, Elizabeth installs them, Pavel uploads software remotely and verifies. Pavel said he hopes a proper modem will work immediately on the existing software; if not he will connect remotely and find the cause.

The call ended on antennas. Pavel noted one earlier cause of the connection failure was insufficient signal level from the antenna. Two antennas are now connected to the module. Genadi suspects that an antenna glued onto a metal enclosure shields badly, and that it may need to sit further outside the enclosure. He would rather place it into an opening than stick it flat on the body, because the signal is being lost.

## Decisions Made

- **The installed 7455 modem is treated as not working in Georgia, and the cause is accepted as a source and firmware mismatch rather than a design fault.** Minsk and Georgia bought the same model number from different sources, with different firmware, for different markets. (Genadi Peari's diagnosis, accepted by Val; Pavel Frolov did not accept the "mistake" framing)
- **Buy the North America variant of the same modem from Amazon (about $16) and test that.** Firmware for the North American market is expected to be correct. (Val and Genadi)
- **Ask KORE which modems they recommend, rather than continuing to guess.** (Val)
- **Also ask KORE for the modem configuration parameters, in particular the APN.** If the parameters are supplied and hard-coded, the modems already in hand may work. (Pavel Frolov's proposal, accepted by Val)
- **Antennas are to be moved out of the metal enclosure rather than glued to it.** Two antennas are now fitted to the module. (Genadi Peari)
- **Val will verify from his own message history when he first asked for the modem work** rather than assert the timing from memory. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Email KORE: which modems do they recommend, and what are the configuration parameters and APN | Right after this call | High | Val: "let's ask KORE which modems they recommend"; Pavel added the APN question |
| 2 | Genadi Peari | Order the North America variant modems from Amazon and ship them to Georgia | Within about two days | High | Correct firmware for the market is the leading theory |
| 3 | Elizabeth Palomino | Install the replacement modems when they arrive in Georgia | On arrival | High | Genadi already has five of each of two types going in |
| 4 | Pavel Frolov | Upload software remotely to the new modems and verify they hold a connection | After installation | High | If a good modem does not work immediately, Pavel connects remotely to find the cause |
| 5 | Genadi Peari | Rework antenna placement so the antenna sits in an opening rather than glued to the metal enclosure | Not fixed | Normal | Suspected shielding loss; two antennas now fitted |
| 6 | Val Levitan | Check his own message history for when he first asked for the modem work | Same day | Normal | Val declined to argue the timing without evidence |

## Open Questions

- Whether the second modem version now going in behaves any better than the first, which is what Pavel will look at.
- Whether KORE will supply modem recommendations and the APN, which would decide between buying new hardware and reconfiguring what is already in the field.

## Note

The second half of this call is an accountability exchange between Val and Pavel Frolov rather than a technical discussion, and it ends unresolved: Pavel said he was upset, Val said he had no wish to upset him and suggested he think it over across the weekend. In the meeting that immediately follows ([[Meeting_Notes_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026]]) Val told Genadi he thought Pavel had been shocked by the comment and had gone home upset, and decided to leave him alone until Monday.
