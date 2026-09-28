# Raw Transcript — Payment Hub — Location Billing & Collection workflow
**Date:** January 6, 2026, 11:17 AM Eastern
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Summary note:** [[Meeting_Notes_Payment_Hub_Billing_Collection_Workflow-January-6-2026]]
---
00:00:11 Speaker 1
So this will be the workflow here. So we're going to create the header. MSVC works. So we'll create the header. We're going to add the invoice line, the invoice within. So then here at the bottom, different types of failure modes, recommendations on how the system should respond, how do we recover from these.
00:00:42 Speaker 1
So these will really need everyone to review and make appropriate changes on how the system should respond, how JVL is going to respond with support. And then alert condition chart. How do we get an item for the team?
00:01:13 Speaker 1
But we also have teams in email. And this is just a structure that we could use, but, again, not part of the requirement, just recommendation on having an alerting structure. We have retry behaviors that we're going to have to implement with MSBC. So the job is going to have to be able to have different error conditions. So let's say we get an MSBC.
00:01:43 Speaker 1
We may want to alert immediately, or we may want to have a retry strategy that attempts to retry with MSBC.
00:02:11 Val
It's a lot of information.
00:02:14 Speaker 1
Yes. This is a big...
00:03:20 Speaker 1
So the copy will go to the copy company because we will maintain the relationship tickets and. the relationships.
00:04:46 Speaker 1
So that's the only way for them to make a good idea.
00:06:10 Speaker 1
So what I wanted is this, I agree, we should, maybe that's all an MSBC side, MSBC is sending.
00:06:53 Speaker 1
Val, was that something we wanted to do, is have MSBC send the actual invoice, or will PaymentHub initiate the email.
00:07:03 Val
No, it should be MSBC.
00:07:08 Speaker 1
Okay, so MSBC will already have that capability, so this is, I think, something.
00:07:17 Val
The PaymentHub should be exactly what the name is, it's a hub. It should not be really a brain of any sort, or a database of any sort.
00:07:43 Speaker 3
Okay, so I'll remove that.
00:08:25 Speaker 3
So if I go up one, so this, most of this will be covered.
00:08:43 Speaker 1
This is actually delivering the invoice. So we have it in here, but I think unless there's something that payment hub just triggers, it may just be the post. When we do our final post, notify invoice is complete and ready. That may be all we have to do. But this one's pretty simple.
00:09:15 Speaker 1
It's just going through the criteria of the invoice. what it should look like or how it should look like. Again, tracking, probably already done, and delivery time. So this, we'll have to learn if we can send it at a specific time,
00:09:49 Speaker 1
controllable and un-controllable by Payment Hub. But either way, Payment Hub will commit the final posting of the invoice, so 1 to 1.30 in this. And then at 8 a.m., Payment Hub is going to start initiating the cost checks. So then we'll have to know. We'll still have the invoice information that was submitted,
00:10:19 Speaker 1
but it can then initiate ACH balance checks. invoices. So in failure modes that could exist, it's just the providers again that probably don't.
00:10:51 Speaker 3
need to worry about that in payment. I think we can review this one a little more in depth.
00:11:13 Speaker 1
once I have a better understanding of what I need to do with MSNBC to get it to email and how do we know it. Okay, so our balance verification, this is what we'll fire off as we get closer to the time to initiate the ACH transaction. Right now, we're going to initiate these using 8 a.m. Central.
00:11:43 Speaker 1
This is Central time, just aligns with dual documentation. So the dual cutoff is 9 a.m., so this is in processing. This should be configurable if we decide we need to go a little bit early, 7 or 6 a.m. But we're going to, at this time, we'll do a balance query through the dual endpoint. And once we have that information, we'll just compare that with the open invoices for that location or open invoices.
00:12:29 Speaker 1
We should be initiating these payments every day. So on the weekend, for example, on Saturday, it's a payment on Saturday, we initiate a payment. Those will be queued up in Douala, but they won't add up. So when we get to Monday, the previous two days have actually been queued up.
00:13:01 Speaker 1
So when we do a balance check, we should look at all of our pending invoices and ensure that because we may not want to add a third invoice, or we may want to just, rather than initiating another ACHP, just disable it, but considering it.
00:13:33 Speaker 4
In that scenario, how would we re-trigger an invoice if we, is it manual at this point in time? If we manually stopped it.
00:13:44 Speaker 1
Correct. So we need a manual way to, so if we determine they have, and we disable the location and we don't initiate an invoice, there has to be a manual process to, one, reactivate the location, and then resubmit invoices. Now we may, the resubmit would be done through MSPC if we needed to resend it to the customer.
00:14:16 Speaker 1
But to activate, once they're reactivated, the payment hood should just be processing them on the next, or we have a manual way to trigger, we reactivate them and we trigger. process. Does that answer your question? Yeah, I think we'll have to unpack how JVL wants to.
00:15:04 Speaker 1
respond. How do we, because the payment hub can easily disable a location, but what are the steps.
00:15:12 Speaker 4
to get them re-enabled? Yeah, and I guess we need to make a decision on our side. Let's just say the customer owes us $2,000 for yesterday. We see they only have $1,000 in their account. Why would we not want to cost about $1,000 and they just still owe us the $2,000? You know, that will trigger a sufficient fund, but that's also how it comes not to keep the account.
00:15:51 Speaker 4
You know, the penalty of the fee should occur.
00:15:55 Speaker 1
Yeah, I think as long as we don't split the invoice, a single invoice, so if it's a $2,000 invoice, but we only bill $1,000, according to the NACHA, if it does an exact invoice, the customer can more easily dispute it. But if they have multiple invoices, two of them are less than $1,000 together, the last one.
00:16:32 Speaker 1
pushing them over their maximum. We could then conceivably create ACH transactions for the first two invoices, the Saturday and Sunday, and then disable them because they don't have enough to cover the invoice. I guess it would be, yeah, they cover Friday, Saturday, they don't have enough to cover Sunday. So we create transactions for Friday, or we let those ACH transactions go through pending. But as long as we don't do a partial draw on an invoice total, I think we're.
00:17:20 Speaker 5
Nathan, just one question to clarify. You said that we can run. ACH transactions, even on Saturday and Sunday, and to wait from DWALA status of execution on Monday related to these two transactions.
00:17:52 Speaker 1
DWALA will queue them up, so we can go ahead and complete our processing on each day.
00:18:02 Speaker 5
As an alternative, do not post any request to DWALA until working day. But in this case, we will need to know the calendar related to Georgia, for example, and know what's working.
00:18:22 Speaker 1
That's correct. If we do it, yes, and we can do it that way. is if we learn that all of a sudden we billed for Friday and Saturday and then over the weekend their checking account is drained and now they can't cover those previous payments that we started, we can cancel those with Duvalo.
00:18:53 Speaker 1
But in your case, what you're saying is if we didn't initiate them, then there's nothing to worry about. We just put the account on because they can't pay.
00:19:07 Speaker 5
In case of a date package, we will be sure that all the payments are either paid by the customer or not, or they do not have sufficient time in case when we have to postpone.
00:19:48 Speaker 1
So we'll have to know what days can we initiate an ACH that they'll actually be processed, and then the logic to handle invoices, how they're submitted. Do we reconcile? If they have three invoices, do we reconcile? They can actually pay for two of them.
00:20:19 Speaker 1
We submit those, and then deactivate because they can't.
00:20:58 Speaker 3
Okay, so we determine they have sufficient funds, and we update the invoice status to.
00:21:39 Speaker 1
ready for payment. This will trigger the initiation. The next step would be initiating this with DWALA, and then we'll have to determine, so we know the insufficient funds. Insufficient funds is flagging the location and disabling the POS. So we'll mark balance check as failed. We update their status to insufficient fund.
00:22:12 Speaker 1
Disable the term. Resubmit the location to an operations team. It can be whatever JVL needs, whatever kind of internal notification you want. Then we log our failure with balance detail. I started looking at regulations and what kind of data we need on balance checks because we are getting more personal account information.
00:22:44 Speaker 1
We may or may not be able to record the actual balance number. We can get the actual balance. So we can compare it, but I'm not sure we can keep it without stepping into more strict regulations. But we may want to do that anyway. So I guess it'll be important for us to figure out if there are more strict regulations there and what we need to do. It may be because Douala backs away their account numbers with the Douala source ID, funding source ID.
00:23:32 Speaker 1
But that may be fine. Then we're not associated with the actual bank account number.
00:23:44 Speaker 5
Actually, I think we need to add one line here, at least a message that will be displayed on the POS device. Um... When it locked.
00:24:01 Speaker 3
Ok, so we're going to display a message on KLS.
00:24:19 Speaker 4
What do you mean manually disable that location you mean.
00:24:25 Speaker 5
Doesn't matter what purpose. Manual lock or automatic lock due to insufficient balance.
00:25:01 Speaker 1
Okay. And this is just diving a little bit deeper. Again, examples on how this may work. This assumes right now we're only, as far as I know, we're only going to have one terminal at a location, but this is just calling out if there would be more than one for that location, they would all be disabled. Let's see. Yeah. So this is, I think, going into what you were saying, Pavel, is we don't have to run balance checks. Whether we initiate the transaction or not, we don't have to run balance checks over the holiday and the weekend because there is a fee for actually running these.
00:25:56 Speaker 1
When we have, you know, in the hundreds of locations that we don't want to run these at all and we do everything once on the next business day.
00:26:11 Val
But the charge is very minimal. It's 17 cents. So we may want to do it anyway to compare with what they've already queued up. Well, I'm not sure if my thinking is correct, but should we continue validating cards if we know that there's no money on the account?
00:26:51 Val
And the answer might be yes. because.
00:27:03 Speaker 4
And they have the ability to fund their account right up until we actually attempt to collect it.
00:27:14 Val
Or they may have an overdraft set up on their account. Which is an interesting idea, should we ask if they have an overdraft on their account? Is there such a flag? That would be an interesting one.
00:27:35 Speaker 4
I would almost say that we add that as a suggestion for the License Service Agreement, Location Service Agreement. We recommend that they do that. Yeah, that's interesting.
00:27:56 Val
At this stage I cannot answer whether... there is any useful, practical purpose of asking for the account balance. But regardless, I think we should put it in the requirement and see if it becomes not useful, then we'll just, you know, option it out.
00:28:30 Val
I cannot answer whether it will be useful or not. I have a mixed opinion.
00:28:47 Speaker 1
All right, so holiday and weekend, that goes into the multiple invoice handling. So this creates the scenario of multiple invoices. totaling due of $815 on Monday, so a balance check would give us, we could do $815 as for always, and that's the approach this is taking, and I probably should see how this might play.
00:29:23 Speaker 1
out, but they may only have $500 when we check their balance, so we say, okay, starting at the top, can they pay the first invoice with $500, yes, then initiate that transaction, block the location because invoice two and three are outstanding, so I think I'd like to create some more scenarios with that, maybe we just need two more.
00:30:26 Speaker 1
So again, so right now the requirement is written as all or nothing. If they can't cover their total, we don't initiate any transactions. We just lock the location.
00:30:40 Val
Was there any NACHA regulation based on all or nothing.
00:30:45 Speaker 1
Not when it comes to multiple invoices. So in this scenario, if we bill just for invoice one, there's no, we're not at risk of anything because we're billing the 333.48 exactly what that invoice is for.
00:31:09 Val
So there is NACHA regulation based on partial payment of the invoice, but not on the partial payment of the total amount. Correct. If it matches a singular invoice.
00:31:26 Speaker 1
Correct. So, right, if we, so this may, another thing we may, thinking through this, we check their balance for A15. In order to comply, we would probably still initiate three draws, because we have three different invoices, and we want our ACH transactions to match those invoices exactly. So we would have to initiate three draws on this, in this scenario.
00:31:59 Speaker 5
Especially here, it could be a question. If they have 800, and we can request, it's not enough to pay for three invoices, but we can take invoice. For yesterday and day before yesterday, but skip invoice for Friday.
00:32:34 Speaker 5
Correct. If it gives us more money.
00:32:42 Speaker 3
Correct. Yeah.
00:32:49 Speaker 4
Change more. Okay.
00:32:56 Speaker 1
So we go with an approach of we cover as many invoices as we can in this scenario, and then disable if we can't cover all of them.
00:33:07 Speaker 4
Yeah, because I would say Business Central's expertise in what's outstanding on an invoice, that's what it does for a living, so we shouldn't be worried about losing tracking of owed monies. I mean, that's what Business Central does. so we're going to update that yeah it's a good solution and then uh as part of the monthly.
00:33:48 Speaker 4
statement generated by business central you know perhaps you know business central can show, the customer hey invoice number one and two have been paid three is outstanding you know so that uh they're less likely to dispute it because we're clearly showing them what happened.
00:34:07 Val
yes yes that that could very well happen easily yes.
00:34:25 Speaker 1
So we have the idea of a manual balance check in the system, and this may or may not be needed, but this may be something we want to be able to initiate manually if we're basically in the reactivation process, whatever the reactivation flow is for a location, if a manual balance check is needed. If we don't have this, then it's going to be, I'm assuming, the customer's going to say, yes, we're good, let's reactivate JVL, reactivates, and then when the process kicks off again, it's going to do this anyway, and would disable them again if they didn't.
00:35:10 Speaker 5
Just one note here, just one idea. Let's assume that... ACH window is closed for today, and we locked the location. At some moment, a customer informed us that he filled his account with money, and actually we can manually check this balance.
00:35:45 Speaker 5
But I'm not sure that this is a good trigger to re-enable the location, because if we enable the location, they will continue working. But at the moment when we actually initiate ACH transaction, probably at this moment they do not have enough funds, even for yesterday and plus the next day. Correct.
00:36:15 Speaker 1
Right. So a similar situation to the weekend. their funds are going down and they wouldn't have enough to cover everything and do we keep them do.
00:36:27 Speaker 5
we allow them to continue generating particular conditions open question because we can check balance at any moment but we do not immediately initiate the exchange transactions and block their money at this moment.
00:37:27 Speaker 1
Okay, so again, failure modes and then suggested responses to these. Something for our review when we actually make policy on how to approach all these situations. And then, again, alerting. DWALA retry behavior. So DWALA does have recommendations on how to do retry with them that were not,
00:38:05 Speaker 1
because they may treat rapid retries as some type of attack. So that's going to really just be the engineering strategy and how they want to do retries with DWALA. And then, let's see, I had some open questions here. So the partial coverage strategy, we just talked about that, and I'm going to change the status back to,
00:38:42 Speaker 1
so I guess the two options left, I do all or nothing, is do we pay oldest first or do we pay what we can't? That would be the system deciding of three invoices. Let's say they only have $100, which one do we pay? I think the simplest solution is to go oldest first, until we can't cover the invoices.
00:39:18 Speaker 1
So we'll do oldest first.
00:39:29 Speaker 5
Oldest first or those invoices that give more money in different order.
00:39:41 Val
Not more money, he meant to say more cash, brings more cash. Combination of invoices that optimize the amount of cash brought into the company.
00:39:54 Speaker 1
Okay, so that would be C.
00:39:57 Val
That's a great point, Pavel.
00:40:02 Speaker 4
I took that to mean that we target dealers, but we're going to take all of the cash and apply it oldest first, and then whatever's left is whatever partial payment on an invoice. I think we're kind of all saying the same thing.
00:40:19 Val
We cannot do partial payment on an invoice. We could do partial payment on the total amount, but it has to be singular invoicing.
00:40:30 Speaker 4
Why? Why can we not do a partial payment on an invoice.
00:40:33 Val
According to NACHA, we can't.
00:40:37 Speaker 4
No, I thought it was according to NACHA, it leads to further customer dispute possibility.
00:40:45 Val
Yes.
00:40:46 Speaker 4
We certainly could, actually.
00:40:47 Val
Correct. We could, but it opens a dispute possibility.
00:40:53 Speaker 1
Yeah. It's easier for the customer to win a dispute if we don't actually invoice them out.
00:41:08 Speaker 4
So then this is going to be interesting business logic. If Business Central can actually juggle which invoice to pull from based on the...
00:41:20 Val
Business Central cannot, but Payment Hub can.
00:41:27 Speaker 1
Correct. So Business Central would invoice, would send the invoices. Payment Hub will decide which ones we initiate payment on. Okay. So balance check timing, we have it at 8 a.m. We may decide we need an earlier buffer. I know in our initial, we're going to have, you know, whatever it is up to.
