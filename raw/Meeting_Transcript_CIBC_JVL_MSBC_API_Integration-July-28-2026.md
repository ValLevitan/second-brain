# Raw Transcript — CIBC/JVL ACH + Microsoft Dynamics API Integration
**Date:** July 28, 2026, 4:00 PM Eastern
**Summary note:** [[Meeting_Notes_CIBC_JVL_MSBC_API_Integration-July-28-2026]]
---

00:00:00 
Trying to make sure that I can move this along as far as what we're looking to do with these new accounts that have been opened for Leviton. I'll tell you that we already have the second account open. That's already been adjusted to be a ZBA. I'll explain to you the discussion that I've had with Val in the past as far as what this account structure is going to look like. There are going to be deposits that are going to come into the account. These deposits are going to come into the account via a third party. They're going to come in a batch format, so there is going to be multiple transactions in one batch. Once those deposits come into the account, they're going to hit the ZBA account. The ZBA account is then going to, at the end of the day, automatically transfer those funds out of that account into a separate account. So all of that is understood for me.
00:01:00 
In the gray area is the API, I mean not the API as far as the technology portion of it. When we are discussing how we want this to actually work with the API, I just need to understand exactly what needs to happen. And if that's already going to be in process or already going to be set up with what we have right now, I'll tell you with the Microsoft system.
00:01:31 
I did confirm last week. Hold on, I got notes here. I did confirm, last week.
00:01:50 
So with our Microsoft Dynamics, there is going to be an API connector. The API connector is kosher. We do have the ability to integrate Microsoft Dynamics into our Business Net Banking. When that is integrated, I think that's where it kind of gets a little bit fuzzy for me as far as what needs to happen once it's integrated. Are we going to be working directly through the Microsoft Dynamics system itself to process payments and not logging on to Business Net Banking?
00:02:28 
Or is Microsoft Dynamics simply going to be used as a means for us to be able to decipher the actual transactions as they occur on the account.
00:02:50 
I got it. How about that? So it's at the end of the chain. The API is for our system to verify the transaction, the money is deposited so that we can reconcile the ledger on our side. So if the automation is already there, for all those handling the deposits in this example, and the CBA is moving the money at the end of the day. Then after that, at some point after that money would move, our system would.
00:03:27 
Then call the API and verify the deposit and the amount that was deposited. As of now, that's what the API would do. We don't need to initiate any transactions, just verify the transaction history.
00:03:45 
So we just want to confirm that through Microsoft Dynamics, it is going to be able to translate our account history into the ledger within Microsoft Dynamics.
00:04:03 
I don't know if we have to go that far. All we need is something. If that's in the Microsoft Dynamics API, then that's where we'll get it. Wherever we can get the transaction history every day, our get whatever the last daily transactions were. That's where we need to make the call. I am not familiar enough with those systems to say yes. That's where we need to pull it from because it may not be if there is another API that just gives us a balance of that account or transactions on that account. That's what we can use.
00:04:43 
Let me break it down, what I think we may need. And then Nathan and Val, you guys tell me if it's something different. I know Val, we were talking about the usage of a transmission system to be set up. I don't really think that we need transmission services as of yet. This is what typically happens. So when we set up an outside aggregator like Microsoft Dynamics, when that's integrated into Business Net Banking, the transactions that are occurring on Business Net Banking will feed directly into Microsoft Dynamics. And then from Microsoft Dynamics, once those transactions are there.
00:05:24 
Then you will be able to confirm within Microsoft Dynamics the date, the dollar amount, and who the sender is of those transactions. Now what I don't know for sure, Nathan, is if I have this batch amount that comes in, if when that is translated into Microsoft Dynamics, it's still going to read that batch amount. If it is still going to read that batch amount, that's fine. What I can do now is set up a report within Business Banking. That is going to give you the ability to take a batch and drill down into the detail of that batch. So if you get a payment of thirty thousand dollars, you can click on it and it'll show you what actually is within that thirty thousand dollars. So if it's three transactions from Michael, three transactions from Nathan, all of that will be within those.
00:06:23 
Badge details. Does that make sense as far as what you all would be needing?
00:06:35 
Logically, it does, but neither Nathan nor I have practical experience with touching these things. We never touched it. But I have a hunch. Inside of me, something tells me, but I cannot prove it yet. When you, Michael, say we are integrated with Microsoft Dynamics, it tells me that we actually probably don't even need what we think an API is. There's probably a much easier path.
00:07:23 
To the information that we're seeking. Through the fact that you guys are already integrated with Microsoft Dynamics, and we use Microsoft Dynamics Cloud, which is always kept as the latest version of Microsoft. So something tells me that this integration is already more developed than we thought.
00:07:53 
I don't know. I'm not an engineer and I really don't know the subject. It's just my hunch.
00:08:01 
What I think we should do is let's continue on in the implementation process. We know two things for sure: the ZBA is going to work the way that you want it to work; those deposits are going to come into that one account. Once they hit that one account, they're going to be moved into another account. There is anything that you need to do. From there, we need to be able to provide you a means to be able to see a transaction detail report from those batches. So you get a batch of thirty thousand dollars, we need to be able to drill down and say, hey, who were the senders of these payments?
00:08:42 
As detailed as possible, including timestamps and any banking charges or service charges, transitional transactional charges. All of these things are important for us, and in the shortest possible time, almost if we could do it in real time, it would be the best for us.
00:09:02 
So what we'll do is let's continue on with the implementation process. As far as the integration into Microsoft Dynamics, my thought is that you can still do that. I don't think that Microsoft Dynamics is going to play as important a role in it as you may need it to. Microsoft Dynamics is literally just going to be able to transfer the transactions within Business Banking into its ledger itself for you, so it's kind of like duplicate it. Some people at some companies that work with them because they need that to be able to reconcile a little bit quicker.
00:09:47 
If there is going to be no need for you to be able to utilize the front of Microsoft Dynamics to process payments or anything like that, and you are going to still do that through Business Banking, that's going to be a pretty easy thing. If you tell me, "Hey Michael, I want to use the interface of Microsoft Dynamics, primarily for all of my banking needs," then we need to look at doing the transmission service. I think that what we're looking at is really being able to see a way for these payments to come in, those payments to be transferred to another account, and for us to have a means to be able to detail what those payments are within that single batch.
00:10:34 
Let's do that. Let's try with that as a starting point. We could always advance if we need to.
00:10:45 
There is a Russian saying: "You gain appetite. As you sit at the table, and you see meal in front of."
00:10:50 
You." So, when.
00:10:55 
We get a taste of it, maybe we say, "Oh Michael, I cannot live without it. I don't know how I lived without it my entire life. I really need it. I want it." But right now, you are probably right. Let's just do something right now. Start working with it and then.
00:11:16 
So what I will do, Balin Nathan, is move forward with the implementation process as is. We won't do the transmission or anything like that. Then we will have someone today, since it's Tuesday, more than likely have someone that'll be contacting us to move it forward before the end of the week. Sounds good. Does that work?
00:11:43 
Is there anything that Nathan needs?
00:11:48 
So what I think is going to happen is that once this is done, Nathan will be best for you to have access given to you on business banking so that you can see exactly what the interface is and exactly what that detail report looks like. From there, you'll be able to decipher whether to say, 'Yes, this is exactly what we will need,' or 'Let's just run this for a couple of months. And then we can pressure test to see if we need to be able to add something additional to it.'
00:12:19 
Sounds good. Michael.
00:12:23 
I'll get on that right after this call. Then we'll be good from here.
00:12:27 
And what's the ETA for you to get things done on your end?
00:12:32 
It's all my stuff is already done. I was just holding it until we had this call. I was lost and I wanted to make sure I understood what we were going to be needing before it was sent in. I want to press send after this call, and then they'll be contacting you within the next couple of days.
00:12:49 
Terrific. That's really good. Thank you. Thank you guys.
00:12:56 
Take care.
