# Raw Transcript — Clayton Chancey — Jira MCP demo and toolset direction (with Lena, Aaron)
**Date:** January 29, 2026, 10:01 AM Eastern
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Summary note:** [[Meeting_Notes_Clayton_Jira_MCP_Demo_and_Toolset_Direction-January-29-2026]]
---
00:00:01 Michael Gottlieb
That's crazy. Yeah, I have friends, because I just moved to the Los Angeles, well, I moved back to Los Angeles, but I spent six years in friends who were based in, snowed into their house. The state doesn't really have sufficient resources to deal with that, like, say, in one, you know.
00:00:36 Speaker 2
All I'd like is to start for instance in the New York City, I like the local island, and they never had it.
00:00:45 Michael Gottlieb
The captain is joining, get the hold.
00:00:56 Val
Okay, morning, everyone. Somebody please record this call. Yeah, and then circulate the transcript. Yes, I shall do that. This meeting is not mine. I'm going to mute myself. Thank you, everyone for joining. I believe it's Clayton who's gonna run the meeting. And yes, I'm going to be in the background. Thank you very much. I'm muting. That's good. I wanted to certainly do something that I think is a good starting place, particularly for you later. But I think we can.
00:01:42 Michael Gottlieb
I built an MC added many of them. to hold on. That's the perfect time to call.
00:02:01 Speaker 4
Ah, yeah. There we go.
00:02:09 Michael Gottlieb
This particular tool is called Game Status, and it will go into your JVL JIRA in context of what you do, conversations baked into it. And so a boilerplate Banilla can get lots of information without having to consume many tokens because a lot of it, we've already put it into the tool. And the things that we're now about to make.
00:02:39 Michael Gottlieb
in our ATI request to get real-time data in JIRA. As we can get information, turn this information in a sync, pretty contextualized. I realize that this tool is probably... level and we used to do that i just wanted to show you the main concept that it can, one game status it can well one tool call is making many api calls that are baked into this.
00:03:15 Michael Gottlieb
only using token it can get total completion it understands the concept of these games how marketers stories that there's a certain hierarchy discussed here's the different variants that exist the market status completion and then the number of features and how many of them and then it understands the difference between omni and rage tells you what's in progress the, filled variant for georgia started so in my mind this is sort of representing a lot.
00:03:55 Michael Gottlieb
Zero. And so I wanted to just pause right there and say, I mean, does this actually feel accurate? Does this feel like the type of task that you spend any time doing and is it useful to then serve and continue to build it out and give it to you.
00:04:23 Speaker 2
It's definitely useful for a status review and very useful. I like it. I use it. How to connect this MCP? I need to ask our IT guys. And they use a token, right.
00:04:47 Val
I want to chime in. I'm sorry. I want to chime in. Let's stop making reference to tokens. I don't care. I simply don't care, and I don't want to hear about it. To me, it's not a subject that we need to discuss. That's number one. Please, please don't save money on tokens. Number two, I want to comment on this. I'm using this, I'm using Aaron's MCP. I have generated a prompt. I actually asked Claude to help me generate the prompt.
00:05:22 Val
I shared this prompt with Elena. She's welcome to it. I'm using this. I'm using very similar... I get very similar reports by person or company-wide. It works. It's amazing for me. For Elena, I don't know, because she knows it by heart. She swims in that water. It's hers. she doesn't really need it. I need it. She, I don't know. What she spends a lot of time on is.
00:05:58 Val
entering tasks. That takes so much time.
00:06:04 Michael Gottlieb
So this is a completely from scratch, brand new. And then I implemented.
00:06:35 Michael Gottlieb
this game status tool that I just demoed to you. 19 minutes. So one of the things I want to show you is how trivial it is. Completely researched. All of this text is handled and Jira will show you how. actually researched and validated the conversation from our transcript last working session in cloud code in the cursive self-include here so what this what this is a very all edit write.
00:07:14 Michael Gottlieb
delete tools it's a read-only version purpose of this demo and then my hope is that by the end of this call i can they exist that are basically automatic documentation take a take up products, create all the complex pages create all the stories automatically in one go pretty much as quickly as we just got status because all of those same calls are the same things that.
00:07:45 Michael Gottlieb
we're doing in a read-only version here to get the status of the games, So this is the reverse version of what I think we are trying to create. So I'm demoing the reverse version to try and be safe. And then by the end of this call, I want it to be very transparent and make it read-only. And I think it would really change your life, Lena, because as you mentioned, this type of standard.
00:08:22 Speaker 4
Something else that I heard, I mentioned that you're using blind still. And I need you to step back away from that and just use the standard. So what I'm getting at is to simplify the tools back. the basic the mcp tools that click the building can be shifted different it really now just has.
00:08:59 Speaker 4
a lot more to do with just having conversations what you're doing and then taking that internal, logic of the mcp server which is actually what's giving us the intelligence and then finally you, mentioned how it is kind of just don't take an absolutist perspective on i will use this tool there is no reason to simultaneously get the thing and have it all sort of work with it.
00:09:29 Speaker 4
once you get comfy to make sure that what is the level of using it just like what's like showed here that you can sort of debate to make it easier for you don't create it.
00:09:49 Michael Gottlieb
a big button that you push to get okay let's move on let me show you what are useful i won't go into like super depth about a methodology that i use but just to just to show you there's a there's a here um so first i created a mcp server that's the things that are available of course this is.
00:10:20 Michael Gottlieb
on the jvl github instance which i got access to the same time val met three hours ago to say hey do you have access i woke up got access to created this mcp and then immediately what i did. to load this mct server that clogged just for itself so it can test itself and then i said hey.
00:10:56 Michael Gottlieb
your very first task is to go research here's the transcript discussing here's a transcript, validate or invalidate or supplement everything we discuss actually going into the source of truth which is jira and you have all these tools that will let you do that and so it went in you know maybe 10 15 minutes overview hierarchy these are all just discovering basic validating the idea.
00:11:31 Michael Gottlieb
that yes you do have an initiative feature which is what we discussed the value streams here's the initiative patterns the structure information but then, It also went down, and it looked at things like feature templates. Okay, here's the standard feature template that we're finding. Game production, complete list, feature list. And so it's going through, looking at all lists,
00:12:04 Michael Gottlieb
finding an example of the template hierarchy.
00:12:07 Val
Bravo, bravo.
00:12:10 Michael Gottlieb
And then here's where we see, oh, and at the end, I think this is also interesting because, Val, you mentioned that, I think what is that it is less organized than Jira, but there is a method to the madness. There is like, there are opinions baked in. So, in other words, I think what I've seen is that there is a, to validate everyone, there's a lot of people going in and manually repeating the same documentation from client's person.
00:12:46 Michael Gottlieb
over and over again because it's all manual also lots of but it seems like the humans have the same general structure of what this should look like there's a thing that by using an mcp server.
00:13:03 Speaker 4
we can reduce that variance i don't know if it's still being used actually brought but you know how you get that smell of people are using paid structures they've been doing that for a long time i don't know whether that's still done or not or whatever but that might be contributing to what you're sort of struck okay so some automations might be yeah i don't know if.
00:13:36 Speaker 2
it's a huge mystery i don't know who runs it.
00:14:03 Val
I just want to quickly comment that we want countries to migrate to Github. I'm gonna park it there.
00:14:20 Michael Gottlieb
Yeah, I mean, I think that adopting these kinds of tools is a working whole way to do that, because you need an adopted way to actually get all that. I mean, Github somehow. if we can adopt these types of tools like the one this one is like specifically being developed for this game design use case and if people have those those type of tools then it becomes just an ai.
00:14:58 Val
migration all right so so our goal is to convert it into dot md and park it together with the code, with the developers code next to the developers code big big sorry big into the developers. already as we correct as we migrate to omni we migrate to github and wedge it.
00:15:31 Val
together with the developers code the qa and everything is need to be we've.
00:15:42 Michael Gottlieb
okay continue it's about your tools okay so let me just talk through this and i think we're already we can talk about next steps here so first of all these are the tools that claude i think at the entire instance recommended that we should create based on the transcript it first said.
00:16:13 Michael Gottlieb
the philosophy here is to embed domain knowledge into the mcd in other words generic tools but to use jvl game designs so that you don't have to do any cognitive work using natural language queries and you don't have to think in jiro versus xyz world you're directly to claude desktop. Exactly what you need, and so that the conventions for how we want this to be structured don't have to live in your head either.
00:16:49 Michael Gottlieb
You don't have to get, like, Val's vision or your vision. Translate it all. And you just speak, and then what comes into existence is in this universal form. So the first thing it suggested, and this is what I just demoed. What made this suggestion, like, 15 minutes ago, 15 minutes before the call, I implemented it, tested it. We hopped on the call, and I demoed it to create a tool called GameStats. And when I committed to this repository, I marked this as done.
00:17:22 Michael Gottlieb
The status is now implemented. The purpose is to answer, what's the status of having used your input, output, here's the behavior, here's what it thinks the code should look like. And so that's implemented. Now, here's another set of tools, and this is what I want to do so that I can then, as you onboard and use them, I am able to. I actually think, by the way, it might be useful for me to just go ahead with some of these before you get this tool,
00:17:59 Michael Gottlieb
since I can probably do it in the next hour. And I have a lot of experience with Aaron, where Aaron and I are knowledge sharing. Aaron is building a tool. I go ahead and download it, start using it, and then he rolls out ten new features that are really cool, and now the work that it would take me to actually go and reinstall this tool is like, well, I should. So I think what I want is just some of these tools and figure out, do these make sense to you as a, one would be to create a game.
00:18:39 Michael Gottlieb
And the idea is to generate the feature and story structure of a new game in one go. And the inputs would be the name of the game, LRS market, initiative, and then if there's a particular time. And these do not need to be filled out by fields. You can describe it, dictate this information, claw it, because it's AI. You can be sort of vague.
00:19:09 Michael Gottlieb
I mean, it needs this information, but you can provide it in whatever. And then the behavior would be that it creates a prep initiative. It generates standard features based on the template of what it knows. It generates standard stories under each feature. It applies all the naming conventions, and it sets up the relationships, blocks, based on everything it knows.
00:19:52 Speaker 2
That's a good question.
00:20:00 Michael Gottlieb
So that's exactly the kind of thing I'm trying to discover. I think we can solve for that. So let me say to you what I think I just heard. The ideal pattern would be that you provide this input, which is but also to clog. In some way, you need to provide some images, and those images need to make their way into the JIRA ticket as, is it attachments or is it embedded within the description.
00:20:32 Speaker 2
Yes.
00:20:40 Michael Gottlieb
For game symbol, you have combat, and also the yellow and the yellow.
00:21:24 Speaker 4
The issue types, the template types, everything else, like what is a project, it didn't make sense to do it with AI tools, very deterministic, I was basically getting to the point of here, run this, and it will create this. through api under but i think that taking the conversational like let's go to let lana negotiate, with building the plan first and then say okay i think i'm ready go ahead and build everything.
00:22:00 Michael Gottlieb
yeah and i think that the images thing thinking through it live i think there's more we can do that and what's best for using this like and i can test this out a little bit i have a jira instance it's not that jbl is posting images to the discipline and so with these lana would.
00:22:32 Michael Gottlieb
these be like ai generated that's like in a folder or desktop or something and then you're.
00:22:42 Speaker 2
Like, we are using AI-generated code to create, but it's never just raw AI-generated. It's always consistent, it's pretty complex and very detailed, I would say, for each, like, for each method of the game. It has, like, a different position of elements, color, schema.
00:23:27 Speaker 2
But, of course, some description I need to enter manually, like animations. How do I know what animation is a symbol of that? Let's, let's... But yeah, the structure, if it would attach at least to proper story, like proper image from my folder, I will name them. So, for example, if it's La Rosa, a symbol, Goldenback, La Rosa games, a symbol, Goldenback, at least attach proper story, then I can add animations.
00:24:07 Michael Gottlieb
Are the images, are the images, the descriptions I don't care about because that's just text that we can get out there, but are the images like compressed image formats like JPEG or PNG.
00:24:26 Speaker 2
Yeah, JPEG and PNG, and PSD files, which are usually games, I look at and...
00:24:52 Michael Gottlieb
That's good, because those can be as binary in the worst-case scenario. That makes it easier. Okay, I'll get to work on that, and we can test this out. One question about this would be, if I want to test this create game from template safely,
00:25:29 Michael Gottlieb
is there a way to do that in the JVL instance where we can do that meaningfully? Should I just use a naming convention like test? Would we need a copy? like the IP and the AHA to a test version or what? That might be a question maybe more for Dimitri or Jirad.
00:25:52 Speaker 2
You might really get some sandbox. Remember, Aaron.
00:25:57 Speaker 4
Yeah, we would have to ask Andre to recreate the sandbox.
00:26:02 Michael Gottlieb
I can do that. I have his email, so I can just actually just take it.
00:26:15 Speaker 4
Right now, we're talking about something that's pretty direct. So, Lana, you're saying, hey, I have all these pictures. Maybe they're in GitHub. Maybe they're in GitRepo. Maybe they're on MyPen. Then you have to negotiate, Claude or the AI, to decide what it's going to look like to do all the items. One of the things that I would be very careful about is that when you have that conversation like that in chat, it will be lost.
00:26:51 Speaker 4
There is no context about how that happens. And one of the things that I've pushed for you guys to do in the art and the development team and the production team is to try to use GitHub for the comments, commenting on issues, commenting on pull requests, and other types of things like that. And the very same MCP server that Clayton, we can prototype here and I would call it ad hoc slightly because basically you're going to let it go and it does the thing.
00:27:25 Speaker 4
The very same MCP server could be connected to a bot instead of GitHub where the cadence of the conversation is written. And you actually have the ongoing and then basically negotiate back and forth that way. Both of them can negotiate with. on because it can just pull the trans conversation in github and eventually you can approve it or transition it on onwards uh creating it yeah we are doing actually for a project but because we don't.
00:28:00 Speaker 2
have too many only projects for now only that's what we did when we commented everything was commented about it and i also hope we did one for fire but because for now all our projects.
00:28:27 Speaker 4
i feel like i've said it a lot so far is aim for where they will be not where it's at. I think we need to hit the ground running on one thing, and what I'm seeing with Clayton's tool here, he's suggesting that you use it as absolutely the right thing as the training wheels to get going, but don't forget, I think you need to be moving, start leading your target.
00:29:02 Michael Gottlieb
I wanted to ask about the value of this other additional, Claude suggested this, but I don't understand the use case deeply enough to know if this is valuable. Claude suggested cloning a game for a market with adaptation-specific structures and structuring the JIRA content differently for a different market, taking the key, the target, creating a new adaptation for its main scene, pay table, etc.
00:29:39 Michael Gottlieb
Is this something that is currently a lot of work.
00:30:20 Val
I'm against manual deletion. And I'm against...
00:30:26 Michael Gottlieb
Well, I was just going to clarify saying manual.
00:30:30 Val
Yeah, she means manual. She means manual.
00:30:34 Michael Gottlieb
These MCT tools that already exist... Let you do all of that as well through manual, through a natural language. So what we all are going to give to you is in addition to these, the tool that I showed you with game status, the create adaptation, thinking about doing, in addition to these, you can also have a conversation about specific things.
00:31:07 Michael Gottlieb
You can say, I want to look at this one ticket. Give me all the time. Oh, delete anything related to X, Y, and Z. Yeah, and I think that removes the actual manual effort because you're not actually interacting.
00:31:41 Michael Gottlieb
and then it is going and doing all that very quickly. So the idea is that there should be a balance of granular tools that let you do specific actions like you would in JIRA manually, and then tools that are broader. It's almost like a combination of all. Val, you.
00:32:00 Val
I want to take you back to the original question you asked. It's screened here. You said you don't understand the clone. Yeah. I think it's extremely important for us. It's a pivotal thing. We do it all the time, create clones for other markets. So let's say we found an interesting concept that works in one market,
00:32:31 Val
even to the point that the math is successful, and we create a clone based on the math or based on... the main character or based on something else or based on main game but we create clones all the time it's the essence of our existence we cannot create fresh content we create clones most of the time and rarely we create fresh content but but creating a clone is the essence of our business.
00:33:06 Michael Gottlieb
right but what i'm hearing lena say i'm sorry to interrupt usually for artists when we call.
00:33:17 Speaker 2
a game because we need to it get like mass and game functionality is blown but for us we need.
00:33:25 Val
to create all these assets today today you're right but if it's properly automated cloning is a superb way of multiplying.
00:33:44 Speaker 4
i think that when you clone things you're kind of using a type of ad hoc.
00:33:48 Speaker 2
oh for issue structures sure yeah for issue structures yeah you need the same structure but different names like for example this was like lion reaches was like seen by sam savannah and so now we are cloning it and making it same structure of issues are the same bonuses are the same functional same so we need the same like list of features and stories but with different names and different.
00:34:19 Val
schemes the frame the frame of the game is the same the math is the same the duration the timing is the peaks and valley of the game is the design the music the tone is different but more same phases.
00:34:38 Michael Gottlieb
so then what i'm hearing, The create adaptation motion should be there. What we should do is we should clone the existing implementation, but we should clone it in a way that makes it easy for the artist to not have to curate all the JIRA stuff. All of the functional, technical, logical design,
00:35:08 Michael Gottlieb
not graphic design, but game design choices would actually be cloned, but we should use Claude to then add the thematic choices and let the artist say, well, we're making a clone, but we're changing the theme from X to Y, and maybe Claude should actually add before it makes all those changes. Okay, I'm going to create an adaptation. Let me check. Is there any theme changes that you're trying to do?
00:35:38 Michael Gottlieb
You can describe that as so, and then when it creates this clone, it removes in savannah themed elements from the textual description and replaces it with either a placeholder to be determined inside and it's a mexico being that it actually incorporates that language automatically it's sort of cloning in a sense but we're using ai to go ahead and do all the edits that you would now do manually after client not not only not only that at the point.
00:36:13 Val
when we clone something there is a massive amount of being the game producer and the director of. design which is lena so the two of them, are discussing to nausea what theme lena is concentrating on producing com part, texture, coloration, hues, tones, it's a massive amount of design that Lena physically by hand is producing right now, it would be phenomenal if we could, and eventually I believe it's possible, from description to bypass Lena's manual work of comb parts and start suggesting a number of different comb parts, direction for comb parts, direction for overall design, direction for texture, etc.
00:37:14 Val
And if it's not possible today, it will be possible in a year.
00:37:21 Michael Gottlieb
Yeah, I mean this is, I think, in my mind, I'm thinking now a bit futuristically, not something that I can build you, I'm thinking this actually becomes a foundation, because Jira and eventually GitHub should be our source for planning the work. And then these elements need to now integrate tools that are diffusion models, basically, to generate digital. So if you're talking about, like, taking a texture from, you know, we have a texture standard for texture,
00:37:55 Michael Gottlieb
and now we need to auto-generate it with a different theme or something like that, we need to use a diffusion model. We can't really use a generative model, at least. And so we need to then integrate Adaptation Pro, which is generative AI, or a large language model, MCP tools, to integrate it with some diffusion models, like Gemini, Nano. We can't really meaningfully have images be generated unless we're generating the project,
00:38:28 Michael Gottlieb
the text descriptions first, because those become the prompt basis. So this becomes the foundation of building any actual.
00:38:40 Val
And another point, another point, I just want to make another point, is that we are now working on JVL's school of game design. And that is the foundation for JVL's truth. So everything about character behavior, sizing, dominance on the screen, contrast, everything is discussed between Lena and the game producer verbally by the game producer.
00:39:16 Val
Because our game producer is not a hands-on individual. He is a vocal individual. He expresses himself vocally. That conversation needs to be recorded and turned into JVL truth, which later needs to become a guiding principle for co-part design. or for theme design, anything that's being designed, there's always a verbal reasoning of why Lena produces certain graphic a certain way.
00:39:47 Val
She just doesn't do it. She listens to the guidance of a game producer whose only instrument is vocal elaboration. And if he can vocally explain things over time, this truth accumulates, and we can start relying on it, for producing handouts, quidem.
00:40:21 Michael Gottlieb
Yeah, so transcripts, that's another reason to use the MCP tool out of the box. And we have to, I need to build these MCP tools, and then Lena... probably Aaron and I need to have a session. We could probably do this next week. We get this working for you, a little bit of a, here's how to use these with transcripts of your conversation with your game.
00:40:53 Michael Gottlieb
producer. So you take those, and Aaron and I might have specific tool opinions that don't really matter that much, but the core loop, record, transcribe this conversation with the game producer, give it to Claude with this MCP in place. Here's how you scaffold those transcripts so that they build up over time. And then I have this instinct to refer to you about it because that's the.
00:41:26 Michael Gottlieb
name that shows up. so uh so accumulate those transcripts in a way that claws understand the cumulative time of your conversation and then all fuzzy conceptual design language that's in the translator should use this tool and cut the chair so you don't have to do all the work it's basically you don't have to engineer.
00:42:00 Speaker 2
your project like like again like uh i did not hear yes like when you uh image generated so, before we use chat gpt of raw and i was very because i think humans i can create and inside this project it's uh learning and learning my style like each nest like uh illustration.
00:42:30 Speaker 2
It's the same style I described. I love it, so I don't know. Because Adobe AI is my favorite.
00:42:42 Speaker 4
So let me put a cherry on top of what Clayton was saying, is that consult with Mr. Axford, who may have some ideas about the idea. I joke a little bit because basically the process that I've given Valve for saving them, considering them, building output from it, and make it accurate is pretty much identical to the same thing.
00:43:15 Speaker 4
that Clayton is going to be doing. We're all incestuous about what is going on in the same process. The second thing is that you've gotten comfortable with ChatGPT being able to create images for you because you...
00:43:43 Val
And that's the key. The emphasis should be made on you were captured by an open AI ecosystem. You are a victim to that prison.
00:43:59 Speaker 4
And we would rather build our own prison where we can open our own.
00:44:05 Speaker 2
Okay, but what kind of image generated do you want to use now.
00:44:09 Speaker 4
There are many kinds. I will leave it at that.
00:44:13 Speaker 2
Oh, starting from February 6th, we need to use something because our subscription is going to end. We recommend something. We need at least a spot to try it.
00:44:24 Michael Gottlieb
Nano Bananas. Yep, a Gemini tool.
00:44:31 Speaker 4
there are many ways to do this everything from local inference it will sign you up with an account of stable diffusion or whatever the point is the image generation aspect of it the actual we need to shift it for you to be in control of exactly where those sources from so you have traceability to know where they came from rather than mysteriously emerging conversation history.
00:45:04 Val
jvl value will be in jvl knowledge and jvl knowledge has to be accessible to j, when lena leaves jvl the knowledge cannot escape you i think ultimately what we're.
00:45:19 Speaker 4
talking about is the system where the decisions the transcripts the design documents and things like that probably going to end up in github, And there'll be a series of markdown files and things of that nature. They could be in hearing issues. They could be in posture where they end up playing at. But my finger points towards the process where things are.
00:45:49 Michael Gottlieb
I just, I think that it's always true no matter what you're learning. It's always universally true that you have to walk before. Trying to get people to run. I have toddlers right now. And if you try to get people to run before they walk, they will stumble. So it's important, even if, and most people in this of AI start running very quickly.
00:46:22 Michael Gottlieb
So it's, I'm not really talking about, we'd have to really slow the pace down. What I'm saying is we can't jump ahead. The first thing, which I think is what Aaron was kind of saying here, the first thing is more the way that you interact rather than which tools you use. Because if you lock into which tools you're using, if it's like ChatGPT versus anything else, then that particular tool's idiosyncrasies, nuances,
00:46:53 Michael Gottlieb
become embedded in your way of work. And that way is not... Now you have to at least do a lot of rework to unlearn those things and use it differently. So I think, from my perspective, it doesn't really matter which AI-generating tool you use. There are many of them. You could use ChatGPT. It's great. But if you're with more than you feel...
00:47:25 Michael Gottlieb
I think this MCP server that I'm building you, which I need to finish and then give to you, and then we need to train a little bit on it. I think this becomes a foundation. Truly, I've done a lot of these training sessions. I can talk about how it works. Blue in the face almost never matters, never does any good until someone gets their hand in it and then that experience. So I truly believe that this meeting, what I wanted to do, validate my idea that some.
00:48:01 Michael Gottlieb
of these tools would be an interesting thing to explore, and the next time we meet, let me give them to you, and in that session, I would like to plan to share your screen and we'll go from zero to getting it fully working, and then there will be a pattern that we'll start using these tools because these tools that I'm building do not have, ChatGPT versus CLAW versus Gemini opinions embedded in them, they have JVL opinions embedded in them.
00:48:33 Michael Gottlieb
That's what we want to move forward, is there's a JVL way of working that is agnostic to whatever AI provider we're using. So we have to start using those tools. And those are the patterns that I think it is fine for us to just absorb. It's like, whatever we decide, that's the prison. We have to move out of other ecosystems and into a custom ecosystem. From my perspective, that's what I think we can do in the next time to meet.
00:49:07 Michael Gottlieb
I have what I need to do that. So I feel that from today's perspective, I need, and then the next meeting that I have on our campus, is next tuesday at the same time um does anyone else need to capture anything from their side whether are we good for today i think i'm fine and then the next meeting for you saying like.
00:49:45 Speaker 2
i i can start to use this mcp so but should i do should i prepare somehow.
00:49:56 Michael Gottlieb
no what i what i'll do and i think this works really well um i just i'm training someone else on this not the same tool but a similar concept right now and i think it will work really well without any preparation next meeting is you and me lena you share your screen and we will walk through the getting this mct server installed connected test, some of the technical but some of the patterns instruct you to like.
00:50:29 Val
get that up but then you should you should have cloud code installed on your yeah okay yeah because now you know what we can.
00:50:40 Michael Gottlieb
get cloud code installed on the meeting and even we should use ai in a certain, get i would say don't prepare at all because the way that we're going to go about this is valuable because we can use this as a how we can enable other jbl employees i would say come with a blank slate don't prepare at all and we'll and we'll get this working from, definitely within that one and we'll even be able to.
00:51:18 Speaker 5
thank you i'm excited.
00:51:21 Michael Gottlieb
uh and i i mentioned this to val over i was some difficulty with microsoft's account so so this meeting moving forward after the jbl meeting so you guys will see an updated invite with it please uh please circulate the transfer yeah we'll do it thank you thanks everyone.
00:52:58 Speaker 4
It means we still have a few minutes before the top of the hour. I think no. I think there's actually space for multiple different types of servers that are going forward. And depending on who you are, you might use them in different ways. There is no reason to have a one-size-fits-all thing. I've built kind of the big overseer. It does the puppet maps. So you will use that.
00:53:30 Speaker 4
And Lana is concerned. We're not building it for Lana as a crisis. We're building it for her role, which is different. And I think that is okay to then have an observer that does that. Consider now the very same agent session that has potentially access to both simultaneously. You just use the tools as needed. So there's overlap.
00:54:02 Val
But when you prompt an AI, how does it know which MC.
00:54:09 Speaker 4
Well, remember a single one of them. So let's say that the one that Clayton has has a comment on an issue. And let's say the one that I've built also. And maybe they're slightly different, but ultimately you have to say, here's the issue ID comment I want to comment on. They're kind of the core things to be able to make. It doesn't really matter which tool it uses because they'll both go to the same end point and end up commenting.
00:54:40 Speaker 4
But when Lana says, I need to figure out what game to plan, that's not something your MCT server has specific in it, but it's a tool listed. And it's, oh, that clearly makes a lot more sense to make a tool called planning a new game. Let me do that.
00:54:58 Val
So it's something that AI could already do on its own.
00:55:03 Speaker 4
Yeah, it does it on its own. When you load together an MCP server, you know, 20, 30 tools or something like that available to it, and it'll just know the descriptions because it's already loaded that into context.
00:55:19 Val
And where does it get description from.
00:55:22 Speaker 4
From the MCP server itself. When you start a session, the MCP can jack all of the conversation.
00:55:32 Val
Okay, understood.
00:55:36 Speaker 4
I'd like to let you know that Atlanta likes to dive into corner cases of justification, so to be careful.
00:55:44 Val
She's going to drag them out. All right.
00:55:53 Speaker 4
We should set up some... Andre, about getting the knowledge graph at least sort of way usable for you.
00:56:04 Val
When are you ready.
00:56:05 Speaker 4
To install it right now. I would like to have you be present while we discuss it and I explain it.
00:56:15 Val
Well, I'm ready. Are you ready.
00:56:17 Speaker 4
Yeah, I mean, I can't do it right this time. I think in the next, you know, with plans next week to get an hour to do an introduction.
00:56:28 Val
Tell me an hour time.
00:56:35 Speaker 4
Let's go.
00:56:42 Val
I can do Monday at 10.
00:56:43 Speaker 4
Let's do that. Monday at 10? Good Monday. at 10 years now, take that slot.
00:57:03 Val
How would they call this meeting.
00:57:07 Speaker 4
Let's call it interest and knowledge. One of the things that is here now is that we will be able to begin planning on having, essentially, a transcript integration system.
00:57:39 Speaker 4
where audio files are loaded into it. Now, this is a bit of a future thing, but I've been thinking, like I said, shooting for where it's gonna be. Right now, you track all this stuff. inside of Teams, and you have a directory structure. It's possible that this tool could be done live. So basically, as you speak, you're plotting out all the content, recording it.
00:58:13 Val
Bravo.
00:58:15 Speaker 4
Which is really useful, because now you can go back and have a conversation about what's in it. It's sort of a way to pre-plot right then and there about how you got it.
00:58:28 Val
What do we need for that, for you to see.
00:58:31 Speaker 4
We just need to get it installed. You can open the browser.
00:58:37 Val
One hour is enough, or should I allocate two hours? So just send to Eli.
00:58:41 Speaker 4
Start with an hour, have him see this project, then how to get installing it, and try to run it. I need him to be pre.
00:58:53 Val
Perfect. Evite has been sent, so, yeah.
00:58:57 Speaker 4
It's complex, and it's not something he's going to figure out and teach it. Try to get this running on. We're going to meet again. We'll continue until we have...
00:59:13 Val
Meeting will continue until morale is improved.
00:59:16 Speaker 4
Exactly. And then we'll just keep upgrading.
00:59:20 Val
Okay.
00:59:21 Speaker 5
I'll see you.
