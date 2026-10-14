# Meeting Summary — Games convert horizontal to vertical
**Date:** October 8, 2026, 10:02 AM – 10:35 AM Eastern
**Duration:** ~33 minutes
**Attendees:** Val Levitan, Igor Metelski, Pavel Frolov, Irina Shishko, Evgeny Kharetski
**Raw transcript:** [[Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026]]

## Summary

Held in Russian. Follow-up to the morning "Rage to Nova port review" ([[Meeting_Notes_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026]]). Igor showed the new try at a vertical Dragon Pays.

**What Igor did.** The production-approved horizontal version already had symbols about 20% wider than tall. Igor moved the same distortion to the vertical: symbols are now about 20% taller than wide (the earlier vertical try was 40%). He made a comp, converted the Rage scene to a Nova scene, and the game runs on it. Time: 1.5 hours, including 40 minutes to generate two videos (main game and free spins). Pavel: looks much better. Val: it worked. Pavel did not like the turtle symbol; Igor can make that one symbol square and fill the rest with alpha. The free space between logo and pay table is reserved for bonus descriptions (wild, scatter), as in new vertical games; those images are not rendered yet. The sky above was extended by simple extrapolation.

**Which games can convert.** Dakota games have new resources and an empty sky area, so they can go vertical. The NAD games (as transcribed) have old static toppers with no video, which is a problem. Val: ask Claude or ChatGPT to make a video from the static picture. Pavel: the video must loop (first frame equals last), about 10 seconds. The "Dragon Pays" title should be a separate video, not baked into the topper. Igor can also add a "liquid glass" reel frame; Pavel: start with plain video first.

**Scope.** Target is Nova, not Rage. Take the Texas games that are horizontal on Rage today and move them to vertical on Nova with Igor's method. Val: no change to math or functionality — a blind conversion. Igor: the port must start with the math. LGS has no mystery progressive support; Igor added it locally only, it is not production code, and LGS is not his project. Pavel: confirm with Efim how to build the container with the Texas math. Free-spin and bonus videos are also needed (Dutch Mill, Clover Fortune and others). Game selection screen is left for later (Daniil already did some work for Calle Ocho).

**Who does the work.** Pavel first proposed giving the video work to Anton Leskevich with Sergei Klemenchev. Val wanted Sergei Klemenchev to convert the Texas games with this method, with minimal help from Igor, and to measure time and process. Pavel: Klemenchev works no more than 2 hours a day, needs training, and should only prepare video. Pavel and Irina: Igor should port the first game, because he can fix game code; otherwise work bounces back and forth. Val agreed.

**Estimate.** Igor: about 2 weeks for one game with port plus tests, because hardware testing is not finished. If tests were ready, about a week. Val accepted that resources and tests take time but does not believe the work itself needs a week. Pavel: that is why we measure.

**Confidentiality.** Val: keep this inside the group so it does not spread in the company and scare anyone. No comments.

## Decisions Made

- **Igor's 20% vertical stretch is acceptable; conversion target is Nova vertical.** (Val Levitan, Pavel Frolov)
- **Texas games on Rage convert to Nova vertical with no change to math or functionality.** (Val Levitan)
- **Igor ports the first game himself; Sergei Klemenchev only prepares video.** First game is Dutch Mill. (Pavel Frolov, Irina Shishko; Val agreed)
- **The work stays confidential inside this group.** (Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Metelski | Prepare the technical task for Sergei Klemenchev (resources, sizes, steps) | Oct 9 | High | Sergei starts Friday |
| 2 | Igor Metelski | Send all needed resources or links, and a list of games with their bonuses and videos | TBD | Normal | For Klemenchev |
| 3 | Sergei Klemenchev | Make a looping video from a static topper (Dutch Mill first), about 10 seconds | Oct 12 | High | Not present; assigned in meeting |
| 4 | Pavel Frolov | Tell Val on Monday whether graphics arrived from Sergei | Oct 12 | Normal | Any Texas game |
| 5 | Pavel Frolov | Confirm with Efim how to build the container with the Texas math | TBD | Normal | Port starts with math |
| 6 | Igor Metelski | Finish the testing work, then report test status at the follow-up meeting | Oct 15 | High | Then start the Dutch Mill port |
| 7 | Igor Metelski | Port Dutch Mill to Nova vertical | Oct 19 | High | Val's target date |

## Open Questions

- How should LGS get mystery progressive support for Texas games, since Igor will not commit to that project? (Igor Metelski)
- How long does a game port really take once tests and resources are ready — one week or less? (Val Levitan, Igor Metelski)

## Dispatch Log

---
*Processed from Teams transcript on October 8, 2026*
*Source meeting: Games convert horizontal to vertical*
