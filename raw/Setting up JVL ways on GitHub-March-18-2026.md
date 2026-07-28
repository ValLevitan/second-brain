**Setting up JVL ways on GitHub-20260318_081006-Meeting Recording**

18 March 2026, 12:10pm

48m 49s

**\
Val Levitan** started transcription

**\
Andrei Bosik** 0:03\
Uh, I I I say my uh things about this.\
Uh, OK uh.\
I can send.\
Link to our.\
Repository.

**\
Aaron Bockelie** 0:21\
The other thing that we\'ve got to to think about too.\
Is.\
There may be a better way to.\
Deploy it. The reason that the way I have shown you guys to do it is to create Cloud Code config as a repo in people\'s user profiles for people using Cloud Code.\
Is that uh?\
That is to force people to to to use it as they should, which is to potentially manage their own version or variant of it, and to version control their own.\
Branch of what they think Cloud Code config should be like.\
So let\'s imagine right now you\'re essentially deploying a prod branch to people\'s computers. OK, so you have a script that runs, it copies it into there.

**\
Andrei Bosik** 1:25\
Mhm.

**\
Aaron Bockelie** 1:29\
And then it\'s essentially cloning that repo locally on everybody\'s computer who\'s using it.

**\
Andrei Bosik** 1:35\
Mhm.

**\
Aaron Bockelie** 1:37\
Uh.\
The whole point of the tool is to give people a chance to have some amount of customization in their own project, in their own environment. That might mean anything from different memory settings to.\
Adding some additional ways for their team or something like that because essentially.\
Um.\
There\'s going to be differences in everybody\'s roles. Pavel using cloud code ways is not going to use it the same as, let\'s say, a theme.

**\
Andrei Bosik** 2:21\
Yeah, I understand. What do you mean? Uh, solution we can uh.\
Hello copies this repository to the personal profile in GitHub, incorporate GitHub and maybe they can copy.\
From their personal rep repository this conflicts.

**\
Aaron Bockelie** 2:48\
I think it\'s actually simpler than that because what you want to be able to do is get all the good ideas from JVL and roll them back into JVL specific ways. So you just let people have branches in cloud code ways internally on JVL. Just make sure you have a naming convention for it.\
And what you can then have is occasionally, maybe every couple months, maybe every month. I don\'t know how how often you want to review it. Maybe it\'s every day.\
You look at all of the different configs that have been pushed up to cloud code ways from the different people and you can then evaluate and incorporate them into the JV LS prod.

**\
Val Levitan** 3:32\
I just want to jump in here because I think it\'s important that I refocus Andrei on the gravity of this decision.\
Because I I think Andrei, although he\'s very, very smart, I don\'t think he realizes how important these decisions that we are making right now.\
Structural decisions for the future of the company.\
We intend to quickly evolve into using super intelligence.\
The Superintelligence in academic sense or in JVL sense?\
They\'re they\'re slightly different. I\'m not looking for super intelligence from an academic perspective, but from now on, everything that will be coming out in terms of intelligence.\
It will be much smarter than many of the people working for JVL.\
So you want to call it super intelligence, higher intelligence, good intelligence, reliable intelligence, whatever it is. And we will be embracing it and because we are going to be embracing it, developing our own ways of doing things.\
And.\
Taking the ownership of these ways and grooming them and promoting them.\
Ways. I\'m talking about ways, our ways and managing our own ways.\
Intelligently, with care, with love.\
Is important because it will make us as a company much smarter if we do it right.\
I\'m putting a lot of emphasis on.\
Incubating.\
And grooming and developing our ways.\
So.\
The branching repository structure, grooming structure, grooming hygiene of how we are going to do it. The discipline to develop this discipline to develop Andrei\'s way.\
Of grooming things it will.\
Elevate JVL to a higher level quickly and exponentially.\
Sorry, I jumped in.

**\
Aaron Bockelie** 6:20\
That\'s OK.\
So.\
Ultimately, what we\'re trying to do here is we\'re trying to change people\'s habits.\
Um.\
You are kind of at the steering wheel for this whole process right now because you\'re in control of the cloning of the continuous integration process for my repo. Oh, by the way, I did look at the other thing you pointed out yesterday and I stole some of the good stuff for it and put it into Waze.\
So we\'ll talk about that later. Um.

**\
Val Levitan** 6:52\
Who? Who? Who are you talking about?

**\
Aaron Bockelie** 6:54\
Andre, so remember yesterday, Andre at the our chat yesterday before we broke, you said, hey, what about this other one? I did some digging into it and it does have a good, had a couple good guidance things that I incorporated into new ways essentially. And that\'s what I want to do today is to just Val has a as a good.

**\
Val Levitan** 6:55\
Oh.

**\
Aaron Bockelie** 7:13\
Essentially an architectural way for JVL that I\'d like to build into ways, but.\
I wish I had a whiteboard right now to draw this to you, Andre, just so we could be clear.

**\
Val Levitan** 7:28\
Yeah, enjoy it. Why not share your screen images?

**\
Aaron Bockelie** 7:30\
Well, I need a drawing tool. Does anybody have one?

**\
Val Levitan** 7:34\
Well, use. Uh, you love. You love that tool. What do you call it?

**\
Aaron Bockelie** 7:37\
I don\'t have Miro.

**\
Val Levitan** 7:39\
Oh, good.

**\
Aaron Bockelie** 7:40\
Not anymore.\
Let\'s see. Maybe there\'s a thing in here.

**\
Val Levitan** 7:46\
Confluence.

**\
Aaron Bockelie** 7:49\
Do you want to set up a confluence page, Andre and I\'ll draw it.

**\**
7:54\
Why not?

**\
Aaron Bockelie** 7:56\
Send me the link.

**\
Andrei Bosik** 7:58\
One second.

**\
Aaron Bockelie** 8:21\
Mm.

**\
Andrei Bosik** 8:45\
Send in chat.

**\
Aaron Bockelie** 8:49\
OK.\
Great. So let\'s see here.\
So there\'s my repo.\
And then we\'ll have.

**\
Val Levitan** 9:17\
Are you sharing your screen?

**\
Aaron Bockelie** 9:18\
No, just open it up. We don\'t have to share the screen. You guys should all be able to participate at the same time.

**\
Val Levitan** 9:22\
Oh, OK. Oh, yeah, yeah, yeah, I see it.

**\
Aaron Bockelie** 9:27\
So then we have um.\
See here, we\'ll do that, hold that main.\
Here, Andre, make your make your pipeline.\
OK.

**\
Andrei Bosik** 9:50\
Mhm.

**\
Aaron Bockelie** 10:04\
This is mine over here. The green one. Yours is over here. Let\'s make yours blue.

**\
Andrei Bosik** 10:09\
Yeah, OK.\
Right.

**\
Aaron Bockelie** 11:15\
OK, so this is a main from here, so let\'s draw that line in there.

**\
Andrei Bosik** 11:27\
I think my main.

**\
Aaron Bockelie** 11:30\
Well, your main should be the same as mine, right?

**\
Andrei Bosik** 11:31\
Go to your main. We need to change arrow.

**\
Aaron Bockelie** 11:37\
It\'s flowing down. Let\'s let\'s take the process of flowing down. So it comes from mine, gets published into my main. It then flows into your main, yeah.

**\
Andrei Bosik** 11:39\
Uh, OK.\
And I think we can.

**\
Aaron Bockelie** 12:36\
What we\'ll do is we\'ll call this one, uh, Val.

**\
Andrei Bosik** 12:42\
Well, for example, each user can create branch in this repository, for example me or.

**\
Aaron Bockelie** 12:47\
Yeah.\
Yeah, so we\'re calling this branch Val, we\'re calling this branch Andre and so forth. But then what we don\'t want to have is main because that directly copies from there. So what we\'re going to have here instead is rod.\
OK.

**\
Andrei Bosik** 13:05\
Um.

**\
Aaron Bockelie** 13:06\
So prod. So you\'re gonna. So basically, oops, you\'re gonna take this.

**\
Andrei Bosik** 13:08\
Yes.\
No.

**\
Aaron Bockelie** 13:13\
You\'re going to go like this.\
Main gets to rod, right?

**\
Andrei Bosik** 13:20\
Yes.

**\
Aaron Bockelie** 13:21\
Or actually what we might do is we might have a stage.

**\
Andrei Bosik** 13:23\
Oh.

**\
Aaron Bockelie** 13:28\
Let\'s do.\
Stage rod.\
And then we also have a another branch called JVL and JVL sits around around with the other people too. And that\'s about what that\'s what we\'re about to commit to today is JVL.\
So what happened is, is that JVL goes into stage and this is stage is an integration point and then we optionally pull Val into stage at times if we see something cool.\
Or we let\'s make a different shape here.\
So what we have here is a little different on JVL. JVL is reserved and special because it\'s known intentional things that we want. The other possible flow that we have here, let\'s put this over here.\
I\'m just trying to work it out as we as we go here, right?\
As we do a pull request into.\
JVL This kind of feels better to me and if I\'m being honest.

**\
Andrei Bosik** 15:26\
I have questions. Personal branch live forever or no? Because for example I create ways that use only me.

**\
Aaron Bockelie** 15:29\
Sure.\
M.\
I think that they can.\
So, so Waze is designed to be able to accommodate lots of different domains of problems, right?\
That\'s why we have a stage direction here, and JVL might have its own stage, right? So we have a we we might we might throw things under.\
Let\'s do this.\
We\'ll just do test.\
UA.\
Is as soon as you guys start integrating a lot of people, the whole flow gets complex and that\'s just how it is.\
We don\'t want to inadvertently break people\'s stuff.\
O here, let\'s let\'s walk through this right now.\
Git pull comes into main for mine. It\'s essentially a clone, right?

**\
Andrei Bosik** 16:44\
Yes.

**\
Aaron Bockelie** 16:45\
Then what we do is we have a JVL branch which is not actually part of the main, but just just ways for JVL. So just like some new ways directories, that kind of thing.\
That\'s the diff. Um.\
What we then typically do over and over is we integrate on merge. So I don\'t know if we want to have tests in QA every single time, but we should have auto tests.\
So.

**\
Andrei Bosik** 17:22\
How we can test ways it\'s.

**\
Aaron Bockelie** 17:25\
There\'s tests built into it right now. You\'re going to see it get tested in just a minute. You\'ll have to, you\'ll have to build the test to be more complex for JVL\'s environment, but that\'s fine. So what we\'re doing here is.\
We take JVL\'s specific ways. We try to integrate on merge from JVL. JVL has just ways but not the code and then we we pass this the scoring.\
And we move it to stage and then from stage you get to promote it to prod and as soon as it\'s promoted to prod you get your script to pull to PC because what you don\'t want to have is a situation where over here.\
Andre, you create a thing. You like it. It works well for you because you have your world view of it. You make a pull request, it moves into JVL, and if it publishes directly into prod and onto people\'s computers, and then suddenly all of the steering is \*\*\*\*\*\*\* broken and everybody\'s computer thinks.\
That they\'re just Andre because you scored it incorrectly and it doesn\'t hit correctly. That\'s a problem. So we need to protect the flow and instead take the test scoring metric to make sure it works.

**\
Andrei Bosik** 18:45\
What difference between uh stage and test key?

**\
Aaron Bockelie** 18:51\
Well, test QA is auto.

**\
Andrei Bosik** 18:52\
After scoring test, so I see, I see OK.\
But maybe we can use this test in stage.

**\
Aaron Bockelie** 19:02\
And then in stage you have a few people that you trust. We\'ll Utah this over here.\
Trusted users who can spot poor performance.

**\
Andrei Bosik** 19:25\
Mhm.

**\
Aaron Bockelie** 19:26\
You need to have a small group of people who understand how Waze works. If you\'re the only person who knows how Waze works, none of this is going to work.

**\
Val Levitan** 19:36\
No, we have Dima who is who is quite good.

**\
Aaron Bockelie** 19:41\
Right, so this is where you have.

**\
Val Levitan** 19:42\
The the only.

**\
Andrei Bosik** 19:43\
And Jenny, that is good too.

**\
Val Levitan** 19:45\
Well, no, no, no. But but in in the IT department we have Dima. The only problem with Dima is that he doesn\'t really want to learn things, but otherwise he\'s OK.

**\
Andrei Bosik** 19:50\
Um.

**\
Aaron Bockelie** 19:55\
Well, Dima\'s not a good person to do this because he\'s not using cloud code for writing code on a daily basis.

**\
Val Levitan** 20:00\
That\'s that\'s true. That\'s true. That\'s true. That\'s true.\
So.\
So Haretsky is very good.

**\
Aaron Bockelie** 20:15\
Sure.

**\
Val Levitan** 20:16\
Let\'s deploy him.

**\
Andrei Bosik** 20:17\
Yeah.

**\
Aaron Bockelie** 20:19\
O you need a couple of people there.\
We\'re just going to call it trusted users who can spot oor erformance because we\'ve already gone through the the scoring metric rocess of of integration.\
Once you get some feedback from this, you can just release from stage to rod and then everybody gets this copy.\
Including Heretsky or whoever is subscribed to the stage, essentially.\
Because what\'s gonna happen is, is that stage is gonna be OK. It\'s gonna basically be an open Jira or a open GitHub issue for a while while we\'re testing stage. And then at some point everybody goes, yeah, I didn\'t notice any difference or or actually it\'s improved or whatever positive.\
Neutral to positive sentiment that you get and then as soon as you start to hear that, then Andre pushes the release button. It goes to prod. This person gets the prod copy as well because it just updates. They can always just manage override and update here.\
And then everybody else gets the roduction version of it.\
Um.\
Finally, let\'s put this over here in the flow to make it make sense.\
O This is the full loo, right?\
See how we have.

**\
Val Levitan** 22:02\
Uh.

**\
Andrei Bosik** 22:05\
What do integration on match between GL diff and test EA?

**\
Aaron Bockelie** 22:13\
So JVL branch isn\'t gonna carry anything other than the.\
Waze files themselves.

**\
Andrei Bosik** 22:24\
Not my questions. What do uh?\
Somebody doing on integration merge or no or it\'s just notification.

**\
Aaron Bockelie** 22:37\
Yeah, it\'s automatic. You\'re going to merge this stuff over. You\'re going to do a diff merge into main. So let\'s talk about what that looks like for a minute.\
Oh.\
Let\'s put this over here. Oops.\
These are probably too big. Let me shrink these a little bit. There we go.\
So do you see how what we\'re doing is we\'re collecting all of the fully functional ways in main and then in the JVL branch we\'ve only got a specific way for JVL and a specific JVL agent. And then basically what happens is.\
Over in stage.\
This becomes merged O we have. Let\'s just make this light teal. I don\'t think I can make two separate colors.\
And I No, that sucks. Thanks a lot here.\
OK, anyway, So what we\'re doing then is this merge that happens.\
Merges everything into stage, so so stage is the combination of everything from main and everything from JVL.\
We\'ll put it here instead.\
You see the difference?

**\
Andrei Bosik** 25:32\
Mhm.\
Yeah.

**\
Aaron Bockelie** 26:15\
So here\'s your kind of flow, right? A little built out a little more. So you\'re going to have otentially emerge conflicts, so you have to do manual resolution.

**\
Andrei Bosik** 26:24\
Mhm.

**\
Aaron Bockelie** 26:26\
So forth.\
Technically, it\'s this.\
Right, because a merge conflict means that you would just go back and fix your JVL branch until it works.

**\
Andrei Bosik** 26:53\
Mm-hmm. Yeah, I understand.

**\
Aaron Bockelie** 27:21\
So the fun part is, is you could probably share this diagram with cloud code in your environment and then start building out essentially this in your in your space.

**\
Andrei Bosik** 27:29\
OK.\
Is it exactly what I do? Yeah, I share this link to Claude and speak about, speak with him about this and integrate this to our repository and our infrastructure.

**\
Aaron Bockelie** 27:44\
Yeah.\
Yep.

**\
Andrei Bosik** 28:00\
OK.\
Oakley.

**\
Aaron Bockelie** 28:06\
So let\'s uh.\
Let\'s push, let\'s let\'s push forward into actually creating the way that Val was talking about yesterday.\
And I want you to share your screen with your Waze environment. And what we\'re going to do is we\'re going to practice the first piece of that flow that we just diagrammed just now by you\'re going to have an Andre branch in Cloud Code Waze on inside of JVL.\
OK.

**\
Andrei Bosik** 28:38\
OK.

**\
Aaron Bockelie** 28:41\
O I\'m going to share the prompt and the text that we\'ve got to do, and then you\'ll see how this works.\
So if you when you open up cloud code and.

**\
Val Levitan** 29:20\
Yes.

**\
Aaron Bockelie** 30:03\
OK. So Val, do you want to share that document from yesterday that you shared with me?

**\
Val Levitan** 30:11\
Yeah.\
Uh.\
We have to.

**\
Aaron Bockelie** 30:21\
What you did do Andre is change into the dot cloud directory where you have that repo on main in there.

**\**
30:31\
Mhm.

**\
Andrei Bosik** 30:38\
Main uh where place it uh code code configs.

**\
Aaron Bockelie** 30:44\
Yeah, wherever you, you know it\'s usually dot cloud, right? So that\'s and that\'s a git repo right now. It should be.

**\
Andrei Bosik** 30:47\
Yes, yes.\
Uh, yes, uh, get for example.

**\
Aaron Bockelie** 30:53\
OK.\
All right.

**\
Andrei Bosik** 30:58\
But I not in main I create another branch to.

**\
Aaron Bockelie** 31:02\
Well, no, let Claude do it.

**\
Andrei Bosik** 31:07\
It\'s to it.\
But.

**\
Aaron Bockelie** 31:10\
O Here\'s the first. Here\'s the prompt.\
And you\'re going to paste that into cloud code. I want you to read it and understand why I\'ve written it that way. And then without pressing enter, you\'re going to take all the text from Val\'s document that he\'s got, and you\'re going to paste that afterwards. So the whole thing is your prompt.

**\
Andrei Bosik** 31:28\
Mm-hmm. OK.

**\
Aaron Bockelie** 31:31\
O Val, if you could share that.

**\
Val Levitan** 31:32\
One second please.\
So the documents that you are referring to, Aaron, are the documents that I shared with you, right?

**\
Aaron Bockelie** 31:46\
Yeah.\
It was, uh, let me find it here.\
Prompt Senior Developer Architect.

**\
Val Levitan** 32:46\
Got it.

**\
Andrei Bosik** 32:46\
Mm-hmm. Yeah, yeah.

**\
Aaron Bockelie** 32:47\
OK, so Andre, open that file U just read through it.

**\
Val Levitan** 32:49\
Aaron, please, Aaron, it\'s so important. Please take a look around that we\'re using the right prompt.

**\
Aaron Bockelie** 32:54\
Yeah, that\'s the right. This is the same prompt we used yesterday, and that\'s the same file that we had yesterday.

**\
Andrei Bosik** 33:00\
It\'s a very big file.

**\
Aaron Bockelie** 33:04\
It\'s not that big, it\'s just text.

**\
Val Levitan** 33:06\
It\'s uh, it\'s dot MD. It\'s dot MD.

**\
Andrei Bosik** 33:07\
Oh, you see?

**\
Aaron Bockelie** 33:10\
Don\'t do it that way. I want you to paste the actual text into it. Just open the document copy.\
Paste.\
There we go.\
O What\'s going to happen here is it\'s going to open a branch.\
And it\'s going to decompose the intentions of this.

**\
Val Levitan** 33:38\
Yeah.

**\
Aaron Bockelie** 33:38\
Of this prompt that Val has built.\
Uh oh.\
Overloaded API endoints this morning.

**\
Val Levitan** 34:20\
Yeah.

**\
Aaron Bockelie** 34:33\
There are errors this morning with Opus.\
So we we may not be able to fully complete this. We\'ll see. I\'m actually able to do it, or Opus is working for me right now at least.

**\
Andrei Bosik** 35:26\
Sometimes, uh, I work uh.\
In different location, for example in Canada, not work in Europe work.

**\
Aaron Bockelie** 35:40\
Yeah.

**\
Andrei Bosik** 35:43\
Maybe in your location work and now location location not work.

**\
Aaron Bockelie** 35:48\
Yeah, the problem is, is that you need to be doing it as your as your account on your machine and everything else rather than me doing it.\
Sometimes I will exit and then open it again.

**\
Andrei Bosik** 36:29\
Yeah, yeah, yeah.

**\
Aaron Bockelie** 36:38\
Yeah, now mine\'s breaking too, so it\'s just global.\
It\'s very slow right now for me.\
Let\'s hoping this would be working this morning.\
Make sure don\'t just start a new session, I would just resume the existing one.

**\
Andrei Bosik** 37:24\
Mhm.

**\
Val Levitan** 37:30\
OK.

**\
Andrei Bosik** 38:09\
OK.

**\
Aaron Bockelie** 38:10\
Mm-hmm.\
Overloaded.\
Do you know which API endpoint you\'re connected to? You\'re on cloud, you\'re the enterprise cloud subscription you guys have.

**\
Andrei Bosik** 38:27\
I don\'t know how I can find this information which I use.

**\
Aaron Bockelie** 38:33\
It\'d be in your cloud terminal stuff in or in the in the administration website.

**\
Andrei Bosik** 38:43\
Do you sync or OK, one second I open.\
This is all what we have in administration.\
Oh.\
I must think maybe in personal.

**\
Aaron Bockelie** 39:12\
I think it\'s usually console dot dot anthropic dot something. Let me.\
Here.\
Consolecloudcom is usually what it is.

**\
Andrei Bosik** 39:30\
Yeah.

**\
Aaron Bockelie** 39:30\
So whatever is happening, it might be resolving because my stuff\'s moving faster again now too.

**\
Val Levitan** 40:07\
A.

**\
Andrei Bosik** 40:10\
I try change my location.

**\
Aaron Bockelie** 40:48\
Well, we can also come back to this later. You have the prompt now.\
I just, I don\'t know if Val, are you able to confirm that you can use because you\'re in a different part of the world?

**\
Val Levitan** 41:03\
Log.

**\
Aaron Bockelie** 41:04\
Yeah.

**\
Val Levitan** 41:06\
It doesn\'t matter whether I\'m able. I mean, I was able to do it this morning, but if Andrei is not able to, let\'s just not push it and he\'s got quite a bit of organization to do. Let him let him organize it.

**\
Aaron Bockelie** 41:19\
OK.\
Yeah.

**\
Val Levitan** 41:21\
And then we\'ll come back to it tomorrow. Why burn time on it?

**\
Aaron Bockelie** 41:24\
Sure. We were just kind of hoping that maybe it would work, but.\
All right, well, let\'s wrap this then right now, because there\'s nothing we\'re at a blocking point until this works.

**\
Val Levitan** 41:35\
Andrei, do you know how to proceed? I don\'t want you to get stuck.

**\
Andrei Bosik** 41:38\
Uh.

**\
Aaron Bockelie** 41:39\
I would like to guide Andre through this. I mean Andre if you want to, but if you think you\'ve got it, but we have to.

**\
Val Levitan** 41:45\
Well, let\'s let\'s let\'s give it a shot. Let\'s go for it. Let\'s give it a shot.\
Let\'s spend another 5-10 minutes on that then if it doesn\'t work with it, with it.

**\
Aaron Bockelie** 41:59\
Why don\'t you do? Let\'s do this.\
Just so it\'s in the JVL ecosystem correctly, we could have Val run it because he might be making some ways as well.

**\
Andrei Bosik** 42:05\
Oh.\
I try to change my external I think from Europe to Canada and to America and nothing to work.

**\
Aaron Bockelie** 42:40\
OK, yeah, yeah.

**\
Val Levitan** 42:45\
Why don\'t you? Why don\'t you restart your cloud?

**\
Aaron Bockelie** 42:46\
Probably just the account.

**\
Andrei Bosik** 42:50\
Uh, I already restart.

**\
Aaron Bockelie** 42:52\
Yeah.

**\
Andrei Bosik** 42:53\
After uh, change API, I restart was sure.

**\
Val Levitan** 42:59\
OK.

**\
Andrei Bosik** 43:01\
Nothing work.

**\
Val Levitan** 43:11\
Our club is experiencing crazy growth there, so.

**\
Aaron Bockelie** 43:13\
Yeah.\
The state instead of resuming the session, which might have certain things.\
Just start a new session and just say hello and see if it even comes back.\
Say hello.\
Hit enter.

**\
Andrei Bosik** 44:36\
Interesting. Just to program.

**\
Aaron Bockelie** 44:38\
Yeah, let\'s just pause for now. We\'ll come back to this.

**\
Val Levitan** 44:44\
Let\'s organize, uh, GitHub.\
We can do it manually.

**\
Andrei Bosik** 44:49\
This service work.

**\
Aaron Bockelie** 44:53\
So you could click the code button in desktop and try it.

**\
Val Levitan** 44:54\
Oh, you.

**\
Aaron Bockelie** 44:58\
You don\'t have to use terminal.

**\
Andrei Bosik** 45:00\
Uh.

**\
Aaron Bockelie** 45:02\
Click on code.

**\
Andrei Bosik** 45:04\
Here it\'s a nice environment. Cloud desktop work on Windows. Cloud code CLI work in my VS Ubuntu.

**\
Aaron Bockelie** 45:05\
Yeah.\
No, you can open a local folder.\
OK.\
Yeah, you\'re gonna have to wait. We can\'t simulate this.

**\
Val Levitan** 47:15\
Well, can we can we proceed with setting up GitHub manually?

**\
Aaron Bockelie** 47:16\
O.\
Yeah, I mean if we want to click through all the stuff.

**\
Val Levitan** 47:29\
All right. OK. OK. So I think that we exhausted today\'s meeting. Let\'s just park it and have another meeting for tomorrow.

**\
Aaron Bockelie** 47:29\
It\'s up to you, Andrei.

**\
Val Levitan** 47:41\
Is that OK with you, Andre?\
Yes, yes, sure.\
If Claude comes back later today and you\'re able to proceed, then finish as much as you can and then tomorrow the meeting will be shorter and more efficient.

**\
Andrei Bosik** 47:52\
Hmm.

**\
Aaron Bockelie** 47:55\
Yeah, well, we\'ll have the prompt ready. Just save the as a text file for now and we\'ll go through it.

**\
Andrei Bosik** 47:55\
OK.

**\
Val Levitan** 48:01\
OK. Thank you very much. This was very useful. Oh, one second. Can you please circulate the link to the drawing that you formatted in this chat before we depart? Yeah, because I want.

**\
Andrei Bosik** 48:17\
Mhm.

**\
Val Levitan** 48:18\
Yeah.

**\
Andrei Bosik** 48:20\
OK.

**\
Val Levitan** 48:22\
It\'s just put put the link inside the chat please and thank you.

**\
Andrei Bosik** 48:22\
Mm.\
Link to uh space uh whiteboard.

**\
Val Levitan** 48:33\
Yes, please. Yes.

**\
Aaron Bockelie** 48:33\
Yes.

**\
Andrei Bosik** 48:34\
Uh, this link is already in chat, but I can send again again.

**\
Val Levitan** 48:39\
Is it in chat? OK, OK, so OK. Thank you very much. Bye guys.

**\
Andrei Bosik** 48:41\
Yeah, yeah, yeah.

**\
Aaron Bockelie** 48:41\
Yeah.\
Thanks. Bye.

**\
Andrei Bosik** 48:47\
Yeah, bye.

**\
Andrei Bosik** stopped transcription
