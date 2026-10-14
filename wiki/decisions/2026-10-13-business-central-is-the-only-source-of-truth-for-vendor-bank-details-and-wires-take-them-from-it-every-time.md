---
type: decision
title: Business Central is the only source of truth for vendor bank details — every wire takes them from Business Central, with no bank-side templates and no manual entry
date: 2026-10-13
aliases: [Business Central drives the template, no templates in Bank of America, vendor bank data source of truth, laborious and unacceptable, wires from Business Central, CSV wire upload, advanced platform]
source-count: 2
status: active
open-commitments: 2
open-questions: 2
---

# Business Central is the only source of truth for vendor bank details (Oct 13 2026)

**Decided:** October 13 2026, by [[wiki/people/val-levitan.md|Val Levitan]], on the [[wiki/meetings/2026-10-13-bank-of-america-cashpro-business-central-source-of-truth-and-customer-ach-portal.md|Bank of America CashPro call]] (3:32 PM Eastern) with Brooks Darnell of [[wiki/organizations/bank-of-america.md|Bank of America]]. [[raw/Meeting_Notes_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]

## What was decided

- **The rule.** "From the controlling perspective, the source of truth. For vendors is residing in Business Central." Bank data for a wire must come "every time from Business Central, not from the template." [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
- **What it stops.** Today, when a supplier's bank details change, "our guys go inside of the bank, the template, and change it there", and Business Central stays unchanged. Val does not accept this. [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
- **No templates kept at the bank.** "What I don't want is for the template to continuously live inside the Bank of America ecosystem." [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
- **No manual entry either.** If the template is not saved and the data cannot come from Business Central automatically, someone must set it up each time: "Then it becomes laborious and unacceptable… That's how I'm doing it now, and it's not working for me." [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
- **If the base CashPro cannot do it, JVL moves up.** "If the initial platform cannot accommodate this feature, then we want to move to the advanced platform." And later: "Then I should go into more advanced systems." [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]

## The options Brooks laid out

- JVL sends about "twenty to thirty wires a month" (Brooks's figure). Wires can be keyed by hand, sent from saved templates, or uploaded as a **CSV file** with many wires on one file. Brooks believes CSV upload is in the base CashPro: "From my understanding, that's correct. I'll double check that." **XML** files need "Cash Pro Connect", at extra cost. [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
- Controls can split the work: some employees only set up a payment; a primary admin or a senior person approves it. [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
- Brooks's first view on Val's rule: "I think we don't have a way of having the system pull it from Business Central… I think with wires, they basically force you to enter that information." He will ask Connie, the bank's API specialist. [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
- Val on cost: "what's important is not the initial cost. My cost on Nathan is much greater than the cost of the platform." [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]

## How it sits against earlier sources

On Sept 8 the bank's specialist Connie said wires at JVL's volume are manageable in CashPro Online with a saved template per vendor (see [[wiki/organizations/bank-of-america.md]], Sept 8). Val's rule rejects that template model for JVL. This is a JVL ruling made after the bank's suggestion, not a contradiction between sources. On Aug 27 Val called outgoing vendor payments "stage two" of the Bank of America work (see [[wiki/topics/business-central-erp-implementation.md]], Aug 27). [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]

## Open commitments

- [ ] Brooks Darnell (Bank of America) — confirm with Connie that CSV wire upload works on the base CashPro, without the upgraded platform — due this week (week of Oct 13 2026) — [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
- [ ] Brooks Darnell (Bank of America) — ask Connie whether the bank can take wire bank details from Business Central with no person entering them — due this week (week of Oct 13 2026) — [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]

## Open questions

- Can Bank of America take vendor bank details from Business Central automatically? If not, what does the "advanced" platform cost and include? — [[raw/Meeting_Notes_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
- Does the base CashPro really support CSV wire upload? Brooks was not fully sure. — [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]

**§15 #9:** no account, routing or other banking identifier was spoken; none is recorded. **§15.8:** clear — Val's remark about Nathan's cost carries no figure.

## Sources

- [[raw/Meeting_Notes_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
- [[raw/Meeting_Transcript_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026.md]]
