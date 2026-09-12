# Meeting Summary — Billy Liu / PlayPay: a bank-licensed Visa wallet, and Val's proposal to take half the company

**Date:** September 2, 2026, ~6:14 PM – 7:45 PM Eastern
**Duration:** ~1 hour 30 minutes
**Attendees:** Val Levitan, Billy Liu (Play Payments / PlayPay), Andrei Klimovich, one further JVL colleague
**Location:** JVL Georgia office
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar match:** none found on val@jvl.ca — filed on content alone

**Raw transcript:** [[Meeting_Transcript_Billy_Liu_PlayPay_Partnership_Deep_Dive-September-2-2026]]
**Related:** [[Meeting_Notes_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026]] — the same day, the other side of the redemption question

## Summary

A long, discursive meeting that ends with Val making a partnership proposal on the spot.

**Who Billy is.** PhD in theoretical physics; wrote code for a friend who built Nova Information Systems, the merchant-processing gateway that supplied First Union (later Wachovia, then Wells Fargo). His claim, offered as context for why Atlanta matters: the city processes about **70% of the world's card transactions**. Play Payments is ten years old and was a side project until, roughly two years ago, **the banking licence came through** — which he described as an epiphany that changed everything. He noted a licensing quirk that matters here: **if you hold a gaming licence you will not get a banking licence**; the Treasury checks, and traditionally the two are polar opposites. He was interviewed roughly ten times across the ten-year process. He also lobbied on the Georgia gift-card question fifteen years ago and donated to get the association going.

**What the product is.** **PlayPay** is the system, **PayApp** the app. The player registers with six pieces of information — first name, last name, an access code (can be the last four of the social), and a handle of at least eight characters. No passport, no social security number, no documents. That creates a wallet; the player then creates a **virtual Visa debit card**, reloadable, FDIC secured, up to $100,000, which can be added to Apple Pay or Google Pay and spent anywhere. Money can be pushed to a debit card, PayPal, Venmo, or back to a bank account. There is no physical card: Visa told them they will support the product but do not want to go backwards into plastic.

**The competitive position against InComm.** Billy competes by offering a **Visa wallet** where InComm offers a Mastercard prepaid card. EasyLink approached PlayPay to provide their digital solution and PlayPay built an API for them; at the point of redemption the player chooses a physical gift card or the PlayPay wallet.

**Fees, extracted by Val over several passes.** $2 per $1,000 load; up to $2,500 per person per day allowed under money-laundering rules, which is three loads at $6 total; $1,000 is "the Georgia thing"; they can allow $4,000 tranches. Pulling money back out to play — a "push" — costs **$2 per push**, so loading $10 back onto a machine costs the player $12. Val flagged this immediately as the weakness. Revenue on the back end comes from Visa interchange sharing, which Billy put at roughly **half a percent**.

**Val's economics, and the proposal.** Val had the number ready from his InComm meeting: InComm also shares half a percent with him. He then scaled it — Georgia Lottery processed **$5 billion in payouts** last year; capture 20% of that and you are moving $1 billion; at the share he was describing that is **$150 million a year**. Billy said he doubted he would be that successful. Val's response was to propose a deal outright: *"You want me to write a contract? Why don't you sleep on it? If you like it, let's meet next week. I get fifty percent of your company. I'm driving you right into the market."* Billy's reply — "And you know what? No one was there when I was driving it myself" — was not a no. Val proposed a celebration dinner next week to sign.

**What Val brings, and his strategic argument.** He offered to **give the hardware away**: a new machine at $16,000 including one unit inside it plus five more Flex ports plus Flex-IQ, connected over SAS 2. His argument for why speed matters: *"There is no magic in this solution. The magic is in speed."* Tomorrow everyone will have the same thing. He must be able to walk into a location and answer yes to every capability question at zero cost, or it does not happen.

**The substantive disagreement — cash.** Val wants the redemption terminal to offer cash, charging perhaps $5 and passing the fee to the location, because that is what players actually come for and because it stops locations creating a black market by buying $500 cards off players for $490. Billy's position is that his two-step process already achieves this lawfully — GLC's rule is that you may not simply hand cash over, and as long as there are two steps you are not breaking the law. Val's deeper point is that the **front fees should go to the store owner** to disincentivise the grey market; Billy noted InComm shares with the master licence holders, not the stores. Val's own framing: *"I should be doing the backend. This is where my money is."*

Billy also raised a patent he holds on **NFC "tap to fund"**, and floated marrying it with JVL's ports. He confirmed InComm is averaging **1.5 cards per day** per location — the same figure Val used against InComm the same day — and called their behaviour difficult, saying they wanted to partner and he expected to be "kicked to the curb."

Val demonstrated JVL's flow in return: no bill acceptor, no printer; the player gets a ticket at the kiosk, walks the machines, cashes out to an electronic wallet, moves on, and redeems at the end — noting frankly that cash redemption at that final step *"is illegal right now"*, which is precisely where Billy's app becomes the legal path.

## Decisions Made

- **Val proposed a formal partnership for 50% of Play Payments**, with JVL driving distribution; Billy to sleep on it and meet next week. Not accepted, not refused.
- **JVL would give away the transactional hardware** — machine at $16,000 including one internal unit, five Flex ports and Flex-IQ — to win the installed base.
- **Front-end fees should go to the location**, per Val, to remove the incentive for a grey cash market. Not agreed by Billy.
- **Celebration dinner proposed for next week** to sign an agreement.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Billy | Sleep on Val's 50% partnership proposal and respond | Next week | Critical | "Why don't you sleep on it? If you like it, let's meet next week" |
| 2 | Val | Meet Billy again next week (Val back Tuesday); prepare the contract | Next week | Critical | Val proposed writing it |
| 3 | Val / Andrei | Model the economics properly — Val's $150M figure was asserted, not calculated with Billy | Before signing | High | Billy could not answer what he makes on $1B transacted |
| 4 | Billy | Confirm the actual revenue share on volume (Visa tiers) | Before signing | High | "I don't know the exact answer because there are tiers" |
| 5 | Val / Billy | Work out whether Billy's NFC tap-to-fund patent marries to JVL Flex ports | Open | Medium | Billy raised the patent unprompted |
| 6 | Val | Resolve the exclusivity question Billy raised — no InComm, no physical card dispensing | Before signing | High | Val's answer was "I don't know. This is a big ask. Maybe even impossible" |

## Key facts worth keeping

- **PlayPay holds a banking licence** (~2 years old, ten-year process). A gaming licence disqualifies you from getting one — a structural moat.
- Product: virtual reloadable **Visa** debit, FDIC secured to $100,000, Apple/Google Pay compatible; **no physical card** (Visa's choice).
- Registration: six fields, no ID documents.
- Fees: $2 per $1,000 load; $2 per push out; $2,500/person/day cap; ~0.5% back-end share.
- **EasyLink already uses PlayPay's API** for its digital redemption option.
- InComm averaging **1.5 cards per day** per location — corroborated independently by Billy and by Val's InComm meeting the same day.
- Georgia Lottery payouts last year: **~$5 billion**.
- Billy holds a patent on NFC tap-to-fund.

## Flagged for Val

The exclusivity Billy asked for — no InComm, no physical card dispensing from JVL kiosks — is in direct tension with the position Val took with InComm on the same day, and with the multiple-clearinghouse capability already specified for Flex-IQ ([[Meeting_Notes_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026]]). Worth settling before any contract.
