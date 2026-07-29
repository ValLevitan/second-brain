**Clayton-Aaron-JVL-20260319_140335UTC-Meeting Recording**

March 19, 2026, 2:03PM

1h 3m 9s

**\
Clayton Chancey** 0:48\
Hey, Lena.

**\
Lena Zhukova** 0:49\
Great done.

**\
Clayton Chancey** 0:54\
OK.\
Get my project pulled up. Um.\
OK, what I did.

**\
Lena Zhukova** 1:04\
OK.

**\
Clayton Chancey** 1:09\
I wanna uh.\
Wanna try something since I might ask you to find a like another meeting or another transcript for me for a meeting.\
And then we can we can test it because I I think I found a way to get a really good transcript, but.

**\
Lena Zhukova** 1:30\
The problem is we we didn\'t have such reach meeting because it\'s for now it\'s a game which we are going to start to develop with a lot of like features we need to open new like other features and stories now in maintenance mode so they already.

**\
Clayton Chancey** 1:31\
Alex.\
Mhm.

**\
Lena Zhukova** 1:50\
Open and created and described. We are just like doing production and we are closing something, reviewing something like pretty soon we are going to have like another new like big project to start and then we are going to have like rich meeting like this. But for now like all other meetings they are not.

**\
Clayton Chancey** 2:04\
Yeah.\
OK.

**\
Lena Zhukova** 2:10\
Good materializing for creation and new features.

**\
Clayton Chancey** 2:12\
Mm OK.\
Well, I think So what I did is I created this, you know, this pipeline with Whisper, which does transcribe OK the the issue, excuse me, the issue. Oh, and with Whisper.

**\
Lena Zhukova** 2:18\
I will.\
Mhm.

**\
Clayton Chancey** 2:33\
You can add the glossary. So I have the glossary and then yeah, and so that helps. And then I I saw the emails back and forth about getting the glossary in GitHub, so that\'s perfect. I can just bring that and use the GitHub glossary.

**\
Lena Zhukova** 2:37\
Mm-hmm. Which is quite important here. Mm-hmm.\
She.

**\
Clayton Chancey** 2:53\
O3 whatever.\
But if I am just transcribing the call, I do not have very accurate diarization to to know who is who.

**\
Lena Zhukova** 3:08\
Mhm.

**\
Clayton Chancey** 3:09\
Right, because I\'m just getting the audio. It\'s like one file, one like mono audio file, and then I\'m transcribing that whole thing and I so I don\'t really know who is who unless there are some contextual clues.\
So I built a pipeline to say, OK, we\'re going to do three things. We\'re going to take the audio and transcribe it. We\'re going to take the original Microsoft Teams transcript, which is which is bad and incorrect.\
As far as the actual content, but it will always be correct as far as who said what. I\'m going to take that and then we\'ll take our new sort of Russian expert transcript. We\'ll take the bad Microsoft Teams transcript that knows who everybody is, and then we\'ll run.

**\
Lena Zhukova** 3:46\
Mm-hmm. That\'s true.

**\
Clayton Chancey** 4:01\
Those through Claude and it will and it there we have lots of good prompting. We can really explain the use case and then on the other end.\
It will produce a transcript which is like the best of all worlds. But I let me see, let me show you, share my screen and.\
And they have one big laptop screen today, but.\
Um for this particular call like the uh.\
The call with the game dev whisper. Um.

**\
Lena Zhukova** 4:38\
Mhm, mhm.

**\
Clayton Chancey** 4:43\
Or this one, the MP3 here. I only have the audio so this is what I was hoping I could get from you and we can test is if I could get the Microsoft Teams transcript which was generated for this one.

**\
Lena Zhukova** 4:46\
Mhm.\
Uh, OK, I can send it to you like this bad transcript. Yeah, OK.

**\
Clayton Chancey** 5:01\
Yeah, like it\'s a bad. We know it\'s kind of a bad one, but if you can send it to me then I can run it to the pipeline and I think we can see if it\'s better.

**\
Lena Zhukova** 5:05\
Sure, sure. I I I can do it too. Just a moment.

**\
Clayton Chancey** 5:10\
OK, cool.

**\
Lena Zhukova** 5:15\
It was in this.\
I\'ll have to meet you.\
Yeah, OK.

**\
Clayton Chancey** 5:49\
Cool. Let me download that. Uh, let me share my screen just so you can see.\
Everything that I\'m doing.\
Uh.\
Um, what did I call this JVL whisperer?\
OK, so then I can go back here and say um.\
I have removed the original game dev audio.\
Plus the new Ms. teams transcript that Lena provided for that same meeting into a original\'s.\
Directory.

**\
Lena Zhukova** 6:58\
When the our vocabulary, I like just glossary is already there, right? So it\'s uh or it\'s mhm, mhm, mhm, OK.

**\
Clayton Chancey** 7:04\
Yeah, we have the, yeah, good, good question actually. Hold on, where is the glossary? Well, that\'s.\
Oh, taxonomy. It\'s in the taxonomy.\
I\'m actually gonna go ahead and move that as well.\
I also moved the taxonomy Excel into that as well for simplicity.\
So that we can run the pipeline.\
On the required artifact and understand what those artifacts are each time. Can you test the approach on these?\
There we are under.\
Uh.\
I spare on the audio.\
Quad on the newly generated transcript plus.\
BTT or plus Ms. transcript plus taxonomy to understand.\
And.\
I created I so the the whisper pipeline apparent. So I did not know this, but there\'s actually a limit to how many like words that you can give it and say actually this is the text on. It\'s like only like 200 words or something like that, so.

**\
Lena Zhukova** 9:01\
OK.\
OK.

**\
Clayton Chancey** 9:13\
What we what I did is I created a a like a preprocessor that basically recognizes which words are it from the taxonomy are part of this call and then it and it only focuses on that and then it runs the whisper transcription.

**\
Lena Zhukova** 9:22\
No.\
Mhm.

**\
Clayton Chancey** 9:32\
By adding only those words from that taxonomy in. And so that seems to help because that way you can have many, many words in your in your glossary or your taxonomy and it\'s still.

**\
Lena Zhukova** 9:44\
Mhm, mhm.

**\
Clayton Chancey** 9:48\
Very reliably going to gonna pick those up and it\'s the it\'s the funniest thing. It\'s like you don\'t even have to.

**\
Lena Zhukova** 10:06\
Yes.

**\
Clayton Chancey** 10:06\
You do that whisper can like hear and detect and understand that word a lot better. And then because we are not relying on whisper to actually understand what that word means in the context.

**\
Lena Zhukova** 10:16\
Hello.

**\
Clayton Chancey** 10:23\
Of what we\'re talking about, which is game design and everything, we can rely on cloud code to translate that correctly later. And so that seems to be the correct pipeline for translating like slang or you know, abbreviations or things like that, so.

**\
Lena Zhukova** 10:28\
Uh.

**\
Clayton Chancey** 10:39\
Like when people talk about resi as resolution and it\'s you know things like this. So I think I think this should work well. We will see this is a Claude. Cloud code is running the.\
The scrits that that do this pipeline so so we\'re seeing kind of the outputs of the Python scripts.\
And we\'ll see how it goes.\
Then if we if we get once we get this working and we I can confirm with you on the call that it\'s it\'s good, it\'s worth it high quality then.\
I have an e-mail I will send to Andrei because I\'ll I\'ll request Microsoft Graph API permissions for just this specific.\
App and so then I will. I\'ll send that permission to him. If he grants it, then this can then become the the automated pipeline for generating Microsoft Teams.

**\
Lena Zhukova** 11:49\
Mhm.

**\
Clayton Chancey** 12:03\
Dial.

**\
Lena Zhukova** 12:04\
So you mean we we don\'t need to do all this like steps. It will be integrated in teams and it it will do it automatically for each transcript. That\'s would be amazing. That would be amazing.

**\
Clayton Chancey** 12:10\
Yeah.\
Yes, yes.\
Yeah.\
That\'s the idea, but it we need to just like hopefully just once without too much back and forth is what I\'m trying to avoid. Hopefully we just once we get the right permissions and access and then we have access to do that from Microsoft Teams, but it can sometimes be like a lot.

**\
Lena Zhukova** 12:20\
And.\
So.

**\
Clayton Chancey** 12:38\
Of trial and error because the Microsoft API is complicated.

**\
Lena Zhukova** 12:42\
I think to to test this capability, I think I will record tomorrow like our daily meetings, like graphical daily meetings because we we are actually we are going to test the capability of this tool, not like ZRMCP because ZRMCP.

**\
Clayton Chancey** 12:53\
Oh, cool.

**\
Lena Zhukova** 13:02\
For now, I think it\'s working pretty good, so I will record it. So we will have like 2 like two sources with a lot of like Russian words and slang and.

**\
Clayton Chancey** 13:06\
Yeah.\
02 sources to take, yeah.\
Mm-hmm.

**\
Lena Zhukova** 13:18\
The English words like mixed with Russian, so it will. Yeah, I will do it tomorrow, yeah.

**\
Clayton Chancey** 13:23\
OK, cool. That\'d be great. And then if you send it to me after the meeting, feel free to just send it on Teams and you can send the audio and the transcript and then I will run it again and and then send you back the.

**\
Lena Zhukova** 13:28\
Mhm.\
OK.\
Mm-hmm. I will. Yeah. OK. I will validate it here. OK.

**\
Clayton Chancey** 13:39\
You know the response for. Yeah, OK, it\'s.

**\
Val Levitan** 13:43\
So sorry. Hi, guys.

**\
Clayton Chancey** 13:46\
Hey, how\'s it going?

**\
Lena Zhukova** 13:46\
Hello.

**\
Val Levitan** 13:47\
Um, pretty good. Sorry for interruption. Um.

**\
Clayton Chancey** 13:53\
No worries.

**\
Val Levitan** 13:54\
We we would like to set up this.\
Um.\
I don\'t know how to call this document semantic understanding.\
Or.\
Back legs, I don\'t know.

**\
Clayton Chancey** 14:13\
Mhm, mhm.

**\
Val Levitan** 14:15\
We\'d like to set it U as a service.

**\
Clayton Chancey** 14:18\
Yep.

**\
Val Levitan** 14:19\
So it it could be accessible by anything else.

**\
Clayton Chancey** 14:24\
Yes.

**\
Val Levitan** 14:25\
Hold on, I I need to attend to this. Please continue.

**\
Clayton Chancey** 14:30\
OK, no worries.\
Yeah, you know.\
Even just using that phrase as a service makes me think, oh man, uh.\
Maybe what we do, this is actually probably what I will do cuz this now removes the dependency of it and Microsoft Graph and all those things. I think. I think maybe what we well, not necessarily totally, but it would be cool to.\
Make this this pipeline a.\
And it like to give it an API. This is something that can be called. So it becomes sort of a microservice where if you have an audio file and then optionally if you also have a like a transcript which is probably bad quality and you wish to improve.\
Then you can submit an API request with those two.\
Parameters and then on the other side now comes out the improved transcript and then maybe you can even send a prompt. And then the nice thing about that would be that our API, our tool, our service just goes to GitHub and consumes the.\
Language mapping or taxonomy that they\'re setting up in GitHub brings that down and reads and interprets it. So this just becomes like another microservice to which you can submit parameters and then it can be an MCP server. If it\'s an API, it can be wired into an automation PowerShell script.

**\
Lena Zhukova** 15:59\
Right.

**\
Clayton Chancey** 16:15\
One in IT who wants to use it can just kind of consume it naturally. That would be a really elegant pattern.

**\
Val Levitan** 16:22\
So, so Andrei has started on this setup right now. I just wanna let you know that whatever you\'re doing with that document run it by Andrei.

**\
Clayton Chancey** 16:26\
Yeah.\
Mhm.\
OK.

**\
Val Levitan** 16:34\
Uh, he has to be incorporated in the solution.

**\
Clayton Chancey** 16:38\
Yeah, I saw some of the emails back and forth and it sounds great to me. I didn\'t want to get in the way. And then I saw that like this morning Andrei was sort of asking for my feedback. But I\'ll I\'ll just, I mean what whatever you guys generate, it sounds like the solution to GitHub that then.\
Sort of naming convention behind that. It\'s perfect because then I do not have to store now the taxonomy as like a spreadsheet. I\'ll just pull it down, whatever\'s in GitHub, I\'ll just pull it down and that becomes part of the process.

**\
Val Levitan** 17:00\
Yeah.\
Exactly so. So let\'s consider it to be a microservice residing on GitHub.

**\
Clayton Chancey** 17:15\
Yeah, yeah, exactly. Yeah.

**\
Val Levitan** 17:19\
OK. Uh, sorry I missed the first part of the meeting. Can uh, can you?

**\
Clayton Chancey** 17:19\
OK.

**\
Val Levitan** 17:25\
Brief me in into Lena\'s current experience.

**\
Clayton Chancey** 17:27\
Mhm.\
Yeah, so we\'ve basically said the MCP server piece is good, it\'s working good. It\'s improved even because I rolled out some changes and gave them to her. It\'s great. The transcription piece, which we\'re doing now, I found a way.\
To do the transcript that it it\'s. I think it\'s very high quality, but it requires not only the audio but also the the incorrect or.\
Unacceptable Microsoft Teams transcript. It requires those two inputs, so I had to get that from Lena, which I just got now. The reason for that is if I run the audio file here, you know the transcript.\
Transcription of a game dev discussion through Whisper. I got it to the place where Whisper transcribes the Russian and the slang pretty well because I\'m prompting Whisper with our taxonomy, but Whisper does not know who is who.

**\
Lena Zhukova** 18:40\
Right, right.

**\
Clayton Chancey** 18:40\
Because it\'s just it\'s just audio. So now I need to actually I take that good transcription but bad diarization and now I I give that good transcript plus the bad transcript from Microsoft Teams which does not translate very.\
Accurately, but it knows who is who and when they are speaking. I can give those both in.

**\
Val Levitan** 19:03\
It has a. It has a it. It has a stamp. It it translates the stamp.

**\
Clayton Chancey** 19:07\
Yeah, as a timestamp and the Microsoft Teams like username and you know, the identity is it knows where all of those audio streams are coming from because Teams is the platform. And so this becomes the pattern. It\'s like we will redo the transcription ourself.

**\
Val Levitan** 19:13\
Yeah.

**\
Clayton Chancey** 19:25\
And then we will take whatever the platform\'s, you know, transcript is, yeah, and then kind of stitch them together through Claude. That\'s a small Claude process that runs and on the end it spits out a a reorganized, reoptimized transcript. And the nice thing about this is that by using Claude.

**\
Val Levitan** 19:29\
stamps.

**\
Clayton Chancey** 19:44\
We can also prompt it in any way we want. Like we could add something custom which says like, you know, this is a game dev context specifically. Oh, and make sure that you pull down this GitHub taxonomy or and so on and so forth. So it gives us flexibility to inject.\
The subtext as needed.

**\
Val Levitan** 20:04\
And and how do you configure the MCP? Do you configure it for Co work or for code or for for both like what? What can I have the access with?

**\
Clayton Chancey** 20:17\
Well, that that\'s the question I wanted to. I needed to get the document from Lena, the actual Microsoft Teams transcript to test the pipeline, which is what we\'re doing here. Then this it\'s a Python script. This can become an MCP.\
There is a new convention for MCP called the MCPB, which lets you create a single. It\'s crazy, it lets you create a single file and then you can give that one file to any user and that user just drops it.\
Into Cloud Desktop or Cloud Cowork or Cloud Code and MCP works, it uploads. So that that\'s what I would do. It\'s the easiest way to deploy it to you guys is to just give you this single MCPB file and then it and then it just loads.

**\
Lena Zhukova** 21:06\
Well.

**\
Val Levitan** 21:08\
But, but hold on a second. How will it work long term? Because we\'re having multiple meetings per day and these meetings are just blah, blah, blah, blah, blah. And the next meeting is the next meeting and the next meeting and we want to gain speed, right? We want to have these meetings.

**\
Clayton Chancey** 21:12\
Mm.\
Yeah.

**\
Val Levitan** 21:25\
So we want to time stamp them based on UTC plus your current time zone. But going back to UTC, so we understand the priority, which discussions took place first, we want to have a central repository of the sources for intelligence. I\'m specifically not calling them intelligence.

**\
Clayton Chancey** 21:29\
Mhm.\
Yeah.\
Yeah.

**\
Val Levitan** 21:45\
But then we want to extract this and from there we want to derive depending on who converses on what subject. But what do we want out of it? We want the ADRS. We want.

**\
Clayton Chancey** 21:46\
Yeah.

**\
Val Levitan** 22:02\
Source potential RAQs, requirements, potential capabilities. We then want to point to our ways of doing things and automatically attempt to create RAQs and capabilities.

**\
Clayton Chancey** 22:14\
Hey.

**\
Val Levitan** 22:20\
And then a breakdown into features based on our ways of business. That\'s the.\
Uh, short, long term.\
Play on word agenda or objective. So where where are we keeping all of this? Where is the repository for this?

**\
Clayton Chancey** 22:33\
Yeah.\
Yeah.

**\
Val Levitan** 22:42\
GitHub cannot be a repository, obviously.

**\
Clayton Chancey** 22:42\
Well, it will be GitHub at the end of the day.\
Wait, why not?

**\
Val Levitan** 22:50\
Well, files are large, many accumulates quickly. We know that it has to be in the cloud. Currently we use Azure.\
We really don\'t need version control in it.

**\
Clayton Chancey** 23:03\
Oh well, well, I think I\'m thinking GitHub is the is the repository for the final generated correct transcripts, which which are not large, they\'re small.\
I think this is a very very small text file.

**\
Val Levitan** 23:21\
Why? Why do we? Why do we need the final? We we need, we need an extraction from the final. Everything else could be kept as a in in the storage we we just need. We just need to pull things that we need to pull and the rest.\
Needs to address to some, you know, chronological.\
Source for a permanent knowledge base. The knowledge base. The knowledge base itself needs to get into GitHub, but knowledge base is, you know, eventually it will trickle down to 2%.

**\
Clayton Chancey** 23:47\
Yes.

**\
Val Levitan** 23:59\
Off.\
You know, filter down to something very small and we increment GitHub with the knowledge base.

**\
Clayton Chancey** 24:03\
Well, this.\
Yeah, well, we\'re sort of talking about two different things here. So first, so let me.

**\
Val Levitan** 24:11\
We are.

**\
Clayton Chancey** 24:17\
Without.\
Wasting too many words on all my thoughts about all this, because I do have thoughts about all this. But I think on the one side is what we\'re doing here, which is I I see this as like it\'s a microservice. Like you said, it\'s a little processing pipeline.\
That lets us take a meeting which happened with its audio and it\'s kind of bad transcript and improve it in a very organization specific way and then out of that pipeline comes.\
A new transcript and anyone can use this. I can use it through an MCP. I can make it an API so that Microsoft admins at JPL can consume this as a service and I can also run it on a schedule.\
So that anytime a meeting takes place in Microsoft Teams, this pipeline transforms the transcript and then puts it out somewhere. So that\'s kind of what I\'m working on just in this small world, but it\'s part of a bigger picture, which is now what you\'re talking about.\
Which is where does that transcript that is improved, let\'s call it the improved transcript. Where does this improved transcript go and what\'s the right way of storing it so that it can be used for business intelligence and.\
And the enterprise brain, the knowledge base, that second question, yeah.

**\
Val Levitan** 25:41\
Just just just one correction. The improved transcript is not knowledge base.

**\
Clayton Chancey** 25:45\
Mhm.\
Correct.

**\
Val Levitan** 25:50\
It just improved source of.

**\
Clayton Chancey** 25:56\
Yeah.

**\
Val Levitan** 25:56\
Filtering.

**\
Clayton Chancey** 25:58\
Yep.\
But.\
In you know, this is not true of an old traditional knowledge base, but I think in the A I era it is true that source material.\
Needs to be stored and referenceable to the to the knowledge base because.\
Every new iece of source material does ultimately change and update the groundings.\
And.\
Mental model, if we could say, of the knowledge base. So an AI that\'s consuming our knowledge base. Let\'s say that the knowledge base is, you know, an abstracted, opinionated.\
Filtering of these original sources. And so there\'s probably going to be much discussion and disagreement and and misinformation in the transcripts in the sources. And we don\'t want all of that in the knowledge base because it contradicts itself and so we we.\
We align or filter or decide on what is the truth, the ontological truth that we are moving forward with and this goes into the knowledge base and the knowledge base will have information that probably person ABC and D disagreed with many times over many months and that is all in the transcripts. But that\'s not the truth and so the truth.\
This is different from the record of conversation, but an AI should have the ability to to distinguish between those, but to reference both because I think the knowledge base.\
If if someone says.\
In a new meeting. Now a new meeting happens and someone says we talked about this. I thought we agreed that we were not doing A. We are doing B instead. What are you guys talking about now? How does the knowledge base as we get this meeting, this transcript, as we get this idea?\
Idea into this living knowledge base. How do we interpret this reference to the past or to disagreement without having to manually research and figure it out? The AI needs to access those records.

**\
Val Levitan** 28:29\
Or or not?\
Oh.\
Absolutely. And I and I fully agree that even if a discussion would take between, you know, 10 smartest people in the room, they would not necessarily have the same truth.

**\
Clayton Chancey** 28:46\
Yeah.\
Right, right.

**\
Val Levitan** 28:51\
And walk away with the same truth. Even if they had an obligation to come with a single decision, they probably wouldn\'t. And the more smart people I have in the room, the less chances I have to come up with uniform truth.

**\
Clayton Chancey** 29:09\
Yeah, Yep.

**\
Val Levitan** 29:10\
So, so absolutely the reference or a reference to sources is required.

**\
Clayton Chancey** 29:19\
Yeah.

**\
Val Levitan** 29:19\
But as long as we\'re making a distinction between sources and what we are considering for the time being being the truth should and that truth should be kept in GitHub because we can revision.

**\
Clayton Chancey** 29:28\
Mhm.

**\
Val Levitan** 29:35\
Truth as the time passes and revision we can we can evolve it, but not necessarily in the right direction as we can we assume the truth.

**\
Clayton Chancey** 29:36\
Yes.

**\
Val Levitan** 29:49\
Or direction of the truth is we could reverse our truth into something else.

**\
Clayton Chancey** 29:57\
Yeah, yeah.

**\
Val Levitan** 29:57\
But Oh yeah, I I absolutely believe that full revised transcript should be accessible by AI and should be treated as the original source of truth.

**\
Clayton Chancey** 30:08\
Mhm.

**\
Val Levitan** 30:12\
Versus revised source of truth.

**\
Clayton Chancey** 30:16\
Yeah, yeah.\
And and I think that should be GitHub too.

**\
Val Levitan** 30:22\
Yeah, but I don\'t know how big that is. I mean, I don\'t want to turn GitHub into a storage room.

**\
Clayton Chancey** 30:31\
Well, I think, yeah, but it\'s a good call. Maybe the operational knowledge that I am coming with is that.\
We we would not need to store the audio files or the Microsoft doc. You know, Teams transcripts all we need to store.\
Is this markdown files that come out which?

**\
Val Levitan** 30:55\
And they\'re micro small.

**\
Clayton Chancey** 30:56\
Let me see if yeah, I\'m trying to find out the exact size here. I don\'t even remember how to get this info, but.

**\
Val Levitan** 31:01\
Yeah, they they\'re usually 22K between 2 and 10K.

**\
Clayton Chancey** 31:04\
Yeah, yeah. I mean it\'s it\'s like you would have to have a million plus words and a mega novel, you know something to to get to 1 MB. So it, I mean it\'s optimized for storing in GitHub. I think it should be OK.

**\
Val Levitan** 31:20\
Yeah, OK.\
OK. OK. OK. I see your point. Yeah. OK. I agree.

**\
Clayton Chancey** 31:29\
So Lena, let me send you this, but also let\'s look through it here together. Because if this, if this is good, great. If it needs some improvement or there\'s nuance, then let\'s work on it. But like, this is the kind of transcript that\'s coming out after transcribing the audio.

**\
Lena Zhukova** 31:43\
But why it\'s translated? Why it\'s translated? Because I used the fixed but still in Russian meeting notes when I sent prompt to UMCP.

**\
Val Levitan** 31:59\
Because the best programming language on Earth today and rapidly developing to become a such programming language, digital programming language is English.

**\
Clayton Chancey** 32:05\
Yeah.\
Yeah, yeah.

**\
Lena Zhukova** 32:13\
Uh, true. But the interesting that uh remember like we discussed that it\'s better to prompt uh quote with your native language and when uh phrases are like uh build like in your native language.

**\
Val Levitan** 32:22\
Correct.\
Correct. Because your lexicon, your your ability to express yourself, is not developed sufficiently enough in your foreign language. It needs to be in your mother tongue because you\'re not. Well, not you, but you know somebody who\'s not.

**\
Clayton Chancey** 32:26\
Yeah.\
Well, that, yeah.

**\
Val Levitan** 32:45\
English free.\
Is they\'re having issues with expressing themselves and therefore the prompts become butchered.

**\
Clayton Chancey** 32:47\
Yeah.\
Yeah.\
Yeah, it\'s an issue with the prompting, not with the the the eye, the A I\'s ability to to read or translate, yeah.

**\
Val Levitan** 33:05\
But the output must be in English, because that\'s your programming language.

**\
Lena Zhukova** 33:11\
OK.

**\
Clayton Chancey** 33:11\
And but also that\'s why I had prompted Claude that like in certain cases where we run across a word which is maybe part of the taxonomy or if Claude feels I I use this language as if it\'s feeling something, but where Claude decides that.\
There\'s a word which we should like note the the exact phrase that was used in the transcript and it will it will do it like this like use like it\'s translating the word IP and then it\'s adding like the you know the phonetics.

**\
Lena Zhukova** 33:40\
Uh huh.\
But yeah, since this I find unnecessary because it it spoils everything because it was good like IP459. It\'s a good lead to your MCP to your Jere MCP and now somehow we have this under.

**\
Clayton Chancey** 33:45\
I.

**\
Lena Zhukova** 34:00\
We don\'t need this IP in Russian because.

**\
Clayton Chancey** 34:02\
Well, well, the reason that this, the reason that this helps, Lena, is because if any of your other devs who maybe are not as fluent in English as you are now coming in and prompting Claude in Russian, which we\'re saying you should.\
Do that because that\'s actually how you\'re going to express exactly what you want. Then now this is a mapping.

**\
Lena Zhukova** 34:25\
But this word they they they would never use in Russian. They would put like IP Swiss number in English. So that\'s why I\'m asking this. This was not very smart to use exactly this word in in Russian.

**\
Clayton Chancey** 34:29\
OK.\
OK, OK.\
OK, OK. Well, that\'s that\'s good to know. Then we can, I can tweak the pipeline and say to Claude, you know what, don\'t don\'t provide these mappings.

**\
Val Levitan** 34:46\
No, no, no, no, no. Let\'s no, no, let\'s not do that because I\'m not sure that the developers will remain Russians. We we\'re, you know we\'re actively attracting non Russian speaking people and we\'re we\'re.

**\
Clayton Chancey** 34:56\
OK.

**\
Val Levitan** 35:02\
You know, actively looking at diversification of knowledge.

**\
Clayton Chancey** 35:09\
OK.

**\
Val Levitan** 35:10\
So let\'s let\'s keep output in precisely literate, grammatically correct English.

**\
Clayton Chancey** 35:18\
OK, I think that\'s what Lena\'s saying too, I think is let\'s keep it this. But like in this, in these cases I I I intentionally asked Claude, hey, add the add the term that was used that was transcribed, which is sort of like.

**\
Val Levitan** 35:36\
Oh, yes, yes.

**\
Clayton Chancey** 35:37\
So what Lena is saying and what you are saying, what I hear is get rid of this like it should just be that.

**\
Lena Zhukova** 35:43\
Yeah, I would get rid because even if somebody will write prompt in Russian to quote, they will will use word spine like name of the program in English or IP. They will put IP like English letters and number of IP.

**\
Clayton Chancey** 35:53\
Mhm.\
OK, OK.

**\
Val Levitan** 35:58\
Right, right. I didn\'t understand that. Sorry. Yeah. Thank you for clarification.

**\
Clayton Chancey** 36:01\
No, that that makes sense. That makes sense to me. OK, I will. I will update that. Let me actually just get Claude working on this now and then I will send you guys.\
I\'ll send you this transcript, Lena. I I want to keep reading through it here just to make sure it\'s accurate because we we have time. We can do it now, but let me get Claude working as well really quick.

**\
Lena Zhukova** 36:17\
OK.\
Yeah, yeah.

**\
Clayton Chancey** 36:25\
What to update the pipeline post processing?\
Be a quad so that the transcript does not include the annotated transliterations.\
But outputs the English translation only. Here are some examples of what I mean and then.\
Not do.\
And I\'ll say.\
From uh, call one.\
And then I will find another one.\
It\'s really only OK, and then I\'ll do that third example here.\
Um.\
And then I want to try something else interesting. Please update the pipeline accordingly. Then run the entire thing again. I would like you to run and generate.\
A new independent output so that we can compare call with game uh dev maze.\
One transcript of empty to the new output and understand how closely aligned they are. This should give us a sense of how probabilistic versus.

**\
Val Levitan** 38:25\
OK.

**\
Clayton Chancey** 38:42\
Deterministic our pipeline truly is.\
OK, while Claude is working on that, I would love to let me send this to you first so that you have it in case we, you know, run out of time. But then I would love to sort of spot check this. So let me.

**\
Lena Zhukova** 38:56\
Mhm.

**\
Clayton Chancey** 39:03\
Send this to you.\
Um, upload from my device.\
Uh, where are we? There\'s so many projects.\
I thought originally that if my desktop was just a place where I only stored the rojects that I\'m sort of working on now, it would be fine. But now there\'s so many of them that.

**\
Val Levitan** 39:32\
Yes.

**\
Clayton Chancey** 39:34\
That makes sense. So I sent that to you. Um.\
Let me just Scroll down a little bit and say something like.\
The things that I\'m looking for really are the speaker attributions. Like I don\'t know if you remember or not, but like are these are these correct? Is this is this good?

**\
Lena Zhukova** 39:59\
I remember, yeah. So what I overlooked like for now seems correct. I remember very good this meeting so I can validate it.

**\
Clayton Chancey** 40:08\
OK.\
OK, so I sent you that.\
Um.

**\
Lena Zhukova** 40:31\
Mm-hmm.

**\
Clayton Chancey** 40:32\
I hope that these are all like like for example this sentence here. In the main game, like all other SD2 games, we\'ll have information about the gold nugget, jackpot, progressive. Oh cool. OK, OK, well I\'ll well then. OK, so good. I will ask you to spot check that.

**\
Lena Zhukova** 40:42\
Yeah, it\'s everything is correct. Yeah, yeah, yeah.

**\
Clayton Chancey** 40:52\
Or not spot check, but to completely validate that.

**\
Lena Zhukova** 40:52\
Mhm.\
Yeah, I will. I will do like complete politician.

**\
Clayton Chancey** 40:58\
And then what I will do is.\
Um.\
I\'ll do a few things, so I will wire this process up so that it can be in and it has an API.\
This also lets me make it into an MC.\
You know what? Let me just dictate my next steps here live and then put it into my plan document. This would be, I think, better.\
Uh.\
I am. While you are doing that, this is just to help me line up my tasks so that cause I have a busy day today so that I can just not have to come back and figure myself out later. So while you\'re doing that I am going to describe some next steps.\
I will provide the transcript of my call today with Lena and Val for you to augment these next steps, but here they are.\
And I\'ll say please uh create a new dot MD file in our reference subdirectory with these uh documented.\
So my understanding is validate the.\
Or I\'ll say yeah.\
I have sent Lena the.\
Outputs of our pipeline or in-depth validation, but our spot check look good to her.\
Yeah, currently running.\
A multi run validation to determine the deterministic probabilistic.\
How do I spell?\
This of the pipeline.\
After this we need to package this pipeline as a microservice.\
Which oh, actually that\'s what I wanted to document is the actual next step is.\
Three, we need to update the pipeline to pull down or reference the linguistic glossary taxonomy info from a.\
Living GitHub repo as opposed to our static Excel document. I will provide more info on this repo. We can build that into our pipeline.\
After this we need to package this pipeline as a microservice which will allow JBL to consume and deploy it in all the useful ways.\
Without dependencies.\
1st we will create an API for our pipeline.\
Allowing users to users or AI agents to send parameters and receive back an improved transcript.\
With the API in place, we will wrap that API in the form of an MCP server and deploy the MCP server as an MCP dot MCPB.\
File for ease of installation and maintenance.\
And then with the API and MCP in place, we will coordinate with Andre from JBL IT to gain.\
Microsoft Graph API.\
Secrets and deploy this microservice.\
As an automatic post processing pipeline for all JPLMS teams meetings that were recorded.\
The output of this will be.\
Improved transcripts.\
In a dedicated GitHub structure that is TBB but will serve as a appendix repo for a GitHub enterprise.\
Knowledge management system.\
OK, that\'s sort of my.

**\
Val Levitan** 46:40\
Please, please, please look at my chat.

**\
Lena Zhukova** 46:53\
On uh.

**\
Clayton Chancey** 46:57\
OK.

**\
Lena Zhukova** 46:57\
I also see one problem here already like I started to read this transcript like participants. So part of them are participants up to Spike 30 and then after that it\'s very strange like extraction from our taxonomy.

**\
Clayton Chancey** 47:04\
Mhm.\
Yeah.\
Yeah.\
Yeah.

**\
Lena Zhukova** 47:17\
Call.

**\
Clayton Chancey** 47:18\
Yeah, you\'re right. It gets participants and terms mixed up, which is probably.

**\
Lena Zhukova** 47:22\
The connection is they\'re not all participants here. Again, this all list that they added to taxonomy vocabulary to connect them to their code names. Like for example like Vladimir Avdev is black, like when in I spoke in Russian. So he wasn\'t a participant in this meeting. Actually we mentioned him, but he was.

**\
Val Levitan** 47:24\
And.

**\
Lena Zhukova** 47:42\
Not a participant.

**\
Clayton Chancey** 47:42\
Oh, OK, OK, then that\'s good. OK, so this is probably claw prompting. Let me add this as a note here as well.\
Um.\
Um.\
Uh, our spot check looked good except for one noticeable strangity. Is that a word?\
This is the kind of thing that is like, I I\'m pretty sure this is not an English word, but it\'s an English like word and I, you know, we want people to feel free to sort of just like express and this, you know, to be able to do that in other languages too.\
Um.\
So the noticeable strains of this is that the participants section includes terms which are of course not actual people participating in the meeting.\
And includes people which were mentioned in conversation.\
But who were not actual attendees? I suspect this is a artifact of how we are running our claw post processing.

**\
Lena Zhukova** 49:38\
From other side when I now like see the whole like meeting text it like breaks properly like what Julia says, what Anastasia said or Dima said or Lena said is this is this everything this is correct but least of participant was surprisingly.

**\
Clayton Chancey** 49:51\
Mm-hmm.\
Right.

**\
Lena Zhukova** 49:58\
Very strange.

**\
Clayton Chancey** 49:59\
Right. Yeah, I know. I actually, I think this is Claude part. Part of what I we ask Claude to do for post processing is is to sort of line up the ontology of all of the people and places and things and stuff that\'s a reference which could have any.\
Nuance. It could be referenced in Russian, but in in a way that we need to like translate appropriately. And I think what it\'s probably doing is it\'s just adding us all to this participant section because this section is hard, hard-coded defined.\
So I need to give Claude a little bit more freedom to do that, but that that I can fix that is easy. What would concern me is if the actual transcription of the text was problematic or was incorrect, that would be that would be now a step a step back. We have to figure something out, but this participant section is.\
Um, it\'s super easy to change.

**\
Lena Zhukova** 51:00\
OK, some name of the games also was not interpreted correctly. Like instead of fortune for four, it just say fortune #4. Interesting that using this tool bus scribe I got better results with name.

**\
Clayton Chancey** 51:01\
OK.

**\
Lena Zhukova** 51:20\
So it actually like understood like correctly as a singlish fortune. So it it\'s great. I know it\'s not an easy because it again it\'s mix English and Chinese and now it\'s mixing with Russian, but Dulbascribe did a good job with this.

**\
Clayton Chancey** 51:34\
Yeah.\
OK, all right, cool. Yeah, see it says on item one, the participants fix is that our output formatter pulls from the get. So it was like I was saying basically that section is hard coded. Claude is not coming up with it.\
Um, and it should instead use the speakers names like yes, please update that.\
OK.

**\
Lena Zhukova** 52:03\
Because the names are interpreted correctly, like as a game names and charms. Yeah, I I will go through it like more like in details, but for now like the transcript itself looks pretty good with some minor issues.

**\
Clayton Chancey** 52:07\
Yeah.\
OK. And then you mentioned.

**\
Lena Zhukova** 52:20\
Uh, video. Yeah, very good result, I would say.

**\
Clayton Chancey** 52:24\
Thank you. So you mentioned that tomorrow you have a meeting as well. It\'s not maybe related to this. Send me the audio and the Microsoft Teams transcript and then if we now have, if we have two different meetings and we can get a good transcript out of both of those, then I will consider it to be.

**\
Lena Zhukova** 52:28\
Yeah, I will send you a record, yeah.\
Mhm.

**\
Clayton Chancey** 52:43\
Good enough to fully automate and I can work on all of the other stuff that I mentioned in my prompt here around the next steps for interacting with GitHub and packaging as a microservice and getting ready for the enterprise brain piece. This is all pretty fast and easy to do because Claude can just do it.\
For me, as long as the logic about transcription is reliable. If we try the second meeting, which you\'re going to have tomorrow, and actually the transcription is kind of bad, then we would need to rework something. So I want to get that pipeline just perfect. Sounds like it\'s close, but let\'s just validate.

**\
Lena Zhukova** 53:18\
Uh huh.\
OK, let\'s do it. And I have one more comment about MCP which we forgot to discuss for now like it works well with images only if they are in desktop and while it was pretty convenient for me with to to working with this issues for this.

**\
Clayton Chancey** 53:22\
So we update it with one more meeting and then we can we can deploy it basically.\
It.\
Yeah.

**\
Lena Zhukova** 53:42\
This one game drag and paste which we are going to start production. In other cases it could be very inconvenient because we can discuss for example several projects and what what should I do? I should like dump all my images in desktop. It\'s it\'s not very good.

**\
Clayton Chancey** 53:49\
Yes.\
Yeah, I actually had a thought or question about this. Um, let me stop sharing.\
Somehow am I? Am I sharing my screen right now? Do you guys see my screen? Oh, I have been sharing for. I thought I was sharing for a while, but.

**\
Lena Zhukova** 54:13\
Now.

**\
Val Levitan** 54:18\
You have been and then you turned it off.

**\
Clayton Chancey** 54:20\
OK, good. All right. I need more copy clearly. But Lena, I was hoping that you could share your screen and go to Claude Cowork because I wanted to see if it would if if we could actually select a folder in the D drive.

**\
Lena Zhukova** 54:30\
Oh.

**\
Val Levitan** 54:36\
OK.

**\
Clayton Chancey** 54:37\
As a folder for Claude Cowork to work on, this is just an idea I had thought. Oh, maybe that would actually help because then this solves it.

**\
Lena Zhukova** 54:38\
OK.\
So yeah, I worked. Yeah, this one. Yeah, I worked in, in, in, in cohort and.

**\
Clayton Chancey** 54:50\
So just start like start a new task in cowork for example.

**\
Lena Zhukova** 54:52\
And that.

**\
Clayton Chancey** 54:56\
And then click the work in a folder. Now can you if you click choose a different folder, can you get to the D drive from here?

**\
Lena Zhukova** 55:04\
I could not, but maybe now it\'s it\'s it\'s it\'s changed.

**\
Clayton Chancey** 55:09\
So just I mean the main point is just to see if we could get somewhere in there and if it has images there. So I guess just try just try something and see.\
And the idea would be to pick the top most folder so that you get access to all the others. Uh yeah.

**\
Lena Zhukova** 55:28\
No, she it\'s immediately. It\'s the same problem I had before.

**\
Clayton Chancey** 55:34\
OK, so it\'s that error is actually very informative that that is the on.

**\
Lena Zhukova** 55:36\
He he only counts my home directories desktop.

**\
Clayton Chancey** 55:40\
Yeah.\
Windows. Yeah, I think that will be a thing for anthropic to figure out. I actually now have a pathway to influences a little bit more because I got finally after much ado.\
Accepted as an anthropic partner. So like my organization, it\'s usually too small. I think they\'re only partnering with organizations that are like at least 1000 employees for now. I I think that, you know, so my application to partner with anthropic got rejected due to size, but then I don\'t know what happened.\
A few days later I got the e-mail that actually they are proceeding with the partnership. So now I have like some technical contacts as a result of that. So this would be one thing that for me would be just like.\
It\'s great. None of us on this call can influence it. The only people who can influence it are anthropic. They can change or update the way that the Linux container within Cloud Kowork interacts on a Windows machine. And I mean that this.\
This is a clear example of it kind of breaks the function of Claude Cowork because actually you have files which are available from your machine even though they\'re not hosted there and Claude Cowork can\'t access it because of a sort of arbitrary firewall restriction, so.\
I will try to talk my it\'s a long-winded way of saying as I\'m thinking about it live that I will try to talk with some people at anthropic about this and see if there\'s any like if if they know this and have a a road map item or can quickly solve it, then that would be great because it will be.\
Probably a bit more technical. It\'s it\'s it\'s quite a technical problem to solve for us to try and do that ourselves because we\'re working around a feature problem in Claude. So let me see if I can.\
Maybe have any influence with them first and then and then we can see what we have to do.

**\
Val Levitan** 57:57\
Can we define a clear agenda for the next meeting?

**\
Clayton Chancey** 58:02\
Yeah, the next meeting we should have a a beta pipeline for the improved transcript subprocess or microservice and we should we should be able to test that and deploy it.

**\
Val Levitan** 58:19\
What does it mean? Can can you be a little more definitive? What does beta pipeline mean?

**\
Clayton Chancey** 58:27\
It means there should be a API and an MCP server that can find a Microsoft Teams meeting and then improve the transcript to be good enough to create a game with the other tools that we\'ve already.\
Uh, we\'ve already built together so.\
So in other words, Lena\'s pipeline of getting a meeting transcript and creating a game from it, we should be able to like fully do that because the actual original transcript is now improved and good enough to do that. So we can test that without having the transcript piece wired up to.\
To the entire JVL enterprise system yet that would be what I think we can do by the next meeting is is have it in beta where it works for Lena and it\'s sort of deployed and running for her and then if that\'s working well then we know it\'s reliable enough to then go in and promote as a.\
JVL service which can be consumed and run on a schedule through the Microsoft Automation platform.

**\
Val Levitan** 59:36\
And did I understand correctly that currently we record in two sources, one is teams and another one is just an outside audio file of some sort?

**\
Clayton Chancey** 59:52\
That audio file is is from Teams, so Teams records that file.

**\
Lena Zhukova** 59:55\
It\'s from teams. It\'s extracted from teams. Uh, week area.

**\
Clayton Chancey** 59:59\
Yeah.

**\
Val Levitan** 59:59\
OK, and how do you extract that audio file? Is it a process through prompting?

**\
Clayton Chancey** 1:00:05\
It\'s through the Microsoft Graph API is what we would need to do and what Lena is doing right now for our testing is she\'s going to Microsoft Teams and downloading it and giving it to me.

**\
Lena Zhukova** 1:00:06\
No, I I.\
Yeah, I just extracted it through VLT player video.

**\
Val Levitan** 1:00:17\
I see that.\
I understand, but but all we\'ll have to supply is that teams file and then there will be a process that internally extracts that audio file.

**\
Clayton Chancey** 1:00:21\
Mhm.\
But.\
Well, yes. So my my end goal is once we get the actual, like we need the actual process of improving a transcript and using it to create a game. Once this is dialed in and it\'s working well, then I can go to Andrei with my finalized list of like, hey, here are the scopes I need and here\'s where we\'re going to wire this.\
I don\'t want to do that like 50 times and it will be like much back and forth until we line this up. But if we line this up, it\'s working for us. Then I can go to Andre and say, hey, let me get an hour of your time and we\'ll do this together. We\'ll wire it up and now it becomes available as like an automated process where when a Microsoft.

**\**
1:01:11\
Mhm.

**\
Clayton Chancey** 1:01:12\
Teams meeting is scheduled and it is automatically recorded. Then this improver process runs automatically and that way Lena has access to the improved transcripts through this GitHub repository. Now this becomes like a pain free way to access that where you don\'t have to manually.\
Invoke it every time and remember to do that, but that requires integration with Andre and that requires us to to finalize the the actual process which we\'re trying to accomplish first so that we don\'t have much and much back forth back and forth with.\
With it.

**\
Val Levitan** 1:01:52\
May I please have the recording of this meeting put back in the chat here whenever.

**\
Clayton Chancey** 1:01:56\
Yeah, sure. I think it it. I think it goes to the chat like the previous one. I saw that you asked for it and it was above in the chat for me.

**\
Val Levitan** 1:02:02\
Mhm.\
I I I asked for it. I asked for it. But all it provides is the summary unless you physically put put the transcript in here. So would you please? Yeah, physically just put the transcript. I got to go. So yeah, thank you.

**\
Clayton Chancey** 1:02:12\
Oh.\
Let me yes.\
So so when you but so when you scroll up you don\'t see like this like this is where you said please share the recording but it has.

**\
Val Levitan** 1:02:27\
Yes, yes, only only you have access to. I mean I have access to transcript on screen. I can see it on screen, but I cannot download it and I cannot put Claude on it.

**\
Clayton Chancey** 1:02:32\
Oh.\
Sure.\
Oh, OK. All right. Well, let me change the permissions for the moon. Yeah.

**\
Lena Zhukova** 1:02:41\
You know you know what the owner of the meeting can do it. I already uh I I got this problem before him.

**\
Clayton Chancey** 1:02:47\
Oh, OK. All right. That that clarifies. I\'ll change the settings on the on the meeting then. That makes sense. No problem.

**\
Val Levitan** 1:02:54\
Thank you.

**\
Clayton Chancey** 1:02:56\
Thank you guys very much and thanks for the extra time. Have a great rest of your day.

**\
Lena Zhukova** 1:02:58\
Thank you very much.

**\
Val Levitan** 1:02:59\
And and and next meeting is when?

**\
Clayton Chancey** 1:03:03\
Tuesday.

**\
Val Levitan** 1:03:04\
Tuesday. Thank you. Bye.

**\
Clayton Chancey** 1:03:05\
Yep. Bye.

**\
Lena Zhukova** 1:03:06\
Goodbye.

**\
Clayton Chancey** stopped transcription
