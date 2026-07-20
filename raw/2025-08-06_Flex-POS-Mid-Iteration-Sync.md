**Transcript**

August 6, 2025, 12:01PM

**Val Levitan** started transcription

**Val Levitan**   0:04  
I trust everyone's doing well.

**Nathan Carver**   0:08  
Doing well. I'm fighting with teams trying to get it to show me video feed.  
How are you doing, Val?

**Val Levitan**   0:22  
I have so many things to do that I'm at a state of confusion.

**Nathan Carver**   0:36  
Yeah, I've been there. I think I'm there now, actually. Trying not to be confused.

**Val Levitan**   0:42  
Well, you're getting married, so no wonder you're confused.

**Nathan Carver**   0:44  
Oh yeah.  
Unfair amount of stress.

**Val Levitan**   0:50  
And deserved.

**Nathan Carver**   0:52  
But.  
She says she's excited, so that's a good thing, I'm hoping.

**Val Levitan**   1:05  
She she's preparing to enslave you.

**Nathan Carver**   1:07  
Why wouldn't she be excited?

**Val Levitan**   1:10  
Exactly.

**Juan Martinez**   1:11  
Right.

**Val Levitan**   1:13  
Natural state of human mind.  
She's she's expanding her domain.

**Pavel Frolov**   1:19  
Good morning.

**Juan Martinez**   1:21  
Thank.

**Nathan Carver**   1:22  
Morning, Pavel.  
Yeah, that might be true. That might be might be exactly what's happening. Oh, gosh.

**Val Levitan**   1:35  
Uh.

**Nathan Carver**   1:37  
All right, I think everyone's here. Should be.  
You can jump in.  
So this was as this meeting was scheduled last week for the purpose of reviewing the architecture progress specifically around data schemas.  
And I believe we were looking more at the holistic system. We did go through many of the requirements yesterday, Pavel and Juan and myself and we've so the requirements that are in GitHub now under.  
The two capabilities of or the primary one is the ticket storage capability. That's pretty well evolved. It's still in review for for Pavel and Juan, so that is drawing out data structures for the tickets.  
We also identified that because of the drive has been for Flex POS, specifically with Mother Goose, that it's going to benefit us to create separate folders for ewallet and Tito so that we can show the distinction.  
Pointed out a lot of distinctions that can be made between the data structure for the ticket and the data for I'm sorry for the Mother Goose ticket and data structures for Tito and e-wallet. So those.  
Differentiations or I'm gonna start putting those into separate folders within GitHub so we can see how those vary.  
I think that's every Juan Pavel. Anything else that?

**Val Levitan**   3:26  
Sorry, sorry, not clear. You identified the two primary capabilities. Are there more or you have not yet identified those?

**Nathan Carver**   3:37  
Let me show you what I have so far for the capabilities.  
Let me share my screen here.  
Yeah.  
OK, so this is our dashboard that's in GitHub that you could go review and.

**Val Levitan**   4:07  
You, you're not.

**Juan Martinez**   4:07  
We only see your logo.

**Nathan Carver**   4:10  
Oh gosh.  
Let me try again. Lines. Sorry, teams is not cooperating.  
Better.

**Val Levitan**   4:22  
Yep.

**Juan Martinez**   4:22  
Yep.

**Nathan Carver**   4:23  
OK, perfect.

**Val Levitan**   4:24  
Look, where is this?

**Nathan Carver**   4:26  
This isn't GitHub. I'm gonna drop. I'll drop the link in the chat, but it's in our Git.

**Val Levitan**   4:30  
Can you can you increase the size of your screen please? Can you zoom in?

**Nathan Carver**   4:33  
Yes.

**Val Levitan**   4:37  
Thank you. Perfect.  
What does Fr stand for?

**Nathan Carver**   4:44  
This is just an internal numbering system I had started with. Basically flex requirement. That's what it stands for.

**Val Levitan**   4:49  
Nice. I see.

**Nathan Carver**   4:52  
So FR1 will be a bucket of requirements for this capability and then when you come down here you'll see each one in in more detail and then you can drive to the Jira or the, I'm sorry, the GitHub.  
Requirement is here. This is considered source of truth and then here's the JIRA link. If you want to trace it into JIRA and see what we have and see the progress of this particular work item, it's the same information.  
When I create the JIRA ticket, I'll put the GitHub information in there, but updates will always be in GitHub, so that's our primary source of truth and the link will circle back from JIRA.

**Val Levitan**   5:36  
Nothing.  
Genadi, do you have access to GitHub?

**Genadi Peari**   5:40  
Yes.

**Val Levitan**   5:41  
OK.  
So this is I'm seeing GitHub and where where are the capabilities listed?

**Nathan Carver**   5:52  
Right here. So this will be at the top system capabilities.  
Here this is just the general name.  
Clicking on this will take you to the capability and the business overview and the technical overview.  
And then scrolling down, you will start to dive into the requirements that are related to this capability that enable it.

**Val Levitan**   6:16  
1\.  
Where are the requirements?

**Nathan Carver**   6:25  
Yeah.  
I'm just scrolling down, you'll see the table requirements, table of contents, and then each one that's listed.

**Val Levitan**   6:35  
What is the name of this capability?

**Nathan Carver**   6:39  
Uh, Mother Goose ticket storage and processing.

**Val Levitan**   6:45  
So.  
The description of this capability is.  
A device is capable of processing Mothergoose ticket storage.  
Is is that the right capability?

**Nathan Carver**   7:06  
Correct. It's capable of processing Mother Goose printed tickets in place of the printer. The Flex PLS replaces the manual human factor of validating and printing Mother Goose ticket with digital validation and activation of Co-am gift card.

**Val Levitan**   7:12  
Uh huh.  
Understood.

**Nathan Carver**   7:22  
Skill-based game operations.

**Val Levitan**   7:24  
Understood. Understood. OK.  
And uh, so far, is there a list of capabilities? Can you take me to a general list of capabilities?

**Nathan Carver**   7:33  
Yes, right here.

**Val Levitan**   7:36  
Got you. OK, so we have 15 capabilities.

**Nathan Carver**   7:41  
Yeah, sorry, these numbers, I'm going to renumber these, but we have currently there's nine, there's nine.

**Val Levitan**   7:45  
Oh, sorry. OK, nine. Got it. OK, OK, here.

**Nathan Carver**   7:51  
Yeah, I got to fix the number in there.

**Val Levitan**   7:54  
No problem. All right.  
And the status review and identified is something that you manually update, yeah.

**Nathan Carver**   8:06  
Correct. So the first two in review have a level of maturity where we're iterating over them and putting them in JIRA and these have been identified for they have some general information in them, but.

**Val Levitan**   8:15  
Uh huh.

**Nathan Carver**   8:22  
Just at a very high level, this is the capabilities we're gonna, we're gonna refine.

**Val Levitan**   8:29  
And how does the count of either requirements or Jira coverage increment? Is that something that you do manually?

**Nathan Carver**   8:37  
So.  
Correct. Because this is GitHub, I'm doing it manually, but Claude makes that incredibly fast to do manually so.

**Val Levitan**   8:50  
Oh, so you run a cloud function and.

**Nathan Carver**   8:54  
Correct.

**Val Levitan**   8:55  
I I see. I got it. OK, OK.

**Nathan Carver**   9:00  
So the claw that I'm using, all of that is actually also committed to the source control, so I have.  
So I'm those are all available to the team and then obviously the Claude instructions are out here. This is everything I'm using.  
So if the team also uses Claude, they'll have, it'll obviously it's going to be set up to use the same structure, so trying to manage it.

**Juan Martinez**   9:40  
Or you lost your audio, Nathan.

**Nathan Carver**   9:44  
Oh gosh, is it back?

**Juan Martinez**   9:44  
There we go.  
Yep.

**Nathan Carver**   9:50  
OK, man, I teams is really giving me a hard time.

**Val Levitan**   9:54  
Can you repeat the running Claude if somebody wants to run Claude?

**Nathan Carver**   10:00  
Oh yes, if somebody wants to run Claude, I've committed the instructions that I'm using. So I have the Claude instructions here and then I've I've added the agents that I'm using here.  
So I have these wall just to ensure that if if people are using cloud to update the documentation, it will stay relatively consistent. The patterns will stay consistent.  
Otherwise, as you know, the AI will just start hallucinating, inventing new patterns, so.

**Val Levitan**   10:40  
Has anybody tried to use cloth aside from you?

**Nathan Carver**   10:44  
Uh, I don't know. I um.

**Pavel Frolov**   10:47  
Actually I I just saw yesterday that it was a new can needs to clawed directory GitHub actually do not actually understand how how it can be used. Probably I need Nathan to.  
Explain.  
Just this this this particular files with MD and the agents folder how it can be used.

**Nathan Carver**   11:09  
Yeah, I can do that.  
Oh, OK. I can show that real quick or we can do that offline either way.

**Val Levitan**   11:26  
Show it real quick. I can benefit from it as well.

**Nathan Carver**   11:32  
Um, so let's see here.  
And OK, so if I have.  
So what I'm doing here if I said to Claude you.  
So I'm asking Claude to just do a review and then there's a a language agent in there.  
That Claude will delegate to.  
1st it's going to find the file.  
And then it should delegate to that language agent. And when the agent's being used, you'll see like a little. OK, it didn't actually. Sometimes Claude does what it wants to do.  
Let's make sure that it's.  
Let's see. Let's try again.  
Review.

**Juan Martinez**   13:08  
And Nathan, this is a local instance of Claude running on your computer.

**Nathan Carver**   13:13  
So it's cloud code that runs locally, but it uses the cloud service to actually do the work.

**Pavel Frolov**   13:22  
Actually, none. None of us using the cloud CLI. We're using VS code.  
Visibility to.

**Val Levitan**   13:33  
No, I'm no, no, I'm using Claude. I'm using Claude. I'm using Claude code.

**Nathan Carver**   13:40  
Yeah, so here I found. So it'll list for me inconsistencies and.  
Oh, I see what it's doing.  
So the idea behind the agents, and I'm trying to get it to fire that agent up, but it's it's not cooperating.

**Pavel Frolov**   13:54  
Oh.

**Nathan Carver**   14:06  
Oh, there's something wrong with the document.  
I had very good use of this last night. So what happens is Claude has a context like the main chat context here and then when it switches to an agent it will delegate to a new sub instance of Claude.  
And the context for that becomes exactly what's in this agent document. So it's a way to distribute AI context across multiple instances, and that keeps the context of the agent very focused.  
Because the more context, a context file is just a prompt, so the more you give it every time you ask it a question, the more tokens it uses up. So this is a way to distribute that load across multiple multiple context.

**Val Levitan**   15:34  
OK, I don't want this meeting to be about Claude. So, you know, it's becoming more complex than I thought. Let's revert back to the agenda of the meeting.

**Nathan Carver**   15:36  
That's it.

**Pavel Frolov**   15:37  
Mm.  
So.

**Nathan Carver**   15:45  
OK, sounds good.

**Val Levitan**   15:49  
OK, so let me just summarize my understanding. We now have initial list of capabilities and we are building a set of requirements, tying up various requirements.  
To a capability or to a set of capabilities.  
And um.  
We're doing it through discussing the overall schematics of the architecture and and applying certain use cases to it.

**Nathan Carver**   16:31  
Correct.  
Correct. And I will be.

**Val Levitan**   16:36  
And and and we're doing it for which product or for the for POS right now, right?

**Nathan Carver**   16:43  
Yeah, my primary focus has been flex POS and we'll start to branch out.

**Val Levitan**   16:48  
So this is the set of capabilities set of use cases specifically focus on on the POS.

**Nathan Carver**   16:58  
Correct.  
Yeah, and I think that'll be a good update the heading to show that.

**Pavel Frolov**   17:12  
And actually list of capabilities for POS based on Mutagus architecture schema will be a little bit different from the POS for Tita operation.  
For Tito E wallet.

**Nathan Carver**   17:35  
Correct.

**Pavel Frolov**   17:36  
So currently we are, uh, we are reviewing uh, Moto goose schema.

**Val Levitan**   17:44  
OK. Thank you, Pavel.  
OK.

**Nathan Carver**   17:56  
So from this dashboard we will have there's the use cases, the architecture and design, and then just kind of a bucket for everything else, development tools and guidelines.  
So go ahead.

**Val Levitan**   18:12  
So sorry, sorry for interruption. So when I look at the set of capabilities for POS, the first capability is Mudagus ticket storage and processing and Pavel said that this is unique for Mudagus processing.

**Nathan Carver**   18:19  
Mhm.

**Val Levitan**   18:32  
So when I look at the overall.  
Capability, full capability of POS. Will it have similar capability instead of Muda Goose ticket storage and processing? Will it have Tito ticket storage and processing?

**Nathan Carver**   18:52  
Correct.

**Val Levitan**   18:53  
But uh, you did not list this capability yet, did you?

**Nathan Carver**   18:59  
Correct. That was our discussion yesterday morning was the need to separate those out and make them and create the independent capabilities so they're clear on what the intent is.

**Val Levitan**   19:15  
So the second capability Tito.  
Storage and processing. Will it have Tito and e-wallet storage and processing or will you have a separate line Tito storage and processing and e-wallet storage and processing as two separate capabilities?

**Nathan Carver**   19:39  
They could be, I think it could go under one digital digital tickets, right? This is a a physical Mother Goose ticket and then the next capability is going to be digital tickets and e-wallet and Tito could fall under that.  
Unless unless Tito is physical then I think whatever makes sense. But I think to answer your question Val is it could be one capability for both or two more capabilities depending on the business function and.

**Juan Martinez**   19:59  
Yeah, we.

**Pavel Frolov**   19:59  
It should it.

**Nathan Carver**   20:15  
Go ahead, Pavel.

**Val Levitan**   20:16  
My.  
Same, same.

**Pavel Frolov**   20:22  
Tickets will be a little bit different. One will have a value of the ticket and the second one will not have this value. At least we need to to differentiate different type of tickets.

**Val Levitan**   20:22  
Time.

**Nathan Carver**   20:33  
OK.

**Pavel Frolov**   20:37  
With.

**Val Levitan**   20:37  
And from my perspective, I would like to have a a way of coming out with, I don't know how to call it a to do list or a different differences list of differences.  
Between various settings, let's say we want to set up a location or convert a location from Muda Goose ticket storage to an e-wallet ticket storage.  
Um.

**Nathan Carver**   21:11  
OK, understood.

**Val Levitan**   21:13  
So I'd like to be able to generate A todo list or a.

**Pavel Frolov**   21:18  
Differences.

**Val Levitan**   21:21  
Yeah.

**Nathan Carver**   21:22  
OK.  
Understood.  
Is this dashboard communicating clearly? Is there any changes we can make I think as we add?

**Val Levitan**   21:39  
I don't know. I really like the dashboard, my personal opinion. I don't know about everybody else's opinion, but to me, to me it's quite clear.

**Nathan Carver**   21:46  
OK.

**Juan Martinez**   21:46  
It's clear.  
Great.

**Val Levitan**   21:54  
So take me, take me to JIRA. When you say JIRA coverage, what exactly does it mean? JIRA coverage?

**Nathan Carver**   22:04  
Um, so it means this right here. So we have.  
4 requirements in this bucket. Three of them are in JIRA.  
And so if you were to come down to the more detailed description, you'll see each requirement and their associated JIRA ticket. So it's just a very high level view to say how many requirements are here and how many we've put into JIRA. If there's a discrepancy, it may be because.  
This requirement is still in progress. It's being refined. In this case, this requirement has been identified as potentially too too much of an engineering or I should say non-functional requirement.  
And so just reviewing this to make it more business, the requirement more higher level business focus.

**Pavel Frolov**   22:56  
Mhm.

**Nathan Carver**   23:00  
But that's what the that's what the two numbers mean. So in this case we have 6 requirements and six JIRA tickets assigned.

**Val Levitan**   23:14  
OK, I am what I'm. I'm kind of maybe running a little bit ahead of you guys, but.  
What is our average velocity of processing?  
These requirements or moving through understanding the capability, the architectural.  
I'm going to say the architectural belonging and then structuring your requirement.  
How? How quickly or slowly are we pacing through it?

**Nathan Carver**   23:47  
Um.  
I don't have a velocity number. We could determine that, but I know we're moving. We're gaining momentum as we go. We had, what was it, two tickets or three tickets in JIRA last week?  
And we now have 9 tickets. So it will, I think it will ebb and flow a little bit as I get out ahead into the the next group of the next capability, what's next and what I can.  
Flow into next and start cranking out those requirements.  
But we can certainly do that. We can start measuring, get a a throughput count of how many requirements are refined in a week. We can get a sense.

**Val Levitan**   24:36  
Yeah.  
No, no, no. I'm only trying to get a sense of when will we be done with.

**Nathan Carver**   24:48  
Right.

**Val Levitan**   24:48  
Keep describing capabilities with most of the requirements for POS. The reason I'm asking is because in the other in the previous meeting we were trying to figure out how to.  
Start physically working on POS and I I really hate to start any work on POS without pretty pretty clear understanding of the capabilities.

**Nathan Carver**   25:17  
OK, understood.

**Val Levitan**   25:25  
And answers the question. I mean how far?  
How far away are we from thorough understanding of capabilities? Is this a final list? Well, the answer is no, but how is to final?

**Nathan Carver**   25:36  
So I think the.  
I think this general list of capabilities is very pretty well understood and if we come into our use case down here.  
We have a well defined use case that takes us through the happy path of entire game, cash out, printed ticket, intercepted player goes through and redeems a gift card.  
So as we're stepping through this, we are associating the capability requirements to each step. Some steps are just this is player and.  
You know, player and cashier communicating.  
So that's that's what I'm doing. So starting at step one, I've mapped out every the capability requirements necessary to complete step one.  
Step 2 is really a a a player cashier communication. So the next one I want to go into is cashier authentication which.  
We actually have, so I need to map those U.  
So I will identify. So we actually have these these requirements written, so I'm going to link them here.  
Oh, right here. OK, and then.  
So and that's what I'm doing. So if you go into each of these requirements in the use case, you can see what's been linked up and as we step through this flow is is pointing out which requirements I'm going to write next.  
And this helps just keep a keeps a good flow and so this is the progress we're making to get through this this use case. So we have a pretty good understanding of all the capabilities needed to complete.  
This use case so the next one Pavel has given me a use case on on the devices and Pavel I forgot the name but.  
Example is another use case that Pavel has. So I'm going to put that in there and we'll do the same thing here. We'll go through and identify all the requirements and the capability that this is associated with. So the more as we step through these use cases is how we'll generate that.  
Um.

**Val Levitan**   28:04  
I would suggest adding a service technician as a persona and the master operator as a persona as soon as soon as possible, actually even ahead of.

**Nathan Carver**   28:15  
OK, yes.

**Val Levitan**   28:22  
A regular customer because we already have pretty good grip on the customer. I just don't want to miss anything on the master operator and the technician.

**Nathan Carver**   28:35  
OK, I'll add those in.  
So that's the that's the approach I'm taking to fleshing out requirements is creating a.

**Val Levitan**   28:48  
I I I really like it. I I think it's very disciplined and this is probably the closest we came to a perfection so far.

**Nathan Carver**   29:00  
OK, good. All right. That's great to hear. I appreciate that.  
OK, so.  
Uh, let's go back.

**Val Levitan**   29:15  
Juan, I assume that you have full access to git, right?

**Juan Martinez**   29:20  
Yes, I do.

**Val Levitan**   29:21  
Yeah, OK.

**Nathan Carver**   29:33  
And OK, any other, any other details we want to dive into?

**Val Levitan**   29:41  
No, I'm pretty satisfied with where it's going. I think I should leave you alone and to have you continue with the Juan and with Pavel.

**Pavel Frolov**   29:46  
But.

**Nathan Carver**   29:52  
OK.

**Val Levitan**   29:53  
And the sooner with less interruption, the sooner you get to a set of full capabilities, the sooner we could have our meeting with Genadi and say, look, Genadi, this is what you need to support.

**Nathan Carver**   30:08  
OK, understood.

**Val Levitan**   30:11  
Genadi, do you have any questions on this?

**Genadi Peari**   30:16  
No, it's a great job. Really, really nice. Really nice.

**Val Levitan**   30:20  
Yeah, yeah, me too. I agree. I.

**Genadi Peari**   30:26  
If I added some page on the confluence, if you want to, we can move it to GitHub as well. It's here.

**Val Levitan**   30:37  
My overwhelming preference is to need everything in GitHub.

**Genadi Peari**   30:45  
And there is some also page for the hardware requirements. We also probably will do it here.

**Nathan Carver**   30:51  
Yes, perfect. OK.

**Genadi Peari**   31:00  
Well, there is a.

**Juan Martinez**   31:03  
Genadi, though, you'll continue to post these into Confluence and then we will move them over into GitHub. Or are you able to directly switch the?

**Genadi Peari**   31:12  
I can.  
OK.  
I think the GitHub should go the final version, not all the interactions we do.

**Val Levitan**   31:23  
On the on the on the country, Genadi, the the best place for iterations is GitHub because it it naturally built for iterations. It keeps version controls.

**Genadi Peari**   31:33  
OK.  
OK.

**Val Levitan**   31:36  
This is really a beautiful place to go through versioning and idea development and evolution. GitHub is really a.  
Version Evolution Control software.

**Genadi Peari**   31:51  
Yeah.

**Val Levitan**   31:56  
No more questions from me. I think that we achieved the purpose of this meeting. The review as far as I'm concerned is complete. I would like to have you.

**Nathan Carver**   31:59  
OK.

**Val Levitan**   32:08  
Function as you were in the last couple of days with more emphasis on tighter meetings and development of capabilities for the POS.

**Nathan Carver**   32:21  
OK, understood.

**Val Levitan**   32:23  
So with that in mind, what are your? What is your schedule now?

**Juan Martinez**   32:29  
Mm.

**Val Levitan**   32:29  
Let's review them quickly. Can you share the calendar?

**Nathan Carver**   32:29  
Oh.  
My next.  
I'm sorry, what was the question?

**Val Levitan**   32:36  
I'd like to review the schedule between you, Nathan, Juan and Pavel as a working working forum.

**Nathan Carver**   32:46  
OK, so our next.  
Our next session is scheduled for Friday, so we'll continue the Monday, Wednesday, Friday cadence if we think we can tighten that up and we can go shorter meetings daily if we feel that's more beneficial.  
What I'm going to continue doing is refining use cases and I'm as I put them in JIRA, I'm notifying Juan and Pavel that they're there and ready for review. They have time to review those and then in one of our in our next cadence meeting we go through them together.  
And then ask it.

**Val Levitan**   33:25  
So I said, Nathan, Nathan, right now you have three meetings a week scheduled where Genadi and I are participating. We don't. I don't want to be in these meetings. I want to.  
Leave you leave that time for your working schedule, your working meetings. I would like to review with the team on a weekly basis.

**Nathan Carver**   33:52  
OK. I will restructure those Friday review is, is that OK with you?

**Val Levitan**   33:52  
So.  
I prefer Wednesday reviews instead of Friday. Friday tends to be a very busy day.

**Nathan Carver**   34:03  
OK.

**Val Levitan**   34:03  
But Wednesday is a is a good review time for me, so schedule me for Wednesdays. Genadi, do you want to be in working meetings or do you want to be only in review meetings?

**Nathan Carver**   34:04  
That's that works.

**Genadi Peari**   34:18  
It it doesn't look beneficial to be here on the working instance.

**Val Levitan**   34:25  
OK, so working meetings where you.

**Genadi Peari**   34:26  
Unless you guys need me.

**Val Levitan**   34:28  
I don't believe so. I agree with you. So schedule Genadi and myself for Wednesday's.

**Nathan Carver**   34:37  
OK.

**Val Levitan**   34:37  
And I prefer for you to have daily meetings with Juan and Pavel, maybe shorter daily meetings.

**Nathan Carver**   34:44  
Yes, OK, I'll create that cadence.  
We'll do 15 minute or half hour dailies and then we'll have a one hour block on Wednesday.

**Val Levitan**   34:50  
OK.

**Nathan Carver**   34:57  
For a full review.

**Val Levitan**   35:01  
OK, terrific. Thank you very much. With that, I think that we achieved the objective for today.

**Pavel Frolov**   35:02  
Thank you.  
OK, bye.

**Nathan Carver**   35:08  
All right.

**Genadi Peari**   35:08  
Thank you.

**Val Levitan**   35:09  
Bye.

**Pavel Frolov**   35:10  
Thank you.

**Nathan Carver**   35:11  
Thank you everyone.

**Val Levitan** stopped transcription