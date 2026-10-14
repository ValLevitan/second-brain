# Meeting Summary — alignment
**Date:** October 8, 2026, 3:59 PM – 5:37 PM Eastern
**Duration:** ~97 minutes
**Attendees:** Val Levitan, Genadi Peari
**Raw transcript:** [[Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026]]

## Summary

Held in Russian.

**BOM standard.** Genadi made the standard for building bills of materials for products and sent Val a pull request. He wants to write one more standard: how to release part numbers (how to assign new numbers). Val works closely with Nathan and expects Nathan to show something on Monday.

**Validator to Minsk.** The validator bought in China and sent to Minsk has a tracking number, but it does not work yet. The supplier swears it was sent and says the number will show in a few days.

**Flex Slim metal not ordered.** Val thought all metal for Flex Slim was ordered. Genadi: no, Misha did nothing. JVL has 10 sets. Brackets came in for the Georgia retrofit (under the card dispenser). The full cabinet metal for ~100 units was not started. Metal is the bottleneck because it cannot go by air; the rest can come fast. Val said he did not expect this.

**Peripherals and boards.** About 20 peripheral sets are on hand; parts for 100 were ordered, including scanners and monitors. Alekseev made the memory much cheaper. Alekseev orders boards online (cheaper and faster); Misha tells him what to order. Genadi thinks Alekseev places the order and Misha pays, but he does not know how this works without a PO. Alekseev also ordered small scanner interface boards (~$4) and 2 IQ boards. IQ: about 25 on hand, need to reach 100. Modems: ordered, 100–150 pieces. Val: IQ parts must be ordered.

**Drawings in GitHub.** All drawings are ready and in GitHub (JVL-Core, hardware-manufacturing repo). By a part number you get all drawings, revisions and the BOM. Val found a folder named "Defrend" (Genadi's old name for decals, labels and other items outside metal, plastic and harnesses) and could not understand it. Harnesses for Flex Pay sit under Flex Pay peripherals. Val: this is wrong, we will redo it. Names need a standard because nobody can remember them. Genadi committed today the Flex Pay Slim BOM with a table; from the number all parts can be pulled.

**Quotation from Hangzhou.** Val wants to practice himself: send the sheet metal drawings to Hangzhou (Jim Tao and Taratan in the system), so he understands the nuances when working with Nathan. Misha sends drawings by email from a report. Genadi's advice: decide the quantities first (for example 100 Georgia sets, some Texas sets); Texas has a different BOM inside (recycler instead of card dispenser); put the two BOM numbers in the system to get a flat list with quantities; ask quotes for 100, 300 and 1,000 so the supplier does not do the work three times; hinges go to a different supplier. Val first said a $200 difference is cheaper than sorting, but wants Texas included too. Prices should go into BC, not GitHub. The Texas BOM does not exist in BC; Genadi only made the recycler part. Val said not to add it because Nathan will do it fast; Genadi said it takes 10 minutes; Val agreed.

**Misha's report.** Misha has a report: enter a product number and quantity, and it shows a flat structure with on hand, on order, in shipment and shortage. Genadi says this is the main tool Misha works with.

**Flex Port back cover for Aristocrat.** Genadi will make it: one large round hole in the middle for all wires. Street cabinet: Val had said to wait (door type, printer, slim or not); still on hold.

**Misha leaves; Mery takes over.** Misha will leave from January (Val thinks it will be sooner). Val proposes Mery (name as heard) takes his role. She returns from vacation on the 19th; training in November and half of December. She speaks Spanish, which helps with Elizabeth. Genadi says the system can work automatically now if the BOM stays in BC. Val: we will not leave it; it is wrong. Focus for the week of Oct 12–20: make the BOM work as Val wants. Val will be in Georgia. Genadi may take some days off but will connect if needed; he will test Nathan's work.

**Data contracts.** Val: the biggest GitHub job, and fully on Genadi, is data contracts. Genadi admitted he did not understand Val's email (revisions vs. components by project). Val explained: three systems (Jira/Confluence, GitHub, MSBC). One Jira project = one GitHub repository. Val's table lists 13 repos (monitors, touchscreens and controllers, 5G modems/antennas/Wi-Fi/routers, power supplies, harnesses, PCBs, sheet metal, plastic, mechanical, labels, etc.). Each repo describes its devices with data contracts: connectors, signals, resolution, size, mounting studs, thread type. AI then finds wrong harnesses, wrong screws, wrong monitors. Supplier datasheets already hold most of this. Development already has 132 repos with prose and data contracts; tests are written automatically. Genadi asked if folders in one repo are enough; Val: no, each project is a repo, including fasteners and labels. Genadi said even if this works, the company will not move forward because of it. Val disagreed: with Misha leaving, it would be a tragedy in a company that depends on one person. Genadi agreed the AI is very smart and the contracts will help over time. After the cleanup, MSBC stops being the BOM source and holds only financial and administrative data per vendor. Next week's goal: be able to order without Misha. Genadi: everything exists except the BOM source and a report; Val: the report also needs everything to work right.

## Decisions Made

- **The BOM will not stay in MSBC as its source; MSBC keeps only financial and administrative data.** — Val rejected Genadi's idea to start now with the BOM in BC. (Decided by Val Levitan)
- **One Jira project = one GitHub repository, including fasteners and labels; folders inside one repo are not enough.** — so each part family has its own data contracts. (Decided by Val Levitan)
- **Folder names like "Defrend" and harnesses under Flex Pay peripherals are wrong and will be redone; names need a standard.** — nobody can remember custom names. (Decided by Val Levitan)
- **Week of Oct 12–20: all effort on making the BOM system (Nathan's work) work.** — goal is ordering without Misha. (Decided by Val Levitan)
- **Mery (name as heard) will take over Misha's role; training starts Oct 19 and runs through November and half of December.** (Decided by Val Levitan)
- **Genadi adds the Texas BOM to BC now.** — Val first said wait, then agreed since it takes 10 minutes. (Decided by Val Levitan, Genadi Peari)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver | Show progress on the BOM system | Oct 12 | High | Stated by Val; Nathan not in meeting |
| 2 | Genadi Peari | Chase the tracking number for the validator shipped from China to Minsk | TBD | Normal | Supplier says a few days |
| 3 | Genadi Peari | Write the standard for releasing / assigning new part numbers | TBD | Normal | Next standard after the BOM standard |
| 4 | Genadi Peari | Add the Texas Flex Slim BOM to BC | Oct 8 | Normal | "10 minutes" |
| 5 | Genadi Peari | Make the Flex Port back cover for Aristocrat (one large round hole for wires) and send it | TBD | Normal | |
| 6 | Genadi Peari | Send Val the link to Flex Pay Slim in the hardware-manufacturing repo | Oct 8 | Normal | Offered in meeting |
| 7 | Genadi Peari | Test Nathan's work as soon as it is ready | Oct 12–20 | High | |
| 8 | Genadi Peari | Write data contracts for each hardware repository, per Val's 13-repo table | TBD | High | "Fully on you" |
| 9 | Val Levitan | Prepare a quotation request to Hangzhou (Jim Tao, Taratan) for Flex Slim sheet metal, Georgia and Texas, himself | TBD | Normal | Practice before Nathan's system |
| 10 | Val Levitan | Start training Mery on ordering | Oct 19 | High | Through Nov and half of Dec |
| 11 | [Needs Val's confirmation] | Order IQ parts/boards (reach 100 units) | TBD | Normal | "This must all be ordered" |

## Open Questions

- What else is not ordered for Flex Slim and peripherals? Someone must check (Genadi). Who owns this is not set.
- How does Misha pay Alekseev's online board orders without a PO? Genadi does not know.
- Quote quantities: Genadi suggests 100 / 300 / 1,000; split between Georgia and Texas not set.
- Street cabinet configuration (door type, printer, slim or not) is still on hold.
- Genadi's possible days off in the week of Oct 12–20 (dates unclear in transcript).

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-14*
*Source meeting: alignment*
