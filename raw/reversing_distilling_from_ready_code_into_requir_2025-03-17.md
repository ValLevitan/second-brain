---
tags:
  - code-maintenance
  - software-improvement
  - repository-migration
  - github
  - val
  - aaron
---

**Transcript**

17 March 2025, 01:57pm

**Val Levitan** started transcription

**Aaron Bockelie** 0:03\
To implement this with a partner, then those are indicators that we
could improve, not the code base, but.\
The description of how to implement it and describing it in the
documentation inside of it.\
This is this is kind of falling into the code maintenance side of things
rather than trying to improve it.\
I don\'t wanna change the source code, I just want to understand it and
So what that means is.\
By understanding it better, it improves the commercial viability of the
software itself, therefore improving its value.\
By being able to utilize it or employ it in more situations faster.\
Is what we would ideally want to be able to do is bring another engineer
into the conversation if if Heem\'s finally on vacation, going to
somewhere relaxing for a while for example.\
Same goes with Igor.\
We need to be able to make sure that we have code that is functional and
usable without you guys necessarily present.\
This doesn\'t mean we\'re gonna get rid of you to not work on it
anymore.\
It just simply means what can we do to ensure we\'re maximizing what
we\'ve got in the code for integration possibilities and and bringing
bringing integration work faster in the door if possible.

**Val Levitan** 1:45\
I started the recording.\
Can you please repeat for the recording?\
What is the next step that we want to execute?\
I heard moving it to GitHub.\
Can you elaborate on it?

**Aaron Bockelie** 1:57\
Sure.\
So currently the code base resides in in in SVN and so I think the very
first thing we need to do is to bring it to the plat modern platform
that jvl is settling on which is get a git based platform.\
And.\
Let\'s move all of the repository.\
Hopefully it\'s. I don\'t know if it\'s one big model repo or if it\'s
several or whatever, but let\'s make sure that there\'s an appropriately
configured space for it.\
To exist on because we\'re not materially changing the code right now.\
We\'re just looking at at it and understanding it, doing static
analysis, documenting it.\
This means that in the git repos, we can begin to understand it better
and ensure that we have a git.\
Focused approach to building the product.\
The framework, since it\'s a known.\
Deterministic piece of software that can be rammed.\
And that means eventually we can begin to approach the same git
development lifecycle. The git flow that we would have for the other
products that Jvl is working on.

**Val Levitan** 3:20\
Is that understood? Accepted. Challenged.\
Questions. If no questions, then I consider meetings closed.\
Let\'s just decide when we can meet again on this.\
Of course.

**Igor Metelski** 3:43\
It\'s not working. Let me see.

**Val Levitan** 3:47\
Of course I understand this. Thank you.

**Efim Podvoiski** 3:50\
So only question is, do we plan it to like stopping the current
development and because there\'s process of switching it will be
painful?\
So do we stop the, for example, the current integration with Hollywood
bets or?\
We plan it for like, I don\'t know for for end of April and finish the
Hollywood bets and then don\'t start anything else.\
Some places I don\'t think that they it will be very easy step to to
switch.

**Val Levitan** 4:23\
I\'m not.\
I\'m not sure that it\'s really a painful issue.\
I I\'ve heard.\
Let\'s say Andrei discuss it and with Pavel and they move their adka
move the other his repositories from SVN and that that wasn\'t painful.

**Efim Podvoiski** 4:41\
Yes, but they\'re not running it yet, right?

**Val Levitan** 4:47\
They are. I mean not they.

**Efim Podvoiski** 4:48\
There\'s on on, on, on, on.

**Val Levitan** 4:51\
One of the they are.\
They are the Ratko moved his entire Omni to get.

**Efim Podvoiski** 4:55\
Yes, yes, I understand.\
Uh, but.

**Val Levitan** 4:59\
Very little issue.

**Efim Podvoiski** 5:01\
OK. We have we have like.\
Builder applications there.\
That are set for taking data from SVN.\
So at least they have to take data from some different source at least.

**Val Levitan** 5:18\
I feel I feel that it should not be more than five days.

**Efim Podvoiski** 5:22\
Yeah. I\'m not saying it\'s more than five days and but it\'s five days
is 5 days, yes.

**Val Levitan** 5:23\
And if.\
Or quite then.

**Efim Podvoiski** 5:29\
And then in an impossible to do anything during these five days, yeah.

**Val Levitan** 5:34\
So my answer to this is definitely move it to Git first.\
And then move on with Hollywood bet because it will be an excellent
practice for us to ensure that as we\'re working in Git, we\'re gaining
the experience with it definitely then I would greatly.

**Aaron Bockelie** 5:50\
If he I have, I have questions about the way it\'s implemented right now
and and in SVN. Do you have builders that exist in Jenkins to build it
right now or is it just simply OK?

**Efim Podvoiski** 5:51\
OK.\
Yes.\
Yes, yes, yes. Yeah, two things.\
One is I have the big project in.\
My God, I have one big project that I built on my machine and test.\
At least run unit tests and run some functionality, some functionality.\
Theoretically everything but I we don\'t do it anymore and we have like
dozens of applications that are built individually from this code base
on on Jenkins and then deploy it, then deploy it to to the cloud.

**Aaron Bockelie** 6:30\
Yep.\
OK.\
And does Jenkins have a cloud deployer automatically as well already?

**Efim Podvoiski** 6:48\
Yes, automatic it can deploy automatically to our development and test
environment, but not to prod environment.

**Aaron Bockelie** 6:57\
OK.\
So. So then what needs to happen then is the initiative. I think Val for
this has to do with looking at the Jenkins recipes that exist and
understanding what they do.\
And then going ahead and rebuilding them as actions on GitHub to do the
same thing.\
It\'s entirely possible that it\'s gonna be.\
Just copy the scripts over from.\
From the from the Jenkins builder Jenkins recipes.\
Check them in as a bunch of build scripts into the repo and then make a
generic action call runner.\
I hope this is being recorded to to just sort of black box it
basically.\
So we just start a container, run the container, run the scripts in it,
get done with it.\
That\'s like stage one of a of a migration from Jenkins to GitHub.\
And then later the actual actions can be refined significantly to break
them all out into the true actions for deploying as they need to. So.\
What probably would have to happen in the meantime, and I think this is
a theme, is your concern is, is that in order to facilitate.\
The ongoing work that you\'ve got you kind of would have to stop
committing code to SVN, or you\'d have to backport back to SVN.\
And from get or establish some pattern like that is what you have to
do.\
So my suggestion would be.\
Still get it to git as fast as you possibly can.\
Like, just make a stopping point and you may even be able to reconfigure
Jenkins to just point to the git repo rather than the SVN repo, and that
might actually be much faster to get started.\
So stage 1, move the code base to Git stage two or stage 1 1/2 Tweak
Jenkins a little bit.\
To use Git rather than SVN, stage two is rip and replace.\
Remove it out of Jenkins.\
Recreate the actions and in GitHub as as they were before and divorce
fully from SVN and Jenkins.

**Efim Podvoiski** 9:18\
Yeah, but stage 3 is like you can do it on a on a laser.

**Aaron Bockelie** 9:25\
Yeah, yeah. You don\'t have to do all of them.\
You just do the ones that are active or necessary, yeah.

**Efim Podvoiski** 9:36\
OK.

**Val Levitan** 9:40\
OK.\
The instructions are recorded for your pleasure here.\
Everything is detailed.\
I suggest you guys.\
Grab the transcript of it. If something is not clear.\
Igor is on vacation until next Monday. As of next Monday, if him, if you
agree, can you please make it a priority?\
For that following week, which is the week of the 24th, and I will check
back with you on the 31st.

**Efim Podvoiski** 10:16\
OK.

**Val Levitan** 10:16\
Is that acceptable to you?

**Efim Podvoiski** 10:18\
Yes, yes. I\'m, I\'m.\
I have to, but the bulk of work is on Andrei Bosik, so he need time to
to do it.

**Val Levitan** 10:28\
He has time. He knows what he\'s doing.\
He has open line with Aaron.\
All the help that you need is available.\
Tell me what you need and we\'ll get it done for you.

**Efim Podvoiski** 10:45\
OK.

**Val Levitan** 10:47\
But I\'m leaving it in your court to manage.\
I\'ll just book myself for a meeting with you on the 31st. Based on the
transcript of this meeting.\
With that, I thank everybody Igor again.\
Have a great vacation.\
Sorry for troubling you and that\'s it. Thank you very much.

**Aaron Bockelie** 11:06\
Great. Thanks.

**Igor Metelski** 11:06\
So that\'s.

**Efim Podvoiski** 11:08\
Thank you.

**Val Levitan** 11:09\
Oh yes.

**Val Levitan** stopped transcription
