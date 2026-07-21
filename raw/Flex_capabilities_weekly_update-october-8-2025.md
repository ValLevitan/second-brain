**Transcript**

October 8, 2025, 12:05PM

**Nathan Carver** started transcription

**Nathan Carver** 0:04  
Alright, let me share a doc here that I can share my screen. So this is on our communication with ACH.  
Vendors.  
Um.  
Share this.  
Make that's it.  
OK, so I dropped the link in the chat, but primarily we can start here. Kind of a vendor readiness table and these are all the vendors I've reached out to and and I have.  
Created connections with all but two. I'm still waiting to hear back on my initial contact with the the bottom two, Phoenix and Sila. Not sure how they pronounce it, but the others I've had some various levels.  
Of communication, the top four I've conversed with their salespeople very specifically. So going from Tabapay and up Tabapay is.  
Actually a really good, I think a very good potential vendor. However, they really need high volume. That's that's what they deal with. So until JVL was up to, you know, up into the 1000 to 2000 locations.  
Um, we don't really satisfy their um.  
Their product, but that's something that we could go back to in the future once once we scaled up.  
The next one, Stripe, they ACH pull, which is what our product will do. We're gonna create, we're gonna initiate ACH transactions to pull funds from a location as opposed to the customer initiating.  
A payment on their side and and and pushing money to JVL. So that is outside Stripe's normal.  
normal product, but that's something that they're going to evaluate and look at what they can do for us. So still waiting to hear back from from their sales team if they can support our use case. The top two, Duala, Modern Treasury, both of them support our use case.  
Case very well between the two Duwallas ready to go, they can. In fact, they could put a team together and help us get set up in the next few months.  
Then Modern Treasury, the one thing that would they would need from us is to reach out to our bank. So the difference between Modern Treasury and Dowalla is Dowalla is a full support. They they basically they move the money for us, they set up the the accounts.  
And they they do everything. We initiate transactions through their API, but Duala handles the rest. Modern Treasury is a just a SAS, a software service. So they they create a an API to our existing.  
Bank, which I believe is Bank of America, and so they provide access to more easily initiate ACH transactions through their API as opposed to having to log into the Bank of America portal, initiate transactions 1 by 1.  
So the difference between the two is Dwala is is a bit of a middle middle man in the process and the flow of money, and Modern Treasury is not in the middle. It's just strictly.  
The location's bank account to JVL's bank account and Modern Treasury is just a way, an easy way for us to to initiate those transactions.

**Val Levitan** 4:22  
But that means modern treasury must be considerably cheaper.

**Nathan Carver** 4:28  
Not really. So well, how that how they turn out is let me see what we have here. So at the top I did a scale comparison here and.  
Dualis still does much better at scale than Modern Treasury. They're pretty close.  
As far as when we're if we're in our pilot at 10 locations, Modern Treasury has a flat fee of about around $6000 a month for their service and then Bank of America would charge us for the ACH.  
Transactions. So in order for us to optimize pricing, we really would have to negotiate good terms with Bank of America and try to negotiate some better terms with Bonner Treasury. So we would have two points to negotiate with.  
Um.  
Whereas Dualla, we're just negotiating with the single vendor and they because they as they control everything. The unknown is Stripe. So Stripe has a flat fee for ACH polls of 1.5% which is.  
Pretty high. So unless they cap that, which I don't know if they can yet because I'm still waiting to hear back, they're really cheap for a pilot rollout. We're looking at 1600 a month as opposed to, you know, over 5000 a month for Dualla and Modern Treasury.  
But as soon as we hit high number, high volume, Stripe will become really expensive. So that's still open negotiation we would need to do with them. If they don't cap it, Stripe is just unreasonable at scale.  
Where Duwalla and Modern Treasury become Duwalla becomes the the most, you know, priced, cost-effective at scale with these three so far.

**Val Levitan** 6:32  
Sorry, you're in parentheses for each of the vendors. You have 500 per location and what is it $500 per location per month or?

**Nathan Carver** 6:33  
The.  
Correct. That's kind of how it would, yeah, it's just splitting it out what the cost per location would be. So if we were to try to recover the cost, that's how much it would be, correct?

**Val Levitan** 6:52  
And it it goes down.  
It goes down to $10 and eventually $7.00 per location per month.

**Nathan Carver** 7:01  
Correct.

**Val Levitan** 7:03  
This is what this is their I I mean this is their platform fee.

**Nathan Carver** 7:12  
Yes, so the I count I had Claude calculate the platform fee using de Wallace quote. So at 10,000 locations we're looking at a minimum of 5000 a month.  
And it could go up, but with just 10 locations, we're not really going to generate that many transactions estimations. As you can see, as we get to 500 locations, there's not a whole lot of change.  
With Duala because they're going to charge a minimum of $2500 for transactions. So if you don't spend over that $2500, that's the minimum they charge. But as you once you break that barrier, then it starts going up incrementally. That's what we see here at the.  
500 locations.  
And then the 2000 locations is, you know, roughly 13,000. So I had with Modern Treasury cause I don't know what Bank of America's cost is gonna be. I I just had, I had Claude go out and look for.  
What it could find for Bank America costs and there's going to be some variation because of the the volume that we have in some. So these are just estimates of what it could be. We wouldn't, we wouldn't know until we actually.  
Talk with the bank and what their what their costs are going to be, but we still have the flat rate regardless with Modern Treasury of 6000 regardless of our negotiations with the bank.  
So with so far the unknown, Duwalla has the fewest unknowns so far. I think we're we're pretty solid understanding of their pricing.  
And this is using same day ACH processing, which is obviously we're gonna get it within 24 hours, but it's still limited to.  
Not running business days. So we wouldn't be able to draw on a Saturday or Sunday with this. We would still need to negotiate with them their what's called Fed now I believe it's like an immediate transaction provided by the.  
Um, Federal Reserve.

**Val Levitan** 9:42  
Explain that. I don't get that.

**Nathan Carver** 9:45  
So there's a a a product called Fed Now and I believe this is something offered by the Federal Reserve that I needed. I was going to start looking into and it's basically an instant payment service.  
That the Federal Reserve offers and I believe, I think Duala can facilitate this, but we may also be able to go directly through another provider of what this. So I I I just kind of discovered it yesterday in some of my conversations.  
So I need to dig into what this service is.  
Um, but essentially it's supposed to be, you know.  
24 hours a day, seven days a week type of transaction service.  
And here's the Yeah, OK, here it is. I'm gonna drop the link to this.  
Um.  
So that's where. So the next steps would be we, you know, we always have, I think Tuala is ready to go. We could always.  
Start that with them.  
The if we want to with Modern Treasury, if we want to go forward with that, I could reach out to Bank of America and try that understanding what their costs are going to be and how that might work for JBL. And then I'm still waiting to hear back from Stripe. They said they would probably they could get back to me early.  
Early next week with with their um their answer on the ability to support our product.  
And then I'm gonna go down to.  
And I'm still waiting to hear to create an established communication with the the bottom 4 vendors here.  
I did hear back from Move in the sense they're asking us for our for JVL's EIN, which.  
Seems a little strange for me, so I don't. I don't know if if we wanna share that with them or not, but I would in order to move forward with move I would need to. I would need JV LS to give them JV LS EIN.  
It must be their way of verifying that we're a real entity.

**Val Levitan** 12:43  
E.

**Nathan Carver** 12:52  
OK, so that'll be my next steps is understanding Stripe and then.  
Getting, uh, more conversations with these with these other vendors.

**Val Levitan** 13:06  
This looks, uh, incredibly inexpensive.

**Nathan Carver** 13:15  
And ex.

**Val Levitan** 13:15  
FedNow FedNow looks incredibly inexpensive.

**Nathan Carver** 13:23  
Let's go look at this.

**Val Levitan** 13:25  
Take a look at the table I just provided.

**Nathan Carver** 13:28  
OK.

**Val Levitan** 13:35  
The fees of $25 has been waived, so it's zero and it's only transactional fee of.  
Half a cent.

**Nathan Carver** 13:47  
Oh, I see.

**Val Levitan** 13:52  
It's half a cent.  
It's half a cent per transaction.

**Nathan Carver** 14:06  
It's really cheap.

**Val Levitan** 14:10  
Should look into it.

**Nathan Carver** 14:14  
So this is a brand new 2025 service.

**Val Levitan** 14:17  
No, it's 20. No, it's 2023. The service is now this 2023, but this is 25 summary.

**Nathan Carver** 14:21  
Oh, 2020.  
Got it.

**Val Levitan** 14:27  
And the $25 fee has been waived in 2025.  
So just really hot off the press.

**Nathan Carver** 14:38  
OK, yeah, we'll dive into this.

**Val Levitan** 14:38  
This is, this is, this is the winner and and they provide services to.  
Two individuals.  
So here I'll show you.

**Nathan Carver** 14:56  
Yeah, it's OK.

**Val Levitan** 15:11  
The service provides interbank clearing and settlement that enables fund to be transferred from account to a sender to the account of the receiver in near real time and at any time, any day of the year.

**Nathan Carver** 15:29  
Excellent.  
OK, good.

**Val Levitan** 15:40  
They have fraud provincial tool.

**Nathan Carver** 15:45  
OK, so we need to dig into this and.

**Val Levitan** 15:49  
That desperately this is this is a good one. This is a good one.

**Nathan Carver** 15:50  
Yep, this is good.

**Pavel Frolov** 15:53  
Perfect.

**Val Levitan** 15:54  
This is really a good one.

**Nathan Carver** 15:58  
Good.

**Val Levitan** 16:01  
I like this one.  
Um, let's see their API.  
Must be on their website.

**Pavel Frolov** 16:40  
And we still need to understand a use case in case when they try to charge some accounts and not enough money from this.

**Nathan Carver** 16:53  
NSF Yeah. Um.

**Pavel Frolov** 16:57  
OK.

**Nathan Carver** 17:19  
OK, so it looks like we have to go through the bank.

**Val Levitan** 17:22  
Yeah, I'm reading that one second, please.  
I think you could build the they call it Fedline connection to go through a certified third party.

**Nathan Carver** 18:36  
Mhm.

**Val Levitan** 18:45  
You gotta dig into it.

**Nathan Carver** 18:48  
Yeah, I'm gonna. I'll dig into this.

**Val Levitan** 18:52  
Yeah, this this one is interesting here posted.

**Nathan Carver** 18:59  
OK.

**Val Levitan** 19:12  
Well, I mean, it's understandable. They require a deposit or institution. So you know, you cannot put the money into your pocket.

**Nathan Carver** 19:23  
Correct.

**Val Levitan** 19:25  
So yeah, I understand this.  
Playing that.  
They also have Fed ACH.  
Basically, it's a private Internet between banks and the Fed.

**Nathan Carver** 20:17  
OK.

**Val Levitan** 21:24  
You cannot connect to it. You need to be um.  
Regulated financial institution or credit union.  
OK, um, yeah, let's let's dig into it.

**Nathan Carver** 22:17  
OK.

**Val Levitan** 22:18  
It may or may not be available to private sector. I don't know. I leaving it up to you to dig at it to dig into it.

**Nathan Carver** 22:27  
OK, I'm gonna start doing that and also look at.  
OK. Going through vendors, going through the bank directly. I'll dig into that. OK, sounds good.  
OK, so that that's where I am right now working with this and um.  
So I'll dive into Fed now and then still I wanna get that use case, the failure mode use case for for pavel. Some of that will depend on the API we use, but I think in general we we can have.  
I'm just gonna use uh duala's API as as a guideline for how.

**Val Levitan** 23:29  
Yeah, let's start. Let's start digging into, uh, Duwalla.

**Nathan Carver** 23:30  
The services would work.

**Val Levitan** 23:36  
And let's start putting Dwala API on development path.

**Nathan Carver** 23:43  
OK, we can do that.

**Val Levitan** 23:45  
Um.  
So I would like to see Tenjira plans. Of course, it's my only instrument of truth.

**Nathan Carver** 23:51  
Mhm.

**Val Levitan** 23:55  
So between Pavel and Nathan, can you please undertake to schedule dual integration and reflect it in Jira plans for our next meeting?

**Pavel Frolov** 24:09  
OK, OK.

**Nathan Carver** 24:10  
OK, Yep, we can do that.

**Val Levitan** 24:11  
And for Nathan, please.  
Undertake the responsibility for digging further into Fed now.

**Nathan Carver** 24:22  
Alright, I'll do that as well.

**Val Levitan** 24:24  
All right, let's discuss. And I don't know if this was on the agenda today or not, but and I don't know if it's possible, but do we need to discuss anything about architecture and?  
Uh, selection of Uh text tag.

**Nathan Carver** 24:50  
Uh, there's nothing on my side as of right now. Um. I'm looking at very simple uh job schedulers. Um.  
Which I think Spring Boot offers up and I and I believe that's in the tech stack. Is that correct, Pavel? That's already in the tech stack, OK.

**Pavel Frolov** 25:08  
Yeah, yeah.

**Nathan Carver** 25:12  
So the stuff I'm looking at is already provided in the tech stack that we have.

**Pavel Frolov** 25:12  
Java Plus.

**Val Levitan** 25:23  
One second, please.  
So the schedule will go under IP632 which is payment hub, am I correct?  
And right now it's broken into, well, a number of features here 123456789 features.  
And it actually is scheduled quite a bit to the the first week of December. Is this still true?  
Because I I don't know where.  
Well, I see the under BEP.  
2656 ACH API adapter. I assume this is where Duala will fit.

**Pavel Frolov** 26:20  
Correct.

**Val Levitan** 26:23  
And the IT it seems like the integration is quite short.  
It's actually only two weeks.

**Pavel Frolov** 26:34  
Yes, yes, yes.

**Val Levitan** 26:35  
And it will finish finish 12 of November. Am I looking at the right thing here?

**Nathan Carver** 26:36  
Yes.

**Pavel Frolov** 26:42  
Yes, the right thing, but it's not estimated fair enough because we do not read through the Voila API documentation, just a rough.

**Nathan Carver** 26:43  
Yes.

**Pavel Frolov** 26:58  
Numbers.

**Val Levitan** 27:01  
Correct. Correct. OK. So let's dive into it a little bit more in the next meeting.

**Pavel Frolov** 27:09  
Yes.

**Nathan Carver** 27:10  
All right, sounds good.

**Val Levitan** 27:12  
OK, then that's it for me.

**Pavel Frolov** 27:15  
Yeah.

**Val Levitan** 27:16  
Nathan, please send the recording for the benefit of Juan and whoever wants to use it. Put it into into this chat please.

**Nathan Carver** 27:28  
All right, will do.

**Val Levitan** 27:30  
Thank you very much. I appreciate everybody's time. Bye, bye.

**Nathan Carver** 27:31  
Thanks everyone. See ya.

**Pavel Frolov** 27:31  
Yep.

**Nathan Carver** stopped transcription