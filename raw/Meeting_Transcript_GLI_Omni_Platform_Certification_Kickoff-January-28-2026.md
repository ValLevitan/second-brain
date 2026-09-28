# Raw Transcript — GLI — Omni platform certification kickoff
**Date:** January 28, 2026, 1:01 PM Eastern
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Summary note:** [[Meeting_Notes_GLI_Omni_Platform_Certification_Kickoff-January-28-2026]]
---
00:00:11 Deborah Oxnem
Hi Pat. Hello. Nice to see you. Nice to see everyone. Nice to see everyone as well. I don't think he's going to be able to join us or not. I know he's double booked. So we can go ahead and get started. Thanks for reaching out and sending all the documentation. This was a great way to kick off the year. And I'm excited to hear everything that you guys are going to be working as we move forward. Dan has joined us. Thank you, Dan, for coming.
00:00:49 Deborah Oxnem
You know, we're ready to kick off. So if you'd like, would you like to start.
00:01:00 Pavel Frolov
your agenda actually we are just to synchronize our what will we do for the next steps from our from your side probably before i'll just let me let me make a quick introduction to alignment.
00:01:30 Val
up up until now you have been approving our products based on v1000 amd processor associated along with v1 1000 we had a framework internal name for that framework internally a jdl was called ridge. And Rage Studio was not only a name for framework, but it was a code name for a development ecosystem on applications available 15 years ago.
00:02:18 Val
So we're talking about 15 years ago, we had entire infrastructure that maintained Black Engine. The ecosystem synchronized the development with the output. That has aged certain applications across the capability development ecosystem developed over decades.
00:02:56 Val
Thank you. And with it, we also applied ourselves, at least tested our games in the online market. So between the online market, the aging ecosystem that we had pushed us into a new framework that created capabilities of being online and land-based, and that was based on HTML.
00:03:39 Val
And so fast forward, we are now rolling out a framework. all-encompassing framework that is tied to a new ecosystem development, graphic development, which is based on Unity.
00:04:11 Val
And under it, there is a linking application into the engine. There's Pixy, which rides on top of it, or incorporated inside of the framework, which inside of Omnia, there is a whole database we call it.
00:04:48 Val
So all of that will be sitting on top of a new hardware platform. based on FP7 process. And all of that will be placed inside our existing cabinet, which is, code name for it is Dash Super.
00:05:23 Val
So yeah, we have a sample game for it. We're not putting it in the market. You guys have seen that game. It's called Calle Ocho, my Spanish pronunciation one. Yeah.
00:05:46 Juan Martinez
Muy bien, muy bien.
00:05:47 Val
Muy bien, gracias. Gracias. Yeah, so. we're not worried about the game it doesn't need to function but it you know provides a tie-in for you guys to test that's all we want it has the new hardware to whichever extent you guys need, that i mean we i mean we tested it internally i don't know to which extent you must test it.
00:06:21 Val
approve it for existing markets and the most important thing is i assume testing random. number generator i'm assuming i'm gonna leave it up to you to direct us uh i don't know to actually testing the framing server.
00:06:52 Val
and I apologize I'm not an engineer so from an administrative perspective I'm just if I'm deviating somewhere and going into an area that I'm unfamiliar with I do apologize I'm going to let engineers speak after this in production so approximate date when we would, enter the lab right now it's contingent on one thing that we're still implementing.
00:07:22 Val
which is a bunch of setups we have prior priorities that are driving some other projects therefore Pavel presented the schedule today looks like realistic submission date Pavel remind me if I'm off.
00:07:52 Pavel Frolov
From here, probably in May, mid-May.
00:08:50 Val
September 1st. three games and follow with the submission. But that is the approximate plan for 2026 as we sit here right now, the 1st of February. Is it possible that I made errors? Most likely, but that's where we sit.
00:09:20 Dan Lewis
Yeah, I always try to set things up, new challenges.
00:09:30 Val
You're right then. And those are just, accept those as estimates, yeah.
00:09:40 Dan Lewis
Yeah, basically what you've done for me so far, I don't feel like it's all that much of a job. We've been working with suppliers. All right, so we're going to need to develop again. It's not that much, but I think we'll be able to get through that.
00:10:13 Dan Lewis
The biggest sales line, the implementation, just the way that, you know, some white paper. have implemented would be helpful to what additional analysis would be needed.
00:10:46 Dan Lewis
Hopefully there's women. I think that was the big take.
00:11:01 Pavel Frolov
so in general words actually mask plus rng that we are going to use for land base will be. as it was introduced for online mark we will package your rng into a container, that will be its usage continue with the previous platform it's very close.
00:12:17 Val
Is it just a logic board, or are we changing the I.O. board.
00:12:27 Pavel Frolov
Actually, yesterday I saw some documents. Gennady updated documents related to hardification. Yeah, it's minor changes. We requested possible changes related to some new printers. We've accepted an optional device.
00:13:19 Deborah Oxnem
are we uh you know previously we needed to take a look at additional pearls so that we could put them in letters for are we in a situation where we can test all possible proof and should we have should we should we try to schedule it so that we test all cameras so that they can all be in the appropriate letters or will we know more when we get closer to the submission i think.
00:13:59 Val
you're right. Dan, explain that to me, show it up for me.
00:14:22 Dan Lewis
Yeah, so let's say, let's list in that, what you're...
00:14:40 Val
So do we need, why don't we create a list of all possible peripherals that we're using, and align ourselves with you on how, so we can test it at one time, it's always cheaper to test it at one.
00:15:01 Dan Lewis
Totally, that's about what... We're not going to do a whole new test all over again. We're going to test whatever we can and we'll do it with whatever.
00:15:29 Val
As undertaking for JVL, we should probably create a list of these employees, incorporate in our...
00:15:40 Dan Lewis
Yeah, agreed.
00:15:42 Juan Martinez
We'll list them all and I'll put a note by previously approved. We don't waste time on something you've already approved and then highlight the new...
00:15:52 Dan Lewis
Exactly, and what's the hard...
00:16:04 Val
And another, just for proper housekeeping, another undertaking for JVL, you wanted a white paper from JVL to you on how our math and RNG is architectured within the new framework.
00:16:27 Dan Lewis
Yeah, exactly. That's how the RNG is called, so it makes it easier.
00:16:48 Val
So, Yefim, this is an undertaking for you, I understand, okay? Okay, anything else, any other undertakings for us.
00:17:05 Dan Lewis
As you develop the games and everything, again, any additional information can provide how we can use those games. I'd also like to talk to you going into a new ecosystem, ways that we may be able to work so that GLI can do some things. But I want to have an ecosystem and have your ecosystem and generate this rather than somebody making it.
00:17:45 Val
Okay, so that will be an undertaking for you then or your side to give to us.
00:17:52 Dan Lewis
Well, that's something for I'm up with it.
00:17:57 Val
So what is the logical architecture for working together.
00:18:23 Dan Lewis
So I think you're asking for another white paper from JVL.
00:18:36 Val
on how we see you embedding your file and getting an output.
00:18:43 Dan Lewis
Well, I think what I'd like to do is what it is. I would like to minimize verbal discussions.
00:18:58 Val
I do appreciate them, but I would like to minimize it, so I do like the idea of us initiating the white paper, you assessing the white paper, and reflecting on it, and then suggesting something else. It's much more efficient than a congressman.
00:19:14 Dan Lewis
Okay.
00:19:15 Val
So, I'm taking it as JVL's undertaking, to provide you with the white paper.
00:19:25 Dan Lewis
IQA testing.
00:19:31 Val
Correct, correct.
00:19:33 Dan Lewis
Maybe we can just build upon that.
00:19:37 Efim Podvoiski 
So, do I understand correctly, then, that you are looking for something like a scale, say, I push these numbers, and I want to see this set of numbers after they are used.
00:19:58 Dan Lewis
Yeah, and in that perspective, anytime there's a deviation, we'll get something that we need to look at. But we'll spend maybe a few hours to do the task.
00:20:33 Dan Lewis
But we've only invested, and it also provides us a better...
00:20:49 Deborah Oxnem
Awesome. Yeah.
00:20:52 Efim Podvoiski 
The change here, I defined was at some... How many? What's the names and some text form.
00:21:02 Dan Lewis
Well, exactly. So, we'll go through your part and say, here's, so we'll be looking for, yeah, here's the real stuff. Yeah. In addition to that, it pays by. We have tools that will look at the image of results and it will then evaluate window, what, you know, based upon.
00:21:47 Dan Lewis
We give it an image of what a chair is supposed to be on the screen and it will compare to that. I mean, that's how I live.
00:22:19 Val
Understood. So we will initiate this white paper and then wait for the cabinet. I have another question or statement. I assume that because we are using the same cabinet as you have already approved, things like electrical or discharge is not applicable in this particular case.
00:22:48 Dan Lewis
Yes, that's not good, especially if it's just a logic. Of course, any new like you're. A few hours.
00:23:20 Val
So, Gennady, do we need any pre-screening on this? Gennady, you're on mute.
00:23:48 Juan Martinez
It doesn't look like we need any pre-screening for this method. It's the test. So, we'll just allow GLI to do their own.
00:24:09 Val
their own set up screens we have a lot of them what is the most efficient way to submit that to test it or to verify as we could probably automate that submission.
00:24:34 Dan Lewis
quite a bit well we're changing practically every single screen that.
00:25:07 Val
there is out there so. Okay, would you accept a white paper from us on how to test it? Because we could probably provide you with a lot of automation.
00:25:23 Dan Lewis
You could supply us. So another undertaking for JVL is to provide white paper for testing of setup script.
00:25:39 Val
Understood. What else am I missing? Okay, so that should conclude our meeting unless anybody else have any questions.
00:25:55 Deborah Oxnem
On my part with the commercials, how would you like to see those homecrafted? Are we starting with? Do we want to make, how do you want us to proceed that way? And then I'll make sure we have enough information to provide scope and things like that.
00:26:12 Val
I'm not sure I understand the question.
00:26:16 Deborah Oxnem
Before we close up, would you like me to read a proposal for you or until we get closer.
00:26:23 Val
No, until we get closer and until you understood our white paper, only then provide us with the proposal.
00:26:32 Deborah Oxnem
You got it.
00:26:33 Val
And that's why we're starting early. I want to start early. I want to make sure that everybody understands the scope, the requirement, the objective, and all of that. And we have plenty of time right now, so let's work diligently on understanding what needs to be done.
00:26:50 Deborah Oxnem
And then if you have any follow-up questions from the documentation, would you like us to reach out to you to then disseminate internally? Or would you like us to reach out to the whole group.
00:27:03 Val
what is your preference no my preference is not to pollute mailboxes so juan and myself are planned and we'll decide how to disseminate the information, great so just one comment i noticed that uh judging by the backgrounds dan and eupheme are in this on the same the same zone same vacation, so enjoy your vacation guys i see that you're together on a vacation, there you go good for you good for you i hope you're on earth.
00:27:34 Val
you're on earth somewhere this is earth it looks like a different planet yeah it looks like a different planet okay thank you very much everyone and enjoy
