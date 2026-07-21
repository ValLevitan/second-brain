**Transcript**

22 September 2025, 12:06pm

**Val Levitan** started transcription

**Aaron Bockelie** 0:15  
Can you hear me all right?

**Aaron Bockelie Incognito** 0:15  
Can you hear me out?

**Val Levitan** 0:16  
Yeah.

**Pavel Frolov** 0:17  
Yep.  
What's my name?

**Aaron Bockelie Incognito** 0:21  
So all with the.

**Aaron Bockelie** 0:22  
So teams has gone to not working at all.

**Aaron Bockelie Incognito** 0:29  
Incognito mode.

**Val Levitan** 0:35  
Your, uh, sound is strange.

**Aaron Bockelie Incognito** 0:37  
Yeah.

**Val Levitan** 0:44  
OK, Pavel, let's start with specification standards.

**Pavel Frolov** 0:51  
Yeah, actually I think we need to discuss how to write good specifications.  
I just tried to to make some some request to AI.  
And I think we can go through this list.  
To understand what is OK and probably to determine probably more optimized form because looks like it's quite big and could be a little bit difficult for our small team.  
Teams to cover all all of this and then uh, I think.

**Aaron Bockelie Incognito** 1:38  
2.

**Pavel Frolov** 1:46  
Probably try to to to discuss steps.

**Aaron Bockelie Incognito** 1:47  
Yes.

**Pavel Frolov** 1:54  
In which order and what sections should be started during the new project development?  
So the the the general general form I I assume that probably looks pretty pretty good.  
Um.  
So if you take a look on.  
Table of contents.

**Aaron Bockelie Incognito** 2:36  
How do you feel about this being useful?

**Pavel Frolov** 2:41  
It usable, it usable, but we need to understand that some of this topics in most of project could could be.  
Feel not very good. I mean not very good quite in short terms only.  
And of course it's it applicable for big project if we want to write specification just for some module.  
It should be something smaller.

**Aaron Bockelie Incognito** 3:31  
So.  
The goal of writing specifications is essentially a way to have a structured way to inform everybody about how something's going to work, right?

**Pavel Frolov** 3:45  
Yes.

**Aaron Bockelie Incognito** 3:48  
How are you?  
Given the tools that you have and the size of your team and the capabilities of people currently to potentially pivot into this, what do you feel are probably the first sort of products that you would want to work on to define the spec for?

**Pavel Frolov** 4:10  
2.  
Oh, actually right now we are starting development of Flex POS.

**Aaron Bockelie Incognito** 4:20  
Mhm.

**Pavel Frolov** 4:21  
And I think it's.  
It can be written, it can be started to write specification for this project or probably as part of this project we are going to develop.  
Uh Flex Payment Uh Cloud Payment Hub.  
That is.

**Val Levitan** 4:47  
I don't know if it's the right thing to do.  
Maybe it is logically, maybe it is, but uh, I have enormous amount of.  
Things that is riding contingent on Omni framework enormous. I mean our entire company's success is riding on Omni framework and I need it properly documented.  
And specification written and I need tests.  
Designed for Omni because all other developments will be riding on Omni.  
So I'm I'm not saying that logically it's incorrect to start with, let's say POS, because indeed we're making it now, and maybe we should also do it to some degree, and Omni POS might be the right thing.

**Aaron Bockelie Incognito** 5:34  
So I think.

**Val Levitan** 5:52  
Because it's quite isolated and we can put Nathan.  
On that job and he can probably do a decent job.  
But JVL's focus should be on reversing only design into a specification.  
This is what I would like to see because without this I don't know how to move forward like I'm I'm stuck. I don't know what to do next and we have a bunch of games that need to be designed. Those games need to be tested and if we don't have specification and we don't have.

**Aaron Bockelie Incognito** 6:18  
Mhm.

**Val Levitan** 6:33  
Uh, test for QA. There is nothing we can do. We will not surely.  
Descend into the old way of doing things and running QA after things are done and I won't be able to move to the new stage of.  
Development habits or development attitude.

**Pavel Frolov** 7:04  
Mhm.

**Val Levitan** 7:04  
So that's all I'm saying. I'm not, I'm not challenging that logically my you you might not be correct. You are obviously what you're saying makes sense. I'm just saying that unfortunately we are where we are. We're still trying to catch up.  
On things that we started.  
You know, years back.

**Aaron Bockelie Incognito** 7:26  
So something that I'm reading in that generated spec doc template is that it's got a lot of formalities in it.

**Pavel Frolov** 7:26  
Mhm.

**Aaron Bockelie Incognito** 7:37  
Everything from numbered headings to lists to all sorts of things in there, and I respect the idea that it promotes things like structure like that. The problem is, is that.  
All of that structure is gonna get in the way of thinking and defining just what actually the spec is for things.  
You can always go back and put it into numbered headings and do all this and the other thing so.  
What I think that.  
The first sort of pass for specification here really isn't about. It's not trying to.  
Emulate or take on some sort of formal appearance of of of a specification. I think your first literal pass for this is to try to describe in sections or in small pieces.

**Val Levitan** 8:20  
OK.

**Aaron Bockelie Incognito** 8:34  
Sort of what you're expecting this thing to do from a capability perspective, because you're kind of reverse engineering a little bit.  
Already got things like so if you're talking about flex or the flex payment system that you're talking about.  
Then I suppose it has is still being developed and the specs can be available for that, but for especially for systems that are kind of already you're producing games for it. I I don't know how you would at this point go back and honestly write specs except for just sort of describing what was built.

**Pavel Frolov** 9:15  
Uh, actually saying saying about Omnia.

**Val Levitan** 9:17  
Sorry.

**Pavel Frolov** 9:22  
Here I think also could be two different approach. First approach just to describe Omni framework and game based on this framework.  
This all interfaces, communications, architecture and so on, but this is only a small part and it's quite difficult to.  
To do tests.

**Aaron Bockelie Incognito** 9:54  
Mhm.

**Pavel Frolov** 9:56  
Test tests for actual machine because without other modules.  
close.  
It will produce just a minor set of tests, but approach #2 try to describe software product.  
Created for EGM based on FP7 platform. In this approach we will need to describe all the components, software components, firmware components.  
Framework, local gaming server, operating system, everything. In this approach, if we try to describe testing procedures, it could be end-to-end tests in most cases.  
But definitely it will be more difficult to make description of everything.

**Aaron Bockelie Incognito** 11:10  
So.  
Part of this is, I mean how did.  
In Confluence you had the game spec for a game or the game, the game at the lines and the ways and the description of the game and all the other things. That's essentially the specification.  
In this situation, we're talking more about. Are we talking more about the code itself that games are played and built on, or are we talking about?  
Also games in when we talk about SEC, are they? Do we have two different types of specifications going on? They're not.  
They're not unrelated to each other. I'm sorry you use a double negative. They're they're related to the the framework spec and how you use it in a game spec and how it's implemented are definitely related to each other. How do you plan on making them actually stay?  
Not dead documents, but actually, you know, living justification or living connection between the two.  
Because otherwise what you're gonna end up doing is you're gonna have a lot of specs written, but no one's gonna be really writing to any doing anything according to what the spec was written.  
How do you actually define this now?  
Your eyes.

**Pavel Frolov** 12:44  
Right now.

**Aaron Bockelie Incognito** 12:45  
And the reason I'm and let me also add this, I'm asking you this.  
Because I have a particular impression in mind and I've sort of discussed it a bit, but I don't feel like I think the team's so small in the way people work that I don't really have any control or influence over.  
Your team doing things because it generally turns into just me. Just I just need to tell people what to do. And part of the problem of telling people what to do is that you can't just tell people what to do. They have to be able to actively engage and think about.  
What to do with the specification and what they would do in the case of being able to create and write things. And there's particular roles that need to be sort of thought about where you might have an engineer that's just writing code according to a spec, but if they're not.  
Really actively engaged as to why they're writing code according to the spec. That's only you only have that luxury in very large development teams where there's a lot of people to sort of pick up the slack. But since you have a very small development team, everybody has to be able to sort of.  
Both think on their own, but also contribute back to the group.

**Pavel Frolov** 14:10  
Mhm, yeah.

**Aaron Bockelie Incognito** 14:13  
So where does the culture lie?

**Pavel Frolov** 14:21  
Awesome.  
I think actually we just need.  
To have well written specification for each project for different purposes.  
We need all the knowledge including requirements.  
Uh.  
To be written in in text because right before now many pieces of software made by verbal requirements.

**Aaron Bockelie Incognito** 15:28  
OK.

**Pavel Frolov** 15:30  
It's a starting point.

**Aaron Bockelie Incognito** 15:33  
Right.

**Pavel Frolov** 15:33  
Developers during the analysis, they understand the technical requirements, but they do not write them in in written form.  
The same with the tests. Irina understands what to test, but not for for all cases. We have test cases.  
In many case they just use tribal knowledge that something needs to be tested, but why? And sequence of tests would be.

**Aaron Bockelie Incognito** 16:11  
Mhm.

**Pavel Frolov** 16:18  
Wrong and something else.  
The next point, if you have a well written specification with architecture, it can be easily analyzed.  
And new developer can easily onboard it.  
Into the project and finally, yes, we are going to to use artificial intelligence that can work, cannot work with tribal knowledge and requirements and architecture made in mines.

**Aaron Bockelie Incognito** 17:09  
So.  
Let's think about maybe the scope of trying to work on this to start with, because it's it's a lot, right? Like I'm I'm trying to imagine I'm you and I'm trying to basically.  
Get a bunch of people who hadn't been doing it this way to now do it this way and they're gonna push back and sort of, well, I don't know or you know, kind of easily fall back into the mode of of of verbal discussion and.  
Sort of creating things around that way.  
I've always felt that the most effective way to do this is to lead by example by providing the pattern and say OK, this is the pattern. I'm writing it up like this. Now I'm not going to actually tell you how it's done. I've written it down.  
And you have until this date to get it done, and I need you to ask me lots of questions. And I'm not going to play the game of if I don't hear anything from you, it must be perfect. Instead, what I'm going to do is I'm going to set up a daily conversation with you.  
To ask you how you're doing and where things are at. It's extremely labor intensive to do this because it disrupts your day entirely. You just become a manager asking somebody else what to do.  
But I think The thing is, is that it also forces the reckoning that you're trying to communicate how to do something differently.  
And in a lot of ways, it's sort of a progression of a skill. You're trying to artificially progress somebody's skill set. Let's let's assume they're very skilled. They know what to do, like they or they could do it. Their technical capability is there, but their ability to work based on.  
This unusual to them way of looking at a spec or how things are written is not familiar with them.  
I think The thing is, is that between the two of you, you have to recognize between you, like if I were Pavel, you know you and somebody who needs to consume these specs and understand what I'm writing down. I really would need to sit down with them and say, so here's the thing.  
Obviously be saying this in Russian. I could just tell you what to do right now and we could have emails and chat and teams, but I cannot. I'm going to write these specs down and I'm going to put them in a git repo and organize them.  
I may use them with write them with AI, but I'm going to do my best to put my words into there and make sure it's clear. And it may feel like at first for me, me being Pavel, that I'm literally doubling my work by nearly writing the code, but just writing a spec.  
And I have to learn. And I also need to tell you, developer, that you're gonna feel like you're doubling your work at first because you're literally reading the spec and then rewriting it again to actually write it.  
But we're both going to learn from this process to understand what is the minimum viable specification necessary to be able to get the work done without reverting to talking in the halls.  
Verbally doing this and that, shoulder tapping and so forth. This is a culture change that is going to occur and it means people aren't necessarily chit chatting about the problems and talking them over as much.  
The idea is to write down the problems that you encountered through defining the problem, writing the spec, committing the code, using git to communicate the conversation, and it is a huge.  
Feeling bad change at first because you're like basically some ******* in the United States says you need to write down everything and it's like quiet like a library as opposed to, you know, just this lively talking about things and in the over your office.  
You know, desks and and chatting over tea or whatever. And the reason that I'm demanding this.  
Is that by changing your behavior to make it so it's written down rather than verbal is that you will eventually learn the pattern of writing it down and communicating and you will return to verbal, but the verbal will return at a higher level of conversation than you had previously.  
This will be. There's a phrase called metacognition thinking about thinking.  
And what I want you to be able to do is I want you to promote thinking about thinking amongst your peers in person, because that's what people do really, really well.  
And then you can write down your thoughts in in the git repos and in the specs and everything else like that.

**Pavel Frolov** 22:11  
Oh.  
Aaron, may I ask you to repeat your last statements to last two statements? It's not. It was not so clear actually.

**Aaron Bockelie Incognito** 22:28  
Understood. So metacognition.  
The word metacognition is a or the phrase.  
Is a phrase that is described as thinking about thinking.

**Pavel Frolov** 22:42  
Mm-hmm.

**Aaron Bockelie Incognito** 22:45  
You're not. Val likes to call it philosophizing. He enjoys putting it into that category. But the reality is, is that I would rather that you are able to sit down and do productive work by reading specs.  
Responding to spec or responding to work in your team written because every bit of written communication that occurs and not in a chat tool, but in like you know an issue that you're working on or in a pull request.  
If you do it there, you have a wealth of information about what's actually being concerned, rather than trying to talk it through in the hallways or over your desks. And what happens is, is that you only have.  
And this is, this is now thinking about thinking. I'm we're literally in a metacognition conversation right now.  
When you sit down at your desks and you talk over the barrier, I don't know what your camera looks like when you're what the rest of the office looks like, but I'm assuming you're all within earshot of each other.  
And I'm assuming you have the headphones rule, which is when the headphones are on, don't talk to me, I'm busy. You probably have that rule too. I I used to have that when I was in an open office and.  
The thing is, is that you would need to shoulder tap people or otherwise chat with them and say hey, I want to discuss XY or Z.  
And it becomes a very convenient way to do things when you're all local to each other in the same office.  
The problem is, is that when you take that time to do that, you only have so much time in the day before the day is done. And So what it means is that you you this this thinking about thinking which is.  
When you're discussing the problem before you're writing code and working on it.  
This thinking about thinking causes you to not be thinking about it yourself. In that space, you're borrowing the brain of your adjacent peer and you're working on it together, which is completely OK.  
The issue is, is that talking like you and me right now? Well, me mostly, unfortunately.  
Takes up a lot more time than it should when if I were to just write this out. If I were to write up a thing about metacognition and send it to you about this, I would have thought about it on my own. I would have written it down and I would have handed it to Pavel and say.  
Need you to think about this this way. That way when you read it and I read it, we've already established this connection and so therefore our metacognition about the problem at hand is operating at a higher level because you and I already have the view and perspective on metacognition.  
When you talk about a problem in the code, implementation, spec, bugs, test, whatever. If you talk about it first, you then have to also talk about how to deal with it if you write it down first.  
People people read faster than they can speak.  
If you write it down 1st and you both communicate and it's written there and you both, you know you wrote it, the engineer read it, and then you speak about it because you still don't understand it.  
You've elevated the metacognition level of solving the problem to a higher level by doing that.  
I'm not even talking about AI yet, I'm just talking about just regular old people solving problems. This is why the pattern of sending a memo back before e-mail to writing an e-mail about things to.  
Talking about things in chat to now writing comments in in uh.  
A a branch or commit or you know some sort of pull request or change. That's why these things are valuable is because you can do that. I would encourage you to do things like look at.  
Active.  
Technical software engineering groups like open source ones because they're available and open where they discuss the various problems to be had and vote for features and things like that.  
It's not the full view, it's just what's written down. But the more effective teams are the ones that can write down more.  
And it's not about writing more to look formal or fill UA bunch of space. It's about being very articular about communicating your intentions.  
So if we think about, if we think about thinking and we look at the thing that you pasted in the chat, there's a lot of good things inside of that list, but there's also a lot of bad things about that inside of that list for JVL specifically, which is.  
The formality and the amount of different things it covers and so I want you to really.  
The the problem I have is that I don't speak Russian and I don't have time to be in the office with you guys and listen to the pattern of how everybody works. And so I have to go on a hunch and a guess about how you were operating.  
And I think the best thing I could give you for advice right now is to consider how you guys communicate verbally and talk about the problem. And and and when I say verbally, it kind of also means teams, like when you're just chatting between stuff on teams.  
That's essentially picking up the phone because it's a it's it's like stream of consciousness and it's informal and it goes away and you don't usually go back to whatever and so it becomes a crutch. And I would rather that you stick with a structure of.  
Discussion on the topics at hand.  
And that probably is actually the more focused aspect of what a spec should look like, so you can sort of avoid the initial voice conversations at first.

**Pavel Frolov** 29:16  
Um.  
Uh, actually I see the benefits of communicating via the git.  
But I still think that the fastest way to exchange minds and ideas is verbal.  
Versus writing in chat and better than writing in git. Better I mean faster.

**Aaron Bockelie Incognito** 29:42  
Yeah.  
Of course.  
But imagine it like this.  
I'm trying to think of a good analogy for this you have.  
You have a bus ticket to ride a bus to anywhere for the day. OK, you get one.  
You get one ride, but you can ride it anywhere. You can just get on that bus and it'll take you as long as you want.  
How? Where do you go? Do you just take it and ride it like a block down the road and you get off again? Because that's as far as you can walk in just a minute or two. Do you take it halfway across town? Do you ride on the bus the entire ride all the way back to the beginning again? Where is your?  
Value out of your expenditure of that effort. Because every time you have a discussion and talk, have a meeting, it's like you have a finite number of these that you can do in a day. You can only do so many.  
And it would make sense to try to plan your trip as much as you can before you use your ticket.  
Because otherwise it's it. You've kind of wasted the value of that engagement.  
And So what means is.  
Comments in GitHub and not chat because that's not recorded correctly, but discussion about the issue at hand.  
And have it recorded against the feature or the whatever you're doing the implementation with. And so and and because we're treating documents as code as well, this means you can have discussions about specifications too. You can ping pong the spec back and forth between each other and have those discussions there.  
And then when you finally sit down and go, OK, we're both in agreement, let's just talk over the last bits because it's faster. When you finally use your bus ticket, it's at a much higher level than it was before where you're kind of sitting there and collaborating. There's nothing wrong with collaborating. I want, I want to say that.  
But we have to force ourselves to to written collaborate first, formally written collaborate before we go to the high frequency informal talking collaboration.  
Because what happens is and and this is another. Here's another problem that happens all the time.  
When you do the written collaboration, very easy to make a ton of assumptions as to what somebody else is thinking or what they're want to do or what they're you just don't know. It's like you have this huge gap and it's almost like.  
By writing it down, you're sort of forced to stay in the narrow topic of what you're considering, because the channel for communication of written for written communication is so much narrower than even you and I talking on this video call. You're seeing my hands move around and I'm.  
Talking with him, trying to be Italian for a minute with my hands, you know, and you see me and I see you and I see your reaction. But imagine if we had sat down, if the direction this conversation went, because it was, it is a bit unstructured.

**Pavel Frolov** 33:11  
Mm-hmm.

**Aaron Bockelie Incognito** 33:20  
Was for me to give you a.  
Article on metacognition state and communication of developer productivity before we even got to having this talk here. You would have read that. Then you and I would have already known sort of what I was thinking already, like telepathy, right?  
I know I'm kind of restating what is obvious.  
In written communication here, but as soon as it's written down like this, it becomes available for everybody else too, not just you. And everybody else is also now machines instead of in addition to people, which is also.  
Super, super valuable.  
So that's all I'm going to say about AI right now. I'm just saying that writing it down amongst everybody else is really valuable.  
I want you just as an example.  
Because it's sort of relevant, and it's a good example. There's the Pixie JS GitHub project.  
Now, at first glance, this isn't really any different than me pointing out the.  
You know, if I if I were to point at JVL's conversations.  
In JIRA about things you might you might tell me, well Aaron, we we do this, we talk about this back and forth, but the issue is, is that when you click into these and start filtering them.  
Like I would suggest looking at uh labels for example or or maybe uh high priority items.  
For example, there's a lot of bugs in the high priority, but let's just let me see if I can find a.  
Lower priority.  
Yeah, those are all bugs.  
But uh.  
Play around with the filtering in here just to kind of look. There's a lot of feature requests and things like that. Um.  
Here's one pending triage.  
Just I just picked one at random.

**Pavel Frolov** 36:06  
Mhm.

**Aaron Bockelie Incognito** 36:08  
Hey, I've been trying to create a texture using a custom filter that I can fill with signed integer values, blah blah blah blah. Thanks for flagging. If you could provide an example, we'll take a look. Thanks. I don't know how he's doing it, but I'm gonna try to blah blah blah. Here's an example.  
So it's very straightforward what's happening here. I want a feature. Tell me how it works. We'll look into it. Oh, here you go. And this is just a very basic example of just collaborating back and forth in a written way right now.  
If you look at ull requests.  
Let me pick a pull request for you.  
Here's a pull request for adding some sort of GL 2D format.  
And you can see there's kind of some, a lot of discussion back and forth where they they, you know, bring some.  
This is just GitHub actions doing stuff, but this is where the communicating with AI is actually bringing things into the conversation. And then let's see if I can find one where there's some people here.  
One minute.  
Here is a pull request from several years ago. I'm cherry picking by highest number of comments back and forth and I want you to observe the cadence, the back and forth and the the discussion where everybody is sort of in this code review looking at the things.  
And.  
The goal here is to have that banter, that that dialogue captured in a platform tool like this, rather than verbally. You could very easily have that code review by swiveling over and asking Sasha about something.  
But if you do the code review through here.  
It's recorded and everybody else learns as well.

**Pavel Frolov** 38:51  
Mhm.

**Aaron Bockelie Incognito** 38:54  
Whereas if I look at and this is actually just been a problem with us migrating through git, you know from sort of Jira to GitHub and moving some stuff around is that.  
It was difficult for this to sort of discussion to exist and now that we're sort of consolidating on GitHub and potentially more than just, you know, commits by writing issues down and tracking a lot of that other stuff.  
This is this is where that spec comes into into play really, really strongly. Writing the specification according to what you want it to be makes it so when you discuss a pull request or you discuss an issue, you can both go back to the spec.  
And think about, well, what did we want to do? And then you might go, Oh no, the spec is incomplete or needs to be changed. And the other thing you can do is you can start looking at what's actually the important part of the spec.  
There's all these tables and all these.  
Project phases and things and stuff inside of a spec. It's like that's a project management spec and I don't think it's. I think you want you you guys are gonna stick with technical specs to start with.

**Pavel Frolov** 40:18  
Yeah.

**Aaron Bockelie Incognito** 40:21  
Because that's what you guys are. You're technical. You're not roject managers.  
Imagine if, yeah, go ahead.

**Pavel Frolov** 40:32  
It should.  
Actually I do not understand right now how well written communication in git will help us to write a specification actually.

**Aaron Bockelie Incognito** 40:51  
O.

**Pavel Frolov** 40:53  
Even if I take all the communication and pass it through the AI.

**Aaron Bockelie Incognito** 40:54  
Let's let's.

**Pavel Frolov** 41:03  
Probably it will help to describe some some issues.

**Aaron Bockelie Incognito** 41:12  
AI tools are an amlifier for what you'd want to do. If you don't know what you're doing, you'll just amlify your incompetence.  
So let's let's play for a minute. I'm going to talk about something that I sort of know how to write, OK?

**Pavel Frolov** 41:33  
Yes.

**Aaron Bockelie Incognito** 41:33  
I want to make an MC server for Microsoft Office secifically for Outlook OK.  
O.  
I want to involve you, Pavel.  
I want you to do the coding for me and I'm going to define what works.  
Do you and I sit down and discuss it first, or do I write down how I want it to work?

**Pavel Frolov** 41:58  
You know this partic.

**Aaron Bockelie Incognito** 42:00  
How do we do it in your office right now?

**Pavel Frolov** 42:04  
Right now we're starting from, yeah, we're starting from some general meeting.

**Aaron Bockelie Incognito** 42:07  
Yeah, if I if I could teleport.  
OK.

**Pavel Frolov** 42:19  
Highly likely in my room on one near the around the table.

**Aaron Bockelie Incognito** 42:23  
Yep.

**Pavel Frolov** 42:28  
And uh.  
I describe what the business needs, what the project is, what what technology it involves into the project, who will be highly likely participate in this project.

**Aaron Bockelie Incognito** 42:38  
Mhm.  
Yes.  
Right.

**Pavel Frolov** 42:48  
How it relates to different components or projects and so on. This is the first first approach.

**Aaron Bockelie Incognito** 42:56  
And you would tell me these things, right? OK, so I think the only thing that you have to change is just write it down instead of tell me and that's your specification.

**Pavel Frolov** 42:59  
Yes.  
The the benefit of verbal communication, it will immediately return your question asked by all the parties. It will be.

**Aaron Bockelie Incognito** 43:21  
Right.

**Pavel Frolov** 43:22  
It will require probably several days.  
To to ask questions written in in GitHub or any other tool and answer this question.

**Aaron Bockelie Incognito** 43:40  
This this is also true, but this is also what happens when you're just initially doing this. O let's let's play this out for justice a minute.

**Pavel Frolov** 43:42  
8.  
Mhm.

**Aaron Bockelie Incognito** 43:52  
I want to switch roles because I know about MCP servers and I know the business justification as to why. And I'm going to tell you because I want your engineering team to write the MCP server. OK, and the reason I'm doing it is because.  
There are techniques to writing it that you don't know about, but when you start doing it, you go, oh, this is duh. I've done this like 100 times in code in the past, you know, make a state machine.  
Make a scored state machine, make a Petri net, make a colored Petri. There's all sorts of things, right? That's from the technical implementations. And then the business justification. The other things are also important too. But realistically, I don't care whether the developers know what the business justification is. They can use it as a reference so they can have empathy.  
As to why we're doing it so they build it right, but that's wasted time. So what I would do is I would create the document myself to start with, I would describe it to myself and I would be.  
Thinking about the people who will be reading this O you and maybe some other one other other engineer.  
And I would be trying to write it in a way that would educate you both when to read beforehand now by me writing this.  
I fully expect that you will actually read it actively. This is not just a decoration to put a stick on the wall and say I wrote this. This is I this me putting the time into writing the spec and the definition of the problem and the other things.  
Also is an expectation that the people who will be reading it will actually read it, because if I come to that when we do eventually meet up in person to talk about it.  
If nobody's read it, I'm gonna cancel the meeting. I'm gonna. No, you you guys didn't read it. Go back and read it and we'll try again next week.  
That's the expectation I I have for this type of stuff.  
Because what's happened is, is that the culture is supposed to be one in which you're proactive about things. You're thinking ahead before you've even started it. And if you come to a meeting reacting to some sort of conversation, nobody's gotten ahead or saved any time.  
And so it's just like it's like a ratchet, right? Like you kind of like stairs or something. The idea is, is that I start the ratchet by writing a specification document about my intentions of what it's supposed to be.  
The people who are going to be working with me will read it and they'll step up their part of the ratchet and get it up there. And then I'm gonna say, did you read it? And they're gonna go, yeah. And then I'm gonna go, OK, let's have a meeting about what's what you think.  
And then you have a meeting now about what the what the reactions were and then I collect that and revise the document. Now that's sort of like a one step spec to meeting to to execution.  
Now a more mature model is this. I write my specification. I request that the other people who are going to be working on it read it. They add comments to that content and I read those comments and they have to actually engage their brain.  
And really write real comments inside of the document. And then I read all those comments and I react to them and I either dismiss them as you didn't know, you didn't understand and this is an opportunity to teach.  
And mentioned to this in a comment, it is a Oh no, I've totally missed that piece. Let me reintegrate this and so I go and rewrite part of the document and I say this was excellent so and so here I've changed this. Tell me what you think now.  
Or perhaps it's just sort of a technical, like a spelling error or some sort of structure thing, and you just fix those and move on. And then you can present another version of this draft, not in person, but as OK guys, I've written it again.  
We're not trying to beat this to death, but here's the second revision of it. Are we in agreement now?  
And then if everybody sort of says, yeah, you addressed the things, now what? Then you can say I'm going to break this down into work so we can start functioning on it. And what happened is, is you never had a meeting, not in person.  
You sort of lived through the specification instead.  
This means that when you do eventually meet up in person and talk about it, all three people have in their head an agreement, a negotiated agreement about what actually is supposed to happen here.  
And any misunderstanding can then be brought out there because it's not that you're negotiating the base problem anymore. You're negotiating, you're you're teaching against what everybody agreed to in the document instead. And the reality is, is it doesn't always, it's not always that clean.  
There's usually some other thing that comes U and you make another revision to the document or whatever.  
But the point is, is to try to reduce the number of meetings you possibly can at all times.  
This asynchronous communication model. Everybody's heard of it, probably at this point, but by rallying around an artifact like a specification or something of that nature is is really helpful to have.  
I currently have a problem at the consulting company I work for, C Prime, in which I write all the specs I want and nobody ever reads them.  
So you know what happens when nobody ever reads them?  
I just let my AI engineers read them for me and I end up writing the code myself and then they're asking me what they can do for work. And I said, well, you didn't ever read any of the specs or even communicate or even talk to me about why you didn't read it. And so I moved on without you.  
And it's not a scalable thing in a lot of ways, and it feels really bad.

**Pavel Frolov** 50:29  
Hmm.

**Aaron Bockelie Incognito** 50:29  
And so The thing is, is that you have to your advantage is that you have people in your office with you. And so instead of reverting back to, well, let's talk about it, you instead say, come on, you got to go read it. Let's just come back to me after lunch. We'll have some coffee or something and tell me you read it. I don't know, something like that.  
And so there's a there's definitely a a culture change to have to do this because I do have people that read the specs and those are the ones that who are working for me that are very highly productive and they're humans, they're not a I people obviously.

**Pavel Frolov** 50:47  
So.

**Aaron Bockelie Incognito** 51:03  
You know, I I write the spec out and they go, is this what you meant? And I go absolutely 100% or oh, you missed this part. This. It's supposed to do it like this. Oh, shoot, I didn't understand. OK, we'll we'll meet back at the end of the week and we move on from there.  
So it's just a different culture.

**Pavel Frolov** 51:20  
Yeah.  
OK, I see your point. Actually, Aaron, just to inform you, we agreed here to make an experiment to pass reverse engineering.  
Of our Omni platform, trying to make everyday meetings with Alexander Beratka, a different person will do this. We'll ask a question related to different aspects of framework.  
Record all those meetings and try to describe these aspects, different documents and then try to join all the knowledge.

**Aaron Bockelie Incognito** 52:08  
Mhm.

**Pavel Frolov** 52:15  
Into one specification document and try to analyze, yeah.

**Aaron Bockelie Incognito** 52:19  
Then this is A and this is like a one time thing, right? Like you're not gonna do this this way for a long time.

**Pavel Frolov** 52:23  
Yes.  
Yes, yes, this is just an experiment to understand if it's good enough to get.  
To get this information.

**Aaron Bockelie Incognito** 52:40  
Mhm.

**Pavel Frolov** 52:40  
And reuse it in future because as Val said, Omni is our nearest future for land based machines.

**Aaron Bockelie Incognito** 52:51  
Yeah.

**Pavel Frolov** 52:53  
So definitely we will need to refer to this work in the future, but of course I think we will switch our development process to have specification.  
In future for different components, at least when we will develop something something new, we will try to describe this first.

**Aaron Bockelie Incognito** 53:18  
Right.  
Do you do you work on cars or anything like that? Like like as a hobby?

**Pavel Frolov** 53:32  
Just.  
Uh, work on.

**Aaron Bockelie Incognito** 53:36  
Cars or machinery, things like that.

**Val Levitan** 53:42  
He he built, he built interior.

**Pavel Frolov** 53:42  
Um.  
Not only I would say I I work on everything around me my by my hands.

**Val Levitan** 53:49  
Home interior.

**Aaron Bockelie Incognito** 53:50  
What?  
OK.  
So, so the things that you do hands on and the things that you have to fix hands on.  
Think about, think about the situation where you're in a kitchen and you want to remodel a kitchen. OK, in a house, you have no access to the plans. You have no access to the person that created it because it was 20 years ago.  
It's just sitting there as it is right now.  
The very first thing you do when you're trying. Oh yeah, exactly. Just like that. I know how that feels. So the very first thing you do is you try to adapt to whatever it is, whatever mess you've been handed or inherited, right? This is my space.  
The plumbing comes out here, the electrical is here and I can't change it away unless I really want to. And So what you typically do is you create an as built. An as built is a phrase as built.  
Means that you're describing it as it is currently built, and you don't have to go into a ton of detail about something you're going to tear out, but everything you're planning on leaving behind becomes part of the as-built diagram or architecture or.  
You know, layout and then you add your new stuff. So all of your cabinets that you've got there potentially work around a light switch or plumbing fixture or or something in that and then you create more from there and then later in the future you've held on to your design because you've built it according to your design.  
And essentially this is what you're now probably doing in some ways with relation to to the code for Omni framework now because someone like Sasha.

**Pavel Frolov** 55:45  
One second.

**Aaron Bockelie Incognito** 55:53  
The.

**Val Levitan** 56:03  
Let let let Irina, let Irina have this meeting by herself. She's capable of having this meeting by herself.

**Pavel Frolov** 56:12  
Mhm.  
Mhm.

**Aaron Bockelie Incognito** 56:17  
Um.

**Pavel Frolov** 56:17  
She.

**Aaron Bockelie Incognito** 56:18  
When you when you go look at what Sash has built, he didn't just randomly build stuff. He is an artisan. He is a Craftsman 20 years ago that built the kitchen and built it according to how he thought was best to work, and it was functional and did exactly what it was supposed to do.  
But he's not there now, technically, and you now have to only rely on the works of Sasha to be able to understand what he was thinking. And you have to get into his brain and think about why did they put the sink here? Why is this counter?  
Like this you have to kind of and and you may not know. Now you have the benefit of access to Sasha. So it's like going back into time and finding that builder who built that kitchen 20 years ago and ask them a million questions. Well, why did you do this? And why did you do that? And why did you do this other thing? And they can explain it to you.  
But this is playing catch up. If Sasha had said here are the plans, this is the what I needed to build for, this is what I needed to accommodate for, and This is why I had to build all these things this way. We'll read those first and then ask questions.  
It's the exact same pattern that I'm talking about of writing this back first. This meta cognition of it becomes the same way. And So what it means then is, is that if you could review all of the intentions of Sasha as they were written down before he started the work.  
When it did come time to talk to this builder.  
The conversation you have, every word you say has a much higher value in it because you've already been thinking about it in the way that they thought about it.  
So when you start doing this one time thing with Sasha and the Omni framework and you know asking him questions.  
What you might try doing before you do that part, the meeting we recorded and everything else like that, is to have him try to write out by separated by concerns what he.  
Why he wrote the code the way he did. And if you came to that then meeting after after reading that and thinking about it and poking through it, you will have a lot more value in the questions you ask at that point. And it's the combination of what he's written down and what's recorded in the.  
the conversation, which now revises everything and makes it more valuable again.

**Pavel Frolov** 58:56  
Mm-hmm. Yeah.

**Aaron Bockelie Incognito** 58:57  
And then once you do that, then what you do is you tell people, OK, no more making stuff before you've written down what you want to make. Write it down first. Bring us into the thing. Take little shave off little pieces of what we want to do at once and make sure we've written it down and there's a spec.  
And things like that. And then suddenly that playing catch up game of having to ask 100 questions about things goes away. It just disappears entirely.

**Val Levitan** 59:27  
Yeah.

**Aaron Bockelie Incognito** 59:27  
So when you have a.  
Now when you build the house, the blueprints and the plans and the design and the architecture portfolio that came with it are all with the house. And when you open the book and you go, oh, they built it for this reason and they did this and here's the layout and all the other things. And so when you go do a remodel with all these plans.  
Of previous it's so much easier to get the work done to make changes.

**Pavel Frolov** 59:58  
Yeah, definitely.

**Aaron Bockelie Incognito** 1:00:03  
And then you edit those plans, republish new version of them as you know you made a change to the purpose of the architecture essentially.

**Pavel Frolov** 1:00:18  
Mm.

**Aaron Bockelie Incognito** 1:01:32  
Just do.  
Keep it interesting and fun.  
Yeah, one second here.

**Pavel Frolov** 1:01:48  
So highly likely, I think we will continue to collect information from Sasha to get specification for Omni framework and Omni game.  
Game.  
And then try to make it wider.  
I mean to to add communication description with different modules, describe LGS module and then.  
Try to to go to the right, to the left and make more and more widely explained architecture for full machine software.

**Aaron Bockelie Incognito** 1:02:50  
So one thing that you might think about is.  
Uh.  
Hang on, no.  
OK.  
Consider.  
Consider this structure.  
When you're talking with Sasha.  
And.  
Do it by concern. So when, when, if there's some module or something that hits, it's built inside of Omni framework, say it's a communication thing or it's a.  
I don't know, maybe it's a maybe it's a resource bus or it's a type injector or it's.  
Some other aspect of the code that works.  
Basically, take a more. Take a structured approach to asking why it exists. Why? Why is this here?  
Why? What is it? You know? Who is it for? When did it get implemented?  
Where is it actually use that and so forth? What is its purpose?

**Pavel Frolov** 1:04:05  
Yeah.

**Aaron Bockelie Incognito** 1:04:09  
This, this becomes the proto, the the proto specification, the spec before the spec, because you're asking these questions and you're saying, well, let's just answer these.

**Pavel Frolov** 1:04:17  
Mhm.  
Right.

**Aaron Bockelie Incognito** 1:04:23  
And then you can go. This piece of code does these things and This is why.  
And especially when you have a situation where it's a lot of it's inside of somebody's head.  
They can start to kinda use this common structure across all the different pieces and answer them. It's almost like an audit. It's like you're auditing the code.  
And when you write the audit, you don't try to make conclusions about what you're auditing. Instead, you just go through the the procedure, the audit rocedure.  
When you've gone through the audit procedure and you've tried to cover every bit of things you observe with a common process, now you can create a whole bunch of conclusions, observations, analysis.  
Connections and whatever to this.  
So for instance, you could then look at all of the code and you can go, who is this for? And the answer will be probably very different every time you ask things. Or there might be some some that are same, or you might have some clusters, or maybe it's all for one person, we don't know. But the point is, is that when you ask specifically across.  
All the code base. Who is this for? You can gain a very interesting insight into your customer, for example.  
If you ask a question, why is this code here across a read all the whys across all the code, you'll get a whole bunch of answers about why this exists and what's valuable, and those essentially become your requirements.  
If you ask when it was created, you suddenly have an understanding of the order of implementation in the building process of thinking about it. You see how you can use this. It's like you're building a multi dimensional database.  
Just on the 5 W 1H pattern.

**Pavel Frolov** 1:06:27  
Mm-hmm.  
OK, any any suggestions? How can I proceed?  
This specification for only.

**Aaron Bockelie Incognito** 1:07:16  
So my my suggestion would be is to look at the code base for Omni, ask Sasha to start adding essentially a written description based on some sort of.

**Pavel Frolov** 1:07:28  
Yes.

**Aaron Bockelie Incognito** 1:07:30  
Why is this here? What does it do? When did you implement it? Who is it for?  
Give him a little bit more than just a single sentence and try not to make it a bureaucracy form that he has to fill out either.  
He needs to be able to sort of type freely about what he thinks it is. Don't try to force him to conform to some document of perfection. I would rather you have a giant paragraph with a bunch of sentences and barely any formatting and misspelled stuff, but at least he got the idea down.  
And typed it all out and saved in there. Then some sort of perfect looking thing already filtered through AI and all of the information that he then wrote lost. Don't do that.

**Pavel Frolov** 1:08:19  
Actually I think approach with a second person looks better for me because Alex he like to to learn somebody.  
In this, in this approach, he he to to to to teach here. Yeah, correct.

**Aaron Bockelie Incognito** 1:08:35  
OK.

**Val Levitan** 1:08:36  
To teach, to teach, to teach.  
He's AI agree. Alex is a natural lecturer. He he likes to.

**Aaron Bockelie Incognito** 1:08:46  
OK.

**Val Levitan** 1:08:50  
Well, it doesn't sound right. He'll he likes to.

**Aaron Bockelie Incognito** 1:08:56  
He likes to inform.

**Val Levitan** 1:08:57  
Hmm.

**Aaron Bockelie Incognito** 1:08:59  
He likes to inform people.

**Val Levitan** 1:09:03  
He's very forward individual. He doesn't have, he doesn't hide anything. He's very transparent and he wants to transfer knowledge. He is extremely proud of his work.  
And he wants this knowledge to be, um, transparent.

**Aaron Bockelie Incognito** 1:09:25  
OK.

**Val Levitan** 1:09:25  
He doesn't. He never hides anything back. Like he doesn't hold anything. He's very, very sure of his own worth. He knows his own worth.

**Aaron Bockelie Incognito** 1:09:31  
So.  
Mhm.

**Val Levitan** 1:09:40  
And he's very happy to transfer knowledge, and when you have a second person in front of him, it all surfaces much easier.

**Pavel Frolov** 1:09:51  
Sure.  
But I I think it will be quite difficult to force Alex to make it in written form actually.

**Val Levitan** 1:10:00  
I agree. I agree.

**Pavel Frolov** 1:10:05  
He hates to write many words.

**Val Levitan** 1:10:10  
But he will talk about it. And if if this meeting is recorded, if this meeting is recorded, that's the essence. You will capture everything.

**Aaron Bockelie Incognito** 1:10:11  
OK.

**Pavel Frolov** 1:10:13  
Yes.

**Aaron Bockelie Incognito** 1:10:17  
So then I suggest I suggest we do this with them. I put a link in there called Rubber duck debugging.  
It sounds funny, but it's true.  
And the intention of this, it's a known thing, is you have a friend that sits on your desk that's inanimate. Now we don't have to do that exactly the same. I'll explain how I think you can do it here with Sasha. And the idea is that the developer sort of speaks.  
To an inanimate object and tries to describe exactly what's going on to that. And the very act of speaking out loud causes that often causes the engineer or the developer to have additional insights as to what the heck they're doing or what's wrong.  
So in this case, what we can do is the second person who will be Sasha's rubber duck will essentially be their their job is to make sure that it's recorded to pick and identify a piece of the code for Sasha to explain to them.  
Sasha explains to the rubber duck. The person listening does not have to entirely fully understand it. They just need to listen and ask some questions.  
So they need to be a little bit technical to be able to at least kind of ask some insights. Sasha needs to understand that he's not going to teach this person how to actually understand it all in that space, and both of them need to understand to stop the recording once you get out of that space.  
And finish it. Take the transcript, turn it to text, save it with the code. Don't rocess it through AI, just keep it in there.

**Pavel Frolov** 1:12:04  
Mhm.

**Aaron Bockelie Incognito** 1:12:08  
If you process this with AI, you will definitely ruin the value of whatever Sasha said.  
You can then review what Sasha said a whole bunch of times after. With all these transcripts in there, you could make a.  
I don't know another docs tree or a transcripts tree or something that kind of mirrors the actual code base tree, for example, and you plan this out ahead of time. Don't just do it ad hoc. I want you to color out the actual file structure.  
The directory structure, where you're gonna have the conversations against the code to make sure it's all covered. You can explain this to Sasha that this is how we're going to do it and he's gonna go. Aaron told you to do this, didn't he? Is what he's gonna say, probably. And then what's gonna happen after that is you can then know how exactly how.  
Meetings you have to have to be able to cover all the code base. You're going to commit all this back into it, and you're going to literally have the word of Sasha across several hours worth of conversations in here describing the code base.

**Val Levitan** 1:13:14  
Look, I'm we we have we we have a working formula. I'm not quite sure why we're trying to reinvent the wheel. We know that Sasha is a good verbal communicator, so we have approximately 5 individuals that need to speak to him.

**Pavel Frolov** 1:13:24  
Yes.

**Aaron Bockelie Incognito** 1:13:33  
OK.

**Val Levitan** 1:13:33  
So the only the only suggestion here I'm I'm hearing that do not convert the recording into with an AI, leave it in the raw format. I don't. I don't understand the reason.

**Aaron Bockelie Incognito** 1:13:46  
Yeah.

**Val Levitan** 1:13:50  
Because to me it doesn't read well, but if you say so, you must have a reason for it. So let's leave it in the raw format, and I assume you want to put it in GitHub. So you probably want to keep it in the form of a raw transcript without any conversion.

**Aaron Bockelie Incognito** 1:14:02  
Yes.  
Right, 'cause what we don't want to have happen.  
Now, if we do a conversion of the transcript, if it's simply capitalizing and moving sentences around and making paragraphs, but it is exactly the same word Sasha says, I'm OK with that. But if it does any interpretation.  
Or understanding of what Sasha wrote. We can't do that.

**Val Levitan** 1:14:35  
But that's fine. I mean, we can specifically prompt an AI by saying do not change the meaning, do not substitute any words, just properly format for convenience of of a reader.

**Aaron Bockelie Incognito** 1:14:37  
Yeah.  
I'm just saying be careful doing that because even if you tell it to do that sometimes it it breaks and and I think it would rather have you have the original raw form as much as you can and then you can go back and.  
Kind of double check it because it's a git repo. You just change it later if you want to. You can go back to the original revision. If you do that against it before you've ever checked it in, you may lose something. This is extremely important to get right.

**Val Levitan** 1:15:19  
OK, so the the the point that I'm carrying out of this conversation is that we will.  
Yeah.  
Uh, have Sasha.  
Lecture or verbalize through code with five specific individuals in the company, and each of them, each five of them really will ask their own customized set of questions based on the on their own set of expertise.  
And their own application for Omni.  
So through the interviewing of with five people, we will really get quite a bit of documentation. So my suggestion was schedule five different days in order not to wear him out.  
But allocate a week, allocate 2 hours per.  
Discussion. If it lasts 3 hours, fine, but as long as Sasha can talk and verbalize, but you know, just allocate couple of hours per day so he's not overburdened with it and put in front of him one of those five per day.  
In a week, you're going to have an incredible amount of knowledge.  
Transferred onto a different medium now. So now you have raw transcript without any intervention of an AI.  
What's the next step? I'm trying to understand the next step.

**Aaron Bockelie Incognito** 1:17:00  
So once we have this, we need to be able to. I'm expecting to see like a tree of all these conversations by all the concerns in the code base.  
And the tree of directories that are in the code base now with all of these raw transcripts from Sasha describing things broken up by concern means that we can take, and this is where we have to kind of make sure he covers the interviewer interviewing Sasha.  
Needs to have made sure that you went through the five WS The Who, what, where, when, why, how, for example.

**Val Levitan** 1:17:35  
Yeah, he has to. Each interviewer has to not just listen, but get squeeze information out of them. Why? Why? Why? Why?

**Aaron Bockelie Incognito** 1:17:44  
Actively address it.  
Yeah, all the others, all the WS.  
Once you have those written down, you can look at each of these concerns and you can then pair that with the code he talked about and you can ask that question and extract that question from the original text. And this is where A I comes in really helpful.  
You're not trying to literally translate it into just another structured format. You can instead say look at the code here. Look at what Sasha told me the code does here. Let's write a specification based on what we found between these two things.

**Val Levitan** 1:18:27  
So who do we delegate this task to? I suggest delegating it to the interviewer.

**Aaron Bockelie Incognito** 1:18:37  
I don't think the interviewer is necessarily the person that's going to synthesize the requirements out of or the specification out of this. I think the interviewer.

**Val Levitan** 1:18:44  
Well, who do you think should be?

**Aaron Bockelie Incognito** 1:18:48  
But.  
I was gonna say the the interviewer should be just making sure Sasha stays.  
In the in the area of concern on the code and that he makes the the interviewer make sure that Sasha addresses the five WS in the in the conversation here. They're like a a news reporter almost. They're kind of sitting there trying to get facts about things and this.  
Help Sasha stay comfortable with with having the conversation.

**Val Levitan** 1:19:20  
But I'm now at the second stage, so we've collected all of this. Who, who, who is the best person to synthesize this information into a an initial spec?

**Aaron Bockelie Incognito** 1:19:32  
Who is the product owner for Omni now?

**Val Levitan** 1:19:38  
We don't have one.

**Aaron Bockelie Incognito** 1:19:41  
So.  
Typically this treasure trove would be given to the product owner to make sure they understand how the spec is created and written.

**Val Levitan** 1:19:54  
We we don't have a product on it. We we need to find a solution how to improvise this.

**Aaron Bockelie Incognito** 1:19:59  
Who is going?  
OK, so like Nathan might be that person, but not really.

**Val Levitan** 1:20:08  
No, Nathan will no.

**Aaron Bockelie Incognito** 1:20:11  
Uh.  
Who's the person who is who cares about the performance of Omni functioning for the company to be able to create games?  
Eventually there has to be somebody who says.

**Val Levitan** 1:20:31  
I can, I I can suggest of putting, let's say, Lena Cima handoff.

**Aaron Bockelie Incognito** 1:20:31  
As.

**Val Levitan** 1:20:39  
Uh, one.

**Aaron Bockelie Incognito** 1:20:42  
Mhm.

**Val Levitan** 1:20:44  
Irina and Pyle.  
As a single product owner. So I I feel that I feel that a coalition of these people with further interviewing Pavel, sorry, not pavel. Sasha probably could.

**Aaron Bockelie Incognito** 1:20:50  
A working group.

**Val Levitan** 1:21:04  
Squeeze more.  
Details.

**Aaron Bockelie Incognito** 1:21:08  
OK, so if we take that approach, we need to make sure that everybody in the working group understands the rules for the working group, which is here's the treasure trove of information. Here are the techniques to get the specs out of things.  
And we always do written communication first before we do verbal and so forth, just like we talked about here. So Sasha or Pavel Pasha, I think you then become sort of the leader of the group because you and I are talking about this kind of concept right now and you can re-explain this to them.

**Pavel Frolov** 1:21:44  
Mhm.

**Aaron Bockelie Incognito** 1:21:45  
And you can throw a.

**Val Levitan** 1:21:47  
You said you said the rules of engagement. You explain the game. So you you you present it as a game. You say here's the rules of the game. This is how we play it and you mediate this.

**Aaron Bockelie Incognito** 1:21:51  
Right.

**Val Levitan** 1:22:02  
Don't participate, but rather mediate.

**Aaron Bockelie Incognito** 1:22:02  
Yeah.  
You go, OK, you need to write that down. Hey, where is the pull request? Hey, where is the spec at? How did you even come up with this idea? Like if they come up to you and start talking about something, you can go, where is it written down?

**Val Levitan** 1:22:21  
Yeah, this is. This is not a part of the game that worries it.

**Aaron Bockelie Incognito** 1:22:24  
Yeah, this you didn't play the game.

**Pavel Frolov** 1:22:27  
Mhm.  
Yeah, here.

**Aaron Bockelie Incognito** 1:22:34  
It's not a bureau. You're not playing the bureaucracy game. You're playing the intelligence, the the courtesy of Intel of intelligence game.

**Val Levitan** 1:22:47  
I think this will work. I think this will work.

**Aaron Bockelie Incognito** 1:22:48  
'Cause otherwise, yeah.

**Pavel Frolov** 1:22:48  
Yeah.

**Aaron Bockelie Incognito** 1:22:55  
And if done right, so here's the challenge that you've got in front of you with having a working group. And there's actually a flip side to this too, which is good. The challenge is that you have four or five other people that now have to adopt this world view that you have to kind of.  
You know, they all want to do things in a different way, and so you're forcing them to sort of do this way and it's much harder. The benefit is, is that if you can get them to do this, you have that many more advocates inside of your company, inside of your group to now also push the same way of working.

**Pavel Frolov** 1:23:31  
Yeah.

**Val Levitan** 1:23:31  
Yeah, because they signed on to the process. Of course, they become active participants.

**Aaron Bockelie Incognito** 1:23:35  
Right. And they're basically promoting this against all the people they rub shoulders with all the time.

**Pavel Frolov** 1:23:44  
Yeah.

**Aaron Bockelie Incognito** 1:23:46  
Politics. It's really what it is comes down to.

**Val Levitan** 1:23:49  
OK, so now we understand how. Let's develop a schedule.

**Aaron Bockelie Incognito** 1:23:59  
So I think the way that.

**Val Levitan** 1:23:59  
So you need to go through, you need to go through the first round of interviewing individuals, 5 individuals.  
You need to schedule this out.

**Pavel Frolov** 1:24:12  
Yeah, actually we already.

**Val Levitan** 1:24:13  
And then advance.  
OK, so now then if if you have that schedule then schedule then the next set.  
I suggest not to have one.  
There's, uh, very little use, but.  
It will convert the conversation from Russian into English, and that will be hugely detrimental because we're gonna lose the eloquency of the expression.  
And we want to keep this eloquent language. Everybody speaks fluent Russian and you want to keep it in the mother tongue language.  
And one is going to shift the meeting into awkwardness.

**Pavel Frolov** 1:24:59  
Mhm.

**Val Levitan** 1:25:06  
So I'm changing my mind on one. It's not going to be useful. It's going to be detrimental.

**Pavel Frolov** 1:25:15  
Yeah, OK.  
OK, this week we will make meetings with Sasha and different developers.  
Uh, to capture.  
His explanation of different modules, API code ways.  
And then I think.  
Take all this.  
Transcript documents and try based on this transcription to prepare specification.

**Val Levitan** 1:26:18  
This could actually turn out to be a revolutionary thing for us.

**Aaron Bockelie Incognito** 1:26:25  
The one one thing.

**Val Levitan** 1:26:25  
I think we're done with all.  
Go ahead.

**Aaron Bockelie Incognito** 1:26:28  
I would like to make sure that we do here is.  
Um.  
Omni's kind of the first one we're trying this with. There's probably other things we can do this with as well to some varying degree, because Omni's been written relatively recently, like within the last shorter period of time, it's easier to do this. The CMS systems and the other things that are old.  
Are probably really hard to do this with because it's just it's been too long. Um.

**Val Levitan** 1:27:00  
I wouldn't do. I wouldn't do CMS. I wouldn't do it.

**Aaron Bockelie Incognito** 1:27:02  
Right, right. I'm kind of giving you an example of where it doesn't. This process doesn't work and in all approaches of this work, this should be a one time thing. It's like we're doing this one time and from this point forward.

**Val Levitan** 1:27:13  
Yes.

**Aaron Bockelie Incognito** 1:27:17  
Let's write the spec first. Like let's let's have that conversation with Sasha before we've written any code. Put that in there first.

**Val Levitan** 1:27:24  
But this is exactly, this is exactly where we're going. This is exactly what we want to do.

**Aaron Bockelie Incognito** 1:27:28  
Yeah.  
Yeah.  
Because what's going to happen here? This is the kind of neat part with the machine learning stuff. If you start adding these bits and stuff in here, you can ask a system to consider the other aspects of the system and combine all the bits together.

**Pavel Frolov** 1:27:32  
Yes.

**Aaron Bockelie Incognito** 1:27:49  
And make sure that we're on track and that we're writing code. And it's not going to be perfect. It's not going to just magically write code, but it's going to accelerate everybody's ability to create something because you've got the supporting metacognition thinking about thinking before you've even started.

**Pavel Frolov** 1:28:10  
Yeah.

**Aaron Bockelie Incognito** 1:28:14  
The actually the other best part is this isn't even support for AI, this is just normal engineering ractice for larger projects in that I've worked with.  
This is a good maturity step.

**Val Levitan** 1:28:34  
OK, guys, that's it. Thank you very much. Pavel, can I just have a short calendar from you? When do you expect things done? You can think about it, send it to me in teams or e-mail.

**Pavel Frolov** 1:28:36  
Yeah. Thank you.  
OK.

**Val Levitan** 1:28:54  
Thank you guys. Have a good day.

**Aaron Bockelie Incognito** 1:28:56  
Thanks. Bye.

**Pavel Frolov** 1:28:57  
Thank you.

**Val Levitan** stopped transcription