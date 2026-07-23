**GitHub_Ways-20260211_102003-Meeting Recording**

11 February 2026, 03:20pm

11m 49s

**Val Levitan** started transcription

**Evgeny Kharetski** 0:03  
The the cloud.  
The process the cloud.

**Pavel Frolov** 0:06  
But.  
Yes.

**Evgeny Kharetski** 0:17  
No, at the committed GitHub repository.

**Pavel Frolov** 0:26  
Yeah. So in general question, what is the best place where to keep all the special ways that our developers are created in separate repository with all the ways?  
Or special dot cloth directory in each repository.  
And special ways designed to work this particular repository and relates to only this repository.

**Evgeny Kharetski** 1:08  
Um.

**Aaron Bockelie** 1:15  
So what you should be doing is in the root of each repository, or technically in the root of every directory you want guidance in, you have a dot claw directory in your in your repo.

**Pavel Frolov** 1:32  
Mhm.

**Aaron Bockelie** 1:32  
And the cloud repo directory is where roject scoe ways can exist and are sensed and used.  
So if you don't have that set U that that's going to be the problem.

**Pavel Frolov** 1:42  
Yes.  
Mm.

**Aaron Bockelie** 1:57  
I can show you what I mean by this if you'd like.

**Pavel Frolov** 2:01  
Yeah.

**Aaron Bockelie** 2:02  
OK.  
So let me so just we just finished the conversation for the last couple hours.  
I'm going to show you what a fresh instantiation of Waze looks like.  
OK.  
So we can see here.  
Here's Claude, right?

**Pavel Frolov** 2:32  
Yes.

**Aaron Bockelie** 2:38  
So in in Claude we have ways the build way, front end, micro front end and way and we have template and if we go into the ways here it's going to build.  
This is a very specific way to webpack federation.

**Pavel Frolov** 2:55  
E.

**Aaron Bockelie** 3:00  
Short and sweet, it has the the match for the what we're looking for. So if anybody talks about Webpack or remote entries or whatever, it's going to get injected.

**Evgeny Kharetski** 3:15  
Uh.

**Aaron Bockelie** 3:25  
Correct. So let me show you the gitignore.  
So do you see?  
Commit ways ignore developer local files. So do you see how we have these in here?

**Pavel Frolov** 3:47  
OK.

**Aaron Bockelie** 3:48  
So we're gonna get Waze is gonna go in here, but we're gonna ignore these things.

**Evgeny Kharetski** 3:53  
Mhm.

**Aaron Bockelie** 3:55  
This way you keep your local to do's and the ways make it into the repo.

**Evgeny Kharetski** 3:56  
Stop on that now.

**Pavel Frolov** 4:01  
Hello.  
OK, probably I have a question. Actually I have dot cloud directory in the home directory or home user user directory.

**Aaron Bockelie** 4:11  
Mhm.  
Yes.

**Pavel Frolov** 4:23  
And also I have dot cloud at each particular folder that that I was working with. What is the relationship between?

**Aaron Bockelie** 4:37  
Yes.

**Pavel Frolov** 4:39  
General settings and project settings.

**Aaron Bockelie** 4:43  
Excellent question. So anthropic has set up this perspective of user scope and project scope. Yeah, so dot Claude in your home directory is your user scope. dot Claude in a project directory is project scope.

**Pavel Frolov** 4:49  
I saw, I saw.

**Aaron Bockelie** 5:01  
So a lot of the consistency of ways actually lives in in user scope. So let me let me show you the difference.

**Pavel Frolov** 5:02  
So this.  
Probably we need to build a system where all the user scope is working plus the project scope.

**Aaron Bockelie** 5:19  
OK.  
Yes, that's what Waze does, is it incorporates both. It reads both. So if I look at Claude in the project scope, you see how I'm in this branch and on this project. So if I go to Waze in project scope that that I just showed you, yeah.

**Pavel Frolov** 5:29  
C. I.  
Mhm.  
Mhm.

**Aaron Bockelie** 5:45  
No, let me show you the difference.  
I'm in dot Claude in my home, right?

**Pavel Frolov** 5:54  
OK.

**Aaron Bockelie** 5:55  
Waze is not directly in here because of the way Claude has to execute. Waze is in the.

**Pavel Frolov** 6:01  
And.

**Aaron Bockelie** 6:06  
Better find it here. Is it uh?  
Sorry, hooks. So ways exists as a submodule of hooks.

**Pavel Frolov** 6:11  
She.

**Aaron Bockelie** 6:18  
And you can see right here, here's the Waze folder.

**Pavel Frolov** 6:21  
Mhm.

**Aaron Bockelie** 6:21  
And under here we have all of the scripts that make Waze work. These are all executing and running under the hood with all the hooks. OK and then under this Waze we have sub sub modules for all the ways if I go to software dev.  
This is where the ways now exist here, and if I go into SSH, here's the way for SSH.  
Or here's the eight oops.  
Here's the way for ADR. Now ways have two components to them. The 1st is just the way, which is just the text file, right? It's just a it's a prompt injection, just like a a skill is in cloud code, yeah.  
Here's the here's how we do it. But Waze also supports macros. So take a look at this, you see at the top here. So we have this sort of policy controls governance and we say right here macro prepend.  
O macros and this is in the documentation for this too, so if you check it out, macros says execute any macros for this way at the beginning rather than the end of the context.  
So what happens is that when we look at this, we can see.  
But this macro is going to detect whether the tooling exists in a project and tell it in the way when you talk about ADR as to whether it's ready to go and tell it tooling declined for this project. Remove the no cloud tooling flag to enable and so it's actually a whole macro that injects this and tells it.  
Exactly how to do it.  
So it's a programmatic, responsive, deterministic prompt that creates things on the fly, and you can put these macros for anything. So if I look at GitHub, there's both a way.  
Here's the way for the general way for GitHub, for all GitHub, for all projects. Works this way, yeah.  
But then there's also a macro. Excuse me, a macro that looks at the project scope. It counts. It uses the GitHub command line tool to count the number of users in there and figures out whether it's a solo project or a collaborative project and tells that to the to the tool.  
It also gives the repository help. Is it well configured or poorly configured and it will eventually harass the the the coding agent a lot if it's a multi user project that's poorly configured and say you should probably think about fixing this.  
So it's all in there doing this, and here's the various scores, right? Has a license, has description, topic, code of conduct, and whatever. That's the GitHub way. And so these are user scope, meaning every project you interact with, whether you have rights to do it or not.  
It's going to kind of do that because as a as a professional software engineer, I hate working in GitHub repos that aren't well configured, and so I'm forcing Claude to take on my way of doing things.  
And my way is the user way. Does that make all sense? It's all connect now.

**Pavel Frolov** 9:46  
Yeah, so we will take general part of all the ways as a separate repository that we will sync with you and each project will have its own set of ways that will be in.  
Injected into user layer of ways.

**Aaron Bockelie** 10:08  
In a project layer of ways O roject ways go into roject layer it all.

**Pavel Frolov** 10:12  
It it will, it will live in the project, but it will inject it into general way, yeah.

**Aaron Bockelie** 10:17  
Yes.  
Into the session, yes, into the session. And so This is why I was telling you how important it is that you keep your forked copy of of the whole Waze grant repo up to date because this is this the user scope Waze.

**Pavel Frolov** 10:24  
Yes.

**Aaron Bockelie** 10:36  
Is how you have a consistent expectation of what a developer should do at JVL who are if you're using the AI tools across everybody.

**Pavel Frolov** 10:47  
It's perfect.

**Aaron Bockelie** 10:49  
And if there's some specialty thing you want to do or add, like configure, turn things off and on. If you're outside of the normal envelope, you could fork it internally and you could have a ways for non developers or whatever too, whatever that might be.  
You can activate and deactivate sections of way sub areas. So if you if you could deactivate the software engineering ways ways group and enable the legal or the finance ways if you wanted to.

**Pavel Frolov** 11:22  
OK, clear.

**Evgeny Kharetski** 11:24  
Thank you.

**Aaron Bockelie** 11:24  
OK. Does that answer it all the way at at Evgeny?

**Pavel Frolov** 11:25  
Thank you. Absolutely.

**Evgeny Kharetski** 11:27  
Yes, yes.

**Aaron Bockelie** 11:29  
OK, I'm excited that you have questions. This is fantastic. So.

**Pavel Frolov** 11:33  
Thank you. Thank you.

**Evgeny Kharetski** 11:35  
Thank you.

**Val Levitan** 11:35  
Pavel, can I get on the can I get on the call with you? Do you need a few minutes?

**Aaron Bockelie** 11:36  
Thanks guys.

**Pavel Frolov** 11:41  
No. Bye.

**Evgeny Kharetski** 11:41  
Bye.

**Aaron Bockelie** 11:41  
Bye.

**Val Levitan** 11:43  
OK. Aaron, thank you very much. Bye.

**Val Levitan** stopped transcription