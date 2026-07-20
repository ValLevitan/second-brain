**Transcript**

August 22, 2025, 12:03PM

**Juan Martinez** started transcription

**Juan Martinez** 0:03  
So per per our last meeting, we said we had a general overview of the topics on our last call and today we were gonna somewhat focus on the diagrams and architecture just to understand, you know, so Pavel.  
Posted those. Some of those I had seen, some of them I have not, so I don't know who's really had time to dig into any of those just yet.

0:27  
OK.

**Juan Martinez** 0:36  
Would you agree that you guys need some more time to just peruse those?

**Nathan Carver** 0:43  
Yeah, I had a some time just to briefly go through them, each of the PDFs, but I haven't looked at it in detail yet.

**Juan Martinez** 0:55  
So I mean what I'd like to do is is sort of work back into those diagrams. Let me just share my screen here. You know, I just want to in in terms of priority, you know as Val put it, you know our first course of business is to release the point of sale device, the flex PO.

**Nathan Carver** 1:02  
OK.

**Juan Martinez** 1:15  
US plus the dispenser by Q4 of this year, you know, October, November, December, whenever that works out to be. In order to make that happen, the goal is to have the point of sale and dispenser be.  
An automatic out-of-the-box device and I I see how that can be done somewhat easily when the location is already up and running and may have already had the device.  
I'm just trying to wrap my head around a brand new location where the Internet has just been deployed. The networking equipment is coming along with POS and it and it's not there yet. How something like that?  
Could even be done. And Pavel, I think you agree when it's a brand new location, there's nothing to auto configure from. We have to start from scratch. So I think we need to envision how we do that. And I just started throwing some things down here. You know, we got to define our network requirements for each location.  
And the minimum Internet requirements, whether we're going to request the site to install a new Internet connection for us or whether we can piggyback on any.  
Network connection may have. Just gonna put a note here. My my only concern with piggy banking is does income have any concerns where they must have a dedicated Internet connection under any MasterCard rules or regs?

**Pavel Frolov** 3:03  
I think this is not a problem because we are switching our income communication to cloud, so highly likely it will be 100% available.

**Nathan Carver** 3:04  
Mhm.  
Yeah.

**Juan Martinez** 3:15  
OK, OK.

**Will Jones** 3:21  
I would think they must have some type of expectation definition of what encryption level we use to to pass you know the critical information. I'm losing the word for it, but anyways for the information that's going to be about the the card.  
Back and forth in the transaction itself. So I wouldn't, I wouldn't expect it to be just whatever we choose at that level. I would expect it to be at least the bare minimum. I I would hope we would choose something that would be acceptable too.

**Nathan Carver** 3:55  
Simply they have O auth two is there.

**Juan Martinez** 3:56  
Sure. Um.

**Nathan Carver** 4:00  
Protocol that they're that they're using. At least that's, I believe that's what's in the API doc.

**Pavel Frolov** 4:01  
Mm.

**Juan Martinez** 4:08  
Can you repeat that to Nathan? What?

**Nathan Carver** 4:11  
So Incomm just does over HTTPS using a lot 2 for their for their handshake and I did. It's not an established, it's not like a a socket connection or a tunnel.

**Juan Martinez** 4:20  
Um.

**Nathan Carver** 4:29  
To income.

**Juan Martinez** 4:30  
OK.

**Nathan Carver** 4:31  
So from, but as Pavel said, because it's in our in our cloud, there's no network, you know, Internet capability requirement that we don't have to worry about the customer meeting. But even then I think it's still pretty.

**Will Jones** 4:32  
Is.

**Nathan Carver** 4:47  
I think their their system is designed to operate over pretty low bandwidth and unstable connections.

**Pavel Frolov** 4:56  
Yeah, actually as we already implemented the basic communication to income to activate the card and actually they do not insist or probably not insist require so.  
Difficult requirements for us to protect communication. It was enough for for right now. So when we switch to Sierra, I do sure that we definitely comply with the minimal requirements.  
Because it will be more secure than the right now.

**Juan Martinez** 5:37  
OK.  
And Pavel, for our sake, from from the location to our cloud, do we?  
You know, do we have a a minimum speed?  
Oh, I'd hate to use the word dial-up, but can this be basic dial-up or we need a minimum, you know, 200 megabyte speed connection? I'm just throwing that out there completely random. I don't know what we need to follow.

**Will Jones** 6:11  
2.  
So, so Juan, in that respect, I don't know that we didn't, you guys don't have a cloud provider, correct?  
That was the question I asked last week.

**Pavel Frolov** 6:24  
Uh.  
Actually, actually we are using right now some servers in cloud based on Amazon, but according to our admin, probably in some cases we will switch to Azure.

**Will Jones** 6:37  
AWS.  
So what what I'd say Juan is that wherever I don't know where they're hosted, they could have they could have you know multi tenant as well like they could definitely be hosted in different locations. But generally speaking we're just going to create some kind of VPC to their their end point to.

**Juan Martinez** 6:57  
Sure.

**Will Jones** 7:07  
Ensure that we can have communication with them. That's a secure that's basically already has some protection around that and then we're just hitting. It sounds like an HTTPS, probably RESTful service that's going to facilitate the transaction with them.

**Nathan Carver** 7:19  
Yeah.

**Will Jones** 7:23  
So I would think that they're probably gonna issue us a client certificate. Is that not the case, Pavel?

**Pavel Frolov** 7:32  
Actually, we do not know exactly how to proceed, but highly likely it will be enough during the bank activation to generate certificates to for us to to access our server.  
So I see it personal generation for each location for each device probably in order not to to allow different devices to access our network from different location or not authorized.

**Will Jones** 8:02  
But that's.

**Pavel Frolov** 8:12  
Terminal to be able to connect to our server.

**Will Jones** 8:16  
Yeah, I think there's there's quite a few ways that we can do that that you know anyway that that that's separate, right? Because that's the communication from our devices to our cloud entity and then from our cloud entity to theirs is just going to be some kind of either computer secure tunnel or something.  
Nothing else, but we will. We'll definitely do what we need to do to set up the security in that connection so that we don't have any possibility of outside interest attacking us.

**Juan Martinez** 8:51  
Yeah, and and Will, my my question was somewhat targeted to the latency in in responding to a a a Tito request in barcode verification. You know, are there already published standards on what a minimum?

**Will Jones** 8:58  
Um.

**Juan Martinez** 9:08  
Solution of speed or is all modern Internet capable of supporting that? You know, and that's probably the case.

**Will Jones** 9:14  
It's, yeah. When you're talking cloud to cloud communication, they're going to be such high volume tunnels. There's no way that the communication latency is going to be any issue except for you're talking about down at the property up to our cloud service, which absolutely you know that it's it.

**Pavel Frolov** 9:16  
It.  
It.

**Nathan Carver** 9:25  
Mhm.

**Juan Martinez** 9:28  
Yeah.

**Pavel Frolov** 9:30  
Yeah.

**Will Jones** 9:34  
It's more less I would say latency because we're probably talking very small packet sizes and that and probably more just the you know the the how.

**Nathan Carver** 9:41  
Yes.

**Will Jones** 9:46  
Not secure, but excuse me, how much fault tolerance that network has, how much we're dropping all the time, and how much we're having to deal with interruptions that could be in, you know, moments or seconds.

**Pavel Frolov** 10:01  
Yeah, in short, you can answer. Yeah, any modern connection will be enough. But what is enough? We need to understand that as a priority #1 is to support.  
Cart issue communication and priority #2 to share some statistical data and so on.

**Juan Martinez** 10:29  
Yes.  
Agreed.  
OK, that answers that. So #2 here, establish an ACH agreement with each location. And yeah, basically we have to solicit the location and they're signing a contract with JBL.  
For the processing of that service fee and the payment back and forth related to those fees. So I have some banking contracts, so I'm going to take this this one up and for our next meeting I'll I'll have some sort of drafts, but this will have to go through our legal.  
Review process just to make sure we've covered that. But naturally this has to be in place and I just put here as a footnote. We we may use an existing JVL bank account or we may need to create a new one dedicated to.  
These transactions in and out per say.  
Uh huh.  
All right, #3 debit location accounts through ACH within 24 hours in accordance with the agreement. So as you know, once a transaction happens, Intercom is expecting us to pay them.  
And we are expecting the customer to pay us to cover that $2.00 fee. So we we just need to set up an automated process through the defined bank accounts on the JBL side and on the location side.  
To try to automate these debits and credits in a timely fashion. Ideally we wouldn't want to pay income until JVL has been paid, but that may not always happen. So you know Val's aware that you know we probably need to keep some funds in the account.

**Nathan Carver** 12:14  
Yeah.

**Juan Martinez** 12:27  
That we are using to pay income and we will just add money to that account as the customers pay us, hopefully in a timely fashion.

**Pavel Frolov** 12:38  
Hmm.

**Juan Martinez** 12:45  
And #4 present a reconcilable accounting detail to each location and master. This actually was a hot spot during this week at the Georgia show, so a lot of customers had concerns about.  
Us introducing a new device called the Flex Pay Kiosk that takes money. So today they know how to reconcile a EGM. Money goes in and out of it and it's trackable.  
But tomorrow money will go into the kiosk. Money in the E wallet solution and Tito will go into the machine as well. So they were having a hard time envisioning how to reconcile.  
Money that went into the kiosk because it's not a machine versus outstanding Tito ticket balances. So definitely you know we we need to nail down the reporting side because that that is.  
Their expectation and that's certainly a day one requirement, you know. So I I again I threw some things down here, you know like the customer should be able to log on through a cloud based log on.  
Likewise, JVL needs some reconciliation reporting tools so that we know what we're owed and by who. And I I just started here, but I'm we need to break down location reports, what we think they may need.  
And then master reports. You know what? What information would the operator need that may or may not mirror what the location reports are?

**Pavel Frolov** 14:32  
Hello.

**Juan Martinez** 14:33  
Any questions on on these topics, gentlemen?

**Pavel Frolov** 14:40  
Not now.

**Will Jones** 14:43  
Let's see. So Juan, on that, are we going to dive into requirements details about what you were just Speaking of in in a separate conversation or just at this point, like what's that?

**Juan Martinez** 14:55  
I literally cause I I got home last night at 9:00 PM. I literally just started working on this. So you you guys tell me I I think I want to just start before writing the actual requirement. Just more detail and notes.

**Will Jones** 14:58  
Oh.  
Mm-hmm.

**Juan Martinez** 15:10  
And I can distribute that and and I think we just brainstorm as a team if we all have requirement ideas, you know we we prepare and present them in a less official capacity and then maybe combine them into their formal requirements afterwards. What what are your thoughts on that?

**Nathan Carver** 15:30  
So our our flow has been to write use cases and then from the acceptance criteria within those use cases we drive out requirements that's that support that.  
Use case. So I've added the two use cases specifically dealing with location onboarding and payment set up through CMS. This would tie into an existing use case we have on device provisioning.  
And then the second use case I added was for the reporting for the location owner.

**Juan Martinez** 16:12  
Yes.

**Nathan Carver** 16:12  
And so I went through, I churned through ideas on what the location owner might be interested in with my obviously limited industry exposure still, but from the very least took the perspective of.  
Location owner has an account that has money being drawn from it, so everything is kind of reported from a specific account, whether that's one or more locations. So that's how that use case is is structured. But so that gives us a starting point at least to start looking at what requirements would we need.  
To satisfy the use case.

**Will Jones** 16:54  
I was, I was interesting as or interested in asking more questions. I just wanted to park it or not on the actual accounting piece because that I was, I was trying to figure out where's the, you know, where are we talking about the actual assets being stored. I mean obviously I can picture a slot and I understand how that counting piece there works.  
And I we we should definitely bring it up for Nathan's purposes too. But where the where they were comfortable with I was understanding. So then I my next question was going to be about the Tito and and the liability of the the Tito tickets and how that's accounted for today and then you know use that as as.

**Juan Martinez** 17:28  
Yeah.

**Will Jones** 17:33  
The the starting point to then discuss what what additional accounting measures need to be in place for the actual transactions that are going on with income.

**Juan Martinez** 17:44  
Right.

**Will Jones** 17:44  
So because I figure that's what you're looking at. You're looking at three different reconciliations that need to happen, and somehow our system has to be able to report on all three so that they come together.

**Juan Martinez** 17:48  
The correct.

**Pavel Frolov** 17:57  
Actually, the schematic is a little bit simpler because you are not allowed to insert money into a terminal. Yeah, because all the.  
All the money inserted directly to machine and for redeem purpose you just present cheater ticket and you you you're getting a card, so no any reconciliation related to money to.  
A kiosk.

**Nathan Carver** 18:34  
Right.

**Will Jones** 18:35  
But the the card, so the funds are on the actual credit meter, right? That is and one of the instruments that we have. And then from there it's gonna go into an income account, right? And that income account is issuing just a.

**Juan Martinez** 18:42  
Yes.

**Will Jones** 18:51  
A gift card that is the accessor to that in that account where they put the balance into. There is a transition between the two. There's a time when it's not on the credit meter and it's not in the income report, right? Is that when it's a Tito?  
Like what? What? Where is it at that point? Where are we actually verifying and keeping the funds when it's in transition?

**Nathan Carver** 19:14  
So I think as far as flex POS goes in this, I don't think we have any awareness of the where the funds were being like the funds inserted to a machine or any other kiosk because our the flex POS in this burst.  
Iteration doesn't have any ability to track that, so all we know is that a ticket was sent to us from the Mother Goose. So that's our first awareness of any type of value.  
For the customer. So from that point, from that ticket being received, all we can really generate, all we can track at that point is the money that we pay income and the money that we take from from the location owner's account.  
So those are the things we have to reconcile. I think those two transactions to the ticket value that we received.

**Will Jones** 20:11  
So we'd not aren't. We are not actually pulling slot meters.

**Juan Martinez** 20:11  
But.

**Nathan Carver** 20:17  
No, not with this first iteration.

**Pavel Frolov** 20:17  
Yes.

**Juan Martinez** 20:21  
Yeah, so I mean.

**Pavel Frolov** 20:21  
Actually this is one one way communication I I would say and no any additional way how to validate it except for taking data from the one way channel.

**Will Jones** 20:37  
Well, we have to have some kind of acknowledgement in order to make sure we actually have added the funds that there's like there's three conditions. In this case, we have to ensure that when there's a cash out that it's added to the account, right. We have to verify that if there is multiple pulses, let's call it that we don't add.  
Add multiple funds to the account for the exact same one, and that the entity that's actually produced that pulse has to ensure that we've added it to the count or they have to resend, right? So there's absolutely some kind of handshake there, or else it's not fault tolerant. Then we are going to lose funds and we have the.  
Potential of double funds if we don't have the if we don't have the potential to lose funds, right? There has to be some kind of handshake.

**Juan Martinez** 21:23  
So can can we break this down into Pavel? Let's first talk about our e-wallet solution and you know, let's follow the dollar in and out.  
So with e-wallet will we we will install a our version of a player tracking device which is an optical scanner at the machine and a display for the guest to interact with. So in this situation your money.  
Goes to the Flexpay kiosk, the e-wallet kiosk, and you you generate an e-wallet ticket you now have. If it was $20, you now have $20 on that ticket. That's one sort of tracking that we need to do from the kiosk. $20 went into the kiosk.  
Now your e-wallet ticket worth $20 is scanned at machine #1, and you can even add more money directly from your pocket onto that machine and play and play and add more money if you want, and then you're cashing out.  
Back to the original e-wallet ticket. So the money is going back onto which could be greater or lower than the original amount onto that e-wallet ticket and then that e-wallet ticket can go to a second or third machine.

**Will Jones** 22:51  
Mm-hmm.

**Juan Martinez** 22:52  
Repeat the entire process and then now you do end up back at the kiosk to redeem that e-wallet ticket, which then goes on to a MasterCard gift card. However, we offer the ability to do a partial transfer.  
Meaning I can keep if I have $100 on the Tito ticket, I want to keep 50 on the ticket and only transfer 50 to the MasterCard gift card. So to Will's point, there's a ton of tracking there that we need to do.

**Will Jones** 23:21  
Got it.

**Juan Martinez** 23:27  
Because you know the the customer in the event of a dispute Pavel, is all of this transactional history related to that E wallet ticket physically on the kiosk? Do we envision them logging on to?  
A website to look up a ticket. If the player insists, hey, I forgot my pin, where can they go and look up that information? So there's certainly some level of of transactional.  
Access that we need to provide them for validating those steps.

**Pavel Frolov** 24:04  
Hm.

**Will Jones** 24:07  
But in, yeah, in that case I'm saying is that is that only JVL machines or is that any any machine that we're transferring? Do we support going to third party?

**Pavel Frolov** 24:07  
Yeah.

**Juan Martinez** 24:16  
Yes, any machine.

**Pavel Frolov** 24:17  
S.

**Will Jones** 24:17  
OK. So in that the only place that I was trying to point and sorry, and this was not knowing e-wallet or anything in that is that there is some kind of acknowledgment that happens when funds get transferred into a machine and when funds get transferred out. If there wasn't, it couldn't possibly work without losing funds.  
Funds or doubling funds, so, but as long as there's a protocol like SAS, like the like cashless transactions, you know on SAS, that's fine, right?

**Juan Martinez** 24:48  
So no, yeah, but just just so you're clear, Will. So in the e-wallet scenario, we're targeting older machines which do not necessarily have a secondary SAS. Remember, Intralot, the state system is already occupying SAS one.

**Will Jones** 25:06  
Mhm.

**Juan Martinez** 25:07  
So we are interacting with the printer and the bill acceptor. That's why SAS is not aware of the funding. Yes. So we're we're we're mimicking the bill acceptor input pulses.

**Will Jones** 25:12  
OK.  
It looks not dirty, huh?  
So.

**Juan Martinez** 25:22  
And we're mimicking the printer out data capture.

**Will Jones** 25:24  
Would why wouldn't JBL do that? That's so cool. That's great. And I mean, obviously you can you can act like the bill acceptor and then the whole machine just thinks that we got cash entered. I love it. It's a ingenuitive for sure. I've never thought of that one before.

**Juan Martinez** 25:30  
Yeah, yeah. And if the the market is.  
Absolutely.  
Definitely.

**Pavel Frolov** 25:41  
Just some some notes. First of all, we are not mimic as a printer. We still use electromagnetic counter for cash out in this case and the second one just just additional information related to E wallet.

**Juan Martinez** 25:53  
Yes.

**Pavel Frolov** 26:01  
Actually it contains 2 counters, 1 relates relates to playable only amount and the second one redeemable amount because we do not support direct entry money on the ticket and directly.  
Take them to a cart. It's prohibited. You need to pass this money through the machine. You need to win something and return money to redeemable balance of the your wallet.

**Will Jones** 26:25  
Mhm.  
Yeah, so it's so it's a non cashable transfer onto it and then it turns over into cashable funds and cashed out. Yeah, OK, that makes good sense too. So, but yeah, it just back to it, there's there's plenty to account for in this one for sure.

**Pavel Frolov** 26:37  
Yes.

**Will Jones** 26:48  
And especially because there is the e-wallet is a actual bank account, right? That is where we are storing bank account being obviously twisting that word, but it is an account for our money, right? It's a it's where we're putting money in. So I'm absolutely going to need to have some ability to do that.

**Juan Martinez** 27:04  
Yes.

**Will Jones** 27:08  
And reconcile, you know, with all the the, the various are these sites closed at least once per day so that we have a time period where we're guaranteed to come out and be able to have, you know, at least enough information to know what credits are in the credit meter, but pretty much come out with a 0.  
0 balance.

**Juan Martinez** 27:29  
A yes and no Will. A lot of locations. You must have a liquor license. So it's a restaurant. As you know, restaurants close at night for whatever hours they do, but a gas station or 711 may be a 24 operate hour operation. So we have both scenarios.

**Will Jones** 27:38  
Hmm.  
How do we account or reconcile today?

**Juan Martinez** 27:54  
Today we don't have, we are not the host system. So this Intralot or Mother Goose system is in place collecting some basic data. But every machine has a primary SaaS port in the market and Intralot, this third party state level organization is collecting the data.

**Will Jones** 28:08  
Hmm.

**Juan Martinez** 28:14  
And supplying that to Georgia Lottery for reconciliation purposes.

**Will Jones** 28:18  
But so for the E wallet solution, we don't use that currently in Georgia.

**Juan Martinez** 28:24  
We know that the e-wallet is is in in in development right now by us. I mean it functions for us at the basic level of the show that we but it's not yet deployed, no.

**Will Jones** 28:31  
Got it. OK, I didn't. I I thought that that was an existing piece of the puzzle and that only the interaction with income was the next one. So how much of this then is is already?

**Juan Martinez** 28:39  
Oh no, no.  
So.

**Will Jones** 28:48  
You know this flex pay ecosystem, how much of it is actually in in the market today and how much is just what we're talking about developing?

**Juan Martinez** 29:00  
Everything related to the Flex Pay ecosystem is not in the market. It's in more advanced prototype state for show use, but we do want to deploy the Flex POS by October, November, December of this year.

**Will Jones** 29:01  
Right.  
OK.  
Yeah.  
Yeah. OK. Sorry, getting me back, getting me on the same page is what you guys already may know that that way. So thank you.

**Juan Martinez** 29:19  
But it is not in the market.  
No, no. So then we we talked about that was the e-wallet solution meant to target older machines that may or may not have SAS, may or may not have a physical printer. So the alternate solution is the Tito solution.

**Will Jones** 29:34  
OK.

**Juan Martinez** 29:46  
And Will, that that is pretty much the same Tito. You know, JBL is is acting as the Tito host. Money goes directly into the machine. You play, you cash out, you get a Tito ticket. The Tito ticket can be moved from machine to machine.  
At the end of your gaming day, you then go to the Flexpay kiosk to cash out that Tito ticket to the MasterCard gift card. So likewise, we still need some transactional data.  
For hey, my ticket isn't working. You know, I think I have more or less money than the ticket says on the face value. You know, those sorts of reconciliation reports need to be available either on the kiosk.  
Or from a a cloud-based client portal for the location and or master to verify a dispute.

**Will Jones** 30:45  
OK, Yep. In in the the Tito solution, are we only talking SAS is the conduit of the the funds from the terminal to a ticket?

**Juan Martinez** 30:57  
Correct. Right, Pavel, with with Tito, we're using full SAS to interact with the machines, correct?

**Pavel Frolov** 31:05  
Yes.

**Juan Martinez** 31:08  
Yeah.  
So.

**Will Jones** 31:09  
OK, so that's like enhanced validation. Do you already know? Yep.

**Juan Martinez** 31:12  
Secure. Secure enhanced? Yep. And for Nathan's sake. So Nathan, once that Tito goes into the machine using SAS in or out, actually the machine's transactional history screens will will track that. So the machine knows bar code number 9872.  
One went in for $100 and a new barcode number was issued by that machine for whatever the cash out amount was. So historically both the ins and outs of Tito are stored in the EGM machine and likewise as we are the owner of the Tito database, we need to also know that information.  
And and have it available in our portal or somewhere.

**Nathan Carver** 31:57  
Right, OK.

**Will Jones** 32:00  
And so this MIB component that we've been referring to is our SAS host that's going to connect to the machines and then be able to facilitate the transaction.

**Juan Martinez** 32:10  
And Pavel, correct me if I'm wrong. Smib certainly facilitates the transaction with the machine, but I believe that at the Flexpay kiosk is the Tito database. It's not at the Smib.

**Will Jones** 32:23  
Yes.

**Pavel Frolov** 32:24  
Yes, exactly.

**Will Jones** 32:24  
Yeah, when I mean SaaS host one, I'm talking about the serial protocol. So it's the connection directly to a machine or a series of machines that we're talking about that's then going to facilitate just the the transfer of the funds and communicate through some kind of Ethernet protocol to the.  
You know to the host which is is where the actual database persistent store is for you know for the quote funds in transit to the income system and cash and eventually go out. But this this is so.

**Juan Martinez** 32:44  
That's that's correct. Will.

**Will Jones** 32:59  
Have we done a SAS based host system before that manages Tito tickets? Are we levering leveraging an existing, I call it CMS? That's not really what it is, but SMS function that we already provide or is this brand new too?

**Pavel Frolov** 33:19  
No. Currently we're just developing such that communicates to our SMIP and SMIP has its own implementation of SAS protocol.

**Will Jones** 33:23  
So.  
OK.  
I'm I'm gonna say my my one second. Wow, there's a lot of moving parts here. That's not a trivial thing to do. Done it several times. It's great, but wow, this is definitely.

**Pavel Frolov** 33:44  
Mhm.

**Will Jones** 33:49  
In itself, a fairly significant, you know, piece of the puzzle to get it right and make sure we don't drop funds, that we don't have problems. And of course we have to somehow have the ability to deal with deal with issues.

**Pavel Frolov** 33:57  
Yes.

**Will Jones** 34:06  
When the terminal doesn't behave like it should behave. So if we're not actually present at the site and trying to help, we have to provide all that functionality to whomever it is so that a customer who has a dispute can be assured to get funds without some kind of other, you know, oddity of the funds actually existing or.  
you know Being added at some later point. So I'll step back down, but there's a lot of pieces. This is really, this is a great project, but it's it's very complex.

**Pavel Frolov** 34:39  
Yeah, actually the the first pilot run of SAS system was done, I assume, on the Georgia show. What? What was the experience?

**Juan Martinez** 34:49  
Yes.  
We it worked flawlessly. I mean both the once we ironed out the initial issue reboots and and that sort of stuff, it worked fine. I mean we we moved Tito ticket from machine to machine and then there was one human error.  
And it was actually made by me in the Tito, the Tito machines. After showing and demoing the e-wallet kiosk so much, I instinctively started my player journey by inserting money into the Tito kiosk. And I shouldn't have and the kiosk misbehaved.  
Because it wasn't supposed to print a ticket, I'm supposed to go right to the machine like normal Tito was. But other than that, once we rebooted the device, everything was back to normal. So yeah, I mean we from the player perspective, everything worked. It auto dispensed a card even though we didn't actually.  
Put money on the card, but the the Tito in Tito out card dispense worked. E wallet in E wallet out card dispense worked on on both sets of games and kiosks.

**Pavel Frolov** 36:05  
So the first positive experience from the fields.

**Juan Martinez** 36:10  
Absolutely, absolutely. Yeah, definitely.

**Will Jones** 36:10  
Yeah, very good.  
The first to first human error in the field too.

**Juan Martinez** 36:16  
Exactly. Yeah, yeah, yeah.

**Will Jones** 36:19  
OK, very OK, intriguing. So it comes back to a Tito ticket. The Tito ticket can of course be used on either of the devices or cashed out at the kiosk or at a at a flex terminal then and that can produce a gift card.

**Juan Martinez** 36:37  
Uh, correct, correct and it.

**Will Jones** 36:38  
Yeah. So and when it produces a gift card, that's going to go, that's going to be a communication protocol that we define from the site back to the server that we have and then from the server that we have, it's a income protocol.

**Juan Martinez** 36:55  
And you call it cloud, the cloud server, right? Will.

**Will Jones** 36:59  
Yeah, either Cloud or it could be, yes, that's exactly what I'm talking about that one. So but it's going from the site to our server and that's actually a misnomer. It could be just a service, but it's something that's in the Cloud then.  
And beyond that, it's the income protocol that the actual transfer. So that thing in the cloud, we're either gonna do a full transfer of funds from site to cloud, from cloud to income or we're gonna go directly across the entire way and then the only thing is the.  
That's facilitating it is just an interim broker of the funds. So that sounds about right.

**Pavel Frolov** 37:42  
Yeah, actually let let me share my screen. I posted the link to this board. Actually we could.

**Will Jones** 37:49  
OK.  
Is that from yesterday? Yeah, or uh, Wednesday?

**Juan Martinez** 37:57  
Oh, this is a new a new board.

**Pavel Frolov** 38:00  
Actually this board was discussed probably 2 weeks ago, but actually together with our developers tried to at at at least.  
A top level view on architecture. So actually here we can see a bank.  
These two machines that works as E wallet schema and through the router it connects to the Internet and in the cloud we have two different.  
Uh, serious.  
One of them right right part. It's something looks like a CMS because you know management system. So in in new words it will be orchestration platform I I think.

**Nathan Carver** 39:00  
Yes.

**Pavel Frolov** 39:05  
And the left part is a cloud servers that works with income, with income or any other third party partner. And here we will need to have an ACH.

**Will Jones** 39:16  
Hmm.

**Pavel Frolov** 39:23  
Communication automatic clearing house as it was shown on in text from Juan.

**Will Jones** 39:33  
Mhm.  
So, but we won't issue a card unless we've had success with the protocol between that ECH and income or whatever the third party is.

**Pavel Frolov** 39:37  
Uh.  
Yes, during a redeem process. So the kiosk or Flex POS initiate a transfer from the no using the Internet through the router.  
So communication will go to the GVLP payment cloud server, then communicate to in call.  
Get answer and if everything is OK then it will get answer on the kiosk and produce activation, make activation of the card and eject the card.  
It's a cut in general.

**Will Jones** 40:33  
Yep. So I think in in this puzzle it's key to think about the funds as something that is it's not just a value but has a has an owner or location. So and it can't be transitioned from 1 owner to another location.  
Without a very watertight communication protocol, something that is at least that that has at least two acknowledgments. I don't think there's any way to do it without two acknowledgments. So the funds need to live somewhere and I think they have to stay in the E wallet until they actually.  
Actually make it to income. Otherwise you'll have to create some kind of transactional logic to say that if they get committed to our server, then they can still get rolled back to the site because obviously you never want them in the server stuck and not able to issue that gift card, which means the player can never walk out of the casino with their.  
Money, so to speak, with any kind of asset that they can use to to access their money. But yeah, interesting puzzle.

**Juan Martinez** 41:41  
And and yeah, Will we the the customers. I asked everyone I could during the show what sort of ticket expiration life they wanted and it was as as low as one day, five days.

**Will Jones** 41:46  
Mhm.

**Juan Martinez** 41:56  
But some, you know, said maybe 30 days. So some of the sharper customers certainly want the guests to come back and to hold on to that E wallet. So we we have to further think about where those funds live.

**Will Jones** 42:04  
Mhm.

**Juan Martinez** 42:12  
For a period of 30 days, you know, with the customer wanting to come back and redeem them at a later time.

**Will Jones** 42:13  
Mm.  
Yeah, because that are these systems that are, you know, all these different systems at the site that that have quote the funds, you know, have have the ownership of the funds until expiry or until they get pushed to a machine or income.  
That you know, how are we considering, you know, backups of that information too? Is there? How do we ensure the integrity of of that site even if it went up in flames?

**Juan Martinez** 42:37  
Yes.  
So just so I understand, your question is how does the local e-wallet kiosk and its data become protected to the cloud or In Sync with the cloud so that we always know how much money is on the wallet even if the kiosk broke and caught fire?  
Fire.

**Will Jones** 43:13  
Yeah, or exactly. Or you can make it so that the kiosk and that the information at the site is really just a dumb terminal and that everything's actually stored in the cloud. That's an acceptable solution too. However, then you have 100% uptime demand in terms of the connectivity.  
Between the site and the cloud, because otherwise you wouldn't be able to ensure that. But it's very interesting when you actually, when we're the owner of the funds, we have much greater responsibility than if it's just the transit piece, right? The transit piece just means you have to.

**Juan Martinez** 43:36  
Sure.

**Will Jones** 43:53  
You have your T's crossed, your I's dotted, and every single one of the the transactions gets successfully committed or successfully rolled back. That's the 22 outcomes to it. So, but if we're actually holding the funds at the site, what's our fault tolerance level for that?

**Juan Martinez** 44:04  
Yeah.

**Will Jones** 44:10  
You know, are we going to be having multiple devices? Are we backing up to the cloud? I know there's all, there's many questions then that that surface in that area.

**Juan Martinez** 44:10  
Sure, sure.

**Pavel Frolov** 44:19  
I assume that we have a requirement one. Correct me if I'm wrong, that if we lost communication to Internet for the location, we can proceed to work at least.

**Juan Martinez** 44:32  
Yeah.

**Pavel Frolov** 44:36  
Able to move between machines, exchange money from machine to machine. Except for generating cards. You can generate card only if Internet is available.

**Nathan Carver** 44:50  
Correct.

**Juan Martinez** 44:50  
Correct. But then that that is the opposite of one of the solutions proposed by Will, meaning the data has to be stored locally in order for that scenario to work with with the ability to not print the final gift card because we've lost connection to income.

**Pavel Frolov** 44:57  
Yes.

**Juan Martinez** 45:08  
So yeah, Will, the the goal was to allow the wallet to move from machine to machine to minimize the guest frustration, but that upon final cash out that can't be done through the kiosk because we may not have Internet connectivity.

**Will Jones** 45:17  
Mhm.

**Juan Martinez** 45:26  
Which means E wallet has to function fully locally.

**Will Jones** 45:30  
Yeah, so that that means that the actual that that kiosk, if you lose that kiosk, you lose money.

**Pavel Frolov** 45:31  
But.  
Not exactly. I assume that we will we'll be able to share all the data related to tickets to accounting directly to JVL.  
Terminal communication server. After we do any operation here on the location, I think we will share this data with the server. This is in order to.

**Will Jones** 46:07  
Yeah.

**Pavel Frolov** 46:11  
To support different feature to be able to replace broken terminal. Of course we do not can support 100% restoration. In some cases we can lose lost money.  
But highly likely if the device broken not during the transaction, I think we will be able to restore actual Tita server state.

**Will Jones** 46:43  
Yeah, I think so. I would, I would think that there's probably going to be a requirement to have a write only durable hardware device in that kiosk that always records transactions. So that should you have that situation, painful as it may be.  
You should be able to restore to the previous one, otherwise you have no ability to handle disputes or the financial disputes that will come with a actual kiosk lost. So you sever the router connection. Let's say it's allowed to operate 24 hours independently. Don't know what.  
The actual term's going to be, but there's obviously going to be a limit to how long it can operate without a connection. And then at the point when it the the device is destroyed is removed that kiosk that how do you get back to the point of understanding what transactions went on while it was running independently?  
So that's where I think there would be other considerations to to to think about that as you know is is is like an ATM as a is an extremely you know resilient unit in the financial transaction world.

**Juan Martinez** 47:58  
So the device that you you just described is an on premise server that interacts with the cloud as needed though, right?

**Will Jones** 48:13  
That's definitely what what was just described by Paul. It is one that can take the full functions without the requirement of having a server in the cloud to communicate to. Obviously it needs probably in the beginning, but once it's severed, it can run completely independently.

**Juan Martinez** 48:32  
Yeah, but in what we're seeing on screen here, both of the left and right squares here represent cloud solutions. If I, you know, so we we I don't see on this drawing a local server.

**Pavel Frolov** 48:42  
Yes.

**Juan Martinez** 48:47  
Or a device that can locally store data, you know, however we want to call it.  
And let me ask you, Pavel, is the flex port capable of storing?  
A limited amount of data for this purpose.  
You know, I've scanned my E ticket.

**Pavel Frolov** 49:10  
Let's sport.  
Flexport is quite a simple device with limited memory.  
I don't think so that we can uh share some some extra data from the server. I mean local server from the.

**Juan Martinez** 49:33  
Right.

**Will Jones** 49:40  
Yeah. Implex sport is the is the iview equivalent, right? Juan, something that's stuck on the Yeah, OK.

**Pavel Frolov** 49:40  
You can.

**Juan Martinez** 49:45  
Yes, correct. That's correct.  
No player tracking, just the facilitation of the optical reading of the Tito ticket or the ORA barcode in the future for a card.

**Will Jones** 49:56  
Yes.  
Is the is the the E wallet terminal, the flex pay in that diagram? Is that a required component of any site?

**Pavel Frolov** 50:10  
Um.

**Juan Martinez** 50:12  
OK.

**Pavel Frolov** 50:12  
No, no. Actually, I think we're going to develop infrastructure.  
To build a location equipment by requirement for of this location. For example instead of a wallet Flex pay it it could be Flex POS plus Flex tower.  
Install it on the location and.

**Juan Martinez** 50:41  
Yeah, well, I mean, I'm sorry. Go ahead, Paul, go ahead.

**Pavel Frolov** 50:44  
And actually each of this device can operate as a server and it it can be changed by by any additional set up I think.

**Will Jones** 50:58  
So they'll they'll have persistence data store local to the site that is either Flexplay, Flex Tower. It's something that can actually persist accounts.

**Pavel Frolov** 51:03  
Mhm.  
Actually we thought about this, not sure that it will be in first generation, but highly likely we can support something, something like this.

**Will Jones** 51:24  
So, so it's not expected in the first generation to have full full fault tolerance to the to an Internet connection loss. It can just it. In some situations there'll be enough to be able to facilitate that and run independent of a server. In other situations it won't.

**Juan Martinez** 51:44  
What? Yeah, like he said, I mean Flex pay realistically our our first target for Q4 of this year is the Flex point of sale device and ideally that does not require a Flex pay kiosk. Remember that the main function of the kiosk is to issue that card.

**Will Jones** 51:53  
Mhm.

**Juan Martinez** 52:03  
And the POS device at the cashier window can scan and produce the dispensing through the dispenser, the card device. So in in our first Q4 go live, we actually don't even want to see a Flexpay kiosk at the.

**Will Jones** 52:04  
Mhm.

**Juan Martinez** 52:23  
First installation site because POS is supposed to be doing everything.

**Will Jones** 52:28  
So and if POS is just a you know is got no actual persistent storage, then in it's you know from what I'm hearing here it's not possible to run independent.  
In other words, if there's a cash out, that cash out has to be stored somewhere where it has persistent storage. It can't not otherwise, unless you're saying like a piece of paper is the actual persistent storage and you trust that that doesn't get copied or whatnot, which obviously wouldn't, but.

**Juan Martinez** 52:55  
Right, right.  
Right.

**Will Jones** 53:02  
So, yeah, so I'm, I'm kind of, you know, oh, happy birthday, Juan. Whoa, there we go. We're we need to sing it. Can we, can we sing it in Russian at the end? Happy birthday. I would like that very much.

**Juan Martinez** 53:08  
Thank you. Thank you.

**Pavel Frolov** 53:10  
Oh.

**Juan Martinez** 53:15  
OK, go ahead, Pavel. All right.  
So what was that, Juan? Go grab some vodka. Is that what you told me to do?

**Will Jones** 53:25  
That's what I heard too. Good ears. But yeah, so, so the the, you know that the point being that, you know, in order to make it so that we don't lose funds.

**Nathan Carver** 53:27  
Yeah.  
So it said.

**Juan Martinez** 53:33  
Thanks. Thanks guys. Yep.

**Will Jones** 53:44  
In the transit, if we don't have a connection, then you know we need something to persist those funds on Prem and then get back to the accounting. We need to have a mechanism for accounting for them because obviously a reconciliation may happen at.  
In a time when it's disconnected, we need to be able to account for funds in any location they might be, whether they're in the e-wallet form, the Tito form, the, you know, already transferred to income.

**Juan Martinez** 54:14  
So I mean, and when you say persistent, do you mean not the device's RAM which could be lost if if something happened, more of a a hard drive, a SSD or something along those lines?

**Will Jones** 54:27  
Correct, correct. And I would even suggest that if we were talking about making this such that it can really run independent for, you know, a long period of time, we also because it's only a onesie at the site, right? It's not guaranteed to be a series of these things.  
We probably need to at least least discuss having some secondary storage that is the kind of write only transaction unit that always allows you to go back to to reconcile fully to say, look, everybody, the worst of the world happened. We lost everything. Somebody either stole that terminal or.  
Some, you know, like caught fire. We should have some kind of unit to go back to to say that's the, you know, that's what happened. These are the actual transactions and then we can come back to a a number that makes sense. Otherwise I can only think the other way that they could do this is to go to the terminal itself.  
And try to reconcile from the terminal what was in and out to, you know, basically what what the player should be, you know, redeemed with. In which case, you know, if the worst case scenario in the world happened, I don't know how we redeem.  
Offline. Does that mean they call somebody in JVL and then JVL issues something through income? I'm not sure and ship them a gift card or do they actually just give them some cash and let them walk away?

**Juan Martinez** 55:42  
Hi.  
Yeah, I mean, they're not supposed to even give them cash. So, but that that's the location's discretion there. They can pay them in lottery. State lottery tickets is a form of acceptable payment. Yeah, but but you're right.

**Will Jones** 55:57  
Yeah.  
OK.  
You know what I mean? It's like a dispute kind of scenario because everything bad happened.

**Juan Martinez** 56:12  
Yeah, but remember, Will, in terms of reconciling at the EGM, so because we're moving the money in through bill acceptor pulses and out through hard meter pulses, we can't say that the wallet ticket number 2251.

**Will Jones** 56:17  
Hmm.

**Juan Martinez** 56:31  
Introduced $20. All we know is $20 was introduced source unknown because it's serial. So it's.

**Will Jones** 56:38  
Mhm, yeah.  
Yeah, it's interesting, but at least they could go back, you know, I don't know that the site has tapes, but they can go back to the terminal that the that the player cashed out from and try to use that as the source of what was cashed out because there's got to be at least a cash out log in the terminal. I'm assuming it's like a normal slot.  
And it's got one, then you could at least use that to determine what payment should be if everything else didn't know.

**Juan Martinez** 57:01  
Sure.  
For sure. Let me ask you based on what Will just described, do we need to rethink about the POS hardware specifications to consider even something as simple as a Compact Flash?  
For for for storage, that's, you know, less volatile than the the RAM in in that device.

**Will Jones** 57:35  
So we don't even have any. Well, it has to have something for the program file, but there's no writable disk on the POS. That's the table top one.

**Juan Martinez** 57:46  
I am.  
I'm not sure if there is.  
See here.

**Will Jones** 57:55  
Is it Pavel today? Does it just assume that there's always a connection to the server?

**Pavel Frolov** 58:04  
Yes, right now we assume that we will have one 100% acceptable server connection to share the data, but.

**Will Jones** 58:18  
Got it. Is it like that's like the payflex port facilitates the transaction off the terminal and communicates directly with the server to put the funds in an account that that resides in the server?

**Pavel Frolov** 58:34  
Actually I think this is not an issue to install SD card for example to store in some some duplicates of data.  
Not much.

**Juan Martinez** 58:54  
Yeah, I I quickly looked at the specs supplied by Genadi Peari and he just doesn't drill down into any sort of memory. So I I don't know if there's any physical storage medium today. We got to consult with him.

**Pavel Frolov** 59:09  
Uh, on current uh uh hardware.  
It's ARM based CPU. Actually this is what we have EMMC storage, some main storage, but additionally it has a slot for SD card.

**Juan Martinez** 59:29  
Oh, OK.

**Will Jones** 59:39  
Yeah, no, we're we're already to seven, so or to to the hours, I know. But I have many more questions now drilling into like what happens when the EGM cashes out and the payflex port is not functioning correctly.

**Juan Martinez** 59:43  
Yeah.

**Will Jones** 59:55  
Like where where do funds go in that scenario? You know, these other kind of things that you probably have already dealt with.  
Like what if it's not communicating with the BV? Does that mean then that the game's tilted? Cause the paypack payflex port is a facilitator between the the printer commit comms, you know the comms between the printer and the actual EGM. So the EGM would have to tilt if the printer device is not functioning anymore.

**Pavel Frolov** 1:00:22  
Yeah, intentionally I think if machine equipped with a real bill acceptor and it connected to our flex port, a flex port connected to the bill acceptor protocol to machine.

**Will Jones** 1:00:32  
Mm.  
Mhm.

**Pavel Frolov** 1:00:58  
It will show a tilt related to build build validator.  
But actually, actually we I think we can operate without the acceptor.  
For some locations we can install flex ports, do not allow player to insert money on the machine, but all the time work is e-wallet. It's also possible operation.

**Will Jones** 1:01:18  
Hmm.

**Pavel Frolov** 1:01:32  
And in this case you'll not produce any bill validator error except for some internal errors on flex port.

**Will Jones** 1:01:33  
OK.  
Mm-hmm.

**Juan Martinez** 1:01:44  
Yeah, that scenario you just described probably would not go overwhelming. Most of the people at the Georgia show liked that you could top off your E wallet by not having to get up from the machine, which players don't want to do, especially if they perceive to be on a lucky streak. So removing the.  
The bill acceptor is probably a no go. Removing the printer that certainly was was a 5050. Yeah, that's a great idea or we're not sure about it yet, but the the bill acceptor would probably going to have to remain in in play for the scenario.

**Will Jones** 1:02:21  
Yeah, players have to get.

**Juan Martinez** 1:02:22  
Well, we'll do you just wanna just.  
Right.

**Will Jones** 1:02:26  
Yeah, I know the players have to obviously accept that, not have any anything to hold in their hand after the session and just feel confident that the e-wallet is is, you know, the funds are always landing in the e-wallet.

**Juan Martinez** 1:02:42  
Sure.  
Will, do you have to get going?

**Will Jones** 1:02:46  
I I do today 'cause we have a software release going tonight. I thought we were doing only an hour today. I'm I'm sorry if I mistook that, but.

**Juan Martinez** 1:02:54  
No, no, absolutely. Yeah, we just ran along. It's my birthday. Will, come on.

**Will Jones** 1:02:56  
Yeah, yeah, yeah. Happy birthday.

**Nathan Carver** 1:02:58  
Mm.  
Happy birthday, Juan.

**Will Jones** 1:03:01  
Yeah, I think this is, this is fascinating now that I have a lot more understanding of the the minutia here. I think there's a lot of interesting points to it to make a resilient system, you know, with so many, as I said, with the so many parts.

**Juan Martinez** 1:03:01  
Yeah, thanks.

**Will Jones** 1:03:18  
Reconciliation. Yeah, we didn't even get to that. Sorry, because I just dug in deeper to these other details. But the reconciliations can also be really intriguing too. But I don't, you know, these these properties that are operating.  
Do they even really have the ability is the is not exactly what I the word I want to use, but will they have the training to do a reconciliation? You know, I mean there's there's no cage, right? There's just maybe some manager behind the.

**Juan Martinez** 1:03:48  
Yeah.  
No.

**Will Jones** 1:03:52  
Counter selling cigarettes if you're lucky, so.

**Juan Martinez** 1:03:56  
Yes and and we'll yeah the you you said it best. These are 1015 dollar an hour employees today. They don't do anything. They have no real knowledge of what's going on other than hey Mother Goose ticket says I owe the guy at machine #420 bucks. Let me go ahead and and.  
Manually encode the gift card and give it to them because most of the product doesn't belong in the location, it belongs to the master operator. So yes, the skill set is very low and in trying to deal with this, they're selling cigarettes, they're filling gas, all these other things at convenience stores.

**Will Jones** 1:04:19  
Yeah.  
Yeah.

**Juan Martinez** 1:04:36  
So that expectation is is not there. There is no accounting department at 99% of these locations.

**Pavel Frolov** 1:04:44  
Yeah, and currently, currently all machine or all bill acceptor contains only bank notes. In future it will be a 5050 in Tita operation bank notes plus tickets and.

**Will Jones** 1:04:44  
Yeah.

**Juan Martinez** 1:04:55  
Yes.

**Will Jones** 1:04:57  
Mhm.

**Juan Martinez** 1:05:00  
Yes.

**Pavel Frolov** 1:05:00  
I don't know what is currently doing casino during reconciliation of do they take this tickets place. It's that special, yeah.

**Juan Martinez** 1:05:13  
Yes.  
Yeah, yeah, they have $100,000 bill and Tito counting machine and you you you load them on, but that has a staff of 20 people supporting that process, so.

**Will Jones** 1:05:26  
Yeah, yeah, there's a there's a lot more that goes with that cage accounting piece. So anyways, I'm, I'm, as I said, Juan, I think I'm just really intrigued to kind of think through this. I guess if I can ask a question like what is?  
Yeah, for me, I'm just feel like I, you know, I'm just on the bottom of the mountain climbing it to understand the full picture. So but what what would be the the ask of producing, you know, the next most valuable piece of information for Pavel, his team, for who, whomever this is?  
Most important for to continue to March and be on, you know on target for that the I don't know what it was January 1st, but the you know the the due date for having a system in the field.

**Juan Martinez** 1:06:15  
I mean, I I'm gonna share my that document that I had on screen with you guys. Now I I would just say is, you know, let's focus on getting Nathan some rough use case scenarios for what happens.

**Nathan Carver** 1:06:15  
Yeah.

**Juan Martinez** 1:06:30  
If this happens scenario kind of thing, I think that that would be the the best thing to truly break down the the points of failures and how we can get to an acceptable reconciliation tool for for go live would be the most important thing.  
Aval, you you agree that we just need to feed you all the the use cases we can. You know basically we still need to digest the diagrams that you share earlier today and and so forth just to understand a little bit more of the architecture.

**Pavel Frolov** 1:06:53  
Yes, yes.  
Yes, it's agree.

**Nathan Carver** 1:07:11  
Yeah. And so and I've added those two use cases out there to drive forward with the first release of Flex POS. So feedback on those and if they're going in the right direction and I'm, I'll just keep turning on use cases and wiring up requirements to support them.

**Juan Martinez** 1:07:31  
Perfect.  
Great. Um.  
And also, so our our next meeting is next Wednesday the 27th. That one I can attend even though I'll be in South Dakota, but Friday the 29th, I'm already booked with a customer in South Dakota and also from Val's.  
Notes. We had a larger team review for this discussion point on the 29th. Do we believe we're gonna be ready or I I would like to move it to the following week.  
The 3rd of September, just because next week is crazy for me in South Dakota as well. Are we all in agreement with that to push it to maybe Wednesday the 3rd of September?

**Pavel Frolov** 1:08:26  
Yeah, yes.

**Will Jones** 1:08:27  
Find that, yeah.

**Nathan Carver** 1:08:28  
Let me look at that real quick. I might be traveling that day.

**Juan Martinez** 1:08:33  
OK, and it could be Tuesday. It doesn't matter. Whatever day works for you, Nathan.

**Will Jones** 1:08:38  
It's.

**Nathan Carver** 1:08:38  
OK.  
OK, so I'm fun fact. I'm getting married on the 7th, so I'm not available that week through the 10th through the 13th. Yes, I'll be on the road on the 3rd, so I could do it on the 2nd.

**Will Jones** 1:08:44  
OK.

**Nathan Carver** 1:08:55  
By the force.

**Juan Martinez** 1:08:57  
well

**Nathan Carver** 1:08:58  
Or the 5th even.

**Juan Martinez** 1:09:00  
We'll do it on. OK, let me let me confirm Val's schedule too, because that's going to be a larger meeting. So we just won't do it on the 3rd. It'll either be the 2nd or the 4th after I speak to Val.

**Will Jones** 1:09:02  
So.  
Yeah, I'll I'll speak to that because at the SEC, I'm dropping my daughter off at school and we travel home on the 2nd. So I'm definitely in transit on a flight on the 2nd, so I wouldn't be able to do that day. Not that it has to include me in whatever meeting, but just saying that I would not be available.

**Juan Martinez** 1:09:25  
OK, so.  
OK, so I will push for the 4th then subject to Val's availability.  
Alright.  
Anything else guys?

**Pavel Frolov** 1:09:40  
No.

**Will Jones** 1:09:41  
Only happy birthday, Juan. What are you doing tonight for your birthday?

**Pavel Frolov** 1:09:43  
It does, then, yeah, again.

**Juan Martinez** 1:09:44  
Yeah. Thank. Thank you. Thank you. Thank you. Alrighty guys. Appreciate it. Thanks everybody. Bye, bye.

**Will Jones** 1:09:49  
All right, take care.

**Pavel Frolov** 1:09:49  
Thank you. Bye.

**Nathan Carver** 1:09:50  
All right, everyone.

**Juan Martinez** stopped transcription