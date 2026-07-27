**Aaron_Val-20260317_091238-Meeting Recording**

17 March 2026, 01:12pm

6m 7s

**\
Val Levitan** 0:03\
These instructions now is to prepare you for the meeting tomorrow. Go ahead, Aaron.

**\
Aaron Bockelie** 0:08\
All right, so all I really want to know is, are you keeping up with the version increments of Cloud code ways for my copy? That\'s kind of question one. Question two, you have an integration path.\
To.\
Track JVL specific ways at and and integrate them into my changes that I make.\
Or do you have a branch that you\'re maintaining that you\'re doing integration into?

**\
Andrei Bosik** 0:35\
Uh.\
First question, we as I earlier say about this, we have a script which automatically update your cloud code configs and cloud code and many many other things in the environment our employers.

**\
Aaron Bockelie** 0:50\
You\'re running that daily, OK?

**\
Andrei Bosik** 0:59\
And about second year questions, we do not change your cloud config now. Maybe in future we made something changes, but now we use your cloud config.

**\
Aaron Bockelie** 1:09\
OK.

**\
Andrei Bosik** 1:16\
As you take, yes.

**\
Aaron Bockelie** 1:16\
Just as it is. OK, So what this conversation tomorrow is going to be is about beginning to add custom components to Cloud Code config and maintain a JVL specific branch instead of.\
Just cloning mine. So this is an integration question. Now the directory changes. What I would suggest thinking about is we can create a JVL branch inside of the cloud code config repo that you maintain.\
With the differences that at these new ways that we\'re planning on creating and then making sure that when somebody clones it, they\'re getting the integrated branch essentially, you know what I mean? So we keep the main main fork, the fork.

**\
Andrei Bosik** 2:05\
Mhm.

**\
Aaron Bockelie** 2:08\
The true fork from mine and then you maintain a JVL copy branch that you keep up to date with all the special JVL ways that I I expect you guys to start building.

**\
Andrei Bosik** 2:21\
But if you remember, we cannot recreate true fork from your repository because we use enterprise, but we have.

**\
Aaron Bockelie** 2:21\
That\'s all.\
Yes.\
Well, I don\'t actually. I don\'t want you guys to meet the content that I\'m that we want to talk about tomorrow would never make it back into my way system on my my copy. This is proprietary JVL ways.\
That we want to start implementing.

**\
Andrei Bosik** 2:52\
Mm-hmm. OK.

**\
Aaron Bockelie** 2:52\
So we have my original copy, then we\'re going to respect the the directory, the directory structure framework for ways, and we\'re going to add some of JVL\'s ways into that. And so then JVL people get this new hybrid of.\
My ongoing versioning of Waze and your integration of additional ways into it.

**\
Andrei Bosik** 3:16\
OK, but for now nothing to nothing to come to me and say we need to integrate something ways custom.

**\
Aaron Bockelie** 3:18\
That\'s it.\
Well, so tomorrow what we\'re going to do is I\'m going to pull you by the ear and I\'m going to say, come on Andre, we\'re going to make some new ways and I\'m going to show you how to decompose what Val has written currently into a set of ways.\
That will then be available for for experimentation and use.

**\
Andrei Bosik** 3:50\
OK, no problem. Our plan as I correct understand here our plan create a branch in our private repository and place here custom ways or custom.

**\
Aaron Bockelie** 3:59\
Mm-hmm.

**\
Andrei Bosik** 4:05\
Skills or something else in this branch. OK, no problem.

**\
Aaron Bockelie** 4:06\
Yes, yes. And then forever and ever, those ones will be JVL specific. They\'ll never make it back into my ways. And that means from that point forward, anybody who wants to use the JVL ways needs to use that branch that we\'re going to be integrating from from this point forward.

**\
Andrei Bosik** 4:25\
Mm-hmm. OK. But uh, as I correctly understand, uh, we can update uh.\
Juvet branch from our main branch because our main branch updated from your repository.

**\
Aaron Bockelie** 4:40\
Yes, you must. So I\'m going to continue building Waze, right. So and you need to be able to pull those new changes and improvements going into it. And as I continue to improve it, Waze is very stable right now in the sense of the how it functions.

**\
Andrei Bosik** 4:44\
Mhm.\
Mhm.

**\
Aaron Bockelie** 4:58\
And adding a whole body of additional ways special for JBL, that\'s an investment that you\'re making and I now am mindful that the ways pattern that I\'ve defined is very flexible and.\
If I make a breaking change to Waze at some point, it\'ll be in the version notes, just like any other software product is essentially. But right now I feel this is an excellent time to be for JVL to begin to create JVL custom ways or proprietary ways and start to use them.\
So tomorrow it\'s make sure we have the branch that we can then have literally in the session. I\'m gonna have you look have cloud code create these new ways based on this document that Val has. We\'re gonna commit them.\
Then we\'re going to test them out and see how they work.\
Just superficially, yeah.

**\
Val Levitan** stopped transcription
