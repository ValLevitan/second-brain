**Transcript**

12 September 2025, 12:06pm

**Val Levitan** started transcription

**Pavel Frolov** 0:30  
If.

0:38  
Oh.

**Val Levitan** 0:46  
Can you zoom in please?

**Andrei Bosik** 0:53  
It's OK.

**Val Levitan** 0:55  
If possible, more please, if possible.

**Andrei Bosik** 0:56  
More.  
OK.

**Val Levitan** 1:10  
The the columns are too wide. You could shrink them. They you don't need such wide.  
OK. Can you increase now?

**Aaron Bockelie** 2:40  
So in the description of work over here on column I.

**Pavel Frolov** 2:44  
She.

**Aaron Bockelie** 2:47  
It seems like there should be a lot of duplicate kind of things just to make make it easy to know like.  
This first one platform Omni framework land base.

**Val Levitan** 3:13  
Sorry, not clear.

**Aaron Bockelie** 3:16  
Um.

**Pavel Frolov** 3:31  
Actually, I think it's better to to describe this work in general, not particularly for each repository, because in most cases it will be the same, right?

**Aaron Bockelie** 3:32  
O.  
Yeah, so. So I think The thing is, is that you could copy and paste this. This one also makes sense here, right?  
So I'm I'm not trying to look for bespoke descriptions on every single one, it's just, but you will have some unique things that have come up.

**Pavel Frolov** 3:51  
Yes.  
In in general discussion this with Andrei, we agreed this that first of all Andrei will need to collect all.  
All parameters that used for different actions, especially secrets to understand that we need to support the same names on you.  
Uh, organization.  
And then we need to understand that those actions.  
That use.  
Code named uh runner self hosted runner.  
We need to specify this for repositories that will be created.  
And then we can start moving and check if all the actions correctly produce artifacts and in some cases fix dependencies and so on.

**Aaron Bockelie** 5:21  
O.  
Essentially what you're doing is transferring the organization as well as renaming it. That's that's kind of what's going on here.  
I also would suggest what you do, Andrei, is you start to build a runbook based on the GitHub documentation. So for example, here's creating and managing repositories right here. I moved. I went over a couple of columns to the right just to keep it out of the way.  
Transferring a repository, you'll have to.

**Pavel Frolov** 5:56  
Transfer or just use some organization.  
That we already have rename it because it already contains lots of settings that we will not need to fulfill again.

**Aaron Bockelie** 6:15  
Yeah, if you want to, I mean pick the one with the most amount of repos that you just need to be renamed. That's fine. I'm I'm not trying to prescribe exactly how to do all that.

**Pavel Frolov** 6:19  
Yes.  
Mhm.

**Aaron Bockelie** 6:29  
The other thing you need to really think about is which features you're going to be enabling, and one of the few that you're going to start with is to have issue tracking needs to be enabled and project tracking needs to be enabled for all projects. Don't disable that stuff.

**Pavel Frolov** 6:46  
I'm not sure that I understand this. Probably I've never.  
Patagis.

**Aaron Bockelie** 6:53  
If you go into a GitHub repository for JVL, most of it's disabled.

**Andrei Bosik** 6:55  
I know about speak. This is GitHub included in GitHub actions which try found secrets in court vulnerability.

**Pavel Frolov** 6:56  
8.

**Andrei Bosik** 7:11  
Do you need this?

**Aaron Bockelie** 7:13  
No, if you go into a GitHub repo, there is literally a thing called issues.  
And you've disabled deactivated that for many of the repos.

**Pavel Frolov** 7:20  
Uh, mm-hmm.  
Are you able to post issues directly to GitHub instead of Jira you mean?

**Aaron Bockelie** 7:35  
Yes, you've deactivated many of the settings for these.

**Pavel Frolov** 7:37  
Mm.

**Andrei Bosik** 7:37  
Oh.  
Uh.

**Pavel Frolov** 7:41  
OK.

**Andrei Bosik** 7:43  
Is this and this?

**Aaron Bockelie** 7:44  
Uh-huh. And projects and discussions.

**Andrei Bosik** 7:48  
Uh, projects. Oh.

**Aaron Bockelie** 7:50  
Scroll down more, there's more.

**Andrei Bosik** 7:54  
Mm.  
OK, I need to enable this to global level and discussions, yeah.

**Aaron Bockelie** 7:58  
Yeah, you you disabled a lot of stuff.

**Val Levitan** 7:59  
And the.

**Andrei Bosik** 8:03  
OK, I can do it. Uh.  
OK, I I enable this slide. OK.

**Aaron Bockelie** 8:29  
I mean if.  
If you feel like the names are all valid based on the patterns that we have, I don't think we need to go through every single one of them.

**Pavel Frolov** 8:47  
Uh.

**Andrei Bosik** 8:50  
We have a proposition with Pasha create the category maybe are here because we have repositories with code which we do not use now, but we want to save this code for future moment.

**Aaron Bockelie** 9:06  
No, you're not going to use that. You're going to just archive the repository using the GitHub method for archive.

**Andrei Bosik** 9:11  
I know about this method, but when we have a repository and it happens, this repository just set is read only, but he is not hidden from the list.

**Aaron Bockelie** 9:24  
So.  
I highly dislike it when you when not you, the royal you, when anybody adds things to a name that's literally a feature capability of a product in general, right? It's very frustrating to see that.

**Pavel Frolov** 9:38  
Different suggestion, different suggestion to create an organization where we can move obsolete code.  
As it's currently not in use, but probably we need to refer it.

**Aaron Bockelie** 9:57  
I would prefer you don't even use GitHub as a backup strategy. I would prefer you back it up and get rid of it off of GitHub. It's a liability to have it up there if it's truly not used.

**Pavel Frolov** 10:12  
But again, this is the best place where we can store sources. So you're saying you can use something else.

**Aaron Bockelie** 10:19  
Right, but what I'm.  
What I'm saying is if it's truly archived, you don't need it anymore. It is irrelevant code and can be gotten rid of.

**Pavel Frolov** 10:31  
Highly likely for some of the repositories, we have a source code that's built into a binary committed to artifact storage and used right now.

**Aaron Bockelie** 10:41  
Yep.  
Right.

**Pavel Frolov** 10:47  
And probably will not be changed for several years, but what if we need changes in this repository in two years?

**Aaron Bockelie** 10:54  
OK.  
Then you should be. Then you should be maintaining the code and it's not archived.

**Pavel Frolov** 11:06  
It it it will exist as a big list of repositories that always will looks like a mesh.

**Aaron Bockelie** 11:14  
Then you should figure out why that is like that and put it into one of the active repositories then.  
Like it doesn't. What you got to get away from is this idea that old code can't be touched.  
If it's if it's living code, then keep it alive and don't don't put it in a in the freezer.

**Pavel Frolov** 11:39  
Uh, why having a different organization?  
Uh is the worst case.

**Aaron Bockelie** 11:51  
Oh.  
OK, let me let me tell a quick story. The Unix command copy CP. OK, the source code for it was feature complete in the mid 90s and yet.

**Pavel Frolov** 12:01  
Mhm.

**Aaron Bockelie** 12:08  
We keep a live copy of that code, constantly updating it and just making sure comments work and that it always builds and stuff. Therefore it's still living even though the code base hasn't changed.  
O.  
In your situation, you have something that was perfection five years ago and has never been built again.  
You should be maintaining the actual build pipeline and the ability to rebuild that code at any time. Therefore the repo isn't isn't obsolete or or archived.  
As soon as you, as soon as you say, uh, we'll put it on archive and we'll just leave the binary and we'll not worry about it for a couple years, you put yourself at risk of not being able to build rebuild it again in the future.  
Have to be able to source your stuff.

**Pavel Frolov** 13:04  
Um.  
Aaron, I am OK to have additional repositories in our general organization. It's not a problem. Just try to explain when we will have 200 repositories, it will be a little bit meshing.

**Aaron Bockelie** 13:13  
Yeah.  
And if you if you do have 200 repositories and it's overwhelming, this is a strong signal that you need to under to try to maybe fix it. You have too much complexity.

**Pavel Frolov** 13:37  
Mm.  
This is a additional overhead.

**Aaron Bockelie** 13:42  
I don't. I don't think it is. I think it's just actually calling out reality for what it is.

**Pavel Frolov** 13:43  
It's.

**Val Levitan** 13:48  
It's like it's like never cleaning your desk.

**Aaron Bockelie** 13:51  
Right.  
It's like accumulating debt and just saying it's OK.  
Own it.

**Pavel Frolov** 13:59  
But the strategy, if we understand that the some repository is not updating for years just to move it to archive organization.  
And we will easily clean as the main organization.

**Aaron Bockelie** 14:23  
I'm not. I I think it would be better to maintain all your work centers as functionally viable rather than to abandon one and say that it's archived.  
I'll leave that final decision up to you, but I'm strongly suggesting that you make sure that you have every bit of code that you use, even occasionally, as something that keeps it alive and and is able to build.

**Pavel Frolov** 14:56  
It will be still be able to build from a archive organization.

**Aaron Bockelie** 15:04  
But it's not archive if you're needing it.

**Pavel Frolov** 15:07  
OK, let's assume that this will be a different name for organization.

**Aaron Bockelie** 15:15  
So what would this? What does this thing do?

**Pavel Frolov** 15:22  
Just long term storage, source storage.

**Aaron Bockelie** 15:33  
I don't understand why it's not just part of the regular source repo list.

**Pavel Frolov** 15:43  
Because we want because I want to remove it from the main list of active repositories.

**Aaron Bockelie** 15:43  
Why is it archived but also being used?  
So why don't you just change the permissions?

**Pavel Frolov** 16:01  
I'm OK, I'm OK to to to have this bigger list because I will not see all the list. Only Andrei will see full the full list, but I anticipate in some years to return back to the to to this discussion.

**Aaron Bockelie** 16:20  
Well.  
Part of this is managing your tool chain, your supply tool chain. What you're talking about is something that is an old piece of code that hasn't been touched in a long time. It's still relevant that you still maybe build fresh if you need to, but it's still.  
There it's still something that you have to have, and at anytime you should be able to consider what else can we do with this tool.  
If I if I build aircraft and I have a tool jig for building the wings on an aircraft that I've been building for the last 40 years.  
I don't just roll that jig into the into the storage unit and bring it out occasionally, I maintain it.  
It's the same thing. You have tooling structure that has to maintain whatever it is this code is contributing to.  
And this this process consumes available resources at the company when it comes time to hold on to it and use it.  
There's you have to have an owner of that code, for example, because if somebody said if if Pavel leaves and you're the only one that has this this particular archived thing, what happens to that code? It it becomes irrelevant without Pavel anymore.  
If you're the only one who knows it from, I'm just bringing up an example. I'm not saying it's you, I'm picking a name and then it has lost all residual value and investment if it's part of the regular herd of code of projects that you maintain and operate.  
Then it remains in the general population and is circulated and kept up to date.  
For instance, I would expect to have Dependabot connected to all of these. So Dependabot is looking at the code and suggesting to keep the thing up to date and and fresh.

**Pavel Frolov** 18:23  
8.

**Aaron Bockelie** 18:23  
If you truly want to freeze the code in time, the longer it sits like that, the harder it is to resurrect it when a time comes to use it again. And if you are holding on to it for a really long time, is it really valuable?  
I understand the the need and desire to hold on to lots and bits of code and pieces, but also it causes things to slow down too.  
I'm not gonna force you to say no, you can't, but.  
I I strongly believe that it it's not optimal to do this.

**Pavel Frolov** 19:13  
Again, I'm OK to continue on as as is.  
But I I do sure that we will return back to this question in the future in some months or in some years.

**Aaron Bockelie** 19:29  
OK, so so let's just talk about that warning for a minute. So basically what you're concerned is, is that one day you're going to realize there's 600 repos in in JVL's environment, right?

**Pavel Frolov** 19:42  
Yes.

**Aaron Bockelie** 19:44  
So why did it get to 600 repos?

**Pavel Frolov** 19:49  
Because actually it relates to different application.

**Aaron Bockelie** 19:54  
And do you really have?

**Pavel Frolov** 19:54  
We do not want to put put to put this application internally within any other repository. For example, it really represents a different product.

**Aaron Bockelie** 20:08  
Right. It feels to me like that's a failure to retire old products that aren't being used.  
Or failure to understand how to maintain the products in a way that is is economically valuable.  
If I held on to every, if I could somehow have held on to everything I've ever produced my entire career, it would. I would spend the majority of my time wading through it and dealing with it. The problem is, is that I don't need most of it.  
So I don't keep it, I just get rid of it.

**Pavel Frolov** 20:49  
Yes, in in assumptions that this project to product.  
Will will not be reused.  
I agree.

**Aaron Bockelie** 21:01  
So So what you do then is instead of keeping it in GitHub, and GitHub is not a backup strategy, you make an archive of it, put it to tape or to somewhere else and remove it from the platform.  
If you really, really need it, you can go back and get it. You could maintain a simple list in GitHub that says this repository has been retired to here.  
And it's offline.  
This is a IT governance question in some ways as much as it is a engineering architecture problem.

**Pavel Frolov** 21:52  
OK, let's move move on.  
So actually we agreed internally that some of the repositories will be joined or merged into a bigger.

**Aaron Bockelie** 22:12  
OK.

**Pavel Frolov** 22:14  
Example local gaming server and omni local gaming server with utils will be moved on the same repository.  
What else? The same for Flex POS Flex pay to to merge modules related to graphic user interface into the main repo.

**Aaron Bockelie** 22:47  
K.  
Did you guys switch the file to another?  
No repo naming. OK, I was looking under the repo naming tab. I noticed there was still some items that were crossed out and controller for example on if you go to the repo naming tab.

**Pavel Frolov** 23:10  
Oh, forgot to to fix. Mm-hmm. Mm-hmm.

**Aaron Bockelie** 23:11  
There was there was some strangeness over there.

**Pavel Frolov** 23:16  
Mm-hmm.

**Aaron Bockelie** 23:17  
Is that supposed to be like that?

**Pavel Frolov** 23:22  
No.

**Aaron Bockelie** 24:37  
So on your planning list I noticed that on rows.  
79 through 86 Roughly, there's a bunch of knowledge.  
Repo names there and are you going to merge all those into just one thing called knowledge?

**Pavel Frolov** 25:03  
Mm.  
Seems no, but at least at least we will need to support different access rights to some of them.

**Aaron Bockelie** 25:04  
What's the goal here?

**Pavel Frolov** 25:13  
I actually, I think most of them can be merged.  
But for example, Canada Border Services Agency looks like it should be a private access for some person only.

**Aaron Bockelie** 25:33  
Val, do you even need that CBSA git repo there? Are you sharing it with other people?

**Val Levitan** 25:38  
No.

**Aaron Bockelie** 25:39  
Let's just delete it.

**Pavel Frolov** 25:40  
Mm-hmm.

**Andrei Bosik** 25:44  
What about another yellow repositories?

**Aaron Bockelie** 25:50  
Seems to me they should all go together.

**Andrei Bosik** 25:53  
How about personas? It's a part of.  
Casino management site or or what?

**Val Levitan** 26:03  
The persona. The persona we should. Yeah, it's general. We should keep it.

**Pavel Frolov** 26:06  
It's a general.  
So everything related to knowledge, knowledge base, I think we will move just to knowledge and organise it internally by directories.

**Aaron Bockelie** 26:23  
Yeah.

**Pavel Frolov** 26:24  
OK.

**Aaron Bockelie** 26:26  
You can continue to build that into a git book or other documentation system.

**Pavel Frolov** 26:32  
Mhm.

**Val Levitan** 26:33  
I think, I think we discussed.  
Uh.  
That knowledge.  
Or the word knowledge should probably.  
Be part of every repository.

**Aaron Bockelie** 26:56  
Right.

**Val Levitan** 26:56  
So maybe this repository should not be called knowledge, but rather something else.

**Aaron Bockelie** 27:03  
So I wouldn't call it just knowledge. It seems to me that there is um.  
Conversations about GitHub between the sandbox repo, get practice template and DevOps architecture. So if you have under your main areas you have platform.  
Is is there a platform for GitHub under your repo naming convention?

**Pavel Frolov** 27:36  
It's enabled name, but don't think that actually we need this repository.

**Andrei Bosik** 27:36  
No.

**Aaron Bockelie** 27:45  
How are you going to manage GitHub?

**Pavel Frolov** 27:52  
Mm.

**Aaron Bockelie** 27:56  
By clicking on stuff or by programmatic methods.

**Pavel Frolov** 28:03  
Uh.

**Aaron Bockelie** 28:03  
For instance, where would the repository validation tool that I I mocked up be stored?

**Pavel Frolov** 28:10  
Andrei suggested to create tools services repository that mostly he will manage and put all the scripts that he need to automatically or half automatically manage repository.  
Tourists manage some services, virtual machines, I assume under this repository.

**Aaron Bockelie** 28:37  
Yeah.  
But if you have a subcategory, all these subcategories are big things like platform style or product style things.  
So my thinking is is that you can put it the word tool under component, but you can't really put it under a subcategory level.  
You go back to the repo naming tab.

**Pavel Frolov** 29:02  
Actually right right now we have tools on category level, not subcategory even.

**Aaron Bockelie** 29:10  
OK.  
So so tools GitHub.

**Pavel Frolov** 29:15  
OK.

**Aaron Bockelie** 29:19  
Or just tools.

**Pavel Frolov** 29:21  
Tools services suggested by Andrei.

**Aaron Bockelie** 29:29  
But services is not a valid sounding subcategory.  
Services is a word that's too generic. I mean, I know you've got it, but it says repositories containing helm charts and configurations for deploying and managing versions of AWS.

**Pavel Frolov** 29:47  
Mhm.

**Aaron Bockelie** 29:49  
So are you going to use a helm chart to manage GitHub? Probably not.

**Andrei Bosik** 29:56  
No.

**Aaron Bockelie** 29:58  
So realistically, it's.  
Tools GitHub.  
I would also expect you to have under subcategory here probably Tools Atlassian.  
If you wanted to rogrammatically manage Alaskan stuff, for example, or Office or Microsoft or whatever.

**Pavel Frolov** 30:18  
Mhm.

**Aaron Bockelie** 30:20  
But I don't. I'm not trying to tell you to make a bunch of repos, I'm just saying it might all just fit under a repo called tools.

**Pavel Frolov** 30:33  
Andrei, are you OK to have just only tools or can we split it to tools GitHub?

**Andrei Bosik** 30:46  
I think it's will be different because it does because tool service is private repository with restricted access, but for example GitHub now this is good practice.  
This is a repository which include manuals and scripts for configure personal computer to work with GitHub and and tools for work with GitHub.

**Pavel Frolov** 31:14  
3.

**Aaron Bockelie** 31:18  
I have a question about maybe this gets solved if we swap the AWS category into a subcategory. So instead of AWS something, it's platform AWS.

**Pavel Frolov** 31:21  
Good.

**Andrei Bosik** 31:33  
I do AWSS category because I need to have in my name repository for which product this repository is.  
Related TS.

**Pavel Frolov** 31:50  
Deleted.

**Aaron Bockelie** 31:52  
And so inside of a, let's hypothesize for a minute a platform AWS repo just for just for the sake of discussion.  
Would it not be possible to then just have a bunch of of subdirectories inside the repo for per product for configuration?

**Andrei Bosik** 32:10  
It's not good. Yes, I can do it, but it's not good because some services start to work slowly when repository is very big.

**Aaron Bockelie** 32:29  
OK. So my next question is, would it not make sense to then just put the pipeline actions and necessary infrastructure into the product itself? So for example?  
Uh.  
Casino management system just has the AW components built right into it, so you don't have to manage them separately.

**Andrei Bosik** 33:01  
No, I didn't show you why.  
For example, one second.  
Uh, if I open uh.  
My repository with for game deployment. I have all game in one repository because I have a common part. I have a template part. This is common between all games and I have deploy.

**Aaron Bockelie** 33:19  
M.

**Andrei Bosik** 33:33  
Yeah, well, uh, for as uh uh.  
So for us environment with different list game and if I do it for each games I need to copy templates, copy common and and I do not have deploy.

**Pavel Frolov** 33:40  
Environment.

**Aaron Bockelie** 33:45  
OK.

**Andrei Bosik** 33:57  
This is back to each environment.

**Aaron Bockelie** 34:01  
All right, so going back to get the the the go back to your repo again, please.

**Andrei Bosik** 34:09  
Oh, in the one SEC here, yeah.

**Aaron Bockelie** 34:12  
VS Code, Yeah, so scroll U to the top. So we have games, right?

**Andrei Bosik** 34:19  
Yes, it's a representory games.

**Aaron Bockelie** 34:22  
What other at that level do you have?  
Collapse of games. Let's assume that you have games, you have cluster, you have alications. What else is there?

**Andrei Bosik** 34:32  
It's not a repository. You can you it's.  
It's not a repository.

**Aaron Bockelie** 34:40  
Well, I'm trying to understand your organization structure that you've got even in here. Like everything's, everything's open for understanding here. So close up games. Do you have anything below games?  
What else do you have at that level?  
No, just.

**Andrei Bosik** 34:58  
I open this repository with games just to clear one second.

**Aaron Bockelie** 35:00  
Just close.  
But.  
I don't want to see just games go back. I want to see everything that was at the games level. Stop hiding that.  
OK, right there. Applications, clusters, CMS games, Omni, Power AI services and Vivian.  
It seems to me that you could have a platform AWS and then this is inside of that sub that get repo.

**Andrei Bosik** 35:53  
In one repo.

**Aaron Bockelie** 35:55  
In a repo called Latform AWS.

**Andrei Bosik** 36:00  
As I say, some services start to work slowly. That's the first second. For example, this is deployed, but this is not deployed, this is.  
Terraform could spray and another Ansible another tools for create cluster and management cluster.

**Aaron Bockelie** 36:26  
Right. But there's still, but there's still configuration that should be managed, right?  
So the fact that you have an archive folder there is really interesting. Go back to that folder that you had.

**Andrei Bosik** 36:41  
Yeah, I have forgot, yes.

**Aaron Bockelie** 36:41  
What's an archive?  
Why do you have an archive folder in here?  
Because you don't have version control, right?

**Andrei Bosik** 36:50  
It's a test, it's a test application, so part of my code which I need to when I create the cluster. But now I don't use this and I move this to archive for because I don't watch this in my.  
Now this is not comfortable for me work when I have folders which are not not needed for me now, but maybe this is.

**Aaron Bockelie** 37:12  
Right.  
But if you but what I but now what I'm getting at go back up to the levels again. I I dislike that we're working. We're navigating in the file the open folder open this open go up one.  
Go up to the cluster, yeah.

**Andrei Bosik** 37:31  
Uh, up.

**Aaron Bockelie** 37:36  
One more. No, keep going up. Sorry, up.

**Andrei Bosik** 37:36  
This is cluster.

**Aaron Bockelie** 37:42  
Open the AW folder.

**Andrei Bosik** 37:44  
It's a. It's a AWS folder.

**Aaron Bockelie** 37:47  
OK, open this folder. Let's open this folder. Don't. I don't want to navigate in the open folder dialog. It's it's uncomfortable.  
Push push open folder right now.

**Andrei Bosik** 38:00  
Uh.

**Aaron Bockelie** 38:03  
Thank you. OK, that's the view I want to see. All right. So imagine in this situation you have a platform AWS git repo, all right? And you have a you actually are doing version releases of your platform AWS.  
At this point in time, this is the current latest version of the platform AWS system for JVL. Just let's just hypothetically say it's version 9.27.  
When you decide that that thing under the archive, those items, let's say they weren't archived yet, but you said, you know, I just need to get rid of these. They're not used, they're experimental or whatever. You would just literally delete them from the repo and you would commit the changes and you'd tag a new version of the.  
AW platform and if you ever wanted to go back in time, you'd go find the older version of your AW platform and there's your files again.  
So what I'm getting at here is I think that you could probably structure this as platform AWS and have all of the concerns for a WS right here like this and manage versions of it in this space.  
This is tying together the whole concept of the AWS platform into version management rather than kind of treating them outside of version control. Now what happens is that when you have say.  
A game deployment you can say you can target all of the the infrastructure for your game. So open U games for a minute.

**Andrei Bosik** 39:45  
I don't agree with you. No, I I can. You need to know.

**Aaron Bockelie** 39:48  
Yeah.  
And.  
Well, let me let me, I'll just let me just finish really quick. So then what happens is that anybody who's outside of this repo, inside of these games somewhere else, Golden China, if it's being used still, one of the notes that's known for Golden China is that it uses a WS platform deployment version.

**Andrei Bosik** 39:54  
OK.

**Aaron Bockelie** 40:11  
9.71 or whatever it is.  
The point is, is that you want to make sure you have a traceable latform deloyment system that is known.  
You're trying to version control your even your latform deloyment.

**Andrei Bosik** 40:35  
And.  
Uh.  
This is different product and uh when uh product.  
When's the repository with source code product, for example, for example, game of Stack Star is built.

**Aaron Bockelie** 41:01  
Yeah.

**Andrei Bosik** 41:01  
This job create commit to this repository and if we move this old repository to one we have big list commits and if I need to for example in this moment I work with cluster for example.  
And if I need to find my commit or go back to some commits, it's a really problem for me.

**Aaron Bockelie** 41:29  
What? What triggers a new version of Aztec Star to be deployed?

**Andrei Bosik** 41:35  
Um.  
New version game.

**Aaron Bockelie** 41:39  
And where is that version stored at?

**Andrei Bosik** 41:44  
Mm.  
He's, uh, version version created dynamically.

**Aaron Bockelie** 41:50  
Right. And but where's?

**Andrei Bosik** 41:51  
He version is increment.

**Aaron Bockelie** 41:55  
Where's the version kept at? It's kept.

**Andrei Bosik** 41:55  
Uh, in uh.  
Yeah.

**Aaron Bockelie** 42:03  
OK, so this is all statically defined, right?

**Andrei Bosik** 42:08  
Yes.

**Aaron Bockelie** 42:09  
So why not if you had a repo called Aztec Star and there was A tagged release version for Aztec Star that was the latest release version of it?  
Why not? Instead of dynamically tagging this, why don't you just go ahead and make it so if somebody in the Aztec Star team actually commit puts in a a a product release for this, your CI system picks it up.  
And does the deloyment automatically? That's how it's supposed to work. This manual process of having to do all this stuff is extremely labor intensive.

**Andrei Bosik** 42:50  
It's work automatically, it's not manual process.

**Aaron Bockelie** 42:52  
Well, what puts the tag in there?

**Andrei Bosik** 42:57  
Uh, in a job.

**Aaron Bockelie** 43:00  
And where does the job come from?

**Andrei Bosik** 43:01  
Do the job.  
Uh.

**Aaron Bockelie** 43:05  
Job comes from.

**Andrei Bosik** 43:07  
This job work now in Jenkins because game squad plays in SVM.

**Aaron Bockelie** 43:11  
In Jenkins.  
Right. So when's the code going to not be in SVN?

**Andrei Bosik** 43:21  
I don't know.

**Aaron Bockelie** 43:23  
This is the problem. You're still splitting your everything in GitHub and SVN right now. If the game was committed into GitHub, they would have a repository for Aztec Star and when they committed a actual like not an interim release or a build release.  
But a roduction release tag version of it, your CI system here running as an action looking for any games in particular repos would see a release and automatically push the release out to everybody.  
After all the tests and everything had passed.  
Putting the control of the release not into you, but into the team that built the software.  
You're the bottleneck right now for this, sort of. Obviously it's not quite there's a it's not a huge problem because you're saying Jenkins does it. But the problem is, is that Jenkins is still pulling things from SVN and you have a split brain now for the entire company for this.  
So I I don't want to try to solve this problem right now on this call. What I'm just trying to say is, is that I think if you start by going with platform AWS and you keep this in here and you start thinking in this way, eventually you'll.  
Clear the path through the forest to build a real Rd. for getting off of SVN for the rest of the of the team.  
That's the real goal. The real goal is to be able to make it so JVL can release software rapidly without a lot of constraints.  
And this is just happens to be one step along the journey of it.

**Pavel Frolov** 45:11  
It's clear, yeah.

**Aaron Bockelie** 45:19  
I know it's kind of a I'm basically saying, well, it's gonna be some work, Andre. Unfortunately, that's just how it is.  
Because the real issue is, is that it sounds to me like SVN is still holding all the games and you're still dependent on on Jenkins, and Jenkins needs to eventually be replaced with GitHub.

**Val Levitan** 45:44  
Well, if you if you remember.  
We started our reform from speaking to Lena.  
And Sasha Biratko.

**Aaron Bockelie** 45:58  
Mm-hmm.

**Val Levitan** 46:00  
And we were not able to move them to GitHub.  
The Omni was not. Omni was not ready at that time. We did not, and we couldn't convince Lena how to work in GitHub. So if you recall, we parked it.

**Aaron Bockelie** 46:21  
Yeah.

**Val Levitan** 46:22  
And decided not to pursue it. It was too difficult. It was just we we it was too many headwinds.

**Aaron Bockelie** 46:30  
Right.

**Val Levitan** 46:30  
So we started with core and we decided that when we move core into git, our next step will be to move graphics into git. So that's why graphic is still is in SVM. We still have not.  
Touched it. We have not done anything about it and moving it right now to get without preparing that side, Lena's side and making them comfortable and making them comfortable, meaning resolving LFS.

**Aaron Bockelie** 46:53  
Yeah.

**Val Levitan** 47:08  
Resolving, you know how to make executable files, how to transfer files, where to store them until that part is resolved and we can show them exact way.  
And if you remember, at that time, Andrei was also not trained on Git. It was too too early for.

**Aaron Bockelie** 47:29  
Yeah, it's been time. Yeah. Well, I think it's just a it's an indicator that it's time to try to solve that problem, or at least define how to how to solve it.

**Val Levitan** 47:33  
Soul.  
I think, I think I would focus on core right now and groom it correctly because we have willing participants here.  
Let's get it to 8020 rule and if it functions we can then start switching Lena's team and then come back and regroom it again.

**Aaron Bockelie** 48:08  
My suggestion is, is that you go platform AWS and you put all the things in there and deal with the outcome of that and then that sets it up to be able to understand how to do deployments from those games when that time comes in the future.

**Andrei Bosik** 48:24  
I'm not agree really. For example, OK, I can agree with about deployment repositories, but last year this is a different. It's different things. It's a.

**Aaron Bockelie** 48:33  
Yeah.

**Andrei Bosik** 48:39  
Management uh and creating classes is it's a not deployment process.

**Aaron Bockelie** 48:46  
Is it part of AWS though?

**Andrei Bosik** 48:48  
It's a part of WS, yes, but it's different things.

**Pavel Frolov** 48:54  
What if we left this as a separate repo platform aware?

**Andrei Bosik** 49:00  
It's it's really need to separate trip.

**Aaron Bockelie** 49:02  
You could call it platform AWS cluster and have it be a thing. Remember, remember your convention. Don't don't fight it, use it. I'm just saying that you I think at a minimum it should be platform AWS for things.

**Pavel Frolov** 49:05  
Yeah.

**Andrei Bosik** 49:07  
Oh, OK, this is OK.

**Pavel Frolov** 49:12  
Cool.

**Aaron Bockelie** 49:19  
And if you decide that every single one of those needs to be its own repo, then so be it. But it has to follow the platform first, then AWS, then the component.

**Andrei Bosik** 49:30  
OK.

**Aaron Bockelie** 49:31  
That's perfectly acceptable in my mind.

**Andrei Bosik** 49:37  
Um.

**Aaron Bockelie** 49:37  
Maybe go to your repo naming tab and add those terms under component first.

**Andrei Bosik** 49:44  
Yeah.  
And uh.

**Pavel Frolov** 50:10  
I moved uh AWS to subcategory.

**Aaron Bockelie** 50:10  
With did.

**Andrei Bosik** 50:16  
OK, sync file.

**Pavel Frolov** 50:24  
Yes.

**Andrei Bosik** 50:26  
And here we can type.

**Aaron Bockelie** 50:40  
I think that looks a lot cleaner to me.  
It's not even actually reading the words, but just sort of seeing what I saw before and what I see now.  
There's less confusion here, and if you need to break it out further, you can.

**Andrei Bosik** 51:04  
OK, OK, I I I think about.

**Aaron Bockelie** 51:08  
Uh, line 70 column E. Is that correct?

**Andrei Bosik** 51:14  
Yes, platform and the US cluster is a different repository from deployment.

**Aaron Bockelie** 51:22  
I thought that was the optional planned target repo. Call me.  
I thought you were going to keep it as cluster.

**Andrei Bosik** 51:33  
Uh uh, platform question.

**Aaron Bockelie** 51:35  
Yeah. So you're gonna, that's the, yeah, that's kind of what I was thinking.

**Andrei Bosik** 51:37  
Um.  
I'm not sure because we have for example Azure or another platform I think.  
But it's a it's a different sync I think, but I have two different repositories for different clusters.

**Aaron Bockelie** 51:58  
Yeah, I just was saying that 70 column EI don't think actually should have anything in it.

**Pavel Frolov** 52:01  
Yeah, actually.  
Yeah, it was an error in column.

**Aaron Bockelie** 52:06  
Yeah.  
OK.

**Andrei Bosik** 52:15  
I'm on this.

**Aaron Bockelie** 52:20  
So as an experiment on call, if you go to Repo naming tab, you have AWS in there right now, but you could very easily now add Azure.  
To this platform or Google or whatever, right?

**Andrei Bosik** 52:34  
Yeah, yeah, yeah. I'm saying it's OK. Yes, yes, yes, it's a.

**Pavel Frolov** 52:39  
And cluster cluster need to be moved from subcategory to component.

**Aaron Bockelie** 52:45  
Yeah.

**Pavel Frolov** 52:47  
Yes.

**Andrei Bosik** 52:50  
Right.  
They will file.

**Aaron Bockelie** 53:23  
OK.  
So I like that categories really just seems to fit that much better now. Infrastructure, knowledge, platform, tools, big, big blocks.

**Andrei Bosik** 53:26  
Which is it?

**Aaron Bockelie** 53:35  
And then the subcategory in here seems to make a lot more sense. They're products and platforms.  
The products.

**Andrei Bosik** 53:44  
Mhm.

**Aaron Bockelie** 53:46  
The component makes more sense because it's generic.  
You could have a component on AWS just as much as you could have our cluster on AWS just as much as you could have it on something else.  
Or a sandbox or whatever.

**Pavel Frolov** 54:12  
Mhm.

**Andrei Bosik** 54:19  
OK, let's go to plan. What about yellow repositories?

**Pavel Frolov** 54:26  
Move.

**Aaron Bockelie** 54:26  
Seems to me they should go to.

**Andrei Bosik** 54:27  
Let's acknowledge, just acknowledge with folders.

**Aaron Bockelie** 54:30  
Yeah.

**Pavel Frolov** 54:31  
Yes.

**Aaron Bockelie** 54:32  
So, so as an example you could have under subcategory, you could have GitHub now now that we're following this pattern. So I'll put GitHub as an example and so you could have a knowledge GitHub specifically for things related outside of the because obviously.

**Andrei Bosik** 54:35  
OK.

**Aaron Bockelie** 54:49  
You're not going to tie GitHub architecture with.  
Game knowledge or or something like that. So you probably have a special call out like think the taxonomy model. We could just have knowledge and knowledge could have a whole bunch of subdirectories for all of the concerns you'd ever want, right?

**Pavel Frolov** 55:06  
Yes.

**Aaron Bockelie** 55:15  
But that might get overwhelming.  
Having everything in one gigantic repo, but it also might be helpful. I don't know if you take the knowledge repo and you break it into several subcategories. GitHub, Jenkins.  
Flex.  
This makes it very easy to build the other knowledge base app aspects of this. If you choose that you want to pack the knowledge into the projects themselves, well, then you just basically.

**Pavel Frolov** 55:47  
Yes.

**Aaron Bockelie** 55:52  
Put all of the knowledge inside of the subcategory an you keep things separated by concerns that are that you need to be separated O for example.  
Um, knowledge about GitHub is never really gonna be inside of the Omni or Miranda or Jenkins or anything else. It's its own concern.  
But knowledge about.  
Omni or Flex or whatever should stick within Omni or Flex or whatever.  
So you do you know about git filter repo and git submodule filter repos those commands?

**Pavel Frolov** 56:51  
Um.  
No.

**Aaron Bockelie** 56:54  
OK, so just really quick, I know we're time over time here. Can you Scroll down on the let's use sheet. I'm just going to add another sheet. I'm going to call it sheet 4. Go to that sheet please.  
So you could have uh knowledge.  
As a repo name and then you could have a submodule called. You could actually throw the submodule of Omni.  
An submodule of.  
I don't know. Actually, let's do.  
Latform Omni submodule of. Let's just make sure I get the names right here.  
Platform flex OK.  
O if you have this.  
This is actually a possible structure you can create for knowledge. Now if you have, let's just say another repo called.  
Knowledge. GitHub. OK, so that falls into this category.  
You could.  
Recursively add whatever git repos and filters you want to a given repo to build with big blocks a meta git repo that actually is just an empty structure that references everything else.  
This allows you to then collect and aggregate the knowledge from all of the other areas of all of your other git repos into one large space and if the docs folder inside of here is correctly structured.  
You can have this meta reo called knowledge that ublishes everything as docs as code underneath from every single reo structure that conforms to that.  
This is essentially a gitbased Confluence environment.  
So I would, I would.  
Look at, you know, filter repo.  
I don't remember the name, but.  
So the reason I'm telling you this is that this sort of knowing these exists or these techniques exists can help you with your naming convention.  
O if we go back to just reo naming again for a minute.  
Go to the repo naming tab again, please.  
If we know a secret where we can extract sub path sub directories out of a git repo, then we can say that you know for most things it's going to be that it's not a separate knowledge repo. Knowledge is just.

**Pavel Frolov** 1:00:23  
Yes.

**Aaron Bockelie** 1:00:30  
Tracked inside of the individual projects. So there's a docs directory for every single one of these, which is your knowledge, right?

**Pavel Frolov** 1:00:33  
Um.  
Sh.

**Aaron Bockelie** 1:00:39  
Then you can have a general knowledge reo just called knowledge.  
And in some cases you can have specialty knowledge repos called knowledge GitHub or knowledge AWS for example, and those also have a slash docs folder. Finally, you have a major git repo that's actually just called knowledge.

**Pavel Frolov** 1:00:59  
Yes.

**Aaron Bockelie** 1:01:01  
That is composed of all of those submodules and git filters.  
And that becomes the living, breathing documentation space for everything. When anybody's making commits, all of the references are cloned and updated into the main knowledge repo all the time.  
If you look at how like other projects that are pretty significantly open on the Internet, the Linux kernel for example, and other doc systems like that, they all sort of work that way as well.  
O We're not inventing the wheel here. This is just a known pattern for doing this.  
O to to wrap it U.  
Let's assume that knowledge for the most part sits with the repos themselves. Knowledge is always existing inside of the inside of Platform Flex or Platform Omni.  
And then we only have to have specialized choice picks of the knowledge category for things that are they themselves need to have that. So if we have knowledge AWS, Andrei, if you go to your planning tab.  
Please go to your planning tab and we find that we have most of this is all under platform AWS. Yeah, so you're going to have a docs directory underneath platform AWS.

**Andrei Bosik** 1:02:38  
Mhm.

**Aaron Bockelie** 1:02:44  
Or maybe you'll have a per directory thing in here, an AWS game slash docs or game slash docs, game slash application slash docs, Vivian slash docs and so forth. But these docs are only related to the deployment aspects.

**Pavel Frolov** 1:02:52  
It.

**Aaron Bockelie** 1:03:02  
Of Vivian on AWS. They're not related to Vivian itself.  
O We're separating the concerns out there.  
Atomic concerns of only what you're worried about for that repo. I can see by everybody's faces that we're all getting to the end of the rope here, so I'm going to stop that. Am I am I making sense by saying this? Does this?  
Does this make sense to you?

**Pavel Frolov** 1:03:36  
I'm not sure that I fully understand last five minutes that you described some filtering.

**Andrei Bosik** 1:03:45  
Now when you use filter you can choose.  
In this example, just one folder which you want to include to the big repository. For example, you can choose a doc folder.

**Aaron Bockelie** 1:04:10  
I'm just searching the Internet for a couple examples of this.  
Here's an example of.  
I don't even want to bring it up right now. I just don't feel like it's gonna be the right.  
So this is a plugin for Make Docs, which is how you would present the documentation from your Knowledge Platform into a consumable mode, and this essentially is a configuration file that pulls the document structures from the other git repos, federating the documentation across from all.  
Of the other repos during the build process of your document site.  
It's really about knowledge federation across all of the different repos.  
That's kind of the best word I can think of for now is federation.  
But that's how I would structure all of the knowledge at this point.  
Let me make a AI generated explainer document for this.  
Almost done.  
This is probably a great starting place to kind of understand what I'm talking about. You should read this on your own time.

**Pavel Frolov** 1:09:49  
Mhm.

**Aaron Bockelie** 1:10:10  
But I think um.

**Pavel Frolov** 1:10:13  
Yeah.

**Aaron Bockelie** 1:10:14  
Kind of the main. The main asect of this is if you look at how you have a documentation site and then you have a pipeline generator and you have all the repos with docs across that.  
Are you all able to see that?

1:10:33  
Mm-hmm.

**Aaron Bockelie** 1:10:36  
OK.  
So basically using make docs or docosaurus for example.  
I think Docasaurus is probably a little more based on Java and maybe actually be more valuable for your for you guys than than make docs, but I don't know, it just depends.  
But what this does is it's shifting the value of the docs from an abstracted confluence page somewhere that's completely disconnected from the code to literally into the code itself. And when people start working on stuff, it's all in the code repo.  
And for those items that are really abstract, for instance, personas, right? Personas are pretty abstract. That might be its own thing, but it can still be brought into the whole structure.  
And then when you think about having a docs directory for say AWS platform for for a cluster or something like that, you can still bring the docs into that alongside of everybody else's docs.  
This becomes the official knowledge repository for the entirety of everything.  
It's not dead dead data now.

**Pavel Frolov** 1:12:18  
OK, we'll take a look on the article to understand how.  
How to work this?  
Derated documentation.  
And what benefits it can provide?

**Aaron Bockelie** 1:12:37  
This is. This is also another reason to get the games into GitHub rather than SVN.

**Pavel Frolov** 1:12:38  
Oh.

**Aaron Bockelie** 1:12:45  
Because you can store the docs with the games too. I don't want to reach that too much right now, but that's where this goes.  
All right.

**Val Levitan** 1:12:57  
But I'm but I'm lacking to understand the resistance.  
From Andrei and Pavel, what's the what's the source of resistance?  
I mean, what's being told here is.  
Practically pure and totally implementable and something that has been in place for.  
As I understand, forever now.  
And has been has been tried by many companies and adopted by those that.  
Are more focused on on proper hygiene of development.  
So it might be not known or might be not familiar.  
And at some point might be counterintuitive and definitely clearly not the way we have been doing things, but So what?  
Aren't we focused on adopting?  
Better hygiene.  
That a methodology?  
So I understand that we probably not have done it. We've never, we've never worked that way. But if this is a practically tried method, it's it's not novel.  
It might be novel to us, as I understand, but it's not novel. There's nothing new about it. We're not breaking any grounds here. There's no we're not on the edge of any technological progress here. We're simply told.  
Here's how the leading companies do it, do it the same way. So what is the issue? What is the hesitation I would have expected from you saying, oh, OK, I've never done it before, but yeah.  
It's logical. Makes sense.  
No.

**Pavel Frolov** 1:15:19  
Val, I even do not understand what you are describing right now, our approach to naming of repositories.  
Or something else.

**Aaron Bockelie** 1:15:36  
This is a corner case about naming. This is. This is what happens when you name them. Well, this is one of the very first things and there's in in the.

**Andrei Bosik** 1:15:37  
No, it's a different things.

**Aaron Bockelie** 1:15:51  
In the ratio of.  
Project of repos that you have on this list. A high number ratio of them are specifically knowledge based.  
Which presents a concern about where this is all going, and what I'm trying to do is to convey to you the purpose of doing this and why, not just telling you to do it.

**Pavel Frolov** 1:16:19  
We understand that in in world where we create repositories on regular basis, it's better to have.  
Defined strategy for naming convention.  
I think we do not have any hesitation here.

**Aaron Bockelie** 1:16:49  
Here's a updated list of it. It's unfortunately Teams numbers it with a number one with a list of actual sites using this method.

**Pavel Frolov** 1:17:08  
If Val mentioned, uh, the last.  
Information from Aaron. I don't have any idea here because I I have not.  
I haven't read this document before.  
I really do not fully understand what it describes.

**Val Levitan** 1:17:32  
The the document, the document that Aaron published was a result of hesitation where he had to prove his point and that's why he published the document. And I don't. I tuned out for a while in the conversation because it was really.

**Aaron Bockelie** 1:17:33  
But.

**Val Levitan** 1:17:52  
I had very little.  
Application on my level to what's being discussed. So although I'm I'm in this meeting but mentally I have departed because it just hardly have any applications to my life.  
But when I tuned in or periodically as I would TuneIn.  
I understood that there is.  
A tag action between where you want to be and where Aaron is telling you to be.  
So my general statement at the end of the meeting was why is there a tag? What? Why do you try to pull your way if Aaron tells you this is the way to do it? Why not blindly say, OK, well, I didn't know that this is the way to do it. Let me do it this way.  
If if in front of you you have a consultant who's consulting for major companies and teaching them how to do things.  
Unless, unless you say, well, I've done it this way and here's my benefit and my ways are better. So then maybe Aaron will learn something and say, OK, well, truly better.

**Pavel Frolov** 1:19:21  
OK, let let me repeat my last message related to archive organization.  
I actually agreed to continue working as is, so we put all repositories into main organization, one of two.  
But probably we will return back to this question in two years when we get lots of repositories.

**Val Levitan** 1:20:09  
But he replied to your question, his reply, if I understood correctly, that there should be a grooming procedure, a hygiene grooming procedure on a regular basis where we remove the repositories that are not.  
Hunger used.  
And again, this is something that really doesn't.  
You know, that doesn't really occupy my day.  
But the overall hygiene of or grooming of all aspects of company, whether it's accounting or engineering or HR department, I think the grooming aspect is.

**Pavel Frolov** 1:20:56  
OK.

**Val Levitan** 1:21:05  
Does not only promote cleanliness, but it also promotes.  
A certain style of.  
Companies life.  
Overall.

**Pavel Frolov** 1:21:27  
But nobody against a clearing procedure. It can be done different ways. Either delete everything that forgot about this code, but in two years understand huh, it was a.  
Amusement project. Let's take them from some place and try to give them new new life. Where can we find it? OK, probably on tapes.  
Let's take a look.  
Different it it could be different way either to move to different organization or to remove or left them leave under the same repository keep keep it growing.  
Different strategies we do not against about clearing procedures.

**Andrei Bosik** 1:22:27  
And different time to recovery.

**Pavel Frolov** 1:22:30  
Yeah.

**Val Levitan** 1:22:39  
But my understanding, this was put away already. This was decided. There was another part of this conversation.

**Pavel Frolov** 1:22:49  
Yeah, because we agreed to postpone the solution until we get stuck on some aspects. For example, we are going to make review of all the repositories and decide what to do then.  
This is them.  
But you don't have solution.

**Andrei Bosik** 1:23:14  
Maybe after two years we we we use another product and currency solution is not applicable.

**Val Levitan** 1:23:23  
OK, so.  
I'm I'm confused as to what is the next step.  
Because and and the reason I'm asking is that.  
Unless we decide on repository naming conventions.  
And.  
Certain archival procedures we, from what I understand, are hesitant to proceeding.  
And I would like to push the process forward. So I just I I need the repositories. I need to clean this up.

**Pavel Frolov** 1:24:15  
I I assume that we already at the stage when we can start moving, moving and renaming repositories.

**Andrei Bosik** 1:24:25  
I think too, yes.

**Val Levitan** 1:24:30  
OK.  
So then.

**Pavel Frolov** 1:24:33  
Seems since we discussed everything and agreed on naming structures, especially on the top level, I mean.  
Components and subcategories. Categories.

**Val Levitan** 1:24:55  
All right, So what is the then? What's the next step and what's the undertakings from this meeting?  
Let's just summarize what's gonna happen next week.  
And and who's? Who's a particular undertaking? Who is it? Who is it assigned to? So is everything assigned to Andrei?

**Pavel Frolov** 1:25:19  
Uh.  
First steps, I think yes, he will need to prepare some.

**Andrei Bosik** 1:25:36  
Yes.

**Pavel Frolov** 1:25:39  
Some data try to to capture all secrets, settings related to organization and repositories in under one place and.

**Val Levitan** 1:25:51  
When you say when you when you say secrets, can you elaborate on that? I'm not sure what what it means.

**Pavel Frolov** 1:25:59  
Secret is a standard parameter type in GitHub to store some parameter in hidden hidden form.

**Andrei Bosik** 1:26:10  
It's.  
Uh and.

**Pavel Frolov** 1:26:14  
And can be reused by actions.

**Val Levitan** 1:26:19  
OK.

**Andrei Bosik** 1:26:19  
And the secrets is not a good naming. It's a naming can have environments. It's environments can be hidden or not hidden and we need to move from all current organization this environments to.  
One organization.

**Val Levitan** 1:26:37  
OK. And how long will it take? What? What does it take?

**Andrei Bosik** 1:26:42  
For me, I think it's one day it's will be enough to do this jobs at environment and at access to run it from other repositories.  
But when our developers start fix some actions, I think they have some problems and they come to me help resolve this problem maybe.  
And this is a need to time too. I can do this on Monday, but on Monday we need to say all on Tuesday our old development and need to start work with their repository.

**Val Levitan** 1:27:34  
So is there a problem with that?

**Pavel Frolov** 1:27:39  
Andrei, are you saying that on Tuesday repositories will be already using new names?

**Andrei Bosik** 1:27:49  
I will be ready to move.

**Pavel Frolov** 1:27:50  
And so.  
Ready to move only.

**Andrei Bosik** 1:27:53  
And if we move, I think we need to move step by step. For example, on Tuesday we can move repositories from GVL core. On Wednesday we can move repositories from GVL.  
Bulls.  
Step by step, not all in one day.

**Val Levitan** 1:28:19  
OK, so Aaron, what would be a sensible check in point for us? At what level?

**Pavel Frolov** 1:28:24  
Yes.

**Val Levitan** 1:28:28  
At what state I should say?

**Aaron Bockelie** 1:28:32  
I think that once you've determined the order of which repos need to be can be renamed first or should be renamed first.

**Val Levitan** 1:28:39  
I don't understand.

**Aaron Bockelie** 1:28:40  
Or which block of work you're going to plan on doing first O these items that have dependencies. For example, you're going to need to make sure that you've handled the dependencies, right?  
So I I think that coming up with a migration plan step by step for those who have dependencies listing what you're going to do, that's a good check in point.

**Pavel Frolov** 1:28:53  
Mhm.

**Aaron Bockelie** 1:28:54  
Yes.

**Val Levitan** 1:29:04  
OK. So the first undertaking is to come up with the migration plan and the best way to discuss the migration plan is when we can read it.

**Aaron Bockelie** 1:29:16  
Yes.

**Val Levitan** 1:29:16  
So we're asking Andrei, please come up with the migration plan, put it on on a.  
In his in this particular chat, let's put it in this chat. I'm going to put the transcript of the meeting also in this chat. So let's put the migration. So the undertaking is for Andrei to come up with a migration plan and present it to us in writing in this chat.

**Andrei Bosik** 1:29:31  
OK.

**Aaron Bockelie** 1:29:46  
Yeah, then we could just kind of think about it, make sure it looks right. It should be relatively quick because and then basically what's gonna happen after that is Andrei, you could.

**Val Levitan** 1:29:47  
Uh.

**Aaron Bockelie** 1:30:00  
Tell us how are you going to? I mean, basically what we're doing is we're turning this into a change management problem. We're making a change. We're going to describe the change. We're going to talk about the change and the backup plan for it because it will damage the company if it's done wrong.  
And then if it seems rational, then we'll let Andrei have the time to do it and see how it goes.

**Val Levitan** 1:30:24  
So when can we? What date can we review the change management plan?

**Aaron Bockelie** 1:30:32  
I think that depends on their.

**Val Levitan** 1:30:32  
Andrei, Andrei, don't squeeze yourself because you have other work to do. So give me a reasonable date when you feel comfortable with.

**Andrei Bosik** 1:30:44  
I have I have many work and I I I can do it. When you say this I need to do it, I can send plan to today.

**Val Levitan** 1:30:57  
I do not want to. I do not want to. I do not want to. I do not want to establish priority for you. Please give me the date based on your current load, the date that you feel comfortable with your date.

**Andrei Bosik** 1:31:15  
Date just on the for plan and or or or what? I'm not sure that I can understand you.

**Val Levitan** 1:31:16  
But.  
Well, I'm sorry that you cannot understand me because I cannot imagine how to be more clear than I am. Please give me the date when you will be able to present us with the change management plan in writing.

**Andrei Bosik** 1:31:40  
No, I understand. Uh, maybe on Tuesday.

**Val Levitan** 1:31:46  
Tuesday.

**Andrei Bosik** 1:31:46  
Yes, we can. Uh.  
OK.

**Aaron Bockelie** 1:32:01  
Thanks. Bye.

**Pavel Frolov** 1:32:01  
Thanks. Thank you. Bye.

**Andrei Bosik** 1:32:02  
OK, sync my.

**Andrei Bosik** stopped transcription