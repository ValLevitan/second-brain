**Clayton-Aaron-JVL-20260428_135827UTC-Meeting Recording**

April 28, 2026, 1:58PM

57m 1s

**\
Clayton Chancey** 0:09\
Hello, hello, test.\
Hey, Lena.

**\
Lena Zhukova** 1:08\
Take them.

**\
Clayton Chancey** 1:11\
Okay.\
No.\
Headphones are not connected. Give me one sec.\
OK, there we go.\
Um\...\
I actually spent a lot of time figuring out what I think happened to us.

**\
Lena Zhukova** 1:36\
Okay.

**\
Clayton Chancey** 1:40\
Uh, if you, if you recall\...\
The last time we met, it was like the images didn\'t upload correctly and there were duplicates. And also that same data\'s new model released, Opus 4.7.

**\
Lena Zhukova** 1:47\
And.

**\
Clayton Chancey** 1:58\
And in the weeks, you know, or 1 1/2, two weeks since then, I\'ve also had\...\
like a lot of problems with Opus 4.7 and very\...\
Like, it doesn\'t follow instructions the same way.

**\
Lena Zhukova** 2:17\
Mhm.

**\
Clayton Chancey** 2:17\
It\'s not that it\'s a worse model, it\'s just very different. But there wasn\'t much documentation about this, and so it was very confusing. And I had another project as well, which is for a university for the economics department where it like\...

**\
Lena Zhukova** 2:34\
\*\*\*\*.

**\
Clayton Chancey** 2:36\
really perform poorly on these tasks. So I did some like benchmarking to try and measure it in different types of tasks and did a lot of work. And then I also figured out how like that we can change back to Opus 4.6 if needed. And I looked at these things and found.\
That it is.\
It is noticeably worse at following instructions over a long period of time with something called multi-needle retrieval, which basically is the exact use case of this, which is like there\'s multiple needles in a big haystack that need to be found.

**\
Lena Zhukova** 3:13\
Mmh.

**\
Clayton Chancey** 3:19\
and extract it very precisely. Like we need to find very specific images and we need to attach them to very specific tickets, all of which are extracted from sometimes one or two lines in a transcript. And so all of this is.

**\
Lena Zhukova** 3:22\
And.

**\
Clayton Chancey** 3:34\
much in Opus 4.6 is really good at it, and Opus 4.7 is specifically not designed to help with this use case. And so anyway, I spent a lot of time proving this to anthropic and having conversations and stuff. And I think what we can do today\
is I want to just try.\
switching back to Opus 4.6 and ask it to test the image flow and see if it does better because ever since I rolled my projects back to Opus 4.6, it\'s working great for me. So that\'s

**\
Lena Zhukova** 4:00\
Mhm.

**\
Clayton Chancey** 4:16\
That\'s my plan for the day is try that and we\'ll see how it how it works and.

**\
Lena Zhukova** 4:21\
Incorrect.

**\
Clayton Chancey** 4:23\
Yeah, so maybe you can share your screen and\...\
We, I think, let\'s just try, let\'s just start in Cowork and try from there first.\
And hopefully, hopefully we should be able to select the model there.\
So let\'s go to Cowork, which is that in the chat bar, that middle tab here.\
And then, okay, so you\'re on Opus 4.6 there. That\'s good.\
Let\'s try clicking into the D drive for our folder and pick like that, even that first folder, that\'s fine. Then we can ask it to look at the last.\
Um game dev.\
Have you had another game dev meeting since the last time we spoke?

**\
Lena Zhukova** 5:23\
No, we did not record. We did not record.

**\
Clayton Chancey** 5:26\
Okay, okay. So then I would, let me tell you what I would type. I\'ll just put it in the chat here. I want to say.\
I would just\...\
Copy paste that message and let\'s give it a quick test just to see how it\'s going before we get too far.

**\
Lena Zhukova** 6:05\
And.

**\
Clayton Chancey** 6:15\
Yeah, and let\'s send that.

**\
Lena Zhukova** 6:31\
Yeah, did we need to mention so it should not copy like existing Jira issue? Like remember it created duplicates like last time because some real issue were created already for twin bison and we didn\'t want them to copy to sandbox.

**\
Clayton Chancey** 6:43\
Ohh.\
I think I think Opus 4.6 will be smart enough. I think Opus 4.7 is so one of the other big differences between these models is that 4.7 follows instructions more literally. It is the term that Anthropic uses, which

**\
Lena Zhukova** 6:53\
Okay.\
To.\
Mm-hmm.

**\
Clayton Chancey** 7:08\
means like it doesn\'t deal well with ambiguity, but 46 is more interpretive. And so I think for like programming, Opus 47 is a bit better. For like, you know, knowledge work, knowledge workers like you or me and people who are not really programmers, it\'s more just like,

**\
Lena Zhukova** 7:12\
And.\
Bet.

**\
Clayton Chancey** 7:30\
instructions for an intern for six is better. So I think, yeah, yeah, I think that\'s funny. Let\'s try an end-to-end test, number one.

**\
Lena Zhukova** 7:31\
And.\
Should I pick the most recent transcript?

**\
Clayton Chancey** 7:43\
And then create new.\
I can already tell that it\'s a lot better. You can hit always allow.\
It\'s actually loading the assets, game assets tool, which Opus 4.7 did not do. You can scroll down and hit always allow.\
As you see, each of these tools, like the way I designed it, is that each of these tools, when they are loaded, it comes with instructions about what to do. And I think Opus 4.7 is essentially just only following your prompt and ignoring the other instructions which are embedded in these tools. And Opus 4.6 is picking them up.

**\
Lena Zhukova** 8:35\
Baby.

**\
Clayton Chancey** 8:39\
And it\'s steering, which is\...\
In my opinion, it\'s like a better way to use a large language model anyway, but I think anthropic.\
Is.

**\
Lena Zhukova** 8:52\
It\'s more focused probably on problems or\...

**\
Clayton Chancey** 8:52\
Yes.\
On coding, you know, Aaron, Aaron, Aaron Bockelie has told me, so, ohh, I used, I used Opus 4.7 as no problem, I don\'t see any problem with it, but he is doing different types of work, I think, than some of us, so\...\
Okay, so it\'s just creating some test tickets and it\'s going to try to map the images, which is fine. So hit allow for this task, yeah.

**\
Lena Zhukova** 9:18\
I love.

**\
Clayton Chancey** 9:32\
Just.

**\
Lena Zhukova** 9:35\
I see already that it\'s it is so like located like proper images to proper proper.

**\
Clayton Chancey** 9:42\
Yeah.\
Yeah.\
Yeah, we just have to make sure that it actually uploads them correctly, which remains to be seen, but\...

**\
Lena Zhukova** 9:50\
And.

**\
Clayton Chancey** 10:05\
To me, it\'s the thing that was really confusing. Yeah, perfect. This is really the test here is if it attaches correctly. The thing that\'s confusing is that they name it Opus 4.6, 4.7, but they\'re so different. It should be actually a different model rather than

**\
Lena Zhukova** 10:22\
Five, yeah, so yeah, it\'s all should do it.

**\
Clayton Chancey** 10:26\
Yeah.\
Okay, the attached tool returned 404 errors. Okay, so that might be something to explore.

**\
Lena Zhukova** 10:28\
It.

**\
Clayton Chancey** 10:39\
Oh, that actually might be my problem. It says the attached tools are looking at a different instance. Okay.\
Okay, this is good. This actually might help me here.\
You can scroll down and hit allow.\
I.\
Okay, so then\...

**\
Lena Zhukova** 12:17\
Only C tickets were created? That\'s strange.

**\
Clayton Chancey** 12:20\
Yes. No, we asked it to only test, so that\'s perfect. That\'s what we want.

**\
Lena Zhukova** 12:23\
No, no, okay, J.\
No, it\'s created suddenly 3 IPs.

**\
Clayton Chancey** 12:48\
Okay, can we click, let\'s go, if you click that ticket link at the bottom there, I just want to make sure that it actually uploaded an image.\
Scroll down.\
Maybe I misunderstood. What where is the what what did Claude Cowork say?

**\
Lena Zhukova** 13:09\
No, it\'s not. It\'s not sandbox. It\'s not sandbox.

**\
Clayton Chancey** 13:15\
Yeah.\
Yes, go back to cowork.\
Hold on, and then click, click back into Chrome.\
Are there attachments here?\
Not not in the sub tickets.

**\
Lena Zhukova** 13:45\
I think, I, I, yeah, I think so, but it\'s not the sandbox, so it is this this attachments validated menu.

**\
Clayton Chancey** 13:49\
Yeah, no, but, but I mean\...\
Yeah, but I mean if you go back to the main ticket where it said it actually uploaded them and then scroll down.\
No, no, the IP 105.4 in production and then scroll down.

**\
Lena Zhukova** 14:01\
Search.\
This is IP then.

**\
Clayton Chancey** 14:12\
Yes. Yeah, so scroll down. Are there any?\
Attachments here at all.

**\
Lena Zhukova** 14:18\
No, no, no, not an IP. Usually we attach images to features.

**\
Clayton Chancey** 14:24\
Yes, but okay, look at Claude Cowork. It tells you.\
that it created attachments on IP 1054. So I think.

**\
Lena Zhukova** 14:35\
But how it can create it and it is this real, this is real production space. Maybe we need to go to sandbox.

**\
Clayton Chancey** 14:36\
This.\
Yeah, I\'m just trying to follow the threads that Claude Cowork gave us and make sure where is this issue. If you look at what Claude Cowork says, it says IP 1054 and you can visually confirm. So I\'m just checking. You\'re obviously looking on the production instance. I don\'t see any issues attached there. So now.\
Let\'s go to the sandbox and look up IP 105.4 there and see if there\'s a difference.

**\
Lena Zhukova** 15:37\
Is this a symbols?

**\
Clayton Chancey** 15:41\
So yeah, that\'s what it\'s talking about. If you look at the child work item, you have that one there.\
So this is the one where it uploaded. Okay. Okay, so we can upload, but the issue\...

**\
Lena Zhukova** 15:48\
Yeah.\
I mean.\
Mm-hmm, so we can just say, yeah, that\'s what I do.

**\
Clayton Chancey** 15:54\
Yeah.\
Okay, perfect. So then here\'s what we can do then. If you go back to Claude Cowork.\
We have an issue where the instance is mismatched. Tickets created through the tool can\'t be found or attached to afterwards. Okay, so let me write a few things. I\'m going to update my clod code configuration here.\
Uh, that um, tickets that uh\...\
all read, search, attach tools operate against the production instance. Whereas, I\'m just prompting my cloud code here.\
Atlassian MVP has parameters supporting distinct production versus sandbox separation for testing.\
This means tickets created through the tool can\'t be found or attached to afterwards.\
This needs to be fixed.\
In the MCP server configuration, so all endpoints are at the same Jared instance.\
Thank you.\
Yeah, it\'s kind of an interesting problem because now that I\'m thinking about it.\
Okay, so\...\
So that.\
All create endpoints target the.\
Val.\
For instance, in this case, sandbox, but read and write.\
Can look at both, depending on the task.\
Okay.\
Let me see.\
If this works.\
It.\
While this build, give me one second, I need to get a tissue in.

**\
Lena Zhukova** 18:52\
Everyone.

**\
Clayton Chancey** 19:22\
Okay.\
Yeah.\
Okay.\
It\'s making some some changes here.\
The.\
Yeah.\
All right, cool.\
Okay.\
It\'s just uh, it\'s just making updates here.\
The.\
The.\
And.

**\
Val Levitan** 23:33\
Mhm.

**\
Clayton Chancey** 23:39\
Okay.

**\
Val Levitan** 23:42\
Yeah.

**\
Clayton Chancey** 23:43\
Once this.\
Finishes Lena, which it\'s building the the update for the Windows piece as well.

**\
Lena Zhukova** 23:52\
Mhm.

**\
Clayton Chancey** 23:53\
Then, all.\
Commit it to GitHub, and then we\'ll switch over to Cloud Code for you and pull that update down. Then we can run that, we\'ll probably just run that same prompt again and test it with a slightly larger set of.\
Tickets to make sure this is this is all end-to-end process is working.

**\
Lena Zhukova** 24:13\
Mhm.

**\
Clayton Chancey** 24:14\
But, but so far, we have actually confirmed that.\
The model change was a key.\
part of that failure last time. So we need to make sure moving forward that we\'re using.

**\
Lena Zhukova** 24:29\
Yeah.

**\
Clayton Chancey** 24:33\
Opus 4.6 for these like long, complex inference tasks like this, where we have specific things you want it to do, but it\'s drawing from like a huge amount of data, like a transcript, a very long prompt, essentially.

**\
Val Levitan** 24:37\
Yeah.

**\
Lena Zhukova** 24:52\
How would I know when I need to update? So maybe it\'s going to be like model 5, model 6, and maybe in some models they will fix these problems. So how would I know in future? So should I stay with this 4.6 forever for this?

**\
Val Levitan** 25:03\
Yeah.\
Yeah.

**\
Lena Zhukova** 25:11\
particular like MCP using.

**\
Clayton Chancey** 25:14\
To be honest with you, there\'s no clear answer for that. This is like, this is one of those things where\...

**\
Lena Zhukova** 25:17\
Mmh.

**\
Clayton Chancey** 25:21\
You have to have the requisite knowledge. I mean, you know, I would recommend sticking with Opus 4.6, but these models are going to continue to change, and some of them are going to be better, some are going to be worse for specific tasks, and it\'s\...\
I have a, I don\'t think that there\'s a sort of like non-technical answer to that question in the industry in the world right now. It\'s pretty much.

**\
Lena Zhukova** 25:45\
Two.\
Right, because I\'m afraid at some point they will not support it, you know, how they do like with old versions.

**\
Clayton Chancey** 25:51\
Yeah.\
Yep.\
I\'m with you.\
I mean, it\'s.\
It\'s just kind of where we\'re at in that.

**\
Lena Zhukova** 26:10\
At this point, yeah.

**\
Clayton Chancey** 26:10\
that world right now. Yeah.\
For now, you know, there are\...

**\
Val Levitan** 26:14\
Can you?

**\
Clayton Chancey** 26:17\
Oh, sorry. Hey, Val.

**\
Val Levitan** 26:17\
Can you, hi, can you sum it up for me? Where are we at?

**\
Clayton Chancey** 26:24\
I\'ve done.\
Let me think, sum it up. The last time that I met with Lena.\
Opus 4.7 had just released that same day, which is in theory a better large language model that\'s more capable, so we used it. The MCP server that I had been building for\
for Lena\'s use case, just performed horribly, terribly, unpredictably. Could not upload images.\
I committed to basically figuring out what was going wrong offline because there were just so many different things, very confusing.\
Um\...\
The same type of thing has happened with multiple other projects of mine.\
I had done extensive benchmarking over the last couple of weeks in partnership with Anthropic to understand some of this. This specific type of tasks that we are doing here in this use case and several other of my projects, Opus 4.7, the new model,\
is really bad at and Opus 4.6, the old model, is far better at. This morning, we logged in, tried again, but made a specific change to just revert to a legacy large language model. It worked fairly well.\
There are a few changes I need to make on the tools, which I\'m making now, but the specific issues we encountered are gone. So Lena is therefore asking, okay, well, I mean, great for now, but what do we do at the next update? How do we know when a large language model is better?\
For our task, or worse, and my, you know, my answer was\...\
Pretty much this at this stage in the industry, the process that I just went through for two weeks is how you know. There\'s not, there\'s not sort of like a an easy lay person.\
answer to figure that out. It\'s a potentially brittle process.\
However, I, you know, there\...\
Most of these model providers, they they do have a fairly long runway for like retiring models altogether, so it could be it could be a year, we\'ll say something like a year.\
Anthropic has been even more conservative, but even OpenAI, which goes really fast, has\...\
you know, they\'ll retire GPT-40 two or three years after the fact. And so I would not expect Opus 4.6 to like just disappear and not be available anymore, but it is expensive for them to operate. So they.\
One of my findings is that by moving everyone onto Opus 4.7, they\'ve saved a lot of compute on their end. The way that Opus 4.7 works is really not ideal for a use case like this.\
That\'s the summary of where we\'re at.

**\
Val Levitan** 29:55\
But, but, but thank you, I appreciate it. If I understand correctly.\
Lena\'s particular use case.\
Yes, only complicated because she needs to\...\
couple images with the transcript. The transcript part of it, from what I gather, works quite well.\
It\'s just touching the images.\
to the transcript that is not reliable.\
And I question whether it\'s the right, the actually right flow of\...\
Ohh.\
Work.

**\
Lena Zhukova** 30:46\
Yeah, I touched the images, no more issues, no, no to transfer back.

**\
Val Levitan** 30:46\
Offered that.

**\
Clayton Chancey** 30:47\
That\'s not quite, that\'s not quite the right.\
That\'s, yeah, so really the flow is that we have this Microsoft Teams recording, which takes, you know, which is bilingual essentially, and we use OpenAI Whisper combined with Claude to\...\
to create a more accurate transcription in this microservice that I created. And that has a fixed model that it uses, which is even Sonnet 4.6, and that works well. And that\'s really sort of unimpacted by anything. And then that creates this GitHub record.\
And then what the tool that sort of broke by using a new model was here we have a series of MCP tools that MCP servers that Lena interacts with, which does something very complex by necessity. It says,\
Go find the latest GitHub game development transcript and pull it down, and you\'re essentially, Claude, using this transcript almost like a prompt, because your instructions regarding the images.\
The nature of the JIRA tickets which need to be created, the location of files, all of this metadata which you require in order to actually create something in JIRA lives somewhere in this transcript. And the name of this type of task, if you give a large language model a task,\
that does not have clear parameters but requires it to fetch something and deduct the parameters, that is called multi-needle threading.\
And that Opus 4.6 Anthropic has specifically said vastly outperforms Opus 4.7 in multi-needle threading. So that specific type of prompt where we are saying, I want you to create Jira tickets. But I\'m not going to tell you what Jira tickets you need to create. You need to 1st read a transcript\
Oh, and also in this case, you have a D drive, a mounted Windows disk that you\'re going to look at, and the images and the artwork exists there. And your task is to figure out what hierarchy and structure of JIRA tickets you need to create. There may be 100 of them, there may be\
two, we don\'t know, and which images to attach to those. These are all different tools because of the way the Windows subsystem has been organized. Opus 4.6 is actually pretty amazing at doing that work.\
And there are no discernible, reliable rules that you can derive beyond that, which are always true in every case, because the team may decide that actually we want to use a different image, or the structure should be slightly different, or we want to name something, or maybe it\'s a new game that\'s like actually a convention that hasn\'t been reused before.\
And so there are all these rules that, well, we can\'t account for this, we can\'t account for that. The most reliable way to do that work programmatically is to rely on Opus 4.6 to infer it all.\
But when Opus 4.7 was set as the new default for Claude Cowork, which was Anthropic\'s decision to save compute costs for themselves.\
that specific type of task, multi-needle threading, that model performs very poorly at, and so it performed very poorly for us. So that\'s my understanding of the flow and then how this model.\
Sort of interacts with that flow.

**\
Val Levitan** 34:44\
I, I, I understand what you\'re saying, but\...

**\
Lena Zhukova** 34:44\
And\...

**\
Val Levitan** 34:48\
Can we not look at this job?\
maybe from a different perspective. Number one is the complication there because specifically because Lena.\
Works in Windows.\
Or could this multi-thread, multi-needle threading?\
Could that be split into\...\
sub operations.

**\
Clayton Chancey** 35:20\
I don\'t believe so.

**\
Val Levitan** 35:21\
Uh.\
Which case, first, second, or both?

**\
Clayton Chancey** 35:27\
Both, both.\
Both, because Cowork, which is the which is the client that Lena is using, called Cowork, does support mounted Windows drives now, so\...

**\
Lena Zhukova** 35:42\
And it works here and worked perfectly. Remember, like I when I created for Dragon base structure, it worked perfectly like your MCP with previous transcript. It worked very well with Windows.

**\
Clayton Chancey** 35:45\
What?\
Yeah.\
So it supports Windows now, now that we\'ve put some work into it, and then Anthropic has also updated Cloud Cowork so that that works. It\'s complex, but it\'s not necessarily more complex than it would be for Mac or Linux now. So we kind of.\
That was true, uh, you know, three weeks ago, and now it\'s not, so that\'s sort of resolved.\
And then the fact that the idea that this process could be broken down into discrete parts.\
Um\...\
I personally seriously doubt that it could that we could do that reliably.\
I mean, maybe it\'s possible that we can do that, but\...\
In my mind.\
There are significant loss typically in the business process that comes from.\
Breaking down a high context task into discrete, deterministic.\
processes because they have to relate to each other.\
That would be the tough part, is that if you break down the decision-making here for this business process, each of the small, easy tasks that Claude would need to do is dependent on the success or failure of another task, and so you have to build this super.\
A complex engine that essentially approaches the complexity of a large language model itself, and so from a\...\
Resource perspective, you may as well just.\
ask a large language model to do that, since what it does is hold a lot of different data points in inference and then simulate the process of reasoning through that. And Opus 4.6, as we\'ve proven, can do that well. So that gives us this sort of durability.\
where different decisions, edge cases, ideas could be had in that transcript. People could talk about and discuss different ways of doing things and kind of no matter what they decide, Opus 4.6 has the tools needed to accomplish that. And if we break that process down into more deterministic

**\
Val Levitan** 38:14\
Yes.

**\
Clayton Chancey** 38:34\
Process then.\
Then a different decision breaks the engine, and now you have this brutal.\
Process, but I mean, that\'s my way of thinking about it anyway.

**\
Val Levitan** 38:46\
And to what degree using 4.6, what degree of reliability does it work now?

**\
Clayton Chancey** 38:55\
It has always worked pretty high for us. It\'s just a matter of getting the\...\
The images uploaded, which we which we just crossed that threshold, and Opus 4.7 is essentially not, it\'s a non-starter, it\'s\...

**\
Lena Zhukova** 39:03\
Yeah, that\'s it.\
I.

**\
Val Levitan** 39:09\
Chrome.\
Cross, cross that, cross that bridge now. You mean it\'s working now with 4.6?

**\
Clayton Chancey** 39:15\
It\'s.\
Yes, it\'s working now with 4.6. We just, I\...

**\
Val Levitan** 39:25\
Sood to which?\
How reliable does it work with 4.6? Is it reliable enough that we can start going with it?

**\
Clayton Chancey** 39:36\
Yeah, I think so. I mean, I have to submit, I have to finish what we set out to do a few minutes ago here, which is, as we\'ve been talking, Cloud Code is updating the configuration. But I think\...\
that we are able to, hold on. I think that we are able to get this.\
push to GitHub, hold down on Lena\'s machine, and then we need to do another test here just now. And then this should be reliable enough to use in production as opposed to production and sandbox, which is where we\'ve been testing. The Opus 4.7 introduction like.\
came at this last minute right before we were ready to move to production and completely threw everything into disarray and forced me to figure out what on earth is happening with the reliability and then prove that it\'s Opus 4.7, which I did.\
So now we\'re back at the place where we can promote this and start using it in production.\
So, I\'ll share my screen just so that you guys can see what I\'m doing as I\'m as I\'m here.\
Share this.\
So, we\'ve made all these changes to the tools to support that specific use case we discussed, Lena.\
I\'m going to say if GitHub off and switch to my JVL GitHub account to make the push.\
The.\
It\'s going to update some documentation automatically. So this is.\
the piece that we needed to change.\
And.\
Oh.\
OK.\
So now, Lena, if you can share again, we can pull this down and test it again.\
So if you can open up, yeah, there and then go to the IP underscore MCP.\
I think you might have to do it with capital.\
Uh, capitalized letters just to\...\
Oh, I\'m sorry, you know what, it\'s CD.

**\
Lena Zhukova** 43:00\
Okay.

**\
Clayton Chancey** 43:01\
Yeah, it\'s that it\'s that exact command, so perfect.\
And then you can just say, pull down the latest version from GitHub and.\
Run, build.

**\
Lena Zhukova** 43:29\
Yes.

**\
Clayton Chancey** 43:30\
Yes, yes indeed.\
Okay.\
You can go ahead in the background, you can quit Cloud Cowork, and then we\'ll have to re.

**\
Lena Zhukova** 43:47\
Uma.

**\
Clayton Chancey** 43:51\
Let me start it again in a second.

**\
Lena Zhukova** 43:55\
Mhm.

**\
Clayton Chancey** 43:57\
Okay, let me just check the bill number here really quick. 99E4DD. Okay, cool.\
All right.

**\
Lena Zhukova** 44:05\
Open, open cloud desktop, yeah.

**\
Clayton Chancey** 44:09\
Yeah, yes, correct.

**\
Val Levitan** 44:12\
If at the end of this meeting, if possible, would you please circulate the recording? I\'d like to understand that we are at the end. Okay, thank you very much. Bye-bye.

**\
Clayton Chancey** 44:17\
Yes, absolutely.\
Yeah, sure.\
Okay, bye.\
And let\'s click that same D drive folder.\
Um\...\
And then I\'m giving you a slightly updated prompt that asks for at least 10 JIRA tickets. So if you can take that from the Teams chat, then we can.

**\
Lena Zhukova** 44:52\
Yeah.

**\
Clayton Chancey** 45:03\
You can test that out.\
Alright.\
\*\*\*\*.\
Go ahead and hit allow.\
Yeah.\
And then.\
Just to.\
Default number one.\
Okay, cool. See, there we go. Now it knows what it\'s doing. Eleven tickets based on twin bison features, each with the relevant comp art image. Go ahead and hit allow.\
Yeah, it still has that same thing I ran into last time, but that\'s fine.\
And then scroll down. I just want to see this at working. Allow.\
Let\'s see if this is successful.\
Cool. Okay. That seems like a positive result. We\'ll wait for it to finish and then we can confirm.

**\
Lena Zhukova** 47:53\
Mhm.

**\
Clayton Chancey** 47:57\
Push.\
You can hit always allow, yes.\
Yeah.\
Okay, cool. And then once it\...\
Finishes weekend.\
Look through some of these tickets and see.

**\
Lena Zhukova** 49:38\
And now it looks like it worked before, like it was very, like very successful when it created structures for Dragon Base, but now it\'s using like on D drive, because before it used.

**\
Clayton Chancey** 49:51\
Yeah.\
Yeah.\
Yeah.

**\
Lena Zhukova** 49:56\
But process was, I like this process, so it gives me links to to each feature, so I like.

**\
Clayton Chancey** 49:56\
Yeah, I think this.\
Yeah.\
Why don\'t we just click into some, like, just kind of spot check this, look at some of those tickets and see that the images were attached well.

**\
Lena Zhukova** 50:15\
Yeah?

**\
Clayton Chancey** 50:19\
Cool.\
Cool.\
If we just check one more.

**\
Lena Zhukova** 50:26\
I have a good check in.\
Yeah.

**\
Clayton Chancey** 50:34\
OK, cool.\
Okay, so we have 10 minutes.\
I guess the outstanding question for me is, do we want to go switch this into production?\
Or do we want do you do you want to test and experiment more?\
I\'m fine to do either, although\...\
Let me think.\
You know, let me just quickly ask my claude, just for my own peace of mind, is there anything that we would want to test specifically, or any approach we would want to take before?\
Basically, setting aside the sandbox and working on me in production.

**\
Lena Zhukova** 51:25\
And let me also, like, go like more in detail. I will read the descriptions for each features. I will see, like, yeah, I don\'t see stories, because we didn\'t ask for stories, so yeah, yeah, yeah, let me let me do a couple of prompts by myself, so then let\'s see how it does go, and I\...

**\
Clayton Chancey** 51:37\
Okay, so you want to\...\
Yeah, yeah, yeah.\
OKOK.

**\
Lena Zhukova** 51:50\
I will let you know, because for now I see like the creation, like the list of features and image attachments is very accurate, but let me check more and let me make a couple of prompts to creating stories inside, according on this transcript.

**\
Clayton Chancey** 52:04\
Okay.\
Okay, that works.

**\
Lena Zhukova** 52:09\
And one more question: will it delete issues in production? So, if I ask, because sometimes I need to delete like like unnecessary features or for deleting, it\'s better to use Aaron\'s add-on.

**\
Clayton Chancey** 52:12\
Yeah.\
I think we can delete. Let me check. Is there a delete issue tool in this NCP? Because this is based on a tool that I built for someone else like a long time ago.

**\
Lena Zhukova** 52:43\
It can ask one more time when I prompt him to delete something and can say, okay, okay, I\'m going to delete this and this, are you sure? And then like, yeah, it would be nice to.

**\
Clayton Chancey** 52:53\
So no, there is not a tool that deletes an issue, but it can delete like a release and it can remove issues from a release, but we don\'t have a delete issue tool. I can add one if you would like. I mean, it\'s very simple. I can add one if you would like. It\'s easier.

**\
Lena Zhukova** 52:57\
And.\
Mhm.\
Would be nice, because in this case, I I will not need to switch between UMCP and Aaron MCP, because I know that Aaron MCP can do it to do some like deleting as well, this to get started without the operation.

**\
Clayton Chancey** 53:19\
Okay.\
Okay.\
Okay.\
I will add, I will add one now. So I\'ll add that and then commit it. And then you are going to test and examine and refine a little bit. And then when we meet on Thursday, if you can have any feedback or thoughts, I mean, you can send it to me on Teams, of course, but also.

**\
Lena Zhukova** 53:41\
Mhm.\
Yeah.

**\
Clayton Chancey** 53:48\
I think it would be great to figure out, can we turn this on to production? And then the process of doing that is simply, we will go into your machine, we will ask Claude Code to change the URL so that instead of looking at production and creating in sandbox, it\'s now looking at production.

**\
Lena Zhukova** 53:51\
Mhm.\
Yeah.\
Mhm.

**\
Clayton Chancey** 54:07\
and creating in production. So it\'s one line change, and then we\'re in production. And so that would be a very, very quick change, and we\'ll ask Cloud Code to do it for us.

**\
Lena Zhukova** 54:07\
Yeah.\
I\...\
Mhm.\
So yeah, and I would, yeah, I would like you to check if you can add delete and archiving also, like, because sometimes you need to archive.\
Some IPs, so also would be nicer, so I would, I can say like archive all IPs under, like, I don\'t know, like Georgia or South Dakota, because we finished with this market for now, so\...

**\
Clayton Chancey** 54:39\
Okay.\
Okay, I can, I have the delete one as I just, Claude just finished building it and I\'ll build an Archive one as well. And then, and then you\'ll get feedback and when we meet next week, we will either resolve any feedback that you find and or.

**\
Lena Zhukova** 54:56\
Really?

**\
Clayton Chancey** 55:02\
Go ahead and turn this on so it\'s live.

**\
Lena Zhukova** 55:03\
Inna.\
And if we will move it to production, I would also ask you how can I proceed with propagating this MCP to my like 2 team leads. So should I, will I ask Andrei to do it? So.

**\
Clayton Chancey** 55:16\
Yeah.\
Yeah, yeah, we\'ll ask Andrei. All, that\'s another action item for me then. I will make sure that the documentation in GitHub, this is all in the JVL GitHub, includes information about installation and configuration so that Andrei can do it.

**\
Lena Zhukova** 55:29\
I.\
And.

**\
Clayton Chancey** 55:42\
remotely, which I think he can do.\
Do you know, do they also have Windows machines?

**\
Lena Zhukova** 55:51\
Mhm.

**\
Clayton Chancey** 55:52\
Okay, well then it\'s the same environment as yours. So I will also update the GitHub with instructions to\...\
Provision other other devices, and that way Andrei can can either do it remotely or can help assist, and I can assist too as well, but that.\
That would be good. Yeah. Okay.

**\
Lena Zhukova** 56:16\
Okay, great. And maybe what we can do, maybe tomorrow we will record another, like, like shorter team meeting, just to check one more time this process with transcript, how it goes to GitHub and everything. Okay, so just one more time, yeah.

**\
Clayton Chancey** 56:17\
No problem.\
Yeah.\
Okay, yeah, that\'d be great.\
Okay. All right, cool.

**\
Lena Zhukova** 56:36\
Okay, great. So I hope like on Thursday we will move it to production. Yeah, I really do because I was the last result looks very good.

**\
Clayton Chancey** 56:37\
Awesome, thanks so much.\
Yeah, I\...\
Yeah, cool, and then I will, I\'ll post the Challa lengthy transcript here in the chat for Val.

**\
Lena Zhukova** 56:47\
Thank you very much, Clayton.\
Mhm.

**\
Clayton Chancey** 56:56\
All right, awesome. Thank you so much, Lena. See you Thursday. Bye.

**\
Lena Zhukova** 56:58\
Thank you, thank you, bye-bye.

**\
Clayton Chancey** stopped transcription
