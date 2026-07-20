---
tags:
  - printer-interaction
  - data-dumping
  - transcript
  - pavel
  - genadi
  - technical
---

**Transcript**

July 14, 2025, 12:03PM

**Nathan Carver** started transcription

**Nathan Carver**   0:03  
Agenda. We should be pretty quick today. Feedback from the meeting we had with Jim.  
On Friday about the printer and specifically that confidence number, that is what we what you thought it was, Pavel. So it's it's a hash basically at the entire ticket data, he said. That's not a problem. He can share that information with us, so that should save us a little bit.  
At a time, he's also writing up.  
Some more robust documentation to send us on intercepting that print signal. We'll ping him today just to make sure that that's still in flight and try to get an idea on when we can expect it, and then that should feed into whatever spike work.  
You have going.  
I think that was it. I think that's all we got from Jim. We're gonna get also look at the transcript of that downloaded and and shared.

   0:57  
Good.

**Nathan Carver**   1:08  
While I know you're driving, if there's anything I'm leaving out, please jump in and let me know.

**Genadi Peari**   1:16  
Any any feedbacks about type of printers? Are they all same communication or it will be in the in the his writings right in the write ups?

**Nathan Carver**   1:30  
Yeah, I did ask him about the different printers and he said that the print signals are all ASCII, so we should see tad spaces, characters and line breaks essentially. So he was.  
Pretty confident that the type of printer they're sending to shouldn't affect us. Um.

**Genadi Peari**   1:51  
OK.  
Good.

**Pavel Frolov**   1:54  
It is.

**Nathan Carver**   1:57  
Now we'll get more detail from him, but hopefully that's pretty straightforward since it's asking.

**Genadi Peari**   2:06  
So it seems POS more or less from the hardware point of view it's like mostly defined if the the the answer from him positive. I don't see any any.

**Nathan Carver**   2:21  
Mhm.

**Genadi Peari**   2:23  
Outstanding questions about the US.

**Nathan Carver**   2:27  
OK, great. Perfect.  
And OK, so.  
That's all for that. Next on the agenda is just prepping for the spike. Paul, do you have any updates there? Are we ready to get started on that or do you need anything, anything more to get started?

**Pavel Frolov**   2:52  
Actually, I think we are ready to to make spike for.  
Uh, data printed on the ticket.

**Nathan Carver**   3:03  
Hmm.

**Pavel Frolov**   3:06  
To get dump of all the data.  
Of the real ticket.  
But I think this is a quite a simple, simple task.

**Nathan Carver**   3:16  
OK.

**Pavel Frolov**   3:20  
And then this data can be used by developers who will develop.

**Nathan Carver**   3:24  
Um.  
No.

**Pavel Frolov**   3:27  
Actual data dumping from the printer and using Java application for this.

**Nathan Carver**   3:32  
Mhm.

**Pavel Frolov**   3:40  
But as as a as a first stage, I think I will connect the real printer and dump all the data.

**Nathan Carver**   3:53  
OK, sounds good.  
So for um, let's see.  
We had our um.  
Alright, I'm gonna pull up so I can share my screen here.  
OK, sharing. Let's see.  
OK, so we have this the ticket storage then work items in in Confluence. We just have to move those to Jira and then.  
You all can create a branching link to them.

**Pavel Frolov**   4:45  
OK.

**Nathan Carver**   4:48  
And if there's, I know we looked at this already. If there's anything in here, Pablo Kanati, that needs to be updated.  
Feel free to just comment update in this in this document.  
And then we'll create the reference to to JIRA. But I think this is pretty straightforward. If there's any questions in here, we can go through them now, but it's gonna be just.  
I queued up the FR 1.1 which is intercepting the print data and then F 1.2 which is store complete ticket metadata. The third one we have is initially we had generated basic integrity hash, but this may just be switched over to.  
Being able to verify the redemption or the confidence number on the printed ticket, or at least to regenerate our own confidence number so we can we can compare them.  
And then we also have going forward the ability to reprint the ticket and there may be some design decision we need there. Do we store the ticket metadata in a record and then should the cashier decide the print they can print?  
From Flex POS? Or are we just a straight pass through or it just prints while we read it?

**Pavel Frolov**   6:23  
I think we do not need, at least at this stage, this function to reprint the ticket from the POS. I think we just need to capture all the tickets.  
And that's all only in read only mode. In this case, Printer will be driven only by Mutogoose hardware and we will will not need to.  
To produce any special behaviour to to support multi master on RS232.

**Nathan Carver**   7:06  
OK, OK.  
So we won't do this for now, and maybe we won't have to at all. So OK, good.

**Pavel Frolov**   7:16  
But but at at this moment.

**Juan Martinez**   7:16  
Guys, I just arrived at the casino. I'm gonna have to drop off. Thank you.

**Pavel Frolov**   7:22  
Yeah, yeah, yeah, you're welcome. At least we need to support processing of a reprinted ticket. We do not need to.

**Nathan Carver**   7:22  
All right. Thanks, Juan.

**Pavel Frolov**   7:38  
To produce multiple redemptions if it repeats the same ticket.

**Nathan Carver**   7:49  
OK. Oh, gotcha. Right.  
If they try to, yeah, if they try to redeem the same ticket again.  
OK.  
OK, perfect.  
All right.  
OK, I think that's all. So we'll put those two tickets in JIRA and then as far as the source of truth.  
The.  
For the documentation of the requirement.  
I think we have some options. We could keep that in JIRA, but a better source of truth may be GitHub, so it's easily referenced. And then we have a link. We just have a hyperlink reference back to the JIRA ticket with a summary information for.  
Um, just for a process tracking, process flow tracking.  
Pavel, do you have a a preference on that? It would it be useful to have these?  
In the repository, I know Val would like us to get more things into GitHub so we can transition away from.  
Atlassian.

**Pavel Frolov**   9:11  
Actually, I do not have any preferences of using either GitHub or Confluence, but I agree with Val that it's better to have to have all the documentation at one place. That's why.  
We need to to place it in GitHub.

**Nathan Carver**   9:28  
OK.  
OK, I'm gonna continue putting things into that flex POS repo and under the docs I'll just I'll create some very simple folder structure, just like architecture and requirements to start with just.  
They keep it simple and I'll put the files in there and then create the Jira tickets and set up the links.  
And just keep you updated there.  
Let's see. That's about it for me. My morning is busy. I'll try to sync up with Juan later today on the Jira side, so you all have it ready to go.  
Oh.  
Uh, tomorrow.  
OK, that is it. That's all I have for planning. Is there anything?  
Pablo Ganati, you want to bring up before we before we break?

**Genadi Peari**   10:33  
Um, I've heard the.  
I I think Wal has had some news about like new ideas about the redemption center. Do you know about it or something?

**Nathan Carver**   10:48  
Oh, no. Was that did that come out of last Friday?  
Do you know when that was brought up? I don't. I I can't think of off the top of my head what that is.

**Genadi Peari**   11:03  
OK, because he postponed the getting sample of the node recycler but.

**Pavel Frolov**   11:11  
Hmm.

**Genadi Peari**   11:15  
Anyways, OK.

**Nathan Carver**   11:17  
OK, yeah, I don't. I'm not sure.

**Genadi Peari**   11:20  
OK.

**Nathan Carver**   11:27  
All right.  
Well, I'm good with breaking early, if you all are ready.

**Pavel Frolov**   11:33  
Q.

**Genadi Peari**   11:39  
Sure.

**Nathan Carver**   11:40  
OK.  
All right. Thanks all. Um.

**Pavel Frolov**   11:44  
Mm-hmm. Yeah. See you on.

**Genadi Peari**   11:46  
Bye.

**Nathan Carver**   11:46  
I'll see you later. Yeah, ping me with any questions. That should be good.

**Pavel Frolov**   11:50  
See you on on Wednesday.

**Genadi Peari**   11:50  
OK.

**Nathan Carver**   11:53  
Yep, on Wednesday.

**Genadi Peari**   11:55  
I will.

**Nathan Carver**   11:56  
Yes.

**Pavel Frolov**   11:57  
Yep.  
Yeah.

**Genadi Peari**   12:07  
Um.

**Pavel Frolov**   12:13  
It's just possible.  
Go.  
OK.  
We could go in for March.  
OK.  
Oh, show the light of the.

**Genadi Peari**   12:57  
Listen.

**Nathan Carver** stopped transcription