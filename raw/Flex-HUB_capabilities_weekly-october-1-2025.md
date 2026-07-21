**Transcript**

October 1, 2025, 12:01PM

**Nathan Carver** started transcription

**Nathan Carver** 0:03  
Uh, we'll dive right in. So um update on ACH vendor. So Pablo, Juan and myself, we met with uh the Duwalla demo team on Monday and we went through the dashboard of how their platform works.  
Works and how we would integrate with it. We have access to their sandbox now where we can simulate a complete environment doing debits or doing ACH debits on on accounts.  
We can even access this. They have API keys so we can actually access this environment from code if we want to experiment. Duala sent us their pricing yesterday.  
I can share that out, but it looks.  
I don't know Juan, if you had a chance to go through it. I think it looks pretty competitive.  
For us, the catch with Duwalla is they have a minimum per month which may affect us in the very early stages. So they have all their fees below, but if if the fees don't total $2500 for the month, that's their.  
That just becomes their flat fee at 2500.  
Um.  
The other pricing, uh, seems OK.

**Juan Martinez** 1:32  
Oh, Nathan, I'm sorry, real quick. So it's not the, it's not the platform service fee of 2500 and there's a plus plus the 2500 for the monthly minimum usage fee. So we're starting out at 5000.

**Nathan Carver** 1:47  
Oh, I see what you're seeing. Yep, you're right. Yep, you're right. So that's a flat fee regardless of what we use. Plus, yeah, that makes the 5000.

**Juan Martinez** 1:47  
That that's how I understood.

**Nathan Carver** 2:00  
So that's pretty, I think, pretty steep for us at the beginning. I also spoke with Stripe yesterday and they're going through our use case. They were going to send me something either late last night or the today. They'll send me an update.  
Um.  
And but looking at their pricing model.

**Val Levitan** 2:22  
Can can you?  
Can you send me that pricing sheet?

**Nathan Carver** 2:27  
Yes, I'll send that to you.  
So looking at their pricing model, they don't have a flat rate, they just have.

**Pavel Frolov** 2:32  
Sure.

**Nathan Carver** 2:37  
8% of the transaction up to a $5 cap on ACH direct transfers.  
So this seems significantly cheaper, especially in the early stages of the platform.

**Pavel Frolov** 2:54  
This is stripe.

**Nathan Carver** 2:57  
Correct. Yeah, this is straight.

**Juan Martinez** 2:59  
OK.

**Nathan Carver** 3:01  
So I expect to hear back from them today. Um.  
If not, I'll follow up.  
The one interesting thing with Stripe I found was they might, they may be able to do batch processing for us. So we would send them the batch of transactions we want to initiate and they would.  
Manage all of them. So rather than us in the future, rather than us having to initiate 2000 separate debits for, you know, 2000 locations, we would just hand that off as a batch job to Stripe.  
And they would execute on that, so um.  
The sales guy I talked to is gonna go look at that. I don't know his technical competency, so he may not understand what the ask is, but he's at least taking that to their team as an option for us.

**Pavel Frolov** 3:46  
Yes.

**Nathan Carver** 4:00  
So I I see the.

**Pavel Frolov** 4:02  
Mhm.

**Nathan Carver** 4:04  
I think these are these are good options. There was also Emilio that I wanted to connect with at Juan shared with me. So I'm going to do that. I one of the things I'm seeing is these are pretty similar. So as long as we.

**Val Levitan** 4:19  
Yes.

**Nathan Carver** 4:21  
Design our system where we can adapt.  
A provider into it. Um, it's not gonna slow us down as far as our initial development.

**Val Levitan** 4:30  
Right. Can I please see this pricing as well?

**Nathan Carver** 4:34  
Yeah, let me drop this link in the chat.

**Juan Martinez** 4:39  
Well, does it make sense for us to just put all the pricing into a spreadsheet to do a side-by-side? I think that would help all of us, I think.

**Nathan Carver** 4:50  
Yeah, do that.

**Val Levitan** 4:52  
Or idea.

**Juan Martinez** 4:57  
So Nathan, I converted the Dewala sheet to Excel, so I'll share that with you here shortly.

**Nathan Carver** 4:57  
Uh.  
Oh, OK, perfect.  
Um.

**Juan Martinez** 5:07  
Actually, I was.

**Val Levitan** 5:08  
But but it seems that we must charge something. I don't know what it is, but.  
There is a charge for every transaction to some extent. I don't know what it is. It depends on the supplier and I think at the end they'll be pretty similar. They will, you know.

**Pavel Frolov** 5:18  
OK.

**Nathan Carver** 5:21  
Correct.

**Val Levitan** 5:28  
But but but there will be some sort of a charge that we.

**Juan Martinez** 5:29  
Yeah.

**Val Levitan** 5:35  
Need to.

**Juan Martinez** 5:35  
Yeah, for for up, yeah, in the Diwalis scenario, we do 1000 transactions per month. It it's 18 cents, a flat 18 cents.

**Val Levitan** 5:48  
Plus 2500.

**Juan Martinez** 5:51  
Plus 5, plus 5000 Val, not 2500, it's 5000 and it's a $1500 one-time integration fee that's at the very bottom there, you know. So for that first customer, there's that additional 1500 while we work out the.

**Pavel Frolov** 5:51  
Mm.  
Actually.  
Yeah.

**Juan Martinez** 6:11  
API connections and all that.

**Pavel Frolov** 6:15  
So if you take just $0.50 from each card activation, we need 10,000 transactions per month to get a 0.

**Val Levitan** 6:29  
No, no. These are different. These are different charges and different risks. These are different risks.

**Juan Martinez** 6:34  
Yeah.

**Val Levitan** 6:36  
So when we charge $0.50 per card activation, this is to mitigate our risk to income.  
We're now talking about risk for ACH transfers, risks and cost associated for ACH transfers. So it looks like it's.  
$1500 plus $5000 a month plus.  
$0.15 per transaction. Something like this.

**Juan Martinez** 7:11  
Yeah, and and the column there labeled standard. I didn't want to steal your thunder, Nathan, but that the T3 plus the T1 standard means ACH transaction Val could take up to three days, so.

**Nathan Carver** 7:26  
Correct, yeah.

**Juan Martinez** 7:27  
What what's tiered here is as you go farther towards the right, if we want same day ACH, now we're talking about $0.48.

**Val Levitan** 7:37  
$0.48 per transaction, but transaction isn't a batch, right? That's a daily transaction.

**Juan Martinez** 7:44  
Yeah, up to 1000 transactions, yes, $0.48.

**Val Levitan** 7:51  
1000 transaction. How can we 1000 transaction from the same address or from different addresses?

**Juan Martinez** 8:03  
Mm.

**Nathan Carver** 8:04  
Uh, from what I understand, it should be just total total transactions regardless of the bank, the source account.

**Val Levitan** 8:11  
So if there are 100 different accounts, it would still the same $0.50.

**Nathan Carver** 8:19  
Yeah. So if we had 100 locations and we we debit them, let's say just 20 days in a month, that puts us at the 2000 transactions.  
So that puts us at Tier 3.  
Um.  
So I think we would quickly go up the tiers once we had, you know, the 2000 locations.  
But at the at the beginning we're gonna be I think well within that Tier 2, that first, that first Tier 2.

**Val Levitan** 8:54  
What do you mean by Tier 1, Tier 2? I don't see. Where is it?

**Nathan Carver** 8:58  
On the left of the.  
Pricing.

**Val Levitan** 9:03  
Uh, OK.

**Nathan Carver** 9:05  
Yeah, so they're that's just how they're qualifying. It looks like there's no tier one, so I'm not sure what that means, but.  
We we can verify that with them, but I I'm reading this as total transactions form the JBL account which would include.  
Every location aggregated together.  
So my initial read on these is um stripe appears to be.  
And I think Juana's idea, we need to put the numbers side by side and and create some scenarios. Also wait till Stripe gets back to us, but just seeing their base pricing, they seem to be more geared towards smaller number of transactions which aligns with our.  
With our rollout stages.  
Um, to all this, Duola really seems to be geared towards the high volume. It's where we start to see savings.

**Juan Martinez** 10:12  
Yeah.  
And uh, OK, go ahead, Nate.

**Nathan Carver** 10:20  
Um.  
Oh, just so.  
I don't think it's beyond. I think it's reasonable for us to take the approach of if we had to do a cheaper vendor up front and then we swap out that vendor. If we build our system accordingly, we should be able to change vendors relatively seamlessly.  
Without disrupting the system, we even have a potential design to have two vendors and have a fall back vendor if the first one was not able to process transactions for whatever reason.  
So that's it. Go ahead, Juan.

**Juan Martinez** 11:02  
No, I I was just gonna almost say exactly what you said is Val what what the what we're seeing on screen it the the numbers are you know it does look expensive at first glance but what the Diwala presentation.  
The level of reporting, the automated emails that they send on behalf of JDL to alert customers that money is low, that they haven't paid. There's a bunch of service in there which we may not need in the beginning, but.  
It could be valuable in the future as as Nathan said where we we should consider having the ability to switch to something like a Diwala which is a more robust solution in helping us track down you know lack of payments or or customers who are consistently not funding or.  
All sorts of things that they do as an automated process.

**Val Levitan** 12:01  
But regardless, we will have to charge something.

**Juan Martinez** 12:06  
Yes.

**Nathan Carver** 12:07  
Yes.

**Val Levitan** 12:08  
And most likely this should.  
Be some sort of a.  
Minimum monthly fee plus transaction fee.

**Juan Martinez** 12:26  
Yeah. Once we get the pricing from from Stripe and and I'll take it on myself to put this into a spreadsheet. Val, I'll, I'll bounce back some suggestions based on all of the pricing that we've gotten just so we get a sense of a monthly recurring fee and then maybe a.  
Daily transactional fee, whatever it is, so that we can cover at least a percentage of our costs, if not 100%.

**Val Levitan** 12:56  
Well, hold on a second. We're in this business because we want to make money. If we don't make money, we don't want to be in this business. So, so we're not, we're not going in here to lose money.

**Juan Martinez** 13:03  
Sure, sure.

**Val Levitan** 13:09  
And ACH transaction is essential and let's say time plus three days or time plus one day. It's not a solution. We need immediate statement.  
Otherwise we're taking a huge risk on validating a card and you know, not getting the money. This is a this is a street business. It's that's no joke. You will have all kinds of jokers out there.

**Juan Martinez** 13:31  
Yeah.

**Nathan Carver** 13:43  
So are we looking at immediate, immediate draw or the T + 0 is the same day? So based on what I've learned is if you there's 33 windows of transactions.  
In a given day for ACH processing, so you there's like a 10:00 AM Eastern Time.  
Cut off for same day ACH processing. So if you submit your transaction within that first window of time, by the third window of time, I believe that's when the money would have cleared the transfer. So there's still a a delay.  
It's not immediate, even though it says T + 0.

**Pavel Frolov** 14:29  
Actually I think even in case of same day ACH, it relates to business day doesn't cover Saturday and Sunday.

**Nathan Carver** 14:37  
Correct.

**Juan Martinez** 14:41  
Yeah.

**Nathan Carver** 14:42  
Correct.

**Pavel Frolov** 14:43  
That is a key point I think.

**Juan Martinez** 14:46  
Yeah.  
Yeah, I mean we're we're we're basically going to be reconciling the day before, not the day of because of that cut off time. So there's there is going to be a gap of because of that. It's not like they say well what time of the day would you like us to collect when we know most of the gaming.

**Pavel Frolov** 14:51  
Yes.  
Pizza.

**Juan Martinez** 15:08  
Happens, you know, later in the afternoon into the evening that that's unrealistic. So we won't be able to capture the, let's just say 2:00 PM to 10:00 PM play because of the timing of of the data capture or the ACH transaction initiation.

**Val Levitan** 15:28  
And we actually need the most gaming will happen between 2:00 PM and 10:00 PM.

**Juan Martinez** 15:34  
Yes, correct.

**Val Levitan** 15:49  
OK, let's keep on working with these providers. The T + 0 is important for now, but let's see where we're gonna get. Let's let's try to figure out the charges.

**Nathan Carver** 16:00  
OK.  
Um, the other thing we can.

**Juan Martinez** 16:05  
Yep.

**Val Levitan** 16:05  
Because right now it's a little hazy because if we have to dish out $5000 per month regardless.  
Even if we have 100 accounts.  
You know, that's a minimum of $50.00 a month per account.  
Plus processing feeds.

**Juan Martinez** 16:25  
Yeah.

**Nathan Carver** 16:29  
Correct.

**Val Levitan** 16:29  
Seems like a processing fee is about 1% or just under 1%.  
So it's about $50.00 per month, plus 1%.  
Uh.  
Can uh somebody verify with um?  
Income if there are similar charges for using that handheld machine, I forgot the name of it.

**Pavel Frolov** 16:59  
The packs.

**Val Levitan** 17:01  
Apoxia.

**Nathan Carver** 17:01  
Hmm.

**Val Levitan** 17:05  
Can can somebody assume this undertaking please?

**Juan Martinez** 17:05  
Sure.

**Nathan Carver** 17:06  
Yeah.  
Yep, we we can do that.

**Juan Martinez** 17:08  
Good.

**Val Levitan** 17:11  
Cool.

**Nathan Carver** 17:13  
Um.  
We can reach out to John.

**Val Levitan** 17:17  
So Nathan, you will.

**Nathan Carver** 17:18  
Yeah, yeah, I'll reach out to John.

**Val Levitan** 17:22  
OK, John, nothing come.

**Nathan Carver** 17:24  
John, John, and Tom, yes.

**Val Levitan** 17:27  
OK.

**Juan Martinez** 17:28  
Val, yesterday you you asked me about balance checking and and you see the very last item on the sheet. There is a 7 cent charge per balance check, so they could be checking the customer's accounts.  
As you asked, that is an option. There is a charge for it.

**Val Levitan** 17:55  
Yeah.  
I'm assuming, uh, about 50 bucks per account.  
Monthly plus 1% transaction fee.  
This is probably in my mind. This is what we should be charging.

**Juan Martinez** 18:18  
Sure.

**Val Levitan** 18:21  
But of course, this is just a preliminary view. OK, good. Let's park it. Let's move on.

**Juan Martinez** 18:27  
OK.

**Nathan Carver** 18:31  
So the next thing on my priorities was beginning the architectural design of our ACH processing. So I saw Pavel, I saw you added me to those racks in Jira. I can start using those.  
At the moment I just I just created a module under the system architecture for the reconciliation engine is what I'm calling that and taking the system as it's set up. Currently I put together the.  
How that reconciliation may interact with the rest of the rest of the system. And so I've got that diagram out here and with some of the initial requirements that are part of that.  
I guess what I'll need is just what numbers to assign them. I just gave them 99 so they wouldn't interfere with any existing numbers. So I've started a a the batch processing orchestration out here.  
What that design's gonna look like, the requirements that I'll start putting in the system, and then just started putting together what a component design might look like. Um.  
Again, this is just using some concepts of the spring batching and using a lot of the spring framework for this. I don't know if the architectural patterns are gonna move into some more Azure based like worker queues or.  
Uh, things of that nature. Uh, but I can start integrating this in with JIRA now that I have those. Um.  
Those tickets.

**Val Levitan** 20:16  
Amazing. Fantastic. Love it.

**Nathan Carver** 20:19  
Um.  
Um, that's it for me, I think for my.

**Val Levitan** 20:25  
So a top a top level question. Um, can you take me through uh?  
I don't know architectural design. How long does it usually take to solidify an architectural design and and what comes after an architectural design is completed?

**Nathan Carver** 20:49  
So um.  
So the design itself, this gives us a base concept. So from here I think what the engineering team would do is take these ideas and translate them into the patterns that they're using and.

**Val Levitan** 21:05  
By what do you mean by parents?

**Nathan Carver** 21:08  
So if Pavel has his, Pavel has his own design with his team and so taking this idea of.  
The batching triggering every let's say this one is scheduled at 7:00 AM every morning. It's going to trigger the settlement. It's going to calculate all the locations amount due to JVL and initiate jobs to start transfers for each of those locations, so.  
That is all based on the framework of the existing system, so those are assumptions I'm making. Pavel and his team may have a different framework, so I think the next step in the design is.  
For the engineering team to morph this into something that makes sense, it may maybe they just take it just as it is and say, yeah, this is good or they're gonna evolve it a little bit. So the next step would be evolve the design.

**Val Levitan** 22:04  
Yes.

**Nathan Carver** 22:07  
Shouldn't take too long and then start building out some components.  
See how those components are fitting together, test them out and then go back to design and it's just gonna be an evolution. So write some code, update your design, write some code, update your design.

**Val Levitan** 22:25  
Is there a design review process before we before you guys agree on something?

**Nathan Carver** 22:36  
We have no official process. I guess in that case, Pavel, if you have a an approach you want to take to this, I can keep putting my design thoughts out here and you all can run with them or we can.  
We can iterate on them.

**Pavel Frolov** 22:55  
Yeah, actually I think first of all we need to to review this with developers, get their thoughts, fix this probably and then I I I will share.  
Changes with Nathan to agree on this or not.

**Nathan Carver** 23:15  
Yeah, that sounds good.

**Val Levitan** 23:17  
So what's the time frame for this?

**Juan Martinez** 23:18  
Yeah.

**Pavel Frolov** 23:23  
Actually right now we have a scheduled some features starting from beginning of November start developing of ACH.  
So until this date, I think we will need to finalize at least don't understand that we are going to work with or some other provider and to understand this architecture schema.  
Oh.  
If you are going to to do this this way.

**Val Levitan** 24:11  
Is this under the payment hub in Jira plans?

**Pavel Frolov** 24:15  
Yes, yes.

**Nathan Carver** 24:17  
Yes.

**Val Levitan** 24:18  
So which?  
Uh.  
Feature is a thunder or.  
What do I What do I look under?

**Pavel Frolov** 24:27  
Um.  
BEP.  
Uh, 2656.  
ACH API adapter and the next BEP 2657 ACH API adapter and reconciliation module for payment hub.

**Nathan Carver** 24:40  
OK.

**Val Levitan** 24:51  
OK, so.  
BP.  
2656 and 2657, there is nothing under them. So what what should there? What should? How should we update the schedule now?

**Pavel Frolov** 25:05  
Yes.

**Val Levitan** 25:12  
Well, what's gonna happen? What? What's gonna happen now? I It's hard for me to picture.

**Pavel Frolov** 25:12  
Before to add.  
Uh, we do not know what will be under this features exactly.

**Val Levitan** 25:34  
Well.  
After we hang up the phone, what's going to happen?

**Nathan Carver** 25:41  
So there was some new tickets and Jira created the requirements. So what what I'm going to do is start taking these requirements that I have in this document and moving them into.  
The requirement structure.  
That'll be my next steps. I wanna make sure that I'm aligning with the what Pavel and team are are putting out there as far as their patterns and linking up all the information together.

**Pavel Frolov** 26:13  
Uh, from this document I think, uh, we will be able to create more requirements that relates to these two features.

**Nathan Carver** 26:22  
Hmm.

**Pavel Frolov** 26:22  
But of of course, until the November 1st, we will need to split it into the stories and put stories. But again, keeping in mind our last conversation with Aaron.  
Should we actually create stories here under the features or to move this issues to GitHub?

**Val Levitan** 26:56  
From my understanding, we agreed to create stories in GitHub, not in JIRA.

**Pavel Frolov** 27:05  
Then you will see nothing under these features for a while.

**Val Levitan** 27:14  
OK.

**Nathan Carver** 27:25  
So that would be our payment hub project.

**Val Levitan** 27:26  
So, so you will. So I'm sorry Nathan, just just just a thought here. So beep 2656 ACH API adapter, that's the feature that will be taken into work. So you'll open a feature branch in.  
It.  
And then sitting with your developers, you will say, OK, let's just break it up into stories.  
And uh, Git will have a bunch of stories in it.  
But as far as let's say I should know, I should have a schedule for when the ACHAPI adapter will be ready, which is October 31st.

**Pavel Frolov** 28:22  
Where where can I find this date ACH API adapter? I see it.  
Finish November 12th.  
Probably need to, uh, update your portfolio.  
Welcome.

**Val Levitan** 29:04  
Oh, yes.  
A lot of changes.  
November 12th, yes.

**Pavel Frolov** 29:15  
Uh, yeah.

**Val Levitan** 29:30  
Yeah, that's, uh, that's kind of makes sense to me.  
I'm sure I'm not asking certain questions.  
At what stage do we?  
I guess engineers select detect tag.

**Pavel Frolov** 30:48  
She.  
Actually in I would say in the beginning when we understand what should be done in general.

**Val Levitan** 30:59  
So.  
So right now you're pretty well at the point where you're selecting a text stack.

**Pavel Frolov** 31:06  
I would say we already selected a text talk.

**Val Levitan** 31:09  
Is it published?

**Pavel Frolov** 31:14  
Uh, yes.  
One second.

**Val Levitan** 31:18  
My understanding when, and correct me if I'm wrong, you guys, I don't. I don't need to qualify my background, but you understand that I'm not an engineer, so I'm just trying to ask questions in order to stimulate discussions in case you guys will find.  
Oh yeah, there is a.  
We have not talked about it, let's just discuss it.  
Oh.  
So when we select a text tag.  
My understanding that there should be a justification why we're selecting a certain text stack and one of one of the points that we should never use is that we're selecting the stack text stack because we're already familiar with them.  
And I have a feeling that this is the prevalent decision making point.

**Pavel Frolov** 32:19  
Um, yeah, the uh, the man.  
The main technologies that you will use is Java and Spring Boot as core processing application.

**Val Levitan** 32:28  
OK.

**Pavel Frolov** 32:37  
And PostgreSQL as a database.  
Both of these technologies able to run under a WS, so a WS will be as hosting site.  
And uh, container platform Kubernetes.

**Val Levitan** 33:10  
So.  
How did we make the selection of tech stock? Is it because it's the best or is it because it's most familiar?

**Pavel Frolov** 33:26  
Most familiar.  
Because we are using this uh tech stack uh in different projects.

**Val Levitan** 33:42  
OK, so next thing is to finalize the architecture.  
Product architecture, am I correct? By product, we're talking about payment hub.

**Pavel Frolov** 33:59  
Architecture is as a living being. It will, it will be changed on the on the fly, but in general I think 80%, yes, you're right, I think within the next two weeks.

**Val Levitan** 34:05  
Yes, yes.

**Pavel Frolov** 34:16  
Highly likely 80% of architecture should be finalized.

**Val Levitan** 34:22  
With the next two weeks.

**Pavel Frolov** 34:24  
Yes.

**Val Levitan** 34:25  
So by October 15th.

**Pavel Frolov** 34:29  
I I'm not sure about architecture related to ACH, but I think we will try to to take a look on it.  
To spend some time with developer to review this architecture.

**Val Levitan** 34:53  
Mhm, mhm.  
OK.  
OK, seems to be.  
I don't think I have any more questions.

**Pavel Frolov** 35:31  
Yeah.

**Val Levitan** 35:33  
1.

**Juan Martinez** 35:35  
No, I I don't. And Nathan, if you have a few minutes after the call, I want to just get with you to go over the pricing so I can start putting all that down.

**Pavel Frolov** 35:45  
May I ask probably a questions that we need to cover. I think we will need to have some new additional use cases related to ACH, for example, what will be the?  
Business logic on our payment hub in case when the ACH reports in an error that some client do not have enough money on his account. Some use cases like this.

**Nathan Carver** 36:20  
OK, we can do that.

**Val Levitan** 36:28  
One, I assume that all these questions need to stimulate the discussion between you and I on what's our distribution model is and whether we will engage an operator or direct to locations.

36:36  
Yes.

**Val Levitan** 36:44  
Which I I think probably is the wrong model should probably engage an operator.

**Juan Martinez** 36:51  
Mhm.

**Val Levitan** 36:52  
And the and the pricing structure, uh.  
And and Nathan, a lot of it will depend on your verification if there if there are charges from past.  
We should kind of get this. Uh.  
Answer it as soon as possible.

**Nathan Carver** 37:14  
Um charges from on the income side or?

**Juan Martinez** 37:18  
Yeah, for using the handheld, their handheld device.

**Val Levitan** 37:18  
No, no charges from charging for using pads for using their handheld device from provider to the location and I think there are two or three providers.

**Nathan Carver** 37:22  
OK, right.

**Val Levitan** 37:36  
That are partners with income.  
So do these income business partners, the partners that provide packs to locations?  
Do they charge monthly fees or transactional fees for ACH transaction?  
They must. There's no way that they don't. It's it's kind of a no brainer to be it's.  
I absolutely don't understand how it could be free of charge.  
Do do do you understand the question that I'm asking?

**Pavel Frolov** 38:11  
Uh.

**Nathan Carver** 38:13  
Yes, yes. Are they?

**Val Levitan** 38:16  
Do do do you want me to repeat it?

**Nathan Carver** 38:19  
No, I think it it makes sense. So um.  
When they use the PAX device, are they what? What type of fee are they charging per transaction per activation on the PAX device? Or do these vendors charge their customer a ACH transaction fee?

**Pavel Frolov** 38:38  
Or both?

**Nathan Carver** 38:39  
So I think we have two, right? There's two types of transactions. There's the actual gift card activation and then the ACH reconciliation transaction, right?

**Val Levitan** 38:46  
Good.  
Yeah, I'm not talking. I'm not talking about, uh, gift card activation.  
We we already clear on get on gift card activation that's between dollar 50 and $3 depending on the card per card. So that's clear we we understand that and that is paid by by the player.

**Nathan Carver** 38:58  
Mm-hmm. OK.  
Correct.

**Val Levitan** 39:09  
So when the player wants a card, that fee goes to a player. Now there is another fee which is moving money from a location to whoever supplies packs.

**Nathan Carver** 39:25  
Correct.

**Val Levitan** 39:25  
That fee is called whatever activation ACH fee. Let's call it ACH fee for clarity and let's treat an ACH fee separate from a gift card activation fee.

**Nathan Carver** 39:30  
Right.  
Is it?

**Juan Martinez** 39:44  
And.

**Val Levitan** 39:44  
So the current question is what is the what are the competitors charging for the ACH transaction and I would assume that it would probably be a monthly fee plus a transaction fee.  
And I assume that there would be some other fees, for example, insufficient fund, you know, and and some other penalties.

**Nathan Carver** 40:14  
Correct.

**Val Levitan** 40:15  
It would be nice for us to get a copy of a contract one. If you could ask Felipe to get us a copy of the contract that they actually signed, we could get all the fees from there because I don't know if I would even trust an answer from John.

**Nathan Carver** 40:15  
Correct.

**Juan Martinez** 40:22  
Sure.

**Val Levitan** 40:31  
And John could say, yeah, there might be some fees, but I don't know what it is.

**Juan Martinez** 40:32  
Yeah, no.

**Pavel Frolov** 40:37  
OK.

**Val Levitan** 40:40  
So Juan, can you undertake the task, the task for verifying or getting a contract from a location?

**Juan Martinez** 40:43  
A absolutely.  
Yes.

**Val Levitan** 40:53  
I actually would like to have a copy of our contract.

**Juan Martinez** 40:57  
No, that makes sense, Val. And there are just a quick online, there are a bunch of potential fees, interchange fees, assessment fees, flat fee, interchange plus fee, card not present charges, PCI compliance, gateway fees, so.  
I'll post this in the chat right now, but this all relates to the PAX type of model, so.

**Val Levitan** 41:26  
And maybe POX publishes their contract, so.  
Maybe we could get in as one of the locations.

**Juan Martinez** 41:35  
Yeah.

**Val Levitan** 41:36  
And get that.  
Or maybe we could pay a location to pretend that we want to pass and go through negotiations.

**Juan Martinez** 41:46  
Yeah.

**Val Levitan** 41:50  
OK, when is our next meeting?

**Nathan Carver** 41:55  
So we are scheduled for next Wednesday.

**Val Levitan** 42:00  
OK, terrific. Please send the recording.  
Um and schedule the meeting for next Wednesday.

**Pavel Frolov** 42:10  
Perfect.

**Val Levitan** 42:10  
I understand that Nathan and father.  
Socializing in between if you, I mean you guys are doing some work when you need to, OK.

**Nathan Carver** 42:19  
Yes, yeah, we still have and we also have our standing meetings on Monday and Thursday, the three of us sync up.

**Val Levitan** 42:25  
OK. That's that's absolutely fantastic. OK. Thank you very much. Nothing else for me unless you have questions.

**Juan Martinez** 42:29  
Yeah.

**Pavel Frolov** 42:31  
OK.  
Thank you. Bye.

**Val Levitan** 42:35  
I will. I will. I booked a meeting with Irene and you for in 45 minutes.

**Juan Martinez** 42:36  
Right.

**Pavel Frolov** 42:41  
OK.

**Juan Martinez** 42:42  
All right. Thanks everybody. Nathan, I'll call you in a few minutes if you have time or you can stay on real quick. The pricing, anything that you can send me, I'll start to consolidate it even from like Taba, the one that basically kind of sort of said no, just so we.

**Val Levitan** 42:42  
Thank you. Bye bye.

**Nathan Carver** 42:47  
Alright, sounds good.  
OK.

**Juan Martinez** 43:02  
Have it all in one sheet.

**Nathan Carver** 43:04  
OK, OK. Yeah, I'll see what I have on from Tabapay, which isn't much, so I don't think they even advertise. But Stripe does advertise, so that should be easy to grab. And then hopefully I'll hear back from them soon. So, OK, sounds good.

**Juan Martinez** 43:06  
Cool.  
8.  
Sure.

**Nathan Carver** 43:21  
Thanks man.

**Nathan Carver** stopped transcription