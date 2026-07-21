**Transcript**

15 September 2025, 06:06pm

**Val Levitan** started transcription

**Val Levitan** 0:03  
Pavel, thank you for joining us at the at this hour. I appreciate it and this is the only time I had and OK, so Nathan, welcome back from your time off.

**Pavel Frolov** 0:09  
OK.

**Val Levitan** 0:14  
Time off.

0:15  
Thank you.

**Val Levitan** 0:16  
Um.  
The point of this meeting is to have really a brief alignment conversation just to ensure that we're kind of reengaging again and there are some critical points that we want to ensure that we'll deliver.  
And the most critical thing for us is obviously, as you know, is.  
The POS.  
And oh, here's one. Perfect.

**Juan Martinez** 0:54  
Sorry, Val. I didn't realize that everybody accepted.

**Val Levitan** 0:59  
Yeah, I and I didn't realize that I didn't include you in the meeting, so my mistake.  
Yeah.  
So this this should be a quick meeting. It is Nathan's return to day-to-day, so I would like to ensure that this week is productive for us and especially.  
Our following meetings. So what we need to deliver on is the POS system for January.  
In order for the POS system to be installed in January, we need the actual hardware, the POS itself, and then we need a back end system. So we're truly running on fumes here we.  
There's quite a bit of things to do.  
And we're running out of time because it's middle of September and half of December will be a write off.  
And then we have a week in January that Minsk would be off.  
So we're really on a extremely tight schedule. What do we have?  
October, November, December, we have three months, right?

**Nathan Carver** 2:23  
OK.

**Val Levitan** 2:29  
So that's extremely tight.  
So we have our um.  
Hardware design practically at 8590% completion stage in terms of design, selection of material, spatial planning.  
Selection of components, let's call it 80 to 90% done. We're at the point where we probably start designing plastic enclosure and move on into tooling. Am I correct, Genadi?

**Genadi Peari** 3:10  
Yes.

**Val Levitan** 3:12  
OK, Pavel is at the stage where he is putting together architectural block diagram high level I understand.  
And from there we can we must zero in on the MVP capabilities for the POS system only.

**Pavel Frolov** 3:34  
Yeah.

**Val Levitan** 3:34  
And this is where you, Nathan, need to come in.  
The sooner we get it, then we need to move in into finalizing the architectural design for the POS side of it and then identifying MVPS and.

**Pavel Frolov** 3:40  
Yep.

**Val Levitan** 3:57  
The technology stock that we're going to be using.  
And then immediately go into writing the spec for those MVP items.  
Am I missing anything?  
So if we break it down into block diagram, if we break it down into time segments.  
Can you guys estimate or tell me what schedule I'm looking at?  
You're shooting from the hip here, I understand that, but approximately if we have in total three months.  
How can we do that?  
Speak freely. If you if you make a mistake, I'm OK with that.  
You know what? While while Nathan and Pavel are focusing on on the answer, Genadi, can you tell me from your perspective?

**Genadi Peari** 5:07  
Um.

**Val Levitan** 5:07  
What's the approximate time?

**Genadi Peari** 5:10  
The.  
The harder the new boards.  
That to be done by end of.  
Mid of November.  
And the design of mechanics to be done by approximately beginning of November.  
And if we do it one January, January, we can build the prototypes like rapid prototypes and and mass production right after Chinese New Year.  
So February.  
I I don't believe we can do all mold to be completed in January, but a few rapid prototypes, not a big product we can build.  
Will be no problem to build.

**Val Levitan** 6:01  
How durable is rapid prototyping right now?

**Genadi Peari** 6:05  
It's very durable, same like a mold.

**Val Levitan** 6:08  
Really.

**Genadi Peari** 6:09  
Yeah.  
Last time I ordered the sound system for the curved, which I have now, which we completed testing. It's it's perfect.  
It's the same.

**Val Levitan** 6:25  
Except you cannot use those smooth material.

**Genadi Peari** 6:33  
Yes, the finish won't be as glossy as on the real ones, but we can do the colors and we can paint with the glossy so it will be very similar.  
And it's not very expensive, it's.

**Val Levitan** 6:46  
Mhm.

**Genadi Peari** 6:49  
It's um.  
It's OK to us to build like 5 to 10 pieces.  
It's not like if I found the source in the China when they do it really cheaply.

**Val Levitan** 7:11  
OK, so if our if our POS will be ready for January through rapid prototyping.  
What are we looking at from? What are we looking?  
In terms of implementing the MVPS for back end design.

**Pavel Frolov** 7:33  
But then.

**Nathan Carver** 7:42  
So I think for the use cases we have an I I think we know majority 90% of what we need to do. So I can hammer out the rest of these use cases, at least the first version for them.  
I can target end of next week.  
but i'll start as they're polished off, handing them over to Pavel and Juan for review.  
so we can iterate on them. I can focus more on what software fields would unblock them where they can start, and I'm assuming that's going to be  
Device provisioning.  
And those types of features.  
And that way we can iterate.  
Try to have them all done as as soon as possible within the next four weeks, but have enough done in the next two weeks that software has requirements and use cases to start consuming and refining.

**Pavel Frolov** 8:51  
Actually from my perspective, I would say that we are going to implement Incom Cloud Payment Hub cloud application until end of October.  
Together with the module for Flex POS that communicates via this payment hub.

**Val Levitan** 9:19  
OK.

**Pavel Frolov** 9:22  
And until January 1st, I assume that we will prepare first application for Flex POS that can process muto goose.  
Commands saves them internally in Flex POS database and able to produce redeem a card.  
Uh, using payment hub.

**Nathan Carver** 9:58  
OK.

**Val Levitan** 10:01  
So what?

**Nathan Carver** 10:02  
Then the requirements would focus on payment hub first.

**Val Levitan** 10:02  
Want.  
Well, one more thing. I think the requirements also needs to focus on the ACH processing because to me that that's an absolute.

**Pavel Frolov** 10:08  
Yeah.

**Genadi Peari** 10:11  
Yes.

**Val Levitan** 10:20  
Showstopper.  
And Nathan, you already identify one or two specialty shops for the ACH processing it. We need to start a relationship with them immediately.

**Nathan Carver** 10:23  
OK.

**Pavel Frolov** 10:24  
Mm.

**Nathan Carver** 10:35  
OK.

**Val Levitan** 10:36  
We need to get their API and discuss terms of business as a matter of first priority, even before you move with the other requirements.

**Nathan Carver** 10:50  
OK.

**Val Levitan** 10:51  
So if possible this should be your up to today afternoon type of a thing.

**Nathan Carver** 10:52  
I agree.  
OK, I agree. That sounds. I'll do that.

**Val Levitan** 11:09  
OK. And then.  
Yeah.  
So we have our marching orders. I will, I will use this transcript to create initial schedule and I will send Nathan and Juan for review and you guys quarterback it.  
Through through this team.  
Is that OK?

**Nathan Carver** 11:38  
Sounds good. Sounds good.

**Genadi Peari** 11:40  
Yep.

**Juan Martinez** 11:41  
Perfect. Thanks, Val.

**Val Levitan** 11:41  
All right. Anything else we should do?

**Pavel Frolov** 11:46  
Mm.

**Val Levitan** 11:47  
OK, so this meeting is good.

**Nathan Carver** 11:47  
I think we're good.

**Val Levitan** 11:50  
Thank you very much.

**Nathan Carver** 11:51  
All right, thanks everyone.

**Pavel Frolov** 11:51  
Yeah, thank you, Mike.

**Val Levitan** 11:53  
Bye.

**Genadi Peari** 11:53  
Thank you.

**Val Levitan** stopped transcription