---
type: decision
title: The "what counts as a game change" regulatory question goes to GLI as a paid consultation, with Val and the engineers on the call — GLI first, the other lab not yet
date: 2026-09-11
aliases: [take it to the lab and pay for it, start with GLI, they are the most savvy, GLI must bring somebody who understands the subject, they will ask for a payment, sometime next week, what is the definition of a change, the checksum does not have to be one number]
source-count: 2
status: active
open-commitments: 4
open-questions: 3
---

# The game-change question goes to GLI as a paid consultation

Ruled by [[wiki/people/val-levitan.md|Val]] at the [[wiki/meetings/2026-09-11-nova-game-change-regulatory-procedure.md|Sept 11 2026 9:30 AM call]]. [[wiki/people/juan-martinez.md|Juan Martinez]] was working down a numbered list of regulatory questions; the meeting established that JVL does not know the answers with confidence and decided to buy them.

**This is NOT a certification date and must not be read as one.** It is a paid advisory session about regulatory procedure. The RAGE-based **South Dakota VLT-2** submission to [[wiki/organizations/gli.md|GLI]] and the **NOVA** submission are separate matters; nothing in this source gives NOVA a GLI date, and none should be inferred from the "next week" target below.

## Question one — the checksum

Juan asked whether the checksum has to be a single number. Val: "**Ask them to do it any other way, but I don't think it has to be one number.**" Juan: "**I will, I will take that one up and investigate that.**" [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]

This closes the loop on the partial/component-checksum question raised at the Aug-11 NOVA architecture session, which was explicitly to be taken to Juan as the person who knows the topic best — see [[wiki/topics/nova-platform-architecture.md]].

## Question two — the lawful procedure when an operator changes a game on a working machine

Juan's framing: "**what is the lawful procedure when an operator changes a game on a working machine, swap, add, enable, disable, or take a bug fix?… Who has to be told**" — and he split it in two [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]:

- **Games submitted up front: nobody has to be told.** "**Previously, we always submitted six games, but [[wiki/people/elizabeth.md|Elizabeth]] or [[wiki/people/felipe-miranda.md|Felipe]] could have chosen to only enable four of the six, meaning the regulator would know that the other two games are in the background and that they could be enabled or disabled at any time by us… all six are approved, and in that scenario, we don't have to tell anybody**" — possibly a reboot after reinstalling or disabling.
- **Going from six games to ten or fifteen: they do have to be told.** "**If we are currently going from six games to the 10 or 15 that we're looking at now for Georgia, then yes… because they have to enable the game in their system.**"

**What the operator actually passes to the regulator is known for South Dakota and unclear for Georgia.** "**for South Dakota, we need to give Lonnie a bin file which contains all the new game information so he can enter it into the Psy Games host system**" and "**there's always going to be a new bin file when we submit an entirely new package**." For Georgia: "**it's not clear because we've already introduced some of the freezing bug fixes and their system did not detect any change. So, you know, what's the definition of a change?**" [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]] *("Psy Games" is the transcript's rendering of the South Dakota host-system vendor and is left as transcribed — the derived notes suggest Sci Games; not asserted here.)* [[raw/Meeting_Notes_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]

## The gap [[wiki/people/pavel.md|Pavel Frolov]] identified — and it is the substance of the meeting

Pavel explained the original Georgia assumption: "**For Georgia, they do not need to test a particular game behavior, just how SAS operates with the game. That's why our bin file contains only part of data center related to SAS operation. It… is not directly relates to game sets.**" Juan thought Georgia used no bin file at all — "**we don't use a bin file in Georgia, do we?**" — and Pavel corrected him: it is used, once, at submission, and "**During submission, [[wiki/people/ivan.md|Ivan]] is doing this**" [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]].

**From that, Pavel drew the risk:**

> "**if we are releasing a new game, but we do not change anything related to local gaming server or data center… hypothetically, adding a new game will not… change a bin file. And in this approach, Lottery will not know anything about new games. That could be a problem.**" [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]

Juan agreed that is the core of it: "**that's at the core of the regulatory issue… any change that affects game outcome or RTP is supposed to require a more sensitive transaction. So if we submit the entire family of 15 games, but never enable it, then yes, we can enable it at will. But if we introduce a completely new game…**" [[wiki/people/irina-shishko.md|Irina Shishko]] made the same point from the software side — everything is connected and a game the Lottery did not know about cannot simply be added: "[к]ак бы каждый софт с этим соединён[,] нельзя просто так добавить игру… вот её там не было, не знал лот[е]ри[я] об этом" [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]].

## The ruling

> **Val:** "**It's perplexing, but we have a relationship with [Interlock], so we can… put them on the line. I mean, we also have a relationship with [GLC], we can put them on the line.**" — then, asked whether he would or would not: "**Probably not immediately.**"
> **Val:** "**I would probably start with GLI. They're the most savvy and they have the most resources to explain things to us**" — and "**I think [Interlock] somewhat adheres to GLI's regulations.**" [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]

*(Two renderings, recorded as spoken. "**Interlock**" is the same garble the Sept-10 Georgia Lottery transcript produced for **Intralot** — see [[wiki/organizations/georgia-lottery-corporation.md]] — and the derived notes flag it as likely Intralot; it is **not** asserted as Intralot here. "**GLC**" appearing one line before "GLI" is most plausibly the same word transcribed twice; also not asserted. Both are queued for owner confirmation.)* [[raw/Meeting_Notes_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]

**Val attached three conditions:**

1. **He and the engineering side join the call**, not Juan alone: "**So, why you then invite us?**" and "**I think it will be productive. I mean, otherwise, which is going to be burning hours on it and nothing's going to come out.**" [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
2. **GLI must field someone with real subject knowledge, not an administrator:** "**GLI needs to bring somebody on the subject who understands it. It's not a, it's not an administrative issue**" and "**if you prep GLI for this, and if you ask them to bring somebody who possesses deep knowledge of the subject for the meeting, then in one meeting would probably iron it out.**" [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
3. **It will cost money, so it has to be productive:** "**And they will ask for a payment. They don't want to consult for free, so they'll ask for a payment. So let's make it a productive one.**" [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]

**Target: "Sometimes for next week"** — i.e. the week of September 14 2026 [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]].

**Val's availability, given in the same breath:** "**Tuesday to Thursday, I'm seeing clients and I'm on the go all the time. And Monday, Monday night is my travel day, so I can do up until late afternoon. And Friday is my stationary day.**" [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]

## Open commitments

- [ ] [[wiki/people/juan-martinez.md|Juan Martinez]] — investigate the checksum question (whether it must be a single number) — due unspecified — [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
- [ ] [[wiki/people/juan-martinez.md|Juan Martinez]] — set up and prep the GLI consultation, insisting on a deep-knowledge participant, and invite Val and the engineers — due week of Sept 14 2026 — [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
- [ ] [[wiki/people/juan-martinez.md|Juan Martinez]] — draft the series of questions for the team to review before the GLI call, "**just to make sure we're all saying the same thing**" — due before the GLI session — [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
- [ ] [[wiki/people/juan-martinez.md|Juan Martinez]] — verify with [[wiki/people/felipe-miranda.md|Felipe]] what the operator actually gives the regulator; known for South Dakota, unclear for Georgia — due unspecified — [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]

## Open questions

- **What counts as a "change" in Georgia?** JVL introduced some of the freezing bug fixes and the regulator's system detected nothing. This is the question the GLI session has to answer — [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
- **Does the Lottery learn about a new game at all**, when the release changes nothing in the local gaming server or data centre and the bin file therefore stays the same? Pavel raised it as a potential problem and nobody resolved it — [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
- **Is the Georgia bin file smaller than the South Dakota one?** Juan asked — "**is the bin file smaller for Georgia than it is for South Dakota because South Dakota contains more information?**" — and got no answer — [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]

**§15.8:** clear — regulatory procedure only. No fee figure was named.

## Sources
- [[raw/Meeting_Notes_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
- [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
