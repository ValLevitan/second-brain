**CI Architecture --- Governance Framework Review (v5.1 Operationalisation)-20260430_080353-Meeting Recording**

30 April 2026, 12:03pm

26m 53s

**\
Val Levitan** started transcription

**\
Aaron Bockelie** 0:04\
and in it, and there\'s a lot of sort of traditions that are being created, minted.\
And I tried to take the direction of, there\'s no way in hell I personally would be able to remember all this stuff being brought into it. It would take a long time to figure it out. So what would be the takeaway from all of this? What would be something I could hold on to my hand with\
or items.\
And these were the four items that I decided, I think, that are the\...\
Intention of all of this together.\
So verification lives at boundaries, not at people. Compliance data is for steering the standard, not steering people. Standard has to be allowed to be wrong. And ceremony is debt.\
Those are the four principles I think that I\'ve read out of this document, these two documents.\
I\'m not discounting what you\'ve written, and I\'m not saying throw it away, I\'m just saying\...\
What\'s my takeaway? What is my if I if if there\'s something I need to remember and how to think and operate as a developer contributor at JVL? What is it? What does it look like?

**\
Val Levitan** 1:21\
But if I, if I may react to what you\'re saying, um\...\
And I usually agree with everything that you say, but I think you\'re slightly discounting the conditions and the environment that this is coming from.\
So\...

**\
Aaron Bockelie** 1:41\
I am aware of that.

**\
Val Levitan** 1:43\
So, this is\...\
an environment by which these ceremonies have never been practiced or used. This is all new. This is like going to university and your professor is lecturing on something and testing you on something.\
And one could ask, well, you know, the professor lays out so much cheer on me and so much textbook. When will I ever use it? Well, I don\'t know if you will ever use it or not. But somebody has to lay out the ground. Somebody has to lay out the rules. Somebody has to write it for the first time.

**\
Aaron Bockelie** 2:13\
Right.

**\
Val Levitan** 2:24\
Will you refer to it at all? Maybe never, maybe partially, maybe once in a blue moon, I don\'t know. But the fact that it needs to be laid out, it had to be laid out. And I\'m, I think, I think for the first time,

**\
Aaron Bockelie** 2:36\
Yeah.

**\
Val Levitan** 2:40\
It is a good job here on laying things out and relatively simplistic because when I read it and I\'m not a technical individual.\
I fully grasp on seventy-five percent of things, and whatever I don\'t grasp, I could have a conversation with Claude, and that will probably simplify things for me, but people that read it are the specialists that will use it on a daily basis. Will they read it once?

**\
Aaron Bockelie** 2:56\
Yeah.\
Yeah.

**\
Val Levitan** 3:11\
Yes, I\'m sure of it. Will they retain 60% or 90%? I don\'t know. But it will be a referral document to which either through Claude or maybe Claude on its own when it, you know, does something or tests something, could refer to it. I think it\'s a great.\
based document that should be saved as a ceremonial document. But I agree also with your statement. A blind.\
Ohh.\
Following a ceremony blindly is death.

**\
Aaron Bockelie** 3:50\
Yeah.

**\
Val Levitan** 3:51\
It just, it, it, it cannot be accepted, so any ceremony.\
is a subject of evolution. I fully understand that. But as a standard document right now, I would save it. I think it\'s\...

**\
Aaron Bockelie** 4:02\
Right.

**\
Val Levitan** 4:07\
Pretty good, pretty good.

**\
Aaron Bockelie** 4:10\
Well, I would say that\...\
I\'m just trying to take the human personal perspective of what do I have to remember to do and what do I have to adjust my behavior as? And I think it\'s perfectly okay to have what you guys shared as the reference, right? Like this is the reference architecture.\
for what it\'s supposed to look like.

**\
Val Levitan** 4:35\
Yeah, yeah.

**\
Aaron Bockelie** 4:36\
The thing I would caution against is naming too many roles with capital letters, like, you know, formal role names and things like that.\
It\'s okay to describe them that way, but kind of on the point of\...\
Number 3 there, it has to be allowed to be wrong if it if it\'s not working right.

**\
Val Levitan** 5:00\
But I think it\'s a general culture JVL. Everybody is quite tolerant of being wrong. That\'s okay.

**\
Aaron Bockelie** 5:06\
Sure. And well, it\'s not the people being wrong, it\'s the document being wrong.

**\
Val Levitan** 5:10\
No, no, I understand. Yeah, yeah, yeah, of course.

**\
Aaron Bockelie** 5:11\
Yeah. I think that just from an operating perspective, you know, like the things that really stick out to me, code owners is probably the very most important thing you could do because it just grants ownership of certain areas rather than it always being nebulous because it was SVN and one giant.\
server and oh, Hobble\'s responsible for the whole thing. Like, no, Hobble\'s not responsible for the whole thing, you know? I think just having that alone is a huge change, and I think it\'s a move in the right direction.

**\
Andrei Bosik** 5:41\
Yeah, like, okay.

**\
Val Levitan** 5:46\
And and and I and I would probably advise this team. And and I\'m only speaking from perspective of knowing the culture. It\'s not an engineering direction, but cultural direction. I advise you guys to really emphasize this. The ownership you need. You need to emphasize Pavel is not the owner.\
Let\'s look at the repository. I\'m giving you the ownership of this. And maybe it\'s not all your code, but I\'m making you the owner of it. And it needs to come with a form of authority.

**\
Aaron Bockelie** 6:15\
Yeah.\
Well, I think not only for not only authority, but responsibility too. So, like I last conversation, I used sheriff and sheriff deputies as an example. This conversation, I\'m going to use the admiral and the fleet for just a minute.

**\
Val Levitan** 6:24\
And I\'m all.

**\
Aaron Bockelie** 6:40\
Val is the admiral; he doesn\'t he sits in an office in a major city and watches his boats go out to sea all the time, and all of the code owners are all the skippers of all the fleets of all the of all the fleet, so the code owners.\
own that ship. They\'re the captain of every one of these ships. And DORA metrics is a way that you evaluate the performance of those ships on their missions, whatever they\'re doing.\
So what happens now is a well-run ship has its crew and its stuff going on and missions and things, whatever it\'s doing. And at any time, the Admiral might pay him a visit out at sea and say, how\'s things going? Is the brass polished? Is everything ship shape and organized? How are you, you know, have you accomplished what you\'ve\
what I told you to do, and they should be able to go, yeah, it\'s great, look, and just things are running.\
That\'s the normal thing. If they show up at a code repo and the code owners are responsible, but everything\'s\...\
messy and stuff is broken or whatever, you know, that should be obvious too. And so setting up a system of both the\...\
DevOps metrics and essentially the\
space metrics, you know, or the developer health metrics as well, like how much friction does a developer have to get work done, that kind of thing. Those are going to be your key indicators, Andrei.\
Um\...\
And I think that what happens is this, these docks that you shared with me become the, when the ships eventually have to come back to port to visit and convene and, you know, do whatever they\'re doing, that\'s the reference architecture that we should be thinking about. So you don\'t think about it all the time.\
I think there\'s possibly a\...\
Um\...\
The beginnings of, I hate to say more meetings or reviews, but there\'s the beginnings of some structured conversations you can plan over a long period of time. Say quarterly, let\'s just throw that out there to begin with. Every quarter.\
during quarterly planning, you could meet up and discuss the state of all of the products which are in these repos and kind of go, how well are we doing against essentially the Constitution that we\'ve written here about how to operate, because we\'ve never had that before.\
And this gives you a chance to kind of test out how well it\'s working, how good the product, the production out of these things has aligned with the goals of the company. So, you know, Sasha, are you\...\
Gonna, which which project would be you be a code owner of, as an example?

**\
Alexander Biratko** 9:39\
Lex dispenser.

**\
Aaron Bockelie** 9:42\
Which one?

**\
Alexander Biratko** 9:44\
Leg dispenser.

**\
Andrei Bosik** 9:45\
What now?\
No, it\'s examples. Sasha is code owner or in many repositories. I know.

**\
Alexander Biratko** 9:50\
No, no, no, no.\
Yes.

**\
Andrei Bosik** 9:56\
Ten repositories where Sasha Scodona.

**\
Aaron Bockelie** 10:00\
Okay, Sasha gonna have enough attention to take care of 10 repositories.

**\
Andrei Bosik** 10:06\
I think, yes.

**\
Aaron Bockelie** 10:08\
All right, so at a quarterly planning, when Sasha has 10 repositories of doing things.\
Sasha\'s need to gonna be able to essentially say.\
These are the performance metrics. This is what I\'ve delivered. This is how many cycles they\'ve ran. This is what version everything\'s on. These are my contributors. This is the velocity of my projects and what it contributes to JVL.

**\
Val Levitan** 10:34\
Basically, he\'s running, he\'s running 10 boats.

**\
Andrei Bosik** 10:35\
We can see.

**\
Aaron Bockelie** 10:38\
Yeah. Each one of these is a book of business for you, essentially. And the charter you hear, okay, we\'re going to switch in alleys again. I don\'t know if this one will land, but it\'s a franchise.\
You, you, this is your franchise operating agreement, essentially.

**\
Val Levitan** 10:55\
Yeah, that\'s a, it\'s going to land. Yeah. Franchise, they understand. Let\'s say McDonald\'s has a McDonald\'s franchise.

**\
Aaron Bockelie** 11:00\
Yeah.\
Right.\
You have to run McDonald\'s according to a particular way in order to keep the franchise license agreement.

**\
Andrei Bosik** 11:13\
Yeah, and if we use the metric, we can see all this.

**\
Aaron Bockelie** 11:13\
So\...

**\
Andrei Bosik** 11:18\
Indicators.

**\
Aaron Bockelie** 11:20\
Yeah.\
So, like I said\...\
The day-to-day of one of your employees, including the and including the general manager of a McDonald\'s or a brand or a group of McDonald\'s, which you might have, so Sasha owns 10 McDonald\'s and you know he doesn\'t own just one. What is he?\
thinking about day to day. He\'s not going to recite the word for word verbatim of the operating model of what\'s going on. He\'s going to be thinking about kind of the principles of governance and how it looks. And that thing I pasted there is kind of my, like, kind of distillation, what it is I would worry about.\
All the time.\
like on any particular day, stepping into the office and looking at what\'s going on and thinking about stuff.\
I would be like, okay, so what are we, how are we measuring? What\'s going on? How are we, what\'s our data look like? What sort of meetings have people had or not? Are you meeting too much? Like it goes both ways, right?\
And so thinking in that way, Sasha, of kind of what\'s the\...\
cadence when you\'re showing up and trying to drive things, what is it going to look like?\
I want to stop talking for a minute because I think that needs to sink in a little bit. What is it going to feel like running this this way?

**\
Val Levitan** 12:56\
I don\'t know if anybody could practically reply to this right now. Maybe we all have our own different images. But I think we\'re at the juncture, if I can sum it up, we\'re at the juncture right now that we all understand that we finally, in our minds,

**\
Aaron Bockelie** 13:03\
Yeah, I think so, too.

**\
Val Levitan** 13:18\
We finally arrived to a set of good decisions.\
They\'re not implemented yet, but we believe in them.\
We don\'t know exactly from a practical perspective how they\'re going to run and what we are going to encounter. But we know that we are facing the right direction.\
And we are about to embark on it.\
So the question that I would have to the team now is what\'s the next step?\
Who does what? I would like to outline a course for the next two weeks of what needs to be achieved with the next two weeks.\
Let\'s lay it out and let\'s come back in two weeks and see if we achieve that. That\'s probably the most productive thing that we can verbalize right now.

**\
Andrei Bosik** 14:15\
In my vision, as I type in file plan, I think we need to implement this.\
Standards to our.\
Infrastructure payment repositories. This repository is in very, very active development now, and we can see what work, what not work. Maybe we need something change or modify standards or reports for reports, for example, because reports cannot work.\
Correctly.\
First, some first days, for example. And after two weeks, we can see what good, what not good.

**\
Val Levitan** 15:05\
Well, the way, the way, and I don\'t know whether I\'m right or not, as I always, I make a disclaimer, I\'m not an engineer, but I cannot picture us.\
drawing a conclusion, what works, what doesn\'t, without trying to\...\
Produce a product out of a repository.

**\
Andrei Bosik** 15:33\
In the current repositories in infrastructure payment are already created artifacts. And we can see how many artifacts built correctly, how many jobs fails. For example, this is Dora metrics show.

**\
Val Levitan** 15:52\
But can we produce a product out of it?\
Product, I know that the product will have minimum viable options, it will have.\
you know, it will probably fail, it will not probably work correctly, but does it go through a cycle of being assembled and\...\
you know, get gets out of a production and whatever shape shape it is. And I don\'t know whether it\'s the right thing to do or not. I you know, but my logic tells me that\'s the only real true sensor. If I would be building a factory and I knew that, OK, I have my line going.\
But not everything that.\
deliveries are not their way. I don\'t have all the parts in, but I can run an assembly and I could run a fake assembly and get, let\'s say, A-frame of a car at the end. No doors, no steering wheel, but I could get through the assembly.\
And then I say, okay, you know, I don\'t have a transmission yet.\
that that sub-assembly did not arrive, but it kind of isolates me in thinking that, okay, now I can add this and now I can add doors and now I can add.\
A windshield, and I could add, you know, electrical.\
But does the frame come out?\
Can I get from Point A to Point?

**\
Andrei Bosik** 17:17\
Mm.

**\
Val Levitan** 17:22\
X.

**\
Andrei Bosik** 17:26\
Mm.

**\
Val Levitan** 17:27\
Am I, am I, Aaron, am I thinking incorrectly here?

**\
Aaron Bockelie** 17:33\
I think you\'re talking in too much detail right now.\
I mean, I think it makes sense, but also, we\'re kind of\...

**\
Val Levitan** 17:36\
Could be.

**\
Aaron Bockelie** 17:42\
Making assumptions about what has to happen before it\'s happened yet.

**\
Val Levitan** 17:48\
Val.

**\
Aaron Bockelie** 17:48\
What I?

**\
Val Levitan** 17:49\
So, how do we how do we know two weeks from now what what is working and what is not?

**\
Aaron Bockelie** 17:50\
What?\
Well\...\
I put some numbered items, just I just typed them up. I deliberately don\'t use AI for that, but this is what I\'m thinking out of this.\
Every repository has at least one code owner. This is the short term two weeks thing, right?\
Every repository has at least one code owner. The checks that I described in the previous document.

**\
Andrei Bosik** 18:14\
Mm.

**\
Aaron Bockelie** 18:20\
It run on every repo.\
So every commit to main with actions, essentially. Use actions to track it.\
When some sort of check fails 3 consecutive failures, you need to have a dashboard somewhere that\'s lagging this.\
So the idea is, is that in the next two weeks, so you get to a point to where you can instrument things. It\'s probably going to be more than two weeks, because you want at least two weeks of measuring things.\
So you need to be able to get to a point to where you can install some actions, some basic actions that just scan on a scheduled basis, looking for CA failure. Okay.\
Some sort of CI failure that happens multiple times of the same kind over 3 strikes throughout, American baseball style here, is essentially something that someone isn\'t catching or caring about.\
So Sasha owns 10 different repos and six of them are throwing consecutive actions. Sasha\'s got a problem because he needs to be dealing with that. And that\'s going to immediately surface that actually Sasha can\'t deal with 10 different repos simultaneously because he\'s overwhelmed.

**\
Andrei Bosik** 19:35\
Uh, I read all uh\...\
Numbers.\
What you sent, I also understand, but I think #5 need to explain for me.

**\
Aaron Bockelie** 19:50\
Right, so in this case, all of the things, all of these numbers, consecutive failures or not, or, you know, things running perfectly, that kind of stuff.\
You can\'t tie that to performance reviews. You can\'t tie that to how much money somebody\'s making.\
If you do, it will immediately turn into a gaming problem.\
Not like JVL producing slots games, but people will twist the numbers and do whatever it takes to fake it.\
consciously or not, to make it so that they look good.

**\
Andrei Bosik** 20:33\
Mhm.

**\
Aaron Bockelie** 20:34\
It absolutely cannot be that.

**\
Andrei Bosik** 20:35\
I understand.\
Uhh.

**\
Aaron Bockelie** 20:39\
It has to stand on its own merit. I would call it valor.

**\
Andrei Bosik** 20:39\
People.

**\
Aaron Bockelie** 20:44\
You know the word Val or what that means, right?

**\
Andrei Bosik** 20:47\
Mhm.\
I understand. Okay. I agree with your points.

**\
Val Levitan** 21:00\
Okay, so, so.

**\
Andrei Bosik** 21:01\
I think about this, too.

**\
Val Levitan** 21:04\
So I don\'t believe that moving this meeting any further will be, will give us any qualitative results. So we\'re at half hour mark.\
I think we agree with the course. I think we\'ve discussed everything that we could possibly discuss at this stage. I\'m actually quite pleased with the result.\
What I would like to suggest is now widening this knowledge within the company. So now we understand everything that needs to be done. Let\'s bring others into it. And let\'s focus on a two-week mark.\
For.\
these particular set of repositories for the transactional products.\
And let\'s measure it in two weeks, where we are.\
So, the next meeting, which is next week, I suggest\...\
You guys have internally?\
with the rest of the developers.\
Bring them on board.\
Let them to come.

**\
Andrei Bosik** 22:25\
I think we can start create report on these points and use use framework which I described, and for example, in Friday.\
On next week, we can create a meeting with Dima Chudzinau and, for example, Sergey Simonov and and show to them this report and speak about this and show our framework and our standards.\
because when we start create our reporting, maybe something changed in this document.

**\
Val Levitan** 23:16\
Okay, that works with me.\
And I\'ll have a meeting on the 14th.\
With this, with this team to review the performance.

**\
Andrei Bosik** 23:31\
I agree.

**\
Aaron Bockelie** 23:32\
Um\...\
What\'s your timeline for getting measures installed on all the repos, Andrei?

**\
Andrei Bosik** 23:40\
Mm.\
I think about, if you mean how often I would like to create this report, I think about one week.

**\
Val Levitan** 23:50\
No, no, no, no, no. Aaron said, when can you install these measures?

**\
Aaron Bockelie** 23:53\
No.

**\
Andrei Bosik** 23:58\
Ahh.\
I think 2 days will be enough to create this.

**\
Aaron Bockelie** 24:08\
Okay, so if you have two days to create it.

**\
Andrei Bosik** 24:11\
Yes, but maybe not, it can work not correctly first time. We need to understand this.

**\
Aaron Bockelie** 24:16\
Right. So here\'s what I think that you should be doing. I think you should take, let\'s just say you start tomorrow morning. That\'s Friday for you, right?

**\
Andrei Bosik** 24:28\
Mmh.

**\
Aaron Bockelie** 24:29\
So if you can get it installed tomorrow on at least one or two repos and verify that it works, you run some CI actions, you see it flagging, you have a dashboard, all that stuff.\
That\'s not enough to get it on everybody. So then Monday rolls around, you\'re going to get it deployed on the rest of them. Then Tuesday, you\'re going to check to make sure that they\'re actually working. Then you need a couple days of signals to actually show up to see that you\'re catching events. That\'s by Wednesday or Thursday. And then by Friday, you can eventually tell people that, hey, this thing\'s good.\
kind of probably measuring enough to get started. And that\'s where you take all the code owners that have all been defined in all of your repos, and you get a thumbs up from everybody. So that\'s one week. That\'s week minus one.\
That next Monday after that is when you would probably start collecting information for two weeks to see how things are going.

**\
Andrei Bosik** 25:13\
Uhh\...\
But I can use history, repository history. I can see.

**\
Aaron Bockelie** 25:27\
No.\
No, you\'re not. You\'re going to only measure from the point that when you started measuring because the act of measuring it and assigning code owners changes the behavior of how the repositories work.

**\
Andrei Bosik** 25:39\
Mm.

**\
Aaron Bockelie** 25:41\
That\'s bad data.

**\
Andrei Bosik** 25:42\
Maybe, yes.\
Okay.

**\
Aaron Bockelie** 25:45\
Because you\'re going to put everybody on notice next Friday that it\'s now being evaluated. And the very fact that you\'re telling them that things are being measured will change the way people think about it and react to this.\
And that\'s what you want to measure.

**\
Val Levitan** 25:58\
OK, so, so we moved it out by one week, which brings us to the twenty-first.

**\
Aaron Bockelie** 26:04\
Yeah, I think that\'s a safe way to do it.

**\
Val Levitan** 26:05\
Oh.\
So the next check for this purpose is the 21st. 21st of May.\
I, uh, it\'s my undertaking. I will circulate the calendar invite.\
Okay, I think that is enough for this subject and for this meeting.

**\
Aaron Bockelie** 26:25\
OK.

**\
Val Levitan** 26:31\
Half an hour, plenty.\
If anybody has questions, happy to answer. Otherwise, then let\'s retire the meeting.

**\
Andrei Bosik** 26:40\
Not now.

**\
Val Levitan** 26:42\
Okay, thank you everyone. And yeah, good luck.

**\
Evgeny Kharetski** 26:43\
Yeah.

**\
Aaron Bockelie** 26:47\
OK, thanks.

**\
Alexander Biratko** 26:48\
Mine.

**\
Evgeny Kharetski** 26:48\
By.

**\
Andrei Bosik** 26:48\
Okay, thank you. Bye-bye.

**\
Aaron Bockelie** 26:50\
BY.

**\
Val Levitan** 26:50\
BY.

**\
Andrei Bosik** stopped transcription
