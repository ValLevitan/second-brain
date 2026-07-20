**Transcript**

August 27, 2025, 12:02PM

**Juan Martinez** started transcription

**Nathan Carver** 0:03  
That's that's where I see this can be helpful if we bring these questions to quickly.  
To review and then we can identify what would be good exception use cases to pick up and then I can start.

**Juan Martinez** 0:18  
OK.

**Nathan Carver** 0:22  
Uh, wiring up requirements and then getting those into JIRA for final review.

**Juan Martinez** 0:29  
Sure.  
OK. I will also send you some use cases, Nathan, this weekend. Hey, Will, good morning when I have some time and I will also work on the ACH contracts that we need to to handle the payments.

**Will Jones** 0:38  
Hey, good morning.

**Pavel Frolov** 0:39  
Good morning.

**Nathan Carver** 0:42  
Hello.

**Juan Martinez** 0:47  
And the wire transfer of funds.

**Nathan Carver** 0:51  
OK.

**Pavel Frolov** 0:52  
Yeah.

**Nathan Carver** 0:53  
Now that's on the, those are contracts on the location owner operator side, correct?

**Juan Martinez** 0:59  
Either or it would be either with the master if if they're going to be paying us the fees or if it the location is going to be paying us. There's two, there's the two scenarios where we enter into a contract with the location or with the master.

**Nathan Carver** 1:04  
Hmm.  
Right.  
So, so I have two questions in that regard. One, I know I don't know if we've decided on an ACH platform yet. I've used Stripe as the example platform in the use case, but I'm not making the assumption that's what we're using it. It just seemed like a good model to follow.

**Juan Martinez** 1:29  
Is it?

**Nathan Carver** 1:36  
For at least for the use cases.

**Juan Martinez** 1:38  
Sure. Is there anything you could share web page or whatever? I do not believe that we we obviously have not selected an ACH provider. You know, my thought would be we we bounce some ideas off income and see if they give us their top three that they've ever dealt.

**Pavel Frolov** 1:38  
Mhm.

**Nathan Carver** 1:47  
OK.

**Juan Martinez** 1:57  
With they just most likely have to do business in Georgia, although ACH is a wireless transaction that can be done anywhere. I, you know, I just think it's a as long as we know that they work in Georgia that that might be a little better for us.

**Nathan Carver** 2:12  
Yeah, OK. I can at least put together the stuff for Stripe. It seems to me what would be important to JVL is obviously transaction fees, but the speed at which we can verify an account and if we can verify without having to do.

**Pavel Frolov** 2:16  
OK.

**Juan Martinez** 2:27  
Yes.

**Nathan Carver** 2:30  
You know, a microtransaction, or if we need to do a microtransaction, which from what I understand is going to take a little longer to verify.

**Juan Martinez** 2:41  
And and you're saying when we we transmit a one cent, three cents and or OK.

**Nathan Carver** 2:47  
Correct. Yeah, I believe Stripe will do both so they can verify without a microtransaction, but they can also fall back to the microtransaction. So it may be good if there's any other criteria that's important to JBL. Those are the two that I could think of.

**Juan Martinez** 2:58  
OK.

**Nathan Carver** 3:07  
Fees and the speed at which we can verify, but maybe there's some other attack that each one can offer that would be, you know, more or less beneficial for JVL. We can consider those too.

**Juan Martinez** 3:21  
Sure.

**Will Jones** 3:21  
But um, if I can ask just what's the use case for the verification?

**Nathan Carver** 3:22  
E.  
So in the location onboarding and payment setup.

**Will Jones** 3:33  
Mhm.

**Nathan Carver** 3:35  
I can pull that up real quick.  
Um, so actually, do you have? I can pull it up in GitHub. Do you have access to GitHub? Uh, Will?

**Will Jones** 3:49  
Certain certain repos. There was one that somebody had sent that I don't and I needed to respond back, but I have access to.  
Why don't I see him again?  
I just need to resign in.

**Nathan Carver** 4:06  
OK, let me, um, let me share this.

**Will Jones** 4:12  
So CMS core, remote setup, CMS front end, payflex, CMS client installations, proto server, scanner, CMS, CAS, Passport and RGS data importer. I also have one more that I don't see on this list.

**Nathan Carver** 4:29  
OK.

**Juan Martinez** 4:29  
Yeah, I didn't hear you say flex POS Will so.

**Will Jones** 4:30  
Which?

**Nathan Carver** 4:34  
OK, yeah, the Flex POS specifically, that's where we started putting this documentation and it kind of stuck there. So we may just need to make sure you have access to that one.

**Will Jones** 4:46  
Yep, that's correct. I do not have Flex POS. I can't see that one. I have Flex Pay Communicator, but not Flex POS. Is that Andre? Is that the person I should send to?

**Nathan Carver** 4:50  
OK.

**Juan Martinez** 4:58  
Yes.

**Pavel Frolov** 4:58  
Yeah, actually, I will. I will ask him right now.

**Nathan Carver** 4:59  
Yeah.

**Will Jones** 5:02  
OK. Thank you.

**Nathan Carver** 5:06  
Yeah, so here is. So there's a use case in here, the location onboarding and set up and I have a just in step two. It takes the user through banking information.  
And so Stripe has the an API that enables us to do instant verification, but that's gonna require them to.

**Juan Martinez** 5:25  
It.

**Nathan Carver** 5:34  
Uh, this was another question I I forgot to add to my list. Um.  
That will require the user to use their credentials through the site to log into the bank. This is similar to what I know. I've done this in like the direct deposit sites and a couple other things, but.  
So there may or may not be a comfort level for them doing that. So that's something for JBL to decide on. But that's what this use case would be. Either if they can log in directly through the portal, we can verify using Stripe API or.  
We do a micro transaction, which according to what I saw, could take one to two days. Um.

**Will Jones** 6:18  
Hmm.  
What's in in terms of them setting up their location as a issuer, is that correct?

**Nathan Carver** 6:20  
So to.  
Correct. So this would be this particular one is the location owner having logged into the portal and they're going through the setup process to for the flex POS.

**Will Jones** 6:32  
Mm.

**Nathan Carver** 6:42  
So the first thing we'll want to do is gather their banking information. Well, I should say Step 2 is gathering the banking information for that overall Flex POS registration process.

**Will Jones** 6:59  
So I'm just doing the background, just thinking of the. So we said they have to set it up with their information. Why? Why is it them and not us? Because they're a distributor of these cards. So they have to have, they have to enter all their financial information. I'm I'm miss, I'm maybe missing.  
A use case that I'm not understanding.

**Juan Martinez** 7:20  
I guess Will so we we enter into an agreement with the we JVL are a reseller of this service from income. So we're we're collecting this fee of $2.00 on behalf of income and when the transfer of funds.

**Will Jones** 7:31  
Mhm, mhm.  
Yeah.

**Juan Martinez** 7:40  
Get onto the card, JVL. If a card is loaded with $100 cash out, we owe that $100 to income in a timely fashion and then the master or the location owes us that $100 cash out. So that that's.

**Will Jones** 7:51  
M.  
Yeah.

**Juan Martinez** 8:00  
The process that we're saying we need an automatic, you know like a 2448 hour debit credit scenario where we're they're depositing money or have monies in this account and we're hitting this account.

**Will Jones** 8:02  
Yeah.  
Mhm.

**Juan Martinez** 8:15  
After we do a reconciliation on a daily basis of what is owed for each location or by each master.

**Will Jones** 8:24  
Got it. OK. And how do the funds get into this account, the one that's the location owner like is that what's what's perceived there is that is that more direct from what is the transactions on the player terminal or they have to go to the bank account and then eventually just their their bank and enter the?

**Juan Martinez** 8:42  
Oh yeah, no, they need to go to the bank account. Yeah. In theory they may give us an existing bank account that they use that's, you know, funded with with monies. However, they fund it or their their general operational account or they create a new account specifically for these cash out.

**Will Jones** 8:44  
Funds.  
Mm-hmm.

**Juan Martinez** 9:03  
Related transactions to the gift card and however they deposit money on a daily, weekly basis, whatever that is, that's on them. Our expectation is that, you know, hey, if we agree that we're going to withdraw all the cash out equivalent amounts on a daily basis.

**Will Jones** 9:12  
Yeah.

**Juan Martinez** 9:22  
Then they need to fund it on a daily basis if they don't have sufficient funds in there to start with.

**Will Jones** 9:26  
Yeah.  
Yeah. OK. Interesting. Just a statement and I'll move on is that I haven't been in this space where we're a brokerage or something like that, you know, moving funds from one to another. And obviously I can say that, you know, I don't know about these.

**Juan Martinez** 9:38  
Yeah.  
Yeah.

**Will Jones** 9:45  
Location owners, but I don't imagine the location owners are the are the the the the credit A type always. So it's going to be interesting if there was no funds in that account and things like that and.

**Juan Martinez** 9:55  
Yeah.

**Will Jones** 10:00  
I don't know that that's here for us to talk about. I assume not that we're really talking about the technical details to ensure that the transition occurs successfully, but I would think the other one has risks in it too.

**Juan Martinez** 10:02  
Sh.  
Oh, they're the.

**Pavel Frolov** 10:13  
I I assume actually I assume that this is quite difficult to make this reconciliation. That's why Val suggested to include automatic clearing house to do this work on behalf of GVL.

**Nathan Carver** 10:13  
Correct.

**Will Jones** 10:27  
Yeah.  
Yeah, yeah, exactly. So, OK, interesting stuff.

**Juan Martinez** 10:32  
Yeah.  
Yeah, but but to your point, Will, yes, I mean we we owe income the money within 24 hours. So if the location has not funded it, it's on us to prepay these outstanding cash out amounts and then go after the location owner. So yes, it it it is.

**Will Jones** 10:42  
Yes.  
Yeah.

**Juan Martinez** 10:54  
A new world for us to collect daily monies owed, which we don't do today other than hey, you owe us on on a monthly basis for machine lease or rental, but beyond that.

**Will Jones** 11:00  
Yeah, I was like, do we?  
Yeah, we the the service technicians are part timing as collectors as well.

**Juan Martinez** 11:13  
Yes, sadly, our technicians don't really have the authorization to go to these locations because up until today with the machines, we only deal with the master. We sell it to the masters and the masters service the locations.

**Will Jones** 11:29  
Yeah.

**Juan Martinez** 11:29  
Now with the locations having direct access to us, we we still can't go there and and and shake them down for lack of a better word.

**Will Jones** 11:38  
Yeah, yeah. So, OK, I'm I'm sorry. Yeah, this is this helped me understand a key component of this problem. I was much more focused on the technical issues, which I think are fascinating and and definitely there.

**Nathan Carver** 11:39  
OK.  
The.

**Juan Martinez** 11:40  
Can be interesting.  
Sure. No, understood. Pavel, is there anything specifically you want from us to make your life easier?

**Pavel Frolov** 12:05  
What do you mean in case of reconciliation or?

**Juan Martinez** 12:13  
Anything. Reconciliation. More use cases.

**Pavel Frolov** 12:18  
Oh, I think no.  
Last time I shared some some documents, links, nothing new, everything on the same stage as previously discussed.

**Juan Martinez** 12:30  
Yes.  
OK. And yeah, I I have, I don't know if the rest of you have, I haven't had time to go through the documents and diagrams that that Pavel shared, so.

**Will Jones** 12:49  
So I did have enough time to go through those last night or at least cursory looks at those. My my thought was one I wanted to go back to the initial synopsis that was handed out that has like the has the objectives that we have for the for the you know before we get to the point.  
Giving a presentation and then making sure that I have my eyes on the prize, kind of, so to speak. And if there's anything you can dole out to me, then I can try to do those actions more offline and I can present back or we can then talk. I can talk more intelligently about them anyways.

**Juan Martinez** 13:11  
Sure.  
Sure.  
Sure.

**Pavel Frolov** 13:29  
Just some some notes related to stages and dates. Initially we discussed with developers and understand right now that it's it will be kind of likely impossible.  
To introduce new management system until January 1st.  
Uh, so our understanding how how to proceed with this project.  
Priority #1 to produce a payment hub that can take about two two months probably of development in parallel to continue work is designing a new CMS.  
Design and I mean graphic user interface use cases, but probably some some features related to back end but try to support.  
Location set up using current CMS because currently we have a management system for our Flex POS, Flex port, Flex pay devices just to make some modifications.  
Of the same dashboard to support Flex POS devices based on Moto Goose schema.  
And in this approach, highly likely we will be able to support Flex POS devices, set up these devices on the location starting from new year, yeah, and continue development.  
Of a new management system, this new back end and new graphic user interface.

**Juan Martinez** 15:41  
So just so I I'm sorry I had to get up and blow my nose here. We're going to obviously continue moving forward with the existing CMS and do you believe on January 1st or Q1 of next year we'll be able to move everything from old to new?  
CMS Is that the goal?

**Pavel Frolov** 16:00  
No, no, no, no, no. The goal is to support installations of the location installation in new year starting from January 1st using our current casino management system.  
And particularly Flex pay, Flex POS dashboard on currently implemented CMS but in parallel to to make features related to new CMS so to to support to parallel.

**Juan Martinez** 16:35  
OK.

**Pavel Frolov** 16:37  
All our streams to be sure that we will be able to set up locations at least for Mutogus Hema until January 1st.

**Juan Martinez** 16:47  
OK.  
OK.

**Pavel Frolov** 16:52  
It will give us more reliable dates to to produce to provide new products.

**Will Jones** 17:03  
Yeah, it sounds more realistic.

**Juan Martinez** 17:05  
Yeah.

**Will Jones** 17:06  
But I still think that there's so many nuances in that the the funds transfers that it's going to be quite interesting or quite difficult to achieve a robust system and ensure that we're not dropping funds in some cases, or at least if we're dropping them, we make sure people know about it so that they can take an action and then ensure.

**Nathan Carver** 17:07  
Makes sense.

**Will Jones** 17:26  
Sure that the funds are re added.

**Pavel Frolov** 17:28  
Yeah, actually we need to to keep keep in mind that if we are switching our payment hub communication to the cloud, then we will need not only to support the OS transactions via this hub, but also make changes for currently implemented.  
Flex pay devices also to use the same payment hub.

**Juan Martinez** 17:54  
Yes.

**Will Jones** 17:55  
So hold on, the requirement of having our interaction, our B to B with the gosh, sorry, what's the name of the the income? Sorry. Yep, moving that to the cloud, that's still a.

**Pavel Frolov** 18:05  
In in como.

**Juan Martinez** 18:06  
Income.

**Will Jones** 18:11  
P1 requirement, correct? We're not attempting to not have that aspect.

**Pavel Frolov** 18:20  
Hi.

**Nathan Carver** 18:20  
It sounds like that would be part of the the payment hub. Does that sound right, Pavel? What's that? Yeah.

**Pavel Frolov** 18:24  
Yes, yes, yes, yes, yes, you're right. Yes, I think, I think this is a requirement that we need to to implement first priority, probably not first, but at least second priority.

**Juan Martinez** 18:27  
Yeah.

**Pavel Frolov** 18:45  
Because it will protect us from different frauds, probably if our payment have implemented within the kiosk or within the POS.  
It's.

**Will Jones** 19:01  
But I think that the the the yeah protection is it's important to consider that the protection is gonna be when we move when we have a secure interface between us and Incom via you know some cloud service.  
Or being that it's hosted in the same cloud service. I thought Azure was the location based on reading those other documents. But regardless, we still there's still an easy entry point if we don't secure our own communications. So we still have the. What I would say is that the.  
You know, for us our service entry point from the site to our cloud services to ensure that there's still a very secure system in the protocol. So I don't think that it doesn't give us security for free obviously and it still doesn't give us security in terms of just being it hosted up there even.  
If we make it a secure environment, we have to ensure that our communications with that service are completely watertight too.

**Juan Martinez** 20:02  
Yeah.  
Agreed. And yeah, my my concern is at the Georgia show this week. We certainly interacted with the kiosk, but we have very little transactional data through any log files on the units to even attempt to reconcile.  
Or even address a player dispute if we had a bad dispense or whatever. So I think the big big exercise is you know we need to follow the flow of monies in and out and I think I'm going to request a sample report from income from a working location and they can.  
The name of, hey, show me what, how you invoice me, JBL on a daily or weekly basis or monthly so we can see the transactions that they're expecting us to pay against and that we would then need to verify on our side.  
Because yeah, we're conceivably it's only 40 to 50 cash outs a day, but that number will grow and and certainly the dollar amounts attached to those could be significant, you know 4 or $500, it's a lot of money adding up as we expand location. So we we need to be careful.

**Will Jones** 21:14  
Mhm.  
Yeah.  
Yeah, absolutely.

**Juan Martinez** 21:24  
OK.

**Nathan Carver** 21:26  
Juan, I'll look in their API doc to see if there's isn't a.  
If they already have an API for that.

**Juan Martinez** 21:35  
OK.

**Nathan Carver** 21:35  
That that we could actually go actively retrieve a report for Uh for a location site or a device ID.

**Juan Martinez** 21:43  
Oh, great. OK.  
Yeah, I thought at some point in time they said they send us an invoice, but maybe that's just the backup.

**Nathan Carver** 21:54  
Well, it may not be the invoice, it may be just like transactions that we've made is.

**Juan Martinez** 21:58  
And look it up, right?

**Nathan Carver** 22:02  
Um.  
Potentially.  
OK.  
So that kind of led into a question I had. Um.  
I think you mentioned fee dispute resolution. That was a a flag I had in the use case that we will need a use case for that.  
If that's going to be a system or, you know, do they do that at a portal, initiate that fee dispute, maybe the same portal where they're getting.  
Their uh reconciliation account information.  
Um, but that's on the radar.

**Juan Martinez** 22:44  
Sure, so the.  
OK. And I do believe that that that fee dispute is something that the player can call income on. You know we have the terms and conditions with the player must accept before generating the card.  
And the fee, the $2.00 fee is known to all of the Co-am players that that's a mandated fee as the system deploys. So any other location that they go to that's a non JVL system, they have the same fee, they have the exact same terms and conditions. So that's.  
Known to the player and I believe on the back of every Coem card is the call us if you have any questions kind of thing.

**Nathan Carver** 23:30  
OK, so we have potential disputes then from. Well, I guess our dispute would come from the whoever is signed up with JVL rather than the location or or the master operator, but then the other dispute is the player.  
Disputing whatever was placed on their gift card. OK, so we kind of have two paths there.

**Juan Martinez** 23:47  
Correct.  
Perfect.

**Will Jones** 23:50  
And that that's.  
And that's a JV, a dispute with JVL mediating.

**Juan Martinez** 23:59  
Yeah, to a certain extent. So income explained to us. And Nathan, correct me if I'm wrong, that, you know, today they feel like they get a ton of excessive calls from players directed at income when they should in fact be directed at the location.  
Or the reseller us in that, hey, did if the card didn't dispense properly or if the player says the cash out should have been 100 but there was only $80.00 on the card, income is hoping that there'll be some resolution or mediation done.

**Nathan Carver** 24:34  
Got it, you know, yeah.

**Will Jones** 24:38  
We didn't lose one.

**Nathan Carver** 24:41  
I'll do.

**Will Jones** 24:42  
Yeah, we'll give him a second to get back. But boy, that's a that's a hefty.  
You know, responsibility to have to be able to field these calls when the device is not in your possession, the actual account is not yours too. So I mean, in order to do that, you'd have to be able to have access or understanding what the actual.

**Nathan Carver** 24:56  
Yeah.

**Will Jones** 25:05  
Amount is an income. So like they came down and the player says you only gave me, you know, 90 bucks and I should have gotten 250. And then you're there, you know, what do they have? A player card. Here's the card number. OK, so we have to then see where it's an issue issued from or something like that.

**Juan Martinez** 25:19  
Exactly, yeah.

**Will Jones** 25:25  
And then be able to even potentially see what the balance is on that card, cause they're gonna ask that question too and we'll be like, well, we're the middleman. You have to call income for that one. Maybe I I'm it's interesting puts us puts us in a.  
An interesting position to really consider what that the player, you know that the disputer disputer, let's call them that, what their disputer experience is going to be like.

**Nathan Carver** 25:53  
Correct and I think.  
And I know that's where like the the transaction receipt comes in.  
If they bought. But again, this is assuming they even look at their receipt because they are going to actually have to accept an agreement that there will be an amount deducted from their winnings to pay for the gift card. But even that isn't a guarantee, right? That they're still not going to wonder why.

**Will Jones** 26:16  
Mm.

**Nathan Carver** 26:21  
They're 5 bucks short or whatever. Um.

**Will Jones** 26:22  
Oh, for sure, yeah. If they're like me who just got a leased car and was like, how many freaking pages? This is ridiculous. It would take me literally like 3 hours to read this. And like, anyways, you just scroll through. I have no idea what was in that text. You think they're not gonna do that at the at the local?

**Nathan Carver** 26:30  
Yeah, cause.  
Yeah, exactly.

**Will Jones** 26:39  
You know, whatever market for sure.

**Nathan Carver** 26:42  
Yeah, exactly. So if we send them a receipt or print a receipt or something that just shows.  
The current balance and you know winnings minus activation fee, current balance, so.

**Will Jones** 26:56  
Yeah.

**Nathan Carver** 26:58  
Potentially. So because we have the income API, we we could probably if for example they were to swipe the card at the flex POS, it could potentially go to a hit on incomes API and get the balance for that card.  
Um.

**Will Jones** 27:17  
This is it if they're at the site.

**Juan Martinez** 27:17  
Sorry guys.

**Nathan Carver** 27:19  
Correct, if they were at the site.

**Will Jones** 27:20  
Yeah, yeah.  
So and we we were just talking about the well, let me just to rephrase or to to synopsize. I was just putting myself in the the the shoes of the person at JBL's who's going to receive the call or maybe say the player who's going to make the call and like what questions they might ask.

**Pavel Frolov** 27:24  
It is.

**Juan Martinez** 27:44  
Mhm.

**Will Jones** 27:44  
And how awkward it is being the middle man to answer those questions because you have to have access to the information, not only the transactions that have gone through the system, which you know should give you should tell a story, but you also potentially have to have access to even the account balance and and income to be able to provide them back that.

**Juan Martinez** 27:46  
Sure.  
OK.  
Right.  
Yes.

**Will Jones** 28:03  
If they've already used some of the gift card, you know, or things like that, you would want to be able to, you know, come up and say, well, my card only has 90 bucks on it. Like, well, we issued it for this amount, Sir, blah blah blah. And then, you know, it's probably important for a person there to say, yeah, and it was issued at this value and I can see that you've made.

**Juan Martinez** 28:12  
Right.

**Will Jones** 28:22  
Made a transaction since then this you know that those kind of things would be, I think, fairly imperative for the person to have access to to be able to answer or handle the dispute successfully.

**Juan Martinez** 28:30  
Yeah.  
Sure. So one option is that the player we offer per the API spec, we offer the ability for them to print a receipt. They can get an e-mail that summarizes what.  
The transaction occurred and and likewise, Pavel, I believe that aren't they able to swipe the card and verify the balance on the card?

**Pavel Frolov** 29:03  
Oh.

**Juan Martinez** 29:04  
Or scan the card and verify.

**Pavel Frolov** 29:08  
Highly likely, yes. Not sure that currently we have this option using API from income, but highly likely for future cards as I remember they they will provide this information.

**Juan Martinez** 29:26  
Right.

**Pavel Frolov** 29:27  
To to update the current status of the card current balance.

**Juan Martinez** 29:34  
Sure, sure.

**Nathan Carver** 29:34  
So I I just opened up the Incom API doc so they do have a check balance endpoint.

**Pavel Frolov** 29:41  
Oh.

**Nathan Carver** 29:42  
Um.  
So um.  
Looking through some of the parameters, but um, this appears to be what?  
Ideally, yeah, if they if we swipe the card, we should be able to call this API if we have the.

**Pavel Frolov** 29:58  
Definitely, definitely they have different API end points to do this, but we do not show that it will work for current type of cards because actually right now it's only limited access to end points.

**Nathan Carver** 30:07  
Yeah.  
Uh, understood.

**Pavel Frolov** 30:18  
Or gift cards. At least we need to to try it on a real cards.

**Nathan Carver** 30:20  
OK, got it.

**Will Jones** 30:28  
OK.  
So do the do you have the ability to see the JVL transactions, things that have happened to that account after it's gone out of the hands of excuse me, JVL, the income transactions, the the things that have gone on with that gift card after it's gone out of JVL's hands?

**Juan Martinez** 30:47  
Me, me as an end user or I'll I'll be a JBL technician right now. No, I don't believe I can see that transactional data on the kiosk.

**Pavel Frolov** 30:52  
Mhm.  
I think so.

**Will Jones** 31:03  
So I'm I'm more just thinking about it from the perspective of an actual person in JBL who's handling this dispute and like, what do they have access to to even handle a dispute?

**Juan Martinez** 31:10  
Sure, sure.  
We we don't that that has that has to be developed. I mean I right now the only remote access into the test kiosk is from Pavel's team.

**Will Jones** 31:18  
When?  
Yeah.

**Juan Martinez** 31:31  
I I don't believe Pavel there isn't a user interface, let's say for Felipe, our man on the ground in Georgia, to go to any internal CMS page and actually be see what occurred at a kiosk. Is is that correct?  
Or does such a view exist?

**Pavel Frolov** 31:52  
Right now it's implemented on Flex pay device, so you can see reports related to tickets related to cards redeemed.  
Uh, but uh.  
Actually we we have this data also in database, but probably it's not reflected in any graphic user interface reports.

**Juan Martinez** 32:26  
Yeah.

**Pavel Frolov** 32:27  
But I do show us that it will it will be implemented in a new CMSI think it's.

**Juan Martinez** 32:37  
Yes.

**Pavel Frolov** 32:38  
Different type of reports, not only related to cards.

**Will Jones** 32:44  
If the if if the dispute point, what kind of list or what kind of transactional information will be there? Will we see you know the the cash out from the actual terminal?

**Pavel Frolov** 32:58  
Um.  
Yes, yes it. I think it will be information related to location terminal ID amount.  
Time. Something like this.  
She paid for for this transaction and last number, last four numbers of cards.

**Will Jones** 33:32  
Will it have like if it's a voucher transaction, will it know that or ticket you know versus other information?

**Pavel Frolov** 33:40  
Yes.

**Will Jones** 33:40  
Or other assets.

**Juan Martinez** 33:46  
Yeah, because the the cash out to the e-wallet, you know we're encoding the cash out amount back to the barcode on the e-wallet ticket. So we we have to know what that is.

**Will Jones** 34:00  
Yes.

**Juan Martinez** 34:10  
Mhm.  
To to Will's point, maybe that do do we need to do a mock up of of some ideal items that should be available for dispute resolution and then we find out what we do and don't have from the API, what we do and don't have, you know, sort of a gap analysis.  
Of reconciliation and investigative items.

**Nathan Carver** 34:38  
Uh, we could do like an ideal use case and then do that gap like.

**Will Jones** 34:38  
Yeah, I.

**Nathan Carver** 34:44  
This would be an ideal situation. Can we do these things or what are we missing?

**Juan Martinez** 34:47  
Sure.

**Will Jones** 34:49  
Yeah, I think like a user scenario is is or user story in this case would be quite appropriate to be able to describe the actual interaction because I I don't know that I I one I I don't have this in my background or experience, but I definitely have this this feeling that the disputes just can be very challenging.

**Juan Martinez** 34:55  
OK.

**Will Jones** 35:08  
Challenging to, you know, to be able to offer enough information to the player to even close it out, even with some kind of offer of, you know, promotion or something at the end of it, just to get them off your back.

**Juan Martinez** 35:09  
Oh, 100%.  
Oh, absolutely. Absolutely.

**Will Jones** 35:23  
So.

**Pavel Frolov** 35:25  
Actually just have probably some some ideas how it can be done. For example, if the player has has a dispute, first of all he will visit a location.  
Provide his card to the cashier. What cashier can do in this case? He can just scan it on the POS device, find all transactions related to this ticket and probably.  
Probably print some some ticket, especially formal ticket with information related to transactions. With this information he can call to income, provide necessary information related to income transaction.  
To understand what is going on with his mind.

**Nathan Carver** 36:21  
Yes.

**Juan Martinez** 36:23  
I like that Pavel. We we I think go even further and on that ticket that we can print out, we should put the phone number for income so it's clear to the player that that number has to match whatever's on the back of the card. But that way we could close the loop on that receipt.  
But yeah, I think ideally is that that if they go their first defense is right there at their location and if they can see a screen that says yes, $50 was transferred to this card on on August 1st at 3:00 PM, then I think you know most cases will be resolved there and then they can go to.  
Income if they need further clarification or or or not.

**Will Jones** 37:07  
Reprint the the receipt at the location so that they have a have some kind of, I don't know, piece of paper trail that tells them basically the issue amount or the the amount of the transaction total, the issued amount, the fee that was charged, the card that was created, you know all the details that are on.

**Juan Martinez** 37:22  
Yeah.

**Will Jones** 37:27  
On there that and the phone numbers you mentioned that would allow them to use that in case of a dispute. So you could even make it so that you know if somebody calls the number so that somebody has a dispute, they call the number with income, income goes, well, I can't handle this. I mean you're you're telling me that you played this game and you won this.

**Juan Martinez** 37:31  
Yeah.

**Will Jones** 37:47  
Or whatever. I don't know anything about it. All I see is that you got this issue. So they're gonna come back and say you need to call JVL, probably not the operator, but if we can avoid that and have them say you need to contact the site where you were at and we can kind of make it that OK contacting the site.

**Juan Martinez** 37:49  
Right.  
Right.  
Right.

**Will Jones** 38:06  
Would allow you to have that conversation with the site and issue this ticket, which actually is something that we require to be able to handle a quote dispute. We could force them or push, you know, we could coerce them. Maybe that's the right way into going back to the site, the correct place to handle the dispute. You can actually say no, that's the terminal over there that you're applying.  
Yeah, on that terminal you you won, you lost whatever. They even have access to the history of the terminal. If it's, you know, if it was just yesterday or something, they can go back and see what was happening. So whereas I think JVL is really at a loss for helping.

**Juan Martinez** 38:34  
Yeah.  
Sure.

**Will Jones** 38:42  
In majority of these situations, if it's not a JBL machine, if it's not, you know, if there's basically no information except for being in the middle and saying, yeah, that's the funds that got transmitted across our system. I don't think there's too much else that you can tell the player except for that.

**Juan Martinez** 38:54  
Absolutely.

**Will Jones** 38:58  
Just confirm the amount and and be done.

**Juan Martinez** 39:02  
Right.

**Pavel Frolov** 39:03  
Mhm.

**Juan Martinez** 39:03  
Agree.

**Will Jones** 39:03  
So I like that. I like the idea of trying to get them back to the site.

**Pavel Frolov** 39:08  
Yeah, first of all, we are helping a cashier because cashiers do not know how to solve any problem. But if you provide them a simple solution, just press a button to print some action list. Yeah, with the necessary information then.

**Will Jones** 39:15  
Yeah.

**Pavel Frolov** 39:28  
A player can read through this report, understand he need to call a special number, provide information printed on the ticket to continue solving of his problem.

**Will Jones** 39:31  
Yeah.  
Yeah, let's say also for the people that are cashiers, not only just giving them the information, but also telling them that that the the transaction completed successfully. I think that gives them the confidence to respond back to the player with a positive, you know, no, this is this happened and it worked. It worked this time.  
You know, it worked fine versus them trying to really look through and decipher and decide did it work. You know, having a clear message on that receipt or that terminal that says transaction completed successfully and then start with that and beyond that have the information that they can share with the players they need.

**Juan Martinez** 40:02  
Yeah.  
Absolutely.

**Will Jones** 40:21  
Because I feel like they're gonna point the finger quick. That's not me. Our property worked great. It's it's them.

**Juan Martinez** 40:23  
Oh, of course.  
Yeah, no, definitely. Guys, should we, should we jump on a call with Incom to have them walk us through a typical dispute situation from actual examples? Does that make sense?

**Pavel Frolov** 40:27  
Mhm.

**Will Jones** 40:41  
I think that would be great. That would be very helpful.

**Nathan Carver** 40:44  
Yeah, I think just from learning from that.

**Juan Martinez** 40:44  
OK, I know Will, you had some things Tuesday. Nathan, you had something on Wednesday.  
Thing on Wednesday.

**Nathan Carver** 40:57  
Um.

**Juan Martinez** 40:57  
Oh.

**Will Jones** 40:58  
Just getting married. Nothing much.

**Nathan Carver** 40:58  
OK.  
Yeah. So depending on which week, next week I'm, Oh yeah, Wednesday I am traveling. So that would be her. I could call in from the road would be my only option.

**Juan Martinez** 41:02  
Yeah.

41:04  
Mhm.

**Juan Martinez** 41:08  
OK.  
Sure. Obviously because we need to be work around income schedule, normally they don't do anything in the morning. They're after 10 or 11 EST time. What is your availability will after?  
Midday and likewise Nathan.

**Will Jones** 41:34  
Yeah, I can generally, yeah. With enough advanced notice I shouldn't have too much trouble to to make it work. I have a few meetings that are sticky ones that I can't avoid and that's on a Tuesday afternoon is more difficult for me one in a Monday morning, but for the most part the rest of the meetings throughout the week I can either find a a replace.

**Juan Martinez** 41:47  
OK.

**Will Jones** 41:54  
Or, you know, or just move the meeting around to accommodate. So yeah, you can let me know. My my boss at the other business knows that I do this too, so he's fine when I come in and say I need to take 1/2 hour, an hour off to do something else.

**Juan Martinez** 41:59  
OK.  
Oh, OK. And then Nathan, you're traveling on the 3rd. Is that in the morning? Is it all day?

**Nathan Carver** 42:12  
It.  
That's gonna be an all day, so the third will be hard for me, I would say.  
Yeah, if it's based on income schedule, if I can't make it, then let's just record the meeting and at least be able to share out the information, so.

**Juan Martinez** 42:32  
OK, well, let me let me see. Let me check for their availability, availability on the 3rd or the 4th of next week.

**Will Jones** 42:43  
Yeah, if I could ask Pavel to to, yeah, please do that. Juan, just going back to a question that stemmed from what Pavel said earlier, Pavel, if you would, what, what is if if you're using the existing CMS and building off of that, it seems like there's, you know, quite a lot of thought.  
It's already got into at least describing the existing C CMS. Now things fit in. So what is what do you need out of this set of meetings to be successful to get to that that that date if that decision's already made?

**Pavel Frolov** 43:21  
You mean using current CMS?

**Will Jones** 43:24  
Yeah, exactly. What do you need to basically go from here to January 1st? What are we? What are we? What's like the top list of items that we're trying to provide from this set of discussions?

**Pavel Frolov** 43:35  
Uh.  
Actually I'm not sure that I fully that I actually have this list, but first of all we need to expand current.  
Dashboard.  
Uh, where we set up uh uh pay devices.  
To support the Flex OS.  
Also we will need to add flex POS.  
Devices to give CMS system to understand newly newly created devices because we do not have this entity right now as POS.

**Nathan Carver** 44:33  
Mm-hmm.

**Pavel Frolov** 44:34  
But but we do have Flex pay devices.  
And the next to expand the registration process for the Flex POS.

**Will Jones** 44:41  
OK.

**Pavel Frolov** 44:56  
Probably that's all, but actually we'll need to to continue digging into.

**Will Jones** 45:06  
But it's primarily from these discussion, do you want requirements or direction on architecture, confirmation and architecture? It sounds to me like we're just talking about you want to know what deck has to go on to the, you know, the user interface that's going to be there for either our personnel, the operator.  
Or the person, the the site, you know the the person on site to be able to handle say the dispute or things like that.

**Pavel Frolov** 45:35  
Yeah, actually probably you need to to know that current CMS already supports different entities like operator, location, lease, device, so on, so on so.  
Actually we're going to reuse these features already implemented and we'll simplify the final implementation.  
That's why I do sure that it will be done until January 1st.

**Will Jones** 46:13  
Got it.  
Do there was another question or sorry, there's one other thing that I wanted to to ask and understand if it does even have any applicability in our discussions and that is HHR. So obviously I know that the HHR start date is targeted before January 1st, it's it's.

**Juan Martinez** 46:51  
Yeah.

**Will Jones** 46:51  
October 15th is what I was what I was told. Anyways, that's still holding. I don't know what the expected duration of that project is, but you know something similar to January 1st. It's not going to take a ton more time than that, I would guess.  
The the question I have is what's the relationship between the CMS and HHR as we're speaking. I don't see, I don't see the overlap in that my expectation with HHR is the terminal and whatever services that are on the terminal are directly connecting to a third party HHR.  
Our server to facilitate the game engine, the game trend, you know, the getting the race ticket sets and things that way. So I don't, you know, I don't see much overlap other than there's some potential for adding a new.  
Terminal type to the CMS or things like that that I don't think, you know, maybe there's a few different configuration settings, I'm not sure. I don't think that it's really a new feature, it's just extending the existing CMS functionality.  
To have to support a new terminal type and not much more. So I don't know what's where am I missing?

**Juan Martinez** 47:58  
Hmm.  
No, the so the the problem is you cannot just buy a JBL machine, install software and and walk away. You know we have this remote initial setup, the RIS file, the the end user is not.

**Will Jones** 48:18  
Mm.

**Juan Martinez** 48:21  
The ability to type in key settings isn't there, so JBLS, the CMS system has to be aware that that serial number has been deployed at that location. We have to create the software file, we have to create the RIS file and then.  
Basically make the machine come alive in our system, you know, scanning of the leases and things like that. So yes, the the architecture to the machines today is very different from other Class 3 manufacturers.  
Where the machine can be just set up on site. That is not the case with the JBL game.

**Will Jones** 49:01  
Is is it not true though that the CMS already supports, if not 95% of the the functionality that would be required to handle a new device type or a new, excuse me, a new EGM type of HHR?  
It it would be extremely close to what we already do with any other variant of game. So is is there any in in this discussion, does the HHR have any significance?

**Juan Martinez** 49:27  
Yes.

**Will Jones** 49:36  
To whatever net is next with the CMS, you know is it? It's just it's just getting added to the CMS and and and that's probably known what needs to change and how how the CMS can support it. So there's probably not much to talk about in this meeting anyways.

**Juan Martinez** 49:56  
I would go ahead, Pavel.

**Pavel Frolov** 49:59  
Just some some notes. First of all, I think we are able to, we will be able to install HHR software on our currently used cabins.  
That's why we do not need any changes related to convenient type, but each new software need to be created in CMS.  
Highly likely it will support some additional fields that we do not support right now in areas probably and.  
Maybe something else?  
But but you're right, 95% it will be the same CMS as as we have right now, but probably with some minor changes related to game setup.  
In areas.

**Juan Martinez** 51:06  
Yeah, yeah. So I guess just to summarize that that's the machine will communicate with CMS as it does today will and then the machine will communicate independently with the new HHR component, but they don't necessarily need to overlap however.  
The we want to add features to CMS to allow the machine to be fully set up without the need for CMS in the future under Omni. So Pavel that that will change at some point in time.  
But right off the bat, yes, they're two independent systems. What the machine does with HHR is new, but what the machine does with CMS might need some some small tweaks, but it's independent from HHR.

**Pavel Frolov** 51:42  
Yes.  
Yeah.

**Will Jones** 51:59  
OK.  
Is is HHR going to be built on Omni? I thought that was the case for sure. OK, OK, we don't, we won't go any further there, just making sure that that was still my understanding is correct.

**Pavel Frolov** 52:12  
Yes, yes.

**Juan Martinez** 52:12  
Yes, yes, yeah.  
Yes, definitely.

**Pavel Frolov** 52:20  
Yeah, actually right now we are on the stage when we are doing the last last features related to bonus game, finishing bonus game implementation based on Omni.  
Uh, next I think we'll be.  
To implement top tier view.  
Uh, for only to general, I think we are quite close to to finishing one month.

**Juan Martinez** 52:54  
OK.

**Pavel Frolov** 52:55  
At least at least first the game implementation based on.

**Will Jones** 52:59  
OK.  
Back to just talking about the the problem at hand.  
With these you know with the the tickets and issuing is all is it the existing CMS system sufficient to handle any kind of transactional dispute on the ground at the casino meaning not not talking about issuing to the gift card but.  
But before that, if there's like any, you know, funds transfer from from the game, you know to the, I don't know what exists currently, but to the kiosk, if the kiosk has ability to, you know, to issue cash, is there a sufficient information already provided to that onsite?  
You know the owner, so we're referring to them, but the on-site person manager to be able to handle any internal casino money movements.  
Internal property casino might be a stretch of the word.

**Pavel Frolov** 54:05  
Oh.

**Juan Martinez** 54:05  
I guess that yeah I the question is, is Felipe and team able to follow the money flow by going through kiosk screens and or EGM screens to determine?  
Exactly what happened in in the process.

**Will Jones** 54:25  
Yeah, more like. So Juan, if you want to say from a a normal, you know, slot management system perspective or vouchering system perspective, you'd have the ability to at least see where you know when issues were or vouchers were issued and where they were redeemed and you can track.  
You know the the money movement in that respect to say, yeah, they added 500 to this machine and then they cashed out for 375. You know that ticket then was redeemed over at this machine where they added it and they cashed out for 225 and then they went to the kiosk and they redeemed their, you know, 225 and they they got.

**Pavel Frolov** 54:47  
OK.

**Juan Martinez** 54:52  
Sure.

**Will Jones** 55:04  
Cash for it. Is there sufficient, you know, information within the CMS system right now or whatever the the component is that lives at the property? Is there sufficient information there to track money movements like that? Or is this, you know, is this just all new areas of the CMS?

**Juan Martinez** 55:06  
Great.

**Will Jones** 55:23  
That we don't currently, you know, currently have since we're going to be able to have money movements facilitated through the CMS.

**Juan Martinez** 55:32  
There's there's no GUI interface for an end user, a JBL personnel that I know of, but I'll let Pavel chime in, but it it it would be difficult right now for me to envision.  
The local team being able to walk through that scenario of of tracking down exactly what happened.

**Pavel Frolov** 55:56  
Yes, Juan, you're right. Yeah, you're not not implement everything and provide all the reports either in CMS or in.  
Our labs here, it's not done yet and the more the most full information right now is placed on Flex pay device as central.

**Will Jones** 56:27  
OK.

**Pavel Frolov** 56:28  
Communication server with a call and in the future it will be moved to the cloud.

**Juan Martinez** 56:39  
OK. Yeah, because our our target is to hopefully go live without a Flexpay device. You know, Flex POS solution is our primary target for the end of this year. So you know, we need to envision accessing all of this data without a Flexpay.

**Will Jones** 56:40  
So.

**Juan Martinez** 56:59  
Physical Flexpay kiosk on Prem.

**Pavel Frolov** 57:00  
Mm-hmm.

**Will Jones** 57:02  
Yeah. So for the, would it be, is this an accurate statement, I guess that So what we've talked about before earlier in this conversation about, you know, handling disputes, is it accurate to say that there needs to be some type of, I don't know, flex point?  
Point of sale user interface, if that's the word, the correct way to say, but there would be some kind of user interface that is accessible at the site that is possible for somebody to to follow the money as it went either being issued or redeemed.  
Including the final redemption in terms of the the issuance of a gift card.

**Juan Martinez** 57:49  
Ideally, yes, there should be will, but I I would say that these. So remember that these aren't casinos, there is no accounting department, there is no slot team that is used to doing any of this day-to-day. So it would be, it would need to be as simplified as possible.

**Will Jones** 57:55  
Yeah.

**Juan Martinez** 58:07  
Possible where I I mean I would envision you enter the card number that you were given and then that simple card number brings in everything that they need to see into one visual report. They're they're, you know, opening reports for a $10.00 an hour.

**Will Jones** 58:22  
Yeah.

**Juan Martinez** 58:27  
Store clerk is would be a massive amount of training that they do not do today.

**Will Jones** 58:33  
Absolutely, yeah. So some simplified list of transactions is probably as as far as it needs to go.

**Juan Martinez** 58:40  
Yes.

**Will Jones** 58:41  
Yep. And then that that the POS is gonna have a a ticket printer or a printer I should say.

**Juan Martinez** 58:50  
Yeah, where the the Mother Goose system has a printer and we agreed that we would leverage that existing printer because the the player has the right to request a receipt. How do we print a receipt from POS? Well, we'll reuse the printers that they already have on hand today.

**Will Jones** 59:09  
What's the What's the Mother Goose like device?  
The physical device that drives the rinter.

**Juan Martinez** 59:15  
I mean I can, I'll send you some specs. It's just a small board that is capturing the daisy chained RS232 machine to machine data by sniffing the pulses from the meters in and out.

**Will Jones** 59:27  
Mm-hmm.  
Yeah.

**Juan Martinez** 59:33  
And then it's converts all that and sends it over to the printer. I believe it's RS485 at that point in time, but we do have the specifications on the Mother Goose.

**Will Jones** 59:42  
In.

**Nathan Carver** 59:45  
Hey guys, I need to I need to sign off, so I'm sorry I need to get going.

**Will Jones** 59:45  
Yeah, the Mother Goose has like some kind of view in her face that.

**Juan Martinez** 59:48  
Yeah, I know no user interface today.

**Pavel Frolov** 59:49  
No, no user interface.  
Just several buttons.

**Will Jones** 59:53  
OK. See you, Nathan.

**Pavel Frolov** 59:55  
Bye.

**Juan Martinez** 59:55  
Don't see anything.

**Nathan Carver** 59:55  
Alright.  
See.

**Will Jones** 59:58  
Yeah, my my thought was maybe just direction one first that I thought that I could probably take this and run with at least envisioning what a user, what a player, a standard player.  
What do you call it session would look like and add on to that another kind of and if the session ended with the player wanting, you know disputing what they cashed out for what they got back, you know what that would at least look like in terms of in a story. So the what we're trying to solve there, I thought that would be very helpful for Nathan because.

**Juan Martinez** 1:00:18  
Right.

**Will Jones** 1:00:35  
He's probably not, you know, is is without experience of being in, you know, the casino, or at least the demands of what casinos need to do to operate. That would be helpful. Saying that I was asking enough questions, so I envision.

**Juan Martinez** 1:00:43  
Sure.

**Will Jones** 1:00:52  
Who's the actual, you know, what I'm gonna call is more the attendant, the person who's working at this site and in helping there and in what what kind of device they have access to and if they have a ticket printer, how the heck do we?

**Juan Martinez** 1:00:57  
Right.  
Yes.

**Will Jones** 1:01:09  
Even push a button to make it print a ticket, you know? Or if we had a printer, how do we push a button to make it print something?

**Juan Martinez** 1:01:18  
Right. So, so today and and bear in mind, well, we we as a manufacturer by Georgia Lottery rules don't have access to that in in the sense of the Mother Goose does what it does and the attendant.

**Will Jones** 1:01:28  
Mhm.

**Juan Martinez** 1:01:35  
Reconciles it however they reconcile it without any input or contact from the manufacturer. So we're not Privy to that process because we technically don't even know where our machines are installed because we're not allowed to by the regulator.

**Will Jones** 1:01:43  
Mhm.  
Hm.

**Juan Martinez** 1:01:53  
So all I can tell you is that the player is sitting at a machine #4 and there's a sticker on it that says #4, and when he cashes out, he tells the attendant. If they if they don't even have line of sight, they might know. OK, I saw you just got up for #4.  
And you're telling me it's $20 and yes, the printer printed a ticket number for $20 and then they manually pay the player that $20. Today, 99% of the transactions are in the form of a gift, a store credit or lottery tickets.

**Will Jones** 1:02:32  
Hmm.

**Juan Martinez** 1:02:33  
You know the gift card is being rolled out now, so that doesn't even happen in a lot of the locations. And sadly, this is where they also sometimes pay a known player in cash, which is illegal under Georgia rules. There might be a small service fee. Hey, you cash.

**Will Jones** 1:02:40  
Mm-hmm.

**Juan Martinez** 1:02:52  
out 20, but if you want cash, I'm only going to give you 18 and they're like, oh sure, no problem. Thank you.

**Will Jones** 1:02:58  
Yeah, put 2 bucks in the bank and you're good. Yeah, yeah.

**Juan Martinez** 1:03:02  
Exactly, exactly. Because a lottery ticket or $20 is not a guarantee $20. You might have a losing lottery ticket.

**Will Jones** 1:03:08  
Sure, yeah, for sure. So, OK, so when they they when we talk about them having a dispute that what interface would be available to that attendant to handle a dispute?

**Juan Martinez** 1:03:25  
To my knowledge, I believe there is no user interface to the Mother Goose today. Correct, Pavel?

**Pavel Frolov** 1:03:32  
Yes, yes, yes.

**Juan Martinez** 1:03:33  
Yeah, I I think that they maybe have a reprint button on the board if the printer malfunctioned, but that's the extent of it is the print. The printed receipt says machine #420. That's all I know and that's all I can pay out.

**Will Jones** 1:03:45  
Yeah.  
So in in that what what would you I I guess then just are we when we're talking about using the printer of of the Mother Goose you know to print out some transactional information that's going to be sufficient for the attendant to handle a dispute without engaging to Incom or.

**Juan Martinez** 1:04:07  
Sure.

**Will Jones** 1:04:12  
That what? What would be? How would they initiate a, you know, another ticket print that would give them this other information? Or is it just always going to print that way?

**Juan Martinez** 1:04:24  
So.  
So it it well, it's not another ticket print. So when we install POS, we've disconnected the printer from Mother Goose. The Mother Goose is sending the data to us, which is.

**Will Jones** 1:04:42  
Mhm.

**Juan Martinez** 1:04:43  
A secure number, the location ID, the date and time, and the dollar value. And we're capturing that. And then this printer will now connect to our Flex POS and we can print.

**Will Jones** 1:04:49  
Mm-hmm.

**Juan Martinez** 1:04:59  
We can replicate what was on that or print additional information including that hey $20 was put on onto this gift card as a scenario. So we don't, we haven't done this yet, but that's what we're going to do. So we can do anything we want, Will, because we're we're defining that right now as to the.  
Flex POS printing out to this printer and we can print out whatever we want within reason.

**Will Jones** 1:05:27  
In in this printed ticket, is this like the one that's machine 5/5 pays collected $5 redeemable? This is the one that comes from Mother Goose right now.

**Juan Martinez** 1:05:37  
That is correct.  
That is correct.

**Will Jones** 1:05:42  
OK, what's this voucher number 2655? How does that get created?

**Juan Martinez** 1:05:50  
Um, are you sharing your screen? I'm sorry, I just uh.

**Will Jones** 1:05:53  
No, Pavel's on the same screen with me right now. I can see him wagging around.

**Juan Martinez** 1:05:56  
Oh.

**Pavel Frolov** 1:05:57  
I I can I can share this screen.

**Will Jones** 1:06:01  
Sorry, I I will have to. I I know we're gone over and I will have to leave in the not distant future because I got a dentist appointment this morning. So I apologize I won't go too much longer.

**Juan Martinez** 1:06:15  
Uh, no problem.

**Will Jones** 1:06:15  
Yeah, what's that voucher number you see right there?

**Juan Martinez** 1:06:20  
That, yeah, that that's a model.

**Pavel Frolov** 1:06:20  
Uh, this is directly printer printed by Uh Mutagusa on the printer, yeah.

**Will Jones** 1:06:27  
Yeah, so it's something from Mother Goose, right?

**Juan Martinez** 1:06:29  
Correct.

**Pavel Frolov** 1:06:29  
Yes.

**Will Jones** 1:06:30  
Yeah, some probably monotonically increasing number of each one that gets printed. Will we have, will we have that information? Does it even matter if we don't have that information?

**Juan Martinez** 1:06:35  
Correct.

**Pavel Frolov** 1:06:36  
Exactly.

**Juan Martinez** 1:06:41  
As we understand it, everything you see on this ticket will be sent to us because we're intercepting it. In principle, this goes to the printer, so now it's coming to us.

**Will Jones** 1:06:51  
Mhm.  
OK.  
And confidence number, what's that thing?

**Pavel Frolov** 1:07:00  
Actually, we have a logic how how it's generated and pay like we can at least validate the value. It's not so reliable, but at least.  
Will protect us from a stupid copy of the tickets.

**Will Jones** 1:07:22  
OK, but a smart copy? No. But a stupid copy? Yes. So if somebody added, you know, white out here and added another, you know, 10 in front of it, it might catch us for that.

**Pavel Frolov** 1:07:26  
Yes, yes.  
Yes.

**Will Jones** 1:07:36  
OK, but anyways, we won't be paying off the ticket, I believe, anyhow, right? We're paying off the pulse that comes from Mother Goose.

**Juan Martinez** 1:07:44  
Corrected. Yeah, there will there. That ticket won't exist because we've intercepted the printer, so that ticket goes away.

**Will Jones** 1:07:51  
Mm.  
Yeah.  
OK, so something gets printed out. If somebody comes back into the casino, excuse me, the property and says, hey, you issued this card to me and I expected it to be this. They don't have their receipt. They've lost their receipt. That would be the most common one. They just have a card and they say this doesn't have enough money on it. It should only it should have had 115.

**Juan Martinez** 1:08:14  
Sure.

**Will Jones** 1:08:20  
On it, but only has $50 on it. So they they come in and then you know are are talking to the person, the attendant. What's the attendant gonna do? Like what can the attendant do? And I'm gonna backfill this or back story here. That person went out and went to someplace.  
Used $100 off the gift card and now only has 50 and maybe they even have the receipt. Let's say they have the receipt and it says it should have 150 and they're coming in and saying it's only $50. This thing is supposed to be 150. You guys screwed me over.

**Juan Martinez** 1:08:47  
Right.  
Yeah, the only person that knows that is income. I think that the player has to follow the instructions on the back of the physical card, which is to call income, who can then say, Oh yeah, that card was created at 9:00 AM, we see at 9:13 you put $25.  
At this gas station and then you're trying to come back and say your card is missing money. Only income knows that.

**Will Jones** 1:09:19  
OK, so.

**Pavel Frolov** 1:09:19  
Or or as as we previously described, issuer can swipe this card. Flex POS find in database this card if it is issue it on this location and provide a report in printed form.  
Is all the information related to cartrid redemption. What was the original value? What was?

**Juan Martinez** 1:09:50  
Yeah, but to to your point though, Pavel, it's only the original value. If the player used it, we we have, we have no record of that Will and and we shouldn't. I mean we're not the card holder clearinghouse that that's a massive amount of data and we certainly don't have access to that.

**Pavel Frolov** 1:09:53  
Yes.  
Yes, yes, exactly. Yes.

**Juan Martinez** 1:10:04  
Yeah.

**Will Jones** 1:10:09  
Can we can we query that income to find out the current balance of the card?

**Pavel Frolov** 1:10:09  
Yes.

**Juan Martinez** 1:10:14  
Yeah, the card itself. When you get it, there's a website address, mygiftcard.com or something like that. Anyone you can enter the barcode on a website and get the actual balance that that is a a function of the card today.

**Will Jones** 1:10:26  
Yeah.  
Yeah, I wonder, I wonder if that would be part of what income would support to, you know, to say like if we can query them to say what was the issuance amount to have that confirmed and then what's the actual balance of the card, then those two bits of information would be the only other two things that I could think to include.

**Juan Martinez** 1:10:39  
I I do believe so.

**Will Jones** 1:10:48  
You know, beyond what our POS, what our transaction logic would it would have been able to show.

**Juan Martinez** 1:10:53  
Yeah, and and I do believe that that that is in the API if I'm not mistaken.

**Will Jones** 1:11:01  
Is that that's what I wrote down earlier from somebody saying that JVL endpoint to check balance?  
Hmm.  
Hmm.

**Juan Martinez** 1:11:16  
Card created here, card created at this time on this day in this amount and and and that's a receipt that could be given to the player.

**Will Jones** 1:11:25  
Yeah. OK. Yeah. So obviously we're trying to define the functionality of what needs to, what needs to exist at the property or what things they have at their disposal at the property. Sorry, I'm, I'm still coming along with understanding of what that ecosystem looks like. So I think I have a better picture.

**Juan Martinez** 1:11:39  
Yes.

**Will Jones** 1:11:45  
Now of it, after asking those questions, obviously there was the part of the being able to access funds from the property itself, from the owner to be able to pay for the actual cards that are being issued and then take.

**Juan Martinez** 1:11:49  
Understood.  
Mhm.  
Right, right.

**Will Jones** 1:12:04  
Our percentage of that pay are $2.00 like the property owner took before. And then on the other side, is there any kind of requirement? I mean there's interaction with income, Pavel, I figured that that's just the API and you already know what you already are working with income. So there's probably.

**Juan Martinez** 1:12:07  
Yeah.  
Sure.

**Will Jones** 1:12:24  
Not a whole lot to expand on there. Or is there any other areas that you're still interested to understand more about the interaction with income?

**Pavel Frolov** 1:12:33  
Right now we're just using the minor request to income just to reauthorize and first of all authenticate our location.  
And then you'll be able to reauthorize card and just authorize card that that we redeem minor tool.

**Will Jones** 1:13:05  
Hmm.

**Pavel Frolov** 1:13:06  
And that's all. That's all. Nothing more from the API.  
At least right now.

**Will Jones** 1:13:14  
Yeah, yeah. Just just moving that interaction to behind the the behind the scenes in a cloud environment so that it can be more secure and then having you know facilitate that transaction through our own endpoint.

**Pavel Frolov** 1:13:23  
Mhm.  
Yes.

**Will Jones** 1:13:34  
Is is that is that cloud environment going to be Azure? Is that correct from what I read in the documentation?

**Pavel Frolov** 1:13:41  
Yes.

**Will Jones** 1:13:42  
OK, I don't know a ton about Azure, you know, ecosystem, but but I'm sure they must have serverless components. That would be the least expensive way to do it and probably the most secure or hosted mechanisms.  
Which then would give us the ability to actually run, you know, on Prem if I ever wanted to, but I'll leave that to a separate architectural discussion. Pavel, do you feel confident in that area in choosing your cloud service provider and and what services they have?

**Pavel Frolov** 1:14:06  
Yeah.  
No, I don't have enough experience with this.

**Will Jones** 1:14:20  
If you'd like, I can at least we could have an aside talking about what things to consider and then what you're you know, what you're interested in achieving. I can also do a little research in Azure so I can find. I can hopefully I realize that.  
You know, AWS to Azure probably very similar in so many ways. It's just Azure's I think a bit more has fewer services but more structure, let's call it that way. They're more organized to a certain extent.

**Pavel Frolov** 1:14:51  
It.  
Actually right now we had some services in cloud using a WS, but for some reason I don't know exactly why it was a decision from our admins plus valve.

**Will Jones** 1:15:03  
Mhm.

**Pavel Frolov** 1:15:12  
To switch to Azure in the future, but not right now.

**Juan Martinez** 1:15:13  
I I I think the the reasoning was that we're already in the Microsoft ecosystem with Teams and Office and all of that. So it just made sense to stick to Azure, which is a Microsoft product.

**Will Jones** 1:15:30  
OK, that's a stretch. I would say that that that, yeah, exactly. I though I do think there was, there was something, there was also a note somewhere off the look in and see where I found it last night that did have some other details of why Azure was being selected, but it was definitely to stay within the Microsoft ecosystem.

**Juan Martinez** 1:15:32  
Yeah, but that's what I was told.

**Will Jones** 1:15:51  
I I was wondering, I know we're writing things in Java, so we're not connected there. Obviously if we were doing stuff in C#, I would say that it it that potentially would be another reason why you'd want to go to Microsoft. It's a little bit easier in in Microsoft to in Azure.

**Juan Martinez** 1:16:03  
Good.

**Will Jones** 1:16:09  
But in any case, yeah, OK, Pavel, I would happily expand on my thoughts to what we would want to consider when we're moving over into that environment, especially if, especially if there's a greater adoption in the CMS when it's rewritten. So if.  
If right now it's just doing it to facilitate this transaction and that's really as far as we're going to go, then it's fairly trivial and there's not much that needs to be considered. But if in the future we're going to expand and all those different components that currently are run on hosted servers.  
They can be integrated into Azure services. Then there's a different, there's there's a much greater question to start talking about already.

**Juan Martinez** 1:17:01  
Great. Yeah. And and guys, I I gotta run when I got my next.

**Will Jones** 1:17:01  
So OK.

**Pavel Frolov** 1:17:02  
We're just.

**Will Jones** 1:17:06  
Me too. I got to go get my teeth cleaned. So I'm sorry to hear that you're sick, Juan. I I actually got sick the beginning of this week, but I feel so many. I woke up today. I was last night. I was thinking like, oh, maybe I should tell these guys that I can't do it because I was just. I didn't sleep the night before. I had massive headache.  
But I slept great last night, finally. I don't know, but that's it. Dayquil. Yeah, I know what you. Yeah. So feel better, Juan.

**Juan Martinez** 1:17:29  
Yeah, this is this is my my best friend these days.

**Pavel Frolov** 1:17:32  
Yeah, yesterday I I I also used this because of headache.

**Juan Martinez** 1:17:37  
Oh.

**Will Jones** 1:17:37  
All right. Well, you guys both feel better.

**Juan Martinez** 1:17:40  
We're getting, we're getting old, guys. All right, guys. Thanks, everybody.

**Will Jones** 1:17:43  
So we'll see you next week. You know, just send out whatever the meeting invitations are. And I'm, I'm very busy from here to the middle of next week just because I'm going to East Coast to take my daughter to school. So, but I will, you know, be back mid next week.

**Pavel Frolov** 1:17:43  
We understand you, yeah.

**Juan Martinez** 1:17:55  
Sure.

**Pavel Frolov** 1:17:59  
Yeah.  
Thank you, bye.

**Will Jones** 1:18:02  
Thanks. Bye.

**Juan Martinez** stopped transcription