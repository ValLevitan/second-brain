---
tags:
  - meeting
  - workflow-design
  - project-planning
  - val
  - pavel
  - flex-pos
---

**Transcript**

June 19, 2025, 10:04AM

**Nathan Carver** started transcription

**Nathan Carver**   0:08  
OK, so I don't have any existing use cases on the flex PLS, so we can just start.  
Whiteboarding what we have.

**Val Levitan**   0:30  
Can we review the objective of this meeting? What are we trying to achieve?

**Nathan Carver**   0:36  
So what I'd like to achieve for this meeting is create the initial use case or workflow of what the Flex POS will be for that first first phase.

**Pavel Frolov**   0:49  
Yes.

**Nathan Carver**   0:51  
I believe that was what, September 1?

**Val Levitan**   0:54  
Right, OK.

**Nathan Carver**   0:55  
Yeah.  
So that at least we can start, um, identifying the work that we need to do to achieve that goal.  
Let me see here. Yeah, OK.  
So I will share this.  
Mhm.  
This whiteboard, OK.  
All right, so the goals for September 1st, what I wrote down from yesterday is we want to connect the three machines. That would be a JVL machine and two competitors machines.  
We're gonna connect the PLS. Um.  
We'll have the PLS connected.  
Not to the machines, but ready to actually.  
Once the generated, once we generate a winning ticket, we will then use the POS to generate the the gift card.  
And then we'll validate the card value of the ticket. So those are just the notes I jotted down. So let's I'd like to go through that workflow in more detail. It seems pretty straightforward, but um.  
I think that would be valuable.

**Val Levitan**   2:51  
I I should probably take a second position in this meeting and I think it's more important for you guys to discuss it.

**Nathan Carver**   3:00  
OK.

**Val Levitan**   3:01  
I I can easily intervene, but.

**Nathan Carver**   3:11  
OK.

**Val Levitan**   3:11  
I think it will be more productive for you, both of you, to interact with each other.

**Nathan Carver**   3:16  
Yes, that that works for me. OK.  
So I'll start just drawing and asking questions and um.  
Probably you and I can just kind of talk through and direct me down if I'm going the wrong way.

**Pavel Frolov**   3:34  
Sorry, my my suggest a little bit different to to to start this meeting probably we need firstly to take a look on capabilities of the XPOS.

**Nathan Carver**   3:40  
Sure.

**Pavel Frolov**   3:53  
Variant with Mutagus simplified variant. I tried to create some first approach documentation related to capabilities. Probably we can review it first to understand.

**Nathan Carver**   4:10  
Yeah.

**Pavel Frolov**   4:12  
Scope of possible use cases. So actually I already committed this markdown file for Flex POS in docs folder. You can open it and we can go through this.  
It I you  
Uh, capabilities probably update something and at least I made some some notes related to securities that we we have never discussed before.

**Nathan Carver**   4:47  
Okay, perfect.

**Pavel Frolov**   4:51  
Would you like to me to share a screen?

**Nathan Carver**   4:55  
Yeah, that would be great. I can share, but feel free to jump in.

**Pavel Frolov**   5:04  
So actually.  
Once again under the Flex POS repository of docs folder. Right now we have Flex POS Muto Goose capabilities file and I think the same file will be for POS.  
Full implementation, but but not now because this is a priority \#1 Mutabus. Correct me if I'm wrong.

**Val Levitan**   5:37  
As we're discussing September 1st beta test, please.

**Pavel Frolov**   5:42  
Yeah, yeah, this document exactly for this case. So this is a device with a 10 inches touch screen, magnetic swipe reader.  
Ethernet port and or some wireless Internet. So this this point we never discussed. I highly likely I think that this POS will be equipped with some.  
3G or other type?  
Uh, so this is designed for legacy yellow board and Muta goose.  
Operational modus, set up mode and work mode. Set up mode. It relates to some settings that can be.

**Nathan Carver**   6:46  
Mhm.

**Pavel Frolov**   6:51  
Set get probably to accept screens related to reporting and so on and to work mode. I think this is exactly what we started discussing discuss discussed yesterday.  
Um.

**Nathan Carver**   7:12  
OK.

**Pavel Frolov**   7:17  
So here for cashier workflow seems this is the same as we started to discuss yesterday, but one moment here I need to keep your attention here.  
In case when the cashier want to issue a card and enter some value manually.  
I think we need to support some security.  
Either by entering pin code or scan some security QR code or swipe special magnetic card to access to special access for cashier or operator or.  
Probably one more idea here. Probably we need to generate some pin code for operational day and this code can be accept accessed.  
Some somehow differently, for example by using mobile phone, mobile application or access to cloud server.

**Nathan Carver**   8:39  
OK, that makes sense.

**Pavel Frolov**   8:47  
So this is just a common descript common points related to.

**Nathan Carver**   8:53  
I'd be, uh, using like an authenticator on a phone on a mobile phone.

**Pavel Frolov**   8:59  
Yeah, probably.

**Nathan Carver**   9:02  
OK.  
Yeah, so if if someone has access to the Flex POS, then they could just generate gift cards, right? 'cause they don't need a ticket or anything like that. There's.

**Pavel Frolov**   9:15  
At first, uh, MVP release, yes.  
So here's a section related to security firmware update options as a separate capability.  
Lease feature we need to support limiting to to set expiration date for a particular POS or push.  
Disabled message from the server.  
To to disable working of current POS next capability remote initial setup. This is an option to push credential settings.  
Some other use the graphic user interface settings probably from our cloud server and lock management this other capability.

**Nathan Carver**   10:30  
Um.

**Pavel Frolov**   10:31  
So any question?

**Nathan Carver**   10:33  
Yeah, that that makes sense to me.  
Yeah, I think authentication securing the device will be a.  
Have a conversation.  
OK.  
Is.  
So the device is connected to the cloud. We have the ability to shut it down remotely.

**Pavel Frolov**   10:52  
8\.

**Nathan Carver**   10:59  
Or at least um.  
Terminate the lease right so I can't do any activity.  
What does it communicate to to actually generate the gift card? What service does it use to do that?

**Pavel Frolov**   11:18  
To generate Uh cards.

**Nathan Carver**   11:20  
R2 so it it.  
It prints to the to the magnetic strip on the card or activates it, but what service is actual financial transaction done?

**Pavel Frolov**   11:33  
Income, income, yeah, probably, probably we need to to to make a section, separate section related to issuing cards, but actually it.

**Val Levitan**   11:34  
In in Kong.

**Nathan Carver**   11:36  
OK.

**Pavel Frolov**   11:51  
To written in some sentences as in commas used, probably need to to separate a different section.

**Val Levitan**   12:01  
Just to help you out, I generated a first case that I described yesterday in the meeting and just maybe to save you some time, here's the use case.

**Nathan Carver**   12:12  
Oh, nice.  
Oh, perfect.

**Val Levitan**   12:23  
This is a player related case. This is very limited capability and this is for September 1st beta test release.

**Nathan Carver**   12:37  
OK.

**Val Levitan**   12:37  
So just for the record.  
Uh.  
Use case. I called it Manual Ticket Redemption for Flex POS target September 1st 25 beta release and goal is to redeem a paper from.  
Some people call it Mother Goose. Some in Georgia they call it Mother Goose. They're actually spelled out as Mutha.

**Nathan Carver**   13:05  
Mhm.

**Val Levitan**   13:08  
So redeem a paper payout ticket generated by Muda Goose with no barcode, just the printed value.

**Pavel Frolov**   13:17  
Hey.

**Nathan Carver**   13:18  
Yes.

**Val Levitan**   13:23  
A bunch of alphanumeric numbers that scanned yesterday for our record.

**Nathan Carver**   13:32  
OK.

**Val Levitan**   13:32  
And transfer its value to a prepaid card.  
As I mentioned yesterday, there is a bunch of cards.  
Hitting the market, but the most credible and the one that income is involved is a MasterCard prepaid MasterCard.  
Right now, for one more year, this MasterCard cannot be recharged. It's a single charge card.  
And that will comply with the new Georgia legislation that is coming into effect on June 1st, 2026\.  
So main steps.  
First step is ticket generation, so player wins on a gaming machine, any gaming machine that is retrofitted with Mother Goose.  
And as I mentioned yesterday, there are approximately 35,000 machines in the state, all of them retrofitted with Muda goose.

**Nathan Carver**   14:41  
Mhm, OK.

**Pavel Frolov**   14:43  
Yes.

**Val Levitan**   14:44  
So machine does not print the payout ticket, but the machine pushes the data into a printer and the printer is located within.  
The within the cache cache cage. I think I mentioned yesterday that the connection between Muda goose slot machine interface board.

**Pavel Frolov**   15:01  
OK.

**Val Levitan**   15:16  
And the printer I believe is RS485 if I'm not mistaken.

**Pavel Frolov**   15:20  
Yeah, exactly.

**Val Levitan**   15:23  
And that's a it's a wire. They actually run a wire from each machine to a printer.

**Pavel Frolov**   15:30  
It's a chainable connects from machine to machine.

**Nathan Carver**   15:34  
Mhm.  
OK.

**Val Levitan**   15:37  
OK, so I'm I'm going to change this here. Instead of machine prints a payout ticket, I'm going to say machine pushes data onto a printer that is located.  
Uh, within uh, cash cage.  
And so assuming that the value of a ticket is $82.00 as in this example.  
And it does not have a barcode, just alphanumeric numbers. So the player approaches the cash cage and.

**Pavel Frolov**   16:15  
Um.

**Val Levitan**   16:17  
The player needs to say, oh hi, I won $82.00 because there could be multiple wins at the same time and there could be multiple tickets generated at the same time, so they identify each other by the winning amount.

**Nathan Carver**   16:30  
Mm-hmm.

**Val Levitan**   16:32  
So there's no other security except calling out the number that he won. Sorry, the amount that he won. So the players visits a cage, says I won $82. A cashier manually.  
Grabs his ticket, looks at the ticket and enters the ticket value, whatever we establish as a value or the need for the fields instead of scanning by hand, enters the data into the POS.  
Of course, I mean, guys, you're engineers. You probably understand that a lot of things could be OCR now, but let's just go manual right now.

**Nathan Carver**   17:17  
Mhm.

**Val Levitan**   17:19  
So then cashier reaches out and takes a blank card which is not yet activated.  
And goes through a process. There are a couple of steps. You need to scan a barcode on the card or swipe a magnetic strip on the card. It connects to the cloud server supplied by income.  
Exchanges the data with income and income sends the validation key as well as deducts $2.00 from the winning. So a typical win of $82. A player will get $80.00 on the card.  
The POS confirms the funding, so I guess you have to swipe the card a few times. I assume Pavel would know better. I don't know. No once. OK, sorry, great. So you scan the you swipe the card once.

**Pavel Frolov**   18:15  
Oh, not necessary.  
But.

**Val Levitan**   18:23  
And um, that's it. The the card now has $80.00.  
And uh, a cashier.  
Hands over the loaded prepaid card to the player. There might be an option where the player says, OK, give me the ticket as well. So here's your ticket. Here's your card. Thank you very much for playing. Come back.  
For this particular beta test, I just want to repeat myself so it's crystal clear.  
September 1st will start at the beta location.  
With income, so the location needs to be registered. So we have a registered location which is our warehouse address.  
Showroom address in Georgia. So it has a specific location identification number on on the Incom server, right? So the beta test will take place.  
At this location.  
Three machines equipped with a mother goose board.  
One of them is JVL machines to other competitive competitors machines.  
A printer.  
And the POS.  
And we will test the most simple workflow to satisfy this.  
Test case. Uh, sorry, this use case.  
By the way, that brings me to the subject. We should probably write test cases, positive and negative test cases for this, and during this test we want to test positive and negative cases.  
So that's the objective for September 1st and that's the use case for September 1st.

**Nathan Carver**   20:28  
Yeah. Perfect.

**Val Levitan**   20:32  
Further, I'm I'm making a point the the barcode validation is not MVP. By barcode I mean Cito.  
No OCR of any sort. We got to make sure that processing fee is deducted. That's one of the positive tests we have to run. No any sort of automation is required at the point.  
At this point.  
Yeah, that's it.  
That that's your first use case.

**Nathan Carver**   21:10  
OK, you can send notes here.  
OK, so for this first use case, um.  
We are essentially testing the handshake that we can generate a card from the three different machines, but we're.  
That we can generate a valid gift card and that we have a good the handshake is between Incom and Flex POS and we're ensuring that we can deduct the processing fee.

**Val Levitan**   21:45  
Well, I didn't want to burden you with this subject, but since you raised it, we have another business architectural model which we'll call the E wallet or temporary wallet.

**Nathan Carver**   21:59  
Mm.

**Val Levitan**   22:03  
And under this architecture, there's slightly different flow real quickly. This is where a player walks into a location and instead of approaching a machine, he approaches a payment kiosk.

**Pavel Frolov**   22:07  
OK.

**Val Levitan**   22:18  
Uh, he makes a payment that a payment kiosk.  
The kiosk issues a temporary wallet in the form of a barcoded ticket, which is very similar to a Tito ticket, but it's not a Tito ticket, it's just a temporary wallet which is paired up with a PIN number.

**Pavel Frolov**   22:24  
Yes.

**Val Levitan**   22:41  
The reason I.

**Nathan Carver**   22:42  
OK, ticket and pin.

**Pavel Frolov**   22:43  
And no, no, no actual value printed on the ticket because it can be changed from time to time.

**Val Levitan**   22:50  
And then he takes this ticket and, you know, walks, walks around the location between the machines and the ticket is your temporary value carrier. This business model will probably not adapt itself in Georgia, specifically in Georgia.  
Maybe somewhere else. This was our initial thought over a year ago of how we wanted to approach the market. We, however, realized that this is probably not a good business model for Georgia Co-am, but we went ahead with it anyways, the reason I'm telling you this.  
It's because as part of this business model, there's still a process of validating the value with income and because this model, we started to work on this model earlier.  
It is ready today for positive integration, positive test integration. We we didn't really push it too much into negative testing.

**Nathan Carver**   23:56  
OK.

**Val Levitan**   23:56  
So it's kind of a. It allows us to test our beta location, which is the warehouse, and it allows us to test a validation with income and the transaction between.  
The player to income and income to JVL.

**Pavel Frolov**   24:13  
Mhm.

**Val Levitan**   24:17  
Because income and JVL are partners on this.

**Nathan Carver**   24:20  
Right. OK.

**Val Levitan**   24:21  
There are there are three three-way bank banking transaction from player to income during the pairing process.  
From income to.  
To JVL. My point again that we're testing this transaction now and it should be polished in a state where you know, kind of cut and paste by September 1st.  
So hopefully you will have to do very little testing on September 1st for the income play player income JVL portion of transactions. That's that's what Pavel is doing now.

**Nathan Carver**   24:54  
OK.  
OK.  
And that's what the E wallet, right? Or is that also with?

**Val Levitan**   25:16  
That's the E wallet. We call this architecture E wallet.

**Nathan Carver**   25:17  
Yeah.

**Val Levitan**   25:22  
Sometimes we we loosely use e-wallet or temporary wallet.

**Nathan Carver**   25:27  
Temporary one, OK and the other this architecture is just flex POS is how we refer to it.

**Val Levitan**   25:35  
Uh, no, this has uh.

**Nathan Carver**   25:40  
Or not the e-mail, but the the.

**Val Levitan**   25:40  
Uh.  
Flex. It has flex pay the the central. The central element of this system is flex pay because this is where you ignite your action. This is your first point of contact in a location.

**Nathan Carver**   25:46  
OK.  
OK.  
OK, sounds good.

**Val Levitan**   26:05  
And and exactly for this reason, we think that this particular architecture will not survive because the first point of contact for the player is always a machine. So this took the player on a detour.  
Having him approach the flex pay first.  
Instead of a machine. So we think that if it competes with other architectural designs, it will not survive.  
It's a it's a major shortcoming.

**Nathan Carver**   26:41  
OK.

**Val Levitan**   26:41  
The the player should gravitate towards the machine and all the transactions should be at the machine and.  
Yeah.

**Nathan Carver**   26:52  
OK, that makes sense.

**Val Levitan**   26:53  
Just, just, just because we're already talking about it. Just one more point.  
This is where everybody feels that.  
Having the MasterCard as single credit like credit once.  
Is is a is problematic and having a card that cannot be reinserted back into the machine is a problem. That's why we feel that the master card.

**Nathan Carver**   27:16  
OK.

**Val Levitan**   27:32  
Um.  
Architecture will change, and we know that it will change.  
For example, Incom is already working on a on a digital electronic wallet that allows at machine transaction.

**Nathan Carver**   27:53  
OK.

**Val Levitan**   27:54  
And and we know and we know that.  
The you could, you could probably take your card and you could probably have a device on the machine. Sorry, in a location where you could.  
Kind of.  
Take your your card, MasterCard, prepaid MasterCard, insert it and then insert a player's card or electronic wallet card almost and put the value.  
On that card or that closed circuit e-wallet, but you'll have to have a merchant number.  
Because MasterCard transacts only through merchant value. The moment the money is on MasterCard, the reverse transaction is a merchant number, right? You have to have a merchant number. But I I I have not discussed it with my team at all. Like this is the first time I'm raising this issue.

**Nathan Carver**   28:48  
Mhm.

**Pavel Frolov**   28:53  
OK.

**Val Levitan**   29:01  
Since we already have flex pay, my thinking is that or flex tower right, we could actually have.  
A merchant number attached to it.  
And um.  
Act as a merchant on a location.  
But but I I don't want to go there right now. It's it's not needed.

**Pavel Frolov**   29:29  
Yes.

**Nathan Carver**   29:31  
OK.

**Val Levitan**   29:32  
Just closing, I'm just giving you the shortcomings of the system.

**Nathan Carver**   29:34  
Yeah.  
Yep, that makes sense. OK.  
So for September one, it's just the flex payer architecture that we'll be testing.

**Pavel Frolov**   29:47  
I would say Flex POS Mutagus.  
Plus.

**Nathan Carver**   29:55  
Right. And that falls under and that falls under the the overall flex pay architecture. Is that how you would refer to it? No. OK.

**Val Levitan**   30:03  
No.

**Pavel Frolov**   30:06  
Absolutely isolated.

**Val Levitan**   30:06  
Yeah.

**Nathan Carver**   30:08  
OK.

**Val Levitan**   30:10  
So we don't even need flex pay in in the system.

**Nathan Carver**   30:15  
OK, so just flex POS, alright.

**Pavel Frolov**   30:25  
Sure.  
OK.

**Val Levitan**   30:25  
Are in 6 1/2 thousand locations. So just picture a state of Georgia, a bunch of variety stores, gas stations, bars that have these. I'm going to repeat this ridiculous term skill machines.  
With the more cash payout, it's prohibited by legislation. So the the entire state is filled filled with 35,000 machines, right?

**Nathan Carver**   30:46  
Mm-hmm.

**Val Levitan**   30:57  
And um.  
Each machine is equipped with Muda Goose and a printer. That's how it's architectured today.  
So remember I told you yesterday, if I was an operator and somebody would offer to me that minimum interruption, minimum investment, would I take that offer or would I try to convert it into a more sophisticated?  
Business schema with Tito ticket in, ticket out or electronic wallet or some other sophistication that required the hard cash investment.  
Probably not. I would probably try to refrain from spending money.  
For each location, I mean I would want the system that could grow with me if I needed to, but the first thing that I would probably want to place is the point of conversion of the card.

**Nathan Carver**   31:58  
Mm-hmm.

**Val Levitan**   32:06  
Of the winning in onto a card, and if I could achieve that and comply with the upcoming legislation as an operator, I would probably be happy with it.  
If something is hazy for you, if you if you cannot connect dots, ask. I mean it's I I don't know to what to what point you're now clear on this.  
I know our industry is weird. It's just it's not really.

**Nathan Carver**   32:35  
Um.  
Yeah, it's it's becoming more clear to me and I think I'll be, I'll definitely be asking more just to make sure I'm using the right terms and what I'm referring to things so.

**Val Levitan**   32:54  
Sure.

**Nathan Carver**   32:54  
Yeah, so like the architecture of E wallet versus.  
Flex POS.  
Uh, when we refer to our overall implementation of Flex POS, is that?  
That's just the name we're calling it, so everyone's gonna be able to identify it correctly.

**Val Levitan**   33:15  
So we we are interchanging hardware names, sorry names for the hardware with business schema.

**Pavel Frolov**   33:16  
But.

**Nathan Carver**   33:22  
Mhm.  
OK.

**Pavel Frolov**   33:28  
Actually, actually let me add something. The first business schema is e-wallet. The second business schema we will we can name it Tito.  
And the third business chema related to Mutagus.

**Nathan Carver**   33:51  
OK.  
OK, so Tito is where the flex POS would fall under, even though it's first pass, it's not connected to that at all, right?

**Val Levitan**   34:02  
Well.  
Cool.  
So I I think Pavel correctly gave you a list of scammers. So electronic wallet, Tito and Muda Goose.

**Nathan Carver**   34:14  
Hmm.

**Pavel Frolov**   34:21  
Yeah, the first schematic works with tickets in form of electronic wallet. The second schema works with theater tickets, different type of communications, but still tickets.  
And the thought schema works without any tickets.

**Val Levitan**   34:45  
Well, take a ticket of the cage, right?

**Pavel Frolov**   34:47  
Yeah, yeah.

**Nathan Carver**   34:49  
Mother Goose's ticket.

**Pavel Frolov**   34:50  
But but player but player do not have any in possession any tickets.

**Nathan Carver**   34:58  
Right, OK.

**Val Levitan**   34:59  
There are problems that Muda Goose has hereditary problem that a player is bound to one machine only. He cannot move between the machines when you when you play with cash or Tito or electronic wallet.  
You can you got tired of one machine. You could put the value back either on electronic wallet or you could print your Tito barcoded ticket and move on to the next machine.  
With Muda Goose you are bound to one machine, so you play it and.  
At the point of when you want to cash in, you have to go back to the cage.  
And cash out.

**Nathan Carver**   35:56  
OK, yeah.

**Val Levitan**   35:56  
And then return to a different.

**Pavel Frolov**   35:57  
And cash out and cash out can cash out can be taken only by goods and you can not enter goods into different machines. This is a problem.

**Val Levitan**   36:09  
Yes, by let's say you.  
Your cash out consists of, let's say, $82.00 of bananas.

**Nathan Carver**   36:16  
Mhm.

**Val Levitan**   36:17  
So you cannot take $82.00 of bananas and then feed it into another machine. It just doesn't work.

**Nathan Carver**   36:26  
Right.  
OK.  
Yeah, the business schemas help clarifies these things. So then the flex POS is able to work within multiple schemas at this point is the idea as a.

**Pavel Frolov**   36:29  
5\.

**Val Levitan**   36:38  
Well, well, Flex POS. So, so now you're talking about hardware devices. Let's just list hardware devices by name. So each name will have flex in front of it. Hyphen.

**Nathan Carver**   36:46  
Right.

**Val Levitan**   36:55  
So flex hyphen.

**Nathan Carver**   36:57  
Mhm.

**Val Levitan**   36:58  
And then we have port.  
PORT.

**Nathan Carver**   37:04  
Mhm.

**Val Levitan**   37:05  
Smib SMIB.  
P.  
Tower and the last one is POS.  
Point of sale.

**Pavel Frolov**   37:20  
And one more Tita server.

**Val Levitan**   37:24  
Sorry and and the and the Tito server. So what I named right now are hardware pieces and each one of them has a a different purpose for it. Now they could all work.

**Nathan Carver**   37:32  
Yep.

**Val Levitan**   37:41  
In various business schemas.

**Nathan Carver**   37:49  
OK. Yes, correct. Yeah, that makes sense.  
OK, perfect.

**Val Levitan**   38:00  
So now by having these various hardware offerings, we can address operators or sorry, masters. I'm gonna call them master because that's how it's called, how they're called in.  
Georgia under Coam legislation.  
We can satisfy master's desire.  
For any of the business schemas that they decide with the hardware that I listed.  
And they address and they address different needs. POS has its own need.  
Tito server, it's all need port, it's all need, it's all need.  
And so forth.

**Nathan Carver**   38:58  
OK.  
This makes sense to me.

**Val Levitan**   39:06  
The more and the more, the more we talk about it, the more it will make sense to.

**Nathan Carver**   39:06  
OK.  
Yeah, yeah, it's the ecosystem's becoming more clear. It's taking some time.

**Val Levitan**   39:16  
It's OK.

**Nathan Carver**   39:18  
Um, perfect.

**Val Levitan**   39:20  
It took it. It took me 41 years.

**Nathan Carver**   39:22  
Hopefully it's not that long for me.  
OK. So then for September.  
Pablo, is there any other, I guess overview you wanted to go through on the engineering side before we start looking at September 1?

**Pavel Frolov**   39:46  
Um.  
Probably I will ask you. I sent you yesterday a link to near my diagram. Do you have access to it?

**Nathan Carver**   40:02  
And let's see here.

**Pavel Frolov**   40:06  
I mean this one.  
Actually I just added yesterday this schema for.

**Nathan Carver**   40:14  
Um.  
Um.

**Pavel Frolov**   40:18  
Uh, schematic diagram related to POS.  
Uh, Mutagus. Uh schema. Business schema.

**Nathan Carver**   40:33  
Let's see here.  
Oh, the mermaid. Yes. Oh, I need to sign into that.  
Are we using SSO there?  
For the the mermaid chart login.

**Pavel Frolov**   40:51  
No.

**Nathan Carver**   41:07  
Um.

**Pavel Frolov**   41:07  
Oh, probably.  
Mm.  
I'm not sure that it it's enable third party access. Probably I can share just by sources.

**Nathan Carver**   41:27  
OK.  
You.  
OK, yeah, I'm worried about getting logged in later.

**Pavel Frolov**   41:46  
But this just provides a general relationship between components I think, but nothing deeper.

**Nathan Carver**   42:02  
OK.  
OK, I'll get that into Mermaid after this.

**Pavel Frolov**   42:23  
Mm-hmm.

**Nathan Carver**   42:24  
Sounds good. Um, OK for the.  
For the next part, then let's look at.  
With my notes, OK.  
We need this.  
OK, um, just for my notes here, so.  
OK.  
So I'm gonna diagram this out so we have.  
The services we have is.  
We have an income service out here.  
Is that correct? Just INCOMN?  
The printer and POS.  
Um.

**Pavel Frolov**   44:33  
I I think I I think you need to add motor goose device that is master for printer.

**Nathan Carver**   44:33  
So for these.  
OK.  
OK, that was.

**Pavel Frolov**   44:43  
It operates printer.

**Nathan Carver**   44:46  
OK, so that is a single device for the location, right?

**Pavel Frolov**   44:50  
Yes, and several yellow boards. Each board installed on each machine. Doesn't matter our machine or competitor machine.  
Hey.

**Nathan Carver**   45:02  
They have a board. Yeah, they have their own internal board, correct, for communicating with Mother Goose.

**Pavel Frolov**   45:06  
Yes, exactly.

**Nathan Carver**   45:08  
OK.  
OK, so these are all going like this.

**Pavel Frolov**   45:15  
No, no, no, no, no, no, no, no. Uh, yeah, yeah, correct. But actually we can specify something like this.  
Oh.  
Like a proxy between.  
You can name it.  
Yeah.  
Yeah.

**Nathan Carver**   45:46  
Oh, I see.  
So each one of these machines will have that.

**Pavel Frolov**   46:00  
It.

**Nathan Carver**   46:12  
OK, so each one of these has the the yellow board.

**Pavel Frolov**   46:13  
Yes.  
Yes.

**Nathan Carver**   46:19  
OK.  
Now is that um the yellow board?  
Is that a JVL product? That's not.

**Pavel Frolov**   46:28  
No, no, it it made by the same con companies that produces terminals.

**Nathan Carver**   46:28  
Yep.  
OK.

**Pavel Frolov**   46:39  
The terminal do not have any displays, just buttons to to print report and it automatically prints print receipt in case when one of the machine cashes out.

**Nathan Carver**   46:58  
OK.  
And this is uh.  
OK, so Mother Goose sends. So when a machine caches out that it's gonna that's gonna travel to the Mother Goose which is going to send this.  
A print job direct to the printer.

**Pavel Frolov**   47:25  
Yes, yes.

**Nathan Carver**   47:30  
Alright, so that sends a print job and then our user.  
Is going to um.  
Basically, this is where the manual step comes in.  
Yeah.  
All right. And then the the digital is back here.  
Get all these minds.  
So this transaction, this is the uh to generate the  
So all of this is in place, so there's really not much for us to do here to get a print other than hook up the machines as they are now and play a game and and print out the winnings.  
So the new pieces for this September 1 is all going to be in this.  
Flex POS in Pomserve.  
And physical gift card.  
So the user what do we need? We need the cashier.  
OK.

**Val Levitan**   49:21  
Are you discussing? Are you discussing personas of who's going to be involved in this?

**Nathan Carver**   49:21  
So then.  
No, I'm just talking about like the the new things that we really want to focus in on testing as far as generating winnings and printing receipts, that's all, that's all stays this as is, right, how it's working in the.  
In the field now, so the new things we want to test is just the Flex POS and the communication to Incom server.

**Val Levitan**   49:45  
Alright.

**Nathan Carver**   49:54  
or September 1\.

**Val Levitan**   49:54  
Exactly, exactly. And that's why I feel that this is the easiest, the most effective thing to start with. Really, there is not much to test. There's not much interruption to the business. We can start testing it immediately. There's full compliance.  
Uh, legislatively.  
Exactly.

**Nathan Carver**   50:19  
OK, so then.  
So this is our MVP.  
OK. So and I think you had your steps in that.  
Look here.  
Alright, so let's create the.  
Cashier Maine enters the ticket value.  
Now is is it just the value that they're going to enter? There's no other record?

**Val Levitan**   51:22  
OK, that's that's that's a good question. We we need to get to the bottom of it. What needs to be entered? I I suggest that all critical fields will have to be entered.  
But we should probably speak to income about it.

**Nathan Carver**   51:38  
OK.

**Val Levitan**   51:44  
And and to a few masters.  
Just to understand what audit trail are they looking for.

**Nathan Carver**   51:55  
OK.  
OK, other ticket.

**Val Levitan**   52:05  
When you talk about personas that's involved in this business schema, it would be a player, a cashier, a location owner, a master.

**Pavel Frolov**   52:09  
See.

**Nathan Carver**   52:11  
Mhm.

**Val Levitan**   52:19  
And income.  
And the JVL technician.

**Nathan Carver**   52:25  
OK.

**Val Levitan**   52:35  
By the way, all of the personas are described in GitHub under knowledge base. We have personas.

**Nathan Carver**   52:43  
Oh, OK, GitHub knowledge based personas. OK, so in this it's he said it's the players, the cashier, location owner.  
JVL Technician.

**Val Levitan**   52:58  
And the master master license holder. In other words, the it's an operator who buys machines and places those machines in locations.

**Nathan Carver**   52:59  
Yeah.  
OK.  
And so the five player, cashier, location owner, JVL technician, master license holder, OK.

**Val Levitan**   53:27  
And income.

**Nathan Carver**   53:29  
In income.  
All right, so.  
To communicate with income, we're definitely gonna need the dollar value in the ticket, but we need to. We need to learn what other.

**Val Levitan**   53:41  
May, may, may. Sorry for interruption. Maybe I missed one persona. It could be GLC Georgia Lottery Corporation.

**Nathan Carver**   53:55  
OK.

**Val Levitan**   53:56  
Mhm.

**Nathan Carver**   54:12  
Corporation.

**Val Levitan**   54:13  
GLC Georgia Lottery Corporation.  
It's a it's a Crown Corporation.

**Nathan Carver**   54:21  
OK.  
All right, so we will need to confirm with Incomm then what other metadata do we need to attach to this?  
Um, from the ticket.

**Val Levitan**   54:34  
I doubt very much that income cares, but we need to verify with master, with a with a few masters and with GLC Georgia Lottery Corporation.

**Nathan Carver**   54:49  
OK.

**Val Levitan**   54:51  
I actually doubt very much that GLC needs anything because they have their SAS port, which they get all the information. They really don't care about the ticket. It's probably master the location owner.  
And uh.  
Yeah, how do they reconcile their book event? I would start with interviewing a master.  
And Felipe could facilitate that exercise.

**Nathan Carver**   55:26  
OK.

**Val Levitan**   55:27  
When speaking to a master, I would keep our business plans private. I would not tell them about the POS and the schema of how we would like to introduce it.  
I would like it to be a surprise to the market.

**Nathan Carver**   55:49  
OK, so we need to schedule that conversation and the use of Felipe can help get that.

**Val Levitan**   55:54  
I am gonna. I'm gonna schedule it right now.

**Nathan Carver**   55:58  
OK, perfect.  
So do we know what income, what income needs from us from this on this for this transaction?

**Pavel Frolov**   56:11  
Yes, yes.

**Nathan Carver**   56:18  
Do we wanna jot? Do you have that in your um docs? I can paste it in or we can just jot down the notes?

**Pavel Frolov**   56:26  
One second. I'll take a look.  
So this is a field that we provide to income.

**Nathan Carver**   57:59  
Yes.  
OK, sorry.

**Pavel Frolov**   58:03  
During login and during uh issue in the card.

**Nathan Carver**   58:12  
OK.

**Pavel Frolov**   58:12  
So access access ID, retailer ID and store ID relates to particular location, terminal ID also for location but could be some.  
Some different devices who initiate Cartesians, but highly likely for first fields are used for general location.  
Code and UPC relates to card data.  
Client ID and client secret relates to Uh credential to access Uh Incom service.

**Nathan Carver**   59:02  
OK.  
OK. So this is the, this is the API call that we're making.

**Pavel Frolov**   59:18  
I I would say is that terminal ID will be ID of our Flex POS device.

**Nathan Carver**   59:18  
Good.

**Pavel Frolov**   59:27  
Will somehow.  
Get from Flex POS serial number.

**Nathan Carver**   59:37  
OK.  
OK, so we we generate this data.  
So for them to issue the.  
OK, so code UPC. So this initiates a financial transaction or is?  
Like.  
Do we send them the dollar amount that we need to process?

**Pavel Frolov**   1:00:10  
Yes, yes.

**Nathan Carver**   1:01:51  
OK.

**Pavel Frolov**   1:01:54  
Seems that location name also in assigned by income during agreement between location and income.  
OK.

**Nathan Carver**   1:02:42  
OK.  
OK, so the cashier manually enters a ticket, the dollar value, the other metadata.  
Then um.  
After they enter that information.

**Pavel Frolov**   1:03:18  
Yes.

**Nathan Carver**   1:03:21  
Do so they're going to swipe a gift card at some point. Does the communication to income happen before or after? Like is it they enter in the ticket information and then they submit this?  
Um.  
Request to income.

**Pavel Frolov**   1:03:40  
Uh, yes, at this moment. Uh.  
Actually we just need 3 requests to income, one to authenticate our terminal.  
With credentials then to call pre-authorize card, particular card. Here we already say the amount we want to pre pre-authorize.

**Nathan Carver**   1:03:58  
OK.

**Pavel Frolov**   1:04:12  
They respond OK if everything suits, limits is OK and so on and last one just issue a card.  
Issue I mean authorized probably command and don't remember right now and after this this card able to to be given for the player.

**Nathan Carver**   1:04:37  
Right.  
OK, so to pre-auth a gift card and authorize a gift card, the card would actually have to be scanned so that income has that card identification right here. OK.

**Pavel Frolov**   1:04:55  
Skip.  
Yes.

**Nathan Carver**   1:05:03  
So do we want the player to swipe the gift card after they enter the ticket so that we put that?  
We capture that data in POS.  
And then the system.  
So they enter the ticket, they swipe, and maybe that just kicks off the system's authentication, preauth and then final auth.  
So the dollar amount is sent to income right in this.  
So this is the.  
This payload here, this is the authentication with income, correct the first call.

**Pavel Frolov**   1:05:57  
No, no, no. This is a mixed value for authentication. We just need two last fields.

**Nathan Carver**   1:06:06  
OK. So there's three endpoints that we're calling now are three, there's three service calls. The first one is the auth.

**Pavel Frolov**   1:06:08  
But.  
Yeah.  
Yes.

**Nathan Carver**   1:06:16  
Um, which I'm assuming.  
All the subsequent whatever they're using. I don't know if they're using tokens or if they're using some type of.  
Um, I don't know what their auth mechanism is once we've once we've authenticated.

**Pavel Frolov**   1:06:32  
Yeah.

**Nathan Carver**   1:06:41  
OK, so it's gonna be limited though, so that auth will expire relatively quickly. Ideally after we've preauth and authorized the gift card that that authorization expires and we have to reauthenticate on the next call.

**Pavel Frolov**   1:07:01  
What was the name?

**Nathan Carver**   1:07:01  
OK.  
See. So.  
Um.  
I mean.  
Probably just a token that's gonna expire.  
And to like quickly.  
OK.  
And so to preauth we we're gonna send the dollar amount.  
The first call's to auth. The second call, we're gonna send the dollar amount with the card related data.  
And then that the last call would be to authorize that card to be used.  
Um.  
Do we know why they have the two calls pretty often off like?

**Pavel Frolov**   1:08:29  
After first request, I think they check.  
Cart. First of all, cart data. Is it suitable for this location? Probably a limitation.

**Nathan Carver**   1:08:35  
Mhm.

**Pavel Frolov**   1:08:46  
Because card has a minimum limit, maximum limit. If you set value higher or lower this limits then it it will be.

**Nathan Carver**   1:08:50  
OK.

**Pavel Frolov**   1:09:02  
Return the error.

**Nathan Carver**   1:09:08  
OK, so there's there's parameters that they're checking in the pre-auth to verify that. So if we don't call.

**Pavel Frolov**   1:09:13  
Yes.

**Nathan Carver**   1:09:17  
If we don't call these in order, if we try to authorize a gift card that hasn't been pre-authed, then ideally that college should fail as well, right?

**Pavel Frolov**   1:09:28  
Definitely.

**Nathan Carver**   1:09:29  
OK.  
Alright.  
So for September 1\.  
Let's see.  
OK, so this is our these three calls will be our handshake with income. Then how do we verify?  
Um, the next thing we have to do is ensure that the processing fee.  
Has been deducted.  
Now would that be we could, how do we verify that is can we look at the dollar amount on the card?  
Or will income give us um?  
I guess how is that deducted? Because income is just assigning a dollar amount to a card. Then do we take $2.00 off that card with flex POS?

**Pavel Frolov**   1:10:36  
When the cashier enters number on the ticket.  
For example $30 then the player will get the card only with $28.00 and $2.00 will be taken from as a service fee.

**Nathan Carver**   1:10:59  
OK, so to verify that the $2.00 was taken, that would just be us requesting the dollar amount we request from income is going to be the winnings minus $2.00.  
In this case, it's gonna be.  
Yeah, the $28.00 plus.  
So we're only gonna request the $28.00 from income to be added to the card. Does that $2.00 then? Does that go anywhere else? Is it?  
Is there anything else for Flex POS to do with that? OK.

**Pavel Frolov**   1:12:09  
No, no, no, no.

**Nathan Carver**   1:12:17  
Does that service fee, does that stay with um?  
The location, does it stay with JVL? Does it? Is it in con? Like where does that mean?  
Where does that go?

**Pavel Frolov**   1:12:37  
Sorry Nathan, what if?

**Nathan Carver**   1:12:39  
Where does who gets the service fee? I guess like because we're deducting that from the total ticket, right?

**Val Levitan**   1:12:46  
Income. Income.

**Pavel Frolov**   1:12:47  
Uh.

**Nathan Carver**   1:12:48  
OK.  
OK.  
Is there anything that we have to send in common other than just the adjusted total value?  
For the service or are they just going to do it when we every time we do an authorized gift card they?

**Pavel Frolov**   1:13:05  
Hmm.  
No, no, no.

**Nathan Carver**   1:13:19  
Income will just automatically deduct that.

**Pavel Frolov**   1:13:19  
We we just we just take $2.00 on each transaction to income and that's all.  
Actually JVL will will pay this money to to income.  
But all the values on the cards will be moved to the card to the player.  
So this two $2.00 is up to agreement between JVL and income.

**Nathan Carver**   1:13:59  
OK.

**Pavel Frolov**   1:14:08  
But we need to to provide this information for the player that this $2.00 or probably other amount will be taken from the player as a service fee.

**Nathan Carver**   1:14:22  
Oh, OK.

**Val Levitan**   1:14:22  
It's not. It's it's not. It's JVL will have to pass on all of the money that's placed on the card.  
So let's say there is a $80.00 or $82.00 payout of which $2.00 is a service charge. JVL needs to collect the entire $82.

**Nathan Carver**   1:14:50  
OK, so how does?

**Val Levitan**   1:14:52  
Although although only 8080 was charged was given to the player and the $2.00 was collected from the player for the service. So JVL will hand over $82 to income.  
So that means the master operator.  
And the location.  
Our response We need to swipe their accounts for $82.

**Nathan Carver**   1:15:27  
OK, so we are going to request the full winning amount from income.  
And then deduct $2.00 after.

**Val Levitan**   1:15:36  
No.  
What do you mean from income?

**Nathan Carver**   1:15:44  
OK, so to authorize the gift card.  
We need to authorize it for a certain dollar amount, so in this example.  
$30 The gift card will have $28.00 applied to it because during the sole process is the $2.00 transaction fee.  
Uh, so.

**Val Levitan**   1:16:06  
The so the winning. So the winning in your case is $30.

**Nathan Carver**   1:16:12  
Correct.

**Val Levitan**   1:16:13  
So JVL needs to collect $30 from this transaction. It needs to come to our bank right away or within, let's say one week, whatever that transaction log is.

**Nathan Carver**   1:16:23  
Right.  
OK. And how does JVL collect that from the ticket?

**Val Levitan**   1:16:36  
From from the location.  
Whoever JVL signs the contract with, I I'm not sure if we're gonna sign the contract with the location or with master, but somebody whoever is our contractual arrangement with.

**Nathan Carver**   1:16:45  
OK.

**Val Levitan**   1:16:55  
We collect the $30 from them.

**Nathan Carver**   1:16:59  
OK, so somewhere in this process we need to log that we need to be able to identify.  
How much we collect from that location 'cause that is not an automatic.  
Is that automatic from Flex POS?

**Val Levitan**   1:17:13  
We we we collect the ticket value, the entire ticket value.

**Nathan Carver**   1:17:20  
Correct. When do we do that? Is that automatic during this automated process or is that going to be like at the end of the week we get a total number of tickets paid out and we collect that amount?

**Val Levitan**   1:17:35  
I I am pushing to do it once a day.  
Whether I will succeed, whether I will succeed or not, I don't know, but it could be, let's say 72 hours, it could be.

**Nathan Carver**   1:17:41  
OK.

**Val Levitan**   1:17:50  
One week, but something within a reasonable time. Imagine.  
That we have 6000 locations.  
How much money we have to front. It's a it's it's a lot of money. It's it's in 10s of millions of dollars that we have to transact.

**Nathan Carver**   1:18:12  
OK.

**Val Levitan**   1:18:14  
So the system has to be automated. We we have to have an ACH.  
ACH stands for Automated Clearing House.  
With each of the accounts, our accounts. So when we say OK, you can have our POS, it means that you gave us your bank information.  
We establish the ACH with you, the automated clearinghouse parameters, and we once a day swipe your account.

**Nathan Carver**   1:18:56  
OK.

**Val Levitan**   1:18:56  
And we give you the reporting accordingly.  
But so one of the one of the MV PS is the real time record, real time record that has to be an MVP.

**Nathan Carver**   1:19:01  
OK.  
OK, perfect.  
OK, so this is gonna happen. Let's say this is happening hourly.  
Or after so many hours we are going to automatically JVL will collect the the the money from the location. So that has to be somewhere in some type of.  
Register right that these tickets were collected and the money is or these tickets were paid out. Money is to be collected still.

**Val Levitan**   1:20:16  
Correct.

**Nathan Carver**   1:20:19  
OK.  
Now is that done right now is.  
How do they do that now? Because everything's just a manual receipt, correct?  
Or do we not? JVL's not doing that now as it is.

**Val Levitan**   1:20:33  
Well, JP is not doing it, but a location does it. So in theory, a location has a paper ticket and they have a key to a machine on a daily basis. They access the machine with the hard key.  
They take an audit meter reading on the screen and they collect cash, so they remove physical cash from the machine.  
Just like any other cash on at at a gas station or a variety store, they take this cash to the bank.  
And it has to be reconciled with the ticket that they.  
You know from from with the goose.  
So they have to do their daily reconciliation. I don't know how they do the daily reconciliation. I don't care.

**Nathan Carver**   1:21:30  
OK.

**Val Levitan**   1:21:32  
And and each each private individual will have his own daily reconciliation because they have different cage operators. So I don't know whether they do shifts like in grocery stores.

**Nathan Carver**   1:21:33  
OK, so we're.

**Pavel Frolov**   1:21:46  
Yeah.

**Val Levitan**   1:21:48  
Which I would do if I if I was them, I would give them a float and then I would take this float back and I would reconcile all the debits and credits.  
I mean the the same goes for a variety store products. You need to count shelves and whatever shortages exist, you need to be able to identify them in almost real time.

**Nathan Carver**   1:22:08  
Mhm.

**Val Levitan**   1:22:17  
So do they do it by shift? Do they do it daily? Weekly? The further away do they do it, the more error, the more, the more gap they have.

**Nathan Carver**   1:22:29  
OK.

**Val Levitan**   1:22:29  
So I don't want to get into it. It's none of my business. I want to get in into collecting my money automatically without waiting and I need to be able to shut down the server, sorry the POS.

**Nathan Carver**   1:22:31  
Yeah, yeah.

**Val Levitan**   1:22:44  
If I did not collect my money immediately.

**Nathan Carver**   1:22:48  
Got it.  
OK.

**Val Levitan**   1:22:53  
So we we call this lease feature.  
So lease on the POS must be an MVP.

**Nathan Carver**   1:22:59  
OK.  
Good, perfect.

**Val Levitan**   1:23:19  
The the lease feature, if not renewed, it has a kill switch.

**Nathan Carver**   1:23:37  
OK, so we need to be able to issue the gift card, collect the winnings. Um.  
But these are the same.

**Val Levitan**   1:23:58  
There are certain features that we already have. Passport RIS stands for Remote Initial Setup.

**Nathan Carver**   1:24:08  
OK.

**Val Levitan**   1:24:08  
It's just the terminology that you should be familiar with.

**Nathan Carver**   1:24:15  
Passport, you said.

**Val Levitan**   1:24:17  
I put everything into, uh, chat.

**Nathan Carver**   1:24:20  
Oh, OK, perfect.

**Val Levitan**   1:24:21  
So if you reach out then I I'm documenting the MVPS just to make it easier on you.

**Nathan Carver**   1:24:29  
Perfect. Alright, so I guess what I need to figure out and we we can talk through then is.

**Pavel Frolov**   1:24:33  
E.

**Nathan Carver**   1:24:35  
We need a record of. We need to store a record of all the obviously all the transactions and for two reasons, just for audit purposes, but we need to know how when we collect the winnings, we need to.  
How do we know how much money to collect?  
So every time the cashier enters a ticket.  
We're going to keep a register of all those entered tickets and then we'll keep a register an accounting of which tickets we've collected for.  
And then we should have the checks and balances at the end, right? We should be able to balance out at the end of the day, total collected, the gift cards issued and then the remaining service fee.  
Oh.

**Pavel Frolov**   1:25:32  
Mhm.

**Nathan Carver**   1:25:34  
All right, so then there needs to be some log right of.  
J register.  
OK, so we're going to, they're gonna enter the ticket, we're gonna enter this into our register. So the next question is where does that get stored?  
Um.  
Um.  
So will will the flex PLS will it? It's gonna have its own storage, some storage capacity.

**Pavel Frolov**   1:26:53  
Yes, yes.  
Yes, yes, it relates to set up mode if you remember in the beginning of meeting.

**Nathan Carver**   1:27:04  
Yeah, OK.

**Pavel Frolov**   1:27:08  
So in setup mode it will provide some reporting. I think all the issued card values will be stored there.  
Optionally all this data will go to the to our cloud server and we can get all this data from cloud server.

**Nathan Carver**   1:27:33  
OK, so that's.

**Pavel Frolov**   1:27:48  
The same server server as probably you remember I need to transfer remote initial setup for the POS and leases for POS.

**Nathan Carver**   1:28:05  
Yeah, OK, that makes sense.

**Val Levitan**   1:28:10  
OK.

**Nathan Carver**   1:28:15  
This is going to do uh, remote setup.  
And lease.

**Pavel Frolov**   1:28:20  
Reporting, releases and reporting, yeah.  
Yes.

**Nathan Carver**   1:28:31  
OK.  
So should the flex POS then?  
Should the would it? Would it make sense for this cloud service to be the intermediate between Flex, POS and Incom?

**Pavel Frolov**   1:28:58  
I don't think so.

**Nathan Carver**   1:29:07  
OK, so we want to.  
OK, so catch your entries to ticket. We register the ticket and value with JVL Cloud.  
So the first thing we do is we update our cloud with a new ticket has just been entered into the system and here's the metadata and value.  
Um.

**Pavel Frolov**   1:29:42  
Actually, I think you do not need immediately to transfer some data to cloud. Probably we need just synchronize several times.

**Val Levitan**   1:29:55  
No, no, no, no, no. They will. They will kill our POS.  
If we do it once a day, at the end of the day we're going to have.  
15% of damaged POS.

**Pavel Frolov**   1:30:12  
I haven't said that it need to be once a day.  
It could be once 15 minutes.

**Val Levitan**   1:30:20  
You.  
I prefer to do it before the transaction is validated.

**Nathan Carver**   1:30:30  
I think my thinking is we want to register that this ticket has been entered into the system and it's identified. The initial record will identify it as being entered when they swipe the card.  
We immediately associate that card swipe with the newly registered ticket in JBL Cloud.  
Then we proceed with authenticating with Incom. That way JVL has a record.  
Before the income process even starts. Um.  
Then idea. So what I'm thinking is for an audit trail then and JVL has an audit trail. This ticket was a was initially entered. This is the initial card that was assigned.  
Then we went into Incom and every response we get back from Incom, we wanna log back to the cloud service.  
Um.  
That way, if any point in time this this whole transaction cycle is broken for, you know, whatever failure mode when the Internet goes down or at least on the JBL side, we have a log that's not just isolated to that.  
POS device.  
So in my thinking it would be.  
We're gonna register the ticket. We're gonna swipe the card. We're going to, uh, register.  
Hard with ticket.  
On JBL cloud.  
Uh, or we do. I mean we could do them both together if if we don't think an extra call is needed.  
Is that thinking? Is that line of thinking making sense?

**Pavel Frolov**   1:32:42  
Yeah.

**Nathan Carver**   1:32:44  
OK.  
So we register either 2 steps or one step, but we register the ticket, we register the card, then we authenticate with Incom.  
We request the pre-authorization of the gift card.  
And they authorized the gift card.  
So when income authorizes the gift card, then does that?  
Is that the Um?  
I guess in the in the background, right, there's financial transactions happening is is that money then that authorizations financially says OK, this gift card.  
Now has the $28. Um.  
Assigned to it or.  
Does Incom say yes, the card is authorized and then JBL puts the $28.00 onto the gift card?

**Val Levitan**   1:33:56  
No.  
It's specifically a function of.  
Income.  
Income. Income has exclusivity on.

**Pavel Frolov**   1:34:11  
Yes.

**Val Levitan**   1:34:12  
Crediting.  
The prepaid MasterCard, we we don't have that operational capability.

**Nathan Carver**   1:34:27  
OK, so income will credit the gift card.  
The dollar amount minus the service fee.

**Val Levitan**   1:34:41  
Yes, correct.

**Nathan Carver**   1:34:42  
OK, but the income doesn't deduct the service fee, we just send them minus $2.00.

**Val Levitan**   1:34:53  
We send them with $2.00.

**Nathan Carver**   1:34:57  
OK, so we sent so.

**Val Levitan**   1:34:59  
So again, again, we we send them exactly what we collected.

**Nathan Carver**   1:35:05  
Which is $30.

**Val Levitan**   1:35:05  
Which is $30.  
Income at that point.  
When we validated the transaction, we say here's we're validating it for $30 income expects and we already have these banking arrangements with them where they swipe our account for $30. They don't even get concerned whether we collect that money or not.

**Nathan Carver**   1:35:34  
OK.  
So when that part is authorized in town, uh deducts.

**Val Levitan**   1:35:44  
Income Income sets out a receivables on their books against JVL's account, and I don't know how often they swipe our account automatically for this $30.

**Nathan Carver**   1:35:54  
OK.

**Val Levitan**   1:36:02  
Well, cumulatively for, you know, all of the money.  
So we better have the money there on the account.

**Pavel Frolov**   1:36:13  
Very likely they will charge us each day. That's why we need each day to to charge all the locations.

**Nathan Carver**   1:36:23  
OK, makes sense.

**Val Levitan**   1:36:23  
Correct.  
Glass have a float. We need a large float of money.  
So at that point, income.  
Sets out a payable for $28.00 to MasterCard.

**Nathan Carver**   1:36:48  
OK.

**Val Levitan**   1:36:50  
And set out a receivables for $30 against JVL.

**Nathan Carver**   1:36:56  
OK, that's what the authorization is doing.

**Val Levitan**   1:37:00  
Right.

**Nathan Carver**   1:37:17  
OK.  
Basically, they're validating their incomes. They have a lot of things they're gonna probably validate there, but we don't have to necessarily worry about that, I guess.

**Pavel Frolov**   1:37:39  
OK.  
OK.  
I.  
Yes.  
E.

**Nathan Carver**   1:38:05  
Actually, we want to register.  
Um.  
OK.  
OK, so let's walk through this. So the cashier, the player brings up the $30 winning ticket. The cashier enters that ticket dollar amount and other metadata to be determined.  
The next the POS will register.  
PLS registers the ticket metadata and value with JVL cloud service.  
The cashier will then swipe a gift card. The PLS will register the card.  
With that ticket on the JVL cloud.  
Then the PLS will authenticate with income.  
And.  
Just for logging purposes, we want to log that communication with income. PLS requests a pre-auth of the gift card.  
It's gonna send the total collected amount in that authorization.  
And gift card and card data.

**Pavel Frolov**   1:40:13  
No, no, no. Here we will send $28.00 to reauthorize card.

**Nathan Carver**   1:40:23  
Oh, OK.  
So when do we send the full amount to income?

**Pavel Frolov**   1:40:32  
It's outside of the schematic. It's a manual process.

**Nathan Carver**   1:40:40  
Oh, OK, so it's not in this.  
So a manual process.

**Pavel Frolov**   1:40:46  
It's a financial transactions outside of this schema.

**Nathan Carver**   1:40:54  
OK, so this.  
8\.  
So when we preauthorize the gift card, we're sending income the total.

**Pavel Frolov**   1:41:03  
Sure.

**Nathan Carver**   1:41:06  
Um.  
The total amounts.  
Minus $2.00 service fee.  
So we're asking NCALM to pre-authorize $28.00 on the gift card.  
OK, we're gonna log that, OK?

**Pavel Frolov**   1:41:34  
Yes.

**Nathan Carver**   1:41:43  
Um, I guess.  
Here uh should is there any other data there store?  
And if we all problem.  
OK. And then we're gonna authorize the card.

**Pavel Frolov**   1:42:14  
Actually income swipes GVL account for full $30 also outside of our of this schematic.  
It's a separate process.

**Nathan Carver**   1:42:28  
OK, yeah, it's not. It's not necessarily like.

**Pavel Frolov**   1:42:28  
And it's it's done, it's done not immediately, but highly likely once a day for entire transactions.

**Nathan Carver**   1:42:38  
OK.

**Pavel Frolov**   1:42:44  
Yes.

**Nathan Carver**   1:42:44  
OK, so this will be a batch process. So, so Incom knows that if we requested a $28.00 gift card that at some point in time they're gonna swipe $28.00 \+ 2\.

**Pavel Frolov**   1:42:45  
Yeah.  
8\.

**Nathan Carver**   1:42:58  
As the service fee.

**Val Levitan**   1:42:59  
No, no, no, no. We are not asking income anything. I believe this is a confusion.

**Pavel Frolov**   1:43:00  
Yes.

**Val Levitan**   1:43:12  
We're not asking anything. We are sending to income a win of $30.  
That's it. That's the only thing that we're sending.

**Pavel Frolov**   1:43:23  
Well, no, no. We using the API we saying that we are authorizing.  
Uh, Vinion \-2 dollars. That's all.

**Val Levitan**   1:43:41  
The the two the $2.00 is.  
Kind of given we we don't even need to authorize the the $2.00.

**Pavel Frolov**   1:43:52  
Yes.

**Val Levitan**   1:43:53  
Which?

**Nathan Carver**   1:43:53  
Yes.

**Val Levitan**   1:43:54  
Yes, what? Yes, we do or yes, we don't.

**Pavel Frolov**   1:44:01  
We do not say anything about $2.00 for transaction, yes.

**Val Levitan**   1:44:04  
That's my point. That's my point. So the only thing we're telling income is that a win is $30. That's it.

**Pavel Frolov**   1:44:12  
No, no. We just say to incomes that the card we assume in the card winning minus $2.00.

**Val Levitan**   1:44:26  
OK, but.  
We're actually saying \-2 dollars.

**Pavel Frolov**   1:44:33  
Yes.

**Val Levitan**   1:44:36  
OK.

**Nathan Carver**   1:44:39  
So the in comma APIs is basically requesting in the API call. We have to tell the API this is how much we want to authorize for the card. So that's why we send it the 28 rather than the full 30\.

**Val Levitan**   1:44:56  
No, but we we're we're sending 30 because the.

**Pavel Frolov**   1:45:01  
During this automatic operation we send in 28, but at the end of day they will calculate all the activated cards, adding $2.00 to each card and provides the full amount.  
Mount to JVL.  
To charge.

**Nathan Carver**   1:45:27  
OK, so JBL will. That's why JBL collects the $30 because.  
Income will collect.  
The $28.00 for the gift card that was applied to the gift card, and then they will add $2.00 as a fee for that gift card, so they'll collect a total of 30\.  
So if we sent them full $30.00 then they would collect $32 from us because they're applying the fee when they collect the money.

**Pavel Frolov**   1:46:02  
Yeah.

**Nathan Carver**   1:46:02  
That makes sense.  
OK, so batch cross income swipes.  
This will be a batch.  
Or the 28 plus.  
New dollar service B.

**Pavel Frolov**   1:46:26  
Actually at this point they can charge not $2.00 but less than according to agreement between between JVL to share the service fee.

**Nathan Carver**   1:46:40  
Oh, OK, so there's some.  
OK, so there's some service fee that's less than $2.00.  
So then JBL and Incom are sharing that, OK.  
OK, register.  
OK.  
OK, does that make sense? This workflow?  
I think I'm still going to want to diagram this out, but.  
OK. So I I think one thing that will be important is talking about how we're collecting.  
What's the process for? There's a batch process that's going to be initiated and JBL is going to go take all the receivables.

**Pavel Frolov**   1:48:57  
Yeah, here on this, on this schematic, I think we need to add outside of Flex POS workflow. It will be workflow between income and JVL to.

**Nathan Carver**   1:49:02  
OK.

**Pavel Frolov**   1:49:13  
To process financial transactions and the same between JVL and location process accounts and data.  
Down some transactions.

**Val Levitan**   1:49:29  
And and reporting.

**Pavel Frolov**   1:49:33  
Yes.

**Nathan Carver**   1:49:37  
OK. So then in that way if we have the ability to, if we register a ticket and we register.  
There's a redemption record out there that was started but never finished. Then we can also audit.  
These things, because the final step here is between authorizing the card and recording that we need to deduct that money from the.  
From the location, we want a way to ensure that this is um.  
That there's no system failure between.  
Uh, income.  
Recording that they're going to deduct the money from JVL and then JVL recording that they need to deduct the money from the customer.  
I don't know if we need to go into this, but for this MVP we don't necessarily need to go into all those failure modes, I think.  
This might cover the MVP, right?

**Pavel Frolov**   1:50:57  
I see. Yeah.

**Nathan Carver**   1:51:00  
Um.  
Collect real time winnings. Well, I guess Val, this will be the batch process then, right? That we can run this process and and and be able to collect everything that's been recorded during the test.  
Um.  
And then we need to be able to shut down that, OK.

**Pavel Frolov**   1:51:23  
It.

**Nathan Carver**   1:51:33  
OK, so for next steps, um.  
Pavel, what would it be helpful for me to do for you? Do you want? I can do more just.  
For me, I would like diagram this workflow out. It just helps me think through it. Um, so I can do that.

**Pavel Frolov**   1:51:55  
Oh.

**Nathan Carver**   1:51:55  
And I'll also go through your schematics that you shared to make sure I understand how the technical side is evolving.

**Pavel Frolov**   1:52:04  
I think at this moment we already can understand what features we need to implement these capabilities.  
And probably next week we will be able to to create the features in Jira at least those.  
Not uh, not implemented for flex play.  
Need to focus and describe in more details.

**Nathan Carver**   1:52:39  
OK.

**Pavel Frolov**   1:52:40  
For example, I see right now quite urgent work to be done to communicate between Flex POS to GVL Cloud.  
Uh, to uh, make reports.  
Or on the flight.  
During the pre-authorized procedure and finalize transaction. If the card already issued then we need to make this records on the cloud server well and then.  
When we have all the records on the cloud server, I think we need to to create a cube to make reports.

**Nathan Carver**   1:53:33  
Mhm.

**Val Levitan**   1:53:35  
Not only that, we need to immediately integrate with Business Central. It has to be a posting because if we don't have the posting, we cannot reconcile with the bank.  
It becomes a a a crazy accounting chore. If if we don't automate the cycle, it will be. I'll have to have 10 people in accounting department.

**Nathan Carver**   1:54:02  
Yeah, OK.  
So I know we've been focused on requirements for Flex POS. Do we want to get into the requirements of the cloud side as well and the reporting and the and the batch processing?

**Val Levitan**   1:54:19  
We do, but not in today's meeting.

**Pavel Frolov**   1:54:20  
Mm.

**Nathan Carver**   1:54:22  
Correct.  
OK.

**Pavel Frolov**   1:54:28  
I think this is most difficult part could be to to make this part on server and posting to central.  
You have never discussed this previously.

**Nathan Carver**   1:54:53  
Um, didn't discuss which one the.

**Pavel Frolov**   1:54:58  
Uh, cloud cloud implementation.

**Nathan Carver**   1:55:00  
Be part of this, yeah.

**Pavel Frolov**   1:55:02  
Yeah.  
We have right now lease, we have right now a remote setup, but a reporting you need to to be.  
Uh, developed.

**Nathan Carver**   1:55:27  
OK.

**Pavel Frolov**   1:55:28  
Get immediate records and to have communication to central.

**Nathan Carver**   1:55:47  
OK.  
All right, so for next steps then.  
For the product side, I'm gonna go through and my goal will be to mature what we talked about a little bit, think through it and try to draw out more requirements I.

**Pavel Frolov**   1:55:57  
Yes.

**Nathan Carver**   1:56:06  
I will. Val Aaron is still meeting with us regularly. I can set up time with.  
For Aaron and I to go through Jira.  
I wanna make sure that I'm getting things in there.  
In a structured way, that'll be useful.

**Val Levitan**   1:56:22  
Yeah, of course.

**Nathan Carver**   1:56:25  
OK, I will do that. And then, yeah, so the plan will be next week problem for us to start putting this into JIRA so the team can.  
Start working towards this.

**Pavel Frolov**   1:56:41  
Yeah.

**Nathan Carver**   1:56:41  
SMVP OK.  
Well, I think that's it. It's 8:00. Well.

**Val Levitan**   1:56:55  
I just want to give you a certain data.

**Nathan Carver**   1:56:56  
Yes.

**Val Levitan**   1:57:03  
Useful data.

**Pavel Frolov**   1:57:03  
It.

**Val Levitan**   1:57:06  
I just put it in ChatGPT. Let me just put it here in the chat.  
These are the things that you probably need to.  
Kee in mind.

**Pavel Frolov**   1:57:35  
T. T.

**Val Levitan**   1:57:48  
Sorry, let me let me put one more thing in here.  
They should have been first.  
So the third is the is the first. The third posting is the first.  
The second is the 2nd and the 3rd and the first should should have been the 3rd. So the point of this is that.  
We know that.  
Machine, on an average, generates approximately $102.00 net win.

**Nathan Carver**   1:58:53  
OK.

**Val Levitan**   1:58:53  
So I'm expecting approximately $92.00 average ticket issued to 10 people.  
Per day, per machine.  
So that's service charge of $2.00. We have to collect approximately $918 per machine.

**Nathan Carver**   2:00:02  
OK, that makes sense.

**Val Levitan**   2:00:13  
OK. When can we have our next meeting?  
We we should get on pace with these meetings, even if it's 30 minutes.

**Nathan Carver**   2:00:26  
Yeah, I think so that's so we have the the sync up tomorrow.

**Pavel Frolov**   2:00:27  
See.

**Nathan Carver**   2:00:34  
Um, think that is that once meeting so.  
I'm available tomorrow to meet if we wanna.  
If we want to meet before us at 6:00 AM.

**Val Levitan**   2:00:51  
So tomorrow meeting is we're going to discuss the mock up screens, right?

**Nathan Carver**   2:00:56  
Yes.

**Pavel Frolov**   2:00:59  
I I don't think that we need to two hours. I I think one hour will be enough and then we can.  
Discuss with Nathan.

**Nathan Carver**   2:01:09  
OK.  
That works for me.

**Val Levitan**   2:01:12  
OK, OK, perfect.

**Nathan Carver**   2:01:19  
All right, very good.

**Val Levitan**   2:01:22  
Thank you very much.

**Pavel Frolov**   2:01:22  
Yeah.

**Nathan Carver**   2:01:22  
Thanks everyone.

**Pavel Frolov**   2:01:25  
Thank you. Bye.

**Nathan Carver**   2:01:26  
Bye.

**Nathan Carver** stopped transcription