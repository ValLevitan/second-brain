---
type: organization
title: Dwolla
date: 2026-08-11
aliases: [Dwolla, Qualls, Diwala, Duwalla, the ACH provider, the third-party ACH rail, Marc Lee, Mark, Nancy Baccam, Nancy]
source-count: 2
open-commitments: 2
open-questions: 3
---

# Dwolla

Dwolla is the ACH payments provider JVL integrated for its location payments. As Dwolla described the flow on Aug 11 2026, it debits each location, the funds settle in a JVL Dwolla balance, and JVL then sweeps them to its own bank account. [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]] The engineering story — how JVL picked Dwolla and built the integration — lives on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Oct 8 2025 onward, with its own citations). This page holds the commercial relationship.

**Name note.** In the Aug-11 2026 recording the company's name is misheard as "Qualls" once ("the sales and partnerships team here at Qualls"); the same speakers say "Dwolla" plainly later on. "Qualls" is kept as an alias only. [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]

## People at Dwolla (no person pages)

- **Marc Lee** — sales and partnerships: "any like business strategy commercial stuff, I am your guy." The transcript spells him "Mark"; the spelling "Marc Lee" comes from the derived notes' calendar pairing. He first met Val on Aug 11 2026. [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]] [[raw/Meeting_Notes_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- **Nancy Baccam** — solutioning. Marc said she "has been mainly in contact with your tech teams" through onboarding and integration. Val called her "a great help and guiding guiding beacon for us." She is also on the [[wiki/meetings/2025-11-05-jvl-dwolla-onboarding-kickoff.md|Nov-5 2025 onboarding kickoff]]. [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- *(The Aug-11 transcript labels speakers only by number. "Speaker 2" is taken as Marc — he introduces himself as sales and says Nancy will ask the questions. "Speaker 3" is taken as Nancy — she asks the technical questions and names Nathan. This is an inference from context.)*

## Aug 11 2026 — Val asks Dwolla to cut the reserve

On the [[wiki/meetings/2026-08-11-dwolla-reserve-reduction-negotiation.md|Aug-11 call]] (8:15 PM ET, English, ~26 min) Val asked Dwolla to shrink the deposit in the order form. §15.8: clear — vendor and company economics only; no named-person pay. [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]

- **The number and the ask.** "I know that we negotiated the agreement with you for thirty six thousand dollars in deposit money, but our rollout at the time of negotiation was very aggressive." He asked Dwolla to "dramatically reduce the uh deposit." [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- **His reasons.** He had "shrunk it dramatically in terms of volume" because he is afraid of mistakes. He had also "moved a couple of additional people into the state of Georgia." JVL is private — "everything comes out from our own pocket." He argued Dwolla is not at risk at the lower volume. [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- **Not a fairness dispute.** "I am comfortable with thirty six thousand dollars. I just don't want to dish out thirty six thousand dollars. If I don't have to… I think it is fair." He promised to be the first to ask for higher limits if the business grows. [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- **The rollout he described.** One test unit in one location near the office "today", watched for about two weeks. Then five more units in September, ten more in October, a pause until January, and a planned rollout in the first quarter of 2027. "By the end of the year, it will be twenty terminals." The five September units would come from a list of "eighty companies that we do business with", after a trade show in Atlanta "at the end of this month" (Val's words). [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- **How long the testing runs.** "In the next four months, I will be in a extensive testing. And could it extend to six months? Yes." He will not go ahead unless the cycle is fully automated — "to automate things with banks with three different providers. It's not easy." He put automation at about "ninety five, ninety nine percent" and said "I am cycle focused. I am not terminal focused right now." [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- **Real money, not ten-dollar tests.** Dwolla asked if $10, or maybe $100, per transaction would do. Val said no. He must match [[wiki/organizations/incom.md|InComm]]'s $1,000-per-card limit because of competition at locations. He expects about $100 per card and five to ten cards a day, so up to about $1,000 a day per terminal, batched daily. [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- **Dwolla's current settings, as Nancy stated them.** For full production: $5,000 per transaction and a $25,000 weekly limit per terminal. Debits are "standard" — three days from the location into the JVL Dwolla balance — then one business day to JVL's bank. JVL is approved for same-day ACH credit. A further limit "is set at one hundred thousand right now" (the sentence follows the sweep from balance to bank; what exactly it caps is not clear in the transcript). Val: "we're far away from it." [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- **Dwolla's way to lower the risk.** Nancy suggested switching off same-day credit during the test period and lowering the client transaction limit. She added that standard debits from business payees carry little risk, because "they can't claim something as unauthorized". Val said same-day credit is "not important during the launch but it will be important in the future." [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- **Financials.** Marc asked for updated financials. Val said "We're at the same level" and he would only be "regurgitating the same financials." Marc read a figure of "on average around one hundred forty thousand" from what JVL had submitted (what the figure measures is not said). Nancy dated the old financials to August–October last year; Val thought it was "eight months or something." [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- **Order of steps (Val's condition, Dwolla agreed).** Nancy said the order form must change — new transaction limit and reserve — and go "I believe to Monica for her to sign", then production access. Val: "let's get agreement on a reserve. Prior to circulating anything else." Nancy: "We wouldn't update the order form until we actually get back to you on the reserve." See [[wiki/people/monica.md]]. [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]

*Notes vs transcript:* the derived notes call it the "signed order form". The transcript never says the order form was signed — only that the agreement was "negotiated" and that an updated form will go to Monica to sign. The notes also leave out the 20-terminal year-end figure, the $100,000 limit, the Atlanta trade show and 80-company list, and the extra staff in Georgia. The transcript is followed here. [[raw/Meeting_Notes_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]] [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]

*(Personal and family remarks from the call's small talk are not recorded, per §15.8.)*

## Open commitments

- [ ] Marc Lee (Dwolla) — take the reduced-reserve request to Dwolla's risk team and come back with a number — due Aug 12–13 2026 (Val: "tomorrow the day after"; Marc: "Yep") — [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- [ ] Nancy Baccam (Dwolla) — once the reserve is agreed, update the order form (transaction limit and reserve language) and send it for Monica's signature; production access follows — due after the reserve answer — [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]

## Open questions

- What reserve did Dwolla's risk team accept for the test period, against the $36,000 in the negotiated agreement? — [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- Were same-day ACH credit switched off and the client transaction limit lowered for the test period, as Nancy suggested? — [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- What does the "one hundred thousand" limit Nancy mentioned actually cap? The sentence is unclear in the transcript. — [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
- [[raw/Meeting_Notes_Dwolla_Reserve_Reduction_Negotiation-August-11-2026.md]]
