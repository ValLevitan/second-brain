**Claude_Code-Yavorski-20260210_160117-Meeting Transcript**

10 February 2026, 01:01pm

6m 48s

**Dzmitry Chudzinau** started transcription

**Aaron Bockelie** 0:07  
Eugene, what have you tried since we last chatted? Anything?

**Eugine Yavorsky** 0:12  
1.  
Alright, I tested the what what we have done.  
Build was successful, but...  
What we have really, what, what, what really was done was unfortunately wrong, because AI make logs into...  
In the console instead of EE prone. So it was supposed that we keep our logs in EE prone.  
But it's totally misunderstood our concept and put our logs in just user console that use it inside, so...

**Aaron Bockelie** 1:02  
Okay.

**Eugine Yavorsky** 1:04  
Unfortunately, what I done was totally wrong, but some connection, all built, everything worked fine.

**Aaron Bockelie** 1:14  
So, all we have to do is correct it now, just ask it to change this, change the spec.

**Eugine Yavorsky** 1:14  
But.  
Yes, I will try to do it myself, but it's not so.  
It's very difficult to work from CMG line. Why difficult? Because I need to see from time to time what rail code he has done, understand the code and probably make some correction steps.

**Aaron Bockelie** 1:45  
Mhm.

**Eugine Yavorsky** 1:51  
So, just give the task.  
and hope that we totally understand it and work in correct way. This concept, it's not working fine. So we need to probably split task to more small task and control how it's doing.  
probably see the code, something like that.

**Aaron Bockelie** 2:19  
So probably what's going on also is Eugene, we don't have a spec for how you were writing that out. So for instance, yeah.

**Eugine Yavorsky** 2:19  
Liz.  
Yes, correct. We we we don't explain him the I what we want really. We just put him couple couple sentences and hope that he understands everything. Probably we need to to.  
Keep more detailed information for him, provide something and control what he is doing.

**Aaron Bockelie** 2:52  
Yeah.

**Eugine Yavorsky** 2:53  
And correct him, something like that.

**Aaron Bockelie** 2:56  
Well, maybe what we could do is kind of focus on the spec of what's expected instead of writing code, right? Because if you don't have a specification, how could you possibly write code that fits the spec, yeah?

**Eugine Yavorsky** 3:13  
Maybe, maybe, let's try.

**Aaron Bockelie** 3:16  
So, do you know how?  
You, when you, when we initially had the change and wrote it, we used JIRA to pull information in, and then looked at what was going on, and then noticed that the issue was empty.  
Build it in, then write the code, and then put it out into the thing, right? That was kind of the pattern we did last time.  
And if you think about it for a minute...  
The JIRA issue became the specification for what was created.  
Yeah, so, like, if we if we looked at the JIRA issue, for example, could you share your screen for a minute and let's go back and look at that JIRA issue?

**Eugine Yavorsky** 3:53  
Maybe, maybe.

**Val Levitan** 4:15  
I just, I just wanna set the agenda, maybe.  
May, may I interject quickly?

**Aaron Bockelie** 4:22  
Sure.

**Eugine Yavorsky** 4:22  
Sure.

**Val Levitan** 4:23  
The agenda is to pass knowledge from Eugine, the contractor, to JBL.  
The the the.  
the company that ordered the service.

**Aaron Bockelie** 4:42  
Right.

**Val Levitan** 4:43  
It's A1 one-time transaction, one-time knowledge transfer.  
We, I mean, Eugine has his way of thinking and working and being, and we don't wanna change that.  
He is not a JVL employee. What we do want, we want to pass the knowledge in an organised format where JVL becomes the owner of that project. That's all we want to do.

**Aaron Bockelie** 5:00  
Yep.

**Val Levitan** 5:13  
And we want to do it in the most compressed, the most efficient time, because we're kind of at the end of the project, we're grabbing the ownership of it, the knowledge of it, and that's it. And we're done.

**Aaron Bockelie** 5:28  
Maybe what we could do instead then, Val, is that I could go ahead and clone all of the repos that Eugene's worked on and just set up all the framework myself. And then I'll basically write a bunch of pull requests for Eugene to review to make sure that the understanding is correct.

**Val Levitan** 5:45  
The most efficient way, the fastest, the most efficient way.

**Aaron Bockelie** 5:49  
That might, that might work pretty good.

**Val Levitan** 5:49  
If, if this is...  
If, yes, and Eugine, I told you, I know Eugene for decades. So he is the most honest, the most honest, the most faithful guy. So he is not keeping anything. He is gladly going to share the knowledge.

**Aaron Bockelie** 5:52  
Yeah.  
Yeah.  
First.  
So, let's do this, Eugene.

**Val Levitan** 6:11  
Yes, I like that proposal very much. Let's get it efficient. Let's take it over and let's move on.

**Aaron Bockelie** 6:18  
I'll just wrap up with this, Eugene, just to kind of...  
finish this thought so I can explain what I'm going to be doing as well. So let's go back to JIRA and look at the actual JIRA issue that you were working on.

**Eugine Yavorsky** 6:38  
And.