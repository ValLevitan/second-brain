**Aaron_Val-March-09-2026-20260309_151459-Meeting Recording**

9 March 2026, 07:14pm

10m 0s

**\
Val Levitan** started transcription

**\
Aaron Bockelie** 0:03\
There it goes. All right, so I like the.\
Like the.\
Um, intentions that you\'ve got here, which is looking for tasks that are in progress with a GitHub branch.\
But I think that the way that you\'ve defined this is.\
Unusually prescriptive. Um.\
You don\'t need to do anything other than run this as a get as an action in GitHub.\
O essentially in the project you can set U actions to do all sorts of things, including interact with Jira and.\
Basically what you could do is use a git hook or a GitHub hook to ensure that Jira and GitHub are are behaving well with each other.\
There\'s no reason to set up a Docker container and a bunch of other stuff and this unnecessary cloud spend for a workload.\
No, you\'re you\'re overcomplicating stuff for what should just be a GitHub action.\
The actual time that it runs is seconds or should be just seconds, and the amount of risk exposure that you have of running a container with rights and permissions to your both code base and to to Jira with.\
Access to that is extremely high.

**\
Val Levitan** 1:44\
OK, thank you for that. I appreciate it. So explain to me because I don\'t. I don\'t know this subject and I might be asking a silly question. My understanding is that GitHub action.\
Is written for a particular repository, one repository at a time, and you cannot glance at our company wide all repositories at the same time. So do you? Are you saying you\'re going to write action for each repository? We may have a lot of repositories.

**\
Aaron Bockelie** 2:06\
Right.\
You absolutely should be doing that, because doing that at one giant thing to solve it all is like playing the Tetris game where you\'re waiting for that one skinny piece to come in and and clear your board and it never does and you lose the game.\
By putting everything, all your eggs in one big basket to ensure consistency, you\'re massively complexifying everything that goes on in your git environment for every everybody.

**\
Val Levitan** 2:49\
OK, so how does it work? I don\'t, I I don\'t know schematically or logically. Can you explain to me? So you wrote action in GitHub to do what? To report on any changes I assume.

**\
Aaron Bockelie** 3:04\
So a GitHub action that checks for any branches.\
Opened in that project. They must be named or related in a way to a JIRA issue, for example.\
So all you\'d have to do is any branch that\'s opened that\'s not of a couple special reserved names, say main for example, right? Or published or a couple reserved names that would be helpful.\
Any other branch must have the pattern of a JIRA issue in it, and it\'d be very straightforward to.\
Look for that Jira issue ID in the name of the branch. Go search Jira for that issue. Look for the reciprocal GitHub link back to the project and if it doesn\'t exist, you prevent people from even committing into the branch.\
So you could or even you know, you basically could just delete the branch if somebody tries to open a branch.\
That is not legal. That is not tracked by Jira. You can actually revent it from even being moving inside of inside of GitHub.

**\
Val Levitan** 4:29\
So before we go into restrictions and prevention within the GitHub, let\'s just discuss. So GitHub, your right actions and then.

**\
Aaron Bockelie** 4:38\
Mhm.

**\
Val Levitan** 4:44\
How do these actions interact or hooped into Jira or vice versa?

**\
Aaron Bockelie** 4:50\
So let me give you one other example before I answer that question. Another way that you could do this is not to explicitly ban people from doing stuff, but you could explicitly ban people from merging a branch back into main without a valid Jira issue.\
So the way this works is that GitHub has this concept called actions, and actions are defined by a directory structure on the root of the repo called dot GitHub slash actions and every folder underneath there is actions for GitHub.\
When you define them, GitHub will, on whatever configuration that that file says it needs to do, do things like spin up a Docker container temporarily to execute code or check permissions or.\
Run a build or whatever else that needs to happen in GitHub and so that action is held by the container in GitHub. The permissions and the security and the keys necessary to get to things is are held in GitHub in escrow protected.\
And then the output from that action does whatever it needs to do in into other systems. So you could create a GitHub action that checks the name of the branch, logs in the Jira, matches up the name of of the issue.\
Checks the issue properties, makes sure that it\'s linked literally back to the the action to the repo itself that it was called from, and if they both connect and match up, then GitHub allows that merge to occur. If it doesn\'t, it doesn\'t allow the merge to occur, for example.

**\
Val Levitan** 6:40\
OK. And how does it? So it does it per Uh repository?

**\
Aaron Bockelie** 6:44\
Yeah.

**\
Val Levitan** 6:46\
So you\'re saying that?\
Doing it per repository, even if there are 500 repositories, I\'m over exaggerating. Still not a burden on the processor and just a small thing, right?

**\
Aaron Bockelie** 7:00\
No, there\'s no burden on that.

**\
Val Levitan** 7:04\
So if you have to do it per repository, assuming that I have a certain number, a certain amount of repositories, who cares?

**\
Aaron Bockelie** 7:12\
Yeah, who cares?

**\
Val Levitan** 7:14\
And so you\'re saying do it on a per repository basis and build it that way, OK.

**\
Aaron Bockelie** 7:20\
Yeah, I would also, if you wanted to have centralized control of managing all the repositories for quality, you have a special repository that can has the tools to check all the other repositories for consistency.

**\
Val Levitan** 7:33\
I do want to have. I do want to have that because I don\'t want anybody to alter the.

**\
Aaron Bockelie** 7:37\
Yeah.

**\
Val Levitan** 7:42\
Uh, alter auctions within the repository.

**\
Aaron Bockelie** 7:46\
Well, no, you you actually do want people to alter actions. You want to allow people to do whatever they want in that inside of that space to get work done. Don\'t ever prevent them from getting work done. But what?

**\
Val Levitan** 7:58\
No, I\'m talking about. I\'m talking about actions that that.

**\
Aaron Bockelie** 8:01\
Yes, I I am too. And actions are incredibly helpful for all sorts of stuff and we should never be preventing people from manipulating them. What you do instead is you make sure that when you query all your environments, all of your all of your repositories.\
You look for that one action that\'s an enforcement action for JIRA, and if it\'s not active and running, then you flag it.\
It\'s like, um.

**\
Val Levitan** 8:29\
And if you flag it, then what? Can you auto fix it?

**\
Aaron Bockelie** 8:30\
Well, then you then, then you go. What the \*\*\*\* are you doing? You\'re not allowed to have this.\
O You flag noncomliant repositories that are tied to actual work.

**\
Val Levitan** 8:38\
Thank you.\
And can you can you tell who made a change?

**\
Aaron Bockelie** 8:48\
Sure, you could just look at the git history. You\'d always be able to see that.

**\
Val Levitan** 8:51\
OK, so if the change made maliciously, you could basically take measures.

**\
Aaron Bockelie** 8:55\
Yeah, or accidentally. Who knows? Yeah, I mean, if somebody did it on purpose to stop something, there\'s there are 100 legitimate reasons to turn off GitHub Actions for a little while for some reason. Everything from holy \*\*\*\*, we broke stuff and now it\'s spewing our stuff onto the Internet. Let\'s just turn off actions and figure that out later.\
To I\'m trying to build new actions for a repo, but I have no idea what I\'m doing, so I\'m just trying to figure it out till it works and I\'ll put everything back when I need to once it\'s working again. So there\'s a there\'s 100 reasons to never prevent people from manipulating actions. Instead, you just make sure they\'re doing what they\'re supposed to do.\
It\'s a it\'s a way of trust and permissiveness, because the other model you take is one in which you have to maintain all of them, and there\'s only one Andrei and there\'s thirty other people. That\'ll never work.

**\
Val Levitan** 9:48\
OK, I\'m gonna shut off the recording because I think we got our meat and potatoes.

**\
Aaron Bockelie** 9:54\
OK.

**\
Val Levitan** stopped transcription
