**Transcript**

September 3, 2025, 12:03PM

**Juan Martinez** started transcription

**Juan Martinez** 0:03  
Some of our other meetings he has been on and and he's briefly discussed it with us. Val, just his unfamiliarity with our CMS has just made it a bit difficult for him.

**Val Levitan** 0:23  
OK, so what's the objective for this meeting?  
What are we tracking?

**Juan Martinez** 0:28  
We're just just a this is a just a our our weekly follow up on on on the CMS block diagram and architecture Nathan has been continually.

**Nathan Carver** 0:30  
Yeah.

**Val Levitan** 0:37  
OK.  
You got it.

**Nathan Carver** 0:43  
And.

**Juan Martinez** 0:46  
Updating GitHub with additional requirements related to cash flow reports, Mother Goose and and things like that so.  
I'm just going to share. Go ahead, Nathan.

**Nathan Carver** 1:00  
Yeah, I.  
So it's just yeah, specifically Juan and Val, the document I put up there on the ACH provider recommendation which is Diwala and with the Diwala now has the integration in the background with plate. I believe that's the name.  
And so we can touch on that and then just a little that also would lead into some of our dispute resolutions if we want to dive into that. I know that was something that we were talking with Will, but.

**Juan Martinez** 1:35  
Yeah.

**Val Levitan** 1:37  
The ACH provider is quite interesting. Can you tell me more about it?

**Nathan Carver** 1:45  
So the Duwalla.  
The reason I went with this one is because one of the risk mitigations we can do is have an instant account verification balance verification. So before we initiate the transaction Duwalla now that they're integrated with played.  
Provides an API that allows us to check the balance that we're going to draw an ACH transaction with this. This is my understanding of their API. So I don't know the cost of that. There is a cost to do that.  
But Diwala has wrapped all of those features up into their total cost, which initially is $0.50 per ACH transaction or I should say point.  
.5% per transaction.  
And it caps at $5 with a minimum of $0.05 and so.  
So that was, I thought that was good. That seemed pretty decent. We would have to adjust our pricing if that was the percentage we went with as far as once we got over the $300.00 ticket range.  
But they also have a negotiation with vendors and I think that's the direction to all is going as they start to, they want to negotiate these based on volume and not just have a flat rate. And so the second thing to all is bringing into that is the integration with played that would give us the.  
The ability to check a balance before we initiate.  
The ACH transaction which would prevent us from having or I should say should mitigate some risk of activating a gift card and the location not having the sufficient funds to.  
To pay JBL.  
So the kind of the way I see that API working out is that we could check the balance and then abort the gift card activation if the location doesn't have sufficient funds.  
We would have to verify all that. Dualla has I think pretty decent documentation and I put some references in there, but I almost should be able to dive in and get more detailed verification if based on the documentation Dualla provides.  
And so, so that was the big thing that I I saw there. I think there's some other options, but that seemed like one of our better options to at least start looking into.

**Val Levitan** 4:12  
Um.  
I just, I I just want to make a point here. When we talk about ACH transaction, we're talking about a once a day transaction with a location where we swipe the entire amount.  
So let's say there were, I don't know, 50 tickets issued and total amount due from a location for that day is $5000. So we swipe the entire amount and transfer the funds.

**Nathan Carver** 4:46  
It.  
I see. So to I see. So that would reduce the the volume, but also cap out the transaction fee at the $5.

**Val Levitan** 5:07  
So that also means that in our contract with the location we should build in this cost.

**Juan Martinez** 5:16  
Yes.

**Nathan Carver** 5:17  
Yes.

**Val Levitan** 5:18  
OK, the other thing that I want to know is.  
Um.  
The time that it will take from the moment we swipe their account or initiate the transaction to the point when their money come to our account or.  
Yeah.

**Nathan Carver** 5:49  
OK. Yeah, I can verify that and dig into the providers on that specifically.

**Val Levitan** 5:57  
That that is, that is essential because we have a.  
Deadline by when income swipes our account.

**Nathan Carver** 6:10  
OK, yeah, that makes sense.

**Juan Martinez** 6:13  
And Val, the ACH portion between JVL and income, that is an ACH that income will set up and we simply provide them our banking information. Is that how you understand it or?  
We need to figure out also how we pay income.

**Val Levitan** 6:38  
No, that's the first variant.  
We set up, I mean we submit our ACH information to income. They set it up on their end.

**Nathan Carver** 6:51  
Mhm.

**Val Levitan** 6:54  
And they swipe our account every, you know, with certain frequency, you know, established contractually.

**Juan Martinez** 7:00  
Yes.  
OK.

**Val Levitan** 7:04  
I also understand that there should be some.  
Reliable accounting between all parties because, you know, we should probably invoice our customers in advance.  
The I assume they confirm the they look at the invoice, they confirm the set of transactions, they probably approve it.  
I or maybe not, I don't know, but I'm pretty sure that there should be some sort of reconciliation in between.

**Nathan Carver** 7:40  
Yes, mhm.

**Val Levitan** 7:40  
And and at the moment I do not quite see exactly how it works, so we should dig into it.

**Nathan Carver** 7:50  
Right. So if we're if we're charging them in batch, then we'll have to um.  
Every gift card transaction that is associated with a specific batch that we withdrew money from them. So that's how we would have to be able to reconcile. So if they looked at a daily withdrawal from their account.  
For $5000, we need to be able to report on every transaction that makes up that $5000 and then be able to trace those into the income.  
At least for our side, we need to be able to trace those into the income transactions and then again into that draw that the income might have on JDL and those may not align if we're not drawing, they're not drawing at the same time.

**Val Levitan** 8:29  
Right.

**Nathan Carver** 8:40  
If incomes drawing multiple times a day.

**Val Levitan** 8:44  
Well, no, I mean we we should probably get on pace drawing equivalent amount at the same time, but probably probably X number of hours ahead of ahead of income.

**Nathan Carver** 8:53  
OK.  
Gotcha. Makes sense.

**Val Levitan** 9:05  
We we should we should be going at the same pace, otherwise it will become impossible to reconcile.

**Juan Martinez** 9:06  
OK.

**Nathan Carver** 9:09  
Yep, right.  
Yeah, I agree.

**Juan Martinez** 9:13  
Yeah. And it's actually, I mean, if we're going to debit the customer's account on a daily basis, it is almost impossible for them to do a real time reconciliation. It always has to be after the fact.

**Nathan Carver** 9:21  
OK.

**Juan Martinez** 9:28  
You know, the gaming day, you know, I don't believe Georgia closes. Are they a 24 hour operation? I need to verify that. But if they aren't and say they close at midnight, you know there's nobody up at midnight to reconcile.  
If we initiate the ACH and you know at that specific time as an example, so this is almost always going to be post withdrawal reconciliation. So we would need to provide as much data as possible and ideally in in the electronic format, so sort of.  
An automated e-mail hits their inbox that they can reconcile against.

**Val Levitan** 10:18  
I almost feel like, I almost feel like every transaction that we approve should add to their reconciliation. They could see it in real time.

**Nathan Carver** 10:19  
So.  
So have like a a running total of what's going to be withdrawn that they can see at any time.

**Val Levitan** 10:34  
Angry.  
Yeah, yeah, yeah. In my opinion that should and we should probably send the notice. Here's another transaction validated, another transaction valid. I I don't know this this probably calls for a dedicated conversation on this subject, but.  
We're getting to a point that is becoming an acute issue that we we need to start addressing in a separate meeting. We should probably move it out of the POS meetings and start addressing accounting issues of separate meetings.

**Nathan Carver** 10:58  
Mhm.  
OK.

**Juan Martinez** 11:12  
Sure.

**Val Levitan** 11:14  
Because it will also influence the CMS architecture.

**Juan Martinez** 11:15  
Point.

**Val Levitan** 11:20  
And the cloud architecture.

**Nathan Carver** 11:23  
Yes.

**Juan Martinez** 11:23  
Yeah.

**Val Levitan** 11:24  
I'm I'm estimating that we will be validating approximately $2 billion in transactions per year.

**Nathan Carver** 11:27  
OK.  
So we can contextualize these as components and have and talk about them architecturally, but then have precise conversations for each.

**Pavel Frolov** 11:36  
Uh.

**Val Levitan** 11:47  
Right.  
So I'm looking at approximately $5 million.  
For overnight deposit.  
That's that's the volume I'm looking for.

**Pavel Frolov** 12:10  
Mhm.  
Looks like it's not a problem for us to provide real-time data for operators and for locations, but still not so clear how to.  
Um.  
To make reconciliation between us and between actual operator and then with us, I mean GL and with.

**Nathan Carver** 12:42  
Yeah.

**Pavel Frolov** 12:47  
Uh, income. It's uh.

**Val Levitan** 12:48  
Yes, but but I I understand and I agree with you Pavel. But the reason it's not clear for us is because we've never done it, but it's quite clear for income or people that were in this business. So between this company that sets up ACH, I'm sure that there are other.  
Customers that you know are looking for instant reconciliation, we're not, we're not the only people that.  
That had that will have this capability. So the the world, the the the financial world is by far more advanced and have done it many times. All we have to do is to start asking questions.

**Nathan Carver** 13:22  
Yeah, well.

**Pavel Frolov** 13:26  
Really.

**Val Levitan** 13:34  
Anyways, I'd like to recommend that this becomes its own its own direction with proper people in the meetings. I mean, for that purpose we don't need Genadi in the meeting.

**Pavel Frolov** 13:34  
Mhm.

**Juan Martinez** 13:49  
Sure. And I'll I'll take it as an action item to get a sample invoice from Incom. Maybe they can just hide the customer name just so we know what they're expecting and and maybe we can use that as a guide for our own template.

**Val Levitan** 14:06  
Yeah, we also need a template of our contract between.  
Operator and, you know, incomes partner.

**Juan Martinez** 14:16  
Yes.

**Val Levitan** 14:19  
OK. But I'm, but I'm glad that there are dedicated companies in the business that handle ACH as a business.

**Juan Martinez** 14:20  
Understood.

**Val Levitan** 14:28  
So yeah, that that kind of that's a that's a great find. How did you find it, Nathan?

**Nathan Carver** 14:35  
I basically turned Claude loose on a on a web research to find to kind of to aggregate different providers and break down their their capabilities and offerings. Most of them are through negotiation of volume.  
Um. And it seemed like, yeah, Dualo's really modernizing their infrastructure for APIs.

**Val Levitan** 14:52  
Does.  
Does does JP Morgan handle any of it?

**Nathan Carver** 15:00  
Yes, I think like banks are like the traditional approach to doing ACH. So I I think most banks you can negotiate.  
As an ACH provider and then Diwala and others are like Stripe. They're the just ACH focused companies more than traditional bank.

**Val Levitan** 15:23  
And can we specify which account to deposit money into?

**Nathan Carver** 15:29  
I believe so. I believe it'd be since they don't host your bank, you would set up that account with them as the primary account or multiple accounts. I'm assuming they can do multiple as well.

**Val Levitan** 15:46  
OK. OK. OK, wonderful. So let's start a different agenda separate from this meeting that deals with ACH and money transfers and all the contractual issues.

**Pavel Frolov** 15:53  
Sure.

**Val Levitan** 16:01  
OK, that's great. Genadi, can you introduce us to the latest design of POS? Can you share it on the screen?  
I think we have our final direction for industrial design. We are doing some more modifications to it, which should be ready this coming Monday, but this will tell you.

**Pavel Frolov** 16:27  
OK.

**Val Levitan** 16:29  
The general direction we're moving in.  
So can you guys see Genadi's screen?

**Pavel Frolov** 16:40  
Yeah.

**Nathan Carver** 16:40  
Yes.

**Genadi Peari** 16:42  
Yeah.

**Val Levitan** 16:42  
Nathan, I know that you're driving. Are you able to see it?

**Nathan Carver** 16:46  
Uh yeah, I see it.

**Val Levitan** 16:48  
OK, so the the few changes that Genadi is making. Go ahead, Genadi.

**Genadi Peari** 16:53  
Yeah, yeah, we'll have a double screen POS as we wanted in the beginning. It looks like this one is defines and feeds everybody's appetite, right? So the main screen will be 8 inches.  
I know Juan very sensitive about this size, so the so the width of the whole device will be 7.5 inches.  
OK, so this one is 8 inches 8 and more like bigger screen. On the back we have a smaller screen for the customer, 7 inches and the less tall. I mean more like squeezed.

**Nathan Carver** 17:22  
OK.

**Genadi Peari** 17:41  
And the scanner position will be not like you see on the side, but it will be in the middle opening here and the ticket will be scanned in the middle, available for scanning for both parties like cashier and the customer.  
Here this will be opening in this this wall in the middle.

**Nathan Carver** 18:02  
Mm.

**Genadi Peari** 18:05  
OK, and the magnetic stripe reader will be on the top, also available for both sides.  
Uh.

**Val Levitan** 18:15  
But uh, but the magnetic stripe reader will be sunk inside of the uh.  
The enclosure.

**Genadi Peari** 18:24  
Yeah, yeah. And also we needed the optional, so probably will be covered.

**Juan Martinez** 18:30  
You mean sunk in as much as possible. It still has to protrude a little bit.

**Nathan Carver** 18:31  
Mhm.

**Val Levitan** 18:35  
It will so the top will have a slide, a slide from from side to side.

**Genadi Peari** 18:39  
Side opening.

**Juan Martinez** 18:41  
OK.  
OK then.

**Genadi Peari** 18:45  
Now regarding the dispenser, inside here we'll have interfaces for all external connections, including dedicated interface to connect the dispenser.  
In case we need it.  
So dispenser in this case will be like dummy product, like just one wire connected here and that's it without any additional features because we have the screens everything here.

**Juan Martinez** 19:22  
OK.

**Genadi Peari** 19:24  
It will also have interfaces for the printer in Motagus.  
We consider to add interface for additional screen if somebody wants to add it and put it on the table with the wired connection instead of this.  
But it looks like it's a very small probability that somebody will ever want it.

**Juan Martinez** 19:57  
But just to confirm, Genadi, because the the name at the bottom says dispenser POS unit.

**Nathan Carver** 19:59  
Mhm.

**Juan Martinez** 20:09  
OK, OK.  
OK.

**Genadi Peari** 20:09  
Just.

**Pavel Frolov** 20:10  
I I I think I have particularly the same question. What is the width of this device? Probably a dispenser can be installed.

**Val Levitan** 20:20  
7/7.

**Pavel Frolov** 20:22  
Within this case.

**Genadi Peari** 20:23  
Hmm.

**Nathan Carver** 20:23  
OK.

**Val Levitan** 20:24  
7 inches we we can we cannot do the dispenser inside of the device because dispenser has a depth.

**Genadi Peari** 20:25  
7.

**Val Levitan** 20:34  
And and the height, certain height and the depth.

**Pavel Frolov** 20:36  
I I mean, I mean widths of the base, not the screen, but the when you see on the 2nd.

**Val Levitan** 20:45  
In this particular, in this particular variation, we would like to see a dispenser as a freestanding autonomous device.

**Nathan Carver** 20:49  
Yeah.

**Pavel Frolov** 20:53  
Mm.

**Val Levitan** 20:55  
That could could be mounted either on the counter or on the pedestal of some sort, and maybe slightly protruding from the cage.

**Pavel Frolov** 20:55  
Sh.  
Sure.

**Genadi Peari** 21:07  
Yeah, Pavel, it's a lot of thinking here. Don't. Don't forget we have a bunch of wires coming here. If you put it on top of the dispenser, you will be. You'll have the whole bunch of wires coming down, which is.

**Val Levitan** 21:09  
OK.

**Genadi Peari** 21:23  
And.

**Val Levitan** 21:24  
Anyways, and it I I think it's important to understand that right now we want to be able to get certain amount of shoulder room and flexibility in the market. So we're looking at 2 autonomous devices, the POS.

**Pavel Frolov** 21:24  
Mm-hmm. OK.

**Val Levitan** 21:41  
And the dispenser are two separate devices.  
Um.  
We're also looking at a at at the POS driving a third autonomous screen.

**Nathan Carver** 21:49  
OK.  
OK.

**Val Levitan** 21:59  
That could extend it with the wire and lay flat on the counter.  
Autonomously closer to a customer.  
As an option.  
And in in this case, we believe we cover any potential or most potential cases.  
No.

**Juan Martinez** 22:29  
So that that optional third screen would just plug in and mirror the current guest facing screen if it wasn't available to them.

**Nathan Carver** 22:31  
7.

**Genadi Peari** 22:39  
No, no, no.

**Val Levitan** 22:41  
No, we'll remove the second screen, so then the POS turns into a single screen and the second screen could be extended.  
Lay flat.

**Juan Martinez** 22:55  
Sure.

**Genadi Peari** 22:57  
You can. You can put the third screen. You don't have to remove the second, but the third screen will have limited.

**Nathan Carver** 23:00  
And.

**Genadi Peari** 23:08  
Graphical performance.

**Nathan Carver** 23:10  
And.

**Pavel Frolov** 23:14  
It's mostly for static data presentation.

**Juan Martinez** 23:18  
Yeah, just just to accept the terms and conditions, right, basically.

**Genadi Peari** 23:19  
It's.  
Yeah, it's like flex sport similar.

**Juan Martinez** 23:24  
OK.  
Sure, but obviously the this third screen will also need to be touch screen as well. OK.

**Genadi Peari** 23:35  
Yes.  
Yeah, so.

**Val Levitan** 23:39  
So a few a few final.

**Juan Martinez** 23:40  
I like that.  
I'm sorry, I I like the third screen option or the floating screen I guess what we could call it. It just it seems easier to place it somewhere for the employees.

**Val Levitan** 23:58  
Well, it's not for the employees, it's for the players, right?

**Juan Martinez** 24:00  
Yeah, but yeah, I meant for the location to actually put it wherever people can actually see it.

**Val Levitan** 24:05  
Yeah, floating screen or autonomous screen, yeah.

**Nathan Carver** 24:08  
OK.

**Juan Martinez** 24:10  
Yeah.

**Val Levitan** 24:14  
So that's the design that we're going for. In general, we'll have a number of modifications illustrated on Monday.  
And yeah, but this is a general direction of design.  
All right. Thank you, Genadi.

**Nathan Carver** 24:36  
Mhm.

**Val Levitan** 24:40  
Um, what's the next thing that we wanna cover on Nathan? What's on your agenda?

**Nathan Carver** 24:46  
So I am writing the dispute use case, dispute resolution use case for Flex POS and it's primarily gonna be driven by the assumption that the customer leaves and then realizes their their $50 winning ticket was only 45.

**Val Levitan** 24:54  
OK.

**Nathan Carver** 25:07  
They're going to come back and complain to the cashier and the mechanism would be the cashier asks for the card, swipes the card on flex POS and we can display to that customer.  
The information that they you know, the reminder that you went through and you you pressed the confirmation button. This was the activation fee, so whatever information, but ideally to enable the device to show the customer the dispute resolution.  
So the cashier doesn't have to do much other than swipe the card and ask the you know and reaffirm the the agreement.  
And by looking at the income API, we can, we can do that. When we swipe, we can go retrieve that information. We can also retrieve any activity that's been on that card from income. And so if there's a current, but if they've used it a couple times, that will also show up.

**Pavel Frolov** 25:51  
And.

**Val Levitan** 26:09  
So it's it's dispute resolution and reversal of transactions.

**Pavel Frolov** 26:09  
Uh.

**Nathan Carver** 26:17  
Reversal of.  
Reversal transactions. You mean like going back just to show the the steps, all the transactions they've taken so far?

**Val Levitan** 26:29  
Well, no, I mean if we want to block the card and say, well, can't use it anymore.

**Nathan Carver** 26:30  
That's a card.  
Oh, with the income API.

**Val Levitan** 26:39  
Yeah.

**Nathan Carver** 26:43  
Yeah, that's uh uh. I need to think if I've seen that.  
They may provide that. I have to look. We can look at the API for that.

**Val Levitan** 26:52  
I know for sure that they provide this, but if this is done, what happens with the charge of $5 and where did the money go and how do we then treat winning ticket? How do we retrieve the winning ticket?  
Like a a lot of things.

**Nathan Carver** 27:13  
So I think a lot of our mitigation will have to be built in in that initial gift card activation. So the audit of the customer accepting the $5 transaction fee before we proceed ensuring that that is clearly communicated to them as best we can.  
What's going to happen and then having our own audit trail back to the user accepting the terms and the card being activated to that specific Mother Goose ticket that we received.  
Inactivated against, so we should have an audit that can go back so we could even recreate the original other goose ticket as you know in the extreme case.

**Val Levitan** 28:01  
Yeah, correct.

**Juan Martinez** 28:03  
Sure.

**Pavel Frolov** 28:04  
Actually, it looks like cashier will not do much with any dispute. He can only provide information related to redeem process. What was the amount? What was the fee?

**Juan Martinez** 28:19  
Right.

**Pavel Frolov** 28:19  
And that's all the next step for cashier and how, how, how can we simplify the cashier work to refer player to third party who can continue resolution, for example link to income.

**Nathan Carver** 28:22  
Correct. Yeah.  
OK.

**Pavel Frolov** 28:37  
Site or telephone number where he can continue his disputing and so on. Probably that's all.

**Juan Martinez** 28:48  
Yeah, I I agree, Pavel. I mean, I was gonna say when the cashier is doing a dispute resolution, we we need to make sure that the her, the location facing screen and the player screen are mirrored.  
So that they can walk them visually through. They're both seeing the exact ticket card, all the redemption processes. But remember, the Coham card already has the income number printed on the back, so it's just educating or reminding the cashier that if they can't.  
Once they've confirmed what they can confirm, the guest just has to go to the number on the back of the card, which is Incom's phone number to prefer the resolution so that that already sort of exists, Nathan.

**Pavel Frolov** 29:34  
Yeah, yeah.  
But at at least we need to be sure that this card actually activated from our side and then the problem right now is on the other side, not not on JVL side.

**Nathan Carver** 29:37  
Alright.

**Juan Martinez** 29:53  
Right, right.

**Nathan Carver** 29:54  
Yeah, I think for JVL, the biggest dispute will be if there's a misunderstanding of the $5 or whatever the activation fee, why their gift card doesn't match the ticket and and I agree we want the when they.

**Pavel Frolov** 30:02  
OK.

**Juan Martinez** 30:05  
Right.

**Nathan Carver** 30:10  
They swipe even the. I guess the customer could swipe the card too. Doesn't necessarily have to be the cashier, but.  
And that information would show up again on the screen with um.  
JVL contact information or QR code they could scan and go to a JVL portal. But then if it goes beyond that, like if it's I think, yeah, if it's beyond the the activation fee and the card is not working or there's a strange transaction on the card.

**Pavel Frolov** 30:22  
So.  
Mhm.

**Nathan Carver** 30:38  
Then they go to. We have to direct them to income after that.

**Juan Martinez** 30:42  
Yes.

**Nathan Carver** 30:49  
OK, that makes sense. I can make sure that I'll make sure that's in the slow.

**Juan Martinez** 30:49  
Um.  
Yeah, Nathan, I suggest some these cashiers are are not used to doing disputes today in their job roles. So we should take the McDonald's approach and and and make that the end result as graphical as possible. So it's crystal clear, you know.

**Nathan Carver** 30:56  
I'll, I'll, I'll refine the slow like that.  
Correct.

**Juan Martinez** 31:15  
Line. Here's the ticket you brought us. Here's the card number or you accepted the fee and this is the total that should be on the card otherwise.

**Nathan Carver** 31:18  
Yeah.

**Juan Martinez** 31:26  
We want to get them in and out.

**Nathan Carver** 31:27  
It.  
Yeah, ideally everything's on the screen and then the contact information for them to proceed with dispute is on the screen too, and the cashier can just point to it.

**Juan Martinez** 31:38  
Yeah.  
Absolutely, absolutely.  
Um.  
From a question Pavel from a without having to log on to a a website, if you just scan the ticket is are the we we need to have some sort of transactional screen.

**Nathan Carver** 31:56  
Mhm.

**Juan Martinez** 32:07  
For for just employee general knowledge that it is a valid ticket, right? I mean we're gonna have if we have a POS only in the Mother Goose scenario, does the POS device have the the database for the Tito ticket or is that in the cloud?

**Pavel Frolov** 32:14  
OK.

**Juan Martinez** 32:25  
Or does it have access to it? I guess is the bigger question.

**Pavel Frolov** 32:30  
You're referring to solution, yes? For this schema, actually cashier will need to log in to the system.

**Juan Martinez** 32:33  
Yes, yes.

**Pavel Frolov** 32:46  
Because actually no any tickets except for electronically put into the database.

**Juan Martinez** 32:55  
Right.

**Pavel Frolov** 32:56  
That's why we need to log in procedure to see a list of all tickets produced by Muto Goose.

**Juan Martinez** 33:05  
Sure.

**Pavel Frolov** 33:08  
And.  
If I think about cheater schema, then probably yes, we can support an option for the player to scan his ticket.

**Nathan Carver** 33:20  
Yeah.

**Pavel Frolov** 33:27  
But what's the purpose?  
Actually, uh.  
Nothing, nothing other than valid or invalid. No more information from the ticket because actual value already printed on the ticket.

**Juan Martinez** 33:49  
Right, right. My, my scenario is, hey, if they had a a ticket in their pocket that they tried to present as a cash out ticket, that may be a photocopy, maybe from another location, you know, we just need to display something that lets them know we've caught them trying to cheat, basically.

**Pavel Frolov** 34:00  
Yeah.  
Yeah, actually I think as we have connection to our.  
Control controlling server I would say then we can try to find this ticket and understand that this ticket belongs to different location and we can say sorry invalid on this location probably this is from different location and it.

**Juan Martinez** 34:34  
Sure.

**Pavel Frolov** 34:35  
It was already redeemed.  
So probably you are cheating or something like this.

**Nathan Carver** 34:40  
Yeah.

**Juan Martinez** 34:42  
Sure.  
So from from a prior discussions, you know we know that there needs to be a log on screen for the cashiers where where is the administration of let's say I've got 5 cashiers at at the 711.  
You know, we JBL don't want to be in the password administration business because cashiers come and go probably on a monthly basis. How? How is the customer logging into the the database or the point of sale device?  
You know, where's the creation of the employees and their passwords being created locally in the cloud? If in the cloud, how are we getting that information to that location?

**Nathan Carver** 35:39  
OK.

**Pavel Frolov** 35:41  
I would say that probably it can be implemented in different stages. The simplest stage just to add in codes on our server side.

**Nathan Carver** 35:44  
OK.

**Juan Martinez** 35:56  
Mm-hmm.

**Pavel Frolov** 35:57  
And assign in code to the POS device.

**Nathan Carver** 35:58  
Cool.

**Pavel Frolov** 36:04  
Next, it could be a different procedures how to create for example credentials on location if you have for example special magnetic card with admin.

**Nathan Carver** 36:05  
OK.

**Pavel Frolov** 36:20  
Rides for the location.  
Exit.

**Juan Martinez** 36:25  
Yeah, I thought about that. But then are we JBL responsible for supplying these magnetic cards? Do we just tell the operators, hey, these are the ones we've tested, please buy them from here. It's your responsibility to encode them. I I just want to understand.

**Nathan Carver** 36:34  
It's good.  
Mhm.

**Juan Martinez** 36:43  
That relationship where we don't want extra work on us. I certainly think of a magnetic card as secure, but it has to be managed by somebody to encode the card with the pin. I and I just don't know who that is because of the specific uniqueness of.  
Georgia and convenience stores and all of that.

**Pavel Frolov** 37:12  
So this is a different topic that we need to cover during our next conversation, at least before we we are ready to production.

**Nathan Carver** 37:14  
So good.

**Juan Martinez** 37:16  
Yes, yeah.

**Pavel Frolov** 37:27  
Environment.

**Juan Martinez** 37:29  
Right.

**Nathan Carver** 37:35  
OK, sounds good. So the focus would be on how do we associate the user to a magnetic card and then a PIN code and then that PIN code associated are those two, the card, the PIN code.

**Pavel Frolov** 37:36  
So my.

**Nathan Carver** 37:52  
Associated to a specific Flex POS device.

**Juan Martinez** 37:57  
Right. And and not even maybe not even having the card, maybe it's just the pin number that you know I we need to do an analysis on you know those cards I and and that there's a cost to the cards.  
And they break, they left them at home. You know, the magnetic stripe got erased because they put it next to whatever. That happens with your hotel room keys all the time. So it it it's magnetic cards or they do require more maintenance than just a password or PIN code.

**Pavel Frolov** 38:33  
Yeah, it it could be some procedure when we assign for example 8 numbers pin code for admin use of the location and the person who has this number 8 digits.

**Juan Martinez** 38:43  
Great.

**Pavel Frolov** 38:49  
He can produce different pin codes for the cashier, for example.

**Juan Martinez** 38:54  
Really.

**Pavel Frolov** 38:56  
Visibility to create new pin codes, to remove old pin codes, so on. But again I I suggest to make it in stages, for example to plan just a simple procedure to create pin code.

**Juan Martinez** 39:02  
Sure.

**Pavel Frolov** 39:14  
Centrally on the server side until the January 1st and then it can be implemented as a separate module.

**Juan Martinez** 39:23  
Sure.

**Pavel Frolov** 39:23  
Can be implemented this different smart procedures, this card, without cards and so on.

**Juan Martinez** 39:32  
Yeah.  
Great.

**Pavel Frolov** 39:37  
Actually, as probably you remember, it was some suggestion when we discussed a mobile based access to dashboards.

**Nathan Carver** 39:38  
OK.

**Pavel Frolov** 39:52  
For the operator or for the location, one of the possible feature was to produce.  
Admin barcode. So when you log in on the mobile phone to your location, you can generate barcode, present it to the device, for example to access some special mode of operation.

**Nathan Carver** 40:11  
Mhm.

**Pavel Frolov** 40:18  
It could be set up new employee, set up new pin code.  
It will enable to create and looks quite simple procedure to how to manage access rights.

**Nathan Carver** 40:34  
1.  
OK.

**Val Levitan** 40:41  
Good.

**Nathan Carver** 40:41  
That makes sense.

**Juan Martinez** 40:45  
Yeah, I I just need to walk through that process. I mean ideally the if if we're giving somebody admin barcode that should be limited to a few people and that scenario works if you're pre setting up the point of sale devices at the at the opera.

**Pavel Frolov** 40:53  
Yeah, absolutely.

**Juan Martinez** 41:05  
Operator's warehouse or distribution point, but that operator or somebody with admin credentials may not be able to get to all of these remote locations that you know we we earlier discussed that the point of sale device.  
For lack of a better word is going to has to be hot swappable. You know how are how are you getting old settings onto the new device? If if you have to use this administrator example code, we just got to walk through that piece.

**Pavel Frolov** 41:40  
Actually administration administrational credential data, pin code or something else it it will be assigned to the location, not directly to device if one device is taken from the location and new one is installed.  
All the settings will be retrieved from the server.

**Nathan Carver** 41:59  
OK.  
Mhm.

**Pavel Frolov** 42:04  
If we if we are doing swap procedure.

**Nathan Carver** 42:06  
OK.

**Pavel Frolov** 42:09  
We already said that this procedure cannot be absolutely automatic. At least we need to to do some some confirmation.

**Juan Martinez** 42:10  
Right.  
Right.  
Right. But so, but Pavel walked me through a a brand new location with a brand new, you know, unconfigured point of sale kiosk or device.

**Nathan Carver** 42:24  
OK.

**Pavel Frolov** 42:36  
First of all, yeah, first of all, this location can be must be created on the server side by by some some person I assume on the 1st.

**Juan Martinez** 42:38  
In terms of setting it up, yeah.

**Pavel Frolov** 42:53  
First installation it will be something in at GVL.  
Who creates this locations until we create different procedures, different probably dashboards how to create this location by the operator.  
When the location created, we can create for example user admin.  
In code for this location so it will enable third party who knows this password or in code. It can login to the system.  
Server system access dashboard with this location.  
And you'll be able to enter credentials related to income, some parameters related to terminal operation and so on.  
I think in general it describes how to enable new location.  
Next, actually this person can will be able to create a pin code for cashier for example.

**Juan Martinez** 44:29  
Right. So basically Felipe's team or your team in the beginning.

**Pavel Frolov** 44:29  
Uh.  
Yes, yes. So the next question will be how to to validate procedure of swapping devices.  
So initially it's I think it can be done remotely from the dashboard as a first stage. As a second stage I would say as as I already described for example if the.

**Nathan Carver** 44:57  
Excellent.  
Looked.

**Pavel Frolov** 45:08  
Super user logged in on the mobile phone to his location, see a dashboard, enters his location name, produces a QR code.  
That enable you to manage devices on the location. Present this QR code to secure scanner on the Flex POS if it if it works again if it's not broken.

**Nathan Carver** 45:33  
Yes.  
OK.

**Juan Martinez** 45:43  
Very good.

**Pavel Frolov** 45:45  
And then it it will for example provide you to remove device from this location and if you scan this QR code on next device on new device we will be able to assign this device to this location and it will get settings.

**Nathan Carver** 45:45  
Yes.  
Thank you.

**Pavel Frolov** 46:04  
From the server and continue working as a initial device.

**Juan Martinez** 46:10  
Sure.  
OK.

**Pavel Frolov** 46:25  
Again here I think stage #1 January 1st to provide access from our server side and any improvements like offline.

**Nathan Carver** 46:33  
OK.  
OK.

**Pavel Frolov** 46:43  
Operation offline devices exchange and something like this will be next stages I think.

**Juan Martinez** 46:57  
Understood.  
Nathan, did you have anything else?

**Nathan Carver** 47:10  
Uh, no, that's it. Um, that was it on my side. Uh.

**Pavel Frolov** 47:17  
Actually, I sorry, sorry, I I just have a question to Nathan. I saw your document related to income transactions.

**Nathan Carver** 47:18  
I'll continue with the dispute. Go ahead.

**Juan Martinez** 47:20  
Go ahead, problem.

**Nathan Carver** 47:23  
8.  
Yeah.  
Yes.

**Pavel Frolov** 47:32  
Have have you had a meeting with Incombe to understand what API request will be available for us? Are we really able to to read to to get current?  
Gift card status or not?

**Nathan Carver** 47:55  
So that is in their API document.  
I'm assuming we have access to it, but there may be restrictions as to what ones we can use and our we've only had one meeting with them and that was a while back and very specifically they said these, you know, these two endpoints are what you'd be interested in.

**Pavel Frolov** 48:07  
Uh.  
Oh.  
Because.  
Because actually we already tried many of API requests, but only three of them were enabled enabled for gift cards. We need to understand that this is this is a full list of all possible cards access so.

**Nathan Carver** 48:19  
OK.  
Oh, I see.

**Pavel Frolov** 48:38  
If you want to use some endpoints, we need to confirm that it's available for our types of cards.

**Nathan Carver** 48:47  
Uh, understood.

**Juan Martinez** 48:49  
Pavel, you're you're you're looking at the GitHub integration architecture. Which specific number or pointer?

**Pavel Frolov** 48:56  
Uh one.  
Uh, one second.  
Um.  
I will share a link.  
Yes.

**Juan Martinez** 49:21  
I mean, this is the link that Nathan provided. I just put it in chat if that's where you're at.

**Pavel Frolov** 49:31  
It.  
Incom APIMG.

**Nathan Carver** 49:54  
OK.

**Pavel Frolov** 49:57  
I refer to this document.  
Actually I I see that it contains lots of data that actually not for our types of cards properly.

**Nathan Carver** 50:12  
I need to be fixed to them.

**Pavel Frolov** 50:27  
Yeah.

**Nathan Carver** 50:27  
Being, yeah, things we don't need.

**Pavel Frolov** 50:27  
OK.

**Nathan Carver** 50:31  
That makes sense.

**Pavel Frolov** 50:33  
Mhm.  
So I I think actually we need to create list of questions to income to understand probably in future in future because as you remember they provided suggested probably to use different types of cards and I anticipate.  
Probably new cards will provide us more functionalities, more features. Probably we will will be able to use them to transfer money to machines to.

**Nathan Carver** 50:57  
Mhm.  
I mean.

**Pavel Frolov** 51:12  
See current balance of the card, but not for the current gift cards.

**Nathan Carver** 51:18  
OK, that makes sense.  
Uh, that's it for me, Juan. I don't have anything else.

**Pavel Frolov** 51:40  
Yeah. Also no, no more questions.

**Nathan Carver** 51:42  
OK.

**Pavel Frolov** 51:50  
So since we lost, uh, Juan.

**Nathan Carver** 51:53  
Oh, we did. OK.

**Pavel Frolov** 52:02  
Oh, I would say that's all for for our today's meeting.

**Nathan Carver** 52:04  
Yeah, so that's it.

**Genadi Peari** 52:08  
OK.

**Nathan Carver** 52:08  
All right. Thanks everyone.

**Pavel Frolov** 52:10  
OK. Thank you. Thank you, Nathan. Thank you all. Bye. Oh, Juan.

**Nathan Carver** 52:14  
Thanks, Pavel. Oh, there's no.

**Juan Martinez** 52:18  
Sorry, my hotel decided to disconnect my Internet. I'm back.

**Pavel Frolov** 52:22  
Oh.

**Nathan Carver** 52:23  
Well, we just decided we were wrapping up since you were you were booted.

**Juan Martinez** 52:26  
Oh, OK.

**Pavel Frolov** 52:27  
Mhm.  
Yeah. OK. Thank you. Bye.

**Nathan Carver** 52:31  
So, all right.

**Juan Martinez** 52:33  
All right. Thanks, everybody. Bye, bye. See you.

**Nathan Carver** 52:34  
Alright, see ya.

**Juan Martinez** stopped transcription