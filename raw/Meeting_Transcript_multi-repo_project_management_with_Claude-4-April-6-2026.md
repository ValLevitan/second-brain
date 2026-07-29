**Mulit-repository project management with Claude-20260406_083626-Meeting Recording**

6 April 2026, 12:36pm

27m 30s

**\
Val Levitan** 0:03\
For joining.

**\
Aaron Bockelie** 0:06\
Sure.

**\
Val Levitan** 0:08\
So let me repost things here. It will be easier for me to do it this way.\
is the first part of the issue. If you could read it, Aaron, it\'s only for you.

**\
Aaron Bockelie** 0:20\
Mhm.\
I see.

**\
Val Levitan** 0:27\
Here\'s next part.

**\
Aaron Bockelie** 0:37\
Okay.

**\
Val Levitan** 0:39\
Here\'s the next part.

**\
Aaron Bockelie** 0:47\
Right.\
The.

**\
Val Levitan** 0:50\
Here\'s.\
Next part.

**\
Aaron Bockelie** 1:01\
Okay.

**\
Val Levitan** 1:05\
Here\'s the final part. One second.\
Hold on.

**\
Aaron Bockelie** 1:35\
Right.

**\
Val Levitan** 1:38\
Okay, so the situation, the way I understand it, is that\...\
When we deal with multi-repositories, Claude, just like a human who works on this repository, understands what\'s in the repository.\
And if it doesn\'t understand, maybe we can add certain set of documentation, specification, timing diagrams, schematic diagrams, whatever is required for that repository. And let\'s assume that we brought Claude as well as human fully up to speed for this repository.\
However, when we work on a product that then that that.\
Oh.\
Need needs needs to address itself to five repositories.\
It needs some sort of a\...\
Repository 0.\
as this team calls it, that has its tentacles to all other repositories in the form of a schematic diagram of some sort.

**\
Aaron Bockelie** 2:38\
Mhm.

**\
Val Levitan** 2:51\
So, maybe this is where you jump in and connect all the repositories together.

**\
Aaron Bockelie** 2:57\
Sure, let me read back to you how I understand things a little bit based on what you just shared with me and kind of what I already know.\
So you have all these repositories in Git now. Most of them came from SVN from before. And in SVN, in many cases, they were just branches in a very large SVN single repository server, right?\
They were directory branches off of 1 big SVN server. Is that correct?\
Like 3, four years ago.\
I just need a thumbs up or a thumbs down on that.

**\
Val Levitan** 3:36\
So, somebody, somebody has to answer.\
Do you understand the question?

**\
Evgeny Kharetski** 3:44\
Yeah, sober.

**\
Val Levitan** 3:44\
Can you repeat the question again, please?

**\
Aaron Bockelie** 3:47\
Three or four years ago, before Git was being used, and you were on SVN, this was all on one SVN server, and all of the different bits were in different directories inside of an SVN server. Is that right?

**\
Alexander Biratko** 4:01\
Yeah.

**\
Aaron Bockelie** 4:01\
And you would pull down subset branches of them, yeah?

**\
Evgeny Kharetski** 4:02\
No.

**\
Alexander Biratko** 4:04\
Yeah.

**\
Aaron Bockelie** 4:05\
Okay, so that architecture of thinking still persists now, even if we\'ve moved into Git, it\'s still thinking that way.\
So what you\'re looking for is to kind of recreate SVN again, first of all.\
And I would caution you against doing that.\
And I think that there\'s actually a middle ground that you can choose as an intermediary as you evolve this set of capabilities over the next couple of years.\
I would consider that every Git repo you have now is a mono repo for one of those concerns now, right? So if you have a Payment Hub and you have Flex POS Station and you have\...\
Whatever they are.\
Each one of those is a Git repo currently.\
And the conversation of do we use Waze or do we use CloudMD or these other things is interesting because I think that there is an opinion that\'s baked into this right now that certain people need all of the software accessible to them and others do not.\
First of all.\
How many on this call, raise your hand, need all of the repos simultaneously cloned on your computer right now to be able to get anything done?\
Nobody.\
Is the question understood what I\'m asking?\
I need, I need an answer.

**\
Dzmitry Chudzinau** 5:47\
Which more?

**\
Aaron Bockelie** 5:50\
Can you help translate Val or Andrei?

**\
Irina Shishko** 5:53\
And.

**\
Andrei Bosik** 5:53\
I think a lot more better to translate than I.

**\
Val Levitan** 5:55\
I, I can\'t translate, but I saw, I saw everybody\'s eyes and nobody was focused, nobody.\
Everybody was thinking about something else, and that\'s why nobody even heard the question. I actually, I think, no, I think I\'m the only one who heard the question.

**\
Aaron Bockelie** 6:08\
Okay, I\'ll ask it again.\
I\'ll ask the question one more time.

**\
Val Levitan** 6:15\
Everyone speaks English. Everyone understands English.

**\
Aaron Bockelie** 6:19\
How many of you, in the course of regular work, need to clone all of the repos on your computer to get work done, to get a single story done?

**\
Evgeny Kharetski** 6:30\
Yeah.

**\
Val Levitan** 6:30\
How many of you work with all of the reports on your computer at the same time?

**\
Dzmitry Chudzinau** 6:38\
No, ohh.

**\
Val Levitan** 6:40\
Not all. Nobody.

**\
Evgeny Kharetski** 6:41\
Mikhail.

**\
Alexander Biratko** 6:43\
No more.

**\
Aaron Bockelie** 6:45\
So, okay, so this now becomes the question of how much of the context of the other repos do you need for Claude to be able to work?\
And also, let me back one up from that.\
How many of those repos, when you\'re not working on everything, do you need as a person, as a human, without any AI, to get work done right now?

**\
Alexander Biratko** 7:14\
Maybe 10.

**\
Evgeny Kharetski** 7:17\
Tiger.

**\
Aaron Bockelie** 7:19\
10 repos.

**\
Val Levitan** 7:19\
At the same time, at the same time.\
You need 10?

**\
Evgeny Kharetski** 7:23\
No, no.

**\
Alexander Biratko** 7:24\
Just.

**\
Val Levitan** 7:25\
At the same time.

**\
Evgeny Kharetski** 7:30\
Most streamer the maximum.

**\
Alexander Biratko** 7:31\
Stay out of the box.

**\
Val Levitan** 7:34\
Three maximum.

**\
Evgeny Kharetski** 7:36\
That is my estrana.

**\
Alexander Biratko** 7:36\
That\'s why it\'s gone.

**\
Aaron Bockelie** 7:36\
So, three.\
The 3 to 10 repos you use as reference while you\'re working on one singular problem, is that correct?

**\
Val Levitan** 7:47\
Three maximum.

**\
Alexander Biratko** 7:47\
Yeah.

**\
Val Levitan** 7:49\
Biratko is working on 10. He is a superhuman.

**\
Alexander Biratko** 7:53\
Yes.

**\
Aaron Bockelie** 7:53\
K.\
So I think that.

**\
Alexander Biratko** 7:56\
Thank you, Val.

**\
Aaron Bockelie** 7:59\
What I think is happening then is that you\'re using all these repos as documentation.\
You\'re using them as patterns to fit and describe.\
Have you ever heard of the phrase data contract? Do you understand what that word means or phrase means?\
A data contract is that these two things will always communicate like this.\
They will speak in this language. They will speak in\...\
JSON streams or a binary coded pattern of particular messages on a bus, they will.\
exchange whatever they need to exchange, but they do it reliably and they only speak of these particular things. That\'s kind of like an example of a data contract. An API endpoint is a data contract, right? I will provide these things with these methods to interact with me.\
And I promise I\'ll always do that.\
So I\'m going to guess right now is that you have inter-messaging between your different modules that don\'t have known data contracts. That it\'s sort of a mystery and they kind of do whatever they need to do and when you try to separate them, everything breaks, is my guess. And that\'s why you have to have all these other repos in here to continue to build and weave.\
things together. Is that the trouble that\'s going on?

**\
Evgeny Kharetski** 9:31\
Dima.

**\
Val Levitan** 9:45\
Ты созвал?

**\
Evgeny Kharetski** 9:45\
Да контракта вот, но основная проблема в том, ну ещё одна проблема.

**\
Val Levitan** 9:50\
Вот имеет проблемы.

**\
Evgeny Kharetski** 9:53\
В том, что у нас, а?\
Есть проблема в том, что у нас одна большая структура plex, но много ну то есть она.

**\
Val Levitan** 10:02\
Он ещё волосача.

**\
Evgeny Kharetski** 10:05\
Но она микросервисной, и вот эти сервисы, то есть клод.

**\
Val Levitan** 10:08\
Патенту макро сервис.

**\
Evgeny Kharetski** 10:11\
Квот не знает о всех сервисах сразу, но хотелось бы, чтобы знал.

**\
Val Levitan** 10:17\
Клод озонового атолл микросервисы semba прошёл лайк клод виноват он.

**\
Evgeny Kharetski** 10:17\
Ш.

**\
Aaron Bockelie** 10:25\
Какая все организацию, очень прокламацию, сервис пика зелёнке, акция в майку сервис говорю.\
Майка сервисиз.

**\
Val Levitan** 10:35\
И юзэд хиосе тасс за Фейсбук, но открыла его слушаю.

**\
Aaron Bockelie** 10:40\
Окей, окей.\
that word specifically correctly.\
If you actually\...

**\
Val Levitan** 10:49\
Do you guys understand or do you want me to wedge myself into translating for you?\
Do you need an interpreter?\
So just say stop and I\'ll jump in.

**\
Aaron Bockelie** 11:05\
Okay.

**\
Val Levitan** 11:06\
Do you understand so far?\
Aaron is a slow micro service, not a continue.

**\
Aaron Bockelie** 11:17\
All right. So in my opinion, and I say my opinion because everybody has opinions on what a microservice is, is that a microservice contains its own data, its own interfaces, its own ability to work on its own. It does not need anything else to run.\
Therefore, it is a service.

**\
Val Levitan** 11:42\
Do you understand?

**\
Aaron Bockelie** 11:42\
It runs independently.

**\
Dzmitry Chudzinau** 11:46\
The.

**\
Val Levitan** 11:46\
Micro service, micro service is a reason when you go send for message with reasonable service.

**\
Dzmitry Chudzinau** 11:51\
Val.\
Talk, maybe.

**\
Val Levitan** 11:53\
Continue.

**\
Aaron Bockelie** 11:56\
OK.\
As soon as you have multiple services in a microservice, it\'s no longer a microservice. It is a\...\
Opposite of a microservice.\
And I think that\'s\...

**\
Val Levitan** 12:09\
Yes, it was, yes, yes, service, but no micro service, it wanted to stay with micro service.

**\
Aaron Bockelie** 12:17\
And so, what I think that you have is a set of interrelated.\
macro services or large services that are bundled together that have particular domains, payment and database and billing and things.

**\
Val Levitan** 12:35\
Are you, are you, are you, are you saying that?\
that our repos are not fragmented enough.

**\
Aaron Bockelie** 12:45\
I am saying not.

**\
Val Levitan** 12:45\
They should be more, they should be, they should be more fragmented.

**\
Aaron Bockelie** 12:49\
No, I am saying that your architecture, the repos have nothing to do with this, other than to hold the code. But the way you\'ve structured the architecture of the platform has interdependencies.\
And so that actually becomes.

**\
Val Levitan** 13:05\
Correctly or incorrectly?

**\
Aaron Bockelie** 13:09\
I am not going to tell you whether they\'re correct or incorrect because it was a decision that was made. There is no wrong way to write code in this sort of structure.\
You need to decide whether it\'s right or wrong for the way that you want to work.\
I would, right now, I\'m going to advise you that most coding agents prefer to work with monorepos where everything has a concern inside of it.\
But A monorepo could be a monorepo of a microservice. You see how those are two different things.\
Monorepo doesn\'t mean microservice.\
They\'re separate.\
So, what you need to start this, oh, go ahead.

**\
Val Levitan** 13:57\
Just, just one, just one, just one second. Hold on, pause.\
I can feel molecular movement.

**\
Aaron Bockelie** 14:11\
You\'re detecting it.

**\
Val Levitan** 14:13\
I\'m detecting molecular movement.\
Just pause for a second.\
No, molecular movement dissipated.

**\
Aaron Bockelie** 14:29\
Okay.\
Well, we\'ll keep going here for a minute. So A mono repo.\
Can you, can anybody tell me I want to have a volunteer? What does mono repo mean to you right now?\
Gonna go to some basics for just a minute.\
Say it in Russian, I\'m sure Val could facilitate the translation.

**\
Val Levitan** 15:00\
Family.\
All services of a product included in one repository. That\'s manual.

**\
Aaron Bockelie** 15:11\
Right.\
Okay, and what if your product is a microservice? Is that still a monorepo?

**\
Alexander Biratko** 15:25\
No.

**\
Evgeny Kharetski** 15:25\
The.

**\
Aaron Bockelie** 15:26\
Why?

**\
Irina Shishko** 15:32\
My link came on the repa.

**\
Alexander Biratko** 15:33\
This is just a simple repository.

**\
Aaron Bockelie** 15:39\
A monorepo of a microservice is a complete piece of software that can stand on its own.\
Just doesn\'t do a lot.\
Is that do you agree or disagree with that statement?

**\
Evgeny Kharetski** 16:02\
Like what?

**\
Val Levitan** 16:04\
Agreed.

**\
Aaron Bockelie** 16:05\
Okay.

**\
Andrei Bosik** 16:05\
And we need to remember about then we have.\
some repositories which use it in different products.

**\
Aaron Bockelie** 16:19\
So what you have then is the same repository used in different combinations. Is that right, Andrei?

**\
Andrei Bosik** 16:26\
Yeah.

**\
Aaron Bockelie** 16:27\
Okay, so I\'m trying to not give you an answer because there\'s no answer to be solved here. It is about understanding what you\'ve got.

**\
Val Levitan** 16:33\
And, and I\'m that.\
And I\'m trying to walk away with a course of auction in about 7 minutes. I have 7 minutes. I need to walk away with course of auction.

**\
Aaron Bockelie** 16:39\
We will, we are going to get there in just a minute.\
At work.\
I already have the answer. I\'m going to tell it what I\'m thinking here. I\'m just trying to lead you to the thinking of it. Otherwise, I\'ll just tell you and then you won\'t really connect.\
So, what\'s happening here, I think?

**\
Val Levitan** 16:58\
Sergey, Sergey is, Sergey is scratching his head. That means molecular movement is going.

**\
Aaron Bockelie** 17:05\
All right.\
So\...\
So what I think is happening here is that each of you have different types of concerns and most of them revolve around I need to grab all of the code and have the entire ecosystem running in a test environment or a dev environment to get any work done at all.\
And that\'s because of a bunch of architecture decisions that were made quite a while ago.\
And what you can do is you can establish a new pattern of what\'s called a poly repo. Do you know what a poly repo is?\
If mono is 1, what is poly?

**\
Val Levitan** 17:44\
Yes, a repo that was born in Poland.

**\
Aaron Bockelie** 17:47\
That\'s pola repo, that\'s not poly repo. That\'s very different.\
They\'d have to, they probably drive trucks really fast on the road too, don\'t they?\
Anyway, a poly repo, which is many, mono is 1, right? So what you\'re going to be doing is you\'re going to build what\'s called a\...\
Meta Meta Poly Repo.\
Meta Poly Repo.\
It is a repo, a repository, that is essentially A repository of submodules.

**\
Irina Shishko** 18:22\
Yeah.

**\
Aaron Bockelie** 18:30\
It is the ecosystem repository.\
You know how we would do that?

**\
Evgeny Kharetski** 18:46\
No, we should be stunned. Well, Roger, squad up Chelsea number.\
Ah.\
Oh.\
Aaron\'s special name is that meta meta poly rippo.

**\
Irina Shishko** 19:04\
The.\
Huh.

**\
Evgeny Kharetski** 19:23\
Strategy for summer.

**\
Irina Shishko** 19:26\
Perfect.

**\
Evgeny Kharetski** 19:26\
So, I can go to Aaron.

**\
Val Levitan** 19:30\
So.\
Translating what Jerez is saying.

**\
Aaron Bockelie** 19:36\
Mm.

**\
Val Levitan** 19:37\
It says, basically, it\'s what I wrote in my\...\
Memo in this chart, this is Meta Poly Repo.

**\
Aaron Bockelie** 19:47\
Now are they actually, so the thing is, is that I expect it to be a Git repo with submodules. Submodules are a very specific Git thing.

**\
Val Levitan** 19:59\
You, you\'re, you\'re confusing everybody. Do you want meta repo or do you want submodule repo?

**\
Aaron Bockelie** 19:59\
This is explicit.\
Meta poly repo is just the term I just invented, which is called a Git repo that has submodules in it. Submodule is an actual Git term.

**\
Val Levitan** 20:19\
So you want configuration with submodules?

**\
Aaron Bockelie** 20:23\
You need a Git repo that actually has nothing in it other than submodules and the attended harness pieces to be able to build the product.

**\
Val Levitan** 20:35\
OK, say it again now.

**\
Aaron Bockelie** 20:36\
That\'s A meta-repo. A meta-repo actually has no functional code in it.

**\
Val Levitan** 20:38\
Okay, see.

**\
Aaron Bockelie** 20:43\
The meta repo does not have functional code for the platform. It only has the sub-module definitions for Git inside of it, and probably integration tools to execute and run the whole platform.\
So it is a meta repo. Without the actual submodules, it does nothing at all.\
And it is managed as a Git repo.

**\
Alexander Biratko** 21:13\
But in this case, we can have information about how repository connect one other.

**\
Aaron Bockelie** 21:25\
Yeah, absolutely. You could put your context in the meta repo.\
Because without the actual submodules, it doesn\'t do anything, right? It\'s just descriptions.\
But I want to caution you with this, and this is why I just spent the last 10, 15 minutes explaining the difference between monorepo and not, that you can use this opportunity to establish stronger data contracts between your other submodules, to begin to turn them into truly independent tools that don\'t require everything to be.\
Pushed together into a giant disk on the computer.\
You have to actually actively push it that direction.

**\
Val Levitan** 22:05\
There\'s not.\
There is no molecular movement. Hold on a second.

**\
Aaron Bockelie** 22:09\
Right, sure.

**\
Val Levitan** 22:12\
One moment.

**\
Aaron Bockelie** 22:15\
Val is going to\...

**\
Alexander Biratko** 22:17\
One Aaron speak fast, Maleka will not move it.

**\
Aaron Bockelie** 22:22\
Ha ha ha.

**\
Val Levitan** 22:22\
You have to you have to repeat yourself again on this. Loud, but you got you got to pronounce words correctly. Don\'t chew it up in Kansas way.

**\
Irina Shishko** 22:23\
Yeah.

**\
Aaron Bockelie** 22:25\
All right.\
So\...

**\
Val Levitan** 22:35\
And, slowly.\
make stops and make sure that molecular movement is transferring from point A to point B.

**\
Aaron Bockelie** 22:47\
Okay, I\'ll make sure the Brownian motion is high.

**\
Val Levitan** 22:51\
Okay.

**\
Aaron Bockelie** 22:53\
So\...\
I told you earlier about the difference between monorepo and how it\'s not related to a microservice, yeah? I want you to be thinking about that.\
Because what I\'m going to tell you is that a meta, a meta poly repo, meta meaning it does not actually contain the thing, just the structure.\
Poly, meaning it contains multiple submodules. Submodules is just a Git repo.\
There\'s no difference, okay?\
You add submodules to this meta repo.\
And when you clone the meta repo recursively, you get all of the repos coming down managed in a tree structure, just like what Evgeny is talking about.\
And what Sasha is saying is that in this meta repo, you can contain steering information or context about all the structure of the meta repo.\
describing what they do.\
And finally, this is not the final state of what you\'re going to work in. It is a crutch. It is a\...\
It is an in-between space because it is a huge anti-pattern to try to build a big poly repo if you\'re experiencing the problems you\'re experiencing right now.\
Instead, take the time and take the architectural effort.\
to begin to break down this.\
monorepo problem that you have.\
presented as polyrepos to actually create more of a microservice style approach to all of your repositories.

**\
Val Levitan** 24:53\
So, I was right.

**\
Aaron Bockelie** 24:53\
You do this, you do this through better definition of the data contracts between the monorepos that you\'ve got, and then at some point\...\
your monorepos start to look like microservices instead.\
Microservice means one with very small concern.\
This means you will eventually break these monorepos up into smaller concerns.\
Do not break things into microservices if it doesn\'t make sense to do that.\
You should always be thinking about the data structure and the pools of data that you\'re managing, not the execution concerns of the software.\
If you have\...\
Five different concerns that require the same data set to work in.\
That\'s A monorepo with all of those things in that data set.\
If you try to break out the data set separate from the computation, that\'s not microservices, that\'s just a mess.\
A microservice in my definition is one that can stand on its own without needing other tools to run or pieces to run.\
And I think that you probably are\...\
relatively well optimized to that right now. And that\'s why I\'m saying it\'s not wrong.\
It is not wrong that you have your repos structured the way they are right now.\
But I think you\'re encountering challenges because they do have some more subdivision that can be done to them.

**\
Val Levitan** 26:36\
So I was right.

**\
Aaron Bockelie** 26:38\
Sounds like it.

**\
Val Levitan** 26:39\
We are not.\
Yet.\
Our repos are not yet at the size or the level of disintegration as we would ideally want them to be.

**\
Aaron Bockelie** 26:53\
Correct. And when you then have the poly repo poly meta repo.\
This allows you to choose the concerns you want to clone to work on, because not everybody on this call is going to work on the same thing.

**\
Irina Shishko** 27:20\
But.

**\
Val Levitan** stopped transcription
