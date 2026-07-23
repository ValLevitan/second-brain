**UI_Claude_Code adaptation COME PREPARED OR DO NOT COME TO THIS MEETING!-20260206_091521-Meeting Recording**

6 February 2026, 02:15pm

1h 48m 2s

**Val Levitan** started transcription

0:09  
Double.

**Irina Shishko** 0:09  
Come.

**Alexander Korochkin** 0:13  
No.

**Val Levitan** 0:14  
Probably then.

**Irina Shishko** 0:30  
Hello.

**Val Levitan** 0:32  
Hello.

**Anton Seregin** 0:37  
It's simple.

**Val Levitan** 0:47  
Buster.

**Aaron Bockelie** 1:50  
Hey, everybody.

**Val Levitan** 1:52  
Oh.

**Irina Shishko** 1:52  
Oh.

**Val Levitan** 1:54  
Bye, Aaron.

**Vladimir Samusenko** 1:54  
Hope.

**Andrei Bosik** 1:56  
Hello.

**Aaron Bockelie** 1:57  
All right, well, we got a lot of people and I think we need to pick up where we left off.  
So uh.

**Val Levitan** 2:04  
Well.

**Aaron Bockelie** 2:06  
We does everybody know what we were doing last time or should we do a quick summary?

**Irina Shishko** 2:12  
Oh.

**Val Levitan** 2:12  
Let's do a quick summary and let's set up the objectives.

**Aaron Bockelie** 2:15  
OK.

**Val Levitan** 2:16  
Let's let's establish one rule. So I'm going to be a little bit sarcastic, but I need to say it again. We cannot read minds.  
So facial expressions, raising hands, this type of sign.  
Is part of the meeting. Otherwise there is no socializing. This is not a lecture. This is a back and forth interaction. We're looking for facial expressions. We're looking for signs of alignment.  
We understand that not all of you speak fluent English. We will try to go slow, but.  
If we run away and you are lost, raise your hand.  
And we will either translate or explain or go slower, but at least this means pause.  
We will try to refrain from.  
Any fancy language we will speak in very plain English.  
OK.  
Thank you. Thank you. Let's move on, Aaron.

**Irina Shishko** 3:37  
OK.

**Aaron Bockelie** 3:41  
Right. Oh.

**Val Levitan** 3:42  
Object, yeah.

**Irina Shishko** 3:59  
То, что мы обсудили?

**Val Levitan** 4:00  
Ай.

**Irina Shishko** 4:01  
Чуть раньше.

**Val Levitan** 4:03  
А эксплуатант turn абдуктор.  
В иоланту тейк.  
Это скрин смс мы лонтон вы Windows табличка простите.  
Он ту горку она простите.  
Can take the screens and convert them into usable material.  
And so we will need Vladimir and Anton Sirodin and Evgeny for sure. Everybody else will benefit from it because at the core of it, Aaron will show us how to use.  
Cloud Desktop.  
And cloud code.  
For peer development.  
Aaron, anything else needs to be said on the objectives?

**Aaron Bockelie** 5:05  
Uh.  
No, I think let's just get into kind of following up where we where I believe we left off, which is.  
I think the top of the pattern, the layouts for all of the screens from Figma and then we'll kind of go from there.  
I I have a few things to say about that that I want to start with, which is that.  
The work put into Figma is is like a.  
And Igor, I want you to kind of either add to this or disagree or agree. The work in Figma is is closer to say, using Adobe Illustrator to draw out a.  
Diagram or or documentation for a purpose or a product than it is actually creating the program or the software for the product is how I believe Figma is usually used.  
But well, the other part of this is that because you're using Figma though, and the way it's structured, it's plumbed underneath is it allows you to directly export this to functional software. So Figma, it has this interesting.

**Ihar Hrybko** 6:13  
Mm.

**Aaron Bockelie** 6:30  
Area where maybe you're drawing elements and pictures, but actually it is decomposable into actual software immediately on export. Is that is that a accurate representation, Igor?

**Ihar Hrybko** 6:43  
I think more accurate will be that we using Figma for prototyping, having discussions how actual user interface will look like.  
How we establish user flow?  
Like user navigation.  
From one tool to another.

**Aaron Bockelie** 7:12  
Mhm.

**Ihar Hrybko** 7:13  
And we have ability to create interactive prototype. So it's not like illustration, it's more functional way and.

**Aaron Bockelie** 7:28  
Sure. It's not exactly the same, obviously. I'm yeah.

**Ihar Hrybko** 7:29  
Yeah, I think, yes.  
But it is a graphical instrument, obviously.

**Aaron Bockelie** 7:36  
Yeah. And So what we can do then is if Igor is creating what is essentially like, let's say, I don't know if you've ever had to design a space or an area or something like that where maybe you use a tiny model, cardboard boxes or something.  
Like that to mock up the actual full size before you do the work. This is what Figma allows us to do, is to actually interact spatially with how the layout in the interface is going to be and then gives us a way to decompose it into code.  
And we need to be all on the same page thinking about this way, because I think that without.  
Having the same conversation, it's going to be very difficult for me to tell you this is how we go from Figma to connected to API back end with a a coding agent because what we have to be able to do is we have to be able to describe all the intermediate steps between doing that.  
And I think that's why we have our our other friends here on the call today is to connect the dots because if we can describe the process then we can iteratively use coding tools to like like Claude to to shorten the time to get to the answer.  
So in this case, um.  
Let's say that Igor has a comprehensive set of interface in a mockup for Figma, and then the very next thing that we have to do if we were doing it all manually, if we were just like, OK, I have the Figma stuff, let me build the next thing and the next thing.  
Is that Igor would export out of Figma the React code into something. He would just push the button and save it. He would commit this code into a git repo and have the React front end. We would be able to verify that this React front end can be ran.  
Outside of Figma now with a Vite server running somewhere.  
We could now click around in the Vite server and lay with it just like we were playing in Figma, but now it's indeendent of Figma. Am I correct or incorrect so far?

**Ihar Hrybko** 9:52  
Yeah, the only difference is we manually created these components using completely tested UI kit from MUI using Joey UI and we basically.

**Aaron Bockelie** 10:06  
Yeah.

**Ihar Hrybko** 10:10  
Create a theme JVL theme for these components to stylize it these components, but we right now we we don't have any button to export directly our layouts into actual.

**Aaron Bockelie** 10:12  
Mhm.  
Right.

**Ihar Hrybko** 10:28  
Uh, suitable or react components?

**Aaron Bockelie** 10:34  
So.

**Ihar Hrybko** 10:34  
So we do it manually or I try to use code code or client to lace a screenshot.  
With a prompt like here we need to create this new layout for new page based on this page already created. So use same pattern and he like goes.

**Aaron Bockelie** 10:57  
Mhm.

**Ihar Hrybko** 11:01  
And create and I need to supervise this.  
Oh.  
Source code that client or cloud code provide.

**Aaron Bockelie** 11:11  
Mhm.  
So, so you can export the design tokens like the colors, the typography, the spacing, I don't know, whatever other sort of conventions you might have into tangible items, right?

**Ihar Hrybko** 11:25  
Yeah, yeah.  
Yes, but we not directly use this because we're using the movie system and we rely on this movie or components UI kit layout system.

**Irina Shishko** 11:32  
Yes.

**Ihar Hrybko** 11:46  
We'll basically use a theme to stolide these components and use these tokens from movie that we override in our team.

**Aaron Bockelie** 11:59  
Ye, so if you're starting with the material UI and then you're kind of modifying it to make it be JVL's material UI, right?

**Ihar Hrybko** 12:09  
Yeah.

**Aaron Bockelie** 12:09  
Do you have any plugins for Figma that support exporting this? Because there are a few out there that do this that generate template types.

**Ihar Hrybko** 12:19  
No, right now we don't have.  
We're actually using not exactly movie, we're using fork for fork of movie called Joy UI.

**Aaron Bockelie** 12:31  
OK.  
And so when it comes to.  
Deciding when to stop using Figma and when to start using the React to the actual React code. How far along have you gotten in that so far?

**Ihar Hrybko** 12:47  
I think we almost completely created layouts for LGS, except some screens. We have some screens that not implemented.

**Aaron Bockelie** 12:56  
Mhm.  
Yeah.  
And yeah.

**Ihar Hrybko** 13:04  
But for now.  
It's done almost completely.

**Aaron Bockelie** 13:09  
And as questions for the rest of the team, do you have a?  
Does the code base support fully checking this? Is it fully documented? Do you have ways to run it and experiment with this from a like a a user test perspective already or not?  
Do you have a builder pipeline for this?

**Vladimir Samusenko** 13:34  
Yeah.

**Ihar Hrybko** 13:35  
Yeah.

**Vladimir Samusenko** 13:36  
I have translate.

**Ihar Hrybko** 13:36  
Builder. Yep, I'll translate.

**Aaron Bockelie** 13:41  
Yeah.

**Evgeny Kharetski** 13:46  
But we sit down on your birth policy too.  
I implement.  
No, no.

**Ihar Hrybko** 14:05  
Yes. So we to have all of them, all all of our team have access to this repo. They can run in dev mode or build.  
And see actual LLJs front end with some mocks the back end into their browser.

**Aaron Bockelie** 14:35  
Do you have in the repo? Do you have a description or an architectural overview of how you expect this whole thing to be built on an ongoing basis and maintained yet?

**Ihar Hrybko** 14:47  
I think some kind of documentation we do have or we at least started to add this documentation because obviously this project is quite large and.  
You cannot do all documentation at a time.  
Yeah, we have docs how to run it, how to build it in read me file at the root of the repo.

**Aaron Bockelie** 15:25  
And do you have who's? Who's the principal owner for all of this? Who? Who's responsible for making sure the process is is defined?

**Ihar Hrybko** 15:37  
I think it's different persons for for the front end part. I think it's Anton, for the back end it's you getting.  
And for actual, we do not, I think we do not have right now actual deployment pipeline.  
Maybe I'm mistaken.  
Well.  
Mhm.  
Ну да, в их в operations and a Павел.  
Да саша братка из способов вода из спад.

**Aaron Bockelie** 16:56  
Какая то судей дизайн да вплавлен пафос тебе буду говорить про море я интерпол пор интересен.

**Ihar Hrybko** 17:12  
Я от инкого олафа вас.  
От дискаунт хау exactly Токио был лук лайк.

**Aaron Bockelie** 17:29  
Can one of you share your screen and point at the actual area where the documentation for the flow and architecture is and show me what repo it is exactly? Let's look at it. I wanna get into practical use of this.

**Ihar Hrybko** 17:29  
Yeah.  
That I repository document.

**Aaron Bockelie** 17:56  
Let's see how it's structured.

**Ihar Hrybko** 18:03  
Evgeny will share his screen right now.

**Aaron Bockelie** 18:06  
OK.

**Evgeny Kharetski** 18:07  
Itna.

**Ihar Hrybko** 18:10  
Yep.

**Irina Shishko** 18:10  
Done.

**Aaron Bockelie** 18:11  
Yep.  
Hey Andre, I have a question for you briefly.

**Andrei Bosik** 18:29  
Mhm.

**Aaron Bockelie** 18:30  
What have you changed the the the default timeouts for authentication and GitHub at all?

**Andrei Bosik** 18:38  
Mhm.

**Aaron Bockelie** 18:40  
Could you make the the?

**Andrei Bosik** 18:40  
Uh, I uh set up uh 8 hours uh to identification.

**Aaron Bockelie** 18:46  
'Cause I notice that when I've tried to log in and use it, I step away from it for 20 minutes and it's asking me to authenticate again all the time. It's really irritating.

**Andrei Bosik** 18:54  
I will check maybe GitHub change some fields to work with Android ID where is a started time for notification OK.

**Aaron Bockelie** 19:08  
OK, and and the reason I ask you this is because any type of continuous authentication breaks means that agent coding tools will continue to break and fail to work as well.

**Andrei Bosik** 19:19  
Hmm. OK, I I will check this.

**Aaron Bockelie** 19:21  
Yeah.  
OK.  
So this is the main readme for the local gaming server. So we clone is this is this your docs that you have?

**Evgeny Kharetski** 19:29  
Yes.  
Hmm.

**Aaron Bockelie** 19:50  
I want to try to view this myself as well.

**Andrei Bosik** 19:51  
Good.  
So translation.

**Ihar Hrybko** 19:59  
So we we have this with me for dev for build and some build pipeline and we have some doc maybe related to some.  
Functionality. I think that's it.

**Irina Shishko** 20:21  
OK.

**Aaron Bockelie** 20:23  
So we see kind of the basics on how to use this.

**Ihar Hrybko** 20:27  
Yeah.

**Aaron Bockelie** 20:28  
But what I'm not seeing though is more of the architectural purpose behind it, rationale and all of the different concerns that you have for how to make this work. And let me if I if I talk fast and it needs to be slowed down, let me know.  
We have to have these defined. They have to exist in the repo because without this guidance, well, first of all, if I'm looking at the repo right now and I really wouldn't know where to start. No AI, just Aaron, just looking at this.  
I would be cool. OK, here's how I get it running, which is nice to have, but when I start looking around and say common or in C3 or in these other areas and I wanted to know.  
For instance, where is the front end of the of the of this product at?  
I don't know where it's at, right?

**Evgeny Kharetski** 21:33  
Yeah.  
Yes.

**Aaron Bockelie** 21:36  
So um.  
How do you feel that? How would all of you describe this to a new person?  
Let's say me. Say I was joining your team and I spoke fluent Russian and you were explaining how Aaron is going to be the new integration engineer for the product.  
What would you tell me to do?

**Evgeny Kharetski** 22:08  
You stay in.  
Mhm.  
Mhm.  
Он ведёт собственно.

**Ihar Hrybko** 22:26  
Да.

**Evgeny Kharetski** 22:26  
Вк.

**Ihar Hrybko** 22:27  
Со оцинковать наушницу xxx плейн.  
Песню passo он завели на конверсах sn.  
From Evgeny, from the front end, like from Anton.  
Not right now like like this.

**Aaron Bockelie** 22:49  
Good.  
Could all could we go through the exercise of explaining that right now from your different perspectives? We can use the meeting chat to do this. I want you all to write down in the meeting chat a paragraph or two in Russian in your native language how you would explain this.  
High level, not in detail.

**Irina Shishko** 23:11  
Mhm.

**Ihar Hrybko** 23:13  
So.  
К туру, как кто понимает да, то есть вот этот папка для чего? Где frontend находится, да там бы.  
Кент, что такое сири ну типа вот это да. Я думаю можно всё такое.

**Aaron Bockelie** 23:40  
Идите ви габи раунд хэнсен твоей такие грустные.

**Ihar Hrybko** 23:44  
2.

**Aaron Bockelie** 23:46  
Я не так и не собрался, так и не батл собрался с нагибаться я.

**Evgeny Kharetski** 23:50  
Но.

**Aaron Bockelie** 23:53  
Амелия такие протесты.

**Ihar Hrybko** 23:53  
На это лицо.

**Evgeny Kharetski** 23:56  
Но попробовать можно.

**Aaron Bockelie** 24:00  
Imagine you're telling this person all at once, this new person all at once, what your guidance is for dealing with it, the way you deal with it. I just want you to give it a try. I want you to write out a couple good paragraphs in chat.

**Val Levitan** 24:12  
Maybe just maybe, maybe, maybe. Let's do this. I like the exercise. Maybe. Hold on a second. Let's let's try something a little bit better. I mean a little bit different.

**Aaron Bockelie** 24:20  
Sure.

**Val Levitan** 24:28  
Why don't we take exactly, literally start your watch 7 minutes, dictate on your phone everything that you know high level about what Aaron is asking you for.  
In your native language, can we do that? Because writing, if everybody starts writing, it's going to be very long.

**Aaron Bockelie** 24:54  
We could do it that way too. It is the same. It is the same output.

**Evgeny Kharetski** 24:56  
Uh uh.

**Val Levitan** 24:58  
And then where where would you like to output all of this?

**Aaron Bockelie** 25:02  
I just want to see it in the meeting chat. That's the simplest place to do it.

**Val Levitan** 25:07  
OK.

**Aaron Bockelie** 25:07  
We just need to collect it.

**Val Levitan** 25:10  
But each one of each one of you, every one of you, whatever you know, if you don't know, just say I don't know.  
And whatever you know, just put it in the meeting chart.  
OK, 7 minutes, yes.

**Aaron Bockelie** 25:24  
Can I? I want to add. Please add one thing to your narrative. Please explain who you are and what your role is and what you do.

**Anton Seregin** 25:25  
He he shut us for uh.

**Aaron Bockelie** 25:37  
When you when you give your answer, that's it. Just so I know who's doing what.

**Val Levitan** 25:43  
OK, so your name, what do you do and what do you know about this repository, right?

**Aaron Bockelie** 25:44  
OK.  
Yeah.

**Val Levitan** 25:54  
E-mail with DLAC is 90 private repository for your commentary high level.

**Evgeny Kharetski** 26:12  
West.  
Yeah, go on, bass. No, just sure that I'm ****.

**Irina Shishko** 26:17  
Yep. Uh, uh, uh, is that LS?

**Val Levitan** 26:22  
Link.

**Evgeny Kharetski** 26:26  
Mhm.

**Val Levitan** 26:29  
OK, turn off your cameras. Turn off your microphones. I'll see you back in 9 minutes.

**Aaron Bockelie** 26:35  
I'll keep the timer too.

**Val Levitan** 26:38  
We'll put on the timer, yeah.

**Vladimir Samusenko** 26:41  
Cook.

**Val Levitan** 26:46  
Turn off your microphones.  
People.

**Aaron Bockelie** 38:03  
OK, I'm seeing us getting our things in.

**Val Levitan** 39:09  
Hm.

**Aaron Bockelie** 39:55  
Is this everybody's feedback now?

**Irina Shishko** 40:01  
Um.

**Aaron Bockelie** 40:01  
Are we missing anybody?

**Irina Shishko** 40:04  
No.

**Ihar Hrybko** 40:11  
Nothing.  
That's sweet.

**Aaron Bockelie** 40:15  
OK.

**Irina Shishko** 40:15  
So.

**Aaron Bockelie** 40:17  
So what what I'm going to do now is in the time that you spent doing that, I used Cloud Code to reestablish my GitHub connection, my off keys, certs and user accounts to connect to.  
The this this project of platform local gaming server. So I have access to it and I've cloned the main branch right now.  
For sake of time and reasons, it has been challenging for me to talk, talk it through because I I'd like to teach and I try to teach, but some cases I just don't actually know the answer and I have to go figure it out myself and this is one of those situations.  
And I'm going to share my screen and I'm going to explicitly tell you what I'm doing and why. And I want you to follow along. This is a this is both like Val said. It's not a lecture. Don't treat this as television to watch and walk away.  
I want you to observe what's going on and take notes because you are going to be doing this in these tools too, OK?

**Irina Shishko** 41:20  
OK.

**Val Levitan** 41:26  
I want to add explicitly something else, and this is extremely important for each one of you sitting here.

**Irina Shishko** 41:27  
Hmm.

**Val Levitan** 41:36  
It is not my job expression.  
You cannot work in JBL.  
Very, very clear message to everyone.  
I am going to give you every opportunity to learn and to excel.  
Because I want you at your best.  
You were hired as though you're the best. I want to keep you as the best and I want to keep you growing and I want to keep you excelling and I want to pay you more money.  
And I want to get rid of the people that do not want to be here. Don't suffer. Do not suffer.

**Aaron Bockelie** 42:19  
OK.

**Val Levitan** 42:27  
So here's an opportunity to learn. Learn and move and excel. Get better.

**Aaron Bockelie** 42:38  
Are you able to read this prompt right here? Is this readable? Is it blurry?

**Val Levitan** 42:43  
Very difficult to read. Very difficult to read.

**Irina Shishko** 42:44  
Mm mm.

**Val Levitan** 42:47  
It's blurry and the font is, yeah, better.

**Irina Shishko** 42:51  
Um, uh, mobile copy.

**Val Levitan** 42:51  
And also also they read. They read very slowly in English, so maybe you could post prompts.

**Aaron Bockelie** 42:57  
I can copy and paste it.

**Val Levitan** 43:00  
Yeah, copy paste prompts.

**Aaron Bockelie** 43:01  
Let me let me paste this into the chat.

**Irina Shishko** 43:03  
Mm-hmm. Yes.

**Aaron Bockelie** 43:04  
I'll do that instead and and I think we just have some limitations with with screen share sometimes unfortunately. Let me let me try one one trick.

**Val Levitan** 43:06  
Yeah.

**Aaron Bockelie** 43:21  
Sometimes if I share with my camera off, it works better.

**Val Levitan** 43:28  
It's very convenient for you to place prawns into chat. It's very good.

**Aaron Bockelie** 43:34  
Does that look any better on the screen share?

**Val Levitan** 43:38  
No, it's the same.

**Aaron Bockelie** 43:39  
OK, well.  
We'll just go.

**Val Levitan** 43:42  
It's it's very nice if you keep on placing prompts into chat.

**Aaron Bockelie** 43:48  
All right, so so this this is what we're going to do. I'm going to actually just copy and paste everything from teams that you just all pasted in there.  
I'm going to uh.  
Aste all that in.  
Right O now we have a team member's text file, which is just literally the copy and paste from everybody. OK.

**Irina Shishko** 44:26  
Yes.

**Aaron Bockelie** 44:27  
And I'm going to use this prompt.  
I'm gonna, uh, copy this additional prompt here. I'm gonna edit that just slightly.

**Irina Shishko** 45:26  
Mhm.

**Aaron Bockelie** 45:32  
So I want you to see what's happening here. Good framing. Making implicit knowledge explicit is one of the highest leverage things a team can do. Let me gather context first. So we're allowing Claude to launch a separate session to explore the repository right now.  
O The very first thing it's going to do is use the context it has, which is the repo that I just cloned, and it's going to just go dig around in it, OK?  
Now you could be doing this too. There is nothing stopping you from writing a similar prompt, but I want you to think for a minute what a prompt means. Prompt not some special way to talk to an AI.  
It's a way of thinking things through and writing out what you're thinking.  
And I and I want you to consider that metacognitive. Is that word connect with you guys? Metacognitive.  
I I'm reading faces, I'm reading minds and it doesn't feel like it's connecting.

**Ihar Hrybko** 46:36  
I I don't think so.

**Aaron Bockelie** 46:41  
Metacognitive means to think about thinking.

**Andrei Bosik** 46:43  
What is?

**Aaron Bockelie** 46:48  
Think about how you think about things.

**Ihar Hrybko** 46:52  
Aaron, can I ask you a question?

**Aaron Bockelie** 46:54  
Yes.

**Ihar Hrybko** 46:56  
Do we talking now all the this flow is like white coding?

**Aaron Bockelie** 47:03  
Yeah, sure. I'm vibe engineering. I'm vibe running a business. I'm vibe making money right now. I mean, here's the thing. You guys need to drop the negative connotation with the word vibe because.

**Ihar Hrybko** 47:11  
That's nice.

**Aaron Bockelie** 47:17  
We might be vibing here, but it's moved far beyond a year ago when the term vibe coding actually came up. And I'm not trying to be angry or upset about it. I'm just saying you can call it that if you'd like, but if it's effective, I don't care what it's called, so.  
Let's be really careful about how you state that word, because it can mean essentially negative connotations for depending on who you're talking to.

**Ihar Hrybko** 47:45  
No, I'm I'm not meaning in negative connotation. As far as I understand, at least for me, will I go like meta coding. So we use LLM and we use ID.

**Aaron Bockelie** 47:47  
Yeah.  
Yeah.

**Ihar Hrybko** 48:02  
To.

**Aaron Bockelie** 48:02  
I like that. I've never heard of that word before. You just said it. Metacoding. I really like that, actually. That's a really smart way of saying it, because just like I'm saying metacognitive, thinking about thinking, metacoding is thinking about coding, right?

**Ihar Hrybko** 48:09  
Yeah.

**Aaron Bockelie** 48:18  
It's kind of a more recise version of it. O if we were to say something about replacing vibe coding with meta coding, that's actually what we're doing here.

**Ihar Hrybko** 48:29  
But there is a difference because for white coders they don't need to be like engineers. They're like writing prompt, getting things done.

**Aaron Bockelie** 48:32  
Sure.  
Yes.  
Mhm.

**Ihar Hrybko** 48:44  
Just like that, but for metacoli we're using some LM and then we supervise the control the architecture because of our knowledge to supervise this process.

**Aaron Bockelie** 49:00  
Right.

**Ihar Hrybko** 49:00  
I think it's kind of difference.

**Aaron Bockelie** 49:03  
So uh.  
Yeah.  
One minute here.  
So what you're describing is exactly what's lacking from this repo right now.  
There is no control about how you do stuff and how it's supposed to be done. There is no description of the actual engineering thought behind the thinking of how it's gone, and that's actually what we're trying to establish right now.  
If it's not written down, it doesn't really exist. You can't build a spaceship without specifications.  
And it has to be written and referenceable and controlled.  
And that's essentially what we're we're trying to establish in this repo at this very moment right now.  
So actually by establishing this documentation, think about the channels available. OK, so I wanna talk about my prompt for a minute. In the prompt that I shared with you guys, I compared 2 words, implicit and explicit.  
What does that translate to in Russian?

**Anton Seregin** 50:25  
So mhm.

**Aaron Bockelie** 50:28  
Does everybody know the difference between the two?  
OK, so when when the architecture and the team dynamics are implicit, everybody on this call except me is in on the in on the game, right? I don't. I don't know how you guys talk and communicate or anything. It's a mystery. You guys are on the other side of the planet basically, right? You actually physically are.  
And I don't know how you work. I have some guesses right as the new guy, but it's not explicit, it's implicit. We have to set this up explicitly because team dynamics and ownership is one part of the engineering aspect of an entire product.  
Vlad, your microphone is very loud, so I'm going to keep muting you. I'm sorry for doing that, just pointing it out. And so when we then consider all, This is why I asked you for all for your roles, because we're making the implicit explicit.  
I'm telling a thing that has the capability to traverse the entire source code, the entire product, right? And see what's written and created. It even can see who committed what code to things. It knows the usernames.  
Because I put your names at the top of each of those description's of what you do, it now knows who did what and where and why. We can look it U we can dig into it really deep. It's explicit.  
And furthermore, when we document this and write it down into the repository, what we're doing is we're giving tools like coding agents a chance to pick up what you're concerned about and what you're doing, because otherwise that context doesn't exist.  
So we can't describe how to go from Figma to React to something in the middle to the back end and figure out what something in the middle is until we know who's the ownership for those.  
And where are the capabilities at for the team? And how to then describe to connect all these things in which ways that make sense? You have to be able to consider all of that. So it's like layers on top of each other, right? We start, we got our source code, right? That's a good place to start. It's functional.  
If you read the read me, it tells you how to run it, but it doesn't tell you why you run it or how or what's the purpose of it really. And so now what we've got to do is begin to build all of that too.  
I'm just watching the token count to sort of count up here a little bit, but we can see here. I want you to see. I want to show you what the the prompt of the coding agent.  
Gave to a sub agent. So do you know what I mean by that by the main agent giving prompt to the sub agent?  
Give you a thumbs up if you understand that that term.

**Anton Seregin** 53:36  
More than proper value sub agent. What is sub agent?

**Aaron Bockelie** 53:37  
That's what putting in.  
Yeah, look at what the look at what the agent itself wrote to a sub agent as a subordinate to go investigate.

**Ihar Hrybko** 54:03  
Momo.

**Val Levitan** 54:10  
It seems like we don't have the exact definition and it would be nice if you could be a little more definitive.  
Aaron.

**Aaron Bockelie** 54:22  
Of what a sub agent is.

**Val Levitan** 54:26  
Yeah.

**Aaron Bockelie** 54:26  
OK, so when we're using cloud code, you invoke a copy and you work with it, right? Think about how powerful it is to use a coding agent. Write me some code. Explain this. Go do that thing. Go do the other thing, right?  
Is that helpful and it makes things go faster when you interact with it. Now what if you have a coding agent that can write the same thing that I just described to other coding agents?  
I'm going to spin up 10 copies of myself and give 10 different things to 10 different agents simultaneously.  
What can you do with that?  
It's a very powerful thing to have that happen, but you have to plan it correctly. You have to kind of do it right and and set up the purpose of it correctly first before you can just let that happen. Otherwise you'll have chaos.

**Val Levitan** 55:29  
Uh.  
Let's spot. Let's pause. Let's pause for a second.

**Irina Shishko** 55:49  
Spaniards.  
One the yeah.

**Anton Seregin** 56:05  
Вообще агент, что ну такой принцип?

**Val Levitan** 56:07  
Елена exe.  
Милана игора explained мо.

**Aaron Bockelie** 56:12  
Окей.  
Все.  
По уйдя с.  
Действительно апрея.  
Полиция спамер вон оклеен ты звали.  
Роман через все его цель.  
Если сцеплен.  
Bains йенс обгонит еще и.  
Физикой.  
Top.  
There is a Claude instance right here. See it this blue one right here. And there's another one, another Claude instance. There's actually multiple Claude instances. I got to filter by.  
Let's see. Bye.  
Man name.  
Well, anyway, there's multiple clawed instances. There's one that's moving one spot. I can't quite catch it, but my point is.  
It's not one Claude instance, it's several processes of Claude running at the same time talking to each other. They are sending messages back and forth to each other.  
When I tell Claude to do something, it's turning to another Claude and saying you do this Claude and you do that Claude and you do that Claude and you do that simultaneously at the same time.  
I have spun up several process engineers simultaneously to investigate the entire code base all at once to understand how this works, and now it's producing the output about this right now.  
You have to see that there's a scale to this that's not quite visible.  
Takes a long time to do this by hand.  
The PR reviewer list shows Anton S, JVL, Evgeny, Igor. Are these the correct GitHub usernames for code owners? What about Alexander and the unnamed FE dev? Do they have GitHub handles?  
So.  
Let me add.

**Val Levitan** 58:21  
Who? Who is this? Who? Who is this unnamed?  
A feed developer.

**Aaron Bockelie** 58:27  
Unnamed front end developer. Who might that be? Does anybody have a guess?

**Val Levitan** 58:34  
Aaron.  
Is it you?

**Aaron Bockelie** 58:36  
I don't know if it's me. No, I would be identified.

**Ihar Hrybko** 58:38  
I.

**Vladimir Samusenko** 58:39  
I think it's me, like, except me.

**Aaron Bockelie** 58:42  
Can you please share your GitHub your GitHub user accounts in chat?

**Ihar Hrybko** 58:49  
Mhm.

**Val Levitan** 58:50  
And Andrei, why would we Andrei, why would we allow somebody on our GitHub with with unnamed?

**Irina Shishko** 58:51  
Don Boyle.

**Aaron Bockelie** 58:59  
It might have been historical, Val, before it was pushed up.

**Andrei Bosik** 59:02  
Uh, I think it's uh when.

**Val Levitan** 59:03  
It cannot be. It cannot be. It cannot be historical because we cleaned out GitHub. This was my direction.

**Andrei Bosik** 59:09  
No, we transfer this from Bitbucket and I think it's a name from Bitbucket.

**Val Levitan** 59:21  
Can you please clean out those names?

**Andrei Bosik** 59:25  
I will try. I am not sure that we can do it in historical.

**Val Levitan** 59:32  
Is it possible to establish the rule that nobody without JVL credentials can access GitHub?

**Andrei Bosik** 59:40  
Uh, you can use more to double what she does. What? No, I see.

**Aaron Bockelie** 59:51  
So right now we're we're letting Claude explore GitHub, the interface for it, and we're trying to figure this out. I'm letting Claude. I told Claude to go ahead and just look at GitHub and see if you can match up what you're seeing in the in the commits from what we see in the GitHub administration.  
So it's kind of trying to match it U for us right now.  
I also asked it to provide me with some evidence of what they're doing so we can maybe deal with it because I have the team in front of me.  
We'll just let it kind of work it out right now for a minute.  
OK, here we go. So it thinks that Alexander Boratko found found Alexander. Here is the different people it found contributing to this. So Andrei, your admin, Evgeny is the Java developer, Igor is the designer, Anton's the front end set up UI, Vlad is the front end and Boratko is QA automation.

**Irina Shishko** 1:01:00  
Hmm. Mm, yes.

**Aaron Bockelie** 1:01:01  
Also, that's what it sees from this repo.

**Evgeny Kharetski** 1:01:02  
And but.

**Alexander Korochkin** 1:01:03  
No.

**Evgeny Kharetski** 1:01:07  
OK.

**Andrei Bosik** 1:01:14  
Let me just.

**Aaron Bockelie** 1:01:15  
It's just going off of what it actually Alexander committed. So just be be aware. It's not just hallucinating this, it's finding the evidence and doing this. Here, let me let's challenge it. So you're saying that Baraka doesn't do that, right?

**Ihar Hrybko** 1:01:31  
No, he's not current automation. He's Java developer.

**Evgeny Kharetski** 1:01:34  
Also Java developer.

**Alexander Korochkin** 1:01:36  
Developer.

**Ihar Hrybko** 1:01:38  
Because I think this Alexander, we have different Alexander on this meeting particular.  
And he is mixing up.

**Val Levitan** 1:01:59  
I think, I think, I think, I think I was a motion, Alexander B at JVL.  
At the Korochkin at Alexander K at JVL.

**Alexander Korochkin** 1:02:23  
So any basal.

**Evgeny Kharetski** 1:02:31  
It's getting shot that bulla.

**Aaron Bockelie** 1:02:37  
Плотненькую эверленд ты с обстоятельствами это failing зачесал.  
Обогащала tales.  
Новых видеозаписей варится он.  
What's implicit? You guys all reacted rather excitedly when I told you Brodka was a QA engineer, which I found kind of funny, actually.  
So let's see here. Andre GitHub admin, one of the five admins in the repo. Full admin permissions. He initially created and set up the repo. He manages GitHub access policies, pipelines and security threat identification. Low code commits only touches gitignore.  
So let's look at these other guys. So Vladimir, LGS 89 doors, battery health, printed ticket, login screens, denomination settings, refactoring, loading hardware, improving front end architecture. This is Vladimir, front end developer.  
QA Automation Evidence Build pipeline work. Multiple updates to build and store YAML. Full win build. Maintain CI workflows that produce testable artifacts. Build assembly. Gameware framework integration. 2826 files. Touch the largest file footprint of any contributor. Extensive back end work.  
And other things notes on Alexander. His meeting description says end to end testing, but his commits show he's a significant back end contributor. Is it confusing a different Alexander?

**Val Levitan** 1:04:17  
Yes.  
He's confusing Alexander Korochkin with Alexander Derok.

**Aaron Bockelie** 1:04:25  
OK, So what we can then say is.

**Val Levitan** 1:04:26  
Because Alexander Alexander Korochkin couldn't write his last name because it's a very long name and would have taken approximately 7 days to write it out. So he just shortened it out to Alexander.  
This is what I always say. Respect, respect. It's so important.  
Respect your Co workers. What do they have to go through in order to guess what you're thinking?

**Aaron Bockelie** 1:05:04  
So all I have to do now is I just correct it. So I've been told that Alexander is actually Alexander Korochkin. This is an easy update. What's his GitHub account? Do you think from the collaborator list we pulled earlier? Alexander K under score JVL read access. This fits perfectly. K Matt Korochkin.  
Readonly access is consistent with a QA role. This meeting description said can't describe the repo structure. Makes sense if he's rimarily a consumer of builds, not a committer.

**Ihar Hrybko** 1:05:37  
Yeah, looks like that.

**Aaron Bockelie** 1:05:52  
Let's note that that Alexander B is definitely part of the team. He's just not on the meeting with us right now.  
Now here's the team roster. Bosik, Evgeny, so forth, right? Alexander Brotka is the back end build integration engineer and Krochkin is the QA automation engineer. Does that feel right?

**Irina Shishko** 1:06:18  
Right.

**Ihar Hrybko** 1:06:19  
Yep.

**Aaron Bockelie** 1:06:21  
Now, do you Remember Me talking about the sandwich, the AI sandwich model? Did I did I tell you about that?

**Ihar Hrybko** 1:06:31  
Yes.

**Evgeny Kharetski** 1:06:31  
Yes.

**Aaron Bockelie** 1:06:31  
Are you familiar, all of you? I need to make sure I see. I need to read minds here. Anton Alexander, you know what I mean by a I sandwich.

**Anton Seregin** 1:06:39  
Couple of words, please.

**Vladimir Samusenko** 1:06:43  
Yeah.

**Aaron Bockelie** 1:06:43  
OK.  
To quickly review, the AI sandwich is a human.  
Sets U the problem. Here's the thing I need to do. Here's what I know about it. Here is the goal.  
OK AI go explore the problem and come up with potential solutions to the problem I have.  
The other that's the middle layer of the sandwich, the filling. The bottom is the human. Again, I accept or reject or want to refactor your output. AI. I'm going to accept this. I'm going to correct you and you're going to go back and fix it, or we're just going to go through and be done.  
O what I did is I shared that initial prompt with you guys, right? This project is mostly code blah blah blah blah blah.  
We let it work for a while. It found all this stuff. This is sort of the brief summary of all the stuff it found.  
It was wrong. And you guys went, Oh my God, that's wrong. And I said, OK, what's actually going on? And so then we correct it and we've completed the sandwich. Now we have the correct model of understanding in context.  
Now with the correct understanding, I can tell it. Let's go ahead and finish this work now, OK?  
OK, I think all this makes sense. Let's put all this together. We need a branch for the work and I'd like you to use a task list and sub agents to start to with to complete to a point where I can review. This is that metacognitive thinking I'm talking about right now, right?  
The metacognition of thinking about the plan that we have to do rather than just doing it.  
Because I am now acting more as the supervisor or the director for my agents than I need to do the work directly myself.  
Because it's in an intermediate state right now, it's not complete. It's sort of wibbly. It's it's not fully formed. I'm asking it to get to a point to where it feels it's complete, to complete its analysis. Then I'm going to read it and I'm going to let you guys read it too.  
Because we're going to push it U to a branch in this git repo and we'll all be able to see it.  
We have the collaboration guide here.  
Like it's gonna create a few others. I gotta zoom out just a little bit. We have the team roles. We have the contributing code owners PR template.

**Val Levitan** 1:10:16  
Please share your prompts. The more prompts you share, the more education we get.

**Aaron Bockelie** 1:10:21  
Yeah, I will.

**Val Levitan** 1:10:24  
I wonder if you could ask Claude to summarize all the prompts you used here.

**Aaron Bockelie** 1:10:32  
I have a way to do that.

**Val Levitan** 1:10:40  
I personally learned by looking watching you do prompting.

**Aaron Bockelie** 1:10:46  
Mhm.  
O I'll just paste this in here.  
I'm just going to share this with you guys. This is sort of the ongoing conversation. You can see where I prompted things.  
And then finally, Andre, this is a prompt for you. Let's use the GitHub well-formed project scoring. Not for open projects, but you know templates, etcetera. Stuff generally kept in dot GitHub. These all affect the quality of GitHub and cause it to look much better and are is much more usable.  
Because right now you're fairly ascended beyond using GitHub as a file, a drive folder right now.  
And this is a way to really improve this a lot. We can add labels, we can add the teams, we can have all this other stuff configured in the project. We have to do this before we can even we got a crawl. We can't even crawl. We're sitting.  
Now we're crawling. We're setting U the GitHub roject correctly, understanding who's doing what, and we have to remember you can't just basically.  
A coding agent is is like a rocket. It's like gas. It's like a fuel. If you just set it off with no control, it's just an explosion and does nothing but break things. Once we've contained it and shaped it and put it into a structure, an engine, a rocket, a shape, something, whatever.  
Now we can force a direction for it. We can give it some direction and control and that's what we're setting U right now.

**Val Levitan** 1:12:27  
Do you guys understand? Do you need a pause?

**Andrei Bosik** 1:12:34  
I understand. Uh, that uh, we uh.

**Irina Shishko** 1:12:35  
Um.

**Val Levitan** 1:12:37  
I I for for example, I understand that Irina is a little bit struggling. My suggestion to you and I I will share this transcript with you, but huddle together and discuss this afterwards.  
For example, it looks like Eugenia Karevsky gets everything.  
OK.  
Maybe you should conference together after this.  
Sorry, Andrea, I interrupted you.

**Andrei Bosik** 1:13:08  
I would like says that I agree with Aaron that we in steady when we can, when we already know how we can work with GitHub and now we can create some rules how we work in GitHub.  
And how we work with GitHub and how we store our code.

**Val Levitan** 1:13:35  
I think what Aaron is doing, he's educating Claude and allowing Claude get educated on the GitHub.

1:13:42  
Yes.

**Aaron Bockelie** 1:13:44  
Yes.

**Val Levitan** 1:13:44  
That that's what he's saying. He's he's.  
Taken Claude. He's he sees Claude is a his. He compared Claude to a rocket.  
So if you do not.  
Build your rocket correctly and you just put gasoline in it and light it up. The rocket is not going to fly, it's going to explode and there's no use to that force. So you're taking a very useful tool like quad code.  
And you're because you're not doing it correctly, it just explodes on you. It doesn't help you, it just creates a mess.  
But if you prep it correctly, if you educate it, if you.  
Allow code cloud code to learn your git structure, GitHub structure interactively with you while you are leading the education. You are the chief educator.  
And Cloud code now took able to wrap its knowledge around the whole situation. Now it becomes a productive tool.

**Aaron Bockelie** 1:15:12  
O What we see here is the work that's now finished. It's ready to commit into a branch. I'm going to tell it to do that.

**Val Levitan** 1:15:24  
And by work, what do you mean work? What kind of work?

**Aaron Bockelie** 1:15:26  
So all six tasks have completed. Here's what's on the docs team collaboration handbook branch. We have a centerpiece talking about from Figma, platform flow and and diagrams for that. We talk about team roles.  
This is only one flow, by the way, guys. This is the one that Igor is concerned about and the one we've been talking about. There are many flows and we can refine that later, right? Think about how many flows there are for doing development. A machine way, a machine flow. Maybe you have hardware you want to work into this, maybe you have.  
Financial stuff. Maybe you have game play. There's a million ways to flow and we can continue to add that to the documentation. Now that we have the basic structure, we have team members.  
Ownership, boundaries, escalation. We have a process handbook. How do we branch? How do we review? How do we do handoff? How do we do testing? How do we do releases?  
Terms in English and Russian documentation index, linking everything, entry point for contributors, vulnerability reporting to Andrei, file ownership and auto reviewer assignment, standard pull request sections, bug report templates, feature request templates, template chooser configurations.  
These are all configurable in GitHub now.  
Think about how much trouble we have configuring some templates and stuff in JIRA. It's all suer duper manual. We just let a coding agent configure everything for us just now.  
So what I've done is I've said I think this is great. Let's go ahead and create a branch, push it and go ahead and write a pull request for this.  
And we're all going to look at this together now. Here's the repo, right?  
I'm going to refresh the page.

**Irina Shishko** 1:17:24  
Oh.

**Aaron Bockelie** 1:17:24  
And I'm going to go look at our other branches.  
Let me make sure we've got that there. Is that the wrong repo? Yeah, sorry, let me get to the right one.

**Ihar Hrybko** 1:17:28  
I think it's wrong ripple.

**Andrei Bosik** 1:17:30  
It's the wrong helper. Yeah, yeah.

**Aaron Bockelie** 1:17:39  
Here we go O team collaboration handbook and GitHub roject infrastructure. Here's the ull request. So I created this. I created this. Not really.  
We can now look at this if we look at this now from the branch perspective.  
We can see the difference.  
We can go into docs. We can look at the summary that talks about what this is. We can look at the development pipeline. How is it supposed to work?  
What's the overview for this look like?  
They let's let's make this a little bigger.  
Figma Design, Design Specs, Components Library, React components, front end app, back end API, CI pipeline, Docker to EGM deployment installed platform.  
This is sort of the general gist of it right here.  
We have an understanding of who's doing what and so forth. We have a glossary of terms EGMLGS, SAS, Tito, JAM, AFT, CC, talk, progressive, DSP, Passport, Bill Validator. It took months for me to extract this stuff out of you guys when I first started working with JVL to understand what the hell SAS is.  
Here it is right here. Lot accounting system, industry protocol for communication between gaming machines and casino management systems.  
Have all this in here and we can define who does what. So now there's no question of who's doing what, right?  
Now, does anybody particularly disagree with this right now?  
Are you reading through this on your own right now on your own computer?  
I want you to do that. I know that we're kind of out of time, but I think it's really important because what I want to do is I want to get group acceptance from you and I want to merge this right now.  
But I'm not going to do that until I can get at least some sort of thumbs up.

**Val Levitan** 1:19:47  
Let's, let's, let's actually, let's actually do that. Let them read it on their computers and let's vote on it. Can we take 5 minutes to read? Turn off your cameras, turn off your microphones, read it, and then we'll vote.

**Aaron Bockelie** 1:20:04  
I want you to put your feedback in this pull request right here. OK, I put the link in the chat.  
Type up what you think.  
You could check the check box off on the test plan if you'd like.  
And I'll wait. I'll set a timer for 5 minutes.  
As you add comments, they will start showing U here. I'll leave my screen share on.

**Val Levitan** 1:26:16  
Great thumbs up.

**Aaron Bockelie** 1:26:30  
All right, so make sure your comments are on the GitHub.  
Pull request not between each other. Did you add any commentary about? Yeah, this is great, I looked at it or anything. You need to add some sort of feedback. You cannot make a pull request in a vacuum.

**Evgeny Kharetski** 1:26:49  
But.

**Val Levitan** 1:26:52  
Sure, take another minute.  
Let's, uh, let's give it another minute. It's going to be quarter to the hour.

**Aaron Bockelie** 1:27:00  
OK.

**Val Levitan** 1:27:04  
Can you display a timer here?

**Aaron Bockelie** 1:27:05  
Oh.

**Val Levitan** 1:27:07  
Let's do 3 minutes.  
We need your comments, please.  
In GitHub.

**Aaron Bockelie** 1:30:23  
Right. Did you guys type up a little bit of a summary of your thoughts?  
I see, uh, Evgeny. I see Vlad.  
Anybody else?  
Andre.  
Refresh.

**Andrei Bosik** 1:30:48  
One second, I would like add a command using quote quote.

**Aaron Bockelie** 1:30:50  
Sure.  
OK.

**Andrei Bosik** 1:31:05  
I finished.

**Aaron Bockelie** 1:31:06  
Excellent.  
I want to point out that what we did was exactly this right here.  
Distributed context capture. This is a variant of this in which I did a bunch of work with my tools, proposed a pull request and potentially you guys are looking at all this and adding your comments in here.  
And then I'm going to be the responsible party for my own pull request, and I'm going to synthesize a response to this and get it merged in.  
Now, I don't know exactly what role I play in this project. Who's the person who would be the I agree with this from a PR perspective?  
Who's the Val has always had a fun sort of it's a democracy until it needs to be a dictatorship kind of thing. I I I kind of that's what's happening here. And I'm at the dictatorship mode where I just need to say I this is the right way to do it and I'm just going to do it now. But I wanted to get your feedback before I did it.  
Everybody OK with this?  
Alright.

**Val Levitan** 1:33:09  
Chris, you know.

**Aaron Bockelie** 1:33:18  
O All I'm going to say is we have some feedback. Let's consider it and amend our work, and then we'll merge it.  
Claude's going to go read the feedback now.  
Reading all of your comments.

**Val Levitan** 1:33:38  
We have heart stop in 5 minutes.

**Aaron Bockelie** 1:33:39  
I'm.  
So I've read your comments and I agree. That's why I'm asking Claude to go look at it, because I'm going to endorse Claude's perspective on this, right? Claude and I are in alignment with what needs to happen.

1:33:41  
OK.

**Aaron Bockelie** 1:33:57  
From Andrei, from Vlad, from Evgeny, Irina and Alexander.  
O We're going to fix the stuff.  
O We've fixed the code owners.  
And then finally, I'm going to add my own review to myself, which is this one here. I'm going to add this to the chat so you can read it as well. So I'm going to that's a prompt too.  
I'd like to add one thing myself. Let's make that main readme more professional and clean it U with reference to this have some concerns separation in it.  
I'm going to let it sort of work through it. I'm I'm minding my context. I'm about to the end of this session. Not a big deal, but it'll work. The current readme is a 293 line monolith mixing backup, back end setup, front end setup, Docker instructions, troubleshooting and development tips with no separation. You said you wanted to clean it up yourself.  
Actually, no.  
I need to correct it. No, I'm lazy, Claude. I want you to clean it up for me.  
I'm going to say, actually, I want you to, and I put a little :) in there because it's OK to have a little bit of banter in these tools. It actually helps the conversation.  
Fair enough. Let me rewrite it with proper concern separation and references to the new docs. I know it's a little unfair to do this after I gave you the PR. I've amended it, but trust me, it'll be better. That's kind of where the dictatorship is coming into play right now.

**Val Levitan** 1:36:12  
You don't have to be polite, but I need to know the truth, not not from you. I need to know the truth from the Minsk team. Is are these meetings useful to you? If not, let's not have them.

**Aaron Bockelie** 1:36:14  
I know.

**Irina Shishko** 1:36:33  
No.

**Anton Seregin** 1:36:34  
So what?

**Irina Shishko** 1:36:39  
Yep.  
It's my.

**Aaron Bockelie** 1:36:43  
Yes.

**Val Levitan** 1:36:46  
Who I'm going to continue inviting you to the meetings. If you feel that these meetings are not useful, don't come.

**Irina Shishko** 1:36:47  
Yeah.

**Val Levitan** 1:36:57  
My goal, my, my goal in the company, my goal is to separate you from those that want to learn and those that don't want to learn.  
I'm OK with that.  
Do not come to the meetings if you don't need it.  
Come to the meetings and also tell me specifically what you're interested in, because Aaron can always find an expert for you.  
Aaron is incredibly connected in the industry. He can find the right expert if you need it.  
This meeting is over now, yes.

**Aaron Bockelie** 1:37:43  
We're just waiting for this and I want you. I want to get a 32nd reaction with what happens to this project. I want you to see what it looks like right now with all of the kind of metadata on the main page and as soon as this is done.

**Val Levitan** 1:37:52  
Yeah.

**Aaron Bockelie** 1:38:00  
Um, let's do this.

**Anton Seregin** 1:38:06  
It was not the.

**Val Levitan** 1:38:08  
The.

**Andrei Bosik** 1:38:08  
No.

**Anton Seregin** 1:38:29  
Коктейль, то есть сгенерирует это шаблон, который можно будет перейти сползать.  
Соответственно других репозиториях.  
Оно это документация, она же должна быть живая, то есть мы можем вносить правки, то есть делать полуверсты.

**Val Levitan** 1:38:39  
Вы.

**Anton Seregin** 1:38:48  
И ну задача, чтобы поддерживать её актуальной.  
Я понимаю, ну контексте именно документациями о тем репозиторий.

**Val Levitan** 1:39:00  
Я я думаю что опять я не инженер, я экземпляров, вы понимаете да я я не инженер.  
Мои объяснения не совсем точное я вам скажу, что я понимаю.  
Я, я понимаю, что вы назвали, я их называю саунд бац. У вас было много саундбар лиц правильных.  
Но вы помоему все это перенесли в очень литературную.  
Литературном смысле.  
Вы сейчас стали свидетелем митинга, которые.  
Развивается.  
И вас просто подтянули вас, как бы взяли, дернули, подтянули и посадили в этот митинг вы попали в какую то.  
Ну в определенной какой-то вакуум небольшой, поэтому Вы смотрите сейчас на это все в литературной форме цифровом режиме.  
Если вы можете смотреть более в аналоговом режиме, более таких.  
В красках то вам будет легче на это смотреть мы наш голод, чтобы вас научить использовать склад коуст для применения во многих.  
Ну во всех жизненных случаях.  
Не только в этом, это не конкретный пример. Это один из примеров, но это.  
То есть на этом мы не начинаем и заканчиваем на этом, это это как бы.

**Andrei Bosik** 1:40:36  
Маленькая часть возможности Клода, где мы можем его использовать.

**Val Levitan** 1:40:39  
Танкер танки Андрей пошептался.

**Irina Shishko** 1:40:41  
Научиться его использовать.  
То, что мы.

**Val Levitan** 1:40:45  
Мы хотим показать вам, как правильно пользоваться промывками, как строить правильно промыты, а где можно использовать это и чем больше вы присутствуете на этих митингах, тем больше у вас раскроется о я могу здесь это сделать. А почему бы мне здесь не попробовать?  
Пробуйте, делайте смотрите, но какой смысл?  
Кладку имеет огромнейший потенциал, это может как пир пир переопредели, пир программа или просто почистить что-то или привести что-то впорядок или найти какую то информацию или даст какую то инструкцию.  
Лимита я в этом не вижу, я пользуюсь кладкой. Вот у себя я не программист я не доверяла, я ничего не произвожу, но я пользуюсь вклад кодом у себя каждый день постоянно.  
Я нахожу пути как его пользоваться. Я учусь от Елена как правильно строить фронты? Я раньше строил промыты.  
Пойди принеси сделать положили унеси.

**Andrei Bosik** 1:41:47  
Но все, что начиная да.

**Irina Shishko** 1:41:47  
Ох, мы все так пользуюсь.

**Val Levitan** 1:41:49  
Сейчас.  
Сейчас я совершенно это не делаю. Сейчас я говорю, у меня есть такая то проблема.  
Я не знаю как решить вот это, но я бы хотел бы получить вот этот результат.  
Я не знаю этой темы, научи меня, как правильно думать.  
Разложи мне все по полочкам, а вот я получил что-то сильно такое умное, написанное, а разлом.  
Скажи мне это всё?  
Simplified напиши мне, как будто бы я десятиклассник.  
Вот такими продуктами я сегодня пользуются, но когда я смотрю, как, например, моя жена делает промт или мои дети, они делают так, я делал 2 года тому назад. Расскажи положи унеси сделай.  
И когда ты перестаешь думать баннеры в цифровом режиме и начинаешь рассуждать, а вот я не понимаю это, а как мне здесь лучше сделать?  
И начинаешь эту этому учиться, то клад процент по вкладу это совершенно другое дело.

**Aaron Bockelie** 1:43:00  
А.  
Товара probably место фима умереть, если за тизер саша окей гайс то урагана.  
Я скоро ещё вида берегов даст я спал.  
What we just completed today, that's the next prompt, by the way, is that we established the basic foundation of the dynamics of this project. Who are the code owners? Who are The Who is the team?  
What are the responsibilities? And we all sort of agreed to that in this too. We established a pattern for documentation. These all will now impact how this coding agents work. What we're going to do is something that we could not have done until we had got this done just now. So the the previous work we just.  
Spent an hour and a half doing was mandatory before we can do this step. This is the next step to happen and what I'm going to show you is a feature that was literally released yesterday which is called Teams.  
Claude teams, not subagents, but teams.  
Teams create completely autonomous coding agents that have dialogue back and forth, have input inboxes, little mailboxes where they send each other messages and chat with each other in a dynamic.  
Because I just understood who you guys are, now these teams are are my delegate proxies of you in here. The delegate proxies of the team members is going to run when I do this now and I tasked it with.  
Let us begin to understand how to grow the documentation to be more mature with automation.  
So it's going to complete the work here.  
So it's going to create the analysis branch for this. I started a new session to do this and what what's going to happen is it's going to read the code owner, code owners. It's going to understand who you guys are. I just want to see watch. I want you to observe the beginning of this.  
So it's going to start the explorer and it's going to look. Let me also look at the team structure from code owners to plan the agent team while we wait. So it's doing the planning for this right now. It's going to start a couple actual.  
Uh, code owner agents.  
To represent you like a weird virtual hologram copy of Alexander and Anton and Irina and Vlad and Evgeny. It's going to act as you on your behalf all at once to come up to a rationale for how we're going to truly enterprise document this at the enterprise scale and scope.  
And that's where I'll leave this right now. I will let the results of this be a branch in the git repo, which should be done in about 20 minutes.  
By doing this, you can save a lot of time on meetings and conversations and things. This is collapsing the bureaucracy of all of this decision work.  
So any questions about what I just told you? Does it sound like a fantasy? Like fake? Like is is Aaron just making up ******** right now? Cause that's kind of what I would have thought if I hadn't known about this kind of stuff.  
I see Irina is looking very dubious. That's the word. That's the English word is dubious. She has that look of mirth on her face right now.

**Val Levitan** 1:47:44  
Fantastic. Fantastic meeting. Love it. Thank you very much everyone. Wishing you a great evening. Bye, bye. I will place. I will place the transcript of the meeting here. Bye, bye.

**Irina Shishko** 1:47:49  
Yes.

**Evgeny Kharetski** 1:47:52  
That's fine, yeah. Bye.

**Aaron Bockelie** 1:47:52  
Thank you.  
Bye.

**Irina Shishko** 1:47:58  
Hi.

**Andrei Bosik** 1:47:58  
Goodbye.

**Alexander Korochkin** 1:47:59  
Right.

**Val Levitan** stopped transcription