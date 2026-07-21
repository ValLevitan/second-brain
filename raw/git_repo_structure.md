**Transcript**

16 September 2025, 12:03pm

**Val Levitan** started transcription

**Aaron Bockelie** 2:23  
Hey, guys.

**Pavel Frolov** 2:25  
Both.

2:26  
OK.

**Val Levitan** 2:28  
Good morning, Aaron.

**Aaron Bockelie** 2:44  
Oh.  
How's things? Are you done yet?

**Val Levitan** 2:48  
I'm hardly hearing you for some reason.

**Aaron Bockelie** 3:01  
Waiting for anybody else?

**Val Levitan** 3:06  
Is it only me or is everyone can hear?

**Aaron Bockelie** 3:09  
I can hear.

**Andrei Bosik** 3:12  
Oh, I see Aaron very, very quiet.

**Val Levitan** 3:17  
Very quiet.

**Andrei Bosik** 3:18  
Yes.

**Aaron Bockelie** 3:19  
OK.

**Andrei Bosik** 3:20  
What?

**Aaron Bockelie** 3:22  
Better.

**Val Levitan** 3:23  
Mm.

**Aaron Bockelie** 3:24  
I don't know. Is that good enough?

**Val Levitan** 3:26  
Yeah, now it's now it's better.

**Andrei Bosik** 3:26  
Yeah.  
Like it's that way that.  
OK, I sent in chat uh links to uh change plan.  
Uh, I place it in uh conference.

**Aaron Bockelie** 4:00  
Any reason the change plan isn't in git or git?

**Val Levitan** 4:04  
Aaron, I cannot hear for some reason.

**Aaron Bockelie** 4:06  
Not sure what's going on. My audio shows that I'm actually overdoing.

**Val Levitan** 4:18  
Right.

**Aaron Bockelie** 4:18  
Yeah.

**Val Levitan** 4:19  
Problem with me.

**Aaron Bockelie** 4:19  
Anyway, what I was wondering is, is there any reason? Let's we'll go through it, but any reason it's not in git why it's in Confluence?

**Andrei Bosik** 4:29  
But.  
No reason, just work with table in confluence more comfortable than in git.

**Aaron Bockelie** 4:32  
OK.  
I see.  
OK.

**Andrei Bosik** 4:45  
I place change plan into language rule and English because the big part of our developers Russian is more native language than English.

**Aaron Bockelie** 4:51  
Yes.  
OK.  
How are you going to track the progress of this change as you do it?

**Andrei Bosik** 5:50  
Um.  
I think we need to, uh, trust.

**Val Levitan** 5:54  
What? What's the? What's the question? What's the question? How are you gonna be tracking changes? If what?

**Aaron Bockelie** 6:03  
How are you going to track the progress of this change?  
As you do it, as you erform it, but this is a.  
Change plan and.  
It's quite large, so it seems to me you're going to update this document overtime because you're not going to be able to erform this entire change in one shot, right?

**Andrei Bosik** 6:31  
Sure. And then I type in these documents that we move step by step by organization, move one organization repositories, it renames these repositories.  
Uh, change Uh actions and some miles. Uh, then move second organizations step by step.  
Uh how?  
Sees the progress. I think we need to transform this change plans to JIRA features, JIRA stories.

**Aaron Bockelie** 7:26  
If we were to consider GitHub a project or the development environment, your product.  
We're changing some of the caabilities around in GitHub, right? And that GitHub caability has many different features.  
Of which two of them are probably the organizations, and in those organizations, there's a story for every single.  
Repo that needs to change, right?

**Andrei Bosik** 7:58  
Yes, as in my vision, one story, one organization.

**Val Levitan** 8:03  
Morning. How are you? Everything good with that extension card or? Yeah, just after you approved it. Oh, OK, yeah, yeah, because I submitted. He doesn't. I submitted something. Got it. I'm here.

**Aaron Bockelie** 8:04  
One story is 1 organization, so you're only gonna have two stories.

**Andrei Bosik** 8:08  
Yeah.  
No one current organization, 11 stories.

**Val Levitan** 8:17  
Mhm.

**Andrei Bosik** 8:23  
An additional story for prepare and the additional story for a review when I finish it all work.

**Aaron Bockelie** 8:35  
So I would give you some advice that you write stories for the structure you want it to end up, not the structure that it is.  
So in this case if you had.  
11 unique things to work on. On the other end, I would write 11 stories, but it sounds to me like you actually have far more repos than that, and so you need a user story for each repo because each one can be atomically changed.  
And convert it over. Otherwise what's going to happen is you're going to have one user story for several different repos simultaneously.  
I would prefer you have smaller units of work to get done because in this case, if they doesn't work, there's a problem. It's easier to back it out because you need to commit to the work being complete. If out of the three different, let's say 1 user story has.  
5 repos in it and one of those repos is not able to move for some reason at the time. Then the other repos that are related to that user story are not complete either.

**Pavel Frolov** 9:56  
So you suggest to create one story for one repo?

**Aaron Bockelie** 10:00  
I think that's the correct move because some of these repos are complicated and have to have their secrets changed around or action pipelines adjusted or dependencies adjusted and so forth.

**Andrei Bosik** 10:01  
Yeah.

**Aaron Bockelie** 10:14  
And you're making it too complicated by trying to bundle a bunch of user stories or a bunch of repos into a single user story.

**Pavel Frolov** 10:38  
Hmm.  
Oh, how many items do we currently have?

**Aaron Bockelie** 10:57  
Lan the whole roject out. All the user stories level items are your backlog.  
And if you were doing this correctly, I'm just going to say it out loud.  
The very first repo that you changed should have been your GitHub repo. The change org document should have been in there in docs, and you should have had a Jira or a GitHub project that tracked your user stories in GitHub.  
For managing GitHub itself and then JIRA would track the feature level item of shifting the away from the existing organization structures.  
This would allow the kind of the structure that Val's looking for, which is Jira contains the higher level items and the lower level items such as the user stories and the tasks underneath that would be tracked in GitHub.  
Additionally, if you track this in.  
You track this work in GitHub as a set of user story level items, a story item per per repo. Tools like Cloud Code can help you with the GitHub command line tool.  
To help move these over automatically for you and you can be done in a matter of a couple hours otentially.  
I'm just talking through how I would go about it.

**Pavel Frolov** 12:33  
Yeah.

**Aaron Bockelie** 12:38  
So.

**Pavel Frolov** 12:47  
Andrei, are you planning to do all this work, move repos by yourself or split this work?  
Give some developers to do this instead of you.

**Andrei Bosik** 13:05  
Move aye, but change actions is is developer work.

**Pavel Frolov** 13:15  
Mhm.

**Andrei Bosik** 13:21  
Rename and move. It's my work. Change dependencies. It's developer work because just he know what need to change. You know he's quoted what do this repository.

**Aaron Bockelie** 13:52  
Are you concerned with my suggestions? You feel that you have adequate description or uncomfortable with the way it is right now?  
OK.

**Pavel Frolov** 14:08  
Um.  
Andrei, are you comfortable to to create one story for one repo to move?

**Andrei Bosik** 14:31  
I think yes, if we uh not uh type any text by each story.

**Pavel Frolov** 14:32  
Or it should be.  
But it looks like the other head of fulfilling uh story description.  
In each particular repository movement is quite.  
Strange to Andrei saying that if it will be just a story with Riyappa XYZ moving to new organization and that's all. But if you fulfill all the story it it will be a a separate.  
Job.

**Aaron Bockelie** 15:19  
So.  
The purpose of, and we're not even really talking about user stories right now, we're just talking about a unit of work the size that it needs to be. I don't really call care if they're called user stories or tasks at this point. I do know that at the level of a user story.

**Pavel Frolov** 15:35  
Mhm.

**Aaron Bockelie** 15:39  
The story is, is that I will be using this git reo in another organization from where it was at before. That's kind of the story to tell.  
And when you do that, it's likely there's a bunch of tasks inside of there that Andrei alluded to already, such as I need to have a developer go work on this particular piece to move the actions over or to recommit this other thing or this other thing because the name changed.  
So each otential user story level item which is related to 1 git repo may have several additional tasks underneath it that have to be done or disatched by other people.  
If you create several repos to be moved under one user story, it makes it more difficult to coordinate everything.  
But I don't want to tell you how to coordinate. I'm just telling you how I would structure it if I was working on this is to make one user story per destination repo and I would do analysis on every single one of those.  
To make sure that I've clearly defined what I expect to have to do on those so they're estimated and I can structure it correctly.  
Once I've done the analysis and understood the requirements or dependencies of each of those repos, I would make sure that I get all the pre pre cursor the requirements done first, such as a resource or some other reference, and then I would go coordinate. I would sequence everything in that order.  
That's how I would approach it, but I don't want to impinge that on you because I'm not doing the work.  
This is what I've done in the past for this Tye of work.

**Pavel Frolov** 17:28  
Actually, I anticipate that about 80% of repositories will be just moved without changes in actions and only rest 20% will require some changes in actions, but it it could be.  
The wrong assumption, but probably.

**Aaron Bockelie** 17:52  
What about notifying the people that the repo's changed or moved?  
Because you have to remember there's a change management aspect to this, which is to tell whoever owns that repo that it's in the new spot for them.

**Pavel Frolov** 18:08  
In this approach, I think we are not so big company. We do understand that if we are moving such repositories that relates to Omni or Omni game.  
You know that the three person right now is working with this Ryopa.

**Aaron Bockelie** 18:30  
Mhm.

**Pavel Frolov** 18:32  
You can just inform start moving and then provide them access to new repo repo and try to review actions and check if it works.

**Aaron Bockelie** 18:33  
OK.

**Pavel Frolov** 18:49  
So it can be done within one day and I think it's not. It should not be a problem.

**Aaron Bockelie** 18:56  
Sure.

**Andrei Bosik** 18:57  
And for I I think informed by teams, I want to create a group with developers and where we can speak about this and informed by this.

**Val Levitan** 19:15  
OK.

**Aaron Bockelie** 19:21  
So how long do you expect this to take?

**Andrei Bosik** 19:34  
By developers one day to change it for each developers.  
For me, two days prepare all environment in GitHub at.

**Aaron Bockelie** 19:53  
OK. So just in general though, like let's say that we agree that this is a good enough place to start. When are you starting and when are you finishing? That's all I really want to know about.

**Andrei Bosik** 20:06  
Oh.

**Aaron Bockelie** 20:18  
Mhm.

**Andrei Bosik** 20:19  
It's two weeks, but it's not to work on this job. It's one day, for example, Sasha change in Omni. One day, for example, Serge change for CMS. One day it's another organization.

**Aaron Bockelie** 20:20  
Two weeks.

**Andrei Bosik** 20:37  
Another organization, for example graphics one day for him and.  
And go, go, go.

**Aaron Bockelie** 20:45  
In your estimate of two weeks, does that take into account everybody's schedule and interruptions and sort of time for messing around when undiscovered things are found?

**Andrei Bosik** 20:59  
No, not not all one time, just for little part developers.

**Aaron Bockelie** 21:07  
OK, so when will the when will all the other organizations be deleted?  
That's kind of the what I'm trying to get at is when will the other orgs no longer exist? That's kind of that's my that's my question.

**Andrei Bosik** 21:28  
Google three weeks.

**Aaron Bockelie** 21:31  
And do you? So are you guessing or are you showing me where it's at? So is the is there time estimates for these? Have you analyzed all the work?

**Andrei Bosik** 21:42  
Yeah, I uh typed this in uh change point this time.

**Aaron Bockelie** 21:51  
Right.  
I'm looking at the 10 item planning repository name. Have you identified which ones will just be a simple just rename and move and which ones are actually challenging?

**Andrei Bosik** 22:07  
And.  
Yes, uh, uh, sure. Uh.  
In 10 we type I type what which repository will be the name and which repository merge in which repository we need to change actions. It's additional information.  
I think developers know what we need, what they need to change in their.

**Aaron Bockelie** 22:39  
Thank you.  
OK, so I think the thing I'm trying to get at right now is that you should be planning per repo. You should be identifying for each repo the potential challenges that you have by actually looking at each one and surveying it and understanding before you commence your work.  
You should order the repos in the order that you plan on changing them, and you should be able to map them into the alignment with people to get each of the bits of work done. So if you have a requirement for a particular developer, make sure that you've got it scheduled out. Make sure that you have their attention.  
And working sessions to be able to get it done and then make sure that your project plan is all lined U that way because this is an important thing and you can't leave this hanging. You have to get it done as fast as you can.  
So that's my advice to you. Don't sort of don't float this. I have a very specific plan in place to make this get done.  
And anybody should be able to ask you how is it going? And you're going to point at a a list of JIRA issues or a spreadsheet or a Confluence page or a get page and you're going to say I am right here right now.  
That would be the precision that I would expect out of a DevOps team to move a bunch of git repos over.  
So let me story time. We're about 3/4 of the way complete and migrating Ford Motor Company. You might have heard them. They make some cars once in a while. They have 60,000 git repos that needed to be moved.  
I have a team of 12 or 14 people working on three different shifts across the globe to help them move it across the finish line. I'm not comparing you against Ford Motor Company, but I am telling you that every single git repo, when it got moved from one thing to the other, had a full plan to move it because it infected it.  
Affected people and some of those repos were just simple, just like the ones you have where nobody cares or knows what it does.  
But we did that, so we would make sure that we actually just didn't miss anything.  
So try to act big, but don't have to be big.  
Or in this case, act professional. You don't have to always do all the all the associated bureaucracy for it. Just make sure that you've got it planned. That's all I'm I'm telling you.

**Pavel Frolov** 25:22  
I I would add something. I think here we we can prioritize some movements keeping in mind that it's better to move all the repos that currently in progress.  
And make it as fast as possible to allow developers work with newly created repositories, repositories name. Probably half of currently existing repository is not in progress right now.

**Aaron Bockelie** 25:50  
Hmm.

**Pavel Frolov** 26:00  
But still important.

**Aaron Bockelie** 26:02  
Uh.

**Pavel Frolov** 26:05  
To check that everything after the move movement will work, we need to to check that action is working and nothing broken.

**Aaron Bockelie** 26:12  
Yeah.  
In a lot of ways, this is like moving file shares around, Andrei, to new paths and new servers, in that when you change them, something's going to depend on it and be broken.

**Andrei Bosik** 26:35  
Yes, yes, I agree.

**Pavel Frolov** 26:36  
Mm.

**Aaron Bockelie** 26:38  
And you need to be thorough in it.

**Val Levitan** 26:39  
Sorry, sorry, I would like. I would like to wrap up this meeting.  
But I do not understand the clear next step undertaking or schedule. So if we can nail that, I prefer to wrap up the meeting and move on.

**Pavel Frolov** 27:02  
Actually the the next step is quite clear for me. Andrei can make some some work related general work related to all repositories it will take about.

**Andrei Bosik** 27:15  
I start to prepare GitHub organizations. Yes, I I start to prepare organization, target organization, two target organizations. It's a first step, second step publish in group in chat.

**Pavel Frolov** 27:17  
Two days, yeah.

**Andrei Bosik** 27:34  
Table with current name.  
Future name or target name and and start work.

**Pavel Frolov** 27:47  
And then we we need a schedule for developers. For example, we need to inform and agreed with Efim, for example, that we are moving mass.

**Andrei Bosik** 28:01  
Uh, it's my.

**Pavel Frolov** 28:02  
Repos.

**Andrei Bosik** 28:05  
Efim him nothing to do with this repos just on the for me I need to change actions.

**Val Levitan** 28:05  
And.

**Pavel Frolov** 28:14  
Mhm.

**Val Levitan** 28:16  
Last time we made these key decisions.  
And this was the undertakings.  
So out of all these undertakings, I understand we only completed one. We created a real migration plan which lacks a solid schedule from what I understand.  
We did not collect all repository settings and secrets.  
And we did not propose migration or order and depend.

**Pavel Frolov** 28:59  
Mm-hmm.

**Val Levitan** 29:00  
Unless AI misinterpreted something.  
For Tuesday, Andrei was supposed to collect all repository settings and secrets. So is it done?

**Andrei Bosik** 29:40  
Oh.  
I think uh.

**Val Levitan** 29:43  
I circulated this together with the new nation.  
You committed to that. You said yes, I will do it for Tuesday. Yes, isn't that?  
It was your schedule, I I told you. I'm not going to pressure you for schedule.

**Andrei Bosik** 30:02  
And all all settings and secrets not all collected because they duplicate in other organizations.  
But partly, yes, I think.  
Migration and other conceptions in the change plan. Yes, I I add add this part in migration plan.  
Paul.

**Val Levitan** 30:29  
OK, so if all of it is done, which?  
I cannot judge whether it is or it isn't.  
Let's develop the next milestone. I'd like to check back in a week. So what can we achieve in a week?  
But.

**Andrei Bosik** 30:53  
I can can prepare uh GitHub uh environments uh in target organization.

**Val Levitan** 31:03  
Well, I think it's too little in one week. I mean, this is.

**Andrei Bosik** 31:07  
Sure, it's a 1-2 days for me. Next step we need to move and rename repositories.

**Pavel Frolov** 31:17  
She.

**Andrei Bosik** 31:24  
Well, could you please speak with developers and add to their work this job? I think one day per organization per organization is enough.

**Pavel Frolov** 31:39  
Mhm.  
The you mean to or to describe new approach to naming and advice them to?  
What start moving or to check after your move?

**Val Levitan** 32:02  
I I feel, I feel like you are frozen. Is there anything on your mind like anything that is?  
Is there anything going internally that?  
That I need to be aware of because something it feels like you are stuck.

**Pavel Frolov** 32:30  
I think Andrei is ready to start this work, ready to to rename.  
And don't want to continue philosophy and.

**Val Levitan** 32:51  
We're not philosophy, we're developing a plan and we want to have a schedule and we want to know what is the set of deliverables for next meeting.  
Can I please understand what is the set of deliverables for next meeting?  
1.

**Pavel Frolov** 33:25  
I would say let's schedule a meeting in two weeks and let's review result of movement.

**Val Levitan** 33:38  
I appreciate this, but I think it's a wrong plan.  
I I do not want to do that.  
For a number of reasons, because going into this these two weeks, the plan is washed out. I don't understand what the result will be.  
And #2 I don't like to leave things for two weeks because I a lot of things will get we will arrive to, we will arrive to the next interval and things are not done.  
And the two weeks will be wasted. So I would like to go maximum a week, but I prefer a few days. For me ideal is to check back on Friday and I would like to have a set of.  
Undertakings that will be done on Friday. Can we do that?

**Pavel Frolov** 34:44  
Yeah, I think until Friday, Andrei already will finish first step of his plan.  
To create.

**Val Levitan** 34:58  
First step, first step of this plan. Can we just verbalize what that what that is?

**Pavel Frolov** 35:05  
It relates to create creation of new organization, create secrets and parameters.  
That will be necessary for all repositories, yeah, and they is not.

**Andrei Bosik** 35:23  
No, no, no, no. Create new organization. We take current organization with the most biggest number of repositories and environments and renames this organization.  
And then move to this organization and other repositories from another organization.

**Pavel Frolov** 35:45  
It's not the first step.

**Andrei Bosik** 35:47  
No, it's not first step. First step is to prepare environment for this move for secrets, move environment.

**Pavel Frolov** 35:53  
What? What is? What is included into environment?

**Andrei Bosik** 36:00  
Uh, secrets. Uh, parameters. Uh.

**Pavel Frolov** 36:10  
And until Friday, we can propose an order of repositories in in which order we are going to proceed.

**Andrei Bosik** 36:22  
I think yes.

**Val Levitan** 36:24  
Sorry, sorry, today is Tuesday. You're saying that Wednesday, Thursday and your day, end of your day Friday. So three days you will as a result of this, you will propose.  
The order of movement.  
Or I misunderstood or I misunderstood something.

**Pavel Frolov** 36:48  
It's a point number, point number two, point number two, point number one to create environment.

**Val Levitan** 36:58  
But how long does it take to create environment? According to Andrei, it's hours.

**Pavel Frolov** 37:03  
Two days.

**Andrei Bosik** 37:05  
No, it's not our.

**Pavel Frolov** 37:05  
As I understand, it was 2 days.

**Val Levitan** 37:12  
OK, so the undertaking for Friday is to create.  
The environment. I don't know what it means. Can somebody spell it out for me?  
Aaron, do you understand what it means? Can you eloquently explain what it is?

**Aaron Bockelie** 37:29  
I don't quite understand what.  
Without breaking it into the smaller pieces, it's very difficult for me to understand how long it takes for things to get done.

**Andrei Bosik** 37:44  
I I can show what I mean. For example, I share my screen one second.

**Pavel Frolov** 37:44  
Andrei.

**Andrei Bosik** 37:52  
For example, if we go, we go to.  
Some organization, for example, or we can see here.  
Um.  
Example secrets. I need to move all these secrets to 1 organization.  
Variables need to move one organization and they need to do it's from all organization to one. It's a first step. Second, for example, we have a runners.  
Uh, we need to move to add uh access to this rhinos. Uh.  
A second I can show.  
And.

**Aaron Bockelie** 38:56  
So you know there's. How are you going to move those secrets over?

**Andrei Bosik** 39:06  
Create with same name the secrets in GitHub and variables because this secret this name of secret of variables is currently used in actions.

**Aaron Bockelie** 39:34  
So you're going to.

**Andrei Bosik** 39:34  
Example use runner on some representorious uh.  
And uh, for example, we use uh.  
I'm not remember where is it's. We use GitHub applications for use some repositories and submodulus and we need to use.  
GitHub applications to build uh.  
Just ******.  
But remember where it's a place.  
Oh, yeah.  
We need to reassign this.  
Oops.

**Aaron Bockelie** 40:30  
Right. So this is that per repo analysis, right? That has to happen.  
Open.

**Andrei Bosik** 40:39  
And uh, prepare, prepare environment.

**Aaron Bockelie** 40:45  
So there's a code repo that somebody created called GitHub Organization Secrets migrator that lets you just basically you would add the action, it collects all the secrets into a bundle and then you run it on the other end and it moves all the secrets over.  
It makes it go really fast.  
Do you plan on using tools like that?

**Andrei Bosik** 41:16  
I'm.

**Aaron Bockelie** 41:17  
Let me send a link to you.  
Here, just as an example, I don't. The last time I used it personally was about a year ago, so I don't remember if that's the actual original copy of it, but it's just basically it's it.

**Val Levitan** 41:43  
1.

**Aaron Bockelie** 41:51  
Uh.  
Is that the right one? Sorry.  
It's around here somewhere.  
There's several different tools that are named like that.  
Just search for GitHub Secrets Manager Migrator basically.

**Pavel Frolov** 42:20  
Mm.

**Val Levitan** 42:24  
1.

**Pavel Frolov** 42:25  
Oh um, can we use uh some MCP?

**Aaron Bockelie** 42:31  
No, you wouldn't. What? No.

**Pavel Frolov** 42:32  
No.

**Val Levitan** 42:35  
1.

**Aaron Bockelie** 42:37  
You don't. You don't want to send your secrets through a language model AI.

**Pavel Frolov** 42:41  
Yes.  
Just names.

**Aaron Bockelie** 42:48  
That's kinda not how that works. Um.

**Pavel Frolov** 42:51  
Yeah.

**Aaron Bockelie** 42:53  
Maybe it's worthwhile to spend a little bit of time researching the the techniques for migrating between organizations in GitHub Enterprise on cloud. There are many automation tools available to do this.  
Just trying to find where it's at.  
Looks like it got deleted, but I found the original author here, so there's the authors.

**Val Levitan** 43:40  
1.

**Aaron Bockelie** 43:57  
Anyway, I don't want to turn this into a technical discovery session. I think you need to really consider.  
How are you going to migrate them efficiently? Are you really going to go out and search all your secrets one by one and retype them all? How are you going to do this? Basically, this is what a runbook actually looks like. This is what a per repo change starts to look like too.

**Val Levitan** 44:07  
1.

**Aaron Bockelie** 44:22  
It.  
I'm just a little frustrated why it seems to have been deleted just recently. Like literally I used it earlier in the year.

**Pavel Frolov** 44:47  
Mm.  
Actually actually I I suggest to use just GitHub CLI is some command to to get list of all secrets.

**Aaron Bockelie** 45:04  
Right, but that doesn't give you the secret itself. The trick is you have to extract them out into a file and then write it out and then encrypt it and then move it over.

**Pavel Frolov** 45:14  
Mhm.

**Aaron Bockelie** 45:14  
That's what this tool did.

**Andrei Bosik** 45:17  
Yeah.  
Aaron, right.

**Aaron Bockelie** 45:34  
So.  
Like I'm saying, come U with a migration path that actually lists all the steps. This will help you understand how long it's going to actually take.

**Pavel Frolov** 45:46  
OK.

**Val Levitan** 45:47  
Andrei, can you please say it in Russian eloquently in a well produced sentence that it makes sense?  
The plan.  
The undertakings for Friday. What will we get on Friday?

**Andrei Bosik** 46:30  
Нет.  
Это можно сделать в пятницы как 1 шаг, так же к пятнице можно распределить.  
Наверное, по дням будет вместе с пашей, чтобы это было более корректно. Кто из разработчиков когда сможет?  
Заняться?  
Изменениями в своих уже репозиториях.

**Val Levitan** 46:53  
Ну то есть создать план на будущее на следующую неделю.

**Andrei Bosik** 46:57  
На ближайшие на ближайшие. Ну он будет включать в себя план 2 недели, поскольку у нас 11 организации. Если брать, что за один день мы планируем перенести одну организацию, то это получится как раз 2 недели.

**Val Levitan** 47:08  
План план на последующие 2 недели.

**Andrei Bosik** 47:11  
Да.

**Pavel Frolov** 47:11  
Ну там я бы добавил, что не совсем это должно быть привязано к организациям. Есть проекты, которые цепляют 2 организации там или даже 3.

**Andrei Bosik** 47:21  
Да тоже есть.

**Pavel Frolov** 47:23  
То есть вот их желательно в один период делать перенос.

**Andrei Bosik** 47:28  
Да.

**Val Levitan** 47:29  
Окей.  
Окей, санью.

**Pavel Frolov** 47:43  
Mm-hmm. OK. Thank you. Bye.

**Andrei Bosik** 47:44  
OK. Bye. Bye.

**Andrei Bosik** stopped transcription