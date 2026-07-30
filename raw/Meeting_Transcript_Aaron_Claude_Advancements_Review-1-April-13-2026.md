**Claude_advancement_review_implimentation-20260413_081845-Meeting Recording**

13 April 2026, 12:18pm

35m 35s

**\
Val Levitan** started transcription

**\
Aaron Bockelie** 0:06\
You back?\
I can\'t hear you now.\
No microphone. Check your mic settings.

**\
Val Levitan** 0:28\
Can you hear me now?

**\
Aaron Bockelie** 0:29\
Yes.\
I can hear you.\
All right. Is the screen share still working?

**\
Val Levitan** 0:39\
Yeah, yeah.

**\
Aaron Bockelie** 0:40\
Okay, so\...\
I\'m gonna stop that chair for just a minute.\
I\'m gonna show you.\
How this is able to work, so\...

**\
Val Levitan** 0:53\
So I didn\'t know that Bash was in fact, as you said, it was hands. And what did you specify as eyes? I forgot. Rust.

**\
Aaron Bockelie** 1:02\
Essentially, anything that comes back from a tool call, any text that streams back is the eyes of or ears of the coding agent.

**\
Val Levitan** 1:12\
But why did you pack Bash as hands? Because I thought that Bash is code.

**\
Aaron Bockelie** 1:19\
No, Bash is just a program that runs.\
Basically, you can think of it as\...\
Any subprocess that Cloud Code can dispatch and capture the output of is considered a tool use.\
So, what happened was\...

**\
Val Levitan** 1:39\
Well, you know, I mean, I mean, I understand that.

**\
Aaron Bockelie** 1:42\
So what happened is that on version\...\
Uh, 2198.\
of plod code.\
The monitor tool was released.\
Monitor tool is special because\...\
It lets Claude watch something in the background and react to it when it changes without pausing the conversation.\
So I\'ve been hoping that this would eventually get released at some point, and they finally did.\
And its intended use is you can say, Claude, watch this log file and log errors as they appear. Or\...\
Watch a pull request or continuous integration job and tell me what its status changes from in progress to done.\
Watch a directory file for changes. Track output from any long-running script you pointed at.\
So what happens is that Claude itself writes a small script for the watcher and runs it in the background. And the background data gets returned back to Claude by each output line, and then Claude picks up that message and does something with it, whatever it might be.\
So it uses the same permission rules as bash, so you can allow and deny it and stuff like that.\
O.\
In order to leverage this, essentially what you need to do is you have to have an idea of what you want this thing to actually do. So in this case, if you\'re thinking, well, I want to watch this log file, you kind of have to tell it that. It\'s probably a tool that doesn\'t surface\
as obvious for a lot of people, unless you\'re kind of already thinking that way.\
The other thing that occurred to me right away was that the idea that you could leave something long running deliberately means that you could use it as a hook for all sorts of other stuff.\
O.\
Um\...\
Hang on one second here.\
I just gotta, I\'m actually fixing something in here as well.\
Um\...\
So what this then means is that if you\'ve got this long running process that can run for hours or for as long as Claude code is running, it means that you could kind of use it as a cell phone for Claude, sort of almost.\
So think about how Claude operates right now. It doesn\'t.\
It doesn\'t really have any awareness other than itself and the user and the space it\'s in.\
As soon as you give it this thing called monitor, Claude can essentially dial a telephone and listen to something on the other end for stuff to come in.\
Well, instead of it dialing a phone and getting a regular thing, let\'s just make it ambient. Let\'s just make it run all the time and pick up a whole bunch of stuff. But we have to be very careful in the way we disclose this because it could just be noise. It\'s like, it\'d be like,\
calling five or six different telephone calls for different processes, and they all put you on different hold music, and it\'s highly confusing when one of them comes out of the thing. So you have to kind of have a structure to it, right? And so that\'s how attend idea came to be, because what it is, is it\'s attending\
to the environment is essentially why I called it that.

**\
Val Levitan** 5:40\
And the tent is your tool, you wrote it.

**\
Aaron Bockelie** 5:42\
Right, it\'s a binary application like Waze.\
in the same code repo as Waze as a monorepo of sort.\
And, uh\...\
One second here.\
So then what happens is that what the hell do you do with a thing like this, right? What use does it have?\
Well, the first use that I found\...\
is that I needed to have a more formal bundle of capabilities, not ad hoc running.\
a bunch of stuff on start. So if we think about what Anthropic is saying, they\'re saying use this to watch for stuff or other things. And it\'s super special use case. But I think that\'s a big waste of the capability of in-session injection.\
So instead, I have a particular way of working about stuff. My opinion is that I use GitHub and that I build stuff with Makefiles and I watch my system for things and whatever. And so why not build a tool that runs in monitor mode all the time?\
That just promotes that all the time, so I don\'t have to remember to ask it a bunch of stuff. I just set up a single capability or a slash command slash attend, and it tells it to start running the monitor tool. From that point forward, I have a structured deterministic framework.\
to put in whatever I want inside of there that might be part of the claude code ecology that I have for my computer.\
The next thing I thought about, which was just like, you know, it would be pretty cool if dot dot dot.\
multiple clods could talk to each other. Because I\'ve been trying to come up with a method of doing that for a while because I don\'t really know why you\'d do that at first, but I needed to try it just to see what would happen. And so when set up properly,\
What happens is that if you have a bunch of adjacent projects running on your computer, let\'s say you, you know how, and I\'ll connect this to your recent discussion about get submodules, how you know you have the, I advise to use the meta.\
the meta repo with all the submodules.

**\
Val Levitan** 8:12\
Yeah.

**\
Aaron Bockelie** 8:14\
So if you have the submodules checked out and you clone the whole meta repo, you invoke.\
You either need to invoke a clod in the master meta repo, or you invoke several clods inside of the submodule areas. If you invoke clod in the submodule, that\'s its home place. You\'re not at the top of the tree. You\'re sort of one or two levels into the tree, right?

**\
Val Levitan** 8:39\
That\'s right, that\'s right.

**\
Aaron Bockelie** 8:42\
And so, if you have\...

**\
Val Levitan** 8:43\
But now, but now you\'re saying I can, I can have multiple cloths doing multiple sub-modules and talk to the main cloth who sits on top of them and and.

**\
Aaron Bockelie** 8:54\
No, it\'s not even talking to a maid Claude. It is actually them coordinating amongst themselves in this own thing.

**\
Val Levitan** 9:01\
Oh yeah, yeah, you don\'t even need the main cloth. It doesn\'t matter who\'s me.

**\
Aaron Bockelie** 9:04\
No, there\'s no reason for a maid cloth.

**\
Val Levitan** 9:06\
Yeah, you just, you just kind of\...\
Uhh.\
Multiply your clods, put them on your on whatever repos you want, and as long as they\'re capable of talking to each other.\
You know, knock yourself out.

**\
Aaron Bockelie** 9:24\
Yeah, yeah.

**\
Val Levitan** 9:25\
Wow, that\'s amazing. I love the idea. But hold on a second. Before, or I mean, sorry, now you cannot do it. You can only do one cloud, one repo.

**\
Aaron Bockelie** 9:28\
And\...\
Well, you could put Claude at the top of your meta repo and it can change its base, its directory in different spots, but the entire conversation session is based on the place where you invoke Claude at. So like if I have root and then I have submodules one through 4,\
Right? If I invoke Claude on root, all of the conversation history and everything going on is based on root, not submodules one through 4.

**\
Val Levitan** 10:06\
It\'s interesting that you say this because when I use Cloud Code, it says what folder do you want to put it on?

**\
Aaron Bockelie** 10:13\
Right.

**\
Val Levitan** 10:15\
So, you have to define the folder.\
So if you put it on very top, it loses its potency as it goes down.

**\
Aaron Bockelie** 10:28\
Yeah, so it\'s\...

**\
Val Levitan** 10:30\
I\'m using, I\'m using childish phrases, not technical. I understand this, but I guess I\'m conveying the same message as you are.

**\
Aaron Bockelie** 10:30\
It\'s well.\
It\'s not that it loses its potency on the way down. It\'s that the scope, the amount of information, the potency remains the same.

**\
Val Levitan** 10:41\
Maybe not.

**\
Aaron Bockelie** 10:52\
It\'s the amount of information as you descend into the tree deeper that dilutes the potency. That\'s a little different way to see it.

**\
Val Levitan** 11:00\
Okay, but I understand what you\'re saying. We\'re basically saying the same thing.

**\
Aaron Bockelie** 11:08\
Oh.

**\
Val Levitan** 11:08\
And, and I\'m sorry, this is now.\
You\'ve gained this ability because you\'re\...\
You have monitor and you have a tent coupled together.

**\
Aaron Bockelie** 11:21\
Yes.

**\
Val Levitan** 11:22\
So one thing, so monitor, so when you put clod on a repo, let\'s call multiple repos, multiple clods, how do you invoke monitor and attempt? Can you explain to me?

**\
Aaron Bockelie** 11:36\
So monitor is built into Claude code. It is not something I wrote. It is something anthropic put in there. And so in Claude, all you do is you just tell Claude, Claude, I want you to monitor this thing. And Claude\'s going to go, OK, let me launch a monitor for that. And what it\'s going to do

**\
Val Levitan** 11:41\
Right.

**\
Aaron Bockelie** 11:55\
is it\'s going to have, it has some internal rules that Anthropic wrote about how to use monitor, which is, don\'t read a static thing, tail a file, use something that\'s going to print out console information occasionally, blah, blah, blah.\
And so when you do that, Claude invokes monitor and then essentially it reacts to things that change. So the most simple monitor that you could have would be\...\
Um, let me think of something, so\...\
There\'s a thing called stat in Linux and Unix. In Unix, when you stat a file, you\'re statting it to, you can stat a file to see when it last got touched by anything in the file system.\
Meaning, you could stat it even if it got a directory listing, but more commonly, you stat the file when somebody saves or changes the file.\
And so you would get a notification, a log line printed, every time that file got touched by a change.\
So you can stat not just individual files, but you can stat entire directory trees or directories. So if you stat an entire directory, you\'ll get a notification when file X, Y, or Z is touched, one after the other. Boop, boop, boop. So if Claude is running a monitor,\
with stat, and running basically bash stat my directory, that\'s the command that it runs. It\'ll sit in the background as a monitor, and anytime you edit a file, Claude instantly knows that you changed this or that file.\
without you typing to Claude. You don\'t have to say, hey, Claude, I edited this file. It just knows it because it saw the stat come up.

**\
Val Levitan** 13:44\
And if, if, if we want to\...\
Understand what has been changed. Claude will tell us in prose.\
What has been changed?

**\
Aaron Bockelie** 14:01\
Yeah, it depends on how you set up the monitor and what you\'re monitoring.

**\
Val Levitan** 14:04\
Well, listen.\
Okay, but let\'s say for me, when developer changes something, they know what they change, but I would like to get it digested by a pros.

**\
Aaron Bockelie** 14:07\
Right.\
So\...

**\
Val Levitan** 14:15\
That explains what has been done.

**\
Aaron Bockelie** 14:18\
That would be, uh\...\
How do I describe that? That would be an excessive way to use Claude code.\
So, what happens is that, in the in the in due course of working on things.\
Statting a bunch of files could bring thousands and thousands of lines of change if you\'re working on stuff, especially if you\'re using a coding agent to make edits.\
Any program that opens something might make edits. If you use Obsidian, right, and you load a new copy of a plugin and you\'re stating the Obsidian directory, there could be 1000 changes instantly because you\'re blindly stating every file system change inside of there. So it\'s not.\
We\'re just picking one example, which is a stat, and I don\'t want you to run with it and say, this is how I\'m going to watch everything. Stat is used as a simple atomic sort of understanding of what a change means.\
If you\'re looking for a change log of what actually happened, you could stat everything in the background and then essentially look at the files and make a difference for every file that was changed. But what you\'re what now what I\'m talking about actually is just called Git.\
That\'s what Git does. So if you\'re looking to track changes, Git would be your friend for that.

**\
Val Levitan** 15:48\
I actually hijacked the conversation and derailed that I shouldn\'t have done it.

**\
Aaron Bockelie** 15:52\
Yeah, it\'s OK. We\'ll get back to we\'ll get back to attend here in a second. So, going back to the idea that you can watch for a system environment change.\
and then it gets injected into the Claude code session without typing anything is essentially the core.\
As an experiment, I wrote a little bash script that ran a connector to download a picture from my webcam to take a picture, save it to the temp directory.\
and then ran ffmpeg to compare the difference from that picture from the last picture.\
Basically, what happens is that if the threshold of the change of the picture is more than 25% different.\
to print something to the console. In this case, it said the picture had changed. And here\'s the picture. Here\'s the latest picture. All it is is 2, it says.

**\
Val Levitan** 16:42\
Peck.

**\
Aaron Bockelie** 16:50\
Webcam has detected significant change. Here is the image of the change.\
The path.\
When Claude monitors that simple little script, it sees that exact text, and so Claude will decide to do something with it. So in this case, I said Claude.\
Monitor this script.\
and tell me when I\'ve left and come back from my desk. And it goes, okay. And so it runs it. And on the first run, it says, here\'s the path to the picture. So you know how you can drag a picture in the Cloud Code and it can see a picture? So it just downloads the picture and looks at it. And it goes, I see you\'re sitting at your desk. Hello, Aaron.

**\
Val Levitan** 17:22\
Yeah, yeah.

**\
Aaron Bockelie** 17:30\
is what it literally says.\
And it said like, nice bookshelf or something like that. And I\'m like, cool. And so then I don\'t say anything to Claude. I just get up and walk away. And I stand outside of the camera angle, and then the script pulls it at the 15-second marker, and it does a diff. And then the difference of me sitting in my\...\
Desk versus not was enough to trigger the script to detect the change. It then prints out the exact same line again that says, picture has changed more than 25%. Here\'s the path to the image. It doesn\'t do anything other than that. It\'s stupid. It just does this, prints this out, right?\
Claude sees this new line set, these new lines in its monitor, and it goes, oh, the script has updated something. Let me see what\'s going on. And then it opens the newest picture and it goes, oh, Aaron has left his desk.\
Where did you go? And then I wait for, and then an alt, and it just basically says, I was given no other instructions, so I\'m just going to wait here. And then I come and sit back down, it changes again, it fires again, he looks at the picture again, and it goes, oh, you\'re back. And so that\'s kind of an example of a sensor loop.\
vector loop for a 10.\
So that\'s kind of a fun one. It was just kind of a, you know, that was the first thing I tried because it was like, oh, I got to try this out. But what it means is that a lot of the useful stuff you want to see that are long-term happening, like get repo changes or build environments.\
or just honestly about anything that you might want to, that you want to have Claude attend to, and can be added as a sensor in this framework.\
So\...\
Let me.\
Turn on another screen share here.\
On the left.\
is a session of\...\
code that has been while we were talking was adding a little bit of nuance to the how attend runs its program and executes stuff.\
Um\...\
Let me just kind of set some things up here.\
On the right side is an empty terminal.\
I\'m in the temp directory in my user home folder.\
The left terminal is in the attend, is in the Claude code directory, which, or the Claude code root directory, which is where I was running, I\'m writing the code for this. So 2 different project directories, two different projects.\
Now, if I run attend\...\
And I just invoke this.\
You can see here where it starts the thing, and it\'s\...

**\
Val Levitan** 20:39\
I, your, your screen is not doing anything; it shows at the end.

**\
Aaron Bockelie** 20:43\
Oh.\
Let me try again. Maybe I picked it wrong.\
I, Teams is such a\...\
The show sometimes.\
Um\...\
It\'s showing stuff now.

**\
Val Levitan** 21:04\
Yes.

**\
Aaron Bockelie** 21:04\
OK, let me do this again.\
When I run attend, as if I were invoking it in a monitor session for Cloud Code, we can see the messages.\
And then it sends this message here and prints it out.\
Hang on one second. I gotta correct something.\
I just got to tune the software a little bit. But anyway, so what happens here is that when attend starts\...\
There\'s a, you can see here, there\'s a tick loop. It starts it. It says 5 sensors registered and it has a context sensor, processes, get, disclosure, and peers. These are five different.\
For better word, there are different eyeballs or different things that it has senses for. Just as you have the five senses of your body, touch, sight, hearing, so forth. These are senses for Claude because it doesn\'t, Claude doesn\'t have a choice. These things get added.\
injected into the monitor through the monitor channel without Claude asking for them to happen.\
So, think about normal tool calls means that Claude has to decide to trigger a tool call, right? You type something and it sends it out. This works the other way around, and then it pushes sensory information into the session of Claude while it\'s working.\
So, this particular message here, which is a set of affordances of how to use attend, it tells how to use messaging and hygiene about typing messages and the length of the messages and saying nothing.\
and don\'t run, attend, run and things like that.\
So this basically gives Claude code some clues, some context clues, on how to use the tool properly, because it doesn\'t have an idea. This is actually very similar to how MCP servers work. When you start an MCP server, it injects a series of rules of how to use the tool.\
and invoke it essentially.\
So\...\
When we look here.\
We can.\
Look at peers, and when I run attend peers, we see myself.\
And we see the.claude directory right here. This session, I\'ve split my terminal into two pieces, the left and the right. And this left terminal is this one right here. So only, and you can see it. Do you see how it says 1 monitor down here?

**\
Val Levitan** 24:27\
Yeah.

**\
Aaron Bockelie** 24:28\
That means that this claud has invoked, I asked it to, I ran the slash attend skill.\
And.\
So now you can see right here it actually even injects itself. Monitor event, attend.\
See how it detected all on its own? And I didn\'t ask it to do anything.\
So now, I\'m going to go ahead and launch Claude in this directory here.\
And I\'m going to say\...\
slash attend.\
And so, it\'s going to, it\'s going to\...\
Connect itself to the Attend framework by doing this.\
See how it says monitor started and now there\'s one monitor and it says monitor event attend get peers process blah blah blah.\
10 is up, standard reheat, no change, state change to flag. Now I\'m going to do another terminal like this.\
And I\'m going to go into my.\
Go to documents.\
And I\'m just going to run attend myself. And I\'m going to say attend.\
Oops, and.\
Send, broadcast.\
This is just Aaron testing a tent after a clean build.

**\
Val Levitan** 26:12\
Yeah, I read it.

**\
Aaron Bockelie** 26:13\
Yeah.\
So it\'s going to write the signal and watch these two sessions over here. I\'m not typing in there. I\'m just going to let them sit.\
You can see that the one on the left got a monitor event.\
And then the other one\'s going to eventually get one as well.\
You can see it\'s thinking.\
Just has to do stuff. I noticed Claude\'s been pretty slow. Now the middle one\'s got it too. See how it picked it up on its own? Not touching this.\
So now it\'s looking at its peers and it\'s going, oh, I know what to do.\
And now it\'s sending messages to each other.\
Hey, peers, Aaron asks us to chat amongst herself to exercise a 10 on a clean build. I\'m in temp. This idling, what are you working on? Anything interesting in your project right now?\
And now this one\'s getting a message back again.\
And it\'s kind of getting another message here. So now they\'re just talking to each other between the two of them.

**\
Val Levitan** 27:17\
So.

**\
Aaron Bockelie** 27:26\
So this one detected that they both talked at the same time.\
Kind of like saying, hello, how\'s your day going simultaneously? You know how that can be awkward, right? And so this other one detected that and went, let me jump forward to know where to go.\
And so now they\'re just talking about this.

**\
Val Levitan** 27:49\
OK, so you obviously see a practical application, which I, which I don\'t see.

**\
Aaron Bockelie** 27:55\
So the practical application, so I\'m just showing you the mechanics of how these can talk to each other between 2 clods that are essentially idle and not doing anything.\
So what we could do is I don\'t have a claude, I don\'t have a project that uses submodules to this extent right now.\
I have one project that has a single sub-module, unrelated to what you\'re seeing here, and I used two clods, one in the main project to work on the software itself, and another clod in the sub-module to fix the library that the main one depends on. So basically\...\
main project, it wasn\'t a meta project like we were discussing for the big umbrella of JVL, but it was more of a, this is an application running and it uses this Git repo as its core library to work.\
And so what I needed to do is I needed to update the core library, but I also wanted this to work as well. And I said to the library, I said, work on this over here, tell the other clod to pause for a minute and work on something else while you fix the core library problem.\
problems and then go ahead and let it know when it\'s done. So then it managed that conversation instead of me having to think about it.\
So this thing then fixed the code, built the binary, verified and tested it, version incremented it, pushed it up to get, and then it told this one, okay, I fixed this, now you can proceed.\
And then this one went and proceeded.\
So in this case, the entire time you and I have been talking, these two on their own have been discussing how to do stuff.\
So actually what happened is that they\'re now talking about\...\
Um\...\
how to improve the 10. So they just, this one just said, hey, this works, but I\'m just reading through this here. This works, but the experience could be better. And this one went, yeah, this looks good. I\'m going to capture that and write that as a GitHub issue so we can fix this.\
So, on its own, it negotiated how to self-improve itself.

**\
Val Levitan** 30:23\
This, this is, this is nuts.\
But it could do it on the code itself.

**\
Aaron Bockelie** 30:30\
Yeah, exactly.

**\
Val Levitan** 30:32\
So it could continuously find vulnerabilities, perfect it, probably release it.

**\
Aaron Bockelie** 30:38\
Right.

**\
Val Levitan** 30:41\
Download it.

**\
Aaron Bockelie** 30:48\
So I just have to say this is great. Sounds like we found some tuning to do. Let\'s fix it is all I have to say.\
And so I just kind of implicitly give it permission to finish it finish what it found and negotiated with another plot.

**\
Val Levitan** 31:02\
So, this\...\
So\...\
So, this loop became possible because you wrote a tent.

**\
Aaron Bockelie** 31:12\
Yeah, I couldn\'t do this before because I would have to be the one shuffling the messages back and forth to each other.\
Think about it like this: if you had an office\...

**\
Val Levitan** 31:21\
So, how does how does some entropic continuously improve their software? Do they have something like a tent?

**\
Aaron Bockelie** 31:32\
I don\'t know, probably. They probably have a lot of stuff they don\'t tell us. That\'s my guess.

**\
Val Levitan** 31:39\
They have a lot of stuff and then they develop it into a module, audit on Tropic and extend its capabilities.

**\
Aaron Bockelie** 31:45\
Yeah.\
Yeah, so they\'re, you know, they\'ve got some internal build of Cloud Code that they use that has other capabilities. When they accidentally release the source code for Cloud Code, a bunch of findings of hidden features were found in that. So obviously they\'re thinking about stuff.

**\
Val Levitan** 32:04\
So, how is it? Is it tested? Can I now deploy it on my repos?

**\
Aaron Bockelie** 32:12\
Yes, so the repo is always up to date. The thing is, is that\...\
Let\'s switch to a different screen share for a minute to show you what what

**\
Val Levitan** 32:21\
Why don\'t I, it\'s 10, it\'s 10 to the hour. You have one more hour.

**\
Aaron Bockelie** 32:25\
You want to get Andrei on the call so I can explain?

**\
Val Levitan** 32:29\
Well, I would get Andrei Biratko and Haretsky.

**\
Aaron Bockelie** 32:34\
Sure, so maybe what we can do is just have a, if you want to do, let\'s set this up properly so everybody should be able to understand me. I\'m just going to explain that both ways and a\...

**\
Val Levitan** 32:44\
Oh, \*\*\*\*, what?\
Or should I set it up for Wednesday or for tomorrow?

**\
Aaron Bockelie** 32:49\
I think what we could do is just, we got the hour, let\'s just give them the intro and they can go explore it on their own if they want to. Because it\'s all in the Git repo, it\'s ready to go, but they need to know a few details about what\'s changed so they kind of have a handhold.

**\
Val Levitan** 33:03\
Yeah.\
The only reservation I have is that we are in the midst of\...\
Agreeing on the repo\'s architecture.

**\
Aaron Bockelie** 33:15\
Yeah.

**\
Val Levitan** 33:15\
And Andres portion of deployment.\
So that\'s what\'s happening.

**\
Aaron Bockelie** 33:23\
Maybe we just bring Andrei in. Let\'s just bring Andrei in and I\'ll quiz him to see what version of the management he\'s using and make sure that he\'s kind of prepared to support this.\
Because it really, this system doesn\'t care if you\'re using Git in whatever ways you want. It\'s agnostic to that.

**\
Val Levitan** 33:48\
No, let\'s do it. Let\'s do it tomorrow. I have the recording of it. I will send them a digest version of it.

**\
Aaron Bockelie** 34:00\
Okay.

**\
Val Levitan** 34:01\
and prep them for the meeting tomorrow and I\'ll book you in. How is your schedule tomorrow?

**\
Aaron Bockelie** 34:08\
I think this time in the morning would be a good starting point. We could do an hour, and if we need more time, then we can grab a second hour.\
Um\...\
See.\
When you\'re done with that scheduling thing, I\'ll go to another topic here.

**\
Val Levitan** stopped transcription
