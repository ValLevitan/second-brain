**Val_Aaron-April-3-2026-20260403_082319-Meeting Recording**

3 April 2026, 12:23pm

22m 1s

**\
Val Levitan** started transcription

**\**
0:03\
So.

**\
Aaron Bockelie** 0:03\
So.\
Bot has been diligently working on this this morning already and also last night find the.\
Window here.

**\
Val Levitan** 0:23\
I can tell you that Doradka and Dima Chudinov and the other guy that works with Dima.

**\
Aaron Bockelie** 0:30\
Uh huh.

**\
Val Levitan** 0:32\
They started code clean up with cloud code, their own code. So Beratka is documenting Omni.

**\
Aaron Bockelie** 0:39\
Yeah.

**\
Val Levitan** 0:47\
And the other two guys are documenting the back office.

**\
Aaron Bockelie** 0:52\
OK.

**\
Val Levitan** 0:53\
So that has has started for us and I\'m very excited about it.

**\
Aaron Bockelie** 0:59\
Good. Do you see this screen? I\'m kind of looking around. OK, so first of all, which is?

**\
Val Levitan** 1:02\
I do see the screen, yeah.

**\
Aaron Bockelie** 1:10\
A cool tool I found was called AB top. So and have you guys take a look at a tool called AB top which starts for agent. B top is what this stands for and you can see what it does is it lists all the cloud sessions they have running and what it\'s actually running for children and stuff. It\'s almost like.\
A process monitor, but it\'s for Claude, so helpful, but more importantly is.\
Waze now has a single Rust binary that\'s very, very fast, has our fancy little text here, and one of the things that we can see now when we\'re running Waze is the current session of how it\'s thinking.\
So these are the disclosure of commands that it\'s got, right?\
And we can actually start to see how Waze actually runs. So this is kind of like you would call it considered an animation. So this is over a session of maybe 45 minutes worth of work.\
And we can see the pattern of it driving through and making all the decisions about which ways to steer this particular session.\
O What we can see in here is all the different ways that got triggered during the conversation as I was working.\
It also shows how many turns distance from the start of the conversation to the head of the conversation. These little markers indicate where in this. So these two little guys here represent the predicted next area of ways that we\'ll be executing for this system.\
When to redisclose Waze and steer it and everything. Basically it\'s transparency about how Waze is actually working.\
Because Waze can predict how the conversation is going based on previous history, it kind of zeros in and centers on what\'s happening and make sure to prepare the next set of ways available for things. So this is available for any of the conversations if you have a really huge one.\
It says the duration was 2 hours and 42 minutes. So if I were to play this.

**\
Val Levitan** 3:23\
Mhm.

**\
Aaron Bockelie** 3:25\
We can see how it runs against a very large conversation that happened.\
O the other thing I\'m working on.\
Is over here, which is multilingual support. O multilingual support is essentially. Let\'s see if I can find it here.\
So this is the list of languages that Waze will support. Of course, your concern is in here as well, right here. So we\'ll have Russian support natively for Waze so that everybody can just type in.\
Their native language and the English description of the way will still steer Claude, but all of the detection of intent, including potentially tuning all of those little crazy slang words and stuff if you wanted to, might be able to be integrated in a ways.\
I don\'t know for sure how well that will work, but if you have something that you like, I don\'t know what the slang words are, but if you have something about shipping something or debugging something or investigating or whatever that.\
You know, kind of activities are, and it happens to coincide with something you\'d like to tell Claude. You can connect the dots. Here\'s the slang. Here\'s the related ways. Let it go, figure it out. And so when somebody says that word in Claude code.\
It\'s possible it will invoke that. It will invoke that particular way, possibly and.

**\
Val Levitan** 5:19\
So is this is this the part of? Is this the part of the new release of your ways? So that will already be wedged into it. The moment you push it out, we\'ll we\'ll download it.

**\
Aaron Bockelie** 5:26\
Yes.\
Yes.

**\
Val Levitan** 5:34\
And our our transcript will just automatically behave better.

**\
Aaron Bockelie** 5:35\
Right.\
If you start typing to cloud code with ways in Russian, Russian prose, meaning typing to it, will trigger the same ways as if you had typed it in English.\
Because what I\'ve done is I\'ve added what\'s called an A multilingual embedding model. It\'s about 120 megabytes of neurons that can relate words to words. And So what I do is I build Russian stem things. Let\'s see if we\'re if we\'re there yet.\
Do it. So I\'m about to kick off Claude building all of the stubs right now. So you have to remember, I don\'t speak most of these languages, so I\'m doing the best I can using a language model to help describe them, right? So see how it\'s able to find all the different ways and all the descriptions.\
It\'s about to run a whole bunch of agents in all the different languages to be able to write all of the different ways, translations, triggers for all the different languages. And So what I would appreciate since this is being recorded is this once this gets pushed up and Andre can verify he can run it and it sort of.\
Works.\
I\'d like him to everybody that needs to who\'s using Waze should understand generally how it works, and if there is tuning for Russian Waze, they should feel free to submit essentially a.\
Pull request or at least a note or drop me a message about what is correct and what\'s wrong or what I should add or what I should remove.\
Then I can use. I can make those changes to tune the Waze detection for Russian to be a little better than just whatever machine translation is.

**\
Val Levitan** 7:45\
So a stupid question. What Lena and Clayton are working on and being implemented through microservices, how is it different? And I know it\'s a stupid question, but.

**\
Aaron Bockelie** 7:58\
So it\'s it\'s not a stupid question because it\'s for a different purpose. Lana and and Clayton are building a universal language tool that could be used anywhere, not just in cloud code. This is kind of highly specific to cloud code. It\'s all contained within it.

**\
Val Levitan** 8:15\
I see.

**\
Aaron Bockelie** 8:17\
And what what Clayton is building is a generalized service that allows you to connect and do all of, you know, ask and request kind of translation for things, which isn\'t as fast as how this works. So this system works extremely.\
close to the hardware itself, so it\'s invoking CPU time to do the computation locally on the computer. Because what you don\'t want to be stuck with is making an API call to an Internet connection every.\
On every single tool, call, turn or whatever, because the one time it doesn\'t work, then your whole cloud code conversation would hang. So this is all local and executes on the computer locally when it runs. It\'s it\'s designed for high performance so you don\'t have.\
You know, problems with all that.\
So we\'re gonna start with Japanese, German, Spanish and I forgot what AR is.\
Can\'t remember what language code. Anyway, the the point is, is that this supports both symbolic language like characters like Chinese and Japanese, as well as regular like Latin root languages as well.\
So it\'s just kind of nice to be able to finally get to this point.

**\
Val Levitan** 9:44\
And it\'s and again, this is part of Waze, right?

**\
Aaron Bockelie** 9:44\
Um.\
Yeah, yeah, yeah.\
So ways.\
These are all the ways that are in the system. So here\'s the locale English model English and the way I\'ve written all of them right now because I\'m I speak English, so I\'ve defined all these, but there\'s no reason you can\'t add any other set of ways for any other topic in any other language.\
Which?\
That\'s very extensible, allowing you to write steering ways for things. And the other thing that I think is really helpful here is we can start to see sort of how.\
Which which way is trigger most often by the type of trigger for match semantic for example?\
I\'ve also started to.\
Build in. Let\'s see here. Governance. Oops.\
Sister.

**\
Val Levitan** 10:53\
Yeah, I call it constitution.

**\
Aaron Bockelie** 10:56\
So I don\'t have a lot of governance set up yet, but it\'s there. It\'s just this project doesn\'t have governance models, but you\'d be able to add whatever governance. So like if you had it, if we were to take all of the.\
If there were, if there were authoring or coding standards for electronic gaming software, you could add governance laws to this, maybe by jurisdiction for example.\
And then you could write ways about how it\'s supposed to be coded in that space. Like, let\'s just say it was like, here\'s a hypothetical.\
Imagine a theme had fully adopts cloud code to be able to work with him to write his math and he has per jurisdiction math models for things or per game style type, finite math versus full, you know, infinite math and whatever.

**\
Val Levitan** 11:49\
She does.

**\
Aaron Bockelie** 11:53\
He could have Claude write a bunch of ways about how that works and then connect that back to jurisdictional or other sort of rules and then have full traceability from here is the actual rule of how it\'s supposed to be to this is the way the coding agent respected the ways to here\'s.\
The code created from that with that way.\
So that\'s where.\
This sort of model comes into play where we\'re looking at a session and we can see where anywhere along the turn what was executed. These turns, which is every single tool call or chunk of work that Claude does.\
Is traceable back to if a way was triggered or not, and if if it\'s not, it\'s just silent. If it\'s triggered, it triggers the way. And this means that because we have this record of all of the old sessions, you could.\
Look at every single decision made during the turns that are happening during these turns, right? And actually then.\
Prove that you were at least following the guidance that was written.\
Um, for example, if we look at.\
This particular way you can see here now on the start of my session.\
Let me go to the top.\
I said we have an open issue we wrote to ourselves about multilingual stubs. Like that was the first thing I said on a brand new fresh session, right?\
And we can see how it corresponded directly to the GitHub delivery software way because I said issue and things like that. And then what happened is, is that it found GitHub issues and it ran issues view and we can see on epoch 4 which is.

**\
Val Levitan** 13:39\
Mhm.

**\
Aaron Bockelie** 13:51\
1/2.\
3-4 where it switched to a branch, it got Waze guidance on delivery.\
And then it also got Waze guidance on commits at the same time. See how Eoch 4 fired for both of those. So it got both the commits and the delivery way. And then the very next thing it did was it said.

**\
Val Levitan** 14:04\
Mhm.\
Yeah.\
Hmm.

**\
Aaron Bockelie** 14:20\
Uh, do you need a? I said. Do you need a task list?\
And then it said no, the issue is detailed enough. Let me do that and we can see in tasks. You see how it triggered the task way because I have a particular way of running tasks too. All of these got injected as it runs through stuff.

**\
Val Levitan** 14:33\
Mhm.

**\
Aaron Bockelie** 14:40\
Eventually it got to a point to where it went to something called check pull and it was kind of looked like it was checking stuff here and and it just keeps going and going. At some point I just can\'t even keep up because it\'s too many things going on for it to do its stuff. But then we\'re right here.

**\
Val Levitan** 14:49\
And.

**\
Aaron Bockelie** 14:58\
This is really fascinating because it turned 30, which is way down the list of stuff that it\'s doing here.\
It launches these agents. Do you see the agent here doing the work?

**\
Val Levitan** 15:10\
Oh.

**\
Aaron Bockelie** 15:12\
The agent itself also gets the steering because this is the main agent. That\'s me and Claude code directly talking to each other. And in this one we see the agent is getting information getting ways about branching so.

**\
Val Levitan** 15:26\
So cool. It\'s incredibly cool.

**\
Aaron Bockelie** 15:27\
A fresh agents running and it it it\'s quite so we can see here a couple of new ones. You know basically it it needed it probably decided I need to run and look at the architectural decisions. So I\'ve got ways steering for ADR.\
And then it got, uh, another, you know, it\'s just kind of just running and doing its thing essentially.

**\
Val Levitan** 15:51\
So.\
It\'s it\'s interesting.\
On one hand, you keep on working on different projects. On another, from another side, you\'re developing your own ways, which kind of steers.\
Like you never have to come back to it. You already developed your ways and it.

**\
Aaron Bockelie** 16:16\
Just works, yeah.

**\
Val Levitan** 16:17\
Just just accelerates actions.

**\
Aaron Bockelie** 16:21\
Right.

**\
Val Levitan** 16:22\
On your behalf, because you already spoke about it, it\'s already known. You don\'t have to regurgitate it all the time, one-on-one with Claude. Otherwise you would have to refer to it every single \*\*\*\*\*\*\* time.

**\
Aaron Bockelie** 16:30\
Right.\
Right. And it got old. It got \*\*\*\*\*\*\* old. I was tired of that. I\'m like, enough of this. Let me do it. Let me build this thing. And so that\'s kind of what this evolved into.

**\
Val Levitan** 16:43\
But how did you?\
Come up originally with the charter with with breaking it down to. I don\'t know how do I call it in English chapters or?

**\
Aaron Bockelie** 17:01\
Um.

**\
Val Levitan** 17:03\
Subject.

**\
Aaron Bockelie** 17:05\
Well, OK, so it started out with.\
A long quite a while ago now, back last year was when I started the Waze project.

**\
Val Levitan** 17:15\
No, you can\'t drink ice things in the morning.

**\
Aaron Bockelie** 17:19\
I I I totally, I I absolutely can. It\'s Kansas, no.

**\
Val Levitan** 17:23\
No, no, no.

**\
Aaron Bockelie** 17:27\
Why not?

**\
Val Levitan** 17:27\
\'Cause you never do it in the morning.

**\
Aaron Bockelie** 17:30\
Why?

**\
Val Levitan** 17:31\
It\'s just it\'s not right.

**\
Aaron Bockelie** 17:33\
Oh, I love drinking ice stuff in the morning. That\'s like my favorite thing.

**\
Val Levitan** 17:35\
No, no, not in the morning. You got to do it in the afternoon, you know, by the grill. But you never do that in the morning. First thing in the morning, you always have a hot drink.

**\
Aaron Bockelie** 17:41\
Oh.\
So I have a hot shower. Did that work?

**\
Val Levitan** 17:51\
No hot shower you need at night because then your body drops temperature.

**\
Aaron Bockelie** 17:57\
OK, I\'m all backwards then.

**\
Val Levitan** 18:00\
You need cold shower in the morning. You need hot drink after the cold shower.

**\
Aaron Bockelie** 18:05\
I\'m gonna try that next week and see what happens.\
I I\'ll be honest, I drink the iced coffee sometimes just because I\'m lazy.

**\
Val Levitan** 18:14\
Yeah, lazy that. That\'s exactly what it does to you.

**\
Aaron Bockelie** 18:17\
Um, so the.\
Thinking basically was I\'m tired of reentering the same things all the time and I knew that anthropic gave the ability to write like a cloud dot MD. You know the the the instructions inside of a repo directory.\
And then they introduced skills and they introduced the other things. But it continuously kept bugging me that there was no such thing as a way of work. And I felt as a person, as a human.\
There\'s a way I go about doing stuff that I like, and that\'s kind of how the literally the word ways came about. First of all, it\'s like this is the way I want to do stuff. And then what I ended up started doing is I started writing out what I wanted to, how I wanted to do it. Literally the 1st way technically.\
And So what I started keeping was a directory just in my documents folder. I kept a list of ways like this is how I want to commit work. This is how I want to write. This is my writing style, like this kind of stuff, you know? And I started telling it that.\
And then pretty soon it got into I wanted to have a user scope cloud MD. You know the cloud definition that describes how to operate and work and.\
That\'s when I started collapsing it all into that. And then I realized that it\'s getting too big and loading way too much text to being in the context. And then it was starting to get stupid and forgetting and I had to keep reminding it. And then I\'m like, why can\'t I just keep reminding it during the process of working? And then that\'s when I was looking at hooks, which they had just introduced.\
So I started adding hooks to certain stuff, like every time I would type a word, it would just match a word and print that out into the session. And that\'s kind of how it started kind of condensing into a more structured sort of thing.\
I\'ve just been revising it as I go, basically.\
The other thing I\'ve done is I\'ve tried to make. I\'m probably going to rename this repo at some point.\
Because it\'s not really cloud code config anymore, it\'s probably going to be agent ways is what I\'m going to end up calling it. So you can kind of see I even made a cloud vibe coded logo of it and sort of describing it. So this is basically what it is.\
This point ways in code how we do things.\
Prescriptive, not proscriptive guidance triggered by context but not requested by intent and then inject in just in time before tools execute.

**\
Val Levitan** 21:15\
Very, very interesting.

**\
Aaron Bockelie** 21:17\
The other thing that I\'m working on too is making it not just for cloud code, it should work with any turn based coding agent that has hooks.\
So it could work with anything, not just cloud code. So that\'ll be really, really helful for that.

**\
Val Levitan** 21:40\
You\'re very cool. Very cool.

**\
Aaron Bockelie** 21:42\
But yeah, anyway, thought you\'d. I can\'t wait to to let you guys at it with.\
With Russian and the other things. So what\'s what\'s? Oh, here we go. This is kind of fun. So as we\'ve been talking.\
Uh.

**\
Val Levitan** stopped transcription
