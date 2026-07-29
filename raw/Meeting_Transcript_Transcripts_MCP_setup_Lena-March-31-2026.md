**Clayton-Aaron-JVL-20260331_140027UTC-Meeting Recording**

March 31, 2026, 2:00PM

1h 14m 32s

**\
Clayton Chancey** 0:34\
I\'m right now. How\'s it going?

**\
Lena Zhukova** 0:36\
Hi, Peter. How are you?

**\
Clayton Chancey** 0:38\
I\'m doing good.\
I think.\
I think we are waiting for Val who wanted to join or who responded to join.\
Yeah, everything working pretty well. Um.\
So what I think we\'ll do today is I\'ll explain how things work and then we can we can.

**\
Lena Zhukova** 1:12\
Mhm.

**\
Clayton Chancey** 1:16\
We can pull down the latest version of the MC tools.

**\
Lena Zhukova** 1:21\
Mhm.

**\
Clayton Chancey** 1:23\
And then we\'ll have to. I added a. I added a new feature in the MCP that accesses this transcripts repository in GitHub and so we need to create an access token.

**\
Lena Zhukova** 1:34\
Mhm.

**\
Clayton Chancey** 1:39\
For your account in GitHub, which also has authorization through the JVL single sign on with Microsoft, and so that\'s a process which I\'ll walk you through how to do it. It\'s pretty fast, but then we we can plug that token for your user account we can.\
Plug that token into the MCP configuration in Cloud and then it will it will pull these these transcripts down from GitHub and and use them to create the games so.

**\
Lena Zhukova** 2:03\
Mhm.

**\
Clayton Chancey** 2:15\
Um, I will.

**\
Lena Zhukova** 2:16\
What about your research to include messages from chat? It\'s not. It\'s interesting because it\'s not going to be transcript anymore. It\'s kind of like a summary, but it.

**\
Clayton Chancey** 2:31\
Yeah, yeah, I.

**\
Lena Zhukova** 2:32\
I don\'t know. I don\'t know what it\'s important to instructions to create some issues in JIRA, but from other side it\'s not a clear transcript already. It is a kind of like a summary.

**\
Clayton Chancey** 2:39\
Mhm.\
Yeah, yeah, I am working on it, so it\'s still in progress. We can, I I think what I want to do is get this working really well if it seems like.\
If it actually works for you well, then we add the chat. I I would rather increment slowly and make sure that each piece works. So hey Val, we were we were just waiting to get kicked off. So hey.

**\
Lena Zhukova** 3:04\
OK, OK.

**\
Val Levitan** 3:11\
Hi, everyone. Hi, guys.

**\
Lena Zhukova** 3:13\
Hello.

**\
Clayton Chancey** 3:14\
So we made very good progress. I want to explain briefly what I did and how I expect it to work and then I will get.

**\
Val Levitan** 3:22\
Is the recording on? Is the recording on?

**\
Clayton Chancey** 3:25\
It is. It is on. It is on and no, you\'re good. And in fact it should be working now where within 10 minutes of the finish of this call, this now also gets uploaded to our GitHub.

**\
Val Levitan** 3:26\
Thank you. Thank you for interrupt. Sorry for interruption.

**\
Clayton Chancey** 3:40\
Transcripts are repositable.

**\
Val Levitan** 3:41\
And how do I get access to this recording?

**\
Clayton Chancey** 3:45\
Well, there\'s a number of ways, but through this MCP server, which I will, that\'s what we will do today on the call is get get this configured. Let me explain what I did briefly so we understand and then there are already some ways that we can enrich this further, which we can pursue.\
OK, So what I have done.\
And I have created this microservice within JVL which is an API that allows you to send information from Microsoft Teams into this API and after a few moments what it spits out is a well actually what it does is it uploads.\
Automatically a transcript to this repository.\
And can you guys see my screen which I\'m sharing just to confirm. OK, OK, so this is an explanation sort of of what it does and the structure. But you\'ll see for example if I go into the transcripts folder here. Now the idea is you probably never need to interact with this.

**\
Val Levitan** 4:40\
Yes, yes.

**\
Clayton Chancey** 4:55\
Through the GitHub user interface, because we want to make this is now available to Claude through MCP. But for example, here\'s some of the pipeline test calls and then here\'s one that the reason that I can tell that Andrei set up the Google or the Microsoft Power Automate script.\
Is because already 19 hours ago some call happened here, which I think was Aaron with with Aaron Bockley. So these calls are coming in here and they\'re organized by date, which is accessible to Quad.\
So for example, I can click into this meeting transcript and this is the this is the transcripts that you gave me, Lena. So this is a little bit of a strange case because it\'s not yet happening in real time. So I put pipeline test here in the name.

**\
Lena Zhukova** 5:48\
Mhm.

**\
Clayton Chancey** 5:49\
But then it gives us the full transcript and this and this is just what\'s coming out of my API and then at the end the terminology key which I\'m keeping this here because this can be used to also this is not this is one thing we can now implement to further enrich the process is this can.\
Can be used to update the glossary, the GitHub glossary so that these become new so that as if you use new language or new things you can you can create like a pull request with the terminology key and then someone who knows.\
The the slang can review the pull request to the glossary repository and filter that as needed. So this becomes this like this feedback loop. But what this lets us do is this lets us use our MCP Sir, let me.\
Um.\
Let me show you an example.\
Uh, I think this is called at last. Let me actually see what is the name of my.\
Less in MCP.\
Yeah.\
So.\
What this lets us do is like I have an instance of cloud code here which is connected to this MCP.\
And so I could look at. This is a little bit different Lena than your Cloud desktop, but it\'s just showing you how this all feeds together. If I was to go look at, so I have this JVL Atlassian MCP connected to this instance of Claude.

**\
Lena Zhukova** 7:43\
Mhm.

**\
Clayton Chancey** 7:50\
If I was to click in here and look at the tools which are available, we have all of these tools here which we already have tested out. These are the ones that you and I have already tested for creating games and navigating JIRA and attachments and all of these. You can see this attachments thing here, which also.\
Another item I\'m working on is how do we get that from your from your D drive. But all of these different things that we can do and then at the end, so the two new tools are related to transcripts, which we will see down here somewhere.\
List transcript and get transcript. What this does now is this does not connect to Jira, this connects to that GitHub instance and so there is a.\
There\'s a new arameter which we will. This is what we will have to set U for you today. This GitHub Personal access token is a new.\
Field which we need to provide to the MCP server configuration and everything else you already have configured, but this it will be a new one. So we will pull. Today we\'ll pull down this MCP server, we\'ll create a GitHub access token and make sure that it is logged in with your SSO so everything is audited.\
Through the JVL security and then we will add it here and by having this token what this lets this lets that the same MCP server which is able to create Jira issues and investigate the game design.\
Structure can also now go to that GitHub repository and get this more correctly translated transcription of the call. And so we\'re bringing it all of that different sources of intelligence kind of into the one engine which can then create a.\
A game from the transcript.

**\
Lena Zhukova** 9:46\
So it will use our glossary from GitHub because it can it might be like updated like so and it all the time it will use the latest version of this glossary OK.

**\
Clayton Chancey** 9:59\
Yeah, so my API, which is actually performing the translation, is using that glossary. So so here here\'s the end to end flow of the whole tool. The way it works is there\'s a meeting which takes place in Microsoft Teams.\
And then after that meeting has processed and the recording and the transcript are available, there is a Microsoft Power Automate script which Andrei wrote and deployed after any meeting takes place.\
Now this Microsoft Power Automate script takes those audio and transcript and then we will need to work on the chat piece as well. As you mentioned, it takes those and it feeds them into this microservice that I created. This microservice takes those ideas and also gets whatever the latest glossary is.\
From GitHub.\
And runs it through this pipeline, which does several things. It\'s somewhat complex, but it produces.\
A more accurate transcription and then and then it automatically sends that to GitHub. And so that is 1 little thing which happens automatically with no human action. And then anytime that you want to create a game from that transcript.\
You can just now if you have this all connected, you mentioned I had a meeting on Wednesday or this last Wednesday or on such and such a date or with such and such a name and I want to create a game from this transcript. Let\'s work on the plan.

**\**
11:26\
Uh.

**\
Clayton Chancey** 11:35\
And so then Claude, using this MCP server, goes to GitHub using this access token. It\'s authenticated with your user account. It searches for the right date and the the name and the participants finds the meeting.

**\
Lena Zhukova** 11:44\
Hello.

**\
Clayton Chancey** 11:53\
And then analyzes the entire transcript, which is now much more accurate than what we could get from Microsoft Teams, and then also goes and investigates as we have kind of described. Now you know how it\'s working. It\'s kind of this familiar thing of it going and investigating the existing JIRA.

**\
Lena Zhukova** 11:59\
Mhm.

**\
Clayton Chancey** 12:09\
Configurations and conventions and this transcript and then proposing a plan of what it should create, which you can, you know, iterate or you know, describe how you would like it to change. And then when you accept the changes, then it pushes all of these changes to JARA.

**\
Lena Zhukova** 12:26\
Mhm.\
And if you\'re discussing like several projects during the meeting, because it\'s usually the case, it\'s rare case when we discuss only one game, it\'s maybe only in the beginning of the project when we are just creating like so usually we\'re discussing like several.

**\
Clayton Chancey** 12:39\
Mhm.

**\
Lena Zhukova** 12:45\
Projects under markets, so it will cover like proper IP and suggest like proper changes and proper spaces, right?

**\
Clayton Chancey** 13:00\
Well, we\'ll see.

**\
Lena Zhukova** 13:01\
OK.

**\
Clayton Chancey** 13:02\
We\'ll see. I mean, you know the.\
The thing with these tools is they\'re not very deterministic, so it\'s all about testing and seeing. So what I would like to do now.

**\
Lena Zhukova** 13:14\
Mhm, OK.

**\
Clayton Chancey** 13:18\
Is I will disconnect from all this. I don\'t think I really need any of this up.\
And then I will get back here and stop sharing and then maybe Lena, you can share your screen and we can get your MCP server updated, your GitHub token created and then and then make sure that that\'s working.

**\
Lena Zhukova** 13:38\
Mhm.

**\
Clayton Chancey** 13:47\
And then we can.\
We can go to you Val and this this. If this is working with Lena, then we\'ll we\'ll definitely be pretty easy to implement for you as well. OK, so let us go to let\'s do CD.\
Space.

**\
Lena Zhukova** 14:13\
Sure.\
Let me.

**\
Clayton Chancey** 14:16\
Yes, actually, yes, that whole that whole string you can actually you can hit run. That\'s perfect. So now let\'s say pull down the latest version.\
Of this tool.\
Or let\'s say pull down the latest version from GitHub.\
Yeah, perfect.\
And then you can do number one.\
And it says that it also found the new transfer tools, so say just say yes.\
And then what we can say is can say um.\
Open the.\
MCP.\
Jason.\
This is yeah, Jason settings file in a text editor.\
So that I can.\
Provide GitHub PAT.\
It.

**\
Lena Zhukova** 16:14\
What? What?

**\
Clayton Chancey** 16:14\
PAT Personal access token. I think it should know that.

**\
Val Levitan** 16:20\
OK.

**\
Clayton Chancey** 16:22\
PAT.

**\
Lena Zhukova** 16:24\
Makes sense.

**\
Clayton Chancey** 16:25\
Yes, yes, perfect.

**\
Lena Zhukova** 16:27\
Mhm.

**\
Clayton Chancey** 16:29\
We could probably give this token to Claude and it would configure it, but it is more secure to just do it this way so you can hit yes.

**\
Lena Zhukova** 16:41\
Um.\
I can\'t this.

**\
Clayton Chancey** 16:47\
OK, can you say hit OK and then just hit escape briefly?\
Hit escape again. Oh, yeah, that\'s actually good. That\'s what I was going to say is open it with notepad. So yeah, just hit Yes to accept that. There we go. Okey doke.

**\
Lena Zhukova** 17:02\
And.

**\
Clayton Chancey** 17:11\
So now.\
So interesting.\
Oh, OK.\
It\'s strange because this does not have the GitHub.\
Pat, let me check one thing.\
Thing.\
Is it possible that I did not push the new template for the environment file? It is possible.\
One moment.\
It\'s.\
Oh wait, this is not the right file. That\'s why this is a dot ENV file. So actually you can close this and this probably is why.\
So then.\
Um.\
Let me just this might be.\
Sorry, one moment. I may have actually like accidentally ignored one file which I needed to push to you. So let me check this really quick.\
OK.\
Let\'s see.\
OK.\
OK.\
OK. I think we\'re actually OK. So then you can.\
You can ask. Why don\'t you just say open that again in notepad?\
As usual, when I think there\'s something wrong, it\'s actually me that was wrong and not Claude. It is. It is actually you can hit #1.\
Uh.\
Hit cancel.\
No one is.\
No.\
Um.\
Yes.\
Man, Windows is frustrating. Can you say?

**\
Val Levitan** 21:11\
Yes.

**\
Clayton Chancey** 21:14\
That file was blank.\
And hit yes.\
Um, hit yes.\
That\'s good. And then.\
And then hit yes.\
Yes.\
And then let\'s screenshot this and give it to Claude because I don\'t know why notepad. It\'s like don\'t don\'t cancel yet. Just screenshot this whole this whole piece. Yeah, and then we want what we\'re gonna need to do is I need to then.

**\
Lena Zhukova** 22:30\
Um.\
Page.

**\
Clayton Chancey** 22:39\
Drag this screenshot into and you can drag with shift.

**\
Lena Zhukova** 22:42\
Um.\
It doesn\'t work. We use some combination of keys. Remember, like we already had this problem. I can don\'t remember this.

**\
Clayton Chancey** 22:51\
Mm-hmm. Yeah. OK, yeah. Windows, right? Yeah. Windows doesn\'t let you do this. Um.\
OK, well then in that case it\'s OK. It\'s it\'s just kind of a we can if it if it\'s not easy then it\'s not worth it. But.

**\
Lena Zhukova** 23:03\
Mhm.

**\
Clayton Chancey** 23:11\
Let\'s you know what? Let\'s work on getting a GitHub access token for you and we will tell Claudecode to copy it from somewhere and that is also safe. So you can close that notepad.

**\
Val Levitan** 23:26\
Mhm.

**\
Clayton Chancey** 23:33\
Now let\'s um.\
Let\'s go to, um, open, you know, Chrome or whatever web browser and go to the.

**\
Lena Zhukova** 23:46\
Oh, I found it. I think it\'s the alt V. We can use alt V and uh.

**\
Clayton Chancey** 23:47\
GitHub instance.

**\
Lena Zhukova** 23:53\
Let\'s try because it\'s no, it\'s not working.

**\
Clayton Chancey** 23:57\
Oh, no, that that works. That works.

**\
Lena Zhukova** 23:58\
Uh, yeah, yeah, yeah, yeah.

**\
Clayton Chancey** 24:01\
Um.\
Yeah, so actually just say this is all I see and then hit enter.\
And then hit yes.\
And then hit yes.\
Um, OK, let\'s uh, let\'s say.\
I close the window and I need you to open it again correctly.\
Anything else?\
There we go. OK, now we can leave this open and just keep this there. Now let\'s open a web browser and you can navigate to this URL which I sent to you in the Teams chat.

**\
Lena Zhukova** 25:31\
So.

**\
Clayton Chancey** 25:45\
And then and let\'s make sure that you can actually get there.

**\
Lena Zhukova** 26:00\
So go to data.

**\
Clayton Chancey** 26:03\
Oh, I sent you a URL in the Teams chat.

**\
Lena Zhukova** 26:05\
Oh, yes.

**\
Clayton Chancey** 26:16\
So yeah, sign on.\
OK, good. So you have access. So then here\'s what we\'ll do. We\'ll set up your access token. So go to your profile in the top right and click the profile picture and then go to settings.

**\
Lena Zhukova** 26:33\
Mhm.

**\
Clayton Chancey** 26:34\
And then on the left, Scroll down to the last item on the very bottom which should say for settings and then go to Personal access tokens and click Tokens Classic.\
And on the top right select generate new token and generate classic which is the second option and then we can let\'s call this transcripts.\
Uh, under score MCP.\
And then let\'s set the expiration pretty far out. So let\'s make it like, yeah, a year. Yeah, perfect. And then just check the very top box that says repo there. That should be all that you need. Yes, perfect.\
Scroll down.\
And hit generate token.\
Now copy this token. There\'s a little button at the end of it. Click that.

**\
Lena Zhukova** 27:41\
OK.\
Mhm.

**\
Clayton Chancey** 27:46\
And go to your notepad.\
And paste that after the very last equal sign at the very end of the text.

**\
Lena Zhukova** 27:56\
Yeah, yeah.

**\
Clayton Chancey** 27:57\
Yes, with no space, just just paste and then and then save this.

**\
Lena Zhukova** 28:02\
Thanks.

**\
Clayton Chancey** 28:05\
Yeah, perfect. And now go back to to the web browser.

**\
Lena Zhukova** 28:09\
I got.

**\
Clayton Chancey** 28:10\
And then there is a thing that says configure SSO in the yes. So then go to JVL core.

**\
Lena Zhukova** 28:21\
Mm-hmm. OK.

**\
Clayton Chancey** 28:21\
And hit authorize.\
And then continue.\
And continue.\
OK, great. So now I\'ll go back to cloud code.\
And say I.\
Included the PAT.

**\
Lena Zhukova** 28:55\
You, you, you, you.

**\
Clayton Chancey** 28:55\
So it\'s PPPAT. Yeah, yeah. And then just hit enter.\
And hit yes.\
OK, great. So now let\'s open Cloud Desktop.\
And let\'s check the oh, actually you can.\
Uh, why don\'t you click relaunch \'cause there\'s a new version that just came out apparently. So there\'s that small little window with the leaf what you see there. Yeah, you can just hit relaunch.

**\
Lena Zhukova** 29:49\
Mhm, mhm.

**\
Clayton Chancey** 29:54\
And then once it comes.\
Back up, which may take a second.\
Maybe.

**\
Lena Zhukova** 30:09\
So it\'s not coming back.

**\
Clayton Chancey** 30:11\
OK, I guess you can just Click to open it the.\
It\'s always something with cloud and windows. It\'s like, oh my, OK, scared me for a second there.\
It.

**\
Lena Zhukova** 30:26\
It\'s not opening at all, so like it\'s stuck and I need to reboot the whole computer and then it starts to work again.

**\
Clayton Chancey** 30:28\
Yeah.\
So let\'s check that the tool the tools are loading. So click that little plus. Oh yeah, that\'s that also works. Yeah, and then connectors and then JVL Atlassian and go to configure.\
And then Scroll down to the bottom and let\'s see that the transcript tools.

**\
Lena Zhukova** 30:51\
Sports.\
Yeah.\
I\'m not sure if you think.

**\
Clayton Chancey** 31:04\
Yeah.

**\
Lena Zhukova** 31:05\
It was there and suddenly it\'s not. It\'s not connected.

**\
Clayton Chancey** 31:13\
Let\'s let\'s try it out anyway, because this might be part of their new way of registering tools. I think it\'s OK Let\'s let\'s try to work and you got to go to I think a new task. So let\'s.

**\
Lena Zhukova** 31:29\
So they specifies the folder or no, not we\'re going to talk.

**\
Clayton Chancey** 31:33\
No, I think it\'s OK. Let\'s just let\'s type in.\
Let me send you a prompt that I know works for me and then we\'ll see if it works for you. I want to create a a game from last transcript.

**\
Lena Zhukova** 31:42\
And that\'s the.\
Mhm.

**\
Clayton Chancey** 31:58\
So try this prompt.\
Uh, and let\'s just see if it works. The reason I\'m.\
Saying this is because the date that was put in the.\
GitHub transcripts repository is as if it was from last Wednesday, so let me do that.

**\
Lena Zhukova** 32:19\
Mm-hmm. OK, yes. Because it\'s not like a.

**\
Clayton Chancey** 32:24\
So let\'s see.\
Right. It was not really from last Wednesday.\
Sorry, one second.\
Yeah.\
Thanks.\
Um.\
OK.\
So it\'s finding the transcripts. I think probably both of those are asking are from the same day in my pipeline, which is good. So it\'s dealing with some ambiguity here by asking. So let\'s do.

**\
Lena Zhukova** 33:12\
I think one which was my my daily meeting with art department and another was our like a game development meeting with stakeholders.

**\
Clayton Chancey** 33:22\
OK, let\'s click just #1.\
So if you click click that first option there that it gave you.\
Um.\
Interesting. This is a little strange here. Why don\'t you instead you see these little, these little?

**\
Lena Zhukova** 33:49\
Yeah.\
Yeah.

**\
Clayton Chancey** 33:58\
Tool things in the chat where it says like used a tool or used two tools. Can you Click to expand that first one? I just want to see.\
What this is?

**\
Lena Zhukova** 34:14\
It is interesting that it\'s starting to ask the strange questions because before like we worked, he understand completely that he needs to work with Jira and Jira issues.

**\
Clayton Chancey** 34:20\
Yeah.\
Yeah, I don\'t think it\'s. I don\'t think it\'s actually reading our tools. I think it\'s it\'s doing something else that\'s not because we saw that our tools did not show up. So it\'s doing something else that is not related to.

**\
Lena Zhukova** 34:35\
Mm-hmm. Yeah. Maybe it\'s disconnected. It\'s really, it\'s really disconnected. Yeah, yeah.

**\
Clayton Chancey** 34:40\
Yeah, this is not related to anything that we built. This is something Claude is doing, so we need to actually find what this is. So if you can click in the first one where it says list sessions and then click this result.\
Ah, yeah, yeah.\
What it\'s doing is it is reading your previous chats with Claude.\
So this is remember some sessions ago. This is where I was kind of saying, you know, I have that memory feature turned off because in my experience it actually kind of poisons these interactions.

**\
Lena Zhukova** 35:12\
And.\
Monday.

**\
Clayton Chancey** 35:20\
This is what\'s happening here. This is pretty.

**\
Lena Zhukova** 35:22\
Do you want you want me to go to settings and at your nose this memory? Because in in other cases it it can help. What do I think it\'s unpredicted.

**\
Clayton Chancey** 35:29\
Sure. Um.\
Really. I think.\
We need to figure out why the MCP tool is not registering, because that should.

**\
Lena Zhukova** 35:40\
Mhm.\
I think this is the problem because it behaves so differently when it uses UMCP with UMCP it understands immediately what it should be done.

**\
Clayton Chancey** 35:42\
Um, support the use case.\
Yeah.\
Yeah, so let\'s instead, let\'s go back to settings.\
And then connectors.\
And then JVL Atlassian.

**\
Lena Zhukova** 36:13\
Now it\'s shows.

**\
Clayton Chancey** 36:13\
Yes.\
Scroll all the way down to the bottom.

**\
Lena Zhukova** 36:17\
But somehow not all items are or it should be like this. So some of them with check marks, some of them are kind of like OK, OK.

**\
Clayton Chancey** 36:26\
Yeah, yeah, no, that\'s fine. That\'s fine.\
Um.\
Oh well, I don\'t see anything about the transcripts here, so it\'s not pulling them the most recent one.

**\
Lena Zhukova** 36:43\
Uh, moves.

**\
Clayton Chancey** 36:44\
Um.\
Let uh, why don\'t we do?\
Um, let\'s go back to cloud code.

**\
Lena Zhukova** 36:58\
What goes, uh, on desktop? Yeah, well.

**\
Clayton Chancey** 37:03\
Uh, leave it open for now.

**\
Lena Zhukova** 37:05\
Mhm.

**\
Clayton Chancey** 37:07\
And then go back to cloud code.

**\
Lena Zhukova** 37:07\
Yeah.

**\
Clayton Chancey** 37:09\
Um.\
Say that.\
Oh, you know, I wonder, say that I say I am.\
Trying to use this in cloud desktop.\
And then hit enter.\
It.\
Um.\
Windows. Windows. Um, hit yes.\
And hit yes.\
Yeah, that\'s what I thought. See, it\'s so confused on Windows, it just does not know how to navigate so well. OK, uh, hit yes.

**\
Lena Zhukova** 38:05\
Yes.

**\
Clayton Chancey** 38:17\
That explains it.\
Um.\
So now now we can close Cloud Desktop and reopen it.\
Uh, let\'s check the settings once again.

**\
Lena Zhukova** 38:43\
Um.

**\
Clayton Chancey** 38:51\
And scroll all the way to the bottom.

**\
Lena Zhukova** 38:54\
Don\'t see that now like much more uh items. Uh with uh check mark. Uh no, now here it\'s.

**\
Clayton Chancey** 39:00\
Yeah, no, we we we have it. Actually, we have it. If you, uh, scroll back up a little bit.

**\
Lena Zhukova** 39:04\
Be sure.

**\
Clayton Chancey** 39:08\
Right there that the.

**\
Lena Zhukova** 39:09\
To get transcript. Uh, what\'s going on?

**\
Clayton Chancey** 39:16\
Yeah, can do this. This is actually.\
A.\
Problem with cowork on Windows? Really. Man, they\'re having problems. Uh, open it again with configure.\
If you go to um.\
Connectors. Yeah, see, that just kills me.

**\
Lena Zhukova** 39:43\
It should be here, right? Like in a separate line and it\'s not here.

**\
Clayton Chancey** 39:45\
OK.\
You know, go to go to chat instead of cowork and I wonder if it is more stable there because these are.

**\
Lena Zhukova** 39:56\
Yeah.

**\
Clayton Chancey** 39:58\
Yeah, and then click plus, click the the little plus and and then look at connectors.

**\
Lena Zhukova** 40:06\
No, it\'s not here.

**\
Clayton Chancey** 40:08\
Um, click tool access.\
Um uh.\
And then click this tools already loaded. Yeah, and now now open the plus again and let\'s see connectors.

**\
Lena Zhukova** 40:19\
Let\'s.\
Mm.

**\
Clayton Chancey** 40:30\
That is just really frustrating.

**\
Lena Zhukova** 40:30\
Disconnected somehow and it was connected and like just.\
In one moment it hop and it disconnect.

**\
Clayton Chancey** 40:43\
Yeah.\
Go back to settings. Let\'s see if it if it pulls up again. That\'s yeah, that\'s extremely frustrating.

**\
Lena Zhukova** 40:58\
Hello.\
Restart. Maybe.

**\
Clayton Chancey** 40:59\
Um.\
Well,\
Yeah, you can try to restart. Clearly I need to research the stability of MCP on Windows because this I\'ve heard from some. I mean, I don\'t use Windows, so it\'s really hard for me to test.\
But I was just reading this morning some.\
Some article where whereby people are complaining about the MC like MCP tool registry in Windows and I didn\'t really read the whole thing. I just saw the headline and then now you know 20 minutes later here we are.

**\
Lena Zhukova** 41:43\
Now it\'s connected.

**\
Clayton Chancey** 41:46\
Yeah, well go to Co work while it\'s while it\'s connected and instead of yeah, so let\'s why don\'t you paste that thing about. I want to create a game and see if it see if it loads here.

**\
Lena Zhukova** 41:56\
Mhm.\
The I think the danger here like if it\'s connecting and disconnecting by itself so you can you can work, you can ask something and in the middle of nowhere disconnected, you\'re not even noticing it and it started to give you answers which are not.

**\
Clayton Chancey** 42:02\
Yeah.\
Yeah.

**\
Lena Zhukova** 42:15\
Uh, through your MCP, but just from cloud and it can can be irrelevant.

**\
Clayton Chancey** 42:19\
Yeah, yeah, I know I need to research the what\'s the reliability. There\'s some reliability issue here and is there something we can do specifically to to help this with Windows? I don\'t know. It\'s working here. So this is of course now actually our tool. So why don\'t you hit always allow because this.

**\
Lena Zhukova** 42:34\
Mhm.

**\
Clayton Chancey** 42:39\
Is just for finding transcript, so there\'s no problem with always allowing this. So see now it finds two and then go ahead and hit always allow again.\
This is how we want it to behave, where it is actually going out to GitHub, getting the transcripts very quickly, finding them.\
Let\'s see now. Here we go. Jira issues and features. Why don\'t you hit #1?

**\
Lena Zhukova** 43:20\
Why it\'s it is even asking about playable games.

**\
Clayton Chancey** 43:26\
Well, yes, see clearly they are making these updates to the Windows client and the that\'s the Windows system prompt which they provide behind the scenes, which is something we need to find a way to accommodate for.\
Yes.\
So what I what I want to just see make sure is that these richer transcripts and the process of interpretation which we are providing for Claude is better.

**\
Lena Zhukova** 44:02\
It is interesting that it interpreted the the name of the game wrong again and in previous version it was normal paste like PAYS like paste pay dragon space. Now it\'s paste.\
And it was already like good in previous versions. It\'s interesting.

**\
Clayton Chancey** 44:18\
Oh, interesting.\
Mm-hmm.\
Yeah, well, it may get the see now it did it because it found it in JIRA. See, that\'s that\'s what we want. If you look, it says, oh, good news, the dragon pays, right?

**\
Lena Zhukova** 44:35\
Yeah, now, now it pays. Yeah. Because, yeah, because it goes to Jira. Yeah, yeah.

**\
Clayton Chancey** 44:39\
This is what we want, right? We want a scaffold context so that as it goes through this process, it it like steers itself to the correct understanding. This is exactly right.

**\
Lena Zhukova** 44:41\
Mhm.

**\
Val Levitan** 44:48\
What if? What if the team changes to either Apple or Linux?

**\
Clayton Chancey** 44:56\
Well, it will be a very painful process, but the the MCP tools will work much better. I don\'t know if that\'s if that alone is worth it. I\'m sure Aaron has pushed you in that direction, but it will.

**\
Lena Zhukova** 45:12\
OK, current currently our tools are not working.

**\
Clayton Chancey** 45:13\
This particular small thing which I am contributing, it will work a lot better on Linux or Mac, but that does not mean that everyone should. It\'s probably easier for me to figure out.

**\
Lena Zhukova** 45:25\
Our custom tools are not work will not work under Linux so I mean the tools we are working my graphical tools.

**\
Val Levitan** 45:36\
I\'m thinking of adding another computer, like a small, small, let\'s say Mac, right? That that brick, the little brick.

**\
Lena Zhukova** 45:40\
Oh, mm-hmm. OK.\
Mhm.

**\
Clayton Chancey** 45:48\
And the Mac mini? Yeah, those are.

**\
Lena Zhukova** 45:50\
Hmm.

**\
Val Levitan** 45:51\
Yeah.

**\
Clayton Chancey** 45:54\
Those are great, but you know you can also run those open clouds on those machines.

**\
Val Levitan** 45:55\
And and just help and yeah, and just focus them on on that.

**\
Lena Zhukova** 46:01\
Um, interesting.

**\
Val Levitan** 46:03\
It\'s a cheaper solution than the whole revolution.

**\
Clayton Chancey** 46:08\
Yes, yes.

**\
Lena Zhukova** 46:08\
And.

**\
Clayton Chancey** 46:11\
Yes, that\'s not a bad idea. Um.\
So let\'s.\
Let\'s do both add and update.

**\
Val Levitan** 46:21\
We we we actually need to switch only Lena, right? Nobody else.

**\
Lena Zhukova** 46:29\
By under 10.

**\
Clayton Chancey** 46:31\
That\'s a I don\'t know the answer to that.

**\
Val Levitan** 46:35\
Well, because when when recording is done, it\'s really only Lena who\'s going to.

**\
Clayton Chancey** 46:35\
Um.

**\
Val Levitan** 46:44\
Yeah, do it.

**\
Lena Zhukova** 46:46\
No, my team leads as well. I need to to to Anastasia and Julia as well because they are managing stories.

**\
Clayton Chancey** 47:01\
Anyone who will need to manage Jira.\
From meeting transcripts.\
And using a clog. So I don\'t know if that is the same group of people as everyone who does currently do that. I think that anyone who will do that that is is who would benefit from doing so in neck.\
So what we\'re looking at here is I wanna see that it it\'s basically enriching the content that we already created from previous runs and that\'s.

**\
Lena Zhukova** 47:43\
Mm-hmm. Yeah. I would like to see what he\'s going to suggest. It\'s interesting.

**\
Clayton Chancey** 47:48\
Yes, yeah.\
OK, cool. So this is good because this to me, this means that by doing a better transcript, we are capturing many more details and.\
It is creating a more accurate.\
Richer Jira backlog. So if you Scroll down, I think it\'s asking for some approval somewhere. I saw there. Yeah, so let\'s.

**\
Lena Zhukova** 48:20\
This is this structure. Actually he found it\'s a structure in sandbox which already was created using the.

**\
Clayton Chancey** 48:25\
Right.\
Right, right. So go ahead and let\'s not use always allow, but you can do the small drop down and hit allow once. Yes, correct.

**\
Lena Zhukova** 48:35\
I love that, yeah.

**\
Clayton Chancey** 48:43\
Yeah, so this is good. To me, this means that when when the MCP is working, it\'s working really good. With the transcript, it\'s really good. I know that we\'re almost out of time, so Val, I need to set up. Clearly, we need to set up maybe a separate set.

**\
Lena Zhukova** 49:01\
Oh.

**\
Clayton Chancey** 49:03\
session for you and me to get this working for you.

**\
Val Levitan** 49:03\
Yeah, yeah, yeah. Separate. Separate session. Yeah, yeah, yeah, yeah. Let\'s focus on. Let\'s focus on Lena. Yeah, Lena, I\'m ordering a mini for you now as we speak.

**\
Clayton Chancey** 49:06\
OK, let me.\
OK.\
Awesome, awesome. This would be great. This would be so great. Again, Lena, let\'s do the allow once session here.

**\
Val Levitan** 49:20\
Lena, Lena, Lena, a ton of excitement would be appreciated.

**\
Clayton Chancey** 49:27\
This is.

**\
Lena Zhukova** 49:30\
Mhm.

**\
Clayton Chancey** 49:32\
No excitement. Yeah, well, once we get it working, it should be really exciting. That thing is perfect for autonomous AI work.

**\
Val Levitan** 49:32\
OK, next time.\
Actually, my my Linux is a beauty.

**\
Clayton Chancey** 49:49\
Um.\
Yeah.

**\
Val Levitan** 49:54\
That\'s what a what a savior in in every respect. Yeah. Anyways, yeah, go ahead and focus on them.

**\
Clayton Chancey** 49:57\
Yeah.\
So then I know what I need to do now. I\'m just because we\'re coming up on with 10 minutes left, I\'m lining up for myself mentally and for the transcript. What are my next steps?\
Uh, I think what I need to do is I need to incorporate the.\
The chat comments from these meetings, so anything which the users are entering into a teams chat during the call. I need to interleave these with the transcript because you provide lots of interesting.\
Interesting links and content there, which becomes a source of truth for the meeting and so this will require me to. This is very easy, but I do have to make a change to my microservice and then it is possible that I ask Andre also to change a few lines in his script, but he\'s being extremely.

**\
Lena Zhukova** 50:46\
So.

**\
Clayton Chancey** 50:59\
responsive, so it should be no problem to do this.\
And then secondly.\
Um, to just, I guess, do some.\
Well, I don\'t know now if we have a Mac coming, I think maybe what we do is we, I can do a little research because I have another client which is also on Windows and it is struggle just like this. So I will do a little research, but because we have a Mac coming, it\'s maybe not, it\'s not the end of the world and this.\
Be just easier and also your images will just work on the Mac.\
So we will kind of expect that and treat it like a saviour for some of our problems. But I I still also want to research it because there I have another person who is not probably not going to get a Mac unfortunately, and we can.\
We can see if there\'s any interesting information.\
Uh, Scroll down here.\
Cool.\
I like that it is. You can see that most of that small text above it says it used this integration and it loaded tools. So this is actually really good. This is probably from that latest update it is.\
Instead of looking at all of the tools from our MC per MCP server at once, it is loading the specific one it needs at a certain time and so using them.\
In a way that saves tokens so that this conversation can run even longer, which is really good for us.

**\
Val Levitan** 52:55\
Yes.

**\
Clayton Chancey** 52:58\
Oh, that\'s cool. That is very cool. It\'s updating the features with meeting notice comments. So this is actually something I added. I thought it\'s it\'s cool if it works, but if it doesn\'t then I don\'t need to mention it. But that\'s actually great.

**\
Lena Zhukova** 53:09\
That\'s very nice.\
No, no, it you usually like all our comments when we discuss some parts of the game, they are very valuable and this is this comments from there like we usually create in descriptions so.

**\
Clayton Chancey** 53:28\
Yeah, so that\'s that\'s great. So this is now I\'m happy. This seems to be working really. It\'s the only piece is.\
The reliability on Windows, which I think we\'re getting solved by just moving this process away from Windows and then the teams chat so that and that should be pretty easy.\
Cool.\
One other question that I had actually, and this is probably a good question for Val.\
In the GitHub repository which stores these transcripts.\
I the the way that Andrei\'s script works is that when a meeting is recorded, it becomes automatically this this.\
This transcript in the GitHub repository. Do we need to?\
Like secure some of those? Like are there types of meetings which would be recorded but which we do not want them to go into this GitHub repository where anyone who has access to this repository can access them?\
Do we need to secure or like permission these transcripts so that only certain people can access them or are we OK with it being kind of wide open?

**\
Val Levitan** 55:00\
Yeah, it\'s a good question. And from the moment you start discussing this already a couple of days back, I was thinking whether it should be wide open or managed. I\'m going to the decision is that it should be managed, it should not be.

**\
Lena Zhukova** 55:00\
OK.

**\
Clayton Chancey** 55:14\
Yes.\
OK.

**\
Val Levitan** 55:20\
Wide open.

**\
Clayton Chancey** 55:21\
OK.

**\
Val Levitan** 55:21\
And I think the best way to do it is to invoke the what is it Microsoft?\
Yeah, the the single, single ID, single signature.

**\
Clayton Chancey** 55:38\
Yeah, the SSL.

**\
Val Levitan** 55:40\
SSO, yeah. And and to have a some sort of a management.\
Application that allows access to it, but furthermore there is there is another.\
Thing in my mind is that it\'s dangerous and incorrect to use transcripts as the source of truth.\
Because it\'s not. It\'s just a it\'s just a conversation. And maybe the conversation in itself and the whole direction in itself could be grossly erroneous.

**\
Clayton Chancey** 56:13\
Uh huh.

**\
Val Levitan** 56:23\
And maybe should not be taken for the truth. So I have not decided and I have not had enough time to discuss it with smart people of what constitutes the truth and what is the process of mining for the truth.

**\
Clayton Chancey** 56:23\
Yeah.\
OK.

**\
Val Levitan** 56:41\
Versus just a stockpile of conversations.\
But one thing I know for sure right now, 100%, I do not want conversations as a form of truth. That is for sure, because many conversations and even.

**\
Clayton Chancey** 56:48\
Yeah.

**\
Val Levitan** 57:03\
Even it could be the entire direction that it\'s taken for a long, long time that is erroneous, that we don\'t want. So the process of truth is a little bit of a of an enigment to me right now.\
Or or I should say, I should say truth mining. What is the what is the process of mining truth?

**\
Clayton Chancey** 57:20\
Yeah.

**\
Val Levitan** 57:29\
It\'s it is.\
It\'s it\'s definitely not parallel to recording conversations. So that that thing I know for sure, but I think I\'ve answered your question previously and furthermore I just want to amplify that.

**\
Clayton Chancey** 57:43\
Yes.

**\
Val Levitan** 57:53\
Even the repositories of the of the conversations themselves, which in the way should be restricted I think, or should be available to a certain group only.

**\
Clayton Chancey** 58:00\
Mm-hmm.\
Yeah.

**\
Val Levitan** 58:08\
Should not find its way to the truth, and the truth should be a different set of data.\
So far, so far, the only source of truth that I\'m kind of leaning towards is mining for ADRS.

**\
Clayton Chancey** 58:17\
Agreed.

**\
Val Levitan** 58:28\
And instead of mining for truth, maybe to mine for ADRS and after every conversation. And that\'s what I\'m doing with my own transcripts. I\'m mining for two things, requirements and ADRS, and those are the only things that I try to.\
Extract from a conversation. Nothing else. Nothing else.

**\
Clayton Chancey** 58:53\
Yeah, and I also don\'t know.

**\
Val Levitan** 58:55\
Because ADR is eventually evolve into specification, timing diagrams, architectural decisions, tech stock election.\
And so forth, but.\
There\'s no other truth from a conversation except a factual ADR or a factual or RAQ or a factual capability. There\'s nothing else. Everything else is blah, blah, blah, blah.

**\
Clayton Chancey** 59:28\
Yeah.\
Yeah. I also don\'t fully know how to mind for truth. I think that the process of doing that can potentially be very different for each organization with some principles that probably.\
Transcend but.\
My theory, I\'m interested if you agree or disagree, is that this repository of chatter back and forth communications, in this case meeting transcripts, is a.\
Necessary foundation in order to it\'s the it\'s the raw materials from which you mine that truth.

**\
Val Levitan** 1:00:20\
One off.

**\
Clayton Chancey** 1:00:22\
One up, yes, yeah.\
So there is a process where something like what Lena is doing now eventually become the refined with tools and principles and processes that we do not currently have or know what they would be at JVL.\
Where rather than going directly from a transcript to create a game, there is now some.\
Other pipeline or process that derives the ground truth based on principles and some of the raw data includes meeting transcripts. But if someone said something in this meeting which contradicts.\
The ground truth and by some principle we know that it is wrong. Then this tool does not create or act upon the wrong information. It self corrects based on some ontological truth and I I don\'t think we have that layer.\
Yet, but we can. We now have a framework to insert it when we decide.

**\
Val Levitan** 1:01:26\
That\'s.\
But that\'s not how I look at what you\'re doing with Lena. And so the the process of game creation consists of three major loops. You are working on on loop #3, which is game production.

**\
Clayton Chancey** 1:01:41\
Mm-hmm. Yeah.\
Mhm.

**\
Val Levitan** 1:01:48\
And to me, game production is an assembly.\
An assembly is a highly efficient thing. This is where we want to move to a full automation.

**\
Clayton Chancey** 1:01:58\
Thank you.

**\
Val Levitan** 1:02:02\
Because it\'s simply an assembly, nothing more. There should be very little creativity within the game production. It\'s just an assembly line and we want to make it as efficient as possible. And so all these conversations.

**\
Clayton Chancey** 1:02:06\
Oh.\
Hello.

**\
Val Levitan** 1:02:20\
Need to be automated and we need to extract tasks, put them into JIRA and execute in the most automated form. And that\'s what you\'re doing now, the game design.\
And idea generations are done in the two levels higher. We have not touched those.

**\
Clayton Chancey** 1:02:45\
Yes.\
Yes.\
But.\
I still think that even in.\
Even most especially in production.\
A ontological sense of what like you mentioned, for example tools, the tools that we should use.\
The images that we should use.\
Lena\'s Claud interface right here is actually providing that intermediate layer right now. Right now, what is happening philosophically is that Lena is using Claud to pull a meeting transcript which we have refined using automation.\
Techniques to be a better meeting transcript and to pull JIRA information and we have refined for an MCP server to be a more rich, accurate JIRA layer. And then she is serving. The user of this Claude instance is actually serving as the ontological filter, so there\'s a person making decisions.\
About what is correct and incorrect and then they are hitting the execute button and things are going. So there is still that layer where we actually cannot fully automate that because if you give it to quad in auto mode.\
We don\'t know. It\'s it\'s pulling from sources of truth which are not actually truth necessarily.

**\
Lena Zhukova** 1:04:15\
Oh yeah, and I I I\'m sure it will do like some hallucinations on the way, so it it should be checked.

**\
Val Levitan** 1:04:22\
I actually, I actually feel that hallucinations will absolutely disappear. It\'s just a matter of time right now.

**\
Clayton Chancey** 1:04:30\
Yes, yeah, yeah, but but.

**\
Val Levitan** 1:04:31\
But so the the hallucination hallucination will never be an issue. I mean, maybe right now, but for a limited time. But let\'s say in a year it will totally disappear. My, my, my.

**\
Clayton Chancey** 1:04:43\
Well, hold on this. This is where Aaron and I strongly disagree on this topic of hallucination. A hallucination is not a problem with the model hallucinations. If you\'re looking at the large language model today, hallucinations don\'t exist.

**\
Val Levitan** 1:04:56\
Yes. No, no, hold on. No, hold on. I I understand where you\'re going with this. I I understand. And because there is no actual physical matter, it it\'s only it it\'s looking for the roots of the sentences. I I understand. I understand the large model.\
Argument.\
I\'m not actually referring to it. I\'m saying that in our case, in what Lena is doing, hallucination will not be an issue.

**\
Clayton Chancey** 1:05:29\
I think, I think what I\'m actually saying is that to a large language model, there\'s no such thing as a hallucination. A hallucination is a user category only. It\'s not even a prompt. It is only in my mind. A hallucination only exists.

**\
Val Levitan** 1:05:39\
Imprompt.\
Impro.

**\
Clayton Chancey** 1:05:48\
Because I have more context than we have given the model and and my context causes me to say, hey, that\'s not correct. But to a large language model, it is only working with what it has and that determines what it does. There is no category of truth or untruth because.

**\
Val Levitan** 1:05:51\
Oh, good point. OK.

**\
Clayton Chancey** 1:06:07\
Large language model is not being, it\'s not conscious, it doesn\'t have.

**\
Lena Zhukova** 1:06:07\
But what I what what I notice, what I notice is sometimes it is trying to fix my like my information and that is saying that it\'s even better, but it\'s not better.

**\
Clayton Chancey** 1:06:19\
Mm-hmm.

**\
Lena Zhukova** 1:06:24\
It\'s his interpretation that is better.

**\
Clayton Chancey** 1:06:24\
Right, right, right. Exactly. And you exactly. So you are the one who knows that this is a hallucination because you have more context. You know your your lived experience in the world and in your life and in JVL and.\
In this project includes more data than the large language model or quad can possibly have, even through its tools. And your context is not engineered, it\'s just experienced. And so a hallucination is not a technological.

**\
Lena Zhukova** 1:06:56\
Mhm.

**\
Clayton Chancey** 1:07:01\
Category. It\'s not something that you can reduce by making the tools more accurate. It is something that exists because you live in reality and the large language model is not a being that lives in reality or experiences. It is a machine.

**\
Lena Zhukova** 1:07:15\
1.

**\
Clayton Chancey** 1:07:16\
That just operates on what it has. And so a hallucination is not a category that exists in a large language model. It is a category that humans use to describe whether the large language model does what they want it to do or not.

**\
Lena Zhukova** 1:07:32\
Um.

**\
Clayton Chancey** 1:07:33\
And the problem with this is that the people building large language models are like 25 year old computer science people who didn\'t finish their philosophy electives and then left and they don\'t. They\'re using terms that anthropomorphize their own technology. So it\'s the long.\
Long way of saying in order to reduce what we are calling hallucinations in the AI industry.\
You have to encode the most important pieces of context from a human experience into a tool somewhere, and this this process of engineering is what reduces what we call hallucinations, not the models getting better.\
The way that we reduce hallucinations is very context specific, and the only way you can reduce them is to actually engineer the situation in which the model can discover what we think is true.

**\
Lena Zhukova** 1:08:17\
And.

**\
Clayton Chancey** 1:08:32\
For any one situation. So this is actually aligned with what you\'re saying, Val. It\'s not a model problem. You can have large language models with absolutely 0 hallucinations today, and this has been true for almost a year. It\'s just an engineering problem, not a model problem. We have to stand up the pipeline, the tools where.\
It\'s getting the information and we have to decide how we determine the truth for anyone task and then build it so that the model has access to that and then there will be no hallucinations. And that is that is what I\'m talking about is like we have the transcripts.\
We have the Jira, we have Lena, and right now Lena has to steer and ultimately make some judgment calls and decisions in this tool in order to prevent hallucinations. So we need to take that knowledge, which Lena is doing.

**\
Lena Zhukova** 1:09:15\
I mean.

**\
Clayton Chancey** 1:09:23\
And actually arrive at some principles and decide as an organization, how do we come to those decisions? How do we decide what is truth and what is not for this specific task? And we have to engineer a process by which Claude can make those same decisions reliably.\
And that\'s that\'s actually very complex, but that will reduce the hallucinations for this task. It\'s simple. And then Claude\'s ability to do that efficiently and fast will improve over time as large language models improve. But large language models don\'t hallucinate.\
They just do what they they just do what they\'re doing. And we as humans judge what they do as either hallucination or not. And that\'s a very important principle because otherwise we\'re now trusting large language models to do something that they can\'t do because we are actually just having more context.

**\
Val Levitan** 1:10:17\
But let\'s let\'s have a resolution on the questions that you asked. I believe that it should be restricted and it should be we should decide who has access to it.\
That\'s number one. So SSO, I think like wedging and SSO here I think is important and we\'re already subscribing to it, so why not to use it and and and it\'s a.

**\
Clayton Chancey** 1:10:32\
Mhm.\
We already have SSO for GitHub for this, so this is already governed by Lena\'s SSO, so that that piece is already exists.

**\
Val Levitan** 1:10:48\
OK, so perfect. Second of all, the resolution should be that recordings is not a source of truth.\
I think right now, for me personally, the only source of truth is are the ADRS.

**\
Clayton Chancey** 1:11:09\
Mhm.

**\
Val Levitan** 1:11:10\
And the specific resolutions that are taken during the meeting? No, no, sorry, ADRS and requirements, I should say. There\'s no other source of truth for me. Everything else is just a speculative conversation.\
But but let\'s focus on the goal. The goal is step by step, embracing various technologies and logic. Most important is to come up with the most amount of efficiencies that we can provide to the team.\
So they spend the least amount of time on what Aaron Nye calls useful bureaucracy.\
And you know, let\'s let\'s stick with the agenda and it will evolve over, you know, next weeks, months. But we know what needs to be done. Let\'s get rid of the useful bureaucracy. So making the team more efficient.\
And every time we\'ll go in loops and review what we have and what else we can offer.

**\
Clayton Chancey** 1:12:19\
Agreed. The other resolution we need to add to the end of this meeting as well is that I need to just. I just want to highlight this for my transcript is that I need to incorporate.\
The chat and interleave this with the transcript per Lena\'s request so that the processing that we\'re doing when we\'re deriving ADRS and and our source of truth, we are at least incorporating the full.\
Range of data from the users so.

**\
Lena Zhukova** 1:12:57\
It\'s very important because very often we send in chat link to requirements as a like reference. So use this requirements to create this task. So if it can go is a CMCP can go to Jira, read this requirements and incorporated for example into description.

**\
Clayton Chancey** 1:12:59\
OK.\
Yeah, yeah.

**\
Lena Zhukova** 1:13:17\
That would be perfect because sometimes we have taken some parts of description from requirements, which is so natural.

**\
Clayton Chancey** 1:13:25\
Yeah, yeah, this should be a.\
A brief fix. There is a dependency on Andrei, but he\'s been very responsive. So my intention is that I\'ll make this change, I\'ll give Andrei the requirements to make his change in the Power Automate script, and then if that is done before our next meeting on Thursday, then we can have that and we should be.\
Sort of like closer and then Lena when your Mac gets here also you know I can Aaron can do this as well, but we can I can help you set up this in the Mac and then the images piece will be solved.\
Completely by that. So these are our next steps. I\'m already taking you guys 15 minutes over our our scheduled meeting and I also need to go. So I think we\'re good. And Val, I know I will post the transcript here in the in the teams chat as soon as it finishes processing.

**\
Val Levitan** 1:14:25\
Thank you very much. Have a great day. Bye.

**\
Clayton Chancey** 1:14:27\
Wonderful.

**\
Val Levitan** 1:14:30\
OK.

**\
Clayton Chancey** stopped transcription
