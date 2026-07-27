**Aaron_Val-20260306_155302-Meeting Recording**

6 March 2026, 08:53pm

9m 46s

**Val Levitan** started transcription

**Aaron Bockelie** 0:03  
This up and build this if you want like a better version of this. So this is just a git repo that is checked literally into the git repo of the GitHub enterprise itself, just like how you have lots of git repos in your enterprise.

**Val Levitan** 0:19  
Mhm.

**Aaron Bockelie** 0:19  
And there is a tool called Enterrise. You can see it right there. It's like a whole bunch of stuff and when we run it.  
This GitHub Enterprise Management Operator is what this is called. We can invite users, we can remove, audit, check, list, cancel invites, copilot, manage and repo management. So.

**Val Levitan** 0:46  
This is a. Is that a purchase tool? GitHub Enterprise Management operators?

**Aaron Bockelie** 0:50  
No, I just made it. It's just no different than anything else I make. It's just, you know, so I don't really need to run it myself, even though I could, right? I could. I could run it like this. I could do enterprise Pi list orgs, right?

**Val Levitan** 0:53  
Oh.  
OK.

**Aaron Bockelie** 1:07  
And it's going to list the organizations inside of the GitHub Enterrise, just like how JVL has organizations, right? OI could do list, I could do repo.

**Val Levitan** 1:14  
Mhm.

**Aaron Bockelie** 1:20  
Repo list and then I could specify an org C prime.  
Enterprise Solutions.  
Oops, hang on org repo.  
I don't remember all of them. Anyway, I don't really know how to use it exactly. I don't really care because I use Cloud to use it for me. I just say tell me all the repos in the C Prime Enterprise Solutions org.  
I didn't have to spell it right. I can be super lazy, right?  
It's going to load the tools. It's going to go check it out. It's going to remember how it works.  
Oh, actually that's one of the things that doesn't work, but here's all the list of repos, right?  
So what we're going to do here is I've just been slowly growing this tool, and so Andrei and whoever needs to get into the mindset of growing the tool too, to expand to what they want it to do. So here's a list of repositories.

**Val Levitan** 2:21  
OK.

**Aaron Bockelie** 2:35  
Right, last udated and so forth.

**Val Levitan** 2:36  
Mhm.

**Aaron Bockelie** 2:50  
O I'm just going to correct it right now in this recording so you can see it. We should add that list repost to the tool. Then I'd like to get a report of who's on what repo.  
So we're letting Claude improve its own tools right this second right now to be able to just interactively figure out what's going on in the repo. And because it's not just like inventing a bunch of ******** that disappears after the chat's done, it's creating tools that can be reused and reused and are actually.  
Computing and grabbing the real data, not hallucinating something.

**Val Levitan** 3:23  
Where do you? Where does this tool reside?

**Aaron Bockelie** 3:27  
It's just on my computer local. It's just a workstation tool. There's no reason I couldn't make this an MCP server, for example, if I wanted to.  
O just the same as you manage JIRA issues, you could manage GitHub repos and stuff inside of a chat and see what's going on too.  
So ignore kind of all this scroll right now. I'm just letting it fix the code because I just realized I asked it something I never asked before and I'm I'm improving it right now to kind of make it better. So it's going to write the code to get this.  
It's based on using the GitHub command line tool, which is GH you've probably seen. I've walked you through using it before and I know that some other you know Andres used GitHub command line tool, but a lot of these activities and I think this is what steered Claude into trying to tell you.  
That you should use JIRA to do a dashboard is that GitHub does not have a bunch of tools out-of-the-box to provide reports and data for this. But what we can do here is just build the tools we need until we have what we want to watch for stuff.  
We've got to check monthly if we need to run something, and because it's running a program to do this, you could just say, hey, make me a program that runs every week and prints me a report out or whatever it is you want to do, or collect metrics or data or things.  
O We're letting it run here.  
I just want to. I want to let it go through the because it wrote the. It wrote the tests for the tool too by instead of justice writing the code so it's running the. We'll let that go in the background.

**Val Levitan** 5:17  
Sure.

**Aaron Bockelie** 5:26  
O I'm going to just let it run. Come on, I can hear my computer fan sinning U it's doing something.

**Val Levitan** 5:38  
What is the? What is the abbreviation for MC?

**Aaron Bockelie** 5:42  
Say that again.

**Val Levitan** 5:44  
NC graph. What is it?

**Aaron Bockelie** 5:45  
Oh, that's just like text mode graph.  
I don't know what it's wrapping up here.  
It'll it'll be a nice little visual here. In just a second we can see some stuff.  
So I'm just gonna tell it let's skip tests for now. We'll run them in a bit.  
O It's going to run a collaborator report.  
So you can see what it's doing is it's collecting the collaborators from each of the repos. There's 62 code repos in this one org, and you can see how there's like all these different collaborators, right?  
The GitHub API only runs so fast, so that's it's rate limited. This would be like clicking inside of every single repo right now in a web page this fast and reading the stuff and scanning it and getting all the information back.  
But instead we have a tool that just kind of collects this information for us in a in a much faster way.

**Val Levitan** 7:10  
Since when has this become a reality available to us? This is in a recent recent six months.

**Aaron Bockelie** 7:15  
Uh.  
No, the GitHub command line tool's been around for a long time.

**Val Levitan** 7:21  
No, no, no. Like what? What you're doing now with Claude?

**Aaron Bockelie** 7:25  
At least the last year, I would say. I wouldn't say any longer than that. I think Claude code and coding agents in general were too stupid or untrustworthy to do this before that.  
OK, here we go. So this is ANSI graphics, right? It's this sort of text mode, colorful little stuff. We can see there's some guy that looks like a mishmash of letters. I don't even know how to pronounce that. That's his username. So count of users by access.

**Val Levitan** 7:44  
Mhm.

**Aaron Bockelie** 7:56  
And then the next on the list is me, yours truly, and then all these other people. And then we can see here repos with extra collaborators beyond the 18 user baseline is these interesting data. 18 users have access to all 62 repos.  
This one is the outlier and here's a Cove file that you can open into a sreadsheet to go look.

**Val Levitan** stopped transcription