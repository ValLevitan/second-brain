**Claude Code integration - continued-20260203_080239-Meeting Recording**

3 February 2026, 01:02pm

2h 23m 46s

**Val Levitan** started transcription

**Aaron Bockelie** 0:03  
Bell.

**Val Levitan** 0:04  
Good morning, everyone.

0:05  
Good morning.

**Pavel Frolov** 0:05  
Hello?

**Irina Shishko** 0:07  
The.

**Val Levitan** 0:09  
Hope everyone is great today.

**Alexander Biratko** 0:12  
Yeah.

**Irina Shishko** 0:14  
Yes.

**Val Levitan** 0:14  
Let's, uh, start. Yeah, Aaron, it's your meeting start.

**Aaron Bockelie** 0:20  
Mhm.  
So how many of you have been able to successfully install cloud code and use it now? Go ahead.  
Um.

**Pavel Frolov** 0:34  
OK.

**Aaron Bockelie** 0:38  
What happened with Evgeny's efforts from last session? Did you discard those or did you actually use them in the code of Evgeny?

**Irina Shishko** 0:48  
Uh, yeah.

**Aaron Bockelie** 1:00  
And can someone translate while I turn on my translator please?

**Pavel Frolov** 1:04  
Actually again you saying that he used lots of solutions, not not exactly the those that was discussed in the end of the previous meeting.

**Aaron Bockelie** 1:12  
OK.  
So let's use that as a starting point, because I think it's important.  
We want to match the type of work that you actually do and the thinking that you do, rather than just blindly accet stuff, which is great.  
So you've getting.  
Can you explain the differences between what was presented and what you eventually went to? What changed?

**Pavel Frolov** 2:01  
Um.

**Evgeny Kharetski** 2:12  
No. Yeah, it's it's possible workflow.

**Irina Shishko** 2:18  
OK.

**Pavel Frolov** 2:25  
Mhm.

**Evgeny Kharetski** 2:26  
What is Montreal?

**Pavel Frolov** 2:36  
Mhm.

**Evgeny Kharetski** 2:52  
Если всё устраивало, то просил реализовать.  
То, что он предложил?  
Вот также очень много с документациями работал, ну то есть там.  
От описания нового функционала.  
Что тоже принципе справлялся на ура с кадрилью работал.  
Ну и наверное все ну вообще много чего делал. Может я просто не всё помню.

**Pavel Frolov** 3:23  
А рон хеви менеджменту в тундре стент но.

**Aaron Bockelie** 3:28  
А.

**Pavel Frolov** 3:29  
Он.

**Aaron Bockelie** 3:30  
Каир специальной.  
Начинающим корабля старт тебя, рапс и мой выбор swf.  
Ты уэйн.  
Пад, сейчас центре возможен.  
Отвратительно начальствующем побегал попу.

**Pavel Frolov** 3:47  
Окей лад лад ми летний экселе Евгений сет за.  
Я хи хи ехали дан это координату команд, схема просто fold райту explain тут lower за проблем is.  
Plan investigate implementation to create a plan implementation plan create to do list for cloud code and then.  
Probably for each particular point in the list.  
Give him additional description or just to ask him to implement one by one. And also if Gainy worked his documentation, asked Claude Code to prepare.  
Documentation for implemented features.  
Seems in general, that's all.

**Aaron Bockelie** 5:07  
OK, so the reason I'm focusing on on Evgeny right now is that.  
This is the kind of the middle of where you're going to need to think about what you've done that was useful and what you've done that was a waste of time, essentially.  
Certain aspects of using these tools can feel like a regression, or can feel like you're technically just sort of doing the same thing slower and more complicated.  
But what really turns into is you need to be able to clearly guide and define the the the rails of what you want things to happen and look like, and you need to do that as early as possible.  
So I I'm going to again focus. So we're going to do something kind of fun today a little bit.  
At least it'll look fun. Let me find it here.  
I'll be using Cloud Desktop to generate the visuals for our discussion today. So the AI sandwich is kind of where we're really going to be sitting at is very, very important. So we need to be able to set constraints, provide context.  
And define the success criteria early, early on in these systems.  
So I know that you guys already do this, and maybe you already know this, but it's one thing to practice to to read about it, and it's another to actually practice it and practice the practicing this feeding of constraint of managing your constraints.

**Pavel Frolov** 6:50  
OK.

**Aaron Bockelie** 6:54  
Is extremely challenging and actually is probably the most difficult part of working with a coding agent. So it's interesting is.  
It's not easy. Why would I change from the way I do things right now? Is kind of the question that you might ask yourself, because essentially it's like having an extra person who's kind of unskilled.  
Um, sitting next to you and you now have to tell it in relatively tight detail what to do.  
So we have to remember that the speed at which these things generate and iterate is significantly different. So let me put this together.  
So I'm kind of using Cloud, Cloud Desktop right now in a similar way that I'm actually telling you about doing it. I'm just using it on the side to rapidly build my presentation and discussion in real time with you.  
Rather than having something prepared, that's going to be just coursework. Because the reality is, is that actual coursework for you guys and putting together slide decks is is not helpful. It just burns money, so.  
What we're trying to do then is we want to understand that every single interaction with a coding agent is going to be these three steps, define, execute and generate, review and decide.  
And when we start thinking about the speed and scale of what execute and generate starts to look like, this is where there now are acceptable trade-offs for the solutions that come out of these systems versus the amount of steering that is necessary to actually get the work done.  
So.  
I don't know what the animation thing is. That's kind of funny. Let's drop that funny robot.  
Ask it to remove the animated runner here, but when we think about the iterations that you as a human can do in a single day is probably two to three in a pull request sort of model.

**Pavel Frolov** 9:48  
Yeah.

**Aaron Bockelie** 10:04  
Um.  
When we think about how many iterations you can get done with the with the with the AI to human review, you can get probably.  
5-10, maybe even 12 reviews a day. So that's 12 code reviews in a single day for a single person.  
And So what I'm doing here is instead of saying AI coding's great, go for it. What instead I'm saying is here is a metric to follow. Here is a goal to try to to hit instead. Let's talk about some goal oriented outcome.  
For coding, rather than just use it because it's fast. That's not using it because it's fast is not actually something that's going to be helpful here.  
When we talk about using it as getting up to this kind of velocity, let's just say 1212 iterations a day, 12 pull requests a day is a potential target for some of you. Then we need to think about how do we?  
Get that with direction. So we got to be able to have tests. Tests are absolutely vital to making this work if you do not have software tests, integration tests, unit tests, specifications.  
Erformance tests.  
All of the above security, you're going to have generation that doesn't work. And then the other kind of pillar to this is the developer experience context. Do you you guys know what I mean by developer experience? Does that sound familiar to you?

**Pavel Frolov** 11:35  
Mhm.

**Aaron Bockelie** 11:47  
Raise your hand if you've heard of developer experience.

**Pavel Frolov** 11:50  
Not exactly.

**Aaron Bockelie** 11:53  
OK, so Pavel, you've experienced developer experience from my product that I built the the the board, the Linux board tool. So I a client command line tool that steers you through all of the steps to be able to make the image, right?

**Pavel Frolov** 12:02  
Mhm.

**Aaron Bockelie** 12:11  
Because if I hadn't done that, I'd have been like, good luck, Pavel, and you would have needed to run all the builds and maybe run the scripts and things like that. And you would have gone Aaron, this is totally useless to me. I cannot use this because it have to invoke all these commands. And I would have said, well, just go read the documentation.  
Do you see how there's a different path? When you think about a build script, when you run a build in a bash file, that's a type of developer experience. You're you're simplifying or presenting a user interface for the developer, right?  
And developer experience can have all sorts of different intentions and meetings. If I were to have to, for example, I wanted to run performance tests against my code. I wanted to test if so many.  
Polygons could be rendered or so many audio files can play or um.  
I don't know, just other sort of actual functional tests for this to hit some targets.  
How would you normally do this? Would you use Java and directly invoke the command to run the class with all of the arameters? Or would you create a convenient scrit that can run at anytime you want?  
This is kind of for Sasha to I'm talking to you, Sasha, just a little bit. Um.  
Sasha, when you are looking for making sure the libraries do the things they do, how do you check them? Do you do it by hand or do you have scripting or other harnesses that help you?

**Alexander Biratko** 13:55  
Mm.

**Pavel Frolov** 14:04  
No.

**Alexander Biratko** 14:07  
Done.

**Pavel Frolov** 14:07  
Hmm.

**Alexander Biratko** 14:09  
Yes.

**Aaron Bockelie** 14:10  
So you can, yeah, yeah. So you run the unit integration tests and they are a type of developer experience or a type of convenience for the developer. And what's interesting is, is what starts out as conveniences for the developers can quickly evolve into tests.

**Alexander Biratko** 14:10  
Unit integration tests.

**Aaron Bockelie** 14:30  
And integration verification and all sorts of other things because you can formalize it.  
And we can also also think of the initial tests that you as a developer write for convenience become context and guardrail themselves for AI tools, because what we're doing now is instead of just writing up a text file.  
Let's see here.  
Uh.  
We'll let Claude put this concept together here. So when we think about what it takes to prompt an A I system, you need to describe what it is you're going to do, right? And when you run the code and you let and you and you see the piece of software do what it does.  
And you find the the.  
Inadequacies of your current software, and you read the user story for what's going to have to get fixed instead. This is all prompting. This is all text. You're describing it to the coding agent to probabilistically create.  
Fixes or imrove the code.  
But it's it's it takes a lot of effort for a human for you to type up this prompt all the time.  
And one of the ways that you can reduce the amount of effort it takes for the human to steer it or or as another dimension to improve the quality of the type of prompting and context for the for the coding agent is to use these automated tools like this.  
And we all have access to them already. We should. You already have linters, you already have type checker tests, you already have integration tests and unit tests and things like that.  
So when we think about what a static prompt for coding something looks like, just do this.  
When you just type it in, that's like the lowest end. When you ask it, go to Jira and read the user story and then do it for me. That's sort of medium. That's low medium effort or medium value when you have in the code base.  
The tools necessary to conveniently work with the code base itself. Lenters, checkers, doc strings, other things like this. These become engineered developer experience and the AI system can get these and.  
Accelerate the speed of development much, much faster than before.  
This means that when you have performance linters and unit tests, when you have deployment components in here already built in, you invest in this one time and then you grow with it. And then the the the A I systems follow along and track with these. They become part of the prompting process themselves.  
So you can start to now let's let's do this.

**Pavel Frolov** 18:28  
It.

**Aaron Bockelie** 19:33  
So what I want to have happen here is I want to be able to provide a a. I want to be able to provide a progression, a thinking model for for you guys. So right now.  
Evgeny, when when on our last session you know how I gave you a prompt that said write some unit tests first before we did the actual code. I know what you ended up doing was a little different, but I I said use unit tests and then write the code. Did you notice that the way I had?  
Prompt that last time. I'll let the translation give me a thumbs up if you understand. OK, and if we had not done that, the type of output that we would have seen the coding agent do would have been very.  
Unpredictable, wildly different, potentially every time we can think about how in the original piece here when we talk about curating and defining when you have a test harness and a test framework.  
When you have deployment tools, when you have performance tools to check all these, these become part of your curating and defining the problem. And So what happens is that we want to keep the robot in the middle. Oops, in the middle part there. Let's go back to this for just a minute.  
We want to keep the robot in the middle here because this is where it lives the best at at generating an incremental changes and and trying it out and when we have to manually review and decide when we have to manually test the code or invoke it.

**Pavel Frolov** 21:07  
Please.

**Aaron Bockelie** 21:13  
We have to manually run erformance or integration tests. This is extremely slow now.  
But if we have the coding and automation for the experience first, if we sort of start by building the tools that allow it to build it and then get to the answer, we come up with a very different sort of experience when we're building it. So we can think about how this sort of starts out.  
Heavy prompting, right? Build me a REST API with these endpoints. Make sure to validate all the inputs, blah blah blah, error handling, this, that and the other thing. It's a lot of work. It's even worse if you already have a big code base because now you have to explain your code base to this thing too, right?  
And when we think about it, it's it's, it's got no guardrails. And so most of the burden is on the human, not the AI model. So you don't feel like you're getting any output that's usable.  
When you start getting into bootstrap mode, when you say make a test script that does this thing or set up a make file or give me a linting configuration or write a pipeline, you're preparing the tools to build the tools to build the tools. You know what I mean by this? There's a recursion here.  
You understand what I mean by recursion of this. This is important to to to to see.  
You're starting by sharpening your knives. You don't butcher the meat with dull knives, right? So we're going to make all these tools work first. Finally, towards the more other end, the mature end of this.  
Add a slash users endpoint. It's already known the context is there. You already have linters, you have doc strings, you have potentially.  
You know REST API docs in there. You have type checks, you have integration tests, so the framework carries the context rather than the person carrying the context.  
And this is the difference between doing it here and going this is too much work and doing it here. And it's like it's kind of almost magic. It's like it follows exactly what you want. It follows the conventions you want. It does all the other things too.  
So this way it's kind of funny because you have to actually put the work into the tools that you need to make to steer it before you can actually use it in in a way that makes sense.

**Pavel Frolov** 23:43  
Um.

**Aaron Bockelie** 23:48  
Let you absorb that for just a minute while I come up with the next prompt here about this.  
So this is the next prompt. We're going to talk about things outside of the software engineering envelope here. So when we talk about what's outside of the envelope, that means the things that really we can't feed to a coding agent.  
Uh.  
So when you guys sit over tea or coffee during a break or decide to go get lunch or something like that, is cloud code listening to you?  
It's not. When you talk about something in the hallways or in chat or whatever, it doesn't have that context either. But as we have been doing this our entire lives, and humanity just does this in general, every single word we say and every experience we have.  
Becomes our context for understanding.  
When when Sasha and Pasha sit down and discuss the technical merit of a certain particular way, because they just need to talk about it to learn it themselves.  
The the robot doesn't hear. They don't have the context. And that's a natural thing that has to happen because we're not robots, we're not computers, we're not a I systems. But what we do have to do is we have to be able to collect this information somehow.  
So much like how Val records all of his conversations, he's not doing it for sort of understanding or keeping a tight record of it. He's doing it because he's found the value in keeping the human part of the interaction as much as possible and using that to steer the systems.  
Let's see here.  
So when we think about human context as guardrails, so technical discussions happen everywhere. We write these docs, we do these things when we don't have, when we keep things in context and out of context, we can keep these tools steered and specific, right? So when we want to include it.  
We include our tools for GitHub issues and things. We keep things like architectural decision records. We keep the technical chat inside of here as much as we can. We keep readmes and contributings in there. All of these things become parts of the context steering that statistically and.  
Robabilistically guides a coding agent into roducing better quality aligned with what you want.  
When you start leaving, including things like vague feature requests, meeting notes, marketing docs, business road maps, these all confuse these tools. They waste your context and they cause it to think about stuff that doesn't make sense or the focus at hand.  
In a different situation where you weren't writing code with cloud code or or coding agents, but instead producing business Rd. maps or producing marketing docs, the inverse applies. I don't think anybody on this, nobody on this call really is in the marketing and and and.  
Sales area, are you? You're all kind of engineering, yeah.  
OI need you to just imagine for a minute you were a salesperson or you were a marketing person and you wanted to use these tools too.

**Pavel Frolov** 28:49  
Yes.

**Aaron Bockelie** 29:01  
This information about GitHub issues, architecture, decision records.  
Meetings and things like that. These would be noise to a salesperson, right? What would happen if you put in in the context of a marketing focus claude session that there's a bunch of bugs in your software?  
We're going to fix. Imagine what would happen. The the agent would include spin it in a good way. We're going to fix all this stuff by next quarter. That would be terrible marketing. It would be absolutely wrong and the marketer would be what happened. I have no idea.  
So they don't include stuff like that. You don't include that kind of detail. And in this case, you need to make sure that when you're working in your context, which is a technical and engineering aspect, you don't include the stuff that's not technical. So you have to.  
Find a way to split this up.  
I added at the end here I said the other things you really want to be able to capture is curated meeting transcripts and conversations too. So you can see how we can take this transcript and extract decisions and add to the documents.  
I would be willing to guess that you could talk to Val about some of the discussions about directions of architecture and things like that. And if he had that transcript, you could convert that transcript directly into decisions.  
That might be architectural decisions, or at least guidance decisions in the code base. And as soon as you do that, as soon as you take you do that through this process.  
Hey, Val, give me that that transcript about the thing we talked about. OK, OK, Pavel. Pavel. Hey, Claude, take this transcript and turn it into the steering for the next quarter for the goals that we're working on for the tool.  
Log code goes. OK, sure.  
Havel reviews the output and accepts the pull request for documentation into the code review. O we've taken the path now of.  
Capturing the conversations or transcripts and turning them into the contact machine into this.  
Middle section here because what Pavel's done is he's added this context here to an automated fashion. He's put the docs into the git repo so it's already available to the tool.  
O when we think about this context then.  
We can co-locate the decisions with the code. This means keeping the decisions in the code base or very adjacent to it. You know what I mean by this now? So GitHub would be where decisions could be made, or the git repo itself can be where decisions are made.  
You have to just like how right now when you guys write a like a pull request or you do a issue commit, you know how you usually mention the JIRA issue.  
So we need to start thinking of JIRA not so much as the technical layer, but as the planning layer, the the administration layer. It would be better to have the issues marked up in GitHub.  
Than JIRA because it's a farther step away. More steps of running commands to get the context from JIRA than it is to get it from GitHub.  
And then the other thing is, is that you want to just dump a bunch of stuff. You don't want to just throw a bunch of raw transcripts and things in there. You have to clean your data first.  
So we need to remember that when we talk about the human discussions here, that the human discussions are the documentation. When you guys talk amongst yourselves, you have to remember that somebody else needs help doing this or you don't get the.  
Acceleration benefits of it, and that's the coding agents.  
I'm not saying set up a phone with a recorder and record every your entire life. That's kind of crazy and not really what you want to do. But what I am saying is, is that for the decisions you made, it's like how many of you guys have a white? Do you use whiteboards in the office right now? Like do you draw stuff out?

**Irina Shishko** 33:55  
Yes.

**Aaron Bockelie** 33:57  
OK. Do you regularly take pictures of the whiteboard?

**Pavel Frolov** 34:02  
From from time to time, yeah.

**Aaron Bockelie** 34:04  
And where do those pictures end U at?

**Pavel Frolov** 34:07  
Mobile phones sometimes some yes, sometimes it it can be attached to some issue, but not but not on a regular basis.

**Aaron Bockelie** 34:09  
But do they go out of the phone into somewhere?  
Like an e-mail or something.  
So you need to get into the habit of sharing that whiteboard with Claude, with the coding agent, and process it into the decisions made and have a short dialogue about processing that all the time. That is a really valuable set of context, because think about what's happening here.  
Here you have the human minds moving at humans dimensionality, way, way more bigger considerations than a coding agent, right? And you're all standing around an information radiator called a whiteboard, and you're puzzling it out. And when you're done, you're like, aha, we've got it.  
It's so we got it so good, we're gonna take a picture of it and send it to everybody. The one person that you need to send it to as well is a conversation with a cloud code or a cloud desktop type of tool.  
To extract that positioning and that reasoning and that meaning, turn it into context, you get to keep.  
If you don't, it's lost. So what I want you to do is I want you to think about how you guys need to start thinking like a data scientist a little more. I'm not saying become data scientists, but I want you to think like 1 a little bit.  
If you feed things noise, you get noise out, garbage and garbage out, right? The old thinking of just throw everything at it doesn't work. You can't just throw any context at stuff. You have to throw the right context. If you were to take the picture of the whiteboard and attach it to the git repo bubble.  
Would that be valuable or would it be better to take a picture of the git repo, have a discussion with the AI system to extract the purpose and meaning of it as you understood it, and check that doc that text document into the git repo?

**Pavel Frolov** 36:18  
What is the the better either have original photo in GitHub or translated data at GitHub?

**Aaron Bockelie** 36:30  
Prepared. Prepared data. Yeah, that's your choices.

**Pavel Frolov** 36:33  
Phone.  
Very likely original photo will be better. Why? Why? Because actually if you perform some some work over this picture.

**Aaron Bockelie** 36:44  
So if the yeah.

**Pavel Frolov** 36:55  
It could be not the full information.

**Aaron Bockelie** 36:56  
Right. So, so how do you control? So this is an interesting thing because I actually disagree and I believe that the translated information is better. But I also agree with you if I think about where you're coming from and what I'm going to say.  
Is with caveat, with the caveat that the AI system never sees the original picture.  
If you include the picture and cloud code picks it up and reads the picture, it's going to be confused because it it was not in that conversation. You humans stood around the whiteboard and discussed it for an hour. None of that context was available to interpret that whiteboard, right?  
So what happens is that the agent reads the whiteboard as if they'd never seen it before in that picture, tries to extract the ideas from it, and it will do OK, but it won't do that great. So what you would be better to have then, assuming that you need to have the original context, because I'm guessing what you're saying.  
Pavel is that you have a particular view into the whiteboard, right? But Irina might have a different view into the whiteboard. Both have your own minds, right?

**Pavel Frolov** 38:11  
Yeah.

**Aaron Bockelie** 38:14  
And So what's? So let's let's break this down a little further. What this actually means is that go back again to the very top, the most important part.

**Pavel Frolov** 38:14  
Exactly.

**Aaron Bockelie** 38:26  
Everybody on that discussion with the whiteboard needs to do this process with the same picture. You will get everybody's opinions broken out into five different ways, right? Say five people were participating in the whiteboard session.  
Afterwards, you combine all these into a actual commit in git of the text document of your understanding of the whiteboard. So Pavel, Irina, Igor, Sasha, Evgeny.  
All five of you are going to have a quick summary review from your perspective of how this makes sense. Maybe two or three back and forth using the sandwich.  
You then one of you chooses to make the commit of that document to the to the git repo, right? So this is an important discussion. You spent an hour doing this. It was an expensive meeting and so forth. Each of you distill the output from your meeting.

**Pavel Frolov** 39:18  
So.

**Aaron Bockelie** 39:30  
And then you all of you contribute to a pull request commentary about this or a GitHub discussion about this.  
Imagine if you start a GitHub issue with the original whiteboard picture and then all of you, all five of you paste your coded your your agent digested version of this into it and then the one person responsible for checking in the output from this.  
Into the code repo is combining all the viewpoints. In fact, I think this is important enough to diagram. We'll get back to think like a data scientist in just a minute here, but let's add this next one too.  
OK, so I'm going to take what I just trying to explain to you and I want to diagram it. So it's very, very clear what I'm trying to say here. And there is a a flip side to this that you're going to understand in just a minute. One is is that when you have share a whiteboard and you have five different perspectives for that whiteboard.  
And then you combine it all into a big document. What you've essentially done is averaged the intentions of everybody into one space. You have used an AI tool to collect the.  
Intentions of everyone, rather than let one person get in front or lead it, or have that one perspective. You've synthesized a set of understandings that are greater than the individual pieces if added up.  
And when you then capture this into the into a git repo for for documentation and and and using it, you have done something that is actually very difficult to do without a lot of extra expense.  
Of having yet another person, a project manager, a product owner, a secretary, whatever you want to call them, to do this sort of bureaucratic work, this, this non work that must be done to understand the problem.  
So when we think about how we take this flow and do it, now we realize how many people do we actually need on the meeting to be able to do this?  
So maybe right now it's all five, but if you can start to remember that certain people have certain viewpoints, you can reduce this amount as you build the context in the git repo for things you can.  
Sort of substitute the person. Let's say Igor has.  
Very specific desires for how UX and front end and sort of the development has. I don't know if that's what you're doing still or tell me if you're doing something else, but if you have particular ways that you want things to happen right, what you can do is if Irina and Paul and Sasha and Pasha are talking.  
Talking about how to test the interface and make it work, but they have to present something to the users as a user interface. If you've previously brought your intentions of how you want things to work from a UX standpoint, from descriptions, from actual templates, from all of the.

**Pavel Frolov** 44:00  
Yes.

**Aaron Bockelie** 44:05  
The.  
Framework for the AI for context around it. You don't necessarily need to be in that meeting now. Now you can go look at the picture of the whiteboard that Pavel said he saved. You can look at the output that they did, and you can let the coding agent review what they did. And the coding agent also has access to all of your considerations about how you're supposed to.  
Us to be putting the stuff together and you can have this conversation much, much faster than you would if you had sat in that meeting for the hour. So in 10 minutes going through the meeting minutes through the discussion with the whiteboard pictures.

**Pavel Frolov** 44:37  
Yes.

**Aaron Bockelie** 44:42  
You're going to get the same or better understanding of what's going on and get your opinion into the situation than you would if you'd spent an hour with those guys doing that. It doesn't mean give up the conversation in with humans, obviously.  
But it means that you can choose to attend less of these meetings and use this as a way to harness that information using the same sandwich theory. So let's I'm kind of getting ahead now. So let me go back to thinking like a data scientist for just a minute and then we'll go forward again. So when we think like a data scientist.  
We need to maximize the signal to noise ratio. When you have a conversation for an hour in front of a whiteboard, everything. Oh yeah.

**Pavel Frolov** 45:24  
I don't know one one second. May I may I ask you to to say a little bit slow because for me it it becomes quite difficult. I assume that the other person will be more difficult.

**Aaron Bockelie** 45:28  
Yes.  
Oh, sorry.  
Yeah, I'm sorry. So, so let me let me just tell you where I'm at. I kind of was moving fast and went into how to understand how to combine a discussion in the real world. I'm going back a little bit now.  
To talk about the what you how you have to think before you have discussions in the real world.  
So you have to think it like a data scientist.  
You have to maximize the signal to noise ratio. This means that everything you say is information. Everything.  
And so when you have a whiteboard and you write, somebody writes their lunch order in the corner of the whiteboard and you take the picture of it. And so Pavel had a sandwich and Irina had the soup. That context can get put into accidentally into the git repo.  
So you have to clean your information up.  
Next.  
You can't just take the raw data. Let's say you clean up your information, but now you have the raw data. You have to structure your raw data in certain ways. So you need to create this into dark architectural decision requirements. You can structure this into tests. You can structure this into other frameworks.  
Types of things.  
You need to be able to label your data. You need to use a labeling structure that makes sense. When you write down architectural decisions, when you write down documentation, you use labels.  
You need to separate by purpose. You can't talk about the back end and the front end in the same conversation. Sometimes if you if they're related to each other, if we say this is affecting that, it's OK because part part of the.  
Purpose. But if you discuss several related unrelated items with each other, separate the separate the purpose.  
Single purpose and then finally, don't just let it happen one time, you have to iterate a few times and loo through it.  
You have to ask what was missing? What was misleading? Evgeny at the beginning of this chat. Remember what I asked you? I said. What did you do instead, right?  
This is right here is the same thing. What was missing? What was misleading? When you catch that thing doing the wrong thing, you have to say you have to, you have to go into what I call metacognitive thinking for just a minute.  
You have to pause and fix the problem right there. You use the coding agent or tools and say I meant this. You did that. Why did you think that? And what's really interesting is these things are very, very blunt and obvious and they will tell you exactly why it made.  
That decision.  
And that is likely the next thing you're going to fix in your context. You've got to write a bug, literally write a bug for your context management to make sure that you cover that gap next time.  
So when we think about this from a data science term and what the developer means, training data is to read these architectural documents, code comments. Make sure you have very verbose code, right? Feature engineering means curating and structuring content text.  
Labels is labels and so forth. O I'll share all these slides with you guys too, so we can, you know you guys will have them. And then finally you are.  
By by taking on this advantage of being able to generate code incredibly fast, that can be good quality. You're not a developer anymore, only you are a data engineer for your AI teammate, and so you're taking on the additional burden.  
Of engineering data for your AI teammate because when you do this you can get a significant speed up of quality output. So kind of like the old saying of.  
Two steps forward, one step back. It's kind of a that's the minimum requirement. But if you could take 10 steps forward and one step back, it's very valuable to do that. So you have to do this in a.  
In a established practice manner to constantly getting to constantly get that that 10 steps forward. Let me find it here.  
Here we go.  
So when we say that without an agent, we can take three good steps a day, OK?  
With a coding agent, you could potentially take up to 12 steps a day, but these first three are consumed with these steps, so you're actually taking nine steps a day. So it's a math. Simple math if you if you spend this much time blocks doing.  
Curating your data as a data scientist, and then you get this much output out of it. You're still yielding twice to three times your typical output that you have for this.  
But you have to be able to do it with direction, so you'll have chaos otherwise. So this is kind of the the two sides of this.  
I'm going to pause for just a minute on this thinking like a data scientist for a minute.  
Does this? Does this sound crazy to you? Does this sound rational? Where do you feel like it is? It's OK to say anything. I want to get some feedback from you guys.  
This is probably besides the sandwich thing at the beginning, the human, the AI, the human piece. Thinking like a data scientist is the second most important part of this whole discussion I'm I'm sharing with you today.

52:30  
Oh.

**Irina Shishko** 52:31  
Mhm.

**Evgeny Kharetski** 52:36  
It's important.

**Alexander Biratko** 52:36  
The moment.

**Irina Shishko** 52:38  
No, she's a private Nepal's.

**Pavel Frolov** 52:44  
Yes.

**Alexander Biratko** 52:51  
Right.

**Evgeny Kharetski** 52:51  
We'll break the conception upon this.

**Pavel Frolov** 52:52  
Mhm.  
Клукс лайк этой банде грит. Вот и theses.  
Подойди ост бичевин disorder вот.  
А венди стенд этот фонарь винит у тумака it.  
Сру.  
В конце.  
Трактует это он дэйли bases усович, то нью роуч николаос райт нау михеев.  
А я в тулузе ткан думаю не ворк фаста зен ю.  
Энд час не тут корректный план.  
Это ворк корабли Андерсен. Вот из вот из дансанд.  
What was the original?  
The meeting, yeah.

53:58  
Intense.

**Pavel Frolov** 53:59  
Intention, yeah.  
But when I say intention, it actually relates to business requirements, what the business needs and how it was translated into tasks, into requirements.  
A architectural decision requirements and so on.

**Aaron Bockelie** 54:28  
Mhm.  
So when you think about that business requirements, architecture requirements and things like that, um.  
These are the pieces that a coding agent or an AI in general, at least a text generating AI, right? That's what this is the the whole conversation we're having about is dealing with the class of AI systems known as generative text output, right? Like all of it.

**Pavel Frolov** 54:39  
It is.

**Aaron Bockelie** 54:57  
So you have to remember that while it might have been traded, trained on all of humanity's information, it actually knows nothing of your life. It does not know that Irina has worked in the games industry for 20 plus years. It does not know that.  
Igor does UX design for back-end platforms. It does not know that Sasha focuses on game engine frameworks right now and other system embedded systems level stuff. It has no idea of those things.  
And your collective experiences, everybody on this team, I haven't picked on Andrei for a little bit. Andrei also includes the fact that Andrei and Dmitri are been have been IT guys for for 1015 years.  
So when you engage these tools and systems, they do not know or care about you. They are just systems that predict information. And So what you bring to the table as people, as as humans here.  
Let's, uh, make sure I got this in the right spot here when you when you.  
Consider where the Uh.  
The conversation happens. You're hired as a human by a company owned by a person or a group to do work, and that work eventually becomes valuable because people pay for it and you make money and life continues, right?  
This system of what I just described happens entirely outside of the context of these coding agents. They have no idea that this happens, nor would you ever share that with them.  
You are in a way like the adult in the room, understanding the real problem at hand. It is a financial, social, political problem that is being solved.  
Right. It has nothing to do with tech at some point.  
And so you, as a human interacting, living in the human world, have to choose which pieces to feed into these systems to get the context, because you're using this system to accelerate your goals and your desires.  
These systems have no goals and desires at all, except for the way the text is is shared with them and then they develop their models internally and you as holding meetings with planning meetings or.  
Um, prioritization or what are we going to do next and all these things?  
You have to actually be actively engaged and in control of those conversations. And what you do is you take the output from that and you think like a data scientist and transform this into actionable steps that these things can do because what you're using it for.  
What you're using these class of systems for is to accelerate the one piece that takes too long right now, which is to enter your wishes into machine language or into architecture, architectural documents, or into.  
Actual artifacts that can execute code.  
So I think.  
I don't want to get too much into the into the non-technical aspect of it, but it is very much you have to decide which part are you relinquishing control over a little bit and which ones are you holding on to. And I suggest holding on to the human pieces of it. So let's move on from thinking like a data scientist for a minute.  
And let's discuss this distributed context capture. This is kind of in that direction a little bit. So here, here's the whiteboard, right? We're talking about services and off flow and databases or whatever. Here, look, you've got a little tool wrench. Do you see it? It's kind of funny.  
I don't know. Everybody's in front of their computers and basically Claude has no access to this information.  
When you when you paste this picture into it, it can read the board, but it still doesn't know the context. It's kind of just random stuff.  
About this from a person with their agents. So Irina and her agents, Igor, Pavel all have different discussions about this.  
And then you share it in a discussion.  
You don't have to say Claude, do it as Claude. You just post it as yourself, but you just let Claude post it for you as an example.  
Then we take the responsible person. So in this case, Irina, you're the responsible person and you say, Claude, combine everybody's viewpoints.  
Into an architectural design.  
Whiteboard. It's mostly in your guys's mind. Whiteboards are a funny thing. Not a lot of information gets actually recorded on a whiteboard. Most of it's in your. It's not working. This is the process of getting it out of your brains.  
This is the process of combining it. This is the process of curating it.  
When you've done this, every single coding agent has access to this decision in its composite form from everybody's viewpoint in a managed, structured, searchable way.  
So This is why you don't add the whiteboard picture, you distribute the interpretation of it. But to Paul's merit, it's good to keep the whiteboard picture because it will remind the people of what you discussed about.  
When you take a whiteboard picture from five years ago, is it useful anymore?  
We've forgotten about it by then, but a whiteboard even a month later, or six months later, or even a year later, we can still remember what was discussed on that whiteboard.  
Questions about this before I move on to the next next piece here.

**Irina Shishko** 1:01:29  
No.

**Pavel Frolov** 1:01:29  
Yeah, everything is quite clear.

**Aaron Bockelie** 1:01:33  
OK, so I'm gonna use a totally different analogy for just a minute. I have a big yard and I have lots of trees and all the time the trees are dropping branches. Like in the winter time, the storms come through. I get a huge branch like a log that fall a dead.  
Piece of a tree falls off. I get all the dumb little branches. I got everything.  
We can think of the AI agent as the burn barrel. It's the fire where we're dealing with things and we have to process this. We have to cut it to the right size. We have to curate our data. We can chop it by hand. It's slow, but we don't want to really do that. We want to do it as fast as possible.  
Which is why I'm even using this to begin with. It's extra effort to hold on to a burn barrel. I have to make sure it's safe. I have to deal with the smoke. I have to be ready to answer if the fire department shows up, all sorts of stuff. But I do this because it's far faster and effective, more effective.  
And doing it by hand.  
So we can kind of think now about how this processing of of things, either physical things or information, is sort of a same thing. And there's particular ways you have to do this. You can't throw the whole tree into the fire pit.  
You can't give it incorrectly processed stuff. You have to feed it properly prepared information.  
So fire doesn't care how big your tree was, it only cares what you feed it, and it's the prep work for this is what makes it useful. I just I really like this analogy because it has it's such a simple thing. Fire is the original technology for humans, right?  
Right in a lot of ways. And we're at a point to where we now have fire for thought, which is amazing thing. But fire is stupid. It can just do the wrong things when incorrectly used. An AI machine processing of intelligence is stupid and can do absolutely the wrong thing when improperly used.  
So this is I'm gonna kind of leave this at this point because an hour long discussion with this is quite a lot to go through.  
Does anybody have any thoughts about this?  
This analogy here.  
Do you disagree with this?

**Alexander Biratko** 1:04:07  
Great.

**Pavel Frolov** 1:04:11  
Agree.

**Aaron Bockelie** 1:04:12  
OK.  
Who's this name?  
Anywhere yet?  
But.

**Irina Shishko** 1:05:10  
Yeah.  
Авторизованный.  
Требования здесь единиц, это всё вместе проанализировать и получить.  
Что?  
Что покрыто тестами, что ещё не покрыл?  
Какими требованиями нужно работать? И, в общем, то это было до.  
Достаточно хорошо сделано просто.  
К рукам.  
Мой.  
Вот скоро.  
Там.  
Я ещё не вижу.

**Aaron Bockelie** 1:07:16  
Солдатами.  
И tengrinews нюхают часочек херринг.

**Irina Shishko** 1:07:32  
Угу.

**Aaron Bockelie** 1:07:34  
Презентировать у тебя остынет, написал как продевает.  
Бустерного, *****.  
Я.

**Irina Shishko** 1:07:42  
Я что то не очень.

**Ihar Hrybko** 1:07:42  
А танька на на на так закрыть тест тест в больницу.  
All the setup screens and understand they correctly aligned with our previous setup and we don't miss anything.

**Aaron Bockelie** 1:08:03  
OK.  
So you're doing it through visual way, like actually looking at the screens. Is that the case?

**Ihar Hrybko** 1:08:08  
In in that way.  
I think we need to ask Irina because I only provide.

**Irina Shishko** 1:08:20  
One second.  
Yes, and I do.  
I want to make ****.

**Pavel Frolov** 1:08:39  
You have to show.

**Ihar Hrybko** 1:08:39  
New site also.

**Irina Shishko** 1:08:40  
Mute.  
I mean.

**Pavel Frolov** 1:08:46  
OK.

**Ihar Hrybko** 1:08:48  
Mhm.

**Pavel Frolov** 1:08:48  
Yes, sure.

**Aaron Bockelie** 1:08:50  
OK.  
Yes.

**Irina Shishko** 1:09:11  
Надо.  
Сапоги.  
Но создать.  
Ричи истории на реализацию авто.  
Тестов.

**Ihar Hrybko** 1:09:24  
На все таки автор.

**Irina Shishko** 1:09:24  
Вот я.  
Да.  
Я всё.  
Хорошо.  
Чем занимался?  
То есть вопрос был в том, как я его использую вот.  
То есть я с клодом проанализировала это, ну посмотрела что где чтоб он ну как бы не руками я вытаскивала, а он с этих прототипов вытащил секции разделы, то есть посмотрела, как он это делает дальше сказал, что мне нужно создать в джиро фичи и истории для написания авто тестов. Вот он опять же.  
Вот, например, сетап чистом проанализировал вот эти разделы, как они делятся, создал стори в джиро.

**Aaron Bockelie** 1:10:05  
Окей.

**Irina Shishko** 1:10:14  
И как бы дальше уже там мы засадили, на кого куда их по сроку ребят жира правильно положили вот этим вот я пробовала.  
Заниматься?

**Aaron Bockelie** 1:10:30  
Намибию.

**Irina Shishko** 1:10:30  
Ну и.

**Aaron Bockelie** 1:10:32  
Намибией веры спецэффект просто скрипты вей.  
Томми Томми какая можем?  
Юра дизайн стефанчук.

**Irina Shishko** 1:10:41  
Вот.

**Aaron Bockelie** 1:10:44  
Игорь сквида, figma макаф.  
And create the test items in JIRA to be able to test it. Is that correct?

**Irina Shishko** 1:11:00  
And maybe we should be short.

**Ihar Hrybko** 1:11:03  
Looks like, yes.

**Aaron Bockelie** 1:11:06  
Pretty close.

**Irina Shishko** 1:11:11  
Oh.

**Pavel Frolov** 1:11:15  
Yes.

**Aaron Bockelie** 1:11:20  
Hey, did you?  
Elapse the time. So remember part of what we're.  
But that.  
Aspect of context because you can see this.  
Order to you have to have access to.  
To turn this from a ickma mock U into possibly.  
Yeah.

**Ihar Hrybko** 1:12:20  
Yeah, I mean by saying into code like the front end part of.

**Aaron Bockelie** 1:12:25  
Yeah, exactly. The front end part. And then Igor also has to know the back end part rather than just make it a pretty user interface.

**Ihar Hrybko** 1:12:30  
Yes.

**Aaron Bockelie** 1:12:41  
So so if I was to write the test.

**Ihar Hrybko** 1:12:42  
Yes.

**Aaron Bockelie** 1:12:46  
She needs to have access to the React front end.  
The back end endpoints the visual images of what's going on.  
And.  
Right.  
That's five things that have to manage.  
Now what is that if you're thinking as well as director, you would want to curate those five things to make sure they're available to you.  
Perhaps in your department.  
They do this is that you have your coding agents.  
You can have it look at a literally login to Figma on a browser and it can see this exact picture like this. It can actually take a screenshot and visually see this image and describe every element on it.  
It can also read through a React prototype export from this, so if you haven't checked into a git repo as the React front end, you have that available.  
If you have an introspection service, a a a tool or a framework to look at the swagger endpoint for this actual API doc, have all the API doc and barring that.  
Maybe you have all the abstraction classes for the endoints.  
Finally, you have access to JIRA. You have access to where JIRA is going to be tracking its tests, and you also have in the GitHub repo the definition of how you want tests written. We want them written this way and so forth.

**Val Levitan** 1:14:48  
You need you need to pause.

**Aaron Bockelie** 1:14:50  
Yep, OK, there's. I'm just trying to describe literally the pieces.

**Val Levitan** 1:14:54  
I don't believe I I I believe it's it's not hitting the point.

**Aaron Bockelie** 1:15:01  
OK, well, I might put this together as another diagram then. Well, just, well, I want you guys to think about what I said so far for so far, what you can catch.  
Let me grab a picture of this.

**Val Levitan** 1:15:13  
It's not it. It's not. It's not hearing the point.

**Aaron Bockelie** 1:15:16  
Can you share your screen again so I can get a picture of that please?

**Irina Shishko** 1:15:18  
Oh, OK.

**Val Levitan** 1:15:24  
You, uh, did you guys check out?  
Already.  
It will start it.

**Ihar Hrybko** 1:15:37  
What is the translation?

**Val Levitan** 1:15:53  
Yeah.  
OK.  
Sopanero the brandish to Aaron Gallerit.  
Good.

**Ihar Hrybko** 1:17:03  
But but.

**Andrei Bosik** 1:17:04  
What am I saying?

**Val Levitan** 1:17:13  
Hello.

**Alexander Biratko** 1:18:29  
Контекстного и некоторые вещи.  
Который.  
Мы думаем, как бы не попади он, он думает, что они не важны. Ну я про искусств.  
На интеллект агентов.

**Val Levitan** 1:18:43  
Я понимаю, что мы этот вопрос вчера с Димой и Андреем.  
Первым показал им соус.  
Над которым он работает и вы, насколько я правильно понимаю ваш вопрос, Александр, я понимаю, что вы про.  
Праздник.  
Но вчера Иран и мы мы об этом уже давно знали. Эрен уже около полугода работает над продуктом, который он вчера показывал.  
Андрею и диме.

**Alexander Biratko** 1:19:20  
Ну я так понимаю, контекст будет сворачиваться, да сворачиваться, сворачиваться в какое то более концентрированный вид. Правильно нет.

**Val Levitan** 1:19:20  
Я бы.  
Я.

**Andrei Bosik** 1:19:27  
Нет.

**Alexander Biratko** 1:19:31  
Нет.

**Irina Shishko** 1:19:33  
Ну проще тогда по, чтобы Иран показал, если.

**Andrei Bosik** 1:19:38  
Но там пока ещё очень сырая версия этого продукта. Вот но если в 2 словах говорить, то будет некая база знаний, пока опять же говорю сырой проект. Он ещё даже, наверное, сложно его Альфа версией назвать. Да, то есть.

**Irina Shishko** 1:19:38  
Все начнётся гадать как я.

**Andrei Bosik** 1:19:55  
Вот.  
Может никак.  
Они, которые мы будем выгружать наши, например, те же самые митинги, ещё какой формат?  
Что можно будет картинки, подарки, мордовские документы, грузить и так далее.  
Так что будет.  
Тогда как?  
Атмосфера.  
Подобное.  
По смыслу вещи, которые с другом связывал, вот и когда он будет строить этот граф.  
Получится возможность, скажем так, объединять какие то знания в какой-то, например, там схожие области и так далее. Ну и соответственно, эти знания потом вызывать и с учат читать вот.  
Просто как там фильтровать потом скажем так.  
Неправильные какие то вещи или заблуждения или заблуждаться, при том можно же быть уверенным, что ты думаешь правильно. На самом деле ты заблуждаешься, да, то есть и вводить в заблуждение его или в.  
Других.  
Коллег, скажем так, вот то этот часть он как бы тоже должен будет обрабатывать, но как вчера вот вал, сказал, пока там есть ещё туман да, когда начнём как то это внедрять пользоваться, то мы сможем этот туман.  
Посеять, но он составил вопрос, задаёшь мы арт?  
Когда показывал инструмент, который должен будет решить эти проблемы.

**Alexander Biratko** 1:21:23  
Ну, блин, это получается сейчас, когда мы работать будем. Вот с этим то есть всё равно тот, кто пишет промт, он должен акцент.  
Сдавать внимание конкретного агента на ту область, с которой ты сейчас работаешь. Ну то есть всё равно контекст общий всё таки остаётся пока что в голове Того, кто сработает, потому что ну весь контекст, пока что яичко не держит. Ну я к этому.

**Val Levitan** 1:21:51  
Это это это это правильно, но я хотел бы заметить 2 вещи.

**Alexander Biratko** 1:21:51  
Ввиду то есть.

**Evgeny Kharetski** 1:21:51  
Ведущий.

**Val Levitan** 1:21:56  
Что то, что назвали эрвина?  
Построй инструмент свой, но сегодня существует инструменты, которые дизайн большими компаниями, которые не сырой его можно купить и пользоваться за него надо платить лицензию где то $100000 в год.  
Можем ли мы себе это позволить? Конечно, можем.  
Но р инструмент очень, очень интересный. Я бы дал возможность ему закончить этот инструмент.  
И я думаю, что он нам поможет, но да.  
А пока у нас есть, давайте не забудем следует.  
Работаем с меньшим контекстом, у нас есть очень много.  
Опрокинетесь на улучшение на размещен.  
Поэтому пока мы дойдем до работы с большим контекстом, давайте хотя бы с маленьким контекстом зачем работать?  
Но саша правильно поднимает вопрос.  
Но я хочу сразу ответить саше.

**Alexander Biratko** 1:22:57  
Не ну я я почему почему?  
Ну ответьте, ответьте потом.

**Val Levitan** 1:23:03  
Что сегодня есть инструмент, который мы можем лицензировать за пару сот $1000 в год, который позволит работать совсем контекстом.  
Это мой ответ был.

**Alexander Biratko** 1:23:15  
Потому что сейчас, когда работаешь с одним и тем же кодом долго ну долго долго он он контекст, всё время добавляет, добавляет, и в какой-то определённый момент ты начинаешь понимать, что он забыл то то, что ты ему говорил.  
Снабжать.  
В принципе уже.

**Pavel Frolov** 1:23:36  
Поэтому.  
Поэтому раз точно говорилось очень важно том плане.  
Что надо проанализировать, как правильно построить запрос, а не пытаться маленькими запросами постоянно нет. Здесь неправильно сделали по другому, неправильно.  
Чтобы.  
Спасибо ответить.

**Alexander Biratko** 1:23:56  
Да моя, потому что правильно задать.  
Вопрос, надо понимать о чём?  
Идет речь, потому что ну понимание проекта. Ну как минимум должно быть в голове у Того, кто задаёт вопрос.

**Andrei Bosik** 1:24:10  
Но, безусловно.  
Вот опять же сказал, а вот кодом.  
Чтобы он не терял контекст, там же все знают, что можно при начале работы попросить его сделать и нет. Он создаст себе папочку. Точка слэш.  
Пропал кот.  
Вот и я периодически.  
Прошу типа те вещи, которые действительно там?  
Будут всегда использоваться, например, да, то есть я могу.  
При сохранить себе там свою документацию, чтобы ты больше таких ошибок там не допускал, и он там ведёт себе м дешевую документ в этой папке точка.

**Pavel Frolov** 1:24:46  
А.

**Andrei Bosik** 1:24:51  
Наш кот.  
Иной, зачем это нужно?  
Обстоятельном поминать тогда листов?  
Потом там хранит все эти ошибки, очень так сказать.

**Pavel Frolov** 1:25:03  
Да, все правильно, ещё файлик, вот вот клодом, d его надо периодически.  
Просить проанализировать и обновить в соответствии с твоими.

**Andrei Bosik** 1:25:10  
Да да Да да да.

**Pavel Frolov** 1:25:12  
Пожелания.  
То, что следующий это не пропадет?

**Andrei Bosik** 1:25:18  
Да да, все верно.

**Val Levitan** 1:25:19  
Давайте давайте давайте сделаем паузу стоп стоп, так я прошу эрвин сделал паузу своё время. Я хочу, чтобы вы сделал паузу.

**Aaron Bockelie** 1:25:34  
Вот те руки.

**Val Levitan** 1:25:36  
А я сполз.  
Так вот они турчаку доска.

**Aaron Bockelie** 1:25:41  
Ай ай а вполне long рейтинг лидирует.  
Kraftwerk прямой.  
Так приятно.

**Val Levitan** 1:25:54  
Ромка.  
Как прошло?  
2.  
В Турции.  
Типологией брось торчал.  
И старый.  
Такой Александра шура Бендер ясенцом в мире.  
Бекон, вот вы ванты франсез мире.  
Из Дерек spires выкладку.  
Концовка иногда.  
Сначала сброд то что?  
Эксперимент выдал контент Windows.  
И.  
Смол английском 40 да и fuer going to континуальный контент.  
Данет сам point это был убит.  
Как абсолютный номер был с этот стол?  
Очень кстати километров общества крафту оболочек сплина.  
Под акк.  
Клиника.  
Андрей становой гончарам он explaining молчит улыбавшимся.  
Стопоря спад.  
Писать ответ вызов.  
Да поезде до конца.  
Почему?  
Недоступно.  
Ага.  
Был посвящен бат.  
Его радиатора компании.  
Это форсировать ул арахамии лайсенс прайс.

**Aaron Bockelie** 1:27:49  
Ясно.

**Val Levitan** 1:27:50  
Bad сом колониалист тулой до 40 сестер Спенсер контент будет.  
Да.  
Хватит долгосрочного резист вода.

**Aaron Bockelie** 1:28:08  
Я.

**Val Levitan** 1:28:11  
И и скотчем.  
Мол канте.  
Я.  
А а эта пещера интерес хуйлан заваров да контент Windows, фарфор, героин.  
Да да, привет.  
О 2.  
Тогда после партия этот лох и номера овр команды сью.  
Еще старта я натурал меры.  
Так.  
Скажем, аппарат будет старый, будет откошен и наконец, в мире аудио.  
Принцесса.  
About Irina and Evil and that discussion.

**Aaron Bockelie** 1:29:10  
I actually have it ready to show when when we want to hear and and Sasha this I put it in the chat.  
The commercial offerings of what I am building against, I'm building a small version of it that I can afford for myself and for others like you guys to potentially use. That is the that is the platform that's out in the world.  
Commercially, that's as close to what I'm building.  
Let me let's go back to the Igor and and Irina conversation, because I think this might help clarify what I was trying to tell you because I this is when Val said, hey, I think you lost them.  
So um.  
In this scenario, Igor has a Figma mockup. We have API backends to validate for tests and we have test procedures that are needed in JIRA.  
Just kind of like what we've got right now. So I mean, as the test director has to identify, you have to identify your data sources because you're going to think like a data scientist. Look, you have your test tube right here. You need to know that the Figma prototype is here and you can use Chrome dev tools to acquire this.  
The API specification, the device registry, endpoint, passport validation, hardware serial number, things like that. That's part of the git repo that you're working in where you're testing at. You have Jira test management tools, right? This is where you're tracking the actual test.  
Procedures and cases. And then you have a git repo where you have test files for automation of tests. You have maybe the React components and so forth. I'm I'm not saying it's all here and ready, I'm saying these are the ingredients that you need as a data scientist to think like this.  
To get moving forward once you know.  
The API specs, which is the feature definitions, the existing test patterns that you already have the labeled examples and the JIRA test execution results, which is the validation feedback loop thinking like a data scientist.  
You can then go through this flow. You can capture the Figma context. You can actually just ask a lot of pictures of this. You can map the API contracts, go look at the code repos and find the the data contracts for this.  
Then you can generate the test rocedures in JIRA.  
Have a test.  
Right.

**Pavel Frolov** 1:31:59  
Yes.

**Aaron Bockelie** 1:32:05  
In this framework, add the actual type test for this based on the data contract and API. Then you can run the test suite, verify the work and it's getting posted to the item to test.  
It means that from essentially the ingredients, you're answering this with functional actual test code and the test results, closing the loop to be able to then introduce this into here for people to check and for.  
Automated test results to work. So now you have the traceability between Figma to Jira to get to continuous integration. You have the labels for this potentially in the test code itself, and even better, possibly in the source code itself in docstrings for example.  
And then you have a feedback loo. Once you've established this pattern, you can now grow this and focus it and to kind of.  
Side way side on a side case address Sasha's concern is that you don't look at the whole code depot. You cannot consume the entire code base in one shot. It just there's no context space for that. You take a specific focus.  
And this means architecting and designing the code structure correctly. You don't write a 10,000 line monolith code, you break it into a bunch of small, no bigger than 500 lines of text code.  
And do an injection pattern for it, for example.  
I guarantee you that if you can't remember what you've written in the code once you've written it, like the general gist of what it is, it's also too big for a coding agent to to deal with.  
There is no way I can remember 50 different functions inside of a 3000 line block of code. I'll just forget I have to scroll up and down all the time and I'm only thinking about the first couple things and if I'm really good.  
I kind of know the whole thing, but as I walk away from it for a bit, I kind of forget again. And I think you have to be honest and realistic about what can you actually hold on in your own mind and then expect one of these machines to do similar.

**Val Levitan** 1:34:28  
Aaron, we we're going to lose them. Let's just stay, stay very focused because I really need.

**Aaron Bockelie** 1:34:31  
Sure.

**Val Levitan** 1:34:36  
Um.

**Aaron Bockelie** 1:34:37  
Well, I don't know how much more focused it gets than this. This is literally how Irina can do this.

**Val Levitan** 1:34:42  
OK, I just want to pause and I just want to ask them a question whether they have a question.  
Because if they don't have a question, I'll ask them to implement it for the next meeting.

**Aaron Bockelie** 1:34:53  
Sure.

**Irina Shishko** 1:34:58  
Oh, still it's still the ships.

**Ihar Hrybko** 1:34:59  
So.

**Aaron Bockelie** 1:35:05  
Uh.

**Val Levitan** 1:35:05  
Was Eli Elis Prasher it's your approach to living in the written AS leadership meeting.  
Их его тургор.

**Aaron Bockelie** 1:35:46  
Этой койкой говорит данные научил.

**Ihar Hrybko** 1:35:49  
Да да лицом берёз о я с Пикассо быть джон хэв энни опытный п. О свадьба с увы дунит мельницу коннект.

**Aaron Bockelie** 1:35:51  
Индекса.  
И.  
Do you have the source code that would create the API endpoints?

**Ihar Hrybko** 1:36:09  
Some kind of.

**Aaron Bockelie** 1:36:10  
Where is the? Where is the server code at?

**Ihar Hrybko** 1:36:12  
We have for now it's monorepo with front end and back end, so we have.

**Aaron Bockelie** 1:36:18  
And where is that monorepo at?

**Ihar Hrybko** 1:36:21  
Oh.

**Aaron Bockelie** 1:36:22  
Sorry to interrupt you. I just want to go quick, right? So.

**Ihar Hrybko** 1:36:26  
It's so.

**Aaron Bockelie** 1:36:26  
Is the model repo in get at least?

**Ihar Hrybko** 1:36:30  
Oh, it's located on the.  
M.  
A platform local game server I guess.

**Aaron Bockelie** 1:36:43  
Let's try an experiment. Open your screen share and open cloud code. Let's just try something.  
I just want to see what I see on your screen first because I don't know how this is going to go.

**Ihar Hrybko** 1:37:00  
OK.

**Aaron Bockelie** 1:37:10  
Sure that we have this completely locally cloned on your machine. Do you have it cloned locally yet?

**Ihar Hrybko** 1:37:15  
Yes, I guess so.  
Yes.

**Aaron Bockelie** 1:37:25  
OK, so so so this is a local gaming server. You're on a.

**Ihar Hrybko** 1:37:25  
So we can switch.

**Andrei Bosik** 1:37:27  
Mm.

**Aaron Bockelie** 1:37:32  
Infrastructure orchestration core, yeah.  
Let's I don't want you to use. I want you to exit this.

**Ihar Hrybko** 1:37:43  
What do we exit? Just.

**Aaron Bockelie** 1:37:45  
So just quit quit out of this for just a minute. Do you use VS code at all?

**Ihar Hrybko** 1:37:50  
Yes, I do.

**Aaron Bockelie** 1:37:51  
OK, let's go to that first.

**Ihar Hrybko** 1:37:54  
OK, so.

**Aaron Bockelie** 1:37:54  
Let's let's just open the project.  
Folder.  
Perfect.  
OK.  
Let's look at this folder structure on the left for a minute O we have.  
LGSUI packages set up UI and so set up UI is kind of the area where you were creating the right.

**Ihar Hrybko** 1:38:31  
The creative.

**Aaron Bockelie** 1:38:31  
The target again.

**Ihar Hrybko** 1:38:33  
I guess you are this is a folder where actually front end part is located. So yeah, tech technically we translating these prototypes into.

**Aaron Bockelie** 1:38:40  
OK, so the front end is in LGSUI.

**Ihar Hrybko** 1:38:48  
React components.  
And uh, this is.  
This lays it on the LG UI.

**Aaron Bockelie** 1:38:58  
And where is the back end services spread out in this code repo at?

**Ihar Hrybko** 1:39:06  
I don't know. I don't uh back end developer.

**Aaron Bockelie** 1:39:09  
Is it in this? Is it in this repo?

**Ihar Hrybko** 1:39:13  
Yes.

**Aaron Bockelie** 1:39:14  
OK, so one minute please.  
Is everything essentially in the common directory?  
Yes, no.

**Evgeny Kharetski** 1:39:27  
Mhm.

**Val Levitan** 1:39:29  
OK.  
Uh, which movers due to uh, I treated Nova Bros.

**Evgeny Kharetski** 1:39:41  
I don't understand your point, your point on.

**Ihar Hrybko** 1:39:42  
Oh, sorry.

**Evgeny Kharetski** 1:39:47  
So everything settle this right this is back.

**Ihar Hrybko** 1:39:47  
So everything except August UI is a back end.

**Aaron Bockelie** 1:39:51  
OK.  
Марина папы.

**Val Levitan** 1:41:38  
Гайс вор на гемблинг бизнес.  
Андрейкин bets.  
Вода карамкен дует, иногда он умрёт.

**Pavel Frolov** 1:41:58  
Планшет аккаунт.  
Лец festo фолата райт и текст вот вильдан, иван ауэр.  
Перекос айсинг евреи боди он же с митинг Андерсен different вот шут дидан.

**Aaron Bockelie** 1:42:17  
Most important thing. OK, so Igor, I need you to right click where it says platform local gaming server and in VS code right there.  
Right click right there. How do we open that locally on your computer? I need to get that folder open in in a Windows terminal.

**Ihar Hrybko** 1:42:39  
Oh.

**Aaron Bockelie** 1:42:42  
Maybe start by revealing explorer or something like that. OK, there we go. So right click here and I need to open Windows Terminal.  
And have you also set up cloud code in WSL or in bash on this machine? Or is it just OK? Can you invoke cloud code in this directory in that environment?

**Ihar Hrybko** 1:43:01  
Yes.  
Oh.

**Aaron Bockelie** 1:43:08  
Now you're doing it the same way that Andre did it the other day, which is broken. Are you sure you have your WL set U correctly?

**Ihar Hrybko** 1:43:15  
Yes.  
So we can switch just to.

**Aaron Bockelie** 1:43:18  
Oh no, that looks this looks OK, so you're in cloud code config. Yeah, so change directories to platform local gaming server in this terminal. This that'll look great.  
Oh.

**Andrei Bosik** 1:43:35  
You're not in the court. You will need to.

**Aaron Bockelie** 1:43:38  
I don't. You cannot invoke. You cannot invoke Claude code out of this or it won't work right. You have to change directories yourself to it. So no exit out of Claude. You're using it wrong.

**Pavel Frolov** 1:43:39  
Oh.

**Ihar Hrybko** 1:43:40  
OK.

**Andrei Bosik** 1:43:46  
I don't ask you to CG. Yes, yes. Slash. No, no, no, no, no, no slash. No.

**Aaron Bockelie** 1:43:49  
Go up one directory, yeah.

**Ihar Hrybko** 1:43:53  
Uh.

**Aaron Bockelie** 1:43:56  
No, there's two dots.  
dot dot. Yeah, there you go.

**Andrei Bosik** 1:44:00  
And use tab for type.

**Ihar Hrybko** 1:44:06  
Um.

**Andrei Bosik** 1:44:10  
No Linux.  
Machine.

**Aaron Bockelie** 1:44:32  
The first thing I want you to do once it launches is to type slash model.  
Enter. Make sure we're using the right model. Great. OK, go ahead. And yeah, so you can hit escape to get back. OK.

**Ihar Hrybko** 1:44:47  
Default is so OK.

**Aaron Bockelie** 1:44:54  
So I need you to just go ahead and paste this entire prompt into it all in one shot.  
And notice that the the ways and hooks isn't working right, so we might need to fix that before this works correctly, but it'll probably work good enough for now.  
Sasha, while this is happening, do you see?  
Each of these agents, including the main one, has 200,000 tokens of content context. This means the supervising agent has 200,000 tokens and each individual one also has 200,000 tokens. So you have a.  
Combined of 800,000 tokens of context here to work with while exploring the repo.  
The main agent is orchestrating the subagents to do the exloration.

**Ihar Hrybko** 1:46:11  
I think.

**Aaron Bockelie** 1:46:13  
Do you want to try stopping this and starting it again? Let's let's actually do that. I want you to hit escape.  
Multiple times.  
Let's stop all the way. We'll see the break stop.  
Again.  
Text slash config.  
Go into the config anel, go down to where it says verbose output and change that to true.  
Now hit escape to go back.  
Now paste the prompt and run it again.  
When you turn on verbose output, it's like kind of understanding its thinking as it goes along, which is really valuable. It's context for the human is what it is.  
See how it says thinking? And then it launches the three Explorer agents with what it's trying to do, and then it's showing all the commands that it's running behind the scenes to do this. And your job, Igor, is to click option two. Yes, allow access to just.  
You'll have to probably do this several times.  
Hit Yes.  
This is why I have a huge monitor with really high resolution because I can fit lots and lots of text on the screen to see what's going on when I do this too.  
I'm not narrating it because I'm sure you guys can just read as I can with what's going on. Igor, if you scroll up a little bit, you can actually see the other agents doing their thing too. It's kind of go down a little bit, like in the middle. Say your scroll bar. Yeah, there you go.  
See how it's finding all the different definitions of what they are.  
You kind of have to read through it while it's finding it.

**Ihar Hrybko** 1:49:42  
Yeah, I guess we have some scroll problem.

**Aaron Bockelie** 1:49:43  
Windows. I'll be honest, I'll be very blunt. Windows sucks for this. Use use Mac OS or Linux for this. It's way better so.

**Ihar Hrybko** 1:49:49  
Yeah.  
I guess it takes some some time because.

**Aaron Bockelie** 1:49:59  
But I understand we use the tools we have. It does. It's still going.

**Ihar Hrybko** 1:50:09  
I think it's only going for actual front end.

**Aaron Bockelie** 1:50:10  
Yes.  
No, it's going everywhere. I saw that when you were scrolling, you just you're only seeing the very bottom of the context and it's generating a lot right now. Look at the token usage count.

**Ihar Hrybko** 1:50:19  
Oh.

**Aaron Bockelie** 1:50:28  
Hit yes and don't ask again some more. Yep.  
So one of the first.  
The code base here is this information that it's discovering because it costs money to make these tokens and add the results as doc strings in all of your content. I would begin thinking about building a tooling harness for context acquisition that literally enumerates the doc strings in all of your code to be able to start understanding how the code works.  
So.  
I want you to note that the main supervisor agent only is using about 20,000 tokens.  
This is probably that's the output of one of the sub agents. So scroll to the very bottom. We're getting we're starting to see how the size of your scroll bar is getting really small.

**Ihar Hrybko** 1:51:41  
So we got.

**Aaron Bockelie** 1:51:51  
So hit yes and allow access.  
Now we're going to make a docs directory and it's going to start writing the documentation for this.  
So it's going to create a API data contracts document that defines how this is. The thing is, is that you need to really consider do you want to split your docs out of this? I would suggest start with this, but then eventually integrate them in the doc string and build some tools like some node tools or something like that.  
That they can generate the doc tree from the doc strings. This way it's always up to date whenever you're making changes to any of your code.

**Ihar Hrybko** 1:52:34  
Yeah, I guess we can.  
Oh.

**Aaron Bockelie** 1:52:39  
Give it a minute, it's not instant.

**Andrei Bosik** 1:53:05  
Oh.

**Ihar Hrybko** 1:53:17  
It.  
Claude is writing, but actually I don't see.  
Any files?

**Pavel Frolov** 1:53:30  
Common dots.

**Ihar Hrybko** 1:53:33  
Yeah, I'm looking into common docs.

**Aaron Bockelie** 1:53:39  
Don't go down one. There you go.

**Ihar Hrybko** 1:53:42  
No this this our docs.

**Aaron Bockelie** 1:53:42  
No.  
What branch are you viewing?

**Irina Shishko** 1:53:49  
Yeah.

**Evgeny Kharetski** 1:53:54  
Oh, finally.

**Ihar Hrybko** 1:53:56  
Oh, finally.

**Irina Shishko** 1:53:56  
But it is on their dogs.  
Mhm.

**Ihar Hrybko** 1:54:06  
OK, so we have that's the main read me.

**Evgeny Kharetski** 1:54:11  
It's still a preview only.

**Aaron Bockelie** 1:54:12  
Look at the architectural overview.

**Ihar Hrybko** 1:54:12  
So good.  
So they should deal like.  
Hello.

**Aaron Bockelie** 1:54:36  
Let's look at the architecture overview.  
Go back to Claude for just a minute. I'm gonna have you. I'm gonna share a prompt with you.  
Just paste that in a cloud.  
So what we're doing now is we're we're iterating, we're correcting things. We built the main output of what we're looking for, but we're making some more nuanced changes in here.  
While it's doing that, we can read this. So let's take a look what it says.  
So it's Apache Felix.  
With a couple layers here.  
Let's get going. Is this accurate so far?

**Ihar Hrybko** 1:56:06  
Some feedback from our developers, I guess.

**Aaron Bockelie** 1:56:10  
Right. So the trick is, is that it's not like like you can just press the output. You have to read it. I agree with this. Remember the third layer of the sandwich is to accept the output. If it's wrong, you have to correct it and then you.

**Evgeny Kharetski** 1:56:11  
Thank you.

**Aaron Bockelie** 1:56:25  
Until it's correct.  
It generally involves a lot more reading now than writing.

**Ihar Hrybko** 1:56:45  
You know.  
I will tell us to the Spark framework.

**Aaron Bockelie** 1:56:59  
Igor, can you can you accept changes?

**Evgeny Kharetski** 1:57:00  
Oh, Spark Sparkle, I suppose it's.

**Aaron Bockelie** 1:57:06  
Oh, there it goes. No, yeah, that's right. So go ahead and close and open these again. It'll render better.  
Create a new preview again.  
Oh, you don't have. You don't have one that renders a mermaid.

**Ihar Hrybko** 1:57:20  
No.

**Evgeny Kharetski** 1:57:21  
No.

**Aaron Bockelie** 1:57:21  
You need to get a. You need to get one of.  
Mark go to and then and search for a markdown. Yeah, mermaid.  
The second one.  
Yeah, so here's kind of the diagram to start with.  
So I want let's just scroll through this real quick 'cause we for sake of time.

**Evgeny Kharetski** 1:58:19  
No business service.  
Spark at no other source to be been working. Spark on the. What's it saying in Jets on us? What's the strike on Jets is.

**Ihar Hrybko** 1:58:44  
Mhm.

**Evgeny Kharetski** 1:58:44  
And pointer.

**Ihar Hrybko** 1:58:51  
Israel.  
Mhm.

**Evgeny Kharetski** 1:58:59  
No, Sir.  
Hardware plugins.  
Oh, the post.

**Irina Shishko** 1:59:11  
Mhm.

**Evgeny Kharetski** 1:59:19  
And if so, progressive plugin.

**Ihar Hrybko** 1:59:23  
Minutes.  
No.

**Aaron Bockelie** 1:59:36  
We kind of have a general description here. Maybe we could look at. Let's just Scroll to the bottom. I kind of want to see what the rest of it is.  
So shared workspace packages. Fine. OK, keep going. OK, let's go look at API data contracts.  
OK.  
So the data contracts for this start to look like this now is what I'm guessing.  
So you can see kind of examples on formats and endpoint registry.  
So.  
Where we?  
Things because actually it sounds to me like there's some architectural improvements that could be made to make this easier for the developer experience for Igor. If you had API doc endpoints for this, for example, that would be really nice to have. We don't have that right now, so we'll just use this.  
You can see how making some improve.  
What?  
Good test scaffolding.  
So we have a couple different types of tests we can run here.  
So we have integration and integration test, contract test, unit tests and so forth.  
These are probably proposed and I don't know if they exist yet or not. I'm.  
You know, that's up to you guys. I don't know your code base.  
Buddy.  
A robot or not?  
That's what I asked to do. I said go ahead and create a test scaffolding structure for everything because it would be.

**Ihar Hrybko** 2:02:48  
Oh, for.

**Aaron Bockelie** 2:02:56  
It would be incorrect or remiss for me to direct it to only make a test scaffolding for front end. Why would we ever do that in a real scenario?  
Right.

**Evgeny Kharetski** 2:03:10  
Let's see, let's see second. Sure. Irina. Irina.

**Ihar Hrybko** 2:03:10  
I think.

**Irina Shishko** 2:03:12  
OK.

**Aaron Bockelie** 2:03:13  
It doesn't mean that we have to build tests for everything. It just means we have to think about how the whole structure would look, thinking architecturally rather than solving the immediate problem.

**Irina Shishko** 2:03:15  
Yeah.

**Evgeny Kharetski** 2:03:17  
OK.  
Stop.  
Uh.

**Irina Shishko** 2:03:55  
Sure.  
So.

**Evgeny Kharetski** 2:04:06  
OK.

**Pavel Frolov** 2:04:06  
No.  
Yes.

**Evgeny Kharetski** 2:04:43  
U test.

**Irina Shishko** 2:04:50  
Not I'm but yeah and yourself.

**Evgeny Kharetski** 2:05:11  
No, is it?  
OK.  
Yes, if you.

**Ihar Hrybko** 2:05:27  
What was?

**Irina Shishko** 2:05:59  
So.  
That's not working.

**Evgeny Kharetski** 2:06:05  
OK.  
Yeah, yeah.

**Ihar Hrybko** 2:06:23  
So.

**Evgeny Kharetski** 2:06:29  
Just like talk with that.

**Ihar Hrybko** 2:06:30  
Just like so.  
OK.

**Irina Shishko** 2:06:43  
So now.

**Ihar Hrybko** 2:06:43  
Other.

**Irina Shishko** 2:06:53  
План, который.  
Тайга.  
Это полезный план.  
Потому что вытащить будет.

**Evgeny Kharetski** 2:07:11  
Как может быть правильным?  
Допустим.  
Условно.  
Когда у нас надо конкретно этого.

**Irina Shishko** 2:07:24  
Это.

**Evgeny Kharetski** 2:07:25  
Проектом.  
Какой-то документации или каких то какого то контекста.

**Irina Shishko** 2:07:31  
А ты то что сейчас?

**Evgeny Kharetski** 2:07:34  
То, что Сейчас мы обсуждаем, это то, что реально экране.

**Irina Shishko** 2:07:36  
Ты имеешь в виду то, что сейчас Игорь делал, я говорю, самый самый первоначальный план, где арен сказал, чтобы нам реализовать. Вот мы там создали в джиро мы взяли figma, мы взяли это самое список айпи мы взяли ещё что-то, мы это всё вместе постепенно как бы соединили и на выходе мы получили тесты.

**Evgeny Kharetski** 2:07:38  
Да да да.  
Да.

**Irina Shishko** 2:08:03  
Я вот про вот этот большой плат сейчас как бы что что сделал Игорь это по ну по мне бы как я поняла была цель.  
Вытащить из баклэнда.  
Вот как раз всё то полезное, что нужно, то есть айпишники для Того, чтобы имея пользоваться.  
Мой.

**Ihar Hrybko** 2:08:27  
Потому что.

**Evgeny Kharetski** 2:08:33  
Вот.

**Ihar Hrybko** 2:08:34  
Рельефа, да.  
То мы как бы пытаемся её каким то образом собрать.

**Evgeny Kharetski** 2:08:37  
Мы как бы пытаемся ее каким то образом попали.

**Irina Shishko** 2:08:40  
Угу, то есть нет, сходя и открывая каждую этап файлик и смотря ага, чтобы вот это сделать, нам нужно копипасты.  
Вот мы вот это будем.  
А то есть попросили Клода и он нам оттуда.  
А он очень много щипнут.

**Ihar Hrybko** 2:08:58  
Далеко не все далеко не все.

**Evgeny Kharetski** 2:08:59  
Ну вообще он даже ну хорошо, если процентов 20 вытащил.

**Irina Shishko** 2:09:00  
Что?

**Ihar Hrybko** 2:09:04  
Я думаю даже меньше.

**Irina Shishko** 2:09:04  
Но возможно, здесь просто не нужно так глобально сразу все искать, а нужно более как бы.

**Evgeny Kharetski** 2:09:08  
Тот тот тот.  
Тот, чтобы реализов.  
20 плана рон, мне кажется, что просто хорошенько поработать с клодом насчёт Того, чтобы описателя книжки.  
Только потом попросить его, это всё с компоновать в одном месте, чтобы по этому чтоб вот это скомпонованная вы могли использовать потом.

**Irina Shishko** 2:09:26  
Хм.  
Но опять же это.

**Evgeny Kharetski** 2:09:33  
В своих задачах.

**Aaron Bockelie** 2:09:36  
Игра эфир.  
Рапс, протекающего силы.  
Чтобы пою песни отстаю а?  
Я да он Райдер.

**Ihar Hrybko** 2:09:58  
Давай.

**Aaron Bockelie** 2:09:59  
Я сплю.  
Она такая программа презентующим таящею.  
Different things. So I just downloaded it. If you want to, you can double click it to open it and see.  
Here. OK, so now just remember that that's there. You could probably remember that path, so it's under users, blah blah blah.  
Andre, can you note that path so we can help Igor have get a reference to it for cloud code. So go back to cloud code.  
Hit yes to allow to edit its own settings.  
We need to get your way system, my way system working because it'll inject a lot more useful context in this right now. So we're going to, we're kind of running in a very simple mode right now rather than being able to express architectural design, things like that.  
OK, so next I need you to uh.  
Take that next prompt that's in there in the chat that says now that we've finished or I'm sorry, let me paste this in. Hang on.  
So that's the next prompt to use. We need to edit this slightly to give it the full path to that test director workflow HTML file.  
Arrow up to the top. Andrei, can you help him get the full path to that? Navigate him through it?

**Pavel Frolov** 2:12:10  
I.

**Aaron Bockelie** 2:12:10  
Because it's on his desktop of his your machine right now so but it you have to do slash mount slash see.  
Blah blah.

**Ihar Hrybko** 2:12:19  
Uh.  
What the hell?

**Andrei Bosik** 2:12:20  
Even on the.  
Still team was.

**Ihar Hrybko** 2:12:30  
No, we get it also. Option. Sure, I'm going to come to support.

**Andrei Bosik** 2:12:30  
Still, as you can.  
Control set.

**Ihar Hrybko** 2:12:41  
Su повисла походу.  
Просто ничего не происходит.

**Andrei Bosik** 2:12:45  
Контроль цен не срабатывает.

**Ihar Hrybko** 2:12:46  
Не срабатывает ничего.

**Aaron Bockelie** 2:12:49  
Игры скептик прорыхлён аутсайдер.

**Andrei Bosik** 2:12:51  
Попробуй тайских нажми, чтобы очистить.

**Ihar Hrybko** 2:12:52  
А оценки.  
Комплект ли?

**Aaron Bockelie** 2:12:56  
Это такая питерская.

**Ihar Hrybko** 2:12:56  
О.  
Но ведь комплект легенда.

**Aaron Bockelie** 2:13:00  
Но.  
Al al да это вы сказали.  
Пал брикен а этот пыл и broken кончился, и мото пытаемся.

**Ihar Hrybko** 2:13:12  
Наук.

**Andrei Bosik** 2:13:14  
The console says it's not and escape not work too.

**Aaron Bockelie** 2:13:14  
Held down escape doesn't work.

**Ihar Hrybko** 2:13:17  
Nope.

**Aaron Bockelie** 2:13:19  
So just close it and we'll just resume the session. It's fine. No, not minimize. You got to close.

**Andrei Bosik** 2:13:22  
Yeah, I think you need to run new session.

**Aaron Bockelie** 2:13:26  
Just starting. Yeah. Well, yeah, OK.  
So give us back to the directory.

**Ihar Hrybko** 2:13:33  
I need to start.

**Aaron Bockelie** 2:13:34  
Baud space dash dash resume.

2:13:41  
Yeah.

**Pavel Frolov** 2:13:43  
Mhm.

**Aaron Bockelie** 2:13:44  
Yep, enter.  
Give it a minute.  
Enter.  
OK, now take that prompt I shared.

**Andrei Bosik** 2:13:58  
Hmm, interesting comment.

**Aaron Bockelie** 2:14:06  
Yeah, you've got some issues with pod code. Do you see the errors and warnings in the corner? So you got you got some work to do, Andre. You gotta get this stuff fixed.  
OK, add the the mount. See. Yep, you got it going.

**Pavel Frolov** 2:14:23  
Actually if if you start from.

**Evgeny Kharetski** 2:14:30  
When you press the desktop, users just talk to the smell.

**Ihar Hrybko** 2:14:34  
Oh.

**Evgeny Kharetski** 2:14:35  
Oh.  
OK.

**Ihar Hrybko** 2:14:44  
Um.

**Andrei Bosik** 2:14:58  
Focus slash.

**Ihar Hrybko** 2:15:01  
Mhm.

**Aaron Bockelie** 2:15:02  
It's case sensitive, right?  
OK.  
Yes, allow.  
Think because it crashed, it didn't save it settings for showing the thinking, so we're not seeing the the thinking right now.  
But basically, OK, so then once we get this.  
You can actually paste this into the prompt while it's still running if you'd like.  
Just hit enter.  
Hit yes to allow claude.  
So by using pointers to point to the documentation in the repo rather than in the dot cloud directory itself, it makes it more flexible because now if you were to set up docstrings and other tools to generatively create the documents procedurally from code.  
Then all the instructions will just update all the time and creating a tight loop of of connection here. Uh oh, looks like we dropped the connection for some reason. Oh, there it goes.  
So at this point, what we've done is we've traversed the entire code base. We've created a high-level overview of understanding of the code base. We've established a set of initial expectations for how testing should look.  
We've created a set of instructions for Claude. The next time you start, it will load and understand how to work and think. And finally, once you can get the Waze configured, we'll be able to leverage architectural decision records.  
And either back port them into the code base or begin creating new ones and sort of evolve this a little bit so you can begin to use these tools more effectively without having to type stuff in all the time. It will acquire the context on its own rather than having to do this.  
I would say if you were to commit this right now, you could just ask Igor, you could ask Claude to just let's do it this way.  
Just say please commit our create a branch, commit our changes. Just do do that with claud.

**Ihar Hrybko** 2:19:21  
I think do we actually need this kind of structure?

**Aaron Bockelie** 2:19:23  
Yeah, it's just a branch. You you could delete it. We'll leave it as it is for now. All of this is temporary, right? If unless you want to actually keep it. So just just say that.

**Ihar Hrybko** 2:19:26  
Oh.

**Aaron Bockelie** 2:19:37  
Not going to tell what the branch name is, we're just going to just do it.  
O It looks like you have various tooling problems you need to fix on your computer.  
So hit yes.  
Andre, I want you to take note of these failures that he's got right now. You can use Claude to fix them too.

**Andrei Bosik** 2:20:23  
Sure.

**Aaron Bockelie** 2:20:42  
Oh no.  
Yeah.  
We may not be able to do this until we can fix these.

**Val Levitan** 2:20:54  
Why are we getting errors?  
Explain to me.

**Aaron Bockelie** 2:20:59  
Yeah, let's just say it.

**Pavel Frolov** 2:21:05  
Get, get, get all of us, for example.

**Evgeny Kharetski** 2:21:14  
You only want.

**Pavel Frolov** 2:21:17  
OK.

**Ihar Hrybko** 2:21:17  
Uh, no bad. That was.

**Val Levitan** 2:21:19  
OK, please, please fix it. We will continue tomorrow. I sent. I sent invite. I want to focus on this thing.

**Evgeny Kharetski** 2:21:24  
Yep.

**Aaron Bockelie** 2:21:29  
So.

**Val Levitan** 2:21:37  
Oh.

**Ihar Hrybko** 2:21:38  
No.

**Irina Shishko** 2:21:42  
Mhm.

**Aaron Bockelie** 2:21:46  
So.

**Irina Shishko** 2:21:48  
Uh, Alexander.

**Andrei Bosik** 2:21:49  
Alexander.

**Val Levitan** 2:21:55  
OK, pretty good still.  
OK.  
Aaron, we have another meeting with Clayton right now.

**Aaron Bockelie** 2:22:11  
Yes, just briefly before we quit, Igor, I want to put the cherry on the top on the effort that we've done here. Can you please exit out of Claude and start a brand new session?  
And I just want you to paste that last message in there, because this kind of addresses Sasha's concern about where's the context go. It also establishes the examples I've given you through this whole talk about how it actually works now.  
We can simply ask, let's review how we're going to build tests for our front end. Just give me a brief summary and because we have all of this context that's now stored in the code base along with it, it's able hopefully to retrieve this. It looks like it's not even getting any tokens.  
Moving.  
It'll give us, it'll give us a overview of our method of doing this and it will stay consistent once you've committed and merged and everything else with every all the other code.  
It looks like we've got problems right now, so maybe we're not going to get it, but it'll eventually come up once you can get inference in point. Once the API server comes up, maybe you've got to disconnect on network or something right now.  
All right, let Valitz, you want to jump over.

**Val Levitan** 2:23:31  
Yeah. Thank you, guys.

**Aaron Bockelie** 2:23:33  
I hope this was helpful. I will get. I will get the docs those this the visuals sent to you OK.

**Ihar Hrybko** 2:23:33  
Thank you. Thank you.

**Pavel Frolov** 2:23:33  
Yeah. Thank you.

**Irina Shishko** 2:23:34  
Yeah.

**Evgeny Kharetski** 2:23:37  
It.

**Pavel Frolov** 2:23:41  
Yeah, thank you. Bye.

**Aaron Bockelie** 2:23:42  
Bye, bye.

**Evgeny Kharetski** 2:23:42  
But.

**Irina Shishko** 2:23:42  
Thank you. Bye.

**Dmitri Kovalchuk** stopped transcription