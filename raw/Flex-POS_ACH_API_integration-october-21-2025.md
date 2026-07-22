**Flex Capabilities Weekly Update-20251022_080343-Meeting Recording**

October 22, 2025, 12:03PM

31m 13s

**Val Levitan** started transcription

0:05  
OK.  
OK.

**Nathan Carver** 0:09  
All right, so to get started, I have the two modules very well defined for the payment hub. This would be the ACH adapter module and the reconciliation module, the adapter being the component that we built that's.  
Essentially swappable for different providers. Should we change providers or have more than one at any point in time? And then the module is or the reconciliation module is the the business rules around doing transfers for all the locations.  
Do do doing daily transfer jobs. So we have there's 23 requirements in total and I have one last refinement. I'm passing over all of them just to make sure there's consistency.  
And then I can start putting them into JIRA.  
And um, I plan to start that this week is my goal.  
Um.  
So that's what I've been focused on. It's very much using Dwala's API as the primary for developing the module that means.  
How Duala does reference IDs, callback hooks for ACE when transactions complete and also the different types of transactions that Duala has.  
So that's where my focus has been. I know we have the Fed now conversation today that was moved to 3:30. Is that still going on today at 3:30? OK.  
So I have a flight at 4:00, so the 3:30 now is a little tight for me, but I'm gonna call in and at least be able to catch the first half.

**Val Levitan** 2:03  
You look.

**Nathan Carver** 2:04  
But eventually I'll have to board the plane.

**Val Levitan** 2:06  
You you don't have to.

**Nathan Carver** 2:09  
OK.

**Val Levitan** 2:10  
So if you skip it, it's OK, don't worry about it.

**Pavel Frolov** 2:14  
OK.

**Nathan Carver** 2:14  
OK, so the document I sent out Valdez, I can share the link again, but this was a doc just used for driving the conversational needs that we would need from an API.

**Pavel Frolov** 2:16  
OK.

**Nathan Carver** 2:29  
Um, I'm going to share that again.

**Val Levitan** 2:35  
Did you manage to find out anything about Fed now?

**Nathan Carver** 2:38  
Um. So I think what we what we knew is um.  
You have to be the financial institution to use it. So we can't directly use Fed now. We have to go through a financial institution and then we have or we have to be ourselves designated as a financial institution.  
Dualla supports it, so we can go through Dualla, but we still have the the costs right of Dualla being the the the middleman, but they do provide that as an option. I'm gonna drop a chart.  
Cody just sent me an update.  
And I think.

**Val Levitan** 3:23  
Well, we have not, we we have not negotiated with Duala. We just got their original off the shelf quote, but we did not negotiate with them. Maybe if we start negotiating and switch to Fed now program.

**Nathan Carver** 3:31  
Right.

**Val Levitan** 3:41  
Under Dwala API, maybe it will be different charges.

**Nathan Carver** 3:47  
Yes. So they, according to what Cody said, yeah, they have a flat 75% or 7075 cent cost per transaction for FedNow and RTP, which are their two immediate.  
Quote UN quote immediate style payments.

**Val Levitan** 4:08  
But what do they?

**Nathan Carver** 4:08  
So on top of the Duala cost, yeah, it would be $0.75 to use them if we don't negotiate, negotiate that down.

**Val Levitan** 4:18  
$0.75 for a transaction meaning what is the transaction meaning the once a day transaction per location. So it could be it could be let's say 20 different.

**Nathan Carver** 4:28  
Correct, correct.

**Val Levitan** 4:34  
Transactions grouped together once a day. That's $0.75, right?

**Nathan Carver** 4:42  
Yeah. So in our pilot we had 10, if we had 10 locations and we we reconcile each all 10, it's yeah, $0.75 per per transaction.  
Yeah, so at 10 locations it would be this $7.50 a day to reconcile all 10.

**Val Levitan** 5:09  
OK, so as it stands right now.  
Dwala is a.  
Realistic and reasonable.  
Venue for us to clear ACH transactions. They have various levels of service.  
Including the service offered by FedNow and we are at the point that we are implementing and the engineering team is moving forward on implementing their protocol.  
And we should start negotiating with them.  
On the fees unless.  
Today's meeting with Wells Fargo yields a result.  
And we could use Fed now under Wells Fargo license.  
Uh, to interface direct with Uh.  
Uh, with the capability of ACH.

**Juan Martinez** 6:26  
I said just to confirm, maybe I missed this from the last meeting. I I was not able to join, but Diwala, how did we make the 2500 + 2500 a month fee, the $5000 go away? We we didn't mention that just now.  
Plus the one time $1500 setup fee.

**Val Levitan** 6:45  
With.  
We we we didn't make it go away.

**Juan Martinez** 6:50  
OK, OK. OK.

**Val Levitan** 6:52  
We we're simply saying we did not negotiate anything. This is an off the shelf.  
An off the shelf quote.  
I do not want to negotiate with Diwala until I am.  
I exhausted the opportunity with Wells Fargo because the most ideal situation for us is to use Wells Fargo with Fed now.

**Nathan Carver** 7:31  
Makes sense.

**Val Levitan** 7:31  
That would that would be the most effective core solution for us.  
You agree one?

**Juan Martinez** 7:42  
Oh, absolutely, definitely.

**Val Levitan** 7:47  
OK.  
Moving on.

**Nathan Carver** 7:51  
Um, yeah. So as far as the requirements go, that's it on my side. Um.

**Val Levitan** 7:57  
So where where are the requirements? Can you send me the link please?

**Nathan Carver** 8:00  
Yes.  
Yep, I'll send you that.

**Val Levitan** 8:04  
Pavel, do you have any questions? Have you had a chance to look at the requirements or you kind of stayed in the background?

**Pavel Frolov** 8:14  
Not the last changes, but previously yeah, I saw requirements and we agreed not to fulfill each small requirement that.  
Nathan posted but keeps them quite big and each requirement can contain a small bullet bullet points related to this requirement. Big requirements.  
Otherwise, we will spend lots of effort to support all the smaller requirements.

**Val Levitan** 8:55  
So my assumption is that we really don't wanna schedule any development yet until we speak to Wells Fargo.

**Pavel Frolov** 9:00  
Help you.  
Uh, related to ACH, yes.

**Val Levitan** 9:08  
OK.

**Pavel Frolov** 9:11  
Actually, I think we need to report to Val that we spoken last time with Nathan and Juan that in calm.

**Val Levitan** 9:12  
Mhm.

**Pavel Frolov** 9:26  
Performance their ACH.  
Not every day, but every working day in the 9:30 as I remember, yeah.

**Nathan Carver** 9:40  
Correct.

**Val Levitan** 9:40  
Yes, but I but I spoke to income privately.

**Pavel Frolov** 9:41  
Zip.

**Val Levitan** 9:46  
And I said we would like to negotiate a deal by which they.  
Transfer money out of our account every second day, every second working day.

**Nathan Carver** 10:05  
OK.

**Pavel Frolov** 10:06  
I think.

**Val Levitan** 10:07  
We, we, we, we want 48 hours in between the time that we get the money and.  
Sorry, we want 24 hours between the time we get our money and the time our account is swiped by income. We want 24 hour gap and we want to allow ourselves 24 hours to swipe all of the accounts to bring money in.  
To do full reconciliation and to see which account is deficient. We we actually want to see which account is deficient in real time and to shut it off.

**Pavel Frolov** 10:45  
That's good, good, good news because previously we thought that we have only 30 minutes to perform all the work between clients and ACH.

**Nathan Carver** 10:45  
That makes sense.

**Val Levitan** 10:58  
We, I mean we do now as as it stands right now. I'm just hoping to create you know like you get in the crowd and you start pushing your out. So I'm I'm hoping that we could get into negotiation and.

**Pavel Frolov** 11:02  
Mhm.

**Juan Martinez** 11:10  
Sure.

**Pavel Frolov** 11:12  
OK.

**Val Levitan** 11:16  
Create some elbow room. It's called elbow room.

**Nathan Carver** 11:19  
So, so income is open to that or we don't know yet.

**Val Levitan** 11:24  
They open to that. They well, they they didn't say. They didn't say absolutely not. Have you have you seen the movie Dumb and Dumber?

**Nathan Carver** 11:26  
OK.  
OK.  
Yeah, yeah.

**Val Levitan** 11:34  
What are my chance? What are my chances of marrying you? So she looks at him and says one in a million. So he says, oh, so I have a chance.

**Nathan Carver** 11:38  
Yeah.

**Juan Martinez** 11:42  
Yeah.

**Nathan Carver** 11:42  
Exactly.

**Val Levitan** 11:45  
So that's the other. That's the attitude I'm taking.

**Nathan Carver** 11:45  
OK.  
OK, we have a chance.

**Juan Martinez** 11:49  
Yeah.

**Val Levitan** 11:50  
What? What are the chances of us getting 48 hours? He says. One in a million. So I said, oh, so I have a chance.

**Juan Martinez** 11:56  
Yeah.

**Nathan Carver** 12:00  
Perfect.

**Val Levitan** 12:01  
Yeah.  
He.

**Nathan Carver** 12:04  
OK, yeah, I dropped the links in the chat here for the two modules. Val, if you.

**Val Levitan** 12:09  
I I just sorry, sorry, one more question because it's not really clear to me and thank you for dropping the lens. Nathan, one more question. So is Duala API materially different from FedNow API?

**Nathan Carver** 12:14  
H.  
Hmm.  
That I don't know. I haven't seen the Fednow API. I'm assuming that their API is is going to be as far as the the contract it's gonna take.  
Pretty similar parameters than that Fednow would need 'cause they're just gonna redirect all of the JBL parameters to Fednow and then probably tack on their own vendor ID.  
Parameters to that API. So if Wells Fargo has something, I can't imagine it's too different than what what Duala would have as an API.  
And the requirements are written in a way. So if we did have to to design some new requirements around the Wells Fargo, it should be pretty isolated to a small subsection of the adapter.

**Val Levitan** 13:26  
Juan, are you planning to be in the meeting?

**Juan Martinez** 13:29  
Oh, absolutely, yeah.

**Val Levitan** 13:31  
OK, I I need to take the meeting from from my car. I'm going to be on the road. So we want to be. I'm going to 0 the conversation on Fed now because I really want to hit, hit.  
The bullseye with the with this conversation, I don't want to start dancing around.  
About any other matters, I just want to tell them that we need them for Fed now. You know, if you can't provide it, go take a hike.  
Uh, they may never heard of Fed now.  
So I would want you to just send them a link.  
If that will be required, OK.

**Pavel Frolov** 14:17  
OK.

**Val Levitan** 14:22  
So again, just to regurgitate, we're not planning any technical work until we have our meeting today with Wells Fargo. How could this meeting go, let's say?  
They need couple of weeks to get back to us or something needs to get pronounced with a little more clarity, but we should be ready to start development.  
One way or the other within next 2-3 weeks.  
What do we need to start development within 2-3 weeks?

**Nathan Carver** 15:07  
So the requirements are there, the design is there. Um.

**Val Levitan** 15:07  
I know.

**Nathan Carver** 15:13  
I think the next after the Wells Fargo conversation, if the Duwalla negotiations move forward, we need to coordinate with Duwalla on engineering setup and integrating with them.  
Because they will designate a team to support us and they have a a window of about 30 days to get their side up and running. So that's something that we'll need to make sure we schedule with our with our teams.  
Uh, that doesn't block the team from designing for their API. It really just it would be a blocker for any final integration. Um.  
And we actually have a sandbox account that we can probably start using as initial testing with our with our code.

**Val Levitan** 16:10  
Right. Sorry, they need 30 days from the moment we we assign to the moment they allocate their engineering team.

**Nathan Carver** 16:20  
No, they can allocate a team I think fairly quickly. They are asking for once we have, once they've designated a team that that team has 30 days to get all the systems set up for us. So we'll need that team in place to start that.  
That 30 day cycle.

**Val Levitan** 16:41  
OK. But we're looking at a rollout location rollout, hypothetically speaking, January 1st. Of course, I understand it's not January 1st. It will be pushed towards the middle of January. Am I, am I correct? Am I, do I understand our timing correctly?

**Nathan Carver** 16:52  
Correct.  
Yes, I believe that that is what we've been focused on as well, 1st of January.

**Val Levitan** 17:03  
But but that's the location rollout. What about beta test? How? How do we do beta test?

**Pavel Frolov** 17:11  
So.

**Nathan Carver** 17:12  
So testing with Diwala, they will set up an environment for us to do that and we will want to have that in December. We should get the ball rolling with them 1st of November.

**Val Levitan** 17:25  
OK, so let's assume that we want to have beta test 1st of December. By the way, just for everybody to be clear, we are closed as of 22nd of December I believe until the.  
5th of January.  
Everywhere. So Pavel, how much time do we need? If we say go, how much time do we need to develop an API or two? Sorry to integrate integrate API so we can do beta test.

**Nathan Carver** 17:45  
OK.

**Pavel Frolov** 18:00  
Implement.

**Val Levitan** 18:05  
Thing in our shop.

**Pavel Frolov** 18:08  
Actually, I think it'll take about one month probably, keeping in mind that we already have some preparation before that, so starting in December I think.  
Highly likely we can finish until end of of the year.  
What?

**Val Levitan** 18:31  
So that means we have to start 15th of November.

**Pavel Frolov** 18:34  
Probably, but please keep in mind that we have different tasks that need to be done by the same persons.

**Val Levitan** 18:50  
OK.

**Pavel Frolov** 18:51  
In the company, actually probably let me share my screen. I will show the some schedule that covers different projects second.  
So here.  
We have, uh, Flex POS.  
And payment hub.  
So here both of this project have the dependencies from each other. So right now we have a basic implementation of payment hub and.  
Demand uh, search switch it to implementing uh back end application for Flex POS.  
To add devices to Flex POS some logic.

**Val Levitan** 20:09  
Well, I see that they're busy until November 15th, more or less, so you could start.

**Pavel Frolov** 20:15  
Oh yeah, in parallel here you can see for payment hub.  
ACHA adapter that starts in in the beginning of November, I I assume or probably it should be moved.  
Uh.  
And reconciliation module also. So actually I think it will be moved to to December reality.  
This one related to ACH.  
Uh, and.  
Here you can see some.  
Some tasks that can be, I think, implemented next year, probably some reporting authentication by magnetic card for example. It's not MVP.  
Receipt print printing a receipt on roll printer. Also I think it's not MVP until end of this year.  
So actually it looks like until December we should mostly finish Flex POS software.  
And in December.

**Val Levitan** 21:43  
Well, the date, sorry, the date, I mean all the tasks that you are showing us are positive dates. So this is not really a proper schedule.

**Pavel Frolov** 21:52  
Mhm.

**Val Levitan** 22:01  
And none of it is in the progress, still in to do stage.

**Pavel Frolov** 22:02  
The.  
Yes, yes, because they planned for the for November. Right now is only end of October.

**Val Levitan** 22:13  
Oh, sorry, I'm looking at a different. Oh, sorry, I was looking. I thought it was a timeline. Got it.

**Pavel Frolov** 22:19  
OK.

**Val Levitan** 22:21  
OK, I understand.  
But you're basically confirming that we can start November 15th and finish by December 15th, you know, take or give a week.

**Pavel Frolov** 22:35  
Yes, yes. I anticipate probably this schedule that partly we are starting in November, in the middle of November implementing some adapters.  
For ECH and actual reconciliation module, it's related to logic and integration with actual provider.

**Val Levitan** 23:05  
I am inclined to go with.  
Now without waiting for Wells Fargo.  
And I'm still hoping that Wells Fargo will give us a positive reply. I just think that in in realistically, even if Wells Fargo jumps on board, there will be a bunch of bureaucratic.  
Barriers that we're going to have to jump through before we even open an account or sign all the papers and start getting anywhere. I don't see it happening.  
At best before March.  
So I think we should use a use Duala for now and look at it at some cost.  
Or cost of entry in the market.

**Pavel Frolov** 24:23  
OK.

**Val Levitan** 24:29  
OK, so if this is the case and we're focusing on Duwalla, what's our next?  
Objective without.  
We should probably start negotiating the price.

**Juan Martinez** 24:41  
That.

**Nathan Carver** 24:45  
Negotiating the price and ensuring that we get our the technical setup started.

**Val Levitan** 24:51  
OK. So as a separate loop, can you introduce me to the right people so I can start negotiating with them?

**Nathan Carver** 25:00  
Yeah, yes.  
I will introduce. I will, yeah, introduce you to Cody, who has been our primary contact.

**Val Levitan** 25:14  
OK.

**Juan Martinez** 25:15  
And Nathan, does it make sense to partly convert these weekly calls now into something focused on the sandbox and actually interacting with their API or at least for an update purposes?

**Nathan Carver** 25:16  
Now I will do that.  
Yes, I think we would want to, we would definitely want to focus roll that in their their setup, getting their sandbox set up and making sure that all the issues are resolved there for the team.

**Juan Martinez** 25:45  
Sure.

**Nathan Carver** 25:46  
OK, perfect.

**Val Levitan** 25:47  
And if this is and if this is the road you're taking, I mean if this is the road we're taking Nathan and Pavel, should we now start detailed planning for API integration actually connecting the requirements to features and?  
You know, breaking it down because right now just one like 2 big blurbs, API integration and reconciliation report.  
But you said you have a how many requirements I forgot.

**Nathan Carver** 26:22  
Correct. Let me let me grab them. So the the adapter itself has eight requirement groups with with details in each of those groups and then.

**Val Levitan** 26:35  
And by group, by group, what do you mean by group?

**Pavel Frolov** 26:39  
Yes.

**Nathan Carver** 26:41  
So this is what Pavel alluded to is we've grouped them into high level requirements and then each of those has a a list of more granular requirements and what Pavel's gonna do is go through and.  
Those more granular pieces in each one of the eight and go through and decide what needs to be implemented now, what can be deferred and what may not be needed. So total granular requirements for the ACH adapter is 93 individual line items.  
And then the reconciliation module has 15 groups with 160 um.  
So the reconciliation module is the primary core for JVL. So the much smaller piece of this is around Duala. That would just be the eight groups that deal with the ACH adapter. So that's what we.  
Would focus on for our integration with Duala.

**Val Levitan** 27:42  
So superficially, without looking at all the details and not be an engineer, I kind of imagine that a group could loosely be defined as a feature.

**Nathan Carver** 27:56  
Correct. So to give you an idea as a group is called transfer initiation.

**Val Levitan** 27:56  
And so I I am lucid.  
Right. So I loosely think of it as a feature. So that means respect respectively we have 8 and 15 features per.

**Nathan Carver** 28:15  
Correct.

**Val Levitan** 28:16  
Product called the product.

**Nathan Carver** 28:20  
Correct. Yep. So they're referred to as module and the requirements that would be right, the product and each module has the the list of features. So the ACH adapter module has the 8 features with detailed requirements under those features.

**Val Levitan** 28:23  
OK.  
OK, so if we go back to our planning module, we probably will see.  
And it's under application I understand.  
Is a transactional solution.

**Pavel Frolov** 28:53  
Yes.

**Val Levitan** 28:53  
So under POS.  
We need to uh.

**Pavel Frolov** 29:02  
And the payment hub.

**Val Levitan** 29:02  
OK.

**Pavel Frolov** 29:08  
So instead of ACH adapter, you suggest to split it into smaller parts based on groups in and reconciliation module 2.

**Val Levitan** 29:15  
Welcome.  
8 features.  
So.  
So ACH API will be split into 8 features and reconciliation module will be split in approximately 15 features and.

**Pavel Frolov** 29:28  
Mhm.  
OK, let me focus. Let me focus on that next meeting. I think I will.

**Val Levitan** 29:36  
Yeah.

**Pavel Frolov** 29:42  
Answer What will be the best? Probably some of these groups can be joined or some of them splitted because I don't see so much features here.

**Val Levitan** 29:58  
I I was approximating. I was simply setting a tone for the next meeting. So. So the undertaking for the next meeting is to split the BEP 2656 and BEP.

**Pavel Frolov** 30:00  
Mm-hmm.  
Yep.

**Val Levitan** 30:16  
2657 into features and have them laid out in the form of a schedule.  
And allocated or assigned to an individual and properly planned. So hopefully as of November 15th we could include it in our sprints.

**Pavel Frolov** 30:41  
Yep.

**Val Levitan** 30:41  
With a with a tentative delivery on or about middle of December.  
OK, that's it for me then.

**Pavel Frolov** 30:57  
OK.  
Mhm.

31:02  
All right.

**Nathan Carver** 31:04  
Um, sounds good. That's it for me.

**Val Levitan** 31:05  
Thank you.

**Juan Martinez** 31:07  
All right. Thanks, everybody. Thank you. Bye, bye.

**Pavel Frolov** 31:08  
OK. Thank you. Bye.

**Val Levitan** 31:08  
Thank you very much. Bye, bye.

**Nathan Carver** 31:09  
All right. Thanks all.

**Val Levitan** stopped transcription