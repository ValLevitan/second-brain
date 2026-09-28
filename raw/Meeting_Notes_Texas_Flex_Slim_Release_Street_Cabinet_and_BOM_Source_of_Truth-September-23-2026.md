# Meeting Summary — alignment-September 23, 2026
**Date:** September 23, 2026, 11:05 AM – 11:58 AM Eastern
**Duration:** About 53 minutes
**Attendees:** Val Levitan, Genadi Peari
**Raw transcript:** [[Meeting_Transcript_Texas_Flex_Slim_Release_Street_Cabinet_and_BOM_Source_of_Truth-September-23-2026]]
**Language:** Russian, with English technical terms throughout

## Summary

This was the regular alignment call between Val and Genadi. It covered four subjects: finishing the Flex Slim and releasing its Texas version, two small IQ items, whether JVL should build its own TITO desktop box, the street cabinet, and — at the end — where the bill of materials lives. The last two were not settled and both were pushed to later work.

**Flex Slim — finishing touches.** Val asked for two changes on the unit they are looking at. The harnesses that connect all the boards should be made shorter so they do not lie in a bundle, and the boards must be covered with a lid or a mesh. Val was firm: "it must be covered, this is not acceptable as it is." Genadi said Provision has prepared a frame but nothing has been ordered yet, and a lid can be done. On the monitor assembly, Genadi said Mandy's team had assembled it wrongly; he made a video with her and walked through every point, and she redid the harness herself. He expects the result to be clean and production-ready.

**The Texas version of the Flex Slim.** Genadi has checked it and there is no change inside the cabinet. The difference between the Georgia and the Texas product is exactly two things: the card dispenser comes out, and a **GCM three-site recycler** goes in where the bill acceptor was. The mounting points already in the cabinet are reused. The only new work is **three extra parts** (the cage/door). Genadi said he would release this today, together with the Texas bill of materials.

**How many, and how to ship them.** There are **10 Flex Slim prototype sets**, split between Georgia and Texas. Val said that is enough for two months and asked for the three extra parts in quantity 10, sent by air. Genadi pushed back — air is not needed, because the lexan will not be ready for a month and a half anyway, and the Minsk shipment sets the pace. Val said the Minsk shipment already left by FedEx Express, should land in about two weeks, and he thinks he can push it through in one more week — a month in total, which a sea shipment would not beat. He then offered to order only 5 by air if Genadi preferred. Genadi said small parcel shipments of bulk parts are simply throwing money away, and Val agreed with him. **The quantity is 10; the shipping mode ended unresolved.**

**Cash and purchase orders — the reason Genadi raised it.** Genadi said he did not see Mikhail Perelman moving on the Georgia order, and asked whether Val had told him to hold. Val said no, the opposite — Mikhail has issued many purchase orders and Val has signed them, but Val is managing cash. He wants Mikhail to negotiate with the suppliers so that either the release or the payment moves; the terms are old, prepayment is written into all of them, and Val called prepayment unreasonable. His concern about Mikhail was specific: *"He accepts their terms, and that is where it ends. After that you cannot move him."* Val said he was trying to sit down with Mikhail that day and go through every signed order to decide what to pay and how much. That meeting happened two hours later — see [[Meeting_Notes_Open_Purchase_Order_Payment_Walkthrough-September-23-2026]].

Genadi's own point was narrower: the Flex Slim metal is the long-lead bottleneck. Fifty sets of metal take two months. If Val later wants a deployment faster than two months, that is where it will break.

**Two small IQ items.** First, the printer cover: the mold will take a long time, so Genadi proposed rapid-prototyping a few covers now. Val agreed and asked for **20**. Genadi said the part is only a cover, carries nothing, and nylon does not crumble. Second, a board fault: Alekseev accidentally shorted plus to minus on the IQ mainboard. There are two power connectors (an option so a cheaper power supply can be used) and a sense line that detects which one is plugged in; if one is not plugged in, it shorts. Val said it can simply be cut with a knife. Genadi had already given the team that workaround and the board itself is corrected. Val said he had missed this problem entirely and had not known about it.

**TITO desktop — Genadi found it already exists on the market.** This is the most consequential finding of the call. Genadi started reviewing the design and saw large plastics, meaning an expensive part. So he checked the market first, and found that **both GCM and TransAct already sell a "TITO desktop"** — he had posted the links in the chat. He said it is exactly what JVL is building now, and Val agreed: "Absolutely." Val's response was immediate — *"nobody needs it, nobody needs it"* — do not do it by force. For the short run JVL will use the existing product; the decision on how to handle it long term comes later.

Genadi noted JVL's own box would have been better, because it would accept any printer, whereas these will likely only take their maker's own printer, and TransAct probably holds most of the market. But he agreed it is better not to put money in. Val's addition: *"money, and most importantly time — there is no time."* **Development on JVL's own box stops.** Genadi will get the documentation (there is none published on connecting it to IQ) and order a sample for Georgia; the plan is to connect it to IQ and offer the customer two options.

**The street cabinet — wood or metal, not settled.** Genadi is clear to start, and will do the layout tomorrow and work with Igor on presentation pictures for Val.

Val advised against metal for the enclosure, pointing out that Frank builds his from plastic and the other maker from plywood. His two arguments were:

1. **Logistics.** Metal is made in China and has to come by sea, in containers. JVL's warehouse here is about **7,000 square feet with low ceilings** and cannot hold stock. If consumption is one container a month, you need three containers in the system at once — one being worked from, one being unloaded, one in transit. A local supplier cutting boards continuously removes all of that. Val expects large quantities because the price will be very low.
2. **Form.** A street cabinet needs no podium; it stands upright, especially a vertical machine, and needs a long rigid back wall. Metal does not lay out that way — no machine handles a sheet that size easily — so it has to be split, bent and screwed together, the way the current cabinet is built in three parts (monitor section, base, podium). That is what makes it expensive. What a street cabinet actually needs, in Val's description, is a well-presented TV, a box of a set depth at or below panel level for the bill acceptor and the printer, and a few cheap brackets with straight rectangular cutouts.

Genadi's counter-arguments were just as specific. Wood means a very large number of brackets — every feature needs one, every mount needs threaded inserts and pilot holes, and someone has to drive a great many screws. That is production time and a source of assembly error. He is also not convinced wood is cheaper: wood cannot be made cheaply in America, the prices they took recently were "insane", so the goods still ship from China either way and there is no saving in the material choice. On the metal side, he argued the street cabinet in metal would be a **simpler** build than the current product — no welded or shaped parts — and would come out perhaps **40% cheaper** than the current metal cost. Val put JVL's current metal cost, with duty and tariffs, at roughly **$350 to $500** per machine, though he said he had not calculated it. Val did not accept the 40% figure: it will still be big parts, still containers, still unloading.

Genadi also recalled a wooden machine from long ago (Val said "Clips"; Genadi thought it was called something else) that was painful to assemble. Val said the intent there was different — a large shaped plastic front around a non-flat tube — and that in the wooden cabinet he himself built 30 years ago all the appeal was in the cabinet profile, and he does not remember it being hard to assemble.

The exchange got tense. Genadi said at one point, *"Okay. I cannot work this way. I have nothing to say."* Val then explained his method: architecture first (settled — a 43" TV, one touchscreen, a button panel), then the materials that go into it, which is the level they were at. Genadi's position was that this cannot be argued without numbers: *"this is your gut feeling that wood is better; my gut feeling is metal is better. I am not arguing, you are probably right — but if you see a wooden cabinet costs 400 and this costs 200, you will ask why pay extra."* He asked for a review — prices and manufacturers — and said the decision would then come by itself. He added, *"you know how I fight for every penny in this design. There is no sentiment here. Whatever is better is better."* Val closed it warmly: *"I have absolutely no doubt your heart is in the right place."*

**Resolution:** Genadi pricing both, decision on numbers afterwards. Genadi said "let's start working" and will show the complexities when he gets into it. He also said the design does not change for him either way — build it in wood, and if it is not liked, move to metal. Val disagreed that little changes in the design, but did not block the start.

**Where the bill of materials lives — GitHub or MSBC.** Val asked where the GitHub ↔ MSBC synchronization project stands, saying he has had no time with Nathan Carver at all and does not know what is needed there. Genadi said he had written Nathan his vision, understanding the point to be that synchronization lets Val put an AI executive over the whole picture. Val corrected the premise directly: *"I can point my AI executive at GitHub just as well — maybe more easily. I do not need the synchronization for that."*

From there the two talked past each other for fifteen minutes, and Val said so at one point ("we are lost in two pine trees"). The positions:

- **Genadi:** he builds the BOM in Business Central, and it is convenient there because a revision change propagates automatically to all related items. All the prices are in MSBC. All orders go out of MSBC. A requisition is easier to raise in BC. He cannot picture maintaining BOM trees in GitHub — a BOM is a list of part numbers and quantities, and Flex has ten different modules; would that be Excel files that merge? And how would they be changed physically?
- **Val:** the sequence is drawing first, then part number, then MSBC. No drawing, no part number. You draw in SolidWorks, the finished part goes into GitHub where the versioning and the history live, the part number list is then carried into MSBC, a supplier is attached, quotations come in, a vendor card with banking information is created for a new supplier, and only then does a purchase order go out against it. The BOM is the **final result** and it is derived from the design; therefore **the source of truth is the latest version of the design, which is in GitHub.**

Genadi asked the question straight: *"the BOM — MSBC or GitHub?"* Val: *"GitHub, of course, because that is the latest version of the design."* Val's reasoning beyond the mechanics was cultural: *"You do not start your design in MSBC. You have no thoughts in MSBC. In front of you is the design and you work with the design, and I would not want to change that, because it is the right culture."*

Genadi twice suspected Val was asking for something larger — *"do you want to build your own ERP system in Git?"* — which Val said he did not understand and did not know how to answer. Val also said, of building it in GitHub, *"you are building it there now — that is already a settled question,"* which Genadi did not accept; he said he builds it in BC.

**One thing was agreed cleanly:** Genadi asked whether the synchronization works both ways. Val: *"Both ways is bad. There must be one source of truth. Otherwise you have two sources of truth."* Genadi did not argue this.

They also disagreed on a smaller point — whether the part number lives in GitHub. Genadi said the link between MSBC and GitHub runs through the part number, which makes finding the documentation trivial. Val said GitHub holds the last drawing number and the last drawing revision, and he is not even sure the part number belongs there at all, since GitHub is for code.

The conversation was cut off mid-thread — Genadi had just started explaining that JVL has a worked-out part-numbering system and that he assigns the numbers by hand when he makes the drawings — when Val said he had a call starting in three minutes. **Val took the undertaking to schedule this as its own meeting.**

## Decisions

- **The Flex Slim boards must be covered** with a lid or mesh, and the harnesses shortened. Open boards are not acceptable. *(Decided by Val Levitan)*
- **The Texas Flex Slim = the Georgia Flex Slim, minus the card dispenser, with a GCM three-site recycler in place of the bill acceptor.** Nothing else in the cabinet changes; existing mounting points are reused; only three new parts are needed. *(Genadi Peari, accepted by Val Levitan)*
- **Genadi releases the Texas configuration and its bill of materials today.** *(Genadi Peari)*
- **Order 10 sets of the three extra parts.** *Shipping mode left unresolved — Val asked for air, Genadi objected that air is wasted because the lexan is a month and a half out, Val offered 5 by air, then agreed with Genadi that parcel-shipping bulk parts throws money away.* *(Val Levitan and Genadi Peari)*
- **Rapid-prototype 20 IQ printer covers now rather than wait for the mold.** *(Decided by Val Levitan, proposed by Genadi Peari)*
- **JVL stops developing its own TITO desktop box.** GCM and TransAct already sell one. For the short run JVL uses theirs, connects it to IQ, and offers the customer two options. *(Decided by Val Levitan, on Genadi Peari's market review)*
- **Work on the street cabinet starts now.** Genadi does the layout tomorrow and works with Igor on presentation pictures. *(Val Levitan and Genadi Peari)*
- **Wood versus metal for the street cabinet is NOT decided.** Genadi prices both and checks manufacturers first; the decision is made on the numbers. *(Genadi Peari's position, accepted by Val Levitan)*
- **The synchronization between GitHub and MSBC must be one-way.** There is one source of truth; two-way sync is rejected. *(Decided by Val Levitan, not disputed)*
- **Val's ruling: the BOM's source of truth is the latest design version in GitHub, not MSBC.** *Genadi did not accept this and the question stays open — see Open Questions.* *(Stated by Val Levitan)*
- **The GitHub ↔ MSBC conversation gets its own meeting.** *(Val Levitan)*

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Release the Texas Flex Slim configuration — card dispenser out, GCM three-site recycler in — and the Texas bill of materials | September 23, 2026 | High | He said he would do it today |
| 2 | Genadi Peari | Order the three extra parts (cage/door) for the recycler, quantity 10 | TBD | High | Shipping mode unresolved — air versus sea, see Open Questions |
| 3 | Genadi Peari | Order 20 rapid-prototype IQ printer covers | TBD | Normal | Rather than wait for the mold |
| 4 | Genadi Peari | Get the documentation for connecting the GCM / TransAct TITO desktop to IQ | TBD | High | None is published; he said he would try |
| 5 | Genadi Peari | Order a TITO desktop sample for Georgia | TBD | Normal | Val: "certainly" |
| 6 | Genadi Peari | Do the street cabinet layout, then work with Igor on the overall picture to present to Val | September 24, 2026 | High | Igor's surname was not said |
| 7 | Genadi Peari | Price wood versus metal for the street cabinet — prices and manufacturers — so the decision is made on numbers | TBD | High | This is the condition he set for deciding |
| 8 | Val Levitan | Schedule a separate meeting on GitHub ↔ MSBC synchronization | TBD | High | He named Andrei and possibly Nathan Carver; one further name in the recording was not clear |
| 9 | Val Levitan | Sit with Mikhail Perelman and go through every signed purchase order to decide what to pay | September 23, 2026 | High | ✔ Done the same afternoon — see [[Meeting_Notes_Open_Purchase_Order_Payment_Walkthrough-September-23-2026]] |
| 10 | Val Levitan | Get Mikhail Perelman to renegotiate supplier terms away from blanket prepayment | TBD | Normal | Raised as a standing frustration, not assigned a date |

## Open Questions

- **Wood or metal for the street cabinet.** The core disagreement of the call. Val argues logistics and form; Genadi argues assembly complexity, bracket count and a claimed 40% saving in a simplified metal build. Unresolved by agreement — Genadi prices both first.
- **Where the BOM lives, and how BOM trees would be maintained in GitHub.** Val ruled GitHub is the source of truth because it holds the latest design. Genadi says he cannot picture maintaining multi-module BOM trees there and continues to build them in Business Central. Deferred to a dedicated meeting.
- **Whether the part number belongs in GitHub at all.** Genadi says the part number is the link between the two systems. Val says GitHub holds the drawing number and revision, and is not sure the part number belongs there. Cut off when Val had to leave.
- **Where a part number is first created.** Genadi had begun describing JVL's worked-out numbering system, assigned by hand when he makes the drawings, when the call ended.
- **Air or sea for the 10 sets of recycler parts.** Val and Genadi ended on opposite sides and then Val agreed with Genadi's cost point without restating the instruction.
- **Who pays for the GCM / TransAct TITO desktop, and how it is priced.** Genadi does not know; they may charge for the box separately or bundle it with their printer. Val said he would not worry about it yet.

## Dispatch Log

---
*Processed from Teams transcript on September 23, 2026*
*Source meeting: alignment-September 23, 2026*
