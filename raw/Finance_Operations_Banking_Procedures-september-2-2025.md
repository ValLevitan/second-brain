**Transcript**

September 5, 2025, 6:04PM

**Lev Rudky** started transcription

**Alka Sood** 0:04  
It started, yeah.

**Val Levitan** 0:05  
That started. Yeah. OK, good.

**Alka Sood** 0:08  
OK, so um what? OK, so let's back up. There's two sides to the banking. OK, the first thing is what is actually happening within the bank. That is us going in, arranging payments, transferring money back and forth. So that's a a direct in the bank account.  
banking activity. So in terms of the software like Navision or Business Central, there's not a lot that really happens in terms of banking other than we will get a list of every transaction that is affected in the bank.  
And we make sure that we post it or we record it in the system manually. We literally will say, oh, $20,000 got moved from one account to the other. So either it's mostly Chris. Chris will then record in Navision or Business Central that money was transferred.  
OK.

**Lev Rudky** 1:09  
So Chris does related postings in the ERP system, right?

**Alka Sood** 1:10  
In the.  
Right. And it's mostly Chris. I'd say it's all Chris. Actually, it's all Chris.

**Lev Rudky** 1:22  
OK, who who will be doing purchase invoices in the system?

**Alka Sood** 1:31  
All right, now here's what I would want to understand. OK, when Mikkel decides to buy something, does he not go into the system and create a purchase order?

**Lev Rudky** 1:40  
Correct. Yeah, he does.

**Alka Sood** 1:42  
So it would be somebody whoever is making the purchase or authorizing the purchase would need to create that purchase.

**Lev Rudky** 1:50  
Yeah, he creates the purchase order, right? But but then at some point purchase invoice needs to be issued.

**Alka Sood** 1:53  
Correct.  
Right. So then the then a vendor will issue a an invoice once they have delivered the goods and services and then we set up the invoice for payment. But but first step, if there is a PO, then Val obviously has to approve that PO and that basically opens up the gate for us to accept an invoice.

**Lev Rudky** 2:20  
Yes, yeah. No, no, no issues with that. OK, go ahead.

**Alka Sood** 2:20  
OK, so.  
Right.  
OK. And then the vendor will send an invoice and we will accumulate the invoices or the payments that are due in the current week and we will send Val a list on Monday morning saying these are all the payments that we have to release from the bank that are due this week.  
And that's again done with an extraction from the system and and perhaps there's some late flying in items that have come in through AP. We want to make sure it's current and we send him a payment proposal.  
Now all those transactions that are those invoices that come in from vendors are entered by Chris. OK.

**Lev Rudky** 3:09  
That's what I So this is Chris.

**Alka Sood** 3:15  
Yeah, she she then sets up the payment request. Val approves the payment request. OK, I I want to go through this really slowly. He approves it saying yes, I'm willing to pay these three invoices on this whole payment schedule. OK.

**Lev Rudky** 3:15  
OK.

**Alka Sood** 3:32  
That basically gives Chris the authorization to set up payments or send a file up to the bank to say we're going to pay these three invoices and we want to withdraw the money from the account. After that, Monica releases the funds.  
looks at that request and she goes, Yes, I'm going to release the funds. So it gets sent up there. In the meantime, Chris will then post in Nav Vision or Business Central that these invoices have been earmarked for payment.  
So she records it as paid. Okay.  
After that, Chris, Chris will do that all up to there, she'll do that. After that, Laura, who's new at this right now, but Laura, once a month, will read the banking statement and validate that all the payments were recording according  
to the bank statements. She's going to use the legal document that is issued by the bank, a bank statement and say, Yep, Yep, Yep, Yep, Yep. Oh, we missed one. This went out, but we have no invoice. What happened? Yep, Yep, Yep. Oh, we missed one. And that is what she is supposed to check for.  
OK.  
When that happens, OK.

**Lev Rudky** 4:53  
Oh.  
Yeah, so basically, uh, Greece.  
Performs the transactions in the system and validates the reconciles the statement, right? Yeah, she audited. OK.

**Alka Sood** 5:08  
And Laura audits it.  
She audits it right.  
Yeah.

**Lev Rudky** 5:24  
I'm asking all of this because of it has to do. It has to do with permissions assignment.

**Alka Sood** 5:27  
Totally fine.  
Totally fine. Totally fine.

**Lev Rudky** 5:36  
OK, so who posts the payment journal?

**Alka Sood** 5:46  
Chris.  
I need a different person that posts the payment journal from the person that audits it.

**Lev Rudky** 6:05  
Yeah, this is basically now what I wanted to know now. So you're saying when?

**Alka Sood** 6:11  
Yeah.

**Lev Rudky** 6:17  
Bank payment is erformed.

**Alka Sood** 6:21  
Yeah.

**Lev Rudky** 6:22  
The physical operation does it reference?

**Alka Sood** 6:27  
Yep.

**Lev Rudky** 6:31  
Invoices or.  
Purchase. Purchase is definitely not, but invoices.

**Alka Sood** 6:37  
No, it the bank. The bank transaction doesn't reference that. But what we have is when we do a banking transaction, we will get a confirmation number, or we call an ACH number.  
And they are instructed to write that ACH number in the memo.  
In in the in the memo in the memo field saying that we did this ACH, we've transferred this is their confirmation or the ACH reference that we have that it went out on the bank and they're they're they're supposed to put in the memo, OK and then we have that reference point.

**Lev Rudky** 6:59  
In the.  
On.

**Alka Sood** 7:14  
But there's no um.

**Lev Rudky** 7:16  
I understand. So it's basically prior to posting there is a reference number populated in the system, right? Reference number obtained.

**Alka Sood** 7:31  
There should be. I I haven't gone down that level of detail or double check this because reconciliations is my baby for next month. But I want to make sure all that traceability is there so we can always go back and find it. OK, that is the intention.

**Lev Rudky** 7:32  
From.  
Oh.  
Who actually?  
Releases funds from the bank. It's it's it's not Chris, it's not Laura, it's not you, right? So she interacts directly with the bank and I'll have.

**Alka Sood** 8:00  
It's Monica. It is Monica.

**Lev Rudky** 8:10  
To find out with her what?  
What references, if any, are provided during transaction?

**Alka Sood** 8:21  
Yeah, I I I can send you a sample of what Chris sends Monica for wire payments. Monica wants to see the invoice for the ACH payments. She's usually got the payment schedule with all the details that we write in the payments that.  
These are getting processed, but I can get Chris to send you a sample of the instructions 'cause she did one last night to to you to show you how we how we communicate with Monica.

**Lev Rudky** 8:57  
So Chris will send me the samples and the.  
The process is the same for both systems, I assume.

**Alka Sood** 9:11  
We want exactly the same process for both systems. For systems, we have a different bank account. It's a Bank of America, right?

**Lev Rudky** 9:20  
Yeah, yeah, I know.

**Alka Sood** 9:21  
It is not as friendly as RBC because poor Ina gets a list of all the payments and she issues them manually out every time she gets a list. And so far we don't have a lot, but over time she's going to get more and more and more, so we need to be able to do batch.  
Batch payments once things migrate over.  
But Ina is the one that releases funds and transfers funds out of Beaufort RBC. Ina has that that authorization.

**Lev Rudky** 9:56  
OK.  
OK, so everything regarding.  
Variables on the ERP side.  
Is done by Chris as per comment.

**Alka Sood** 10:18  
We're gonna Yeah, because she's gonna does everything. She's the AP Clerk.

**Lev Rudky** 10:24  
OK, that basically this is what I wanted to know. I'll I'll prob. I'll probably.

**Alka Sood** 10:31  
OK, no problem.

**Lev Rudky** 10:36  
So.  
Direct in case of RBC.  
Direct bank interaction, like releasing the payments, is done by Monica.

**Alka Sood** 10:52  
But setting up the payments is done by Chris.

**Lev Rudky** 10:57  
Yeah, I I I do like that. I'm familiar with that. But physical bank, I'm just, I just want to find out. No, I I just want reference wise like what reference is going to.

**Alka Sood** 11:06  
Control wise, Monica releases. Yeah, control wise Monica.

**Lev Rudky** 11:15  
Interruptual bank transaction, yeah.

**Alka Sood** 11:19  
Yeah, I'll I'll send you a sample of the payment instructions that Chris sent Monica last night. I'll get her to send that the recent version to you and really that's what Monica uses. And with wires, what Chris will do is set up the wire. She'll set it all up on A and she'll take a picture of it and she attaches the invoice and then she sends a note to Monica to say.  
This wire must be released, so Monica looks at the wire, she looks at the invoice, does her own match, and off it goes.

**Lev Rudky** 11:47  
You know, but off it goes, whatever goes out. The thing is, I just curious what references are included in this out of the book.

**Alka Sood** 11:59  
It's usually the invoice number. It's usually the invoice number, the amount, you know all of that is in there, the name, who it is from, all that stuff.

**Lev Rudky** 12:03  
Yeah, yeah. So basically what I need is basically only invoice number like to make sure that it goes out.

**Val Levitan** 12:15  
May I may I suggest that even if we have a certain process right now?  
Let's look at it carefully because it would be helpful for everyone involved in this circle.  
To rely strictly on capabilities, standard capabilities of Business Central as we're moving away from.  
Um, my vision.  
And more and more into Business Central, it would be nice to have these native capabilities rather than circulating a foreign application as an attachment or something else.

**Alka Sood** 12:58  
I agree.  
I totally agree. So ideally for me, Val, what I would love for you to do is get a one Monday morning for you to get a link to say please authorize the following disbursements that we have scheduled. OK, then you will from coming from Business Central, right? Just a link.

**Val Levitan** 13:16  
And also and also.  
Yeah. And also and also if I could comment within Business Central, that would be very helpful.

**Alka Sood** 13:24  
Bingo. Exactly. So yes, I authorize. Hey, I want more information, not authorized. Whatever you do, you write your your conversation in there and then and then you press submit. And let's say there were 10 payments and you authorized 3. So then the three that are authorized for payments say now these are teed up.  
your disbursement. And then Monica gets a link that says these three invoices. Once Chris has set them up in the bank, she says these are teed off for disbursement. She gets another link. Here's my link and the link can go back and you can drill down and get the invoice number. Perfect world, right?  
And then Monica goes, yeah, here's my link. Check, check, check, authorize. OK, so that would be the perfect world.

**Val Levitan** 14:06  
Um.  
And I also would like to make one comment. I didn't want to interrupt you, but I mean as we're moving away from the primary subject, when the purchase order was issued, we went into, we went into sales invoices immediately, but actually there is a.

**Alka Sood** 14:18  
Same thing.

**Val Levitan** 14:26  
Intermittent step in between, which is a receipt, a receipt of goods, and that's an that's an important step because this is where the count takes place.

**Alka Sood** 14:34  
Correct.

**Val Levitan** 14:41  
Or count verification. Well, we don't count all the time, but if the count is different then the expectation on the vendor's invoice would be different as well and so that that would influence posting.

**Alka Sood** 14:42  
Yes.  
Yes, exactly.  
Exactly. For me it is. We're going to reject this invoice doesn't match the PO.

**Val Levitan** 15:02  
No, doesn't match the doesn't match the receipt.

**Alka Sood** 15:03  
Or the receipt. And by the way, we also match. It's a three-way match. We call it the fancy three-way match. You match the PO to the bill of lading or the packing slip to the invoice. You want the three-way match to go.

**Lev Rudky** 15:04  
Yeah.  
Yeah.

**Val Levitan** 15:10  
Yes.

**Alka Sood** 15:18  
Perfect. If there's a dispute, then he said this is being disputed, and if it's a dispute, then it goes to the authorizer of the PO and said we're we're disputing this invoice. Please deal with the vendor.

**Val Levitan** 15:26  
And.

**Alka Sood** 15:33  
Like Mikel, hey, the invoice didn't match. The receipt didn't match the PO. Please deal with the vendor.

**Val Levitan** 15:39  
Yeah, or price doesn't match or quantity don't match, whatever it is here.

**Alka Sood** 15:40  
And.  
Whatever the aspects are, right? Or there were five defective goods in here.

**Lev Rudky** 15:49  
I I just want to comment that technically you cannot. If there is a PO, you cannot.

**Alka Sood** 15:51  
OK.

**Lev Rudky** 16:04  
Invoice anything that hasn't been received.

**Val Levitan** 16:10  
No, but it could be received. But yeah, what if it's not complete?

**Alka Sood** 16:10  
Correct. But what if it's a partial shipment?  
What if it's a partial shipment?

**Lev Rudky** 16:15  
It's part. No, it's partial receipt. You received 20 out of 100. You can invoice only 20 out of.

**Val Levitan** 16:23  
Oh, I see. You won't be. You won't be able to enter the amount that exceeds the receipt. Wonderful, right? Yeah.

**Lev Rudky** 16:30  
Yeah, so so the system will not allow it.

**Alka Sood** 16:32  
See and see.  
So in in in the way I I've set these up elsewhere is you got the PO that says 10 units at $10, right? In comes the goods Arcadia or whomever would have no visibility on the price but would say.  
And no visibility on what's expected. We'll just say I received 8.  
He doesn't know that we're expecting 10.  
And then he gets a notification, hey, you received eight, there's two back ordered. Do you agree? Yes. So we've got to kind of really map that out properly so that we know what what you know how we want to process it up. That's all the workflow.

**Lev Rudky** 17:16  
Well, basically.  
He cannot.  
He cannot receive.  
He cannot receive anything.  
Exceeding the price on the purchase order, exceeding unit price on on the.

**Val Levitan** 17:42  
He's not. He's not. He's not exposed to a price. He's only exposed to a quantity.

**Lev Rudky** 17:48  
Yeah.  
That's on the packing list. He actually he works with a purchase order and on the purchase order he sees he receives into purchase order whatever he receives and on the.

**Alka Sood** 17:51  
Yeah.

**Val Levitan** 17:53  
And the.  
He he he actually shouldn't be exposed to a purchase order. Should also he should only be exposed to to a quantity.

**Alka Sood** 18:08  
He should be big.  
Correct.  
That's that might make sense cause you know, like you don't want him to be like looking at the price of the good of the whole, cause you could mush the numbers together to get the right price but not get the quantity that you're looking for.

**Val Levitan** 18:28  
No, but that's also confidential information. You don't want anybody to know that.

**Lev Rudky** 18:29  
Yeah.

**Alka Sood** 18:31  
Yeah.  
Correct, correct.

**Lev Rudky** 18:34  
Well.  
The way it works now, he works with purchase order and sees everything in the purchase order and he cannot. He can.

**Val Levitan** 18:47  
I know, I know. But we're setting up, we're setting up, uh, new stuff, right? So.

**Lev Rudky** 18:51  
Yeah, but whatever I hear now, it's uh.  
Oh, should they?  
With it he receives.

**Val Levitan** 19:08  
It.  
Whatever you hear now is what, a new requirement or?

**Lev Rudky** 19:10  
It's a completely new requirement. It's it's if.

**Alka Sood** 19:16  
Well,

**Val Levitan** 19:20  
I I would say, I I would say that we didn't set it up correctly, you know, 30 years ago.

**Lev Rudky** 19:23  
Uh.

**Alka Sood** 19:26  
Is it? Is my question. Is it? Is my question because the receiver should have a different screen that says the receiver screen should look like everything with quantities and PO number but nothing else.  
And what that receiver screen or that user interface says, I'm going to go back to the PO, but I'm only going to populate part of the data, so the receiver is only going to see the quantities.  
Or even the quantities. I don't want him to see the quantities ideally, so that I know that it's done with integrity because it's very what we have found is that if we tell people they're expecting 8, they won't count them. They go, yeah, we got 8.

**Lev Rudky** 20:08  
This I understand this point.  
It.  
But.

**Val Levitan** 20:14  
That's that's actually an excellent point. I never thought about it this way.

**Lev Rudky** 20:19  
So.  
I may be.  
I can hide.  
The price.

**Alka Sood** 20:30  
You hide part of the data, absolutely.

**Lev Rudky** 20:32  
Yeah, but.

**Alka Sood** 20:38  
Or you hide the data and the quantity and you get an error message.

**Val Levitan** 20:39  
And I'll.  
And I and I'll and I'll tell you something interesting that now that we're moving away from Toronto, it's the most perfect time for us to instill new rules. It's really very nice.

**Alka Sood** 20:53  
Correct.  
Correct.

**Lev Rudky** 20:57  
OK, I will look into it.

**Alka Sood** 21:01  
I think it's a user screen more than anything. Lab is a receiver. You label the profile as a receiver and they have a special screen to receive and all they do is get the PO number and they enter the quantities and the system says hey, we're back ordered for or hey.

**Lev Rudky** 21:05  
Uh.

**Alka Sood** 21:16  
We we didn't get the quantities and some there's an alert that has to go up somewhere. Something has to happen.

**Lev Rudky** 21:21  
Well, we.  
We receive.  
In stages sometimes, right? So the alerts are normal, but if we.

**Alka Sood** 21:34  
Mm-hmm. Yep.

**Lev Rudky** 21:45  
I I I don't see.

**Alka Sood** 21:48  
I see a problem.

**Lev Rudky** 21:48  
I see a problem with, let's say normally something that arrives in a regional manufacturer's packaging.  
It doesn't in in what?

**Alka Sood** 22:02  
I I see a problem.  
Well, the packing slip, if the packing slip says, I mean the a vendor should say listen, you ordered 100, we've sent you 8020 are on route and the expected delivery date is a month from now. All of that is really critical information says all right, we've got 80 out of the 100, so we're going to accept this, we're going to accept an invoice for.  
80 units.

**Lev Rudky** 22:28  
Yeah, let us how it works now.

**Alka Sood** 22:30  
And and 20 are back ordered, and the expected delivery date for the back ordered, or why? But I feel that the vendor invoice or the vendor packing slip should provide all that information. and if it doesn't, then we have to train our vendors if you're short short shipping us.  
You better indicate when the back order is going to be completed.

**Val Levitan** 22:52  
It's a very valid comment.

**Alka Sood** 22:55  
I'm just talking about control, right, Val?

**Val Levitan** 23:00  
No, it's a very, very valid comment.

**Lev Rudky** 23:04  
OK.

**Alka Sood** 23:04  
And if two are damaged, what's happened? What What happens if they send 10 and eight are in good shape and two are in bad shape? Hey, two of these are damaged. We're only going to accept 8. Invoice must be for eight. Give us restitution for two. Tell us what to do with them. Either send two more or reduce your invoice.  
I mean, we have to have some kind of control.

**Lev Rudky** 23:26  
Well, I said before, you cannot pay more than you received, right? It's no restitutions there because it's not being paid.

**Alka Sood** 23:36  
I'm talking about 882 damaged. I received 10.

**Lev Rudky** 23:39  
Too damaged. It's if if you get damaged parts, it's.

**Alka Sood** 23:41  
I've technically only received 8.

**Lev Rudky** 23:49  
It's uh.  
Separate story how how to deal with them. It's not something that happens very, very often.

**Alka Sood** 23:52  
OK.  
But I can. I can sit and map all those. Yeah, I can sit and map out all those processes for you. I think I've done it once before. I'll certainly share that again with you if you'd like, and we can take it from there. That's no problem.

**Lev Rudky** 24:00  
Eat.  
Just a second.

**Alka Sood** 24:23  
I actually have a hard stop at 2:30. Just giving you a heads up, OK?

**Lev Rudky** 24:27  
So OK, I basically I got I received what I needed to receive now.

**Alka Sood** 24:35  
OK, perfect. And I'll get Chris to send you the sample of what reference information is given a sample of of the things, OK.

**Lev Rudky** 24:42  
OK, OK.

**Alka Sood** 24:43  
Okay, perfect. Anytime, feel free to reach out.

**Lev Rudky** 24:46  
No.  
OK. OK. Thank you.

**Alka Sood** 24:50  
Bye.

**Lev Rudky** 24:51  
Hi.

**Lev Rudky** stopped transcription