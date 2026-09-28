# Raw Transcript — CIBC (Michael Hill) + Nathan Carver — ZBA account + Business Central API integration
**Date:** July 28, 2026, 4:01 PM Eastern (meeting ~13 min; trailing unrelated background audio after 00:23 ignored)
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Summary note:** [[Meeting_Notes_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026]]
---
00:00:00 Michael
Trying to make sure that I can move this along as far as what we're looking to do with these new accounts that have been opened for Leviton. Um, I'll tell you that we already have the second account open. That's already uh been adjusted to be a ZBA. I'll explain to you kind of the discussion that I've had with Val in the past as far as what this account structure is going to look like. There are going to be deposits that are going to come into the account these deposits. Deposits are going to come into the account via a third party. They're going to come in a batch format, so there is going to be multiple transactions in one batch. Once those deposits come into the account, they're going to hit the ZBA account. The ZBA account is then going to at the end of the day, automatically transfer those funds out of that account into a separate account. Okay, so all of that is understood for me.
00:01:00 Michael
So, in the gray area with is the API, I mean not the API as far as the um. The technology portion of it so, When we are discussing, like how we want this to actually work with the API I, just need to understand exactly what needs to happen. And if that's already going to be in process or already going to be set up with what we have right now, I'll tell you with the Microsoft system.
00:01:31 Michael
I did confirm last week. Hold on, I got notes here. I did confirm, last week.
00:01:50 Michael
Okay, So with our Microsoft Dynamics, um there is going to be a API connector. So the API connector is kosher. So we do have the ability to be able to integrate, the Microsoft Dynamics into our Business Net Banking. Okay, so when that is integrated, I think that's where it kind of gets a little bit fuzzy for me as far as like, what needs to happen once it's integrated. Are, we going to be working directly through the Microsoft Dynamics system itself to process payments and not logging on to Business Net Banking?
00:02:28 Michael
Or is Microsoft Dynamics simply going to be used as a means for us to be able to just decipher the actual transactions as they occur on the account. Thank you. I mean.
00:02:50 Nathan Carver
Oh, okay, I got it. How about that? Yes, okay, so it'sum at the end of the chain. The API is for our system to verify the transaction, the money is deposited so that we can reconcile the ledger on our side. So if the automation is already there, for all those handling the deposits in this example, and the CBA is moving the money at the end of the day. So then after that, at some point after that money would move, our system would.
00:03:27 Nathan Carver
Then call the API, verify that deposit and the amount that was deposited. Um. So as as of now, that's what the API would do. So we don't need to initiate any transactions, just verify transaction history.
00:03:45 Michael
So we just want to confirm that through the Microsoft Dynamics, that it is going to be able to translate our account history, Into the ledger within Microsoft Dynamics.
00:04:03 Nathan Carver
Um, I don't know if we have to go that far. All we need is something. If that's in the Microsoft Dynamics API, then that's where we'll get it. Wherever we can get the transaction history every day, our get you know whatever the last daily transactions were. That's, That's where we need to make the call. So, I am not familiar enough with those systems to say yes, That's where we need to pull it from because it may not be if there is another API, that just gives us a balance of that account or transactions on that account. That's what we can use.
00:04:43 Michael
So, Let me kind of break it down, what I think we may need. And then Nathan and Val, you guys tell me if it's something different. Okay? So, I know Val, We were talking about the usage of like a transmission system to be set up. I don't really, I don't think that we need transmission services as of yet. This is what typically happens. So when we set up an outside aggregator like Microsoft Dynamics, when that's integrated into Business Net Banking, What happens is the transactions that are occurring on Business Net Banking. They will feed directly into Microsoft Dynamics. And then from Microsoft Dynamics, once those transactions are there.
00:05:24 Michael
Then you will be able to confirm within those within Microsoft Dynamics the date, the dollar amount, and who the sender is of those transactions. Okay. Now what what I don't know for sure, Nathan is if I have like this batch amount that comes in if when that is translated into Microsoft Dynamics, if it's still going to read that batch amount. If it is still going to read that batch amount, that's Fine, What I can do now is I can set up a report within Business Banking. That is going to give you the ability to take a batch and be able to drill down into the detail of that batch. So if you get a payment of thirty thousand dollars, You can click on it and it'll show you what actually is within that thirty thousand dollars. So if it's three transactions from Michael, three transactions from Nathan, all of that will be within those.
00:06:23 Michael
Badge details. Does that jive? Does that make sense as far as like what you all would be needing?
00:06:35 Val Levitan
Logically, it does, but neither Nathan nor I have practical experience with uh touching these things. We we we never we never touched it. But I have a hunch. Like inside of me, something tells me, but I cannot prove it yet. But something tells me when you Michael say we are integrated with Microsoft Dynamics, It tells me that we actually probably don't even need what we think an API is. We probably there's probably a much easier path.
00:07:23 Val Levitan
To the information that we're seeking. Through the fact that you guys, are already integrated with Microsoft Dynamics, and we use Microsoft Dynamics Cloud, which is always kept as a last version of Microsoft. So something tells me that this integration is already more developed than we thought. But.
00:07:53 Val Levitan
I don't know. I'm not an engineer, and I really don't know the subject. It's just my hunch.
00:08:01 Michael
So, what what I think we we should do is let's continue on in the implementation process. We know two things for sure:. The ZBA is going to work the way that you want it to work;. Those deposits are going to come into that one account. Once they hit that one account, they're going to be moved into another account. There is anything that you need to do. From there, We need to be able to provide you a means to be able to see a transaction detail report from those batches. So you get a batch of thirty thousand dollars, we need to be able to drill down and say, hey, who were the senders of these payments?
00:08:42 Val Levitan
As detailed as possible, including timestamps and any banking charges or service charges, transitional transactional charges. All of these things are important for us, and in the shortest possible time, almost if we could do it in real time, it would be the best for us.
00:09:02 Michael
So what I what what we what we'll do is let's continue on with the implementation process, as is okay. As far as the integration into Microsoft Dynamics, my thought is that you can still. So do that, But I don't think that Microsoft Dynamics is going to play as an important role in it, as you may need it to. Microsoft Dynamics is literally just going to be able to transfer the transactions within Business Banking into its ledger itself for you, so it's kind of like duplicate it. Now, Some people that some companies that work with them because they need that to be able to reconcile a little bit quicker.
00:09:47 Michael
If, there is going to be not any need for you to be able to utilize the front of Microsoft Dynamics to process payments or anything like that, if you are going to still do that through Business Banking, that's going to be a pretty easy thing. If you tell me like, "Hey Michael, I want to use the interface of Microsoft Dynamics, primarily for all of my banking needs," then we need to look at doing the transmission service. I don't think that's that, That's what we're looking at. I think that what we're looking at is really being able to see a way for these payments to come in, those payments to be transferred to another account, And then for us to have a means to be able to detail what those payments are within that single batch.
00:10:34 Val Levitan
Okay, let's you know let's do that. Let's try with you know let's have it as a starting point. We could always advance if we need to if we yes.
00:10:45 Val Levitan
You know, There is a Russian saying:" Y ou gain appetite. As you sit at the table, and you see meal in front of.
00:10:50 Val
You." So, when.
00:10:55 Val Levitan
We get a taste of it, maybe we say," Oh Michael, I cannot live without it. I don't know how I lived without it my entire life. I really need it. I want it." But right now, you are probably right. Let's just do something right now. Start working with it and then.
00:11:16 Michael
Okay, so what I what I will do, uh, Balin Nathan is I will move forward with the implementation process as is. We won't do the transmission or anything like that. And, then we will have someone today is Tuesday more than likely have someone that'll be contacting us to move it forward before the end of the week. Sounds good. Does that work?
00:11:43 Val Levitan
Is uh is there anything that Nathan needs to.
00:11:48 Michael
No, So what I think what I think is going to happen, Nathan is going to be best for you is once this is done for you to have access given to you on business that banking so that you can see exactly what the interface is exactly what that detail report looks like. Think then from there, You'll be able to decipher to say, hey, yes, this is exactly what we will need. Or hey, let's just run this a couple of months. And then we can. Press ure tested to see if we need to be able to add something additional to it.
00:12:19 Val Levitan
Okay, sounds good. Okay, okay Michael.
00:12:23 Michael
Okay, I'll get on that right after this call. And then we'll we'll be we'll be good from here.
00:12:27 Val Levitan
And uh what's the ETA for you to get things done on your end?
00:12:32 Michael
It's all all my stuff is already done. I was just holding it until we had this call. Cause I was I was lost and I wanted to make sure I understood what we were uh going to be needing before i it was sent in. So, I want to just, Press send after this call, and then they'll be contacting you within the next couple of days.
00:12:49 Val
Okay, terrific. That's really good. Thank you. Okay, thank you. Thank you guys. Thank you.
00:12:56 Michael
Take care.
00:23:33 Val
Where'd she get it? She got it somewhere, then she put it on her head. I guess what he does something. Get a new bowl of water. Well, then she came forward and she sat here, push me in, push me in, and she wastyping.
00:23:51 Val Levitan
Away andtyping in the uh. Get her one. Ooh wah.
00:23:57 Speaker 6
That whap thing? Bobby say honey?
00:25:44 Val
Okay, I will not forgive.
00:26:44 Speaker 6
Career. Just about it, got her all set up with this other colleague of yours. And then, remember I told you that I kind of maneuvered. I thought that I maneuvered as if she's signing up for.
00:27:25 Val
Hundred. And then the US, she was pretty much. Seven fifty is like five hundred dollars.
00:27:30 Speaker 6
Yeah, but the problem is that like there minus eight hundred, but it's a membership for the year, right So here it's also for the year, but she's not doing anything.
00:33:05 Speaker 6
I decided to do her a favor, cause I've gone so much. I got on that sale and link her account to mine and buy it all under her account. So she can get all the things. One of the products has a funky smell, so was that Baby Village find?
00:33:35 Speaker 6
I use them on a bunch of people, and I am trying to exchange it. Usually, It's so easy in S ephor a ;. It's like one of those places that they'll return anything you want a year later, if you want to return. But here is the one.
00:34:43 Speaker 6
My credit card, my phone number. No, no. If you have any questions.
00:37:11 Val
The point is, you have to cut down.
00:37:42 Val
Rearrange your lifestyle.
