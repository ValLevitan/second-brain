# Meeting Summary — NOVA Game Change Regulatory Procedure

**Date:** September 11, 2026, 9:30 AM - 9:49 AM Eastern
**Duration:** approximately 19 minutes
**Attendees:** Val Levitan (organiser), Juan Martinez, Pavel Frolov, Irina Shishko. Sasha was absent — Pavel reported a family bereavement.
**Raw transcript:** [[Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026]]
**Source meeting:** NOVA remote game updates: certification and checksum — Microsoft Teams

## Summary

Juan was working down a list of regulatory questions about remote game updates. The meeting did not answer them — it established that JVL does not know the answers with confidence and decided to buy the answer from a test lab.

**Question one — the checksum as a single number.** Val's position was that they can ask the regulator to do it any other way, but he does not think it has to be one number. Juan took it away to investigate.

**Question two — the lawful procedure when an operator changes a game on a working machine.** This covers swapping, adding, enabling, disabling, or taking a bug fix, and the question is who has to be told. Juan split it in two.

Where all the games were submitted up front, nobody needs to be told. His Georgia example: JVL always submitted six games, and Elizabeth or Felipe could choose to enable only four of them, with the regulator knowing the other two sit in the background and can be enabled or disabled at any time. All six are approved, so no notification is required — possibly a reboot of the machine after reinstalling or disabling. Where Georgia goes from six games to the ten or fifteen now being contemplated, the regulator does have to be told, because they have to enable the game in their own system.

What the operator passes to the regulator needs verifying with Felipe. For South Dakota, Juan said they give Lonnie a bin file containing all the new game information so he can enter it into the host system, and there is always a new bin file when an entirely new package is submitted. For Georgia it is not clear: JVL has already introduced some of the freezing bug fixes and the regulator's system did not detect any change — which left Juan asking what the definition of a change actually is.

**The gap Pavel identified.** Pavel explained that the original assumption for Georgia was that they do not test particular game behaviour, only how SAS operates with the game, which is why JVL's bin file contains only the part of the data relating to SAS operation and does not relate directly to game sets. Juan initially thought Georgia used no bin file at all; Pavel corrected him — it is used, sent once during submission, and Ivan does it.

From that, Pavel drew the risk: if JVL releases a new game without changing anything relating to the local gaming server or data centre, the bin file does not change, and the Lottery would know nothing about the new game. He said that could be a problem. Juan agreed it is at the core of the regulatory issue, because any change affecting game outcome or RTP is supposed to require a more sensitive transaction. Submit the whole family of fifteen and never enable them, and JVL can enable at will; introduce a genuinely new game and that is different. Irina made the same point from the software side — everything is connected, and a game the Lottery did not know about cannot simply be added. Juan also asked whether the Georgia bin file is smaller than the South Dakota one, which holds more information; that was not answered.

**Val's direction — take it to the lab, and pay for it.** JVL has relationships with both test labs, but Val did not want to put the second one on the line at this stage. He would start with GLI, calling them the most savvy with the most resources to explain things, and said the other lab somewhat adheres to GLI's regulations anyway. Juan took it as his own action item, and Val asked to be invited to the call — his reasoning being that otherwise hours get burned and nothing comes out of it.

Val set two conditions. GLI must bring somebody who understands the subject, because this is not an administrative issue; if Juan preps them and asks for someone with deep knowledge, one meeting would probably iron it out. And GLI will ask for payment, because they do not consult for free — so it needs to be a productive session. Target is sometime next week. Juan will first draft a series of questions for the team to review so everyone is saying the same thing.

**Val's availability.** Tuesday to Thursday he is seeing clients and on the go. Monday is his travel day, so he can do up to late afternoon. Friday is his stationary day.

## Decisions Made

- **The checksum does not have to be a single number** — the regulator can be asked to do it another way. (Val Levitan)
- **Take the game-change regulatory question to GLI as a paid consultation**, rather than trying to resolve it internally. (Val Levitan)
- **Start with GLI and not the other lab at this stage** — GLI is the more capable of the two and the other broadly follows its regulations. (Val Levitan)
- **GLI must field somebody with deep subject knowledge, not an administrator**, and must be prepped in advance so one meeting settles it. (Val Levitan)
- **Val and the engineering side join the GLI call** rather than letting Juan take it alone. (Val Levitan)
- **Target the GLI session for next week.** (Val Levitan / Juan Martinez)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Juan Martinez | Investigate the checksum question — whether it must be a single number | TBD | Normal | Val does not believe it has to be |
| 2 | Juan Martinez | Set up and prep the GLI consultation, insisting on a deep-knowledge participant, and invite Val and the team | Week of September 14, 2026 | High | Paid engagement; Val's availability is Monday to late afternoon, and Friday |
| 3 | Juan Martinez | Draft the series of questions for the team to review before the GLI call | Before the GLI session | High | So everyone is saying the same thing |
| 4 | Juan Martinez | Verify with Felipe what the operator actually gives the regulator | TBD | Normal | Known for South Dakota (bin file to Lonnie), unclear for Georgia |

## Open Questions

- **What counts as a "change" in Georgia.** JVL introduced freezing bug fixes and the regulator's system detected nothing. This is the question the GLI session has to answer.
- **Whether the Lottery learns about a new game at all** when the release changes nothing in the local gaming server or data centre, so the bin file stays the same. Pavel raised this as a potential problem; Juan tied it to the rule that changes affecting game outcome or RTP require a more sensitive transaction.
- **Whether the Georgia bin file is smaller than the South Dakota one.** Juan asked; it was not answered in the meeting.

## Notes on the transcript

The recording mixes Russian and English and the Teams transcription is heavily degraded in the Russian passages; the English exchanges between Juan, Pavel and Val are clean and carry the substance. Two proper nouns in the raw file look like mis-transcriptions and are worth confirming with Val before they are treated as fact: the second test lab is rendered "Interlock" throughout (likely Intralot), and the South Dakota host system is rendered "Psy Games" (likely Sci Games). The raw transcript is preserved unchanged.
