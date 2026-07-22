**application of GitHub for graphic design team-20251120_090505-Meeting Recording**

20 November 2025, 02:05pm

26m 14s

**Val Levitan** started transcription

**Val Levitan** 0:04  
He's consulting to.  
Yeah, to.  
JBL on a number of the subjects. He is an extraordinary individual, extraordinary.  
A wealth of knowledge on on a number of subjects comes with a lot of experience he works for.  
Aside from JVL key consults for less provenant companies like Ford, Nestle, IBM, Goldman Sachs.

**Aaron Bockelie** 0:39  
IBM.

**Val Levitan** 0:44  
To name a few, they're not as good as JVL, but it's OK.

**Sergey Kleimenychev** 0:48  
Some some casual garage companies.

**Andrei Bosik** 0:49  
Some casual, various companies.

**Aaron Bockelie** 0:51  
Deville has more charisma.

**Val Levitan** 0:51  
Aaron Sergey is.  
Design generalist, meaning that he is a little bit of a programmer, a little bit of a designer, a little bit of a of a nut case, but basically he fits very well into JVL culture.  
So one of the subjects and and the reason I brought Andrei to this because Andrei and Sergey actually sit next next offices.  
Basically they share a wall together, but.  
While they share a very, very thin wall, they share a very, very huge gap in communication. They don't talk to each other, then they don't like each other, they don't respect each other.  
They do not like to get into one room with each other. And so the fact that Andrei already know knows all the answers to these questions, Sergey totally ignores them because he doesn't believe that Andrei knows anything.  
So for that reason, all the way from Kansas City.  
Here's Aaron, who's going to discuss the subjects that Andrei already knows very well, and you and him could discuss it in your own time. But maybe now, with Aaron helping you out.  
You will build some trust to Andrei and next time you will go directly to him.  
OK, Sergey, so the question you asked me, you said that using GitHub might be good for the developers, but it's not good for.

**Sergey Kleimenychev** 2:46  
Oh, it is good for the developers.

**Val Levitan** 2:49  
OK, doesn't matter because you're not a developer, so not important. Whether it's good or not good, you said it could be acceptable for the developers. Go and kill yourself, do whatever you want with the developers. But as far as the graphic designers are concerned, it's ***** ** **** and you don't want to use it because it takes a lot of of your time.

**Sergey Kleimenychev** 2:53  
it. T

**Val Levitan** 3:09  
And we're just wasting your time rather than making you productive and making you.  
Use your energy on something useful. So I'm putting you in front of Andrei, who knows the subject and has tested it himself, and Aaron, who is able to answer all your questions. So now after this tedious introduction specifically.  
So my A I could record all of my beef with you and so I could stick it, stick it to you in about half a year in writing based based on the A I recording. Now go go ahead and discuss this with Aaron.

**Aaron Bockelie** 3:38  
So.

**Sergey Kleimenychev** 3:46  
On the body.

**Val Levitan** 3:51  
All you want, we only we only have 22 minutes.

**Sergey Kleimenychev** 3:56  
Yeah, OK.  
Put it in perspective, the world just is somewhat there, but there are nuances. My personal beef with Git in this particular case was because Git requires to use Git LFS, which is a basically.  
A duct tape solution over the git, which wasn't intended in the 1st place originally, and in my personal opinion for us as artists, it wouldn't solve any particular issues like we have our workflow.  
Uh, and when you change your tools, you're either, uh, getting some new.  
Fancy things that help you. You streamline your processes or it serves some other purpose. I'm not aware of any other purposes that Git would serve for artists other than streamlining the pipeline, and in our case it actually does.  
Quite the opposite, because while people use SVN, it's like it's a dump and easy. It's easy, but it's integrated SVN and everyone can use it. Everyone knows how to use it. It takes like a little space in our little part of our brain just to use it and to do it. It doesn't.  
Uh, add any anxiety, any complexity and other stuff. Git does. It's not that Git is a bad tool, it's just that it's a complex tool.  
If I was choose, I would not change anything for our test. I would use SVN. Since we are already in it, there's no point in rolling back like we're in a position where when we're better off fixing.  
Existing issues and streamlining the Git usage. And for that I think we should do a couple adjustments to the process just to make artists lives easier because well, I do use Git also at home in my personal projects and I do know how it works.  
I did break it a couple of times. I had to fix it. I had to get my hands dirty and understand how it works. The others don't and they shouldn't.  
As far as I can tell, like for them it should be just a couple clicks and everything works. Nothing more, nothing less.  
I can get to proposals if everyone is anyone is interested.

**Val Levitan** 6:16  
OK.

**Aaron Bockelie** 6:19  
So what do you what?  
Let me start by saying.  
It will be the code repo of choice for most of the game work.  
Git LFS is the current closest to the metal approach related to Git that we have that store large asset files and things like that.  
Um.  
I am not opposed to something else that can work with Git and uses Git LFS as a matter of convenience, a layer on top of abstraction for artists to use. So is that kind of the direction you're thinking? I'd like to.  
It like so to share with what you're thinking.

**Sergey Kleimenychev** 7:08  
I I never used anything on top of it, but I personally use minor alias scripts and stuff that helps me forget about stuff. Like if anything takes three or four steps and I do it regularly, I'll try to hide it. Like I do one command, it does all for me. I I have no chance of forgetting anything.  
Because like for example, Git LFS install is a mandatory stuff for every of your repos that you clone. Because if you don't do it, you don't have hooks. It suddenly pulls in only BLOB pointers, but not the blobs themselves. And if I know how it works, artists don't. They will panic. They will, they will not understand what just had happened.

**Aaron Bockelie** 7:40  
Right.

**Sergey Kleimenychev** 7:46  
Have to go and help them. So to mitigate this stuff I would basically divide this stuff into onboarding part which requires to set up anything you need for Git including aliases and then just use them so that people can do an easy clone and never think about it.  
The other issue is like in my personal experience, I had a case when I did a stash and then I have unstashed it and the git LFS didn't fire up, so I had pointers at that point. This stuff also should be just in case explained for people because.  
It's just a question of time when someone will stash accidentally his stuff and won't be able to retrieve it, and it's generally a work in progress which no one wants to lose.  
So I would go at least this way to make it easier. And the last proposal I would do is I would recommend to use squash mergers because nobody needs this long heavy tree of mergers with a history that's not needed by any one of artists. I will just squash it, have it tidy.  
Nice streamlined git history that doesn't bother us with a bunch of details. Plus we have an ability to lose the stuff over time with hoofing mechanisms and remove big blobs that are also carried in with the long tree because if we do daily renders and we push them in, it's about.  
GB of data per person each day, which is in my opinion too much.

**Aaron Bockelie** 9:10  
Yep.  
Yeah. So I mean, if I were to kind of summarize what you're actually saying here, the way I hear it is we should be using Git, we should be using LFS, but we should be modifying the way we actually use it.

**Sergey Kleimenychev** 9:30  
At this point, yes, because there's no point in rolling back. The decision was already made.

**Aaron Bockelie** 9:30  
That.  
Yeah.  
Right.  
So, so I think The thing is, is that I want to think about how I I know this exists. I know that the artists and the and the people who are committing work don't understand git very well right now.  
They're using these things very naively and they basically just do minimally and minimally think about it.

**Sergey Kleimenychev** 10:03  
Basically follow the steps, which is, in my opinion, a bit of a problem.

**Aaron Bockelie** 10:04  
Right.  
They they follow the steps and they're not thinking why they're following the steps.

**Sergey Kleimenychev** 10:10  
Yeah, more more importantly, they don't understand the consequences of any of those steps.

**Aaron Bockelie** 10:15  
So so perhaps what we need to be doing is we need to be thinking what experience, what user interaction experience are they having with Git and with their tool chain? Are they just working in VS code? Are they trying to just do it on the terminal on the command line for Git?  
Commands. Are they installing the git plugin for Windows where you right click on stuff and you can kind of just manipulate it there? Are they using a GitHub desktop application? For example, GitHub desktop is actually quite nice and can help.  
With that, and then Andrei probably can start help by enhancing the repos with some hooks, with some with some ability to to block certain types of commits and to otherwise make it more intelligent.  
To work with the tools to give some people some guidelines and some senses.

**Sergey Kleimenychev** 11:12  
And we already have VS code as our environment to do this stuff. I don't use it, I use CLI, just got used to it. So like I don't need it. But for everyone else who needs a visual feedback, they use VS code. So this stuff is set up. I don't know how to set up aliases there.

**Aaron Bockelie** 11:21  
Here.

**Sergey Kleimenychev** 11:29  
Which I assume will fall on Andrei, unless we do it together.

**Aaron Bockelie** 11:33  
So, so instead of jumping directly into building yet more tools, I think that the right thing to do would be to let's say Sergey, if you were an advocate for all the artists for what is the correct flow for things, not not the only correct flow, but a flow.  
That prevents the rapid stacking of GB sized art assets onto LFS store for example. Like how do we, how do we prevent that from happening? And So what we then need to do is.

**Sergey Kleimenychev** 12:04  
We we cannot escape immediate commits, but we can at least help the cleaning process remove the unnecessary stuff.

**Aaron Bockelie** 12:13  
Correct. And and then the other thing is, is that a good DevOps environment has monitoring. So Andrei, we should be getting dashboards showing how much stuff we're putting into our repos or into our LFS space for example, right?  
And then also we can set up some of ongoing tasks to be able to clean up all those old things to make sure that nobody's got ancient, you know, unnecessary intermediary files committed. And then like I was saying, you can do, you can add commit hooks.  
You can do other checks in git to make sure that people don't do the wrong things, or at least guide them to do the right things, whatever those are. But what I think it needs to be defined is is a better what you've got is the people themselves who don't know git are defining the flow for git.  
And what's happened is they won't give you a very nuanced flow. And So what we need to be able to do is sort of be more deliberate in the actual flow for this and get away from thinking that get LFS.  
And Git is just another file share. People seem to think that it's still a file share in a lot of ways, and it's we all know, at least on this call, we all know it's not that.

**Sergey Kleimenychev** 13:35  
If I were to define the goal for what to do next, I would define it as first we should reduce the interaction surface between artists and git. They should touch it as little as possible, like the stuff should be accessible via a press of a button.  
Anything like pulling, pushing and not being worried about extra set up for stuff like like LFS. This is like the first thing we should do and then we can try to expand on how people use it. Do they understand how it works? Because I did try to explain to some of the artists how this stuff works in in general like what are commits.  
It's how it's stored, how it works, why it was done this way and people are getting overloaded like it's for the first time it's too much. So the best way is to remove steps that might which might lead to errors and then everything else. And also I think it's important to know that my initial rant about.  
Git came from the fact that I didn't knew that any pull via LFS does not pull everything in. I thought that it works exactly like git. If you don't mess with it originally and put any extra filters, it will literally pull every BLOB that it has in LFS, which is not true. So the biggest.  
The issue is mitigated already by the fact that LFS only pulls the actual commit. So the other one is whether we are worried about our GitHub space, then we should squash. I would also squash because it's easier to read. You don't see a bunch of stuff that you don't think. You literally need the last commit where is the important data that is being.  
Like this is what I've done, I've done. No one is interested in seeing my intermediate process and thrown out renders.  
This is the other thing I would do, and the most important one is to set up everyone else in a way that they once fire a script to set up and forget about it. And then each clone is easy and people will never think about extra tuning that might break this way. They don't have to.  
Face the actual issues when it breaks.

**Aaron Bockelie** 15:48  
In order to solve this properly, I think that what you really need to do is we need to define the requirements and what is the what is the characteristics of your of your artist right now.  
Because Sergey, you have the ability to use the command line, and more importantly, I'm I'm I'm also summarizing a lot by saying use the command line. More importantly, you recognize.  
The implications of certain ways of of the git flow that is being used right now and.  
What we need to be able to say is, is that the artists who are also contributing to this probably don't recognize or understand the implications of them pushing lots of files up to LFS or doing the work they're doing.  
And this means essentially understanding what the average artist in the group is. How many people are we talking about? Is it 20?

**Sergey Kleimenychev** 16:52  
No, no, no, but four people.

**Aaron Bockelie** 16:53  
Or so.  
Or people.

**Sergey Kleimenychev** 16:57  
Me, Nesta, Eula and.

**Aaron Bockelie** 16:58  
So.  
So nobody else is committing to get repo or content.

**Sergey Kleimenychev** 17:03  
Dima, I think he's more aware, more or less aware. It's about 5 people and I don't know if there are any other commissioned artists who does. At least one does. So there might be a bit more this this ones I I know for sure it's at least five people.

**Aaron Bockelie** 17:13  
OK.  
So when we.  
So when we have a very small population, it is we have the advantage of everybody being able to support each other and what probably needs to happen is set up a set of guidelines and rules requirements essentially.  
That collectively gives everybody a chance to work in a way that makes sense.

**Sergey Kleimenychev** 17:39  
Yeah.

**Aaron Bockelie** 17:40  
And what will then have to happen is some amount of of assuming that you will use either some tools to help reduce the footprint or you know of interaction with it that the surface like you're saying or we.  
Write some scripts or some other things to be able to help people not have to interact with this as much. But I think that what would have to happen then is that becomes essentially a product. So who's going to own this product, which is the simplification of the git flow for artists?  
Is that you?

**Sergey Kleimenychev** 18:20  
And me.

**Aaron Bockelie** 18:22  
And are you willing to take that on for forever?

**Sergey Kleimenychev** 18:25  
At least as long as I'm working here, if I get fired, I obviously will not be the one doing it.

**Aaron Bockelie** 18:28  
OK.  
So, so then the The thing is, is that we got to now involve Andrei and others to go, OK, so what's the cost of maintaining it? How are we going to verify that it's working correctly? How are we going to monitor this like you know all the typical IT spend problems that.  
Can occur with with investing in this. We've already considered this just for git itself and git LFS is basic, but I agree that.  
Simplifying the process for artists where they're less likely to choose the wrong direction to take their files the way they've committed in the git will help in the long term. But I also am concerned that we're building items of convenience for people that should know how to use git a little better.  
Because these are essentially the original, highly skilled people that need to interact with technical platforms, and if they don't have some fundamental understanding of how Git actually works, that's a problem too.  
So what I don't we got to walk the line between like for instance.  
I know a little bit about a whole lot of things, but I write scripts for a lot of the things I do because I know that when I have to type them in manually, it takes forever. So I write a script. But I also know when that script isn't doing what I want anymore and I fix the script and update it and change it and it.  
You know, it matures after a while. What I'm concerned with is that the people that are using these conveniences to make the process go faster and make it so you kind of have a more repeatability, you know, not checking in as many files, that kind of stuff, is they won't understand what they're doing.  
The scripts will be now available. They'll use them and no one will grow. So it actually needs to be two two sides of the coin here. One is this.  
A convenience set of convenience tools to make it go faster, but also they need to be able to do this without the convenience tools. O we need to get people to be smarter.

**Sergey Kleimenychev** 20:41  
I agree. It's just that it's just that I would put it in the order of the most important thing. It should be easy to use. The second one they should learn by myself like fiddling with this stuff. That's.

**Aaron Bockelie** 20:47  
Of course.

**Val Levitan** 20:51  
I I I disagree with this order.

**Aaron Bockelie** 20:51  
Yes.  
OK.

**Sergey Kleimenychev** 20:57  
Wait.

**Val Levitan** 20:57  
They they should learn.

**Sergey Kleimenychev** 21:00  
No, of course, but the word should.

**Val Levitan** 21:01  
Not, of course, they cannot work for us if they don't learn. I learn.  
I'm 62 years of age.  
I am not an engineer nor a developer, but I understand in order for me to lead the company forward, I must learn. If I must learn, if I must understand git, if I must learn applications.  
They must learn to work for JVL. The market is open. They either learn or they cannot work for JVL.

**Sergey Kleimenychev** 21:41  
Let me put it this way. Uh, we can.

**Val Levitan** 21:42  
I also, I also, I also want to. I also want to make one more point which I believe you don't understand.  
We implement tools not for me and not for you. We implement tools for overall company's operational improvement. Improvement includes integrity, includes certain conveniences, security, etcetera.  
We chose chose GitHub versus SVN because it provides us with overall improvement in the company, not necessarily the best possible choice for graphic designers.  
But the best possible tool for the company overall.  
So whoever is now works for the company will have to address themselves to the tool to this application and will have to learn it or cannot work for the company.  
So now we're coming to about 3 minutes.  
Stop. Any other technical questions that I should set up a meeting with Aaron?  
Because you really have Andrei who can answer all the questions.

**Sergey Kleimenychev** 23:06  
Well, if we are given permission, me and Andrei can fiddle about this idea and think of the ways how to improve it and how much time and effort it might take.

**Val Levitan** 23:17  
We we are not. We're not going to buy additional tools. I am.

**Sergey Kleimenychev** 23:20  
No, it's not about additional tools. It's about setting up existing tools. We don't need anything extra. We just have to make this stuff work. That's the only thing we have to do.

**Aaron Bockelie** 23:27  
Yeah.

**Val Levitan** 23:27  
1.

**Aaron Bockelie** 23:28  
There's no no new tools needed.

**Val Levitan** 23:33  
Your suggestions are more than welcome. Please give give them to Andrei. As I said, I want to participate in every single discussion, so you're more than welcome to include me in your discussion if you think that it's important.  
Include me in. I will not necessarily reply, but as you see, I can bring expertise on board. So I'm taking your suggestion very, very carefully with a lot of attention. I think that you are worth while consulting.

**Aaron Bockelie** 23:55  
OK.

**Val Levitan** 24:06  
I'm consulting you, but I'm telling you that you need to start thinking about the tool for the company.  
Not a tool for graphic designer.

**Sergey Kleimenychev** 24:23  
OK.

**Val Levitan** 24:24  
OK.

**Sergey Kleimenychev** 24:24  
Yeah.

**Val Levitan** 24:25  
All right. So thank you very much. Anything else? No.

**Aaron Bockelie** 24:28  
I'd like to just summarize really quickly. So I think that you have some legit concerns about the flow of a very small team. I think the team needs to learn how to use Git better. You know, there's literally a website called Oh **** Git. It's really funny.  
And you can just go to it. Here it is right here. People need to be comfortable with using these tools.  
Next, if you're using VS Code, that still might be too complicated for artists. I would consider just GitHub Desktop, which is an excellent tool and integrates LFS nicely with things, but I think that Sergey.  
You and Andrei have all the tools at your disposal to be able to help the artist.  
Find this better. Find the way. And I implore you, I I really want you to really think, how are you going to teach them to be better at this rather than give them conveniences and crutches?  
That's the most important thing I can think of on that and this whole topic right now. Do not, do not let them be lazy.

**Sergey Kleimenychev** 25:40  
If I'm given enough time, I can do it. I see no problem doing it as well as with Blender. I do teach people anytime I have I get a chance.

**Aaron Bockelie** 25:52  
OK, so work with Andrei. Andrei, you know where I'm, you know where I live.

**Sergey Kleimenychev** 25:58  
I'm like a sweat.

**Aaron Bockelie** 25:59  
You can always he he can ask questions, but I I know that you're very capable, so.

**Val Levitan** 26:07  
Thank you very much. All the best, Aaron. We have another meeting. Thank you. Bye, bye.

**Aaron Bockelie** 26:07  
Just try. Yeah. Thanks.  
OK. Thanks, Bill.

**Sergey Kleimenychev** 26:12  
Bye.

**Andrei Bosik** stopped transcription