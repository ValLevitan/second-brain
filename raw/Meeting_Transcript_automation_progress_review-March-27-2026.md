**Clayton-Aaron-JVL-20260327_140036UTC-Meeting Recording**

March 27, 2026, 2:00PM

19m 12s

**\
Clayton Chancey** 0:18\
Hey, Lena, how are you?

**\
Lena Zhukova** 0:19\
Yeah, I\'m good. Clayton, how are you?

**\
Clayton Chancey** 0:22\
I\'m good. I\'m, uh, I\'m carrying my laptop upstairs back to my office real quick, so I\'ll get my camera. Yeah, um.

**\
Lena Zhukova** 0:28\
Mhm.

**\
Clayton Chancey** 0:34\
This might be a short meeting. I mean, I do have a lot of really cool progress I can share with you all, but but Claude code is having a huge outage right now. Are really.

**\
Lena Zhukova** 0:39\
OK.\
Mm nice.

**\
Clayton Chancey** 0:50\
Really anthropic plug as an organization is having a huge outage. So I just, I just left a a big incident management call where I was sort of.\
Trying to help people troubleshoot some things. I may need to go back there in a few moments and slash. I don\'t know that we can really do much work here besides just I can tell you.

**\
Lena Zhukova** 1:16\
Interesting. Like from your experience, do you find that the anthropic has more often some problems that ChatGPT? No.\
Because I I know like chat chat when we used to chat actually we also had like some issues.

**\
Clayton Chancey** 1:35\
Um.\
Yeah, yeah. I mean they\'re, they\'re, they\'re all of these companies are like the most infrastructure heavy consumer platforms that have ever existed. So I hear people making and it is kind of funny that these are the same people who say like, hey, voting is solved.

**\
Lena Zhukova** 1:54\
Mm.

**\
Clayton Chancey** 2:02\
There\'s no such thing as a human programmers are not needed anymore and then they\'re having outages like every week. But at the same time I get it because the problems that are happening are problems that.

**\
Lena Zhukova** 2:05\
OK.

**\
Clayton Chancey** 2:14\
Are essentially new. You know, I don\'t know that anyone has ever really had these problems before, but.\
Let me OK, we are recording so Val can get the transcript. Aaron will not join because he is also part of this incident which I just was on the call with him so I had to leave.

**\
Lena Zhukova** 2:27\
Mhm.\
Mhm.

**\
Clayton Chancey** 2:36\
But here is what I did. I took the second call and the first call together and I ran them. I created a pipeline which is really.\
Really accurate, really good and I.\
I can send you the outputs of this pipeline just for the second call, just for your for your review, but I think I got it really really well. Claude code and Claude are also reviewing and we have a like a 99% on average 99%. Sometimes it can go as low as like 92.

**\
Lena Zhukova** 3:00\
Mhm.

**\
Clayton Chancey** 3:14\
But the average throughput is a is a 90% accuracy. It uses it. So basically what I did is I took this pipeline and I made it into an API that I\'m hosting and so JVL now has this like microservice.

**\
Lena Zhukova** 3:28\
Mhm.

**\
Clayton Chancey** 3:31\
Which is hosted and anyone can make an API request to this service and I have to have an API token which I can provide and they can provide the audio file. You can\'t. You need to provide the audio file at least, but you can also provide the taxonomy.\
Information and then the Microsoft Teams transcript. The more that you have, the more accurate it is and this pipeline will use. It will basically transcribe the audio on its own.

**\
Lena Zhukova** 3:55\
Mm-hmm.

**\
Clayton Chancey** 4:06\
Which gets better. Russian, English, slang, all of that stuff. It\'s fine-tuned for that. And then it will use the Microsoft Teams transcripts to know who was in the call and when they were speaking, because Microsoft Teams actually will know that.\
Far better than our transcription tool will, and so we\'ll combine these two and then we run it again after that through Claude to streamline and understand. And Claude was given some prompting around.

**\
Lena Zhukova** 4:33\
Mhm.

**\
Clayton Chancey** 4:39\
The nature of the conversation and the JVL specifics and so it it will translate everything until like JVL speak even Russian slang.

**\
Lena Zhukova** 4:49\
May I ask what happens with chat content and the video content of the meeting? Because we are sharing screens during meeting and we also throw in some images or even like some information into chat.

**\
Clayton Chancey** 4:50\
And.\
Mhm.\
Mm-hmm. Nothing is. Nothing is happening. All of this is doing is generating a transcript only.

**\
Lena Zhukova** 5:05\
Um.\
So it\'s it\'s it\'s only about like what we are talking about. It\'s not so as a content context is not like taken into account. Yeah, so it\'s.

**\
Clayton Chancey** 5:19\
Yeah, right, right.\
Yeah, well, it may be. Usually what will happen is it will be.\
Reflected. Like if you say I\'m sharing my screen, do you see this? Oh yeah, I see this. And if I click here, oh, OK. And like these sorts of things, like Claude doesn\'t know what you\'re talking about, but it knows that you\'re sharing the screen.\
Uh, and this is true of Microsoft Teams as well. It doesn\'t also process the video, it will only process the audio and then present you with the video.

**\
Lena Zhukova** 5:47\
To.\
But interesting, I think it can easily process for example like some text or links from chat, right? Because it\'s part of discussion. So I think it would be helpful for example if you are.

**\
Clayton Chancey** 6:03\
Mhm.\
Yeah.

**\
Lena Zhukova** 6:09\
Uh, throwing some links to some uh general issue to chat or some maybe some. I don\'t know some points uh from some documents uh or something like this. It would be nice to include it in.

**\
Clayton Chancey** 6:11\
OK.\
OK.\
OK.\
Yeah, yeah that I can that I can do. What I would need then is if we could go back into game one and or the the game dev maze, the first call that you sent me and then the game dev maze 2.\
That you sent me.\
If we could get the chat content, which is I think you can just download it, then we can try this as well. And this would now be like there\'s the just so I understand. I think the way I would do this is I would do everything the same as I\'m doing now, but before it goes to Claude at the end.

**\
Lena Zhukova** 6:49\
OK. Yeah.

**\
Clayton Chancey** 7:02\
I would say also here\'s chat content and I want you to take the the timestamps of the transcript and the timestamp of the chat and interleave them so that in the final document, yeah.

**\
Lena Zhukova** 7:08\
Mhm.\
Yeah, they they need to be synchronized because they need to be synchronized. It\'s important. Yeah, I will send it. It\'s especially important for second meeting. In first meeting we share less information in chat because I almost all the time shared screens. But in second meeting, yes, we have chat which I can download and send to you and I.

**\
Clayton Chancey** 7:18\
Yeah.\
OK.\
Mhm.

**\
Lena Zhukova** 7:33\
Less about shared screen because when I share with somebody sharing screen we explain a lot about it. So we discuss and so it\'s more or less from our discussion it\'s pretty like clear information what what what we need to do, for example what issue we need to create. But sometimes important information is.

**\
Clayton Chancey** 7:38\
Yeah.\
Mm-hmm.\
Yeah.

**\
Lena Zhukova** 7:53\
In in the chat like it can be like some bullet points from some dog for example again all some links to other issues which can be like for a for example for requirements we can send links and say OK you need to follow this rack when you you do this story so.

**\
Clayton Chancey** 7:59\
Yeah.\
Yeah.

**\
Lena Zhukova** 8:10\
It it, it might be pretty important.

**\
Clayton Chancey** 8:13\
Well, there are there are ways by the way to process that the whole video and to like I use Gemini for this regularly where I actually like if I am sharing a video where I\'m.\
Like clicking through screens and like demonstrating a product or something. I will upload the video to Gemini, the whole video file, you know, 300 megabytes or whatever and then and then tell Gemini I want you to. You don\'t need to transcribe, but I want you to just.

**\
Lena Zhukova** 8:38\
OK.

**\
Clayton Chancey** 8:48\
Describe every single click and point and like it will come out and say like then the user clicked this button and then they moved their mouse and clicked this button and they typed this and it will do that well. So maybe it\'s a bit of a stretch goal for.\
I think it would be useful to experiment with that.

**\
Lena Zhukova** 9:08\
But it\'s a it\'s a more for future maybe because I again I worry less about it but chat that\'s I think more like an actual problem. I will send you the chat upload from last meeting here.

**\
Clayton Chancey** 9:09\
Cause if you could get that.\
Yeah. Hey, Val.\
OK.\
I\'ll catch you up. Good morning.

**\
Val Levitan** 9:24\
Good morning. Good morning, everyone. I\'m sorry I was finishing my previous meeting and I had a running.

**\
Lena Zhukova** 9:26\
But.

**\
Clayton Chancey** 9:29\
Yeah, no, you\'re good. I I was telling Lena that, you know, Anthropic is having a very large outage right now and I was just leading a troubleshooting call, like an incident call, which I probably need to head back to once I\'m done here.\
And cloud code is for for many people is completely down right now. But I was just explaining to her what I did and then what I what I will do when the outage is over.\
Outage is over. I took our pipeline, which we devised to translate these meetings.\
And I I got it working really, really well. It\'s very reliable and I made it an API, a microservice. So it\'s hosted and there is a an API endpoint where you can simply you have to have a token which I can provide.\
And then you can submit the meeting information, including the audio, the transcript from Microsoft Teams, the taxonomy, and then you can pull it and it takes one or two minutes and then it responds with this beautiful, perfect transcript.\
So what I would like to do is I will my next step would be to work directly with Andrei and I think it would be really the best way to do this would be a Microsoft Power Automate script since you\'re already in the Microsoft platform.\
The Power Automate script will listen for the end of any Microsoft Teams meeting and when a Microsoft Teams meeting concludes, it will run this API call. It\'s very quickly and then at the end.\
It will post the finished transcript to a GitHub repository and then now you have this flow or anytime you have a Microsoft Teams meeting automatically. If the meeting was recorded then some.\
Two to five minutes later, this perfect welltranslated transcription will appear in GitHub.\
And I will need to work directly with Andre, but I told I but I can do that. I can do that easily with him.\
I I was telling this to Lena and she made a good suggestion. This would be one thing which we could add before I go to Andre.\
Is, she said. What about the chat content? When they\'re having a meeting and then someone opens in the meeting, someone opens a chat like like what I\'m doing now and they send a chat that is now time stamped.

**\
Val Levitan** 12:17\
Yeah.

**\
Clayton Chancey** 12:20\
Within the call. So I\'m going to, I\'m going to work to interleave those. That will be good. And then when I finish this, it\'s just a few moments then I\'ll work directly with Andre and we will build this. This is now a microservice, a JVL microservice which you should not need to to do anything.\
Should be kind of this seamless experience. Oh, so the only other thing that I\'m saying all this because I looked through the JVL GitHub to see where this.\
Techlex repo was what you what you emailed about. I couldn\'t find it so I wanted to see was this actually built and in progress yet or do I need permissions because that would be probably.\
A good place to put these transcripts.

**\
Val Levitan** 13:12\
This is fantastic. This is something that you should pick up with Andrei.

**\
Clayton Chancey** 13:17\
OK, I can. I can just pick up and work with him. All right, well then my my running.

**\
Val Levitan** 13:22\
Can we please set up? Can we please set up a meeting between you and Andrei?

**\
Clayton Chancey** 13:27\
Yes, Yep, that I have a message ready to send to him now. Um, so once.

**\
Val Levitan** 13:32\
Please, please invite me to the meeting.

**\
Clayton Chancey** 13:36\
OK, I will do.\
All right. Well, then we\'re good.

**\
Val Levitan** 13:39\
Can you send me? Can you send me this transcript now?

**\
Clayton Chancey** 13:43\
Yeah, I absolutely will do so right now.

**\
Val Levitan** 13:44\
Like now, like now, please.

**\
Clayton Chancey** 13:46\
Yeah, absolutely.

**\
Val Levitan** 13:47\
Thank you very much. What\'s when? When is the next meeting with Lena?

**\
Clayton Chancey** 13:49\
All right.\
It will be next Tuesday.\
Next Tuesday morning at this time.\
And I am back on the West Coast, so I\'m back in my regular schedule. I we I will. I\'ll be a free and available to meet then and I should I would. I will try to meet with Andre either today and if it\'s too late for him or too late for me, then I will. I will meet with him on Monday and it\'s.

**\
Lena Zhukova** 14:10\
Mhm.

**\
Clayton Chancey** 14:21\
Microsoft Power Automate is very simple. I think it should be hopefully working.

**\
Val Levitan** 14:25\
Schedule. Schedule for Monday, please.

**\
Clayton Chancey** 14:29\
OK, I will do.

**\
Lena Zhukova** 14:30\
And I also would like to make a comment about your MCP. I really like how your MCP working for me like but I\'m working in sandbox. I don\'t want to populate it for other like artists or I don\'t know maybe we want to give it to all developers but I would like to fix the sync with folder so so.

**\
Clayton Chancey** 14:46\
Mhm.

**\
Lena Zhukova** 14:50\
I would like to use a specific folder. I don\'t want to down the recent to desktop. So once once we fix it I I would like to make it like working for the Algira and I would like to give it to to.

**\
Clayton Chancey** 14:51\
Yeah.\
Yes.\
Yeah, I.\
Yeah.

**\
Lena Zhukova** 15:07\
I I would like to give it all from our department, but maybe we want to also give it to to all to them. I I really like how it works now in sandbox.

**\
Clayton Chancey** 15:14\
Yeah.\
That\'s good. I spoke with anthropic with so I I created AI spoke to someone who created an internal record or feature request or I don\'t know what you call it on this issue for.

**\
Lena Zhukova** 15:18\
OK.

**\
Clayton Chancey** 15:32\
Mounted drives for a Windows client and I hope that we can we can resolve it.\
I think if by the time that this microservice for transcription is not working, if by the time that it is working, if now this issue with the mounted drive is the blocker to our end-to-end process which we set out to accomplish, then we can develop a workaround.\
And there are ways that you can do that just for Windows, which sort of trick the Windows file system into thinking that it\'s not a mounted drive, but it is a solution that we implement on your machine. And so I would need to probably cooperate and work with JVL IT to sort of.

**\
Lena Zhukova** 16:00\
Mhm.

**\
Clayton Chancey** 16:18\
Make sure that this happens for anyone else with a windows.

**\
Lena Zhukova** 16:18\
And then they will need to do it for all developers who are going to use this.

**\
Clayton Chancey** 16:22\
Yeah, yeah, the best. The best solution by far is that anthropic can change and update their product and then it would be a bit of a painful process to do that for every Windows machine, but it would it would resolve the problem. And so I am hoping let\'s wait until.\
Our whole pipeline is done and then if people with Windows machines can\'t use it without this pain, then we can solve this problem. But I\'m hoping that they can fix that while they\'re in the middle of figuring out their outage they\'re having today, so we\'ll we\'ll see.

**\
Lena Zhukova** 16:42\
Mhm.\
Interested in would it work with some folder in GitHub if we will send it to some like for for our like for our future like pipeline?

**\
Clayton Chancey** 17:11\
Well.\
It could. However, GitHub robably is not the place to store images depending on their size, but GitHub is.

**\
Lena Zhukova** 17:22\
But we are storing. We are using a large files system and we are storing like MFS here.

**\
Val Levitan** 17:27\
LFS. We\'re using. We\'re using LFS.

**\
Clayton Chancey** 17:32\
Oh well, that was that was the solution that I was gonna use as well for the Windows workaround.

**\
Lena Zhukova** 17:33\
Yes, totally.

**\
Clayton Chancey** 17:41\
Let me think about it. We would need to rework something. So ultimately, ultimately if we stored those files in GitHub.\
My MCP server would still need to bring those files down into the temporary directory where Claude Cowork is working, but it can delete them after it\'s done and so it would be like this pass through and that is exactly the same thing that I would be doing in a Windows machine to solve the problem.

**\
Lena Zhukova** 17:57\
No.\
It can work actually with downloaded folder now in downloaded branch on my machine because I again like when I work with my branch I download it to my to my machine work and then I upload back to GitHub. So if it again if it will work with some specific Windows folder it will resolve the problem.

**\
Clayton Chancey** 18:19\
Yeah.\
OK.\
Yeah, let\'s see if we can get the client problem solved. The the Windows client for Cloud solved. If we can, great. And I mean we have till Tuesday. I mean we the rest of the the work will be done on Tuesday. So if it\'s.

**\
Lena Zhukova** 18:41\
OK.

**\
Clayton Chancey** 18:51\
If it\'s solved by then, then we\'re really good. If it\'s not solved by then, then we have a workaround we can implement.\
So that\'s my that\'s my thought anyway.

**\
Val Levitan** 19:01\
Thank you. Can you please place the transcript here?\
Thank you very much. Bye.

**\
Clayton Chancey** stopped transcription
