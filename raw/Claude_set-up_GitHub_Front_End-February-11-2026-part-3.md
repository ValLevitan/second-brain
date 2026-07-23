**Claude set-up for GitHub for Front End development-20260211_092416-Meeting Recording**

11 February 2026, 02:24pm

47m 26s

**Aaron Bockelie** 0:03  
No in flex POS.  
Didn't you?

**Pavel Frolov** 0:08  
Orchestration part, registration server and part related to CXPOS operating.

**Aaron Bockelie** 0:20  
Yeah.  
So, so I'm gonna open up the Flex POS repo on my machine here. So bright bright mode for stuff, OK.  
So I see Flex POS.  
I see flex O back end and front end.  
I see somebody has accidentally committed the dot cloud directory in there.  
I guess fine, but we're gonna use Waze and fix that.  
That would be Nathan Carver and we can bring that into we can take his ways and uplift them in or his commands and uplift them into ways.  
Uh.  
Let's go. OK, so here's here's like platform flex POS, yeah.

**Pavel Frolov** 1:26  
Yeah.

**Aaron Bockelie** 1:32  
The front end and back end are part of the same monorepo. It looks like this is is what I see.

**Pavel Frolov** 1:39  
Yes.

**Aaron Bockelie** 1:41  
And.  
Here is the plot instructions, right? Good start. It's quite long. This is older because it was committed six months ago. Plot code has changed and we're using Waze and some other stuff.  
So I can tell you right now that my observation is this repo needs some work. It needs to take these and and weave them into the Waze system. We're going to use that and we'll still have a dot cloud directory, but it's going to look different than the way it is now.  
O We have agents right here, and I can tell you right now that having this many agents in cloud context is really challenging.  
This is a ton of context that's going to basically make log code very, very difficult to use.  
Because it's too much.

**Pavel Frolov** 2:42  
Mhm.

**Aaron Bockelie** 2:44  
Uh, when we look at the commands.  
This is also too much because the it's too too detailed. It's a good start, but cloud code has gotten a lot better in the last six months than this than than this and we don't need all this.  
So just like how software is changing overtime with new versions, we can think that active development on tools like Cloud Code are rapid and move really really fast and so these prompts have to get changed.

**Pavel Frolov** 3:18  
Aaron, I'm sorry for interrupting you. Seems I will need to leave this conversation and left you without me because right now we're going to.

**Aaron Bockelie** 3:24  
Yes.

**Pavel Frolov** 3:34  
Dumitrius Dwola.

**Aaron Bockelie** 3:37  
OK.

**Pavel Frolov** 3:38  
And seems I I need to help our team to translate at least.

**Aaron Bockelie** 3:42  
Oh, boy. OK, we'll we'll be fine. Thank you, Pavel.

**Pavel Frolov** 3:45  
Probably I will return back to to this conversation until you finish, I would say. OK.

**Aaron Bockelie** 3:53  
Sure. We'll we'll work it out. Thanks, Pavel.

**Pavel Frolov** 3:56  
OK.

**Aaron Bockelie** 4:00  
OK. So Anton, you're mostly working in platform Flex POS, yeah?

**Anton Seregin** 4:10  
No, currently I'm mostly have working on my first the repo I.  
Messaging. It's a infrastructure construction core front end was the first in list.

**Aaron Bockelie** 4:23  
OK.  
This one.

**Anton Seregin** 4:33  
Just flex POS, mostly pages is completed, are completed.

**Aaron Bockelie** 4:43  
This one here in orchestration core.

**Anton Seregin** 4:47  
Yeah, it's a project that will be developed next next month and.  
Actually, uh.  
Actively developing will be here so.  
I can.  
Describe something about structure or architecture about this project. It's also one that.

**Aaron Bockelie** 5:28  
Actually I'm what's funny is I'm just reading the cloud MD that you have up here, which is as descriptive as anything to understand what's going on. So you have a web pack module federation that allows multiple front ends depending on user access controls.

**Anton Seregin** 5:30  
What?

**Aaron Bockelie** 5:48  
Or groups or something like that to present different customized user interface. Is that correct?

**Anton Seregin** 5:55  
Yes, it's correct. We have many, we will have many micro potent services which can be deployed in for example Docker.

**Aaron Bockelie** 5:59  
OK.

**Anton Seregin** 6:11  
Continuous.

**Aaron Bockelie** 6:12  
Right.

**Anton Seregin** 6:13  
And so on.

**Aaron Bockelie** 6:16  
Is there a architecture description of how this fits into the bigger picture?

**Anton Seregin** 6:26  
Uh, no, we don't have now, but we can uh, next page.

**Aaron Bockelie** 6:34  
OK.

**Anton Seregin** 6:34  
So.

**Aaron Bockelie** 6:36  
So, so one of the things that we've got to consider here is giving context for not even just cloud code, but just for regular humans. For me, my very first question I ask to my mind when I see this repo is.  
How does it communicate with the other parts of the ecosystem?  
Right, like I'm imagining the flex POS, the little the little hardware reader with the screen. I'm assuming maybe pulls these little front ends and uses them to render stuff, I'm guessing.  
But I don't know, I'm just guessing. And so with no context of how this fits into the bigger architecture, there really is no way for me to understand how to potentially see how this fits and what it communicates with.  
So.  
If we were to try to apply some of the practices I'm talking about.  
You can. It may be perfectly fine for to to just do some of the ways config and add some documentation and basically set U some tools and be done especially.  
If you are the only person essentially working on this, however.  
If you don't want to be the owner for forever of this, like if you want to be able to work on something new besides this at some point, you need to be able to hand it off and have sufficient context for where it fits into the architecture at JVL, right? Like otherwise.  
Everybody's going to ask you for the entire time you continue to exist at JVL how this works, and you don't want that.  
You want to you want to hand this off as soon as possible.  
So.  
Is there anywhere if if this is JBL core?  
And we have these repos in JVL core.  
Is there any other project that references the infrastructure orchestration repo?  
What? What consumes this and what provide? What's the the getters and setters for this? What's the feeders and consumer, the feeders and the consumers?  
Where does this sit in the in the ecosystem?

**Anton Seregin** 9:22  
Uh, it's uh.

**Aaron Bockelie** 9:23  
Vladimir, you're shaking your head like you have no idea.

**Vladimir Samusenko** 9:26  
I I I just I even have access only for.

**Anton Seregin** 9:27  
OK.

**Vladimir Samusenko** 9:35  
I guess and I I it's my first time I see how much, how many, how many repositories we have.

**Aaron Bockelie** 9:47  
Yeah, well, surprise.  
We'll get you. We'll get you more visibility as soon as possible.  
So one of the things that we're going to immediately bounce against, up against, we're going to run into problems with is a unifying architecture understanding of how the entire ecosystem works.  
What's happened is, is that a lot of people have kind of said the same thing over and over again, right?  
And.

**Anton Seregin** 10:32  
Yeah.

**Aaron Bockelie** 10:34  
We we're going to need to, I think. Unfortunately Pavel needs to kind of steer some of this and he's busy, which is.

**Anton Seregin** 10:36  
OK.

**Aaron Bockelie** 10:45  
You need to be able to reference in in your orchestration core front end here.  
You need to be able to reference all the other pieces where this goes to and what it depends on. What are its dependencies? Essentially right? Like if this runs here, what is it serving?  
And what? What serves it?  
We can set that aside for a minute and instead talk about how do we align this repo with the Waze and make sure that we are capturing the and converting this into a system that makes sense for Waze.  
I have a feeling with the time remaining we're not going to get to.  
Doing it unless I do it. I could clone this and instantly change this to work with Waze, but I think you guys need to actually make it make it a a a pass at doing this or you'll never learn.

**Val Levitan** 11:52  
You you should do it, Aaron. It will expedite things.

**Aaron Bockelie** 11:57  
OK.  
You guys OK with that? Because I'm going to, I'm going to test you afterwards about how you're going to make it work.  
You're gonna you gotta pay attention here.

**Val Levitan** 12:08  
This this this meeting is recorded. If you talk through this, it will be a good lesson.

**Aaron Bockelie** 12:17  
All right. Well, let's see here.

**Val Levitan** 12:17  
Um.  
We're recording audio and video, so try to share your screen. Is is Pavel still on?

**Aaron Bockelie** 12:26  
Yep.  
He had a translation thing he had to run and do.  
All right, here's what I'm going to do. I'm going to switch over to JVL mode here on my machine.  
I'm gonna clone your repo, Anton.  
I'm gonna invoke Claude.  
And as you know, I already have my latest version of Waze configured on Cloud right now. It doesn't look any different, but it's all there.  
So what I'm going to do is I'm going to just start a prompt and I'll share the prompt with you guys in chat.

**Val Levitan** 13:32  
Yes, a piece of work that meeting. Yeah, transcript. Yeah, establish.  
OK.

**Aaron Bockelie** 14:37  
So what I want you to do is think about this prompt and maybe translate it to to Russian and think about it that way and almost go back and try to type it back, type it up again.  
OK.  
So as soon as I put this in here, we get 123 different coding agents simultaneously reviewing the repo and looking at the ways OK.  
We're going to let it.  
Do things.  
The other thing I'm telling it, I'm reminding it.  
Is this?  
Now it's found everything. It's looking at the Waze. It's going to go ahead and create the local template for Waze and do all the work.  
So it's going to share the findings and discuss the ambiguous pieces of this project.  
So what it's binding and what its status is.  
So it's going to look at. So now we have this dynamic kind of constructor here for what we're it's asking questions. Now what ADR domains make sense for this front end monorepo? The template ships with this. I'd suggest domains that reflect the actual decision space here.  
Is it front end focused on the architecture, shared deendencies, patterns, UI framework, theming components? O look we have.  
These guys here, these ones here, these ones here. So we have core front end infrastructure and integration. Those are the architectural decision domains that it thinks we need to put together for this repo. Is that sound right, Anton?

**Anton Seregin** 18:13  
Yes.

**Aaron Bockelie** 18:14  
OK, I'm going to choose that.  
And for for local domain, for local ways, we're going to create some starter ways.  
The current Claudmd is doing everything. Architecture, docs, import conventions, webpack patterns, MF set guides. Should we restructure it? Yes, we're going to slim down and move to the Waze system.  
Did we write an inaugural ADR documenting that the Waze adoption itself, it's meaningful architectural process decision worth recording? Yes, absolutely. So CI just it kind of just gave us the choices already.  
And it's new to you, this whole ways thing and architecture, ADR and whatever. But to me this is a massive convenience. I just say one thing and it already does all the stuff I've already been working on for weeks and months to configure and impose the governance in this repo.

**Anton Seregin** 19:05  
But.

**Aaron Bockelie** 19:14  
So all I have to do is say yes, submit answers and because the ways we have are available, it's now following all these instructions to go get this all set up for us.

**Anton Seregin** 19:18  
Hey.

**Aaron Bockelie** 19:27  
We're gonna allow it to create all this stuff.  
So it's gonna copy in ADR tools. It's gonna create the different domains.  
Of ADRS for us.

**Anton Seregin** 19:50  
Yeah.

**Aaron Bockelie** 19:56  
Vlad, just to pick on you for a minute, this process equally applies to the repos that you will be working in too.

**Vladimir Samusenko** 20:03  
Yeah, yeah, I'm just.

**Anton Seregin** 20:03  
Yeah.

**Aaron Bockelie** 20:04  
Yeah, yeah.  
So we've had our first ADR adopt ADR driven development with Waze system.

**Anton Seregin** 20:11  
OK.

**Aaron Bockelie** 20:15  
And it says this front end monorepo has grown to include multiple micro front ends, a host application, a BFF service, shared libraries and complex Webpack module federation configuration. Architectural knowledge lives primarily in a single cloud dot MD file that's 200 lines.  
Lines that acts as both roject documentation and AI guidance.  
This creates several problems. Flat guidance. All context is loaded regardless of what you're working on. No decision trail. Past architectural choices aren't recorded with the reasoning. Onboarding friction. New contributors, human or AI, get a wall of text.  
Rather than contextual, relevant guidance.  
These are the problems we're solving by defining this.  
Oh well, I'm just gonna let it create all this stuff. Does it take forever to read through this with you? And what we'll do is get this sort of initially configured.  
Now good, let me slim down Claude MD. I need to move the domain specific guidance into ways and keep it focused on the things.  
I'm just gonna give it a little reminder for this.  
I'll share what I just said here.  
One of the things that Claude does very well is a pattern of creating what is I call A to do list.  
To do something, something and.  
If we keep that in there, what happens is to do lists, if not properly get ignored, can can leak into the repo, the main repo. We never want to have to do lists leak into the main repo because they're always out of date. There's something specific to the developer doing contribution with, so like Anton.  
You have a.  
To do list in your copy of this repo on your machine and then you commit it and then I clone it. I'm going to get your to do and I'm going to be doing different things than you're doing and then confusion happens, right?

**Anton Seregin** 23:22  
Yes, if I put this prompt and.  
I have uh.  
Some different answer.

**Aaron Bockelie** 23:32  
Yeah, so so what's going to happen here is I don't want you to actually commit it because you don't have the latest Waze installation and I do probably. So let me do this work in this branch and I will push this up to the repo and then you can clone it down. But you also have to clone the latest version of the Waze into.

**Anton Seregin** 23:34  
OK.

**Aaron Bockelie** 23:52  
Your environment before you can start really using this.

**Anton Seregin** 24:06  
Uh.  
I don't have one question. We need to repeatedly.

**Aaron Bockelie** 24:08  
So.  
Yeah.

**Anton Seregin** 24:16  
Around this ways in in our project.

**Aaron Bockelie** 24:23  
No, you never have to run it once it's set up right. It just works. It just exists.

**Anton Seregin** 24:26  
Yeah.  
And this can have some changes in future and we need to sync it with our repo.

**Aaron Bockelie** 24:47  
So there's repo scope ways, there's project scope and there's user scope. OK, just how just the same as Claude has user scope and project scope instructions. Waze work on project scope and user scope as well.

**Anton Seregin** 24:48  
OK.

**Aaron Bockelie** 25:06  
So what's happened here is that we've created some specific ways for this project that I never want to incorporate into my user scope because it's specific for this project. So we have a a build way, a front end way, and a micro front end way for this.

**Val Levitan** 25:10  
OK.

**Aaron Bockelie** 25:22  
We've taken apart the original Claude document that you have and put it into Waze.  
And we've now set up the ADR system to be able to begin to make decisions.  
These are the principle changes that I that's going on here and we're going to get the ways committed and all the other bits here. So this is kind of a way to.  
Give that guidance.  
Into the project repository when it gets cloned now. So what we're going to do, I just want to get through this and and kind of finish up this this phase of this for a minute.  
Do you see how it offers to commit this and push so you can review in GitHub?  
Want me to commit this and push so you can review in GitHub? You see that question?  
It's offering something to me.  
Pod code out-of-the-box doesn't do this. It just sits there and waits for the next thing for you to tell it what to do. This is the Waze stuff getting added in the secretly in the background and you don't even see it happening because it's being injected in inside of the context.  
I'll show you how to audit it in a second. So I'm just going to say yes, commit and push. I'm just going to literally hit tab.  
So I'm gonna at follow up with this.  
Ush. Now let me run a code review focused on the ADR set and documentation changes.  
So this is the next romt that I I told it to say here.  
And so now it's going to just you're reviewing the changes on the branch. The intent of this PR is to adopt ADR driven development and a ways system for contextual guidance. Here's what was done.  
Tooling was installed, the first ADR written about ADRS. The local project Waze was created, Cloud MD was refactored, Gitignore was updated and we created the first index. Your review focus is is it set up second is.  
Is it well structured? Third is, does it still make sense?  
There's no better tool to configure Cloud than Cloud itself, basically.  
We're going to let it run the review. It's doing so right now, and if you were to go over to the repo right now, you're going to see that there's a branch out there.  
We're going to look at this internally right now.  
We're doing an internal review. We're going to come back and address any things it might find.  
Because I'm I'm managing intentions right now. I'm not writing code. I have intentions. I I intend to use a DRS. I intend to set up ways to work this way. I intend to give you tooling to operate this platform. I don't know anything about what you're working on yet, Anton.  
Because I haven't really looked at it, I don't know nothing, but I intend to set this structure up and that's the level I'm thinking about. I'm not thinking about what code I'm writing, I'm thinking about my intentions.  
I know it looks boring. We're just sitting here waiting for paint to dry, so sorry, it's a little bit slow.  
I have been noticing there's been a few network hiccups and this is taking almost longer than I want it to, but we'll see what happens.

**Val Levitan** 31:09  
H.

**Aaron Bockelie** 31:55  
So something I noticed that we should probably update is the readme, which is a little out of date, so we're going to make sure that we get this all put together too.  
It looks like the other agent might be sticky right now, so I'm just going to manage that. Nothing ever goes right in demos, yeah?  
So I noticed that sometimes.  
When initially setting this stuff up, it gets a little bit messy because these tools try to look at everything in the environment. So I just was watching that. No, that usually doesn't happen, but I'll look into that. So what we have is the review findings is the ADR system looks good. Waze is fine.  
Let's fix those things.  
I'm going to say let's fix those two things, which is trailing, trailing new lines and sort of defining the the project. Read me a little better.  
And we're going to create a pull request U on the repo.  
And So what I want you to do, Anton, is as soon as that pull request is up there, I want you to go look at it.  
Now there's two ways you could look at that pull request. You could look at it with your own eyes and read it, which I suggest you do, but then you could also as a second thing, literally while you're reading it with your own eyes and inspecting it.  
If you have your cloud configuration baseline set U you could have cloud insect the R as well and add some commentary as to what it finds as well.

**Val Levitan** 35:28  
Yeah.

**Aaron Bockelie** 35:31  
And you could direct it based on what you saw first. So the order is just like the sandwich, right? You are going to read this PR and then you're gonna say I'm concerned about these things and then you're gonna tell your cloud agent I'm concerned about these things and it will go look at it based on.

**Val Levitan** 35:31  
Um.

**Aaron Bockelie** 35:51  
On your behalf and it will add its.  
Basically it's findings based on what you curated, potentially back to the pull request.  
And you're gonna allow that pull request to stand that those comments for the pull request to stand for you.  
At that point, I can look at what you wrote, which is an amplification of what your intentions were, and I can incorporate all of your stuff into my things since I have my perspective as well, and we'll come up with a synthesis of both of our perspectives on this to make sure we're doing the right thing.  
This is actually no different than if you and I were just working on this on our own, but suddenly the language barriers are completely gone because you work in Russian and do your things and whatever, and I work in English and think about my stuff. And now we're combining the two because we're just mashing together the context of both of our approaches to things.

**Anton Seregin** 37:11  
So my comments can be in Russian and we don't breaking down anything in this law.

**Val Levitan** 37:17  
Yeah.

**Aaron Bockelie** 37:27  
Yeah, whatever you want to do.

**Val Levitan** 37:30  
As a matter of fact, your comments should be in Russian because you're thinking in Russian, you're communicating in Russian, your your mother tongue is in Russian, and Claude will not understand your English. It will get confused with your English.  
So you should only speak to Claude in Russian.

**Aaron Bockelie** 38:17  
I wonder if there's some authentication context failures going on with things, which is why it's all running very slow.  
Yeah, there's something weird going on with this repo, and I wonder if there's something going on with the auth. It's hanging on every single call right now.

**Val Levitan** 39:48  
Should I ask Andre to come in?

**Aaron Bockelie** 39:51  
No, there's.  
He wouldn't know what to do.  
There is an interaction in the between GitHub, the status and the tool calls that are happening for this for the agent to run because of multifactor auth and other things. I'm suspecting there's a delay going on right now.

**Val Levitan** 40:11  
Yeah.

**Aaron Bockelie** 40:23  
For any actions I're running.  
Could just be odds broken too.  
Sorry, I'm just doing a little bit of investigation rather than actually fixing the repo right now.  
So while that's working.  
Yeah, we never got the PR to actually execute, which is interesting.  
So you can see here I've got a special thing that I have to.  
Manage my directory environment. So I've this is specific to my computer, not yours. So just give me a minute and I'm going to restart this. This should be better.  
Sorry about that.  
What's unusual is that this repo behaves differently than the other ones, so there's probably some inconsistencies in the way it's working.

**Pavel Frolov** 45:24  
Yeah.

**Aaron Bockelie** 47:05  
I'm probably going to need to not waste your guys's time any further on this right now and figure out why this repo is behaving different than the other ones for GitHub commands. It may be a permission difference and something else.

**Val Levitan** stopped transcription