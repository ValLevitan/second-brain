**Continues_Intergation_architecture_payment_platform-April-17-2026-20260417_081019-Meeting Recording**

17 April 2026, 12:10pm

2h 19m 2s

**\
Val Levitan** started transcription

**\
Val Levitan** 0:03\
Meeting without me to the best of your ability. I have to. I don\'t know what to do.\
Just go, go ahead with your meeting. I cannot hear.

**\
Andrei Bosik** 0:12\
No, I have a problem.\
Yes, this mobile can use now.\
No, okay, the right thing, the attack.\
Mhm.\
OK, I share my screen. As you can see, I create as we speak about meta repository. This is a repository which contain information about all another repositories which included to this.\
Um\...\
big product. In this example, this is a\...

**\
Evgeny Kharetski** 1:00\
My, my, my employee, Andrei.

**\
Alexander Biratko** 1:00\
And.

**\
Andrei Bosik** 1:04\
One second.

**\
Alexander Biratko** 1:06\
Yeah.

**\
Evgeny Kharetski** 1:09\
Is it better?

**\
Andrei Bosik** 1:11\
No.

**\
Evgeny Kharetski** 1:12\
Or, no.

**\
Alexander Biratko** 1:12\
Yeah.

**\
Andrei Bosik** 1:13\
Yeah, okay. And the\...\
This repository contained information about all parts which included to this big product.\
You can see we have here, contracts, deploy, and documentation test. It start, maybe we change some information which contains this meta repository at some information in future.

**\
Evgeny Kharetski** 1:33\
IN.

**\
Alexander Biratko** 1:37\
Oh.

**\
Andrei Bosik** 1:49\
This is beta version.\
Uh\...\
Jima Chudzinau add information to.\
Services repository, as I say, which is part of this big repository and add information to this repository. We use to do this information, our conversation on past meetings.

**\
Alexander Biratko** 2:10\
She.

**\
Andrei Bosik** 2:19\
And Sasha create the command using this information too, and Sasha can say about this document.

**\
Alexander Biratko** 2:33\
Okay.\
Let\'s meet.

**\
Andrei Bosik** 2:38\
I think more better if you share your screen, and\...

**\
Alexander Biratko** 2:39\
Sood.\
I.

**\
Andrei Bosik** 2:42\
Show this document.

**\
Alexander Biratko** 2:51\
The.

**\
Aaron Bockelie** 2:57\
Can you?\
Do you, did you link all of the?\
sub-modules into that as well, or is it just docs about things?

**\
Andrei Bosik** 3:07\
Um\...\
This documentation created Dmitriy Chudzinau, and I\'m not sure, but I think he does not create this.\
As some models and create just the links in documentation to another repositories.

**\
Alexander Biratko** 3:20\
Yep.

**\
Andrei Bosik** 3:30\
Because when we work with some models, they have some.\
Problems.

**\
Aaron Bockelie** 3:38\
What are those problems?

**\
Andrei Bosik** 3:41\
I need to remember, I think we need to say about this. Maybe Sasha can add more information about this, why we not use some models.

**\
Alexander Biratko** 3:52\
Uh\...\
The.

**\
Andrei Bosik** 4:01\
Sasha, you enable your translator.

**\
Aaron Bockelie** 4:03\
Yes, it takes a second.

**\
Alexander Biratko** 4:05\
It.\
Okay.\
Yeah, Peari was\...\
Ya, adal clodo. Nash conversation pre deduce. Ye opera sil pro analyser, es kaki nas mogudas probleme. Ad news problem cloto causal submodule.

**\
Val Levitan** 4:27\
Harry Peari mode, waiting for connection.

**\
Alexander Biratko** 4:33\
Um\...

**\
Andrei Bosik** 4:43\
Uh, do you need to translate down?

**\
Aaron Bockelie** 4:48\
It says\...\
Ask analyzer problems might await us, and one of the problems pointed out was submodules.\
So, what is what is the problem though?

**\
Andrei Bosik** 4:57\
Yeah.\
Sasha now show these problems.

**\
Aaron Bockelie** 5:02\
OK.

**\
Alexander Biratko** 5:06\
Just.

**\
Val Levitan** 5:13\
Yeah.

**\
Alexander Biratko** 5:30\
Mm.\
In the shot.

**\
Val Levitan** 6:11\
Yeah.

**\
Evgeny Kharetski** 6:24\
I\'ll try transcript.

**\
Alexander Biratko** 6:26\
In Perelman.\
Sorry, sorry.

**\
Aaron Bockelie** 6:30\
Huh, that\'s okay.

**\
Alexander Biratko** 6:32\
But, but translation.

**\
Aaron Bockelie** 6:34\
Yeah.

**\
Evgeny Kharetski** 6:35\
Yeah.

**\
Aaron Bockelie** 6:40\
It\'s like Russian, but not Russian. It\'s very weird.

**\
Alexander Biratko** 6:42\
Yeah, yeah.\
It is Google Translator.\
It.

**\
Aaron Bockelie** 6:58\
OK, so.\
Let\'s talk about this for a minute. When does a developer need to clone the entire tree of everything?

**\
Alexander Biratko** 7:16\
One time.

**\
Aaron Bockelie** 7:18\
Well\...

**\
Alexander Biratko** 7:20\
Yeah.

**\
Aaron Bockelie** 7:20\
Let\'s talk more about the scenario of it, right? So\...\
Developers working on\...\
on some problem, whatever that might be.\
How often do they actually need to clone everything, including all submodules, to make it work?\
to investigate the problem, do you think?

**\
Alexander Biratko** 7:47\
I think we can do it one time.\
and check out all repositories to own computers.

**\
Aaron Bockelie** 7:55\
What?\
O.\
Well\...\
I think maybe I\'m not getting to the question properly. Let me ask it a different way.\
If I have a very rich\...\
Large software platform, and I am working on exactly one piece of it.\
Um\...\
It would be very fragile for me to clone that and all of the submodules and then attempt to do work on it.\
OK.

**\
Alexander Biratko** 8:36\
Yeah.

**\
Aaron Bockelie** 8:36\
But\...\
I don\'t need to work on all the pieces of it. I work on the piece I need to work on. Whatever.\
whatever sub-repo that is.\
And I don\'t, and I shouldn\'t, be trying to completely replicate the entire build stack locally all the time. I should be depending on the build engine, the build system, to verify things for me.

**\
Alexander Biratko** 9:03\
John.

**\
Aaron Bockelie** 9:04\
Because if I\...\
Make a change to a sub to a repo that is a sub-module of the larger system.

**\
Alexander Biratko** 9:09\
Yeah.\
So.

**\
Aaron Bockelie** 9:14\
Most of the time, I should not be making any changes that materially affect.

**\
Alexander Biratko** 9:16\
Scism.

**\
Aaron Bockelie** 9:20\
the contracts between that submodule and what it does and the rest of the system.

**\
Alexander Biratko** 9:21\
Yeah.\
Seated.\
Six.

**\
Aaron Bockelie** 9:29\
There\'s an \*\*\*, we have to make an assumption.

**\
Val Levitan** 9:32\
Yeah.

**\
Aaron Bockelie** 9:33\
So the assumption is, is that\...\
Whatever I\'m working on.\
should be able to be verifiable and testable on its own without needing to clone it and the entire master meta repo and everything else all the time for all developers.

**\
Alexander Biratko** 9:48\
Pizza.\
Sorry.\
What?\
The.\
Awesome.

**\
Aaron Bockelie** 10:04\
The continuous integration space that is highly controlled and scripted, rather than\...

**\
Alexander Biratko** 10:05\
Excellent.

**\
Aaron Bockelie** 10:12\
you know, ad hoc on everybody\'s developer.

**\
Alexander Biratko** 10:14\
If.

**\
Aaron Bockelie** 10:15\
Environment.\
If it\'s not that way right now, if you have to clone everything, including submodules, to get any work done, this is more of an architecture problem of interdependency than it is anything else.

**\
Alexander Biratko** 10:23\
Oh.\
Love.

**\
Aaron Bockelie** 10:34\
And if you don\'t have a make system or some sort of local build system that you can run on everybody\'s machine to be able to programmatically clone everything and build and test everything anyway, that\'s also a shortcoming that needs to be addressed as well.

**\
Alexander Biratko** 10:38\
presentations.

**\
Aaron Bockelie** 10:54\
So, Baud might be saying get submodules is a risky choice, but I believe that it\'s also a risky choice because of the ways of what it sees right now and the way your repos are configured.

**\
Alexander Biratko** 11:10\
The.

**\
Aaron Bockelie** 11:11\
I think a risky choice, that word.\
is extremely subjective and it is an opinion based on information that already exists right now.

**\
Alexander Biratko** 11:16\
Yes.

**\
Aaron Bockelie** 11:21\
So I\'m not going to call that a hallucination because it\'s not.

**\
Alexander Biratko** 11:21\
I.\
Shakti\'s \*\*\*\*, Padmi.

**\
Aaron Bockelie** 11:25\
But what it is, is it\'s probably based on what it\'s actually looking at your code base says.

**\
Alexander Biratko** 11:33\
We also have problems with some models now, is our work where we use some models. It\'s really problems.

**\
Aaron Bockelie** 11:46\
What are the problems though? Like what is happening?

**\
Alexander Biratko** 11:51\
Grandpa will detach her.\
I worked.\
And try to push and to see.\
To have.\
That I should have, I don\'t know why.

**\
Aaron Bockelie** 12:04\
What?\
Why would you be in detached head, though?\
You should fix the head detachment problem with Git first before attempting to use it.

**\
Alexander Biratko** 12:15\
I think it maybe, maybe.\
It\'s no.

**\
Aaron Bockelie** 12:27\
I mean.\
So\...

**\
Alexander Biratko** 12:36\
No.\
Ohh, Kaka Kaka Raiznitsa isjvlsystemsatlassiannet Silko Eli at the Budit submodule.

**\
Andrei Bosik** 12:51\
No, which difference between we use of models or links to repositories, which benefits we do have if we use some models?

**\
Aaron Bockelie** 13:03\
So I would say that the benefit of a submodule is that you can clone the main repo and get the submodules and track it. I am not saying that you have to do that.\
There is no right answer to any of this.\
is what works based on the shape of the code base that you\'ve got.\
Ideally, you shouldn\'t have to clone any of these submodules. They should be all published as libraries to your internal artifact repository, and you just use the libraries.\
That doesn\'t, that shouldn\'t need the submodules at all.

**\
Andrei Bosik** 13:35\
And.\
It\'s not libraries, it\'s a microservices.

**\
Alexander Biratko** 13:44\
Play.

**\
Aaron Bockelie** 13:45\
Right, so\...\
Why wouldn\'t you just have a Docker Compose that runs all of these services?\
If you\'re trying to run it against that, I, I, the problem here\'s.

**\
Andrei Bosik** 13:56\
Mm.

**\
Aaron Bockelie** 13:57\
I think there\'s some issues right now. One, on the previous meeting, we were talking about it as if it was a monorepo and we were going to break it up. Two.

**\
Alexander Biratko** 14:00\
Yeah.

**\
Andrei Bosik** 14:05\
We found that this is a mistake. We do not have mother repo.

**\
Aaron Bockelie** 14:07\
Yes, right. Two, you do have a bunch of independent repos that ideally should run all on their own anyway, and they all are built into, I\'m assuming, Docker images are ready to go to be able to be pulled down. You don\'t have to build images every time.

**\
Alexander Biratko** 14:24\
S.

**\
Aaron Bockelie** 14:26\
Three.\
If you have images and they have\...\
a trustworthy or consistent approach to how they work.\
You really need to grab all the code for everything and build the whole universe every time you want to do something on your computer. I wouldn\'t want to do that. It takes too long.\
So, the, the\...

**\
Andrei Bosik** 14:50\
Mm.

**\
Aaron Bockelie** 14:54\
Submodule and meta repo thing is probably principally for a DevOps angle where you\'re trying to do the full continuous integration path, which is what I was saying in the last meeting.\
But I\'m imagining the\...\
more specific developer experience of working on any particular module is just clone that repo and work on it. There\'s no, there\'s only one place that has potentially sub-modules and that\'s the integration repo.

**\
Andrei Bosik** 15:28\
But you know, we have part of this repository which will be deployed to cloud and this is a\...\
back end with front end system and we have part repositories which and finally have product for land base equipment. For example, in this product, this is a\...\
Payment terminal.\
You cannot download all as some models because you cannot run, for example, for payment terminal on your computer.\
You can run only.\
Docker images - that\'s all I think.

**\
Aaron Bockelie** 16:35\
So, I mean, I don\'t see anything wrong with being able to run Docker images only for this machine, these pieces of software. What\'s wrong with that?

**\
Andrei Bosik** 16:44\
No, it\'s not wrong. I just say that when you add all repositories as submodulers, you download.\
You don\'t load code for payment terminal.\
We should not need it for you, for example.

**\
Aaron Bockelie** 17:07\
Right, and so are you thinking that you\'re telling all your developers to grab the continuous integration repo and clone that recursively for any work?

**\
Andrei Bosik** 17:17\
Ohh.

**\
Alexander Biratko** 17:20\
No, no.

**\
Aaron Bockelie** 17:23\
So if they\'re not grabbing the continuous integration repo, the meta repo, there shouldn\'t be anybody grabbing repos that are actually submodules.

**\
Andrei Bosik** 17:35\
Not clear for me, not understand.

**\
Aaron Bockelie** 17:40\
Um\...\
Let\'s see.\
I will use.\
I will use chat to log chat to draw a picture. Give me a minute.

**\
Andrei Bosik** 18:25\
But.\
I think this is not the main thing. We at any time can switch from links to some models.

**\
Val Levitan** 20:08\
Happy birthday to you!

**\
Aaron Bockelie** 20:11\
I\...

**\
Alexander Biratko** 20:15\
Yes.

**\
Aaron Bockelie** 20:39\
So I\'m just trying to have claw instead of diagram. It\'s funny, we used to draw diagrams in whiteboards. Now we don\'t even have to do that anymore. We just make the pictures and stuff.\
The point I\'m trying to illustrate is that\...\
I want to understand and discuss.\
How you see?\
submodules versus links versus working on something and where the other submodules actually produce.\
containers and how you would then use a registry of containers and use essentially Docker Compose to build and host the local environment to run inside of to do your work.\
Let\'s see how it diagrams this. This is not as good as I was hoping it would be.\
Well, this is actually okay.\
O, if you have a\...\
continuous integration deploy environment. That\'s what Claude is drawing as what we\'re calling the meta repo, right?\
and we\'re submoduling each of these things.\
These produce Docker images that go off to CI for building things.\
In the local developer workflow, we might just clone Auth API, and the Docker Compose has to pull all the other containers in there and lets you work.\
Is this what you\'re thinking of doing right now?\
Because this is how I would work if I had multiple concerns.\
Let me.

**\
Evgeny Kharetski** 22:44\
But in this, but but in this, when you clone it, there is no data contract, it\'s on the on meta repo.

**\
Aaron Bockelie** 22:44\
Let me give you, ohh, go ahead.\
No, of course there\'s a data contract. The contract is built right into all of the repos. If it\'s not, it needs to be. Every single one of these has to attest that they can do something, right?\
The Auth API is going to have a surface that says, I do this, right?\
The web front end says, I consume that. The data pipeline says, I move this to that.\
That\'s all defined inside of each of the repos.

**\
Evgeny Kharetski** 23:26\
But we said that the meta repo contains all data contracts.

**\
Aaron Bockelie** 23:33\
The meta repo is going to be able to verify all those contracts.\
But\...\
At some point, why would you divorce the tests from the product itself?\
If you had a bunch of integration tests and a bunch of mocks for making sure it does what it does.\
Does it make sense to make those separate? I\'m wondering if this is a translation problem, like literally English to Russian or Russian to English or something like that right now. Because I would not want to have you have separate verification tests and data contracts.\
Test against.\
you know, the outside, not packaged with the repo.\
Not to mention, not to mention.\
You could say that this service is, let\'s look at right here, services auth API, right?

**\
Evgeny Kharetski** 24:34\
Yeah.

**\
Aaron Bockelie** 24:34\
This could actually have a submodule of the CA.\
So you could actually submodule each of these back to the CI and grab your integration test to verify data contract correctness.\
There\'s just a bunch of ways to decide how you want to do it. It depends on the shape of what your product is doing.\
So, if I ran make data contract tests right here inside of the Auth API, I could literally watch the make tool go and make sure that we have the clone submodule for not only just the branch, but the particular.

**\
Evgeny Kharetski** 25:08\
Okay.\
Go, go.\
I think that means things like variable.

**\
Aaron Bockelie** 25:19\
directory structure for continuing integration tests to be able to run them. You just have to be clever in how you actually put them together so they\'re reusable.

**\
Evgeny Kharetski** 25:22\
You, you know.\
Yeah.

**\
Aaron Bockelie** 25:28\
Are you going to build reusable data contract tests for all of your different modules? I would.\
Why would you want to rewrite those over and over and over again?

**\
Evgeny Kharetski** 25:38\
You should probably be in court.

**\
Aaron Bockelie** 25:40\
Having one copy of the contract is very important. Most of that works well outside of software engineering too.

**\
Evgeny Kharetski** 25:57\
Hi, yes, that was come.\
In my.

**\
Alexander Biratko** 26:22\
Yet, uh, Aaron post to data contract, some product, some service on data contract.

**\
Evgeny Kharetski** 26:32\
Yeah.\
No, I can no cocktail.\
Opposite good was not sure.

**\
Alexander Biratko** 26:40\
Just.\
No, no.\
Aaron, you translate it now?

**\
Aaron Bockelie** 26:54\
My translator just\...\
sort of.

**\
Alexander Biratko** 26:57\
Okay, I I will I will try to English in your case, meta repo has links to.

**\
Aaron Bockelie** 26:58\
Stop!

**\
Alexander Biratko** 27:09\
Uh, service reports, alright.

**\
Evgeny Kharetski** 27:09\
The.

**\
Aaron Bockelie** 27:13\
OK.

**\
Alexander Biratko** 27:14\
Ah.\
If we work in service repo, we need link to meta repo. It will be also a submodule cross.

**\
Evgeny Kharetski** 27:16\
What we need to better?\
Outlook.\
Cross.

**\
Alexander Biratko** 27:27\
Lincoln?

**\
Evgeny Kharetski** 27:27\
CA.

**\
Aaron Bockelie** 27:28\
Yeah, depending on how you are.\
Let me write it out how I see it.

**\
Alexander Biratko** 29:13\
Hello?\
Yeah.\
Yes, we will have.

**\
Evgeny Kharetski** 29:55\
Yes, we will.

**\
Alexander Biratko** 29:59\
Uh, unit tests for checking.

**\
Evgeny Kharetski** 29:59\
In your.

**\
Alexander Biratko** 30:03\
Contract data contract inside service repos.\
But, uh\...\
Yeah.\
The data contract will.

**\
Evgeny Kharetski** 30:12\
Come from you.

**\
Alexander Biratko** 30:16\
Inside.

**\
Evgeny Kharetski** 30:17\
Sood.

**\
Alexander Biratko** 30:19\
Integration repo.\
Yeah.\
Yeah.

**\
Aaron Bockelie** 31:02\
But do you see what I mean by?\
contract can be one-sided, it just promises that it delivers these things, but a codependency where both have to work together is not ideal.

**\
Andrei Bosik** 31:47\
Do you mean that?\
That the contracts.\
Show only that what this application?\
Will do.\
For example, I sent you data in this format in this in this.

**\
Aaron Bockelie** 32:05\
Um\...\
Yeah.

**\
Andrei Bosik** 32:14\
Post get query or something else.\
And, ohh, is this is this all, yeah?

**\
Aaron Bockelie** 32:23\
Let me write this out.

**\
Alexander Biratko** 33:05\
Yeah.\
Yeah.\
Yeah.\
Yeah.\
Yeah.

**\
Val Levitan** 36:31\
Yeah.

**\
Aaron Bockelie** 37:19\
I find it easier just to type and then you guys to read and translate that way.\
We\'ve gone full circle. We now create the, we create the transcript before we say anything.\
Sorry, we\'re doing it this way, but this is kind of\...\
I\'m trying to point out that it\'s more complex than just a one-way graph of how things go together.

**\
Alexander Biratko** 37:54\
If you work with external systems, it\'s right.

**\
Evgeny Kharetski** 37:54\
Work this external system.

**\
Alexander Biratko** 37:59\
We should get our data contract and write our code for work with this contract. Inside our systems, we\...

**\
Evgeny Kharetski** 38:03\
One for.\
Okay.\
More.\
By our systems.\
VA.

**\
Alexander Biratko** 38:14\
Can do some more; we can say, \"Please get me more information about this item, and\...\"

**\
Evgeny Kharetski** 38:14\
Danzo song.

**\
Alexander Biratko** 38:26\
This contract should be.

**\
Val Levitan** 38:30\
I\'m back.

**\
Andrei Bosik** 38:35\
Can you hear us?

**\
Alexander Biratko** 38:36\
Uh\...

**\
Val Levitan** 38:37\
Yeah, I can see him here.

**\
Andrei Bosik** 38:40\
Cool.

**\
Aaron Bockelie** 38:43\
So\...

**\
Alexander Biratko** 38:43\
And I, I think we need one place.\
Of store the data contracts.

**\
Aaron Bockelie** 38:54\
Have you?\
Have you ever heard of the Zero Trust Model?\
You have an, if you, it\'s pretty common.\
Google kind of pioneered it a long time ago, and then it sort of made a lot of sense for how to build software.\
Google wasn\'t the only one, but they made it popular.\
The.

**\
Val Levitan** 39:34\
Zero Trust Model.\
Yeah.

**\
Alexander Biratko** 39:42\
Yes.\
No.

**\
Andrei Bosik** 39:47\
Yes, nice to talk with.

**\
Evgeny Kharetski** 39:56\
Yeah, presto.

**\
Alexander Biratko** 39:56\
Sticks.

**\
Val Levitan** 40:07\
interactivity first.

**\
Evgeny Kharetski** 40:17\
It\'s my, yeah, it\'s a no, the other thing my email is listening.

**\
Alexander Biratko** 40:17\
No, no.

**\
Val Levitan** 40:22\
He made it, he made it, he made it, but for sure.

**\
Alexander Biratko** 40:24\
Mute.

**\
Evgeny Kharetski** 40:24\
Yeah.

**\
Alexander Biratko** 40:25\
But almost Aaron Prostaduction.

**\
Val Levitan** 40:31\
Zero Trust.

**\
Andrei Bosik** 40:37\
Okay.

**\
Val Levitan** 40:38\
I used it with not in our minor communication at the process.\
I thought, what\'s what specifically?

**\
Alexander Biratko** 40:53\
Yeah.

**\
Val Levitan** 40:56\
Yeah.

**\
Alexander Biratko** 40:57\
More with me the money, many specific culture.

**\
Evgeny Kharetski** 40:58\
Looking at the.\
Which could have?

**\
Andrei Bosik** 41:09\
Val.

**\
Alexander Biratko** 41:12\
Oh, no, no, no.\
Ohh no.

**\
Aaron Bockelie** 41:20\
А вот я считаю.

**\
Evgeny Kharetski** 41:21\
Да.

**\
Andrei Bosik** 41:29\
А в утра и они то рано репенту окон здесь моя шейк из нотворк.\
Bote tray what secand?

**\
Aaron Bockelie** 41:36\
Алло окей.\
5.

**\
Evgeny Kharetski** 42:09\
Лес.

**\
Alexander Biratko** 42:13\
Яс.

**\
Aaron Bockelie** 42:19\
По игру этот пара.

**\
Andrei Bosik** 42:29\
Сейчас он бадом.

**\
Aaron Bockelie** 42:29\
Это wip pod not tase store storter он comersation.\
Мелот этапов декс.

**\
Alexander Biratko** 42:40\
Цель посреди страницы внизу.

**\
Andrei Bosik** 42:42\
А свинья окей.

**\
Aaron Bockelie** 42:42\
Парам.

**\
Andrei Bosik** 42:44\
Окей.

**\
Aaron Bockelie** 42:47\
Всё ещё low dankat comer tation rome mot chure.

**\
Val Levitan** 42:52\
Приказ я знал bye banner yan and den and andendesdosorkelbal b pn.

**\
Aaron Bockelie** 42:54\
А.\
Я.

**\
Evgeny Kharetski** 43:06\
Если сайт открылся, значит только он работает.\
На сайт не открывается без рупена.

**\
Aaron Bockelie** 43:30\
Процент maik ai.\
Но.\
Это молчать.\
Да.\
Всё.\
Он carver sation in wo happens.\
WWW.\
Hatsa.\
Oper innate destap red oper.

**\
Val Levitan** 45:33\
Браузер.

**\
Aaron Bockelie** 45:34\
Окей.\
На workenger.

**\
Andrei Bosik** 45:37\
Инбраусер.

**\
Aaron Bockelie** 45:41\
In seregint trade dest sustube it\'s too.

**\
Val Levitan** 45:44\
Яз.

**\
Aaron Bockelie** 45:46\
Они делал плача инсайрча insirede pro insired ecation.\
Или Андрей и трада окей.

**\
Val Levitan** 45:56\
6.

**\
Andrei Bosik** 45:59\
А.\
I open elenk in brouser moting cate inten clades.

**\
Aaron Bockelie** 46:04\
Брай.\
What world?

**\
Andrei Bosik** 46:10\
А окей.\
Whatsacon.

**\
Aaron Bockelie** 46:13\
Warche irina wity sess is, noting cher bock the is is not staft there is.\
Окей.

**\
Andrei Bosik** 46:26\
Энд здесь из десктопабликэйшн.

**\
Aaron Bockelie** 46:29\
Доставка Apple castion.

**\
Andrei Bosik** 46:37\
Да.\
Мэбиэ consention истопли cant heopen.

**\
Aaron Bockelie** 46:51\
О это wark tow toway.\
Кентинию.\
Oldery borem.

**\
Val Levitan** 47:09\
Но, но точно сочны.\
Даёмный общины гевзию старки роуд хансэйшн.

**\
Aaron Bockelie** 47:18\
Это целый andresty be brokercate без новые works.\
Мы говорим.\
Ну.\
В.\
File and the ns.\
Интересно.\
Стал нючать.

**\
Andrei Bosik** 49:53\
А iask QQ.\
Donate sap не файл окей чат indestop innater.

**\
Aaron Bockelie** 49:57\
Эти.\
Это.

**\
Andrei Bosik** 50:01\
Окей доступ мол.\
Автобус.\
Can take ze txils.

**\
Aaron Bockelie** 50:09\
Натяните.

**\
Andrei Bosik** 50:12\
А whatsacanda.\
Ага спасибо won sace cast.\
Окей.\
Аски himabater zored pross motel.

**\
Aaron Bockelie** 50:32\
Н.\
Но те, кто правда правильно colds.\
Здесь я бы разных запал, обзывают rust архитектуру.

**\
Evgeny Kharetski** 50:51\
Андрюш там в этом в чате над предыдущее Сообщение.

**\
Andrei Bosik** 50:54\
А инчес все я достанет.

**\
Evgeny Kharetski** 50:56\
10 гот ситто discos.

**\
Aaron Bockelie** 50:57\
Только парады.\
Ирэн ирэн c luring morden a pro g gord gord no nowed senter.\
И майк интернет.\
Став.

**\
Val Levitan** 53:10\
Вот stard mart.\
Боровы.

**\
Aaron Bockelie** 53:17\
Эвиринг.

**\
Andrei Bosik** 53:18\
Вы Америка балт.\
Эрон модо.

**\
Aaron Bockelie** 54:33\
Перелинглы dolan exted afrent profter susiner.

**\
Andrei Bosik** 54:50\
Я он с этого.\
Ну ей просто.\
А.

**\
Aaron Bockelie** 55:29\
Зацеп этот палова прилиной.\
От них.\
Ещё бы и.

**\
Andrei Bosik** 55:53\
Здесь документ викенсизет дата контракт контейн и chuckation herвис.\
Not metropsetore.\
А.\
Энд дата контракт нет.

**\
Aaron Bockelie** 56:09\
Амери.\
Позитории из уанwай экспорта contracks.

**\
Andrei Bosik** 56:17\
Окей.

**\
Aaron Bockelie** 56:27\
Pay forom two shisterms is t ru a sama jow i production да is accory we we i do.\
В самом стайл рипору.\
Свидания, полдарком lancianer ther.\
Fcores every tanket anibaly with and sliby comther proderction sordy cine pay prock peariss areginal.\
Ingenering firem prossen dat.\
Конечно, Терека антракс.\
Еще пифайдинг истории зинса рта чая еще риск i hared.\
Fi fi.\
И казни любимый.\
Ау.\
Wer can cantract sement spreed.

**\
Andrei Bosik** 58:06\
Поверьте мне.

**\
Aaron Bockelie** 58:07\
Emines the ting the never change inverient.\
Line w red perfery.\
Рай ремейнс латте finks red.\
Etmetmentsity, cantilea ts ната.\
So in weer and mets now redde now thanges.

**\
Val Levitan** 58:33\
Постоянная.

**\
Aaron Bockelie** 58:50\
Candasin tan sare per contrack lancashire cont contracks is isment fre for fory postirist.\
Cantracks wonder hove.\
Вот через what mast we trubber for reck and start and pross candas and whes wores garin te atter werts and inverine ins insive cantracks the instreet is.\
Пересекли формэйшн suftware in tower aver.\
Conterpet serger truss tant foup и вэд.\
Атцистем.\
Да.\
Well, clay and and the test.\
Дарит да wer clame stedu.\
Платформ состоит здесь what comple carity dange?\
Здесь ватчик контракт, и вот эти.\
Пацией пациэкс саша.\
Саша камза cantrack red esek inflay ade campriny.\
Саша tecray and.\
Уважаемову.\
Ruinger.

**\
Andrei Bosik** 1:00:32\
61.

**\
Aaron Bockelie** 1:00:40\
Своей они мото СПИДа дели tipsterswain softer.\
Meryage aber abnchive therea and w reddre, twer, sussia, spieke fline.\
Пробериком перебиз компрезидента.\
Аудио долда из этого спрашиваешь?\
Frow dower we itr promestersted sars is supportar dase.\
Herother properys fervery fervery in martine or oree all wiberber холл функции.\
Gosne sare surster support YouTube you worth you wor t we than no go.\
Anite you traw.\
Алло вижу женщину в спросить the se store the leve me goo g gaty, the iside shis libery histel nacare tanklass.\
So I\'m going to make a structure in mine that can make an array of rectangles and draw my bar chart.\
And then Sasha\'s like, great, it\'s working. But this is version one. Version 2 is everybody decides that Sasha\'s platform is going to be a business rendering system for drawing graphs of various kinds, okay? And so you talk with Sasha, not with the code.

**\
Alexander Biratko** 1:02:14\
Ahh.

**\
Aaron Bockelie** 1:02:33\
You sit down at the table or in a meeting and you say, Sasha, can you build me an abstraction for building bar charts? Here\'s what I did in my code.\
I\'m going to write this up as a thing and you can pull requests into yours and we\'re going to upgrade the expectations of the contract. So now Sasha goes, that\'s a great idea.\
Now I\'ve got a bar chart function. And so if any, you can throw away all of your code that you wrote because you don\'t need to worry about it anymore. Sasha has assumed responsibility for creating that, and he is contractually promising. He\'s promising that if you have

**\
Alexander Biratko** 1:02:57\
Yeah.

**\
Aaron Bockelie** 1:03:11\
these things ready, the preconditions, and you feed it this data that is invariant, the post conditions is you will get a graph popping up out of the library. And so you don\'t have to worry about how it works because you\'ve communicated and formed that contract between the two of you.\
And you don\'t have to worry about his stuff. He worries about his concern. You worry about your concern. Zero trust between each other. You negotiate it and discuss. Now, Sasha, whenever he\'s doing work and fixing stuff,\
He doesn\'t consult you every time, that just wastes your time. He just builds his thing and ensures that the contracts he\'s promised to draw graphs remain invariant over time.\
Now, I\'ll throw Andrei into the mix.\
So Andrei, he\'s publishing an analytics platform. He\'s in charge of the analytics platform.\
And Andrei knows that the analytics platform has consumers and stuff in the stuff that Evgeny has created, and it has the rendering system that Sasha has. And Andrei doesn\'t really care how either of them works, because he\'s got his own set of problems to deal with, which is making sure the platform does what it\'s supposed to do.\
So he\'s got a bunch of integration pass checks for everything. If I throw random graph data at it, does the graph run? Yes. Do I throw database data and it gets consumed? Yes. If I run the whole thing and request a graph, does it work? Yes.\
That\'s the kind of checks that Andres system is doing. That\'s integration between the different subsystems inside of your platform.

**\
Andrei Bosik** 1:04:58\
Thank you.\
People.

**\
Aaron Bockelie** 1:05:04\
And so each of you have your own concerns, and you implicitly trust that it works because you have a zero trust model of how it\'s supposed to execute.

**\
Andrei Bosik** 1:05:10\
Okay.

**\
Aaron Bockelie** 1:05:15\
So when it breaks, you go, well, it broke. Okay, we\'ll keep on the same version as before, because Evgeny and Sasha and Andrei are writing out version numbers. You\'re tagging your commits, you\'re tagging your build, right? So Evgeny has a particular version that he has that he\'s working on, and Sasha has

**\
Andrei Bosik** 1:05:36\
Oh.

**\
Aaron Bockelie** 1:05:38\
Tagged a particular version that promises that it can run these, it can draw graphs.\
And when Sasha does a new update, he posts a new version. But Evgeny is smart and says, I depend on Sasha\'s stuff. I\'m going to pin at this version, right? We all pin versions on things. You don\'t just run latest and hope for the best. That\'s crazy.\
So\...\
Between Sasha and Evgeny working as a unit to make sure everything works, they talk to Andrei. Andrei goes, oh yeah, it\'s version XYZ for this and ABC for that. He keeps a record in his integration environment of all of the modules with these versions seem to work pretty well.\
very few bugs in them, we\'re going to push that combination of things in the manifest out to the platform for the customers to use.

**\
Andrei Bosik** 1:06:27\
Business.

**\
Aaron Bockelie** 1:06:31\
And that\'s the overall structure that what I\'m trying to describe here kind of starts to look like.\
Like, Evgeny, if you were to go grab a Postgres SQL Docker image, right?\
To do something with.

**\
Evgeny Kharetski** 1:06:55\
Okay.

**\
Aaron Bockelie** 1:06:55\
Would you just run latest and hope for the best? Or would you pick a particular version and sort of just stick with that for a while?

**\
Evgeny Kharetski** 1:06:58\
No, no.\
BY N.

**\
Aaron Bockelie** 1:07:04\
Yeah, and Sasha, you wouldn\'t just go with the latest Pixie version and hope for the best. You pin Pixie at a particular version, yeah?

**\
Alexander Biratko** 1:07:14\
Yeah?

**\
Aaron Bockelie** 1:07:15\
So, I mean, it\'s the same thing. It\'s just you\'re building it internally. You\'re deciding that your internal systems are no different than the external ones you use. And by calling it zero trust, that means you don\'t trust the other things to actually work ever. You just verify and pin the version with a known thing that actually works.\
And then this way you can kind of let out the, you can spill out of your container the amount of work necessary to improve the surface of your product instead of being subject to the whims of it instead.\
I, I kind of like to\...

**\
Alexander Biratko** 1:08:00\
G.

**\
Aaron Bockelie** 1:08:01\
Maybe I just haven\'t had enough breakfast. I didn\'t eat anything this morning. But when you\'re making food, if you take your flour to make bread, do you just pour the bag into it or do you scoop it out and measure it? You measure it. Otherwise, you\'re going to have some really broken, you\'re not going to have good food. The same thing.

**\
Evgeny Kharetski** 1:08:24\
Okay.

**\
Alexander Biratko** 1:08:26\
Yeah. Data contract integration.

**\
Evgeny Kharetski** 1:08:31\
I think so.\
What principle principle of contractor?

**\
Alexander Biratko** 1:08:44\
I think I pointed out that.\
I switch it.

**\
Evgeny Kharetski** 1:08:55\
Можешь замениться?\
Вопрос о том, как.\
Откуда верхний репозиторий узнает о всех контрактах?\
Возможно, остается открытым для нас, но но то есть условно тут принцип в том, что тесты должны выявлять проблемы на этапе.\
А.\
Энданты интеграционных тестов.

**\
Alexander Biratko** 1:09:23\
Ну тогда возникает вопрос, как другой репозиторий узнает о контракте, ну другого репозитория, которого он нужен?

**\
Evgeny Kharetski** 1:09:30\
Он не.

**\
Alexander Biratko** 1:09:35\
То есть если они вообще еще нечем, не знают друг о друге, значит они и контракты друг друга не знают, где они узнают контракт.

**\
Evgeny Kharetski** 1:09:35\
Ты.\
Но.\
Но ты должен когда то используешь чей то.\
Как это сказать? Чита услуги, да ты должен уточнить, что там с той стороны умеют и использовать это.

**\
Alexander Biratko** 1:09:57\
Вот работа и дело, что мы говорим о том, что клон будет писать, например.\
И значит наш.\
Репозиторий, в котором мы работаем, должен иметь ссылку на тот репозиторий, для которого мы ну, на который мы пишем контракт, или.\
Используем его контракт, но мы говорили, что мы друг о друга не знаем, поэтому здесь возникают проблемы.

**\
Evgeny Kharetski** 1:10:23\
Я согласен, я тоже не очень понимаю как пока что как.

**\
Val Levitan** 1:10:27\
Я, я не думаю, что в этом проблема.\
Я думаю, что в этом вся прелесть.\
Потому что это это проходит обратно к теории зироу Траст.

**\
Evgeny Kharetski** 1:10:31\
Но.

**\
Alexander Biratko** 1:10:37\
Нет, мы мы к тому, что связь между между 2 этими репозиториями, она должна быть тогда.

**\
Val Levitan** 1:10:38\
Я понимаю.\
Я не вижу этой связи, я не понимаю, зачем она должна быть.

**\
Alexander Biratko** 1:10:47\
Ну смотрите вот как арон прием, привел пример, один делает трендер движок 2 делает там то что делает то, что будет рендериться, как вот этот вот женя, которая будет делать для рендер движка чтото?\
Смог что то сделать, не зная португаль контракта, дата контракта движках.\
Рендера.

**\
Evgeny Kharetski** 1:11:14\
Я должен его знать?\
Но я могу пойти и посмотреть. Собственно, тут тот речь идет о том, чтобы ну и как бы клод это всё.

**\
Alexander Biratko** 1:11:20\
Ну поэтому но но но.\
Знал.

**\
Evgeny Kharetski** 1:11:27\
Как так? Как тогда аккумулировал в себя, понимал куда ходить, зачем ходить, как ходить и так далее.

**\
Val Levitan** 1:11:35\
Я я я так не вижу.\
Я вижу что.\
Когда делается апплищен, который разговаривает с вашим аппликеном.\
Нет секунду.\
Ладнот inbook wication infedy snoniум зор пэррео зорком перерисон leches tuerpen beanor.\
Соул.\
Это концепция частый зондеструт, он консептов дейзонд свои черепазы.\
А ты ракт?\
Это то есть оборствовал sunderstored.\
Кто то надо аплакать да и новочную пазы.\
Эстрада самтонион топовет lega lack candactorandy orces sher des.\
RMT filldet.

**\
Aaron Bockelie** 1:13:10\
Да, это компания. То есть way more ditstedas.\
Соу.\
Мы с тобой так пошли?

**\
Val Levitan** 1:13:21\
Но я Сталин в этот комплект компресс.

**\
Aaron Bockelie** 1:13:25\
Я гол окей.\
Вил виллы, вилластик.

**\
Val Levitan** 1:13:27\
Я мы печастану докощен вот а вот.

**\
Aaron Bockelie** 1:13:31\
And thes prely castle, battsy, say hove.\
Сами вот теперь.

**\
Evgeny Kharetski** 1:13:53\
One second.

**\
Alexander Biratko** 1:13:53\
backend and front-end, any application.

**\
Aaron Bockelie** 1:13:57\
Fine. What is the front end written in?

**\
Alexander Biratko** 1:14:04\
Front should call some get post IP.

**\
Val Levitan** 1:14:09\
Music here on the pizza.

**\
Alexander Biratko** 1:14:11\
Ohh, never mind.

**\
Aaron Bockelie** 1:14:12\
Is it react?

**\
Alexander Biratko** 1:14:14\
Example react just just JS native JS.

**\
Aaron Bockelie** 1:14:15\
OK, what?

**\
Evgeny Kharetski** 1:14:18\
Yes.\
Thank you.\
Yes, on Java backend.

**\
Alexander Biratko** 1:14:22\
And Java backend.

**\
Aaron Bockelie** 1:14:23\
What\'s the back end?

**\
Evgeny Kharetski** 1:14:24\
Jama.

**\
Alexander Biratko** 1:14:24\
John.

**\
Aaron Bockelie** 1:14:26\
Okay.\
How is Java invoked? Is it Apache?\
How is it run?

**\
Alexander Biratko** 1:14:33\
I\'m cut.

**\
Evgeny Kharetski** 1:14:34\
Uhh\...

**\
Aaron Bockelie** 1:14:35\
Tomcat, alright.

**\
Alexander Biratko** 1:14:36\
Spring, spring, tomcat.

**\
Evgeny Kharetski** 1:14:36\
Big.

**\
Aaron Bockelie** 1:14:38\
Sure, Spring Framework, Tomcat, whatever.\
Does the front end give two \*\*\*\*\* about what the back end runs inside of? Or is it all rest based?

**\
Alexander Biratko** 1:14:52\
Yes.

**\
Aaron Bockelie** 1:14:53\
All rest based, right?

**\
Evgeny Kharetski** 1:14:54\
Yes, yeah, yeah.

**\
Alexander Biratko** 1:14:54\
Yes, yes.

**\
Aaron Bockelie** 1:14:56\
So I could go theoretically.\
Take the Java.\
Rewrite it all in Rust, and it would work exactly the same, right?

**\
Evgeny Kharetski** 1:15:06\
Yes.

**\
Aaron Bockelie** 1:15:08\
Where is the contract of what that backend does? What is the contract?

**\
Evgeny Kharetski** 1:15:16\
Um\...

**\
Alexander Biratko** 1:15:18\
If we don\'t write in separate file, it\'s just some SharePoints.

**\
Evgeny Kharetski** 1:15:25\
One.

**\
Aaron Bockelie** 1:15:28\
I would I would postulate that the contract, from my perspective as a React front-end developer, is that there is a\...

**\
Alexander Biratko** 1:15:29\
Mm.

**\
Aaron Bockelie** 1:15:41\
There is a set of API endpoints that I can use that are described.

**\
Alexander Biratko** 1:15:45\
Yes, yes.

**\
Aaron Bockelie** 1:15:47\
That\'s the only contract I need as a front-end developer.\
But, what?

**\
Alexander Biratko** 1:15:53\
Yes.

**\
Aaron Bockelie** 1:15:55\
Does the backend developer need to care about the front end?

**\
Evgeny Kharetski** 1:16:01\
Oh.

**\
Alexander Biratko** 1:16:03\
What front-end should\...\
You, you means front-end is first.

**\
Evgeny Kharetski** 1:16:09\
Long time.\
Ohh.

**\
Aaron Bockelie** 1:16:13\
No, there\'s no first or last here. So if\...\
If the front end.

**\
Evgeny Kharetski** 1:16:18\
If, if he, if he will get you.

**\
Alexander Biratko** 1:16:18\
If you will get new API on backend, how front will know about new?

**\
Evgeny Kharetski** 1:16:23\
He, how long you know about?

**\
Aaron Bockelie** 1:16:28\
Front doesn\'t know anything. Front doesn\'t trust back. Back doesn\'t trust front.

**\
Alexander Biratko** 1:16:28\
Rudky.

**\
Aaron Bockelie** 1:16:34\
So if backend creates a new endpoint, some API call, API endpoint in REST.\
The front end should work exactly the same as it did before.\
Right? A non-breaking change to a new API endpoint for some new thing.\
Let\'s assume the backend is a payment system backend, okay?\
and I create a new endpoint for a new type of payment style.\
It\'s actually not even a new full endpoint. It\'s just like a property inside of an existing.\
at rest endpoint for managing a payment system of some kind.\
The front end doesn\'t trust the back end. The front end has no idea that the back end has this new capability to accept payment in this new form.\
We don\'t care because we don\'t trust it.\
So now what has to happen is external to both the front end and the back end. Someone said, hey, back end team, add a new payment capability for X.\
Okay.\
The backend team adds this new payment capability for X, and they\'re like, I\'m done.\
The front-end team probably is aware that this happens because you guys sit next to each other. Hey, we added a payment capability for X, right? So the front-end team is like, all right, for back-end team, how are you actually implementing it? The back-end team says, oh, we\'re just going to add a new property.\
it over here so you can plan. The front-end team can work in parallel while the back-end team is actually building, but they don\'t trust it yet because they\'re still working on an older version.\
When the front-end team finally gets to implementing what they think works, according to how the back-end team says that their spec is going to be written for that capability of that payment thing.\
Then we never tried it yet. We\'ve never done any integrations tests. So now the integration team, that would be Andrei, gets involved with making sure that he has a test that can issue a payment through driving the front-end web interface and expecting a back-end payment in that new type.\
The work.\
So we have a trifecta here. We have the back end with a new capability that was driven first. We have the front end that was then created to leverage this back end capability. And we have the operational platform, which verifies that both work.\
and can trust it and then moves forward to push that into the environment.

**\
Val Levitan** 1:19:28\
And actually, if I may quickly interject in here, actually, it doesn\'t matter who goes first, front end or back end. And front, well, well.

**\
Aaron Bockelie** 1:19:35\
No.\
Well, it kind of does, because if you expose the front end and somebody clicks it and it breaks, that\'s a problem.

**\
Val Levitan** 1:19:41\
Well, hold up, hold on.\
Well, I don\'t know if it\'s possible to write a routine that if back end doesn\'t answer, then the front end just loops into something else. Maybe.

**\
Aaron Bockelie** 1:19:52\
Sure, it could say not supported or something like that.

**\
Val Levitan** 1:19:54\
Yeah, maybe not support it yet, but the the point the point in this architecture is that.\
a repository that is on this side of the river, on this side of the bank.

**\
Aaron Bockelie** 1:20:10\
We can\'t see your video if you\'re I can\'t see your video at least.

**\
Val Levitan** 1:20:13\
You cannot?

**\
Aaron Bockelie** 1:20:14\
No, you\'re just a gray rectangle.

**\
Evgeny Kharetski** 1:20:15\
No.

**\
Val Levitan** 1:20:16\
Really? I\'m so sorry.

**\
Aaron Bockelie** 1:20:17\
Yeah, that\'s OK.\
Some days were just gray rectangles, though.

**\
Val Levitan** 1:20:24\
Oh man, I see my picture and everything. Ah, I have to sign in the \*\*\*\*\*\*\* team, the \*\*\*\*\*\*\* \*\*\*\*\* \*\* \*\*\*\* mic.

**\
Aaron Bockelie** 1:20:31\
Yeah.\
And this is the day that we switched to Google Meet, isn\'t it?\
I\'m joking. Maybe. I don\'t know. I\'m trying not to make more work for you guys.

**\
Alexander Biratko** 1:20:53\
And I have a question about it.

**\
Evgeny Kharetski** 1:20:53\
Thank you.

**\
Val Levitan** 1:20:56\
I \*\*\*\*\*\*\* hate Microsoft.

**\
Alexander Biratko** 1:20:57\
Ah.

**\
Aaron Bockelie** 1:21:00\
Oh, I can see you now at least. Now I get to see your rage and it\'s working, so that\'s always good.

**\
Val Levitan** 1:21:06\
I \*\*\*\*\*\*\* hate this \*\*\*\*\*\*\* Microsoft \*\*\*\*\*\*\* Bill Gates.

**\
Aaron Bockelie** 1:21:12\
Yeah.

**\
Val Levitan** 1:21:14\
Mark and socialist.\
Maybe.

**\
Alexander Biratko** 1:21:20\
Uh.

**\
Val Levitan** 1:21:21\
Already.\
Um\...\
I was saying that, I think what you\'re saying, if I understood it in my primitive language, is that in this example,\
the repositories that are, so we have a river, we have left bank and the right bank.\
Right bank, let\'s assume that right bank is a bunch of backend repositories.\
And Left Bank is a bunch of front-end repositories. The only way they know about each other is the end-to-end protocol of some sort. They really don\'t know anything about each other. They don\'t give a \*\*\*\* about each other.

**\
Aaron Bockelie** 1:22:07\
Mhm.\
Nope.

**\
Val Levitan** 1:22:13\
So, that\'s why all of the repositories that are on the\...\
Right bank of the river.\
They also have, they really don\'t care about each other because they\'re quite independent.

**\
Aaron Bockelie** 1:22:27\
Mhm.

**\
Val Levitan** 1:22:29\
And the only thing that unites them is that river, that flow of information.\
that is represented in the end-to-end communication.

**\
Aaron Bockelie** 1:22:39\
Yeah.

**\
Alexander Biratko** 1:22:43\
I see one problem.\
Who will write the test?

**\
Evgeny Kharetski** 1:22:48\
By at best.

**\
Aaron Bockelie** 1:22:51\
Usually, the developer writes the test to assert that they can do the thing.

**\
Evgeny Kharetski** 1:22:54\
The developer.

**\
Alexander Biratko** 1:22:54\
The developer should know about the protocol data contract.

**\
Evgeny Kharetski** 1:22:57\
Should know about.\
Love it.

**\
Aaron Bockelie** 1:23:02\
Think about it like this.\
The developer has to write at least unit tests to ensure that their code does what it does, right?

**\
Evgeny Kharetski** 1:23:11\
Yeah.

**\
Aaron Bockelie** 1:23:12\
And if you\'ve got a bunch of unit tests, what are unit tests other than ensuring consistency of whatever it is you\'ve built?

**\
Alexander Biratko** 1:23:22\
Right.

**\
Aaron Bockelie** 1:23:23\
So here, let me give you a screen share of something.\
I have previously told you about my excursion into writing software libraries for Bluetooth stack for headphones, yeah?

**\
Evgeny Kharetski** 1:23:35\
Yeah.

**\
Aaron Bockelie** 1:23:36\
This is when I run rust doc.\
You know, if your cargo dock, if you ever run cargo dock, it\'s kind of magic.\
You get a HTML page, right? Static. This is all of the connection methods available in this Rust crate that I\'ve got to be able to write something to control headphones.\
This is essentially the code contract that I that I promise will work.\
Right.\
So these public functions, see how many public functions there are in this transport for BMAP connection.\
Create a connection from Transport and Device Config.\
Device configuration, start the drain to all the async, blah, blah, blah. Just kind of, you know, there\'s just all this stuff in here, right? And so we can look at it and we can see all of the promises inside of there.\
Now, if I instead of looking at that, let\'s look at some of the traits that we have. These are implicit traits for sending things to the connection. And there\'s different implementations, and there\'s different structures that we have. Like we have to promise a particular structure for this, right? This is all normal stuff.\
This is the code level contract of what\'s going on here, because the very moment that I rename battery to batteries, I\'ve broken the contract with anybody else who uses this library to make software, and it\'ll break everybody\'s software when they compile against it, right?

**\
Evgeny Kharetski** 1:25:10\
Yes.

**\
Aaron Bockelie** 1:25:10\
So I, as the owner of this particular thing, would say, hey guys.\
For a reason, I renamed the function, the public function of battery to batteries.\
You will break on the next version of the, if you pin your version against the newest version, watch for that because it\'ll break.\
I don\'t care who uses my software. I give, I don\'t care at all. I don\'t trust them. I don\'t care. But I provide the convenience or the, what was the term that Val coined several years ago now? The\
It was the something about\...\
Was it was the courtesy of disclosure or something like that that you said, Val, remember it?

**\
Val Levitan** 1:26:04\
Yeah, yeah.

**\
Aaron Bockelie** 1:26:06\
The courtesy is that the release notes are danger, breaking change. I changed live battery to batteries. All of your builds are going to break when you switch to this version, so watch for that and change it in your code. That\'s the courtesy of disclosure or courtesy of.\
you know, telling people. I don\'t have to. I could just do nothing and just change it and be one of those self-important developers and let everybody just deal with it. But people might eventually switch away from this library to something else. Or if you\'re inside of a company and it\'s all captive with private stuff, you\'re going to get the short end of the \*\*\*\*\*\* stick because everybody\'s going to be upset with you that you changed something without telling anybody.\
and wasting time and money.\
So this is what I\'m saying is is that code contracts are normal things, but it\'s just that abstracted term kind of the reality is something like this and you could just as easily have\
an open API specification that goes all of your REST endpoints, or a GraphQL introspection endpoint that lets you look at all the graphs. It depends on what context and what you\'re looking at. C, you can go static analysis all the functions too, or in Java, or in Python, or whatever. It\'s just\...\
It\'s this promise that this is the way the software works, and let me enumerate it. And so when somebody wants to write a headphone application, they can read that Rust Fargo doc and kind of go, oh, I get it. If you\'re creating an audio management subsystem for an arcade.\
For a game cabinet, it\'s going to have promises about that.\
And then you get into all the crazy details about how maybe this hardware isn\'t supported, and this hardware has these features and those capabilities, and you have an abstraction layer. And so your full contract has a lot of stuff about enumerating the capabilities of this particular hardware platform. Oh, by the way, I\'ll also tell you what audio platform.

**\
Alexander Biratko** 1:27:48\
Shh.

**\
Aaron Bockelie** 1:28:06\
performance using and stuff, and so forth. So you build these, all these assumptions sort of start to grow into things. If you\'re creating a game that needs stereo audio and high fidelity this and that and channels and whatever, you must use this thing. And so you kind of start to grow into the assumptions of how everything works.\
And part of the job of the whole architecture of this is to make sure you don\'t become codependent on assumptions and lock everybody into one big mess at the end of the day.

**\
Val Levitan** 1:28:41\
So nobody says \*\*\*\*\*\*\* Microsoft.

**\
Aaron Bockelie** 1:28:43\
Right.

**\
Alexander Biratko** 1:28:47\
Let\'s back to our example, backend, frontend, and backend has new API.

**\
Evgeny Kharetski** 1:28:47\
That.\
Sample.

**\
Aaron Bockelie** 1:28:56\
Yep.\
Back in his new API, yeah?

**\
Alexander Biratko** 1:28:58\
In this.

**\
Evgeny Kharetski** 1:28:58\
Please.

**\
Alexander Biratko** 1:29:00\
Yeah.

**\
Aaron Bockelie** 1:29:01\
OK.

**\
Alexander Biratko** 1:29:01\
And in this case, integration repos should add new test for new API back backend.

**\
Evgeny Kharetski** 1:29:02\
And in this case.\
Information records.\
Four.

**\
Alexander Biratko** 1:29:18\
I right understand, and\...

**\
Aaron Bockelie** 1:29:18\
Yeah.

**\
Evgeny Kharetski** 1:29:18\
Brothers.

**\
Andrei Bosik** 1:29:19\
I think, yes.

**\
Evgeny Kharetski** 1:29:19\
And the\...

**\
Aaron Bockelie** 1:29:19\
So that would be the next, so that, so let\'s put it in order, okay? Time order of implementation. Order number one, the back end creates a new API endpoint, okay? And the new API endpoint.\
Already ships with test unit tests.\
So we can assume that the, let me write this down. I\'m gonna actually type it in chat as we follow along. One, back end gets a new API endpoint.

**\
Andrei Bosik** 1:30:00\
And one more question. What is the first? First, we create contract and then we implement changes or we create changes and then update our data contract.

**\
Aaron Bockelie** 1:30:04\
Sood.\
No, you don\'t make any contracts.\
No, no.

**\
Evgeny Kharetski** 1:30:12\
I.

**\
Aaron Bockelie** 1:30:13\
No, no, look at the chat. One, back end gets a new API endpoint with and ships with unit tests asserting the stableness of the endpoint. Okay.

**\
Evgeny Kharetski** 1:30:25\
CA.

**\
Aaron Bockelie** 1:30:25\
We can say just for just for order preference precedence, let\'s do 0 for a minute.\
So step 0 is this actually. This is your customer. Juan wants a new thing that is decided and it is decided to add a new API endpoint.

**\
Evgeny Kharetski** 1:30:41\
Yeah.

**\
Aaron Bockelie** 1:30:52\
OK, the business wants this thing.

**\
Evgeny Kharetski** 1:30:53\
OK.

**\
Aaron Bockelie** 1:30:58\
So after one, we get it back and gets a new API endpoint and ships the unit test, asserting the stableness of the endpoint. Let\'s go to what Sasha, what you\'re saying is that step 2 is that the CI integration.\
group owner creates an integration test for this, yeah.\
So, step two.

**\
Alexander Biratko** 1:31:21\
Yeah.

**\
Aaron Bockelie** 1:31:53\
Okay, so step 2 is the CI integration creates new tests to verify the API endpoint, right?

**\
Val Levitan** 1:31:54\
Yeah.

**\
Aaron Bockelie** 1:32:01\
They\'re not unit tests, they\'re CI tests.\
They only have tests for ensuring the API exists right now. This now asserts in the CI pipeline that the new API endpoint will be trusted.\
I\'m going to add another note to this.\
So this is incomplete because there is no front end yet, right?

**\
Val Levitan** 1:32:24\
Yeah.

**\
Aaron Bockelie** 1:32:28\
The whole capability for the platform is incomplete. So we can mark it as testable, but incomplete.

**\
Evgeny Kharetski** 1:32:29\
Yes.

**\
Aaron Bockelie** 1:32:36\
And what\'s step three?\
Sasha, what\'s step three?\
Run in, right?

**\
Alexander Biratko** 1:32:50\
Maybe do front-end.

**\
Aaron Bockelie** 1:32:55\
Right, so front-end.

**\
Alexander Biratko** 1:32:57\
Bolt.

**\
Aaron Bockelie** 1:33:31\
So that\'s step 3. And then step 4.

**\
Val Levitan** 1:33:32\
Yeah.

**\
Alexander Biratko** 1:33:32\
Yeah.

**\
Val Levitan** 1:34:01\
Yeah.

**\
Aaron Bockelie** 1:34:01\
Step 4 is you improve the CI, right? CI integration adds tests to the capability for this concern. Now they\'ve got a bundle of tests to assert the back end, they can assert the front end, and they can assert a flow from front end to back end.\
And so it holds on to that now.

**\
Alexander Biratko** 1:34:24\
For use new API, front-end should know what is API.

**\
Evgeny Kharetski** 1:34:25\
No one is.\
That she.\
No, what is?

**\
Aaron Bockelie** 1:34:33\
But tell me what you mean by no. How does code know something?

**\
Alexander Biratko** 1:34:39\
Data model.\
Data model.

**\
Aaron Bockelie** 1:34:43\
Okay, does the front end, does front end developers usually hold a data model?\
Or do they hold an experience?

**\
Alexander Biratko** 1:34:59\
See to backend repo.

**\
Evgeny Kharetski** 1:35:00\
Yeah.\
Accounts.

**\
Aaron Bockelie** 1:35:03\
Right. The back end repo has asserts their claim that these are the things I do. The back end says I give 2 \*\*\*\*\*. I do not care what the front end thinks.

**\
Alexander Biratko** 1:35:04\
Yeah.\
Yeah, but but and front end should be without backend.

**\
Aaron Bockelie** 1:35:17\
Right.

**\
Evgeny Kharetski** 1:35:24\
So, welcome.

**\
Aaron Bockelie** 1:35:26\
Front end looks at back end and says, OK, back end, I trust you. You\'re not going to change, right?

**\
Alexander Biratko** 1:35:32\
Then, backend is then then backend should be first.

**\
Evgeny Kharetski** 1:35:32\
Then, back and then, then back and see you first.

**\
Aaron Bockelie** 1:35:39\
Back end is probably first, right? Because if you don\'t have a front end, it breaks. Unless you have, you\'re preloading things or whatever, this feature isn\'t supported yet or whatever you want to do. Every single one of those patterns adds complexity. And when I say the front end trusts the back end, the front end only trusts the back end is as far as it gets.\
can for its current iteration. The front end never trusts the back end, it just asserts that it works.\
I can build whatever crazy stuff I want on the front end, but if there\'s no back-end endpoint to sustain it or support it, the front end\'s just going to do nothing.\
Right.

**\
Evgeny Kharetski** 1:36:22\
Yes.

**\
Aaron Bockelie** 1:36:23\
I could build a huge mockup of the whole product in the front end. And there\'s like literally one backend API endpoint that actually works. Maybe call it Auth.

**\
Andrei Bosik** 1:36:23\
Yeah.

**\
Evgeny Kharetski** 1:36:24\
Okay.

**\
Aaron Bockelie** 1:36:32\
then everything hasn\'t been built yet for the front end yet. And none of it works. But it will work eventually because we built all of this UI convention, right? Because we\'d already made a ton of assumptions that we will eventually have a back end that worked.\
And if it turns out that you completely changed the back end to some other set of conventions or API endpoints, you have a lot of work ahead of yourself to make the front end do what it needs to do.\
But if the back end completely changes its code but remains consistent in the way it behaves, the front end actually doesn\'t care.\
You can completely walk, take it out and put something else in instead.

**\
Evgeny Kharetski** 1:37:22\
Yeah, my rules come.

**\
Aaron Bockelie** 1:37:23\
That\'s the boundary that I was talking about in the chat that I shared.

**\
Evgeny Kharetski** 1:37:25\
Ohh.\
Yeah, you should open your mile.\
Data contractor, the file abstract.

**\
Aaron Bockelie** 1:37:53\
Процент.

**\
Evgeny Kharetski** 1:37:55\
Ну индийский кейс.

**\
Aaron Bockelie** 1:38:05\
Да с.\
Serry serd o you spiete prone and.\
FUR am.

**\
Evgeny Kharetski** 1:38:28\
Угу.

**\
Aaron Bockelie** 1:38:43\
Да таким.\
Howdester stars of irina wetronet on setsister.\
When it executes in.

**\
Alexander Biratko** 1:38:54\
But we, but we can have next case when front say we need.

**\
Evgeny Kharetski** 1:38:55\
The.\
Hello.\
Only.

**\
Alexander Biratko** 1:39:07\
To do this page with this data model and backend.

**\
Evgeny Kharetski** 1:39:07\
To do this page.\
Please.\
And Biratko.

**\
Alexander Biratko** 1:39:16\
Do it.

**\
Evgeny Kharetski** 1:39:16\
Movie.

**\
Aaron Bockelie** 1:39:20\
I\'m not sure what I understand by that.

**\
Evgeny Kharetski** 1:39:28\
First question, are those competitive results?

**\
Alexander Biratko** 1:39:28\
The.\
Inna.\
Front end.\
Yeah, it.

**\
Val Levitan** 1:39:42\
Sometimes, front-end requests a certain page with certain data.

**\
Aaron Bockelie** 1:39:48\
Right?

**\
Alexander Biratko** 1:39:48\
A backend, a backend projects a idiot post the front end of a sleder to most on process.

**\
Evgeny Kharetski** 1:39:48\
Yeah, yeah.\
What is it?

**\
Val Levitan** 1:39:53\
And then.\
And back end follows the front end in that case.

**\
Aaron Bockelie** 1:39:59\
No.\
Who\'s the source of truth?

**\
Alexander Biratko** 1:40:04\
Oh.

**\
Evgeny Kharetski** 1:40:04\
Cool.

**\
Val Levitan** 1:40:05\
Toys flushing properly.

**\
Evgeny Kharetski** 1:40:08\
With the stock control plus.

**\
Alexander Biratko** 1:40:08\
I don\'t know.\
I, I think that\'s a contract.

**\
Aaron Bockelie** 1:40:15\
No.\
I think that the source of truth emerges from the interaction, the data contracts arise from the mutual understanding of the different systems.\
At the end of the day.\
You have to think about what it is your application is.

**\
Val Levitan** 1:40:33\
It\'s actually quite interesting. So you\'re saying that the data contract is not static.

**\
Aaron Bockelie** 1:40:39\
No.\
Always moving and shifting.

**\
Val Levitan** 1:40:41\
And, and, and I think they they interpret it as data contract is written once in the static.

**\
Aaron Bockelie** 1:40:48\
If you write it once, then your application will never change.

**\
Val Levitan** 1:40:52\
It will age. It\'s actually interesting. I never thought about it.\
I wanna make sure they understand this.

**\
Evgeny Kharetski** 1:40:59\
Am I too much?

**\
Aaron Bockelie** 1:40:59\
Every time you change the features, it changes.

**\
Alexander Biratko** 1:40:59\
Peck.

**\
Val Levitan** 1:40:59\
Sood.\
So, so, so it\'s a if it\'s a life organ, then\...\
there must be negotiation that takes place between the two interactions. And you as a system architect, you mitigate it, and you say, yeah, yeah, yeah, let\'s advance the data contract. And then it advances on both sides.

**\
Aaron Bockelie** 1:41:21\
What\'s interesting is that I\'m picking this up in the way that I feel like it\'s being discussed as if these systems can negotiate themselves, which is not true. I might be, maybe I\'m just falsely picking this up on this. The only thing that negotiates.

**\
Val Levitan** 1:41:34\
You, you can you can only you can only pick it up from me, but I am not an engineer and I\'m \*\*\*\*\*\*\*\*\*\*\*\* my way through, so if you\'re picking it up from me, you should kill it immediately.

**\
Aaron Bockelie** 1:41:39\
Yeah.\
Sure.\
Okay.\
Yeah, so the reality is that it\'s people that make these contracts. It\'s people that make the code somehow work.\
Maybe they use cloud code to write the code, but it\'s still people that define what it\'s going to do.

**\
Val Levitan** 1:42:02\
but today it\'s people. But eventually it will start, the cloud code will pick it up and will say, look, we have contract non-compliance here. One side knows about this, another side tells me this, what should we do? And today the person will probably make a decision.\
In the future, maybe not, I don\'t know. But the point is that I think me and the guys at Minsk probably understood that the data contract is a static element, or it\'s not, it\'s a progressive element.

**\
Aaron Bockelie** 1:42:27\
Okay.\
The data contract is valid as long as\...\
and whatever that contract actually is.\
The promise of whatever it\'s going to do remains the same until someone chooses to change the promise.\
The terms of service that this\...\
This mod, this this capability has.\
So I want to\...\
I want to address this like both the future state and current state and what it kind of implies.\
So, any of these systems?

**\
Val Levitan** 1:43:15\
Before you go on, can I ask them a question on how they understand the data contractors?

**\
Aaron Bockelie** 1:43:17\
Sure.\
Yeah.

**\
Val Levitan** 1:43:21\
I have to open my data contract.

**\
Evgeny Kharetski** 1:43:24\
No, yeah. Source of truth.

**\
Val Levitan** 1:43:45\
You still, you still on?

**\
Evgeny Kharetski** 1:44:04\
Talk to dozen that is related to that contract.

**\
Val Levitan** 1:44:16\
So, you begin this?

**\
Evgeny Kharetski** 1:44:21\
Mm.

**\
Val Levitan** 1:44:22\
Prosthetic, prosthetic.

**\
Andrei Bosik** 1:44:24\
Oh, amazing tool.\
These we need to know.

**\
Val Levitan** 1:44:31\
Okay, so Evgeny understands that a data contract is written by, let\'s say, assume that he is writing the code as him. So he writes the data contract first.\
It\'s a document, I don\'t know, it\'s probably dot MD, I assume. Maybe, I don\'t know what he means by that.\
And the data contract exists first, then you start applying code to it. Then if data contract, if something changes and the data contract needs to be advanced, he publishes a new version of data contract. The old data contract does not disappear.\
but a new data contract adds to the old contract or differences established, I assume, or additions are added.\
And from there, the reliance is on new data contract. That\'s how he understood. I\'m just simply translating. I\'m acting as a translator.

**\
Aaron Bockelie** 1:45:24\
For sure, yeah.

**\
Val Levitan** 1:45:27\
Is that is that how it works?

**\
Aaron Bockelie** 1:45:31\
No, I\'m typing it out.

**\
Evgeny Kharetski** 1:45:35\
Yeah, yeah, boy.

**\
Val Levitan** 1:45:55\
I\'m still not.

**\
Evgeny Kharetski** 1:45:58\
No, yesterday it\'s a bullet.\
No, sketch them, sketch them.

**\
Val Levitan** 1:46:07\
OKOK, no.

**\
Andrei Bosik** 1:46:07\
When you have a process.

**\
Aaron Bockelie** 1:46:29\
Uh, I want you to read that thing there.\
So\...\
Let me know when you\'re done.

**\
Val Levitan** 1:47:33\
This is going to, I mean, I understand, I understand the capabilities and requirements, all understood, but we need to assume that capabilities and requirements have been provided and understood, because what you just did now with this statement is you essentially.\
Put the entire JVL at a still stand. We won\'t be able to produce one \*\*\*\*\*\*\* thing.\
Because we don\'t have the infrastructure. The small companies don\'t have infrastructure to take it from requirements and capabilities. It\'s just the reason such an infrastructure.

**\
Aaron Bockelie** 1:48:14\
I agree and disagree with you simultaneously, Val, and let me explain why.

**\
Val Levitan** 1:48:18\
That\'s not, that\'s not, that\'s not a problem. I, I, I have no problems for you disagreeing. I\'m just telling you factual thing.

**\
Aaron Bockelie** 1:48:21\
Yeah, yeah, but, but let\...

**\
Val Levitan** 1:48:27\
I\'m just telling you how binary minds think, and you just cannot get it through your mind. It just\...\
It\'s remarkable, you know.\
At the end of this whole thing, there is only one source of truth. You know what that source of truth is?\
Take one guess.\
It\'s a word consisting of four letters.\
It\'s called Kesh.

**\
Aaron Bockelie** 1:49:02\
Yep.

**\
Val Levitan** 1:49:03\
If I cannot make cash.\
Then, nothing works.\
I don\'t care what theory you put in place. I don\'t know how you build your software. The bottom line, I must get cash.

**\
Aaron Bockelie** 1:49:23\
So, I have, there\'s a follow-up in this, is that what I\'m telling you by ideally\...\
that you start with requirements and capabilities and build all that.\
That\'s the that\'s the right way to do it.\
If you already have code that works, you already have a contract.

**\
Val Levitan** 1:49:42\
Maybe it\'s the right way to do it, but you are telling this to binary minds. So all they do now is they say, you know what, I buy into it. That\'s amazing, fantastic.

**\
Aaron Bockelie** 1:49:56\
There is a\...

**\
Val Levitan** 1:49:57\
Go, go, go and get me requirements and capabilities. Just go, go, go do it, go do it.

**\
Aaron Bockelie** 1:50:02\
No, it won\'t happen because you guys can\'t do it. So\...

**\
Val Levitan** 1:50:05\
OK, so why do you put it there?

**\
Aaron Bockelie** 1:50:08\
Because that\'s the right way to do it.

**\
Val Levitan** 1:50:10\
I know, but we\'ll get there. But first, they need to understand what the contract is. That\'s the narrow subject.

**\
Aaron Bockelie** 1:50:17\
It\'s very straightforward right now. The contract is whatever the hell your software does right now is the contract.

**\
Val Levitan** 1:50:23\
Okay, so how do we get it? We need practicality.

**\
Aaron Bockelie** 1:50:26\
It\'s already, you already got it.\
You already have it. Give me your code for Java and I\'ll create Javadoc and you\'ll have your contract.

**\
Val Levitan** 1:50:37\
So, tell him that, so tell, so tell him that.

**\
Aaron Bockelie** 1:50:37\
Your contract already exists.

**\
Val Levitan** 1:50:41\
So if you tell them that, they will interpret it this way.

**\
Aaron Bockelie** 1:50:41\
Because it\'s in four different ways. It\'s in whatever many different languages you\'ve got, and it is whatever many different layers you\'ve got, because you\'ve got API layers and code layers and data model layers, and everything is a different type of contract.\
Open that HTML file that I sent you to. It\'s a table listing what I would consider a contract across a whole bunch of different things.\
So each of these is essentially your contract.\
I am it, I consume.\
What\'s the surface, right?\
If you have all the same language across all of your stuff, and all you\'re doing is\...\
Writing things, even there, you\'re still going to end up with some sort of other layer of interaction.\
As soon as you throw an HTTP, you know, a web service in front of something, you have another layer of contracts on top of the code itself.\
O.\
The Val spread it saying, cash is what speaks.\
The probably the most straightforward thing to do is to make sure that whatever your application is doing right now, you can present this information to people and that\'s the contract of what it should do.\
A contract is not a literal legal document that\'s written in markdown inside of your software. That\'s stupid. A contract is dynamic and generated from the code as it\'s written and enforced by code tests that make sure it does the right thing.\
If you want an actual document that describes it as a contract, you don\'t write down statically, oh, this function does this and that function does that.\
You instead write out these functions will do these capabilities and it fulfills these obligations. Throw that as a markdown file inside of the Git repo alongside of it, and then make sure that all of the developers, both AI and human, ensure that whatever\
Document that comes out of the code language that you\'ve chosen supports all that and can be referenced to it.\
You can literally write down inside of the Java doc what JIRA issue or exactly what function or capability this thing is for.\
This ties it directly to that. It\'s about creating that network of understanding across everything.\
When you have huge, sprawling services and systems that work everywhere, the only thing you can do is to not trust the other systems. You just have to publish what you\'re capable of doing.

**\
Evgeny Kharetski** 1:53:55\
The.

**\
Aaron Bockelie** 1:54:02\
Don\'t try to formalize a data contract by writing it down as a document and publishing it like that.\
You should make that part of your continuous integration for the whole system.

**\
Evgeny Kharetski** 1:54:13\
Yes.

**\
Aaron Bockelie** 1:54:15\
So\...\
Let\'s pick one module per minute. FlexPay API backend, okay?

**\
Evgeny Kharetski** 1:54:20\
What?

**\
Aaron Bockelie** 1:54:24\
It has a Swagger endpoint for being able to tell you what all the rest URLs are.\
And when you\...\
post that code to the code repo, not the integration repo, just its own. It can stand on its own and operate. It doesn\'t need a front end to work. It just needs to have the API interface be operated in the correct manner, and it should function on its own, right?\
So as soon as you build that and you post it, you\'re going to run static analysis and write, and you\'re going to create the Swagger document. It\'s going to get generated into actual static text that\'s posted in the documentation directory.\
inside of the repo so anybody could browse it and go, oh, that\'s what it does. So they can just read the docs. They don\'t have to run the code. It\'s right there. And every single commit updates the docs because part of the CI process does that.\
There, there is never anybody writing docs by hand for data contracts using data contracts.\
It\'s always just sort of updated anytime the code\'s updated, because the code is what actually matters, and the code is actually what drives it. And therefore, any handwritten anything is always out of date.\
You\'re muted, Val.

**\
Val Levitan** 1:55:59\
So if there is a code written today, how do you back into a data contract from a code?

**\
Aaron Bockelie** 1:56:09\
If it\'s Java, you\'re going to run the Java doc tools to generate all of the documentation for all of the classes and stuff inside of it. That will then.

**\
Val Levitan** 1:56:18\
So, that\'s the attachment that you put in the chat, right? That\'s\...

**\
Aaron Bockelie** 1:56:23\
Yeah, like there\'s, yeah, it depends on the language, right?

**\
Val Levitan** 1:56:27\
So depending on the language, this is how you back into the contract.

**\
Aaron Bockelie** 1:56:32\
This is how you publish the current copy of it.

**\
Val Levitan** 1:56:32\
Let me, let me.\
Let me ask them in Russian.\
Um\...\
Evgeny, we are not sure the that data contract.\
On.

**\
Evgeny Kharetski** 1:56:54\
It\'s just such as Panet. No, yeah, I had to because that\'s to touch to my personal meeting. If see, no, yes, yes, document by at the integration repository, no.

**\
Val Levitan** 1:57:15\
You, you, you, Evgeny.

**\
Evgeny Kharetski** 1:57:18\
Yeah.

**\
Val Levitan** 1:57:35\
But one to me, that\'s a no.\
Yalmo, go to at the night of Toshi.

**\
Evgeny Kharetski** 1:57:59\
Okay.\
Okay.

**\
Val Levitan** 1:58:03\
Whatever, whatever, yes, put mushroom.

**\
Evgeny Kharetski** 1:58:09\
Very well listener.

**\
Val Levitan** 1:58:10\
Yours dominion will know it.\
At the.\
What?\
Miller, my company.

**\
Evgeny Kharetski** 1:58:38\
Like, touch them.

**\
Val Levitan** 1:58:40\
What?\
What?

**\
Alexander Biratko** 1:58:48\
The.\
I need data contractor.

**\
Val Levitan** 1:59:30\
Yeah.

**\
Alexander Biratko** 1:59:36\
No, Tsimanov meeting to is the creator, the repository.\
It was mostly besides code bull.

**\
Val Levitan** 1:59:59\
Yeah, yeah.\
In Abaro, she mentioned clothes night.\
Yeah.\
Yeah.

**\
Evgeny Kharetski** 2:00:28\
No, like that.\
No taste.

**\
Andrei Bosik** 2:00:34\
Best thing.

**\
Evgeny Kharetski** 2:00:36\
Test it.

**\
Val Levitan** 2:00:44\
Yeah, yeah, the product.

**\
Evgeny Kharetski** 2:00:53\
2.\
Ну.

**\
Alexander Biratko** 2:00:57\
Ну просто просто интегришн репозитории принимают другой, так сказать, функционал или чтото такое другое.

**\
Evgeny Kharetski** 2:01:04\
Да то есть мы. Я хочу сказать, что мы изначально.

**\
Val Levitan** 2:01:07\
Да я не верю что я не верю что должен быть интеграшен репозиторой.

**\
Alexander Biratko** 2:01:12\
А где будут диплом и всякие скрипты? Общие общий холстек, например.

**\
Val Levitan** 2:01:21\
Fir seconder tink senting ene wat?\
Sentine in wonit to jumpin to son fones s.\
Doployment and intergration, repsettor IT collet, intergration, repository, downd, intergratson, repestiotory.\
Еду.

**\
Aaron Bockelie** 2:01:48\
Час.

**\
Val Levitan** 2:01:48\
Окей, энд.\
Does the work?

**\
Andrei Bosik** 2:01:56\
And what contains this repository? They do not contain data contracts.\
Data contract store in.

**\
Aaron Bockelie** 2:02:02\
Mm.

**\
Andrei Bosik** 2:02:06\
Repository with code with product, but what store integration repository?\
Deployment.

**\
Aaron Bockelie** 2:02:16\
I think the integration it has the deployment the the.

**\
Andrei Bosik** 2:02:19\
Integration tests.

**\
Aaron Bockelie** 2:02:20\
Right, it has the deployment architecture, whatever it might be, if it\'s if it\'s a Docker compose, if it\'s a\...\
Uh, what I forget which, what do you use for steering Kubernetes?

**\
Andrei Bosik** 2:02:35\
Yeah, I can chat.

**\
Aaron Bockelie** 2:02:37\
Yeah, so you have Helm charts, those would be inside of there.\
and so forth.\
So, Elm chart, integration tests to invoke things. Sometimes integration tests just invoke tests inside of the other modules too.\
Depends on how it\'s set up.\
Probably where your monitoring stuff ends up as well. How do you set up monitoring? How do you build up the actual environment from it? Like if you have Terraform, right? If Terraform\'s in there and you\'re defining your infrastructure to begin with in that CI repository, that would probably be where that goes to.\
But it could be in a separate thing. This depends how complex your environment is.\
You should at any time be able to invoke all the tests in a in a dev environment from your CI repo. So, for instance\...\
Let\'s imagine you have the front end and the back end and it all works, okay?\
The front end has a bunch of React tests, TypeScript tests, something like that, right?\
You should be able to invoke all of the tests for TypeScript, which will go out with live API keys or credentials or whatever it takes to auth against the backend and invoke all of the tests and then verify that those things actually change. That\'s your integration test suite.\
And then you should be able to tear it all down afterwards, because you just contaminated the database with a bunch of test data or whatever it is, and just do it over and over. It should be idempotent is the phrase, is the word to use for when you\'re running CI tests. You should be able to just click it and let it run, and it does its thing over and over and over again.\
Again, if you want to.

**\
Val Levitan** 2:04:43\
Did you, did you understand, or or?

**\
Alexander Biratko** 2:04:49\
Understand.

**\
Andrei Bosik** 2:04:49\
I understand.

**\
Val Levitan** 2:04:49\
Andrei.

**\
Evgeny Kharetski** 2:04:49\
No, Lena.

**\
Val Levitan** 2:04:51\
Is it so it\'s clear now?

**\
Alexander Biratko** 2:04:54\
Yeah.

**\
Val Levitan** 2:04:55\
Okay, so Alexander.

**\
Alexander Biratko** 2:05:00\
No.

**\
Evgeny Kharetski** 2:05:05\
So, one point that should be\...

**\
Alexander Biratko** 2:05:22\
Не нужно, то у нас сужается, как бы наш интеграшенный позиторий он становится более специфичным, только в основном для интегришн тестов и дипломента.

**\
Evgeny Kharetski** 2:05:25\
Называется.\
Специфично.\
Для Того, чтобы.

**\
Alexander Biratko** 2:05:36\
А наши?

**\
Evgeny Kharetski** 2:05:37\
Наши.

**\
Alexander Biratko** 2:05:39\
Репозитории, то есть сервисные репозитории, они становятся чутьчуть шире, то есть там должно быть более грамотно описано.\
Дата контракты. Ну то есть если там нету, там опана пиари какого нибудь свайгера там надо его дописать.

**\
Evgeny Kharetski** 2:05:50\
Ну, то есть если там между там?\
15.

**\
Alexander Biratko** 2:05:56\
И чтобы это было легко получить этой этот IPI и ну и всё, да?

**\
Val Levitan** 2:06:05\
А сантигард.\
А сантисгард.\
На Андрей.\
То кто меня был?\
Допломен пайплан house nork.\
Йондостен тунка юбэшанс.

**\
Andrei Bosik** 2:06:32\
I say, how is this?\
And.

**\
Val Levitan** 2:06:37\
No, no, don\'t do that. Don\'t say how you see it.\
Say it, say it how I see it.\
I\'m just kidding. I\'m just kidding.

**\
Andrei Bosik** 2:06:47\
Okay.\
Ohh.\
In integration repository, we store deployment actions.\
to deploy.\
Release artifacts from.\
Repository with services.\
We, in integration repository, we have, for example, Docker compose file to run this environment on a developer machine.\
We have.\
Integration test documentation.\
Ohh.\
Maybe a Helm charts. I don\'t know. I need to think about this.\
And do we have in this repository a sec?\
I think, yes, we can have this. We can have some page, for example, or something else that show which version of each component is already deployed on our environment.\
Is that how I see?\
And using, I think.

**\
Val Levitan** 2:08:13\
Okay.\
Okay, Eugine.

**\
Evgeny Kharetski** 2:08:18\
No.

**\
Val Levitan** 2:08:19\
So tell me how will Claude?\
Sit there.\
And develop \*\*\*\* on its own.\
So, how is it going to work?

**\
Evgeny Kharetski** 2:08:35\
Um\...

**\
Val Levitan** 2:08:38\
And remember, every week or every month, cloth is becoming more and more potent.\
Nope.

**\
Evgeny Kharetski** 2:09:14\
To beer.\
А корона будет гораздо важнее в использовании, то есть ну это будет, можно сказать, основным инструментом с точки зрения Того, если нам нужно разрабатывать несколько частей.\
Одного и Того, ну то есть несколько сервисов разных, но они должны взаимодействовать друг с другом.\
Вот, соответственно, они должны обмениваться данными между собой о том, как.\
Они принимают данные или как они отправляют данные друг другу.\
Вот и в таком случае. Ну то есть я себе это вижу, так что, допустим, я разрабатываю. Ну то есть я вот разработчик мне приходит задачу, мне говорят, нужно сделать это, чтобы работало вот так.\
Я понимаю, что это затрагивает, скорее всего, ну там в обсуждениях с кодом, допустим, мы понимаем.\
Что это затронет там 3 сервиса?\
Вот соответственно, я говорю, давай разобьем.\
Сессии.\
Эти 3 сервиса и будем работать в них сообща. Вот так я себе это вижу через атент, соответственно, который был презентован я сейчас свой тестирую гоняю, ну пока что.\
Выглядит, что это очень полезная штука в таком.\
При таких сценариях использования.

**\
Val Levitan** 2:10:42\
Александр.\
То, что Евгений сказал, это вас?\
Вы с этим согласны ли? Он просто мне спиздел, потому что я ничего не понимаю.

**\
Alexander Biratko** 2:10:56\
Ну я не тестировала тент женя тестировал, пробовал. То есть в целом механизм рабочий, то есть тот клод, который.\
Находится в.\
Другом репозиторе и, например, мой клод, которым я сейчас активно пользуюсь, он может спрашивать, какой у тебя IP да получать от него?\
Насчёт Того, насколько это эффективно полезно, скорее всего, нужно будет отдельные вот эти плоды обучать или не обучать, но они должны быть экспертами в своём репозитории, и тогда это будет полезно, если они не будут экспертами. Тогда смысла нету, можно своему клоду сказать, иди посмотри, что там в репозитории.

**\
Evgeny Kharetski** 2:11:19\
Насчет Того, насколько это действительно полезно, скорее всего, нужно будет отдельно вот эти плоды обучать или не обучать, но они должны быть экспертами в своём реквизитории, и тогда это будет полезно, если они не будут экспертами. Тогда смысла нету к своему плоду сказать. Люди посмотрели, что там будет такое.

**\
Alexander Biratko** 2:11:37\
А если тот, если тот клод будет экспертом, то есть он будет больше знать о своём репозитории, то это будет полезно.

**\
Evgeny Kharetski** 2:11:39\
Плохо будет сфера там, то есть он больше значит своём какихто.\
Вот экспертом в сессии становятся, когда к нему загружается нужный контекст, а если ты его запускаешь в определённой папке, то он загружает тот контекст, который в этой папке, ну то есть квот м ди мемори для этого проекта и так далее.\
То есть, соответственно, всегда будет нужный контекст для нужной папки.

**\
Val Levitan** 2:12:05\
А вес нам много начнет своей. Вот ичмонов сэдбикоза говно фокена и dey what dan sergen.\
Интерпретс atw well bea.

**\
Aaron Bockelie** 2:12:14\
Да.

**\
Val Levitan** 2:12:20\
А бока борщ.\
А борщ.\
Борщ туба до насмерть борщ.

**\
Andrei Bosik** 2:12:31\
Иного ты сборщина ising amercan dona tiss sup.

**\
Val Levitan** 2:12:32\
Всё.\
Этой болезни.

**\
Aaron Bockelie** 2:12:35\
А больше рагерпороги злай.

**\
Val Levitan** 2:12:37\
Всё.\
Всё я выпарину.

**\
Aaron Bockelie** 2:12:39\
3.

**\
Andrei Bosik** 2:12:40\
Или что праздник?

**\
Aaron Bockelie** 2:12:41\
Э.

**\
Andrei Bosik** 2:12:41\
Окей.

**\
Val Levitan** 2:12:42\
Солбат айсэй майкадэл finel li red.

**\
Aaron Bockelie** 2:12:50\
Окей.

**\
Val Levitan** 2:12:50\
Ангон тупо до чан скрипт here.\
А вот лайт, который райт в ru.\
Wony rutvortion for.\
Sechlal all atow andrei andi.\
Евгений парк halk cload is goognet seder.\
Dold dork dat you you sto do you os goons.\
Лука clot anite you bosch.\
Эндув колл нахрен.\
Энд ю Андрей а вон читу адж инфорд to ploym met sechin.

**\
Andrei Bosik** 2:13:42\
А эл ради уже старт ворком пауза.

**\
Val Levitan** 2:13:43\
Freed day sorrd.\
Абраев абрагов, мире.\
Он чувствует toursty.

**\
Andrei Bosik** 2:14:00\
Четверг.

**\
Val Levitan** 2:14:01\
Уинстай.

**\
Andrei Bosik** 2:14:01\
В среду.\
Ту успешный среды.

**\
Evgeny Kharetski** 2:14:04\
Пока ты успеешь, а мы нет. Ну у нас же 24 выходных сейчас.

**\
Alexander Biratko** 2:14:07\
Я просто я в четверг скорее всего не смогу просто ну либо тогда фрайдэйж.

**\
Evgeny Kharetski** 2:14:11\
У нас же мы же выйдем в среду только на работу.

**\
Alexander Biratko** 2:14:14\
Угу ну.

**\
Val Levitan** 2:14:14\
А яс яс taty back free.\
Fredy fredy.\
Энд.\
А плиз.\
Surrkel ad docement befor ami becost eran isped reder.\
Ангетян вредит файв минетс.\
Sekel late yout your dan dackement fodi mery.\
Мид миллениун фрари.\
А его poder transcreporen intestate.

**\
Aaron Bockelie** 2:15:01\
Danoren andreid cance andreit canor somryste hold tan tangli penter thire inter there.

**\
Val Levitan** 2:15:14\
Пару ви фор в орж информ михал ю гоинг туэ дай.\
For ituse torey i won no to hi won to del live to da cance metrop porove your sony tory worsten to do ro cance free wors what banner?\
Энтэн инклура pared innat.\
Оп хауер ту кипоне двенсин тераканц вот стремко dvencein deer cancert.\
Ивона тейк not freeby watmanday.

**\
Andrei Bosik** 2:16:14\
how we type release number, version number. It\'s not easy questions when you, I start working with this.

**\
Val Levitan** 2:16:24\
So, one important thing for me\...\
Right now, the cycle of test, they have these bunch of tests that they\'re running, visual test for Michael Gottlieb, for Juan Martinez, for Lena.\
So that needs to be done, not the way it\'s done today.\
Because today it\'s a \*\*\*\*\*\*\* process.\
And that needs to be done on a fly.\
Battle.\
Clear by Nathan.\
It\'s a religious holiday coming up, right?

**\
Alexander Biratko** 2:17:14\
Near.

**\
Evgeny Kharetski** 2:17:14\
Yeah.

**\
Andrei Bosik** 2:17:14\
Mhm.

**\
Val Levitan** 2:17:15\
What are we doing? What\'s the tradition, religious tradition? What are we doing during this?

**\
Alexander Biratko** 2:17:21\
Naklabish.

**\
Evgeny Kharetski** 2:17:24\
Butch that.

**\
Val Levitan** 2:17:24\
But.

**\
Aaron Bockelie** 2:17:25\
What is it?

**\
Evgeny Kharetski** 2:17:26\
Not to.

**\
Val Levitan** 2:17:27\
Visit, visit cemeteries.

**\
Aaron Bockelie** 2:17:29\
Oh.\
Really? That\'s interesting.

**\
Andrei Bosik** 2:17:32\
Yeah, spring clear, spring clear in.

**\
Alexander Biratko** 2:17:33\
Yeah.

**\
Val Levitan** 2:17:38\
And what\'s the, you guys know the prayer?\
Do you pray?

**\
Andrei Bosik** 2:17:44\
Oh.

**\
Val Levitan** 2:17:45\
Sood.

**\
Aaron Bockelie** 2:17:45\
Do you visit, do you visit your relatives or do you do visit anywhere?

**\
Val Levitan** 2:17:49\
No, relatives.

**\
Aaron Bockelie** 2:17:50\
Okay.

**\
Val Levitan** 2:17:53\
But there\'s no prayer when when you\'re when you\'re at the cemetery, but\...

**\
Alexander Biratko** 2:17:53\
How do you?

**\
Andrei Bosik** 2:17:55\
No, I know.

**\
Evgeny Kharetski** 2:17:56\
Mm.\
Mhm.

**\
Alexander Biratko** 2:17:59\
Ohh.

**\
Andrei Bosik** 2:17:59\
No, I don\'t know.

**\
Val Levitan** 2:17:59\
But not, not you, not you, but normal people. Do they pray?

**\
Alexander Biratko** 2:18:01\
Yes.

**\
Andrei Bosik** 2:18:04\
I am normal people.

**\
Val Levitan** 2:18:05\
No, you are not normal.

**\
Andrei Bosik** 2:18:07\
Yeah.\
I am the best people in.

**\
Val Levitan** 2:18:11\
I didn\'t say you\'re not good, but you\'re not normal.

**\
Andrei Bosik** 2:18:12\
Yeah.\
Wow.

**\
Val Levitan** 2:18:15\
You don\'t pray, you\'re not normal. You gotta believe in God.

**\
Andrei Bosik** 2:18:16\
But.

**\
Alexander Biratko** 2:18:20\
Sometimes, yes.

**\
Val Levitan** 2:18:21\
You pray? Good for you. You should.\
It\'s good to believe in something more than money.\
All right, I love you all. No matter what Aaron says about you, you\'re a bunch of good people.

**\
Aaron Bockelie** 2:18:38\
Yeah.

**\
Val Levitan** 2:18:39\
Okay, have a good weekend.\
All right, thanks guys. I am exhausted from all of you. Like I am a victim in this. I want you to think I\'m a victim.

**\
Evgeny Kharetski** 2:18:42\
Let\'s see, man. Bye.

**\
Alexander Biratko** 2:18:42\
Bye. Bye.

**\
Andrei Bosik** 2:18:42\
Yes, thank you.

**\
Evgeny Kharetski** 2:18:51\
Yeah.

**\
Aaron Bockelie** 2:18:51\
Yeah.

**\
Val Levitan** 2:18:52\
You, you are abusing me.\
Goodbye.

**\
Aaron Bockelie** 2:18:56\
Learning sometimes hurts.

**\
Val Levitan** 2:18:58\
Oh, boy, it hurts. By.

**\
Evgeny Kharetski** 2:19:01\
BY.

**\
Aaron Bockelie** 2:19:01\
Why?

**\
Alexander Biratko** 2:19:02\
BY.

**\
Andrei Bosik** stopped transcription
